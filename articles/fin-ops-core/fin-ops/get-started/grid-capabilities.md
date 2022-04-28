---
title: Možnosti mřížky
description: Toto téma popisuje několik výkonných funkcí ovládacího prvku mřížky. Chcete-li mít přístup k těmto funkcím, je nutné povolit novou funkci mřížky.
author: jasongre
ms.date: 03/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2020-02-29
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 08348185a424d20b6da1563189496b7dd51944d9
ms.sourcegitcommit: edc887e0526c415466e9691e642028ecd97cdbe7
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/14/2022
ms.locfileid: "8602955"
---
# <a name="grid-capabilities"></a>Možnosti mřížky

[!include [banner](../includes/banner.md)]

Nový ovládací prvek mřížky poskytuje několik užitečných a výkonných funkcí, které lze použít k vylepšení produktivity uživatelů, vytvoření zajímavějších zobrazení dat a získání smysluplných přehledů dat. Tento článek se týká následujících možností: 

- Vypočet součtů
- Zadávání před systémem
- Vyhodnocování matematických výrazů 
- Seskupení tabulkových dat (povoleno samostatně pomocí funkce **Seskupení do mřížek**)
- Zmrazení sloupců (povoleno samostatně pomocí funkce **Zmrazení sloupců v mřížkách**)
- Automaticky přizpůsobit šířku sloupce
- Roztažitelné sloupce

## <a name="calculating-totals"></a>Vypočet součtů
V finančních a provozních aplikacích mají uživatelé možnost zobrazit součty v dolní části číselných sloupců v mřížkách. Tyto součty se zobrazí v části zápatí v dolní části mřížky. 

### <a name="showing-the-grid-footer"></a>Zobrazení zápatí mřížky
Finanční a provozní aplikace obsahují oblast zápatí v dolní části každé tabulkové mřížky. V zápatí je možné zobrazit cenné informace související s daty, která se zobrazí v mřížce. Následuje několik příkladů těchto informací:

- Počet vybraných řádků v tabulce (při výběru více než jednoho záznamu)
- Celkové součty v dolní části konfigurovaných číselných sloupců
- Počet řádků v sadě dat 

Toto zápatí je ve výchozím nastavení skryto, ale lze je zapnout. Chcete-li zobrazit zápatí pro mřížku, vyberte tlačítko **Možnost mřížky** v záhlaví mřížky a vyberte možnost **Zobrazit zápatí**. Po zapnutí zápatí pro konkrétní mřížku bude toto nastavení zapamatováno, dokud se uživatel nerozhodne zápatí skrýt. Chcete-li zápatí skrýt, vyberte **Skrýt zápatí** v nabídce **Možnosti mřížky**.

### <a name="specifying-columns-with-totals"></a>Určení sloupců se součty
V současné době ve výchozím nastavení žádné sloupce nezobrazují součty. Namísto toho je tato činnost považována za jednorázovou, podobně jako nastavení šířky sloupců v mřížce. Jakmile určíte, že chcete zobrazit součty pro sloupec, toto nastavení se při další návštěvě stránky zapamatuje.

Existují dva způsoby konfigurace sloupce pro zobrazení celkového součtu: 

- Pravým tlačítkem klikněte na sloupec, pro který chcete zjistit celkovou hodnotu, a vyberte **Sečíst tento sloupec**. Tato akce způsobí provedení tří událostí:

    1. Zápatí se zobrazí. 
    2. Bude uložena vaše preference pro zobrazení součtu v tomto sloupci. 
    3. Tato akce zahájí výpočet součtu pro tento sloupec a všechny dříve konfigurované, pro zobrazení celkových hodnot. Čas potřebný k zobrazení celkového součtu závisí na velikosti sady dat, kterou vytváříte.

- Poté, co je zápatí viditelné, vyberte **Zobrazit součet** v oblasti zápatí v dolní části sloupce, pro který chcete zobrazit součet. Pokud neexistují žádné konfigurované sloupce, tlačítko **Zobrazit součet** bude k dispozici pro všechny číselné sloupce. 

    Je-li pro součty nakonfigurován alespoň jeden sloupec, budou tlačítka **Zobrazit součet** k dispozici pouze při přechodu nebo výběru. Akce vybírání **Zobrazit součet** pouze ukládá vaši předvolbu pro zobrazení součtu v tomto sloupci, takže přednost bude uplatněna během příštích návštěv na stránce. V zápatí je tento stav označen pomlčkou, která se zobrazí ve sloupci. (Případně, je-li sada dat dostatečně malá, součet se zobrazí okamžitě.)

Pokud uděláte chybu a již nechcete zobrazovat celkový součet v určitém sloupci, klikněte pravým tlačítkem na sloupec a vyberte možnost **Skrýt součet**, nebo v zápatí daného sloupce zvolte tlačítko **Skrýt součet**. Tato preference bude také uložena pro budoucí návštěvy na stránce. 

### <a name="calculating-totals"></a>Výpočet součtů
Když přejdete na stránku se zobrazeným zápatím a sloupci, které jsou již pro součty nakonfigurovány, mohou být součty zobrazeny v zápatí nebo nikoliv. Chování je závislé na velikosti datové sady na stránce. Pokud je datová sada dostatečně malá, součty se zobrazí automaticky spolu s počtem řádků v sadě dat. Pokud v zápatí existují pomlčky pod sloupci, které jste nakonfigurovali pro součty, je sada dat příliš velká, aby systém mohl zobrazit součty okamžitě, a k výpočtu součtů je nutné provést explicitní akci. Tu provedete kliknutím na tlačítko **Vypočítat** v zápatí, nebo klikněte pravým tlačítkem na sloupec, pro který chcete vytvořit součet a vyberte možnost **Sečíst tento sloupec**.

Pokud výpočet trvá příliš dlouho, můžete operaci zrušit kliknutím na tlačítko **Zrušit**. Někdy je datová sada příliš velká pro výpočet součtů (limit stanovený vaší organizací) a místo toho budete upozorněni na filtrování dat. 

> [!NOTE]
> Správci systému mohou upravit limit počtu záznamů dostupných pro výpočet součtů úpravou parametru **Maximální počet místních záznamů pro každou mřížku** na stránce **Možnosti výkonu klienta**. Výchozí hodnota je 25 000 záznamů. Správci by měli být při úpravě této hodnoty opatrní, protože příliš velká hodnota může vyčerpat dostupnou paměť v počítači uživatele. Doporučení je nepřekročit 50 000 záznamů.   

Součty se aktualizují automaticky při aktualizaci, odstranění nebo vytvoření řádků v sadě dat.

## <a name="typing-ahead-of-the-system"></a>Zadávání před systémem
V mnoha obchodních situacích je schopnost rychlého zadávání dat do systému velmi důležitá. Než byl zaveden nový ovládací prvek mřížky, uživatelé mohli měnit data pouze v aktuálním řádku. Před vytvořením nového řádku nebo přepnutím na jiný řádek byli nuceni čekat, než systém úspěšně ověří provedené změny. Ve snaze o zkrácení doby, kdy uživatelé čekají na dokončení těchto ověření, a za účelem zvýšení produktivity uživatelů nová mřížka tato ověření upravuje, takže jsou asynchronní. Uživatel se proto může přesunout do jiných řádků a provést změny, zatímco ověřování předchozích řádků čekají na vyřízení. 

Kvůli tomuto novému chování byl do levé části sloupce výběru řádku přidán nový sloupec se stavem řádku, pokud je mřížka v režimu úprav. Tento sloupec uvádí jeden z následujících stavů:

- **Prázdné** – žádný stavový obrázek označuje, že byl řádek úspěšně uložen systémem.
- **Čekání na zpracování** – tento stav znamená, že změny v řádku dosud nebyly uloženy serverem, ale jsou ve frontě změn, které je nutné zpracovat. Před provedením akce mimo mřížku je nutné počkat na zpracování všech čekajících změn. Dále je text v těchto řádcích kurzívou, aby označoval neuložený stav řádků. 
- **Neplatný stav** - Tento stav označuje, že během zpracování řádku bylo spuštěno nějaké varování nebo zpráva, a mohlo to zabránit systému v uložení změn v tomto řádku. Ve staré mřížce, pokud se uložení nezdařilo, jste byli nuceni navrátit se do řádku a okamžitě problémy opravit. V nové mřížce se však zobrazí upozornění, že došlo k potížím s ověřením, ale můžete se rozhodnout, kdy chcete opravit problémy v řádku. Až budete připraveni problém vyřešit, můžete vrátit fokus ručně do řádku. Alternativně můžete vybrat akci **Opravit tento problém**. Tato akce okamžitě přesune fokus zpět do řádku s problémem a umožní vám provádět úpravy uvnitř nebo vně mřížky. Všimněte si, že zpracování následných čekajících řádků je zastaveno, dokud nebude toto upozornění na ověření vyřešeno. 
- **Pozastaveno** – tento stav znamená, že zpracování bylo pozastaveno, protože ověření řádku aktivovalo překryvné dialogové okno, které vyžaduje vstup uživatele. Vzhledem k tomu, že uživatel může zadávat data v některém jiném řádku, místní dialogové okno se tomuto uživateli nezobrazí okamžitě. Namísto toho se zobrazí v případě, že uživatel zvolí obnovení zpracování. Tento stav je doprovázen oznámením, které uživatele informuje o situaci. Oznámení zahrnuje akci **Obnovit zpracování**, která aktivuje místní dialogové okno.

Když uživatelé zadávají data v místě, kam zatím nedošlo zpracování serveru, mohou očekávat několik omezení při zadávání dat, jako je například nemožnost vyhledávání, ověřování na úrovni ovládacích prvků a zadávání výchozích hodnot. Uživatelé, kteří potřebují rozevírací seznam pro vyhledání hodnoty, by měli počkat, až server dojde k aktuálnímu řádku. Ověření na úrovni ovládacích prvků a zadání výchozích hodnot také proběhnou, když server zpracuje daný řádek.

### <a name="pasting-from-excel"></a>Vkládání z aplikace Excel
Uživatelé vždy mohou exportovat data z mřížek v finančních a provozních aplikacích do aplikace Microsoft Excel pomocí mechanismu **Exportu do aplikace Excel**. Nicméně možnost zadávání dat před systémem umožňuje, aby nová mřížka podporovala kopírování tabulek z aplikace Excel a jejich vložení přímo do mřížek v finančních a provozních aplikacích. Buňka mřížky, z níž je zahájena operace vložení, určuje, kde bude zkopírovaná tabulka vložena. Obsah mřížky je přepsán obsahem zkopírované tabulky s výjimkou dvou případů:

- Pokud počet sloupců ve zkopírované tabulce překračuje počet sloupců, které zůstanou v mřížce, počínaje místem vložení, uživatel bude upozorněn, že nadbytečné sloupce byly ignorovány. 
- Pokud počet řádků ve zkopírované tabulce překračuje počet řádků v mřížce, počínaje místem vložení, budou existující buňky přepsány vloženým obsahem a všechny další řádky z kopírované tabulky budou vloženy jako nové řádky v dolní části mřížky. 

## <a name="evaluating-math-expressions"></a>Vyhodnocování matematických výrazů
Jedná se o prostředek pro zvýšení produktivity, uživatelé mohou zadávat matematické vzorce do číselných buněk v mřížce. Není nutné provádět výpočet v aplikaci mimo systém. Zadáte-li například hodnotu **=15\*4** a poté se stisknutím klávesy **Tab** přesunete mimo pole, systém vyhodnotí výraz a do pole zapíše hodnotu **60**.

Chcete-li, aby systém rozpoznal hodnotu jako výraz, zahajte tuto hodnotu znaménkem rovná se (**=**). Další informace o podporovaných operátorech a syntaxi naleznete v tématu [Podporované matematické symboly](http://bugwheels94.github.io/math-expression-evaluator/#supported-maths-symbols).

## <a name="grouping-tabular-data"></a>Seskupení tabulkových dat
Obchodní uživatelé často potřebují provádět ad hoc analýzu dat. I když to lze provést exportem dat do aplikace Microsoft Excel a použitím kontingenčních tabulek, funkce (Preview) **Seskupení do mřížek**, která je závislá na nové funkci řízení mřížky, umožňuje uživatelům organizovat tabulková data v rámci finančních a provozních aplikací. Protože tato funkce rozšiřuje funkci **součtů**, **seskupení** umožňuje získat smysluplné přehledy o datech poskytnutím mezisoučtů na úrovni skupiny.

Chcete-li použít tuto funkci, klikněte pravým tlačítkem na sloupec, podle kterého chcete provést seskupení, a zvolte **Seskupit tento sloupec**. Tato akce seřadí data podle vybraného sloupce, přidá nový sloupec **Seskupit podle** na začátek mřížky a vloží „řádky záhlaví“ na začátek každé skupiny. Tyto řádky záhlaví obsahují následující informace o každé skupině:

- Hodnota dat pro skupinu 
- Název sloupce (tyto informace budou obzvlášť užitečné, když máte více úrovní seskupení)
- Počet datových řádků v této skupině
- Mezisoučty pro všechny sloupce konfigurované pro zobrazení součtů

Pokud jsou povolena [uložená zobrazení](saved-views.md), lze toto seskupení uložit přizpůsobením jako součást zobrazení pro rychlý přístup při další návštěvě stránky.

### <a name="multiple-levels-of-grouping"></a>Více úrovní seskupení
Poté, co seskupíte data podle jednoho sloupce, můžete data seskupit podle jiného sloupce výběrem možnosti **Seskupit podle tohoto sloupce** na požadovaném sloupci. Tento proces lze opakovat, dokud nemáte 5 vnořených úrovní seskupení, což je maximální podporovaná hloubka. V tomto okamžiku již nebudete moci seskupovat podle dalších sloupců.

Seskupení podle libovolného sloupce můžete kdykoli odebrat kliknutím pravým tlačítkem na daný sloupec a výběrem příkazu **Zrušit seskupení**. Seskupení můžete také odebrat ze všech sloupců výběrem **Možností mřížky** a následně příkazu **Oddělit vše**.

### <a name="sorting-grouped-data"></a>Řazení seskupených dat
Po seskupení dat podle jednoho nebo více sloupců můžete změnit směr řazení pro kterýkoli sloupec seskupení pomocí odpovídajícího záhlaví sloupce. 

Chování při řazení podle neseskupených sloupců závisí na verzi vašeho produktu:

- Pokud ve verzi 10.0.24 a dřívějších řadíte podle neseskupeného sloupce, seskupení se odstraní ze všech sloupců a data se seřadí podle vybraného sloupce. 
- Pokud ve verzi 10.0.25 nebo pozdější řadíte podle neseskupeného sloupce, seskupení zůstane beze změny a data se seřadí v rámci jednotlivých skupin podle vybraného sloupce.

### <a name="expanding-and-collapsing-groups"></a>Rozbalení a sbalení skupin
V počátečním seskupení dat budou všechny skupiny rozbaleny. Můžete vytvořit souhrnná zobrazení dat sbalením jednotlivých skupin, nebo si můžete rozbalením a sbalením skupiny usnadnit navigaci v datech. Chcete-li skupinu rozbalit nebo sbalit, vyberte tlačítko se znakem > v příslušném řádku záhlaví skupiny. Všimněte si, že stav rozbalení/sbalení jednotlivých skupin **není** uložen v individuálním nastavení.

### <a name="selecting-and-unselecting-rows-at-the-group-level"></a>Výběr a zrušení výběru řádků na úrovni skupiny
Stejně jako můžete vybrat (nebo zrušit výběr) všech řádků v mřížce zaškrtnutím políčka v horní části prvního sloupce v mřížce, můžete také rychle vybrat (nebo zrušit výběr) všechny řádky ve skupině výběrem zaškrtávacího políčka v příslušném řádku záhlaví skupiny. Zaškrtávací políčko v řádku záhlaví skupiny bude vždy odrážet aktuální stav výběru řádků v této skupině, bez ohledu na to, zda jsou vybrány všechny řádky, nejsou vybrány žádné řádky nebo jsou vybrány pouze některé řádky.

### <a name="hiding-column-names"></a>Skrytí názvů sloupců
Při seskupení dat je výchozím chováním zobrazení názvu sloupce v řádku záhlaví skupiny. Můžete zvolit potlačení názvu sloupce v řádcích záhlaví skupiny výběrem **Možnosti mřížky** > **Skrýt název sloupce skupiny**.

### <a name="grouping-on-date-and-time-columns"></a>Seskupování podle sloupců data a času
Počínaje verzí 10.0.24 byla pro pole Datum nebo DateTime přidána možnost pro seskupení podle roku, měsíce nebo dne. „Hodnota“ skupiny v odpovídajícím řádku záhlaví bude odpovídat formátu z tohoto pole. Navíc pro pole DateTime a Čas můžete seskupovat podle hodin, minut nebo sekund. 

## <a name="freezing-columns"></a>Zmrazení sloupců
Některé sloupce v mřížce mohou být dostatečně důležité pro kontext, který se nemá rolovat mimo zobrazení. Místo toho můžete chtít, aby byly hodnoty v těchto sloupcích vždy viditelné. Funkce **Zmrazení sloupců v mřížce** poskytuje tuto flexibilitu uživatelům. 

Chcete-li sloupec ukotvit, klikněte pravým tlačítkem do záhlaví sloupce a poté vyberte **Ukotvit sloupec**. Při prvním provedení tohoto kroku se vybraný sloupec stane prvním sloupcem a již se nebude posouvat mimo zobrazení. Jakýkoli následující sloupec, který zmrazíte, bude přidán napravo od posledního zmrazeného sloupce. Pomocí standardní funkce Přesunout můžete změnit pořadí zmrazených sloupců podle potřeby. Ukotvené sloupce však nelze přesunout, aby se zobrazily mezi množinou nezmrazených sloupců. Ukotvené sloupce podobně nelze přesunout, aby se zobrazily mezi množinou zmrazených sloupců.

Chcete-li sloupec odmrazit, klikněte pravým tlačítkem do záhlaví zmrazeného sloupce a poté vyberte **Odmrazit sloupec**. 

Všimněte si, že výběr řádků a sloupce stavu řádků v nové mřížce jsou vždy zmrazeny jako první dva sloupce. Proto, když jsou tyto sloupce zahrnuty do mřížky, budou vždy viditelné pro uživatele, bez ohledu na polohu vodorovného posouvání v mřížce. U těchto dvou sloupců nelze změnit pořadí.

## <a name="autofit-column-width"></a>Automaticky přizpůsobit šířku sloupce
Podobně jako v Excelu mohou uživatelé automaticky vynutit změnu velikosti sloupce na základě obsahu aktuálně zobrazeného v tomto sloupci. Chcete-li to provést, poklepejte na úchyty pro změnu velikosti ve sloupci nebo přesuňte kurzor do záhlaví sloupce a stiskněte **A** (pro automatické přizpůsobení). Tato funkce je dostupná od verze 10.0.23.

## <a name="frequently-asked-questions"></a>Časté dotazy
### <a name="how-do-i-enable-the-new-grid-control-in-my-environment"></a>Jak povolím novému ovládacímu prvku mřížky ve svém prostředí? 

Funkce **Nový ovládací prvek mřížky** je k dispozici přímo ve správě funkcí v jakémkoli prostředí. Po povolení funkce ve správě funkcí budou všechny následující relace uživatelů využívat nové ovládání mřížky. 

Tato funkce je ve výchozím nastavení povolena od verze 10.0.21 a od října 2022 se stává povinnou.  

## <a name="developer-opting-out-individual-pages-from-using-the-new-grid"></a>[Vývojář] Odhlásit jednotlivé stránky z používání nové mřížky 
Pokud vaše organizace objeví stránku, která má nějaké problémy s využitím nové mřížky, je k dispozici rozhraní API, které umožňuje jednotlivému formuláři používat starší ovládací prvek mřížky, přičemž stále umožňuje ostatním systémům využívat nový ovládací prvek mřížky. Chcete-li jednotlivou stránku odhlásit z nové mřížky, přidejte následující příspěvek volání `super()` s metodou formuláře `run()`.

```this.forceLegacyGrid();```

Toto rozhraní API bude respektováno do doby, kdy bude nový ovládací prvek mřížky povinný. Tato změna je aktuálně plánována na říjen 2022. Pokud nějaké problémy vyžadují použití tohoto rozhraní API, nahlaste je společnosti Microsoft.

### <a name="forcing-a-page-to-use-the-new-grid-after-previously-opting-out-the-grid"></a>Vynucení stránky k použití nové mřížky po předchozím odhlášení z mřížky
Pokud jste se z používání nové mřížky odhlásili pro jednotlivou stránku, možná budete chtít později novou mřížku po vyřešení základních problémů znovu povolit. Chcete -li to provést, jednoduše odeberte volání na `forceLegacyGrid()`. Změna se neprojeví, dokud nenastane jedna z následujících situací:

- **Opětovné nasazení prostředí**: Když je prostředí aktualizováno a znovu nasazeno, tabulka, která ukládá stránky, které se odhlásily z nové mřížky (FormControlReactGridState), se automaticky vymaže.
- **Ruční čištění tabulky**: Pro scénáře vývoje budete muset použít SQL k vymazání tabulky FormControlReactGridState a restartování AOS. Tato kombinace akcí resetuje ukládání do mezipaměti stránek, které se odhlásily z nové mřížky.

## <a name="developer-opting-individual-grids-out-of-the-typing-ahead-of-the-system-capability"></a>[Vývojář] Odhlášení jednotlivých mřížek z funkce Zadávání před systémem
Objevily se některé scénáře, které se dobře nehodí pro funkci mřížky *Zadávání před systémem*. (Například nějaký kód, který se spustí při ověření řádku, způsobí spuštění průzkumu zdroje dat a průzkum pak může poškodit neprovedené úpravy na existujících řádcích.) Pokud vaše organizace takový scénář objeví, je k dispozici rozhraní API, které umožňuje vývojáři odhlásit jednotlivou mřížku z asynchronního ověřování řádků a vrátit se ke staršímu chování.

Když je asynchronní ověřování řádků v mřížce zakázáno, uživatelé nemohou vytvořit nový řádek nebo se přesunout do jiného existujícího řádku v mřížce, pokud jsou na aktuálním řádku problémy s ověřením. Jako vedlejší efekt této akce nelze vložit tabulky z Excelu do mřížek Finance a Operace.

Chcete-li jednotlivou mřížku odhlásit z asynchronního ověřování řádku, přidejte následující volání po `super()` v metodě formuláře `run()`.

```<gridControl>.allowPreemptiveClient(false);```

> [!NOTE]
> - Toto volání by mělo být vyvoláno pouze ve výjimečných případech a nemělo by být normou pro všechny mřížky.
> - Nedoporučujeme přepínat toto rozhraní API za běhu po načtení formuláře.

## <a name="developer-size-to-available-width-columns"></a>[Vývojář] Sloupce velikosti k dostupné šířce
Pokud vývojář nastaví vlastnost **WidthMode** na **SizeToAvailable** pro sloupce uvnitř nové mřížky mají tyto sloupce zpočátku stejnou šířku, jakou by měli, kdyby byla vlastnost nastavena na **SizeToContent**. Roztahují se však, aby uvnitř mřížky využili jakoukoli další dostupnou šířku. Pokud je vlastnost nastavena na **SizeToAvailable** pro více sloupců sdílejí všechny tyto sloupce jakoukoli další dostupnou šířku uvnitř mřížky. Pokud však uživatel ručně změní velikost jednoho z těchto sloupců, sloupec se stane statickým. Zůstane na této šířce a již se nebude natahovat, aby zabírala další dostupnou šířku mřížky.

## <a name="known-issues"></a>Známé problémy
Tato část udržuje seznam známých problémů pro nový ovládací prvek mřížky.

### <a name="open-issues"></a>Otevřené problémy
- Po aktivaci funkce **Nový ovládací prvek mřížky** budou některé stránky i nadále využívat existující ovládací prvek mřížky. To se stane v následujících situacích:
 
    - Na stránce existuje seznam karet, který je vykreslen ve více sloupcích.
    - Na stránce existuje seskupený seznam karet.
    - Mřížkový sloupec s nereaktivním rozšiřitelným ovládacím prvkem.

    Když se uživatel poprvé setká s jednou z těchto situací, zobrazí se zpráva o aktualizaci stránky. Po zobrazení této zprávy bude stránka nadále využívat stávající mřížku pro všechny uživatele až do další aktualizace produktu. Pro budoucí aktualizaci bude zváženo lepší zacházení s těmito scénáři, aby bylo možné využít novou mřížku.

- [KB 4582758] Záznamy jsou rozmazané, když změníte velikost písma ze 100 na jakékoli jiné procento
- [KB 4592012] Neočekávaná chyba klienta v IE11 při vkládání více řádků z Excelu

    Microsoft neprovádí opravu tohoto problému


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
