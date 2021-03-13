---
title: Vytvoření nové zakázky na doplnění stavu zásob dodávky
description: Tto téma vysvětluje, jak vytvořit objednávku doplnění stavu zásob dodávky, kde můžete sledovat očekávanou dodávku od dodavatele do skladu dodávky.
author: RichardLuan
manager: tfehr
ms.date: 08/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ConsignmentReplenishmentOrder, ConsignmentReplenishmentOrderCreate, InventTrans, ConsignmentDraftReplenishmentOrderJournal, InventOnhandMovement, InventOnhandItem, InventItemIdLookupSimple, ConsignmentProductReceiptJournal, ConsignmentReplenishmentOrderLineQuantity
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b27b4d87add38fac29c9eba4ace08af91f9faca1
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/16/2021
ms.locfileid: "5020147"
---
# <a name="create-a-consignment-replenishment-order"></a><span data-ttu-id="2c5ed-103">Vytvoření nové zakázky na doplnění stavu zásob dodávky</span><span class="sxs-lookup"><span data-stu-id="2c5ed-103">Create a consignment replenishment order</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2c5ed-104">Tto téma vysvětluje, jak vytvořit objednávku doplnění stavu zásob dodávky, kde můžete sledovat očekávanou dodávku od dodavatele do skladu dodávky.</span><span class="sxs-lookup"><span data-stu-id="2c5ed-104">This topic explains how to create a consignment replenishment order where you can track the expected delivery from a vendor into your consignment inventory.</span></span> <span data-ttu-id="2c5ed-105">Také ukazuje, jak zaznamenávat příjem produktů tak, aby byla zásoba dodávky registrována jako zásoby na skladě ve vlastnictví dodavatele.</span><span class="sxs-lookup"><span data-stu-id="2c5ed-105">It also shows how to record a receipt of products so that the consignment inventory is registered as on-hand inventory owned by the vendor.</span></span> <span data-ttu-id="2c5ed-106">Tuto proceduru obvykle provádí zásobovací pracovník.</span><span class="sxs-lookup"><span data-stu-id="2c5ed-106">This procedure would typically be done by a procurement professional.</span></span> <span data-ttu-id="2c5ed-107">Tohoto průvodce můžete použít s ukázkových dat společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="2c5ed-107">You can use this guide in demo data company USMF.</span></span> <span data-ttu-id="2c5ed-108">Tento postup je určen pro funkci, která byla přidána do Dynamics 365 for Operations, verze 1611.</span><span class="sxs-lookup"><span data-stu-id="2c5ed-108">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>

## <a name="create-a-consignment-replenishment-order"></a><span data-ttu-id="2c5ed-109">Vytvoření nové zakázky na doplnění stavu zásob dodávky</span><span class="sxs-lookup"><span data-stu-id="2c5ed-109">Create a consignment replenishment order</span></span>
1. <span data-ttu-id="2c5ed-110">V navigačním podokně přejděte na **Moduly > Zásobování a zdroje > Stav zásob dodávky > Zakázky na doplnění stavu zásob dodávky**.</span><span class="sxs-lookup"><span data-stu-id="2c5ed-110">In the navigation pane, go to **Modules > Procurement and sourcing > Consignment > Consignment replenishment orders**.</span></span>
2. <span data-ttu-id="2c5ed-111">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="2c5ed-111">Select **New**.</span></span>
3. <span data-ttu-id="2c5ed-112">V poli **Účet dodavatele** vyberte dodavatele **US-104** (musíte vybrat dodavatele, který je zaregistrován jako vlastník na stránce **Vlastníci zásob**).</span><span class="sxs-lookup"><span data-stu-id="2c5ed-112">In the **Vendor account** field, select vendor **US-104** (you must select a vendor that's registered as an owner in the **inventory owners** page).</span></span> 
4. <span data-ttu-id="2c5ed-113">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="2c5ed-113">Select **OK**.</span></span>
5. <span data-ttu-id="2c5ed-114">Vyberte **Přidat řádek**.</span><span class="sxs-lookup"><span data-stu-id="2c5ed-114">Select **Add line**.</span></span>
6. <span data-ttu-id="2c5ed-115">Do pole **Číslo položky** zadejte `M9211CI` (je nutné vybrat položku, která je nastavena pro zásoby dodávky).</span><span class="sxs-lookup"><span data-stu-id="2c5ed-115">In the **Item number** field, type `M9211CI` (you must select an item that is set up for consignment inventory).</span></span>
7. <span data-ttu-id="2c5ed-116">Zadejte číslo do pole **Množství**.</span><span class="sxs-lookup"><span data-stu-id="2c5ed-116">In the **Quantity** field, enter a number.</span></span>
8. <span data-ttu-id="2c5ed-117">Zadejte datum do pole **Požadované datum dodání**.</span><span class="sxs-lookup"><span data-stu-id="2c5ed-117">In the **Requested delivery date** field, enter a date.</span></span> <span data-ttu-id="2c5ed-118">Požadované a potvrzené datum používá modul MRP pro očekávané přijetí zboží.</span><span class="sxs-lookup"><span data-stu-id="2c5ed-118">The requested and confirmed dates are used by the MRP engine for the expected arrival of the goods.</span></span>  
9. <span data-ttu-id="2c5ed-119">Zadejte datum do pole **Potvrzené datum dodání**.</span><span class="sxs-lookup"><span data-stu-id="2c5ed-119">In the **Confirmed delivery date** field, enter a date.</span></span>
10. <span data-ttu-id="2c5ed-120">Rozbalte sekci **Podrobnosti řádku**.</span><span class="sxs-lookup"><span data-stu-id="2c5ed-120">Expand the **Line details** section.</span></span>
11. <span data-ttu-id="2c5ed-121">Vyberte kartu **Dimenze zásob**.</span><span class="sxs-lookup"><span data-stu-id="2c5ed-121">Select the **Inventory dimensions** tab.</span></span>
12. <span data-ttu-id="2c5ed-122">Chcete-li zobrazit vlastníka v poli **Vlastník dimenze zásob**, aktualizujte stránku.</span><span class="sxs-lookup"><span data-stu-id="2c5ed-122">To show the owner in the **Inventory dimensions owner** field, refresh the page.</span></span> <span data-ttu-id="2c5ed-123">Dodavatel US-104 je nyní uveden jako vlastník.</span><span class="sxs-lookup"><span data-stu-id="2c5ed-123">Vendor US-104 is now listed as the owner.</span></span>  

## <a name="check-the-inventory-transaction-status"></a><span data-ttu-id="2c5ed-124">Zkontrolujte stav transakce zásob.</span><span class="sxs-lookup"><span data-stu-id="2c5ed-124">Check the inventory transaction status</span></span>
1. <span data-ttu-id="2c5ed-125">Vyberte **skladový model**.</span><span class="sxs-lookup"><span data-stu-id="2c5ed-125">Select **Inventory**.</span></span>
2. <span data-ttu-id="2c5ed-126">Vyberte **Transakce**.</span><span class="sxs-lookup"><span data-stu-id="2c5ed-126">Select **Transactions**.</span></span>
3. <span data-ttu-id="2c5ed-127">Všimněte si, že pole **Příjemka** je nastaveno na **Objednáno** v požadovaném řádku.</span><span class="sxs-lookup"><span data-stu-id="2c5ed-127">In the desired row, notice that the **Receipt** field is set to **Ordered**.</span></span>  
4. <span data-ttu-id="2c5ed-128">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="2c5ed-128">Close the page.</span></span>

## <a name="receive-items"></a><span data-ttu-id="2c5ed-129">Přijmout položky</span><span class="sxs-lookup"><span data-stu-id="2c5ed-129">Receive items</span></span>
1. <span data-ttu-id="2c5ed-130">Vyberte **Příjemka produktu**.</span><span class="sxs-lookup"><span data-stu-id="2c5ed-130">Select **Product receipt**.</span></span>
2. <span data-ttu-id="2c5ed-131">Zadejte hodnotu do pole **Externí příjemka produktu**.</span><span class="sxs-lookup"><span data-stu-id="2c5ed-131">In the **External product receipt** field, type a value.</span></span>
3. <span data-ttu-id="2c5ed-132">Do pole **Množství** zadejte číslo, které je nižší než číslo, které je zde uvedeno.</span><span class="sxs-lookup"><span data-stu-id="2c5ed-132">In the **Quantity** field, enter a number that's lower than the number that's shown there.</span></span> 
4. <span data-ttu-id="2c5ed-133">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="2c5ed-133">Select **OK**.</span></span>

## <a name="check-the-on-hand-inventory"></a><span data-ttu-id="2c5ed-134">Zkontrolujte množství na skladě.</span><span class="sxs-lookup"><span data-stu-id="2c5ed-134">Check the on-hand inventory</span></span>
1. <span data-ttu-id="2c5ed-135">Vyberte **skladový model**.</span><span class="sxs-lookup"><span data-stu-id="2c5ed-135">Select **Inventory**.</span></span>
2. <span data-ttu-id="2c5ed-136">Vyberte **Na skladě**.</span><span class="sxs-lookup"><span data-stu-id="2c5ed-136">Select **On-hand**.</span></span>
3. <span data-ttu-id="2c5ed-137">Vyberte **Přehled**.</span><span class="sxs-lookup"><span data-stu-id="2c5ed-137">Select **Overview**.</span></span> <span data-ttu-id="2c5ed-138">Položky, které byly přijaty jako zásoby dodávky ve vlastnictví dodavatele, jsou k dispozici na skladě.</span><span class="sxs-lookup"><span data-stu-id="2c5ed-138">The items that have been received as consignment inventory owned by the vendor are available on-hand.</span></span> <span data-ttu-id="2c5ed-139">Zbývající množství na objednávce doplnění stavu zásob dodávky je uvedeno v poli **Celkem objednáno**.</span><span class="sxs-lookup"><span data-stu-id="2c5ed-139">The remaining quantity on the consignment replenishment order is shown in the **Ordered in total** field.</span></span>  
4. <span data-ttu-id="2c5ed-140">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="2c5ed-140">Close the page.</span></span>

