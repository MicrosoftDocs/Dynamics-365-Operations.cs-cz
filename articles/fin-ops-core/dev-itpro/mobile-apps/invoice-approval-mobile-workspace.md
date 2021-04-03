---
title: Mobilní pracovní prostor pro schválení faktur
description: Toto téma obsahuje informace o mobilním pracovním prostoru Schválení faktur.
author: abruer
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 3d90b89900b35bce648841aa9e49737a25309ce2
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570063"
---
# <a name="invoice-approvals-mobile-workspace"></a><span data-ttu-id="b6ea8-103">Mobilní pracovní prostor pro schválení faktur</span><span class="sxs-lookup"><span data-stu-id="b6ea8-103">Invoice approvals mobile workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b6ea8-104">Toto téma obsahuje informace o mobilním pracovním prostoru **Schválení faktur**.</span><span class="sxs-lookup"><span data-stu-id="b6ea8-104">This topic provides information about the **Invoice approvals** mobile workspace.</span></span> <span data-ttu-id="b6ea8-105">Tento pracovní prostor obsahuje seznam faktur, které vám byly přiřazeny v procesu workflowu záhlaví faktury dodavatele.</span><span class="sxs-lookup"><span data-stu-id="b6ea8-105">This workspace provides a list of invoices that have been assigned to you through the vendor invoice header workflow process.</span></span> 

<span data-ttu-id="b6ea8-106">Tento mobilní pracovní prostor je určen k použití s mobilní aplikací Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b6ea8-106">This mobile workspace is intended to be used with the Finance and Operations mobile app.</span></span>

## <a name="overview"></a><span data-ttu-id="b6ea8-107">Přehled</span><span class="sxs-lookup"><span data-stu-id="b6ea8-107">Overview</span></span>

<span data-ttu-id="b6ea8-108">V mobilním pracovním prostoru **Schválení faktur** si úředníci a manažeři v oblasti závazků mohou prohlížet faktury, které jim byly přiřazeny v rámci procesu workflowu záhlaví faktury dodavatele.</span><span class="sxs-lookup"><span data-stu-id="b6ea8-108">The **Invoice approvals** mobile workspace lets Accounts payable clerks and managers view invoices that have been assigned to them as part of the vendor invoice header workflow process.</span></span> <span data-ttu-id="b6ea8-109">Můžete si prohlížet informace o faktuře i podrobnosti o řádcích a distribuci, abyste se s jejich pomocí mohli lépe rozhodovat při schvalování.</span><span class="sxs-lookup"><span data-stu-id="b6ea8-109">You can view the invoice information, and even the line and distribution details, to help you make informed approval decisions.</span></span> <span data-ttu-id="b6ea8-110">V pracovním prostoru můžete provádět příslušná opatření a posouvat faktury dále v procesu workflowu.</span><span class="sxs-lookup"><span data-stu-id="b6ea8-110">From the workspace, you can take action to move the invoice through the workflow process.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="b6ea8-111">Požadavky</span><span class="sxs-lookup"><span data-stu-id="b6ea8-111">Prerequisites</span></span>

<span data-ttu-id="b6ea8-112">Před použitím tohoto mobilního pracovního prostoru musí být splněny následující předpoklady.</span><span class="sxs-lookup"><span data-stu-id="b6ea8-112">Before you can use this mobile workspace, the following prerequisites must be met.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="b6ea8-113">Předpoklad</span><span class="sxs-lookup"><span data-stu-id="b6ea8-113">Prerequisite</span></span></th>
<th><span data-ttu-id="b6ea8-114">Role</span><span class="sxs-lookup"><span data-stu-id="b6ea8-114">Role</span></span></th>
<th><span data-ttu-id="b6ea8-115">Popis</span><span class="sxs-lookup"><span data-stu-id="b6ea8-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b6ea8-116">Microsoft Dynamics 365 Finance musí být nasazen ve vaší organizaci.</span><span class="sxs-lookup"><span data-stu-id="b6ea8-116">Microsoft Dynamics 365 Finance must be deployed in your organization.</span></span></td>
<td><span data-ttu-id="b6ea8-117">Správce systému</span><span class="sxs-lookup"><span data-stu-id="b6ea8-117">System administrator</span></span></td>
<td><span data-ttu-id="b6ea8-118">Viz část <a href="../deployment/deploy-demo-environment.md">Nasazení ukázkového prostředí</a>.</span><span class="sxs-lookup"><span data-stu-id="b6ea8-118">See <a href="../deployment/deploy-demo-environment.md">Deploy a demo environment</a>.</span></span>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="b6ea8-119">Mobilní pracovní prostor <strong>Schválení faktur</strong> musí být publikován.</span><span class="sxs-lookup"><span data-stu-id="b6ea8-119">The <strong>Invoice approvals</strong> mobile workspace must be published.</span></span></td>
<td><span data-ttu-id="b6ea8-120">Správce systému</span><span class="sxs-lookup"><span data-stu-id="b6ea8-120">System administrator</span></span></td>
<td><span data-ttu-id="b6ea8-121">Viz téma <a href="publish-mobile-workspace.md">Publikování mobilního pracovního prostoru</a>.</span><span class="sxs-lookup"><span data-stu-id="b6ea8-121">See <a href="publish-mobile-workspace.md">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="b6ea8-122">Stáhněte a nainstalujte mobilní aplikaci</span><span class="sxs-lookup"><span data-stu-id="b6ea8-122">Download and install the mobile app</span></span>

<span data-ttu-id="b6ea8-123">Stáhněte a nainstalujte mobilní aplikaci Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="b6ea8-123">Download and install the Finance and Operations mobile app:</span></span>

-   [<span data-ttu-id="b6ea8-124">Pro telefony Android</span><span class="sxs-lookup"><span data-stu-id="b6ea8-124">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
-   [<span data-ttu-id="b6ea8-125">Pro telefony iPhone</span><span class="sxs-lookup"><span data-stu-id="b6ea8-125">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="b6ea8-126">Přihlaste se do mobilní aplikace</span><span class="sxs-lookup"><span data-stu-id="b6ea8-126">Sign in to the mobile app</span></span>

1.  <span data-ttu-id="b6ea8-127">Spusťte aplikaci na svém mobilním zařízení.</span><span class="sxs-lookup"><span data-stu-id="b6ea8-127">Start the app on your mobile device.</span></span>
2.  <span data-ttu-id="b6ea8-128">Zadejte URL adresu Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="b6ea8-128">Enter your Microsoft Dynamics 365 URL.</span></span>
3.  <span data-ttu-id="b6ea8-129">Při prvním přihlášení se zobrazí výzva k zadání uživatelského jména a hesla.</span><span class="sxs-lookup"><span data-stu-id="b6ea8-129">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="b6ea8-130">Zadejte své přihlašovací údaje.</span><span class="sxs-lookup"><span data-stu-id="b6ea8-130">Enter your credentials.</span></span>
4.  <span data-ttu-id="b6ea8-131">Po přihlášení se zobrazí dostupné pracovní prostory pro vaši společnost.</span><span class="sxs-lookup"><span data-stu-id="b6ea8-131">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="b6ea8-132">Všimněte si, že pokud správce systému později publikuje nový pracovní prostor, budete muset aktualizovat seznam mobilních pracovních prostorů.</span><span class="sxs-lookup"><span data-stu-id="b6ea8-132">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

    <span data-ttu-id="b6ea8-133">[![Vyžádání aktualizace](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="b6ea8-133">[![Pull to refresh](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span></span>

## <a name="approve-invoices-by-using-the-invoice-approvals-mobile-workspace"></a><span data-ttu-id="b6ea8-134">Schválení faktur pomocí mobilního pracovního prostoru Schválení faktur</span><span class="sxs-lookup"><span data-stu-id="b6ea8-134">Approve invoices by using the Invoice approvals mobile workspace</span></span>
1.  <span data-ttu-id="b6ea8-135">Ve svém mobilním zařízení vyberte pracovní prostor **Schválení faktur**.</span><span class="sxs-lookup"><span data-stu-id="b6ea8-135">On your mobile device, select the **Invoice approvals** workspace.</span></span>
2.  <span data-ttu-id="b6ea8-136">Vyberte fakturu, která vám byla přiřazena procesem workflowu záhlaví faktury dodavatele.</span><span class="sxs-lookup"><span data-stu-id="b6ea8-136">Select the invoice that has been assigned to you by the vendor invoice header workflow process.</span></span>
3.  <span data-ttu-id="b6ea8-137">Na stránce **Podrobnosti faktury** zkontrolujte informace záhlaví faktury, například informace o dodavateli a datu.</span><span class="sxs-lookup"><span data-stu-id="b6ea8-137">On the **Invoice details** page, review the invoice header information, such as the vendor and date information.</span></span>
4.  <span data-ttu-id="b6ea8-138">Výběrem řádku faktury zobrazíte podrobnější informace v zobrazení **Podrobnosti řádku faktury**.</span><span class="sxs-lookup"><span data-stu-id="b6ea8-138">Select a line on the invoice to view more detailed information about it in the **Invoice line details** view.</span></span>
5.  <span data-ttu-id="b6ea8-139">V zobrazení **Podrobnosti řádku faktury** můžete výběrem možnosti **Distribuce** zobrazit distribuce řádků.</span><span class="sxs-lookup"><span data-stu-id="b6ea8-139">In the **Invoice line details** view, select **Distributions** to show the line distributions.</span></span> <span data-ttu-id="b6ea8-140">Zde si můžete prohlédnout účetnictví spojené s řádkem faktury.</span><span class="sxs-lookup"><span data-stu-id="b6ea8-140">Here, you can view the accounting for the invoice line.</span></span> <span data-ttu-id="b6ea8-141">K zobrazeným informacím patří finanční dimenze a hlavní účet.</span><span class="sxs-lookup"><span data-stu-id="b6ea8-141">The information that is shown includes the financial dimensions and the main account.</span></span>
6.  <span data-ttu-id="b6ea8-142">Na stránce **Podrobnosti faktury** můžete výběrem možnosti **Distribuce** zobrazit všechny distribuce.</span><span class="sxs-lookup"><span data-stu-id="b6ea8-142">On the **Invoice details** page, select **Distributions** to show all distributions.</span></span> <span data-ttu-id="b6ea8-143">Zde si můžete prohlédnout účetnictví spojené s celou fakturou.</span><span class="sxs-lookup"><span data-stu-id="b6ea8-143">Here, you can view the accounting for the whole invoice.</span></span> <span data-ttu-id="b6ea8-144">K zobrazeným informacím patří finanční dimenze a hlavní účty.</span><span class="sxs-lookup"><span data-stu-id="b6ea8-144">The information that is shown includes the financial dimensions and the main accounts.</span></span> 
7.  <span data-ttu-id="b6ea8-145">Výběrem možnosti **Přílohy** zobrazíte další poznámky nebo soubory, které jsou připojeny k faktuře.</span><span class="sxs-lookup"><span data-stu-id="b6ea8-145">Select **Attachments** to view any notes or files that are attached to the invoice.</span></span>
8.  <span data-ttu-id="b6ea8-146">Na stránce **Podrobnosti faktury** vyberte požadovanou akci workflowu a dokončete tak proces kontroly.</span><span class="sxs-lookup"><span data-stu-id="b6ea8-146">On the **Invoice details** page, select the appropriate workflow action to complete your review process.</span></span>
9.  <span data-ttu-id="b6ea8-147">Vyberte **Hotovo**.</span><span class="sxs-lookup"><span data-stu-id="b6ea8-147">Select **Done**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]