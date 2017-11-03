---
title: "Sledování přesnosti prognózy"
description: "Tento článek popisuje typy přesnosti prognózy, které aplikace Microsoft Dynamics 365 for Finance and Operations vypočítává, a popisuje způsob, jakým lze hodnoty přesnosti zobrazit."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 72863
ms.assetid: 810a0d63-f4c6-4167-b2b3-a178b74ead89
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: bd84dde353972d2d259706dd9f8f3621cef04472
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="monitor-forecast-accuracy"></a><span data-ttu-id="5b8b5-103">Sledování přesnosti prognózy</span><span class="sxs-lookup"><span data-stu-id="5b8b5-103">Monitor forecast accuracy</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="5b8b5-104">Tento článek popisuje typy přesnosti prognózy, které aplikace Microsoft Dynamics 365 for Finance and Operations vypočítává, a popisuje způsob, jakým lze hodnoty přesnosti zobrazit.</span><span class="sxs-lookup"><span data-stu-id="5b8b5-104">This article describes the types of forecast accuracy that Microsoft Dynamics 365 for Finance and Operations calculates, and explains how you can view the accuracy values.</span></span>

<span data-ttu-id="5b8b5-105">Aplikace Finance and Operations provádí výpočet následujících typů přesnosti prognózy:</span><span class="sxs-lookup"><span data-stu-id="5b8b5-105">Finance and Operations calculates the following types of forecast accuracy:</span></span>

-   <span data-ttu-id="5b8b5-106">Historická přesnost prognózy porovnáním historické prognózy, kterou hlavní plánování používá s historickou poptávkou.</span><span class="sxs-lookup"><span data-stu-id="5b8b5-106">Historical forecast accuracy, by comparing the historical forecast that Master Planning uses with the historical demand.</span></span> <span data-ttu-id="5b8b5-107">K zobrazení hodnot (absolutní hodnoty a hodnoty v procentech) pro historickou přesnost prognózy klepněte na tlačítko **Zobrazit přesnost** na stránce **Podrobnosti prognózy poptávky**.</span><span class="sxs-lookup"><span data-stu-id="5b8b5-107">To view the values (both absolute values and percentage values) for historical forecast accuracy, click **Show accuracy** on the **Demand forecast details** page.</span></span>
-   <span data-ttu-id="5b8b5-108">Odhadovaná přesnost modelu prognózy, který slouží ke generování předpovědi.</span><span class="sxs-lookup"><span data-stu-id="5b8b5-108">The estimated accuracy of the forecasting model that is used to generate the predictions.</span></span> <span data-ttu-id="5b8b5-109">Procento přesnosti lze zobrazit v části **Podrobnosti modelu – MAPE** na stránce **Podrobnosti prognózy poptávky**.</span><span class="sxs-lookup"><span data-stu-id="5b8b5-109">You can view the accuracy percentage under **Model details - MAPE** on the **Demand forecast details** page.</span></span> 

<span data-ttu-id="5b8b5-110">**Poznámka:** Pokud používáte službu Demand forecasting Microsoft Azure Machine Learning aplikace Finance and Operations, přesnost výpočtu interního modelu vychází ze sady testovaných dat.</span><span class="sxs-lookup"><span data-stu-id="5b8b5-110">**Note:** If you use the Finance and Operations Demand forecasting Microsoft Azure Machine Learning service, the calculation of internal model accuracy is based on the test data set.</span></span> <span data-ttu-id="5b8b5-111">Pokud chcete určit velikost sady testovaných dat, nastavte parametr **TEST\_SET\_SIZE\_PERCENT** na stránce **Parametry tvorby prognóz poptávky**.</span><span class="sxs-lookup"><span data-stu-id="5b8b5-111">To specify the size of the test data set, set the **TEST\_SET\_SIZE\_PERCENT** parameter on the **Demand forecasting parameters** page.</span></span> <span data-ttu-id="5b8b5-112">Pokud je nastavena hodnota na **20**, posledních 20 procent historických dat se použije k výpočtu přesnosti interního modelu.</span><span class="sxs-lookup"><span data-stu-id="5b8b5-112">For example, if you set the value to **20**, the last 20 percent of the historical data will be used to calculate the internal model accuracy.</span></span>


<a name="see-also"></a><span data-ttu-id="5b8b5-113">Viz také</span><span class="sxs-lookup"><span data-stu-id="5b8b5-113">See also</span></span>
--------

[<span data-ttu-id="5b8b5-114">Autorizování upravené prognózy</span><span class="sxs-lookup"><span data-stu-id="5b8b5-114">Authorizing the adjusted forecast</span></span>](authorize-adjusted-forecast.md)

[<span data-ttu-id="5b8b5-115">Odebrání odlehlých hodnot z historických dat transakcí při výpočtu prognózy poptávky</span><span class="sxs-lookup"><span data-stu-id="5b8b5-115">Remove outliers from historical transaction data when calculating a demand forecast</span></span>](remove-historical-outliers-calculating-demand-forecast.md)




