---
title: Přehled odchozího procesu
description: Toto téma obsahuje přehled odchozího procesu v modulu Řízení zásob.
author: perlynne
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSOrder, WMSShipment, MCRPickingWorkbench, WMSPickingRegistration, CustomFilterGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 274363
ms.assetid: 375807b2-a426-4f1b-bc1f-2fe00fd48413
ms.search.region: global
ms.search.industry: Distribution
ms.author: perlynne
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.openlocfilehash: 27596bf260c069af4a7457c0eb8d02c45e5202b9
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "5000227"
---
# <a name="outbound-process-overview"></a><span data-ttu-id="6deca-103">Přehled odchozího procesu</span><span class="sxs-lookup"><span data-stu-id="6deca-103">Outbound process overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6deca-104">Toto téma obsahuje přehled odchozího procesu v modulu Řízení zásob.</span><span class="sxs-lookup"><span data-stu-id="6deca-104">This topic provides an overview of the outbound process in Inventory management.</span></span>

## <a name="output-orders"></a><span data-ttu-id="6deca-105">Výstupní objednávky</span><span class="sxs-lookup"><span data-stu-id="6deca-105">Output orders</span></span>

<span data-ttu-id="6deca-106">Výstupní objednávky se používají k propojení řádků prodejní objednávky a řádků převodního příkazu s odchozími procesy výdeje, které používají výdejky.</span><span class="sxs-lookup"><span data-stu-id="6deca-106">Output orders are used to link sales order lines and transfer order lines with the outbound picking processes that use picking lists.</span></span>

<span data-ttu-id="6deca-107">Pokud jsou dodací listy generovány buď z prodejních objednávek nebo převodních příkazů, budou automaticky vytvořeny výstupní objednávky a dodávky.</span><span class="sxs-lookup"><span data-stu-id="6deca-107">When picking lists are generated from either sales orders or transfer orders, output orders and shipments are automatically created.</span></span> <span data-ttu-id="6deca-108">Výdejka má vztah jedna ku jedné s dodávkou.</span><span class="sxs-lookup"><span data-stu-id="6deca-108">A picking list has a one-to-one relationship with a shipment.</span></span> <span data-ttu-id="6deca-109">Dodávku převodního příkazu nebo dodací list prodejní objednávky lze zpracovat z dodávky.</span><span class="sxs-lookup"><span data-stu-id="6deca-109">The transfer order shipment or the sales order packing slip can be processed from the shipment.</span></span> 

<span data-ttu-id="6deca-110">Následující diagram znázorňuje přehled procesu výstupních objednávek.</span><span class="sxs-lookup"><span data-stu-id="6deca-110">The following diagram shows an overview of the process for outbound orders.</span></span> 

<span data-ttu-id="6deca-111">[![Přehled procesu výstupních objednávek](./media/outbound-order.png)](./media/outbound-order.png)</span><span class="sxs-lookup"><span data-stu-id="6deca-111">[![Overview of the outbound order process](./media/outbound-order.png)](./media/outbound-order.png)</span></span>

<span data-ttu-id="6deca-112">Můžete nastavit výstupní pravidla určující způsob, jak má program zpracovat odchozí proces.</span><span class="sxs-lookup"><span data-stu-id="6deca-112">You can set up outbound rules to define how the program should handle the outbound process.</span></span> <span data-ttu-id="6deca-113">Tato pravidla můžete použít ke kontrole procesu dodávky.</span><span class="sxs-lookup"><span data-stu-id="6deca-113">You can use these rules to control the shipment process.</span></span> <span data-ttu-id="6deca-114">Pravidla můžete použít obzvláště ke kontrole toho, během které fáze procesu lze odeslat dodávku.</span><span class="sxs-lookup"><span data-stu-id="6deca-114">In particular, you can use the rules to control which stage in the process a shipment can be sent during.</span></span> <span data-ttu-id="6deca-115">Následující nastavení určují způsob zpracování odchozích procesů.</span><span class="sxs-lookup"><span data-stu-id="6deca-115">The following settings define how the outbound processes are handled.</span></span>

## <a name="picking-route-status-for-sales-and-transfer-orders"></a><span data-ttu-id="6deca-116">Stav postupu výdeje pro prodejní objednávky a převodní příkazy</span><span class="sxs-lookup"><span data-stu-id="6deca-116">Picking route status for sales and transfer orders</span></span> 

<span data-ttu-id="6deca-117">Přejděte na **Pohledávky** \> **Nastavení** \> **Parametry pohledávek** a poté na kartě **Aktualizace** vyberte hodnotu v poli **Stav postupu výdeje**.</span><span class="sxs-lookup"><span data-stu-id="6deca-117">Go to **Account receivable** \> **Setup** \> **Account receivable parameters**, and then, on the **Updates** tab, select a value in the **Picking route status** field.</span></span>

<span data-ttu-id="6deca-118">[![Pole stav postupu výdeje pro prodejní objednávky](./media/picking-route-status-sales-order.png)](./media/picking-route-status-sales-order.png)</span><span class="sxs-lookup"><span data-stu-id="6deca-118">[![Picking route status field for sales orders](./media/picking-route-status-sales-order.png)](./media/picking-route-status-sales-order.png)</span></span>

<span data-ttu-id="6deca-119">Pokud je pole **Stav postupu výdeje** nastaveno na **Dokončeno**, dojde k procesu výdeje automaticky jako součásti procesu generování výdejek.</span><span class="sxs-lookup"><span data-stu-id="6deca-119">If the **Picking route status** field is set to **Completed**, the picking process occurs automatically as part of the process of generating picking lists.</span></span> <span data-ttu-id="6deca-120">Pokud je pole nastaveno na **Aktivováno**, řádky výdejky musíte aktualizovat ručně.</span><span class="sxs-lookup"><span data-stu-id="6deca-120">If the field is set to **Activated**, the picking list lines must be manually updated.</span></span>

<span data-ttu-id="6deca-121">Stejné nastavení se vztahuje k převodním příkazům.</span><span class="sxs-lookup"><span data-stu-id="6deca-121">The same setup applies to transfer orders.</span></span> <span data-ttu-id="6deca-122">Přejděte na **Řízení zásob** \> **Nastavení** \> **Parametry řízení zásob a skladu** a poté na kartě **Přeprava** vyberte hodnotu v poli **Stav postupu výdeje**.</span><span class="sxs-lookup"><span data-stu-id="6deca-122">Go to **Inventory management** \> **Setup** \> **Inventory and warehouse management parameters**, and then, on the **Transport** tab, select a value in the **Picking route status** field.</span></span>

<span data-ttu-id="6deca-123">[![Pole stav postupu výdeje pro převodní příkazy](./media/picking-route-status-transfer-order.png)](./media/picking-route-status-transfer-order.png)</span><span class="sxs-lookup"><span data-stu-id="6deca-123">[![Picking route status field for transfer orders](./media/picking-route-status-transfer-order.png)](./media/picking-route-status-transfer-order.png)</span></span>

## <a name="end-output-inventory-orders"></a><span data-ttu-id="6deca-124">Ukončení výstupních skladových objednávek</span><span class="sxs-lookup"><span data-stu-id="6deca-124">End output inventory orders</span></span>

<span data-ttu-id="6deca-125">Přejděte na **Řízení zásob** \> **Nastavení** \> **Parametry řízení zásob a skladu** a poté na kartě **Obecné** nastavte možnost **Ukončit výstupní skladovou objednávku**.</span><span class="sxs-lookup"><span data-stu-id="6deca-125">Go to **Inventory management** \> **Setup** \> **Inventory and warehouse management parameters**, and then, on the **General** tab, set the **End output inventory order** option.</span></span>

<span data-ttu-id="6deca-126">[![Možnost Ukončit výstupní skladovou objednávku](./media//end-output-inventory-order.png)](./media//end-output-inventory-order.png)</span><span class="sxs-lookup"><span data-stu-id="6deca-126">[![End output inventory order option](./media//end-output-inventory-order.png)](./media//end-output-inventory-order.png)</span></span>

<span data-ttu-id="6deca-127">Když pracovníci ve skladu snižují množství výdejky, budou z expedice odebrána odpovídající množství oskladové objednávky.</span><span class="sxs-lookup"><span data-stu-id="6deca-127">When the warehouse worker reduces the picking list quantities, then the corresponding inventory order quantities will be removed from the shipment.</span></span> <span data-ttu-id="6deca-128">Při aktualizaci výdejky v určitý okamžik se zbývající množství vykáže zpět do objednávky, pokud je možnost **Ukončit výstupní skladovou objednávku** nastavena na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="6deca-128">When the picking list is updated at a point in time, the remaining quantities get reported back to the order if the **End output inventory order** option is set to **Yes**.</span></span> <span data-ttu-id="6deca-129">Pokud je možnost **Ukončit výstupní skladovou objednávku** nastavena na **Ne**, zbývající množství se zachová jako otevřené množství výstupní objednávky a je nutné ho přidat do nové výdejky jako součást funkce **Otevřené výstupní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="6deca-129">If the **End output inventory order** option is set to **No**, the remaining quantities are kept as an open output order quantity and must be added to a new picking list as part of the **Open output orders** functionality.</span></span> 

<span data-ttu-id="6deca-130">[![Příkaz Otevřít výstupní objednávky v nabídce funkcí](./media/open-output-order.png)](./media/open-output-order.png)</span><span class="sxs-lookup"><span data-stu-id="6deca-130">[![Open output orders command on the Functions menu](./media/open-output-order.png)](./media/open-output-order.png)</span></span>

<span data-ttu-id="6deca-131">[![Nabídka funkcí na stránce Otevřít výstupní objednávky](./media/open-output-order-function.png)](./media/open-output-order-function.png)</span><span class="sxs-lookup"><span data-stu-id="6deca-131">[![Functions menu on the Open output orders page](./media/open-output-order-function.png)](./media/open-output-order-function.png)</span></span>

## <a name="reduce-quantity"></a><span data-ttu-id="6deca-132">Snížit množství</span><span class="sxs-lookup"><span data-stu-id="6deca-132">Reduce quantity</span></span>

<span data-ttu-id="6deca-133">Třetí parametr, který můžete použít jako součást procesu generování výdejek, je parametr **Snížit množství**.</span><span class="sxs-lookup"><span data-stu-id="6deca-133">The third parameter that you can use as part of the process of generating picking lists is the **Reduce quantity** parameter.</span></span> <span data-ttu-id="6deca-134">Nastavení tohoto parametru se používá spolu s nastavením **Rezervace**, které spustí proces rezervace jako součást uvolnění do skladu.</span><span class="sxs-lookup"><span data-stu-id="6deca-134">The setting of this parameter works together with the **Reservation** setting that triggers a reservation process as part of the release to the warehouse.</span></span>

<span data-ttu-id="6deca-135">[![Parametr Snížit množství](./media/reduce-quantity.png)](./media/reduce-quantity.png)</span><span class="sxs-lookup"><span data-stu-id="6deca-135">[![Reduce quantity parameter](./media/reduce-quantity.png)](./media/reduce-quantity.png)</span></span>

## <a name="example-of-an-outbound-process-for-a-sales-order"></a><span data-ttu-id="6deca-136">Příklad odchozího procesu pro prodejní objednávku</span><span class="sxs-lookup"><span data-stu-id="6deca-136">Example of an outbound process for a sales order</span></span>

<span data-ttu-id="6deca-137">V tomto příkladu je prodejní objednávka pro dvě položky.</span><span class="sxs-lookup"><span data-stu-id="6deca-137">For this example, there is a sales order for two items.</span></span> <span data-ttu-id="6deca-138">Během generování seznamu výdejek zvolte parametr **Snížit množství**.</span><span class="sxs-lookup"><span data-stu-id="6deca-138">During picking list generation, you select the **Reduce quantity** parameter.</span></span> <span data-ttu-id="6deca-139">Tím uvolníte a vytvoříte řádky výdeje pouze pro dostupné zásoby na skladě.</span><span class="sxs-lookup"><span data-stu-id="6deca-139">Therefore, you release and create picking lines only for available on-hand inventory.</span></span> <span data-ttu-id="6deca-140">Výdej musí být nahlášen pomocí procesu registrace výdejek (**Stav postupu výdeje** = **Aktivováno**).</span><span class="sxs-lookup"><span data-stu-id="6deca-140">The picking must be reported via a registration process for picking lists (**Picking route status** = **Activated**).</span></span>

<span data-ttu-id="6deca-141">Zásoby. které nebyly ještě rezervovány, se zarezervují během generování výdejek.</span><span class="sxs-lookup"><span data-stu-id="6deca-141">The inventory that hasn't already been reserved is reserved during picking list generation.</span></span> <span data-ttu-id="6deca-142">Nedostupné zásoby lze buď odebrat z prodejní objednávky nebo uvolnit do skladu pro pozdější odchozí zpracování, až budou zásoby k dispozici pro výdej.</span><span class="sxs-lookup"><span data-stu-id="6deca-142">The unavailable inventory can be either removed from the sales order or released to the warehouse for outbound processing later, when inventory is available for picking.</span></span>

<span data-ttu-id="6deca-143">[![Aktualizace výdejky](./media/update-picking-list.png)](./media/update-picking-list.png)</span><span class="sxs-lookup"><span data-stu-id="6deca-143">[![Update the picking list](./media/update-picking-list.png)](./media/update-picking-list.png)</span></span>

<span data-ttu-id="6deca-144">Jakmile byly vyskladněny všechny řádků výdeje na stránce **Registrace výdejky**, přidružená dodávka je dokončena.</span><span class="sxs-lookup"><span data-stu-id="6deca-144">As soon as all the picking lines have been picked on the **Picking list registration** page, the associated shipment is completed.</span></span> <span data-ttu-id="6deca-145">Poté lze inicializovat proces pro dodací listy prodejní objednávky na základě vyskladněných zásob.</span><span class="sxs-lookup"><span data-stu-id="6deca-145">The process for sales order packing slips can then be initialized based on the picked inventory.</span></span>

<span data-ttu-id="6deca-146">[![Aktualizace odchozích dodávek](./media/outbound-shipments.png)](./media/outbound-shipments.png)</span><span class="sxs-lookup"><span data-stu-id="6deca-146">[![Update outbound shipments](./media/outbound-shipments.png)](./media/outbound-shipments.png)</span></span>
