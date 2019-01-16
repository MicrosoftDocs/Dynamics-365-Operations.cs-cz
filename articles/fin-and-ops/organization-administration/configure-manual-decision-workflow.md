---
title: "Konfigurace ručních rozhodnutí ve workflow"
description: "Toto téma vysvětluje, jak nakonfigurovat vlastnosti ručního rozhodnutí."
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 192101
ms.assetid: 0bccad77-1a44-4f08-967b-12c62c02afc7
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 3ee5334c87b2b0acae2afa6882feca63e3b9cc8e
ms.openlocfilehash: d09e99a5bf99593a8fa7682f9d4f29eaa4e7c836
ms.contentlocale: cs-cz
ms.lasthandoff: 12/18/2018

---

# <a name="configure-manual-decisions-in-a-workflow"></a><span data-ttu-id="2db9f-103">Konfigurace ručních rozhodnutí ve workflow</span><span class="sxs-lookup"><span data-stu-id="2db9f-103">Configure manual decisions in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2db9f-104">Toto téma vysvětluje, jak nakonfigurovat vlastnosti ručního rozhodnutí.</span><span class="sxs-lookup"><span data-stu-id="2db9f-104">This topic explains how to configure the properties of a manual decision.</span></span>

<span data-ttu-id="2db9f-105">Pokud budete chtít nakonfigurovat ruční rozhodnutí v editoru workflowu, klikněte pravým tlačítkem myši na ruční rozhodnutí a kliknutím na tlačítko **Vlastnosti** otevřete stránku **Vlastnosti**.</span><span class="sxs-lookup"><span data-stu-id="2db9f-105">To configure a manual decision in the workflow editor, right-click the manual decision, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="2db9f-106">Následně nakonfigurujte vlastnosti dílčího workflowu pomocí ručního rozhodnutí.</span><span class="sxs-lookup"><span data-stu-id="2db9f-106">Then use the following procedures to configure the properties of the manual decision.</span></span>

## <a name="name-the-decision"></a><span data-ttu-id="2db9f-107">Název rozhodnutí</span><span class="sxs-lookup"><span data-stu-id="2db9f-107">Name the decision</span></span>

<span data-ttu-id="2db9f-108">Pomocí následujících kroků zadejte název ručního rozhodnutí.</span><span class="sxs-lookup"><span data-stu-id="2db9f-108">Follow these steps to enter a name for the manual decision.</span></span>

1. <span data-ttu-id="2db9f-109">V levém podokně klepněte na tlačítko **Základní nastavení**.</span><span class="sxs-lookup"><span data-stu-id="2db9f-109">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="2db9f-110">V poli **Název** zadejte jedinečný název ručního rozhodnutí.</span><span class="sxs-lookup"><span data-stu-id="2db9f-110">In the **Name** field, enter a unique name for the manual decision.</span></span>

## <a name="enter-a-subject-line-and-instructions"></a><span data-ttu-id="2db9f-111">Zadání řádku předmětu a pokynů</span><span class="sxs-lookup"><span data-stu-id="2db9f-111">Enter a subject line and instructions</span></span>

<span data-ttu-id="2db9f-112">Musíte zadat řádek předmětu a pokyny pro uživatele přiřazené k tomuto ručnímu rozhodnutí.</span><span class="sxs-lookup"><span data-stu-id="2db9f-112">You must provide a subject line and instructions to users who are assigned to the manual decision.</span></span> <span data-ttu-id="2db9f-113">Například pokud konfigurujete rozhodnutí pro nákupní požadavky, uživatel, který je k rozhodnutí přiřazeno, uvidí řádek s předmětem a pokyny na stránce **Nákupní žádanky**.</span><span class="sxs-lookup"><span data-stu-id="2db9f-113">For example, if you're configuring a decision for purchase requisitions, the user who is assigned to the decision sees the subject line and instructions on the **Purchase requisitions** page.</span></span> <span data-ttu-id="2db9f-114">Řádek předmětu se zobrazí na panelu zpráv na stránce.</span><span class="sxs-lookup"><span data-stu-id="2db9f-114">The subject line appears in a message bar on the page.</span></span> <span data-ttu-id="2db9f-115">Uživatel poté může kliknutím na ikonu na panelu zpráv zobrazit pokyny.</span><span class="sxs-lookup"><span data-stu-id="2db9f-115">The user can then click the icon in the message bar to view the instructions.</span></span> <span data-ttu-id="2db9f-116">K zadání řádku předmětu a pokynů použijte následující postup.</span><span class="sxs-lookup"><span data-stu-id="2db9f-116">Follow these steps to enter a subject line and instructions.</span></span>

1. <span data-ttu-id="2db9f-117">V levém podokně klepněte na tlačítko **Základní nastavení**.</span><span class="sxs-lookup"><span data-stu-id="2db9f-117">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="2db9f-118">Na kartě **Pokyny** v poli **Předmět pracovní položky** zadejte řádek předmětu.</span><span class="sxs-lookup"><span data-stu-id="2db9f-118">On the **Instructions** tab, in the **Work item subject** field, enter the subject line.</span></span>
3. <span data-ttu-id="2db9f-119">Řádek předmětu můžete přizpůsobit vložením zástupného textu.</span><span class="sxs-lookup"><span data-stu-id="2db9f-119">To personalize the subject line, you can insert placeholders.</span></span> <span data-ttu-id="2db9f-120">Zástupný text bude při zobrazení řádku předmětu uživatelům nahrazen odpovídacími daty.</span><span class="sxs-lookup"><span data-stu-id="2db9f-120">Placeholders are replaced with appropriate data when the subject line is shown to users.</span></span> <span data-ttu-id="2db9f-121">Při vkládání zástupného textu postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="2db9f-121">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="2db9f-122">V textovém poli klepnutím zadejte, kde se má zástupný text zobrazit.</span><span class="sxs-lookup"><span data-stu-id="2db9f-122">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="2db9f-123">Klikněte na **Vložit zástupný text**.</span><span class="sxs-lookup"><span data-stu-id="2db9f-123">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="2db9f-124">V nově otevřeném seznamu vyberte vkládaný zástupný text.</span><span class="sxs-lookup"><span data-stu-id="2db9f-124">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="2db9f-125">Klepněte na tlačítko **Vložit**.</span><span class="sxs-lookup"><span data-stu-id="2db9f-125">Click **Insert**.</span></span>

4. <span data-ttu-id="2db9f-126">Chcete-li přidat překlady řádku předmětu, postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="2db9f-126">To add translations of the subject line, follow these steps:</span></span>

    1. <span data-ttu-id="2db9f-127">Klikněte na **Překlady**.</span><span class="sxs-lookup"><span data-stu-id="2db9f-127">Click **Translations**.</span></span>
    2. <span data-ttu-id="2db9f-128">Na nově otevřené stránce klikněte na **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="2db9f-128">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="2db9f-129">V nově otevřeném seznamu vyberte jazyk, který chcete použít pro zadání textu.</span><span class="sxs-lookup"><span data-stu-id="2db9f-129">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="2db9f-130">V poli **Přeložený text** zadejte text.</span><span class="sxs-lookup"><span data-stu-id="2db9f-130">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="2db9f-131">Text můžete přizpůsobit vložením zástupného textu podle pokynů v kroku 3.</span><span class="sxs-lookup"><span data-stu-id="2db9f-131">To personalize the text, you can insert placeholders as described in step 3.</span></span>
    6. <span data-ttu-id="2db9f-132">Klepněte na tlačítko **Zavřít**.</span><span class="sxs-lookup"><span data-stu-id="2db9f-132">Click **Close**.</span></span>

5. <span data-ttu-id="2db9f-133">V poli **Pokyny pracovní položky** zadejte pokyny.</span><span class="sxs-lookup"><span data-stu-id="2db9f-133">In the **Work item instructions** field, enter the instructions.</span></span>
6. <span data-ttu-id="2db9f-134">Pokyny můžete přizpůsobit vložením zástupného textu.</span><span class="sxs-lookup"><span data-stu-id="2db9f-134">To personalize the instructions, you can insert placeholders.</span></span> <span data-ttu-id="2db9f-135">Zástupný text bude při zobrazení pokynů uživatelům nahrazen odpovídacími daty.</span><span class="sxs-lookup"><span data-stu-id="2db9f-135">Placeholders are replaced with appropriate data when the instructions are shown to users.</span></span> <span data-ttu-id="2db9f-136">Při vkládání zástupného textu postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="2db9f-136">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="2db9f-137">V textovém poli klepnutím zadejte, kde se má zástupný text zobrazit.</span><span class="sxs-lookup"><span data-stu-id="2db9f-137">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="2db9f-138">Klikněte na **Vložit zástupný text**.</span><span class="sxs-lookup"><span data-stu-id="2db9f-138">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="2db9f-139">V nově otevřeném seznamu vyberte vkládaný zástupný text.</span><span class="sxs-lookup"><span data-stu-id="2db9f-139">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="2db9f-140">Klepněte na tlačítko **Vložit**.</span><span class="sxs-lookup"><span data-stu-id="2db9f-140">Click **Insert**.</span></span>

7. <span data-ttu-id="2db9f-141">Chcete-li přidat překlady pokynů, postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="2db9f-141">To add translations of the instructions, follow these steps:</span></span>

    1. <span data-ttu-id="2db9f-142">Klikněte na **Překlady**.</span><span class="sxs-lookup"><span data-stu-id="2db9f-142">Click **Translations**.</span></span>
    2. <span data-ttu-id="2db9f-143">Na nově otevřené stránce klikněte na **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="2db9f-143">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="2db9f-144">V nově otevřeném seznamu vyberte jazyk, který chcete použít pro zadání textu.</span><span class="sxs-lookup"><span data-stu-id="2db9f-144">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="2db9f-145">V poli **Přeložený text** zadejte text.</span><span class="sxs-lookup"><span data-stu-id="2db9f-145">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="2db9f-146">Text můžete přizpůsobit vložením zástupného textu podle pokynů v kroku 6.</span><span class="sxs-lookup"><span data-stu-id="2db9f-146">To personalize the text, you can insert placeholders as described in step 6.</span></span>
    6. <span data-ttu-id="2db9f-147">Klepněte na tlačítko **Zavřít**.</span><span class="sxs-lookup"><span data-stu-id="2db9f-147">Click **Close**.</span></span>

## <a name="specify-the-possible-outcomes-of-a-decision"></a><span data-ttu-id="2db9f-148">Určete možné výsledky rozhodnutí</span><span class="sxs-lookup"><span data-stu-id="2db9f-148">Specify the possible outcomes of a decision</span></span>

<span data-ttu-id="2db9f-149">obvykle pokud je dokument přiřazen pracovníkovi s rozhodovací pravomocí, je tomuto pracovníkovi kladena otázka.</span><span class="sxs-lookup"><span data-stu-id="2db9f-149">Typically, when a document is assigned to a decision maker, the decision maker is asked a question.</span></span> <span data-ttu-id="2db9f-150">Na tuto otázku se obvykle odpovídá možnostmi **Ano** nebo **Ne**, nebo **Pravda** nebo **Nepravda**.</span><span class="sxs-lookup"><span data-stu-id="2db9f-150">The answer to this question is usually **Yes** or **No**, or **True** or **False**.</span></span> <span data-ttu-id="2db9f-151">Podle následujících kroků můžete určit možné výsledky ručního rozhodnutí.</span><span class="sxs-lookup"><span data-stu-id="2db9f-151">Follow these steps to specify the possible outcomes of the manual decision.</span></span>

1. <span data-ttu-id="2db9f-152">V levém podokně klepněte na tlačítko **Základní nastavení**.</span><span class="sxs-lookup"><span data-stu-id="2db9f-152">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="2db9f-153">Na kartě **Výsledky** v poli **Výsledek 1** zadejte název výsledku nebo možnost.</span><span class="sxs-lookup"><span data-stu-id="2db9f-153">On the **Outcomes** tab, in the **Outcome 1** field, enter the name of the outcome, or the option.</span></span>
3. <span data-ttu-id="2db9f-154">Chcete-li přidat překlady výsledků, postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="2db9f-154">To add translations of the outcome, follow these steps:</span></span>

    1. <span data-ttu-id="2db9f-155">Klikněte na **Překlady**.</span><span class="sxs-lookup"><span data-stu-id="2db9f-155">Click **Translations**.</span></span>
    2. <span data-ttu-id="2db9f-156">Na nově otevřené stránce klikněte na **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="2db9f-156">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="2db9f-157">V nově otevřeném seznamu vyberte jazyk, který chcete použít pro zadání textu.</span><span class="sxs-lookup"><span data-stu-id="2db9f-157">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="2db9f-158">V poli **Přeložený text** zadejte text.</span><span class="sxs-lookup"><span data-stu-id="2db9f-158">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="2db9f-159">Klepněte na tlačítko **Zavřít**.</span><span class="sxs-lookup"><span data-stu-id="2db9f-159">Click **Close**.</span></span>

4. <span data-ttu-id="2db9f-160">V poli **Výsledek 2** zadejte název výsledku nebo možnost.</span><span class="sxs-lookup"><span data-stu-id="2db9f-160">In the **Outcome 2** field, enter the name of the outcome, or the option.</span></span>
5. <span data-ttu-id="2db9f-161">Chcete-li přidat překlady výsledků, postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="2db9f-161">To add translations of the outcome, follow these steps:</span></span>

    1. <span data-ttu-id="2db9f-162">Klikněte na **Překlady**.</span><span class="sxs-lookup"><span data-stu-id="2db9f-162">Click **Translations**.</span></span>
    2. <span data-ttu-id="2db9f-163">Na nově otevřené stránce klikněte na **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="2db9f-163">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="2db9f-164">V nově otevřeném seznamu vyberte jazyk, který chcete použít pro zadání textu.</span><span class="sxs-lookup"><span data-stu-id="2db9f-164">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="2db9f-165">V poli **Přeložený text** zadejte text.</span><span class="sxs-lookup"><span data-stu-id="2db9f-165">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="2db9f-166">Klepněte na tlačítko **Zavřít**.</span><span class="sxs-lookup"><span data-stu-id="2db9f-166">Click **Close**.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="2db9f-167">Zadejte, kdy se mají odesílat oznámení.</span><span class="sxs-lookup"><span data-stu-id="2db9f-167">Specify when notifications are sent</span></span>

<span data-ttu-id="2db9f-168">Můžete odeslat oznámení uživatelům, jakmile bude rozhodnutí provedeno, delegováno nebo eskalováno.</span><span class="sxs-lookup"><span data-stu-id="2db9f-168">You can send notifications to people when a decision has been made, delegated, or escalated.</span></span> <span data-ttu-id="2db9f-169">Podle těchto kroků můžete určit oznámení, které se odešle, a osoby, kterým se odešle.</span><span class="sxs-lookup"><span data-stu-id="2db9f-169">Follow these steps to specify when notifications are sent, and who the notifications are sent to.</span></span>

1. <span data-ttu-id="2db9f-170">V levém podokně klikněte na **Oznámení**.</span><span class="sxs-lookup"><span data-stu-id="2db9f-170">In the left pane, click **Notifications**.</span></span>
2. <span data-ttu-id="2db9f-171">Označte pole vedle událostí, při kterých se oznámení odešle:</span><span class="sxs-lookup"><span data-stu-id="2db9f-171">Select the check box next to the events that notifications should be sent for:</span></span>

    - <span data-ttu-id="2db9f-172">**\[Volba 1\]** – přiřazený uživatel vybral možnost **\[Volba 1\]**.</span><span class="sxs-lookup"><span data-stu-id="2db9f-172">**\[Choice 1\]** – The assigned user has selected **\[Choice 1\]**.</span></span>
    - <span data-ttu-id="2db9f-173">**\[Volba 2\]** – přiřazený uživatel vybral možnost **\[Volba 2\]**.</span><span class="sxs-lookup"><span data-stu-id="2db9f-173">**\[Choice 2\]** – The assigned user has selected **\[Choice 2\]**.</span></span>
    - <span data-ttu-id="2db9f-174">**Delegovat** – přiřazený uživatel přiřadil rozhodnutí jinému uživateli.</span><span class="sxs-lookup"><span data-stu-id="2db9f-174">**Delegate** – The assigned user has assigned the decision to another user.</span></span>
    - <span data-ttu-id="2db9f-175">**Eskalovat** – přiřazený uživatel neučinil rozhodnutí v přiděleném čase.</span><span class="sxs-lookup"><span data-stu-id="2db9f-175">**Escalate** – The assigned user hasn't made the decision in the allotted time.</span></span>

3. <span data-ttu-id="2db9f-176">Vyberte řádek pro událost, kterou jste vybrali v kroku 2.</span><span class="sxs-lookup"><span data-stu-id="2db9f-176">Select the row for an event that you selected in step 2.</span></span>
4. <span data-ttu-id="2db9f-177">Na kartě **Text oznámení** zadejte v textovém poli text oznámení.</span><span class="sxs-lookup"><span data-stu-id="2db9f-177">On the **Notification text** tab, in the text box, enter the text of the notification.</span></span>
5. <span data-ttu-id="2db9f-178">Oznámení můžete přizpůsobit vložením zástupného textu.</span><span class="sxs-lookup"><span data-stu-id="2db9f-178">To personalize the notification, you can insert placeholders.</span></span> <span data-ttu-id="2db9f-179">Zástupný text bude při zobrazení oznámení uživatelům nahrazen odpovídacími daty.</span><span class="sxs-lookup"><span data-stu-id="2db9f-179">Placeholders are replaced with appropriate data when the notification is show to users.</span></span> <span data-ttu-id="2db9f-180">Při vkládání zástupného textu postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="2db9f-180">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="2db9f-181">V textovém poli klepnutím zadejte, kde se má zástupný text zobrazit.</span><span class="sxs-lookup"><span data-stu-id="2db9f-181">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="2db9f-182">Klikněte na **Vložit zástupný text**.</span><span class="sxs-lookup"><span data-stu-id="2db9f-182">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="2db9f-183">V nově otevřeném seznamu vyberte vkládaný zástupný text.</span><span class="sxs-lookup"><span data-stu-id="2db9f-183">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="2db9f-184">Klepněte na tlačítko **Vložit**.</span><span class="sxs-lookup"><span data-stu-id="2db9f-184">Click **Insert**.</span></span>

6. <span data-ttu-id="2db9f-185">Chcete-li přidat překlady oznámení, postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="2db9f-185">To add translations of the notification, follow these steps:</span></span>

    1. <span data-ttu-id="2db9f-186">Klikněte na **Překlady**.</span><span class="sxs-lookup"><span data-stu-id="2db9f-186">Click **Translations**.</span></span>
    2. <span data-ttu-id="2db9f-187">Na nově otevřené stránce klikněte na **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="2db9f-187">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="2db9f-188">V nově otevřeném seznamu vyberte jazyk, který chcete použít pro zadání textu.</span><span class="sxs-lookup"><span data-stu-id="2db9f-188">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="2db9f-189">V poli **Přeložený text** zadejte text.</span><span class="sxs-lookup"><span data-stu-id="2db9f-189">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="2db9f-190">Text můžete přizpůsobit vložením zástupného textu podle pokynů v kroku 5.</span><span class="sxs-lookup"><span data-stu-id="2db9f-190">To personalize the text, you can insert placeholders as described in step 5.</span></span>
    6. <span data-ttu-id="2db9f-191">Klepněte na tlačítko **Zavřít**.</span><span class="sxs-lookup"><span data-stu-id="2db9f-191">Click **Close**.</span></span>

7. <span data-ttu-id="2db9f-192">Na kartě **Příjemce** zadejte osoby, kterým budou upozornění odesílána.</span><span class="sxs-lookup"><span data-stu-id="2db9f-192">On the **Recipient** tab, specify who the notifications are sent to.</span></span> <span data-ttu-id="2db9f-193">Vyberte jednu z možností v následující tabulce a před přechodem na krok 8 postupujte podle dalších kroků pro tuto možnost.</span><span class="sxs-lookup"><span data-stu-id="2db9f-193">Select one of the options in the following table, and then follow the additional steps for that option before you go to step 8.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="2db9f-194">Možnost</span><span class="sxs-lookup"><span data-stu-id="2db9f-194">Option</span></span></th>
    <th><span data-ttu-id="2db9f-195">Příjemce oznámení</span><span class="sxs-lookup"><span data-stu-id="2db9f-195">Notification recipients</span></span></th>
    <th><span data-ttu-id="2db9f-196">Další kroky</span><span class="sxs-lookup"><span data-stu-id="2db9f-196">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="2db9f-197">Účastník</span><span class="sxs-lookup"><span data-stu-id="2db9f-197">Participant</span></span></td>
    <td><span data-ttu-id="2db9f-198">Uživatelé, kteří jsou přiřazeni k určité skupině nebo roli</span><span class="sxs-lookup"><span data-stu-id="2db9f-198">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="2db9f-199">Po výběru možnosti <strong>Účastník</strong> na kartě <strong>Založeno na roli</strong> v seznamu <strong>Typ účastníka</strong> vyberte typ skupiny nebo role, které chcete oznámení odeslat.</span><span class="sxs-lookup"><span data-stu-id="2db9f-199">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="2db9f-200">V seznamu <strong>Účastník</strong> vyberte skupinu, které chcete oznámení odeslat.</span><span class="sxs-lookup"><span data-stu-id="2db9f-200">In the <strong>Participant</strong> list, select the group or to send notifications to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="2db9f-201">Uživatel workflowu</span><span class="sxs-lookup"><span data-stu-id="2db9f-201">Workflow user</span></span></td>
    <td><span data-ttu-id="2db9f-202">Uživatelé v aktuálním workflowu</span><span class="sxs-lookup"><span data-stu-id="2db9f-202">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="2db9f-203">Po výběru možnosti <strong>Uživatel workflowu</strong> na kartě <strong>Uživatel workflowu</strong> v seznamu <strong>Uživatel workflowu</strong> vyberte uživatele, který se podílí na workflowu.</span><span class="sxs-lookup"><span data-stu-id="2db9f-203">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="2db9f-204">Uživatel</span><span class="sxs-lookup"><span data-stu-id="2db9f-204">User</span></span></td>
    <td><span data-ttu-id="2db9f-205">Konkrétní uživatelé aplikace Microsoft Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="2db9f-205">Specific Microsoft Dynamics 365 for Finance and Operations users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="2db9f-206">Po výběru možnosti <strong>Uživatel</strong> klepněte na kartu <strong>Uživatel</strong>.</span><span class="sxs-lookup"><span data-stu-id="2db9f-206">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="2db9f-207">Seznam <strong>Dostupní uživatelé</strong> obsahuje všechny uživatele aplikace Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="2db9f-207">The <strong>Available users</strong> list includes all Finance and Operations users.</span></span> <span data-ttu-id="2db9f-208">Vyberte uživatele, kterým chcete odeslat oznámení, a pak přesuňte tyto uživatele do seznamu <strong>Vybraní uživatelé</strong>.</span><span class="sxs-lookup"><span data-stu-id="2db9f-208">Select the users to send notifications to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

8. <span data-ttu-id="2db9f-209">Zopakujte kroky 3 až 7 pro každou událost, kterou jste vybrali v kroku 2.</span><span class="sxs-lookup"><span data-stu-id="2db9f-209">Repeat steps 3 through 7 for each event that you selected in step 2.</span></span>

## <a name="assign-a-decision"></a><span data-ttu-id="2db9f-210">Přiřazení rozhodnutí</span><span class="sxs-lookup"><span data-stu-id="2db9f-210">Assign a decision</span></span>

<span data-ttu-id="2db9f-211">Pomocí následujícího postupu určíte, komu má být ruční rozhodnutí přiřazeno.</span><span class="sxs-lookup"><span data-stu-id="2db9f-211">Follow these steps to specify who a manual decision should be assigned to.</span></span>

1. <span data-ttu-id="2db9f-212">V levém podokně klikněte na **Přiřazení**.</span><span class="sxs-lookup"><span data-stu-id="2db9f-212">In the left pane, click **Assignment**.</span></span>
2. <span data-ttu-id="2db9f-213">Na kartě **Typ přiřazení** vyberte jednu z možností v následující tabulce a před přechodem na krok 3 postupujte podle dalších kroků pro tuto možnost.</span><span class="sxs-lookup"><span data-stu-id="2db9f-213">On the **Assignment type** tab, select one of the options in the following table, and then follow the additional steps for that option before you go to step 3.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="2db9f-214">Možnost</span><span class="sxs-lookup"><span data-stu-id="2db9f-214">Option</span></span></th>
    <th><span data-ttu-id="2db9f-215">Uživatelé, kterým je rozhodnutí přiřazeno</span><span class="sxs-lookup"><span data-stu-id="2db9f-215">Users that the decision is assigned to</span></span></th>
    <th><span data-ttu-id="2db9f-216">Další kroky</span><span class="sxs-lookup"><span data-stu-id="2db9f-216">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="2db9f-217">Účastník</span><span class="sxs-lookup"><span data-stu-id="2db9f-217">Participant</span></span></td>
    <td><span data-ttu-id="2db9f-218">Uživatelé, kteří jsou přiřazeni k určité skupině nebo roli</span><span class="sxs-lookup"><span data-stu-id="2db9f-218">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="2db9f-219">Po výběru možnosti <strong>Účastník</strong> na kartě <strong>Založeno na roli</strong> v seznamu <strong>Typ účastníka</strong> vyberte typ skupiny nebo role, které chcete rozhodnutí přiřadit.</span><span class="sxs-lookup"><span data-stu-id="2db9f-219">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to assign the decision to.</span></span></li>
    <li><span data-ttu-id="2db9f-220">V seznamu <strong>Účastník</strong> vyberte skupinu nebo roli, které chcete rozhodnutí přiřadit.</span><span class="sxs-lookup"><span data-stu-id="2db9f-220">In the <strong>Participant</strong> list, select the group or role to assign the decision to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="2db9f-221">Hierarchie</span><span class="sxs-lookup"><span data-stu-id="2db9f-221">Hierarchy</span></span></td>
    <td><span data-ttu-id="2db9f-222">Uživatelé v určité organizační hierarchii</span><span class="sxs-lookup"><span data-stu-id="2db9f-222">Users in a specific organizational hierarchy</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="2db9f-223">Po výběru možnosti <strong>Hierarchie</strong> na kartě <strong>Výběr hierarchie</strong> v seznamu <strong>Typ hierarchie</strong> vyberte typ hierarchie, které chcete rozhodnutí přiřadit.</span><span class="sxs-lookup"><span data-stu-id="2db9f-223">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to assign the decision to.</span></span></li>
    <li><span data-ttu-id="2db9f-224">Systém musí z hierarchie načíst rozsah jmen uživatelů.</span><span class="sxs-lookup"><span data-stu-id="2db9f-224">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="2db9f-225">Tato jména představují uživatele, kterým může být rozhodnutí přiřazen.</span><span class="sxs-lookup"><span data-stu-id="2db9f-225">These names represent users that the decision can be assigned to.</span></span> <span data-ttu-id="2db9f-226">Podle těchto kroků určete počáteční a koncový bod rozsahu uživatelských jmen, které systém obdrží:</span><span class="sxs-lookup"><span data-stu-id="2db9f-226">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="2db9f-227">Chcete-li zadat počáteční bod, vyberte osobu v seznamu <strong>Začátek od</strong>.</span><span class="sxs-lookup"><span data-stu-id="2db9f-227">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="2db9f-228">Chcete-li zadat koncový bod, klepněte na možnost <strong>Přidat podmínku</strong>.</span><span class="sxs-lookup"><span data-stu-id="2db9f-228">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="2db9f-229">Poté zadáním podmínky označte, kde v hierarchii má systém přestat načítat jména.</span><span class="sxs-lookup"><span data-stu-id="2db9f-229">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="2db9f-230">Na kartě <strong>Možnosti hierarchie</strong> zadejte uživatele v rozsahu, kterým by měl být rozhodnutí přiřazeno:</span><span class="sxs-lookup"><span data-stu-id="2db9f-230">On the <strong>Hierarchy options</strong> tab, specify which users in the range the decision should be assigned to:</span></span> <ul>
    <li><span data-ttu-id="2db9f-231"><strong>Přiřadit všechny načtené uživatele</strong> – rozhodnutí bude přiřazeno všem uživatelům v rozsahu.</span><span class="sxs-lookup"><span data-stu-id="2db9f-231"><strong>Assign to all users retrieved</strong> – The decision is assigned to all users in the range.</span></span></li>
    <li><span data-ttu-id="2db9f-232"><strong>Přiřadit pouze poslednímu načtenému uživateli</strong> – rozhodnutí bude přiřazeno pouze poslednímu uživateli v rozsahu.</span><span class="sxs-lookup"><span data-stu-id="2db9f-232"><strong>Assign only to last user retrieved</strong> – The decision is assigned to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="2db9f-233"><strong>Vyloučit uživatele splňující následující podmínku</strong> – rozhodnutí není přiřazeno žádnému uživateli v rozsahu, který odpovídá konkrétní podmínce.</span><span class="sxs-lookup"><span data-stu-id="2db9f-233"><strong>Exclude users with the following condition</strong> – The decision isn't assigned to any users in the range who meet a specific condition.</span></span> <span data-ttu-id="2db9f-234">Po klepnutí na volbu <strong>Přidat podmínku</strong> určete požadovanou podmínku.</span><span class="sxs-lookup"><span data-stu-id="2db9f-234">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="2db9f-235">Uživatel workflowu</span><span class="sxs-lookup"><span data-stu-id="2db9f-235">Workflow user</span></span></td>
    <td><span data-ttu-id="2db9f-236">Uživatelé v aktuálním workflowu</span><span class="sxs-lookup"><span data-stu-id="2db9f-236">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="2db9f-237">Po výběru možnosti <strong>Uživatel workflowu</strong> na kartě <strong>Uživatel workflowu</strong> v seznamu <strong>Uživatel workflowu</strong> vyberte uživatele, který se podílí na workflowu.</span><span class="sxs-lookup"><span data-stu-id="2db9f-237">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="2db9f-238">Uživatel</span><span class="sxs-lookup"><span data-stu-id="2db9f-238">User</span></span></td>
    <td><span data-ttu-id="2db9f-239">Konkrétní uživatelé aplikace Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="2db9f-239">Specific Finance and Operations users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="2db9f-240">Po výběru možnosti <strong>Uživatel</strong> klepněte na kartu <strong>Uživatel</strong>.</span><span class="sxs-lookup"><span data-stu-id="2db9f-240">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="2db9f-241">Seznam <strong>Dostupní uživatelé</strong> obsahuje všechny uživatele aplikace Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="2db9f-241">The <strong>Available users</strong> list includes all Finance and Operations users.</span></span> <span data-ttu-id="2db9f-242">Vyberte uživatele, kterým chcete rozhodnutí přiřadit, a pak přesuňte tyto uživatele do seznamu <strong>Vybraní uživatelé</strong>.</span><span class="sxs-lookup"><span data-stu-id="2db9f-242">Select the users to assign the decision to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="2db9f-243">Fronta</span><span class="sxs-lookup"><span data-stu-id="2db9f-243">Queue</span></span></td>
    <td><span data-ttu-id="2db9f-244">Fronta pracovních položek</span><span class="sxs-lookup"><span data-stu-id="2db9f-244">A work item queue</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="2db9f-245">Po výběru možnosti <strong>Fronta</strong> klepněte na kartu <strong>Založeno na frontě</strong>.</span><span class="sxs-lookup"><span data-stu-id="2db9f-245">After you select <strong>Queue</strong>, click the <strong>Queue based</strong> tab.</span></span></li>
    <li><span data-ttu-id="2db9f-246">Chcete-li přiřadit rozhodnutí konkrétní frontě, postupujte následujícím způsobem:</span><span class="sxs-lookup"><span data-stu-id="2db9f-246">To assign the decision to a specific queue, follow these steps:</span></span> <ol>
    <li><span data-ttu-id="2db9f-247">V seznamu <strong>Typ fronty</strong> vyberte <strong>Fronty pracovních položek</strong>.</span><span class="sxs-lookup"><span data-stu-id="2db9f-247">In the <strong>Queue type</strong> list, select <strong>Work item queues</strong>.</span></span></li>
    <li><span data-ttu-id="2db9f-248">V seznamu <strong>Název fronty</strong> vyberte frontu.</span><span class="sxs-lookup"><span data-stu-id="2db9f-248">In the <strong>Queue name</strong> list, select the queue.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="2db9f-249">Pokud by konkrétní podmínka měla určit frontu, které bude rozhodnutí přiřazeno, postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="2db9f-249">If a specific condition should determine which queue the decision is assigned to, follow these steps:</span></span> <ol>
    <li><span data-ttu-id="2db9f-250">V seznamu <strong>Typ fronty</strong> vyberte <strong>Podmíněné fronty pracovních položek</strong>.</span><span class="sxs-lookup"><span data-stu-id="2db9f-250">In the <strong>Queue type</strong> list, select <strong>Conditional work item queues</strong>.</span></span></li>
    <li><span data-ttu-id="2db9f-251">V seznamu <strong>Název fronty</strong> vyberte <strong>Podmíněná fronta</strong>.</span><span class="sxs-lookup"><span data-stu-id="2db9f-251">In the <strong>Queue name</strong> list, select <strong>Conditional queue</strong>.</span></span></li>
    </ol>
    </li>
    </ol>
    <blockquote>[!NOTE] <span data-ttu-id="2db9f-252">Tato možnost se používá pouze u několika workflowů, jako je například správa případů.</span><span class="sxs-lookup"><span data-stu-id="2db9f-252">This option is used for only a few workflows, such as Case management.</span></span></blockquote>
    </td>
    </tr>
    </tbody>
    </table>

3. <span data-ttu-id="2db9f-253">Na kartě **Časový limit** v poli **Trvání** určete, kolik času má uživatel na rozhodnutí.</span><span class="sxs-lookup"><span data-stu-id="2db9f-253">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to make the decision.</span></span> <span data-ttu-id="2db9f-254">Vyberte některou z následujících možností:</span><span class="sxs-lookup"><span data-stu-id="2db9f-254">Select one of the following options:</span></span>

    - <span data-ttu-id="2db9f-255">**Hodiny** – zadejte počet hodin, které má uživatel na rozhodnutí.</span><span class="sxs-lookup"><span data-stu-id="2db9f-255">**Hours** – Enter the number of hours that the user has to make the decision.</span></span> <span data-ttu-id="2db9f-256">Pak vyberte kalendář, který vaše organizace používá, a zadejte informace o pracovním týdnu vaší organizace.</span><span class="sxs-lookup"><span data-stu-id="2db9f-256">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="2db9f-257">**Dny** – zadejte počet dnů, které má uživatel na rozhodnutí.</span><span class="sxs-lookup"><span data-stu-id="2db9f-257">**Days** – Enter the number of days that the user has to make the decision.</span></span> <span data-ttu-id="2db9f-258">Pak vyberte kalendář, který vaše organizace používá, a zadejte informace o pracovním týdnu vaší organizace.</span><span class="sxs-lookup"><span data-stu-id="2db9f-258">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="2db9f-259">**Týdny** – zadejte počet týdnů, které má uživatel na rozhodnutí.</span><span class="sxs-lookup"><span data-stu-id="2db9f-259">**Weeks** – Enter the number of weeks that the user has to make the decision.</span></span>
    - <span data-ttu-id="2db9f-260">**Měsíce** – vyberte den a týden, do kdy se musí uživatel rozhodnout.</span><span class="sxs-lookup"><span data-stu-id="2db9f-260">**Months** – Select the day and week that the user must make the decision by.</span></span> <span data-ttu-id="2db9f-261">Můžete například požadovat, aby uživatel učinil rozhodnutí do třetího pátku v daném měsíci.</span><span class="sxs-lookup"><span data-stu-id="2db9f-261">For example, you might want the user to make the decision by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="2db9f-262">**Roky** – vyberte den, týden a měsíc, do kdy se musí uživatel rozhodnout.</span><span class="sxs-lookup"><span data-stu-id="2db9f-262">**Years** – Select the day, week, and month that the user must make the decision by.</span></span> <span data-ttu-id="2db9f-263">Můžete například požadovat, aby uživatel učinil rozhodnutí do třetího pátku v prosinci.</span><span class="sxs-lookup"><span data-stu-id="2db9f-263">For example, you might want the user to make the decision by Friday of the third week of December.</span></span>

    <span data-ttu-id="2db9f-264">Pokud uživatel v přiděleném čase rozhodnutí neučiní, rozhodnutí bude v prodlení.</span><span class="sxs-lookup"><span data-stu-id="2db9f-264">If the user doesn't make the decision in the allotted time, the decision is overdue.</span></span> <span data-ttu-id="2db9f-265">Rozhodnutí v prodlení je eskalován na základě možností vybraných v oblasti stránky **Eskalace**.</span><span class="sxs-lookup"><span data-stu-id="2db9f-265">A decision that is overdue is escalated, based on the options that you select in the **Escalation** area of the page.</span></span>

## <a name="specify-what-happens-when-a-decision-is-overdue"></a><span data-ttu-id="2db9f-266">Určení akce prováděné při zpoždění rozhodnutí</span><span class="sxs-lookup"><span data-stu-id="2db9f-266">Specify what happens when a decision is overdue</span></span>

<span data-ttu-id="2db9f-267">Pokud uživatel v přiděleném čase rozhodnutí neučiní, rozhodnutí bude v prodlení.</span><span class="sxs-lookup"><span data-stu-id="2db9f-267">If a user doesn't make the decision in the allotted time, the decision is overdue.</span></span> <span data-ttu-id="2db9f-268">Rozhodnutí, které je v prodlení, může být eskalováno nebo automaticky přiřazeno jinému uživateli.</span><span class="sxs-lookup"><span data-stu-id="2db9f-268">A decision that is overdue can be escalated, or automatically assigned to another user.</span></span> <span data-ttu-id="2db9f-269">Pro eskalování rozhodnutí v prodlení postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="2db9f-269">Follow these steps to escalate the decision if it's overdue.</span></span>

1. <span data-ttu-id="2db9f-270">V levém podokně klikněte na **Eskalování**.</span><span class="sxs-lookup"><span data-stu-id="2db9f-270">In the left pane, click **Escalation**.</span></span>
2. <span data-ttu-id="2db9f-271">Označte pole **Použít eskalační cestu** a vytvořte tak eskalační cestu.</span><span class="sxs-lookup"><span data-stu-id="2db9f-271">Select the **Use escalation path** check box to create an escalation path.</span></span> <span data-ttu-id="2db9f-272">Systém automaticky přiřadí dané rozhodnutí uživatelům uvedeným v cestě eskalace.</span><span class="sxs-lookup"><span data-stu-id="2db9f-272">The system automatically assigns the decision to the users who are listed in the escalation path.</span></span> <span data-ttu-id="2db9f-273">Například v následující tabulce naleznete příklad eskalační cesty.</span><span class="sxs-lookup"><span data-stu-id="2db9f-273">For example, the following table represents an escalation path.</span></span>

    | <span data-ttu-id="2db9f-274">Pořadí</span><span class="sxs-lookup"><span data-stu-id="2db9f-274">Sequence</span></span> | <span data-ttu-id="2db9f-275">Eskalační cesta</span><span class="sxs-lookup"><span data-stu-id="2db9f-275">Escalation path</span></span>            |
    |----------|----------------------------|
    | <span data-ttu-id="2db9f-276">1</span><span class="sxs-lookup"><span data-stu-id="2db9f-276">1</span></span>        | <span data-ttu-id="2db9f-277">Přiřadit k: Donna</span><span class="sxs-lookup"><span data-stu-id="2db9f-277">Assign to: Donna</span></span>           |
    | <span data-ttu-id="2db9f-278">2</span><span class="sxs-lookup"><span data-stu-id="2db9f-278">2</span></span>        | <span data-ttu-id="2db9f-279">Přiřadit k: Erin</span><span class="sxs-lookup"><span data-stu-id="2db9f-279">Assign to: Erin</span></span>            |
    | <span data-ttu-id="2db9f-280">3</span><span class="sxs-lookup"><span data-stu-id="2db9f-280">3</span></span>        | <span data-ttu-id="2db9f-281">Konečná akce: \[Volba 1\]</span><span class="sxs-lookup"><span data-stu-id="2db9f-281">Final action: \[Choice 1\]</span></span> |

    <span data-ttu-id="2db9f-282">V tomto příkladu systém přiřadí zpožděné rozhodnutí Donně.</span><span class="sxs-lookup"><span data-stu-id="2db9f-282">In this example, the system assigns the overdue decision to Donna.</span></span> <span data-ttu-id="2db9f-283">Pokud Donna v určeném čase rozhodnutí neučiní, systém přiřadí rozhodnutí Erin.</span><span class="sxs-lookup"><span data-stu-id="2db9f-283">If Donna doesn't make the decision in the allotted time, the system assigns the decision to Erin.</span></span> <span data-ttu-id="2db9f-284">Pokud Erin v určeném čase rozhodnutí neučiní, systém jako rozhodnutí vybere možnost **\[Volba 1\]**.</span><span class="sxs-lookup"><span data-stu-id="2db9f-284">If Erin doesn't make the decision in the allotted time, the system selects **\[Choice 1\]** as the decision.</span></span>

3. <span data-ttu-id="2db9f-285">Pokud chcete přidat uživatele do eskalační cesty, klepněte na tlačítko **Přidat eskalaci**.</span><span class="sxs-lookup"><span data-stu-id="2db9f-285">To add a user to the escalation path, click **Add escalation**.</span></span> <span data-ttu-id="2db9f-286">Vyberte jednu z možností v následující tabulce a před přechodem na krok 4 postupujte podle dalších kroků pro tuto možnost.</span><span class="sxs-lookup"><span data-stu-id="2db9f-286">Select one of the options in the following table, and then follow the additional steps for that option before you go to step 4.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="2db9f-287">Možnost</span><span class="sxs-lookup"><span data-stu-id="2db9f-287">Option</span></span></th>
    <th><span data-ttu-id="2db9f-288">Uživatelé, kterým je rozhodnutí eskalováno</span><span class="sxs-lookup"><span data-stu-id="2db9f-288">Users that the decision is escalated to</span></span></th>
    <th><span data-ttu-id="2db9f-289">Další kroky</span><span class="sxs-lookup"><span data-stu-id="2db9f-289">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="2db9f-290">Hierarchie</span><span class="sxs-lookup"><span data-stu-id="2db9f-290">Hierarchy</span></span></td>
    <td><span data-ttu-id="2db9f-291">Uživatelé v určité organizační hierarchii</span><span class="sxs-lookup"><span data-stu-id="2db9f-291">Users in a specific organizational hierarchy</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="2db9f-292">Po výběru možnosti <strong>Hierarchie</strong> na kartě <strong>Výběr hierarchie</strong> v seznamu <strong>Typ hierarchie</strong> vyberte typ hierarchie, ke které rozhodnutí eskalovat.</span><span class="sxs-lookup"><span data-stu-id="2db9f-292">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to escalate the decision to.</span></span></li>
    <li><span data-ttu-id="2db9f-293">Systém musí z hierarchie načíst rozsah jmen uživatelů.</span><span class="sxs-lookup"><span data-stu-id="2db9f-293">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="2db9f-294">Tato jména představují uživatele, ke kterým může být rozhodnutí eskalováno.</span><span class="sxs-lookup"><span data-stu-id="2db9f-294">These names represent users that the decision can be escalated to.</span></span> <span data-ttu-id="2db9f-295">Podle těchto kroků určete počáteční a koncový bod rozsahu uživatelských jmen, které systém obdrží:</span><span class="sxs-lookup"><span data-stu-id="2db9f-295">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="2db9f-296">Chcete-li zadat počáteční bod, vyberte osobu v seznamu <strong>Začátek od</strong>.</span><span class="sxs-lookup"><span data-stu-id="2db9f-296">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="2db9f-297">Chcete-li zadat koncový bod, klepněte na možnost <strong>Přidat podmínku</strong>.</span><span class="sxs-lookup"><span data-stu-id="2db9f-297">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="2db9f-298">Poté zadáním podmínky označte, kde v hierarchii má systém přestat načítat jména.</span><span class="sxs-lookup"><span data-stu-id="2db9f-298">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="2db9f-299">Na kartě <strong>Možnosti hierarchie</strong> zadejte uživatele v rozsahu, ke kterým by měl být rozhodnutí eskalováno:</span><span class="sxs-lookup"><span data-stu-id="2db9f-299">On the <strong>Hierarchy options</strong> tab, specify which users in the range the decision should be escalated to:</span></span> <ul>
    <li><span data-ttu-id="2db9f-300"><strong>Přiřadit všechny načtené uživatele</strong> – rozhodnutí dokument bude eskalováno všem uživatelům v rozsahu.</span><span class="sxs-lookup"><span data-stu-id="2db9f-300"><strong>Assign to all users retrieved</strong> – The decision is escalated to all users in the range.</span></span></li>
    <li><span data-ttu-id="2db9f-301"><strong>Přiřadit pouze poslednímu načtenému uživateli</strong> – rozhodnutí bude eskalováno pouze poslednímu uživateli v rozsahu.</span><span class="sxs-lookup"><span data-stu-id="2db9f-301"><strong>Assign only to last user retrieved</strong> – The decision is escalated to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="2db9f-302"><strong>Vyloučit uživatele splňující následující podmínku</strong> – rozhodnutí není eskalováno žádnému uživateli v rozsahu, který odpovídá konkrétní podmínce.</span><span class="sxs-lookup"><span data-stu-id="2db9f-302"><strong>Exclude users with the following condition:</strong> – The decision isn't escalated to any users in the range who meet a specific condition.</span></span> <span data-ttu-id="2db9f-303">Po klepnutí na volbu <strong>Přidat podmínku</strong> určete požadovanou podmínku.</span><span class="sxs-lookup"><span data-stu-id="2db9f-303">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="2db9f-304">Uživatel workflowu</span><span class="sxs-lookup"><span data-stu-id="2db9f-304">Workflow user</span></span></td>
    <td><span data-ttu-id="2db9f-305">Uživatelé v aktuálním workflowu</span><span class="sxs-lookup"><span data-stu-id="2db9f-305">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="2db9f-306">Po výběru možnosti <strong>Uživatel workflowu</strong> na kartě <strong>Uživatel workflowu</strong> v seznamu <strong>Uživatel workflowu</strong> vyberte uživatele, který se podílí na workflowu.</span><span class="sxs-lookup"><span data-stu-id="2db9f-306">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="2db9f-307">Uživatel</span><span class="sxs-lookup"><span data-stu-id="2db9f-307">User</span></span></td>
    <td><span data-ttu-id="2db9f-308">Konkrétní uživatelé aplikace Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="2db9f-308">Specific Finance and Operations users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="2db9f-309">Po výběru možnosti <strong>Uživatel</strong> klepněte na kartu <strong>Uživatel</strong>.</span><span class="sxs-lookup"><span data-stu-id="2db9f-309">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="2db9f-310">Seznam <strong>Dostupní uživatelé</strong> obsahuje všechny uživatele aplikace Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="2db9f-310">The <strong>Available users</strong> list includes all Finance and Operations users.</span></span> <span data-ttu-id="2db9f-311">Vyberte uživatele, ke kterým chcete rozhodnutí eskalovat, a pak přesuňte tyto uživatele do seznamu <strong>Vybraní uživatelé</strong>.</span><span class="sxs-lookup"><span data-stu-id="2db9f-311">Select the users to escalate the decision to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

4. <span data-ttu-id="2db9f-312">Na kartě **Časový limit** v poli **Trvání** určete, kolik času má uživatel na rozhodnutí.</span><span class="sxs-lookup"><span data-stu-id="2db9f-312">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to make the decision.</span></span> <span data-ttu-id="2db9f-313">Vyberte některou z následujících možností:</span><span class="sxs-lookup"><span data-stu-id="2db9f-313">Select one of the following options:</span></span>

    - <span data-ttu-id="2db9f-314">**Hodiny** – zadejte počet hodin, které má uživatel na rozhodnutí.</span><span class="sxs-lookup"><span data-stu-id="2db9f-314">**Hours** – Enter the number of hours that the user has to make the decision.</span></span> <span data-ttu-id="2db9f-315">Pak vyberte kalendář, který vaše organizace používá, a zadejte informace o pracovním týdnu vaší organizace.</span><span class="sxs-lookup"><span data-stu-id="2db9f-315">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="2db9f-316">**Dny** – zadejte počet dnů, které má uživatel na rozhodnutí.</span><span class="sxs-lookup"><span data-stu-id="2db9f-316">**Days** – Enter the number of days that the user has to make the decision.</span></span> <span data-ttu-id="2db9f-317">Pak vyberte kalendář, který vaše organizace používá, a zadejte informace o pracovním týdnu vaší organizace.</span><span class="sxs-lookup"><span data-stu-id="2db9f-317">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="2db9f-318">**Týdny** – zadejte počet týdnů, které má uživatel na rozhodnutí.</span><span class="sxs-lookup"><span data-stu-id="2db9f-318">**Weeks** – Enter the number of weeks that the user has to make the decision.</span></span>
    - <span data-ttu-id="2db9f-319">**Měsíce** – vyberte den a týden, do kdy se musí uživatel rozhodnout.</span><span class="sxs-lookup"><span data-stu-id="2db9f-319">**Months** – Select the day and week that the user must make the decision by.</span></span> <span data-ttu-id="2db9f-320">Můžete například požadovat, aby uživatel učinil rozhodnutí do třetího pátku v daném měsíci.</span><span class="sxs-lookup"><span data-stu-id="2db9f-320">For example, you might want the user to make the decision by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="2db9f-321">**Roky** – vyberte den, týden a měsíc, do kdy se musí uživatel rozhodnout.</span><span class="sxs-lookup"><span data-stu-id="2db9f-321">**Years** – Select the day, week, and month that the user must make the decision by.</span></span> <span data-ttu-id="2db9f-322">Můžete například požadovat, aby uživatel učinil rozhodnutí do třetího pátku v prosinci.</span><span class="sxs-lookup"><span data-stu-id="2db9f-322">For example, you might want the user to make the decision by Friday of the third week of December.</span></span>

5. <span data-ttu-id="2db9f-323">Zopakujte kroky 3 a 4 u každého uživatele, který má být přidán do eskalační cesty.</span><span class="sxs-lookup"><span data-stu-id="2db9f-323">Repeat steps 3 through 4 for each user that should be added to the escalation path.</span></span> <span data-ttu-id="2db9f-324">Pořadí uživatelů lze změnit.</span><span class="sxs-lookup"><span data-stu-id="2db9f-324">You can change the order of the users.</span></span>
6. <span data-ttu-id="2db9f-325">Pokud uživatelé v eskalační cestě v určeném čase rozhodnutí neučiní, systém sám provede rozhodnutí.</span><span class="sxs-lookup"><span data-stu-id="2db9f-325">If the users in the escalation path don't make the decision in the allotted time, the system makes the decision.</span></span> <span data-ttu-id="2db9f-326">Možnost, kterou systém vybere, můžete vybrat výběrem řádku **Akce** a na kartě **Konečná akce** vyberte možnost.</span><span class="sxs-lookup"><span data-stu-id="2db9f-326">To specify the option that the system selects, select the **Action** row, and then, on the **End action** tab, select an option.</span></span>

## <a name="set-a-time-limit"></a><span data-ttu-id="2db9f-327">Nastavení časového limitu</span><span class="sxs-lookup"><span data-stu-id="2db9f-327">Set a time limit</span></span>

<span data-ttu-id="2db9f-328">Tento postup použijte, pokud je rozhodnutí nutné učinit v určitém čase.</span><span class="sxs-lookup"><span data-stu-id="2db9f-328">Follow these steps if the decision must be made in a specific time.</span></span>

> [!NOTE]
> <span data-ttu-id="2db9f-329">Možnosti, které vyberete v rámci této procedury, přepíší možnosti vybrané v oblasti **Přiřazení** a **Eskalace** na stránce.</span><span class="sxs-lookup"><span data-stu-id="2db9f-329">The options that you select in this procedure override the options that you selected in the **Assignment** and **Escalation** areas of the page.</span></span>

1. <span data-ttu-id="2db9f-330">V levém podokně klepněte na tlačítko **Pokročilá nastavení**.</span><span class="sxs-lookup"><span data-stu-id="2db9f-330">In the left pane, click **Advanced settings**.</span></span>
2. <span data-ttu-id="2db9f-331">Označte pole **Nastavit časový limit pro prvek workflowu**.</span><span class="sxs-lookup"><span data-stu-id="2db9f-331">Select the **Set a time limit for the workflow element** check box.</span></span>
3. <span data-ttu-id="2db9f-332">V poli **Trvání** upřesněte, kdy má být rozhodnutí učiněno.</span><span class="sxs-lookup"><span data-stu-id="2db9f-332">In the **Duration** field, specify when the decision must be made.</span></span> <span data-ttu-id="2db9f-333">Vyberte některou z následujících možností:</span><span class="sxs-lookup"><span data-stu-id="2db9f-333">Select one of the following options:</span></span>

    - <span data-ttu-id="2db9f-334">**Hodiny** – zadejte počet hodin</span><span class="sxs-lookup"><span data-stu-id="2db9f-334">**Hours** – Enter the number of hours.</span></span> <span data-ttu-id="2db9f-335">Pak vyberte kalendář, který vaše organizace používá, a zadejte informace o pracovním týdnu vaší organizace.</span><span class="sxs-lookup"><span data-stu-id="2db9f-335">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="2db9f-336">**Dny** – zadejte počet dnů</span><span class="sxs-lookup"><span data-stu-id="2db9f-336">**Days** – Enter the number of days.</span></span> <span data-ttu-id="2db9f-337">Pak vyberte kalendář, který vaše organizace používá, a zadejte informace o pracovním týdnu vaší organizace.</span><span class="sxs-lookup"><span data-stu-id="2db9f-337">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="2db9f-338">**Týdny** – zadejte počet týdnů.</span><span class="sxs-lookup"><span data-stu-id="2db9f-338">**Weeks** – Enter the number of weeks.</span></span>
    - <span data-ttu-id="2db9f-339">**Měsíce** – vyberte den a týden, do kdy má být rozhodnutí učiněno.</span><span class="sxs-lookup"><span data-stu-id="2db9f-339">**Months** – Select the day and week that the decision must be made by.</span></span> <span data-ttu-id="2db9f-340">Můžete například požadovat, aby bylo rozhodnutí učiněno do třetího pátku v daném měsíci.</span><span class="sxs-lookup"><span data-stu-id="2db9f-340">For example, you might want the decision to be made by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="2db9f-341">**Roky** – vyberte den, týden a měsíc, do kdy má být rozhodnutí učiněno.</span><span class="sxs-lookup"><span data-stu-id="2db9f-341">**Years** – Select the day, week, and month that the decision must be made by.</span></span> <span data-ttu-id="2db9f-342">Můžete například požadovat, aby bylo rozhodnutí učiněno do třetího pátku v prosinci.</span><span class="sxs-lookup"><span data-stu-id="2db9f-342">For example, you might want the decision to be made by Friday of the third week of December.</span></span>

4. <span data-ttu-id="2db9f-343">Dojde-li k překročení časového limitu, systém učiní rozhodnutí.</span><span class="sxs-lookup"><span data-stu-id="2db9f-343">If the time limit is exceeded, the system makes the decision.</span></span> <span data-ttu-id="2db9f-344">V seznamu **Akce** vyberte možnost, která má být vybrána.</span><span class="sxs-lookup"><span data-stu-id="2db9f-344">In the **Action** list, select the option that the system should select.</span></span>

