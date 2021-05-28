---
title: Pole Datum posledního testování se neaktualizuje při vytvoření více objednávek kvality
description: Pole Datum posledního testování se neaktualizuje při vytvoření více objednávek kvality.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventBatch
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 6f796bdaa88d32b1c58dd8a4bca19f0ce4f3943d
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026348"
---
# <a name="the-last-tested-date-field-isnt-updated-when-multiple-quality-orders-are-created"></a>Pole Datum posledního testování se neaktualizuje při vytvoření více objednávek kvality

Číslo článku znalostní báze: 4612803

## <a name="symptoms"></a>Příznaky

Pole **Datum posledního testování** se neaktualizuje při vytvoření více objednávek kvality.

## <a name="resolution"></a>Rozlišení

Systém se chová tak, jak byl navržen. Datum posledního testování nesouvisí s objednávkami kvality. Ukládá datum, kdy bylo hotové zboží poprvé zakoupeno nebo vyrobeno. Toto datum se používá k výpočtu data upozornění na dobu použitelnosti.
