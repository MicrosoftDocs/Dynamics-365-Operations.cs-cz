---
title: Vyhledání akce
description: Tento článek popisuje funkci hledání akce. Hledání akce vám pomůže najít a spustit akce na stránce.
author: jasongre
manager: AnnBe
ms.date: 03/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 62303
ms.assetid: 62c70de0-fdde-4417-8e08-0583fb095a40
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bd4d81f010149c762dac0f4e6fa912c2e2cef072
ms.sourcegitcommit: 48c39c0c0949fe48b3536d9d2d0e451d561ff5c6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2020
ms.locfileid: "3112161"
---
# <a name="action-search"></a><span data-ttu-id="6ce9a-104">Vyhledání akce</span><span class="sxs-lookup"><span data-stu-id="6ce9a-104">Action search</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6ce9a-105">Tento článek popisuje funkci hledání akce.</span><span class="sxs-lookup"><span data-stu-id="6ce9a-105">This article describes the action search functionality.</span></span> <span data-ttu-id="6ce9a-106">Hledání akce vám pomůže najít a spustit akce na stránce.</span><span class="sxs-lookup"><span data-stu-id="6ce9a-106">Action search will help you find and run actions on a page.</span></span>

## <a name="introduction"></a><span data-ttu-id="6ce9a-107">Úvod</span><span class="sxs-lookup"><span data-stu-id="6ce9a-107">Introduction</span></span>

<span data-ttu-id="6ce9a-108">Stránky primárně vystavují příkazy v podoknech akcí, standardním podokně akcí, které se zobrazí v horní části stránky, a na panelech nástrojů, které se zobrazují v různých částech stránky.</span><span class="sxs-lookup"><span data-stu-id="6ce9a-108">Pages primarily expose commands on Action Panes, both the standard Action Pane that appears at the top of a page and the toolbars that appear in various sections of the page.</span></span> <span data-ttu-id="6ce9a-109">V předchozích verzích umožňovala funkce Klíčové tipy rychlý přístup k libovolnému tlačítku v podokně akcí stisknutím klávesy Alt a řady čísel.</span><span class="sxs-lookup"><span data-stu-id="6ce9a-109">In previous versions, a Key Tips feature let you quickly access any button on an Action Pane by pressing the Alt key and then a series of letters.</span></span>

<span data-ttu-id="6ce9a-110">[![keyTipsAX6](./media/keytipsax6.png)](./media/keytipsax6.png)</span><span class="sxs-lookup"><span data-stu-id="6ce9a-110">[![keyTipsAX6](./media/keytipsax6.png)](./media/keytipsax6.png)</span></span>

<span data-ttu-id="6ce9a-111">Klíčocé tipy již nejsou k dispozici, ale byly nahrazeny funkcí hledání akce.</span><span class="sxs-lookup"><span data-stu-id="6ce9a-111">Key Tips are no longer available but have been replaced by the action search feature.</span></span> <span data-ttu-id="6ce9a-112">Nová funkce vám umožňuje rychle vyhledat a spustit tlačítko z jakéhokoli viditelného podokna akcí.</span><span class="sxs-lookup"><span data-stu-id="6ce9a-112">This new feature lets you quickly search for and run a button from any visible Action Pane.</span></span>

## <a name="using-action-search"></a><span data-ttu-id="6ce9a-113">Použití hledání akcí</span><span class="sxs-lookup"><span data-stu-id="6ce9a-113">Using action search</span></span>

<span data-ttu-id="6ce9a-114">Chcete-li použít funkci hledání akce, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="6ce9a-114">To use the action search feature, follow these steps.</span></span>

1. <span data-ttu-id="6ce9a-115">V podokně akcí, klepněte na pole **vyhledávání akcí**.</span><span class="sxs-lookup"><span data-stu-id="6ce9a-115">On the Action Pane, click in the **action search** field.</span></span> <span data-ttu-id="6ce9a-116">(Pole **vyhledávání akcí** obsahuje ikonu lupy.)</span><span class="sxs-lookup"><span data-stu-id="6ce9a-116">(The **action search** field contains a magnifying glass icon.)</span></span>
2. <span data-ttu-id="6ce9a-117">Zadejte část nebo celý název tlačítka, které chcete spustit.</span><span class="sxs-lookup"><span data-stu-id="6ce9a-117">Type all or part of the name of the button that you want to run.</span></span> <span data-ttu-id="6ce9a-118">Můžete také hledat pomocí slov z „cesty“ k tlačítku.</span><span class="sxs-lookup"><span data-stu-id="6ce9a-118">You can also search by using words from the button's "path."</span></span> <span data-ttu-id="6ce9a-119">(Další informace o najdete v další části tohoto článku.) Obvykle se tlačítka se zobrazí v horní části seznamu výsledků poté, co zadáte dva až čtyři znaky.</span><span class="sxs-lookup"><span data-stu-id="6ce9a-119">(For more information, see the next section of this article.) Typically, a button will appear near the top of the results list after you've typed two to four characters.</span></span>
3. <span data-ttu-id="6ce9a-120">Najděte a spusťte tlačítko v seznamu výsledků (pomocí myši nebo klávesnice).</span><span class="sxs-lookup"><span data-stu-id="6ce9a-120">Find and run the button in the results list (by using your mouse or keyboard).</span></span>

<span data-ttu-id="6ce9a-121">Po spuštění tlačítka bude výběr vrácen do vaší poslední pozice na stránce tak, abyste mohli pokračovat v práci.</span><span class="sxs-lookup"><span data-stu-id="6ce9a-121">After the button is run, the focus is returned to your last position on the page, so that you can continue to work.</span></span>

<span data-ttu-id="6ce9a-122">[![action-search-field](./media/action-search-field.png)](./media/action-search-field.png)</span><span class="sxs-lookup"><span data-stu-id="6ce9a-122">[![action-search-field](./media/action-search-field.png)](./media/action-search-field.png)</span></span>

<span data-ttu-id="6ce9a-123">Vyhledávání akcí také spustíte stisknutím kláves Ctrl +/ nebo Alt + Q.</span><span class="sxs-lookup"><span data-stu-id="6ce9a-123">You can also start action search by pressing Ctrl+/ or Alt+Q.</span></span> <span data-ttu-id="6ce9a-124">Stiskněte klávesovou zkratku ještě jednou, chcete-li se vrátit na výběr do vaší poslední pozice na stránce.</span><span class="sxs-lookup"><span data-stu-id="6ce9a-124">Press the keyboard shortcut again to return the focus to your last position on the page.</span></span>

## <a name="understanding-the-results-list"></a><span data-ttu-id="6ce9a-125">Vysvětlivky k seznamu výsledků</span><span class="sxs-lookup"><span data-stu-id="6ce9a-125">Understanding the results list</span></span>

<span data-ttu-id="6ce9a-126">Často musíte znát umístění i kontext tlačítka, abyste plně porozuměli účelu daného tlačítka.</span><span class="sxs-lookup"><span data-stu-id="6ce9a-126">Often, you must know both the location and the context of a button to fully understand the purpose of that button.</span></span> <span data-ttu-id="6ce9a-127">Proto se zobrazují další informace pro každou položku v seznamu výsledků, které vám pomohou přesně pochopit, která tlačítka se zobrazí v seznamu.</span><span class="sxs-lookup"><span data-stu-id="6ce9a-127">Therefore, additional information is shown for each item in the results list, to help you understand exactly which buttons appear in the list.</span></span> <span data-ttu-id="6ce9a-128">Zejména se zobrazí "cesta" tlačítka.</span><span class="sxs-lookup"><span data-stu-id="6ce9a-128">In particular, the "path" of the button is shown.</span></span> <span data-ttu-id="6ce9a-129">Tato cesta může obsahovat popisky tyto prvky uživatelského rozhraní odpovídajícím způsobem:</span><span class="sxs-lookup"><span data-stu-id="6ce9a-129">This path might include the labels of the following UI elements, as relevant:</span></span>

- <span data-ttu-id="6ce9a-130">Karta podokno akcí</span><span class="sxs-lookup"><span data-stu-id="6ce9a-130">Action Pane tab</span></span>
- <span data-ttu-id="6ce9a-131">Skupina tlačítek</span><span class="sxs-lookup"><span data-stu-id="6ce9a-131">Button group</span></span>
- <span data-ttu-id="6ce9a-132">Tlačítko nabídky (pokud je tlačítko uvnitř tlačítka nabídky)</span><span class="sxs-lookup"><span data-stu-id="6ce9a-132">Menu button (if the button is inside a menu button)</span></span>
- <span data-ttu-id="6ce9a-133">Oddělovač nabídky (pokud tlačítko je v pojmenované skupině v rámci tlačítka nabídky)</span><span class="sxs-lookup"><span data-stu-id="6ce9a-133">Menu separator (if the button is inside a named group inside a menu button)</span></span>
- <span data-ttu-id="6ce9a-134">Skupina nebo karta na stránce (například název pevné záložky)</span><span class="sxs-lookup"><span data-stu-id="6ce9a-134">Group or tab on the page (for example, the name of a FastTab)</span></span>

<span data-ttu-id="6ce9a-135">Předpokládejme například, že jste zadali výraz **cel** do pole **vyhledávání akcí** a nyní prověřujete seznam výsledků.</span><span class="sxs-lookup"><span data-stu-id="6ce9a-135">For example, you typed **tot** in the **action search** field and are now examining the results list.</span></span> <span data-ttu-id="6ce9a-136">První položka u tlačítek, která má název **Celkem**, je zvýrazněna.</span><span class="sxs-lookup"><span data-stu-id="6ce9a-136">The first entry, for a button that is named **Totals**, is highlighted.</span></span> <span data-ttu-id="6ce9a-137">Rovněž je zobrazena cesta tlačítka **Prodejní objednávka** &gt; **Zobrazení**.</span><span class="sxs-lookup"><span data-stu-id="6ce9a-137">A button path of **Sales order** &gt; **View** is also shown.</span></span> <span data-ttu-id="6ce9a-138">Část **Prodejní objednávka** cesty odpovídá kartě **Prodejní objednávka** v podokně akcí a část **Zobrazení** cesty odpovídá skupině **Zobrazení** na této kartě. Podobně cesta tlačítka **Celková sleva** tlačítko (**Prodej** &gt; **Vypočítat**) informuje o tom, že toto tlačítko se nachází ve skupině **Vypočítat** na kartě podokna akcí **Prodej**.</span><span class="sxs-lookup"><span data-stu-id="6ce9a-138">The **Sales order** part of the path corresponds to the **Sales order** tab on the Action Pane, and the **View** part of the path corresponds to the **View** group on that tab. Similarly, the path of the **Total discount** button (**Sell** &gt; **Calculate**) informs you that this button is located in the **Calculate** group on the **Sell** tab of the Action Pane.</span></span> <span data-ttu-id="6ce9a-139">Z toho vyplývá, že tyto informace vám pomohou pochopit, které tlačítko bude přesně vyvoláno vyhledáním akce (pokud ho vyberete v podokně výsledků).</span><span class="sxs-lookup"><span data-stu-id="6ce9a-139">Therefore, this information helps you understand exactly which button will be triggered by action search (if you select that button in the results list).</span></span>

<span data-ttu-id="6ce9a-140">[![action-search-field-with-data](./media/action-search-field-with-data.png)](./media/action-search-field-with-data.png)</span><span class="sxs-lookup"><span data-stu-id="6ce9a-140">[![action-search-field-with-data](./media/action-search-field-with-data.png)](./media/action-search-field-with-data.png)</span></span>

<span data-ttu-id="6ce9a-141">V předchozím příkladu vyhledávání akce ukázalo výsledky ze standardního podokna akcí v horní části stránky.</span><span class="sxs-lookup"><span data-stu-id="6ce9a-141">In the previous example, action search showed results from the standard Action Pane at the top of a page.</span></span> <span data-ttu-id="6ce9a-142">Vyhledávání akcí však zobrazuje také výsledky viditelných panelů nástrojů, které jsou umístěny na dalších místech na stránce.</span><span class="sxs-lookup"><span data-stu-id="6ce9a-142">However, action search also shows results from visible toolbars that are located in other places on the page.</span></span> <span data-ttu-id="6ce9a-143">Například vyhledáváte tlačítko **Zásoby na skladě**, které se nachází na pevné záložce **Řádky prodejní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="6ce9a-143">For example, you're searching for the **On-hand inventory** button that is located on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="6ce9a-144">V tomto případě cesta tlačítka v seznamu výsledků (**Řádky prodejní objednávky**&gt;**Zásoby**&gt;**Zobrazení**) vás informuje o tom, že toto tlačítko se nachází v nadpisu **Zobrazení** na tlačítku nabídky **Zásob** na pevné záložce **Řádky prodejní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="6ce9a-144">In this case, the button path in the results list (**Sales order lines** &gt; **Inventory** &gt; **View**) informs you that this button is located under the **View** heading on the **Inventory** menu button on the **Sales order lines** FastTab.</span></span>

<span data-ttu-id="6ce9a-145">[![on-hand-inventory](./media/on-hand-inventory.png)](./media/on-hand-inventory.png)</span><span class="sxs-lookup"><span data-stu-id="6ce9a-145">[![on-hand-inventory](./media/on-hand-inventory.png)](./media/on-hand-inventory.png)</span></span>

> [!NOTE]
> <span data-ttu-id="6ce9a-146">V hledání Akcí se nezobrazují některá tlačítka.</span><span class="sxs-lookup"><span data-stu-id="6ce9a-146">There are some buttons that do not show up in Action search.</span></span> <span data-ttu-id="6ce9a-147">Tyto zahrnují tlačítka ukončení dialogu a tlačítka z podformulářů.</span><span class="sxs-lookup"><span data-stu-id="6ce9a-147">These include drop dialog buttons and buttons from subforms.</span></span> 

## <a name="action-search-vs-navigation-search"></a><span data-ttu-id="6ce9a-148">Vyhledávání akcí versus hledání navigace</span><span class="sxs-lookup"><span data-stu-id="6ce9a-148">Action search vs. Navigation search</span></span>

<span data-ttu-id="6ce9a-149">Akce hledání je určena k vyhledání a spuštění akcí na stránce. Existuje i samostatný mechanismus vyhledávání pro vyhledávání a navigaci na stránky.</span><span class="sxs-lookup"><span data-stu-id="6ce9a-149">Whereas action search is intended to find and run actions on a page, there is a separate search mechanism for finding and navigating to pages.</span></span> <span data-ttu-id="6ce9a-150">Další informace o této funkci naleznete v článku [Hledání navigace](navigation-search.md).</span><span class="sxs-lookup"><span data-stu-id="6ce9a-150">For more information about that feature, see the [Navigation search](navigation-search.md) article.</span></span>
