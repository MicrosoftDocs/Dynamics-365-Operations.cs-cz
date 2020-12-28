---
title: Rozšíření aplikace Talent o Power Apps a Power Automate
description: Tento článek popisuje několik příkladů scénářů rozšíření pro aplikaci Microsoft Dynamics 365 Talent - Attract používající Microsoft Power Apps a Microsoft Power Automate.
author: negudava
manager: Annbe
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent;Core;Experience Apps
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: cfdf36e9486aa4853d3bf674afa73ec3a4d1c161
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529627"
---
# <a name="extend-talent-with-power-apps-and-power-automate"></a><span data-ttu-id="9869f-103">Rozšíření aplikace Talent o Power Apps a Power Automate</span><span class="sxs-lookup"><span data-stu-id="9869f-103">Extend Talent with Power Apps and Power Automate</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="9869f-104">Tento článek popisuje několik příkladů scénářů rozšíření pro aplikaci Microsoft Dynamics 365 Talent: Attract používající Microsoft Power Apps a Microsoft Power Automate.</span><span class="sxs-lookup"><span data-stu-id="9869f-104">This article describes some examples of extensibility scenarios for Microsoft Dynamics 365 Talent: Attract that use Microsoft Power Apps and Microsoft Power Automate.</span></span> <span data-ttu-id="9869f-105">Můžete importovat balíček řešení přidružený ke každému příkladu do prostředí Power Apps.</span><span class="sxs-lookup"><span data-stu-id="9869f-105">You can import the solution package that is associated with each example into your Power Apps environment.</span></span> <span data-ttu-id="9869f-106">Poté můžete tyto balíčky použít pokyny jako návod nebo jako počáteční body pro implementaci scénářů, které jsou použitelné pro vaši organizaci.</span><span class="sxs-lookup"><span data-stu-id="9869f-106">You can then use the packages either as guidance or as starting points to implement scenarios that are applicable to your organization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9869f-107">Pokud chcete používat šablony a aplikaci, které jsou popsány v tomto článku „tak, jak jsou“, nezapomeňte je otestovat, abyste se ujistili, že pokrývají všechny scénáře, které jsou specifické pro vaši implementaci.</span><span class="sxs-lookup"><span data-stu-id="9869f-107">If you want to use the templates and app that are described in this article "as is," be sure to test them to make sure that they cover all the scenarios that are specific to your implementation.</span></span>


## <a name="prerequisites"></a><span data-ttu-id="9869f-108">Předpoklady</span><span class="sxs-lookup"><span data-stu-id="9869f-108">Prerequisites</span></span>

- <span data-ttu-id="9869f-109">Pro import balíčků, musí mít uživatelé oprávnění **Tvůrce prostředí**.</span><span class="sxs-lookup"><span data-stu-id="9869f-109">To import packages, users must have the **Environment Maker** permission.</span></span>
- <span data-ttu-id="9869f-110">Pro export nebo import aplikací musí mít uživatelé licenci Power Apps Plan 2 nebo zkušební licenci Power Apps Plan 2.</span><span class="sxs-lookup"><span data-stu-id="9869f-110">To export or import apps, users must have a Power Apps Plan 2 license or a Power Apps Plan 2 trial license.</span></span>

## <a name="power-automate--form-connect"></a><span data-ttu-id="9869f-111">Power Automate – připojení k formuláři</span><span class="sxs-lookup"><span data-stu-id="9869f-111">Power Automate – Form Connect</span></span>

<span data-ttu-id="9869f-112">Šablonu **Power Automate – připojení k formuláři** lze použít ke čtení dat z Microsoft Forms a ukládat je do entity Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="9869f-112">The **Power Automate – Form Connect** template can be used to read data from Microsoft Forms and store it in a Common Data Service entity.</span></span>

<span data-ttu-id="9869f-113">Tuto šablonu lze rozšířit tak, aby ji bylo možné použít pro jiné scénáře.</span><span class="sxs-lookup"><span data-stu-id="9869f-113">This template can be extended so that it can be used for other scenarios.</span></span> <span data-ttu-id="9869f-114">Několik příkladů:</span><span class="sxs-lookup"><span data-stu-id="9869f-114">Here are some examples:</span></span>

- <span data-ttu-id="9869f-115">Zaznamenání hodnocení kandidáta.</span><span class="sxs-lookup"><span data-stu-id="9869f-115">Capture candidate assessments.</span></span>
- <span data-ttu-id="9869f-116">Zaznamenání výsledků z dotazníků kurzu.</span><span class="sxs-lookup"><span data-stu-id="9869f-116">Capture results from course questionnaires.</span></span>
- <span data-ttu-id="9869f-117">Kompilace knihovny otázek na pohovoru pro správce lidských zdrojů.</span><span class="sxs-lookup"><span data-stu-id="9869f-117">Compile a library of interview questions for Human resources (HR) administrators.</span></span>
- <span data-ttu-id="9869f-118">Zaznamenání hodnocení kandidáta z procesu pohovoru</span><span class="sxs-lookup"><span data-stu-id="9869f-118">Capture a candidate's evaluation of the interview process</span></span>

<span data-ttu-id="9869f-119">V aplikaci Microsoft Dynamics 365: Attract můžete použít formuláře na portálu kandidáta, kde kandidáti vyplňují své detaily.</span><span class="sxs-lookup"><span data-stu-id="9869f-119">In Microsoft Dynamics 365: Attract, you can use forms in the candidate portal, where candidates fill in details.</span></span> <span data-ttu-id="9869f-120">Formuláře lze také integrovat jako aktivity do šablony práce.</span><span class="sxs-lookup"><span data-stu-id="9869f-120">You can also embed forms as activities in a job template.</span></span>

<span data-ttu-id="9869f-121">Když kandidát odešle formulář, Microsoft Power Automate zaznamená odeslání formuláře, přečte data a uloží je do entity Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="9869f-121">When a candidate submits a form, Microsoft Power Automate captures the form submission, reads the data, and stores it in the Common Data Service entity.</span></span>

<span data-ttu-id="9869f-122">Chcete-li stáhnout šablonu **Power Automate – připojení k formuláři** a Struktur vlastní entity, přejděte na [Power Automate – připojení k formuláři](https://go.microsoft.com/fwlink/?linkid=2081988) v Microsoft Download Center.</span><span class="sxs-lookup"><span data-stu-id="9869f-122">To download the **Power Automate – Form Connect** template and Custom Entity Structure, go to [Power Automate – Form Connect](https://go.microsoft.com/fwlink/?linkid=2081988) on the Microsoft Download Center.</span></span>

## <a name="power-automate--sharepoint-integration"></a><span data-ttu-id="9869f-123">Power Automate – integrace se službou SharePoint</span><span class="sxs-lookup"><span data-stu-id="9869f-123">Power Automate – SharePoint Integration</span></span>

<span data-ttu-id="9869f-124">Šablonu **Power Automate – Integrace SharePoint** lze použít ke čtení dat ze seznamu aplikace Microsoft SharePoint porovnání seznamu s hodnotami polí pro všechny entity Common Data Service a odesílání výsledků porovnání e-mailovým oznámením.</span><span class="sxs-lookup"><span data-stu-id="9869f-124">The **Power Automate – SharePoint Integration** template can be used to read data from a Microsoft SharePoint list, compare the list with field values for any Common Data Service entity, and send the results of the comparison as a notification email.</span></span> 

<span data-ttu-id="9869f-125">Organizace může míst sadu dovedností, které naléhavě vyžaduje.</span><span class="sxs-lookup"><span data-stu-id="9869f-125">An organization might have a set of skills that it urgently requires.</span></span> <span data-ttu-id="9869f-126">Tyto dovednosti mohou být uloženy v aplikaci SharePoint jako seznam SharePoint.</span><span class="sxs-lookup"><span data-stu-id="9869f-126">These skills can be stored in SharePoint as a SharePoint list.</span></span> <span data-ttu-id="9869f-127">Když kandidát požádá o práci, u které je uvedena sada požadovaných dovedností, dojde k odeslání e-mailového oznámení, pokud existuje významná shoda mezi dovednostmi kandidáta, a dovednostmi, které jsou uloženy v aplikaci SharePoint.</span><span class="sxs-lookup"><span data-stu-id="9869f-127">When a candidate applies for any job that a set of required skills is listed for, if there is a significant match between the candidate's skill and the skills that are stored in SharePoint, a notification email is sent.</span></span> <span data-ttu-id="9869f-128">To pomáhá obsadit naléhavě požadované pozice rychleji, protože oznámení pomáhají náborovým pracovníkům kontaktovat a interně najmout kandidáty v rámci organizace.</span><span class="sxs-lookup"><span data-stu-id="9869f-128">This helps fill positions that are urgently required faster, because the notifications help recruiters cross-hire candidates throughout the organization.</span></span>

<span data-ttu-id="9869f-129">Tuto šablonu lze rozšířit, aby ji bylo možné použít pro všechny scénáře, které zahrnují integraci SharePoint.</span><span class="sxs-lookup"><span data-stu-id="9869f-129">This template can be extended so that it can be used for any scenario that involves SharePoint integration.</span></span>

<span data-ttu-id="9869f-130">Chcete-li stáhnout šablonu **Power Automate – Integrace SharePoint**, přejděte na [Power Automate – Integrace SharePoint](https://go.microsoft.com/fwlink/?linkid=2082109) v Microsoft Download Center.</span><span class="sxs-lookup"><span data-stu-id="9869f-130">To download the **Power Automate – SharePoint Integration** template, go to [Power Automate – SharePoint Integration](https://go.microsoft.com/fwlink/?linkid=2082109) on the Microsoft Download Center.</span></span>

## <a name="referral-app"></a><span data-ttu-id="9869f-131">Referenční aplikace</span><span class="sxs-lookup"><span data-stu-id="9869f-131">Referral App</span></span>

<span data-ttu-id="9869f-132">Pomocí Referenční aplikace můžete přidat kandidáty do sdílené skupiny talentů.</span><span class="sxs-lookup"><span data-stu-id="9869f-132">You can use the Referral App to add candidates to a shared talent pool.</span></span> <span data-ttu-id="9869f-133">Poskytovatel reference může zadat **Křestní jméno**, **Příjmení**, **E-mail** a **Adresa URL LinkedIn** při odesílání uchazeče.</span><span class="sxs-lookup"><span data-stu-id="9869f-133">The referrer can enter **Firstname**, **Lastname**, **Email**, and **LinkedIn URL** when submitting a candidate.</span></span> <span data-ttu-id="9869f-134">Zdrojová metadata kandidáta jsou poté naplněna informacemi o poskytovateli reference.</span><span class="sxs-lookup"><span data-stu-id="9869f-134">The candidate source metadata is then populated with the referrer’s information.</span></span>

<span data-ttu-id="9869f-135">Tuto aplikaci můžete vložit do samoobsluhy zaměstnanců pro odesílání poskytovatelů reference nebo ji můžete použít jako hypertextový odkaz na podnikovém portálu a spustit jako samostatnou aplikaci.</span><span class="sxs-lookup"><span data-stu-id="9869f-135">You can embed this app in Employee self service for submitting referrals, or you can use it as a hyperlink in the corporate portal and run it as a stand-alone app.</span></span>

<span data-ttu-id="9869f-136">Chcete-li stáhnout **Referenční aplikaci**, přejděte na [Řešení rozšiřitelnosti Dynamics 365 Talent: Referenční aplikace](https://www.microsoft.com/download/details.aspx?id=58497) na webu Microsoft Download Center.</span><span class="sxs-lookup"><span data-stu-id="9869f-136">To download **Referral App**, go to [Dynamics 365 Talent extensibility solution: Referral App](https://www.microsoft.com/download/details.aspx?id=58497) on the Microsoft Download Center.</span></span> <span data-ttu-id="9869f-137">Chcete-li přidat další funkce, můžete tuto aplikaci importovat a přizpůsobit ji.</span><span class="sxs-lookup"><span data-stu-id="9869f-137">You can import this app and customize it to add additional functionality.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9869f-138">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="9869f-138">Additional resources</span></span>

[<span data-ttu-id="9869f-139">Microsoft Power Platform</span><span class="sxs-lookup"><span data-stu-id="9869f-139">The Microsoft Power Platform</span></span>](https://docs.microsoft.com/power-platform/admin/admin-documentation)</br>
[<span data-ttu-id="9869f-140">Migrace aplikace mezi klienty a prostředími</span><span class="sxs-lookup"><span data-stu-id="9869f-140">Migrate app between tenants and environments</span></span>](https://docs.microsoft.com/power-platform/admin/environment-and-tenant-migration)
