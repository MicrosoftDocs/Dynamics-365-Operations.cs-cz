---
title: "Spravovat plánované objednávky"
description: "Tento článek obsahuje informace o postupu správy plánovaných objednávek. Popisuje, jak můžete aktualizovat stav plánovaných objednávek, upevnit je a zobrazit filtr plánovaných objednávek, které mají stejný stav, jako vybraná plánovaná objednávka."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 19151
ms.assetid: 54123f4c-b4ca-4ce4-9358-b067aa04c968
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: c63fb039fc3bda00073c3e2a808a06b1d745a786
ms.contentlocale: cs-cz
ms.lasthandoff: 04/13/2018

---

# <a name="maintain-planned-orders"></a><span data-ttu-id="eb9a4-104">Spravovat plánované objednávky</span><span class="sxs-lookup"><span data-stu-id="eb9a4-104">Maintain planned orders</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="eb9a4-105">Tento článek obsahuje informace o postupu správy plánovaných objednávek.</span><span class="sxs-lookup"><span data-stu-id="eb9a4-105">This article provides information about how to manage planned orders.</span></span> <span data-ttu-id="eb9a4-106">Popisuje, jak můžete aktualizovat stav plánovaných objednávek, upevnit je a zobrazit filtr plánovaných objednávek, které mají stejný stav, jako vybraná plánovaná objednávka.</span><span class="sxs-lookup"><span data-stu-id="eb9a4-106">It describes how you can update the status of planned orders, firm them, and filter for planned orders that have the same status as a selected planned order.</span></span>

<span data-ttu-id="eb9a4-107">Naplánované objednávky lze spravovat v pracovním prostoru **Hlavní plánování**, na seznamu **Plánovaná objednávka** nebo na seznamech **Plánované výrobní zakázky**, **Plánované nákupní objednávky** a **Plánovaný převod**.</span><span class="sxs-lookup"><span data-stu-id="eb9a4-107">You can manage planned orders from the **Master planning** workspace, the **Planned order** list, or the **Planned production orders**, **Planned purchase orders**, and **Planned transfer** lists.</span></span> <span data-ttu-id="eb9a4-108">Pole **Stav** lze použít ke sledování průběhu.</span><span class="sxs-lookup"><span data-stu-id="eb9a4-108">You can use the **Status** field to help track your progress.</span></span> <span data-ttu-id="eb9a4-109">Používají se následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="eb9a4-109">The following values are used:</span></span>

-   <span data-ttu-id="eb9a4-110">Když hlavní plánování vytvoří naplánované objednávky, mají stav **Nezpracovaná**.</span><span class="sxs-lookup"><span data-stu-id="eb9a4-110">When master planning generates planned orders, the planned orders have a status of **Unprocessed**.</span></span>
-   <span data-ttu-id="eb9a4-111">Když se rozhodnete plánovanou objednávku nepotvrdit, můžete jí přiřadit stav **Dokončeno**.</span><span class="sxs-lookup"><span data-stu-id="eb9a4-111">If you decide not to firm a planned order, you can give it a status of **Completed**.</span></span>
-   <span data-ttu-id="eb9a4-112">Když se rozhodnete plánovanou objednávku potvrdit, můžete jí přiřadit stav **Schváleno**.</span><span class="sxs-lookup"><span data-stu-id="eb9a4-112">When you decide to firm a planned order, you can give it a status of **Approved**.</span></span> <span data-ttu-id="eb9a4-113">Tento stav označuje, že schvalujete potvrzení plánované objednávky, ale ta však ještě není potvrzena.</span><span class="sxs-lookup"><span data-stu-id="eb9a4-113">This status indicates that you approve firming of the planned order, but it isn't firmed yet.</span></span>

<span data-ttu-id="eb9a4-114">**Poznámka:** Schválená plánovaná objednávka je přesunuta v aktuálním stavu k dalšímu výpočtu hlavního plánování.</span><span class="sxs-lookup"><span data-stu-id="eb9a4-114">**Note:** An approved planned order is transferred, in its current state, to the next master planning calculation.</span></span> <span data-ttu-id="eb9a4-115">Plánované objednávky lze potvrdit kliknutím na položku **Potvrdit**.</span><span class="sxs-lookup"><span data-stu-id="eb9a4-115">You can firm planned orders by clicking **Firm**.</span></span> <span data-ttu-id="eb9a4-116">Upevnit lze následující plánované objednávky:</span><span class="sxs-lookup"><span data-stu-id="eb9a4-116">You can firm the following planned orders:</span></span>

-   <span data-ttu-id="eb9a4-117">Plánovaná objednávka, která je vybrána.</span><span class="sxs-lookup"><span data-stu-id="eb9a4-117">The planned order that is selected.</span></span>
-   <span data-ttu-id="eb9a4-118">Více plánovaných objednávek.</span><span class="sxs-lookup"><span data-stu-id="eb9a4-118">Multiple planned orders.</span></span>
-   <span data-ttu-id="eb9a4-119">Plánované objednávky vytvořené rozpadem na stránce **Rozpad**.</span><span class="sxs-lookup"><span data-stu-id="eb9a4-119">Planned orders that are generated by an explosion from the **Explosion** page.</span></span> <span data-ttu-id="eb9a4-120">Klikněte na možnost **Plánované objednávky**, vyberte plánovanou objednávku a klikněte na položku **Potvrdit**.</span><span class="sxs-lookup"><span data-stu-id="eb9a4-120">Click **Planned orders**, select the planned order, and then click **Firm**.</span></span>

<span data-ttu-id="eb9a4-121">Když je plánovaná objednávka potvrzena, přesune se do částí objednávek příslušného modulu.</span><span class="sxs-lookup"><span data-stu-id="eb9a4-121">When a planned order is firmed, it's moved to the orders section of the relevant module.</span></span> <span data-ttu-id="eb9a4-122">**Poznámka:** Můžete kliknout pravým tlačítkem na plánovanou objednávku s určitým stavem a pomocí filtru zobrazit ostatní objednávky se stejným stavem.</span><span class="sxs-lookup"><span data-stu-id="eb9a4-122">**Note:** You can right-click a planned order that has a particular status and filter for other planned orders that have the same status.</span></span> <span data-ttu-id="eb9a4-123">Tato funkce je užitečná, pokud například chcete zobrazit všechny plánované objednávky, které mají stav **Schváleno**, abyste je mohli poté potvrdit.</span><span class="sxs-lookup"><span data-stu-id="eb9a4-123">This functionality is useful if, for example, you want to filter for all planned orders that have a status of **Approved**, so that you can then firm them.</span></span>

<a name="see-also"></a><span data-ttu-id="eb9a4-124">Viz také</span><span class="sxs-lookup"><span data-stu-id="eb9a4-124">See also</span></span>
--------

[<span data-ttu-id="eb9a4-125">Hlavní plány</span><span class="sxs-lookup"><span data-stu-id="eb9a4-125">Master plans</span></span>](master-plans.md)




