---
title: Funkce kariérního webu v aplikaci Attract
description: Toto téma poskytuje přehled funkce kariérního webu vystaveného kandidátům v aplikaci Attract
author: josaw1
manager: AnnBe
ms.date: 02/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-02-12
ms.dyn365.ops.version: AX 7.1.0, Talent April 2018 update
ms.openlocfilehash: 087ab4034a1e601e7f3514c77d56ef54b0c5c52d
ms.sourcegitcommit: 1ee613a88edddab036d145f27f19d071a4b8ad24
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/13/2019
ms.locfileid: "389952"
---
# <a name="career-site-functionality-in-attract"></a><span data-ttu-id="c9db5-103">Funkce kariérního webu v aplikaci Attract</span><span class="sxs-lookup"><span data-stu-id="c9db5-103">Career site functionality in Attract</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="c9db5-104">Toto téma poskytuje přehled funkce kariérního webu vystaveného kandidátům v aplikaci Microsoft Dynamics 365 for Talent: Attract.</span><span class="sxs-lookup"><span data-stu-id="c9db5-104">This topic provides an overview of the candidate-facing career site functionality in Microsoft Dynamics 365 for Talent: Attract.</span></span> <span data-ttu-id="c9db5-105">Také vysvětluje, jak tuto funkci nastavit.</span><span class="sxs-lookup"><span data-stu-id="c9db5-105">It also explains how to set up this functionality.</span></span>

<span data-ttu-id="c9db5-106">Attract poskytuje jeden kariérní web pro každé prostředí v klientovi.</span><span class="sxs-lookup"><span data-stu-id="c9db5-106">Attract provides one career site for each environment in a tenant.</span></span> <span data-ttu-id="c9db5-107">Pokud například organizace používá prostředí pro vývoj a testovací prostředí, je zřízen jeden kariérní web pro vývojové prostředí a jiný pro testovací prostředí.</span><span class="sxs-lookup"><span data-stu-id="c9db5-107">For example, if an organization has a development environment and a test environment, one career site is provisioned for the development environment, and another career site is provisioned for the test environment.</span></span> <span data-ttu-id="c9db5-108">Každý kariérní web je zcela nezávislý a má vlastní mechanismus ověřování.</span><span class="sxs-lookup"><span data-stu-id="c9db5-108">Each career site is completely isolated and has its own authentication mechanism.</span></span> <span data-ttu-id="c9db5-109">Mezi kariérními weby nejsou sdíleny pracovní pozice a profily kandidátů.</span><span class="sxs-lookup"><span data-stu-id="c9db5-109">Jobs and candidate profiles aren't shared between career sites.</span></span>

<span data-ttu-id="c9db5-110">Ve výchozím nastavení je kariérní web veřejný.</span><span class="sxs-lookup"><span data-stu-id="c9db5-110">By default, the career site is public.</span></span> <span data-ttu-id="c9db5-111">Proto mohou kandidáti zobrazit všechna pracovní místa, která jsou označena jako externí, aniž by se museli přihlásit.</span><span class="sxs-lookup"><span data-stu-id="c9db5-111">Therefore, candidates can view all jobs that are marked as external without having to sign in.</span></span> <span data-ttu-id="c9db5-112">Všechny ostatní akce však vyžadují, aby se uchazeči přihlásili.</span><span class="sxs-lookup"><span data-stu-id="c9db5-112">However, all other actions require that candidates sign in.</span></span>

## <a name="career-site-management"></a><span data-ttu-id="c9db5-113">Správa kariérního webu</span><span class="sxs-lookup"><span data-stu-id="c9db5-113">Career site management</span></span>

<span data-ttu-id="c9db5-114">Pokud chcete nastavit hodnoty pro následující položky, přihlaste se k systému Attract jako správce, vyberte **Centrum pro správu** v nabídce **Nastavení** nabídky (symbol ozubeného kola) a pak vyberte kartu **informace o společnosti**.</span><span class="sxs-lookup"><span data-stu-id="c9db5-114">To set the values for the following items, sign in to Attract as an administrator, select **Admin center** on the **Settings** menu (the gear symbol), and then select the **Company information** tab.</span></span>

-   <span data-ttu-id="c9db5-115">**Název organizace:** - Název organizace se objevuje v navigačním panelu v horní části kariérního webu.</span><span class="sxs-lookup"><span data-stu-id="c9db5-115">**Organization name** - The organization name appears on the navigation bar at the top of the career site.</span></span> <span data-ttu-id="c9db5-116">Když uchazeč vybere název organizace, přejde na stránku se seznamem všech otevřených pracovních míst.</span><span class="sxs-lookup"><span data-stu-id="c9db5-116">By selecting the organization name, candidates go to a page that lists all open jobs.</span></span>

-   <span data-ttu-id="c9db5-117">**Logo organizace:** - V levém horním rohu kariérního webu se zobrazuje obrázek loga organizace.</span><span class="sxs-lookup"><span data-stu-id="c9db5-117">**Organization logo** - An image of the organization's logo appears in the upper left of the career site.</span></span> <span data-ttu-id="c9db5-118">Když uchazeč vybere obrázek loga, přejde na stránku se seznamem všech otevřených pracovních míst.</span><span class="sxs-lookup"><span data-stu-id="c9db5-118">By selecting the logo image, candidates go to a page that lists all open jobs.</span></span>

    >   [!NOTE] 
    >   <span data-ttu-id="c9db5-119">Obrázek loga, který se zobrazí na stránce kariérního webu, má pevnou výšku 20 pixelů (px).</span><span class="sxs-lookup"><span data-stu-id="c9db5-119">The logo image that appears on the career site has a fixed height of 20 pixels (px).</span></span> <span data-ttu-id="c9db5-120">Obrázek, který přidáte do Centra pro správu, se přizpůsobuje stránce.</span><span class="sxs-lookup"><span data-stu-id="c9db5-120">The image that you add in the Admin center is scaled to fit.</span></span> <span data-ttu-id="c9db5-121">Proto se může šířka měnit v závislosti na obrázku.</span><span class="sxs-lookup"><span data-stu-id="c9db5-121">Therefore, depending on the image, the width might change.</span></span>
 
<span data-ttu-id="c9db5-122">Pokud chcete nastavit hodnoty pro následující položky, přihlaste se k aplikaci Attract jako správce, vyberte **Centrum pro správu** v nabídce **Nastavení** a poté zvolte kartu **Správa kariérního webu**.</span><span class="sxs-lookup"><span data-stu-id="c9db5-122">To set the values for the following items, sign in to Attract as an administrator, select **Admin center** on the **Settings** menu, and then select the **Career site management** tab.</span></span>

-   <span data-ttu-id="c9db5-123">**Optimalizace pro vyhledávače** - Pokud je povolena, budou všechny nabídky práce publikované na kariérním webu Attract vyhledávatelné pomocí vyhledávačů, jako jsou Bing a Google.</span><span class="sxs-lookup"><span data-stu-id="c9db5-123">**Search Engine Optimization** - When enabled, all public jobs posted to Attract career site will be searchable using search engines like Bing and Google.</span></span>

    >   [!NOTE] 
    >   <span data-ttu-id="c9db5-124">Může dojít ke zpoždění mezi zapnutím tohoto nastavení a zobrazením výsledků vyhledávání, v závislosti na používaném vyhledávači.</span><span class="sxs-lookup"><span data-stu-id="c9db5-124">There might be a delay between turning this setting on and search results appearing, depending on the search engine that you are using.</span></span>
         
## <a name="career-site-urls"></a><span data-ttu-id="c9db5-125">URL adresy kariérního webu</span><span class="sxs-lookup"><span data-stu-id="c9db5-125">Career site URLs</span></span>

<span data-ttu-id="c9db5-126">Následující seznam obsahuje běžně používané URL adresy kariérního webu a způsob přístupu.</span><span class="sxs-lookup"><span data-stu-id="c9db5-126">The following list contains the commonly used career site URLs and how to access them.</span></span>

-   <span data-ttu-id="c9db5-127">**Adresa URL domovské stránky kariérního webu** – Chcete-li zobrazit adresu URL domovské stránky kariérního webu, přihlaste se k aplikaci Attract jako správce, vyberte **Centrum pro správu** v nabídce **Nastavení** a poté vyberte kartu **Správa kariérního webu**.</span><span class="sxs-lookup"><span data-stu-id="c9db5-127">**Career site home page URL** - To view the career site home page URL, sign in to Attract as an administrator, select **Admin center** on the **Settings** menu, and then select the **Career site management** tab.</span></span>

-   <span data-ttu-id="c9db5-128">**URL adresa individuální žádosti o publikování práce** - Když [publikujete externí práci](Creating-jobs-Attract.md#postings) poprvé, můžete zkopírovat odkaz **Požádat** z aplikace Attract.</span><span class="sxs-lookup"><span data-stu-id="c9db5-128">**Individual job post apply URL** - When you [post an external job](Creating-jobs-Attract.md#postings) for the first time, you can copy the **Apply** link from the Attract application.</span></span> <span data-ttu-id="c9db5-129">Adresa URL pro tento odkaz bude v následujícím formátu: [https://jobs.talent.dynamics.com/jobs/\<company_name\>/\<environment_number\>/\<job_number\>/apply](https://jobs.talent.dynamics.com/jobs/%3ccompany_name%3e/%3cenvironment_number%3e/%3cjob_number%3e/apply)</span><span class="sxs-lookup"><span data-stu-id="c9db5-129">The URL for this link will be in the following format: [https://jobs.talent.dynamics.com/jobs/\<company_name\>/\<environment_number\>/\<job_number\>/apply](https://jobs.talent.dynamics.com/jobs/%3ccompany_name%3e/%3cenvironment_number%3e/%3cjob_number%3e/apply)</span></span>

-   <span data-ttu-id="c9db5-130">**URL adresa individuálního publikování práce** – Adresa URL publikování práce je dílčí řetězec žádosti.</span><span class="sxs-lookup"><span data-stu-id="c9db5-130">**Individual job post URL** - The URL of the job post is a substring of the Apply URL.</span></span> <span data-ttu-id="c9db5-131">Sestává ze všech položek až k číslu práce.</span><span class="sxs-lookup"><span data-stu-id="c9db5-131">It consists of everything up through the job number.</span></span> <span data-ttu-id="c9db5-132">Proto je pro předchozí adresu URL žádosti URL adresa publikování práce [https://jobs.talent.dynamics.com/jobs/\<company_name\>/\<environment_number\>/\<job_number\>](https://jobs.talent.dynamics.com/jobs/%3ccompany_name%3e/%3cenvironment_number%3e/%3cjob_number%3e)</span><span class="sxs-lookup"><span data-stu-id="c9db5-132">Therefore, for the preceding Apply URL, the job post URL is [https://jobs.talent.dynamics.com/jobs/\<company_name\>/\<environment_number\>/\<job_number\>](https://jobs.talent.dynamics.com/jobs/%3ccompany_name%3e/%3cenvironment_number%3e/%3cjob_number%3e)</span></span>

## <a name="authentication-options"></a><span data-ttu-id="c9db5-133">Možnosti ověřování</span><span class="sxs-lookup"><span data-stu-id="c9db5-133">Authentication options</span></span>

<span data-ttu-id="c9db5-134">Uchazeči mají k dispozici následující možnosti přihlašování ke kariérním webu Attract:</span><span class="sxs-lookup"><span data-stu-id="c9db5-134">Candidates have the following sign-in options for an Attract career site:</span></span>

-   <span data-ttu-id="c9db5-135">Osobní účet:</span><span class="sxs-lookup"><span data-stu-id="c9db5-135">Personal account:</span></span>

    -   <span data-ttu-id="c9db5-136">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="c9db5-136">LinkedIn</span></span>

    -   <span data-ttu-id="c9db5-137">Microsoft</span><span class="sxs-lookup"><span data-stu-id="c9db5-137">Microsoft</span></span>

    -   <span data-ttu-id="c9db5-138">Google</span><span class="sxs-lookup"><span data-stu-id="c9db5-138">Google</span></span>

    -   <span data-ttu-id="c9db5-139">Facebook</span><span class="sxs-lookup"><span data-stu-id="c9db5-139">Facebook</span></span>

-   <span data-ttu-id="c9db5-140">Pracovní nebo školní účet:</span><span class="sxs-lookup"><span data-stu-id="c9db5-140">Work or school account:</span></span>

    -   <span data-ttu-id="c9db5-141">Microsoft Azure Active Directory (Azure AD)</span><span class="sxs-lookup"><span data-stu-id="c9db5-141">Microsoft Azure Active Directory (Azure AD)</span></span>

<span data-ttu-id="c9db5-142">Přihlašování ke službě Azure AD je určeno pouze pro interní kandidáty.</span><span class="sxs-lookup"><span data-stu-id="c9db5-142">Azure AD sign-in is intended only for internal candidates.</span></span> <span data-ttu-id="c9db5-143">Proto funguje pouze pro interní uchazeče, kteří používají své přihlašovací údaje služby Azure AD.</span><span class="sxs-lookup"><span data-stu-id="c9db5-143">Therefore, it works only for internal candidates who use their company Azure AD credentials.</span></span> <span data-ttu-id="c9db5-144">Například uchazeč, který je aktuálně zaměstnancem společnosti Contoso Ltd., chce zažádat o zaměstnání v nesouvisející společnost Alpine Ski House.</span><span class="sxs-lookup"><span data-stu-id="c9db5-144">For example, a candidate who is currently an employee of Contoso Ltd wants to apply for a job in an unrelated company, Alpine Ski House.</span></span> <span data-ttu-id="c9db5-145">V takovém případě přihlášení nebude úspěšné, pokud se zaměstnanec pokusí použít své přihlašovací údaje ke službě Azure AD od společnosti Contoso Ltd.</span><span class="sxs-lookup"><span data-stu-id="c9db5-145">In this case, the sign-in will be unsuccessful if the employee tries to use Azure AD credentials from Contoso Ltd.</span></span>

## <a name="create-and-maintain-a-profile"></a><span data-ttu-id="c9db5-146">Vytvoření a správa profilu</span><span class="sxs-lookup"><span data-stu-id="c9db5-146">Create and maintain a profile</span></span>

<span data-ttu-id="c9db5-147">Poté, co se uchazeči přihlásí ke kariérnímu webu, mohou vybrat **Můj profil** na navigačním panelu v horní části stránky, kde mohou vytvořit a spravovat svůj profil.</span><span class="sxs-lookup"><span data-stu-id="c9db5-147">After candidates sign in to the career site, they can select **My profile** on the navigation bar at the top of the page to create and maintain their profile.</span></span>
<span data-ttu-id="c9db5-148">Profil obsahuje osobní údaje, údaje o pracovních zkušenostech, podrobnostech o vzdělání, dokumenty, odkazy a informace o kvalifikačních předpokladech.</span><span class="sxs-lookup"><span data-stu-id="c9db5-148">The profile includes personal information, information about work experience, education details, documents, links, and information about skill sets.</span></span> <span data-ttu-id="c9db5-149">Po vytvoření lze profil použít k zažádání o pracovní místa, o která má uchazeč zájem.</span><span class="sxs-lookup"><span data-stu-id="c9db5-149">After a profile is created, it can be used to apply for jobs that the candidate is interested in.</span></span> <span data-ttu-id="c9db5-150">Profily také pomáhají systému Attract doporučit správná pracovní místa uchazečům.</span><span class="sxs-lookup"><span data-stu-id="c9db5-150">Profiles also help Attract recommend the right jobs to candidates.</span></span>

>   [!NOTE]
>   <span data-ttu-id="c9db5-151">Pokud kandidát použije ID e-mailu k přihlášení pomocí jednoho z výše uvedených poskytovatelů ověřování, toto e-mailové ID bude standardně nastaveno na ID e-mailu kontaktu přidruženého k profilu.</span><span class="sxs-lookup"><span data-stu-id="c9db5-151">If a candidate uses an email ID to sign in using one of the authentication providers listed above, that email ID will default to the contact email ID associated with the profile.</span></span> <span data-ttu-id="c9db5-152">Ty druhé však mohou být kdykoliv změněny a jsou zcela nezávislé na prvním.</span><span class="sxs-lookup"><span data-stu-id="c9db5-152">However, the latter can be changed at any time and is completely independent of the former.</span></span> <span data-ttu-id="c9db5-153">Attract vždy použije ID e-mailu kontaktu pro přidružení k vašemu profilu pro všechny e-mailové komunikace.</span><span class="sxs-lookup"><span data-stu-id="c9db5-153">Attract will always use the contact email ID to associate with your profile for all email communications.</span></span>

## <a name="find-the-right-job"></a><span data-ttu-id="c9db5-154">Vyhledání správné práce</span><span class="sxs-lookup"><span data-stu-id="c9db5-154">Find the right job</span></span>

<span data-ttu-id="c9db5-155">Na stránce se seznamem práce mohou uchazeči vyhledat určité pracovní místo zadáním hledaných pojmů.</span><span class="sxs-lookup"><span data-stu-id="c9db5-155">On the job list page, candidates can search for a specific job by entering search terms.</span></span> <span data-ttu-id="c9db5-156">Funkce vyhledávání vyhledá hledané termíny v názvech a popisech pracovní pozice a zobrazí jako výsledky relevantní pracovní místa.</span><span class="sxs-lookup"><span data-stu-id="c9db5-156">The search functionality looks for the search terms in job titles and job descriptions, and shows relevant jobs as results.</span></span> <span data-ttu-id="c9db5-157">Uchazeči mohou kdykoli filtrovat výsledky na základě místa výkonu práce nebo pracovní funkce.</span><span class="sxs-lookup"><span data-stu-id="c9db5-157">Candidates can filter the results at any time, based on the job location or job function.</span></span>

<span data-ttu-id="c9db5-158">Uchazeči také mohou zobrazit sadu doporučených pracovních míst na kariérním webu.</span><span class="sxs-lookup"><span data-stu-id="c9db5-158">Candidates can also view a set of recommended jobs on the career site.</span></span> <span data-ttu-id="c9db5-159">Pracovní místa, která jsou uchazeči doporučena, jsou založena na minulých žádostech uchazeče, profilu a životopisech.</span><span class="sxs-lookup"><span data-stu-id="c9db5-159">The jobs that are recommended to a candidate are based on the candidate's past applications, profile, and resumes.</span></span>

>   [!NOTE] 
>   <span data-ttu-id="c9db5-160">Doporučení pracovních míst se zobrazí pouze v případě, že je na kariérním webu zveřejněno nejméně 10 pracovních míst, a pokud uchazeč vyplnil svůj profil.</span><span class="sxs-lookup"><span data-stu-id="c9db5-160">Job recommendations are shown only if at least 10 jobs are posted on the career site, and if the candidate has completed a profile.</span></span>

## <a name="apply-for-jobs"></a><span data-ttu-id="c9db5-161">Žádost o práci</span><span class="sxs-lookup"><span data-stu-id="c9db5-161">Apply for jobs</span></span>

<span data-ttu-id="c9db5-162">Poté, co uchazeči najdou správnou práci, mohou o ni zažádat pomocí tlačítka **Požádat** na stránce **Podrobnosti o práci**.</span><span class="sxs-lookup"><span data-stu-id="c9db5-162">After candidates find the right job, they can apply by using the **Apply** button on the **Job details** page.</span></span> <span data-ttu-id="c9db5-163">V tomto okamžiku mohou uchazeči vytvořit nový profil nebo zkontrolovat informace ve svém existujícím profilu.</span><span class="sxs-lookup"><span data-stu-id="c9db5-163">At this point, candidates can either create a new profile or review the information in their existing profile.</span></span>
<span data-ttu-id="c9db5-164">Uchazeči také mohou nahrát podle potřeby životopis a odeslat žádost o práci.</span><span class="sxs-lookup"><span data-stu-id="c9db5-164">Candidates can also upload a resume, as required, and then submit the job application.</span></span>

## <a name="check-application-status"></a><span data-ttu-id="c9db5-165">Kontrola stavu žádosti</span><span class="sxs-lookup"><span data-stu-id="c9db5-165">Check application status</span></span>

<span data-ttu-id="c9db5-166">Poté, co uchazeči zažádají o jedno nebo více pracovních míst, mohou na navigačním panelu v horní části stránky vybrat možnost **Žádosti** k zobrazení otevřených a uzavřených žádostí.</span><span class="sxs-lookup"><span data-stu-id="c9db5-166">After candidates apply for one or more jobs, they can select **Applications** on the navigation bar at the top of the page to view their open and closed applications.</span></span> <span data-ttu-id="c9db5-167">Jakmile uchazeči otevřou některou ze svých žádostí, uvidí aktuální fázi a jakékoli čekající položky akcí, které je nutné dokončit.</span><span class="sxs-lookup"><span data-stu-id="c9db5-167">When candidates open one of their applications, they see the current stage and any pending action items that they must complete.</span></span> <span data-ttu-id="c9db5-168">Pokud musí například uchazeč poskytnout potenciální data pro pohovor mezi čtyřma očima, na stránce se zobrazí dostupné možnosti.</span><span class="sxs-lookup"><span data-stu-id="c9db5-168">For example, if a candidate must provide potential dates for an in-person interview, the page shows the available options.</span></span>

## <a name="internal-jobs"></a><span data-ttu-id="c9db5-169">Interní pracovní pozice</span><span class="sxs-lookup"><span data-stu-id="c9db5-169">Internal jobs</span></span>

<span data-ttu-id="c9db5-170">V současné době se pracovní pozice, které jsou označeny jako interní a publikované na kariérním webu Attract, na kariérním webu nezobrazují.</span><span class="sxs-lookup"><span data-stu-id="c9db5-170">Currently, jobs that are marked as internal and posted to the Attract career site don't appear on the career site.</span></span> <span data-ttu-id="c9db5-171">Jsou přístupné pouze prostřednictvím přímé adresy URL **Požádat**, kterou lze kopírovat z aplikace Attract.</span><span class="sxs-lookup"><span data-stu-id="c9db5-171">They are only accessible using the direct **Apply** URL that can be copied from the Attract application.</span></span>
