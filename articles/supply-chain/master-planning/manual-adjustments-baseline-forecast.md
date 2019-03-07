---
title: Ruční úpravy základní prognózy
description: Toto téma vysvětluje, jak lze provádět ruční úpravy v základní prognóze, a jak zobrazit podrobnosti o prognóze.
author: roxanadiaconu
manager: AnnBe
ms.date: 11/02/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanForecastViewer
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 72704
ms.assetid: e7c5d44e-07bc-40b1-a4b3-8ba46483ef9e
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a7c7d1fcaaeef7a01b43886e4d69458dbd942439
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "315882"
---
# <a name="make-manual-adjustments-to-the-baseline-forecast"></a><span data-ttu-id="7aef7-103">Ruční úpravy základní prognózy</span><span class="sxs-lookup"><span data-stu-id="7aef7-103">Make manual adjustments to the baseline forecast</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7aef7-104">Toto téma vysvětluje, jak lze provádět ruční úpravy v základní prognóze, a jak zobrazit podrobnosti o prognóze.</span><span class="sxs-lookup"><span data-stu-id="7aef7-104">This topic explains how you can make manual adjustments to a baseline forecast and view details of the forecast.</span></span> 

<span data-ttu-id="7aef7-105">Dříve, než začnete provádět ruční úpravy, je třeba mít na paměti několik konceptů z různých stran.</span><span class="sxs-lookup"><span data-stu-id="7aef7-105">Before you make manual adjustments, it's important that you understand a few concepts on various pages.</span></span>

## <a name="grid-on-the-adjusted-demand-forecast-page"></a><span data-ttu-id="7aef7-106">Tabulka na stránce Upravená prognóza poptávky</span><span class="sxs-lookup"><span data-stu-id="7aef7-106">Grid on the Adjusted demand forecast page</span></span>
<span data-ttu-id="7aef7-107">Stránka **Upravená prognóza poptávky** obsahuje tabulku, která obsahuje následující strukturu:</span><span class="sxs-lookup"><span data-stu-id="7aef7-107">The **Adjusted demand forecast** page includes a grid that has the following structure:</span></span>

-   <span data-ttu-id="7aef7-108">V prvním sloupci se zobrazují položky, alokační klíče položky, společnosti apod., pro které je prognóza generována.</span><span class="sxs-lookup"><span data-stu-id="7aef7-108">The first column shows the items, item allocation keys, companies, and so on, that the forecast has been generated for.</span></span> <span data-ttu-id="7aef7-109">Podtitulek stránky obsahuje popis aktuálních dimenzí prognózy, které jsou zobrazeny v mřížce.</span><span class="sxs-lookup"><span data-stu-id="7aef7-109">The subtitle of the page provides a description of the current forecast dimensions that are shown in the grid.</span></span> <span data-ttu-id="7aef7-110">Například, když je podnadpis stránky **Společnost / pracoviště / alokační klíč položky** a jedno ze záhlaví sloupců v mřížce je **USMF / 1 / D\_Alloc**, daný řádek popisuje prognózu pro společnost, s pracovištěm 1 a alokačním klíčem položky **D\_Alloc**.</span><span class="sxs-lookup"><span data-stu-id="7aef7-110">For example, if the subtitle of the page is **Company / Site / Item allocation key**, and one of the row headers in the grid is **USMF / 1 / D\_Alloc**, that row shows the forecast for the USMF company, site 1, and the **D\_Alloc** item allocation key.</span></span>
-   <span data-ttu-id="7aef7-111">Další sloupce představují intervaly prognóz, pro které jsou prognózy generované.</span><span class="sxs-lookup"><span data-stu-id="7aef7-111">Subsequent columns represent the forecast buckets that the forecast has been generated for.</span></span> <span data-ttu-id="7aef7-112">Záhlaví každého sloupce je první datem intervalu prognózy, který je zobrazen ve sloupci.</span><span class="sxs-lookup"><span data-stu-id="7aef7-112">Each column header is the first date of the forecast bucket that the column shows.</span></span>
-   <span data-ttu-id="7aef7-113">Hodnoty buněk představují prognózu pro jednu položku, alokační klíč položky a tak dále, pro tento konkrétní interval prognózy.</span><span class="sxs-lookup"><span data-stu-id="7aef7-113">The values in the cells represent the forecast for one item, item allocation key, and so on, for that specific forecast bucket.</span></span>

## <a name="forecast-aggregation-and-de-aggregation"></a><span data-ttu-id="7aef7-114">Seskupení a zrušení seskupení prognózy</span><span class="sxs-lookup"><span data-stu-id="7aef7-114">Forecast aggregation and de-aggregation</span></span>
<span data-ttu-id="7aef7-115">Podtitulek stránky popisuje úroveň seskupení prognózy.</span><span class="sxs-lookup"><span data-stu-id="7aef7-115">The subtitle of the page shows the level of forecast aggregation.</span></span> 

<span data-ttu-id="7aef7-116">Například pokud je podnadpis stránky **Společnost / pracoviště / alokační klíč / číslo položky / barva / velikost / konfigurace / styl**, neexistuje žádná agregace prognózy a prognóza se zobrazí na úrovni položky a jejích dimenzích.</span><span class="sxs-lookup"><span data-stu-id="7aef7-116">For example, if the subtitle of the page is **Company / Site / Allocation key / Item number / Color / Size / Configuration / Style**, there is no forecast aggregation, and the forecast is shown at the level of the item and its dimensions.</span></span> <span data-ttu-id="7aef7-117">Pokud chcete změnit agregaci, použijte stránku **Změna dimenzí prognózy**, kterou lze otevřít z nabídky aplikace.</span><span class="sxs-lookup"><span data-stu-id="7aef7-117">To change the aggregation, use the **Change forecast dimensions** page, which you can open from the application menu.</span></span> 

<span data-ttu-id="7aef7-118">Pokud chcete upravit prognózu, klikněte na libovolnou buňku, která je k dispozici, a zadejte upravenou hodnotu prognózy.</span><span class="sxs-lookup"><span data-stu-id="7aef7-118">To modify the forecast, click in any of the cells that are available, and type the adjusted forecast value.</span></span> <span data-ttu-id="7aef7-119">Upravená buňka bude okamžitě zobrazena tučně a označí tak, že uvedená prognóza není prognózou vytvořenou ve službě generování prognózy poptávky, ale že je ručně upravená.</span><span class="sxs-lookup"><span data-stu-id="7aef7-119">The edited cell immediately becomes bold to indicate that the forecast that it shows isn't the forecast that the demand forecasting service created, but has been manually adjusted.</span></span> 

<span data-ttu-id="7aef7-120">Pokud změníte agregaci v situaci, kdy chcete zobrazit více agregovaná data, můžete použít stránku **Řádky prognózy poptávky** a zobrazit tak jednotlivé řádky prognóz, které tvoří agregovanou prognózu.</span><span class="sxs-lookup"><span data-stu-id="7aef7-120">If you change the aggregation to make the page show more aggregated data, you can use the **Demand forecast lines** page to see the individual forecast lines that make up the aggregated forecast.</span></span> 

<span data-ttu-id="7aef7-121">Například jste vygenerovali prognózu na úrovni položky, ale víte, že poptávka pro tuto položku se zvýší pro všechna pracoviště z důvodu povýšení nebo jiné podobné události.</span><span class="sxs-lookup"><span data-stu-id="7aef7-121">For example, you've generated the forecast at the item level, but you know that the demand for this item will increase across all sites because of a promotion or another similar event.</span></span> <span data-ttu-id="7aef7-122">V tomto případě můžete nastavit agregaci na **Společnost / alokační klíč položky / položka** na stránce **Změna dimenzí prognózy**.</span><span class="sxs-lookup"><span data-stu-id="7aef7-122">In this case, you can set the aggregation to **Company / Item allocation key / Item** on the **Change forecast dimensions** page.</span></span> <span data-ttu-id="7aef7-123">V mřížce **Upravená prognóza poptávky** můžete nastavit globální prognózu pro položku pro všechna pracoviště.</span><span class="sxs-lookup"><span data-stu-id="7aef7-123">You can adjust the global forecast for the item across all sites in the **Adjusted demand forecast** grid.</span></span> <span data-ttu-id="7aef7-124">Chcete-li vidět změny pro všechna pracoviště, otevřete stránku **Řádky prognózy poptávky**.</span><span class="sxs-lookup"><span data-stu-id="7aef7-124">To see the effect of your change across all sites, open the **Demand forecast lines** page.</span></span> <span data-ttu-id="7aef7-125">Na této stránce uvidíte jeden řádek pro položku pro každé pracoviště, upravené množství prognózy a původní množství prognózy.</span><span class="sxs-lookup"><span data-stu-id="7aef7-125">On this page, you will see one line for the item for each site, the adjusted forecast quantity, and the original forecast quantity.</span></span> 

<span data-ttu-id="7aef7-126">Po provedení úprav prognózy na agregační úrovni použije systém vážené přidělení a rozdělí změny mezi řádky tvořící agregaci.</span><span class="sxs-lookup"><span data-stu-id="7aef7-126">When the adjustment of the forecasted quantity is made at an aggregated level, the system uses weighted allocation to distribute the change among the lines that create the aggregation.</span></span> 

<span data-ttu-id="7aef7-127">Můžete provést také ruční úpravy na stránce **Řádky prognózy poptávky**, a to změnou buď buňky **Celkové množství** nebo **Množství** v mřížce pro zrušení agregace.</span><span class="sxs-lookup"><span data-stu-id="7aef7-127">You can also make manual adjustments on the **Demand forecast lines** page, by modifying either the **Total quantity** value or the **Quantity** cells in the de-aggregation grid.</span></span>

## <a name="viewing-details-of-the-forecast"></a><span data-ttu-id="7aef7-128">Zobrazení podrobností o prognóze</span><span class="sxs-lookup"><span data-stu-id="7aef7-128">Viewing details of the forecast</span></span>
<span data-ttu-id="7aef7-129">Můžete otevřít stránku **Podrobnosti prognózy poptávky** a zobrazit další informace o prognóze.</span><span class="sxs-lookup"><span data-stu-id="7aef7-129">You can open the **Demand forecast details** page to view more information about the forecast.</span></span> 

<span data-ttu-id="7aef7-130">Stránka **Podrobnosti prognózy poptávky** popisuje následující informace v grafickém a tabulkovém formátu:</span><span class="sxs-lookup"><span data-stu-id="7aef7-130">The **Demand forecast details** page shows the following information in graphical and tabular formats:</span></span>

-   <span data-ttu-id="7aef7-131">Historická poptávka, na které je předpověď prognózy založena.</span><span class="sxs-lookup"><span data-stu-id="7aef7-131">The historical demand that the forecast predictions are based on.</span></span>
-   <span data-ttu-id="7aef7-132">Aktuální prognóza používaná pro hlavní plánování.</span><span class="sxs-lookup"><span data-stu-id="7aef7-132">The current forecast that is used by Master planning.</span></span>
-   <span data-ttu-id="7aef7-133">Hodnoty nové prognózy poptávky a částky, o které byly ručně upraveny.</span><span class="sxs-lookup"><span data-stu-id="7aef7-133">The new demand forecast values and the amounts they have been manually adjusted by.</span></span>
-   <span data-ttu-id="7aef7-134">Interval spolehlivosti pro předpokládané hodnoty.</span><span class="sxs-lookup"><span data-stu-id="7aef7-134">The confidence interval for the forecasted values.</span></span>
-   <span data-ttu-id="7aef7-135">Model prognózy, který byl použit ke generování předpovědi.</span><span class="sxs-lookup"><span data-stu-id="7aef7-135">The forecast model that was used to generate the forecast.</span></span> <span data-ttu-id="7aef7-136">Pokud zobrazíte souhrnné údaje, zobrazí se seznam všech metod, které byly použity pro všechny agregované časové úseky.</span><span class="sxs-lookup"><span data-stu-id="7aef7-136">If you're viewing aggregated data, you will see the list of all the methods that were used for all the aggregated time series.</span></span>
-   <span data-ttu-id="7aef7-137">Přesnost interního modelu (MAPE).</span><span class="sxs-lookup"><span data-stu-id="7aef7-137">The internal model accuracy (MAPE).</span></span> <span data-ttu-id="7aef7-138">Další informace o přesnosti prognózy naleznete v tématu [Sledování přesnosti prognózy](monitor-forecast-accuracy.md).</span><span class="sxs-lookup"><span data-stu-id="7aef7-138">For more information about forecast accuracy, see [Monitoring forecast accuracy](monitor-forecast-accuracy.md).</span></span>

<span data-ttu-id="7aef7-139">**Poznámky:**</span><span class="sxs-lookup"><span data-stu-id="7aef7-139">**Notes:**</span></span>

-   <span data-ttu-id="7aef7-140">Interval jistoty, který se zobrazí v části **Prognóza** na stránce, představuje rozdíl mezi horním limitem intervalu jistoty a dolním limitem intervalu jistoty.</span><span class="sxs-lookup"><span data-stu-id="7aef7-140">The confidence interval that appears in the **Forecast** section of the page represents the difference between the confidence interval upper limit and the confidence interval lower limit.</span></span> <span data-ttu-id="7aef7-141">Pokud chcete zobrazit hodnoty pro dolní a horní limit, umístěte ukazatel myši do grafu v části **Historická poptávka a prognóza – graficky**.</span><span class="sxs-lookup"><span data-stu-id="7aef7-141">To see the values for the upper and lower limits, hover over the chart in the **Historical demand and forecast graphically** section.</span></span>
-   <span data-ttu-id="7aef7-142">Pokud používáte službu pro prognózu poptávky strojového učení Microsoft Azure v aplikaci Finance and Operations, můžete určit podíl úrovně jistoty, který by měla mít generovaná prognóza.</span><span class="sxs-lookup"><span data-stu-id="7aef7-142">If you use the Finance and Operations Demand forecasting Microsoft Azure Machine Learning service, you can specify the confidence level percentage that the forecast that is generated should have.</span></span> <span data-ttu-id="7aef7-143">Interval jistoty obsahuje určitý úsek hodnot, které fungují jako vhodné odhady pro prognózu poptávky.</span><span class="sxs-lookup"><span data-stu-id="7aef7-143">A confidence interval consists of a range of values that act as good estimates for the demand forecast.</span></span> <span data-ttu-id="7aef7-144">95% úroveň jistoty například označuje existenci 5% riziko, že prognóza poptávky se bude nacházet mimo rozsah intervalu jistoty.</span><span class="sxs-lookup"><span data-stu-id="7aef7-144">A 95-percent confidence level percentage indicates that there is a 5-percent risk that the demand forecast falls outside the confidence interval range.</span></span>

<span data-ttu-id="7aef7-145">Musíte také provést ruční úpravy prognózy na stránce **Podrobnosti prognózy poptávky** tím, že změníte hodnoty na řádku **Prognóza** v části **Prognóza**.</span><span class="sxs-lookup"><span data-stu-id="7aef7-145">You can also make manual adjustments to the forecast on the **Demand forecast details** page, by modifying the values in the **Forecast** row in the **Forecast** section.</span></span>

<a name="additional-resources"></a><span data-ttu-id="7aef7-146">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="7aef7-146">Additional resources</span></span>
--------

[<span data-ttu-id="7aef7-147">Měření přesnosti prognózy</span><span class="sxs-lookup"><span data-stu-id="7aef7-147">Monitoring forecast accuracy</span></span>](monitor-forecast-accuracy.md)

[<span data-ttu-id="7aef7-148">Generování statistické základní prognózy</span><span class="sxs-lookup"><span data-stu-id="7aef7-148">Generating a statistical baseline forecast</span></span>](generate-statistical-baseline-forecast.md)



