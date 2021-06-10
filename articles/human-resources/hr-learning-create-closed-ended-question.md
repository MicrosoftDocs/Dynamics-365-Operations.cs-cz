---
title: Vytvoření dotazu s uzavřeným koncem
description: Dotazy s uzavřeným koncem umožňují poskytovat možnosti, ze kterých si respondent může vybírat.
author: andreabichsel
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KMAnswerCollection, KMAnswer, KMQuestion, HcmLearningWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b0316661d8be04cc5912e88bc50b3a1c7a73bbcb
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/18/2021
ms.locfileid: "6056677"
---
# <a name="create-a-closed-ended-question"></a><span data-ttu-id="ef185-103">Vytvoření dotazu s uzavřeným koncem</span><span class="sxs-lookup"><span data-stu-id="ef185-103">Create a closed ended question</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



<span data-ttu-id="ef185-104">Dotazy s uzavřeným koncem umožňují poskytovat možnosti, ze kterých si respondent může vybírat.</span><span class="sxs-lookup"><span data-stu-id="ef185-104">Closed-ended questions allow you to provide options for the respondent to choose from.</span></span> <span data-ttu-id="ef185-105">Nejprve je nutné vytvořit skupinu odpovědí s odpověďmi, a následně vytvořit dotaz, který bude používat skupinu odpovědí.</span><span class="sxs-lookup"><span data-stu-id="ef185-105">First, you need to create the Answer group with the answers, then create the question that will use the answer group.</span></span> <span data-ttu-id="ef185-106">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="ef185-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-an-answer-group"></a><span data-ttu-id="ef185-107">Vytvoření skupiny odpovědí</span><span class="sxs-lookup"><span data-stu-id="ef185-107">Create an answer group</span></span>
1. <span data-ttu-id="ef185-108">Přejít na Dotazník > Návrh > Skupiny odpovědí.</span><span class="sxs-lookup"><span data-stu-id="ef185-108">Go to Questionnaire > Design > Answer groups.</span></span>
2. <span data-ttu-id="ef185-109">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="ef185-109">Click New.</span></span>
3. <span data-ttu-id="ef185-110">Zadejte hodnotu do pole Skupina odpovědí.</span><span class="sxs-lookup"><span data-stu-id="ef185-110">In the Answer group field, type a value.</span></span>
4. <span data-ttu-id="ef185-111">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="ef185-111">In the Description field, type a value.</span></span>
    * <span data-ttu-id="ef185-112">Pomocí funkci Náhodně můžete náhodně umístit odpovědi v jiném pořadí pokaždé, když je pro otázku použita skupina odpovědí.</span><span class="sxs-lookup"><span data-stu-id="ef185-112">Use the Randomize functionality to randomly place the answers in a different order each time the answer group is used for a question.</span></span>  
5. <span data-ttu-id="ef185-113">Klepněte na tlačítko Odpověď.</span><span class="sxs-lookup"><span data-stu-id="ef185-113">Click Answer.</span></span>
6. <span data-ttu-id="ef185-114">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="ef185-114">Click New.</span></span>
    * <span data-ttu-id="ef185-115">Číselná řada určuje pořadí, v němž se zobrazují odpovědí, pokud není pro skupinu odpovědí vybrána možnost Náhodně.</span><span class="sxs-lookup"><span data-stu-id="ef185-115">Sequence number controls the order in which the answers are displayed, unless Randomize is selected for the Answer group.</span></span>  
    * <span data-ttu-id="ef185-116">Body můžete přidělit k odpovědím a použít je pro hodnocení dotazníku.</span><span class="sxs-lookup"><span data-stu-id="ef185-116">Points can be awarded to answers for use in scoring the questionnaire.</span></span>  
7. <span data-ttu-id="ef185-117">Do pole Body zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="ef185-117">In the Points field, enter a number.</span></span>
    * <span data-ttu-id="ef185-118">Správnou odpověď můžete nechat označit a určit tak, že vybraná odpověď je správná.</span><span class="sxs-lookup"><span data-stu-id="ef185-118">The correct answer can be marked to indicate that the selected answer is the correct one.</span></span> <span data-ttu-id="ef185-119">Tento údaj lze použít pro hodnocení dotazníku.</span><span class="sxs-lookup"><span data-stu-id="ef185-119">This can be used for scoring the questionnaire.</span></span>  
8. <span data-ttu-id="ef185-120">Zadejte hodnotu do pole Odpověď.</span><span class="sxs-lookup"><span data-stu-id="ef185-120">In the Answer field, type a value.</span></span>
    * <span data-ttu-id="ef185-121">Pokračujte ve vytváření možností výběru odpovědí pro skupinu odpovědí.</span><span class="sxs-lookup"><span data-stu-id="ef185-121">Continue to create answer selection options for the answer group.</span></span>  
9. <span data-ttu-id="ef185-122">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="ef185-122">Click New.</span></span>
10. <span data-ttu-id="ef185-123">Do pole Body zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="ef185-123">In the Points field, enter a number.</span></span>
11. <span data-ttu-id="ef185-124">Zadejte hodnotu do pole Odpověď.</span><span class="sxs-lookup"><span data-stu-id="ef185-124">In the Answer field, type a value.</span></span>
12. <span data-ttu-id="ef185-125">Klepněte na možnost Nový.</span><span class="sxs-lookup"><span data-stu-id="ef185-125">Click New.</span></span>
13. <span data-ttu-id="ef185-126">Do pole Body zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="ef185-126">In the Points field, enter a number.</span></span>
14. <span data-ttu-id="ef185-127">Zadejte hodnotu do pole Odpověď.</span><span class="sxs-lookup"><span data-stu-id="ef185-127">In the Answer field, type a value.</span></span>
15. <span data-ttu-id="ef185-128">Klepněte na možnost Nový.</span><span class="sxs-lookup"><span data-stu-id="ef185-128">Click New.</span></span>
16. <span data-ttu-id="ef185-129">Do pole Body zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="ef185-129">In the Points field, enter a number.</span></span>
17. <span data-ttu-id="ef185-130">Zadejte hodnotu do pole Odpověď.</span><span class="sxs-lookup"><span data-stu-id="ef185-130">In the Answer field, type a value.</span></span>
18. <span data-ttu-id="ef185-131">Klepněte na možnost Nový.</span><span class="sxs-lookup"><span data-stu-id="ef185-131">Click New.</span></span>
19. <span data-ttu-id="ef185-132">Do pole Body zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="ef185-132">In the Points field, enter a number.</span></span>
20. <span data-ttu-id="ef185-133">Zadejte hodnotu do pole Odpověď.</span><span class="sxs-lookup"><span data-stu-id="ef185-133">In the Answer field, type a value.</span></span>
21. <span data-ttu-id="ef185-134">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="ef185-134">Close the page.</span></span>
22. <span data-ttu-id="ef185-135">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="ef185-135">Close the page.</span></span>

## <a name="create-the-question"></a><span data-ttu-id="ef185-136">Vytvoření dotazu</span><span class="sxs-lookup"><span data-stu-id="ef185-136">Create the question</span></span>
1. <span data-ttu-id="ef185-137">Přejít na Dotazník > Návrh > Otázky.</span><span class="sxs-lookup"><span data-stu-id="ef185-137">Go to Questionnaire > Design > Questions.</span></span>
2. <span data-ttu-id="ef185-138">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="ef185-138">Click New.</span></span>
3. <span data-ttu-id="ef185-139">Pole Typ slouží k seskupení příbuzných dotazů.</span><span class="sxs-lookup"><span data-stu-id="ef185-139">Use the Type field to group related questions together.</span></span>
    * <span data-ttu-id="ef185-140">Pro dotazy s uzavřeným koncem můžete použít typy vstupu, jako např. Zaškrtávací políčko, Alternativní tlačítko nebo Pole se seznamem.</span><span class="sxs-lookup"><span data-stu-id="ef185-140">You can use input types of Check box, Alternative button, or Combo box for closed-ended questions.</span></span>  
4. <span data-ttu-id="ef185-141">Vyberte možnost v poli Typ vstupu.</span><span class="sxs-lookup"><span data-stu-id="ef185-141">In the Input type field, select an option.</span></span>
5. <span data-ttu-id="ef185-142">V poli Skupina odpovědí zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="ef185-142">In the Answer group field, enter or select a value.</span></span>
6. <span data-ttu-id="ef185-143">Zadejte hodnotu do pole Text.</span><span class="sxs-lookup"><span data-stu-id="ef185-143">In the Text field, type a value.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]