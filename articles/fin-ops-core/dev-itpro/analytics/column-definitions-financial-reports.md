---
title: Definice sloupce ve finančních sestavách
description: Tento článek obsahuje informace o definicích sloupce. Definice sloupce je součástí sestavy nebo stavebního bloku, který definuje obsah jednotlivých sloupců v sestavě. Stejně jako definice řádků lze základní definice sloupců použít u více sestav.
author: ShylaThompson
manager: AnnBe
ms.date: 10/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: kfend
ms.custom: 106601
ms.assetid: 66e72a48-edab-4e9d-815f-596a1623c258
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 611e5cdfd2289bb2c690a72659e9ba47d6309cfe
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687223"
---
# <a name="column-definitions-in-financial-reports"></a>Definice sloupce ve finančních sestavách

[!include [banner](../includes/banner.md)]

Tento článek obsahuje informace o definicích sloupce. Definice sloupce je součástí sestavy nebo stavebního bloku, který definuje obsah jednotlivých sloupců v sestavě. Stejně jako definice řádků lze základní definice sloupců použít u více sestav.

## <a name="create-and-modify-a-column-definition"></a>Vytvoření a úprava definice sloupce

Definice sloupce může obsahovat 2 až 255 sloupců.

### <a name="create-a-column-definition"></a>Vytvoření definice sloupce

1. V Návrháři sestav v navigačním podokně klikněte na tlačítko **Definice sloupce**.
2. V nabídce **Soubor** klikněte na tlačítko **Nový** a vyberte možnost **Definice sloupce**.
3. Přidejte obsah do definice sloupce.

### <a name="open-a-column-definition"></a>Otevření definice sloupce

1. V Návrháři sestav v navigačním podokně klikněte na tlačítko **Definice sloupce**.
2. Dvojitým kliknutím na definici sloupce tuto definici otevřete.

### <a name="add-a-column-to-a-column-definition"></a>Přidání sloupce do definice sloupce

1. V Návrháři sestav klikněte na tlačítko **Definice sloupce** a potom otevřete definici sloupce ke změně.
2. Vyberte sloupce, kam má být vložen nový sloupec.
3. V nabídce **Upravit** klikněte na tlačítko **Vložit sloupec**. Nový sloupec se zobrazí nalevo od sloupce, který jste vybrali.

### <a name="delete-a-column-from-a-column-definition"></a>Odstranění sloupce z definice sloupců

1. V Návrháři sestav klikněte na položku **Definice sloupců** a otevřete definici sloupců, kterou chcete změnit.
2. Vyberte sloupec, který chcete odstranit.
3. V nabídce **Úpravy** klikněte na příkaz **Odstranit sloupec**.

## <a name="contents-of-a-column-definition"></a>Obsah definice sloupce
Definice sloupce zahrnuje následující informace:

- Sloupec popisů pro definici řádku.
- Sloupce částky, které zobrazují data z finančních dat, nebo výpočtů založených na jiných datech v definici sloupce
- Sloupce formátování
- Sloupce atributů

Tyto informace se zobrazí v následujících částech definice sloupce:

- Oblast záhlaví definice sloupce obsahuje text a formátování nadpisu, které se zobrazí v sestavě. Záhlaví se může vztahovat na jeden sloupec dat, může být rozšířeno na více sloupců nebo být pro sloupce použito za určitých podmínek. Definice sloupce může obsahovat tolik řádků záhlaví sloupců, kolik budete potřebovat.

    > [!NOTE]
    > Záhlaví sloupců jsou použita pro všechny sloupce dat v sestavě. Záhlaví sestavy platí pro celou sestavu. Lze definovat záhlaví sestavy na kartě **Záhlaví a zápatí** v rámci definice sestavy.

- Řádky podrobností sloupců jsou řádky pod řádků záhlaví v definici sloupce. Řádky podrobností sloupců definují informace, které jsou zahrnuty do sestavy. Následující tabulka obsahuje seznam řádků podrobností sloupců a jejich popis.

    | Název řádku podrobností sloupce                                                | Popis                                                                                            |
    |-----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
    | Typ sloupce                                                           | (Požadováno) Určete typ dat ve sloupci.                                                     |
    | Kód knihy / Kategorie atributů                                          | Zadejte informace o finančních datech pro sloupce typů **FD** a **ATTR**.                       |
    | Pokrytá období pro období fiskálního roku                                    | Zadejte informace o finančních datech pro sloupce typu **FD**.                                     |
    | Vzorec                                                               | Zadejte vzorec pro výpočet sloupců typu **CALC**.                                        |
    | Extra mezery šířky sloupce před ovládacím prvkem potlačení tisku formátu sloupce | Určuje speciální možnosti formátování.                                                                        |
    | Omezení sloupců                                                   | Omezit data.                                                                                         |
    | Organizační jednotka                                                        | Omezí sloupec tak, aby se zobrazovala pouze data pro zadanou organizační jednotku.                      |
    | Filtr měny zobrazení měny                                      | Umožňuje naformátovat měnu.                                                                                       |
    | Filtr dimenze                                                      | Určete filtr pro omezení dat na určité organizační jednotky finančních dat.                           |
    | Filtr atributů                                                      | Určete filtr k omezení finančních dat.                                                       |
    | Počáteční datum Koncové datum                                                   | Umožňuje omezit finanční data na konkrétní kalendářní data.                                                         |
    | Zarovnání                                                         | Zarovnání vlevo, na střed nebo vpravo zarovná text popisu, který je zadán v definici řádku. |

## <a name="column-restrictions-in-a-column-definition"></a>Omezení sloupce v definici sloupců
Pomocí omezení sloupců můžete určit, jak používá definice sloupce data nebo jak počítá informace. Můžete také omezit sloupec sestavy na konkrétní jednotku nebo konkrétní kalendářní data.

> [!NOTE]
> Kód **Omezení sloupce** přepisuje jakékoli konfliktní nastavení, které je přiřazeno v definici řádků.

### <a name="column-restrictions-cell"></a>Buňka Omezení sloupce

Buňka **Omezení sloupce** může zahrnovat kódy, které omezují nebo potlačují informace, jako jsou například formátování řádků, podrobnosti a částky pro daný sloupec.

#### <a name="add-a-column-restriction-in-a-column-definition"></a>Přidání omezení sloupce do definice sloupce

1. V Návrháři sestav otevřete definici sloupce k úpravě.
2. Klikněte dvakrát na buňku **Omezení sloupce** pro sloupec k omezení.
3. V dialogovém okně **Omezení sloupce** vyberte v seznamu jeden nebo více kódů a klikněte na tlačítko **OK**.

### <a name="column-restriction-codes"></a>Kódy omezení sloupce

Následující tabulka popisuje kódy omezení sloupce.

| Kód omezení sloupce | Popis |
|-------------------------|-------------|
| SU                      | Potlačí podtržení sloupce, kde je zadán příkaz podtržení (**---**) nebo příkaz dvojitého podtržení (**===**) v definici řádku. Nemusí být vhodné například podtrhovat částky, které jsou vytvářeny podle výpočtu procentuální hodnoty. |
| ST                      | Potlačí součty, aby se zobrazily v tomto sloupci pouze podrobnosti (například statistický sloupec). |
| SD                      | Potlačí podrobnosti, takže se ve sloupci zobrazí pouze řádky **TOT** a **CAL** (z definice řádku). |
| DR                      | Omezí částky ve sloupci **FD** na částky Má dáti. |
| CR                      | Omezí částky ve sloupci **FD** na částky Dal. |
| ADJ                     | Omezí částky v tomto sloupci na částky oprav za období, pokud jsou tyto částky k dispozici. |
| XAD                     | Omezí částky v tomto sloupci tak, aby byly vyloučeny částky oprav za období. |
| PT                      | Omezí částky ve sloupci tak, aby pouze zaúčtované transakce byly zahrnuty, pokud tyto transakce jsou k dispozici. |
| UPT                     | Omezí částky ve sloupci tak, aby byly zahrnuty pouze nezaúčtované transakce, pokud jsou tyto transakce k dispozici.<p><strong>Poznámka:</strong> Ne všichni poskytovatelé dat podporují nezaúčtované transakce. </p> |

### <a name="restrict-a-column-to-a-reporting-unit"></a>Omezení sloupce na organizační jednotku

1. V Návrháři sestav otevřete definici sloupce k úpravě.
2. Klikněte dvakrát na buňku **Jednotka výkaznictví** pro sloupec k omezení.
3. V dialogovém okně **Výběr jednotky výkaznictví** v seznamu **Strom výkaznictví** vyberte strom.
4. Rozbalte nebo sbalte seznam jednotek vyberte jednotku výkaznictví a klikněte na tlačítko **OK**.

## <a name="format-column-headers"></a>Formátování záhlaví sloupců
Záhlaví, která se objevují v horní části sloupců v sestavě, můžete přidávat, upravovat a odstraňovat. Také můžete nakonfigurovat podmíněné pokrývání záhlaví sloupců na základě pole **Období** z definice sloupce a pole **Základní období** z definic sestavy. Základní období vám pomůže ušetřit čas při vytváření sestav s klouzavými prognózami.

### <a name="create-and-manage-column-headers"></a>Vytvoření a správa záhlaví sloupců

Můžete přidat, upravit a odstranit záhlaví, která se zobrazí v horní části sloupců v sestavě, pomocí dialogového okna **Záhlaví sloupce**. Pole dialogového okna **Záhlaví sloupce** jsou popsána v následující tabulce.

| Pole                 | Popis |
|-----------------------|-------------|
| Text záhlaví sloupce    | Tento text se zobrazí v záhlaví sloupce. Můžete zadat text přímo do tohoto pole nebo kliknout na tlačítko **Vložit automatický text** a vybrat možnost, která aktualizuje záhlaví sloupce pokaždé, když je vygenerována sestava. Chcete-li zahrnout více kódů automatického textu, klikněte na tlačítko **Vložit automatický text** znovu a potom klikněte na další kód v seznamu. |
| Možnosti formátu        | Použít formátování pro záhlaví sloupce, například rámeček nebo podtržení. |
| Rozšířit z Rozšířit do | Definuje sloupce, na které se text záhlaví vztahuje. |
| Zarovnání         | Určete jak má být text záhlaví sloupce zarovnán pro sloupec nebo rozsah sloupců určený pomocí polí **Pokrýt od** a **Pokrýt k**. |

### <a name="create-a-column-header"></a>Vytvoření záhlaví sloupce

1. V Návrháři sestav otevřete definici sloupců, kterou chcete změnit.
2. Klikněte dvakrát na buňku záhlaví.
3. V dialogovém okně **Záhlaví sloupce** zadejte text záhlaví sloupce. Případně klikněte na tlačítko **Vložit automatický text** a vyberte možnost.
4. V poli **Možnosti formátu** vyberte formát pro záhlaví.
5. V poli **Pokrýt od** zadejte písmeno sloupce, nad kterým má začít záhlaví sloupců. V poli **Pokrýt k** zadejte písmeno sloupce, nad kterým má končit záhlaví sloupců.
6. V části **Zarovnání** vyberte, zda má být text záhlaví sloupců zarovnaný vlevo, zarovnaný na střed nebo zarovnaný vpravo.
7. Klepněte na tlačítko **OK**.

### <a name="add-a-column-header-row"></a>Přidání řádku záhlaví sloupců

1. V Návrháři sestav otevřete definici sloupců, kterou chcete změnit.
2. Vyberte buňku v řádku záhlaví.
3. V nabídce **Upravit** klikněte na tlačítko **Vložit řádek**. Nový řádek je vložen nad řádek, který jste vybrali v kroku 2.

> [!NOTE]
> Používáte-li v sestavě pro záhlaví sestavy čtyři nebo více řádků, záhlaví se budou při exportu sestavy do listu aplikace Excel překrývat. Chcete-li zobrazit všechna záhlaví v sestavě, zvětšete horní okraj v definici sestavy.

### <a name="delete-a-column-header-row"></a>Odstranění řádku záhlaví sloupců

1. V Návrháři sestav otevřete definici sloupců, kterou chcete změnit.
2. Vyberte buňku pro odstranění v řádku záhlaví.
3. V nabídce **Upravit** klikněte na tlačítko **Odstranit řádek**.

### <a name="create-an-automatically-generated-header"></a>Vytvoření automaticky generovaného záhlaví

Návrhář sestav může automaticky generovat záhlaví sloupců na základě kódů automatického textu. Kódy automatického textu jsou proměnné, které se aktualizují při každém generování sestavy. Tyto kódy mohou být zahrnuty do libovolného záhlaví sloupce a určovat informace, které se u sestavy liší, jako je například datum nebo číslo období. Jednu definici sloupců proto můžete použít pro více definic sestav, časových období a organizačních stromů. Protože kódy automatického textu závisí na informacích kalendáře z řádků podrobností definice sloupce, jsou podporovány pouze u sloupců **CALC** a **FD**. Způsob, jakým je kód automatického textu zobrazen v buňce záhlaví sloupce, má vliv na to, jak se tyto údaje zobrazují v sestavě. V dialogovém okně **Záhlaví sloupce** se kódy automatického textu zobrazí s malými i velkými znaky. V sestavě se proto text se zobrazí velkými i malými písmeny. Například u standardního kalendářního roku **\@CalMonthLong** převede měsíc **7** na **červenec**. Pokud má být v sestavě název měsíce uveden velkými písmeny (například **ČERVENEC**), zadejte kód automatického textu velkými písmeny do pole **Text záhlaví sloupce**. Například zadejte **\@CALMONTHLONG**. Kódy lze používat společně s textem. Například zadejte následující text záhlaví:**Period \@FiscalPeriod-\@FiscalYear from \@StartDate to \@EndDate**. Záhlaví sestavy, které bude vygenerováno, bude vypadat nápodobně: **Period 1-02 od 1.1.2002 do 31.1.2002**.

> [!NOTE]
> Formát částí textu, jako například dlouhé datum, závisí na vašich místních nastaveních serveru. Tato nastavení můžete změnit, kliknutím na tlačítko **Start**, na položku **Ovládací panely** a nakonec na položku **Oblast a jazyk**. V následující tabulce jsou uvedeny dostupné možnosti automatického textu u záhlaví sloupců.


| Možnost a kód automatického textu                | Popis |
|-----------------------------------------|-------------|
| Název měsíce (@CalMonthLong)              | Vytiskne v záhlaví sloupce název aktuálního měsíce. Pokud se rozhodnete zaokrouhlovat částky v sestavách na tisíce, milióny nebo miliardy, nebo pokud šířku sloupce v sestavě nastavíte na méně než 9 znaků, zkrátí se název měsíce na první tři znaky. |
| Zkrácený název měsíce (@CalMonthShort) | Vytiskne zkrácený název měsíce pro vybrané fiskální období. |
| Číslo období (@FiscalPeriod)           | Vytiskne číselnou formu fiskálního období, který je určený pro daný sloupec. Pokud sloupec překlenuje několik období, vytiskne se poslední období v tomto rozsahu. |
| Popis období (@FiscalPeriodName)  | Vytiskne popis fiskálního období, který je určen ve finančních datech. |
| Fiskální rok (@FiscalYear)               | Vytiskne fiskální rok tohoto sloupce v číselné formě. |
| Kalendářní rok (@CalYear)                | Vytiskne kalendářní rok tohoto sloupce v číselné formě. |
| Počáteční datum (@StartDate)                 | Vytiskne počáteční datum pro sloupec. |
| Koncové datum (@EndDate)                     | Vytiskne koncové datum pro sloupec. |
| Název jednotky ze stromu (@UnitName)         | Pokud sloupec omezíte na konkrétní jednotku organizačního stromu, vytiskne v záhlaví sloupce její název. |
| Popis jednotky (@UnitDesc)            | Pokud sloupec omezíte na konkrétní jednotku organizačního stromu, vytiskne v záhlaví sloupce její popis. |
| Kód knihy (@BookCode)                   | Vytiskne kód knihy zadaný ve sloupci. |
| Prázdný řádek (@Blank)                     | Vloží do záhlaví sloupce prázdný řádek. |

### <a name="create-a-conditional-spanning-header"></a>Vytvoření podmíněného překlenovacího záhlaví

Podmíněná překlenovací záhlaví mohou na základě zadaného data období zasahovat do více sloupců. Pokud máte například sestavu rozpočtu na fiskální rok a chcete zobrazit skutečné rozpočty za minulé měsíce s předpokládanými rozpočty na budoucí měsíce, můžete pomocí podmíněných překlenovacích záhlaví automaticky aktualizovat záhlaví sestavy. Při vytváření podmíněných překlenovacích záhlaví dávejte pozor na následující situace:

- Jakákoli podmínka zastavení (pole **Pokrýt k**) vyhovující před podmínkou začátku (pole **Pokrýt od**) bude ignorována. Pokud má například sloupec B podmínku rozšíření definovánu jako BASE+1 až BASE, hodnota BASE je ve sloupci C a BASE+1 ve sloupci D. V takovém případě podmínka konce ve sloupci C je ignorována a tisk záhlaví začíná sloupcem D.
- Zadáte-li záhlaví sloupců, která se překrývají, budou se překrývat při vytištění v sestavě. estava bude vygenerována, ale zobrazí se následující upozornění v poli **Stav fronty sestav**: „Záhlaví sloupců používající základ se překrývají s jinými záhlavími sloupců a mohou způsobit překrývání textu.“ Například definice záhlaví sloupce B je B až BASE+1 a definice záhlaví ve sloupci D je BASE+1 až F. V takovém případě se záhlaví tisknou na sebe a jsou nečitelná. Vždy při použití funkce BASE v definici **Pokrýt od / Pokrýt k** si prohlédněte vygenerovanou sestavu a zkontrolujte, zda se záhlaví nepřekrývají.
- Pokud v definici pokrytí zadáte hodnotu BASE ve sloupci Netisknout (**NP**), bude ignorována bez ohledu na to, co je definováno v definici sloupce. Tento scénář je v podstatě stejný, jako když nevytvoříte definici záhlaví sloupce.
- V případě sloupců s podmíněným tiskem (**P&lt;B**, **P&gt;=B**) se záhlaví s podmíněným pokrytím chová jako jakákoli běžná definice záhlaví sloupce. Pokud je například výsledkem podmínky hodnota Nepravda, bude tisk záhlaví začínat na každém dalším sloupci odpovídajícím podmínce rozšíření.

#### <a name="create-a-conditional-spanning-header"></a>Vytvoření podmíněného překlenovacího záhlaví

1. V Návrháři sestav otevřete definici sloupců, kterou chcete změnit.
2. Klikněte dvakrát na buňku záhlaví.
3. V dialogovém okně **Záhlaví sloupce** zadejte text záhlaví sloupce. Případně klikněte na tlačítko **Vložit automatický text** a vyberte možnost.
4. V poli **Možnosti formátu** vyberte styl formátování pro záhlaví.
5. Zadejte období vztahující se k základnímu období, které je zadáno při generování sestavy. V polích **Pokrýt od** a **Pokrýt k** zadejte některou z následujících hodnot: **BASE**, **BASE-X** nebo **BASE+X**, kde X je počet období od základního období. Zadáte-li například **BASE** do pole **Pokrýt od**, text záhlaví sloupce s podmíněným pokrytím začíná v záhlaví sloupce, kde se hodnota definice sestavy **Základní období** rovná hodnotě definice sloupce **Období**. Končí ve sloupci, který je určen v poli **Pokrýt k**. Proto pokud je pokrytí od BASE k M a hodnota definice sestavy **Základní období** je **4**, záhlaví začne ve sloupci, ve kterém je období nastaveno na hodnotu **4** a končí ve sloupci M. Záhlaví končí a začínají pouze v tisknutých sloupcích.
6. V části **Zarovnání** vyberte, zda má být text záhlaví sloupců zarovnaný vlevo, zarovnaný na střed nebo zarovnaný vpravo.
7. Klikněte na tlačítko **OK**.

#### <a name="example-of-a-conditional-spanning-header"></a>Příklad podmíněného překlenovacího záhlaví

Uživatel vytváří sestavu pro dynamickou šestiměsíční prognózu. Uživatel chce, aby se přes sloupce obsahující skutečná data vytisklo slovo „Skutečnost“ a přes sloupce obsahující prognózy rozpočtu slovo „Rozpočet“. Každý měsíc, kdy je spuštěna sestava, přibude jeden sloupec se skutečnými hodnotami a ubude jeden sloupec rozpočtu. Přestože uživatel může při každém generování sestavy upravit záhlaví ruční změnou definice sloupce, rozhodne se ušetřit si čas a práci a vytvoří podmíněná překlenovací záhlaví, která automaticky vytvoří záhlaví u příslušných sloupců při každém spuštění sestavy. Uživatel otevře Návrhář sestav, klikne na tlačítko **Definice sloupce** v navigačním podokně a otevře definici sloupce pro sestavu. Uživatel potom zadá následující informace. Základní období v definici sestavy je 4.

|      Formát         |  A   | mld.             | K             | D             | E             | F             | G             | H             | I             | J             | tis.             | L             | mil.             |
|---------------------|------|---------------|---------------|---------------|---------------|---------------|---------------|---------------|---------------|---------------|---------------|---------------|---------------|
| Záhlaví 1            |      | Skutečná        | Rozpočet        |               |               |               |               |               |               |               |               |               |               |
| Záhlaví 2            |      | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong |
| Záhlaví 3            |      |               |               |               |               |               |               |               |               |               |               |               |               |
| Typ sloupce         | POPIS | FD            | FD            | FD            | FD            | FD            | FD            | FD            | FD            | FD            | FD            | FD            | FD            |
| Kód knihy/atribut |      | SKUTEČNÝ        | ROZPOČET2012    | SKUTEČNÝ        | ROZPOČET2012    | SKUTEČNÝ        | ROZPOČET2012    | SKUTEČNÝ        | ROZPOČET2012    | SKUTEČNÝ        | ROZPOČET2012    | SKUTEČNÝ        | ROZPOČET2012    |
| Fiskální rok         |      | ZÁKLAD          | ZÁKLAD          | ZÁKLAD          | ZÁKLAD          | ZÁKLAD          | ZÁKLAD          | ZÁKLAD          | ZÁKLAD          | ZÁKLAD          | ZÁKLAD          | ZÁKLAD          | ZÁKLAD          |
| Období              |      | 1             | 1             | 2             | 2             | 3             | 3             | 4             | 4             | 5             | 5             | 6             | 6             |
| Pokrytá období     |      | PERIODICKÝ      | PERIODICKÝ      | PERIODICKÝ      | PERIODICKÝ      | PERIODICKÝ      | PERIODICKÝ      | PERIODICKÝ      | PERIODICKÝ      | PERIODICKÝ      | PERIODICKÝ      | PERIODICKÝ      | PERIODICKÝ      |
| Šířka sloupce        | 30   | 10            | 10            | 10            | 10            | 10            | 10            | 10            | 10            | 10            | 10            | 10            | 10            |
| Řízení tisku       |      | P&lt;=B       | P&gt;B        | P&lt;=B       | P&gt;B        | P&lt;=B       | P&gt;B        | P&lt;=B       | P&gt;B        | P&lt;=B       | P&gt;B        | P&lt;=B       | P&gt;B        |

Uživatel kliknutím dvakrát na buňku záhlaví sloupce otevřete dialogové okno **Záhlaví sloupce** a zadá následující informace.

| Pole              | Hodnota                 |
|--------------------|-----------------------|
| Text záhlaví sloupce | Skutečné                |
| Vložit automatický text    | Nebyla vybrána žádná možnost. |
| Možnosti formátu     | Pole                   |
| Zarovnání      | Nebyla vybrána žádná možnost. |
| Rozšířit z        | mld.                     |
| Rozšířit do          | ZÁKLAD                  |
| Záhlaví rozpočtu      | BASE+1 až koncový sloupec  |

Po zadání informací uživatel klikne na **OK**. Poté uživatel kliknutím dvakrát na buňku záhlaví sloupce C otevře dialogové okno **Záhlaví sloupce** a zadá následující informace.

| Pole              | Hodnota                 |
|--------------------|-----------------------|
| Text záhlaví sloupce | Rozpočet                |
| Vložit automatický text    | Nebyla vybrána žádná možnost. |
| Možnosti formátu     | Pole                   |
| Zarovnání      | Nebyla vybrána žádná možnost. |
| Rozšířit z        | C                     |
| Rozšířit do          | ZÁKLAD+2                |

Nyní pokaždé, když tato zpráva je generována, přes sloupce obsahující skutečná data se vytiskne slovo „Skutečnost“ a přes sloupce obsahující prognózy rozpočtu slovo „Rozpočet“. Navíc počet sloupců se upraví každý měsíc.

## <a name="apply-column-justification"></a>Použití zarovnání sloupce
Buňka **Zarovnání** se používá k formátování zarovnání sloupce popisu v sestavě. Tato možnost má vliv jen na popisy sloupců, a ne na hodnoty samotné.

1. V Návrháři sestav otevřete definici sloupců, kterou chcete změnit.
2. Dvakrát klikněte na buňku **Zarovnání**.
3. Vyberte jednu z následujících hodnot na seznamu:

    - **Žádné** – nebude použito žádné zarovnání.
    - **Vlevo** – popisy sloupců se zarovnají doleva.
    - **Na střed** – popisy sloupců se zarovnají na střed.
    - **Vpravo** – popisy sloupců se zarovnají doprava.

## <a name="add-special-formatting-options"></a>Přidání speciálních možností formátování
Řádky podrobností ve sloupci formátování v definici sloupců umožňují uplatnit speciální formátování na vybrané sloupce. I když jsou některé možnosti **Řízení tisku** a možnosti **Omezení sloupce** specifické pro sloupce **FD**, většina možnosti platí pro všechny typy sloupců. Formátování zadané v definici řádku přepíše formátování, které je zadáno v definici sloupce a v definici sestavy. Formátování zadané v definici řádku však přepíše formátování, které je zadáno v definici sloupce. Následující řádky se považují za řádky formátování:

- Šířka sloupce
- Mezery navíc před sloupcem
- Přepsání formátu/měny
- Řízení tisku

### <a name="changing-the-column-width"></a>Změna šířky sloupce

Buňka **Šířka sloupce** určí počet znaků, které mají být použity pro šířku tohoto sloupce v tištěné sestavě. Šířka sloupců je důležitá pro sloupce, které obsahují částky (sloupce typu **CALC**, **WKS** nebo **FD**), popisy (sloupce typu **DESC**) nebo vyplnění (sloupce typu **FILL**). Ve výchozím nastavení je zvolena možnost **Automaticky přizpůsobit**, takže každý sloupec je automaticky upraven podle obsahu.

#### <a name="specify-the-width-of-a-column-on-a-report"></a>Zadání šířky sloupce v sestavě

1. V Návrháři sestav otevřete definici sloupců, kterou chcete změnit.
2. V buňce **Šířka sloupce** zadejte počet míst pro šířku sloupce. Maximální šířka jakéhokoli sloupce je 255 znaků (toto číslo zahrnuje procenta, čárky i závorky). Chcete-li návrháři sestav umožnit výběr vhodné šířky pro sloupec na základě obsahu buněk, můžete dvakrát kliknout na buňku **Šířka sloupce** a poté kliknout na možnost **Automaticky přizpůsobit**.

### <a name="add-space-between-columns"></a>Přidání mezery mezi sloupci

Buňka **Další mezery před sloupcem** určuje šířku oddělovače mezi jedním sloupcem a přiléhajícími sloupci v definici sloupců. Nastavení **Další mezery před sloupcem** ovlivní všechny řádky podrobností sloupce pro daný sloupec, ale nikoli řádky záhlaví sloupce. Pomocí této možnosti můžete oddělit skupiny sloupců nebo přidat několik mezer před popis tak, aby byl sloupec s popisy odsazen od názvů v sestavě, které jsou zarovnány doleva. Ve výchozím nastavení jsou mezi jednotlivými sloupci dvě mezery. Toto nastavení lze změnit na kartě **Nastavení** v definici sestavy.

#### <a name="specify-the-space-between-columns"></a>Zadání mezery mezi sloupci

1. V Návrháři sestav otevřete definici sloupců, kterou chcete změnit.
2. V buňce **Další mezery před sloupcem** zadejte počet mezer k vložení mezi sloupce.

### <a name="specify-a-format-currency-override"></a>Určení přepsání formátu a měny

Buňka **Přepsání formátu/měny** určuje formátování desetinných míst, měny a procentuálních hodnot ve sloupci. Toto formátování má přednost před veškerým formátováním, které je určeno v definici sestavy nebo systémovými výchozími hodnotami.

#### <a name="assign-a-format-currency-override-to-a-report-column"></a>Přiřazení přepsání formátu a měny ke sloupci sestavy

1. V Návrháři sestav otevřete definici sloupců, kterou chcete změnit.
2. Dvakrát klikněte na buňku **Přepsání formátu/měny** ve sloupci s částkou.
3. V dialogovém okně **Přepsání formátu** vyberte možnosti formátování.

### <a name="add-a-print-control-code"></a>Přidání kódů řízení tisku

Buňka **Řízení tisku** může obsahovat kódy, které upraví zobrazení nebo charakteristiky tisku sloupce. Existují dva typy tiskových řídicích kódů: standardní kódy řízení tisku a podmíněné kódy řízení tisku.

#### <a name="regular-print-control-codes"></a>Standardní kódy řízení tisku

| Kód řízení tisku | Význam                                     | Popis |
|--------------------|-------------------------------------------------|-------------|
| NP                 | Netisknout                                     | Částky v tomto sloupci se nebudou tisknout ani používat ve výpočtech. Chcete-li sloupec, který se netiskne, použít ve výpočtu, použijte ve výpočetním vzorci přímý odkaz na sloupec. Například netisknutý sloupec C je součástí následujícího výpočtu: **B+C+D**. Netisknutý sloupec C však není součástí následujícího výpočtu: **B:D**. |
| XCR                | Změna znaménka, pokud obvyklý zůstatek řádku je typu Dal | Vytvoří rozpočet nebo porovnávací sestavu, ve které je nepříznivá odchylka (například deficit výnosů nebo překročení výdajů) vždy záporná. Použitím tohoto kódu na sloupec **CALC** obrátíte znaménko částky sloupce, pokud je typický zůstatek daného řádku typu Dal (dle určení hodnoty **C** ve sloupci **Normální zůstatek** v definici řádku).<p><strong>Poznámka:</strong> Pro řádky <strong>TOT</strong> a řádky </strong>CAL</strong>, které obvykle nesou zůstatek typu Dal, je třeba zadat hodnotu <strong>C</strong> do sloupce <strong>Normální zůstatek</strong> v definici řádku.</p> |
| X0                 | Potlačit sloupec v případě, že obsahuje pouze nuly nebo prázdné hodnoty          | Vyloučí sloupec **FD** ze sestavy, pokud jsou všechny buňky ve sloupci prázdné nebo obsahují nuly. |
| SR                 | Potlačit zaokrouhlování                               | Zabrání zaokrouhlení částek v tomto sloupci. |
| XR                 | Potlačit zahrnutí                                 | Potlačí zahrnutí. Pokud sestava používá organizační strom, nebudou částky v tomto sloupci zahrnuty do následných nadřazených uzlů. |
| RP                 | Opakovat sloupec na každé stránce                      | Opakuje zadaný sloupec na všech stránkách sestavy. Například můžete použít kontrolní kód **RP** k zahrnutí sloupce typu **ROW**, který shromáždí kódy řádků na každé stránce. |
| WT                 |  Zalamovat text                                      |  Pokud je text příliš dlouhý na místo ve sloupci, zalomí tato možnost text tak, aby se celý text vešel do sloupce. |

#### <a name="conditional-print-control-codes"></a>Podmíněné kódy řízení tisku

| Podmíněný kód řízení tisku | popis                                                                             |
|--------------------------------|-----------------------------------------------------------------------------------------|
| (žádný)                         | Zruší výběr podmíněného tisku.                                                  |
| P&lt;B                         | Zobrazí určený sloupec pouze v případě, že je hodnota období menší než základní období.             |
| P&gt;B                         | Zobrazí určený sloupec pouze v případě, že je hodnota období větší než základní období.             |
| P=B                            | Zobrazí určený sloupec pouze v případě, že se hodnota období rovná základnímu období.              |
| P&lt;=B                        | Zobrazí určený sloupec pouze v případě, že je hodnota období menší nebo rovna základnímu období. |
| P&gt;=B                        | Zobrazí určený sloupec pouze v případě, že je hodnota období větší nebo rovna základnímu období. |

#### <a name="add-print-control-codes-to-a-report-column"></a>Přidání kódů řízení tisku do sloupce sestavy

1. V Návrháři sestav otevřete definici sloupců, kterou chcete změnit.
2. Dvakrát klikněte na buňku **Řízení tisku**.
3. V dialogovém okně **Řízení tisku** vyberte kód ze seznamu **Výběr možností řízení tisku**. Chcete-li vybrat více než jeden kód, podržte klávesu Ctrl a vyberte kódy.
4. Vyberte možnost v poli **Podmíněné možnosti tisku**. Ve výchozím nastavení je vybrána položka **(žádné)**. Lze vybrat pouze jeden podmíněný kód tisku současně.
5. Klikněte na tlačítko **OK**.

> [!TIP]
> Můžete také zadat tiskové kódy přímo do buňky **Řízení tisku**. Jednotlivé kódy řízení tisku oddělte čárkou.

## <a name="column-types"></a>Typy sloupce
Typ informací, které zahrnuje každý sloupec v sestavě, je určen hodnotou v řádku **Typ sloupce** v definici sloupce. Každá definice sloupce musí obsahovat minimálně jeden sloupec popisu (**DESC**) a jeden sloupec částky (**FD**, **WKS** nebo **CALC**).

> [!NOTE]
> Kódy typu sloupce se nevztahují na všechny účetní systémy. Vyberete-li typ, který není pro daný účetním systémem platný, zobrazí se daný sloupec v sestavě jako prázdný.

### <a name="specify-a-column-type"></a>Zadání typu sloupce

1. V Návrháři sestav otevřete definici sloupců, kterou chcete změnit.
2. V odpovídajícím sloupci dvakrát klikněte na buňku v řádku **Typ sloupce**.
3. Vyberte typ sloupce ze seznamu. Následující tabulka popisuje různé typy sloupce.

    <table>
    <thead>
    <tr>
    <th>Kód typu sloupce</th>
    <th>Popis</th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td>FD</td>
    <td>Zobrazte finanční data při použití sloupce <strong>Odkaz na finanční dimenze</strong> v definici řádku. Vyberete-li typ sloupce <strong>FD</strong>, jsou v následujících řádcích automaticky přiřazena výchozí nastavení: <ul>
    <li><strong>Kód knihy / Kategorie atributů:</strong> ACTUAL</li>
    <li><strong>Kód knihy / Kategorie atributů:</strong> ACTUAL</li>
    <li><strong>Fiskální rok:</strong> BASE</li>
    <li><strong>Období:</strong> BASE</li>
    <li><strong>Pokrytá období:</strong> PERIODIC</li>
    <li><strong>Šířka sloupce:</strong> 14</li>
    </ul>
Tato výchozí nastavení můžete změnit.</td>
    </tr>
    <tr>
    <td>VÝPOČET</td>
    <td>Zobrazí výsledek jednoduchého nebo komplexního výpočtu, který je určen v buňce <strong>Vzorec</strong>. Další informace naleznete v tématu <a href="advanced-formatting-options-financial-reporting.md">Rozšířené možnosti formátování v návrháři sestav</a>.</td>
    </tr>
    <tr>
    <td>POPIS</td>
    <td>Zobrazí popis řádku z definice řádku. Tento sloupec sice často bývá prvním sloupcem v sestavě, může však být na jakékoli pozici.</td>
    </tr>
    <tr>
    <td>ŘÁDEK</td>
    <td>Zobrazí jednotlivé kódy řádků pro finanční řádky ze sloupce <strong>Kód řádku</strong> v definici řádku. Další informace naleznete v tématu <a href="row-definitions-financial-reporting.md">Definice řádku ve finančním výkaznictví</a>.</td>
    </tr>
    <tr>
    <td>ACCT (kódy účtů)</td>
    <td>Zobrazí hodnoty segmentů nebo dimenzí finančních dat, které platí pro jednotlivé řádky. Pro sestavy podrobností o účtu a transakcích je vytištěn plně kvalifikovaný účet (například <strong>110140-070-0101</strong>). Pokud byly ve sloupci <strong>Odkaz na finanční dimenze</strong> v přidružené definici řádku zadány rozsahy, je rozsah uzavřen do hranatých závorek a je při zpracování považován za jedinou hodnotu (například <strong>[110140:110700]-070-[0101:0200]</strong>). U finančních sestav a sestav na vysoké úrovni, které jsou kombinací několika účtů, je vytištěn odkaz na finanční data z definice řádku (například <strong>1100:1200</strong>).</td>
    </tr>
    <tr>
    <td>VYPLNIT</td>
    <td>Vyplní buňku znakem, který uzavřete do jednoduchých uvozovek. Pokud nezadáte žádný znak, bude prázdný sloupec prázdný. Chcete-li například vyplnit sloupec třemi tečkami (...), zadejte hodnotu <strong>FILL</strong> <strong>'.'</strong>.</td>
    </tr>
    <tr>
    <td>STRANA</td>
    <td>Vloží do sestav svislý konec stránky. Sloupce napravo od sloupce <strong>PAGE</strong> se zobrazí na jiné stránce.</td>
    </tr>
    <tr>
    <td>ATTR</td>
    <td>Pokud váš účetní systém podporuje atributy, zobrazí ve sloupci atribut účtu nebo transakce. Atribut, který se musí vztahovat na jeden úplný účet, vyextrahuje z finančních dat příslušné informace o účtu nebo transakci. Atributy na úrovni účtu zobrazí data z účtu a atributy na úrovni transakce zobrazí data z doby, kdy byla zaúčtována transakce. Pokud jako typ sloupce vyberete typ <strong>ATTR</strong>, pak v řádku podrobností <strong>Kód knihy / Kategorie atributů</strong> definice sloupce zadejte kategorii atributu.</td>
    </tr>
    </tbody>
    </table>

### <a name="financial-dimensions-column"></a>Sloupec Finanční dimenze

Následující definic řádků **Definice sloupce** platí pro sloupce, které mají typ sloupce **FD** (částky z finančních dimenzí).

#### <a name="book-codeattribute-category-cell"></a>Buňka Kód knihy / Kategorie atributů

Buňka **Kód knihy / atribut kategorie** identifikuje kód knihy pro data ve sloupci **FD**. Definice sloupce může obsahovat více skutečných, rozpočtových a statistických sloupců. Definice sloupců také dokáže zobrazit různá období (například aktuální nebo od začátku roku) a různé částky. Seznam kódů knih odráží skutečné, rozpočtové a statistické (nefinanční) možnosti, které byly stanoveny ve vašich finančních datech.

#### <a name="fiscal-year-cell"></a>Buňka Fiskální rok

Buňka **Fiskální rok** identifikuje fiskální rok, který má sloupec zahrnovat. Tento rok se může vztahovat k základnímu roku, který je zadáno při generování sestavy. K dispozici jsou tyto možnosti.

| Možnost  | Popis                                                                                                                  |
|---------|------------------------------------------------------------------------------------------------------------------------------|
| ZÁKLAD    | Použije základní rok, který je zadán v době vytvoření sestavy.                                                                          |
| BASE+\# | Použije rok, který následuje \# let po základním roku. Například pro použití třetího roku po základním roku zadejte hodnotu **BASE+3**. |
| BASE-\# | Použije rok, který uplynul \# let před základním rokem. Chcete-li například použít předchozí rok, zadejte hodnotu **BASE-1**.                 |
| \#      | Zadá aktuální fiskální rok.                                                                                                |

#### <a name="period-cell"></a>Buňka Období

Buňka **Období** identifikuje fiskální období, která má sloupec zahrnovat. Toto období se může vztahovat k základnímu období, které je zadáno při generování sestavy. Existují tyto možnosti.

| Parametr          | popis |
|-----------------|-------------|
| ZÁKLAD            | Použije základní období. |
| BASE+\#         | Použije období, které následuje \# období po základním období. Například pro použití třetího období po základním období zadejte hodnotu **BASE+3**. |
| BASE-\#         | Použije období, které uplynulo \# období před základním obdobím. Chcete-li například použít předchozí období, zadejte hodnotu **BASE-1**. |
| BASE-\#:BASE    | Použije více období, od několika období před základním obdobím až po základní období. Například pro použití tři předchozích období a základního období zadejte hodnotu **BASE-3:BASE**. |
| BASE:BASE+\#    | Použije více období, od základního období až po několik období po základním období. Například pro použití základního období a dvou následujících období zadejte hodnotu **BASE:BASE+2**. |
| BASE-\#:BASE+\# | Použije více období, od několika období před základním obdobím až po několik období po základním období. Například pro použití tři předchozích období, základního období a dvou následujících období zadejte hodnotu **BASE-3:BASE+2**. |
| 1:ZÁKLAD          | Použije více období, od prvního období až po základní období. |
| \#              | Vždy použije konkrétní číslo období. Nedoporučujeme používat tuto možnost, protože snižuje flexibilitu definice sloupce. |
| \#                                      : \#           | Vždy použije konkrétní rozsah období. Nedoporučujeme používat tuto možnost, protože snižuje flexibilitu definice sloupce. |

Při zadávání období můžete překročit hranice fiskálního roku a v rozsahu období můžete použít různé roky. Například zadejte jako období hodnotu **BASE-5** (představující posledních šest období) a spusťte sestavu, která má základní období 2. V takovém případě tato sestava obsahuje data pro první dvě období zadaného fiskálního roku a poslední čtyři období předchozího fiskálního roku.

### <a name="specify-the-periods-for-an-fd-column"></a>Zadání období pro sloupec FD

1. V Návrháři sestav otevřete definici sloupců, kterou chcete změnit.
2. Ve sloupci **FD** klikněte dvakrát na buňku v řádku **Období** a potom vyberte možnost v seznamu.
3. Na řádku vzorce nad navigačním podoknem nebo v buňce **Období** zadejte vzorec. Nahraďte jakýkoli znak křížku (\#) odpovídající hodnotou.

#### <a name="periods-covered-cell"></a>Buňka Pokrytá období

Buňka **Pokrytá období** identifikuje částku, kterou má sloupec zobrazit. Tato částka je relativní vůči hodnotě v buňkách **Fiskální rok** a **Období** pro sloupec. K dispozici jsou tyto možnosti.

| Možnost      | Popis                                                                 |
|-------------|-----------------------------------------------------------------------------|
| PERIODICKÝ    | Zobrazí součet pohybů za aktuální období nebo rozsah období. |
| PERIODICKÝ/BB | Zobrazí počáteční zůstatek za aktuální období nebo rozsah období.   |
| Od začátku roku         | Zobrazí součet pohybů od začátku roku.                               |
| OD POČÁTKU ROKU/BB      | Zobrazí počáteční zůstatek za tento rok.                                 |

### <a name="specify-the-periods-that-are-covered-for-an-fd-column"></a>Zadání pokrytých období pro sloupec FD

1. V Návrháři sestav otevřete definici sloupců, kterou chcete změnit.
2. Ve sloupci **FD** klikněte dvakrát na buňku v řádku **Pokrytá období** a potom vyberte možnost v seznamu.

### <a name="attribute-filter-in-a-column-definition"></a>Filtr atributů v definici sloupce

Atributy jsou hodnoty finančních dat, které podrobněji definují účet nebo transakci. Atributy účtu zahrnují položky **Majetek**, **Závazky**, **Výnosy** a **Výdaje**. Atributy transakce zahrnují položky **Popis transakce** a **Datum použití transakce**. Podpora atributů se v systémech Microsoft Microsoft Dynamics ERP může lišit. Buňka **Filtr atributů** omezuje data ve sloupcích **FD** na konkrétní hodnoty nebo rozsahy pro kategorie atributů. Ačkoli lze tuto funkci použít spolu se sloupcem **ATTR**, sloupec **ATTR** není požadován. Ve sloupci **FD** existuje limit účtů nebo transakcí, které bude sestava obsahovat z filtru atributů.

> [!NOTE]
> Pokud chcete zjistit, jaké atributy váš systém ERP podporuje, prostudujte příručku pro integraci svého systému.

#### <a name="apply-an-attribute-filter-for-an-fd-column-on-a-report"></a>Použití filtru atributů u sloupce FD v sestavě

1. V Návrháři sestav otevřete definici sloupců, kterou chcete změnit.
2. Dvakrát klikněte na buňku **Filtr atributů** u některého sloupce **FD**.
3. V dialogovém okně **Filtr atributů** dvakrát klikněte na buňku ve sloupci **Atribut** a vyberte typ filtru.
4. Chcete-li výsledky dále omezit, zadejte rozsah do sloupců **Od** a **Do**. Buňka **Od** musí obsahovat hodnotu.
5. Klepněte na tlačítko **OK**.

#### <a name="example-of-an-attribute-filter"></a>Příklad filtru atributů

Následující příklad ukazuje část popisu sloupce, který má atribut účtu v řádku **Kód knihy / atribut kategorie**. Filtr atributů pro tento sloupec určuje rozsah hodnot, které mají být zahrnuty do sestavy.

|      Filter                  | A    | mld.                   |
|------------------------------|------|---------------------|
| Typ sloupce                  | POPIS | FD                  |
| Kód knihy / Kategorie atributů |      | SKUTEČNÉ              |
| Fiskální rok                  |      | ZÁKLAD                |
| Období                       |      | 1:ZÁKLAD              |
| Pokrytá období              |      | PERIODICKÝ            |
| ...                          |      |                     |
| Šířka sloupce                 | 30   |                     |
| ...                          |      |                     |
| Filtr atributů             |      | Odkaz=\[01:10\] |

### <a name="dimension-filter-in-a-column-definition"></a>Filtr dimenzí v definici sloupce

Filtr dimenzí slouží k omezení sloupce **FD** na konkrétní hodnoty dimenzí. Filtr může obsahovat jednu dimenzi, rozsah dimenzí nebo skupinu dimenzí. Filtr může také obsahovat sady hodnot dimenzí. Vzhledem k tomu, že se mohou hodnoty dimenzí lišit, nemusí ..\\financial-dimensions\\dimension-based system odpovídat přesné délce. Filtr se použije bez ohledu na to, zda sestava obsahuje strom výkaznictví, či nikoli. Můžete použít zástupné znaky (\* nebo ?) na jakékoli pozici. Když zadáte více účtů, vložte mezi účty čárku, jak je uvedeno v následujícím příkladu: +Částka=\[1200\], +Částka=\[1100\], Oddělení=\[01?\] Abyste získali všechna oddělení pro konkrétní účet,můžete vyloučit dimenzi oddělení z filtru dimenzí. Například oba následující filtry dimenzí jsou zpracovány stejným způsobem:

- +Účet=\[1100\],Oddělení
- +Účet=\[1100\]

Můžete také použít jakoukoli kombinaci alfanumerických znaků pro přesnou shodu a můžete definovat částečné dimenze. Například hodnota **Umístění = \[10\*\]** zahrnuje všechny hodnoty dimenze umístění začínající na 10.

#### <a name="apply-a-dimension-filter-for-a-column-on-a-report"></a>Použití filtru dimenzí pro definici sloupce v sestavě

1. V Návrháři sestav otevřete definici sloupců, kterou chcete změnit.
2. Klikněte dvakrát na buňku **Filtr dimenzí** pro sloupec **FD**.
3. V dialogovém okně **Dimenze** zadejte filtry, které chcete použít.
4. Klepněte na tlačítko **OK**.

### <a name="format-a-multiple-currency-report-in-a-column-definition"></a>Formátování sestavy s více měnami v definici sloupce

Sestava více měn může zobrazit částky v zúčtovací měně hlavní knihy, v měně vykazování hlavní knihy, původní měně transakce nebo v převedené měně vykazování. Zúčtovací měna společnosti je definována v nastavení hlavní knihy. Nepleťte si toto nastavení s místním nastavením operačního systému, kde se konfigurují symboly výchozí měny pro sestavy. Definice sloupce obsahuje následující dostupné buňky související s měnou:

- **Zobrazení měny** – určuje typ měny (účetnictví, vykazování, transakce nebo převedené výkaznictví), ve které se transakce zobrazí. Funkce převodu na měnu vykazování se někdy označuje jako převod měny. Převod měn je schopnost uvádět částky hlavní knihy v sestavách v měně, která nemusí být funkční měnou nebo měno vykazování společnosti, ani měnou, ve které byla zadána transakce.
- **Filtr měny** – definuje filtr měny. V sestavě jsou zobrazeny pouze transakce, které byly zadány ve vybrané měně.

> 
Chcete-li určit zúčtovací měnu společnosti, postupujte takto.

1. V Návrháři sestav klikněte v nabídce **Společnost** na příkaz **Společnosti**.
2. V dialogovém okně **Společnosti** vyberte společnost a klikněte na tlačítko **Zobrazení**.
3. V dialogovém okně **Zobrazit společnost** v části **Možnosti místního nastavení** můžete zobrazit měnu, která je definovaná pro vybranou společnost.

#### <a name="specify-the-currency-on-a-multiple-currency-report"></a>Zadání měny v sestavě s více měnami

1. V Návrháři sestav otevřete definici sloupců, kterou chcete změnit.
2. Klikněte dvakrát na buňku **Zobrazení měny** v odpovídajícím sloupci **FD** a poté vyberte možnost zobrazení informací o měně: **Zúčtovací měna pro hlavní knihu**, **Vykazování hlavní knihy**, měnu transakce nebo vyberte možnost převodu na jinou měnu vykazování.
3. Klikněte dvakrát na buňku **Filtr měny** v odpovídajícím sloupci **FD** a poté vyberte odpovídající kód měny v seznamu. V sestavě jsou zobrazeny pouze transakce, které byly zadány v této měně.


### <a name="example-for-currency-display-and-currency-filter-cells"></a>Příklad pro buňky Zobrazení měny a Filtr měny

Uživatel ve své definici sloupce vybral následující měny:

- **Filtr měny:** Jen
- **Zobrazení měny:** Zúčtovací měna z hlavní knihy (USD)

Vzhledem k filtru měny, který uživatel vybral, se do sestavy zahrnou pouze transakce, které byly zadány v japonských jenech (JPY). Vzhledem k zobrazení měny, které uživatel vybral, se v sestavě zobrazí tyto transakce v zúčtovací měně (americké dolary – USD).

#### <a name="currency-filter-and-currency-display-combinations"></a>Kombinace filtru měny a zobrazení měny

Následující tabulka obsahuje výsledky sestavy, které mohou nastat pro různé kombinace možností v buňkách **Zobrazení měny** a **Filtr měny** z důvodu voleb, které uživatel provedl. Funkční měna je USD.


| Buňka Zobrazení měny                        | Buňka Filtr měny | Výsledek sestavy |
|----------------------------------------------|----------------------|---------------|
| Měna transakce                 | **JEN**              | **6 000 Y** – výsledek ukazuje pouze transakce, které byly zadány v měně JPY. |
| Zúčtovací měna z hlavní knihy | **JEN**              |**60 $** – výsledek zobrazí pouze transakce, které byly zadány v měně JPY, a tyto transakce zobrazí v měně USD.<p><strong>Poznámka:</strong> Směnný kurz je přibližně 100 JPY na USD.</p> |
| Zúčtovací měna z hlavní knihy | Prázdné                | **2 310 USD** – Výsledek zobrazí všechna data v zúčtovací měně, která je určena v hlavní knize.<p><strong>Poznámka:</strong> Tato částka je součtem všech transakcí v zúčtovací měně.</p> |
| Měna transakce                 | Prázdné                | **2 250 $** – výsledek obsahuje všechny částky v měně, ve které byla provedena transakce. To znamená, že součet skládá dohromady částky z různých měn. |

### <a name="calculation-column-in-a-column-definition"></a>Sloupec Výpočet v definici sloupců

Typ sloupce **CALC** v definici sloupce podporuje složité výpočty v buňce **Formula** a může obsahovat operátory **+**, **-**, **\**_ a _*/**, a také příkazy **IF/THEN/ELSE**. Sloupec výpočtu může také odkazovat na libovolný sloupec, dokonce i následující sloupce. Kromě toho výpočet sloupce můžete zahrnout také fiskální rok a období k podpoře záhlaví sloupce. Vzorec výpočtu může mít délku až 1 024 znaků. Pokud chcete výsledek výpočtu vyjádřit procentuální hodnotou, použijte formát přepisu.

> [!NOTE]
> Ve výsledcích výpočetních vzorců nejsou zahrnuty hodnoty v netisknutelných rozsazích sloupců. Například hodnota **A:D** vytiskne hodnotu **0** (nula), zatímco hodnota **A+B+C** pro netisknuté hodnoty vypočítá hodnotu.

#### <a name="operators-in-calculation-columns"></a>Operátory ve výpočetních sloupcích

Chcete-li sloupce sčítat, odečítat, násobit nebo dělit, zadejte písmena sloupců v pořadí výpočtu a pak jednotlivá písmena sloupců oddělte příslušným operátorem. Následující tabulka vysvětluje operátory, které lze použít ve sloupci výpočtu.

| Operátor | Příklad výpočtu | popis |
|----------|---------------------|-------------|
| +        | A+C                 | Přičte částku ve sloupci A k částce ve sloupci C. |
| :        | A:C A:C-D           | Sečte rozsah po sobě jdoucích sloupců. Například vzorec **A:C** sečte součty sloupců od A do C a vzorec **A:C-D** sečte součty sloupců od A do C a potom odečte částku ve sloupci D. |
| -        | A-C                 | Odečte částku ve sloupci A od částky ve sloupci C.<p><strong>Poznámka:</strong> znaménko minus (-) lze také slouží k obrácení znamének ve sloupci. Například můžete použít vzorec <strong>-A+B</strong> k přičtení obrácené hodnoty částky ve sloupci A k částce ve sloupci B.</p> |
| \*       | A\*C                | Vynásobí částku ve sloupci A částkou ve sloupci C. |
| /        | A/C                 | Vydělí částku ve sloupci A částkou ve sloupci C. |

#### <a name="use-a-calculation-formula-in-a-column-definition"></a>Použije vzorec výpočtu v definici sloupce

1. V Návrháři sestav otevřete definici sloupců, kterou chcete změnit.
2. V příslušném sloupci **CALC** zadejte vzorec do buňky **Vzorec**.

#### <a name="complex-calculations"></a>Složité výpočty

Složitý výpočet může obsahovat libovolnou kombinaci odkazů na buňky, operátorů, hodnot a úrovní vnořených závorek. Vypočítat k výpočtu průměru ze sloupců A a B použijte výpočetní vzorec **((A+B)/2)**.

#### <a name="specify-report-cells-in-a-column-calculation"></a>Zadání buněk sestavy ve výpočtu sloupce

Na konkrétní buňku sestavy lze odkázat zadáním písmene sloupce a kódu řádku. Například **B.100** odkazuje na kód řádku 100 ve sloupci B. Můžete vydělit celý sloupec konkrétní hodnotou buňky sestavy, která se nachází ve stejném sloupci. Například výpočet **B/B.100** znamená, že částka ve sloupci B má být vydělena hodnotou v řádku s kódem 100 ve sloupci B. Odkazuje-li výpočet na sloupec, který závisí na jiném sloupci, je nejprve vyřešen závislý sloupec. Pokud nějaký sloupec odkážete na jiný sloupec a tento sloupec odkazuje zpět na první sloupec, způsobíte chybu cyklického odkazu.

> [!NOTE]
> Výpočet může být nesprávný, pokud změníte prioritu výpočtů sestavy. Prioritu pro výpočet lze nastavit na kartě **Nastavení** v definici sestavy.

#### <a name="multiply-or-divide-a-column-by-a-base-row"></a>Násobení nebo dělení sloupce základním řádkem

Můžete vytvořit sloupec, který zobrazuje všechny hodnoty v zadaném sloupci jako procentuální hodnotu určitého základu. Můžete tedy znázornit vztahy mezi řádky, například procentuální hodnotu řádku prodeje nebo procentuální hodnotu řádku celkových výdajů. Chcete-li násobit nebo dělit každý řádek v konkrétním sloupci základním řádkem, zadejte sloupec k použití při výpočtu a potom zadejte hodnotu **\*BASEROW** nebo **/BASEROW**. Zadejte například vzorec **C\*BASEROW** nebo **C/BASEROW**.

> [!NOTE]
> Pokud v definici sloupců použijete výpočet základního řádku, musí každá definice řádků použitá s touto definicí sloupců obsahovat alespoň jeden základní řádek pro výpočty.

#### <a name="divide-the-amount-in-a-column-by-the-number-of-periods"></a>Vydělení částky ve sloupci počtem období

Částku v některém sloupci můžete vydělit zadaným počtem období. Například vzorec **B/Období** vydělí hodnotu ve sloupci B počtem období ve sloupci B. Pokud výpočet pokrývá více sloupců, zadejte počet období, který má být použit ve výpočtu. Například vzorec **(B+C)/Období** sečte částky ve sloupcích B a C a potom výslednou hodnotu vydělí hodnotou období.

## <a name="additional-resources"></a>Další zdroje

[Definice řádku v návrháři finanční sestavy](row-definitions-financial-reporting.md)

[Rozšířené možnosti formátování ve finančním výkaznictví](advanced-formatting-options-financial-reporting.md)
