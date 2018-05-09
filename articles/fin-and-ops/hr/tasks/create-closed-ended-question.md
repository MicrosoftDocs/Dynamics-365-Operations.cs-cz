--- 
title: "Vytvoření dotazu s uzavřeným koncem"
description: "Dotazy s uzavřeným koncem umožňují poskytovat možnosti, ze kterých si respondent může vybírat."
author: kherr75
manager: AnnBe
ms.date: 06/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations, Talent
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 64afc316c7692101c2ad98a6cadc21204cfe5348
ms.contentlocale: cs-cz
ms.lasthandoff: 05/08/2018

---
# <a name="create-a-closed-ended-question"></a><span data-ttu-id="39afc-103">Vytvoření dotazu s uzavřeným koncem</span><span class="sxs-lookup"><span data-stu-id="39afc-103">Create a closed ended question</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="39afc-104">Dotazy s uzavřeným koncem umožňují poskytovat možnosti, ze kterých si respondent může vybírat.</span><span class="sxs-lookup"><span data-stu-id="39afc-104">Closed-ended questions allow you to provide options for the respondent to choose from.</span></span> <span data-ttu-id="39afc-105">Nejprve je nutné vytvořit skupinu odpovědí s odpověďmi, a následně vytvořit dotaz, který bude používat skupinu odpovědí.</span><span class="sxs-lookup"><span data-stu-id="39afc-105">First, you need to create the Answer group with the answers, then create the question that will use the answer group.</span></span> <span data-ttu-id="39afc-106">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="39afc-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-an-answer-group"></a><span data-ttu-id="39afc-107">Vytvoření skupiny odpovědí</span><span class="sxs-lookup"><span data-stu-id="39afc-107">Create an answer group</span></span>
1. <span data-ttu-id="39afc-108">Přejít na Dotazník > Návrh > Skupiny odpovědí.</span><span class="sxs-lookup"><span data-stu-id="39afc-108">Go to Questionnaire > Design > Answer groups.</span></span>
2. <span data-ttu-id="39afc-109">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="39afc-109">Click New.</span></span>
3. <span data-ttu-id="39afc-110">Zadejte hodnotu do pole Skupina odpovědí.</span><span class="sxs-lookup"><span data-stu-id="39afc-110">In the Answer group field, type a value.</span></span>
4. <span data-ttu-id="39afc-111">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="39afc-111">In the Description field, type a value.</span></span>
    * <span data-ttu-id="39afc-112">Pomocí funkci Náhodně můžete náhodně umístit odpovědi v jiném pořadí pokaždé, když je pro otázku použita skupina odpovědí.</span><span class="sxs-lookup"><span data-stu-id="39afc-112">Use the Randomize functionality to randomly place the answers in a different order each time the answer group is used for a question.</span></span>  
5. <span data-ttu-id="39afc-113">Klepněte na tlačítko Odpověď.</span><span class="sxs-lookup"><span data-stu-id="39afc-113">Click Answer.</span></span>
6. <span data-ttu-id="39afc-114">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="39afc-114">Click New.</span></span>
    * <span data-ttu-id="39afc-115">Číselná řada určuje pořadí, v němž se zobrazují odpovědí, pokud není pro skupinu odpovědí vybrána možnost Náhodně.</span><span class="sxs-lookup"><span data-stu-id="39afc-115">Sequence number controls the order in which the answers are displayed, unless Randomize is selected for the Answer group.</span></span>  
    * <span data-ttu-id="39afc-116">Body můžete přidělit k odpovědím a použít je pro hodnocení dotazníku.</span><span class="sxs-lookup"><span data-stu-id="39afc-116">Points can be awarded to answers for use in scoring the questionnaire.</span></span>  
7. <span data-ttu-id="39afc-117">Do pole Body zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="39afc-117">In the Points field, enter a number.</span></span>
    * <span data-ttu-id="39afc-118">Správnou odpověď můžete nechat označit a určit tak, že vybraná odpověď je správná.</span><span class="sxs-lookup"><span data-stu-id="39afc-118">The correct answer can be marked to indicate that the selected answer is the correct one.</span></span> <span data-ttu-id="39afc-119">Tento údaj lze použít pro hodnocení dotazníku.</span><span class="sxs-lookup"><span data-stu-id="39afc-119">This can be used for scoring the questionnaire.</span></span>  
8. <span data-ttu-id="39afc-120">Zadejte hodnotu do pole Odpověď.</span><span class="sxs-lookup"><span data-stu-id="39afc-120">In the Answer field, type a value.</span></span>
    * <span data-ttu-id="39afc-121">Pokračujte ve vytváření možností výběru odpovědí pro skupinu odpovědí.</span><span class="sxs-lookup"><span data-stu-id="39afc-121">Continue to create answer selection options for the answer group.</span></span>  
9. <span data-ttu-id="39afc-122">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="39afc-122">Click New.</span></span>
10. <span data-ttu-id="39afc-123">Do pole Body zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="39afc-123">In the Points field, enter a number.</span></span>
11. <span data-ttu-id="39afc-124">Zadejte hodnotu do pole Odpověď.</span><span class="sxs-lookup"><span data-stu-id="39afc-124">In the Answer field, type a value.</span></span>
12. <span data-ttu-id="39afc-125">Klepněte na možnost Nový.</span><span class="sxs-lookup"><span data-stu-id="39afc-125">Click New.</span></span>
13. <span data-ttu-id="39afc-126">Do pole Body zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="39afc-126">In the Points field, enter a number.</span></span>
14. <span data-ttu-id="39afc-127">Zadejte hodnotu do pole Odpověď.</span><span class="sxs-lookup"><span data-stu-id="39afc-127">In the Answer field, type a value.</span></span>
15. <span data-ttu-id="39afc-128">Klepněte na možnost Nový.</span><span class="sxs-lookup"><span data-stu-id="39afc-128">Click New.</span></span>
16. <span data-ttu-id="39afc-129">Do pole Body zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="39afc-129">In the Points field, enter a number.</span></span>
17. <span data-ttu-id="39afc-130">Zadejte hodnotu do pole Odpověď.</span><span class="sxs-lookup"><span data-stu-id="39afc-130">In the Answer field, type a value.</span></span>
18. <span data-ttu-id="39afc-131">Klepněte na možnost Nový.</span><span class="sxs-lookup"><span data-stu-id="39afc-131">Click New.</span></span>
19. <span data-ttu-id="39afc-132">Do pole Body zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="39afc-132">In the Points field, enter a number.</span></span>
20. <span data-ttu-id="39afc-133">Zadejte hodnotu do pole Odpověď.</span><span class="sxs-lookup"><span data-stu-id="39afc-133">In the Answer field, type a value.</span></span>
21. <span data-ttu-id="39afc-134">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="39afc-134">Close the page.</span></span>
22. <span data-ttu-id="39afc-135">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="39afc-135">Close the page.</span></span>

## <a name="create-the-question"></a><span data-ttu-id="39afc-136">Vytvoření dotazu</span><span class="sxs-lookup"><span data-stu-id="39afc-136">Create the question</span></span>
1. <span data-ttu-id="39afc-137">Přejít na Dotazník > Návrh > Otázky.</span><span class="sxs-lookup"><span data-stu-id="39afc-137">Go to Questionnaire > Design > Questions.</span></span>
2. <span data-ttu-id="39afc-138">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="39afc-138">Click New.</span></span>
3. <span data-ttu-id="39afc-139">Pole Typ slouží k seskupení příbuzných dotazů.</span><span class="sxs-lookup"><span data-stu-id="39afc-139">Use the Type field to group related questions together.</span></span>
    * <span data-ttu-id="39afc-140">Pro dotazy s uzavřeným koncem můžete použít typy vstupu, jako např. Zaškrtávací políčko, Alternativní tlačítko nebo Pole se seznamem.</span><span class="sxs-lookup"><span data-stu-id="39afc-140">You can use input types of Check box, Alternative button, or Combo box for closed-ended questions.</span></span>  
4. <span data-ttu-id="39afc-141">Vyberte možnost v poli Typ vstupu.</span><span class="sxs-lookup"><span data-stu-id="39afc-141">In the Input type field, select an option.</span></span>
5. <span data-ttu-id="39afc-142">V poli Skupina odpovědí zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="39afc-142">In the Answer group field, enter or select a value.</span></span>
6. <span data-ttu-id="39afc-143">Zadejte hodnotu do pole Text.</span><span class="sxs-lookup"><span data-stu-id="39afc-143">In the Text field, type a value.</span></span>


