---
title: Skupiny konsolidačních účtů a další konsolidační účty
description: Toto téma obsahuje informace o skupinách konsolidačních účtů a další konsolidačních účtech a vysvětluje způsob jejich použití.
author: panolte
ms.date: 01/11/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerConsolidateAccountGroup
audience: Application User
ms.reviewer: roschlom
ms.custom: 265544
ms.assetid: 71c31df7-b655-46a8-8844-4f92a8bd71b0
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 489f5417b6044e02d4711a03a17d6c19031cc2ee
ms.sourcegitcommit: 62ca651c94e61aaa69cfa59e861f263f89d01c4a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/03/2021
ms.locfileid: "7883380"
---
# <a name="consolidation-account-groups-and-additional-consolidation-accounts"></a>Skupiny konsolidačních účtů a další konsolidační účty

[!include [banner](../includes/banner.md)]

Toto téma obsahuje informace o skupinách konsolidačních účtů a další konsolidačních účtech a vysvětluje způsob jejich použití.

## <a name="consolidation-account-groups"></a>Skupiny konsolidačních účtů

Skupiny konsolidačních účtů umožňují vytvářet skupiny účtů, které chcete použít pro konsolidaci dat. Konsolidační účetní skupina obvykle představuje vládou nařízenou účtovou osnovu. Konsolidační skupina účtů může také mapovat účty do skupiny, která je definována centrálou společnosti. Skupiny konsolidačních účtů naleznete v oblasti **Nastavení** modulu **Konsolidace**. Při přidání nové skupiny zadejte jedinečný identifikátor pro skupinu účtů a název.

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
