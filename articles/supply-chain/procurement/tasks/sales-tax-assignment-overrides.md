--- 
title: "Přiřazení a přepsání DPH"
description: "Tento postup ukazuje, jak přiřadit skupiny DPH k maloobchodním kanálům."
author: mkirknel
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 05f3abf7359a9bfb3c708739551498333802dd0c
ms.contentlocale: cs-cz
ms.lasthandoff: 08/07/2018

---
# <a name="sales-tax-assignment-and-overrides"></a><span data-ttu-id="a3de4-103">Přiřazení a přepsání DPH</span><span class="sxs-lookup"><span data-stu-id="a3de4-103">Sales tax assignment and overrides</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a3de4-104">Tento postup ukazuje, jak přiřadit skupiny DPH k maloobchodním kanálům.</span><span class="sxs-lookup"><span data-stu-id="a3de4-104">This procedure demonstrates how to assign sales tax groups to retail channels.</span></span> <span data-ttu-id="a3de4-105">Provede vás také procesem vytvoření nového přepsání DPH a jeho přiřazení k existující skupině přepsání DPH.</span><span class="sxs-lookup"><span data-stu-id="a3de4-105">It also walks through the process of creating a new sales tax override and assigning it to an existing sales tax override group.</span></span> <span data-ttu-id="a3de4-106">Tento postup</span><span class="sxs-lookup"><span data-stu-id="a3de4-106">This procedure</span></span>

<span data-ttu-id="a3de4-107">používá v ukázkových datech společnost USRT.</span><span class="sxs-lookup"><span data-stu-id="a3de4-107">uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="a3de4-108">Přejděte do nabídky Maloobchodní a velkoobchodní prodej > Kanály > Maloobchody > Všechny maloobchody.</span><span class="sxs-lookup"><span data-stu-id="a3de4-108">Go to Retail and commerce > Channels > Retail stores > All retail stores.</span></span>
2. <span data-ttu-id="a3de4-109">V seznamu klepněte na odkaz ID maloobchodní sítě – "Houston".</span><span class="sxs-lookup"><span data-stu-id="a3de4-109">In the list, click the Retail Channel ID link for "Houston."</span></span>
3. <span data-ttu-id="a3de4-110">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="a3de4-110">Click Edit.</span></span>
    * <span data-ttu-id="a3de4-111">Pole „Skupina DPH“ obsahuje seznam skupin DPH pro aktuální společnost.</span><span class="sxs-lookup"><span data-stu-id="a3de4-111">The "Sales tax group" field contains the list of sales tax groups for the current company.</span></span> <span data-ttu-id="a3de4-112">Aktuálně přiřazená skupina je obecnou skupinou DPH pro „Texas“.</span><span class="sxs-lookup"><span data-stu-id="a3de4-112">The currently assigned group is a generic "Texas" sales tax group.</span></span> <span data-ttu-id="a3de4-113">Existují také skupiny DPH pro "Washington" a "Washington, King County."</span><span class="sxs-lookup"><span data-stu-id="a3de4-113">There are also sales tax groups for "Washington" and "Washington, King County."</span></span> <span data-ttu-id="a3de4-114">Skupiny DPH mohou zahrnovat platné daně pro více obcí.</span><span class="sxs-lookup"><span data-stu-id="a3de4-114">Sales tax groups can include applicable taxes for multiple municipalities.</span></span>  
    * <span data-ttu-id="a3de4-115">Pole „Přepsání DPH“ je místo, kde lze mapovat skupiny přepisujících DPH k obchodnímu kanálu.</span><span class="sxs-lookup"><span data-stu-id="a3de4-115">The "Sales tax override" field is where sales tax override groups can be mapped to the channel.</span></span> <span data-ttu-id="a3de4-116">Skupiny přepisujících DPH lze použít pro seskupení přepisujících DPH platných pro více obchodů.</span><span class="sxs-lookup"><span data-stu-id="a3de4-116">Sales tax override groups can be used to group together sales tax overrides that work for multiple stores.</span></span> <span data-ttu-id="a3de4-117">Namísto ručního postupného přiřazování přepisujících DPH jednoho po druhém je možné kvůli úspoře času vytvořit skupinu a přiřadit ji přímo k obchodním kanálům.</span><span class="sxs-lookup"><span data-stu-id="a3de4-117">Rather than manually assigning sales tax overrides one by one, the group can be created and assigned directly to the channels to save time.</span></span>  
4. <span data-ttu-id="a3de4-118">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="a3de4-118">Click Save.</span></span>
5. <span data-ttu-id="a3de4-119">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="a3de4-119">Close the page.</span></span>
6. <span data-ttu-id="a3de4-120">Přejděte na Maloobchodní a velkoobchodní prodej > Nastavení kanálu > DPH > Přepsání DPH.</span><span class="sxs-lookup"><span data-stu-id="a3de4-120">Go to Retail and commerce > Channel setup > Sales taxes > Sales tax overrides.</span></span>
7. <span data-ttu-id="a3de4-121">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="a3de4-121">Click New.</span></span>
8. <span data-ttu-id="a3de4-122">Do pole Přepsání DPH zadejte název nového přepsání.</span><span class="sxs-lookup"><span data-stu-id="a3de4-122">In the Sales tax override field, provide a name for your new override.</span></span>
9. <span data-ttu-id="a3de4-123">Do pole Popis zadejte popis přepsání.</span><span class="sxs-lookup"><span data-stu-id="a3de4-123">In the Description field, provide a description of the override.</span></span>
10. <span data-ttu-id="a3de4-124">Nastavte stav na "Povolit".</span><span class="sxs-lookup"><span data-stu-id="a3de4-124">Set the status to "Enable."</span></span>
11. <span data-ttu-id="a3de4-125">Rozbalte nebo sbalte oddíl Přepsání.</span><span class="sxs-lookup"><span data-stu-id="a3de4-125">Expand or collapse the Override section.</span></span>
12. <span data-ttu-id="a3de4-126">Vyberte volbu v poli Typ.</span><span class="sxs-lookup"><span data-stu-id="a3de4-126">In the Type field, select an option.</span></span>
    * <span data-ttu-id="a3de4-127">Skupiny DPH zboží lze použít k přepsání daně pro konkrétní zboží, které patří do dané skupiny.</span><span class="sxs-lookup"><span data-stu-id="a3de4-127">Item sales tax groups can be used to override taxes for specific items that belong to the group.</span></span> <span data-ttu-id="a3de4-128">Například potraviny jsou obvykle daněny odlišně od pevného zboží a pravděpodobně vyžadují vlastní skupinu DPH.</span><span class="sxs-lookup"><span data-stu-id="a3de4-128">For example, food items are typically taxed differently from hard goods, and would likely have their own sales tax group.</span></span>     <span data-ttu-id="a3de4-129">Skupiny DPH jsou skupiny daní, které se vztahují k daném obchodnímu kanálu.</span><span class="sxs-lookup"><span data-stu-id="a3de4-129">Sales tax groups are groups of taxes that are applicable to a particular channel.</span></span> <span data-ttu-id="a3de4-130">Pokud například obchodní kanál prodává v maloobchodní i podnikatelské oblasti, je možné použít odlišné skupiny DPH zboží.</span><span class="sxs-lookup"><span data-stu-id="a3de4-130">For example, if a channel sells both retail and business-to-business, different items sales tax groups may be used.</span></span> <span data-ttu-id="a3de4-131">Všechny platné daně by byly mapovány ke skupině prodejní daně.</span><span class="sxs-lookup"><span data-stu-id="a3de4-131">All the applicable taxes would be mapped to the sales tax group.</span></span>  
    * <span data-ttu-id="a3de4-132">Nově můžete vybrat daně "Od" a "Do" nebo "Z daňové skupiny" a "Do daňové skupiny" a vytvořit tak přepisující DPH.</span><span class="sxs-lookup"><span data-stu-id="a3de4-132">Now you can select the "From" and "To" taxes or "From tax group" and "To tax group" to create your sales tax override.</span></span>    <span data-ttu-id="a3de4-133">Pole "Od" označuje daně nebo daňovou skupinu, která bude přepsána.</span><span class="sxs-lookup"><span data-stu-id="a3de4-133">The "From" field indicates the tax or tax group to be overridden.</span></span> <span data-ttu-id="a3de4-134">Přepsání podle skupiny DPH zboží nabízí jiné možnosti, než přepsání podle skupiny DPH.</span><span class="sxs-lookup"><span data-stu-id="a3de4-134">Overriding by Item sales tax group provides different options than overriding by sales tax group.</span></span>    <span data-ttu-id="a3de4-135">Přepsání DPH můžete nastavit a přepsat daně v celé transakci nebo na konkrétních řádcích v transakci.</span><span class="sxs-lookup"><span data-stu-id="a3de4-135">Sales tax overrides can be set up to override taxes on entire transactions or on particular lines in the transaction.</span></span>  
13. <span data-ttu-id="a3de4-136">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="a3de4-136">Click Save.</span></span>
14. <span data-ttu-id="a3de4-137">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="a3de4-137">Close the page.</span></span>
15. <span data-ttu-id="a3de4-138">Přejděte na Maloobchodní a velkoobchodní prodej > Nastavení kanálu > DPH > Skupiny přepsání DPH.</span><span class="sxs-lookup"><span data-stu-id="a3de4-138">Go to Retail and commerce > Channel setup > Sales taxes > Sales tax override groups.</span></span>
    * <span data-ttu-id="a3de4-139">V tomto kroku přiřadíte nově vytvořené přepisující DPH ke skupině přepisujících DPH přiřazených k obchodnímu kanálu Houston.</span><span class="sxs-lookup"><span data-stu-id="a3de4-139">In this step you will assigned the newly created sales tax override to the sales tax override group assigned to the Houston channel.</span></span>  
16. <span data-ttu-id="a3de4-140">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="a3de4-140">Click Edit.</span></span>
17. <span data-ttu-id="a3de4-141">Rozbalte nebo sbalte oddíl Nastavení.</span><span class="sxs-lookup"><span data-stu-id="a3de4-141">Expand or collapse the Setup section.</span></span>
18. <span data-ttu-id="a3de4-142">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="a3de4-142">Click Add.</span></span>
19. <span data-ttu-id="a3de4-143">V poli Přepsání DPH kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="a3de4-143">In the Sales tax override field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="a3de4-144">Vyberte ze seznamu dříve vytvořené přepsání DPH.</span><span class="sxs-lookup"><span data-stu-id="a3de4-144">Select the previously created sales tax override from the list.</span></span>
21. <span data-ttu-id="a3de4-145">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="a3de4-145">In the list, click the link in the selected row.</span></span>
22. <span data-ttu-id="a3de4-146">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="a3de4-146">Click Save.</span></span>


