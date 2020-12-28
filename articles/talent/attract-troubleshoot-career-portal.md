---
title: Uživatelé aplikace Attract nemohou žádat o zaměstnání z kariérního portálu
description: Toto téma vysvětluje, jak řešit problém, kdy uživatelé Attract nemohou žádat o zaměstnání z kariérního portálu.
author: andreabichsel
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-09-23
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: e1d72bef6d8bbe15e27326f66341915ba44a09b4
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460533"
---
# <a name="attract-users-cant-apply-for-jobs-from-career-portal"></a><span data-ttu-id="ed9ac-103">Uživatelé aplikace Attract nemohou žádat o zaměstnání z kariérního portálu</span><span class="sxs-lookup"><span data-stu-id="ed9ac-103">Attract users can't apply for jobs from career portal</span></span>

[!include [banner](includes/banner.md)]

## <a name="issue"></a><span data-ttu-id="ed9ac-104">Výdej</span><span class="sxs-lookup"><span data-stu-id="ed9ac-104">Issue</span></span>

<span data-ttu-id="ed9ac-105">Uživatelé aplikace Attract nemohou žádat o zaměstnání z kariérního portálu.</span><span class="sxs-lookup"><span data-stu-id="ed9ac-105">Attract users can't apply for jobs from the career portal.</span></span> <span data-ttu-id="ed9ac-106">Když se snaží ucházet o práci, která byla vytvořena v Dynamics 365 Talent: Attract, prohlížeč načítá stránku průběžně a nedokončí akci.</span><span class="sxs-lookup"><span data-stu-id="ed9ac-106">When they try to apply for a job that was created in Dynamics 365 Talent: Attract, the browser loads the page continuously and doesn't complete the action.</span></span>

## <a name="cause"></a><span data-ttu-id="ed9ac-107">Příčina</span><span class="sxs-lookup"><span data-stu-id="ed9ac-107">Cause</span></span>

<span data-ttu-id="ed9ac-108">K tomuto problému dochází, když tým pro vztahy s talenty nemá uživatelskou roli Talent.</span><span class="sxs-lookup"><span data-stu-id="ed9ac-108">This problem occurs when the Talent Relationship Team doesn't have the Talent user role.</span></span>

## <a name="resolution"></a><span data-ttu-id="ed9ac-109">Rozlišení</span><span class="sxs-lookup"><span data-stu-id="ed9ac-109">Resolution</span></span>

<span data-ttu-id="ed9ac-110">Přiřaďte roli uživatele Talent týmu pro vztahy s talenty.</span><span class="sxs-lookup"><span data-stu-id="ed9ac-110">Assign the Talent user role to the Talent Relationship Team.</span></span>

1. <span data-ttu-id="ed9ac-111">Přihlaste se do [centra pro správu Power Platform](https://admin.powerplatform.microsoft.com) s některým z následujících pověření správce:</span><span class="sxs-lookup"><span data-stu-id="ed9ac-111">Sign in to the [Power Platform admin center](https://admin.powerplatform.microsoft.com) with any of the following admin credentials:</span></span>

   - <span data-ttu-id="ed9ac-112">Správce Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="ed9ac-112">Dynamics 365 admin</span></span>
   - <span data-ttu-id="ed9ac-113">Globální správce</span><span class="sxs-lookup"><span data-stu-id="ed9ac-113">Global admin</span></span>
   - <span data-ttu-id="ed9ac-114">Správce Power Platform</span><span class="sxs-lookup"><span data-stu-id="ed9ac-114">Power Platform admin</span></span>

2. <span data-ttu-id="ed9ac-115">V navigačním podokně vyberte **Prostředí** a poté vyberte prostředí, ve kterém přiřadíte uživatelskou roli Talent týmu pro vztahy s talenty.</span><span class="sxs-lookup"><span data-stu-id="ed9ac-115">In the navigation pane, select **Environments**, and then select the environment in which to assign the Talent user role to the Talent Relationship Team.</span></span>

   ![Výběr prostředí](./media/attract-troubleshoot-career-portal-select-environment.png)

3. <span data-ttu-id="ed9ac-117">V podokně **Prostředí** vyberte **Adresa URL prostředí** a přihlaste se k portálu pro správu prostředí (například https:<orgname>.crm.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="ed9ac-117">In the **Environments** pane, select the **Environment URL** and sign in to the environment's admin portal (for example, https:<orgname>.crm.dynamics.com).</span></span>

4. <span data-ttu-id="ed9ac-118">Vyberte **Nastavení**, vyberte **Systém** a potom vyberte **Zabezpečení**.</span><span class="sxs-lookup"><span data-stu-id="ed9ac-118">Select **Settings**, select **System**, and then select **Security**.</span></span>

   ![Přechod na Zabezpečení](./media/attract-troubleshoot-career-portal-security.png)

5. <span data-ttu-id="ed9ac-120">Vyberte **Týmy**.</span><span class="sxs-lookup"><span data-stu-id="ed9ac-120">Select **Teams**.</span></span>

   ![Výběr položky Týmy](./media/attract-troubleshoot-career-portal-security-teams.png)

6. <span data-ttu-id="ed9ac-122">Do vyhledávacího pole zadejte **Tým pro vztahy s talenty** a poté vyberte tým z výsledků vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="ed9ac-122">Search for **Talent Relationship Team** in the search box, and then select the team from the search results.</span></span>

7. <span data-ttu-id="ed9ac-123">Z pásu karet vyberte **SPRAVOVAT ROLE**.</span><span class="sxs-lookup"><span data-stu-id="ed9ac-123">Select **MANAGE ROLES** from the ribbon.</span></span>

8. <span data-ttu-id="ed9ac-124">V dialogovém okně **Správa rolí týmu** vyberte **Uživatel Talent** ze seznamu dostupných rolí a poté vyberte **OK** pro použití role.</span><span class="sxs-lookup"><span data-stu-id="ed9ac-124">In the **Manage Team Roles** dialog, select **Talent user** from the list of available roles, and then select **OK** to apply the role.</span></span>

   ![Použití role](./media/attract-troubleshoot-career-portal-apply-role.png)

9. <span data-ttu-id="ed9ac-126">Otestujte změny:</span><span class="sxs-lookup"><span data-stu-id="ed9ac-126">Test your changes:</span></span>

   1. <span data-ttu-id="ed9ac-127">Přihlaste se na kariérní portál z nového okna prohlížeče.</span><span class="sxs-lookup"><span data-stu-id="ed9ac-127">Sign in to the career portal from a new browser window.</span></span>
   2. <span data-ttu-id="ed9ac-128">Požádejte o práci z kariérního portálu.</span><span class="sxs-lookup"><span data-stu-id="ed9ac-128">Apply for the job from the career portal.</span></span> 