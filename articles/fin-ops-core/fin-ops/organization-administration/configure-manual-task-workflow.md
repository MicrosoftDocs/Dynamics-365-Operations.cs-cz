---
title: Konfigurace ručních úloh ve workflow
description: Toto téma vysvětluje, jak nakonfigurovat vlastnosti ručního úkolu.
author: sericks007
manager: AnnBe
ms.date: 08/23/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 192191
ms.assetid: 27f1afde-ff26-4b6f-8c11-27ec49130bbb
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 492c49b1a3e8334bca401770c4c2db04e8892691
ms.sourcegitcommit: 1d5a4f70a931e78b06811add97c1962e8d93689b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/13/2020
ms.locfileid: "3124628"
---
# <a name="configure-manual-tasks-in-a-workflow"></a><span data-ttu-id="ffa49-103">Konfigurace ručních úloh ve workflow</span><span class="sxs-lookup"><span data-stu-id="ffa49-103">Configure manual tasks in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ffa49-104">Toto téma vysvětluje, jak nakonfigurovat vlastnosti ručního úkolu.</span><span class="sxs-lookup"><span data-stu-id="ffa49-104">This topic explains how to configure the properties for a manual task.</span></span>

<span data-ttu-id="ffa49-105">Pokud budete chtít nakonfigurovat ruční úkol v editoru workflowu, klikněte pravým tlačítkem myši na úkol a kliknutím na tlačítko **Vlastnosti** otevřete stránku **Vlastnosti**.</span><span class="sxs-lookup"><span data-stu-id="ffa49-105">To configure a manual task in the workflow editor, right-click the task, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="ffa49-106">Následně nakonfigurujte vlastnosti dílčího workflowu pomocí ručního úkolu.</span><span class="sxs-lookup"><span data-stu-id="ffa49-106">Then use the following procedures to configure the properties for the manual task.</span></span>

## <a name="name-the-task"></a><span data-ttu-id="ffa49-107">Pojmenování úlohy</span><span class="sxs-lookup"><span data-stu-id="ffa49-107">Name the task</span></span>

<span data-ttu-id="ffa49-108">Pomocí následujících kroků zadejte název ručního úkolu.</span><span class="sxs-lookup"><span data-stu-id="ffa49-108">Follow these steps to enter a name for the manual task.</span></span>

1. <span data-ttu-id="ffa49-109">V levém podokně klepněte na tlačítko **Základní nastavení**.</span><span class="sxs-lookup"><span data-stu-id="ffa49-109">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="ffa49-110">Do pole **Název** zadejte jedinečný název úlohy.</span><span class="sxs-lookup"><span data-stu-id="ffa49-110">In the **Name** field, enter a unique name for the task.</span></span>

## <a name="enter-a-subject-line-and-instructions"></a><span data-ttu-id="ffa49-111">Zadání řádku předmětu a pokynů</span><span class="sxs-lookup"><span data-stu-id="ffa49-111">Enter a subject line and instructions</span></span>

<span data-ttu-id="ffa49-112">Musíte zadat řádek předmětu a pokyny pro uživatele přiřazené k dané úkolu.</span><span class="sxs-lookup"><span data-stu-id="ffa49-112">You must provide a subject line and instructions to users who are assigned to the task.</span></span> <span data-ttu-id="ffa49-113">Například pokud konfigurujete úkol pro nákupní požadavky, uživatel, který je k úkolu přiřazen, uvidí řádek s předmětem a pokyny na stránce **Nákupní žádanky**.</span><span class="sxs-lookup"><span data-stu-id="ffa49-113">For example, if you're configuring a task for purchase requisitions, the user who is assigned to the task sees the subject line and instructions on the **Purchase requisitions** page.</span></span> <span data-ttu-id="ffa49-114">Řádek předmětu se zobrazí na panelu zpráv na stránce.</span><span class="sxs-lookup"><span data-stu-id="ffa49-114">The subject line appears in a message bar on the page.</span></span> <span data-ttu-id="ffa49-115">Uživatel poté může kliknutím na ikonu na panelu zpráv zobrazit pokyny.</span><span class="sxs-lookup"><span data-stu-id="ffa49-115">The user can then click the icon in the message bar to view the instructions.</span></span> <span data-ttu-id="ffa49-116">K zadání řádku předmětu a pokynů použijte následující postup.</span><span class="sxs-lookup"><span data-stu-id="ffa49-116">Follow these steps to enter a subject line and instructions.</span></span>

1. <span data-ttu-id="ffa49-117">V levém podokně klepněte na tlačítko **Základní nastavení**.</span><span class="sxs-lookup"><span data-stu-id="ffa49-117">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="ffa49-118">V poli **Předmět pracovní položky** zadejte řádek předmětu.</span><span class="sxs-lookup"><span data-stu-id="ffa49-118">In the **Work item subject** field, enter the subject line.</span></span>
3. <span data-ttu-id="ffa49-119">Řádek předmětu můžete přizpůsobit vložením zástupného textu.</span><span class="sxs-lookup"><span data-stu-id="ffa49-119">To personalize the subject line, you can insert placeholders.</span></span> <span data-ttu-id="ffa49-120">Zástupný text bude při zobrazení řádku předmětu uživatelům nahrazen odpovídacími daty.</span><span class="sxs-lookup"><span data-stu-id="ffa49-120">Placeholders are replaced with appropriate data when the subject line is shown to users.</span></span> <span data-ttu-id="ffa49-121">Při vkládání zástupného textu postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="ffa49-121">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="ffa49-122">V textovém poli klepnutím zadejte, kde se má zástupný text zobrazit.</span><span class="sxs-lookup"><span data-stu-id="ffa49-122">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="ffa49-123">Klikněte na **Vložit zástupný text**.</span><span class="sxs-lookup"><span data-stu-id="ffa49-123">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="ffa49-124">V nově otevřeném seznamu vyberte vkládaný zástupný text.</span><span class="sxs-lookup"><span data-stu-id="ffa49-124">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="ffa49-125">Klepněte na tlačítko **Vložit**.</span><span class="sxs-lookup"><span data-stu-id="ffa49-125">Click **Insert**.</span></span>

4. <span data-ttu-id="ffa49-126">Chcete-li přidat překlady řádku předmětu, postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="ffa49-126">To add translations of the subject line, follow these steps:</span></span>

    1. <span data-ttu-id="ffa49-127">Klikněte na **Překlady**.</span><span class="sxs-lookup"><span data-stu-id="ffa49-127">Click **Translations**.</span></span>
    2. <span data-ttu-id="ffa49-128">Na nově otevřené stránce klikněte na **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="ffa49-128">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="ffa49-129">V nově otevřeném seznamu vyberte jazyk, který chcete použít pro zadání textu.</span><span class="sxs-lookup"><span data-stu-id="ffa49-129">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="ffa49-130">V poli **Přeložený text** zadejte text.</span><span class="sxs-lookup"><span data-stu-id="ffa49-130">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="ffa49-131">Text můžete přizpůsobit vložením zástupného textu podle pokynů v kroku 3.</span><span class="sxs-lookup"><span data-stu-id="ffa49-131">To personalize the text, you can insert placeholders as described in step 3.</span></span>
    6. <span data-ttu-id="ffa49-132">Klepněte na tlačítko **Zavřít**.</span><span class="sxs-lookup"><span data-stu-id="ffa49-132">Click **Close**.</span></span>

5. <span data-ttu-id="ffa49-133">V poli **Pokyny pracovní položky** zadejte pokyny.</span><span class="sxs-lookup"><span data-stu-id="ffa49-133">In the **Work item instructions** field, enter the instructions.</span></span>
6. <span data-ttu-id="ffa49-134">Pokyny můžete přizpůsobit vložením zástupného textu.</span><span class="sxs-lookup"><span data-stu-id="ffa49-134">To personalize the instructions, you can insert placeholders.</span></span> <span data-ttu-id="ffa49-135">Zástupný text bude při zobrazení pokynů uživatelům nahrazen odpovídacími daty.</span><span class="sxs-lookup"><span data-stu-id="ffa49-135">Placeholders are replaced with appropriate data when the instructions are shown to users.</span></span> <span data-ttu-id="ffa49-136">Při vkládání zástupného textu postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="ffa49-136">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="ffa49-137">V textovém poli klepnutím zadejte, kde se má zástupný text zobrazit.</span><span class="sxs-lookup"><span data-stu-id="ffa49-137">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="ffa49-138">Klikněte na **Vložit zástupný text**.</span><span class="sxs-lookup"><span data-stu-id="ffa49-138">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="ffa49-139">V nově otevřeném seznamu vyberte vkládaný zástupný text.</span><span class="sxs-lookup"><span data-stu-id="ffa49-139">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="ffa49-140">Klepněte na tlačítko **Vložit**.</span><span class="sxs-lookup"><span data-stu-id="ffa49-140">Click **Insert**.</span></span>

7. <span data-ttu-id="ffa49-141">Chcete-li přidat překlady pokynů, postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="ffa49-141">To add translations of the instructions, follow these steps:</span></span>

    1. <span data-ttu-id="ffa49-142">Klikněte na **Překlady**.</span><span class="sxs-lookup"><span data-stu-id="ffa49-142">Click **Translations**.</span></span>
    2. <span data-ttu-id="ffa49-143">Na nově otevřené stránce klikněte na **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="ffa49-143">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="ffa49-144">V nově otevřeném seznamu vyberte jazyk, který chcete použít pro zadání textu.</span><span class="sxs-lookup"><span data-stu-id="ffa49-144">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="ffa49-145">V poli **Přeložený text** zadejte text.</span><span class="sxs-lookup"><span data-stu-id="ffa49-145">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="ffa49-146">Text můžete přizpůsobit vložením zástupného textu podle pokynů v kroku 6.</span><span class="sxs-lookup"><span data-stu-id="ffa49-146">To personalize the text, you can insert placeholders as described in step 6.</span></span>
    6. <span data-ttu-id="ffa49-147">Klepněte na tlačítko **Zavřít**.</span><span class="sxs-lookup"><span data-stu-id="ffa49-147">Click **Close**.</span></span>

## <a name="assign-the-task"></a><span data-ttu-id="ffa49-148">Přiřazení úlohy</span><span class="sxs-lookup"><span data-stu-id="ffa49-148">Assign the task</span></span>

<span data-ttu-id="ffa49-149">Pomocí následujícího postupu určíte, komu má být ruční úkol přiřazen.</span><span class="sxs-lookup"><span data-stu-id="ffa49-149">Follow these steps to specify who the manual task should be assigned to.</span></span>

1. <span data-ttu-id="ffa49-150">V levém podokně klikněte na **Přiřazení**.</span><span class="sxs-lookup"><span data-stu-id="ffa49-150">In the left pane, click **Assignment**.</span></span>
2. <span data-ttu-id="ffa49-151">Na kartě **Typ přiřazení** vyberte jednu z možností v následující tabulce a před přechodem na krok 3 postupujte podle dalších kroků pro tuto možnost.</span><span class="sxs-lookup"><span data-stu-id="ffa49-151">On the **Assignment type** tab, select one of the options in the following table, and then follow the additional steps for that option before you go to step 3.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="ffa49-152">Možnost</span><span class="sxs-lookup"><span data-stu-id="ffa49-152">Option</span></span></th>
    <th><span data-ttu-id="ffa49-153">Uživatelé, ke kterým je úkol přiřazen</span><span class="sxs-lookup"><span data-stu-id="ffa49-153">Users that the task is assigned to</span></span></th>
    <th><span data-ttu-id="ffa49-154">Další kroky</span><span class="sxs-lookup"><span data-stu-id="ffa49-154">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="ffa49-155">Účastník</span><span class="sxs-lookup"><span data-stu-id="ffa49-155">Participant</span></span></td>
    <td><span data-ttu-id="ffa49-156">Uživatelé, kteří jsou přiřazeni k určité skupině nebo roli</span><span class="sxs-lookup"><span data-stu-id="ffa49-156">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="ffa49-157">Po výběru možnosti <strong>Účastník</strong> na kartě <strong>Založeno na roli</strong> v seznamu <strong>Typ účastníka</strong> vyberte typ skupiny nebo role, ke které chcete úkol přiřadit.</span><span class="sxs-lookup"><span data-stu-id="ffa49-157">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to assign the task to.</span></span></li>
    <li><span data-ttu-id="ffa49-158">V seznamu <strong>Účastník</strong> vyberte skupinu nebo roli, ke které chcete úkol přiřadit.</span><span class="sxs-lookup"><span data-stu-id="ffa49-158">In the <strong>Participant</strong> list, select the group or role to assign the task to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="ffa49-159">Hierarchie</span><span class="sxs-lookup"><span data-stu-id="ffa49-159">Hierarchy</span></span></td>
    <td><span data-ttu-id="ffa49-160">Uživatelé v určité organizační hierarchii</span><span class="sxs-lookup"><span data-stu-id="ffa49-160">Users in a specific organizational hierarchy</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="ffa49-161">Po výběru možnosti <strong>Hierarchie</strong> na kartě <strong>Výběr hierarchie</strong> v seznamu <strong>Typ hierarchie</strong> vyberte typ hierarchie, ke které chcete úkol přiřadit.</span><span class="sxs-lookup"><span data-stu-id="ffa49-161">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to assign the task to.</span></span></li>
    <li><span data-ttu-id="ffa49-162">Systém musí z hierarchie načíst rozsah jmen uživatelů.</span><span class="sxs-lookup"><span data-stu-id="ffa49-162">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="ffa49-163">Tato jména představují uživatele, ke kterým může být úkol přiřazen.</span><span class="sxs-lookup"><span data-stu-id="ffa49-163">These names represent users that the task can be assigned to.</span></span> <span data-ttu-id="ffa49-164">Podle těchto kroků určete počáteční a koncový bod rozsahu uživatelských jmen, které systém obdrží:</span><span class="sxs-lookup"><span data-stu-id="ffa49-164">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="ffa49-165">Chcete-li zadat počáteční bod, vyberte osobu v seznamu <strong>Začátek od</strong>.</span><span class="sxs-lookup"><span data-stu-id="ffa49-165">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="ffa49-166">Chcete-li zadat koncový bod, klepněte na možnost <strong>Přidat podmínku</strong>.</span><span class="sxs-lookup"><span data-stu-id="ffa49-166">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="ffa49-167">Poté zadáním podmínky označte, kde v hierarchii má systém přestat načítat jména.</span><span class="sxs-lookup"><span data-stu-id="ffa49-167">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="ffa49-168">Na kartě <strong>Možnosti hierarchie</strong> zadejte uživatele v rozsahu, ke kterým by měl být úkol přiřazen:</span><span class="sxs-lookup"><span data-stu-id="ffa49-168">On the <strong>Hierarchy options</strong> tab, specify which users in the range the task should be assigned to:</span></span> <ul>
    <li><span data-ttu-id="ffa49-169"><strong>Přiřadit všechny načtené uživatele</strong> – úkol bude přiřazen všem uživatelům v rozsahu.</span><span class="sxs-lookup"><span data-stu-id="ffa49-169"><strong>Assign to all users retrieved</strong> – The task is assigned to all users in the range.</span></span></li>
    <li><span data-ttu-id="ffa49-170"><strong>Přiřadit pouze poslednímu načtenému uživateli</strong> – úkol bude přiřazen pouze poslednímu uživateli v rozsahu.</span><span class="sxs-lookup"><span data-stu-id="ffa49-170"><strong>Assign only to last user retrieved</strong> – The task is assigned to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="ffa49-171"><strong>Vyloučit uživatele splňující následující podmínku</strong> – úkol není přiřazen žádnému uživateli v rozsahu, který odpovídá konkrétní podmínce.</span><span class="sxs-lookup"><span data-stu-id="ffa49-171"><strong>Exclude users with the following condition</strong> – The task isn't assigned to users in the range who meet a specific condition.</span></span> <span data-ttu-id="ffa49-172">Po klepnutí na volbu <strong>Přidat podmínku</strong> určete požadovanou podmínku.</span><span class="sxs-lookup"><span data-stu-id="ffa49-172">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="ffa49-173">Uživatel workflowu</span><span class="sxs-lookup"><span data-stu-id="ffa49-173">Workflow user</span></span></td>
    <td><span data-ttu-id="ffa49-174">Uživatelé v aktuálním workflowu</span><span class="sxs-lookup"><span data-stu-id="ffa49-174">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="ffa49-175">Po výběru možnosti <strong>Uživatel workflowu</strong> na kartě <strong>Uživatel workflowu</strong> v seznamu <strong>Uživatel workflowu</strong> vyberte uživatele, který se podílí na workflowu.</span><span class="sxs-lookup"><span data-stu-id="ffa49-175">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="ffa49-176">Uživatel</span><span class="sxs-lookup"><span data-stu-id="ffa49-176">User</span></span></td>
    <td><span data-ttu-id="ffa49-177">Konkrétní uživatelé</span><span class="sxs-lookup"><span data-stu-id="ffa49-177">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="ffa49-178">Po výběru možnosti <strong>Uživatel</strong> klepněte na kartu <strong>Uživatel</strong>.</span><span class="sxs-lookup"><span data-stu-id="ffa49-178">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="ffa49-179">Seznam <strong>Dostupní uživatelé</strong> obsahuje všechny uživatele.</span><span class="sxs-lookup"><span data-stu-id="ffa49-179">The <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="ffa49-180">Vyberte uživatele, ke kterým chcete úkol přiřadit, a pak přesuňte tyto uživatele do seznamu <strong>Vybraní uživatelé</strong>.</span><span class="sxs-lookup"><span data-stu-id="ffa49-180">Select the users to assign the task to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="ffa49-181">Fronta</span><span class="sxs-lookup"><span data-stu-id="ffa49-181">Queue</span></span></td>
    <td><span data-ttu-id="ffa49-182">Fronta pracovních položek</span><span class="sxs-lookup"><span data-stu-id="ffa49-182">A work item queue</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="ffa49-183">Po výběru možnosti <strong>Fronta</strong> klepněte na kartu <strong>Založeno na frontě</strong>.</span><span class="sxs-lookup"><span data-stu-id="ffa49-183">After you select <strong>Queue</strong>, click the <strong>Queue based</strong> tab.</span></span></li>
    <li><span data-ttu-id="ffa49-184">Chcete-li přiřadit úkol konkrétní frontě, postupujte následujícím způsobem:</span><span class="sxs-lookup"><span data-stu-id="ffa49-184">To assign the task to a specific queue, follow these steps:</span></span> <ol>
    <li><span data-ttu-id="ffa49-185">V seznamu <strong>Typ fronty</strong> vyberte <strong>Fronty pracovních položek</strong>.</span><span class="sxs-lookup"><span data-stu-id="ffa49-185">In the <strong>Queue type</strong> list, select <strong>Work item queues</strong>.</span></span></li>
    <li><span data-ttu-id="ffa49-186">V seznamu <strong>Název fronty</strong> vyberte frontu.</span><span class="sxs-lookup"><span data-stu-id="ffa49-186">In the <strong>Queue name</strong> list, select the queue.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="ffa49-187">Pokud by konkrétní podmínka měla určit frontu, ke které bude úkol přiřazen, postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="ffa49-187">If a specific condition should determine which queue the task is assigned to, follow these steps:</span></span> <ol>
    <li><span data-ttu-id="ffa49-188">V seznamu <strong>Typ fronty</strong> vyberte <strong>Podmíněné fronty pracovních položek</strong>.</span><span class="sxs-lookup"><span data-stu-id="ffa49-188">In the <strong>Queue type</strong> list, select <strong>Conditional work item queues</strong>.</span></span></li>
    <li><span data-ttu-id="ffa49-189">V seznamu <strong>Název fronty</strong> vyberte <strong>Podmíněná fronta</strong>.</span><span class="sxs-lookup"><span data-stu-id="ffa49-189">In the <strong>Queue name</strong> list, select <strong>Conditional queue</strong>.</span></span></li>
    </ol>
    </li>
    </ol>
    <blockquote>[!NOTE] <span data-ttu-id="ffa49-190">Tato možnost se používá pouze u několika workflowů, jako je například správa případů.</span><span class="sxs-lookup"><span data-stu-id="ffa49-190">This option is used for only a few workflows, such as Case management.</span></span></blockquote>
    </td>
    </tr>
    </tbody>
    </table>

3. <span data-ttu-id="ffa49-191">Na kartě **Časový limit** v poli **Trvání** určete, kolik času má uživatel na dokončení úkolu.</span><span class="sxs-lookup"><span data-stu-id="ffa49-191">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to complete the task.</span></span> <span data-ttu-id="ffa49-192">Vyberte některou z následujících možností:</span><span class="sxs-lookup"><span data-stu-id="ffa49-192">Select one of the following options:</span></span>

    - <span data-ttu-id="ffa49-193">**Hodiny** – zadejte počet hodin, které má uživatel na dokončení úkolu.</span><span class="sxs-lookup"><span data-stu-id="ffa49-193">**Hours** – Enter the number of hours that the user has to complete the task.</span></span> <span data-ttu-id="ffa49-194">Pak vyberte kalendář, který vaše organizace používá, a zadejte informace o pracovním týdnu vaší organizace.</span><span class="sxs-lookup"><span data-stu-id="ffa49-194">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="ffa49-195">**Dny** – zadejte počet dnů, které má uživatel na dokončení úkolu.</span><span class="sxs-lookup"><span data-stu-id="ffa49-195">**Days** – Enter the number of days that the user has to complete the task.</span></span> <span data-ttu-id="ffa49-196">Pak vyberte kalendář, který vaše organizace používá, a zadejte informace o pracovním týdnu vaší organizace.</span><span class="sxs-lookup"><span data-stu-id="ffa49-196">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="ffa49-197">**Týdny** – zadejte počet týdnů, které má uživatel na dokončení úkolu.</span><span class="sxs-lookup"><span data-stu-id="ffa49-197">**Weeks** – Enter the number of weeks that the user has to complete the task.</span></span>
    - <span data-ttu-id="ffa49-198">**Měsíce** – vyberte den a týden, do kdy musí uživatel dokončit úkol.</span><span class="sxs-lookup"><span data-stu-id="ffa49-198">**Months** – Select the day and week that the user must complete the task by.</span></span> <span data-ttu-id="ffa49-199">Můžete například požadovat, aby uživatel úlohu dokončil do třetího pátku v daném měsíci.</span><span class="sxs-lookup"><span data-stu-id="ffa49-199">For example, you might want the user to complete the task by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="ffa49-200">**Roky** – vyberte den, týden a měsíc, do kdy musí uživatel dokončit úkol.</span><span class="sxs-lookup"><span data-stu-id="ffa49-200">**Years** – Select the day, week, and month that the user must complete the task by.</span></span> <span data-ttu-id="ffa49-201">Můžete například požadovat, aby uživatel úlohu dokončil do třetího pátku v prosinci.</span><span class="sxs-lookup"><span data-stu-id="ffa49-201">For example, you might want the user to complete the task by Friday of the third week of December.</span></span>

    <span data-ttu-id="ffa49-202">Pokud uživatel v přiděleném čase úkol nedokončí, úkol bude v prodlení.</span><span class="sxs-lookup"><span data-stu-id="ffa49-202">If the user doesn't complete the task in the allotted time, the task is overdue.</span></span> <span data-ttu-id="ffa49-203">Úkol v prodlení je eskalován na základě možností vybraných v oblasti stránky **Eskalace**.</span><span class="sxs-lookup"><span data-stu-id="ffa49-203">A task that is overdue can be escalated, based on the options that you select in the **Escalation** area of the page.</span></span>

## <a name="specify-what-happens-when-the-task-is-overdue"></a><span data-ttu-id="ffa49-204">Určení akce prováděné při zpoždění úlohy</span><span class="sxs-lookup"><span data-stu-id="ffa49-204">Specify what happens when the task is overdue</span></span>

<span data-ttu-id="ffa49-205">Pokud uživatel v přiděleném čase ruční úkol nedokončí, úkol bude v prodlení.</span><span class="sxs-lookup"><span data-stu-id="ffa49-205">If a user doesn't complete the manual task in the allotted time, the task is overdue.</span></span> <span data-ttu-id="ffa49-206">Úkol, který je v prodlení, může být eskalován nebo automaticky přiřazen jinému uživateli.</span><span class="sxs-lookup"><span data-stu-id="ffa49-206">A task that is overdue can be escalated, or automatically assigned to another user.</span></span> <span data-ttu-id="ffa49-207">Pro eskalování úkolu v prodlení postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="ffa49-207">Follow these steps to escalate the task if it's overdue.</span></span>

1. <span data-ttu-id="ffa49-208">V levém podokně klikněte na **Eskalování**.</span><span class="sxs-lookup"><span data-stu-id="ffa49-208">In the left pane, click **Escalation**.</span></span>
2. <span data-ttu-id="ffa49-209">Označte pole **Použít eskalační cestu** a vytvořte tak eskalační cestu.</span><span class="sxs-lookup"><span data-stu-id="ffa49-209">Select the **Use escalation path** check box to create an escalation path.</span></span> <span data-ttu-id="ffa49-210">Systém automaticky přiřadí daný úkol uživatelům uvedeným v cestě eskalace.</span><span class="sxs-lookup"><span data-stu-id="ffa49-210">The system automatically assigns the task to the users who are listed in the escalation path.</span></span> <span data-ttu-id="ffa49-211">Například v následující tabulce naleznete příklad eskalační cesty.</span><span class="sxs-lookup"><span data-stu-id="ffa49-211">For example, the following table represents an escalation path.</span></span>

    | <span data-ttu-id="ffa49-212">Pořadí</span><span class="sxs-lookup"><span data-stu-id="ffa49-212">Sequence</span></span> | <span data-ttu-id="ffa49-213">Eskalační cesta</span><span class="sxs-lookup"><span data-stu-id="ffa49-213">Escalation path</span></span>      |
    |----------|----------------------|
    | <span data-ttu-id="ffa49-214">1</span><span class="sxs-lookup"><span data-stu-id="ffa49-214">1</span></span>        | <span data-ttu-id="ffa49-215">Přiřadit k: Donna</span><span class="sxs-lookup"><span data-stu-id="ffa49-215">Assign to: Donna</span></span>     |
    | <span data-ttu-id="ffa49-216">2</span><span class="sxs-lookup"><span data-stu-id="ffa49-216">2</span></span>        | <span data-ttu-id="ffa49-217">Přiřadit k: Erin</span><span class="sxs-lookup"><span data-stu-id="ffa49-217">Assign to: Erin</span></span>      |
    | <span data-ttu-id="ffa49-218">3</span><span class="sxs-lookup"><span data-stu-id="ffa49-218">3</span></span>        | <span data-ttu-id="ffa49-219">Finální akce: odmítnutí</span><span class="sxs-lookup"><span data-stu-id="ffa49-219">Final action: Reject</span></span> |

    <span data-ttu-id="ffa49-220">V tomto příkladu systém přiřadí zpožděný úkol Donně.</span><span class="sxs-lookup"><span data-stu-id="ffa49-220">In this example, the system assigns the overdue task to Donna.</span></span> <span data-ttu-id="ffa49-221">Pokud ji Donna v určeném čase úkol nedokončí, systém přiřadí úkol Erin.</span><span class="sxs-lookup"><span data-stu-id="ffa49-221">If Donna doesn't complete the task in the allotted time, the system assigns the task to Erin.</span></span> <span data-ttu-id="ffa49-222">Pokud Erin v přiděleném čase úkol nedokončí, systému dokument odeslaný ke zpracování zamítne.</span><span class="sxs-lookup"><span data-stu-id="ffa49-222">If Erin doesn't complete the task in the allotted time, the system rejects the document that was submitted for processing.</span></span>

3. <span data-ttu-id="ffa49-223">Pokud chcete přidat uživatele do eskalační cesty, klepněte na tlačítko **Přidat eskalaci**.</span><span class="sxs-lookup"><span data-stu-id="ffa49-223">To add a user to the escalation path, click **Add escalation**.</span></span> <span data-ttu-id="ffa49-224">Na kartě **Typ přiřazení** vyberte jednu z možností v následující tabulce a před přechodem na krok 4 postupujte podle dalších kroků pro tuto možnost.</span><span class="sxs-lookup"><span data-stu-id="ffa49-224">On the **Assignment type** tab, select one of the options in the following table, and then follow the additional steps for that option before you go to step 4.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="ffa49-225">Možnost</span><span class="sxs-lookup"><span data-stu-id="ffa49-225">Option</span></span></th>
    <th><span data-ttu-id="ffa49-226">Uživatelé, ke kterým je úkol eskalován</span><span class="sxs-lookup"><span data-stu-id="ffa49-226">Users that the task is escalated to</span></span></th>
    <th><span data-ttu-id="ffa49-227">Další kroky</span><span class="sxs-lookup"><span data-stu-id="ffa49-227">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="ffa49-228">Hierarchie</span><span class="sxs-lookup"><span data-stu-id="ffa49-228">Hierarchy</span></span></td>
    <td><span data-ttu-id="ffa49-229">Uživatelé v určité organizační hierarchii</span><span class="sxs-lookup"><span data-stu-id="ffa49-229">Users in a specific organizational hierarchy</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="ffa49-230">Po výběru možnosti <strong>Hierarchie</strong> na kartě <strong>Výběr hierarchie</strong> v seznamu <strong>Typ hierarchie</strong> vyberte typ hierarchie, ke které chcete úkol eskalovat.</span><span class="sxs-lookup"><span data-stu-id="ffa49-230">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to escalate the task to.</span></span></li>
    <li><span data-ttu-id="ffa49-231">Systém musí z hierarchie načíst rozsah jmen uživatelů.</span><span class="sxs-lookup"><span data-stu-id="ffa49-231">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="ffa49-232">Tato jména představují uživatele, ke kterým může být úkol eskalován.</span><span class="sxs-lookup"><span data-stu-id="ffa49-232">These names represent users that the task can be escalated to.</span></span> <span data-ttu-id="ffa49-233">Podle těchto kroků určete počáteční a koncový bod rozsahu uživatelských jmen, které systém obdrží:</span><span class="sxs-lookup"><span data-stu-id="ffa49-233">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="ffa49-234">Chcete-li zadat počáteční bod, vyberte osobu v seznamu <strong>Začátek od</strong>.</span><span class="sxs-lookup"><span data-stu-id="ffa49-234">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="ffa49-235">Chcete-li zadat koncový bod, klepněte na možnost <strong>Přidat podmínku</strong>.</span><span class="sxs-lookup"><span data-stu-id="ffa49-235">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="ffa49-236">Poté zadáním podmínky označte, kde v hierarchii má systém přestat načítat jména.</span><span class="sxs-lookup"><span data-stu-id="ffa49-236">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="ffa49-237">Na kartě <strong>Možnosti hierarchie</strong> zadejte uživatele v rozsahu, ke kterým by měl být úkol eskalován:</span><span class="sxs-lookup"><span data-stu-id="ffa49-237">On the <strong>Hierarchy options</strong> tab, specify which users in the range the task should be escalated to:</span></span> <ul>
    <li><span data-ttu-id="ffa49-238"><strong>Přiřadit všechny načtené uživatele</strong> – úkol bude eskalován všem uživatelům v rozsahu.</span><span class="sxs-lookup"><span data-stu-id="ffa49-238"><strong>Assign to all users retrieved</strong> – The task is escalated to all users in the range.</span></span></li>
    <li><span data-ttu-id="ffa49-239"><strong>Přiřadit pouze poslednímu načtenému uživateli</strong> – úkol bude eskalován pouze poslednímu uživateli v rozsahu.</span><span class="sxs-lookup"><span data-stu-id="ffa49-239"><strong>Assign only to last user retrieved</strong> – The task is escalated to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="ffa49-240"><strong>Vyloučit uživatele splňující následující podmínku</strong> – úkol není eskalován žádnému uživateli v rozsahu, který odpovídá konkrétní podmínce.</span><span class="sxs-lookup"><span data-stu-id="ffa49-240"><strong>Exclude users with the following condition</strong> – This task isn't escalated to users in the range who meet a specific condition.</span></span> <span data-ttu-id="ffa49-241">Po klepnutí na volbu <strong>Přidat podmínku</strong> určete požadovanou podmínku.</span><span class="sxs-lookup"><span data-stu-id="ffa49-241">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="ffa49-242">Uživatel workflowu</span><span class="sxs-lookup"><span data-stu-id="ffa49-242">Workflow user</span></span></td>
    <td><span data-ttu-id="ffa49-243">Uživatelé v aktuálním workflowu</span><span class="sxs-lookup"><span data-stu-id="ffa49-243">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="ffa49-244">Po výběru možnosti <strong>Uživatel workflowu</strong> na kartě <strong>Uživatel workflowu</strong> v seznamu <strong>Uživatel workflowu</strong> vyberte uživatele, který se podílí na workflowu.</span><span class="sxs-lookup"><span data-stu-id="ffa49-244">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="ffa49-245">Uživatel</span><span class="sxs-lookup"><span data-stu-id="ffa49-245">User</span></span></td>
    <td><span data-ttu-id="ffa49-246">Konkrétní uživatelé</span><span class="sxs-lookup"><span data-stu-id="ffa49-246">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="ffa49-247">Po výběru možnosti <strong>Uživatel</strong> klepněte na kartu <strong>Uživatel</strong>.</span><span class="sxs-lookup"><span data-stu-id="ffa49-247">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="ffa49-248">Seznam <strong>Dostupní uživatelé</strong> obsahuje všechny uživatele.</span><span class="sxs-lookup"><span data-stu-id="ffa49-248">The <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="ffa49-249">Vyberte uživatele, kterým chcete úkol eskalovat, a pak přesuňte tyto uživatele do seznamu <strong>Vybraní uživatelé</strong>.</span><span class="sxs-lookup"><span data-stu-id="ffa49-249">Select the users to escalate the task to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

4. <span data-ttu-id="ffa49-250">Na kartě **Časový limit** v poli **Trvání** určete, kolik času má uživatel na dokončení úkolu.</span><span class="sxs-lookup"><span data-stu-id="ffa49-250">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to complete the task.</span></span> <span data-ttu-id="ffa49-251">Vyberte některou z následujících možností:</span><span class="sxs-lookup"><span data-stu-id="ffa49-251">Select one of the following options:</span></span>

    - <span data-ttu-id="ffa49-252">**Hodiny** – zadejte počet hodin, které má uživatel na dokončení úkolu.</span><span class="sxs-lookup"><span data-stu-id="ffa49-252">**Hours** – Enter the number of hours that the user has to complete the task.</span></span> <span data-ttu-id="ffa49-253">Pak vyberte kalendář, který vaše organizace používá, a zadejte informace o pracovním týdnu vaší organizace.</span><span class="sxs-lookup"><span data-stu-id="ffa49-253">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="ffa49-254">**Dny** – zadejte počet dnů, které má uživatel na dokončení úkolu.</span><span class="sxs-lookup"><span data-stu-id="ffa49-254">**Days** – Enter the number of days that the user has to complete the task.</span></span> <span data-ttu-id="ffa49-255">Pak vyberte kalendář, který vaše organizace používá, a zadejte informace o pracovním týdnu vaší organizace.</span><span class="sxs-lookup"><span data-stu-id="ffa49-255">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="ffa49-256">**Týdny** – zadejte počet týdnů, které má uživatel na dokončení úkolu.</span><span class="sxs-lookup"><span data-stu-id="ffa49-256">**Weeks** – Enter the number of weeks that the user has to complete the task.</span></span>
    - <span data-ttu-id="ffa49-257">**Měsíce** – vyberte den a týden, do kdy musí uživatel dokončit úkol.</span><span class="sxs-lookup"><span data-stu-id="ffa49-257">**Months** – Select the day and week that the user must complete the task by.</span></span> <span data-ttu-id="ffa49-258">Můžete například požadovat, aby uživatel úlohu dokončil do třetího pátku v daném měsíci.</span><span class="sxs-lookup"><span data-stu-id="ffa49-258">For example, you might want the user to complete the task by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="ffa49-259">**Roky** – vyberte den, týden a měsíc, do kdy musí uživatel dokončit úkol.</span><span class="sxs-lookup"><span data-stu-id="ffa49-259">**Years** – Select the day, week, and month that the user must complete the task by.</span></span> <span data-ttu-id="ffa49-260">Můžete například požadovat, aby uživatel úlohu dokončil do třetího pátku v prosinci.</span><span class="sxs-lookup"><span data-stu-id="ffa49-260">For example, you might want the user to complete the task by Friday of the third week of December.</span></span>

5. <span data-ttu-id="ffa49-261">Zopakujte kroky 3 a 4 u každého uživatele, který má být přidán do eskalační cesty.</span><span class="sxs-lookup"><span data-stu-id="ffa49-261">Repeat steps 3 through 4 for each user that should be added to the escalation path.</span></span> <span data-ttu-id="ffa49-262">Pořadí uživatelů lze změnit.</span><span class="sxs-lookup"><span data-stu-id="ffa49-262">You can change the order of the users.</span></span>
6. <span data-ttu-id="ffa49-263">Pokud uživatelé v eskalační cestě v určeném čase úkol nedokončí, systém sám provede u úkolu vhodnou akci.</span><span class="sxs-lookup"><span data-stu-id="ffa49-263">If the users in the escalation path don't complete the task in the allotted time, the system takes action on the task.</span></span> <span data-ttu-id="ffa49-264">Akci, kterou systém provede, můžete vybrat výběrem řádku **Akce** a na kartě **Konečná akce** vyberte akci.</span><span class="sxs-lookup"><span data-stu-id="ffa49-264">To specify the action that the system takes, select the **Action** row, and then, on the **End action** tab, select an action.</span></span>

## <a name="specify-when-the-system-automatically-acts-on-the-task"></a><span data-ttu-id="ffa49-265">Určení podmínky, podle které systém automaticky provede akci u úkolu</span><span class="sxs-lookup"><span data-stu-id="ffa49-265">Specify when the system automatically acts on the task</span></span>

<span data-ttu-id="ffa49-266">Systém lze nastavit tak, aby při splnění určitých podmínek prováděl akce u ručních úkolů.</span><span class="sxs-lookup"><span data-stu-id="ffa49-266">You can configure the system to take action on the manual task if specific conditions are met.</span></span> <span data-ttu-id="ffa49-267">Například úkol bude vyžadovat, aby člen oddělení pro vyúčtování výdajů zkontrolovat příjmové doklady, které byly odeslány společně s vyúčtováním výdajů.</span><span class="sxs-lookup"><span data-stu-id="ffa49-267">For example, a task requires that a member of the Expense reports department review the receipts that are submitted together with an expense report.</span></span> <span data-ttu-id="ffa49-268">Podle zásad společnosti musí být tento úkol proveden v případě, že celková částka vyúčtování výdajů bude větší než 100 USD.</span><span class="sxs-lookup"><span data-stu-id="ffa49-268">According to company policy, this task must be performed if the total amount of the expense report is more than USD 100.</span></span> <span data-ttu-id="ffa49-269">V tomto scénáři lze systém nastavit tak, aby automaticky označil úkol za **Dokončený** v situaci, kdy je celková částka nižší než 100.</span><span class="sxs-lookup"><span data-stu-id="ffa49-269">In this scenario, you can configure the system to automatically mark the task as **Complete** when the total amount is less than 100.</span></span> <span data-ttu-id="ffa49-270">Pomocí tohoto postupu určete podmínky, za kterých má systém zpracovávat ruční úkol.</span><span class="sxs-lookup"><span data-stu-id="ffa49-270">Follow these steps to specify when the system takes action on the manual task.</span></span>

1. <span data-ttu-id="ffa49-271">V levém podokně klepněte na tlačítko **Automatické akce**.</span><span class="sxs-lookup"><span data-stu-id="ffa49-271">In the left pane, click **Automatic actions**.</span></span>
2. <span data-ttu-id="ffa49-272">Označte pole **Povolit automatické akce**.</span><span class="sxs-lookup"><span data-stu-id="ffa49-272">Select the **Enable automatic actions** check box.</span></span>
3. <span data-ttu-id="ffa49-273">Klepněte na možnost **Přidat podmínku**.</span><span class="sxs-lookup"><span data-stu-id="ffa49-273">Click **Add condition**.</span></span>
4. <span data-ttu-id="ffa49-274">Zadání podmínky</span><span class="sxs-lookup"><span data-stu-id="ffa49-274">Enter a condition.</span></span>
5. <span data-ttu-id="ffa49-275">Zadejte všechny další podmínky, které jsou požadovány.</span><span class="sxs-lookup"><span data-stu-id="ffa49-275">Enter any additional conditions that are required.</span></span>
6. <span data-ttu-id="ffa49-276">Chcete-li ověřit, zda jsou zadané podmínky nastaveny správně, postupujte následovně:</span><span class="sxs-lookup"><span data-stu-id="ffa49-276">To verify that the conditions that you entered are configured correctly, follow these steps:</span></span>

    1. <span data-ttu-id="ffa49-277">Klepněte na možnost **Test**.</span><span class="sxs-lookup"><span data-stu-id="ffa49-277">Click **Test**.</span></span>
    2. <span data-ttu-id="ffa49-278">Na stránce **Podmínka testovacího workflowu** v oblasti **Ověřit podmínku** vyberte záznam.</span><span class="sxs-lookup"><span data-stu-id="ffa49-278">On the **Test workflow condition** page, in the **Validate condition** area, select a record.</span></span>
    3. <span data-ttu-id="ffa49-279">Klepněte na možnost **Test**.</span><span class="sxs-lookup"><span data-stu-id="ffa49-279">Click **Test**.</span></span> <span data-ttu-id="ffa49-280">Systém záznam vyhodnotí a určí, zda odpovídá zadaným podmínkám.</span><span class="sxs-lookup"><span data-stu-id="ffa49-280">The system evaluates the record to determine whether it meets the conditions that you defined.</span></span>
    4. <span data-ttu-id="ffa49-281">Klikněte na tlačítko **OK** nebo klepnutím na tlačítko **Storno** se vraťte na stránku **Vlastnosti**.</span><span class="sxs-lookup"><span data-stu-id="ffa49-281">Click **OK** or **Cancel** to return to the **Properties** page.</span></span>

7. <span data-ttu-id="ffa49-282">V seznamu **Akce automatického dokončení** vyberte akci, která má být u úkolu provedena.</span><span class="sxs-lookup"><span data-stu-id="ffa49-282">In the **Auto complete action** list, select the action that the system should take on the task.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="ffa49-283">Zadejte, kdy se mají odesílat oznámení.</span><span class="sxs-lookup"><span data-stu-id="ffa49-283">Specify when notifications are sent</span></span>

<span data-ttu-id="ffa49-284">Při delegování, eskalování, dokončení nebo zamítnutí ruční úlohy a při zadání požadavku na změnu můžete zaslat oznámení určeným osobám.</span><span class="sxs-lookup"><span data-stu-id="ffa49-284">You can send notifications to people when a manual task has been delegated, escalated, completed, or rejected, or when a change has been requested.</span></span> <span data-ttu-id="ffa49-285">Podle těchto kroků můžete určit oznámení, které se odešle, a osoby, kterým se odešle.</span><span class="sxs-lookup"><span data-stu-id="ffa49-285">Follow these steps to specify when notifications are sent, and who the notifications are sent to.</span></span>

1. <span data-ttu-id="ffa49-286">V levém podokně klikněte na **Oznámení**.</span><span class="sxs-lookup"><span data-stu-id="ffa49-286">In the left pane, click **Notifications**.</span></span>
2. <span data-ttu-id="ffa49-287">Označte pole vedle událostí, při kterých se oznámení odešle:</span><span class="sxs-lookup"><span data-stu-id="ffa49-287">Select the check box next to the events that notifications should be sent for:</span></span>

    - <span data-ttu-id="ffa49-288">**Delegovat** – úkol byl přiřazen jinému uživateli.</span><span class="sxs-lookup"><span data-stu-id="ffa49-288">**Delegate** – The task has been assigned to another user.</span></span>
    - <span data-ttu-id="ffa49-289">**Eskalovat** – přiřazený uživatel nedokončil úkol v přiděleném čase.</span><span class="sxs-lookup"><span data-stu-id="ffa49-289">**Escalate** – The assigned user hasn't completed the task in the allotted time.</span></span>
    - <span data-ttu-id="ffa49-290">**Dokončit** – přiřazený uživatel dokončil úkol.</span><span class="sxs-lookup"><span data-stu-id="ffa49-290">**Complete** – The assigned user has completed the task.</span></span>
    - <span data-ttu-id="ffa49-291">**Odmítnout** – přiřazený uživatel odmítl dokument, který byl odeslán.</span><span class="sxs-lookup"><span data-stu-id="ffa49-291">**Reject** – The assigned user has rejected the document that was submitted.</span></span>
    - <span data-ttu-id="ffa49-292">**Žádost o změnu** – přiřazený uživatel požádal o změnu dokumentu, který byl odeslán.</span><span class="sxs-lookup"><span data-stu-id="ffa49-292">**Request change** – The assigned user has requested a change to the document that was submitted.</span></span>

3. <span data-ttu-id="ffa49-293">Vyberte řádek pro událost, kterou jste vybrali v kroku 2.</span><span class="sxs-lookup"><span data-stu-id="ffa49-293">Select the row for an event that you selected in step 2.</span></span>
4. <span data-ttu-id="ffa49-294">Na kartě **Text oznámení** zadejte v textovém poli text oznámení.</span><span class="sxs-lookup"><span data-stu-id="ffa49-294">On the **Notification text** tab, in the text box, enter the text of the notification.</span></span>
5. <span data-ttu-id="ffa49-295">Oznámení můžete přizpůsobit vložením zástupného textu.</span><span class="sxs-lookup"><span data-stu-id="ffa49-295">To personalize the notification, you can insert placeholders.</span></span> <span data-ttu-id="ffa49-296">Zástupný text bude při zobrazení oznámení uživatelům nahrazen odpovídacími informacemi.</span><span class="sxs-lookup"><span data-stu-id="ffa49-296">Placeholders are replaced with appropriate information when the notification is shown to users.</span></span> <span data-ttu-id="ffa49-297">Při vkládání zástupného textu postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="ffa49-297">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="ffa49-298">V textovém poli klepnutím zadejte, kde se má zástupný text zobrazit.</span><span class="sxs-lookup"><span data-stu-id="ffa49-298">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="ffa49-299">Klikněte na **Vložit zástupný text**.</span><span class="sxs-lookup"><span data-stu-id="ffa49-299">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="ffa49-300">V nově otevřeném seznamu vyberte vkládaný zástupný text.</span><span class="sxs-lookup"><span data-stu-id="ffa49-300">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="ffa49-301">Klepněte na tlačítko **Vložit**.</span><span class="sxs-lookup"><span data-stu-id="ffa49-301">Click **Insert**.</span></span>

6. <span data-ttu-id="ffa49-302">Chcete-li přidat překlady oznámení, postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="ffa49-302">To add translations of the notification, follow these steps:</span></span>

    1. <span data-ttu-id="ffa49-303">Klikněte na **Překlady**.</span><span class="sxs-lookup"><span data-stu-id="ffa49-303">Click **Translations**.</span></span>
    2. <span data-ttu-id="ffa49-304">Na nově otevřené stránce klikněte na **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="ffa49-304">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="ffa49-305">V nově otevřeném seznamu vyberte jazyk, který chcete použít pro zadání textu.</span><span class="sxs-lookup"><span data-stu-id="ffa49-305">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="ffa49-306">V poli **Přeložený text** zadejte text.</span><span class="sxs-lookup"><span data-stu-id="ffa49-306">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="ffa49-307">Text můžete přizpůsobit vložením zástupného textu podle pokynů v kroku 5.</span><span class="sxs-lookup"><span data-stu-id="ffa49-307">To personalize the text, you can insert placeholders as described in step 5.</span></span>
    6. <span data-ttu-id="ffa49-308">Klepněte na tlačítko **Zavřít**.</span><span class="sxs-lookup"><span data-stu-id="ffa49-308">Click **Close**.</span></span>

7. <span data-ttu-id="ffa49-309">Na kartě **Příjemce** zadejte osoby, kterým budou upozornění odesílána.</span><span class="sxs-lookup"><span data-stu-id="ffa49-309">On the **Recipient** tab, specify who the notifications are sent to.</span></span> <span data-ttu-id="ffa49-310">Vyberte jednu z možností v následující tabulce a před přechodem na krok 8 postupujte podle dalších kroků pro tuto možnost.</span><span class="sxs-lookup"><span data-stu-id="ffa49-310">Select one of the options in the following table, and then follow the additional steps for that option before you go to step 8.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="ffa49-311">Možnost</span><span class="sxs-lookup"><span data-stu-id="ffa49-311">Option</span></span></th>
    <th><span data-ttu-id="ffa49-312">Příjemce oznámení</span><span class="sxs-lookup"><span data-stu-id="ffa49-312">Notification recipients</span></span></th>
    <th><span data-ttu-id="ffa49-313">Další kroky</span><span class="sxs-lookup"><span data-stu-id="ffa49-313">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="ffa49-314">Účastník</span><span class="sxs-lookup"><span data-stu-id="ffa49-314">Participant</span></span></td>
    <td><span data-ttu-id="ffa49-315">Uživatelé, kteří jsou přiřazeni k určité skupině nebo roli</span><span class="sxs-lookup"><span data-stu-id="ffa49-315">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="ffa49-316">Po výběru možnosti <strong>Účastník</strong> na kartě <strong>Založeno na roli</strong> v seznamu <strong>Typ účastníka</strong> vyberte typ skupiny nebo role, které chcete oznámení odeslat.</span><span class="sxs-lookup"><span data-stu-id="ffa49-316">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="ffa49-317">V seznamu <strong>Účastník</strong> vyberte skupinu nebo roli, které chcete oznámení odeslat.</span><span class="sxs-lookup"><span data-stu-id="ffa49-317">In the <strong>Participant</strong> list, select the group or role to send notifications to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="ffa49-318">Uživatel workflowu</span><span class="sxs-lookup"><span data-stu-id="ffa49-318">Workflow user</span></span></td>
    <td><span data-ttu-id="ffa49-319">Uživatelé v aktuálním workflowu</span><span class="sxs-lookup"><span data-stu-id="ffa49-319">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="ffa49-320">Po výběru možnosti <strong>Uživatel workflowu</strong> na kartě <strong>Uživatel workflowu</strong> v seznamu <strong>Uživatel workflowu</strong> vyberte uživatele, který se podílí na workflowu.</span><span class="sxs-lookup"><span data-stu-id="ffa49-320">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="ffa49-321">Uživatel</span><span class="sxs-lookup"><span data-stu-id="ffa49-321">User</span></span></td>
    <td><span data-ttu-id="ffa49-322">Konkrétní uživatelé</span><span class="sxs-lookup"><span data-stu-id="ffa49-322">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="ffa49-323">Po výběru možnosti <strong>Uživatel</strong> klepněte na kartu <strong>Uživatel</strong>.</span><span class="sxs-lookup"><span data-stu-id="ffa49-323">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="ffa49-324">Seznam <strong>Dostupní uživatelé</strong> obsahuje všechny uživatele.</span><span class="sxs-lookup"><span data-stu-id="ffa49-324">The <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="ffa49-325">Vyberte uživatele, kterým chcete odeslat oznámení, a pak přesuňte tyto uživatele do seznamu <strong>Vybraní uživatelé</strong>.</span><span class="sxs-lookup"><span data-stu-id="ffa49-325">Select the users to send notifications to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

8. <span data-ttu-id="ffa49-326">Zopakujte kroky 3 až 7 pro každou událost, kterou jste vybrali v kroku 2.</span><span class="sxs-lookup"><span data-stu-id="ffa49-326">Repeat steps 3 through 7 for each event that you selected in step 2.</span></span>

## <a name="set-a-time-limit"></a><span data-ttu-id="ffa49-327">Nastavení časového limitu</span><span class="sxs-lookup"><span data-stu-id="ffa49-327">Set a time limit</span></span>

<span data-ttu-id="ffa49-328">Tento postup použijte, pokud je ruční úkol nutné dokončit v určitém čase.</span><span class="sxs-lookup"><span data-stu-id="ffa49-328">Follow these steps if the manual task must be completed in a specific time.</span></span>

> [!NOTE]
> <span data-ttu-id="ffa49-329">Možnosti, které vyberete v rámci této procedury, přepíší možnosti vybrané v oblasti **Přiřazení** a **Eskalace** na stránce.</span><span class="sxs-lookup"><span data-stu-id="ffa49-329">The options that you select in this procedure override the options that you selected in the **Assignment** and **Escalation** areas of the page.</span></span>

1. <span data-ttu-id="ffa49-330">V levém podokně klepněte na tlačítko **Pokročilá nastavení**.</span><span class="sxs-lookup"><span data-stu-id="ffa49-330">In the left pane, click **Advanced settings**.</span></span>
2. <span data-ttu-id="ffa49-331">Označte pole **Nastavit časový limit pro prvek workflowu**.</span><span class="sxs-lookup"><span data-stu-id="ffa49-331">Select the **Set a time limit for the workflow element** check box.</span></span>
3. <span data-ttu-id="ffa49-332">V poli **Trvání** upřesněte, kdy má být úloha dokončena.</span><span class="sxs-lookup"><span data-stu-id="ffa49-332">In the **Duration** field, specify when the task must be completed.</span></span> <span data-ttu-id="ffa49-333">Vyberte některou z následujících možností:</span><span class="sxs-lookup"><span data-stu-id="ffa49-333">Select one of the following options:</span></span>

    - <span data-ttu-id="ffa49-334">**Hodiny** – zadejte počet hodin, během kterých má být úkol dokončen.</span><span class="sxs-lookup"><span data-stu-id="ffa49-334">**Hours** – Enter the number of hours that the task must be completed in.</span></span> <span data-ttu-id="ffa49-335">Pak vyberte kalendář, který vaše organizace používá, a zadejte informace o pracovním týdnu vaší organizace.</span><span class="sxs-lookup"><span data-stu-id="ffa49-335">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="ffa49-336">**Dny** – zadejte počet dnů, během kterých má být úkol dokončen.</span><span class="sxs-lookup"><span data-stu-id="ffa49-336">**Days** – Enter the number of days that the task must be completed in.</span></span> <span data-ttu-id="ffa49-337">Pak vyberte kalendář, který vaše organizace používá, a zadejte informace o pracovním týdnu vaší organizace.</span><span class="sxs-lookup"><span data-stu-id="ffa49-337">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="ffa49-338">**Týdny** – zadejte počet týdnů, během kterých má být úkol dokončen.</span><span class="sxs-lookup"><span data-stu-id="ffa49-338">**Weeks** – Enter the number of weeks that the task must be completed in.</span></span>
    - <span data-ttu-id="ffa49-339">**Měsíce** – vyberte den a týden, do kdy má být úkol dokončen.</span><span class="sxs-lookup"><span data-stu-id="ffa49-339">**Months** – Select the day and week that the task must be completed by.</span></span> <span data-ttu-id="ffa49-340">Můžete například požadovat, aby byl úkol dokončen do třetího pátku v daném měsíci.</span><span class="sxs-lookup"><span data-stu-id="ffa49-340">For example, you might want the task to be completed by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="ffa49-341">**Roky** – vyberte den, týden a měsíc, do kdy má být úkol dokončen.</span><span class="sxs-lookup"><span data-stu-id="ffa49-341">**Years** – Select the day, week, and month that the task must be completed by.</span></span> <span data-ttu-id="ffa49-342">Můžete například požadovat, aby byl úkol dokončen do třetího pátku v prosinci.</span><span class="sxs-lookup"><span data-stu-id="ffa49-342">For example, you might want the task to be completed by Friday of the third week of December.</span></span>

4. <span data-ttu-id="ffa49-343">Dojde-li k překročení časového limitu, systém u úlohy provede akci.</span><span class="sxs-lookup"><span data-stu-id="ffa49-343">If the time limit is exceeded, the system takes action on the task.</span></span> <span data-ttu-id="ffa49-344">V seznamu **Akce** vyberte akci, která má být provedena.</span><span class="sxs-lookup"><span data-stu-id="ffa49-344">In the **Action** list, select the action that the system should take.</span></span>

## <a name="specify-which-actions-are-available-to-the-user"></a><span data-ttu-id="ffa49-345">Určení dostupných akcí pro uživatele</span><span class="sxs-lookup"><span data-stu-id="ffa49-345">Specify which actions are available to the user</span></span>

<span data-ttu-id="ffa49-346">Po přiřazení ruční úlohy uživateli musí uživatel danou úlohu zpracovat.</span><span class="sxs-lookup"><span data-stu-id="ffa49-346">When the manual task is assigned to a user, the user must take action on the task.</span></span> <span data-ttu-id="ffa49-347">Pomocí tohoto postupu určete akce, které může uživatel u úkolu provádět.</span><span class="sxs-lookup"><span data-stu-id="ffa49-347">Follow these steps to specify which actions the user can take on the task.</span></span>

> [!NOTE]
> <span data-ttu-id="ffa49-348">Dostupné akce se budou lišit v závislosti na tom, jak byl úkol navržen.</span><span class="sxs-lookup"><span data-stu-id="ffa49-348">The actions that are available vary, depending on the design of the task.</span></span>

1. <span data-ttu-id="ffa49-349">V levém podokně klepněte na tlačítko **Pokročilá nastavení**.</span><span class="sxs-lookup"><span data-stu-id="ffa49-349">In the left pane, click **Advanced settings**.</span></span>
2. <span data-ttu-id="ffa49-350">Chcete-li uživateli umožnit, aby úkol označil jako **Dokončený**, označte pole **Dokončený**.</span><span class="sxs-lookup"><span data-stu-id="ffa49-350">Select the **Complete** check box if the user should be able to mark the task as **Complete**.</span></span>
3. <span data-ttu-id="ffa49-351">Chcete-li uživateli umožnit označení odeslaného dokumentu jako zamítnutého, označte pole **Zamítnout**.</span><span class="sxs-lookup"><span data-stu-id="ffa49-351">Select the **Reject** check box if the user should be able to reject the document that was submitted.</span></span>
4. <span data-ttu-id="ffa49-352">Chcete-li uživateli umožnit vyžádání změn v odeslaném dokumentu, zaškrtněte políčko **Požadavek na změnu**.</span><span class="sxs-lookup"><span data-stu-id="ffa49-352">Select the **Request change** check box if the user should be able to request changes to the document that was submitted.</span></span>
5. <span data-ttu-id="ffa49-353">Chcete-li uživateli umožnit, aby úlohu postoupil jinému uživateli, zaškrtněte políčko **Delegovat**.</span><span class="sxs-lookup"><span data-stu-id="ffa49-353">Select the **Delegate** check box if the user should be able to assign the task to another user.</span></span>
6. <span data-ttu-id="ffa49-354">Chcete-li uživateli umožnit, aby úlohu přeřadil jinému uživateli ve frontě pracovních položek, označte pole **Znovu přiřadit**.</span><span class="sxs-lookup"><span data-stu-id="ffa49-354">Select the **Reassign** check box if the user should be able to reassign the task to another user in the work item queue.</span></span>
7. <span data-ttu-id="ffa49-355">Chcete-li uživateli umožnit, aby úlohu přeřadil do fronty pracovních položek, označte pole **Uvolnit**.</span><span class="sxs-lookup"><span data-stu-id="ffa49-355">Select the **Release** check box if the user should be able to reassign the task to the work item queue.</span></span> <span data-ttu-id="ffa49-356">Jiný uživatel pak může úkol dokončit.</span><span class="sxs-lookup"><span data-stu-id="ffa49-356">Another user can then complete the task.</span></span>
