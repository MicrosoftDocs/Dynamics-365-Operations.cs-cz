---
title: Vytvoření kritérií pro výběr prodejní ceny
description: Tato procedura ukazuje, jak vytvořit kritérium výběru prodejní ceny pro modely prodejní ceny podle atributů.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelSelectionCriteria, SysQueryForm, SysQueryTableLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5a616dcfdd755efc9bf0473e9239acb9127f11f8
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818150"
---
# <a name="create-sales-price-selection-criteria"></a><span data-ttu-id="4e364-103">Vytvoření kritérií pro výběr prodejní ceny</span><span class="sxs-lookup"><span data-stu-id="4e364-103">Create sales price selection criteria</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4e364-104">Tato procedura ukazuje, jak vytvořit kritérium výběru prodejní ceny pro modely prodejní ceny podle atributů.</span><span class="sxs-lookup"><span data-stu-id="4e364-104">This procedure shows how to create a sales price selection criterion for attribute-based sales price models.</span></span> <span data-ttu-id="4e364-105">Spuštění této procedury vyžaduje, aby byl k dispozici nejméně jeden model prodejní ceny.</span><span class="sxs-lookup"><span data-stu-id="4e364-105">This procedure requires that at least one sales price model be available.</span></span> <span data-ttu-id="4e364-106">Tento příklad používá cenový model pro model prodejních cen řešení Reproduktor ve společnosti ukázkových dat USMF.</span><span class="sxs-lookup"><span data-stu-id="4e364-106">This example uses the price model for the Speaker solution sales price model in the USMF demo data company.</span></span> <span data-ttu-id="4e364-107">Manažer produktu obvykle používá tuto proceduru.</span><span class="sxs-lookup"><span data-stu-id="4e364-107">Typically, a product manager uses this procedure.</span></span>


## <a name="add-a-new-criterion-for-an-existing-sales-price-model"></a><span data-ttu-id="4e364-108">Přidání nového kritéria pro existující model prodejní ceny</span><span class="sxs-lookup"><span data-stu-id="4e364-108">Add a new criterion for an existing sales price model</span></span>
1. <span data-ttu-id="4e364-109">Klepněte na Definice modelu varianty produktu.</span><span class="sxs-lookup"><span data-stu-id="4e364-109">Click Product variant model definition.</span></span>
2. <span data-ttu-id="4e364-110">Klepněte na Modely konfigurace produktu.</span><span class="sxs-lookup"><span data-stu-id="4e364-110">Click Product configuration models.</span></span>
3. <span data-ttu-id="4e364-111">V seznamu vyberte řádek pro model výrobku řešení reproduktoru, ale neklikejte na odkaz pro název modelu.</span><span class="sxs-lookup"><span data-stu-id="4e364-111">In the list, select the row for the Speaker solution product model, but don't click the link for the model name.</span></span>
4. <span data-ttu-id="4e364-112">V podokně akcí klepněte na možnost Model.</span><span class="sxs-lookup"><span data-stu-id="4e364-112">On the Action Pane, click Model.</span></span>
5. <span data-ttu-id="4e364-113">Klikněte na Kritéria cenového modelu.</span><span class="sxs-lookup"><span data-stu-id="4e364-113">Click Price model criteria.</span></span>
6. <span data-ttu-id="4e364-114">Klikněte na možnost Nový.</span><span class="sxs-lookup"><span data-stu-id="4e364-114">Click New.</span></span>
7. <span data-ttu-id="4e364-115">Do pole Název zadejte hodnotu Skupina odběratelů 10.</span><span class="sxs-lookup"><span data-stu-id="4e364-115">In the Name field, type 'Customer group 10'.</span></span>
    * <span data-ttu-id="4e364-116">Název kritéria cenového modelu se používá na pomoc při identifikaci základních kritérií výběru.</span><span class="sxs-lookup"><span data-stu-id="4e364-116">The name of the price model criterion is used to help identify the underlying selection criteria.</span></span>  
8. <span data-ttu-id="4e364-117">V poli Cenový model zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="4e364-117">In the Price model field, enter or select a value.</span></span>
9. <span data-ttu-id="4e364-118">V poli Výchozí typ objednávky vyberte možnost Prodejní objednávka.</span><span class="sxs-lookup"><span data-stu-id="4e364-118">In the Order type field, select Sales order.</span></span>
    * <span data-ttu-id="4e364-119">Typ objednávky určuje databázová pole, která budou k dispozici pro výběrový dotaz.</span><span class="sxs-lookup"><span data-stu-id="4e364-119">The order type determines the database fields that will be available for the selection query.</span></span>  
10. <span data-ttu-id="4e364-120">Zadejte datum do pole Platné od data.</span><span class="sxs-lookup"><span data-stu-id="4e364-120">In the Valid from field, enter a date.</span></span>
11. <span data-ttu-id="4e364-121">Do pole Ukončit platnost k datu zadejte datum.</span><span class="sxs-lookup"><span data-stu-id="4e364-121">In the Expire by field, enter a date.</span></span>
12. <span data-ttu-id="4e364-122">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="4e364-122">Click Save.</span></span>

## <a name="create-the-query-for-the-selection-criteria"></a><span data-ttu-id="4e364-123">Vytvoření dotazu pro kritérium výběru</span><span class="sxs-lookup"><span data-stu-id="4e364-123">Create the query for the selection criteria</span></span>
1. <span data-ttu-id="4e364-124">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="4e364-124">Click Edit.</span></span>
2. <span data-ttu-id="4e364-125">V poli Tabulka vyberte Odběratelé.</span><span class="sxs-lookup"><span data-stu-id="4e364-125">In the Table field, select Customers.</span></span> 
3. <span data-ttu-id="4e364-126">V poli Pole vyberte Skupina odběratelů.</span><span class="sxs-lookup"><span data-stu-id="4e364-126">In the Field field, select Customer group.</span></span>
    * <span data-ttu-id="4e364-127">V tomto příkladu použijeme jako kritérium výběru konkrétní skupinu odběratelů.</span><span class="sxs-lookup"><span data-stu-id="4e364-127">In this example, we will use a specific customer group for the selection criteria.</span></span>  
4. <span data-ttu-id="4e364-128">V poli Kritéria vyberte Skupina odběratelů 10.</span><span class="sxs-lookup"><span data-stu-id="4e364-128">In the Criteria field, select Customer group 10.</span></span> 
5. <span data-ttu-id="4e364-129">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="4e364-129">Click OK.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]