---
title: Přiznání k DPH (Německo)
description: Toto téma popisuje, jak nastavit a vygenerovat předběžné přiznání k dani z přidané hodnoty (DPH) pro Německo v oficiálním formátu XML.
author: anasyash
ms.date: 03/10/2022
ms.topic: article
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: anasyash
ms.search.validFrom: ''
ms.openlocfilehash: a761a145a876584728098a92b3f3e93ac718a164
ms.sourcegitcommit: 9c19898e1f41495f804c7f07e2636b53a098c4c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/10/2022
ms.locfileid: "8402796"
---
# <a name="vat-declaration-germany"></a>Přiznání k DPH (Německo)

[!include [banner](../includes/banner.md)]

Toto téma popisuje, jak nastavit a vygenerovat předběžné přiznání k dani z přidané hodnoty (DPH) pro Německo v oficiálním formátu XML. Toto téma také vysvětluje, jak zobrazit náhled přiznání k DPH v Microsoft Excel.

Chcete-li automaticky vygenerovat sestavu, vytvořte dostatek kódů DPH, aby bylo možné vést samostatné účetnictví DPH pro každé pole na předběžném přiznání k DPH. Navíc v parametrech specifických pro aplikaci ve formátu elektronického výkaznictví (ER) pro předběžné přiznání k DPH přidružte kódy DPH k výsledku vyhledávání pro pole v přiznání k DPH.

Pro Německo musíte nakonfigurovat **Vyhledání pole sestavy**. Další informace, jak nastavit parametry specifické pro aplikaci, najdete v části [Nastavení parametrů specifických pro aplikaci pro pole přiznání k DPH](#set-up-application-specific-parameters-for-vat-declaration-fields) dále v tomto tématu.

V následující tabulce sloupec „Výsledek vyhledávání“ zobrazuje výsledek vyhledávání, který je předkonfigurován pro konkrétní řádek přiznání k DPH ve formátu přiznání k DPH. Tyto informace použijte ke správnému přidružení kódů DPH k výsledku vyhledávání a poté k řádku přiznání k DPH.

### <a name="vat-declaration-overview"></a><a name="vat-declaration-overview"></a>Přehled přiznání k DPH

Předběžné přiznání k DPH v Německu obsahuje následující informace.

**SEKCE – DODÁVKY A DALŠÍ SLUŽBY**

**Zdanitelné prodeje**

| Řádek | Pole - základ daně | Pole - částka daně | Popis                                                                                                                                      | Výsledek vyhledávání                                                                             |
|-----|----------------|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| 20  | 81             | Bez kódu     | Zdanitelný prodej se sazbou daně 19 procent.                                                                                                       | 20-TaxableSalesStandard</br>73-BadDebtsWriteOffStandard (81/50) – se znaménkem mínus             |
| 21  | 86             | Bez kódu     | Zdanitelný prodej se sazbou daně 7 procent.                                                                                                        | 21-TaxableSalesReduced</br>73-BadDebtsWriteOffReduced (86/50) – se znaménkem mínus               |
| 22  | 35             | 36               | Zdanitelné prodeje za jiné daňové sazby.                                                                                                                | 22-TaxableSalesOtherRates</br>73-BadDebtsWriteOffOtherRates (35/36/50) – se znaménkem mínus      |
| 23  | 77             | *Žádná částka daně*  | Dodávky od zemědělských a lesnických podniků v souladu s §24 německého zákona o DPH (UStG) zákazníkům, kteří mají DIČ. | 23-EUSalesAverageRate24</br>73-BadDebtsWriteOffEUSalesAverageRate24 (77/50) – se znaménkem mínus |
| 24  | 76             | 80               | Prodeje, ze kterých je třeba zaplatit daň podle § 24 UStG (pilařské výrobky, nápoje a alkoholické nápoje).                                | 24-SalesAverageRate24</br>73-BadDebtsWriteOffSalesAverageRate24 (76/80/50)                    |

**Prodeje osvobozené od daně s odpočtem daně na vstupu**

| Řádek | Pole - základ daně | Pole - částka daně | Popis                                                                       | Výsledek vyhledávání                       |
|-----|----------------|------------------|-----------------------------------------------------------------------------------|-------------------------------------|
| 26  | 41             | *Žádná částka daně*  | Dodávky uvnitř Společenství zákazníkům, kteří mají DIČ.                       | 26-EUSales                          |
| 27  | 44             | *Žádná částka daně*  | Dodávky nových vozidel v rámci Společenství kupujícím, kteří nemají DIČ.    | 27-EUSalesNewVehicles               |
| 28  | 49             | *Žádná částka daně*  | Dodávky nových vozidel uvnitř Společenství mimo společnost.                     | 28-EUSalesNewVehiclesOutsideCompany |
| 29  | 43             | *Žádná částka daně*  | Ostatní prodeje bez daně, které mají odpočet daně na vstupu, jako jsou vývozní dodávky. | 29-ExportOtherTaxFreeSales          |

**Prodeje osvobozené od daně bez odpočtu daně na vstupu**

| Řádek | Pole - základ daně | Pole - částka daně | Popis                                            | Výsledek vyhledávání                           |
|-----|----------------|------------------|--------------------------------------------------------|-----------------------------------------|
| 30  | 48             | *Žádná částka daně*  | Prodej bez daně, který nemá odpočet daně na vstupu. | 30-TaxFreeSalesWithoutInputTaxDeduction |

**Intrakomunitární pořízení**

| Řádek | Pole - základ daně | Pole - částka daně | Popis                                                                                                                   | Výsledek vyhledávání                                                    |
|-----|----------------|------------------|-------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| 33  | 91             | *Žádná částka daně*  | Nezdaněné intrakomunitární pořízení některých předmětů a investičního zlata.                                                    | 33-TaxFreeEUPurchase                                             |
| 34  | 89             | Bez kódu     | Zdanitelná intrakomunitární pořízení se sazbou daně 19 procent.                                                             | 34-EUPurchaseStandard</br>34-UseTaxEUPurchaseStandard (89/61)        |
| 35  | 93             | Bez kódu     | Zdanitelná intrakomunitární pořízení se sazbou daně 7 procent.                                                              | 35-EUPurchaseReduced</br>35-UseTaxEUPurchaseReduced (93/61)          |
| 36  | 95             | 98               | Zdanitelná intrakomunitární pořízení s jinými sazbami daně.                                                                      | 36-EUPurchaseOtherRates</br>36-UseTaxEUPurchaseOtherRates (95/98/61) |
| 37  | 94             | 96               | Zdanitelné intrakomunitární pořízení nových vozidel od dodavatelů, kteří nemají DIČ, v obecné sazbě daně. | 37-EUPurchaseVehicles</br>37-UseTaxEUPurchaseVehicles (94/96/61)     |

**ODDÍL – PŘÍJEMCE JAKO DAŇOVÝ DLUŽNÍK**

| Řádek | Pole - základ daně | Pole - částka daně | Popis                                                                        | Výsledek vyhledávání                                                                                        |
|-----|----------------|------------------|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| 40  | 46             | 47               | Ostatní služby podnikatele na základě zbývajícího území Společenství.        | 40-BeneficiaryTaxDebtor</br>40-UseTaxBeneficiaryTaxDebtor (46/47/66)                                                                              |
| 41  | 73             | 74               | Prodeje podle §13b odst. 2 č. 3 UStG.                               | 41-BeneficiaryTaxDebtorRealEstateTransfer</br>41-UseTaxBeneficiaryTaxDebtorRealEstateTransfer (73/74/67) |
| 42  | 84             | 85               | Ostatní služby podle §13b odst. 2 č. 1, 2 a 4 až 12 UStG. | 42-BeneficiaryTaxDebtorOther</br>42-UseTaxBeneficiaryTaxDebtorOther (84/85/67)                           |

**ODDÍL – DOPLŇUJÍCÍ INFORMACE O PRODEJI**

| Řádek | Pole - základ daně  | Pole - částka daně | Popis                                                                                                | Výsledek vyhledávání                                                                                    |
|-----|-----------------|------------------|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| 48  | 42              | *Žádná částka daně*  | Dodávky prvním zákazníkem v případě intrakomunitárních trojúhelníkových transakcí.                   | 48-DeliveriesFirstCustomerEUTriangular                                                           |
| 49  | 60              | *Žádná částka daně*  | Zdanitelné prodeje provádějícího podnikatele, za které příjemce služby dluží daň. | 49-SalesServicesReverseCharge                                                                    |
| 50  | 21              | *Žádná částka daně*  | Ostatní nezdanitelné služby.                                                                                | 50-OtherServicesNonTaxable                                                                       |
| 51  | 45              | *Žádná částka daně*  | Ostatní nezdanitelné prodeje, pokud místo plnění není v Německu.                                    | 51-OtherSalesNonTaxable                                                                          |
| 52  | *Žádná částka daně* | *Žádná částka daně*  | DPH                                                                                                       | Řádek 20 + řádek 21 + řádek 22 + řádek 2 4 + řádek 34 + řádek 35 + řádek 36 + řádek 37 + řádek 40 + řádek 41 + řádek 42 |

**ODDÍL – ODPOČETNÁ DAŇ NA VSTUPU**

| Řádek | Pole - částka daně | Popis                                                                                                | Výsledek vyhledávání                                                                                                                                                                |
|-----|------------------|------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 55  | 66               | Částky daně ze vstupní faktury od jiných společností, služeb a trojúhelníkových transakcí v rámci Společenství.     | 55-InputTax 40-UseTaxBeneficiaryTaxDebtor (46/47/66)</br>74-BadDebtsWriteOffInputTax (66/37) – se znaménkem mínus                                                                   |
| 56  | 61               | Částky daně na vstupu z intrakomunitárního pořízení zboží.                                           | 56-InputTaxEUPurchase 34-UseTaxEUPurchaseStandard (89/61)</br>35-UseTaxEUPurchaseReduced (93/61)</br>36-UseTaxEUPurchaseOtherRates (95/98/61)</br>37-UseTaxEUPurchaseVehicles (94/96/61) |
| 57  | 62               | Uplatněná dovozní daň z prodeje.                                                                                 | 57-InputTaxImport                                                                                                                                                            |
| 58  | 67               | Částky daně na vstupu ze služeb ve smyslu §13b UStG.                                        | 58-InputTaxServices</br>41-UseTaxBeneficiaryTaxDebtorRealEstateTransfer (73/74/67)</br>42-UseTaxBeneficiaryTaxDebtorOther (84/85/67)                                                 |
| 59  | 63               | Částky daně na vstupu, které se vypočítávají podle obecných průměrných sazeb.                                  | 59-InputTaxAverageRates</br>74-BadDebtsWriteOffInputTaxAverageRates (63/37) – se znaménkem mínus                                                                                    |
| 60  | 59               | Odpočet daně na vstupu u intrakomunitárních dodávek nových vozidel mimo společnost a malé podniky. | 60-InputTaxEUPurchaseNewVehicles</br>74-BadDebtsWriteOffInputTaxEUPurchaseNewVehicles (59/37) – se znaménkem mínus                                                                  |
| 61  | 64               | Oprava odpočtů daně na vstupu.                                                                     | 61-InputTaxCorrection                                                                                                                                                        |
| 62  | \-               | Zbývající částka.                                                                                      | Řádek 52 – řádek 55 – řádek 56 – řádek 57 – řádek 58 – řádek 50 – řádek 60 – řádek 61                                                                                                        |

**ODDÍL – OSTATNÍ ČÁSTKY DANĚ**

| Řádek | Pole - částka daně | Popis                                                                                                                                                                                                                                                         | Výsledek vyhledávání                                 |
|-----|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| 64  | 65               | Daň z důvodu změny formy zdanění a dodatečná daň ze zdaněných záloh z důvodu změny daňové sazby.                                                                                                                                        | 64-AdditionalTaxDueChangeTaxRate              |
| 65  | 69               | Nesprávné nebo neoprávněné částky daně, které jsou uvedeny na fakturách, a částky daně, které jsou dlužné v souladu s §6a (4) věta 2, oddíl 17 (1) věta 7 nebo oddíl 25b (2) UStG, nebo které dluží outsourcingová společnost nebo skladník. | 65-TaxDecreaseCorrection                      |
| 67  | 39               | Odečtení pevné zvláštní zálohy na trvalé prodloužení. Tento řádek se standardně vyplňuje až při posledním předběžném oznámení zdaňovacího období.                                                                                                  | Parametr uživatelského vstupu v dialogovém okně sestavy |
| 68  | 83               | Zbývající záloha na daň z prodeje a zbývající přeplatek. Před částkou uveďte znaménko minus.                                                                                                                                                          | Řádek 62 + řádek 64 – řádek 65 – řádek 66             |

**ODDÍL – DOPLŇUJÍCÍ INFORMACE O SNÍŽENÍ**

| Řádek | Pole - základ daně | Pole - částka daně | Popis                                                            | Výsledek vyhledávání                                                                                                                                                                                                    |
|-----|----------------|------------------|------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 73  | 50             | \-               | Snížení základu daně na řádcích 20 až 24.                      | 73-BadDebtsWriteOffStandard (81/50)</br>73-BadDebtsWriteOffReduced (86/50)</br>73-BadDebtsWriteOffOtherRates (35/36/50)</br>73-BadDebtsWriteOffEUSalesAverageRate24 (77/50)</br>73-BadDebtsWriteOffSalesAverageRate24 (76/80/50) |
| 74  | \-             | 37               | Snížení částek odčitatelné daně na vstupu na řádcích 55, 59 a 60. | 74-BadDebtsWriteOffInputTax (66/37)</br>74-BadDebtsWriteOffInputTaxAverageRates (63/37)</br>74-BadDebtsWriteOffInputTaxEUPurchaseNewVehicles (59/37)                                                                     |

#### <a name="purchase-reverse-charge-vat"></a>Nákupní reverse charge VAT

Pokud nakonfigurujete kódy DPH tak, aby zaúčtovaly přenesení daňové povinnosti k DPH pomocí importního DPH, přidružte své kódy DPH k výsledku vyhledávání **Vyhledání pole sestavy**, který v názvu obsahuje „UseTax“.

Případně můžete nakonfigurovat dva samostatné kódy daně z prodeje: jeden pro splatnou DPH a jeden pro odpočet DPH. Poté přiřaďte každý kód k odpovídajícím výsledkům vyhledávání **Vyhledání pole sestavy**.

Například pro zdanitelné pořízení v rámci Společenství se standardní sazbou nakonfigurujete kód daně z prodeje **UT_S_EU** s daní z použití a přiřaďte ji k výsledku vyhledávání **34-UseTaxEUPurchaseStandard** **Vyhledání pole sestavy**. V tomto případě částky, které používají kód DPH **UT_S_EU**, se projeví v kolonkách 089 a 061 (řádky 34 a 56).

Případně můžete nakonfigurovat dva kódy DPH:

  - **DPH_S_EU**, který má hodnotu daňové sazby -19 procent
  - **InVAT_S_EU**, který má hodnotu daňové sazby 19 procent

Poté přiřaďte kódy k odpovídajícím výsledkům vyhledávání **Vyhledání pole sestavy** následujícím způsobem:

  - Přiřaďte **VAT_S_EU** s výsledkem vyhledávání **34-EUPurchaseStandard**.
  - Přiřaďte **InVAT_S_EUU** s výsledkem vyhledávání **56-InputTaxEUPurchase**.

V tomto případě částky, které používají kód DPH **VAT_S_EU**, se projeví v kolonce 089 (řádek 34). Částky, které používají kód DPH **InVAT_S_EU**, se projeví v kolonce 061 (řádek 56).

Další informace, jak konfigurovat přenesení daňové povinnosti k DPH, viz [Přenesení daňové povinnosti](emea-reverse-charge.md).

## <a name="configure-system-parameters"></a>Konfigurace systémových parametrů

Chcete-li vygenerovat přiznání k DPH, musíte nakonfigurovat daňové číslo (Steuernummer) vaší organizace.

1. Přejděte do části na **Správa organizace** > **Organizace** > **Právnické osoby**.
2. Vyberte právnickou osobu a poté vyberte možnost **ID registrace**.
3. Vyberte nebo vytvořte adresu v Německu a poté na pevné záložce **Registrační ID** vyberte **Přidat**.
4. V poli **Typ registrace** vyberte typ registrace, který je vyhrazen pro Německo a který používá kategorii registrace **Enterprise ID (COID)**.
5. Do pole **Registrační číslo** zadejte daňové číslo.
6. Na kartě **Všeobecné** do pole **Platné od** zadejte datum, kdy číslo vstoupí v platnost.

Další informace o tom, jak nastavit kategorie a typy registrace, viz [Registrační ID](emea-registration-ids.md).

## <a name="set-up-a-vat-declaration-for-germany"></a>Nastavení přiznání k DPH pro Německo

### <a name="import-er-configurations"></a>Import konfigurací ER

Otevřete pracovní prostor **Elektronické hlášení** a importujte následující nebo novější verze těchto formátů ER:

   - Prohlášení k DPH Excel (DE).version.101.16.12.xml
   - Prohlášení k DPH XML (DE).version.101.16.xml

### <a name="set-up-application-specific-parameters-for-vat-declaration-fields"></a><a name="set-up-application-specific-parameters-for-vat-declaration-fields"></a>Nastavení parametrů specifických pro aplikace pro pole přiznání k DPH

Chcete-li automaticky generovat přiznání k DPH, musíte přidružit kódy DPH v aplikaci a výsledky vyhledávání v konfiguraci ER.

> [!NOTE]
> Doporučujeme, abyste aktivovali funkci **Použít parametry specifické pro aplikaci z předchozích verzí formátů ER** v pracovním prostoru **Správa funkcí**. Když je tato funkce povolena, parametry, které jsou konfigurovány pro dřívější verzi formátu ER, se automaticky stanou použitelnými u novější verze stejného formátu. Pokud tato funkce není povolena, musíte u každé verze formátu explicitně konfigurovat parametry specifické pro aplikaci. Funkce **Použít parametry specifické pro aplikaci z předchozích verzí formátů ER** je dostupná v pracovním prostoru **Správa funkcí** od verze Finance 10.0.23. Další informace o tom, jak nastavit parametry formátu ER pro každou právnickou osobu najdete v tématu [Nastavení parametrů formátu elektronického výkaznictví podle právnické osoby](../../fin-ops-core/dev-itpro/analytics/er-app-specific-parameters-set-up.md).

Pomocí těchto kroků definujte, které kódy DPH generují která pole v přiznání k DPH.

1. Přejděte na **Pracovní prostory** > **Elektronické výkaznictví** a vyberte **Konfigurace výkaznictví**.
2. Vyberte konfiguraci **Přiznání k DPH v XML (DE)** a poté vyberte **Konfigurace \> Nastavení parametrů specifických pro aplikaci**.
3. Na stránce **Parametry specifické pro aplikaci**, na pevné záložce **Vyhledávání** vyberte **Vyhledání pole sestavy**.
4. Na pevné záložce **Podmínky** nastavte následující pole k přiřazení kódů DPH a polí sestavy.

    | Pole                  | Popis                                                                                                                                                                                                                                                                                                          |
    |------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Výsledek vyhledávání          | Vyberte hodnotu pole sestavy. Další informace o hodnotách a jejich přiřazení k řádkům přiznání k DPH najdete v části [Přehled přiznání k DPH](#vat-declaration-overview) dříve v tomto tématu.                                                                                               |
    | Kód daně               | Vyberte kód DPH, který chcete přidružit k poli sestavy. Zaúčtované daňové transakce, které používají vybraný kód DPH, budou shromážděny v příslušné kolonce přiznání. Doporučujeme oddělit kódy DPH tak, aby jeden kód DPH generoval částky pouze v jedné kolonce přiznání. |
    | Klasifikátor transakcí | Pokud jste vytvořili dostatek kódů DPH k určení kolonky přiznání, vyberte **\*Ne prázdné\***. Pokud jste nevytvořili dostatek kódů DPH, takže jeden kód DPH vygeneruje částky pouze v jedné kolonce přiznání, můžete vytvořit klasifikátor transakcí. K dispozici jsou následující klasifikátory transakcí:</br>-   **Nákup**</br>-   **PurchaseExempt** (nákup osvobozený od daně)</br>-   **PurchaseReverseCharge** (daň splatná z nákupní reverse charge)</br>-   **Prodej**</br>-   **SalesExempt** (prodej osvobozený od daně)</br>-   **SalesReverseCharge** (daň odvedená z přenesené daňové povinnosti při nákupu nebo prodeji)</br>-   **Importní DPH.** </br>Pro každý klasifikátor transakcí je k dispozici také klasifikátor dobropisu. Například jeden z těchto klasifikátorů je **PurchaseCreditNote** (nákupní dobropis).</br>Nezapomeňte vytvořit dva řádky pro každý kód DPH: jeden s hodnotou klasifikátoru transakce a jeden s klasifikátorem transakce pro hodnotu dobropisu. |

    > [!NOTE]
    > Přiřaďte všechny kódy DPH k výsledkům vyhledávání. Pokud by některé kódy DPH neměly generovat hodnoty v přiznání k DPH, přiřaďte je k výsledku vyhledávání **Ostatní**.

    ![Stránka specifické parametry aplikace](media/69ecb881f12819259ca166b9b98b8303.jpg)

5. V poli **Stav** změňte hodnotu na **Dokončeno**.
6. V podokně akcí vyberte **Exprt** pro export nastavení parametrů specifických pro aplikaci.
7. Vyberte konfiguraci **Přiznání k DPH pro Excel (DE)** a poté v podokně Akce volbou **Import** importujte parametry, pro které jste nakonfigurovali **Přiznání k DPH v XML (DE)**.
8. V poli **Stav** vyberte možnost **Dokončeno**.

### <a name="set-up-the-vat-reporting-format-for-preview-amounts-in-excel"></a>Nastavte formát hlášení DPH pro náhled částky v Excelu

1. V pracovním prostoru **Správa funkcí** najděte a povolte funkci **Sestavy formátu výkazu DPH**.
2. Přejděte do **Hlavní knihy** > **Nastavení** > **Parametry hlavní knihy**.
3. Na kartě **DPH** na záložce s náhledem **Možnosti daně** v poli **Mapování formátu přiznání k DPH** vyberte **Přiznání k DPH pro Excel (DE)**.

   Tento formát je vytištěn při spuštění sestavy **Vykázat DPH pro období vyrovnání**. Vytiskne se také při výběru **Tisk** na stránce **Platby DPH**.

4. Na stránce **Finanční úřady** vyberte finanční úřad a poté v poli **Rozvržení sestavy** vyberte **Výchozí**.

Pokud konfigurujete přiznání k DPH v právnické osobě, která má [více registrací k DPH](emea-reporting-for-multiple-vat-registrations.md), postupujte následovně:

1. Přejděte do **Hlavní knihy** > **Nastavení** > **Parametry hlavní knihy**.
2. Na kartě **DPH** na pevné záložce **Elektronické hlášení pro země/oblasti**, na řádku pro **DEU** vyberte formát ER **Přiznání k DPH Excel (DE)**.

## <a name="set-up-electronic-messages"></a>Nastavení elektronických zpráv

### <a name="download-and-import-the-data-package-that-has-example-settings-for-electronic-messages"></a>Stažení a import balíčku dat, který obsahuje ukázkové nastavení elektronických zpráv

Datový balíček obsahuje nastavení elektronické zprávy, která slouží k vygenerování přiznání k DPH ve formátu XML a následnému náhledu v Excelu. Tato nastavení můžete rozšířit nebo vytvořit vlastní. Další informace, jak pracovat s elektronickými zprávami a jak vytvořit vlastní nastavení, najdete v části [Elektronické zasílání zpráv](../general-ledger/electronic-messaging.md).

1. V [Microsoft Dynamics Lifecycle Services(LCS)](https://lcs.dynamics.com/v2), v knihovně Sdílený majetek vyberte **Datový balíček** jako typ majteku a poté stáhněte **Balíček EM přiznání k DPH DE**. Stažený soubor má název **DE VAT declaration EM package.zip**.
2. V Dynamics 365 Finance, v pracovním prostoru **Správa dat** vyberte **Importovat**.
3. Na pevné záložce **Import** v poli **Název slupiny** zadejte název úlohy.
4. Na záložce s náhledem **Vybrané entity** vyberte **Přidat soubor**.
5. V dialogovém okně **Přidat soubor** ověřte, že je pole **Formát zdrojových dat** nastaveno na **Balíček**, vyberte **Nahrát a přidat** a poté vyberte soubor zip, který jste stáhli dříve.
6. Vyberte **Zavřít**.
7. Po nahrání datových entit v podokně akcí vyberte **Importovat**.
8. Přejděte na **Daň** > **Dotazy a sestavy** > **Elektronické zprávy** > **Elektronické zprávy** a ověřte zpracování importovaných elektronických zpráv.

### <a name="configure-electronic-messages"></a>Konfigurace elektronických zpráv

1. Přejděte na **Daň** > **Nastavení** > **Elektronické zprávy** > **Akce naplnění záznamů**.
2. Vyberte řádek pro **DE Vyplňte záznamy vratky DPH** a poté vyberte **Upravit dotaz**.
3. Pomocí filtru vyberte období vyrovnání, která chcete zahrnout do sestavy.
4. Pokud musíte vykazovat daňové transakce z jiných období vyrovnání v jiném přiznání, vytvořte novou akci **Naplnit záznamy** a vyberte příslušná období vypořádání.

## <a name="preview-the-vat-declaration-in-excel"></a>Náhled přiznání k DPH v Excelu

### <a name="preview-the-vat-declaration-in-excel-from-the-report-sales-tax-for-settlement-period-periodic-task"></a>Náhled přiznání k DPH v aplikaci Excel z periodické úlohy Vykázat DPH pro období vyrovnání

1. Přejděte na **Daň** > **Periodické úlohy** > **Prohlášení** > **DPH** > **Vykázat DPH pro období vyrovnání**.
2. Vyberte hodnotu v poli **Období vyrovnání**.
3. V poli **Verze platby DPH** vyberte některou z následujících hodnot:

    - **Originál**: Vygenerujte sestavu pro transakce DPH původní platby DPH nebo před vygenerováním platby DPH.
    - **Opravy**: Generuje sestavu transakcí DPH všech dalších plateb DPH za dané období.
    - **Celkový seznam**: Generuje sestavu všech transakcí DPH za dané období, včetně původní a všech oprav.

4. V poli **Od data** vyberte počáteční datum období vykazování.
5. Vyberte **OK** a zkontrolujte sestavu Excel.

### <a name="settle-and-post-sales-tax"></a><a name="settle-and-post-sales-tax"></a>Vyrovnat a zaúčtovat DPH

1. Přejděte na **Daň** > **Periodické úlohy** > **Přiznání** > **DPH** > **Vyrovnat a zaúčtovat DPH**.
2. Vyberte hodnotu v poli **Období vyrovnání**.
3. V poli **Verze platby DPH** vyberte některou z následujících hodnot:

    - **Původní**: Vygeneruje původní platbu DPH pro období vyrovnání.
    - **Poslední opravy**: Vygeneruje opravu platby DPH po vytvoření původní platby DPH pro období vyrovnání.

4. V poli **Od data** vyberte počáteční datum období vykazování.
5. Vyberte **OK**.

### <a name="preview-the-vat-declaration-in-excel-from-a-sales-tax-payment"></a>Náhled přiznání k DPH v aplikaci Excel z plateb DPH

1. Přejděte na **Daň** > **Dotazy a sestavy** > **Dotazy na DPH** > **Platby DPH** a vyberte řádek platby DPH.
2. Vyberte možnost **Tisk sestavy** a poté vyberte možnost **OK**.
3. Zkontrolujte soubor Excel, který je vygenerován pro vybraný řádek platby DPH.

    > [!NOTE]
    > Sestava je vygenerována pouze pro vybraný řádek platby DPH. Pokud chcete vygenerovat např. opravné přiznání, které obsahuje všechny opravy za období, nebo náhradní přiznán, které obsahuje původní údaje a všechny opravy, použijte periodický úkol **Vykázat DPH za zúčtovací období**.

## <a name="generate-a-vat-declaration-from-electronic-messages"></a>Generování přiznání k DPH z elektronických zpráv

Když pro generování sestavy používáte elektronické zprávy, můžete shromažďovat daňové údaje od více právnických osob. Více informací naleznete v sekci [Spustit přiznání k DPH pro více právnických osob](#run-a-vat-declaration-for-multiple-legal-entities) dále v tomto tématu.

Následující postup platí pro příklad zpracování elektronické zprávy, který jste importovali z knihovny sdíleného majetku LCS.

1. Přejděte na **Daň** > **Dotazy a sestavy** > **Elektronické zprávy** > **Elektronické zprávy**.
2. V levém podokně vyberte **DE Přiznání k DPH**.
3. Na záložce s náhledem **Zprávy** vyberte **Novýá** a poté v dialogovém okně **Spuštění zpracování** vyberte **OK**.
4. Vyberte řádek zprávy, který je vytvořen, zadejte popis a poté zadejte počáteční a konečné datum přiznání.

    > [!NOTE]
    > Kroky 5 až 7 jsou volitelné.

5. Volitelné: Na záložce s náhledem **Zprávy** vyberte **Shromažďovat data** a potom vyberte **OK**. Do zprávy se přidají platby DPH, které byly vygenerovány dříve. Více informací naleznete v předchozích části [Vyrovnat a zaúčtovat DPH](#settle-and-post-sales-tax) v tomto tématu. Pokud tento krok přeskočíte, stále můžete vygenerovat přiznání k DPH pomocí pole **Verze přiznání k DPH** v dialogovém okně **Přiznání**.
6. Volitelné: Na kartě s náhledem **Položky zprávy** zkontrolujte platby DPH, které jsou přeneseny ke zpracování. Ve výchozím nastavení jsou zahrnuty všechny platby DPH ve vybraném období, které nebyly zahrnuty v žádné jiné zprávě stejného zpracování.
7. Volitelně: Vyberte **Původní dokument**, chcete-li zkontrolovat platby DPH, nebo zvolte **Odstranit**, chcete-li vyloučit ze zpracování platby DPH. Pokud tento krok přeskočíte, stále můžete vygenerovat přiznání k DPH pomocí pole **Verze přiznání k DPH** v dialogovém okně **Přiznání**.
8. Na záložce s náhledem **Zprávy** vyberte **Aktualizovat status**. V dialogovém okně **Aktualizovat status** vyberte **Připraveno k vygenerování** a poté vyberte **OK**. Ověřte, že se stav zprávy změnil na **Připraveno k vygenerování**.
9. Vyberte **Generovat sestavu**. Chcete-li zobrazit náhled částek přiznání k DPH, v dialogovém okně **Spustit zpracování** vyberte **Náhled sestavy** a potom vyberte **OK**.
10. V dialogovém okně **Parametry elektronického výkaznictví** nastavte následující pole a poté vyberte **OK**.

    | **Pole**                                   | **popis**                                                                                                                                                                                                              |
    |---------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Období vyrovnání                           | Vyberte období vyrovnání. Pokud jste vybrali **Shromažďovat data** v kroku 5, můžete nechat toto pole prázdné. Sestava vygenerována pro transakce DPH, které jsou zahrnuty ve shromážděných platbách DPH. |
    | Verze daňového přiznání                     | Vyberte jednu z následujících hodnot:</br>-   **Originál** - Vygenerujte sestavu pro transakce DPH původní platby DPH nebo před vygenerováním platby DPH.</br>-   **Opravy** - Generuje sestavu transakcí DPH všech dalších plateb DPH za dané období.</br>-   **Celkový seznam** – Generuje sestavu všech transakcí DPH za dané období, včetně původní a všech oprav.|
    | Daňový zástupce | Pokud je to možné, vyberte stranu, která je daňovým zástupcem pro přiznání k DPH. Informace o vybrané straně se exportují do prvku XML **DatenLieferant**. |
    | Kontaktní osoba | Vyberte osobu v organizaci, která je dodavatelem dat. Informace o vybrané osobě se exportují do prvku XML **DatenLieferant**. |
    | Opravné vrácení | Vyberte **Ano**, pokud se jedná o opravné přiznání k DPH. V tomto případě bude mít XML element KZ10 hodnotu **1**.|
    | Podpůrné dokumenty | Vyberte **Ano**, pokud zašlete také podpůrné dokumenty. V tomto případě bude mít XML element KZ22 hodnotu **1**.|
    | Mandát inkasa SEPA bude výjimečně zrušen| Vyberte **Ano**, bude-li pro toto období předběžné registrace výjimečně zrušeno povolení k SEPA inkasu. Například kvůli kompenzačním požadavkům. Případný zbývající zůstatek je třeba uhradit samostatně. V tomto případě bude mít XML element KZ26 hodnotu **1**. |
    | Započtení požadované výše náhrady | Vyberte **Ano**, jde-li o započtení požadované částky náhrady nebo pokud byla částka náhrady přiřazena. V tomto případě bude mít XML element KZ29 hodnotu **1**. |
    | Speciální záloha trvalé prodloužení | Zadejte částku odpočtu pevné zvláštní zálohy na trvalé prodloužení. Tato odpočetná částka je obvykle dokončena až při poslední předregistraci zdaňovacího období. Částka je exportována v řádku 67 (kolonka 39) a XML prvku KZ39 přiznání k DPH. |

11. V pravém horním rohu stránky vyberte **Přílohy** a poté vyberte možnost **Otevřít**.
12. Zkontrolujte částky v dokumentu aplikace Excel a poté vyberte **Vygenerovat sestavu**.
13. Chcete-li vygenerovar přiznání k DPH ve formátu XML, v dialogovém okně **Spuštění zpracování** vyberte **Generovat sestavu** a pak vyberte **OK**.
14. V dialogovém okně **Parametry elektronického hlášení** nastavte pole podle popisu v kroku 10.
15. Vyberte **Přílohy** v pravém horním rohu stránky, stáhněte soubor a použijte jej k odeslání finančnímu úřadu.

## <a name="run-a-vat-declaration-for-multiple-legal-entities"></a><a name="run-a-vat-declaration-for-multiple-legal-entities"></a>Spuštění přiznání k DPH pro několik právnických osob

Chcete-li použít formáty k vykázání přiznání k DPH pro skupinu právnických osob, musíte nejprve nastavit parametry formátů ER specifické pro aplikacipro kódy DPH ze všech požadovaných právnických osob.

### <a name="set-up-electronic-messages-to-collect-tax-data-from-several-legal-entities"></a>Vytvoření elektronických zpráv ke shromažďování daňových údajů od několika právnických osob

Chcete-li nastavit elektronické zprávy, které budou shromažďovat údaje od více právnických osob, postupujte takto.

1. Přejděte na **Pracovní prostory** > **Správa funkcí**.
2. Najděte a vyberte funkci **Mezipodnikové dotazy pro akce vyplnění záznamů** v seznamu a vyberte **Povolit nyní**.
3. Přejděte na **Daň** > **Nastavení** > **Elektronické zprávy \> Akce naplnění záznamů**.
4. Na stránce **Akce vyplnění záznamů** vyberte řádek pro **DE Vyplnit záznamy vratky DPH**.

   V mřížce **Nastavení datových zdrojů** je k dispozici nové pole **Společnost**. U existujících záznamů toto pole zobrazuje identifikátor aktuální právnické osoby.

5. V mřížce **Nastavení zdrojů dat** přidejte řádek pro každou další právnickou osobu, která musí být zahrnuta do vykazování. U každého nového řádku je třeba nastavit tato pole.

    | Pole                  | Popis                                                                                                                   |
    |------------------------|-------------------------------------------------------------------------------------------------------------------------------|
    | Název                   | Zadejte hodnotu, která vám pomůže pochopit, odkud tento záznam pochází. Například zadejte **Platba DPH dceřiné společnosti 1**. |
    | Typ položky zprávy      | Vyberte **Vratka DPH**. Tato hodnota je jedinou hodnotou, která je k dispozici pro všechny záznamy.                                    |
    | Typ účtu           | Vyberte **Vše**.                                                                                                               |
    | Název hlavní tabulky      | Zadejte **TaxReportVoucher** pro všechny záznamy.                                                                             |
    | Pole čísla dokumentu  | Zadejte **Voucher** pro všechny záznamy.                                                                                      |
    | Pole data dokumentu    | Zadejte **TransDate** pro všechny záznamy.                                                                                    |
    | Pole účtu dokumentu | Zadejte **TaxPeriod** pro všechny záznamy.                                                                                    |
    | Společnost                | Vyberte ID právnické osoby.                                                                                            |
    | Dotaz uživatele             | Toto zaškrtávací políčko je automaticky zaškrtnuto, když definujete kritéria volbou **Upravit dotaz**.                                 |

6. U každého nového řádku vyberte **Upravit dotaz** a zadejte související zúčtovací období pro právnickou osobu, která je uvedena v poli **Společnost** na řádku.

Po dokončení tohoto nastavení bude funkce **Shromažďovat data** na stránce **Elektronické zprávy** shromažďovat platby DPH od všech právnických osob, které jste definovali.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
