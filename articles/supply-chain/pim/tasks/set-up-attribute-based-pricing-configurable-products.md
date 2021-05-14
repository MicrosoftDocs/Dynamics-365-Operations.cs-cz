---
title: Nastavení ocenění podle atributů pro konfigurovatelné produkty
description: Toto téma vysvětluje, jak nastavit ceny na základě atributů.
author: ShylaThompson
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelList, PCPriceModel, PCConstraintEditor
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0c30c520e7265c2676937f5191844f6789c364e6
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921234"
---
# <a name="set-up-attribute-based-pricing-for-configurable-products"></a><span data-ttu-id="ef1e7-103">Nastavení ocenění podle atributů pro konfigurovatelné produkty</span><span class="sxs-lookup"><span data-stu-id="ef1e7-103">Set up attribute-based pricing for configurable products</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ef1e7-104">Toto téma vysvětluje, jak nastavit ceny na základě atributů.</span><span class="sxs-lookup"><span data-stu-id="ef1e7-104">This topic explains how to set up attribute-based pricing.</span></span> <span data-ttu-id="ef1e7-105">Jako předpoklad musíte mít model konfigurace produktu, který má jednu nebo více komponent a atributů.</span><span class="sxs-lookup"><span data-stu-id="ef1e7-105">As a prerequisite, you must have a product configuration model that has one or more components and attributes.</span></span> <span data-ttu-id="ef1e7-106">Tento příklad využívá model špičkového reproduktoru v ukázkové datové společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="ef1e7-106">This example uses the High End Speaker product model in the USMF demo data company.</span></span> <span data-ttu-id="ef1e7-107">Manažer produktu obvykle používá tuto proceduru.</span><span class="sxs-lookup"><span data-stu-id="ef1e7-107">Typically, a product manager uses this procedure.</span></span>


## <a name="create-a-new-price-model"></a><span data-ttu-id="ef1e7-108">Vytvoření nového cenového modelu</span><span class="sxs-lookup"><span data-stu-id="ef1e7-108">Create a new price model</span></span>

1. <span data-ttu-id="ef1e7-109">Přejděte na **Řízení informací o produktech \> Produkty \> Modely konfigurace produktu**.</span><span class="sxs-lookup"><span data-stu-id="ef1e7-109">Go to **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="ef1e7-110">V seznamu vyberte řádek **Špičkový reproduktor**, ale nevybírejte odkaz pro název.</span><span class="sxs-lookup"><span data-stu-id="ef1e7-110">In the list, select the **High End Speaker** line, but don't select the link for the name.</span></span>
1. <span data-ttu-id="ef1e7-111">V podokně akcí zvolte **Model**.</span><span class="sxs-lookup"><span data-stu-id="ef1e7-111">On the Action Pane, select **Model**.</span></span>
1. <span data-ttu-id="ef1e7-112">Vyberte **Cenové modely**.</span><span class="sxs-lookup"><span data-stu-id="ef1e7-112">Select **Price models**.</span></span>
1. <span data-ttu-id="ef1e7-113">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="ef1e7-113">Select **New**.</span></span>
1. <span data-ttu-id="ef1e7-114">Do pole **Název cenového modelu** zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="ef1e7-114">In the **Price model name** field, type a value.</span></span> <span data-ttu-id="ef1e7-115">Použijte název, který usnadňuje identifikaci modelu.</span><span class="sxs-lookup"><span data-stu-id="ef1e7-115">Use a name that makes the model easy to identify.</span></span>  
1. <span data-ttu-id="ef1e7-116">Zadejte hodnotu do pole **Popis**.</span><span class="sxs-lookup"><span data-stu-id="ef1e7-116">In the **Description** field, type a value.</span></span>
1. <span data-ttu-id="ef1e7-117">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="ef1e7-117">Select **Save**.</span></span>

## <a name="add-price-elements"></a><span data-ttu-id="ef1e7-118">Přidání cenových prvků</span><span class="sxs-lookup"><span data-stu-id="ef1e7-118">Add price elements</span></span>

1. <span data-ttu-id="ef1e7-119">Vyberte možnost **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="ef1e7-119">Select **Edit**.</span></span> <span data-ttu-id="ef1e7-120">Každá komponenta v produktovém modelu u může mít element základní ceny a libovolný počet pravidel výrazu ceny.</span><span class="sxs-lookup"><span data-stu-id="ef1e7-120">Each component in a product model can have a base price element and any number of price expression rules.</span></span> <span data-ttu-id="ef1e7-121">Můžete také přidat ceny v různých měnách.</span><span class="sxs-lookup"><span data-stu-id="ef1e7-121">You can also add prices in different currencies.</span></span>  
2. <span data-ttu-id="ef1e7-122">Zadejte hodnotu do pole **Výraz základní ceny**.</span><span class="sxs-lookup"><span data-stu-id="ef1e7-122">In the **Base price expression** field, type a value.</span></span> <span data-ttu-id="ef1e7-123">Zadejte například 100.</span><span class="sxs-lookup"><span data-stu-id="ef1e7-123">For example, type 100.</span></span> <span data-ttu-id="ef1e7-124">Výraz základní ceny může být číselná hodnota nebo se může skládat z aritmetického výpočtu, který zahrnuje jeden nebo více atributů.</span><span class="sxs-lookup"><span data-stu-id="ef1e7-124">A base price expression can be a numerical value, or it can consist of an arithmetic calculation that involves one or more attributes.</span></span>  
3. <span data-ttu-id="ef1e7-125">Vyberte **přidat**.</span><span class="sxs-lookup"><span data-stu-id="ef1e7-125">Select **Add**.</span></span>
4. <span data-ttu-id="ef1e7-126">Do pole **Název** zadejte `Rosewood`.</span><span class="sxs-lookup"><span data-stu-id="ef1e7-126">In the **Name** field, type `Rosewood`.</span></span> <span data-ttu-id="ef1e7-127">Název cenový výraz pomáhá určit, co představuje cenový prvek.</span><span class="sxs-lookup"><span data-stu-id="ef1e7-127">The price expression name helps identify what the price element represents.</span></span> <span data-ttu-id="ef1e7-128">V tomto příkladu vytváříme cenový prvek pro možnost Dokončení skříňky z růžového dřeva.</span><span class="sxs-lookup"><span data-stu-id="ef1e7-128">In this example, we are creating a price element for the Rosewood speaker cabinet finish option.</span></span>  
5. <span data-ttu-id="ef1e7-129">Vyberte **Podmínku úpravy**.</span><span class="sxs-lookup"><span data-stu-id="ef1e7-129">Select **Edit condition**.</span></span> <span data-ttu-id="ef1e7-130">Cenové podmínky pomáhají zaručit, že prvek cenového výrazu je součástí prodejní ceny pouze v případě, že existuje určité kombinace atributů.</span><span class="sxs-lookup"><span data-stu-id="ef1e7-130">A price condition helps guarantee that a price expression element is included in the sales price only if a specific combination of attributes is present.</span></span>  
6. <span data-ttu-id="ef1e7-131">Do pole **ConstraintBody** zadejte `CabinetFinish=="Rosewood"`.</span><span class="sxs-lookup"><span data-stu-id="ef1e7-131">In the **ConstraintBody** field, enter `CabinetFinish=="Rosewood"`.</span></span>
7. <span data-ttu-id="ef1e7-132">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="ef1e7-132">Select **OK**.</span></span>
8. <span data-ttu-id="ef1e7-133">Zadejte hodnotu do pole **Výraz**.</span><span class="sxs-lookup"><span data-stu-id="ef1e7-133">In the **Expression** field, type a value.</span></span> <span data-ttu-id="ef1e7-134">Zadejte například typ `50`.</span><span class="sxs-lookup"><span data-stu-id="ef1e7-134">For example, type `50`.</span></span> 
9. <span data-ttu-id="ef1e7-135">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="ef1e7-135">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]