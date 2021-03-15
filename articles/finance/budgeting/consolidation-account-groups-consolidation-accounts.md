---
title: Skupiny konsolidačních účtů a další konsolidační účty
description: Toto téma obsahuje informace o skupinách konsolidačních účtů a další konsolidačních účtech a vysvětluje způsob jejich použití v aplikaci Microsoft Dynamics 365 Finance.
author: aprilolson
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerConsolidateAccountGroup
audience: Application User
ms.reviewer: roschlom
ms.custom: 265544
ms.assetid: 71c31df7-b655-46a8-8844-4f92a8bd71b0
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 5a4e3b4d7bb1d5feefd843cdc347b4a08f94a85a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4982181"
---
# <a name="consolidation-account-groups-and-additional-consolidation-accounts"></a>Skupiny konsolidačních účtů a další konsolidační účty

[!include [banner](../includes/banner.md)]

Toto téma obsahuje informace o skupinách konsolidačních účtů a další konsolidačních účtech a vysvětluje způsob jejich použití v aplikaci Microsoft Dynamics 365 Finance.

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


Další informace naleznete v tématu [Vytvoření skupin konsolidace a další konsolidace účtů](../general-ledger/tasks/create-consolidation-groups.md). 





[!INCLUDE[footer-include](../../includes/footer-banner.md)]