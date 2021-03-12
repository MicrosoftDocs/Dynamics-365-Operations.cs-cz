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
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1a807ee2743f051528b6b96ddf1eaada65283933
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4968647"
---
# <a name="create-sales-tax-transactions-on-documents"></a><span data-ttu-id="64310-103">Vytváření transakcí DPH v dokladech</span><span class="sxs-lookup"><span data-stu-id="64310-103">Create sales tax transactions on documents</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="64310-104">DPH v dokumentech se vypočítá zadáním skupiny DPH a skupiny DPH položky na řádky dokladu.</span><span class="sxs-lookup"><span data-stu-id="64310-104">Sales tax on documents is calculated by providing a Sales tax group and an Item sales tax group on document lines.</span></span> <span data-ttu-id="64310-105">Ty vychází z hlavních dat, ale lze je změnit ručně, pokud je to nutné.</span><span class="sxs-lookup"><span data-stu-id="64310-105">These default from master data but can be changed manually if necessary.</span></span> <span data-ttu-id="64310-106">Vypočtenou částku prodejní daně lze zkontrolovat na úrovni řádku a dokumentu.</span><span class="sxs-lookup"><span data-stu-id="64310-106">The calculated sales tax can be checked on a line and document level.</span></span> <span data-ttu-id="64310-107">Tento úkol používá ukázkovou společnost USMF.</span><span class="sxs-lookup"><span data-stu-id="64310-107">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="64310-108">Přejděte na Pohledávky > Objednávky > Všechny prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="64310-108">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="64310-109">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="64310-109">Click New.</span></span>
3. <span data-ttu-id="64310-110">V poli Účet odběratele kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="64310-110">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="64310-111">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="64310-111">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="64310-112">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="64310-112">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="64310-113">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="64310-113">Click OK.</span></span>
7. <span data-ttu-id="64310-114">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="64310-114">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="64310-115">V poli Číslo zboží kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="64310-115">In the Item number field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="64310-116">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="64310-116">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="64310-117">Zadejte číslo do pole Jednotková cena.</span><span class="sxs-lookup"><span data-stu-id="64310-117">In the Unit price field, enter a number.</span></span>
11. <span data-ttu-id="64310-118">Rozbalte nebo sbalte oddíl Podrobnosti řádku.</span><span class="sxs-lookup"><span data-stu-id="64310-118">Expand or collapse the Line details section.</span></span>
12. <span data-ttu-id="64310-119">Klepněte na kartu Nastavení.</span><span class="sxs-lookup"><span data-stu-id="64310-119">Click the Setup tab.</span></span>
13. <span data-ttu-id="64310-120">V poli Skupina DPH zboží kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="64310-120">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="64310-121">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="64310-121">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="64310-122">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="64310-122">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="64310-123">Klepněte na tlačítko Finanční údaje.</span><span class="sxs-lookup"><span data-stu-id="64310-123">Click Financials.</span></span>
17. <span data-ttu-id="64310-124">Klikněte na DPH.</span><span class="sxs-lookup"><span data-stu-id="64310-124">Click Sales tax.</span></span>
18. <span data-ttu-id="64310-125">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="64310-125">Click OK.</span></span>
19. <span data-ttu-id="64310-126">Klikněte na položku Přidat řádek.</span><span class="sxs-lookup"><span data-stu-id="64310-126">Click Add line.</span></span>
20. <span data-ttu-id="64310-127">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="64310-127">In the list, mark the selected row.</span></span>
21. <span data-ttu-id="64310-128">V poli Číslo zboží kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="64310-128">In the Item number field, click the drop-down button to open the lookup.</span></span>
22. <span data-ttu-id="64310-129">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="64310-129">In the list, find and select the desired record.</span></span>
23. <span data-ttu-id="64310-130">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="64310-130">In the list, click the link in the selected row.</span></span>
24. <span data-ttu-id="64310-131">Zadejte číslo do pole Jednotková cena.</span><span class="sxs-lookup"><span data-stu-id="64310-131">In the Unit price field, enter a number.</span></span>
25. <span data-ttu-id="64310-132">V poli Skupina DPH zboží kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="64310-132">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
26. <span data-ttu-id="64310-133">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="64310-133">In the list, find and select the desired record.</span></span>
27. <span data-ttu-id="64310-134">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="64310-134">In the list, click the link in the selected row.</span></span>
28. <span data-ttu-id="64310-135">V podokně akcí klikněte na možnost Prodej.</span><span class="sxs-lookup"><span data-stu-id="64310-135">On the Action Pane, click Sell.</span></span>
29. <span data-ttu-id="64310-136">Klikněte na DPH.</span><span class="sxs-lookup"><span data-stu-id="64310-136">Click Sales tax.</span></span>
30. <span data-ttu-id="64310-137">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="64310-137">Click OK.</span></span>

