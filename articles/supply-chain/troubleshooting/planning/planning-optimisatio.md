---
title: Plánovaná nákupní objednávka se vytvoří, když nákup existuje do záporných dnů
description: Pokud je kód pokrytí min./max., Optimalizace plánování vytvoří plánovanou nákupní objednávku, pokud existuje nákup v záporných dnech.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo,MpsIntegrationParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ilebedev
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 826496c2de956ff949dd79ab8aa643053719bf75
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026343"
---
# <a name="planned-purchase-order-is-created-when-a-purchase-exists-within-negative-days"></a><span data-ttu-id="d7f3a-103">Plánovaná nákupní objednávka se vytvoří, když nákup existuje do záporných dnů</span><span class="sxs-lookup"><span data-stu-id="d7f3a-103">Planned purchase order is created when a purchase exists within negative days</span></span>

<span data-ttu-id="d7f3a-104">Číslo článku znalostní báze: 4614298</span><span class="sxs-lookup"><span data-stu-id="d7f3a-104">KB number: 4614298</span></span>

## <a name="symptoms"></a><span data-ttu-id="d7f3a-105">Příznaky</span><span class="sxs-lookup"><span data-stu-id="d7f3a-105">Symptoms</span></span>

<span data-ttu-id="d7f3a-106">Pokud je kód pokrytí *min./max.*, Optimalizace plánování vytvoří plánovanou nákupní objednávku, pokud existuje nákup v záporných dnech.</span><span class="sxs-lookup"><span data-stu-id="d7f3a-106">If the coverage code is *Min/max*, Planning Optimization creates a planned purchase order when a purchase exists within negative days.</span></span>

## <a name="resolution"></a><span data-ttu-id="d7f3a-107">Rozlišení</span><span class="sxs-lookup"><span data-stu-id="d7f3a-107">Resolution</span></span>

<span data-ttu-id="d7f3a-108">Optimalizace plánování nepodporuje negativní dny.</span><span class="sxs-lookup"><span data-stu-id="d7f3a-108">Planning Optimization doesn't support negative days.</span></span> <span data-ttu-id="d7f3a-109">Vždy však zajistí, že plánované objednávky nebudou naplánovány v době realizace vzhledem k aktuálnímu datu.</span><span class="sxs-lookup"><span data-stu-id="d7f3a-109">However, it always ensures that planned orders won't be scheduled within the lead time relative to the current date.</span></span> <span data-ttu-id="d7f3a-110">Například dodací lhůta pro nákup je 10 dní a očekává se, že nákupní objednávka dorazí osm dní ode dneška.</span><span class="sxs-lookup"><span data-stu-id="d7f3a-110">For example, the purchase lead time is 10 days, and a purchase order is expected to arrive eight days from today.</span></span> <span data-ttu-id="d7f3a-111">V takovém případě bude nákupní objednávka použita jako nabídka pro poptávku, což je pět dní ode dneška.</span><span class="sxs-lookup"><span data-stu-id="d7f3a-111">In this case, the purchase order will be used as supply for demand that is five days from today.</span></span>

<span data-ttu-id="d7f3a-112">Proto doporučujeme upravit dobu realizace tak, aby pokryla všechny (nebo téměř všechny) vaše scénáře.</span><span class="sxs-lookup"><span data-stu-id="d7f3a-112">Therefore, we recommend that you adjust your lead times to cover all (or almost all) of your scenarios.</span></span>
