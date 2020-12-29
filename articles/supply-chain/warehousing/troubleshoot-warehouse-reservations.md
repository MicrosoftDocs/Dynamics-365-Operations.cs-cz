---
title: Odstraňování problémů s rezervacemi v řízení skladu
description: Toto téma popisuje, jak vyřešit běžné problémy, s nimiž se můžete setkat při práci s rezervacemi skladu v Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 6151797001b1ccdb7e371c70b90c304a5ab422d8
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645111"
---
# <a name="troubleshoot-reservations-in-warehouse-management"></a><span data-ttu-id="65d27-103">Odstraňování problémů s rezervacemi v řízení skladu</span><span class="sxs-lookup"><span data-stu-id="65d27-103">Troubleshoot reservations in warehouse management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="65d27-104">Toto téma popisuje, jak vyřešit běžné problémy, s nimiž se můžete setkat při práci s rezervacemi skladu v Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="65d27-104">This topic describes how to fix common issues that you might encounter while you work with warehouse reservations in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-reservations-cannot-be-removed-because-there-is-work-created-which-relies-on-the-reservations"></a><span data-ttu-id="65d27-105">Zobrazuje se mi následující chybová zpráva: „Nelze odebrat rezervace, protože existuje práce, která závisí na rezervacích."</span><span class="sxs-lookup"><span data-stu-id="65d27-105">I receive the following error message: "Reservations cannot be removed because there is work created which relies on the reservations."</span></span>

### <a name="issue-description"></a><span data-ttu-id="65d27-106">Popis problému</span><span class="sxs-lookup"><span data-stu-id="65d27-106">Issue description</span></span>

<span data-ttu-id="65d27-107">Na řádku prodeje nemůžete zrušit rezervaci zásob, protože proti řádku je otevřená práce.</span><span class="sxs-lookup"><span data-stu-id="65d27-107">You can't unreserve inventory on a sales line, because there is open work against the line.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="65d27-108">Řešení problému</span><span class="sxs-lookup"><span data-stu-id="65d27-108">Issue resolution</span></span>

<span data-ttu-id="65d27-109">Prozkoumejte, zda existuje práce skupiny balení, která přepravuje položku z balicí stanice na jiné místo (např *Nákladová brána*).</span><span class="sxs-lookup"><span data-stu-id="65d27-109">Investigate whether open packing group work exists to bring the item from a packing station to another location (such as *Baydoor*).</span></span> <span data-ttu-id="65d27-110">Zkontrolujte záznamy na stránkách **Protokol historie vytvoření práce** a **Podrobnosti o práci**, abyste zjistili, co fyzicky rezervuje zásoby, a poté dokončete nebo odstraňte práci, abyste rezervaci uvolnili.</span><span class="sxs-lookup"><span data-stu-id="65d27-110">Review the records on the **Work creation history log** and **Work details** pages to determine what is physically reserving the inventory, and then complete or delete the work to free up the reservation.</span></span>

## <a name="i-receive-the-following-error-message-inventory-quantity--1-could-not-be-updated-due-to-insufficient-inventory-transactions-for-item-2"></a><span data-ttu-id="65d27-111">Zobrazuje se následující chybová zpráva: „Množství zásob -%1 nelze aktualizovat z důvodu nedostatečných transakcí zásob pro položku %2...."</span><span class="sxs-lookup"><span data-stu-id="65d27-111">I receive the following error message: "Inventory quantity -%1 could not be updated due to insufficient inventory transactions for item %2...."</span></span>

### <a name="issue-description"></a><span data-ttu-id="65d27-112">Popis problému</span><span class="sxs-lookup"><span data-stu-id="65d27-112">Issue description</span></span>

<span data-ttu-id="65d27-113">K tomuto problému může dojít, pokud systém nemůže aktualizovat množství zásob, protože není k dispozici dostatek transakcí zásob, které mají zadané dimenze.</span><span class="sxs-lookup"><span data-stu-id="65d27-113">This issue can occur if the system can't update an inventory quantity because there aren't enough inventory transactions that have the specified dimensions.</span></span> <span data-ttu-id="65d27-114">Následuje úplné znění chybové zprávy:</span><span class="sxs-lookup"><span data-stu-id="65d27-114">Here is the full text of the full error message:</span></span>

> <span data-ttu-id="65d27-115">Množství zásob -%1 nelze aktualizovat z důvodu nedostatečných transakcí zásob pro položku %2 s rozměry Velikost =%3, Barva =%4, Dodatky =%5, Místo =%6, Sklad =%7, Umístění =%8, Stav zásob = K dispozici, Registrační značka =%9, Číslo šarže =%10 pro referenční ID %11 na ID šarže %12.</span><span class="sxs-lookup"><span data-stu-id="65d27-115">Inventory quantity -%1 could not be updated due to insufficient inventory transactions for item %2 with dimensions Size=%3, Color=%4, Additions=%5, Site=%6, Warehouse=%7, Location=%8, Inventory status=Available, License plate=%9, Batch number=%10 for reference ID %11 on Lot ID %12.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="65d27-116">Řešení problému</span><span class="sxs-lookup"><span data-stu-id="65d27-116">Issue resolution</span></span>

<span data-ttu-id="65d27-117">Ujistěte se, že žádné transakce zásob fyzicky nerezervují množství.</span><span class="sxs-lookup"><span data-stu-id="65d27-117">Make sure that no inventory transactions are physically reserving the quantity.</span></span> <span data-ttu-id="65d27-118">Například tyto transakce mohou otevřít objednávky kvality, záznamy blokující zásoby nebo výstupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="65d27-118">For example, these transactions might open quality orders, inventory blocking records, or output orders.</span></span>

## <a name="i-receive-the-following-error-message-physical-on-handcannot-be-reserved-because-only-000-are-available-in-the-inventory"></a><span data-ttu-id="65d27-119">Zobrazuje se následující chybová zpráva: „Fyzicky na skladě ... nelze rezervovat, protože v zásobách je k dispozici pouze 0,00.“</span><span class="sxs-lookup"><span data-stu-id="65d27-119">I receive the following error message: "Physical on-hand...cannot be reserved because only 0.00 are available in the inventory."</span></span>

### <a name="issue-description"></a><span data-ttu-id="65d27-120">Popis problému</span><span class="sxs-lookup"><span data-stu-id="65d27-120">Issue description</span></span>

<span data-ttu-id="65d27-121">K tomuto problému může dojít, pokud systém nemůže aktualizovat množství zásob, protože není k dispozici dostatek transakcí zásob, které mají zadané dimenze.</span><span class="sxs-lookup"><span data-stu-id="65d27-121">This issue can occur if the system can't update an inventory quantity because there aren't enough inventory transactions that have the specified dimensions.</span></span> <span data-ttu-id="65d27-122">Následuje úplné znění chybové zprávy:</span><span class="sxs-lookup"><span data-stu-id="65d27-122">Here is the full text of the full error message:</span></span>

> <span data-ttu-id="65d27-123">Fyzicky na skladě Místo =%1, Sklad =%2, Stav zásob = Dostupné, Číslo šarže =%3, Majitel =%4: %5 nelze rezervovat, protože v zásobách je k dispozici pouze 0,00.</span><span class="sxs-lookup"><span data-stu-id="65d27-123">Physical on-hand Site=%1, Warehouse=%2, Inventory status=Available, Batch number=%3, Owner=%4: %5 cannot be reserved because only 0.00 are available in the inventory.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="65d27-124">Řešení problému</span><span class="sxs-lookup"><span data-stu-id="65d27-124">Issue resolution</span></span>

<span data-ttu-id="65d27-125">Tento problém je pravděpodobně způsoben otevřenou prací.</span><span class="sxs-lookup"><span data-stu-id="65d27-125">This issue is probably caused by open work.</span></span> <span data-ttu-id="65d27-126">Buď dokončete práci, nebo přijměte bez vytvoření práce.</span><span class="sxs-lookup"><span data-stu-id="65d27-126">Either complete the work or receive without work creation.</span></span> <span data-ttu-id="65d27-127">Ujistěte se, že žádné transakce zásob fyzicky nerezervují množství.</span><span class="sxs-lookup"><span data-stu-id="65d27-127">Make sure that no inventory transactions are physically reserving the quantity.</span></span> <span data-ttu-id="65d27-128">Například tyto transakce mohou být otevřené objednávky kvality, záznamy blokující zásoby nebo výstupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="65d27-128">For example, these transactions might be open quality orders, inventory blocking records, or output orders.</span></span>

## <a name="i-receive-the-following-error-message-to-be-assigned-to-wave-load-lines-must-specify-the-dimensions-above-the-location-to-assign-these-dimensions-reserve-and-recreate-the-load-line"></a><span data-ttu-id="65d27-129">Zobrazuje se následující chybová zpráva: „Aby bylo možné přiřadit vlně, musí řádky nákladu určit rozměry nad umístěním.</span><span class="sxs-lookup"><span data-stu-id="65d27-129">I receive the following error message: "To be assigned to wave, load lines must specify the dimensions above the location.</span></span> <span data-ttu-id="65d27-130">Chcete-li přiřadit tyto rozměry, zarezervujte a znovu vytvořte řádek nákladu. “</span><span class="sxs-lookup"><span data-stu-id="65d27-130">To assign these dimensions, reserve and recreate the load line."</span></span>

### <a name="issue-description"></a><span data-ttu-id="65d27-131">Popis problému</span><span class="sxs-lookup"><span data-stu-id="65d27-131">Issue description</span></span>

<span data-ttu-id="65d27-132">Pokud používáte položku, která má hierarchii rezervace "dávka nad" (s dimenzí **Číslo šarže** umístěnou *nad* dimenzí **Umístění**), příkaz **Uvolnit do skladu** na stránce **Pracovní plocha plánování nákladu** pro částečné množství nefunguje.</span><span class="sxs-lookup"><span data-stu-id="65d27-132">When you use an item that has a "batch above" reservation hierarchy (with the **Batch number** dimension placed *above* the **Location** dimension), the **Release to warehouse** command on the **Load planning workbench** page for a partial quantity doesn't work.</span></span> <span data-ttu-id="65d27-133">Zobrazí se tato chybová zpráva a pro částečné množství se nevytvoří žádná práce.</span><span class="sxs-lookup"><span data-stu-id="65d27-133">You receive this error message, and no work is created for the partial quantity.</span></span>

<span data-ttu-id="65d27-134">Pokud však používáte položku, která má hierarchii rezervace "dávka pod" (s dimenzí **Číslo šarže** umístěnou *pod* dimenzí **Umístění**), můžete uvolnit náklad ze stránky **Pracovní plocha plánování nákladu** pro částečné množství.</span><span class="sxs-lookup"><span data-stu-id="65d27-134">However, if you use an item that has a "batch below" reservation hierarchy (with the **Batch number** dimension placed *below* the **Location** dimension), you can release a load from the **Load planning workbench** page for a partial quantity.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="65d27-135">Řešení problému</span><span class="sxs-lookup"><span data-stu-id="65d27-135">Issue resolution</span></span>

<span data-ttu-id="65d27-136">Toto chování je záměrné.</span><span class="sxs-lookup"><span data-stu-id="65d27-136">This behavior is by design.</span></span> <span data-ttu-id="65d27-137">Pokud vložíte dimenzi nad dimenzi **Umístění** v hierarchii rezervací, musí být zadána před uvolněním do skladu.</span><span class="sxs-lookup"><span data-stu-id="65d27-137">If you put a dimension above the **Location** dimension in the reservation hierarchy, it must be specified before the release to the warehouse.</span></span> <span data-ttu-id="65d27-138">Společnost Microsoft vyhodnotila tento problém a zjistila, že se jedná o omezení funkcí během uvolnění do skladu z pracovní plochy plánování nákladu.</span><span class="sxs-lookup"><span data-stu-id="65d27-138">Microsoft has evaluated this issue and has determined that it's a feature limitation during releases to the warehouse from the load planning workbench.</span></span> <span data-ttu-id="65d27-139">Částečná množství nelze uvolnit, pokud je není apecifikována jedna nebo více dimenzí nad **Umístěním**.</span><span class="sxs-lookup"><span data-stu-id="65d27-139">Partial quantities can't be released if one or more dimensions above **Location** aren't specified.</span></span>

<span data-ttu-id="65d27-140">Další informace viz [Flexibilní zásada rezervace dimenze na úrovni skladu](flexible-warehouse-level-dimension-reservation.md).</span><span class="sxs-lookup"><span data-stu-id="65d27-140">For more information, see [Flexible warehouse-level dimension reservation policy](flexible-warehouse-level-dimension-reservation.md).</span></span>
