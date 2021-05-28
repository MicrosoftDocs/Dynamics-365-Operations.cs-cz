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
ms.openlocfilehash: a8af535257ce217629d5ba92e624623c3ea39345
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026350"
---
# <a name="quantity-on-a-started-quarantine-order-isnt-updated-when-the-order-is-split"></a><span data-ttu-id="52d98-103">Množství u zahájené objednávky karantény se při rozdělení objednávky neaktualizuje</span><span class="sxs-lookup"><span data-stu-id="52d98-103">Quantity on a started quarantine order isn't updated when the order is split</span></span>

<span data-ttu-id="52d98-104">Číslo článku znalostní báze: 4613113</span><span class="sxs-lookup"><span data-stu-id="52d98-104">KB number: 4613113</span></span>

## <a name="symptoms"></a><span data-ttu-id="52d98-105">Příznaky</span><span class="sxs-lookup"><span data-stu-id="52d98-105">Symptoms</span></span>

<span data-ttu-id="52d98-106">Když vytvoříte objednávku karantény a pokusíte se ji rozdělit, množství objednávky se po rozdělení neaktualizuje.</span><span class="sxs-lookup"><span data-stu-id="52d98-106">When you create a quarantine order and try to split it, the order quantity isn't updated to the remaining quantity after the split.</span></span>

## <a name="resolution"></a><span data-ttu-id="52d98-107">Rozlišení</span><span class="sxs-lookup"><span data-stu-id="52d98-107">Resolution</span></span>

<span data-ttu-id="52d98-108">Systém nezmění původní množství z objednávky karantény, aby zajistil, že můžete sledovat původní množství, které bylo pro danou objednávku karantény vytvořeno.</span><span class="sxs-lookup"><span data-stu-id="52d98-108">The system doesn't change the original quantity from a quarantine order to ensure that you can track the original quantity that was created for that quarantine order.</span></span> <span data-ttu-id="52d98-109">Systém však sleduje množství, které je rozděleno z objednávky karantény.</span><span class="sxs-lookup"><span data-stu-id="52d98-109">However, the system does track the quantity that is split from a quarantine order.</span></span> <span data-ttu-id="52d98-110">K tomuto sledování používá databázové pole s názvem `QuantityThatHasSplitIntoOtherQuarantineOrders`.</span><span class="sxs-lookup"><span data-stu-id="52d98-110">To do this tracking, it uses a database field that is named `QuantityThatHasSplitIntoOtherQuarantineOrders`.</span></span> <span data-ttu-id="52d98-111">Toto pole se však nezobrazuje v uživatelském rozhraní (UI).</span><span class="sxs-lookup"><span data-stu-id="52d98-111">However, this field isn't visible in the user interface (UI).</span></span>
