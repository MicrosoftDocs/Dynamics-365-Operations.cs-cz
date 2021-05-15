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
ms.openlocfilehash: 69d22c3321beaa2667ee20bff00acd746714b993
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920524"
---
# <a name="create-sales-price-selection-criteria"></a><span data-ttu-id="064d2-103">Vytvoření kritérií pro výběr prodejní ceny</span><span class="sxs-lookup"><span data-stu-id="064d2-103">Create sales price selection criteria</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="064d2-104">Tato procedura ukazuje, jak vytvořit kritérium výběru prodejní ceny pro modely prodejní ceny podle atributů.</span><span class="sxs-lookup"><span data-stu-id="064d2-104">This procedure shows how to create a sales price selection criterion for attribute-based sales price models.</span></span> <span data-ttu-id="064d2-105">Spuštění této procedury vyžaduje, aby byl k dispozici nejméně jeden model prodejní ceny.</span><span class="sxs-lookup"><span data-stu-id="064d2-105">This procedure requires that at least one sales price model be available.</span></span> <span data-ttu-id="064d2-106">Tento příklad používá cenový model pro model prodejních cen řešení Reproduktor ve společnosti ukázkových dat USMF.</span><span class="sxs-lookup"><span data-stu-id="064d2-106">This example uses the price model for the Speaker solution sales price model in the USMF demo data company.</span></span> <span data-ttu-id="064d2-107">Manažer produktu obvykle používá tuto proceduru.</span><span class="sxs-lookup"><span data-stu-id="064d2-107">Typically, a product manager uses this procedure.</span></span>

## <a name="add-a-new-criterion-for-an-existing-sales-price-model"></a><span data-ttu-id="064d2-108">Přidání nového kritéria pro existující model prodejní ceny</span><span class="sxs-lookup"><span data-stu-id="064d2-108">Add a new criterion for an existing sales price model</span></span>

1. <span data-ttu-id="064d2-109">Přejděte na **Řízení informací o produktech \> Produkty \> Modely konfigurace produktu**.</span><span class="sxs-lookup"><span data-stu-id="064d2-109">Go to **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="064d2-110">V seznamu vyberte řádek pro model výrobku řešení reproduktoru, ale neklikejte na odkaz pro název modelu.</span><span class="sxs-lookup"><span data-stu-id="064d2-110">In the list, select the row for the Speaker solution product model, but don't select the link for the model name.</span></span>
1. <span data-ttu-id="064d2-111">V podokně akcí zvolte **Model**.</span><span class="sxs-lookup"><span data-stu-id="064d2-111">On the Action Pane, select **Model**.</span></span>
1. <span data-ttu-id="064d2-112">Vyberte **Kritéria cenového modelu**.</span><span class="sxs-lookup"><span data-stu-id="064d2-112">Select **Price model criteria**.</span></span>
1. <span data-ttu-id="064d2-113">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="064d2-113">Select **New**.</span></span>
1. <span data-ttu-id="064d2-114">Do pole **Název** zadejte hodnotu „Skupina odběratelů 10“.</span><span class="sxs-lookup"><span data-stu-id="064d2-114">In the **Name** field, type 'Customer group 10'.</span></span>
    * <span data-ttu-id="064d2-115">Název kritéria cenového modelu se používá na pomoc při identifikaci základních kritérií výběru.</span><span class="sxs-lookup"><span data-stu-id="064d2-115">The name of the price model criterion is used to help identify the underlying selection criteria.</span></span>  
1. <span data-ttu-id="064d2-116">V poli **Cenový model** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="064d2-116">In the **Price model** field, enter or select a value.</span></span>
1. <span data-ttu-id="064d2-117">V poli **Typ objednávky** vyberte možnost *Prodejní objednávka*.</span><span class="sxs-lookup"><span data-stu-id="064d2-117">In the **Order type** field, select *Sales order*.</span></span>
    * <span data-ttu-id="064d2-118">Typ objednávky určuje databázová pole, která budou k dispozici pro výběrový dotaz.</span><span class="sxs-lookup"><span data-stu-id="064d2-118">The order type determines the database fields that will be available for the selection query.</span></span>  
1. <span data-ttu-id="064d2-119">Zadejte datum do pole **Platné od data**.</span><span class="sxs-lookup"><span data-stu-id="064d2-119">In the **Valid from** field, enter a date.</span></span>
1. <span data-ttu-id="064d2-120">Do pole **Ukončit platnost k datu** zadejte datum.</span><span class="sxs-lookup"><span data-stu-id="064d2-120">In the **Expire by** field, enter a date.</span></span>
1. <span data-ttu-id="064d2-121">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="064d2-121">Select **Save**.</span></span>

## <a name="create-the-query-for-the-selection-criteria"></a><span data-ttu-id="064d2-122">Vytvoření dotazu pro kritérium výběru</span><span class="sxs-lookup"><span data-stu-id="064d2-122">Create the query for the selection criteria</span></span>

1. <span data-ttu-id="064d2-123">Vyberte možnost **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="064d2-123">Select **Edit**.</span></span>
2. <span data-ttu-id="064d2-124">V poli **Tabulka** vyberte *Odběratelé*.</span><span class="sxs-lookup"><span data-stu-id="064d2-124">In the **Table** field, select *Customers*.</span></span>
3. <span data-ttu-id="064d2-125">V poli **Pole** vyberte *Skupina odběratelů*.</span><span class="sxs-lookup"><span data-stu-id="064d2-125">In the **Field** field, select *Customer group*.</span></span>
    * <span data-ttu-id="064d2-126">V tomto příkladu použijeme jako kritérium výběru konkrétní skupinu odběratelů.</span><span class="sxs-lookup"><span data-stu-id="064d2-126">In this example, we will use a specific customer group for the selection criteria.</span></span>  
4. <span data-ttu-id="064d2-127">V poli **Kritéria** vyberte *Skupina odběratelů 10*.</span><span class="sxs-lookup"><span data-stu-id="064d2-127">In the **Criteria** field, select *Customer group 10*.</span></span>
5. <span data-ttu-id="064d2-128">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="064d2-128">Select **OK**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]