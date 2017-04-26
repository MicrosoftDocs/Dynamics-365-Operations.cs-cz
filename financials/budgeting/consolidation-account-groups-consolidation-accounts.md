---
title: "Další konsolidační účty a skupiny konsolidačních účtů"
description: "Toto téma obsahuje informace o další konsolidační účty a skupiny konsolidačních účtů a vysvětluje způsob jejich použití v aplikaci Microsoft Dynamics 365 pro operace."
author: RobinARH
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 265544
ms.assetid: 71c31df7-b655-46a8-8844-4f92a8bd71b0
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 9f4d7fdd8cfa7a540fce219f6ae4792e57dfbe44
ms.openlocfilehash: f9c5aaa389c9c2f85d1ab91cbf3d2222cbebef55
ms.lasthandoff: 03/31/2017


---

# <a name="consolidation-account-groups-and-additional-consolidation-accounts"></a>Další konsolidační účty a skupiny konsolidačních účtů

[!include[banner](../includes/banner.md)]


Toto téma obsahuje informace o další konsolidační účty a skupiny konsolidačních účtů a vysvětluje způsob jejich použití v aplikaci Microsoft Dynamics 365 pro operace.

<a name="consolidation-account-groups"></a>Skupiny konsolidačních účtů
----------------------------

Skupiny konsolidačních účtů umožňují vytvářet skupiny účtů, které chcete použít ke sloučení dat. Nejčastěji používané skupinu konsolidačních účtů představuje nařízené vládou účtové osnovy nebo mapování účtů do skupiny, který je definován v sídle společnosti. Můžete najít konsolidace skupiny účtů v **nastavení** oblast **konsolidace** modulu. Při přidání nové skupiny zadejte jedinečný identifikátor pro skupinu účtů a název.

## <a name="additional-consolidation-accounts"></a>Další konsolidační účty
Další konsolidační účty umožňují přiřadit účet z existující účtové osnově skupinu konsolidačních účtů. Potom zadáte hodnotu účtu konsolidace a název. 

Můžete najít další konsolidační účty v **nastavení** oblast **konsolidace** modulu. Při vytváření nového účtu konsolidace, je nutné zadat následující informace:

-   **Hlavní účet** – toto pole je vyhledávání, které jsou uvedeny hlavní účty, které jsou založeny na účtové osnovy, které jste vybrali na stránce. Vyberete-li účet, název je automaticky zadána **název účtu hlavní** pole.
-   **Skupinu konsolidačních účtů** – toto pole použít k určení skupiny přiřadit účet. Při konsolidaci dvěma různými způsoby, je nutné přidat stejný účet pro všechny skupiny čtyř konsolidačních účtů.
-   **Konsolidační účet** – zadejte hodnotu konsolidační účet. Tato hodnota nemusí být účet z účtové osnovy. Může být libovolná hodnota, které požadujete.
-   **Název účtu konsolidace** – zadejte název účtu, který chcete zobrazit v dotazech a sestavách.
-   **Úrovně SAT** – toto pole slouží k oznámení výpisy z účtu mexických finančnímu úřadu. 

Po dokončení vytváření skupiny konsolidačních účtů a další konsolidační účty můžete konsolidovat online procesu vyberte skupinu.





