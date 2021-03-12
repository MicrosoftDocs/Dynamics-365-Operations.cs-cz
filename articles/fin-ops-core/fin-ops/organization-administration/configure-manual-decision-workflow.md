---
title: Konfigurace ručních rozhodnutí ve workflow
description: Toto téma vysvětluje, jak nakonfigurovat vlastnosti ručního rozhodnutí.
author: ChrisGarty
manager: AnnBe
ms.date: 06/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 192101
ms.assetid: 0bccad77-1a44-4f08-967b-12c62c02afc7
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d351facbce02355ddb4bdf91d43d9df561e4f3b5
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/19/2020
ms.locfileid: "4798845"
---
# <a name="configure-manual-decisions-in-a-workflow"></a><span data-ttu-id="3478b-103">Konfigurace ručních rozhodnutí ve workflow</span><span class="sxs-lookup"><span data-stu-id="3478b-103">Configure manual decisions in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3478b-104">Toto téma vysvětluje, jak nakonfigurovat vlastnosti ručního rozhodnutí.</span><span class="sxs-lookup"><span data-stu-id="3478b-104">This topic explains how to configure the properties of a manual decision.</span></span>

<span data-ttu-id="3478b-105">Pokud budete chtít nakonfigurovat ruční rozhodnutí v editoru workflowu, klikněte pravým tlačítkem myši na ruční rozhodnutí a kliknutím na tlačítko **Vlastnosti** otevřete stránku **Vlastnosti**.</span><span class="sxs-lookup"><span data-stu-id="3478b-105">To configure a manual decision in the workflow editor, right-click the manual decision, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="3478b-106">Následně nakonfigurujte vlastnosti dílčího workflowu pomocí ručního rozhodnutí.</span><span class="sxs-lookup"><span data-stu-id="3478b-106">Then use the following procedures to configure the properties of the manual decision.</span></span>

## <a name="name-the-decision"></a><span data-ttu-id="3478b-107">Název rozhodnutí</span><span class="sxs-lookup"><span data-stu-id="3478b-107">Name the decision</span></span>

<span data-ttu-id="3478b-108">Pomocí následujících kroků zadejte název ručního rozhodnutí.</span><span class="sxs-lookup"><span data-stu-id="3478b-108">Follow these steps to enter a name for the manual decision.</span></span>

1. <span data-ttu-id="3478b-109">V levém podokně klepněte na tlačítko **Základní nastavení**.</span><span class="sxs-lookup"><span data-stu-id="3478b-109">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="3478b-110">V poli **Název** zadejte jedinečný název ručního rozhodnutí.</span><span class="sxs-lookup"><span data-stu-id="3478b-110">In the **Name** field, enter a unique name for the manual decision.</span></span>

## <a name="enter-a-subject-line-and-instructions"></a><span data-ttu-id="3478b-111">Zadání řádku předmětu a pokynů</span><span class="sxs-lookup"><span data-stu-id="3478b-111">Enter a subject line and instructions</span></span>

<span data-ttu-id="3478b-112">Musíte zadat řádek předmětu a pokyny pro uživatele přiřazené k tomuto ručnímu rozhodnutí.</span><span class="sxs-lookup"><span data-stu-id="3478b-112">You must provide a subject line and instructions to users who are assigned to the manual decision.</span></span> <span data-ttu-id="3478b-113">Například pokud konfigurujete rozhodnutí pro nákupní požadavky, uživatel, který je k rozhodnutí přiřazeno, uvidí řádek s předmětem a pokyny na stránce **Nákupní žádanky**.</span><span class="sxs-lookup"><span data-stu-id="3478b-113">For example, if you're configuring a decision for purchase requisitions, the user who is assigned to the decision sees the subject line and instructions on the **Purchase requisitions** page.</span></span> <span data-ttu-id="3478b-114">Řádek předmětu se zobrazí na panelu zpráv na stránce.</span><span class="sxs-lookup"><span data-stu-id="3478b-114">The subject line appears in a message bar on the page.</span></span> <span data-ttu-id="3478b-115">Uživatel poté může kliknutím na ikonu na panelu zpráv zobrazit pokyny.</span><span class="sxs-lookup"><span data-stu-id="3478b-115">The user can then click the icon in the message bar to view the instructions.</span></span> <span data-ttu-id="3478b-116">K zadání řádku předmětu a pokynů použijte následující postup.</span><span class="sxs-lookup"><span data-stu-id="3478b-116">Follow these steps to enter a subject line and instructions.</span></span>

1. <span data-ttu-id="3478b-117">V levém podokně klepněte na tlačítko **Základní nastavení**.</span><span class="sxs-lookup"><span data-stu-id="3478b-117">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="3478b-118">Na kartě **Pokyny** v poli **Předmět pracovní položky** zadejte řádek předmětu.</span><span class="sxs-lookup"><span data-stu-id="3478b-118">On the **Instructions** tab, in the **Work item subject** field, enter the subject line.</span></span>
3. <span data-ttu-id="3478b-119">Řádek předmětu můžete přizpůsobit vložením zástupného textu.</span><span class="sxs-lookup"><span data-stu-id="3478b-119">To personalize the subject line, you can insert placeholders.</span></span> <span data-ttu-id="3478b-120">Zástupný text bude při zobrazení řádku předmětu uživatelům nahrazen odpovídacími daty.</span><span class="sxs-lookup"><span data-stu-id="3478b-120">Placeholders are replaced with appropriate data when the subject line is shown to users.</span></span> <span data-ttu-id="3478b-121">Při vkládání zástupného textu postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="3478b-121">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="3478b-122">V textovém poli klepnutím zadejte, kde se má zástupný text zobrazit.</span><span class="sxs-lookup"><span data-stu-id="3478b-122">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="3478b-123">Klikněte na **Vložit zástupný text**.</span><span class="sxs-lookup"><span data-stu-id="3478b-123">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="3478b-124">V nově otevřeném seznamu vyberte vkládaný zástupný text.</span><span class="sxs-lookup"><span data-stu-id="3478b-124">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="3478b-125">Klepněte na tlačítko **Vložit**.</span><span class="sxs-lookup"><span data-stu-id="3478b-125">Click **Insert**.</span></span>

4. <span data-ttu-id="3478b-126">Chcete-li přidat překlady řádku předmětu, postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="3478b-126">To add translations of the subject line, follow these steps:</span></span>

    1. <span data-ttu-id="3478b-127">Klikněte na **Překlady**.</span><span class="sxs-lookup"><span data-stu-id="3478b-127">Click **Translations**.</span></span>
    2. <span data-ttu-id="3478b-128">Na nově otevřené stránce klikněte na **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="3478b-128">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="3478b-129">V nově otevřeném seznamu vyberte jazyk, který chcete použít pro zadání textu.</span><span class="sxs-lookup"><span data-stu-id="3478b-129">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="3478b-130">V poli **Přeložený text** zadejte text.</span><span class="sxs-lookup"><span data-stu-id="3478b-130">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="3478b-131">Text můžete přizpůsobit vložením zástupného textu podle pokynů v kroku 3.</span><span class="sxs-lookup"><span data-stu-id="3478b-131">To personalize the text, you can insert placeholders as described in step 3.</span></span>
    6. <span data-ttu-id="3478b-132">Klepněte na tlačítko **Zavřít**.</span><span class="sxs-lookup"><span data-stu-id="3478b-132">Click **Close**.</span></span>

5. <span data-ttu-id="3478b-133">V poli **Pokyny pracovní položky** zadejte pokyny.</span><span class="sxs-lookup"><span data-stu-id="3478b-133">In the **Work item instructions** field, enter the instructions.</span></span>
6. <span data-ttu-id="3478b-134">Pokyny můžete přizpůsobit vložením zástupného textu.</span><span class="sxs-lookup"><span data-stu-id="3478b-134">To personalize the instructions, you can insert placeholders.</span></span> <span data-ttu-id="3478b-135">Zástupný text bude při zobrazení pokynů uživatelům nahrazen odpovídacími daty.</span><span class="sxs-lookup"><span data-stu-id="3478b-135">Placeholders are replaced with appropriate data when the instructions are shown to users.</span></span> <span data-ttu-id="3478b-136">Při vkládání zástupného textu postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="3478b-136">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="3478b-137">V textovém poli klepnutím zadejte, kde se má zástupný text zobrazit.</span><span class="sxs-lookup"><span data-stu-id="3478b-137">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="3478b-138">Klikněte na **Vložit zástupný text**.</span><span class="sxs-lookup"><span data-stu-id="3478b-138">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="3478b-139">V nově otevřeném seznamu vyberte vkládaný zástupný text.</span><span class="sxs-lookup"><span data-stu-id="3478b-139">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="3478b-140">Klepněte na tlačítko **Vložit**.</span><span class="sxs-lookup"><span data-stu-id="3478b-140">Click **Insert**.</span></span>

7. <span data-ttu-id="3478b-141">Chcete-li přidat překlady pokynů, postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="3478b-141">To add translations of the instructions, follow these steps:</span></span>

    1. <span data-ttu-id="3478b-142">Klikněte na **Překlady**.</span><span class="sxs-lookup"><span data-stu-id="3478b-142">Click **Translations**.</span></span>
    2. <span data-ttu-id="3478b-143">Na nově otevřené stránce klikněte na **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="3478b-143">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="3478b-144">V nově otevřeném seznamu vyberte jazyk, který chcete použít pro zadání textu.</span><span class="sxs-lookup"><span data-stu-id="3478b-144">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="3478b-145">V poli **Přeložený text** zadejte text.</span><span class="sxs-lookup"><span data-stu-id="3478b-145">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="3478b-146">Text můžete přizpůsobit vložením zástupného textu podle pokynů v kroku 6.</span><span class="sxs-lookup"><span data-stu-id="3478b-146">To personalize the text, you can insert placeholders as described in step 6.</span></span>
    6. <span data-ttu-id="3478b-147">Klepněte na tlačítko **Zavřít**.</span><span class="sxs-lookup"><span data-stu-id="3478b-147">Click **Close**.</span></span>

## <a name="specify-the-possible-outcomes-of-a-decision"></a><span data-ttu-id="3478b-148">Určete možné výsledky rozhodnutí</span><span class="sxs-lookup"><span data-stu-id="3478b-148">Specify the possible outcomes of a decision</span></span>

<span data-ttu-id="3478b-149">obvykle pokud je dokument přiřazen pracovníkovi s rozhodovací pravomocí, je tomuto pracovníkovi kladena otázka.</span><span class="sxs-lookup"><span data-stu-id="3478b-149">Typically, when a document is assigned to a decision maker, the decision maker is asked a question.</span></span> <span data-ttu-id="3478b-150">Na tuto otázku se obvykle odpovídá možnostmi **Ano** nebo **Ne**, nebo **Pravda** nebo **Nepravda**.</span><span class="sxs-lookup"><span data-stu-id="3478b-150">The answer to this question is usually **Yes** or **No**, or **True** or **False**.</span></span> <span data-ttu-id="3478b-151">Podle následujících kroků můžete určit možné výsledky ručního rozhodnutí.</span><span class="sxs-lookup"><span data-stu-id="3478b-151">Follow these steps to specify the possible outcomes of the manual decision.</span></span>

1. <span data-ttu-id="3478b-152">V levém podokně klepněte na tlačítko **Základní nastavení**.</span><span class="sxs-lookup"><span data-stu-id="3478b-152">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="3478b-153">Na kartě **Výsledky** v poli **Výsledek 1** zadejte název výsledku nebo možnost.</span><span class="sxs-lookup"><span data-stu-id="3478b-153">On the **Outcomes** tab, in the **Outcome 1** field, enter the name of the outcome, or the option.</span></span>
3. <span data-ttu-id="3478b-154">Chcete-li přidat překlady výsledků, postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="3478b-154">To add translations of the outcome, follow these steps:</span></span>

    1. <span data-ttu-id="3478b-155">Klikněte na **Překlady**.</span><span class="sxs-lookup"><span data-stu-id="3478b-155">Click **Translations**.</span></span>
    2. <span data-ttu-id="3478b-156">Na nově otevřené stránce klikněte na **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="3478b-156">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="3478b-157">V nově otevřeném seznamu vyberte jazyk, který chcete použít pro zadání textu.</span><span class="sxs-lookup"><span data-stu-id="3478b-157">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="3478b-158">V poli **Přeložený text** zadejte text.</span><span class="sxs-lookup"><span data-stu-id="3478b-158">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="3478b-159">Klepněte na tlačítko **Zavřít**.</span><span class="sxs-lookup"><span data-stu-id="3478b-159">Click **Close**.</span></span>

4. <span data-ttu-id="3478b-160">V poli **Výsledek 2** zadejte název výsledku nebo možnost.</span><span class="sxs-lookup"><span data-stu-id="3478b-160">In the **Outcome 2** field, enter the name of the outcome, or the option.</span></span>
5. <span data-ttu-id="3478b-161">Chcete-li přidat překlady výsledků, postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="3478b-161">To add translations of the outcome, follow these steps:</span></span>

    1. <span data-ttu-id="3478b-162">Klikněte na **Překlady**.</span><span class="sxs-lookup"><span data-stu-id="3478b-162">Click **Translations**.</span></span>
    2. <span data-ttu-id="3478b-163">Na nově otevřené stránce klikněte na **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="3478b-163">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="3478b-164">V nově otevřeném seznamu vyberte jazyk, který chcete použít pro zadání textu.</span><span class="sxs-lookup"><span data-stu-id="3478b-164">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="3478b-165">V poli **Přeložený text** zadejte text.</span><span class="sxs-lookup"><span data-stu-id="3478b-165">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="3478b-166">Klepněte na tlačítko **Zavřít**.</span><span class="sxs-lookup"><span data-stu-id="3478b-166">Click **Close**.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="3478b-167">Zadejte, kdy se mají odesílat oznámení.</span><span class="sxs-lookup"><span data-stu-id="3478b-167">Specify when notifications are sent</span></span>

<span data-ttu-id="3478b-168">Můžete odeslat oznámení uživatelům, jakmile bude rozhodnutí provedeno, delegováno nebo eskalováno.</span><span class="sxs-lookup"><span data-stu-id="3478b-168">You can send notifications to people when a decision has been made, delegated, or escalated.</span></span> <span data-ttu-id="3478b-169">Podle těchto kroků můžete určit oznámení, které se odešle, a osoby, kterým se odešle.</span><span class="sxs-lookup"><span data-stu-id="3478b-169">Follow these steps to specify when notifications are sent, and who the notifications are sent to.</span></span>

1. <span data-ttu-id="3478b-170">V levém podokně klikněte na **Oznámení**.</span><span class="sxs-lookup"><span data-stu-id="3478b-170">In the left pane, click **Notifications**.</span></span>
2. <span data-ttu-id="3478b-171">Označte pole vedle událostí, při kterých se oznámení odešle:</span><span class="sxs-lookup"><span data-stu-id="3478b-171">Select the check box next to the events that notifications should be sent for:</span></span>

    - <span data-ttu-id="3478b-172">**\[Volba 1\]** – přiřazený uživatel vybral možnost **\[Volba 1\]**.</span><span class="sxs-lookup"><span data-stu-id="3478b-172">**\[Choice 1\]** – The assigned user has selected **\[Choice 1\]**.</span></span>
    - <span data-ttu-id="3478b-173">**\[Volba 2\]** – přiřazený uživatel vybral možnost **\[Volba 2\]**.</span><span class="sxs-lookup"><span data-stu-id="3478b-173">**\[Choice 2\]** – The assigned user has selected **\[Choice 2\]**.</span></span>
    - <span data-ttu-id="3478b-174">**Delegovat** – přiřazený uživatel přiřadil rozhodnutí jinému uživateli.</span><span class="sxs-lookup"><span data-stu-id="3478b-174">**Delegate** – The assigned user has assigned the decision to another user.</span></span>
    - <span data-ttu-id="3478b-175">**Eskalovat** – přiřazený uživatel neučinil rozhodnutí v přiděleném čase.</span><span class="sxs-lookup"><span data-stu-id="3478b-175">**Escalate** – The assigned user hasn't made the decision in the allotted time.</span></span>

3. <span data-ttu-id="3478b-176">Vyberte řádek pro událost, kterou jste vybrali v kroku 2.</span><span class="sxs-lookup"><span data-stu-id="3478b-176">Select the row for an event that you selected in step 2.</span></span>
4. <span data-ttu-id="3478b-177">Na kartě **Text oznámení** zadejte v textovém poli text oznámení.</span><span class="sxs-lookup"><span data-stu-id="3478b-177">On the **Notification text** tab, in the text box, enter the text of the notification.</span></span>
5. <span data-ttu-id="3478b-178">Oznámení můžete přizpůsobit vložením zástupného textu.</span><span class="sxs-lookup"><span data-stu-id="3478b-178">To personalize the notification, you can insert placeholders.</span></span> <span data-ttu-id="3478b-179">Zástupný text bude při zobrazení oznámení uživatelům nahrazen odpovídacími daty.</span><span class="sxs-lookup"><span data-stu-id="3478b-179">Placeholders are replaced with appropriate data when the notification is show to users.</span></span> <span data-ttu-id="3478b-180">Při vkládání zástupného textu postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="3478b-180">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="3478b-181">V textovém poli klepnutím zadejte, kde se má zástupný text zobrazit.</span><span class="sxs-lookup"><span data-stu-id="3478b-181">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="3478b-182">Klikněte na **Vložit zástupný text**.</span><span class="sxs-lookup"><span data-stu-id="3478b-182">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="3478b-183">V nově otevřeném seznamu vyberte vkládaný zástupný text.</span><span class="sxs-lookup"><span data-stu-id="3478b-183">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="3478b-184">Klepněte na tlačítko **Vložit**.</span><span class="sxs-lookup"><span data-stu-id="3478b-184">Click **Insert**.</span></span>

6. <span data-ttu-id="3478b-185">Chcete-li přidat překlady oznámení, postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="3478b-185">To add translations of the notification, follow these steps:</span></span>

    1. <span data-ttu-id="3478b-186">Klikněte na **Překlady**.</span><span class="sxs-lookup"><span data-stu-id="3478b-186">Click **Translations**.</span></span>
    2. <span data-ttu-id="3478b-187">Na nově otevřené stránce klikněte na **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="3478b-187">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="3478b-188">V nově otevřeném seznamu vyberte jazyk, který chcete použít pro zadání textu.</span><span class="sxs-lookup"><span data-stu-id="3478b-188">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="3478b-189">V poli **Přeložený text** zadejte text.</span><span class="sxs-lookup"><span data-stu-id="3478b-189">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="3478b-190">Text můžete přizpůsobit vložením zástupného textu podle pokynů v kroku 5.</span><span class="sxs-lookup"><span data-stu-id="3478b-190">To personalize the text, you can insert placeholders as described in step 5.</span></span>
    6. <span data-ttu-id="3478b-191">Klepněte na tlačítko **Zavřít**.</span><span class="sxs-lookup"><span data-stu-id="3478b-191">Click **Close**.</span></span>

7. <span data-ttu-id="3478b-192">Na kartě **Příjemce** zadejte osoby, kterým budou upozornění odesílána.</span><span class="sxs-lookup"><span data-stu-id="3478b-192">On the **Recipient** tab, specify who the notifications are sent to.</span></span> <span data-ttu-id="3478b-193">Vyberte jednu z možností v následující tabulce a před přechodem na krok 8 postupujte podle dalších kroků pro tuto možnost.</span><span class="sxs-lookup"><span data-stu-id="3478b-193">Select one of the options in the following table, and then follow the additional steps for that option before you go to step 8.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="3478b-194">Možnost</span><span class="sxs-lookup"><span data-stu-id="3478b-194">Option</span></span></th>
    <th><span data-ttu-id="3478b-195">Příjemce oznámení</span><span class="sxs-lookup"><span data-stu-id="3478b-195">Notification recipients</span></span></th>
    <th><span data-ttu-id="3478b-196">Další kroky</span><span class="sxs-lookup"><span data-stu-id="3478b-196">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="3478b-197">Účastník</span><span class="sxs-lookup"><span data-stu-id="3478b-197">Participant</span></span></td>
    <td><span data-ttu-id="3478b-198">Uživatelé, kteří jsou přiřazeni k určité skupině nebo roli</span><span class="sxs-lookup"><span data-stu-id="3478b-198">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="3478b-199">Po výběru možnosti <strong>Účastník</strong> na kartě <strong>Založeno na roli</strong> v seznamu <strong>Typ účastníka</strong> vyberte typ skupiny nebo role, které chcete oznámení odeslat.</span><span class="sxs-lookup"><span data-stu-id="3478b-199">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="3478b-200">V seznamu <strong>Účastník</strong> vyberte skupinu, které chcete oznámení odeslat.</span><span class="sxs-lookup"><span data-stu-id="3478b-200">In the <strong>Participant</strong> list, select the group or to send notifications to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="3478b-201">Uživatel workflowu</span><span class="sxs-lookup"><span data-stu-id="3478b-201">Workflow user</span></span></td>
    <td><span data-ttu-id="3478b-202">Uživatelé v aktuálním workflowu</span><span class="sxs-lookup"><span data-stu-id="3478b-202">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="3478b-203">Po výběru možnosti <strong>Uživatel workflowu</strong> na kartě <strong>Uživatel workflowu</strong> v seznamu <strong>Uživatel workflowu</strong> vyberte uživatele, který se podílí na workflowu.</span><span class="sxs-lookup"><span data-stu-id="3478b-203">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="3478b-204">Uživatel</span><span class="sxs-lookup"><span data-stu-id="3478b-204">User</span></span></td>
    <td><span data-ttu-id="3478b-205">Konkrétní uživatelé</span><span class="sxs-lookup"><span data-stu-id="3478b-205">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="3478b-206">Po výběru možnosti <strong>Uživatel</strong> klepněte na kartu <strong>Uživatel</strong>.</span><span class="sxs-lookup"><span data-stu-id="3478b-206">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="3478b-207">Seznam <strong>Dostupní uživatelé</strong> obsahuje všechny uživatele.</span><span class="sxs-lookup"><span data-stu-id="3478b-207">The <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="3478b-208">Vyberte uživatele, kterým chcete odeslat oznámení, a pak přesuňte tyto uživatele do seznamu <strong>Vybraní uživatelé</strong>.</span><span class="sxs-lookup"><span data-stu-id="3478b-208">Select the users to send notifications to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

8. <span data-ttu-id="3478b-209">Zopakujte kroky 3 až 7 pro každou událost, kterou jste vybrali v kroku 2.</span><span class="sxs-lookup"><span data-stu-id="3478b-209">Repeat steps 3 through 7 for each event that you selected in step 2.</span></span>

## <a name="assign-a-decision"></a><span data-ttu-id="3478b-210">Přiřazení rozhodnutí</span><span class="sxs-lookup"><span data-stu-id="3478b-210">Assign a decision</span></span>

<span data-ttu-id="3478b-211">Pomocí následujícího postupu určíte, komu má být ruční rozhodnutí přiřazeno.</span><span class="sxs-lookup"><span data-stu-id="3478b-211">Follow these steps to specify who a manual decision should be assigned to.</span></span>

1. <span data-ttu-id="3478b-212">V levém podokně klikněte na **Přiřazení**.</span><span class="sxs-lookup"><span data-stu-id="3478b-212">In the left pane, click **Assignment**.</span></span>
2. <span data-ttu-id="3478b-213">Na kartě **Typ přiřazení** vyberte jednu z možností v následující tabulce a před přechodem na krok 3 postupujte podle dalších kroků pro tuto možnost.</span><span class="sxs-lookup"><span data-stu-id="3478b-213">On the **Assignment type** tab, select one of the options in the following table, and then follow the additional steps for that option before you go to step 3.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="3478b-214">Možnost</span><span class="sxs-lookup"><span data-stu-id="3478b-214">Option</span></span></th>
    <th><span data-ttu-id="3478b-215">Uživatelé, kterým je rozhodnutí přiřazeno</span><span class="sxs-lookup"><span data-stu-id="3478b-215">Users that the decision is assigned to</span></span></th>
    <th><span data-ttu-id="3478b-216">Další kroky</span><span class="sxs-lookup"><span data-stu-id="3478b-216">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="3478b-217">Účastník</span><span class="sxs-lookup"><span data-stu-id="3478b-217">Participant</span></span></td>
    <td><span data-ttu-id="3478b-218">Uživatelé, kteří jsou přiřazeni k určité skupině nebo roli</span><span class="sxs-lookup"><span data-stu-id="3478b-218">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="3478b-219">Po výběru možnosti <strong>Účastník</strong> na kartě <strong>Založeno na roli</strong> v seznamu <strong>Typ účastníka</strong> vyberte typ skupiny nebo role, které chcete rozhodnutí přiřadit.</span><span class="sxs-lookup"><span data-stu-id="3478b-219">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to assign the decision to.</span></span></li>
    <li><span data-ttu-id="3478b-220">V seznamu <strong>Účastník</strong> vyberte skupinu nebo roli, které chcete rozhodnutí přiřadit.</span><span class="sxs-lookup"><span data-stu-id="3478b-220">In the <strong>Participant</strong> list, select the group or role to assign the decision to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="3478b-221">Hierarchie</span><span class="sxs-lookup"><span data-stu-id="3478b-221">Hierarchy</span></span></td>
    <td><span data-ttu-id="3478b-222">Uživatelé v určité organizační hierarchii</span><span class="sxs-lookup"><span data-stu-id="3478b-222">Users in a specific organizational hierarchy</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="3478b-223">Po výběru možnosti <strong>Hierarchie</strong> na kartě <strong>Výběr hierarchie</strong> v seznamu <strong>Typ hierarchie</strong> vyberte typ hierarchie, které chcete rozhodnutí přiřadit.</span><span class="sxs-lookup"><span data-stu-id="3478b-223">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to assign the decision to.</span></span></li>
    <li><span data-ttu-id="3478b-224">Systém musí z hierarchie načíst rozsah jmen uživatelů.</span><span class="sxs-lookup"><span data-stu-id="3478b-224">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="3478b-225">Tato jména představují uživatele, kterým může být rozhodnutí přiřazen.</span><span class="sxs-lookup"><span data-stu-id="3478b-225">These names represent users that the decision can be assigned to.</span></span> <span data-ttu-id="3478b-226">Podle těchto kroků určete počáteční a koncový bod rozsahu uživatelských jmen, které systém obdrží:</span><span class="sxs-lookup"><span data-stu-id="3478b-226">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="3478b-227">Chcete-li zadat počáteční bod, vyberte osobu v seznamu <strong>Začátek od</strong>.</span><span class="sxs-lookup"><span data-stu-id="3478b-227">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="3478b-228">Chcete-li zadat koncový bod, klepněte na možnost <strong>Přidat podmínku</strong>.</span><span class="sxs-lookup"><span data-stu-id="3478b-228">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="3478b-229">Poté zadáním podmínky označte, kde v hierarchii má systém přestat načítat jména.</span><span class="sxs-lookup"><span data-stu-id="3478b-229">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="3478b-230">Na kartě <strong>Možnosti hierarchie</strong> zadejte uživatele v rozsahu, kterým by měl být rozhodnutí přiřazeno:</span><span class="sxs-lookup"><span data-stu-id="3478b-230">On the <strong>Hierarchy options</strong> tab, specify which users in the range the decision should be assigned to:</span></span> <ul>
    <li><span data-ttu-id="3478b-231"><strong>Přiřadit všechny načtené uživatele</strong> – rozhodnutí bude přiřazeno všem uživatelům v rozsahu.</span><span class="sxs-lookup"><span data-stu-id="3478b-231"><strong>Assign to all users retrieved</strong> – The decision is assigned to all users in the range.</span></span></li>
    <li><span data-ttu-id="3478b-232"><strong>Přiřadit pouze poslednímu načtenému uživateli</strong> – rozhodnutí bude přiřazeno pouze poslednímu uživateli v rozsahu.</span><span class="sxs-lookup"><span data-stu-id="3478b-232"><strong>Assign only to last user retrieved</strong> – The decision is assigned to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="3478b-233"><strong>Vyloučit uživatele splňující následující podmínku</strong> – rozhodnutí není přiřazeno žádnému uživateli v rozsahu, který odpovídá konkrétní podmínce.</span><span class="sxs-lookup"><span data-stu-id="3478b-233"><strong>Exclude users with the following condition</strong> – The decision isn't assigned to any users in the range who meet a specific condition.</span></span> <span data-ttu-id="3478b-234">Po klepnutí na volbu <strong>Přidat podmínku</strong> určete požadovanou podmínku.</span><span class="sxs-lookup"><span data-stu-id="3478b-234">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="3478b-235">Uživatel workflowu</span><span class="sxs-lookup"><span data-stu-id="3478b-235">Workflow user</span></span></td>
    <td><span data-ttu-id="3478b-236">Uživatelé v aktuálním workflowu</span><span class="sxs-lookup"><span data-stu-id="3478b-236">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="3478b-237">Po výběru možnosti <strong>Uživatel workflowu</strong> na kartě <strong>Uživatel workflowu</strong> v seznamu <strong>Uživatel workflowu</strong> vyberte uživatele, který se podílí na workflowu.</span><span class="sxs-lookup"><span data-stu-id="3478b-237">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="3478b-238">Uživatel</span><span class="sxs-lookup"><span data-stu-id="3478b-238">User</span></span></td>
    <td><span data-ttu-id="3478b-239">Konkrétní uživatelé</span><span class="sxs-lookup"><span data-stu-id="3478b-239">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="3478b-240">Po výběru možnosti <strong>Uživatel</strong> klepněte na kartu <strong>Uživatel</strong>.</span><span class="sxs-lookup"><span data-stu-id="3478b-240">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="3478b-241">Seznam <strong>Dostupní uživatelé</strong> obsahuje všechny uživatele.</span><span class="sxs-lookup"><span data-stu-id="3478b-241">The <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="3478b-242">Vyberte uživatele, kterým chcete rozhodnutí přiřadit, a pak přesuňte tyto uživatele do seznamu <strong>Vybraní uživatelé</strong>.</span><span class="sxs-lookup"><span data-stu-id="3478b-242">Select the users to assign the decision to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

3. <span data-ttu-id="3478b-243">Na kartě **Časový limit** v poli **Trvání** určete, kolik času má uživatel na rozhodnutí.</span><span class="sxs-lookup"><span data-stu-id="3478b-243">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to make the decision.</span></span> <span data-ttu-id="3478b-244">Vyberte některou z následujících možností:</span><span class="sxs-lookup"><span data-stu-id="3478b-244">Select one of the following options:</span></span>

    - <span data-ttu-id="3478b-245">**Hodiny** – zadejte počet hodin, které má uživatel na rozhodnutí.</span><span class="sxs-lookup"><span data-stu-id="3478b-245">**Hours** – Enter the number of hours that the user has to make the decision.</span></span> <span data-ttu-id="3478b-246">Pak vyberte kalendář, který vaše organizace používá, a zadejte informace o pracovním týdnu vaší organizace.</span><span class="sxs-lookup"><span data-stu-id="3478b-246">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="3478b-247">**Dny** – zadejte počet dnů, které má uživatel na rozhodnutí.</span><span class="sxs-lookup"><span data-stu-id="3478b-247">**Days** – Enter the number of days that the user has to make the decision.</span></span> <span data-ttu-id="3478b-248">Pak vyberte kalendář, který vaše organizace používá, a zadejte informace o pracovním týdnu vaší organizace.</span><span class="sxs-lookup"><span data-stu-id="3478b-248">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="3478b-249">**Týdny** – zadejte počet týdnů, které má uživatel na rozhodnutí.</span><span class="sxs-lookup"><span data-stu-id="3478b-249">**Weeks** – Enter the number of weeks that the user has to make the decision.</span></span>
    - <span data-ttu-id="3478b-250">**Měsíce** – vyberte den a týden, do kdy se musí uživatel rozhodnout.</span><span class="sxs-lookup"><span data-stu-id="3478b-250">**Months** – Select the day and week that the user must make the decision by.</span></span> <span data-ttu-id="3478b-251">Můžete například požadovat, aby uživatel učinil rozhodnutí do třetího pátku v daném měsíci.</span><span class="sxs-lookup"><span data-stu-id="3478b-251">For example, you might want the user to make the decision by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="3478b-252">**Roky** – vyberte den, týden a měsíc, do kdy se musí uživatel rozhodnout.</span><span class="sxs-lookup"><span data-stu-id="3478b-252">**Years** – Select the day, week, and month that the user must make the decision by.</span></span> <span data-ttu-id="3478b-253">Můžete například požadovat, aby uživatel učinil rozhodnutí do třetího pátku v prosinci.</span><span class="sxs-lookup"><span data-stu-id="3478b-253">For example, you might want the user to make the decision by Friday of the third week of December.</span></span>

    <span data-ttu-id="3478b-254">Pokud uživatel v přiděleném čase rozhodnutí neučiní, rozhodnutí bude v prodlení.</span><span class="sxs-lookup"><span data-stu-id="3478b-254">If the user doesn't make the decision in the allotted time, the decision is overdue.</span></span> <span data-ttu-id="3478b-255">Rozhodnutí v prodlení je eskalován na základě možností vybraných v oblasti stránky **Eskalace**.</span><span class="sxs-lookup"><span data-stu-id="3478b-255">A decision that is overdue is escalated, based on the options that you select in the **Escalation** area of the page.</span></span>

## <a name="specify-what-happens-when-a-decision-is-overdue"></a><span data-ttu-id="3478b-256">Určení akce prováděné při zpoždění rozhodnutí</span><span class="sxs-lookup"><span data-stu-id="3478b-256">Specify what happens when a decision is overdue</span></span>

<span data-ttu-id="3478b-257">Pokud uživatel v přiděleném čase rozhodnutí neučiní, rozhodnutí bude v prodlení.</span><span class="sxs-lookup"><span data-stu-id="3478b-257">If a user doesn't make the decision in the allotted time, the decision is overdue.</span></span> <span data-ttu-id="3478b-258">Rozhodnutí, které je v prodlení, může být eskalováno nebo automaticky přiřazeno jinému uživateli.</span><span class="sxs-lookup"><span data-stu-id="3478b-258">A decision that is overdue can be escalated, or automatically assigned to another user.</span></span> <span data-ttu-id="3478b-259">Pro eskalování rozhodnutí v prodlení postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="3478b-259">Follow these steps to escalate the decision if it's overdue.</span></span>

1. <span data-ttu-id="3478b-260">V levém podokně klikněte na **Eskalování**.</span><span class="sxs-lookup"><span data-stu-id="3478b-260">In the left pane, click **Escalation**.</span></span>
2. <span data-ttu-id="3478b-261">Označte pole **Použít eskalační cestu** a vytvořte tak eskalační cestu.</span><span class="sxs-lookup"><span data-stu-id="3478b-261">Select the **Use escalation path** check box to create an escalation path.</span></span> <span data-ttu-id="3478b-262">Systém automaticky přiřadí dané rozhodnutí uživatelům uvedeným v cestě eskalace.</span><span class="sxs-lookup"><span data-stu-id="3478b-262">The system automatically assigns the decision to the users who are listed in the escalation path.</span></span> <span data-ttu-id="3478b-263">Například v následující tabulce naleznete příklad eskalační cesty.</span><span class="sxs-lookup"><span data-stu-id="3478b-263">For example, the following table represents an escalation path.</span></span>

    | <span data-ttu-id="3478b-264">Pořadí</span><span class="sxs-lookup"><span data-stu-id="3478b-264">Sequence</span></span> | <span data-ttu-id="3478b-265">Eskalační cesta</span><span class="sxs-lookup"><span data-stu-id="3478b-265">Escalation path</span></span>            |
    |----------|----------------------------|
    | <span data-ttu-id="3478b-266">1</span><span class="sxs-lookup"><span data-stu-id="3478b-266">1</span></span>        | <span data-ttu-id="3478b-267">Přiřadit k: Donna</span><span class="sxs-lookup"><span data-stu-id="3478b-267">Assign to: Donna</span></span>           |
    | <span data-ttu-id="3478b-268">2</span><span class="sxs-lookup"><span data-stu-id="3478b-268">2</span></span>        | <span data-ttu-id="3478b-269">Přiřadit k: Erin</span><span class="sxs-lookup"><span data-stu-id="3478b-269">Assign to: Erin</span></span>            |
    | <span data-ttu-id="3478b-270">3</span><span class="sxs-lookup"><span data-stu-id="3478b-270">3</span></span>        | <span data-ttu-id="3478b-271">Konečná akce: \[Volba 1\]</span><span class="sxs-lookup"><span data-stu-id="3478b-271">Final action: \[Choice 1\]</span></span> |

    <span data-ttu-id="3478b-272">V tomto příkladu systém přiřadí zpožděné rozhodnutí Donně.</span><span class="sxs-lookup"><span data-stu-id="3478b-272">In this example, the system assigns the overdue decision to Donna.</span></span> <span data-ttu-id="3478b-273">Pokud Donna v určeném čase rozhodnutí neučiní, systém přiřadí rozhodnutí Erin.</span><span class="sxs-lookup"><span data-stu-id="3478b-273">If Donna doesn't make the decision in the allotted time, the system assigns the decision to Erin.</span></span> <span data-ttu-id="3478b-274">Pokud Erin v určeném čase rozhodnutí neučiní, systém jako rozhodnutí vybere možnost **\[Volba 1\]**.</span><span class="sxs-lookup"><span data-stu-id="3478b-274">If Erin doesn't make the decision in the allotted time, the system selects **\[Choice 1\]** as the decision.</span></span>

3. <span data-ttu-id="3478b-275">Pokud chcete přidat uživatele do eskalační cesty, klepněte na tlačítko **Přidat eskalaci**.</span><span class="sxs-lookup"><span data-stu-id="3478b-275">To add a user to the escalation path, click **Add escalation**.</span></span> <span data-ttu-id="3478b-276">Vyberte jednu z možností v následující tabulce a před přechodem na krok 4 postupujte podle dalších kroků pro tuto možnost.</span><span class="sxs-lookup"><span data-stu-id="3478b-276">Select one of the options in the following table, and then follow the additional steps for that option before you go to step 4.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="3478b-277">Možnost</span><span class="sxs-lookup"><span data-stu-id="3478b-277">Option</span></span></th>
    <th><span data-ttu-id="3478b-278">Uživatelé, kterým je rozhodnutí eskalováno</span><span class="sxs-lookup"><span data-stu-id="3478b-278">Users that the decision is escalated to</span></span></th>
    <th><span data-ttu-id="3478b-279">Další kroky</span><span class="sxs-lookup"><span data-stu-id="3478b-279">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="3478b-280">Hierarchie</span><span class="sxs-lookup"><span data-stu-id="3478b-280">Hierarchy</span></span></td>
    <td><span data-ttu-id="3478b-281">Uživatelé v určité organizační hierarchii</span><span class="sxs-lookup"><span data-stu-id="3478b-281">Users in a specific organizational hierarchy</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="3478b-282">Po výběru možnosti <strong>Hierarchie</strong> na kartě <strong>Výběr hierarchie</strong> v seznamu <strong>Typ hierarchie</strong> vyberte typ hierarchie, ke které rozhodnutí eskalovat.</span><span class="sxs-lookup"><span data-stu-id="3478b-282">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to escalate the decision to.</span></span></li>
    <li><span data-ttu-id="3478b-283">Systém musí z hierarchie načíst rozsah jmen uživatelů.</span><span class="sxs-lookup"><span data-stu-id="3478b-283">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="3478b-284">Tato jména představují uživatele, ke kterým může být rozhodnutí eskalováno.</span><span class="sxs-lookup"><span data-stu-id="3478b-284">These names represent users that the decision can be escalated to.</span></span> <span data-ttu-id="3478b-285">Podle těchto kroků určete počáteční a koncový bod rozsahu uživatelských jmen, které systém obdrží:</span><span class="sxs-lookup"><span data-stu-id="3478b-285">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="3478b-286">Chcete-li zadat počáteční bod, vyberte osobu v seznamu <strong>Začátek od</strong>.</span><span class="sxs-lookup"><span data-stu-id="3478b-286">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="3478b-287">Chcete-li zadat koncový bod, klepněte na možnost <strong>Přidat podmínku</strong>.</span><span class="sxs-lookup"><span data-stu-id="3478b-287">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="3478b-288">Poté zadáním podmínky označte, kde v hierarchii má systém přestat načítat jména.</span><span class="sxs-lookup"><span data-stu-id="3478b-288">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="3478b-289">Na kartě <strong>Možnosti hierarchie</strong> zadejte uživatele v rozsahu, ke kterým by měl být rozhodnutí eskalováno:</span><span class="sxs-lookup"><span data-stu-id="3478b-289">On the <strong>Hierarchy options</strong> tab, specify which users in the range the decision should be escalated to:</span></span> <ul>
    <li><span data-ttu-id="3478b-290"><strong>Přiřadit všechny načtené uživatele</strong> – rozhodnutí dokument bude eskalováno všem uživatelům v rozsahu.</span><span class="sxs-lookup"><span data-stu-id="3478b-290"><strong>Assign to all users retrieved</strong> – The decision is escalated to all users in the range.</span></span></li>
    <li><span data-ttu-id="3478b-291"><strong>Přiřadit pouze poslednímu načtenému uživateli</strong> – rozhodnutí bude eskalováno pouze poslednímu uživateli v rozsahu.</span><span class="sxs-lookup"><span data-stu-id="3478b-291"><strong>Assign only to last user retrieved</strong> – The decision is escalated to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="3478b-292"><strong>Vyloučit uživatele splňující následující podmínku</strong> – rozhodnutí není eskalováno žádnému uživateli v rozsahu, který odpovídá konkrétní podmínce.</span><span class="sxs-lookup"><span data-stu-id="3478b-292"><strong>Exclude users with the following condition:</strong> – The decision isn't escalated to any users in the range who meet a specific condition.</span></span> <span data-ttu-id="3478b-293">Po klepnutí na volbu <strong>Přidat podmínku</strong> určete požadovanou podmínku.</span><span class="sxs-lookup"><span data-stu-id="3478b-293">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="3478b-294">Uživatel workflowu</span><span class="sxs-lookup"><span data-stu-id="3478b-294">Workflow user</span></span></td>
    <td><span data-ttu-id="3478b-295">Uživatelé v aktuálním workflowu</span><span class="sxs-lookup"><span data-stu-id="3478b-295">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="3478b-296">Po výběru možnosti <strong>Uživatel workflowu</strong> na kartě <strong>Uživatel workflowu</strong> v seznamu <strong>Uživatel workflowu</strong> vyberte uživatele, který se podílí na workflowu.</span><span class="sxs-lookup"><span data-stu-id="3478b-296">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="3478b-297">Uživatel</span><span class="sxs-lookup"><span data-stu-id="3478b-297">User</span></span></td>
    <td><span data-ttu-id="3478b-298">Konkrétní uživatelé</span><span class="sxs-lookup"><span data-stu-id="3478b-298">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="3478b-299">Po výběru možnosti <strong>Uživatel</strong> klepněte na kartu <strong>Uživatel</strong>.</span><span class="sxs-lookup"><span data-stu-id="3478b-299">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="3478b-300">Seznam <strong>Dostupní uživatelé</strong> obsahuje všechny uživatele.</span><span class="sxs-lookup"><span data-stu-id="3478b-300">The <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="3478b-301">Vyberte uživatele, ke kterým chcete rozhodnutí eskalovat, a pak přesuňte tyto uživatele do seznamu <strong>Vybraní uživatelé</strong>.</span><span class="sxs-lookup"><span data-stu-id="3478b-301">Select the users to escalate the decision to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

4. <span data-ttu-id="3478b-302">Na kartě **Časový limit** v poli **Trvání** určete, kolik času má uživatel na rozhodnutí.</span><span class="sxs-lookup"><span data-stu-id="3478b-302">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to make the decision.</span></span> <span data-ttu-id="3478b-303">Vyberte některou z následujících možností:</span><span class="sxs-lookup"><span data-stu-id="3478b-303">Select one of the following options:</span></span>

    - <span data-ttu-id="3478b-304">**Hodiny** – zadejte počet hodin, které má uživatel na rozhodnutí.</span><span class="sxs-lookup"><span data-stu-id="3478b-304">**Hours** – Enter the number of hours that the user has to make the decision.</span></span> <span data-ttu-id="3478b-305">Pak vyberte kalendář, který vaše organizace používá, a zadejte informace o pracovním týdnu vaší organizace.</span><span class="sxs-lookup"><span data-stu-id="3478b-305">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="3478b-306">**Dny** – zadejte počet dnů, které má uživatel na rozhodnutí.</span><span class="sxs-lookup"><span data-stu-id="3478b-306">**Days** – Enter the number of days that the user has to make the decision.</span></span> <span data-ttu-id="3478b-307">Pak vyberte kalendář, který vaše organizace používá, a zadejte informace o pracovním týdnu vaší organizace.</span><span class="sxs-lookup"><span data-stu-id="3478b-307">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="3478b-308">**Týdny** – zadejte počet týdnů, které má uživatel na rozhodnutí.</span><span class="sxs-lookup"><span data-stu-id="3478b-308">**Weeks** – Enter the number of weeks that the user has to make the decision.</span></span>
    - <span data-ttu-id="3478b-309">**Měsíce** – vyberte den a týden, do kdy se musí uživatel rozhodnout.</span><span class="sxs-lookup"><span data-stu-id="3478b-309">**Months** – Select the day and week that the user must make the decision by.</span></span> <span data-ttu-id="3478b-310">Můžete například požadovat, aby uživatel učinil rozhodnutí do třetího pátku v daném měsíci.</span><span class="sxs-lookup"><span data-stu-id="3478b-310">For example, you might want the user to make the decision by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="3478b-311">**Roky** – vyberte den, týden a měsíc, do kdy se musí uživatel rozhodnout.</span><span class="sxs-lookup"><span data-stu-id="3478b-311">**Years** – Select the day, week, and month that the user must make the decision by.</span></span> <span data-ttu-id="3478b-312">Můžete například požadovat, aby uživatel učinil rozhodnutí do třetího pátku v prosinci.</span><span class="sxs-lookup"><span data-stu-id="3478b-312">For example, you might want the user to make the decision by Friday of the third week of December.</span></span>

5. <span data-ttu-id="3478b-313">Zopakujte kroky 3 a 4 u každého uživatele, který má být přidán do eskalační cesty.</span><span class="sxs-lookup"><span data-stu-id="3478b-313">Repeat steps 3 through 4 for each user that should be added to the escalation path.</span></span> <span data-ttu-id="3478b-314">Pořadí uživatelů lze změnit.</span><span class="sxs-lookup"><span data-stu-id="3478b-314">You can change the order of the users.</span></span>
6. <span data-ttu-id="3478b-315">Pokud uživatelé v eskalační cestě v určeném čase rozhodnutí neučiní, systém sám provede rozhodnutí.</span><span class="sxs-lookup"><span data-stu-id="3478b-315">If the users in the escalation path don't make the decision in the allotted time, the system makes the decision.</span></span> <span data-ttu-id="3478b-316">Možnost, kterou systém vybere, můžete vybrat výběrem řádku **Akce** a na kartě **Konečná akce** vyberte možnost.</span><span class="sxs-lookup"><span data-stu-id="3478b-316">To specify the option that the system selects, select the **Action** row, and then, on the **End action** tab, select an option.</span></span>

## <a name="set-a-time-limit"></a><span data-ttu-id="3478b-317">Nastavení časového limitu</span><span class="sxs-lookup"><span data-stu-id="3478b-317">Set a time limit</span></span>

<span data-ttu-id="3478b-318">Tento postup použijte, pokud je rozhodnutí nutné učinit v určitém čase.</span><span class="sxs-lookup"><span data-stu-id="3478b-318">Follow these steps if the decision must be made in a specific time.</span></span>

> [!NOTE]
> <span data-ttu-id="3478b-319">Možnosti, které vyberete v rámci této procedury, přepíší možnosti vybrané v oblasti **Přiřazení** a **Eskalace** na stránce.</span><span class="sxs-lookup"><span data-stu-id="3478b-319">The options that you select in this procedure override the options that you selected in the **Assignment** and **Escalation** areas of the page.</span></span>

1. <span data-ttu-id="3478b-320">V levém podokně klepněte na tlačítko **Pokročilá nastavení**.</span><span class="sxs-lookup"><span data-stu-id="3478b-320">In the left pane, click **Advanced settings**.</span></span>
2. <span data-ttu-id="3478b-321">Označte pole **Nastavit časový limit pro prvek workflowu**.</span><span class="sxs-lookup"><span data-stu-id="3478b-321">Select the **Set a time limit for the workflow element** check box.</span></span>
3. <span data-ttu-id="3478b-322">V poli **Trvání** upřesněte, kdy má být rozhodnutí učiněno.</span><span class="sxs-lookup"><span data-stu-id="3478b-322">In the **Duration** field, specify when the decision must be made.</span></span> <span data-ttu-id="3478b-323">Vyberte některou z následujících možností:</span><span class="sxs-lookup"><span data-stu-id="3478b-323">Select one of the following options:</span></span>

    - <span data-ttu-id="3478b-324">**Hodiny** – zadejte počet hodin</span><span class="sxs-lookup"><span data-stu-id="3478b-324">**Hours** – Enter the number of hours.</span></span> <span data-ttu-id="3478b-325">Pak vyberte kalendář, který vaše organizace používá, a zadejte informace o pracovním týdnu vaší organizace.</span><span class="sxs-lookup"><span data-stu-id="3478b-325">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="3478b-326">**Dny** – zadejte počet dnů</span><span class="sxs-lookup"><span data-stu-id="3478b-326">**Days** – Enter the number of days.</span></span> <span data-ttu-id="3478b-327">Pak vyberte kalendář, který vaše organizace používá, a zadejte informace o pracovním týdnu vaší organizace.</span><span class="sxs-lookup"><span data-stu-id="3478b-327">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="3478b-328">**Týdny** – zadejte počet týdnů.</span><span class="sxs-lookup"><span data-stu-id="3478b-328">**Weeks** – Enter the number of weeks.</span></span>
    - <span data-ttu-id="3478b-329">**Měsíce** – vyberte den a týden, do kdy má být rozhodnutí učiněno.</span><span class="sxs-lookup"><span data-stu-id="3478b-329">**Months** – Select the day and week that the decision must be made by.</span></span> <span data-ttu-id="3478b-330">Můžete například požadovat, aby bylo rozhodnutí učiněno do třetího pátku v daném měsíci.</span><span class="sxs-lookup"><span data-stu-id="3478b-330">For example, you might want the decision to be made by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="3478b-331">**Roky** – vyberte den, týden a měsíc, do kdy má být rozhodnutí učiněno.</span><span class="sxs-lookup"><span data-stu-id="3478b-331">**Years** – Select the day, week, and month that the decision must be made by.</span></span> <span data-ttu-id="3478b-332">Můžete například požadovat, aby bylo rozhodnutí učiněno do třetího pátku v prosinci.</span><span class="sxs-lookup"><span data-stu-id="3478b-332">For example, you might want the decision to be made by Friday of the third week of December.</span></span>

4. <span data-ttu-id="3478b-333">Dojde-li k překročení časového limitu, systém učiní rozhodnutí.</span><span class="sxs-lookup"><span data-stu-id="3478b-333">If the time limit is exceeded, the system makes the decision.</span></span> <span data-ttu-id="3478b-334">V seznamu **Akce** vyberte možnost, která má být vybrána.</span><span class="sxs-lookup"><span data-stu-id="3478b-334">In the **Action** list, select the option that the system should select.</span></span>
