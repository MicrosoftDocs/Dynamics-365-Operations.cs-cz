---
title: Německý Intrastat
description: Toto téma obsahuje informace o deklaraci Intrastat ve Německu.
author: anasyash
ms.date: 09/09/2021
ms.topic: article
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: anasyash
ms.search.validFrom: ''
ms.openlocfilehash: 50c412fdfd7118843d285cbb70e8e44847c9d4a5
ms.sourcegitcommit: 7a2001e4d01b252f5231d94b50945fd31562b2bc
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/15/2021
ms.locfileid: "7487918"
---
# <a name="german-intrastat"></a>Německý Intrastat

[!include [banner](../includes/banner.md)]

Stránka **Intrastat** se použije pro vygenerování a nahlášení informací o obchodu mezi zeměmi Evropské unie (EU). Německé prohlášení Intrastat obsahuje informace o obchodu se zbožím pro vykazování. Sestava je formátována podle pokynů německých úřadů, které jsou uvedeny na stránce [6.2 Deklarace souborů ve formátu INSTAT/XML](https://www-idev.destatis.de/idev/doc/intra_en/hilfe6_2.html).

V následující tabulce jsou uvedena pole, která jsou zahrnuta v německém prohlášení Intrastat.

| Pole | Expedice | Dovoz |
|-------------------------|-------------------------|-------------------------|
| Referenční období | X | X |
| Kód směru | X | X |
| Měna prohlášení Intrastat</br>**Poznámka**: Tato měna je <em>zúčtovací měna</em>. | X | X |
| Kód zboží | X | X |
| Název komodity | X | X |
| Doplňkový kód jednotky | X | X |
| Členský stát odeslání / místa určení | X | X |
| Čistá hmotnost | X | X |
| Množství v doplňkových jednotkách | X | X |
| Země/oblast původu |  | X |
| Fakturovaná částka | X |  |
| Statistická hodnota | X | X |
| Povaha transakce | X | X |
| Způsob dopravy | X | X |
| Kód oblasti</br>**Poznámka:**</br><ul></br><li>Pokud je zemí nebo oblastí původu Německo a faktura je určena k odeslání, zobrazí se kód Intrastat pro stát původu.</li></br><li>Pokud země nebo oblast původu není Německo a faktura je určena k odeslání, zobrazí se kód **99**.</li></br><li>Pokud je faktura za doručení, zobrazí se kód Intrastat pro stát.</li></br></ul> | X | X |
| Kód přístavu / letiště / vnitrozemského přístavu | X | X |
| Dodací podmínky | X | X |


## <a name="set-up-intrastat"></a>Vytvořit Intrastat

1. Nastavte kódy společnosti.

    1. Přejděte do části na **Správa organizace** > **Organizace** > **Právnické osoby**.
    2. Na záložce s náhledem **Zahraniční obchod a logistika** v sekci **Identifikace** zadejte do pole **DVR** ID smlouvy o výměně. Toto ID text bude součástí sestavy.
    3. V poli **Export čísla osvobozeného od DPH** zadejte DIČ vaší společnosti pro export.
    4. V poli **Import čísla osvobozeného od DPH** zadejte DIČ vaší společnosti pro import.
    5. V poli **Kód Intrastat** zadejte kód Intrastat, který je přiřazen právnické osobě.
    6. Na pevné záložce **Daňová registrace** v poli **Daňové registrační číslo** zadejte daňové identifikační číslo (DIČ) vaší společnosti.

    > [!NOTE]
    > Pokud generujete sestavu Intrastat pro pobočky, do pole **Daňové registrační číslo** zadejte daňové registrační číslo vaší mateřské společnosti.

2. V [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index) v knihovně sdíleného majetku si stáhněte nejnovější verze následujících konfigurací elektronického výkaznictví (ER) pro přiznání Intrasat.

    - Modul Intrastat
    - Sestava Intrastat
    - INSTAT XML
    - INSTAT XML (DE)

3. Nastavení parametrů zahraničního obchodu:

    1. V Dynamics 365 Finance přejděte na **Daň** > **Nastavení** > **Parametry zahraničního obchodu**.
    2. Na kartě **Intrastat** na pevné záložce **Elektronické hlášení** v poli **Mapování formátu souboru** vyberte **Intrastat XML (DE)**.
    3. V poli **Mapování formátu sestavy** vyberte **Sestava Intrastat**.
    4. Na pevné záložce **Hierarchie komoditních kódů** v poli **Hierarchie kategorií** vyberte **Intrastat**.
    5. V poli **Kód transakce** vyberte kód transakce pro převody majetku. Tento kód použijete pro transakce, které provádí skutečné nebo plánované převody majetku v souvislosti s kompenzací (finanční nebo jinou). Použijete jej také pro opravy.
    6. V poli **Dobropis** vyberte kód transakce pro vrácení zboží.
    7. V poli **Pracovník** vyberte kontaktní osobu pro sestavu Intrastat. Případně na kartě **Kontakt** zadejte nebo vyberte hodnoty v polích **Jméno**, **Telefon**, **Fax**, **E-mail** a **Internetová adresa**. Tato pole jsou součástí sestavy.
    8. V poli **Úřad** vyberte autoritu Intrastat.
    9. Jděte na **Daň** > **Nepřímé daně** > **DPH** > **Finanční úřady** a zadejte následující informace pro úřad Intrastat, kterou jste vybrali v předchozím kroku:

       - Identifikace úřadu
       - Adresa
       - Kontaktní informace

    10. Na kartě **Vlastnosti země/oblasti** v poli **Země/oblast** jsou uvedeny všechny země nebo oblasti, se kterými vaše společnost obchoduje. Pro každou zemi nebo oblast v poli **Typ země/oblasti** vyberte **EU**, aby se země nebo oblast objevila ve vaší sestavě Intrastat.

4. Nastavení kódů oblastí.

    1. Přejděte do nabídky **Správa organizace** > **Globální adresář** > **Globální adresář** > **Nastavení adresy**.
    2. Na kartě **Stát/provincie** v poli **Země/oblast** vyberte **DEU** a poté vyberte **Použít filtr**.
    3. V mřížce vyberte stát. Poté do pole **Kód Intrastat** zadejte jedinečný kód Intrastat.

5. Nastavte adresu původu produktu.

    1. Přejděte na **Řízení informací o produktech** > **Produkty** > **Uvolněné produkty**.
    2. V mřížce vyberte produkt.
    3. Na záložce s náhledem **Zahraniční obchod** v sekci **Intrastat** v poli **Země původu** vyberte **DEU**.

6. Přejděte na **Daň** > **Nastavení** > **Zahraniční obchod** > **Komprese Intrastatu** a vyberte pole, která mají být porovnána po shrnutí informací Intrastat. Pro německý Intrastat vyberte následující pole:

    - Zboží
    - Země nebo oblast
    - Oprava
    - Směr
    - Dodací podmínky
    - Faktura
    - Země/oblast původu
    - Přístav
    - Země/oblast odesílatele
    - Stav odesílatele
    - Statistická procedura
    - Kód transakce
    - Přeprava
    - DIČ

### <a name="intrastat-transfer"></a>Přenos Intrastat

Na stránce **Intrastat** v podokně akcí vyberte **Přenos** k automatickému přenosu informací o obchodu uvnitř Společenství z vašich prodejních objednávek, faktury s volným textem, nákupní objednávky, faktury dodavatele, účtenky produktů dodavatele **,** faktury projektu a objednávky přenosu. Budou přeneseny pouze dokumenty, které mají jako zemi nebo region určení (pro odeslání) nebo zásilku (pro přijetí) zemi EU.

Alternativně můžete ručně zadat transakce výběrem **Nový** v podokně akcí.

### <a name="generate-an-intrastat-report"></a>Vygenerovat sestavu Intrastat

1. Přejděte na **Daň** > **Deklarace** > **Zahraniční obchod** > **Intrastat**.
2. V podokně akcí vyberte **Výstup** > **Sestava**.
3. V dialogovém okně **Sestava Intrastat** nastavte následující pole.

    | Pole | popis |
    |-------------------------|-------------------------|
    | Od data | Vyberte počáteční datum sestavy. |
    | Do data | Vyberte koncové datum sestavy. |
    | Generovat soubor | Tuto možnost nastavte na **Ano**, chcete-li generovat soubor .xml. |
    | Název souboru | Pole ponechejte prázdné. Název souboru je generován automaticky a skládá se ze značky XML **&lt;envelopeId&gt;** a přípony souboru **.xml**.</br>Hodnota **&lt;envelopeId&gt;** je zřetězením následujících prvků v tomto pořadí:</br><ol type="1"></br><li>Hodnota značky **&lt;interchangeAgreementId&gt;**</li></br><li>Spojovník (-)</li></br><li>Hodnota značky **&lt;referencePeriod ve formátu RRRRMM&gt;**</li></br><li>Spojovník (-)</li></br><li>Hodnota značky **&lt;Envelope/DateTime/date ve formátu RRRRMMDD&gt;**</li></br><li>Spojovník (-)</li></br><li>Hodnota značky **&lt;Envelope/DateTime/time ve formátu hhmm&gt;**</li></br></ol> |
    | Směr | <ul></br><li>Vyberte **Příchozí zásilky** pro vykázání příchozích zásilek do společenství.</li></br><li>Vyberte **Odchozí zásilky** pro vykázání odchozích zásilek v rámci komunity.</li></br><li>Vyberte **Obě** pro vykázání jak příchozích, tak odchozích zásilek.</li></br></ul> |
    | Daňové registrační číslo | Pokud se číslo liší od daňového registračního čísla právnické osoby, zadejte registrační číslo, které má být použito ke generování identifikačního kódu odesílatele. |


## <a name="example"></a>Příklad

Tento příklad ukazuje, jak zaúčtovat příchozí a odchozí zásilky pro Intrastat. Použije právnickou osobu **DEMF**.

1. V [LCS](https://lcs.dynamics.com/Logon/Index) v knihovně sdíleného majetku si stáhněte nejnovější verze následujících konfigurací elektronického výkaznictví pro formát přiznání Intrasat:

    - Modul Intrastat
    - Sestava Intrastat
    - Intrastat XML
    - Intrastat XML (DE)

2. Vytvoření kódů transakce.

    1. Přejděte na **Daň** > **Nastavení** > **Zahraniční obchod** > **Kódy transakcí**.
    2. V podokně akcí zvolte **Nový**.
    3. Do pole **Kód** **transakce** zadejte **21**.
    4. Do pole **Název** zadejte **Vrácení zboží**.
    5. V podokně akcí vyberte **Uložit**.

3. Nastavte identifikační číslo úřadu.

    1. Jděte na **Daň** > **Nepřímé daně** > **DPH** > **Finanční úřady**.
    2. V seznamu vyberte **Finanční úřad**.
    3. V poli **Identifikace úřadu** zadejte **123**.

4. Nastavení kódů oblastí.

    1. Přejděte do nabídky **Správa organizace** > **Globální adresář** > **Globální adresář** > **Nastavení adresy**.
    2. Na kartě **Stát/provincie** v poli **Země/oblast** vyberte **DEU** a poté vyberte **Použít filtr**.
    3. V mřížce vyberte **BÝT** a poté do pole **Kód Intrastat** zadejte **11**.
    4. V podokně akcí vyberte **Uložit**.

5. Nastavte parametry zahraničního obchodu.

    1. Přejděte na **Daň** > **Nastavení** > **Zahraniční obchod** > **Parametry zahraničního obchodu**.
    2. Na kartě **Intrastat** na záložce s náhledem **Obecné** v poli **Kód** **transakce** vyberte **11**.
    3. V poli **Dobropis** vyberte **21**.
    4. V poli **Úřad** vyberte **Finanční úřad**.
    5. Na záložce s náhledem **Elektronické výkaznictví** v poli **Mapování formátu souboru** vyberte **INSTAT XML (DE)**.
    6. V poli **Mapování formátu sestavy** vyberte **Sestava Intrastat**.
    7. Na záložce s náhledem **Hierarchie komoditních kódů** v poli **Hierarchie kategorií** zkontrolujte, zda je vybrána možnost **Intrastat**.
    8. Na kartě **Vlastností země/oblasti** vyberte **Nová**.
    9. V poli **Země/oblast strany** vyberte **FRA**.
    10. V poli **Typ země/oblasti** vyberte **EU**.

6. K produktu přiřaďte kód komodity a nastavte původ produktu. Pole **Kód komodity**, **Země/oblast původu** a **Stát původu** se pak automaticky nastaví na prodejní a nákupní objednávky, když vyberete produkt.

    1. Přejděte na **Řízení informací o produktech** > **Produkty** > **Uvolněné produkty**.
    2. V mřížce vyberte **D0001**.
    3. Na záložce s náhledem **Zahraniční obchod** v sekci **Intrastat** v poli **Komodita** vyberte **920 20 34**.
    4. V sekci **Původ** v poli **Země/oblast** vyberte **DEU**.
    5. Na záložce s náhledem **Správa zásob** v sekci **Měření hmotnosti** v poli **Čistá hmotnost** zadejte **12**.
    6. V podokně akcí vyberte **Uložit**.

7. Ke způsobu doručení přiřaďte dopravu. Přepravní kód se pak automaticky nastaví na objednávky, když zvolíte způsob doručení.

    1. Přejděte na **Zásobování a zdroje** > **Nastavení** > **Distribuce** > **Způsoby doručení**.
    2. V seznamu vyberte **10**.
    3. Na pevné záložce **Zahraniční obchod** v poli **Přeprava** vyberte **01**.

8. Vytvořte prodejní objednávku se zákazníkem z EU.

    1. Přejděte na **Pohledávky** > **Objednávky** > **Všechny prodejní objednávky**.
    2. V podokně akcí zvolte **Nový**.
    3. V dialogovém okně **Vytvořit prodejní objednávku** na záložce s náhledem **Zákazník** v sekci **Zákazník** vyberte v poli **Účet zákazníka** hodnotu **DE-012**.
    4. Na záložce s náhledem **Obecné** v sekci **Dimenze úložiště** v poli **Lokalita** vyberte **1**.
    5. V poli **Sklad** zvolte **11**.
    6. Vyberte **OK**.
    7. Na kartě **Záhlaví** na záložce s náhledem **Zahraniční obchod** v poli **Přístav** vyberte **53**.
    8. V poli **Statistická procedura** vyberte **31710**.
    9.  Na kartě **Řádky** na záložce s náhledem **Řádky** **prodejní objednávky** v poli **Číslo položky** vyberte **D0001**. Poté do pole **Množství** zadejte **10**.
    10. Na záložce s náhledem **Podrobnosti řádku** na kartě **Zahraniční obchod** zkontrolujte, zda jsou automaticky nastavena pole **Kód transakce**, **Přeprava**, **Komodita** a **Země/oblast původu**.
    11. V podokně akcí vyberte **Uložit**.
    12. V podokně akcí na kartě **Faktura** v sekci **Generovat** zvolte **Faktura**.
    13. V dialogovém okně **Účtování faktury** na pevné záložce **Parametry** v sekci **Parametr**, v poli **Množství** vyberte **Všechny**.
    14. Výběrem tlačítka **OK** zaúčtujte fakturu.

9.  Přeneste transakci do deníku Intrastat a zkontrolujte výsledek.

    1. Přejděte na **Daň** > **Deklarace** > **Zahraniční obchod** > **Intrastat**.
    2. V podokně akcí zvolte **Převod**.
    3. V dialogovém okně **Intrastat (přenos)** v sekci **Parametry** nastavte možnost **Zákaznická faktura** na **Ano**.
    4. Vyberte **Filtr**.
    5. V dialogovém okně **Filtr Intrastat** na kartě **Rozsah** vyberte první řádek a ujistěte se, že pole **Pole** je nastaveno na **Datum**.
    6. V poli **Kritéria** vyberte aktuální datum.
    7. Zvolte **OK** a zavřete dialogové okno **Filtr Intrastat**.
    8. Vyberte **OK** pro zavření dialogového okna **Intrastat (převod)** a zkontrolujte výsledek. Řádek představuje prodejní objednávku, kterou jste vytvořili dříve.

        ![Řádek, který představuje prodejní objednávku na stránce Intrastat](media/intrastat_deu_1.png)

10. Vyberte řádek transakce a poté vyberte kartu **Obecné**, čímž zobrazíte další podrobnosti.

    ![Podrobnosti o prodejní objednávce na kartě Obecné na stránce Intrastat](media/intrastat_deu_2.png)

11. Vytvoření dobropisu pomocí prodejní objednávky.

    1. Přejděte na **Pohledávky** > **Objednávky** > **Všechny prodejní objednávky**.
    2. V podokně akcí zvolte **Nový**.
    3. V dialogovém okně **Vytvořit prodejní objednávku** na záložce s náhledem **Zákazník** v sekci **Zákazník** vyberte v poli **Účet zákazníka** hodnotu **DE-012**.
    4. Na záložce s náhledem **Obecné** v sekci **Dimenze úložiště** v poli **Lokalita** vyberte **1**.
    5. V poli **Sklad** zvolte **11**.
    6. Na kartě **Záhlaví** na záložce s náhledem **Zahraniční obchod** v poli **Přístav** vyberte **53**.
    7. V poli **Statistická procedura** vyberte **31710**.
    8. Na kartě **Řádky** na záložce s náhledem **Řádky** **prodejní objednávky** v poli **Číslo položky** vyberte **D0001**. Poté do pole **Množství** zadejte **-2**.
    9. Na záložce s náhledem **Podrobnosti řádku** na kartě **Zahraniční obchod** v poli **Kód transakce** vyberte **21**.
    10. Ujistěte se, že pole **Přeprava**, **Komodita** a **Země/oblast původu** jsou automaticky nastavena.
    11. V podokně akcí vyberte **Uložit**.
    12. V podokně akcí na kartě **Faktura** v sekci **Generovat** zvolte **Faktura**.
    13. V dialogovém okně **Účtování faktury** na pevné záložce **Parametry** v sekci **Parametr**, v poli **Množství** vyberte **Všechny**.
    14. Výběrem tlačítka **OK** zaúčtujte fakturu.

12. Přeneste transakci do deníku Intrastat a zkontrolujte výsledek.

    1. Přejděte na **Daň** > **Deklarace** > **Zahraniční obchod** > **Intrastat**.
    2. V podokně akcí zvolte **Převod**.
    3. V dialogovém okně **Intrastat (přenos)** v sekci **Parametry** nastavte možnost **Zákaznická faktura** na **Ano**.
    4. Vyberte **OK** pro zavření dialogového okna **Intrastat (převod)** a zkontrolujte výsledek. Byl přidán nový řádek, kde je pole **Směr** nastaveno na **Příchozí zásilky**.            
        Tento řádek představuje fyzické vrácení zboží.

        ![Řádek pro fyzické vrácení zboží na stránce Intrastat](media/intrastat_deu_3.png)

13. Vyberte řádek transakce a poté vyberte kartu **Obecné**, čímž zobrazíte další podrobnosti.

    ![Podrobnosti o fyzickém vrácení zboží na kartě Obecné na stránce Intrastat](media/intrastat_deu_4.png)

14. Vytvoření opravy pomocí prodejní objednávky:

    1. Přejděte na **Pohledávky** > **Objednávky** > **Všechny prodejní objednávky**.
    2. V podokně akcí zvolte **Nový**.
    3. V dialogovém okně **Vytvořit prodejní objednávku** na záložce s náhledem **Zákazník** v sekci **Zákazník** vyberte v poli **Účet zákazníka** hodnotu **DE-012**.
    4. Na záložce s náhledem **Obecné** v sekci **Dimenze úložiště** v poli **Lokalita** vyberte **1**.
    5. V poli **Sklad** zvolte **11**.
    6. Na kartě **Záhlaví** na záložce s náhledem **Zahraniční obchod** v poli **Přístav** vyberte **53**.
    7. V poli **Statistická procedura** vyberte **31710**.
    8. Na kartě **Řádky** na záložce s náhledem **Řádky** **prodejní objednávky** v poli **Číslo položky** vyberte **D0001**. Poté do pole **Množství** zadejte **-3**.
    9. Na záložce s náhledem **Podrobnosti řádku** na kartě **Zahraniční obchod** v poli **Kód transakce** vyberte **11**.
    10. Ujistěte se, že pole **Přeprava**, **Komodita** a **Země/oblast původu** jsou automaticky nastavena.
    11. V podokně akcí vyberte **Uložit**.
    12. Ujistěte se, že v poli **Kód transakce** je nastavena hodnota 11.
    13. V podokně akcí na kartě **Faktura** v sekci **Generovat** zvolte **Faktura**.
    14. V dialogovém okně **Účtování faktury** na pevné záložce **Parametry** v sekci **Parametr**, v poli **Množství** vyberte **Všechny**.
    15. Výběrem tlačítka **OK** zaúčtujte fakturu.

15. Přeneste transakci do deníku Intrastat a zkontrolujte výsledek:

    1. Přejděte na **Daň** > **Deklarace** > **Zahraniční obchod** > **Intrastat**.
    2. V podokně akcí zvolte **Převod**.
    3. V dialogovém okně **Intrastat (přenos)** v sekci **Parametry** nastavte možnost **Zákaznická faktura** na **Ano**.
    4. Vyberte **OK** pro zavření dialogového okna **Intrastat (převod)** a zkontrolujte výsledek. Byl přidán nový řádek, kde se ve sloupci **Oprava** zobrazuje zaškrtávací políčko.

        ![Řádek pro opravu na stránce Intrastat](media/intrastat_deu_5.png)

16. Vyberte řádek transakce a poté vyberte kartu **Obecné**, čímž zobrazíte další podrobnosti.

    ![Podrobnosti opravy na kartě Obecné na stránce Intrastat](media/intrastat_deu_6.png)

17. V podokně akcí vyberte **Výstup** > **Sestava**.
18. V dialogovém okně **Sestava Intrastat** na pevné záložce **Parametry** v sekci **Datum** vyberte měsíc prodejní objednávky, kterou jste vytvořili.
19. V sekci **Možnosti** **exportu** nastavte možnost **Generovat soubor** na **Ano**.
20. Do pole **Název souboru** zadejte požadovaný název.
21. Vyberte **OK** a zkontrolujte vygenerovanou sestavu. Následující tabulka zobrazuje hodnoty v ukázkové sestavě.

    | **Jméno**                  | **Prodejní faktura**  |   **Oprava**   | **Dobropis** |
    |---------------------------|--------------------|--------------------|-----------------|
    | declarationId             | 2021-07-D          | 2021-07-A          |                 |
    | referencePeriod           | 2021-07            | 2021-07            |                 |
    | PSIId                     | 11203/118/12345000 | 11203/118/12345000 |                 |
    | functionCode              | O                  | O                  |                 |
    | flowCode                  | D                  | A                  |                 |
    | CurrencyCode              | EUR                | EUR                |                 |
    | itemNumber                | 0000362            | 0000362            | 0000361         |
    | CN8Code                   | 9202034            | 9202034            | 9202034         |
    | goodsDescription          | Speaker            | Speaker            | Speaker         |
    | MSConsDestCode            | FR                 | FR                 | FR              |
    | countryOfOriginCode       | \-                 | \-                 | DE              |
    | netMass                   | 120                | -36                | 24              |
    | invoicedAmount            | 3290               | -987               | \-              |
    | StatisticalValue          | 3290               | -987               | 658             |
    | natureOfTransactionACode  | 1                  | 1                  | 2               |
    | natureOfTransactionBCode  | 1                  | 1                  | 1               |
    | modeOfTransportCode       | 01                 | 01                 | 01              |
    | regionCode                | 11                 | 11                 | 11              |
    | portAirportInlandportCode | 53                 | 53                 | 53              |

