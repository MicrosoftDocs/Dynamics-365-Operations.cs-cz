---
title: Schválit plánované objednávky
description: Tohle téma popisuje schválení plánovaných objednávek, které jsou podporovány optimalizací plánování.
author: ChristianRytt
manager: tfehr
ms.date: 08/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-08-21
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 8745a461986c1f16f2b3f9fd23011701d104a30c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5264011"
---
# <a name="approve-planned-orders"></a><span data-ttu-id="02442-103">Schválit plánované objednávky</span><span class="sxs-lookup"><span data-stu-id="02442-103">Approve planned orders</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="02442-104">Tohle téma poskytuje informace, jak aktualizovat stav plánovaných objednávek v optimalizaci plánování.</span><span class="sxs-lookup"><span data-stu-id="02442-104">This topic provides information about how to update the status of planned orders in Planning Optimization.</span></span>

<span data-ttu-id="02442-105">Schválení plánovaných objednávek je volitelným krokem na cestě k vytvoření potvrzené objednávky z plánované objednávky.</span><span class="sxs-lookup"><span data-stu-id="02442-105">Note that approval of planned orders is an optional step, on the way to create a firmed order from a planned order.</span></span> <span data-ttu-id="02442-106">Doporučujeme schválit změněné plánované objednávky, jinak budou úpravy ignorovány a přepsány při dalším běhu plánování.</span><span class="sxs-lookup"><span data-stu-id="02442-106">It is recommended to approve modified planned orders, otherwise the edits will be ignored and overwritten by the next planning run.</span></span>

![Tok plánované objednávky](media/approved-planned-orders-1.png)

<span data-ttu-id="02442-108">Pole **Stav** vám pomůže zvládnout váš postup využitím následujících hodnot:</span><span class="sxs-lookup"><span data-stu-id="02442-108">The **Status** field helps you tack your progress using the following values:</span></span>

- <span data-ttu-id="02442-109">**Nezpracováno:** Když hlavní plánování vytvoří naplánované objednávky, mají stav *Nezpracováno*.</span><span class="sxs-lookup"><span data-stu-id="02442-109">**Unprocessed:** When master planning generates planned orders, the planned orders have a status of *Unprocessed*.</span></span> <span data-ttu-id="02442-110">Plánované objednávky s tímto stavem budou odstraněny během dalšího běhu plánování.</span><span class="sxs-lookup"><span data-stu-id="02442-110">Planned orders with this status will be deleted during the next planning run.</span></span>
- <span data-ttu-id="02442-111">**Dokončeno:** Pokud se rozhodnete nepotvrdit plánovanou objednávku, můžete změnit stav na *Dokončeno* k označení, že jste dokončili vyhodnocení této plánované objednávky.</span><span class="sxs-lookup"><span data-stu-id="02442-111">**Completed:** If you decide not to firm a planned order, you can change the status to *Completed* to indicate that you completed evaluating this planned order.</span></span> <span data-ttu-id="02442-112">Mějte na paměti, že se stavy *Nezpracováno* a *Dokončeno* systém zachází stejně.</span><span class="sxs-lookup"><span data-stu-id="02442-112">Note that a status of *Unprocessed* and *Completed* are treated the same by the system.</span></span>
- <span data-ttu-id="02442-113">**Schváleno:** Chcete-li zachovat úpravy nebo plánujete potvrdit plánovanou objednávku, změňte stav na *Schváleno* .</span><span class="sxs-lookup"><span data-stu-id="02442-113">**Approved:** If you want to keep edits or are planning to firm a planned order, change the status to *Approved*.</span></span> <span data-ttu-id="02442-114">Plánované objednávky se stavem *Schváleno* jsou hlavním plánováním považovány za fixní a očekávané dodávky, takže nebudou během pozdějších běhů hlavního plánování změněny ani odstraněny.</span><span class="sxs-lookup"><span data-stu-id="02442-114">Planned orders with *Approved* status are considered as fixed and expected supply by master planning, so they are not modified or deleted during later master planning runs.</span></span> <span data-ttu-id="02442-115">Pro dosažení tohoto cíle logika plánování zkopíruje *schválené* plánované objednávky z původní verze plánu do nové verze plánu během hlavního plánování.</span><span class="sxs-lookup"><span data-stu-id="02442-115">To achieve this, the planning logic copies the *Approved* planned orders from the old plan version to the new plan version during master planning.</span></span> <span data-ttu-id="02442-116">Pamatujte si, že plánované objednávky ve stavu *Schváleno* jsou považovány za dodávky v rámci konkrétního hlavního plánu.</span><span class="sxs-lookup"><span data-stu-id="02442-116">Note that *Approved* planned orders are only considered supply within the specific master plan.</span></span>

<span data-ttu-id="02442-117">Naplánované objednávky lze spravovat v pracovním prostoru **Hlavní plánování**, na seznamu **Plánovaná objednávka** nebo na seznamech **Plánované výrobní zakázky**, **Plánované nákupní objednávky** a **Plánovaný převod**.</span><span class="sxs-lookup"><span data-stu-id="02442-117">You can manage planned orders from the  **Master planning**  workspace, the  **Planned order**  list, or the  **Planned production orders**,  **Planned purchase orders**, and  **Planned transfer**  lists.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]