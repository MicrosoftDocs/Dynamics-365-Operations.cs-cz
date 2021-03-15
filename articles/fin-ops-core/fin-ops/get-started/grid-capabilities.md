---
title: Možnosti mřížky
description: Toto téma popisuje několik výkonných funkcí ovládacího prvku mřížky. Chcete-li mít přístup k těmto funkcím, je nutné povolit novou funkci mřížky.
author: jasongre
manager: AnnBe
ms.date: 01/22/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DefaultDashboard
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2020-02-29
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: f8ec45208ea86f4b1782eaeb1d14bb414e3b577f
ms.sourcegitcommit: e88c96d1cb817a22db81856cadb563c095ab2671
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/02/2021
ms.locfileid: "5104302"
---
# <a name="grid-capabilities"></a>Možnosti mřížky

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Nový ovládací prvek mřížky poskytuje několik užitečných a výkonných funkcí, které lze použít k vylepšení produktivity uživatelů, vytvoření zajímavějších zobrazení dat a získání smysluplných přehledů dat. Tento článek se týká následujících možností: 

-  Vypočet součtů
-  Zadávání před systémem
-  Vyhodnocování matematických výrazů 
-  Seskupení tabulkových dat (povoleno samostatně pomocí funkce **(Preview) Seskupení do mřížek**)
-  Zmrazení sloupců

## <a name="calculating-totals"></a>Vypočet součtů
V aplikacích Finance and Operations mají uživatelé možnost zobrazit součty v dolní části číselných sloupců v mřížkách. Tyto součty se zobrazí v části zápatí v dolní části mřížky. 

### <a name="showing-the-grid-footer"></a>Zobrazení zápatí mřížky
Aplikace Finance and Operations obsahují oblast zápatí v dolní části každé tabulkové mřížky. V zápatí je možné zobrazit cenné informace související s daty, která se zobrazí v mřížce. Následuje několik příkladů těchto informací:

- Počet vybraných řádků v tabulce (při výběru více než jednoho záznamu)
- Celkové součty v dolní části konfigurovaných číselných sloupců
- Počet řádků v sadě dat 

Toto zápatí je ve výchozím nastavení skryto, ale lze je zapnout. Chcete-li zobrazit zápatí pro mřížku, klikněte pravým tlačítkem na záhlaví sloupce v mřížce a vyberte možnost **Zobrazit zápatí**. Po zapnutí zápatí pro konkrétní mřížku bude toto nastavení zapamatováno, dokud se uživatel nerozhodne zápatí skrýt. Chcete-li zápatí skrýt, klikněte pravým tlačítkem na záhlaví sloupce a vyberte **Skrýt zápatí**.  (Provedení akce **Zobrazit zápatí / Skrýt zápatí** bude v budoucí aktualizaci přemístěno na nové místo. 

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

Pokud výpočet trvá příliš dlouho, můžete operaci zrušit kliknutím na tlačítko **Zrušit**. Někdy je však datová sada příliš velká pro výpočet součtů (limit stanovený vaší organizací) a místo toho budete upozorněni na filtrování dat.

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
Uživatelé vždy mohou exportovat data z mřížek v aplikacích Finance and Operations do aplikace Excel pomocí mechanismu **Exportu do aplikace Excel**. Nicméně možnost zadávání dat před systémem umožňuje, aby nová mřížka podporovala kopírování tabulek z aplikace Excel a jejich vložení přímo do mřížek v aplikacích Finance and Operations. Buňka mřížky, z níž je zahájena operace vložení, určuje, kde bude zkopírovaná tabulka vložena. Obsah mřížky je přepsán obsahem zkopírované tabulky s výjimkou dvou případů:

- Pokud počet sloupců ve zkopírované tabulce překračuje počet sloupců, které zůstanou v mřížce, počínaje místem vložení, uživatel bude upozorněn, že nadbytečné sloupce byly ignorovány. 
- Pokud počet řádků ve zkopírované tabulce překračuje počet řádků v mřížce, počínaje místem vložení, budou existující buňky přepsány vloženým obsahem a všechny další řádky z kopírované tabulky budou vloženy jako nové řádky v dolní části mřížky. 

## <a name="evaluating-math-expressions"></a>Vyhodnocování matematických výrazů
Jedná se o prostředek pro zvýšení produktivity, uživatelé mohou zadávat matematické vzorce do číselných buněk v mřížce. Není nutné provádět výpočet v aplikaci mimo systém. Zadáte-li například hodnotu **=15\*4** a poté se stisknutím klávesy **Tab** přesunete mimo pole, systém vyhodnotí výraz a do pole zapíše hodnotu **60**.

Chcete-li, aby systém rozpoznal hodnotu jako výraz, zahajte tuto hodnotu znaménkem rovná se (**=**). Další informace o podporovaných operátorech a syntaxi naleznete v tématu [Podporované matematické symboly](http://bugwheels94.github.io/math-expression-evaluator/#supported-maths-symbols).

## <a name="grouping-tabular-data"></a>Seskupení tabulkových dat
Obchodní uživatelé často potřebují provádět ad hoc analýzu dat. I když to lze provést exportem dat do aplikace Microsoft Excel a použitím kontingenčních tabulek, funkce **Seskupení do mřížek**, která je obecně dostupná ve verzi 10.0.16/Platform update 40 a je závislá na nové funkci řízení mřížky, umožňuje uživatelům organizovat tabulková data v rámci aplikací Finance and Operations. Protože tato funkce rozšiřuje funkci **součtů**, **seskupení** umožňuje získat smysluplné přehledy o datech poskytnutím mezisoučtů na úrovni skupiny.

Chcete-li použít tuto funkci, klikněte pravým tlačítkem na sloupec, podle kterého chcete provést seskupení, a zvolte **Seskupit tento sloupec**. Tato akce seřadí data podle vybraného sloupce, přidá nový sloupec **Seskupit podle** na začátek mřížky a vloží „řádky záhlaví“ na začátek každé skupiny. Tyto řádky záhlaví obsahují následující informace o každé skupině: 
-  Hodnota dat pro skupinu 
-  Název sloupce (tyto informace budou obzvlášť užitečné, když máte více úrovní seskupení)  
-  Počet datových řádků v této skupině
-  Mezisoučty pro všechny sloupce konfigurované pro zobrazení součtů

Pokud jsou povolena [uložená zobrazení](saved-views.md), lze toto seskupení uložit přizpůsobením jako součást zobrazení pro rychlý přístup při další návštěvě stránky.  

### <a name="multiple-levels-of-grouping"></a>Více úrovní seskupení
Poté, co seskupíte data podle jednoho sloupce, můžete data seskupit podle jiného sloupce výběrem možnosti **Seskupit podle tohoto sloupce** na požadovaném sloupci. Tento proces lze opakovat, dokud nemáte 5 vnořených úrovní seskupení, což je maximální podporovaná hloubka. V tomto okamžiku již nebudete moci seskupovat podle dalších sloupců.  

Seskupení podle libovolného sloupce můžete kdykoli odebrat kliknutím pravým tlačítkem na daný sloupec a výběrem příkazu **Zrušit seskupení**. Seskupení můžete také odebrat ze všech sloupců výběrem **Možností mřížky** a následně příkazu **Oddělit vše**.   

Před verzí 10.0.16/Platform update 40 je podporována pouze jedna úroveň seskupení. V těchto verzích, pokud jsou data seskupena a vyberete možnost **Seskupit podle tohoto sloupce** pro jiný sloupec, se původní seskupení nahradí.  


### <a name="expanding-and-collapsing-groups"></a>Rozbalení a sbalení skupin
V počátečním seskupení dat budou všechny skupiny rozbaleny. Můžete vytvořit souhrnná zobrazení dat sbalením jednotlivých skupin, nebo si můžete rozbalením a sbalením skupiny usnadnit navigaci v datech. Chcete-li skupinu rozbalit nebo sbalit, vyberte tlačítko se znakem > v příslušném řádku záhlaví skupiny. Všimněte si, že stav rozbalení/sbalení jednotlivých skupin **není** uložen v individuálním nastavení.

### <a name="selecting-and-unselecting-rows-at-the-group-level"></a>Výběr a zrušení výběru řádků na úrovni skupiny
Stejně jako můžete vybrat (nebo zrušit výběr) všech řádků v mřížce zaškrtnutím políčka v horní části prvního sloupce v mřížce, můžete také rychle vybrat (nebo zrušit výběr) všechny řádky ve skupině výběrem zaškrtávacího políčka v příslušném řádku záhlaví skupiny. Zaškrtávací políčko v řádku záhlaví skupiny bude vždy odrážet aktuální stav výběru řádků v této skupině, bez ohledu na to, zda jsou vybrány všechny řádky, nejsou vybrány žádné řádky nebo jsou vybrány pouze některé řádky.

### <a name="hiding-column-names"></a>Skrytí názvů sloupců
Při seskupení dat je výchozím chováním zobrazení názvu sloupce v řádku záhlaví skupiny. Počínaje verzí 10.0.14 / Platform Update 38 můžete zvolit potlačení názvu sloupce v řádcích záhlaví skupiny výběrem **Možnosti mřížky** > **Skrýt název sloupce skupiny**.

## <a name="freezing-columns"></a>Zmrazení sloupců
Některé sloupce v mřížce mohou být dostatečně důležité pro kontext, který se nemá rolovat mimo zobrazení. Místo toho chcete, aby byly hodnoty v těchto sloupcích vždy viditelné. Ve verzi 10.0.17 poskytuje funkce **Ukotvit sloupce v mřížce** tuto flexibilitu uživatelům. 

Chcete-li sloupec ukotvit, klikněte pravým tlačítkem do záhlaví sloupce a poté vyberte **Ukotvit sloupec**. Při prvním provedení tohoto kroku se vybraný sloupec stane prvním sloupcem a již se nebude posouvat mimo zobrazení. Jakýkoli následující sloupec, který zmrazíte, bude přidán napravo od posledního zmrazeného sloupce. Pomocí standardní funkce Přesunout můžete změnit pořadí zmrazených sloupců podle potřeby. Ukotvené sloupce však nelze přesunout, aby se zobrazily mezi množinou nezmrazených sloupců. Ukotvené sloupce podobně nelze přesunout, aby se zobrazily mezi množinou zmrazených sloupců.

Chcete-li sloupec odmrazit, klikněte pravým tlačítkem do záhlaví zmrazeného sloupce a poté vyberte **Odmrazit sloupec**. 

Všimněte si, že výběr řádků a sloupce stavu řádků v nové mřížce jsou vždy zmrazeny jako první dva sloupce. Proto, když jsou tyto sloupce zahrnuty do mřížky, budou vždy viditelné pro uživatele, bez ohledu na polohu vodorovného posouvání v mřížce. U těchto dvou sloupců nelze změnit pořadí.

## <a name="frequently-asked-questions"></a>Časté dotazy
### <a name="how-do-i-enable-the-new-grid-control-in-my-environment"></a>Jak povolím novému ovládacímu prvku mřížky ve svém prostředí? 

**10.0.9 / Platform update 33 a novější**

Funkce **Nový ovládací prvek mřížky** je k dispozici přímo ve správě funkcí v jakémkoli prostředí. Podobně jako jiné veřejné funkce náhledu je povolení této funkce v produkčním prostředí podmíněno [dodatečnou smlouvou o použití](https://go.microsoft.com/fwlink/?linkid=2105274).  

**10.0.8 / Platform update 32 a 10.0.7 / Platform update 31**

Funkci **Nový ovládací prvek mřížky** lze povolit v prostředí úrovně 1 (Dev/Test) a úrovně 2 (Sandbox), aby bylo možné poskytnout další změny testování a návrhu pomocí následujících kroků.

1.  **Povolit let**: spustit následující příkaz SQL: 

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, enabled, FLIGHTSERVICEID, PARTITION) VALUES('CLIReactGridEnableFeature', 1, 0, 5637144576);`

2. **Obnovit IIS** pro vyprázdnění statickou mezipaměť testovací verze. 

3.  **Najít funkci**: přejděte do pracovního prostoru **Správa funkcí**. Pokud se **Nový ovládací prvek mřížky** neobjeví v seznamu všech funkcí, vyberte **Vyhledat aktualizace**.   

4.  **Povolit funkci**: vyhledejte funkci **Nový ovládací prvek mřížky** v seznamu funkcí a v podokně podrobností vyberte **Povolit nyní**. Uvědomte si, že je požadována aktualizace prohlížeče. 

Všechny následující uživatelské relace budou povoleným Novým ovládacím prvkem mřížky.

## <a name="developer-opting-out-individual-pages-from-using-the-new-grid"></a>[Vývojář] Odhlásit jednotlivé stránky z používání nové mřížky 
Pokud vaše organizace objeví stránku, která má nějaké problémy s využitím nové mřížky, od verze 10.0.13/Platform update 37 je k dispozici rozhraní API, které umožňuje jednotlivému formuláři používat starší ovládací prvek mřížky, přičemž stále umožňuje ostatním systémům využívat nový ovládací prvek mřížky. Chcete-li jednotlivou stránku odhlásit z nové mřížky, přidejte následující příspěvek volání `super()` s metodou formuláře `run()`.

 ```this.forceLegacyGrid();```

Toto rozhraní API bude respektováno až do vydání října 2021, kdy bude nový ovládací prvek mřížky povinný. Pokud nějaké problémy vyžadují použití tohoto rozhraní API, nahlaste je společnosti Microsoft.

## <a name="developer-size-to-available-width-columns"></a>[Vývojář] Sloupce velikosti k dostupné šířce
Pokud vývojář nastaví vlastnost **WidthMode** na **SizeToAvailable** pro sloupce uvnitř nové mřížky mají tyto sloupce zpočátku stejnou šířku, jakou by měli, kdyby byla vlastnost nastavena na **SizeToContent**. Roztahují se však, aby uvnitř mřížky využili jakoukoli další dostupnou šířku. Pokud je vlastnost nastavena na **SizeToAvailable** pro více sloupců sdílejí všechny tyto sloupce jakoukoli další dostupnou šířku uvnitř mřížky. Pokud však uživatel ručně změní velikost jednoho z těchto sloupců, sloupec se stane statickým. Zůstane na této šířce a již se nebude natahovat, aby zabírala další dostupnou šířku mřížky.  

## <a name="known-issues"></a>Známé problémy
Tato část udržuje seznam známých problémů pro nový ovládací prvek mřížky.  

### <a name="open-issues"></a>Otevřené problémy
-  Po aktivaci funkce **Nový ovládací prvek mřížky** budou některé stránky i nadále využívat existující ovládací prvek mřížky. To se stane v následujících situacích:  
    -  Na stránce existuje seznam karet, který je vykreslen ve více sloupcích.
    -  Na stránce existuje seskupený seznam karet.
    -  Mřížkový sloupec s nereaktivním rozšiřitelným ovládacím prvkem.

    Když se uživatel poprvé setká s jednou z těchto situací, zobrazí se zpráva o aktualizaci stránky. Po zobrazení této zprávy bude stránka nadále využívat stávající mřížku pro všechny uživatele až do další aktualizace produktu. Pro budoucí aktualizaci bude zváženo lepší zacházení s těmito scénáři, aby bylo možné využít novou mřížku.    
    
-  [KB 4582758] Záznamy jsou rozmazané, když změníte velikost písma ze 100 na jakékoli jiné procento
-  [KB 4592012] Neočekávaná chyba klienta v IE11 při vkládání více řádků z Excelu
    -  Microsoft neprovádí opravu tohoto problému

### <a name="fixed-as-part-of-10016"></a>Opraveno jako součást verze 10.0.16

-  [KB 4598335] Víceřádkové ovládací prvky řetězce nerespektují jejich DisplayHeights v seznamech / kartách 
-  [KB 4591891] Řádky návrhu faktury zmizí, když zrušíte označení řádků
-  [KB 4592104] Nelze upravovat záznamy po kliknutí na „Opravit problém“ a přesunu na jiný řádek bez vyřešení problému s ověřením
-  [KB 4594449] Ve výběru data chybí tlačítka „Nikdy“ a „Vymazat“ 
-  [KB 4594448] Zadání času je v nové mřížce zacházeno odlišně
-  [KB 4600059] Neočekávaná chyba klienta s omezením e-mailu
-  [KB 4574584] Náhled přílohy výdajů není k dispozici, když umístíte ukazatel myši nad ikonu potvrzení

### <a name="fixed-as-part-of-10015"></a>Opraveno jako součást verze 10.0.15    

-  (Aktualizace kvality) [KB 4594444] Neočekávaná chyba klienta s náhledem pro řízení segmentovaného vstupu
-  [KB 4582723] Možnosti zobrazení se nezobrazí, když je voláte později v životním cyklu formuláře
-  [KB 4591988] Problémy s použitím klávesnice k výběru hodnoty z vyhledávání ReferenceGroup
-  [KB 4588958] Test Regression Suite Automation Tool (RSAT) selhává s chybou: TypeError: Nelze přečíst vlastnost 'text' nedefinované
-  [KB 4591970] Neočekávaná chyba klienta při vkládání z aplikace Excel byla provedena ihned po kliknutí do mřížky
-  [KB 4591904] Změny dat se neuloží, pokud po úpravě ovládacího prvku uživatel okamžitě klikne a otevře vyhledání jiného ovládacího prvku
-  [KB 4584752] Neočekávaná chyba klienta ve stránce Návrhy faktury projektu
-  [KB 4584540] Nelze opustit mřížku po vložení jednoho řádku do řádku deníku
-  [KB 4591908] Při vytváření nového řádku zůstává zaostření ve sloupci, ve kterém jste byli

### <a name="fixed-as-part-of-10014"></a>Opraveno jako součást verze 10.0.14

-  (Aktualizace kvality) [KB 4584752] Neočekávaná chyba klienta ve stránce Návrhy faktury projektu
-  [KB 4583880] Testy Regression Suite Automation Tool (RSAT) selhaly při akci OpenLookup se zprávou "Cannot read property RowIndex of undefined"
-  [KB 4583847] Neočekávaná chyba klienta při procházení jednotlivými vyhledáváními

### <a name="fixed-as-part-of-10013"></a>Opraveno jako součást verze 10.0.13

-  (Aktualizace kvality) [KB 4584752] Neočekávaná chyba klienta ve stránce Návrhy faktury projektu
-  (Aktualizace kvality) [KB 4583880] Testy Regression Suite Automation Tool (RSAT) selhaly při akci OpenLookup se zprávou "Cannot read property RowIndex of undefined"
-  (Aktualizace kvality) [KB 4583847] Neočekávaná chyba klienta při procházení jednotlivými vyhledáváními 
-  (Aktualizace kvality) [Chyba 471777] Nelze vybrat pole v mřížce pro úpravy nebo vytvoření mobilní aplikace
-  [KB 4582727] Mřížka zamrzne poté, co uživatel dostane dialog pro položky s více množstvími
-  [Chyba 474851] Hypertextové odkazy v ovládacích prvcích referenční skupiny nefungují 
-  [Chyba 474848] Rozšířené náhledy s mřížkami se nezobrazí
-  [KB 4582726] Vlastnost RotateSign není respektována  
-  [Chyba 470173] Zaškrtávací políčka v neaktivních řádcích se přepínají po kliknutí na mezeru v buňce
-  [Chyba 474848] Rozšířené náhledy s mřížkami se nezobrazí
-  [Chyba 474851] Hypertextové odkazy v ovládacích prvcích referenční skupiny nefungují 
-  [Chyba 471777] Nelze vybrat pole v mřížce pro úpravy nebo vytvoření mobilní aplikace
-  [KB 4569441] Problémy s vykreslováním vícesloupcových seznamů karet, popisů obrázků a možností zobrazení v některých polích
-  [KB 4575279] Ne všechny označené řádky se v General Journal odstraní
-  [KB 4575233] Možnosti zobrazení se po přesunutí do jiného řádku neobnoví
-  [Chyba 477884] Vyhledávání vrátí nesprávnou hodnotu / záznam, pokud je aktivována nová kontrola mřížky
-  [KB 4571095] K zaúčtování příjemky produktu dochází při náhodném stisknutí klávesy Enter (správné zpracování výchozí akce stránky)
-  [KB 4575437] Vyhledávání s upravitelnými ovládacími prvky se neočekávaně uzavírají
-  [KB 4569418] Duplicitní řádek vytvořený ve formuláři harmonogramu doručení
-  [KB 4575435] Rozšířený náhled někdy přetrvává, i když ukazatel myši není poblíž pole
-  [KB 4575434] Vyhledávání není filtrováno, když bylo pole změněno
-  [KB 4575430] Hodnoty v polích pro hesla nejsou v mřížce maskovány
-  [KB 4569438] "Zpracování se zastavilo kvůli problému s ověřením" se zobrazí po označení řádků při vyřizování dodavatelských transakcí
-  [KB 4569434] Obnovení formuláře právnických osob má za následek méně záznamů
-  [KB 4575297] Při úpravách a tabulování v mřížce se fokus neustále pohybuje na podokně záznamníku úloh
-  [KB 4566773] Korekční transakce se na dotazu na transakce s poukázkami nezobrazují jako negativní 
-  [KB 4575288] Při výběru hranice mezi řádky v jednoduchém seznamu se fokus resetuje na aktivní řádek
-  [KB 4575287] Zaostření se nevrátí do prvního sloupce, když pomocí šipky dolů vytvoříte nový řádek v denících
-  [KB 4564819] Nelze odstranit řádky ve faktuře s volným textem (protože zdroj dat ChangeGroupMode = ImplicitInnerOuter)
-  [KB 4563317] Pro obrázky nejsou zobrazeny popisky/rozšířené náhledy

### <a name="fixed-as-part-of-10012"></a>Opraveno jako součást verze 10.0.12

- [KB 4558545] Ovládací prvky tabulky neaktualizují obsah zobrazených položek.
- [KB 4558570] Po odstranění záznamu jsou položky stále zobrazeny na stránce.
- [KB 4558572] Styl, který je přidružen k panelu seznamu **ExtendedStyle**, není použit.
- [KB 4558573] Chyby ověření nelze opravit, pokud je požadovaná změna mimo mřížku.
- [KB 4558584] Záporná čísla nejsou správně vykreslena.
- [KB 4560726] "Neočekávaná chyba klienta" nastane po přepínání mezi seznamy pomocí ovládacího prvku zobrazení seznamu.
- [KB 4562141] Po přidání nového záznamu jsou mřížkové indexy vypnuty.
- [KB 4562151] Možnosti záznamníku úloh **Ověřit** a **Kopírovat** nejsou dostupné pro ovládací prvky data a čísla. 
- [KB 4562153] Zaškrtávací políčka na více seznamech nejsou na mřížkách seznamu / karet viditelná.
- [KB 4562646] Někdy nemůžete-kliknout mimo mřížku, pokud vyberete více řádků v mřížce.
- [KB 4562647] Fokus je resetován na první ovládací prvek v dialogovém okně **Publikovat** po přidání nového řádku do mřížky bezpečnostních rolí.
- [KB 4563310] Rozšířený náhled není po změně řádku uzavřen.
- [KB 4563313] "Neočekávaná chyba klienta" se objeví v Internet Explorer, když je při vyhledávání vybrána hodnota.
- [KB 4564557] Vyhledávací a rozbalovací nabídky se neotevřou v Internet Explorer
- [KB 4563324] Navigace nefunguje po otevření pracovního prostoru **Personální management**.

### <a name="fixed-as-part-of-10011"></a>Opraveno jako součást verze 10.0.11

- [Vystavení 432458] Na začátku některých podřízených kolekcí se zobrazí prázdné nebo duplicitní řádky.
- [KB 4549711] Řádky v návrhu platby nelze po povolení nového ovládacího prvku mřížky správně odebrat.
- [KB 4558374] Záznamy, které vyžadují dialogové okno s polymorfním selektorem, nelze vytvořit.
- [KB 4558375] Text nápovědy se nezobrazuje ve sloupcích v nové mřížce.
- [KB 4558376] Mřížky panelů seznamů nejsou vykresleny ve správné výšce v aplikaci Internet Explorer.
- [KB 4558377] Sloupce v poli se seznamem s šířkou **SizeToAvailable** nejsou na některých stránkách vykresleny.
- [KB 4558378] Při procházení k podrobnostem je někdy zobrazen nesprávný záznam.
- [KB 4558379] Při otevření vyhledávání dochází k chybě, pokud **ReplaceOnLookup**=**No**.
- [KB 4558380] Volné místo v mřížce není po sbalení části stránky vyplněno ihned.
- [KB 4558381] Záporná čísla nejsou správně vykreslena / Uživatelé jsou někdy zablokováni při vzniku problémů s ověřením.
- [KB 4558382] Dochází k neočekávaným chybám klienta.
- [KB 4558383] Ovládací prvky mimo mřížku se po odstranění posledního záznamu neaktualizují.
- [KB 4558587] Referenční skupiny s poli se seznamem pro náhradní pole nezobrazují hodnoty.
- [KB 4562143] Po změně řádku nejsou aktualizována pole / Po odstranění řádku dojde k zablokování zpracování mřížky.
- [KB 4562645] Nastane výjimka, když je vyhledávání otevřeno, zatímco jsou spuštěny testy Regression Suite Automation Tool (RSAT).

### <a name="fixed-as-part-of-10010"></a>Opraveno jako součást verze 10.0.10

- [Problém 414301] Při vytvoření nových řádků zmizí některá data z předchozích řádků.
- [Chyba 417044] Pro mřížky ve stylu seznamu neexistuje žádná zpráva o prázdné mřížce.
- [KB 4539058] Některé mřížky (obvykle na záložkách s náhledem) někdy nejsou vykresleny (ale budou vykresleny, pokud oddálíte zobrazení).
- [KB 4549734] Pokud je označující sloupec skrytý, aktivní řádky nejsou považovány za označené.
- [KB 4549796] Hodnoty nelze upravovat v mřížce v režimu zobrazení.
- [KB 4558367] Výběr textu není konzistentní při změně řádků.
- [KB 4558368] Vícenásobný výběr pomocí klávesnice je povolen v situacích výběru jedné položky.
- [KB 4558369] V hierarchické mřížce zmizí obrázky stavu.
- [KB 4558370] Nový řádek není posunut do zobrazení.
- [KB 4558372] Nová mřížka je zablokovaná v režimu zpracování, pokud počet sloupců ve vloženém obsahu přesahuje počet zbývajících sloupců v mřížce.
- [KB 4562631] Časové hodnoty nejsou správně naformátovány.

### <a name="quality-update-for-1009platform-update-33"></a>Aktualizace pro zvýšení kvality pro verzi 10.0.9 / Platform update 33

- [KB 4550367] Časové hodnoty nejsou správně naformátovány.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]