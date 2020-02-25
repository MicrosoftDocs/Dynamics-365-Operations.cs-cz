---
title: Nastavení dotazu jako závislého na odpovědi na předcházející otázku
description: Podmíněné otázky umožňují určit, jaké následující otázky budou prezentovány respondentům na základě odpovědi na předchozí otázku.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KMCollection, KMCollectionQuestion, KMCollectionQuestionTree
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a6e49814212b69a618fc3d855b7e290e6b6ff303
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008431"
---
# <a name="make-a-question-dependent-on-the-answer-of-the-previous-question"></a><span data-ttu-id="bdb82-103">Nastavení dotazu jako závislého na odpovědi na předcházející otázku</span><span class="sxs-lookup"><span data-stu-id="bdb82-103">Make a question dependent on the answer of the previous question</span></span>



<span data-ttu-id="bdb82-104">Podmíněné otázky umožňují určit, jaké následující otázky budou prezentovány respondentům na základě odpovědi na předchozí otázku.</span><span class="sxs-lookup"><span data-stu-id="bdb82-104">Conditional questions allow you to specify what follow-up question will be presented to a respondent, based on the answer to the preceding question.</span></span> <span data-ttu-id="bdb82-105">Například pokud je dotaz "Máte raději kávu nebo čaj?", je možné logickou následnou otázku určit v závislosti na tom, zda respondent vybere jako odpověď kávu nebo čaj.</span><span class="sxs-lookup"><span data-stu-id="bdb82-105">For example, if you ask "Do you prefer coffee or tea," a logical follow-up question can be determined depending on whether the respondent selects coffee or tea as their answer.</span></span> <span data-ttu-id="bdb82-106">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="bdb82-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="find-the-existing-questionnaire"></a><span data-ttu-id="bdb82-107">Vyhledání existujícího dotazníku</span><span class="sxs-lookup"><span data-stu-id="bdb82-107">Find the existing questionnaire</span></span>
1. <span data-ttu-id="bdb82-108">Přejděte na Dotazník > Návrh > Dotazníky.</span><span class="sxs-lookup"><span data-stu-id="bdb82-108">Go to Questionnaire > Design > Questionnaires.</span></span>
2. <span data-ttu-id="bdb82-109">Na seznamu vyberte dotazník WorkFH.</span><span class="sxs-lookup"><span data-stu-id="bdb82-109">In the list, select the WorkFH questionnaire.</span></span>

## <a name="add-all-questions-and-sub-questions-to-the-questionnaire"></a><span data-ttu-id="bdb82-110">Přidání všech otázek a dílčích otázek do dotazníku</span><span class="sxs-lookup"><span data-stu-id="bdb82-110">Add all questions and sub-questions to the Questionnaire</span></span>
1. <span data-ttu-id="bdb82-111">Klepněte na tlačítko Dotazy.</span><span class="sxs-lookup"><span data-stu-id="bdb82-111">Click Questions.</span></span>
2. <span data-ttu-id="bdb82-112">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="bdb82-112">Click New.</span></span>
3. <span data-ttu-id="bdb82-113">V poli Otázka vyberte otázku číslo 00016.</span><span class="sxs-lookup"><span data-stu-id="bdb82-113">In the Question field, select question number 00016.</span></span>
4. <span data-ttu-id="bdb82-114">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="bdb82-114">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="bdb82-115">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="bdb82-115">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="bdb82-116">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="bdb82-116">Click Save.</span></span>
7. <span data-ttu-id="bdb82-117">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="bdb82-117">Close the page.</span></span>

## <a name="set-the-questionnaire-sequence-to-conditional-and-make-the-question-dependent-on-the-appropriate-question"></a><span data-ttu-id="bdb82-118">Nastavte pořadí dotazníků na podmíněné a nastavte otázku tak, aby byla závislá na odpovídající otázce</span><span class="sxs-lookup"><span data-stu-id="bdb82-118">Set the Questionnaire Sequence to Conditional and make the question dependent on the appropriate question</span></span>
1. <span data-ttu-id="bdb82-119">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="bdb82-119">Click Edit.</span></span>
2. <span data-ttu-id="bdb82-120">Rozbalte sekci Nastavení.</span><span class="sxs-lookup"><span data-stu-id="bdb82-120">Expand the Setup section.</span></span>
3. <span data-ttu-id="bdb82-121">V poli Pořadí otázek vyberte Podmíněné.</span><span class="sxs-lookup"><span data-stu-id="bdb82-121">In the Question order field, select 'Conditional'.</span></span>
4. <span data-ttu-id="bdb82-122">Klikněte na Podmíněná otázka.</span><span class="sxs-lookup"><span data-stu-id="bdb82-122">Click Conditional question.</span></span>
5. <span data-ttu-id="bdb82-123">Ve stromovém zobrazení vyberte "Otázky/Vysvětlete, proč jste odpověděli na předchozí otázku tak, jak jste odpověděli".</span><span class="sxs-lookup"><span data-stu-id="bdb82-123">In the tree, select 'Questions\Explain why you answered the previous question the way you did?'.</span></span>
6. <span data-ttu-id="bdb82-124">V poli Prvotní otázka vyberte otázku 00009.</span><span class="sxs-lookup"><span data-stu-id="bdb82-124">In the Primary question field, select question 00009</span></span>
7. <span data-ttu-id="bdb82-125">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="bdb82-125">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="bdb82-126">V poli Odpověď zadejte pořadové ID odpovědi pro možnosti odpovědí, na kterých má být otázka závislá.</span><span class="sxs-lookup"><span data-stu-id="bdb82-126">In the Answer field, enter the answer sequence ID of the answer option you want to make the question dependent on.</span></span> <span data-ttu-id="bdb82-127">Pro první možnost odpovědi zadejte například 1.</span><span class="sxs-lookup"><span data-stu-id="bdb82-127">For example, enter 1 for the first answer option.</span></span>
9. <span data-ttu-id="bdb82-128">Klepněte na tlačítko Uložit.</span><span class="sxs-lookup"><span data-stu-id="bdb82-128">Click Save.</span></span>
10. <span data-ttu-id="bdb82-129">Ve stromovém zobrazení vyberte "Otázky\Jsem placen(a) odpovídajícím způsobem za prováděnou práci".</span><span class="sxs-lookup"><span data-stu-id="bdb82-129">In the tree, select 'Questions\I am paid fairly for the work I do.'.</span></span>
    * <span data-ttu-id="bdb82-130">Mějte na paměti, že strom otázek se aktualizuje a odráží závislosti.</span><span class="sxs-lookup"><span data-stu-id="bdb82-130">Note that the question tree updated to show the dependency.</span></span>  

