---
title: "Definice sloupce ve finančních sestavách"
description: "Tento článek obsahuje informace o definicích sloupce. Definice sloupce je součástí sestavy nebo stavebního bloku, který definuje obsah jednotlivých sloupců v sestavě. Stejně jako definice řádků lze základní definice sloupců použít u více sestav."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Management Reporter, UnifiedOperations, Core
ms.custom: 106601
ms.assetid: 66e72a48-edab-4e9d-815f-596a1623c258
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30T00:00:00.000Z
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 770a1681e4fa9974b081d0c63a10eb1961f13014
ms.openlocfilehash: d976988a599f65de9957c53a2d149576a1a11d83
ms.contentlocale: cs-cz
ms.lasthandoff: 06/13/2017

---

# <a name="column-definitions-in-financial-reports"></a>Definice sloupce ve finančních sestavách

[!include[banner](../includes/banner.md)]


Tento článek obsahuje informace o definicích sloupce. Definice sloupce je součástí sestavy nebo stavebního bloku, který definuje obsah jednotlivých sloupců v sestavě. Stejně jako definice řádků lze základní definice sloupců použít u více sestav.

<a name="create-and-modify-a-column-definition"></a>Vytvoření a úprava definice sloupce
-------------------------------------

Definice sloupce může obsahovat 2 až 255 sloupců.

### <a name="create-a-column-definition"></a>Vytvoření definice sloupce

1.  V Návrháři sestav v navigačním podokně klikněte na tlačítko **Definice sloupce**.
2.  V nabídce **Soubor** klikněte na tlačítko **Nový** a vyberte možnost **Definice sloupce**.
3.  Přidejte obsah definice sloupce.

### <a name="open-a-column-definition"></a>Otevření definice sloupce

1.  V Návrháři sestav v navigačním podokně klikněte na tlačítko **Definice sloupce**.
2.  Kliknutím dvakrát otevřete definici sloupce.

### <a name="add-a-column-to-a-column-definition"></a>Přidání sloupce do definice sloupce

1.  V Návrháři sestav klikněte na tlačítko **Definice sloupce** a potom otevřete definici sloupce ke změně.
2.  Vyberte sloupec v místě, kam chcete vložit nový sloupec.
3.  V nabídce **Upravit** klikněte na tlačítko **Vložit sloupec**. Nový sloupec se zobrazí nalevo od sloupce, který jste vybrali.

### <a name="delete-a-column-from-a-column-definition"></a>Odstranění sloupce z definice sloupce

1.  V Návrháři sestav klikněte na tlačítko **Definice sloupce** a potom otevřete definici sloupce ke změně.
2.  Vyberte sloupec, který chcete odstranit.
3.  V nabídce **Upravit** klikněte na tlačítko **Odstranit sloupec**.

## <a name="contents-of-a-column-definition"></a>Obsah definice sloupce
Definice sloupce obsahuje následující informace:

-   sloupec s popisy pro definice řádku;
-   sloupce s částkami, které obsahují data z finančních dat, list aplikace Microsoft Excel nebo výpočty, které jsou založeny na jiných datech definice sloupce;
-   sloupce formátování;
-   sloupce atributů.

Tyto informace se zobrazí v následujících oblastech v definici sloupce:

-   Oblast záhlaví definice sloupce obsahuje text a formátování záhlaví, které se zobrazí v sestavě. Záhlaví může platit pro jeden sloupec dat, může zahrnovat více sloupců nebo může platit pro sloupce na základě podmínek. Definice sloupce může zahrnovat libovolný počet řádků záhlaví sloupců dle potřeby. **Poznámka:** Záhlaví sloupců platí pro jednotlivé sloupce dat v sestavě. Záhlaví sestavy platí pro celou sestavu. Lze definovat záhlaví sestavy na kartě **Záhlaví a zápatí** v rámci definice sestavy.
-   Řádky s podrobnostmi sloupců jsou řádky pod řádky záhlaví v definici sloupce. Řádky s podrobnostmi sloupce definují informace, které jsou zahrnuty v sestavě. V následující tabulce jsou uvedeny a popsány řádky podrobností sloupce.

    | Název řádku podrobností sloupce                                                | Popis                                                                                            |
    |-----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
    | Typ sloupce                                                           | (Požadováno) Určete typ dat ve sloupci.                                                     |
    | Kód knihy / atribut kategorie                                          | Zadejte informace o finančních datech pro sloupce typů **FD** a **ATTR**.                       |
    | Zahrnutá období fiskálního roku                                    | Zadejte informace o finančních datech pro sloupce typu **FD**.                                     |
    | Receptura                                                               | Zadejte vzorec pro výpočet sloupců typu **CALC**.                                        |
    | Šířka sloupce Další mezery před sloupcem Přepsání formátu Řízení tisku | Určete speciální možnosti formátování.                                                                        |
    | Omezení sloupce                                                   | Omezují data.                                                                                         |
    | Jednotka výkaznictví                                                        | Omezí sloupec, aby zobrazoval data pouze pro určenou jednotku výkaznictví.                      |
    | Zobrazení měny Filtr měny                                      | Formátuje měnu.                                                                                       |
    | Filtr dimenze                                                      | Určete filtr k omezení dat na určitá finanční data jednotek výkaznictví.                           |
    | Filtr atributů                                                      | Definujte filtr pro omezení finančních dat.                                                       |
    | Počáteční datum Koncové datum                                                   | Omezuje finanční údaje na konkrétní data.                                                         |
    | Odůvodnění                                                         | Zarovná doleva, na střed nebo doprava text popisu, který je určen v definici řádku. |

## <a name="column-restrictions-in-a-column-definition"></a>Omezení sloupce v definici sloupce
Omezení sloupce slouží k určení způsobu, jakým definice sloupce používá data nebo počítá informace. Můžete také omezit sloupec sestavy na určitou jednotku nebo konkrétní data. **Poznámka:** A kód **Omezení sloupce** přepíše všechna konfliktní nastavení, která jsou přiřazena v definici řádku.

### <a name="column-restrictions-cell"></a>Buňka Omezení sloupce

Buňka **Omezení sloupce** může zahrnovat kódy, které omezují nebo potlačují informace, jako jsou například formátování řádků, podrobnosti a částky pro daný sloupec.

#### <a name="add-a-column-restriction-in-a-column-definition"></a>Přidání omezení sloupce do definice sloupce

1.  V Návrháři sestav otevřete definici sloupce k úpravě.
2.  Klikněte dvakrát na buňku **Omezení sloupce** pro sloupec k omezení.
3.  V dialogovém okně **Omezení sloupce** vyberte v seznamu jeden nebo více kódů a klikněte na tlačítko **OK**.

### <a name="column-restriction-codes"></a>Kódy omezení sloupce

V následující tabulce jsou popsány kódy omezení sloupce.

| Kód omezení sloupce | Popis                                                                                                                                                                                                                                                                                                                             |
|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SU                      | Potlačí podtržení sloupce, kde je zadán příkaz podtržení (**---**) nebo příkaz dvojitého podtržení (**===**) v definici řádku. Nemusí být vhodné například podtrhovat částky, které jsou vytvářeny podle výpočtu procentuální hodnoty.                                                                        |
| ST                      | Potlačí součty, aby byly ve sloupci uvedeny pouze podrobnosti (například statistický sloupec).                                                                                                                                                                                                                                      |
| SD                      | Potlačí podrobnosti, takže se ve sloupci zobrazí pouze řádky **TOT** a **CAL** (z definice řádku).                                                                                                                                                                                                                              |
| OŘ                      | Omezí částky ve sloupci **FD** na částky Má dáti.                                                                                                                                                                                                                                                                              |
| CR                      | Omezí částky ve sloupci **FD** na částky Dal.                                                                                                                                                                                                                                                                             |
| ADJ                     | Omezí částky ve sloupci na částky úpravy období, jsou-li tyto částky k dispozici.                                                                                                                                                                                                                                        |
| XAD                     | Omezí částky ve sloupci tak, aby byly částky úpravy období vyloučeny.                                                                                                                                                                                                                                                     |
| PP                      | Omezí částky ve sloupci tak, aby byly zahrnuty pouze zaúčtované transakce, pokud jsou tyto transakce k dispozici.                                                                                                                                                                                                                 |
| UPT                     | Omezí částky ve sloupci tak, aby byly zahrnuty pouze nezaúčtované transakce, pokud jsou tyto transakce k dispozici. **Poznámka:** Ne všichni poskytovatelé dat podporují nezaúčtované transakce. Další informace naleznete v [příručce k integraci dat](http://go.microsoft.com/fwlink/?LinkID=162565) systému Microsoft Dynamics ERP. |

### <a name="restrict-a-column-to-a-reporting-unit"></a>Omezení sloupce na jednotku výkaznictví

1.  V Návrháři sestav otevřete definici sloupce k úpravě.
2.  Klikněte dvakrát na buňku **Jednotka výkaznictví** pro sloupec k omezení.
3.  V dialogovém okně **Výběr jednotky výkaznictví** v seznamu **Strom výkaznictví** vyberte strom.
4.  Rozbalte nebo sbalte seznam jednotek vyberte jednotku výkaznictví a klikněte na tlačítko **OK**.

## <a name="format-column-headers"></a>Záhlaví sloupců formátu
Můžete přidat, upravit a odstranit záhlaví, která se zobrazí v horní části sloupců v sestavě. Také můžete nakonfigurovat podmíněné pokrývání záhlaví sloupců na základě pole **Období** z definice sloupce a pole **Základní období** z definic sestavy. Funkce základního období pomáhá šetřit čas při vytváření sestav průběžných prognóz.

### <a name="create-and-manage-column-headers"></a>Vytvoření a správa záhlaví sloupců

Můžete přidat, upravit a odstranit záhlaví, která se zobrazí v horní části sloupců v sestavě, pomocí dialogového okna **Záhlaví sloupce**. Pole dialogového okna **Záhlaví sloupce** jsou popsána v následující tabulce.

| Pole                 | Popis                                                                                                                                                                                                                                                                                                              |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Text záhlaví sloupce    | Tento text se zobrazí v záhlaví sloupce. Můžete zadat text přímo do tohoto pole nebo kliknout na tlačítko **Vložit automatický text** a vybrat možnost, která aktualizuje záhlaví sloupce pokaždé, když je vygenerována sestava. Chcete-li zahrnout více kódů automatického textu, klikněte na tlačítko **Vložit automatický text** znovu a potom klikněte na další kód v seznamu. |
| Možnosti formátu        | Použijte formátování na záhlaví sloupce, například ohraničení nebo podtržení.                                                                                                                                                                                                                                                           |
| Pokrýt od Pokrýt k | Definujte sloupec nebo sloupce, pro které textu záhlaví platí.                                                                                                                                                                                                                                                            |
| Odůvodnění         | Určete jak má být text záhlaví sloupce zarovnán pro sloupec nebo rozsah sloupců určený pomocí polí **Pokrýt od** a **Pokrýt k**.                                                                                                                                                               |

### <a name="create-a-column-header"></a>Vytvoření záhlaví sloupce

1.  V Návrháři sestav otevřete definici sloupce k úpravě.
2.  Klikněte dvakrát na buňku záhlaví.
3.  V dialogovém okně **Záhlaví sloupce** zadejte text záhlaví sloupce. Případně klikněte na tlačítko **Vložit automatický text** a vyberte možnost.
4.  V poli **Možnosti formátu** vyberte formát pro záhlaví.
5.  V poli **Pokrýt od** zadejte písmeno sloupce, nad kterým má začít záhlaví sloupců. V poli **Pokrýt k** zadejte písmeno sloupce, nad kterým má končit záhlaví sloupců.
6.  V části **Zarovnání** vyberte, zda má být text záhlaví sloupců zarovnaný vlevo, zarovnaný na střed nebo zarovnaný vpravo.
7.  Klepněte na tlačítko **OK**.

### <a name="add-a-column-header-row"></a>Přidání řádku záhlaví sloupců

1.  V Návrháři sestav otevřete definici sloupce k úpravě.
2.  Vyberte buňku v řádku záhlaví.
3.  V nabídce **Upravit** klikněte na tlačítko **Vložit řádek**. Nový řádek se vloží nad řádek, který jste vybrali v kroku 2. **Poznámka:** používáte-li v sestavě pro záhlaví sestavy čtyři nebo více řádků, záhlaví se budou při exportu sestavy do listu aplikace Excel překrývat. Chcete-li v sestavě zobrazit všechna záhlaví, zvětšete horní okraj v definici sestavy.

### <a name="delete-a-column-header-row"></a>Odstranění řádku záhlaví sloupců

1.  V Návrháři sestav otevřete definici sloupce k úpravě.
2.  V řádku záhlaví vyberte buňku k odstranění.
3.  V nabídce **Upravit** klikněte na tlačítko **Odstranit řádek**.

### <a name="create-an-automatically-generated-header"></a>Vytvoření automaticky generovaného záhlaví

Návrhář sestav může automaticky generovat záhlaví sloupců na základě kódů automatického textu. Kódy automatického textu jsou proměnné, které jsou aktualizovány při každém vygenerování sestavy. Jakékoli záhlaví sloupce může zahrnovat tyto kódy s cílem určit informace sestavy, které se mohou lišit, jako například kalendářní data nebo čísla období. Můžete tedy použít jednu definici sloupce pro více definic sestavy, časových období a stromů výkaznictví. Protože kódy automatického textu závisí na informacích kalendáře z řádků podrobností definice sloupce, jsou podporovány pouze u sloupců **CALC**, **FD** a **WKS**. Způsob, jakým se kód automatického textu zobrazí v buňce záhlaví sloupce ovlivňuje způsob zobrazení informací na sestavě. V dialogovém okně **Záhlaví sloupce** se kódy automatického textu zobrazí s malými i velkými znaky. Proto se text zobrazí s malými i velkými znaky v sestavě. Například ve standardním kalendářním roku vypíše kód **@CalMonthLong** měsíc **7** jako **Červenec**. Pokud má název měsíce být psán velkými písmeny (například **ČERVENEC**), zadejte kód automatického textu velkými písmeny do pole **Text záhlaví sloupce**. Například zadejte **@CALMONTHLONG**. Můžete kombinovat kódy a text. Například zadejte následující text záhlaví: **Období @FiscalPeriod-@FiscalYear od @StartDate do @EndDate**. Záhlaví sestavy, které bude vygenerováno, bude vypadat nápodobně: **Period 1-02 od 1.1.2002 do 31.1.2002**. **Poznámka:** Formát částí textu, jako například dlouhé datum, závisí na vašich místních nastaveních serveru Finance and Operations. Tato nastavení můžete změnit, kliknutím na tlačítko **Start**, na položku **Ovládací panely** a nakonec na položku **Oblast a jazyk**. V následující tabulce jsou uvedeny dostupné možnosti automatického textu pro záhlaví sloupců.

| Možnost a kód automatického textu                | popis                                                                                                                                                                                                                                                                                      |
|-----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Název měsíce (@CalMonthLong)              | Vytiskne název aktuálního měsíce v záhlaví sloupce. Pokud se rozhodnete zaokrouhlovat částky v sestavě na tisíce, miliony nebo miliardy nebo nastavíte šířku sloupce v sestavě na menší šířku než devět znaků, název měsíce se zkrátí na první tři znaky. |
| Zkrácený název měsíce (@CalMonthShort) | Vytiskne zkrácený název měsíce pro vybrané fiskální období.                                                                                                                                                                                                                          |
| Číslo období (@FiscalPeriod)           | Vytiskne číselnou formu fiskálního období, které je určeno pro daný sloupec. Pokud sloupec zahrnuje více období, vytiskne se poslední období v rozsahu.                                                                                                                                   |
| Popis období (@FiscalPeriodName)  | Vytiskne popis fiskálního období, které je určeno ve finančních datech.                                                                                                                                                                                                                    |
| Fiskální rok (@FiscalYear)               | Vytiskne fiskální rok pro sloupec v číselné formě.                                                                                                                                                                                                                                            |
| Kalendářní rok (@CalYear)                | Vytiskne kalendářní rok pro sloupec v číselné formě.                                                                                                                                                                                                                                          |
| Počáteční datum (@StartDate)                 | Vytiskne počáteční datum pro sloupec.                                                                                                                                                                                                                                                             |
| Koncové datum (@EndDate)                     | Vytiskne koncové datum pro sloupec.                                                                                                                                                                                                                                                               |
| Název jednotky ze stromu (@UnitName)         | Jestliže omezíte sloupce pro určitou jednotku stromu výkaznictví, vytiskne název jednotky v záhlaví sloupce.                                                                                                                                                                                     |
| Popis jednotky (@UnitDesc)            | Jestliže omezíte sloupec na určitou jednotku stromu výkaznictví, vytiskne popis jednotky v záhlaví sloupce.                                                                                                                                                                              |
| Kód knihy (@BookCode)                   | Vytiskne kód knihy stanovený ve sloupci.                                                                                                                                                                                                                                             |
| Prázdný řádek (@Blank)                     | Vloží prázdný řádek do záhlaví sloupce.                                                                                                                                                                                                                                                       |

### <a name="create-a-conditional-spanning-header"></a>Vytvoří záhlaví s podmíněným pokrytím

Záhlaví s podmíněným pokrytím mohou zahrnovat více sloupců, které vycházejí z dat pro určité období. Například pokud máte sestavu rozpočtu pro fiskální rok a chcete zobrazit skutečné rozpočty posledních měsíců spolu s předpokládanými rozpočty budoucích měsíců, můžete použít záhlaví s podmíněným pokrytím k automatické aktualizaci záhlaví sestavy. Při vytváření záhlaví s podmíněným pokrytím mějte na zřeteli následující situace:

-   Jakákoli podmínka zastavení (pole **Pokrýt k**) vyhovující před podmínkou začátku (pole **Pokrýt od**) bude ignorována. Například sloupec B má podmínku pokrytí definovanou jako BASE+1 až BASE. Období BASE je ve sloupci C a BASE+1 ve sloupci D. V takovém případě je podmínka zastavení ve sloupci C ignorována a tisk záhlaví začíná od sloupce D.
-   Pokud zadáte záhlaví sloupců, které se budou překrývat, budou se překrývat i při tisku sestavy. estava bude vygenerována, ale zobrazí se následující upozornění v poli **Stav fronty sestav**: „Záhlaví sloupců používající základ se překrývají s jinými záhlavími sloupců a mohou způsobit překrývání textu.“ Například definice záhlaví sloupce B je B až BASE+1 a definice záhlaví ve sloupci D je BASE+1 až F. V takovém případě se záhlaví tisknou na sebe a jsou nečitelná. Vždy při použití funkce BASE v definici **Pokrýt od / Pokrýt k** si prohlédněte vygenerovanou sestavu a zkontrolujte, zda se záhlaví nepřekrývají.
-   Pokud v definici pokrytí zadáte hodnotu BASE ve sloupci Netisknout (**NP**), bude ignorována bez ohledu na to, co je definováno v definici sloupce. Tento scénář je v podstatě stejný, jako když nevytvoříte definici záhlaví sloupce.
-   V případě sloupců s podmíněným tiskem (**P&lt;B**, **P&gt;=B**) se záhlaví s podmíněným pokrytím chová jako jakákoli běžná definice záhlaví sloupce. Například pokud podmínka není splněna, všechny následné sloupce splňující podmínku pokrytí zahájí tisk záhlaví.

#### <a name="create-a-conditional-spanning-header"></a>Vytvoří záhlaví s podmíněným pokrytím

1.  V Návrháři sestav otevřete definici sloupce k úpravě.
2.  Klikněte dvakrát na buňku záhlaví.
3.  V dialogovém okně **Záhlaví sloupce** zadejte text záhlaví sloupce. Případně klikněte na tlačítko **Vložit automatický text** a vyberte možnost.
4.   V poli **Možnosti formátu** vyberte styl formátování pro záhlaví.
5.  Zadejte období vzhledem k základnímu období, které se stanoví během generování sestavy. V polích **Pokrýt od** a **Pokrýt k** zadejte některou z následujících hodnot: **BASE**, **BASE-X** nebo **BASE+X**, kde X je počet období od základního období. Zadáte-li například **BASE** do pole **Pokrýt od**, text záhlaví sloupce s podmíněným pokrytím začíná v záhlaví sloupce, kde se hodnota definice sestavy **Základní období** rovná hodnotě definice sloupce **Období**. Končí ve sloupci, který je určen v poli **Pokrýt k**. Proto pokud je pokrytí od BASE k M a hodnota definice sestavy **Základní období** je **4**, záhlaví začne ve sloupci, ve kterém je období nastaveno na hodnotu **4** a končí ve sloupci M. Záhlaví končí a začínají pouze v tisknutých sloupcích.
6.  V části **Zarovnání** vyberte, zda má být text záhlaví sloupců zarovnaný vlevo, zarovnaný na střed nebo zarovnaný vpravo.
7.  Klepněte na tlačítko **OK**.

#### <a name="example-of-a-conditional-spanning-header"></a>Příklad záhlaví s podmíněným pokrytím

Pavla vytváří sestavu pro dynamickou šestiměsíční prognózu. Chce, aby bylo vytištěno slovo „Skutečné“ nad sloupci, které obsahují skutečná data, a slovo „Rozpočet“ má být vytištěno nad sloupci, které obsahují prognózy rozpočtu. Každý měsíc spuštění sestavy přibude navíc jeden skutečný sloupec a ubude jeden sloupec rozpočtu. Ačkoli může Pavla upravit definici sloupců pokaždé, když sestavu generuje, a ručně upravit záhlaví, aby ušetřila čas a úsilí, rozhodla se vytvořit záhlaví s podmíněným pokrytím, která budou automaticky vytvářet záhlaví na příslušnými sloupci při každém spuštění sestavy. Pavla otevře Návrhář sestav, klikne na tlačítko **Definice sloupce** v navigačním podokně a otevře definici sloupce pro sestavu. Poté zadá následující informace. Základní období v definici sestavy je 4.

|                     | A.    | mld.             | K             | P             | E.             | F.             | G.             | H.             | N             | J             | tis.             | V             | mil.             |
|---------------------|------|---------------|---------------|---------------|---------------|---------------|---------------|---------------|---------------|---------------|---------------|---------------|---------------|
| Záhlaví 1            |      | Skutečná        | Rozpočet        |               |               |               |               |               |               |               |               |               |               |
| Záhlaví 2            |      | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong |
| Záhlaví 3            |      |               |               |               |               |               |               |               |               |               |               |               |               |
| Typ sloupce         | POPIS | FD            | FD            | FD            | FD            | FD            | FD            | FD            | FD            | FD            | FD            | FD            | FD            |
| Kód knihy / atribut |      | SKUTEČNÝ        | ROZPOČET2012    | SKUTEČNÝ        | ROZPOČET2012    | SKUTEČNÝ        | ROZPOČET2012    | SKUTEČNÝ        | ROZPOČET2012    | SKUTEČNÝ        | ROZPOČET2012    | SKUTEČNÝ        | ROZPOČET2012    |
| Fiskální rok         |      | ZÁKLAD          | ZÁKLAD          | ZÁKLAD          | ZÁKLAD          | ZÁKLAD          | ZÁKLAD          | ZÁKLAD          | ZÁKLAD          | ZÁKLAD          | ZÁKLAD          | ZÁKLAD          | ZÁKLAD          |
| Období              |      | 1             | 1             | 2             | 2             | 3             | 3             | 4             | 4             | 5             | 5             | 6             | 6             |
| Pokrytá období     |      | PERIODICKÝ      | PERIODICKÝ      | PERIODICKÝ      | PERIODICKÝ      | PERIODICKÝ      | PERIODICKÝ      | PERIODICKÝ      | PERIODICKÝ      | PERIODICKÝ      | PERIODICKÝ      | PERIODICKÝ      | PERIODICKÝ      |
| Šířka sloupce        | 30   | 10            | 10            | 10            | 10            | 10            | 10            | 10            | 10            | 10            | 10            | 10            | 10            |
| Řízení tisku       |      | P&lt;=B       | P&gt;B        | P&lt;=B       | P&gt;B        | P&lt;=B       | P&gt;B        | P&lt;=B       | P&gt;B        | P&lt;=B       | P&gt;B        | P&lt;=B       | P&gt;B        |

Pavla kliknutím dvakrát na buňku záhlaví sloupce otevřete dialogové okno **Záhlaví sloupce**, kam zadá následující informace.

| Pole              | Hodnota                 |
|--------------------|-----------------------|
| Text záhlaví sloupce | Skutečnost                |
| Vložit automatický text    | Nebude proveden žádný výběr. |
| Možnosti formátu     | Pole                   |
| Odůvodnění      | Nebude proveden žádný výběr. |
| Pokrýt od        | mld.                     |
| Pokrýt k          | ZÁKLAD                  |
| Záhlaví rozpočtu      | BASE+1 po konečný sloupec  |

Poté, co dokončí zadávání informací, Pavla klikne na tlačítko **OK**. Poté kliknutím dvakrát na buňku záhlaví sloupce C otevřete dialogové okno **Záhlaví sloupce**, kam zadá následující informace.

| Pole              | Hodnota                 |
|--------------------|-----------------------|
| Text záhlaví sloupce | Rozpočet                |
| Vložit automatický text    | Nebude proveden žádný výběr. |
| Možnosti formátu     | Pole                   |
| Odůvodnění      | Nebude proveden žádný výběr. |
| Pokrýt od        | K                     |
| Pokrýt k          | ZÁKLAD+2                |

Nyní při každém vygenerování této sestavy bude vytištěno slovo „Skutečné“ nad sloupci, které obsahují skutečná data, a slovo „Rozpočet“ bude vytištěno nad sloupci, které obsahují prognózy rozpočtu. Navíc bude počet sloupců upraven každý měsíc.

## <a name="apply-column-justification"></a>Použít zarovnání sloupce
Buňka **Zarovnání** se používá k formátování zarovnání sloupce popisu v sestavě. Tato možnost ovlivňuje pouze popisy sloupců ne skutečné hodnoty.

1.  V Návrháři sestav otevřete definici sloupce k úpravě.
2.  Dvakrát klikněte na buňku **Zarovnání**.
3.  Vyberte ze seznamu jednu z následujících hodnot:
    -   **Žádné** – nebude použito žádné zarovnání.
    -   **Vlevo** – popisy sloupců se zarovnají doleva.
    -   **Na střed** – popisy sloupců se zarovnají na střed.
    -   **Vpravo** – popisy sloupců se zarovnají doprava.

## <a name="add-special-formatting-options"></a>Přidání speciálních možností formátování
V definici sloupce aplikují řádky podrobností sloupce formátování speciální formátování na vybrané sloupce. I když jsou některé možnosti **Řízení tisku** a možnosti **Omezení sloupce** specifické pro sloupce **FD**, většina možnosti platí pro všechny typy sloupců. Formátování určené v definici sloupce přepíše formátování určené v definici sestavy. Nicméně formátování určené v definici řádku přepíše formátování určené v definici sloupce. Tyto řádky jsou považovány za řádky formátování:

-   Šířka sloupce
-   Další mezery před sloupcem
-   Přepsání formátu/měny
-   Řízení tisku

### <a name="changing-the-column-width"></a>Změna šířky sloupce

Buňka **Šířka sloupce** určí počet znaků, které mají být použity pro šířku tohoto sloupce v tištěné sestavě. Šířka sloupců je důležitá pro sloupce, které obsahují částky (sloupce typu **CALC**, **WKS** nebo **FD**), popisy (sloupce typu **DESC**) nebo vyplnění (sloupce typu **FILL**). Ve výchozím nastavení je zvolena možnost **Automaticky přizpůsobit**, takže každý sloupec je automaticky upraven podle obsahu.

#### <a name="specify-the-width-of-a-column-on-a-report"></a>Určení šířky sloupce v sestavě

1.  V Návrháři sestav otevřete definici sloupce k úpravě.
2.  V buňce **Šířka sloupce** zadejte počet míst pro šířku sloupce. Maximální šířka jakéhokoli sloupce je 255 znaků (toto číslo zahrnuje procenta, čárky i závorky). Chcete-li návrháři sestav umožnit výběr vhodné šířky pro sloupec na základě obsahu buněk, můžete dvakrát kliknout na buňku **Šířka sloupce** a poté kliknout na možnost **Automaticky přizpůsobit**.

### <a name="add-space-between-columns"></a>Přidání mezery mezi sloupci

Buňka **Další mezery před sloupcem** určuje šířku oddělovače mezi jedním sloupcem a přiléhajícími sloupci v definici sloupců. Nastavení **Další mezery před sloupcem** ovlivní všechny řádky podrobností sloupce pro daný sloupec, ale nikoli řádky záhlaví sloupce. Tuto možnost použijte k oddělení skupin sloupců nebo přidání několika mezer před popis, aby byl sloupec popisu odsazený od doleva zarovnaných nadpisů v sestavě. Výchozí počet mezer mezi jednotlivými sloupci je 2. Toto nastavení lze změnit na kartě **Nastavení** v definici sestavy.

#### <a name="specify-the-space-between-columns"></a>Určení mezery mezi sloupci

1.  V Návrháři sestav otevřete definici sloupce k úpravě.
2.  V buňce **Další mezery před sloupcem** zadejte počet mezer k vložení mezi sloupce.

### <a name="specify-a-currency"></a>Určení měny

Buňka **Přepsání formátu/měny** určuje formátování desetinných míst, měny a procentuálních hodnot ve sloupci. Toto formátování přepíše jakékoli formátování určené v definici sestavy nebo výchozích hodnotách systému.

#### <a name="assign-a-format-currency-override-to-a-report-column"></a>Přiřazení přepsání formátu nebo měny ke sloupci sestavy

1.  V Návrháři sestav otevřete definici sloupce k úpravě.
2.  Klikněte dvakrát na buňku **Přepsání formátu/měny** ve sloupci s částkami.
3.  V dialogovém okně **Přepsání formátu** vyberte možnosti formátování.

### <a name="add-a-print-control-code"></a>Přidání kontrolního kódu tisku

Buňka **Řízení tisku** může obsahovat kódy, které upraví zobrazení nebo charakteristiky tisku sloupce. Existují dva typy kontrolních kódů tisku: normální kontrolní kódy tisku a podmíněné kontrolní kódy tisku.

#### <a name="regular-print-control-codes"></a>Normální kontrolní kódy tisku

| Kontrolní kód tisku | Převod                                     | Popis                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|--------------------|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| NP                 | Netisknuté                                     | Vyloučí částky v tomto sloupci ze sestavy, která bude vytištěna, a z výpočtů. Chcete-li do výpočtu zahrnout netisknutý sloupec, odkazujte na sloupec přímo ve vzorci výpočtu. Například netisknutý sloupec C je součástí následujícího výpočtu: **B+C+D**. Netisknutý sloupec C však není součástí následujícího výpočtu: **B:D**.                                                                                                                                          |
| XCR                | Změnit znaménko pokud je obvyklý zůstatek řádku typu Dal | Vytvoří rozpočtovou nebo srovnávací sestavu, kde je jakákoli nepříznivá odchylka (například nedostatek výnosů nebo překročení výdajů) vždy záporná. Použitím tohoto kódu na sloupec **CALC** obrátíte znaménko částky sloupce, pokud je typický zůstatek daného řádku typu Dal (dle určení hodnoty **C** ve sloupci **Normální zůstatek** v definici řádku). **Poznámka:** Pro řádky **TOT** a řádky **CAL**, které obvykle nesou zůstatek typu Dal, je třeba zadat hodnotu **C** do sloupce **Normální zůstatek** v definici řádku. |
| X0                 | Potlačit sloupec v případě samých nul nebo prázdných hodnot          | Vyloučí sloupec **FD** ze sestavy, pokud jsou všechny buňky ve sloupci prázdné nebo obsahují nuly.                                                                                                                                                                                                                                                                                                                                                                                                                             |
| SR                 | Potlačit zaokrouhlení                               | Zabrání zaokrouhlení částek v tomto sloupci.                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| XR                 | Potlačit shrnutí                                 | Potlačí shrnutí. Pokud sestava používá strom výkaznictví, částky v tomto sloupci nebudou shrnuty do následných nadřazených uzlů.                                                                                                                                                                                                                                                                                                                                                                                                   |
| RP                 | Opakovat sloupec na každé stránce.                      | Zopakuje určený sloupec na každé stránce sestavy. Například můžete použít kontrolní kód **RP** k zahrnutí sloupce typu **ROW**, který shromáždí kódy řádků na každé stránce.                                                                                                                                                                                                                                                                                                                                           |
| WT                 |  Zalamovat text                                      |  Pokud je text ve sloupci příliš dlouhý a nevejde se do prostoru, zalomte text tak, aby zůstal ve sloupci.                                                                                                                                                                                                                                                                                                                                                                                                                            |

#### <a name="conditional-print-control-codes"></a>Podmíněné kontrolní kódy tisku

| Podmíněný kontrolní kód tisku | popis                                                                             |
|--------------------------------|-----------------------------------------------------------------------------------------|
| (žádný)                         | Zruší výběr podmíněného tisku.                                                  |
| P&lt;B                         | Zobrazí určený sloupec pouze v případě, že je hodnota období menší než základní období.             |
| P&gt;B                         | Zobrazí určený sloupec pouze v případě, že je hodnota období větší než základní období.             |
| P=B                            | Zobrazí určený sloupec pouze v případě, že se hodnota období rovná základnímu období.              |
| P&lt;=B                        | Zobrazí určený sloupec pouze v případě, že je hodnota období menší nebo rovna základnímu období. |
| P&gt;=B                        | Zobrazí určený sloupec pouze v případě, že je hodnota období větší nebo rovna základnímu období. |

#### <a name="add-print-control-codes-to-a-report-column"></a>Přidání kontrolních kódů tisku do sloupce sestavy

1.  V Návrháři sestav otevřete definici sloupce k úpravě.
2.  Klikněte dvakrát na buňku **Řízení tisku**.
3.  V dialogovém okně **Řízení tisku** vyberte kód ze seznamu **Výběr možností řízení tisku**. Chcete-li vybrat více než jeden kód, podržte klávesu Ctrl a vyberte kódy.
4.  Vyberte možnost v poli **Podmíněné možnosti tisku**. Ve výchozím nastavení je zvolena možnost **(žádný)**. Lze vybrat pouze jeden podmíněný kód tisku současně.
5.  Klikněte na tlačítko **OK**.

> [!TIP]
> Můžete také zadat tiskové kódy přímo do buňky **Řízení tisku**. Více kontrolních kódů tisku oddělte čárkou.


## <a name="column-types"></a>Typy sloupce
Typ informací, které zahrnuje každý sloupec v sestavě, je určen hodnotou v řádku **Typ sloupce** v definici sloupce. Každá definice sloupce musí obsahovat alespoň jeden sloupec popisu (**DESC**) a jeden sloupec částky (**FD**, **WKS** nebo **CALC**). **Poznámka:** Kódy typu sloupce se nevztahují na všechny účetní systémy. Pokud jste vybrali typ, který není platný pro váš účetní systém, daný sloupec bude v sestavě prázdný.

### <a name="specify-a-column-type"></a>Určení typu sloupce

1.  V Návrháři sestav otevřete definici sloupce k úpravě.
2.  V odpovídajícím sloupci dvakrát klikněte na buňku v řádku **Typ sloupce**.
3.  V seznamu vyberte typ sloupce. Následující tabulka popisuje různé typy sloupců.
    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>Kód typu sloupce</th>
    <th>Popis</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>FD</td>
    <td>Zobrazí finanční data nebo data z listu aplikace Excel při použití sloupce <strong>Odkaz na finanční dimenze</strong> nebo sloupce <strong>Odkaz na list</strong> v definici řádku. Když vyberete typ sloupce <strong>FD</strong>, bude automaticky zadáno výchozí nastavení pro tyto řádky: <ul>
    <li><strong>Kód knihy / atribut kategorie:</strong> ACTUAL</li>
    <li><strong>Kód knihy / atribut kategorie:</strong> ACTUAL</li>
    <li><strong>Fiskální rok:</strong> BASE</li>
    <li><strong>Období:</strong> BASE</li>
    <li><strong>Pokrytá období:</strong> PERIODIC</li>
    <li><strong>Šířka sloupce:</strong> 14</li>
    </ul>
Tato výchozí nastavení lze změnit.</td>
    </tr>
    <tr class="even">
    <td>VÝPOČET</td>
    <td>Zobrazí výsledek jednoduchého nebo komplexního výpočtu, který je určen v buňce <strong>Vzorec</strong>. Další informace naleznete v tématu <a href="advanced-formatting-options-financial-reporting.md">Rozšířené možnosti formátování v návrháři sestav</a>.</td>
    </tr>
    <tr class="odd">
    <td>POPIS</td>
    <td>Zobrazí popis řádku z definice řádku. Ačkoli je sloupec popisu často prvním sloupcem v sestavě, může být na libovolné pozici.</td>
    </tr>
    <tr class="even">
    <td>ŘÁDEK</td>
    <td>Zobrazí jednotlivé kódy řádků pro finanční řádky ze sloupce <strong>Kód řádku</strong> v definici řádku. Další informace naleznete v tématu <a href="row-definitions-financial-reporting.md">Definice řádku ve finančním výkaznictví</a>.</td>
    </tr>
    <tr class="odd">
    <td>ACCT (kódy účtů)</td>
    <td>Zobrazí hodnoty segmentů nebo dimenzí finančních dat, které platí pro jednotlivé řádky. Pro sestavy podrobností o účtech a transakcích je vytištěn plně kvalifikovaný účet (například <strong>110140-070-0101</strong>). Pokud byly stanoveny rozsahy ve sloupci <strong>Odkaz na finanční dimenze</strong> v související definici řádku, bude rozsah uzavřen do hranatých závorek a bude považován za jednu hodnotu (například <strong>[110140:110700]-070-[0101:0200]</strong>). Pro finanční sestavy a sestavy vysoké úrovně, které jsou kombinací více účtů, se vytiskne odkaz na finanční data z definice řádku (například <strong>1100:1200</strong>).</td>
    </tr>
    <tr class="even">
    <td>VYPLNIT</td>
    <td>Buňku vyplňte znakem, který uzavřete do jednoduchých uvozovek. Pokud nezadáte znak, sloupec je prázdný. Chcete-li například vyplnit sloupec třemi tečkami (...), zadejte hodnotu <strong>FILL</strong> <strong>'.'</strong>.</td>
    </tr>
    <tr class="odd">
    <td>STRANA</td>
    <td>Vloží svislý konec stránky do sestavy. Sloupce, které jsou napravo od sloupce <strong>PAGE</strong> se zobrazí na další stránce.</td>
    </tr>
    <tr class="even">
    <td>WKS</td>
    <td>Zobrazí data, která pocházejí z listu aplikace Excel. Když vyberete typ sloupce <strong>WKS</strong>, bude automaticky zadáno výchozí nastavení pro tyto řádky: <ul>
    <li><strong>Fiskální rok:</strong> PERIODIC</li>
    <li><strong>Období:</strong> BASE</li>
    </ul>
Tato výchozí nastavení lze změnit.</td>
    </tr>
    <tr class="odd">
    <td>ATTR</td>
    <td>Pokud váš účetní systém podporuje atributy, zobrazí ve sloupci atribut účtu nebo transakce. Atribut, který musí platit pro jeden úplný účet, získá související informace o účtu nebo transakci z finančních dat. Atributy na úrovni účtu zobrazují data z účtu a atributy na úrovni transakce zobrazují data vzniklá v době, kdy byla transakce zaúčtována. Vyberete-li hodnotu <strong>ATTR</strong> jako typ sloupce, určete kategorii atributu v řádku podrobností <strong>Kód knihy / atribut kategorie</strong> v definici sloupce.</td>
    </tr>
    </tbody>
    </table>

### <a name="financial-dimensions-column"></a>Sloupec finančních dimenzí

Následující definic řádků **Definice sloupce** platí pro sloupce, které mají typ sloupce **FD** (částky z finančních dimenzí).

#### <a name="book-codeattribute-category-cell"></a>Buňka Kód knihy / atribut kategorie

Buňka **Kód knihy / atribut kategorie** identifikuje kód knihy pro data ve sloupci **FD**. Definice sloupce může zahrnovat více skutečných, rozpočtových a statistických sloupců. Definice sloupce může také zobrazovat různá období, například aktuální částky, částky od začátku roku nebo jiné částky. Seznam kódů knih odráží skutečné, rozpočtové a statistické (nefinanční) možnosti, které byly stanoveny ve vašich finančních datech.

#### <a name="fiscal-year-cell"></a>Buňka Fiskální rok

Buňka **Fiskální rok** identifikuje fiskální rok, který má sloupec zahrnovat. Rok může být relativní vůči základnímu roku, které se stanoví během generování sestavy. Existují tyto možnosti.

| Možnost  | Popis                                                                                                                  |
|---------|------------------------------------------------------------------------------------------------------------------------------|
| ZÁKLAD    | Použije základní rok, který je zadán v době vytvoření sestavy.                                                                          |
| BASE+\# | Použije rok, který následuje \# let po základním roku. Například pro použití třetího roku po základním roku zadejte hodnotu **BASE+3**. |
| BASE-\# | Použije rok, který uplynul \# let před základním rokem. Chcete-li například použít předchozí rok, zadejte hodnotu **BASE-1**.                 |
| \#      | Zadá aktuální fiskální rok.                                                                                                |

#### <a name="period-cell"></a>Buňka Období

Buňka **Období** identifikuje fiskální období, která má sloupec zahrnovat. Období může být relativní vzhledem k základnímu období, které se stanoví během generování sestavy. Existují tyto možnosti.

| Parametr          | popis                                                                                                                                                                                                                          |
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ZÁKLAD            | Použije základní období.                                                                                                                                                                                                                 |
| BASE+\#         | Použije období, které následuje \# období po základním období. Například pro použití třetího období po základním období zadejte hodnotu **BASE+3**.                                                                                               |
| BASE-\#         | Použije období, které uplynulo \# období před základním obdobím. Chcete-li například použít předchozí období, zadejte hodnotu **BASE-1**.                                                                                                                 |
| BASE-\#:BASE    | Použije více období, od několika období před základním obdobím až po základní období. Například pro použití tři předchozích období a základního období zadejte hodnotu **BASE-3:BASE**.                                                |
| BASE:BASE+\#    | Použije více období, od základního období až po několik období po základním období. Například pro použití základního období a dvou následujících období zadejte hodnotu **BASE:BASE+2**.                                                  |
| BASE-\#:BASE+\# | Použije více období, od několika období před základním obdobím až po několik období po základním období. Například pro použití tři předchozích období, základního období a dvou následujících období zadejte hodnotu **BASE-3:BASE+2**. |
| 1:ZÁKLAD          | Použije více období, od prvního období až po základní období.                                                                                                                                                                 |
| \#              | Vždy použije konkrétní číslo období. Nedoporučujeme používat tuto možnost, protože snižuje flexibilitu definice sloupce.                                                                                       |
| \#                                      : \#           | Vždy použije konkrétní rozsah období. Nedoporučujeme používat tuto možnost, protože snižuje flexibilitu definice sloupce.                                                                                    |

Můžete jít za hranice fiskálního roku v kterémkoli určení období a můžete kombinovat roky v rozmezí období. Například zadejte jako období hodnotu **BASE-5** (představující posledních šest období) a spusťte sestavu, která má základní období 2. V takovém případě tato sestava obsahuje data pro první dvě období zadaného fiskálního roku a poslední čtyři období předchozího fiskálního roku.

### <a name="specify-the-periods-for-an-fd-column"></a>Určení období pro sloupec FD

1.  V Návrháři sestav otevřete definici sloupce k úpravě.
2.  Ve sloupci **FD** klikněte dvakrát na buňku v řádku **Období** a potom vyberte možnost v seznamu.
3.  Na řádku vzorce nad navigačním podoknem nebo v buňce **Období** zadejte vzorec. Nahraďte jakýkoli znak křížku (\#) odpovídající hodnotou.

#### <a name="periods-covered-cell"></a>Buňka Pokrytá období

Buňka **Pokrytá období** identifikuje částku, kterou má sloupec zobrazit. Tato částka je relativní vůči hodnotě v buňkách **Fiskální rok** a **Období** pro sloupec. Existují tyto možnosti.

| Možnost      | Popis                                                                 |
|-------------|-----------------------------------------------------------------------------|
| PERIODICKÝ    | Zobrazí součet aktivity pro aktuální období nebo rozsah období. |
| PERIODICKÝ/BB | Zobrazí počáteční zůstatek pro aktuální období nebo rozsah období.   |
| Od začátku roku         | Zobrazí součet aktivity od začátku roku.                               |
| OD POČÁTKU ROKU/BB      | Zobrazí počáteční zůstatek pro rok.                                 |

### <a name="specify-the-periods-that-are-covered-for-an-fd-column"></a>Určení období, která jsou pokryta pro sloupec FD

1.  V Návrháři sestav otevřete definici sloupce k úpravě.
2.  Ve sloupci **FD** klikněte dvakrát na buňku v řádku **Pokrytá období** a potom vyberte možnost v seznamu.

### <a name="attribute-filter-in-a-column-definition"></a>Filtr atributů v definici sloupce

Atributy jsou hodnoty finančních dat, které dále definují účet nebo transakci. Atributy účtu zahrnují položky **Majetek**, **Závazky**, **Výnosy** a **Výdaje**. Atributy transakce zahrnují položky **Popis transakce** a **Datum použití transakce**. Podpora atributů se může lišit mezi systémy Microsoft Dynamics ERP. Buňka **Filtr atributů** omezuje data ve sloupcích **FD** na konkrétní hodnoty nebo rozsahy pro kategorie atributů. Ačkoli lze tuto funkci použít spolu se sloupcem **ATTR**, sloupec **ATTR** není požadován. Ve sloupci **FD** existuje limit účtů nebo transakcí, které bude sestava obsahovat z filtru atributů. **Poznámka:** Atributy, které váš systém ERP podporuje, najdete v průvodci integrace pro váš systému.

#### <a name="apply-an-attribute-filter-for-an-fd-column-on-a-report"></a>Použití filtr atributů pro sloupec FD v sestavě

1.  V Návrháři sestav otevřete definici sloupce k úpravě.
2.  Klikněte dvakrát na buňku **Filtr atributů** pro sloupec **FD**.
3.  V dialogovém okně **Filtr atributů** klikněte dvakrát na buňku ve sloupci **Atribut** a poté vyberte typ filtru.
4.  Chcete-li výsledky dále omezit, zadejte rozsah do sloupců **Od** a **Do**. Buňka **Od** musí obsahovat hodnotu.
5.  Klepněte na tlačítko **OK**.

#### <a name="example-of-an-attribute-filter"></a>Příklad filtru atributů

Následující příklad ukazuje část popisu sloupce, který má atribut účtu v řádku **Kód knihy / atribut kategorie**. Filtr atributů pro tento sloupec určuje rozsah hodnot, které mají být zahrnuty do sestavy.

|                              | O    | mld.                    |
|------------------------------|------|----------------------|
| Typ sloupce                  | POPIS | FD                   |
| Kód knihy / atribut kategorie |      | SKUTEČNÝ               |
| Fiskální rok                  |      | ZÁKLAD                 |
| Období                       |      | 1:ZÁKLAD               |
| Pokrytá období              |      | PERIODICKÝ             |
| ...                          |      |                      |
| Šířka sloupce                 | 30   |                      |
| ...                          |      |                      |
| Filtr atributů             |      |  Odkaz=\[01:10\] |

### <a name="dimension-filter-in-a-column-definition"></a>Filtr dimenzí v definici sloupce

Filtr dimenzí slouží k omezení sloupce **FD** na konkrétní hodnoty dimenzí. Filtr může zahrnovat jednu dimenzi, rozsah dimenzí nebo skupinu dimenzí. Filtr může také obsahovat sady hodnot dimenzí. Vzhledem k tomu, že se mohou hodnoty dimenzí lišit, nemusí ..\finanční dimenze\systém založený na dimenzích odpovídat přesné délce. Filtr se použije bez ohledu na to, zda sestava obsahuje strom výkaznictví, či nikoli. Můžete použít zástupné znaky (\* nebo ?) na jakékoli pozici. Když zadáte více účtů, vložte mezi účty čárku, jak je uvedeno v následujícím příkladu: +Částka=\[1200\], +Částka=\[1100\], Oddělení=\[01?\] Abyste získali všechna oddělení pro konkrétní účet,můžete vyloučit dimenzi oddělení z filtru dimenzí. Například oba následující filtry dimenzí jsou zpracovány stejným způsobem:

-   +Účet=\[1100\],Oddělení
-   +Účet=\[1100\]

Můžete také použít jakoukoli kombinaci alfanumerických znaků pro přesnou shodu a můžete definovat částečné dimenze. Například hodnota **Umístění = \[10\*\]** zahrnuje všechny hodnoty dimenze umístění začínající na 10.

#### <a name="apply-a-dimension-filter-for-a-column-on-a-report"></a>Použití filtru dimenzí pro sloupec v sestavě

1.  V Návrháři sestav otevřete definici sloupce k úpravě.
2.  Klikněte dvakrát na buňku **Filtr dimenzí** pro sloupec **FD**.
3.  V dialogovém okně **Dimenze** zadejte filtry, které chcete použít.
4.  Klepněte na tlačítko **OK**.

### <a name="format-a-multiple-currency-report-in-a-column-definition"></a>Formátování sestavy s více měnami v definici sloupce

Sestava s více měnami může zobrazit částky v přirozené (místní) měně, funkční (výchozí) měně nebo měně vykazování. Funkční měna společnosti je definována v systému Microsoft Dynamics ERP. Nepleťte si toto nastavení systému ERP s možnostmi místního nastavení operačního systému, kde lze konfigurovat symboly výchozí měny, které se používají v sestavách. Následující buňky související s měnou jsou k dispozici v definici sloupce:

-   **Zobrazení měny** – určuje typ měny (přirozená, funkční nebo vykazovací) ve které se transakce zobrazí. Tato funkce je někdy označována jako převod měny. Převod měny je možnost vykazovat částky hlavní knihy v měně, která nemusí být funkční měnou společnosti nebo měnou, ve které byla zadána transakce.
-   **Filtr měny** – definuje filtr měny. V sestavě jsou zobrazeny pouze transakce, které byly zadány ve vybrané měně.

> [!NOTE]
> Abyste mohli vytvářet sestavy, které používají více měn, je nutné zaškrtnout políčko **Zahrnout všechny měny vykazování** na kartě **Sestava**. Abyste určili funkční měnu společnosti, postupujte následovně.

1.  V Návrháři sestav v nabídce **Společnost** klikněte na položku **Společnosti**.
2.  V dialogovém okně **Společnosti** vyberte společnost a klikněte na tlačítko **Zobrazení**.
3.  V dialogovém okně **Zobrazit společnost** v části **Možnosti místního nastavení** můžete zobrazit měnu, která je definovaná pro vybranou společnost.

#### <a name="specify-the-currency-on-a-multiple-currency-report"></a>Určení měny v sestavě s více měnami

1.  V Návrháři sestav otevřete definici sloupce k úpravě.
2.  Klikněte dvakrát na buňku **Zobrazení měny** v odpovídajícím sloupci **FD** a poté vyberte možnost zobrazení informací o měně: **Přirozená/původní měna**, **Funkční měna z informací o společnosti** nebo měna vykazování.
3.  Klikněte dvakrát na buňku **Filtr měny** v odpovídajícím sloupci **FD** a poté vyberte odpovídající kód měny v seznamu. V sestavě jsou zobrazeny pouze transakce, které byly zadány v této měně.

> [!NOTE]
> Možnosti zde popsané se mohou lišit v závislosti na systému ERP. Další informace naleznete v [dokumentaci systému Microsoft ERP](https://www.microsoft.com/en-us/download/details.aspx?id=5916).

### <a name="example-for-currency-display-and-currency-filter-cells"></a>Příklad pro buňky Zobrazení měny a Filtr měny

Pavla provedla tyto volby měny ve své definici sloupce:

-   **Filtr měny:** Jen
-   **Zobrazení měny:** Funkční (USD)

Kvůli filtru měny, který Pavla vybrala, obsahuje sestava pouze transakce, které byly zadány v japonském jenu (JPY). Kvůli zobrazení měny, které zvolila, zobrazí sestava tyto transakce ve funkční měně, amerických dolarech (USD).

#### <a name="currency-filter-and-currency-display-combinations"></a>Kombinace filtru měny a zobrazení měny

Následující tabulka obsahuje výsledky sestavy, které mohou nastat pro různé kombinace možností v buňkách **Zobrazení měny** a **Filtr měny** z důvodu voleb, které Pavla učinila. Funkční měna je USD.

| Buňka Zobrazení měny                        | Buňka Filtr měny | Výsledek sestavy                                                                                                                                                                                    |
|----------------------------------------------|----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Přirozená/původní měna                 | **JEN**              | **6 000 Y** – výsledek ukazuje pouze transakce, které byly zadány v měně JPY.                                                                                                                        |
| Funkční měna z informací o společnosti | **JEN**              | **60 $** – výsledek zobrazí pouze transakce, které byly zadány v měně JPY, a tyto transakce zobrazí v měně USD. **Poznámka:** Směnný kurz je přibližně 100 JPY na USD.                    |
| Funkční měna z informací o společnosti | Prázdné                | **$2,310\*\*** – výsledek zobrazí všechna data ve funkční měně, která je určena v informacích o společnosti. **Poznámka:** Tato částka je součtem všech transakcí ve funkční měně. |
| Přirozená/původní měna                 | Prázdné                | **2 250 $** – výsledek obsahuje všechny částky v měně, ve které byla provedena transakce.                                                                                                 |

### <a name="calculation-column-in-a-column-definition"></a>Sloupec výpočtu v definici sloupce

Typ sloupce **CALC** v definici sloupce podporuje složité výpočty v buňce **Vzorec** a může obsahovat operátory **+**, **-**, **\*** a **/**, a také výrazy **IF/THEN/ELSE**. Sloupec výpočtu může také odkazovat na libovolný sloupec, dokonce i následující sloupce. Navíc může sloupec výpočtů zahrnovat také fiskální rok a období k podpoře záhlaví sloupce. Vzorec výpočtu může obsahovat až 1 024 znaků. Chcete-li vyjádřit výsledky výpočtu jako procentuální hodnotu, použijte přepsání zvláštního formátu. **Poznámka:** výsledky vzorců pro výpočet nezahrnují hodnoty do netisknutých rozsahů sloupců. Například hodnota **A:D** vytiskne hodnotu **0** (nula), zatímco hodnota **A+B+C** pro netisknuté hodnoty vypočítá hodnotu.

#### <a name="operators-in-calculation-columns"></a>Operátory ve sloupcích výpočtů

Chcete-li přičíst, odečíst, násobit, nebo dělit sloupce, zadejte písmena sloupců v pořadí výpočtu a potom použijte odpovídající operátor k oddělení jednotlivých písmen sloupců. Následující tabulka vysvětluje operátory, které lze použít ve sloupci výpočtu.

| Operátor | Příklad výpočtu | popis                                                                                                                                                                                                                                    |
|----------|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| +        | A+C                 | Přičte částku ve sloupci A k částce ve sloupci C.                                                                                                                                                                                          |
| :        | A:C A:C-D           | Sečte rozsah po sobě následujících sloupců. Například vzorec **A:C** sečte součty sloupců od A do C a vzorec **A:C-D** sečte součty sloupců od A do C a potom odečte částku ve sloupci D.                          |
| -        | A-C                 | Odečte částku ve sloupci A od částky ve sloupci C. **Poznámka:** Znaménko minus (-) také slouží k obrácení znamének ve sloupci. Například můžete použít vzorec **-A+B** k přičtení obrácené hodnoty částky ve sloupci A k částce ve sloupci B. |
| \*       | A\*C                | Vynásobí částku ve sloupci A částkou ve sloupci C.                                                                                                                                                                                     |
| /        | A/C                 | Vydělí částku ve sloupci A částkou ve sloupci C.                                                                                                                                                                                       |

#### <a name="use-a-calculation-formula-in-a-column-definition"></a>Použije vzorec výpočtu v definici sloupce

1.  V Návrháři sestav otevřete definici sloupce k úpravě.
2.  V příslušném sloupci **CALC** zadejte vzorec do buňky **Vzorec**.

#### <a name="complex-calculations"></a>Složité výpočty

Složitý výpočet může obsahovat jakoukoli kombinaci odkazů na buňky, operátorů, hodnot a úrovní vnořených závorek. Vypočítat k výpočtu průměru ze sloupců A a B použijte výpočetní vzorec **((A+B)/2)**.

#### <a name="specify-report-cells-in-a-column-calculation"></a>Určení buněk sestavy ve výpočtu sloupce

Můžete odkazovat na konkrétní buňku sestavy zadáním písmene sloupce a kódu řádku. Například **B.100** odkazuje na kód řádku 100 ve sloupci B. Můžete vydělit celý sloupec konkrétní hodnotou buňky sestavy, která se nachází ve stejném sloupci. Například výpočet **B/B.100** znamená, že částka ve sloupci B má být vydělena hodnotou v řádku s kódem 100 ve sloupci B. Odkazuje-li výpočet na sloupec, který závisí na jiném sloupci, je nejprve vyřešen závislý sloupec. Pokud sloupec odkazujete na jiný sloupec, který se odkazuje zpět na první sloupec, způsobíte chybu cyklického odkazu. **Poznámka:** Výpočet může být nesprávný, pokud změníte prioritu výpočtu pro sestavu. Prioritu pro výpočet lze nastavit na kartě **Nastavení** v definici sestavy.

#### <a name="multiply-or-divide-a-column-by-a-base-row"></a>Násobení nebo dělení sloupce základním řádkem

Můžete vytvořit sloupec zobrazující všechny hodnoty ve určeném sloupci jako procento základního čísla. Proto je možné zobrazit vztahy mezi řádky, například procento řádku prodeje nebo procento řádku celkových výdajů. Chcete-li násobit nebo dělit každý řádek v konkrétním sloupci základním řádkem, zadejte sloupec k použití při výpočtu a potom zadejte hodnotu **\*BASEROW** nebo **/BASEROW**. Zadejte například vzorec **C\*BASEROW** nebo **C/BASEROW**. **Poznámka:** Když použijete výpočet základního řádku v definici sloupce, ujistěte se, že každá definice řádku použitá s touto definicí sloupce obsahuje alespoň jeden základní řádek pro výpočty.

#### <a name="divide-the-amount-in-a-column-by-the-number-of-periods"></a>Vydělení částky ve sloupci počtem období

Částku ve sloupci můžete vydělit určený počtem období. Například vzorec **B/Období** vydělí hodnotu ve sloupci B počtem období ve sloupci B. Pokud výpočet pokrývá více sloupců, zadejte počet období, který má být použit ve výpočtu. Například vzorec **(B+C)/Období** sečte částky ve sloupcích B a C a potom výslednou hodnotu vydělí hodnotou období.

<a name="see-also"></a>Viz také
--------

[Definice řádku ve finančním výkaznictví](row-definitions-financial-reporting.md)

[Rozšířené možnosti formátování ve finančním výkaznictví](advanced-formatting-options-financial-reporting.md)




