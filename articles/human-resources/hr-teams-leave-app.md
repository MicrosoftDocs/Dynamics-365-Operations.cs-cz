---
title: Správa žádostí o dovolenou v aplikaci Teams
description: Toto téma ukazuje, jak požádat o volno v aplikaci Dynamics 365 Human Resources v Microsoft Teams.
author: andreabichsel
ms.date: 05/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeaveAbsenceWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 661bb8369fe4dbe6cdf6ee0fb05d16f4350ecf5a
ms.sourcegitcommit: c5c8f19a696ad4a3d68dffd63bfe7b484b999d2b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/25/2021
ms.locfileid: "6097252"
---
# <a name="manage-leave-requests-in-teams"></a><span data-ttu-id="bc877-103">Správa žádostí o dovolenou v aplikaci Teams</span><span class="sxs-lookup"><span data-stu-id="bc877-103">Manage leave requests in Teams</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="bc877-104">Aplikace Dynamics 365 Human Resources v aplikaci Microsoft Teams vám umožňuje rychle požádat o volno a zobrazit informace o svém zůstatku volna přímo v Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="bc877-104">The Dynamics 365 Human Resources app in Microsoft Teams lets you quickly request time off and view your time-off balance information right in Microsoft Teams.</span></span> <span data-ttu-id="bc877-105">Můžete komunikovat s robotem a požádat o informace a zahájit žádost o dovolenou.</span><span class="sxs-lookup"><span data-stu-id="bc877-105">You can interact with a bot to request information and start a leave request.</span></span> <span data-ttu-id="bc877-106">Karta **Volno** poskytuje podrobnější informace.</span><span class="sxs-lookup"><span data-stu-id="bc877-106">The **Time off** tab provides more detailed information.</span></span> <span data-ttu-id="bc877-107">Kromě toho můžete lidem posílat informace o svém nadcházejícím volnu v Teams a chatech mimo aplikaci Human Resources.</span><span class="sxs-lookup"><span data-stu-id="bc877-107">You can also send people information about your upcoming time off in Teams and chats outside the Human Resources app.</span></span>

## <a name="install-the-app"></a><span data-ttu-id="bc877-108">Instalace aplikace</span><span class="sxs-lookup"><span data-stu-id="bc877-108">Install the app</span></span>

<span data-ttu-id="bc877-109">Aplikaci Dynamics 365 Human Resources najdete v obchodě Teams.</span><span class="sxs-lookup"><span data-stu-id="bc877-109">You can find the Dynamics 365 Human Resources app in the Teams store.</span></span>

1. <span data-ttu-id="bc877-110">V Microsoft Teams přejděte do seznamu aplikací.</span><span class="sxs-lookup"><span data-stu-id="bc877-110">In Microsoft Teams, navigate to the list of apps.</span></span>
 
2. <span data-ttu-id="bc877-111">Vyhledejte Dynamics 365 Human Resources a poté vyberte dlaždici **Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="bc877-111">Search for Dynamics 365 Human Resources, and then select the **Human Resources** tile.</span></span>

3. <span data-ttu-id="bc877-112">Vyberte tlačítko **Přidat** pro instalaci aplikace.</span><span class="sxs-lookup"><span data-stu-id="bc877-112">Select the **Add** button to install the app.</span></span>

<span data-ttu-id="bc877-113">Pokud vás aplikace nepřihlásí automaticky, vyberte kartu **Nastavení** pro přihlášení.</span><span class="sxs-lookup"><span data-stu-id="bc877-113">If the app doesn't automatically sign you in, select the **Settings** tab to sign in.</span></span>

> [!NOTE]
> <span data-ttu-id="bc877-114">Pokud nevidíte přihlašovací dialogové okno, zkontrolujte nastavení prohlížeče a povolte automaticky otevíraná okna.</span><span class="sxs-lookup"><span data-stu-id="bc877-114">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span> 

<span data-ttu-id="bc877-115">Pokud máte přístup k více než jedné instanci aplikace Human Resources, můžete vybrat prostředí, ke kterému se chcete připojit, na kartě **Nastavení**.</span><span class="sxs-lookup"><span data-stu-id="bc877-115">If you have access to more than one instance of Human Resources, you can select which environment you want to connect to in the **Settings** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="bc877-116">Aplikace nyní podporuje roli zabezpečení správce systému.</span><span class="sxs-lookup"><span data-stu-id="bc877-116">The app now supports the System Administrator security role.</span></span>
 
## <a name="use-the-bot"></a><span data-ttu-id="bc877-117">Použití robota</span><span class="sxs-lookup"><span data-stu-id="bc877-117">Use the bot</span></span>

<span data-ttu-id="bc877-118">Po instalaci aplikace se zobrazí uvítací zpráva, která vás informuje o typech akcí, které může robot provést vaším jménem.</span><span class="sxs-lookup"><span data-stu-id="bc877-118">After the app installs, a welcome message appears, letting you know the types of actions the bot can take on your behalf.</span></span>

> [!NOTE]
> <span data-ttu-id="bc877-119">Při první interakci s robotem se možná budete muset přihlásit.</span><span class="sxs-lookup"><span data-stu-id="bc877-119">When first interacting with the bot, you might need to sign in.</span></span> <span data-ttu-id="bc877-120">Pokud nevidíte přihlašovací dialogové okno, zkontrolujte nastavení prohlížeče a povolte automaticky otevíraná okna.</span><span class="sxs-lookup"><span data-stu-id="bc877-120">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span>

<span data-ttu-id="bc877-121">Můžete požádat robota a následující akce:</span><span class="sxs-lookup"><span data-stu-id="bc877-121">You can ask the bot to:</span></span>

- <span data-ttu-id="bc877-122">Zobrazit aktuální zůstatky dovolené.</span><span class="sxs-lookup"><span data-stu-id="bc877-122">View your current leave balances.</span></span> <span data-ttu-id="bc877-123">Například pošlete zprávu s názvem „Zobrazit zůstatky dovolené“.</span><span class="sxs-lookup"><span data-stu-id="bc877-123">For example, send a message that says, "View leave balances."</span></span>

- <span data-ttu-id="bc877-124">Zahájit žádost o volno za vás.</span><span class="sxs-lookup"><span data-stu-id="bc877-124">Start a leave request for you.</span></span> <span data-ttu-id="bc877-125">Například pošlete zprávu s textem „Vezměte si volno“ nebo „Chci si vzít volno na příští čtvrtek a pátek“, aby bylo konkrétnější požadovat dovolenou u typu dovolené na dovolenou.</span><span class="sxs-lookup"><span data-stu-id="bc877-125">For example, send a message that says, “Take time off” or “I want to take vacation time off next Thursday and Friday” to be more specific for requesting leave for the vacation leave type.</span></span> 

  ![Zahájení žádosti o volno v chatu Teams](./media/hr-teams-leave-app-initiate.png)

- <span data-ttu-id="bc877-127">Chatovací robot za vás vyplní žádost o volno.</span><span class="sxs-lookup"><span data-stu-id="bc877-127">The chat bot will populate a leave request for you.</span></span> <span data-ttu-id="bc877-128">Vyberte možnost **Požádat o volno** a upravte podrobnosti své žádosti.</span><span class="sxs-lookup"><span data-stu-id="bc877-128">Select **Request time off** and edit the details for your request.</span></span>

   <span data-ttu-id="bc877-129">Pokud chcete odeslat žádosti o dovolenou pro více typů dovolené na stejné datum, vyberte možnost **Rozdělit den s** v nabídce **Více možností**.</span><span class="sxs-lookup"><span data-stu-id="bc877-129">If you want to submit leave requests for multiple leave types for the same date, select the **Split day with** option from the **More options** menu.</span></span> 

   <span data-ttu-id="bc877-130">Pokud vyberete půldenní dovolenou, když je jednotka žádosti o dovolenou ve dnech, můžete určit, zda chcete požádat o volno v první půlden nebo druhý půlden výběrem možnosti **Půldenní definice** v nabídce **Více možností**.</span><span class="sxs-lookup"><span data-stu-id="bc877-130">If you select a half day leave when the leave request unit is in days, you can specify whether you want to request time off the first half day or the second half day by selecting the **Half day definition** option from the **More options** menu.</span></span>
   
   ![Půldenní definice](./media/HalfDayDefinitions.png)

- <span data-ttu-id="bc877-132">Po dokončení úprav podrobností žádosti o volno vyberte **Odeslat** a předejte žádost ke schválení.</span><span class="sxs-lookup"><span data-stu-id="bc877-132">When you're done editing your leave request details, select **Submit** to submit it for approval.</span></span>

  ![Odeslání žádosti o volno](./media/hr-teams-leave-app-submit.png)

## <a name="manage-your-leave-in-teams"></a><span data-ttu-id="bc877-134">Správa volna v aplikaci Teams</span><span class="sxs-lookup"><span data-stu-id="bc877-134">Manage your leave in Teams</span></span>

<span data-ttu-id="bc877-135">Karta **Volno** umožňuje zobrazit:</span><span class="sxs-lookup"><span data-stu-id="bc877-135">The **Time off** tab allows you to view:</span></span> 

- <span data-ttu-id="bc877-136">Informace o zůstatku pro každý typ volna, ke kterému jste zaregistrováni</span><span class="sxs-lookup"><span data-stu-id="bc877-136">Balance information for each leave type you're enrolled in</span></span>

- <span data-ttu-id="bc877-137">Nadcházející žádosti o volno</span><span class="sxs-lookup"><span data-stu-id="bc877-137">Upcoming leave requests</span></span>

- <span data-ttu-id="bc877-138">Žádosti o volno</span><span class="sxs-lookup"><span data-stu-id="bc877-138">Time-off requests</span></span>

- <span data-ttu-id="bc877-139">Koncept žádostí o volno</span><span class="sxs-lookup"><span data-stu-id="bc877-139">Draft leave requests</span></span>
 
### <a name="create-a-new-request"></a><span data-ttu-id="bc877-140">Vytvoření nové žádosti</span><span class="sxs-lookup"><span data-stu-id="bc877-140">Create a new request</span></span>

1. <span data-ttu-id="bc877-141">Chcete-li vytvořit novou žádost o volno, zvolte **Nová žádost**.</span><span class="sxs-lookup"><span data-stu-id="bc877-141">To create a new leave request, select **New request**.</span></span>

2. <span data-ttu-id="bc877-142">Zadejte den nebo dny, na které chcete volno, a poté vyberte **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="bc877-142">Enter the day or days you want to take off, and then select **Add**.</span></span>

   ![Přidání volna aplikace pracovního volna Human Resources Teams](./media/TimeOffHours.png)

3. <span data-ttu-id="bc877-144">V případě potřeby zadejte kód důvodu.</span><span class="sxs-lookup"><span data-stu-id="bc877-144">If applicable, enter a reason code.</span></span> <span data-ttu-id="bc877-145">Také zadejte případné komentáře a přidejte všechny přílohy.</span><span class="sxs-lookup"><span data-stu-id="bc877-145">Also enter any comments and add any attachments.</span></span>

4. <span data-ttu-id="bc877-146">Pokud chcete odeslat žádosti o dovolenou pro více typů dovolené na stejné datum, vyberte možnost **Rozdělit den s** v nabídce **Více možností**.</span><span class="sxs-lookup"><span data-stu-id="bc877-146">Select the **Split day with** option from the **More options** menu if you want to submit multiple leave request entries for the same date for different leave types.</span></span>

5. <span data-ttu-id="bc877-147">Vyberte možnost **Půldenní definice** k určení, zda chcete požádat o první půl dne volna nebo o druhou půl dne volna.</span><span class="sxs-lookup"><span data-stu-id="bc877-147">Select the **Half day definition** option to specify if you want to request the first half day off or the second half day off.</span></span> <span data-ttu-id="bc877-148">Tato možnost je k dispozici, když je jednotka žádosti o dovolenou ve dnech a požadovaná částka je 0,5 dne.</span><span class="sxs-lookup"><span data-stu-id="bc877-148">This option is available when the leave request unit is in days and the amount requested is 0.5 days.</span></span>

6. <span data-ttu-id="bc877-149">Až zadáte informace, zadejte **Odeslat** pro odeslání žádosti ke schválení.</span><span class="sxs-lookup"><span data-stu-id="bc877-149">When you're done entering information, enter **Submit** to submit it for approval.</span></span> <span data-ttu-id="bc877-150">Můžete také vložit **Uložit jako koncept** a vrátit se k žádosti později.</span><span class="sxs-lookup"><span data-stu-id="bc877-150">You can also enter **Save as draft** to come back to it later.</span></span>

### <a name="manage-draft-requests"></a><span data-ttu-id="bc877-151">Správa konceptů žádostí</span><span class="sxs-lookup"><span data-stu-id="bc877-151">Manage draft requests</span></span>

1. <span data-ttu-id="bc877-152">Zvolte kartu **Koncepty**.</span><span class="sxs-lookup"><span data-stu-id="bc877-152">Select the **Drafts** tab.</span></span>

2. <span data-ttu-id="bc877-153">Vyberte symbol tužky, chcete-li žádost upravit, nebo vyberte koš, chcete-li žádost odstranit.</span><span class="sxs-lookup"><span data-stu-id="bc877-153">Select the pencil to edit the request, or select the trash can to delete the request.</span></span>

3. <span data-ttu-id="bc877-154">Proveďte potřebné změny.</span><span class="sxs-lookup"><span data-stu-id="bc877-154">Make any necessary changes.</span></span> <span data-ttu-id="bc877-155">Až zadáte informace, napište **Odeslat** pro odeslání žádosti ke schválení.</span><span class="sxs-lookup"><span data-stu-id="bc877-155">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="bc877-156">Můžete také zvolit **Uložit jako koncept** a vrátit se k žádosti později.</span><span class="sxs-lookup"><span data-stu-id="bc877-156">You can also select **Save as draft** to come back to it later.</span></span>
   
### <a name="respond-to-teams-notifications"></a><span data-ttu-id="bc877-157">Odpovídejte na oznámení týmů</span><span class="sxs-lookup"><span data-stu-id="bc877-157">Respond to Teams notifications</span></span>

<span data-ttu-id="bc877-158">Když vy nebo pracovník, jehož jste schvalovatelem, odešlete žádost o pracovní volno, obdržíte oznámení v aplikaci Human Resources v Teams.</span><span class="sxs-lookup"><span data-stu-id="bc877-158">When you or a worker you're an approver for submits a leave request, you'll receive a notification in the Human Resources app in Teams.</span></span> <span data-ttu-id="bc877-159">Chcete-li oznámení zobrazit, vyberte jej.</span><span class="sxs-lookup"><span data-stu-id="bc877-159">You can select the notification to view it.</span></span> <span data-ttu-id="bc877-160">Oznámení se také zobrazují v oblasti **Chat**.</span><span class="sxs-lookup"><span data-stu-id="bc877-160">Notifications also appear in the **Chat** area.</span></span>

<span data-ttu-id="bc877-161">Pokud jste schvalovatel, můžete v oznámení zvolit možnosti **Schválit** nebo **Odmítnout**.</span><span class="sxs-lookup"><span data-stu-id="bc877-161">If you're an approver, you can select **Approve** or **Deny** in the notification.</span></span> <span data-ttu-id="bc877-162">Můžete také zadat volitelnou zprávu.</span><span class="sxs-lookup"><span data-stu-id="bc877-162">You can also provide an optional message.</span></span>

## <a name="send-upcoming-time-off-information-to-your-coworkers"></a><span data-ttu-id="bc877-163">Pošlete nadcházející informace o volném čase vašim spolupracovníkům</span><span class="sxs-lookup"><span data-stu-id="bc877-163">Send upcoming time-off information to your coworkers</span></span>

<span data-ttu-id="bc877-164">Po instalaci aplikace Human Resources pro Teams můžete snadno poslat informace o svém nadcházejícím volnu svým spolupracovníkům v týmech nebo chatech.</span><span class="sxs-lookup"><span data-stu-id="bc877-164">After you install the Human Resources app for Teams, you can easily send information about your upcoming time off to your coworkers in teams or chats.</span></span>

1. <span data-ttu-id="bc877-165">V týmu nebo chatu v Teams vyberte tlačítko Human Resources pod oknem chatu.</span><span class="sxs-lookup"><span data-stu-id="bc877-165">In a team or chat in Teams, select the Human Resources button below the chat window.</span></span>

   ![Tlačítko Human Resources pod oknem chatu](./media/hr-teams-leave-app-chat-button.png)

2. <span data-ttu-id="bc877-167">Vyberte žádost o dovolenou, kterou chcete sdílet.</span><span class="sxs-lookup"><span data-stu-id="bc877-167">Select the leave request you want to share.</span></span> <span data-ttu-id="bc877-168">Pokud chcete sdílet koncept žádosti o dovolenou, nejprve vyberte **Koncepty**.</span><span class="sxs-lookup"><span data-stu-id="bc877-168">If you want to share a draft leave request, select **Drafts** first.</span></span>

<span data-ttu-id="bc877-169">Vaše žádost o dovolenou se zobrazí v chatu.</span><span class="sxs-lookup"><span data-stu-id="bc877-169">Your leave request will display in the chat.</span></span>

<span data-ttu-id="bc877-170">Pokud jste sdíleli koncept žádosti, zobrazí se jako koncept.</span><span class="sxs-lookup"><span data-stu-id="bc877-170">If you shared a draft request, it will display as a draft.</span></span>

## <a name="view-your-teams-leave-calendar"></a><span data-ttu-id="bc877-171">Zobrazení kalendáře pracovního volna týmu</span><span class="sxs-lookup"><span data-stu-id="bc877-171">View your team's leave calendar</span></span>

<span data-ttu-id="bc877-172">Pokud jste manažer s přímými podřízenými, můžete si prohlédnout schválené a nevyřízené pracovní volno vašeho týmu.</span><span class="sxs-lookup"><span data-stu-id="bc877-172">If you're a manager with direct reports, you can view your team's approved and pending time off.</span></span>

1. <span data-ttu-id="bc877-173">V aplikaci Human Resources v Teams vyberte **Volno**.</span><span class="sxs-lookup"><span data-stu-id="bc877-173">In the Human Resources app in Teams, select **Time off**.</span></span>

2. <span data-ttu-id="bc877-174">Vyberte **Kalendář týmu**.</span><span class="sxs-lookup"><span data-stu-id="bc877-174">Select **Team calendar**.</span></span> <span data-ttu-id="bc877-175">Kalendář zobrazuje schválené a nevyřízené volno vašich přímých podřízených.</span><span class="sxs-lookup"><span data-stu-id="bc877-175">The calendar displays your direct reports' approved and pending time off.</span></span>

   > [!NOTE]
   > <span data-ttu-id="bc877-176">Pokud týmový kalendář nevidíte, požádejte správce o jeho aktivaci.</span><span class="sxs-lookup"><span data-stu-id="bc877-176">If you can't see the team calendar, ask your admin to enable it.</span></span> <span data-ttu-id="bc877-177">Další informace naleznete v tématu [Instalace a nastavení](hr-admin-teams-leave-app.md#install-and-setup).</span><span class="sxs-lookup"><span data-stu-id="bc877-177">For more information, see [Install and setup](hr-admin-teams-leave-app.md#install-and-setup).</span></span>

## <a name="supported-languages"></a><span data-ttu-id="bc877-178">Podporované jazyky</span><span class="sxs-lookup"><span data-stu-id="bc877-178">Supported languages</span></span>

<span data-ttu-id="bc877-179">Aplikace Dynamics 365 Human Resources v Teams podporuje následující jazyky:</span><span class="sxs-lookup"><span data-stu-id="bc877-179">The Dynamics 365 Human Resources app in Teams supports the following languages:</span></span>

| <span data-ttu-id="bc877-180">ID národního prostředí</span><span class="sxs-lookup"><span data-stu-id="bc877-180">Locale ID</span></span> | <span data-ttu-id="bc877-181">Jazyk</span><span class="sxs-lookup"><span data-stu-id="bc877-181">Language</span></span> |
| --- | --- |
| <span data-ttu-id="bc877-182">de-DE</span><span class="sxs-lookup"><span data-stu-id="bc877-182">de-DE</span></span> | <span data-ttu-id="bc877-183">Němčina (Německo)</span><span class="sxs-lookup"><span data-stu-id="bc877-183">German (Germany)</span></span> |
| <span data-ttu-id="bc877-184">es-ES</span><span class="sxs-lookup"><span data-stu-id="bc877-184">es-ES</span></span> | <span data-ttu-id="bc877-185">Španělština (Španělsko)</span><span class="sxs-lookup"><span data-stu-id="bc877-185">Spanish (Spain)</span></span> |
| <span data-ttu-id="bc877-186">es-MX</span><span class="sxs-lookup"><span data-stu-id="bc877-186">es-MX</span></span> | <span data-ttu-id="bc877-187">Španělština (Mexiko)</span><span class="sxs-lookup"><span data-stu-id="bc877-187">Spanish (Mexico)</span></span> |
| <span data-ttu-id="bc877-188">fr-CA</span><span class="sxs-lookup"><span data-stu-id="bc877-188">fr-CA</span></span> | <span data-ttu-id="bc877-189">Francouzština (Kanada)</span><span class="sxs-lookup"><span data-stu-id="bc877-189">French (Canada)</span></span> |
| <span data-ttu-id="bc877-190">fr-FR</span><span class="sxs-lookup"><span data-stu-id="bc877-190">fr-FR</span></span> | <span data-ttu-id="bc877-191">Francouzština (Francie)</span><span class="sxs-lookup"><span data-stu-id="bc877-191">French (France)</span></span> |
| <span data-ttu-id="bc877-192">it-IT</span><span class="sxs-lookup"><span data-stu-id="bc877-192">it-IT</span></span> | <span data-ttu-id="bc877-193">Italština (Itálie)</span><span class="sxs-lookup"><span data-stu-id="bc877-193">Italian (Italy)</span></span> |
| <span data-ttu-id="bc877-194">nl-NL</span><span class="sxs-lookup"><span data-stu-id="bc877-194">nl-NL</span></span> | <span data-ttu-id="bc877-195">Holandština (Nizozemsko)</span><span class="sxs-lookup"><span data-stu-id="bc877-195">Dutch (Netherlands)</span></span> |
| <span data-ttu-id="bc877-196">pt-BR</span><span class="sxs-lookup"><span data-stu-id="bc877-196">pt-BR</span></span> | <span data-ttu-id="bc877-197">Portugalština (Brazílie)</span><span class="sxs-lookup"><span data-stu-id="bc877-197">Portuguese (Brazil)</span></span> |
| <span data-ttu-id="bc877-198">tr-TR</span><span class="sxs-lookup"><span data-stu-id="bc877-198">tr-TR</span></span> | <span data-ttu-id="bc877-199">Turečtina (Turecko)</span><span class="sxs-lookup"><span data-stu-id="bc877-199">Turkish (Turkey)</span></span> |
| <span data-ttu-id="bc877-200">zh-CN</span><span class="sxs-lookup"><span data-stu-id="bc877-200">zh-CN</span></span> | <span data-ttu-id="bc877-201">Čínština (zjednodušená)</span><span class="sxs-lookup"><span data-stu-id="bc877-201">Chinese (Simplified)</span></span> |

## <a name="troubleshooting"></a><span data-ttu-id="bc877-202">Řešení potíží</span><span class="sxs-lookup"><span data-stu-id="bc877-202">Troubleshooting</span></span>

<span data-ttu-id="bc877-203">Pokud máte potíže s přihlášením nebo používáním aplikace Dynamics 365 Human Resources Teams, zkuste problémy vyřešit podle těchto pokynů.</span><span class="sxs-lookup"><span data-stu-id="bc877-203">If you're having trouble signing into or using the Dynamics 365 Human Resources Teams app, try following these troubleshooting instructions.</span></span> <span data-ttu-id="bc877-204">Pokud problémy přetrvávají i po pokusu o vyřešení, obraťte se na podporu.</span><span class="sxs-lookup"><span data-stu-id="bc877-204">If you're still having problems after troubleshooting, contact Support.</span></span> <span data-ttu-id="bc877-205">Pro další informace si přečtěte [Získání podpory](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span><span class="sxs-lookup"><span data-stu-id="bc877-205">For more information, see [Get support](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span></span>

### <a name="cant-sign-into-the-human-resources-app-in-teams"></a><span data-ttu-id="bc877-206">Nelze se přihlásit do aplikace Human Resources v Teams</span><span class="sxs-lookup"><span data-stu-id="bc877-206">Can't sign into the Human Resources app in Teams</span></span>

<span data-ttu-id="bc877-207">Pokud se nemůžete do aplikace přihlásit, je možné, že účet, pomocí kterého se přihlašujete do Microsoft Teams není spojen se záznamem zaměstnance v Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="bc877-207">If you can't sign into the app, it's possible that the account you're using to sign into Microsoft Teams isn't associated with an employee record in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="bc877-208">Požádejtea správce systému o ověření, jestli je váš záznam zaměstnance správně přidružen.</span><span class="sxs-lookup"><span data-stu-id="bc877-208">Contact your system administrator to ensure your employee record is correctly associated.</span></span>

### <a name="translations-dont-display-correctly"></a><span data-ttu-id="bc877-209">Překlady se nezobrazují správně</span><span class="sxs-lookup"><span data-stu-id="bc877-209">Translations don't display correctly</span></span>

<span data-ttu-id="bc877-210">Pokud se překlady nezobrazují podle očekávání, ujistěte se, že jazyk, který vyberete v Teams, odpovídá jazyku vybranému v **Možnostech uživatele** Human Resources.</span><span class="sxs-lookup"><span data-stu-id="bc877-210">If translations don't display as expected, make sure the language you select in Teams matches the language selected in Human Resources **User options**.</span></span>

<span data-ttu-id="bc877-211">V Teams se podívejte na pole **Jazyk aplikace** v **Nastavení**.</span><span class="sxs-lookup"><span data-stu-id="bc877-211">In Teams, look at **App language** in **Settings**.</span></span>

![Nastavení Teams](./media/hr-teams-leave-app-settings.png)

<span data-ttu-id="bc877-213">V Human Resources vyberte **Nastavení** a poté vyberte **Možnosti uživatele**.</span><span class="sxs-lookup"><span data-stu-id="bc877-213">In Human Resources, select **Settings** and then select **User options**.</span></span> <span data-ttu-id="bc877-214">Ověřte, že pole **Jazyk** odpovídá poli **Jazyk aplikace** v Teams.</span><span class="sxs-lookup"><span data-stu-id="bc877-214">Verify that the **Language** field matches the **App language** field in Teams.</span></span>

![Možnosti uživatele v Human Resources](./media/hr-teams-leave-app-user-options.png)

<span data-ttu-id="bc877-216">Pokud problémy s překladem přetrvávají, dejte nám vědět.</span><span class="sxs-lookup"><span data-stu-id="bc877-216">If you still experience translation issues, let us know.</span></span> <span data-ttu-id="bc877-217">Informace najdete v tématu [Získání podpory pro aplikace Finance and Operations nebo Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).</span><span class="sxs-lookup"><span data-stu-id="bc877-217">For information, see [Get support for Finance and Operations apps or Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).</span></span>

### <a name="error-when-approving-leave-requests-in-the-human-resources-app-in-teams"></a><span data-ttu-id="bc877-218">Chyba při schvalování žádostí o dovolenou v aplikaci Human Resources v Teams</span><span class="sxs-lookup"><span data-stu-id="bc877-218">Error when approving leave requests in the Human Resources app in Teams</span></span>

<span data-ttu-id="bc877-219">Pokud se vám při pokusu o schválení žádostí o dovolenou v aplikaci Teams zobrazí chyba, zkuste v rámci řešení potíží následující kroky:</span><span class="sxs-lookup"><span data-stu-id="bc877-219">If you receive an error when you're trying to approve leave requests in the Teams app, try the following troubleshooting steps:</span></span>

1. <span data-ttu-id="bc877-220">Ověřte, že účet, který používáte k přihlášení k Microsoft Teams, je stejný, jaký používáte pro přístup k Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="bc877-220">Verify that the account you're using to sign into Microsoft Teams is the same one you use for accessing Dynamics 365 Human Resources.</span></span>

2. <span data-ttu-id="bc877-221">Ověřte, jestli jste platným schvalovatelem požadavku, a to kontrolou nastavení pracovního postupu pro schválení dovolené.</span><span class="sxs-lookup"><span data-stu-id="bc877-221">Verify that you're a valid approver for the request by checking the workflow settings for leave approval.</span></span> <span data-ttu-id="bc877-222">Další informace o pracovních postupech žádostí o dovolenou najdete v tématu [Vytvoření pracovního postupu žádosti o dovolenou](hr-leave-and-absence-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="bc877-222">For more information about leave request workflows, see [Create a leave request workflow](hr-leave-and-absence-workflow.md).</span></span>

### <a name="leave-approvers-dont-receive-teams-chat-messages-to-approve-leave-requests"></a><span data-ttu-id="bc877-223">Schvalovatelé dovolené nedostávají zprávy chatu Teams ke schválení žádostí o dovolenou</span><span class="sxs-lookup"><span data-stu-id="bc877-223">Leave approvers don't receive Teams chat messages to approve leave requests</span></span>

1. <span data-ttu-id="bc877-224">Zajistěte, aby byla povolena oznámení pro prostředí a uživatele.</span><span class="sxs-lookup"><span data-stu-id="bc877-224">Ensure notifications are enabled for the environment and the user.</span></span> <span data-ttu-id="bc877-225">Další informace viz [Povolení oznámení pro aplikaci Human Resources v Teams](hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams) a [Zapnutí nebo vypnutí oznámení aplikace Teams pro jednotlivé uživatele](hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users).</span><span class="sxs-lookup"><span data-stu-id="bc877-225">For more information, see [Enable notifications for the Human Resources app in Teams](hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams) and [Turn Teams notifications on or off for individual users](hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users).</span></span>

2. <span data-ttu-id="bc877-226">Ujistěte se, že jsou uživatelé přihlášeni ke kartě **Chaty** se stejnými přihlašovacími údaji, které používají pro schvalování žádostí o dovolenou.</span><span class="sxs-lookup"><span data-stu-id="bc877-226">Ensure users are signed into the **Chats** tab with the same credentials they use for approving leave requests.</span></span> <span data-ttu-id="bc877-227">Pomocí zpráv „odhlásit se“ a poté „přihlásit“ se přihlaste se správnými přihlašovacími údaji.</span><span class="sxs-lookup"><span data-stu-id="bc877-227">Use the messages "sign out" and then "sign in" to sign in with the correct credentials.</span></span>

3. <span data-ttu-id="bc877-228">Pokud problém přetrvává, zkontrolujte stav dávkové úlohy systému Business Events jako správce systému.</span><span class="sxs-lookup"><span data-stu-id="bc877-228">If the issue persists, check the status of the Business Events system batch job as a system administrator.</span></span> <span data-ttu-id="bc877-229">Pokud je ve fázi čekání nebo provádění, zkuste to znovu za několik minut.</span><span class="sxs-lookup"><span data-stu-id="bc877-229">If it's in a waiting or executing stage, check back in a few minutes.</span></span> <span data-ttu-id="bc877-230">Pokud se stav nezmění, přihlaste se na lístek podpory, aby náš tým mohl problém vyřešit.</span><span class="sxs-lookup"><span data-stu-id="bc877-230">If the status remains unchanged, log a support ticket so our team can help resolve the issue.</span></span>

## <a name="known-accessibility-issues"></a><span data-ttu-id="bc877-231">Známé problémy s usnadněním</span><span class="sxs-lookup"><span data-stu-id="bc877-231">Known accessibility issues</span></span>

<span data-ttu-id="bc877-232">Aplikace Human Resources v Teams má následující problémy s usnadněním, na jejichž řešení pracujeme pro budoucí verze.</span><span class="sxs-lookup"><span data-stu-id="bc877-232">The Human Resources app in Teams has the following accessibility issues that we're working on fixing in future releases.</span></span>

| <span data-ttu-id="bc877-233">Výdej</span><span class="sxs-lookup"><span data-stu-id="bc877-233">Issue</span></span> | <span data-ttu-id="bc877-234">Řešení nebo vysvětlení</span><span class="sxs-lookup"><span data-stu-id="bc877-234">Workaround or explanation</span></span> |
| --- | --- |
| <span data-ttu-id="bc877-235">Zvětšení plochy o 400 % skryje některá tlačítka akcí.</span><span class="sxs-lookup"><span data-stu-id="bc877-235">Zooming to 400% on desktop hides some of the action buttons from view.</span></span> | <span data-ttu-id="bc877-236">Doporučujeme místo toho používat lupu, dokud nebudeme moci tuto úroveň zvětšení podporovat.</span><span class="sxs-lookup"><span data-stu-id="bc877-236">We recommend using a magnifier instead until we can support this zoom level.</span></span> |
| <span data-ttu-id="bc877-237">Na kartě **Volno** hlasový komentář oznamuje akci tlačítka při čtení záhlaví mřížky volna.</span><span class="sxs-lookup"><span data-stu-id="bc877-237">On the **Time off** tab, voiceover announces a button action while reading the header for the time-off grid.</span></span> | <span data-ttu-id="bc877-238">Záhlaví a prvky v mřížce jsou seskupeny podle roku a jsou sbalitelné.</span><span class="sxs-lookup"><span data-stu-id="bc877-238">The header and elements within the grid are grouped by year, and they're collapsible.</span></span> <span data-ttu-id="bc877-239">Komentář to interpretuje jako položku s akcemi, kterou ale není.</span><span class="sxs-lookup"><span data-stu-id="bc877-239">Voiceover interprets this as an actionable item, but it isn't.</span></span> |
| <span data-ttu-id="bc877-240">Na kartě **Volno** je při přechodu na **Kód důvodu** v nové žádosti potřeba potáhnutí prstem navíc.</span><span class="sxs-lookup"><span data-stu-id="bc877-240">On the **Time off** tab, there's an extra swipe gesture when navigating to **Reason code** in a new request.</span></span> | <span data-ttu-id="bc877-241">Neexistuje žádný skrytý ovládací prvek, ke kterému se potáhnutí prstem pokouší dostat.</span><span class="sxs-lookup"><span data-stu-id="bc877-241">There is no hidden control that the swipe navigation is trying to get to.</span></span> |
| <span data-ttu-id="bc877-242">Na kartě **Volno**, pokud potáhnete prstem, když je kalendář otevřený, skončíte mimo ovládací prvek namísto horní části v nové žádosti nebo během úpravy požadavku.</span><span class="sxs-lookup"><span data-stu-id="bc877-242">On the **Time off** tab, if you swipe while the calendar is open, you end up outside the control instead of at the top in a new request or while editing a request.</span></span> | <span data-ttu-id="bc877-243">Když dosáhnete položky **Přejít na dnešek**, považujte to za konec ovládacího prvku a potáhnutím prstem opačným směrem se dostanete zpět nahoru.</span><span class="sxs-lookup"><span data-stu-id="bc877-243">When you reach **Go to today**, consider that to be the end of the control and swipe in the reverse direction to get back to the top.</span></span> |
| <span data-ttu-id="bc877-244">Na kartě **Chat**, když zadáte datum při používání asistenčního nástroje nebo navigace pomocí klávesnice, přeskočí fokus zpět na začátek.</span><span class="sxs-lookup"><span data-stu-id="bc877-244">On the **Chat** tab, the focus jumps back to the top when you enter a date while using the assistive tool or keyboard navigation.</span></span> | <span data-ttu-id="bc877-245">Stiskněte klávesu Tab, dokud se znovu nedostanete do oblasti zadávání.</span><span class="sxs-lookup"><span data-stu-id="bc877-245">Tab until you reach your input area again.</span></span> |

## <a name="privacy-notice"></a><span data-ttu-id="bc877-246">Oznámení o ochraně osobních údajů</span><span class="sxs-lookup"><span data-stu-id="bc877-246">Privacy notice</span></span>

### <a name="microsoft-language-understanding-intelligent-service-luis"></a><span data-ttu-id="bc877-247">Microsoft Language Understanding Intelligent Service (LUIS)</span><span class="sxs-lookup"><span data-stu-id="bc877-247">Microsoft Language Understanding Intelligent Service (LUIS)</span></span>

<span data-ttu-id="bc877-248">S robotem Dynamics 365 Human Resources v aplikaci Microsoft Teams jsou textové vstupy uživatele analyzovány pro porozumění základním dotazům/záměrům.</span><span class="sxs-lookup"><span data-stu-id="bc877-248">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="bc877-249">Vstup uživatele, například „Vyhledat účet Contoso“, je přesměrován na jednu ze služeb Cognitive Services společnosti Microsoft nazvanou Language Understanding Intelligent Service (LUIS).</span><span class="sxs-lookup"><span data-stu-id="bc877-249">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="bc877-250">Přečtěte si více o LUIS  [zde](https://www.luis.ai/).</span><span class="sxs-lookup"><span data-stu-id="bc877-250">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="bc877-251">Služba LUIS ujasňuje nebo chápe záměr vstupu uživatele (v tomto případě je záměrem najít informace) a cílovou entitu (v tomto případě je zamýšlenou entitou účet s názvem Contoso).</span><span class="sxs-lookup"><span data-stu-id="bc877-251">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="bc877-252">Tyto informace jsou poté předány do řešení  [Azure Bot Framework](https://azure.microsoft.com/services/bot-service/) společnosti Microsoft, které interaguje s daty z Dynamics 365 Human Resources a načte požadované informace pro uživatelský dotaz.</span><span class="sxs-lookup"><span data-stu-id="bc877-252">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/), which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="bc877-253">Instalací a umožněním přístupu k používání robota souhlasíte s tím, že umožníte službě LUIS a rámci robota Azure zpracovat záměr za vstupem, což má za následek vylepšenou konverzační uživatelskou zkušenost.</span><span class="sxs-lookup"><span data-stu-id="bc877-253">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="bc877-254">Služba LUIS a rámec robota Azure mohou mít ve srovnání s Dynamics 365 Human Resources různé úrovně shody.</span><span class="sxs-lookup"><span data-stu-id="bc877-254">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="bc877-255">Zatímco služba LUIS má přístup pouze k uživatelským dotazům a není určena k připojení k datům nebo účtu uživatele Dynamics 365 Human Resources, uživatel robota Dynamics 365 Human Resources může dobrovolně zadat dotaz obsahující zákaznická data, osobní údaje nebo jiná data a takový obsah dotazu by mohl být zaslán do služby LUIS a do rámce robota Azure.</span><span class="sxs-lookup"><span data-stu-id="bc877-255">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="bc877-256">Obsah dotazů a zpráv uživatele je v systému LUIS uchováván maximálně 30 dní, je šifrován a nepoužívá se pro školení ani zlepšení služeb.</span><span class="sxs-lookup"><span data-stu-id="bc877-256">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="bc877-257">Přečtěte si více o Cognitive Services  [zde](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span><span class="sxs-lookup"><span data-stu-id="bc877-257">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="bc877-258">Chcete-li spravovat nastavení administrátora pro aplikace v Microsoft Teams, přejděte do [centra pro správu Microsoft Teams](https://admin.teams.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="bc877-258">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span>

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a><span data-ttu-id="bc877-259">Microsoft Teams  Azure Event Grid a Azure Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="bc877-259">Microsoft Teams, Azure Event Grid, and Azure Cosmos DB</span></span>

<span data-ttu-id="bc877-260">Při použití aplikace Dynamics 365 Human Resources v Microsoft Teams mohou některá data zákazníků téct mimo geografickou oblast, kde je nasazena služba Human Resources vašeho klienta.</span><span class="sxs-lookup"><span data-stu-id="bc877-260">When using the Dynamics 365 Human Resources app in Microsoft Teams, certain customer data may flow outside of the geographic region where your tenant’s Human Resources service is deployed.</span></span>

<span data-ttu-id="bc877-261">Dynamics 365 Human Resources přenáší podrobnosti o žádosti o pracovní volno a úkolu pracovního postupu do Microsoft Azure Event Grid a Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="bc877-261">Dynamics 365 Human Resources transmits the employee’s leave request and workflow task details to Microsoft Azure Event Grid and Microsoft Teams.</span></span> <span data-ttu-id="bc877-262">Tato data mohou být uložena v Event Grid Microsoft Azure až 24 hodin a budou zpracována ve Spojených státech, jsou šifrována během přenosu a v klidu a nejsou používána společností Microsoft nebo jejími subprocesory pro školení nebo vylepšení služeb.</span><span class="sxs-lookup"><span data-stu-id="bc877-262">This data may be stored in Microsoft Azure Event Grid for up to 24 hours and will be processed in the United States, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="bc877-263">Chcete-li zjistit, kde jsou vaše data uložena v Teams, přečtěte si [Umístění dat v Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).</span><span class="sxs-lookup"><span data-stu-id="bc877-263">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).</span></span>

<span data-ttu-id="bc877-264">Při konverzaci s chatovacím robotem v aplikaci Human Resources může být obsah konverzace uložen v Azure Cosmos DB a přenesen do Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="bc877-264">While conversing with the chat bot in the Human Resources app, the conversation content may be stored in Azure Cosmos DB and transmitted to Microsoft Teams.</span></span> <span data-ttu-id="bc877-265">Tato data mohou být uložena v Azure Cosmos DB po dobu až 24 hodin a mohou být zpracovávána mimo geografickou oblast, kde je nasazena služba Human Resources vašeho nájemce, je šifrována během přenosu a v klidu a není používána společností Microsoft nebo jejími subprocesory pro školení nebo vylepšení služeb.</span><span class="sxs-lookup"><span data-stu-id="bc877-265">This data may be stored in Azure Cosmos DB for up to 24 hours and may be processed outside of the geographic region where your tenant's Human Resources service is deployed, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="bc877-266">Chcete-li zjistit, kde jsou vaše data uložena v Teams, přečtěte si [Umístění dat v Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).</span><span class="sxs-lookup"><span data-stu-id="bc877-266">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).</span></span>
 
<span data-ttu-id="bc877-267">Chcete-li omezit přístup k aplikaci Human Resources v Microsoft Teams pro vaši organizaci nebo uživatele ve vaší organizaci, přečtěte si [Spravujte zásady oprávnění aplikace v Microsoft Teams](/MicrosoftTeams/teams-app-permission-policies).</span><span class="sxs-lookup"><span data-stu-id="bc877-267">To restrict access to the Human Resources app in Microsoft Teams for your organization or users within your organization, see [Manage app permission policies in Microsoft Teams](/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="see-also"></a><span data-ttu-id="bc877-268">Viz také</span><span class="sxs-lookup"><span data-stu-id="bc877-268">See also</span></span>

[<span data-ttu-id="bc877-269">Stažení a instalace aplikace Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="bc877-269">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="bc877-270">Centrum nápovědy Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="bc877-270">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="bc877-271">Aplikace Human Resources v Teams</span><span class="sxs-lookup"><span data-stu-id="bc877-271">Human Resources app in Teams</span></span>](hr-admin-teams-leave-app.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
