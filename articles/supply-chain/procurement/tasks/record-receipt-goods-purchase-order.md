--- 
title: "Zaznamenání příjmu zboží na nákupní objednávce"
description: "Tento postup popisuje, jak pořídit záznam příjmu zboží přímo na nákupní objednávce."
author: FrankDahl
manager: AnnBe
ms.date: 08/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 3a9c87b8790ed6cfe4139180f1f1785db04e7431
ms.contentlocale: cs-cz
ms.lasthandoff: 05/08/2018

---
# <a name="record-the-receipt-of-goods-on-the-purchase-order"></a><span data-ttu-id="7e9f7-103">Zaznamenání příjmu zboží na nákupní objednávce</span><span class="sxs-lookup"><span data-stu-id="7e9f7-103">Record the receipt of goods on the purchase order</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7e9f7-104">Tento postup popisuje, jak pořídit záznam příjmu zboží přímo na nákupní objednávce.</span><span class="sxs-lookup"><span data-stu-id="7e9f7-104">This procedure shows you how to record receipt of goods directly on a purchase order.</span></span> <span data-ttu-id="7e9f7-105">Dále je možné zaregistrovat příjemku produktu ve skladu a poté později ji zaznamenat na nákupní objednávce.</span><span class="sxs-lookup"><span data-stu-id="7e9f7-105">It’s also possible to register product receipt in the warehouse, and then later record it on the purchase order.</span></span> <span data-ttu-id="7e9f7-106">Tato úloha je provedena obvykle nákupčím nebo koordinátorem závazků.</span><span class="sxs-lookup"><span data-stu-id="7e9f7-106">This task is typically done by a purchasing agent or an accounts payable coordinator.</span></span> <span data-ttu-id="7e9f7-107">Příklad v této příručce lze použít v rámci ukázkových dat společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="7e9f7-107">The example shown in this guide can be used in the USMF demo data company.</span></span> <span data-ttu-id="7e9f7-108">Příklad obsahuje kroky k vytvoření jednoduché nákupní objednávky tak, že umístíte postup jako průvodce úkolem.</span><span class="sxs-lookup"><span data-stu-id="7e9f7-108">The example includes steps to create a simple purchase order so that you can play the procedure as a task guide.</span></span> <span data-ttu-id="7e9f7-109">Pokud jste použili postup na vlastních datech, můžete spustit dílčí úkol Záznam příjmu zboží.</span><span class="sxs-lookup"><span data-stu-id="7e9f7-109">If you were using the procedure on your own data, you would start at the Record receipt of goods subtask.</span></span>


## <a name="prepare-a-new-purchase-order-for-receipt-of-goods"></a><span data-ttu-id="7e9f7-110">Příprava nové nákupní objednávky pro příjem zboží</span><span class="sxs-lookup"><span data-stu-id="7e9f7-110">Prepare a new purchase order for receipt of goods</span></span>
1. <span data-ttu-id="7e9f7-111">Přejděte do nabídky Zásobování a zdroje > Nákupní objednávky > Všechny nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="7e9f7-111">Go to Procurement and sourcing > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="7e9f7-112">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="7e9f7-112">Click New.</span></span>
3. <span data-ttu-id="7e9f7-113">Zadejte hodnotu US-101 do pole Účet dodavatele.</span><span class="sxs-lookup"><span data-stu-id="7e9f7-113">In the Vendor account field, enter US-101.</span></span>
4. <span data-ttu-id="7e9f7-114">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="7e9f7-114">Click OK.</span></span>
5. <span data-ttu-id="7e9f7-115">V poli Číslo zboží zadejte 'M0001'.</span><span class="sxs-lookup"><span data-stu-id="7e9f7-115">In the Item number field, enter M0001.</span></span>
6. <span data-ttu-id="7e9f7-116">Zadejte číslo 5 do pole Množství.</span><span class="sxs-lookup"><span data-stu-id="7e9f7-116">In the Quantity field, enter 5.</span></span>
7. <span data-ttu-id="7e9f7-117">V podokně akcí klikněte na položku Nákup.</span><span class="sxs-lookup"><span data-stu-id="7e9f7-117">On the Action Pane, click Purchase.</span></span>
8. <span data-ttu-id="7e9f7-118">Klikněte na tlačítko Potvrdit.</span><span class="sxs-lookup"><span data-stu-id="7e9f7-118">Click Confirm.</span></span>

## <a name="record-receipt-of-goods"></a><span data-ttu-id="7e9f7-119">Záznam příjmu zboží</span><span class="sxs-lookup"><span data-stu-id="7e9f7-119">Record receipt of goods</span></span>
1. <span data-ttu-id="7e9f7-120">V podokně akcí klikněte na položku Přijmout.</span><span class="sxs-lookup"><span data-stu-id="7e9f7-120">On the Action Pane, click Receive.</span></span>
2. <span data-ttu-id="7e9f7-121">Klikněte na položku Příjemka produktu.</span><span class="sxs-lookup"><span data-stu-id="7e9f7-121">Click Product receipt.</span></span>
    * <span data-ttu-id="7e9f7-122">Pole Množství umožňuje nastavit různé možnosti pro množství, které chcete obdržet.</span><span class="sxs-lookup"><span data-stu-id="7e9f7-122">The Quantity field allows you to select different options for the quantity that you want to receive.</span></span> <span data-ttu-id="7e9f7-123">Pokud již bylo množství zaregistrováno ve skladu, můžete vybrat Registrované množství.</span><span class="sxs-lookup"><span data-stu-id="7e9f7-123">For example, if a quantity has previously been registered in the warehouse, you can select Registered quantity.</span></span>  <span data-ttu-id="7e9f7-124">Pro tuto hodnotu použijte hodnotu Objednané množství.</span><span class="sxs-lookup"><span data-stu-id="7e9f7-124">For this example, use the value Ordered quantity.</span></span>   
3. <span data-ttu-id="7e9f7-125">Zadejte libovolnou hodnotu do pole Příjemka produktu.</span><span class="sxs-lookup"><span data-stu-id="7e9f7-125">In the Product receipt field, type any value.</span></span>
    * <span data-ttu-id="7e9f7-126">Toto pole slouží k zadání reference, která bude použita jako doklad pro deník příjemek produktů.</span><span class="sxs-lookup"><span data-stu-id="7e9f7-126">This field is used to enter a reference that will be used as voucher for the product receipt journal.</span></span>  
4. <span data-ttu-id="7e9f7-127">Rozbalte sekci Řádky.</span><span class="sxs-lookup"><span data-stu-id="7e9f7-127">Expand the Lines section.</span></span>
5. <span data-ttu-id="7e9f7-128">Nastavte množství na hodnotu 4.</span><span class="sxs-lookup"><span data-stu-id="7e9f7-128">Set Quantity to '4'.</span></span>
    * <span data-ttu-id="7e9f7-129">Zde je možné ručně zadat množství přijaté pro každý řádek objednávky.</span><span class="sxs-lookup"><span data-stu-id="7e9f7-129">Here you are able to manually specify the quantity that is being received for each line on the order.</span></span>  
6. <span data-ttu-id="7e9f7-130">Sbalte oddíl Řádky.</span><span class="sxs-lookup"><span data-stu-id="7e9f7-130">Collapse the Lines section.</span></span>
7. <span data-ttu-id="7e9f7-131">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="7e9f7-131">Click OK.</span></span>
    * <span data-ttu-id="7e9f7-132">Zboží bylo zaznamenáno jako obdržené v nákupní objednávce a deník příjemek produktů byl vytvořen jako dokument, který tuto akci odráží.</span><span class="sxs-lookup"><span data-stu-id="7e9f7-132">The goods have now been recorded as received on the purchase order, and a product receipt journal has been created as document to reflect this.</span></span> <span data-ttu-id="7e9f7-133">Akci Příjemka produktu můžete použít ke kontrole deníků vytvořených s nákupní objednávkou a zobrazit tak, co bylo přijato, a kdy.</span><span class="sxs-lookup"><span data-stu-id="7e9f7-133">You can use the Product receipt action to review the journals created with the purchase order, and see what was received, and when.</span></span>  


