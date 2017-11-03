---
title: "Hledání akce"
description: "Tento článek popisuje funkci hledání akce v aplikaci Microsoft Dynamics 365 for Finance and Operations. Hledání akce vám pomůže najít a spustit akce na stránce."
author: jasongre
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 62303
ms.assetid: 62c70de0-fdde-4417-8e08-0583fb095a40
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 6563b6f422eb5562e9fc67c3734cf753a49d466d
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="action-search"></a><span data-ttu-id="c78d8-104">Hledání akce</span><span class="sxs-lookup"><span data-stu-id="c78d8-104">Action search</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="c78d8-105">Tento článek popisuje funkci hledání akce v aplikaci Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c78d8-105">This article describes the action search functionality in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="c78d8-106">Hledání akce vám pomůže najít a spustit akce na stránce.</span><span class="sxs-lookup"><span data-stu-id="c78d8-106">Action search will help you find and run actions on a page.</span></span>

<a name="introduction"></a><span data-ttu-id="c78d8-107">Úvod</span><span class="sxs-lookup"><span data-stu-id="c78d8-107">Introduction</span></span>
------------

<span data-ttu-id="c78d8-108">Stránky v aplikaci Microsoft Dynamics 365 for Finance and Operations vystavují příkazy v podoknech akcí, standardním podokně akcí, které se zobrazí v horní části stránky, a na panelech nástrojů, které se zobrazují v různých částech stránky.</span><span class="sxs-lookup"><span data-stu-id="c78d8-108">Pages in Microsoft Dynamics 365 for Finance and Operations primarily expose commands on Action Panes, both the standard Action Pane that appears at the top of a page and the toolbars that appear in various sections of the page.</span></span> <span data-ttu-id="c78d8-109">V předchozích verzích aplikace Dynamics AX umožňovala funkce Klíčové tipy rychlý přístup k libovolnému tlačítku v podokně akcí stisknutím klávesy Alt a řady čísel.</span><span class="sxs-lookup"><span data-stu-id="c78d8-109">In previous versions, a Key Tips feature let you quickly access any button on an Action Pane by pressing the Alt key and then a series of letters.</span></span> 

<span data-ttu-id="c78d8-110">[![keyTipsAX6](./media/keytipsax6.png)](./media/keytipsax6.png) V aktuální verzi aplikace Finance and Operations nejsou tipy ke klávesám dále dostupné, ale byly nahrazeny funkcí vyhledávání akce.</span><span class="sxs-lookup"><span data-stu-id="c78d8-110">[![keyTipsAX6](./media/keytipsax6.png)](./media/keytipsax6.png) However, in the current version of Finance and Operations, Key Tips are no longer available but have been replaced by the action search feature.</span></span> <span data-ttu-id="c78d8-111">Nová funkce vám umožňuje rychle vyhledat a spustit tlačítko z jakéhokoli viditelného podokna akcí.</span><span class="sxs-lookup"><span data-stu-id="c78d8-111">This new feature lets you quickly search for and run a button from any visible Action Pane.</span></span>

## <a name="using-action-search"></a><span data-ttu-id="c78d8-112">Použití hledání akcí</span><span class="sxs-lookup"><span data-stu-id="c78d8-112">Using action search</span></span>
<span data-ttu-id="c78d8-113">Chcete-li použít funkci hledání akce, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="c78d8-113">To use the action search feature, follow these steps.</span></span>

1.  <span data-ttu-id="c78d8-114">V podokně akcí, klepněte na pole **vyhledávání akcí**.</span><span class="sxs-lookup"><span data-stu-id="c78d8-114">On the Action Pane, click in the **action search** field.</span></span> <span data-ttu-id="c78d8-115">(Pole **vyhledávání akcí** obsahuje ikonu lupy.)</span><span class="sxs-lookup"><span data-stu-id="c78d8-115">(The **action search** field contains a magnifying glass icon.)</span></span>
2.  <span data-ttu-id="c78d8-116">Zadejte část nebo celý název tlačítka, které chcete spustit.</span><span class="sxs-lookup"><span data-stu-id="c78d8-116">Type all or part of the name of the button that you want to run.</span></span> <span data-ttu-id="c78d8-117">Můžete také hledat pomocí slov z „cesty“ k tlačítku.</span><span class="sxs-lookup"><span data-stu-id="c78d8-117">You can also search by using words from the button's "path."</span></span> <span data-ttu-id="c78d8-118">(Další informace o najdete v další části tohoto článku.) Obvykle se tlačítka se zobrazí v horní části seznamu výsledků poté, co zadáte dva až čtyři znaky.</span><span class="sxs-lookup"><span data-stu-id="c78d8-118">(For more information, see the next section of this article.) Typically, a button will appear near the top of the results list after you've typed two to four characters.</span></span>
3.  <span data-ttu-id="c78d8-119">Najděte a spusťte tlačítko v seznamu výsledků (pomocí myši nebo klávesnice).</span><span class="sxs-lookup"><span data-stu-id="c78d8-119">Find and run the button in the results list (by using your mouse or keyboard).</span></span>

<span data-ttu-id="c78d8-120">Po spuštění tlačítka bude výběr vrácen do vaší poslední pozice na stránce tak, abyste mohli pokračovat v práci.</span><span class="sxs-lookup"><span data-stu-id="c78d8-120">After the button is run, the focus is returned to your last position on the page, so that you can continue to work.</span></span> 

<span data-ttu-id="c78d8-121">[![action-search-field](./media/action-search-field.png)](./media/action-search-field.png)</span><span class="sxs-lookup"><span data-stu-id="c78d8-121">[![action-search-field](./media/action-search-field.png)](./media/action-search-field.png)</span></span>

<span data-ttu-id="c78d8-122">Vyhledávání akcí také spustíte stisknutím kláves Ctrl +/ nebo Alt + Q.</span><span class="sxs-lookup"><span data-stu-id="c78d8-122">You can also start action search by pressing Ctrl+/ or Alt+Q.</span></span> <span data-ttu-id="c78d8-123">Stiskněte klávesovou zkratku ještě jednou, chcete-li se vrátit na výběr do vaší poslední pozice na stránce.</span><span class="sxs-lookup"><span data-stu-id="c78d8-123">Press the keyboard shortcut again to return the focus to your last position on the page.</span></span>

## <a name="understanding-the-results-list"></a><span data-ttu-id="c78d8-124">Vysvětlivky k seznamu výsledků</span><span class="sxs-lookup"><span data-stu-id="c78d8-124">Understanding the results list</span></span>
<span data-ttu-id="c78d8-125">Často v aplikaci Finance and Operations musíte znát umístění i kontext tlačítka, abyste plně porozuměli účelu daného tlačítka.</span><span class="sxs-lookup"><span data-stu-id="c78d8-125">Often, in Finance and Operations, you must know both the location and the context of a button to fully understand the purpose of that button.</span></span> <span data-ttu-id="c78d8-126">Proto se zobrazují další informace pro každou položku v seznamu výsledků, které vám pomohou přesně pochopit, která tlačítka se zobrazí v seznamu.</span><span class="sxs-lookup"><span data-stu-id="c78d8-126">Therefore, additional information is shown for each item in the results list, to help you understand exactly which buttons appear in the list.</span></span> <span data-ttu-id="c78d8-127">Zejména se zobrazí "cesta" tlačítka.</span><span class="sxs-lookup"><span data-stu-id="c78d8-127">In particular, the "path" of the button is shown.</span></span> <span data-ttu-id="c78d8-128">Tato cesta může obsahovat popisky tyto prvky uživatelského rozhraní odpovídajícím způsobem:</span><span class="sxs-lookup"><span data-stu-id="c78d8-128">This path might include the labels of the following UI elements, as relevant:</span></span>

-   <span data-ttu-id="c78d8-129">Karta podokno akcí</span><span class="sxs-lookup"><span data-stu-id="c78d8-129">Action Pane tab</span></span>
-   <span data-ttu-id="c78d8-130">Skupina tlačítek</span><span class="sxs-lookup"><span data-stu-id="c78d8-130">Button group</span></span>
-   <span data-ttu-id="c78d8-131">Tlačítko nabídky (pokud je tlačítko uvnitř tlačítka nabídky)</span><span class="sxs-lookup"><span data-stu-id="c78d8-131">Menu button (if the button is inside a menu button)</span></span>
-   <span data-ttu-id="c78d8-132">Oddělovač nabídky (pokud tlačítko je v pojmenované skupině v rámci tlačítka nabídky)</span><span class="sxs-lookup"><span data-stu-id="c78d8-132">Menu separator (if the button is inside a named group inside a menu button)</span></span>
-   <span data-ttu-id="c78d8-133">Skupina nebo karta na stránce (například název pevné záložky)</span><span class="sxs-lookup"><span data-stu-id="c78d8-133">Group or tab on the page (for example, the name of a FastTab)</span></span>

<span data-ttu-id="c78d8-134">Předpokládejme například, že jste zadali výraz **cel** do pole **vyhledávání akcí** a nyní prověřujete seznam výsledků.</span><span class="sxs-lookup"><span data-stu-id="c78d8-134">For example, you typed **tot** in the **action search** field and are now examining the results list.</span></span> <span data-ttu-id="c78d8-135">První položka u tlačítek, která má název **Celkem**, je zvýrazněna.</span><span class="sxs-lookup"><span data-stu-id="c78d8-135">The first entry, for a button that is named **Totals**, is highlighted.</span></span> <span data-ttu-id="c78d8-136">Rovněž je zobrazena cesta tlačítka **Prodejní objednávka** &gt; **Zobrazení**.</span><span class="sxs-lookup"><span data-stu-id="c78d8-136">A button path of **Sales order** &gt; **View** is also shown.</span></span> <span data-ttu-id="c78d8-137">Část **Prodejní objednávka** cesty odpovídá kartě **Prodejní objednávka** v podokně akcí a část **Zobrazení** cesty odpovídá skupině **Zobrazení** na této kartě. Podobně cesta tlačítka **Celková sleva** tlačítko (**Prodej** &gt; **Vypočítat**) informuje o tom, že toto tlačítko se nachází ve skupině **Vypočítat** na kartě podokna akcí **Prodej**.</span><span class="sxs-lookup"><span data-stu-id="c78d8-137">The **Sales order** part of the path corresponds to the **Sales order** tab on the Action Pane, and the **View** part of the path corresponds to the **View** group on that tab. Similarly, the path of the **Total discount** button (**Sell** &gt; **Calculate**) informs you that this button is located in the **Calculate** group on the **Sell** tab of the Action Pane.</span></span> <span data-ttu-id="c78d8-138">Z toho vyplývá, že tyto informace vám pomohou pochopit, které tlačítko bude přesně vyvoláno vyhledáním akce (pokud ho vyberete v podokně výsledků).</span><span class="sxs-lookup"><span data-stu-id="c78d8-138">Therefore, this information helps you understand exactly which button will be triggered by action search (if you select that button in the results list).</span></span> 

<span data-ttu-id="c78d8-139">[![action-search-field-with-data](./media/action-search-field-with-data.png)](./media/action-search-field-with-data.png)</span><span class="sxs-lookup"><span data-stu-id="c78d8-139">[![action-search-field-with-data](./media/action-search-field-with-data.png)](./media/action-search-field-with-data.png)</span></span> 

<span data-ttu-id="c78d8-140">V předchozím příkladu vyhledávání akce ukázalo výsledky ze standardního podokna akcí v horní části stránky.</span><span class="sxs-lookup"><span data-stu-id="c78d8-140">In the previous example, action search showed results from the standard Action Pane at the top of a page.</span></span> <span data-ttu-id="c78d8-141">Vyhledávání akcí však zobrazuje také výsledky viditelných panelů nástrojů, které jsou umístěny na dalších místech na stránce.</span><span class="sxs-lookup"><span data-stu-id="c78d8-141">However, action search also shows results from visible toolbars that are located in other places on the page.</span></span> <span data-ttu-id="c78d8-142">Například vyhledáváte tlačítko **Zásoby na skladě**, které se nachází na pevné záložce **Řádky prodejní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="c78d8-142">For example, you're searching for the **On-hand inventory** button that is located on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="c78d8-143">V tomto případě cesta tlačítka v seznamu výsledků (**Řádky prodejní objednávky**&gt;**Zásoby**&gt;**Zobrazení**) vás informuje o tom, že toto tlačítko se nachází v nadpisu **Zobrazení** na tlačítku nabídky **Zásob** na pevné záložce **Řádky prodejní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="c78d8-143">In this case, the button path in the results list (**Sales order lines** &gt; **Inventory** &gt; **View**) informs you that this button is located under the **View** heading on the **Inventory** menu button on the **Sales order lines** FastTab.</span></span> 

<span data-ttu-id="c78d8-144">[![on-hand-inventory](./media/on-hand-inventory.png)](./media/on-hand-inventory.png)</span><span class="sxs-lookup"><span data-stu-id="c78d8-144">[![on-hand-inventory](./media/on-hand-inventory.png)](./media/on-hand-inventory.png)</span></span>

## <a name="action-search-vs-navigation-search"></a><span data-ttu-id="c78d8-145">Vyhledávání akcí versus hledání navigace</span><span class="sxs-lookup"><span data-stu-id="c78d8-145">Action search vs. Navigation search</span></span>
<span data-ttu-id="c78d8-146">Akce hledání je určena k vyhledání a spuštění akcí na stránce. Existuje i samostatný mechanismus vyhledávání pro vyhledávání a navigaci na stránky aplikace Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c78d8-146">Whereas action search is intended to find and run actions on a page, there is a separate search mechanism for finding and navigating to pages in Finance and Operations.</span></span> <span data-ttu-id="c78d8-147">Další informace o této funkci naleznete v článku [Hledání navigace](navigation-search.md).</span><span class="sxs-lookup"><span data-stu-id="c78d8-147">For more information about that feature, see the [Navigation search](navigation-search.md) article.</span></span>




