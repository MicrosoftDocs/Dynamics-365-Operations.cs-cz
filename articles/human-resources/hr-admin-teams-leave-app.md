---
title: Aplikace Human Resources v Teams
description: V tomto tématu se seznámíte s aplikací Microsoft Dynamics 365 Human Resources v aplikaci Microsoft Teams.
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
ms.openlocfilehash: 423ec36a73e8af9d915c5cfe16bd4d552448e2b6
ms.sourcegitcommit: d1541831d556b722a71aed442043ffb4a4576d87
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/20/2020
ms.locfileid: "3388109"
---
# <a name="human-resources-app-in-teams"></a><span data-ttu-id="ab3d7-103">Aplikace Human Resources v Teams</span><span class="sxs-lookup"><span data-stu-id="ab3d7-103">Human Resources app in Teams</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="ab3d7-104">Aplikace Microsoft Dynamics 365 Human Resources v aplikaci Microsoft Teams umožňuje zaměstnancům rychle požádat o volno a zobrazit informace o jejich zůstatku volna v Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="ab3d7-104">The Microsoft Dynamics 365 Human Resources app in Microsoft Teams lets employees quickly request time off and view their time-off balance information in Microsoft Teams.</span></span> <span data-ttu-id="ab3d7-105">Zaměstnanci mohou komunikovat s robotem a vyžádat si informace.</span><span class="sxs-lookup"><span data-stu-id="ab3d7-105">Employees can interact with a bot to request information.</span></span> <span data-ttu-id="ab3d7-106">Karta **Volno** poskytuje podrobnější informace.</span><span class="sxs-lookup"><span data-stu-id="ab3d7-106">The **Time off** tab provides more detailed information.</span></span>

![Robot aplikace pracovního volna Human Resources Teams](./media/hr-admin-teams-leave-app-bot.png)

![Karta volna aplikace pracovního volna Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab.png)

## <a name="install-and-setup"></a><span data-ttu-id="ab3d7-109">Instalace a nastavení</span><span class="sxs-lookup"><span data-stu-id="ab3d7-109">Install and setup</span></span>

<span data-ttu-id="ab3d7-110">Aplikaci Human Resources najdete v obchodě Teams.</span><span class="sxs-lookup"><span data-stu-id="ab3d7-110">You can find the Human Resources app in the Teams store.</span></span> <span data-ttu-id="ab3d7-111">Informace o instalaci aplikace Teams najdete v části [Správa žádostí o dovolenou v aplikaci Teams](hr-teams-leave-app.md).</span><span class="sxs-lookup"><span data-stu-id="ab3d7-111">For information about installing the Teams app, see [Manage leave requests in Teams](hr-teams-leave-app.md).</span></span>

<span data-ttu-id="ab3d7-112">Informace o správě oprávnění k aplikaci v Teams naleznete v části [Správa zásad povolení k aplikaci v Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span><span class="sxs-lookup"><span data-stu-id="ab3d7-112">For information about managing app permissions in Teams, see [Manage app permission policies in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="known-issues"></a><span data-ttu-id="ab3d7-113">Známé problémy</span><span class="sxs-lookup"><span data-stu-id="ab3d7-113">Known issues</span></span>

| <span data-ttu-id="ab3d7-114">Výdej</span><span class="sxs-lookup"><span data-stu-id="ab3d7-114">Issue</span></span> | <span data-ttu-id="ab3d7-115">Stav</span><span class="sxs-lookup"><span data-stu-id="ab3d7-115">Status</span></span> |
| --- | --- |
| <span data-ttu-id="ab3d7-116">Zůstatek je nesprávný při zadávání volna pro budoucí datum.</span><span class="sxs-lookup"><span data-stu-id="ab3d7-116">The balance is incorrect when submitting time off for a future date.</span></span> | <span data-ttu-id="ab3d7-117">Prognózy ještě nejsou k dispozici.</span><span class="sxs-lookup"><span data-stu-id="ab3d7-117">Forecasting isn't yet available.</span></span> <span data-ttu-id="ab3d7-118">Zůstatek se zobrazuje pro aktuální datum.</span><span class="sxs-lookup"><span data-stu-id="ab3d7-118">The balance displays for the current date.</span></span> |
| <span data-ttu-id="ab3d7-119">Při snižování počtu hodin obsažených ve stávající žádosti **Zůstatek účtu** klesá místo aby stoupal.</span><span class="sxs-lookup"><span data-stu-id="ab3d7-119">When reducing the number of hours taken in an existing request, the **Remaining balance** goes down instead of up.</span></span> | <span data-ttu-id="ab3d7-120">Budeme řešit tento známý problém v budoucnosti.</span><span class="sxs-lookup"><span data-stu-id="ab3d7-120">We'll address this known issue in the future.</span></span> <span data-ttu-id="ab3d7-121">Zobrazení je nesprávné, ale správná množství jsou upravena po odeslání.</span><span class="sxs-lookup"><span data-stu-id="ab3d7-121">The display is incorrect, but the correct amounts are adjusted upon submission.</span></span> |
| <span data-ttu-id="ab3d7-122">Pro stejná data se zobrazují dvě karty **Nadcházející volno**.</span><span class="sxs-lookup"><span data-stu-id="ab3d7-122">Two **Upcoming time off** cards display for the same dates.</span></span> | <span data-ttu-id="ab3d7-123">Karty představují jednotlivá odeslání.</span><span class="sxs-lookup"><span data-stu-id="ab3d7-123">The cards represent individual submissions.</span></span> <span data-ttu-id="ab3d7-124">Budeme i nadále brát v potaz zpětnou vazbu a provádět úpravy.</span><span class="sxs-lookup"><span data-stu-id="ab3d7-124">We'll continue to take feedback and make adjustments.</span></span> |
| <span data-ttu-id="ab3d7-125">Nelze zrušit požadavek ve stavu **Probíhá kontrola**.</span><span class="sxs-lookup"><span data-stu-id="ab3d7-125">Unable to cancel an **In review** request.</span></span> | <span data-ttu-id="ab3d7-126">Tato funkce není momentálně podporována a bude přidána v budoucím vydání.</span><span class="sxs-lookup"><span data-stu-id="ab3d7-126">This functionality isn't currently supported and will be added in a future release.</span></span> |
| <span data-ttu-id="ab3d7-127">Informace o zůstatku se počítají od dnešního dne.</span><span class="sxs-lookup"><span data-stu-id="ab3d7-127">Balance information is calculated as of today.</span></span> | <span data-ttu-id="ab3d7-128">Systém aktuálně nezobrazuje zůstatky od období časového rozlišení, i když je nakonfigurováno v parametrech pracovního volna a absence.</span><span class="sxs-lookup"><span data-stu-id="ab3d7-128">The system currently doesn't display balances as of the accrual period, even if it's configured in Leave and absence parameters.</span></span> |

## <a name="privacy-notice"></a><span data-ttu-id="ab3d7-129">Oznámení o ochraně osobních údajů</span><span class="sxs-lookup"><span data-stu-id="ab3d7-129">Privacy notice</span></span>

<span data-ttu-id="ab3d7-130">S robotem Dynamics 365 Human Resources v aplikaci Microsoft Teams jsou textové vstupy uživatele analyzovány pro porozumění základním dotazům/záměrům.</span><span class="sxs-lookup"><span data-stu-id="ab3d7-130">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="ab3d7-131">Vstup uživatele, například „Vyhledat účet Contoso“, je přesměrován na jednu ze služeb Cognitive Services společnosti Microsoft nazvanou Language Understanding Intelligent Service (LUIS).</span><span class="sxs-lookup"><span data-stu-id="ab3d7-131">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="ab3d7-132">Přečtěte si více o LUIS  [zde](https://www.luis.ai/).</span><span class="sxs-lookup"><span data-stu-id="ab3d7-132">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="ab3d7-133">Služba LUIS ujasňuje nebo chápe záměr vstupu uživatele (v tomto případě je záměrem najít informace) a cílovou entitu (v tomto případě je zamýšlenou entitou účet s názvem Contoso).</span><span class="sxs-lookup"><span data-stu-id="ab3d7-133">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="ab3d7-134">Tyto informace jsou poté předány do  [rámce robota Azure](https://azure.microsoft.com/services/bot-service/)  společnosti Microsoft, který interaguje s daty z Dynamics 365 Human Resources a načte požadované informace pro uživatelský dotaz.</span><span class="sxs-lookup"><span data-stu-id="ab3d7-134">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/) which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="ab3d7-135">Instalací a umožněním přístupu k používání robota souhlasíte s tím, že umožníte službě LUIS a rámci robota Azure zpracovat záměr za vstupem, což má za následek vylepšenou konverzační uživatelskou zkušenost.</span><span class="sxs-lookup"><span data-stu-id="ab3d7-135">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="ab3d7-136">Služba LUIS a rámec robota Azure mohou mít ve srovnání s Dynamics 365 Human Resources různé úrovně shody.</span><span class="sxs-lookup"><span data-stu-id="ab3d7-136">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="ab3d7-137">Zatímco služba LUIS má přístup pouze k uživatelským dotazům a není určena k připojení k datům nebo účtu uživatele Dynamics 365 Human Resources, uživatel robota Dynamics 365 Human Resources může dobrovolně zadat dotaz obsahující zákaznická data, osobní údaje nebo jiná data a takový obsah dotazu by mohl být zaslán do služby LUIS a do rámce robota Azure.</span><span class="sxs-lookup"><span data-stu-id="ab3d7-137">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="ab3d7-138">Obsah dotazů a zpráv uživatele je v systému LUIS uchováván maximálně 30 dní, je šifrován a nepoužívá se pro školení ani zlepšení služeb.</span><span class="sxs-lookup"><span data-stu-id="ab3d7-138">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="ab3d7-139">Přečtěte si více o Cognitive Services  [zde](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span><span class="sxs-lookup"><span data-stu-id="ab3d7-139">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="ab3d7-140">Chcete-li spravovat nastavení administrátora pro aplikace v Microsoft Teams, přejděte do [centra pro správu Microsoft Teams](https://admin.teams.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="ab3d7-140">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span> 

## <a name="see-also"></a><span data-ttu-id="ab3d7-141">Viz také</span><span class="sxs-lookup"><span data-stu-id="ab3d7-141">See also</span></span> 

[<span data-ttu-id="ab3d7-142">Stažení a instalace aplikace Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="ab3d7-142">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="ab3d7-143">Centrum nápovědy Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="ab3d7-143">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="ab3d7-144">Správa žádostí o dovolenou v aplikaci Teams</span><span class="sxs-lookup"><span data-stu-id="ab3d7-144">Manage leave requests in Teams</span></span>](hr-teams-leave-app.md)

