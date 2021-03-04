---
title: Přizpůsobení uživatelského prostředí
description: Toto téma vysvětluje, jakým způsobem lze přizpůsobit aplikaci.
author: jasongre
manager: AnnBe
ms.date: 09/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserSetup, DefaultDashboard
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 62363
ms.assetid: 57b445d7-3e9e-4228-8728-f63b9dbd77a3
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e46c392c43b63ef443f66d8ea8f9e91a9df3d126
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/08/2020
ms.locfileid: "4693225"
---
# <a name="personalize-the-user-experience"></a>Přizpůsobení uživatelského prostředí

[!include [banner](../includes/banner.md)]

Toto téma vysvětluje, jak si můžete přizpůsobit aplikaci, a pokrývá následující témata: 

- **Možnosti pro celý systém** - Tyto možnosti personalizace jsou provedeny na stránce nastavení a jsou dostupné všem uživatelům. Mezi příklady patří barevný motiv a časové pásmo. 
- **Omezený přístup k personalizaci** - Na této úrovni přístupu aplikace automaticky ukládá uživatelské akce spojené s běžným používáním stránky a při příští návštěvě se obnoví. Například aplikace uchovává informace o šířce sloupců mřížky, upravíte-li je a rozbalíte a sbalíte stav pevné záložky. 
- **Úplný přístup k personalizaci** - Na této úrovni přístupu mají uživatelé přístup k veškerým možnostem personalizace v aplikaci. Zejména mají přístup na panel nástrojů **Personalizace**. 
- **Sdílení personalizace** - Uživatelé, kteří mají plný přístup k personalizaci, mohou exportovat personalizace svých stránek a sdílet je s ostatními uživateli.
- **Správa personalizací** - Oprávnění uživatelé mají přístup na stránku pro správu **Personalizace** všech personalizací na úrovni organizace. 

## <a name="system-wide-options-for-the-current-user"></a>Systémové možnosti pro aktuálního uživatele

Stránka **Uživatelské možnosti** obsahuje několik systémových nastavení pro aktuálního uživatele. Tyto možnosti jsou k dispozici všem uživatelům, a to i uživatelům, kteří k personalizaci nemají přístup. Chcete-li otevřít stránku **Uživatelské možnosti**, vyberte tlačítko **Nastavení** na navigační panelu a pak vyberte **Uživatelské možnosti**. Stránka **Uživatelské možnosti** má čtyři karty, které obsahují různá uživatelské nastavení:

- **Vizuální** - Vyberte barvu motivu a výchozí velikost prvků na svých stránkách.
- **Předvolby** – Vyberte výchozí hodnoty, které se používají při každém otevření systému. Tyto hodnoty zahrnují výchozí společnost, úvodní stránku a výchozí režim zobrazení/úprav. (Režim zobrazení/úprav určuje, zda je stránka uzamčena pro zobrazení nebo otevřena pro úpravy při každém otevření.) Tato karta také obsahuje možnosti pro jazyk, časové pásmo a datum, čas a formáty čísel. Konečně jsou také na této kartě zahrnuty různé předvolby, které se liší podle verze.
- **Účet** - Zobrazte nebo upravte jméno uživatele a ostatní možnosti vztahující se k účtu.
- **Workflow** – Vyberte možnosti týkající se workflowu.

Kromě změny uživatelských nastavení můžete také pomocí stránky **Uživatelské možnosti** zobrazit a odstranit data o používání a přizpůsobení. Chcete-li zobrazit svá data o využití, vyberte **Data o použití** v podokně akcí. Na kartě **Individuální nastavení** můžete zobrazit a spravovat osobní změny provedené na stránkách v systému. Na této kartě můžete také vynulovat vysvětlivky k funkcím (tj. překryvná okna, která zavádějí nové funkce systému). Poté budete znovu upozorněni na dříve nalezené funkce.

> [!NOTE]
> Pokud je funkce [Uložená zobrazení](saved-views.md) zapnutá, můžete zobrazit a spravovat svá individulální nastavení výběrem možnosti **Individuální nastavení** v podokně akcí na stránce **Možnosti uživatele**.

## <a name="restricted-personalization-access-formerly-implicit-personalizations"></a>Omezený přístup k personalizaci (dříve implicitní personalizace)

Na úrovni **Omezený přístup k personalizaci** aplikace automaticky ukládá uživatelské akce spojené s běžným používáním stránky a při příští návštěvě se obnoví. Není vyžadována žádná výslovná akce uložení. 

Zde je seznam akcí, které spadají do běžného používání stránky a na které se vztahuje omezený přístup k personalizaci: 

- **Šířka sloupce mřížky** - Šířku sloupce v mřížce můžete upravit výběrem na ukazateli velikosti vlevo nebo vpravo od záhlaví a jeho posunem doleva nebo doprava na požadovanou šířku sloupce. Aplikace ukládá šířku, kterou jste pro sloupec nastavili. Při příštím otevření této stránky se pak změní velikost sloupce na tuto šířku.
- **Součty zápatí a sloupců mřížky** – *(k dispozici pouze se zapnutým ovládacím prvkem mřížky)* Můžete se rozhodnout, zda má být součet zobrazen v dolní části libovolného číselného sloupce mřížky a také bez ohledu na to, zda má být zápatí mřížky viditelné. Aplikace ukládá tato data a použije je při příštím otevření stránky. Další informace naleznete v části [Schopnosti mřížky](grid-capabilities.md). 
- **Pevné záložky** - Některé stránky mají možnost rozbalení oddílů, kterým se říká *pevné záložky*. Aplikace ukládá informace o pevných záložkách, které jste rozbalili nebo sbalili. Když pak příště otevřete stránku, stejné pevné záložky budou buď rozbaleny nebo sbaleny, podle poslední interakce se stránkou. V některých případech můžete zlepšit výkon systému sbalením pevné záložky, protože aplikace nebude muset načítat informace o dané pevné záložce, dokud záložka nebude rozbalena. Jak je vysvětleno dále v tomto tématu, můžete také změnit pořadí pevných záložek na stránce.
- **FactBoxes** – některé stránky mají podokno **Související informace**, které obsahuje informace určené pouze pro čtení, které souvisejí s aktuálním předmětem stránky. Každý oddíl v podokně **Související informace** je známé jako *Okno s fakty*. Podokno **Související informace** můžete rozbalit nebo sbalit stejně jako jednotlivá okna s fakty. Aplikace tyto předvolby uloží. Potom se při příštím otevření stránky podokno **Související informace** a jednotlivá okna s fakty rozbalí nebo sbalí na základě vaší poslední interakce se stránkou. V některých případech můžete zlepšit výkon systému sbalením podokna **Související informace** nebo okna s fakty, protože aplikace nebude muset načítat informace o dané pevné záložce, dokud okno s fakty nebude rozbaleno.
- **Podokna akcí** – *Podokno akcí* se zobrazí v horní části většiny stránek. Podokno akcí obsahuje tlačítka pro řadu akcí, které lze provést na aktuální stránce. Tato tlačítka jsou často organizována na kartách. Můžete *připnout* celé otevřené podokno akcí nebo ho můžete mít sbalené ve výchozím nastavení. Když příště otevřete stránku, podokno akcí bude otevřeno nebo sbaleno, podle poslední interakce se stránkou. Pokud jste připnuli podokno akcí v otevřeném stavu, zobrazí se poslední použitá karta.
- **QuickFilters** – *QuickFilter* se zobrazuje nad mnohými mřížkami. QuickFilter vám umožní filtrovat mřížku na základě jednoho sloupce, který jste vybrali. Aplikace uloží sloupec, který jste vyfiltrovali. Poté při příštím otevření této stránky bude mřížka ve výchozím nastavení vyfiltrována na stejném sloupci. Poté však můžete vybrat jiný sloupec pro filtrování mřížky.
- **Filtry záhlaví sloupce** – Při filtrování mřížky pomocí *filtrů záhlaví sloupce* můžete změnit operátor filtru, pokud potřebujete vyhledat data, která chcete. Lze například změnit operátor z **začíná** na **je přesně**. Při každém použít filtru záhlaví sloupce a změně operátora filtru aplikace uloží změny. Poté se operátor filtru obnoví při příštím filtrování v daném sloupci.
- **Navigační podokno** – Můžete otevřít *navigační podokno* výběrem tlačítka **Rozbalit navigační podokno** vlevo nahoře na každé stránce. (Tomuto tlačítku se někdy říká tlačítko _**nabídky**_, *hamburger*, *hamburgerová nabídka* nebo *hamburgerové tlačítko*.) Navigační podokno můžete připnout v otevřeném stavu nebo ho můžete mít ve výchozím nastavení sbalené. Poté, co je připnuto navigační podokno otevřené, aplikace ho zachová otevřené, dokud ho nesbalíte.

## <a name="full-personalization-access-formerly-explicit-personalizations"></a>Plný přístup k personalizaci (dříve explicitní personalizace)

Na úrovni **Úplný přístup k personalizaci** mají uživatelé přístup k veškerým možnostem personalizace v aplikaci. Protože různí lidé a společnosti mají při interakci s aplikací různé potřeby, zejména pokud jde o využívaná pole, přizpůsobení poskytuje nástroje, které umožňují uživatelům a organizacím přizpůsobit způsob, jakým jsou informace uspořádány a interagovány v aplikaci. Tyto funkce jsou klíčem k poskytování zjednodušených a optimalizovaných zkušeností v aplikaci, které jsou přizpůsobeny vám a vaší organizaci. 

Pokud je zapnutá funkce [Uložená zobrazení](saved-views.md), je k zachování těchto změn uživatelského prostředí pro konkrétní zobrazení vyžadováno explicitní uložení. Pokud je funkce **Uložená zobrazení** vypnutá, tyto změny se automaticky uloží.

Následující oddíly se zabývají rozsahem možností personalizace, které jsou uživatelům k dispozici na úrovni **plný přístup k personalizaci**. Zde je několik příkladů těchto možností:

- Možnosti místní nabídky
- Panel nástrojů **Personalizace**
- Přidání dlaždic, seznamů a odkazů do pracovních prostorů
- Přidání souhrnu z pracovního prostoru do řídicího panelu
- Individuální nastavení řídicího panelu

### <a name="shortcut-menu-options"></a>Možnosti místní nabídky

Místní nabídky umožňují několik způsobů explicitně změnit rozhraní stránky, aby lépe odpovídalo vašim požadavkům, nebo požadavkům vaší organizace. (Místní nabídka se také nazývá *nabídka pravého tlačítka myši* nebo *kontextové nabídka*.)

Nejtypičtější a nejdůležitější změny, které lze na stránce provést, jsou k dispozici přímo jako možnosti místní nabídky. Například když chcete přidat nebo skrýt sloupce v mřížce, můžete tak učinit pouhým kliknutím pravým tlačítkem na záhlaví sloupce mřížky a pak vybrat **Přidat sloupce** nebo **Skrýt tento sloupec**.

Kromě toho jsou k dispozici základní typy přizpůsobení kliknutím pravým tlačítkem myši a následným výběrem **Přizpůsobit**. (Všimněte si, že ne všechny prvky na stránce mohou být přizpůsobeny.) Použijete-li tuto metodu přizpůsobení, zobrazí se *okno Vlastnosti* prvku.

![Přizpůsobení vlastností prvku](./media/cli-element-property-window.png)

Můžete použít okno vlastností pro individuální nastavení prvku následujícími způsoby:

- Změna popisku prvku.
- Skrytí prvku, takže není zobrazen na stránce. Data v poli nejsou odstraněna nebo upravena. Informace se nezobrazuje na stránce déle.
- Zahrňte informace v oddílu souhrnu pevné záložky (pokud je prvkem o pevná záložka).
- Přeskočte pole, aby nikdy nezískalo výběr při přechodu na stránku.
- Zabraňte úpravě data v poli (pro jakýkoliv záznam).
- Určete pole, které má být požadováno pro zadávání dat. Pokud v tomto poli nebyla zadána žádná hodnota, zobrazí se s červeným ohraničením a hvězdičkou pro označení tohoto stavu. Tato možnost je k dispozici pouze při spuštění ve verzi 10.0.11, když jsou zapnuté funkce [Uložená zobrazení](saved-views.md) a **Určit pole, které vyžadují individuální nastavení**.

Okna vlastností mohou obsahovat další možnosti přizpůsobení, v závislosti na prvku. Například okno vlastností pro dlaždici umožňuje promítnout dlaždici do řídicího panelu a okna vlastnosti pro řídicí panel umožňuje vytvořit nový vlastní pracovní prostor.

### <a name="the-personalization-toolbar"></a>Panel nástrojů individuálních nastavení

Pokud chcete provést více změn stránky nebo provést změny, které nejsou k dispozici prostřednictvím dalších mechanismů (jako je například změna uspořádání prvků), lze použít panel nástrojů **Individuální nastavení**. Chcete-li otevřít panel nástrojů **Individuální nastavení**, proveďte jeden z následujících kroků:

- Vyberte **Ctrl+Shift+P** z libovolného prvku na stránce.
- V okně vlastností prvku vyberte **Přizpůsobit tuto stránku**.
- Vyberte **Přizpůsobit tuto stránku** ve skupině **Přizpůsobit** na kartě **Možnosti** podokna akcí libovolné stránky.
- Na navigačním panelu vyberte tlačítko **nastavení** (symbol ozubeného kola) a pak vyberte volbu **přizpůsobit**.

[![Panel nástrojů individuálních nastavení](./media/restyledPersonalizationToolbar.png)](./media/restyledPersonalizationToolbar.png)

#### <a name="navigating-the-page"></a>Navigace na stránce

Pokud je panel nástrojů **Přizpůsobení** otevřený, je podkladová stránka jen pro čtení (jinými slovy, data nelze upravovat), ale je stále interaktivní. Konkrétně můžete rozbalit nebo sbalit podokno **související informace**, přepnout karty, rozbalit nebo sbalit oddíly stejně, jako obvykle provádíte tyto akce na stránce. Chcete-li použít změnu individuálního nastavení na sbalitelnou část nebo kartu, (například skrýt pevnou záložku), stačí vybrat tlačítko, které se zobrazí vedle sbalitelné části nebo karty, když je na něm zaměřena klávesnice nebo na něj najedete kurzorem myši.

#### <a name="personalization-tools"></a>Nástroje individuálních nastavení

Jsou k dispozici následující nástroje na panelu nástrojů **Přizpůsobení**:

- Použijte nástroj **Vybrat** k výběru a změně vlastností prvku. Chcete-li použít tento nástroj, vyberte na panelu nástrojů tlačítko **vybrat** a pak vyberte požadovaný prvek. Při výběru prvku se otevře okno vlastností prvku, kde můžete změnit jakékoli vlastnosti pro daný prvek. Proces můžete opakovat pro další prvky, které je možné přizpůsobit na této stránce. Všimněte si, že některé vlastnosti přizpůsobení nemusí být v některých scénářích k dispozici. Nemůžete například zamknout pole, které je povinné.
- Chcete-li skrýt prvek na stránce, zvolte nástroj **Skrýt**. Chcete-li použít tento nástroj, vyberte na panelu nástrojů tlačítko **Skrýt** a pak vyberte požadovaný prvek ke skrytí. Když použijete nástroj **Skrýt**, všechny prvky, které jsou nyní skryté, jsou viditelné, ale jsou zobrazeny v šedém kontejneru. Poté můžete prvek zviditelnit jeho výběrem. Chcete-li vidět, jak bude stránka vypadat po skrytí prvků, přepněte do jiného nástroje pro individuální nastavení nebo zavřete panel nástrojů individuálního nastavení.
- Použijte nástroj **Přidat pole** pro přidání polí na stránku. Použijete-li tento nástroj, můžete přidat pouze pole, která jsou součástí definice stránky. Informace o postupu při vytváření nových polí, které nejsou součástí aktuální definice stránky, naleznete v tématu [Vytvoření a práce s vlastními poli](user-defined-fields.md). Po výběru tlačítka **Přidat pole** na panelu nástrojů je nutné nejprve vybrat mřížku či oblast, kam chcete pole přidat. Dialogové okno zobrazí seznam polí souvisejících se zvolenou mřížkou nebo oblastí. V dialogovém okně vyberte jedno nebo více polí pro přidání a zvolte **aktualizovat**. Chcete-li odebrat pole, které jste dříve přidali, opakujte proces, ale v dialogovém okně zrušte výběr pole.
- Zvolte nástroj pro **Přesunutí**, pokud chcete přesunout prvek na jiné místo v rámci aktuální skupiny prvků. Všimněte si, že prvek nelze přesunout mimo nadřazenou skupinu. Chcete-li použít tento nástroj, vyberte na panelu nástrojů tlačítko **Přesunout** a pak vyberte požadovaný prvek k přesunutí. Při výběru prvku aplikace kontroluje stránku a určuje místa, do nichž lze prvek přesunout. Tato umístění se nazývají *zóny přetažení*. Když přetahujete prvek z aktuální skupiny, každá zóna k přetažení je zobrazena jako vybarvená a tučná oblast, kam lze prvek přetáhnout.
- Použijte nástroj **Přeskočit**, chcete-li odebrat prvek z řady karet klávesnic na stránce. Když na panelu nástrojů vyberete tlačítko **Přeskočit**, všechny prvky, které jsou nyní přeskočené, jsou viditelné a jsou zobrazeny v šedém kontejneru. Můžete interaktivně odebrat nebo přidat pole do pořadí polí.
- Použijte nástroj **Zobrazit v záhlaví**, když chcete zobrazit v oddílu souhrnu pevné záložky prvek. Když vyberete na panelu nástrojů tlačítko **Zobrazit v záhlaví**, všechna pole, která byla vybrána jako souhrnná pole, jsou zobrazena v šedém kontejneru. Lze interaktivně přidat pole na souhrn pevné záložky a odstranit pole ze souhrnu pevných záložek výběrem pole.
- Chcete-li určit prvek požadovaný pro zadávání dat, použijte nástroj **Vyžadovat**. Když na panelu nástrojů vyberete tlačítko **Vyžadovat**, všechny prvky, u kterých je vyžadováno individuální nastavení, jsou viditelné a jsou zobrazeny v šedém kontejneru. Pak můžete znovu uričt, aby nevyžadovaly individuální nastavení. Tato možnost je k dispozici pouze při spuštění ve verzi 10.0.12 a pozdější, když je zapnutá funkce **Určit pole, které vyžadují individuální nastavení**.
- Zvolte nástroj **Zamknout**, když chcete označit prvek jako upravitelný nebo neupravitelný. Když na panelu nástrojů vyberete tlačítko **Zamnkout**, všechny prvky, které jsou nyní neupravitelné, jsou viditelné a jsou zobrazeny v šedém kontejneru. Pak je můžete znovu udělat upravitelnými. Všimněte si, že některá pole jsou povinná a nelze je upravovat. Vedle těchto polí se zobrazí symbol visacího zámku.
- Pomocí nástroje **Přidat aplikaci z Power Apps** vložte aplikaci, která byla vytvořena pomocí Microsoft Power Apps, na stránku. Podrobné informace o tom, jak vložit aplikaci z Power Apps na stránku, získáte v tématu [Vkládání aplikací z Power Apps](embed-power-apps.md). Tato možnost je k dispozici pouze tehdy, je-li vypnutá funkce [uložená zobrazení](saved-views.md).
- Pomocí tlačítka **Přidat aplikaci** vložte aplikaci, která byla vytvořena v Microsoft Power Apps nebo třetí stranou, na stránku.. Tato možnost je k dispozici pouze tehdy, je-li zapnutá funkce [uložená zobrazení](saved-views.md). 
- Zvolte nástroj **Vymazat**, pokud chcete obnovit výchozí nainstalovaný stav stránky. Vymaže všechna individuální nastavení na aktuální stránce. Tuto akci nelze vrátit zpět. Tento nástroj použijte pouze v případě, že jste si jisti, že chcete resetovat stránku. Pokud je zapnutá funkce **Uložená zobrazení**, tento nástroj vymaže personalizace aktuálního zobrazení.
- Použijte nástroj **Import** k načtení přizpůsobení ze souboru, který jste vy nebo někdo jiný dříve vytvořili pro tuto stránku. 

    - Když je funkce **Uložená zobrazení** vypnutá, můžete si vybrat, zda přidat nebo nahradit stávající personalizace personalizacemi, které se importují pro stránku. Tuto akci nelze vrátit zpět. Po importu přizpůsobení je tedy nutné ručně vymazat nebo zrušit všechny požadované změny.
    - Pokud je funkce **Uložené pohledy** zapnutá, importované personalizace se stanou pohledem na stránku. Pokud zobrazení již existuje, budete mít možnost přeskočit import, nahradit aktuální zobrazení, které má stejný název, nebo přejmenovat importované zobrazení.

- Použijte nástroj **Export** pro uložení vašeho přizpůsobení stránky do souboru. Individuální nastavení pak můžete sdílet s jinými uživateli. Tito uživatelé musí importovat soubor, který obsahuje vaše přizpůsobení stránky. Pokud je zapnutá funkce **Uložená zobrazení**, tento nástroj uloží vaše aktuální zobrazení do souboru pro sdílení.
- Zvolte tlačítko **Zavřít** k zavření panelu nástrojů **Přizpůsobení** a návratu stránky do jejího předchozího interaktivního stavu.

Při použití panelu nástrojů **Individuální nastavení** se vaše přizpůsobení běžně uplatní, jakmile je provedete. Je-li však funkce [Uložená zobrazení](saved-views.md) zapnutá, musíte individuální nastavení výslovně uložit do zvoleného zobrazení.

V některých případech se zobrazí ikona visacího zámku s prvkem pro výběr nástroje. Tento symbol označuje, že nemůžete změnit vlastnosti prvku, které se vztahují k vybranému nástroji, protože změny těchto vlastností zabrání tomu, aby stránka fungovala správně.

### <a name="adding-tiles-lists-and-links-to-a-workspace"></a>Přidání dlaždic, seznamů a odkazů do pracovního prostoru

U některých stránek, které obsahují seznamy, je funkce individuálního nastavení **Přidat do pracovního prostoru** k dispozici ve skupině **Přizpůsobit** na kartě **Možnosti** v podokně akcí. Tato funkce umožňuje nabízení relevantních informací z aktuálního seznamu do konkrétního pracovního prostoru. Informace zobrazené v pracovním prostoru mohou být založeny buď na celém seznamu, nebo na filtrované a seřazené verzi seznamu. Můžete také určit, zda se informace se zobrazí v pracovním prostoru jako seznam, jako souhrnná dlaždice, která zobrazí počet položek v seznamu, nebo jako odkaz.

> [!NOTE]
> Pokud je zapnutá funkce [Uložená zobrazení](saved-views.md), bude obsah, který zadáte do pracovního prostoru, přímo propojen se zobrazením. Dotaz zobrazení se používá k načtení dat v pracovním prostoru a odpovídající dlaždice nebo odkaz v pracovním prostoru otevře stránku s tímto zobrazením, takže se na něj uplatní dotazy a přizpůsobení zobrazení. Pokud je zobrazení aktualizováno, odpovídající prvky pracovního prostoru budou upraveny na novou definici zobrazení.

[![Přidat na pracovní prostor](./media/personalization-addtoworkspace.png)](./media/personalization-addtoworkspace.png)

- Chcete-li přidat seznam do pracovního prostoru, nejprve seřaďte nebo filtrujte seznam na stránce tak, aby zobrazoval informace, jak chcete, aby se zobrazovaly v pracovním prostoru. (Pokud je funkce **Uložená zobrazení** zapnutá, nemůžete pokračovat, dokud neuložíte zobrazení s těmito podmínkami.) Poté vyberte možnost **Přidat do pracovního prostoru**. Vyberte pracovní prostor a potom v poli **Prezentace** zvolte **Seznam**. Po výběru **Konfigurovat** se zobrazí se dialogové okno, kde můžete vybrat sloupce, které se mají zobrazit na seznamu v pracovním prostoru. Můžete také určit popisek použitý pro seznam v pracovním prostoru.
- Chcete-li přidat dlaždici do pracovního prostoru, nejprve vyfiltrujte seznam na stránce, aby ukázal data, která chcete sumarizovat, nebo k nim mít rychlý přístup. (Pokud je funkce **Uložená zobrazení** zapnutá, nemůžete pokračovat, dokud neuložíte zobrazení s těmito podmínkami.) Poté vyberte možnost **Přidat do pracovního prostoru**. Vyberte pracovní prostor a potom v poli **Prezentace** zvolte **Dlaždice**. Po výběru **Konfigurovat** se zobrazí se dialogové okno, kde můžete určit popisek, který by měl být použit pro dlaždici v pracovním prostoru. Můžete také určit, zda má dlaždice ukazovat počet. Po přidání dlaždice do pracovního prostoru ji můžete vybrat k otevření aktuální stránky z pracovního prostoru. Poté můžete zobrazit filtrovaný seznam, který je spojený s dlaždicí.
- Chcete-li přidat odkaz na pracovní prostor, nejprve filtrujte na stránce seznam tak, aby zobrazoval data, která vás zajímají. (Pokud je funkce **Uložená zobrazení** zapnutá, nemůžete pokračovat, dokud neuložíte zobrazení s těmito podmínkami.) Poté vyberte možnost **Přidat do pracovního prostoru**. Vyberte pracovní prostor a potom v poli **Prezentace** zvolte **Odkaz**. Po výběru **Konfigurovat** se zobrazí se dialogové okno, kde můžete určit popisek, který se má použít pro odkaz. Můžete také volitelně zadat popisek pro nový oddíl, který bude tento odkaz obsahovat.

Po přidání seznamu, dlaždice nebo odkazu do pracovního prostoru můžete otevřít pracovní prostor a přeuspořádat jeho prvky podle potřeby.

### <a name="adding-a-summary-from-a-workspace-to-a-dashboard"></a>Přidání souhrnu z pracovního prostoru do řídicího panelu

Některé pracovní prostory obsahují dlaždice s početem (tzn. dlaždice s čísly na nich) a můžete také nechat dlaždice zobrazit na řídicím panelu. V pracovním prostoru klikněte pravým tlačítkem na dlaždici s počtem, vyberte **Přizpůsobit** a poté v okně vlastností dlaždice vyberte **Připnout na řídicí panel**. Příště, až budete otevírat (a aktualizovat) řídicí panel, zobrazí se vám tento počet pod navigační dlaždicí daného pracovního prostoru. Tento počet můžete vybrat pro přechod přímo na data, která reprezentuje.

### <a name="personalizing-your-dashboard"></a>Individuální nastavení řídicího panelu

Řídicí panel je často první stránkou, která se zobrazí při otevření aplikace. Lze jej přizpůsobit jako kteroukoli jinou stránku v systému pomocí stejných mechanismů, které byly popsány dříve v tomto tématu. 

> [!WARNING]
> Když v současné době skrýváte obsah na hlavním panelu, je důležité, abyste přímo zacílili na dlaždici, nikoli na prostor kolem ní. Pokud skupinu skryjete kolem dlaždice, mohlo by dojít k neočekávaným výsledkům, pokud bude později přidáno více dlaždic nebo pokud je systém přepnut do jiného jazyka.

Jedinou jedinečnou možností personalizace, která je k dispozici na řídicím panelu, je možnost přidat dlaždice. 

- Pokud je funkce **Aplikace na celou stránku** vypnutá, můžete přidat novou dlaždici tak, že kliknete pravým tlačítkem myši na řídicí panel a vyberete **Přidat pracovní prostor**. V dolní části řídicího panelu se vytvoří nová dlaždice pracovního prostoru. Tuto novou dlaždici pracovního prostoru můžete přejmenovat, jak chcete. Můžete také přidat seznamy, odkazy a dlaždice do pracovního prostoru, jak je popsáno v části tématu [Přidání dlaždic, seznamů a odkazů do pracovního prostoru](personalize-user-experience.md#adding-tiles-lists-and-links-to-a-workspace).
- Pokud je funkce **Aplikace na celou stránku** vypnutá, můžete přidat novou dlaždici tak, že kliknete pravým tlačítkem myši na řídicí panel a vyberete **Přidat aplikaci**. V dialogovém okně vyberte, zda chcete přidat dlaždici pro nový pracovní prostor nebo dlaždici, která má obsah z Power Apps nebo webu. Poté podle pokynů nakonfigurujte vybranou možnost. V dolní části řídicího panelu se vytvoří nová dlaždice. 

## <a name="sharing-personalizations"></a>Sdílení individuálních nastavení

Poté, co jste přizpůsobili stránku, můžete svá individuální nastavení sdílet s dalšími uživateli prostřednictvím exportu přizpůsobené stránky. Poté můžete požádat ostatní uživatele o import souboru personalizace. Případně můžete dát vaše přizpůsobení uživateli s oprávněními správce. Tento uživatel pak může použít váš soubor individuálního nastavení na mnoho uživatelů současně pomocí stránky pro správu **Individuální nastavení**.

## <a name="administration-of-personalizations"></a>Správa přizpůsobení

Stránka **Individuální nastavení** je ústředním centrem pro správu individuálních nastavení na úrovni organizace. Obsah a možnosti na této stránce závisí na tom, zda byla zapnuta funkce **Uložená zobrazení**.

Zákazníci, kteří mají zapnutou funkci **Uložená zobrazení**, by si měli přečíst téma Globální správa zobrazení v tématu [Uložená zobrazení](saved-views.md).

U zákazníků, kteří ještě nezapnuli funkci [Uložená zobrazení](saved-views.md), má tato stránka čtyři karty:

- **Použít** – můžete importovat nebo zvolit individuální nastavení pro jednoho nebo více uživatelů. Chcete-li použít přizpůsobení pro jednoho nebo více uživatelů, nejprve vyberte roli a uživatele, kteří tuto roli mají. Poté buď vyberte existující personalizaci, která se bude vztahovat na vybrané uživatele, nebo importovat soubor personalizace. Přizpůsobení bude ověřeno a použito pro všechny vybrané uživatele, když příště otevřou vybrané stránky.
- **Vymazat** – Můžete vymazat všechna přizpůsobení stránky nebo pracovního prostoru pro jednoho nebo více uživatelů. Nejprve vyberte stránku nebo pracovní prostor, aby se zobrazil seznam uživatelů, kteří u nich provedli individuální nastavení. Poté vyberte uživatele, kteří by měli mít individuální nastavení pro tuto stránku nebo pracovní prostor odstraněno, a vyberte **Vymazat**. Všechna přizpůsobení, která vybraní uživatelé použili u vybrané stránky nebo pracovního prostoru, se smažou. Tuto akci nelze vrátit zpět. Pokud však byla personalizace uložena pro stránku nebo pracovní prostor, může být tato personalizace znovu importována.
- **Uživatelé** – vyberte uživatele a zobrazte seznam stránek, pro které má uživatel individuální nastavení. Pak můžete zapnout možnost zvoleného uživatele zapnout nebo vypnout přizpůsobení pro specifické stránky nebo pro celý systém. Rovněž můžete vymazat, importovat nebo exportovat individuální nastavení pro uživatele. Kromě toho můžete vynulovat vysvětlivky k funkcím pro uživatele. V takovém případě, pokud uživatel předtím odstranil všechna překryvná okna, která zavádějí nové funkce, zobrazí se znovu při příštím výskytu těchto funkcí uživatelem.
- **Systém:** – Zde můžete dočasně vypnout přizpůsobení v systému pro všechny uživatele. V tomto případě budou všechna individuální nastavení odstraněna pro všechny uživatele a všechny stránky budou obnoveny do výchozího stavu. Pokud později zapnete přizpůsobení znovu, veškerá přizpůsobení budou znovu použita. Můžete trvale odstranit veškerá přizpůsobení v systému pro všechny uživatele. Neexistuje žádný způsob obnovení individuálního nastavení, které bylo odstraněno. Proto se před provedením tohoto úkolu ujistěte, že jste exportovali všechna individuální nastavení, která můžete chtít později.

## <a name="personalizing-inventory-dimensions"></a>Individuální nastavení dimenzí zásob

Když si přizpůsobíte nastavení dimenze zásob na stránce, zvažte nastavení, která byla vytvořena pomocí možnosti **Zobrazení dimenzí**. Například používáte přizpůsobení ke skrytí sloupce pro dimenzi čísla skladové dávky, ale sloupec se objeví při příštím otevření stránky K tomu dochází, protože nastavení **Zobrazení dimenzí** kontroluje dimenze zásob, které jsou zobrazeny. Nastavení **Zobrazení dimenzí** platí pro všechny stránky a přepíše všechna individuální nastavení polí dimenze zásob na jednotlivých stránkách.

V předchozím příkladu, pokud nechcete, aby se zobrazil sloupec dimenze zásob čísla dávky na stránce, musíte tuto dimenzi vymazat jako součást volby **Zobrazení dimenzí** pro tuto stránku.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]