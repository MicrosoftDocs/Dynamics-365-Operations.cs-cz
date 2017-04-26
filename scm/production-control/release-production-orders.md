---
title: "Vydání výrobních zakázek"
description: "Uvolněná výrobní zakázka je objednávka, která byla schválena k výrobě. Výraz Uvolněná popisuje stav v životním cyklu výrobní zakázky, kde je výrobní zakázka k dispozici ke spuštění v rámci dílenské výroby a skladových procesů."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ProdParmRelease
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 2414
ms.assetid: 50c2257b-2924-44f5-b7c1-11f498092053
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: c4ebedab6d7de62479d3bc80583afadbe780aac4
ms.lasthandoff: 03/31/2017


---

# <a name="release-production-orders"></a>Vydání výrobních zakázek

[!include[banner](../includes/banner.md)]


Uvolněná výrobní zakázka je objednávka, která byla schválena k výrobě. Výraz Uvolněná popisuje stav v životním cyklu výrobní zakázky, kde je výrobní zakázka k dispozici ke spuštění v rámci dílenské výroby a skladových procesů. 

<a name="characteristics-of-the-released-state"></a>Charakteristika stavu Uvolněno
-------------------------------------

Stav **Uvolněno** je jeden ze stavů životního cyklu výrobní zakázky. Výrobní zakázky, které jsou ve stavu **Uvolněno**, jsou k dispozici pro spuštění v dílenské výrobě a pro procesy skladu. Stav **Uvolněno** má následující charakteristiky:

-   Výrobní zakázku lze změnit na stav **Uvolněno** ve výrobní zakázce nebo pomocí dávkového zpracování. Výrobní zakázky lze rovněž automaticky aktualizovat s použitím potvrzení plánovaných výrobních zakázek pomocí pole **Ochranná doba potvrzení** na stránce **Hlavní plán**.
-   Stav **Uvolněno** je signál pro dílenskou obsluhu (operátory) pro spouštění výrobních úloh v dílně.
-   Výrobní doklady, jako například karty technického postupu, postupy úlohy a pracovní karty poskytují informace o výrobních úlohách, a lze je vydat.
-   Pro materiály, které jsou fyzicky rezervovány, se vytvoří skladová práce pro výdej materiálu pro výrobní zakázku.

## <a name="releasing-jobs-to-the-shop-floor"></a>Uvolnění úloh do výroby
Po uvolnění výrobní zakázky jsou výrobní úlohy, které se vztahují k objednávce, viditelné a připravené pro registraci. Operátory můžete provádět registrace úlohy, například Start, Stop a dokončení, buď **úlohu karty terminál** stránky nebo **úlohu karty zařízení** stránky. Zaznamenat čas a množství automaticky převedeny z registračních stránek deníky výroby ke sledování spotřebovaný čas a množství.

## <a name="route-cards"></a>Karty technologického postupu
Karta technologického postupu poskytuje souhrn informací pocházejících z nastavení operací a technologických postupů a z metod plánování úloh.

## <a name="route-jobs"></a>Operace tech. postupu
Operace technologického postupu obsahuje podrobný seznam všech úloh určité operace a zahrnuje časové údaje pro dobu nastavení, zpracování, čekání a přepravy. Operace lakování bude například vyžadovat údaje pro jednotlivé úlohy, jako je doba nastavení, doba zpracování (pro proces lakování) a doba čekání (pro zasychání).

## <a name="job-cards"></a>Úkolové lístky
Na úkolových lístcích jsou uvedena čísla jednotlivých úloh pro určitou operaci. (Vždy jedna úloha na stránku.) Úlohy uvedené na úkolovém lístku a jejich odhadované doby pocházejí z konfiguračních údajů na kartách technologického postupu a z údajů pro operace technologického postupu. Z úkolového lístku můžete otevřít stránku **Řádky výr. deníku**, **úkolový lístek**. Zpětnou vazbu ohledně výrobního procesu mohou poskytnout osoby používající provozní prostředky. K dispozici jsou pole, do nichž můžete zadat statistické údaje o spotřebě a informace, jako jsou například chyby v množství.

## <a name="warehouse-work-for-raw-material-picking"></a>Skladová práce pro výdej surovin
Práce pro výdej surovin je vytvořena v průběhu uvolnění. Práce je generován pouze pro množství materiálů, která byla fyzicky rezervována pro výrobní zakázky před vydáním objednávky. Následující nastavení je vyžadováno ke generování práce skladu pro výdej suroviny:

-   Směrnice skladového místa pro výdej surovin, které určují, ve kterém umístění skladu chcete vydat materiál
-   Šablona vlny pro suroviny, kde jsou konfigurovány zásady provedení skladové práce
-   Vstupní místo výroby, která určuje, kam jsou materiály umístěny





