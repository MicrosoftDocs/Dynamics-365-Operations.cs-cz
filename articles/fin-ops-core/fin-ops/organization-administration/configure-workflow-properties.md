---
title: Konfigurace vlastností workflow
description: Toto téma vysvětluje, jak nakonfigurovat různé vlastnosti workflowu.
author: sericks007
manager: AnnBe
ms.date: 07/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 196083
ms.assetid: 192b7a98-7d04-4c7a-a986-29d797a8a837
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 268448049955170b8eb9e64cbd50416565a041b1
ms.sourcegitcommit: 561d06c2a74602dfaa40334d8afac5053aebc055
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/07/2020
ms.locfileid: "3541102"
---
# <a name="configure-workflow-properties"></a><span data-ttu-id="cf28b-103">Konfigurace vlastností workflow</span><span class="sxs-lookup"><span data-stu-id="cf28b-103">Configure workflow properties</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cf28b-104">Toto téma vysvětluje, jak nakonfigurovat různé vlastnosti workflowu.</span><span class="sxs-lookup"><span data-stu-id="cf28b-104">This topic explains how to configure the various properties of a workflow.</span></span>

<span data-ttu-id="cf28b-105">Pokud chcete konfigurovat vlastnosti workflowu, otevřete workflow v editoru workflowu.</span><span class="sxs-lookup"><span data-stu-id="cf28b-105">To configure the properties of a workflow, open the workflow in the workflow editor.</span></span> <span data-ttu-id="cf28b-106">Klikněte na plátno editoru workflowu a klepněte na tlačítko **Vlastnosti** k otevření stránky **Vlastnosti**.</span><span class="sxs-lookup"><span data-stu-id="cf28b-106">Click the canvas of the workflow editor, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="cf28b-107">Pro konfiguraci vlastností workflowu můžete použít následující kroky.</span><span class="sxs-lookup"><span data-stu-id="cf28b-107">You can then use the following procedures to configure the various properties of the workflow.</span></span>

## <a name="name-the-workflow"></a><span data-ttu-id="cf28b-108">Pojmenování workflowu</span><span class="sxs-lookup"><span data-stu-id="cf28b-108">Name the workflow</span></span>

<span data-ttu-id="cf28b-109">Pomocí následujících kroků zadejte název workflowu.</span><span class="sxs-lookup"><span data-stu-id="cf28b-109">Follow these steps to enter a name for the workflow.</span></span>

1. <span data-ttu-id="cf28b-110">V levém podokně klepněte na tlačítko **Základní nastavení**.</span><span class="sxs-lookup"><span data-stu-id="cf28b-110">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="cf28b-111">V poli **Název** zadejte jedinečný název workflowu.</span><span class="sxs-lookup"><span data-stu-id="cf28b-111">In the **Name** field, enter a unique name for the workflow.</span></span> <span data-ttu-id="cf28b-112">Předpokládejme například, že vytváříte workflowy nákupních požadavků pro každou zemi nebo oblast, ve které působíte. Pro workflow nákupního požadavku můžete například zadat název **Nákupní požadavky – Dánsko** nebo **Nákupní požadavky – Španělsko**.</span><span class="sxs-lookup"><span data-stu-id="cf28b-112">For example, if you create a purchase requisition workflow for each country/region that you operate in, you can name the purchase requisition workflow **Purchase Requisitions Denmark** or **Purchase Requisitions Spain**.</span></span>

## <a name="specify-the-workflow-owner"></a><span data-ttu-id="cf28b-113">Zadání vlastníka workflowu</span><span class="sxs-lookup"><span data-stu-id="cf28b-113">Specify the workflow owner</span></span>

<span data-ttu-id="cf28b-114">Vlastník workflowu je osoba, která bude spravovat workflow.</span><span class="sxs-lookup"><span data-stu-id="cf28b-114">The workflow owner is the person who manages and maintains the workflow.</span></span> <span data-ttu-id="cf28b-115">Vlastníka workflowu můžete zadat provedením následujícího postupu.</span><span class="sxs-lookup"><span data-stu-id="cf28b-115">Follow these steps to specify the workflow owner.</span></span>

1. <span data-ttu-id="cf28b-116">V levém podokně klepněte na tlačítko **Základní nastavení**.</span><span class="sxs-lookup"><span data-stu-id="cf28b-116">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="cf28b-117">V seznamu **Vlastník** vyberte jméno osoby, který bude spravovat tento workflow.</span><span class="sxs-lookup"><span data-stu-id="cf28b-117">In the **Owner** list, select the name of the person who will manage the workflow.</span></span>

## <a name="select-an-email-template"></a><span data-ttu-id="cf28b-118">Výběr šablony e-mailu</span><span class="sxs-lookup"><span data-stu-id="cf28b-118">Select an email template</span></span>

<span data-ttu-id="cf28b-119">Podle těchto kroků vyberte šablonu e-mailu, která se používá k vytvoření oznámení o workflowu.</span><span class="sxs-lookup"><span data-stu-id="cf28b-119">Follow these steps to select the email template that is used to generate notification messages about the workflow.</span></span>

1. <span data-ttu-id="cf28b-120">V levém podokně klepněte na tlačítko **Základní nastavení**.</span><span class="sxs-lookup"><span data-stu-id="cf28b-120">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="cf28b-121">V seznamu **Šablona e-mailu k oznámení pro workflow** vyberte šablonu.</span><span class="sxs-lookup"><span data-stu-id="cf28b-121">In the **Email template for workflow notifications** list, select the template.</span></span>

## <a name="enter-instructions-for-users"></a><span data-ttu-id="cf28b-122">Zadání pokynů pro uživatele</span><span class="sxs-lookup"><span data-stu-id="cf28b-122">Enter instructions for users</span></span>

<span data-ttu-id="cf28b-123">Můžete zadat pokyny pro uživatele, kteří budou odesílat dokumenty ke zpracování a schválení.</span><span class="sxs-lookup"><span data-stu-id="cf28b-123">You can provide instructions to users who submit documents for processing and approval.</span></span> <span data-ttu-id="cf28b-124">Tito uživatelé jsou označovány jako *původci*.</span><span class="sxs-lookup"><span data-stu-id="cf28b-124">These users are also referred to as *originators*.</span></span> <span data-ttu-id="cf28b-125">Budeme například předpokládat, že vytváříte workflow nákupní žádanky, a že jste zadali pokyny.</span><span class="sxs-lookup"><span data-stu-id="cf28b-125">For example, you're creating a purchase requisition workflow, and you enter instructions.</span></span> <span data-ttu-id="cf28b-126">Tyto pokyny mohou zobrazit uživatelé zadáním nákupního požadavku na stránce **Nákupní požadavky**.</span><span class="sxs-lookup"><span data-stu-id="cf28b-126">Those instructions can then be viewed by users who enter purchase requisitions on the **Purchase requisitions** page.</span></span> <span data-ttu-id="cf28b-127">Původce může zobrazit pokyny klepnutím na příslušnou ikonu na panelu zpráv pro workflow.</span><span class="sxs-lookup"><span data-stu-id="cf28b-127">To view instructions, the originator clicks the icon in the workflow message bar.</span></span> <span data-ttu-id="cf28b-128">Pokyny pro uživatele můžete zadat provedením následujícího postupu.</span><span class="sxs-lookup"><span data-stu-id="cf28b-128">Follow these steps to enter instructions for users.</span></span>

1. <span data-ttu-id="cf28b-129">V levém podokně klepněte na tlačítko **Základní nastavení**.</span><span class="sxs-lookup"><span data-stu-id="cf28b-129">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="cf28b-130">V poli **Pokyny pro odeslání** zadejte pokyny.</span><span class="sxs-lookup"><span data-stu-id="cf28b-130">In the **Submission instructions** field, enter the instructions.</span></span>
3. <span data-ttu-id="cf28b-131">Pokyny můžete přizpůsobit vložením zástupného textu.</span><span class="sxs-lookup"><span data-stu-id="cf28b-131">To personalize the instructions, you can insert placeholders.</span></span> <span data-ttu-id="cf28b-132">Zástupný text bude při zobrazení pokynů uživatelům nahrazen odpovídacími daty.</span><span class="sxs-lookup"><span data-stu-id="cf28b-132">Placeholders are replaced with the appropriate data when the instructions are shown to users.</span></span> <span data-ttu-id="cf28b-133">Při vkládání zástupného textu postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="cf28b-133">To insert a placeholder, follow these steps:</span></span>

    1. <span data-ttu-id="cf28b-134">Klepnutím v poli **Pokyny pro odeslání** zadejte, kde se má zástupný text zobrazit.</span><span class="sxs-lookup"><span data-stu-id="cf28b-134">Click in the **Submission instructions** field to specify where the placeholder should appear.</span></span>
    2. <span data-ttu-id="cf28b-135">Klikněte na **Vložit zástupný text**.</span><span class="sxs-lookup"><span data-stu-id="cf28b-135">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="cf28b-136">V nově otevřeném seznamu vyberte vkládaný zástupný text.</span><span class="sxs-lookup"><span data-stu-id="cf28b-136">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="cf28b-137">Klepněte na tlačítko **Vložit**.</span><span class="sxs-lookup"><span data-stu-id="cf28b-137">Click **Insert**.</span></span>

4. <span data-ttu-id="cf28b-138">Chcete-li přidat překlady pokynů, postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="cf28b-138">To add translations of the instructions, follow these steps:</span></span>

    1. <span data-ttu-id="cf28b-139">Klikněte na **Překlady**.</span><span class="sxs-lookup"><span data-stu-id="cf28b-139">Click **Translations**.</span></span>
    2. <span data-ttu-id="cf28b-140">Na nově otevřené stránce klikněte na **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="cf28b-140">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="cf28b-141">V nově otevřeném seznamu vyberte jazyk, který chcete použít pro zadání textu.</span><span class="sxs-lookup"><span data-stu-id="cf28b-141">In the list that appears, select the language that you will enter the text in.</span></span>
    4. <span data-ttu-id="cf28b-142">V poli **Přeložený text** zadejte text.</span><span class="sxs-lookup"><span data-stu-id="cf28b-142">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="cf28b-143">Text můžete přizpůsobit vložením zástupného textu.</span><span class="sxs-lookup"><span data-stu-id="cf28b-143">To personalize the text, you can insert placeholders.</span></span> <span data-ttu-id="cf28b-144">Pokyny, jak zadat zástupný text, naleznete v kroku 3.</span><span class="sxs-lookup"><span data-stu-id="cf28b-144">For instructions about how to enter a placeholder, see step 3.</span></span>
    6. <span data-ttu-id="cf28b-145">Klepněte na tlačítko **Zavřít**.</span><span class="sxs-lookup"><span data-stu-id="cf28b-145">Click **Close**.</span></span>

## <a name="specify-when-this-workflow-is-used-through-activation-conditions"></a><span data-ttu-id="cf28b-146">Určete, kdy se tento workflow používá v podmínkách aktivace</span><span class="sxs-lookup"><span data-stu-id="cf28b-146">Specify when this workflow is used through activation conditions</span></span>

<span data-ttu-id="cf28b-147">Můžete vytvořit více workflowů založených na stejném typu workflowu.</span><span class="sxs-lookup"><span data-stu-id="cf28b-147">You can create multiple workflows that are based on the same workflow type.</span></span> <span data-ttu-id="cf28b-148">Pokud máte více workflowů založených na stejném typu, je nutné zadat, kdy má být který workflow použit pomocí podmínek aktivace.</span><span class="sxs-lookup"><span data-stu-id="cf28b-148">When you have multiple workflows that are based on the same type, you must specify when each workflow is used using activation conditions.</span></span> <span data-ttu-id="cf28b-149">Nejsou-li podmínky aktivace splněny, použije se výchozí Workflow.</span><span class="sxs-lookup"><span data-stu-id="cf28b-149">If activation conditions are not met, then the default workflow is used.</span></span> <span data-ttu-id="cf28b-150">Podobně, pokud je pro typ workflowu definována pouze jedna konfigurace workflowu, bude tato konfigurace workflowu použita bez ohledu na podmínky aktivace.</span><span class="sxs-lookup"><span data-stu-id="cf28b-150">Similarly, if there is only one workflow configuration defined for a workflow type, then that workflow configuration will be used regardless of the activation conditions.</span></span>

<span data-ttu-id="cf28b-151">Můžete například vytvořit workflow nákupních požadavků, pro každou zemi nebo oblast, ve které působíte, například Nákupní požadavky – Dánsko a Nákupní požadavky – Španělsko s následujícími podmínkami:</span><span class="sxs-lookup"><span data-stu-id="cf28b-151">For example, you can create a purchase requisition workflow for each country/region that you operate in, such as Purchase Requisitions Denmark and Purchase Requisitions Spain, with the following conditions:</span></span>

- <span data-ttu-id="cf28b-152">Nákupní požadavky – Dánsko se má používat v případě, že země či oblast = DK</span><span class="sxs-lookup"><span data-stu-id="cf28b-152">Purchase Requisitions Denmark is used when: country/region = DK</span></span>
- <span data-ttu-id="cf28b-153">Nákupní požadavky – Španělsko se má používat v případě, že země či oblast = ES</span><span class="sxs-lookup"><span data-stu-id="cf28b-153">Purchase Requisitions Spain is used when: country/region = ES</span></span>

<span data-ttu-id="cf28b-154">Pomocí následujících kroků zadejte, kdy se má použít workflow, který konfigurujete.</span><span class="sxs-lookup"><span data-stu-id="cf28b-154">Follow these steps to specify when the workflow that you're configuring is used.</span></span>

1. <span data-ttu-id="cf28b-155">V levém podokně klikněte na **Aktivace**.</span><span class="sxs-lookup"><span data-stu-id="cf28b-155">In the left pane, click **Activation**.</span></span>
2. <span data-ttu-id="cf28b-156">Označte pole **Nastavit podmínky pro spuštění tohoto workflowu**.</span><span class="sxs-lookup"><span data-stu-id="cf28b-156">Select the **Set the conditions for running this workflow** check box.</span></span>
3. <span data-ttu-id="cf28b-157">Klepněte na možnost **Přidat podmínku**.</span><span class="sxs-lookup"><span data-stu-id="cf28b-157">Click **Add condition**.</span></span>
4. <span data-ttu-id="cf28b-158">Zadání podmínky</span><span class="sxs-lookup"><span data-stu-id="cf28b-158">Enter a condition.</span></span>
5. <span data-ttu-id="cf28b-159">Zadejte všechny další podmínky, které jsou požadovány.</span><span class="sxs-lookup"><span data-stu-id="cf28b-159">Enter any additional conditions that are required.</span></span>
6. <span data-ttu-id="cf28b-160">Proveďte pracovní postup s některými cílovými záznamy a ověřte, zda podmínka správně zahrnuje a vylučuje záznamy.</span><span class="sxs-lookup"><span data-stu-id="cf28b-160">Run through the workflow with some target records to verify that the condition correctly includes and excludes records.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="cf28b-161">Zadejte, kdy se mají odesílat oznámení.</span><span class="sxs-lookup"><span data-stu-id="cf28b-161">Specify when notifications are sent</span></span>

<span data-ttu-id="cf28b-162">Když je dokument odeslán ke zpracování, je vytvořena instance workflowu.</span><span class="sxs-lookup"><span data-stu-id="cf28b-162">When a document is submitted for processing, a workflow instance is created.</span></span> <span data-ttu-id="cf28b-163">Uživatelům lze odeslat oznámení v případech, kdy jsou instance workflowu (na základě tohoto workflowu) spuštěny, dokončeny, zrušeny nebo zastaveny z důvodu chyby.</span><span class="sxs-lookup"><span data-stu-id="cf28b-163">You can send notifications to users when workflow instances that are based on the workflow are started, completed, terminated, or stopped because of an error.</span></span> <span data-ttu-id="cf28b-164">Pomocí následujících kroků můžete zadat, kdy mají být odeslána oznámení.</span><span class="sxs-lookup"><span data-stu-id="cf28b-164">Follow these steps to specify when notifications are sent.</span></span>

1. <span data-ttu-id="cf28b-165">V levém podokně klikněte na **Oznámení**.</span><span class="sxs-lookup"><span data-stu-id="cf28b-165">In the left pane, click **Notifications**.</span></span>
2. <span data-ttu-id="cf28b-166">Označte pole u každé události, která má spustit oznámení:</span><span class="sxs-lookup"><span data-stu-id="cf28b-166">Select the check box for each event that should trigger notifications:</span></span>

    - <span data-ttu-id="cf28b-167">**Zahájeno** – odesílat oznámení při zahájení instance workflowu.</span><span class="sxs-lookup"><span data-stu-id="cf28b-167">**Started** – Send notifications when a workflow instance is started.</span></span>
    - <span data-ttu-id="cf28b-168">**Zastaveno** – odesílat oznámení v případě, že je instance workflowu zastavena z důvodu chyby.</span><span class="sxs-lookup"><span data-stu-id="cf28b-168">**Stopped** – Send notifications when a workflow instance is stopped because of an error.</span></span>
    - <span data-ttu-id="cf28b-169">**Dokončeno** – odesílat oznámení při dokončení instance workflowu.</span><span class="sxs-lookup"><span data-stu-id="cf28b-169">**Completed** – Send notifications when a workflow instance is completed.</span></span>
    - <span data-ttu-id="cf28b-170">**Bez možnosti obnovy** – odesílat oznámení v případě, že je instance workflowu zastavena z důvodu neobnovitelné chyby.</span><span class="sxs-lookup"><span data-stu-id="cf28b-170">**Unrecoverable** – Send notifications when a workflow instance is stopped because of an unrecoverable error.</span></span>
    - <span data-ttu-id="cf28b-171">**Ukončeno** – odesílat oznámení při ukončení instance workflowu.</span><span class="sxs-lookup"><span data-stu-id="cf28b-171">**Terminated** – Send notifications when a workflow instance is terminated.</span></span>

3. <span data-ttu-id="cf28b-172">Vyberte řádek pro událost, kterou jste vybrali v kroku 2.</span><span class="sxs-lookup"><span data-stu-id="cf28b-172">Select the row for an event that you selected in step 2.</span></span>
4. <span data-ttu-id="cf28b-173">Na kartě **Text oznámení** zadejte text oznámení.</span><span class="sxs-lookup"><span data-stu-id="cf28b-173">On the **Notification text** tab, enter the text of the notification.</span></span>
5. <span data-ttu-id="cf28b-174">Text můžete přizpůsobit vložením zástupného textu.</span><span class="sxs-lookup"><span data-stu-id="cf28b-174">To personalize the text, you can insert placeholders.</span></span> <span data-ttu-id="cf28b-175">Zástupný text bude při zobrazení textu uživatelům nahrazen odpovídacími daty.</span><span class="sxs-lookup"><span data-stu-id="cf28b-175">Placeholders are replaced with the appropriate data when the text is shown to users.</span></span> <span data-ttu-id="cf28b-176">Při vkládání zástupného textu postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="cf28b-176">To insert a placeholder, follow these steps:</span></span>

    1. <span data-ttu-id="cf28b-177">Klepnutím do pole zadejte, kde se má zástupný text zobrazit.</span><span class="sxs-lookup"><span data-stu-id="cf28b-177">Click in the field to specify where the placeholder should appear.</span></span>
    2. <span data-ttu-id="cf28b-178">Klikněte na **Vložit zástupný text**.</span><span class="sxs-lookup"><span data-stu-id="cf28b-178">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="cf28b-179">V nově otevřeném seznamu vyberte vkládaný zástupný text.</span><span class="sxs-lookup"><span data-stu-id="cf28b-179">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="cf28b-180">Klepněte na tlačítko **Vložit**.</span><span class="sxs-lookup"><span data-stu-id="cf28b-180">Click **Insert**.</span></span>
    5. <span data-ttu-id="cf28b-181">Běžný zástupce za **Text oznámení**, který má být zahrnut, je "Poslední poznámky: %Workflow.Last note%", který zobrazuje všechny komentáře z předchozího kroku.</span><span class="sxs-lookup"><span data-stu-id="cf28b-181">A common **Notification text** placeholder to include is "Last Notes: %Workflow.Last note%", which displays any comments from the previous step.</span></span>

6. <span data-ttu-id="cf28b-182">Chcete-li přidat překlady textu, postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="cf28b-182">To add translations of the text, follow these steps:</span></span>

    1. <span data-ttu-id="cf28b-183">Klikněte na **Překlady**.</span><span class="sxs-lookup"><span data-stu-id="cf28b-183">Click **Translations**.</span></span>
    2. <span data-ttu-id="cf28b-184">Na nově otevřené stránce klikněte na **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="cf28b-184">On the page that appears, Click **Add**.</span></span>
    3. <span data-ttu-id="cf28b-185">V nově otevřeném seznamu vyberte jazyk, který chcete použít pro zadání textu.</span><span class="sxs-lookup"><span data-stu-id="cf28b-185">In the list that appears, select the language that you will enter the text in.</span></span>
    4. <span data-ttu-id="cf28b-186">V poli **Přeložený text** zadejte text.</span><span class="sxs-lookup"><span data-stu-id="cf28b-186">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="cf28b-187">Text můžete přizpůsobit vložením zástupného textu.</span><span class="sxs-lookup"><span data-stu-id="cf28b-187">To personalize the text, you can insert placeholders.</span></span> <span data-ttu-id="cf28b-188">Pokyny, jak zadat zástupný text, naleznete v kroku 5.</span><span class="sxs-lookup"><span data-stu-id="cf28b-188">For instructions about how to enter a placeholder, see step 5.</span></span>
    6. <span data-ttu-id="cf28b-189">Klepněte na tlačítko **Zavřít**.</span><span class="sxs-lookup"><span data-stu-id="cf28b-189">Click **Close**.</span></span>

7. <span data-ttu-id="cf28b-190">Na kartě **Příjemce** použijte následující možnosti k určení příjemce oznámení.</span><span class="sxs-lookup"><span data-stu-id="cf28b-190">On the **Recipient** tab, use the following options to specify who should receive the notifications.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="cf28b-191">Možnost</span><span class="sxs-lookup"><span data-stu-id="cf28b-191">Option</span></span></th>
    <th><span data-ttu-id="cf28b-192">Oznámení bude odesláno těmto uživatelům</span><span class="sxs-lookup"><span data-stu-id="cf28b-192">Notifications are sent to these users</span></span></th>
    <th><span data-ttu-id="cf28b-193">Při odesílání oznámení postupujte takto</span><span class="sxs-lookup"><span data-stu-id="cf28b-193">To send notifications, follow these steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="cf28b-194">Účastník</span><span class="sxs-lookup"><span data-stu-id="cf28b-194">Participant</span></span></td>
    <td><span data-ttu-id="cf28b-195">Uživatelé, kteří jsou přiřazeni k určité skupině nebo roli</span><span class="sxs-lookup"><span data-stu-id="cf28b-195">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="cf28b-196">Na kartě <strong>Příjemce</strong> klepněte na možnost <strong>Účastník</strong>.</span><span class="sxs-lookup"><span data-stu-id="cf28b-196">On the <strong>Recipient</strong> tab, click <strong>Participant</strong>.</span></span></li>
    <li><span data-ttu-id="cf28b-197">Na kartě <strong>Založeno na roli</strong> v seznamu <strong>Typ účastníka</strong> vyberte typ skupiny nebo role, které chcete oznámení odeslat.</span><span class="sxs-lookup"><span data-stu-id="cf28b-197">On the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="cf28b-198">V seznamu <strong>Účastník</strong> vyberte skupinu nebo roli, které chcete oznámení odeslat.</span><span class="sxs-lookup"><span data-stu-id="cf28b-198">In the <strong>Participant</strong> list, select the group or role to send notifications to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="cf28b-199">Uživatel workflowu</span><span class="sxs-lookup"><span data-stu-id="cf28b-199">Workflow user</span></span></td>
    <td><span data-ttu-id="cf28b-200">Uživatelé, kteří jsou účastníci tohoto workflowu</span><span class="sxs-lookup"><span data-stu-id="cf28b-200">Users who are participants in this workflow</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="cf28b-201">Na kartě <strong>Příjemce</strong> klepněte na možnost <strong>Uživatel workflowu</strong>.</span><span class="sxs-lookup"><span data-stu-id="cf28b-201">On the <strong>Recipient</strong> tab, click <strong>Workflow user</strong>.</span></span></li>
    <li><span data-ttu-id="cf28b-202">Na kartě <strong>Uživatel workflowu</strong> v seznamu <strong>Uživatel workflowu</strong> vyberte účastníka tohoto workflowu.</span><span class="sxs-lookup"><span data-stu-id="cf28b-202">On the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a participant in this workflow.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="cf28b-203">Uživatel</span><span class="sxs-lookup"><span data-stu-id="cf28b-203">User</span></span></td>
    <td><span data-ttu-id="cf28b-204">Konkrétní uživatelé</span><span class="sxs-lookup"><span data-stu-id="cf28b-204">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="cf28b-205">Na kartě <strong>Příjemce</strong> klepněte na možnost <strong>Uživatel</strong>.</span><span class="sxs-lookup"><span data-stu-id="cf28b-205">On the <strong>Recipient</strong> tab, click <strong>User</strong>.</span></span></li>
    <li><span data-ttu-id="cf28b-206">Na kartě <strong>Uživatel</strong> obsahuje seznam <strong>Dostupní uživatelé</strong> všechny uživatele.</span><span class="sxs-lookup"><span data-stu-id="cf28b-206">On the <strong>User</strong> tab, the <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="cf28b-207">Vyberte uživatele, kterým chcete odeslat oznámení, a pak přesuňte tyto uživatele do seznamu <strong>Vybraní uživatelé</strong>.</span><span class="sxs-lookup"><span data-stu-id="cf28b-207">Select the users to send notifications to, and move those users into the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

8. <span data-ttu-id="cf28b-208">Zopakujte kroky 3 až 7 pro každou událost, kterou jste vybrali v kroku 2.</span><span class="sxs-lookup"><span data-stu-id="cf28b-208">Repeat steps 3 through 7 for each event that you selected in step 2.</span></span>

## <a name="enter-comments-about-the-changes-that-you-made-to-the-workflow"></a><span data-ttu-id="cf28b-209">Zadejte komentáře ke změnám provedeným v daném workflowu</span><span class="sxs-lookup"><span data-stu-id="cf28b-209">Enter comments about the changes that you made to the workflow</span></span>

<span data-ttu-id="cf28b-210">Chcete-li zadat komentáře ke změnám provedeným u tohoto workflowu, proveďte následující kroky.</span><span class="sxs-lookup"><span data-stu-id="cf28b-210">To enter comments about the changes that you made to the workflow, follow these steps.</span></span>

1. <span data-ttu-id="cf28b-211">V levém podokně klikněte na **Poznámky**.</span><span class="sxs-lookup"><span data-stu-id="cf28b-211">In the left pane, click **Notes**.</span></span>
2. <span data-ttu-id="cf28b-212">V poli **Zadat komentáře k workflowu** zadejte své poznámky.</span><span class="sxs-lookup"><span data-stu-id="cf28b-212">In the **Enter comments about the workflow** field, enter your comments.</span></span>
3. <span data-ttu-id="cf28b-213">Zkontrolujte své komentáře.</span><span class="sxs-lookup"><span data-stu-id="cf28b-213">Review your comments.</span></span> <span data-ttu-id="cf28b-214">Po přidání komentáře je již nelze upravit.</span><span class="sxs-lookup"><span data-stu-id="cf28b-214">After you add comments, you can't modify them.</span></span>
4. <span data-ttu-id="cf28b-215">Kliknutím na **Přidat** přidáte komentáře do oblasti **Historie poznámek**.</span><span class="sxs-lookup"><span data-stu-id="cf28b-215">Click **Add** to add your comments to the **Comment history** area.</span></span>
