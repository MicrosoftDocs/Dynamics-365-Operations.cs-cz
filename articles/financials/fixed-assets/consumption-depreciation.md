---
title: "Odpis spotřeby"
description: "Tento článek poskytuje přehled o metodě odpisu spotřeby."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 13751
ms.assetid: d25a681f-49a5-4bfc-aa76-1c6373e35dd8
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 0c48877058edf8251ef6eb5dd63d7eecd1866f33
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---

# <a name="consumption-depreciation"></a><span data-ttu-id="463fe-103">Odpis spotřeby</span><span class="sxs-lookup"><span data-stu-id="463fe-103">Consumption depreciation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="463fe-104">Tento článek poskytuje přehled o metodě odpisu spotřeby.</span><span class="sxs-lookup"><span data-stu-id="463fe-104">This article gives an overview of the Consumption method of depreciation.</span></span>

<span data-ttu-id="463fe-105">Když vytvoříte odpisový plán pro dlouhodobý majetek a vyberete položku **Spotřeba** v poli **Metoda** ve formuláři **Odpisové plány**, budou dlouhodobé majetky přiřazeny k odpisovému plánu podle jejich používání.</span><span class="sxs-lookup"><span data-stu-id="463fe-105">If you set up a depreciation profile for fixed assets and select **Consumption** in the **Method** field on the **Depreciation profiles** page, fixed assets are assigned to the depreciation profile based on their usage.</span></span> <span data-ttu-id="463fe-106">Na stránce **Odpisové plány** není nutné nastavovat procenta a intervaly.</span><span class="sxs-lookup"><span data-stu-id="463fe-106">You don't have to set up percentages and intervals on the **Depreciation profiles** page.</span></span> <span data-ttu-id="463fe-107">Po vytvoření odpisového plánu využívajícího metodu Spotřeba můžete metodu nastavit několika způsoby.</span><span class="sxs-lookup"><span data-stu-id="463fe-107">After you create a depreciation profile that uses the Consumption method, you can set up the method in various ways.</span></span>

## <a name="set-up-and-use-consumption-depreciation"></a><span data-ttu-id="463fe-108">Nastavení a použití odpisu spotřeby</span><span class="sxs-lookup"><span data-stu-id="463fe-108">Set up and use consumption depreciation</span></span>
1.  <span data-ttu-id="463fe-109">Na stránce **Odpisové plány** vytvořte odpisový plán.</span><span class="sxs-lookup"><span data-stu-id="463fe-109">On the **Depreciation profiles** page, create the depreciation profile.</span></span> <span data-ttu-id="463fe-110">Pro výpočet spotřeby musí odpisový plán obsahovat ID a název a v poli **Metoda** musí být zvolena možnost **Spotřeba**.</span><span class="sxs-lookup"><span data-stu-id="463fe-110">For consumption calculations, the depreciation profile must have an ID and a name, and **Consumption** must be selected in the **Method** field.</span></span>
2.  <span data-ttu-id="463fe-111">Na stránce  **Koeficienty spotřeby** nastavte koeficienty spotřeby.</span><span class="sxs-lookup"><span data-stu-id="463fe-111">On the **Consumption factors** page, set up consumption factors.</span></span> <span data-ttu-id="463fe-112">Každý koeficient spotřeby musí mít ID a název a koeficient spotřeby, který je zadán jako množství nebo jako procento.</span><span class="sxs-lookup"><span data-stu-id="463fe-112">Each consumption factor must have an ID and a name, and a consumption factor that is specified as either a quantity or a percentage.</span></span>
3.  <span data-ttu-id="463fe-113">Na stránce **Jednotky spotřeby** nastavte jednotky spotřeby.</span><span class="sxs-lookup"><span data-stu-id="463fe-113">On the **Consumption units** page, set up consumption units.</span></span> <span data-ttu-id="463fe-114">Každá jednotka spotřeby musí mít ID a název.</span><span class="sxs-lookup"><span data-stu-id="463fe-114">Each consumption unit must have an ID and a name.</span></span> <span data-ttu-id="463fe-115">Na stránce **Odpis spotřeby** se pro výpočet odpisu spotřeby používají odpisové jednotky.</span><span class="sxs-lookup"><span data-stu-id="463fe-115">Depreciation units are used to calculate consumption depreciation on the **Consumption depreciation** page.</span></span> <span data-ttu-id="463fe-116">Příklady jednotek jsou kilometr (km), kilogram (kg) nebo hodina.</span><span class="sxs-lookup"><span data-stu-id="463fe-116">Examples of units are kilometer (km), kilogram (kg), and hour.</span></span>
4.  <span data-ttu-id="463fe-117">Na stránce **Dlouhodobý majetek** nastavte jednotlivé položky dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="463fe-117">On the **Fixed assets** page, set up individual fixed assets.</span></span> <span data-ttu-id="463fe-118">Pro každý dlouhodobý majetek zvolte oceňovací model a knihu odpisů, které mají odpisový plán.</span><span class="sxs-lookup"><span data-stu-id="463fe-118">For each fixed asset, select value models and depreciation books that have depreciation profiles.</span></span> <span data-ttu-id="463fe-119">Pokud některý z vašich dlouhodobých majetků používá odpisové plány založené na metodě Spotřeba, je nutné nastavit oceňovací model nebo knihy odpisů pro odpis spotřeby.</span><span class="sxs-lookup"><span data-stu-id="463fe-119">You must set up value models or depreciation books for consumption depreciation if any of your fixed assets use depreciation profiles that are based on the Consumption method.</span></span> <span data-ttu-id="463fe-120">Toto nastavení se provádí buď na kartě **Odpisy** na stránce **Oceňovací modely**, nebo na pevné záložce **Obecné** na stránce **Odpisový plán**.</span><span class="sxs-lookup"><span data-stu-id="463fe-120">This setup is done either on the **Depreciation** tab of the **Value models** page or on the **General** FastTab of the **Depreciation profile** page.</span></span> <span data-ttu-id="463fe-121">Stejný oceňovací model můžete použít pro více položek dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="463fe-121">You can use the same value model for multiple fixed assets.</span></span> <span data-ttu-id="463fe-122">Odpisové plány tvoří součást oceňovacího modelu nebo knihy odpisů, které jsou vybrány pro každý dlouhodobý majetek.</span><span class="sxs-lookup"><span data-stu-id="463fe-122">Depreciation profiles are part of the value model or depreciation book that you select for each fixed asset.</span></span> <span data-ttu-id="463fe-123">Profily nelze přidávat ani upravovat přímo na stránce **Dlouhodobý majetek**.</span><span class="sxs-lookup"><span data-stu-id="463fe-123">You can't add or modify depreciation profiles directly on the **Fixed assets** page.</span></span> <span data-ttu-id="463fe-124">Odpisové profily je možné upravovat pouze na stránce **Knihy odpisů**.</span><span class="sxs-lookup"><span data-stu-id="463fe-124">You can modify depreciation profiles only on the **Depreciation books** page.</span></span>
5.  <span data-ttu-id="463fe-125">Na stránce **Oceňovací modely** nebo na stránce **Odpisové knihy** zadejte do skupiny polí **Odpis spotřeby** tyto informace:</span><span class="sxs-lookup"><span data-stu-id="463fe-125">On the **Value models** page or the **Depreciation books** page, in the **Consumption depreciation** field group, enter information in the following fields:</span></span>
    -   <span data-ttu-id="463fe-126">Koeficient spotřeby</span><span class="sxs-lookup"><span data-stu-id="463fe-126">Consumption factor</span></span>
    -   <span data-ttu-id="463fe-127">Jednotka</span><span class="sxs-lookup"><span data-stu-id="463fe-127">Unit</span></span>
    -   <span data-ttu-id="463fe-128">Jednotkový odpis</span><span class="sxs-lookup"><span data-stu-id="463fe-128">Unit depreciation</span></span>
    -   <span data-ttu-id="463fe-129">Odhadovaná spotřeba</span><span class="sxs-lookup"><span data-stu-id="463fe-129">Estimated consumption</span></span>

    <span data-ttu-id="463fe-130">V poli **Zaúčtovaná spotřeba** se zobrazuje odpis spotřeby v jednotkách, které již byly zaúčtovány buď pro kombinaci dlouhodobého majetku a oceňovacího modelu, nebo pro knihu odpisů.</span><span class="sxs-lookup"><span data-stu-id="463fe-130">The **Posted consumption** field shows the consumption depreciation, in units, that has already been posted either for the combination of the fixed asset and value model, or for the depreciation book.</span></span> <span data-ttu-id="463fe-131">Hodnotu v tomto poli nelze ručně upravit.</span><span class="sxs-lookup"><span data-stu-id="463fe-131">You can't manually update the value in this field.</span></span>

## <a name="examples"></a><span data-ttu-id="463fe-132">Příklad</span><span class="sxs-lookup"><span data-stu-id="463fe-132">Examples</span></span>
### <a name="example-1"></a><span data-ttu-id="463fe-133">Příklad 1</span><span class="sxs-lookup"><span data-stu-id="463fe-133">Example 1</span></span>

<span data-ttu-id="463fe-134">Následující koeficient spotřeby je nastaven na 31. leden:</span><span class="sxs-lookup"><span data-stu-id="463fe-134">The following consumption factor is set up for January 31:</span></span>

-   <span data-ttu-id="463fe-135">Množství je 1 000.</span><span class="sxs-lookup"><span data-stu-id="463fe-135">The quantity is 1,000.</span></span>
-   <span data-ttu-id="463fe-136">Odpisová cena jednotky, která je určena pro dlouhodobý majetek, je 1,5.</span><span class="sxs-lookup"><span data-stu-id="463fe-136">The unit depreciation price that is specified for the fixed asset is 1.5.</span></span>

<span data-ttu-id="463fe-137">Návrh odpisu dne 31. ledna vypadá takto: množství × jednotkový odpis 1 000 × 1,5 = 1 500. Jestliže je pro dlouhodobý majetek nastaven procentuální koeficient, bude odhadované množství v poli **Odhadovaná spotřeba** pro oceňovací model dlouhodobého majetku vynásobeno procentem, které je nastaveno pro vybrané koncové datum.</span><span class="sxs-lookup"><span data-stu-id="463fe-137">The depreciation proposal on January 31 is as follows: Quantity × Unit depreciation 1,000 × 1.5 = 1,500 If the factor that is specified for the fixed asset is a percentage factor, the quantity that is estimated in the **Estimated consumption** field for the value model of the fixed asset is multiplied by the percentage that is set up for the selected end date.</span></span> <span data-ttu-id="463fe-138">Výsledné množství je pak navrženo jako odpisové množství pro dané období.</span><span class="sxs-lookup"><span data-stu-id="463fe-138">The resulting quantity is then suggested as the depreciation quantity for the period.</span></span>

### <a name="example-2"></a><span data-ttu-id="463fe-139">Příklad 2</span><span class="sxs-lookup"><span data-stu-id="463fe-139">Example 2</span></span>

<span data-ttu-id="463fe-140">Následující koeficient pro odpis spotřeby je nastaven na 31. leden:</span><span class="sxs-lookup"><span data-stu-id="463fe-140">The following factor for consumption depreciation is set up for January 31:</span></span>

-   <span data-ttu-id="463fe-141">Procentuální hodnota činí 10 procent.</span><span class="sxs-lookup"><span data-stu-id="463fe-141">The percentage is 10 percent.</span></span>
-   <span data-ttu-id="463fe-142">Odpisová cena jednotky, která je určena pro dlouhodobý majetek, je 1,5.</span><span class="sxs-lookup"><span data-stu-id="463fe-142">The unit depreciation price that is specified for the fixed asset is 1.5.</span></span>
-   <span data-ttu-id="463fe-143">Odhadované množství dlouhodobého majetku je 2 000.</span><span class="sxs-lookup"><span data-stu-id="463fe-143">The estimated quantity of the fixed asset is 2,000.</span></span>

<span data-ttu-id="463fe-144">Odpisový plán 31. ledna vypadá takto: odhadované množství × procento × jednotkový odpis 2 000 × 0,10 × 1,5 = 300</span><span class="sxs-lookup"><span data-stu-id="463fe-144">The depreciation proposal on January 31 is as follows: Estimated quantity × Percentage × Unit depreciation 2,000 × .10 × 1.5 = 300</span></span>




