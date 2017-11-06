---
title: "Domovská stránka mobilní aplikace"
description: "Toto téma popisuje mobilní aplikaci Microsoft Dynamics 365 for Unified Operations a poskytuje odkazy na zdroje, které vám mohou pomoci ji implementovat ve vaší organizaci."
author: sericks007
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 272853
ms.assetid: c99f818f-27b3-4e45-92b4-74272dad0e17
ms.search.region: Global
ms.author: sericks
ms.dyn365.ops.intro: Platform update 4
ms.search.validFrom: 2017-02-28
ms.translationtype: HT
ms.sourcegitcommit: 9ee81bbdd22fed4ef6ea97080fe1f6b3d82bcaf5
ms.openlocfilehash: 88e4737bd8abf7f7dbab54fa6fb18afa525177e9
ms.contentlocale: cs-cz
ms.lasthandoff: 11/06/2017

---

# <a name="mobile-app-home-page"></a><span data-ttu-id="82841-103">Domovská stránka mobilní aplikace</span><span class="sxs-lookup"><span data-stu-id="82841-103">Mobile app home page</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="82841-104">Toto téma popisuje mobilní aplikaci Microsoft Dynamics 365 for Unified Operations a poskytuje odkazy na zdroje, které vám mohou pomoci ji implementovat ve vaší organizaci.</span><span class="sxs-lookup"><span data-stu-id="82841-104">This topic describes the Microsoft Dynamics 365 for Unified Operations mobile app and provides links to resources that can help you implement it in your organization.</span></span>

> [!NOTE]
> <span data-ttu-id="82841-105">Aplikace měla dříve název *Microsoft Dynamics 365 for Finance and Operations*.</span><span class="sxs-lookup"><span data-stu-id="82841-105">The mobile app was previously named *Microsoft Dynamics 365 for Finance and Operations*.</span></span>

<a name="overview"></a><span data-ttu-id="82841-106">Přehled</span><span class="sxs-lookup"><span data-stu-id="82841-106">Overview</span></span>
--------

<span data-ttu-id="82841-107">Mobilní aplikace umožňuje vaší organizaci zpřístupnit své obchodní procesy na mobilních zařízeních.</span><span class="sxs-lookup"><span data-stu-id="82841-107">The mobile app enables your organization to make its business processes available on mobile devices.</span></span> <span data-ttu-id="82841-108">Jakmile váš správce IT povolí mobilní pracovní prostory pro vaši organizaci, mohou se uživatelé přihlásit k aplikaci a okamžitě začít pracovat s obchodními procesy ze svých mobilních zařízení.</span><span class="sxs-lookup"><span data-stu-id="82841-108">After your IT admin enables the mobile workspaces for your organization, users can sign in to the app and immediately begin to run business processes from their mobile devices.</span></span> <span data-ttu-id="82841-109">Mobilní aplikace obsahuje následující funkce, které vám mohou pomoci zvýšit produktivitu:</span><span class="sxs-lookup"><span data-stu-id="82841-109">The mobile app includes the following features that can help increase productivity:</span></span>

- <span data-ttu-id="82841-110">Uživatelé mohou zobrazit, upravit a reagovat na obchodní data, i v případě, kdy mají občasné síťové připojení nebo kdy jsou jejich mobilní zařízení zcela offline.</span><span class="sxs-lookup"><span data-stu-id="82841-110">Users can view, edit, and act on business data, even if they have intermittent network connectivity or their mobile devices are completely offline.</span></span> <span data-ttu-id="82841-111">Poté, co zařízení obnoví připojení k síti, offline datové operace se automaticky synchronizují s aplikací Dynamics 365 for Finance and Operations, Enterprise edition nebo Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="82841-111">When a device reestablishes a network connection, offline data operations are automatically synchronized with Dynamics 365 for Finance and Operations, Enterprise edition, or Microsoft Dynamics 365 for Finance and Operations.</span></span>
- <span data-ttu-id="82841-112">IT správci nebo vývojáři mohou vytvořit a publikovat mobilní pracovní prostory, které byly vytvořeny na míru pro jejich organizace.</span><span class="sxs-lookup"><span data-stu-id="82841-112">IT admins or developers can build and publish mobile workspaces that have been tailored to their organization.</span></span> <span data-ttu-id="82841-113">Aplikace používá vaše existující kódy majetku.</span><span class="sxs-lookup"><span data-stu-id="82841-113">The app uses your existing code assets.</span></span> <span data-ttu-id="82841-114">Z toho vyplývá, že není nutné znovu zavádět vaše postupy ověření, obchodní logik nebo konfiguraci zabezpečení.</span><span class="sxs-lookup"><span data-stu-id="82841-114">Therefore, you don't have to re-implement your validation procedures, business logic, or security configuration.</span></span>
- <span data-ttu-id="82841-115">IT správci nebo vývojáři mohou snadno navrhnout mobilní pracovní prostory pomocí „ukaž a klikni“ návrháře pracovního prostoru, který je součástí webového klienta.</span><span class="sxs-lookup"><span data-stu-id="82841-115">IT admins or developers can easily design mobile workspaces by using the point-and-click workspace designer that is included with the web client.</span></span>
- <span data-ttu-id="82841-116">IT správci nebo vývojáři mohou volitelně optimalizovat offline možnosti pracovního prostoru pomocí architektury rozšíření obchodní logiky.</span><span class="sxs-lookup"><span data-stu-id="82841-116">IT admins or developers can optionally optimize the offline capabilities of workspaces by using the Business logic extensibility framework.</span></span> <span data-ttu-id="82841-117">Vzhledem k tomu, že data se stále zpracovávají, i když je zařízení v režimu offline, vaše mobilní scénáře zůstávají bohaté a plynulé i tehdy, když nemají stálé síťové připojení.</span><span class="sxs-lookup"><span data-stu-id="82841-117">Because data continues to be processed while a device is offline, your mobile scenarios remain rich and fluid, even if devices don't have constant network connectivity.</span></span>

## <a name="elements-of-the-mobile-app"></a><span data-ttu-id="82841-118">Prvky mobilní aplikace</span><span class="sxs-lookup"><span data-stu-id="82841-118">Elements of the mobile app</span></span>
<span data-ttu-id="82841-119">Navigace v mobilní aplikaci se skládá ze čtyř základních konceptů: řídicího panelu, pracovních prostorů, stránek a akcí.</span><span class="sxs-lookup"><span data-stu-id="82841-119">Navigation in the mobile app consists of four basic concepts: the dashboard, workspaces, pages, and actions.</span></span> 

<span data-ttu-id="82841-120">[![Navigační koncepty v mobilní aplikaci](./media/mobilephoneapp1-1024x536.png)](./media/mobilephoneapp1.png)</span><span class="sxs-lookup"><span data-stu-id="82841-120">[![Navigation concepts in the mobile app](./media/mobilephoneapp1-1024x536.png)](./media/mobilephoneapp1.png)</span></span>

1. <span data-ttu-id="82841-121">Při spuštění aplikace přejděte do **řídicího panelu**.</span><span class="sxs-lookup"><span data-stu-id="82841-121">When you start the app, you go to the **dashboard**.</span></span>
2. <span data-ttu-id="82841-122">Na řídicím panelu můžete zobrazit seznam **pracovních prostorů**, které jsou publikované.</span><span class="sxs-lookup"><span data-stu-id="82841-122">On the dashboard, you can see a list of **workspaces** that have been published.</span></span>
3. <span data-ttu-id="82841-123">V každé pracovním prostoru se zobrazí seznam **stránek** dostupných pro daný pracovní prostor.</span><span class="sxs-lookup"><span data-stu-id="82841-123">In each workspace, you can see a list of **pages** that are available for that workspace.</span></span>
4. <span data-ttu-id="82841-124">Jakmile se dostanete na stránku, můžete provést několik akcí.</span><span class="sxs-lookup"><span data-stu-id="82841-124">After you're on a page, you can perform several actions.</span></span> <span data-ttu-id="82841-125">Několik příkladů:</span><span class="sxs-lookup"><span data-stu-id="82841-125">Here are some examples:</span></span>

    - <span data-ttu-id="82841-126">Zobrazení podrobných dat</span><span class="sxs-lookup"><span data-stu-id="82841-126">View detailed data.</span></span>
    - <span data-ttu-id="82841-127">Přechod na jiné stránky pro související data, jako jsou například podrobnosti entity nebo řádky.</span><span class="sxs-lookup"><span data-stu-id="82841-127">Navigate to other pages for related data, such as entity details or lines.</span></span>
    - <span data-ttu-id="82841-128">Zobrazení seznamu **akcí**, které jsou k dispozici pro danou stránku.</span><span class="sxs-lookup"><span data-stu-id="82841-128">See a list of **actions** that are available for that page.</span></span> <span data-ttu-id="82841-129">Akce vám umožňují vytvořit nebo upravit stávající data.</span><span class="sxs-lookup"><span data-stu-id="82841-129">Actions let you create or edit existing data.</span></span>

## <a name="implementation-process"></a><span data-ttu-id="82841-130">Proces implementace</span><span class="sxs-lookup"><span data-stu-id="82841-130">Implementation process</span></span>
<span data-ttu-id="82841-131">Následující obrázek znázorňuje proces implementace mobilních pracovních prostorů, které poskytuje společnost Microsoft, a vlastních mobilních pracovních prostorů.</span><span class="sxs-lookup"><span data-stu-id="82841-131">The following illustration shows the process for implementing both mobile workspaces that are provided by Microsoft and custom mobile workspaces.</span></span> 

![Proces implementace mobilní aplikace](./media/Mobile-implementation-process-5.png)

<span data-ttu-id="82841-133">Následující tabulka obsahuje odkazy na zdroje, které vám mohou pomoci při implementaci mobilních pracovních prostorů poskytovaných společností Microsoft a vlastních mobilních pracovních prostorů</span><span class="sxs-lookup"><span data-stu-id="82841-133">The following table includes links to resources that can help you implement both mobile workspaces that are provided by Microsoft and custom mobile workspaces.</span></span> <span data-ttu-id="82841-134">Čísla v prvním sloupci odpovídají číslovaným krokům na předchozím obrázku.</span><span class="sxs-lookup"><span data-stu-id="82841-134">The numbers in the first column correspond to the numbered steps in the previous illustration.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="82841-135">Krok</span><span class="sxs-lookup"><span data-stu-id="82841-135">Step</span></span></th>
<th><span data-ttu-id="82841-136">Role</span><span class="sxs-lookup"><span data-stu-id="82841-136">Role</span></span></th>
<th><span data-ttu-id="82841-137">Akce</span><span class="sxs-lookup"><span data-stu-id="82841-137">Action</span></span></th>
<th><span data-ttu-id="82841-138">Prostředky umožňující dokončit akci</span><span class="sxs-lookup"><span data-stu-id="82841-138">Resources to help you complete the action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="82841-139">1</span><span class="sxs-lookup"><span data-stu-id="82841-139">1</span></span></td>
<td><span data-ttu-id="82841-140">Správce systému</span><span class="sxs-lookup"><span data-stu-id="82841-140">System administrator</span></span></td>
<td><span data-ttu-id="82841-141">Implementace aplikace Finance and Operations nebo Finance and Operations ve vaší organizaci.</span><span class="sxs-lookup"><span data-stu-id="82841-141">Implement Finance and Operations or Finance and Operations in your organization.</span></span></td>
<td><ul><li><span data-ttu-id="82841-142">Pokud jste dosud nenainstalovali verzi aplikace Microsoft Dynamics 365, podívejte se do části <a href="../deployment/deploy-demo-environment.md">Nasazení prostředí pro ukázku</a>.</span><span class="sxs-lookup"><span data-stu-id="82841-142">If you haven't yet deployed a version of Microsoft Dynamics 365, see <a href="../deployment/deploy-demo-environment.md">Deploy a demo environment</a>.</span></span></li><li><span data-ttu-id="82841-143">Pokud chcete zobrazit seznam mobilních pracovních prostorů, které lze použít, přejděte do tématu <a href="mobile-workspaces-released.md">Nedávno vydané mobilní pracovní prostory</a>.</span><span class="sxs-lookup"><span data-stu-id="82841-143">To see a list of mobile workspaces that can be used, see <a href="mobile-workspaces-released.md">Mobile workspaces recently released</a>.</span></span></li></ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="82841-144">2</span><span class="sxs-lookup"><span data-stu-id="82841-144">2</span></span></td>
<td><span data-ttu-id="82841-145">Správce systému</span><span class="sxs-lookup"><span data-stu-id="82841-145">System administrator</span></span></td>
<td><span data-ttu-id="82841-146"><strong>Pokud používáte aplikaci Microsoft Dynamics 365 for Finance and Operations verze 1611:</strong> Stáhněte si a nainstalujte články znalostní báze umožňující mobilní pracovní prostory, které poskytuje Microsoft.</span><span class="sxs-lookup"><span data-stu-id="82841-146"><strong>If you're using Microsoft Dynamics 365 for Finance and Operations version 1611:</strong> Download and install KBs that enable the mobile workspaces that are provided by Microsoft.</span></span></td>
<td><span data-ttu-id="82841-147">Další informace naleznete v následujících tématech:</span><span class="sxs-lookup"><span data-stu-id="82841-147">See the following topics for more information:</span></span>
<ul>

<li><span data-ttu-id="82841-148"><a href="../../financials/cost-accounting/cost-controlling-mobile-workspace.md">Mobilní pracovní prostory Řízení nákladů</a></span><span class="sxs-lookup"><span data-stu-id="82841-148"><a href="../../financials/cost-accounting/cost-controlling-mobile-workspace.md">Cost controlling mobile workspaces</a></span></span></li>
<li><span data-ttu-id="82841-149"><a href="../../supply-chain/inventory/inventory-on-hand-mobile-workspace.md">Mobilní pracovní prostor zásob na skladě</a></span><span class="sxs-lookup"><span data-stu-id="82841-149"><a href="../../supply-chain/inventory/inventory-on-hand-mobile-workspace.md">Inventory on-hand mobile workspace</a></span></span></li>
<li><span data-ttu-id="82841-150"><a href="../../supply-chain/sales-marketing/sales-orders-mobile-workspace.md">Mobilní pracovní prostory prodejních objednávek</a></span><span class="sxs-lookup"><span data-stu-id="82841-150"><a href="../../supply-chain/sales-marketing/sales-orders-mobile-workspace.md">Sales orders mobile workspaces</a></span></span></li>
<li><span data-ttu-id="82841-151"><a href="../../supply-chain/procurement/vendor-collaboration-mobile-workspace.md">Mobilní pracovní prostor dodavatelské spolupráce</a></span><span class="sxs-lookup"><span data-stu-id="82841-151"><a href="../../supply-chain/procurement/vendor-collaboration-mobile-workspace.md">Vendor collaboration mobile workspace</a></span></span></li>
<li><span data-ttu-id="82841-152"><a href="../../financials/project-management/project-time-entry-mobile-workspace.md">Mobilní pracovní prostor zadání času projektu</a></span><span class="sxs-lookup"><span data-stu-id="82841-152"><a href="../../financials/project-management/project-time-entry-mobile-workspace.md">Project time entry mobile workspace</a></span></span></li>
<li><span data-ttu-id="82841-153"><a href="../../financials/expense-management/expense-management-mobile-workspace.md">Pracovnímu prostor správy výdajů</a></span><span class="sxs-lookup"><span data-stu-id="82841-153"><a href="../../financials/expense-management/expense-management-mobile-workspace.md">Expense management mobile workspace</a></span></span></li>

</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="82841-154">3</span><span class="sxs-lookup"><span data-stu-id="82841-154">3</span></span></td>
<td><span data-ttu-id="82841-155">Správce systému</span><span class="sxs-lookup"><span data-stu-id="82841-155">System administrator</span></span></td>
<td><span data-ttu-id="82841-156">Publikujte mobilní pracovní prostory, které poskytuje společnost Microsoft.</span><span class="sxs-lookup"><span data-stu-id="82841-156">Publish the mobile workspaces that are provided by Microsoft.</span></span></td>
<td><span data-ttu-id="82841-157"><a href="publish-mobile-workspace.md">Publikování mobilního pracovního prostoru</a>
</span><span class="sxs-lookup"><span data-stu-id="82841-157"><a href="publish-mobile-workspace.md">Publish a mobile workspace</a>
</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="82841-158">4</span><span class="sxs-lookup"><span data-stu-id="82841-158">4</span></span></td>
<td><span data-ttu-id="82841-159">Vývojáři nebo nezávislí výrobci softwaru</span><span class="sxs-lookup"><span data-stu-id="82841-159">Developer or independent software vendor (ISV)</span></span></td>
<td><span data-ttu-id="82841-160">Použijte mobilní platformu k vytváření vlastních mobilních pracovních prostorů.</span><span class="sxs-lookup"><span data-stu-id="82841-160">Use the mobile platform to create custom mobile workspaces.</span></span></td>
<td><span data-ttu-id="82841-161"><a href="platform/mobile-platform-home-page.md">Mobilní platforma</a></span><span class="sxs-lookup"><span data-stu-id="82841-161"><a href="platform/mobile-platform-home-page.md">Mobile platform</a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="82841-162">5</span><span class="sxs-lookup"><span data-stu-id="82841-162">5</span></span></td>
<td><span data-ttu-id="82841-163">ISV</span><span class="sxs-lookup"><span data-stu-id="82841-163">ISV</span></span></td>
<td><span data-ttu-id="82841-164">Vytvořte nasaditelný balíček, který obsahuje vlastní mobilní pracovní prostory, a odešlete balíček do služby Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="82841-164">Create a deployable package that contains custom mobile workspaces, and upload the package to Microsoft Dynamics Lifecycle Services (LCS).</span></span></td>
<td><span data-ttu-id="82841-165"><a href="../deployment/create-apply-deployable-package.md">Vytvoření nasaditelného balíčku</a></span><span class="sxs-lookup"><span data-stu-id="82841-165"><a href="../deployment/create-apply-deployable-package.md">Create a deployable package</a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="82841-166">6</span><span class="sxs-lookup"><span data-stu-id="82841-166">6</span></span></td>
<td><span data-ttu-id="82841-167">Správce systému</span><span class="sxs-lookup"><span data-stu-id="82841-167">System administrator</span></span></td>
<td><span data-ttu-id="82841-168">Použijte nasaditelný balíček obsahující vlastní pracovní prostory, které poskytl nezávislý výrobce softwaru (ISV).</span><span class="sxs-lookup"><span data-stu-id="82841-168">Apply the deployable package that contains the custom workspaces that are provided by the independent software vendor (ISV).</span></span></td>
<td><span data-ttu-id="82841-169"><a href="../deployment/apply-deployable-package-system.md">Použití nasaditelného balíčku</a></span><span class="sxs-lookup"><span data-stu-id="82841-169"><a href="../deployment/apply-deployable-package-system.md">Apply a deployable package</a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="82841-170">7</span><span class="sxs-lookup"><span data-stu-id="82841-170">7</span></span></td>
<td><span data-ttu-id="82841-171">Správce systému</span><span class="sxs-lookup"><span data-stu-id="82841-171">System administrator</span></span></td>
<td><span data-ttu-id="82841-172">Publikujte vlastní mobilní pracovní prostory, které poskytuje nezávislý výrobce softwaru.</span><span class="sxs-lookup"><span data-stu-id="82841-172">Publish the custom mobile workspaces that are provided by the ISV.</span></span></td>
<td><span data-ttu-id="82841-173"><a href="publish-mobile-workspace.md">Publikování mobilního pracovního prostoru</a></span><span class="sxs-lookup"><span data-stu-id="82841-173"><a href="publish-mobile-workspace.md">Publish a mobile workspace</a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="82841-174">8</span><span class="sxs-lookup"><span data-stu-id="82841-174">8</span></span></td>
<td><span data-ttu-id="82841-175">Uživatel</span><span class="sxs-lookup"><span data-stu-id="82841-175">User</span></span></td>
<td><span data-ttu-id="82841-176">Stáhněte a nainstalujte mobilní aplikaci.</span><span class="sxs-lookup"><span data-stu-id="82841-176">Download and install the mobile app.</span></span></td>
<td><ul>
<li><span data-ttu-id="82841-177"><a href="https://go.microsoft.com/fwlink/?linkid=850662">Pro telefony Android</a></span><span class="sxs-lookup"><span data-stu-id="82841-177"><a href="https://go.microsoft.com/fwlink/?linkid=850662">For Android phones</a></span></span></li>
<li><span data-ttu-id="82841-178"><a href="https://go.microsoft.com/fwlink/?linkid=850663">Pro telefony iPhone</a></span><span class="sxs-lookup"><span data-stu-id="82841-178"><a href="https://go.microsoft.com/fwlink/?linkid=850663">For iPhones</a></span></span></li></ul>
</td>
</tr>
<tr class="odd">
<td><span data-ttu-id="82841-179">9</span><span class="sxs-lookup"><span data-stu-id="82841-179">9</span></span></td>
<td><span data-ttu-id="82841-180">Uživatel</span><span class="sxs-lookup"><span data-stu-id="82841-180">User</span></span></td>
<td><span data-ttu-id="82841-181">Přihlaste se do mobilní aplikace a použijte ji.</span><span class="sxs-lookup"><span data-stu-id="82841-181">Sign in, and use the mobile app.</span></span> <span data-ttu-id="82841-182">Aplikaci zahrnuje mobilní pracovní prostory, které byly publikovány správcem systému.</span><span class="sxs-lookup"><span data-stu-id="82841-182">The app includes the mobile workspaces that have been published by the system administrator.</span></span></td>
<td><span data-ttu-id="82841-183">Pokud chcete zobrazit seznam mobilních pracovních prostorů poskytnutých společností Microsoft, přejděte do tématu <a href="mobile-workspaces-released.md">Nedávno vydané mobilní pracovní prostory</a>.</span><span class="sxs-lookup"><span data-stu-id="82841-183">To see a list of mobile workspaces that are provided by Microsoft, see <a href="mobile-workspaces-released.md">Mobile workspaces recently released</a>.</span></span>
</td>
</tr>
</tbody>
</table>

