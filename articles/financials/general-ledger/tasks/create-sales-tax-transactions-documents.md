---
title: Vytváření transakcí DPH v dokladech
description: DPH v dokumentech se vypočítá zadáním skupiny DPH a skupiny DPH položky na řádky dokladu.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, TaxTmpWorkTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 02e3ea556da9abefd37ce585086241d1e45aa0fa
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1571205"
---
# <a name="create-sales-tax-transactions-on-documents"></a><span data-ttu-id="14a6e-103">Vytváření transakcí DPH v dokladech</span><span class="sxs-lookup"><span data-stu-id="14a6e-103">Create sales tax transactions on documents</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="14a6e-104">DPH v dokumentech se vypočítá zadáním skupiny DPH a skupiny DPH položky na řádky dokladu.</span><span class="sxs-lookup"><span data-stu-id="14a6e-104">Sales tax on documents is calculated by providing a Sales tax group and an Item sales tax group on document lines.</span></span> <span data-ttu-id="14a6e-105">Ty vychází z hlavních dat, ale lze je změnit ručně, pokud je to nutné.</span><span class="sxs-lookup"><span data-stu-id="14a6e-105">These default from master data but can be changed manually if necessary.</span></span> <span data-ttu-id="14a6e-106">Vypočtenou částku prodejní daně lze zkontrolovat na úrovni řádku a dokumentu.</span><span class="sxs-lookup"><span data-stu-id="14a6e-106">The calculated sales tax can be checked on a line and document level.</span></span> <span data-ttu-id="14a6e-107">Tento úkol používá ukázkovou společnost USMF.</span><span class="sxs-lookup"><span data-stu-id="14a6e-107">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="14a6e-108">Přejděte na Pohledávky > Objednávky > Všechny prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="14a6e-108">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="14a6e-109">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="14a6e-109">Click New.</span></span>
3. <span data-ttu-id="14a6e-110">V poli Účet odběratele kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="14a6e-110">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="14a6e-111">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="14a6e-111">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="14a6e-112">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="14a6e-112">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="14a6e-113">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="14a6e-113">Click OK.</span></span>
7. <span data-ttu-id="14a6e-114">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="14a6e-114">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="14a6e-115">V poli Číslo zboží kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="14a6e-115">In the Item number field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="14a6e-116">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="14a6e-116">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="14a6e-117">Zadejte číslo do pole Jednotková cena.</span><span class="sxs-lookup"><span data-stu-id="14a6e-117">In the Unit price field, enter a number.</span></span>
11. <span data-ttu-id="14a6e-118">Rozbalte nebo sbalte oddíl Podrobnosti řádku.</span><span class="sxs-lookup"><span data-stu-id="14a6e-118">Expand or collapse the Line details section.</span></span>
12. <span data-ttu-id="14a6e-119">Klepněte na kartu Nastavení.</span><span class="sxs-lookup"><span data-stu-id="14a6e-119">Click the Setup tab.</span></span>
13. <span data-ttu-id="14a6e-120">V poli Skupina DPH zboží kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="14a6e-120">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="14a6e-121">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="14a6e-121">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="14a6e-122">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="14a6e-122">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="14a6e-123">Klepněte na tlačítko Finanční údaje.</span><span class="sxs-lookup"><span data-stu-id="14a6e-123">Click Financials.</span></span>
17. <span data-ttu-id="14a6e-124">Klikněte na DPH.</span><span class="sxs-lookup"><span data-stu-id="14a6e-124">Click Sales tax.</span></span>
18. <span data-ttu-id="14a6e-125">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="14a6e-125">Click OK.</span></span>
19. <span data-ttu-id="14a6e-126">Klikněte na položku Přidat řádek.</span><span class="sxs-lookup"><span data-stu-id="14a6e-126">Click Add line.</span></span>
20. <span data-ttu-id="14a6e-127">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="14a6e-127">In the list, mark the selected row.</span></span>
21. <span data-ttu-id="14a6e-128">V poli Číslo zboží kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="14a6e-128">In the Item number field, click the drop-down button to open the lookup.</span></span>
22. <span data-ttu-id="14a6e-129">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="14a6e-129">In the list, find and select the desired record.</span></span>
23. <span data-ttu-id="14a6e-130">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="14a6e-130">In the list, click the link in the selected row.</span></span>
24. <span data-ttu-id="14a6e-131">Zadejte číslo do pole Jednotková cena.</span><span class="sxs-lookup"><span data-stu-id="14a6e-131">In the Unit price field, enter a number.</span></span>
25. <span data-ttu-id="14a6e-132">V poli Skupina DPH zboží kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="14a6e-132">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
26. <span data-ttu-id="14a6e-133">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="14a6e-133">In the list, find and select the desired record.</span></span>
27. <span data-ttu-id="14a6e-134">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="14a6e-134">In the list, click the link in the selected row.</span></span>
28. <span data-ttu-id="14a6e-135">V podokně akcí klikněte na možnost Prodej.</span><span class="sxs-lookup"><span data-stu-id="14a6e-135">On the Action Pane, click Sell.</span></span>
29. <span data-ttu-id="14a6e-136">Klikněte na DPH.</span><span class="sxs-lookup"><span data-stu-id="14a6e-136">Click Sales tax.</span></span>
30. <span data-ttu-id="14a6e-137">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="14a6e-137">Click OK.</span></span>

