---
title: "Konfigurace vlastností workflow"
description: "Toto téma vysvětluje, jak nakonfigurovat různé vlastnosti workflowu."
author: sericks007
manager: AnnBe
ms.date: 07/17/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 196083
ms.assetid: 192b7a98-7d04-4c7a-a986-29d797a8a837
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ba03473dd6fc31d51fd4e890acac1cd1494ef5a3
ms.openlocfilehash: a327b85f18f03294a237c3795ae2e1f4a97095f0
ms.contentlocale: cs-cz
ms.lasthandoff: 08/08/2018

---

# <a name="configure-workflow-properties"></a><span data-ttu-id="8aa2f-103">Konfigurace vlastností workflow</span><span class="sxs-lookup"><span data-stu-id="8aa2f-103">Configure workflow properties</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8aa2f-104">Toto téma vysvětluje, jak nakonfigurovat různé vlastnosti workflowu.</span><span class="sxs-lookup"><span data-stu-id="8aa2f-104">This topic explains how to configure the various properties of a workflow.</span></span>

<span data-ttu-id="8aa2f-105">Pokud chcete konfigurovat vlastnosti workflowu, otevřete workflow v editoru workflowu.</span><span class="sxs-lookup"><span data-stu-id="8aa2f-105">To configure the properties of a workflow, open the workflow in the workflow editor.</span></span> <span data-ttu-id="8aa2f-106">Klikněte na plátno editoru workflowu a klepněte na tlačítko **Vlastnosti** k otevření stránky **Vlastnosti**.</span><span class="sxs-lookup"><span data-stu-id="8aa2f-106">Click the canvas of the workflow editor, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="8aa2f-107">Pro konfiguraci vlastností workflowu můžete použít následující kroky.</span><span class="sxs-lookup"><span data-stu-id="8aa2f-107">You can then use the following procedures to configure the various properties of the workflow.</span></span>

## <a name="name-the-workflow"></a><span data-ttu-id="8aa2f-108">Pojmenování workflowu</span><span class="sxs-lookup"><span data-stu-id="8aa2f-108">Name the workflow</span></span>
<span data-ttu-id="8aa2f-109">Pomocí následujících kroků zadejte název workflowu.</span><span class="sxs-lookup"><span data-stu-id="8aa2f-109">Follow these steps to enter a name for the workflow.</span></span>

1.  <span data-ttu-id="8aa2f-110">V levém podokně klepněte na tlačítko **Základní nastavení**.</span><span class="sxs-lookup"><span data-stu-id="8aa2f-110">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="8aa2f-111">V poli **Název** zadejte jedinečný název workflowu.</span><span class="sxs-lookup"><span data-stu-id="8aa2f-111">In the **Name** field, enter a unique name for the workflow.</span></span> <span data-ttu-id="8aa2f-112">Předpokládejme například, že vytváříte workflowy nákupních požadavků pro každou zemi nebo oblast, ve které působíte. Pro workflow nákupního požadavku můžete například zadat název **Nákupní požadavky – Dánsko** nebo **Nákupní požadavky – Španělsko**.</span><span class="sxs-lookup"><span data-stu-id="8aa2f-112">For example, if you create a purchase requisition workflow for each country/region that you operate in, you can name the purchase requisition workflow **Purchase Requisitions Denmark** or **Purchase Requisitions Spain**.</span></span>

## <a name="specify-the-workflow-owner"></a><span data-ttu-id="8aa2f-113">Zadání vlastníka workflowu</span><span class="sxs-lookup"><span data-stu-id="8aa2f-113">Specify the workflow owner</span></span>
<span data-ttu-id="8aa2f-114">Vlastník workflowu je osoba, která bude spravovat workflow.</span><span class="sxs-lookup"><span data-stu-id="8aa2f-114">The workflow owner is the person who manages and maintains the workflow.</span></span> <span data-ttu-id="8aa2f-115">Vlastníka workflowu můžete zadat provedením následujícího postupu.</span><span class="sxs-lookup"><span data-stu-id="8aa2f-115">Follow these steps to specify the workflow owner.</span></span>

1.  <span data-ttu-id="8aa2f-116">V levém podokně klepněte na tlačítko **Základní nastavení**.</span><span class="sxs-lookup"><span data-stu-id="8aa2f-116">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="8aa2f-117">V seznamu **Vlastník** vyberte jméno osoby, který bude spravovat tento workflow.</span><span class="sxs-lookup"><span data-stu-id="8aa2f-117">In the **Owner** list, select the name of the person who will manage the workflow.</span></span>

## <a name="select-an-email-template"></a><span data-ttu-id="8aa2f-118">Výběr šablony e-mailu</span><span class="sxs-lookup"><span data-stu-id="8aa2f-118">Select an email template</span></span>
<span data-ttu-id="8aa2f-119">Podle těchto kroků vyberte šablonu e-mailu, která se používá k vytvoření oznámení o workflowu.</span><span class="sxs-lookup"><span data-stu-id="8aa2f-119">Follow these steps to select the email template that is used to generate notification messages about the workflow.</span></span>

1.  <span data-ttu-id="8aa2f-120">V levém podokně klepněte na tlačítko **Základní nastavení**.</span><span class="sxs-lookup"><span data-stu-id="8aa2f-120">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="8aa2f-121">V seznamu **Šablona e-mailu k oznámení pro workflow** vyberte šablonu.</span><span class="sxs-lookup"><span data-stu-id="8aa2f-121">In the **Email template for workflow notifications** list, select the template.</span></span>

## <a name="enter-instructions-for-users"></a><span data-ttu-id="8aa2f-122">Zadání pokynů pro uživatele</span><span class="sxs-lookup"><span data-stu-id="8aa2f-122">Enter instructions for users</span></span>
<span data-ttu-id="8aa2f-123">Můžete zadat pokyny pro uživatele, kteří budou odesílat dokumenty ke zpracování a schválení.</span><span class="sxs-lookup"><span data-stu-id="8aa2f-123">You can provide instructions to users who submit documents for processing and approval.</span></span> <span data-ttu-id="8aa2f-124">Tito uživatelé jsou označovány jako *původci*.</span><span class="sxs-lookup"><span data-stu-id="8aa2f-124">These users are also referred to as *originators*.</span></span> <span data-ttu-id="8aa2f-125">Budeme například předpokládat, že vytváříte workflow nákupní žádanky, a že jste zadali pokyny.</span><span class="sxs-lookup"><span data-stu-id="8aa2f-125">For example, you're creating a purchase requisition workflow, and you enter instructions.</span></span> <span data-ttu-id="8aa2f-126">Tyto pokyny mohou zobrazit uživatelé zadáním nákupního požadavku na stránce **Nákupní požadavky**.</span><span class="sxs-lookup"><span data-stu-id="8aa2f-126">Those instructions can then be viewed by users who enter purchase requisitions on the **Purchase requisitions** page.</span></span> <span data-ttu-id="8aa2f-127">Původce může zobrazit pokyny klepnutím na příslušnou ikonu na panelu zpráv pro workflow.</span><span class="sxs-lookup"><span data-stu-id="8aa2f-127">To view instructions, the originator clicks the icon in the workflow message bar.</span></span> <span data-ttu-id="8aa2f-128">Pokyny pro uživatele můžete zadat provedením následujícího postupu.</span><span class="sxs-lookup"><span data-stu-id="8aa2f-128">Follow these steps to enter instructions for users.</span></span>

1.  <span data-ttu-id="8aa2f-129">V levém podokně klepněte na tlačítko **Základní nastavení**.</span><span class="sxs-lookup"><span data-stu-id="8aa2f-129">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="8aa2f-130">V poli **Pokyny pro odeslání** zadejte pokyny.</span><span class="sxs-lookup"><span data-stu-id="8aa2f-130">In the **Submission instructions** field, enter the instructions.</span></span>
3.  <span data-ttu-id="8aa2f-131">Pokyny můžete přizpůsobit vložením zástupného textu.</span><span class="sxs-lookup"><span data-stu-id="8aa2f-131">To personalize the instructions, you can insert placeholders.</span></span> <span data-ttu-id="8aa2f-132">Zástupný text bude při zobrazení pokynů uživatelům nahrazen odpovídacími daty.</span><span class="sxs-lookup"><span data-stu-id="8aa2f-132">Placeholders are replaced with the appropriate data when the instructions are shown to users.</span></span> <span data-ttu-id="8aa2f-133">Při vkládání zástupného textu postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="8aa2f-133">To insert a placeholder, follow these steps:</span></span>
    1.  <span data-ttu-id="8aa2f-134">Klepnutím v poli **Pokyny pro odeslání** zadejte, kde se má zástupný text zobrazit.</span><span class="sxs-lookup"><span data-stu-id="8aa2f-134">Click in the **Submission instructions** field to specify where the placeholder should appear.</span></span>
    2.  <span data-ttu-id="8aa2f-135">Klikněte na **Vložit zástupný text**.</span><span class="sxs-lookup"><span data-stu-id="8aa2f-135">Click **Insert placeholder**.</span></span>
    3.  <span data-ttu-id="8aa2f-136">V nově otevřeném seznamu vyberte vkládaný zástupný text.</span><span class="sxs-lookup"><span data-stu-id="8aa2f-136">In the list that appears, select the placeholder to insert.</span></span>
    4.  <span data-ttu-id="8aa2f-137">Klepněte na tlačítko **Vložit**.</span><span class="sxs-lookup"><span data-stu-id="8aa2f-137">Click **Insert**.</span></span>

4.  <span data-ttu-id="8aa2f-138">Chcete-li přidat překlady pokynů, postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="8aa2f-138">To add translations of the instructions, follow these steps:</span></span>
    1.  <span data-ttu-id="8aa2f-139">Klikněte na **Překlady**.</span><span class="sxs-lookup"><span data-stu-id="8aa2f-139">Click **Translations**.</span></span>
    2.  <span data-ttu-id="8aa2f-140">Na nově otevřené stránce klikněte na **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="8aa2f-140">On the page that appears, click **Add**.</span></span>
    3.  <span data-ttu-id="8aa2f-141">V nově otevřeném seznamu vyberte jazyk, který chcete použít pro zadání textu.</span><span class="sxs-lookup"><span data-stu-id="8aa2f-141">In the list that appears, select the language that you will enter the text in.</span></span>
    4.  <span data-ttu-id="8aa2f-142">V poli **Přeložený text** zadejte text.</span><span class="sxs-lookup"><span data-stu-id="8aa2f-142">In the **Translated text** field, enter the text.</span></span>
    5.  <span data-ttu-id="8aa2f-143">Text můžete přizpůsobit vložením zástupného textu.</span><span class="sxs-lookup"><span data-stu-id="8aa2f-143">To personalize the text, you can insert placeholders.</span></span> <span data-ttu-id="8aa2f-144">Pokyny, jak zadat zástupný text, naleznete v kroku 3.</span><span class="sxs-lookup"><span data-stu-id="8aa2f-144">For instructions about how to enter a placeholder, see step 3.</span></span>
    6.  <span data-ttu-id="8aa2f-145">Klepněte na tlačítko **Zavřít**.</span><span class="sxs-lookup"><span data-stu-id="8aa2f-145">Click **Close**.</span></span>

## <a name="specify-when-this-workflow-is-used"></a><span data-ttu-id="8aa2f-146">Určete, kdy se má použít tento workflow.</span><span class="sxs-lookup"><span data-stu-id="8aa2f-146">Specify when this workflow is used</span></span>
<span data-ttu-id="8aa2f-147">Můžete vytvořit více workflowů založených na stejném typu.</span><span class="sxs-lookup"><span data-stu-id="8aa2f-147">You can create multiple workflows that are based on the same type.</span></span> <span data-ttu-id="8aa2f-148">Můžete například vytvořit workflow nákupních požadavků, pro každou zemi nebo oblast, ve které působíte, například Nákupní požadavky – Dánsko a Nákupní požadavky – Španělsko.</span><span class="sxs-lookup"><span data-stu-id="8aa2f-148">For example, you can create a purchase requisition workflow for each country/region that you operate in, such as Purchase Requisitions Denmark and Purchase Requisitions Spain.</span></span> <span data-ttu-id="8aa2f-149">Pokud máte více workflowů založených na stejném typu, je nutné zadat, kdy má být který workflow použit.</span><span class="sxs-lookup"><span data-stu-id="8aa2f-149">When you have multiple workflows that are based on the same type, you must specify when each workflow is used.</span></span> <span data-ttu-id="8aa2f-150">U předchozího příkladu zadáte následující podmínky:</span><span class="sxs-lookup"><span data-stu-id="8aa2f-150">For the preceding example, you specify the following conditions:</span></span>

-   <span data-ttu-id="8aa2f-151">Nákupní požadavky – Dánsko se má používat v případě, že země či oblast = DK</span><span class="sxs-lookup"><span data-stu-id="8aa2f-151">Purchase Requisitions Denmark is used when: country/region = DK</span></span>
-   <span data-ttu-id="8aa2f-152">Nákupní požadavky – Španělsko se má používat v případě, že země či oblast = ES</span><span class="sxs-lookup"><span data-stu-id="8aa2f-152">Purchase Requisitions Spain is used when: country/region = ES</span></span>

<span data-ttu-id="8aa2f-153">Pomocí následujících kroků zadejte, kdy se má použít workflow, který konfigurujete.</span><span class="sxs-lookup"><span data-stu-id="8aa2f-153">Follow these steps to specify when the workflow that you're configuring is used.</span></span>

1.  <span data-ttu-id="8aa2f-154">V levém podokně klikněte na **Aktivace**.</span><span class="sxs-lookup"><span data-stu-id="8aa2f-154">In the left pane, click **Activation**.</span></span>
2.  <span data-ttu-id="8aa2f-155">Označte pole **Nastavit podmínky pro spuštění tohoto workflowu**.</span><span class="sxs-lookup"><span data-stu-id="8aa2f-155">Select the **Set the conditions for running this workflow** check box.</span></span>
3.  <span data-ttu-id="8aa2f-156">Klepněte na možnost **Přidat podmínku**.</span><span class="sxs-lookup"><span data-stu-id="8aa2f-156">Click **Add condition**.</span></span>
4.  <span data-ttu-id="8aa2f-157">Zadání podmínky</span><span class="sxs-lookup"><span data-stu-id="8aa2f-157">Enter a condition.</span></span>
5.  <span data-ttu-id="8aa2f-158">Zadejte všechny další podmínky, které jsou požadovány.</span><span class="sxs-lookup"><span data-stu-id="8aa2f-158">Enter any additional conditions that are required.</span></span>
6.  <span data-ttu-id="8aa2f-159">Chcete-li ověřit, zda jsou zadané podmínky nastaveny správně, postupujte následovně:</span><span class="sxs-lookup"><span data-stu-id="8aa2f-159">To verify that the conditions that you entered are set correctly, follow these steps:</span></span>
    1.  <span data-ttu-id="8aa2f-160">Klepněte na možnost **Test**.</span><span class="sxs-lookup"><span data-stu-id="8aa2f-160">Click **Test**.</span></span>
    2.  <span data-ttu-id="8aa2f-161">Na stránce **Podmínka testovacího workflowu** v oblasti **Ověřit podmínku** vyberte záznam.</span><span class="sxs-lookup"><span data-stu-id="8aa2f-161">On the **Test workflow condition** page, in the **Validate condition** area, select a record.</span></span>
    3.  <span data-ttu-id="8aa2f-162">Klepněte na možnost **Test**.</span><span class="sxs-lookup"><span data-stu-id="8aa2f-162">Click **Test**.</span></span> <span data-ttu-id="8aa2f-163">Systém záznam vyhodnotí a určí, zda odpovídá zadaným podmínkám.</span><span class="sxs-lookup"><span data-stu-id="8aa2f-163">The system evaluates the record to determine whether it meets the conditions that you specified.</span></span> <span data-ttu-id="8aa2f-164">Například pokud vytváříte workflow nákupního požadavku pro Španělsko, oblast **Ověřit podmínku** na stránce bude obsahovat seznam nákupních žádanek.</span><span class="sxs-lookup"><span data-stu-id="8aa2f-164">For example, if you're creating a purchase requisition workflow for Spain, the **Validate condition** area of the page shows a list of purchase requisitions.</span></span> <span data-ttu-id="8aa2f-165">Po klepnutí na možnost **Test** systém vyhodnotí vybraný nákupní požadavek, aby zjistil, zda země či oblast = ES.</span><span class="sxs-lookup"><span data-stu-id="8aa2f-165">When you click **Test**, the system evaluates the selected purchase requisition to determine whether the country/region is ES.</span></span>
    4.  <span data-ttu-id="8aa2f-166">Klikněte na tlačítko **OK** nebo klepnutím na tlačítko **Storno** se vraťte na stránku **Vlastnosti**.</span><span class="sxs-lookup"><span data-stu-id="8aa2f-166">Click **OK** or **Cancel** to return to the **Properties** page.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="8aa2f-167">Zadejte, kdy se mají odesílat oznámení.</span><span class="sxs-lookup"><span data-stu-id="8aa2f-167">Specify when notifications are sent</span></span>
<span data-ttu-id="8aa2f-168">Když je dokument odeslán ke zpracování, je vytvořena instance workflowu.</span><span class="sxs-lookup"><span data-stu-id="8aa2f-168">When a document is submitted for processing, a workflow instance is created.</span></span> <span data-ttu-id="8aa2f-169">Uživatelům lze odeslat oznámení v případech, kdy jsou instance workflowu (na základě tohoto workflowu) spuštěny, dokončeny, zrušeny nebo zastaveny z důvodu chyby.</span><span class="sxs-lookup"><span data-stu-id="8aa2f-169">You can send notifications to users when workflow instances that are based on the workflow are started, completed, terminated, or stopped because of an error.</span></span> <span data-ttu-id="8aa2f-170">Pomocí následujících kroků můžete zadat, kdy mají být odeslána oznámení.</span><span class="sxs-lookup"><span data-stu-id="8aa2f-170">Follow these steps to specify when notifications are sent.</span></span>

1.  <span data-ttu-id="8aa2f-171">V levém podokně klikněte na **Oznámení**.</span><span class="sxs-lookup"><span data-stu-id="8aa2f-171">In the left pane, click **Notifications**.</span></span>
2.  <span data-ttu-id="8aa2f-172">Označte pole u každé události, která má spustit oznámení:</span><span class="sxs-lookup"><span data-stu-id="8aa2f-172">Select the check box for each event that should trigger notifications:</span></span>
    -   <span data-ttu-id="8aa2f-173">**Zahájeno** – odesílat oznámení při zahájení instance workflowu.</span><span class="sxs-lookup"><span data-stu-id="8aa2f-173">**Started** – Send notifications when a workflow instance is started.</span></span>
    -   <span data-ttu-id="8aa2f-174">**Zastaveno** – odesílat oznámení v případě, že je instance workflowu zastavena z důvodu chyby.</span><span class="sxs-lookup"><span data-stu-id="8aa2f-174">**Stopped** – Send notifications when a workflow instance is stopped because of an error.</span></span>
    -   <span data-ttu-id="8aa2f-175">**Dokončeno** – odesílat oznámení při dokončení instance workflowu.</span><span class="sxs-lookup"><span data-stu-id="8aa2f-175">**Completed** – Send notifications when a workflow instance is completed.</span></span>
    -   <span data-ttu-id="8aa2f-176">**Bez možnosti obnovy** – odesílat oznámení v případě, že je instance workflowu zastavena z důvodu neobnovitelné chyby.</span><span class="sxs-lookup"><span data-stu-id="8aa2f-176">**Unrecoverable** – Send notifications when a workflow instance is stopped because of an unrecoverable error.</span></span>
    -   <span data-ttu-id="8aa2f-177">**Ukončeno** – odesílat oznámení při ukončení instance workflowu.</span><span class="sxs-lookup"><span data-stu-id="8aa2f-177">**Terminated** – Send notifications when a workflow instance is terminated.</span></span>

3.  <span data-ttu-id="8aa2f-178">Vyberte řádek pro událost, kterou jste vybrali v kroku 2.</span><span class="sxs-lookup"><span data-stu-id="8aa2f-178">Select the row for an event that you selected in step 2.</span></span>
4.  <span data-ttu-id="8aa2f-179">Na kartě **Text oznámení** zadejte text oznámení.</span><span class="sxs-lookup"><span data-stu-id="8aa2f-179">On the **Notification text** tab, enter the text of the notification.</span></span>
5.  <span data-ttu-id="8aa2f-180">Text můžete přizpůsobit vložením zástupného textu.</span><span class="sxs-lookup"><span data-stu-id="8aa2f-180">To personalize the text, you can insert placeholders.</span></span> <span data-ttu-id="8aa2f-181">Zástupný text bude při zobrazení textu uživatelům nahrazen odpovídacími daty.</span><span class="sxs-lookup"><span data-stu-id="8aa2f-181">Placeholders are replaced with the appropriate data when the text is shown to users.</span></span> <span data-ttu-id="8aa2f-182">Při vkládání zástupného textu postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="8aa2f-182">To insert a placeholder, follow these steps:</span></span>
    1.  <span data-ttu-id="8aa2f-183">Klepnutím do pole zadejte, kde se má zástupný text zobrazit.</span><span class="sxs-lookup"><span data-stu-id="8aa2f-183">Click in the field to specify where the placeholder should appear.</span></span>
    2.  <span data-ttu-id="8aa2f-184">Klikněte na **Vložit zástupný text**.</span><span class="sxs-lookup"><span data-stu-id="8aa2f-184">Click **Insert placeholder**.</span></span>
    3.  <span data-ttu-id="8aa2f-185">V nově otevřeném seznamu vyberte vkládaný zástupný text.</span><span class="sxs-lookup"><span data-stu-id="8aa2f-185">In the list that appears, select the placeholder to insert.</span></span>
    4.  <span data-ttu-id="8aa2f-186">Klepněte na tlačítko **Vložit**.</span><span class="sxs-lookup"><span data-stu-id="8aa2f-186">Click **Insert**.</span></span>
    5.  <span data-ttu-id="8aa2f-187">Běžný zástupce za **Text oznámení**, který má byt zahrnut, je Poslední poznámky: %Workflow.Last note%", který zobrazuje všechny komentáře z předchozího kroku.</span><span class="sxs-lookup"><span data-stu-id="8aa2f-187">A common **Notification text** placeholder to include is "Last Notes: %Workflow.Last note%", which displays any comments from the previous step.</span></span>

6.  <span data-ttu-id="8aa2f-188">Chcete-li přidat překlady textu, postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="8aa2f-188">To add translations of the text, follow these steps:</span></span>
    1.  <span data-ttu-id="8aa2f-189">Klikněte na **Překlady**.</span><span class="sxs-lookup"><span data-stu-id="8aa2f-189">Click **Translations**.</span></span>
    2.  <span data-ttu-id="8aa2f-190">Na nově otevřené stránce klikněte na **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="8aa2f-190">On the page that appears, Click **Add**.</span></span>
    3.  <span data-ttu-id="8aa2f-191">V nově otevřeném seznamu vyberte jazyk, který chcete použít pro zadání textu.</span><span class="sxs-lookup"><span data-stu-id="8aa2f-191">In the list that appears, select the language that you will enter the text in.</span></span>
    4.  <span data-ttu-id="8aa2f-192">V poli **Přeložený text** zadejte text.</span><span class="sxs-lookup"><span data-stu-id="8aa2f-192">In the **Translated text** field, enter the text.</span></span>
    5.  <span data-ttu-id="8aa2f-193">Text můžete přizpůsobit vložením zástupného textu.</span><span class="sxs-lookup"><span data-stu-id="8aa2f-193">To personalize the text, you can insert placeholders.</span></span> <span data-ttu-id="8aa2f-194">Pokyny, jak zadat zástupný text, naleznete v kroku 5.</span><span class="sxs-lookup"><span data-stu-id="8aa2f-194">For instructions about how to enter a placeholder, see step 5.</span></span>
    6.  <span data-ttu-id="8aa2f-195">Klepněte na tlačítko **Zavřít**.</span><span class="sxs-lookup"><span data-stu-id="8aa2f-195">Click **Close**.</span></span>

7.  <span data-ttu-id="8aa2f-196">Na kartě **Příjemce** použijte následující možnosti k určení příjemce oznámení.</span><span class="sxs-lookup"><span data-stu-id="8aa2f-196">On the **Recipient** tab, use the following options to specify who should receive the notifications.</span></span>
    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="8aa2f-197">Možnost</span><span class="sxs-lookup"><span data-stu-id="8aa2f-197">Option</span></span></th>
    <th><span data-ttu-id="8aa2f-198">Oznámení bude odesláno těmto uživatelům</span><span class="sxs-lookup"><span data-stu-id="8aa2f-198">Notifications are sent to these users</span></span></th>
    <th><span data-ttu-id="8aa2f-199">Při odesílání oznámení postupujte takto</span><span class="sxs-lookup"><span data-stu-id="8aa2f-199">To send notifications, follow these steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="8aa2f-200">Účastník</span><span class="sxs-lookup"><span data-stu-id="8aa2f-200">Participant</span></span></td>
    <td><span data-ttu-id="8aa2f-201">Uživatelé, kteří jsou přiřazeni k určité skupině nebo roli</span><span class="sxs-lookup"><span data-stu-id="8aa2f-201">Users who are assigned to a specific group or role</span></span></td>
    <td><ol>
    <li><span data-ttu-id="8aa2f-202">Na kartě <strong>Příjemce</strong> klepněte na možnost <strong>Účastník</strong>.</span><span class="sxs-lookup"><span data-stu-id="8aa2f-202">On the <strong>Recipient</strong> tab, click <strong>Participant</strong>.</span></span></li>
    <li><span data-ttu-id="8aa2f-203">Na kartě <strong>Založeno na roli</strong> v seznamu <strong>Typ účastníka</strong> vyberte typ skupiny nebo role, které chcete oznámení odeslat.</span><span class="sxs-lookup"><span data-stu-id="8aa2f-203">On the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="8aa2f-204">V seznamu <strong>Účastník</strong> vyberte skupinu nebo roli, které chcete oznámení odeslat.</span><span class="sxs-lookup"><span data-stu-id="8aa2f-204">In the <strong>Participant</strong> list, select the group or role to send notifications to.</span></span></li>
    </ol></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="8aa2f-205">Uživatel workflowu</span><span class="sxs-lookup"><span data-stu-id="8aa2f-205">Workflow user</span></span></td>
    <td><span data-ttu-id="8aa2f-206">Uživatelé, kteří jsou účastníci tohoto workflowu</span><span class="sxs-lookup"><span data-stu-id="8aa2f-206">Users who are participants in this workflow</span></span></td>
    <td><ol>
    <li><span data-ttu-id="8aa2f-207">Na kartě <strong>Příjemce</strong> klepněte na možnost <strong>Uživatel workflowu</strong>.</span><span class="sxs-lookup"><span data-stu-id="8aa2f-207">On the <strong>Recipient</strong> tab, click <strong>Workflow user</strong>.</span></span></li>
    <li><span data-ttu-id="8aa2f-208">Na kartě <strong>Uživatel workflowu</strong> v seznamu <strong>Uživatel workflowu</strong> vyberte účastníka tohoto workflowu.</span><span class="sxs-lookup"><span data-stu-id="8aa2f-208">On the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a participant in this workflow.</span></span></li>
    </ol></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="8aa2f-209">Uživatel</span><span class="sxs-lookup"><span data-stu-id="8aa2f-209">User</span></span></td>
    <td><span data-ttu-id="8aa2f-210">Konkrétní uživatelé aplikace Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="8aa2f-210">Specific Finance and Operations users</span></span></td>
    <td><ol>
    <li><span data-ttu-id="8aa2f-211">Na kartě <strong>Příjemce</strong> klepněte na možnost <strong>Uživatel</strong>.</span><span class="sxs-lookup"><span data-stu-id="8aa2f-211">On the <strong>Recipient</strong> tab, click <strong>User</strong>.</span></span></li>
    <li><span data-ttu-id="8aa2f-212">Na kartě <strong>Uživatel</strong> obsahuje seznam <strong>Dostupní uživatelé</strong> všechny uživatele aplikace Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="8aa2f-212">On the <strong>User</strong> tab, the <strong>Available users</strong> list includes all Finance and Operations users.</span></span> <span data-ttu-id="8aa2f-213">Vyberte uživatele, kterým chcete odeslat oznámení, a pak přesuňte tyto uživatele do seznamu <strong>Vybraní uživatelé</strong>.</span><span class="sxs-lookup"><span data-stu-id="8aa2f-213">Select the users to send notifications to, and move those users into the <strong>Selected users</strong> list.</span></span></li>
    </ol></td>
    </tr>
    </tbody>
    </table>

8.  <span data-ttu-id="8aa2f-214">Zopakujte kroky 3 až 7 pro každou událost, kterou jste vybrali v kroku 2.</span><span class="sxs-lookup"><span data-stu-id="8aa2f-214">Repeat steps 3 through 7 for each event that you selected in step 2.</span></span>

## <a name="enter-comments-about-the-changes-that-you-made-to-the-workflow"></a><span data-ttu-id="8aa2f-215">Zadejte komentáře ke změnám provedeným v daném workflowu</span><span class="sxs-lookup"><span data-stu-id="8aa2f-215">Enter comments about the changes that you made to the workflow</span></span>
<span data-ttu-id="8aa2f-216">Chcete-li zadat komentáře ke změnám provedeným u tohoto workflowu, proveďte následující kroky.</span><span class="sxs-lookup"><span data-stu-id="8aa2f-216">To enter comments about the changes that you made to the workflow, follow these steps.</span></span>

1.  <span data-ttu-id="8aa2f-217">V levém podokně klikněte na **Poznámky**.</span><span class="sxs-lookup"><span data-stu-id="8aa2f-217">In the left pane, click **Notes**.</span></span>
2.  <span data-ttu-id="8aa2f-218">V poli **Zadat komentáře k workflowu** zadejte své poznámky.</span><span class="sxs-lookup"><span data-stu-id="8aa2f-218">In the **Enter comments about the workflow** field, enter your comments.</span></span>
3.  <span data-ttu-id="8aa2f-219">Zkontrolujte své komentáře.</span><span class="sxs-lookup"><span data-stu-id="8aa2f-219">Review your comments.</span></span> <span data-ttu-id="8aa2f-220">Po přidání komentáře je již nelze upravit.</span><span class="sxs-lookup"><span data-stu-id="8aa2f-220">After you add comments, you can't modify them.</span></span>
4.  <span data-ttu-id="8aa2f-221">Kliknutím na **Přidat** přidáte komentáře do oblasti **Historie poznámek**.</span><span class="sxs-lookup"><span data-stu-id="8aa2f-221">Click **Add** to add your comments to the **Comment history** area.</span></span>





