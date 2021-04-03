---
title: Dostupnost zásob v dvojitém zápisu
description: Toto téma obsahuje informace o kontrole dostupnosti zásob ve dvojím zapisování.
author: yijialuan
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: riluan
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-05-26
ms.openlocfilehash: 48e54c043967ea5db15938857bd8f020dd4dfc64
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2021
ms.locfileid: "5566732"
---
# <a name="inventory-availability-in-dual-write"></a><span data-ttu-id="5197f-103">Dostupnost zásob v dvojitém zápisu</span><span class="sxs-lookup"><span data-stu-id="5197f-103">Inventory availability in dual-write</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5197f-104">Pomocí dostupnosti zásob můžete zkontrolovat své zásoby před přidáním produktu do formulářů **Nabídky**, **Objednávky** nebo **Faktury** v modelem řízených aplikacích v Microsoft Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="5197f-104">By using inventory availability, you can check your inventory before you add a product to the **Quotations**, **Orders**, or **Invoices** page in Microsoft Dynamics 365 Sales.</span></span> <span data-ttu-id="5197f-105">Například kontrolujete zásoby a určíte, že jednou z klíčových úloh ve [zpeněžení potenciálního zákazníka](dual-write-prospect-to-cash.md) je určení data plnění.</span><span class="sxs-lookup"><span data-stu-id="5197f-105">For example, you check inventory and determine a fulfillment date as one key task in the [prospect-to-cash](dual-write-prospect-to-cash.md) process.</span></span>

<span data-ttu-id="5197f-106">Pokud nemáte dostatek zásob, můžete odhadnout datum dodání na základě předpokládaných příjmů a problémů se zásobami.</span><span class="sxs-lookup"><span data-stu-id="5197f-106">If you don't have enough inventory, you can estimate a delivery date, based on projected inventory receipts and issues.</span></span> <span data-ttu-id="5197f-107">Můžete také zkontrolovat dostupné informace o produktu Lze slíbit (ATP), kde najdete množství ATP v předem definované ochranné době.</span><span class="sxs-lookup"><span data-stu-id="5197f-107">You can also check the product's available-to-promise (ATP) information, where you can find the ATP quantity in the predefined time fence.</span></span>

## <a name="on-hand-inventory"></a><span data-ttu-id="5197f-108">Zásoby na skladě</span><span class="sxs-lookup"><span data-stu-id="5197f-108">On-hand inventory</span></span>

<span data-ttu-id="5197f-109">V Dynamics 365 Sales bylo přidáno nové tlačítko **Zásoby na skladě** do záhlaví stránek **Nabídky**, **Objednávky** a **Faktury**.</span><span class="sxs-lookup"><span data-stu-id="5197f-109">In Dynamics 365 Sales, a new **On-hand Inventory** button has been added to the header of the **Quotes**, **Orders**, and **Invoices** pages.</span></span> <span data-ttu-id="5197f-110">Po výběru tohoto tlačítka se zobrazí dialogové okno, kde můžete určit společnost a produkt, u kterého chcete zkontrolovat zásoby na skladě.</span><span class="sxs-lookup"><span data-stu-id="5197f-110">When you select this button, a dialog box appears, where you can specify the company and the product that you want to check the on-hand inventory for.</span></span> <span data-ttu-id="5197f-111">Toto dialogové okno zobrazuje stejné informace jako [Zásoby na skladě](../../../../supply-chain/inventory/tasks/check-availability-stock.md).</span><span class="sxs-lookup"><span data-stu-id="5197f-111">This dialog box shows the same information as [On-hand inventory](../../../../supply-chain/inventory/tasks/check-availability-stock.md).</span></span>

<span data-ttu-id="5197f-112">Dialogové okno vrací informace o zásobách z Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="5197f-112">The dialog box returns the inventory information from Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="5197f-113">Tato informace obsahuje následující množství:</span><span class="sxs-lookup"><span data-stu-id="5197f-113">This information includes the following quantities:</span></span>

- <span data-ttu-id="5197f-114">Množství na skladě</span><span class="sxs-lookup"><span data-stu-id="5197f-114">On-hand quantity</span></span>
- <span data-ttu-id="5197f-115">Rezervované množství na skladě</span><span class="sxs-lookup"><span data-stu-id="5197f-115">Reserved on-hand quantity</span></span>
- <span data-ttu-id="5197f-116">Dostupné množství na skladě</span><span class="sxs-lookup"><span data-stu-id="5197f-116">Available on-hand quantity</span></span>
- <span data-ttu-id="5197f-117">Objednané množství</span><span class="sxs-lookup"><span data-stu-id="5197f-117">Ordered quantity</span></span>
- <span data-ttu-id="5197f-118">Množství na objednávce</span><span class="sxs-lookup"><span data-stu-id="5197f-118">On-order quantity</span></span>
- <span data-ttu-id="5197f-119">Rezervované objednané množství</span><span class="sxs-lookup"><span data-stu-id="5197f-119">Reserved ordered quantity</span></span>
- <span data-ttu-id="5197f-120">Celkové dostupné množství</span><span class="sxs-lookup"><span data-stu-id="5197f-120">Total available quantity</span></span>

## <a name="atp-information"></a><span data-ttu-id="5197f-121">Informace ATP</span><span class="sxs-lookup"><span data-stu-id="5197f-121">ATP information</span></span>

<span data-ttu-id="5197f-122">Do aplikace Sales bylo přidáno nové tlačítko **Informace ATP** k položkám řádku na stránkách **Nabídky**, **Objednávky** a **Faktury**.</span><span class="sxs-lookup"><span data-stu-id="5197f-122">In Sales, a new **ATP Information** button has been added to line items on the **Quotes**, **Orders**, and **Invoices** pages.</span></span> <span data-ttu-id="5197f-123">Po výběru tlačítka se zobrazí dialogové okno, kde můžete určit společnost, produkt, skladové pracoviště, sklad zásob a množství na objednávce.</span><span class="sxs-lookup"><span data-stu-id="5197f-123">When you select this button, a dialog box appears, where you can specify the company, product, inventory site, inventory warehouse, and order quantity.</span></span> <span data-ttu-id="5197f-124">Toto dialogové okno má stejná nastavení, jaká jsou popsána v části [Příslib objednávky](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations).</span><span class="sxs-lookup"><span data-stu-id="5197f-124">This dialog box has the same settings that are described in [Order promising](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations).</span></span>

<span data-ttu-id="5197f-125">Dialogové okno vrací informace ATP ze Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="5197f-125">The dialog box returns the ATP information from Supply Chain Management.</span></span> <span data-ttu-id="5197f-126">Tato informace obsahuje následující množství:</span><span class="sxs-lookup"><span data-stu-id="5197f-126">This information includes the following quantities:</span></span>

- <span data-ttu-id="5197f-127">Množství ATP</span><span class="sxs-lookup"><span data-stu-id="5197f-127">ATP quantity</span></span>
- <span data-ttu-id="5197f-128">Množství příjmu</span><span class="sxs-lookup"><span data-stu-id="5197f-128">Receipt quantity</span></span>
- <span data-ttu-id="5197f-129">Množství výdeje</span><span class="sxs-lookup"><span data-stu-id="5197f-129">Issue quantity</span></span>
- <span data-ttu-id="5197f-130">Množství na skladě</span><span class="sxs-lookup"><span data-stu-id="5197f-130">On-hand quantity</span></span>

## <a name="how-it-works"></a><span data-ttu-id="5197f-131">Jak to funguje</span><span class="sxs-lookup"><span data-stu-id="5197f-131">How it works</span></span>

<span data-ttu-id="5197f-132">Když vyberete tlačítko **Zásoby na skladě** na stránce **Nabídky**, **Objednávky** nebo **Faktury**, provede se živé volání rozhraní API duálního zápisu **Zásoby na skladě**.</span><span class="sxs-lookup"><span data-stu-id="5197f-132">When you select the **On-hand Inventory** button on the **Quotes**, **Orders**, or **Invoices** page, a live dual-write call is made to the **Onhand inventory** API.</span></span> <span data-ttu-id="5197f-133">API vypočítá zásoby na skladě pro daný produkt.</span><span class="sxs-lookup"><span data-stu-id="5197f-133">The API calculates the on-hand inventory for the given product.</span></span> <span data-ttu-id="5197f-134">Výsledek se uloží do tabulek **InventCDSInventoryOnHandRequestEntity** a **InventCDSInventoryOnHandEntryEntity** a poté se zapíše do Dataverse duálním zápisem.</span><span class="sxs-lookup"><span data-stu-id="5197f-134">The result is stored in the **InventCDSInventoryOnHandRequestEntity** and **InventCDSInventoryOnHandEntryEntity** tables, and then is written to Dataverse by dual-write.</span></span> <span data-ttu-id="5197f-135">Chcete-li použít tuto funkci, musíte spustit následující mapy duálního zápisu.</span><span class="sxs-lookup"><span data-stu-id="5197f-135">To use this functionality, you need to run the following dual-write maps.</span></span> <span data-ttu-id="5197f-136">Při spuštění map přeskočte počáteční synchronizaci.</span><span class="sxs-lookup"><span data-stu-id="5197f-136">Skip initial synchronization when you run the maps.</span></span>

- <span data-ttu-id="5197f-137">Ruční záznamy o zásobách CDS (msdyn_inventoryonhandentries)</span><span class="sxs-lookup"><span data-stu-id="5197f-137">CDS inventory on-hand entries (msdyn_inventoryonhandentries)</span></span>
- <span data-ttu-id="5197f-138">Ruční žádosti o zásoby CDS (msdyn_inventoryonhandrequests)</span><span class="sxs-lookup"><span data-stu-id="5197f-138">CDS inventory on-hand requests (msdyn_inventoryonhandrequests)</span></span>

## <a name="templates"></a><span data-ttu-id="5197f-139">Šablony</span><span class="sxs-lookup"><span data-stu-id="5197f-139">Templates</span></span>
<span data-ttu-id="5197f-140">Následující šablony jsou k dispozici pro vystavení údajů o přímých zásobách.</span><span class="sxs-lookup"><span data-stu-id="5197f-140">The following templates are available for the exposing the onhand inventory data.</span></span>

<span data-ttu-id="5197f-141">Aplikace Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="5197f-141">Finance and Operations apps</span></span> | <span data-ttu-id="5197f-142">Aplikace Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="5197f-142">Customer engagement app</span></span> | <span data-ttu-id="5197f-143">popis</span><span class="sxs-lookup"><span data-stu-id="5197f-143">Description</span></span> 
---|---|---
[<span data-ttu-id="5197f-144">Položky zásob na skladě CDS</span><span class="sxs-lookup"><span data-stu-id="5197f-144">CDS inventory on-hand entries</span></span>](#145) | <span data-ttu-id="5197f-145">msdyn_inventoryonhandentries</span><span class="sxs-lookup"><span data-stu-id="5197f-145">msdyn_inventoryonhandentries</span></span> |
[<span data-ttu-id="5197f-146">Požadavky na zásoby na skladě CDS</span><span class="sxs-lookup"><span data-stu-id="5197f-146">CDS inventory on-hand requests</span></span>](#147) | <span data-ttu-id="5197f-147">msdyn_inventoryonhandrequests</span><span class="sxs-lookup"><span data-stu-id="5197f-147">msdyn_inventoryonhandrequests</span></span> |

[!include [banner](../../includes/dual-write-symbols.md)]

###  <a name="cds-inventory-on-hand-entries-msdyn_inventoryonhandentries"></a><a name="145"></a><span data-ttu-id="5197f-148">Ruční záznamy o zásobách CDS (msdyn_inventoryonhandentries)</span><span class="sxs-lookup"><span data-stu-id="5197f-148">CDS inventory on-hand entries (msdyn_inventoryonhandentries)</span></span>

<span data-ttu-id="5197f-149">Tato šablona synchronizuje data mezi aplikacemi Finance and Operations a Dataverse.</span><span class="sxs-lookup"><span data-stu-id="5197f-149">This template synchronizes data between Finance and Operations apps and Dataverse.</span></span>

<span data-ttu-id="5197f-150">Pole aplikace Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="5197f-150">Finance and Operations field</span></span> | <span data-ttu-id="5197f-151">Typ mapování</span><span class="sxs-lookup"><span data-stu-id="5197f-151">Map type</span></span> | <span data-ttu-id="5197f-152">Pole Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="5197f-152">Customer engagement field</span></span> | <span data-ttu-id="5197f-153">Výchozí hodnota</span><span class="sxs-lookup"><span data-stu-id="5197f-153">Default value</span></span>
---|---|---|---
`REQUESTID` | = | `msdyn_request.msdyn_requestid` |
`INVENTORYSITEID` | = | `msdyn_inventorysite.msdyn_siteid` |
`INVENTORYWAREHOUSEID` | = | `msdyn_inventorywarehouse.msdyn_warehouseidentifier` |
`AVAILABLEONHANDQUANTITY` | > | `msdyn_availableonhandquantity` |
`AVAILABLEORDEREDQUANTITY` | > | `msdyn_availableorderedquantity` |
`ONHANDQUANTITY` | > | `msdyn_onhandquantity` |
`ONORDERQUANTITY` | > | `msdyn_onorderquantity` |
`ORDEREDQUANTITY` | > | `msdyn_orderedquantity` |
`RESERVEDONHANDQUANTITY` | > | `msdyn_reservedonhandquantity` |
`RESERVEDORDEREDQUANTITY` | > | `msdyn_reservedorderedquantity` |
`TOTALAVAILABLEQUANTITY` | > | `msdyn_totalavailablequantity` |
`ATPDATE` | = | `msdyn_atpdate` |
`ATPQUANTITY` | > | `msdyn_atpquantity` |
`PROJECTEDISSUEQUANTITY` | > | `msdyn_projectedissuequantity` |
`PROJECTEDONHANDQUANTITY` | > | `msdyn_projectedonhandquantity` |
`PROJECTEDRECEIPTQUANTITY` | > | `msdyn_projectedreceiptquantity` |
`ORDERQUANTITY` | > | `msdyn_orderquantity` |
`UNAVAILABLEONHANDQUANTITY` | > | `msdyn_unavailableonhandquantity` |

###  <a name="cds-inventory-on-hand-requests-msdyn_inventoryonhandrequests"></a><a name="147"></a><span data-ttu-id="5197f-154">Ruční žádosti o zásoby CDS (msdyn_inventoryonhandrequests)</span><span class="sxs-lookup"><span data-stu-id="5197f-154">CDS inventory on-hand requests (msdyn_inventoryonhandrequests)</span></span>

<span data-ttu-id="5197f-155">Tato šablona synchronizuje data mezi aplikacemi Finance and Operations a Dataverse.</span><span class="sxs-lookup"><span data-stu-id="5197f-155">This template synchronizes data between Finance and Operations apps and Dataverse.</span></span>

<span data-ttu-id="5197f-156">Pole aplikace Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="5197f-156">Finance and Operations field</span></span> | <span data-ttu-id="5197f-157">Typ mapování</span><span class="sxs-lookup"><span data-stu-id="5197f-157">Map type</span></span> | <span data-ttu-id="5197f-158">Pole Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="5197f-158">Customer engagement field</span></span> | <span data-ttu-id="5197f-159">Výchozí hodnota</span><span class="sxs-lookup"><span data-stu-id="5197f-159">Default value</span></span>
---|---|---|---
`REQUESTID` | = | `msdyn_requestid` |
`PRODUCTNUMBER` | < | `msdyn_product.msdyn_productnumber` |
`ISATPCALCULATION` | << | `msdyn_isatpcalculation` |
`ORDERQUANTITY` | < | `msdyn_orderquantity` |
`INVENTORYSITEID` | < | `msdyn_inventorysite.msdyn_siteid` |
`INVENTORYWAREHOUSEID` | < | `msdyn_inventorywarehouse.msdyn_warehouseidentifier` |
`REFERENCENUMBER` | < | `msdyn_referencenumber` |
`LINECREATIONSEQUENCENUMBER` | < | `msdyn_linecreationsequencenumber` |






[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]