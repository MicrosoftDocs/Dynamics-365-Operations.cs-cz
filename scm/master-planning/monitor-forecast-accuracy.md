---
title: "Přesnosti prognózy monitor"
description: "Tento článek popisuje typy přesnost prognózy, že 365 Microsoft Dynamics pro operace počítá a vysvětluje, jak lze zobrazit hodnoty přesnosti."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 72863
ms.assetid: 810a0d63-f4c6-4167-b2b3-a178b74ead89
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: d3f88a4fa54217cea909c54955de05e2175db0cd
ms.lasthandoff: 03/29/2017


---

# <a name="monitor-forecast-accuracy"></a>Přesnosti prognózy monitor

[!include[banner](../includes/banner.md)]


Tento článek popisuje typy přesnost prognózy, že 365 Microsoft Dynamics pro operace počítá a vysvětluje, jak lze zobrazit hodnoty přesnosti.

Dynamics 365 pro operace vypočítá přesnost prognózy na následující druhy:

-   Historická přesnost prognózy porovnáním historické prognózy, kterou hlavní plánování používá s historickou poptávkou. K zobrazení hodnot (absolutní hodnoty a hodnoty v procentech) pro historickou přesnost prognózy klepněte na tlačítko **Zobrazit přesnost** na stránce **Podrobnosti prognózy poptávky**.
-   Odhadovaná přesnost modelu prognózy, který slouží ke generování předpovědi. Procento přesnosti lze zobrazit v části **Podrobnosti modelu – MAPE** na stránce **Podrobnosti prognózy poptávky**. 

**Poznámka:** používáte-li Dynamics 365 operace poptávky prognózy služby Microsoft Azure Machine Learning, výpočet přesnosti interní model je založen na sada dat testu. Chcete-li určit velikost sada dat testu, nastavte **TEST\_nastavit\_velikost\_PROCENT** parametr **parametry prognózy poptávky** stránky. Pokud je nastavena hodnota na **20**, posledních 20 procent historických dat se použije k výpočtu přesnosti interního modelu.


<a name="see-also"></a>Viz také
--------

[Authorizing the adjusted forecast](authorize-adjusted-forecast.md)

[Remove outliers from historical transaction data when calculating a demand forecast](remove-historical-outliers-calculating-demand-forecast.md)




