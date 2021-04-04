---
title: Monitorování přesnosti prognózy
description: Toto téma popisuje typy přesnosti prognózy, které aplikace Dynamics 365 Supply Chain Management vypočítává, a popisuje způsob, jakým lze hodnoty přesnosti zobrazit.
author: roxanadiaconu
manager: tfehr
ms.date: 01/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanForecastDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: 72863
ms.assetid: 810a0d63-f4c6-4167-b2b3-a178b74ead89
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8548fa9f64a579816e51bbd7ad9f63db290eaa38
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5244200"
---
# <a name="monitor-forecast-accuracy"></a><span data-ttu-id="378e8-103">Monitorování přesnosti prognózy</span><span class="sxs-lookup"><span data-stu-id="378e8-103">Monitor forecast accuracy</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="378e8-104">Toto téma popisuje typy přesnosti prognózy, které aplikace Microsoft Dynamics 365 Supply Chain Management vypočítává, a popisuje způsob, jakým lze hodnoty přesnosti zobrazit.</span><span class="sxs-lookup"><span data-stu-id="378e8-104">This topic describes the types of forecast accuracy that Microsoft Dynamics 365 Supply Chain Management calculates, and explains how you can view the accuracy values.</span></span>

<span data-ttu-id="378e8-105">Aplikace Supply Chain Management provádí výpočet následujících typů přesnosti prognózy:</span><span class="sxs-lookup"><span data-stu-id="378e8-105">Supply Chain Management calculates the following types of forecast accuracy:</span></span>

-   <span data-ttu-id="378e8-106">Historická přesnost prognózy porovnáním historické prognózy, kterou hlavní plánování používá s historickou poptávkou.</span><span class="sxs-lookup"><span data-stu-id="378e8-106">Historical forecast accuracy, by comparing the historical forecast that Master Planning uses with the historical demand.</span></span> <span data-ttu-id="378e8-107">K zobrazení hodnot (absolutní hodnoty a hodnoty v procentech) pro historickou přesnost prognózy klepněte na tlačítko **Zobrazit přesnost** na stránce **Podrobnosti prognózy poptávky**.</span><span class="sxs-lookup"><span data-stu-id="378e8-107">To view the values (both absolute values and percentage values) for historical forecast accuracy, click **Show accuracy** on the **Demand forecast details** page.</span></span>
-   <span data-ttu-id="378e8-108">Odhadovaná přesnost modelu prognózy, který slouží ke generování předpovědi.</span><span class="sxs-lookup"><span data-stu-id="378e8-108">The estimated accuracy of the forecasting model that is used to generate the predictions.</span></span> <span data-ttu-id="378e8-109">Procento přesnosti lze zobrazit v části **Podrobnosti modelu – MAPE** na stránce **Podrobnosti prognózy poptávky**.</span><span class="sxs-lookup"><span data-stu-id="378e8-109">You can view the accuracy percentage under **Model details - MAPE** on the **Demand forecast details** page.</span></span> 

> [!NOTE]
> <span data-ttu-id="378e8-110">Pokud používáte strojové učení Microsoft Azure prognózy poptávky, přesnost výpočtu interního modelu vychází ze sady testovaných dat.</span><span class="sxs-lookup"><span data-stu-id="378e8-110">If you use the Demand forecasting Microsoft Azure Machine Learning, the calculation of internal model accuracy is based on the test data set.</span></span> <span data-ttu-id="378e8-111">Pokud chcete určit velikost sady testovaných dat, nastavte parametr **TEST\_SET\_SIZE\_PERCENT** na stránce **Parametry tvorby prognóz poptávky**.</span><span class="sxs-lookup"><span data-stu-id="378e8-111">To specify the size of the test data set, set the **TEST\_SET\_SIZE\_PERCENT** parameter on the **Demand forecasting parameters** page.</span></span> <span data-ttu-id="378e8-112">Pokud je nastavena hodnota na **20**, posledních 20 procent historických dat se použije k výpočtu přesnosti interního modelu.</span><span class="sxs-lookup"><span data-stu-id="378e8-112">For example, if you set the value to **20**, the last 20 percent of the historical data will be used to calculate the internal model accuracy.</span></span>


<a name="additional-resources"></a><span data-ttu-id="378e8-113">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="378e8-113">Additional resources</span></span>
--------

[<span data-ttu-id="378e8-114">Autorizace upravené prognózy</span><span class="sxs-lookup"><span data-stu-id="378e8-114">Authorize an adjusted forecast</span></span>](authorize-adjusted-forecast.md)

[<span data-ttu-id="378e8-115">Odebrání odlehlých hodnot z historických dat transakcí při výpočtu prognózy poptávky</span><span class="sxs-lookup"><span data-stu-id="378e8-115">Remove outliers from historical transaction data when calculating a demand forecast</span></span>](remove-historical-outliers-calculating-demand-forecast.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]