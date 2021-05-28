---
title: Na kartě Aktivní ceny na stránce Cena zboží není žádná hodnota od data
description: Na kartě Aktivní ceny na stránce Cena zboží není žádná hodnota od data.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventItemPrice
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 3dd13f6a3e5ce3c894e96f420358d337f2e43dba
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026352"
---
# <a name="there-is-no-from-date-value-on-the-active-prices-tab-of-the-item-price-page"></a><span data-ttu-id="3d285-103">Na kartě Aktivní ceny na stránce Cena zboží není žádná hodnota od data</span><span class="sxs-lookup"><span data-stu-id="3d285-103">There is no From date value on the Active prices tab of the Item price page</span></span>

<span data-ttu-id="3d285-104">Číslo článku znalostní báze: 4613548</span><span class="sxs-lookup"><span data-stu-id="3d285-104">KB number: 4613548</span></span>

## <a name="symptoms"></a><span data-ttu-id="3d285-105">Příznaky</span><span class="sxs-lookup"><span data-stu-id="3d285-105">Symptoms</span></span>

<span data-ttu-id="3d285-106">Na kartě **Aktivní ceny** na stránce **Cena zboží** není žádná hodnota **Od data**.</span><span class="sxs-lookup"><span data-stu-id="3d285-106">There is no **From date** value on the **Active prices** tab of the **Item price** page.</span></span>

## <a name="resolution"></a><span data-ttu-id="3d285-107">Rozlišení</span><span class="sxs-lookup"><span data-stu-id="3d285-107">Resolution</span></span>

<span data-ttu-id="3d285-108">Hodnota **Od data** (datum účinnosti), která je nastavena na nevyřízenou cenu, se nepřenáší na aktivní cenu.</span><span class="sxs-lookup"><span data-stu-id="3d285-108">The **From date** value (effective date) that is set on the pending price isn't transferred to the active price.</span></span>

<span data-ttu-id="3d285-109">Záznam o ceně položky má po vložení stav *Čeká na zpracování* a zamýšlené datum účinnosti.</span><span class="sxs-lookup"><span data-stu-id="3d285-109">When an item cost record is first entered, it has a status of *Pending* and an intended effective date.</span></span> <span data-ttu-id="3d285-110">Když záznamu o ceně položky aktivujete, změní se jeho stav na *Aktivní* a datum účinnosti se změní na datum aktivace.</span><span class="sxs-lookup"><span data-stu-id="3d285-110">When you activate the item cost record, the status is updated to *Active*, and the effective date is updated to the activation date.</span></span> <span data-ttu-id="3d285-111">Proto je datum aktivace aktivní ceny vždy skutečným datem aktivace.</span><span class="sxs-lookup"><span data-stu-id="3d285-111">Therefore, the active price's activation date is always the actual date of the activation.</span></span>

<span data-ttu-id="3d285-112">Další informace naleznete v tématu [Přehled verzí výpočtu nákladů](../../cost-management/costing-versions.md).</span><span class="sxs-lookup"><span data-stu-id="3d285-112">For more information, see [Costing versions overview](../../cost-management/costing-versions.md).</span></span>
