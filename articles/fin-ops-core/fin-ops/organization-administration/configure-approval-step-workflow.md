---
title: Konfigurace schvalovacích kroků ve workflowu
description: Toto téma vysvětluje, jak nakonfigurovat vlastnosti schvalovacího kroku.
author: ChrisGarty
manager: AnnBe
ms.date: 08/23/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 192161
ms.assetid: 8b478e3d-d6b4-403b-aae0-f639a71ca36c
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 69035be84d489d6ea2342c6974cfa9a31531f1c7
ms.sourcegitcommit: e55efd2f62bf60f678108c09ad4701a76b20cc68
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/17/2020
ms.locfileid: "3698064"
---
# <a name="configure-approval-steps-in-a-workflow"></a><span data-ttu-id="8c08e-103">Konfigurace schvalovacích kroků ve workflowu</span><span class="sxs-lookup"><span data-stu-id="8c08e-103">Configure approval steps in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8c08e-104">Toto téma vysvětluje, jak nakonfigurovat vlastnosti schvalovacího kroku.</span><span class="sxs-lookup"><span data-stu-id="8c08e-104">This topic explains how to configure the properties of an approval step.</span></span>

<span data-ttu-id="8c08e-105">Pokud budete chtít nakonfigurovat schvalovací krok v editoru workflowu, klikněte pravým tlačítkem myši na krok schválení a kliknutím na tlačítko **Vlastnosti** otevřete stránku **Vlastnosti**.</span><span class="sxs-lookup"><span data-stu-id="8c08e-105">To configure an approval step in the workflow editor, right-click the approval step, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="8c08e-106">Následně nakonfigurujte vlastnosti dílčího workflowu pomocí schvalovacího kroku.</span><span class="sxs-lookup"><span data-stu-id="8c08e-106">Then use the following procedures to configure the properties of the approval step.</span></span>

## <a name="name-the-step"></a><span data-ttu-id="8c08e-107">Pojmenování kroku</span><span class="sxs-lookup"><span data-stu-id="8c08e-107">Name the step</span></span>
<span data-ttu-id="8c08e-108">Pomocí následujících kroků zadejte název schvalovacího kroku.</span><span class="sxs-lookup"><span data-stu-id="8c08e-108">Follow these steps to enter a name for the approval step.</span></span>

1. <span data-ttu-id="8c08e-109">V levém podokně klepněte na tlačítko **Základní nastavení**.</span><span class="sxs-lookup"><span data-stu-id="8c08e-109">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="8c08e-110">Do pole **Název** zadejte jedinečný název schvalovacího kroku.</span><span class="sxs-lookup"><span data-stu-id="8c08e-110">In the **Name** field, enter a unique name for the approval step.</span></span>

## <a name="enter-a-subject-line-and-instructions"></a><span data-ttu-id="8c08e-111">Zadání řádku předmětu a pokynů</span><span class="sxs-lookup"><span data-stu-id="8c08e-111">Enter a subject line and instructions</span></span>

<span data-ttu-id="8c08e-112">Musíte zadat řádek předmětu a pokyny pro uživatele přiřazené k tomuto schvalovacímu kroku.</span><span class="sxs-lookup"><span data-stu-id="8c08e-112">You must provide a subject line and instructions to users who are assigned to the approval step.</span></span> <span data-ttu-id="8c08e-113">Například pokud konfigurujete schvalovací krok pro nákupní požadavky, uživatel, který je ke kroku přiřazen, uvidí řádek s předmětem a pokyny na stránce **Nákupní žádanky**.</span><span class="sxs-lookup"><span data-stu-id="8c08e-113">For example, if you're configuring an approval step for purchase requisitions, the user who is assigned to the step sees the subject line and instructions on the **Purchase requisitions** page.</span></span> <span data-ttu-id="8c08e-114">Řádek předmětu se zobrazí na panelu zpráv na stránce.</span><span class="sxs-lookup"><span data-stu-id="8c08e-114">The subject line appears in a message bar on the page.</span></span> <span data-ttu-id="8c08e-115">Uživatel poté může kliknutím na ikonu na panelu zpráv zobrazit pokyny.</span><span class="sxs-lookup"><span data-stu-id="8c08e-115">The user can then click the icon in the message bar to see the instructions.</span></span> <span data-ttu-id="8c08e-116">K zadání řádku předmětu a pokynů použijte následující postup.</span><span class="sxs-lookup"><span data-stu-id="8c08e-116">Follow these steps to enter a subject line and instructions.</span></span>

1. <span data-ttu-id="8c08e-117">V levém podokně klepněte na tlačítko **Základní nastavení**.</span><span class="sxs-lookup"><span data-stu-id="8c08e-117">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="8c08e-118">V poli **Předmět pracovní položky** zadejte řádek předmětu.</span><span class="sxs-lookup"><span data-stu-id="8c08e-118">In the **Work item subject** field, enter the subject line.</span></span>
3. <span data-ttu-id="8c08e-119">Řádek předmětu můžete přizpůsobit vložením zástupného textu.</span><span class="sxs-lookup"><span data-stu-id="8c08e-119">To personalize the subject line, you can insert placeholders.</span></span> <span data-ttu-id="8c08e-120">Zástupný text bude při zobrazení řádku předmětu uživatelům nahrazen odpovídacími daty.</span><span class="sxs-lookup"><span data-stu-id="8c08e-120">Placeholders are replaced with appropriate data when the subject line is shown to users.</span></span> <span data-ttu-id="8c08e-121">Při vkládání zástupného textu postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="8c08e-121">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="8c08e-122">V textovém poli klepnutím zadejte, kde se má zástupný text zobrazit.</span><span class="sxs-lookup"><span data-stu-id="8c08e-122">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="8c08e-123">Klikněte na **Vložit zástupný text**.</span><span class="sxs-lookup"><span data-stu-id="8c08e-123">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="8c08e-124">V nově otevřeném seznamu vyberte vkládaný zástupný text.</span><span class="sxs-lookup"><span data-stu-id="8c08e-124">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="8c08e-125">Klepněte na tlačítko **Vložit**.</span><span class="sxs-lookup"><span data-stu-id="8c08e-125">Click **Insert**.</span></span>

4. <span data-ttu-id="8c08e-126">Chcete-li přidat překlady řádku předmětu, postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="8c08e-126">To add translations of the subject line, follow these steps:</span></span>

    1. <span data-ttu-id="8c08e-127">Klikněte na **Překlady**.</span><span class="sxs-lookup"><span data-stu-id="8c08e-127">Click **Translations**.</span></span>
    2. <span data-ttu-id="8c08e-128">Na nově otevřené stránce klikněte na **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="8c08e-128">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="8c08e-129">V nově otevřeném seznamu vyberte jazyk, který chcete použít pro zadání textu.</span><span class="sxs-lookup"><span data-stu-id="8c08e-129">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="8c08e-130">V poli **Přeložený text** zadejte text.</span><span class="sxs-lookup"><span data-stu-id="8c08e-130">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="8c08e-131">Text můžete přizpůsobit vložením zástupného textu podle pokynů v kroku 3.</span><span class="sxs-lookup"><span data-stu-id="8c08e-131">To personalize the text, you can insert placeholders as described in step 3.</span></span>
    6. <span data-ttu-id="8c08e-132">Klepněte na tlačítko **Zavřít**.</span><span class="sxs-lookup"><span data-stu-id="8c08e-132">Click **Close**.</span></span>

5. <span data-ttu-id="8c08e-133">V poli **Pokyny pracovní položky** zadejte pokyny.</span><span class="sxs-lookup"><span data-stu-id="8c08e-133">In the **Work item instructions** field, enter the instructions.</span></span>
6. <span data-ttu-id="8c08e-134">Pokyny můžete přizpůsobit vložením zástupného textu.</span><span class="sxs-lookup"><span data-stu-id="8c08e-134">To personalize the instructions, you can insert placeholders.</span></span> <span data-ttu-id="8c08e-135">Zástupný text bude při zobrazení pokynů uživatelům nahrazen odpovídacími daty.</span><span class="sxs-lookup"><span data-stu-id="8c08e-135">Placeholders are replaced with appropriate data when the instructions are shown to users.</span></span> <span data-ttu-id="8c08e-136">Při vkládání zástupného textu postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="8c08e-136">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="8c08e-137">V textovém poli klepnutím zadejte, kde se má zástupný text zobrazit.</span><span class="sxs-lookup"><span data-stu-id="8c08e-137">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="8c08e-138">Klikněte na **Vložit zástupný text**.</span><span class="sxs-lookup"><span data-stu-id="8c08e-138">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="8c08e-139">V nově otevřeném seznamu vyberte vkládaný zástupný text.</span><span class="sxs-lookup"><span data-stu-id="8c08e-139">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="8c08e-140">Klepněte na tlačítko **Vložit**.</span><span class="sxs-lookup"><span data-stu-id="8c08e-140">Click **Insert**.</span></span>

7. <span data-ttu-id="8c08e-141">Chcete-li přidat překlady pokynů, postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="8c08e-141">To add translations of the instructions, follow these steps:</span></span>

    1. <span data-ttu-id="8c08e-142">Klikněte na **Překlady**.</span><span class="sxs-lookup"><span data-stu-id="8c08e-142">Click **Translations**.</span></span>
    2. <span data-ttu-id="8c08e-143">Na nově otevřené stránce klikněte na **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="8c08e-143">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="8c08e-144">V nově otevřeném seznamu vyberte jazyk, který chcete použít pro zadání textu.</span><span class="sxs-lookup"><span data-stu-id="8c08e-144">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="8c08e-145">V poli **Přeložený text** zadejte text.</span><span class="sxs-lookup"><span data-stu-id="8c08e-145">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="8c08e-146">Text můžete přizpůsobit vložením zástupného textu podle pokynů v kroku 6.</span><span class="sxs-lookup"><span data-stu-id="8c08e-146">To personalize the text, you can insert placeholders as described in step 6.</span></span>
    6. <span data-ttu-id="8c08e-147">Klepněte na tlačítko **Zavřít**.</span><span class="sxs-lookup"><span data-stu-id="8c08e-147">Click **Close**.</span></span>

## <a name="assign-the-approval-step"></a><span data-ttu-id="8c08e-148">Přiřazení schvalovacího kroku</span><span class="sxs-lookup"><span data-stu-id="8c08e-148">Assign the approval step</span></span>

<span data-ttu-id="8c08e-149">Pomocí následujícího postupu určíte, komu má být schvalovací krok přiřazen.</span><span class="sxs-lookup"><span data-stu-id="8c08e-149">Follow these steps to specify who the approval step should be assigned to.</span></span>

1. <span data-ttu-id="8c08e-150">V levém podokně klikněte na **Přiřazení**.</span><span class="sxs-lookup"><span data-stu-id="8c08e-150">In the left pane, click **Assignment**.</span></span>
2. <span data-ttu-id="8c08e-151">Na kartě **Typ přiřazení** vyberte jednu z možností v následující tabulce a před přechodem na krok 3 postupujte podle dalších kroků pro tuto možnost.</span><span class="sxs-lookup"><span data-stu-id="8c08e-151">On the **Assignment type** tab, select one of the options in the following table, and then follow the additional steps for that option before you go to step 3.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="8c08e-152">Možnost</span><span class="sxs-lookup"><span data-stu-id="8c08e-152">Option</span></span></th>
    <th><span data-ttu-id="8c08e-153">Uživatelé, kterým je schvalovací krok přiřazen</span><span class="sxs-lookup"><span data-stu-id="8c08e-153">Users that the approval step is assigned to</span></span></th>
    <th><span data-ttu-id="8c08e-154">Další kroky</span><span class="sxs-lookup"><span data-stu-id="8c08e-154">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="8c08e-155">Účastník</span><span class="sxs-lookup"><span data-stu-id="8c08e-155">Participant</span></span></td>
    <td><span data-ttu-id="8c08e-156">Uživatelé, kteří jsou přiřazeni k určité skupině nebo roli</span><span class="sxs-lookup"><span data-stu-id="8c08e-156">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="8c08e-157">Po výběru možnosti <strong>Účastník</strong> na kartě <strong>Založeno na roli</strong> v seznamu <strong>Typ účastníka</strong> vyberte typ skupiny nebo role, ke které chcete krok přiřadit.</span><span class="sxs-lookup"><span data-stu-id="8c08e-157">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to assign the step to.</span></span></li>
    <li><span data-ttu-id="8c08e-158">V seznamu <strong>Účastník</strong> vyberte skupinu nebo roli, ke které chcete krok přiřadit.</span><span class="sxs-lookup"><span data-stu-id="8c08e-158">In the <strong>Participant</strong> list, select the group or role to assign the step to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="8c08e-159">Hierarchie</span><span class="sxs-lookup"><span data-stu-id="8c08e-159">Hierarchy</span></span></td>
    <td><span data-ttu-id="8c08e-160">Uživatelé v určité organizační hierarchii</span><span class="sxs-lookup"><span data-stu-id="8c08e-160">Users in a specific organizational hierarchy</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="8c08e-161">Po výběru možnosti <strong>Hierarchie</strong> na kartě <strong>Výběr hierarchie</strong> v seznamu <strong>Typ hierarchie</strong> vyberte typ hierarchie, ke které chcete krok přiřadit.</span><span class="sxs-lookup"><span data-stu-id="8c08e-161">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to assign the step to.</span></span></li>
    <li><span data-ttu-id="8c08e-162">Systém musí z hierarchie načíst rozsah jmen uživatelů.</span><span class="sxs-lookup"><span data-stu-id="8c08e-162">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="8c08e-163">Tato jména představují uživatele, ke kterým může být krok přiřazen.</span><span class="sxs-lookup"><span data-stu-id="8c08e-163">These names represent users that the step can be assigned to.</span></span> <span data-ttu-id="8c08e-164">Podle těchto kroků určete počáteční a koncový bod rozsahu uživatelských jmen, které systém obdrží:</span><span class="sxs-lookup"><span data-stu-id="8c08e-164">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="8c08e-165">Chcete-li zadat počáteční bod, vyberte osobu v seznamu <strong>Začátek od</strong>.</span><span class="sxs-lookup"><span data-stu-id="8c08e-165">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="8c08e-166">Chcete-li zadat koncový bod, klepněte na možnost <strong>Přidat podmínku</strong>.</span><span class="sxs-lookup"><span data-stu-id="8c08e-166">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="8c08e-167">Poté zadáním podmínky označte, kde v hierarchii má systém přestat načítat jména.</span><span class="sxs-lookup"><span data-stu-id="8c08e-167">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="8c08e-168">Na kartě <strong>Možnosti hierarchie</strong> zadejte uživatele v rozsahu, ke kterým by měl být krok přiřazen:</span><span class="sxs-lookup"><span data-stu-id="8c08e-168">On the <strong>Hierarchy options</strong> tab, specify which users in the range the step should be assigned to:</span></span> <ul>
    <li><span data-ttu-id="8c08e-169"><strong>Přiřadit všechny načtené uživatele</strong> – krok bude přiřazen všem uživatelům v rozsahu.</span><span class="sxs-lookup"><span data-stu-id="8c08e-169"><strong>Assign to all users retrieved</strong> – The step is assigned to all users in the range.</span></span></li>
    <li><span data-ttu-id="8c08e-170"><strong>Přiřadit pouze poslednímu načtenému uživateli</strong> – krok bude přiřazen pouze poslednímu uživateli v rozsahu.</span><span class="sxs-lookup"><span data-stu-id="8c08e-170"><strong>Assign only to last user retrieved</strong> – The step is assigned to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="8c08e-171"><strong>Vyloučit uživatele splňující následující podmínku</strong> – krok není přiřazen žádnému uživateli v rozsahu, který odpovídá konkrétní podmínce.</span><span class="sxs-lookup"><span data-stu-id="8c08e-171"><strong>Exclude users with the following condition</strong> – The step isn't assigned to any users in the range who meet a specific condition.</span></span> <span data-ttu-id="8c08e-172">Po klepnutí na volbu <strong>Přidat podmínku</strong> určete požadovanou podmínku.</span><span class="sxs-lookup"><span data-stu-id="8c08e-172">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="8c08e-173">Uživatel workflowu</span><span class="sxs-lookup"><span data-stu-id="8c08e-173">Workflow user</span></span></td>
    <td><span data-ttu-id="8c08e-174">Uživatelé v aktuálním workflowu</span><span class="sxs-lookup"><span data-stu-id="8c08e-174">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="8c08e-175">Po výběru možnosti <strong>Uživatel workflowu</strong> na kartě <strong>Uživatel workflowu</strong> v seznamu <strong>Uživatel workflowu</strong> vyberte uživatele, který se podílí na workflowu.</span><span class="sxs-lookup"><span data-stu-id="8c08e-175">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="8c08e-176">Uživatel</span><span class="sxs-lookup"><span data-stu-id="8c08e-176">User</span></span></td>
    <td><span data-ttu-id="8c08e-177">Konkrétní uživatelé</span><span class="sxs-lookup"><span data-stu-id="8c08e-177">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="8c08e-178">Po výběru možnosti <strong>Uživatel</strong> klepněte na kartu <strong>Uživatel</strong>.</span><span class="sxs-lookup"><span data-stu-id="8c08e-178">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="8c08e-179">Seznam <strong>Dostupní uživatelé</strong> obsahuje všechny uživatele systému.</span><span class="sxs-lookup"><span data-stu-id="8c08e-179">The <strong>Available users</strong> list includes all system users.</span></span> <span data-ttu-id="8c08e-180">Vyberte uživatele, ke kterým chcete krok přiřadit, a pak přesuňte tyto uživatele do seznamu <strong>Vybraní uživatelé</strong>.</span><span class="sxs-lookup"><span data-stu-id="8c08e-180">Select the users to assign the step to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

3. <span data-ttu-id="8c08e-181">Na kartě **Časový limit** v poli **Trvání** určete, kolik času má uživatel pro provedení akce nebo reakce na dokumenty, které dosáhly schvalovacího kroku.</span><span class="sxs-lookup"><span data-stu-id="8c08e-181">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to take action on, or respond to, documents that reach the approval step.</span></span> <span data-ttu-id="8c08e-182">Vyberte některou z následujících možností:</span><span class="sxs-lookup"><span data-stu-id="8c08e-182">Select one of the following options:</span></span>

    - <span data-ttu-id="8c08e-183">**Hodiny** – zadejte počet hodin, které má uživatel reagovat.</span><span class="sxs-lookup"><span data-stu-id="8c08e-183">**Hours** – Enter the number of hours that the user has to respond.</span></span> <span data-ttu-id="8c08e-184">Pak vyberte kalendář, který vaše organizace používá, a zadejte informace o pracovním týdnu vaší organizace.</span><span class="sxs-lookup"><span data-stu-id="8c08e-184">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="8c08e-185">**Dny** – zadejte počet dnů, které má uživatel reagovat.</span><span class="sxs-lookup"><span data-stu-id="8c08e-185">**Days** – Enter the number of days that the user has to respond.</span></span> <span data-ttu-id="8c08e-186">Pak vyberte kalendář, který vaše organizace používá, a zadejte informace o pracovním týdnu vaší organizace.</span><span class="sxs-lookup"><span data-stu-id="8c08e-186">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="8c08e-187">**Týdny** – zadejte počet týdnů, které má uživatel reagovat.</span><span class="sxs-lookup"><span data-stu-id="8c08e-187">**Weeks** – Enter the number of weeks that the user has to respond.</span></span>
    - <span data-ttu-id="8c08e-188">**Měsíce** – vyberte den a týden, do kdy musí uživatel reagovat.</span><span class="sxs-lookup"><span data-stu-id="8c08e-188">**Months** – Select the day and week that the user must respond by.</span></span> <span data-ttu-id="8c08e-189">Můžete například požadovat, aby uživatel odpověděl do pátku třetího týdne v měsíci.</span><span class="sxs-lookup"><span data-stu-id="8c08e-189">For example, you might want the user to respond by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="8c08e-190">**Roky** – vyberte den, týden a měsíc, do kdy musí uživatel reagovat.</span><span class="sxs-lookup"><span data-stu-id="8c08e-190">**Years** – Select the day, week, and month that the user must respond by.</span></span> <span data-ttu-id="8c08e-191">Můžete například požadovat, aby uživatel odpověděl do pátku třetího týdne v prosinci.</span><span class="sxs-lookup"><span data-stu-id="8c08e-191">For example, you might want the user to respond by Friday of the third week of December.</span></span>

    <span data-ttu-id="8c08e-192">Pokud uživatel u dokumentu neprovede akci v přiděleném čase, dokument bude v prodlení.</span><span class="sxs-lookup"><span data-stu-id="8c08e-192">If the user doesn't take action on the document in the allotted time, the document is overdue.</span></span> <span data-ttu-id="8c08e-193">Dokument v prodlení je eskalován na základě možností vybraných v oblasti stránky **Eskalace**.</span><span class="sxs-lookup"><span data-stu-id="8c08e-193">A document that is overdue is escalated, based on the options that you select in the **Escalation** area of the page.</span></span>

4. <span data-ttu-id="8c08e-194">Jestliže přiřadíte schvalovací krok více uživatelům nebo skupině uživatelů na kartě **Zásada dokončení**, vyberte jednu z následujících možností:</span><span class="sxs-lookup"><span data-stu-id="8c08e-194">If you assigned the approval step to multiple users or a group of users, on the **Completion policy** tab, select one of the following options:</span></span>

    - <span data-ttu-id="8c08e-195">**Jednotlivý schvalovatel** – akce použitá pro dokument je určena první reagující osobou.</span><span class="sxs-lookup"><span data-stu-id="8c08e-195">**Single approver** – The action that is applied to the document is determined by the first person who responds.</span></span> <span data-ttu-id="8c08e-196">Například Sam odeslal vyúčtování výdajů ve výši 15 000 USD.</span><span class="sxs-lookup"><span data-stu-id="8c08e-196">For example, Sam has submitted an expense report for USD 15,000.</span></span> <span data-ttu-id="8c08e-197">Vyúčtování výdajů je aktuálně přiřazeno uživatelům Sue, Jo a Bill.</span><span class="sxs-lookup"><span data-stu-id="8c08e-197">The expense report is currently assigned to Sue, Jo, and Bill.</span></span> <span data-ttu-id="8c08e-198">Pokud je Sue první osobou reagující na dokument, je akce, kterou provede, použita pro dokument.</span><span class="sxs-lookup"><span data-stu-id="8c08e-198">If Sue is the first person who responds to the document, the action that she takes is applied to the document.</span></span> <span data-ttu-id="8c08e-199">Jestliže ho Sue odmítne, je dokument zamítnut a odeslán zpět Samovi.</span><span class="sxs-lookup"><span data-stu-id="8c08e-199">If Sue rejects the document, it's rejected and sent back to Sam.</span></span> <span data-ttu-id="8c08e-200">Jakmile Sue dokument schválí, je odeslán Anně ke schválení.</span><span class="sxs-lookup"><span data-stu-id="8c08e-200">If Sue approves the document, it's sent to Ann for approval.</span></span>

        ![Workflow se schvalovacím procesem](./media/workflow_multipleusersinstep.gif)

    - <span data-ttu-id="8c08e-202">**Většina schvalovatelů** – akce použitá pro dokument je určena, když reaguje většina schvalujících.</span><span class="sxs-lookup"><span data-stu-id="8c08e-202">**Majority of approvers** – The action that is applied to the document is determined when most of the approvers respond.</span></span> <span data-ttu-id="8c08e-203">Například Sam odeslal vyúčtování výdajů ve výši 15 000 USD.</span><span class="sxs-lookup"><span data-stu-id="8c08e-203">For example, Sam has submitted an expense report for USD 15,000.</span></span> <span data-ttu-id="8c08e-204">Vyúčtování výdajů je aktuálně přiřazeno uživatelům Sue, Jo a Bill.</span><span class="sxs-lookup"><span data-stu-id="8c08e-204">The expense report is currently assigned to Sue, Jo, and Bill.</span></span> <span data-ttu-id="8c08e-205">Akci použitou pro dokument určují první dva schvalující, kteří reagují, tedy Sue a Jo.</span><span class="sxs-lookup"><span data-stu-id="8c08e-205">If Sue and Jo are the first two approvers who respond, the action that they take is applied to the document.</span></span>

        - <span data-ttu-id="8c08e-206">Jestliže Sue dokument schválí a Jo ho zamítne, je dokument zamítnut a odeslán zpět Samovi.</span><span class="sxs-lookup"><span data-stu-id="8c08e-206">If Sue approves the document, but Jo rejects it, the document is rejected and sent back to Sam.</span></span>
        - <span data-ttu-id="8c08e-207">Jestliže Sue i Jo dokument schválí, je dokument odeslán Anně ke schválení.</span><span class="sxs-lookup"><span data-stu-id="8c08e-207">If both Sue and Jo approve the document, it's sent to Ann for approval.</span></span>

    - <span data-ttu-id="8c08e-208">**Procentuální počet schvalovatelů** – akce použitá pro dokument je určena, když reaguje konkrétní procento schvalujících.</span><span class="sxs-lookup"><span data-stu-id="8c08e-208">**Percentage of approvers** – The action that is applied to the document is determined when a specific percentage of the approvers respond.</span></span> <span data-ttu-id="8c08e-209">Například Sam odeslal vyúčtování výdajů ve výši 15 000 USD.</span><span class="sxs-lookup"><span data-stu-id="8c08e-209">For example, Sam has submitted an expense report for USD 15,000.</span></span> <span data-ttu-id="8c08e-210">Vyúčtování výdajů je momentálně přiřazeno Sue, Jo a Billovi a vy zadáte pro procento hodnotu **50**.</span><span class="sxs-lookup"><span data-stu-id="8c08e-210">The expense report is currently assigned to Sue, Jo, and Bill, and you entered **50** as the percentage.</span></span> <span data-ttu-id="8c08e-211">Jestliže Sue a Jo jsou prvními dvěma schvalující, kteří reagují, akce, kterou provedou, je použitá v dokumentu vzhledem k tomu, že splňují požadavky 50 procent schvalovatelů.</span><span class="sxs-lookup"><span data-stu-id="8c08e-211">If Sue and Jo are the first two approvers who respond, the action that they take is applied to the document, because they meet the requirement for 50 percent of approvers.</span></span>

        - <span data-ttu-id="8c08e-212">Jestliže Sue dokument schválí a Jo ho zamítne, je dokument zamítnut a odeslán zpět Samovi.</span><span class="sxs-lookup"><span data-stu-id="8c08e-212">If Sue approves the document, but Jo rejects it, the document is rejected and sent back to Sam.</span></span>
        - <span data-ttu-id="8c08e-213">Jestliže Sue i Jo dokument schválí, je dokument odeslán Anně ke schválení.</span><span class="sxs-lookup"><span data-stu-id="8c08e-213">If both Sue and Jo approve the document, it's sent to Ann for approval.</span></span>

    - <span data-ttu-id="8c08e-214">**Všichni schvalovatelé** – dokument musí schválit všichni schvalovatelé.</span><span class="sxs-lookup"><span data-stu-id="8c08e-214">**All approvers** – All the approvers must approve the document.</span></span> <span data-ttu-id="8c08e-215">V opačném případě se ve workflowu nedá pokračovat.</span><span class="sxs-lookup"><span data-stu-id="8c08e-215">Otherwise, the workflow can't continue.</span></span> <span data-ttu-id="8c08e-216">Například Sam odeslal vyúčtování výdajů ve výši 15 000 USD.</span><span class="sxs-lookup"><span data-stu-id="8c08e-216">For example, Sam has submitted an expense report for USD 15,000.</span></span> <span data-ttu-id="8c08e-217">Vyúčtování výdajů je aktuálně přiřazeno uživatelům Sue, Jo a Bill.</span><span class="sxs-lookup"><span data-stu-id="8c08e-217">The expense report is currently assigned to Sue, Jo, and Bill.</span></span> <span data-ttu-id="8c08e-218">Jestliže Sue a Jo dokument schválí a Bill ho zamítne, je dokument zamítnut a odeslán zpět Stanislavovi.</span><span class="sxs-lookup"><span data-stu-id="8c08e-218">If Sue and Joe approve the document, but Bill rejects it, the document is rejected and sent back to Sam.</span></span> <span data-ttu-id="8c08e-219">Jestliže Sue, Jo a Bill dokument schválí, je dokument odeslán Anně ke schválení.</span><span class="sxs-lookup"><span data-stu-id="8c08e-219">If Sue, Jo, and Bill all approve the document, it's sent to Ann for approval.</span></span>

## <a name="specify-when-the-approval-step-is-required"></a><span data-ttu-id="8c08e-220">Určete, kdy je schvalovací krok vyžadován.</span><span class="sxs-lookup"><span data-stu-id="8c08e-220">Specify when the approval step is required</span></span>

<span data-ttu-id="8c08e-221">Můžete určit, kdy je schvalovací krok vyžadován.</span><span class="sxs-lookup"><span data-stu-id="8c08e-221">You can specify when the approval step is required.</span></span> <span data-ttu-id="8c08e-222">Schvalovací krok může být vždy vyžadován, nebo může být vyžadován pouze v případě splnění určitých podmínek.</span><span class="sxs-lookup"><span data-stu-id="8c08e-222">The approval step can always be required, or it can be required only if specific conditions are met.</span></span>

### <a name="the-approval-step-is-always-required"></a><span data-ttu-id="8c08e-223">Schvalovací krok je vyžadován vždy</span><span class="sxs-lookup"><span data-stu-id="8c08e-223">The approval step is always required</span></span>

<span data-ttu-id="8c08e-224">Pokud je schvalovací krok vyžadován vždy, postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="8c08e-224">Follow these steps if the approval step is always required.</span></span>

1. <span data-ttu-id="8c08e-225">V levém podokně klikněte na **Podmínka**.</span><span class="sxs-lookup"><span data-stu-id="8c08e-225">In the left pane, click **Condition**.</span></span>
2. <span data-ttu-id="8c08e-226">Vyberte možnost **Vždy spustit tento krok**.</span><span class="sxs-lookup"><span data-stu-id="8c08e-226">Select the **Always run this step** option.</span></span>

### <a name="the-approval-step-is-required-in-specific-conditions"></a><span data-ttu-id="8c08e-227">Schvalovací krok je vyžadován za určitých podmínek</span><span class="sxs-lookup"><span data-stu-id="8c08e-227">The approval step is required in specific conditions</span></span>

<span data-ttu-id="8c08e-228">Schvalovací krok, který konfigurujete, může být vyžadován pouze po splnění určitých podmínek.</span><span class="sxs-lookup"><span data-stu-id="8c08e-228">The approval step that you're configuring might be required only if specific conditions are met.</span></span> <span data-ttu-id="8c08e-229">Například pokud konfigurujete schvalovací krok pro workflow nákupního požadavku můžete chtít, aby ke schvalovacímu kroku docházelo pouze v případě, že je nákupní požadavek je vyšší než 10 000 USD.</span><span class="sxs-lookup"><span data-stu-id="8c08e-229">For example, if you're configuring an approval step for a purchase requisition workflow, you might want the approval step to occur only if the amount of the purchase requisition is more than USD 10,000.</span></span> <span data-ttu-id="8c08e-230">Pomocí následujícího postupu určete, kdy je schvalovací krok vyžadován.</span><span class="sxs-lookup"><span data-stu-id="8c08e-230">Follow these steps to specify when the approval step is required.</span></span>

1. <span data-ttu-id="8c08e-231">V levém podokně klikněte na **Podmínka**.</span><span class="sxs-lookup"><span data-stu-id="8c08e-231">In the left pane, click **Condition**.</span></span>
2. <span data-ttu-id="8c08e-232">Vyberte možnost **Provést tento krok pouze v případě, že je splněna následující podmínka**.</span><span class="sxs-lookup"><span data-stu-id="8c08e-232">Select the **Run this step only when the following condition is met** option.</span></span>
3. <span data-ttu-id="8c08e-233">Zadání podmínky</span><span class="sxs-lookup"><span data-stu-id="8c08e-233">Enter a condition.</span></span>
4. <span data-ttu-id="8c08e-234">Zadejte všechny další podmínky, které jsou požadovány.</span><span class="sxs-lookup"><span data-stu-id="8c08e-234">Enter any additional conditions that are required.</span></span>
5. <span data-ttu-id="8c08e-235">Chcete-li ověřit, zda jsou zadané podmínky nastaveny správně, postupujte následovně:</span><span class="sxs-lookup"><span data-stu-id="8c08e-235">To verify that the conditions that you entered are configured correctly, follow these steps:</span></span>

    1. <span data-ttu-id="8c08e-236">Klepněte na možnost **Test**.</span><span class="sxs-lookup"><span data-stu-id="8c08e-236">Click **Test**.</span></span>
    2. <span data-ttu-id="8c08e-237">Na stránce **Podmínka testovacího workflowu** v oblasti **Ověřit podmínku** vyberte záznam.</span><span class="sxs-lookup"><span data-stu-id="8c08e-237">On the **Test workflow condition** page, in the **Validate condition** area, select a record.</span></span>
    3. <span data-ttu-id="8c08e-238">Klepněte na možnost **Test**.</span><span class="sxs-lookup"><span data-stu-id="8c08e-238">Click **Test**.</span></span> <span data-ttu-id="8c08e-239">Systém záznam vyhodnotí a určí, zda odpovídá zadaným podmínkám.</span><span class="sxs-lookup"><span data-stu-id="8c08e-239">The system evaluates the record to determine whether it meets the conditions that you defined.</span></span>
    4. <span data-ttu-id="8c08e-240">Klikněte na tlačítko **OK** nebo klepnutím na tlačítko **Storno** se vraťte na stránku **Vlastnosti**.</span><span class="sxs-lookup"><span data-stu-id="8c08e-240">Click **OK** or **Cancel** to return to the **Properties** page.</span></span>

## <a name="specify-what-happens-when-the-document-is-overdue"></a><span data-ttu-id="8c08e-241">Co by se mělo stát, je-li dokument zpožděný</span><span class="sxs-lookup"><span data-stu-id="8c08e-241">Specify what happens when the document is overdue</span></span>

<span data-ttu-id="8c08e-242">Pokud uživatel u dokumentu neprovede akci v přiděleném čase, dokument bude v prodlení.</span><span class="sxs-lookup"><span data-stu-id="8c08e-242">If a user doesn't take action on a document in the allotted time, the document is overdue.</span></span> <span data-ttu-id="8c08e-243">Dokument, který je v prodlení, může být eskalován nebo automaticky přiřazen ke schválení jinému uživateli.</span><span class="sxs-lookup"><span data-stu-id="8c08e-243">A document that is overdue can be escalated, or automatically assigned to another user for approval.</span></span> <span data-ttu-id="8c08e-244">Pro eskalování dokumentu v prodlení postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="8c08e-244">Follow these steps to escalate the document if it's overdue.</span></span>

1. <span data-ttu-id="8c08e-245">V levém podokně klikněte na **Eskalování**.</span><span class="sxs-lookup"><span data-stu-id="8c08e-245">In the left pane, click **Escalation**.</span></span>
2. <span data-ttu-id="8c08e-246">Označte pole **Použít eskalační cestu** a vytvořte tak eskalační cestu.</span><span class="sxs-lookup"><span data-stu-id="8c08e-246">Select the **Use escalation path** check box to create an escalation path.</span></span> <span data-ttu-id="8c08e-247">Systém automaticky přiřadí daný dokument uživatelům uvedeným v cestě eskalace.</span><span class="sxs-lookup"><span data-stu-id="8c08e-247">The system automatically assigns the document to the users who are listed in the escalation path.</span></span> <span data-ttu-id="8c08e-248">Například v následující tabulce naleznete příklad eskalační cesty.</span><span class="sxs-lookup"><span data-stu-id="8c08e-248">For example, the following table represents an escalation path.</span></span>

    | <span data-ttu-id="8c08e-249">Pořadí</span><span class="sxs-lookup"><span data-stu-id="8c08e-249">Sequence</span></span> | <span data-ttu-id="8c08e-250">Eskalační cesta</span><span class="sxs-lookup"><span data-stu-id="8c08e-250">Escalation path</span></span>      |
    |----------|----------------------|
    | <span data-ttu-id="8c08e-251">1</span><span class="sxs-lookup"><span data-stu-id="8c08e-251">1</span></span>        | <span data-ttu-id="8c08e-252">Přiřadit k: Donna</span><span class="sxs-lookup"><span data-stu-id="8c08e-252">Assign to: Donna</span></span>     |
    | <span data-ttu-id="8c08e-253">2</span><span class="sxs-lookup"><span data-stu-id="8c08e-253">2</span></span>        | <span data-ttu-id="8c08e-254">Přiřadit k: Erin</span><span class="sxs-lookup"><span data-stu-id="8c08e-254">Assign to: Erin</span></span>      |
    | <span data-ttu-id="8c08e-255">3</span><span class="sxs-lookup"><span data-stu-id="8c08e-255">3</span></span>        | <span data-ttu-id="8c08e-256">Finální akce: odmítnutí</span><span class="sxs-lookup"><span data-stu-id="8c08e-256">Final action: Reject</span></span> |

    <span data-ttu-id="8c08e-257">V tomto příkladu systém přiřadí zpožděný dokument Donně.</span><span class="sxs-lookup"><span data-stu-id="8c08e-257">In this example, the system assigns the overdue document to Donna.</span></span> <span data-ttu-id="8c08e-258">Pokud Donna v přiděleném čase nereaguje, systém přiřadí dokument Erin.</span><span class="sxs-lookup"><span data-stu-id="8c08e-258">If Donna doesn't respond in the allotted time, the system assigns the document to Erin.</span></span> <span data-ttu-id="8c08e-259">Pokud Erin v přiděleném čase nereaguje, systém dokument zamítne.</span><span class="sxs-lookup"><span data-stu-id="8c08e-259">If Erin doesn't respond in the allotted time, the system rejects the document.</span></span>

3. <span data-ttu-id="8c08e-260">Pokud chcete přidat uživatele do eskalační cesty, klepněte na tlačítko **Přidat eskalaci**.</span><span class="sxs-lookup"><span data-stu-id="8c08e-260">To add a user to the escalation path, click **Add escalation**.</span></span> <span data-ttu-id="8c08e-261">Na kartě **Typ přiřazení** vyberte jednu z možností v následující tabulce a před přechodem na krok 4 postupujte podle dalších kroků pro tuto možnost.</span><span class="sxs-lookup"><span data-stu-id="8c08e-261">On the **Assignment type** tab, select one of the options in the following table, and then follow the additional steps for that option before you go to step 4.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="8c08e-262">Možnost</span><span class="sxs-lookup"><span data-stu-id="8c08e-262">Option</span></span></th>
    <th><span data-ttu-id="8c08e-263">Uživatelé, kterým je dokument eskalován</span><span class="sxs-lookup"><span data-stu-id="8c08e-263">Users that the document is escalated to</span></span></th>
    <th><span data-ttu-id="8c08e-264">Další kroky</span><span class="sxs-lookup"><span data-stu-id="8c08e-264">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="8c08e-265">Hierarchie</span><span class="sxs-lookup"><span data-stu-id="8c08e-265">Hierarchy</span></span></td>
    <td><span data-ttu-id="8c08e-266">Uživatelé v určité organizační hierarchii</span><span class="sxs-lookup"><span data-stu-id="8c08e-266">Users in a specific organizational hierarchy</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="8c08e-267">Po výběru možnosti <strong>Hierarchie</strong> na kartě <strong>Výběr hierarchie</strong> v seznamu <strong>Typ hierarchie</strong> vyberte typ hierarchie, ke které dokument eskalovat.</span><span class="sxs-lookup"><span data-stu-id="8c08e-267">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to escalate the document to.</span></span></li>
    <li><span data-ttu-id="8c08e-268">Systém musí z hierarchie načíst rozsah jmen uživatelů.</span><span class="sxs-lookup"><span data-stu-id="8c08e-268">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="8c08e-269">Tato jména představují uživatele, ke kterým může být dokument eskalován.</span><span class="sxs-lookup"><span data-stu-id="8c08e-269">These names represent users that the document can be escalated to.</span></span> <span data-ttu-id="8c08e-270">Podle těchto kroků určete počáteční a koncový bod rozsahu uživatelských jmen, které systém obdrží:</span><span class="sxs-lookup"><span data-stu-id="8c08e-270">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="8c08e-271">Chcete-li zadat počáteční bod, vyberte osobu v seznamu <strong>Začátek od</strong>.</span><span class="sxs-lookup"><span data-stu-id="8c08e-271">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="8c08e-272">Chcete-li zadat koncový bod, klepněte na možnost <strong>Přidat podmínku</strong>.</span><span class="sxs-lookup"><span data-stu-id="8c08e-272">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="8c08e-273">Poté zadáním podmínky označte, kde v hierarchii má systém přestat načítat jména.</span><span class="sxs-lookup"><span data-stu-id="8c08e-273">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="8c08e-274">Na kartě <strong>Možnosti hierarchie</strong> zadejte uživatele v rozsahu, ke kterým by měl být dokument eskalován:</span><span class="sxs-lookup"><span data-stu-id="8c08e-274">On the <strong>Hierarchy options</strong> tab, specify which users in the range the document should be escalated to:</span></span> <ul>
    <li><span data-ttu-id="8c08e-275"><strong>Přiřadit všechny načtené uživatele</strong> – dokument bude eskalován všem uživatelům v rozsahu.</span><span class="sxs-lookup"><span data-stu-id="8c08e-275"><strong>Assign to all users retrieved</strong> – The document is escalated to all users in the range.</span></span></li>
    <li><span data-ttu-id="8c08e-276"><strong>Přiřadit pouze poslednímu načtenému uživateli</strong> – dokument bude eskalován pouze poslednímu uživateli v rozsahu.</span><span class="sxs-lookup"><span data-stu-id="8c08e-276"><strong>Assign only to last user retrieved</strong> – The document is escalated to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="8c08e-277"><strong>Vyloučit uživatele splňující následující podmínku</strong> – dokument není eskalován žádnému uživateli v rozsahu, který odpovídá konkrétní podmínce.</span><span class="sxs-lookup"><span data-stu-id="8c08e-277"><strong>Exclude users with the following condition</strong> – The document isn't escalated to any users in the range who meet a specific condition.</span></span> <span data-ttu-id="8c08e-278">Po klepnutí na volbu <strong>Přidat podmínku</strong> určete požadovanou podmínku.</span><span class="sxs-lookup"><span data-stu-id="8c08e-278">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="8c08e-279">Uživatel workflowu</span><span class="sxs-lookup"><span data-stu-id="8c08e-279">Workflow user</span></span></td>
    <td><span data-ttu-id="8c08e-280">Uživatelé v aktuálním workflowu</span><span class="sxs-lookup"><span data-stu-id="8c08e-280">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="8c08e-281">Po výběru možnosti <strong>Uživatel workflowu</strong> na kartě <strong>Uživatel workflowu</strong> v seznamu <strong>Uživatel workflowu</strong> vyberte uživatele, který se podílí na workflowu.</span><span class="sxs-lookup"><span data-stu-id="8c08e-281">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="8c08e-282">Uživatel</span><span class="sxs-lookup"><span data-stu-id="8c08e-282">User</span></span></td>
    <td><span data-ttu-id="8c08e-283">Konkrétní uživatelé</span><span class="sxs-lookup"><span data-stu-id="8c08e-283">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="8c08e-284">Po výběru možnosti <strong>Uživatel</strong> klepněte na kartu <strong>Uživatel</strong>.</span><span class="sxs-lookup"><span data-stu-id="8c08e-284">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="8c08e-285">Seznam <strong>Dostupní uživatelé</strong> obsahuje všechny uživatele.</span><span class="sxs-lookup"><span data-stu-id="8c08e-285">The <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="8c08e-286">Vyberte uživatele, ke kterým chcete dokument eskalovat, a pak přesuňte tyto uživatele do seznamu <strong>Vybraní uživatelé</strong>.</span><span class="sxs-lookup"><span data-stu-id="8c08e-286">Select the users to escalate the document to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

4. <span data-ttu-id="8c08e-287">Na kartě **Časový limit** v poli **Trvání** určete, kolik času má uživatel pro provedení akce nebo reakce na dokumenty.</span><span class="sxs-lookup"><span data-stu-id="8c08e-287">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to take action on, or respond to, documents.</span></span> <span data-ttu-id="8c08e-288">Vyberte některou z následujících možností:</span><span class="sxs-lookup"><span data-stu-id="8c08e-288">Select one of the following options:</span></span>

    - <span data-ttu-id="8c08e-289">**Hodiny** – zadejte počet hodin, které má uživatel reagovat.</span><span class="sxs-lookup"><span data-stu-id="8c08e-289">**Hours** – Enter the number of hours that the user has to respond.</span></span> <span data-ttu-id="8c08e-290">Pak vyberte kalendář, který vaše organizace používá, a zadejte informace o pracovním týdnu vaší organizace.</span><span class="sxs-lookup"><span data-stu-id="8c08e-290">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="8c08e-291">**Dny** – zadejte počet dnů, které má uživatel reagovat.</span><span class="sxs-lookup"><span data-stu-id="8c08e-291">**Days** – Enter the number of days that the user has to respond.</span></span> <span data-ttu-id="8c08e-292">Pak vyberte kalendář, který vaše organizace používá, a zadejte informace o pracovním týdnu vaší organizace.</span><span class="sxs-lookup"><span data-stu-id="8c08e-292">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="8c08e-293">**Týdny** – zadejte počet týdnů, které má uživatel reagovat.</span><span class="sxs-lookup"><span data-stu-id="8c08e-293">**Weeks** – Enter the number of weeks that the user has to respond.</span></span>
    - <span data-ttu-id="8c08e-294">**Měsíce** – vyberte den a týden, do kdy musí uživatel reagovat.</span><span class="sxs-lookup"><span data-stu-id="8c08e-294">**Months** – Select the day and week that the user must respond by.</span></span> <span data-ttu-id="8c08e-295">Můžete například požadovat, aby uživatel odpověděl do pátku třetího týdne v měsíci.</span><span class="sxs-lookup"><span data-stu-id="8c08e-295">For example, you might want the user to respond by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="8c08e-296">**Roky** – vyberte den, týden a měsíc, do kdy musí uživatel reagovat.</span><span class="sxs-lookup"><span data-stu-id="8c08e-296">**Years** – Select the day, week, and month that the user must respond by.</span></span> <span data-ttu-id="8c08e-297">Můžete například požadovat, aby uživatel odpověděl do pátku třetího týdne v prosinci.</span><span class="sxs-lookup"><span data-stu-id="8c08e-297">For example, you might want the user to respond by Friday of the third week of December.</span></span>

5. <span data-ttu-id="8c08e-298">Zopakujte kroky 3 a 4 u každého uživatele, který má být přidán do eskalační cesty.</span><span class="sxs-lookup"><span data-stu-id="8c08e-298">Repeat steps 3 through 4 for each user that should be added to the escalation path.</span></span> <span data-ttu-id="8c08e-299">Pořadí uživatelů lze změnit.</span><span class="sxs-lookup"><span data-stu-id="8c08e-299">You can change the order of the users.</span></span>
6. <span data-ttu-id="8c08e-300">Pokud uživatelé v eskalační cestě nereagují v určeném čase, systém automaticky provede akci vhodnou pro daný dokument.</span><span class="sxs-lookup"><span data-stu-id="8c08e-300">If the users in the escalation path don't respond in the allotted time, the system automatically take action on the document.</span></span> <span data-ttu-id="8c08e-301">Akci, kterou systém provede, můžete vybrat výběrem řádku **Akce** a na kartě **Konečná akce** vyberte akci.</span><span class="sxs-lookup"><span data-stu-id="8c08e-301">To specify the action that the system takes, select the **Action** row, and then, on the **End action** tab, select an action.</span></span>
