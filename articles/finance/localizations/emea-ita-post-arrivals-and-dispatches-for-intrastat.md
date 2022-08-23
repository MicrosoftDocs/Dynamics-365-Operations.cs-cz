---
title: Zaúčtování příchozích a odchozích zásilek pro Intrastat
description: Tento článek ukazuje, jak zaúčtovat příchozí a odchozí zásilky pro Intrastat.
author: AdamTrukawka
ms.date: 08/23/2021
ms.topic: article
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: atrukawk
ms.search.validFrom: ''
ms.openlocfilehash: b6d46efd477f526c4bec3515086e10aa8172c579
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9280680"
---
# <a name="post-arrivals-and-dispatches-for-intrastat"></a>Zaúčtování příchozích a odchozích zásilek pro Intrastat

[!include [banner](../includes/banner.md)]

Tento článek ukazuje, jak zaúčtovat příchozí a odchozí zásilky pro Intrastat. Příklad používá právnickou osobu **ITCO**.

## <a name="setup"></a>Nastavení

1. Importujte nejnovější verzi následujících konfigurací elektronického hlášení (ER):

    - Modul Intrastat
    - Sestava Intrastat
    - Intrastat (IT)

    Další informace viz [Stáhněte si konfigurace elektronického výkaznictví z Globálního úložiště konfigurační služby](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md).

2. V Microsoft Dynamics 365 Finance definujte následující číselné sekvence jako souvislé: **Gen\_397**, **Acco\_16403**, **Gen\_407** a **PUR\_EU**.

    1. Přejděte na **Správa organizace** > **Číselné řady** > **Číselné řady**.
    2. V mřížce vyberte jeden z kódů číselné řady.
    3. V podokně akcí vyberte **Upravit**.
    4. Na pevné záložce **Obecné** v části **Nastavení** nastavte možnost **Souvislé** na **Ano**.
    5. V podokně akcí vyberte **Uložit**.

3. Nastavit adresu skladu.

    1. Přejděte na **Řízení skladu** &gt; **Nastavení** &gt; **Sklad** &gt; **Sklady**.
    2. V seznamu vyberte sklad **11**.
    3. Na záložce s náhledem **Adresa** vyberte **Přidat**.
    4. V dialogovém okně **Nová** **adresa** v poli **Název** **nebo** **popis** zadejte **Hlavní**.
    5. V poli **Země/oblast** vyberte **ITA (Itálie)**.
    6. V poli **Město** vyberte **Aprilia**.
    7. Vyberte **OK**.

4. Nastavit kódy transakcí.

    1. Přejděte na **Daň** > **Nastavení** > **Zahraniční obchod** > **Kódy transakcí**.
    2. Vyberte **Nový** a nastavte kód transakce pro převody majetku.

        - Do pole **Kód transakce** zadejte **1**.
        - V poli **Název** zadejte **Převod majetku**.

    3. Vyberte **Nový** a nastavte kód transakce pro vratky.

        - Do pole **Kód** **transakce** zadejte **2**.
        - Do pole **Název** zadejte **Vrácení zboží**.

5.  Nastavte parametry zahraničního obchodu.

    1. Přejděte na **Daň** > **Nastavení** > **Zahraniční obchod** > **Parametry zahraničního obchodu**.
    2. Na kartě **Intrastat** na záložce s náhledem **Obecné** v poli **Kód** **transakce** vyberte **1**.
    3. V poli **Dobropis** vyberte **2**.
    4. V poli **Období vykazování prodeje** vyberte **Měsíc**.
    5. V poli **Období vykazování nákupu** vyberte **Měsíc**.
    6. Na záložce s náhledem **Elektronické výkaznictví** v poli **Mapování formátu souboru** vyberte **Intrastat (IT)**.
    7. V poli **Mapování formátu vykazování** vyberte **Sestava Intrastat**.
    8. Na pevné záložce **Hierarchie komoditních kódů** v poli **Hierarchie kategorií** vyberte **Intrastat**.
    9. Na pevné záložce **Statistická hodnota** nastavte možnost **Tiskněte a exportujte statistické údaje** na **Ano**.
    10. Na kartě **Vlastnosti země/regionu** ověřte, zda existují následující řádky.

        | **Strana/země/oblast** | **Kód Intrastat** | **Měna** | **Typ země/oblasti** |
        |--------------------------|--------------------|--------------|-------------------------|
        | ITA                      | IT                 | EUR          | Domácí                |
        | SMR                      | SM                 | EUR          | Zvláštní domácí        |

    11. Na panelu nástrojů vyberte možnost **Nový** a vytvořte následující řádek.

        | **Strana/země/oblast** | **Kód Intrastat** | **Měna** | **Typ země/oblasti** |
        |--------------------------|--------------------|--------------|-------------------------|
        | DNK                      | DK                 | DKK          | EU                      |

6. Nastavit čísla osvobození od daně.

    1. Přejděte na **Daň** > **Nastavení** > **DPH** > **čísla osvobození od daně**.
    2. V podokně akcí vyberte možnost **Nový** a vytvořte následující řádky.

        | **Země nebo oblast** | **DIČ** | **Název společnosti** |
        |--------------------|-----------------------|------------------|
        | DEU                | DE3456789012          | UE VENDOR        |
        | DNK                | DK0987654321          | Odběratel ER      |

7. Nastavte adresu dodavatele.

    1. Přejděte do části **Pohledávky** &gt; **Dodavatelé** &gt; **Všichni dodavatelé**.
    2. V mřížce vyberte **UE Vendor**.
    3. Na záložce s náhledem **Adresy** vyberte **Přidat**.
    4. V dialogovém okně **Nová adresa** v poli **Název nebo popis** zadejte **Německo**.
    5. V poli **Země/region** vyberte **DEU**.
    6. Výběrem **OK** vytvořte novou adresu.
    7. Na pevné záložce **Faktura a dodávky** v sekci **DPH** v poli **Číslo osvobození od daně** vyberte **Vše** a pak vyberte **DE1234567890**.
    8. V podokně akcí vyberte **Uložit**.

8. Nastavte adresy odběratelů.

    1. Přejděte na **Pohledávky** > **Odběratelé** > **Všichni odběratelé**.
    2. V mřížce vyberte **ITCO-000001**.
    3. Na záložce s náhledem **Adresy** vyberte **Upravit**.
    4. V dialogovém okně **Nová adresa** v poli **Název nebo popis** zadejte **San Marino**.
    5. V poli **Země/region** vyberte **SMR**.
    6. Výběrem **OK** vytvořte novou adresu.
    7. Na pevné záložce **Faktura a dodání** v sekci **Faktura** v poli **Fakturační účet** vyberte **ITCO-000001**.
    8. V poli **Skupina číselných řad** vyberte **IT\_VENDOM**.
    9. V podokně akcí zvolte **Uložit** a zavřete stránku.
    10. Na stránce **Všichni odběratelé** v mřížce vyberte **ITCO-000002**.
    11. Na záložce s náhledem **Adresy** vyberte **Přidat**.
    12. V dialogovém okně **Nová adresa** v poli **Název nebo popis** zadejte **Dánsko**.
    13. V poli **Země/region** vyberte **DNK**.
    14. Výběrem **OK** vytvořte novou adresu.
    15. Na záložce s náhledem **Demografie prodeje** v poli **Měna** vyberte **DKK**.
    16. Na pevné záložce **Faktura a dodávky** v sekci **DPH** v poli **Skupina DPH** vyberte **IT\_PUREU**.
    17. V poli **Číslo osvobození od daně** vyberte **Vše** a poté vyberte **DK0987654321**.
    18. V podokně akcí vyberte **Uložit**.

9. Nastavení hierarchie kategorií.

    1. Přejděte do nabídky **Řízení informací o produktech** > **Nastavení** > **Kategorie a atributy** > **Hierarchie kategorií**.
    2. V mřížce vyberte **Intrastat**.
    3. V podokně akcí vyberte možnost **Nový uzel kategorií**.
    4. Do pole **Název** zadejte **Servis**.
    5. Do pole **Kód** zadejte **123456**.
    6. V podokně akcí vyberte **Uložit**.

10. Nastavení produktů.

    1. Přejděte na **Řízení informací o produktech** > **Produkty** > **Uvolněné produkty**.
    2. V mřížce vyberte **ITEM**.
    3. Na pevné záložce **Nákup** v sekci **Správa** v poli **Dodavatgegl** vyberte **ITCO-000001**.
    4. Na záložce s náhledem **Zahraniční obchod** v sekci **Intrastat** v poli **Komodita** vyberte **\[100 200 30\] Speaker**.
    5. V sekci **Původ** v poli **Země/oblast** vyberte **DEU**.
    6. V poli **Stát/provincie** vyberte možnost **BE**.
    7. Na záložce s náhledem **Správa zásob** v sekci **Čisté měření** v poli **Čistá hmotnost** zadejte **5**.
    8. V podokně akcí vyberte **Uložit**.
    9. Na stránce **Vydané produkty** v mřížce vyberte **Servisní položka**.
    10. Na záložce s náhledem **Zahraniční obchod** v sekci **Intrastat** v poli **Komodita** vyberte **\[123456\] Servis**.
    11. V podokně akcí vyberte **Uložit**.

11. Nastavení metod dopravy.

    1. Přejděte na **Daň** > **Nastavení** > **Zahraniční obchod** > **Metoda dopravy**.
    2. V podokně akcí vyberte možnost **Nový** a vytvořte následující metody dopravy.

        | **Přeprava** | **Popis** |
        |---------------|-----------------|
        | 1             | Silnice            |
        | 2             | Letecky             |

12. Nastavit způsob dodání.

    1. Přejděte na **Zásobování a zdroje** > **Nastavení** > **Distribuce** > **Způsoby doručení**.
    2. V podokně akcí zvolte **Nový**.
    3. V poli **Způsob dodání** zadejte **1**.
    4. V poli **Popis** zadejte **Kamion**.
    5. Na pevné záložce **Zahraniční obchod** v poli **Přeprava** vyberte **1 Silnice**.
    6. V podokně akcí vyberte **Uložit**.

13. Nastavit podmínky dodání.

    1. Přejděte na **Závazky** > **Nastavení** > **Podmínky doručení**.
    2. V seznamu vyberte **CFR**.
    3. Na pevné záložce **Obecné** v poli **Kód Intrasat** zadejte **1**.

## <a name="post-arrivals-for-intrastat"></a>Příchozí zásilky pro Intrastat

### <a name="purchase-goods-by-using-a-purchase-order"></a>Nakupujte zboží pomocí nákupní objednávky

Tato část příkladu ukazuje, jak použít nákupní objednávku k nákupu zboží (položek) ze zemí Evropské unie (EU).

1. Přejděte na **Závazky** > **Nákupní objednávky** > **Všechny nákupní objednávky**.
2.  V podokně akcí zvolte **Nový**.
3.  V dialogovém okně **Vytvoření nákupní objednávky** v poli **Účet dodavatele** vyberte **UE Vendor**.
4.  Na pevné záložce **Správa** v poli **Jazyk** vyberte **it**.
5.  Vyberte **OK**.
6.  V zobrazení **Záhlaví** na pevné záložce **Zahraniční** **obchod** ověřte, že je pole **Kód transakce** nastaveno na **1**.
7.  Ověřte, že pole **Kraj původu/destinace** je nastaveno na **RM**.
8.  Na pevné záložce **Doručení** v oddíle **Doručení** v poli **Režim doručení** vyberte **1**.
9.  V poli **Dodacé podmínky** vyberte **CFR**.
10. Na kartě **Řádky** na záložce s náhledem **Řádky nákupní objednávky** v poli **Číslo položky** vyberte **Položka**.
11. V poli **Pracoviště** zvolte **1**.
12. V poli **Sklad** zvolte **11**.
13. Do pole **Množství** zadejte **10**.
14. Do pole **Jednotková cena** zadejte **100**.
15. Na kartě **Nastavení** v sekci **DPH** v poli **Skupina DPH položek** vyberte **22%EU**.
16. V podokně akcí na kartě **Nákup** ve skupině **Akce** zvolte **Potvrdit**.
17. V podokně akcí na kartě **Faktura** ve skupině **Generovat** zvolte **Faktura**.
18. V podokně akcí vyberte **Výchozí od**.
19. V poli **Výchozí množství pro řádky** vyberte **Objednané množství** a vyberte **OK**.
20. Na pevné záložce **Záhlaví faktury dodavatele** v sekci **Identifikace faktury** v poli **Číslo** zadejte **0001**.
21. V sekci **Termíny faktur** v poli **Datum faktury** vyberte **9.7.2021**.
22. Chcete-li zaúčtovat fakturu, vyberte **Zaúčtovat** z akčního podokna.

### <a name="purchase-services-by-using-a-vendor-invoice"></a>Nakupujte služby pomocí faktury dodavatele

Tato část příkladu ukazuje, jak použít fakturu dodavatele k nákupu služeb ze zemí Evropské unie.

1. Přejděte na **Závazky** > **Faktury** > **Deník faktur**.
2. V podokně akcí zvolte **Nový**.
3. V poli **Název** vyberte **VEND\_EUINV**.
4. V podokně akcí zvolte **Řádky**.
5. V poli **Datum** zadejte hododnotu **7/9/2021**.
6. V poli **Typ účtu** vyberte **Dodavatel**.
7. V poli **Účet** vyberte **UE Vendor**.
8. Do pole **Datum faktury** vyberte **9. 7. 2021**.
9. Do pole **Faktura** zadejte **ITA-0004**.
10. Do pole **Kredit** zadejte **120000**.
11. V poli **typ** **protiúčtu** vyberte **Hlavní kniha**.
12. V poli **Protiúčet** vyberte **110130**.
13. V poli **Skupina DPH** vyberte položku **IT\_PUREU**.
14. V poli **Skupina DPH položek** vyberte **22%EU**.
15. Na kartě **Zahraniční obchod** proveďte následující kroky:

    1. Do pole **Kód transakce** zadejte **1**.
    2. V poli **Doprava** vyberte **2 Vzduch**.
    3. V poli **Komodita** vyberte **\[123456\] Service**.
    4. V poli **Země/region** vyberte **ITA**.
    5. V poli **Stát/provincie** vyberte možnost **LAZ**.
    6. V poli **Okres původu / určení** vyberte **LT**.


16. V podokně akcí zvolte **Zaúčtovat**.
17. Vytvořte prohlášení Intrastat pro příjezdy.

    1. Přejděte na **Daň** > **Deklarace** > **Zahraniční obchod** > **Intrastat**.
    2. V podokně akcí zvolte **Převod**.
    3. V dialogovém okně **Intrastat (přenos)** nastavte možnost **Faktura dodavatele** na **Ano**.
    4. Vyberte **OK** pro přenesení transakcí a pak zkontrolujte deník Intrastat.

   ![Stránka deníku Intrastat, karta Přehled.](media/ita_intrastat_journal_vendor_invoice.png)

18. Zkontrolujte kartu **Všeobecné** pro nákupní objednávku.

    ![Podrobnosti řádků deníku Intrastat pro nákupní objednávku](media/ita_intrastat_journal_purchase_order_line_details.png)

19. Zkontrolujte kartu **Všeobecné** pro fakturu dodavatele.

    ![Podrobnosti řádku deníku Intrastat pro fakturu dodavatele](media/ita_intrastat_journal_vendor_invoice_line_details.png)

20. Generování sestavy Intrasat pro přijaté položky.

    1. V podokně akcí vyberte **Výstup** > **Sestava**.
    2. V dialogovém okně **Sestava Intrastat** v sekci **Datum** v poli **Od data** vyberte **1.7.2021**.
    3. V poli **Do data** vyberte **31/7/2021**.
    4. V sekci **Možnosti exportu** nastavte možnost **Generovat soubor** a **Generovat sestavu** na **Ano**.
    5. Do pole **Název souboru** zadejte **Soubor příchozích položek**.
    6. Do pole **Název souboru sestavy** zadejte **Sestava příchozích položek**.
    7. V poli **Směr** vyberte hodnotu **Příchozí**.
    8. Do pole **Referenční číslo** zadejte **123456**.
    9. Vyberte **OK**, chcete-li vygenerovat sestavu Intrastat a soubor Intrastat a zkontrolovat je.

    Následující obrázek znázorňuje příklad sestavy Intrasat.

    ![Přehled příchozích položek Intrastat.](media/ita_intrastat_arrivals_report.png)

    Následující obrázek znázorňuje příklad souboru Intrasat.

    ![Soubor příchozích položek Intrastat.](media/ita_intrastat_arrivals_file.png)

## <a name="post-dispatches-for-intrastat"></a>Odchozí zásilky pro Intrastat

### <a name="sell-goods-by-using-a-sales-order"></a>Prodávejte zboží pomocí prodejní objednávky

Tato část příkladu ukazuje, jak použít prodejní objednávku k prodeji zboží (položek) do zemí Evropské unie (EU).

1. Přejděte na **Pohledávky** > **Objednávky** > **Všechny prodejní objednávky**.
2. V podokně akcí zvolte **Nový**.
3. V dialogovém okně **Vytvořit prodejní objednávku** vyberte v poli **Účet odběratele** hodnotu **ITCO-000002**.
4. Vyberte **OK**.
5. V zobrazení **Záhlaví** na pevné záložce **Doručení** v sekci **Různé info o doručení** v poli **Způsob dodání** vyberte **1 kamion**.
6. V poli **Dodacé podmínky** vyberte **CFR**.
7. V zobrazení **Řádky** na záložce s náhledem **Řádky prodejní objednávky** v poli **Číslo položky** vyberte **ITEM**.
8. Do pole **Množství** zadejte **50**.
9. V poli **Pracoviště** zvolte **1**.
10. V poli **Sklad** zvolte **11**.
11. Do pole **Jednotková cena** zadejte **250**.
12. Na pevné záložce **Podrobnosti řádků** Nn kartě **Nastavení** v sekci **DPH** v poli **Skupina DPH položek** vyberte **22%EU**.
13. V podokně akcí vyberte **Uložit**.
14. V podokně akcí na kartě **Faktura** ve skupině **Generovat** vyberte **Fakturu** a vytvořte fakturu pro objednávku.
15. V dialogovém okně **Účtování faktury** na pevné záložce **Parametry** v sekci **Parametr**, v poli **Množství** vyberte **Všechny**.
16. Na pevné záložce **Nastavení** v poli **Datum** **faktury** vyberte **9.7.2021**.
17. Vyberte **OK**.
18. Kontrola řádků v deníku Intrasat.

    1. Přejděte na **Daň** > **Deklarace** > **Zahraniční obchod** > **Intrastat**.
    2. V podokně akcí zvolte **Převod**.
    3. V dialogovém okně **Intrastat (přenos)** nastavte možnost **Zákaznická faktura** na **Ano**.
    4. Vyberte **OK** pro přenesení transakcí a zkontrolujte deník Intrastat. Transakce dobropisu je označena jako opravná a má zápornou částku faktury.

        ![Stránka deníku Intrastat](media/ita_intrastat_journal_sales_order.png)

        ![Podrobnosti řádků deníku Intrastat pro prodejní objednávku](media/ita_intrastat_journal_sales_order_line_details.png)

### <a name="return-goods-by-using-a-credit-note"></a>Vraťte zboží pomocí dobropisu

Tato část příkladu ukazuje, jak použít dobropis k vrácení zboží (položek) ze zemí Evropské unie (EU).

1. Přejděte na **Pohledávky** > **Objednávky** > **Všechny prodejní objednávky**.
2. V podokně akcí zvolte **Nový**.
3. V dialogovém okně **Vytvořit prodejní objednávku** vyberte v poli **Účet odběratele** hodnotu **ITCO-000002**.
4. Vyberte **OK**.
5. V zobrazení **Záhlaví** na pevné záložce **Doručení** v sekci **Různé info o doručení** v poli **Způsob dodání** vyberte **1 kamion**.
6. V poli **Dodacé podmínky** vyberte **CFR**.
7. Na pevné záložce **Zahraniční obchod** v poli **Kód přepravy** vyberte **2**.
8. Na kartě **Řádky** na záložce s náhledem **Řádky prodejní objednávky** v poli **Číslo položky** vyberte **ITEM**.
9. Zadejte číslo **-10** do pole **Množství**.
10. V poli **Pracoviště** zvolte **1**.
11. V poli **Sklad** zvolte **11**.
12. Do pole **Jednotková cena** zadejte **250**.
13. Na pevné záložce **Podrobnosti řádků** Nn kartě **Nastavení** v sekci **DPH** v poli **Skupina DPH položek** vyberte **22%EU**.
14. V sekci **Vrácená objednávka** v poli **ID šarže vrácení** vyberte šarži, kterou jste vytvořili dříve.
15. V podokně akcí vyberte **Uložit**.
16. V podokně akcí na kartě **Faktura** ve skupině **Generovat** vyberte **Fakturu** a vytvořte fakturu pro objednávku.
17. Na pevné záložce **Parametry** v sekci **Parametr**  v poli **Množství** vyberte **Vše**.
18. V dialogovém okně **Účtování faktury** na pevné záložce **Nastavit** v poli **Datum** **faktury** vyberte **9.7.2021**.
19. Výběrem tlačítka **OK** zaúčtujte fakturu.
20. Kontrola řádků v deníku Intrasat.

    1. Přejděte na **Daň** > **Deklarace** > **Zahraniční obchod** > **Intrastat**.
    2. V podokně akcí zvolte **Převod**.
    3. V dialogovém okně **Intrastat (přenos)** nastavte možnost **Zákaznická faktura** na **Ano**.
    4. Vyberte **OK** pro přenesení transakcí a zkontrolujte deník Intrastat. Transakce dobropisu je označena jako opravná a má zápornou částku faktury.

    ![Dobropis deníku Intrastat](media/ita_intrastat_journal_credit_note.png)

    ![Podrobnosti řádku deníku Intrastat pro dobropis](media/ita_intrastat_journal_credit_note_line_details.png)

### <a name="sell-goods-to-san-marino-by-using-a-sales-order"></a>Prodávejte zboží do San Marina pomocí prodejní objednávky

Tato část příkladu ukazuje, jak použít prodejní objednávku k nákupu zboží (položek) do Sana Marina.

1. Přejděte na **Pohledávky** > **Objednávky** > **Všechny prodejní objednávky**.
2. V podokně akcí zvolte **Nový**.
3. V dialogovém okně **Vytvořit prodejní objednávku** vyberte v poli **Účet odběratele** hodnotu **ITCO-000001**.
4. Vyberte **OK**.
5. V zobrazení **Záhlaví** na pevné záložce **Doručení** v sekci **Různé info o doručení** v poli **Způsob dodání** vyberte **1**.
6. V poli **Dodacé podmínky** vyberte **CFR**.
7. Na kartě **Řádky** na záložce s náhledem **Řádky prodejní objednávky** v poli **Číslo položky** vyberte **ITEM**.
8. Do pole **Množství** zadejte **30**.
9. V poli **Pracoviště** zvolte **1**.
10. V poli **Sklad** zvolte **11**.
11. Do pole **Jednotková cena** zadejte **200**.
12. V podokně akcí vyberte **Uložit**.
13. V podokně akcí na kartě **Faktura** ve skupině **Generovat** vyberte **Fakturu** a vytvořte fakturu pro objednávku.
14. Na pevné záložce **Parametry** v sekci **Parametr**  v poli **Množství** vyberte **Vše**.
15. V dialogovém okně **Účtování faktury** na pevné záložce **Nastavit** v poli **Datum** **faktury** vyberte **9.7.2021**.
16. Výběrem tlačítka **OK** zaúčtujte fakturu.
17. Kontrola řádků v deníku Intrasat.

    1. Přejděte na **Daň** > **Deklarace** > **Zahraniční obchod** > **Intrastat**.
    2. V podokně akcí zvolte **Převod**.
    3. V dialogovém okně **Intrastat (přenos)** nastavte možnost **Zákaznická faktura** na **Ano**.
    4. Vyberte **OK** pro přenesení transakcí a zkontrolujte deník Intrastat.

   ![Deník Intrastat pro San Marino](media/ita_intrastat_journal_sales_order_san_marino.png)

   ![Podrobnosti řádku deníku Intrastat pro San Marino](media/ita_intrastat_journal_sales_order_san_marino_line_details.png)

18. Vytvořte prohlášení Intrastat pro odchozí položky.

    1. Přejděte na **Daň** &gt; **Deklarace** &gt; **Zahraniční obchod** &gt; **Intrastat**.
    2. V podokně akcí vyberte **Výstup** &gt; **Sestava**.
    3. V dialogovém okně **Sestava Intrastat** v sekci **Datum** v poli **Od data** vyberte **1.7.2021**.
    4. V poli **Do data** vyberte **31/7/2021**.
    5. V sekci **Možnosti exportu** nastavte možnost **Generovat soubor** a **Generovat sestavu** na **Ano**.
    6. Do pole **Název souboru** zadejte **Soubor odchozích položek**.
    7. Do pole **Název souboru sestavy** zadejte **Sestava odchozích položek**.
    8. V poli **Směr** vyberte hodnotu **Expedice**.
    9. Do pole **Referenční číslo** zadejte **98754**.
    10. Vyberte **OK**, chcete-li vygenerovat sestavu Intrastat a soubor Intrastat.

        Následující obrázek znázorňuje příklad vytisknuté sestavy Intrasat.

        ![Sestava Intrastat](media/ita_intrastat_report_for_dispatches.png)

        Následující obrázek znázorňuje příklad vytisknutého souboru Intrasat.

        ![Soubor Intrastat pro odchozí položky](media/ita_intrastat_file_for_dispatches.png)
