---
title: Konfigurace schvalovacích procesů ve workflowu
description: Pomocí následujícího postupu nakonfigurujte vlastnosti schvalovacího procesu.
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 195643
ms.assetid: f853f57b-83ae-4fb0-a9fa-06ea3fc34fa1
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 08641eaac31813a8bee3231118f8e2bf802ea3e1
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1555526"
---
# <a name="configure-approval-processes-in-a-workflow"></a><span data-ttu-id="04775-103">Konfigurace schvalovacích procesů ve workflowu</span><span class="sxs-lookup"><span data-stu-id="04775-103">Configure approval processes in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="04775-104">Pomocí následujícího postupu nakonfigurujte vlastnosti schvalovacího procesu.</span><span class="sxs-lookup"><span data-stu-id="04775-104">Use the following procedure to configure the properties of the approval process.</span></span>

<span data-ttu-id="04775-105">Pokud budete chtít nakonfigurovat schvalovací proces, v editoru workflowu klikněte pravým tlačítkem myši na prvek schválení a kliknutím na tlačítko **Vlastnosti** otevřete formulář **Vlastnosti**.</span><span class="sxs-lookup"><span data-stu-id="04775-105">To configure an approval process, in the workflow editor, right-click the approval element, and then click **Properties** to open the **Properties** form.</span></span>

## <a name="name-the-approval-process"></a><span data-ttu-id="04775-106">Pojmenování schvalovacího procesu</span><span class="sxs-lookup"><span data-stu-id="04775-106">Name the approval process</span></span>

<span data-ttu-id="04775-107">Pomocí následujících kroků zadejte název schvalovacího procesu.</span><span class="sxs-lookup"><span data-stu-id="04775-107">Follow these steps to enter a name for the approval process.</span></span>

1. <span data-ttu-id="04775-108">V levém podokně klepněte na tlačítko **Základní nastavení**.</span><span class="sxs-lookup"><span data-stu-id="04775-108">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="04775-109">V poli **Název** zadejte jedinečný název schvalovacího procesu.</span><span class="sxs-lookup"><span data-stu-id="04775-109">In the **Name** field, enter a unique name for the approval process.</span></span>

## <a name="specify-when-the-system-automatically-acts-on-the-document"></a><span data-ttu-id="04775-110">Určení podmínky, podle které systém automaticky provede akci u dokumentu</span><span class="sxs-lookup"><span data-stu-id="04775-110">Specify when the system automatically acts on the document</span></span>

<span data-ttu-id="04775-111">Můžete nakonfigurovat systém tak, aby automaticky zpracoval dokument, pokud jsou splněny určité podmínky.</span><span class="sxs-lookup"><span data-stu-id="04775-111">You can configure the system to automatically act on the document if specific conditions are met.</span></span> <span data-ttu-id="04775-112">Systém může například schvalovat vyúčtování výdajů, která mají celkové částky nižší než 100 USD.</span><span class="sxs-lookup"><span data-stu-id="04775-112">For example, the system can approve expense reports that have total amounts that are less than USD 100.</span></span> <span data-ttu-id="04775-113">Pomocí tohoto postupu určete podmínky, za kterých má systém u dokumentu provést akci.</span><span class="sxs-lookup"><span data-stu-id="04775-113">Follow these steps to specify when the system acts on the document.</span></span>

1. <span data-ttu-id="04775-114">V levém podokně klepněte na tlačítko **Automatické akce**.</span><span class="sxs-lookup"><span data-stu-id="04775-114">In the left pane, click **Automatic actions**.</span></span>
2. <span data-ttu-id="04775-115">Označte pole **Povolit automatické akce**.</span><span class="sxs-lookup"><span data-stu-id="04775-115">Select the **Enable automatic actions** check box.</span></span>
3. <span data-ttu-id="04775-116">Klikněte na možnost **Přidat podmínku**.</span><span class="sxs-lookup"><span data-stu-id="04775-116">Click **Add condition**.</span></span>
4. <span data-ttu-id="04775-117">Zadání podmínky</span><span class="sxs-lookup"><span data-stu-id="04775-117">Enter a condition.</span></span>
5. <span data-ttu-id="04775-118">V případě potřeby zadejte další podmínky.</span><span class="sxs-lookup"><span data-stu-id="04775-118">Enter additional conditions, if necessary.</span></span>
6. <span data-ttu-id="04775-119">Chcete-li ověřit, zda jsou zadané podmínky nastaveny správně, postupujte následovně:</span><span class="sxs-lookup"><span data-stu-id="04775-119">To verify that the conditions that you entered are configured correctly, complete the following steps:</span></span>

    1. <span data-ttu-id="04775-120">Klepnutím na tlačítko **Test** otevřete formulář **Podmínka testovacího workflowu**.</span><span class="sxs-lookup"><span data-stu-id="04775-120">Click **Test** to open the **Test workflow condition** form.</span></span>
    2. <span data-ttu-id="04775-121">Vyberte v oblasti **Ověřit podmínku** formuláře záznam.</span><span class="sxs-lookup"><span data-stu-id="04775-121">Select a record in the **Validate condition** area of the form.</span></span>
    3. <span data-ttu-id="04775-122">Klepněte na možnost **Test**.</span><span class="sxs-lookup"><span data-stu-id="04775-122">Click **Test**.</span></span> <span data-ttu-id="04775-123">Systém záznam vyhodnotí a určí, zda odpovídá zadaným podmínkám.</span><span class="sxs-lookup"><span data-stu-id="04775-123">The system evaluates the record to determine whether it meets the conditions that you defined.</span></span>
    4. <span data-ttu-id="04775-124">Kliknutím na tlačítko **OK** nebo **Zrušit** se vraťte do formuláře **Vlastnosti**.</span><span class="sxs-lookup"><span data-stu-id="04775-124">Click **OK** or **Cancel** to return to the **Properties** form.</span></span>

7. <span data-ttu-id="04775-125">V seznamu **Akce automatického dokončení** vyberte akci, která má být u dokumentu provedena.</span><span class="sxs-lookup"><span data-stu-id="04775-125">In the **Auto complete action** list, select the action that the system should take on the document.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="04775-126">Zadejte, kdy se mají odesílat oznámení.</span><span class="sxs-lookup"><span data-stu-id="04775-126">Specify when notifications are sent</span></span>

<span data-ttu-id="04775-127">Při schválení, zamítnutí, delegování nebo eskalování dokumentu nebo při zadání požadavku na změnu můžete zaslat oznámení určeným osobám.</span><span class="sxs-lookup"><span data-stu-id="04775-127">You can send notifications to people when a document has been approved, rejected, delegated, or escalated, or when a change has been requested.</span></span> <span data-ttu-id="04775-128">Podle těchto kroků můžete určit oznámení, které se odešle, a osoby, kterým se odešle.</span><span class="sxs-lookup"><span data-stu-id="04775-128">Follow these steps to specify when notifications are sent, and who the notifications are sent to.</span></span>

1. <span data-ttu-id="04775-129">V levém podokně klikněte na **Oznámení**.</span><span class="sxs-lookup"><span data-stu-id="04775-129">In the left pane, click **Notifications**.</span></span>
2. <span data-ttu-id="04775-130">Označte pole vedle událostí, při kterých se oznámení odešle:</span><span class="sxs-lookup"><span data-stu-id="04775-130">Select the check box next to the events to send notifications for:</span></span>

    - <span data-ttu-id="04775-131">**Delegování** – přiřazení dokumentu jinému uživateli ke schválení.</span><span class="sxs-lookup"><span data-stu-id="04775-131">**Delegate** – When a document has been assigned to another user for approval.</span></span>
    - <span data-ttu-id="04775-132">**Eskalace** – přiřazený uživatel nereagoval na dokument v přiděleném čase.</span><span class="sxs-lookup"><span data-stu-id="04775-132">**Escalate** – When the assigned user has not acted on a document in the allotted time.</span></span>
    - <span data-ttu-id="04775-133">**Schválení** – schválení dokumentu.</span><span class="sxs-lookup"><span data-stu-id="04775-133">**Approve** – When a document has been approved.</span></span>
    - <span data-ttu-id="04775-134">**Zamítnutí** – zamítnutí dokumentu.</span><span class="sxs-lookup"><span data-stu-id="04775-134">**Reject** – When a document has been rejected.</span></span>
    - <span data-ttu-id="04775-135">**Požadavek na změnu** – přidělený uživatel požaduje změnu odeslaného dokumentu.</span><span class="sxs-lookup"><span data-stu-id="04775-135">**Request change** – When the assigned user has requested a change to a document that was submitted.</span></span>

3. <span data-ttu-id="04775-136">Vyberte řádek pro událost, kterou jste vybrali v kroku 2.</span><span class="sxs-lookup"><span data-stu-id="04775-136">Select the row for an event that you selected in step 2.</span></span>
4. <span data-ttu-id="04775-137">Klepněte na kartu **Text oznámení**.</span><span class="sxs-lookup"><span data-stu-id="04775-137">Click the **Notification text** tab.</span></span>
5. <span data-ttu-id="04775-138">Do textového pole zadejte název oznámení.</span><span class="sxs-lookup"><span data-stu-id="04775-138">In the text box, enter the text for the notification.</span></span>
6. <span data-ttu-id="04775-139">Text můžete přizpůsobit vložením zástupného textu, který bude při zobrazení uživatelům nahrazen odpovídacími daty.</span><span class="sxs-lookup"><span data-stu-id="04775-139">To personalize the text, you can insert placeholders, which are replaced with the appropriate data when they are displayed to users.</span></span> <span data-ttu-id="04775-140">Při vkládání zástupného textu postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="04775-140">To insert a placeholder, follow these steps:</span></span>

    1. <span data-ttu-id="04775-141">Klepněte do textového pole do umístění, kde se má zástupný text zobrazit.</span><span class="sxs-lookup"><span data-stu-id="04775-141">Click in the text box at the location where the placeholder should appear.</span></span>
    2. <span data-ttu-id="04775-142">Klikněte na **Vložit zástupný text**.</span><span class="sxs-lookup"><span data-stu-id="04775-142">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="04775-143">V seznamu, který se zobrazí, vyberte vkládaný zástupný text.</span><span class="sxs-lookup"><span data-stu-id="04775-143">In the list that is displayed, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="04775-144">Klepněte na tlačítko **Vložit**.</span><span class="sxs-lookup"><span data-stu-id="04775-144">Click **Insert**.</span></span>

7. <span data-ttu-id="04775-145">Chcete-li přidat překlady oznámení, klikněte na **Překlady**.</span><span class="sxs-lookup"><span data-stu-id="04775-145">To add translations of the notification, click **Translations**.</span></span> <span data-ttu-id="04775-146">Ve formuláři, který se zobrazí, postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="04775-146">In the form that is displayed, follow these steps:</span></span>

    1. <span data-ttu-id="04775-147">Klikněte na tlačítko **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="04775-147">Click **Add**.</span></span>
    2. <span data-ttu-id="04775-148">V otevřeném seznamu vyberte jazyk, který chcete použít pro zadání textu.</span><span class="sxs-lookup"><span data-stu-id="04775-148">In the list that is displayed, select the language in which you will enter the text.</span></span>
    3. <span data-ttu-id="04775-149">V textovém poli **Přeložený text** zadejte text.</span><span class="sxs-lookup"><span data-stu-id="04775-149">In the **Translated text** text box, enter the text.</span></span>
    4. <span data-ttu-id="04775-150">Text můžete přizpůsobit vložením zástupného textu.</span><span class="sxs-lookup"><span data-stu-id="04775-150">To personalize the text, insert placeholders.</span></span>
    5. <span data-ttu-id="04775-151">Klepněte na tlačítko **Zavřít**.</span><span class="sxs-lookup"><span data-stu-id="04775-151">Click **Close**.</span></span>

8. <span data-ttu-id="04775-152">Klikněte na kartu **Příjemce**.</span><span class="sxs-lookup"><span data-stu-id="04775-152">Click the **Recipient** tab.</span></span>
9. <span data-ttu-id="04775-153">Zadejte, komu se mají odesílat oznámení.</span><span class="sxs-lookup"><span data-stu-id="04775-153">Specify who the notifications are sent to.</span></span> <span data-ttu-id="04775-154">Vyberte jednu z možností v následující tabulce a před přechodem na krok 10 postupujte podle dalších kroků pro tuto možnost.</span><span class="sxs-lookup"><span data-stu-id="04775-154">Select one of the options in the following table, and then follow the additional steps for the option before you go to step 10.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="04775-155">Parametr</span><span class="sxs-lookup"><span data-stu-id="04775-155">Option</span></span></th>
    <th><span data-ttu-id="04775-156">Příjemce oznámení</span><span class="sxs-lookup"><span data-stu-id="04775-156">Notification recipients</span></span></th>
    <th><span data-ttu-id="04775-157">Další kroky</span><span class="sxs-lookup"><span data-stu-id="04775-157">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="04775-158"><strong>Účastník</strong></span><span class="sxs-lookup"><span data-stu-id="04775-158"><strong>Participant</strong></span></span></td>
    <td><span data-ttu-id="04775-159">Uživatelé, kteří jsou přiřazeni k určité skupině nebo roli</span><span class="sxs-lookup"><span data-stu-id="04775-159">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="04775-160">Po výběru možnosti <strong>Účastník</strong> klepněte na kartu <strong>Založeno na roli</strong>.</span><span class="sxs-lookup"><span data-stu-id="04775-160">After you select <strong>Participant</strong>, click the <strong>Role based</strong> tab.</span></span></li>
    <li><span data-ttu-id="04775-161">V seznamu <strong>Typ účastníka</strong> vyberte typ skupiny nebo role, které chcete oznámení odeslat.</span><span class="sxs-lookup"><span data-stu-id="04775-161">In the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="04775-162">V seznamu <strong>Účastník</strong> vyberte skupinu nebo roli, které chcete oznámení odeslat.</span><span class="sxs-lookup"><span data-stu-id="04775-162">In the <strong>Participant</strong> list, select the group or role to send notifications to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="04775-163"><strong>Uživatel workflowu</strong></span><span class="sxs-lookup"><span data-stu-id="04775-163"><strong>Workflow user</strong></span></span></td>
    <td><span data-ttu-id="04775-164">Uživatelé zúčastnění v aktuálním workflowu</span><span class="sxs-lookup"><span data-stu-id="04775-164">Users who participate in the current workflow</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="04775-165">Po výběru možnosti <strong>Uživatel workflowu</strong> klepněte na kartu <strong>Uživatel workflowu</strong>.</span><span class="sxs-lookup"><span data-stu-id="04775-165">After you select <strong>Workflow user</strong>, click the <strong>Workflow user</strong> tab.</span></span></li>
    <li><span data-ttu-id="04775-166">V seznamu <strong>Uživatel workflowu</strong> vyberte uživatele, který se účastní workflowu.</span><span class="sxs-lookup"><span data-stu-id="04775-166">In the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="04775-167"><strong>Uživatel</strong></span><span class="sxs-lookup"><span data-stu-id="04775-167"><strong>User</strong></span></span></td>
    <td><span data-ttu-id="04775-168">Konkrétní uživatelé Microsoft Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="04775-168">Specific Microsoft Dynamics 365 for Finance and Operations users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="04775-169">Po výběru možnosti <strong>Uživatel</strong> klepněte na kartu <strong>Uživatel</strong>.</span><span class="sxs-lookup"><span data-stu-id="04775-169">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="04775-170"><strong>Dostupní uživatelé</strong> seznam obsahuje všechny uživatele aplikace Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="04775-170">The <strong>Available users</strong>: list includes all Microsoft Dynamics 365 for Finance and Operations users.</span></span> <span data-ttu-id="04775-171">Vyberte uživatele, kterým chcete odeslat oznámení, a pak přesuňte tyto uživatele do seznamu <strong>Vybraní uživatelé</strong>.</span><span class="sxs-lookup"><span data-stu-id="04775-171">Select the users to send notifications to, and then move these users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

10. <span data-ttu-id="04775-172">Opakujte kroky 3 až 9 pro každou událost, kterou jste vybrali v kroku 2.</span><span class="sxs-lookup"><span data-stu-id="04775-172">Repeat steps 3 through 9 for each event that you selected in step 2.</span></span>

## <a name="specify-a-final-approver"></a><span data-ttu-id="04775-173"> Určení konečného schvalovatele</span><span class="sxs-lookup"><span data-stu-id="04775-173">Specify a final approver</span></span>

<span data-ttu-id="04775-174">Můžete určit konečného schvalovatele scénářů, kde je schvalujícím osoba, která odeslala dokument ke schválení.</span><span class="sxs-lookup"><span data-stu-id="04775-174">You may want to designate a final approver for scenarios where the approver is the person who submitted the document for approval.</span></span> <span data-ttu-id="04775-175">Chcete-li určit konečného schvalovatele, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="04775-175">Follow these steps to specify a final approver.</span></span>

1. <span data-ttu-id="04775-176">V levém podokně klepněte na tlačítko **Pokročilá nastavení**.</span><span class="sxs-lookup"><span data-stu-id="04775-176">In the left pane, click **Advanced settings**.</span></span>
2. <span data-ttu-id="04775-177">Zaškrtněte políčko **Použít konečného schvalovatele**.</span><span class="sxs-lookup"><span data-stu-id="04775-177">Select the **Use final approver** check box.</span></span>
3. <span data-ttu-id="04775-178">V seznamu vyberte uživatele, který bude konečným schvalovatelem.</span><span class="sxs-lookup"><span data-stu-id="04775-178">In the list, select the user to be the final approver.</span></span>

## <a name="set-a-time-limit"></a><span data-ttu-id="04775-179">Nastavení časového limitu</span><span class="sxs-lookup"><span data-stu-id="04775-179">Set a time limit</span></span>

<span data-ttu-id="04775-180">Tento postup použijte, pokud je proces schvalování nutné dokončit v určitém čase.</span><span class="sxs-lookup"><span data-stu-id="04775-180">Follow these steps if the approval process must be completed in a specific time.</span></span>

> [!NOTE]
> <span data-ttu-id="04775-181">Možnosti, které v těchto krocích vyberete, přepíší možnosti vybrané v oblasti **Přiřazení** a **Eskalace** jednotlivých schvalovacích kroků.</span><span class="sxs-lookup"><span data-stu-id="04775-181">The options that you select in these steps override the options that you selected in the **Assignment** and **Escalation** areas of each approval step.</span></span>

1. <span data-ttu-id="04775-182">V levém podokně klepněte na tlačítko **Pokročilá nastavení**.</span><span class="sxs-lookup"><span data-stu-id="04775-182">In the left pane, click **Advanced settings**.</span></span>
2. <span data-ttu-id="04775-183">Zaškrtněte políčko **Nastavit časový limit pro prvek** **workflowu**.</span><span class="sxs-lookup"><span data-stu-id="04775-183">Select the **Set a time limit for the workflow** **element** check box.</span></span>
3. <span data-ttu-id="04775-184">V poli **Trvání** upřesněte, kdy má být schvalovací proces dokončen.</span><span class="sxs-lookup"><span data-stu-id="04775-184">In the **Duration** field, specify when the approval process must be completed.</span></span> <span data-ttu-id="04775-185">Vyberte některou z následujících možností:</span><span class="sxs-lookup"><span data-stu-id="04775-185">Select one of the following options:</span></span>

    - <span data-ttu-id="04775-186">**Hodiny** – zadejte počet hodin, dokdy musí být schvalovací proces dokončen.</span><span class="sxs-lookup"><span data-stu-id="04775-186">**Hours** – Enter the number of hours in which the approval process must be completed.</span></span> <span data-ttu-id="04775-187">Pak vyberte kalendář, který vaše organizace používá, a zadejte informace o pracovním týdnu vaší organizace.</span><span class="sxs-lookup"><span data-stu-id="04775-187">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="04775-188">**Dny** – zadejte počet dní, dokdy musí být schvalovací proces dokončen.</span><span class="sxs-lookup"><span data-stu-id="04775-188">**Days** – Enter the number of days in which the approval process must be completed.</span></span> <span data-ttu-id="04775-189">Pak vyberte kalendář, který vaše organizace používá, a zadejte informace o pracovním týdnu vaší organizace.</span><span class="sxs-lookup"><span data-stu-id="04775-189">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="04775-190">**Týdny** – zadejte počet týdnů, dokdy musí být schvalovací proces dokončen.</span><span class="sxs-lookup"><span data-stu-id="04775-190">**Weeks** – Enter the number of weeks in which the approval process must be completed.</span></span>
    - <span data-ttu-id="04775-191">**Měsíce** – vyberte den a týden, do kdy má být schvalovací proces dokončen.</span><span class="sxs-lookup"><span data-stu-id="04775-191">**Months** – Select the day and week by which the approval process must be completed.</span></span> <span data-ttu-id="04775-192">Můžete například požadovat, aby byl schvalovací proces dokončen do třetího pátku v daném měsíci.</span><span class="sxs-lookup"><span data-stu-id="04775-192">For example, you may want the approval process to be completed by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="04775-193">**Roky** – vyberte den, týden a měsíc, do kdy má být schvalovací proces dokončen.</span><span class="sxs-lookup"><span data-stu-id="04775-193">**Years** – Select the day, week, and month by which the approval process must be completed.</span></span> <span data-ttu-id="04775-194">Můžete například požadovat, aby byl schvalovací proces dokončen do třetího pátku v prosinci.</span><span class="sxs-lookup"><span data-stu-id="04775-194">For example, you may want the approval process to be completed by Friday of the third week of December.</span></span>

4. <span data-ttu-id="04775-195">Dojde-li k překročení časového limitu, systém u dokumentu provede akci.</span><span class="sxs-lookup"><span data-stu-id="04775-195">If the time limit is exceeded, the system acts on the document.</span></span> <span data-ttu-id="04775-196">V seznamu **Akce** vyberte akci, která má být provedena.</span><span class="sxs-lookup"><span data-stu-id="04775-196">In the **Action** list, select the action that the system should take.</span></span>

## <a name="specify-which-actions-are-available-to-the-user"></a><span data-ttu-id="04775-197">Určení dostupných akcí pro uživatele</span><span class="sxs-lookup"><span data-stu-id="04775-197">Specify which actions are available to the user</span></span>

<span data-ttu-id="04775-198">Po přidělení dokumentu uživateli ke schválení musí uživatel daný dokument zpracovat.</span><span class="sxs-lookup"><span data-stu-id="04775-198">When a document is assigned to a user for approval, the user must act on the document.</span></span> <span data-ttu-id="04775-199">Pomocí tohoto postupu určete akce, které může uživatel u odeslaného dokumentu provádět.</span><span class="sxs-lookup"><span data-stu-id="04775-199">Follows these steps to specify which actions the user can take on the document that was submitted.</span></span>

1. <span data-ttu-id="04775-200">V levém podokně klepněte na tlačítko **Pokročilá nastavení**.</span><span class="sxs-lookup"><span data-stu-id="04775-200">In the left pane, click **Advanced settings**.</span></span>
2. <span data-ttu-id="04775-201">Chcete-li uživatelům umožnit schválení dokumentu, zaškrtněte políčko **Schválit**.</span><span class="sxs-lookup"><span data-stu-id="04775-201">Select the **Approve** check box if the user can approve the document.</span></span>
3. <span data-ttu-id="04775-202">Chcete-li uživatelům zamítnout schválení dokumentu, zaškrtněte políčko **Zamítnout**.</span><span class="sxs-lookup"><span data-stu-id="04775-202">Select the **Reject** check box the user can reject the document.</span></span>
4. <span data-ttu-id="04775-203">Chcete-li uživatelům umožnit vyžádání změn v dokumentu, zaškrtněte políčko **Požadavek na změnu**.</span><span class="sxs-lookup"><span data-stu-id="04775-203">Select the **Request change** check box the user can request changes to the document.</span></span>
5. <span data-ttu-id="04775-204">Chcete-li uživateli umožnit, aby úlohu postoupil jinému uživateli ke schválení, zaškrtněte políčko **Delegovat**.</span><span class="sxs-lookup"><span data-stu-id="04775-204">Select the **Delegate** check box if the user can assign the document to another user for approval.</span></span>

> [!NOTE]
> <span data-ttu-id="04775-205">Políčko **Povolit akce z pracovního seznamu v podnikovém portálu** se již nepoužívá.</span><span class="sxs-lookup"><span data-stu-id="04775-205">The **Enable actions from the work list in Enterprise Portal** check box has been deprecated.</span></span>

## <a name="configure-the-approval-steps"></a><span data-ttu-id="04775-206"> Konfigurace kroků schválení</span><span class="sxs-lookup"><span data-stu-id="04775-206">Configure the approval steps</span></span>

<span data-ttu-id="04775-207">Schvalovací proces se skládá z kroků schválení.</span><span class="sxs-lookup"><span data-stu-id="04775-207">An approval process consists of approval steps.</span></span> <span data-ttu-id="04775-208">Pomocí následujícího postupu přidáte do schvalovacího procesu kroky a nakonfigurujete je.</span><span class="sxs-lookup"><span data-stu-id="04775-208">Complete the following procedure to add steps the approval process and configure the steps.</span></span>

1. <span data-ttu-id="04775-209">V editoru workflowu poklepejte na schvalovací proces.</span><span class="sxs-lookup"><span data-stu-id="04775-209">In the workflow editor, double-click the approval process.</span></span> <span data-ttu-id="04775-210">V editoru workflowu se zobrazí kroky schvalovacího procesu.</span><span class="sxs-lookup"><span data-stu-id="04775-210">The workflow editor displays the steps of the approval process.</span></span>
2. <span data-ttu-id="04775-211">Chcete-li přidat schvalovací krok, přetáhněte krok z oblasti **Prvky workflowu** na plátno.</span><span class="sxs-lookup"><span data-stu-id="04775-211">To add an approval step, drag the step from the **Workflow elements** area to the canvas.</span></span>
3. <span data-ttu-id="04775-212">Chcete-li nakonfigurovat schvalovací krok, získáte informace v části [Konfigurace schvalovacího kroku](configure-approval-step-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="04775-212">To configure an approval step, see [Configure an approval step](configure-approval-step-workflow.md).</span></span>
