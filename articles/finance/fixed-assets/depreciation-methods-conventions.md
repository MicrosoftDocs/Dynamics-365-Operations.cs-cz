---
title: Odpisové metody a způsoby odpisu
description: Tento článek poskytuje přehled odpisových zásad a metod, které jsou podporovány v aplikaci Microsoft Dynamics 365 Finance.
author: ShylaThompson
ms.date: 04/25/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetDepreciationProfile, AssetGroupBookSetup, AssetGroupDepBookSetup
audience: Application User
ms.reviewer: roschlom
ms.custom: 3441
ms.assetid: 1d8267b1-86a8-44bf-8814-f56b5d45a0ae
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 76b20c895519edb7316c2b9a6b223a109a307e77
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/04/2021
ms.locfileid: "6189390"
---
# <a name="depreciation-methods-and-conventions"></a>Odpisové metody a způsoby odpisu

[!include [banner](../includes/banner.md)]

Tento článek poskytuje přehled podporovaných odpisových zásad a metod.

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





## <a name="additional-resources"></a>Další zdroje

[Odpisy dlouhodobého majetku](fixed-asset-depreciation.md)

[Lineární odpisování](Straight-line-service-life-depreciation.md)

[Degresivní odpis](reduce-balance-depreciation.md)

[Ruční odpis](manual-depreciation.md)

[Odpis koeficientem](factor-depreciation.md)

[Odpis spotřeby](consumption-depreciation.md)

[Lineární odpis s vyrovnáním na konci životnosti](straight-line-life-remaining-depreciation.md)

[Degresivní odpis 125 procent](125-percent-reducing-balance-depreciation.md)

[Degresivní odpis 150 procent](150-percent-reducing-balance-depreciation.md)

[Degresivní odpis 175 procent](175-percent-reducing-balance-depreciation.md)

[Degresivní odpis 200 procent](200-percent-reducing-balance-depreciation.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]