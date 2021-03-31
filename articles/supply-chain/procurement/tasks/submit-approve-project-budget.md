---
title: Odeslání a schválení rozpočtu projektu
description: Tento postup ukazuje způsob vytvoření a odeslání rozpočtu projektu.
author: RichardLuan
manager: tfehr
ms.date: 08/13/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjBudget, WorkflowSubmitDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Service industries
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 72ac6705ef8584ef41980a1cc9490227538de365
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5222842"
---
# <a name="submit-and-approve-project-budget"></a><span data-ttu-id="46014-103">Odeslání a schválení rozpočtu projektu</span><span class="sxs-lookup"><span data-stu-id="46014-103">Submit and approve project budget</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="46014-104">Tento postup ukazuje způsob vytvoření a odeslání rozpočtu projektu.</span><span class="sxs-lookup"><span data-stu-id="46014-104">This procedure shows you how to create and submit the budget for a project.</span></span> 

<span data-ttu-id="46014-105">Při vytvoření rozpočtu projektu můžete zadat odhadované výnosy a náklady projektu a použít je pro kontrolu skutečných transakcí projektu.</span><span class="sxs-lookup"><span data-stu-id="46014-105">When you create a project budget, you can enter estimated revenues and costs for a project, and then use those to control actual project transactions.</span></span> <span data-ttu-id="46014-106">V rozpočtu projektu musí být všechny původní rozpočty a revize odeslány do workflow projektu ke schválení.</span><span class="sxs-lookup"><span data-stu-id="46014-106">In project budgeting, all original budgets and revisions must be sent to project workflow for approval.</span></span> <span data-ttu-id="46014-107">Workflow vám poskytuje lepší kontrolu nad procesy a vytváří záznam historie změn.</span><span class="sxs-lookup"><span data-stu-id="46014-107">Workflow gives you increased control over the process and creates a change history record.</span></span>

<span data-ttu-id="46014-108">Tento úkol byl vytvořen pomocí sady dat USSI.</span><span class="sxs-lookup"><span data-stu-id="46014-108">This task was created using the USSI data set.</span></span>

1. <span data-ttu-id="46014-109">V **navigačním podokně** přejděte na **Moduly > Řízení projektů a účetnictví > Projekty > Všechny projekty**.</span><span class="sxs-lookup"><span data-stu-id="46014-109">In the **Navigation pane**, go to **Modules > Project management and accounting > Projects > All projects**.</span></span>
2. <span data-ttu-id="46014-110">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="46014-110">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="46014-111">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="46014-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="46014-112">V **podokně akcí** klikněte na možnost **Plán**.</span><span class="sxs-lookup"><span data-stu-id="46014-112">On the **Action Pane**, click **Plan**.</span></span>
5. <span data-ttu-id="46014-113">Klikněte na **Rozpočet projektu**.</span><span class="sxs-lookup"><span data-stu-id="46014-113">Click **Project budget**.</span></span>
6. <span data-ttu-id="46014-114">Zadejte hodnotu do pole **Popis**.</span><span class="sxs-lookup"><span data-stu-id="46014-114">In the **Description** field, type a value.</span></span>
7. <span data-ttu-id="46014-115">Rozbalte pevnou záložku **Náklady**.</span><span class="sxs-lookup"><span data-stu-id="46014-115">Expand the **Cost** fastTab.</span></span>
8. <span data-ttu-id="46014-116">Klepněte na možnost **Nový**.</span><span class="sxs-lookup"><span data-stu-id="46014-116">Click **New**.</span></span>
9. <span data-ttu-id="46014-117">V poli **Typ transakce** vyberte možnost.</span><span class="sxs-lookup"><span data-stu-id="46014-117">In the **Transaction type** field, select an option.</span></span>
10. <span data-ttu-id="46014-118">V poli **Kategorie** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="46014-118">In the **Category** field, enter or select a value.</span></span>
11. <span data-ttu-id="46014-119">Zadejte číslo do pole **Původní rozpočet**.</span><span class="sxs-lookup"><span data-stu-id="46014-119">In the **Original budget** field, enter a number.</span></span>
12. <span data-ttu-id="46014-120">Rozbalte pevnou záložku **Výnosy**.</span><span class="sxs-lookup"><span data-stu-id="46014-120">Expand the **Revenues** fastTab.</span></span>
13. <span data-ttu-id="46014-121">Klepněte na možnost **Nový**.</span><span class="sxs-lookup"><span data-stu-id="46014-121">Click **New**.</span></span>
14. <span data-ttu-id="46014-122">Označte na seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="46014-122">In the list, mark the selected row.</span></span>
15. <span data-ttu-id="46014-123">V poli **Typ transakce** vyberte možnost.</span><span class="sxs-lookup"><span data-stu-id="46014-123">In the **Transaction type** field, select an option.</span></span>
16. <span data-ttu-id="46014-124">V poli **Kategorie** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="46014-124">In the **Category** field, enter or select a value.</span></span>
17. <span data-ttu-id="46014-125">Zadejte číslo do pole **Původní rozpočet**.</span><span class="sxs-lookup"><span data-stu-id="46014-125">In the **Original budget** field, enter a number.</span></span>
18. <span data-ttu-id="46014-126">Klikněte na možnost **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="46014-126">Click **Save**.</span></span>
19. <span data-ttu-id="46014-127">Klikněte na **Workflow**.</span><span class="sxs-lookup"><span data-stu-id="46014-127">Click **Workflow**.</span></span>
20. <span data-ttu-id="46014-128">Klepněte na tlačítko **Odeslat**.</span><span class="sxs-lookup"><span data-stu-id="46014-128">Click **Submit**.</span></span>
21. <span data-ttu-id="46014-129">Zadejte hodnotu do pole **Komentář**.</span><span class="sxs-lookup"><span data-stu-id="46014-129">In the **Comment** field, type a value.</span></span>
22. <span data-ttu-id="46014-130">Klepněte na tlačítko **Odeslat**.</span><span class="sxs-lookup"><span data-stu-id="46014-130">Click **Submit**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]