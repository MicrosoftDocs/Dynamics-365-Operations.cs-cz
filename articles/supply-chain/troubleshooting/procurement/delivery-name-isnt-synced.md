---
title: Po změně dodací adresy nákupní objednávky není název doručení synchronizován
description: Po změně dodací adresy v záhlaví nákupní objednávky se název dodávky nesynchronizuje.
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 588d1ef6250d249aa4fc9da4f5125e9a34c0255f
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475764"
---
# <a name="the-delivery-name-isnt-synced-after-changing-a-purchase-order-delivery-address"></a>Po změně dodací adresy nákupní objednávky není název doručení synchronizován

## <a name="symptoms"></a>Příznaky

Adresa v záhlaví nákupní objednávky se aktualizuje na adresu, která není doručovací adresou. I když je adresa na nákupní objednávce aktualizována, název dodávky není aktualizován na základě aktualizované adresy.

## <a name="resolution"></a>Řešení

Toto chování je záměrné. Vybraná adresa musí být klasifikována jako doručovací adresa. Jinak se název doručení neaktualizuje na základě vybrané adresy.
