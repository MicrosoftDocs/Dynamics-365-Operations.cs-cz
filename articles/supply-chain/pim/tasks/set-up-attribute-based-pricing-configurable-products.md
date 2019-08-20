---
title: Nastavení ocenění podle atributů pro konfigurovatelné produkty
description: Tato procedura popisuje, jak nastavit ceny na základě atributů.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelList, PCPriceModel, PCConstraintEditor
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ba84fa4de660d16b266763fff5b0b794ed327c81
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/01/2019
ms.locfileid: "1844194"
---
# <a name="set-up-attribute-based-pricing-for-configurable-products"></a><span data-ttu-id="e533d-103">Nastavení ocenění podle atributů pro konfigurovatelné produkty</span><span class="sxs-lookup"><span data-stu-id="e533d-103">Set up attribute-based pricing for configurable products</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e533d-104">Tato procedura popisuje, jak nastavit ceny na základě atributů.</span><span class="sxs-lookup"><span data-stu-id="e533d-104">This procedure shows how to set up attribute-based pricing.</span></span> <span data-ttu-id="e533d-105">Jako předpoklad musíte mít model konfigurace produktu, který má jednu nebo více komponent a atributů.</span><span class="sxs-lookup"><span data-stu-id="e533d-105">As a prerequisite, you must have a product configuration model that has one or more components and attributes.</span></span> <span data-ttu-id="e533d-106">Tento příklad využívá model špičkového reproduktoru v ukázkové datové společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="e533d-106">This example uses the High End Speaker product model in the USMF demo data company.</span></span> <span data-ttu-id="e533d-107">Manažer produktu obvykle používá tuto proceduru.</span><span class="sxs-lookup"><span data-stu-id="e533d-107">Typically, a product manager uses this procedure.</span></span>


## <a name="create-a-new-price-model"></a><span data-ttu-id="e533d-108">Vytvoření nového cenového modelu</span><span class="sxs-lookup"><span data-stu-id="e533d-108">Create a new price model</span></span>
1. <span data-ttu-id="e533d-109">Klepněte na Definice modelu varianty produktu.</span><span class="sxs-lookup"><span data-stu-id="e533d-109">Click Product variant model definition.</span></span>
2. <span data-ttu-id="e533d-110">Klepněte na Modely konfigurace produktu.</span><span class="sxs-lookup"><span data-stu-id="e533d-110">Click Product configuration models.</span></span>
3. <span data-ttu-id="e533d-111">V seznamu vyberte řádek Špičkový reproduktor, ale neklepejte na odkaz pro název.</span><span class="sxs-lookup"><span data-stu-id="e533d-111">In the list, select the High End Speaker line, but don’t click the link for the name.</span></span>
4. <span data-ttu-id="e533d-112">V podokně akcí klepněte na možnost Model.</span><span class="sxs-lookup"><span data-stu-id="e533d-112">On the Action Pane, click Model.</span></span>
5. <span data-ttu-id="e533d-113">Klikněte na Cenové modely.</span><span class="sxs-lookup"><span data-stu-id="e533d-113">Click Price models.</span></span>
6. <span data-ttu-id="e533d-114">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="e533d-114">Click New.</span></span>
7. <span data-ttu-id="e533d-115">Do pole Název modelu zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="e533d-115">In the Price model name field, type a value.</span></span>
    * <span data-ttu-id="e533d-116">Použijte název, který usnadňuje identifikaci modelu.</span><span class="sxs-lookup"><span data-stu-id="e533d-116">Use a name that makes the model easy to identify.</span></span>  
8. <span data-ttu-id="e533d-117">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="e533d-117">In the Description field, type a value.</span></span>
9. <span data-ttu-id="e533d-118">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="e533d-118">Click Save.</span></span>

## <a name="add-price-elements"></a><span data-ttu-id="e533d-119">Přidání cenových prvků</span><span class="sxs-lookup"><span data-stu-id="e533d-119">Add price elements</span></span>
1. <span data-ttu-id="e533d-120">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="e533d-120">Click Edit.</span></span>
    * <span data-ttu-id="e533d-121">Každá komponenta v produktovém modelu u může mít element základní ceny a libovolný počet pravidel výrazu ceny.</span><span class="sxs-lookup"><span data-stu-id="e533d-121">Each component in a product model can have a base price element and any number of price expression rules.</span></span> <span data-ttu-id="e533d-122">Můžete také přidat ceny v různých měnách.</span><span class="sxs-lookup"><span data-stu-id="e533d-122">You can also add prices in different currencies.</span></span>  
2. <span data-ttu-id="e533d-123">Zadejte hodnotu do pole Výraz základní ceny.</span><span class="sxs-lookup"><span data-stu-id="e533d-123">In the Base price expression field, type a value.</span></span>
    * <span data-ttu-id="e533d-124">Zadejte například 100.</span><span class="sxs-lookup"><span data-stu-id="e533d-124">For example, type 100.</span></span>   <span data-ttu-id="e533d-125">Výraz základní ceny může být číselná hodnota nebo se může skládat z aritmetického výpočtu, který zahrnuje jeden nebo více atributů.</span><span class="sxs-lookup"><span data-stu-id="e533d-125">A base price expression can be a numerical value, or it can consist of an arithmetic calculation that involves one or more attributes.</span></span>  
3. <span data-ttu-id="e533d-126">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="e533d-126">Click Add.</span></span>
4. <span data-ttu-id="e533d-127">Zadejte text „Růžové dřevo“ do pole Název.</span><span class="sxs-lookup"><span data-stu-id="e533d-127">In the Name field, type ‘Rosewood’.</span></span>
    * <span data-ttu-id="e533d-128">Název cenový výraz pomáhá určit, co představuje cenový prvek.</span><span class="sxs-lookup"><span data-stu-id="e533d-128">The price expression name helps identify what the price element represents.</span></span> <span data-ttu-id="e533d-129">V tomto příkladu vytváříme cenový prvek pro možnost Dokončení skříňky z růžového dřeva.</span><span class="sxs-lookup"><span data-stu-id="e533d-129">In this example, we are creating a price element for the Rosewood speaker cabinet finish option.</span></span>  
5. <span data-ttu-id="e533d-130">Klikněte na Upravit podmínku.</span><span class="sxs-lookup"><span data-stu-id="e533d-130">Click Edit condition.</span></span>
    * <span data-ttu-id="e533d-131">Cenové podmínky pomáhají zaručit, že prvek cenového výrazu je součástí prodejní ceny pouze v případě, že existuje určité kombinace atributů.</span><span class="sxs-lookup"><span data-stu-id="e533d-131">A price condition helps guarantee that a price expression element is included in the sales price only if a specific combination of attributes is present.</span></span>  
6. <span data-ttu-id="e533d-132">Do pole Základ omezení zadejte Povrchová úprava skříně == „růžové dřevo“.</span><span class="sxs-lookup"><span data-stu-id="e533d-132">In the ConstraintBody field, enter 'CabinetFinish=="Rosewood"'.</span></span>
7. <span data-ttu-id="e533d-133">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="e533d-133">Click OK.</span></span>
8. <span data-ttu-id="e533d-134">Zadejte hodnotu do pole Výraz.</span><span class="sxs-lookup"><span data-stu-id="e533d-134">In the Expression field, type a value.</span></span>
    * <span data-ttu-id="e533d-135">Zadejte například 50.</span><span class="sxs-lookup"><span data-stu-id="e533d-135">For example, type 50.</span></span>  
9. <span data-ttu-id="e533d-136">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="e533d-136">Close the page.</span></span>
10. <span data-ttu-id="e533d-137">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="e533d-137">Close the page.</span></span>

