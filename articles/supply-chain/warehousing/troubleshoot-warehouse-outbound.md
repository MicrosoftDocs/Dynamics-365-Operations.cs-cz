---
title: Řešení potíží s odchozími skladovými operacemi
description: Toto téma popisuje, jak vyřešit běžné problémy, s nimiž se můžete setkat při práci s odchozími skladovými operacemi v Microsoft Dynamics 365 Supply Chain Management.
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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 165ac8145ad75c2c6619764b9abe855b9d32eb46
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993971"
---
# <a name="troubleshoot-outbound-warehouse-operations"></a><span data-ttu-id="bc5ef-103">Řešení potíží s odchozími skladovými operacemi</span><span class="sxs-lookup"><span data-stu-id="bc5ef-103">Troubleshoot outbound warehouse operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bc5ef-104">Toto téma popisuje, jak vyřešit běžné problémy, s nimiž se můžete setkat při práci s odchozími skladovými operacemi v Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="bc5ef-104">This topic describes how to fix common issues that you might encounter while you work with outbound warehouse operations in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-sales-order-could-not-be-released"></a><span data-ttu-id="bc5ef-105">Zobrazí se následující chybová zpráva: „Prodejní objednávku nelze uvolnit.“</span><span class="sxs-lookup"><span data-stu-id="bc5ef-105">I receive the following error message: "Sales order could not be released."</span></span>

### <a name="issue-description"></a><span data-ttu-id="bc5ef-106">Popis problému</span><span class="sxs-lookup"><span data-stu-id="bc5ef-106">Issue description</span></span>

<span data-ttu-id="bc5ef-107">K tomuto problému může dojít z několika důvodů.</span><span class="sxs-lookup"><span data-stu-id="bc5ef-107">This issue can occur for several reasons.</span></span> <span data-ttu-id="bc5ef-108">Například je objednávka blokována správou kreditů a není možné vytvářet žádné zásilky, dokud nezadáte platnou poštovní adresu pro všechny prodejní řádky spojené s prodejní objednávkou.</span><span class="sxs-lookup"><span data-stu-id="bc5ef-108">For example, the order is on credit management hold, and no shipments can be created until a valid postal address is entered for all sales lines that are associated with a sales order.</span></span> <span data-ttu-id="bc5ef-109">Alternativně existuje blokování objednávky, které musí být vyřešeno, než bude možné objednávku uvolnit do skladu.</span><span class="sxs-lookup"><span data-stu-id="bc5ef-109">Alternatively, there is an order hold that must be addressed before the order can be released to the warehouse.</span></span> <span data-ttu-id="bc5ef-110">Toto pozastavení může být specifické pro objednávku nebo může být na zákaznickém účtu.</span><span class="sxs-lookup"><span data-stu-id="bc5ef-110">This hold might be order-specific, or it might be on the customer account.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="bc5ef-111">Řešení problému</span><span class="sxs-lookup"><span data-stu-id="bc5ef-111">Issue resolution</span></span>

<span data-ttu-id="bc5ef-112">Přidejte nebo aktualizujte adresu na řádcích prodejní objednávky a objednávky a poté objednávku uvolněte do skladu.</span><span class="sxs-lookup"><span data-stu-id="bc5ef-112">Add or update the address on the sales order and order lines, and then release the order to the warehouse.</span></span> <span data-ttu-id="bc5ef-113">Objednávky lze do skladu uvolnit, pouze pokud mají platnou dodací adresu (podle nastavení formátu adresy v modulu **Správa organizace**).</span><span class="sxs-lookup"><span data-stu-id="bc5ef-113">Orders can be released to the warehouse only if they have a valid delivery address (per the address format setup in the **Organization administration** module).</span></span>

<span data-ttu-id="bc5ef-114">Prozkoumejte pozastavení objednávky a vyřešte problémy.</span><span class="sxs-lookup"><span data-stu-id="bc5ef-114">Investigate the order hold, and address the issues.</span></span> <span data-ttu-id="bc5ef-115">Poté odeberte blokování objednávky nebo zákazníka a uvolněte objednávku do skladu.</span><span class="sxs-lookup"><span data-stu-id="bc5ef-115">Then remove the hold from the order or customer, and release the order to the warehouse.</span></span>

## <a name="i-receive-the-following-message-the-shipment-for-load-1-has-been-confirmed-however-no-lines-are-posted"></a><span data-ttu-id="bc5ef-116">Zobrazuje se následující zpráva: „Zásilka s nákladem 1% byla potvrzena.“</span><span class="sxs-lookup"><span data-stu-id="bc5ef-116">I receive the following message: "The shipment for load 1% has been confirmed."</span></span> <span data-ttu-id="bc5ef-117">Žádné řádky však nejsou vystaveny.</span><span class="sxs-lookup"><span data-stu-id="bc5ef-117">However, no lines are posted.</span></span>

### <a name="issue-description"></a><span data-ttu-id="bc5ef-118">Popis problému</span><span class="sxs-lookup"><span data-stu-id="bc5ef-118">Issue description</span></span>

<span data-ttu-id="bc5ef-119">Zásilka s nákladem byla potvrzena, ale k dalšímu odeslání nedošlo.</span><span class="sxs-lookup"><span data-stu-id="bc5ef-119">A shipment on a load was confirmed, but no further posting occurred.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="bc5ef-120">Řešení problému</span><span class="sxs-lookup"><span data-stu-id="bc5ef-120">Issue resolution</span></span>

<span data-ttu-id="bc5ef-121">Potvrzení zásilky nemá vliv na odeslání.</span><span class="sxs-lookup"><span data-stu-id="bc5ef-121">Shipment confirmation doesn't affect posting.</span></span> <span data-ttu-id="bc5ef-122">Pouze aktualizuje stav zásilky a nákladu.</span><span class="sxs-lookup"><span data-stu-id="bc5ef-122">It just updates the shipment and load status.</span></span> <span data-ttu-id="bc5ef-123">Vystavení musí proběhnout v samostatném procesu.</span><span class="sxs-lookup"><span data-stu-id="bc5ef-123">Posting must occur in a separate process.</span></span>

## <a name="i-receive-the-following-error-message-direct-delivery-is-not-able-to-process-for-warehouse-1-as-it-has-warehouse-management-enabled-please-specify-another-warehouse-that-is-not-enabled-for-warehouse-management"></a><span data-ttu-id="bc5ef-124">Zobrazuje se následující chybová zpráva: „Přímé doručení není možné zpracovat pro sklad 1%, protože má povolenou správu skladu.</span><span class="sxs-lookup"><span data-stu-id="bc5ef-124">I receive the following error message: "Direct delivery is not able to process for warehouse 1% as it has warehouse management enabled.</span></span> <span data-ttu-id="bc5ef-125">Zadejte prosím jiný sklad, který nemá povolenou správu skladu. “</span><span class="sxs-lookup"><span data-stu-id="bc5ef-125">Please specify another warehouse that is not enabled for warehouse management."</span></span>

### <a name="issue-description"></a><span data-ttu-id="bc5ef-126">Popis problému</span><span class="sxs-lookup"><span data-stu-id="bc5ef-126">Issue description</span></span>

<span data-ttu-id="bc5ef-127">Položka je přidána na prodejní řádek pro přímé dodání ze skladu, který je povolen pro správu skladu (WMS).</span><span class="sxs-lookup"><span data-stu-id="bc5ef-127">An item is added to a sales line for direct delivery from a warehouse that is enabled for warehouse management (WMS).</span></span> <span data-ttu-id="bc5ef-128">Tato chybová zpráva se zobrazí při aktualizaci řádku prodeje.</span><span class="sxs-lookup"><span data-stu-id="bc5ef-128">You receive this error message when the sales line is updated.</span></span> 

### <a name="issue-resolution"></a><span data-ttu-id="bc5ef-129">Řešení problému</span><span class="sxs-lookup"><span data-stu-id="bc5ef-129">Issue resolution</span></span>

<span data-ttu-id="bc5ef-130">Společnost Microsoft vyhodnotila tento problém a zjistila, že jde o omezení funkcí.</span><span class="sxs-lookup"><span data-stu-id="bc5ef-130">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="bc5ef-131">V současné době WMS nepodporuje přímé doručování.</span><span class="sxs-lookup"><span data-stu-id="bc5ef-131">Currently, WMS doesn't support direct delivery.</span></span> <span data-ttu-id="bc5ef-132">Chcete-li tedy použít přímé doručení, musíte vybrat položku a sklad, který nespadá do WMS.</span><span class="sxs-lookup"><span data-stu-id="bc5ef-132">Therefore, to use direct delivery, you must select a non-WMS item and warehouse.</span></span>
