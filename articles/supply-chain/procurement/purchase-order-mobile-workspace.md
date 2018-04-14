---
title: "Mobilní pracovní prostor schvalování nákupních objednávek"
description: "Toto téma obsahuje informace o mobilním pracovním prostoru Schválení nákupní objednávky, který umožňuje zobrazit nákupní objednávky a odpovědět na ně prostřednictvím akce. Nákupní objednávky můžete například schválit nebo odmítnout."
author: mkirknel
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchVendorPortalRequests
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations, Retail
ms.custom: 30211
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 96d92016a4634291c5d519a2935992b3a50b65dd
ms.contentlocale: cs-cz
ms.lasthandoff: 04/13/2018

---

# <a name="purchase-order-approval-mobile-workspace"></a><span data-ttu-id="452d2-104">Mobilní pracovní prostor schvalování nákupních objednávek</span><span class="sxs-lookup"><span data-stu-id="452d2-104">Purchase order approval mobile workspace</span></span>

[!INCLUDE [banner](../includes/banner.md)]

[!INCLUDE [retail name](../includes/retail-name.md)]

<span data-ttu-id="452d2-105">Toto téma obsahuje informace o mobilním pracovním prostoru **Schválení nákupní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="452d2-105">This topic provides information about the **Purchase order approval** mobile workspace.</span></span> <span data-ttu-id="452d2-106">Tento pracovní prostor vám umožní zobrazit nákupní objednávky a reagovat na ně pomocí akcí.</span><span class="sxs-lookup"><span data-stu-id="452d2-106">This workspace lets you view purchase orders and respond to them through actions.</span></span> <span data-ttu-id="452d2-107">Nákupní objednávky můžete například schválit nebo odmítnout.</span><span class="sxs-lookup"><span data-stu-id="452d2-107">For example, you can approve or reject a purchase order.</span></span>
 
## <a name="overview"></a><span data-ttu-id="452d2-108">Přehled</span><span class="sxs-lookup"><span data-stu-id="452d2-108">Overview</span></span> 
<span data-ttu-id="452d2-109">Nákupní objednávky, které vyžadují schválení, procházejí workflowem schválení.</span><span class="sxs-lookup"><span data-stu-id="452d2-109">Purchase orders that requires approval go through an approval workflow.</span></span> <span data-ttu-id="452d2-110">Workflow může obsahovat různé kroky, které vyžadují, aby jedna nebo více osob provedly akci.</span><span class="sxs-lookup"><span data-stu-id="452d2-110">The workflow can include various steps that require that one or more people take action.</span></span> <span data-ttu-id="452d2-111">Osoba může například muset dokončit úlohu nebo schválit nákupní objednávku.</span><span class="sxs-lookup"><span data-stu-id="452d2-111">For example, a person might have to complete a task or approve the purchase order.</span></span> 

<span data-ttu-id="452d2-112">Mobilní pracovní prostor **Schválení nákupní objednávky** umožňuje snadno zobrazit a odpovědět na nákupní objednávky z mobilního zařízení.</span><span class="sxs-lookup"><span data-stu-id="452d2-112">The **Purchase order approval** mobile workspace lets you easily view and respond to purchase orders from your mobile device.</span></span> <span data-ttu-id="452d2-113">Tento pracovní prostor také umožňuje přijmout stejné akce workflowu, které lze provést z webového klienta Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="452d2-113">This workspace also lets you take the same workflow actions that you can take from the Microsoft Dynamics 365 for Finance and Operations, web client.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="452d2-114">Požadavky</span><span class="sxs-lookup"><span data-stu-id="452d2-114">Prerequisites</span></span>
<span data-ttu-id="452d2-115">Předpoklady se liší podle verze aplikace Finance and Operations, která byla nasazena ve vaší organizaci.</span><span class="sxs-lookup"><span data-stu-id="452d2-115">The prerequisites vary, depending on the version of Finance and Operations that has been deployed for your organization.</span></span>

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-finance-and-operations"></a><span data-ttu-id="452d2-116">Požadavky, pokud používáte aplikaci Microsoft Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="452d2-116">Prerequisites if you use Microsoft Dynamics 365 for Finance and Operations</span></span> 
<span data-ttu-id="452d2-117">Pokud je ve vaší organizaci nasazena aktualizace aplikace Microsoft Dynamics 365 for Finance and Operations, správce systému musí mobilní pracovní prostor **Schválení nákupní objednávky** publikovat.</span><span class="sxs-lookup"><span data-stu-id="452d2-117">If Microsoft Dynamics 365 for Finance and Operations has been deployed for your organization, the system administrator must publish the **Purchase order approval** mobile workspace.</span></span> <span data-ttu-id="452d2-118">Více pokynů naleznete v tématu [Publikování mobilního pracovního prostoru](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).</span><span class="sxs-lookup"><span data-stu-id="452d2-118">For instructions, see [Publish a mobile workspace](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).</span></span>

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-operations-version-1611-with-platform-update-3-or-later"></a><span data-ttu-id="452d2-119">Požadavky, pokud používáte aplikaci Microsoft Dynamics 365 for Operations verze 1611 s aktualizací Platform 3 nebo novější</span><span class="sxs-lookup"><span data-stu-id="452d2-119">Prerequisites if you use Microsoft Dynamics 365 for Operations version 1611 with Platform update 3 or later</span></span>
<span data-ttu-id="452d2-120">Pokud je ve vaší organizaci nasazena aplikace Microsoft Dynamics 365 for Operations verze 1611 s aktualizací Platform 3 nebo novější, správce systému musí dokončit následující předpoklady.</span><span class="sxs-lookup"><span data-stu-id="452d2-120">If Microsoft Dynamics 365 for Operations version 1611 with Platform update 3 or later has been deployed for your organization, the system administrator must complete the following prerequisites.</span></span> 

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="452d2-121">Předpoklad</span><span class="sxs-lookup"><span data-stu-id="452d2-121">Prerequisite</span></span></th>
<th><span data-ttu-id="452d2-122">Role</span><span class="sxs-lookup"><span data-stu-id="452d2-122">Role</span></span></th>
<th><span data-ttu-id="452d2-123">popis</span><span class="sxs-lookup"><span data-stu-id="452d2-123">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="452d2-124">Implementujte opravu KB 4017918.</span><span class="sxs-lookup"><span data-stu-id="452d2-124">Implement KB 4017918.</span></span></td>
<td><span data-ttu-id="452d2-125">Správce systému</span><span class="sxs-lookup"><span data-stu-id="452d2-125">System administrator</span></span></td>
<td><span data-ttu-id="452d2-126">KB 4017918 je X ++ aktualizace nebo oprava hotfix metadat obsahující mobilní pracovní prostor <strong>Schválení nákupní objednávky</strong>.</span><span class="sxs-lookup"><span data-stu-id="452d2-126">KB 4017918 is an X++ update or metadata hotfix that contains the <strong>Purchase order approval</strong> mobile workspace.</span></span> <span data-ttu-id="452d2-127">Pro implementaci KB 4017918 musí správce systému provést tyto kroky:</span><span class="sxs-lookup"><span data-stu-id="452d2-127">To implement KB 4017918, your system administrator must follow these steps.</span></span>
<ol>
<li><span data-ttu-id="452d2-128"><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Stažení opravy hotfix metadat ze služby Microsoft Dynamics Lifecycle Services (LCS)</a>.</span><span class="sxs-lookup"><span data-stu-id="452d2-128"><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Download the metadata hotfix from Microsoft Dynamics Lifecycle Services (LCS)</a>.</span></span></li>
<li><span data-ttu-id="452d2-129"><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Nainstalujte opravu hotfix metadat</a>.</span><span class="sxs-lookup"><span data-stu-id="452d2-129"><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Install the metadata hotfix</a>.</span></span></li>
<li><span data-ttu-id="452d2-130"><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Vytvořte nasaditelný balíček</a>, který obsahuje model <strong>SCMMobile</strong>, a nahrajte ho do LCS.</span><span class="sxs-lookup"><span data-stu-id="452d2-130"><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Create a deployable package</a> that contains the <strong>SCMMobile</strong> model, and then upload the deployable package to LCS.</span></span></li>
<li><span data-ttu-id="452d2-131"><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Použití nasaditelného balíčku</a></span><span class="sxs-lookup"><span data-stu-id="452d2-131"><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Apply the deployable package</a>.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="452d2-132">Publikujte mobilní pracovní prostor <strong>Schválení nákupní objednávky</strong>.</span><span class="sxs-lookup"><span data-stu-id="452d2-132">Publish the <strong>Purchase order approval</strong> mobile workspace.</span></span></td>
<td><span data-ttu-id="452d2-133">Správce systému</span><span class="sxs-lookup"><span data-stu-id="452d2-133">System administrator</span></span></td>
<td><span data-ttu-id="452d2-134">Viz téma <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Publikování mobilního pracovního prostoru</a>.</span><span class="sxs-lookup"><span data-stu-id="452d2-134">See <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="452d2-135">Stáhněte a nainstalujte mobilní aplikaci</span><span class="sxs-lookup"><span data-stu-id="452d2-135">Download and install the mobile app</span></span>
<span data-ttu-id="452d2-136">Stáhněte a nainstalujte mobilní aplikaci 365 Microsoft Dynamics for Unified Operations:</span><span class="sxs-lookup"><span data-stu-id="452d2-136">Download and install the Microsoft Dynamics 365 for Unified Operations mobile app:</span></span>

- [<span data-ttu-id="452d2-137">Pro telefony Android</span><span class="sxs-lookup"><span data-stu-id="452d2-137">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
- [<span data-ttu-id="452d2-138">Pro telefony iPhone</span><span class="sxs-lookup"><span data-stu-id="452d2-138">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)


## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="452d2-139">Přihlaste se do mobilní aplikace</span><span class="sxs-lookup"><span data-stu-id="452d2-139">Sign in to the mobile app</span></span>

1. <span data-ttu-id="452d2-140">Spusťte aplikaci na svém mobilním zařízení.</span><span class="sxs-lookup"><span data-stu-id="452d2-140">Start the app on your mobile device.</span></span>
2. <span data-ttu-id="452d2-141">Zadejte adresu URL aplikace Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="452d2-141">Enter your Microsoft Dynamics 365 URL.</span></span>
3. <span data-ttu-id="452d2-142">Při prvním přihlášení se zobrazí výzva k zadání uživatelského jména a hesla.</span><span class="sxs-lookup"><span data-stu-id="452d2-142">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="452d2-143">Zadejte své přihlašovací údaje.</span><span class="sxs-lookup"><span data-stu-id="452d2-143">Enter your credentials.</span></span>
4. <span data-ttu-id="452d2-144">Po přihlášení se zobrazí dostupné pracovní prostory pro vaši společnost.</span><span class="sxs-lookup"><span data-stu-id="452d2-144">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="452d2-145">Všimněte si, že pokud správce systému později publikuje nový pracovní prostor, budete muset aktualizovat seznam mobilních pracovních prostorů.</span><span class="sxs-lookup"><span data-stu-id="452d2-145">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

![Pracovní prostor Schválení nákupní objednávky v seznamu dostupných pracovních prostorů](./media/po-workspaces.png)

## <a name="view-orders-that-are-assigned-to-you"></a><span data-ttu-id="452d2-147">Zobrazení objednávek, které jsou vám přiřazeny</span><span class="sxs-lookup"><span data-stu-id="452d2-147">View orders that are assigned to you</span></span>
1. <span data-ttu-id="452d2-148">Ve svém mobilním zařízení vyberte pracovní prostor **Schválení nákupní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="452d2-148">On your mobile device, select the **Purchase order approval** workspace.</span></span>
2. <span data-ttu-id="452d2-149">Vyberte **objednávky přiřazené mně** k zobrazení všech nákupních objednávek, u kterých jste byli vyzváni k provedení akce ve workflowu schválení nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="452d2-149">Select **Orders assigned to me** to view all the purchase orders for which you've been asked to take action in the purchase order approval workflow.</span></span>
3. <span data-ttu-id="452d2-150">Vyberte objednávku.</span><span class="sxs-lookup"><span data-stu-id="452d2-150">Select an order.</span></span> <span data-ttu-id="452d2-151">Na stránce **Podrobnosti objednávky** se zobrazí informace v záhlaví objednávky a řádky.</span><span class="sxs-lookup"><span data-stu-id="452d2-151">On the **Order details** page, you will see the order header information and lines.</span></span> <span data-ttu-id="452d2-152">Můžete také vyhledat pokyny z úlohy workflowu.</span><span class="sxs-lookup"><span data-stu-id="452d2-152">You can also find guidelines from the workflow task.</span></span>
4. <span data-ttu-id="452d2-153">Vyberte možnost **Rozúčtování** k otevření stránky **Rozúčtování v záhlaví**.</span><span class="sxs-lookup"><span data-stu-id="452d2-153">Select **Accounting distributions** to open the **Header accounting distributions** page.</span></span>
5. <span data-ttu-id="452d2-154">Vraťte se na stránku **Podrobnosti objednávky** a vyberte řádek.</span><span class="sxs-lookup"><span data-stu-id="452d2-154">Return to the **Order details** page, and select a line.</span></span> <span data-ttu-id="452d2-155">Z podrobností o řádku objednávky můžete také zkoumat rozúčtování specifické pro řádek.</span><span class="sxs-lookup"><span data-stu-id="452d2-155">From the order line details, you can also explore the line-specific accounting distributions.</span></span>

## <a name="complete-an-action-on-the-purchase-order"></a><span data-ttu-id="452d2-156">Dokončení akce u nákupní objednávky</span><span class="sxs-lookup"><span data-stu-id="452d2-156">Complete an action on the purchase order</span></span>
<span data-ttu-id="452d2-157">Poté, co jste navštívili nákupní objednávku, která je vám přiřazena, a přečetli si pokyny workflowu, měli byste být připravení k provedení akce.</span><span class="sxs-lookup"><span data-stu-id="452d2-157">After you've viewed the purchase order that is assigned to you and read the workflow instructions, you should be ready to take action.</span></span>

1. <span data-ttu-id="452d2-158">Ve svém mobilním zařízení vyberte pracovní prostor **Schválení nákupní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="452d2-158">On your mobile device, select the **Purchase order approval** workspace.</span></span>
2. <span data-ttu-id="452d2-159">Vyberte **objednávky přiřazené mně** k zobrazení všech nákupních objednávek, u kterých jste byli vyzváni k provedení akce ve workflowu schválení nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="452d2-159">Select **Orders assigned to me** to view all the purchase orders for which you've been asked to take action in the purchase order approval workflow.</span></span>
3. <span data-ttu-id="452d2-160">Vyberte objednávku a zobrazte stránku podrobností.</span><span class="sxs-lookup"><span data-stu-id="452d2-160">Select an order, and view the details page.</span></span>
4. <span data-ttu-id="452d2-161">Vyberte **Akce** pro zobrazení dostupných akcí.</span><span class="sxs-lookup"><span data-stu-id="452d2-161">Select **Actions** to show the available actions.</span></span> <span data-ttu-id="452d2-162">Akce, které jsou k dispozici, závisí na úloze, která vám byla přiřazena.</span><span class="sxs-lookup"><span data-stu-id="452d2-162">The actions that are available depend on the task that has been assigned to you.</span></span>

    | <span data-ttu-id="452d2-163">Akce úlohy</span><span class="sxs-lookup"><span data-stu-id="452d2-163">Task action</span></span>    | <span data-ttu-id="452d2-164">Akce schválení</span><span class="sxs-lookup"><span data-stu-id="452d2-164">Approval action</span></span>  |
    |----------------|------------------|
    | <span data-ttu-id="452d2-165">Dokončit</span><span class="sxs-lookup"><span data-stu-id="452d2-165">Complete</span></span>       | <span data-ttu-id="452d2-166">Schválit</span><span class="sxs-lookup"><span data-stu-id="452d2-166">Approve</span></span>          |
    | <span data-ttu-id="452d2-167">Vrácení</span><span class="sxs-lookup"><span data-stu-id="452d2-167">Return</span></span>         | <span data-ttu-id="452d2-168">Zamítnout</span><span class="sxs-lookup"><span data-stu-id="452d2-168">Reject</span></span>           |
    | <span data-ttu-id="452d2-169">Požadavek na změnu</span><span class="sxs-lookup"><span data-stu-id="452d2-169">Request change</span></span> | <span data-ttu-id="452d2-170">Požadavek na změnu</span><span class="sxs-lookup"><span data-stu-id="452d2-170">Request change</span></span>   |
    | <span data-ttu-id="452d2-171">Zástupce</span><span class="sxs-lookup"><span data-stu-id="452d2-171">Delegate</span></span>       | <span data-ttu-id="452d2-172">Zástupce</span><span class="sxs-lookup"><span data-stu-id="452d2-172">Delegate</span></span>         |

5. <span data-ttu-id="452d2-173">Vyberte odpovídající akci.</span><span class="sxs-lookup"><span data-stu-id="452d2-173">Select the appropriate action.</span></span>
6. <span data-ttu-id="452d2-174">Na stránce **Dokončit úkol** zadejte komentář.</span><span class="sxs-lookup"><span data-stu-id="452d2-174">On the **Complete task** page, enter a comment.</span></span> <span data-ttu-id="452d2-175">Všimněte si, že pokud jste vybrali akci **Delegovat**, je nutné vybrat uživatele, kterému má být úkol delegován.</span><span class="sxs-lookup"><span data-stu-id="452d2-175">Note that if you select the **Delegate** action, you must select a user to delegate the task to.</span></span>
7. <span data-ttu-id="452d2-176">Vyberte **Hotovo**.</span><span class="sxs-lookup"><span data-stu-id="452d2-176">Select **Done**.</span></span> <span data-ttu-id="452d2-177">Po aktualizaci pracovního prostoru již nákupní objednávka nebude v tomto seznamu.</span><span class="sxs-lookup"><span data-stu-id="452d2-177">After you refresh your workspace, the purchase order will no longer be in your list.</span></span> 

