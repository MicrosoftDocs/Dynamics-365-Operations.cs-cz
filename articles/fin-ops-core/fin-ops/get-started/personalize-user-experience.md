---
title: Přizpůsobení uživatelského prostředí
description: Toto téma vysvětluje, jakým způsobem lze přizpůsobit aplikaci.
author: jasongre
manager: AnnBe
ms.date: 04/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserSetup, DefaultDashboard
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 62363
ms.assetid: 57b445d7-3e9e-4228-8728-f63b9dbd77a3
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d0a995d25cfc5e78cc76dd73ddea2fb8bd904328
ms.sourcegitcommit: cd8a28be0acf31c547db1b8f6703dd4b0f62940c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/14/2020
ms.locfileid: "3260499"
---
# <a name="personalize-the-user-experience"></a>Přizpůsobení uživatelského prostředí

[!include [banner](../includes/banner.md)]

Toto téma vysvětluje, jakým způsobem lze přizpůsobit aplikaci.

Existují tři základní třídy přizpůsobení.

- Individuální nastavení provedené na stránce nastavení. Mezi příklady patří barevný motiv a časové pásmo.
- Individuální nastavení související s použitím stránky. Tato individuální nastavení jsou známá jako *implicitní*. Například systém uchovává informace o šířce sloupců mřížky, upravíte-li je a rozbalíte a sbalíte stav pevné záložky.
- Individuální nastavení, které uživatel provádí ve vzhledu stránky změnou způsobu zobrazení nebo působení prvku na stránce, často prostřednictvím interaktivního režimu individuálního nastavení. Tato individuální nastavení jsou známá jako *explicitní*. Uživatel může například přidat, skrýt nebo změnit uspořádání prvků na stránce.

Všechna individuální nastavení, která uživatel udělá, jsou určena pouze pro daného uživatele, bez ohledu na typ individuálního nastavení nebo společnost, se kterými uživatel pracuje. Změny, které uživatel provede na stránce, neovlivní ostatní uživatelé v systému.

## <a name="system-wide-options-for-the-current-user"></a>Systémové možnosti pro aktuálního uživatele

Stránka **Uživatelské možnosti** obsahuje několik systémových nastavení pro aktuálního uživatele. Chcete-li otevřít stránku **Uživatelské možnosti**, vyberte tlačítko **Nastavení** (symbol ozubeného kola) na navigační panelu a pak vyberte **Uživatelské možnosti**. Stránka **Uživatelské možnosti** má čtyři karty, které obsahují různá uživatelské nastavení:

- **Vizuální** - Vyberte barvu motivu a výchozí velikost prvků na svých stránkách.
- **Předvolby** – Vyberte výchozí hodnoty, které se používají při každém otevření systému. Tyto hodnoty zahrnují společnosti, úvodní stránku a výchozí režim zobrazení/úprav. (Režim zobrazení/úprav určuje, zda je stránka uzamčena pro zobrazení nebo otevřena pro úpravy při každém otevření.) Tato karta také obsahuje možnosti pro jazyk, časové pásmo a datum, čas a formáty čísel. Konečně jsou také na této kartě zahrnuty různé předvolby, které se liší podle verze.
- **Účet**- Upravte jméno uživatele a ostatní možnosti vztahující se k účtu.
- **Workflow** – Vyberte možnosti týkající se workflowu.

Kromě změny uživatelských nastavení můžete také pomocí stránky **Uživatelské možnosti** zobrazit a odstranit data o používání a přizpůsobení. V podokně akcí vyberte **Údaje o využití**.

Když používáte aplikaci, mnoho z vašich voleb se uloží, aby byl systém v budoucnu jednodušší pro vaše použití. Na kartě **Individuální nastavení** můžete zobrazit a spravovat osobní změny provedené na stránkách v systému. Na této kartě můžete také vynulovat vysvětlivky k funkcím (tj. překryvná okna, která zavádějí nové funkce systému). Poté budete znovu upozorněni na dříve nalezené funkce.

> [!NOTE]
> Pokud je funkce [Uložená zobrazení](saved-views.md) zapnutá, můžete zobrazit a spravovat svá individulální nastavení výběrem možnosti **Individuální nastavení** v podokně akcí na stránce **Možnosti uživatele**.

## <a name="implicit-personalizations"></a>Implicitní individuální nastavení

Implicitní individuální nastavení jsou ta přizpůsobení, která provádíte pouhou spoluprací s některými ovládací prvky, které ukládají jejich aktuální viditelný stav.

- **Šířka sloupce mřížky** - Šířku sloupce v mřížce můžete upravit výběrem na ukazateli velikosti vlevo nebo vpravo od záhlaví a jeho posunem doleva nebo doprava na požadovanou šířku sloupce. Aplikace ukládá šířku, kterou jste pro sloupec nastavili. Při příštím otevření stránky obsahující tuto mřížku se pak změní velikost sloupce na tuto šířku.
- **Součty sloupců mřížky** – (k dispozici pouze s povoleným ovládacím prvkem mřížky) Můžete se rozhodnout, zda má být součet zobrazen v dolní části libovolného číselného sloupce mřížky a také bez ohledu na to, zda je zápatí mřížky viditelné. Aplikace ukládá tato data, aby byly tyto předvolby při příštím otevření stránky zapamatovány. Další informace naleznete v tématu [Možnosti mřížky](grid-capabilities.md). 
- **Pevné záložky** - Některé stránky mají možnost rozbalení oddílů, kterým se říká *pevné záložky*. Aplikace ukládá informace o pevných záložkách, které jste rozbalili a sbalili. Když pak příště otevřete stránku, stejné pevné záložky budou buď rozbaleny nebo sbaleny, podle poslední interakce se stránkou. V některých případech můžete zlepšit výkon systému sbalením pevné záložky, protože aplikace nebude muset načítat informace o dané pevné záložce, dokud záložka nebude rozbalena. Jak je vysvětleno dále v tomto tématu, můžete také změnit pořadí pevných záložek na stránce.
- **Pole s fakty** – některé stránky mají podokno **Související informace**, které obsahuje informace určené pouze pro čtení, které souvisejí s aktuálním předmětem stránky. Každý oddíl v podokně **Související informace** je známé jako *Pole s fakty*. Podokno **Související informace** můžete rozbalit nebo sbalit stejně jako jednotlivá okna s fakty. Aplikace tyto předvolby uloží. Potom se při příštím otevření stránky podokno **Související informace** a jednotlivá okna s fakty rozbalí nebo sbalí na základě vaší poslední interakce se stránkou. V některých případech můžete zlepšit výkon systému sbalením okna s fakty, protože aplikace nebude muset načítat informace o dané pevné záložce, dokud okno s fakty nebude rozbaleno.
- **Podokna akcí** – *Podokno akcí* se zobrazí v horní části většiny stránek. Podokno akcí obsahuje tlačítka pro řadu akcí, které lze provést na aktuální stránce. Tato tlačítka jsou často organizována na kartách. Můžete připnout celé otevřené podokno akcí nebo ho můžete mít sbalené ve výchozím nastavení. Když pak příště otevřete stránku, podokno akcí bude otevřeno nebo sbaleno, podle poslední interakce se stránkou. Pokud jste připnuli podokno akcí v otevřeném stavu, zobrazí se poslední použitá karta.
- **QuickFilters** – *QuickFilter* se zobrazuje nad mnohými mřížkami. QuickFilter vám umožní filtrovat mřížku na základě sloupce, který jste vybrali. Aplikace uloží sloupec, který jste vyfiltrovali. Poté při příštím otevření stránky, která obsahuje danou mřížky, bude mřížka vyfiltrována na stejném sloupci. Poté však můžete vybrat jiný sloupec pro filtrování mřížky.
- **Filtry záhlaví sloupce** – Při filtrování mřížky pomocí *filtrů záhlaví sloupce* můžete změnit operátor filtru, pokud potřebujete vyhledat data, která chcete. Lze například změnit operátor z **začíná** na **je přesně**. Při každém použít filtru záhlaví sloupce a změně operátora filtru aplikace uloží změny. Poté se operátor filtru obnoví při příštím filtrování v daném sloupci.
- **Navigační podokno** – Můžete otevřít *navigační podokno* výběrem tlačítka **Rozbalit navigační podokno** vlevo nahoře na každé stránce. (Tomuto tlačítku se někdy říká tlačítko _**nabídky**_, *hamburger*, *hamburgerová nabídka* nebo *hamburgerové tlačítko*.) Navigační podokno můžete připnout v otevřeném stavu nebo ho můžete mít ve výchozím nastavení sbalené. Poté, co je připnuto navigační podokno otevřené, aplikace ho zachová otevřené, dokud ho nesbalíte.

## <a name="explicit-personalizations"></a>Explicitní individuální nastavení

Různí lidé a společnosti mají jiný pohled na data, která jsou pro ně nejdůležitější, a údaje, které nevyžadují pro způsob, jakým provozují svou firmu. Můžete si přesně přizpůsobit způsob, jakým se informace uspořádají a jak s nimi budete nakládat. Můžete také určit, že některé informace mají být skryty. Tyto funkce jsou klíčem k osobní a produktivnímu rozhraní a jsou to příklady explicitního přizpůsobení. Explicitní individuální nastavení jsou taková, která provádíte explicitně, protože chcete změnit vzhled nebo chování prvku nebo stránky.

### <a name="shortcut-menu-options"></a>Možnosti místní nabídky

Místní nabídky umožňují několik způsobů explicitně změnit stránku, aby odpovídala vašim požadavkům, nebo požadavkům vaší společnosti. (Místní nabídka se také nazývá *nabídka pravého tlačítka myši* nebo *kontextové nabídka*.)

Nejtypičtější a nejdůležitější změny, které lze na stránce provést, jsou k dispozici přímo jako možnosti místní nabídky. Například od aktualizace Platform Update 17 můžete přidat nebo skrýt sloupce v mřížce pouhým kliknutím pravým tlačítkem na záhlaví sloupce mřížky a pak vybrat **Přidat sloupce** nebo **Skrýt tento sloupec**.

Kromě toho jsou k dispozici základní typy explicitního přizpůsobení kliknutím pravým tlačítkem myši a následným výběrem **Přizpůsobit**. (Všimněte si, že ne všechny prvky na stránce mohou být přizpůsobeny.) Použijete-li tuto metodu přizpůsobení, zobrazí se okno Vlastnosti prvku.

![Přizpůsobení vlastností prvku](./media/cli-element-property-window.png)

Můžete použít okno vlastností pro individuální nastavení prvku následujícími způsoby:

- Změna popisku prvku.
- Skrytí prvku, takže není zobrazen na stránce. Data v poli nejsou odstraněna nebo upravena. Informace se nezobrazuje na stránce déle.
- Zahrňte informace v oddílu souhrnu pevné záložky (pokud je prvkem o pevná záložka).
- Přeskočte pole, aby nikdy nezískalo výběr při přechodu na stránku.
- Zabraňte úpravě data v poli (pro jakýkoliv záznam).
- Určete pole, které má být požadováno pro zadávání dat. Pokud v tomto poli nebyla zadána žádná hodnota, zobrazí se s červeným ohraničením a hvězdičkou pro označení tohoto stavu. Tato možnost je k dispozici pouze při spuštění ve verzi 10.0.11, když jsou povoleny funkce [Uložená zobrazení](saved-views.md) a **Určit pole, které vyžadují individuální nastavení**.

Okna vlastností mohou obsahovat další možnosti přizpůsobení, v závislosti na prvku. Například okno vlastností pro dlaždici umožňuje promítnout dlaždici do řídicího panelu a okno vlastnosti pro řídicí panel umožňuje vytvořit nový pracovní prostor na tomto řídicím panelu.

### <a name="the-personalization-toolbar"></a>Panel nástrojů individuálních nastavení

Pokud chcete provést více změn stránky nebo provést změny, které nejsou k dispozici prostřednictvím dalších mechanismů (jako je například změna uspořádání prvků), lze použít panel nástrojů **Individuální nastavení**. Chcete-li otevřít panel nástrojů **Individuální nastavení**, proveďte jeden z následujících kroků:

- V okně vlastností prvku vyberte **Přizpůsobit tuto stránku**.
- Vyberte **Přizpůsobit tuto stránku** ve skupině **Přizpůsobit** na kartě **Možnosti** podokna akcí libovolné stránky.
- Na navigačním panelu vyberte tlačítko **nastavení** (symbol ozubeného kola) a pak vyberte volbu **přizpůsobit**.

[![Panel nástrojů individuálních nastavení](./media/restyledPersonalizationToolbar.png)](./media/restyledPersonalizationToolbar.png)

#### <a name="navigating-the-page"></a>Navigace na stránce

Pokud je panel nástrojů **Přizpůsobení** otevřený, je podkladová stránka jen pro čtení (jinými slovy, data nelze upravovat), ale je stále interaktivní. Konkrétně můžete rozbalit nebo sbalit podokno **související informace**, přepnout karty, rozbalit nebo sbalit oddíly stejně, jako obvykle provádíte tyto akce na stránce. Chcete-li použít změnu individuálního nastavení na sbalitelnou část nebo kartu, (například skrýt pevnou záložku), stačí vybrat tlačítko, které se zobrazí vedle sbalitelné části nebo karty, když je na něm zaměřena klávesnice nebo na něj najedete kurzorem myši.

#### <a name="personalization-tools"></a>Nástroje individuálních nastavení

Jsou k dispozici následující nástroje na panelu nástrojů **Přizpůsobení**:

- Použijte nástroj **Vybrat** k výběru a změně vlastností prvku. Chcete-li použít tento nástroj, vyberte na panelu nástrojů tlačítko **vybrat** a pak vyberte požadovaný prvek. Při výběru prvku se otevře okno vlastností prvku a můžete změnit jakékoli vlastnosti pro daný prvek. Proces můžete opakovat pro další prvky, které je možné přizpůsobit na této stránce. Všimněte si, že některé vlastnosti přizpůsobení nemusí být v některých scénářích k dispozici. Nemůžete například zamknout pole, které je povinné.
- Chcete-li skrýt prvek na stránce, zvolte nástroj **Skrýt**. Chcete-li použít tento nástroj, vyberte na panelu nástrojů tlačítko **Skrýt** a pak vyberte požadovaný prvek ke skrytí. Když použijete nástroj **Skrýt**, všechny prvky, které jsou nyní skryté, jsou viditelné a jsou zobrazeny v šedém kontejneru. Poté můžete prvek zviditelnit jeho výběrem. Chcete-li vidět, jak bude stránka vypadat po skrytí prvků, přepněte do jiného nástroje pro individuální nastavení.
- Použijte nástroj **Přidat pole** pro přidání pole na stránku. Použijete-li tento nástroj, můžete přidat pouze pole, která jsou součástí definice stránky. Informace o postupu při vytváření nových polí, které nejsou součástí aktuální definice stránky, naleznete v tématu [Vytvoření a práce s vlastními poli](user-defined-fields.md). Po výběru tlačítka **Přidat pole** na panelu nástrojů je nutné nejprve vybrat skupinu nebo oblast, kam chcete pole přidat. Dialogové okno zobrazí seznam polí souvisejících se zvolenou skupinou nebo oblastí. V dialogovém okně vyberte jedno nebo více polí pro přidání a zvolte **Vložit**. Chcete-li odebrat pole, které jste dříve přidali, opakujte proces, ale v dialogovém okně zrušte výběr pole.
- Zvolte nástroj pro **Přesunutí**, pokud chcete přesunout prvek na jiné místo v rámci aktuální skupiny prvků. Všimněte si, že prvek nelze přesunout mimo nadřazenou skupinu. Chcete-li použít tento nástroj, vyberte na panelu nástrojů tlačítko **Přesunout** a pak vyberte požadovaný prvek k přesunutí. Při výběru prvku aplikace kontroluje stránku a určuje místa, do nichž lze prvek přesunout. Tato umístění se nazývají *zóny přetažení*. Když přetahujete prvek z aktuální skupiny, každá zóna k přetažení je zobrazena jako vybarvená a tučná oblast, kam lze prvek přetáhnout.
- Použijte nástroj **Přeskočit**, chcete-li odebrat prvek z řady karet klávesnic na stránce. Když na panelu nástrojů vyberete tlačítko **Přeskočit**, všechny prvky, které jsou nyní přeskočené, jsou viditelné a jsou zobrazeny v šedém kontejneru. Můžete interaktivně odebrat nebo přidat pole do pořadí polí.
- Použijte nástroj **Zobrazit v záhlaví**, když chcete zobrazit v oddílu souhrnu pevné záložky prvek. Když vyberete na panelu nástrojů tlačítko **Zobrazit v záhlaví**, všechna pole, která byla vybrána jako souhrnná pole, jsou zobrazena v šedém kontejneru. Lze interaktivně přidat pole na souhrn pevné záložky a odstranit pole ze souhrnu pevných záložek výběrem pole.
- Chcete-li určit prvek požadovaný pro zadávání dat, použijte nástroj **Vyžadovat**. Když na panelu nástrojů vyberete tlačítko **Vyžadovat**, všechny prvky, u kterých je vyžadováno individuální nastavení, jsou viditelné a jsou zobrazeny v šedém kontejneru. Pak můžete znovu uričt, aby nevyžadovaly individuální nastavení. Tato možnost je k dispozici pouze v budoucím vydání, když jsou povoleny funkce [Uložená zobrazení](saved-views.md) a **Určit pole, které vyžadují individuální nastavení**.
- Zvolte nástroj **Zamknout**, když chcete označit prvek jako upravitelný nebo neupravitelný. Když na panelu nástrojů vyberete tlačítko **Zamnkout**, všechny prvky, které jsou nyní neupravitelné, jsou viditelné a jsou zobrazeny v šedém kontejneru. Pak je můžete znovu udělat upravitelnými. Všimněte si, že některá pole jsou povinná a nelze je upravovat. Vedle těchto polí se zobrazí symbol visacího zámku.
- Pomocí tlačítka **Přidat aplikaci z Power Apps** vložte aplikaci, která byla vytvořena pomocí Microsoft Power Apps, na stránku. Podrobné informace o tom, jak vložit aplikaci z Power Apps na stránku, získáte v tématu [Vkládání aplikací z Power Apps](embed-power-apps.md). Tato možnost je k dispozici pouze tehdy, je-li zakázána funkce [uložená zobrazení](saved-views.md).  
- Pomocí tlačítka **Přidat aplikaci** vložte aplikaci, která byla vytvořena v Microsoft Power Apps nebo třetí stranou, na stránku.. Tato možnost je k dispozici pouze tehdy, je-li povolena funkce [uložená zobrazení](saved-views.md). 
- Zvolte nástroj **Vymazat**, pokud chcete obnovit výchozí nainstalovaný stav stránky. Vymaže všechna individuální nastavení na aktuální stránce. Neexistuje akce vrácení. Tento nástroj použijte pouze v případě, že jste si jisti, že chcete resetovat stránku.
- Použijte nástroj **Import** k načtení přizpůsobení ze souboru, který jste vy nebo někdo jiný dříve vytvořili pro tuto stránku. Při importu přizpůsobení pro stránku můžete zvolit, zda mají být přidána nebo nahrazena všechna existující přizpůsobení pro danou stránku. Neexistuje akce vrácení. Po importu přizpůsobení je tedy nutné ručně vymazat nebo zrušit všechny požadované změny.
- Použijte nástroj **Export** pro uložení vašeho přizpůsobení stránky do souboru. Individuální nastavení pak můžete sdílet s jinými uživateli. Tito uživatelé musí importovat soubor, který obsahuje vaše přizpůsobení stránky.
- Zvolte tlačítko **Zavřít** k zavření panelu nástrojů **Přizpůsobení** a návratu stránky do jejího předchozího interaktivního stavu.

Při použití panelu nástrojů **Individuální nastavení** se vaše přizpůsobení běžně uplatní, jakmile je provedete. Je-li však funkce [Uložená zobrazení](saved-views.md) zapnutá, musíte individuální nastavení výslovně uložit do zvoleného zobrazení.

V některých případech se zobrazí ikona visacího zámku s prvkem pro výběr nástroje. Tento symbol označuje, že nemůžete změnit vlastnosti prvku, které se vztahují k vybranému nástroji, protože změny těchto vlastností zabrání tomu, aby stránka fungovala správně.

### <a name="adding-a-tile-list-or-link-to-a-workspace"></a>Přidání dlaždice, seznamu nebo odkazu do pracovního prostoru

U některých stránek, které obsahují seznamy, je funkce individuálního nastavení **Přidat do pracovního prostoru** k dispozici ve skupině **Přizpůsobit** na kartě **Možnosti** v podokně akcí. Tato funkce umožňuje nabízení relevantních informací z aktuálního seznamu do konkrétního pracovního prostoru. Informace zobrazené v pracovním prostoru mohou být založeny buď na celém seznamu, nebo na filtrované a seřazené verzi seznamu. Můžete také určit, zda se informace se zobrazí v pracovním prostoru jako seznam, jako souhrnná dlaždice, která zobrazí počet položek v seznamu, nebo jako odkaz.

> [!NOTE]
> Pokud je zapnutá funkce [Uložená zobrazení](saved-views.md), bude obsah, který zadáte do pracovního prostoru, přímo propojen se zobrazením. Dotaz zobrazení se používá k načtení dat v pracovním prostoru a odpovídající dlaždice nebo odkaz v pracovním prostoru otevře stránku s tímto zobrazením, takže se na něj uplatní dotazy a přizpůsobení zobrazení.

[![Přidat na pracovní prostor](./media/personalization-addtoworkspace.png)](./media/personalization-addtoworkspace.png)

- Chcete-li přidat seznam do pracovního prostoru, nejprve seřaďte nebo filtrujte seznam na stránce tak, aby zobrazoval informace, jak chcete, aby se zobrazovaly v pracovním prostoru. (Pokud je funkce Uložená zobrazení zapnuta, nemůžete pokračovat, dokud neuložíte zobrazení s těmito podmínkami.) Poté vyberte možnost **Přidat do pracovního prostoru**. Vyberte pracovní prostor a potom v poli **Prezentace** zvolte **Seznam**. Po výběru **Konfigurovat** se zobrazí se dialogové okno, kde můžete vybrat sloupce, které se mají zobrazit na seznamu v pracovním prostoru. Můžete také určit popisek použitý pro seznam v pracovním prostoru.
- Chcete-li přidat dlaždici do pracovního prostoru, nejprve vyfiltrujte seznam na stránce, aby ukázal data, která chcete sumarizovat, nebo k nim mít rychlý přístup. (Pokud je funkce Uložená zobrazení zapnuta, nemůžete pokračovat, dokud neuložíte zobrazení s těmito podmínkami.) Poté vyberte možnost **Přidat do pracovního prostoru**. Vyberte pracovní prostor a potom v poli **Prezentace** zvolte **Dlaždice**. Po výběru **Konfigurovat** se zobrazí se dialogové okno, kde můžete určit popisek, který by měl být použit pro dlaždici v pracovním prostoru. Můžete také určit, zda má dlaždice ukazovat počet. Po přidání dlaždice do pracovního prostoru ji můžete vybrat k otevření aktuální stránky z pracovního prostoru. Poté můžete zobrazit filtrovaný seznam, který je spojený s dlaždicí.
- Chcete-li přidat odkaz na pracovní prostor, nejprve filtrujte na stránce seznam tak, aby zobrazoval data, která vás zajímají. (Pokud je funkce Uložená zobrazení zapnuta, nemůžete pokračovat, dokud neuložíte zobrazení s těmito podmínkami.) Poté vyberte možnost **Přidat do pracovního prostoru**. Vyberte pracovní prostor a potom v poli **Prezentace** zvolte **Odkaz**. Po výběru **Konfigurovat** se zobrazí se dialogové okno, kde můžete určit popisek, který se má použít pro odkaz. Můžete také volitelně zadat popisek pro nový oddíl, který bude tento odkaz obsahovat.

Po přidání seznamu, dlaždice nebo odkazu do pracovního prostoru můžete otevřít pracovní prostor a přeuspořádat jeho prvky podle potřeby.

### <a name="adding-a-summary-from-a-workspace-to-a-dashboard"></a>Přidání souhrnu z pracovního prostoru do řídicího panelu

Některé pracovní prostory obsahují dlaždice s početem (tzn. dlaždice s čísly na nich) a můžete také nechat dlaždice zobrazit na řídicím panelu. V pracovním prostoru klikněte pravým tlačítkem na dlaždici s počtem, vyberte **Přizpůsobit** a poté v okně vlastností dlaždice vyberte **Připnout na řídicí panel**. Příště, až budete otevírat (a aktualizovat) vybraný řídicí panel, zobrazí se vám tento počet pod navigační dlaždicí daného pracovního prostoru. Tento počet můžete vybrat pro přechod přímo na data, která reprezentuje.

### <a name="personalizing-your-dashboard"></a>Individuální nastavení řídicího panelu

Řídicí panel je často první stránkou, která se zobrazí při otevření aplikace. Řídicí panel lze přizpůsobit, aby zobrazil pouze dlaždice pracovního prostoru, které chcete zobrazit. Dlaždice můžete také uspořádat tak, aby se zobrazovaly v pořadí, v němž je chcete vidět, přejmenovat navigační dlaždice pracovního prostoru nebo přidat nový pracovní prostor.

Chcete-li přizpůsobit řídicí panel, klikněte pravým tlačítkem na libovolnou dlaždici, a pak vyberte **Přizpůsobit** pro otevření okna vlastností dlaždice.

- Chcete-li vybranou dlaždici skrýt nebo přejmenovat, můžete tuto změnu provést přímo v okně vlastností.
- Pokud chcete přeuspořádat dlaždice pracovního prostoru, vyberte v okně vlastností možnost **Přizpůsobit tuto stránku** a otevřete panel nástrojů **Přizpůsobení**. Dlaždice můžete přeuspořádat pomocí nástroje **Přesun** podle vaší potřeby.
- Chcete-li přidat novou dlaždici pracovního prostoru, v okně vlastností vyberte **Přidat pracovní prostor**. V dolní části řídicího panelu se vytvoří nová dlaždice pracovního prostoru. Tuto novou dlaždici pracovního prostoru můžete přejmenovat, jak chcete. Můžete také přidat seznamy, odkazy a dlaždice do pracovního prostoru, jak je popsáno v části tématu [Přidání seznamů, odkazů nebo dlaždic do pracovního prostoru](#adding-a-tile-list-or-link-to-a-workspace).

## <a name="administration-of-personalizations"></a>Správa přizpůsobení

Poté, co jste přizpůsobili stránku, můžete svá individuální nastavení sdílet s dalšími uživateli prostřednictvím exportu přizpůsobené stránky. Pak můžete požádat ostatní uživatele, aby otevřeli přizpůsobenou stránku a importovali přizpůsobený soubor, který jste vytvořili. Případně můžete dát vaše přizpůsobení uživateli s oprávněními správce. Tento uživatel pak může použít soubor personalizace pro mnoho uživatelů najednou.

Uživatelé, kteří mají oprávnění správce, také mohou spravovat přizpůsobení ostatních uživatelů na stránce **Nastavení přizpůsobení**.

U zákazníků, kteří nezapnuli funkci [Uložená zobrazení](saved-views.md), má tato stránka čtyři karty:

- **Použít** – můžete importovat nebo zvolit individuální nastavení pro jednoho nebo více uživatelů. Chcete-li použít přizpůsobení pro jednoho nebo více uživatelů, nejprve vyberte roli a uživatele, kteří tuto roli mají. Poté buď vyberte existující personalizaci, která se bude vztahovat na vybrané uživatele, nebo importovat soubor personalizace. Přizpůsobení bude ověřeno a použito pro všechny vybrané uživatele, když příště otevřou vybrané stránky.
- **Vymazat** – Můžete vymazat všechna přizpůsobení stránky nebo pracovního prostoru pro jednoho nebo více uživatelů. Nejprve vyberte stránku nebo pracovní prostor, aby se zobrazil seznam uživatelů, kteří u nich provedli individuální nastavení. Poté vyberte uživatele, kteří by měli mít individuální nastavení pro tuto stránku nebo pracovní prostor odstraněno, a vyberte **Vymazat**. Všechna přizpůsobení, která vybraní uživatelé použili u vybrané stránky nebo pracovního prostoru, se smažou. Tuto akci nelze vrátit zpět. Pokud však byla personalizace uložena pro stránku nebo pracovní prostor, může být tato personalizace znovu importována.
- **Uživatelé** – vyberte uživatele a zobrazte seznam stránek, pro které má uživatel individuální nastavení. Pak můžete zapnout možnost zvoleného uživatele zapnout nebo vypnout přizpůsobení pro specifické stránky nebo pro celý systém. Rovněž můžete vymazat, importovat nebo exportovat individuální nastavení pro uživatele. Kromě toho můžete vynulovat vysvětlivky k funkcím pro uživatele. V takovém případě, pokud uživatel předtím odstranil všechna překryvná okna, která zavádějí nové funkce, zobrazí se znovu při příštím výskytu těchto funkcí uživatelem.
- **Systém:** – Zde můžete dočasně vypnout přizpůsobení v systému pro všechny uživatele. V tomto případě budou všechna individuální nastavení odstraněna pro všechny uživatele a všechny stránky budou obnoveny do výchozího stavu. Pokud později zapnete přizpůsobení znovu, veškerá přizpůsobení budou znovu použita. Můžete trvale odstranit veškerá přizpůsobení v systému pro všechny uživatele. Neexistuje žádný způsob obnovení individuálního nastavení, které bylo odstraněno. Proto se před provedením tohoto úkolu ujistěte, že jste exportovali všechna individuální nastavení, která můžete chtít později.

Pro zákazníky, kteří zapnuli funkci [Uložená zobrazení](saved-views.md), nabízí stránka **Individuální nastavení** pět karet:

- **Publikovaná zobrazení** – tato zobrazení byla publikována ve vaší organizaci. Chcete-li změnit uživatele, kteří jsou cílem těchto zobrazení, můžete změnit role zabezpečení nebo právnické osoby, které jsou přidruženy k jednotlivým zobrazením. Můžete také exportovat nebo odstranit jedno nebo více publikovaných zobrazení.
- **Nepublikovaná zobrazení** – tato zobrazení jsou náhledy šablon, které byly importovány do systému, ale ještě nebyly publikovány. Tato zobrazení můžete publikovat, exportovat nebo odstranit.
- **Osobní zobrazení** – tato zobrazení byla vytvořena uživateli v systému. Do organizace můžete publikovat osobní zobrazení nebo je zkopírovat z jednoho či více těchto zobrazení do jiných uživatelů. Tato zobrazení můžete také exportovat nebo odstranit podle potřeby.
- **Uživatelé** – vyberte uživatele a zobrazte seznam stránek, pro které má uživatel individuální nastavení. Pak můžete zapnout možnost zvoleného uživatele zapnout nebo vypnout přizpůsobení pro specifické stránky nebo pro celý systém. Rovněž můžete vymazat, importovat nebo exportovat individuální nastavení pro uživatele. Kromě toho můžete vynulovat vysvětlivky k funkcím pro uživatele. V takovém případě, pokud uživatel předtím odstranil všechna překryvná okna, která zavádějí nové funkce, zobrazí se znovu při příštím výskytu těchto funkcí uživatelem.
- **Systém:** – Zde můžete dočasně vypnout přizpůsobení v systému pro všechny uživatele. V tomto případě budou všechna individuální nastavení odstraněna pro všechny uživatele a všechny stránky budou obnoveny do výchozího stavu. Pokud později zapnete přizpůsobení znovu, veškerá přizpůsobení budou znovu použita. Můžete trvale odstranit veškerá přizpůsobení v systému pro všechny uživatele. Neexistuje žádný způsob obnovení individuálního nastavení, které bylo odstraněno. Proto se před provedením tohoto úkolu ujistěte, že jste exportovali všechna individuální nastavení, která můžete chtít později.

Uživatelé, kteří mají přístup na stránku **Individuální nastavení**, mohou také importovat osobní zobrazení nebo zobrazení šablony pomocí tlačítka **Importovat zobrazení** v podokně akcí.

## <a name="personalizing-inventory-dimensions"></a>Individuální nastavení dimenzí zásob

Když si přizpůsobíte nastavení dimenze zásob na stránce, zvažte nastavení, která byla vytvořena pomocí možnosti **Zobrazení dimenzí**. Například používáte přizpůsobení ke skrytí sloupce pro dimenzi čísla skladové dávky, ale sloupec se objeví při příštím otevření stránky K tomu dochází, protože nastavení **Zobrazení dimenzí** kontroluje dimenze zásob, které jsou zobrazeny. Nastavení **Zobrazení dimenzí** platí pro všechny stránky a přepíše všechna individuální nastavení polí dimenze zásob na jednotlivých stránkách.

V předchozím příkladu, pokud nechcete, aby se zobrazil sloupec dimenze zásob čísla dávky na stránce, musíte tuto dimenzi vymazat jako součást volby **Zobrazení dimenzí** pro tuto stránku.
