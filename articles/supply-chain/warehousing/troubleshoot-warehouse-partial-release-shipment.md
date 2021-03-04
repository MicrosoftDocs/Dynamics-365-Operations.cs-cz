---
title: Odstraňování potíží s částečným uvolněním a částečnou dodávkou
description: Toto téma popisuje, jak vyřešit běžné problémy, s nimiž se můžete setkat při práci s příchozími s částečným uvolněním a částečnými dodávkami v Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: e89a430f90374733b23fadaf53f5bab598d67d62
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645941"
---
# <a name="troubleshoot-partial-releases-and-partial-shipments"></a>Odstraňování potíží s částečným uvolněním a částečnou dodávkou

[!include [banner](../includes/banner.md)]

Toto téma popisuje, jak vyřešit běžné problémy, s nimiž se můžete setkat při práci s příchozími s částečným uvolněním a částečnými dodávkami v Microsoft Dynamics 365 Supply Chain Management.

## <a name="the-release-status-of-a-sales-order-remains-partially-released-even-after-the-sales-order-is-invoiced"></a>Stav uvolnění prodejní objednávky zůstává Částečně uvolněn i po fakturaci prodejní objednávky.

### <a name="issue-description"></a>Popis problému

Prodejní objednávka je objednávka dodání, ale jedna nebo více položek v ní má jiný způsob dodání. Po fakturaci objednávky má stále stav uvolnění *Částečně uvolněn*.

Například prodejní objednávka má dvě položky: jednu pro doručení a druhou pro vyzvednutí. Dodání i vyzvednutí byly provedeny. Proto byly oba řádky fakturovány. Stav uvolnění se však stále zobrazuje jako *Částečně uvolněno*, což je zavádějící.

### <a name="issue-resolution"></a>Řešení problému

Stav uvolnění se vztahuje pouze na řádky objednávky, kde jsou položky povoleny pro správu skladu. Stav uvolnění proto zůstává *Částečně uvolněno* v tomto scénáři. Společnost Microsoft vyhodnotila tento problém a zjistila, že jde o omezení funkcí. Jako součást procesu dodacího listu a procesu fakturace bylo možné přidat rozšíření pro aktualizaci stavu uvolnění.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]