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
# <a name="the-last-tested-date-field-isnt-updated-when-multiple-quality-orders-are-created"></a><span data-ttu-id="e7f39-103">Pole Datum posledního testování se neaktualizuje při vytvoření více objednávek kvality</span><span class="sxs-lookup"><span data-stu-id="e7f39-103">The Last tested date field isn't updated when multiple quality orders are created</span></span>

<span data-ttu-id="e7f39-104">Číslo článku znalostní báze: 4612803</span><span class="sxs-lookup"><span data-stu-id="e7f39-104">KB number: 4612803</span></span>

## <a name="symptoms"></a><span data-ttu-id="e7f39-105">Příznaky</span><span class="sxs-lookup"><span data-stu-id="e7f39-105">Symptoms</span></span>

<span data-ttu-id="e7f39-106">Pole **Datum posledního testování** se neaktualizuje při vytvoření více objednávek kvality.</span><span class="sxs-lookup"><span data-stu-id="e7f39-106">The **Last tested date** field isn't updated when multiple quality orders are created.</span></span>

## <a name="resolution"></a><span data-ttu-id="e7f39-107">Rozlišení</span><span class="sxs-lookup"><span data-stu-id="e7f39-107">Resolution</span></span>

<span data-ttu-id="e7f39-108">Systém se chová tak, jak byl navržen.</span><span class="sxs-lookup"><span data-stu-id="e7f39-108">The system is behaving as designed.</span></span> <span data-ttu-id="e7f39-109">Datum posledního testování nesouvisí s objednávkami kvality.</span><span class="sxs-lookup"><span data-stu-id="e7f39-109">The last tested date isn't related to quality orders.</span></span> <span data-ttu-id="e7f39-110">Ukládá datum, kdy bylo hotové zboží poprvé zakoupeno nebo vyrobeno.</span><span class="sxs-lookup"><span data-stu-id="e7f39-110">It stores the date when the finished goods were first purchased or manufactured.</span></span> <span data-ttu-id="e7f39-111">Toto datum se používá k výpočtu data upozornění na dobu použitelnosti.</span><span class="sxs-lookup"><span data-stu-id="e7f39-111">This date is used to calculate the shelf life advice date.</span></span>
