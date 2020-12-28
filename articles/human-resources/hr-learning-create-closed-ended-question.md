---
title: Vytvoření dotazu s uzavřeným koncem
description: Dotazy s uzavřeným koncem umožňují poskytovat možnosti, ze kterých si respondent může vybírat.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KMAnswerCollection, KMAnswer, KMQuestion, HcmLearningWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a2eb53290d39fef0bf439a199dfd774138823ec2
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4417696"
---
# <a name="create-a-closed-ended-question"></a><span data-ttu-id="aff87-103">Vytvoření dotazu s uzavřeným koncem</span><span class="sxs-lookup"><span data-stu-id="aff87-103">Create a closed ended question</span></span>



<span data-ttu-id="aff87-104">Dotazy s uzavřeným koncem umožňují poskytovat možnosti, ze kterých si respondent může vybírat.</span><span class="sxs-lookup"><span data-stu-id="aff87-104">Closed-ended questions allow you to provide options for the respondent to choose from.</span></span> <span data-ttu-id="aff87-105">Nejprve je nutné vytvořit skupinu odpovědí s odpověďmi, a následně vytvořit dotaz, který bude používat skupinu odpovědí.</span><span class="sxs-lookup"><span data-stu-id="aff87-105">First, you need to create the Answer group with the answers, then create the question that will use the answer group.</span></span> <span data-ttu-id="aff87-106">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="aff87-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-an-answer-group"></a><span data-ttu-id="aff87-107">Vytvoření skupiny odpovědí</span><span class="sxs-lookup"><span data-stu-id="aff87-107">Create an answer group</span></span>
1. <span data-ttu-id="aff87-108">Přejít na Dotazník > Návrh > Skupiny odpovědí.</span><span class="sxs-lookup"><span data-stu-id="aff87-108">Go to Questionnaire > Design > Answer groups.</span></span>
2. <span data-ttu-id="aff87-109">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="aff87-109">Click New.</span></span>
3. <span data-ttu-id="aff87-110">Zadejte hodnotu do pole Skupina odpovědí.</span><span class="sxs-lookup"><span data-stu-id="aff87-110">In the Answer group field, type a value.</span></span>
4. <span data-ttu-id="aff87-111">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="aff87-111">In the Description field, type a value.</span></span>
    * <span data-ttu-id="aff87-112">Pomocí funkci Náhodně můžete náhodně umístit odpovědi v jiném pořadí pokaždé, když je pro otázku použita skupina odpovědí.</span><span class="sxs-lookup"><span data-stu-id="aff87-112">Use the Randomize functionality to randomly place the answers in a different order each time the answer group is used for a question.</span></span>  
5. <span data-ttu-id="aff87-113">Klepněte na tlačítko Odpověď.</span><span class="sxs-lookup"><span data-stu-id="aff87-113">Click Answer.</span></span>
6. <span data-ttu-id="aff87-114">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="aff87-114">Click New.</span></span>
    * <span data-ttu-id="aff87-115">Číselná řada určuje pořadí, v němž se zobrazují odpovědí, pokud není pro skupinu odpovědí vybrána možnost Náhodně.</span><span class="sxs-lookup"><span data-stu-id="aff87-115">Sequence number controls the order in which the answers are displayed, unless Randomize is selected for the Answer group.</span></span>  
    * <span data-ttu-id="aff87-116">Body můžete přidělit k odpovědím a použít je pro hodnocení dotazníku.</span><span class="sxs-lookup"><span data-stu-id="aff87-116">Points can be awarded to answers for use in scoring the questionnaire.</span></span>  
7. <span data-ttu-id="aff87-117">Do pole Body zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="aff87-117">In the Points field, enter a number.</span></span>
    * <span data-ttu-id="aff87-118">Správnou odpověď můžete nechat označit a určit tak, že vybraná odpověď je správná.</span><span class="sxs-lookup"><span data-stu-id="aff87-118">The correct answer can be marked to indicate that the selected answer is the correct one.</span></span> <span data-ttu-id="aff87-119">Tento údaj lze použít pro hodnocení dotazníku.</span><span class="sxs-lookup"><span data-stu-id="aff87-119">This can be used for scoring the questionnaire.</span></span>  
8. <span data-ttu-id="aff87-120">Zadejte hodnotu do pole Odpověď.</span><span class="sxs-lookup"><span data-stu-id="aff87-120">In the Answer field, type a value.</span></span>
    * <span data-ttu-id="aff87-121">Pokračujte ve vytváření možností výběru odpovědí pro skupinu odpovědí.</span><span class="sxs-lookup"><span data-stu-id="aff87-121">Continue to create answer selection options for the answer group.</span></span>  
9. <span data-ttu-id="aff87-122">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="aff87-122">Click New.</span></span>
10. <span data-ttu-id="aff87-123">Do pole Body zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="aff87-123">In the Points field, enter a number.</span></span>
11. <span data-ttu-id="aff87-124">Zadejte hodnotu do pole Odpověď.</span><span class="sxs-lookup"><span data-stu-id="aff87-124">In the Answer field, type a value.</span></span>
12. <span data-ttu-id="aff87-125">Klepněte na možnost Nový.</span><span class="sxs-lookup"><span data-stu-id="aff87-125">Click New.</span></span>
13. <span data-ttu-id="aff87-126">Do pole Body zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="aff87-126">In the Points field, enter a number.</span></span>
14. <span data-ttu-id="aff87-127">Zadejte hodnotu do pole Odpověď.</span><span class="sxs-lookup"><span data-stu-id="aff87-127">In the Answer field, type a value.</span></span>
15. <span data-ttu-id="aff87-128">Klepněte na možnost Nový.</span><span class="sxs-lookup"><span data-stu-id="aff87-128">Click New.</span></span>
16. <span data-ttu-id="aff87-129">Do pole Body zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="aff87-129">In the Points field, enter a number.</span></span>
17. <span data-ttu-id="aff87-130">Zadejte hodnotu do pole Odpověď.</span><span class="sxs-lookup"><span data-stu-id="aff87-130">In the Answer field, type a value.</span></span>
18. <span data-ttu-id="aff87-131">Klepněte na možnost Nový.</span><span class="sxs-lookup"><span data-stu-id="aff87-131">Click New.</span></span>
19. <span data-ttu-id="aff87-132">Do pole Body zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="aff87-132">In the Points field, enter a number.</span></span>
20. <span data-ttu-id="aff87-133">Zadejte hodnotu do pole Odpověď.</span><span class="sxs-lookup"><span data-stu-id="aff87-133">In the Answer field, type a value.</span></span>
21. <span data-ttu-id="aff87-134">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="aff87-134">Close the page.</span></span>
22. <span data-ttu-id="aff87-135">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="aff87-135">Close the page.</span></span>

## <a name="create-the-question"></a><span data-ttu-id="aff87-136">Vytvoření dotazu</span><span class="sxs-lookup"><span data-stu-id="aff87-136">Create the question</span></span>
1. <span data-ttu-id="aff87-137">Přejít na Dotazník > Návrh > Otázky.</span><span class="sxs-lookup"><span data-stu-id="aff87-137">Go to Questionnaire > Design > Questions.</span></span>
2. <span data-ttu-id="aff87-138">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="aff87-138">Click New.</span></span>
3. <span data-ttu-id="aff87-139">Pole Typ slouží k seskupení příbuzných dotazů.</span><span class="sxs-lookup"><span data-stu-id="aff87-139">Use the Type field to group related questions together.</span></span>
    * <span data-ttu-id="aff87-140">Pro dotazy s uzavřeným koncem můžete použít typy vstupu, jako např. Zaškrtávací políčko, Alternativní tlačítko nebo Pole se seznamem.</span><span class="sxs-lookup"><span data-stu-id="aff87-140">You can use input types of Check box, Alternative button, or Combo box for closed-ended questions.</span></span>  
4. <span data-ttu-id="aff87-141">Vyberte možnost v poli Typ vstupu.</span><span class="sxs-lookup"><span data-stu-id="aff87-141">In the Input type field, select an option.</span></span>
5. <span data-ttu-id="aff87-142">V poli Skupina odpovědí zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="aff87-142">In the Answer group field, enter or select a value.</span></span>
6. <span data-ttu-id="aff87-143">Zadejte hodnotu do pole Text.</span><span class="sxs-lookup"><span data-stu-id="aff87-143">In the Text field, type a value.</span></span>

