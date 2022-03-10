---
title: Množství u zahájené objednávky karantény se při rozdělení objednávky neaktualizuje
description: Když vytvoříte objednávku karantény a pokusíte se ji rozdělit, množství objednávky se neaktualizuje na rozdělené zbývající množství.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventQuarantineOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: shawan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 4625570cb706199dca78f23b1864ca1d81cc66e896cf10d6d5f16cf1a9d1dc16
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6713487"
---
# <a name="quantity-on-a-started-quarantine-order-isnt-updated-when-the-order-is-split"></a>Množství u zahájené objednávky karantény se při rozdělení objednávky neaktualizuje

Číslo článku znalostní báze: 4613113

## <a name="symptoms"></a>Příznaky

Když vytvoříte objednávku karantény a pokusíte se ji rozdělit, množství objednávky se po rozdělení neaktualizuje.

## <a name="resolution"></a>Rozlišení

Systém nezmění původní množství z objednávky karantény, aby zajistil, že můžete sledovat původní množství, které bylo pro danou objednávku karantény vytvořeno. Systém však sleduje množství, které je rozděleno z objednávky karantény. K tomuto sledování používá databázové pole s názvem `QuantityThatHasSplitIntoOtherQuarantineOrders`. Toto pole se však nezobrazuje v uživatelském rozhraní (UI).
