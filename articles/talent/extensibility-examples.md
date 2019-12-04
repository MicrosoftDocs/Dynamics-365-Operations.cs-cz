---
title: Rozšíření aplikace Talent o Power Apps a Power Automate
description: Toto téma popisuje několik příkladů scénářů rozšíření pro aplikaci Microsoft Dynamics 365 Talent používající Microsoft Power Apps a Microsoft Power Automate.
author: negudava
manager: Annbe
ms.date: 05/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: Dynamics 365 Talent;PowerApps;Flow;Common Data Service
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
ms.openlocfilehash: 3bb61297e294aa3f2d06f542bebe29d7afae9c3b
ms.sourcegitcommit: 9cc6a011bfdd1b0fe505760b6bf429eb6c65862a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/25/2019
ms.locfileid: "2832831"
---
# <a name="extend-talent-with-power-apps-and-power-automate"></a><span data-ttu-id="36925-103">Rozšíření aplikace Talent o Power Apps a Power Automate</span><span class="sxs-lookup"><span data-stu-id="36925-103">Extend Talent with Power Apps and Power Automate</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="36925-104">Toto téma popisuje několik příkladů scénářů rozšíření pro aplikaci Microsoft Dynamics 365 Talent používající Microsoft Power Apps a Microsoft Power Automate.</span><span class="sxs-lookup"><span data-stu-id="36925-104">This topic describes some examples of extensibility scenarios for Microsoft Dynamics 365 Talent that use Microsoft Power Apps and Microsoft Power Automate.</span></span> <span data-ttu-id="36925-105">Můžete importovat balíček řešení přidružený ke každému příkladu do prostředí Power Apps.</span><span class="sxs-lookup"><span data-stu-id="36925-105">You can import the solution package that is associated with each example into your Power Apps environment.</span></span> <span data-ttu-id="36925-106">Poté můžete tyto balíčky použít pokyny jako návod nebo jako počáteční body pro implementaci scénářů, které jsou použitelné pro vaši organizaci.</span><span class="sxs-lookup"><span data-stu-id="36925-106">You can then use the packages either as guidance or as starting points to implement scenarios that are applicable to your organization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="36925-107">Pokud chcete používat šablony a aplikaci, které jsou popsány v tomto tématu „tak, jak jsou“, nezapomeňte je otestovat, abyste se ujistili, že pokrývají všechny scénáře, které jsou specifické pro vaši implementaci.</span><span class="sxs-lookup"><span data-stu-id="36925-107">If you want to use the templates and app that are described in this topic "as is," be sure to test them to make sure that they cover all the scenarios that are specific to your implementation.</span></span>


## <a name="prerequisites"></a><span data-ttu-id="36925-108">Předpoklady</span><span class="sxs-lookup"><span data-stu-id="36925-108">Prerequisites</span></span>

- <span data-ttu-id="36925-109">Pro import balíčků, musí mít uživatelé oprávnění **Tvůrce prostředí**.</span><span class="sxs-lookup"><span data-stu-id="36925-109">To import packages, users must have the **Environment Maker** permission.</span></span>
- <span data-ttu-id="36925-110">Pro export nebo import aplikací musí mít uživatelé licenci Power Apps Plan 2 nebo zkušební licenci Power Apps Plan 2.</span><span class="sxs-lookup"><span data-stu-id="36925-110">To export or import apps, users must have a Power Apps Plan 2 license or a Power Apps Plan 2 trial license.</span></span>

## <a name="power-automate--form-connect"></a><span data-ttu-id="36925-111">Power Automate – připojení k formuláři</span><span class="sxs-lookup"><span data-stu-id="36925-111">Power Automate – Form Connect</span></span>

<span data-ttu-id="36925-112">Šablonu **Power Automate – připojení k formuláři** lze použít ke čtení dat z Microsoft Forms a ukládat je do entity Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="36925-112">The **Power Automate – Form Connect** template can be used to read data from Microsoft Forms and store it in a Common Data Service entity.</span></span>

<span data-ttu-id="36925-113">Tuto šablonu lze rozšířit tak, aby ji bylo možné použít pro jiné scénáře.</span><span class="sxs-lookup"><span data-stu-id="36925-113">This template can be extended so that it can be used for other scenarios.</span></span> <span data-ttu-id="36925-114">Několik příkladů:</span><span class="sxs-lookup"><span data-stu-id="36925-114">Here are some examples:</span></span>

- <span data-ttu-id="36925-115">Zaznamenání hodnocení kandidáta.</span><span class="sxs-lookup"><span data-stu-id="36925-115">Capture candidate assessments.</span></span>
- <span data-ttu-id="36925-116">Zaznamenání výsledků z dotazníků kurzu.</span><span class="sxs-lookup"><span data-stu-id="36925-116">Capture results from course questionnaires.</span></span>
- <span data-ttu-id="36925-117">Kompilace knihovny otázek na pohovoru pro správce lidských zdrojů.</span><span class="sxs-lookup"><span data-stu-id="36925-117">Compile a library of interview questions for Human resources (HR) administrators.</span></span>
- <span data-ttu-id="36925-118">Zaznamenání hodnocení kandidáta z procesu pohovoru</span><span class="sxs-lookup"><span data-stu-id="36925-118">Capture a candidate's evaluation of the interview process</span></span>

<span data-ttu-id="36925-119">V aplikaci Microsoft Dynamics 365: Attract lze zobrazit formuláře na portálu kandidáta a kandidáti mohou vyplnit podrobnosti.</span><span class="sxs-lookup"><span data-stu-id="36925-119">In Microsoft Dynamics 365: Attract, forms can appear in Candidate portal, and candidates can fill in details.</span></span> <span data-ttu-id="36925-120">Formuláře lze také integrovat jako aktivity do šablony práce.</span><span class="sxs-lookup"><span data-stu-id="36925-120">Forms can also be embedded as activities in a job template.</span></span>

<span data-ttu-id="36925-121">Když kandidát odešle formulář, Microsoft Power Automate zaznamená odeslání formuláře, přečte data a uloží je do entity Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="36925-121">When a candidate submits a form, Microsoft Power Automate captures the form submission, reads the data, and stores it in the Common Data Service entity.</span></span>

<span data-ttu-id="36925-122">Chcete-li stáhnout šablonu **Power Automate – připojení k formuláři** a Struktur vlastní entity, přejděte na [Power Automate – připojení k formuláři](https://go.microsoft.com/fwlink/?linkid=2081988) v Microsoft Download Center.</span><span class="sxs-lookup"><span data-stu-id="36925-122">To download the **Power Automate – Form Connect** template and Custom Entity Structure, go to [Power Automate – Form Connect](https://go.microsoft.com/fwlink/?linkid=2081988) on the Microsoft Download Center.</span></span>

## <a name="initiate-and-extract-parameters-passed-to-power-apps"></a><span data-ttu-id="36925-123">Zahájení a extrakce parametrů předaných do Power Apps</span><span class="sxs-lookup"><span data-stu-id="36925-123">Initiate and Extract Parameters Passed to Power Apps</span></span>

<span data-ttu-id="36925-124">Šablonu **Zahájení a extrakce parametrů předaných do Power Apps** lze použít jako výchozí bod pro všechny scénáře Power Apps specifické pro aplikaci Attract.</span><span class="sxs-lookup"><span data-stu-id="36925-124">The **Initiate and Extract Parameters Passed to Power Apps** template can be used as a starting point for any Power Apps scenario that is specific to Attract.</span></span> <span data-ttu-id="36925-125">Obsahuje všechny výchozí parametry, které jsou předávány aplikací Attract, jako je například **Žádost o práci**, **ID kandidáta** a **ID práce**.</span><span class="sxs-lookup"><span data-stu-id="36925-125">It includes all the default parameters that are passed by Attract, such as **Job Application**, **Candidate ID**, and **JobID**.</span></span>

<span data-ttu-id="36925-126">Tato šablona může být použita k získání hodnotícího formuláře kandidáta, aby náborový manažer mohl zobrazit hodnocení, které kandidát vyplnil.</span><span class="sxs-lookup"><span data-stu-id="36925-126">This template can be used to retrieve a candidate assessment form, so that a hiring manager can view the assessment that a candidate filled in.</span></span>

<span data-ttu-id="36925-127">Aplikace, které jsou vytvořeny s použitím Power Apps lze vložit do šablony práce v aplikaci Attract.</span><span class="sxs-lookup"><span data-stu-id="36925-127">Apps that are created by using Power Apps can be embedded into the job template in Attract.</span></span>

<span data-ttu-id="36925-128">Chcete-li stáhnout šablonu **Zahájení a extrakce parametrů předaných do Power Apps** strukturu vlastní entity, přejděte na [Zahájení a extrakce parametrů předaných do Power Apps](https://go.microsoft.com/fwlink/?linkid=2081991) v Microsoft Download Center.</span><span class="sxs-lookup"><span data-stu-id="36925-128">To download the **Initiate and Extract Parameters Passed to Power Apps** template and Custom Entity Structure, go to [Initiate and Extract Parameters Passed to Power Apps](https://go.microsoft.com/fwlink/?linkid=2081991) on the Microsoft Download Center.</span></span>

## <a name="integration-with-office-365"></a><span data-ttu-id="36925-129">Integrace s aplikací Office 365</span><span class="sxs-lookup"><span data-stu-id="36925-129">Integration with Office 365</span></span>

<span data-ttu-id="36925-130">Aplikaci **Integrace s Office 365** lze použít k extrakci informací o týmu pro přihlášené uživatele z Microsoft Office 365.</span><span class="sxs-lookup"><span data-stu-id="36925-130">The **Integration with Office 365** app can be used to extract team information for signed-in users from Microsoft Office 365.</span></span> <span data-ttu-id="36925-131">Odkazuje zaměstnance v aplikaci Talent na extrakci podrobností příchodu a odchodu a záznamy výjimek.</span><span class="sxs-lookup"><span data-stu-id="36925-131">It references workers in Talent to extract clock-in and clock-out details and exception recordings.</span></span> <span data-ttu-id="36925-132">Podrobnosti příchodu a odchodu jsou uloženy ve vlastních entitách Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="36925-132">Clock-in and Clock-out details are stored in custom Common Data Service entities.</span></span> <span data-ttu-id="36925-133">Předpokladem je, že tyto údaje jsou vyplňovány ze systémů třetích stran prostřednictvím integrace.</span><span class="sxs-lookup"><span data-stu-id="36925-133">The assumption is that these details are filled in from third-party systems via integration.</span></span>

<span data-ttu-id="36925-134">Tuto aplikaci lze rozšířit tak, aby ji bylo možné použít pro jiné scénáře.</span><span class="sxs-lookup"><span data-stu-id="36925-134">This app can be extended so that it can be used for other scenarios.</span></span> <span data-ttu-id="36925-135">Například ji lze použít pro zobrazení informací o dovolené týmu, událostech kalendáře a jakýchkoliv událostech specifických pro tým.</span><span class="sxs-lookup"><span data-stu-id="36925-135">For example, it can be used to show team vacation information, calendar events, and any team-specific events.</span></span>

<span data-ttu-id="36925-136">Chcete-li stáhnout aplikaci **Integrace s Office 365** a Strukturu entity zákazníka, přejděte na [Integrace s Office 365](https://go.microsoft.com/fwlink/?linkid=2081787) v Microsoft Download Center.</span><span class="sxs-lookup"><span data-stu-id="36925-136">To download the **Integration with Office 365** app and Custome Entity Structure, go to [Integration with Office 365](https://go.microsoft.com/fwlink/?linkid=2081787) on the Microsoft Download Center.</span></span>

## <a name="power-automate--email-notification"></a><span data-ttu-id="36925-137">Power Automate - mailové oznámení</span><span class="sxs-lookup"><span data-stu-id="36925-137">Power Automate – Email Notification</span></span>

<span data-ttu-id="36925-138">Šablonu **Power Automate – E-mailové oznámení** lze použít pro scénáře e-mailových oznámení.</span><span class="sxs-lookup"><span data-stu-id="36925-138">The **Power Automate – Email Notification** template can be used for email notification scenarios.</span></span> <span data-ttu-id="36925-139">Slouží ke spouštění e-mailových oznámení pro kandidáty, které náborový tým odmítl během jakékoliv fáze náborového procesu.</span><span class="sxs-lookup"><span data-stu-id="36925-139">It can be used to trigger notification emails to candidates that the hiring team rejects during any stage of the recruiting process.</span></span>

<span data-ttu-id="36925-140">Tuto šablonu můžete rozšířit ke sledování změn fáze kandidáta průběhu náborového procesu a k odesílání oznámení náborovému týmu a kandidátovi.</span><span class="sxs-lookup"><span data-stu-id="36925-140">This template can be extended to track changes to the candidate stage throughout the recruiting process, and to send notifications to the hiring team and candidate.</span></span>

<span data-ttu-id="36925-141">Obecně lze nastavit toky pro entity, které jsou uloženy v Common Data Service, pro odesílání oznámení pro události, které nastanou v aplikacích Core HR, Attract, nebo Onboard.</span><span class="sxs-lookup"><span data-stu-id="36925-141">In general, for entities that are stored in Common Data Service, flows can be set up to send notifications for events that occur in Core HR, Attract, or Onboard.</span></span>

<span data-ttu-id="36925-142">Chcete-li stáhnout šablonu **Power Automate – e-mailové oznámení**, přejděte na [Power Automate – e-mailové oznámení](https://go.microsoft.com/fwlink/?linkid=2082103) v Microsoft Download Center.</span><span class="sxs-lookup"><span data-stu-id="36925-142">To download the **Power Automate – Email Notification** template, go to [Power Automate – Email Notification](https://go.microsoft.com/fwlink/?linkid=2082103) on the Microsoft Download Center.</span></span>

## <a name="power-automate--sql-connect-and-execute"></a><span data-ttu-id="36925-143">Power Automate – připojení k SQL a provedení</span><span class="sxs-lookup"><span data-stu-id="36925-143">Power Automate – SQL Connect and execute</span></span>

<span data-ttu-id="36925-144">Šablona **Power Automate – připojení k SQL a provedení** se připojuje k serveru Microsoft SQL Server a povoluje spuštění SQL dotazů.</span><span class="sxs-lookup"><span data-stu-id="36925-144">The **Power Automate – SQL Connect and execute** template connects to Microsoft SQL Server and enables SQL queries to be run.</span></span>

<span data-ttu-id="36925-145">I když je tato šablona určena ke čtení a aktualizaci tabulek SQL, lze ji rozšířit tak, aby ji bylo možné použít pro jiné scénáře.</span><span class="sxs-lookup"><span data-stu-id="36925-145">Although this template is designed to read and update SQL tables, it can be extended so that it can be used for other scenarios.</span></span> <span data-ttu-id="36925-146">Například ji můžete použít k vyplnění tabulky fázování v Common Data Service záznamy z SQL Serveru a pravidelné synchronizaci tabulky fázování pomocí přírůstkového nabízení z SQL Serveru.</span><span class="sxs-lookup"><span data-stu-id="36925-146">For example, it can be used to fill a staging table in Common Data Service with records from SQL Server, and to periodically synchronize the staging table by using an incremental push from SQL Server.</span></span>

<span data-ttu-id="36925-147">Chcete-li stáhnout šablonu **Power Automate – připojení k SQL a provedení**, přejděte na [Power Automate – připojení k SQL a provedení](https://go.microsoft.com/fwlink/?linkid=2081789) v Microsoft Download Center.</span><span class="sxs-lookup"><span data-stu-id="36925-147">To download the **Power Automate – SQL Connect and execute** template, go to [Power Automate – SQL Connect and execute](https://go.microsoft.com/fwlink/?linkid=2081789) on the Microsoft Download Center.</span></span>

## <a name="power-automate--sharepoint-integration"></a><span data-ttu-id="36925-148">Power Automate – integrace se službou SharePoint</span><span class="sxs-lookup"><span data-stu-id="36925-148">Power Automate – SharePoint Integration</span></span>

<span data-ttu-id="36925-149">Šablonu **Power Automate – Integrace SharePoint** lze použít ke čtení dat ze seznamu aplikace Microsoft SharePoint porovnání seznamu s hodnotami polí pro všechny entity Common Data Service a odesílání výsledků porovnání e-mailovým oznámením.</span><span class="sxs-lookup"><span data-stu-id="36925-149">The **Power Automate – SharePoint Integration** template can be used to read data from a Microsoft SharePoint list, compare the list with field values for any Common Data Service entity, and send the results of the comparison as a notification email.</span></span> 

<span data-ttu-id="36925-150">Organizace může míst sadu dovedností, které naléhavě vyžaduje.</span><span class="sxs-lookup"><span data-stu-id="36925-150">An organization might have a set of skills that it urgently requires.</span></span> <span data-ttu-id="36925-151">Tyto dovednosti mohou být uloženy v aplikaci SharePoint jako seznam SharePoint.</span><span class="sxs-lookup"><span data-stu-id="36925-151">These skills can be stored in SharePoint as a SharePoint list.</span></span> <span data-ttu-id="36925-152">Když kandidát požádá o práci, u které je uvedena sada požadovaných dovedností, dojde k odeslání e-mailového oznámení, pokud existuje významná shoda mezi dovednostmi kandidáta, a dovednostmi, které jsou uloženy v aplikaci SharePoint.</span><span class="sxs-lookup"><span data-stu-id="36925-152">When a candidate applies for any job that a set of required skills is listed for, if there is a significant match between the candidate's skill and the skills that are stored in SharePoint, a notification email is sent.</span></span> <span data-ttu-id="36925-153">Tímto způsobem se obsadí naléhavě požadované pozice rychleji, protože oznámení pomáhají náborovým pracovníkům kontaktovat a interně najmout kandidáty v rámci organizace.</span><span class="sxs-lookup"><span data-stu-id="36925-153">In this way, positions that are urgently required are filled faster, because the notifications help recruiters reach out and cross-hire candidates throughout the organization.</span></span>

<span data-ttu-id="36925-154">Tuto šablonu lze rozšířit, aby ji bylo možné použít pro všechny scénáře, které zahrnují integraci SharePoint.</span><span class="sxs-lookup"><span data-stu-id="36925-154">This template can be extended so that it can be used for any scenario that involves SharePoint integration.</span></span>

<span data-ttu-id="36925-155">Chcete-li stáhnout šablonu **Power Automate – Integrace SharePoint**, přejděte na [Power Automate – Integrace SharePoint](https://go.microsoft.com/fwlink/?linkid=2082109) v Microsoft Download Center.</span><span class="sxs-lookup"><span data-stu-id="36925-155">To download the **Power Automate – SharePoint Integration** template, go to [Power Automate – SharePoint Integration](https://go.microsoft.com/fwlink/?linkid=2082109) on the Microsoft Download Center.</span></span>

## <a name="referral-app"></a><span data-ttu-id="36925-156">Referenční aplikace</span><span class="sxs-lookup"><span data-stu-id="36925-156">Referral App</span></span>
<span data-ttu-id="36925-157">Pomocí Referenční aplikace můžete přidat kandidáty do sdílené skupiny talentů.</span><span class="sxs-lookup"><span data-stu-id="36925-157">You can use the Referral App to add candidates to a shared talent pool.</span></span> <span data-ttu-id="36925-158">Poskytovatel reference může zadat **Křestní jméno**, **Příjmení**, **E-mail** a **Adresa URL LinkedIn** při odesílání uchazeče.</span><span class="sxs-lookup"><span data-stu-id="36925-158">The referrer can enter **Firstname**, **Lastname**, **Email**, and **Linkedln URL** when submitting a candidate.</span></span> <span data-ttu-id="36925-159">Zdrojová metadata kandidáta jsou poté naplněna informacemi o poskytovateli reference.</span><span class="sxs-lookup"><span data-stu-id="36925-159">The candidate source metadata is then populated with the referrer’s information.</span></span>

<span data-ttu-id="36925-160">Tuto aplikaci můžete vložit do samoobsluhy zaměstnanců (ESS) pro odesílání poskytovatelů reference nebo ji můžete použít jako hypertextový odkaz na podnikovém portálu a spustit jako samostatnou aplikaci.</span><span class="sxs-lookup"><span data-stu-id="36925-160">You can embed this app in Employee self-service (ESS) for submitting referrals, or you can be use it as a hyperlink in the Corporate Portal and run as a stand-alone app.</span></span>

<span data-ttu-id="36925-161">Chcete-li stáhnout **Referenční aplikaci**, přejděte na [Řešení rozšiřitelnosti Dynamics 365 Talent: Referenční aplikace](http://www.microsoft.com/downloads/details.aspx?FamilyID=9a59c9d1-f8a1-4d4d-b768-cfc4f4eb9d0d) na webu Microsoft Download Center.</span><span class="sxs-lookup"><span data-stu-id="36925-161">To download **Referral App**, go to [Dynamics 365 Talent extensibility solution: Referral App](http://www.microsoft.com/downloads/details.aspx?FamilyID=9a59c9d1-f8a1-4d4d-b768-cfc4f4eb9d0d) on the Microsoft Download Center.</span></span> <span data-ttu-id="36925-162">Chcete-li přidat další funkce, můžete tuto aplikaci importovat a přizpůsobit ji.</span><span class="sxs-lookup"><span data-stu-id="36925-162">You can import this app and customize it to add additional functionality.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="36925-163">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="36925-163">Additional resources</span></span>

[<span data-ttu-id="36925-164">Microsoft Power Platform</span><span class="sxs-lookup"><span data-stu-id="36925-164">The Microsoft Power Platform</span></span>](https://docs.microsoft.com/power-platform/admin/admin-documentation)

[<span data-ttu-id="36925-165">Migrace aplikace mezi klienty a prostředími</span><span class="sxs-lookup"><span data-stu-id="36925-165">Migrate app between tenants and environments</span></span>](https://docs.microsoft.com/power-platform/admin/environment-and-tenant-migration)
