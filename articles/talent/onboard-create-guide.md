---
title: Vytvoření a odeslání průvodce zaškolením za použití Dynamics 365 Talent - Onboard
description: V tomto tématu je vysvětleno, jak pomocí aplikace Microsoft Dynamics 365 Talent - Onboard vytvořit průvodce zaškolením pro nové zaměstnance. Tento úkol je zásadním prvním krokem strategie pro nakládání s lidským kapitálem (HCM).
author: andreabichsel
manager: ''
ms.date: 05/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HcmCourseType, HcmCourseTypeGroup, HRMCourseTable
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-05-06
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 2371d86165390503312c2848842acf4745a8ed7a
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/06/2019
ms.locfileid: "2898241"
---
# <a name="create-and-send-an-onboarding-guide"></a><span data-ttu-id="e826f-104">Vytvoření a odeslání průvodce zaškolením</span><span class="sxs-lookup"><span data-stu-id="e826f-104">Create and send an onboarding guide</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e826f-105">Aplikace Microsoft Dynamics 365 Talent: Onboard umožňuje vytvářet průvodce zaškolením na základě šablon, které jste vytvořili sami, z šablon, které jsou k dispozici v galerii, nebo od začátku.</span><span class="sxs-lookup"><span data-stu-id="e826f-105">Microsoft Dynamics 365 Talent: Onboard lets you create onboarding guides from templates that you created yourself, from templates that are available in a gallery, or from scratch.</span></span>

<span data-ttu-id="e826f-106">Jakmile vytvoříte průvodce zaškolením, můžete ji odeslat novému zaměstnanci.</span><span class="sxs-lookup"><span data-stu-id="e826f-106">After you've created an onboarding guide, you can send it to a new hire.</span></span> <span data-ttu-id="e826f-107">Případně jej můžete odeslat více novým zaměstnancům, které zadáte v souboru Microsoft Excel, který stáhnete z aplikace Onboard.</span><span class="sxs-lookup"><span data-stu-id="e826f-107">Alternatively, you can send it to multiple new hires that you specify in a Microsoft Excel file that you download from the Onboard app.</span></span>

## <a name="create-an-onboarding-guide-from-a-template-and-send-it-to-a-single-new-hire"></a><span data-ttu-id="e826f-108">Vytvořte průvodce zaškolením ze šablony a odešlete ji jedinému novému zaměstnanci</span><span class="sxs-lookup"><span data-stu-id="e826f-108">Create an onboarding guide from a template and send it to a single new hire</span></span>

1. <span data-ttu-id="e826f-109">V levé nabídce vyberte možnost **Šablony**.</span><span class="sxs-lookup"><span data-stu-id="e826f-109">On the left menu, select **Templates**.</span></span>
2. <span data-ttu-id="e826f-110">V části **Moje šablony** vyberte šablonu, kterou chcete nastavit jako průvodce zaškolením pro nového zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="e826f-110">Under **My templates**, select the template that you want to set up as an onboarding guide for the new hire.</span></span>
3. <span data-ttu-id="e826f-111">Podle potřeby upravte šablonu.</span><span class="sxs-lookup"><span data-stu-id="e826f-111">Edit the template as you desire.</span></span> <span data-ttu-id="e826f-112">Nezapomeňte si pravidelně ukládat svou práci.</span><span class="sxs-lookup"><span data-stu-id="e826f-112">Be sure to save your work as you go.</span></span>
4. <span data-ttu-id="e826f-113">Po dokončení úprav šablony vyberte možnost **Vytvořit průvodce**.</span><span class="sxs-lookup"><span data-stu-id="e826f-113">When you've finished editing the template, select **Create guide**.</span></span>

    <span data-ttu-id="e826f-114">[![Vytvoření průvodce zaškolením ze šablony.](./media/onboard-create-guide.png)](./media/onboard-create-guide.png)</span><span class="sxs-lookup"><span data-stu-id="e826f-114">[![Creating an onboarding guide from a template](./media/onboard-create-guide.png)](./media/onboard-create-guide.png)</span></span>

5. <span data-ttu-id="e826f-115">V okně **Vytvořit průvodce**, které je v sekci **Koho zaškolujete?**, zadejte jméno nebo e-mailovou adresu nového zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="e826f-115">In the **Create a guide** window, under **Who are you onboarding**, enter the new hire's name or email address.</span></span> <span data-ttu-id="e826f-116">Pokud nový zaměstnanec není dosud v systému, vyberte možnost **Přidat nyní** a zadejte informace o daném zaměstnanci.</span><span class="sxs-lookup"><span data-stu-id="e826f-116">If the new hire isn't in the system yet, select **Add now**, and enter the employee's information.</span></span>

    ![[<span data-ttu-id="e826f-117">Zadání údajů pro průvodce zaškolením</span><span class="sxs-lookup"><span data-stu-id="e826f-117">Entering information for the onboarding guide</span></span>](./media/onboard-create-a-guide-window.png)](./media/onboard-create-a-guide-window.png)

6. <span data-ttu-id="e826f-118">V části **Kdy začínají?** vyberte počáteční datum.</span><span class="sxs-lookup"><span data-stu-id="e826f-118">Under **When do they start**, select a start date.</span></span>
7. <span data-ttu-id="e826f-119">Má-li být průvodce zaškolením automaticky odeslán novému zaměstnanci k určitému datu, ujistěte se, že je zaškrtnuta možnost **Naplánovat datum automatického odeslání** a vyberte datum automatického odeslání.</span><span class="sxs-lookup"><span data-stu-id="e826f-119">If the onboarding guide should be sent automatically to the new hire on a specific date, make sure that the **Schedule an automatic send date** option is turned on, and then select the automatic send date.</span></span> <span data-ttu-id="e826f-120">Chcete-li průvodce odeslat okamžitě, vypněte možnost **Naplánovat datum automatického odeslání**.</span><span class="sxs-lookup"><span data-stu-id="e826f-120">To send the guide immediately, turn off the **Schedule an automatic send date** option.</span></span>
8. <span data-ttu-id="e826f-121">Vyberte **Hotovo**.</span><span class="sxs-lookup"><span data-stu-id="e826f-121">Select **Done**.</span></span>
9. <span data-ttu-id="e826f-122">Po dokončení úprav průvodce zaškolení vyberte možnost **Odeslat** v pravém horním rohu.</span><span class="sxs-lookup"><span data-stu-id="e826f-122">When you've finished editing the onboarding guide, select **Send** in the upper-right corner.</span></span> <span data-ttu-id="e826f-123">Potom proveďte jeden z následujících kroků:</span><span class="sxs-lookup"><span data-stu-id="e826f-123">Then follow one of these steps:</span></span>

    - <span data-ttu-id="e826f-124">Chcete-li odeslat novému zaměstnanci odkaz na průvodce zaškolením, vyberte možnost **Kopírovat odkaz** a poté vyberte **Kopírovat**.</span><span class="sxs-lookup"><span data-stu-id="e826f-124">To send the new hire a link to the onboarding guide, select **copy a link**, and then select **Copy**.</span></span>
    - <span data-ttu-id="e826f-125">Chcete-li před odesláním upravit e-mailovou zprávu s průvodcem zaškolením, vyberte **Přizpůsobte si e-mail před jeho odesláním**, vyberte **Další**, přizpůsobte e-mail požadovaným způsobem a pak vyberte možnost **Odeslat**.</span><span class="sxs-lookup"><span data-stu-id="e826f-125">To customize the email for the onboarding guide before you send it, select **Customize the email before sending**, select **Next**, customize the email as you desire, and then select **Send**.</span></span>
    - <span data-ttu-id="e826f-126">Chcete-li odeslat e-mail bez jeho přizpůsobení, vyberte možnost **Další** a pak vyberte **Odeslat**.</span><span class="sxs-lookup"><span data-stu-id="e826f-126">To send the email without customizing it, select **Next**, and then select **Send**.</span></span>

## <a name="create-an-onboarding-guide-from-a-template-and-send-it-to-multiple-new-hires"></a><span data-ttu-id="e826f-127">Vytvořte průvodce zaškolením ze šablony a odešlete jej více novým zaměstnancům</span><span class="sxs-lookup"><span data-stu-id="e826f-127">Create an onboarding guide from a template and send it to multiple new hires</span></span>

<span data-ttu-id="e826f-128">Onboard vám umožňuje odeslat průvodce zaškolením několika novým zaměstnancům současně.</span><span class="sxs-lookup"><span data-stu-id="e826f-128">Onboard lets you send an onboarding guide to multiple new hires at the same time.</span></span>

1. <span data-ttu-id="e826f-129">V levé nabídce vyberte možnost **Šablony**.</span><span class="sxs-lookup"><span data-stu-id="e826f-129">On the left menu, select **Templates**.</span></span>
2. <span data-ttu-id="e826f-130">V části **Moje šablony** vyberte šablonu, kterou chcete nastavit jako průvodce zaškolením pro nové zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="e826f-130">Under **My templates**, select the template that you want to set up as an onboarding guide for the new hires.</span></span>
3. <span data-ttu-id="e826f-131">Podle potřeby upravte šablonu.</span><span class="sxs-lookup"><span data-stu-id="e826f-131">Edit the template as you desire.</span></span> <span data-ttu-id="e826f-132">Nezapomeňte si pravidelně ukládat svou práci.</span><span class="sxs-lookup"><span data-stu-id="e826f-132">Be sure to save your work as you go.</span></span>
4. <span data-ttu-id="e826f-133">Po dokončení úprav šablony vyberte možnost **Vytvořit průvodce**.</span><span class="sxs-lookup"><span data-stu-id="e826f-133">When you've finished editing the template, select **Create guide**.</span></span>
5. <span data-ttu-id="e826f-134">V okně **Vytvořit průvodce** vyberte možnost **Potřebujete zaškolit více lidí najednou**.</span><span class="sxs-lookup"><span data-stu-id="e826f-134">In the **Create a guide** window, select **Need to onboard multiple people at once**.</span></span>

    <span data-ttu-id="e826f-135">[![Vytvoření průvodce zaškolením pro více nových zaměstnanců](./media/onboard-send-guide-multiple-people.png)](./media/onboard-send-guide-multiple-people.png)</span><span class="sxs-lookup"><span data-stu-id="e826f-135">[![Creating an onboarding guide for multiple new hires](./media/onboard-send-guide-multiple-people.png)](./media/onboard-send-guide-multiple-people.png)</span></span>

6. <span data-ttu-id="e826f-136">Vyberte **šablonu nového zaměstnance**.</span><span class="sxs-lookup"><span data-stu-id="e826f-136">Select **new hire template**.</span></span>
7. <span data-ttu-id="e826f-137">Po stažení souboru .xlsx vyberte možnost **Otevřít**, zadejte informace o zaměstnancích do sešitu aplikace Excel a sešit uložte.</span><span class="sxs-lookup"><span data-stu-id="e826f-137">After the .xlsx file is downloaded, select **Open**, enter the employees' information in the Excel workbook, and save the workbook.</span></span>

    <span data-ttu-id="e826f-138">[![Probíhá stahování šablony aplikace Excel pro odeslání průvodce zaškolením více novým zaměstnancům](./media/onboard-send-guide-download-spreadsheet.png)](./media/onboard-send-guide-download-spreadsheet.png)</span><span class="sxs-lookup"><span data-stu-id="e826f-138">[![Downloading the Excel template for sending the onboarding guide to multiple new hires](./media/onboard-send-guide-download-spreadsheet.png)](./media/onboard-send-guide-download-spreadsheet.png)</span></span>

    > [!NOTE]
    > <span data-ttu-id="e826f-139">Před úpravou sešitu je nutné vybrat možnost **Povolit úpravy** v aplikaci Excel.</span><span class="sxs-lookup"><span data-stu-id="e826f-139">Before you can edit the workbook, you must select **Enable editing** in Excel.</span></span>
    > 
    > <span data-ttu-id="e826f-140">[![Povolit úpravy](./media/onboard-send-guide-enable-editing.png)](./media/onboard-send-guide-enable-editing.png)</span><span class="sxs-lookup"><span data-stu-id="e826f-140">[![Enabling editing](./media/onboard-send-guide-enable-editing.png)](./media/onboard-send-guide-enable-editing.png)</span></span>

8. <span data-ttu-id="e826f-141">Přetáhněte sešit aplikace Excel do vymezené oblasti v okně **Vytvořit více průvodců** nebo klepnutím na libovolné místo v této oblasti vyhledejte soubor v počítači.</span><span class="sxs-lookup"><span data-stu-id="e826f-141">Drag the Excel workbook to the designated area in the **Create multiple guides** window, or click anywhere in that area to browse for the file on your computer.</span></span>

    <span data-ttu-id="e826f-142">[![Přetažení upraveného sešitu](./media/onboard-send-guide-drag-spreadsheet.png)](./media/onboard-send-guide-drag-spreadsheet.png)</span><span class="sxs-lookup"><span data-stu-id="e826f-142">[![Dragging the edited workbook](./media/onboard-send-guide-drag-spreadsheet.png)](./media/onboard-send-guide-drag-spreadsheet.png)</span></span>

9. <span data-ttu-id="e826f-143">Po dokončení úprav průvodce zaškolení vyberte možnost **Odeslat** v pravém horním rohu.</span><span class="sxs-lookup"><span data-stu-id="e826f-143">When you've finished editing the onboarding guide, select **Send** in the upper-right corner.</span></span> <span data-ttu-id="e826f-144">Potom proveďte jeden z následujících kroků:</span><span class="sxs-lookup"><span data-stu-id="e826f-144">Then follow one of these steps:</span></span>

    - <span data-ttu-id="e826f-145">Chcete-li odeslat novým zaměstnancům odkaz na průvodce zaškolením, vyberte možnost **Kopírovat odkaz** a poté vyberte **Kopírovat**.</span><span class="sxs-lookup"><span data-stu-id="e826f-145">To send the new hires a link to the onboarding guide, select **copy a link**, and then select **Copy**.</span></span>
    - <span data-ttu-id="e826f-146">Chcete-li před odesláním upravit e-mailovou zprávu s průvodcem zaškolením, vyberte **Přizpůsobte si e-mail před jeho odesláním**, vyberte **Další**, přizpůsobte e-mail požadovaným způsobem a pak vyberte možnost **Odeslat**.</span><span class="sxs-lookup"><span data-stu-id="e826f-146">To customize the email for the onboarding guide before you send it, select **Customize the email before sending**, select **Next**, customize the email as you desire, and then select **Send**.</span></span>
    - <span data-ttu-id="e826f-147">Chcete-li odeslat e-mail bez jeho přizpůsobení, vyberte možnost **Další** a pak vyberte **Odeslat**.</span><span class="sxs-lookup"><span data-stu-id="e826f-147">To send the email without customizing it, select **Next**, and then select **Send**.</span></span>

## <a name="create-a-guide-without-using-a-template"></a><span data-ttu-id="e826f-148">Vytvořit průvodce bez použití šablony</span><span class="sxs-lookup"><span data-stu-id="e826f-148">Create a guide without using a template</span></span>

<span data-ttu-id="e826f-149">Není vždy nutné vytvářet průvodce ze šablony.</span><span class="sxs-lookup"><span data-stu-id="e826f-149">You don't always have to create a guide from a template.</span></span> <span data-ttu-id="e826f-150">Chcete-li, můžete místo toho vytvořit průvodce od začátku.</span><span class="sxs-lookup"><span data-stu-id="e826f-150">If you prefer, you can create a guide from scratch instead.</span></span>

1. <span data-ttu-id="e826f-151">V levé nabídce vyberte možnost **Průvodce** a poté vyberte tlačítko **Přidat** (znaménko plus \[**+**\]).</span><span class="sxs-lookup"><span data-stu-id="e826f-151">On the left menu, select **Guides**, and then select the **Add** button (the plus sign \[**+**\]).</span></span>
2. <span data-ttu-id="e826f-152">V okně **Vytvořit průvodce**, které je v sekci **Koho zaškolujete?**, zadejte jméno nebo e-mailovou adresu nového zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="e826f-152">In the **Create a guide** window, under **Who are you onboarding**, enter the new hire's name or email address.</span></span> <span data-ttu-id="e826f-153">Pokud nový zaměstnanec není dosud v systému, vyberte možnost **Přidat nyní** a zadejte informace o daném zaměstnanci.</span><span class="sxs-lookup"><span data-stu-id="e826f-153">If the new hire isn't in the system yet, select **Add now**, and enter the employee's information.</span></span>

    ![[<span data-ttu-id="e826f-154">Zadání údajů pro průvodce zaškolením</span><span class="sxs-lookup"><span data-stu-id="e826f-154">Entering information for the onboarding guide</span></span>](./media/onboard-create-a-guide-window.png)](./media/onboard-create-a-guide-window.png)

3. <span data-ttu-id="e826f-155">V části **Kdy začínají?** vyberte počáteční datum.</span><span class="sxs-lookup"><span data-stu-id="e826f-155">Under **When do they start**, select a start date.</span></span>
4. <span data-ttu-id="e826f-156">Má-li být průvodce zaškolením automaticky odeslán novému zaměstnanci k určitému datu, ujistěte se, že je zaškrtnuta možnost **Naplánovat datum automatického odeslání** a vyberte datum automatického odeslání.</span><span class="sxs-lookup"><span data-stu-id="e826f-156">If the onboarding guide should be sent automatically to the new hire on a specific date, make sure that the **Schedule an automatic send date** option is turned on, and then select the automatic send date.</span></span> <span data-ttu-id="e826f-157">Chcete-li průvodce odeslat okamžitě, vypněte možnost **Naplánovat datum automatického odeslání**.</span><span class="sxs-lookup"><span data-stu-id="e826f-157">To send the guide immediately, turn off the **Schedule an automatic send date** option.</span></span>
5. <span data-ttu-id="e826f-158">Vyberte **Hotovo**.</span><span class="sxs-lookup"><span data-stu-id="e826f-158">Select **Done**.</span></span>

## <a name="save-a-guide-as-a-template"></a><span data-ttu-id="e826f-159">Uložit průvodce jako šablonu</span><span class="sxs-lookup"><span data-stu-id="e826f-159">Save a guide as a template</span></span>

<span data-ttu-id="e826f-160">Průvodce zaškolením můžete uložit jako šablonu.</span><span class="sxs-lookup"><span data-stu-id="e826f-160">You can save an onboarding guide as a template.</span></span> <span data-ttu-id="e826f-161">Tímto způsobem můžete ušetřit čas, když musíte později vytvořit další průvodce.</span><span class="sxs-lookup"><span data-stu-id="e826f-161">In this way, you can save time when you must create more onboarding guides later.</span></span>

1. <span data-ttu-id="e826f-162">V levé nabídce vyberte možnost **Průvodci**.</span><span class="sxs-lookup"><span data-stu-id="e826f-162">On the left menu, select **Guides**.</span></span>
2. <span data-ttu-id="e826f-163">Vyberte tlačítko **Více** (tři tečky \[**...**\]) pro průvodce, ze kterého chcete vytvořit šablonu, a poté vyberte možnost **Uložit jako šablonu**.</span><span class="sxs-lookup"><span data-stu-id="e826f-163">Select the **More** button (the ellipsis \[**...**\]) for the guide that you want to create a template from, and then select **Save as template**.</span></span>

    ![[<span data-ttu-id="e826f-164">Uložení průvodce zaškolením jako šablonu.</span><span class="sxs-lookup"><span data-stu-id="e826f-164">Saving an onboarding guide as a template</span></span>](./media/onboard-save-guide-as-template.png)](./media/onboard-save-guide-as-template.png)

3. <span data-ttu-id="e826f-165">V okně **Uložit jako novou šablonu** zadejte název nové šablony a pak vyberte možnost **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="e826f-165">In the **Save as a new template** window, enter a name for your new template, and then select **Save**.</span></span>

## <a name="next-steps"></a><span data-ttu-id="e826f-166">Další kroky</span><span class="sxs-lookup"><span data-stu-id="e826f-166">Next steps</span></span>

- [<span data-ttu-id="e826f-167">Úprava průvodců a šablon zaškolení</span><span class="sxs-lookup"><span data-stu-id="e826f-167">Edit onboarding guides and templates</span></span>](./onboard-edit-guides-templates.md)
- [<span data-ttu-id="e826f-168">Sdílení obsahu s jinými přispěvateli</span><span class="sxs-lookup"><span data-stu-id="e826f-168">Share content with other contributors</span></span>](./onboard-share-template.md)
- [<span data-ttu-id="e826f-169">Zobrazit stav úkolů a zaškolení zaměstnanců</span><span class="sxs-lookup"><span data-stu-id="e826f-169">View the status of tasks and onboarding employees</span></span>](./onboard-view-status.md)
- [<span data-ttu-id="e826f-170">Vytvořit náborové týmy v Onboard</span><span class="sxs-lookup"><span data-stu-id="e826f-170">Create hiring teams in Onboard</span></span>](./onboard-create-team.md)

### <a name="see-also"></a><span data-ttu-id="e826f-171">Viz také</span><span class="sxs-lookup"><span data-stu-id="e826f-171">See also</span></span>

- [<span data-ttu-id="e826f-172">Vyzkoušejte nebo kupte aplikaci Onboard</span><span class="sxs-lookup"><span data-stu-id="e826f-172">Try or buy the Onboard app</span></span>](https://dynamics.microsoft.com/talent/onboard/)
- [<span data-ttu-id="e826f-173">Co je nového a co se změnilo v aplikaci Dynamics 365 Talent</span><span class="sxs-lookup"><span data-stu-id="e826f-173">What's new or changed in Dynamics 365 Talent</span></span>](./whats-new.md)
- [<span data-ttu-id="e826f-174">Plány vydání</span><span class="sxs-lookup"><span data-stu-id="e826f-174">Release plans</span></span>](https://docs.microsoft.com/business-applications-release-notes/index)
- [<span data-ttu-id="e826f-175">Získání podpory pro Microsoft Dynamics 365 Talent</span><span class="sxs-lookup"><span data-stu-id="e826f-175">Get support for Microsoft Dynamics 365 Talent</span></span>](./talent-support.md)
