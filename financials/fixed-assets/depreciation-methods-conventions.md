---
title: "Odpisové metody a způsoby odpisu"
description: "Tento článek poskytuje přehled odpisových zásad a metod, které jsou podporovány v aplikaci Microsoft Dynamics AX."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: AssetDepreciationProfile, AssetGroupBookSetup, AssetGroupDepBookSetup
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 3441
ms.assetid: 1d8267b1-86a8-44bf-8814-f56b5d45a0ae
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 8e89a57dda8f2d392483ed13c686ea97b74926b0
ms.openlocfilehash: 51c053e6c130d20258e02284d097431a18bb38cb
ms.lasthandoff: 03/31/2017


---

# <a name="depreciation-methods-and-conventions"></a>Odpisové metody a způsoby odpisu

[!include[banner](../includes/banner.md)]


Tento článek poskytuje přehled odpisových zásad a metod, které jsou podporovány v aplikaci Microsoft Dynamics AX.

K dispozici máte několik metod a způsobů odpisu. Metody slouží k přidělení odpisové hodnoty dlouhodobého majetku jednotlivým fiskálním obdobím. Odpisová hodnota dlouhodobého majetku je pořizovací cena snížená o likvidační hodnotu. 

Používáte-li určitý způsob odpisu a změníte poslední datum zahájení odpisu určitého majetku, které přeskočí některé odpisy, bude odpis za poslední rok pravděpodobně vyšší nebo nižší, než bylo očekáváno. Odpis je nastaven podle počtu období ovlivněných změnou posledního data zahájení odpisu.

Pokud například používáte půlroční způsob odpisu déle než tři roky, trvá odpis běžně přes 3 a půl roku. Změníte-li během tohoto období poslední datum spuštění odpisu, nebude v posledním roce odpisu zahrnut počet ovlivněných období. Posunete-li toto datum o tři měsíce, bude pro odpis v posledním roce důležitých devět měsíců, přičemž za normálních okolností by to bylo šest.

K dispozici máte následující způsoby odpisu.


-   Pololetí
-   Celý měsíc
-   Polovina čtvrtletí
-   Polovina měsíce (1. den v měsíci)
-   Polovina měsíce (15. den v měsíci)
-   Pololetí (počátek roku)
-   Pololetí (příští rok)

Můžete vybírat z následujících metod odpisování:
-   Lineární
-   Zrychleně
-   Ručně
-   Koeficient
-   Spotřeba
-   Lineární s vyrovnáním na konci životnosti
-   Degresivní 200 %
-   Degresivní 175 %
-   Degresivní 150 %
-   Degresivní 125 %

 



<a name="see-also"></a>Viz také
--------

[Fixed asset depreciation](fixed-asset-depreciation.md)

[Straight line service life depreciation](Straight-line-service-life-depreciation.md)

[Reducing balance depreciation](reduce-balance-depreciation.md)

[Manual depreciation](manual-depreciation.md)

[Factor depreciation](factor-depreciation.md)

[Consumption depreciation](consumption-depreciation.md)

[Straight line life remaining depreciation](straight-line-life-remaining-depreciation.md)

[125 % degresivní odpisování](125-percent-reducing-balance-depreciation.md)

[150 % degresivního odpisování](150-percent-reducing-balance-depreciation.md)

[175 % degresivní odpisování](175-percent-reducing-balance-depreciation.md)

[200 % degresivní odpisování](200-percent-reducing-balance-depreciation.md)



