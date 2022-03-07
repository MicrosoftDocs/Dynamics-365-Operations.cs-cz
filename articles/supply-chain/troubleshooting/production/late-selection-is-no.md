---
title: Při resetování produkčních objednávek pomocí dávkové úlohy není dodržen pozdní výběr
description: Když použijete opakovanou dávkovou úlohu k obnovení stavu výrobní zakázky, nebudou respektovány pozdní výběry.
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: e53198f427f4060421a4f0078277682c43db1320
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026331"
---
# <a name="late-selection-isnt-respected-when-production-orders-are-reset-via-a-batch-job"></a>Při resetování produkčních objednávek pomocí dávkové úlohy není dodržen pozdní výběr

Číslo článku znalostní báze: 4614634

## <a name="symptoms"></a>Příznaky

Když použijete opakovanou dávkovou úlohu k obnovení stavu výrobní zakázky, nebudou respektovány pozdní výběry.

## <a name="resolution"></a>Rozlišení

Současný design nepodporuje použití pozdního výběru pro proces *Resetovat stav*.
