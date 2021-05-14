---
title: Karanténní příkazy
description: Toto téma popisuje jak použít karanténní příkazy k blokování zásob.
author: perlynne
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventLocation, InventModelGroup, InventQuarantineOrder, InventQuarantineParmEnd, InventQuarantineParmReportFinished, InventQuarantineParmStartUp, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.custom: 30021
ms.assetid: d5047727-653c-49da-b489-6fd3fe50445e
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5e1eed14b7d38cf569af7192dec9580e771f06df
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956175"
---
# <a name="quarantine-orders"></a><span data-ttu-id="df0f3-103">Karanténní příkazy</span><span class="sxs-lookup"><span data-stu-id="df0f3-103">Quarantine orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="df0f3-104">Toto téma popisuje jak použít karanténní příkazy k blokování zásob.</span><span class="sxs-lookup"><span data-stu-id="df0f3-104">This topic describes how to use quarantine orders to block inventory.</span></span>

<span data-ttu-id="df0f3-105">Karanténní příkazy vám umožňují blokovat zásoby.</span><span class="sxs-lookup"><span data-stu-id="df0f3-105">Quarantine orders let you block inventory.</span></span> <span data-ttu-id="df0f3-106">Můžete například chtít umístit do karantény položky z důvodů kontroly kvality.</span><span class="sxs-lookup"><span data-stu-id="df0f3-106">For example, you might want to quarantine items for quality control reasons.</span></span> <span data-ttu-id="df0f3-107">Sklad, který byl umístěn do karantény, je převeden do karanténního skladu.</span><span class="sxs-lookup"><span data-stu-id="df0f3-107">Inventory that has been quarantined is transferred to a quarantine warehouse.</span></span>

> [!NOTE]
> <span data-ttu-id="df0f3-108">Pokud používáte rozšířené procesy správy skladu (v modulu Řízení skladu), zpracování karanténního příkazu se používá pouze pro vrácení prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="df0f3-108">If you're using advanced warehouse management processes (in Warehouse management), quarantine order processing is used only for return sales orders.</span></span>

## <a name="quarantine-on-hand-inventory-items"></a><span data-ttu-id="df0f3-109">Karanténní zásoby položek na skladě</span><span class="sxs-lookup"><span data-stu-id="df0f3-109">Quarantine on-hand inventory items</span></span>

<span data-ttu-id="df0f3-110">Při umístění položek do karantény můžete vytvořit karanténní příkazy ručně nebo systém nastavit tak, aby vytvářel karanténní příkazy automaticky při zpracování příchozích.</span><span class="sxs-lookup"><span data-stu-id="df0f3-110">When you quarantine items, you can either manually create the quarantine orders or set up the system to automatically create them during inbound processing.</span></span>

<span data-ttu-id="df0f3-111">Chcete-li nastavit systém tak, aby automaticky generoval karanténní příkazy, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="df0f3-111">To set up the system to automatically generate quarantine orders, follow these steps.</span></span>

1. <span data-ttu-id="df0f3-112">Přejděte k nabídce **Řízení zásob \> Nastavení \> Zásoby \> Skupiny modelu položky**.</span><span class="sxs-lookup"><span data-stu-id="df0f3-112">Go to **Inventory management \> Setup \> Inventory \> Item model groups**.</span></span>
1. <span data-ttu-id="df0f3-113">Vyberte relevantní skupinu modelu v podokně seznamu, nebo vytvořte novou skupinu modelu.</span><span class="sxs-lookup"><span data-stu-id="df0f3-113">Select a relevant model group in the list pane, or create a new model group.</span></span>
1. <span data-ttu-id="df0f3-114">Na záložce s náhledem **Zásady zásob** zaškrtněte políčko **Řízení karantény**.</span><span class="sxs-lookup"><span data-stu-id="df0f3-114">On the **Inventory policies** FastTab, select the **Quarantine management** check box.</span></span>
1. <span data-ttu-id="df0f3-115">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="df0f3-115">Close the page.</span></span>
1. <span data-ttu-id="df0f3-116">V poli **Karanténní sklad** pro přijímací sklady zadejte výchozí karanténní sklad.</span><span class="sxs-lookup"><span data-stu-id="df0f3-116">In the **Quarantine warehouse** field for the receiving warehouses, specify a default quarantine warehouse.</span></span>

<span data-ttu-id="df0f3-117">Pokud položka, která je zaregistrována jako přijatá ve skladu, patří do skupiny modelů, kde je vybráno zaškrtávací políčko **Řízení karantény**, systém pro ni vygeneruje karanténní příkaz.</span><span class="sxs-lookup"><span data-stu-id="df0f3-117">When an item that is registered as received at the warehouse belongs to a model group where the **Quarantine management** check box is selected, the system generates a quarantine order for it.</span></span> <span data-ttu-id="df0f3-118">Karanténní příkaz dává pracovníkům pokyn, aby položku přesunuli do karanténního skladu.</span><span class="sxs-lookup"><span data-stu-id="df0f3-118">The quarantine order instructs workers to move the item to the quarantine warehouse.</span></span>

<span data-ttu-id="df0f3-119">Při ručním vytváření karanténních příkazů na stránce **Karanténní příkazy** není požadováno, aby v přidružené skupině modelů položek byla položka nastavena pro řízení karantény.</span><span class="sxs-lookup"><span data-stu-id="df0f3-119">When you manually create quarantine orders on the **Quarantine orders** page, the item doesn't have to be set up for quarantine management in the associated item model group.</span></span> <span data-ttu-id="df0f3-120">Za tímto účelem je nutné zadat zásob na skladě, která mají být umístěny do karantény, a karanténní sklad, který má být použit.</span><span class="sxs-lookup"><span data-stu-id="df0f3-120">For this process, you must specify the on-hand inventory that should be quarantined and the quarantine warehouse that should be used.</span></span> <span data-ttu-id="df0f3-121">Můžete použít stavy karanténních příkazů pro usnadnění plánování procesu.</span><span class="sxs-lookup"><span data-stu-id="df0f3-121">You can use the quarantine order statuses to help plan the process.</span></span>

## <a name="quarantine-order-statuses"></a><span data-ttu-id="df0f3-122">Stavy karanténního příkazu</span><span class="sxs-lookup"><span data-stu-id="df0f3-122">Quarantine order statuses</span></span>

<span data-ttu-id="df0f3-123">Karanténní příkazy mohou mít tyto stavy:</span><span class="sxs-lookup"><span data-stu-id="df0f3-123">Quarantine orders can have the following statuses:</span></span>

- <span data-ttu-id="df0f3-124">Vytvořeno</span><span class="sxs-lookup"><span data-stu-id="df0f3-124">Created</span></span>
- <span data-ttu-id="df0f3-125">Zahájeno</span><span class="sxs-lookup"><span data-stu-id="df0f3-125">Started</span></span>
- <span data-ttu-id="df0f3-126">Ohlášeno jako dokončené</span><span class="sxs-lookup"><span data-stu-id="df0f3-126">Reported as finished</span></span>
- <span data-ttu-id="df0f3-127">Ukončeno</span><span class="sxs-lookup"><span data-stu-id="df0f3-127">Ended</span></span>

### <a name="created"></a><span data-ttu-id="df0f3-128">Vytvořeno</span><span class="sxs-lookup"><span data-stu-id="df0f3-128">Created</span></span>

<span data-ttu-id="df0f3-129">Jestliže byla ručně vytvořena karanténní objednávka, ale položka ještě není uložena do karanténního skladu, karanténní příkaz obdrží stav **Vytvořeno**.</span><span class="sxs-lookup"><span data-stu-id="df0f3-129">When a quarantine order has been created manually, but the item isn't yet in the quarantine warehouse, the quarantine order has a status of **Created**.</span></span> <span data-ttu-id="df0f3-130">Vygenerují se dvě skladové transakce.</span><span class="sxs-lookup"><span data-stu-id="df0f3-130">Two inventory transactions are generated.</span></span> <span data-ttu-id="df0f3-131">Jedna je transakce výdeje, která může mít stav **Na objednávce**, **Rezervované – fyzicky** nebo **Vyskladněno**.</span><span class="sxs-lookup"><span data-stu-id="df0f3-131">One transaction is an issue transaction that can have a status of **On order**, **Reserved physical**, or **Picked**.</span></span> <span data-ttu-id="df0f3-132">Druhá je příjmová transakce, která může mít v karanténním skladu stav **Objednáno** nebo **Registrováno**.</span><span class="sxs-lookup"><span data-stu-id="df0f3-132">The other transaction is a receipt transaction that can have a status of **Ordered** or **Registered** at the quarantine warehouse.</span></span> <span data-ttu-id="df0f3-133">Rezervaci, vyskladnění a aktualizaci registrace zásob můžete provádět pomocí obvyklých procesů.</span><span class="sxs-lookup"><span data-stu-id="df0f3-133">You can reserve, pick, and register updates to the inventory by using the usual processes.</span></span>

### <a name="started"></a><span data-ttu-id="df0f3-134">Zahájeno</span><span class="sxs-lookup"><span data-stu-id="df0f3-134">Started</span></span>

<span data-ttu-id="df0f3-135">Když je karanténní příkaz ve stavu **Zahájeno** jsou pak položky přesunuty z obyčejného skladu do karanténního skladu a vytvoří se dvě skladové transakce.</span><span class="sxs-lookup"><span data-stu-id="df0f3-135">When a quarantine order has a status of **Started**, the inventory is transferred from the regular warehouse to the quarantine warehouse, and two inventory transactions are generated.</span></span> <span data-ttu-id="df0f3-136">Jedna transakce se nachází ve stavu **Odečteno** a jiné transakce nachází ve stavu **Přijato**.</span><span class="sxs-lookup"><span data-stu-id="df0f3-136">One transaction has a status of **Deducted**, and the other transaction has a status of **Received**.</span></span> <span data-ttu-id="df0f3-137">Zároveň se vytvoří také dvě skladové transakce k zajištění zpětného převodu.</span><span class="sxs-lookup"><span data-stu-id="df0f3-137">At the same time, two inventory transactions are created to handle the return transfer.</span></span> <span data-ttu-id="df0f3-138">Tyto transakce nejsou datovány.</span><span class="sxs-lookup"><span data-stu-id="df0f3-138">These transactions aren't dated.</span></span> <span data-ttu-id="df0f3-139">Jedna transakce se nachází ve stavu **Rezervované – fyzicky** a jiné transakce nachází ve stavu **Objednáno**.</span><span class="sxs-lookup"><span data-stu-id="df0f3-139">One transaction has a status of **Reserved physical**, and the other transaction has a status of **Ordered**.</span></span>

### <a name="reported-as-finished"></a><span data-ttu-id="df0f3-140">Ohlášeno jako dokončené</span><span class="sxs-lookup"><span data-stu-id="df0f3-140">Reported as finished</span></span>

<span data-ttu-id="df0f3-141">Chcete-li nahlásit zahájený karanténní příkaz jako dokončený, otevřete příkaz a vyberte v podokně akcí možnost **Oznámit jako dokončené**.</span><span class="sxs-lookup"><span data-stu-id="df0f3-141">To report a started quarantine order as finished, open the order, and select **Report as finished** on the Action Pane.</span></span> <span data-ttu-id="df0f3-142">Položka je uvolněna z karantény, ale ještě nebyla přesunuta zpět do běžného skladu.</span><span class="sxs-lookup"><span data-stu-id="df0f3-142">The item is released from quarantine, but it isn't yet moved back to the regular warehouse.</span></span> <span data-ttu-id="df0f3-143">Přesun zpět do běžného skladu je možné zpracovat pomocí deníku doručení položky, který může být inicializován během procesu oznámení jako dokončeno.</span><span class="sxs-lookup"><span data-stu-id="df0f3-143">The movement back to the regular warehouse can be processed via an item arrival journal that can be initialized during the report as finished process.</span></span>

### <a name="ended"></a><span data-ttu-id="df0f3-144">Ukončeno</span><span class="sxs-lookup"><span data-stu-id="df0f3-144">Ended</span></span>

<span data-ttu-id="df0f3-145">Když je karanténní příkaz ukončen, je položka přesunuta z karanténního skladu zpět do běžného skladu.</span><span class="sxs-lookup"><span data-stu-id="df0f3-145">When a quarantine order is ended, the item is moved from the quarantine warehouse back to the regular warehouse.</span></span> <span data-ttu-id="df0f3-146">Stav transakce zboží je v karanténním skladu nastaven na hodnotu *Prodáno* a v běžném skladu na *Koupeno*.</span><span class="sxs-lookup"><span data-stu-id="df0f3-146">The status of the item transaction is set to *Sold* at the quarantine warehouse and *Purchased* at the regular warehouse.</span></span>

## <a name="quarantine-order-scrap"></a><span data-ttu-id="df0f3-147">Vyřazení karanténních příkazů</span><span class="sxs-lookup"><span data-stu-id="df0f3-147">Quarantine order scrap</span></span>

<span data-ttu-id="df0f3-148">Jako součást procesu karanténní objednávky je možné zásoby vyřadit.</span><span class="sxs-lookup"><span data-stu-id="df0f3-148">As part of the quarantine order process, you can scrap inventory.</span></span> <span data-ttu-id="df0f3-149">Při zpracování vyřazených zásob je stav zásob nastaven na *Prodáno* podle transakce výdeje z karanténního skladu.</span><span class="sxs-lookup"><span data-stu-id="df0f3-149">When you process scrap, the status of the inventory is set to *Sold* by an issue transaction from the quarantine warehouse.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="df0f3-150">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="df0f3-150">Additional resources</span></span>

- [<span data-ttu-id="df0f3-151">Blokování zásob</span><span class="sxs-lookup"><span data-stu-id="df0f3-151">Inventory blocking</span></span>](inventory-blocking.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
