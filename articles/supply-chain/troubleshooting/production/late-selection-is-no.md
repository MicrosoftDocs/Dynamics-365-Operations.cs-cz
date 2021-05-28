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
# <a name="late-selection-isnt-respected-when-production-orders-are-reset-via-a-batch-job"></a><span data-ttu-id="a1ac6-103">Při resetování produkčních objednávek pomocí dávkové úlohy není dodržen pozdní výběr</span><span class="sxs-lookup"><span data-stu-id="a1ac6-103">Late selection isn't respected when production orders are reset via a batch job</span></span>

<span data-ttu-id="a1ac6-104">Číslo článku znalostní báze: 4614634</span><span class="sxs-lookup"><span data-stu-id="a1ac6-104">KB number: 4614634</span></span>

## <a name="symptoms"></a><span data-ttu-id="a1ac6-105">Příznaky</span><span class="sxs-lookup"><span data-stu-id="a1ac6-105">Symptoms</span></span>

<span data-ttu-id="a1ac6-106">Když použijete opakovanou dávkovou úlohu k obnovení stavu výrobní zakázky, nebudou respektovány pozdní výběry.</span><span class="sxs-lookup"><span data-stu-id="a1ac6-106">When you use a recurring batch job to reset the status of a production order, late selections aren't respected.</span></span>

## <a name="resolution"></a><span data-ttu-id="a1ac6-107">Rozlišení</span><span class="sxs-lookup"><span data-stu-id="a1ac6-107">Resolution</span></span>

<span data-ttu-id="a1ac6-108">Současný design nepodporuje použití pozdního výběru pro proces *Resetovat stav*.</span><span class="sxs-lookup"><span data-stu-id="a1ac6-108">The current design doesn't support the use of late selections for the *Reset status* process.</span></span>
