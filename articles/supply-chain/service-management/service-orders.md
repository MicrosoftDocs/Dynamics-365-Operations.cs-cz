---
title: Servisní zakázky
description: Servisní zakázka představuje návštěvu servisního technika u zákazníka ve stanovený den.
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b4d347556d25831bb3f9175e8606e0b41d98bdd8
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/12/2019
ms.locfileid: "1743236"
---
# <a name="service-orders"></a><span data-ttu-id="35a95-103">Servisní zakázky</span><span class="sxs-lookup"><span data-stu-id="35a95-103">Service orders</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="35a95-104">Servisní zakázka představuje návštěvu servisního technika u zákazníka ve stanovený den.</span><span class="sxs-lookup"><span data-stu-id="35a95-104">A service order represents a visit that a service technician makes to a customer site on a specific date.</span></span> <span data-ttu-id="35a95-105">Každá servisní zakázka se skládá z jednoho nebo více řádků servisní zakázky.</span><span class="sxs-lookup"><span data-stu-id="35a95-105">Each service order consists of one or more service order lines.</span></span> <span data-ttu-id="35a95-106">Řádky servisní zakázky představují hodiny práce, kterou musí provést servisní technik, a související položky, výdaje a poplatky.</span><span class="sxs-lookup"><span data-stu-id="35a95-106">Service order lines represent the hours of work that must be performed by the service technician, and the related items, expenses, and fees.</span></span>

<span data-ttu-id="35a95-107">K řádku servisní zakázky můžete připojit úkoly a předměty.</span><span class="sxs-lookup"><span data-stu-id="35a95-107">You can attach tasks and objects to a service order line.</span></span> <span data-ttu-id="35a95-108">Poté můžete seskupit řádky servisní zakázky podle úkolu nebo předmětu.</span><span class="sxs-lookup"><span data-stu-id="35a95-108">You can then group service order lines by task or by object.</span></span> <span data-ttu-id="35a95-109">K řádkům servisních zakázek také můžete připojit skladové položky.</span><span class="sxs-lookup"><span data-stu-id="35a95-109">You can also attach items that are listed in inventory to service order lines.</span></span>

## <a name="create-service-orders"></a><span data-ttu-id="35a95-110">Vytváření servisních zakázek</span><span class="sxs-lookup"><span data-stu-id="35a95-110">Create service orders</span></span>

<span data-ttu-id="35a95-111">Servisní zakázky jsou vytvářeny na základě servisní smlouvy a řádků obsažených v této smlouvě.</span><span class="sxs-lookup"><span data-stu-id="35a95-111">You can create service orders based on a service agreement and the lines that are contained in that agreement.</span></span> <span data-ttu-id="35a95-112">Můžete však vytvořit servisní zakázky, které jsou asociovány se servisní smlouvou pouze za období, které je určeno ve smlouvě.</span><span class="sxs-lookup"><span data-stu-id="35a95-112">However, you can create service orders that are associated with a service agreement only in the period that is specified in the agreement.</span></span> <span data-ttu-id="35a95-113">Například pokud je servisní smlouva platná pro kalendářní rok 2011, můžete servisní zakázky vytvářet pro smlouvu z 1. ledna 2011 a 31. prosince 2011.</span><span class="sxs-lookup"><span data-stu-id="35a95-113">For example, if a service agreement is valid for the 2011 calendar year, you can create service orders for the agreement from January 1, 2011, and December 31, 2011.</span></span>

<span data-ttu-id="35a95-114">Servisní zakázky lze také vytvořit samostatně jejich přidružení ke smlouvě.</span><span class="sxs-lookup"><span data-stu-id="35a95-114">You can also create service orders individually, without associating them with an agreement.</span></span> <span data-ttu-id="35a95-115">Tyto servisní zakázky lze použít ke zpracování neplánovaných nebo jednorázových servisních zásahů.</span><span class="sxs-lookup"><span data-stu-id="35a95-115">These service orders can be used to handle unscheduled or one-time service visits.</span></span> <span data-ttu-id="35a95-116">Například v březnu se zákazník rozhodne, že potřebuje nad rámec servisních zásahů, které jsou uvedené v servisní smlouvě, provést servis dvou strojů.</span><span class="sxs-lookup"><span data-stu-id="35a95-116">For example, in the month of March, your customer wants service to be performed on two machines, in addition to the machines that are specified in the service agreement.</span></span> <span data-ttu-id="35a95-117">Pro tento úkol lze servisní zakázky vytvořit bez jejich přidružení k servisním smlouvám.</span><span class="sxs-lookup"><span data-stu-id="35a95-117">For this task, you create service orders but do not associate them with an agreement.</span></span>


> [!NOTE]
> <P><span data-ttu-id="35a95-118">K vytvoření servisních zakázek, které nejsou spojeny se servisní smlouvou, je nutné zaškrtnout políčko <STRONG>Povolit bez servisní smlouvy</STRONG> ve formuláři <STRONG>parametry správy servisu</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="35a95-118">To create service orders that are not associated with a service agreement, you must select the <STRONG>Allow without service agreement</STRONG> check box in the <STRONG>Service management parameters</STRONG> form.</span></span></P>

<span data-ttu-id="35a95-119">**Scénář**</span><span class="sxs-lookup"><span data-stu-id="35a95-119">**Scenario**</span></span>

<span data-ttu-id="35a95-120">Následující scénář popisuje jinou situaci, kdy je užitečné nejdříve vytvořit servisní zakázku, která není přidružena k servisní smlouvě.</span><span class="sxs-lookup"><span data-stu-id="35a95-120">The following scenario describes another situation where it is useful to create a service order that is not associated with a service agreement.</span></span>

<span data-ttu-id="35a95-121">Dispečerka společnosti přijme telefonickou žádost o servis výtahu.</span><span class="sxs-lookup"><span data-stu-id="35a95-121">The company dispatcher receives a call requesting emergency service on an elevator.</span></span> <span data-ttu-id="35a95-122">Neexistuje žádný čas nastavení servisní smlouvy a projektu služby.</span><span class="sxs-lookup"><span data-stu-id="35a95-122">There is no time to set up a service agreement and a project for the service.</span></span> <span data-ttu-id="35a95-123">Proto dispečerka vytvoří servisní zakázku přímo ve formuláři **servisní zakázky**, připojí servisní zakázku ke stávajícímu projektu a vytvoří řádky servisní zakázky.</span><span class="sxs-lookup"><span data-stu-id="35a95-123">Therefore, the dispatcher creates a service order directly in the **Service orders** form, attaches the service order to an existing project, and creates the service order lines.</span></span> <span data-ttu-id="35a95-124">Kvůli zaznamenání práce, která nesouvisí se servisní smlouvou, může dispečerka vytvořit vztah s úkolem nebo předmětem stávající servisní zakázky.</span><span class="sxs-lookup"><span data-stu-id="35a95-124">The dispatcher also creates a task or object relation for an existing service order, to record work that is not related to the service agreement.</span></span> <span data-ttu-id="35a95-125">Další informace naleznete v tématu [ruční vytvoření servisních zakázek](create-service-orders-manually.md) a [vytvoření vztahů servisních úloh](create-service-task-relations.md).</span><span class="sxs-lookup"><span data-stu-id="35a95-125">For more information, see [Create service orders manually](create-service-orders-manually.md) and [Create service task relations](create-service-task-relations.md).</span></span>

## <a name="monitor-the-progress-of-service-orders"></a><span data-ttu-id="35a95-126">Sledování průběhu servisních zakázek</span><span class="sxs-lookup"><span data-stu-id="35a95-126">Monitor the progress of service orders</span></span>

<span data-ttu-id="35a95-127">Pokud chcete monitorovat pokrok servisní zakázky v různých týmech a pracovních procesech, můžete nastavit systém fází a kódů důvodu servisních zakázek.</span><span class="sxs-lookup"><span data-stu-id="35a95-127">To monitor the progress of a sales order through the different teams and work processes, you can set up a system of stages and reason codes for service orders.</span></span> <span data-ttu-id="35a95-128">Pro každou fázi můžete zadat povolené akce:</span><span class="sxs-lookup"><span data-stu-id="35a95-128">For each stage, you can specify the actions that are allowed.</span></span> <span data-ttu-id="35a95-129">Další informace naleznete v tématu [Vytvoření kódů důvodu](create-reason-codes.md).</span><span class="sxs-lookup"><span data-stu-id="35a95-129">For more information, see [Create reason codes](create-reason-codes.md).</span></span>

<span data-ttu-id="35a95-130">**Příklad**</span><span class="sxs-lookup"><span data-stu-id="35a95-130">**Example**</span></span>

<span data-ttu-id="35a95-131">Servisní zakázky je schválena dispečerkou.</span><span class="sxs-lookup"><span data-stu-id="35a95-131">A service order is approved by the dispatcher.</span></span> <span data-ttu-id="35a95-132">Ta provede aktualizaci fáze servisní zakázky a uvede kód důvodu, který označuje, že servisní zakázka byla uvolněna pro servisního technika.</span><span class="sxs-lookup"><span data-stu-id="35a95-132">The dispatcher updates the stage of the service order and specifies a reason code that indicates that the service order has been released to the service technician.</span></span> <span data-ttu-id="35a95-133">Technik navštíví zákazníka a realizuje servisní zakázku.</span><span class="sxs-lookup"><span data-stu-id="35a95-133">The technician goes to the customer site and performs the service.</span></span>

## <a name="specify-item-requirements-for-service-orders"></a><span data-ttu-id="35a95-134">Určení požadavků položky pro servisní zakázky</span><span class="sxs-lookup"><span data-stu-id="35a95-134">Specify item requirements for service orders</span></span>

<span data-ttu-id="35a95-135">Můžete určit skladové položky, které jsou požadovány pro servisní zakázky.</span><span class="sxs-lookup"><span data-stu-id="35a95-135">You can specify the inventory items that are required for service orders.</span></span> <span data-ttu-id="35a95-136">Servisní zakázka však musí být spojena s projektem.</span><span class="sxs-lookup"><span data-stu-id="35a95-136">However, the service order must be associated with a project.</span></span> <span data-ttu-id="35a95-137">Požadavky zboží pro objednávky služeb jsou zpracovávány prostřednictvím projektu.</span><span class="sxs-lookup"><span data-stu-id="35a95-137">Item requirements for service orders are processed through a project.</span></span> 

<span data-ttu-id="35a95-138">**Příklad**</span><span class="sxs-lookup"><span data-stu-id="35a95-138">**Example**</span></span>

<span data-ttu-id="35a95-139">Servisní zakázky, které jsou vytvořené ze servisních smluv, zpracuje dispečerka.</span><span class="sxs-lookup"><span data-stu-id="35a95-139">The service orders that are created from the service agreement are processed by the dispatcher.</span></span> <span data-ttu-id="35a95-140">U první servisní zakázky dispečerka zjistí, že servisní technik potřebuje důležitý náhradní díl, který momentálně není na skladě.</span><span class="sxs-lookup"><span data-stu-id="35a95-140">For the first service order, the dispatcher realizes that the service technician requires an important spare part that is not in the on-hand inventory.</span></span> <span data-ttu-id="35a95-141">Vytvoří proto pro náhradní díl požadavek na položku přímo ze servisní zakázky.</span><span class="sxs-lookup"><span data-stu-id="35a95-141">Therefore, the dispatcher creates an item requirement for the spare part directly from the service order.</span></span>

## <a name="move-and-post-lines"></a><span data-ttu-id="35a95-142">Přesun a zaúčtování řádků</span><span class="sxs-lookup"><span data-stu-id="35a95-142">Move and post lines</span></span>

<span data-ttu-id="35a95-143">Servisní technik vrátí servisním zásahu upraví a aktualizuje řádky servisní zakázky.</span><span class="sxs-lookup"><span data-stu-id="35a95-143">A service technician returns from a service visit, and then modifies and updates the service order lines.</span></span> <span data-ttu-id="35a95-144">Při servisním zásahu technik provedl servisní úkon, který je naplánován na příští servisní návštěvu.</span><span class="sxs-lookup"><span data-stu-id="35a95-144">During the service visit, the technician performed a service job that was scheduled for the next service visit.</span></span> <span data-ttu-id="35a95-145">Technik proto přesune řádky z dalšího servisního zásahu do aktuálního servisního zásahu.</span><span class="sxs-lookup"><span data-stu-id="35a95-145">Therefore, the technician moves the lines from the next service visit to the current service visit.</span></span> <span data-ttu-id="35a95-146">Technik zaúčtuje servisní zakázku.</span><span class="sxs-lookup"><span data-stu-id="35a95-146">The technician then posts the service order.</span></span> <span data-ttu-id="35a95-147">Další informace o fázích servisní zakázky naleznete v tématu [Přesunutí řádků servisní zakázky](move-service-order-lines.md)..</span><span class="sxs-lookup"><span data-stu-id="35a95-147">For more information, see [Move service order lines](move-service-order-lines.md).</span></span>

## <a name="cancel-service-orders"></a><span data-ttu-id="35a95-148">Zrušit servisní zakázky</span><span class="sxs-lookup"><span data-stu-id="35a95-148">Cancel service orders</span></span>

<span data-ttu-id="35a95-149">Jedna ze servisních zakázek, které byly vytvořeny v lednu, je zastaralá, protože servisní zásah byl zrušen.</span><span class="sxs-lookup"><span data-stu-id="35a95-149">One of the other service orders that was generated for the month of January becomes obsolete, because the job is canceled.</span></span> <span data-ttu-id="35a95-150">Proto dispečerka tuto servisní zakázku zruší.</span><span class="sxs-lookup"><span data-stu-id="35a95-150">Therefore, the service dispatcher cancels the service order.</span></span> <span data-ttu-id="35a95-151">Další informace o kombinování servisních zakázek naleznete v tématu [Zrušení servisních zakázek](cancel-service-orders.md).</span><span class="sxs-lookup"><span data-stu-id="35a95-151">For more information, see [Cancel service orders](cancel-service-orders.md).</span></span>

## <a name="post-from-projects"></a><span data-ttu-id="35a95-152">Účtování z projektů</span><span class="sxs-lookup"><span data-stu-id="35a95-152">Post from projects</span></span>

<span data-ttu-id="35a95-153">Na konci každého týdne chce dispečerka zaúčtovat všechny servisní zakázky, které jsou připojené k určitému projektu.</span><span class="sxs-lookup"><span data-stu-id="35a95-153">At the end of each week, the dispatcher wants to post all service orders that are attached to a specific project.</span></span> <span data-ttu-id="35a95-154">Proto dispečerka vyhledá příslušný projekt ve formuláři **projekty** a zaúčtuje servisní zakázky, které byly dokončeny.</span><span class="sxs-lookup"><span data-stu-id="35a95-154">Therefore, the dispatcher locates the relevant project in the **Projects** form and posts the service orders that have been completed.</span></span> <span data-ttu-id="35a95-155">Další informace naleznete v tématu [Zaúčtování servisních zakázek (formulář třídy)](https://technet.microsoft.com/library/aa574685\(v=ax.60\)).</span><span class="sxs-lookup"><span data-stu-id="35a95-155">For more information, see [Post service orders (class form)](https://technet.microsoft.com/library/aa574685\(v=ax.60\)).</span></span>

## <a name="delete-service-orders"></a><span data-ttu-id="35a95-156">Odstranit servisní zakázky</span><span class="sxs-lookup"><span data-stu-id="35a95-156">Delete service orders</span></span>

<span data-ttu-id="35a95-157">Ve druhé polovině roku zákazník dospěje k závěru, že servisních zásahů je příliš málo.</span><span class="sxs-lookup"><span data-stu-id="35a95-157">During the second half of the year, your customer decides that the service visits are too infrequent.</span></span> <span data-ttu-id="35a95-158">Pro zbývající dobu servisní smlouvy musíte vytvořit novou sadu častějších servisních zásahů.</span><span class="sxs-lookup"><span data-stu-id="35a95-158">You must create a new, more frequent series of service visits for the remaining time on the service agreement.</span></span> <span data-ttu-id="35a95-159">To znamená, že musíte odstranit stávající servisní zakázky, které již byly vytvořeny (I), a místo nich vytvořit zakázky nové.</span><span class="sxs-lookup"><span data-stu-id="35a95-159">Therefore, you must delete the existing service orders and create new service orders.</span></span> <span data-ttu-id="35a95-160">Další informace naleznete v tématu [Odstranění servisních zakázek](delete-service-orders.md).</span><span class="sxs-lookup"><span data-stu-id="35a95-160">For more information, see [Delete service orders](delete-service-orders.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="35a95-161">Viz také</span><span class="sxs-lookup"><span data-stu-id="35a95-161">See also</span></span>

<span data-ttu-id="35a95-162">[Servisní zakázky (formulář)](https://technet.microsoft.com/library/aa554361\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="35a95-162">[Service orders (form)](https://technet.microsoft.com/library/aa554361\(v=ax.60\))</span></span>

  


