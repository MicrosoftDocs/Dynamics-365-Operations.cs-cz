---
title: "Funkce kariérního webu v systému Attract"
description: "Tento článek uvádí přehled funkce kariérního webu určené pro uchazeče v aplikaci Microsoft Dynamics 365 for Talent - Attract. Také popisuje postup nastavení této funkce."
author: josaw
manager: AnnBe
ms.date: 10/18/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2018-10-18
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e890e32049e930b70c2d0aac8aa8206ab999418a
ms.openlocfilehash: 452e3e92ea32ab5f1e3720ab81ff2f7ea18b2a06
ms.contentlocale: cs-cz
ms.lasthandoff: 10/22/2018

---
# <a name="career-site-functionality-in-attract"></a><span data-ttu-id="3f9b4-104">Funkce kariérního webu v systému Attract</span><span class="sxs-lookup"><span data-stu-id="3f9b4-104">Career site functionality in Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3f9b4-105">Tento článek uvádí přehled funkce kariérního webu určené pro uchazeče v aplikaci Microsoft Dynamics 365 for Talent: Attract.</span><span class="sxs-lookup"><span data-stu-id="3f9b4-105">This article provides an overview of the candidate-facing career site functionality in Microsoft Dynamics 365 for Talent: Attract.</span></span> <span data-ttu-id="3f9b4-106">Také popisuje postup nastavení této funkce.</span><span class="sxs-lookup"><span data-stu-id="3f9b4-106">It also explains how to set up this functionality.</span></span>

## <a name="overview"></a><span data-ttu-id="3f9b4-107">Přehled</span><span class="sxs-lookup"><span data-stu-id="3f9b4-107">Overview</span></span>

<span data-ttu-id="3f9b4-108">Attract poskytuje jeden kariérní web pro každé prostředí v klientovi.</span><span class="sxs-lookup"><span data-stu-id="3f9b4-108">Attract provides one career site for each environment in a tenant.</span></span> <span data-ttu-id="3f9b4-109">Pokud například organizace používá prostředí pro vývoj a testovací prostředí, je poskytován jeden kariérní web pro vývojové prostředí a jiný pro testovací prostředí.</span><span class="sxs-lookup"><span data-stu-id="3f9b4-109">For example, if an organization has a development environment and a test environment, one career site is provisioned for the development environment, and another career site is provisioned for the test environment.</span></span> <span data-ttu-id="3f9b4-110">Každý kariérní web však je **zcela nezávislý** a má vlastní mechanismus ověřování.</span><span class="sxs-lookup"><span data-stu-id="3f9b4-110">Each career site is **completely isolated** and has its own authentication mechanism.</span></span> <span data-ttu-id="3f9b4-111">Mezi kariérními weby nejsou sdíleny pracovní pozice a profily uchazečů.</span><span class="sxs-lookup"><span data-stu-id="3f9b4-111">Jobs and candidate profiles aren't shared between career sites.</span></span>

<span data-ttu-id="3f9b4-112">Ve výchozím nastavení je kariérní web veřejný.</span><span class="sxs-lookup"><span data-stu-id="3f9b4-112">By default, the career site is public.</span></span> <span data-ttu-id="3f9b4-113">Proto mohou kandidáti zobrazit všechna pracovní místa, která jsou označena jako externí, aniž by se museli přihlásit.</span><span class="sxs-lookup"><span data-stu-id="3f9b4-113">Therefore, candidates can view all jobs that are marked as external without having to sign in.</span></span> <span data-ttu-id="3f9b4-114">Všechny ostatní akce však vyžadují, aby se uchazeči přihlásili.</span><span class="sxs-lookup"><span data-stu-id="3f9b4-114">However, all other actions require that candidates sign in.</span></span>

## <a name="career-site-management"></a><span data-ttu-id="3f9b4-115">Správa kariérního webu</span><span class="sxs-lookup"><span data-stu-id="3f9b4-115">Career site management</span></span>

<span data-ttu-id="3f9b4-116">Následující položky na kariérním webu jsou řízeny nastaveními:</span><span class="sxs-lookup"><span data-stu-id="3f9b4-116">The following items on the career site are controlled by settings:</span></span>

- <span data-ttu-id="3f9b4-117">**Název organizace:** Název organizace se objevuje v navigačním panelu v horní části kariérního webu.</span><span class="sxs-lookup"><span data-stu-id="3f9b4-117">**Organization name:** The organization name appears on the navigation bar at the top of the career site.</span></span> <span data-ttu-id="3f9b4-118">Když uchazeč vybere název organizace, přejde na stránku se seznamem všech otevřených pracovních míst.</span><span class="sxs-lookup"><span data-stu-id="3f9b4-118">By selecting the organization name, candidates go to a page that lists all open jobs.</span></span>
- <span data-ttu-id="3f9b4-119">**Logo organizace:** V levém horním rohu kariérního webu se zobrazuje obrázek loga organizace.</span><span class="sxs-lookup"><span data-stu-id="3f9b4-119">**Organization logo:** An image of the organization's logo appears in the upper left of the career site.</span></span> <span data-ttu-id="3f9b4-120">Když uchazeč vybere obrázek loga, přejde na stránku se seznamem všech otevřených pracovních míst.</span><span class="sxs-lookup"><span data-stu-id="3f9b4-120">By selecting the logo image, candidates go to a page that lists all open jobs.</span></span>

<span data-ttu-id="3f9b4-121">Pokud chcete nastavit hodnoty pro název a logo organizace, přihlaste se k systému Attract jako správce, vyberte **Centrum pro správu** v nabídce **Nastavení** nabídky (symbol ozubeného kola) a pak vyberte kartu **informace o společnosti**.</span><span class="sxs-lookup"><span data-stu-id="3f9b4-121">To set the values for the organization name and logo, sign in to Attract as an administrator, select **Admin center** on the **Settings** menu (the gear symbol), and then select the **Company information** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="3f9b4-122">Obrázek loga, který se zobrazí na stránce kariérního webu, má pevnou výšku 20 pixelů (px).</span><span class="sxs-lookup"><span data-stu-id="3f9b4-122">The logo image that appears on the career site has a fixed height of 20 pixels (px).</span></span> <span data-ttu-id="3f9b4-123">Obrázek, který přidáte do Centra pro správu, se přizpůsobuje stránce.</span><span class="sxs-lookup"><span data-stu-id="3f9b4-123">The image that you add in the Admin center is scaled to fit.</span></span> <span data-ttu-id="3f9b4-124">Proto se může šířka měnit v závislosti na obrázku.</span><span class="sxs-lookup"><span data-stu-id="3f9b4-124">Therefore, depending on the image, the width might change.</span></span>

## <a name="career-site-url"></a><span data-ttu-id="3f9b4-125">Adresa URL kariérního webu</span><span class="sxs-lookup"><span data-stu-id="3f9b4-125">Career site URL</span></span>

<span data-ttu-id="3f9b4-126">Když [zveřejníte externí pracovní pozici](./Creating-jobs-Attract.md#postings) poprvé, můžete zkopírovat odkaz **Použít** z aplikace Attract.</span><span class="sxs-lookup"><span data-stu-id="3f9b4-126">When you [post an external job](./Creating-jobs-Attract.md#postings) for the first time, you can copy the **Apply** link from the Attract application.</span></span> <span data-ttu-id="3f9b4-127">Adresa URL pro tento odkaz bude v následujícím formátu: `https://jobs.talent.dynamics.com/jobs/<company_name>/<environment_number>/<job_number>/apply`</span><span class="sxs-lookup"><span data-stu-id="3f9b4-127">The URL for this link will be in the following format: `https://jobs.talent.dynamics.com/jobs/<company_name>/<environment_number>/<job_number>/apply`</span></span>

<span data-ttu-id="3f9b4-128">Adresa URL kariérního webu je dílčí řetězec pro **použití** adresy URL.</span><span class="sxs-lookup"><span data-stu-id="3f9b4-128">The URL of the career site is a substring of the **Apply** URL.</span></span> <span data-ttu-id="3f9b4-129">Sestává ze všech položek až k názvu společnosti.</span><span class="sxs-lookup"><span data-stu-id="3f9b4-129">It consists of everything up through the company name.</span></span> <span data-ttu-id="3f9b4-130">Proto je pro předchozí adresu URL pro **použití** adresa URL kariérního webu `https://jobs.talent.dynamics.com/jobs/<company_name>/`.</span><span class="sxs-lookup"><span data-stu-id="3f9b4-130">Therefore, for the preceding **Apply** URL, the career site URL is `https://jobs.talent.dynamics.com/jobs/<company_name>/`.</span></span>

## <a name="authentication-options"></a><span data-ttu-id="3f9b4-131">Možnosti ověřování</span><span class="sxs-lookup"><span data-stu-id="3f9b4-131">Authentication options</span></span>

<span data-ttu-id="3f9b4-132">Uchazeči mají k dispozici následující možnosti přihlašování ke kariérním webu Attract:</span><span class="sxs-lookup"><span data-stu-id="3f9b4-132">Candidates have the following sign-in options for an Attract career site:</span></span>

- <span data-ttu-id="3f9b4-133">Osobní účet:</span><span class="sxs-lookup"><span data-stu-id="3f9b4-133">Personal account:</span></span>

    - <span data-ttu-id="3f9b4-134">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="3f9b4-134">LinkedIn</span></span>
    - <span data-ttu-id="3f9b4-135">Microsoft </span><span class="sxs-lookup"><span data-stu-id="3f9b4-135">Microsoft</span></span>
    - <span data-ttu-id="3f9b4-136">Google</span><span class="sxs-lookup"><span data-stu-id="3f9b4-136">Google</span></span>
    - <span data-ttu-id="3f9b4-137">Facebook</span><span class="sxs-lookup"><span data-stu-id="3f9b4-137">Facebook</span></span>

- <span data-ttu-id="3f9b4-138">Pracovní nebo školní účet:</span><span class="sxs-lookup"><span data-stu-id="3f9b4-138">Work or school account:</span></span>

    - <span data-ttu-id="3f9b4-139">Microsoft Azure Active Directory (Azure AD)</span><span class="sxs-lookup"><span data-stu-id="3f9b4-139">Microsoft Azure Active Directory (Azure AD)</span></span>

<span data-ttu-id="3f9b4-140">Přihlašování ke službě Azure AD je určeno pouze pro interní uchazeče.</span><span class="sxs-lookup"><span data-stu-id="3f9b4-140">Azure AD sign-in is intended only for internal candidates.</span></span> <span data-ttu-id="3f9b4-141">Proto funguje pouze pro interní uchazeče, kteří používají své přihlašovací údaje služby Azure AD.</span><span class="sxs-lookup"><span data-stu-id="3f9b4-141">Therefore, it works only for internal candidates who use their company Azure AD credentials.</span></span> <span data-ttu-id="3f9b4-142">Například uchazeč, který je aktuálně zaměstnancem společnosti Contoso Ltd., chce zažádat o zaměstnání v nesouvisející společnost Alpine Ski House.</span><span class="sxs-lookup"><span data-stu-id="3f9b4-142">For example, a candidate who is currently an employee of Contoso Ltd wants to apply for a job in an unrelated company, Alpine Ski House.</span></span> <span data-ttu-id="3f9b4-143">V takovém případě přihlášení nebude úspěšné, pokud se zaměstnanec pokusí použít své přihlašovací údaje ke službě Azure AD od společnosti Contoso Ltd.</span><span class="sxs-lookup"><span data-stu-id="3f9b4-143">In this case, the sign-in will be unsuccessful if the employee tries to use his or her Azure AD credentials from Contoso Ltd.</span></span>

## <a name="create-and-maintain-a-profile"></a><span data-ttu-id="3f9b4-144">Vytvoření a správa profilu</span><span class="sxs-lookup"><span data-stu-id="3f9b4-144">Create and maintain a profile</span></span>

<span data-ttu-id="3f9b4-145">Poté, co se uchazeči přihlásí ke kariérnímu webu, mohou vybrat **Můj profil** na navigačním panelu v horní části stránky, kde mohou vytvořit a spravovat svůj profil.</span><span class="sxs-lookup"><span data-stu-id="3f9b4-145">After candidates sign in to the career site, they can select **My profile** on the navigation bar at the top of the page to create and maintain their profile.</span></span> <span data-ttu-id="3f9b4-146">Profil obsahuje osobní údaje, údaje o pracovních zkušenostech, podrobnostech o vzdělání, dokumenty, odkazy a informace o kvalifikačních předpokladech.</span><span class="sxs-lookup"><span data-stu-id="3f9b4-146">The profile includes personal information, information about work experience, education details, documents, links, and information about skill sets.</span></span> <span data-ttu-id="3f9b4-147">Po vytvoření lze profil použít k zažádání o pracovní místa, o která má uchazeč zájem.</span><span class="sxs-lookup"><span data-stu-id="3f9b4-147">After a profile is created, it can be used to apply for jobs that the candidate is interested in.</span></span> <span data-ttu-id="3f9b4-148">Profily také pomáhají systému Attract doporučit správná pracovní místa uchazečům.</span><span class="sxs-lookup"><span data-stu-id="3f9b4-148">Profiles also help Attract recommend the right jobs to candidates.</span></span>

## <a name="find-the-right-job"></a><span data-ttu-id="3f9b4-149">Vyhledání správné práce</span><span class="sxs-lookup"><span data-stu-id="3f9b4-149">Find the right job</span></span>

<span data-ttu-id="3f9b4-150">Na stránce se seznamem práce mohou uchazeči vyhledat určité pracovní místo zadáním hledaných pojmů.</span><span class="sxs-lookup"><span data-stu-id="3f9b4-150">On the job list page, candidates can search for a specific job by entering search terms.</span></span> <span data-ttu-id="3f9b4-151">Funkce vyhledávání vyhledá hledané termíny v názvech a popisech pracovní pozice a zobrazí jako výsledky relevantní pracovní místa.</span><span class="sxs-lookup"><span data-stu-id="3f9b4-151">The search functionality looks for the search terms in job titles and job descriptions, and shows relevant jobs as results.</span></span> <span data-ttu-id="3f9b4-152">Uchazeči mohou kdykoli filtrovat výsledky na základě místa výkonu práce nebo pracovní funkce.</span><span class="sxs-lookup"><span data-stu-id="3f9b4-152">Candidates can filter the results at any time, based on the job location or job function.</span></span>

<span data-ttu-id="3f9b4-153">Uchazeči také mohou zobrazit sadu doporučených pracovních míst na kariérním webu.</span><span class="sxs-lookup"><span data-stu-id="3f9b4-153">Candidates can also view a set of recommended jobs on the career site.</span></span> <span data-ttu-id="3f9b4-154">Pracovní místa, která jsou uchazeči doporučena, jsou založena na minulých žádostech uchazeče, profilu a životopisech.</span><span class="sxs-lookup"><span data-stu-id="3f9b4-154">The jobs that are recommended to a candidate are based on the candidate's past applications, profile, and resumes.</span></span>

> [!NOTE]
> <span data-ttu-id="3f9b4-155">Doporučení pracovních míst se zobrazí pouze v případě, že je na kariérním webu zveřejněno nejméně 10 pracovních míst, a pokud uchazeč vyplnil svůj profil.</span><span class="sxs-lookup"><span data-stu-id="3f9b4-155">Job recommendations are shown only if at least 10 jobs are posted on the career site, and if the candidate has completed his or her profile.</span></span>

## <a name="apply-for-jobs"></a><span data-ttu-id="3f9b4-156">Žádost o práci</span><span class="sxs-lookup"><span data-stu-id="3f9b4-156">Apply for jobs</span></span>

<span data-ttu-id="3f9b4-157">Poté, co uchazeči najdou správnou práci, mohou o ni zažádat pomocí tlačítka **použít** na stránce podrobností o pracovním místě.</span><span class="sxs-lookup"><span data-stu-id="3f9b4-157">After candidates find the right job, they can apply by using the **Apply** button on the job details page.</span></span> <span data-ttu-id="3f9b4-158">V tomto okamžiku mohou uchazeči vytvořit zcela nový profil nebo zkontrolovat informace ve svém existujícím profilu.</span><span class="sxs-lookup"><span data-stu-id="3f9b4-158">At this point, candidates can either create a brand-new profile or review the information in their existing profile.</span></span> <span data-ttu-id="3f9b4-159">Uchazeči také mohou nahrát podle potřeby životopis a odeslat žádost o práci.</span><span class="sxs-lookup"><span data-stu-id="3f9b4-159">Candidates can also upload a resume, as required, and then submit the job application.</span></span>

## <a name="check-application-status"></a><span data-ttu-id="3f9b4-160">Kontrola stavu žádosti</span><span class="sxs-lookup"><span data-stu-id="3f9b4-160">Check application status</span></span>

<span data-ttu-id="3f9b4-161">Poté, co uchazeči zažádají o jedno nebo více pracovních míst, mohou na navigačním panelu v horní části stránky vybrat možnost **Žádosti** k zobrazení otevřených a uzavřených žádostí.</span><span class="sxs-lookup"><span data-stu-id="3f9b4-161">After candidates apply for one or more jobs, they can select **Applications** on the navigation bar at the top of the page to view their open and closed applications.</span></span> <span data-ttu-id="3f9b4-162">Jakmile uchazeči otevřou některou ze svých žádostí, uvidí aktuální fázi a jakékoli čekající položky akcí, které je nutné dokončit.</span><span class="sxs-lookup"><span data-stu-id="3f9b4-162">When candidates open one of their applications, they see the current stage and any pending action items that they must complete.</span></span> <span data-ttu-id="3f9b4-163">Pokud musí například uchazeč poskytnout potenciální data pro pohovor mezi čtyřma očima, na stránce se zobrazí jeho možnosti.</span><span class="sxs-lookup"><span data-stu-id="3f9b4-163">For example, if a candidate must provide potential dates for an in-person interview, the page shows his or her options.</span></span>

## <a name="internal-jobs"></a><span data-ttu-id="3f9b4-164">Interní pracovní pozice</span><span class="sxs-lookup"><span data-stu-id="3f9b4-164">Internal jobs</span></span>

<span data-ttu-id="3f9b4-165">V současné době se pracovní pozice, které jsou označeny jako interní a publikované na kariérním webu Attract, na kariérním webu nezobrazují.</span><span class="sxs-lookup"><span data-stu-id="3f9b4-165">Currently, jobs that are marked as internal and posted to the Attract career site don't appear on the career site.</span></span> <span data-ttu-id="3f9b4-166">Jsou přístupné pouze prostřednictvím přímé adresy URL **Použít**, kterou lze kopírovat z aplikace Attract.</span><span class="sxs-lookup"><span data-stu-id="3f9b4-166">They are accessible only via the direct **Apply** URL that can be copied from the Attract application.</span></span>

