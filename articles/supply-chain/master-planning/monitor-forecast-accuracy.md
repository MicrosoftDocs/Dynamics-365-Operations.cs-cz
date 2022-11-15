---
title: Sledování přesnosti prognózy
description: Tento článek popisuje typy přesnosti prognózy, které aplikace Dynamics 365 Supply Chain Management vypočítává, a popisuje způsob, jakým lze hodnoty přesnosti zobrazit.
author: t-benebo
ms.date: 01/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqDemPlanForecastDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: 72863
ms.assetid: 810a0d63-f4c6-4167-b2b3-a178b74ead89
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 76248d87533fd233b255060aa278c76e13719700
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740732"
---
# <a name="monitor-forecast-accuracy"></a>Sledování přesnosti prognózy

[!include [banner](../includes/banner.md)]

Tento článek popisuje typy přesnosti prognózy, které aplikace Microsoft Dynamics 365 Supply Chain Management vypočítává, a popisuje způsob, jakým lze hodnoty přesnosti zobrazit.

Aplikace Supply Chain Management provádí výpočet následujících typů přesnosti prognózy:

-   Historická přesnost prognózy porovnáním historické prognózy, kterou hlavní plánování používá s historickou poptávkou. K zobrazení hodnot (absolutní hodnoty a hodnoty v procentech) pro historickou přesnost prognózy klepněte na tlačítko **Zobrazit přesnost** na stránce **Podrobnosti prognózy poptávky**.
-   Odhadovaná přesnost modelu prognózy, který slouží ke generování předpovědi. Procento přesnosti lze zobrazit v části **Podrobnosti modelu – MAPE** na stránce **Podrobnosti prognózy poptávky**. 

> [!NOTE]
> Pokud používáte strojové učení Microsoft Azure prognózy poptávky, přesnost výpočtu interního modelu vychází ze sady testovaných dat. Pokud chcete určit velikost sady testovaných dat, nastavte parametr **TEST\_SET\_SIZE\_PERCENT** na stránce **Parametry tvorby prognóz poptávky**. Pokud je nastavena hodnota na **20**, posledních 20 procent historických dat se použije k výpočtu přesnosti interního modelu.


## <a name="additional-resources"></a>Další zdroje

- [Autorizace upravené prognózy](authorize-adjusted-forecast.md)
- [Odebrání odlehlých hodnot z historických dat transakcí při výpočtu prognózy poptávky](remove-historical-outliers-calculating-demand-forecast.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]