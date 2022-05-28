---
title: Švédský Intrastat
description: Toto téma obsahuje informace o sestavě Intrastat ve Švédsku.
author: anasyash
ms.date: 8/24/2021
ms.topic: article
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: anasyash
ms.search.validFrom: ''
ms.openlocfilehash: 1031b93950e44fe3b1b6254bf1503b4c09d6fd10
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/07/2022
ms.locfileid: "8727391"
---
# <a name="swedish-intrastat"></a>Švédský Intrastat

[!include[banner](../includes/banner.md)]

Stránka **Intrastat** se použije pro vygenerování a nahlášení informací o obchodu mezi zeměmi Evropské unie (EU). Švédské prohlášení Intrastat obsahuje informace o obchodu se zbožím pro vykazování.

Ve švédské deklaraci Intrastat jsou zahrnuta následující pole:

   - ISO kód partnerské země
   - Kód transakce
   - Kód zboží
   - Dodatečná jednotka
   - Váha
   - Fakturovaná částka

## <a name="set-up-intrastat"></a>Vytvořit Intrastat

Importujte nejnovější verzi následujících konfigurací elektronického hlášení (ER):

   - Modul Intrastat
   - Sestava Intrastat
   - Intrastat (SE)

Další informace viz [Stáhněte si konfigurace elektronického výkaznictví z Globálního úložiště konfigurační služby](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md).

## <a name="set-up-foreign-trade-parameters"></a>Nastavit parametry zahraničního obchodu

1. V Microsoft Dynamics 365 Finance přejděte na **Daň** > **Nastavení** > **Parametry zahraničního obchodu**.
2. Na kartě **Intrastat** na pevné záložce **Elektronické hlášení** v poli **Mapování formátu souboru** vyberte **Intrastat (SE)**.
3. V poli **Mapování formátu sestavy** vyberte **Sestava Intrastat**.
4. Na pevné záložce **Hierarchie komoditních kódů** v poli **Hierarchie kategorií** vyberte **Intrastat**.
5. V poli **Kód transakce** vyberte kód transakce pro převody majetku. Tento kód použijete pro transakce, které provádí skutečné nebo plánované převody majetku v souvislosti s kompenzací (finanční nebo jinou). Použijete jej také pro opravy. Společnosti ve Švédsku používají jednomístné transakční kódy.
6. V poli **Dobropis** vyberte kód transakce pro vrácení zboží.
7. Na kartě **Vlastnosti země/oblasti** v poli **Země/oblast** jsou uvedeny všechny země nebo oblasti, se kterými vaše společnost obchoduje. Pro každou zemi, která je součástí EU, v poli **Typ země/oblasti** vyberte **EU**, aby se země objevila ve vaší sestavě Intrastat.

## <a name="set-up-the-product-parameters-for-the-intrastat-declaration"></a>Nastavte parametry produktu pro prohlášení Intrastat

1. Přejděte na **Řízení informací o produktech** > **Produkty** > **Uvolněné produkty**.
2. V mřížce vyberte produkt.
3. Na pevné záložce **Zahraniční obchod** v sekci **Intrastat** v poli **Komodita** vyberte příslušný kód komodity.
4. Na záložce s náhledem **Správa zásob** v poli **Čistá hmotnost** zadejte hmotnost produktů v kilogramech.
5. Přejděte na **Daň** > **Nastavení** > **Zahraniční obchod** > **Komprese Intrastatu** a vyberte pole, která mají být porovnána po shrnutí informací Intrastat. Pro švédský Intrastat vyberte následující pole:

    - Zboží
    - Kód transakce
    - Směr
    - Země nebo oblast
    - Oprava
    - Faktura

## <a name="intrastat-transfer"></a>Přenos Intrastat

Na stránce **Intrastat** v podokně akcí můžete vybrat **Přenos** k automatickému přenosu informací o obchodu uvnitř Společenství z vašich prodejních objednávek, faktury s volným textem, nákupní objednávky, faktury dodavatele, účtenky produktů dodavatele, faktury projektu a objednávky přenosu. Budou přeneseny pouze dokumenty, které mají jako zemi nebo region určení (pro odeslání) nebo zásilku (pro přijetí) zemi EU.

Alternativně můžete ručně zadat transakce výběrem **Nový** v podokně akcí.

### <a name="generate-an-intrastat-report"></a>Vygenerovat sestavu Intrastat

1. Přejděte na **Daň** > **Deklarace** > **Zahraniční obchod** > **Intrastat**.
2. V podokně akcí vyberte **Výstup** > **Sestava**.
3. V dialogovém okně **Sestava Intrastat** nastavte následující pole.

    | Pole            | popis                                                                                                                         |
    |------------------|-------------------------------------------------------------------------------------------------------------------------------------|
    | Od data        | Vyberte počáteční datum sestavy.                                                                                               |
    | Do data          | Vyberte koncové datum sestavy.                                                                                                 |
    | Generovat soubor    | Tuto možnost nastavte na **Ano**, chcete-li generovat soubor .txt pro vaši sestavu Intrasat.                                                       |
    | Název souboru        | Zadejte název souboru .txt.                                                                                                    |
    | Generovat sestavu  | Tuto možnost nastavte na **Ano**, chcete-li generovat soubor .xlxs pro vaši sestavu Intrasat.                                                     |
    | Název souboru sestavy | Zadejte název souboru .xlxs.                                                                                                   |
    | Směr        | Vyberte **Příjezdy** pro zprávu o příchozích do společenství. Vyberte **Odeslání** pro zprávu o odeslání v rámci komunity. |

4. Vyberte **OK** a zkontrolujte vygenerové sestavy.

## <a name="example"></a>Příklad

Tento příklad ukazuje, jak zaúčtovat příchozí a odchozí zásilky pro Intrastat. Použije právnickou osobu **DEMF**.

### <a name="preliminary-setup"></a>Předběžné nastavení

1. Přejděte na **Správa organizace** > **Organizace** > **Právnické osoby** a vyberte právnickou osobu **DEMF**.
2. Na pevné záložce **Adresy** vyberte **Upravit** a poté v poli **Země/oblast** vyberte **SWE (Švédsko)**.
3. Importujte nejnovější verzi následujících konfigurací ER:

    - Modul Intrastat
    - Sestava Intrastat
    - Intrastat (SE)

### <a name="create-transaction-codes"></a>Vytvoření kódů transakce

1. Přejděte na **Daň** > **Nastavení** > **Zahraniční obchod** > **Kódy transakcí**.
2. V podokně akcí zvolte **Nový**.
3. Do pole **Kód** **transakce** zadejte **1**.
4. Do pole **Název** zadejte **Běžné transakce**.
5. V podokně akcí vyberte **Uložit**.

### <a name="set-up-foreign-trade-parameters"></a>Nastavit parametry zahraničního obchodu

1. Přejděte na **Daň** > **Nastavení** > **Zahraniční obchod** > **Parametry zahraničního obchodu**.
2. Na kartě **Intrastat** na záložce s náhledem **Obecné** v poli **Kód** **transakce** vyberte **1**.
3. Na záložce s náhledem **Elektronické výkaznictví** v poli **Mapování formátu souboru** vyberte **Intrastat (SE)**.
4. V poli **Mapování formátu sestavy** vyberte **Sestava Intrastat**.
5. Na záložce s náhledem **Hierarchie komoditních kódů** v poli **Hierarchie kategorií** zkontrolujte, zda je vybrána možnost **Intrastat**.
6. Na kartě **Vlastností země/oblasti** vyberte **Nová**.
7. V poli **Země/oblast strany** vyberte **SWE**.
8. V poli **Typ země/oblasti** vyberte **Domácí**.
9. V poli **Země / region strany** vyberte **DEU** a poté v poli **Typ země / regionu** vyberte **EU**.

### <a name="set-up-product-information"></a>Nastavení Informací o produktu

1. Přejděte na **Řízení informací o produktech** > **Produkty** > **Uvolněné produkty**.
2. V mřížce vyberte **D0001**.
3. Na záložce s náhledem **Zahraniční obchod** v sekci **Intrastat** v poli **Komodita** vyberte **100 200 30**.
4. Na záložce s náhledem **Správa zásob** v sekci **Měření hmotnosti** v poli **Čistá hmotnost** zadejte **5**.
5. V podokně akcí vyberte **Uložit**.

### <a name="change-the-site-address"></a>Změňte adresu webu

1. Přejděte do nabídky **Warehouse Management** > **Nastavení** > **Sklad** > **Pracoviště**.
2. V mřížce vyberte **1**.
3. Na záložce s náhledem **Adresy** vyberte **Upravit**.
4. V dialogovém okně **Upravit adresu** v poli **Země/oblast** vyberte **SWE**.
5. Vyberte **OK**.

### <a name="create-a-sales-order-with-an-eu-customer"></a>Vytvořte prodejní objednávku se zákazníkem z EU

1. Přejděte na **Pohledávky** > **Objednávky** > **Všechny prodejní objednávky**.
2. V podokně akcí zvolte **Nový**.
3. V dialogovém okně **Vytvořit prodejní objednávku** na záložce s náhledem **Zákazník** v sekci **Zákazník** vyberte v poli **Účet zákazníka** hodnotu **DE-015**.
4. Na záložce s náhledem **Obecné** v sekci **Dimenze úložiště** v poli **Lokalita** vyberte **1**.
5. V poli **Sklad** zvolte **11**.
6. Vyberte **OK**.
7. Na kartě **Řádky** na záložce s náhledem **Řádky prodejní objednávky** v poli **Číslo položky** vyberte **D0001**. Poté do pole **Množství** zadejte **10**.
8. Na záložce s náhledem **Podrobnosti řádku** na kartě **Zahraniční obchod** zkontrolujte, zda jsou automaticky nastavena pole **Kód transakce** a **Komodita**.
9. V podokně akcí vyberte **Uložit**.
10. V podokně akcí na kartě **Faktura** v sekci **Generovat** zvolte **Faktura**.
11. V dialogovém okně **Účtování faktury** na pevné záložce **Parametry** v sekci **Parametr**, v poli **Množství** vyberte **Všechny**.
12. Výběrem tlačítka **OK** zaúčtujte fakturu.

### <a name="transfer-the-transaction-to-the-intrastat-journal-and-review-the-result"></a>Přeneste transakci do deníku Intrastat a zkontrolujte výsledek

1. Přejděte na **Daň** > **Deklarace** > **Zahraniční obchod** > **Intrastat**.
2. V podokně akcí zvolte **Převod**.
3. V dialogovém okně **Intrastat (přenos)** v sekci **Parametry** nastavte možnost **Zákaznická faktura** na **Ano**.
4. Vyberte **Filtr**.
5. V dialogovém okně **Filtr Intrastat** na kartě **Rozsah** vyberte první řádek a ujistěte se, že pole **Pole** je nastaveno na **Datum**.
6. V poli **Kritéria** vyberte aktuální datum.
7. Zvolte **OK** a zavřete dialogové okno **Filtr Intrastat**.
8. Vyberte **OK** pro zavření dialogového okna **Intrastat (převod)** a zkontrolujte výsledek. Řádek představuje prodejní objednávku, kterou jste vytvořili dříve.

    ![Řádky deníku Intrastat pro prodejní objednávku](media/swe_intrastat_journal_sales_order.png)

9. Vyberte řádek transakce a poté vyberte kartu **Obecné**, čímž zobrazíte další podrobnosti.

    ![Podrobnosti řádků deníku Intrastat pro prodejní objednávku](media/swe_intrastat_journal_sales_order_line_details.png)

10. V podokně akcí vyberte **Výstup** > **Sestava**.
11. V dialogovém okně **Sestava Intrastat** na pevné záložce **Parametry** v sekci **Datum** vyberte měsíc prodejní objednávky, kterou jste vytvořili.
12. V sekci **Možnosti** **exportu** nastavte možnost **Generovat soubor** na **Ano**. Potom do pole **Název souboru** zadejte požadovaný název.
13. Nastavte možnost **Generovat sestavu** na **Ano**. Potom do pole **Název souboru sestavy** zadejte požadovaný název.
14. V poli **Směr** vyberte hodnotu **Expedice**.
15. Vyberte **OK** a zkontrolujte vygenerovanou sestavu ve formátu .txt. Následující tabulka zobrazuje hodnoty v ukázkové sestavě.

    | ISO kód partnerské země | Kód transakce | Kód zboží | Dodatečná jednotka | Váha | Fakturovaná částka |
    |--------------------------|------------------|----------------|-----------------|--------|----------------|
    | IT                       | 1                | 10020030       | 0               | 50     | 3290           |

16. Zkontrolujte vygenerovaný soubor ve fromátu Excel.

    ![Sestava Intrastat](media/swe_intrastat_report_for_dispatches.png)

### <a name="create-a-purchase-order"></a>Vytvoření nákupní objednávky

1. Přejděte na **Závazky** > **Nákupní objednávky** > **Všechny nákupní objednávky**.
2. V podokně akcí zvolte **Nový**.
3. V dialogovém okně **Vytvoření nákupní objednávky** v poli **Účet dodavatele** vyberte **DE-001**.
4. Vyberte **OK**.
5. Na kartě **Záhlaví** na pevné záložce **Zahraniční** **obchod** ověřte, že je pole **Kód transakce** nastaveno na **1**.
6. Na kartě **Řádky** na záložce s náhledem **Řádky nákupní objednávky** v poli **Číslo položky** vyberte **D0001**. Poté do pole **Množství** zadejte **6**.
7. V podokně akcí na kartě **Nákup** ve skupině **Akce** zvolte **Potvrdit**.
8. V podokně akcí na kartě **Faktura** ve skupině **Generovat** zvolte **Faktura**.
9. V podokně akcí vyberte **Výchozí od**. V poli **Výchozí množství pro řádky** vyberte **Objednané množství**. Pak vyberte **OK**.
10. Na pevné záložce **Záhlaví faktury dodavatele** v sekci **Identifikace faktury** v poli **Číslo** zadejte **0001**.
11. Chcete-li zaúčtovat fakturu, vyberte **Zaúčtovat** z akčního podokna.

### <a name="create-an-intrastat-declaration-for-arrivals"></a>Vytvořte prohlášení Intrastat pro příchozí položky

1. Přejděte na **Daň** > **Deklarace** > **Zahraniční obchod** > **Intrastat**.
2. V podokně akcí zvolte **Převod**.
3. V dialogovém okně **Intrastat (přenos)** nastavte možnost **Faktura dodavatele** na **Ano**.
4. Vyberte **OK** pro přenesení transakcí a zkontrolujte deník Intrastat.

    ![Intrastat deník pro nákupní objednávku](media/swe_intrastat_journal_purchase_order.png)

5. Zkontrolujte kartu **Všeobecné** pro nákupní objednávku.

    ![Podrobnosti řádků deníku Intrastat pro nákupní objednávku](media/swe_intrastat_journal_purchase_order_line_details.png)

6. V podokně akcí vyberte **Výstup** > **Sestava**.
7. V dialogovém okně **Sestava Intrastat** na pevné záložce **Parametry** v sekci **Datum** vyberte měsíc prodejní objednávky, kterou jste vytvořili.
8. V sekci **Možnosti** **exportu** nastavte možnost **Generovat soubor** na **Ano**. Potom do pole **Název souboru** zadejte požadovaný název.
9. Nastavte možnost **Generovat sestavu** na **Ano**. Potom do pole **Název souboru sestavy** zadejte požadovaný název.
10. V poli **Směr** vyberte hodnotu **Příchozí**.
11. Vyberte **OK** a zkontrolujte vygenerovanou sestavu ve formátu .txt. Následující tabulka zobrazuje hodnoty v ukázkové sestavě.

    | ISO kód partnerské země | Kód transakce | Kód zboží | Dodatečná jednotka | Váha | Fakturovaná částka |
    |--------------------------|------------------|----------------|-----------------|--------|----------------|
    | IT                       | 1                | 10020030       | 0               | 30     | 1714           |

12. Zkontrolujte vygenerovaný soubor ve fromátu Excel.

    ![Přehled příchozích položek Intrastat](media/swe_intrastat_arrivals_report.png)
