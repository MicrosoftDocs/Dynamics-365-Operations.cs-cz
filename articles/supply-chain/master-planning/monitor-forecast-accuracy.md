---
title: Monitorování přesnosti prognózy
description: Toto téma popisuje typy přesnosti prognózy, které aplikace Dynamics 365 Supply Chain Management vypočítává, a popisuje způsob, jakým lze hodnoty přesnosti zobrazit.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanForecastDetails
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 72863
ms.assetid: 810a0d63-f4c6-4167-b2b3-a178b74ead89
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6f238afadfa064e972ef11a95fdad073f63ff20c
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250661"
---
# <a name="monitor-forecast-accuracy"></a>Monitorování přesnosti prognózy

[!include [banner](../includes/banner.md)]

Toto téma popisuje typy přesnosti prognózy, které aplikace Microsoft Dynamics 365 Supply Chain Management vypočítává, a popisuje způsob, jakým lze hodnoty přesnosti zobrazit.

Aplikace Supply Chain Management provádí výpočet následujících typů přesnosti prognózy:

-   Historická přesnost prognózy porovnáním historické prognózy, kterou hlavní plánování používá s historickou poptávkou. K zobrazení hodnot (absolutní hodnoty a hodnoty v procentech) pro historickou přesnost prognózy klepněte na tlačítko **Zobrazit přesnost** na stránce **Podrobnosti prognózy poptávky**.
-   Odhadovaná přesnost modelu prognózy, který slouží ke generování předpovědi. Procento přesnosti lze zobrazit v části **Podrobnosti modelu – MAPE** na stránce **Podrobnosti prognózy poptávky**. 

> [!NOTE]
> Pokud používáte službu strojového učení Microsoft Azure prognózy poptávky, přesnost výpočtu interního modelu vychází ze sady testovaných dat. Pokud chcete určit velikost sady testovaných dat, nastavte parametr **TEST\_SET\_SIZE\_PERCENT** na stránce **Parametry tvorby prognóz poptávky**. Pokud je nastavena hodnota na **20**, posledních 20 procent historických dat se použije k výpočtu přesnosti interního modelu.


<a name="additional-resources"></a>Další zdroje
--------

[Autorizování upravené prognózy](authorize-adjusted-forecast.md)

[Odebrání odlehlých hodnot z historických dat transakcí při výpočtu prognózy poptávky](remove-historical-outliers-calculating-demand-forecast.md)



