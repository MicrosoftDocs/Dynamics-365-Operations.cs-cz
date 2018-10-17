--- 
title: "Odeslání a schválení rozpočtu projektu"
description: "Tento postup ukazuje způsob vytvoření a odeslání rozpočtu projektu."
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProjProjectsListPage, ProjTable, ProjBudget, WorkflowSubmitDialog
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: f727e19d3f8c424b1c59e52602b7e907151f4492
ms.contentlocale: cs-cz
ms.lasthandoff: 09/14/2018

---
# <a name="submit-and-approve-project-budget"></a><span data-ttu-id="2357c-103">Odeslání a schválení rozpočtu projektu</span><span class="sxs-lookup"><span data-stu-id="2357c-103">Submit and approve project budget</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2357c-104">Tento postup ukazuje způsob vytvoření a odeslání rozpočtu projektu.</span><span class="sxs-lookup"><span data-stu-id="2357c-104">This procedure shows you how to create and submit the budget for a project.</span></span> 

<span data-ttu-id="2357c-105">Při vytvoření rozpočtu projektu můžete zadat odhadované výnosy a náklady projektu a použít je pro kontrolu skutečných transakcí projektu.</span><span class="sxs-lookup"><span data-stu-id="2357c-105">When you create a project budget, you can enter estimated revenues and costs for a project, and then use those to control actual project transactions.</span></span> <span data-ttu-id="2357c-106">V rozpočtu projektu musí být všechny původní rozpočty a revize odeslány do workflow projektu ke schválení.</span><span class="sxs-lookup"><span data-stu-id="2357c-106">In project budgeting, all original budgets and revisions must be sent to project workflow for approval.</span></span> <span data-ttu-id="2357c-107">Workflow vám poskytuje lepší kontrolu nad procesy a vytváří záznam historie změn.</span><span class="sxs-lookup"><span data-stu-id="2357c-107">Workflow gives you increased control over the process and creates a change history record.</span></span>

<span data-ttu-id="2357c-108">Tento úkol byl vytvořen pomocí sady dat USSI.</span><span class="sxs-lookup"><span data-stu-id="2357c-108">This task was created using the USSI data set.</span></span>

1. <span data-ttu-id="2357c-109">Přejděte na Řízení projektu a účetnictví > Projekty > Všechny projekty.</span><span class="sxs-lookup"><span data-stu-id="2357c-109">Go to Project management and accounting > Projects > All projects.</span></span>
2. <span data-ttu-id="2357c-110">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="2357c-110">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="2357c-111">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="2357c-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="2357c-112">V podokně akcí klikněte na možnost Plán.</span><span class="sxs-lookup"><span data-stu-id="2357c-112">On the Action Pane, click Plan.</span></span>
5. <span data-ttu-id="2357c-113">Klikněte na Rozpočet projektu.</span><span class="sxs-lookup"><span data-stu-id="2357c-113">Click Project budget.</span></span>
6. <span data-ttu-id="2357c-114">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="2357c-114">In the Description field, type a value.</span></span>
7. <span data-ttu-id="2357c-115">Rozbalte sekci Náklady</span><span class="sxs-lookup"><span data-stu-id="2357c-115">Expand the Cost section</span></span>
8. <span data-ttu-id="2357c-116">Klikněte na možnost Nový.</span><span class="sxs-lookup"><span data-stu-id="2357c-116">Click New.</span></span>
9. <span data-ttu-id="2357c-117">V poli Typ transakce vyberte možnost.</span><span class="sxs-lookup"><span data-stu-id="2357c-117">In the Transaction type field, select an option.</span></span>
10. <span data-ttu-id="2357c-118">V poli Kategorie zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="2357c-118">In the Category field, enter or select a value.</span></span>
11. <span data-ttu-id="2357c-119">Zadejte číslo do pole Původní rozpočet.</span><span class="sxs-lookup"><span data-stu-id="2357c-119">In the Original budget field, enter a number.</span></span>
12. <span data-ttu-id="2357c-120">Rozbalte sekci Výnosy.</span><span class="sxs-lookup"><span data-stu-id="2357c-120">Expand the Revenues section.</span></span>
13. <span data-ttu-id="2357c-121">Klepněte na možnost Nový.</span><span class="sxs-lookup"><span data-stu-id="2357c-121">Click New.</span></span>
14. <span data-ttu-id="2357c-122">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="2357c-122">In the list, mark the selected row.</span></span>
15. <span data-ttu-id="2357c-123">V poli Typ transakce vyberte možnost.</span><span class="sxs-lookup"><span data-stu-id="2357c-123">In the Transaction type field, select an option.</span></span>
16. <span data-ttu-id="2357c-124">V poli Kategorie zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="2357c-124">In the Category field, enter or select a value.</span></span>
17. <span data-ttu-id="2357c-125">Zadejte číslo do pole Původní rozpočet.</span><span class="sxs-lookup"><span data-stu-id="2357c-125">In the Original budget field, enter a number.</span></span>
18. <span data-ttu-id="2357c-126">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="2357c-126">Click Save.</span></span>
19. <span data-ttu-id="2357c-127">Klikněte na Workflow.</span><span class="sxs-lookup"><span data-stu-id="2357c-127">Click Workflow.</span></span>
20. <span data-ttu-id="2357c-128">Klepněte na tlačítko Odeslat.</span><span class="sxs-lookup"><span data-stu-id="2357c-128">Click Submit.</span></span>
21. <span data-ttu-id="2357c-129">Zadejte hodnotu do pole Komentář.</span><span class="sxs-lookup"><span data-stu-id="2357c-129">In the Comment field, type a value.</span></span>
22. <span data-ttu-id="2357c-130">Klepněte na tlačítko Odeslat.</span><span class="sxs-lookup"><span data-stu-id="2357c-130">Click Submit.</span></span>


