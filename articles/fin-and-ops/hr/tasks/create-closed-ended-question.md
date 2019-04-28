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
ms.search.form: KMAnswerCollection, KMAnswer, KMQuestion
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 92e4f9697fc00798d917db6f7f50d7e3b8739233
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/19/2019
ms.locfileid: "858645"
---
# <a name="create-a-closed-ended-question"></a><span data-ttu-id="c300a-103">Vytvoření dotazu s uzavřeným koncem</span><span class="sxs-lookup"><span data-stu-id="c300a-103">Create a closed ended question</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c300a-104">Dotazy s uzavřeným koncem umožňují poskytovat možnosti, ze kterých si respondent může vybírat.</span><span class="sxs-lookup"><span data-stu-id="c300a-104">Closed-ended questions allow you to provide options for the respondent to choose from.</span></span> <span data-ttu-id="c300a-105">Nejprve je nutné vytvořit skupinu odpovědí s odpověďmi, a následně vytvořit dotaz, který bude používat skupinu odpovědí.</span><span class="sxs-lookup"><span data-stu-id="c300a-105">First, you need to create the Answer group with the answers, then create the question that will use the answer group.</span></span> <span data-ttu-id="c300a-106">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="c300a-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-an-answer-group"></a><span data-ttu-id="c300a-107">Vytvoření skupiny odpovědí</span><span class="sxs-lookup"><span data-stu-id="c300a-107">Create an answer group</span></span>
1. <span data-ttu-id="c300a-108">Přejít na Dotazník > Návrh > Skupiny odpovědí.</span><span class="sxs-lookup"><span data-stu-id="c300a-108">Go to Questionnaire > Design > Answer groups.</span></span>
2. <span data-ttu-id="c300a-109">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="c300a-109">Click New.</span></span>
3. <span data-ttu-id="c300a-110">Zadejte hodnotu do pole Skupina odpovědí.</span><span class="sxs-lookup"><span data-stu-id="c300a-110">In the Answer group field, type a value.</span></span>
4. <span data-ttu-id="c300a-111">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="c300a-111">In the Description field, type a value.</span></span>
    * <span data-ttu-id="c300a-112">Pomocí funkci Náhodně můžete náhodně umístit odpovědi v jiném pořadí pokaždé, když je pro otázku použita skupina odpovědí.</span><span class="sxs-lookup"><span data-stu-id="c300a-112">Use the Randomize functionality to randomly place the answers in a different order each time the answer group is used for a question.</span></span>  
5. <span data-ttu-id="c300a-113">Klepněte na tlačítko Odpověď.</span><span class="sxs-lookup"><span data-stu-id="c300a-113">Click Answer.</span></span>
6. <span data-ttu-id="c300a-114">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="c300a-114">Click New.</span></span>
    * <span data-ttu-id="c300a-115">Číselná řada určuje pořadí, v němž se zobrazují odpovědí, pokud není pro skupinu odpovědí vybrána možnost Náhodně.</span><span class="sxs-lookup"><span data-stu-id="c300a-115">Sequence number controls the order in which the answers are displayed, unless Randomize is selected for the Answer group.</span></span>  
    * <span data-ttu-id="c300a-116">Body můžete přidělit k odpovědím a použít je pro hodnocení dotazníku.</span><span class="sxs-lookup"><span data-stu-id="c300a-116">Points can be awarded to answers for use in scoring the questionnaire.</span></span>  
7. <span data-ttu-id="c300a-117">Do pole Body zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="c300a-117">In the Points field, enter a number.</span></span>
    * <span data-ttu-id="c300a-118">Správnou odpověď můžete nechat označit a určit tak, že vybraná odpověď je správná.</span><span class="sxs-lookup"><span data-stu-id="c300a-118">The correct answer can be marked to indicate that the selected answer is the correct one.</span></span> <span data-ttu-id="c300a-119">Tento údaj lze použít pro hodnocení dotazníku.</span><span class="sxs-lookup"><span data-stu-id="c300a-119">This can be used for scoring the questionnaire.</span></span>  
8. <span data-ttu-id="c300a-120">Zadejte hodnotu do pole Odpověď.</span><span class="sxs-lookup"><span data-stu-id="c300a-120">In the Answer field, type a value.</span></span>
    * <span data-ttu-id="c300a-121">Pokračujte ve vytváření možností výběru odpovědí pro skupinu odpovědí.</span><span class="sxs-lookup"><span data-stu-id="c300a-121">Continue to create answer selection options for the answer group.</span></span>  
9. <span data-ttu-id="c300a-122">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="c300a-122">Click New.</span></span>
10. <span data-ttu-id="c300a-123">Do pole Body zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="c300a-123">In the Points field, enter a number.</span></span>
11. <span data-ttu-id="c300a-124">Zadejte hodnotu do pole Odpověď.</span><span class="sxs-lookup"><span data-stu-id="c300a-124">In the Answer field, type a value.</span></span>
12. <span data-ttu-id="c300a-125">Klepněte na možnost Nový.</span><span class="sxs-lookup"><span data-stu-id="c300a-125">Click New.</span></span>
13. <span data-ttu-id="c300a-126">Do pole Body zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="c300a-126">In the Points field, enter a number.</span></span>
14. <span data-ttu-id="c300a-127">Zadejte hodnotu do pole Odpověď.</span><span class="sxs-lookup"><span data-stu-id="c300a-127">In the Answer field, type a value.</span></span>
15. <span data-ttu-id="c300a-128">Klepněte na možnost Nový.</span><span class="sxs-lookup"><span data-stu-id="c300a-128">Click New.</span></span>
16. <span data-ttu-id="c300a-129">Do pole Body zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="c300a-129">In the Points field, enter a number.</span></span>
17. <span data-ttu-id="c300a-130">Zadejte hodnotu do pole Odpověď.</span><span class="sxs-lookup"><span data-stu-id="c300a-130">In the Answer field, type a value.</span></span>
18. <span data-ttu-id="c300a-131">Klepněte na možnost Nový.</span><span class="sxs-lookup"><span data-stu-id="c300a-131">Click New.</span></span>
19. <span data-ttu-id="c300a-132">Do pole Body zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="c300a-132">In the Points field, enter a number.</span></span>
20. <span data-ttu-id="c300a-133">Zadejte hodnotu do pole Odpověď.</span><span class="sxs-lookup"><span data-stu-id="c300a-133">In the Answer field, type a value.</span></span>
21. <span data-ttu-id="c300a-134">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="c300a-134">Close the page.</span></span>
22. <span data-ttu-id="c300a-135">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="c300a-135">Close the page.</span></span>

## <a name="create-the-question"></a><span data-ttu-id="c300a-136">Vytvoření dotazu</span><span class="sxs-lookup"><span data-stu-id="c300a-136">Create the question</span></span>
1. <span data-ttu-id="c300a-137">Přejít na Dotazník > Návrh > Otázky.</span><span class="sxs-lookup"><span data-stu-id="c300a-137">Go to Questionnaire > Design > Questions.</span></span>
2. <span data-ttu-id="c300a-138">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="c300a-138">Click New.</span></span>
3. <span data-ttu-id="c300a-139">Pole Typ slouží k seskupení příbuzných dotazů.</span><span class="sxs-lookup"><span data-stu-id="c300a-139">Use the Type field to group related questions together.</span></span>
    * <span data-ttu-id="c300a-140">Pro dotazy s uzavřeným koncem můžete použít typy vstupu, jako např. Zaškrtávací políčko, Alternativní tlačítko nebo Pole se seznamem.</span><span class="sxs-lookup"><span data-stu-id="c300a-140">You can use input types of Check box, Alternative button, or Combo box for closed-ended questions.</span></span>  
4. <span data-ttu-id="c300a-141">Vyberte možnost v poli Typ vstupu.</span><span class="sxs-lookup"><span data-stu-id="c300a-141">In the Input type field, select an option.</span></span>
5. <span data-ttu-id="c300a-142">V poli Skupina odpovědí zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="c300a-142">In the Answer group field, enter or select a value.</span></span>
6. <span data-ttu-id="c300a-143">Zadejte hodnotu do pole Text.</span><span class="sxs-lookup"><span data-stu-id="c300a-143">In the Text field, type a value.</span></span>

