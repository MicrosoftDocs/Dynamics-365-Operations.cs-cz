---
title: Karanténní příkazy
description: Toto téma popisuje použití karanténních příkazů k blokování zásob.
author: perlynne
manager: tfehr
ms.date: 11/02/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventLocation, InventModelGroup, InventQuarantineOrder, InventQuarantineParmEnd, InventQuarantineParmReportFinished, InventQuarantineParmStartUp, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 30021
ms.assetid: d5047727-653c-49da-b489-6fd3fe50445e
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 25ba4aa92d968f4dfb0dc23b1ac459cda2d52b61
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4424087"
---
# <a name="quarantine-orders"></a><span data-ttu-id="fe49e-103">Karanténní příkazy</span><span class="sxs-lookup"><span data-stu-id="fe49e-103">Quarantine orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fe49e-104">Toto téma popisuje použití karanténních příkazů k blokování zásob.</span><span class="sxs-lookup"><span data-stu-id="fe49e-104">This topic describes how quarantine orders are used to block inventory.</span></span>

<span data-ttu-id="fe49e-105">Karanténní příkazy lze použít k blokování zásob.</span><span class="sxs-lookup"><span data-stu-id="fe49e-105">Quarantine orders can be used to block inventory.</span></span> <span data-ttu-id="fe49e-106">Můžete například chtít umístit do karantény položky z důvodů kontroly kvality.</span><span class="sxs-lookup"><span data-stu-id="fe49e-106">For example, you might want to quarantine items for quality control reasons.</span></span> <span data-ttu-id="fe49e-107">Sklad, který byl umístěn do karantény, je převeden do karanténního skladu.</span><span class="sxs-lookup"><span data-stu-id="fe49e-107">Inventory that has been quarantined is transferred to a quarantine warehouse.</span></span> <span data-ttu-id="fe49e-108">**Poznámka:** Pokud používáte rozšířené procesy správy skladu (v modulu Řízení skladu), zpracování karanténní objednávky se používá pouze pro vrácení prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="fe49e-108">**Note:** If you're using advanced warehouse management processes (in Warehouse management), quarantine order processing is used only for return sales orders.</span></span>

## <a name="quarantine-on-hand-inventory-items"></a><span data-ttu-id="fe49e-109">Karanténní zásoby položek na skladě</span><span class="sxs-lookup"><span data-stu-id="fe49e-109">Quarantine on-hand inventory items</span></span>
<span data-ttu-id="fe49e-110">Při umístění položek do karantény můžete vytvořit karanténní příkazy ručně nebo systém nastavit tak, aby vytvářel karanténní příkazy automaticky při zpracování příchozích.</span><span class="sxs-lookup"><span data-stu-id="fe49e-110">When you quarantine items, you can either create the quarantine orders manually or set up the system to create the quarantine orders automatically during inbound processing.</span></span> <span data-ttu-id="fe49e-111">Pokud chcete automaticky vytvořit karanténní příkazy, zaškrtněte možnost **Řízení karantény** na kartě **Zásady zásob** na stránce **Skupiny modelů položek**.</span><span class="sxs-lookup"><span data-stu-id="fe49e-111">To create quarantine orders automatically, select the **Quarantine management** option on the **Inventory policies** tab on the **Item model groups** page.</span></span> <span data-ttu-id="fe49e-112">Je nutné také určit výchozí karanténní sklad v poli **Karanténní sklad** pro přijímací sklady.</span><span class="sxs-lookup"><span data-stu-id="fe49e-112">You must also specify a default quarantine warehouse in the **Quarantine warehouse** field for the receiving warehouses.</span></span> <span data-ttu-id="fe49e-113">Když jsou zásoby fyzicky na skladě zaznamenány v nákupní objednávce nebo výrobní zakázce, položky umístěné do karantény jsou automaticky přesunuty do karanténního skladu v aplikaci Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="fe49e-113">When the physically on-hand inventory is recorded in a purchase order or production order, quarantined items are automatically moved to a quarantine warehouse in Supply Chain Management.</span></span> <span data-ttu-id="fe49e-114">K tomuto pohybu dochází, pokud se změní stav karanténního příkazu na **Zahájeno**.</span><span class="sxs-lookup"><span data-stu-id="fe49e-114">This movement occurs because the status of the quarantine order is changed to **Started**.</span></span> <span data-ttu-id="fe49e-115">Při ručním vytváření karanténních příkazů, není požadováno, aby v přidružené skupině modelů položek položka byla nastavena pro řízení karantény.</span><span class="sxs-lookup"><span data-stu-id="fe49e-115">When you create quarantine orders manually, the item doesn't have to be set up for quarantine management in the associated item model group.</span></span> <span data-ttu-id="fe49e-116">Za tímto účelem je nutné zadat zásob na skladě, která mají být umístěny do karantény, a karanténní sklad, který má být použit.</span><span class="sxs-lookup"><span data-stu-id="fe49e-116">For this process, you must specify the on-hand inventory that should be quarantined and the quarantine warehouse that should be used.</span></span> <span data-ttu-id="fe49e-117">Můžete použít stavy karanténních příkazů pro usnadnění plánování procesu.</span><span class="sxs-lookup"><span data-stu-id="fe49e-117">You can use the quarantine order statuses to help plan the process.</span></span>

## <a name="quarantine-order-statuses"></a><span data-ttu-id="fe49e-118">Stavy karanténního příkazu</span><span class="sxs-lookup"><span data-stu-id="fe49e-118">Quarantine order statuses</span></span>
<span data-ttu-id="fe49e-119">Karanténní příkazy mohou mít tyto stavy:</span><span class="sxs-lookup"><span data-stu-id="fe49e-119">Quarantine orders can have the following statuses:</span></span>

-   <span data-ttu-id="fe49e-120">Vytvořeno</span><span class="sxs-lookup"><span data-stu-id="fe49e-120">Created</span></span>
-   <span data-ttu-id="fe49e-121">Zahájeno</span><span class="sxs-lookup"><span data-stu-id="fe49e-121">Started</span></span>
-   <span data-ttu-id="fe49e-122">Ohlášeno jako dokončené</span><span class="sxs-lookup"><span data-stu-id="fe49e-122">Reported as finished</span></span>
-   <span data-ttu-id="fe49e-123">Ukončeno</span><span class="sxs-lookup"><span data-stu-id="fe49e-123">Ended</span></span>

### <a name="created"></a><span data-ttu-id="fe49e-124">Vytvořeno</span><span class="sxs-lookup"><span data-stu-id="fe49e-124">Created</span></span>

<span data-ttu-id="fe49e-125">Jestliže byla ručně vytvořena karanténní objednávka, ale položka ještě není uložena do karanténního skladu, karanténní příkaz obdrží stav **Vytvořeno**.</span><span class="sxs-lookup"><span data-stu-id="fe49e-125">When a quarantine order has been created manually, but the item isn't yet in the quarantine warehouse, the quarantine order has a status of **Created**.</span></span> <span data-ttu-id="fe49e-126">Vygenerují se dvě skladové transakce.</span><span class="sxs-lookup"><span data-stu-id="fe49e-126">Two inventory transactions are generated.</span></span> <span data-ttu-id="fe49e-127">Jedna je transakce výdeje, která může mít stav **Na objednávce**, **Rezervované – fyzicky** nebo **Vyskladněno**.</span><span class="sxs-lookup"><span data-stu-id="fe49e-127">One transaction is an issue transaction that can have a status of **On order**, **Reserved physical**, or **Picked**.</span></span> <span data-ttu-id="fe49e-128">Druhá je příjmová transakce, která může mít v karanténním skladu stav **Objednáno** nebo **Registrováno**.</span><span class="sxs-lookup"><span data-stu-id="fe49e-128">The other transaction is a receipt transaction that can have a status of **Ordered** or **Registered** at the quarantine warehouse.</span></span> <span data-ttu-id="fe49e-129">Rezervaci, vyskladnění a aktualizaci registrace zásob můžete provádět pomocí obvyklých procesů.</span><span class="sxs-lookup"><span data-stu-id="fe49e-129">You can reserve, pick, and register updates to the inventory by using the usual processes.</span></span>

### <a name="started"></a><span data-ttu-id="fe49e-130">Zahájeno</span><span class="sxs-lookup"><span data-stu-id="fe49e-130">Started</span></span>

<span data-ttu-id="fe49e-131">Když je karanténní příkaz ve stavu **Zahájeno** jsou pak položky přesunuty z obyčejného skladu do karanténního skladu a vytvoří se dvě skladové transakce.</span><span class="sxs-lookup"><span data-stu-id="fe49e-131">When a quarantine order has a status of **Started**, the inventory is transferred from the regular warehouse to the quarantine warehouse, and two inventory transactions are generated.</span></span> <span data-ttu-id="fe49e-132">Jedna transakce se nachází ve stavu **Odečteno** a jiné transakce nachází ve stavu **Přijato**.</span><span class="sxs-lookup"><span data-stu-id="fe49e-132">One transaction has a status of **Deducted**, and the other transaction has a status of **Received**.</span></span> <span data-ttu-id="fe49e-133">Zároveň se vytvoří také dvě skladové transakce k zajištění zpětného převodu.</span><span class="sxs-lookup"><span data-stu-id="fe49e-133">At the same time, two inventory transactions are created to handle the return transfer.</span></span> <span data-ttu-id="fe49e-134">Tyto transakce nejsou datovány.</span><span class="sxs-lookup"><span data-stu-id="fe49e-134">These transactions aren't dated.</span></span> <span data-ttu-id="fe49e-135">Jedna transakce se nachází ve stavu **Rezervované – fyzicky** a jiné transakce nachází ve stavu **Objednáno**.</span><span class="sxs-lookup"><span data-stu-id="fe49e-135">One transaction has a status of **Reserved physical**, and the other transaction has a status of **Ordered**.</span></span>

### <a name="reported-as-finished"></a><span data-ttu-id="fe49e-136">Ohlášeno jako dokončené</span><span class="sxs-lookup"><span data-stu-id="fe49e-136">Reported as finished</span></span>

<span data-ttu-id="fe49e-137">Klepnutím na položku **Ohlásit jako dokončené** můžete ohlásit zahájený karanténní příkaz jako dokončený.</span><span class="sxs-lookup"><span data-stu-id="fe49e-137">By clicking **Report as finished**, you can report a started quarantine order as finished.</span></span> <span data-ttu-id="fe49e-138">Položka je uvolněna z karantény, ale ještě nebyla přesunuta zpět do běžného skladu.</span><span class="sxs-lookup"><span data-stu-id="fe49e-138">The item is released from quarantine but isn't yet moved back to the regular warehouse.</span></span> <span data-ttu-id="fe49e-139">Přesun zpět do běžného skladu je možné zpracovat pomocí deníku doručení položky, který může být inicializován během procesu Vykázat jako dokončené.</span><span class="sxs-lookup"><span data-stu-id="fe49e-139">The movement back to the regular warehouse can be processed via an Item arrival journal that can be initialized during the Report as finished process.</span></span>

### <a name="ended"></a><span data-ttu-id="fe49e-140">Ukončeno</span><span class="sxs-lookup"><span data-stu-id="fe49e-140">Ended</span></span>

<span data-ttu-id="fe49e-141">Když je karanténní příkaz ukončen, je položka přesunuta z karanténního skladu zpět do běžného skladu.</span><span class="sxs-lookup"><span data-stu-id="fe49e-141">When a quarantine order is ended, the item is moved from the quarantine warehouse back to the regular warehouse.</span></span> <span data-ttu-id="fe49e-142">Stav transakce zboží je v karanténním skladu nastaven na hodnotu **Prodáno** a v běžném skladu na **Koupeno**.</span><span class="sxs-lookup"><span data-stu-id="fe49e-142">The status of the item transaction is set to **Sold** at the quarantine warehouse and **Purchased** at the regular warehouse.</span></span>

## <a name="quarantine-order-scrap"></a><span data-ttu-id="fe49e-143">Vyřazení karanténních příkazů</span><span class="sxs-lookup"><span data-stu-id="fe49e-143">Quarantine order scrap</span></span>
<span data-ttu-id="fe49e-144">Jako součást procesu karanténní objednávky je možné zásoby vyřadit.</span><span class="sxs-lookup"><span data-stu-id="fe49e-144">As part of the quarantine order process, you can scrap inventory.</span></span> <span data-ttu-id="fe49e-145">Při zpracování vyřazených zásob bude stav zásob nastaven na **Prodáno** podle transakce výdeje z karanténního skladu.</span><span class="sxs-lookup"><span data-stu-id="fe49e-145">When you process scrap, the status of the inventory will be set to **Sold** by an issue transaction from the quarantine warehouse.</span></span>

<a name="additional-resources"></a><span data-ttu-id="fe49e-146">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="fe49e-146">Additional resources</span></span>
--------

[<span data-ttu-id="fe49e-147">Blokování zásob</span><span class="sxs-lookup"><span data-stu-id="fe49e-147">Inventory blocking</span></span>](inventory-blocking.md)
