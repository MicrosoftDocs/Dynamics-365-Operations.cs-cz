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
ms.openlocfilehash: 9a35abcb8a2f6aa8031c8d84a44c2a8ad93883ac
ms.sourcegitcommit: 0354ca7e566fbd2eb0aabdd40000d4ac5c44ea78
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/04/2020
ms.locfileid: "4669157"
---
# <a name="recruit-job-candidates"></a><span data-ttu-id="7d5f8-103">Nábor uchazečů o práci</span><span class="sxs-lookup"><span data-stu-id="7d5f8-103">Recruit job candidates</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="7d5f8-104">Dynamics 365 Human Resources vám pomůže spravovat žádosti o nábor.</span><span class="sxs-lookup"><span data-stu-id="7d5f8-104">Dynamics 365 Human Resources helps you to manage recruiting requests.</span></span> <span data-ttu-id="7d5f8-105">Pomůže vám také s bezproblémovým přechodem uchazečů o zaměstnání na zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="7d5f8-105">It also helps you seamlessly transition job candidates to employees.</span></span> <span data-ttu-id="7d5f8-106">Pokud vaše organizace používá samostatnou náborovou aplikaci, může váš náborový proces zahrnovat následující kroky:</span><span class="sxs-lookup"><span data-stu-id="7d5f8-106">If your organization uses a separate recruiting application, your recruiting process might include the following steps:</span></span>

- <span data-ttu-id="7d5f8-107">Zadejte svou žádost o nábor v Human Resources.</span><span class="sxs-lookup"><span data-stu-id="7d5f8-107">Enter your recruiting request in Human Resources.</span></span>
- <span data-ttu-id="7d5f8-108">Přijměte doporučení kandidátů v Human Resources z náborové aplikace.</span><span class="sxs-lookup"><span data-stu-id="7d5f8-108">Receive candidate referrals in Human Resources from the recruiting application.</span></span>
- <span data-ttu-id="7d5f8-109">Dokončete proces schvalování kandidátů v Human Resources.</span><span class="sxs-lookup"><span data-stu-id="7d5f8-109">Complete the candidate approval process in Human Resources.</span></span>

<span data-ttu-id="7d5f8-110">Pokud nepoužíváte samostatnou náborovou aplikaci, můžete kandidáty spravovat také ručně v Human Resources.</span><span class="sxs-lookup"><span data-stu-id="7d5f8-110">If you aren't using a separate recruiting application, you can also manually manage candidates in Human Resources.</span></span>

>[!NOTE]
><span data-ttu-id="7d5f8-111">Pokud jste správcem nebo vývojářem a chcete integrovat Human Resources s náborovou aplikací jiných výrobců, přečtěte si [Konfigurace integrace Common Data Service](hr-admin-integration-common-data-service.md) a [Konfigurace virtuální entity Common Data Service](hr-admin-integration-common-data-service-virtual-entities.md)</span><span class="sxs-lookup"><span data-stu-id="7d5f8-111">If you're an admin or developer and want to integrate Human Resources with a third-party recruiting application, see [Configure Common Data Service integration](hr-admin-integration-common-data-service.md) and [Configure Common Data Service virtual entities](hr-admin-integration-common-data-service-virtual-entities.md)</span></span>
>
> <span data-ttu-id="7d5f8-112">Najdete zde také náborové integrační aplikace v [AppSource](https://appsource.microsoft.com/marketplace/apps?search=recruiting%20dynamics).</span><span class="sxs-lookup"><span data-stu-id="7d5f8-112">You can also find recruiting integration apps on [AppSource](https://appsource.microsoft.com/marketplace/apps?search=recruiting%20dynamics).</span></span>
>
> <span data-ttu-id="7d5f8-113">Chcete-li vyzkoušet naši funkci Preview pro integraci s LinkedIn Talent Hub, podívejte se do tématu [Integrace s LinkedIn Talent Hub](hr-admin-integration-linkedin.md).</span><span class="sxs-lookup"><span data-stu-id="7d5f8-113">To try out our preview feature for integrating with LinkedIn Talent Hub, see [Integrate with LinkedIn Talent Hub](hr-admin-integration-linkedin.md).</span></span>

## <a name="enable-recruiting-requests"></a><span data-ttu-id="7d5f8-114">Povolit požadavky na nábor</span><span class="sxs-lookup"><span data-stu-id="7d5f8-114">Enable recruiting requests</span></span>

<span data-ttu-id="7d5f8-115">Pokud chcete odeslat žádosti o nábor v Human Resources, musíte nejprve povolit tuto funkci v části **Parametry Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="7d5f8-115">If you want to submit recruiting requests in Human Resources, you must first enable the functionality in **Human resources parameters**.</span></span>

1. <span data-ttu-id="7d5f8-116">V pracovním prostoru **Správa zaměstnanců** vyberte kartu **Odkazy**.</span><span class="sxs-lookup"><span data-stu-id="7d5f8-116">In the **Personnel management** workspace, select **Links**.</span></span>

2. <span data-ttu-id="7d5f8-117">V části **Nastavení** vyberte **parametry lidských zdrojů**.</span><span class="sxs-lookup"><span data-stu-id="7d5f8-117">Under **Setup**, select **Human resources parameters**.</span></span>

3. <span data-ttu-id="7d5f8-118">Na kartě **Obecné** v části **NÁBOR** nastavte **Povolit žádosti o nábor** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="7d5f8-118">On the **General** tab, under **RECRUITING**, set **Enable recruiting requests** to **Yes**.</span></span>

   ![Povolit požadavky na nábor](./media/hr-recruit-0-enable-requests.png)

## <a name="add-a-recruiting-request-location"></a><span data-ttu-id="7d5f8-120">Přidání umístění žádosti o nábor</span><span class="sxs-lookup"><span data-stu-id="7d5f8-120">Add a recruiting request location</span></span>

<span data-ttu-id="7d5f8-121">Pokud má vaše organizace více umístění, můžete je přidat, aby si žadatelé mohli vybrat místo, kde bude nový nábor probíhat.</span><span class="sxs-lookup"><span data-stu-id="7d5f8-121">If your organization has multiple locations, you can add them so requestors can select a location where the new recruit will be working.</span></span> <span data-ttu-id="7d5f8-122">Umístění bude zahrnuto do publikovaného pracovního místa.</span><span class="sxs-lookup"><span data-stu-id="7d5f8-122">The location will be included in the job posting.</span></span>

1. <span data-ttu-id="7d5f8-123">Do vyhledávacího pole zadejte **umístění žádosti o nábor**.</span><span class="sxs-lookup"><span data-stu-id="7d5f8-123">In the search bar, enter **recruiting request location**.</span></span>

2. <span data-ttu-id="7d5f8-124">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="7d5f8-124">Select **New**.</span></span>

3. <span data-ttu-id="7d5f8-125">V poli **Umístění žádosti o nábor** zadejte název umístění.</span><span class="sxs-lookup"><span data-stu-id="7d5f8-125">In the **Recruiting request location** field, enter the location name.</span></span>

   ![Přidání umístění žádosti o nábor](./media/hr-recruit-0a-add-location.png)

4. <span data-ttu-id="7d5f8-127">Do pole **Popis** zadejte popis umístění.</span><span class="sxs-lookup"><span data-stu-id="7d5f8-127">In the **Description**, enter a description for the location.</span></span>

5. <span data-ttu-id="7d5f8-128">Ve volbě **Umístění** vyberte **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="7d5f8-128">Under **Location**, select **Add**.</span></span> <span data-ttu-id="7d5f8-129">Pokud se otevře okno **Nová adresa**, zadejte adresu umístění.</span><span class="sxs-lookup"><span data-stu-id="7d5f8-129">If the **New address** popout appears, enter the address for the location.</span></span>

   ![Zadejte adresu](./media/hr-recruit-0b-address.png)

6. <span data-ttu-id="7d5f8-131">Pod **Kontaktní informace** zadejte kontaktní informace místa.</span><span class="sxs-lookup"><span data-stu-id="7d5f8-131">Under **Contact information**, enter the information for the location's contact.</span></span>

7. <span data-ttu-id="7d5f8-132">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="7d5f8-132">Select **Save**.</span></span>

## <a name="add-a-recruiting-request"></a><span data-ttu-id="7d5f8-133">Přidání žádosti o nábor</span><span class="sxs-lookup"><span data-stu-id="7d5f8-133">Add a recruiting request</span></span>

<span data-ttu-id="7d5f8-134">Manažeři mohou odesílat žádosti o nábor v Human Resources.</span><span class="sxs-lookup"><span data-stu-id="7d5f8-134">Managers can submit recruiting requests in Human Resources.</span></span> <span data-ttu-id="7d5f8-135">Pokud používáte samostatnou náborovou aplikaci, po dokončení těchto kroků odešlete žádost o nábor a zahájíte proces náboru v této aplikaci.</span><span class="sxs-lookup"><span data-stu-id="7d5f8-135">If you use a separate recruiting application, completing these steps will send a recruiting request and start the recruiting process in that application.</span></span> <span data-ttu-id="7d5f8-136">V opačném případě dokončením tohoto postupu zahájíte pracovní postup pro svůj vlastní interní proces náboru.</span><span class="sxs-lookup"><span data-stu-id="7d5f8-136">Otherwise, complete this procedure to begin the workflow for your own internal recruiting process.</span></span>

1. <span data-ttu-id="7d5f8-137">Vyberte **Samoobsluha pro zaměstnance**.</span><span class="sxs-lookup"><span data-stu-id="7d5f8-137">Select **Employee self service**.</span></span>

2. <span data-ttu-id="7d5f8-138">Vyberte kartu **Můj tým**.</span><span class="sxs-lookup"><span data-stu-id="7d5f8-138">Select the **My team** tab.</span></span>

3. <span data-ttu-id="7d5f8-139">Vyberte **Žádost o nábor**.</span><span class="sxs-lookup"><span data-stu-id="7d5f8-139">Select  **Request to recruit**.</span></span>

   ![Zahájení žádosti o nábor](./media/hr-recruit-1-request-to-recruit.png)

4. <span data-ttu-id="7d5f8-141">Vyplňte pole **Popis**, **Práce** a **Odhadované počáteční datum**.</span><span class="sxs-lookup"><span data-stu-id="7d5f8-141">Complete the **Description**, **Job**, and **Estimated start date** fields.</span></span>

   ![Vyplnění žádosti o nábor](./media/hr-recruit-2-request-to-recruit.png)

5. <span data-ttu-id="7d5f8-143">Vyberte **Pokračovat**.</span><span class="sxs-lookup"><span data-stu-id="7d5f8-143">Select **Continue**.</span></span> <span data-ttu-id="7d5f8-144">Zobrazí se žádost o nábor pro vaši pozici.</span><span class="sxs-lookup"><span data-stu-id="7d5f8-144">The recruiting request for your position appears.</span></span>

6. <span data-ttu-id="7d5f8-145">V části **Obecné** vyberte náboráře z rozevíracího seznamu **Náborář** a poté vyberte umístění z rozevíracího seznamu **Umístění žádosti na nábor**.</span><span class="sxs-lookup"><span data-stu-id="7d5f8-145">Under **General**, select a recruiter from the **Recruiter** dropdown, and then select a location from the **Recruiting request location** dropdown.</span></span>

7. <span data-ttu-id="7d5f8-146">V části **Práce** podle potřeby změňte informace a poté vyberte **Vytvořit podrobnosti z práce**.</span><span class="sxs-lookup"><span data-stu-id="7d5f8-146">Under **Job**, change any information as needed, and then select **Create details from job**.</span></span>

   ![Vytvořte podrobnosti z úlohy](./media/hr-recruit-3-create-details-from-job.png)

   <span data-ttu-id="7d5f8-148">Zbytek žádosti o nábor se naplní výchozími informacemi o zadané práci.</span><span class="sxs-lookup"><span data-stu-id="7d5f8-148">The rest of the recruiting request will populate with the default information for the job you entered.</span></span>

8. <span data-ttu-id="7d5f8-149">V části **Vnější popis** zadejte popis práce, který se bude zobrazovat navenek.</span><span class="sxs-lookup"><span data-stu-id="7d5f8-149">Under **External description**, enter an external-facing job description.</span></span>

9. <span data-ttu-id="7d5f8-150">V části **Pozice** vyberte **Přidat** a poté vyberte pozici pro tuto žádost o nábor.</span><span class="sxs-lookup"><span data-stu-id="7d5f8-150">Under **Positions**, select **Add**, and then select a position for this recruiting request.</span></span>

   ![Přidání pozice](./media/hr-recruit-4-select-position.png)

10. <span data-ttu-id="7d5f8-152">V části **Dovednosti** vyberte **Přidat** a poté vyberte dovednost.</span><span class="sxs-lookup"><span data-stu-id="7d5f8-152">Under **Skills**, select **Add**, and then select a skill.</span></span>

11. <span data-ttu-id="7d5f8-153">V části **Požadavky na vzdělání** vyberte **Přidat** a poté vyberte hodnoty z rozevíracích seznamů **Vzdělání** a **Úroveň vzdělání**.</span><span class="sxs-lookup"><span data-stu-id="7d5f8-153">Under **Educational requirements**, select **Add**, and then select values from the **Education** and **Level of education** dropdowns.</span></span>

   ![Přidání dalších požadavků](./media/hr-recruit-5-select-educational-requirements.png)

12. <span data-ttu-id="7d5f8-155">V části **Komentář** podle potřeby přidávejte komentáře.</span><span class="sxs-lookup"><span data-stu-id="7d5f8-155">Under **Comment**, add comments as necessary.</span></span>

13. <span data-ttu-id="7d5f8-156">V části **Kompenzace** vyberte úroveň z rozevíracího seznamu **Úroveň** a poté upravte **Dolní prahová hodnota**, **Kontrolní bod** a **Horní prahová hodnota**, jak je potřeba.</span><span class="sxs-lookup"><span data-stu-id="7d5f8-156">Under **Compensation**, select a level from the **Level** dropdown, and then adjust **Low threshold**, **Control point**, and **High threshold** as necessary.</span></span>

14. <span data-ttu-id="7d5f8-157">Když je vaše žádost o nábor dokončen a jste připraveni zahájit proces náboru, vyberte **Aktivovat** v řádku nabídek.</span><span class="sxs-lookup"><span data-stu-id="7d5f8-157">When your recruiting request is complete and you're ready to start the recruiting process, select **Activate** in the menu bar.</span></span>

   ![Aktivace žádosti o nábor](./media/hr-recruit-6-activate-recruit-request.png)

15. <span data-ttu-id="7d5f8-159">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="7d5f8-159">Select **Save**.</span></span>

## <a name="view-and-edit-your-recruiting-requests"></a><span data-ttu-id="7d5f8-160">Zobrazení a úpravy žádostí o nábor</span><span class="sxs-lookup"><span data-stu-id="7d5f8-160">View and edit your recruiting requests</span></span>

<span data-ttu-id="7d5f8-161">Pokud jste manažer a chcete zobrazit své vlastní požadavky:</span><span class="sxs-lookup"><span data-stu-id="7d5f8-161">If you're a manager and want to view your own requests:</span></span>

1. <span data-ttu-id="7d5f8-162">Vyberte **Samoobsluha pro zaměstnance**.</span><span class="sxs-lookup"><span data-stu-id="7d5f8-162">Select **Employee self service**.</span></span>

2. <span data-ttu-id="7d5f8-163">Vyberte kartu **Můj tým**.</span><span class="sxs-lookup"><span data-stu-id="7d5f8-163">Select the **My team** tab.</span></span>

3. <span data-ttu-id="7d5f8-164">V části **Informace o mém týmu** vyberte kartu **Žádosti o nábor**.</span><span class="sxs-lookup"><span data-stu-id="7d5f8-164">Under **My team information**, select the **Recruiting requests** tab.</span></span>

   ![Výběr karty Žádosti o nábor](./media/hr-recruit-7-recruiting-requests.png)

4. <span data-ttu-id="7d5f8-166">Chcete-li zobrazit nebo upravit žádost o nábor, vyberte jej v mřížce.</span><span class="sxs-lookup"><span data-stu-id="7d5f8-166">To view or edit a recruiting request, select it in the grid.</span></span>

<span data-ttu-id="7d5f8-167">Pokud jste personalista a chcete zobrazit všechny žádosti o nábor:</span><span class="sxs-lookup"><span data-stu-id="7d5f8-167">If you're an HR pro and want to view all recruiting requests:</span></span>

1. <span data-ttu-id="7d5f8-168">Vyberte **Správa zaměstnanců**.</span><span class="sxs-lookup"><span data-stu-id="7d5f8-168">Select **Personnel management**.</span></span>

2. <span data-ttu-id="7d5f8-169">Vyberte **Žádosti o nábor**.</span><span class="sxs-lookup"><span data-stu-id="7d5f8-169">Select **Recruiting requests**.</span></span>

   ![Zobrazení žádostí o nábor ve správě zaměstnanců](./media/hr-recruit-8-recruiting-requests-personnel-management.png)

3. <span data-ttu-id="7d5f8-171">Chcete-li zobrazit nebo upravit žádost o nábor, vyberte jej v mřížce.</span><span class="sxs-lookup"><span data-stu-id="7d5f8-171">To view or edit a recruiting request, select it in the grid.</span></span>

## <a name="add-or-edit-a-candidate-profile"></a><span data-ttu-id="7d5f8-172">Přidání nebo úprava profilu kandidáta</span><span class="sxs-lookup"><span data-stu-id="7d5f8-172">Add or edit a candidate profile</span></span>

<span data-ttu-id="7d5f8-173">Pokud vaše organizace integrovala jinou aplikaci pro správu žádostí o nábor, žádosti o nábor se předají této aplikaci.</span><span class="sxs-lookup"><span data-stu-id="7d5f8-173">If your organization has integrated with another application to manage recruiting requests, recruiting requests are forwarded to that application.</span></span> <span data-ttu-id="7d5f8-174">Náborová aplikace poté odešle informace o kandidátovi zpět do Human Resources.</span><span class="sxs-lookup"><span data-stu-id="7d5f8-174">The recruiting application then sends candidate information back to Human Resources.</span></span> <span data-ttu-id="7d5f8-175">V opačném případě můžete sledovat vlastní interní procesy náboru a zadávat informace o kandidátech ručně.</span><span class="sxs-lookup"><span data-stu-id="7d5f8-175">Otherwise, you can follow your own internal recruiting processes and enter candidate information manually.</span></span>

1. <span data-ttu-id="7d5f8-176">Vyberte **Správa zaměstnanců**.</span><span class="sxs-lookup"><span data-stu-id="7d5f8-176">Select **Personnel management**.</span></span>

2. <span data-ttu-id="7d5f8-177">Vybrerte **Odkazy**.</span><span class="sxs-lookup"><span data-stu-id="7d5f8-177">Select **Links**.</span></span>

3. <span data-ttu-id="7d5f8-178">V části **Nábor** vyberte **Kandidáti**.</span><span class="sxs-lookup"><span data-stu-id="7d5f8-178">Under **Recruiting**, select **Candidates**.</span></span>

   ![Zobrazení kandidátů](./media/hr-recruit-9-candidates.png)

4. <span data-ttu-id="7d5f8-180">Chcete-li přidat kandidáta, vyberte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="7d5f8-180">To add a candidate, select **New**.</span></span> <span data-ttu-id="7d5f8-181">Chcete-li upravit existujícího kandidáta, vyberte jej ze seznamu a pak vyberte možnost **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="7d5f8-181">To edit an existing candidate, select the candidate from the list and then select **Edit**.</span></span> <span data-ttu-id="7d5f8-182">Zobrazí se profil kandidáta.</span><span class="sxs-lookup"><span data-stu-id="7d5f8-182">The candidate profile appears.</span></span>

5. <span data-ttu-id="7d5f8-183">V části **Souhrn kandidáta** podle potřeby zadejte nebo upravte informace o kandidátovi.</span><span class="sxs-lookup"><span data-stu-id="7d5f8-183">Under **Candidate summary**, enter or edit the candidate information as necessary.</span></span>

6. <span data-ttu-id="7d5f8-184">V části **Žádosti o nábor** vyberte žádost o nábor, se kterou chcete kandidáta propojit.</span><span class="sxs-lookup"><span data-stu-id="7d5f8-184">Under **Recruiting request**, select a recruiting request to link the candidate to.</span></span> <span data-ttu-id="7d5f8-185">Poté dle potřeby vyplňte pole **Odhadované počáteční datum**, **Náborový manažer**, **Pozice** a **Popis**.</span><span class="sxs-lookup"><span data-stu-id="7d5f8-185">Then complete the **Estimated start date**, **Hiring manager**, **Position**, and **Description fields** as appropriate.</span></span>

   ![Odkaz na žádost o nábor](./media/hr-recruit-10-link-to-recruiting-request.png)

7. <span data-ttu-id="7d5f8-187">Vyplňte všechny informace v následujících oblastech, které chcete zahrnout do záznamu kandidáta:</span><span class="sxs-lookup"><span data-stu-id="7d5f8-187">Complete all the information in the following areas that you want to include in the candidate's record:</span></span>
   - <span data-ttu-id="7d5f8-188">**Komentáře**</span><span class="sxs-lookup"><span data-stu-id="7d5f8-188">**Comments**</span></span>
   - <span data-ttu-id="7d5f8-189">**Profesionální zkušenosti**</span><span class="sxs-lookup"><span data-stu-id="7d5f8-189">**Professional experience**</span></span>
   - <span data-ttu-id="7d5f8-190">**Kontaktní informace**</span><span class="sxs-lookup"><span data-stu-id="7d5f8-190">**Contact information**</span></span>
   - <span data-ttu-id="7d5f8-191">**Vzdělání**</span><span class="sxs-lookup"><span data-stu-id="7d5f8-191">**Education**</span></span>
   - <span data-ttu-id="7d5f8-192">**Dovednosti**</span><span class="sxs-lookup"><span data-stu-id="7d5f8-192">**Skills**</span></span>
   - <span data-ttu-id="7d5f8-193">**Certifikáty**</span><span class="sxs-lookup"><span data-stu-id="7d5f8-193">**Certificates**</span></span>
   - <span data-ttu-id="7d5f8-194">**Prověřování**</span><span class="sxs-lookup"><span data-stu-id="7d5f8-194">**Screenings**</span></span>

8. <span data-ttu-id="7d5f8-195">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="7d5f8-195">Select **Save**.</span></span>

## <a name="hire-a-candidate"></a><span data-ttu-id="7d5f8-196">Přijetí kandidáta</span><span class="sxs-lookup"><span data-stu-id="7d5f8-196">Hire a candidate</span></span>

<span data-ttu-id="7d5f8-197">Až budete připraveni přijmout kandidáta, postupujte podle tohoto postupu a přeměňte kandidáta na zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="7d5f8-197">When you're ready to hire a candidate, follow this procedure to transition the candidate to an employee.</span></span>

1. <span data-ttu-id="7d5f8-198">Na formuláři kandidáta vyberte **Přijmout**.</span><span class="sxs-lookup"><span data-stu-id="7d5f8-198">On the candidate form, select **Hire**.</span></span>

   ![Přijetí kandidáta](./media/hr-recruit-11-hire.png)

2. <span data-ttu-id="7d5f8-200">Ve formuláři **Přijetí nového pracovníka** pod **Podrobnosti** vyplňte všechna pole.</span><span class="sxs-lookup"><span data-stu-id="7d5f8-200">On the **Hire new worker** form, under **Details**, complete all the fields.</span></span>

   ![Zadání podrobností nového zaměstnance](./media/hr-recruit-12-hire-new-worker.png)

3. <span data-ttu-id="7d5f8-202">Pod **Podrobnosti o pozici** ověřte a podle potřeby změňte informace.</span><span class="sxs-lookup"><span data-stu-id="7d5f8-202">Under **Position details**, verify and change information as necessary.</span></span>

4. <span data-ttu-id="7d5f8-203">V části **Kontrolní seznamy náboru** vyberte příslušné kontrolní seznamy náboru pro tohoto zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="7d5f8-203">Under **Onboarding checklists**, select the relevant onboarding checklists for this employee.</span></span>

5. <span data-ttu-id="7d5f8-204">Volbou **Pokračovat** vytvoříte záznam zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="7d5f8-204">Select **Continue** to create the employee record.</span></span>

   >[!NOTE]
   ><span data-ttu-id="7d5f8-205">V závislosti na pracovních postupech vaší organizace může záznam kandidáta projít dalšími schvalovacími kroky, než se stane záznamem zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="7d5f8-205">Depending on your organization's workflows, the candidate record may go through additional approval steps before becoming an employee record.</span></span>

## <a name="decide-not-to-hire-a-candidate"></a><span data-ttu-id="7d5f8-206">Rozhodnutí o nepřijatí kandidáta</span><span class="sxs-lookup"><span data-stu-id="7d5f8-206">Decide not to hire a candidate</span></span>

<span data-ttu-id="7d5f8-207">Pokud se rozhodnete kandidáta nepřijmout, postupujte podle tohoto postupu, kterým jej vyřadíte z procesu prověřování.</span><span class="sxs-lookup"><span data-stu-id="7d5f8-207">If you decide not to hire a candidate, follow this procedure to remove them from the vetting process.</span></span> 

1. <span data-ttu-id="7d5f8-208">Na formuláři kandidáta vyberte **Nepřijmout**.</span><span class="sxs-lookup"><span data-stu-id="7d5f8-208">On the candidate form, select **Do not hire**.</span></span>

   ![Nepřijetí kandidáta](./media/hr-recruit-13-do-not-hire.png)

2. <span data-ttu-id="7d5f8-210">Vyberte **Kód důvodu** a přidejte veškeré potřebné komentáře.</span><span class="sxs-lookup"><span data-stu-id="7d5f8-210">Select a **Reason code** and include any comments.</span></span>

3. <span data-ttu-id="7d5f8-211">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="7d5f8-211">Select **OK**.</span></span>

## <a name="dismiss-a-candidate"></a><span data-ttu-id="7d5f8-212">Propuštění kandidáta</span><span class="sxs-lookup"><span data-stu-id="7d5f8-212">Dismiss a candidate</span></span>

<span data-ttu-id="7d5f8-213">V případě potřeby můžete kandidáta poté, co ho přijmete, propustit.</span><span class="sxs-lookup"><span data-stu-id="7d5f8-213">If needed, you can dismiss a candidate after hiring them.</span></span> <span data-ttu-id="7d5f8-214">Například kandidát může vaši nabídku odmítnout nebo se neobjeví hned první den.</span><span class="sxs-lookup"><span data-stu-id="7d5f8-214">For example, a candidate might reject your offer or not show up on their first day.</span></span>

- <span data-ttu-id="7d5f8-215">Na formuláři kandidáta vyberte **Propustit kandidáta**.</span><span class="sxs-lookup"><span data-stu-id="7d5f8-215">On the candidate form, select **Dismiss candidate**.</span></span>

  ![Zamítnout kandidáta](./media/hr-recruit-14-dismiss-candidate.png)

## <a name="see-also"></a><span data-ttu-id="7d5f8-217">Viz také</span><span class="sxs-lookup"><span data-stu-id="7d5f8-217">See also</span></span>

[<span data-ttu-id="7d5f8-218">Konfigurace virtuálních entit Common Data Service</span><span class="sxs-lookup"><span data-stu-id="7d5f8-218">Configure Common Data Service virtual entities</span></span>](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[<span data-ttu-id="7d5f8-219">Organizování zaměstnanců</span><span class="sxs-lookup"><span data-stu-id="7d5f8-219">Organize your workforce</span></span>](hr-personnel-departments-jobs-positions.md)<br>
[<span data-ttu-id="7d5f8-220">Nastavení komponent práce</span><span class="sxs-lookup"><span data-stu-id="7d5f8-220">Set up the components of a job</span></span>](hr-personnel-jobs.md)