---
title: "Přizpůsobení uživatelského prostředí"
description: "Toto téma vysvětluje, jakým způsobem lze přizpůsobit aplikaci Microsoft Dynamics 365 for Finance and Operations."
author: TLeforMicrosoft
manager: AnnBe
ms.date: 05/24/2018
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
ms.sourcegitcommit: 862bbf4d1d9b0dc2b6dc418ee766ed4dedef49fe
ms.openlocfilehash: 8ad5bd607f08d4e0b266d86a96a0b7f3e352c4cd
ms.contentlocale: cs-cz
ms.lasthandoff: 05/24/2018

---

# <a name="personalize-the-user-experience"></a>Přizpůsobení uživatelského prostředí

[!include [banner](../includes/banner.md)]

Toto téma vysvětluje, jakým způsobem lze přizpůsobit aplikaci Microsoft Dynamics 365 for Finance and Operations.

V aplikaci Finance and Operations existují tři základní třídy individuálních nastavení. 
- Individuální nastavení provedené na stránce nastavení. Mezi příklady patří barevný motiv a časové pásmo.
- Individuální nastavení týkající se využití stránky, kterému se říká *implicitní*. Například aplikace Finance and Operations uchovává informace o šířce sloupců mřížky, upravíte-li je a rozbalíte a sbalíte stav pevné záložky. 
- Individuální nastavení, které uživatel provádí pro úpravu vzhledu stránky změnou způsobu zobrazení nebo působení prvku na stránce, často prostřednictvím interaktivního režimu individuálního nastavení. Tato individuální nastavení se nazývají *explicitní*. Uživatel může například přidat, skrýt nebo změnit pořadí prvků na stránce.

Všechna individuální nastavení, která uživatel v aplikaci Finance and Operations udělá, jsou určena pouze pro daného uživatele, bez ohledu na typ individuálního nastavení nebo společnost, se kterými uživatel pracuje. Změny, které uživatel provede na stránce, neovlivní ostatní uživatelé v systému.

## <a name="system-wide-options-for-the-current-user"></a>Systémové možnosti pro aktuálního uživatele
Stránka **Uživatelské možnosti** obsahuje několik systémových nastavení pro aktuálního uživatele. Chcete-li otevřít stránku **Uživatelské možnosti**, vyberte nabídku **Nastavení** (symbol ozubeného kola) na navigační panelu a pak vyberte **Uživatelské možnosti**. Stránka **Uživatelské možnosti** má čtyři karty, které obsahují různá uživatelské nastavení:

- **Vizuální** - Vyberte barvu motivu a výchozí velikost prvků na svých stránkách.
- **Předvolby** – Vyberte výchozí hodnoty, které se používají při každém otevření aplikace Finance and Operations. Tyto hodnoty zahrnují společnosti, úvodní stránku a výchozí režim zobrazení/úprav. (Režim zobrazení/úprav určuje, zda je stránka uzamčena pro zobrazení nebo otevřena pro úpravy při každém otevření.) Tato karta také obsahuje možnosti pro jazyk, časové pásmo a datum, čas a formát čísel. Konečně jsou také na této kartě zahrnuty různé předvolby, které se liší podle verze.
- **Účet**- Upravte jméno uživatele a ostatní možnosti vztahující se k účtu.
- **Workflow** – Vyberte možnosti týkající se workflowu.

## <a name="implicit-personalizations"></a>Implicitní individuální nastavení
Implicitní individuální nastavení jsou ta přizpůsobení, která provádíte pouhou spoluprací s některými ovládací prvky, které pamatují jejich aktuální viditelný stav.

- **Sloupce mřížky** - Šířku sloupce v mřížce můžete upravit výběrem na ukazateli velikosti vlevo nebo vpravo od záhlaví a jeho posunem doleva nebo doprava na požadovanou šířku sloupce. Finance and Operations ukládá šířku, kterou jste pro sloupec nastavili. Změní pak sloupec na tuto šířku pokaždé, když otevřete stránku, která obsahuje dané tuto mřížku.
- **Pevné záložky** - Některé stránky mají možnost rozbalení oddílů, kterým se říká *pevné záložky*. Finance and Operations ukládá informace o pevných záložkách, které jste rozbalili a sbalili. Pokaždé, když se vrátíte na stránku, stejné pevné záložky budou buď rozbaleny nebo sbaleny, podle poslední interakce se stránkou. V některých případech můžete zlepšit výkon systému sbalením pevné záložky, protože aplikace Finance and Operations nebude muset načítat informace o dané pevné záložce, dokud záložka nebude rozbalena. Jak bude vysvětleno dále v tomto tématu, můžete také změnit pořadí pevných záložek na stránce.
- **Okna s fakty** - Některé stránky obsahují oddíl s názvem *okna s fakty*. Toto podokno obsahuje jen informace pro čtení související s aktuálním předmětem stránky. Každý oddíl v podokně okna s fakty se nazývá *okno s fakty*. Lze skrýt nebo zobrazit celé podokno s fakty a lze rozbalit nebo sbalit jednotlivá okna s fakty. Finance and Operations ukládá vaše předvolby. Pokaždé, když se vrátíte na stránku, stav podokna okna s fakty a jednotlivá okna s fakty budou obnovena podle poslední interakce se stránkou. V některých případech můžete zlepšit výkon systému sbalením okna s fakty, protože aplikace Finance and Operations nebude muset načítat informace o oknu s fakty, dokud okno s fakty nebude rozbaleno.
- **Podokna akcí** – *Podokno akcí* se zobrazí v horní části většiny stránek. Podokno akcí obsahuje tlačítka pro řadu akcí, které lze provést na aktuální stránce. Tato tlačítka jsou často organizována na kartách. Můžete připojit otevřené celé podokno akcí, nebo ho můžete mít sbaleno ve výchozím nastavení. Poté při příštím otevření stránky Finance and Operations obnoví připnutý stav podokna akcí. Pokud je podokno akcí připnuto otevřené, Finance and Operations zobrazí také naposledy použitou kartu akcí.
- **QuickFilters** – *QuickFilter* se zobrazuje nad mnohými mřížkami. QuickFilter vám umožní filtrovat mřížku na základě sloupce, který jste vybrali. Finance and Operations ukládá sloupec, kterou jste vyfiltrovali. Poté při příštím otevření stránky, která obsahuje danou mřížky, bude mřížka vyfiltrována na stejném sloupci. Poté však můžete filtrovat na mřížku na jiný sloupec.
- **Filtry záhlaví sloupce** – Při filtrování mřížky pomocí *filtrů záhlaví sloupce* můžete změnit operátor filtru, pokud potřebujete vyhledat data, která chcete. Lze například změnit operátor z **začíná** na **je přesně**. Při každém použít filtru záhlaví sloupce a úpravě operátoru filtru Finance and Operations uloží změny. Poté se obnoví operátor filtru při příštím filtrování na v daném sloupci.
- **Navigační podokno** – Můžete otevřít *Navigační podokno* výběrem tlačítka **Nabídka** tlačítko v levé části každé stránky. (Tlačítku **Nabídka** se někdy říká *hamburger*, *hamburger nabídka*, nebo *hamburger tlačítko*.) Můžete připojit navigační podokno otevřené nebo ho můžete mít ve výchozím nastavení sbalené. Poté, co je připnuto navigační podokno otevřené, Finance and Operations ho zachová otevřené, dokud ho nesbalíte.

## <a name="explicit-personalizations"></a>Explicitní individuální nastavení
Různí lidé a společnosti mají jiný pohled na data, která jsou pro ně nejdůležitější, nebo údaje, které nevyžadují pro způsob, jakým provozují svou firmu. V aplikaci Finance and Operations můžete si můžete ušít na míru způsob, jakým se informace uspořádají a jak s nimi budete nakládat. Můžete také určit, že některé informace mají být skryty. Tyto funkce jsou klíčem k osobní a produktivnímu rozhraní a jsou to příklady explicitního přizpůsobení. Explicitní individuální nastavení jsou taková, která provádíte explicitně s úmyslem změnit vzhled nebo chování prvku nebo stránky.

### <a name="shortcut-menu-options"></a>Možnosti místní nabídky
Místní nabídky umožňují několik způsobů explicitně změnit stránku, aby odpovídala vašim požadavkům, nebo požadavkům vaší společnosti. (Místní nabídka se také nazývá *nabídka pravého tlačítka myši* nebo *kontextové nabídka*.)

Nejtypičtější a nejdůležitější změny, které lze na stránce provést, jsou k dispozici přímo jako možnosti místní nabídky. Například můžete přidat nebo skrýt sloupce v mřížce pouhým kliknutím pravým tlačítkem na záhlaví sloupce mřížky a pak vybrat **Přidat sloupce** nebo **Skrýt tento sloupec**.

Kromě toho jsou k dispozici základní typy explicitního přizpůsobení kliknutím pravým tlačítkem myši a následným výběrem **Přizpůsobit**. (Všimněte si, že ne všechny prvky na stránce mohou být přizpůsobeny.) Použijete-li tuto metodu přizpůsobení, zobrazí se okno Vlastnosti prvku.

[![Přizpůsobení vlastností prvku](./media/personalization-element-properties.jpg)](./media/personalization-element-properties.jpg)

Můžete použít okno vlastností pro individuální nastavení prvku následujícími způsoby:

- Změna popisku prvku.
- Skrytí prvku, takže není zobrazen na stránce. Data v poli nejsou odstraněna nebo upravena. Informace se nezobrazuje na stránce déle.
- Zahrňte informace v oddílu souhrnu pevné záložky (pokud je prvkem o pevná záložka).
- Přeskočte pole, po stisknutí klávesy Tab pro procházení polí na stránce.
- Zabraňte úpravě data v poli (pro jakýkoliv záznam).

Okna vlastností mohou obsahovat další možnosti přizpůsobení, v závislosti na prvku. Například okno vlastností pro dlaždici umožňuje promítnout dlaždici do řídicího panelu a okno vlastnosti pro řídicí panel umožňuje vytvořit nový pracovní prostor na tomto řídicím panelu.

### <a name="the-personalization-toolbar"></a>Panel nástrojů individuálních nastavení
Pokud chcete přesunout nebo skrýt prvky, nebo provést několik změn na stránce, můžete vybrat panel nástrojů **Přizpůsobení**. Chcete-li otevřít panel nástrojů **Přizpůsobení**, vyberte **Přizpůsobit tento formulář** v okně vlastnosti prvku. Můžete také vybrat **Přizpůsobit tento formulář** ve skupině **Přizpůsobit** na kartě **Možnosti** každého podokna akcí.

[![Panel nástrojů individuálních nastavení](./media/personalization-personalizationtoolbar.jpg)](./media/personalization-personalizationtoolbar.jpg)

Když je panel nástrojů **Přizpůsobení** otevřený, stránka není interaktivní. Nelze zadat data nebo rozbalit nebo sbalit oddíly. Lze změnit pouze prvky, které tvoří stránku.

Jsou k dispozici následující nástroje na panelu nástrojů **Přizpůsobení**:

- Použijte nástroj **Vybrat** k výběru a změně vlastností prvku. Zvolte nástroj **Vybrat** a poté vyberte prvek, jehož vlastnosti chcete změnit. Při výběru prvku se otevře okno vlastností prvku a můžete upravit jakékoli vlastnosti pro daný prvek. Proces můžete opakovat pro další prvky, které je možné přizpůsobit na této stránce. Vzhledem k tomu, jakým způsobem jsou některé prvky používány, Finance a Operace vám nedovolí změnit některé z jejich vlastností. Proto při výběru prvku se můžete pravděpodobně setkat s tím, že některé vlastnosti nelze změnit. Nemůžete například skrýt pole, které je povinné.
- Zvolte nástroj pro **Přesunutí**, pokud chcete přesunout prvek na jiné místo v rámci aktuální skupiny prvků. (Prvek nelze přesunout mimo nadřazenou skupinu). Zvolte nástroj **Přesunutí** a poté vyberte prvek, který chcete přesunout. Při výběru prvku Finance and Operations kontroluje stránku a určí, kdy lze přesunout prvek. Poté vytvoří řadu zón k přetažení. Když přetahujete prvek z aktuální skupiny, každá zóna k přetažení je zobrazena jako vybarvená a tučná oblast, kam lze prvek přetáhnout.
- Chcete-li skrýt prvek na stránce, zvolte nástroj **Skrýt**. Zvolte nástroj **Skrýt** a poté vyberte prvek, který chcete skrýt. Když vyberete nástroj **Skrýt**, všechny prvky, které jsou nyní skryté, jsou viditelné a jsou zobrazeny v šedém kontejneru. Poté je lze zrušit jejich skrytí. Výběrem nástroje **Výběr** si můžete prohlédnout, jak bude vypadat stránka s vybranými skrytými prvky.
- Použijte nástroj **Souhrn**, když chcete zobrazit v oddílu souhrnu pevné záložky prvek. Nástroj Souhrn platí pouze pro pole, která jsou obsažena na oddílu pevné záložky. Když vyberete nástroj **Souhrn**, všechna pole, která byla vybrána jako souhrnná pole, jsou zobrazena v šedém kontejneru. Lze interaktivně přidat pole na souhrn pevné záložky a odstranit pole ze souhrnu pevných záložek výběrem pole.
- Použijte nástroj **Přeskočit**, chcete-li odebrat prvek z řady karet klávesnic na stránce. Když vyberete nástroj **Přeskočit**, všechny prvky, které jsou nyní přeskočené, jsou viditelné a jsou zobrazeny v šedém kontejneru. Můžete je pak znovu přidat do řady karet.
- Zvolte nástroj **Upravit**, když chcete označit prvek jako upravitelný nebo neupravitelný. Když vyberete nástroj **Upravit**, všechny prvky, které jsou nyní neupravitelné, jsou viditelné a jsou zobrazeny v šedém kontejneru. Pak je můžete znovu udělat upravitelnými. Všimněte si, že některá pole jsou povinná a nelze je upravovat. Vedle těchto polí se zobrazí symbol visacího zámku.
- Použijte tlačítko **Vložit** a zobrazíte seznam prvků, které lze vložit na stránku.

    - Vyberte nástroj **Pole** pod možností **Vložit** pro přidání pole na stránku. Když použijete nástroj **Pole**, lze přidat pouze pole, která jsou součástí definice stránky, ale nejsou nyní zobrazeny na stránce. Informace o postupu při vytváření nových polí, které nejsou součástí aktuální definice stránky, naleznete v tématu [Vlastní pole](user-defined-fields.md). Po výběru nástroje **Pole** je nutné nejprve vybrat skupinu nebo oblast, kam chcete pole přidat. Dialogové okno zobrazí seznam polí souvisejících se zvolenou skupinou nebo oblastí. V dialogovém okně vyberte jedno nebo více polí pro přidání a zvolte **Vložit**. Chcete-li odebrat pole, které jste dříve přidali, opakujte proces, ale v dialogovém okně zrušte výběr pole.
    - Vyberte nástroj **PowerApp** pod možností **Vložit** a vložte aplikaci vytvořenou pomocí Microsoft PowerApps na stránce. Podrobné informace o tom, jak aplikace PowerApps vkládá na stránku, najdete v tématu [Vložit PowerApps](embed-power-apps.md).

- Zvolte tlačítko **Správa** k zobrazení seznamu možností řízení týkající se všech individuálních nastavení pro aktuální stránku.

    - Zvolte **Vymazat**, pokud chcete obnovit výchozí nainstalovaný stav stránky. Vymaže všechna individuální nastavení na aktuální stránce. Neexistuje akce vrácení. Tuto možnost použijte pouze v případě, že jste si jisti, že chcete resetovat stránku.
    - Použijte možnost **Import** k načtení přizpůsobení ze souboru, který jste vy nebo někdo jiný dříve vytvořili pro tuto stránku. Všechna aktuální přizpůsobení stránky budou nahrazena individuálním nastavením z vybraného souboru.
    - Vyberte **Export** pro uložení vašeho přizpůsobení stránky do souboru. Individuální nastavení můžete sdílet s jinými uživateli. Tito uživatelé musí importovat soubor, který obsahuje vaše přizpůsobení stránky.

- Zvolte tlačítko **Zavřít** k zavření panelu nástrojů **Přizpůsobení** a návratu stránky do jejího předchozího interaktivního stavu.

Když použijete panel nástrojů **Přizpůsobení**, operace ukládání jsou implicitní. Vaše individuální nastavení bude účinné ihned po jeho provedení a není nutné vybírat tlačítko **Uložit**. V některých případech se zobrazí ikona visacího zámku s prvkem pro výběr nástroje. Tento symbol označuje, že nemůžete změnit vlastnosti prvku, které se vztahují k vybranému nástroji, protože změny těchto vlastností zabrání tomu, aby stránka fungovala správně.

### <a name="adding-a-tile-list-or-link-to-a-workspace"></a>Přidání dlaždice, seznamu nebo odkazu do pracovního prostoru
U některých stránek, které obsahují seznamy, je další funkce přizpůsobení k dispozici. Tlačítko **Přidat do pracovního prostoru** ve skupině **Přizpůsobit** na kartě **Možnosti** podokna akcí zobrazuje informace z aktuálního seznamu v konkrétním pracovním prostoru. Můžete zobrazit filtrované a seřazené zobrazení informací v pracovním prostoru nebo můžete zobrazit výchozí zobrazení. Můžete také určit, zda se informace se zobrazí v pracovním prostoru jako seznam, jako souhrnná dlaždice, která zobrazí počet položek v seznamu, nebo jako odkaz.

[![Přidat na pracovní prostor](./media/personalization-addtoworkspace.png)](./media/personalization-addtoworkspace.png)

- Chcete-li přidat seznam do pracovního prostoru, nejprve seřaďte nebo filtrujte seznam na stránce tak, aby zobrazoval informace, jak chcete, aby se zobrazovaly v pracovním prostoru. Pak vyberte **Přidat do pracovního prostoru**. Vyberte pracovní prostor a potom v poli **Prezentace** zvolte **Seznam**. Po výběru **Konfigurovat** se zobrazí se dialogové okno, kde můžete vybrat sloupce, které se mají zobrazit na seznamu v pracovním prostoru. Můžete také určit popisek pro seznam v pracovním prostoru.
- Chcete-li přidat dlaždici do pracovního prostoru, nejprve vyfiltrujte seznam na stránce, aby ukázal data, která chcete sumarizovat, nebo k nim mít rychlý přístup. Pak vyberte **Přidat do pracovního prostoru**. Vyberte pracovní prostor a potom v poli **Prezentace** zvolte **Dlaždice**. Po výběru **Konfigurovat** se zobrazí se dialogové okno, kde můžete určit popisek pro dlaždici v pracovním prostoru. Můžete také určit, zda má dlaždice ukazovat počet. Po přidání dlaždice do pracovního prostoru jej můžete vybrat, chcete-li otevřít aktuální stránku z pracovního prostoru a zobrazit filtrovaný seznam, který je spojen s dlaždicí.
- Chcete-li přidat odkaz na pracovní prostor, nejprve filtrujte na stránce seznam tak, aby zobrazoval data, která vás zajímají. Pak vyberte **Přidat do pracovního prostoru**. Vyberte pracovní prostor a potom v poli **Prezentace** zvolte **Odkaz**. Po výběru **Konfigurovat** se zobrazí se dialogové okno, kde můžete určit popisek pro odkaz. Můžete také volitelně zadat popisek pro nový oddíl, který bude tento odkaz obsahovat.

Po přidání seznamu, dlaždice nebo odkazu do pracovního prostoru můžete otevřít pracovní prostor a uspořádat jeho prvky podle potřeby.

### <a name="adding-a-summary-from-a-workspace-to-a-dashboard"></a>Přidání souhrnu z pracovního prostoru do řídicího panelu
Některé pracovní prostory obsahují dlaždice s početem (tzn. dlaždice s čísly na nich) a můžete také nechat dlaždice zobrazit na řídicím panelu. V pracovním prostoru klepněte pravým tlačítkem na dlaždici s počtem a vyberte **Přizpůsobit**. V okně vlastností dlaždice vyberte **Připnout na řídicí panel**. Příště, až budete otevírat (a aktualizovat) vybraný řídicí panel, zobrazí se vám tento počet pod navigační dlaždicí daného pracovního prostoru. Tento počet můžete vybrat pro přechod přímo na data, která reprezentuje.

### <a name="personalizing-your-dashboard"></a>Individuální nastavení řídicího panelu
Řídicí panel je často první stránkou, která se zobrazí při otevření aplikace Finance and Operations. Řídicí panel lze přizpůsobit, aby zobrazil pouze dlaždice pracovního prostoru, které chcete zobrazit. Dlaždice můžete také uspořádat tak, aby byly v pořadí, v němž je chcete vidět, přejmenovat navigační dlaždice pracovního prostoru nebo přidat zcela nový pracovní prostor.

Chcete-li přizpůsobit řídicí panel, klikněte pravým tlačítkem na libovolnou dlaždici, a pak vyberte **Přizpůsobit** pro otevření okna vlastností dlaždice.

- Chcete-li vybranou dlaždici skrýt nebo přejmenovat, můžete tuto změnu provést přímo v okně vlastností.
- Pokud chcete přeuspořádat dlaždice pracovního prostoru, vyberte v okně vlastností možnost **Přizpůsobit** a otevřete panel nástrojů **Přizpůsobení**. Dlaždice můžete uspořádat pomocí nástroje **Přesun** podle vaší potřeby.
- Chcete-li vytvořit novou dlaždici pracovního prostoru, v okně vlastností vyberte **Přidat pracovní prostor**. V dolní části řídicího panelu se vytvoří nová dlaždice pracovního prostoru. Tuto novou dlaždici pracovního prostoru můžete přejmenovat, jak chcete. Můžete také přidat seznamy, odkazy a dlaždice do pracovního prostoru, jak je popsáno v části tématu [Přidání seznamů, odkazů nebo dlaždic do pracovního prostoru](personalize-user-experience.md#adding-a-tile-list-or-link-to-a-workspace).

## <a name="administration-of-personalization"></a>Správa přizpůsobení
Poté, co jste přizpůsobili stránku, můžete svá individuální nastavení sdílet s dalšími uživateli prostřednictvím exportu přizpůsobené stránky. Pak můžete požádat ostatní uživatele, aby otevřeli přizpůsobenou stránku a importovali přizpůsobený soubor, který jste vytvořili. Případně můžete dát vaše přizpůsobení uživateli s oprávněními správce. Tento uživatel pak může použít soubor personalizace pro mnoho uživatelů najednou.

Uživatelé, kteří mají oprávnění správce, také mohou spravovat přizpůsobení ostatních uživatelů na stránce **Nastavení přizpůsobení**. Tato stránka obsahuje čtyři karty:

- **Použít** – můžete importovat nebo zvolit individuální nastavení pro jednoho nebo více uživatelů. Chcete-li použít přizpůsobení pro jednoho nebo více uživatelů, nejprve vyberte roli a uživatele, kteří tuto roli mají. Poté buď vyberte existující personalizaci, která se bude vztahovat na vybrané uživatele, nebo importovat soubor personalizace. Přizpůsobení bude ověřeno a použito pro všechny vybrané uživatele, když příště otevřou vybrané stránky.
- **Vymazat** – Můžete vymazat všechna přizpůsobení stránky nebo pracovního prostoru pro jednoho nebo více uživatelů. Nejprve vyberte stránku nebo pracovní prostor, aby se zobrazil seznam uživatelů, kteří u nich provedli individuální nastavení. Poté vyberte uživatele, kteří by měli mít individuální nastavení pro tuto stránku nebo pracovní prostor odstraněno, a vyberte **Vymazat**. Všechna přizpůsobení, která vybraní uživatelé použili u vybrané stránky nebo pracovního prostoru, se smažou. Tuto akci nelze vrátit zpět. Pokud však byla personalizace uložena pro stránku nebo pracovní prostor, může být tato personalizace znovu importována.
- **Manažer podle uživatele** – vyberte uživatele a zobrazte seznam stránek, pro které má tato osoba individuální nastavení. Můžete povolit nebo zakázat možnost zvoleného uživatele použít přizpůsobení pro specifické stránky nebo pro celý systém. Rovněž můžete vymazat, importovat nebo exportovat individuální nastavení pro vybraného uživatele.
- **Systém:** – Zde můžete dočasně zakázat veškerá přizpůsobení v systému pro všechny uživatele. V takovém případě se přizpůsobení odstraní. Všechny stránky se resetují na výchozí nastavení pro všechny uživatele. Pokud později znovu povolíte přizpůsobení, veškerá přizpůsobení budou znovu použita. Můžete trvale odstranit veškerá přizpůsobení v systému pro všechny uživatele. Neexistuje žádný způsob obnovení individuálního nastavení, které bylo odstraněno. Proto se před provedením tohoto úkolu ujistěte, že jste exportovali všechna individuální nastavení, která můžete chtít později.

## <a name="personalization-of-inventory-dimensions"></a>Přizpůsobení dimenzí zásob

Když si přizpůsobíte nastavení dimenze zásob na stránce, zvažte nastavení, která byla vytvořena pomocí možnosti **Zobrazení dimenzí**. Například používáte přizpůsobení ke skrytí sloupce pro dimenzi čísla skladové dávky, ale sloupec se objeví při příštím otevření stránky K tomu dochází, protože nastavení **Zobrazení dimenzí** kontroluje dimenze zásob, které jsou zobrazeny.

Nastavení **Zobrazení dimenzí** platí pro všechny stránky a přepíše všechna individuální nastavení polí dimenze zásob na jednotlivých stránkách.

Proto v předchozím příkladu, pokud nechcete, aby se zobrazil sloupec dimenze zásob čísla dávky, musíte tuto dimenzi vymazat jako součást volby **Zobrazení dimenzí** pro tabulku. Tato změna by nakonec neplatila pouze pro jednu konkrétní stránku, ale pro všechny stránky.

