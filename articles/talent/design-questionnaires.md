---
title: Návrh dotazníků
description: Toto téma popisuje postup vytváření dotazníku. Prvním krokem je návrh dotazníku. Při navrhování dotazníku můžete pouze zapsat otázky a odpovědi, ale také vytvořit strukturu, která umožňuje záznam a uspořádání odpovědí.
author: andreabichsel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KCMCollectionType, KMAnswerCollection, KMCollection
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 17341
ms.assetid: b27e2f12-c7a0-4a54-b8d8-17819f8a1c72
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.openlocfilehash: 6405b6a680f31c62e16f3bb707ec0a4ccdad3d23
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/18/2019
ms.locfileid: "2813907"
---
# <a name="design-questionnaires"></a><span data-ttu-id="24154-105">Návrh dotazníků</span><span class="sxs-lookup"><span data-stu-id="24154-105">Design questionnaires</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="24154-106">Toto téma popisuje postup vytváření dotazníku.</span><span class="sxs-lookup"><span data-stu-id="24154-106">This topic describes the process for creating a questionnaire.</span></span> <span data-ttu-id="24154-107">Prvním krokem je návrh dotazníku.</span><span class="sxs-lookup"><span data-stu-id="24154-107">The first step is to design the questionnaire.</span></span> <span data-ttu-id="24154-108">Při navrhování dotazníku můžete pouze zapsat otázky a odpovědi, ale také vytvořit strukturu, která umožňuje záznam a uspořádání odpovědí.</span><span class="sxs-lookup"><span data-stu-id="24154-108">When you design a questionnaire, you not only write the questions and answers, but also create the structure that enables answers to be recorded and tabulated.</span></span> 

<span data-ttu-id="24154-109">Pečlivě navržený dotazník pomáhá zvyšovat kvalitu dat, která shromažďujete.</span><span class="sxs-lookup"><span data-stu-id="24154-109">A carefully designed questionnaire can help increase the quality of the data that you collect.</span></span> <span data-ttu-id="24154-110">Díky promyšlenému návrhu můžete lépe a ve vhodný okamžik vybrat požadované otázky k dotazníku.</span><span class="sxs-lookup"><span data-stu-id="24154-110">Through careful design, you can better select the appropriate options at the appropriate time for a questionnaire.</span></span> <span data-ttu-id="24154-111">Následující body vám pomohou naplánovat efektivní dotazník:</span><span class="sxs-lookup"><span data-stu-id="24154-111">The following points can help you plan an effective questionnaire:</span></span>

-   <span data-ttu-id="24154-112">Jasně definovaný účel dotazníku je zajistit, aby otázky podporovaly účel.</span><span class="sxs-lookup"><span data-stu-id="24154-112">Clearly define the purpose of the questionnaire to help guarantee that the questions support the purpose.</span></span>
-   <span data-ttu-id="24154-113">Stanovte jednotlivce nebo skupiny osob, po kterých budete chtít dotazník vyplňovat.</span><span class="sxs-lookup"><span data-stu-id="24154-113">Determine the individual person or the group of people who should complete the questionnaire.</span></span>
-   <span data-ttu-id="24154-114">Zadejte otázky, které se zobrazí v dotazníku, a zahrňte možnosti odpovědí, je-li třeba.</span><span class="sxs-lookup"><span data-stu-id="24154-114">Write questions that will appear on the questionnaire, and include answer choices, if applicable.</span></span>
-   <span data-ttu-id="24154-115">Ujistěte se, že dotazník logicky plyne, aby respondenti zůstali aktivní.</span><span class="sxs-lookup"><span data-stu-id="24154-115">Be sure that the questionnaire flows logically, so that respondents remain engaged.</span></span>
-   <span data-ttu-id="24154-116">Otázky a odpovědi uspořádejte v pořadí, ve kterém se mají zobrazovat respondentům.</span><span class="sxs-lookup"><span data-stu-id="24154-116">Arrange questions and answers in the order that they should be presented to respondents in.</span></span>
-   <span data-ttu-id="24154-117">Rozhodněte se, jak by měly být vyhodnocovány výsledky, je-li třeba.</span><span class="sxs-lookup"><span data-stu-id="24154-117">Decide how the results should be evaluated, if applicable.</span></span>
-   <span data-ttu-id="24154-118">Rozhodněte, zda budete potřebovat další funkce.</span><span class="sxs-lookup"><span data-stu-id="24154-118">Decide whether you’ll need additional features.</span></span> <span data-ttu-id="24154-119">Například určete, zda a jak mají být výsledky kategorizovány, zda se požaduje časový limit nebo zda budou všechny otázky povinné.</span><span class="sxs-lookup"><span data-stu-id="24154-119">For example, determine whether and how results should be categorized, whether a time limit is required, or whether all the questions will be mandatory.</span></span>

<span data-ttu-id="24154-120">Návrhová fáze zahrnuje čtyři kategorie úkolů, které je třeba dokončit v následujícím pořadí:</span><span class="sxs-lookup"><span data-stu-id="24154-120">The design phase includes four categories of tasks that you must complete in this order:</span></span>

1.  <span data-ttu-id="24154-121">Nastavte předpoklady podle potřeby.</span><span class="sxs-lookup"><span data-stu-id="24154-121">Set up prerequisites, as required.</span></span>
2.  <span data-ttu-id="24154-122">Nastavte skupiny odpovědí a odpovědi podle potřeby.</span><span class="sxs-lookup"><span data-stu-id="24154-122">Set up answer groups and answers, if applicable.</span></span>
3.  <span data-ttu-id="24154-123">Nastavte otázky a jejich přiřazení ke skupinám odpovědí.</span><span class="sxs-lookup"><span data-stu-id="24154-123">Set up questions and their association with the answer groups.</span></span>
4.  <span data-ttu-id="24154-124">Nastavte dotazník jako takový a přiřaďte k němu otázky.</span><span class="sxs-lookup"><span data-stu-id="24154-124">Set up the questionnaire itself, and attach questions to it.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="24154-125">Požadavky</span><span class="sxs-lookup"><span data-stu-id="24154-125">Prerequisites</span></span>
<span data-ttu-id="24154-126">Některé předpoklady musí být stanoveny před vytvořením dotazníků, odpovědí a otázek.</span><span class="sxs-lookup"><span data-stu-id="24154-126">Some prerequisites must be in place before you can create questionnaires, answers, and questions.</span></span> <span data-ttu-id="24154-127">Avšak ne všechny předpoklady jsou nutné pro plnou funkčnost.</span><span class="sxs-lookup"><span data-stu-id="24154-127">However, not all prerequisites are required for full functionality.</span></span>

### <a name="required"></a><span data-ttu-id="24154-128">Požadováno</span><span class="sxs-lookup"><span data-stu-id="24154-128">Required</span></span>

| <span data-ttu-id="24154-129">Předpoklad</span><span class="sxs-lookup"><span data-stu-id="24154-129">Prerequisite</span></span>        | <span data-ttu-id="24154-130">Popis</span><span class="sxs-lookup"><span data-stu-id="24154-130">Description</span></span>                |
|---------------------|----------------------------|
| <span data-ttu-id="24154-131">Typy dotazníku</span><span class="sxs-lookup"><span data-stu-id="24154-131">Questionnaire types</span></span> | <span data-ttu-id="24154-132">Kategorizujte dotazníky.</span><span class="sxs-lookup"><span data-stu-id="24154-132">Categorize questionnaires.</span></span> |
| <span data-ttu-id="24154-133">Typy otázek</span><span class="sxs-lookup"><span data-stu-id="24154-133">Question types</span></span>      | <span data-ttu-id="24154-134">Kategorizujte otázky.</span><span class="sxs-lookup"><span data-stu-id="24154-134">Categorize questions.</span></span>      |

### <a name="optional"></a><span data-ttu-id="24154-135">Volitelné</span><span class="sxs-lookup"><span data-stu-id="24154-135">Optional</span></span>

| <span data-ttu-id="24154-136">Předpoklad</span><span class="sxs-lookup"><span data-stu-id="24154-136">Prerequisite</span></span>             | <span data-ttu-id="24154-137">Popis</span><span class="sxs-lookup"><span data-stu-id="24154-137">Description</span></span>                                                    |
|--------------------------|----------------------------------------------------------------|
| <span data-ttu-id="24154-138">Parametry dotazníků</span><span class="sxs-lookup"><span data-stu-id="24154-138">Questionnaire parameters</span></span> | <span data-ttu-id="24154-139">Upravte základní ovládací prvky a výchozí nastavení pro dotazníky.</span><span class="sxs-lookup"><span data-stu-id="24154-139">Modify basic controls and default settings for questionnaires.</span></span> |

### <a name="questionnaire-types"></a><span data-ttu-id="24154-140">Typy dotazníku</span><span class="sxs-lookup"><span data-stu-id="24154-140">Questionnaire types</span></span>

<span data-ttu-id="24154-141">Typy dotazníků jsou povinné a musí být přiřazeny při vytváření dotazníku.</span><span class="sxs-lookup"><span data-stu-id="24154-141">Questionnaire types are required and must be assigned when you create a questionnaire.</span></span> <span data-ttu-id="24154-142">Typy dotazníku umožňují snadněji spravovat a klasifikovat dotazníky.</span><span class="sxs-lookup"><span data-stu-id="24154-142">Questionnaire types help you manage and classify questionnaires more easily.</span></span> <span data-ttu-id="24154-143">Typy dotazníků slouží ke klasifikaci dotazníků a jejich odlišení od sebe navzájem.</span><span class="sxs-lookup"><span data-stu-id="24154-143">Use questionnaire types to classify questionnaires and differentiate them from each other.</span></span> <span data-ttu-id="24154-144">Pokud máte například několik dotazníků, ze kterých můžete vybírat, můžete je filtrovat podle typu a usnadnit tak hledání specifického dotazníku.</span><span class="sxs-lookup"><span data-stu-id="24154-144">For example, if you have multiple questionnaires to select from, you can filter them by type to help make it easier to find a particular questionnaire.</span></span> <span data-ttu-id="24154-145">Následuje několik příkladů typů dotazníku:</span><span class="sxs-lookup"><span data-stu-id="24154-145">Here are some examples of questionnaire types:</span></span>

-   <span data-ttu-id="24154-146">Rozvoj lidských zdrojů</span><span class="sxs-lookup"><span data-stu-id="24154-146">Human resource development</span></span>
-   <span data-ttu-id="24154-147">Průzkumy odběratelů</span><span class="sxs-lookup"><span data-stu-id="24154-147">Customer surveys</span></span>
-   <span data-ttu-id="24154-148">Proces kontroly</span><span class="sxs-lookup"><span data-stu-id="24154-148">Review process</span></span>

### <a name="question-types"></a><span data-ttu-id="24154-149">Typy otázek</span><span class="sxs-lookup"><span data-stu-id="24154-149">Question types</span></span>

<span data-ttu-id="24154-150">Typy otázek jsou povinné a musí být přiřazeny při vytváření otázky.</span><span class="sxs-lookup"><span data-stu-id="24154-150">Question types are required and must be assigned when you create a question.</span></span> 

<span data-ttu-id="24154-151">Typy otázek se používají k rozdělení otázek do kategorií pro účely vykazování.</span><span class="sxs-lookup"><span data-stu-id="24154-151">Use question types to categorize questions for reporting.</span></span> <span data-ttu-id="24154-152">Typy otázek také usnadňují hledání otázek, protože typy slouží jako filtry na stránce **Otázky**.</span><span class="sxs-lookup"><span data-stu-id="24154-152">Question types also make it easier to find questions, because you can use types as filters on the **Questions** page.</span></span> <span data-ttu-id="24154-153">Následuje několik příkladů typů otázek:</span><span class="sxs-lookup"><span data-stu-id="24154-153">Here are some examples of question types:</span></span>

-   <span data-ttu-id="24154-154">Lidské zdroje</span><span class="sxs-lookup"><span data-stu-id="24154-154">Human resource</span></span>
-   <span data-ttu-id="24154-155">Řízení podniku</span><span class="sxs-lookup"><span data-stu-id="24154-155">Managing business</span></span>
-   <span data-ttu-id="24154-156">Hodnocení kurzu</span><span class="sxs-lookup"><span data-stu-id="24154-156">Course evaluation</span></span>

### <a name="questionnaire-parameters"></a><span data-ttu-id="24154-157">Parametry dotazníků</span><span class="sxs-lookup"><span data-stu-id="24154-157">Questionnaire parameters</span></span>

<span data-ttu-id="24154-158">Parametry dotazníku jsou volitelné.</span><span class="sxs-lookup"><span data-stu-id="24154-158">Questionnaire parameters are optional.</span></span> <span data-ttu-id="24154-159">Nemusíte je použít, v závislosti na požadavcích vaší společnosti.</span><span class="sxs-lookup"><span data-stu-id="24154-159">You might not use them, depending on your company’s requirements.</span></span> 

<span data-ttu-id="24154-160">Parametry dotazníku definují anonymitu, kódy číselných řad a typy odkazů dotazníku.</span><span class="sxs-lookup"><span data-stu-id="24154-160">Questionnaire parameters define the anonymity, number sequence codes, and reference types of a questionnaire.</span></span> <span data-ttu-id="24154-161">Když organizace distribuuje dotazník, může být třeba možnost respondentům umožnit, aby zůstali anonymní.</span><span class="sxs-lookup"><span data-stu-id="24154-161">When an organization distributes a questionnaire, the option to allow respondents to remain anonymous might be of concern.</span></span> 

<span data-ttu-id="24154-162">Kódy číselných řad se používají k uspořádání otázek a odpovědí.</span><span class="sxs-lookup"><span data-stu-id="24154-162">The number sequence codes are used to organize questions and answers.</span></span> <span data-ttu-id="24154-163">Na základě těchto kódů číselných řad jsou hodnoty automaticky přiřazeny k položkám.</span><span class="sxs-lookup"><span data-stu-id="24154-163">Based on these number sequence codes, values are automatically assigned to items.</span></span> 

<span data-ttu-id="24154-164">Dříve než začnete definovat vaše data, měli byste definovat veškeré parametry.</span><span class="sxs-lookup"><span data-stu-id="24154-164">You should define all parameters before you begin to create your data.</span></span> <span data-ttu-id="24154-165">Vaše parametrů dotazníku můžete kdykoliv upravit.</span><span class="sxs-lookup"><span data-stu-id="24154-165">You can modify the questionnaire parameter settings at any time.</span></span>

## <a name="questionnaire-components"></a><span data-ttu-id="24154-166">Komponenty dotazníku</span><span class="sxs-lookup"><span data-stu-id="24154-166">Questionnaire components</span></span>
<span data-ttu-id="24154-167">Dotazníky zahrnují tři hlavní prvky: skupiny odpovědí, které obsahují odpovědi pro otázky s možností více odpovědí, otázky a dotazník jako takový.</span><span class="sxs-lookup"><span data-stu-id="24154-167">Questionnaires comprise three main elements: answer groups that contain the answers for multiple choice questions, questions, and the questionnaire itself.</span></span><span data-ttu-id="24154-168">Volitelně lze otázky v dotazníku seskupit do skupin výsledků.</span><span class="sxs-lookup"><span data-stu-id="24154-168"> You can optionally group the questions on a questionnaire into result groups.</span></span> <span data-ttu-id="24154-169">Skupiny výsledků umožňují rozdělit otázky do kategorií a poskytují další analýzy v dotazníku.</span><span class="sxs-lookup"><span data-stu-id="24154-169">Result groups let you categorize questions and provide further analysis on the questionnaire.</span></span> 

<span data-ttu-id="24154-170">[![Komponenty dotazníku](./media/questionnairecomponents-1024x615.png)](./media/questionnairecomponents.png)</span><span class="sxs-lookup"><span data-stu-id="24154-170">[![QuestionnaireComponents](./media/questionnairecomponents-1024x615.png)](./media/questionnairecomponents.png)</span></span>

### <a name="answer-groups-and-answers"></a><span data-ttu-id="24154-171">Skupiny odpovědí a odpovědi</span><span class="sxs-lookup"><span data-stu-id="24154-171">Answer groups and answers</span></span>

<span data-ttu-id="24154-172">Respondenti mohou na otázku odpovědět dvěma způsoby v závislosti na předmětu otázky:</span><span class="sxs-lookup"><span data-stu-id="24154-172">Respondents can answer a question in two ways, depending on the subject of the question:</span></span>

-   <span data-ttu-id="24154-173">Otevřené otázky nevyžadují odpovědi v určitém formátu.</span><span class="sxs-lookup"><span data-stu-id="24154-173">Open-ended questions don’t require responses in a specific format.</span></span> <span data-ttu-id="24154-174">Respondenti mohou odpověď zadat jako text, číslo, datum nebo čas.</span><span class="sxs-lookup"><span data-stu-id="24154-174">Respondents can type a response as text, a number, a date, or a time.</span></span> <span data-ttu-id="24154-175">Tyto otázky obvykle vyžadují, aby respondenti zadali subjektivní informace, jako je například názor, popis, hodnocení nebo odhad.</span><span class="sxs-lookup"><span data-stu-id="24154-175">These questions typically require that the respondents provide subjective information in their answers, such as an opinion, description, evaluation, or estimate.</span></span>
-   <span data-ttu-id="24154-176">Uzavřené otázky vyžadují, aby respondent vybral odpověď ze seznamu možných správných odpovědí.</span><span class="sxs-lookup"><span data-stu-id="24154-176">Closed-ended questions require that the respondent select an answer in a list of possible correct answers.</span></span>

<span data-ttu-id="24154-177">Chcete-li poskytnout seznam možných odpovědí pro uzavřené otázky, můžete vytvořit odpovědi na stránce **Skupiny odpovědí**.</span><span class="sxs-lookup"><span data-stu-id="24154-177">To provide a list of possible answers for closed-ended questions, you can create answers on the **Answer groups** page.</span></span> 

<span data-ttu-id="24154-178">Skupiny odpovědí a odpovědi jsou součásti hlavní části informací, ze kterých jsou otázky vytvořeny.</span><span class="sxs-lookup"><span data-stu-id="24154-178">Answer groups and answers are components that make up the main body of information that questions are created from.</span></span> <span data-ttu-id="24154-179">Po vytvoření skupiny odpovědí můžete skupinu odpovědí přiřadit k otázce v poli **Skupina odpovědí**na stránce **Otázky**.</span><span class="sxs-lookup"><span data-stu-id="24154-179">After you create an answer group, you can associate the answer group with a question in the **Answer group** field on the **Questions** page.</span></span> 

<span data-ttu-id="24154-180">Skupinu odpovědí lze použít pro více otázek ve jednom dotazníku a pro více dotazníků.</span><span class="sxs-lookup"><span data-stu-id="24154-180">An answer group can be used for more than one question on the same questionnaire, and can also be used on more than one questionnaire.</span></span> 

> [!NOTE]
> <span data-ttu-id="24154-181">Pokud změníte textu odpovědi ve skupinách odpovědí, které již byly použity u vyplněných dotazníků, data může být obtížné vyhodnotit a výsledky dotazníku mohou být neplatné.</span><span class="sxs-lookup"><span data-stu-id="24154-181">If you modify answer text in answer groups that have already been used on completed questionnaires, data can become difficult to evaluate, and questionnaire results might no longer be valid.</span></span> <span data-ttu-id="24154-182">Pokud musíte změnit skupinu odpovědí, zvažte vytvoření nové skupiny odpovědí namísto změny již existující skupiny.</span><span class="sxs-lookup"><span data-stu-id="24154-182">If you must change an answer group, consider creating a new answer group instead of changing an existing one.</span></span> <span data-ttu-id="24154-183">Skupiny odpovědí, které byly přiřazeny k určité otázce či odpovědi, nebo které byly zodpovězeny, není možné odstranit.</span><span class="sxs-lookup"><span data-stu-id="24154-183">You can't delete answer groups that are attached to a question or answer, or that have been answered.</span></span>

### <a name="questions"></a><span data-ttu-id="24154-184">Otázky</span><span class="sxs-lookup"><span data-stu-id="24154-184">Questions</span></span>

<span data-ttu-id="24154-185">Dotazník musí obsahovat otázky.</span><span class="sxs-lookup"><span data-stu-id="24154-185">A questionnaire must contain questions.</span></span> <span data-ttu-id="24154-186">Otázky mohou být otevřené nebo uzavřené.</span><span class="sxs-lookup"><span data-stu-id="24154-186">Questions can be either open-ended or closed-ended.</span></span>

-   <span data-ttu-id="24154-187">Odpovědi na otevřené otázky nejsou řízeny a respondenti mohou své odpovědi zadat.</span><span class="sxs-lookup"><span data-stu-id="24154-187">The responses to open-ended questions aren't controlled, and respondents can type their answers.</span></span>
-   <span data-ttu-id="24154-188">Uzavřené otázky vyžadují seznam předdefinovaných možností odpovědí a otázky mohou být strukturovány tak, aby mohl respondent vybrat více odpovědí.</span><span class="sxs-lookup"><span data-stu-id="24154-188">Closed-ended questions require a list of predefined response options, and the questions can be structured to let a respondent select multiple responses.</span></span> <span data-ttu-id="24154-189">Otázky by měly být formulovány tak, aby bylo možné od respondenta získat konkrétní informace a musí být propojeny se skupinou odpovědí, která obsahuje možnosti odpovědí pro každou uzavřenou otázku.</span><span class="sxs-lookup"><span data-stu-id="24154-189">Questions should be designed to elicit specific information from a respondent and must be linked to an answer group that provides the response options for each closed-ended question.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="24154-190">Před nastavením uzavřených otázek je nutné vytvořit skupiny odpovědí a odpovědi.</span><span class="sxs-lookup"><span data-stu-id="24154-190">Before you can set up closed-ended questions, you must create answer groups and answers.</span></span>

<span data-ttu-id="24154-191">Otázky lze uspořádat do hierarchie podmíněných otázek tak, aby druhotné otázky závisely na odpovědi, kterou respondent vybere pro předchozí otázku.</span><span class="sxs-lookup"><span data-stu-id="24154-191">Questions can be arranged in a conditional question hierarchy, so that secondary questions depend on the answer that the respondent selects for the previous question.</span></span> <span data-ttu-id="24154-192">Můžete nejprve napsat otázky a poté je uspořádat do hierarchie.</span><span class="sxs-lookup"><span data-stu-id="24154-192">You can write the questions first and then arrange them into a hierarchy later.</span></span>

## <a name="setting-up-questionnaires"></a><span data-ttu-id="24154-193">Nastavení dotazníků</span><span class="sxs-lookup"><span data-stu-id="24154-193">Setting up questionnaires</span></span>

> [!NOTE]
> <span data-ttu-id="24154-194">Před nastavením dotazníku je nutné nastavit odpovědi, dotazy a požadavky.</span><span class="sxs-lookup"><span data-stu-id="24154-194">Before you can set up a questionnaire, you must set up answers, questions, and prerequisites.</span></span> 

<span data-ttu-id="24154-195">U jednotlivých dotazníků lze určit následující údaje:</span><span class="sxs-lookup"><span data-stu-id="24154-195">For each questionnaire, you can specify the following information:</span></span>

-   <span data-ttu-id="24154-196">Celkový čas nebo časový limit pro zodpovězení povinných otázek.</span><span class="sxs-lookup"><span data-stu-id="24154-196">The total time or time limit to answer mandatory questions.</span></span>
-   <span data-ttu-id="24154-197">Zda jsou všechny otázky povinné.</span><span class="sxs-lookup"><span data-stu-id="24154-197">Whether all questions are mandatory.</span></span>
-   <span data-ttu-id="24154-198">Zda mají být vypočítány body v dotazníku.</span><span class="sxs-lookup"><span data-stu-id="24154-198">Whether to calculate points on a questionnaire.</span></span>
-   <span data-ttu-id="24154-199">Jak mají být výsledky rozděleny do kategorií.</span><span class="sxs-lookup"><span data-stu-id="24154-199">How to categorize results.</span></span>
-   <span data-ttu-id="24154-200">Zda bude dotazník k dispozici pro omezenou skupinu respondentů.</span><span class="sxs-lookup"><span data-stu-id="24154-200">Whether the questionnaire will be available to a restricted set of respondents.</span></span>
-   <span data-ttu-id="24154-201">Zda má být šablona formuláře zobrazena jako pozadí každé stránky dotazníku.</span><span class="sxs-lookup"><span data-stu-id="24154-201">Whether a form template should be displayed as a background behind each page of the questionnaire.</span></span>
-   <span data-ttu-id="24154-202">Zda jsou nutné doplňující poznámky objasňující respondentům účel dotazníku.</span><span class="sxs-lookup"><span data-stu-id="24154-202">Whether additional notes are required in order to clarify the intent of the questionnaire for the respondents.</span></span>
-   <span data-ttu-id="24154-203">Zda chcete zobrazit otázky v daném pořadí nebo je náhodně vybírat ze zdroje.</span><span class="sxs-lookup"><span data-stu-id="24154-203">Whether to display questions in a fixed order or randomly select them from a pool.</span></span>
-   <span data-ttu-id="24154-204">Zda budou otázky pokládány, pouze pokud byly pro předchozí odpovědi zadány konkrétní odpovědi.</span><span class="sxs-lookup"><span data-stu-id="24154-204">Whether questions will be asked only if specific responses are given for previous answers.</span></span>

### <a name="set-up-a-questionnaire"></a><span data-ttu-id="24154-205">Nastavení dotazníku</span><span class="sxs-lookup"><span data-stu-id="24154-205">Set up a questionnaire</span></span>

<span data-ttu-id="24154-206">Primární stránka, kterou použijete k nastavení dotazníku, je stránka **Dotazníky**.</span><span class="sxs-lookup"><span data-stu-id="24154-206">The primary page that you use to set up a questionnaire is the **Questionnaires** page.</span></span> <span data-ttu-id="24154-207">Chcete-li nastavit dotazník, proveďte následující úkony v uvedeném pořadí:</span><span class="sxs-lookup"><span data-stu-id="24154-207">To set up a questionnaire, complete the following tasks in order:</span></span>

1.  <span data-ttu-id="24154-208">Vytvořte dotazník.</span><span class="sxs-lookup"><span data-stu-id="24154-208">Create a questionnaire.</span></span>
2.  <span data-ttu-id="24154-209">Proveďte jeden z následujících kroků pro připojení otázek k dotazníku:</span><span class="sxs-lookup"><span data-stu-id="24154-209">Follow one of these steps to attach questions to the questionnaire:</span></span>
    -   <span data-ttu-id="24154-210">Pokud používáte skupiny výsledků, otázky je možné přiřadit do dotazníku pomocí skupin výsledků.</span><span class="sxs-lookup"><span data-stu-id="24154-210">If you're using result groups, you can attach questions to a questionnaire by using result groups.</span></span> <span data-ttu-id="24154-211">Nejprve nastavte skupiny výsledků dotazníku a pak přidejte do skupiny výsledků otázky.</span><span class="sxs-lookup"><span data-stu-id="24154-211">First set up the result groups for the questionnaire, and then add questions to the result groups.</span></span>
    -   <span data-ttu-id="24154-212">Pokud nepoužíváte skupiny výsledků, otázky je možné přiřadit přímo do dotazníku.</span><span class="sxs-lookup"><span data-stu-id="24154-212">If you aren't using result groups, you can attach questions directly to the questionnaire.</span></span>

3.  <span data-ttu-id="24154-213">Nastavte hierarchii podmíněných otázek, je-li třeba.</span><span class="sxs-lookup"><span data-stu-id="24154-213">Set up a conditional question hierarchy, if it's required.</span></span>
4.  <span data-ttu-id="24154-214">Otestujte dotazník.</span><span class="sxs-lookup"><span data-stu-id="24154-214">Test the questionnaire.</span></span>

<span data-ttu-id="24154-215">Na stránce **Dotazníky** kliknutím na možnost **Ověřit** otestujte, zda je dotazník správně sestaven.</span><span class="sxs-lookup"><span data-stu-id="24154-215">On the **Questionnaires** page, click **Validate** to test whether the questionnaire is assembled correctly.</span></span> <span data-ttu-id="24154-216">Doporučujeme však vyplnit otazník a otestovat jej sami před distribucí.</span><span class="sxs-lookup"><span data-stu-id="24154-216">However, it's also a good idea to complete the questionnaire and test it yourself before you distribute it.</span></span>

### <a name="modify-a-questionnaire"></a><span data-ttu-id="24154-217">Úprava dotazníku</span><span class="sxs-lookup"><span data-stu-id="24154-217">Modify a questionnaire</span></span>

<span data-ttu-id="24154-218">Na stránce **Dotazníky** můžete provést následující úkoly:</span><span class="sxs-lookup"><span data-stu-id="24154-218">You can complete the following tasks on the **Questionnaires** page:</span></span>

-   <span data-ttu-id="24154-219">Upravovat informace v dotazníku, například skupiny výsledků a otázky.</span><span class="sxs-lookup"><span data-stu-id="24154-219">Modify information in the questionnaire, such as the result groups and questions.</span></span>
-   <span data-ttu-id="24154-220">Odstraňovat a přidávat otázky.</span><span class="sxs-lookup"><span data-stu-id="24154-220">Delete and add questions.</span></span>
-   <span data-ttu-id="24154-221">Provádět změny ve skupinách výsledků a v pořadovém čísle.</span><span class="sxs-lookup"><span data-stu-id="24154-221">Make changes in the result groups and sequence number.</span></span> 

> [!CAUTION]
> <span data-ttu-id="24154-222">Při provádění změn v dotaznících, které již byly zodpovězeny, postupujte opatrně.</span><span class="sxs-lookup"><span data-stu-id="24154-222">Be careful when you change questionnaires that have already been answered.</span></span> <span data-ttu-id="24154-223">Změny mohou snížit přesnost statistiky, což může ovlivnit kvalitu podkladů pro vyhodnocení.</span><span class="sxs-lookup"><span data-stu-id="24154-223">Changes can reduce the accuracy of statistics and therefore make them a poor basis for evaluation.</span></span> <span data-ttu-id="24154-224">Místo toho, abyste měnili otázku, která již byla zodpovězena, zvažte vytvoření nové otázky.</span><span class="sxs-lookup"><span data-stu-id="24154-224">Consider creating a new question instead of changing a question that has already been answered.</span></span>

<span data-ttu-id="24154-225">V dotazníku nelze odstranit následujících typy otázek:</span><span class="sxs-lookup"><span data-stu-id="24154-225">In a questionnaire, you can't delete the following types of questions:</span></span>

-   <span data-ttu-id="24154-226">Otázky, které jsou připojeny k dotazníku</span><span class="sxs-lookup"><span data-stu-id="24154-226">Questions that are attached to a questionnaire</span></span>
-   <span data-ttu-id="24154-227">Otázky, které již byly zodpovězeny a proto se zobrazí v dialogu **Odpovědi**.</span><span class="sxs-lookup"><span data-stu-id="24154-227">Questions that have already been answered and therefore appear in the **Answers** dialog box.</span></span>

### <a name="result-groups"></a><span data-ttu-id="24154-228">Skupiny výsledků</span><span class="sxs-lookup"><span data-stu-id="24154-228">Result groups</span></span>

<span data-ttu-id="24154-229">Při připojování otázek k dotazníku jsou skupiny výsledků volitelné.</span><span class="sxs-lookup"><span data-stu-id="24154-229">Result groups are optional when you attach questions to a questionnaire.</span></span> 

<span data-ttu-id="24154-230">Skupiny výsledků se používají pro výpočet bodů a kategorizaci výsledků dotazníku.</span><span class="sxs-lookup"><span data-stu-id="24154-230">A result group is used to calculate points and categorize the results of a questionnaire.</span></span> <span data-ttu-id="24154-231">Při použití skupin výsledků můžete provádět následující úkoly:</span><span class="sxs-lookup"><span data-stu-id="24154-231">If you use result groups, you can perform the following tasks:</span></span>

-   <span data-ttu-id="24154-232">Vyhodnoťte výsledky dotazníků na základě statistik bodů.</span><span class="sxs-lookup"><span data-stu-id="24154-232">Evaluate questionnaire results, based on point statistics.</span></span>
-   <span data-ttu-id="24154-233">Vyhodnoťte výsledek respondenta pro každou skupinu výsledků, kterou nastavíte.</span><span class="sxs-lookup"><span data-stu-id="24154-233">Evaluate a respondent’s score for each result group that you set up.</span></span>
-   <span data-ttu-id="24154-234">Generovat statistiku pro každou skupinu výsledků, což vám může pomoci analyzovat výsledky.</span><span class="sxs-lookup"><span data-stu-id="24154-234">Generate statistics for each result group to help you analyze results.</span></span>
-   <span data-ttu-id="24154-235">Vytiskněte sestavu, který zobrazuje výsledky pro každou skupinu výsledků a také volitelné body a texty, které jsou založeny na bodech získaných v každé skupině výsledků.</span><span class="sxs-lookup"><span data-stu-id="24154-235">Print a report that shows results for each result group, and also optional points/texts that are based on points that are earned in each result group.</span></span>

> [!NOTE]
> <span data-ttu-id="24154-236">Před nastavením skupin výsledků je nutné dokončit následující úkoly:</span><span class="sxs-lookup"><span data-stu-id="24154-236">Before you can set up result groups, you must complete the following tasks:</span></span>

-   <span data-ttu-id="24154-237">Nastavte uzavřené otázky.</span><span class="sxs-lookup"><span data-stu-id="24154-237">Set up closed-ended questions.</span></span> <span data-ttu-id="24154-238">Pro uzavřenou otázku musí být tato zadání na stránce **Otázky** nastavena na **Zaškrtávací políčko**, **Alternativní tlačítko** nebo **Pole se seznamem**.</span><span class="sxs-lookup"><span data-stu-id="24154-238">For a closed-ended question, the input type on the **Questions** page must be **Check box**, **Alternative button**, or **Combo box**.</span></span>
-   <span data-ttu-id="24154-239">Definujte body pro odpovědi ve skupinách odpovědí, které jsou přiřazeny jednotlivým otázkám.</span><span class="sxs-lookup"><span data-stu-id="24154-239">Define points for answers in the answer groups that are assigned to each question.</span></span>
-   <span data-ttu-id="24154-240">Nastavte dotazník.</span><span class="sxs-lookup"><span data-stu-id="24154-240">Set up a questionnaire.</span></span>

<span data-ttu-id="24154-241">Chcete-li připojení otázky k dotazníku pomocí skupin výsledků, nejprve nastavte skupiny výsledků pro dotazník a pak přidejte do skupiny výsledků otázky.</span><span class="sxs-lookup"><span data-stu-id="24154-241">To attach questions to a questionnaire by using result groups, first set up the result groups for the questionnaire, and then add questions to the result groups.</span></span> <span data-ttu-id="24154-242">Pokud nepoužíváte skupiny výsledků, otázky je možné přiřadit přímo do dotazníku.</span><span class="sxs-lookup"><span data-stu-id="24154-242">If you don't use result groups, you can attach questions directly to a questionnaire.</span></span> 

<span data-ttu-id="24154-243">Nastavte více skupin výsledků a vyhodnoťte body, které respondent získá za jednotlivé kategorie.</span><span class="sxs-lookup"><span data-stu-id="24154-243">You can set up multiple result groups to evaluate the points that a respondent earns in each category.</span></span> <span data-ttu-id="24154-244">Po vyplnění dotazníku můžete zobrazit body, které byly získány pro jednotlivé skupiny výsledků.</span><span class="sxs-lookup"><span data-stu-id="24154-244">After a questionnaire is completed, you can view the points that have been achieved for each result group.</span></span> 

> [!TIP]
> <span data-ttu-id="24154-245">Chcete-li vyhodnocovat dotazník pomocí bodů, ale nikoli samostatných kategorií, můžete přidat všechny otázky do jedné skupiny výsledků.</span><span class="sxs-lookup"><span data-stu-id="24154-245">To evaluate a questionnaire by using points but not separate categories, you can add all questions to a single result group.</span></span> 

<span data-ttu-id="24154-246">Pro každou skupinu výsledků můžete také nastavit jednu nebo více zpráv založených na bodech, které respondent získá po vyplnění dotazníku.</span><span class="sxs-lookup"><span data-stu-id="24154-246">For each result group, you can also set up one or more point-based messages that respondents receive after they complete a questionnaire.</span></span> <span data-ttu-id="24154-247">Zobrazený text se může lišit v závislosti na výsledku, jehož respondenti dosáhnou ve skupině výsledků.</span><span class="sxs-lookup"><span data-stu-id="24154-247">The text that is shown can vary, depending on the score that a respondent achieves in a result group.</span></span> <span data-ttu-id="24154-248">Chcete-li použít zprávy založené na bodech, musíte definovat intervaly bodů a popis každého intervalu.</span><span class="sxs-lookup"><span data-stu-id="24154-248">To use point-based messages, you must define point intervals and a description of each interval.</span></span> <span data-ttu-id="24154-249">Když respondent získá hodnocení určitého intervalu, bude text zahrnut do sestavy výsledků.</span><span class="sxs-lookup"><span data-stu-id="24154-249">When a respondent achieves a score in a specific interval, the text for that interval is included on the results report.</span></span> 

<span data-ttu-id="24154-250">Vzhledem k tomu, že skupina výsledků souvisí s body, které jsou přiřazeny konkrétní sadě otázek v dotazníku, můžete pro dotazník použít pouze určitou skupinu výsledků.</span><span class="sxs-lookup"><span data-stu-id="24154-250">Because a result group is related to the points that are associated with specific sets of questions on a questionnaire, you can use only a specific result group for a questionnaire.</span></span>

#### <a name="example-pointstexts-for-result-group-3"></a><span data-ttu-id="24154-251">Příklad: Body/text pro skupinu výsledků 3</span><span class="sxs-lookup"><span data-stu-id="24154-251">Example: Points/texts for result group 3</span></span>

<span data-ttu-id="24154-252">Používáte dotazník pro test vedení s 15 otázkami ve třech kategoriích.</span><span class="sxs-lookup"><span data-stu-id="24154-252">You're using a questionnaire for a leadership test that has 15 questions in three categories.</span></span> <span data-ttu-id="24154-253">Můžete vytvořit tři skupiny výsledků a přidat pět otázek pro každou skupinu výsledků.</span><span class="sxs-lookup"><span data-stu-id="24154-253">You create three result groups and add five questions to each result group.</span></span> <span data-ttu-id="24154-254">Body jsou poté sečteny ve třech skupinách.</span><span class="sxs-lookup"><span data-stu-id="24154-254">Points are then totaled in the three groups.</span></span> <span data-ttu-id="24154-255">Tři skupiny výsledků jsou následující:</span><span class="sxs-lookup"><span data-stu-id="24154-255">The three result groups are as follows:</span></span>

-   <span data-ttu-id="24154-256">kreativní schopnosti,</span><span class="sxs-lookup"><span data-stu-id="24154-256">Creative abilities</span></span>
-   <span data-ttu-id="24154-257">vedoucí schopnosti,</span><span class="sxs-lookup"><span data-stu-id="24154-257">Leadership abilities</span></span>
-   <span data-ttu-id="24154-258">technické schopnosti.</span><span class="sxs-lookup"><span data-stu-id="24154-258">Technical abilities</span></span>

<span data-ttu-id="24154-259">Chcete-li použít zprávy založené na bodech, nastavte intervaly textu pro každou skupinu výsledků.</span><span class="sxs-lookup"><span data-stu-id="24154-259">To use point-based messages, you set up text intervals for each result group.</span></span> <span data-ttu-id="24154-260">Každé otázce jsou přiděleny dva body.</span><span class="sxs-lookup"><span data-stu-id="24154-260">Each question is assigned two points.</span></span> <span data-ttu-id="24154-261">Maximální počet bodů v jednotlivých skupinách výsledků je tedy 10.</span><span class="sxs-lookup"><span data-stu-id="24154-261">Therefore, the maximum point total in each result group is 10.</span></span> 

<span data-ttu-id="24154-262">Následující tabulka uvádí zprávy podle bodů, které definujete pro skupinu výsledků „schopnosti vedení“.</span><span class="sxs-lookup"><span data-stu-id="24154-262">The following table shows the point-based messages that you define for the “leadership abilities” result group.</span></span>

| <span data-ttu-id="24154-263">Bodový interval</span><span class="sxs-lookup"><span data-stu-id="24154-263">Point interval</span></span> | <span data-ttu-id="24154-264">Text</span><span class="sxs-lookup"><span data-stu-id="24154-264">Text</span></span>                                       |
|----------------|--------------------------------------------|
| <span data-ttu-id="24154-265">1 až 3</span><span class="sxs-lookup"><span data-stu-id="24154-265">1 to 3</span></span>         | <span data-ttu-id="24154-266">Máte průměrné vůdcovské schopnosti.</span><span class="sxs-lookup"><span data-stu-id="24154-266">You have average leadership abilities.</span></span>     |
| <span data-ttu-id="24154-267">4 až 7</span><span class="sxs-lookup"><span data-stu-id="24154-267">4 to 7</span></span>         | <span data-ttu-id="24154-268">Máte dobré vůdcovské schopnosti.</span><span class="sxs-lookup"><span data-stu-id="24154-268">You have good leadership abilities.</span></span>        |
| <span data-ttu-id="24154-269">8 až 10</span><span class="sxs-lookup"><span data-stu-id="24154-269">8 to 10</span></span>        | <span data-ttu-id="24154-270">Máte výjimečné vůdcovské schopnosti.</span><span class="sxs-lookup"><span data-stu-id="24154-270">You have outstanding leadership abilities.</span></span> |

<span data-ttu-id="24154-271">Můžete nastavit bodové intervaly a texty pro každou skupinu výsledků v dotazníku.</span><span class="sxs-lookup"><span data-stu-id="24154-271">You can set up point intervals and texts for each result group on a questionnaire.</span></span> <span data-ttu-id="24154-272">Texty, které odpovídají hodnocení každého respondenta, jsou zobrazeny pro každou skupinu výsledků.</span><span class="sxs-lookup"><span data-stu-id="24154-272">Texts that correspond to each respondent’s score are displayed for each result group.</span></span> 

> [!NOTE]
> <span data-ttu-id="24154-273">Intervaly a texty lze měnit.</span><span class="sxs-lookup"><span data-stu-id="24154-273">You can change intervals and texts.</span></span> <span data-ttu-id="24154-274">Pokud však již byl dotazník vyplněn, mohou změny způsobit nesrovnalosti mezi předchozími a novými sestavami výsledků.</span><span class="sxs-lookup"><span data-stu-id="24154-274">However, if a questionnaire has been completed, changes might cause differences between previous and new result reports.</span></span>

### <a name="conditional-question-hierarchies"></a><span data-ttu-id="24154-275">Hierarchie podmíněných otázek</span><span class="sxs-lookup"><span data-stu-id="24154-275">Conditional question hierarchies</span></span>

<span data-ttu-id="24154-276">Hierarchie podmíněných otázek jsou volitelné při nastavování dotazníku.</span><span class="sxs-lookup"><span data-stu-id="24154-276">Conditional question hierarchies are optional when you set up a questionnaire.</span></span> 

> [!NOTE]
> <span data-ttu-id="24154-277">Před nastavením hierarchie podmíněných otázek je třeba připojit otázky, které mají přiřazeny skupiny odpovědí k dotazníku.</span><span class="sxs-lookup"><span data-stu-id="24154-277">Before you can set up a conditional question hierarchy, you must attach questions that have assigned answer groups to the questionnaire.</span></span> 

<span data-ttu-id="24154-278">Chcete-li použít podmíněné otázky a vytvářet hierarchii otázek v dotazníku, můžete vytvořit posloupnost, ve které jsou otázky prezentovány, tak, aby závisela na odpovědi vybrané respondentem pro jednotlivé otázky.</span><span class="sxs-lookup"><span data-stu-id="24154-278">To use conditional questions to create a question hierarchy in a questionnaire, you can make the sequence that questions are presented in depend on the answer that a respondent selects for each question.</span></span> <span data-ttu-id="24154-279">Pomocí úpravy posloupnosti otázek respondenta můžete dotazník upravit, kdy jej respondent vyplní.</span><span class="sxs-lookup"><span data-stu-id="24154-279">By basing the question sequence on a respondent’s answer, you can modify the questionnaire as the respondent completes it.</span></span>

#### <a name="examples"></a><span data-ttu-id="24154-280">Příklad</span><span class="sxs-lookup"><span data-stu-id="24154-280">Examples</span></span>

<span data-ttu-id="24154-281">Právnická osoba nabízí zboží i služby zákazníkům.</span><span class="sxs-lookup"><span data-stu-id="24154-281">A legal entity offers both items and services to its customers.</span></span> <span data-ttu-id="24154-282">V takovém případě obvykle dochází k tomu, že někteří odběratelé kupují pouze zboží, jiní pouze služby a někteří zboží i služby.</span><span class="sxs-lookup"><span data-stu-id="24154-282">As typically occurs in such cases, some customers purchase only items, some purchase only services, and some purchase both items and services.</span></span> <span data-ttu-id="24154-283">Proto pokud právnická osoba distribuuje průzkum spokojenosti zákazníků, použije na dotazník podmíněnou strukturu, aby odběratelé, kteří nakupují pouze služby, nemuseli odpovídat na otázky o zboží.</span><span class="sxs-lookup"><span data-stu-id="24154-283">Therefore, when the legal entity distributes a customer satisfaction survey, it applies a conditional structure to the questionnaire, so that customers who purchase only services don't have to answer questions about items.</span></span> 

<span data-ttu-id="24154-284">Případně můžete nastavit dotazník tak, že pokud respondent vybere odpověď A na otázku 1, další v pořadí bude otázka 2.</span><span class="sxs-lookup"><span data-stu-id="24154-284">Alternatively, you set up a questionnaire so that if a respondent selects answer A for question 1, question 2 is next in the question sequence.</span></span> <span data-ttu-id="24154-285">Pokud však respondent vybere odpověď B na otázku 1, následuje otázka 5.</span><span class="sxs-lookup"><span data-stu-id="24154-285">However, if the respondent selects answer B for question 1, question 5 is next.</span></span>

<a name="additional-resources"></a><span data-ttu-id="24154-286">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="24154-286">Additional resources</span></span>
--------

[<span data-ttu-id="24154-287">Dotazníky</span><span class="sxs-lookup"><span data-stu-id="24154-287">Questionnaires</span></span>](questionnaires.md)

[<span data-ttu-id="24154-288">Distribuce a plánování dotazníků</span><span class="sxs-lookup"><span data-stu-id="24154-288">Distribute and schedule questionnaires</span></span>](distribute-questionnaires.md)

[<span data-ttu-id="24154-289">Zobrazení a vyhodnocení výsledků dotazníků</span><span class="sxs-lookup"><span data-stu-id="24154-289">View and evaluate the results of questionnaires</span></span>](evaluate-questionnaire-results.md)

