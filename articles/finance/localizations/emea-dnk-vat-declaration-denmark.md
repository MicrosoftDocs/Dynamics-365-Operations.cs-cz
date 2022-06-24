---
title: Přiznání k DPH (Dánsko)
description: Tento článek popisuje, jak nastavit a vygenerovat předběžné přiznání k dani z přidané hodnoty (DPH) pro Dánsko.
author: anasyash
ms.date: 03/10/2022
ms.topic: article
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: anasyash
ms.search.validFrom: ''
ms.openlocfilehash: 666dc96cb169ab28ac3938299a3f245e3b4511ab
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8862992"
---
# <a name="vat-declaration-denmark"></a>Přiznání k DPH (Dánsko)

[!include [banner](../includes/banner.md)]

Tento článek popisuje, jak nastavit přiznání k dani z přidané hodnoty (DPH) pro Dánsko a zobrazit jeho náhled v aplikaci Microsoft Excel.

Chcete-li automaticky vygenerovat sestavu, vytvořte nejprve dostatek kódů DPH, aby bylo možné vést samostatné účetnictví DPH pro každé pole na předběžném přiznání k DPH. Navíc v parametrech specifických pro aplikaci ve formátu elektronického výkaznictví (ER) pro předběžné přiznání k DPH přidružte kódy DPH k výsledku vyhledávání pro pole v přiznání k DPH.

Pro Dánsko musíte nakonfigurovat **Vyhledání pole sestavy**. Další informace, jak nastavit parametry specifické pro aplikaci, najdete v části [Nastavení parametrů specifických pro aplikaci pro pole přiznání k DPH](#set-up-application-specific-parameters) dále v tomto článku.

V následující tabulce sloupec „Výsledek vyhledávání“ zobrazuje výsledek vyhledávání, který je předkonfigurován pro konkrétní řádek přiznání k DPH ve formátu přiznání k DPH. Tyto informace použijte ke správnému přidružení kódů DPH k výsledku vyhledávání a poté k řádku přiznání k DPH.

### <a name="vat-declaration-overview"></a>Přehled přiznání k DPH

Předběžné přiznání k DPH v Dánsku obsahuje následující informace.

**Splatná VAT**

| Popis                                                  | Základ daně / Částka daně | Výsledek vyhledávání / Celkem                                                                                                                                                                                                                                                                                                                          |
|--------------------------------------------------------------|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DPH na výstupu                                                   | Částka daně          | **OutputVAT**</br> **DomesticVATUseTax** (také uvedeno v poli „DPH na vstupu")                                                                                                                                                                                                                                                                       |
| DPH na zboží atd. zakoupené v zahraničí                           | Částka daně          | **PurchaseGoodsAbroad**</br>**PurchaseGoodsAbroadUseTax** (také uvedeno v poli „DPH na vstupu“)</br>**PurchaseGoodsEU** (Základ daně se vykazuje v „kolonce B - pořízení zboží.“)</br>**PurchaseGoodsEUUseTax** (Částka daně je také uvedena v poli „DPH na vstupu“. Základ daně se vykazuje v „kolonce A - pořízení zboží.“)                   |
| DPH na služby zakoupené v zahraničí podléhající přenesení daňové povinnosti | Částka daně          | **PurchaseServicesAbroad**</br> **PurchaseServicesAbroadUseTax** (také uvedeno v poli „DPH na vstupu“)</br>**PurchaseServicesEU** (Základ daně se vykazuje v „kolonce A - pořízení zboží.“)</br>**PurchaseServicesEUUseTax** (Částka daně je také uvedena v poli „DPH na vstupu“. Základ daně se vykazuje v „kolonce A - pořízení služeb.“) |
| Celková odváděná daň                                                | Částka daně          | Součet předchozích tří kolonek                                                                                                                                                                                                                                                                                                            |

**Srážky**

| Popis                                                                               | Základ daně / Částka daně | Výsledek vyhledávání / Celkem                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|-------------------------------------------------------------------------------------------|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DPH na vstupu                                                                                 | Částka daně          | **InputVAT**</br> **DomesticVATUseTax** (také uvedeno v kolonce „DPH na výstupu“)</br>**PurchaseGoodsAbroadUseTax** (také uvedeno v kolonce „DPH na zboží apod. zakoupené v zahraničí“)</br>**PurchaseServicesAbroadUseTax** (vykazuje se také v kolonce „DPH za služby zakoupené v zahraničí podléhající přenesené daňové povinnosti“)</br>**PurchaseGoodsEUUseTax** (také uvedeno v kolonce „DPH na zboží apod. zakoupené v zahraničí“)</br> **PurchaseServicesEUUseTax** (vykazuje se také v kolonce „DPH za služby zakoupené v zahraničí podléhající přenesené daňové povinnosti“) |
| Poplatek za ropu a plynové láhve                                                                  | Částka daně          | **OilGasDuty**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Poplatek za zemní a koksárenský plyn                                                             | Částka daně          | **NaturalTownGasDuty**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Poplatek za uhlík                                                                               | Částka daně          | **CarbonDuty**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| CO2Duty                                                                                   | Částka daně          | **CO2Duty**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Poplatek za vodu                                                                              | Částka daně          | **WaterCharge**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Celkové srážky                                                                          | Částka daně          | Součet předchozích šesti kolonek                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Celková částka poplatků (kladná částka = provedení platby, záporná částka = obdržení refundace) | Částka daně          | „Celková odváděná daň“ – „Celkové odpočty“                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |

**Doplňující informace**

| Popis                                                                                                                                                                                                                                | Základ daně / Částka daně | Výsledek vyhledávání / Celkem                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------|-------------------------------------------------|
| Kolonka A – pořízení zboží. Hodnota bez DPH pořízení zboží v rámci Unie.                                                                                                                                                   | Základ daně            | **PurchaseGoodsEU PurchaseGoodsEUUseTax**       |
| Kolonka A – pořízení služeb. Hodnota bez DPH pořízení služeb v rámci Unie.                                                                                                                                             | Základ daně            | **PurchaseServicesEU PurchaseServicesEUUseTax** |
| Kolonka B – poskytování zboží – uveďte do „EU-prodej bez DPH“/dánský systém VIES. Hodnota bez DPH poskytování zboží v rámci Unie                                                                                                           | Základ daně            | **SalesGoodsEU**                                |
| Kolonka B – dodání – neuvádějte do „EU-prodej bez DPH“/dánský systém VIES. Hodnota bez DPH některých dodávek v rámci Unie, například instalace, montáž, prodej na dálku a nové dopravní prostředky u osob nepovinných k dani. | Základ daně            | **SalesInstallationAssemblyEtcEU**              |
| Kolonka B - poskytování služeb. Hodnota bez DPH u dodávek služeb v rámci Unie, za které je kupující povinen zaplatit DPH jako přenesení daňové povinnosti – musí být také vykázána v kolonce „EU-prodej bez DPH“/dánský systém VIES.                          | Základ daně            | **SalesServicesEU**                             |
| Box C - ostatní dodávky. Hodnota dodání jiného zboží a služeb, které jsou dodávány bez DPH na území Dánska, do jiných členských států EU a do třetích zemí nebo třetích území.                                     | Základ daně            | **OtherSuppliesWithoutVAT**                     |

#### <a name="purchase-reverse-charge-vat"></a>Nákupní reverse charge VAT

Pokud nakonfigurujete kódy DPH tak, aby zaúčtovaly přenesení daňové povinnosti k DPH pomocí importního DPH, přidružte své kódy DPH k výsledku vyhledávání **Vyhledání pole sestavy**, který v názvu obsahuje „UseTax“.

Případně můžete nakonfigurovat dva samostatné kódy daně z prodeje: jeden pro splatnou DPH a jeden pro odpočet DPH. Poté přiřaďte každý kód k odpovídajícím výsledkům vyhledávání **Vyhledání pole sestavy**.

Například pro zdanitelné pořízení v rámci Společenství nakonfigurujete kód daně z prodeje **UT_S_EU** s daní z použití a přiřaďte ji k výsledku vyhledávání **PurchaseGoodsEUUseTax** z **Vyhledání pole sestavy**. V tomto případě částky daně, které používají kód DPH **UT_S_EU**, se projeví v kolonkách „DPH na zboží atd. zakoupené v zahraničí“ a „DPH na vstupu“. Základy daně se vykazují v „kolonce B - pořízení zboží.“

Případně můžete nakonfigurovat dva kódy DPH:

- **DPH_S_EU**, který má hodnotu daňové sazby -25 procent
- **InVAT_S_EU**, který má hodnotu daňové sazby 25 procent

Poté přiřaďte kódy k odpovídajícím výsledkům vyhledávání **Vyhledání pole sestavy** následujícím způsobem:

- Přiřaďte **VAT_S_EU** k výsledku vyhledávání **PurchaseGoodsEU**.
- Přiřaďte **InVAT_S_EUU** k výsledku vyhledávání **InputVAT**.

V tomto případě částky, které používají kód DPH **VAT_S_EU**, se projeví v kolonkách „DPH na zboží atd. zakoupeno v zahraničí“ a „kolonka A - pořízení zboží.“ Částky, které používají kód DPH **InVAT_S_EU**, se projeví v kolonce „DPH na vstupu“.

Další informace, jak konfigurovat přenesení daňové povinnosti k DPH, viz [Přenesení daňové povinnosti](emea-reverse-charge.md).

## <a name="configure-system-parameters"></a>Konfigurace systémových parametrů

Chcete-li vygenerovat přiznání k DPH, musíte nakonfigurovat DIČ.

1. Přejděte do části na **Správa organizace** > **Organizace** > **Právnické osoby**.
2. Vyberte právnickou osobu a poté vyberte možnost **ID registrace**.
3. Vyberte nebo vytvořte adresu v Dánsku a poté na záložce **Registrační ID** vyberte **Přidat**.
4. V poli **Typ registrace** vyberte typ registrace, který je vyhrazen pro Dánsko a který používá kategorii registrace **DIČ**.
5. Do pole **Registrační číslo** zadejte daňové číslo.
6. Na kartě **Všeobecné** do pole **Platné od** zadejte datum, kdy číslo vstoupí v platnost.

Další informace o tom, jak nastavit kategorie a typy registrace, viz [Registrační ID](emea-registration-ids.md).

## <a name="set-up-a-vat-declaration-preview-for-denmark"></a>Nastavení náhledu přiznání k DPH pro Dánsko

### <a name="import-er-configurations"></a>Import konfigurací ER

Otevřete pracovní prostor **Elektronické výkaznictví** a importujte formát ER **Prohlášení k DPH Excel (DK)**.

Další informace viz [Stáhněte si konfigurace elektronického výkaznictví z Globálního úložiště konfigurační služby](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md).

### <a name="set-up-application-specific-parameters-for-vat-declaration-fields"></a><a name="set-up-application-specific-parameters"></a>Nastavení parametrů specifických pro aplikace pro pole přiznání k DPH

> [!NOTE]
> Doporučujeme, abyste aktivovali funkci **Použít parametry specifické pro aplikaci z předchozích verzí formátů ER** v pracovním prostoru **Správa funkcí**. Když je tato funkce povolena, parametry, které jsou konfigurovány pro dřívější verzi formátu ER, se automaticky stanou použitelnými u novější verze stejného formátu. Pokud tato funkce není povolena, musíte u každé verze formátu explicitně konfigurovat parametry specifické pro aplikaci. Funkce **Použít parametry specifické pro aplikaci z předchozích verzí formátů ER** je dostupná v pracovním prostoru **Správa funkcí** od verze Finance 10.0.23. Další informace o tom, jak nastavit parametry formátu ER pro každou právnickou osobu najdete v tématu [Nastavení parametrů formátu elektronického výkaznictví podle právnické osoby](../../fin-ops-core/dev-itpro/analytics/er-app-specific-parameters-set-up.md).

Chcete-li automaticky generovat přiznání k DPH, musíte přidružit kódy DPH v aplikaci a výsledky vyhledávání v konfiguraci ER.

Pomocí těchto kroků definujte, které kódy DPH generují která pole v přiznání k DPH.

1. Přejděte na **Pracovní prostory** > **Elektronické výkaznictví** a vyberte **Konfigurace výkaznictví**.
2. Vyberte konfiguraci **Přiznání k DPH Excel (DK)** a poté vyberte **Konfigurace \> Nastavení parametrů specifických pro aplikaci**.
3. Na stránce **Parametry specifické pro aplikaci**, na pevné záložce **Vyhledávání** vyberte **Vyhledání pole sestavy**.
4. Na pevné záložce **Podmínky** nastavte následující pole k přiřazení kódů DPH a polí sestavy.

    | Pole                  | Popis                                                                                                                                                                                                                                                                                                          |
    |------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Výsledek vyhledávání          | Vyberte hodnotu pole sestavy. Další informace o hodnotách a jejich přiřazení k řádkům přiznání k DPH najdete v části [Přehled přiznání k DPH](#vat-declaration-overview) dříve v tomto článku.                                                                                               |
    | Kód daně               | Vyberte kód DPH, který chcete přidružit k poli sestavy. Zaúčtované daňové transakce, které používají vybraný kód DPH, budou shromážděny v příslušné kolonce přiznání. Doporučujeme oddělit kódy DPH tak, aby jeden kód DPH generoval částky pouze v jedné kolonce přiznání. |
    | Klasifikátor transakcí | Pokud jste vytvořili dostatek kódů DPH k určení kolonky přiznání, vyberte **\*Ne prázdné\***. Pokud jste nevytvořili dostatek kódů DPH, takže jeden kód DPH vygeneruje částky pouze v jedné kolonce přiznání, můžete vytvořit klasifikátor transakcí. K dispozici jsou následující klasifikátory transakcí:</br>-   **Nákup**</br>-   **PurchaseExempt** (nákup osvobozený od daně)</br>-   **PurchaseReverseCharge** (daň splatná z nákupní reverse charge)</br>-   **Prodej**</br>-   **SalesExempt** (prodej osvobozený od daně)</br>-   **SalesReverseCharge** (daň odvedená z přenesené daňové povinnosti při nákupu nebo prodeji)</br>-   **Importní DPH.** </br>Pro každý klasifikátor transakcí je k dispozici také klasifikátor dobropisu. Například jeden z těchto klasifikátorů je **PurchaseCreditNote** (nákupní dobropis).</br>Nezapomeňte vytvořit dva řádky pro každý kód DPH: jeden s hodnotou klasifikátoru transakce a jeden s klasifikátorem transakce pro hodnotu dobropisu. |


    > [!NOTE]
    > Přiřaďte všechny kódy DPH k výsledkům vyhledávání. Pokud by některé kódy DPH neměly generovat hodnoty v přiznání k DPH, přiřaďte je k výsledku vyhledávání **Ostatní**.

    ![Stránka specifické parametry aplikace.](media/7db74920fad66a0db7fad60758698cc0.png)


5. V poli **Stav** změňte hodnotu na **Dokončeno**.

### <a name="set-up-the-vat-reporting-format-for-preview-amounts-in-excel"></a>Nastavte formát hlášení DPH pro náhled částky v Excelu

1. V pracovním prostoru **Správa funkcí** najděte a vyberte funkci **Sestavy formátu výkazu DPH**. funkci v seznamu a poté vyberte **Povolit nyní**.
2. Přejděte do **Hlavní knihy** > **Nastavení** > **Parametry hlavní knihy**.
3. Na kartě **DPH** na záložce **Možnosti daně** v poli **Mapování formátu přiznání k DPH** vyberte formát ER **Přiznání k DPH Excel (DK)**.

   Tento formát je vytištěn při spuštění sestavy **Vykázat DPH pro období vyrovnání**. Vytiskne se také při výběru **Tisk** na stránce **Platby DPH**.

4. Na stránce **Finanční úřady** vyberte finanční úřad a poté v poli **Rozvržení sestavy** vyberte **Výchozí**.

Pokud konfigurujete přiznání k DPH v právnické osobě, která má [více registrací k DPH](emea-reporting-for-multiple-vat-registrations.md), postupujte následovně.

1. Přejděte do nabídky **Hlavní kniha** \> **Nastavení** \> **Parametry hlavní knihy**.
2. Na kartě **DPH** na záložce **Elektronické hlášení pro země/oblasti**, na řádku pro **DNK** vyberte formát ER **Přiznání k DPH Excel (DK)**.

## <a name="set-up-electronic-messages"></a>Nastavení elektronických zpráv

### <a name="download-and-import-the-data-package-that-has-example-settings-for-electronic-messages"></a>Stažení a import balíčku dat, který obsahuje ukázkové nastavení elektronických zpráv

Datový balíček obsahuje nastavení elektronické zprávy, která slouží k náhledu přiznání k DPH ve formátu Excel. Tato nastavení můžete rozšířit nebo vytvořit vlastní. Další informace, jak pracovat s elektronickými zprávami a jak vytvořit vlastní nastavení, najdete v části [Elektronické zasílání zpráv](../general-ledger/electronic-messaging.md).

1. V [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/v2), v knihovně Sdílený majetek vyberte **Datový balíček** jako typ majetku a poté stáhněte **Balíček přiznání k DPH DK**. Stažený soubor má název **DK VAT declaration package.zip**.
2. Ve Finance , v pracovním prostoru **Správa dat** vyberte **Importovat**.
3. Na pevné záložce **Import** v poli **Název slupiny** zadejte název úlohy.
4. Na záložce s náhledem **Vybrané entity** vyberte **Přidat soubor**.
5. V dialogovém okně **Přidat soubor** ověřte, že je pole **Formát zdrojových dat** nastaveno na **Balíček**, vyberte **Nahrát a přidat** a poté vyberte soubor zip, který jste stáhli dříve.
6. Vyberte **Zavřít**.
7. Po nahrání datových entit v podokně akcí vyberte **Importovat**.
8. Přejděte na **Daň** > **Dotazy a sestavy** > **Elektronické zprávy** > **Elektronické zprávy** a ověřte zpracování importovaných elektronických zpráv (**DK Přiznání k DPH**).

### <a name="configure-electronic-messages"></a>Konfigurace elektronických zpráv

1. Přejděte na **Daň** > **Nastavení** > **Elektronické zprávy** > **Akce naplnění záznamů**.
2. Vyberte řádek pro **DK Vyplňte záznamy vratky DPH** a poté vyberte **Upravit dotaz**.
3. Pomocí filtru vyberte období vyrovnání, která chcete zahrnout do sestavy.
4. Pokud musíte vykazovat daňové transakce z jiných období vyrovnání v jiném přiznání, vytvořte novou akci **Naplnit záznamy** a vyberte příslušná období vypořádání.

## <a name="preview-the-vat-declaration-in-excel"></a>Náhled přiznání k DPH v Excelu

### <a name="preview-the-vat-declaration-in-excel-from-the-report-sales-tax-for-settlement-period-periodic-task"></a><a name="preview-vat-excel"></a>Náhled přiznání k DPH v aplikaci Excel z periodické úlohy Vykázat DPH pro období vyrovnání

1. Přejděte na **Daň** > **Periodické úlohy** > **Prohlášení** > **DPH** > **Vykázat DPH pro období vyrovnání**.
2. Vyberte hodnotu v poli **Období vyrovnání**.
3. V poli **Verze platby DPH** vyberte některou z následujících hodnot:

    - **Originál**: Vygenerujte sestavu pro transakce DPH původní platby DPH nebo před vygenerováním platby DPH.
    - **Opravy**: Generuje sestavu transakcí DPH všech dalších plateb DPH za dané období.
    - **Celkový seznam**: Generuje sestavu všech transakcí DPH za dané období, včetně původní a všech oprav.

4. V poli **Od data** vyberte počáteční datum období vykazování.
5. Vyberte **OK** a zkontrolujte sestavu Excel.

### <a name="settle-and-post-sales-tax"></a>Vyrovnat a zaúčtovat DPH

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
> Sestava je vygenerována pouze pro vybraný řádek platby DPH. Pokud musíte vygenerovat např. opravné přiznání, které obsahuje všechny opravy za období, nebo náhradní přiznán, které obsahuje původní údaje a všechny opravy, použijte periodický úkol **Vykázat DPH za zúčtovací období**.

## <a name="generate-a-vat-declaration-from-electronic-messages"></a>Generování přiznání k DPH z elektronických zpráv

Když pro generování sestavy používáte elektronické zprávy, můžete shromažďovat daňové údaje od více právnických osob. Více informací naleznete v sekci [Spustit přiznání k DPH pro více právnických osob](#run-vat-declaration) dále v tomto článku.

Následující postup platí pro příklad zpracování elektronické zprávy, který jste předtím importovali z knihovny sdíleného majetku LCS.

1. Přejděte na **Daň \> Dotazy a sestavy \> Elektronické zprávy \> Elektronické zprávy**.
2. V levém podokně vyberte **DK Přiznání k DPH**.
3. Na záložce s náhledem **Zprávy** vyberte **Novýá** a poté v dialogovém okně **Spuštění zpracování** vyberte **OK**.
4. Vyberte řádek zprávy, který je vytvořen, zadejte popis a poté zadejte počáteční a konečné datum přiznání.

   > [!NOTE]
   > Kroky 5 až 7 jsou volitelné.

5. Volitelné: Na záložce s náhledem **Zprávy** vyberte **Shromažďovat data** a potom vyberte **OK**. Do zprávy se přidají platby DPH, které byly vygenerovány dříve. Více informací naleznete v předchozích části [Vyrovnat a zaúčtovat DPH](#settle-and-post-sales-tax) v tomto článku. Pokud tento krok přeskočíte, stále můžete vygenerovat přiznání k DPH pomocí pole **Verze přiznání k DPH** v dialogovém okně **Přiznání**.
6. Volitelné: Na kartě s náhledem **Položky zprávy** zkontrolujte platby DPH, které jsou přeneseny ke zpracování. Ve výchozím nastavení jsou zahrnuty všechny platby DPH ve vybraném období, které nebyly zahrnuty v žádné jiné zprávě stejného zpracování.
7. Volitelně: Vyberte **Původní dokument**, chcete-li zkontrolovat platby DPH, nebo zvolte **Odstranit**, chcete-li vyloučit ze zpracování platby DPH. Pokud tento krok přeskočíte, stále můžete vygenerovat přiznání k DPH pomocí pole **Verze přiznání k DPH** v dialogovém okně **Přiznání**.
8. Na záložce s náhledem **Zprávy** vyberte **Aktualizovat status**. V dialogovém okně **Aktualizovat status** vyberte **Připraveno k vygenerování** a poté vyberte **OK**. Ověřte, že se stav zprávy změnil na **Připraveno k vygenerování**.
9. Vyberte **Generovat sestavu**. Chcete-li zobrazit náhled částek přiznání k DPH, v dialogovém okně **Spustit zpracování** vyberte **Náhled sestavy** a potom vyberte **OK**.
10. V dialogovém okně **Parametry elektronického hlášení** nastavte pole podle popisu v části [Náhled přiznání k DPH v aplikaci Excel z periodické úlohy Vykázat DPH pro období vyrovnání](#preview-vat-excel) výše v tomto článku a poté vyberte **OK**.
11. Vyberte tlačítko **Příloha** (symbol sponky) v pravém horním rohu stránky, a poté výběrem příkazu **Otevřít** soubor otevřete. Zkontrolujte částky v dokumentu Excel.

## <a name="run-a-vat-declaration-for-multiple-legal-entities"></a><a name="run-vat-declaration"></a>Spuštění přiznání k DPH pro několik právnických osob

Chcete-li použít formáty k vykázání přiznání k DPH pro skupinu právnických osob, musíte nejprve nastavit parametry formátů ER specifické pro aplikacipro kódy DPH ze všech požadovaných právnických osob.

### <a name="set-up-electronic-messages-to-collect-tax-data-from-several-legal-entities"></a>Vytvoření elektronických zpráv ke shromažďování daňových údajů od několika právnických osob

Chcete-li nastavit elektronické zprávy, které budou shromažďovat údaje od více právnických osob, postupujte takto.

1. Přejděte na **Pracovní prostory** > **Správa funkcí**.
2. Najděte a vyberte funkci **Mezipodnikové dotazy pro akce vyplnění záznamů** v seznamu a vyberte **Povolit nyní**.
3. Přejděte na **Daň** > **Nastavení** > **Elektronické zprávy** > **Akce naplnění záznamů**.
4. Na stránce **Akce vyplnění záznamů** vyberte řádek pro **DK Vyplnit záznamy vratky DPH**.

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
