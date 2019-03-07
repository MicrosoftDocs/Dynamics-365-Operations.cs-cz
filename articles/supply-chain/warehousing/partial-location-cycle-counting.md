---
title: Částečná cyklická inventura místa
description: Aktuální operace výpočtů řídí plány cyklické inventury. Můžete požadovat, aby byly započítány pouze konkrétní produkty a varianty produktů namísto všech zásob na skladě ve skladovém místě.
author: perlynne
manager: AnnBe
ms.date: 11/02/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSCycleCountPlan, WHSWorkLineCycleCount, WHSWorkTemplateLineGroup, WHSWorkTemplateTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cd7cb8b35023ed63af191545d01c60c2c7cc8ef5
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "320643"
---
# <a name="partial-location-cycle-counting"></a><span data-ttu-id="3a4bd-104">Částečná cyklická inventura místa</span><span class="sxs-lookup"><span data-stu-id="3a4bd-104">Partial location cycle counting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3a4bd-105">Aktuální operace výpočtů řídí plány cyklické inventury.</span><span class="sxs-lookup"><span data-stu-id="3a4bd-105">Cycle count plans guide the actual counting operations.</span></span> <span data-ttu-id="3a4bd-106">Můžete požadovat, aby byly započítány pouze konkrétní produkty a varianty produktů namísto všech zásob na skladě ve skladovém místě.</span><span class="sxs-lookup"><span data-stu-id="3a4bd-106">You can request that only specific products and product variants be counted instead of all on-hand inventory in a location.</span></span>

<span data-ttu-id="3a4bd-107">Když použijete plány cyklické inventury k vytvoření prací na inventuře, můžete řídit vlastní inventurní operace.</span><span class="sxs-lookup"><span data-stu-id="3a4bd-107">By using cycle count plans to create counting work, you can guide the actual counting operations.</span></span> <span data-ttu-id="3a4bd-108">Můžete požadovat, aby byly započítány pouze konkrétní produkty a varianty produktů namísto všech zásob na skladě ve skladovém místě.</span><span class="sxs-lookup"><span data-stu-id="3a4bd-108">You can request that only specific products and product variants be counted instead of all on-hand inventory in a location.</span></span> <span data-ttu-id="3a4bd-109">Vyfiltrováním konkrétních produktů může vedoucí skladu snížit kontrolu režie, vyhnout se chybám konsolidace a ušetřit čas.</span><span class="sxs-lookup"><span data-stu-id="3a4bd-109">By filtering on specific products, the warehouse manager can reduce review overhead, avoid consolidation mistakes, and save time.</span></span>

## <a name="how-to-configure-partial-location-cycle-counting"></a><span data-ttu-id="3a4bd-110">Konfigurace cyklické inventury částečného místa</span><span class="sxs-lookup"><span data-stu-id="3a4bd-110">How to configure partial location cycle counting</span></span>
<span data-ttu-id="3a4bd-111">Když použijete proces práce ve skladu pro skladové operace inventury, pro každé místo se vytvoří záhlaví práce.</span><span class="sxs-lookup"><span data-stu-id="3a4bd-111">When you use the warehouse work process for counting operations, a work header is created for each location.</span></span> <span data-ttu-id="3a4bd-112">Při definování plánu cyklické inventury můžete použít dotaz **Vybrat umístění** k omezení vytvořené práce cyklické inventury.</span><span class="sxs-lookup"><span data-stu-id="3a4bd-112">When you define the cycle count plan, you can use the **Select locations** query to limit the cycle counting work that is created.</span></span> <span data-ttu-id="3a4bd-113">Vyberete-li produkty pro plán cyklické inventury, můžete vybrat dotazy na produkt a variantu produktu k upřesnění toho, co je do inventury zahrnuto.</span><span class="sxs-lookup"><span data-stu-id="3a4bd-113">When you select products for the cycle count plan, you can select both product and product variant queries to refine what is counted.</span></span> 

<span data-ttu-id="3a4bd-114">Můžete přidružit **šablonu práce** k plánu cyklické inventury pro definování, jak by měla být vytvořena práce cyklické inventury.</span><span class="sxs-lookup"><span data-stu-id="3a4bd-114">You can associate a **work template** with a cycle count plan to define how the cycle count work should be created.</span></span> <span data-ttu-id="3a4bd-115">Šablona práce pro operace inventury přímo odkazuje na plán cyklické inventury.</span><span class="sxs-lookup"><span data-stu-id="3a4bd-115">The work template for counting operations is directly referenced from the cycle count plan.</span></span> 

<span data-ttu-id="3a4bd-116">Při definování podrobností šablony práce můžete vybrat možnost **Zalomení řádků práce** k určení, zda řádky práce na inventuře musí být seskupeny podle čísla položky nebo varianty produktu.</span><span class="sxs-lookup"><span data-stu-id="3a4bd-116">When you define the work template details, you can use the **Work line breaks** option to specify whether the counting work lines must be grouped by item number or product variant number.</span></span> <span data-ttu-id="3a4bd-117">Toto nastavení není povinné, pokud chcete provést výpočet zásob na skladě pouze pro konkrétní produkty ve skladovém místě.</span><span class="sxs-lookup"><span data-stu-id="3a4bd-117">This setup is required if you want to count on-hand inventory only for specific products in a location.</span></span> <span data-ttu-id="3a4bd-118">Řádky práce cyklické inventury, které jsou vytvořeny, budou mít úroveň informací, kterou zde definujete, a řízené cyklické operace budou zpracovány na základě této úrovně.</span><span class="sxs-lookup"><span data-stu-id="3a4bd-118">The cycle counting work lines that are created will have the level of information that you define here, and the guided counting operation will be handled based on this level.</span></span> 

<span data-ttu-id="3a4bd-119">Pokud přiřadíte plány cyklické inventury šablonám práce pomocí možnosti **Zalomení řádků práce**, je vybráno pole **částečné cyklické inventury** pro vybranou práci cyklické inventury, která je vytvořena, a vytvoří se více řádků práce cyklické inventury na základě definice pracovní šablony.</span><span class="sxs-lookup"><span data-stu-id="3a4bd-119">If you associate cycle count plans with work templates by using the **Work lines breaks** option, the **Partial cycle count** field is selected for the cycle counting work that is created, and multiple cycle counting work lines will be created based on the definition of the work template.</span></span> 

<span data-ttu-id="3a4bd-120">Předtím, než lze zpracovat práci cyklické inventury, musíte přinejmenším zaškrtnout políčko **Zobrazit číslo položky** nabídky mobilního zařízení v rámci nastavení cyklické inventury.</span><span class="sxs-lookup"><span data-stu-id="3a4bd-120">Before partial cycle count work can be processed, you must, at a minimum, select **Display item number** for the mobile device menu item as part of the cycle counting setup.</span></span> <span data-ttu-id="3a4bd-121">Operátor skladu bude požádán o zaznamenání pouze těch informací o inventuře, které souvisí s řádky inventury (čísla položky a dimenze produktů).</span><span class="sxs-lookup"><span data-stu-id="3a4bd-121">The warehouse operator will be asked to record only counting information that is related to the counting lines (item numbers and product dimensions).</span></span> <span data-ttu-id="3a4bd-122">Všechny ostatní zásoby na skladě budou v tomto procesu inventury ignorovány.</span><span class="sxs-lookup"><span data-stu-id="3a4bd-122">All other on-hand inventory will be ignored for this counting process.</span></span> 

<span data-ttu-id="3a4bd-123">Pro proces částečné cyklické inventury nebude datum/čas **poslední cyklické inventury** pro skladové místo aktualizovány.</span><span class="sxs-lookup"><span data-stu-id="3a4bd-123">For the partial cycle count process, the **Last cycle count** date/time won’t be updated for the location.</span></span>

## <a name="example"></a><span data-ttu-id="3a4bd-124">Příklad</span><span class="sxs-lookup"><span data-stu-id="3a4bd-124">Example</span></span>
<span data-ttu-id="3a4bd-125">V tomto příkladu se pro sklad 61 musí započítat pouze číslo položky A0001.</span><span class="sxs-lookup"><span data-stu-id="3a4bd-125">For this example, only item number A0001 must be counted in warehouse 61.</span></span>

1.  <span data-ttu-id="3a4bd-126">Je vytvořena nová šablona práce pro cyklickou inventuru.</span><span class="sxs-lookup"><span data-stu-id="3a4bd-126">A new work template for cycle counting is created.</span></span> <span data-ttu-id="3a4bd-127">Možnost **Zalomení řádků práce** se používá k seskupení řádek práce inventury podle čísla položky.</span><span class="sxs-lookup"><span data-stu-id="3a4bd-127">The **Work line breaks** option is used to group counting work lines by item number.</span></span> <span data-ttu-id="3a4bd-128">Proto bude vytvořená práce výpočtu cyklické inventury mít řádky na číslo položky.</span><span class="sxs-lookup"><span data-stu-id="3a4bd-128">Therefore, the cycle counting work that is created will have lines per item number.</span></span> <span data-ttu-id="3a4bd-129">Také můžete seskupit řádky podle čísla varianty produktu.</span><span class="sxs-lookup"><span data-stu-id="3a4bd-129">You can also group the lines by product variant number.</span></span>
2.  <span data-ttu-id="3a4bd-130">Je vytvořen nový plán cyklické inventury, který odkazuje na nově vytvořenou šablonu práce.</span><span class="sxs-lookup"><span data-stu-id="3a4bd-130">A new cycle counting plan is created that references the newly created work template.</span></span> <span data-ttu-id="3a4bd-131">Plán cyklické inventury zahrnuje všechna místa ve skladu 61 (dotaz **vybrat umístění**), které blokuje zásoby s číslem položky A0001.</span><span class="sxs-lookup"><span data-stu-id="3a4bd-131">The cycle counting plan includes all locations in warehouse 61 (**Select locations** query) that hold inventory for item number A0001.</span></span> <span data-ttu-id="3a4bd-132">Výběr konkrétních produktů je definován v oddílu **Výběr produktů cyklické inventury**.</span><span class="sxs-lookup"><span data-stu-id="3a4bd-132">The selection of specific products is defined in the **Cycle count product selections** section.</span></span>
3.  <span data-ttu-id="3a4bd-133">Můžete vybrat produkty pro plány cyklické inventury pomocí nastavení pole **Prázdná skladová místa** na **Vyloučit prázdná**.</span><span class="sxs-lookup"><span data-stu-id="3a4bd-133">You can select products for cycle counting plans by setting the **Empty locations** field to **Exclude empty**.</span></span> <span data-ttu-id="3a4bd-134">Při zpracování plánu cyklické inventury je vytvořena práce částečné cyklické inventury pro číslo položky A0001.</span><span class="sxs-lookup"><span data-stu-id="3a4bd-134">When the cycle counting plan is processed, partial cycle count work for item number A0001 is created.</span></span> <span data-ttu-id="3a4bd-135">Skutečný proces inventury lze provést pomocí položky nabídky mobilního zařízení pro řízené cyklické inventury.</span><span class="sxs-lookup"><span data-stu-id="3a4bd-135">The actual counting process can be performed by using a mobile device menu item for guided cycle counting.</span></span>



<a name="additional-resources"></a><span data-ttu-id="3a4bd-136">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="3a4bd-136">Additional resources</span></span>
--------

[<span data-ttu-id="3a4bd-137">Cyklická inventura</span><span class="sxs-lookup"><span data-stu-id="3a4bd-137">Cycle counting</span></span>](cycle-counting.md)

