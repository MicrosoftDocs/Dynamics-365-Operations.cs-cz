---
title: Spravovat plánované objednávky
description: Toto téma obsahuje informace o postupu správy plánovaných objednávek. Popisuje, jak můžete aktualizovat stav plánovaných objednávek, upevnit je a zobrazit filtr plánovaných objednávek, které mají stejný stav, jako vybraná plánovaná objednávka.
author: roxanadiaconu
manager: AnnBe
ms.date: 11/07/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19151
ms.assetid: 54123f4c-b4ca-4ce4-9358-b067aa04c968
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 68bccb632255eac975dc150cf322d4c579ff2f24
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/18/2019
ms.locfileid: "2813769"
---
# <a name="maintain-planned-orders"></a><span data-ttu-id="e2975-104">Spravovat plánované objednávky</span><span class="sxs-lookup"><span data-stu-id="e2975-104">Maintain planned orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e2975-105">Toto téma obsahuje informace o postupu správy plánovaných objednávek.</span><span class="sxs-lookup"><span data-stu-id="e2975-105">This topic provides information about how to manage planned orders.</span></span> <span data-ttu-id="e2975-106">Popisuje, jak můžete aktualizovat stav plánovaných objednávek, upevnit je a zobrazit filtr plánovaných objednávek, které mají stejný stav, jako vybraná plánovaná objednávka.</span><span class="sxs-lookup"><span data-stu-id="e2975-106">It describes how you can update the status of planned orders, firm them, and filter for planned orders that have the same status as a selected planned order.</span></span>

<span data-ttu-id="e2975-107">Naplánované objednávky lze spravovat v pracovním prostoru **Hlavní plánování**, na seznamu **Plánovaná objednávka** nebo na seznamech **Plánované výrobní zakázky**, **Plánované nákupní objednávky** a **Plánovaný převod**.</span><span class="sxs-lookup"><span data-stu-id="e2975-107">You can manage planned orders from the **Master planning** workspace, the **Planned order** list, or the **Planned production orders**, **Planned purchase orders**, and **Planned transfer** lists.</span></span> 

## <a name="planned-order-status"></a><span data-ttu-id="e2975-108">Stav plánované objednávky</span><span class="sxs-lookup"><span data-stu-id="e2975-108">Planned order status</span></span>
<span data-ttu-id="e2975-109">Pole **Stav** lze použít ke sledování průběhu.</span><span class="sxs-lookup"><span data-stu-id="e2975-109">You can use the **Status** field to help track your progress.</span></span> <span data-ttu-id="e2975-110">Používají se následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="e2975-110">The following values are used:</span></span>

-   <span data-ttu-id="e2975-111">Když hlavní plánování vytvoří naplánované objednávky, mají stav **Nezpracovaná**.</span><span class="sxs-lookup"><span data-stu-id="e2975-111">When master planning generates planned orders, the planned orders have a status of **Unprocessed**.</span></span>
-   <span data-ttu-id="e2975-112">Když se rozhodnete plánovanou objednávku nepotvrdit, můžete jí přiřadit stav **Dokončeno**.</span><span class="sxs-lookup"><span data-stu-id="e2975-112">If you decide not to firm a planned order, you can give it a status of **Completed**.</span></span>
-   <span data-ttu-id="e2975-113">Chcete-li potvrdit plánovanou objednávku, můžete její stav změnit na **Schváleno**.</span><span class="sxs-lookup"><span data-stu-id="e2975-113">If you want to firm a planned order, you can change the status to **Approved**.</span></span> <span data-ttu-id="e2975-114">Plánované objednávky se stavem **Schváleno** jsou respektovány hlavním plánováním, takže nebudou během pozdějšího běhu hlavního plánování změněny ani odstraněny.</span><span class="sxs-lookup"><span data-stu-id="e2975-114">Planned orders with **Approved** status are respected by master planning, so they are not modified or deleted during a later master planning run.</span></span> 

## <a name="firming-planned-orders"></a><span data-ttu-id="e2975-115">Potvrzení plánovaných objednávek</span><span class="sxs-lookup"><span data-stu-id="e2975-115">Firming planned orders</span></span> 
<span data-ttu-id="e2975-116">Při potvrzení plánovaných objednávek jsou vytvořeny reálné objednávky.</span><span class="sxs-lookup"><span data-stu-id="e2975-116">By firming planned orders, real orders are created.</span></span> <span data-ttu-id="e2975-117">Tyto informace jsou také známy jako *vydané* nebo *otevřené* objednávky.</span><span class="sxs-lookup"><span data-stu-id="e2975-117">These are also know as *released* or *open orders*.</span></span> <span data-ttu-id="e2975-118">Když je plánovaná objednávka potvrzena, přesune se do částí objednávek příslušného modulu.</span><span class="sxs-lookup"><span data-stu-id="e2975-118">When a planned order is firmed, it's moved to the orders section of the relevant module.</span></span>

<span data-ttu-id="e2975-119">Na stránce **plánované objednávky** můžete vybrat dvě možnosti potvrzení:</span><span class="sxs-lookup"><span data-stu-id="e2975-119">You can select two firming options from the **Planned orders** page:</span></span>

-   <span data-ttu-id="e2975-120">**Pevné** – tímto potvrdíte jednu nebo více vybraných plánovaných objednávek.</span><span class="sxs-lookup"><span data-stu-id="e2975-120">**Firm** – This will firm one or multiple selected planned orders.</span></span>
-   <span data-ttu-id="e2975-121">**Potvrdit vše** – Tato akce potvrdí všech plánovaných objednávek ve filtru.</span><span class="sxs-lookup"><span data-stu-id="e2975-121">**Firm all** – This will firm all planned orders in the filter.</span></span> <span data-ttu-id="e2975-122">Když použijete možnost **Potvrdit vše**, nemusíte vybírat plánovanou objednávku, všechny plánované objednávky v rámci tohoto filtru budou potvrzeny.</span><span class="sxs-lookup"><span data-stu-id="e2975-122">Using **Firm all** you don’t have to select the planned order, all planned orders within the filter will be firmed.</span></span> <span data-ttu-id="e2975-123">Tato možnost může být užitečná v případě, že potvrzujete vysoký počet plánovaných objednávek.</span><span class="sxs-lookup"><span data-stu-id="e2975-123">This option can be useful if you are firming a high number of planned orders.</span></span>

> [!NOTE]
> <span data-ttu-id="e2975-124">Můžete sledovat plánovanou objednávku, která byla potvrzena v **Historii potvrzení** v části **Formulář plánované objednávky > Zobrazení > Historie potvrzení**.</span><span class="sxs-lookup"><span data-stu-id="e2975-124">You can track a planned order that was firmed from **Firming history** under **Planned orders form > View > Firming history**.</span></span>

## <a name="parallelize-firming"></a><span data-ttu-id="e2975-125">Paralelizovat potvrzení</span><span class="sxs-lookup"><span data-stu-id="e2975-125">Parallelize firming</span></span>
<span data-ttu-id="e2975-126">Pokud plánujete potvrdit více objednávek najednou, může paralelní provedení zlepšit dobu provádění nebo výkon.</span><span class="sxs-lookup"><span data-stu-id="e2975-126">If you are planning to firm many orders at the same time, parallelizing the run can improve the run time or performance.</span></span> <span data-ttu-id="e2975-127">Tato možnost je k dispozici při potvrzování více plánovaných objednávek pomocí možnosti **Potvrdit** nebo **Potvrdit vše**.</span><span class="sxs-lookup"><span data-stu-id="e2975-127">This option is available when firming multiple planned orders with either **Firm** or **Firm all**.</span></span> <span data-ttu-id="e2975-128">K dispozici jsou následující parametry:</span><span class="sxs-lookup"><span data-stu-id="e2975-128">The following parameters are available:</span></span>

-   <span data-ttu-id="e2975-129">**Paralelizovat potvrzení** – Pokud je nastaveno **Ano**, proces potvrzování bude paralelizován s počtem podprocesů definovaných v poli **Počet podprocesů**.</span><span class="sxs-lookup"><span data-stu-id="e2975-129">**Parallelize firming** – If **Yes**, the firming process will be parallelized with the number of threads defined in **Number of threads**.</span></span>
-   <span data-ttu-id="e2975-130">**Počet podprocesů** – řídí počet podprocesů použitých k parallelize procesu potvrzování.</span><span class="sxs-lookup"><span data-stu-id="e2975-130">**Number of threads** – Controls the number of threads used to parallelize the firming process.</span></span> <span data-ttu-id="e2975-131">Parametr se zobrazuje pouze tehdy, je-li volba **Paralelizovat potvrzení** nastavena na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="e2975-131">The parameter is only shown when **Parallelize firming** is set to **Yes**.</span></span>


<a name="additional-resources"></a><span data-ttu-id="e2975-132">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="e2975-132">Additional resources</span></span>
--------

[<span data-ttu-id="e2975-133">Přehled hlavních plánů</span><span class="sxs-lookup"><span data-stu-id="e2975-133">Master plans overview</span></span>](master-plans.md)



