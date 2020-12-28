---
title: Správa žádostí o dovolenou v aplikaci Teams
description: Toto téma ukazuje, jak požádat o volno v aplikaci Dynamics 365 Human Resources v Microsoft Teams.
author: andreabichsel
manager: AnnBe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d24c257054578282f1a2eafa050094194a358aa0
ms.sourcegitcommit: 369639cd92e03fe792ed9d61a329d842aafa052f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/29/2020
ms.locfileid: "4417718"
---
# <a name="manage-leave-requests-in-teams"></a><span data-ttu-id="ae66e-103">Správa žádostí o dovolenou v aplikaci Teams</span><span class="sxs-lookup"><span data-stu-id="ae66e-103">Manage leave requests in Teams</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="ae66e-104">Aplikace Microsoft Dynamics 365 Human Resources v aplikaci Microsoft Teams vám umožňuje rychle požádat o volno a zobrazit informace o svém zůstatku volna přímo v Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="ae66e-104">The Microsoft Dynamics 365 Human Resources app in Microsoft Teams lets you quickly request time off and view your time-off balance information right in Microsoft Teams.</span></span> <span data-ttu-id="ae66e-105">Můžete komunikovat s robotem a požádat o informace a zahájit žádost o dovolenou.</span><span class="sxs-lookup"><span data-stu-id="ae66e-105">You can interact with a bot to request information and start a leave request.</span></span> <span data-ttu-id="ae66e-106">Karta **Volno** poskytuje podrobnější informace.</span><span class="sxs-lookup"><span data-stu-id="ae66e-106">The **Time off** tab provides more detailed information.</span></span> <span data-ttu-id="ae66e-107">Kromě toho můžete lidem posílat informace o svém nadcházejícím volnu v týmech a chatech mimo aplikaci Human Resources.</span><span class="sxs-lookup"><span data-stu-id="ae66e-107">You can also send people information about your upcoming time off in teams and chats outside the Human Resources app.</span></span>

## <a name="install-the-app"></a><span data-ttu-id="ae66e-108">Instalace aplikace</span><span class="sxs-lookup"><span data-stu-id="ae66e-108">Install the app</span></span>

<span data-ttu-id="ae66e-109">Aplikaci Human Resources najdete v obchodě Teams.</span><span class="sxs-lookup"><span data-stu-id="ae66e-109">You can find the Human Resources app in the Teams store.</span></span>

1. <span data-ttu-id="ae66e-110">V aplikaci Microsoft Teams zvolte tři tečky.</span><span class="sxs-lookup"><span data-stu-id="ae66e-110">In Microsoft Teams, select the ellipses.</span></span>

   ![Tři tečky aplikace pracovního volna Human Resources Teams](./media/hr-teams-leave-app-ellipses.png)
 
2. <span data-ttu-id="ae66e-112">Vyhledejte Dynamics 365 Human Resources a poté vyberte dlaždici **Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="ae66e-112">Search for Dynamics 365 Human Resources, and then select the **Human Resources** tile.</span></span>

   ![Dlaždice HR aplikace pracovního volna Human Resources Teams](./media/hr-teams-leave-app-human-resources-tile.png)

3. <span data-ttu-id="ae66e-114">Vyberte tlačítko **Přidat** pro instalaci aplikace.</span><span class="sxs-lookup"><span data-stu-id="ae66e-114">Select the **Add** button to install the app.</span></span>

   ![Instalace aplikace pracovního volna Human Resources Teams](./media/hr-teams-leave-app-in-store.png)

<span data-ttu-id="ae66e-116">Pokud vás aplikace nepřihlásí automaticky, vyberte kartu **Nastavení** pro přihlášení.</span><span class="sxs-lookup"><span data-stu-id="ae66e-116">If the app doesn't automatically sign you in, select the **Settings** tab to sign in.</span></span>

![Karta nastavení aplikace pracovního volna Human Resources Teams](./media/hr-teams-leave-app-settings-tab.png)

> [!NOTE]
> <span data-ttu-id="ae66e-118">Pokud nevidíte přihlašovací dialogové okno, zkontrolujte nastavení prohlížeče a povolte automaticky otevíraná okna.</span><span class="sxs-lookup"><span data-stu-id="ae66e-118">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span> 

<span data-ttu-id="ae66e-119">Pokud máte přístup k více než jedné instanci aplikace Human Resources, můžete vybrat prostředí, ke kterému se chcete připojit, na kartě **Nastavení**.</span><span class="sxs-lookup"><span data-stu-id="ae66e-119">If you have access to more than one instance of Human Resources, you can select which environment you want to connect to in the **Settings** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="ae66e-120">Aplikace nyní podporuje roli zabezpečení správce systému.</span><span class="sxs-lookup"><span data-stu-id="ae66e-120">The app now supports the System Administrator security role.</span></span>
 
## <a name="use-the-bot"></a><span data-ttu-id="ae66e-121">Použití robota</span><span class="sxs-lookup"><span data-stu-id="ae66e-121">Use the bot</span></span>

<span data-ttu-id="ae66e-122">Po instalaci aplikace se zobrazí uvítací zpráva, která vás informuje o typech akcí, které může robot provést vaším jménem.</span><span class="sxs-lookup"><span data-stu-id="ae66e-122">After the app installs, a welcome message appears, letting you know the types of actions the bot can take on your behalf.</span></span>

![Uvítací zpráva robota aplikace pracovního volna Human Resources Teams](./media/hr-teams-leave-app-bot.png)
 
> [!NOTE]
> <span data-ttu-id="ae66e-124">Při první interakci s robotem se možná budete muset přihlásit.</span><span class="sxs-lookup"><span data-stu-id="ae66e-124">When first interacting with the bot, you might need to sign in.</span></span> <span data-ttu-id="ae66e-125">Pokud nevidíte přihlašovací dialogové okno, zkontrolujte nastavení prohlížeče a povolte automaticky otevíraná okna.</span><span class="sxs-lookup"><span data-stu-id="ae66e-125">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span>

<span data-ttu-id="ae66e-126">Můžete požádat robota a následující akce:</span><span class="sxs-lookup"><span data-stu-id="ae66e-126">You can ask the bot to:</span></span>

- <span data-ttu-id="ae66e-127">Zobrazit informace o zůstatku volna pro každý typ volna, do kterého jste zaregistrováni.</span><span class="sxs-lookup"><span data-stu-id="ae66e-127">Show time-off balance information for each leave type you're enrolled in.</span></span>

   ![Zobrazení zůstatků aplikace pracovního volna Human Resources Teams](./media/hr-teams-leave-app-bot-balances.png)
 
- <span data-ttu-id="ae66e-129">Zobrazit další podrobnosti o konkrétním typu volna.</span><span class="sxs-lookup"><span data-stu-id="ae66e-129">Show additional details about a specific leave type.</span></span>

   ![Zobrazení podrobností aplikace pracovního volna Human Resources Teams](./media/hr-teams-leave-app-bot-details.png)

- <span data-ttu-id="ae66e-131">Zahájit žádost o volno za vás.</span><span class="sxs-lookup"><span data-stu-id="ae66e-131">Start a leave request for you.</span></span>

   ![Žádost o volno aplikace pracovního volna Human Resources Teams](./media/hr-teams-leave-app-bot-request.png)
 
<span data-ttu-id="ae66e-133">Po zahájení žádosti o dovolenou můžete upravit dny přímo na kartě.</span><span class="sxs-lookup"><span data-stu-id="ae66e-133">After you start a leave request, you can adjust the days right within the card.</span></span>

![Úprava žádosti aplikace pracovního volna Human Resources Teams](./media/hr-teams-leave-app-bot-edit.png)
 
<span data-ttu-id="ae66e-135">Až zadáte informace, vyberte **Odeslat** pro odeslání žádosti ke schválení.</span><span class="sxs-lookup"><span data-stu-id="ae66e-135">When you're done entering information, select **Submit** to submit it for approval.</span></span> <span data-ttu-id="ae66e-136">Můžete také zvolit **Uložit jako koncept** a vrátit se k žádosti později.</span><span class="sxs-lookup"><span data-stu-id="ae66e-136">You can also select **Save as draft** to come back to it later.</span></span>

![Odeslání žádosti aplikace pracovního volna Human Resources Teams](./media/hr-teams-leave-app-bot-submit.png)

## <a name="manage-your-leave-in-teams"></a><span data-ttu-id="ae66e-138">Správa volna v aplikaci Teams</span><span class="sxs-lookup"><span data-stu-id="ae66e-138">Manage your leave in Teams</span></span>

<span data-ttu-id="ae66e-139">Karta **Volno** umožňuje zobrazit:</span><span class="sxs-lookup"><span data-stu-id="ae66e-139">The **Time off** tab allows you to view:</span></span>

- <span data-ttu-id="ae66e-140">Informace o zůstatku pro každý typ volna, ke kterému jste zaregistrováni</span><span class="sxs-lookup"><span data-stu-id="ae66e-140">Balance information for each leave type you're enrolled in</span></span>

- <span data-ttu-id="ae66e-141">Nadcházející žádosti o volno</span><span class="sxs-lookup"><span data-stu-id="ae66e-141">Upcoming leave requests</span></span>

- <span data-ttu-id="ae66e-142">Žádosti o volno</span><span class="sxs-lookup"><span data-stu-id="ae66e-142">Time-off requests</span></span>

- <span data-ttu-id="ae66e-143">Koncept žádostí o volno</span><span class="sxs-lookup"><span data-stu-id="ae66e-143">Draft leave requests</span></span>

![Karta volna aplikace pracovního volna Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab.png)
 
### <a name="create-a-new-request"></a><span data-ttu-id="ae66e-145">Vytvoření nové žádosti</span><span class="sxs-lookup"><span data-stu-id="ae66e-145">Create a new request</span></span>

1. <span data-ttu-id="ae66e-146">Chcete-li vytvořit novou žádost o volno, zvolte **Nová žádost**.</span><span class="sxs-lookup"><span data-stu-id="ae66e-146">To create a new leave request, select **New request**.</span></span>

   ![Nová žádost aplikace pracovního volna Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab-new.png)

2. <span data-ttu-id="ae66e-148">Zadejte den nebo dny, na které chcete volno, a poté vyberte **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="ae66e-148">Enter the day or days you want to take off, and then select **Add**.</span></span>

   ![Přidání volna aplikace pracovního volna Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab-add.png)

3. <span data-ttu-id="ae66e-150">V případě potřeby zadejte kód důvodu.</span><span class="sxs-lookup"><span data-stu-id="ae66e-150">If applicable, enter a reason code.</span></span> <span data-ttu-id="ae66e-151">Také zadejte případné komentáře a přidejte všechny přílohy.</span><span class="sxs-lookup"><span data-stu-id="ae66e-151">Also enter any comments and add any attachments.</span></span>

4. <span data-ttu-id="ae66e-152">Až zadáte informace, napište **Odeslat** pro odeslání žádosti ke schválení.</span><span class="sxs-lookup"><span data-stu-id="ae66e-152">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="ae66e-153">Můžete také naspat **Uložit jako koncept** a vrátit se k žádosti později.</span><span class="sxs-lookup"><span data-stu-id="ae66e-153">You can also type **Save as draft** to come back to it later.</span></span>

### <a name="manage-draft-requests"></a><span data-ttu-id="ae66e-154">Správa konceptů žádostí</span><span class="sxs-lookup"><span data-stu-id="ae66e-154">Manage draft requests</span></span>

1. <span data-ttu-id="ae66e-155">Zvolte kartu **Koncepty**.</span><span class="sxs-lookup"><span data-stu-id="ae66e-155">Select the **Drafts** tab.</span></span>

   ![Karta konceptů aplikace pracovního volna Human Resources Teams](./media/hr-teams-leave-app-drafts-tab.png)

2. <span data-ttu-id="ae66e-157">Vyberte symbol tužky, chcete-li žádost upravit, nebo vyberte koš, chcete-li žádost odstranit.</span><span class="sxs-lookup"><span data-stu-id="ae66e-157">Select the pencil to edit the request, or select the trash can to delete the request.</span></span>

3. <span data-ttu-id="ae66e-158">Proveďte potřebné změny.</span><span class="sxs-lookup"><span data-stu-id="ae66e-158">Make any necessary changes.</span></span> <span data-ttu-id="ae66e-159">Až zadáte informace, napište **Odeslat** pro odeslání žádosti ke schválení.</span><span class="sxs-lookup"><span data-stu-id="ae66e-159">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="ae66e-160">Můžete také zvolit **Uložit jako koncept** a vrátit se k žádosti později.</span><span class="sxs-lookup"><span data-stu-id="ae66e-160">You can also select **Save as draft** to come back to it later.</span></span>

   ![Úprava konceptu aplikace pracovního volna Human Resources Teams](./media/hr-teams-leave-app-drafts-edit.png)
   
### <a name="respond-to-teams-notifications"></a><span data-ttu-id="ae66e-162">Odpovídejte na oznámení týmů</span><span class="sxs-lookup"><span data-stu-id="ae66e-162">Respond to Teams notifications</span></span>

<span data-ttu-id="ae66e-163">Když vy nebo pracovník, jehož jste schvalovatelem, odešlete žádost o pracovní volno, obdržíte oznámení v aplikaci Human Resources v Teams.</span><span class="sxs-lookup"><span data-stu-id="ae66e-163">When you or a worker you're an approver for submits a leave request, you'll receive a notification in the Human Resources app in Teams.</span></span> <span data-ttu-id="ae66e-164">Chcete-li oznámení zobrazit, vyberte jej.</span><span class="sxs-lookup"><span data-stu-id="ae66e-164">You can select the notification to view it.</span></span> <span data-ttu-id="ae66e-165">Oznámení se také zobrazují v oblasti **Chat**.</span><span class="sxs-lookup"><span data-stu-id="ae66e-165">Notifications also appear in the **Chat** area.</span></span>

<span data-ttu-id="ae66e-166">Pokud jste schvalovatel, můžete v oznámení zvolit možnosti **Schválit** nebo **Odmítnout**.</span><span class="sxs-lookup"><span data-stu-id="ae66e-166">If you're an approver, you can select **Approve** or **Deny** in the notification.</span></span> <span data-ttu-id="ae66e-167">Můžete také zadat volitelnou zprávu.</span><span class="sxs-lookup"><span data-stu-id="ae66e-167">You can also provide an optional message.</span></span>

![Oznámení o žádosti o pracovní volno v aplikaci Human Resources Teams](./media/hr-teams-leave-app-notification.png)

## <a name="send-upcoming-time-off-information-to-your-coworkers"></a><span data-ttu-id="ae66e-169">Pošlete nadcházející informace o volném čase vašim spolupracovníkům</span><span class="sxs-lookup"><span data-stu-id="ae66e-169">Send upcoming time-off information to your coworkers</span></span>

<span data-ttu-id="ae66e-170">Po instalaci aplikace Human Resources pro Teams můžete snadno poslat informace o svém nadcházejícím volnu svým spolupracovníkům v týmech nebo chatech.</span><span class="sxs-lookup"><span data-stu-id="ae66e-170">After you install the Human Resources app for Teams, you can easily send information about your upcoming time off to your coworkers in teams or chats.</span></span>

1. <span data-ttu-id="ae66e-171">V týmu nebo chatu v Teams vyberte tlačítko Human Resources pod oknem chatu.</span><span class="sxs-lookup"><span data-stu-id="ae66e-171">In a team or chat in Teams, select the Human Resources button below the chat window.</span></span>

   ![Tlačítko Human Resources pod oknem chatu](./media/hr-teams-leave-app-chat-button.png)

2. <span data-ttu-id="ae66e-173">Vyberte žádost o dovolenou, kterou chcete sdílet.</span><span class="sxs-lookup"><span data-stu-id="ae66e-173">Select the leave request you want to share.</span></span> <span data-ttu-id="ae66e-174">Pokud chcete sdílet koncept žádosti o dovolenou, nejprve vyberte **Koncepty**.</span><span class="sxs-lookup"><span data-stu-id="ae66e-174">If you want to share a draft leave request, select **Drafts** first.</span></span>

   ![Vyberte nadcházející žádost o dovolenou ke sdílení](./media/hr-teams-leave-app-chat-search.png)

<span data-ttu-id="ae66e-176">Vaše žádost o dovolenou se zobrazí v chatu.</span><span class="sxs-lookup"><span data-stu-id="ae66e-176">Your leave request will display in the chat.</span></span>

![Karta s žádostí o volno v Human Resources](./media/hr-teams-leave-app-chat-card.png)

<span data-ttu-id="ae66e-178">Pokud jste sdíleli koncept žádosti, zobrazí se jako koncept:</span><span class="sxs-lookup"><span data-stu-id="ae66e-178">If you shared a draft request, it will display as a draft:</span></span>

![Karta s konceptem žádosti o volno v Human Resources](./media/hr-teams-leave-app-chat-draft-card.png)

## <a name="view-your-teams-leave-calendar"></a><span data-ttu-id="ae66e-180">Zobrazení kalendáře pracovního volna týmu</span><span class="sxs-lookup"><span data-stu-id="ae66e-180">View your team's leave calendar</span></span>

<span data-ttu-id="ae66e-181">Pokud jste manažer s přímými podřízenými, můžete si prohlédnout schválené a nevyřízené pracovní volno vašeho týmu.</span><span class="sxs-lookup"><span data-stu-id="ae66e-181">If you're a manager with direct reports, you can view your team's approved and pending time off.</span></span>

1. <span data-ttu-id="ae66e-182">V aplikaci Human Resources v Teams vyberte **Volno**.</span><span class="sxs-lookup"><span data-stu-id="ae66e-182">In the Human Resources app in Teams, select **Time off**.</span></span>

2. <span data-ttu-id="ae66e-183">Vyberte **Kalendář týmu**.</span><span class="sxs-lookup"><span data-stu-id="ae66e-183">Select **Team calendar**.</span></span>

   ![Zobrazení kalendáře v aplikaci Human Resources Teams](./media/hr-teams-leave-app-view-calendar.png)

<span data-ttu-id="ae66e-185">Kalendář zobrazuje schválené a nevyřízené volno vašich přímých podřízených.</span><span class="sxs-lookup"><span data-stu-id="ae66e-185">The calendar displays your direct reports' approved and pending time off.</span></span>

![Kalendář volna v aplikaci Human Resources Teams](./media/hr-teams-leave-app-calendar.png)

## <a name="troubleshooting"></a><span data-ttu-id="ae66e-187">Řešení potíží</span><span class="sxs-lookup"><span data-stu-id="ae66e-187">Troubleshooting</span></span>

<span data-ttu-id="ae66e-188">Pokud máte potíže s přihlášením nebo používáním aplikace Human Resources Teams, zkuste problémy vyřešit podle těchto pokynů.</span><span class="sxs-lookup"><span data-stu-id="ae66e-188">If you're having trouble signing into or using the Human Resources Teams app, try following these troubleshooting instructions.</span></span> <span data-ttu-id="ae66e-189">Pokud problémy přetrvávají i po pokusu o vyřešení, obraťte se na podporu.</span><span class="sxs-lookup"><span data-stu-id="ae66e-189">If you're still having problems after troubleshooting, contact Support.</span></span> <span data-ttu-id="ae66e-190">Pro další informace si přečtěte [Získání podpory](hr-admin-troubleshooting-support.md).</span><span class="sxs-lookup"><span data-stu-id="ae66e-190">For more information, see [Get support](hr-admin-troubleshooting-support.md).</span></span>

### <a name="cant-sign-into-the-human-resources-app-in-teams"></a><span data-ttu-id="ae66e-191">Nelze se přihlásit do aplikace Human Resources v Teams</span><span class="sxs-lookup"><span data-stu-id="ae66e-191">Can't sign into the Human Resources app in Teams</span></span>

<span data-ttu-id="ae66e-192">Pokud se nemůžete do aplikace přihlásit, je možné, že účet, pomocí kterého se přihlašujete do Microsoft Teams není spojen se záznamem zaměstnance v Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="ae66e-192">If you can't sign into the app, it's possible that the account you're using to sign into Microsoft Teams isn't associated with an employee record in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="ae66e-193">Požádejtea správce systému o ověření, jestli je váš záznam zaměstnance správně přidružen.</span><span class="sxs-lookup"><span data-stu-id="ae66e-193">Contact your system administrator to ensure your employee record is correctly associated.</span></span>

### <a name="error-when-approving-leave-requests-in-the-human-resources-app-in-teams"></a><span data-ttu-id="ae66e-194">Chyba při schvalování žádostí o dovolenou v aplikaci Human Resources v Teams</span><span class="sxs-lookup"><span data-stu-id="ae66e-194">Error when approving leave requests in the Human Resources app in Teams</span></span>

<span data-ttu-id="ae66e-195">Pokud se vám při pokusu o schválení žádostí o dovolenou v aplikaci Teams zobrazí chyba, zkuste v rámci řešení potíží následující kroky:</span><span class="sxs-lookup"><span data-stu-id="ae66e-195">If you receive an error when you're trying to approve leave requests in the Teams app, try the following troubleshooting steps:</span></span>

1. <span data-ttu-id="ae66e-196">Ověřte, že účet, který používáte k přihlášení k Microsoft Teams, je stejný, jaký používáte pro přístup k Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="ae66e-196">Verify that the account you're using to sign into Microsoft Teams is the same one you use for accessing Dynamics 365 Human Resources.</span></span>

2. <span data-ttu-id="ae66e-197">Ověřte, jestli jste platným schvalovatelem požadavku, a to kontrolou nastavení pracovního postupu pro schválení dovolené.</span><span class="sxs-lookup"><span data-stu-id="ae66e-197">Verify that you're a valid approver for the request by checking the workflow settings for leave approval.</span></span> <span data-ttu-id="ae66e-198">Další informace o pracovních postupech žádostí o dovolenou najdete v tématu [Vytvoření pracovního postupu žádosti o dovolenou](hr-leave-and-absence-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="ae66e-198">For more information about leave request workflows, see [Create a leave request workflow](hr-leave-and-absence-workflow.md).</span></span>

## <a name="known-accessibility-issues"></a><span data-ttu-id="ae66e-199">Známé problémy s usnadněním</span><span class="sxs-lookup"><span data-stu-id="ae66e-199">Known accessibility issues</span></span>

<span data-ttu-id="ae66e-200">Aplikace Human Resources v Teams má následující problémy s usnadněním, na jejichž řešení pracujeme pro budoucí verze.</span><span class="sxs-lookup"><span data-stu-id="ae66e-200">The Human Resources app in Teams has the following accessibility issues that we're working on fixing in future releases.</span></span>

| <span data-ttu-id="ae66e-201">Výdej</span><span class="sxs-lookup"><span data-stu-id="ae66e-201">Issue</span></span> | <span data-ttu-id="ae66e-202">Řešení nebo vysvětlení</span><span class="sxs-lookup"><span data-stu-id="ae66e-202">Workaround or explanation</span></span> |
| --- | --- |
| <span data-ttu-id="ae66e-203">Zvětšení plochy o 400 % skryje některá tlačítka akcí.</span><span class="sxs-lookup"><span data-stu-id="ae66e-203">Zooming to 400% on desktop hides some of the action buttons from view.</span></span> | <span data-ttu-id="ae66e-204">Doporučujeme místo toho používat lupu, dokud nebudeme moci tuto úroveň zvětšení podporovat.</span><span class="sxs-lookup"><span data-stu-id="ae66e-204">We recommend using a magnifier instead until we can support this zoom level.</span></span> |
| <span data-ttu-id="ae66e-205">Na kartě **Volno** hlasový komentář oznamuje akci tlačítka při čtení záhlaví mřížky volna.</span><span class="sxs-lookup"><span data-stu-id="ae66e-205">On the **Time off** tab, voiceover announces a button action while reading the header for the time-off grid.</span></span> | <span data-ttu-id="ae66e-206">Záhlaví a prvky v mřížce jsou seskupeny podle roku a jsou sbalitelné.</span><span class="sxs-lookup"><span data-stu-id="ae66e-206">The header and elements within the grid are grouped by year, and they're collapsible.</span></span> <span data-ttu-id="ae66e-207">Komentář to interpretuje jako položku s akcemi, kterou ale není.</span><span class="sxs-lookup"><span data-stu-id="ae66e-207">Voiceover interprets this as an actionable item, but it isn't.</span></span> |
| <span data-ttu-id="ae66e-208">Pokud potáhnete prstem, když je otevřeno místní okno nebo nabídka, hlasový komentář přeskočí čtení obsahu místního okna nebo nabídky.</span><span class="sxs-lookup"><span data-stu-id="ae66e-208">If you swipe while a popup or menu is open, voiceover skips reading the popup or menu contents.</span></span> | <span data-ttu-id="ae66e-209">Prozkoumejte obsah pomocí skenování prstem.</span><span class="sxs-lookup"><span data-stu-id="ae66e-209">Explore the content using finger scanning.</span></span> |
| <span data-ttu-id="ae66e-210">Na kartě **Volno** je při přechodu na **Kód důvodu** v nové žádosti potřeba potáhnutí prstem navíc.</span><span class="sxs-lookup"><span data-stu-id="ae66e-210">On the **Time off** tab, there's an extra swipe gesture when navigating to **Reason code** in a new request.</span></span> | <span data-ttu-id="ae66e-211">Neexistuje žádný skrytý ovládací prvek, ke kterému se potáhnutí prstem pokouší dostat.</span><span class="sxs-lookup"><span data-stu-id="ae66e-211">There is no hidden control that the swipe navigation is trying to get to.</span></span> |
| <span data-ttu-id="ae66e-212">Na kartě **Volno**, pokud potáhnete prstem, když je kalendář otevřený, skončíte mimo ovládací prvek namísto horní části v nové žádosti nebo během úpravy požadavku.</span><span class="sxs-lookup"><span data-stu-id="ae66e-212">On the **Time off** tab, if you swipe while the calendar is open, you end up outside the control instead of at the top in a new request or while editing a request.</span></span> | <span data-ttu-id="ae66e-213">Když dosáhnete položky **Přejít na dnešek**, považujte to za konec ovládacího prvku a potáhnutím prstem opačným směrem se dostanete zpět nahoru.</span><span class="sxs-lookup"><span data-stu-id="ae66e-213">When you reach **Go to today**, consider that to be the end of the control and swipe in the reverse direction to get back to the top.</span></span> |
| <span data-ttu-id="ae66e-214">Komentář nečte popisky kalendářních dat.</span><span class="sxs-lookup"><span data-stu-id="ae66e-214">Voiceover doesn't read the labels for dates.</span></span> | <span data-ttu-id="ae66e-215">Data v párech jsou vždy **Počáteční datum** a **Koncové datum**.</span><span class="sxs-lookup"><span data-stu-id="ae66e-215">The dates encountered in pairs are always **Start date** and **End date**.</span></span> |
| <span data-ttu-id="ae66e-216">Na kartě **Chat**, když zadáte datum při používání asistenčního nástroje nebo navigace pomocí klávesnice, přeskočí fokus zpět na začátek.</span><span class="sxs-lookup"><span data-stu-id="ae66e-216">On the **Chat** tab, the focus jumps back to the top when you enter a date while using the assistive tool or keyboard navigation.</span></span> | <span data-ttu-id="ae66e-217">Stiskněte klávesu Tab, dokud se znovu nedostanete do oblasti zadávání.</span><span class="sxs-lookup"><span data-stu-id="ae66e-217">Tab until you reach your input area again.</span></span> |

## <a name="privacy-notice"></a><span data-ttu-id="ae66e-218">Oznámení o ochraně osobních údajů</span><span class="sxs-lookup"><span data-stu-id="ae66e-218">Privacy notice</span></span>

### <a name="microsoft-language-understanding-intelligent-service-luis"></a><span data-ttu-id="ae66e-219">Microsoft Language Understanding Intelligent Service (LUIS)</span><span class="sxs-lookup"><span data-stu-id="ae66e-219">Microsoft Language Understanding Intelligent Service (LUIS)</span></span>

<span data-ttu-id="ae66e-220">S robotem Dynamics 365 Human Resources v aplikaci Microsoft Teams jsou textové vstupy uživatele analyzovány pro porozumění základním dotazům/záměrům.</span><span class="sxs-lookup"><span data-stu-id="ae66e-220">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="ae66e-221">Vstup uživatele, například „Vyhledat účet Contoso“, je přesměrován na jednu ze služeb Cognitive Services společnosti Microsoft nazvanou Language Understanding Intelligent Service (LUIS).</span><span class="sxs-lookup"><span data-stu-id="ae66e-221">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="ae66e-222">Přečtěte si více o LUIS  [zde](https://www.luis.ai/).</span><span class="sxs-lookup"><span data-stu-id="ae66e-222">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="ae66e-223">Služba LUIS ujasňuje nebo chápe záměr vstupu uživatele (v tomto případě je záměrem najít informace) a cílovou entitu (v tomto případě je zamýšlenou entitou účet s názvem Contoso).</span><span class="sxs-lookup"><span data-stu-id="ae66e-223">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="ae66e-224">Tyto informace jsou poté předány do řešení  [Azure Bot Framework](https://azure.microsoft.com/services/bot-service/) společnosti Microsoft, které interaguje s daty z Dynamics 365 Human Resources a načte požadované informace pro uživatelský dotaz.</span><span class="sxs-lookup"><span data-stu-id="ae66e-224">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/), which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="ae66e-225">Instalací a umožněním přístupu k používání robota souhlasíte s tím, že umožníte službě LUIS a rámci robota Azure zpracovat záměr za vstupem, což má za následek vylepšenou konverzační uživatelskou zkušenost.</span><span class="sxs-lookup"><span data-stu-id="ae66e-225">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="ae66e-226">Služba LUIS a rámec robota Azure mohou mít ve srovnání s Dynamics 365 Human Resources různé úrovně shody.</span><span class="sxs-lookup"><span data-stu-id="ae66e-226">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="ae66e-227">Zatímco služba LUIS má přístup pouze k uživatelským dotazům a není určena k připojení k datům nebo účtu uživatele Dynamics 365 Human Resources, uživatel robota Dynamics 365 Human Resources může dobrovolně zadat dotaz obsahující zákaznická data, osobní údaje nebo jiná data a takový obsah dotazu by mohl být zaslán do služby LUIS a do rámce robota Azure.</span><span class="sxs-lookup"><span data-stu-id="ae66e-227">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="ae66e-228">Obsah dotazů a zpráv uživatele je v systému LUIS uchováván maximálně 30 dní, je šifrován a nepoužívá se pro školení ani zlepšení služeb.</span><span class="sxs-lookup"><span data-stu-id="ae66e-228">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="ae66e-229">Přečtěte si více o Cognitive Services  [zde](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span><span class="sxs-lookup"><span data-stu-id="ae66e-229">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="ae66e-230">Chcete-li spravovat nastavení administrátora pro aplikace v Microsoft Teams, přejděte do [centra pro správu Microsoft Teams](https://admin.teams.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="ae66e-230">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span>

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a><span data-ttu-id="ae66e-231">Microsoft Teams  Azure Event Grid a Azure Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="ae66e-231">Microsoft Teams, Azure Event Grid, and Azure Cosmos DB</span></span>

<span data-ttu-id="ae66e-232">Při použití aplikace Dynamics 365 Human Resources v Microsoft Teams mohou některá data zákazníků téct mimo geografickou oblast, kde je nasazena služba Human Resources vašeho klienta.</span><span class="sxs-lookup"><span data-stu-id="ae66e-232">When using the Dynamics 365 Human Resources app in Microsoft Teams, certain customer data may flow outside of the geographic region where your tenant’s Human Resources service is deployed.</span></span>

<span data-ttu-id="ae66e-233">Dynamics 365 Human Resources přenáší podrobnosti o žádosti o pracovní volno a úkolu pracovního postupu do Microsoft Azure Event Grid a Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="ae66e-233">Dynamics 365 Human Resources transmits the employee’s leave request and workflow task details to Microsoft Azure Event Grid and Microsoft Teams.</span></span> <span data-ttu-id="ae66e-234">Tato data mohou být uložena v Event Grid Microsoft Azure až 24 hodin a budou zpracována ve Spojených státech, jsou šifrována během přenosu a v klidu a nejsou používána společností Microsoft nebo jejími subprocesory pro školení nebo vylepšení služeb.</span><span class="sxs-lookup"><span data-stu-id="ae66e-234">This data may be stored in Microsoft Azure Event Grid for up to 24 hours and will be processed in the United States, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="ae66e-235">Chcete-li zjistit, kde jsou vaše data uložena v Teams, přečtěte si [Umístění dat v Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="ae66e-235">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span></span>

<span data-ttu-id="ae66e-236">Při konverzaci s chatovacím robotem v aplikaci Human Resources může být obsah konverzace uložen v Azure Cosmos DB a přenesen do Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="ae66e-236">While conversing with the chat bot in the Human Resources app, the conversation content may be stored in Azure Cosmos DB and transmitted to Microsoft Teams.</span></span> <span data-ttu-id="ae66e-237">Tato data mohou být uložena v Azure Cosmos DB po dobu až 24 hodin a mohou být zpracovávána mimo geografickou oblast, kde je nasazena služba Human Resources vašeho nájemce, je šifrována během přenosu a v klidu a není používána společností Microsoft nebo jejími subprocesory pro školení nebo vylepšení služeb.</span><span class="sxs-lookup"><span data-stu-id="ae66e-237">This data may be stored in Azure Cosmos DB for up to 24 hours and may be processed outside of the geographic region where your tenant's Human Resources service is deployed, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="ae66e-238">Chcete-li zjistit, kde jsou vaše data uložena v Teams, přečtěte si [Umístění dat v Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="ae66e-238">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span></span>
 
<span data-ttu-id="ae66e-239">Chcete-li omezit přístup k aplikaci Human Resources v Microsoft Teams pro vaši organizaci nebo uživatele ve vaší organizaci, přečtěte si [Spravujte zásady oprávnění aplikace v Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span><span class="sxs-lookup"><span data-stu-id="ae66e-239">To restrict access to the Human Resources app in Microsoft Teams for your organization or users within your organization, see [Manage app permission policies in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="see-also"></a><span data-ttu-id="ae66e-240">Viz také</span><span class="sxs-lookup"><span data-stu-id="ae66e-240">See also</span></span>

[<span data-ttu-id="ae66e-241">Stažení a instalace aplikace Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="ae66e-241">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="ae66e-242">Centrum nápovědy Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="ae66e-242">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="ae66e-243">Aplikace Human Resources v Teams</span><span class="sxs-lookup"><span data-stu-id="ae66e-243">Human Resources app in Teams</span></span>](hr-admin-teams-leave-app.md)
