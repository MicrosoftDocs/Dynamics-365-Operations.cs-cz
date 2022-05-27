---
title: Funkční mezery mezi sestavami o hodnotě/stárnutí zásob a jejich verzemi úložiště
description: Funkční mezery mezi sestavami o hodnotě/stárnutí zásob a jejich verzemi úložiště
author: AndersGirke
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: InventAgingStorage, InventAgingStorageChart, InventAgingStorageDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: f74389648034bf036ce48ac84b3421a8a340f105
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/04/2022
ms.locfileid: "8686646"
---
# <a name="functional-gaps-between-inventory-valueaging-reports-and-their-storage-versions"></a>Funkční mezery mezi sestavami o hodnotě/stárnutí zásob a jejich verzemi úložiště

Funkce [Uložení sestavy stáří zásob](/dynamics365/supply-chain/cost-management/inventory-aging-report-storage) a [Sestava úložiště hodnot zásob](/dynamics365/supply-chain/cost-management/inventory-value-report-storage) umožňují aplikaci Supply Chain Management zobrazit velké objemy transakcí zásob. V každém případě se výsledky sestavy ukládají k procházení a exportu, na rozdíl od verzí těchto sestav bez úložiště. Některé funkce, které existují ve verzích těchto sestav bez úložiště, však ve verzích úložiště neexistují. Následující pododdíly shrnují rozdíly a poskytují alternativní řešení.

## <a name="storage-reports-dont-include-subtotals-even-if-they-are-enabled-in-the-report-layout"></a>Sestavy úložiště nezahrnují mezisoučty, i když jsou povoleny v rozložení sestavy

Mezisoučty mohou způsobit problémy při exportu výsledku, zejména pokud uživatelé změní sekvenci záznamů.

Chcete-li zkontrolovat mezisoučty, můžete exportovat výsledek do Microsoft Excel. Alternativně, pokud chcete zkontrolovat mezisoučty v rámci Supply Chain Management, použijte [správu funkcí](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview) a povolte funkce *Nový ovládací prvek mřížky* a *Seskupení do mřížek*, které poskytují mnohem flexibilnější způsob, jak zobrazit mezisoučet pro každou skupinu podle sloupce. Další informace naleznete v části [Schopnosti mřížky](/dynamics365/fin-ops-core/fin-ops/get-started/grid-capabilities).

## <a name="inventory-value-storage-report-doesnt-support-ledger-account-information"></a>Sestava úložiště hodnot zásob nepodporuje informace o účtu hlavní knihy

Můžete spustit předvahu, abyste získali zůstatek na účtech zásob a porovnali jej se sestavou **Úložiště hodnot zásob**.
