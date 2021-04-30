---
title: Domovská stránka mobilní aplikace
description: Toto téma popisuje mobilní aplikaci Finance and Operations (Dynamics 365) a poskytuje odkazy na zdroje, které vám mohou pomoci ji implementovat ve vaší organizaci.
author: ChrisGarty
ms.date: 01/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.custom: 272853
ms.assetid: c99f818f-27b3-4e45-92b4-74272dad0e17
ms.search.region: Global
ms.author: cgarty
ms.dyn365.ops.version: Platform update 4
ms.search.validFrom: 2017-02-28
ms.openlocfilehash: 9707a1f8a90a615dbc8f34f4bb1f05d34d8fe7f3
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/16/2021
ms.locfileid: "5908225"
---
# <a name="mobile-app-home-page"></a><span data-ttu-id="b95c1-103">Domovská stránka mobilní aplikace</span><span class="sxs-lookup"><span data-stu-id="b95c1-103">Mobile app home page</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b95c1-104">Toto téma popisuje mobilní aplikaci **Finance and Operations (Dynamics 365)** a poskytuje odkazy na zdroje, které vám mohou pomoci ji implementovat ve vaší organizaci.</span><span class="sxs-lookup"><span data-stu-id="b95c1-104">This topic describes the **Finance and Operations (Dynamics 365)** mobile app and provides links to resources that can help you implement it in your organization.</span></span>

<a name="overview"></a><span data-ttu-id="b95c1-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="b95c1-105">Overview</span></span>
--------

<span data-ttu-id="b95c1-106">Mobilní aplikace umožňuje vaší organizaci zpřístupnit své obchodní procesy na mobilních zařízeních.</span><span class="sxs-lookup"><span data-stu-id="b95c1-106">The mobile app enables your organization to make its business processes available on mobile devices.</span></span> <span data-ttu-id="b95c1-107">Jakmile váš správce IT povolí mobilní pracovní prostory pro vaši organizaci, mohou se uživatelé přihlásit k aplikaci a okamžitě začít pracovat s obchodními procesy ze svých mobilních zařízení.</span><span class="sxs-lookup"><span data-stu-id="b95c1-107">After your IT admin enables the mobile workspaces for your organization, users can sign in to the app and immediately begin to run business processes from their mobile devices.</span></span> <span data-ttu-id="b95c1-108">Mobilní aplikace obsahuje následující funkce, které vám mohou pomoci zvýšit produktivitu:</span><span class="sxs-lookup"><span data-stu-id="b95c1-108">The mobile app includes the following features that can help increase productivity:</span></span>

- <span data-ttu-id="b95c1-109">Uživatelé mohou zobrazit, upravit a reagovat na obchodní data, i v případě, kdy mají občasné síťové připojení nebo kdy jsou jejich mobilní zařízení zcela offline.</span><span class="sxs-lookup"><span data-stu-id="b95c1-109">Users can view, edit, and act on business data, even if they have intermittent network connectivity or their mobile devices are completely offline.</span></span> <span data-ttu-id="b95c1-110">Při obnovení připojení k síti se offline datové operace automaticky zesynchronizují.</span><span class="sxs-lookup"><span data-stu-id="b95c1-110">When a device reestablishes a network connection, offline data operations are automatically synchronized.</span></span>
- <span data-ttu-id="b95c1-111">IT správci nebo vývojáři mohou vytvořit a publikovat mobilní pracovní prostory, které byly vytvořeny na míru pro jejich organizace.</span><span class="sxs-lookup"><span data-stu-id="b95c1-111">IT admins or developers can build and publish mobile workspaces that have been tailored to their organization.</span></span> <span data-ttu-id="b95c1-112">Aplikace používá vaše existující kódy majetku.</span><span class="sxs-lookup"><span data-stu-id="b95c1-112">The app uses your existing code assets.</span></span> <span data-ttu-id="b95c1-113">Z toho vyplývá, že není nutné znovu zavádět vaše postupy ověření, obchodní logik nebo konfiguraci zabezpečení.</span><span class="sxs-lookup"><span data-stu-id="b95c1-113">Therefore, you don't have to re-implement your validation procedures, business logic, or security configuration.</span></span>
- <span data-ttu-id="b95c1-114">IT správci nebo vývojáři mohou snadno navrhnout mobilní pracovní prostory pomocí „ukaž a klikni“ návrháře pracovního prostoru, který je součástí webového klienta.</span><span class="sxs-lookup"><span data-stu-id="b95c1-114">IT admins or developers can easily design mobile workspaces by using the point-and-click workspace designer that is included with the web client.</span></span>
- <span data-ttu-id="b95c1-115">IT správci nebo vývojáři mohou volitelně optimalizovat offline možnosti pracovního prostoru pomocí architektury rozšíření obchodní logiky.</span><span class="sxs-lookup"><span data-stu-id="b95c1-115">IT admins or developers can optionally optimize the offline capabilities of workspaces by using the Business logic extensibility framework.</span></span> <span data-ttu-id="b95c1-116">Vzhledem k tomu, že data se stále zpracovávají, i když je zařízení v režimu offline, vaše mobilní scénáře zůstávají bohaté a plynulé i tehdy, když nemají stálé síťové připojení.</span><span class="sxs-lookup"><span data-stu-id="b95c1-116">Because data continues to be processed while a device is offline, your mobile scenarios remain rich and fluid, even if devices don't have constant network connectivity.</span></span>

## <a name="elements-of-the-mobile-app"></a><span data-ttu-id="b95c1-117">Prvky mobilní aplikace</span><span class="sxs-lookup"><span data-stu-id="b95c1-117">Elements of the mobile app</span></span>
<span data-ttu-id="b95c1-118">Navigace v mobilní aplikaci se skládá ze čtyř základních konceptů: řídicího panelu, pracovních prostorů, stránek a akcí.</span><span class="sxs-lookup"><span data-stu-id="b95c1-118">Navigation in the mobile app consists of four basic concepts: the dashboard, workspaces, pages, and actions.</span></span> 

<span data-ttu-id="b95c1-119">[![Navigační koncepty v mobilní aplikaci](./media/mobilephoneapp1-1024x536.png)](./media/mobilephoneapp1.png)</span><span class="sxs-lookup"><span data-stu-id="b95c1-119">[![Navigation concepts in the mobile app](./media/mobilephoneapp1-1024x536.png)](./media/mobilephoneapp1.png)</span></span>

1. <span data-ttu-id="b95c1-120">Při spuštění aplikace přejděte do **řídicího panelu**.</span><span class="sxs-lookup"><span data-stu-id="b95c1-120">When you start the app, you go to the **dashboard**.</span></span>
2. <span data-ttu-id="b95c1-121">Na řídicím panelu můžete zobrazit seznam **pracovních prostorů**, které jsou publikované.</span><span class="sxs-lookup"><span data-stu-id="b95c1-121">On the dashboard, you can see a list of **workspaces** that have been published.</span></span>
3. <span data-ttu-id="b95c1-122">V každé pracovním prostoru se zobrazí seznam **stránek** dostupných pro daný pracovní prostor.</span><span class="sxs-lookup"><span data-stu-id="b95c1-122">In each workspace, you can see a list of **pages** that are available for that workspace.</span></span>
4. <span data-ttu-id="b95c1-123">Jakmile se dostanete na stránku, můžete provést několik akcí.</span><span class="sxs-lookup"><span data-stu-id="b95c1-123">After you're on a page, you can perform several actions.</span></span> <span data-ttu-id="b95c1-124">Několik příkladů:</span><span class="sxs-lookup"><span data-stu-id="b95c1-124">Here are some examples:</span></span>

    - <span data-ttu-id="b95c1-125">Zobrazení podrobných dat</span><span class="sxs-lookup"><span data-stu-id="b95c1-125">View detailed data.</span></span>
    - <span data-ttu-id="b95c1-126">Přechod na jiné stránky pro související data, jako jsou například podrobnosti entity nebo řádky.</span><span class="sxs-lookup"><span data-stu-id="b95c1-126">Navigate to other pages for related data, such as entity details or lines.</span></span>
    - <span data-ttu-id="b95c1-127">Zobrazení seznamu **akcí**, které jsou k dispozici pro danou stránku.</span><span class="sxs-lookup"><span data-stu-id="b95c1-127">See a list of **actions** that are available for that page.</span></span> <span data-ttu-id="b95c1-128">Akce vám umožňují vytvořit nebo upravit stávající data.</span><span class="sxs-lookup"><span data-stu-id="b95c1-128">Actions let you create or edit existing data.</span></span>

## <a name="implementation-process"></a><span data-ttu-id="b95c1-129">Proces implementace</span><span class="sxs-lookup"><span data-stu-id="b95c1-129">Implementation process</span></span>
<span data-ttu-id="b95c1-130">Následující obrázek znázorňuje proces implementace mobilních pracovních prostorů, které poskytuje společnost Microsoft, a vlastních mobilních pracovních prostorů.</span><span class="sxs-lookup"><span data-stu-id="b95c1-130">The following illustration shows the process for implementing both mobile workspaces that are provided by Microsoft and custom mobile workspaces.</span></span> 

<span data-ttu-id="b95c1-131">[![Proces implementace mobilní aplikace](./media/Mobile-implementation-process-5.png)](./media/Mobile-implementation-process-5.png)</span><span class="sxs-lookup"><span data-stu-id="b95c1-131">[![Mobile apps implementation process](./media/Mobile-implementation-process-5.png)](./media/Mobile-implementation-process-5.png)</span></span>

<span data-ttu-id="b95c1-132">Následující tabulka obsahuje odkazy na zdroje, které vám mohou pomoci při implementaci mobilních pracovních prostorů poskytovaných společností Microsoft a vlastních mobilních pracovních prostorů</span><span class="sxs-lookup"><span data-stu-id="b95c1-132">The following table includes links to resources that can help you implement both mobile workspaces that are provided by Microsoft and custom mobile workspaces.</span></span> <span data-ttu-id="b95c1-133">Čísla v prvním sloupci odpovídají číslovaným krokům na předchozím obrázku.</span><span class="sxs-lookup"><span data-stu-id="b95c1-133">The numbers in the first column correspond to the numbered steps in the previous illustration.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b95c1-134">Krok</span><span class="sxs-lookup"><span data-stu-id="b95c1-134">Step</span></span></th>
<th><span data-ttu-id="b95c1-135">Role</span><span class="sxs-lookup"><span data-stu-id="b95c1-135">Role</span></span></th>
<th><span data-ttu-id="b95c1-136">Akce</span><span class="sxs-lookup"><span data-stu-id="b95c1-136">Action</span></span></th>
<th><span data-ttu-id="b95c1-137">Prostředky umožňující dokončit akci</span><span class="sxs-lookup"><span data-stu-id="b95c1-137">Resources to help you complete the action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b95c1-138">1</span><span class="sxs-lookup"><span data-stu-id="b95c1-138">1</span></span></td>
<td><span data-ttu-id="b95c1-139">Správce systému</span><span class="sxs-lookup"><span data-stu-id="b95c1-139">System administrator</span></span></td>
<td><span data-ttu-id="b95c1-140">Implementujte aplikaci Finance and Operations ve vaší organizaci.</span><span class="sxs-lookup"><span data-stu-id="b95c1-140">Implement the Finance and Operations app in your organization.</span></span></td>
<td><ul><li><span data-ttu-id="b95c1-141">Pokud jste dosud nenainstalovali verzi aplikace Microsoft Dynamics 365, podívejte se do části <a href="../deployment/deploy-demo-environment.md">Nasazení prostředí pro ukázku</a>.</span><span class="sxs-lookup"><span data-stu-id="b95c1-141">If you haven&#39;t yet deployed a version of Microsoft Dynamics 365, see <a href="../deployment/deploy-demo-environment.md">Deploy a demo environment</a>.</span></span></li><li><span data-ttu-id="b95c1-142">Pokud chcete zobrazit seznam mobilních pracovních prostorů, které lze použít, přejděte do tématu <a href="mobile-workspaces-released.md">Nedávno vydané mobilní pracovní prostory</a>.</span><span class="sxs-lookup"><span data-stu-id="b95c1-142">To see a list of mobile workspaces that can be used, see <a href="mobile-workspaces-released.md">Mobile workspaces recently released</a>.</span></span></li></ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b95c1-143">2</span><span class="sxs-lookup"><span data-stu-id="b95c1-143">2</span></span></td>
<td><span data-ttu-id="b95c1-144">Správce systému</span><span class="sxs-lookup"><span data-stu-id="b95c1-144">System administrator</span></span></td>
<td><span data-ttu-id="b95c1-145"><strong>Pokud používáte Microsoft Dynamics 365 for Operations verzi 1611:</strong> Stáhněte a nainstalujte články znalostní báze, které umožňují mobilní pracovní prostory poskytnuté společností Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b95c1-145"><strong>If you&#39;re using Microsoft Dynamics 365 for Operations version 1611:</strong> Download and install KBs that enable the mobile workspaces that are provided by Microsoft.</span></span></td>
<td><span data-ttu-id="b95c1-146">Další informace naleznete v následujících tématech:</span><span class="sxs-lookup"><span data-stu-id="b95c1-146">See the following topics for more information:</span></span>
<ul>

<li><span data-ttu-id="b95c1-147"><a href="../../../finance/cost-accounting/cost-controlling-mobile-workspace.md">Mobilní pracovní prostory Řízení nákladů</a></span><span class="sxs-lookup"><span data-stu-id="b95c1-147"><a href="../../../finance/cost-accounting/cost-controlling-mobile-workspace.md">Cost controlling mobile workspaces</a></span></span></li>
<li><span data-ttu-id="b95c1-148"><a href="../../../supply-chain/inventory/inventory-on-hand-mobile-workspace.md">Mobilní pracovní prostor zásob na skladě</a></span><span class="sxs-lookup"><span data-stu-id="b95c1-148"><a href="../../../supply-chain/inventory/inventory-on-hand-mobile-workspace.md">Inventory on-hand mobile workspace</a></span></span></li>
<li><span data-ttu-id="b95c1-149"><a href="../../../supply-chain/sales-marketing/sales-orders-mobile-workspace.md">Mobilní pracovní prostory prodejních objednávek</a></span><span class="sxs-lookup"><span data-stu-id="b95c1-149"><a href="../../../supply-chain/sales-marketing/sales-orders-mobile-workspace.md">Sales orders mobile workspaces</a></span></span></li>
<li><span data-ttu-id="b95c1-150"><a href="../../../supply-chain/procurement/vendor-collaboration-mobile-workspace.md">Mobilní pracovní prostor dodavatelské spolupráce</a></span><span class="sxs-lookup"><span data-stu-id="b95c1-150"><a href="../../../supply-chain/procurement/vendor-collaboration-mobile-workspace.md">Vendor collaboration mobile workspace</a></span></span></li>
<li><span data-ttu-id="b95c1-151"><a href="/dynamics365/project-operations/prod-pma/project-time-entry-mobile-workspace">Mobilní pracovní prostor zadání času projektu</a></span><span class="sxs-lookup"><span data-stu-id="b95c1-151"><a href="/dynamics365/project-operations/prod-pma/project-time-entry-mobile-workspace">Project time entry mobile workspace</a></span></span></li>
<li><span data-ttu-id="b95c1-152"><a href="/dynamics365/project-operations/prod-exp/expense-management-mobile-workspace">Pracovnímu prostor správy výdajů</a></span><span class="sxs-lookup"><span data-stu-id="b95c1-152"><a href="/dynamics365/project-operations/prod-exp/expense-management-mobile-workspace">Expense management mobile workspace</a></span></span></li>

</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b95c1-153">3</span><span class="sxs-lookup"><span data-stu-id="b95c1-153">3</span></span></td>
<td><span data-ttu-id="b95c1-154">Správce systému</span><span class="sxs-lookup"><span data-stu-id="b95c1-154">System administrator</span></span></td>
<td><span data-ttu-id="b95c1-155">Publikujte mobilní pracovní prostory, které poskytuje společnost Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b95c1-155">Publish the mobile workspaces that are provided by Microsoft.</span></span></td>
<td><span data-ttu-id="b95c1-156"><a href="publish-mobile-workspace.md">Publikování mobilního pracovního prostoru</a>
</span><span class="sxs-lookup"><span data-stu-id="b95c1-156"><a href="publish-mobile-workspace.md">Publish a mobile workspace</a>
</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b95c1-157">4</span><span class="sxs-lookup"><span data-stu-id="b95c1-157">4</span></span></td>
<td><span data-ttu-id="b95c1-158">Vývojáři nebo nezávislí výrobci softwaru</span><span class="sxs-lookup"><span data-stu-id="b95c1-158">Developer or independent software vendor (ISV)</span></span></td>
<td><span data-ttu-id="b95c1-159">Použijte mobilní platformu k vytváření vlastních mobilních pracovních prostorů.</span><span class="sxs-lookup"><span data-stu-id="b95c1-159">Use the mobile platform to create custom mobile workspaces.</span></span></td>
<td><span data-ttu-id="b95c1-160"><a href="platform/mobile-platform-home-page.md">Mobilní platforma</a></span><span class="sxs-lookup"><span data-stu-id="b95c1-160"><a href="platform/mobile-platform-home-page.md">Mobile platform</a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b95c1-161">5</span><span class="sxs-lookup"><span data-stu-id="b95c1-161">5</span></span></td>
<td><span data-ttu-id="b95c1-162">ISV</span><span class="sxs-lookup"><span data-stu-id="b95c1-162">ISV</span></span></td>
<td><span data-ttu-id="b95c1-163">Vytvořte nasaditelný balíček, který obsahuje vlastní mobilní pracovní prostory, a odešlete balíček do služby Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="b95c1-163">Create a deployable package that contains custom mobile workspaces, and upload the package to Microsoft Dynamics Lifecycle Services (LCS).</span></span></td>
<td><span data-ttu-id="b95c1-164"><a href="../deployment/create-apply-deployable-package.md">Vytvoření nasaditelného balíčku</a></span><span class="sxs-lookup"><span data-stu-id="b95c1-164"><a href="../deployment/create-apply-deployable-package.md">Create a deployable package</a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b95c1-165">6</span><span class="sxs-lookup"><span data-stu-id="b95c1-165">6</span></span></td>
<td><span data-ttu-id="b95c1-166">Správce systému</span><span class="sxs-lookup"><span data-stu-id="b95c1-166">System administrator</span></span></td>
<td><span data-ttu-id="b95c1-167">Použijte nasaditelný balíček obsahující vlastní pracovní prostory, které poskytl nezávislý výrobce softwaru (ISV).</span><span class="sxs-lookup"><span data-stu-id="b95c1-167">Apply the deployable package that contains the custom workspaces that are provided by the independent software vendor (ISV).</span></span></td>
<td><span data-ttu-id="b95c1-168"><a href="../deployment/apply-deployable-package-system.md">Použití nasaditelného balíčku</a></span><span class="sxs-lookup"><span data-stu-id="b95c1-168"><a href="../deployment/apply-deployable-package-system.md">Apply a deployable package</a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b95c1-169">7</span><span class="sxs-lookup"><span data-stu-id="b95c1-169">7</span></span></td>
<td><span data-ttu-id="b95c1-170">Správce systému</span><span class="sxs-lookup"><span data-stu-id="b95c1-170">System administrator</span></span></td>
<td><span data-ttu-id="b95c1-171">Publikujte vlastní mobilní pracovní prostory, které poskytuje nezávislý výrobce softwaru.</span><span class="sxs-lookup"><span data-stu-id="b95c1-171">Publish the custom mobile workspaces that are provided by the ISV.</span></span></td>
<td><span data-ttu-id="b95c1-172"><a href="publish-mobile-workspace.md">Publikování mobilního pracovního prostoru</a></span><span class="sxs-lookup"><span data-stu-id="b95c1-172"><a href="publish-mobile-workspace.md">Publish a mobile workspace</a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b95c1-173">8</span><span class="sxs-lookup"><span data-stu-id="b95c1-173">8</span></span></td>
<td><span data-ttu-id="b95c1-174">Uživatel</span><span class="sxs-lookup"><span data-stu-id="b95c1-174">User</span></span></td>
<td><span data-ttu-id="b95c1-175">Stáhněte a nainstalujte mobilní aplikaci.</span><span class="sxs-lookup"><span data-stu-id="b95c1-175">Download and install the mobile app.</span></span></td>
<td><span data-ttu-id="b95c1-176">Aplikace 
<a href="https://go.microsoft.com/fwlink/?linkid=850662">Finance and Operations pro Android</a></span><span class="sxs-lookup"><span data-stu-id="b95c1-176">
<a href="https://go.microsoft.com/fwlink/?linkid=850662">Finance and Operations app for Android</a></span></span><BR/><span data-ttu-id="b95c1-177">Aplikace 
<a href="https://go.microsoft.com/fwlink/?linkid=850663">Finance and Operations pro iOS</a></span><span class="sxs-lookup"><span data-stu-id="b95c1-177">
<a href="https://go.microsoft.com/fwlink/?linkid=850663">Finance and Operations app for iOS</a></span></span><BR/>
<span data-ttu-id="b95c1-178">(Není podporován Windows Phone)</span><span class="sxs-lookup"><span data-stu-id="b95c1-178">(Windows Phone unsupported)</span></span>
</td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b95c1-179">9</span><span class="sxs-lookup"><span data-stu-id="b95c1-179">9</span></span></td>
<td><span data-ttu-id="b95c1-180">Uživatel</span><span class="sxs-lookup"><span data-stu-id="b95c1-180">User</span></span></td>
<td><span data-ttu-id="b95c1-181">Přihlaste se do mobilní aplikace a použijte ji.</span><span class="sxs-lookup"><span data-stu-id="b95c1-181">Sign in, and use the mobile app.</span></span> <span data-ttu-id="b95c1-182">Aplikaci zahrnuje mobilní pracovní prostory, které byly publikovány správcem systému.</span><span class="sxs-lookup"><span data-stu-id="b95c1-182">The app includes the mobile workspaces that have been published by the system administrator.</span></span></td>
<td><span data-ttu-id="b95c1-183">Pokud chcete zobrazit seznam mobilních pracovních prostorů poskytnutých společností Microsoft, přejděte do tématu <a href="mobile-workspaces-released.md">Nedávno vydané mobilní pracovní prostory</a>.</span><span class="sxs-lookup"><span data-stu-id="b95c1-183">To see a list of mobile workspaces that are provided by Microsoft, see <a href="mobile-workspaces-released.md">Mobile workspaces recently released</a>.</span></span>
</td>
</tr>
</tbody>
</table>

## <a name="troubleshooting"></a><span data-ttu-id="b95c1-184">Řešení potíží</span><span class="sxs-lookup"><span data-stu-id="b95c1-184">Troubleshooting</span></span>
[<span data-ttu-id="b95c1-185">Zdroje mobilní platformy</span><span class="sxs-lookup"><span data-stu-id="b95c1-185">Mobile platform resources</span></span>](platform/mobile-platform-home-page.md#troubleshooting-the-app)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]