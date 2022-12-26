---
title: Možnosti mřížky
description: Tento článek popisuje několik výkonných funkcí ovládacího prvku mřížky. Chcete-li mít přístup k těmto funkcím, je nutné povolit novou funkci mřížky.
author: jasongre
ms.date: 08/29/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard
audience: Application User, Developer, IT Pro
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2020-02-29
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 6d14bba13dbf701a8c27c10ac2d318b071092bc1
ms.sourcegitcommit: 77ffeccffff28fbb6ff576864d7abddd412cdab6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/15/2022
ms.locfileid: "9852366"
---
# <a name="grid-capabilities"></a>Možnosti mřížky

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Nový ovládací prvek mřížky poskytuje několik užitečných a výkonných funkcí, které lze použít k vylepšení produktivity uživatelů, vytvoření zajímavějších zobrazení dat a získání smysluplných přehledů dat. Tento článek se týká následujících možností: 

- Zobrazení vypočtených hodnot 
- Zadávání před systémem
- Vyhodnocování matematických výrazů 
- Seskupení tabulkových dat (povoleno samostatně pomocí funkce **Seskupení do mřížek**)
- Zmrazení sloupců (povoleno samostatně pomocí funkce **Zmrazení sloupců v mřížkách**)
- Automaticky přizpůsobit šířku sloupce
- Roztažitelné sloupce

## <a name="showing-calculated-values"></a>Zobrazení vypočtených hodnot
Ve finančních a provozních aplikacích mohou uživatelé zobrazit vypočítanou hodnotu pro každý číselný sloupec v mřížce. Tyto vypočítané hodnoty se zobrazí v části zápatí v dolní části mřížky.

[![Zobrazení vypočtených hodnot v mřížkách.](./media/grids-aggregation.png)](./media/grids-aggregation.png)

Ve verzích před 10.0.29 je součet jedinou podporovanou vypočítanou hodnotou. Nicméně od verze 10.0.29 po aktivaci funkce **Rozšířené možnosti agregace mřížky** si uživatelé mohou vybrat z následujících čtyř vypočtených hodnot:

- Minimum
- Maximum
- Celkem
- Průměr

Jeden sloupec může zobrazovat pouze jeden typ vypočítané hodnoty. Každý sloupec v mřížce však lze nakonfigurovat tak, aby zobrazoval jiný typ vypočítané hodnoty.

### <a name="showing-the-grid-footer"></a>Zobrazení zápatí mřížky
Finanční a provozní aplikace obsahují oblast zápatí v dolní části každé tabulkové mřížky. V zápatí je možné zobrazit cenné informace související s daty, která se zobrazí v mřížce. Následuje několik příkladů těchto informací:

- Počet vybraných řádků v tabulce (při výběru více než jednoho záznamu)
- Vypočítané hodnoty v dolní části konfigurovaných číselných sloupců (například celkové součty)
- Počet řádků v sadě dat 

Toto zápatí je ve výchozím nastavení skryto, ale lze je zapnout. Chcete-li zobrazit zápatí pro mřížku, vyberte tlačítko **Možnost mřížky** v záhlaví mřížky a vyberte možnost **Zobrazit zápatí**. Po zapnutí zápatí pro konkrétní mřížku bude toto nastavení zapamatováno, dokud se uživatel nerozhodne zápatí skrýt. Chcete-li zápatí skrýt, vyberte **Skrýt zápatí** v nabídce **Možnosti mřížky**.

### <a name="specifying-columns-with-calculated-values"></a>Určení sloupců s vypočítanými hodnotami
V současné době ve výchozím nastavení žádné sloupce nezobrazují vypočítané hodnoty. Namísto toho je nastavení považováno za jednorázové, podobně jako nastavení šířky sloupců v mřížce. Jakmile určíte, že chcete zobrazit vypočítanou hodnotu pro sloupec, toto nastavení se při další návštěvě stránky zapamatuje.

Existují dva způsoby konfigurace sloupce pro zobrazení vypočítané hodnoty:

- Vyberte a podržte (nebo klikněte pravým tlačítkem) ve sloupci, pro který chcete zobrazit vypočítanou hodnotu. Pokud je aktivní funkce **Rozšířené možnosti agregace mřížky** je povolena, vyberte **Zobrazit součty sloupců** a poté vyberte požadovanou vypočítanou hodnotu. Pokud tato funkce není povolena, vyberte **Součet tohoto sloupce**. Tato akce způsobí provedení tří událostí:

    1. Zobrazí se zápatí mřížky. 
    2. Vaše preference pro zobrazení vypočítané hodnoty pro sloupec se uloží. 
    3. Tato akce zahájí požadovaný výpočet pro sloupec a všechny dříve konfigurované, pro zobrazení vypočítané hodnoty. Čas potřebný k zobrazení vypočítaných hodnot závisí na velikosti sady dat.

- Po zobrazení zápatí vyberte **Zobrazit součet** (nebo **Vybrat vypočítanou hodnotu**, pokud je aktivní funkce **Rozšířené možnosti agregace mřížky**) v oblasti zápatí v dolní části sloupce, pro který chcete zobrazit vypočítanou hodnotu. Pokud neexistují žádné konfigurované sloupce, toto tlačítko bude k dispozici v zápatí všech číselných sloupců.

    Poté, co je alespoň jeden sloupec nakonfigurován tak, aby zobrazoval vypočítanou hodnotu, tlačítko **Zobrazit součet** (nebo **Vybrat vypočítanou hodnotu**) bude dostupné pouze při umístění kurzoru nebo zaměření. Akce vybírání tlačítka pouze ukládá vaši předvolbu pro zobrazení vypočítané hodnoty ve sloupci, takže přednost bude uplatněna během příštích návštěv na stránce. V zápatí je tento stav označen pomlčkou, která se zobrazí ve sloupci. (Všimněte si, že vypočítaná hodnota se zobrazí okamžitě, pokud je datová sada dostatečně malá.)

Pokud uděláte chybu a již nechcete zobrazit vypočítanou hodnotu v konkrétním sloupci, vyberte a podržte (nebo klikněte pravým tlačítkem) ve sloupci a poté vyberte **Skrýt součet** (nebo **Zobrazit součty sloupců \> Žádný**, pokud je aktivní funkce **Rozšířené možnosti agregace mřížky**). Případně vyberte **Skrýt součet** (nebo **Skrýt vypočítanou hodnotu**) v zápatí v tomto sloupci. Tato preference bude také uložena pro budoucí návštěvy na stránce. 

### <a name="calculating-aggregate-values"></a>Výpočet souhrnných hodnot
Když přejdete na stránku, kde je viditelné zápatí a sloupce jsou již nakonfigurovány tak, aby zobrazovaly vypočítané hodnoty, nemusí se tyto hodnoty v zápatí zobrazit. Chování je závislé na velikosti datové sady na stránce. Pokud je datová sada dostatečně malá, vypočítané hodnoty se zobrazí automaticky spolu s počtem řádků v sadě dat. Pokud v zápatí existují pomlčky pod sloupci, které jste nakonfigurovali pro součty, je sada dat příliš velká, aby systém mohl zobrazit vypočtené hodnoty okamžitě. V tomto případě je pro výpočet hodnot vyžadována explicitní akce. Chcete-li vypočítat hodnoty, vyberte tlačítko **Vypočítat** v patičce. Alternativně vyberte a podržte (nebo klikněte pravým tlačítkem) ve sloupci, pro který chcete zobrazit součet, a poté vyberte **Součet tohoto sloupce** (nebo **Zobrazit součty sloupců** a poté požadovanou vypočtenou hodnotu, pokud je aktivní funkce **Rozšířené možnosti agregace mřížky**).

Pokud výpočet trvá příliš dlouho, můžete operaci kdykoli zrušit kliknutím na tlačítko **Zrušit**. Někdy bude datová sada příliš velká na výpočet agregovaných hodnot (omezení stanovené vaší organizací). V takovém případě budete místo toho upozorněni, abyste svá data více filtrovali.

> [!NOTE]
> Správci systému mohou upravit limit počtu záznamů dostupných pro výpočet agregátů úpravou parametru **Maximální počet místních záznamů pro každou mřížku** na stránce **Možnosti výkonu klienta**. Výchozí hodnota je 25 000 záznamů. Správci by měli být při úpravě této hodnoty opatrní, protože příliš velká hodnota může vyčerpat dostupnou paměť v počítači uživatele. Doporučujeme nepřekračovat 50 000 záznamů.

Vypočítané hodnoty se aktualizují automaticky při aktualizaci, odstranění nebo vytvoření řádků v sadě dat.

## <a name="typing-ahead-of-the-system"></a>Zadávání před systémem
V mnoha obchodních situacích je schopnost rychlého zadávání dat do systému velmi důležitá. Než byl zaveden nový ovládací prvek mřížky, uživatelé mohli měnit data pouze v aktuálním řádku. Proto poté, co provedli změny v řádku, uživatelé nemohli přepnout na jiný řádek nebo vytvořit nový řádek, dokud systém úspěšně neověřil změny v aktuálním řádku a (v případě vytvoření řádku) nespustil veškerou logiku, která je přidružena k vytvoření nového řádku. Ve snaze o zkrácení doby, kdy uživatelé čekají na provedení těchto operací, a za účelem zvýšení produktivity uživatelů nová mřížka tyto akce upravuje, takže jsou asynchronní. Uživatelé mohou vytvářet nové řádky nebo se přesouvat do jiných řádků a provádět změny, zatímco logika vytváření řádku čekají na vyřízení. 

[![Zadávání před systémem.](./media/gridFastEntry-07-25-2022.gif)](./media/gridFastEntry-07-25-2022.gif)

Kvůli tomuto novému chování byl do levé části sloupce výběru řádku přidán nový sloupec se stavem řádku, pokud je mřížka v režimu úprav. Tento sloupec uvádí jeden z následujících stavů:

- **Prázdné** – žádný stavový obrázek označuje, že byl řádek úspěšně uložen systémem.
- **Čekání na zpracování** – tento stav znamená, že změny v řádku dosud nebyly uloženy serverem, ale jsou ve frontě změn, které je nutné zpracovat. Před provedením akce mimo mřížku je nutné počkat na zpracování všech čekajících změn. Dále je text v těchto řádcích kurzívou, aby označoval neuložený stav řádků. 
- **Neplatný stav** - Tento stav označuje, že během zpracování řádku bylo spuštěno nějaké varování nebo zpráva, a mohlo to zabránit systému v uložení změn v tomto řádku. Ve staré mřížce, pokud se uložení nezdařilo, jste byli nuceni navrátit se do řádku a okamžitě problémy opravit. V nové mřížce se však zobrazí upozornění, že došlo k potížím s ověřením, ale můžete se rozhodnout, kdy chcete opravit problémy v řádku. Až budete připraveni problém vyřešit, můžete vrátit fokus ručně do řádku. Alternativně můžete vybrat akci **Opravit tento problém**. Tato akce okamžitě přesune fokus zpět do řádku s problémem a umožní vám provádět úpravy uvnitř nebo vně mřížky. Všimněte si, že zpracování následných čekajících řádků je zastaveno, dokud nebude toto upozornění na ověření vyřešeno. 
- **Pozastaveno** – tento stav znamená, že zpracování bylo pozastaveno, protože ověření řádku aktivovalo překryvné dialogové okno, které vyžaduje vstup uživatele. Vzhledem k tomu, že uživatel může zadávat data v některém jiném řádku, místní dialogové okno se tomuto uživateli nezobrazí okamžitě. Namísto toho se zobrazí v případě, že uživatel zvolí obnovení zpracování. Tento stav je doprovázen oznámením, které uživatele informuje o situaci. Oznámení zahrnuje akci **Obnovit zpracování**, která aktivuje místní dialogové okno.

### <a name="differences-when-entering-data-ahead-of-the-system"></a>Rozdíly při zadávání dat před systémem
Když zadáte data před místem, kde je systém zpracovává, můžete očekávat několik změn v prostředí zadávání dat:

- Všimnete si, že zde nejsou žádné vyhledávací rozevírací seznamy, hodnoty polí nejsou ověřeny po přesunutí do jiného sloupce ve stejném řádku a sloupce zpočátku nezobrazují výchozí hodnoty. K tomuto chování dochází při vytváření nebo aktualizaci před systémem. Jakmile však systém dohoní místo, kde právě upravujete, obnoví se standardní prostředí. Pokud jste provedli změny v poli, které obvykle přijímá výchozí hodnotu, vaše změny přepíší výchozí hodnotu pole, když server začne řádek zpracovávat.
- Pokud vytvoříte nový řádek pomocí klávesy **Šipka dolů**, všechny sloupce v mřížce se zobrazí jako upravitelné. Ve výchozím nastavení bude fokus umístěn do prvního sloupce v novém řádku. Tento sloupec nemusí být stejný sloupec, který získal počáteční fokus ve starší mřížce, nebo stejný sloupec, který přijme fokus po výběru tlačítka **Nový**. Vaše organizace může přizpůsobit systém a změnit sloupec, který obdrží počáteční fokus, když je vybrána klávesa **Šipka dolů**. Více informací naleznete v části [Určení sloupce, který obdrží počáteční fokus při vytváření nových řádků pomocí klávesy šipka dolů](#developer-specifying-the-column-that-receives-the-initial-focus-when-new-rows-are-created-by-using-the-down-arrow-key). Bez ohledu na to můžete použít personalizaci k optimalizaci každé mřížky pro zadávání dat. Konkrétně můžete změnit pořadí polí tak, aby první sloupec byl sloupec, do kterého chcete začít zadávat data. Můžete také chtít změnit pořadí polí obecně pro zadávání dat, snížit počet zarážek tabulátoru a skrýt všechna pole, která nejsou pro zadávání dat v tomto konkrétním zobrazení vyžadována.

### <a name="pasting-from-excel"></a>Vkládání z aplikace Excel
Uživatelé vždy mohou exportovat data z mřížek v finančních a provozních aplikacích do aplikace Microsoft Excel pomocí mechanismu **Exportu do aplikace Excel**. Nicméně možnost zadávání dat před systémem umožňuje, aby nová mřížka podporovala kopírování tabulek z aplikace Excel a jejich vložení přímo do mřížek v finančních a provozních aplikacích. Buňka mřížky, z níž je zahájena operace vložení, určuje, kde bude zkopírovaná tabulka vložena. Obsah mřížky je přepsán obsahem zkopírované tabulky s výjimkou dvou případů:

- Pokud počet sloupců ve zkopírované tabulce překračuje počet sloupců, které zůstanou v mřížce, počínaje místem vložení, uživatel bude upozorněn, že nadbytečné sloupce byly ignorovány. 
- Pokud počet řádků ve zkopírované tabulce překračuje počet řádků v mřížce, počínaje místem vložení, budou existující buňky přepsány vloženým obsahem a všechny další řádky z kopírované tabulky budou vloženy jako nové řádky v dolní části mřížky. 

## <a name="evaluating-math-expressions"></a>Vyhodnocování matematických výrazů
Jedná se o prostředek pro zvýšení produktivity, uživatelé mohou zadávat matematické vzorce do číselných buněk v mřížce. Není nutné provádět výpočet v aplikaci mimo systém. Zadáte-li například hodnotu **=15\*4** a poté se stisknutím klávesy **Tab** přesunete mimo pole, systém vyhodnotí výraz a do pole zapíše hodnotu **60**.

[![Vyhodnocování matematických výrazů.](./media/gridMathExpression-07-25-2022.gif)](./media/gridMathExpression-07-25-2022.gif)

Chcete-li, aby systém rozpoznal hodnotu jako výraz, zahajte tuto hodnotu znaménkem rovná se (**=**). Další informace o podporovaných operátorech a syntaxi naleznete v tématu [Podporované matematické symboly](http://bugwheels94.github.io/math-expression-evaluator/#supported-maths-symbols).

Od verze 10.0.29 byla rozšířena schopnost vyhodnocovat matematické výrazy v numerických ovládacích prvcích a je nyní dostupná i mimo mřížku.

## <a name="grouping-tabular-data"></a>Seskupení tabulkových dat
Obchodní uživatelé často potřebují provádět ad hoc analýzu dat. I když lze tuto analýzu provést exportem dat do aplikace Microsoft Excel a použitím kontingenčních tabulek, funkce (Preview) **Seskupení do mřížek**, která je závislá na nové funkci řízení mřížky, umožňuje uživatelům organizovat tabulková data v rámci finančních a provozních aplikací. Protože tato funkce rozšiřuje funkci **Vypočítané hodnoty**, **seskupení** umožňuje získat smysluplné přehledy o datech poskytnutím vypočtených hodnot (například mezisoučtů) na úrovni skupiny.

[![Seskupování dat v mřížce.](./media/grids-groupingWithTotals.png)](./media/grids-groupingWithTotals.png)

Chcete-li použít tuto funkci, klikněte pravým tlačítkem na sloupec, podle kterého chcete provést seskupení, a zvolte **Seskupit tento sloupec**. Tato akce seřadí data podle vybraného sloupce, přidá nový sloupec **Seskupit podle** na začátek mřížky a vloží „řádky záhlaví“ na začátek každé skupiny. Tyto řádky záhlaví obsahují následující informace o každé skupině:

- Hodnota dat pro skupinu 
- Název sloupce (tyto informace budou obzvlášť užitečné, když máte více úrovní seskupení)
- Počet datových řádků v této skupině
- Vypočítané hodnoty pro libovolný nakonfigurovaný sloupec (například mezisoučty, pokud je sloupec nakonfigurován tak, aby zobrazoval součet)

Pokud je povolena funkce [Uložená zobrazení](saved-views.md), můžete uložit seskupení jako součást zobrazení na stránkách, které umožňují ukládání dotazů do zobrazení. Například u těch s voliči velkých zobrazení. Další informace naleznete v části [Přepínání mezi zobrazeními](saved-views.md#switching-between-views). 

### <a name="multiple-levels-of-grouping"></a>Více úrovní seskupení
Poté, co seskupíte data podle jednoho sloupce, můžete data seskupit podle jiného sloupce výběrem možnosti **Seskupit podle tohoto sloupce** na požadovaném sloupci. Tento proces lze opakovat, dokud nemáte 5 vnořených úrovní seskupení, což je maximální podporovaná hloubka. V tomto okamžiku již nebudete moci seskupovat podle dalších sloupců.

Seskupení podle libovolného sloupce můžete kdykoli odebrat kliknutím pravým tlačítkem na daný sloupec a výběrem příkazu **Zrušit seskupení**. Seskupení můžete také odebrat ze všech sloupců výběrem **Možností mřížky** a následně příkazu **Oddělit vše**.

### <a name="sorting-grouped-data"></a>Řazení seskupených dat
Po seskupení dat podle jednoho nebo více sloupců můžete změnit směr řazení pro kterýkoli sloupec seskupení pomocí odpovídajícího záhlaví sloupce. 

Pokud řadíte podle neseskupeného sloupce, seskupení zůstane nedotčeno. Data jsou seřazena uvnitř každé skupiny na základě vybraného sloupce.

### <a name="expanding-and-collapsing-groups"></a>Rozbalení a sbalení skupin
V počátečním seskupení dat budou všechny skupiny rozbaleny. Můžete vytvořit souhrnná zobrazení dat sbalením jednotlivých skupin, nebo si můžete rozbalením a sbalením skupiny usnadnit navigaci v datech. Chcete-li skupinu rozbalit nebo sbalit, vyberte tlačítko se znakem > v příslušném řádku záhlaví skupiny. Všimněte si, že stav rozbalení/sbalení jednotlivých skupin **není** uložen v individuálním nastavení.

### <a name="selecting-and-unselecting-rows-at-the-group-level"></a>Výběr a zrušení výběru řádků na úrovni skupiny
Stejně jako můžete vybrat (nebo zrušit výběr) všech řádků v mřížce zaškrtnutím políčka v horní části prvního sloupce v mřížce, můžete také rychle vybrat (nebo zrušit výběr) všechny řádky ve skupině výběrem zaškrtávacího políčka v příslušném řádku záhlaví skupiny. Zaškrtávací políčko v řádku záhlaví skupiny bude vždy odrážet aktuální stav výběru řádků v této skupině, bez ohledu na to, zda jsou vybrány všechny řádky, nejsou vybrány žádné řádky nebo jsou vybrány pouze některé řádky.

### <a name="hiding-column-names"></a>Skrytí názvů sloupců
Při seskupení dat je výchozím chováním zobrazení názvu sloupce v řádku záhlaví skupiny. Můžete zvolit potlačení názvu sloupce v řádcích záhlaví skupiny výběrem **Možnosti mřížky** > **Skrýt název sloupce skupiny**.

### <a name="grouping-on-date-and-time-columns"></a>Seskupování podle sloupců data a času
Při seskupování podle polí Datum nebo DateTime máte možnost pro seskupení podle roku, měsíce nebo dne. „Hodnota“ skupiny v odpovídajícím řádku záhlaví bude odpovídat formátu z tohoto pole. Navíc pro pole DateTime a Čas můžete seskupovat podle hodin, minut nebo sekund.

> [!IMPORTANT]
> Uživatelé aktuálně nemohou přidat sloupec seskupení poté, co se seskupí na segmentu sloupce data nebo času.

## <a name="freezing-columns"></a>Zmrazení sloupců
Některé sloupce v mřížce mohou být dostatečně důležité pro kontext, který se nemá rolovat mimo zobrazení. Místo toho můžete chtít, aby byly hodnoty v těchto sloupcích vždy viditelné. Funkce **Zmrazení sloupců v mřížce** poskytuje tuto flexibilitu uživatelům. 

[![Zablokování sloupců v mřížce.](./media/gridFreezingColumns-07-25-2022.gif)](./media/gridFreezingColumns-07-25-2022.gif)

Chcete-li sloupec ukotvit, klikněte pravým tlačítkem do záhlaví sloupce a poté vyberte **Ukotvit sloupec**. Při prvním provedení tohoto kroku se vybraný sloupec stane prvním sloupcem a již se nebude posouvat mimo zobrazení. Jakýkoli následující sloupec, který zmrazíte, bude přidán napravo od posledního zmrazeného sloupce. Pomocí standardní funkce Přesunout můžete změnit pořadí zmrazených sloupců podle potřeby. Ukotvené sloupce však nelze přesunout, aby se zobrazily mezi množinou nezmrazených sloupců. Ukotvené sloupce podobně nelze přesunout, aby se zobrazily mezi množinou zmrazených sloupců.

Chcete-li sloupec odmrazit, klikněte pravým tlačítkem do záhlaví zmrazeného sloupce a poté vyberte **Odmrazit sloupec**. 

Všimněte si, že výběr řádků a sloupce stavu řádků v nové mřížce jsou vždy zmrazeny jako první dva sloupce. Proto, když jsou tyto sloupce zahrnuty do mřížky, budou vždy viditelné pro uživatele, bez ohledu na polohu vodorovného posouvání v mřížce. U těchto dvou sloupců nelze změnit pořadí.

## <a name="autofit-column-width"></a>Automaticky přizpůsobit šířku sloupce
Podobně jako v Excelu mohou uživatelé automaticky vynutit změnu velikosti sloupce na základě obsahu aktuálně zobrazeného v tomto sloupci. Stačí dvakrát klepnout (nebo dvakrát kliknout) na úchyty velikosti ve sloupci. Případně umístěte fokus do záhlaví sloupce a poté stiskněte klávesu **A** (pro automatické přizpůsobení).

## <a name="frequently-asked-questions"></a>Časté dotazy
### <a name="how-do-i-enable-the-new-grid-control-in-my-environment"></a>Jak povolím novému ovládacímu prvku mřížky ve svém prostředí? 

Funkce **Nový ovládací prvek mřížky** je k dispozici přímo ve správě funkcí v jakémkoli prostředí. Po povolení funkce ve správě funkcí budou všechny následující relace uživatelů využívat nové ovládání mřížky. 

Tato funkce začala být standardně povolena ve verzi 10.0.21. Má se stát povinným v říjnu 2022.

## <a name="developer-topics"></a>Témata pro vývojáře

### <a name="developer-opting-out-individual-pages-from-using-the-new-grid"></a>[Vývojář] Odhlásit jednotlivé stránky z používání nové mřížky 
Pokud vaše organizace objeví stránku, která má nějaké problémy s využitím nové mřížky, je k dispozici rozhraní API, které umožňuje jednotlivému formuláři používat starší ovládací prvek mřížky, přičemž stále umožňuje ostatním systémům využívat nový ovládací prvek mřížky. Chcete-li jednotlivou stránku odhlásit z nové mřížky, přidejte následující příspěvek volání `super()` s metodou formuláře `run()`.

```this.forceLegacyGrid();```

Toto rozhraní API bude nakonec zastaralé, aby bylo možné odebrat starší ovládací prvek mřížky. Zůstane však k dispozici po dobu nejméně 12 měsíců od oznámení ukončení podpory. Pokud nějaké problémy vyžadují použití tohoto rozhraní API, nahlaste je společnosti Microsoft.

#### <a name="forcing-a-page-to-use-the-new-grid-after-previously-opting-out-the-grid"></a>Vynucení stránky k použití nové mřížky po předchozím odhlášení z mřížky
Pokud jste se z používání nové mřížky odhlásili pro jednotlivou stránku, možná budete chtít později novou mřížku po vyřešení základních problémů znovu povolit. Chcete -li to provést, jednoduše odeberte volání na `forceLegacyGrid()`. Změna se neprojeví, dokud nenastane jedna z následujících situací:

- **Opětovné nasazení prostředí**: Když je prostředí aktualizováno a znovu nasazeno, tabulka, která ukládá stránky, které se odhlásily z nové mřížky (FormControlReactGridState), se automaticky vymaže.
- **Ruční čištění tabulky**: Pro scénáře vývoje budete muset použít SQL k vymazání tabulky FormControlReactGridState a restartování AOS. Tato kombinace akcí resetuje ukládání do mezipaměti stránek, které se odhlásily z nové mřížky.

### <a name="developer-opting-individual-grids-out-of-the-typing-ahead-of-the-system-capability"></a>[Vývojář] Odhlášení jednotlivých mřížek z funkce Zadávání před systémem
Objevily se některé scénáře, které se dobře nehodí pro funkci mřížky *Zadávání před systémem*. (Například nějaký kód, který se spustí při ověření řádku, způsobí spuštění průzkumu zdroje dat a průzkum pak může poškodit neprovedené úpravy na existujících řádcích.) Pokud vaše organizace takový scénář objeví, je k dispozici rozhraní API, které umožňuje vývojáři odhlásit jednotlivou mřížku z asynchronního ověřování řádků a vrátit se ke staršímu chování.

Když je asynchronní ověřování řádků v mřížce zakázáno, uživatelé nemohou vytvořit nový řádek nebo se přesunout do jiného existujícího řádku v mřížce, pokud jsou na aktuálním řádku problémy s ověřením. Jako vedlejší efekt této akce nelze vložit tabulky z Excelu do mřížek finance a provoz.

Chcete-li jednotlivou mřížku odhlásit z asynchronního ověřování řádku, přidejte následující volání po `super()` v metodě formuláře `run()`.

```<gridControl>.allowPreemptiveClient(false);```

> [!NOTE]
> - Toto volání by mělo být vyvoláno pouze ve výjimečných případech a nemělo by být normou pro všechny mřížky.
> - Nedoporučujeme přepínat toto rozhraní API za běhu po načtení formuláře.

### <a name="developer-size-to-available-width-columns"></a>[Vývojář] Sloupce velikosti k dostupné šířce
Pokud vývojář nastaví vlastnost **WidthMode** na **SizeToAvailable** pro sloupce uvnitř nové mřížky mají tyto sloupce zpočátku stejnou šířku, jakou by měli, kdyby byla vlastnost nastavena na **SizeToContent**. Roztahují se však, aby uvnitř mřížky využili jakoukoli další dostupnou šířku. Pokud je vlastnost nastavena na **SizeToAvailable** pro více sloupců sdílejí všechny tyto sloupce jakoukoli další dostupnou šířku uvnitř mřížky. Pokud však uživatel ručně změní velikost jednoho z těchto sloupců, sloupec se stane statickým. Zůstane na této šířce a již se nebude natahovat, aby zabírala další dostupnou šířku mřížky.

### <a name="developer-specifying-the-column-that-receives-the-initial-focus-when-new-rows-are-created-by-using-the-down-arrow-key"></a>[Vývojář] Určení sloupce, který obdrží počáteční fokus při vytváření nových řádků pomocí klávesy šipka dolů
Jak bylo diskutováno v části [Rozdíly při zadávání dat před systémem](#differences-when-entering-data-ahead-of-the-system), pokud je aktivní možnost „Psaní před systémem“ a uživatel vytvoří nový řádek pomocí klávesy **Šipka dolů**, výchozím chováním je umístit fokus do prvního sloupce v novém řádku. Toto chování se může lišit od chování ve starší mřížce, nebo když je vybráno tlačítko **Nový**.

Uživatelé a organizace mohou vytvářet uložené pohledy, které jsou optimalizovány pro zadávání dat. (Můžete například změnit pořadí sloupců tak, aby první sloupec byl ten, do kterého chcete začít zadávat data.) Kromě toho od verze 10.0.29 mohou organizace toto chování upravit pomocí metody **selectedControlOnCreate()**. Tato metoda umožňuje vývojáři zadat sloupce, které obdrží počáteční fokus při vytváření nového řádku pomocí klávesy **Šipka dolů**. Toto rozhraní API jako vstup přebírá ID ovládacího prvku, které odpovídá sloupci, který by měl získat počáteční fokus.

### <a name="developer-handling-grids-with-non-react-extensible-controls"></a>[Vývojář] Manipulace s mřížkami s rozšiřitelnými ovládacími prvky bez React
Když se při načítání mřížky setká systém s rozšiřitelným ovládacím prvkem, který není založen na Reactu, systém místo toho vynutí vykreslení starší mřížky. Když se uživatel poprvé setká s touto situací, zobrazí se zpráva, že je potřeba stránku aktualizovat. Poté tato stránka automaticky načte starší mřížku bez dalších upozornění pro uživatele až do příští aktualizace systému. 

Pro trvalé překonání této situace mohou autoři rozšiřitelných ovládacích prvků vytvořit verzi ovládacího prvku React pro použití v mřížce.  Po vyvinutí může být třída X++ pro ovládací prvek doplněna atributem **FormReactControlAttribute** k určení umístění balíčku React, který se má načíst pro daný ovládací prvek. Viz třída `SegmentedEntryControl` jako příklad.  

## <a name="known-issues"></a>Známé problémy
Tato část udržuje seznam známých problémů pro nový ovládací prvek mřížky.

### <a name="open-issues"></a>Otevřené problémy
- Po aktivaci funkce **Nový ovládací prvek mřížky** budou některé stránky i nadále využívat existující ovládací prvek mřížky. To se stane v následujících situacích:
 
    - [Vyřešeno] Problém 762533: Neočekávaná chyba klienta při výběru řádku v seznamu karet.
    - [Vyřešeno] Na stránce existuje seznam karet, který je vykreslen ve více sloupcích.
        - Tento typ seznamu karet je podporován **novým ovládacím prvkem grid** počínaje verzí 10.0.30. Jakékoli použití forceLegacyGrid() pro tento účel lze odstranit. 
    - [Vyřešeno] Na stránce existuje seskupený seznam karet.
        - Seskupené seznamy karet jsou podporovány **novým ovládacím prvkem grid** počínaje verzí 10.0.30. Jakékoli použití forceLegacyGrid() pro tento účel lze odstranit. 
    - [Vyřešeno] Sloupec mřížky s rozšiřitelným ovládacím prvkem jiným než React.
        - Rozšiřitelné ovládací prvky mohou poskytnout verzi React ovládacího prvku, který se načte při umístění do mřížky, a upravit definici ovládacího prvku tak, aby se tento ovládací prvek načetl při použití v mřížce. Další podrobnosti naleznete v příslušné sekci pro vývojáře. 

    Když se uživatel poprvé setká s jednou z těchto situací, zobrazí se zpráva o aktualizaci stránky. Po zobrazení této zprávy bude stránka nadále využívat stávající mřížku pro všechny uživatele až do další aktualizace produktu. Pro budoucí aktualizaci bude zváženo lepší zacházení s těmito scénáři, aby bylo možné využít novou mřížku.

- [KB 4582758] Záznamy jsou rozmazané, když změníte velikost písma ze 100 na jakékoli jiné procento

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

