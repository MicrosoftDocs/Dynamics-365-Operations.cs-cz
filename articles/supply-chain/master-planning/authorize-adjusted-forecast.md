---
title: Autorizovat upravenou prognózu
description: Ne všechna data prognózy musí být ověřeny okamžitě. Tento článek vysvětluje, jak můžete určit období, pro které je prognóza autorizována. Také vysvětluje, jak lze autorizovat předpovědi pro určité společnosti a modely prognóz.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanImportForecastDialog
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 72734
ms.assetid: cb8fd809-605a-4a8b-a390-636edfec21f9
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6c397329993bd3014b608cdc50d5002dcd5ed6a4
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "313467"
---
# <a name="authorize-an-adjusted-forecast"></a><span data-ttu-id="9b60a-105">Autorizovat upravenou prognózu</span><span class="sxs-lookup"><span data-stu-id="9b60a-105">Authorize an adjusted forecast</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9b60a-106">Ne všechna data prognózy musí být ověřeny okamžitě.</span><span class="sxs-lookup"><span data-stu-id="9b60a-106">Not all forecast data must be authorized immediately.</span></span> <span data-ttu-id="9b60a-107">Tento článek vysvětluje, jak můžete určit období, pro které je prognóza autorizována.</span><span class="sxs-lookup"><span data-stu-id="9b60a-107">This article explains how you can specify the period that a forecast is authorized for.</span></span> <span data-ttu-id="9b60a-108">Také vysvětluje, jak lze autorizovat předpovědi pro určité společnosti a modely prognóz.</span><span class="sxs-lookup"><span data-stu-id="9b60a-108">It also explains how you can authorize the forecast for specific companies and forecast models.</span></span>

<span data-ttu-id="9b60a-109">Ne všechna data prognózy musí být ověřeny okamžitě.</span><span class="sxs-lookup"><span data-stu-id="9b60a-109">Not all forecast data must be authorized immediately.</span></span> <span data-ttu-id="9b60a-110">Můžete zadat počáteční a koncové datum v období, pro které je prognóza schválena.</span><span class="sxs-lookup"><span data-stu-id="9b60a-110">You can specify the start and end dates of the period that the forecast is authorized for.</span></span> <span data-ttu-id="9b60a-111">Tato funkce umožňuje zmrazit určité období.</span><span class="sxs-lookup"><span data-stu-id="9b60a-111">This functionality lets you freeze specific buckets.</span></span> 

<span data-ttu-id="9b60a-112">Počáteční a koncová data, které zadáte, musí odpovídat počátečním a koncovým datům intervalu, ve kterém je prognóza generována.</span><span class="sxs-lookup"><span data-stu-id="9b60a-112">The start and end dates that you specify must correspond to the start and end dates of the bucket that the forecast is generated in.</span></span> <span data-ttu-id="9b60a-113">Systém vynucuje tato omezení a automaticky upraví data, pokud jsou úpravy nutné.</span><span class="sxs-lookup"><span data-stu-id="9b60a-113">The system enforces this restriction and automatically adjusts the dates, if adjustment is required.</span></span> 

<span data-ttu-id="9b60a-114">Na kartě **Podrobnosti** na stránce **Autorizace** můžete zobrazit podrobnosti o naposledy vygenerované prognóze.</span><span class="sxs-lookup"><span data-stu-id="9b60a-114">On the **Details** tab of the **Authorization** page, you can view details about the forecast that was most recently generated.</span></span> 

<span data-ttu-id="9b60a-115">Můžete vybrat společnosti a modely prognóz a povolit tak použití předpovědi.</span><span class="sxs-lookup"><span data-stu-id="9b60a-115">You can select the companies and the forecast models to authorize the forecast for use.</span></span> <span data-ttu-id="9b60a-116">Ve výchozím nastavení obsahuje mřížka všechny společnosti, pro které poptávka prognózy byla vytvořena.</span><span class="sxs-lookup"><span data-stu-id="9b60a-116">By default, the grid includes all the companies that forecast demand has been created for.</span></span> <span data-ttu-id="9b60a-117">Pro každou společnost je předem nastaven model prognózy, který odpovídá aktuálnímu plánu prognózy, který je nastaven v parametrech hlavního plánování.</span><span class="sxs-lookup"><span data-stu-id="9b60a-117">For each company, the forecast model that corresponds to the current forecast plan that is set up in the master planning parameters is prefilled.</span></span> <span data-ttu-id="9b60a-118">Tento model prognózy lze však změnit na libovolný model prognózy, který patří k dané společnosti.</span><span class="sxs-lookup"><span data-stu-id="9b60a-118">However, you can change this forecast model to any forecast model that belongs to that company.</span></span> <span data-ttu-id="9b60a-119">Pokud žádná data prognózy poptávky nebyla vygenerována ve vybrané společnosti, obdržíte během importu zprávu s upozorněním.</span><span class="sxs-lookup"><span data-stu-id="9b60a-119">If no forecast demand data has been generated for a selected company, you receive a warning message at import time.</span></span> 

<span data-ttu-id="9b60a-120">Ujistěte se, že rozumíte způsobu, jakým pole **Uložit ruční úpravy provedené v základní prognóze poptávky** funguje.</span><span class="sxs-lookup"><span data-stu-id="9b60a-120">It's very important that you understand how the **Save the manual adjustments made to the baseline demand forecast** check box works.</span></span> <span data-ttu-id="9b60a-121">Pokud jste provedli ruční úpravy pro statistickou základní prognózu, upravené hodnoty jsou registrovány pro použití i v případě, že je zaškrtnutí tohoto políčka zrušeno.</span><span class="sxs-lookup"><span data-stu-id="9b60a-121">If you've made manual adjustments to the statistical baseline forecast, the adjusted values are authorized for use, even if this check box is cleared.</span></span> <span data-ttu-id="9b60a-122">Po povolení však budou změny zrušeny.</span><span class="sxs-lookup"><span data-stu-id="9b60a-122">However, the changes are discarded after the authorization.</span></span> <span data-ttu-id="9b60a-123">Při příštím vygenerování prognózy bude tato prognóza tedy pouze statistická a nenabízí žádné ruční přepsání, i když je vybrána možnost **Přeneste ruční úpravy do prognózy poptávky**.</span><span class="sxs-lookup"><span data-stu-id="9b60a-123">Therefore, the next time that a forecast is generated, that forecast is only a statistical forecast and doesn't have any manual overrides, even if **Transfer manual adjustments to the demand forecast** is selected.</span></span> <span data-ttu-id="9b60a-124">Proto můžete použít pole **Uložit ruční úpravy provedené v základní prognóze poptávky** jako mechanismus, který vám umožní zachovat nebo zrušit všechny ruční změny.</span><span class="sxs-lookup"><span data-stu-id="9b60a-124">Therefore, you can consider the **Save the manual adjustments made to the baseline demand forecast** check box a mechanism that lets you keep or discard all manual changes.</span></span>

<a name="additional-resources"></a><span data-ttu-id="9b60a-125">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="9b60a-125">Additional resources</span></span>
--------

[<span data-ttu-id="9b60a-126">Ruční úpravy základní prognózy</span><span class="sxs-lookup"><span data-stu-id="9b60a-126">Making manual adjustments to the baseline forecast</span></span>](manual-adjustments-baseline-forecast.md)

[<span data-ttu-id="9b60a-127">Měření přesnosti prognózy</span><span class="sxs-lookup"><span data-stu-id="9b60a-127">Monitoring forecast accuracy</span></span>](monitor-forecast-accuracy.md)



