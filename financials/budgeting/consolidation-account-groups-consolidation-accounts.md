---
title: "Skupiny konsolidačních účtů a další konsolidační účty"
description: "Toto téma obsahuje informace o skupinách konsolidačních účtů a další konsolidačních účtech a vysvětluje způsob jejich použití v aplikaci Microsoft Dynamics 365 for Finance and Operations, Enterprise edition."
author: RobinARH
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 265544
ms.assetid: 71c31df7-b655-46a8-8844-4f92a8bd71b0
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30T00:00:00.000Z
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 835669de01deb1ba0dcc5752d9d6d8f498e6ff7d
ms.contentlocale: cs-cz
ms.lasthandoff: 06/13/2017

---

# <a name="consolidation-account-groups-and-additional-consolidation-accounts"></a>Skupiny konsolidačních účtů a další konsolidační účty

[!include[banner](../includes/banner.md)]


Toto téma obsahuje informace o skupinách konsolidačních účtů a další konsolidačních účtech a vysvětluje způsob jejich použití v aplikaci Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.

<a name="consolidation-account-groups"></a>Skupiny konsolidačních účtů
----------------------------

Skupiny konsolidačních účtů umožňují vytvářet skupiny účtů, které chcete použít pro konsolidaci dat. Nejčastěji představuje skupina konsolidačních účtů vládou nařízené účtové osnovy nebo mapování účtů do skupiny, která je definována ústředím společnosti. Skupiny konsolidačních účtů naleznete v oblasti **Nastavení** modulu **Konsolidace**. Při přidání nové skupiny zadejte jedinečný identifikátor pro skupinu účtů a název.

## <a name="additional-consolidation-accounts"></a>Další konsolidační účty
Další konsolidační účty umožňují přiřadit účet z existující účtové osnovy do skupiny konsolidačních účtů. Potom můžete zadat hodnotu a název konsolidačního účtu. 

Další konsolidační účty naleznete v oblasti **Nastavení** modulu **Konsolidace**. Při vytváření nového konsolidačního účtu je nutné zadat následující informace:

-   **Hlavní účet** – toto pole je vyhledávání, které zobrazí všechny hlavní účty, které jsou založeny na účtových osnovách vybraných na stránce. Vyberete-li účet, název je automaticky zadán do pole **Název hlavního účtu**.
-   **Skupinu konsolidačních účtů** – toto pole použijte k určení skupiny, do které má být účet přiřazen. Při konsolidaci dvěma různými způsoby je nutné přidat stejný účet pro všechny čtyři skupiny konsolidačních účtů.
-   **Konsolidační účet** – zadejte hodnotu konsolidačního účtu. Tato hodnota nemusí být účet z účtové osnovy. Může to být libovolná požadovaná hodnota.
-   **Název konsolidačního účtu** – zadejte název účtu tak, jak se bude objevovat v dotazech a sestavách.
-   **Úrovně SAT** – toto pole slouží k oznámení výpisů z účtů pro mexické finanční úřady. 

Když dokončíte vytváření skupin konsolidačních účtů a dalších konsolidačních účtů, můžete zvolit skupinu v procesu online konsolidace.





