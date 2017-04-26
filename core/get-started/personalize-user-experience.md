---
title: "Individuální nastavení prostředí uživatele"
description: "Tento článek vysvětluje, jak lze přizpůsobit 365 Microsoft Dynamics pro operace."
author: RobinARH
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: SysUserSetup
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 62363
ms.assetid: 57b445d7-3e9e-4228-8728-f63b9dbd77a3
ms.search.region: Global
ms.author: tlefor
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 4bb647cfd3f012efbffa93a81462c538a24ac850
ms.openlocfilehash: 8965c193839002776b3c61036b23b54625c974a4
ms.lasthandoff: 03/31/2017


---

# <a name="personalize-the-user-experience"></a>Individuální nastavení prostředí uživatele

[!include[banner](../includes/banner.md)]


Tento článek vysvětluje, jak lze přizpůsobit 365 Microsoft Dynamics pro operace.

Existuje mnoho typů přizpůsobení v 365 Microsoft Dynamics pro operace. Některá přizpůsobení jsou výběry, které byly vytvořeny v seznamu voleb na stránce nastavení. Implicitní některé individuální nastavení, například Dynamics 365 operací uchovává informace o šířku sloupců mřížky Pokud upravíte a rozbalený sbalený stav záložky s náhledem. Jiná přizpůsobení jsou explicitní. Pro explicitní přizpůsobení zadejte režim interaktivního přizpůsobení a upravte vzhled stránky přímo řízením způsobu, jakým se elementy zobrazují či reagují na stránce. 

Všechny individuální nastavení libovolného typu, které uživatel provede v 365 Dynamics pro operace jsou pro daného uživatele, bez ohledu na společnost, který interakci uživatele s. Změny, které uživatel provede na stránce neovlivní ostatní uživatelé v systému.

## <a name="systemwide-options-for-the-current-user"></a>Systémové možnosti pro aktuálního uživatele
Navigační panel obsahuje obrázek ozubeného kola, který se nazývá tlačítko nabídky **Nastavení**. Při otevírání nabídky **Nastavení** se zobrazí počet voleb. Při výběru **Možnosti** se uživateli otevře stránka **Možnosti**. Zde naleznete těchto čtyřech možnosti karet: **Vizuální vlastnosti**, **Předvolby**, **Účet** a **Workflow**.

-   **Vizuální vlastnosti: **Vyberte motiv barvy a výchozí velikost prvků vašich stránek.
-   **Předvolby:** Zde můžete vybrat výchozí hodnoty pro každé spuštění 365 Dynamics pro operace, včetně společnosti, úvodní stránky a výchozí režim zobrazení nebo úpravy (která určuje, pokud stránky je uzamčen pro zobrazení nebo otevřít pro úpravy při každém otevření). Naleznete zde také jazyk, časové pásmo a datum, čas a možnosti formátu čísel. Nakonec tato stránka obsahuje číslo různých předvoleb, které se liší od dílčí verze.
-   **Účet: **Je používán k poskytování ID uživatele a ostatních možností vztahujících se k účtu.
-   **Workflow: **Zde volíte možnosti týkající se workflowu.

## <a name="implicit-personalizations"></a>Implicitní individuální nastavení
Implicitní individuální nastavení jsou ta přizpůsobení, která provádíte pouhou spoluprací s některými ovládací prvky, které pamatují jejich aktuální viditelný stav. 

**Sloupce mřížky:** Šířku sloupce v seznamu můžete upravit výběrem na ukazateli velikosti vlevo nebo vpravo od záhlaví a jeho posunem doleva nebo doprava na požadovanou šířku. Dynamics 365 pro operace uloží šířku chcete vytvořit a zobrazit tuto šířku sloupce při každém otevření stránky seznamu. 

**Pevné záložky:** Některé stránky mají možnost rozbalení oddílů, kterým se říká pevné záložky. Dynamics 365 pro operace bude ukládat záložky, které jste rozbalili a záložky, které jsou sbaleny. Vždy, když se vrátíte na stránku, stejné pevné záložky bude rozbalené nebo sbalené podle jejich posledního použití. V tomto článku si vysvětlíme, jak změnit pořadí oddílů pevných záložek. V některých případech sbalení záložky s náhledem můžete zvýšit výkon protože 365 Dynamics pro operace nebude nutné načítat informace na této záložce s náhledem, dokud je rozšířena záložce s náhledem. 

**Okna s fakty:** Některé stránky obsahují oddíl s názvem podokna oken s fakty. Toto podokno obsahuje jen informace pro čtení související s aktuálním předmětem stránky. Každý oddíl v podokně okna s fakty se nazývá okno s fakty. Můžete rozbalit nebo sbalit pole faktů a 365 Dynamics pro operace uloží vaše preference. V některých případech sbalení skutečnost políčka může zlepšit výkon protože 365 Dynamics pro operace nemusí načíst informace pro pole tuto skutečnost, dokud pole skutečnost je rozbalen.

## <a name="explicit-personalizations-using-the-personalization-toolbar"></a>Explicitní přizpůsobení za použití panelu nástrojů přizpůsobení.
Každý osoba a společnost má jinou perspektivu, která data jsou pro ně nejdůležitější, nebo která data nejsou potřebná pro způsob, jakým spouštějí svá obchodní data. Schopnost přizpůsobit způsob, jakým vaše informace jsou objednané, několik druhů vzájemně působících s nebo dokonce skryté je klíčem k tvorbě 365 Dynamics pro operace zkušenost osobní a užitkové. 

Individuální nastavení explicitní jsou tyto individuální nastavení explicitně provádět s úmyslem změnit vzhled nebo chování prvku nebo stránky, volba přizpůsobení nabídky. Nejzákladnějším typem explicitní přizpůsobení je kde prvku klepněte pravým tlačítkem myši a vyberte **přizpůsobit**. (Všimněte si, že ne všechny prvky na stránce mohou být přizpůsobována.) Vyberete-li tuto metodu přizpůsobení, se zobrazí okno Vlastnosti prvku. 

[![Přizpůsobení vlastností prvku](./media/personalization-element-properties.jpg)](./media/personalization-element-properties.jpg) 

Prvek na vaší stránce přizpůsobíte tímto způsobem: pokud jednoduše chcete změnit popisek prvku, skrýt prvek tak, aby nebyl zobrazen na stránce (to nezmění všechna data, jednoduše se vám nezobrazí informace), včetně informací v oddílu souhrnu pevné záložky (pokud je prvek v pevné záložce), při použití tabulátoru vynechejte pole nebo to zařiďte tak, aby nemohla být data změněna jeho označením jako „Neupravovat“. 

Pokud chcete přesunout nebo skrýt prvky nebo provést několik změn, můžete použít nástroj individuálního nastavení, který je k dispozici v okně Vlastnosti prvků výběrem **Přizpůsobit tento formulář**. Panel nástrojů přizpůsobení je také dostupný na podokno akcí formuláře, pod skupinou přizpůsobení karty **Možnosti**. Vyberte **přizpůsobit tento formulář** a zobrazí se vám panel nástrojů přizpůsobení. 

[![Přizpůsobení panelu nástrojů](./media/personalization-personalizationtoolbar.jpg)](./media/personalization-personalizationtoolbar.jpg)

Přizpůsobení panelu nástrojů má číslo přizpůsobení akcí. Zvolte nástroj **Vybrat**, pokud chcete vybrat a změnit vlastnosti mnoha prvků po jednom. Za prvé, klepněte na nástroj Vybrat a pak klepněte na prvek, jehož vlastnosti chcete upravit. Při výběru prvku se otevře okno vlastností prvku a můžete upravit jakékoli vlastnosti pro daný prvek. Proces můžete opakovat další prvky formuláře, které je možné přizpůsobit. V některých případech po výběru prvku a uvidíte, že některé vlastnosti nelze měnit. To znamená, že na základě způsobu aktuální prvek je použit, 365 Dynamics pro operace nelze umožňují měnit vlastnosti. Nemůžete například skrýt pole, které je požadováno. 

Zvolte nástroj pro **Přesunutí**, pokud chcete vybrat a přesunout prvek na jiné místo v rámci aktuální skupiny prvků. (Prvek nelze přesunout mimo nadřazenou skupinu). Za prvé, klepněte na nástroj Přesunout a pak klepněte na prvek, který chcete přesunout. Po klepnutí na prvek, který chcete přesunout, 365 Dynamics pro operace bude naskenujte formulář pochopit, kde se tento prvek lze přesunout a vytvořit řadu "drop zóny", která zobrazí jako barevný, tučný řádek u oblasti, kde možné přetáhnout prvek a přetáhněte element na aktuální skupinu kolem. 

Chcete-li provést výběr a skrýt prvek, zvolte možnost **skrýt**. Ke skrytí prvku stačí vybrat nástroj Skrýt a klepnout na prvek, který se má skrýt. Vyberete-li nástroj skrytí, nyní všechny skryté prvky budou viditelné a zobrazené v šedém kontejneru, takže můžete vybrat prvek, který chcete zobrazit. Zvolte nástroj pro výběr, aby jste si prohlédnuli stránku s vybranými skrytými prvky. Zvolte nástroj **Souhrn**, pokud chcete v pevné záložce v oblasti souhrnu zobrazit číslo nebo pole řetězců. Nástroj Souhrn platí pouze pro pole, která jsou obsažena v pevné záložce oddílu. Při výběru nástroj souhrnné Dynamics 365 pro operace se zobrazí všechna pole, která byla vybrána jako souhrnné pole jejich uzavřením do šedě kontejneru. Klepnutím na pole můžete interaktivně přidávat a odebírat pole ze pevné záložky shrnutí. 

Zvolte **přeskočit** nástroj pro odebrání prvku z pořadí karta klávesnice na stránce. Při výběru nástroje přeskočit všechny aktuálně přeskočené prvky budou zobrazeny v šedě kontejneru, takže je možné je znovu tak, aby byly součástí sekvence kartu výběrem vynechaných elementu. 

Zvolte nástroj **Upravit**, když chcete označit prvek jako upravitelný nebo neupravitelný. Vyberete-li nástroj úprav, nyní všechny needitovatelné prvky budou zobrazené v šedém kontejneru, takže můžete vybrat ty, který chcete mít editovatelné. Všimněte si, že některá pole jsou povinná a nelze je upravovat. Tato pole se zobrazí s ikonou visacího zámku. 

Zvolte nástroj **přidání** pro přidání pole na stránku. Pomocí nástroje přidávání nelze vytvořit nové pole, ale můžete přidat pole, které jsou součástí aktuální definice stránky, ale nejsou zobrazena na stránce. Vyberete-li nástroj přidání, musíte nejprve vybrat skupinu nebo oblast, kam chcete pole přidat. Dialogové okno zobrazí seznam polí souvisejících s oddílem, který jste vybrali. Z tohoto dialogového okna můžete vybrat jedno či více polí, a klepněte na vložit. Chcete-li později odstranit dříve přidané pole, opakujte tento postup, ale pouze vymažte pole, která jste předtím přidali. 

Zvolte **Správa** tlačítka zobrazíte seznam možností řízení týkající se všechna individuální nastavení pro aktuální stránku. 

Zvolte **vymazat** obnovit na výchozí stránce nainstalovaný stav. Vymaže všechna individuální nastavení na aktuální stránce. Neexistuje žádná akce zpět, takže pouze tuto možnost použijte, když jste si jisti, chcete-li obnovit stránku. 

Použijte možnost **importu** k přizpůsobení ze souboru přizpůsobení, které jste vy nebo někdo jiný dříve vytvořili pro tuto stránku. Import přizpůsobení smaže veškerá přizpůsobení, která jste provedli na celé stránce, místo použití všech individuálních nastavení z vybraného souboru. Pokud chcete uložit nebo sdílet přizpůsobení, pak vyberete možnost **exportovat** pro uložení individuálního nastavení do souboru. 

Zvolte tlačítko **Zavřít** k zavření panelu nástrojů a návratu na stránku do dříve interaktivního stavu. 

Pomocí panelu nástrojů individuálního nastavení je uložení změn implicitní. Vaše individuální nastavení se provádí okamžitě, jakmile je učiníte, a není nutné klepnout tlačítko **Uložit**. V některých případech zobrazí ikona visacího zámku s prvkem při výběru nástroje. To znamená, nelze změnit pořadí stránky pracovat správně, vlastnosti týkající se vybraného nástroje. Po otevření nástrojů přizpůsobení se stránka stane neinteraktivní. Nelze zadat data nebo rozbalit nebo sbalit oddíly.

## <a name="explicit-personalization-adding-a-tile-or-list-to-a-workspace"></a>Explicitní přizpůsobení: Přidat dlaždici nebo seznam do pracovního prostoru
Některé stránky se seznamy mají funkci dalšího přizpůsobení, která je k dispozici v rámci podokna akcí, ve skupině přizpůsobit na kartě Možnosti. Vyberte možnost **Přidat na pracovní prostor** k otevření rozevíracího seznamu, v němž můžete zobrazit informace v aktuálním seznamu (filtrovaném a řazeném nebo výchozím) na pracovní prostor jako seznam nebo dlaždici souhrnu (kterou lze použít pro zobrazení počtu položek v seznamu). 

[![Add to workspace](./media/personalization-addtoworkspace.png)](./media/personalization-addtoworkspace.png) 

Chcete-li přidat seznam do pracovního prostoru, nejprve seřaďte nebo filtrujte seznam pomocí informace, kterou chcete zobrazit na svém pracovním prostoru, pak vyberte dialog Přidat do pracovního prostoru. Poté vyberte požadovaný pracovní prostor a vyberte **seznam** z rozevíracího seznamu prezentace. Když vyberete **seznam**, otevře se dialogové okno, které vám umožní vám vybrat sloupce, které chcete zobrazit v seznamu, a popis pro seznam, jak bude zobrazen v pracovním prostoru. 

Chcete-li přidat dlaždici do pracovního prostoru, nejprve vyfiltrujte seznam představující data, která chcete sumarizovat (nebo k nim mít rychlý přístup). Poté otevřete dialogové okno Přidat do pracovního prostoru. Poté vyberte požadovaný pracovní prostor a vyberte položku **Dlaždice** z rozevíracího seznamu prezentace. Když vyberete **dlaždici**, otevře se dialogové okno, umožňující poskytování dlaždici popiskem, a rozhodnete, zda dlaždice bude zobrazovat počet. Když dlaždici umístíte do pracovního prostoru, dlaždice vám umožní otevírat aktuální stránku pracovního prostoru a zobrazovat seznam informací o dlaždici. 

Až je váš seznam nebo dlaždice přidán do pracovního prostoru, můžete tento pracovní prostor otevírat a měnit pořadí v seznamu nebo na dlaždici v rámci skupiny, se kterou byl uveden.

## <a name="explicit-personalization-adding-a-summary-from-a-workspace-to-a-dashboard"></a>Explicitní přizpůsobení: Přidání součtu z pracovního prostoru do řídicího panelu
Některé pracovní prostory obsahují počet panelů (kameny s čísly na nich), které také chcete zobrazit v řídicím panelu. V pracovním prostoru klepněte pravým tlačítkem myši počet dlaždic a vyberte **přizpůsobit**. Vyberte možnost **Připnout na řídicí panel**. Příště, až budete přicházet (a aktualizovat) do vybraného řídicího panelu, zobrazí se vám v řídicím panelu tento počet pod navigační dlaždicí daného pracovního prostoru.

## <a name="explicit-personalization-personalizing-your-dashboard"></a>Explicitní přizpůsobení: Přizpůsobení řídicího panelu
Řídicí panel je často první stránky, které se zobrazí při otevření 365 Dynamics pro operace. Můžete přizpůsobit řídicí panel k přejmenování vašich navigačních dlaždic pracovního prostoru, aby byly zobrazeny pouze dlaždice, které chcete zobrazit, přejmenovány dlaždice nebo uspořádány v pořadí, v jakém je chcete zobrazit. Nastavení řídicího panelu provedete výběrem dlaždice a klepnutím pravého tlačítka myši otevřete kontextovou nabídku. V kontextové nabídce vyberte **Přizpůsobit**. Pokud vybranou dlaždici chcete skrýt, přejmenovat nebo přeskočit, můžete provést tuto změnu přímo v okně vlastností, které se objevilo. Pokud chcete uspořádat dlaždice, vyberte možnost **Přizpůsobit tento formuláře** v okně Vlastnosti a otevřete panel nástrojů Přizpůsobení. Dlaždice můžete uspořádat pomocí nástroje přesunu.

## <a name="administration-of-personalization"></a>Správa přizpůsobení
Je možné přizpůsobit stránku a sdílet ji s jinými uživateli jednoduše exportem přizpůsobené stránky a požádáním ostatních uživatelů o navigaci na přizpůsobenou stránku a importem přizpůsobeného souboru, který jste vytvořili. Má-li uživatel oprávnění správce, může také spravovat přizpůsobení ostatních uživatelů na stránce **Nastavení přizpůsobení**. Přejděte na stránku b. Na stránce **přizpůsobení** naleznete dvě karty, jednu označenou jako **Systém** a druhou označenou jako ** Uživatelé**. 

**Systém:** Zde můžete dočasně zakázat nebo "vypnout" veškerá přizpůsobení v systému. To neodstraní přizpůsobení, ale resetuje všechny formuláře do výchozího stavu. Můžete později znovu povolit přizpůsobení a mít veškerá přizpůsobení znovu použita pro jednotlivé formuláře uživatelů. Můžete také odstranit veškerá individuální nastavení pro všechny uživatele. Všimněte si, že při odstranění přizpůsobení neexistuje žádný způsob znovu automaticky povolit přizpůsobení ze systému. Před provedením tohoto kroku se ujistěte, že jste provedli export individuálního nastavení, které chcete později importovat. 

**Uživatelé:** Zde se můžete rozhodnout, zda každý uživatel může provádět implicitní nebo explicitní přizpůsobení. Můžete také určit, zda každý uživatel může provést implicitní nebo explicitní individuální nastavení na základě specifického formuláře. Navíc můžete pro každého uživatele importovat, exportovat nebo odstranit přizpůsobení. 

**Poznámka:** V první verzi správa přizpůsobení umožňuje pouze řízení uživatelů na základě uživatelů.




