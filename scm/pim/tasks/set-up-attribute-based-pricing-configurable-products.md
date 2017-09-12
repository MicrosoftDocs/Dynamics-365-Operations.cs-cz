--- 
title: "Nastavení ocenění podle atributů pro konfigurovatelné produkty"
description: "Tato procedura popisuje, jak nastavit ceny na základě atributů."
author: BibiSp
manager: AnnBe
ms.date: 10/12/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: b113fb639b5d7c50e519a0225b1e5d8315b7f3a9
ms.contentlocale: cs-cz
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-attribute-based-pricing-for-configurable-products"></a><span data-ttu-id="a99ba-103">Nastavení ocenění podle atributů pro konfigurovatelné produkty</span><span class="sxs-lookup"><span data-stu-id="a99ba-103">Set up attribute-based pricing for configurable products</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a99ba-104">Tato procedura popisuje, jak nastavit ceny na základě atributů.</span><span class="sxs-lookup"><span data-stu-id="a99ba-104">This procedure shows how to set up attribute-based pricing.</span></span> <span data-ttu-id="a99ba-105">Jako předpoklad musíte mít model konfigurace produktu, který má jednu nebo více komponent a atributů.</span><span class="sxs-lookup"><span data-stu-id="a99ba-105">As a prerequisite, you must have a product configuration model that has one or more components and attributes.</span></span> <span data-ttu-id="a99ba-106">Tento příklad využívá model špičkového reproduktoru v ukázkové datové společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="a99ba-106">This example uses the High End Speaker product model in the USMF demo data company.</span></span> <span data-ttu-id="a99ba-107">Manažer produktu obvykle používá tuto proceduru.</span><span class="sxs-lookup"><span data-stu-id="a99ba-107">Typically, a product manager uses this procedure.</span></span>


## <a name="create-a-new-price-model"></a><span data-ttu-id="a99ba-108">Vytvoření nového cenového modelu</span><span class="sxs-lookup"><span data-stu-id="a99ba-108">Create a new price model</span></span>
1. <span data-ttu-id="a99ba-109">Klepněte na Definice modelu varianty produktu.</span><span class="sxs-lookup"><span data-stu-id="a99ba-109">Click Product variant model definition.</span></span>
2. <span data-ttu-id="a99ba-110">Klepněte na Modely konfigurace produktu.</span><span class="sxs-lookup"><span data-stu-id="a99ba-110">Click Product configuration models.</span></span>
3. <span data-ttu-id="a99ba-111">V seznamu vyberte řádek Špičkový reproduktor, ale neklepejte na odkaz pro název.</span><span class="sxs-lookup"><span data-stu-id="a99ba-111">In the list, select the High End Speaker line, but don’t click the link for the name.</span></span>
4. <span data-ttu-id="a99ba-112">V podokně akcí klepněte na možnost Model.</span><span class="sxs-lookup"><span data-stu-id="a99ba-112">On the Action Pane, click Model.</span></span>
5. <span data-ttu-id="a99ba-113">Klikněte na Cenové modely.</span><span class="sxs-lookup"><span data-stu-id="a99ba-113">Click Price models.</span></span>
6. <span data-ttu-id="a99ba-114">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="a99ba-114">Click New.</span></span>
7. <span data-ttu-id="a99ba-115">Do pole Název modelu zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="a99ba-115">In the Price model name field, type a value.</span></span>
    * <span data-ttu-id="a99ba-116">Použijte název, který usnadňuje identifikaci modelu.</span><span class="sxs-lookup"><span data-stu-id="a99ba-116">Use a name that makes the model easy to identify.</span></span>  
8. <span data-ttu-id="a99ba-117">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="a99ba-117">In the Description field, type a value.</span></span>
9. <span data-ttu-id="a99ba-118">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="a99ba-118">Click Save.</span></span>

## <a name="add-price-elements"></a><span data-ttu-id="a99ba-119">Přidání cenových prvků</span><span class="sxs-lookup"><span data-stu-id="a99ba-119">Add price elements</span></span>
1. <span data-ttu-id="a99ba-120">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="a99ba-120">Click Edit.</span></span>
    * <span data-ttu-id="a99ba-121">Každá komponenta v produktovém modelu u může mít element základní ceny a libovolný počet pravidel výrazu ceny.</span><span class="sxs-lookup"><span data-stu-id="a99ba-121">Each component in a product model can have a base price element and any number of price expression rules.</span></span> <span data-ttu-id="a99ba-122">Můžete také přidat ceny v různých měnách.</span><span class="sxs-lookup"><span data-stu-id="a99ba-122">You can also add prices in different currencies.</span></span>  
2. <span data-ttu-id="a99ba-123">Zadejte hodnotu do pole Výraz základní ceny.</span><span class="sxs-lookup"><span data-stu-id="a99ba-123">In the Base price expression field, type a value.</span></span>
    * <span data-ttu-id="a99ba-124">Zadejte například 100.</span><span class="sxs-lookup"><span data-stu-id="a99ba-124">For example, type 100.</span></span>   <span data-ttu-id="a99ba-125">Výraz základní ceny může být číselná hodnota nebo se může skládat z aritmetického výpočtu, který zahrnuje jeden nebo více atributů.</span><span class="sxs-lookup"><span data-stu-id="a99ba-125">A base price expression can be a numerical value, or it can consist of an arithmetic calculation that involves one or more attributes.</span></span>  
3. <span data-ttu-id="a99ba-126">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="a99ba-126">Click Add.</span></span>
4. <span data-ttu-id="a99ba-127">Zadejte text „Růžové dřevo“ do pole Název.</span><span class="sxs-lookup"><span data-stu-id="a99ba-127">In the Name field, type ‘Rosewood’.</span></span>
    * <span data-ttu-id="a99ba-128">Název cenový výraz pomáhá určit, co představuje cenový prvek.</span><span class="sxs-lookup"><span data-stu-id="a99ba-128">The price expression name helps identify what the price element represents.</span></span> <span data-ttu-id="a99ba-129">V tomto příkladu vytváříme cenový prvek pro možnost Dokončení skříňky z růžového dřeva.</span><span class="sxs-lookup"><span data-stu-id="a99ba-129">In this example, we are creating a price element for the Rosewood speaker cabinet finish option.</span></span>  
5. <span data-ttu-id="a99ba-130">Klikněte na Upravit podmínku.</span><span class="sxs-lookup"><span data-stu-id="a99ba-130">Click Edit condition.</span></span>
    * <span data-ttu-id="a99ba-131">Cenové podmínky pomáhají zaručit, že prvek cenového výrazu je součástí prodejní ceny pouze v případě, že existuje určité kombinace atributů.</span><span class="sxs-lookup"><span data-stu-id="a99ba-131">A price condition helps guarantee that a price expression element is included in the sales price only if a specific combination of attributes is present.</span></span>  
6. <span data-ttu-id="a99ba-132">Do pole Základ omezení zadejte Povrchová úprava skříně == „růžové dřevo“.</span><span class="sxs-lookup"><span data-stu-id="a99ba-132">In the ConstraintBody field, enter 'CabinetFinish=="Rosewood"'.</span></span>
7. <span data-ttu-id="a99ba-133">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="a99ba-133">Click OK.</span></span>
8. <span data-ttu-id="a99ba-134">Zadejte hodnotu do pole Výraz.</span><span class="sxs-lookup"><span data-stu-id="a99ba-134">In the Expression field, type a value.</span></span>
    * <span data-ttu-id="a99ba-135">Zadejte například 50.</span><span class="sxs-lookup"><span data-stu-id="a99ba-135">For example, type 50.</span></span>  
9. <span data-ttu-id="a99ba-136">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="a99ba-136">Close the page.</span></span>
10. <span data-ttu-id="a99ba-137">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="a99ba-137">Close the page.</span></span>


