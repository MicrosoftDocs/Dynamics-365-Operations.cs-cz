---
title: Vydaný produkt nemůžete smazat
description: Uvolněný produkt a všechny jeho varianty můžete odstranit, pouze pokud uvolněný produkt nemá žádné související transakce.
author: SmithaNataraj
ms.date: 06/11/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-11
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 2f03d45a36401314a4b02ff354fabb474568c48b
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475828"
---
# <a name="you-cant-delete-a-released-product"></a>Vydaný produkt nemůžete smazat

## <a name="symptoms"></a>Příznaky

Uvolněný produkt a všechny jeho varianty můžete odstranit, pouze pokud uvolněný produkt nemá žádné související transakce.

## <a name="resolution"></a>Řešení

Podle těchto pokynů odstraníte uvolněný produkt nebo základní produkt.

1. Zavřete všechny otevřené transakce pro položky.
1. Snižte zásoby na 0 (nula).
1. Proveďte uzávěrku skladu.
1. Odstraňte všechny varianty produktu pro hlavní produkt, který chcete odstranit.
