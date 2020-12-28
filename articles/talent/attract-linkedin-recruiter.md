---
title: Zdrojování kandidátů pomocí LinkedIn Recruiter v aplikaci Attract
description: Použijte integraci LinkedIn poskytovanou aplikací Microsoft Dynamics 365 Talent - Attract ke zdrojování uchazečů o zaměstnání pomocí LinkedIn Recruiter.
author: andreabichsel
manager: AnnBe
ms.date: 08/31/2020
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
ms.openlocfilehash: 96e4660c4958bf5f2a0910bfad770e1e713f800f
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528262"
---
# <a name="source-candidates-with-linkedin-recruiter-in-attract"></a><span data-ttu-id="db087-103">Zdrojování kandidátů pomocí LinkedIn Recruiter v aplikaci Attract</span><span class="sxs-lookup"><span data-stu-id="db087-103">Source candidates with LinkedIn Recruiter in Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="db087-104">LinkedIn je nejvyšší světová síť profesionálů, která poskytuje přístup k nejlepším talentům.</span><span class="sxs-lookup"><span data-stu-id="db087-104">LinkedIn is the world's largest online professional network, giving you access to the world's top talent.</span></span> <span data-ttu-id="db087-105">Microsoft Dynamics 365 Talent: Attract vám umožní zdrojovat kandidáty přímo z LinkedIn.</span><span class="sxs-lookup"><span data-stu-id="db087-105">Microsoft Dynamics 365 Talent: Attract lets you source candidates directly from LinkedIn.</span></span> <span data-ttu-id="db087-106">Proto je snazší než kdykoli dříve najít talenty, které potřebujete k obsazení otevřených pozic.</span><span class="sxs-lookup"><span data-stu-id="db087-106">Therefore, it's easier than ever to find the talent that you need to fill your open positions.</span></span> <span data-ttu-id="db087-107">Po nastavení připojení k LinkedIn prostřednictvím Attract můžete zobrazit potenciální kandidáty na LinkedIn a exportovat je do aplikace jediným kliknutím.</span><span class="sxs-lookup"><span data-stu-id="db087-107">After you set up your connection with LinkedIn through Attract, you can view potential LinkedIn candidates for your positions and export them into Attract with just one click.</span></span>

<span data-ttu-id="db087-108">Pokud tuto funkcinemáte, obraťte se na správce. Dříve než budete moci využít výhod LinkedIn Recruiter z Attract, je nutné, aby váš správce [nastavil integraci s LinkedIn](./attract-admin-linkedin.md).</span><span class="sxs-lookup"><span data-stu-id="db087-108">If you don't seem to have this capability, contact your admin. Before you can take advantage of LinkedIn Recruiter from Attract, your admin must [set up integration with LinkedIn](./attract-admin-linkedin.md).</span></span> <span data-ttu-id="db087-109">Poté můžete nastavit připojení LinkedIn Recruiter a začít vyhledávat kandidáty.</span><span class="sxs-lookup"><span data-stu-id="db087-109">You can then set up your connection with LinkedIn Recruiter and start finding candidates.</span></span>

>[!IMPORTANT]
><span data-ttu-id="db087-110">Od 1. července 2020 již LinkedIn nepodporuje Internet Explorer 11.</span><span class="sxs-lookup"><span data-stu-id="db087-110">As of July 1, 2020, LinkedIn no longer supports Internet Explorer 11.</span></span> <span data-ttu-id="db087-111">Uživatelé mohou stále používat LinkedIn s Internet Explorer 11, ale zobrazí se výzva k upgradu nebo použití jiného prohlížeče.</span><span class="sxs-lookup"><span data-stu-id="db087-111">Users can still access LinkedIn with Internet Explorer 11, but will be prompted to upgrade or use a different browser.</span></span> <span data-ttu-id="db087-112">Další informace viz [Podporované internetové prohlížeče pro LinkedIn](https://www.linkedin.com/help/linkedin/answer/4135/supported-internet-browsers-for-linkedin).</span><span class="sxs-lookup"><span data-stu-id="db087-112">For more information, see [Supported Internet Browsers for LinkedIn](https://www.linkedin.com/help/linkedin/answer/4135/supported-internet-browsers-for-linkedin).</span></span>

## <a name="set-up-your-connection-with-linkedin-recruiter"></a><span data-ttu-id="db087-113">Nastavit připojení pomocí LinkedIn Recruiter</span><span class="sxs-lookup"><span data-stu-id="db087-113">Set up your connection with LinkedIn Recruiter</span></span>

<span data-ttu-id="db087-114">Chcete-li začít pracovat s LinkedIn Recruiter prostřednictvím aplikace Attract, je nutné vytvořit připojení pomocí LinkedIn Recruiter.</span><span class="sxs-lookup"><span data-stu-id="db087-114">Before you can start working with LinkedIn Recruiter through Attract, you must set up your connection with LinkedIn Recruiter.</span></span> <span data-ttu-id="db087-115">V tomto kroku budete potřebovat své přihlašovací údaje do LinkedIn Recruiter.</span><span class="sxs-lookup"><span data-stu-id="db087-115">For this step, you need your LinkedIn Recruiter credentials.</span></span>

1. <span data-ttu-id="db087-116">Zvolte tlačítko **Nastavení** (ikona ozubeného kola) v pravém horním rohu stránky.</span><span class="sxs-lookup"><span data-stu-id="db087-116">Select the **Settings** button (gear icon) in the upper-right corner of the page.</span></span>
2. <span data-ttu-id="db087-117">Vyberte **Nastavení uživatele**.</span><span class="sxs-lookup"><span data-stu-id="db087-117">Select **User settings**.</span></span>
3. <span data-ttu-id="db087-118">Na kartě **Připojení** vyberte možnost **Připojit** vedle **LinkedIn**.</span><span class="sxs-lookup"><span data-stu-id="db087-118">On the **Connections** tab, select **Connect** next to **LinkedIn**.</span></span> <span data-ttu-id="db087-119">Postupujte podle pokynů, které jsou k dispozici službou LinkedIn.</span><span class="sxs-lookup"><span data-stu-id="db087-119">Follow the instructions that are provided by LinkedIn.</span></span>

    ![[<span data-ttu-id="db087-120">Nastavení připojení k LinkedIn Recruiter z aplikace Attract</span><span class="sxs-lookup"><span data-stu-id="db087-120">Set up connection to LinkedIn Recruiter from Attract</span></span>](./media/attract-set-up-linkedin-recruiter-connection.png)](./media/attract-set-up-linkedin-recruiter-connection.png)

## <a name="view-linkedin-candidates-in-attract"></a><span data-ttu-id="db087-121">Zobrazit kandidáty LinkedIn v aplikaci Attract</span><span class="sxs-lookup"><span data-stu-id="db087-121">View LinkedIn candidates in Attract</span></span>

<span data-ttu-id="db087-122">Po připojení LinkedIn Recruiter můžete zobrazit linkedinové profily kandidátů v aplikaci Attract.</span><span class="sxs-lookup"><span data-stu-id="db087-122">After you're connected to LinkedIn Recruiter, you can view candidates' LinkedIn profiles in Attract.</span></span>

>[!NOTE]
><span data-ttu-id="db087-123">Pokud vám byla přidělena licence Recruiter (Náborář), můžete zobrazit úplné informace o kandidátech.</span><span class="sxs-lookup"><span data-stu-id="db087-123">If you have a Recruiter seat assigned to you, you can see the candidates' full information.</span></span><br><br>
><span data-ttu-id="db087-124">Pokud máte licenci Hiring Manager (Náborový manažer) nebo žádnou licenci, nezapomeňte se odhlásit z LinkedIn nebo LinkedIn Recruiter před přechodem na kartu LinkedIn pro kandidáta v aplikaci Attract.</span><span class="sxs-lookup"><span data-stu-id="db087-124">If you have a Hiring Manager seat or no seat assigned to you, be sure to sign out of LinkedIn or LinkedIn Recruiter before navigating to the LinkedIn tab for a candidate in Attract.</span></span> <span data-ttu-id="db087-125">Budete moci zobrazit základní údaje veřejného profilu kandidáta, například jeho křestní jméno a příjmení.</span><span class="sxs-lookup"><span data-stu-id="db087-125">You'll be able to see the candidate's basic public profile data, such as their first and last name.</span></span>

1. <span data-ttu-id="db087-126">V aplikaci Attract vyberte **Pracovní pozice** nebo **Skupiny talentů** v levé části a poté vyberte uchazeče.</span><span class="sxs-lookup"><span data-stu-id="db087-126">In Attract, select **Jobs** or **Talent pools** on the left, and then select an applicant.</span></span>

    ![[<span data-ttu-id="db087-127">Zobrazit kandidáty LinkedIn v aplikaci Attract</span><span class="sxs-lookup"><span data-stu-id="db087-127">View LinkedIn candidates in Attract</span></span>](./media/attract-view-linkedin-candidates.png)](./media/attract-view-linkedin-candidates.png)

2. <span data-ttu-id="db087-128">V profilu kandidáta vyberte kartu **LinkedIn**. Můžete zobrazit profil kandidáta a historii InMail.</span><span class="sxs-lookup"><span data-stu-id="db087-128">In the candidate's profile, select the **LinkedIn** tab. You can view the candidate's profile and InMail history.</span></span>

   ![Zobrazení informací o kandidátovi na LinkedIn](./media/attract-candidate-linkedin-tab.png)

<span data-ttu-id="db087-130">Odtud můžete provést následující akce:</span><span class="sxs-lookup"><span data-stu-id="db087-130">From here, you can perform the following actions:</span></span>

- <span data-ttu-id="db087-131">Vyberte kartu **Náborové aktivity** k zobrazení následujících:</span><span class="sxs-lookup"><span data-stu-id="db087-131">Select the **Recruiting activities** tab to view:</span></span>
   
   - <span data-ttu-id="db087-132">Poznámky o náboráři (veřejné i soukromé).</span><span class="sxs-lookup"><span data-stu-id="db087-132">Recruiter notes (both public and private).</span></span> <span data-ttu-id="db087-133">Ve výchozím nastavení jsou poznámky soukromé a viditelné pouze pro vlastníka poznámek.</span><span class="sxs-lookup"><span data-stu-id="db087-133">By default, notes are private and only visible to the owner of the notes.</span></span>
   - <span data-ttu-id="db087-134">Aktivita InMail (mimo obsah InMail).</span><span class="sxs-lookup"><span data-stu-id="db087-134">InMail activity (but not the InMail content).</span></span> <span data-ttu-id="db087-135">Posunutím do dolní části stránky zobrazíte výměnu InMail s vaším potenciálním zákazníkem a další uživatele ve vaší organizaci, kteří s vaším potenciálním zákazníkem interagují.</span><span class="sxs-lookup"><span data-stu-id="db087-135">Scroll to the bottom of the page to view the InMail exchange with your prospect and view other users in your organization who are interacting with your prospect.</span></span>
   - <span data-ttu-id="db087-136">Aktivita odmítnutí kandidátů</span><span class="sxs-lookup"><span data-stu-id="db087-136">Candidate rejection activity</span></span>

- <span data-ttu-id="db087-137">Volbou **Odeslat InMail** pošlete InMail, aniž byste museli opustit aplikaci Attract.</span><span class="sxs-lookup"><span data-stu-id="db087-137">Select **Send InMail** to send InMail without having to leave Attract.</span></span>

- <span data-ttu-id="db087-138">Volbou **Uložit do úlohy** uložíte úlohu, aniž byste opustili Attract.</span><span class="sxs-lookup"><span data-stu-id="db087-138">Select **Save to a job** to save the job without leaving Attract.</span></span>

> [!NOTE]
> <span data-ttu-id="db087-139">LinkedIn profil uchazeče se zobrazí v Attract, když se informace o uživateli kandidáta shodují s informacemi LinkedIn.</span><span class="sxs-lookup"><span data-stu-id="db087-139">A candidate's LinkedIn profile will display in Attract when the candidate's Attract information matches the LinkedIn information.</span></span> <span data-ttu-id="db087-140">Používají se následující pravidla párování:</span><span class="sxs-lookup"><span data-stu-id="db087-140">Here are the matching rules that are used:</span></span>
> 
> 1. <span data-ttu-id="db087-141">Pokud se e-mailová adresa a ID člena LinkedIn shoduje s v aplikaci Attract a LinkedIn, zobrazí se profil kandidáta.</span><span class="sxs-lookup"><span data-stu-id="db087-141">If the email address and LinkedIn member ID match in Attract and LinkedIn, the candidate's profile is shown.</span></span> <span data-ttu-id="db087-142">Kandidáti stále mají možnost propojit nebo zrušit propojení svého LinkedIn profilu s Attract.</span><span class="sxs-lookup"><span data-stu-id="db087-142">Candidates still have the option to link or unlink their LinkedIn profile from Attract.</span></span>
> 2. <span data-ttu-id="db087-143">Pokud neodpovídá e-mailová adresa nebo ID člena LinkedIn, zobrazí se seznam možných kandidátů.</span><span class="sxs-lookup"><span data-stu-id="db087-143">If the email address or LinkedIn member ID doesn't match, you see a list of possible candidates.</span></span> <span data-ttu-id="db087-144">Poté můžete vybrat kandidáta v seznamu a propojit tento profil.</span><span class="sxs-lookup"><span data-stu-id="db087-144">You can then select a candidate in the list and link the profile.</span></span>
> 3. <span data-ttu-id="db087-145">Pokud neexistují žádné vyhovující položky, budete upozorněni, že nebyla nalezena žádná shoda.</span><span class="sxs-lookup"><span data-stu-id="db087-145">If there are no good matches, you're notified that no match was found.</span></span>

## <a name="export-linkedin-candidates-to-attract-with-one-click"></a><span data-ttu-id="db087-146">Exportovat kandidáty z LinkedIn do Attract jedním kliknutím</span><span class="sxs-lookup"><span data-stu-id="db087-146">Export LinkedIn candidates to Attract with one click</span></span>

<span data-ttu-id="db087-147">Při revizi kandidátů v LinkedIn Recruiter je můžete exportovat do pracovních pozic, které jsou aktuálně otevřeny v aplikaci Attract.</span><span class="sxs-lookup"><span data-stu-id="db087-147">While you're reviewing candidates in LinkedIn Recruiter, you can export them to jobs that you currently have open in Attract.</span></span> <span data-ttu-id="db087-148">Pro tento krok potřebujete oprávnění náborového manažera nebo náborového pracovníka v aplikaci Attract.</span><span class="sxs-lookup"><span data-stu-id="db087-148">For this step, you need Recruiter or Hiring Manager permissions in Attract.</span></span> <span data-ttu-id="db087-149">Další informace o rolích v Attract naleznete v tématu [Zabezpečení a správa rolí v aplikaci Attract](https://docs.microsoft.com/dynamics365/unified-operations/talent/security-attract).</span><span class="sxs-lookup"><span data-stu-id="db087-149">For more information about roles in Attract, see [Security and role management in Attract](https://docs.microsoft.com/dynamics365/unified-operations/talent/security-attract).</span></span>

<span data-ttu-id="db087-150">Je také nutné zajistit, aby úloha měla fázi potenciálního uchazeče.</span><span class="sxs-lookup"><span data-stu-id="db087-150">You must also make sure that the job has a Prospect stage.</span></span> <span data-ttu-id="db087-151">Další informace naleznete v tématu [Aktivita potenciálního uchazeče](./activities-attract.md#prospect-activity).</span><span class="sxs-lookup"><span data-stu-id="db087-151">For more information, see [Prospect activity](./activities-attract.md#prospect-activity).</span></span>

1. <span data-ttu-id="db087-152">V aplikai Attract vytvořte pozici, přiřaďte příslušné role a aktivujte pracovní pozici.</span><span class="sxs-lookup"><span data-stu-id="db087-152">In Attract, create a job, assign the appropriate roles, and activate the job.</span></span>
2. <span data-ttu-id="db087-153">V LinkedIn Recruiter vyhledejte vhodného kandidáta na práci a přejděte k profilu uchazeče.</span><span class="sxs-lookup"><span data-stu-id="db087-153">In LinkedIn Recruiter, find a good candidate for the job, and go to the candidate's profile.</span></span>
3. <span data-ttu-id="db087-154">Ve vyhledávacím poli na kartě kontaktu vyhledejte pracovní místo pomocí názvu nebo ID pracovního místa, které bylo aktivováno v systému Attract.</span><span class="sxs-lookup"><span data-stu-id="db087-154">In the job search box in the contact card, find the job by using the title or the Job ID that was activated in Attract.</span></span> <span data-ttu-id="db087-155">Pokud pracovní místo nenajdete, vyberte **Změnit ATS** k vyhledání správné instance Attract.</span><span class="sxs-lookup"><span data-stu-id="db087-155">If you can't find the job, select **Change ATS** to find the correct Attract instance.</span></span>
4. <span data-ttu-id="db087-156">Vyberte práci a pak vyberte **Export**.</span><span class="sxs-lookup"><span data-stu-id="db087-156">Select the job, and then select **Export**.</span></span>
5. <span data-ttu-id="db087-157">V aplikaci Attract otevřete úlohu.</span><span class="sxs-lookup"><span data-stu-id="db087-157">In Attract, open the job.</span></span> <span data-ttu-id="db087-158">Exportovaný kandidát se zobrazí na kartě **Potenciální uchazeč** pro danou úlohu.</span><span class="sxs-lookup"><span data-stu-id="db087-158">The exported candidate will appear on the **Prospect** tab of the job.</span></span>

## <a name="view-attract-information-in-linkedin-recruiter"></a><span data-ttu-id="db087-159">Zobrazit informace o aplikaci Attract v LinkedIn Recruiter</span><span class="sxs-lookup"><span data-stu-id="db087-159">View Attract information in LinkedIn Recruiter</span></span>

<span data-ttu-id="db087-160">Pomocí LinkedIn Recruiter můžete sledovat, zda uchazeč žádal o jiná pracovní místa ve vaší organizaci, podívat se, kde se kandidát nachází v různých fází žádostí o pracovní pozici, a zobrazit zpětnou vazbu a komentáře z aplikace Attract.</span><span class="sxs-lookup"><span data-stu-id="db087-160">In LinkedIn Recruiter, you can track whether a candidate applied to other jobs in your organization, see where the candidate is in the various stages for job applications, and view feedback and comments from Attract.</span></span>

1. <span data-ttu-id="db087-161">Otevřete LinkedIn Recruiter a vyberte požadovaný profil kandidáta.</span><span class="sxs-lookup"><span data-stu-id="db087-161">Open LinkedIn Recruiter, and select a candidate profile.</span></span>
2. <span data-ttu-id="db087-162">Přesuňte ukazatel myši na **V ATS**.</span><span class="sxs-lookup"><span data-stu-id="db087-162">Hover over **In ATS**.</span></span>
3. <span data-ttu-id="db087-163">Chcete-li zobrazit informace o uchazečích, které jsou uloženy v Attract, vyberte některou z následujících možností:</span><span class="sxs-lookup"><span data-stu-id="db087-163">Select any of the following options to view the candidate information that is stored in Attract:</span></span>

    - <span data-ttu-id="db087-164">**Úlohy & stavy** – zobrazení úloh, jejichž součástí je uchazeč, nejnovější stav a způsob, jakým uchazeč postupuje pro každou práci.</span><span class="sxs-lookup"><span data-stu-id="db087-164">**Jobs & Statuses** – See jobs that the candidate is part of, the latest status, and how the candidate is progressing for each job.</span></span>
    - <span data-ttu-id="db087-165">**Zpětná vazba z pohovoru** – zobrazení zpětné vazby, kterou vedoucí pohovorů zaslali do systému Attract.</span><span class="sxs-lookup"><span data-stu-id="db087-165">**Interview Feedback** – See feedback that interviewers have submitted in Attract.</span></span>
    - <span data-ttu-id="db087-166">**Poznámky** – zobrazí se poznámky, které byly pro tohoto kandidáta zadány v Attract.</span><span class="sxs-lookup"><span data-stu-id="db087-166">**Notes** – See any notes that have been entered for this candidate in Attract.</span></span>

    ![[<span data-ttu-id="db087-167">Zobrazení informací o aplikaci Attract v LinkedIn Recruiter</span><span class="sxs-lookup"><span data-stu-id="db087-167">View Attract information from LinkedIn Recruiter</span></span>](./media/attract-view-information-from-linkedin-recruiter.png)](./media/attract-view-information-from-linkedin-recruiter.png)

> [!NOTE]
> <span data-ttu-id="db087-168">Údaje o uchazeči a žádosti se nebudou synchronizovat s programem LinkedIn Recruiter, pokud se uchazeč nedostal za fázi potenciálního uchazeče.</span><span class="sxs-lookup"><span data-stu-id="db087-168">Candidate and application data won't be synced with LinkedIn Recruiter if the candidate hasn't moved past the Prospect stage.</span></span>

## <a name="view-linkedin-talent-pools"></a><span data-ttu-id="db087-169">Zobrazit skupiny talentů LinkedIn</span><span class="sxs-lookup"><span data-stu-id="db087-169">View LinkedIn talent pools</span></span>

<span data-ttu-id="db087-170">Pokud kandidáti souhlasí se sdílením svého LinkedIn profilu s libovolným uživatelem ve vaší organizaci, vytvoří se nový záznam uchazeče v aplikaci Attract.</span><span class="sxs-lookup"><span data-stu-id="db087-170">If candidates agree to share their LinkedIn profiles with any user in your organization, a new candidate record is created in Attract.</span></span> <span data-ttu-id="db087-171">Tito kandidáti pak budou uvedeni v systémově vytvořené skupině talentů LinkedIn.</span><span class="sxs-lookup"><span data-stu-id="db087-171">These candidates then appear in a system-created LinkedIn talent pool.</span></span>

1. <span data-ttu-id="db087-172">V systému Attract vyberte **Skupiny talentů** na levé straně.</span><span class="sxs-lookup"><span data-stu-id="db087-172">In Attract, select **Talent pools** on the left.</span></span>
2. <span data-ttu-id="db087-173">Vyberte skupinu talentů LinkedIn.</span><span class="sxs-lookup"><span data-stu-id="db087-173">Select the LinkedIn talent pool.</span></span> <span data-ttu-id="db087-174">Zobrazí se seznam kandidátů a jejich profilů se zakázaným inzerováním z LinkedIn.</span><span class="sxs-lookup"><span data-stu-id="db087-174">You will see a list of candidates and their stub profiles from LinkedIn.</span></span> <span data-ttu-id="db087-175">Profily se zakázaným inzerováním obsahují křestní jména a příjmení kandidáta a e-mailovou adresu, pokud se ji uchazeč rozhodne sdílet.</span><span class="sxs-lookup"><span data-stu-id="db087-175">Stub profiles contain the candidate's first and last names and email address, if the candidate chose to share it.</span></span>

## <a name="see-also"></a><span data-ttu-id="db087-176">Viz také</span><span class="sxs-lookup"><span data-stu-id="db087-176">See also</span></span>

[<span data-ttu-id="db087-177">Časté dotazy týkající se integrace Attract s řešením LinkedIn</span><span class="sxs-lookup"><span data-stu-id="db087-177">Attract integration with LinkedIn FAQ</span></span>](./attract-linkedin-faq.md)

[<span data-ttu-id="db087-178">Nastavení integrace s řešením LinkedIn pro aplikaci Microsoft Dynamics 365 Talent - Attract</span><span class="sxs-lookup"><span data-stu-id="db087-178">Set up integration with LinkedIn for Microsoft Dynamics 365 Talent - Attract</span></span>](./attract-admin-linkedin.md)

[<span data-ttu-id="db087-179">Vytvoření, schválení a zveřejnění pracovních míst v aplikaci Attract</span><span class="sxs-lookup"><span data-stu-id="db087-179">Create, approve, and post jobs in Attract</span></span>](./creating-jobs-attract.md)

[<span data-ttu-id="db087-180">Publikování pracovních míst na LinkedIn z aplikace Microsoft Dynamics 365 Talent - Attract</span><span class="sxs-lookup"><span data-stu-id="db087-180">Post jobs to LinkedIn from Microsoft Dynamics 365 Talent - Attract</span></span>](./attract-post-jobs-to-linkedin.md)

[<span data-ttu-id="db087-181">Odstraňování problémů s integrací s LinkedIn a aplikací Microsoft Dynamics 365 Talent - Attract</span><span class="sxs-lookup"><span data-stu-id="db087-181">Troubleshooting integration with LinkedIn and Microsoft Dynamics 365 Talent - Attract</span></span>](./attract-troubleshoot-linkedin.md)
