---
title: "Vytvoření nové zakázky na doplnění stavu zásob dodávky"
description: "Tato procedura ukazuje, jak vytvořit objednávku doplnění stavu zásob dodávky, kde můžete sledovat očekávanou dodávku od dodavatele do skladu dodávky."
author: mkirknel
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 0c8af002efb12f5b18100d2eb6c41c69a3daef1e
ms.contentlocale: cs-cz
ms.lasthandoff: 05/08/2018

---
# <a name="create-a-consignment-replenishment-order"></a><span data-ttu-id="d1071-103">Vytvoření nové zakázky na doplnění stavu zásob dodávky</span><span class="sxs-lookup"><span data-stu-id="d1071-103">Create a consignment replenishment order</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d1071-104">Tato procedura ukazuje, jak vytvořit objednávku doplnění stavu zásob dodávky, kde můžete sledovat očekávanou dodávku od dodavatele do skladu dodávky.</span><span class="sxs-lookup"><span data-stu-id="d1071-104">This procedure shows how to create a consignment replenishment order where you can track the expected delivery from a vendor into your consignment inventory.</span></span> <span data-ttu-id="d1071-105">Také ukazuje, jak zaznamenávat příjem produktů tak, aby byla zásoba dodávky registrována jako zásoby na skladě ve vlastnictví dodavatele.</span><span class="sxs-lookup"><span data-stu-id="d1071-105">It also shows how to record a receipt of products so that the consignment inventory is registered as on-hand inventory owned by the vendor.</span></span> <span data-ttu-id="d1071-106">Tuto proceduru obvykle provádí zásobovací pracovník.</span><span class="sxs-lookup"><span data-stu-id="d1071-106">This procedure would typically be done by a procurement professional.</span></span> <span data-ttu-id="d1071-107">Tohoto průvodce můžete použít s ukázkových dat společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="d1071-107">You can use this guide in demo data company USMF.</span></span> <span data-ttu-id="d1071-108">Tato procedura je určena pro funkci, která byla přidána do aplikace Dynamics 365 for Operations, verze 1611.</span><span class="sxs-lookup"><span data-stu-id="d1071-108">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>




## <a name="create-a-consignment-replenishment-order"></a><span data-ttu-id="d1071-109">Vytvoření nové zakázky na doplnění stavu zásob dodávky</span><span class="sxs-lookup"><span data-stu-id="d1071-109">Create a consignment replenishment order</span></span>
1. <span data-ttu-id="d1071-110">Přejděte do nabídky Zásobování a zdroje > Zásilka > Zakázky na doplnění stavu zásob dodávky.</span><span class="sxs-lookup"><span data-stu-id="d1071-110">Go to Procurement and sourcing > Consignment > Consignment replenishment orders.</span></span>
2. <span data-ttu-id="d1071-111">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="d1071-111">Click New.</span></span>
3. <span data-ttu-id="d1071-112">V poli Účet dodavatele vyberte dodavatele US-104.</span><span class="sxs-lookup"><span data-stu-id="d1071-112">In the Vendor account field, select vendor US-104.</span></span>
    * <span data-ttu-id="d1071-113">Je nutné vybrat dodavatele, který je registrován jako vlastník na stránce Vlastníci zásob.</span><span class="sxs-lookup"><span data-stu-id="d1071-113">You must select a vendor that’s registered as an owner in the Inventory owners page.</span></span>  
4. <span data-ttu-id="d1071-114">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="d1071-114">Click OK.</span></span>
5. <span data-ttu-id="d1071-115">Klikněte na položku Přidat řádek.</span><span class="sxs-lookup"><span data-stu-id="d1071-115">Click Add line.</span></span>
6. <span data-ttu-id="d1071-116">Do pole Číslo položky zadejte M9211CI.</span><span class="sxs-lookup"><span data-stu-id="d1071-116">In the Item number field, type M9211CI.</span></span>
    * <span data-ttu-id="d1071-117">Je nutné vybrat položku, která je nastavena pro zásoby dodávky.</span><span class="sxs-lookup"><span data-stu-id="d1071-117">You must select an item that is set up for consignment inventory.</span></span>  
7. <span data-ttu-id="d1071-118">Zadejte číslo do pole Množství.</span><span class="sxs-lookup"><span data-stu-id="d1071-118">In the Quantity field, enter a number.</span></span>
8. <span data-ttu-id="d1071-119">Zadejte datum do pole Požadované datum dodání.</span><span class="sxs-lookup"><span data-stu-id="d1071-119">In the Requested delivery date field, enter a date.</span></span>
    * <span data-ttu-id="d1071-120">Požadované a potvrzené datum používá modul MRP pro očekávané přijetí zboží.</span><span class="sxs-lookup"><span data-stu-id="d1071-120">The requested and confirmed dates are used by the MRP engine for the expected arrival of the goods.</span></span>  
9. <span data-ttu-id="d1071-121">Zadejte datum do pole Potvrzené datum dodání.</span><span class="sxs-lookup"><span data-stu-id="d1071-121">In the Confirmed delivery date field, enter a date.</span></span>
10. <span data-ttu-id="d1071-122">Rozbalte sekci Podrobnosti řádku.</span><span class="sxs-lookup"><span data-stu-id="d1071-122">Expand the Line details section.</span></span>
11. <span data-ttu-id="d1071-123">Klepněte na kartu Dimenze zásob.</span><span class="sxs-lookup"><span data-stu-id="d1071-123">Click the Inventory dimensions tab.</span></span>
12. <span data-ttu-id="d1071-124">Chcete-li zobrazit vlastníka v poli Vlastník dimenze zásob, aktualizujte stránku.</span><span class="sxs-lookup"><span data-stu-id="d1071-124">To show the owner in the Inventory dimensions owner field, refresh the page.</span></span>
    * <span data-ttu-id="d1071-125">Dodavatel US-104 je nyní uveden jako vlastník.</span><span class="sxs-lookup"><span data-stu-id="d1071-125">Vendor US-104 is now listed as the owner.</span></span>  

## <a name="check-the-inventory-transaction-status"></a><span data-ttu-id="d1071-126">Zkontrolujte stav transakce zásob.</span><span class="sxs-lookup"><span data-stu-id="d1071-126">Check the inventory transaction status</span></span>
1. <span data-ttu-id="d1071-127">Klepněte na položku Zásoby.</span><span class="sxs-lookup"><span data-stu-id="d1071-127">Click Inventory.</span></span>
2. <span data-ttu-id="d1071-128">Klikněte na Transakce.</span><span class="sxs-lookup"><span data-stu-id="d1071-128">Click Transactions.</span></span>
3. <span data-ttu-id="d1071-129">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="d1071-129">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="d1071-130">Všimněte si, že pole Příjem je nastaveno na Objednáno.</span><span class="sxs-lookup"><span data-stu-id="d1071-130">Notice that the Receipt field is set to Ordered.</span></span>  
4. <span data-ttu-id="d1071-131">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="d1071-131">Close the page.</span></span>

## <a name="receive-items"></a><span data-ttu-id="d1071-132">Přijmout položky</span><span class="sxs-lookup"><span data-stu-id="d1071-132">Receive items</span></span>
1. <span data-ttu-id="d1071-133">Klikněte na položku Příjemka produktu.</span><span class="sxs-lookup"><span data-stu-id="d1071-133">Click Product receipt.</span></span>
2. <span data-ttu-id="d1071-134">Zadejte hodnotu do pole Externí příjemka produktu.</span><span class="sxs-lookup"><span data-stu-id="d1071-134">In the External product receipt field, type a value.</span></span>
3. <span data-ttu-id="d1071-135">Do pole Množství zadejte číslo, které je nižší než číslo, které je zde uvedeno.</span><span class="sxs-lookup"><span data-stu-id="d1071-135">In the Quantity field, enter a number that’s lower than the number that’s shown there.</span></span>
4. <span data-ttu-id="d1071-136">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="d1071-136">Click OK.</span></span>

## <a name="check-the-on-hand-inventory"></a><span data-ttu-id="d1071-137">Zkontrolujte množství na skladě.</span><span class="sxs-lookup"><span data-stu-id="d1071-137">Check the on-hand inventory</span></span>
1. <span data-ttu-id="d1071-138">Klepněte na položku Zásoby.</span><span class="sxs-lookup"><span data-stu-id="d1071-138">Click Inventory.</span></span>
2. <span data-ttu-id="d1071-139">Klikněte na Na skladě.</span><span class="sxs-lookup"><span data-stu-id="d1071-139">Click On-hand.</span></span>
3. <span data-ttu-id="d1071-140">Klepněte na tlačítko Přehled.</span><span class="sxs-lookup"><span data-stu-id="d1071-140">Click Overview.</span></span>
    * <span data-ttu-id="d1071-141">Položky, které byly přijaty jako zásoby dodávky ve vlastnictví dodavatele, jsou k dispozici na skladě.</span><span class="sxs-lookup"><span data-stu-id="d1071-141">The items that have been received as consignment inventory owned by the vendor are available on-hand.</span></span> <span data-ttu-id="d1071-142">Zbývající množství na objednávce doplnění stavu zásob dodávky je uvedeno v poli Celkem objednáno.</span><span class="sxs-lookup"><span data-stu-id="d1071-142">The remaining quantity on the consignment replenishment order is shown in the Ordered in total field.</span></span>  
4. <span data-ttu-id="d1071-143">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="d1071-143">Close the page.</span></span>
5. <span data-ttu-id="d1071-144">Klikněte na tlačítko Zavřít.</span><span class="sxs-lookup"><span data-stu-id="d1071-144">Click Close.</span></span>

