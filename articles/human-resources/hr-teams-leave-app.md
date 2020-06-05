---
title: Správa žádostí o dovolenou v aplikaci Teams
description: Toto téma ukazuje, jak požádat o volno v aplikaci Dynamics 365 Human Resources v Microsoft Teams.
author: andreabichsel
manager: AnnBe
ms.date: 05/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 67501a1fa65493a1a23eb6176ece5be98d6e4659
ms.sourcegitcommit: 7fc0726c0a93ce6f4dafaad3232b4687f61cdc88
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/21/2020
ms.locfileid: "3393001"
---
# <a name="manage-leave-requests-in-teams"></a><span data-ttu-id="2ffa8-103">Správa žádostí o dovolenou v aplikaci Teams</span><span class="sxs-lookup"><span data-stu-id="2ffa8-103">Manage leave requests in Teams</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="2ffa8-104">Aplikace Microsoft Dynamics 365 Human Resources v aplikaci Microsoft Teams vám umožňuje rychle požádat o volno a zobrazit informace o svém zůstatku volna přímo v Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="2ffa8-104">The Microsoft Dynamics 365 Human Resources app in Microsoft Teams lets you quickly request time off and view your time-off balance information right in Microsoft Teams.</span></span> <span data-ttu-id="2ffa8-105">Můžete komunikovat s robotem a vyžádat si informace.</span><span class="sxs-lookup"><span data-stu-id="2ffa8-105">You can interact with a bot to request information.</span></span> <span data-ttu-id="2ffa8-106">Karta **Volno** poskytuje podrobnější informace.</span><span class="sxs-lookup"><span data-stu-id="2ffa8-106">The **Time off** tab provides more detailed information.</span></span>

## <a name="install-the-app"></a><span data-ttu-id="2ffa8-107">Instalace aplikace</span><span class="sxs-lookup"><span data-stu-id="2ffa8-107">Install the app</span></span>

<span data-ttu-id="2ffa8-108">Aplikaci Human Resources najdete v obchodě Teams.</span><span class="sxs-lookup"><span data-stu-id="2ffa8-108">You can find the Human Resources app in the Teams store.</span></span>

1. <span data-ttu-id="2ffa8-109">V aplikaci Microsoft Teams zvolte tři tečky.</span><span class="sxs-lookup"><span data-stu-id="2ffa8-109">In Microsoft Teams, select the ellipses.</span></span>

   ![Tři tečky aplikace pracovního volna Human Resources Teams](./media/hr-teams-leave-app-ellipses.png)
 
2. <span data-ttu-id="2ffa8-111">Vyhledejte Dynamics 365 Human Resources a poté vyberte dlaždici **Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="2ffa8-111">Search for Dynamics 365 Human Resources, and then select the **Human Resources** tile.</span></span>

   ![Dlaždice HR aplikace pracovního volna Human Resources Teams](./media/hr-teams-leave-app-human-resources-tile.png)

3. <span data-ttu-id="2ffa8-113">Vyberte tlačítko **Přidat** pro instalaci aplikace.</span><span class="sxs-lookup"><span data-stu-id="2ffa8-113">Select the **Add** button to install the app.</span></span>

   ![Instalace aplikace pracovního volna Human Resources Teams](./media/hr-teams-leave-app-in-store.png)

<span data-ttu-id="2ffa8-115">Pokud vás aplikace nepřihlásí automaticky, vyberte kartu **Nastavení** pro přihlášení.</span><span class="sxs-lookup"><span data-stu-id="2ffa8-115">If the app doesn't automatically sign you in, select the **Settings** tab to sign in.</span></span>

![Karta nastavení aplikace pracovního volna Human Resources Teams](./media/hr-teams-leave-app-settings-tab.png)

> [!NOTE]
> <span data-ttu-id="2ffa8-117">Pokud nevidíte přihlašovací dialogové okno, zkontrolujte nastavení prohlížeče a povolte automaticky otevíraná okna.</span><span class="sxs-lookup"><span data-stu-id="2ffa8-117">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span> 

<span data-ttu-id="2ffa8-118">Pokud máte přístup k více než jedné instanci aplikace Human Resources, můžete vybrat prostředí, ke kterému se chcete připojit, na kartě **Nastavení**.</span><span class="sxs-lookup"><span data-stu-id="2ffa8-118">If you have access to more than one instance of Human Resources, you can select which environment you want to connect to in the **Settings** tab.</span></span>

> [!WARNING]
> <span data-ttu-id="2ffa8-119">Aplikace aktuálně nepodporuje roli zabezpečení správce systému a zobrazí chybovou zprávu, pokud se přihlásíte pomocí účtu správce systému.</span><span class="sxs-lookup"><span data-stu-id="2ffa8-119">The app doesn't currently support the System Administrator security role, and will display an error message if you sign in with a System Administrator account.</span></span> <span data-ttu-id="2ffa8-120">Chcete-li se přihlásit pomocí jiného účtu, na kartě **Nastavení** vyberte tlačítko **Přepnout účty** a poté se přihlaste pomocí uživatelského účtu, který nemá oprávnění správce systému.</span><span class="sxs-lookup"><span data-stu-id="2ffa8-120">To sign in with a different account, on the **Settings** tab, select the **Switch accounts** button, and then sign in with a user account that doesn’t have System Administrator privileges.</span></span>
 
## <a name="use-the-bot"></a><span data-ttu-id="2ffa8-121">Použití robota</span><span class="sxs-lookup"><span data-stu-id="2ffa8-121">Use the bot</span></span>

<span data-ttu-id="2ffa8-122">Po instalaci aplikace se zobrazí uvítací zpráva, která vás informuje o typech akcí, které může robot provést vaším jménem.</span><span class="sxs-lookup"><span data-stu-id="2ffa8-122">After the app installs, a welcome message appears, letting you know the types of actions the bot can take on your behalf.</span></span>

![Uvítací zpráva robota aplikace pracovního volna Human Resources Teams](./media/hr-teams-leave-app-bot.png)
 
> [!NOTE]
> <span data-ttu-id="2ffa8-124">Při první interakci s robotem se možná budete muset přihlásit.</span><span class="sxs-lookup"><span data-stu-id="2ffa8-124">When first interacting with the bot, you might need to sign in.</span></span> <span data-ttu-id="2ffa8-125">Pokud nevidíte přihlašovací dialogové okno, zkontrolujte nastavení prohlížeče a povolte automaticky otevíraná okna.</span><span class="sxs-lookup"><span data-stu-id="2ffa8-125">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span>

<span data-ttu-id="2ffa8-126">Můžete požádat robota a následující akce:</span><span class="sxs-lookup"><span data-stu-id="2ffa8-126">You can ask the bot to:</span></span>

- <span data-ttu-id="2ffa8-127">Zobrazit informace o zůstatku volna pro každý typ volna, do kterého jste zaregistrováni.</span><span class="sxs-lookup"><span data-stu-id="2ffa8-127">Show time-off balance information for each leave type you're enrolled in.</span></span>

   ![Zobrazení zůstatků aplikace pracovního volna Human Resources Teams](./media/hr-teams-leave-app-bot-balances.png)
 
- <span data-ttu-id="2ffa8-129">Zobrazit další podrobnosti o konkrétním typu volna.</span><span class="sxs-lookup"><span data-stu-id="2ffa8-129">Show additional details about a specific leave type.</span></span>

   ![Zobrazení podrobností aplikace pracovního volna Human Resources Teams](./media/hr-teams-leave-app-bot-details.png)

- <span data-ttu-id="2ffa8-131">Zahájit žádost o volno za vás.</span><span class="sxs-lookup"><span data-stu-id="2ffa8-131">Start a leave request for you.</span></span>

   ![Žádost o volno aplikace pracovního volna Human Resources Teams](./media/hr-teams-leave-app-bot-request.png)
 
<span data-ttu-id="2ffa8-133">Po zahájení žádosti o volno můžete upravit dny přímo na kartě nebo můžete vybrat možnost **Upravit podrobnosti** pro přidání dalších informací k vaší žádosti.</span><span class="sxs-lookup"><span data-stu-id="2ffa8-133">After you start a leave request, you can adjust the days right within the card, or you can select **Edit details** to add additional information to your request.</span></span>

![Úprava žádosti aplikace pracovního volna Human Resources Teams](./media/hr-teams-leave-app-bot-edit.png)
 
<span data-ttu-id="2ffa8-135">Až zadáte informace, napište **Odeslat** pro odeslání žádosti ke schválení.</span><span class="sxs-lookup"><span data-stu-id="2ffa8-135">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="2ffa8-136">Můžete také naspat **Uložit jako koncept** a vrátit se k žádosti později.</span><span class="sxs-lookup"><span data-stu-id="2ffa8-136">You can also type **Save as draft** to come back to it later.</span></span>

![Odeslání žádosti aplikace pracovního volna Human Resources Teams](./media/hr-teams-leave-app-bot-submit.png)

## <a name="manage-your-leave-in-teams"></a><span data-ttu-id="2ffa8-138">Správa volna v aplikaci Teams</span><span class="sxs-lookup"><span data-stu-id="2ffa8-138">Manage your leave in Teams</span></span>

<span data-ttu-id="2ffa8-139">Karta **Volno** umožňuje zobrazit:</span><span class="sxs-lookup"><span data-stu-id="2ffa8-139">The **Time off** tab allows you to view:</span></span>

- <span data-ttu-id="2ffa8-140">Informace o zůstatku pro každý typ volna, ke kterému jste zaregistrováni</span><span class="sxs-lookup"><span data-stu-id="2ffa8-140">Balance information for each leave type you're enrolled in</span></span>

- <span data-ttu-id="2ffa8-141">Nadcházející žádosti o volno</span><span class="sxs-lookup"><span data-stu-id="2ffa8-141">Upcoming leave requests</span></span>

- <span data-ttu-id="2ffa8-142">Žádosti o volno</span><span class="sxs-lookup"><span data-stu-id="2ffa8-142">Time-off requests</span></span>

- <span data-ttu-id="2ffa8-143">Koncept žádostí o volno</span><span class="sxs-lookup"><span data-stu-id="2ffa8-143">Draft leave requests</span></span>

![Karta volna aplikace pracovního volna Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab.png)
 
### <a name="create-a-new-request"></a><span data-ttu-id="2ffa8-145">Vytvoření nové žádosti</span><span class="sxs-lookup"><span data-stu-id="2ffa8-145">Create a new request</span></span>

1. <span data-ttu-id="2ffa8-146">Chcete-li vytvořit novou žádost o volno, zvolte **Nová žádost**.</span><span class="sxs-lookup"><span data-stu-id="2ffa8-146">To create a new leave request, select **New request**.</span></span>

   ![Nová žádost aplikace pracovního volna Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab-new.png)

2. <span data-ttu-id="2ffa8-148">Zadejte den nebo dny, na které chcete volno, a poté vyberte **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="2ffa8-148">Enter the day or days you want to take off, and then select **Add**.</span></span>

   ![Přidání volna aplikace pracovního volna Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab-add.png)

3. <span data-ttu-id="2ffa8-150">V případě potřeby zadejte kód důvodu.</span><span class="sxs-lookup"><span data-stu-id="2ffa8-150">If applicable, enter a reason code.</span></span> <span data-ttu-id="2ffa8-151">Také zadejte případné komentáře a přidejte všechny přílohy.</span><span class="sxs-lookup"><span data-stu-id="2ffa8-151">Also enter any comments and add any attachments.</span></span>

4. <span data-ttu-id="2ffa8-152">Až zadáte informace, napište **Odeslat** pro odeslání žádosti ke schválení.</span><span class="sxs-lookup"><span data-stu-id="2ffa8-152">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="2ffa8-153">Můžete také naspat **Uložit jako koncept** a vrátit se k žádosti později.</span><span class="sxs-lookup"><span data-stu-id="2ffa8-153">You can also type **Save as draft** to come back to it later.</span></span>

### <a name="manage-draft-requests"></a><span data-ttu-id="2ffa8-154">Správa konceptů žádostí</span><span class="sxs-lookup"><span data-stu-id="2ffa8-154">Manage draft requests</span></span>

1. <span data-ttu-id="2ffa8-155">Zvolte kartu **Koncepty**.</span><span class="sxs-lookup"><span data-stu-id="2ffa8-155">Select the **Drafts** tab.</span></span>

   ![Karta konceptů aplikace pracovního volna Human Resources Teams](./media/hr-teams-leave-app-drafts-tab.png)

2. <span data-ttu-id="2ffa8-157">Vyberte symbol tužky, chcete-li žádost upravit, nebo vyberte koš, chcete-li žádost odstranit.</span><span class="sxs-lookup"><span data-stu-id="2ffa8-157">Select the pencil to edit the request, or select the trash can to delete the request.</span></span>

3. <span data-ttu-id="2ffa8-158">Proveďte potřebné změny.</span><span class="sxs-lookup"><span data-stu-id="2ffa8-158">Make any necessary changes.</span></span> <span data-ttu-id="2ffa8-159">Až zadáte informace, napište **Odeslat** pro odeslání žádosti ke schválení.</span><span class="sxs-lookup"><span data-stu-id="2ffa8-159">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="2ffa8-160">Můžete také zvolit **Uložit jako koncept** a vrátit se k žádosti později.</span><span class="sxs-lookup"><span data-stu-id="2ffa8-160">You can also select **Save as draft** to come back to it later.</span></span>

   ![Úprava konceptu aplikace pracovního volna Human Resources Teams](./media/hr-teams-leave-app-drafts-edit.png)
   
## <a name="privacy-notice"></a><span data-ttu-id="2ffa8-162">Oznámení o ochraně osobních údajů</span><span class="sxs-lookup"><span data-stu-id="2ffa8-162">Privacy notice</span></span>

<span data-ttu-id="2ffa8-163">S robotem Dynamics 365 Human Resources v aplikaci Microsoft Teams jsou textové vstupy uživatele analyzovány pro porozumění základním dotazům/záměrům.</span><span class="sxs-lookup"><span data-stu-id="2ffa8-163">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="2ffa8-164">Vstup uživatele, například „Vyhledat účet Contoso“, je přesměrován na jednu ze služeb Cognitive Services společnosti Microsoft nazvanou Language Understanding Intelligent Service (LUIS).</span><span class="sxs-lookup"><span data-stu-id="2ffa8-164">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="2ffa8-165">Přečtěte si více o LUIS  [zde](https://www.luis.ai/).</span><span class="sxs-lookup"><span data-stu-id="2ffa8-165">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="2ffa8-166">Služba LUIS ujasňuje nebo chápe záměr vstupu uživatele (v tomto případě je záměrem najít informace) a cílovou entitu (v tomto případě je zamýšlenou entitou účet s názvem Contoso).</span><span class="sxs-lookup"><span data-stu-id="2ffa8-166">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="2ffa8-167">Tyto informace jsou poté předány do  [rámce robota Azure](https://azure.microsoft.com/services/bot-service/)  společnosti Microsoft, který interaguje s daty z Dynamics 365 Human Resources a načte požadované informace pro uživatelský dotaz.</span><span class="sxs-lookup"><span data-stu-id="2ffa8-167">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/) which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="2ffa8-168">Instalací a umožněním přístupu k používání robota souhlasíte s tím, že umožníte službě LUIS a rámci robota Azure zpracovat záměr za vstupem, což má za následek vylepšenou konverzační uživatelskou zkušenost.</span><span class="sxs-lookup"><span data-stu-id="2ffa8-168">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="2ffa8-169">Služba LUIS a rámec robota Azure mohou mít ve srovnání s Dynamics 365 Human Resources různé úrovně shody.</span><span class="sxs-lookup"><span data-stu-id="2ffa8-169">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="2ffa8-170">Zatímco služba LUIS má přístup pouze k uživatelským dotazům a není určena k připojení k datům nebo účtu uživatele Dynamics 365 Human Resources, uživatel robota Dynamics 365 Human Resources může dobrovolně zadat dotaz obsahující zákaznická data, osobní údaje nebo jiná data a takový obsah dotazu by mohl být zaslán do služby LUIS a do rámce robota Azure.</span><span class="sxs-lookup"><span data-stu-id="2ffa8-170">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="2ffa8-171">Obsah dotazů a zpráv uživatele je v systému LUIS uchováván maximálně 30 dní, je šifrován a nepoužívá se pro školení ani zlepšení služeb.</span><span class="sxs-lookup"><span data-stu-id="2ffa8-171">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="2ffa8-172">Přečtěte si více o Cognitive Services  [zde](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span><span class="sxs-lookup"><span data-stu-id="2ffa8-172">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="2ffa8-173">Chcete-li spravovat nastavení administrátora pro aplikace v Microsoft Teams, přejděte do [centra pro správu Microsoft Teams](https://admin.teams.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="2ffa8-173">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span> 

## <a name="see-also"></a><span data-ttu-id="2ffa8-174">Viz také</span><span class="sxs-lookup"><span data-stu-id="2ffa8-174">See also</span></span>

[<span data-ttu-id="2ffa8-175">Stažení a instalace aplikace Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="2ffa8-175">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="2ffa8-176">Centrum nápovědy Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="2ffa8-176">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="2ffa8-177">Aplikace Human Resources v Teams</span><span class="sxs-lookup"><span data-stu-id="2ffa8-177">Human Resources app in Teams</span></span>](hr-admin-teams-leave-app.md)
