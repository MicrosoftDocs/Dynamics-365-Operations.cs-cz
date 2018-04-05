---
title: "Definování přístupových práv pro kontrolory objektů nákladů"
description: "Toto téma poskytuje informace o přístupových právech pro kontrolory objektů nákladů."
author: AndersGirke
manager: AnnBe
ms.date: 06/24/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMCostControlWorkspace, CAMParameters
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 6403aabb6b029807b42ab1ccb11756dcb0dda5dc
ms.contentlocale: cs-cz
ms.lasthandoff: 03/26/2018

---

# <a name="access-rights-of-a-cost-object-controller"></a><span data-ttu-id="3ad3c-103">Přístupová práva kontrolora objektu nákladů</span><span class="sxs-lookup"><span data-stu-id="3ad3c-103">Access rights of a cost object controller</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="3ad3c-104">Pracovní prostor **Řízení nákladů** je centrální bod, kde si mohou manažeři zobrazit výkonnost svých objektů nákladů.</span><span class="sxs-lookup"><span data-stu-id="3ad3c-104">The **Cost control** workspace is a central point where managers can view the performance of their cost objects.</span></span> <span data-ttu-id="3ad3c-105">Tento pracovní prostor umožňuje manažerům využít data nákladového účetnictví, i když nejsou nákladovými účetními.</span><span class="sxs-lookup"><span data-stu-id="3ad3c-105">This workspace lets managers consume Cost accounting data even though they aren't cost accountants.</span></span> <span data-ttu-id="3ad3c-106">Z důvodu bezpečnosti by mělo být dovoleno manažerům zobrazovat pouze data nákladového účetnictví, která se vztahují ke konkrétním objektům nákladů, za které jsou zodpovědní.</span><span class="sxs-lookup"><span data-stu-id="3ad3c-106">For security reasons, managers should be allowed to see only the Cost accounting data that is related to the specific cost objects that they are responsible for.</span></span>

<span data-ttu-id="3ad3c-107">Existují čtyři jedinečné role v nákladovém účetnictví.</span><span class="sxs-lookup"><span data-stu-id="3ad3c-107">There are four unique roles in Cost accounting.</span></span>

| <span data-ttu-id="3ad3c-108">Název role</span><span class="sxs-lookup"><span data-stu-id="3ad3c-108">Role name</span></span>               | <span data-ttu-id="3ad3c-109">Licence</span><span class="sxs-lookup"><span data-stu-id="3ad3c-109">License</span></span>      |
|-------------------------|--------------|
| <span data-ttu-id="3ad3c-110">Správce nákladového účetnictví</span><span class="sxs-lookup"><span data-stu-id="3ad3c-110">Cost accounting manager</span></span> | <span data-ttu-id="3ad3c-111">Aktivita</span><span class="sxs-lookup"><span data-stu-id="3ad3c-111">Activity</span></span>     |
| <span data-ttu-id="3ad3c-112">Nákladový účetní</span><span class="sxs-lookup"><span data-stu-id="3ad3c-112">Cost accountant</span></span>         | <span data-ttu-id="3ad3c-113">Operations</span><span class="sxs-lookup"><span data-stu-id="3ad3c-113">Operations</span></span>   |
| <span data-ttu-id="3ad3c-114">Úředník na pozici nákladového účetního</span><span class="sxs-lookup"><span data-stu-id="3ad3c-114">Cost accountant clerk</span></span>   | <span data-ttu-id="3ad3c-115">Operations</span><span class="sxs-lookup"><span data-stu-id="3ad3c-115">Operations</span></span>   |
| <span data-ttu-id="3ad3c-116">Kontrolor objektu nákladů</span><span class="sxs-lookup"><span data-stu-id="3ad3c-116">Cost object controller</span></span>  | <span data-ttu-id="3ad3c-117">Členové týmu</span><span class="sxs-lookup"><span data-stu-id="3ad3c-117">Team members</span></span> |

<span data-ttu-id="3ad3c-118">Toto téma vysvětluje, jak přiřadit manažerovi roli **Kontrolor objektu nákladů**.</span><span class="sxs-lookup"><span data-stu-id="3ad3c-118">This topic explains how to assign the **Cost object controller** role to a manager.</span></span>

<span data-ttu-id="3ad3c-119">Když je manažerovi přiřazena role **Kontrolor objektu nákladů**, může manažer provádět následující úkoly:</span><span class="sxs-lookup"><span data-stu-id="3ad3c-119">When the **Cost object controller** role is assigned to a manager, the manager can perform the following tasks:</span></span>

- <span data-ttu-id="3ad3c-120">Přistupovat k pracovnímu prostoru **Řízení nákladů** (v klientovi).</span><span class="sxs-lookup"><span data-stu-id="3ad3c-120">Access the **Cost control** workspace (in the client).</span></span>

    - <span data-ttu-id="3ad3c-121">Procházet a mít přístup pro zobrazení ke stránkám, které podporují podrobné procházení.</span><span class="sxs-lookup"><span data-stu-id="3ad3c-121">Drill through and have view access to the pages that support the drill-through experience.</span></span>

- <span data-ttu-id="3ad3c-122">Přistupovat k pracovnímu prostoru **Řízení nákladů** (v mobilní aplikaci).</span><span class="sxs-lookup"><span data-stu-id="3ad3c-122">Access the **Cost control** workspace (in the mobile application).</span></span>

> [!NOTE]
> <span data-ttu-id="3ad3c-123">**Náklady objektu řízeného** role není řízení nákladů, které předměty má uživatel přístup a zobrazit data pro.</span><span class="sxs-lookup"><span data-stu-id="3ad3c-123">The **Cost object controller** role doesn't control which cost objects the user can access and view data for.</span></span> <span data-ttu-id="3ad3c-124">Zabezpečení na úrovni řádku je poskytováno prostřednictvím hierarchií dimenzí a hierarchie přístupového seznamu.</span><span class="sxs-lookup"><span data-stu-id="3ad3c-124">Row-level security is provided via dimension hierarchies and the Access list hierarchy.</span></span>

## <a name="grant-access-rights"></a><span data-ttu-id="3ad3c-125">Udělení přístupových práv</span><span class="sxs-lookup"><span data-stu-id="3ad3c-125">Grant access rights</span></span>
<span data-ttu-id="3ad3c-126">Následující příklad ukazuje, jak může vypadat hierarchie dimenzí.</span><span class="sxs-lookup"><span data-stu-id="3ad3c-126">The following example shows what a dimension hierarchy can look like.</span></span>

<span data-ttu-id="3ad3c-127">**Podrobnosti hierarchie dimenze**</span><span class="sxs-lookup"><span data-stu-id="3ad3c-127">**Dimension hierarchy details**</span></span>

| <span data-ttu-id="3ad3c-128">Název hierarchie dimenze</span><span class="sxs-lookup"><span data-stu-id="3ad3c-128">Dimension hierarchy name</span></span> | <span data-ttu-id="3ad3c-129">Dimenze</span><span class="sxs-lookup"><span data-stu-id="3ad3c-129">Dimension</span></span>    | <span data-ttu-id="3ad3c-130">Název typu hierarchie dimenze</span><span class="sxs-lookup"><span data-stu-id="3ad3c-130">Dimension hierarchy type name</span></span>      | <span data-ttu-id="3ad3c-131">Hierarchie přístupového seznamu</span><span class="sxs-lookup"><span data-stu-id="3ad3c-131">Access list hierarchy</span></span> |
|--------------------------|--------------|------------------------------------|-----------------------|
| <span data-ttu-id="3ad3c-132">Organizace</span><span class="sxs-lookup"><span data-stu-id="3ad3c-132">Organization</span></span>             | <span data-ttu-id="3ad3c-133">Nákladová střediska</span><span class="sxs-lookup"><span data-stu-id="3ad3c-133">Cost centers</span></span> | <span data-ttu-id="3ad3c-134">Hierarchie klasifikace dimenzí</span><span class="sxs-lookup"><span data-stu-id="3ad3c-134">Dimension classification hierarchy</span></span> | <span data-ttu-id="3ad3c-135">**Ano**</span><span class="sxs-lookup"><span data-stu-id="3ad3c-135">**Yes**</span></span>               |

<span data-ttu-id="3ad3c-136">Můžete použít pevnou záložku **Uživatelé** v návrháři hierarchie, abyste vložili jedno nebo více ID uživatele na každém uzlu.</span><span class="sxs-lookup"><span data-stu-id="3ad3c-136">You can use the **Users** FastTab in the hierarchy designer to insert one or more user IDs on each node.</span></span>

|                                   | <span data-ttu-id="3ad3c-137">Uživatelé</span><span class="sxs-lookup"><span data-stu-id="3ad3c-137">Users</span></span>            | <span data-ttu-id="3ad3c-138">Rozsahy členu dimenze</span><span class="sxs-lookup"><span data-stu-id="3ad3c-138">Dimension member ranges</span></span>   |                         |
|-----------------------------------|------------------|---------------------------|-------------------------|
| <span data-ttu-id="3ad3c-139">**Uzly**</span><span class="sxs-lookup"><span data-stu-id="3ad3c-139">**Nodes**</span></span>                         | <span data-ttu-id="3ad3c-140">**ID uživatele**</span><span class="sxs-lookup"><span data-stu-id="3ad3c-140">**User ID**</span></span>      | <span data-ttu-id="3ad3c-141">**Od členu dimenze**</span><span class="sxs-lookup"><span data-stu-id="3ad3c-141">**From dimension member**</span></span> | <span data-ttu-id="3ad3c-142">**Po člen dimenze**</span><span class="sxs-lookup"><span data-stu-id="3ad3c-142">**To dimension member**</span></span> |
| <span data-ttu-id="3ad3c-143">Organizace</span><span class="sxs-lookup"><span data-stu-id="3ad3c-143">Organization</span></span>                      | <span data-ttu-id="3ad3c-144">Benjamin, Claire</span><span class="sxs-lookup"><span data-stu-id="3ad3c-144">Benjamin, Claire</span></span> |                           |                         |
| <span data-ttu-id="3ad3c-145">&nbsp;&nbsp;Správce</span><span class="sxs-lookup"><span data-stu-id="3ad3c-145">&nbsp;&nbsp;Admin</span></span>                 | <span data-ttu-id="3ad3c-146">Duben</span><span class="sxs-lookup"><span data-stu-id="3ad3c-146">April</span></span>            |                           |                         |
| <span data-ttu-id="3ad3c-147">&nbsp;&nbsp;&nbsp;&nbsp;Finance</span><span class="sxs-lookup"><span data-stu-id="3ad3c-147">&nbsp;&nbsp;&nbsp;&nbsp;Finance</span></span>   | <span data-ttu-id="3ad3c-148">Alicia</span><span class="sxs-lookup"><span data-stu-id="3ad3c-148">Alicia</span></span>           | <span data-ttu-id="3ad3c-149">CC002</span><span class="sxs-lookup"><span data-stu-id="3ad3c-149">CC002</span></span>                     | <span data-ttu-id="3ad3c-150">CC003</span><span class="sxs-lookup"><span data-stu-id="3ad3c-150">CC003</span></span>                   |
|                                   |                  | <span data-ttu-id="3ad3c-151">CC007</span><span class="sxs-lookup"><span data-stu-id="3ad3c-151">CC007</span></span>                     | <span data-ttu-id="3ad3c-152">CC007</span><span class="sxs-lookup"><span data-stu-id="3ad3c-152">CC007</span></span>                   |
| <span data-ttu-id="3ad3c-153">&nbsp;&nbsp;&nbsp;&nbsp;HR</span><span class="sxs-lookup"><span data-stu-id="3ad3c-153">&nbsp;&nbsp;&nbsp;&nbsp;HR</span></span>        | <span data-ttu-id="3ad3c-154">Arnie</span><span class="sxs-lookup"><span data-stu-id="3ad3c-154">Arnie</span></span>            | <span data-ttu-id="3ad3c-155">CC001</span><span class="sxs-lookup"><span data-stu-id="3ad3c-155">CC001</span></span>                     | <span data-ttu-id="3ad3c-156">CC001</span><span class="sxs-lookup"><span data-stu-id="3ad3c-156">CC001</span></span>                   |
| <span data-ttu-id="3ad3c-157">&nbsp;&nbsp;Výroba</span><span class="sxs-lookup"><span data-stu-id="3ad3c-157">&nbsp;&nbsp;Production</span></span>            | <span data-ttu-id="3ad3c-158">David</span><span class="sxs-lookup"><span data-stu-id="3ad3c-158">David</span></span>            |                           |                         |
| <span data-ttu-id="3ad3c-159">&nbsp;&nbsp;&nbsp;&nbsp;Balení</span><span class="sxs-lookup"><span data-stu-id="3ad3c-159">&nbsp;&nbsp;&nbsp;&nbsp;Packaging</span></span> | <span data-ttu-id="3ad3c-160">Ellen</span><span class="sxs-lookup"><span data-stu-id="3ad3c-160">Ellen</span></span>            | <span data-ttu-id="3ad3c-161">CC005</span><span class="sxs-lookup"><span data-stu-id="3ad3c-161">CC005</span></span>                     | <span data-ttu-id="3ad3c-162">CC005</span><span class="sxs-lookup"><span data-stu-id="3ad3c-162">CC005</span></span>                   |
| <span data-ttu-id="3ad3c-163">&nbsp;&nbsp;&nbsp;&nbsp;Sestavení</span><span class="sxs-lookup"><span data-stu-id="3ad3c-163">&nbsp;&nbsp;&nbsp;&nbsp;Assembly</span></span>  | <span data-ttu-id="3ad3c-164">Chris</span><span class="sxs-lookup"><span data-stu-id="3ad3c-164">Chris</span></span>            | <span data-ttu-id="3ad3c-165">CC006</span><span class="sxs-lookup"><span data-stu-id="3ad3c-165">CC006</span></span>                     | <span data-ttu-id="3ad3c-166">CC006</span><span class="sxs-lookup"><span data-stu-id="3ad3c-166">CC006</span></span>                   |

> [!NOTE]
> <span data-ttu-id="3ad3c-167">Nákladoví účetní musí být přiřazeni do hierarchie nejvyšší úrovně, aby mohli nahlížet do všech položek nákladového účetnictví.</span><span class="sxs-lookup"><span data-stu-id="3ad3c-167">Cost accountants should be assigned to the top level of the hierarchy, so that they can see all entries in Cost accounting.</span></span>

<span data-ttu-id="3ad3c-168">Než bude možné použít hierarchii přístupového seznamu a jeho bezpečnostní nastavení, musí být možnost **Povolit přístup k zobrazení pro členy dimenze objektu nákladů** nastavena na **Ano** na kartě **Obecné** na stránce **Parametry nákladového účetnictví** (**Nákladové účetnictví** > **Nastavení** > **Parametry**).</span><span class="sxs-lookup"><span data-stu-id="3ad3c-168">Before the Access list hierarchy and its security settings can be applied, the **Enable view access for cost object dimension members** option must be set to **Yes** on the **General** tab of the **Cost accounting parameters** page (**Cost accounting** > **Setup** > **Parameters**).</span></span>

<span data-ttu-id="3ad3c-169">Nastavení pro hierarchii přístupového seznamu se používají ke kontrole dat, zobrazených v následujících oblastech:</span><span class="sxs-lookup"><span data-stu-id="3ad3c-169">The settings for the Access list hierarchy are used to control the data that is shown in following areas:</span></span>

- <span data-ttu-id="3ad3c-170">Pracovní prostor **Řízení nákladů** (v klientovi):</span><span class="sxs-lookup"><span data-stu-id="3ad3c-170">**Cost control** workspace (in the client):</span></span>

    - <span data-ttu-id="3ad3c-171">Data na stránkách, které se používají k podrobnému prohlížení</span><span class="sxs-lookup"><span data-stu-id="3ad3c-171">Data on the pages that are used for drill-through</span></span>

- <span data-ttu-id="3ad3c-172">Pracovní prostoru **Řízení nákladů** (v mobilní aplikaci):</span><span class="sxs-lookup"><span data-stu-id="3ad3c-172">**Cost control** workspace (in the mobile application):</span></span>

    - <span data-ttu-id="3ad3c-173">Zůstatky na kartách</span><span class="sxs-lookup"><span data-stu-id="3ad3c-173">Balances in cards</span></span>

- <span data-ttu-id="3ad3c-174">Microsoft Power BI:</span><span class="sxs-lookup"><span data-stu-id="3ad3c-174">Microsoft Power BI:</span></span>

    - <span data-ttu-id="3ad3c-175">Data zobrazená ve vizualizacích Power BI</span><span class="sxs-lookup"><span data-stu-id="3ad3c-175">Data that is shown in Power BI visualizations</span></span>
    - <span data-ttu-id="3ad3c-176">Vizualizace dat Power BI, vložené do klienta Microsoft Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="3ad3c-176">Data Power BI visualizations that are embedded in the Microsoft Dynamics 365 for Finance and Operations, client</span></span>

> [!IMPORTANT]
> - <span data-ttu-id="3ad3c-177">Než může hierarchie přístupového seznamu ovlivnit data v Power BI, musí být spárována hierarchie přístupového seznamu a zabezpečení na úrovni řádku v Power BI.</span><span class="sxs-lookup"><span data-stu-id="3ad3c-177">Before the Access list hierarchy can affect data in Power BI, the Access list hierarchy and row-level security in Power BI must be paired.</span></span> <span data-ttu-id="3ad3c-178">Další informace naleznete v tématu [Nastavení zabezpečení pro balíček obsahu nákladového účetnictví](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md).</span><span class="sxs-lookup"><span data-stu-id="3ad3c-178">For more information, see [Set up security for Cost accounting content pack](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md).</span></span>
> - <span data-ttu-id="3ad3c-179">Toto téma popisuje požadavky, které musí být splněny před použitím pracovního prostoru **Řízení nákladů**.</span><span class="sxs-lookup"><span data-stu-id="3ad3c-179">This topic shows the prerequisites that must be in place before you can use the **Cost control** workspace.</span></span>

<span data-ttu-id="3ad3c-180">Viz také</span><span class="sxs-lookup"><span data-stu-id="3ad3c-180">See also</span></span>

- [<span data-ttu-id="3ad3c-181">Pracovní prostor kontroly nákladů</span><span class="sxs-lookup"><span data-stu-id="3ad3c-181">Cost control workspace</span></span>](cost-control-workspace.md)
- [<span data-ttu-id="3ad3c-182">Hierarchie dimenzí</span><span class="sxs-lookup"><span data-stu-id="3ad3c-182">Dimension hierarchy</span></span>](dimension-hierarchy.md)
- [<span data-ttu-id="3ad3c-183">Nastavení zabezpečení pro balíček obsahu nákladového účetnictví</span><span class="sxs-lookup"><span data-stu-id="3ad3c-183">Set up security for Cost accounting content pack</span></span>](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md)

