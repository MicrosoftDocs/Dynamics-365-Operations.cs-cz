---
title: Mapové dovednosti
description: Můžete vytvořit vyhledávání mapování dovedností a vyhledat kvalifikovanou osobu v Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSkill, HcmSkillGapProfile, HcmSkillMapping, HcmSkillType, HcmEmployeeDevelopmentWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 3361
ms.assetid: c2ce94c0-933d-4edb-822c-7f0e7b49e4ee
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 03b7860fbde89097141cfe48f2c240dc127aa9c3
ms.sourcegitcommit: 48528233e0f02dbd47e96e030254ef65f2bb899e
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/20/2021
ms.locfileid: "6076581"
---
# <a name="map-skills"></a><span data-ttu-id="32077-103">Mapové dovednosti</span><span class="sxs-lookup"><span data-stu-id="32077-103">Map skills</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="32077-104">Můžete vytvořit vyhledávání mapování dovedností a vyhledat kvalifikovanou osobu v Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="32077-104">You can create a skill-mapping search to find a qualified person in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="32077-105">Hledání mapování dovedností vrátí výsledky pro zadaná kritéria prohlédnutím následujících informací:</span><span class="sxs-lookup"><span data-stu-id="32077-105">Skill-mapping searches return results for criteria you enter by looking through the following information:</span></span>

- <span data-ttu-id="32077-106">Dovednosti</span><span class="sxs-lookup"><span data-stu-id="32077-106">Skills</span></span>
- <span data-ttu-id="32077-107">Vzdělání</span><span class="sxs-lookup"><span data-stu-id="32077-107">Education</span></span>
- <span data-ttu-id="32077-108">Certifikáty</span><span class="sxs-lookup"><span data-stu-id="32077-108">Certificates</span></span>
- <span data-ttu-id="32077-109">Pozice</span><span class="sxs-lookup"><span data-stu-id="32077-109">Positions</span></span>
- <span data-ttu-id="32077-110">Zkušenost z projektu</span><span class="sxs-lookup"><span data-stu-id="32077-110">Project experience</span></span>

<span data-ttu-id="32077-111">Například můžete najít lidi ve vaší organizaci, kteří získali CPA.</span><span class="sxs-lookup"><span data-stu-id="32077-111">For example, you can find people in your organization who have earned their CPA.</span></span>

<span data-ttu-id="32077-112">Profily mapování dovedností umožňují vyhledání aktuálního zaměstnance nebo kandidáta s kvalifikací, která přímo odpovídá obchodním potřebám.</span><span class="sxs-lookup"><span data-stu-id="32077-112">Skill-mapping profiles allow you to find current employees or candidates with qualifications that directly correspond to business needs.</span></span>

> [!NOTE]
> <span data-ttu-id="32077-113">V seznamu s výsledky mapování dovednosti budou zobrazeni nebo zahrnuti v profilu dovedností pouze zaměstnanci, uchazeči a kontaktní osoby, které jsou vybrány k zahrnutí do hledání v rámci mapování dovedností.</span><span class="sxs-lookup"><span data-stu-id="32077-113">Only workers, applicants, and contact persons who are selected to be included in skill-mapping searches will display in a skill-mapping results list, or be included in a skill profile.</span></span> <span data-ttu-id="32077-114">Chcete-li zahrnout osobu do vyhledávání v rámci mapování dovedností, nastavte možnost **Zahrnout do mapování dovedností** na hodnotu **Ano** na následujících stránkách:</span><span class="sxs-lookup"><span data-stu-id="32077-114">To include a person in skill mapping searches, set the **Include in skill mapping** selection to **Yes** in the following pages:</span></span><br>
> - <span data-ttu-id="32077-115">Pracovní podproces</span><span class="sxs-lookup"><span data-stu-id="32077-115">Worker</span></span><br>
> - <span data-ttu-id="32077-116">Zaměstnanec</span><span class="sxs-lookup"><span data-stu-id="32077-116">Employee</span></span><br>
> - <span data-ttu-id="32077-117">Uchazeč</span><span class="sxs-lookup"><span data-stu-id="32077-117">Applicant</span></span><br>
> - <span data-ttu-id="32077-118">Kontakty</span><span class="sxs-lookup"><span data-stu-id="32077-118">Contacts</span></span><br>

<span data-ttu-id="32077-119">Chcete-li vytvořit mapování dovedností, přejděte na **Rozvoj zaměstnanců > Odkazy > Mapování dovedností**.</span><span class="sxs-lookup"><span data-stu-id="32077-119">To create a skill mapping, go to **Employee development > Links > Skill mapping**.</span></span> <span data-ttu-id="32077-120">Chcete-li vytvořit profil mapování dovedností, přejděte na **Rozvoj zaměstnanců > Odkazy > Profily mapování dovedností**.</span><span class="sxs-lookup"><span data-stu-id="32077-120">To create a skill-mapping profile, go to **Employee development > Links > Skill mapping profiles**.</span></span>

## <a name="skill-gap-analysis-and-skill-profile-analysis"></a><span data-ttu-id="32077-121">Analýza mezer v dovednostech a analýza profilu dovedností</span><span class="sxs-lookup"><span data-stu-id="32077-121">Skill gap analysis and skill profile analysis</span></span>

<span data-ttu-id="32077-122">Můžete vytvořit analýzu profilu dovedností a zobrazit seznam kompetencí dané osoby.</span><span class="sxs-lookup"><span data-stu-id="32077-122">You can create a skill profile analysis to view a list of a person's competencies.</span></span> <span data-ttu-id="32077-123">Můžete vytvořit analýzy dovednostních mezer k porovnání dovedností dané osoby s dovednostmi požadovanými pro úlohu.</span><span class="sxs-lookup"><span data-stu-id="32077-123">You can create a skill gap analysis to compare a person’s skills and the skills required for a job.</span></span>

<span data-ttu-id="32077-124">Chcete-li vytvořit analýzu mezer, přejděte na **Rozvoj zaměstnanců > Odkazy > Úloha analýzy mezer v dovednostech - osoba**.</span><span class="sxs-lookup"><span data-stu-id="32077-124">To create a gap analysis, go to **Employee development > Links > Skill gap analysis job - person**.</span></span> <span data-ttu-id="32077-125">Chcete-li vytvořit analýzu profilu dovedností, přejděte na **Rozvoj zaměstnanců > Odkazy > Analýza profilu dovedností**.</span><span class="sxs-lookup"><span data-stu-id="32077-125">To create a skill profile analysis, go to **Employee development > Links > Skill profile analysis**.</span></span>

## <a name="see-also"></a><span data-ttu-id="32077-126">Viz také</span><span class="sxs-lookup"><span data-stu-id="32077-126">See also</span></span>

[<span data-ttu-id="32077-127">Nakonfigurujte dovednosti</span><span class="sxs-lookup"><span data-stu-id="32077-127">Configure skills</span></span>](hr-develop-skills.md)<br>
[<span data-ttu-id="32077-128">Zadejte dovednosti</span><span class="sxs-lookup"><span data-stu-id="32077-128">Enter skills</span></span>](hr-develop-enter-skills.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]