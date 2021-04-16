---
title: Správa žádostí o dovolenou v aplikaci Teams
description: Toto téma ukazuje, jak požádat o volno v aplikaci Dynamics 365 Human Resources v Microsoft Teams.
author: andreabichsel
ms.date: 02/23/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 72fa3309b77717d0291b8b6828ed5bc4c65e95ab
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5790565"
---
# <a name="manage-leave-requests-in-teams"></a><span data-ttu-id="6907c-103">Správa žádostí o dovolenou v aplikaci Teams</span><span class="sxs-lookup"><span data-stu-id="6907c-103">Manage leave requests in Teams</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="6907c-104">Aplikace Dynamics 365 Human Resources v aplikaci Microsoft Teams vám umožňuje rychle požádat o volno a zobrazit informace o svém zůstatku volna přímo v Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="6907c-104">The Dynamics 365 Human Resources app in Microsoft Teams lets you quickly request time off and view your time-off balance information right in Microsoft Teams.</span></span> <span data-ttu-id="6907c-105">Můžete komunikovat s robotem a požádat o informace a zahájit žádost o dovolenou.</span><span class="sxs-lookup"><span data-stu-id="6907c-105">You can interact with a bot to request information and start a leave request.</span></span> <span data-ttu-id="6907c-106">Karta **Volno** poskytuje podrobnější informace.</span><span class="sxs-lookup"><span data-stu-id="6907c-106">The **Time off** tab provides more detailed information.</span></span> <span data-ttu-id="6907c-107">Kromě toho můžete lidem posílat informace o svém nadcházejícím volnu v Teams a chatech mimo aplikaci Human Resources.</span><span class="sxs-lookup"><span data-stu-id="6907c-107">You can also send people information about your upcoming time off in Teams and chats outside the Human Resources app.</span></span>

## <a name="install-the-app"></a><span data-ttu-id="6907c-108">Instalace aplikace</span><span class="sxs-lookup"><span data-stu-id="6907c-108">Install the app</span></span>

<span data-ttu-id="6907c-109">Aplikaci Dynamics 365 Human Resources najdete v obchodě Teams.</span><span class="sxs-lookup"><span data-stu-id="6907c-109">You can find the Dynamics 365 Human Resources app in the Teams store.</span></span>

1. <span data-ttu-id="6907c-110">V aplikaci Microsoft Teams zvolte tři tečky.</span><span class="sxs-lookup"><span data-stu-id="6907c-110">In Microsoft Teams, select the ellipses.</span></span>

   ![Tři tečky aplikace pracovního volna Human Resources Teams](./media/hr-teams-leave-app-ellipses.png)
 
2. <span data-ttu-id="6907c-112">Vyhledejte Dynamics 365 Human Resources a poté vyberte dlaždici **Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="6907c-112">Search for Dynamics 365 Human Resources, and then select the **Human Resources** tile.</span></span>

   ![Dlaždice HR aplikace pracovního volna Human Resources Teams](./media/hr-teams-leave-app-human-resources-tile.png)

3. <span data-ttu-id="6907c-114">Vyberte tlačítko **Přidat** pro instalaci aplikace.</span><span class="sxs-lookup"><span data-stu-id="6907c-114">Select the **Add** button to install the app.</span></span>

   ![Instalace aplikace pracovního volna Human Resources Teams](./media/hr-teams-leave-app-in-store.png)

<span data-ttu-id="6907c-116">Pokud vás aplikace nepřihlásí automaticky, vyberte kartu **Nastavení** pro přihlášení.</span><span class="sxs-lookup"><span data-stu-id="6907c-116">If the app doesn't automatically sign you in, select the **Settings** tab to sign in.</span></span>

![Karta nastavení aplikace pracovního volna Human Resources Teams](./media/hr-teams-leave-app-settings-tab.png)

> [!NOTE]
> <span data-ttu-id="6907c-118">Pokud nevidíte přihlašovací dialogové okno, zkontrolujte nastavení prohlížeče a povolte automaticky otevíraná okna.</span><span class="sxs-lookup"><span data-stu-id="6907c-118">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span> 

<span data-ttu-id="6907c-119">Pokud máte přístup k více než jedné instanci aplikace Human Resources, můžete vybrat prostředí, ke kterému se chcete připojit, na kartě **Nastavení**.</span><span class="sxs-lookup"><span data-stu-id="6907c-119">If you have access to more than one instance of Human Resources, you can select which environment you want to connect to in the **Settings** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="6907c-120">Aplikace nyní podporuje roli zabezpečení správce systému.</span><span class="sxs-lookup"><span data-stu-id="6907c-120">The app now supports the System Administrator security role.</span></span>
 
## <a name="use-the-bot"></a><span data-ttu-id="6907c-121">Použití robota</span><span class="sxs-lookup"><span data-stu-id="6907c-121">Use the bot</span></span>

<span data-ttu-id="6907c-122">Po instalaci aplikace se zobrazí uvítací zpráva, která vás informuje o typech akcí, které může robot provést vaším jménem.</span><span class="sxs-lookup"><span data-stu-id="6907c-122">After the app installs, a welcome message appears, letting you know the types of actions the bot can take on your behalf.</span></span>

![Uvítací zpráva robota aplikace pracovního volna Human Resources Teams](./media/hr-teams-leave-app-bot.png)
 
> [!NOTE]
> <span data-ttu-id="6907c-124">Při první interakci s robotem se možná budete muset přihlásit.</span><span class="sxs-lookup"><span data-stu-id="6907c-124">When first interacting with the bot, you might need to sign in.</span></span> <span data-ttu-id="6907c-125">Pokud nevidíte přihlašovací dialogové okno, zkontrolujte nastavení prohlížeče a povolte automaticky otevíraná okna.</span><span class="sxs-lookup"><span data-stu-id="6907c-125">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span>

<span data-ttu-id="6907c-126">Můžete požádat robota a následující akce:</span><span class="sxs-lookup"><span data-stu-id="6907c-126">You can ask the bot to:</span></span>

- <span data-ttu-id="6907c-127">Zahájit žádost o volno za vás.</span><span class="sxs-lookup"><span data-stu-id="6907c-127">Start a leave request for you.</span></span>

  ![Zahájení žádosti o volno v chatu Teams](./media/hr-teams-leave-app-initiate.png)

- <span data-ttu-id="6907c-129">Chatovací robot za vás vyplní žádost o volno.</span><span class="sxs-lookup"><span data-stu-id="6907c-129">The chat bot will populate a leave request for you.</span></span> <span data-ttu-id="6907c-130">Vyberte možnost **Požádat o volno** a upravte podrobnosti své žádosti.</span><span class="sxs-lookup"><span data-stu-id="6907c-130">Select **Request time off** and edit the details for your request.</span></span>

  ![Úprava podrobností žádosti o volno](./media/hr-teams-leave-app-details.png)

- <span data-ttu-id="6907c-132">Po dokončení úprav podrobností žádosti o volno vyberte **Odeslat** a předejte žádost ke schválení.</span><span class="sxs-lookup"><span data-stu-id="6907c-132">When you're done editing your leave request details, select **Submit** to submit it for approval.</span></span>

  ![Odeslání žádosti o volno](./media/hr-teams-leave-app-submit.png)

## <a name="manage-your-leave-in-teams"></a><span data-ttu-id="6907c-134">Správa volna v aplikaci Teams</span><span class="sxs-lookup"><span data-stu-id="6907c-134">Manage your leave in Teams</span></span>

<span data-ttu-id="6907c-135">Karta **Volno** umožňuje zobrazit:</span><span class="sxs-lookup"><span data-stu-id="6907c-135">The **Time off** tab allows you to view:</span></span> 

- <span data-ttu-id="6907c-136">Informace o zůstatku pro každý typ volna, ke kterému jste zaregistrováni</span><span class="sxs-lookup"><span data-stu-id="6907c-136">Balance information for each leave type you're enrolled in</span></span>

- <span data-ttu-id="6907c-137">Nadcházející žádosti o volno</span><span class="sxs-lookup"><span data-stu-id="6907c-137">Upcoming leave requests</span></span>

- <span data-ttu-id="6907c-138">Žádosti o volno</span><span class="sxs-lookup"><span data-stu-id="6907c-138">Time-off requests</span></span>

- <span data-ttu-id="6907c-139">Koncept žádostí o volno</span><span class="sxs-lookup"><span data-stu-id="6907c-139">Draft leave requests</span></span>

![Karta volna aplikace pracovního volna Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab.png)
 
### <a name="create-a-new-request"></a><span data-ttu-id="6907c-141">Vytvoření nové žádosti</span><span class="sxs-lookup"><span data-stu-id="6907c-141">Create a new request</span></span>

1. <span data-ttu-id="6907c-142">Chcete-li vytvořit novou žádost o volno, zvolte **Nová žádost**.</span><span class="sxs-lookup"><span data-stu-id="6907c-142">To create a new leave request, select **New request**.</span></span>

   ![Nová žádost aplikace pracovního volna Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab-new.png)

2. <span data-ttu-id="6907c-144">Zadejte den nebo dny, na které chcete volno, a poté vyberte **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="6907c-144">Enter the day or days you want to take off, and then select **Add**.</span></span>

   ![Přidání volna aplikace pracovního volna Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab-add.png)

3. <span data-ttu-id="6907c-146">V případě potřeby zadejte kód důvodu.</span><span class="sxs-lookup"><span data-stu-id="6907c-146">If applicable, enter a reason code.</span></span> <span data-ttu-id="6907c-147">Také zadejte případné komentáře a přidejte všechny přílohy.</span><span class="sxs-lookup"><span data-stu-id="6907c-147">Also enter any comments and add any attachments.</span></span>

4. <span data-ttu-id="6907c-148">Až zadáte informace, napište **Odeslat** pro odeslání žádosti ke schválení.</span><span class="sxs-lookup"><span data-stu-id="6907c-148">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="6907c-149">Můžete také naspat **Uložit jako koncept** a vrátit se k žádosti později.</span><span class="sxs-lookup"><span data-stu-id="6907c-149">You can also type **Save as draft** to come back to it later.</span></span>

### <a name="manage-draft-requests"></a><span data-ttu-id="6907c-150">Správa konceptů žádostí</span><span class="sxs-lookup"><span data-stu-id="6907c-150">Manage draft requests</span></span>

1. <span data-ttu-id="6907c-151">Zvolte kartu **Koncepty**.</span><span class="sxs-lookup"><span data-stu-id="6907c-151">Select the **Drafts** tab.</span></span>

   ![Karta konceptů aplikace pracovního volna Human Resources Teams](./media/hr-teams-leave-app-drafts-tab.png)

2. <span data-ttu-id="6907c-153">Vyberte symbol tužky, chcete-li žádost upravit, nebo vyberte koš, chcete-li žádost odstranit.</span><span class="sxs-lookup"><span data-stu-id="6907c-153">Select the pencil to edit the request, or select the trash can to delete the request.</span></span>

3. <span data-ttu-id="6907c-154">Proveďte potřebné změny.</span><span class="sxs-lookup"><span data-stu-id="6907c-154">Make any necessary changes.</span></span> <span data-ttu-id="6907c-155">Až zadáte informace, napište **Odeslat** pro odeslání žádosti ke schválení.</span><span class="sxs-lookup"><span data-stu-id="6907c-155">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="6907c-156">Můžete také zvolit **Uložit jako koncept** a vrátit se k žádosti později.</span><span class="sxs-lookup"><span data-stu-id="6907c-156">You can also select **Save as draft** to come back to it later.</span></span>

   ![Úprava konceptu aplikace pracovního volna Human Resources Teams](./media/hr-teams-leave-app-drafts-edit.png)
   
### <a name="respond-to-teams-notifications"></a><span data-ttu-id="6907c-158">Odpovídejte na oznámení týmů</span><span class="sxs-lookup"><span data-stu-id="6907c-158">Respond to Teams notifications</span></span>

<span data-ttu-id="6907c-159">Když vy nebo pracovník, jehož jste schvalovatelem, odešlete žádost o pracovní volno, obdržíte oznámení v aplikaci Human Resources v Teams.</span><span class="sxs-lookup"><span data-stu-id="6907c-159">When you or a worker you're an approver for submits a leave request, you'll receive a notification in the Human Resources app in Teams.</span></span> <span data-ttu-id="6907c-160">Chcete-li oznámení zobrazit, vyberte jej.</span><span class="sxs-lookup"><span data-stu-id="6907c-160">You can select the notification to view it.</span></span> <span data-ttu-id="6907c-161">Oznámení se také zobrazují v oblasti **Chat**.</span><span class="sxs-lookup"><span data-stu-id="6907c-161">Notifications also appear in the **Chat** area.</span></span>

<span data-ttu-id="6907c-162">Pokud jste schvalovatel, můžete v oznámení zvolit možnosti **Schválit** nebo **Odmítnout**.</span><span class="sxs-lookup"><span data-stu-id="6907c-162">If you're an approver, you can select **Approve** or **Deny** in the notification.</span></span> <span data-ttu-id="6907c-163">Můžete také zadat volitelnou zprávu.</span><span class="sxs-lookup"><span data-stu-id="6907c-163">You can also provide an optional message.</span></span>

![Oznámení o žádosti o pracovní volno v aplikaci Human Resources Teams](./media/hr-teams-leave-app-notification.png)

## <a name="send-upcoming-time-off-information-to-your-coworkers"></a><span data-ttu-id="6907c-165">Pošlete nadcházející informace o volném čase vašim spolupracovníkům</span><span class="sxs-lookup"><span data-stu-id="6907c-165">Send upcoming time-off information to your coworkers</span></span>

<span data-ttu-id="6907c-166">Po instalaci aplikace Human Resources pro Teams můžete snadno poslat informace o svém nadcházejícím volnu svým spolupracovníkům v týmech nebo chatech.</span><span class="sxs-lookup"><span data-stu-id="6907c-166">After you install the Human Resources app for Teams, you can easily send information about your upcoming time off to your coworkers in teams or chats.</span></span>

1. <span data-ttu-id="6907c-167">V týmu nebo chatu v Teams vyberte tlačítko Human Resources pod oknem chatu.</span><span class="sxs-lookup"><span data-stu-id="6907c-167">In a team or chat in Teams, select the Human Resources button below the chat window.</span></span>

   ![Tlačítko Human Resources pod oknem chatu](./media/hr-teams-leave-app-chat-button.png)

2. <span data-ttu-id="6907c-169">Vyberte žádost o dovolenou, kterou chcete sdílet.</span><span class="sxs-lookup"><span data-stu-id="6907c-169">Select the leave request you want to share.</span></span> <span data-ttu-id="6907c-170">Pokud chcete sdílet koncept žádosti o dovolenou, nejprve vyberte **Koncepty**.</span><span class="sxs-lookup"><span data-stu-id="6907c-170">If you want to share a draft leave request, select **Drafts** first.</span></span>

   ![Vyberte nadcházející žádost o dovolenou ke sdílení](./media/hr-teams-leave-app-chat-search.png)

<span data-ttu-id="6907c-172">Vaše žádost o dovolenou se zobrazí v chatu.</span><span class="sxs-lookup"><span data-stu-id="6907c-172">Your leave request will display in the chat.</span></span>

![Karta s žádostí o volno v Human Resources](./media/hr-teams-leave-app-chat-card.png)

<span data-ttu-id="6907c-174">Pokud jste sdíleli koncept žádosti, zobrazí se jako koncept:</span><span class="sxs-lookup"><span data-stu-id="6907c-174">If you shared a draft request, it will display as a draft:</span></span>

![Karta s konceptem žádosti o volno v Human Resources](./media/hr-teams-leave-app-chat-draft-card.png)

## <a name="view-your-teams-leave-calendar"></a><span data-ttu-id="6907c-176">Zobrazení kalendáře pracovního volna týmu</span><span class="sxs-lookup"><span data-stu-id="6907c-176">View your team's leave calendar</span></span>

<span data-ttu-id="6907c-177">Pokud jste manažer s přímými podřízenými, můžete si prohlédnout schválené a nevyřízené pracovní volno vašeho týmu.</span><span class="sxs-lookup"><span data-stu-id="6907c-177">If you're a manager with direct reports, you can view your team's approved and pending time off.</span></span>

1. <span data-ttu-id="6907c-178">V aplikaci Human Resources v Teams vyberte **Volno**.</span><span class="sxs-lookup"><span data-stu-id="6907c-178">In the Human Resources app in Teams, select **Time off**.</span></span>

2. <span data-ttu-id="6907c-179">Vyberte **Kalendář týmu**.</span><span class="sxs-lookup"><span data-stu-id="6907c-179">Select **Team calendar**.</span></span> <span data-ttu-id="6907c-180">Kalendář zobrazuje schválené a nevyřízené volno vašich přímých podřízených.</span><span class="sxs-lookup"><span data-stu-id="6907c-180">The calendar displays your direct reports' approved and pending time off.</span></span>

   ![Zobrazení kalendáře v aplikaci Human Resources Teams](./media/hr-teams-leave-app-view-calendar.png)

   > [!NOTE]
   > <span data-ttu-id="6907c-182">Pokud týmový kalendář nevidíte, požádejte správce o jeho aktivaci.</span><span class="sxs-lookup"><span data-stu-id="6907c-182">If you can't see the team calendar, ask your admin to enable it.</span></span> <span data-ttu-id="6907c-183">Další informace naleznete v tématu [Instalace a nastavení](hr-admin-teams-leave-app.md#install-and-setup).</span><span class="sxs-lookup"><span data-stu-id="6907c-183">For more information, see [Install and setup](hr-admin-teams-leave-app.md#install-and-setup).</span></span>

## <a name="supported-languages"></a><span data-ttu-id="6907c-184">Podporované jazyky</span><span class="sxs-lookup"><span data-stu-id="6907c-184">Supported languages</span></span>

<span data-ttu-id="6907c-185">Aplikace Dynamics 365 Human Resources v Teams podporuje následující jazyky:</span><span class="sxs-lookup"><span data-stu-id="6907c-185">The Dynamics 365 Human Resources app in Teams supports the following languages:</span></span>

| <span data-ttu-id="6907c-186">ID národního prostředí</span><span class="sxs-lookup"><span data-stu-id="6907c-186">Locale ID</span></span> | <span data-ttu-id="6907c-187">Jazyk</span><span class="sxs-lookup"><span data-stu-id="6907c-187">Language</span></span> |
| --- | --- |
| <span data-ttu-id="6907c-188">de-DE</span><span class="sxs-lookup"><span data-stu-id="6907c-188">de-DE</span></span> | <span data-ttu-id="6907c-189">Němčina (Německo)</span><span class="sxs-lookup"><span data-stu-id="6907c-189">German (Germany)</span></span> |
| <span data-ttu-id="6907c-190">es-ES</span><span class="sxs-lookup"><span data-stu-id="6907c-190">es-ES</span></span> | <span data-ttu-id="6907c-191">Španělština (Španělsko)</span><span class="sxs-lookup"><span data-stu-id="6907c-191">Spanish (Spain)</span></span> |
| <span data-ttu-id="6907c-192">es-MX</span><span class="sxs-lookup"><span data-stu-id="6907c-192">es-MX</span></span> | <span data-ttu-id="6907c-193">Španělština (Mexiko)</span><span class="sxs-lookup"><span data-stu-id="6907c-193">Spanish (Mexico)</span></span> |
| <span data-ttu-id="6907c-194">fr-CA</span><span class="sxs-lookup"><span data-stu-id="6907c-194">fr-CA</span></span> | <span data-ttu-id="6907c-195">Francouzština (Kanada)</span><span class="sxs-lookup"><span data-stu-id="6907c-195">French (Canada)</span></span> |
| <span data-ttu-id="6907c-196">fr-FR</span><span class="sxs-lookup"><span data-stu-id="6907c-196">fr-FR</span></span> | <span data-ttu-id="6907c-197">Francouzština (Francie)</span><span class="sxs-lookup"><span data-stu-id="6907c-197">French (France)</span></span> |
| <span data-ttu-id="6907c-198">it-IT</span><span class="sxs-lookup"><span data-stu-id="6907c-198">it-IT</span></span> | <span data-ttu-id="6907c-199">Italština (Itálie)</span><span class="sxs-lookup"><span data-stu-id="6907c-199">Italian (Italy)</span></span> |
| <span data-ttu-id="6907c-200">nl-NL</span><span class="sxs-lookup"><span data-stu-id="6907c-200">nl-NL</span></span> | <span data-ttu-id="6907c-201">Holandština (Nizozemsko)</span><span class="sxs-lookup"><span data-stu-id="6907c-201">Dutch (Netherlands)</span></span> |
| <span data-ttu-id="6907c-202">pt-BR</span><span class="sxs-lookup"><span data-stu-id="6907c-202">pt-BR</span></span> | <span data-ttu-id="6907c-203">Portugalština (Brazílie)</span><span class="sxs-lookup"><span data-stu-id="6907c-203">Portuguese (Brazil)</span></span> |
| <span data-ttu-id="6907c-204">tr-TR</span><span class="sxs-lookup"><span data-stu-id="6907c-204">tr-TR</span></span> | <span data-ttu-id="6907c-205">Turečtina (Turecko)</span><span class="sxs-lookup"><span data-stu-id="6907c-205">Turkish (Turkey)</span></span> |
| <span data-ttu-id="6907c-206">zh-CN</span><span class="sxs-lookup"><span data-stu-id="6907c-206">zh-CN</span></span> | <span data-ttu-id="6907c-207">Čínština (zjednodušená)</span><span class="sxs-lookup"><span data-stu-id="6907c-207">Chinese (Simplified)</span></span> |

## <a name="troubleshooting"></a><span data-ttu-id="6907c-208">Řešení potíží</span><span class="sxs-lookup"><span data-stu-id="6907c-208">Troubleshooting</span></span>

<span data-ttu-id="6907c-209">Pokud máte potíže s přihlášením nebo používáním aplikace Dynamics 365 Human Resources Teams, zkuste problémy vyřešit podle těchto pokynů.</span><span class="sxs-lookup"><span data-stu-id="6907c-209">If you're having trouble signing into or using the Dynamics 365 Human Resources Teams app, try following these troubleshooting instructions.</span></span> <span data-ttu-id="6907c-210">Pokud problémy přetrvávají i po pokusu o vyřešení, obraťte se na podporu.</span><span class="sxs-lookup"><span data-stu-id="6907c-210">If you're still having problems after troubleshooting, contact Support.</span></span> <span data-ttu-id="6907c-211">Pro další informace si přečtěte [Získání podpory](hr-admin-troubleshooting-support.md).</span><span class="sxs-lookup"><span data-stu-id="6907c-211">For more information, see [Get support](hr-admin-troubleshooting-support.md).</span></span>

### <a name="cant-sign-into-the-human-resources-app-in-teams"></a><span data-ttu-id="6907c-212">Nelze se přihlásit do aplikace Human Resources v Teams</span><span class="sxs-lookup"><span data-stu-id="6907c-212">Can't sign into the Human Resources app in Teams</span></span>

<span data-ttu-id="6907c-213">Pokud se nemůžete do aplikace přihlásit, je možné, že účet, pomocí kterého se přihlašujete do Microsoft Teams není spojen se záznamem zaměstnance v Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="6907c-213">If you can't sign into the app, it's possible that the account you're using to sign into Microsoft Teams isn't associated with an employee record in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="6907c-214">Požádejtea správce systému o ověření, jestli je váš záznam zaměstnance správně přidružen.</span><span class="sxs-lookup"><span data-stu-id="6907c-214">Contact your system administrator to ensure your employee record is correctly associated.</span></span>

### <a name="translations-dont-display-correctly"></a><span data-ttu-id="6907c-215">Překlady se nezobrazují správně</span><span class="sxs-lookup"><span data-stu-id="6907c-215">Translations don't display correctly</span></span>

<span data-ttu-id="6907c-216">Pokud se překlady nezobrazují podle očekávání, ujistěte se, že jazyk, který vyberete v Teams, odpovídá jazyku vybranému v **Možnostech uživatele** Human Resources.</span><span class="sxs-lookup"><span data-stu-id="6907c-216">If translations don't display as expected, make sure the language you select in Teams matches the language selected in Human Resources **User options**.</span></span>

<span data-ttu-id="6907c-217">V Teams se podívejte na pole **Jazyk aplikace** v **Nastavení**.</span><span class="sxs-lookup"><span data-stu-id="6907c-217">In Teams, look at **App language** in **Settings**.</span></span>

![Nastavení Teams](./media/hr-teams-leave-app-settings.png)

<span data-ttu-id="6907c-219">V Human Resources vyberte **Nastavení** a poté vyberte **Možnosti uživatele**.</span><span class="sxs-lookup"><span data-stu-id="6907c-219">In Human Resources, select **Settings** and then select **User options**.</span></span> <span data-ttu-id="6907c-220">Ověřte, že pole **Jazyk** odpovídá poli **Jazyk aplikace** v Teams.</span><span class="sxs-lookup"><span data-stu-id="6907c-220">Verify that the **Language** field matches the **App language** field in Teams.</span></span>

![Možnosti uživatele v Human Resources](./media/hr-teams-leave-app-user-options.png)

<span data-ttu-id="6907c-222">Pokud problémy s překladem přetrvávají, dejte nám vědět.</span><span class="sxs-lookup"><span data-stu-id="6907c-222">If you still experience translation issues, let us know.</span></span> <span data-ttu-id="6907c-223">Informace najdete v tématu [Získání podpory pro aplikace Finance and Operations nebo Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs-support?toc=/dynamics365/human-resources/toc.json).</span><span class="sxs-lookup"><span data-stu-id="6907c-223">For information, see [Get support for Finance and Operations apps or Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs-support?toc=/dynamics365/human-resources/toc.json).</span></span>

### <a name="error-when-approving-leave-requests-in-the-human-resources-app-in-teams"></a><span data-ttu-id="6907c-224">Chyba při schvalování žádostí o dovolenou v aplikaci Human Resources v Teams</span><span class="sxs-lookup"><span data-stu-id="6907c-224">Error when approving leave requests in the Human Resources app in Teams</span></span>

<span data-ttu-id="6907c-225">Pokud se vám při pokusu o schválení žádostí o dovolenou v aplikaci Teams zobrazí chyba, zkuste v rámci řešení potíží následující kroky:</span><span class="sxs-lookup"><span data-stu-id="6907c-225">If you receive an error when you're trying to approve leave requests in the Teams app, try the following troubleshooting steps:</span></span>

1. <span data-ttu-id="6907c-226">Ověřte, že účet, který používáte k přihlášení k Microsoft Teams, je stejný, jaký používáte pro přístup k Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="6907c-226">Verify that the account you're using to sign into Microsoft Teams is the same one you use for accessing Dynamics 365 Human Resources.</span></span>

2. <span data-ttu-id="6907c-227">Ověřte, jestli jste platným schvalovatelem požadavku, a to kontrolou nastavení pracovního postupu pro schválení dovolené.</span><span class="sxs-lookup"><span data-stu-id="6907c-227">Verify that you're a valid approver for the request by checking the workflow settings for leave approval.</span></span> <span data-ttu-id="6907c-228">Další informace o pracovních postupech žádostí o dovolenou najdete v tématu [Vytvoření pracovního postupu žádosti o dovolenou](hr-leave-and-absence-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="6907c-228">For more information about leave request workflows, see [Create a leave request workflow](hr-leave-and-absence-workflow.md).</span></span>

## <a name="known-accessibility-issues"></a><span data-ttu-id="6907c-229">Známé problémy s usnadněním</span><span class="sxs-lookup"><span data-stu-id="6907c-229">Known accessibility issues</span></span>

<span data-ttu-id="6907c-230">Aplikace Human Resources v Teams má následující problémy s usnadněním, na jejichž řešení pracujeme pro budoucí verze.</span><span class="sxs-lookup"><span data-stu-id="6907c-230">The Human Resources app in Teams has the following accessibility issues that we're working on fixing in future releases.</span></span>

| <span data-ttu-id="6907c-231">Výdej</span><span class="sxs-lookup"><span data-stu-id="6907c-231">Issue</span></span> | <span data-ttu-id="6907c-232">Řešení nebo vysvětlení</span><span class="sxs-lookup"><span data-stu-id="6907c-232">Workaround or explanation</span></span> |
| --- | --- |
| <span data-ttu-id="6907c-233">Zvětšení plochy o 400 % skryje některá tlačítka akcí.</span><span class="sxs-lookup"><span data-stu-id="6907c-233">Zooming to 400% on desktop hides some of the action buttons from view.</span></span> | <span data-ttu-id="6907c-234">Doporučujeme místo toho používat lupu, dokud nebudeme moci tuto úroveň zvětšení podporovat.</span><span class="sxs-lookup"><span data-stu-id="6907c-234">We recommend using a magnifier instead until we can support this zoom level.</span></span> |
| <span data-ttu-id="6907c-235">Na kartě **Volno** hlasový komentář oznamuje akci tlačítka při čtení záhlaví mřížky volna.</span><span class="sxs-lookup"><span data-stu-id="6907c-235">On the **Time off** tab, voiceover announces a button action while reading the header for the time-off grid.</span></span> | <span data-ttu-id="6907c-236">Záhlaví a prvky v mřížce jsou seskupeny podle roku a jsou sbalitelné.</span><span class="sxs-lookup"><span data-stu-id="6907c-236">The header and elements within the grid are grouped by year, and they're collapsible.</span></span> <span data-ttu-id="6907c-237">Komentář to interpretuje jako položku s akcemi, kterou ale není.</span><span class="sxs-lookup"><span data-stu-id="6907c-237">Voiceover interprets this as an actionable item, but it isn't.</span></span> |
| <span data-ttu-id="6907c-238">Na kartě **Volno** je při přechodu na **Kód důvodu** v nové žádosti potřeba potáhnutí prstem navíc.</span><span class="sxs-lookup"><span data-stu-id="6907c-238">On the **Time off** tab, there's an extra swipe gesture when navigating to **Reason code** in a new request.</span></span> | <span data-ttu-id="6907c-239">Neexistuje žádný skrytý ovládací prvek, ke kterému se potáhnutí prstem pokouší dostat.</span><span class="sxs-lookup"><span data-stu-id="6907c-239">There is no hidden control that the swipe navigation is trying to get to.</span></span> |
| <span data-ttu-id="6907c-240">Na kartě **Volno**, pokud potáhnete prstem, když je kalendář otevřený, skončíte mimo ovládací prvek namísto horní části v nové žádosti nebo během úpravy požadavku.</span><span class="sxs-lookup"><span data-stu-id="6907c-240">On the **Time off** tab, if you swipe while the calendar is open, you end up outside the control instead of at the top in a new request or while editing a request.</span></span> | <span data-ttu-id="6907c-241">Když dosáhnete položky **Přejít na dnešek**, považujte to za konec ovládacího prvku a potáhnutím prstem opačným směrem se dostanete zpět nahoru.</span><span class="sxs-lookup"><span data-stu-id="6907c-241">When you reach **Go to today**, consider that to be the end of the control and swipe in the reverse direction to get back to the top.</span></span> |
| <span data-ttu-id="6907c-242">Na kartě **Chat**, když zadáte datum při používání asistenčního nástroje nebo navigace pomocí klávesnice, přeskočí fokus zpět na začátek.</span><span class="sxs-lookup"><span data-stu-id="6907c-242">On the **Chat** tab, the focus jumps back to the top when you enter a date while using the assistive tool or keyboard navigation.</span></span> | <span data-ttu-id="6907c-243">Stiskněte klávesu Tab, dokud se znovu nedostanete do oblasti zadávání.</span><span class="sxs-lookup"><span data-stu-id="6907c-243">Tab until you reach your input area again.</span></span> |

## <a name="privacy-notice"></a><span data-ttu-id="6907c-244">Oznámení o ochraně osobních údajů</span><span class="sxs-lookup"><span data-stu-id="6907c-244">Privacy notice</span></span>

### <a name="microsoft-language-understanding-intelligent-service-luis"></a><span data-ttu-id="6907c-245">Microsoft Language Understanding Intelligent Service (LUIS)</span><span class="sxs-lookup"><span data-stu-id="6907c-245">Microsoft Language Understanding Intelligent Service (LUIS)</span></span>

<span data-ttu-id="6907c-246">S robotem Dynamics 365 Human Resources v aplikaci Microsoft Teams jsou textové vstupy uživatele analyzovány pro porozumění základním dotazům/záměrům.</span><span class="sxs-lookup"><span data-stu-id="6907c-246">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="6907c-247">Vstup uživatele, například „Vyhledat účet Contoso“, je přesměrován na jednu ze služeb Cognitive Services společnosti Microsoft nazvanou Language Understanding Intelligent Service (LUIS).</span><span class="sxs-lookup"><span data-stu-id="6907c-247">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="6907c-248">Přečtěte si více o LUIS  [zde](https://www.luis.ai/).</span><span class="sxs-lookup"><span data-stu-id="6907c-248">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="6907c-249">Služba LUIS ujasňuje nebo chápe záměr vstupu uživatele (v tomto případě je záměrem najít informace) a cílovou entitu (v tomto případě je zamýšlenou entitou účet s názvem Contoso).</span><span class="sxs-lookup"><span data-stu-id="6907c-249">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="6907c-250">Tyto informace jsou poté předány do řešení  [Azure Bot Framework](https://azure.microsoft.com/services/bot-service/) společnosti Microsoft, které interaguje s daty z Dynamics 365 Human Resources a načte požadované informace pro uživatelský dotaz.</span><span class="sxs-lookup"><span data-stu-id="6907c-250">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/), which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="6907c-251">Instalací a umožněním přístupu k používání robota souhlasíte s tím, že umožníte službě LUIS a rámci robota Azure zpracovat záměr za vstupem, což má za následek vylepšenou konverzační uživatelskou zkušenost.</span><span class="sxs-lookup"><span data-stu-id="6907c-251">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="6907c-252">Služba LUIS a rámec robota Azure mohou mít ve srovnání s Dynamics 365 Human Resources různé úrovně shody.</span><span class="sxs-lookup"><span data-stu-id="6907c-252">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="6907c-253">Zatímco služba LUIS má přístup pouze k uživatelským dotazům a není určena k připojení k datům nebo účtu uživatele Dynamics 365 Human Resources, uživatel robota Dynamics 365 Human Resources může dobrovolně zadat dotaz obsahující zákaznická data, osobní údaje nebo jiná data a takový obsah dotazu by mohl být zaslán do služby LUIS a do rámce robota Azure.</span><span class="sxs-lookup"><span data-stu-id="6907c-253">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="6907c-254">Obsah dotazů a zpráv uživatele je v systému LUIS uchováván maximálně 30 dní, je šifrován a nepoužívá se pro školení ani zlepšení služeb.</span><span class="sxs-lookup"><span data-stu-id="6907c-254">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="6907c-255">Přečtěte si více o Cognitive Services  [zde](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span><span class="sxs-lookup"><span data-stu-id="6907c-255">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="6907c-256">Chcete-li spravovat nastavení administrátora pro aplikace v Microsoft Teams, přejděte do [centra pro správu Microsoft Teams](https://admin.teams.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="6907c-256">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span>

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a><span data-ttu-id="6907c-257">Microsoft Teams  Azure Event Grid a Azure Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="6907c-257">Microsoft Teams, Azure Event Grid, and Azure Cosmos DB</span></span>

<span data-ttu-id="6907c-258">Při použití aplikace Dynamics 365 Human Resources v Microsoft Teams mohou některá data zákazníků téct mimo geografickou oblast, kde je nasazena služba Human Resources vašeho klienta.</span><span class="sxs-lookup"><span data-stu-id="6907c-258">When using the Dynamics 365 Human Resources app in Microsoft Teams, certain customer data may flow outside of the geographic region where your tenant’s Human Resources service is deployed.</span></span>

<span data-ttu-id="6907c-259">Dynamics 365 Human Resources přenáší podrobnosti o žádosti o pracovní volno a úkolu pracovního postupu do Microsoft Azure Event Grid a Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="6907c-259">Dynamics 365 Human Resources transmits the employee’s leave request and workflow task details to Microsoft Azure Event Grid and Microsoft Teams.</span></span> <span data-ttu-id="6907c-260">Tato data mohou být uložena v Event Grid Microsoft Azure až 24 hodin a budou zpracována ve Spojených státech, jsou šifrována během přenosu a v klidu a nejsou používána společností Microsoft nebo jejími subprocesory pro školení nebo vylepšení služeb.</span><span class="sxs-lookup"><span data-stu-id="6907c-260">This data may be stored in Microsoft Azure Event Grid for up to 24 hours and will be processed in the United States, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="6907c-261">Chcete-li zjistit, kde jsou vaše data uložena v Teams, přečtěte si [Umístění dat v Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="6907c-261">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span></span>

<span data-ttu-id="6907c-262">Při konverzaci s chatovacím robotem v aplikaci Human Resources může být obsah konverzace uložen v Azure Cosmos DB a přenesen do Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="6907c-262">While conversing with the chat bot in the Human Resources app, the conversation content may be stored in Azure Cosmos DB and transmitted to Microsoft Teams.</span></span> <span data-ttu-id="6907c-263">Tato data mohou být uložena v Azure Cosmos DB po dobu až 24 hodin a mohou být zpracovávána mimo geografickou oblast, kde je nasazena služba Human Resources vašeho nájemce, je šifrována během přenosu a v klidu a není používána společností Microsoft nebo jejími subprocesory pro školení nebo vylepšení služeb.</span><span class="sxs-lookup"><span data-stu-id="6907c-263">This data may be stored in Azure Cosmos DB for up to 24 hours and may be processed outside of the geographic region where your tenant's Human Resources service is deployed, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="6907c-264">Chcete-li zjistit, kde jsou vaše data uložena v Teams, přečtěte si [Umístění dat v Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="6907c-264">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span></span>
 
<span data-ttu-id="6907c-265">Chcete-li omezit přístup k aplikaci Human Resources v Microsoft Teams pro vaši organizaci nebo uživatele ve vaší organizaci, přečtěte si [Spravujte zásady oprávnění aplikace v Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span><span class="sxs-lookup"><span data-stu-id="6907c-265">To restrict access to the Human Resources app in Microsoft Teams for your organization or users within your organization, see [Manage app permission policies in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="see-also"></a><span data-ttu-id="6907c-266">Viz také</span><span class="sxs-lookup"><span data-stu-id="6907c-266">See also</span></span>

[<span data-ttu-id="6907c-267">Stažení a instalace aplikace Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="6907c-267">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="6907c-268">Centrum nápovědy Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="6907c-268">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="6907c-269">Aplikace Human Resources v Teams</span><span class="sxs-lookup"><span data-stu-id="6907c-269">Human Resources app in Teams</span></span>](hr-admin-teams-leave-app.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]