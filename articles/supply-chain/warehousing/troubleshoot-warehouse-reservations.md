---
title: Odstraňování problémů s rezervacemi v řízení skladu
description: Toto téma popisuje, jak vyřešit běžné problémy, s nimiž se můžete setkat při práci s rezervacemi skladu v Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: d0d73396772ed9e8397797d6685fb550d911303b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828099"
---
# <a name="troubleshoot-reservations-in-warehouse-management"></a><span data-ttu-id="cdc5a-103">Odstraňování problémů s rezervacemi v řízení skladu</span><span class="sxs-lookup"><span data-stu-id="cdc5a-103">Troubleshoot reservations in warehouse management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cdc5a-104">Toto téma popisuje, jak vyřešit běžné problémy, s nimiž se můžete setkat při práci s rezervacemi skladu v Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="cdc5a-104">This topic describes how to fix common issues that you might encounter while you work with warehouse reservations in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="cdc5a-105">Témata související s registracemi čísla dávky a sériového čísla najdete v tématu [Odstraňování problémů s hierarchiemi dávkových a sériových rezervací ve skladu](troubleshoot-warehouse-batch-and-serial-reservation-hierarchies.md).</span><span class="sxs-lookup"><span data-stu-id="cdc5a-105">For topics that are related to batch and serial number registrations, see [Troubleshoot warehouse batch and serial reservation hierarchies](troubleshoot-warehouse-batch-and-serial-reservation-hierarchies.md).</span></span>

## <a name="i-receive-the-following-error-message-reservations-cannot-be-removed-because-there-is-work-created-which-relies-on-the-reservations"></a><span data-ttu-id="cdc5a-106">Zobrazuje se mi následující chybová zpráva: „Nelze odebrat rezervace, protože existuje práce, která závisí na rezervacích."</span><span class="sxs-lookup"><span data-stu-id="cdc5a-106">I receive the following error message: "Reservations cannot be removed because there is work created which relies on the reservations."</span></span>

### <a name="issue-description"></a><span data-ttu-id="cdc5a-107">Popis problému</span><span class="sxs-lookup"><span data-stu-id="cdc5a-107">Issue description</span></span>

<span data-ttu-id="cdc5a-108">Na řádku prodeje nemůžete zrušit rezervaci zásob, protože proti řádku je otevřená práce.</span><span class="sxs-lookup"><span data-stu-id="cdc5a-108">You can't unreserve inventory on a sales line, because there is open work against the line.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="cdc5a-109">Řešení problému</span><span class="sxs-lookup"><span data-stu-id="cdc5a-109">Issue resolution</span></span>

<span data-ttu-id="cdc5a-110">Prozkoumejte, zda existuje práce skupiny balení, která přepravuje položku z balicí stanice na jiné místo (např *Nákladová brána*).</span><span class="sxs-lookup"><span data-stu-id="cdc5a-110">Investigate whether open packing group work exists to bring the item from a packing station to another location (such as *Baydoor*).</span></span> <span data-ttu-id="cdc5a-111">Zkontrolujte záznamy na stránkách **Protokol historie vytvoření práce** a **Podrobnosti o práci**, abyste zjistili, co fyzicky rezervuje zásoby, a poté dokončete nebo odstraňte práci, abyste rezervaci uvolnili.</span><span class="sxs-lookup"><span data-stu-id="cdc5a-111">Review the records on the **Work creation history log** and **Work details** pages to determine what is physically reserving the inventory, and then complete or delete the work to free up the reservation.</span></span>

## <a name="i-receive-the-following-error-message-inventory-quantity--1-could-not-be-updated-due-to-insufficient-inventory-transactions-for-item-2"></a><span data-ttu-id="cdc5a-112">Zobrazuje se následující chybová zpráva: „Množství zásob -%1 nelze aktualizovat z důvodu nedostatečných transakcí zásob pro položku %2...."</span><span class="sxs-lookup"><span data-stu-id="cdc5a-112">I receive the following error message: "Inventory quantity -%1 could not be updated due to insufficient inventory transactions for item %2...."</span></span>

### <a name="issue-description"></a><span data-ttu-id="cdc5a-113">Popis problému</span><span class="sxs-lookup"><span data-stu-id="cdc5a-113">Issue description</span></span>

<span data-ttu-id="cdc5a-114">K tomuto problému může dojít, pokud systém nemůže aktualizovat množství zásob, protože není k dispozici dostatek transakcí zásob, které mají zadané dimenze.</span><span class="sxs-lookup"><span data-stu-id="cdc5a-114">This issue can occur if the system can't update an inventory quantity because there aren't enough inventory transactions that have the specified dimensions.</span></span> <span data-ttu-id="cdc5a-115">Následuje úplné znění chybové zprávy:</span><span class="sxs-lookup"><span data-stu-id="cdc5a-115">Here is the full text of the full error message:</span></span>

> <span data-ttu-id="cdc5a-116">Množství zásob -%1 nelze aktualizovat z důvodu nedostatečných transakcí zásob pro položku %2 s rozměry Velikost =%3, Barva =%4, Dodatky =%5, Místo =%6, Sklad =%7, Umístění =%8, Stav zásob = K dispozici, Registrační značka =%9, Číslo šarže =%10 pro referenční ID %11 na ID šarže %12.</span><span class="sxs-lookup"><span data-stu-id="cdc5a-116">Inventory quantity -%1 could not be updated due to insufficient inventory transactions for item %2 with dimensions Size=%3, Color=%4, Additions=%5, Site=%6, Warehouse=%7, Location=%8, Inventory status=Available, License plate=%9, Batch number=%10 for reference ID %11 on Lot ID %12.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="cdc5a-117">Řešení problému</span><span class="sxs-lookup"><span data-stu-id="cdc5a-117">Issue resolution</span></span>

<span data-ttu-id="cdc5a-118">Ujistěte se, že žádné transakce zásob fyzicky nerezervují množství.</span><span class="sxs-lookup"><span data-stu-id="cdc5a-118">Make sure that no inventory transactions are physically reserving the quantity.</span></span> <span data-ttu-id="cdc5a-119">Například tyto transakce mohou otevřít objednávky kvality, záznamy blokující zásoby nebo výstupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="cdc5a-119">For example, these transactions might open quality orders, inventory blocking records, or output orders.</span></span>

## <a name="i-receive-the-following-error-message-physical-on-handcannot-be-reserved-because-only-000-are-available-in-the-inventory"></a><span data-ttu-id="cdc5a-120">Zobrazuje se následující chybová zpráva: „Fyzicky na skladě ... nelze rezervovat, protože v zásobách je k dispozici pouze 0,00.“</span><span class="sxs-lookup"><span data-stu-id="cdc5a-120">I receive the following error message: "Physical on-hand...cannot be reserved because only 0.00 are available in the inventory."</span></span>

### <a name="issue-description"></a><span data-ttu-id="cdc5a-121">Popis problému</span><span class="sxs-lookup"><span data-stu-id="cdc5a-121">Issue description</span></span>

<span data-ttu-id="cdc5a-122">K tomuto problému může dojít, pokud systém nemůže aktualizovat množství zásob, protože není k dispozici dostatek transakcí zásob, které mají zadané dimenze.</span><span class="sxs-lookup"><span data-stu-id="cdc5a-122">This issue can occur if the system can't update an inventory quantity because there aren't enough inventory transactions that have the specified dimensions.</span></span> <span data-ttu-id="cdc5a-123">Následuje úplné znění chybové zprávy:</span><span class="sxs-lookup"><span data-stu-id="cdc5a-123">Here is the full text of the full error message:</span></span>

> <span data-ttu-id="cdc5a-124">Fyzicky na skladě Místo =%1, Sklad =%2, Stav zásob = Dostupné, Číslo šarže =%3, Majitel =%4: %5 nelze rezervovat, protože v zásobách je k dispozici pouze 0,00.</span><span class="sxs-lookup"><span data-stu-id="cdc5a-124">Physical on-hand Site=%1, Warehouse=%2, Inventory status=Available, Batch number=%3, Owner=%4: %5 cannot be reserved because only 0.00 are available in the inventory.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="cdc5a-125">Řešení problému</span><span class="sxs-lookup"><span data-stu-id="cdc5a-125">Issue resolution</span></span>

<span data-ttu-id="cdc5a-126">Tento problém je pravděpodobně způsoben otevřenou prací.</span><span class="sxs-lookup"><span data-stu-id="cdc5a-126">This issue is probably caused by open work.</span></span> <span data-ttu-id="cdc5a-127">Buď dokončete práci, nebo přijměte bez vytvoření práce.</span><span class="sxs-lookup"><span data-stu-id="cdc5a-127">Either complete the work or receive without work creation.</span></span> <span data-ttu-id="cdc5a-128">Ujistěte se, že žádné transakce zásob fyzicky nerezervují množství.</span><span class="sxs-lookup"><span data-stu-id="cdc5a-128">Make sure that no inventory transactions are physically reserving the quantity.</span></span> <span data-ttu-id="cdc5a-129">Například tyto transakce mohou být otevřené objednávky kvality, záznamy blokující zásoby nebo výstupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="cdc5a-129">For example, these transactions might be open quality orders, inventory blocking records, or output orders.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
