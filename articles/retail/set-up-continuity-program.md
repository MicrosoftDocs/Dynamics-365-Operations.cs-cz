---
title: "Nastavení programu trvání pro kontaktní středisko"
description: "Tento článek popisuje, jak lze nastavit program trvání pro kontaktní středisko."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: MCROrderParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16081
ms.assetid: 426a9be7-a931-4780-b372-e06f6083dd60
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 6f0042bf45354113b2bce22ae81365dee837824d
ms.contentlocale: cs-cz
ms.lasthandoff: 04/13/2018

---

# <a name="set-up-a-continuity-program-for-a-call-center"></a><span data-ttu-id="c3407-103">Nastavení programu trvání pro kontaktní středisko</span><span class="sxs-lookup"><span data-stu-id="c3407-103">Set up a continuity program for a call center</span></span>

[!INCLUDE [banner](includes/banner.md)]

<span data-ttu-id="c3407-104">Tento článek popisuje, jak lze nastavit program trvání pro kontaktní středisko.</span><span class="sxs-lookup"><span data-stu-id="c3407-104">This article describes how to set up a continuity program for a call center.</span></span>

<span data-ttu-id="c3407-105">V rámci programu trvání, který je znám také jako program opakování objednávky, mohou odběratelé přijímat pravidelné dodávky produktu podle předem určeného plánu.</span><span class="sxs-lookup"><span data-stu-id="c3407-105">In a continuity program, which is also known as a recurring order program, customers receive regular product shipments according to a predefined schedule.</span></span> <span data-ttu-id="c3407-106">Jednotlivé dodávky mohou obsahovat různé produkty, stejně jako v případě klub „kniha měsíce“ nebo je možné opakovaně odesílat stejný výrobek.</span><span class="sxs-lookup"><span data-stu-id="c3407-106">Each shipment can contain a different product, as in the case of a book-of-the-month club, or the same product can be sent repeatedly.</span></span> <span data-ttu-id="c3407-107">K nastavení programu trvání je třeba dokončit následující úlohy.</span><span class="sxs-lookup"><span data-stu-id="c3407-107">To set up a continuity program, you must complete the following tasks.</span></span>

1.  <span data-ttu-id="c3407-108">Nastavte parametry programu trvání na stránce **Parametry kontaktního střediska**.</span><span class="sxs-lookup"><span data-stu-id="c3407-108">Set the continuity parameters on the **Call center parameters** page.</span></span>
2.  <span data-ttu-id="c3407-109">Vytvořte program trvání, který určuje podrobnosti, jako je platební kalendář, časové období dodávky a zda probíhá účtování předem.</span><span class="sxs-lookup"><span data-stu-id="c3407-109">Create a continuity program that specifies details such as the payment schedule, the timing of the shipments, and whether billing is up front.</span></span> <span data-ttu-id="c3407-110">Je také nutné přidat seznam produktů, které spadají do programu trvání.</span><span class="sxs-lookup"><span data-stu-id="c3407-110">You must also add a list of products that are included in the continuity program.</span></span> <span data-ttu-id="c3407-111">Každý výrobek obdrží číslo ID události přiřazené postupně, počínaje 1.</span><span class="sxs-lookup"><span data-stu-id="c3407-111">Each product receives an event ID number that is assigned sequentially, beginning with 1.</span></span> <span data-ttu-id="c3407-112">ID události určí pořadí, ve kterém jsou výrobky odesílány.</span><span class="sxs-lookup"><span data-stu-id="c3407-112">The event IDs determine the order that products are sent in.</span></span>
    -   <span data-ttu-id="c3407-113">Pokud zákazníci obdrží různé produkty v rámci jednotlivých dodávek, produkty jsou odeslány v postupném pořadí podle jejich ID události a počínaje aktuální událostí.</span><span class="sxs-lookup"><span data-stu-id="c3407-113">If customers receive a different product in each shipment, the products are sent in sequential order, based on their event IDs and beginning with the current event.</span></span>
    -   <span data-ttu-id="c3407-114">Pokud odběratelé přijímají stejný produkt v rámci každé dodávky, bude seznam obsahovat pouze jeden produkt, který má jedno ID události.</span><span class="sxs-lookup"><span data-stu-id="c3407-114">If customers receive the same product in each shipment, the list contains only one product that has one event ID.</span></span> <span data-ttu-id="c3407-115">Stejná událost se děje opakovaně.</span><span class="sxs-lookup"><span data-stu-id="c3407-115">The same event occurs repeatedly.</span></span> <span data-ttu-id="c3407-116">Můžete zadat počet opakování každé události.</span><span class="sxs-lookup"><span data-stu-id="c3407-116">You can specify how many times each event is repeated.</span></span>

3.  <span data-ttu-id="c3407-117">Vytvořte nadřazený produkt, který představuje program trvání vytvořený v úkolu 2.</span><span class="sxs-lookup"><span data-stu-id="c3407-117">Create a parent product that represents the continuity program that you created in task 2.</span></span> <span data-ttu-id="c3407-118">Pokud přidáte tento produkt do prodejní objednávky, otevře se stránka **Trvání**.</span><span class="sxs-lookup"><span data-stu-id="c3407-118">If you add this product to a sales order, the **Continuity** page opens.</span></span> <span data-ttu-id="c3407-119">Tuto stránku můžete poté použít k vytvoření samotné trvalé objednávky.</span><span class="sxs-lookup"><span data-stu-id="c3407-119">You can then use that page to create the actual continuity order.</span></span> <span data-ttu-id="c3407-120">Nadřazený produkt neurčuje jednotlivé produkty, které odběratel obdrží v jednotlivých dodávkách.</span><span class="sxs-lookup"><span data-stu-id="c3407-120">The parent product doesn't specify the individual products that the customer receives in each shipment.</span></span>

<span data-ttu-id="c3407-121">Poté, co jste nastavili program trvání podle pokynů výše, můžete vytvořit trvalou objednávku pro odběratele.</span><span class="sxs-lookup"><span data-stu-id="c3407-121">After you've set up a continuity program as described above, you can create a continuity order for a customer.</span></span> <span data-ttu-id="c3407-122">Je také třeba provádět následující úlohy údržby.</span><span class="sxs-lookup"><span data-stu-id="c3407-122">You might also have to perform the following additional maintenance tasks.</span></span>

-   <span data-ttu-id="c3407-123">**Aktualizujte aktuální období trvalé události** – nastavte dávkovou úlohu, která systém informuje o tom, jaké je aktuální období události.</span><span class="sxs-lookup"><span data-stu-id="c3407-123">**Update the current continuity event period** – Set up a batch job that tells the system what the current event period is.</span></span>
-   <span data-ttu-id="c3407-124">**Vytvořte podřízené trvalé objednávky** – vytvořte podřízené objednávky z nadřazených trvalých objednávek.</span><span class="sxs-lookup"><span data-stu-id="c3407-124">**Create continuity child orders** – Create child orders from the parent continuity order.</span></span>
-   <span data-ttu-id="c3407-125">**Zpracujte trvalé platby** – zpracování fakturace a oznámení pro platby, které jsou přidruženy k prodejním trvalým objednávkám.</span><span class="sxs-lookup"><span data-stu-id="c3407-125">**Process continuity payments** – Process billing and notifications for payments that are associated with continuity sales orders.</span></span>
-   <span data-ttu-id="c3407-126">**Rozšiřte řádky trvání** (je-li vyžadováno) – zvyšte počet opakování povolených u trvalé události.</span><span class="sxs-lookup"><span data-stu-id="c3407-126">**Extend continuity lines** (if required) – Extend the number of times that a continuity event can be repeated.</span></span> <span data-ttu-id="c3407-127">Opakování dodávky lze poté překročit přes limit, který byl nastaven v poli **Prahová hodnota opakování trvalé položky** v parametrech kontaktního střediska.</span><span class="sxs-lookup"><span data-stu-id="c3407-127">The repetition of shipments can then extend beyond the limit that was set in the **Continuity repeat threshold** field in the call center parameters.</span></span>
-   <span data-ttu-id="c3407-128">**Proveďte aktualizaci trvání** (je-li vyžadováno) – synchronizujte změny mezi programem trvání a nadřazenými trvalými prodejními objednávkami.</span><span class="sxs-lookup"><span data-stu-id="c3407-128">**Perform a continuity update** (if required) – Synchronize changes between the continuity program and the continuity parent sales orders.</span></span>
-   <span data-ttu-id="c3407-129">**Zavřete nadřazené řádky trvání a objednávky** – zavřete trvalé objednávky.</span><span class="sxs-lookup"><span data-stu-id="c3407-129">**Close continuity parent lines and orders** – Close continuity orders.</span></span>





