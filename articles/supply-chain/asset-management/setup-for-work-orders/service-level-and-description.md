---
title: Úroveň a popis služby
description: V tomto tématu jsou vysvětleny úrovně a popis služby v modulu Správa majetku.
author: josaw1
manager: tfehr
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetObjectServiceLevel, EntAssetWorkOrderStandardDescription, EntAssetWorkOrderServiceLevel, EntAssetServiceLevelLookup
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 65a3a0b6c2c052c41be469591c1281c1cce2b7d0
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5226778"
---
# <a name="service-level-and-description"></a><span data-ttu-id="d1987-103">Úroveň a popis služby</span><span class="sxs-lookup"><span data-stu-id="d1987-103">Service level and description</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="d1987-104">Při vytvoření pracovního příkazu můžete pro něj definovat úrovně služeb a přidat do něj obecný popis.</span><span class="sxs-lookup"><span data-stu-id="d1987-104">When you create a work order, you might want to define the service levels for it and add a general description to it.</span></span> <span data-ttu-id="d1987-105">Na stránce **Úrovně služeb pracovního příkazu** můžete vytvářet úrovně služeb a na stránce **Popis pracovního příkazu** můžete vytvářet popis.</span><span class="sxs-lookup"><span data-stu-id="d1987-105">You can create work order service levels on the **Work order service levels** page and descriptions on the **Work order description** page.</span></span>

## <a name="create-a-service-level"></a><span data-ttu-id="d1987-106">Vytvoření úrovně služeb</span><span class="sxs-lookup"><span data-stu-id="d1987-106">Create a service level</span></span>

1. <span data-ttu-id="d1987-107">Vyberte **Správa majetku** \> **Nastavení** \> **Pracovní příkazy** \> **Úroveň služeb**.</span><span class="sxs-lookup"><span data-stu-id="d1987-107">Select **Asset management** \> **Setup** \> **Work orders** \> **Service level**.</span></span>
2. <span data-ttu-id="d1987-108">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="d1987-108">Select **New**.</span></span>
3. <span data-ttu-id="d1987-109">V poli **Úroveň služeb** zadejte úroveň služeb (například číslo).</span><span class="sxs-lookup"><span data-stu-id="d1987-109">In the **Service level** field, enter the service level (for example, a number).</span></span>
4. <span data-ttu-id="d1987-110">Do pole **Název** zadejte název.</span><span class="sxs-lookup"><span data-stu-id="d1987-110">In the **Name** field, enter a name.</span></span>

    <span data-ttu-id="d1987-111">Na pevné záložce **Pracovní příkazy** můžete definovat očekávaná počáteční a koncová data a časy.</span><span class="sxs-lookup"><span data-stu-id="d1987-111">On the **Work orders** FastTab, you can define expected start and end dates and times.</span></span> <span data-ttu-id="d1987-112">Pole na této pevné záložce definují období, v průběhu kterého by měly být pracovní příkazy zahájeny a ukončeny.</span><span class="sxs-lookup"><span data-stu-id="d1987-112">The fields on this FastTab define the period that work orders should be started and ended during.</span></span> <span data-ttu-id="d1987-113">Používají se pro ručně vytvořené pracovní příkazy a pracovní příkazy vytvořené na základě požadavků na údržbu.</span><span class="sxs-lookup"><span data-stu-id="d1987-113">They are used for work orders that are manually created and work orders that are created based on maintenance requests.</span></span> 

5. <span data-ttu-id="d1987-114">Do pole **Počáteční den** zadejte počet dní určující období, během kterého má být pracovní příkaz zahájen.</span><span class="sxs-lookup"><span data-stu-id="d1987-114">In the **Start day** field, enter a number of days to define the period that the work order should start during.</span></span> <span data-ttu-id="d1987-115">Počet dnů se vypočítá od data vytvoření pracovního příkazu.</span><span class="sxs-lookup"><span data-stu-id="d1987-115">The number of days is calculated from the creation date of the work order.</span></span> <span data-ttu-id="d1987-116">Má-li být například pracovní příkaz zahájen při vytvoření, zadejte hodnotu **0**.</span><span class="sxs-lookup"><span data-stu-id="d1987-116">For example, if the work order should start when it's created, enter **0**.</span></span> <span data-ttu-id="d1987-117">Má-li být pracovní příkaz zahájen v průběhu jednoho týdne po vytvoření, zadejte hodnotu **7**.</span><span class="sxs-lookup"><span data-stu-id="d1987-117">If the work order should start within one week after it's created, enter **7**.</span></span>
6. <span data-ttu-id="d1987-118">Chcete-li nastavit i čas zahájení pro pracovní příkaz kromě počátečního data, nastavte volbu **Nastavit počáteční čas** na hodnotu **Ano**.</span><span class="sxs-lookup"><span data-stu-id="d1987-118">To set a start time for the work order, in addition to a start date, set the **Set start time** option to **Yes**.</span></span> <span data-ttu-id="d1987-119">Poté zadejte počáteční čas do pole **Čas zahájní**.</span><span class="sxs-lookup"><span data-stu-id="d1987-119">Then enter the start time in the **Start time** field.</span></span> <span data-ttu-id="d1987-120">Pokud nastavíte možnost na **Ne**, použije se aktuální čas dne.</span><span class="sxs-lookup"><span data-stu-id="d1987-120">If you set the option to **No**, the current time of day is used.</span></span>
7. <span data-ttu-id="d1987-121">Do pole **Koncový den** zadejte počet dní určující období, během kterého má být pracovní příkaz ukončen.</span><span class="sxs-lookup"><span data-stu-id="d1987-121">In the **End day** field, enter a number of days to define the period that the work order should end during.</span></span> <span data-ttu-id="d1987-122">Počet dnů se vypočítá od počátečního data pracovního příkazu.</span><span class="sxs-lookup"><span data-stu-id="d1987-122">The number of days is calculated from the start date of the work order.</span></span> <span data-ttu-id="d1987-123">Má-li například pracovní příkaz končit během jednoho týdne od počátečního data, zadejte **7**.</span><span class="sxs-lookup"><span data-stu-id="d1987-123">For example, if the work order should end within one week of its start date, enter **7**.</span></span>
8. <span data-ttu-id="d1987-124">Chcete-li nastavit i čas ukončení pro pracovní příkaz kromě koncového data, nastavte volbu **Nastavit koncový čas** na hodnotu **Ano**.</span><span class="sxs-lookup"><span data-stu-id="d1987-124">To set an end time for the work order, in addition to an end date, set the **Set end time** option to **Yes**.</span></span> <span data-ttu-id="d1987-125">Poté zadejte čas ukončení do pole **Čas ukončení**.</span><span class="sxs-lookup"><span data-stu-id="d1987-125">Then enter the end time in the **End time** field.</span></span> <span data-ttu-id="d1987-126">Pokud nastavíte možnost na **Ne**, použije se aktuální čas dne.</span><span class="sxs-lookup"><span data-stu-id="d1987-126">If you set the option to **No**, the current time of day is used.</span></span>
9. <span data-ttu-id="d1987-127">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="d1987-127">Select **Save**.</span></span>

![Stránka Úroveň služby pracovních příkazů](media/19-setup-for-work-orders.png)

## <a name="create-a-description"></a><span data-ttu-id="d1987-129">Vytvořit popis</span><span class="sxs-lookup"><span data-stu-id="d1987-129">Create a description</span></span>

1. <span data-ttu-id="d1987-130">Vyberte **Správa majetku** \> **Nastavení** \> **Pracovní příkazy** \> **Popisy**.</span><span class="sxs-lookup"><span data-stu-id="d1987-130">Select **Asset management** \> **Setup** \> **Work orders** \> **Descriptions**.</span></span>
2. <span data-ttu-id="d1987-131">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="d1987-131">Select **New**.</span></span>
3. <span data-ttu-id="d1987-132">Zadejte popis do pole **Popis**.</span><span class="sxs-lookup"><span data-stu-id="d1987-132">In the **Description** field, enter the description.</span></span>
4. <span data-ttu-id="d1987-133">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="d1987-133">Select **Save**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]