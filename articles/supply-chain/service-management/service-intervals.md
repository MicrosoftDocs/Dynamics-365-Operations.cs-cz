---
title: Intervaly servisu
description: Servisní interval určuje, jak často jsou pro řádky servisní smlouvy vytvářeny řádky servisní zakázky při automatickém vytváření servisních zakázek.
author: ShylaThompson
manager: tfehr
ms.date: 02/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: da43f914af75a7f85dc43d3ab1d16abcd82561c1
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5242978"
---
# <a name="service-intervals"></a><span data-ttu-id="340c0-103">Intervaly servisu</span><span class="sxs-lookup"><span data-stu-id="340c0-103">Service intervals</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="340c0-104">Interval servisní smlouvy určuje, jak často jsou pro řádky servisní smlouvy vytvářeny řádky servisní zakázky při automatickém vytváření servisních zakázek.</span><span class="sxs-lookup"><span data-stu-id="340c0-104">The service agreement interval indicates the frequency with which service order lines are created for service agreement lines when you create service orders automatically.</span></span>

<span data-ttu-id="340c0-105">Pokud vytváříte servisní zakázky automaticky, řádky servisní zakázky se vytvářejí podle intervalu, který jste zadali v řádku servisní smlouvy od počátečního data řádku smlouvy.</span><span class="sxs-lookup"><span data-stu-id="340c0-105">When you create service orders automatically, service order lines are created according to the interval that you have specified for the service agreement line from the start date of the agreement line.</span></span>

<span data-ttu-id="340c0-106">Pokud je pole **Interval** řádku servisní smlouvy na stránce **Servisní smlouvy** prázdné, řádek představuje jednorázovou událost a nepoužívá se při opakovaném vytváření servisních zakázek.</span><span class="sxs-lookup"><span data-stu-id="340c0-106">If the **Interval** field of a service agreement line in the **Service agreements** page is blank, the line is a one-time event, and it is not used to create service orders repeatedly.</span></span>

## <a name="example"></a><span data-ttu-id="340c0-107">Příklad</span><span class="sxs-lookup"><span data-stu-id="340c0-107">Example</span></span>

<span data-ttu-id="340c0-108">Tento příklad ukazuje, jaký vliv má interval servisu na řádky servisní smlouvy a servisní zakázky na servisní zakázce.</span><span class="sxs-lookup"><span data-stu-id="340c0-108">This example illustrates how a service interval will affect service agreement lines and service order lines on a service order.</span></span>

### <a name="create-a-service-agreement"></a><span data-ttu-id="340c0-109">Vytvoření servisní smlouvy</span><span class="sxs-lookup"><span data-stu-id="340c0-109">Create a service agreement</span></span>

<span data-ttu-id="340c0-110">Nejprve vytvořte servisní smlouvu a nastavte možnost **Kombinace servisních zakázek** na **Podle servisní smlouvy**.</span><span class="sxs-lookup"><span data-stu-id="340c0-110">First, you create a service agreement and set the **Combine service orders** option to **By service agreement**.</span></span>

1. <span data-ttu-id="340c0-111">Klikněte na **Servisní smlouvy**</span><span class="sxs-lookup"><span data-stu-id="340c0-111">Click **Service agreements**</span></span>
2. <span data-ttu-id="340c0-112">V **podokně akcí** na kartě **Servisní smlouva** ve skupině **Nová** klikněte na **Servisní smlouva** a vytvořte novou servisní smlouvu.</span><span class="sxs-lookup"><span data-stu-id="340c0-112">On the **Action Pane**, on the **Service agreement** tab, in the **New** group, click **Service agreement** to create a new service agreement.</span></span>
3. <span data-ttu-id="340c0-113">Zadejte popis, vyberte projekt v poli **ID projektu** a zadejte datum do pole **Počáteční datum**.</span><span class="sxs-lookup"><span data-stu-id="340c0-113">Enter a description, select a project in the **Project ID** field, and enter a date in the **Start date** field.</span></span>
4. <span data-ttu-id="340c0-114">V poli **Kombinace servisních zakázek** vyberte **Podle servisní smlouvy**.</span><span class="sxs-lookup"><span data-stu-id="340c0-114">In the **Combine service orders** field, select **By service agreement**.</span></span>

<span data-ttu-id="340c0-115">Nyní jste vytvořili následující servisní smlouvu:</span><span class="sxs-lookup"><span data-stu-id="340c0-115">You have now created the following service agreement:</span></span>

| <span data-ttu-id="340c0-116">Project</span><span class="sxs-lookup"><span data-stu-id="340c0-116">Project</span></span>      | <span data-ttu-id="340c0-117">Počáteční datum</span><span class="sxs-lookup"><span data-stu-id="340c0-117">Start date</span></span>                                                                         |
|--------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="340c0-118">Váš projekt</span><span class="sxs-lookup"><span data-stu-id="340c0-118">Your project</span></span> | <span data-ttu-id="340c0-119">Datum, které jste určili pro projekt.</span><span class="sxs-lookup"><span data-stu-id="340c0-119">The date you specified for the project.</span></span> <span data-ttu-id="340c0-120">V tomto příkladu se používá aktuální datum.</span><span class="sxs-lookup"><span data-stu-id="340c0-120">In this example, the current date is used.</span></span> |

### <a name="create-a-service-agreement-line"></a><span data-ttu-id="340c0-121">Vytvoření řádku servisní smlouvy</span><span class="sxs-lookup"><span data-stu-id="340c0-121">Create a service agreement line</span></span>

<span data-ttu-id="340c0-122">Dále vytvoříte řádek servisní smlouvy s typem transakce **Hodina**.</span><span class="sxs-lookup"><span data-stu-id="340c0-122">Next, you create a service agreement line that has the transaction type **Hour**.</span></span>

<span data-ttu-id="340c0-123">Pro dokončení této části příkladu musíte vytvořit interval servisu 10 dní na stránce **Servisní intervaly**.</span><span class="sxs-lookup"><span data-stu-id="340c0-123">To complete this part of the example, you must create a service interval of 10 days in the **Service intervals** page.</span></span> 

1. <span data-ttu-id="340c0-124">Vyberte servisní smlouvu, kterou jste právě vytvořili.</span><span class="sxs-lookup"><span data-stu-id="340c0-124">Select the service agreement that you just created.</span></span> 
2. <span data-ttu-id="340c0-125">Na pevné záložce **Řádky** klikněte na tlačítko **Přidat** a vytvořte nový řádek v dolním podokně stránky **Servisní smlouvy**.</span><span class="sxs-lookup"><span data-stu-id="340c0-125">On the **Lines** FastTab, click the **Add** button to create a new line in the lower pane of the **Service agreements** page.</span></span>
3. <span data-ttu-id="340c0-126">V poli **Typ transakce** zvolte **Hodina**.</span><span class="sxs-lookup"><span data-stu-id="340c0-126">In the **Transaction type** field, select **Hour**.</span></span>
4. <span data-ttu-id="340c0-127">V poli **Pracovník** vyberte pracovníka, který dodá servis.</span><span class="sxs-lookup"><span data-stu-id="340c0-127">In the **Worker** field, select the worker who will deliver the service.</span></span>
5. <span data-ttu-id="340c0-128">V poli **Interval servisu** vyberte interval 10 dní.</span><span class="sxs-lookup"><span data-stu-id="340c0-128">In the **Service interval** field, select the 10 days interval.</span></span>

<span data-ttu-id="340c0-129">Nyní jste vytvořili řádek servisní smlouvy s následujícími informacemi:</span><span class="sxs-lookup"><span data-stu-id="340c0-129">You have now created a service agreement line with the following information:</span></span>

| <span data-ttu-id="340c0-130">typ transakce</span><span class="sxs-lookup"><span data-stu-id="340c0-130">Transaction type</span></span> | <span data-ttu-id="340c0-131">Počáteční datum</span><span class="sxs-lookup"><span data-stu-id="340c0-131">Start date</span></span>                               | <span data-ttu-id="340c0-132">Interval servisu</span><span class="sxs-lookup"><span data-stu-id="340c0-132">Service interval</span></span> |
|------------------|------------------------------------------|------------------|
| <span data-ttu-id="340c0-133">Hodina</span><span class="sxs-lookup"><span data-stu-id="340c0-133">Hour</span></span>             | <span data-ttu-id="340c0-134">Aktuální datum.</span><span class="sxs-lookup"><span data-stu-id="340c0-134">The current date.</span></span>                        | <span data-ttu-id="340c0-135">Každých 10 dní</span><span class="sxs-lookup"><span data-stu-id="340c0-135">Every 10 days</span></span>    |
| <span data-ttu-id="340c0-136">Pracovní podproces</span><span class="sxs-lookup"><span data-stu-id="340c0-136">Worker</span></span>           | <span data-ttu-id="340c0-137">Pracovník, který provede servis.</span><span class="sxs-lookup"><span data-stu-id="340c0-137">The worker who will perform the service.</span></span> |                  |

<span data-ttu-id="340c0-138">Pro řádek není určené žádné časové okno.</span><span class="sxs-lookup"><span data-stu-id="340c0-138">There is no time window specified for the line.</span></span> 

### <a name="create-planned-service-orders"></a><span data-ttu-id="340c0-139">Vytvoření plánovaných servisních zakázek</span><span class="sxs-lookup"><span data-stu-id="340c0-139">Create planned service orders</span></span>

<span data-ttu-id="340c0-140">Nyní můžete vytvořit plánované servisní zakázky nebo řádky servisních zakázek nadcházející měsíc.</span><span class="sxs-lookup"><span data-stu-id="340c0-140">You can now create planned service orders and service order lines for the coming month.</span></span>

1. <span data-ttu-id="340c0-141">Na stránce **Servisní smlouvy** v **podokně akcí** na kartě **Dodat** klikněte na **Plánované servisní zakázky**.</span><span class="sxs-lookup"><span data-stu-id="340c0-141">In the **Service agreements** page, on the **Action Pane**, on the **Deliver** tab, click **Planned service orders**.</span></span>
2. <span data-ttu-id="340c0-142">Na stránce **Vytváření servisních zakázek** zadejte aktuální datum do pole **Od data** a datum, které je od aktuálního data za měsíc zadejte do pole **Do data**.</span><span class="sxs-lookup"><span data-stu-id="340c0-142">In the **Create service orders** page, enter the current date in the **From date** field and a date that is one month from the current date in the **To date** field.</span></span>
3. <span data-ttu-id="340c0-143">Nastavte posuvník **Hodina** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="340c0-143">Set the **Hour** slider to **Yes**.</span></span> 
4. <span data-ttu-id="340c0-144">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="340c0-144">Click **OK**.</span></span>

<span data-ttu-id="340c0-145">Vzhledem k tomu, že servisní zakázka neobsahuje žádné seskupení (definováno možností **Podle servisní smlouvy** v poli **Kombinace servisních zakázek**), pro jednu servisní zakázku je vytvořený jeden řádek.</span><span class="sxs-lookup"><span data-stu-id="340c0-145">Because there is no grouping on the service order (defined by the **By service agreement** option in the **Combine service orders** field), one service order line is created per service order.</span></span>

### <a name="service-orders-created"></a><span data-ttu-id="340c0-146">Vytvořené servisní zakázky</span><span class="sxs-lookup"><span data-stu-id="340c0-146">Service orders created</span></span>

<span data-ttu-id="340c0-147">Tři řádky servisních zakázek byly vytvořeny v tomto časovém rozsahu, který jste zadali v dialogovém okně **Vytváření servisních zakázek**.</span><span class="sxs-lookup"><span data-stu-id="340c0-147">Three service order lines have been created within the time frame that you specified in the **Create service orders** dialog box.</span></span> <span data-ttu-id="340c0-148">Můžete zobrazit řádky servisní zakázky na stránce **Servisní smlouvy** (**Podokno akcí** \> karta **Dodat** tlačítko \>**Zobrazit**).</span><span class="sxs-lookup"><span data-stu-id="340c0-148">You can view the service order lines in the **Service agreements** page (**Action Pane** \> **Deliver** tab \>**View** button).</span></span>

## <a name="related-topics"></a><span data-ttu-id="340c0-149">Související témata</span><span class="sxs-lookup"><span data-stu-id="340c0-149">Related topics</span></span>

[<span data-ttu-id="340c0-150">Nastavení intervalů servisu</span><span class="sxs-lookup"><span data-stu-id="340c0-150">Set up service intervals</span></span>](set-up-service-intervals.md)  



[!INCLUDE[footer-include](../../includes/footer-banner.md)]