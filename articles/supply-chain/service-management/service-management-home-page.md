---
title: "Správa servisu"
description: "Za pomoci správy servisu můžete sestavit servisní smlouvy a předplatné služeb, zpracování servisních zakázek, dotazů odběratelů a ke správě a analýze poskytování služeb odběratelům."
author: YuyuScheller
manager: AnnBe
ms.date: 05/09/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 02cdf4615e2071f2b7de2e86b6f9e6637c6e5d8d
ms.openlocfilehash: 236ab21b2d1c5a4e82270e5381d163e97437cb7f
ms.contentlocale: cs-cz
ms.lasthandoff: 05/09/2018

---


# <a name="service-management"></a><span data-ttu-id="7d5b0-103">Správa servisu</span><span class="sxs-lookup"><span data-stu-id="7d5b0-103">Service management</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="7d5b0-104">Za pomoci **správy servisu** můžete sestavit servisní smlouvy a předplatné služeb, zpracování servisních zakázek, dotazů odběratelů a ke správě a analýze poskytování služeb odběratelům.</span><span class="sxs-lookup"><span data-stu-id="7d5b0-104">Use **Service management** to establish service agreements and service subscriptions, handle service orders and customer inquiries, and to manage and analyze the delivery of services to customers.</span></span> <span data-ttu-id="7d5b0-105">Můžete použít servisní smlouvy a s jejich pomocí definovat zdroje, které se používají při typické servisní návštěvě.</span><span class="sxs-lookup"><span data-stu-id="7d5b0-105">You can use service agreements to define the resources that are used in a typical service visit.</span></span> <span data-ttu-id="7d5b0-106">Servisních smluv můžete také použít pro zobrazení toho, jak jsou tyto zdroje fakturovány odběrateli.</span><span class="sxs-lookup"><span data-stu-id="7d5b0-106">You can also use service agreements to view how those resources are invoiced to the customer.</span></span> <span data-ttu-id="7d5b0-107">Servisní smlouva můžete také zahrnout smlouvu o úrovni služeb, která určuje standardní rychlost odezvy a nabízí nástroje pro záznam skutečného času.</span><span class="sxs-lookup"><span data-stu-id="7d5b0-107">A service agreement can also include a service level agreement that specifies standard response times, and offers tools to record the actual time.</span></span>

<span data-ttu-id="7d5b0-108">Můžete vytvořit servisní zakázky a spravovat tak informace o plánované a neplánované návštěvě servisního technika na pracovišti odběratele.</span><span class="sxs-lookup"><span data-stu-id="7d5b0-108">You can create service orders to manage information about scheduled and unscheduled visits by a service technician to a customer site.</span></span> <span data-ttu-id="7d5b0-109">Servisní zakázky mohou obsahovat informace jako například:</span><span class="sxs-lookup"><span data-stu-id="7d5b0-109">Service orders include information such as:</span></span>

1.  <span data-ttu-id="7d5b0-110">Počet hodin práce servisního technika</span><span class="sxs-lookup"><span data-stu-id="7d5b0-110">The hours of work that the service technician will perform</span></span>

2.  <span data-ttu-id="7d5b0-111">Typ služby nebo opravy</span><span class="sxs-lookup"><span data-stu-id="7d5b0-111">The type of service or repair</span></span>

3.  <span data-ttu-id="7d5b0-112">Položku, kterou je třeba opravit, včetně podrobností o symptomech a diagnóze</span><span class="sxs-lookup"><span data-stu-id="7d5b0-112">The item to repair, including details about the symptoms and diagnosis</span></span>

4.  <span data-ttu-id="7d5b0-113">Všechny výdaje a poplatky za služby nebo opravy</span><span class="sxs-lookup"><span data-stu-id="7d5b0-113">Any expenses and fees related to the service or repair</span></span>

<span data-ttu-id="7d5b0-114">Odběratele mohou odeslat servisní požadavky z internetu pomocí podnikového portálu.</span><span class="sxs-lookup"><span data-stu-id="7d5b0-114">Customers can submit service requests through the Internet by using the Enterprise Portal.</span></span> <span data-ttu-id="7d5b0-115">Tyto požadavky můžete přijmout, zpracovat a zajistit jejich expedici.</span><span class="sxs-lookup"><span data-stu-id="7d5b0-115">You can receive, process, and dispatch these requests.</span></span> <span data-ttu-id="7d5b0-116">Po vytvoření servisní zakázky můžete prostřednictvím fází servisu sledovat průběh a stanovit pravidla, která určují, jaké akce budou povoleny v jednotlivých fázích.</span><span class="sxs-lookup"><span data-stu-id="7d5b0-116">After you have created a service order, you can use service stages to monitor progress and specify rules that control what actions are enabled in each stage.</span></span> <span data-ttu-id="7d5b0-117">Po dokončení servisní zakázky se můžete od zakázky odhlásit, potvrdit tak její dokončení, a následně zaúčtovat objednávku a spustit proces fakturace.</span><span class="sxs-lookup"><span data-stu-id="7d5b0-117">When a service order is complete, you can sign off on the order to confirm that it is complete, and then post the order to start the invoice process.</span></span>

<span data-ttu-id="7d5b0-118">Pomocí nástrojů pro vykazování můžete sledovat marže ze servisní objednávky a transakce za předplatné, a vytisknout popis práce a příjemky za práci.</span><span class="sxs-lookup"><span data-stu-id="7d5b0-118">Use the reporting tools to monitor service order margins and subscription transactions, and print work descriptions and work receipts.</span></span>

## <a name="business-processes"></a><span data-ttu-id="7d5b0-119">Obchodní procesy</span><span class="sxs-lookup"><span data-stu-id="7d5b0-119">Business processes</span></span>

<span data-ttu-id="7d5b0-120">Následující diagram znázorňuje vysoké úrovně obchodních procesů pro **řízení servisu** a zobrazí, kde se procesy služby integrují s jinými moduly v aplikaci Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="7d5b0-120">The following diagram illustrates the high level business processes for **Service management**, and shows where service processes integrate with other modules in Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="7d5b0-121">[![Diagram obchodního procesu Správa služby](./media/sm_home_page.gif)](./media/sm_home_page.gif)</span><span class="sxs-lookup"><span data-stu-id="7d5b0-121">[![Service management business process diagram](./media/sm_home_page.gif)](./media/sm_home_page.gif)</span></span>

## <a name="service-management-at-a-glance"></a><span data-ttu-id="7d5b0-122">Řízení služeb v kostce</span><span class="sxs-lookup"><span data-stu-id="7d5b0-122">Service management at a glance</span></span>

<table>
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7d5b0-123">Důležité úkoly</span><span class="sxs-lookup"><span data-stu-id="7d5b0-123">Important tasks</span></span></p></th>
<th><p><span data-ttu-id="7d5b0-124">Hlavní formuláře</span><span class="sxs-lookup"><span data-stu-id="7d5b0-124">Primary forms</span></span></p></th>
<th><p><span data-ttu-id="7d5b0-125">Oblíbené sestavy</span><span class="sxs-lookup"><span data-stu-id="7d5b0-125">Popular reports</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7d5b0-126">Plnění servisních smluv</span><span class="sxs-lookup"><span data-stu-id="7d5b0-126">Fulfill service agreements</span></span></a></p></td>
<td><p><span data-ttu-id="7d5b0-127"><a href="https://technet.microsoft.com/en-us/library/aa617823(v=ax.60)">Servisní smlouvy (formulář)</a></span><span class="sxs-lookup"><span data-stu-id="7d5b0-127"><a href="https://technet.microsoft.com/en-us/library/aa617823(v=ax.60)">Service agreements (form)</a></span></span></p></td>
<td><p><span data-ttu-id="7d5b0-128"><strong>Marže servisní zakázky</strong></span><span class="sxs-lookup"><span data-stu-id="7d5b0-128"><strong>Service order margin</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7d5b0-129">Zpracování dotazů od odběratele</span><span class="sxs-lookup"><span data-stu-id="7d5b0-129">Handle customer inquiries</span></span></a></p></td>
<td><p><span data-ttu-id="7d5b0-130"><a href="https://technet.microsoft.com/en-us/library/aa554361(v=ax.60)">Servisní zakázky (formulář)</a></span><span class="sxs-lookup"><span data-stu-id="7d5b0-130"><a href="https://technet.microsoft.com/en-us/library/aa554361(v=ax.60)">Service orders (form)</a></span></span></p></td>
<td><p><span data-ttu-id="7d5b0-131"><strong>Popis práce</strong></span><span class="sxs-lookup"><span data-stu-id="7d5b0-131"><strong>Work description</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="7d5b0-132"><a href="https://technet.microsoft.com/en-us/library/hh242789(v=ax.60)">Expediční vývěska (formulář)</a></span><span class="sxs-lookup"><span data-stu-id="7d5b0-132"><a href="https://technet.microsoft.com/en-us/library/hh242789(v=ax.60)">Dispatch board (form)</a></span></span></p></td>
<td><p><span data-ttu-id="7d5b0-133"><strong>Transakce – předplatné</strong></span><span class="sxs-lookup"><span data-stu-id="7d5b0-133"><strong>Transaction - subscription</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="7d5b0-134"><strong>Transakce poplatků předplatného</strong></span><span class="sxs-lookup"><span data-stu-id="7d5b0-134"><strong>Subscription fee transactions</strong></span></span></p></td>
</tr>
</tbody>
</table>


## <a name="integration-of-service-management"></a><span data-ttu-id="7d5b0-135">Integrace modulu Řízení služeb</span><span class="sxs-lookup"><span data-stu-id="7d5b0-135">Integration of Service management</span></span>

<span data-ttu-id="7d5b0-136">Řízení služeb lze integrovat s následujícími moduly v aplikaci Microsoft Dynamics 365 for Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="7d5b0-136">Service management can be integrated with the following modules in Microsoft Dynamics 365 for Finance and Operations:</span></span>

  - [<span data-ttu-id="7d5b0-137">Prodej a marketing</span><span class="sxs-lookup"><span data-stu-id="7d5b0-137">Sales and marketing</span></span>](../sales-marketing/overview-sales-marketing.md)

  - [<span data-ttu-id="7d5b0-138">Lidské zdroje</span><span class="sxs-lookup"><span data-stu-id="7d5b0-138">Human resources</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/index)

  


