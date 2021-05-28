---
title: Kumulace zákaznických slev selže při použití skupin slev na položky
description: Když použijete dohody o slevách na zákazníka v kombinaci se skupinami slev na položky, vypočítají se slevy, ale kumulace selže.
author: sherry-zheng
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: PdsRebateTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 5222d5a52a34ecfa4a1eac96a2cb561f257f17ea
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026327"
---
# <a name="cumulation-of-customer-rebates-fails-when-item-rebate-groups-are-used"></a><span data-ttu-id="3b7d9-103">Kumulace zákaznických slev selže při použití skupin slev na položky</span><span class="sxs-lookup"><span data-stu-id="3b7d9-103">Cumulation of customer rebates fails when item rebate groups are used</span></span>

<span data-ttu-id="3b7d9-104">Číslo článku znalostní báze: 4611372</span><span class="sxs-lookup"><span data-stu-id="3b7d9-104">KB number: 4611372</span></span>

## <a name="symptoms"></a><span data-ttu-id="3b7d9-105">Příznaky</span><span class="sxs-lookup"><span data-stu-id="3b7d9-105">Symptoms</span></span>

<span data-ttu-id="3b7d9-106">Když použijete dohody o slevách (typu *částka*) v kombinaci se skupinami slev na položky, vypočítají se slevy, ale kumulace selže.</span><span class="sxs-lookup"><span data-stu-id="3b7d9-106">When you use customer rebate agreements (of the *amount* type) in combination with item rebate groups, rebates are calculated, but cumulation fails.</span></span>

## <a name="resolution"></a><span data-ttu-id="3b7d9-107">Rozlišení</span><span class="sxs-lookup"><span data-stu-id="3b7d9-107">Resolution</span></span>

<span data-ttu-id="3b7d9-108">Systém se chová tak, jak byl navržen.</span><span class="sxs-lookup"><span data-stu-id="3b7d9-108">The system is behaving as designed.</span></span> <span data-ttu-id="3b7d9-109">Skupiny položek seskupují pouze položky, které mají stejnou podmínku prahové hodnoty.</span><span class="sxs-lookup"><span data-stu-id="3b7d9-109">Item groups group only items that have the same threshold condition.</span></span> <span data-ttu-id="3b7d9-110">Podmínka slevy (prahová hodnota) je nastavena proti částce pro každou položku, nikoli proti kumulované částce pro jakoukoli položku ve skupině položek.</span><span class="sxs-lookup"><span data-stu-id="3b7d9-110">The rebate condition (threshold) is set against the amount for each item, not against the cumulated amount for any item in the item group.</span></span>
