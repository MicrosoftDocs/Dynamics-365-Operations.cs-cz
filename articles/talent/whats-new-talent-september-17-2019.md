---
title: Co je nového nebo upraveného v aplikaci Dynamics 365 for Talent (17. září 2019)
description: Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 for Talent.
author: Darinkramer
manager: AnnBe
ms.date: 9/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-09-17
ms.dyn365.ops.version: Talent
ms.openlocfilehash: b7bdbbee7468eba100dedc96b5bcee7e03f249e1
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460559"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-september-17-2019"></a><span data-ttu-id="aa945-103">Co je nového nebo upraveného v aplikaci Dynamics 365 for Talent (17. září 2019)</span><span class="sxs-lookup"><span data-stu-id="aa945-103">What's new or changed in Dynamics 365 for Talent (September 17, 2019)</span></span>

<span data-ttu-id="aa945-104">Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Dynamics 365 for Talent.</span><span class="sxs-lookup"><span data-stu-id="aa945-104">This topic describes features that are either new or changed in Dynamics 365 for Talent.</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="aa945-105">Změny v aplikaci Attract</span><span class="sxs-lookup"><span data-stu-id="aa945-105">Changes in Attract</span></span>
<span data-ttu-id="aa945-106">Tato verze obsahuje dílčí opravy chyb pro aplikaci Dynamics 365 Talent: Attract.</span><span class="sxs-lookup"><span data-stu-id="aa945-106">This release includes minor bug fixes for Dynamics 365 Talent: Attract.</span></span>

## <a name="changes-in-onboard"></a><span data-ttu-id="aa945-107">Změny v aplikaci Onboard</span><span class="sxs-lookup"><span data-stu-id="aa945-107">Changes in Onboard</span></span>
<span data-ttu-id="aa945-108">Tato verze obsahuje dílčí opravy chyb pro aplikaci Dynamics 365 Talent: Onboard.</span><span class="sxs-lookup"><span data-stu-id="aa945-108">This release includes minor bug fixes for Dynamics 365 Talent: Onboard.</span></span>

## <a name="changes-in-core-hr"></a><span data-ttu-id="aa945-109">Změny v Core HR</span><span class="sxs-lookup"><span data-stu-id="aa945-109">Changes in Core HR</span></span>
<span data-ttu-id="aa945-110">Změny popsané v této části se vztahují na číslo sestavení 8.1.2492.</span><span class="sxs-lookup"><span data-stu-id="aa945-110">Changes described in this section apply to build number 8.1.2492.</span></span> <span data-ttu-id="aa945-111">Čísla v závorkách v některých záhlavích se vztahují na čísla podpory v Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="aa945-111">The numbers in parentheses in some headings refer to support numbers in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

### <a name="you-can-enable-preview-features-in-sandbox-and-trial-environments"></a><span data-ttu-id="aa945-112">Můžete povolit funkce náhledu v izolovaném prostoru a zkušebních prostředích.</span><span class="sxs-lookup"><span data-stu-id="aa945-112">You can enable preview features in Sandbox and Trial environments</span></span>

<span data-ttu-id="aa945-113">Když zřizujete novou instanci aplikace Talent, můžete určit, zda je typem instance Produkce nebo Sandbox.</span><span class="sxs-lookup"><span data-stu-id="aa945-113">When you provision a new instance of Talent, you can specify whether the instance type is Production or Sandbox.</span></span> <span data-ttu-id="aa945-114">Instance typu Sandbox umožňují dřívější zkoušení nových funkcí.</span><span class="sxs-lookup"><span data-stu-id="aa945-114">Instances of the Sandbox type allow for early trial of new features.</span></span> <span data-ttu-id="aa945-115">Chcete-li, aby byla jedna z existujících instancí aktualizována na typ instance Sandbox, obraťte se na podporu a inicializujte požadavek na změnu.</span><span class="sxs-lookup"><span data-stu-id="aa945-115">If you want one of your existing instances to be updated to the Sandbox instance type, contact Support to initiate the change request.</span></span>

<span data-ttu-id="aa945-116">Další informace o tom, jak jsou publikovány změny, naleznete v části [Zřízení aplikace Talent](./provisioning-talent.md).</span><span class="sxs-lookup"><span data-stu-id="aa945-116">For more information about how changes are published, see [Provision Talent](./provisioning-talent.md).</span></span>

### <a name="human-resources-staff-cant-see-performance-review-details-once-assigned-to-them-by-workflow-370308"></a><span data-ttu-id="aa945-117">Pracovníci personálního oddělení nevidí podrobnosti o kontrole výkonu, které jsou jim přiřazeny podle workflowu (370308).</span><span class="sxs-lookup"><span data-stu-id="aa945-117">Human Resources staff can't see performance review details once assigned to them by workflow (370308)</span></span>

<span data-ttu-id="aa945-118">Díky aktualizaci tohoto týdne budou pracovníci v oblasti lidských zdrojů moci vidět podrobnosti o kontrole výkonu, které vám byly přiřazeny prostřednictvím zpracování workflowu.</span><span class="sxs-lookup"><span data-stu-id="aa945-118">With this week's update, HR professionals will be able to see performance review details that have been assigned to them through workflow processing.</span></span> <span data-ttu-id="aa945-119">Chcete-li zobrazit recenze, přejděte na **samoobslužné stránky zaměstnanců > pracovní položky přiřazené mně**.</span><span class="sxs-lookup"><span data-stu-id="aa945-119">To view reviews, navigate to **Employee self-service > Work items assigned to me**.</span></span>

### <a name="job-family-field-missing-in-the-manage-changes-page-for-job-details-346031"></a><span data-ttu-id="aa945-120">Na stránce Správa změn pro podrobnosti úlohy chybí pole rodina úloh (346031)</span><span class="sxs-lookup"><span data-stu-id="aa945-120">Job family field missing in the Manage changes page for job details (346031)</span></span>

<span data-ttu-id="aa945-121">V této verzi bylo pro podrobnosti úlohy na stránce **Spravovat změny** přidáno pole rodina práce.</span><span class="sxs-lookup"><span data-stu-id="aa945-121">In this release, the job family field has been added to the **Manage changes** page for job details.</span></span>

## <a name="in-preview"></a><span data-ttu-id="aa945-122">Náhled</span><span class="sxs-lookup"><span data-stu-id="aa945-122">In preview</span></span>

### <a name="streamlined-employee-entry-and-navigation"></a><span data-ttu-id="aa945-123">Zjednodušené zadávání zaměstnance a navigace</span><span class="sxs-lookup"><span data-stu-id="aa945-123">Streamlined employee entry and navigation</span></span>

<span data-ttu-id="aa945-124">Tato funkce je nyní k dispozici v prostředích izolovaného prostoru.</span><span class="sxs-lookup"><span data-stu-id="aa945-124">This functionality is now available in sandbox environments.</span></span> <span data-ttu-id="aa945-125">Chcete-li tuto funkci zapnout, přejděte na **Správa systému > Odkazy > Nastavení > Systémové parametry > Funkce náhledu**.</span><span class="sxs-lookup"><span data-stu-id="aa945-125">To turn this feature on, navigate to **System administration > Links > Setup > System parameters > Preview features**.</span></span> <span data-ttu-id="aa945-126">Vyberte **Rozšířený formulář pracovníka a navigace**.</span><span class="sxs-lookup"><span data-stu-id="aa945-126">Select **Enhanced worker form and navigation**.</span></span> <span data-ttu-id="aa945-127">To povolí tyto změny pro všechny uživatele.</span><span class="sxs-lookup"><span data-stu-id="aa945-127">This will enable these changes for all users.</span></span> <span data-ttu-id="aa945-128">Tuto možnost můžete kdykoli vypnout.</span><span class="sxs-lookup"><span data-stu-id="aa945-128">You can turn this option off at any time.</span></span>

<span data-ttu-id="aa945-129">Další informace naleznete v tématu [Zjednodušené zadání zaměstnance a navigace](./streamlined-employee-entry.md).</span><span class="sxs-lookup"><span data-stu-id="aa945-129">For more information, see [Streamlined employee entry and navigation](./streamlined-employee-entry.md).</span></span> <span data-ttu-id="aa945-130">Chcete-li zobrazit změny, podívejte se na video [Přehled vlny 2 verze Dynamics 365 for Talent 2019](https://aka.ms/ROGT19RW2ROV).</span><span class="sxs-lookup"><span data-stu-id="aa945-130">To see the changes, watch the video [Dynamics 365 for Talent 2019 release wave 2 overview](https://aka.ms/ROGT19RW2ROV).</span></span>
