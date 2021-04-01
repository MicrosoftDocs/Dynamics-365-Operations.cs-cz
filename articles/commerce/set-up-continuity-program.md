---
title: Nastavení programů kontinuity pro kontaktní střediska
description: Tento článek popisuje, jak lze nastavit program trvání pro kontaktní středisko.
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: MCROrderParameters
audience: Application User
ms.reviewer: josaw
ms.custom: 16081
ms.assetid: 426a9be7-a931-4780-b372-e06f6083dd60
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 2428cafc45f074f7e2b4c3e59877079b8c1d4a92
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5242954"
---
# <a name="set-up-continuity-programs-for-call-centers"></a><span data-ttu-id="2cce8-103">Nastavení programů kontinuity pro kontaktní střediska</span><span class="sxs-lookup"><span data-stu-id="2cce8-103">Set up continuity programs for call centers</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2cce8-104">Tento článek popisuje, jak lze nastavit program trvání pro kontaktní středisko.</span><span class="sxs-lookup"><span data-stu-id="2cce8-104">This article describes how to set up a continuity program for a call center.</span></span>

<span data-ttu-id="2cce8-105">V rámci programu trvání, který je znám také jako program opakování objednávky, mohou odběratelé přijímat pravidelné dodávky produktu podle předem určeného plánu.</span><span class="sxs-lookup"><span data-stu-id="2cce8-105">In a continuity program, which is also known as a recurring order program, customers receive regular product shipments according to a predefined schedule.</span></span> <span data-ttu-id="2cce8-106">Jednotlivé dodávky mohou obsahovat různé produkty, stejně jako v případě klub „kniha měsíce“ nebo je možné opakovaně odesílat stejný výrobek.</span><span class="sxs-lookup"><span data-stu-id="2cce8-106">Each shipment can contain a different product, as in the case of a book-of-the-month club, or the same product can be sent repeatedly.</span></span> <span data-ttu-id="2cce8-107">K nastavení programu trvání je třeba dokončit následující úlohy.</span><span class="sxs-lookup"><span data-stu-id="2cce8-107">To set up a continuity program, you must complete the following tasks.</span></span>

1. <span data-ttu-id="2cce8-108">Nastavte parametry programu trvání na stránce **Parametry kontaktního střediska**.</span><span class="sxs-lookup"><span data-stu-id="2cce8-108">Set the continuity parameters on the **Call center parameters** page.</span></span>
2. <span data-ttu-id="2cce8-109">Vytvořte program trvání, který určuje podrobnosti, jako je platební kalendář, časové období dodávky a zda probíhá účtování předem.</span><span class="sxs-lookup"><span data-stu-id="2cce8-109">Create a continuity program that specifies details such as the payment schedule, the timing of the shipments, and whether billing is up front.</span></span> <span data-ttu-id="2cce8-110">Je také nutné přidat seznam produktů, které spadají do programu trvání.</span><span class="sxs-lookup"><span data-stu-id="2cce8-110">You must also add a list of products that are included in the continuity program.</span></span> <span data-ttu-id="2cce8-111">Každý výrobek obdrží číslo ID události přiřazené postupně, počínaje 1.</span><span class="sxs-lookup"><span data-stu-id="2cce8-111">Each product receives an event ID number that is assigned sequentially, beginning with 1.</span></span> <span data-ttu-id="2cce8-112">ID události určí pořadí, ve kterém jsou výrobky odesílány.</span><span class="sxs-lookup"><span data-stu-id="2cce8-112">The event IDs determine the order that products are sent in.</span></span>

    - <span data-ttu-id="2cce8-113">Pokud zákazníci obdrží různé produkty v rámci jednotlivých dodávek, produkty jsou odeslány v postupném pořadí podle jejich ID události a počínaje aktuální událostí.</span><span class="sxs-lookup"><span data-stu-id="2cce8-113">If customers receive a different product in each shipment, the products are sent in sequential order, based on their event IDs and beginning with the current event.</span></span>
    - <span data-ttu-id="2cce8-114">Pokud odběratelé přijímají stejný produkt v rámci každé dodávky, bude seznam obsahovat pouze jeden produkt, který má jedno ID události.</span><span class="sxs-lookup"><span data-stu-id="2cce8-114">If customers receive the same product in each shipment, the list contains only one product that has one event ID.</span></span> <span data-ttu-id="2cce8-115">Stejná událost se děje opakovaně.</span><span class="sxs-lookup"><span data-stu-id="2cce8-115">The same event occurs repeatedly.</span></span> <span data-ttu-id="2cce8-116">Můžete zadat počet opakování každé události.</span><span class="sxs-lookup"><span data-stu-id="2cce8-116">You can specify how many times each event is repeated.</span></span>

3. <span data-ttu-id="2cce8-117">Vytvořte nadřazený produkt, který představuje program trvání vytvořený v úkolu 2.</span><span class="sxs-lookup"><span data-stu-id="2cce8-117">Create a parent product that represents the continuity program that you created in task 2.</span></span> <span data-ttu-id="2cce8-118">Pokud přidáte tento produkt do prodejní objednávky, otevře se stránka **Trvání**.</span><span class="sxs-lookup"><span data-stu-id="2cce8-118">If you add this product to a sales order, the **Continuity** page opens.</span></span> <span data-ttu-id="2cce8-119">Tuto stránku můžete poté použít k vytvoření samotné trvalé objednávky.</span><span class="sxs-lookup"><span data-stu-id="2cce8-119">You can then use that page to create the actual continuity order.</span></span> <span data-ttu-id="2cce8-120">Nadřazený produkt neurčuje jednotlivé produkty, které odběratel obdrží v jednotlivých dodávkách.</span><span class="sxs-lookup"><span data-stu-id="2cce8-120">The parent product doesn't specify the individual products that the customer receives in each shipment.</span></span>

<span data-ttu-id="2cce8-121">Poté, co jste nastavili program trvání podle pokynů výše, můžete vytvořit trvalou objednávku pro odběratele.</span><span class="sxs-lookup"><span data-stu-id="2cce8-121">After you've set up a continuity program as described above, you can create a continuity order for a customer.</span></span> <span data-ttu-id="2cce8-122">Je také třeba provádět následující úlohy údržby.</span><span class="sxs-lookup"><span data-stu-id="2cce8-122">You might also have to perform the following additional maintenance tasks.</span></span>

- <span data-ttu-id="2cce8-123">**Aktualizujte aktuální období trvalé události** – nastavte dávkovou úlohu, která systém informuje o tom, jaké je aktuální období události.</span><span class="sxs-lookup"><span data-stu-id="2cce8-123">**Update the current continuity event period** – Set up a batch job that tells the system what the current event period is.</span></span>
- <span data-ttu-id="2cce8-124">**Vytvořte podřízené trvalé objednávky** – vytvořte podřízené objednávky z nadřazených trvalých objednávek.</span><span class="sxs-lookup"><span data-stu-id="2cce8-124">**Create continuity child orders** – Create child orders from the parent continuity order.</span></span>
- <span data-ttu-id="2cce8-125">**Zpracujte trvalé platby** – zpracování fakturace a oznámení pro platby, které jsou přidruženy k prodejním trvalým objednávkám.</span><span class="sxs-lookup"><span data-stu-id="2cce8-125">**Process continuity payments** – Process billing and notifications for payments that are associated with continuity sales orders.</span></span>
- <span data-ttu-id="2cce8-126">**Rozšiřte řádky trvání** (je-li vyžadováno) – zvyšte počet opakování povolených u trvalé události.</span><span class="sxs-lookup"><span data-stu-id="2cce8-126">**Extend continuity lines** (if required) – Extend the number of times that a continuity event can be repeated.</span></span> <span data-ttu-id="2cce8-127">Opakování dodávky lze poté překročit přes limit, který byl nastaven v poli **Prahová hodnota opakování trvalé položky** v parametrech kontaktního střediska.</span><span class="sxs-lookup"><span data-stu-id="2cce8-127">The repetition of shipments can then extend beyond the limit that was set in the **Continuity repeat threshold** field in the call center parameters.</span></span>
- <span data-ttu-id="2cce8-128">**Proveďte aktualizaci trvání** (je-li vyžadováno) – synchronizujte změny mezi programem trvání a nadřazenými trvalými prodejními objednávkami.</span><span class="sxs-lookup"><span data-stu-id="2cce8-128">**Perform a continuity update** (if required) – Synchronize changes between the continuity program and the continuity parent sales orders.</span></span>
- <span data-ttu-id="2cce8-129">**Zavřete nadřazené řádky trvání a objednávky** – zavřete trvalé objednávky.</span><span class="sxs-lookup"><span data-stu-id="2cce8-129">**Close continuity parent lines and orders** – Close continuity orders.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]