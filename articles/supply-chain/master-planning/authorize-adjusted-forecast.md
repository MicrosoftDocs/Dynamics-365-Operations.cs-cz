---
title: Autorizovat upravenou prognózu
description: Ne všechna data prognózy musí být ověřeny okamžitě. Tento článek vysvětluje, jak můžete určit období, pro které je prognóza autorizována. Také vysvětluje, jak lze autorizovat předpovědi pro určité společnosti a modely prognóz.
author: roxanadiaconu
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanImportForecastDialog
audience: Application User
ms.reviewer: kamaybac
ms.custom: 72734
ms.assetid: cb8fd809-605a-4a8b-a390-636edfec21f9
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 834ec090bc2bc8486bcb64b756c101a1142a0766
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5264785"
---
# <a name="authorize-an-adjusted-forecast"></a>Autorizovat upravenou prognózu

[!include [banner](../includes/banner.md)]

Ne všechna data prognózy musí být ověřeny okamžitě. Tento článek vysvětluje, jak můžete určit období, pro které je prognóza autorizována. Také vysvětluje, jak lze autorizovat předpovědi pro určité společnosti a modely prognóz.

Ne všechna data prognózy musí být ověřeny okamžitě. Můžete zadat počáteční a koncové datum v období, pro které je prognóza schválena. Tato funkce umožňuje zmrazit určité období. 

Počáteční a koncová data, které zadáte, musí odpovídat počátečním a koncovým datům intervalu, ve kterém je prognóza generována. Systém vynucuje tato omezení a automaticky upraví data, pokud jsou úpravy nutné. 

Na kartě **Podrobnosti** na stránce **Autorizace** můžete zobrazit podrobnosti o naposledy vygenerované prognóze. 

Můžete vybrat společnosti a modely prognóz a povolit tak použití předpovědi. Ve výchozím nastavení obsahuje mřížka všechny společnosti, pro které poptávka prognózy byla vytvořena. Pro každou společnost je předem nastaven model prognózy, který odpovídá aktuálnímu plánu prognózy, který je nastaven v parametrech hlavního plánování. Tento model prognózy lze však změnit na libovolný model prognózy, který patří k dané společnosti. Pokud žádná data prognózy poptávky nebyla vygenerována ve vybrané společnosti, obdržíte během importu zprávu s upozorněním. 

Ujistěte se, že rozumíte způsobu, jakým pole **Uložit ruční úpravy provedené v základní prognóze poptávky** funguje. Pokud jste provedli ruční úpravy pro statistickou základní prognózu, upravené hodnoty jsou registrovány pro použití i v případě, že je zaškrtnutí tohoto políčka zrušeno. Po povolení však budou změny zrušeny. Při příštím vygenerování prognózy bude tato prognóza tedy pouze statistická a nenabízí žádné ruční přepsání, i když je vybrána možnost **Přeneste ruční úpravy do prognózy poptávky**. Proto můžete použít pole **Uložit ruční úpravy provedené v základní prognóze poptávky** jako mechanismus, který vám umožní zachovat nebo zrušit všechny ruční změny.

<a name="additional-resources"></a>Další zdroje
--------

[Ruční úpravy základní prognózy](manual-adjustments-baseline-forecast.md)

[Monitorování přesnosti prognózy](monitor-forecast-accuracy.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]