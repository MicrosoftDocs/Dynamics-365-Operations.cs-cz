---
title: "Přizpůsobení uživatelského prostředí"
description: "Toto téma vysvětluje, jakým způsobem lze přizpůsobit aplikaci Microsoft Dynamics 365 for Finance and Operations."
author: TLeforMicrosoft
manager: AnnBe
ms.date: 10/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysUserSetup, DefaultDashboard
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 62363
ms.assetid: 57b445d7-3e9e-4228-8728-f63b9dbd77a3
ms.search.region: Global
ms.author: tlefor
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7a828090fa34eb96d2b557eb06e48ad05b421ae8
ms.openlocfilehash: 3d969069dd5f447b449df84b097527d3814aa338
ms.contentlocale: cs-cz
ms.lasthandoff: 11/20/2017

---

# <a name="personalize-the-user-experience"></a>Přizpůsobení uživatelského prostředí

[!include [banner](../includes/banner.md)]

Toto téma vysvětluje, jakým způsobem lze přizpůsobit aplikaci Microsoft Dynamics 365 for Finance and Operations.

K dispozici je více typů přizpůsobení v aplikaci Dynamics 365 for Finance and Operations. Některá přizpůsobení jsou výběry, které byly vytvořeny v seznamu voleb na stránce nastavení. Některá přizpůsobení jsou implicitní, například že aplikace Finance and Operations uchovává informace o šířce sloupců mřížky, upravíte-li je a rozbalíte a sbalíte stav pevné záložky. Jiná přizpůsobení jsou explicitní. Pro explicitní přizpůsobení zadejte režim interaktivního přizpůsobení a upravte vzhled stránky přímo řízením způsobu, jakým se elementy zobrazují či reagují na stránce. 

Všechna individuální nastavení kteréhokoli typu, které uživatel v aplikaci Finance and Operations udělá, jsou určeny pouze pro daného uživatele, bez ohledu na společnost, se kterou uživatel pracuje. Změny, které uživatel provede na stránce neovlivní ostatní uživatelé v systému.

## <a name="system-wide-options-for-the-current-user"></a>Systémové možnosti pro aktuálního uživatele
Navigační panel obsahuje obrázek ozubeného kola, který se nazývá tlačítko nabídky **Nastavení**. Při otevírání nabídky **Nastavení** se zobrazí počet voleb. Při výběru **Možnosti** se uživateli otevře stránka **Možnosti**. Najdete zde tyto čtyři karty s možnostmi: 

-   **Vizuální** - Vyberte motiv barvy a výchozí velikost prvků na svých stránkách.
-   **Předvolby** - Zde můžete vybrat výchozí hodnoty pokaždé, když otevřete aplikaci Finance and Operations včetně společnosti, úvodní stránky a výchozího režim zobrazení/úprav (určující, zda je stránka uzamčena pro zobrazení nebo otevření k úpravám při každém otevření). Naleznete zde také jazyk, časové pásmo a datum, čas a možnosti formátu čísel. Nakonec tato stránka obsahuje číslo různých předvoleb, které se liší od dílčí verze.
-   **Účet**- Je používán k poskytování ID uživatele a ostatních možností vztahujících se k účtu.
-   **Workflow**- Zde volíte možnosti týkající se workflowu.

## <a name="implicit-personalizations"></a>Implicitní individuální nastavení
Implicitní individuální nastavení jsou ta přizpůsobení, která provádíte pouhou spoluprací s některými ovládací prvky, které pamatují jejich aktuální viditelný stav. 

- **Sloupce mřížky** - Šířku sloupce v seznamu můžete upravit výběrem na ukazateli velikosti vlevo nebo vpravo od záhlaví a jeho posunem doleva nebo doprava na požadovanou šířku. Aplikace Finance and Operations uloží požadovanou šířku a zobrazí tento sloupec této šířky při každém otevření stránky se seznamem. 

- **Pevné záložky** - Některé stránky mají možnost rozbalení oddílů, kterým se říká *pevné záložky*. Finance and Operations si ukládá, kterou pevnou záložku jste rozbalili a kterou sbalili. Vždy, když se vrátíte na stránku, stejné pevné záložky bude rozbalené nebo sbalené podle jejich posledního použití. V tomto článku si vysvětlíme, jak změnit pořadí oddílů pevných záložek. V některých případech sbalení pevné záložky můžete zvýšit výkon, protože aplikace Finance and Operations nebude muset načítat informace o dané pevné záložce, dokud záložka nebude rozbalena. 

- **Okna s fakty** - Některé stránky obsahují oddíl s názvem *okna s fakty*. Toto podokno obsahuje jen informace pro čtení související s aktuálním předmětem stránky. Každý oddíl v podokně okna s fakty se nazývá okno s fakty. Můžete rozbalit nebo sbalit pole faktů a aplikace Finance and Operations uloží vaše preference. V některých případech sbalení okna s fakty můžete zvýšit výkon, protože aplikace Finance and Operations nebude muset načítat informace o daném okně s fakty, dokud okno nebude rozbaleno.

## <a name="explicit-personalizations-using-the-personalization-toolbar"></a>Explicitní přizpůsobení za použití panelu nástrojů přizpůsobení.
Každý osoba a společnost má jinou perspektivu, která data jsou pro ně nejdůležitější, nebo která data nejsou potřebná pro způsob, jakým spouštějí svá obchodní data. Možnost přizpůsobit způsob, jak je objednaná vaše informace, jak vzájemně působí, nebo dokonce jakým způsobem je skrytá, je klíčem k tvorbě osobního a výrobního prostředí aplikace Finance and Operations. 

Explicitní individuální nastavení jsou taková, která provádíte explicitně s úmyslem změnit vzhled nebo chování prvku nebo stránky, volbou nabídky přizpůsobení. Nejzákladnějším typem explicitního přizpůsobení je, když na prvek kliknete pravým tlačítkem myši a vyberete **Přizpůsobit**. (Všimněte si, že ne všechny prvky na stránce mohou být přizpůsobeny.) Vyberete-li tuto metodu přizpůsobení zobrazí se okno Vlastnosti prvku. 

[![Přizpůsobení vlastností prvku](./media/personalization-element-properties.jpg)](./media/personalization-element-properties.jpg) 

Prvek na vaší stránce přizpůsobíte tímto způsobem: pokud jednoduše chcete změnit popisek prvku, skrýt prvek tak, aby nebyl zobrazen na stránce (to nezmění všechna data, jednoduše se vám nezobrazí informace), včetně informací v oddílu souhrnu pevné záložky (pokud je prvek v pevné záložce), při použití tabulátoru vynechejte pole nebo to zařiďte tak, aby nemohla být data změněna jeho označením jako „Neupravovat“. 

Pokud chcete přesunout nebo skrýt prvky nebo provést několik změn, můžete použít nástroj individuálního nastavení, který je k dispozici v okně Vlastnosti prvků výběrem **Přizpůsobit tento formulář**. Panel nástrojů individuálních nastavení je též k dispozici v podokně akcí formuláře pod skupinou **Přizpůsobit** na kartě **Možnosti**. Zvolte **Přizpůsobit tento formulář** a zobrazí se panel nástrojů individuálních nastavení. 

[![Panel nástrojů Přizpůsobení](./media/personalization-personalizationtoolbar.jpg)](./media/personalization-personalizationtoolbar.jpg)

Panel nástrojů Přizpůsobení má několik akcí přizpůsobení. 

- Zvolte nástroj **Vybrat**, pokud chcete vybrat a změnit vlastnosti mnoha prvků po jednom. Za prvé, klepněte na nástroj Vybrat a pak klepněte na prvek, jehož vlastnosti chcete upravit. Při výběru prvku se otevře okno vlastností prvku a můžete upravit jakékoli vlastnosti pro daný prvek. Proces můžete opakovat další prvky formuláře, které je možné přizpůsobit. V některých případech po výběru prvku a uvidíte, že některé vlastnosti nelze měnit. To znamená, že na základě způsobu aktuálního používaného prvku vám aplikace Finance and Operations neumožňuje měnit vlastnosti. Nemůžete například skrýt pole, které je požadováno. 

- Zvolte nástroj pro **Přesunutí**, pokud chcete vybrat a přesunout prvek na jiné místo v rámci aktuální skupiny prvků. (Prvek nelze přesunout mimo nadřazenou skupinu). Za prvé, klepněte na nástroj Přesunout a pak klepněte na prvek, který chcete přesunout. Po klepnutí na prvek, který chcete přesunout, prohledá aplikace Finance and Operations formulář, aby určila, kam tento prvek lze přesunout, a vytvoří řadu „zóny přetažení“, která se zobrazí jako barevné tučné řádky u oblasti, kam v aktuální skupině lze prvek přetáhnout. 

- Chcete-li provést výběr a skrýt prvek, zvolte možnost **skrýt**. Ke skrytí prvku stačí vybrat nástroj Skrýt a klepnout na prvek, který se má skrýt. Vyberete-li nástroj skrytí, nyní všechny skryté prvky budou viditelné a zobrazené v šedém kontejneru, takže můžete vybrat prvek, který chcete zobrazit. 

- Zvolte nástroj **Výběr**, a prohlédněte si, jak bude vypadat stránka s vybranými skrytými prvky. 

- Zvolte nástroj **Souhrn**, pokud chcete v pevné záložce v oblasti souhrnu zobrazit číslo nebo pole řetězců. Nástroj Souhrn platí pouze pro pole, která jsou obsažena v pevné záložce oddílu. Když vyberete nástroj Souhrn, aplikace Finance and Operations zobrazí všechna pole, která byla vybrána jako souhrnná pole, jejich uzavřením v šedém kontejneru. Klepnutím na pole můžete interaktivně přidávat a odebírat pole ze pevné záložky shrnutí. 

- Zvolte nástroj **Přeskočit**, chcete-li odebrat prvek z řady karet klávesnic na stránce. Vyberete-li si nástroj přeskočení, všechny aktuálně přeskočené prvky se zobrazí v šedém kontejneru, takže je možné je znovu zvolit, aby byly součástí pořadí karet výběrem přeskočených prvků. 

- Zvolte nástroj **Upravit**, když chcete označit prvek jako *Upravitelný* nebo *Neupravitelný*. Vyberete-li nástroj úprav, nyní všechny needitovatelné prvky budou zobrazené v šedém kontejneru, takže můžete vybrat ty, který chcete mít editovatelné. Všimněte si, že některá pole jsou povinná a nelze je upravovat. Tato pole se zobrazí s ikonou visacího zámku. 

- Zvolte nástroj **přidání** pro přidání pole na stránku. Pomocí nástroje přidávání nelze vytvořit nové pole, ale můžete přidat pole, které jsou součástí aktuální definice stránky, ale nejsou zobrazena na stránce. Vyberete-li nástroj přidání, musíte nejprve vybrat skupinu nebo oblast, kam chcete pole přidat. Dialogové okno zobrazí seznam polí souvisejících s oddílem, který jste vybrali. Z tohoto dialogového okna můžete vybrat jedno či více polí a klikněte na **Vložit**. Chcete-li později odstranit dříve přidané pole, opakujte tento postup, ale pouze vymažte pole, která jste předtím přidali. 

- Zvolte tlačítko **Správa** k zobrazení seznamu možností řízení týkající se všech individuálních nastavení pro aktuální stránku. 

- Zvolte **Vymazat**, pokud chcete obnovit výchozí nainstalovaný stav stránky. Vymaže všechna individuální nastavení na aktuální stránce. Neexistuje žádná akce vrácení zpět, takže tuto možnost použijte, pouze když jste si jisti, že chcete obnovit stránku. 

- Použijte možnost **importu** k přizpůsobení ze souboru přizpůsobení, které jste vy nebo někdo jiný dříve vytvořili pro tuto stránku. Import přizpůsobení smaže veškerá přizpůsobení, která jste provedli na celé stránce, místo použití všech individuálních nastavení z vybraného souboru. Pokud chcete uložit nebo sdílet přizpůsobení, pak vyberete možnost **exportovat** pro uložení individuálního nastavení do souboru. 

- Zvolte tlačítko **Zavřít** k zavření panelu nástrojů a návratu stránky do jejího předchozího interaktivního stavu. 

Pomocí panelu nástrojů individuálního nastavení je uložení změn implicitní. Vaše individuální nastavení se provádí okamžitě, jakmile je učiníte, a není nutné klepnout tlačítko **Uložit**. V některých případech se zobrazí ikona visacího zámku s prvkem pro výběr nástroje. To znamená, že pokud má stránka pracovat správně, nemůžete měnit vlastnosti související s vybraným nástrojem. Po otevření nástrojů přizpůsobení se stránka stane neinteraktivní. Nelze zadat data nebo rozbalit nebo sbalit oddíly.

## <a name="explicit-personalization-adding-a-tile-or-list-to-a-workspace"></a>Explicitní přizpůsobení: Přidat dlaždici nebo seznam do pracovního prostoru
Některé stránky se seznamy budou mít k dispozici funkci dalšího individuálního nastavení v rámci svého podokna akcí ve skupině **Přizpůsobení** na kartě **Možnosti**. Zvolte možnost **Přidat do pracovního prostoru** a otevřete rozevírací seznam, v němž můžete zobrazit informace v aktuálním seznamu (filtrované a řazené nebo výchozí) v pracovním prostoru jako seznam nebo dlaždici souhrnu (který lze použít k zobrazení počtu položek v seznamu). 

[![Přidat na pracovní prostor](./media/personalization-addtoworkspace.png)](./media/personalization-addtoworkspace.png) 

Chcete-li přidat seznam do pracovního prostoru, nejprve seřaďte nebo filtrujte seznam pomocí informace, kterou chcete zobrazit na svém pracovním prostoru, pak vyberte dialog **Přidat do pracovního prostoru**. Poté vyberte požadovaný pracovní prostor a vyberte **Seznam** z rozevíracího seznamu **Prezentace**. Když vyberete **Seznam**, otevře se dialogové okno, které vám umožní vám vybrat sloupce, které chcete zobrazit v seznamu, a popis pro seznam, jak bude zobrazen v pracovním prostoru. 

Chcete-li přidat dlaždici do pracovního prostoru, nejprve vyfiltrujte seznam představující data, která chcete sumarizovat (nebo k nim mít rychlý přístup). Poté otevřete nabídku dialogového okna **Přidat do pracovního prostoru**. Poté vyberte požadovaný pracovní prostor a vyberte položku **Dlaždice** z rozevíracího seznamu **Prezentace**. Když vyberete **dlaždici**, otevře se dialogové okno, umožňující poskytování dlaždici popiskem, a rozhodnete, zda dlaždice bude zobrazovat počet. Když dlaždici umístíte do pracovního prostoru, dlaždice vám umožní otevírat aktuální stránku pracovního prostoru a zobrazovat seznam informací o dlaždici. 

Až je váš seznam nebo dlaždice přidán do pracovního prostoru, můžete tento pracovní prostor otevírat a měnit pořadí v seznamu nebo na dlaždici v rámci skupiny, se kterou byl uveden.

## <a name="explicit-personalization-adding-a-summary-from-a-workspace-to-a-dashboard"></a>Explicitní přizpůsobení: Přidání součtu z pracovního prostoru do řídicího panelu
Některé pracovní prostory obsahují počet dlaždic (dlaždice s číslicemi), které také chcete zobrazit v řídicím panelu. V pracovním prostoru klikněte pravým tlačítkem na dlaždici s počtem, vyberte **Přizpůsobit** a poté vyberte **Připnout na řídicí panel**. Příště, až budete přicházet (a aktualizovat) do vybraného řídicího panelu, zobrazí se vám v řídicím panelu tento počet pod navigační dlaždicí daného pracovního prostoru.

## <a name="explicit-personalization-personalizing-your-dashboard"></a>Explicitní přizpůsobení: Přizpůsobení řídicího panelu
Řídicí panel je často první stránkou, která se zobrazí při otevření aplikace Finance and Operations. Můžete přizpůsobit řídicí panel k přejmenování vašich navigačních dlaždic pracovního prostoru, aby byly zobrazeny pouze dlaždice, které chcete zobrazit, přejmenovány dlaždice nebo uspořádány v pořadí, v jakém je chcete zobrazit. 

Nastavení řídicího panelu provedete výběrem dlaždice a klepnutím pravého tlačítka myši otevřete kontextovou nabídku. V kontextové nabídce vyberte **Přizpůsobit**. Pokud vybranou dlaždici chcete skrýt, přejmenovat nebo přeskočit, můžete provést tuto změnu přímo v okně vlastností, které se objevilo. Pokud chcete uspořádat dlaždice, vyberte možnost **Přizpůsobit tento formuláře** v okně Vlastnosti a otevřete panel nástrojů Přizpůsobení. Dlaždice můžete uspořádat pomocí nástroje **Přesun**.

## <a name="administration-of-personalization"></a>Správa přizpůsobení
Poté, co jste přizpůsobili stránku, můžete svá individuální nastavení sdílet s dalšími uživateli prostřednictvím exportu přizpůsobené stránky. Poté můžete požádat jiné uživatele, aby přešli na stránku individuálního nastavení a naimportovali soubor individuálního nastavení, který jste vytvořili, nebo můžete poskytnout své individuální nastavení uživateli, který má oprávnění správce a může použít váš soubor individuálního nastavení pro více uživatelů najednou.

Uživatelé, kteří mají oprávnění správce, také mohou spravovat přizpůsobení ostatních uživatelů na stránce **Nastavení přizpůsobení**. Tato stránka obsahuje čtyři karty: 

- **Použít** – můžete importovat nebo zvolit individuální nastavení pro jednoho nebo více uživatelů. Chcete-li použít individuální nastavení pro jednoho nebo více uživatelů, zvolte roli a uživatele v rámci této role. Poté zvolte existující individuální nastavení nebo naimportujte soubor individuálního nastavení k použití na vybrané uživatele.  Přizpůsobení bude ověřeno a použito pro všechny vybrané uživatele, když příště otevřou vybrané stránky.

- **Vymazat** – můžete vymazat přizpůsobení stránky nebo pracovního prostoru pro jednoho nebo více uživatelů. Vyberte stránku a zobrazte seznam uživatelů, kteří si přizpůsobili tuto stránku. Poté vyberte uživatele, kteří by měli mít individuální nastavení pro tuto stránku odstraněno, a vyberte **Vymazat**. Všechna přizpůsobení, která vybraní uživatelé použili u vybrané stránky nebo pracovního prostoru, se smažou. Tuto akci nelze vrátit zpět. Pokud má však stránka nebo pracovní prostor uložené přizpůsobení, lze toto přizpůsobení opět importovat.

- **Manažer podle uživatele** – vyberte uživatele a zobrazte seznam stránek, pro které má tato osoba individuální nastavení.  Poté můžete povolit nebo zakázat jejich možnost přizpůsobení pro specifické stránky nebo pro celý systém.  Rovněž můžete vymazat, importovat nebo exportovat individuální nastavení pro tohoto uživatele.

- **Systém:** – Zde můžete dočasně zakázat veškerá přizpůsobení v systému pro všechny uživatele. Takový krok neodstraní individuální nastavení, ale pouze obnoví všechny stránky pro všechny uživatele do výchozího stavu. Pokud později znovu povolíte přizpůsobení, veškerá přizpůsobení budou znovu použita. Můžete trvale odstranit veškerá přizpůsobení v systému pro všechny uživatele. Ujistěte se, že vyexportujete veškerá individuální nastavení, která byste později mohli chtít, předtím, než provedete tento krok. Později už nebude možnost odstraněná individuální nastavení obnovit. 

## <a name="personalization-of-inventory-dimensions"></a>Přizpůsobení dimenzí zásob

Když si přizpůsobíte nastavení dimenze zásob na stránce, zvažte nastavení, která byla vytvořena pomocí možnosti **Zobrazení dimenzí**. Například když použijete přizpůsobení ke skrytí sloupce pro dimenzi čísla skladové dávky a sloupec se zobrazí při příštím otevření stránky, může to být proto, že nastavení zobrazení dimenze ovládá, které sloupce dimenze zásob se zobrazí. 

Nastavení zobrazení dimenzí platí pro všechny stránky a tato nastavení přepíší všechny individuální nastavení polí dimenze zásob na jednotlivých stránkách. 

Například pomocí dimenze čísla skladové dávky by tato dimenze musela být vymazána jako součást možnosti **Zobrazení dimenzí**, aby tato tabulka nezobrazovala tento sloupec. Tato změna by nakonec neplatila pouze pro jednu konkrétní stránku, ale pro všechny stránky.

