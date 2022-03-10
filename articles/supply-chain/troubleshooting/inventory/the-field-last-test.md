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
ms.openlocfilehash: 46523c55f4fd42b0985397752f0c62a3e1a55e177f2308e20b7064e339758269
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6742021"
---
# <a name="the-last-tested-date-field-isnt-updated-when-multiple-quality-orders-are-created"></a>Pole Datum posledního testování se neaktualizuje při vytvoření více objednávek kvality

Číslo článku znalostní báze: 4612803

## <a name="symptoms"></a>Příznaky

Pole **Datum posledního testování** se neaktualizuje při vytvoření více objednávek kvality.

## <a name="resolution"></a>Rozlišení

Systém se chová tak, jak byl navržen. Datum posledního testování nesouvisí s objednávkami kvality. Ukládá datum, kdy bylo hotové zboží poprvé zakoupeno nebo vyrobeno. Toto datum se používá k výpočtu data upozornění na dobu použitelnosti.
