---
title: Přehled správy servisu
description: Za pomoci správy servisu můžete sestavit servisní smlouvy a předplatné služeb, zpracování servisních zakázek, dotazů odběratelů a ke správě a analýze poskytování služeb odběratelům.
author: ShylaThompson
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 451aeebd46d60251eed940016486509c4aa3f458
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4423503"
---
# <a name="service-management-overview"></a><span data-ttu-id="eb168-103">Přehled správy servisu</span><span class="sxs-lookup"><span data-stu-id="eb168-103">Service management overview</span></span>

[!include [banner](../includes/banner.md)]


<span data-ttu-id="eb168-104">Za pomoci **správy servisu** můžete sestavit servisní smlouvy a předplatné služeb, zpracování servisních zakázek, dotazů odběratelů a ke správě a analýze poskytování služeb odběratelům.</span><span class="sxs-lookup"><span data-stu-id="eb168-104">Use **Service management** to establish service agreements and service subscriptions, handle service orders and customer inquiries, and to manage and analyze the delivery of services to customers.</span></span> <span data-ttu-id="eb168-105">Můžete použít servisní smlouvy a s jejich pomocí definovat zdroje, které se používají při typické servisní návštěvě.</span><span class="sxs-lookup"><span data-stu-id="eb168-105">You can use service agreements to define the resources that are used in a typical service visit.</span></span> <span data-ttu-id="eb168-106">Servisních smluv můžete také použít pro zobrazení toho, jak jsou tyto zdroje fakturovány odběrateli.</span><span class="sxs-lookup"><span data-stu-id="eb168-106">You can also use service agreements to view how those resources are invoiced to the customer.</span></span> <span data-ttu-id="eb168-107">Servisní smlouva můžete také zahrnout smlouvu o úrovni služeb, která určuje standardní rychlost odezvy a nabízí nástroje pro záznam skutečného času.</span><span class="sxs-lookup"><span data-stu-id="eb168-107">A service agreement can also include a service level agreement that specifies standard response times, and offers tools to record the actual time.</span></span>

<span data-ttu-id="eb168-108">Můžete vytvořit servisní zakázky a spravovat tak informace o plánované a neplánované návštěvě servisního technika na pracovišti odběratele.</span><span class="sxs-lookup"><span data-stu-id="eb168-108">You can create service orders to manage information about scheduled and unscheduled visits by a service technician to a customer site.</span></span> <span data-ttu-id="eb168-109">Servisní zakázky mohou obsahovat informace jako například:</span><span class="sxs-lookup"><span data-stu-id="eb168-109">Service orders include information such as:</span></span>

1.  <span data-ttu-id="eb168-110">Počet hodin práce servisního technika</span><span class="sxs-lookup"><span data-stu-id="eb168-110">The hours of work that the service technician will perform</span></span>

2.  <span data-ttu-id="eb168-111">Typ služby nebo opravy</span><span class="sxs-lookup"><span data-stu-id="eb168-111">The type of service or repair</span></span>

3.  <span data-ttu-id="eb168-112">Položku, kterou je třeba opravit, včetně podrobností o symptomech a diagnóze</span><span class="sxs-lookup"><span data-stu-id="eb168-112">The item to repair, including details about the symptoms and diagnosis</span></span>

4.  <span data-ttu-id="eb168-113">Všechny výdaje a poplatky za služby nebo opravy</span><span class="sxs-lookup"><span data-stu-id="eb168-113">Any expenses and fees related to the service or repair</span></span>

<span data-ttu-id="eb168-114">Servisní požadavky můžete přijmout, zpracovat a zajistit jejich expedici.</span><span class="sxs-lookup"><span data-stu-id="eb168-114">You can receive, process, and dispatch service requests.</span></span> <span data-ttu-id="eb168-115">Po vytvoření servisní zakázky můžete prostřednictvím fází servisu sledovat průběh a stanovit pravidla, která určují, jaké akce budou povoleny v jednotlivých fázích.</span><span class="sxs-lookup"><span data-stu-id="eb168-115">After you have created a service order, you can use service stages to monitor progress and specify rules that control what actions are enabled in each stage.</span></span> <span data-ttu-id="eb168-116">Po dokončení servisní zakázky se můžete od zakázky odhlásit, potvrdit tak její dokončení, a následně zaúčtovat objednávku a spustit proces fakturace.</span><span class="sxs-lookup"><span data-stu-id="eb168-116">When a service order is complete, you can sign off on the order to confirm that it is complete, and then post the order to start the invoice process.</span></span>

<span data-ttu-id="eb168-117">Pomocí nástrojů pro vykazování můžete sledovat marže ze servisní objednávky a transakce za předplatné, a vytisknout popis práce a příjemky za práci.</span><span class="sxs-lookup"><span data-stu-id="eb168-117">Use the reporting tools to monitor service order margins and subscription transactions, and print work descriptions and work receipts.</span></span>

## <a name="business-processes"></a><span data-ttu-id="eb168-118">Obchodní procesy</span><span class="sxs-lookup"><span data-stu-id="eb168-118">Business processes</span></span>

<span data-ttu-id="eb168-119">Následující diagram znázorňuje obchodní procesy vysoké úrovně pro **řízení služeb** a popisuje, kde se procesy služby integrují v jiných modulech.</span><span class="sxs-lookup"><span data-stu-id="eb168-119">The following diagram illustrates the high level business processes for **Service management**, and shows where service processes integrate with other modules.</span></span>

<span data-ttu-id="eb168-120">[![Diagram obchodního procesu Správa služby](./media/sm_home_page.gif)](./media/sm_home_page.gif)</span><span class="sxs-lookup"><span data-stu-id="eb168-120">[![Service management business process diagram](./media/sm_home_page.gif)](./media/sm_home_page.gif)</span></span>

## <a name="service-management-at-a-glance"></a><span data-ttu-id="eb168-121">Řízení služeb v kostce</span><span class="sxs-lookup"><span data-stu-id="eb168-121">Service management at a glance</span></span>

|<span data-ttu-id="eb168-122">Důležité úkoly</span><span class="sxs-lookup"><span data-stu-id="eb168-122">Important tasks</span></span>           | <span data-ttu-id="eb168-123">Primární stránky</span><span class="sxs-lookup"><span data-stu-id="eb168-123">Primary pages</span></span>                         |<span data-ttu-id="eb168-124">Oblíbené sestavy</span><span class="sxs-lookup"><span data-stu-id="eb168-124">Popular reports</span></span>              |
|--------------------------|---------------------------------------|-----------------------------|
|<span data-ttu-id="eb168-125">Plnění servisních smluv</span><span class="sxs-lookup"><span data-stu-id="eb168-125">Fulfill service agreements</span></span>|<span data-ttu-id="eb168-126">Servisní smlouvy</span><span class="sxs-lookup"><span data-stu-id="eb168-126">Service agreements</span></span>                     |<span data-ttu-id="eb168-127">Marže servisní zakázky</span><span class="sxs-lookup"><span data-stu-id="eb168-127">Service order margin</span></span>         |
|<span data-ttu-id="eb168-128">Zpracování dotazů od odběratele</span><span class="sxs-lookup"><span data-stu-id="eb168-128">Handle customer inquiries</span></span> |<span data-ttu-id="eb168-129">Servisní zakázky</span><span class="sxs-lookup"><span data-stu-id="eb168-129">Service orders</span></span>                         |<span data-ttu-id="eb168-130">Popis práce</span><span class="sxs-lookup"><span data-stu-id="eb168-130">Work description</span></span>             |
|                          |<span data-ttu-id="eb168-131">Expediční vývěska</span><span class="sxs-lookup"><span data-stu-id="eb168-131">Dispatch board</span></span>                         |<span data-ttu-id="eb168-132">Transakce – předplatné</span><span class="sxs-lookup"><span data-stu-id="eb168-132">Transaction - subscription</span></span>   |
|                          |                                       |<span data-ttu-id="eb168-133">Transakce poplatků předplatného</span><span class="sxs-lookup"><span data-stu-id="eb168-133">Subscription fee transactions</span></span>|


## <a name="integration-of-service-management"></a><span data-ttu-id="eb168-134">Integrace modulu Řízení služeb</span><span class="sxs-lookup"><span data-stu-id="eb168-134">Integration of Service management</span></span>

<span data-ttu-id="eb168-135">Řízení služeb lze integrovat do těchto produktů v rámci modulů:</span><span class="sxs-lookup"><span data-stu-id="eb168-135">Service management can be integrated with the following modules:</span></span>

  - [<span data-ttu-id="eb168-136">Přehled prodeje a marketingu</span><span class="sxs-lookup"><span data-stu-id="eb168-136">Sales and marketing overview</span></span>](../sales-marketing/overview-sales-marketing.md)
  - [<span data-ttu-id="eb168-137">Lidské zdroje</span><span class="sxs-lookup"><span data-stu-id="eb168-137">Human resources</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/index)

  

