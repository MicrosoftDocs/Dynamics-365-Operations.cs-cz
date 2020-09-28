---
title: Aplikace Human Resources v Teams
description: V tomto tématu se seznámíte s aplikací Microsoft Dynamics 365 Human Resources v aplikaci Microsoft Teams.
author: andreabichsel
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: FeatureManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a022f8297066793080d254baa01410884a3fafd9
ms.sourcegitcommit: 55b729361ea852e38531c51972c6730e3d9c2b45
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/08/2020
ms.locfileid: "3776301"
---
# <a name="human-resources-app-in-teams"></a><span data-ttu-id="cd3bf-103">Aplikace Human Resources v Teams</span><span class="sxs-lookup"><span data-stu-id="cd3bf-103">Human Resources app in Teams</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="cd3bf-104">Aplikace Microsoft Dynamics 365 Human Resources v aplikaci Microsoft Teams umožňuje zaměstnancům rychle požádat o volno a zobrazit informace o jejich zůstatku volna v Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="cd3bf-104">The Microsoft Dynamics 365 Human Resources app in Microsoft Teams lets employees quickly request time off and view their time-off balance information in Microsoft Teams.</span></span> <span data-ttu-id="cd3bf-105">Zaměstnanci mohou komunikovat s robotem a vyžádat si informace.</span><span class="sxs-lookup"><span data-stu-id="cd3bf-105">Employees can interact with a bot to request information.</span></span> <span data-ttu-id="cd3bf-106">Karta **Volno** poskytuje podrobnější informace.</span><span class="sxs-lookup"><span data-stu-id="cd3bf-106">The **Time off** tab provides more detailed information.</span></span>

![Robot aplikace pracovního volna Human Resources Teams](./media/hr-admin-teams-leave-app-bot.png)

![Karta volna aplikace pracovního volna Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab.png)

## <a name="install-and-setup"></a><span data-ttu-id="cd3bf-109">Instalace a nastavení</span><span class="sxs-lookup"><span data-stu-id="cd3bf-109">Install and setup</span></span>

<span data-ttu-id="cd3bf-110">Aplikaci Human Resources najdete v obchodě Teams.</span><span class="sxs-lookup"><span data-stu-id="cd3bf-110">You can find the Human Resources app in the Teams store.</span></span> <span data-ttu-id="cd3bf-111">Informace o instalaci aplikace Teams najdete v části [Správa žádostí o dovolenou v aplikaci Teams](hr-teams-leave-app.md).</span><span class="sxs-lookup"><span data-stu-id="cd3bf-111">For information about installing the Teams app, see [Manage leave requests in Teams](hr-teams-leave-app.md).</span></span>

<span data-ttu-id="cd3bf-112">Informace o správě oprávnění k aplikaci v Teams naleznete v části [Správa zásad povolení k aplikaci v Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span><span class="sxs-lookup"><span data-stu-id="cd3bf-112">For information about managing app permissions in Teams, see [Manage app permission policies in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="enable-notifications-for-the-human-resources-app-in-teams"></a><span data-ttu-id="cd3bf-113">Povolení oznámení pro aplikaci Human Resources v Teams</span><span class="sxs-lookup"><span data-stu-id="cd3bf-113">Enable notifications for the Human Resources app in Teams</span></span>

<span data-ttu-id="cd3bf-114">Pokud chcete, aby uživatelé dostávali oznámení o žádostech o pracovní volno v aplikaci Teams, musíte povolit oznámení v aplikaci Human Resources.</span><span class="sxs-lookup"><span data-stu-id="cd3bf-114">If you want users to receive leave request notifications in the Teams app, you must enable notifications in Human Resources.</span></span>

>[!NOTE]
><span data-ttu-id="cd3bf-115">Oznámení dostanou pouze uživatelé, kteří jsou přihlášeni k Teams a používají aplikaci Human Resources Teams.</span><span class="sxs-lookup"><span data-stu-id="cd3bf-115">Only users who are signed into Teams and using the Human Resources Teams app will receive notifications.</span></span>

1. <span data-ttu-id="cd3bf-116">V modulu Human Resources vyberte **Správa systému**.</span><span class="sxs-lookup"><span data-stu-id="cd3bf-116">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="cd3bf-117">Vybrerte **Odkazy**.</span><span class="sxs-lookup"><span data-stu-id="cd3bf-117">Select **Links**.</span></span>

3. <span data-ttu-id="cd3bf-118">V části **Nastavení** vyberte **Systémové parametry**.</span><span class="sxs-lookup"><span data-stu-id="cd3bf-118">Under **Setup**, select **System parameters**.</span></span>

4. <span data-ttu-id="cd3bf-119">Na kartě **Obecné** nastavte možnost **Povolit oznámení pro aplikaci Teams** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="cd3bf-119">On the **General** tab, set **Enable notifications for Teams app** to **Yes**.</span></span>

   ![Povolení oznámení aplikace Teams v systémových parametrech](./media/hr-admin-teams-leave-app-enable-notifications.png)

5. <span data-ttu-id="cd3bf-121">Chcete-li zapnout oznámení Teams pro všechny uživatele, při výzvě vyberte **Ano**.</span><span class="sxs-lookup"><span data-stu-id="cd3bf-121">To turn on Teams notifications for all users, select **Yes** at the prompt.</span></span>

   ![Povolení oznámení Teams pro všechny uživatele](./media/hr-admin-teams-leave-app-notifications-all-users.png)

### <a name="turn-teams-notifications-on-or-off-for-individual-users"></a><span data-ttu-id="cd3bf-123">Zapnutí nebo vypnutí oznámení aplikace Teams pro jednotlivé uživatele</span><span class="sxs-lookup"><span data-stu-id="cd3bf-123">Turn Teams notifications on or off for individual users</span></span>

<span data-ttu-id="cd3bf-124">Jakmile povolíte oznámení pro aplikaci Human Resources Teams, můžete oznámení zapnout nebo vypnout pro jednotlivé uživatele.</span><span class="sxs-lookup"><span data-stu-id="cd3bf-124">After you've enabled notifications for the Human Resources Teams app, you can turn notifications on or off for individual users.</span></span>

1. <span data-ttu-id="cd3bf-125">V modulu Human Resources vyberte **Správa systému**.</span><span class="sxs-lookup"><span data-stu-id="cd3bf-125">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="cd3bf-126">Vybrerte **Odkazy**.</span><span class="sxs-lookup"><span data-stu-id="cd3bf-126">Select **Links**.</span></span>

3. <span data-ttu-id="cd3bf-127">V části **Uživatelé** vyberte **Možnosti uživatele**.</span><span class="sxs-lookup"><span data-stu-id="cd3bf-127">Under **Users**, select **User options**.</span></span>

4. <span data-ttu-id="cd3bf-128">Vyberte kartu **Pracovní postup**.</span><span class="sxs-lookup"><span data-stu-id="cd3bf-128">Select the **Workflow** tab.</span></span>

5. <span data-ttu-id="cd3bf-129">Nastavte možnost **Povolit oznámení pro aplikaci Teams** na **Ano**, čímž povolíte oznámení pro uživatele nebo **Ne**, čímž deaktivujete oznámení pro uživatele.</span><span class="sxs-lookup"><span data-stu-id="cd3bf-129">Set **Enable notifications for Teams app** to **Yes** to enable notifications for the user or **No** to disable notifications for the user.</span></span>

   ![Povolte oznámení aplikace Teams na kartě Možnosti uživatele na kartě Pracovní postup.](./media/hr-admin-teams-leave-app-notifications.png)

6. <span data-ttu-id="cd3bf-131">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="cd3bf-131">Select **Save**.</span></span>

## <a name="known-issues"></a><span data-ttu-id="cd3bf-132">Známé problémy</span><span class="sxs-lookup"><span data-stu-id="cd3bf-132">Known issues</span></span>

| <span data-ttu-id="cd3bf-133">Výdej</span><span class="sxs-lookup"><span data-stu-id="cd3bf-133">Issue</span></span> | <span data-ttu-id="cd3bf-134">Stav</span><span class="sxs-lookup"><span data-stu-id="cd3bf-134">Status</span></span> |
| --- | --- |
| <span data-ttu-id="cd3bf-135">Horizontální posouvání nefunguje na Android telefonech</span><span class="sxs-lookup"><span data-stu-id="cd3bf-135">Horizontal scrolling doesn't work on Android phones</span></span> | <span data-ttu-id="cd3bf-136">Horizontální posouvání není problém na zařízeních iOS nebo počítačích.</span><span class="sxs-lookup"><span data-stu-id="cd3bf-136">Horizontal scrolling isn't an issue on iOS or desktop devices.</span></span> <span data-ttu-id="cd3bf-137">Pracujeme na opravě pro Android.</span><span class="sxs-lookup"><span data-stu-id="cd3bf-137">We're working on a fix for Android.</span></span> |
| <span data-ttu-id="cd3bf-138">Chyba: Při hledání prostředí, ke kterému se lze připojit, došlo k problému.</span><span class="sxs-lookup"><span data-stu-id="cd3bf-138">Error: There is an issue finding an environment to connect to.</span></span> | <span data-ttu-id="cd3bf-139">Tato chyba se může zobrazit, i když jste ověřili, že uživatel má přístup k jednomu nebo více prostředím lidských zdrojů.</span><span class="sxs-lookup"><span data-stu-id="cd3bf-139">You might receive this error even if you've verified that the user can access one or more Human Resources environments.</span></span> <span data-ttu-id="cd3bf-140">Navíc možná neuvidíte všechna očekávaná prostředí.</span><span class="sxs-lookup"><span data-stu-id="cd3bf-140">Also, you might not see all the environments you expect.</span></span> <span data-ttu-id="cd3bf-141">Dokud tento problém nevyřešíme, odstraňte uživatele a znovu jej importujte, abyste problém vyřešili.</span><span class="sxs-lookup"><span data-stu-id="cd3bf-141">Until we fix this issue, delete the user and then import them in again to resolve the problem.</span></span> |
| <span data-ttu-id="cd3bf-142">Zůstatek je nesprávný při zadávání volna pro budoucí datum.</span><span class="sxs-lookup"><span data-stu-id="cd3bf-142">The balance is incorrect when submitting time off for a future date.</span></span> | <span data-ttu-id="cd3bf-143">Prognózy ještě nejsou k dispozici.</span><span class="sxs-lookup"><span data-stu-id="cd3bf-143">Forecasting isn't yet available.</span></span> <span data-ttu-id="cd3bf-144">Zůstatek se zobrazuje pro aktuální datum.</span><span class="sxs-lookup"><span data-stu-id="cd3bf-144">The balance displays for the current date.</span></span> |
| <span data-ttu-id="cd3bf-145">Nelze zrušit požadavek ve stavu **Probíhá kontrola**.</span><span class="sxs-lookup"><span data-stu-id="cd3bf-145">Unable to cancel an **In review** request.</span></span> | <span data-ttu-id="cd3bf-146">Tato funkce není momentálně podporována a bude přidána v budoucím vydání.</span><span class="sxs-lookup"><span data-stu-id="cd3bf-146">This functionality isn't currently supported and will be added in a future release.</span></span> |
| <span data-ttu-id="cd3bf-147">Informace o zůstatku se počítají od dnešního dne.</span><span class="sxs-lookup"><span data-stu-id="cd3bf-147">Balance information is calculated as of today.</span></span> | <span data-ttu-id="cd3bf-148">Systém aktuálně nezobrazuje zůstatky od období časového rozlišení, i když je nakonfigurováno v parametrech pracovního volna a absence.</span><span class="sxs-lookup"><span data-stu-id="cd3bf-148">The system currently doesn't display balances as of the accrual period, even if it's configured in Leave and absence parameters.</span></span> |

## <a name="privacy-notice"></a><span data-ttu-id="cd3bf-149">Oznámení o ochraně osobních údajů</span><span class="sxs-lookup"><span data-stu-id="cd3bf-149">Privacy notice</span></span>

### <a name="microsoft-language-understanding-intelligent-service-luis"></a><span data-ttu-id="cd3bf-150">Microsoft Language Understanding Intelligent Service (LUIS)</span><span class="sxs-lookup"><span data-stu-id="cd3bf-150">Microsoft Language Understanding Intelligent Service (LUIS)</span></span>

<span data-ttu-id="cd3bf-151">S robotem Dynamics 365 Human Resources v aplikaci Microsoft Teams jsou textové vstupy uživatele analyzovány pro porozumění základním dotazům/záměrům.</span><span class="sxs-lookup"><span data-stu-id="cd3bf-151">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="cd3bf-152">Vstup uživatele, například „Vyhledat účet Contoso“, je přesměrován na jednu ze služeb Cognitive Services společnosti Microsoft nazvanou Language Understanding Intelligent Service (LUIS).</span><span class="sxs-lookup"><span data-stu-id="cd3bf-152">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="cd3bf-153">Přečtěte si více o LUIS  [zde](https://www.luis.ai/).</span><span class="sxs-lookup"><span data-stu-id="cd3bf-153">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="cd3bf-154">Služba LUIS ujasňuje nebo chápe záměr vstupu uživatele (v tomto případě je záměrem najít informace) a cílovou entitu (v tomto případě je zamýšlenou entitou účet s názvem Contoso).</span><span class="sxs-lookup"><span data-stu-id="cd3bf-154">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="cd3bf-155">Tyto informace jsou poté předány do řešení  [Azure Bot Framework](https://azure.microsoft.com/services/bot-service/) společnosti Microsoft, které interaguje s daty z Dynamics 365 Human Resources a načte požadované informace pro uživatelský dotaz.</span><span class="sxs-lookup"><span data-stu-id="cd3bf-155">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/), which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="cd3bf-156">Instalací a umožněním přístupu k používání robota souhlasíte s tím, že umožníte službě LUIS a rámci robota Azure zpracovat záměr za vstupem, což má za následek vylepšenou konverzační uživatelskou zkušenost.</span><span class="sxs-lookup"><span data-stu-id="cd3bf-156">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="cd3bf-157">Služba LUIS a rámec robota Azure mohou mít ve srovnání s Dynamics 365 Human Resources různé úrovně shody.</span><span class="sxs-lookup"><span data-stu-id="cd3bf-157">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="cd3bf-158">Zatímco služba LUIS má přístup pouze k uživatelským dotazům a není určena k připojení k datům nebo účtu uživatele Dynamics 365 Human Resources, uživatel robota Dynamics 365 Human Resources může dobrovolně zadat dotaz obsahující zákaznická data, osobní údaje nebo jiná data a takový obsah dotazu by mohl být zaslán do služby LUIS a do rámce robota Azure.</span><span class="sxs-lookup"><span data-stu-id="cd3bf-158">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="cd3bf-159">Obsah dotazů a zpráv uživatele je v systému LUIS uchováván maximálně 30 dní, je šifrován a nepoužívá se pro školení ani zlepšení služeb.</span><span class="sxs-lookup"><span data-stu-id="cd3bf-159">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="cd3bf-160">Přečtěte si více o Cognitive Services  [zde](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span><span class="sxs-lookup"><span data-stu-id="cd3bf-160">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="cd3bf-161">Chcete-li spravovat nastavení administrátora pro aplikace v Microsoft Teams, přejděte do [centra pro správu Microsoft Teams](https://admin.teams.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="cd3bf-161">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span>

### <a name="microsoft-azure-event-grid-and-microsoft-teams"></a><span data-ttu-id="cd3bf-162">Microsoft Azure Event Grid a Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="cd3bf-162">Microsoft Azure Event Grid and Microsoft Teams</span></span>

<span data-ttu-id="cd3bf-163">Při použití funkce oznámení pro aplikaci Dynamics 365 Human Resources v Teams budou některá data zákazníků téct mimo geografickou oblast, kde je nasazena služba Human Resources vašeho klienta.</span><span class="sxs-lookup"><span data-stu-id="cd3bf-163">When using the notifications feature for the Dynamics 365 Human Resources app in Teams, certain customer data will flow outside of the geographic region where your tenant’s Human Resources service is deployed.</span></span> <span data-ttu-id="cd3bf-164">Dynamics 365 Human Resources přenáší podrobnosti o žádosti o pracovní volno a úkolu pracovního postupu do Microsoft Azure Event Grid a Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="cd3bf-164">Dynamics 365 Human Resources transmits the employee’s leave request and workflow task details to Microsoft Azure Event Grid and Microsoft Teams.</span></span> <span data-ttu-id="cd3bf-165">Tato data mohou být uložena až 24 hodin a zpracována ve Spojených státech, jsou šifrována během přenosu a v klidu a nejsou používána společností Microsoft nebo jejími subprocesory pro školení nebo vylepšení služeb.</span><span class="sxs-lookup"><span data-stu-id="cd3bf-165">This data may be stored for up to 24 hours and processed in the United States, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span>

## <a name="see-also"></a><span data-ttu-id="cd3bf-166">Viz také</span><span class="sxs-lookup"><span data-stu-id="cd3bf-166">See also</span></span> 

[<span data-ttu-id="cd3bf-167">Stažení a instalace aplikace Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="cd3bf-167">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="cd3bf-168">Centrum nápovědy Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="cd3bf-168">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="cd3bf-169">Správa žádostí o dovolenou v aplikaci Teams</span><span class="sxs-lookup"><span data-stu-id="cd3bf-169">Manage leave requests in Teams</span></span>](hr-teams-leave-app.md)

