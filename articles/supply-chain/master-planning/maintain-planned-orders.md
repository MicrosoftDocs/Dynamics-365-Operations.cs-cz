---
title: Spravovat plánované objednávky
description: Toto téma obsahuje informace o postupu správy plánovaných objednávek. Popisuje, jak můžete aktualizovat stav plánovaných objednávek, upevnit je a zobrazit filtr plánovaných objednávek, které mají stejný stav, jako vybraná plánovaná objednávka.
author: roxanadiaconu
manager: tfehr
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransPo, ReqTransFirmLog
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19151
ms.assetid: 54123f4c-b4ca-4ce4-9358-b067aa04c968
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f62381ca212e711fd61e12c9ec8f066ec124a933
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4424053"
---
# <a name="maintain-planned-orders"></a><span data-ttu-id="9ed98-104">Spravovat plánované objednávky</span><span class="sxs-lookup"><span data-stu-id="9ed98-104">Maintain planned orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9ed98-105">Toto téma obsahuje informace o postupu správy plánovaných objednávek.</span><span class="sxs-lookup"><span data-stu-id="9ed98-105">This topic provides information about how to manage planned orders.</span></span> <span data-ttu-id="9ed98-106">Popisuje, jak můžete aktualizovat stav plánovaných objednávek, upevnit je a zobrazit filtr plánovaných objednávek, které mají stejný stav, jako vybraná plánovaná objednávka.</span><span class="sxs-lookup"><span data-stu-id="9ed98-106">It describes how you can update the status of planned orders, firm them, and filter for planned orders that have the same status as a selected planned order.</span></span>

<span data-ttu-id="9ed98-107">Naplánované objednávky lze spravovat v pracovním prostoru **Hlavní plánování**, na seznamu **Plánovaná objednávka** nebo na seznamech **Plánované výrobní zakázky**, **Plánované nákupní objednávky** a **Plánovaný převod**.</span><span class="sxs-lookup"><span data-stu-id="9ed98-107">You can manage planned orders from the **Master planning** workspace, the **Planned order** list, or the **Planned production orders**, **Planned purchase orders**, and **Planned transfer** lists.</span></span> 

## <a name="planned-order-status"></a><span data-ttu-id="9ed98-108">Stav plánované objednávky</span><span class="sxs-lookup"><span data-stu-id="9ed98-108">Planned order status</span></span>
<span data-ttu-id="9ed98-109">Pole **Stav** lze použít ke sledování průběhu.</span><span class="sxs-lookup"><span data-stu-id="9ed98-109">You can use the **Status** field to help track your progress.</span></span> <span data-ttu-id="9ed98-110">Používají se následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="9ed98-110">The following values are used:</span></span>

-   <span data-ttu-id="9ed98-111">Když hlavní plánování vytvoří naplánované objednávky, mají stav **Nezpracovaná**.</span><span class="sxs-lookup"><span data-stu-id="9ed98-111">When master planning generates planned orders, the planned orders have a status of **Unprocessed**.</span></span>
-   <span data-ttu-id="9ed98-112">Když se rozhodnete plánovanou objednávku nepotvrdit, můžete jí přiřadit stav **Dokončeno**.</span><span class="sxs-lookup"><span data-stu-id="9ed98-112">If you decide not to firm a planned order, you can give it a status of **Completed**.</span></span>
-   <span data-ttu-id="9ed98-113">Chcete-li potvrdit plánovanou objednávku, můžete její stav změnit na **Schváleno**.</span><span class="sxs-lookup"><span data-stu-id="9ed98-113">If you want to firm a planned order, you can change the status to **Approved**.</span></span> <span data-ttu-id="9ed98-114">Plánované objednávky se stavem **Schváleno** jsou respektovány hlavním plánováním, takže nebudou během pozdějšího běhu hlavního plánování změněny ani odstraněny.</span><span class="sxs-lookup"><span data-stu-id="9ed98-114">Planned orders with **Approved** status are respected by master planning, so they are not modified or deleted during a later master planning run.</span></span> <span data-ttu-id="9ed98-115">Pro dosažení tohoto cíle logika plánování zkopíruje **schválené** plánované objednávky z původní verze plánu do nové verze plánu během hlavního plánování.</span><span class="sxs-lookup"><span data-stu-id="9ed98-115">To achieve this, the planning logic copies the **Approved** planned orders from the old plan version to the new plan version during master planning.</span></span>

## <a name="firming-planned-orders"></a><span data-ttu-id="9ed98-116">Potvrzení plánovaných objednávek</span><span class="sxs-lookup"><span data-stu-id="9ed98-116">Firming planned orders</span></span> 
<span data-ttu-id="9ed98-117">Při potvrzení plánovaných objednávek jsou vytvořeny reálné objednávky.</span><span class="sxs-lookup"><span data-stu-id="9ed98-117">By firming planned orders, real orders are created.</span></span> <span data-ttu-id="9ed98-118">Ty jsou známy také jako *vydané* nebo *otevřené* objednávky.</span><span class="sxs-lookup"><span data-stu-id="9ed98-118">These are also known as *released* or *open orders*.</span></span> <span data-ttu-id="9ed98-119">Když je plánovaná objednávka potvrzena, přesune se do částí objednávek příslušného modulu.</span><span class="sxs-lookup"><span data-stu-id="9ed98-119">When a planned order is firmed, it's moved to the orders section of the relevant module.</span></span>

<span data-ttu-id="9ed98-120">Na stránce **plánované objednávky** můžete vybrat dvě možnosti potvrzení:</span><span class="sxs-lookup"><span data-stu-id="9ed98-120">You can select two firming options from the **Planned orders** page:</span></span>

-   <span data-ttu-id="9ed98-121">**Pevné** – tímto potvrdíte jednu nebo více vybraných plánovaných objednávek.</span><span class="sxs-lookup"><span data-stu-id="9ed98-121">**Firm** – This will firm one or multiple selected planned orders.</span></span>
-   <span data-ttu-id="9ed98-122">**Potvrdit vše** – Tato akce potvrdí všech plánovaných objednávek ve filtru.</span><span class="sxs-lookup"><span data-stu-id="9ed98-122">**Firm all** – This will firm all planned orders in the filter.</span></span> <span data-ttu-id="9ed98-123">Když použijete možnost **Potvrdit vše**, nemusíte vybírat plánovanou objednávku, všechny plánované objednávky v rámci tohoto filtru budou potvrzeny.</span><span class="sxs-lookup"><span data-stu-id="9ed98-123">Using **Firm all** you don’t have to select the planned order, all planned orders within the filter will be firmed.</span></span> <span data-ttu-id="9ed98-124">Tato možnost může být užitečná v případě, že potvrzujete vysoký počet plánovaných objednávek.</span><span class="sxs-lookup"><span data-stu-id="9ed98-124">This option can be useful if you are firming a high number of planned orders.</span></span>

> [!NOTE]
> <span data-ttu-id="9ed98-125">Můžete sledovat plánovanou objednávku, která byla potvrzena v **Historii potvrzení** v části **Formulář plánované objednávky > Zobrazení > Historie potvrzení**.</span><span class="sxs-lookup"><span data-stu-id="9ed98-125">You can track a planned order that was firmed from **Firming history** under **Planned orders form > View > Firming history**.</span></span>

## <a name="parallelize-firming"></a><span data-ttu-id="9ed98-126">Paralelizovat potvrzení</span><span class="sxs-lookup"><span data-stu-id="9ed98-126">Parallelize firming</span></span>
<span data-ttu-id="9ed98-127">Pokud plánujete potvrdit více objednávek najednou, může paralelní provedení zlepšit dobu provádění nebo výkon.</span><span class="sxs-lookup"><span data-stu-id="9ed98-127">If you are planning to firm many orders at the same time, parallelizing the run can improve the run time or performance.</span></span> <span data-ttu-id="9ed98-128">Tato možnost je k dispozici při potvrzování více plánovaných objednávek pomocí možnosti **Potvrdit** nebo **Potvrdit vše**.</span><span class="sxs-lookup"><span data-stu-id="9ed98-128">This option is available when firming multiple planned orders with either **Firm** or **Firm all**.</span></span> <span data-ttu-id="9ed98-129">K dispozici jsou následující parametry:</span><span class="sxs-lookup"><span data-stu-id="9ed98-129">The following parameters are available:</span></span>

-   <span data-ttu-id="9ed98-130">**Paralelizovat potvrzení** – Pokud je nastaveno **Ano**, proces potvrzování bude paralelizován s počtem podprocesů definovaných v poli **Počet podprocesů**.</span><span class="sxs-lookup"><span data-stu-id="9ed98-130">**Parallelize firming** – If **Yes**, the firming process will be parallelized with the number of threads defined in **Number of threads**.</span></span>
-   <span data-ttu-id="9ed98-131">**Počet podprocesů** – řídí počet podprocesů použitých k parallelize procesu potvrzování.</span><span class="sxs-lookup"><span data-stu-id="9ed98-131">**Number of threads** – Controls the number of threads used to parallelize the firming process.</span></span> <span data-ttu-id="9ed98-132">Parametr se zobrazuje pouze tehdy, je-li volba **Paralelizovat potvrzení** nastavena na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="9ed98-132">The parameter is only shown when **Parallelize firming** is set to **Yes**.</span></span>

> [!NOTE]
> <span data-ttu-id="9ed98-133">Možnost pro **Paralelizovat potvrzení** je zobrazena pouze v případě, že jste vybrali více než jednu plánovanou objednávku pro potvrzení.</span><span class="sxs-lookup"><span data-stu-id="9ed98-133">The option for **Parallelize firming** is only shown when you have more than one planned order selected for firming.</span></span>

<a name="additional-resources"></a><span data-ttu-id="9ed98-134">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="9ed98-134">Additional resources</span></span>
--------

[<span data-ttu-id="9ed98-135">Přehled hlavních plánů</span><span class="sxs-lookup"><span data-stu-id="9ed98-135">Master plans overview</span></span>](master-plans.md)



