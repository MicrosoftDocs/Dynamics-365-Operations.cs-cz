---
title: Zaznamenání příjmu zboží na nákupní objednávce
description: Toto téma popisuje, jak pořídit záznam příjmu zboží přímo na nákupní objednávce.
author: RichardLuan
manager: tfehr
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchCreateOrder, InventItemIdLookupPurchase, PurchEditLines
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5cdf2b8624bf0319cd421ec11417695cfd4c78db
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5244080"
---
# <a name="record-the-receipt-of-goods-on-the-purchase-order"></a><span data-ttu-id="3988a-103">Zaznamenání příjmu zboží na nákupní objednávce</span><span class="sxs-lookup"><span data-stu-id="3988a-103">Record the receipt of goods on the purchase order</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3988a-104">Toto téma popisuje, jak pořídit záznam příjmu zboží přímo na nákupní objednávce.</span><span class="sxs-lookup"><span data-stu-id="3988a-104">This topic explains how to record receipt of goods directly on a purchase order.</span></span> <span data-ttu-id="3988a-105">Dále je možné zaregistrovat příjemku produktu ve skladu a poté později ji zaznamenat na nákupní objednávce.</span><span class="sxs-lookup"><span data-stu-id="3988a-105">It's also possible to register product receipt in the warehouse, and then later record it on the purchase order.</span></span> <span data-ttu-id="3988a-106">Tato úloha je provedena obvykle nákupčím nebo koordinátorem závazků.</span><span class="sxs-lookup"><span data-stu-id="3988a-106">This task is typically done by a purchasing agent or an accounts payable coordinator.</span></span> <span data-ttu-id="3988a-107">Příklad v této příručce lze použít v rámci ukázkových dat společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="3988a-107">The example shown in this guide can be used in the USMF demo data company.</span></span> <span data-ttu-id="3988a-108">Příklad obsahuje kroky k vytvoření jednoduché nákupní objednávky tak, že umístíte postup jako průvodce úkolem.</span><span class="sxs-lookup"><span data-stu-id="3988a-108">The example includes steps to create a simple purchase order so that you can play the procedure as a task guide.</span></span> <span data-ttu-id="3988a-109">Pokud jste použili postup na vlastních datech, můžete spustit dílčí úkol **Záznam příjmu zboží**.</span><span class="sxs-lookup"><span data-stu-id="3988a-109">If you were using the procedure on your own data, you would start at the **Record receipt of goods** subtask.</span></span>


## <a name="prepare-a-new-purchase-order-for-receipt-of-goods"></a><span data-ttu-id="3988a-110">Příprava nové nákupní objednávky pro příjem zboží</span><span class="sxs-lookup"><span data-stu-id="3988a-110">Prepare a new purchase order for receipt of goods</span></span>
1. <span data-ttu-id="3988a-111">Přejděte na **Navigační podokno > Moduly > Zásobování a zdroje > Nákupní objednávky > Všechny nákupní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="3988a-111">Go to **Navigation pane > Modules > Procurement and sourcing > Purchase orders > All purchase orders**.</span></span>
2. <span data-ttu-id="3988a-112">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="3988a-112">Select **New**.</span></span>
3. <span data-ttu-id="3988a-113">Do pole **Účet dodavatele** zadejte `US-101`.</span><span class="sxs-lookup"><span data-stu-id="3988a-113">In the **Vendor account** field, enter `US-101`.</span></span>
4. <span data-ttu-id="3988a-114">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="3988a-114">Select **OK**.</span></span>
5. <span data-ttu-id="3988a-115">Do pole **Číslo položky** zadejte `M0001`.</span><span class="sxs-lookup"><span data-stu-id="3988a-115">In the **Item number** field, enter `M0001`.</span></span>
6. <span data-ttu-id="3988a-116">Do pole **Množství** zadejte `5`.</span><span class="sxs-lookup"><span data-stu-id="3988a-116">In the **Quantity** field, enter `5`.</span></span>
7. <span data-ttu-id="3988a-117">V podokně akcí klikněte na možnost **Zakoupit**.</span><span class="sxs-lookup"><span data-stu-id="3988a-117">On the Action Pane, select **Purchase**.</span></span>
8. <span data-ttu-id="3988a-118">Vyberte **Potvrdit**.</span><span class="sxs-lookup"><span data-stu-id="3988a-118">Select **Confirm**.</span></span>

## <a name="record-receipt-of-goods"></a><span data-ttu-id="3988a-119">Záznam příjmu zboží</span><span class="sxs-lookup"><span data-stu-id="3988a-119">Record receipt of goods</span></span>
1. <span data-ttu-id="3988a-120">V podokně akcí klikněte na možnost **Přijmout**.</span><span class="sxs-lookup"><span data-stu-id="3988a-120">On the Action Pane, select **Receive**.</span></span>
2. <span data-ttu-id="3988a-121">Vyberte **Příjemka produktu**.</span><span class="sxs-lookup"><span data-stu-id="3988a-121">Select **Product receipt**.</span></span> <span data-ttu-id="3988a-122">Pole **Množství** umožňuje nastavit různé možnosti pro množství, které chcete obdržet.</span><span class="sxs-lookup"><span data-stu-id="3988a-122">The **Quantity** field allows you to select different options for the quantity that you want to receive.</span></span> <span data-ttu-id="3988a-123">Pokud již bylo množství zaregistrováno ve skladu, můžete vybrat **Registrované množství**.</span><span class="sxs-lookup"><span data-stu-id="3988a-123">For example, if a quantity has previously been registered in the warehouse, you can select **Registered quantity**.</span></span> <span data-ttu-id="3988a-124">Pro tuto hodnotu použijte hodnotu **Objednané množství**.</span><span class="sxs-lookup"><span data-stu-id="3988a-124">For this example, use the value **Ordered quantity**.</span></span>
3. <span data-ttu-id="3988a-125">Rozbalte sekci **Přehled**.</span><span class="sxs-lookup"><span data-stu-id="3988a-125">Expand the **Overview** section.</span></span>
4. <span data-ttu-id="3988a-126">Do pole **Příjemka produktu** zadejte libovolnou hodnotu.</span><span class="sxs-lookup"><span data-stu-id="3988a-126">In the **Product receipt** field, type any value.</span></span> <span data-ttu-id="3988a-127">Toto pole slouží k zadání reference, která bude použita jako doklad pro deník příjemek produktů.</span><span class="sxs-lookup"><span data-stu-id="3988a-127">This field is used to enter a reference that will be used as voucher for the product receipt journal.</span></span>  
5. <span data-ttu-id="3988a-128">Rozbalte sekci **Řádky**.</span><span class="sxs-lookup"><span data-stu-id="3988a-128">Expand the **Lines** section.</span></span>
6. <span data-ttu-id="3988a-129">Nastavte **Množství** na hodnotu 4.</span><span class="sxs-lookup"><span data-stu-id="3988a-129">Set **Quantity** to '4'.</span></span> <span data-ttu-id="3988a-130">Zde je možné ručně zadat množství přijaté pro každý řádek objednávky.</span><span class="sxs-lookup"><span data-stu-id="3988a-130">Here you are able to manually specify the quantity that is being received for each line on the order.</span></span>  
7. <span data-ttu-id="3988a-131">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="3988a-131">Select **OK**.</span></span> <span data-ttu-id="3988a-132">Zboží bylo zaznamenáno jako obdržené v nákupní objednávce a deník příjemek produktů byl vytvořen jako dokument, který tuto akci odráží.</span><span class="sxs-lookup"><span data-stu-id="3988a-132">The goods have now been recorded as received on the purchase order, and a product receipt journal has been created as document to reflect this.</span></span> <span data-ttu-id="3988a-133">Akci Příjemka produktu můžete použít ke kontrole deníků vytvořených s nákupní objednávkou a zobrazit tak, co bylo přijato, a kdy.</span><span class="sxs-lookup"><span data-stu-id="3988a-133">You can use the Product receipt action to review the journals created with the purchase order, and see what was received, and when.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]