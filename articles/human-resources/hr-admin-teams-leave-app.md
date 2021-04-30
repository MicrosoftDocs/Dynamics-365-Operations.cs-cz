---
title: Aplikace Human Resources v Teams
description: V tomto tématu se seznámíte s aplikací Microsoft Dynamics 365 Human Resources v aplikaci Microsoft Teams.
author: andreabichsel
ms.date: 02/23/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 3926acd07a68f59682c18f4f7bc290dc1e21d0b6
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/13/2021
ms.locfileid: "5889733"
---
# <a name="human-resources-app-in-teams"></a><span data-ttu-id="31da9-103">Aplikace Human Resources v Teams</span><span class="sxs-lookup"><span data-stu-id="31da9-103">Human Resources app in Teams</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="31da9-104">Aplikace Microsoft Dynamics 365 Human Resources v aplikaci Microsoft Teams umožňuje zaměstnancům rychle požádat o volno a zobrazit informace o jejich zůstatku volna v Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="31da9-104">The Microsoft Dynamics 365 Human Resources app in Microsoft Teams lets employees quickly request time off and view their time-off balance information in Microsoft Teams.</span></span> <span data-ttu-id="31da9-105">Zaměstnanci mohou komunikovat s robotem a vyžádat si informace.</span><span class="sxs-lookup"><span data-stu-id="31da9-105">Employees can interact with a bot to request information.</span></span> <span data-ttu-id="31da9-106">Karta **Volno** poskytuje podrobnější informace.</span><span class="sxs-lookup"><span data-stu-id="31da9-106">The **Time off** tab provides more detailed information.</span></span> <span data-ttu-id="31da9-107">Kromě toho můžou lidem posílat informace o svém nadcházejícím volnu v týmech a chatech mimo aplikaci Human Resources.</span><span class="sxs-lookup"><span data-stu-id="31da9-107">In addition, they can send people information about upcoming time off in teams and chats outside the Human Resources app.</span></span>

![Robot aplikace pracovního volna Human Resources Teams](./media/hr-teams-leave-app-bot.png)

![Karta volna aplikace pracovního volna Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab.png)

![Karta s žádostí o volno v Human Resources](./media/hr-teams-leave-app-chat-card.png)

## <a name="install-and-setup"></a><span data-ttu-id="31da9-111">Instalace a nastavení</span><span class="sxs-lookup"><span data-stu-id="31da9-111">Install and setup</span></span>

<span data-ttu-id="31da9-112">Aplikaci Dynamics 365 Human Resources najdete v obchodě Teams.</span><span class="sxs-lookup"><span data-stu-id="31da9-112">You can find the Dynamics 365 Human Resources app in the Teams store.</span></span> <span data-ttu-id="31da9-113">Informace o instalaci aplikace Teams najdete v části [Správa žádostí o dovolenou v aplikaci Teams](hr-teams-leave-app.md).</span><span class="sxs-lookup"><span data-stu-id="31da9-113">For information about installing the Teams app, see [Manage leave requests in Teams](hr-teams-leave-app.md).</span></span>

<span data-ttu-id="31da9-114">Informace o správě oprávnění k aplikaci v Teams naleznete v části [Správa zásad povolení k aplikaci v Microsoft Teams](/MicrosoftTeams/teams-app-permission-policies).</span><span class="sxs-lookup"><span data-stu-id="31da9-114">For information about managing app permissions in Teams, see [Manage app permission policies in Microsoft Teams](/MicrosoftTeams/teams-app-permission-policies).</span></span>

<span data-ttu-id="31da9-115">Pokud chcete, aby si uživatelé v aplikaci prohlíželi kalendář dovolené a nepřítomnosti, musíte povolit funkci **Kalendář dovolené a nepřítomnosti v Teams** ve Správě funkcí.</span><span class="sxs-lookup"><span data-stu-id="31da9-115">If you want your users to view the Leave and absence calendar in the app, you'll need to enable the **Leave and absence calendar in Teams** in Feature management.</span></span> <span data-ttu-id="31da9-116">Další informace o povolení funkcí naleznete v tématu [Správa funkcí](hr-admin-manage-features.md).</span><span class="sxs-lookup"><span data-stu-id="31da9-116">For more information about enabling features, see [Manage features](hr-admin-manage-features.md).</span></span>

## <a name="enable-notifications-for-the-human-resources-app-in-teams"></a><span data-ttu-id="31da9-117">Povolení oznámení pro aplikaci Human Resources v Teams</span><span class="sxs-lookup"><span data-stu-id="31da9-117">Enable notifications for the Human Resources app in Teams</span></span>

<span data-ttu-id="31da9-118">Pokud chcete, aby uživatelé dostávali oznámení o žádostech o pracovní volno v aplikaci Teams, musíte povolit oznámení v aplikaci Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="31da9-118">If you want users to receive leave request notifications in the Teams app, you must enable notifications in Dynamics 365 Human Resources.</span></span>

>[!NOTE]
><span data-ttu-id="31da9-119">Oznámení dostanou pouze uživatelé, kteří jsou přihlášeni do Teams a používají aplikaci Dynamics 365 Human Resources Teams.</span><span class="sxs-lookup"><span data-stu-id="31da9-119">Only users who are signed into Teams and using the Dynamics 365 Human Resources Teams app will receive notifications.</span></span>

1. <span data-ttu-id="31da9-120">V modulu Human Resources vyberte **Správa systému**.</span><span class="sxs-lookup"><span data-stu-id="31da9-120">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="31da9-121">Vybrerte **Odkazy**.</span><span class="sxs-lookup"><span data-stu-id="31da9-121">Select **Links**.</span></span>

3. <span data-ttu-id="31da9-122">V části **Nastavení** vyberte **Systémové parametry**.</span><span class="sxs-lookup"><span data-stu-id="31da9-122">Under **Setup**, select **System parameters**.</span></span>

4. <span data-ttu-id="31da9-123">Na kartě **Obecné** nastavte možnost **Povolit oznámení pro aplikaci Teams** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="31da9-123">On the **General** tab, set **Enable notifications for Teams app** to **Yes**.</span></span>

   ![Povolení oznámení aplikace Teams v systémových parametrech](./media/hr-admin-teams-leave-app-enable-notifications.png)

5. <span data-ttu-id="31da9-125">Chcete-li zapnout oznámení Teams pro všechny uživatele, při výzvě vyberte **Ano**.</span><span class="sxs-lookup"><span data-stu-id="31da9-125">To turn on Teams notifications for all users, select **Yes** at the prompt.</span></span>

   ![Povolení oznámení Teams pro všechny uživatele](./media/hr-admin-teams-leave-app-notifications-all-users.png)

### <a name="turn-teams-notifications-on-or-off-for-individual-users"></a><span data-ttu-id="31da9-127">Zapnutí nebo vypnutí oznámení aplikace Teams pro jednotlivé uživatele</span><span class="sxs-lookup"><span data-stu-id="31da9-127">Turn Teams notifications on or off for individual users</span></span>

<span data-ttu-id="31da9-128">Jakmile povolíte oznámení pro aplikaci Dynamics 365 Human Resources Teams, můžete oznámení zapnout nebo vypnout pro jednotlivé uživatele.</span><span class="sxs-lookup"><span data-stu-id="31da9-128">After you've enabled notifications for the Dynamics 365 Human Resources Teams app, you can turn notifications on or off for individual users.</span></span>

1. <span data-ttu-id="31da9-129">V modulu Human Resources vyberte **Správa systému**.</span><span class="sxs-lookup"><span data-stu-id="31da9-129">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="31da9-130">Vybrerte **Odkazy**.</span><span class="sxs-lookup"><span data-stu-id="31da9-130">Select **Links**.</span></span>

3. <span data-ttu-id="31da9-131">V části **Uživatelé** vyberte **Možnosti uživatele**.</span><span class="sxs-lookup"><span data-stu-id="31da9-131">Under **Users**, select **User options**.</span></span>

4. <span data-ttu-id="31da9-132">Vyberte kartu **Pracovní postup**.</span><span class="sxs-lookup"><span data-stu-id="31da9-132">Select the **Workflow** tab.</span></span>

5. <span data-ttu-id="31da9-133">Nastavte možnost **Povolit oznámení pro aplikaci Teams** na **Ano**, čímž povolíte oznámení pro uživatele nebo **Ne**, čímž deaktivujete oznámení pro uživatele.</span><span class="sxs-lookup"><span data-stu-id="31da9-133">Set **Enable notifications for Teams app** to **Yes** to enable notifications for the user or **No** to disable notifications for the user.</span></span>

   ![Povolte oznámení aplikace Teams na kartě Možnosti uživatele na kartě Pracovní postup.](./media/hr-admin-teams-leave-app-notifications.png)

6. <span data-ttu-id="31da9-135">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="31da9-135">Select **Save**.</span></span>

## <a name="supported-languages"></a><span data-ttu-id="31da9-136">Podporované jazyky</span><span class="sxs-lookup"><span data-stu-id="31da9-136">Supported languages</span></span>

<span data-ttu-id="31da9-137">Aplikace Dynamics 365 Human Resources v Teams podporuje následující jazyky:</span><span class="sxs-lookup"><span data-stu-id="31da9-137">The Dynamics 365 Human Resources app in Teams supports the following languages:</span></span>

| <span data-ttu-id="31da9-138">ID národního prostředí</span><span class="sxs-lookup"><span data-stu-id="31da9-138">Locale ID</span></span> | <span data-ttu-id="31da9-139">Jazyk</span><span class="sxs-lookup"><span data-stu-id="31da9-139">Language</span></span> |
| --- | --- |
| <span data-ttu-id="31da9-140">de-DE</span><span class="sxs-lookup"><span data-stu-id="31da9-140">de-DE</span></span> | <span data-ttu-id="31da9-141">Němčina (Německo)</span><span class="sxs-lookup"><span data-stu-id="31da9-141">German (Germany)</span></span> |
| <span data-ttu-id="31da9-142">es-ES</span><span class="sxs-lookup"><span data-stu-id="31da9-142">es-ES</span></span> | <span data-ttu-id="31da9-143">Španělština (Španělsko)</span><span class="sxs-lookup"><span data-stu-id="31da9-143">Spanish (Spain)</span></span> |
| <span data-ttu-id="31da9-144">es-MX</span><span class="sxs-lookup"><span data-stu-id="31da9-144">es-MX</span></span> | <span data-ttu-id="31da9-145">Španělština (Mexiko)</span><span class="sxs-lookup"><span data-stu-id="31da9-145">Spanish (Mexico)</span></span> |
| <span data-ttu-id="31da9-146">fr-CA</span><span class="sxs-lookup"><span data-stu-id="31da9-146">fr-CA</span></span> | <span data-ttu-id="31da9-147">Francouzština (Kanada)</span><span class="sxs-lookup"><span data-stu-id="31da9-147">French (Canada)</span></span> |
| <span data-ttu-id="31da9-148">fr-FR</span><span class="sxs-lookup"><span data-stu-id="31da9-148">fr-FR</span></span> | <span data-ttu-id="31da9-149">Francouzština (Francie)</span><span class="sxs-lookup"><span data-stu-id="31da9-149">French (France)</span></span> |
| <span data-ttu-id="31da9-150">it-IT</span><span class="sxs-lookup"><span data-stu-id="31da9-150">it-IT</span></span> | <span data-ttu-id="31da9-151">Italština (Itálie)</span><span class="sxs-lookup"><span data-stu-id="31da9-151">Italian (Italy)</span></span> |
| <span data-ttu-id="31da9-152">nl-NL</span><span class="sxs-lookup"><span data-stu-id="31da9-152">nl-NL</span></span> | <span data-ttu-id="31da9-153">Holandština (Nizozemsko)</span><span class="sxs-lookup"><span data-stu-id="31da9-153">Dutch (Netherlands)</span></span> |
| <span data-ttu-id="31da9-154">pt-BR</span><span class="sxs-lookup"><span data-stu-id="31da9-154">pt-BR</span></span> | <span data-ttu-id="31da9-155">Portugalština (Brazílie)</span><span class="sxs-lookup"><span data-stu-id="31da9-155">Portuguese (Brazil)</span></span> |
| <span data-ttu-id="31da9-156">tr-TR</span><span class="sxs-lookup"><span data-stu-id="31da9-156">tr-TR</span></span> | <span data-ttu-id="31da9-157">Turečtina (Turecko)</span><span class="sxs-lookup"><span data-stu-id="31da9-157">Turkish (Turkey)</span></span> |
| <span data-ttu-id="31da9-158">zh-CN</span><span class="sxs-lookup"><span data-stu-id="31da9-158">zh-CN</span></span> | <span data-ttu-id="31da9-159">Čínština (zjednodušená)</span><span class="sxs-lookup"><span data-stu-id="31da9-159">Chinese (Simplified)</span></span> |

## <a name="notes"></a><span data-ttu-id="31da9-160">Poznámky</span><span class="sxs-lookup"><span data-stu-id="31da9-160">Notes</span></span>

<span data-ttu-id="31da9-161">Následující pracovní položky jsou určeny pro budoucí vydání:</span><span class="sxs-lookup"><span data-stu-id="31da9-161">The following work items are slated for future releases:</span></span>

| <span data-ttu-id="31da9-162">Pracovní položka</span><span class="sxs-lookup"><span data-stu-id="31da9-162">Work item</span></span> | <span data-ttu-id="31da9-163">Stav</span><span class="sxs-lookup"><span data-stu-id="31da9-163">Status</span></span> |
| --- | --- |
| <span data-ttu-id="31da9-164">Zůstatek je nesprávný při zadávání volna pro budoucí datum.</span><span class="sxs-lookup"><span data-stu-id="31da9-164">The balance is incorrect when submitting time off for a future date.</span></span> | <span data-ttu-id="31da9-165">Prognózy ještě nejsou k dispozici.</span><span class="sxs-lookup"><span data-stu-id="31da9-165">Forecasting isn't yet available.</span></span> <span data-ttu-id="31da9-166">Zůstatek se zobrazuje pro aktuální datum.</span><span class="sxs-lookup"><span data-stu-id="31da9-166">The balance displays for the current date.</span></span> |
| <span data-ttu-id="31da9-167">Nelze zrušit požadavek ve stavu **Probíhá kontrola**.</span><span class="sxs-lookup"><span data-stu-id="31da9-167">Unable to cancel an **In review** request.</span></span> | <span data-ttu-id="31da9-168">Tato funkce není momentálně podporována a bude přidána v budoucím vydání.</span><span class="sxs-lookup"><span data-stu-id="31da9-168">This functionality isn't currently supported and will be added in a future release.</span></span> |
| <span data-ttu-id="31da9-169">Informace o zůstatku se počítají od dnešního dne.</span><span class="sxs-lookup"><span data-stu-id="31da9-169">Balance information is calculated as of today.</span></span> | <span data-ttu-id="31da9-170">Systém aktuálně nezobrazuje zůstatky od období časového rozlišení, i když je nakonfigurováno v parametrech pracovního volna a absence.</span><span class="sxs-lookup"><span data-stu-id="31da9-170">The system currently doesn't display balances as of the accrual period, even if it's configured in Leave and absence parameters.</span></span> |

## <a name="troubleshooting"></a><span data-ttu-id="31da9-171">Řešení potíží</span><span class="sxs-lookup"><span data-stu-id="31da9-171">Troubleshooting</span></span>

<span data-ttu-id="31da9-172">Pokud má uživatel potíže s přihlášením nebo používáním aplikace Human Resources Teams, zkuste problémy vyřešit podle těchto pokynů.</span><span class="sxs-lookup"><span data-stu-id="31da9-172">If a user is having trouble signing into or using the Human Resources Teams app, try following these troubleshooting instructions.</span></span> <span data-ttu-id="31da9-173">Pokud problémy přetrvávají i po pokusu o vyřešení, obraťte se na podporu.</span><span class="sxs-lookup"><span data-stu-id="31da9-173">If you're still having problems after troubleshooting, contact Support.</span></span> <span data-ttu-id="31da9-174">Pro další informace si přečtěte [Získání podpory](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span><span class="sxs-lookup"><span data-stu-id="31da9-174">For more information, see [Get support](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span></span>

### <a name="cant-sign-into-the-human-resources-app-in-teams"></a><span data-ttu-id="31da9-175">Nelze se přihlásit do aplikace Human Resources v Teams</span><span class="sxs-lookup"><span data-stu-id="31da9-175">Can't sign into the Human Resources app in Teams</span></span>

<span data-ttu-id="31da9-176">Pokud vás uživatel kontaktuje, protože se nemůže přihlásit do aplikace, ověřte, zda má přidružený záznam zaměstnance v Human Resources.</span><span class="sxs-lookup"><span data-stu-id="31da9-176">If a user contacts you because they can't sign into the app, verify that they have an associated employee record in Human Resources.</span></span>

### <a name="error-when-approving-leave-requests-in-the-human-resources-app-in-teams"></a><span data-ttu-id="31da9-177">Chyba při schvalování žádostí o dovolenou v aplikaci Human Resources v Teams</span><span class="sxs-lookup"><span data-stu-id="31da9-177">Error when approving leave requests in the Human Resources app in Teams</span></span>

<span data-ttu-id="31da9-178">Pokud se uživateli při pokusu o schválení žádostí o dovolenou v aplikaci Teams zobrazí chyba, zkuste v rámci řešení potíží následující kroky:</span><span class="sxs-lookup"><span data-stu-id="31da9-178">If a user receives an error while trying to approve,  leave requests in the Teams app, try the following troubleshooting steps:</span></span>

1. <span data-ttu-id="31da9-179">Ověřte, že jeho účet Teams je stejný, jaký používá pro přístup k Human Resources.</span><span class="sxs-lookup"><span data-stu-id="31da9-179">Verify that their Teams account is the same one they use for accessing Human Resources.</span></span>

2. <span data-ttu-id="31da9-180">Ověřte, zda je platným schvalovatelem požadavku, a to kontrolou nastavení pracovního postupu pro schválení dovolené.</span><span class="sxs-lookup"><span data-stu-id="31da9-180">Verify that they're a valid approver for the request by checking the workflow settings for leave approval.</span></span> <span data-ttu-id="31da9-181">Další informace o pracovních postupech žádostí o dovolenou najdete v tématu [Vytvoření pracovního postupu žádosti o dovolenou](hr-leave-and-absence-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="31da9-181">For more information about leave request workflows, see [Create a leave request workflow](hr-leave-and-absence-workflow.md).</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="31da9-182">Oznámení o ochraně osobních údajů</span><span class="sxs-lookup"><span data-stu-id="31da9-182">Privacy notice</span></span>

### <a name="microsoft-language-understanding-intelligent-service-luis"></a><span data-ttu-id="31da9-183">Microsoft Language Understanding Intelligent Service (LUIS)</span><span class="sxs-lookup"><span data-stu-id="31da9-183">Microsoft Language Understanding Intelligent Service (LUIS)</span></span>

<span data-ttu-id="31da9-184">S robotem Dynamics 365 Human Resources v aplikaci Microsoft Teams jsou textové vstupy uživatele analyzovány pro porozumění základním dotazům/záměrům.</span><span class="sxs-lookup"><span data-stu-id="31da9-184">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="31da9-185">Vstup uživatele, například „Vyhledat účet Contoso“, je přesměrován na jednu ze služeb Cognitive Services společnosti Microsoft nazvanou Language Understanding Intelligent Service (LUIS).</span><span class="sxs-lookup"><span data-stu-id="31da9-185">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="31da9-186">Přečtěte si více o LUIS  [zde](https://www.luis.ai/).</span><span class="sxs-lookup"><span data-stu-id="31da9-186">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="31da9-187">Služba LUIS ujasňuje nebo chápe záměr vstupu uživatele (v tomto případě je záměrem najít informace) a cílovou entitu (v tomto případě je zamýšlenou entitou účet s názvem Contoso).</span><span class="sxs-lookup"><span data-stu-id="31da9-187">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="31da9-188">Tyto informace jsou poté předány do řešení  [Azure Bot Framework](https://azure.microsoft.com/services/bot-service/) společnosti Microsoft, které interaguje s daty z Dynamics 365 Human Resources a načte požadované informace pro uživatelský dotaz.</span><span class="sxs-lookup"><span data-stu-id="31da9-188">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/), which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="31da9-189">Instalací a umožněním přístupu k používání robota souhlasíte s tím, že umožníte službě LUIS a rámci robota Azure zpracovat záměr za vstupem, což má za následek vylepšenou konverzační uživatelskou zkušenost.</span><span class="sxs-lookup"><span data-stu-id="31da9-189">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="31da9-190">Služba LUIS a rámec robota Azure mohou mít ve srovnání s Dynamics 365 Human Resources různé úrovně shody.</span><span class="sxs-lookup"><span data-stu-id="31da9-190">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="31da9-191">Zatímco služba LUIS má přístup pouze k uživatelským dotazům a není určena k připojení k datům nebo účtu uživatele Dynamics 365 Human Resources, uživatel robota Dynamics 365 Human Resources může dobrovolně zadat dotaz obsahující zákaznická data, osobní údaje nebo jiná data a takový obsah dotazu by mohl být zaslán do služby LUIS a do rámce robota Azure.</span><span class="sxs-lookup"><span data-stu-id="31da9-191">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="31da9-192">Obsah dotazů a zpráv uživatele je v systému LUIS uchováván maximálně 30 dní, je šifrován a nepoužívá se pro školení ani zlepšení služeb.</span><span class="sxs-lookup"><span data-stu-id="31da9-192">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="31da9-193">Přečtěte si více o Cognitive Services  [zde](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span><span class="sxs-lookup"><span data-stu-id="31da9-193">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="31da9-194">Chcete-li spravovat nastavení administrátora pro aplikace v Microsoft Teams, přejděte do [centra pro správu Microsoft Teams](https://admin.teams.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="31da9-194">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span>

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a><span data-ttu-id="31da9-195">Microsoft Teams  Azure Event Grid a Azure Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="31da9-195">Microsoft Teams, Azure Event Grid, and Azure Cosmos DB</span></span>

<span data-ttu-id="31da9-196">Při použití aplikace Dynamics 365 Human Resources v Microsoft Teams mohou některá data zákazníků téct mimo geografickou oblast, kde je nasazena služba Human Resources vašeho klienta.</span><span class="sxs-lookup"><span data-stu-id="31da9-196">When using the Dynamics 365 Human Resources app in Microsoft Teams, certain customer data may flow outside of the geographic region where your tenant’s Human Resources service is deployed.</span></span>

<span data-ttu-id="31da9-197">Dynamics 365 Human Resources přenáší podrobnosti o žádosti o pracovní volno a úkolu pracovního postupu do Microsoft Azure Event Grid a Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="31da9-197">Dynamics 365 Human Resources transmits the employee’s leave request and workflow task details to Microsoft Azure Event Grid and Microsoft Teams.</span></span> <span data-ttu-id="31da9-198">Tato data mohou být uložena v Event Grid Microsoft Azure až 24 hodin a budou zpracována ve Spojených státech, jsou šifrována během přenosu a v klidu a nejsou používána společností Microsoft nebo jejími subprocesory pro školení nebo vylepšení služeb.</span><span class="sxs-lookup"><span data-stu-id="31da9-198">This data may be stored in Microsoft Azure Event Grid for up to 24 hours and will be processed in the United States, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="31da9-199">Chcete-li zjistit, kde jsou vaše data uložena v Teams, přečtěte si [Umístění dat v Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).</span><span class="sxs-lookup"><span data-stu-id="31da9-199">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).</span></span>

<span data-ttu-id="31da9-200">Při konverzaci s chatovacím robotem v aplikaci Human Resources může být obsah konverzace uložen v Azure Cosmos DB a přenesen do Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="31da9-200">While conversing with the chat bot in the Human Resources app, the conversation content may be stored in Azure Cosmos DB and transmitted to Microsoft Teams.</span></span> <span data-ttu-id="31da9-201">Tato data mohou být uložena v Azure Cosmos DB po dobu až 24 hodin a mohou být zpracovávána mimo geografickou oblast, kde je nasazena služba Human Resources vašeho nájemce, je šifrována během přenosu a v klidu a není používána společností Microsoft nebo jejími subprocesory pro školení nebo vylepšení služeb.</span><span class="sxs-lookup"><span data-stu-id="31da9-201">This data may be stored in Azure Cosmos DB for up to 24 hours and may be processed outside of the geographic region where your tenant's Human Resources service is deployed, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="31da9-202">Chcete-li zjistit, kde jsou vaše data uložena v Teams, přečtěte si [Umístění dat v Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).</span><span class="sxs-lookup"><span data-stu-id="31da9-202">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).</span></span>
 
<span data-ttu-id="31da9-203">Chcete-li omezit přístup k aplikaci Human Resources v Microsoft Teams pro vaši organizaci nebo uživatele ve vaší organizaci, přečtěte si [Spravujte zásady oprávnění aplikace v Microsoft Teams](/MicrosoftTeams/teams-app-permission-policies).</span><span class="sxs-lookup"><span data-stu-id="31da9-203">To restrict access to the Human Resources app in Microsoft Teams for your organization or users within your organization, see [Manage app permission policies in Microsoft Teams](/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="see-also"></a><span data-ttu-id="31da9-204">Viz také</span><span class="sxs-lookup"><span data-stu-id="31da9-204">See also</span></span> 

[<span data-ttu-id="31da9-205">Stažení a instalace aplikace Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="31da9-205">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="31da9-206">Centrum nápovědy Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="31da9-206">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="31da9-207">Správa žádostí o dovolenou v aplikaci Teams</span><span class="sxs-lookup"><span data-stu-id="31da9-207">Manage leave requests in Teams</span></span>](hr-teams-leave-app.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]