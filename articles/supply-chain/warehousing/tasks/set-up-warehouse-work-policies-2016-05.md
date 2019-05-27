---
title: Nastavení zásad práce ve skladu (aplikace, květen 2016)
description: Skladové procesy ne vždy zahrnují skladovou práci.
author: johanhoffmann
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkPolicy, WMSLocationIdLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 34b4255c85bb53f7e238b60559890571070953a6
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1569072"
---
# <a name="set-up-warehouse-work-policies-application-may-2016"></a><span data-ttu-id="4190b-103">Nastavení zásad práce ve skladu (aplikace, květen 2016)</span><span class="sxs-lookup"><span data-stu-id="4190b-103">Set up warehouse work policies (Application, May 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4190b-104">Skladové procesy ne vždy zahrnují skladovou práci.</span><span class="sxs-lookup"><span data-stu-id="4190b-104">Warehouse processes don’t always include warehouse work.</span></span> <span data-ttu-id="4190b-105">Definováním zásad práce můžete zabránit vytváření práce pro výdej surovin, ale také vyskladnění dokončených výrobků pro sérii produktů v konkrétních umístěních.</span><span class="sxs-lookup"><span data-stu-id="4190b-105">By defining a work policy, you can prevent the creation of work for raw material picking and put-away of finished goods for a set of products at specific locations.</span></span> <span data-ttu-id="4190b-106">K vytvoření tohoto záznamu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="4190b-106">The USMF demo data company was used to create this recording.</span></span> <span data-ttu-id="4190b-107">Tento průvodce úkolem vyžaduje aplikaci Dynamics AX 7.0.1 nebo novější.</span><span class="sxs-lookup"><span data-stu-id="4190b-107">This task guide requires Dynamics AX application 7.0.1 or later.</span></span>

1. <span data-ttu-id="4190b-108">Přejděte do nabídky Řízení skladu > Nastavení > Práce > Pracovní zásady.</span><span class="sxs-lookup"><span data-stu-id="4190b-108">Go to Warehouse management > Setup > Work > Work policies.</span></span>
2. <span data-ttu-id="4190b-109">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="4190b-109">Click New.</span></span>
3. <span data-ttu-id="4190b-110">Do pole Název pracovní zásady zadejte „Žádné vyskladnění“.</span><span class="sxs-lookup"><span data-stu-id="4190b-110">In the Work policy name field, type 'No put-away work'.</span></span>
4. <span data-ttu-id="4190b-111">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="4190b-111">Click Save.</span></span>
5. <span data-ttu-id="4190b-112">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="4190b-112">Click Add.</span></span>
6. <span data-ttu-id="4190b-113">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="4190b-113">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="4190b-114">V poli Typ pořadí pracovních činností vyberte možnost Výdej dokončeného zboží.</span><span class="sxs-lookup"><span data-stu-id="4190b-114">In the Work order type field, select 'Finished goods put away'.</span></span>
8. <span data-ttu-id="4190b-115">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="4190b-115">Click Add.</span></span>
9. <span data-ttu-id="4190b-116">Označte na seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="4190b-116">In the list, mark the selected row.</span></span>
10. <span data-ttu-id="4190b-117">V poli Typ pořadí pracovních činností vyberte Vyskladnění vedlejšího produktu.</span><span class="sxs-lookup"><span data-stu-id="4190b-117">In the Work order type field, select 'Co-product and by-product put away'.</span></span>
11. <span data-ttu-id="4190b-118">Rozbalte oblast Skladová místa.</span><span class="sxs-lookup"><span data-stu-id="4190b-118">Expand the Inventory locations section.</span></span>
12. <span data-ttu-id="4190b-119">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="4190b-119">Click Add.</span></span>
13. <span data-ttu-id="4190b-120">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="4190b-120">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="4190b-121">V seznamu Sklad zadejte „51“.</span><span class="sxs-lookup"><span data-stu-id="4190b-121">In the Warehouse list, enter '51'.</span></span>
15. <span data-ttu-id="4190b-122">V poli Umístění zadejte nebo vyberte hodnotu 001.</span><span class="sxs-lookup"><span data-stu-id="4190b-122">In the Location field, enter or select '001'.</span></span>
16. <span data-ttu-id="4190b-123">Rozbalte část Produkty.</span><span class="sxs-lookup"><span data-stu-id="4190b-123">Expand the Products section.</span></span>
17. <span data-ttu-id="4190b-124">Vyberte možnost Vybráno v poli Výběr produktu.</span><span class="sxs-lookup"><span data-stu-id="4190b-124">In the Product selection field, select 'Selected'.</span></span>
18. <span data-ttu-id="4190b-125">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="4190b-125">Click Add.</span></span>
19. <span data-ttu-id="4190b-126">Označte na seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="4190b-126">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="4190b-127">V poli Číslo zboží zadejte nebo vyberte hodnotu L0101.</span><span class="sxs-lookup"><span data-stu-id="4190b-127">In the Item number field, enter or select 'L0101'.</span></span>
21. <span data-ttu-id="4190b-128">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="4190b-128">Click Save.</span></span>

