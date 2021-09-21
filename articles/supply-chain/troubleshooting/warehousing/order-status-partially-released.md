---
title: Stav objednávky zůstává Částečně uvolněno i po fakturaci
description: V některých případech stav prodejní objednávky zůstává Částečně uvolněno i po její fakturaci. Tato stránka vysvětluje proč a uvádí možné řešení.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 8bfe7ecfd4beb6e77e8dd1e23ccd896d067bdb51
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475806"
---
# <a name="order-status-remains-partially-released-even-after-the-sales-order-is-invoiced"></a>Stav objednávky zůstává částečně uvolněn i po fakturaci prodejní objednávky

## <a name="symptoms"></a>Příznaky

Prodejní objednávka je objednávka dodání, ale jedna nebo více položek v ní má jiný způsob dodání. Po fakturaci objednávky má stále stav uvolnění *Částečně uvolněn*.

Například prodejní objednávka má dvě položky: jednu pro doručení a druhou pro vyzvednutí. Dodání i vyzvednutí byly provedeny. Proto byly oba řádky fakturovány. Stav uvolnění se však stále zobrazuje jako *Částečně uvolněno*, což je zavádějící.

## <a name="workaround"></a>Alternativní řešení

Stav uvolnění se vztahuje pouze na řádky objednávky, kde jsou položky povoleny pro správu skladu. Stav uvolnění proto zůstává *Částečně uvolněno* v tomto scénáři. Společnost Microsoft vyhodnotila tento problém a zjistila, že jde o omezení funkcí. Jako součást procesu dodacího listu a procesu fakturace bylo možné přidat rozšíření pro aktualizaci stavu uvolnění.
