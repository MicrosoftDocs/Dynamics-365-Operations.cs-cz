---
title: Mobilní pracovní prostor pro schválení faktur
description: Toto téma obsahuje informace o mobilním pracovním prostoru Schválení faktur. Tento pracovní prostor obsahuje seznam faktur, které vám byly přiřazeny v procesu workflowu záhlaví faktury dodavatele.
author: abruer
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: d4ea1d81b0e4f92974ceb7d46386c9d9f6e48979
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/30/2019
ms.locfileid: "2248996"
---
# <a name="invoice-approvals-mobile-workspace"></a><span data-ttu-id="e6759-104">Mobilní pracovní prostor pro schválení faktur</span><span class="sxs-lookup"><span data-stu-id="e6759-104">Invoice approvals mobile workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e6759-105">Toto téma obsahuje informace o mobilním pracovním prostoru **Schválení faktur**.</span><span class="sxs-lookup"><span data-stu-id="e6759-105">This topic provides information about the **Invoice approvals** mobile workspace.</span></span> <span data-ttu-id="e6759-106">Tento pracovní prostor obsahuje seznam faktur, které vám byly přiřazeny v procesu workflowu záhlaví faktury dodavatele.</span><span class="sxs-lookup"><span data-stu-id="e6759-106">This workspace provides a list of invoices that have been assigned to you through the vendor invoice header workflow process.</span></span> 

<span data-ttu-id="e6759-107">Tento mobilní pracovní prostor je určen k použití s mobilní aplikací Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e6759-107">This mobile workspace is intended to be used with the Finance and Operations mobile app.</span></span>

## <a name="overview"></a><span data-ttu-id="e6759-108">Přehled</span><span class="sxs-lookup"><span data-stu-id="e6759-108">Overview</span></span>

<span data-ttu-id="e6759-109">V mobilním pracovním prostoru **Schválení faktur** si úředníci a manažeři v oblasti závazků mohou prohlížet faktury, které jim byly přiřazeny v rámci procesu workflowu záhlaví faktury dodavatele.</span><span class="sxs-lookup"><span data-stu-id="e6759-109">The **Invoice approvals** mobile workspace lets Accounts payable clerks and managers view invoices that have been assigned to them as part of the vendor invoice header workflow process.</span></span> <span data-ttu-id="e6759-110">Můžete si prohlížet informace o faktuře i podrobnosti o řádcích a distribuci, abyste se s jejich pomocí mohli lépe rozhodovat při schvalování.</span><span class="sxs-lookup"><span data-stu-id="e6759-110">You can view the invoice information, and even the line and distribution details, to help you make informed approval decisions.</span></span> <span data-ttu-id="e6759-111">V pracovním prostoru můžete provádět příslušná opatření a posouvat faktury dále v procesu workflowu.</span><span class="sxs-lookup"><span data-stu-id="e6759-111">From the workspace, you can take action to move the invoice through the workflow process.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="e6759-112">Požadavky</span><span class="sxs-lookup"><span data-stu-id="e6759-112">Prerequisites</span></span>

<span data-ttu-id="e6759-113">Před použitím tohoto mobilního pracovního prostoru musí být splněny následující předpoklady.</span><span class="sxs-lookup"><span data-stu-id="e6759-113">Before you can use this mobile workspace, the following prerequisites must be met.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e6759-114">Předpoklad</span><span class="sxs-lookup"><span data-stu-id="e6759-114">Prerequisite</span></span></th>
<th><span data-ttu-id="e6759-115">Role</span><span class="sxs-lookup"><span data-stu-id="e6759-115">Role</span></span></th>
<th><span data-ttu-id="e6759-116">Popis</span><span class="sxs-lookup"><span data-stu-id="e6759-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e6759-117">Microsoft Dynamics 365 Finance musí být nasazen ve vaší organizaci.</span><span class="sxs-lookup"><span data-stu-id="e6759-117">Microsoft Dynamics 365 Finance must be deployed in your organization.</span></span></td>
<td><span data-ttu-id="e6759-118">Správce systému</span><span class="sxs-lookup"><span data-stu-id="e6759-118">System administrator</span></span></td>
<td><span data-ttu-id="e6759-119">Viz část <a href="../deployment/deploy-demo-environment.md">Nasazení ukázkového prostředí</a>.</span><span class="sxs-lookup"><span data-stu-id="e6759-119">See <a href="../deployment/deploy-demo-environment.md">Deploy a demo environment</a>.</span></span>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="e6759-120">Mobilní pracovní prostor <strong>Schválení faktur</strong> musí být publikován.</span><span class="sxs-lookup"><span data-stu-id="e6759-120">The <strong>Invoice approvals</strong> mobile workspace must be published.</span></span></td>
<td><span data-ttu-id="e6759-121">Správce systému</span><span class="sxs-lookup"><span data-stu-id="e6759-121">System administrator</span></span></td>
<td><span data-ttu-id="e6759-122">Viz téma <a href="publish-mobile-workspace.md">Publikování mobilního pracovního prostoru</a>.</span><span class="sxs-lookup"><span data-stu-id="e6759-122">See <a href="publish-mobile-workspace.md">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="e6759-123">Stáhněte a nainstalujte mobilní aplikaci</span><span class="sxs-lookup"><span data-stu-id="e6759-123">Download and install the mobile app</span></span>

<span data-ttu-id="e6759-124">Stáhněte a nainstalujte mobilní aplikaci Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="e6759-124">Download and install the Finance and Operations mobile app:</span></span>

-   [<span data-ttu-id="e6759-125">Pro telefony Android</span><span class="sxs-lookup"><span data-stu-id="e6759-125">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
-   [<span data-ttu-id="e6759-126">Pro telefony iPhone</span><span class="sxs-lookup"><span data-stu-id="e6759-126">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="e6759-127">Přihlaste se do mobilní aplikace</span><span class="sxs-lookup"><span data-stu-id="e6759-127">Sign in to the mobile app</span></span>

1.  <span data-ttu-id="e6759-128">Spusťte aplikaci na svém mobilním zařízení.</span><span class="sxs-lookup"><span data-stu-id="e6759-128">Start the app on your mobile device.</span></span>
2.  <span data-ttu-id="e6759-129">Zadejte URL adresu Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="e6759-129">Enter your Microsoft Dynamics 365 URL.</span></span>
3.  <span data-ttu-id="e6759-130">Při prvním přihlášení se zobrazí výzva k zadání uživatelského jména a hesla.</span><span class="sxs-lookup"><span data-stu-id="e6759-130">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="e6759-131">Zadejte své přihlašovací údaje.</span><span class="sxs-lookup"><span data-stu-id="e6759-131">Enter your credentials.</span></span>
4.  <span data-ttu-id="e6759-132">Po přihlášení se zobrazí dostupné pracovní prostory pro vaši společnost.</span><span class="sxs-lookup"><span data-stu-id="e6759-132">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="e6759-133">Všimněte si, že pokud správce systému později publikuje nový pracovní prostor, budete muset aktualizovat seznam mobilních pracovních prostorů.</span><span class="sxs-lookup"><span data-stu-id="e6759-133">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

    <span data-ttu-id="e6759-134">[![Vyžádání aktualizace](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="e6759-134">[![Pull to refresh](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span></span>

## <a name="approve-invoices-by-using-the-invoice-approvals-mobile-workspace"></a><span data-ttu-id="e6759-135">Schválení faktur pomocí mobilního pracovního prostoru Schválení faktur</span><span class="sxs-lookup"><span data-stu-id="e6759-135">Approve invoices by using the Invoice approvals mobile workspace</span></span>
1.  <span data-ttu-id="e6759-136">Ve svém mobilním zařízení vyberte pracovní prostor **Schválení faktur**.</span><span class="sxs-lookup"><span data-stu-id="e6759-136">On your mobile device, select the **Invoice approvals** workspace.</span></span>
2.  <span data-ttu-id="e6759-137">Vyberte fakturu, která vám byla přiřazena procesem workflowu záhlaví faktury dodavatele.</span><span class="sxs-lookup"><span data-stu-id="e6759-137">Select the invoice that has been assigned to you by the vendor invoice header workflow process.</span></span>
3.  <span data-ttu-id="e6759-138">Na stránce **Podrobnosti faktury** zkontrolujte informace záhlaví faktury, například informace o dodavateli a datu.</span><span class="sxs-lookup"><span data-stu-id="e6759-138">On the **Invoice details** page, review the invoice header information, such as the vendor and date information.</span></span>
4.  <span data-ttu-id="e6759-139">Výběrem řádku faktury zobrazíte podrobnější informace v zobrazení **Podrobnosti řádku faktury**.</span><span class="sxs-lookup"><span data-stu-id="e6759-139">Select a line on the invoice to view more detailed information about it in the **Invoice line details** view.</span></span>
5.  <span data-ttu-id="e6759-140">V zobrazení **Podrobnosti řádku faktury** můžete výběrem možnosti **Distribuce** zobrazit distribuce řádků.</span><span class="sxs-lookup"><span data-stu-id="e6759-140">In the **Invoice line details** view, select **Distributions** to show the line distributions.</span></span> <span data-ttu-id="e6759-141">Zde si můžete prohlédnout účetnictví spojené s řádkem faktury.</span><span class="sxs-lookup"><span data-stu-id="e6759-141">Here, you can view the accounting for the invoice line.</span></span> <span data-ttu-id="e6759-142">K zobrazeným informacím patří finanční dimenze a hlavní účet.</span><span class="sxs-lookup"><span data-stu-id="e6759-142">The information that is shown includes the financial dimensions and the main account.</span></span>
6.  <span data-ttu-id="e6759-143">Na stránce **Podrobnosti faktury** můžete výběrem možnosti **Distribuce** zobrazit všechny distribuce.</span><span class="sxs-lookup"><span data-stu-id="e6759-143">On the **Invoice details** page, select **Distributions** to show all distributions.</span></span> <span data-ttu-id="e6759-144">Zde si můžete prohlédnout účetnictví spojené s celou fakturou.</span><span class="sxs-lookup"><span data-stu-id="e6759-144">Here, you can view the accounting for the whole invoice.</span></span> <span data-ttu-id="e6759-145">K zobrazeným informacím patří finanční dimenze a hlavní účty.</span><span class="sxs-lookup"><span data-stu-id="e6759-145">The information that is shown includes the financial dimensions and the main accounts.</span></span> 
7.  <span data-ttu-id="e6759-146">Výběrem možnosti **Přílohy** zobrazíte další poznámky nebo soubory, které jsou připojeny k faktuře.</span><span class="sxs-lookup"><span data-stu-id="e6759-146">Select **Attachments** to view any notes or files that are attached to the invoice.</span></span>
8.  <span data-ttu-id="e6759-147">Na stránce **Podrobnosti faktury** vyberte požadovanou akci workflowu a dokončete tak proces kontroly.</span><span class="sxs-lookup"><span data-stu-id="e6759-147">On the **Invoice details** page, select the appropriate workflow action to complete your review process.</span></span>
9.  <span data-ttu-id="e6759-148">Vyberte **Hotovo**.</span><span class="sxs-lookup"><span data-stu-id="e6759-148">Select **Done**.</span></span>
