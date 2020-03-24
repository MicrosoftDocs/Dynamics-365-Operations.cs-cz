---
title: Odstraněné nebo zastaralé funkce v aplikaci Dynamics 365 Finance
description: Toto téma popisuje funkce, které byly odebrány nebo u nichž se plánuje odstranění z Dynamics 365 Finance.
author: roschlom
manager: AnnBe
ms.date: 03/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2020-03-02
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: ec13076e6a05c3402af566487f7921f6971da215
ms.sourcegitcommit: 1e7e7c4bc197b0a42e4d53d2a54600a2fb125b69
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/13/2020
ms.locfileid: "3127970"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-finance"></a><span data-ttu-id="8b230-103">Odstraněné nebo zastaralé funkce v aplikaci Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="8b230-103">Removed or deprecated features in Dynamics 365 Finance</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8b230-104">Toto téma popisuje funkce, které byly odebrány nebo u nichž se plánuje odstranění z Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="8b230-104">This topic describes features that have been removed, or that are planned for removal from Dynamics 365 Finance.</span></span>

- <span data-ttu-id="8b230-105">*Odstraněná* funkce již není k dispozici v produktu.</span><span class="sxs-lookup"><span data-stu-id="8b230-105">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="8b230-106">*Zastaralá* funkce není v aktivním nasazení a v budoucí aktualizaci může být odstraněna.</span><span class="sxs-lookup"><span data-stu-id="8b230-106">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="8b230-107">Tento seznam je určen k tomu, aby vám pomohl zvážit tyto odstraněné a zastaralé funkce při svém plánování.</span><span class="sxs-lookup"><span data-stu-id="8b230-107">This list is intended to help you consider these removals and deprecations for your own planning.</span></span> 

> [!NOTE]
> <span data-ttu-id="8b230-108">Podrobné informace o objektech v aplikacích Finance and Operations lze nalézt v části [Sestavy technických informací](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span><span class="sxs-lookup"><span data-stu-id="8b230-108">Detailed information about objects in Finance and Operations apps can be found in the [Technical reference reports](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span></span> <span data-ttu-id="8b230-109">Můžete srovnat různé verze těchto sestav a zjistíte, které objekty se změnily nebo byly odstraněny v každé z verzí aplikací Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="8b230-109">You can compare the different versions of these reports to learn about objects that have changed or been removed in each version of Finance and Operations apps.</span></span>

## <a name="features-removed-or-deprecated-in-the-finance-10012-release"></a><span data-ttu-id="8b230-110">Odebrané nebo zastaralé funkce v aplikaci Finance verze 10.0.12</span><span class="sxs-lookup"><span data-stu-id="8b230-110">Features removed or deprecated in the Finance 10.0.12 release</span></span>

### <a name="polish-ssrs-reports-sales-vat-register-purchase-vat-register-eu-summary-vat-register--feature-reference-pl-00014"></a><span data-ttu-id="8b230-111">Polské sestavy SSRS: registr DPH na výstupu, registr DPH na vstupu, souhrnný registr DPH v EU – odkaz na funkci PL-00014</span><span class="sxs-lookup"><span data-stu-id="8b230-111">Polish SSRS reports: Sales VAT register, Purchase VAT register, EU summary VAT register – Feature reference PL-00014</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="8b230-112">**Důvod pro zrušení/odstranění**</span><span class="sxs-lookup"><span data-stu-id="8b230-112">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="8b230-113">Není vyžadováno zákonem.</span><span class="sxs-lookup"><span data-stu-id="8b230-113">Not legally required.</span></span>  |
| <span data-ttu-id="8b230-114">**Nahrazeno jinou funkcí?**</span><span class="sxs-lookup"><span data-stu-id="8b230-114">**Replaced by another feature?**</span></span>   | <span data-ttu-id="8b230-115">Ano (formát aplikace Excel pro standardní soubor auditu s přiznáním k DPH – JPK_VDEK)</span><span class="sxs-lookup"><span data-stu-id="8b230-115">Yes (Excel format for Standard Audit File with VAT declaration - JPK_VDEK)</span></span> |
| <span data-ttu-id="8b230-116">**Ovlivněné oblasti produktu**</span><span class="sxs-lookup"><span data-stu-id="8b230-116">**Product areas affected**</span></span>         | <span data-ttu-id="8b230-117">Přihláška</span><span class="sxs-lookup"><span data-stu-id="8b230-117">Application</span></span> |
| <span data-ttu-id="8b230-118">**Možnost nasazení**</span><span class="sxs-lookup"><span data-stu-id="8b230-118">**Deployment option**</span></span>              | <span data-ttu-id="8b230-119">Vše</span><span class="sxs-lookup"><span data-stu-id="8b230-119">All</span></span> |
| <span data-ttu-id="8b230-120">**Stav**</span><span class="sxs-lookup"><span data-stu-id="8b230-120">**Status**</span></span>                         | <span data-ttu-id="8b230-121">Zastaralé: Od 1. července 2021 plánujeme již dále nepodporovat sestavy SSRS: **registr DPH na výstupu, registr DPH na vstupu, souhrnný registr DPH v EU – odkaz na funkci PL-00014**.</span><span class="sxs-lookup"><span data-stu-id="8b230-121">Deprecated: By July 1, 2021, we plan to no longer support the SSRS reports: **Sales VAT register, Purchase VAT register, EU summary VAT register – Feature reference PL-00014**.</span></span> <span data-ttu-id="8b230-122">Namísto toho bude zaveden příklad formátu aplikace Excel pro standardní soubor auditu s přiznáním k DPH (JPK_VDEK).</span><span class="sxs-lookup"><span data-stu-id="8b230-122">Excel format example for Standard Audit File with VAT declaration (JPK_VDEK) will be introduced instead.</span></span> |

## <a name="features-removed-or-deprecated-in-the-finance-1007-release"></a><span data-ttu-id="8b230-123">Odebrané nebo zastaralé funkce v aplikaci Finance verze 10.0.7</span><span class="sxs-lookup"><span data-stu-id="8b230-123">Features removed or deprecated in the Finance 10.0.7 release</span></span>

### <a name="workflow-request-change-dialog-box-no-longer-includes-user-selection-drop-down-list"></a><span data-ttu-id="8b230-124">Dialogové okno pro změnu požadavku workflowu již neobsahuje rozevírací seznam pro výběr uživatele.</span><span class="sxs-lookup"><span data-stu-id="8b230-124">Workflow request change dialog box no longer includes user selection drop-down list</span></span>
|   |  |
|------------|--------------------|
| <span data-ttu-id="8b230-125">**Důvod pro zrušení/odstranění**</span><span class="sxs-lookup"><span data-stu-id="8b230-125">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="8b230-126">Změněno na funkci s výběrem skupiny účtů.</span><span class="sxs-lookup"><span data-stu-id="8b230-126">Changed to the feature with account groups selection.</span></span>  |
| <span data-ttu-id="8b230-127">**Nahrazeno jinou funkcí?**</span><span class="sxs-lookup"><span data-stu-id="8b230-127">**Replaced by another feature?**</span></span>   | <span data-ttu-id="8b230-128">Ano</span><span class="sxs-lookup"><span data-stu-id="8b230-128">Yes</span></span> |
| <span data-ttu-id="8b230-129">**Ovlivněné oblasti produktu**</span><span class="sxs-lookup"><span data-stu-id="8b230-129">**Product areas affected**</span></span>         | <span data-ttu-id="8b230-130">Workflow</span><span class="sxs-lookup"><span data-stu-id="8b230-130">Workflow</span></span> |
| <span data-ttu-id="8b230-131">**Možnost nasazení**</span><span class="sxs-lookup"><span data-stu-id="8b230-131">**Deployment option**</span></span>              | <span data-ttu-id="8b230-132">Vše</span><span class="sxs-lookup"><span data-stu-id="8b230-132">All</span></span> |
| <span data-ttu-id="8b230-133">**Stav**</span><span class="sxs-lookup"><span data-stu-id="8b230-133">**Status**</span></span>                         | <span data-ttu-id="8b230-134">Zastaralé: do 1. prosince 2020 plánujeme nadále nepodporovat nastavení čínských typů dokladů bez výběru skupin účtů.</span><span class="sxs-lookup"><span data-stu-id="8b230-134">Deprecated: By December 1, 2020, we plan to no longer support Chinese voucher types setup without Account groups selection.</span></span> <span data-ttu-id="8b230-135">Další informace o novém designu najdete v části [Co je nového ve verzi 10.0.7](whats-new-changed-10-0-7.md).</span><span class="sxs-lookup"><span data-stu-id="8b230-135">Find more details about the new design in [What's new in 10.0.7](whats-new-changed-10-0-7.md).</span></span> |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a><span data-ttu-id="8b230-136">Předchozí oznámení o odebraných nebo zastaralých funkcích</span><span class="sxs-lookup"><span data-stu-id="8b230-136">Previous announcements about removed or deprecated features</span></span>
<span data-ttu-id="8b230-137">Další informace o funkcích, které byly v předchozích verzích odebrány nebo zastaraly, naleznete v tématu [Odebrané nebo zastaralé funkce v předchozích verzích](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).</span><span class="sxs-lookup"><span data-stu-id="8b230-137">To learn more about features that have been removed or deprecated in previous releases, see [Removed or deprecated features in previous releases](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).</span></span>
