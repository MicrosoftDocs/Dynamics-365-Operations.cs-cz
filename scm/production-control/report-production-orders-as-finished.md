---
title: "Vykázat výrobní zakázky jako dokončené"
description: "Vykázat jako dokončené je ve fázi výroby. V této fázi je vykázán hotový výrobek a je přesunut z výrobní zakázky do zásob."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ProdJournalTransJob, ProdJournalTransProd, ProdJournalTransRoute, ProdParmReportFinished, ProdRouteOprOverview
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 27061
ms.assetid: 1c2dfc54-a293-49f2-9b96-5a912ac5762c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: f6369a424d384a93d1497825b6877b929e76f8b9
ms.contentlocale: cs-cz
ms.lasthandoff: 04/25/2017


---

# <a name="report-production-orders-as-finished"></a>Vykázat výrobní zakázky jako dokončené

[!include[banner](../includes/banner.md)]


Vykázat jako dokončené je ve fázi výroby. V této fázi je vykázán hotový výrobek a je přesunut z výrobní zakázky do zásob.

Je-li výrobní zakázka vykázána jako dokončená, jsou ve skladu zásob aktualizována množství dokončeného zboží. Částečné množství původně plánovaného množství objednávky může být hlášeno jako dokončené. Je také možné nahlásit množství chyb se přidruženými důvody chyb při vykazování množství jako dokončeného. Když výrobní zakázka dosáhne stavu Ohlášeno jako dokončené, znamená to, že ve výrobní zakázce nebude uváděné žádné další množství.
Tyto následující vlastnosti jsou také přidruženy k procesu **Ohlásit jako dokončené**:
-   Je možné nastavit spotřebu surovin a času, který je úměrný hodnotě hlášeného množství (zpětné vyprázdnění)
-   Odloženou práci lze generovat pro položky, které jsou povoleny pro procesy skladu.
-   Plánované nebo standardní náklady dokončeného zboží lze nastavit k vykazovaní do účtů hlavní knihy.
-   Objednávku kvality lze vytvořit pro vykázané množství na základě nastavení přidružení kvality.

Množství je vykazováno do výstupní umístění. Poté se vytvoří práce skladu pro převedení množství z výstupního umístění do cílového umístění definovaného směrnicí umístění místa pro odloženou práci.

-   Objednávku kvality lze vytvořit se po ohlášení dokončení výrobní zakázky, pokud bylo nastaveno přidružení kvality.

## <a name="set-a-production-order-to-reporting-as-finished"></a>Nastavené výrobní zakázky na Hlášeno jako dokončené
K nastavení stavu výrobní zakázky na **Hlášeno jako dokončené** můžete použít standardní funkci aktualizace výrobní zakázky nebo deníky technických postupů a karet úloh, nebo pomocí deníku **Hlášeno jako dokončené**. Můžete také aktualizovat stav na **Hlášeno jako dokončené** prostřednictvím terminálu karty úloh a stránek zařízení karty úloh, když vykazujete poslední práce výrobní zakázky. V závěru můžete povolit možnost **Hlášeno jako dokončené** jako proces pro řešení zařízení ručně ovládaného skladu.  




