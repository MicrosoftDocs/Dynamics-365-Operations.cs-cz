---
title: Přístupová práva kontrolorů objektu nákladů
description: Toto téma poskytuje informace o přístupových právech pro kontrolory objektů nákladů.
author: AndersGirke
ms.date: 06/24/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CAMCostControlWorkspace, CAMParameters
audience: Application User
ms.reviewer: roschlom
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roschlom
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: fa8faf0f0f45f901151b3b20a1792b3d8f264fa6
ms.sourcegitcommit: 7d0cfb359a4abc7392ddb3f0b3e9539c40b7204d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/14/2021
ms.locfileid: "5897617"
---
# <a name="access-rights-for-cost-object-controllers"></a><span data-ttu-id="5a5c2-103">Přístupová práva kontrolorů objektu nákladů</span><span class="sxs-lookup"><span data-stu-id="5a5c2-103">Access rights for cost object controllers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5a5c2-104">Pracovní prostor **Řízení nákladů** je centrální bod, kde si mohou manažeři zobrazit výkonnost svých objektů nákladů.</span><span class="sxs-lookup"><span data-stu-id="5a5c2-104">The **Cost control** workspace is a central point where managers can view the performance of their cost objects.</span></span> <span data-ttu-id="5a5c2-105">Tento pracovní prostor umožňuje manažerům využít data nákladového účetnictví, i když nejsou nákladovými účetními.</span><span class="sxs-lookup"><span data-stu-id="5a5c2-105">This workspace lets managers consume Cost accounting data even though they aren't cost accountants.</span></span> <span data-ttu-id="5a5c2-106">Z důvodu bezpečnosti by mělo být dovoleno manažerům zobrazovat pouze data nákladového účetnictví, která se vztahují ke konkrétním objektům nákladů, za které jsou zodpovědní.</span><span class="sxs-lookup"><span data-stu-id="5a5c2-106">For security reasons, managers should be allowed to see only the Cost accounting data that is related to the specific cost objects that they are responsible for.</span></span>

<span data-ttu-id="5a5c2-107">Existují čtyři jedinečné role v nákladovém účetnictví.</span><span class="sxs-lookup"><span data-stu-id="5a5c2-107">There are four unique roles in Cost accounting.</span></span>

| <span data-ttu-id="5a5c2-108">Název role</span><span class="sxs-lookup"><span data-stu-id="5a5c2-108">Role name</span></span>               | <span data-ttu-id="5a5c2-109">Licence</span><span class="sxs-lookup"><span data-stu-id="5a5c2-109">License</span></span>      |
|-------------------------|--------------|
| <span data-ttu-id="5a5c2-110">Správce nákladového účetnictví</span><span class="sxs-lookup"><span data-stu-id="5a5c2-110">Cost accounting manager</span></span> | <span data-ttu-id="5a5c2-111">Aktivita</span><span class="sxs-lookup"><span data-stu-id="5a5c2-111">Activity</span></span>     |
| <span data-ttu-id="5a5c2-112">Nákladový účetní</span><span class="sxs-lookup"><span data-stu-id="5a5c2-112">Cost accountant</span></span>         | <span data-ttu-id="5a5c2-113">Operations</span><span class="sxs-lookup"><span data-stu-id="5a5c2-113">Operations</span></span>   |
| <span data-ttu-id="5a5c2-114">Úředník na pozici nákladového účetního</span><span class="sxs-lookup"><span data-stu-id="5a5c2-114">Cost accountant clerk</span></span>   | <span data-ttu-id="5a5c2-115">Operations</span><span class="sxs-lookup"><span data-stu-id="5a5c2-115">Operations</span></span>   |
| <span data-ttu-id="5a5c2-116">Kontrolor objektu nákladů</span><span class="sxs-lookup"><span data-stu-id="5a5c2-116">Cost object controller</span></span>  | <span data-ttu-id="5a5c2-117">Členové týmu</span><span class="sxs-lookup"><span data-stu-id="5a5c2-117">Team members</span></span> |

<span data-ttu-id="5a5c2-118">Toto téma vysvětluje, jak přiřadit manažerovi roli **Kontrolor objektu nákladů**.</span><span class="sxs-lookup"><span data-stu-id="5a5c2-118">This topic explains how to assign the **Cost object controller** role to a manager.</span></span>

<span data-ttu-id="5a5c2-119">Když je manažerovi přiřazena role **Kontrolor objektu nákladů**, může manažer provádět následující úkoly:</span><span class="sxs-lookup"><span data-stu-id="5a5c2-119">When the **Cost object controller** role is assigned to a manager, the manager can perform the following tasks:</span></span>

- <span data-ttu-id="5a5c2-120">Přistupovat k pracovnímu prostoru **Řízení nákladů** (v klientovi).</span><span class="sxs-lookup"><span data-stu-id="5a5c2-120">Access the **Cost control** workspace (in the client).</span></span>

    - <span data-ttu-id="5a5c2-121">Procházet a mít přístup pro zobrazení ke stránkám, které podporují podrobné procházení.</span><span class="sxs-lookup"><span data-stu-id="5a5c2-121">Drill through and have view access to the pages that support the drill-through experience.</span></span>

- <span data-ttu-id="5a5c2-122">Přistupovat k pracovnímu prostoru **Řízení nákladů** (v mobilní aplikaci).</span><span class="sxs-lookup"><span data-stu-id="5a5c2-122">Access the **Cost control** workspace (in the mobile application).</span></span>

> [!NOTE]
> <span data-ttu-id="5a5c2-123">**Náklady objektu řízeného** role není řízení nákladů, které předměty má uživatel přístup a zobrazit data pro.</span><span class="sxs-lookup"><span data-stu-id="5a5c2-123">The **Cost object controller** role doesn't control which cost objects the user can access and view data for.</span></span> <span data-ttu-id="5a5c2-124">Zabezpečení na úrovni řádku je poskytováno prostřednictvím hierarchií dimenzí a hierarchie přístupového seznamu.</span><span class="sxs-lookup"><span data-stu-id="5a5c2-124">Row-level security is provided via dimension hierarchies and the Access list hierarchy.</span></span>

## <a name="grant-access-rights"></a><span data-ttu-id="5a5c2-125">Udělení přístupových práv</span><span class="sxs-lookup"><span data-stu-id="5a5c2-125">Grant access rights</span></span>
<span data-ttu-id="5a5c2-126">Následující příklad ukazuje, jak může vypadat hierarchie dimenzí.</span><span class="sxs-lookup"><span data-stu-id="5a5c2-126">The following example shows what a dimension hierarchy can look like.</span></span>

<span data-ttu-id="5a5c2-127">**Podrobnosti hierarchie dimenze**</span><span class="sxs-lookup"><span data-stu-id="5a5c2-127">**Dimension hierarchy details**</span></span>

| <span data-ttu-id="5a5c2-128">Název hierarchie dimenze</span><span class="sxs-lookup"><span data-stu-id="5a5c2-128">Dimension hierarchy name</span></span> | <span data-ttu-id="5a5c2-129">Dimenze</span><span class="sxs-lookup"><span data-stu-id="5a5c2-129">Dimension</span></span>    | <span data-ttu-id="5a5c2-130">Název typu hierarchie dimenze</span><span class="sxs-lookup"><span data-stu-id="5a5c2-130">Dimension hierarchy type name</span></span>      | <span data-ttu-id="5a5c2-131">Hierarchie přístupového seznamu</span><span class="sxs-lookup"><span data-stu-id="5a5c2-131">Access list hierarchy</span></span> |
|--------------------------|--------------|------------------------------------|-----------------------|
| <span data-ttu-id="5a5c2-132">Organizace</span><span class="sxs-lookup"><span data-stu-id="5a5c2-132">Organization</span></span>             | <span data-ttu-id="5a5c2-133">Nákladová střediska</span><span class="sxs-lookup"><span data-stu-id="5a5c2-133">Cost centers</span></span> | <span data-ttu-id="5a5c2-134">Hierarchie klasifikace dimenzí</span><span class="sxs-lookup"><span data-stu-id="5a5c2-134">Dimension classification hierarchy</span></span> | <span data-ttu-id="5a5c2-135">**Ano**</span><span class="sxs-lookup"><span data-stu-id="5a5c2-135">**Yes**</span></span>               |

<span data-ttu-id="5a5c2-136">Můžete použít pevnou záložku **Uživatelé** v návrháři hierarchie, abyste vložili jedno nebo více ID uživatele na každém uzlu.</span><span class="sxs-lookup"><span data-stu-id="5a5c2-136">You can use the **Users** FastTab in the hierarchy designer to insert one or more user IDs on each node.</span></span>

|             <span data-ttu-id="5a5c2-137">Uzly</span><span class="sxs-lookup"><span data-stu-id="5a5c2-137">Nodes</span></span>                 | <span data-ttu-id="5a5c2-138">Uživatelé</span><span class="sxs-lookup"><span data-stu-id="5a5c2-138">Users</span></span>            | <span data-ttu-id="5a5c2-139">Z členu dimenze</span><span class="sxs-lookup"><span data-stu-id="5a5c2-139">From dimension member</span></span>     |   <span data-ttu-id="5a5c2-140">Člen do dimenze</span><span class="sxs-lookup"><span data-stu-id="5a5c2-140">To dimension member</span></span>   |
|-----------------------------------|------------------|---------------------------|-------------------------|
| <span data-ttu-id="5a5c2-141">Organizace</span><span class="sxs-lookup"><span data-stu-id="5a5c2-141">Organization</span></span>                      | <span data-ttu-id="5a5c2-142">Benjamin, Claire</span><span class="sxs-lookup"><span data-stu-id="5a5c2-142">Benjamin, Claire</span></span> |                           |                         |
| <span data-ttu-id="5a5c2-143">&nbsp;&nbsp;Správce</span><span class="sxs-lookup"><span data-stu-id="5a5c2-143">&nbsp;&nbsp;Admin</span></span>                 | <span data-ttu-id="5a5c2-144">Duben</span><span class="sxs-lookup"><span data-stu-id="5a5c2-144">April</span></span>            |                           |                         |
| <span data-ttu-id="5a5c2-145">&nbsp;&nbsp;&nbsp;&nbsp;Finance</span><span class="sxs-lookup"><span data-stu-id="5a5c2-145">&nbsp;&nbsp;&nbsp;&nbsp;Finance</span></span>   | <span data-ttu-id="5a5c2-146">Alicia</span><span class="sxs-lookup"><span data-stu-id="5a5c2-146">Alicia</span></span>           | <span data-ttu-id="5a5c2-147">CC002</span><span class="sxs-lookup"><span data-stu-id="5a5c2-147">CC002</span></span>                     | <span data-ttu-id="5a5c2-148">CC003</span><span class="sxs-lookup"><span data-stu-id="5a5c2-148">CC003</span></span>                   |
|                                   |                  | <span data-ttu-id="5a5c2-149">CC007</span><span class="sxs-lookup"><span data-stu-id="5a5c2-149">CC007</span></span>                     | <span data-ttu-id="5a5c2-150">CC007</span><span class="sxs-lookup"><span data-stu-id="5a5c2-150">CC007</span></span>                   |
| <span data-ttu-id="5a5c2-151">&nbsp;&nbsp;&nbsp;&nbsp;HR</span><span class="sxs-lookup"><span data-stu-id="5a5c2-151">&nbsp;&nbsp;&nbsp;&nbsp;HR</span></span>        | <span data-ttu-id="5a5c2-152">Arnie</span><span class="sxs-lookup"><span data-stu-id="5a5c2-152">Arnie</span></span>            | <span data-ttu-id="5a5c2-153">CC001</span><span class="sxs-lookup"><span data-stu-id="5a5c2-153">CC001</span></span>                     | <span data-ttu-id="5a5c2-154">CC001</span><span class="sxs-lookup"><span data-stu-id="5a5c2-154">CC001</span></span>                   |
| <span data-ttu-id="5a5c2-155">&nbsp;&nbsp;Výroba</span><span class="sxs-lookup"><span data-stu-id="5a5c2-155">&nbsp;&nbsp;Production</span></span>            | <span data-ttu-id="5a5c2-156">David</span><span class="sxs-lookup"><span data-stu-id="5a5c2-156">David</span></span>            |                           |                         |
| <span data-ttu-id="5a5c2-157">&nbsp;&nbsp;&nbsp;&nbsp;Balení</span><span class="sxs-lookup"><span data-stu-id="5a5c2-157">&nbsp;&nbsp;&nbsp;&nbsp;Packaging</span></span> | <span data-ttu-id="5a5c2-158">Ellen</span><span class="sxs-lookup"><span data-stu-id="5a5c2-158">Ellen</span></span>            | <span data-ttu-id="5a5c2-159">CC005</span><span class="sxs-lookup"><span data-stu-id="5a5c2-159">CC005</span></span>                     | <span data-ttu-id="5a5c2-160">CC005</span><span class="sxs-lookup"><span data-stu-id="5a5c2-160">CC005</span></span>                   |
| <span data-ttu-id="5a5c2-161">&nbsp;&nbsp;&nbsp;&nbsp;Sestavení</span><span class="sxs-lookup"><span data-stu-id="5a5c2-161">&nbsp;&nbsp;&nbsp;&nbsp;Assembly</span></span>  | <span data-ttu-id="5a5c2-162">Chris</span><span class="sxs-lookup"><span data-stu-id="5a5c2-162">Chris</span></span>            | <span data-ttu-id="5a5c2-163">CC006</span><span class="sxs-lookup"><span data-stu-id="5a5c2-163">CC006</span></span>                     | <span data-ttu-id="5a5c2-164">CC006</span><span class="sxs-lookup"><span data-stu-id="5a5c2-164">CC006</span></span>                   |

> [!NOTE]
> <span data-ttu-id="5a5c2-165">Nákladoví účetní musí být přiřazeni do hierarchie nejvyšší úrovně, aby mohli nahlížet do všech položek nákladového účetnictví.</span><span class="sxs-lookup"><span data-stu-id="5a5c2-165">Cost accountants should be assigned to the top level of the hierarchy, so that they can see all entries in Cost accounting.</span></span>

<span data-ttu-id="5a5c2-166">Než bude možné použít hierarchii přístupového seznamu a jeho bezpečnostní nastavení, musí být možnost **Povolit přístup k zobrazení pro členy dimenze objektu nákladů** nastavena na **Ano** na kartě **Obecné** na stránce **Parametry nákladového účetnictví** (**Nákladové účetnictví** > **Nastavení** > **Parametry**).</span><span class="sxs-lookup"><span data-stu-id="5a5c2-166">Before the Access list hierarchy and its security settings can be applied, the **Enable view access for cost object dimension members** option must be set to **Yes** on the **General** tab of the **Cost accounting parameters** page (**Cost accounting** > **Setup** > **Parameters**).</span></span>

<span data-ttu-id="5a5c2-167">Nastavení pro hierarchii přístupového seznamu se používají ke kontrole dat, zobrazených v následujících oblastech:</span><span class="sxs-lookup"><span data-stu-id="5a5c2-167">The settings for the Access list hierarchy are used to control the data that is shown in following areas:</span></span>

- <span data-ttu-id="5a5c2-168">Pracovní prostor **Řízení nákladů** (v klientovi):</span><span class="sxs-lookup"><span data-stu-id="5a5c2-168">**Cost control** workspace (in the client):</span></span>

    - <span data-ttu-id="5a5c2-169">Data na stránkách, které se používají k podrobnému prohlížení</span><span class="sxs-lookup"><span data-stu-id="5a5c2-169">Data on the pages that are used for drill-through</span></span>

- <span data-ttu-id="5a5c2-170">Pracovní prostoru **Řízení nákladů** (v mobilní aplikaci):</span><span class="sxs-lookup"><span data-stu-id="5a5c2-170">**Cost control** workspace (in the mobile application):</span></span>

    - <span data-ttu-id="5a5c2-171">Zůstatky na kartách</span><span class="sxs-lookup"><span data-stu-id="5a5c2-171">Balances in cards</span></span>

- <span data-ttu-id="5a5c2-172">Microsoft Power BI:</span><span class="sxs-lookup"><span data-stu-id="5a5c2-172">Microsoft Power BI:</span></span>

    - <span data-ttu-id="5a5c2-173">Data zobrazená ve vizualizacích Power BI</span><span class="sxs-lookup"><span data-stu-id="5a5c2-173">Data that is shown in Power BI visualizations</span></span>
    - <span data-ttu-id="5a5c2-174">Vizualizace dat Power BI, které jsou vloženy do klienta Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="5a5c2-174">Data Power BI visualizations that are embedded in the Dynamics 365 Finance client</span></span>

> [!IMPORTANT]
> - <span data-ttu-id="5a5c2-175">Než může hierarchie přístupového seznamu ovlivnit data v Power BI, musí být spárována hierarchie přístupového seznamu a zabezpečení na úrovni řádku v Power BI.</span><span class="sxs-lookup"><span data-stu-id="5a5c2-175">Before the Access list hierarchy can affect data in Power BI, the Access list hierarchy and row-level security in Power BI must be paired.</span></span> <span data-ttu-id="5a5c2-176">Další informace naleznete v tématu [Nastavení zabezpečení pro balíček obsahu nákladového účetnictví](../../fin-ops-core/dev-itpro/analytics/setup-security-cost-accounting-content-pack.md).</span><span class="sxs-lookup"><span data-stu-id="5a5c2-176">For more information, see [Set up security for Cost accounting content pack](../../fin-ops-core/dev-itpro/analytics/setup-security-cost-accounting-content-pack.md).</span></span>
> - <span data-ttu-id="5a5c2-177">Toto téma popisuje požadavky, které musí být splněny před použitím pracovního prostoru **Řízení nákladů**.</span><span class="sxs-lookup"><span data-stu-id="5a5c2-177">This topic shows the prerequisites that must be in place before you can use the **Cost control** workspace.</span></span>

<span data-ttu-id="5a5c2-178">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="5a5c2-178">Additional resources</span></span>

- [<span data-ttu-id="5a5c2-179">Pracovní prostor kontroly nákladů</span><span class="sxs-lookup"><span data-stu-id="5a5c2-179">Cost control workspace</span></span>](cost-control-workspace.md)
- [<span data-ttu-id="5a5c2-180">Hierarchie dimenzí</span><span class="sxs-lookup"><span data-stu-id="5a5c2-180">Dimension hierarchy</span></span>](dimension-hierarchy.md)
- [<span data-ttu-id="5a5c2-181">Nastavení zabezpečení pro balíček obsahu nákladového účetnictví</span><span class="sxs-lookup"><span data-stu-id="5a5c2-181">Set up security for Cost accounting content pack</span></span>](../../fin-ops-core/dev-itpro/analytics/setup-security-cost-accounting-content-pack.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
