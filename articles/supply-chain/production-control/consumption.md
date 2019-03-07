---
title: Výpočet spotřeby materiálu
description: Tento článek poskytuje informace o různých volbách, které se vztahují k výpočtu spotřeby materiálu.
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMDesignerEditBOM, BOMTable, ProdBOM
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 53401
ms.assetid: 9cff88e4-0425-4707-9178-3c2cb10df7c2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3e4010b5abb6b5a871d098422f1489cb2db3a071
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "316181"
---
# <a name="calculate-material-consumption"></a><span data-ttu-id="eb1e0-103">Výpočet spotřeby materiálu</span><span class="sxs-lookup"><span data-stu-id="eb1e0-103">Calculate material consumption</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="eb1e0-104">Tento článek poskytuje informace o různých volbách, které se vztahují k výpočtu spotřeby materiálu.</span><span class="sxs-lookup"><span data-stu-id="eb1e0-104">This article provides information about various options that are related to the calculation of material consumption.</span></span> 

<span data-ttu-id="eb1e0-105">Následující možnosti, které se vztahují k výpočtu spotřeby materiálu, jsou k dispozici na kartě **Nastavení** a **Spotřeba kroku** na pevné záložce **Podrobnosti řádku** na stránce **Kusovník**.</span><span class="sxs-lookup"><span data-stu-id="eb1e0-105">The following options that are related to the calculation of material consumption are available on the **Setup** and **Step consumption** tabs on the **Line details** FastTab of the **Bill of materials** page.</span></span>

## <a name="variable-and-constant-consumption"></a><span data-ttu-id="eb1e0-106">Proměnná a konstantní spotřeba</span><span class="sxs-lookup"><span data-stu-id="eb1e0-106">Variable and constant consumption</span></span>
<span data-ttu-id="eb1e0-107">V poli **Spotřeba je** můžete určit, zda se spotřeba vypočte jako konstantní množství nebo variabilní množství.</span><span class="sxs-lookup"><span data-stu-id="eb1e0-107">In the **Consumption is** field, you can select whether consumption should be calculated as a constant quantity or a variable quantity.</span></span> <span data-ttu-id="eb1e0-108">Vyberte **Konstantní**, pokud jsou pevné množství nebo objem nutné pro výrobu, bez ohledu na vyráběné množství.</span><span class="sxs-lookup"><span data-stu-id="eb1e0-108">Select **Constant** if a fixed quantity or volume is required for the production, regardless of the quantity that is produced.</span></span> <span data-ttu-id="eb1e0-109">Vyberte **Variabilní**, což je výchozí nastavení, je-li požadované množství materiálu v dokončeném zboží úměrné počtu dokončených výrobků, které jsou vyrobeny.</span><span class="sxs-lookup"><span data-stu-id="eb1e0-109">Select **Variable**, which is the default setting, if the required amount of material in the finished goods is proportional to the number of finished goods that are produced.</span></span>

## <a name="calculating-consumption-from-a-formula"></a><span data-ttu-id="eb1e0-110">Výpočet spotřeby podle vzorce</span><span class="sxs-lookup"><span data-stu-id="eb1e0-110">Calculating consumption from a formula</span></span>
<span data-ttu-id="eb1e0-111">V poli **Vzorec** můžete nastavit různé vzorce pro výpočet spotřeby materiálu.</span><span class="sxs-lookup"><span data-stu-id="eb1e0-111">In the **Formula** field, you can set up various formulas for calculating material consumption.</span></span> <span data-ttu-id="eb1e0-112">Pokud použijete výchozí hodnotu, **Standardní**, spotřeba není vypočtena ze vzorce.</span><span class="sxs-lookup"><span data-stu-id="eb1e0-112">If you use the default value, **Standard**, the consumption isn't calculated from a formula.</span></span> <span data-ttu-id="eb1e0-113">Následující vzorce mohou pracovat spolu v polích **Výška**, **Šířka**, **Hloubka**, **Hustota** a **Konstantní**:</span><span class="sxs-lookup"><span data-stu-id="eb1e0-113">The following formulas work together with the **Height**, **Width**, **Depth**, **Density**, and **Constant** fields:</span></span>

-   <span data-ttu-id="eb1e0-114">Výška \* Konstantní</span><span class="sxs-lookup"><span data-stu-id="eb1e0-114">Height \* Constant</span></span>
-   <span data-ttu-id="eb1e0-115">Výška \* Šířka \* Konstantní</span><span class="sxs-lookup"><span data-stu-id="eb1e0-115">Height \* Width \* Constant</span></span>
-   <span data-ttu-id="eb1e0-116">Výška \* Šířka \* Hloubka \* Konstantní</span><span class="sxs-lookup"><span data-stu-id="eb1e0-116">Height \* Width \* Depth \* Constant</span></span>
-   <span data-ttu-id="eb1e0-117">(Výška \* Šířka \* Hloubka / Hustota) \* Konstantní</span><span class="sxs-lookup"><span data-stu-id="eb1e0-117">(Height \* Width \* Depth / Density) \* Constant</span></span>

## <a name="rounding-up-and-multiples"></a><span data-ttu-id="eb1e0-118">Zaokrouhlení a násobky</span><span class="sxs-lookup"><span data-stu-id="eb1e0-118">Rounding up and multiples</span></span>
<span data-ttu-id="eb1e0-119">Společně pole **Zaokrouhlení** a **Násobky** umožňují zaokrouhlování hodnoty spotřeby materiálu.</span><span class="sxs-lookup"><span data-stu-id="eb1e0-119">Together, the **Rounding up** and **Multiples** fields let you round up the material consumption value.</span></span> <span data-ttu-id="eb1e0-120">Například můžete použít zaokrouhlování hodnoty podle manipulační jednotky, ve které jsou suroviny vydané pro výrobu.</span><span class="sxs-lookup"><span data-stu-id="eb1e0-120">For example, you can round up the value according to the handling unit in which the raw material is picked for production.</span></span> <span data-ttu-id="eb1e0-121">Existují tyto možnosti v poli **Zaokrouhlení**: **Množství**, **Měření** a **Spotřeby**.</span><span class="sxs-lookup"><span data-stu-id="eb1e0-121">The following options are available in the **Rounding up** field: **Quantity**, **Measurement**, and **Consumption**.</span></span>

### <a name="quantity"></a><span data-ttu-id="eb1e0-122">Množství</span><span class="sxs-lookup"><span data-stu-id="eb1e0-122">Quantity</span></span>

<span data-ttu-id="eb1e0-123">Vyberete-li **Množství** jako mechanismus zaokrouhlování, množství musí být násobkem zadaného množství.</span><span class="sxs-lookup"><span data-stu-id="eb1e0-123">If you select **Quantity** as the rounding-up mechanism, the quantity must be a multiple of the specified quantity.</span></span> <span data-ttu-id="eb1e0-124">Jsou-li například vyžadována celá čísla, vyberte **1** v poli **Násobky**.</span><span class="sxs-lookup"><span data-stu-id="eb1e0-124">For example, if whole numbers are required, select **1** in the **Multiples** field.</span></span> <span data-ttu-id="eb1e0-125">Čísla jsou pak zaokrouhlena na množství dělitelné hodnotou 1.</span><span class="sxs-lookup"><span data-stu-id="eb1e0-125">Numbers are then rounded up to a quantity that is divisible by 1.</span></span>

### <a name="measurement"></a><span data-ttu-id="eb1e0-126">Měrný systém</span><span class="sxs-lookup"><span data-stu-id="eb1e0-126">Measurement</span></span>

<span data-ttu-id="eb1e0-127">Obvykle vyberete **Měření** jako mechanismus zaokrouhlování, pokud surovina přichází ve specifických dimenzích.</span><span class="sxs-lookup"><span data-stu-id="eb1e0-127">Typically, you select **Measurement** as the rounding-up mechanism when the raw material comes in specific dimensions.</span></span> <span data-ttu-id="eb1e0-128">Například část 2metrové kovové trubice je vyžadována pro dokončené zboží, a kovová trubice je uložena v délce 4,5 metru.</span><span class="sxs-lookup"><span data-stu-id="eb1e0-128">For example, a piece of 2-meter metal tube is required for a finished good, and the metal tube is stored in 4.5-meter lengths.</span></span> <span data-ttu-id="eb1e0-129">V takovém případě mechanismus zaokrouhlování **Měření** lze použít k výpočtu toho, kolik kovových trubek je zapotřebí pro výrobu určitého počtu kusů dokončeného zboží.</span><span class="sxs-lookup"><span data-stu-id="eb1e0-129">In this case, the **Measurement** rounding-up mechanism can be used to calculate how many metal tubes are required to produce a specific number of pieces of the finished good.</span></span> <span data-ttu-id="eb1e0-130">V tomto příkladu je pole **Vzorec** nastaveno na **Výška \* Konstantní**.</span><span class="sxs-lookup"><span data-stu-id="eb1e0-130">For this example, the **Formula** field is set to **Height \* Constant**.</span></span> <span data-ttu-id="eb1e0-131">Pole **Výška** je nastaveno na **2** pro označení délky trubky potřebné k dokončení výrobku.</span><span class="sxs-lookup"><span data-stu-id="eb1e0-131">The **Height** field is set to **2** to indicate the length of the tube that is required for the finished good.</span></span> <span data-ttu-id="eb1e0-132">Pole **Více** je nastaveno na **4,5** a označuje tak, že je trubice vydaná v délkách po 4,5 metrech.</span><span class="sxs-lookup"><span data-stu-id="eb1e0-132">The **Multiple** field is set to **4.5** to indicate that the tube is picked in lengths of 4.5 meters.</span></span> <span data-ttu-id="eb1e0-133">Kalkulace je tato:</span><span class="sxs-lookup"><span data-stu-id="eb1e0-133">Here is the calculation:</span></span>

1.  <span data-ttu-id="eb1e0-134">Počet násobků, které jsou požadovány pro 10 kusů dokončeného zboží: 10 ÷ 2 = 5 kusů</span><span class="sxs-lookup"><span data-stu-id="eb1e0-134">Number of multiples that are required for 10 pieces of the finished good: 10 ÷ 2 = 5 pieces</span></span>
2.  <span data-ttu-id="eb1e0-135">Celková spotřeba: 4,5 x 5 = 22,5 metru kovové trubice</span><span class="sxs-lookup"><span data-stu-id="eb1e0-135">Total consumption:  4.5 × 5 = 22.5 meters of metal tube</span></span>

<span data-ttu-id="eb1e0-136">Předpokládá se, že, 0,5 metru trubice je vyřazeno pro každých pět částí trubice, která je spotřebována.</span><span class="sxs-lookup"><span data-stu-id="eb1e0-136">It's assumed that 0.5 meter of tube is scrapped for every five pieces of tube that are consumed.</span></span>

### <a name="consumption"></a><span data-ttu-id="eb1e0-137">Spotřeba</span><span class="sxs-lookup"><span data-stu-id="eb1e0-137">Consumption</span></span>

<span data-ttu-id="eb1e0-138">Obvykle vyberete**Spotřeba** jako mechanismus zaokrouhlování, když musí být suroviny vyskladněny v celém množství konkrétní manipulační jednotky produktu.</span><span class="sxs-lookup"><span data-stu-id="eb1e0-138">Typically, you select **Consumption** as the rounding-up mechanism when raw material must be picked in whole quantities of a specific handling unit of the product.</span></span> <span data-ttu-id="eb1e0-139">Například k výrobě jednoho kusu dokončeného zboží jsou použity 2 plechovky barvy a barva je vydána v 25litrových plechovkách.</span><span class="sxs-lookup"><span data-stu-id="eb1e0-139">For example, 2 quarts of paint are used to produce one piece of a finished good, and the paint is picked in 25-quart cans.</span></span> <span data-ttu-id="eb1e0-140">V takovém případě mechanismus zaokrouhlování **Spotřeba** lze použít k zaokrouhlení spotřeby nahoru na celá čísla 25litrových plechovek.</span><span class="sxs-lookup"><span data-stu-id="eb1e0-140">In this case, the **Consumption** rounding-up mechanism can be used to round up consumption to whole numbers of 25-quart cans.</span></span> <span data-ttu-id="eb1e0-141">Následuje výpočet množství barvy, která je vyžadována, pokud je třeba vyrobit 180 kusů dokončeného zboží:</span><span class="sxs-lookup"><span data-stu-id="eb1e0-141">Here is the calculation for the amount of paint that is required if 180 pieces of the finished good must be produced:</span></span>

1.  <span data-ttu-id="eb1e0-142">Barva, která je nutná (bez odpadu): 180 x 2 = 360 plechovek</span><span class="sxs-lookup"><span data-stu-id="eb1e0-142">Paint that is required, excluding scrap: 180 × 2 = 360 quarts</span></span>
2.  <span data-ttu-id="eb1e0-143">Počet plechovek: 360 ÷ 25 = 14,4, což je zaokrouhleno 15.</span><span class="sxs-lookup"><span data-stu-id="eb1e0-143">Number of cans: 360 ÷ 25 = 14.4, which is rounded up to 15</span></span>
3.  <span data-ttu-id="eb1e0-144">Barva, která je nutná (včetně odpadu): 15 x 25 = 375 plechovek</span><span class="sxs-lookup"><span data-stu-id="eb1e0-144">Paint that is required, including scrap: 15 × 25 = 375 quarts</span></span>

## <a name="step-consumption"></a><span data-ttu-id="eb1e0-145">Spotřeba kroku</span><span class="sxs-lookup"><span data-stu-id="eb1e0-145">Step consumption</span></span>
<span data-ttu-id="eb1e0-146">Spotřeba kroku se používá k výpočtu konstantní spotřeby v intervalech množství.</span><span class="sxs-lookup"><span data-stu-id="eb1e0-146">Step consumption is used to calculate constant consumption in quantity intervals.</span></span> <span data-ttu-id="eb1e0-147">Vyberete-li **Spotřeba kroku** v poli **Vzorec** na kartě **Nastavení**, můžete přidat informace o krocích na kartě **Spotřeba kroku**. Pevné spotřebované množství lze nastavit v intervalech vyrobeného množství.</span><span class="sxs-lookup"><span data-stu-id="eb1e0-147">If you select **Step consumption** in the **Formula** field on the **Setup** tab, you can add information about the steps on the **Step consumption** tab. The fixed consumed quantity can be set up in intervals of the produced quantity.</span></span> <span data-ttu-id="eb1e0-148">Například spotřeba kroku je nastavena způsobem znázorněným v následující tabulce.</span><span class="sxs-lookup"><span data-stu-id="eb1e0-148">For example, step consumption is set up as shown in the following table.</span></span>

| <span data-ttu-id="eb1e0-149">Od řady</span><span class="sxs-lookup"><span data-stu-id="eb1e0-149">From series</span></span> | <span data-ttu-id="eb1e0-150">Množství</span><span class="sxs-lookup"><span data-stu-id="eb1e0-150">Quantity</span></span> |
|-------------|----------|
| <span data-ttu-id="eb1e0-151">0,00</span><span class="sxs-lookup"><span data-stu-id="eb1e0-151">0.00</span></span>        | <span data-ttu-id="eb1e0-152">10,0000</span><span class="sxs-lookup"><span data-stu-id="eb1e0-152">10.0000</span></span>  |
| <span data-ttu-id="eb1e0-153">100,00</span><span class="sxs-lookup"><span data-stu-id="eb1e0-153">100.00</span></span>      | <span data-ttu-id="eb1e0-154">20,0000</span><span class="sxs-lookup"><span data-stu-id="eb1e0-154">20.0000</span></span>  |
| <span data-ttu-id="eb1e0-155">200,00</span><span class="sxs-lookup"><span data-stu-id="eb1e0-155">200.00</span></span>      | <span data-ttu-id="eb1e0-156">40,0000</span><span class="sxs-lookup"><span data-stu-id="eb1e0-156">40.0000</span></span>  |

<span data-ttu-id="eb1e0-157">Množství kusovníku je 1 a výrobní množství je 110.</span><span class="sxs-lookup"><span data-stu-id="eb1e0-157">The bill of materials (BOM) quantity is 1, and the production quantity is 110.</span></span> <span data-ttu-id="eb1e0-158">Vzorec pro spotřebu je Z řady (Množství) = Spotřeba.</span><span class="sxs-lookup"><span data-stu-id="eb1e0-158">The formula for the consumption is From series (Quantity) = Consumption.</span></span> <span data-ttu-id="eb1e0-159">Protože výrobní množství je 110, spadá do kategorie "Ze série 100".</span><span class="sxs-lookup"><span data-stu-id="eb1e0-159">Because the production quantity is 110, it falls into the "From 100 series."</span></span> <span data-ttu-id="eb1e0-160">Množství je proto 20.</span><span class="sxs-lookup"><span data-stu-id="eb1e0-160">Therefore, the quantity is 20.</span></span>



