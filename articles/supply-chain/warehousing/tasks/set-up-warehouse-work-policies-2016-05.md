--- 
title: "Nastavení zásad práce ve skladu "
description: "Skladové procesy ne vždy zahrnují skladovou práci."
author: johanhoffmann
manager: AnnBe
ms.date: 06/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: b7d579ca7e2b9ca8cbead74b2c2ababfd142f171
ms.contentlocale: cs-cz
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-warehouse-work-policies"></a><span data-ttu-id="f29bd-103">Nastavení zásad práce ve skladu </span><span class="sxs-lookup"><span data-stu-id="f29bd-103">Set up warehouse work policies</span></span> 

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f29bd-104">Skladové procesy ne vždy zahrnují skladovou práci.</span><span class="sxs-lookup"><span data-stu-id="f29bd-104">Warehouse processes don’t always include warehouse work.</span></span> <span data-ttu-id="f29bd-105">Definováním zásad práce můžete zabránit vytváření práce pro výdej surovin, ale také vyskladnění dokončených výrobků pro sérii produktů v konkrétních umístěních.</span><span class="sxs-lookup"><span data-stu-id="f29bd-105">By defining a work policy, you can prevent the creation of work for raw material picking and put-away of finished goods for a set of products at specific locations.</span></span> <span data-ttu-id="f29bd-106">K vytvoření tohoto záznamu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="f29bd-106">The USMF demo data company was used to create this recording.</span></span> <span data-ttu-id="f29bd-107">Tento průvodce úkolem vyžaduje aplikaci Dynamics AX 7.0.1 nebo novější.</span><span class="sxs-lookup"><span data-stu-id="f29bd-107">This task guide requires Dynamics AX application 7.0.1 or later.</span></span>

1. <span data-ttu-id="f29bd-108">Přejděte do nabídky Řízení skladu > Nastavení > Práce > Pracovní zásady.</span><span class="sxs-lookup"><span data-stu-id="f29bd-108">Go to Warehouse management > Setup > Work > Work policies.</span></span>
2. <span data-ttu-id="f29bd-109">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="f29bd-109">Click New.</span></span>
3. <span data-ttu-id="f29bd-110">Do pole Název pracovní zásady zadejte „Žádné vyskladnění“.</span><span class="sxs-lookup"><span data-stu-id="f29bd-110">In the Work policy name field, type 'No put-away work'.</span></span>
4. <span data-ttu-id="f29bd-111">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="f29bd-111">Click Save.</span></span>
5. <span data-ttu-id="f29bd-112">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="f29bd-112">Click Add.</span></span>
6. <span data-ttu-id="f29bd-113">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="f29bd-113">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="f29bd-114">V poli Typ pořadí pracovních činností vyberte možnost Výdej dokončeného zboží.</span><span class="sxs-lookup"><span data-stu-id="f29bd-114">In the Work order type field, select 'Finished goods put away'.</span></span>
8. <span data-ttu-id="f29bd-115">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="f29bd-115">Click Add.</span></span>
9. <span data-ttu-id="f29bd-116">Označte na seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="f29bd-116">In the list, mark the selected row.</span></span>
10. <span data-ttu-id="f29bd-117">V poli Typ pořadí pracovních činností vyberte Vyskladnění vedlejšího produktu.</span><span class="sxs-lookup"><span data-stu-id="f29bd-117">In the Work order type field, select 'Co-product and by-product put away'.</span></span>
11. <span data-ttu-id="f29bd-118">Rozbalte oblast Skladová místa.</span><span class="sxs-lookup"><span data-stu-id="f29bd-118">Expand the Inventory locations section.</span></span>
12. <span data-ttu-id="f29bd-119">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="f29bd-119">Click Add.</span></span>
13. <span data-ttu-id="f29bd-120">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="f29bd-120">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="f29bd-121">V seznamu Sklad zadejte „51“.</span><span class="sxs-lookup"><span data-stu-id="f29bd-121">In the Warehouse list, enter '51'.</span></span>
15. <span data-ttu-id="f29bd-122">V poli Umístění zadejte nebo vyberte hodnotu 001.</span><span class="sxs-lookup"><span data-stu-id="f29bd-122">In the Location field, enter or select '001'.</span></span>
16. <span data-ttu-id="f29bd-123">Rozbalte část Produkty.</span><span class="sxs-lookup"><span data-stu-id="f29bd-123">Expand the Products section.</span></span>
17. <span data-ttu-id="f29bd-124">Vyberte možnost Vybráno v poli Výběr produktu.</span><span class="sxs-lookup"><span data-stu-id="f29bd-124">In the Product selection field, select 'Selected'.</span></span>
18. <span data-ttu-id="f29bd-125">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="f29bd-125">Click Add.</span></span>
19. <span data-ttu-id="f29bd-126">Označte na seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="f29bd-126">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="f29bd-127">V poli Číslo zboží zadejte nebo vyberte hodnotu L0101.</span><span class="sxs-lookup"><span data-stu-id="f29bd-127">In the Item number field, enter or select 'L0101'.</span></span>
21. <span data-ttu-id="f29bd-128">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="f29bd-128">Click Save.</span></span>


