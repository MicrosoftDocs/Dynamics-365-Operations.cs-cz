---
title: Nábor uchazečů o práci
description: Toto téma ukazuje, jak najímat kandidáty v Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 12/03/2020
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
ms.search.validFrom: 2020-12-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6aca285133495dfe023dfd18bdeb050aabcafee6
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/19/2021
ms.locfileid: "5478277"
---
# <a name="recruit-job-candidates"></a><span data-ttu-id="5a075-103">Nábor uchazečů o práci</span><span class="sxs-lookup"><span data-stu-id="5a075-103">Recruit job candidates</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="5a075-104">Dynamics 365 Human Resources vám pomůže spravovat žádosti o nábor.</span><span class="sxs-lookup"><span data-stu-id="5a075-104">Dynamics 365 Human Resources helps you to manage recruiting requests.</span></span> <span data-ttu-id="5a075-105">Pomůže vám také s bezproblémovým přechodem uchazečů o zaměstnání na zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="5a075-105">It also helps you seamlessly transition job candidates to employees.</span></span> <span data-ttu-id="5a075-106">Pokud vaše organizace používá samostatnou náborovou aplikaci, může váš náborový proces zahrnovat následující kroky:</span><span class="sxs-lookup"><span data-stu-id="5a075-106">If your organization uses a separate recruiting application, your recruiting process might include the following steps:</span></span>

- <span data-ttu-id="5a075-107">Zadejte svou žádost o nábor v Human Resources.</span><span class="sxs-lookup"><span data-stu-id="5a075-107">Enter your recruiting request in Human Resources.</span></span>
- <span data-ttu-id="5a075-108">Přijměte doporučení kandidátů v Human Resources z náborové aplikace.</span><span class="sxs-lookup"><span data-stu-id="5a075-108">Receive candidate referrals in Human Resources from the recruiting application.</span></span>
- <span data-ttu-id="5a075-109">Dokončete proces schvalování kandidátů v Human Resources.</span><span class="sxs-lookup"><span data-stu-id="5a075-109">Complete the candidate approval process in Human Resources.</span></span>

<span data-ttu-id="5a075-110">Pokud nepoužíváte samostatnou náborovou aplikaci, můžete kandidáty spravovat také ručně v Human Resources.</span><span class="sxs-lookup"><span data-stu-id="5a075-110">If you aren't using a separate recruiting application, you can also manually manage candidates in Human Resources.</span></span>

>[!NOTE]
><span data-ttu-id="5a075-111">Pokud jste správcem nebo vývojářem a chcete integrovat Human Resources s náborovou aplikací jiných výrobců, přečtěte si [Konfigurace integrace Dataverse](hr-admin-integration-common-data-service.md) a [Konfigurace virtuálních tabulek Dataverse](hr-admin-integration-common-data-service-virtual-entities.md)</span><span class="sxs-lookup"><span data-stu-id="5a075-111">If you're an admin or developer and want to integrate Human Resources with a third-party recruiting application, see [Configure Dataverse integration](hr-admin-integration-common-data-service.md) and [Configure Dataverse virtual tables](hr-admin-integration-common-data-service-virtual-entities.md)</span></span>
>
> <span data-ttu-id="5a075-112">Najdete zde také náborové integrační aplikace v [AppSource](https://appsource.microsoft.com/marketplace/apps?search=recruiting%20dynamics).</span><span class="sxs-lookup"><span data-stu-id="5a075-112">You can also find recruiting integration apps on [AppSource](https://appsource.microsoft.com/marketplace/apps?search=recruiting%20dynamics).</span></span>
>
> <span data-ttu-id="5a075-113">Chcete-li vyzkoušet naši funkci Preview pro integraci s LinkedIn Talent Hub, podívejte se do tématu [Integrace s LinkedIn Talent Hub](hr-admin-integration-linkedin.md).</span><span class="sxs-lookup"><span data-stu-id="5a075-113">To try out our preview feature for integrating with LinkedIn Talent Hub, see [Integrate with LinkedIn Talent Hub](hr-admin-integration-linkedin.md).</span></span>

## <a name="enable-recruiting-requests"></a><span data-ttu-id="5a075-114">Povolit požadavky na nábor</span><span class="sxs-lookup"><span data-stu-id="5a075-114">Enable recruiting requests</span></span>

<span data-ttu-id="5a075-115">Pokud chcete odeslat žádosti o nábor v Human Resources, musíte nejprve povolit tuto funkci v části **Sdílené parametry Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="5a075-115">If you want to submit recruiting requests in Human Resources, you must first enable the functionality in **Human resources shared parameters**.</span></span>

1. <span data-ttu-id="5a075-116">V pracovním prostoru **Správa zaměstnanců** vyberte kartu **Odkazy**.</span><span class="sxs-lookup"><span data-stu-id="5a075-116">In the **Personnel management** workspace, select **Links**.</span></span>

2. <span data-ttu-id="5a075-117">V části **Nastavení** vyberte **Sdílené parametry Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="5a075-117">Under **Setup**, select **Human resources shared parameters**.</span></span>

3. <span data-ttu-id="5a075-118">Na kartě **Nábor** v části **NÁBOR** nastavte **Povolit žádosti o nábor** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="5a075-118">On the **Recruitment** tab, under **RECRUITING**, set **Enable recruiting requests** to **Yes**.</span></span>

## <a name="add-a-recruiting-request-location"></a><span data-ttu-id="5a075-119">Přidání umístění žádosti o nábor</span><span class="sxs-lookup"><span data-stu-id="5a075-119">Add a recruiting request location</span></span>

<span data-ttu-id="5a075-120">Pokud má vaše organizace více umístění, můžete je přidat, aby si žadatelé mohli vybrat místo, kde bude nový nábor probíhat.</span><span class="sxs-lookup"><span data-stu-id="5a075-120">If your organization has multiple locations, you can add them so requestors can select a location where the new recruit will be working.</span></span> <span data-ttu-id="5a075-121">Umístění bude zahrnuto do publikovaného pracovního místa.</span><span class="sxs-lookup"><span data-stu-id="5a075-121">The location will be included in the job posting.</span></span>

1. <span data-ttu-id="5a075-122">Do vyhledávacího pole zadejte **umístění žádosti o nábor**.</span><span class="sxs-lookup"><span data-stu-id="5a075-122">In the search bar, enter **recruiting request location**.</span></span>

2. <span data-ttu-id="5a075-123">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="5a075-123">Select **New**.</span></span>

3. <span data-ttu-id="5a075-124">V poli **Umístění žádosti o nábor** zadejte název umístění.</span><span class="sxs-lookup"><span data-stu-id="5a075-124">In the **Recruiting request location** field, enter the location name.</span></span>

   ![Přidání umístění žádosti o nábor](./media/hr-recruit-0a-add-location.png)

4. <span data-ttu-id="5a075-126">Do pole **Popis** zadejte popis umístění.</span><span class="sxs-lookup"><span data-stu-id="5a075-126">In the **Description**, enter a description for the location.</span></span>

5. <span data-ttu-id="5a075-127">Ve volbě **Umístění** vyberte **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="5a075-127">Under **Location**, select **Add**.</span></span> <span data-ttu-id="5a075-128">Pokud se otevře okno **Nová adresa**, zadejte adresu umístění.</span><span class="sxs-lookup"><span data-stu-id="5a075-128">If the **New address** popout appears, enter the address for the location.</span></span>

   ![Zadejte adresu](./media/hr-recruit-0b-address.png)

6. <span data-ttu-id="5a075-130">Pod **Kontaktní informace** zadejte kontaktní informace místa.</span><span class="sxs-lookup"><span data-stu-id="5a075-130">Under **Contact information**, enter the information for the location's contact.</span></span>

7. <span data-ttu-id="5a075-131">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="5a075-131">Select **Save**.</span></span>

## <a name="add-a-recruiting-request"></a><span data-ttu-id="5a075-132">Přidání žádosti o nábor</span><span class="sxs-lookup"><span data-stu-id="5a075-132">Add a recruiting request</span></span>

<span data-ttu-id="5a075-133">Manažeři mohou odesílat žádosti o nábor v Human Resources.</span><span class="sxs-lookup"><span data-stu-id="5a075-133">Managers can submit recruiting requests in Human Resources.</span></span> <span data-ttu-id="5a075-134">Pokud používáte samostatnou náborovou aplikaci, po dokončení těchto kroků odešlete žádost o nábor a zahájíte proces náboru v této aplikaci.</span><span class="sxs-lookup"><span data-stu-id="5a075-134">If you use a separate recruiting application, completing these steps will send a recruiting request and start the recruiting process in that application.</span></span> <span data-ttu-id="5a075-135">V opačném případě dokončením tohoto postupu zahájíte pracovní postup pro svůj vlastní interní proces náboru.</span><span class="sxs-lookup"><span data-stu-id="5a075-135">Otherwise, complete this procedure to begin the workflow for your own internal recruiting process.</span></span>

1. <span data-ttu-id="5a075-136">Vyberte **Samoobsluha pro zaměstnance**.</span><span class="sxs-lookup"><span data-stu-id="5a075-136">Select **Employee self service**.</span></span>

2. <span data-ttu-id="5a075-137">Vyberte kartu **Můj tým**.</span><span class="sxs-lookup"><span data-stu-id="5a075-137">Select the **My team** tab.</span></span>

3. <span data-ttu-id="5a075-138">Vyberte **Žádost o nábor**.</span><span class="sxs-lookup"><span data-stu-id="5a075-138">Select  **Request to recruit**.</span></span>

   ![Zahájení žádosti o nábor](./media/hr-recruit-1-request-to-recruit.png)

4. <span data-ttu-id="5a075-140">Vyplňte pole **Popis**, **Práce** a **Odhadované počáteční datum**.</span><span class="sxs-lookup"><span data-stu-id="5a075-140">Complete the **Description**, **Job**, and **Estimated start date** fields.</span></span>

   ![Vyplnění žádosti o nábor](./media/hr-recruit-2-request-to-recruit.png)

5. <span data-ttu-id="5a075-142">Vyberte **Pokračovat**.</span><span class="sxs-lookup"><span data-stu-id="5a075-142">Select **Continue**.</span></span> <span data-ttu-id="5a075-143">Zobrazí se žádost o nábor pro vaši pozici.</span><span class="sxs-lookup"><span data-stu-id="5a075-143">The recruiting request for your position appears.</span></span>

6. <span data-ttu-id="5a075-144">V části **Obecné** vyberte náboráře z rozevíracího seznamu **Náborář** a poté vyberte umístění z rozevíracího seznamu **Umístění žádosti na nábor**.</span><span class="sxs-lookup"><span data-stu-id="5a075-144">Under **General**, select a recruiter from the **Recruiter** dropdown, and then select a location from the **Recruiting request location** dropdown.</span></span>

7. <span data-ttu-id="5a075-145">V části **Práce** podle potřeby změňte informace a poté vyberte **Vytvořit podrobnosti z práce**.</span><span class="sxs-lookup"><span data-stu-id="5a075-145">Under **Job**, change any information as needed, and then select **Create details from job**.</span></span>

   ![Vytvořte podrobnosti z úlohy](./media/hr-recruit-3-create-details-from-job.png)

   <span data-ttu-id="5a075-147">Zbytek žádosti o nábor se naplní výchozími informacemi o zadané práci.</span><span class="sxs-lookup"><span data-stu-id="5a075-147">The rest of the recruiting request will populate with the default information for the job you entered.</span></span>

8. <span data-ttu-id="5a075-148">V části **Vnější popis** zadejte popis práce, který se bude zobrazovat navenek.</span><span class="sxs-lookup"><span data-stu-id="5a075-148">Under **External description**, enter an external-facing job description.</span></span>

9. <span data-ttu-id="5a075-149">V části **Pozice** vyberte **Přidat** a poté vyberte pozici pro tuto žádost o nábor.</span><span class="sxs-lookup"><span data-stu-id="5a075-149">Under **Positions**, select **Add**, and then select a position for this recruiting request.</span></span>

   ![Přidání pozice](./media/hr-recruit-4-select-position.png)

10. <span data-ttu-id="5a075-151">V části **Dovednosti** vyberte **Přidat** a poté vyberte dovednost.</span><span class="sxs-lookup"><span data-stu-id="5a075-151">Under **Skills**, select **Add**, and then select a skill.</span></span>

11. <span data-ttu-id="5a075-152">V části **Požadavky na vzdělání** vyberte **Přidat** a poté vyberte hodnoty z rozevíracích seznamů **Vzdělání** a **Úroveň vzdělání**.</span><span class="sxs-lookup"><span data-stu-id="5a075-152">Under **Educational requirements**, select **Add**, and then select values from the **Education** and **Level of education** dropdowns.</span></span>

   ![Přidání dalších požadavků](./media/hr-recruit-5-select-educational-requirements.png)

12. <span data-ttu-id="5a075-154">V části **Komentář** podle potřeby přidávejte komentáře.</span><span class="sxs-lookup"><span data-stu-id="5a075-154">Under **Comment**, add comments as necessary.</span></span>

13. <span data-ttu-id="5a075-155">V části **Kompenzace** vyberte úroveň z rozevíracího seznamu **Úroveň** a poté upravte **Dolní prahová hodnota**, **Kontrolní bod** a **Horní prahová hodnota**, jak je potřeba.</span><span class="sxs-lookup"><span data-stu-id="5a075-155">Under **Compensation**, select a level from the **Level** dropdown, and then adjust **Low threshold**, **Control point**, and **High threshold** as necessary.</span></span>

14. <span data-ttu-id="5a075-156">Když je vaše žádost o nábor dokončen a jste připraveni zahájit proces náboru, vyberte **Aktivovat** v řádku nabídek.</span><span class="sxs-lookup"><span data-stu-id="5a075-156">When your recruiting request is complete and you're ready to start the recruiting process, select **Activate** in the menu bar.</span></span>

   ![Aktivace žádosti o nábor](./media/hr-recruit-6-activate-recruit-request.png)

15. <span data-ttu-id="5a075-158">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="5a075-158">Select **Save**.</span></span>

## <a name="view-and-edit-your-recruiting-requests"></a><span data-ttu-id="5a075-159">Zobrazení a úpravy žádostí o nábor</span><span class="sxs-lookup"><span data-stu-id="5a075-159">View and edit your recruiting requests</span></span>

<span data-ttu-id="5a075-160">Pokud jste manažer a chcete zobrazit své vlastní požadavky:</span><span class="sxs-lookup"><span data-stu-id="5a075-160">If you're a manager and want to view your own requests:</span></span>

1. <span data-ttu-id="5a075-161">Vyberte **Samoobsluha pro zaměstnance**.</span><span class="sxs-lookup"><span data-stu-id="5a075-161">Select **Employee self service**.</span></span>

2. <span data-ttu-id="5a075-162">Vyberte kartu **Můj tým**.</span><span class="sxs-lookup"><span data-stu-id="5a075-162">Select the **My team** tab.</span></span>

3. <span data-ttu-id="5a075-163">V části **Informace o mém týmu** vyberte kartu **Žádosti o nábor**.</span><span class="sxs-lookup"><span data-stu-id="5a075-163">Under **My team information**, select the **Recruiting requests** tab.</span></span>

   ![Výběr karty Žádosti o nábor](./media/hr-recruit-7-recruiting-requests.png)

4. <span data-ttu-id="5a075-165">Chcete-li zobrazit nebo upravit žádost o nábor, vyberte jej v mřížce.</span><span class="sxs-lookup"><span data-stu-id="5a075-165">To view or edit a recruiting request, select it in the grid.</span></span>

<span data-ttu-id="5a075-166">Pokud jste personalista a chcete zobrazit všechny žádosti o nábor:</span><span class="sxs-lookup"><span data-stu-id="5a075-166">If you're an HR pro and want to view all recruiting requests:</span></span>

1. <span data-ttu-id="5a075-167">Vyberte **Správa zaměstnanců**.</span><span class="sxs-lookup"><span data-stu-id="5a075-167">Select **Personnel management**.</span></span>

2. <span data-ttu-id="5a075-168">Vyberte **Žádosti o nábor**.</span><span class="sxs-lookup"><span data-stu-id="5a075-168">Select **Recruiting requests**.</span></span>

   ![Zobrazení žádostí o nábor ve správě zaměstnanců](./media/hr-recruit-8-recruiting-requests-personnel-management.png)

3. <span data-ttu-id="5a075-170">Chcete-li zobrazit nebo upravit žádost o nábor, vyberte jej v mřížce.</span><span class="sxs-lookup"><span data-stu-id="5a075-170">To view or edit a recruiting request, select it in the grid.</span></span>

## <a name="add-or-edit-a-candidate-profile"></a><span data-ttu-id="5a075-171">Přidání nebo úprava profilu kandidáta</span><span class="sxs-lookup"><span data-stu-id="5a075-171">Add or edit a candidate profile</span></span>

<span data-ttu-id="5a075-172">Pokud vaše organizace integrovala jinou aplikaci pro správu žádostí o nábor, žádosti o nábor se předají této aplikaci.</span><span class="sxs-lookup"><span data-stu-id="5a075-172">If your organization has integrated with another application to manage recruiting requests, recruiting requests are forwarded to that application.</span></span> <span data-ttu-id="5a075-173">Náborová aplikace poté odešle informace o kandidátovi zpět do Human Resources.</span><span class="sxs-lookup"><span data-stu-id="5a075-173">The recruiting application then sends candidate information back to Human Resources.</span></span> <span data-ttu-id="5a075-174">V opačném případě můžete sledovat vlastní interní procesy náboru a zadávat informace o kandidátech ručně.</span><span class="sxs-lookup"><span data-stu-id="5a075-174">Otherwise, you can follow your own internal recruiting processes and enter candidate information manually.</span></span>

1. <span data-ttu-id="5a075-175">Vyberte **Správa zaměstnanců**.</span><span class="sxs-lookup"><span data-stu-id="5a075-175">Select **Personnel management**.</span></span>

2. <span data-ttu-id="5a075-176">Vybrerte **Odkazy**.</span><span class="sxs-lookup"><span data-stu-id="5a075-176">Select **Links**.</span></span>

3. <span data-ttu-id="5a075-177">V části **Nábor** vyberte **Kandidáti**.</span><span class="sxs-lookup"><span data-stu-id="5a075-177">Under **Recruiting**, select **Candidates**.</span></span>

   ![Zobrazení kandidátů](./media/hr-recruit-9-candidates.png)

4. <span data-ttu-id="5a075-179">Chcete-li přidat kandidáta, vyberte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="5a075-179">To add a candidate, select **New**.</span></span> <span data-ttu-id="5a075-180">Chcete-li upravit existujícího kandidáta, vyberte jej ze seznamu a pak vyberte možnost **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="5a075-180">To edit an existing candidate, select the candidate from the list and then select **Edit**.</span></span> <span data-ttu-id="5a075-181">Zobrazí se profil kandidáta.</span><span class="sxs-lookup"><span data-stu-id="5a075-181">The candidate profile appears.</span></span>

5. <span data-ttu-id="5a075-182">V části **Souhrn kandidáta** podle potřeby zadejte nebo upravte informace o kandidátovi.</span><span class="sxs-lookup"><span data-stu-id="5a075-182">Under **Candidate summary**, enter or edit the candidate information as necessary.</span></span>

6. <span data-ttu-id="5a075-183">V části **Žádosti o nábor** vyberte žádost o nábor, se kterou chcete kandidáta propojit.</span><span class="sxs-lookup"><span data-stu-id="5a075-183">Under **Recruiting request**, select a recruiting request to link the candidate to.</span></span> <span data-ttu-id="5a075-184">Poté dle potřeby vyplňte pole **Odhadované počáteční datum**, **Náborový manažer**, **Pozice** a **Popis**.</span><span class="sxs-lookup"><span data-stu-id="5a075-184">Then complete the **Estimated start date**, **Hiring manager**, **Position**, and **Description fields** as appropriate.</span></span>

   ![Odkaz na žádost o nábor](./media/hr-recruit-10-link-to-recruiting-request.png)

7. <span data-ttu-id="5a075-186">Vyplňte všechny informace v následujících oblastech, které chcete zahrnout do záznamu kandidáta:</span><span class="sxs-lookup"><span data-stu-id="5a075-186">Complete all the information in the following areas that you want to include in the candidate's record:</span></span>
   - <span data-ttu-id="5a075-187">**Komentáře**</span><span class="sxs-lookup"><span data-stu-id="5a075-187">**Comments**</span></span>
   - <span data-ttu-id="5a075-188">**Profesionální zkušenosti**</span><span class="sxs-lookup"><span data-stu-id="5a075-188">**Professional experience**</span></span>
   - <span data-ttu-id="5a075-189">**Kontaktní informace**</span><span class="sxs-lookup"><span data-stu-id="5a075-189">**Contact information**</span></span>
   - <span data-ttu-id="5a075-190">**Vzdělání**</span><span class="sxs-lookup"><span data-stu-id="5a075-190">**Education**</span></span>
   - <span data-ttu-id="5a075-191">**Dovednosti**</span><span class="sxs-lookup"><span data-stu-id="5a075-191">**Skills**</span></span>
   - <span data-ttu-id="5a075-192">**Certifikáty**</span><span class="sxs-lookup"><span data-stu-id="5a075-192">**Certificates**</span></span>
   - <span data-ttu-id="5a075-193">**Prověřování**</span><span class="sxs-lookup"><span data-stu-id="5a075-193">**Screenings**</span></span>

8. <span data-ttu-id="5a075-194">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="5a075-194">Select **Save**.</span></span>

## <a name="hire-a-candidate"></a><span data-ttu-id="5a075-195">Přijetí kandidáta</span><span class="sxs-lookup"><span data-stu-id="5a075-195">Hire a candidate</span></span>

<span data-ttu-id="5a075-196">Až budete připraveni přijmout kandidáta, postupujte podle tohoto postupu a přeměňte kandidáta na zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="5a075-196">When you're ready to hire a candidate, follow this procedure to transition the candidate to an employee.</span></span>

1. <span data-ttu-id="5a075-197">Na formuláři kandidáta vyberte **Přijmout**.</span><span class="sxs-lookup"><span data-stu-id="5a075-197">On the candidate form, select **Hire**.</span></span>

   ![Přijetí kandidáta](./media/hr-recruit-11-hire.png)

2. <span data-ttu-id="5a075-199">Ve formuláři **Přijetí nového pracovníka** pod **Podrobnosti** vyplňte všechna pole.</span><span class="sxs-lookup"><span data-stu-id="5a075-199">On the **Hire new worker** form, under **Details**, complete all the fields.</span></span>

   ![Zadání podrobností nového zaměstnance](./media/hr-recruit-12-hire-new-worker.png)

3. <span data-ttu-id="5a075-201">Pod **Podrobnosti o pozici** ověřte a podle potřeby změňte informace.</span><span class="sxs-lookup"><span data-stu-id="5a075-201">Under **Position details**, verify and change information as necessary.</span></span>

4. <span data-ttu-id="5a075-202">V části **Kontrolní seznamy náboru** vyberte příslušné kontrolní seznamy náboru pro tohoto zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="5a075-202">Under **Onboarding checklists**, select the relevant onboarding checklists for this employee.</span></span>

5. <span data-ttu-id="5a075-203">Volbou **Pokračovat** vytvoříte záznam zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="5a075-203">Select **Continue** to create the employee record.</span></span>

   >[!NOTE]
   ><span data-ttu-id="5a075-204">V závislosti na pracovních postupech vaší organizace může záznam kandidáta projít dalšími schvalovacími kroky, než se stane záznamem zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="5a075-204">Depending on your organization's workflows, the candidate record may go through additional approval steps before becoming an employee record.</span></span>

## <a name="decide-not-to-hire-a-candidate"></a><span data-ttu-id="5a075-205">Rozhodnutí o nepřijatí kandidáta</span><span class="sxs-lookup"><span data-stu-id="5a075-205">Decide not to hire a candidate</span></span>

<span data-ttu-id="5a075-206">Pokud se rozhodnete kandidáta nepřijmout, postupujte podle tohoto postupu, kterým jej vyřadíte z procesu prověřování.</span><span class="sxs-lookup"><span data-stu-id="5a075-206">If you decide not to hire a candidate, follow this procedure to remove them from the vetting process.</span></span> 

1. <span data-ttu-id="5a075-207">Na formuláři kandidáta vyberte **Nepřijmout**.</span><span class="sxs-lookup"><span data-stu-id="5a075-207">On the candidate form, select **Do not hire**.</span></span>

   ![Nepřijetí kandidáta](./media/hr-recruit-13-do-not-hire.png)

2. <span data-ttu-id="5a075-209">Vyberte **Kód důvodu** a přidejte veškeré potřebné komentáře.</span><span class="sxs-lookup"><span data-stu-id="5a075-209">Select a **Reason code** and include any comments.</span></span>

3. <span data-ttu-id="5a075-210">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="5a075-210">Select **OK**.</span></span>

## <a name="dismiss-a-candidate"></a><span data-ttu-id="5a075-211">Propuštění kandidáta</span><span class="sxs-lookup"><span data-stu-id="5a075-211">Dismiss a candidate</span></span>

<span data-ttu-id="5a075-212">V případě potřeby můžete kandidáta poté, co ho přijmete, propustit.</span><span class="sxs-lookup"><span data-stu-id="5a075-212">If needed, you can dismiss a candidate after hiring them.</span></span> <span data-ttu-id="5a075-213">Například kandidát může vaši nabídku odmítnout nebo se neobjeví hned první den.</span><span class="sxs-lookup"><span data-stu-id="5a075-213">For example, a candidate might reject your offer or not show up on their first day.</span></span>

- <span data-ttu-id="5a075-214">Na formuláři kandidáta vyberte **Propustit kandidáta**.</span><span class="sxs-lookup"><span data-stu-id="5a075-214">On the candidate form, select **Dismiss candidate**.</span></span>

  ![Zamítnout kandidáta](./media/hr-recruit-14-dismiss-candidate.png)

## <a name="see-also"></a><span data-ttu-id="5a075-216">Viz také</span><span class="sxs-lookup"><span data-stu-id="5a075-216">See also</span></span>

[<span data-ttu-id="5a075-217">Konfigurace virtuálních tabulek Dataverse</span><span class="sxs-lookup"><span data-stu-id="5a075-217">Configure Dataverse virtual tables</span></span>](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[<span data-ttu-id="5a075-218">Organizování zaměstnanců</span><span class="sxs-lookup"><span data-stu-id="5a075-218">Organize your workforce</span></span>](hr-personnel-departments-jobs-positions.md)<br>
[<span data-ttu-id="5a075-219">Nastavení komponent práce</span><span class="sxs-lookup"><span data-stu-id="5a075-219">Set up the components of a job</span></span>](hr-personnel-jobs.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
