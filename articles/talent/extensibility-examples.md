---
title: Rozšíření aplikace Talent pomocí PowerApps a Microsoft Flow - příkladové scénáře
description: Toto téma popisuje několik příkladů scénářů rozšíření pro aplikaci Microsoft Dynamics 365 for Talent používající Microsoft PowerApps a Microsoft Flow.
author: negudava
manager: Annbe
ms.date: 05/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: Dynamics 365 for Talent;PowerApps;Flow;Common Data Service
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent;Core;Experience Apps
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2019-03-04
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: c113b0f4ab2c8e44d00fcfca3f0a6ca828a854ae
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517502"
---
# <a name="extend-talent-by-using-powerapps-and-microsoft-flow---example-scenarios"></a><span data-ttu-id="8eb62-103">Rozšíření aplikace Talent pomocí PowerApps a Microsoft Flow - příkladové scénáře</span><span class="sxs-lookup"><span data-stu-id="8eb62-103">Extend Talent by using PowerApps and Microsoft Flow - Example scenarios</span></span>

<span data-ttu-id="8eb62-104">Toto téma popisuje několik příkladů scénářů rozšíření pro aplikaci Microsoft Dynamics 365 for Talent používající Microsoft PowerApps a Microsoft Flow.</span><span class="sxs-lookup"><span data-stu-id="8eb62-104">This topic describes some examples of extensibility scenarios for Microsoft Dynamics 365 for Talent that use Microsoft PowerApps and Microsoft Flow.</span></span> <span data-ttu-id="8eb62-105">Můžete importovat balíček řešení přidružený ke každému příkladu do prostředí PowerApps.</span><span class="sxs-lookup"><span data-stu-id="8eb62-105">You can import the solution package that is associated with each example into your PowerApps environment.</span></span> <span data-ttu-id="8eb62-106">Poté můžete tyto balíčky použít pokyny jako návod nebo jako počáteční body pro implementaci scénářů, které jsou použitelné pro vaši organizaci.</span><span class="sxs-lookup"><span data-stu-id="8eb62-106">You can then use the packages either as guidance or as starting points to implement scenarios that are applicable to your organization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8eb62-107">Pokud chcete používat šablony a aplikaci, které jsou popsány v tomto tématu „tak, jak jsou“, nezapomeňte je otestovat, abyste se ujistili, že pokrývají všechny scénáře, které jsou specifické pro vaši implementaci.</span><span class="sxs-lookup"><span data-stu-id="8eb62-107">If you want to use the templates and app that are described in this topic "as is," be sure to test them to make sure that they cover all the scenarios that are specific to your implementation.</span></span>


## <a name="prerequisites"></a><span data-ttu-id="8eb62-108">Předpoklady</span><span class="sxs-lookup"><span data-stu-id="8eb62-108">Prerequisites</span></span>

- <span data-ttu-id="8eb62-109">Pro import balíčků, musí mít uživatelé oprávnění **Tvůrce prostředí**.</span><span class="sxs-lookup"><span data-stu-id="8eb62-109">To import packages, users must have the **Environment Maker** permission.</span></span>
- <span data-ttu-id="8eb62-110">Pro export nebo import aplikací musí mít uživatelé licenci PowerApps Plan 2 nebo zkušební licenci PowerApps Plan 2.</span><span class="sxs-lookup"><span data-stu-id="8eb62-110">To export or import apps, users must have a PowerApps Plan 2 license or a PowerApps Plan 2 trial license.</span></span>

## <a name="flow--form-connect"></a><span data-ttu-id="8eb62-111">Tok – připojení k formuláři</span><span class="sxs-lookup"><span data-stu-id="8eb62-111">Flow – Form Connect</span></span>

<span data-ttu-id="8eb62-112">Šablonu **Tok – připojení k formuláři** lze použít ke čtení dat z Microsoft Forms a ukládat je do entity Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="8eb62-112">The **Flow – Form Connect** template can be used to read data from Microsoft Forms and store it in a Common Data Service entity.</span></span>

<span data-ttu-id="8eb62-113">Tuto šablonu lze rozšířit tak, aby ji bylo možné použít pro jiné scénáře.</span><span class="sxs-lookup"><span data-stu-id="8eb62-113">This template can be extended so that it can be used for other scenarios.</span></span> <span data-ttu-id="8eb62-114">Několik příkladů:</span><span class="sxs-lookup"><span data-stu-id="8eb62-114">Here are some examples:</span></span>

- <span data-ttu-id="8eb62-115">Zaznamenání hodnocení kandidáta.</span><span class="sxs-lookup"><span data-stu-id="8eb62-115">Capture candidate assessments.</span></span>
- <span data-ttu-id="8eb62-116">Zaznamenání výsledků z dotazníků kurzu.</span><span class="sxs-lookup"><span data-stu-id="8eb62-116">Capture results from course questionnaires.</span></span>
- <span data-ttu-id="8eb62-117">Kompilace knihovny otázek na pohovoru pro správce lidských zdrojů.</span><span class="sxs-lookup"><span data-stu-id="8eb62-117">Compile a library of interview questions for Human resources (HR) administrators.</span></span>
- <span data-ttu-id="8eb62-118">Zaznamenání hodnocení kandidáta z procesu pohovoru</span><span class="sxs-lookup"><span data-stu-id="8eb62-118">Capture a candidate's evaluation of the interview process</span></span>

<span data-ttu-id="8eb62-119">V aplikaci Microsoft Dynamics 365: Attract lze zobrazit formuláře na portálu kandidáta a kandidáti mohou vyplnit podrobnosti.</span><span class="sxs-lookup"><span data-stu-id="8eb62-119">In Microsoft Dynamics 365: Attract, forms can appear in Candidate portal, and candidates can fill in details.</span></span> <span data-ttu-id="8eb62-120">Formuláře lze také integrovat jako aktivity do šablony práce.</span><span class="sxs-lookup"><span data-stu-id="8eb62-120">Forms can also be embedded as activities in a job template.</span></span>

<span data-ttu-id="8eb62-121">Když kandidát odešle formulář, Microsoft Flow zaznamená odeslání formuláře, přečte data a uloží je do entity Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="8eb62-121">When a candidate submits a form, Microsoft Flow captures the form submission, reads the data, and stores it in the Common Data Service entity.</span></span>

<span data-ttu-id="8eb62-122">Chcete-li stáhnout šablonu **Flow – Form Connect** a strukturu vlastní entity, přejděte na [Flow – Form Connect](https://go.microsoft.com/fwlink/?linkid=2081988) v Microsoft Download Center.</span><span class="sxs-lookup"><span data-stu-id="8eb62-122">To download the **Flow – Form Connect** template and Custom Entity Structure, go to [Flow – Form Connect](https://go.microsoft.com/fwlink/?linkid=2081988) on the Microsoft Download Center.</span></span>

## <a name="initiate-and-extract-parameters-passed-to-powerapps"></a><span data-ttu-id="8eb62-123">Zahájení a extrakce parametrů předaných do Powerapps</span><span class="sxs-lookup"><span data-stu-id="8eb62-123">Initiate and Extract Parameters Passed to Powerapps</span></span>

<span data-ttu-id="8eb62-124">Šablonu **Zahájení a extrakce parametrů předaných do Powerapps** lze použít jako výchozí bod pro všechny scénáře PowerApps specifické pro aplikaci Attract.</span><span class="sxs-lookup"><span data-stu-id="8eb62-124">The **Initiate and Extract Parameters Passed to Powerapps** template can be used as a starting point for any PowerApps scenario that is specific to Attract.</span></span> <span data-ttu-id="8eb62-125">Obsahuje všechny výchozí parametry, které jsou předávány aplikací Attract, jako je například **Žádost o práci**, **ID kandidáta** a **ID práce**.</span><span class="sxs-lookup"><span data-stu-id="8eb62-125">It includes all the default parameters that are passed by Attract, such as **Job Application**, **Candidate ID**, and **JobID**.</span></span>

<span data-ttu-id="8eb62-126">Tato šablona může být použita k získání hodnotícího formuláře kandidáta, aby náborový manažer mohl zobrazit hodnocení, které kandidát vyplnil.</span><span class="sxs-lookup"><span data-stu-id="8eb62-126">This template can be used to retrieve a candidate assessment form, so that a hiring manager can view the assessment that a candidate filled in.</span></span>

<span data-ttu-id="8eb62-127">Aplikace, které jsou vytvořeny s použitím PowerApps lze vložit do šablony práce v aplikaci Attract.</span><span class="sxs-lookup"><span data-stu-id="8eb62-127">Apps that are created by using PowerApps can be embedded into the job template in Attract.</span></span>

<span data-ttu-id="8eb62-128">Chcete-li stáhnout šablonu **Zahájení a extrakce parametrů předaných do Powerapps** a strukturu vlastní entity, přejděte na [Zahájení a extrakce parametrů předaných do Powerapps](https://go.microsoft.com/fwlink/?linkid=2081991) v Microsoft Download Center.</span><span class="sxs-lookup"><span data-stu-id="8eb62-128">To download the **Initiate and Extract Parameters Passed to Powerapps** template and Custom Entity Structure, go to [Initiate and Extract Parameters Passed to Powerapps](https://go.microsoft.com/fwlink/?linkid=2081991) on the Microsoft Download Center.</span></span>

## <a name="integration-with-office-365"></a><span data-ttu-id="8eb62-129">Integrace s aplikací Office 365</span><span class="sxs-lookup"><span data-stu-id="8eb62-129">Integration with Office 365</span></span>

<span data-ttu-id="8eb62-130">Aplikaci **Integrace s Office 365** lze použít k extrakci informací o týmu pro přihlášené uživatele z Microsoft Office 365.</span><span class="sxs-lookup"><span data-stu-id="8eb62-130">The **Integration with Office 365** app can be used to extract team information for signed-in users from Microsoft Office 365.</span></span> <span data-ttu-id="8eb62-131">Odkazuje zaměstnance v aplikaci Talent na extrakci podrobností příchodu a odchodu a záznamy výjimek.</span><span class="sxs-lookup"><span data-stu-id="8eb62-131">It references workers in Talent to extract clock-in and clock-out details and exception recordings.</span></span> <span data-ttu-id="8eb62-132">Podrobnosti příchodu a odchodu jsou uloženy ve vlastních entitách Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="8eb62-132">Clock-in and Clock-out details are stored in custom Common Data Service entities.</span></span> <span data-ttu-id="8eb62-133">Předpokladem je, že tyto údaje jsou vyplňovány ze systémů třetích stran prostřednictvím integrace.</span><span class="sxs-lookup"><span data-stu-id="8eb62-133">The assumption is that these details are filled in from third-party systems via integration.</span></span>

<span data-ttu-id="8eb62-134">Tuto aplikaci lze rozšířit tak, aby ji bylo možné použít pro jiné scénáře.</span><span class="sxs-lookup"><span data-stu-id="8eb62-134">This app can be extended so that it can be used for other scenarios.</span></span> <span data-ttu-id="8eb62-135">Například ji lze použít pro zobrazení informací o dovolené týmu, událostech kalendáře a jakýchkoliv událostech specifických pro tým.</span><span class="sxs-lookup"><span data-stu-id="8eb62-135">For example, it can be used to show team vacation information, calendar events, and any team-specific events.</span></span>

<span data-ttu-id="8eb62-136">Chcete-li stáhnout aplikaci **Integrace s Office 365** a Strukturu entity zákazníka, přejděte na [Integrace s Office 365](https://go.microsoft.com/fwlink/?linkid=2081787) v Microsoft Download Center.</span><span class="sxs-lookup"><span data-stu-id="8eb62-136">To download the **Integration with Office 365** app and Custome Entity Structure, go to [Integration with Office 365](https://go.microsoft.com/fwlink/?linkid=2081787) on the Microsoft Download Center.</span></span>

## <a name="flow--email-notification"></a><span data-ttu-id="8eb62-137">Tok – E-mailové oznámení</span><span class="sxs-lookup"><span data-stu-id="8eb62-137">Flow – Email Notification</span></span>

<span data-ttu-id="8eb62-138">Šablonu **Tok – E-mailové oznámení** lze použít pro scénáře e-mailových oznámení.</span><span class="sxs-lookup"><span data-stu-id="8eb62-138">The **Flow – Email Notification** template can be used for email notification scenarios.</span></span> <span data-ttu-id="8eb62-139">Slouží ke spouštění e-mailových oznámení pro kandidáty, které náborový tým odmítl během jakékoliv fáze náborového procesu.</span><span class="sxs-lookup"><span data-stu-id="8eb62-139">It can be used to trigger notification emails to candidates that the hiring team rejects during any stage of the recruiting process.</span></span>

<span data-ttu-id="8eb62-140">Tuto šablonu můžete rozšířit ke sledování změn fáze kandidáta průběhu náborového procesu a k odesílání oznámení náborovému týmu a kandidátovi.</span><span class="sxs-lookup"><span data-stu-id="8eb62-140">This template can be extended to track changes to the candidate stage throughout the recruiting process, and to send notifications to the hiring team and candidate.</span></span>

<span data-ttu-id="8eb62-141">Obecně lze nastavit toky pro entity, které jsou uloženy v Common Data Service, pro odesílání oznámení pro události, které nastanou v aplikacích Core HR, Attract, nebo Dynamics 365 Talent: Onboard.</span><span class="sxs-lookup"><span data-stu-id="8eb62-141">In general, for entities that are stored in Common Data Service, flows can be set up to send notifications for events that occur in Core HR, Attract, or Dynamics 365 Talent: Onboard.</span></span>

<span data-ttu-id="8eb62-142">Chcete-li stáhnout šablonu **Tok – e-mailové oznámení**, přejděte na [Tok – e-mailové oznámení](https://go.microsoft.com/fwlink/?linkid=2082103) v Microsoft Download Center.</span><span class="sxs-lookup"><span data-stu-id="8eb62-142">To download the **Flow – Email Notification** template, go to [Flow – Email Notification](https://go.microsoft.com/fwlink/?linkid=2082103) on the Microsoft Download Center.</span></span>

## <a name="flow--sql-connect-and-execute"></a><span data-ttu-id="8eb62-143">Tok – připojení k SQL a provedení</span><span class="sxs-lookup"><span data-stu-id="8eb62-143">Flow – SQL Connect and execute</span></span>

<span data-ttu-id="8eb62-144">Šablona **Tok – připojení k SQL a provedení** se připojuje k serveru Microsoft SQL Server a povoluje spuštění SQL dotazů.</span><span class="sxs-lookup"><span data-stu-id="8eb62-144">The **Flow – SQL Connect and execute** template connects to Microsoft SQL Server and enables SQL queries to be run.</span></span>

<span data-ttu-id="8eb62-145">I když je tato šablona určena ke čtení a aktualizaci tabulek SQL, lze ji rozšířit tak, aby ji bylo možné použít pro jiné scénáře.</span><span class="sxs-lookup"><span data-stu-id="8eb62-145">Although this template is designed to read and update SQL tables, it can be extended so that it can be used for other scenarios.</span></span> <span data-ttu-id="8eb62-146">Například ji můžete použít k vyplnění tabulky fázování v Common Data Service záznamy z SQL Serveru a pravidelné synchronizaci tabulky fázování pomocí přírůstkového nabízení z SQL Serveru.</span><span class="sxs-lookup"><span data-stu-id="8eb62-146">For example, it can be used to fill a staging table in Common Data Service with records from SQL Server, and to periodically synchronize the staging table by using an incremental push from SQL Server.</span></span>

<span data-ttu-id="8eb62-147">Chcete-li stáhnout šablonu **Tok – připojení k SQL a provedení**, přejděte na [Tok – připojení k SQL a provedení](https://go.microsoft.com/fwlink/?linkid=2081789) v Microsoft Download Center.</span><span class="sxs-lookup"><span data-stu-id="8eb62-147">To download the **Flow – SQL Connect and execute** template, go to [Flow – SQL Connect and execute](https://go.microsoft.com/fwlink/?linkid=2081789) on the Microsoft Download Center.</span></span>

## <a name="flow--sharepoint-integration"></a><span data-ttu-id="8eb62-148">Tok - Integrace SharePoint</span><span class="sxs-lookup"><span data-stu-id="8eb62-148">Flow – SharePoint Integration</span></span>

<span data-ttu-id="8eb62-149">Šablonu **Tok – Integrace SharePoint** lze použít ke čtení dat ze seznamu aplikace Microsoft SharePoint, porovnání seznamu s hodnotami polí pro všechny entity Common Data Service a odesílání výsledků porovnání e-mailovým oznámením.</span><span class="sxs-lookup"><span data-stu-id="8eb62-149">The **Flow – SharePoint Integration** template can be used to read data from a Microsoft SharePoint list, compare the list with field values for any Common Data Service entity, and send the results of the comparison as a notification email.</span></span> 

<span data-ttu-id="8eb62-150">Organizace může míst sadu dovedností, které naléhavě vyžaduje.</span><span class="sxs-lookup"><span data-stu-id="8eb62-150">An organization might have a set of skills that it urgently requires.</span></span> <span data-ttu-id="8eb62-151">Tyto dovednosti mohou být uloženy v aplikaci SharePoint jako seznam SharePoint.</span><span class="sxs-lookup"><span data-stu-id="8eb62-151">These skills can be stored in SharePoint as a SharePoint list.</span></span> <span data-ttu-id="8eb62-152">Když kandidát požádá o práci, u které je uvedena sada požadovaných dovedností, dojde k odeslání e-mailového oznámení, pokud existuje významná shoda mezi dovednostmi kandidáta, a dovednostmi, které jsou uloženy v aplikaci SharePoint.</span><span class="sxs-lookup"><span data-stu-id="8eb62-152">When a candidate applies for any job that a set of required skills is listed for, if there is a significant match between the candidate's skill and the skills that are stored in SharePoint, a notification email is sent.</span></span> <span data-ttu-id="8eb62-153">Tímto způsobem se obsadí naléhavě požadované pozice rychleji, protože oznámení pomáhají náborovým pracovníkům kontaktovat a interně najmout kandidáty v rámci organizace.</span><span class="sxs-lookup"><span data-stu-id="8eb62-153">In this way, positions that are urgently required are filled faster, because the notifications help recruiters reach out and cross-hire candidates throughout the organization.</span></span>

<span data-ttu-id="8eb62-154">Tuto šablonu lze rozšířit, aby ji bylo možné použít pro všechny scénáře, které zahrnují integraci SharePoint.</span><span class="sxs-lookup"><span data-stu-id="8eb62-154">This template can be extended so that it can be used for any scenario that involves SharePoint integration.</span></span>

<span data-ttu-id="8eb62-155">Chcete-li stáhnout šablonu **Tok - Integrace SharePoint**, přejděte na [Tok - Integrace SharePoint](https://go.microsoft.com/fwlink/?linkid=2082109) v Microsoft Download Center.</span><span class="sxs-lookup"><span data-stu-id="8eb62-155">To download the **Flow – SharePoint Integration** template, go to [Flow – SharePoint Integration](https://go.microsoft.com/fwlink/?linkid=2082109) on the Microsoft Download Center.</span></span>

## <a name="admin-console-to-manage-talent-pools"></a><span data-ttu-id="8eb62-156">Konzola správce pro správu skupin talentů</span><span class="sxs-lookup"><span data-stu-id="8eb62-156">Admin console to manage talent pools</span></span>

<span data-ttu-id="8eb62-157">Když povolíte integraci se službou LinkedIn, Attract automaticky vytvoří skupinu talentů LinkedIn.</span><span class="sxs-lookup"><span data-stu-id="8eb62-157">When you enable integration with LinkedIn, Attract automatically createas a LinkedIn talent pool.</span></span> <span data-ttu-id="8eb62-158">Když náborový pracovník vymění InMail za nábor prostřednictvím služby LinkedIn, Attract vytvoří profil a nábor se stane členem skupiny talentu LinkedIn.</span><span class="sxs-lookup"><span data-stu-id="8eb62-158">When a recruiter exchanges InMail with a recruit through LinkedIn, Attract creates a profile for the recruit, and the recruit becomes a member of the LinkedIn talent pool.</span></span> <span data-ttu-id="8eb62-159">Tato aplikace PowerApps je užitečná pro reorganizaci kandidátů ve skupinách talentů na základě dovedností.</span><span class="sxs-lookup"><span data-stu-id="8eb62-159">This PowerApps app is useful for reorganizing candidates in talent pools based on skill.</span></span>

<span data-ttu-id="8eb62-160">Spusťte tuto aplikaci PowerApps jako konzolu správce, která provede následující úkoly:</span><span class="sxs-lookup"><span data-stu-id="8eb62-160">Run this PowerApps app as an admin console to perform the following tasks:</span></span>

- <span data-ttu-id="8eb62-161">Uvede seznam kandidátů ve skupině talentů</span><span class="sxs-lookup"><span data-stu-id="8eb62-161">List candidates in a talent pool</span></span>
- <span data-ttu-id="8eb62-162">Přidá a odstraní kandidáty ze skupiny talentů</span><span class="sxs-lookup"><span data-stu-id="8eb62-162">Add and remove candidates from a talent pool</span></span>
- <span data-ttu-id="8eb62-163">Přesune kandidáty z jedné skupiny talentů do druhé</span><span class="sxs-lookup"><span data-stu-id="8eb62-163">Move candidates from one talent pool to another</span></span>
- <span data-ttu-id="8eb62-164">Určí, zda kandidáti jsou již součástí skupiny talentů před jejich přesunutím</span><span class="sxs-lookup"><span data-stu-id="8eb62-164">Determine whether candidates are already part of a talent pool before moving them</span></span>
- <span data-ttu-id="8eb62-165">Ověří dovednosti kandidátů před jejich přesunutím do jiných skupin talentů</span><span class="sxs-lookup"><span data-stu-id="8eb62-165">Check the skills of candidates before moving them to other talent pools</span></span>

<span data-ttu-id="8eb62-166">Tato aplikace PowerApps používá vztahy N:N, takže ji můžete použít jako šablonu pro jiné scénáře, kde potřebujete extrahovat záznamy, které mají vztahy N:N.</span><span class="sxs-lookup"><span data-stu-id="8eb62-166">This PowerApps app uses many-to-many relationships, so you can use it as a template for other scenarios where you need to extract records that have many-to-many relationships.</span></span>

<span data-ttu-id="8eb62-167">Chcete-li stáhnout šablonu **Konzola správce pro správu skupin talentů**, přejděte na [Konzola správce pro správu skupin talentů](http://www.microsoft.com/downloads/details.aspx?FamilyID=780a5eee-0e2a-4159-9a83-009f9ccdc469) v Microsoft Download Center.</span><span class="sxs-lookup"><span data-stu-id="8eb62-167">To download the **Admin console to manage talent pools** template,  go to [Admin console to manage talent pools](http://www.microsoft.com/downloads/details.aspx?FamilyID=780a5eee-0e2a-4159-9a83-009f9ccdc469) on the Microsoft Download Center.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8eb62-168">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="8eb62-168">Additional resources</span></span>

[<span data-ttu-id="8eb62-169">Microsoft Power Platform</span><span class="sxs-lookup"><span data-stu-id="8eb62-169">The Microsoft Power Platform</span></span>](https://docs.microsoft.com/power-platform/admin/admin-documentation)

[<span data-ttu-id="8eb62-170">Migrace aplikace mezi klienty a prostředími</span><span class="sxs-lookup"><span data-stu-id="8eb62-170">Migrate app between tenants and environments</span></span>](https://docs.microsoft.com/en-us/power-platform/admin/environment-and-tenant-migration)
