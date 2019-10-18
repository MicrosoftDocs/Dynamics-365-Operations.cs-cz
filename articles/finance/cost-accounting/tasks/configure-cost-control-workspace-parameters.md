---
title: Konfigurace parametrů pracovního prostoru řízení nákladů
description: Pomocí tohoto postupu nastavte pracovní prostor řízení nákladů tak, aby vedoucí pracovníci na různých úrovních v rámci organizace mohli získat přehled o svých objektech nákladů, jako jsou nákladová střediska nebo skupiny produktů.
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 867bfd2f2d1ff486e683cb11c38906dd0efe8c14
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/27/2019
ms.locfileid: "2187859"
---
# <a name="configure-cost-control-workspace-parameters"></a><span data-ttu-id="2908d-103">Konfigurace parametrů pracovního prostoru řízení nákladů</span><span class="sxs-lookup"><span data-stu-id="2908d-103">Configure cost control workspace parameters</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2908d-104">Pomocí tohoto postupu nastavte pracovní prostor řízení nákladů tak, aby vedoucí pracovníci na různých úrovních v rámci organizace mohli získat přehled o svých objektech nákladů, jako jsou nákladová střediska nebo skupiny produktů.</span><span class="sxs-lookup"><span data-stu-id="2908d-104">Use this procedure to configure the Cost control workspace so that managers at various levels in an organization can gain insight into their cost objects, such as cost centers and product groups.</span></span> <span data-ttu-id="2908d-105">K vytvoření tohoto záznamu jsou použita ukázková data společnosti USP2.</span><span class="sxs-lookup"><span data-stu-id="2908d-105">The USP2 demo company was used to create this recording.</span></span>

1. <span data-ttu-id="2908d-106">Přejděte na Nákladové účetnictví > Nastavení > Konfigurace pracovního prostoru pro řízení nákladů.</span><span class="sxs-lookup"><span data-stu-id="2908d-106">Go to Cost accounting > Setup > Cost control workspace configuration.</span></span>
2. <span data-ttu-id="2908d-107">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="2908d-107">Click New.</span></span>
3. <span data-ttu-id="2908d-108">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="2908d-108">In the Name field, type a value.</span></span>
4. <span data-ttu-id="2908d-109">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="2908d-109">In the Description field, type a value.</span></span>
5. <span data-ttu-id="2908d-110">Vyberte možnost Ano v poli Publikováno.</span><span class="sxs-lookup"><span data-stu-id="2908d-110">Select Yes in the Published field.</span></span>
    * <span data-ttu-id="2908d-111">Pokud tuto možnost nastavíte na Ano, uživatelé s přiřazenou některou z těchto rolí si mohou zobrazit sestavu v pracovním prostoru řízení nákladů: manažer nákladového účetnictví, nákladový účetní, úředník na pozici nákladového účetního nebo kontrolor objektu nákladů.</span><span class="sxs-lookup"><span data-stu-id="2908d-111">If you set this option to Yes, users who are assigned one of these roles can see the report in the Cost control workspace: cost accounting manager, cost accountant, cost accountant clerk, or cost object controller.</span></span> <span data-ttu-id="2908d-112">Pokud tuto možnost nastavíte na Ne, pouze uživatelé s přiřazenou některou z těchto rolí si mohou zobrazit sestavu v pracovním prostoru řízení nákladů: manažer nákladového účetnictví, nákladový účetní nebo úředník na pozici nákladového účetního.</span><span class="sxs-lookup"><span data-stu-id="2908d-112">If you set this option to No, only users who are assigned one of these roles can see the report in the Cost control workspace: cost accounting manager, cost accountant, or cost accountant clerk.</span></span>  
6. <span data-ttu-id="2908d-113">Rozbalte oddíl Filtrování dat.</span><span class="sxs-lookup"><span data-stu-id="2908d-113">Expand the Data filtering section.</span></span>
7. <span data-ttu-id="2908d-114">V poli Jednotka řízení nákladů zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="2908d-114">In the Cost control unit field, enter or select a value.</span></span>
8. <span data-ttu-id="2908d-115">V poli Původní verze rozpočtu zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="2908d-115">In the Budget original version field, enter or select a value.</span></span>
9. <span data-ttu-id="2908d-116">V poli Hierarchie dimenze prvku nákladů zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="2908d-116">In the Cost element dimension hierarchy field, enter or select a value.</span></span>
10. <span data-ttu-id="2908d-117">V poli Hierarchie dimenze objektu nákladů zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="2908d-117">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
11. <span data-ttu-id="2908d-118">Rozbalte část Přiřazení záznamů výpočtů.</span><span class="sxs-lookup"><span data-stu-id="2908d-118">Expand the Assign calculation records section.</span></span>
12. <span data-ttu-id="2908d-119">Klikněte na možnost Nový.</span><span class="sxs-lookup"><span data-stu-id="2908d-119">Click New.</span></span>
13. <span data-ttu-id="2908d-120">Označte na seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="2908d-120">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="2908d-121">V poli Období fiskálního kalendáře zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="2908d-121">In the Fiscal calendar period field, enter or select a value.</span></span>
15. <span data-ttu-id="2908d-122">V poli Aktuální verze zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="2908d-122">In the Actual version field, enter or select a value.</span></span>
16. <span data-ttu-id="2908d-123">Rozbalte část Fiskální období dle sloupce.</span><span class="sxs-lookup"><span data-stu-id="2908d-123">Expand the Fiscal periods per column section.</span></span>
17. <span data-ttu-id="2908d-124">Vyberte možnost Ano v poli Aktuální období.</span><span class="sxs-lookup"><span data-stu-id="2908d-124">Select Yes in the Current period field.</span></span>
18. <span data-ttu-id="2908d-125">Rozbalte část Sloupce k zobrazení nákladů.</span><span class="sxs-lookup"><span data-stu-id="2908d-125">Expand the Columns to display for costs section.</span></span>
19. <span data-ttu-id="2908d-126">Vyberte možnost Ano v poli Pevné náklady.</span><span class="sxs-lookup"><span data-stu-id="2908d-126">Select Yes in the Fixed cost field.</span></span>
20. <span data-ttu-id="2908d-127">Vyberte možnost Ano v poli Proměnné náklady.</span><span class="sxs-lookup"><span data-stu-id="2908d-127">Select Yes in the Variable cost field.</span></span>
21. <span data-ttu-id="2908d-128">Vyberte možnost Ano v poli Celkové náklady.</span><span class="sxs-lookup"><span data-stu-id="2908d-128">Select Yes in the Total cost field.</span></span>
22. <span data-ttu-id="2908d-129">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="2908d-129">Click Save.</span></span>
23. <span data-ttu-id="2908d-130">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="2908d-130">Close the page.</span></span>
24. <span data-ttu-id="2908d-131">Přejděte do části Nákladové účetnictví > Pracovní prostory > Řízení nákladů.</span><span class="sxs-lookup"><span data-stu-id="2908d-131">Go to Cost accounting > Workspaces > Cost control.</span></span>
25. <span data-ttu-id="2908d-132">Vyberte výpis podle toho, zda chcete zobrazit pevné, proměnné, celkové nebo nezatříděné náklady pro vybraná fiskální období.</span><span class="sxs-lookup"><span data-stu-id="2908d-132">Select a statement to see fixed, variable, total, and unclassified costs for the selected fiscal periods.</span></span>
26. <span data-ttu-id="2908d-133">V poli Období fiskálního kalendáře zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="2908d-133">In the Fiscal calendar period field, enter or select a value.</span></span>
27. <span data-ttu-id="2908d-134">V poli Uzel hierarchie dimenze objektu nákladů zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="2908d-134">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="2908d-135">Po výběru hierarchie dimenzí objektu nákladů rozbalte hierarchii dimenzí prvku nákladů a prohlédněte si požadované nákladové hodnoty.</span><span class="sxs-lookup"><span data-stu-id="2908d-135">After you've selected a Cost object dimension hierarchy, expand the Cost element dimension hierarchy to see the desired cost values.</span></span> <span data-ttu-id="2908d-136">Můžete například rozbalit hierarchii Výrobní režie a zjistit z ní hodnoty.</span><span class="sxs-lookup"><span data-stu-id="2908d-136">For example, you can expand the hierarchy to Manufacturing overhead to see the value.</span></span>  

