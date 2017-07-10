---
title: "Sledování přesnosti prognózy"
description: "Tento článek popisuje typy přesnosti prognózy, které aplikace Microsoft Dynamics 365 for Finance and Operations vypočítává, a popisuje způsob, jakým lze hodnoty přesnosti zobrazit."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 72863
ms.assetid: 810a0d63-f4c6-4167-b2b3-a178b74ead89
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 56d3f0312e684ab076f9116ac6638bcd67b52e58
ms.contentlocale: cs-cz
ms.lasthandoff: 06/13/2017


---

# <a name="monitor-forecast-accuracy"></a>Sledování přesnosti prognózy

[!include[banner](../includes/banner.md)]


Tento článek popisuje typy přesnosti prognózy, které aplikace Microsoft Dynamics 365 for Finance and Operations vypočítává, a popisuje způsob, jakým lze hodnoty přesnosti zobrazit.

Aplikace Finance and Operations provádí výpočet následujících typů přesnosti prognózy:

-   Historická přesnost prognózy porovnáním historické prognózy, kterou hlavní plánování používá s historickou poptávkou. K zobrazení hodnot (absolutní hodnoty a hodnoty v procentech) pro historickou přesnost prognózy klepněte na tlačítko **Zobrazit přesnost** na stránce **Podrobnosti prognózy poptávky**.
-   Odhadovaná přesnost modelu prognózy, který slouží ke generování předpovědi. Procento přesnosti lze zobrazit v části **Podrobnosti modelu – MAPE** na stránce **Podrobnosti prognózy poptávky**. 

**Poznámka:** Pokud používáte službu Demand forecasting Microsoft Azure Machine Learning aplikace Finance and Operations, přesnost výpočtu interního modelu vychází ze sady testovaných dat. Pokud chcete určit velikost sady testovaných dat, nastavte parametr **TEST\_SET\_SIZE\_PERCENT** na stránce **Parametry tvorby prognóz poptávky**. Pokud je nastavena hodnota na **20**, posledních 20 procent historických dat se použije k výpočtu přesnosti interního modelu.


<a name="see-also"></a>Viz také
--------

[Autorizování upravené prognózy](authorize-adjusted-forecast.md)

[Odebrání odlehlých hodnot z historických dat transakcí při výpočtu prognózy poptávky](remove-historical-outliers-calculating-demand-forecast.md)




