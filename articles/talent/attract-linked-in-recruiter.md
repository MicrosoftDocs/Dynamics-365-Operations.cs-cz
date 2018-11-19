---
title: "Zajištění zdrojů pomocí LinkedIn Recruiter"
description: "Toto téma obsahuje informace o používání strojového učení pro získání doporučení práce a uchazeče o práci."
author: josaw
manager: AnnBe
ms.date: 10/15/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.search.industry: 
ms.author: josaw
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.translationtype: HT
ms.sourcegitcommit: 2fc6bf25d303d7d8de8002a923a080b90dcfbeab
ms.openlocfilehash: 106103e2c3d8f3d89aac5140174e5794da22536f
ms.contentlocale: cs-cz
ms.lasthandoff: 10/24/2018

---

# <a name="sourcing-with-linkedin-recruiter"></a><span data-ttu-id="2ed8e-103">Zajištění zdrojů pomocí LinkedIn Recruiter</span><span class="sxs-lookup"><span data-stu-id="2ed8e-103">Sourcing with LinkedIn Recruiter</span></span>
[!include[banner](../includes/banner.md)]

<span data-ttu-id="2ed8e-104">LinkedIn je největší databáze talentů na světě a často slouží jako primární systém, který náboráři používají k vyhledávání, komunikaci a zajišťování zdrojů uchazečů o pracovní pozice, které chtějí náboráři obsadit.</span><span class="sxs-lookup"><span data-stu-id="2ed8e-104">LinkedIn is the world’s largest talent database and often the primary system that recruiters use to find, communicate with, and source candidates for the jobs that recruiters are looking to fill.</span></span> <span data-ttu-id="2ed8e-105">Integrace programu LinkedIn Recruiter s aplikací Dynamics 365 for Talent: Attract uživatelům usnadňuje nábor a udržování synchronizace dat mezi dvěma systémy.</span><span class="sxs-lookup"><span data-stu-id="2ed8e-105">LinkedIn Recruiter integration with Dynamics 365 for Talent: Attract makes it easier for users to hire, and to keep the data in sync between the two systems.</span></span>

> [!NOTE]
> <span data-ttu-id="2ed8e-106">Aby bylo možné používat integraci programu LinkedIn Recruiter s aplikací Attract, je potřeba doplněk Comprehensive hiring a licence LinkedIn Recruiter.</span><span class="sxs-lookup"><span data-stu-id="2ed8e-106">You need the Comprehensive hiring add-on and LinkedIn Recruiter seats to be able to use LinkedIn Recruiter integration with Attract.</span></span>

## <a name="set-up-linkedin-recruiter-with-attract"></a><span data-ttu-id="2ed8e-107">Nastavení webu LinkedIn Recruiter s aplikací Attract</span><span class="sxs-lookup"><span data-stu-id="2ed8e-107">Set up LinkedIn Recruiter with Attract</span></span> 

<span data-ttu-id="2ed8e-108">Než budete moci využívat program LinkedIn Recruiter, musíte nakonfigurovat přístup na úrovni smlouvy nebo společnosti s instancí aplikace Attract.</span><span class="sxs-lookup"><span data-stu-id="2ed8e-108">Before you can use the LinkedIn Recruiter capabilities, you must configure contract-level or company-level access with your Attract instance.</span></span> <span data-ttu-id="2ed8e-109">Pro dokončení procesu konfigurace musíte spolupracovat s uživatelem, který je správce vaší smlouvy o programu LinkedIn Recruiter.</span><span class="sxs-lookup"><span data-stu-id="2ed8e-109">To complete the configuration process, you must work with the user who is an Admin on your LinkedIn Recruiter contract.</span></span> <span data-ttu-id="2ed8e-110">Pomocí následujících kroků nakonfigurujte LinkedIn Recruiter s aplikací Attract.</span><span class="sxs-lookup"><span data-stu-id="2ed8e-110">Complete the following steps to configure LinkedIn Recruiter with Attract.</span></span>

1.  <span data-ttu-id="2ed8e-111">Přihlaste se k aplikaci Attract jako správce a přejděte na **nastavení pro správu**.</span><span class="sxs-lookup"><span data-stu-id="2ed8e-111">Sign in to Attract as an Admin and go to **Admin Settings**.</span></span>

2.  <span data-ttu-id="2ed8e-112">V levém podokně klikněte na kartu **Integrace LinkedIn**.</span><span class="sxs-lookup"><span data-stu-id="2ed8e-112">On the left pane, click the **LinkedIn Integration** tab.</span></span>

<span data-ttu-id="2ed8e-113">[![Zobrazení správce aplikace Attract ke spuštění integrace s programem LinkedIn Recruiter](./media/LinkedInConnect.png)](./media/LinkedInConnect.png)</span><span class="sxs-lookup"><span data-stu-id="2ed8e-113">[![Attract Admin view to start LinkedIn Recruiter integration](./media/LinkedInConnect.png)](./media/LinkedInConnect.png)</span></span>

3.  <span data-ttu-id="2ed8e-114">Klikněte na tlačítko **připojit** pro spuštění nastavení. Budete provedeni procesem registrace LinkedIn.</span><span class="sxs-lookup"><span data-stu-id="2ed8e-114">Click **Connect** to start the setup and be guided through the LinkedIn sign-in process.</span></span>

4.  <span data-ttu-id="2ed8e-115">Pokud máte licence na více smluv LinkedIn, vyberte smlouvu, kterou chcete spojit se systémem Attract.</span><span class="sxs-lookup"><span data-stu-id="2ed8e-115">If you have seats on multiple LinkedIn contracts, select the contract that you would like to connect to the Attract system.</span></span> <span data-ttu-id="2ed8e-116">Pokud máte licenci jenom v rámci jedné smlouvy LinkedIn, tento krok není potřeba.</span><span class="sxs-lookup"><span data-stu-id="2ed8e-116">If you have a seat on only one LinkedIn contract, this step will not be needed.</span></span>

5.  <span data-ttu-id="2ed8e-117">V nastavení pro správu se nyní načte miniaplikace LinkedIn se seznamem integrací.</span><span class="sxs-lookup"><span data-stu-id="2ed8e-117">The LinkedIn widget will now load in your Admin settings with the list of integrations shown.</span></span> <span data-ttu-id="2ed8e-118">Ve skupinovém rámečku **připojení systému Recruiter** klikněte na tlačítko **Požadavek**.</span><span class="sxs-lookup"><span data-stu-id="2ed8e-118">Under **Recruiter System connect**, click **Request**.</span></span>

<span data-ttu-id="2ed8e-119">[![Zobrazení správce aplikace Attract k vyžádání integrace s programem LinkedIn Recruiter](./media/RequestLinkedInRSC.png)](./media/RequestLinkedInRSC.png)</span><span class="sxs-lookup"><span data-stu-id="2ed8e-119">[![Attract Admin view to Request LinkedIn Recruiter integration](./media/RequestLinkedInRSC.png)](./media/RequestLinkedInRSC.png)</span></span>

6.  <span data-ttu-id="2ed8e-120">Po vyžádání integrace ze systému Attract se zobrazí jako **Připraveno pro partnera** a dá se zapnout z **nastavení správy systému Recruiter**.</span><span class="sxs-lookup"><span data-stu-id="2ed8e-120">After the integration is requested from Attract, it will show as **Partner ready** and is ready to be turned on from **Recruiter Admin settings**.</span></span> <span data-ttu-id="2ed8e-121">Pokud a této stránce vidíte také možnost **Upozornit partnera**, počkejte chvíli, klikněte na tlačítko **Upozornit partnera** a poté stránku aktualizujte.</span><span class="sxs-lookup"><span data-stu-id="2ed8e-121">If you see **Notify partner** on this page, wait a few seconds, click **Notify partner**, and then refresh the page.</span></span> <span data-ttu-id="2ed8e-122">Nyní by se měla zobrazovat jako **připravená pro partnera**.</span><span class="sxs-lookup"><span data-stu-id="2ed8e-122">It should now show as **Partner ready**.</span></span>

<span data-ttu-id="2ed8e-123">[![Zobrazení správce systému Attract k označení strany požadavků Attract, které byly dokončeny.](./media/PartnerReadyRSC.png)](./media/PartnerReadyRSC.png)</span><span class="sxs-lookup"><span data-stu-id="2ed8e-123">[![Attract Admin view to indicate Attract side of requests have been completed](./media/PartnerReadyRSC.png)](./media/PartnerReadyRSC.png)</span></span>

<span data-ttu-id="2ed8e-124">Pokud chcete dokončit další krok, musíte mít oprávnění správce smluv LinkedIn Recruiter.</span><span class="sxs-lookup"><span data-stu-id="2ed8e-124">To complete the next step, you need to have an Admin privilege on your LinkedIn Recruiter Contract.</span></span>

7.  <span data-ttu-id="2ed8e-125">Přihaste se k webu LinkedIn pomocí účtu správce a přejděte na web LinkedIn Recruiter vpravo nahoře.</span><span class="sxs-lookup"><span data-stu-id="2ed8e-125">Sign in to LinkedIn using the Admin account and go to LinkedIn Recruiter on the top right.</span></span> 

8. <span data-ttu-id="2ed8e-126">V nabídce **Další** v horní části obrazovky klikněte na **nastavení pro správu** a potom klikněte na kartu **ATS**.</span><span class="sxs-lookup"><span data-stu-id="2ed8e-126">On the **More** menu at the top of the screen, click **Admin Settings**, and then click the **ATS** Tab.</span></span>

<span data-ttu-id="2ed8e-127">Systém Attract bude uveden s několika možnostmi, které lze zapnout.</span><span class="sxs-lookup"><span data-stu-id="2ed8e-127">The Attract system will be listed with a couple of options that can be turned on.</span></span>

9. <span data-ttu-id="2ed8e-128">Pokud chcete povolit export pouze 1-kliknutím pro **indikátor In-ATS** a **miniaplikaci In-ATS profil**, vyberte **přístup na úrovni společnosti**.</span><span class="sxs-lookup"><span data-stu-id="2ed8e-128">If you want to enable only 1-Click export for the **In-ATS indicator** and the **In-ATS Profile Widget**, select **Company-level access**.</span></span> <span data-ttu-id="2ed8e-129">Pokud chcete povolit všechny funkce přístupu na úrovni společnosti plus historii InMail a přístupu neúplného profilu InMail, vyberte **Přístup na úrovni smlouvy**.</span><span class="sxs-lookup"><span data-stu-id="2ed8e-129">If you want to enable all of Company-level access features plus InMail history, Notes history, and the InMail stub profile access, select **Contract-level access**.</span></span>

10. <span data-ttu-id="2ed8e-130">Zapněte požadovanou úroveň přístupu z nastavení **Admin ATS** programu LinkedIn Recruiter.</span><span class="sxs-lookup"><span data-stu-id="2ed8e-130">Turn on the desired access level from your LinkedIn Recruiter **Admin-ATS** settings.</span></span>

<span data-ttu-id="2ed8e-131">[![Zapnutí integrace aplikace Attract ze zobrazení pro správu proramu LinkedIn Recruiter](./media/EnableRSC.png)](./media/EnableRSC.png)</span><span class="sxs-lookup"><span data-stu-id="2ed8e-131">[![Turn on Attract integration from LinkedIn Recruiter Admin view](./media/EnableRSC.png)](./media/EnableRSC.png)</span></span>

12. <span data-ttu-id="2ed8e-132">Přejděte zpět na nastavení pro správu jako správce Attract a vyberte kartu **Integrace LinkedIn**. Měli byste vidět vytížení miniaplikace LinkedIn načíst zobrazující možnost **povoleno** se zapnutou vybranou úrovní přístupu.</span><span class="sxs-lookup"><span data-stu-id="2ed8e-132">Go back to Attract Admin Settings as an AttractAdmin and select the **LinkedIn integration** tab. You should now see the LinkedIn widget load showing **Enabled** with the selected access level turned on.</span></span>

<span data-ttu-id="2ed8e-133">[![Dokončená integrace programu LinkedIn Recruiter](./media/RSCSetupComplete.png)](./media/RSCSetupComplete.png)</span><span class="sxs-lookup"><span data-stu-id="2ed8e-133">[![LinkedIn Recruiter integration complete](./media/RSCSetupComplete.png)](./media/RSCSetupComplete.png)</span></span>

## <a name="using-linkedin-recruiter-capabilities"></a><span data-ttu-id="2ed8e-134">Použití možností webu LinkedIn Recruiter</span><span class="sxs-lookup"><span data-stu-id="2ed8e-134">Using LinkedIn Recruiter capabilities</span></span>

<span data-ttu-id="2ed8e-135">Poté, co správce systému Attract povolí možnosti programu LinkedIn Recruiter, je program k dispozici pro přístup manažerům náboru a náborářům.</span><span class="sxs-lookup"><span data-stu-id="2ed8e-135">After LinkedIn Recruiter capabilities has been enabled by the Attract Admin it is available for hiring managers and recruiters to access.</span></span> <span data-ttu-id="2ed8e-136">Pokud chcete tyto možnosti použít, připojte se k účtu LinkedIn v části **uživatelská nastavení**.</span><span class="sxs-lookup"><span data-stu-id="2ed8e-136">To use these capabilities, connect your LinkedIn account under **User Settings**.</span></span> <span data-ttu-id="2ed8e-137">Poté, co byla připojena nastavení správce a uživatele, bude k dispozici několik možností.</span><span class="sxs-lookup"><span data-stu-id="2ed8e-137">Several capabilities will be available after both the Admin and User settings have been connected.</span></span>

### <a name="in-ats-profile-widget"></a><span data-ttu-id="2ed8e-138">Miniaplikace In-ATS profile</span><span class="sxs-lookup"><span data-stu-id="2ed8e-138">In-ATS profile widget</span></span>

<span data-ttu-id="2ed8e-139">V systému Attract můžete zobrazit profil LinkedIn uchazeče.</span><span class="sxs-lookup"><span data-stu-id="2ed8e-139">You can view the candidate’s LinkedIn profile in Attract.</span></span> <span data-ttu-id="2ed8e-140">Miniaplikace LinkedIn zobrazí profil uchazeče, když informace ATS odpovídá informacím o webu LinkedIn uživatelů.</span><span class="sxs-lookup"><span data-stu-id="2ed8e-140">The LinkedIn widget will display the candidate profile when the ATS information matches the LinkedIn information of its users.</span></span>

<span data-ttu-id="2ed8e-141">Pokud chcete zobrazit profil, přejděte na profil uchazeče z pracovní pozice nebo fondu talentů.</span><span class="sxs-lookup"><span data-stu-id="2ed8e-141">To view a profile, go the candidate profile either from a job or talent pool.</span></span> <span data-ttu-id="2ed8e-142">V profilu uchazeče vyberte kartu **LinkedIn** a načte se miniaplikace profilu.</span><span class="sxs-lookup"><span data-stu-id="2ed8e-142">In the candidate profile, select the **LinkedIn** tab and the profile widget will load.</span></span> <span data-ttu-id="2ed8e-143">Její pomocí určete zda se jedná o shodu.</span><span class="sxs-lookup"><span data-stu-id="2ed8e-143">Using the profile widget, indicate if this is the correct match.</span></span> <span data-ttu-id="2ed8e-144">Pokud tomu tak není, najděte správnou osobu.</span><span class="sxs-lookup"><span data-stu-id="2ed8e-144">If it is not, find the correct person.</span></span> <span data-ttu-id="2ed8e-145">Z této stránky lze také uložit uchazeče do projektů LinkedIn Recruiter.</span><span class="sxs-lookup"><span data-stu-id="2ed8e-145">You can also save the candidate to your LinkedIn Recruiter projects from this page.</span></span>

### <a name="1-click-export"></a><span data-ttu-id="2ed8e-146">1-Klikněte na Exportovat.</span><span class="sxs-lookup"><span data-stu-id="2ed8e-146">1-click export</span></span> 

<span data-ttu-id="2ed8e-147">Při vybírání uchazečů ve službě LinkedIn můžete 1 kliknutím exportovat uchazeče do pracovních míst, která máte v současné době otevřená.</span><span class="sxs-lookup"><span data-stu-id="2ed8e-147">While sourcing candidates in LinkedIn, you can 1-click export the candidate to the jobs that you currently have open.</span></span> <span data-ttu-id="2ed8e-148">Proveďte následující kroky pro export 1 kliknutím.</span><span class="sxs-lookup"><span data-stu-id="2ed8e-148">Complete the following steps for a 1-click export.</span></span> <span data-ttu-id="2ed8e-149">Před dokončením těchto kroků ověřte, zda je vám přiřazená role manažera náboru nebo náboráře pro danou pracovní pozici a zda je pozice ve fázi **Potenciální zákazník**.</span><span class="sxs-lookup"><span data-stu-id="2ed8e-149">Before you complete these steps, verify that you are a assigned the role of Hiring manager or Recruiter for the job and that the job has a **Prospect** stage.</span></span>

1.  <span data-ttu-id="2ed8e-150">Vytvořte pozici, přiřaďte příslušné role a aktivujte pracovní pozici.</span><span class="sxs-lookup"><span data-stu-id="2ed8e-150">Create the job, assign the appropriate roles, and activate the job.</span></span>

2.  <span data-ttu-id="2ed8e-151">Po aktivaci pracovního místa přejděte do programu LinkedIn Recruiter.</span><span class="sxs-lookup"><span data-stu-id="2ed8e-151">When the job is activated, navigate to LinkedIn Recruiter.</span></span>

3.  <span data-ttu-id="2ed8e-152">Vyhledejte hledaného uchazeče a přejděte do jeho profilu.</span><span class="sxs-lookup"><span data-stu-id="2ed8e-152">Find the candidate that you are looking for and go to their profile.</span></span>

4.  <span data-ttu-id="2ed8e-153">Pomocí vyhledávacího pole na kartě kontaktu vyhledejte pracovní místo pomocí názvu nebo ID pracovního místa, které bylo aktivováno v systému Attract.</span><span class="sxs-lookup"><span data-stu-id="2ed8e-153">Using the job search box in the contact card, find the job using the title or the Job ID that was activated in Attract.</span></span> <span data-ttu-id="2ed8e-154">Pokud pracovní místo nenajdete, klikněte na tlačítko **Změnit ATS** k vyhledání správné instance Attract.</span><span class="sxs-lookup"><span data-stu-id="2ed8e-154">If you don’t find the job, click **Change ATS** to find the correct Attract instance.</span></span>

5. <span data-ttu-id="2ed8e-155">Po výběru pracovního místa klikněte na tlačítko **exportovat**.</span><span class="sxs-lookup"><span data-stu-id="2ed8e-155">After the job is selected, click **Export**.</span></span> <span data-ttu-id="2ed8e-156">Aplikace Attract nyní vyhledá uchazeče.</span><span class="sxs-lookup"><span data-stu-id="2ed8e-156">The candidate is now fetched by Attract.</span></span>

6.  <span data-ttu-id="2ed8e-157">Přejděte do aplikace Attract a otevřete příslušné pracovní místo.</span><span class="sxs-lookup"><span data-stu-id="2ed8e-157">Go to Attract and open the respective job.</span></span> <span data-ttu-id="2ed8e-158">Uchazeče, kterého jste právě exportovali, najdete ve fázi **Potenciální zákazník** v pracovní pozici.</span><span class="sxs-lookup"><span data-stu-id="2ed8e-158">You will find the candidate that you just exported in the **Prospect** stage of the job.</span></span>

### <a name="in-ats-indicator"></a><span data-ttu-id="2ed8e-159">Indikátor In-ATS</span><span class="sxs-lookup"><span data-stu-id="2ed8e-159">In-ATS indicator</span></span> 

<span data-ttu-id="2ed8e-160">Pomocí systému LinkedIn Recruiter můžete sledovat, zda uchazeč žádal o jiná pracovní místa ve vaší organizaci, podívat se, kde se nachází v různých fází žádostí o pracovní pozici, a zobrazit zpětnou vazbu a komentáře z aplikace Attract v programu LinkedIn Recruiter.</span><span class="sxs-lookup"><span data-stu-id="2ed8e-160">Using LinkedIn recruiter, you can track whether a candidate has applied to other jobs in your organization, look at where they are in different stages of job applications, and view the feedback and comments from Attract in LinkedIn Recruiter.</span></span>

1.  <span data-ttu-id="2ed8e-161">Otevřete LinkedIn Recruiter a vyhledejte profil uchazeče, který hledáte.</span><span class="sxs-lookup"><span data-stu-id="2ed8e-161">Open LinkedIn Recruiter and locate the candidate profile that you are looking for.</span></span>

2.  <span data-ttu-id="2ed8e-162">Přejděte dolů k zobrazení oddílu **In-ATS** v profilu uchazeče.</span><span class="sxs-lookup"><span data-stu-id="2ed8e-162">Scroll down to view the **In-ATS** section on the candidate’s profile.</span></span>

3.  <span data-ttu-id="2ed8e-163">Tento miniaplikace slouží k zobrazení všech informací o uchazeči, které jsou k dispozici v aplikaci Attract ze zobrazení LinkedIn Recruiter.</span><span class="sxs-lookup"><span data-stu-id="2ed8e-163">You can use this widget to view all of the information about the candidate that’s present in Attract from within the LinkedIn Recruiter view.</span></span>

4.  <span data-ttu-id="2ed8e-164">Vyberte kartu **Pracovní místa a stavy** k zobrazení pracovních míst, která jsou součástí nejnovějšího stavu, a způsb, jakým se pohybovala proti jednotlivým pracovním místům.</span><span class="sxs-lookup"><span data-stu-id="2ed8e-164">Select the **Jobs & Statuses** tab to see jobs they are part of, the latest status, and how they have been moving against each job.</span></span>

5.  <span data-ttu-id="2ed8e-165">Vyberte kartu **Zpětná vazba z pohovoru** k zobrazení zpětné vazby, kterou vedoucí pohovorů zaslali do systému Attract.</span><span class="sxs-lookup"><span data-stu-id="2ed8e-165">Select the **Interview Feedback** tab to see feedback that the interviewers have submitted in Attract.</span></span>

6.  <span data-ttu-id="2ed8e-166">Výběrem karty **Poznámky** zobrazte poznámky, které byly zachyceny pro tohoto uchazeče v aplikaci Attract.</span><span class="sxs-lookup"><span data-stu-id="2ed8e-166">Select the **Notes** tab to see notes that have been captured for this applicant in Attract.</span></span>

### <a name="inmail-history"></a><span data-ttu-id="2ed8e-167">Historie InMail</span><span class="sxs-lookup"><span data-stu-id="2ed8e-167">InMail history</span></span>

<span data-ttu-id="2ed8e-168">Historie webu LinkedIn InMail je v programu LinkedIn Recruiter dostupná s přístupem na úrovni smlouvy.</span><span class="sxs-lookup"><span data-stu-id="2ed8e-168">The LinkedIn InMail history is available with contract-level access with LinkedIn Recruiter.</span></span> <span data-ttu-id="2ed8e-169">Pokud tato možnost povolena, můžete zobrazit celou historii InMail s uchazečem.</span><span class="sxs-lookup"><span data-stu-id="2ed8e-169">When it is enabled, you can view your entire InMail history with the candidate.</span></span> <span data-ttu-id="2ed8e-170">Můžete se také podívat, kdo další z vaší organizace si vyměňoval InMail s uchazečem, nemůžete však zobrazit zprávy, které si zasílali.</span><span class="sxs-lookup"><span data-stu-id="2ed8e-170">You can also see who else from your organization has exchanged InMail with the candidate, however you can't view the messages between them.</span></span>

<span data-ttu-id="2ed8e-171">Pokud chcete zobrazit historii InMail, přejděte na kartu **LinkedIn** a přejděte do spodní části stránky a zobrazte historii.</span><span class="sxs-lookup"><span data-stu-id="2ed8e-171">To view InMail history, go to a candidate’s profile, go to the **LinkedIn** tab and scroll to the bottom of the page to view the history.</span></span> <span data-ttu-id="2ed8e-172">Můžete zobrazit historii InMail pouze v případě, že uchazeč odpověděl na vaši žádost a rozhodl se nasdílet s vámi svůj profil ve službě LinkedIn.</span><span class="sxs-lookup"><span data-stu-id="2ed8e-172">You can view the InMail history only if the candidate has responded to your request and chosen to share their profile with you in LinkedIn.</span></span> <span data-ttu-id="2ed8e-173">Zprávy z InMail se každých několik hodin synchronizují s aplikací Attract.</span><span class="sxs-lookup"><span data-stu-id="2ed8e-173">The messages from InMail sync with Attract every couple of hours.</span></span>

### <a name="notes-history"></a><span data-ttu-id="2ed8e-174">Historie poznámek</span><span class="sxs-lookup"><span data-stu-id="2ed8e-174">Notes history</span></span> 

<span data-ttu-id="2ed8e-175">Historie poznámek LinkedIn je v programu LinkedIn Recruiter dostupná s přístupem na úrovni smlouvy.</span><span class="sxs-lookup"><span data-stu-id="2ed8e-175">The LinkedIn notes history is available with contract-level access with LinkedIn Recruiter.</span></span> <span data-ttu-id="2ed8e-176">Pokud je to povoleno, můžete zobrazit poznámky, které byly zachyceny o uchazeči podle různých náborářů z vaší organizace.</span><span class="sxs-lookup"><span data-stu-id="2ed8e-176">When it is enabled, you can view the notes that have been captured about the candidate by different recruiters from your organization.</span></span>

<span data-ttu-id="2ed8e-177">Pokud chcete zobrazit historii poznámek, přejděte na kartu **LinkedIn** a přejděte do spodní části stránky a zobrazte historii.</span><span class="sxs-lookup"><span data-stu-id="2ed8e-177">To view Notes history, go to a candidate’s profile, go to the **LinkedIn** tab and scroll to the bottom of the page to view the history.</span></span> <span data-ttu-id="2ed8e-178">Můžete zobrazit všechny poznámky o uchazeči z webu LinkedIn Recruiter.</span><span class="sxs-lookup"><span data-stu-id="2ed8e-178">You can view all the notes about the candidate from LinkedIn Recruiter.</span></span>

### <a name="inmail-stub-profile"></a><span data-ttu-id="2ed8e-179">Profil InMail se zakázaným inzerováním</span><span class="sxs-lookup"><span data-stu-id="2ed8e-179">InMail stub profile</span></span>

<span data-ttu-id="2ed8e-180">Profil InMail se zakázaným inzerováním je v programu LinkedIn Recruiter dostupný s přístupem na úrovni smlouvy.</span><span class="sxs-lookup"><span data-stu-id="2ed8e-180">The InMail stub profile is available with contract-level access with LinkedIn Recruiter.</span></span> <span data-ttu-id="2ed8e-181">Pokud uchazeči souhlasí se sdílením svých profilů LinkedIn s libovolným uživatelem ve vaší organizaci, můžete sledovat uchazeče v aplikaci Attract a pro každého uchazeče se vytvoří nový záznam uchazeče.</span><span class="sxs-lookup"><span data-stu-id="2ed8e-181">If candidates agree to share their LinkedIn profiles with any user in your organization, you can track the candidates in Attract and a new candidate record will be created for each candidate.</span></span>

<span data-ttu-id="2ed8e-182">Chcete-li zobrazit seznam uchazečů, přejděte na **Fondy talentů**, aby se zobrazil fond talentů LinkedIn vytvořený systémem.</span><span class="sxs-lookup"><span data-stu-id="2ed8e-182">To view the list of candidates, go to **Talent pools** to see a system-created LinkedIn talent pool.</span></span> <span data-ttu-id="2ed8e-183">Tento fond talentů obsahuje seznam uchazečů a jejich profily se zakázaným inzerováním z webu LinkedIn, zobrazující křestní jméno a příjmení uchazeče.</span><span class="sxs-lookup"><span data-stu-id="2ed8e-183">This talent pool contains the list candidates and their stub profiles as received from LinkedIn, showing the candidate's first name and last name.</span></span> <span data-ttu-id="2ed8e-184">ID e-mailu uchazeče se zobrazí, pokud uchazeč nastavil sdílení své e-mailové adresy.</span><span class="sxs-lookup"><span data-stu-id="2ed8e-184">The candidate’s email ID will be displayed if the candidate had chosen to share their email address.</span></span>

