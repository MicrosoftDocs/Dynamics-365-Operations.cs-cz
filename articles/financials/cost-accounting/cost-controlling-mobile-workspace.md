---
title: "Mobilní pracovní prostor Řízení nákladů"
description: "Toto téma obsahuje informace o mobilním pracovním prostoru řízení nákladů. Tento pracovní prostor umožňuje manažerům nákladového střediska zobrazit informace o výkonu nákladového střediska kdykoli a odkudkoli."
author: AndersGirke
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 267114
ms.assetid: 612f2988-b2b9-420d-9825-40b99dc0e204
ms.search.region: global
ms.author: aevengir
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 8724f33176b4ff7730cd9d15e825bab794a10ac6
ms.contentlocale: cs-cz
ms.lasthandoff: 04/13/2018

---

# <a name="cost-controlling-mobile-workspace"></a><span data-ttu-id="f8e2d-104">Mobilní pracovní prostor Řízení nákladů</span><span class="sxs-lookup"><span data-stu-id="f8e2d-104">Cost controlling mobile workspace</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="f8e2d-105">Toto téma obsahuje informace o mobilním pracovním prostoru **Řízení nákladů**.</span><span class="sxs-lookup"><span data-stu-id="f8e2d-105">This topic provides information about the **Cost controlling** mobile workspace.</span></span> <span data-ttu-id="f8e2d-106">Tento pracovní prostor umožňuje manažerům nákladového střediska zobrazit informace o výkonu nákladového střediska kdykoli a odkudkoli.</span><span class="sxs-lookup"><span data-stu-id="f8e2d-106">This workspace lets cost center managers view information about cost center performance anytime and anywhere.</span></span>

<span data-ttu-id="f8e2d-107">Tento mobilní pracovní prostor je určen k použití s mobilní aplikací Microsoft Dynamics 365 for Unified Operations.</span><span class="sxs-lookup"><span data-stu-id="f8e2d-107">This mobile workspace is intended to be used with the Microsoft Dynamics 365 for Unified Operations mobile app.</span></span>

## <a name="overview"></a><span data-ttu-id="f8e2d-108">Přehled</span><span class="sxs-lookup"><span data-stu-id="f8e2d-108">Overview</span></span>
<span data-ttu-id="f8e2d-109">Mobilní pracovní prostor **Řízení nákladů** poskytuje okamžitý přehled o aktuálním výkonu nákladových středisek porovnáním skutečných nákladů s rozpočtovými náklady.</span><span class="sxs-lookup"><span data-stu-id="f8e2d-109">The **Cost controlling** mobile workspace provides an instant view of the current performance of cost centers by comparing actual costs against the budgeted costs.</span></span> <span data-ttu-id="f8e2d-110">Můžete přejít na podrobnosti stavů jednotlivých prvků nákladů.</span><span class="sxs-lookup"><span data-stu-id="f8e2d-110">You can drill down to the status of individual cost elements.</span></span>

<span data-ttu-id="f8e2d-111">Zaměstnanec například obdrží pozvánku na mezinárodní konferenci, ale organizace musí pokrývat všechny cestovní výdaje.</span><span class="sxs-lookup"><span data-stu-id="f8e2d-111">For example, an employee receives an invitation to an international conference, but the organization must cover all the travel expenses.</span></span> <span data-ttu-id="f8e2d-112">Zaměstnanec se zeptá svého manažera, zda se může konference zúčastnit.</span><span class="sxs-lookup"><span data-stu-id="f8e2d-112">The employee asks his manager whether he can attend the conference.</span></span> <span data-ttu-id="f8e2d-113">Manažer rychle otevře mobilní pracovní prostor **řízení nákladů** na svém mobilním telefonu a zjistí, zda má rozpočet pro zaměstnance k účasti na konferenci.</span><span class="sxs-lookup"><span data-stu-id="f8e2d-113">The manager opens the **Cost controlling** mobile workspace on her mobile device to see whether she has budget for the employee to attend the conference.</span></span>

### <a name="data-security"></a><span data-ttu-id="f8e2d-114">Zabezpečení dat</span><span class="sxs-lookup"><span data-stu-id="f8e2d-114">Data security</span></span>
<span data-ttu-id="f8e2d-115">Data v mobilním pracovním prostoru **řízení nákladů** jsou zabezpečena pomocí pověření uživatele.</span><span class="sxs-lookup"><span data-stu-id="f8e2d-115">The data in the **Cost controlling** mobile workspace is secured through user credentials.</span></span> <span data-ttu-id="f8e2d-116">Manažeři nákladového střediska mohou vidět data pouze pro své nákladové středisko.</span><span class="sxs-lookup"><span data-stu-id="f8e2d-116">Cost center managers are allowed to see data only for their own cost center.</span></span> <span data-ttu-id="f8e2d-117">Úroveň zabezpečení přístupu je spravována v rámci modulu **Nákladové účetnictví**.</span><span class="sxs-lookup"><span data-stu-id="f8e2d-117">The access-level security is managed in the **Cost accounting** module.</span></span>

<span data-ttu-id="f8e2d-118">Účetní definují konfiguraci mobilního pracovního prostoru **řízení nákladů** v modulu **Nákladové účetnictví**.</span><span class="sxs-lookup"><span data-stu-id="f8e2d-118">Cost accountants define the configuration of the **Cost controlling** mobile workspace in the **Cost accounting** module.</span></span> <span data-ttu-id="f8e2d-119">Po publikování pracovního prostoru do mobilní aplikace bude v aplikaci pracovní prostor k dispozici.</span><span class="sxs-lookup"><span data-stu-id="f8e2d-119">After the workspace is published to the mobile app, it's available in the app.</span></span> <span data-ttu-id="f8e2d-120">Všichni manažeři nákladových středisek v organizaci tak mohou prohlížet data ve stejném formátu.</span><span class="sxs-lookup"><span data-stu-id="f8e2d-120">Therefore, all cost center managers in the organization can view data in the same format.</span></span>

### <a name="actions-views-and-links"></a><span data-ttu-id="f8e2d-121">Akce, zobrazení a odkazy</span><span class="sxs-lookup"><span data-stu-id="f8e2d-121">Actions, views, and links</span></span>
<span data-ttu-id="f8e2d-122">Mobilní pracovní prostor **Řízení nákladů** poskytuje následující akce, zobrazení a odkazy:</span><span class="sxs-lookup"><span data-stu-id="f8e2d-122">The **Cost controlling** mobile workspace provides the following actions, views, and links:</span></span>

-   <span data-ttu-id="f8e2d-123">**Akce:**</span><span class="sxs-lookup"><span data-stu-id="f8e2d-123">**Actions:**</span></span>

    -   <span data-ttu-id="f8e2d-124">Pomocí možnosti **Vybrat konfiguraci** vyberte rozložení.</span><span class="sxs-lookup"><span data-stu-id="f8e2d-124">Use **Select configuration** to select a layout.</span></span>
    -   <span data-ttu-id="f8e2d-125">Pomocí možnosti **Vybrat nákladový objekt** vyberte nákladová střediska, podle kterých budete filtrovat data.</span><span class="sxs-lookup"><span data-stu-id="f8e2d-125">Use **Select cost object** to select the cost centers to filter data on.</span></span>
    
        > [!NOTE]
        > <span data-ttu-id="f8e2d-126">Nákladová střediska, která jsou zobrazená v seznamu závisí na přístupu, který je udělený v modulu **Nákladové účetnictví**.</span><span class="sxs-lookup"><span data-stu-id="f8e2d-126">The cost centers that appear in the list depend on the access that is granted in the **Cost accounting** module.</span></span>

-   <span data-ttu-id="f8e2d-127">**Zobrazení:** Podle toho, jaké akce jsou vybrané a jaká je konfigurace v modulu **Nákladové účetnictví**, můžete zobrazit následující informace na kartách:</span><span class="sxs-lookup"><span data-stu-id="f8e2d-127">**Views:** Based on the actions that are selected and the configuration in the **Cost accounting** module, you can view the following information on the cards:</span></span>

    -   <span data-ttu-id="f8e2d-128">Skutečnost a rozpočet (aktuální období)</span><span class="sxs-lookup"><span data-stu-id="f8e2d-128">Actual vs budget (current period)</span></span>
    -   <span data-ttu-id="f8e2d-129">Skutečnost a revidovaný rozpočet (aktuální období)</span><span class="sxs-lookup"><span data-stu-id="f8e2d-129">Actual vs revised budget (current period)</span></span>
    -   <span data-ttu-id="f8e2d-130">Skutečnost vs. rozpočet (předchozí období)</span><span class="sxs-lookup"><span data-stu-id="f8e2d-130">Actual vs budget (previous period)</span></span>
    -   <span data-ttu-id="f8e2d-131">Skutečnost vs. revidovaný rozpočet (předchozí období)</span><span class="sxs-lookup"><span data-stu-id="f8e2d-131">Actual vs revised budget (previous period)</span></span>
    -   <span data-ttu-id="f8e2d-132">Skutečnost vs. rozpočet (od začátku roku)</span><span class="sxs-lookup"><span data-stu-id="f8e2d-132">Actual vs budget (year to date)</span></span>
    -   <span data-ttu-id="f8e2d-133">Skutečnost vs. revidovaný rozpočet (od začátku roku)</span><span class="sxs-lookup"><span data-stu-id="f8e2d-133">Actual vs revised budget (year to date)</span></span>

    <span data-ttu-id="f8e2d-134">Na každé kartě jsou zobrazeny následující hodnoty: Skutečné, Rozpočet, Odchylka a Odchylka v %.</span><span class="sxs-lookup"><span data-stu-id="f8e2d-134">The following amounts are shown on every card: Actual, Budget, Variance, and Variance %.</span></span>

-   <span data-ttu-id="f8e2d-135">**Odkazy:**</span><span class="sxs-lookup"><span data-stu-id="f8e2d-135">**Links:**</span></span>

    -   <span data-ttu-id="f8e2d-136">Podrobnosti za aktuální období</span><span class="sxs-lookup"><span data-stu-id="f8e2d-136">Details for current period</span></span>
    -   <span data-ttu-id="f8e2d-137">Podrobnosti za předchozí období</span><span class="sxs-lookup"><span data-stu-id="f8e2d-137">Details for previous period</span></span>
    -   <span data-ttu-id="f8e2d-138">Podrobnosti za období od začátku roku</span><span class="sxs-lookup"><span data-stu-id="f8e2d-138">Details for year to date</span></span>

    <span data-ttu-id="f8e2d-139">Při výběru odkazu se zobrazí karta pro každý nákladový prvek.</span><span class="sxs-lookup"><span data-stu-id="f8e2d-139">When you select a link, a card is shown for each cost element.</span></span> <span data-ttu-id="f8e2d-140">Na každé kartě jsou uvedeny následující částky: skutečnost, rozpočet, odchylka rozpočtu, % odchylky rozpočtu, revidovaný rozpočet, odchylka revidovaného rozpočtu a % odchylky revidovaného rozpočtu.</span><span class="sxs-lookup"><span data-stu-id="f8e2d-140">The following amounts are shown on every card: Actual, Budget, Budget variance, Budget variance %, Revised budget, Revised budget variance, and Revised budget variance %.</span></span>
    
    <span data-ttu-id="f8e2d-141">[![Karta pro prvek nákladů ](./media/Cost-controlling.png)](./media/Cost-controlling.png)</span><span class="sxs-lookup"><span data-stu-id="f8e2d-141">[![Card for a cost element](./media/Cost-controlling.png)](./media/Cost-controlling.png)</span></span>

## <a name="prerequisites"></a><span data-ttu-id="f8e2d-142">Požadavky</span><span class="sxs-lookup"><span data-stu-id="f8e2d-142">Prerequisites</span></span>
<span data-ttu-id="f8e2d-143">Předpoklady se liší podle verze aplikace Microsoft Dynamics 365, která byla nasazena ve vaší organizaci.</span><span class="sxs-lookup"><span data-stu-id="f8e2d-143">The prerequisites differ, based on the version of Microsoft Dynamics 365 that has been deployed for your organization.</span></span>

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-finance-and-operations"></a><span data-ttu-id="f8e2d-144">Požadavky, pokud používáte aplikaci Microsoft Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="f8e2d-144">Prerequisites if you use Microsoft Dynamics 365 for Finance and Operations</span></span>
<span data-ttu-id="f8e2d-145">Pokud je ve vaší organizaci nasazena aplikace Microsoft Dynamics 365 for Finance and Operations, správce systému musí publikovat mobilní pracovní prostor **Řízení nákladů**.</span><span class="sxs-lookup"><span data-stu-id="f8e2d-145">If Microsoft Dynamics 365 for Finance and Operations has been deployed for your organization, the system administrator must publish the **Cost controlling** mobile workspace.</span></span> <span data-ttu-id="f8e2d-146">Více pokynů naleznete v tématu [Publikování mobilního pracovního prostoru](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).</span><span class="sxs-lookup"><span data-stu-id="f8e2d-146">For instructions, see [Publish a mobile workspace](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).</span></span>

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-operations-version-1611-with-platform-update-3-or-later"></a><span data-ttu-id="f8e2d-147">Požadavky, pokud používáte aplikaci Microsoft Dynamics 365 for Operations verze 1611 s aktualizací platformy 3 nebo novější</span><span class="sxs-lookup"><span data-stu-id="f8e2d-147">Prerequisites if you use Microsoft Dynamics 365 for Operations version 1611 with platform update 3 or later</span></span>
<span data-ttu-id="f8e2d-148">Pokud je ve vaší organizaci nasazena aplikace Microsoft Dynamics 365 for Operations verze 1611 s aktualizací platformy 3 nebo novější, správce systému musí dokončit následující předpoklady.</span><span class="sxs-lookup"><span data-stu-id="f8e2d-148">If Microsoft Dynamics 365 for Operations version 1611 with platform update 3 or later has been deployed for your organization, the system administrator must complete the following prerequisites.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="f8e2d-149">Předpoklad</span><span class="sxs-lookup"><span data-stu-id="f8e2d-149">Prerequisite</span></span></th>
<th><span data-ttu-id="f8e2d-150">Role</span><span class="sxs-lookup"><span data-stu-id="f8e2d-150">Role</span></span></th>
<th><span data-ttu-id="f8e2d-151">popis</span><span class="sxs-lookup"><span data-stu-id="f8e2d-151">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f8e2d-152">Implementujte opravu KB 4013633.</span><span class="sxs-lookup"><span data-stu-id="f8e2d-152">Implement KB 4013633.</span></span></td>
<td><span data-ttu-id="f8e2d-153">Správce systému</span><span class="sxs-lookup"><span data-stu-id="f8e2d-153">System administrator</span></span></td>

<td><span data-ttu-id="f8e2d-154">KB 4013633 je X ++ aktualizace nebo oprava hotfix metadat obsahující mobilní pracovní prostor <strong>Řízení nákladů</strong>.</span><span class="sxs-lookup"><span data-stu-id="f8e2d-154">KB 4013633 is an X++ update or metadata hotfix that contains the <strong>Cost controlling</strong> mobile workspace.</span></span> <span data-ttu-id="f8e2d-155">Pro implementaci KB 4013633 musí správce systému provést tyto kroky:</span><span class="sxs-lookup"><span data-stu-id="f8e2d-155">To implement KB 4013633, your system administrator must follow these steps.</span></span>
<ol>
<li><span data-ttu-id="f8e2d-156"><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Stažení opravy hotfix metadat ze služby Microsoft Dynamics Lifecycle Services (LCS)</a>.</span><span class="sxs-lookup"><span data-stu-id="f8e2d-156"><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Download the metadata hotfix from Microsoft Dynamics Lifecycle Services (LCS)</a>.</span></span></li>
<li><span data-ttu-id="f8e2d-157"><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Nainstalujte opravu hotfix metadat</a>.</span><span class="sxs-lookup"><span data-stu-id="f8e2d-157"><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Install the metadata hotfix</a>.</span></span></li>
<li><span data-ttu-id="f8e2d-158"><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Vytvořte nasaditelný balíček</a>, který obsahuje model <strong>SCMMobile</strong>, a nahrajte ho do LCS.</span><span class="sxs-lookup"><span data-stu-id="f8e2d-158"><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Create a deployable package</a> that contains the <strong>SCMMobile</strong> model, and then upload the deployable package to LCS.</span></span></li>
<li><span data-ttu-id="f8e2d-159"><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Použití nasaditelného balíčku</a></span><span class="sxs-lookup"><span data-stu-id="f8e2d-159"><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Apply the deployable package</a>.</span></span></li>

</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f8e2d-160">Publikování mobilního pracovního prostoru <strong>Řízení nákladů</strong>.</span><span class="sxs-lookup"><span data-stu-id="f8e2d-160">Publish the <strong>Cost controlling</strong> mobile workspace.</span></span></td>
<td><span data-ttu-id="f8e2d-161">Správce systému</span><span class="sxs-lookup"><span data-stu-id="f8e2d-161">System administrator</span></span></td>
<td><span data-ttu-id="f8e2d-162">Viz téma <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Publikování mobilního pracovního prostoru</a>.</span><span class="sxs-lookup"><span data-stu-id="f8e2d-162">See <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>


## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="f8e2d-163">Stáhněte a nainstalujte mobilní aplikaci</span><span class="sxs-lookup"><span data-stu-id="f8e2d-163">Download and install the mobile app</span></span>
<span data-ttu-id="f8e2d-164">Stáhněte a nainstalujte mobilní aplikaci 365 Dynamics for Unified Operations:</span><span class="sxs-lookup"><span data-stu-id="f8e2d-164">Download and install the Dynamics 365 for Unified Operations mobile app:</span></span>

-   [<span data-ttu-id="f8e2d-165">Pro telefony Android</span><span class="sxs-lookup"><span data-stu-id="f8e2d-165">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
-   [<span data-ttu-id="f8e2d-166">Pro telefony iPhone</span><span class="sxs-lookup"><span data-stu-id="f8e2d-166">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="f8e2d-167">Přihlaste se do mobilní aplikace</span><span class="sxs-lookup"><span data-stu-id="f8e2d-167">Sign in to the mobile app</span></span>

1.  <span data-ttu-id="f8e2d-168">Spusťte aplikaci na svém mobilním zařízení.</span><span class="sxs-lookup"><span data-stu-id="f8e2d-168">Start the app on your mobile device.</span></span>
2.  <span data-ttu-id="f8e2d-169">Zadejte adresu URL aplikace Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="f8e2d-169">Enter your Dynamics 365 URL.</span></span>
3.  <span data-ttu-id="f8e2d-170">Při prvním přihlášení se zobrazí výzva k zadání uživatelského jména a hesla.</span><span class="sxs-lookup"><span data-stu-id="f8e2d-170">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="f8e2d-171">Zadejte své přihlašovací údaje.</span><span class="sxs-lookup"><span data-stu-id="f8e2d-171">Enter your credentials.</span></span>
4.  <span data-ttu-id="f8e2d-172">Po přihlášení se zobrazí dostupné pracovní prostory pro vaši společnost.</span><span class="sxs-lookup"><span data-stu-id="f8e2d-172">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="f8e2d-173">Všimněte si, že pokud správce systému později publikuje nový pracovní prostor, budete muset aktualizovat seznam mobilních pracovních prostorů.</span><span class="sxs-lookup"><span data-stu-id="f8e2d-173">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

<span data-ttu-id="f8e2d-174">[![Vyžádání aktualizace](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="f8e2d-174">[![Pull to refresh](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span></span>

## <a name="view-the-performance-of-your-cost-center-by-using-the-cost-controlling-mobile-workspace"></a><span data-ttu-id="f8e2d-175">Zobrazení výkonu nákladového střediska pomocí mobilního pracovního prostoru řízení nákladů</span><span class="sxs-lookup"><span data-stu-id="f8e2d-175">View the performance of your cost center by using the Cost controlling mobile workspace</span></span>

1.  <span data-ttu-id="f8e2d-176">Na svém mobilním zařízení vyberte pracovní prostor **Řízení nákladů**.</span><span class="sxs-lookup"><span data-stu-id="f8e2d-176">On your mobile device, select the **Cost controlling** workspace.</span></span>
2.  <span data-ttu-id="f8e2d-177">Vyberte **Řízení objektu nákladů**.</span><span class="sxs-lookup"><span data-stu-id="f8e2d-177">Select **Cost object controlling**.</span></span>
3.  <span data-ttu-id="f8e2d-178">Vyberte **Akce**.</span><span class="sxs-lookup"><span data-stu-id="f8e2d-178">Select **Actions**.</span></span>
4.  <span data-ttu-id="f8e2d-179">Vyberte **Vybrat konfiguraci** pro výběr rozvržení řízení nákladů.</span><span class="sxs-lookup"><span data-stu-id="f8e2d-179">Select **Select configuration** to select a cost controlling layout.</span></span>
5.  <span data-ttu-id="f8e2d-180">Vyberte **Hotovo**.</span><span class="sxs-lookup"><span data-stu-id="f8e2d-180">Select **Done**.</span></span>
6.  <span data-ttu-id="f8e2d-181">Vyberte **Akce**.</span><span class="sxs-lookup"><span data-stu-id="f8e2d-181">Select **Actions**.</span></span>
7.  <span data-ttu-id="f8e2d-182">Vyberte tlačítko **Zvolit objekt nákladů** a vyberte nákladová střediska, ke kterým vám byl udělen přístup.</span><span class="sxs-lookup"><span data-stu-id="f8e2d-182">Select **Select cost object** to select the cost centers that you've been granted access to.</span></span>
8.  <span data-ttu-id="f8e2d-183">Vyberte **Hotovo**.</span><span class="sxs-lookup"><span data-stu-id="f8e2d-183">Select **Done**.</span></span>
9.  <span data-ttu-id="f8e2d-184">Zobrazte celkovou výkonnost vašeho nákladového střediska.</span><span class="sxs-lookup"><span data-stu-id="f8e2d-184">View the overall performance of your cost center.</span></span>
10. <span data-ttu-id="f8e2d-185">Vyberte odkaz **Podrobnosti pro aktuální období**.</span><span class="sxs-lookup"><span data-stu-id="f8e2d-185">Select the **Details for current period** link.</span></span>
11. <span data-ttu-id="f8e2d-186">Zobrazte výkonnost jednotlivých prvků nákladů.</span><span class="sxs-lookup"><span data-stu-id="f8e2d-186">View the performance of individual cost elements.</span></span>
12. <span data-ttu-id="f8e2d-187">Můžete také vyhledat konkrétní prvky nákladů.</span><span class="sxs-lookup"><span data-stu-id="f8e2d-187">You can also search for specific cost elements.</span></span>


