---
title: "Konfigurace vlastností workflowu"
description: "Toto téma vysvětluje, jak nakonfigurovat různé vlastnosti workflowu."
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
ms.custom: 196083
ms.assetid: 192b7a98-7d04-4c7a-a986-29d797a8a837
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 5c24f6555508272b65aeb81c5a16a0bd2407f1b4
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="configure-the-properties-of-a-workflow"></a><span data-ttu-id="a1980-103">Konfigurace vlastností workflowu</span><span class="sxs-lookup"><span data-stu-id="a1980-103">Configure the properties of a workflow</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="a1980-104">Toto téma vysvětluje, jak nakonfigurovat různé vlastnosti workflowu.</span><span class="sxs-lookup"><span data-stu-id="a1980-104">This topic explains how to configure the various properties of a workflow.</span></span>

<span data-ttu-id="a1980-105">Pokud chcete konfigurovat vlastnosti workflowu, otevřete workflow v editoru workflowu.</span><span class="sxs-lookup"><span data-stu-id="a1980-105">To configure the properties of a workflow, open the workflow in the workflow editor.</span></span> <span data-ttu-id="a1980-106">Klikněte na plátno editoru workflowu a klepněte na tlačítko **Vlastnosti** k otevření stránky **Vlastnosti**.</span><span class="sxs-lookup"><span data-stu-id="a1980-106">Click the canvas of the workflow editor, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="a1980-107">Pro konfiguraci vlastností workflowu můžete použít následující kroky.</span><span class="sxs-lookup"><span data-stu-id="a1980-107">You can then use the following procedures to configure the various properties of the workflow.</span></span>

## <a name="name-the-workflow"></a><span data-ttu-id="a1980-108">Pojmenování workflowu</span><span class="sxs-lookup"><span data-stu-id="a1980-108">Name the workflow</span></span>
<span data-ttu-id="a1980-109">Pomocí následujících kroků zadejte název workflowu.</span><span class="sxs-lookup"><span data-stu-id="a1980-109">Follow these steps to enter a name for the workflow.</span></span>

1.  <span data-ttu-id="a1980-110">V levém podokně klepněte na tlačítko **Základní nastavení**.</span><span class="sxs-lookup"><span data-stu-id="a1980-110">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="a1980-111">V poli **Název** zadejte jedinečný název workflowu.</span><span class="sxs-lookup"><span data-stu-id="a1980-111">In the **Name** field, enter a unique name for the workflow.</span></span> <span data-ttu-id="a1980-112">Předpokládejme například, že vytváříte workflowy nákupních požadavků pro každou zemi nebo oblast, ve které působíte. Pro workflow nákupního požadavku můžete například zadat název **Nákupní požadavky – Dánsko** nebo **Nákupní požadavky – Španělsko**.</span><span class="sxs-lookup"><span data-stu-id="a1980-112">For example, if you create a purchase requisition workflow for each country/region that you operate in, you can name the purchase requisition workflow **Purchase Requisitions Denmark** or **Purchase Requisitions Spain**.</span></span>

## <a name="specify-the-workflow-owner"></a><span data-ttu-id="a1980-113">Zadání vlastníka workflowu</span><span class="sxs-lookup"><span data-stu-id="a1980-113">Specify the workflow owner</span></span>
<span data-ttu-id="a1980-114">Vlastník workflowu je osoba, která bude spravovat workflow.</span><span class="sxs-lookup"><span data-stu-id="a1980-114">The workflow owner is the person who manages and maintains the workflow.</span></span> <span data-ttu-id="a1980-115">Vlastníka workflowu můžete zadat provedením následujícího postupu.</span><span class="sxs-lookup"><span data-stu-id="a1980-115">Follow these steps to specify the workflow owner.</span></span>

1.  <span data-ttu-id="a1980-116">V levém podokně klepněte na tlačítko **Základní nastavení**.</span><span class="sxs-lookup"><span data-stu-id="a1980-116">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="a1980-117">V seznamu **Vlastník** vyberte jméno osoby, který bude spravovat tento workflow.</span><span class="sxs-lookup"><span data-stu-id="a1980-117">In the **Owner** list, select the name of the person who will manage the workflow.</span></span>

## <a name="select-an-email-template"></a><span data-ttu-id="a1980-118">Výběr šablony e-mailu</span><span class="sxs-lookup"><span data-stu-id="a1980-118">Select an email template</span></span>
<span data-ttu-id="a1980-119">Podle těchto kroků vyberte šablonu e-mailu, která se používá k vytvoření oznámení o workflowu.</span><span class="sxs-lookup"><span data-stu-id="a1980-119">Follow these steps to select the email template that is used to generate notification messages about the workflow.</span></span>

1.  <span data-ttu-id="a1980-120">V levém podokně klepněte na tlačítko **Základní nastavení**.</span><span class="sxs-lookup"><span data-stu-id="a1980-120">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="a1980-121">V seznamu **Šablona e-mailu k oznámení pro workflow** vyberte šablonu.</span><span class="sxs-lookup"><span data-stu-id="a1980-121">In the **Email template for workflow notifications** list, select the template.</span></span>

## <a name="enter-instructions-for-users"></a><span data-ttu-id="a1980-122">Zadání pokynů pro uživatele</span><span class="sxs-lookup"><span data-stu-id="a1980-122">Enter instructions for users</span></span>
<span data-ttu-id="a1980-123">Můžete zadat pokyny pro uživatele, kteří budou odesílat dokumenty ke zpracování a schválení.</span><span class="sxs-lookup"><span data-stu-id="a1980-123">You can provide instructions to users who submit documents for processing and approval.</span></span> <span data-ttu-id="a1980-124">Tito uživatelé jsou označovány jako *původci*.</span><span class="sxs-lookup"><span data-stu-id="a1980-124">These users are also referred to as *originators*.</span></span> <span data-ttu-id="a1980-125">Budeme například předpokládat, že vytváříte workflow nákupní žádanky, a že jste zadali pokyny.</span><span class="sxs-lookup"><span data-stu-id="a1980-125">For example, you're creating a purchase requisition workflow, and you enter instructions.</span></span> <span data-ttu-id="a1980-126">Tyto pokyny mohou zobrazit uživatelé zadáním nákupního požadavku na stránce **Nákupní požadavky**.</span><span class="sxs-lookup"><span data-stu-id="a1980-126">Those instructions can then be viewed by users who enter purchase requisitions on the **Purchase requisitions** page.</span></span> <span data-ttu-id="a1980-127">Původce může zobrazit pokyny klepnutím na příslušnou ikonu na panelu zpráv pro workflow.</span><span class="sxs-lookup"><span data-stu-id="a1980-127">To view instructions, the originator clicks the icon in the workflow message bar.</span></span> <span data-ttu-id="a1980-128">Pokyny pro uživatele můžete zadat provedením následujícího postupu.</span><span class="sxs-lookup"><span data-stu-id="a1980-128">Follow these steps to enter instructions for users.</span></span>

1.  <span data-ttu-id="a1980-129">V levém podokně klepněte na tlačítko **Základní nastavení**.</span><span class="sxs-lookup"><span data-stu-id="a1980-129">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="a1980-130">V poli **Pokyny pro odeslání** zadejte pokyny.</span><span class="sxs-lookup"><span data-stu-id="a1980-130">In the **Submission instructions** field, enter the instructions.</span></span>
3.  <span data-ttu-id="a1980-131">Pokyny můžete přizpůsobit vložením zástupného textu.</span><span class="sxs-lookup"><span data-stu-id="a1980-131">To personalize the instructions, you can insert placeholders.</span></span> <span data-ttu-id="a1980-132">Zástupný text bude při zobrazení pokynů uživatelům nahrazen odpovídacími daty.</span><span class="sxs-lookup"><span data-stu-id="a1980-132">Placeholders are replaced with the appropriate data when the instructions are shown to users.</span></span> <span data-ttu-id="a1980-133">Při vkládání zástupného textu postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="a1980-133">To insert a placeholder, follow these steps:</span></span>
    1.  <span data-ttu-id="a1980-134">Klepnutím v poli **Pokyny pro odeslání** zadejte, kde se má zástupný text zobrazit.</span><span class="sxs-lookup"><span data-stu-id="a1980-134">Click in the **Submission instructions** field to specify where the placeholder should appear.</span></span>
    2.  <span data-ttu-id="a1980-135">Klikněte na **Vložit zástupný text**.</span><span class="sxs-lookup"><span data-stu-id="a1980-135">Click **Insert placeholder**.</span></span>
    3.  <span data-ttu-id="a1980-136">V nově otevřeném seznamu vyberte vkládaný zástupný text.</span><span class="sxs-lookup"><span data-stu-id="a1980-136">In the list that appears, select the placeholder to insert.</span></span>
    4.  <span data-ttu-id="a1980-137">Klepněte na tlačítko **Vložit**.</span><span class="sxs-lookup"><span data-stu-id="a1980-137">Click **Insert**.</span></span>

4.  <span data-ttu-id="a1980-138">Chcete-li přidat překlady pokynů, postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="a1980-138">To add translations of the instructions, follow these steps:</span></span>
    1.  <span data-ttu-id="a1980-139">Klikněte na **Překlady**.</span><span class="sxs-lookup"><span data-stu-id="a1980-139">Click **Translations**.</span></span>
    2.  <span data-ttu-id="a1980-140">Na nově otevřené stránce klikněte na **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="a1980-140">On the page that appears, click **Add**.</span></span>
    3.  <span data-ttu-id="a1980-141">V nově otevřeném seznamu vyberte jazyk, který chcete použít pro zadání textu.</span><span class="sxs-lookup"><span data-stu-id="a1980-141">In the list that appears, select the language that you will enter the text in.</span></span>
    4.  <span data-ttu-id="a1980-142">V poli **Přeložený text** zadejte text.</span><span class="sxs-lookup"><span data-stu-id="a1980-142">In the **Translated text** field, enter the text.</span></span>
    5.  <span data-ttu-id="a1980-143">Text můžete přizpůsobit vložením zástupného textu.</span><span class="sxs-lookup"><span data-stu-id="a1980-143">To personalize the text, you can insert placeholders.</span></span> <span data-ttu-id="a1980-144">Pokyny, jak zadat zástupný text, naleznete v kroku 3.</span><span class="sxs-lookup"><span data-stu-id="a1980-144">For instructions about how to enter a placeholder, see step 3.</span></span>
    6.  <span data-ttu-id="a1980-145">Klepněte na tlačítko **Zavřít**.</span><span class="sxs-lookup"><span data-stu-id="a1980-145">Click **Close**.</span></span>

## <a name="specify-when-this-workflow-is-used"></a><span data-ttu-id="a1980-146">Určete, kdy se má použít tento workflow.</span><span class="sxs-lookup"><span data-stu-id="a1980-146">Specify when this workflow is used</span></span>
<span data-ttu-id="a1980-147">Můžete vytvořit více workflowů založených na stejném typu.</span><span class="sxs-lookup"><span data-stu-id="a1980-147">You can create multiple workflows that are based on the same type.</span></span> <span data-ttu-id="a1980-148">Můžete například vytvořit workflow nákupních požadavků, pro každou zemi nebo oblast, ve které působíte, například Nákupní požadavky – Dánsko a Nákupní požadavky – Španělsko.</span><span class="sxs-lookup"><span data-stu-id="a1980-148">For example, you can create a purchase requisition workflow for each country/region that you operate in, such as Purchase Requisitions Denmark and Purchase Requisitions Spain.</span></span> <span data-ttu-id="a1980-149">Pokud máte více workflowů založených na stejném typu, je nutné zadat, kdy má být který workflow použit.</span><span class="sxs-lookup"><span data-stu-id="a1980-149">When you have multiple workflows that are based on the same type, you must specify when each workflow is used.</span></span> <span data-ttu-id="a1980-150">U předchozího příkladu zadáte následující podmínky:</span><span class="sxs-lookup"><span data-stu-id="a1980-150">For the preceding example, you specify the following conditions:</span></span>

-   <span data-ttu-id="a1980-151">Nákupní požadavky – Dánsko se má používat v případě, že země či oblast = DK</span><span class="sxs-lookup"><span data-stu-id="a1980-151">Purchase Requisitions Denmark is used when: country/region = DK</span></span>
-   <span data-ttu-id="a1980-152">Nákupní požadavky – Španělsko se má používat v případě, že země či oblast = ES</span><span class="sxs-lookup"><span data-stu-id="a1980-152">Purchase Requisitions Spain is used when: country/region = ES</span></span>

<span data-ttu-id="a1980-153">Pomocí následujících kroků zadejte, kdy se má použít workflow, který konfigurujete.</span><span class="sxs-lookup"><span data-stu-id="a1980-153">Follow these steps to specify when the workflow that you're configuring is used.</span></span>

1.  <span data-ttu-id="a1980-154">V levém podokně klikněte na **Aktivace**.</span><span class="sxs-lookup"><span data-stu-id="a1980-154">In the left pane, click **Activation**.</span></span>
2.  <span data-ttu-id="a1980-155">Označte pole **Nastavit podmínky pro spuštění tohoto workflowu**.</span><span class="sxs-lookup"><span data-stu-id="a1980-155">Select the **Set the conditions for running this workflow** check box.</span></span>
3.  <span data-ttu-id="a1980-156">Klepněte na možnost **Přidat podmínku**.</span><span class="sxs-lookup"><span data-stu-id="a1980-156">Click **Add condition**.</span></span>
4.  <span data-ttu-id="a1980-157">Zadání podmínky</span><span class="sxs-lookup"><span data-stu-id="a1980-157">Enter a condition.</span></span>
5.  <span data-ttu-id="a1980-158">Zadejte všechny další podmínky, které jsou požadovány.</span><span class="sxs-lookup"><span data-stu-id="a1980-158">Enter any additional conditions that are required.</span></span>
6.  <span data-ttu-id="a1980-159">Chcete-li ověřit, zda jsou zadané podmínky nastaveny správně, postupujte následovně:</span><span class="sxs-lookup"><span data-stu-id="a1980-159">To verify that the conditions that you entered are set correctly, follow these steps:</span></span>
    1.  <span data-ttu-id="a1980-160">Klepněte na možnost **Test**.</span><span class="sxs-lookup"><span data-stu-id="a1980-160">Click **Test**.</span></span>
    2.  <span data-ttu-id="a1980-161">Na stránce **Podmínka testovacího workflowu** v oblasti **Ověřit podmínku** vyberte záznam.</span><span class="sxs-lookup"><span data-stu-id="a1980-161">On the **Test workflow condition** page, in the **Validate condition** area, select a record.</span></span>
    3.  <span data-ttu-id="a1980-162">Klepněte na možnost **Test**.</span><span class="sxs-lookup"><span data-stu-id="a1980-162">Click **Test**.</span></span> <span data-ttu-id="a1980-163">Systém záznam vyhodnotí a určí, zda odpovídá zadaným podmínkám.</span><span class="sxs-lookup"><span data-stu-id="a1980-163">The system evaluates the record to determine whether it meets the conditions that you specified.</span></span> <span data-ttu-id="a1980-164">Například pokud vytváříte workflow nákupního požadavku pro Španělsko, oblast **Ověřit podmínku** na stránce bude obsahovat seznam nákupních žádanek.</span><span class="sxs-lookup"><span data-stu-id="a1980-164">For example, if you're creating a purchase requisition workflow for Spain, the **Validate condition** area of the page shows a list of purchase requisitions.</span></span> <span data-ttu-id="a1980-165">Po klepnutí na možnost **Test** systém vyhodnotí vybraný nákupní požadavek, aby zjistil, zda země či oblast = ES.</span><span class="sxs-lookup"><span data-stu-id="a1980-165">When you click **Test**, the system evaluates the selected purchase requisition to determine whether the country/region is ES.</span></span>
    4.  <span data-ttu-id="a1980-166">Klikněte na tlačítko **OK** nebo klepnutím na tlačítko **Storno** se vraťte na stránku **Vlastnosti**.</span><span class="sxs-lookup"><span data-stu-id="a1980-166">Click **OK** or **Cancel** to return to the **Properties** page.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="a1980-167">Zadejte, kdy se mají odesílat oznámení.</span><span class="sxs-lookup"><span data-stu-id="a1980-167">Specify when notifications are sent</span></span>
<span data-ttu-id="a1980-168">Když je dokument odeslán ke zpracování, je vytvořena instance workflowu.</span><span class="sxs-lookup"><span data-stu-id="a1980-168">When a document is submitted for processing, a workflow instance is created.</span></span> <span data-ttu-id="a1980-169">Uživatelům lze odeslat oznámení v případech, kdy jsou instance workflowu (na základě tohoto workflowu) spuštěny, dokončeny, zrušeny nebo zastaveny z důvodu chyby.</span><span class="sxs-lookup"><span data-stu-id="a1980-169">You can send notifications to users when workflow instances that are based on the workflow are started, completed, terminated, or stopped because of an error.</span></span> <span data-ttu-id="a1980-170">Pomocí následujících kroků můžete zadat, kdy mají být odeslána oznámení.</span><span class="sxs-lookup"><span data-stu-id="a1980-170">Follow these steps to specify when notifications are sent.</span></span>

1.  <span data-ttu-id="a1980-171">V levém podokně klikněte na **Oznámení**.</span><span class="sxs-lookup"><span data-stu-id="a1980-171">In the left pane, click **Notifications**.</span></span>
2.  <span data-ttu-id="a1980-172">Označte pole u každé události, která má spustit oznámení:</span><span class="sxs-lookup"><span data-stu-id="a1980-172">Select the check box for each event that should trigger notifications:</span></span>
    -   <span data-ttu-id="a1980-173">**Zahájeno** – odesílat oznámení při zahájení instance workflowu.</span><span class="sxs-lookup"><span data-stu-id="a1980-173">**Started** – Send notifications when a workflow instance is started.</span></span>
    -   <span data-ttu-id="a1980-174">**Zastaveno** – odesílat oznámení v případě, že je instance workflowu zastavena z důvodu chyby.</span><span class="sxs-lookup"><span data-stu-id="a1980-174">**Stopped** – Send notifications when a workflow instance is stopped because of an error.</span></span>
    -   <span data-ttu-id="a1980-175">**Dokončeno** – odesílat oznámení při dokončení instance workflowu.</span><span class="sxs-lookup"><span data-stu-id="a1980-175">**Completed** – Send notifications when a workflow instance is completed.</span></span>
    -   <span data-ttu-id="a1980-176">**Bez možnosti obnovy** – odesílat oznámení v případě, že je instance workflowu zastavena z důvodu neobnovitelné chyby.</span><span class="sxs-lookup"><span data-stu-id="a1980-176">**Unrecoverable** – Send notifications when a workflow instance is stopped because of an unrecoverable error.</span></span>
    -   <span data-ttu-id="a1980-177">**Ukončeno** – odesílat oznámení při ukončení instance workflowu.</span><span class="sxs-lookup"><span data-stu-id="a1980-177">**Terminated** – Send notifications when a workflow instance is terminated.</span></span>

3.  <span data-ttu-id="a1980-178">Vyberte řádek pro událost, kterou jste vybrali v kroku 2.</span><span class="sxs-lookup"><span data-stu-id="a1980-178">Select the row for an event that you selected in step 2.</span></span>
4.  <span data-ttu-id="a1980-179">Na kartě **Text oznámení** zadejte text oznámení.</span><span class="sxs-lookup"><span data-stu-id="a1980-179">On the **Notification text** tab, enter the text of the notification.</span></span>
5.  <span data-ttu-id="a1980-180">Text můžete přizpůsobit vložením zástupného textu.</span><span class="sxs-lookup"><span data-stu-id="a1980-180">To personalize the text, you can insert placeholders.</span></span> <span data-ttu-id="a1980-181">Zástupný text bude při zobrazení textu uživatelům nahrazen odpovídacími daty.</span><span class="sxs-lookup"><span data-stu-id="a1980-181">Placeholders are replaced with the appropriate data when the text is shown to users.</span></span> <span data-ttu-id="a1980-182">Při vkládání zástupného textu postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="a1980-182">To insert a placeholder, follow these steps:</span></span>
    1.  <span data-ttu-id="a1980-183">Klepnutím do pole zadejte, kde se má zástupný text zobrazit.</span><span class="sxs-lookup"><span data-stu-id="a1980-183">Click in the field to specify where the placeholder should appear.</span></span>
    2.  <span data-ttu-id="a1980-184">Klikněte na **Vložit zástupný text**.</span><span class="sxs-lookup"><span data-stu-id="a1980-184">Click **Insert placeholder**.</span></span>
    3.  <span data-ttu-id="a1980-185">V nově otevřeném seznamu vyberte vkládaný zástupný text.</span><span class="sxs-lookup"><span data-stu-id="a1980-185">In the list that appears, select the placeholder to insert.</span></span>
    4.  <span data-ttu-id="a1980-186">Klepněte na tlačítko **Vložit**.</span><span class="sxs-lookup"><span data-stu-id="a1980-186">Click **Insert**.</span></span>

6.  <span data-ttu-id="a1980-187">Chcete-li přidat překlady textu, postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="a1980-187">To add translations of the text, follow these steps:</span></span>
    1.  <span data-ttu-id="a1980-188">Klikněte na **Překlady**.</span><span class="sxs-lookup"><span data-stu-id="a1980-188">Click **Translations**.</span></span>
    2.  <span data-ttu-id="a1980-189">Na nově otevřené stránce klikněte na **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="a1980-189">On the page that appears, Click **Add**.</span></span>
    3.  <span data-ttu-id="a1980-190">V nově otevřeném seznamu vyberte jazyk, který chcete použít pro zadání textu.</span><span class="sxs-lookup"><span data-stu-id="a1980-190">In the list that appears, select the language that you will enter the text in.</span></span>
    4.  <span data-ttu-id="a1980-191">V poli **Přeložený text** zadejte text.</span><span class="sxs-lookup"><span data-stu-id="a1980-191">In the **Translated text** field, enter the text.</span></span>
    5.  <span data-ttu-id="a1980-192">Text můžete přizpůsobit vložením zástupného textu.</span><span class="sxs-lookup"><span data-stu-id="a1980-192">To personalize the text, you can insert placeholders.</span></span> <span data-ttu-id="a1980-193">Pokyny, jak zadat zástupný text, naleznete v kroku 5.</span><span class="sxs-lookup"><span data-stu-id="a1980-193">For instructions about how to enter a placeholder, see step 5.</span></span>
    6.  <span data-ttu-id="a1980-194">Klepněte na tlačítko **Zavřít**.</span><span class="sxs-lookup"><span data-stu-id="a1980-194">Click **Close**.</span></span>

7.  <span data-ttu-id="a1980-195">Na kartě **Příjemce** použijte následující možnosti k určení příjemce oznámení.</span><span class="sxs-lookup"><span data-stu-id="a1980-195">On the **Recipient** tab, use the following options to specify who should receive the notifications.</span></span>
    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="a1980-196">Možnost</span><span class="sxs-lookup"><span data-stu-id="a1980-196">Option</span></span></th>
    <th><span data-ttu-id="a1980-197">Oznámení bude odesláno těmto uživatelům</span><span class="sxs-lookup"><span data-stu-id="a1980-197">Notifications are sent to these users</span></span></th>
    <th><span data-ttu-id="a1980-198">Při odesílání oznámení postupujte takto</span><span class="sxs-lookup"><span data-stu-id="a1980-198">To send notifications, follow these steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="a1980-199">Účastník</span><span class="sxs-lookup"><span data-stu-id="a1980-199">Participant</span></span></td>
    <td><span data-ttu-id="a1980-200">Uživatelé, kteří jsou přiřazeni k určité skupině nebo roli</span><span class="sxs-lookup"><span data-stu-id="a1980-200">Users who are assigned to a specific group or role</span></span></td>
    <td><ol>
    <li><span data-ttu-id="a1980-201">Na kartě <strong>Příjemce</strong> klepněte na možnost <strong>Účastník</strong>.</span><span class="sxs-lookup"><span data-stu-id="a1980-201">On the <strong>Recipient</strong> tab, click <strong>Participant</strong>.</span></span></li>
    <li><span data-ttu-id="a1980-202">Na kartě <strong>Založeno na roli</strong> v seznamu <strong>Typ účastníka</strong> vyberte typ skupiny nebo role, které chcete oznámení odeslat.</span><span class="sxs-lookup"><span data-stu-id="a1980-202">On the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="a1980-203">V seznamu <strong>Účastník</strong> vyberte skupinu nebo roli, které chcete oznámení odeslat.</span><span class="sxs-lookup"><span data-stu-id="a1980-203">In the <strong>Participant</strong> list, select the group or role to send notifications to.</span></span></li>
    </ol></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="a1980-204">Uživatel workflowu</span><span class="sxs-lookup"><span data-stu-id="a1980-204">Workflow user</span></span></td>
    <td><span data-ttu-id="a1980-205">Uživatelé, kteří jsou účastníci tohoto workflowu</span><span class="sxs-lookup"><span data-stu-id="a1980-205">Users who are participants in this workflow</span></span></td>
    <td><ol>
    <li><span data-ttu-id="a1980-206">Na kartě <strong>Příjemce</strong> klepněte na možnost <strong>Uživatel workflowu</strong>.</span><span class="sxs-lookup"><span data-stu-id="a1980-206">On the <strong>Recipient</strong> tab, click <strong>Workflow user</strong>.</span></span></li>
    <li><span data-ttu-id="a1980-207">Na kartě <strong>Uživatel workflowu</strong> v seznamu <strong>Uživatel workflowu</strong> vyberte účastníka tohoto workflowu.</span><span class="sxs-lookup"><span data-stu-id="a1980-207">On the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a participant in this workflow.</span></span></li>
    </ol></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="a1980-208">Uživatel</span><span class="sxs-lookup"><span data-stu-id="a1980-208">User</span></span></td>
    <td><span data-ttu-id="a1980-209">Konkrétní uživatelé aplikace Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a1980-209">Specific Finance and Operations users</span></span></td>
    <td><ol>
    <li><span data-ttu-id="a1980-210">Na kartě <strong>Příjemce</strong> klepněte na možnost <strong>Uživatel</strong>.</span><span class="sxs-lookup"><span data-stu-id="a1980-210">On the <strong>Recipient</strong> tab, click <strong>User</strong>.</span></span></li>
    <li><span data-ttu-id="a1980-211">Na kartě <strong>Uživatel</strong> obsahuje seznam <strong>Dostupní uživatelé</strong> všechny uživatele aplikace Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a1980-211">On the <strong>User</strong> tab, the <strong>Available users</strong> list includes all Finance and Operations users.</span></span> <span data-ttu-id="a1980-212">Vyberte uživatele, kterým chcete odeslat oznámení, a pak přesuňte tyto uživatele do seznamu <strong>Vybraní uživatelé</strong>.</span><span class="sxs-lookup"><span data-stu-id="a1980-212">Select the users to send notifications to, and move those users into the <strong>Selected users</strong> list.</span></span></li>
    </ol></td>
    </tr>
    </tbody>
    </table>

8.  <span data-ttu-id="a1980-213">Zopakujte kroky 3 až 7 pro každou událost, kterou jste vybrali v kroku 2.</span><span class="sxs-lookup"><span data-stu-id="a1980-213">Repeat steps 3 through 7 for each event that you selected in step 2.</span></span>

## <a name="enter-comments-about-the-changes-that-you-made-to-the-workflow"></a><span data-ttu-id="a1980-214">Zadejte komentáře ke změnám provedeným v daném workflowu</span><span class="sxs-lookup"><span data-stu-id="a1980-214">Enter comments about the changes that you made to the workflow</span></span>
<span data-ttu-id="a1980-215">Chcete-li zadat komentáře ke změnám provedeným u tohoto workflowu, proveďte následující kroky.</span><span class="sxs-lookup"><span data-stu-id="a1980-215">To enter comments about the changes that you made to the workflow, follow these steps.</span></span>

1.  <span data-ttu-id="a1980-216">V levém podokně klikněte na **Poznámky**.</span><span class="sxs-lookup"><span data-stu-id="a1980-216">In the left pane, click **Notes**.</span></span>
2.  <span data-ttu-id="a1980-217">V poli **Zadat komentáře k workflowu** zadejte své poznámky.</span><span class="sxs-lookup"><span data-stu-id="a1980-217">In the **Enter comments about the workflow** field, enter your comments.</span></span>
3.  <span data-ttu-id="a1980-218">Zkontrolujte své komentáře.</span><span class="sxs-lookup"><span data-stu-id="a1980-218">Review your comments.</span></span> <span data-ttu-id="a1980-219">Po přidání komentáře je již nelze upravit.</span><span class="sxs-lookup"><span data-stu-id="a1980-219">After you add comments, you can't modify them.</span></span>
4.  <span data-ttu-id="a1980-220">Kliknutím na **Přidat** přidáte komentáře do oblasti **Historie poznámek**.</span><span class="sxs-lookup"><span data-stu-id="a1980-220">Click **Add** to add your comments to the **Comment history** area.</span></span>





