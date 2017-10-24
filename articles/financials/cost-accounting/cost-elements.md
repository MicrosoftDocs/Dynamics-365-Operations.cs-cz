---
title: "Dimenze prvku nákladů"
description: "Coby jeden ze základních pilířů v nákladovém účetnictví se dimenze prvků nákladů používají pro kategorizaci a sledování, kam jsou náklady převáděny."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMDimension
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 223204
ms.assetid: 1eda0e62-760b-4737-9dfd-3c3c38d80c1a
ms.search.region: global
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 00a09120116183785d96ed1e18c577d5430fa16b
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---

# <a name="cost-element-dimensions"></a><span data-ttu-id="488f6-103">Dimenze prvku nákladů</span><span class="sxs-lookup"><span data-stu-id="488f6-103">Cost element dimensions</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="488f6-104">Coby jeden ze základních pilířů v nákladovém účetnictví se dimenze prvků nákladů používají pro kategorizaci a sledování, kam jsou náklady převáděny.</span><span class="sxs-lookup"><span data-stu-id="488f6-104">As one of the core pillars in Cost accounting, cost element dimensions are used to categorize and track where costs flow to.</span></span> 

<span data-ttu-id="488f6-105">Prvek nákladů odpovídá příslušné položce nákladů v účtové osnově.</span><span class="sxs-lookup"><span data-stu-id="488f6-105">A cost element corresponds to a cost-relevant item in the chart of accounts.</span></span> <span data-ttu-id="488f6-106">V zásadě může jít o libovolný typ prvku v nejnižší úrovni společnosti, kde může docházet k toku nákladů.</span><span class="sxs-lookup"><span data-stu-id="488f6-106">Basically, it can be any type of element at the lowest level in a business where costs can flow to.</span></span> <span data-ttu-id="488f6-107">Prvky nákladů jako koncept se pohybují od účtů hlavní knihy po všechny prostředky související s náklady.</span><span class="sxs-lookup"><span data-stu-id="488f6-107">Cost elements as a concept range from ledger accounts to all cost-relevant resources.</span></span> <span data-ttu-id="488f6-108">V současné době nákladové účetnictví podporuje účty hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="488f6-108">Currently, Cost accounting supports ledger accounts.</span></span>

## <a name="two-types-of-cost-elements"></a><span data-ttu-id="488f6-109">Dva typy prvků nákladů</span><span class="sxs-lookup"><span data-stu-id="488f6-109">Two types of cost elements</span></span>
<span data-ttu-id="488f6-110">Existují dva typy prvků nákladů: primární prvky nákladů a sekundární prvky nákladů.</span><span class="sxs-lookup"><span data-stu-id="488f6-110">There are two types of cost elements: primary cost elements and secondary cost elements.</span></span> <span data-ttu-id="488f6-111">Následující tabulka popisuje rozdíly mezi oběma typy.</span><span class="sxs-lookup"><span data-stu-id="488f6-111">The following table describes the difference between the two types.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="488f6-112"><strong>Primární prvky nákladů</strong></span><span class="sxs-lookup"><span data-stu-id="488f6-112"><strong>Primary cost elements</strong></span></span></td>
<td><span data-ttu-id="488f6-113"><strong>Prvky druhotných nákladů</strong></span><span class="sxs-lookup"><span data-stu-id="488f6-113"><strong>Secondary cost elements</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="488f6-114">Primární prvky nákladů představují tok nákladů z finančního účetnictví do nákladového účetnictví.</span><span class="sxs-lookup"><span data-stu-id="488f6-114">The primary cost elements represent the flow of costs from financial accounting to cost accounting.</span></span> <span data-ttu-id="488f6-115">Struktura prvku nákladů odpovídá ziskům a ztrátám účetní struktury v hlavní knize, kde prvek nákladů může odpovídat hlavnímu účtu.</span><span class="sxs-lookup"><span data-stu-id="488f6-115">The cost element structure corresponds to the profit and loss account structure in the general ledger, where a cost element can correspond to a main account.</span></span> <span data-ttu-id="488f6-116">Ne všechny hlavní účty musejí být nutně prezentovány jako prvky nákladů závisející na obchodních potřebách.</span><span class="sxs-lookup"><span data-stu-id="488f6-116">Not all main accounts may necessarily be represented as cost elements depending on the business needs.</span></span> <span data-ttu-id="488f6-117">Příklady primárních prvků nákladů zahrnují:</span><span class="sxs-lookup"><span data-stu-id="488f6-117">Examples of primary cost elements include:</span></span>
<ul>
<li><span data-ttu-id="488f6-118">Náklady prodaného zboží</span><span class="sxs-lookup"><span data-stu-id="488f6-118">Costs of goods sold (COGs)</span></span></li>
<li><span data-ttu-id="488f6-119">Nepřímé náklady na materiál</span><span class="sxs-lookup"><span data-stu-id="488f6-119">Indirect material costs</span></span></li>
<li><span data-ttu-id="488f6-120">Osobní náklady</span><span class="sxs-lookup"><span data-stu-id="488f6-120">Personnel costs</span></span></li>
<li><span data-ttu-id="488f6-121">Náklady na energii</span><span class="sxs-lookup"><span data-stu-id="488f6-121">Energy costs</span></span></li>
</ul></td>
<td><span data-ttu-id="488f6-122">Sekundární prvky nákladů představují tok nákladů interně, protože tyto náklady vznikají a používají se pouze v nákladovém účetnictví.</span><span class="sxs-lookup"><span data-stu-id="488f6-122">The secondary cost elements represent the flow of costs internally because these costs are created and used only in Cost accounting.</span></span> <span data-ttu-id="488f6-123">Používají se pokud chcete zajistit, že lze sledovat zdroje nákladů.</span><span class="sxs-lookup"><span data-stu-id="488f6-123">They are used to secure that the source of costs can be traced.</span></span> <span data-ttu-id="488f6-124">Tyto prvky nákladů se používají při přidělování nákladů a výpočtech režijních nákladů.</span><span class="sxs-lookup"><span data-stu-id="488f6-124">These cost elements are used in cost allocations and overhead calculations.</span></span> <span data-ttu-id="488f6-125">Příklady sekundárních prvků nákladů zahrnují:</span><span class="sxs-lookup"><span data-stu-id="488f6-125">Examples of secondary cost elements include:</span></span>
<ul>
<li><span data-ttu-id="488f6-126">Výrobní náklady</span><span class="sxs-lookup"><span data-stu-id="488f6-126">Production costs</span></span></li>
<li><span data-ttu-id="488f6-127">Výroba, materiál a režie marketingu</span><span class="sxs-lookup"><span data-stu-id="488f6-127">Production, material, and marketing overheads</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="cost-element-dimensions-and-cost-element-dimension-members"></a><span data-ttu-id="488f6-128">Dimenze prvku nákladů a členy dimenze prvku nákladů</span><span class="sxs-lookup"><span data-stu-id="488f6-128">Cost element dimensions and cost element dimension members</span></span>
<span data-ttu-id="488f6-129">Prvky náklady se označují jako *dimenze prvků nákladů* .</span><span class="sxs-lookup"><span data-stu-id="488f6-129">Cost elements are referred to as *cost element dimensions* .</span></span> <span data-ttu-id="488f6-130">Hodnoty jednotlivých dimenzí se nazývají *členy dimenze prvku nákladů*.</span><span class="sxs-lookup"><span data-stu-id="488f6-130">The individual dimension values are called *cost element dimension members*.</span></span> <span data-ttu-id="488f6-131">V USA máme například strukturu účtové osnovy (COA), která je základem pro statutární vykazování.</span><span class="sxs-lookup"><span data-stu-id="488f6-131">For example, you have a US chart of accounts structure (COA) that is the base for your statutory reporting.</span></span> <span data-ttu-id="488f6-132">Tato COA slouží jako dimenze prvku nákladů.</span><span class="sxs-lookup"><span data-stu-id="488f6-132">This COA is used as the cost element dimension.</span></span> <span data-ttu-id="488f6-133">Účty, které jsou primární prvky nákladů, jsou představovány jako členy dimenze prvku nákladů v nákladovém účetnictví.</span><span class="sxs-lookup"><span data-stu-id="488f6-133">The accounts, which are primary cost elements, are represented as the cost element dimension members in Cost accounting.</span></span> <span data-ttu-id="488f6-134">Následující obrázek znázorňuje příklad hlavního účtu jako dimenze prvku nákladů s jeho aktuálními hlavními účty jako členy dimenze prvku nákladů.</span><span class="sxs-lookup"><span data-stu-id="488f6-134">The following screenshot shows an example of Main Accounts as the cost element dimension with its actual main accounts as the cost element dimension members.</span></span> 

<span data-ttu-id="488f6-135">[![Dimenze prvku nákladů](./media/cost-element-dimensions.png)](./media/cost-element-dimensions.png)</span><span class="sxs-lookup"><span data-stu-id="488f6-135">[![cost-element-dimensions](./media/cost-element-dimensions.png)](./media/cost-element-dimensions.png)</span></span>

## <a name="import-cost-element-dimension-members-through-data-connectors"></a><span data-ttu-id="488f6-136">Import členů dimenze prvků nákladů pomocí datových konektorů</span><span class="sxs-lookup"><span data-stu-id="488f6-136">Import cost element dimension members through data connectors</span></span>
<span data-ttu-id="488f6-137">K usnadnění nastavení členů dimenze prvku nákladů v nákladovém účetnictví můžete použít datové konektory, které jsou předem připravené nebo vytvořené na míru, abyste získali zpět primární prvky nákladů z jednoho nebo více zdrojových systémů.</span><span class="sxs-lookup"><span data-stu-id="488f6-137">To ease the setup of cost element dimension members in Cost accounting, you can use data connectors that are either pre-built or your custom build to retrieve the primary cost elements from one or more source systems.</span></span>

## <a name="implementation-considerations"></a><span data-ttu-id="488f6-138">Na co myslet při implementaci</span><span class="sxs-lookup"><span data-stu-id="488f6-138">Implementation considerations</span></span>
<span data-ttu-id="488f6-139">Jelikož prvky nákladů představují nejnižší úroveň podrobností o nákladech, měli byste se ujistit, že všechny požadované prvky nákladů pro manažerské vykazování jsou zahrnuty při implementací struktury prvků nákladů.</span><span class="sxs-lookup"><span data-stu-id="488f6-139">As cost elements represent the lowest level of cost details, you should make sure that all the cost elements required to make the managerial reporting are included when you implement the cost elements structure.</span></span> <span data-ttu-id="488f6-140">Může být obtížné najít vhodný počet prvků nákladů pro řízení nákladů.</span><span class="sxs-lookup"><span data-stu-id="488f6-140">It can be a challenge to find an appropriate number of cost elements for cost control.</span></span> <span data-ttu-id="488f6-141">Tisíce prvků nákladů pravděpodobně ztíží řízení jednotlivých prvků nákladů.</span><span class="sxs-lookup"><span data-stu-id="488f6-141">Having thousands of cost elements can make it difficult to control each cost element.</span></span> <span data-ttu-id="488f6-142">Jako alternativní postup lze seskupit prvky nákladů a správu řízení nákladů v agregační úrovni.</span><span class="sxs-lookup"><span data-stu-id="488f6-142">As an alternative, you can group cost elements and manage cost control at an aggregated level.</span></span>




