---
title: "Autorizovat upravenou prognózu"
description: "Ne všechna data prognózy musí být ověřeny okamžitě. Tento článek vysvětluje, jak můžete určit období, pro které je prognóza autorizována. Také vysvětluje, jak lze autorizovat předpovědi pro určité společnosti a modely prognóz."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqDemPlanImportForecastDialog
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 72734
ms.assetid: cb8fd809-605a-4a8b-a390-636edfec21f9
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 399a7a21ec71fe50e280ccb24699cda76d571990
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---

# <a name="authorize-an-adjusted-forecast"></a>Autorizovat upravenou prognózu

[!include[banner](../includes/banner.md)]


Ne všechna data prognózy musí být ověřeny okamžitě. Tento článek vysvětluje, jak můžete určit období, pro které je prognóza autorizována. Také vysvětluje, jak lze autorizovat předpovědi pro určité společnosti a modely prognóz.

Ne všechna data prognózy musí být ověřeny okamžitě. Můžete zadat počáteční a koncové datum v období, pro které je prognóza schválena. Tato funkce umožňuje zmrazit určité období. 

Počáteční a koncová data, které zadáte, musí odpovídat počátečním a koncovým datům intervalu, ve kterém je prognóza generována. Systém vynucuje tato omezení a automaticky upraví data, pokud jsou úpravy nutné. 

Na kartě **Podrobnosti** na stránce **Autorizace** můžete zobrazit podrobnosti o naposledy vygenerované prognóze. 

Můžete vybrat společnosti a modely prognóz a povolit tak použití předpovědi. Ve výchozím nastavení obsahuje mřížka všechny společnosti, pro které poptávka prognózy byla vytvořena. Pro každou společnost je předem nastaven model prognózy, který odpovídá aktuálnímu plánu prognózy, který je nastaven v parametrech hlavního plánování. Tento model prognózy lze však změnit na libovolný model prognózy, který patří k dané společnosti. Pokud žádná data prognózy poptávky nebyla vygenerována ve vybrané společnosti, obdržíte během importu zprávu s upozorněním. 

Ujistěte se, že rozumíte způsobu, jakým pole **Uložit ruční úpravy provedené v základní prognóze poptávky** funguje. Pokud jste provedli ruční úpravy pro statistickou základní prognózu, upravené hodnoty jsou registrovány pro použití i v případě, že je zaškrtnutí tohoto políčka zrušeno. Po povolení však budou změny zrušeny. Při příštím vygenerování prognózy bude tato prognóza tedy pouze statistická a nenabízí žádné ruční přepsání, i když je vybrána možnost **Přeneste ruční úpravy do prognózy poptávky**. Proto můžete použít pole **Uložit ruční úpravy provedené v základní prognóze poptávky** jako mechanismus, který vám umožní zachovat nebo zrušit všechny ruční změny.

<a name="see-also"></a>Viz také
--------

[Ruční úpravy základní prognózy](manual-adjustments-baseline-forecast.md)

[Měření přesnosti prognózy](monitor-forecast-accuracy.md)




