---
title: Zdroje pomocí LinkedIn Recruiter
description: Toto téma obsahuje informace o používání strojového učení pro získání doporučení práce a uchazeče o práci.
author: andreabichsel
manager: AnnBe
ms.date: 12/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.search.industry: ''
ms.author: anbichse
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 4ac7a302e5bf589beb2b560b0ff5818e90c67139
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/19/2019
ms.locfileid: "859567"
---
# <a name="sourcing-with-linkedin-recruiter"></a><span data-ttu-id="b25a5-103">Zdroje pomocí LinkedIn Recruiter</span><span class="sxs-lookup"><span data-stu-id="b25a5-103">Sourcing with LinkedIn Recruiter</span></span>
[!include[banner](../includes/banner.md)]

<span data-ttu-id="b25a5-104">LinkedIn je největší databáze talentů na světě a často slouží jako primární systém, který náboráři používají k vyhledávání, komunikaci a zajišťování zdrojů uchazečů o pracovní pozice, které chtějí náboráři obsadit.</span><span class="sxs-lookup"><span data-stu-id="b25a5-104">LinkedIn is the world’s largest talent database and often the primary system that recruiters use to find, communicate with, and source candidates for the jobs that recruiters are looking to fill.</span></span> <span data-ttu-id="b25a5-105">Integrace programu LinkedIn Recruiter s aplikací Dynamics 365 for Talent: Attract uživatelům usnadňuje nábor a udržování synchronizace dat mezi dvěma systémy.</span><span class="sxs-lookup"><span data-stu-id="b25a5-105">LinkedIn Recruiter integration with Dynamics 365 for Talent: Attract makes it easier for users to hire, and to keep the data in sync between the two systems.</span></span>

> [!NOTE]
> <span data-ttu-id="b25a5-106">Aby bylo možné používat integraci programu LinkedIn Recruiter s aplikací Attract, je potřeba doplněk Comprehensive hiring a licence LinkedIn Recruiter.</span><span class="sxs-lookup"><span data-stu-id="b25a5-106">You need the Comprehensive hiring add-on and LinkedIn Recruiter seats to be able to use LinkedIn Recruiter integration with Attract.</span></span>

## <a name="set-up-linkedin-recruiter-with-attract"></a><span data-ttu-id="b25a5-107">Nastavení programu LinkedIn Recruiter s aplikací Attract</span><span class="sxs-lookup"><span data-stu-id="b25a5-107">Set up LinkedIn Recruiter with Attract</span></span> 

<span data-ttu-id="b25a5-108">Než budete moci využívat program LinkedIn Recruiter, musíte nakonfigurovat přístup na úrovni smlouvy nebo společnosti s instancí aplikace Attract.</span><span class="sxs-lookup"><span data-stu-id="b25a5-108">Before you can use the LinkedIn Recruiter capabilities, you must configure contract-level or company-level access with your Attract instance.</span></span> <span data-ttu-id="b25a5-109">Pro dokončení procesu konfigurace musíte spolupracovat s uživatelem, který je správce vaší smlouvy o programu LinkedIn Recruiter.</span><span class="sxs-lookup"><span data-stu-id="b25a5-109">To complete the configuration process, you must work with the user who is an Admin on your LinkedIn Recruiter contract.</span></span> <span data-ttu-id="b25a5-110">Pomocí následujících kroků nakonfigurujte LinkedIn Recruiter s aplikací Attract.</span><span class="sxs-lookup"><span data-stu-id="b25a5-110">Complete the following steps to configure LinkedIn Recruiter with Attract.</span></span>

1.  <span data-ttu-id="b25a5-111">Přihlaste se k aplikaci Attract jako správce a přejděte na **nastavení pro správu**.</span><span class="sxs-lookup"><span data-stu-id="b25a5-111">Sign in to Attract as an Admin and go to **Admin Settings**.</span></span>

2.  <span data-ttu-id="b25a5-112">V levém podokně klikněte na kartu **Integrace LinkedIn**.</span><span class="sxs-lookup"><span data-stu-id="b25a5-112">On the left pane, click the **LinkedIn Integration** tab.</span></span>

<span data-ttu-id="b25a5-113">[![Zobrazení správce aplikace Attract ke spuštění integrace s programem LinkedIn Recruiter](./media/LinkedInConnect.png)](./media/LinkedInConnect.png)</span><span class="sxs-lookup"><span data-stu-id="b25a5-113">[![Attract Admin view to start LinkedIn Recruiter integration](./media/LinkedInConnect.png)](./media/LinkedInConnect.png)</span></span>

3.  <span data-ttu-id="b25a5-114">Klikněte na tlačítko **připojit** pro spuštění nastavení. Budete provedeni procesem registrace LinkedIn.</span><span class="sxs-lookup"><span data-stu-id="b25a5-114">Click **Connect** to start the setup and be guided through the LinkedIn sign-in process.</span></span>

4.  <span data-ttu-id="b25a5-115">Pokud máte licence na více smluv LinkedIn, vyberte smlouvu, kterou chcete spojit se systémem Attract.</span><span class="sxs-lookup"><span data-stu-id="b25a5-115">If you have seats on multiple LinkedIn contracts, select the contract that you would like to connect to the Attract system.</span></span> <span data-ttu-id="b25a5-116">Pokud máte licenci jenom v rámci jedné smlouvy LinkedIn, tento krok není potřeba.</span><span class="sxs-lookup"><span data-stu-id="b25a5-116">If you have a seat on only one LinkedIn contract, this step will not be needed.</span></span>

5.  <span data-ttu-id="b25a5-117">V nastavení pro správu se nyní načte miniaplikace LinkedIn se seznamem integrací.</span><span class="sxs-lookup"><span data-stu-id="b25a5-117">The LinkedIn widget will now load in your Admin settings with the list of integrations shown.</span></span> <span data-ttu-id="b25a5-118">Ve skupinovém rámečku **připojení systému Recruiter** klikněte na tlačítko **Požadavek**.</span><span class="sxs-lookup"><span data-stu-id="b25a5-118">Under **Recruiter System connect**, click **Request**.</span></span>

<span data-ttu-id="b25a5-119">[![Zobrazení správce aplikace Attract k vyžádání integrace s programem LinkedIn Recruiter](./media/RequestLinkedInRSC.png)](./media/RequestLinkedInRSC.png)</span><span class="sxs-lookup"><span data-stu-id="b25a5-119">[![Attract Admin view to Request LinkedIn Recruiter integration](./media/RequestLinkedInRSC.png)](./media/RequestLinkedInRSC.png)</span></span>

6.  <span data-ttu-id="b25a5-120">Po vyžádání integrace ze systému Attract se zobrazí jako **Připraveno pro partnera** a dá se zapnout z **nastavení správy systému Recruiter**.</span><span class="sxs-lookup"><span data-stu-id="b25a5-120">After the integration is requested from Attract, it will show as **Partner ready** and is ready to be turned on from **Recruiter Admin settings**.</span></span> <span data-ttu-id="b25a5-121">Pokud a této stránce vidíte také možnost **Upozornit partnera**, počkejte chvíli, klikněte na tlačítko **Upozornit partnera** a poté stránku aktualizujte.</span><span class="sxs-lookup"><span data-stu-id="b25a5-121">If you see **Notify partner** on this page, wait a few seconds, click **Notify partner**, and then refresh the page.</span></span> <span data-ttu-id="b25a5-122">Nyní by se měla zobrazovat jako **připravená pro partnera**.</span><span class="sxs-lookup"><span data-stu-id="b25a5-122">It should now show as **Partner ready**.</span></span>

<span data-ttu-id="b25a5-123">[![Zobrazení správce systému Attract k označení strany požadavků Attract, které byly dokončeny.](./media/PartnerReadyRSC.png)](./media/PartnerReadyRSC.png)</span><span class="sxs-lookup"><span data-stu-id="b25a5-123">[![Attract Admin view to indicate Attract side of requests have been completed](./media/PartnerReadyRSC.png)](./media/PartnerReadyRSC.png)</span></span>

<span data-ttu-id="b25a5-124">Pokud chcete dokončit další krok, musíte mít oprávnění správce smluv LinkedIn Recruiter.</span><span class="sxs-lookup"><span data-stu-id="b25a5-124">To complete the next step, you need to have an Admin privilege on your LinkedIn Recruiter Contract.</span></span>

7.  <span data-ttu-id="b25a5-125">Přihaste se k webu LinkedIn pomocí účtu správce a přejděte na web LinkedIn Recruiter vpravo nahoře.</span><span class="sxs-lookup"><span data-stu-id="b25a5-125">Sign in to LinkedIn using the Admin account and go to LinkedIn Recruiter on the top right.</span></span> 

8. <span data-ttu-id="b25a5-126">V nabídce **Další** v horní části obrazovky klikněte na **nastavení pro správu** a potom klikněte na kartu **ATS**.</span><span class="sxs-lookup"><span data-stu-id="b25a5-126">On the **More** menu at the top of the screen, click **Admin Settings**, and then click the **ATS** Tab.</span></span>

<span data-ttu-id="b25a5-127">Systém Attract bude uveden s několika možnostmi, které lze zapnout.</span><span class="sxs-lookup"><span data-stu-id="b25a5-127">The Attract system will be listed with a couple of options that can be turned on.</span></span>

9. <span data-ttu-id="b25a5-128">Pokud chcete povolit export pouze 1-kliknutím pro **indikátor In-ATS** a **miniaplikaci In-ATS profil**, vyberte **přístup na úrovni společnosti**.</span><span class="sxs-lookup"><span data-stu-id="b25a5-128">If you want to enable only 1-Click export for the **In-ATS indicator** and the **In-ATS Profile Widget**, select **Company-level access**.</span></span> <span data-ttu-id="b25a5-129">Pokud chcete povolit všechny funkce přístupu na úrovni společnosti plus historii InMail a přístupu neúplného profilu InMail, vyberte **Přístup na úrovni smlouvy**.</span><span class="sxs-lookup"><span data-stu-id="b25a5-129">If you want to enable all of Company-level access features plus InMail history, Notes history, and the InMail stub profile access, select **Contract-level access**.</span></span>

10. <span data-ttu-id="b25a5-130">Zapněte požadovanou úroveň přístupu z nastavení LinkedIn Recruiter **Admin-ATS**.</span><span class="sxs-lookup"><span data-stu-id="b25a5-130">Turn on the desired access level from your LinkedIn Recruiter **Admin-ATS** settings.</span></span>

<span data-ttu-id="b25a5-131">[![Zapnutí integrace aplikace Attract ze zobrazení pro správu programu LinkedIn Recruiter](./media/EnableRSC.png)](./media/EnableRSC.png)</span><span class="sxs-lookup"><span data-stu-id="b25a5-131">[![Turn on Attract integration from LinkedIn Recruiter Admin view](./media/EnableRSC.png)](./media/EnableRSC.png)</span></span>

12. <span data-ttu-id="b25a5-132">Přejděte zpět na nastavení pro správu jako správce Attract a vyberte kartu **Integrace LinkedIn**. Měli byste vidět vytížení miniaplikace LinkedIn načíst zobrazující možnost **povoleno** se zapnutou vybranou úrovní přístupu.</span><span class="sxs-lookup"><span data-stu-id="b25a5-132">Go back to Attract Admin Settings as an AttractAdmin and select the **LinkedIn integration** tab. You should now see the LinkedIn widget load showing **Enabled** with the selected access level turned on.</span></span>

<span data-ttu-id="b25a5-133">[![Dokončení integrace LinkedIn Recruiter](./media/RSCSetupComplete.png)](./media/RSCSetupComplete.png)</span><span class="sxs-lookup"><span data-stu-id="b25a5-133">[![LinkedIn Recruiter integration complete](./media/RSCSetupComplete.png)](./media/RSCSetupComplete.png)</span></span>

## <a name="using-linkedin-recruiter-capabilities"></a><span data-ttu-id="b25a5-134">Použití dovedností LinkedIn Recruiter</span><span class="sxs-lookup"><span data-stu-id="b25a5-134">Using LinkedIn Recruiter capabilities</span></span>

<span data-ttu-id="b25a5-135">Poté, co správce systému Attract povolí možnosti programu LinkedIn Recruiter, je program k dispozici pro přístup manažerům náboru a náborářům.</span><span class="sxs-lookup"><span data-stu-id="b25a5-135">After LinkedIn Recruiter capabilities has been enabled by the Attract Admin it is available for hiring managers and recruiters to access.</span></span> <span data-ttu-id="b25a5-136">Pokud chcete tyto možnosti použít, připojte se k účtu LinkedIn v části **uživatelská nastavení**.</span><span class="sxs-lookup"><span data-stu-id="b25a5-136">To use these capabilities, connect your LinkedIn account under **User Settings**.</span></span> <span data-ttu-id="b25a5-137">Poté, co byla připojena nastavení správce a uživatele, bude k dispozici několik možností.</span><span class="sxs-lookup"><span data-stu-id="b25a5-137">Several capabilities will be available after both the Admin and User settings have been connected.</span></span>

### <a name="in-ats-profile-widget"></a><span data-ttu-id="b25a5-138">Miniaplikace In-ATS profile</span><span class="sxs-lookup"><span data-stu-id="b25a5-138">In-ATS profile widget</span></span>

<span data-ttu-id="b25a5-139">V systému Attract můžete zobrazit profil LinkedIn uchazeče.</span><span class="sxs-lookup"><span data-stu-id="b25a5-139">You can view the candidate’s LinkedIn profile in Attract.</span></span> <span data-ttu-id="b25a5-140">Miniaplikace LinkedIn zobrazí profil uchazeče, když informace ATS odpovídá informacím o webu LinkedIn uživatelů.</span><span class="sxs-lookup"><span data-stu-id="b25a5-140">The LinkedIn widget will display the candidate profile when the ATS information matches the LinkedIn information of its users.</span></span>

<span data-ttu-id="b25a5-141">Pokud chcete zobrazit profil, přejděte na profil uchazeče z pracovní pozice nebo fondu talentů.</span><span class="sxs-lookup"><span data-stu-id="b25a5-141">To view a profile, go the candidate profile either from a job or talent pool.</span></span> <span data-ttu-id="b25a5-142">V profilu uchazeče vyberte kartu **LinkedIn** a načte se miniaplikace profilu.</span><span class="sxs-lookup"><span data-stu-id="b25a5-142">In the candidate profile, select the **LinkedIn** tab and the profile widget will load.</span></span> <span data-ttu-id="b25a5-143">Z této stránky lze také uložit uchazeče do projektů LinkedIn Recruiter.</span><span class="sxs-lookup"><span data-stu-id="b25a5-143">You can also save the candidate to your LinkedIn Recruiter projects from this page.</span></span>
1. <span data-ttu-id="b25a5-144">Pokud web LinkedIn nalezl shodu na základě e-mailu a ID člena LinkedIn (přesná shoda), zobrazí se profil uchazeče.</span><span class="sxs-lookup"><span data-stu-id="b25a5-144">If LinkedIn found the match based on email and LinkedIn member ID (exact match), the candidate's profile will be shown.</span></span> <span data-ttu-id="b25a5-145">Uživatel přesto má možnost připojit nebo odpojit profil.</span><span class="sxs-lookup"><span data-stu-id="b25a5-145">The user still has an option to link/unlink the profile.</span></span>

2. <span data-ttu-id="b25a5-146">Pokud webu LinkedIn nemůže najít uchazeče na základě jeho e-mailu nebo ID člena, zobrazí seznam možných shod uchazečů na základě jména uchazeče a uživatel si může některou vybrat a propojit profil.</span><span class="sxs-lookup"><span data-stu-id="b25a5-146">If LinkedIn cannot find the candidate based on their email or member ID, it will show a list of possible candidate matches based on candidate name and the user can choose one of them and link the profile.</span></span>  

3. <span data-ttu-id="b25a5-147">V případě, že web LinkedIn nemůže najít uchazeče podle jména, vrátí informaci, že nebyla nalezena shoda.</span><span class="sxs-lookup"><span data-stu-id="b25a5-147">If LinkedIn cannot find any candidate based on the name, it will return that no match was found.</span></span>

### <a name="1-click-export"></a><span data-ttu-id="b25a5-148">1-Klikněte na Exportovat.</span><span class="sxs-lookup"><span data-stu-id="b25a5-148">1-click export</span></span> 

<span data-ttu-id="b25a5-149">Při vybírání uchazečů ve službě LinkedIn můžete 1 kliknutím exportovat uchazeče do pracovních míst, která máte v současné době otevřená.</span><span class="sxs-lookup"><span data-stu-id="b25a5-149">While sourcing candidates in LinkedIn, you can 1-click export the candidate to the jobs that you currently have open.</span></span> <span data-ttu-id="b25a5-150">Proveďte následující kroky pro export 1 kliknutím.</span><span class="sxs-lookup"><span data-stu-id="b25a5-150">Complete the following steps for a 1-click export.</span></span> <span data-ttu-id="b25a5-151">Před dokončením těchto kroků ověřte, zda je vám přiřazená role manažera náboru nebo náboráře pro danou pracovní pozici a zda je pozice ve fázi **Potenciální zákazník**.</span><span class="sxs-lookup"><span data-stu-id="b25a5-151">Before you complete these steps, verify that you are a assigned the role of Hiring manager or Recruiter for the job and that the job has a **Prospect** stage.</span></span>

1.  <span data-ttu-id="b25a5-152">Vytvořte pozici, přiřaďte příslušné role a aktivujte pracovní pozici.</span><span class="sxs-lookup"><span data-stu-id="b25a5-152">Create the job, assign the appropriate roles, and activate the job.</span></span>

2.  <span data-ttu-id="b25a5-153">Po aktivaci pracovního místa přejděte do programu LinkedIn Recruiter.</span><span class="sxs-lookup"><span data-stu-id="b25a5-153">When the job is activated, navigate to LinkedIn Recruiter.</span></span>

3.  <span data-ttu-id="b25a5-154">Vyhledejte hledaného uchazeče a přejděte do jeho profilu.</span><span class="sxs-lookup"><span data-stu-id="b25a5-154">Find the candidate that you are looking for and go to their profile.</span></span>

4.  <span data-ttu-id="b25a5-155">Pomocí vyhledávacího pole na kartě kontaktu vyhledejte pracovní místo pomocí názvu nebo ID pracovního místa, které bylo aktivováno v systému Attract.</span><span class="sxs-lookup"><span data-stu-id="b25a5-155">Using the job search box in the contact card, find the job using the title or the Job ID that was activated in Attract.</span></span> <span data-ttu-id="b25a5-156">Pokud pracovní místo nenajdete, klikněte na tlačítko **Změnit ATS** k vyhledání správné instance Attract.</span><span class="sxs-lookup"><span data-stu-id="b25a5-156">If you don’t find the job, click **Change ATS** to find the correct Attract instance.</span></span>

5. <span data-ttu-id="b25a5-157">Po výběru pracovního místa klikněte na tlačítko **exportovat**.</span><span class="sxs-lookup"><span data-stu-id="b25a5-157">After the job is selected, click **Export**.</span></span> <span data-ttu-id="b25a5-158">Aplikace Attract nyní vyhledá uchazeče.</span><span class="sxs-lookup"><span data-stu-id="b25a5-158">The candidate is now fetched by Attract.</span></span>

6.  <span data-ttu-id="b25a5-159">Přejděte do aplikace Attract a otevřete příslušné pracovní místo.</span><span class="sxs-lookup"><span data-stu-id="b25a5-159">Go to Attract and open the respective job.</span></span> <span data-ttu-id="b25a5-160">Uchazeče, kterého jste právě exportovali, najdete ve fázi **Potenciální zákazník** v pracovní pozici.</span><span class="sxs-lookup"><span data-stu-id="b25a5-160">You will find the candidate that you just exported in the **Prospect** stage of the job.</span></span>

### <a name="in-ats-indicator"></a><span data-ttu-id="b25a5-161">Indikátor In-ATS</span><span class="sxs-lookup"><span data-stu-id="b25a5-161">In-ATS indicator</span></span> 

<span data-ttu-id="b25a5-162">Pomocí systému LinkedIn Recruiter můžete sledovat, zda uchazeč žádal o jiná pracovní místa ve vaší organizaci, podívat se, kde se nachází v různých fází žádostí o pracovní pozici, a zobrazit zpětnou vazbu a komentáře z aplikace Attract v programu LinkedIn Recruiter.</span><span class="sxs-lookup"><span data-stu-id="b25a5-162">Using LinkedIn recruiter, you can track whether a candidate has applied to other jobs in your organization, look at where they are in different stages of job applications, and view the feedback and comments from Attract in LinkedIn Recruiter.</span></span>

1.  <span data-ttu-id="b25a5-163">Otevřete LinkedIn Recruiter a vyhledejte profil uchazeče, který hledáte.</span><span class="sxs-lookup"><span data-stu-id="b25a5-163">Open LinkedIn Recruiter and locate the candidate profile that you are looking for.</span></span>

2.  <span data-ttu-id="b25a5-164">Přejděte dolů k zobrazení oddílu **In-ATS** v profilu uchazeče.</span><span class="sxs-lookup"><span data-stu-id="b25a5-164">Scroll down to view the **In-ATS** section on the candidate’s profile.</span></span>

3.  <span data-ttu-id="b25a5-165">Tento miniaplikace slouží k zobrazení všech informací o uchazeči, které jsou k dispozici v aplikaci Attract ze zobrazení LinkedIn Recruiter.</span><span class="sxs-lookup"><span data-stu-id="b25a5-165">You can use this widget to view all of the information about the candidate that’s present in Attract from within the LinkedIn Recruiter view.</span></span>

4.  <span data-ttu-id="b25a5-166">Vyberte kartu **Pracovní místa a stavy** k zobrazení pracovních míst, která jsou součástí nejnovějšího stavu, a způsb, jakým se pohybovala proti jednotlivým pracovním místům.</span><span class="sxs-lookup"><span data-stu-id="b25a5-166">Select the **Jobs & Statuses** tab to see jobs they are part of, the latest status, and how they have been moving against each job.</span></span>

5.  <span data-ttu-id="b25a5-167">Vyberte kartu **Zpětná vazba z pohovoru** k zobrazení zpětné vazby, kterou vedoucí pohovorů zaslali do systému Attract.</span><span class="sxs-lookup"><span data-stu-id="b25a5-167">Select the **Interview Feedback** tab to see feedback that the interviewers have submitted in Attract.</span></span>

6.  <span data-ttu-id="b25a5-168">Výběrem karty **Poznámky** zobrazte poznámky, které byly zachyceny pro tohoto uchazeče v aplikaci Attract.</span><span class="sxs-lookup"><span data-stu-id="b25a5-168">Select the **Notes** tab to see notes that have been captured for this applicant in Attract.</span></span>

> [!NOTE]
> <span data-ttu-id="b25a5-169">Údaje o uchazeči a žádosti se nebudou synchronizovat s programem LinkedIn Recruiter, pokud se uchazeč nedostal za fázi potenciálního zákazníka.</span><span class="sxs-lookup"><span data-stu-id="b25a5-169">Candidate and application data will not be synced to LinkedIn Recruiter if the candidate hasn't moved past the prospect stage.</span></span>

### <a name="inmail-history"></a><span data-ttu-id="b25a5-170">Historie InMail</span><span class="sxs-lookup"><span data-stu-id="b25a5-170">InMail history</span></span>

<span data-ttu-id="b25a5-171">Historie LinkedIn InMail je v programu LinkedIn Recruiter dostupná s přístupem na úrovni smlouvy.</span><span class="sxs-lookup"><span data-stu-id="b25a5-171">The LinkedIn InMail history is available with contract-level access with LinkedIn Recruiter.</span></span> <span data-ttu-id="b25a5-172">Pokud tato možnost povolena, můžete zobrazit celou historii InMail s uchazečem.</span><span class="sxs-lookup"><span data-stu-id="b25a5-172">When it is enabled, you can view your entire InMail history with the candidate.</span></span> <span data-ttu-id="b25a5-173">Můžete se také podívat, kdo další z vaší organizace si vyměňoval InMail s uchazečem, nemůžete však zobrazit zprávy, které si zasílali.</span><span class="sxs-lookup"><span data-stu-id="b25a5-173">You can also see who else from your organization has exchanged InMail with the candidate, however you can't view the messages between them.</span></span>

<span data-ttu-id="b25a5-174">Pokud chcete zobrazit historii InMail, přejděte na kartu **LinkedIn** a přejděte do spodní části stránky a zobrazte historii.</span><span class="sxs-lookup"><span data-stu-id="b25a5-174">To view InMail history, go to a candidate’s profile, go to the **LinkedIn** tab and scroll to the bottom of the page to view the history.</span></span> <span data-ttu-id="b25a5-175">Pokud jste vedli diskusi s uchazečem, můžete zobrazit historii InMail.</span><span class="sxs-lookup"><span data-stu-id="b25a5-175">You can view InMail history if you have had a discussion with the candidate.</span></span> <span data-ttu-id="b25a5-176">Zprávy z InMail se každých několik hodin synchronizují s aplikací Attract.</span><span class="sxs-lookup"><span data-stu-id="b25a5-176">The messages from InMail will sync with Attract every couple of hours.</span></span>

### <a name="notes-history"></a><span data-ttu-id="b25a5-177">Historie poznámek</span><span class="sxs-lookup"><span data-stu-id="b25a5-177">Notes history</span></span> 

<span data-ttu-id="b25a5-178">Historie poznámek je v programu LinkedIn Recruiter dostupná s přístupem na úrovni smlouvy.</span><span class="sxs-lookup"><span data-stu-id="b25a5-178">The LinkedIn notes history is available with contract-level access with LinkedIn Recruiter.</span></span> <span data-ttu-id="b25a5-179">Pokud je to povoleno, můžete zobrazit poznámky, které byly zachyceny o uchazeči podle různých náborářů z vaší organizace.</span><span class="sxs-lookup"><span data-stu-id="b25a5-179">When it is enabled, you can view the notes that have been captured about the candidate by different recruiters from your organization.</span></span>

<span data-ttu-id="b25a5-180">Pokud chcete zobrazit historii poznámek, přejděte na kartu **LinkedIn** a přejděte do spodní části stránky a zobrazte historii.</span><span class="sxs-lookup"><span data-stu-id="b25a5-180">To view Notes history, go to a candidate’s profile, go to the **LinkedIn** tab and scroll to the bottom of the page to view the history.</span></span> <span data-ttu-id="b25a5-181">Můžete zobrazit všechny poznámky o uchazeči z webu LinkedIn Recruiter.</span><span class="sxs-lookup"><span data-stu-id="b25a5-181">You can view all the notes about the candidate from LinkedIn Recruiter.</span></span>

### <a name="inmail-stub-profile"></a><span data-ttu-id="b25a5-182">Profil InMail se zakázaným inzerováním</span><span class="sxs-lookup"><span data-stu-id="b25a5-182">InMail stub profile</span></span>

<span data-ttu-id="b25a5-183">Profil InMail se zakázaným inzerováním je v programu LinkedIn Recruiter dostupný s přístupem na úrovni smlouvy.</span><span class="sxs-lookup"><span data-stu-id="b25a5-183">The InMail stub profile is available with contract-level access with LinkedIn Recruiter.</span></span> <span data-ttu-id="b25a5-184">Pokud uchazeči souhlasí se sdílením svých profilů LinkedIn s libovolným uživatelem ve vaší organizaci, můžete sledovat uchazeče v aplikaci Attract a pro každého uchazeče se vytvoří nový záznam uchazeče.</span><span class="sxs-lookup"><span data-stu-id="b25a5-184">If candidates agree to share their LinkedIn profiles with any user in your organization, you can track the candidates in Attract and a new candidate record will be created for each candidate.</span></span> <span data-ttu-id="b25a5-185">Pokud uchazeč existuje v systému a má e-mailovou adresu nebo se rozhodl sdílet adresu s náborářem, můžete zobrazit jeho e-mailovou adresu.</span><span class="sxs-lookup"><span data-stu-id="b25a5-185">You can view candidate's email address if the candidate already exists in the system with an email address or has chosen to share their address with the recruiter.</span></span>

<span data-ttu-id="b25a5-186">Chcete-li zobrazit seznam uchazečů, přejděte na **Fondy talentů**, aby se zobrazil fond talentů LinkedIn vytvořený systémem.</span><span class="sxs-lookup"><span data-stu-id="b25a5-186">To view the list of candidates, go to **Talent pools** to see a system-created LinkedIn talent pool.</span></span> <span data-ttu-id="b25a5-187">Tento fond talentů obsahuje seznam uchazečů a jejich profily se zakázaným inzerováním z webu LinkedIn, zobrazující křestní jméno a příjmení uchazeče.</span><span class="sxs-lookup"><span data-stu-id="b25a5-187">This talent pool contains the list candidates and their stub profiles as received from LinkedIn, showing the candidate's first name and last name.</span></span> <span data-ttu-id="b25a5-188">ID e-mailu uchazeče se zobrazí, pokud uchazeč nastavil sdílení své e-mailové adresy.</span><span class="sxs-lookup"><span data-stu-id="b25a5-188">The candidate’s email ID will be displayed if the candidate had chosen to share their email address.</span></span>
