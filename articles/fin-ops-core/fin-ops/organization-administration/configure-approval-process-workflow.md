---
title: Konfigurace schvalovacích procesů ve workflowu
description: Pomocí následujícího postupu nakonfigurujte vlastnosti schvalovacího procesu.
author: sericks007
manager: AnnBe
ms.date: 01/24/2020
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
ms.openlocfilehash: 1f58e227542b1e5ca1235748d14e71bddac826ee
ms.sourcegitcommit: 759325234a763e14071348a6f5399999a92f8264
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/25/2020
ms.locfileid: "2983757"
---
# <a name="configure-approval-processes-in-a-workflow"></a><span data-ttu-id="df34d-103">Konfigurace schvalovacích procesů ve workflowu</span><span class="sxs-lookup"><span data-stu-id="df34d-103">Configure approval processes in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="df34d-104">Pomocí následujícího postupu nakonfigurujte vlastnosti schvalovacího procesu.</span><span class="sxs-lookup"><span data-stu-id="df34d-104">Use the following procedure to configure the properties of the approval process.</span></span>

<span data-ttu-id="df34d-105">Pokud budete chtít nakonfigurovat schvalovací proces, v editoru workflowu klikněte pravým tlačítkem myši na prvek schválení a kliknutím na tlačítko **Vlastnosti** otevřete formulář **Vlastnosti**.</span><span class="sxs-lookup"><span data-stu-id="df34d-105">To configure an approval process, in the workflow editor, right-click the approval element, and then click **Properties** to open the **Properties** form.</span></span>

## <a name="name-the-approval-process"></a><span data-ttu-id="df34d-106">Pojmenování schvalovacího procesu</span><span class="sxs-lookup"><span data-stu-id="df34d-106">Name the approval process</span></span>

<span data-ttu-id="df34d-107">Pomocí následujících kroků zadejte název schvalovacího procesu.</span><span class="sxs-lookup"><span data-stu-id="df34d-107">Follow these steps to enter a name for the approval process.</span></span>

1. <span data-ttu-id="df34d-108">V levém podokně klepněte na tlačítko **Základní nastavení**.</span><span class="sxs-lookup"><span data-stu-id="df34d-108">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="df34d-109">V poli **Název** zadejte jedinečný název schvalovacího procesu.</span><span class="sxs-lookup"><span data-stu-id="df34d-109">In the **Name** field, enter a unique name for the approval process.</span></span>

## <a name="specify-when-the-system-automatically-acts-on-the-document"></a><span data-ttu-id="df34d-110">Určení podmínky, podle které systém automaticky provede akci u dokumentu</span><span class="sxs-lookup"><span data-stu-id="df34d-110">Specify when the system automatically acts on the document</span></span>

<span data-ttu-id="df34d-111">Můžete nakonfigurovat systém tak, aby automaticky zpracoval dokument, pokud jsou splněny určité podmínky.</span><span class="sxs-lookup"><span data-stu-id="df34d-111">You can configure the system to automatically act on the document if specific conditions are met.</span></span> <span data-ttu-id="df34d-112">Systém může například schvalovat vyúčtování výdajů, která mají celkové částky nižší než 100 USD.</span><span class="sxs-lookup"><span data-stu-id="df34d-112">For example, the system can approve expense reports that have total amounts that are less than USD 100.</span></span> <span data-ttu-id="df34d-113">Pomocí tohoto postupu určete podmínky, za kterých má systém u dokumentu provést akci.</span><span class="sxs-lookup"><span data-stu-id="df34d-113">Follow these steps to specify when the system acts on the document.</span></span>

1. <span data-ttu-id="df34d-114">V levém podokně klepněte na tlačítko **Automatické akce**.</span><span class="sxs-lookup"><span data-stu-id="df34d-114">In the left pane, click **Automatic actions**.</span></span>
2. <span data-ttu-id="df34d-115">Označte pole **Povolit automatické akce**.</span><span class="sxs-lookup"><span data-stu-id="df34d-115">Select the **Enable automatic actions** check box.</span></span>
3. <span data-ttu-id="df34d-116">Klikněte na možnost **Přidat podmínku**.</span><span class="sxs-lookup"><span data-stu-id="df34d-116">Click **Add condition**.</span></span>
4. <span data-ttu-id="df34d-117">Zadání podmínky</span><span class="sxs-lookup"><span data-stu-id="df34d-117">Enter a condition.</span></span>
5. <span data-ttu-id="df34d-118">V případě potřeby zadejte další podmínky.</span><span class="sxs-lookup"><span data-stu-id="df34d-118">Enter additional conditions, if necessary.</span></span>
6. <span data-ttu-id="df34d-119">Chcete-li ověřit, zda jsou zadané podmínky nastaveny správně, postupujte následovně:</span><span class="sxs-lookup"><span data-stu-id="df34d-119">To verify that the conditions that you entered are configured correctly, complete the following steps:</span></span>

    1. <span data-ttu-id="df34d-120">Klepnutím na tlačítko **Test** otevřete formulář **Podmínka testovacího workflowu**.</span><span class="sxs-lookup"><span data-stu-id="df34d-120">Click **Test** to open the **Test workflow condition** form.</span></span>
    2. <span data-ttu-id="df34d-121">Vyberte v oblasti **Ověřit podmínku** formuláře záznam.</span><span class="sxs-lookup"><span data-stu-id="df34d-121">Select a record in the **Validate condition** area of the form.</span></span>
    3. <span data-ttu-id="df34d-122">Klepněte na možnost **Test**.</span><span class="sxs-lookup"><span data-stu-id="df34d-122">Click **Test**.</span></span> <span data-ttu-id="df34d-123">Systém záznam vyhodnotí a určí, zda odpovídá zadaným podmínkám.</span><span class="sxs-lookup"><span data-stu-id="df34d-123">The system evaluates the record to determine whether it meets the conditions that you defined.</span></span>
    4. <span data-ttu-id="df34d-124">Kliknutím na tlačítko **OK** nebo **Zrušit** se vraťte do formuláře **Vlastnosti**.</span><span class="sxs-lookup"><span data-stu-id="df34d-124">Click **OK** or **Cancel** to return to the **Properties** form.</span></span>

7. <span data-ttu-id="df34d-125">V seznamu **Akce automatického dokončení** vyberte akci, která má být u dokumentu provedena.</span><span class="sxs-lookup"><span data-stu-id="df34d-125">In the **Auto complete action** list, select the action that the system should take on the document.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="df34d-126">Zadejte, kdy se mají odesílat oznámení.</span><span class="sxs-lookup"><span data-stu-id="df34d-126">Specify when notifications are sent</span></span>

<span data-ttu-id="df34d-127">Při schválení, zamítnutí, delegování nebo eskalování dokumentu nebo při zadání požadavku na změnu můžete zaslat oznámení určeným osobám.</span><span class="sxs-lookup"><span data-stu-id="df34d-127">You can send notifications to people when a document has been approved, rejected, delegated, or escalated, or when a change has been requested.</span></span> <span data-ttu-id="df34d-128">Podle těchto kroků můžete určit oznámení, které se odešle, a osoby, kterým se odešle.</span><span class="sxs-lookup"><span data-stu-id="df34d-128">Follow these steps to specify when notifications are sent, and who the notifications are sent to.</span></span>

1. <span data-ttu-id="df34d-129">V levém podokně klikněte na **Oznámení**.</span><span class="sxs-lookup"><span data-stu-id="df34d-129">In the left pane, click **Notifications**.</span></span>
2. <span data-ttu-id="df34d-130">Označte pole vedle událostí, při kterých se oznámení odešle:</span><span class="sxs-lookup"><span data-stu-id="df34d-130">Select the check box next to the events to send notifications for:</span></span>

    - <span data-ttu-id="df34d-131">**Delegování** – přiřazení dokumentu jinému uživateli ke schválení.</span><span class="sxs-lookup"><span data-stu-id="df34d-131">**Delegate** – When a document has been assigned to another user for approval.</span></span>
    - <span data-ttu-id="df34d-132">**Eskalace** – přiřazený uživatel nereagoval na dokument v přiděleném čase.</span><span class="sxs-lookup"><span data-stu-id="df34d-132">**Escalate** – When the assigned user has not acted on a document in the allotted time.</span></span>
    - <span data-ttu-id="df34d-133">**Schválení** – schválení dokumentu.</span><span class="sxs-lookup"><span data-stu-id="df34d-133">**Approve** – When a document has been approved.</span></span>
    - <span data-ttu-id="df34d-134">**Zamítnutí** – zamítnutí dokumentu.</span><span class="sxs-lookup"><span data-stu-id="df34d-134">**Reject** – When a document has been rejected.</span></span>
    - <span data-ttu-id="df34d-135">**Požadavek na změnu** – přidělený uživatel požaduje změnu odeslaného dokumentu.</span><span class="sxs-lookup"><span data-stu-id="df34d-135">**Request change** – When the assigned user has requested a change to a document that was submitted.</span></span>

3. <span data-ttu-id="df34d-136">Vyberte řádek pro událost, kterou jste vybrali v kroku 2.</span><span class="sxs-lookup"><span data-stu-id="df34d-136">Select the row for an event that you selected in step 2.</span></span>
4. <span data-ttu-id="df34d-137">Klepněte na kartu **Text oznámení**.</span><span class="sxs-lookup"><span data-stu-id="df34d-137">Click the **Notification text** tab.</span></span>
5. <span data-ttu-id="df34d-138">Do textového pole zadejte název oznámení.</span><span class="sxs-lookup"><span data-stu-id="df34d-138">In the text box, enter the text for the notification.</span></span>
6. <span data-ttu-id="df34d-139">Text můžete přizpůsobit vložením zástupného textu, který bude při zobrazení uživatelům nahrazen odpovídacími daty.</span><span class="sxs-lookup"><span data-stu-id="df34d-139">To personalize the text, you can insert placeholders, which are replaced with the appropriate data when they are displayed to users.</span></span> <span data-ttu-id="df34d-140">Při vkládání zástupného textu postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="df34d-140">To insert a placeholder, follow these steps:</span></span>

    1. <span data-ttu-id="df34d-141">Klepněte do textového pole do umístění, kde se má zástupný text zobrazit.</span><span class="sxs-lookup"><span data-stu-id="df34d-141">Click in the text box at the location where the placeholder should appear.</span></span>
    2. <span data-ttu-id="df34d-142">Klikněte na **Vložit zástupný text**.</span><span class="sxs-lookup"><span data-stu-id="df34d-142">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="df34d-143">V seznamu, který se zobrazí, vyberte vkládaný zástupný text.</span><span class="sxs-lookup"><span data-stu-id="df34d-143">In the list that is displayed, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="df34d-144">Klepněte na tlačítko **Vložit**.</span><span class="sxs-lookup"><span data-stu-id="df34d-144">Click **Insert**.</span></span>

7. <span data-ttu-id="df34d-145">Chcete-li přidat překlady oznámení, klikněte na **Překlady**.</span><span class="sxs-lookup"><span data-stu-id="df34d-145">To add translations of the notification, click **Translations**.</span></span> <span data-ttu-id="df34d-146">Ve formuláři, který se zobrazí, postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="df34d-146">In the form that is displayed, follow these steps:</span></span>

    1. <span data-ttu-id="df34d-147">Klikněte na tlačítko **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="df34d-147">Click **Add**.</span></span>
    2. <span data-ttu-id="df34d-148">V otevřeném seznamu vyberte jazyk, který chcete použít pro zadání textu.</span><span class="sxs-lookup"><span data-stu-id="df34d-148">In the list that is displayed, select the language in which you will enter the text.</span></span>
    3. <span data-ttu-id="df34d-149">V textovém poli **Přeložený text** zadejte text.</span><span class="sxs-lookup"><span data-stu-id="df34d-149">In the **Translated text** text box, enter the text.</span></span>
    4. <span data-ttu-id="df34d-150">Text můžete přizpůsobit vložením zástupného textu.</span><span class="sxs-lookup"><span data-stu-id="df34d-150">To personalize the text, insert placeholders.</span></span>
    5. <span data-ttu-id="df34d-151">Klepněte na tlačítko **Zavřít**.</span><span class="sxs-lookup"><span data-stu-id="df34d-151">Click **Close**.</span></span>

8. <span data-ttu-id="df34d-152">Klikněte na kartu **Příjemce**.</span><span class="sxs-lookup"><span data-stu-id="df34d-152">Click the **Recipient** tab.</span></span>
9. <span data-ttu-id="df34d-153">Zadejte, komu se mají odesílat oznámení.</span><span class="sxs-lookup"><span data-stu-id="df34d-153">Specify who the notifications are sent to.</span></span> <span data-ttu-id="df34d-154">Vyberte jednu z možností v následující tabulce a před přechodem na krok 10 postupujte podle dalších kroků pro tuto možnost.</span><span class="sxs-lookup"><span data-stu-id="df34d-154">Select one of the options in the following table, and then follow the additional steps for the option before you go to step 10.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="df34d-155">Parametr</span><span class="sxs-lookup"><span data-stu-id="df34d-155">Option</span></span></th>
    <th><span data-ttu-id="df34d-156">Příjemce oznámení</span><span class="sxs-lookup"><span data-stu-id="df34d-156">Notification recipients</span></span></th>
    <th><span data-ttu-id="df34d-157">Další kroky</span><span class="sxs-lookup"><span data-stu-id="df34d-157">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="df34d-158"><strong>Účastník</strong></span><span class="sxs-lookup"><span data-stu-id="df34d-158"><strong>Participant</strong></span></span></td>
    <td><span data-ttu-id="df34d-159">Uživatelé, kteří jsou přiřazeni k určité skupině nebo roli</span><span class="sxs-lookup"><span data-stu-id="df34d-159">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="df34d-160">Po výběru možnosti <strong>Účastník</strong> klepněte na kartu <strong>Založeno na roli</strong>.</span><span class="sxs-lookup"><span data-stu-id="df34d-160">After you select <strong>Participant</strong>, click the <strong>Role based</strong> tab.</span></span></li>
    <li><span data-ttu-id="df34d-161">V seznamu <strong>Typ účastníka</strong> vyberte typ skupiny nebo role, které chcete oznámení odeslat.</span><span class="sxs-lookup"><span data-stu-id="df34d-161">In the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="df34d-162">V seznamu <strong>Účastník</strong> vyberte skupinu nebo roli, které chcete oznámení odeslat.</span><span class="sxs-lookup"><span data-stu-id="df34d-162">In the <strong>Participant</strong> list, select the group or role to send notifications to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="df34d-163"><strong>Uživatel workflowu</strong></span><span class="sxs-lookup"><span data-stu-id="df34d-163"><strong>Workflow user</strong></span></span></td>
    <td><span data-ttu-id="df34d-164">Uživatelé zúčastnění v aktuálním workflowu</span><span class="sxs-lookup"><span data-stu-id="df34d-164">Users who participate in the current workflow</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="df34d-165">Po výběru možnosti <strong>Uživatel workflowu</strong> klepněte na kartu <strong>Uživatel workflowu</strong>.</span><span class="sxs-lookup"><span data-stu-id="df34d-165">After you select <strong>Workflow user</strong>, click the <strong>Workflow user</strong> tab.</span></span></li>
    <li><span data-ttu-id="df34d-166">V seznamu <strong>Uživatel workflowu</strong> vyberte uživatele, který se účastní workflowu.</span><span class="sxs-lookup"><span data-stu-id="df34d-166">In the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="df34d-167"><strong>Uživatel</strong></span><span class="sxs-lookup"><span data-stu-id="df34d-167"><strong>User</strong></span></span></td>
    <td><span data-ttu-id="df34d-168">Konkrétní uživatelé</span><span class="sxs-lookup"><span data-stu-id="df34d-168">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="df34d-169">Po výběru možnosti <strong>Uživatel</strong> klepněte na kartu <strong>Uživatel</strong>.</span><span class="sxs-lookup"><span data-stu-id="df34d-169">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="df34d-170">Vyberte uživatele, kterým chcete odeslat oznámení, a pak přesuňte tyto uživatele do seznamu <strong>Vybraní uživatelé</strong>.</span><span class="sxs-lookup"><span data-stu-id="df34d-170">Select the users to send notifications to, and then move these users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

10. <span data-ttu-id="df34d-171">Opakujte kroky 3 až 9 pro každou událost, kterou jste vybrali v kroku 2.</span><span class="sxs-lookup"><span data-stu-id="df34d-171">Repeat steps 3 through 9 for each event that you selected in step 2.</span></span>

## <a name="specify-a-final-approver"></a><span data-ttu-id="df34d-172"> Určení konečného schvalovatele</span><span class="sxs-lookup"><span data-stu-id="df34d-172">Specify a final approver</span></span>

<span data-ttu-id="df34d-173">Můžete určit konečného schvalovatele pro scénáře, kde schvalující je osoba, která dokument odeslala ke schválení a je používáno "zakázat schválení odesílatelem".</span><span class="sxs-lookup"><span data-stu-id="df34d-173">You can designate a final approver for scenarios where the approver is the person who submitted the document for approval and the "disallow approval by submitter" is being used.</span></span> <span data-ttu-id="df34d-174">Chcete-li určit konečného schvalovatele, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="df34d-174">Follow these steps to specify a final approver.</span></span>

1. <span data-ttu-id="df34d-175">V editoru workflowu klikněte pravým tlačítkem myši na prvek schválení a výběrem **Vlastnosti** otevřete formulář **Vlastnosti**.</span><span class="sxs-lookup"><span data-stu-id="df34d-175">In the workflow editor, right-click the approval element, and then select **Properties** to open the **Properties** form.</span></span>
2. <span data-ttu-id="df34d-176">V levém podokně klepněte na tlačítko **Pokročilá nastavení**.</span><span class="sxs-lookup"><span data-stu-id="df34d-176">In the left pane, click **Advanced settings**.</span></span>
3. <span data-ttu-id="df34d-177">Zaškrtněte políčko **Použít konečného schvalovatele**.</span><span class="sxs-lookup"><span data-stu-id="df34d-177">Select the **Use final approver** check box.</span></span>
4. <span data-ttu-id="df34d-178">V seznamu vyberte uživatele, který bude konečným schvalovatelem.</span><span class="sxs-lookup"><span data-stu-id="df34d-178">In the list, select a user to be the final approver.</span></span>

## <a name="set-a-time-limit"></a><span data-ttu-id="df34d-179">Nastavení časového limitu</span><span class="sxs-lookup"><span data-stu-id="df34d-179">Set a time limit</span></span>

<span data-ttu-id="df34d-180">Tento postup použijte, pokud je proces schvalování nutné dokončit v určitém čase.</span><span class="sxs-lookup"><span data-stu-id="df34d-180">Follow these steps if the approval process must be completed in a specific time.</span></span>

> [!NOTE]
> <span data-ttu-id="df34d-181">Možnosti, které v těchto krocích vyberete, přepíší možnosti vybrané v oblasti **Přiřazení** a **Eskalace** jednotlivých schvalovacích kroků.</span><span class="sxs-lookup"><span data-stu-id="df34d-181">The options that you select in these steps override the options that you selected in the **Assignment** and **Escalation** areas of each approval step.</span></span>

1. <span data-ttu-id="df34d-182">V levém podokně klepněte na tlačítko **Pokročilá nastavení**.</span><span class="sxs-lookup"><span data-stu-id="df34d-182">In the left pane, click **Advanced settings**.</span></span>
2. <span data-ttu-id="df34d-183">Zaškrtněte políčko **Nastavit časový limit pro prvek** **workflowu**.</span><span class="sxs-lookup"><span data-stu-id="df34d-183">Select the **Set a time limit for the workflow** **element** check box.</span></span>
3. <span data-ttu-id="df34d-184">V poli **Trvání** upřesněte, kdy má být schvalovací proces dokončen.</span><span class="sxs-lookup"><span data-stu-id="df34d-184">In the **Duration** field, specify when the approval process must be completed.</span></span> <span data-ttu-id="df34d-185">Vyberte některou z následujících možností:</span><span class="sxs-lookup"><span data-stu-id="df34d-185">Select one of the following options:</span></span>

    - <span data-ttu-id="df34d-186">**Hodiny** – zadejte počet hodin, dokdy musí být schvalovací proces dokončen.</span><span class="sxs-lookup"><span data-stu-id="df34d-186">**Hours** – Enter the number of hours in which the approval process must be completed.</span></span> <span data-ttu-id="df34d-187">Pak vyberte kalendář, který vaše organizace používá, a zadejte informace o pracovním týdnu vaší organizace.</span><span class="sxs-lookup"><span data-stu-id="df34d-187">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="df34d-188">**Dny** – zadejte počet dní, dokdy musí být schvalovací proces dokončen.</span><span class="sxs-lookup"><span data-stu-id="df34d-188">**Days** – Enter the number of days in which the approval process must be completed.</span></span> <span data-ttu-id="df34d-189">Pak vyberte kalendář, který vaše organizace používá, a zadejte informace o pracovním týdnu vaší organizace.</span><span class="sxs-lookup"><span data-stu-id="df34d-189">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="df34d-190">**Týdny** – zadejte počet týdnů, dokdy musí být schvalovací proces dokončen.</span><span class="sxs-lookup"><span data-stu-id="df34d-190">**Weeks** – Enter the number of weeks in which the approval process must be completed.</span></span>
    - <span data-ttu-id="df34d-191">**Měsíce** – vyberte den a týden, do kdy má být schvalovací proces dokončen.</span><span class="sxs-lookup"><span data-stu-id="df34d-191">**Months** – Select the day and week by which the approval process must be completed.</span></span> <span data-ttu-id="df34d-192">Můžete například požadovat, aby byl schvalovací proces dokončen do třetího pátku v daném měsíci.</span><span class="sxs-lookup"><span data-stu-id="df34d-192">For example, you may want the approval process to be completed by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="df34d-193">**Roky** – vyberte den, týden a měsíc, do kdy má být schvalovací proces dokončen.</span><span class="sxs-lookup"><span data-stu-id="df34d-193">**Years** – Select the day, week, and month by which the approval process must be completed.</span></span> <span data-ttu-id="df34d-194">Můžete například požadovat, aby byl schvalovací proces dokončen do třetího pátku v prosinci.</span><span class="sxs-lookup"><span data-stu-id="df34d-194">For example, you may want the approval process to be completed by Friday of the third week of December.</span></span>

4. <span data-ttu-id="df34d-195">Dojde-li k překročení časového limitu, systém u dokumentu provede akci.</span><span class="sxs-lookup"><span data-stu-id="df34d-195">If the time limit is exceeded, the system acts on the document.</span></span> <span data-ttu-id="df34d-196">V seznamu **Akce** vyberte akci, která má být provedena.</span><span class="sxs-lookup"><span data-stu-id="df34d-196">In the **Action** list, select the action that the system should take.</span></span>

## <a name="specify-which-actions-are-available-to-the-user"></a><span data-ttu-id="df34d-197">Určení dostupných akcí pro uživatele</span><span class="sxs-lookup"><span data-stu-id="df34d-197">Specify which actions are available to the user</span></span>

<span data-ttu-id="df34d-198">Po přidělení dokumentu uživateli ke schválení musí uživatel daný dokument zpracovat.</span><span class="sxs-lookup"><span data-stu-id="df34d-198">When a document is assigned to a user for approval, the user must act on the document.</span></span> <span data-ttu-id="df34d-199">Pomocí tohoto postupu určete akce, které může uživatel u odeslaného dokumentu provádět.</span><span class="sxs-lookup"><span data-stu-id="df34d-199">Follows these steps to specify which actions the user can take on the document that was submitted.</span></span>

1. <span data-ttu-id="df34d-200">V levém podokně klepněte na tlačítko **Pokročilá nastavení**.</span><span class="sxs-lookup"><span data-stu-id="df34d-200">In the left pane, click **Advanced settings**.</span></span>
2. <span data-ttu-id="df34d-201">Chcete-li uživatelům umožnit schválení dokumentu, zaškrtněte políčko **Schválit**.</span><span class="sxs-lookup"><span data-stu-id="df34d-201">Select the **Approve** check box if the user can approve the document.</span></span>
3. <span data-ttu-id="df34d-202">Chcete-li uživatelům zamítnout schválení dokumentu, zaškrtněte políčko **Zamítnout**.</span><span class="sxs-lookup"><span data-stu-id="df34d-202">Select the **Reject** check box the user can reject the document.</span></span>
4. <span data-ttu-id="df34d-203">Chcete-li uživatelům umožnit vyžádání změn v dokumentu, zaškrtněte políčko **Požadavek na změnu**.</span><span class="sxs-lookup"><span data-stu-id="df34d-203">Select the **Request change** check box the user can request changes to the document.</span></span>
5. <span data-ttu-id="df34d-204">Chcete-li uživateli umožnit, aby úlohu postoupil jinému uživateli ke schválení, zaškrtněte políčko **Delegovat**.</span><span class="sxs-lookup"><span data-stu-id="df34d-204">Select the **Delegate** check box if the user can assign the document to another user for approval.</span></span>

> [!NOTE]
> <span data-ttu-id="df34d-205">Políčko **Povolit akce z pracovního seznamu v podnikovém portálu** se již nepoužívá.</span><span class="sxs-lookup"><span data-stu-id="df34d-205">The **Enable actions from the work list in Enterprise Portal** check box has been deprecated.</span></span>

## <a name="configure-the-approval-steps"></a><span data-ttu-id="df34d-206"> Konfigurace kroků schválení</span><span class="sxs-lookup"><span data-stu-id="df34d-206">Configure the approval steps</span></span>

<span data-ttu-id="df34d-207">Schvalovací proces se skládá z kroků schválení.</span><span class="sxs-lookup"><span data-stu-id="df34d-207">An approval process consists of approval steps.</span></span> <span data-ttu-id="df34d-208">Pomocí následujícího postupu přidáte do schvalovacího procesu kroky a nakonfigurujete je.</span><span class="sxs-lookup"><span data-stu-id="df34d-208">Complete the following procedure to add steps the approval process and configure the steps.</span></span>

1. <span data-ttu-id="df34d-209">V editoru workflowu poklepejte na schvalovací proces.</span><span class="sxs-lookup"><span data-stu-id="df34d-209">In the workflow editor, double-click the approval process.</span></span> <span data-ttu-id="df34d-210">V editoru workflowu se zobrazí kroky schvalovacího procesu.</span><span class="sxs-lookup"><span data-stu-id="df34d-210">The workflow editor displays the steps of the approval process.</span></span>
2. <span data-ttu-id="df34d-211">Chcete-li přidat schvalovací krok, přetáhněte krok z oblasti **Prvky workflowu** na plátno.</span><span class="sxs-lookup"><span data-stu-id="df34d-211">To add an approval step, drag the step from the **Workflow elements** area to the canvas.</span></span>
3. <span data-ttu-id="df34d-212">Chcete-li nakonfigurovat schvalovací krok, získáte informace v části [Konfigurace schvalovacích kroků ve workflow](configure-approval-step-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="df34d-212">To configure an approval step, see [Configure approval steps in a workflow](configure-approval-step-workflow.md).</span></span>
