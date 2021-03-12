---
title: Nastavení ocenění podle atributů pro konfigurovatelné produkty
description: Toto téma vysvětluje, jak nastavit ceny na základě atributů.
author: ShylaThompson
manager: tfehr
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelList, PCPriceModel, PCConstraintEditor
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b2f9a78902ff1a0333c46c8ad9142338678b6e7d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4986772"
---
# <a name="set-up-attribute-based-pricing-for-configurable-products"></a><span data-ttu-id="1034b-103">Nastavení ocenění podle atributů pro konfigurovatelné produkty</span><span class="sxs-lookup"><span data-stu-id="1034b-103">Set up attribute-based pricing for configurable products</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1034b-104">Toto téma vysvětluje, jak nastavit ceny na základě atributů.</span><span class="sxs-lookup"><span data-stu-id="1034b-104">This topic explains how to set up attribute-based pricing.</span></span> <span data-ttu-id="1034b-105">Jako předpoklad musíte mít model konfigurace produktu, který má jednu nebo více komponent a atributů.</span><span class="sxs-lookup"><span data-stu-id="1034b-105">As a prerequisite, you must have a product configuration model that has one or more components and attributes.</span></span> <span data-ttu-id="1034b-106">Tento příklad využívá model špičkového reproduktoru v ukázkové datové společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="1034b-106">This example uses the High End Speaker product model in the USMF demo data company.</span></span> <span data-ttu-id="1034b-107">Manažer produktu obvykle používá tuto proceduru.</span><span class="sxs-lookup"><span data-stu-id="1034b-107">Typically, a product manager uses this procedure.</span></span>


## <a name="create-a-new-price-model"></a><span data-ttu-id="1034b-108">Vytvoření nového cenového modelu</span><span class="sxs-lookup"><span data-stu-id="1034b-108">Create a new price model</span></span>
1. <span data-ttu-id="1034b-109">Vyberte **Definici modelu varianty produktu** na domovské stránce.</span><span class="sxs-lookup"><span data-stu-id="1034b-109">Select **Product variant model definition** on the home page.</span></span>
2. <span data-ttu-id="1034b-110">Vyberte **Modely konfigurace produktu** v části **odkazy**.</span><span class="sxs-lookup"><span data-stu-id="1034b-110">Select **Product configuration models** in the **links** section.</span></span>
3. <span data-ttu-id="1034b-111">V seznamu vyberte řádek **Špičkový reproduktor**, ale nevybírejte odkaz pro název.</span><span class="sxs-lookup"><span data-stu-id="1034b-111">In the list, select the **High End Speaker** line, but don't select the link for the name.</span></span>
4. <span data-ttu-id="1034b-112">V podokně akcí zvolte **Model**.</span><span class="sxs-lookup"><span data-stu-id="1034b-112">On the Action Pane, select **Model**.</span></span>
5. <span data-ttu-id="1034b-113">Vyberte **Cenové modely**.</span><span class="sxs-lookup"><span data-stu-id="1034b-113">Select **Price models**.</span></span>
6. <span data-ttu-id="1034b-114">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="1034b-114">Select **New**.</span></span>
7. <span data-ttu-id="1034b-115">Do pole **Název cenového modelu** zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="1034b-115">In the **Price model name** field, type a value.</span></span> <span data-ttu-id="1034b-116">Použijte název, který usnadňuje identifikaci modelu.</span><span class="sxs-lookup"><span data-stu-id="1034b-116">Use a name that makes the model easy to identify.</span></span>  
8. <span data-ttu-id="1034b-117">Zadejte hodnotu do pole **Popis**.</span><span class="sxs-lookup"><span data-stu-id="1034b-117">In the **Description** field, type a value.</span></span>
9. <span data-ttu-id="1034b-118">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="1034b-118">Select **Save**.</span></span>

## <a name="add-price-elements"></a><span data-ttu-id="1034b-119">Přidání cenových prvků</span><span class="sxs-lookup"><span data-stu-id="1034b-119">Add price elements</span></span>
1. <span data-ttu-id="1034b-120">Vyberte možnost **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="1034b-120">Select **Edit**.</span></span> <span data-ttu-id="1034b-121">Každá komponenta v produktovém modelu u může mít element základní ceny a libovolný počet pravidel výrazu ceny.</span><span class="sxs-lookup"><span data-stu-id="1034b-121">Each component in a product model can have a base price element and any number of price expression rules.</span></span> <span data-ttu-id="1034b-122">Můžete také přidat ceny v různých měnách.</span><span class="sxs-lookup"><span data-stu-id="1034b-122">You can also add prices in different currencies.</span></span>  
2. <span data-ttu-id="1034b-123">Zadejte hodnotu do pole **Výraz základní ceny**.</span><span class="sxs-lookup"><span data-stu-id="1034b-123">In the **Base price expression** field, type a value.</span></span> <span data-ttu-id="1034b-124">Zadejte například 100.</span><span class="sxs-lookup"><span data-stu-id="1034b-124">For example, type 100.</span></span> <span data-ttu-id="1034b-125">Výraz základní ceny může být číselná hodnota nebo se může skládat z aritmetického výpočtu, který zahrnuje jeden nebo více atributů.</span><span class="sxs-lookup"><span data-stu-id="1034b-125">A base price expression can be a numerical value, or it can consist of an arithmetic calculation that involves one or more attributes.</span></span>  
3. <span data-ttu-id="1034b-126">Vyberte **přidat**.</span><span class="sxs-lookup"><span data-stu-id="1034b-126">Select **Add**.</span></span>
4. <span data-ttu-id="1034b-127">Do pole **Název** zadejte `Rosewood`.</span><span class="sxs-lookup"><span data-stu-id="1034b-127">In the **Name** field, type `Rosewood`.</span></span> <span data-ttu-id="1034b-128">Název cenový výraz pomáhá určit, co představuje cenový prvek.</span><span class="sxs-lookup"><span data-stu-id="1034b-128">The price expression name helps identify what the price element represents.</span></span> <span data-ttu-id="1034b-129">V tomto příkladu vytváříme cenový prvek pro možnost Dokončení skříňky z růžového dřeva.</span><span class="sxs-lookup"><span data-stu-id="1034b-129">In this example, we are creating a price element for the Rosewood speaker cabinet finish option.</span></span>  
5. <span data-ttu-id="1034b-130">Vyberte **Podmínku úpravy**.</span><span class="sxs-lookup"><span data-stu-id="1034b-130">Select **Edit condition**.</span></span> <span data-ttu-id="1034b-131">Cenové podmínky pomáhají zaručit, že prvek cenového výrazu je součástí prodejní ceny pouze v případě, že existuje určité kombinace atributů.</span><span class="sxs-lookup"><span data-stu-id="1034b-131">A price condition helps guarantee that a price expression element is included in the sales price only if a specific combination of attributes is present.</span></span>  
6. <span data-ttu-id="1034b-132">Do pole **ConstraintBody** zadejte `CabinetFinish=="Rosewood"`.</span><span class="sxs-lookup"><span data-stu-id="1034b-132">In the **ConstraintBody** field, enter `CabinetFinish=="Rosewood"`.</span></span>
7. <span data-ttu-id="1034b-133">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="1034b-133">Select **OK**.</span></span>
8. <span data-ttu-id="1034b-134">Zadejte hodnotu do pole **Výraz**.</span><span class="sxs-lookup"><span data-stu-id="1034b-134">In the **Expression** field, type a value.</span></span> <span data-ttu-id="1034b-135">Zadejte například typ `50`.</span><span class="sxs-lookup"><span data-stu-id="1034b-135">For example, type `50`.</span></span> 
9. <span data-ttu-id="1034b-136">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="1034b-136">Close the page.</span></span>

