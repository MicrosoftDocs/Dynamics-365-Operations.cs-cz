---
title: Odstraněné nebo zastaralé funkce v aplikaci Dynamics 365 Finance
description: Toto téma popisuje funkce, které byly odebrány nebo u nichž se plánuje odstranění z Dynamics 365 Finance.
author: roschlom
manager: AnnBe
ms.date: 12/07/2020
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
ms.openlocfilehash: a406db6d78302fa05596a58fffb7464222d4bfea
ms.sourcegitcommit: 069ed5789517b550065e5e2317658fec4027359e
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/07/2020
ms.locfileid: "4689487"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-finance"></a><span data-ttu-id="7a218-103">Odstraněné nebo zastaralé funkce v aplikaci Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="7a218-103">Removed or deprecated features in Dynamics 365 Finance</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7a218-104">Toto téma popisuje funkce, které byly odebrány nebo u nichž se plánuje odstranění z Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="7a218-104">This topic describes features that have been removed, or that are planned for removal from Dynamics 365 Finance.</span></span>

- <span data-ttu-id="7a218-105">*Odstraněná* funkce již není k dispozici v produktu.</span><span class="sxs-lookup"><span data-stu-id="7a218-105">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="7a218-106">*Zastaralá* funkce není v aktivním nasazení a v budoucí aktualizaci může být odstraněna.</span><span class="sxs-lookup"><span data-stu-id="7a218-106">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="7a218-107">Tento seznam je určen k tomu, aby vám pomohl zvážit tyto odstraněné a zastaralé funkce při svém plánování.</span><span class="sxs-lookup"><span data-stu-id="7a218-107">This list is intended to help you consider these removals and deprecations for your own planning.</span></span> 

> [!NOTE]
> <span data-ttu-id="7a218-108">Podrobné informace o objektech v aplikacích Finance and Operations lze nalézt v části [Sestavy technických informací](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span><span class="sxs-lookup"><span data-stu-id="7a218-108">Detailed information about objects in Finance and Operations apps can be found in the [Technical reference reports](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span></span> <span data-ttu-id="7a218-109">Můžete srovnat různé verze těchto sestav a zjistíte, které objekty se změnily nebo byly odstraněny v každé z verzí aplikací Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="7a218-109">You can compare the different versions of these reports to learn about objects that have changed or been removed in each version of Finance and Operations apps.</span></span>

## <a name="features-removed-or-deprecated-in-the-finance-10016-release"></a><span data-ttu-id="7a218-110">Odebrané nebo zastaralé funkce v aplikaci Finance verze 10.0.16</span><span class="sxs-lookup"><span data-stu-id="7a218-110">Features removed or deprecated in the Finance 10.0.16 release</span></span>

### <a name="ledger-transaction-export-format-be-electronic-reporting-format-and-respective-ledger-transaction-export-be-model-for-belgium"></a><span data-ttu-id="7a218-111">„Formát exportu transakcí hlavní knihy (BE)“ Formát elektronického hlášení a příslušný model „Export transakcí hlavní knihy (BE)“ pro Belgii</span><span class="sxs-lookup"><span data-stu-id="7a218-111">"Ledger transaction export format (BE)" Electronic reporting format and respective "Ledger transaction export (BE)" model for Belgium</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="7a218-112">**Důvod pro zrušení/odstranění**</span><span class="sxs-lookup"><span data-stu-id="7a218-112">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="7a218-113">Nahrazeno novým formátem ER v modelu „Standardní soubor auditu (SAF-T)“.</span><span class="sxs-lookup"><span data-stu-id="7a218-113">Replaced with new ER format under "Standard Audit File (SAF-T)" model.</span></span>  |
| <span data-ttu-id="7a218-114">**Nahrazeno jinou funkcí?**</span><span class="sxs-lookup"><span data-stu-id="7a218-114">**Replaced by another feature?**</span></span>   | <span data-ttu-id="7a218-115">Ano</span><span class="sxs-lookup"><span data-stu-id="7a218-115">Yes</span></span> |
| <span data-ttu-id="7a218-116">**Ovlivněné oblasti produktu**</span><span class="sxs-lookup"><span data-stu-id="7a218-116">**Product areas affected**</span></span>         | <span data-ttu-id="7a218-117">Přihláška</span><span class="sxs-lookup"><span data-stu-id="7a218-117">Application</span></span> |
| <span data-ttu-id="7a218-118">**Možnost nasazení**</span><span class="sxs-lookup"><span data-stu-id="7a218-118">**Deployment option**</span></span>              | <span data-ttu-id="7a218-119">Vše</span><span class="sxs-lookup"><span data-stu-id="7a218-119">All</span></span> |
| <span data-ttu-id="7a218-120">**Stav**</span><span class="sxs-lookup"><span data-stu-id="7a218-120">**Status**</span></span>                         | <span data-ttu-id="7a218-121">Zastaralé: Do 1. prosince 2021 plánujeme, že již nebudeme podporovat formát elektronického výkaznictví (ER) „Formát exportu transakcí hlavní knihy (BE)“ a příslušný model „Export transakcí hlavní knihy (BE)“.</span><span class="sxs-lookup"><span data-stu-id="7a218-121">Deprecated: By December 1, 2021, we plan to no longer support the "Ledger transaction export format (BE)" Electronic reporting (ER) format and respective "Ledger transaction export (BE)" model.</span></span> <span data-ttu-id="7a218-122">V rámci modelu „Standardní soubor auditu (SAF-T)“ je místo toho zaveden nový formát „Export dat hlavní knihy (BE)“ spolu s „Mapováním datového modelu hlavní knihy“.</span><span class="sxs-lookup"><span data-stu-id="7a218-122">A new "General ledger data export (BE)" format together with "General ledger data model mapping" are introduced instead under the "Standard Audit File (SAF-T)" model.</span></span> |

### <a name="vat-100-report-for-the-united-kingdom-in-ssrs-format"></a><span data-ttu-id="7a218-123">Sestava "VAT 100" pro spojené království ve formátu SSRS</span><span class="sxs-lookup"><span data-stu-id="7a218-123">"VAT 100" report for the United Kingdom in SSRS format</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="7a218-124">**Důvod pro zrušení/odstranění**</span><span class="sxs-lookup"><span data-stu-id="7a218-124">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="7a218-125">Nahrazeno novým formátem ER - formát „Declaration VAT Excel (UK)“ pod „Model daňového přiznání“.</span><span class="sxs-lookup"><span data-stu-id="7a218-125">Replaced with new ER format - "VAT Declaration Excel (UK)" format under "Tax declaration model".</span></span>  |
| <span data-ttu-id="7a218-126">**Nahrazeno jinou funkcí?**</span><span class="sxs-lookup"><span data-stu-id="7a218-126">**Replaced by another feature?**</span></span>   | <span data-ttu-id="7a218-127">Ano</span><span class="sxs-lookup"><span data-stu-id="7a218-127">Yes</span></span> |
| <span data-ttu-id="7a218-128">**Ovlivněné oblasti produktu**</span><span class="sxs-lookup"><span data-stu-id="7a218-128">**Product areas affected**</span></span>         | <span data-ttu-id="7a218-129">Přihláška</span><span class="sxs-lookup"><span data-stu-id="7a218-129">Application</span></span> |
| <span data-ttu-id="7a218-130">**Možnost nasazení**</span><span class="sxs-lookup"><span data-stu-id="7a218-130">**Deployment option**</span></span>              | <span data-ttu-id="7a218-131">Vše</span><span class="sxs-lookup"><span data-stu-id="7a218-131">All</span></span> |
| <span data-ttu-id="7a218-132">**Stav**</span><span class="sxs-lookup"><span data-stu-id="7a218-132">**Status**</span></span>                         | <span data-ttu-id="7a218-133">Zastaralé: Do 1. prosince 2021 plánujeme, že již nebudeme podporovat „přehled 100 DPH“ ve formátu SSRS.</span><span class="sxs-lookup"><span data-stu-id="7a218-133">Deprecated: By December 1, 2021, we plan to no longer support the "VAT 100 report" in SSRS format.</span></span> <span data-ttu-id="7a218-134">Pro EU byl zaveden nový formát "Prohlášení o DPH Excel (UK)" v sekci "Model daňového přiznání" [Funkce DPH MTD](../localizations/emea-gbr-mtd-vat-integration.md).</span><span class="sxs-lookup"><span data-stu-id="7a218-134">A new "VAT Declaration Excel (UK)" format under "Tax declaration model" was introduced in the [MTD VAT feature](../localizations/emea-gbr-mtd-vat-integration.md).</span></span> |

## <a name="features-removed-or-deprecated-in-the-finance-10015-release"></a><span data-ttu-id="7a218-135">Odebrané nebo zastaralé funkce v aplikaci Finance verze 10.0.15</span><span class="sxs-lookup"><span data-stu-id="7a218-135">Features removed or deprecated in the Finance 10.0.15 release</span></span>

### <a name="internet-explorer-11-support-for-dynamics-365-is-deprecated"></a><span data-ttu-id="7a218-136">Podpora aplikace Internet Explorer 11 pro Dynamics 365 je zastaralá</span><span class="sxs-lookup"><span data-stu-id="7a218-136">Internet Explorer 11 support for Dynamics 365 is deprecated</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="7a218-137">**Důvod pro zrušení/odstranění**</span><span class="sxs-lookup"><span data-stu-id="7a218-137">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="7a218-138">S platností od prosince 2020 je podpora aplikace Microsoft Internet Explorer 11 zastaralá pro všechny produkty Dynamics 365 a Internet Explorer 11 nebude podporován po srpnu 2021.</span><span class="sxs-lookup"><span data-stu-id="7a218-138">Effective December 2020, Microsoft Internet Explorer 11 support for all Dynamics 365 products is deprecated, and Internet Explorer 11 won’t be supported after August 2021.</span></span><br><br><span data-ttu-id="7a218-139">To bude mít dopad na zákazníky, kteří používají produkty Dynamics 365, které jsou navrženy pro použití prostřednictvím rozhraní Internet Explorer 11.</span><span class="sxs-lookup"><span data-stu-id="7a218-139">This will impact customers who use Dynamics 365 products that are designed to be used through an Internet Explorer 11 interface.</span></span> <span data-ttu-id="7a218-140">Po srpnu 2021 nebude Internet Explorer 11 podporován pro takové produkty Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="7a218-140">After August 2021, Internet Explorer 11 won't be supported for such Dynamics 365 products.</span></span> |
| <span data-ttu-id="7a218-141">**Nahrazeno jinou funkcí?**</span><span class="sxs-lookup"><span data-stu-id="7a218-141">**Replaced by another feature?**</span></span>   | <span data-ttu-id="7a218-142">Doporučujeme zákazníkům přejít na Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="7a218-142">We recommend that customers transition to Microsoft Edge.</span></span>|
| <span data-ttu-id="7a218-143">**Ovlivněné oblasti produktu**</span><span class="sxs-lookup"><span data-stu-id="7a218-143">**Product areas affected**</span></span>         | <span data-ttu-id="7a218-144">Všechny produkty Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="7a218-144">All Dynamics 365 products</span></span> |
| <span data-ttu-id="7a218-145">**Možnost nasazení**</span><span class="sxs-lookup"><span data-stu-id="7a218-145">**Deployment option**</span></span>              | <span data-ttu-id="7a218-146">Vše</span><span class="sxs-lookup"><span data-stu-id="7a218-146">All</span></span>|
| <span data-ttu-id="7a218-147">**Stav**</span><span class="sxs-lookup"><span data-stu-id="7a218-147">**Status**</span></span>                         | <span data-ttu-id="7a218-148">Zastaralé.</span><span class="sxs-lookup"><span data-stu-id="7a218-148">Deprecated.</span></span> <span data-ttu-id="7a218-149">Internet Explorer 11 nebude podporován po srpnu 2021.</span><span class="sxs-lookup"><span data-stu-id="7a218-149">Internet Explorer 11 won’t be supported after August 2021.</span></span>|

## <a name="features-removed-or-deprecated-in-the-finance-10012-release"></a><span data-ttu-id="7a218-150">Odebrané nebo zastaralé funkce v aplikaci Finance verze 10.0.12</span><span class="sxs-lookup"><span data-stu-id="7a218-150">Features removed or deprecated in the Finance 10.0.12 release</span></span>

### <a name="polish-ssrs-reports-sales-vat-register-purchase-vat-register-eu-summary-vat-register--feature-reference-pl-00014"></a><span data-ttu-id="7a218-151">Polské sestavy SSRS: registr DPH na výstupu, registr DPH na vstupu, souhrnný registr DPH v EU – odkaz na funkci PL-00014</span><span class="sxs-lookup"><span data-stu-id="7a218-151">Polish SSRS reports: Sales VAT register, Purchase VAT register, EU summary VAT register – Feature reference PL-00014</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="7a218-152">**Důvod pro zrušení/odstranění**</span><span class="sxs-lookup"><span data-stu-id="7a218-152">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="7a218-153">Není vyžadováno zákonem.</span><span class="sxs-lookup"><span data-stu-id="7a218-153">Not legally required.</span></span>  |
| <span data-ttu-id="7a218-154">**Nahrazeno jinou funkcí?**</span><span class="sxs-lookup"><span data-stu-id="7a218-154">**Replaced by another feature?**</span></span>   | <span data-ttu-id="7a218-155">Ano (formát aplikace Excel pro standardní soubor auditu s přiznáním k DPH – JPK_VDEK)</span><span class="sxs-lookup"><span data-stu-id="7a218-155">Yes (Excel format for Standard Audit File with VAT declaration - JPK_VDEK)</span></span> |
| <span data-ttu-id="7a218-156">**Ovlivněné oblasti produktu**</span><span class="sxs-lookup"><span data-stu-id="7a218-156">**Product areas affected**</span></span>         | <span data-ttu-id="7a218-157">Přihláška</span><span class="sxs-lookup"><span data-stu-id="7a218-157">Application</span></span> |
| <span data-ttu-id="7a218-158">**Možnost nasazení**</span><span class="sxs-lookup"><span data-stu-id="7a218-158">**Deployment option**</span></span>              | <span data-ttu-id="7a218-159">Vše</span><span class="sxs-lookup"><span data-stu-id="7a218-159">All</span></span> |
| <span data-ttu-id="7a218-160">**Stav**</span><span class="sxs-lookup"><span data-stu-id="7a218-160">**Status**</span></span>                         | <span data-ttu-id="7a218-161">Zastaralé: Od 1. července 2021 plánujeme již dále nepodporovat sestavy SSRS: **registr DPH na výstupu, registr DPH na vstupu, souhrnný registr DPH v EU – odkaz na funkci PL-00014**.</span><span class="sxs-lookup"><span data-stu-id="7a218-161">Deprecated: By July 1, 2021, we plan to no longer support the SSRS reports: **Sales VAT register, Purchase VAT register, EU summary VAT register – Feature reference PL-00014**.</span></span> <span data-ttu-id="7a218-162">Namísto toho bude zaveden příklad formátu aplikace Excel pro standardní soubor auditu s přiznáním k DPH (JPK_VDEK).</span><span class="sxs-lookup"><span data-stu-id="7a218-162">Excel format example for Standard Audit File with VAT declaration (JPK_VDEK) will be introduced instead.</span></span> |

## <a name="features-removed-or-deprecated-in-the-finance-10011-release"></a><span data-ttu-id="7a218-163">Odebrané nebo zastaralé funkce v aplikaci Finance verze 10.0.11</span><span class="sxs-lookup"><span data-stu-id="7a218-163">Features removed or deprecated in the Finance 10.0.11 release</span></span>

### <a name="norwegian-standard-main-accounts"></a><span data-ttu-id="7a218-164">Standardní hlavní účty pro Norsko</span><span class="sxs-lookup"><span data-stu-id="7a218-164">Norwegian Standard main accounts</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="7a218-165">**Důvod pro zrušení/odstranění**</span><span class="sxs-lookup"><span data-stu-id="7a218-165">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="7a218-166">Změnit návrh</span><span class="sxs-lookup"><span data-stu-id="7a218-166">Redesign</span></span>  |
| <span data-ttu-id="7a218-167">**Nahrazeno jinou funkcí?**</span><span class="sxs-lookup"><span data-stu-id="7a218-167">**Replaced by another feature?**</span></span>   | <span data-ttu-id="7a218-168">Ano (nahrazeno parametry specifickými pro aplikaci formátu ER)</span><span class="sxs-lookup"><span data-stu-id="7a218-168">Yes (Replaced with ER format application-specific parameters)</span></span> |
| <span data-ttu-id="7a218-169">**Ovlivněné oblasti produktu**</span><span class="sxs-lookup"><span data-stu-id="7a218-169">**Product areas affected**</span></span>         | <span data-ttu-id="7a218-170">Přihláška</span><span class="sxs-lookup"><span data-stu-id="7a218-170">Application</span></span> |
| <span data-ttu-id="7a218-171">**Možnost nasazení**</span><span class="sxs-lookup"><span data-stu-id="7a218-171">**Deployment option**</span></span>              | <span data-ttu-id="7a218-172">Vše</span><span class="sxs-lookup"><span data-stu-id="7a218-172">All</span></span> |
| <span data-ttu-id="7a218-173">**Stav**</span><span class="sxs-lookup"><span data-stu-id="7a218-173">**Status**</span></span>                         | <span data-ttu-id="7a218-174">Zastaralé: od 1. dubna 2021 nebude možné podporovat funkce související se standardními hlavními účty: referenční pole, související tabulka, entita dat.</span><span class="sxs-lookup"><span data-stu-id="7a218-174">Deprecated: By April 1, 2021, we plan to no longer support functionality related to Standard main accounts: Reference field, related table, data entity.</span></span> |

## <a name="features-removed-or-deprecated-in-the-finance-1007-release"></a><span data-ttu-id="7a218-175">Odebrané nebo zastaralé funkce v aplikaci Finance verze 10.0.7</span><span class="sxs-lookup"><span data-stu-id="7a218-175">Features removed or deprecated in the Finance 10.0.7 release</span></span>

### <a name="workflow-request-change-dialog-box-no-longer-includes-user-selection-drop-down-list"></a><span data-ttu-id="7a218-176">Dialogové okno pro změnu požadavku workflowu již neobsahuje rozevírací seznam pro výběr uživatele.</span><span class="sxs-lookup"><span data-stu-id="7a218-176">Workflow request change dialog box no longer includes user selection drop-down list</span></span>
|   |  |
|------------|--------------------|
| <span data-ttu-id="7a218-177">**Důvod pro zrušení/odstranění**</span><span class="sxs-lookup"><span data-stu-id="7a218-177">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="7a218-178">Změněno na funkci s výběrem skupiny účtů.</span><span class="sxs-lookup"><span data-stu-id="7a218-178">Changed to the feature with account groups selection.</span></span>  |
| <span data-ttu-id="7a218-179">**Nahrazeno jinou funkcí?**</span><span class="sxs-lookup"><span data-stu-id="7a218-179">**Replaced by another feature?**</span></span>   | <span data-ttu-id="7a218-180">Ano</span><span class="sxs-lookup"><span data-stu-id="7a218-180">Yes</span></span> |
| <span data-ttu-id="7a218-181">**Ovlivněné oblasti produktu**</span><span class="sxs-lookup"><span data-stu-id="7a218-181">**Product areas affected**</span></span>         | <span data-ttu-id="7a218-182">Workflow</span><span class="sxs-lookup"><span data-stu-id="7a218-182">Workflow</span></span> |
| <span data-ttu-id="7a218-183">**Možnost nasazení**</span><span class="sxs-lookup"><span data-stu-id="7a218-183">**Deployment option**</span></span>              | <span data-ttu-id="7a218-184">Vše</span><span class="sxs-lookup"><span data-stu-id="7a218-184">All</span></span> |
| <span data-ttu-id="7a218-185">**Stav**</span><span class="sxs-lookup"><span data-stu-id="7a218-185">**Status**</span></span>                         | <span data-ttu-id="7a218-186">Zastaralé: do 1. prosince 2020 plánujeme nadále nepodporovat nastavení čínských typů dokladů bez výběru skupin účtů.</span><span class="sxs-lookup"><span data-stu-id="7a218-186">Deprecated: By December 1, 2020, we plan to no longer support Chinese voucher types setup without Account groups selection.</span></span> <span data-ttu-id="7a218-187">Další informace o novém designu najdete v části [Co je nového ve verzi 10.0.7](whats-new-changed-10-0-7.md).</span><span class="sxs-lookup"><span data-stu-id="7a218-187">Find more details about the new design in [What's new in 10.0.7](whats-new-changed-10-0-7.md).</span></span> |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a><span data-ttu-id="7a218-188">Předchozí oznámení o odebraných nebo zastaralých funkcích</span><span class="sxs-lookup"><span data-stu-id="7a218-188">Previous announcements about removed or deprecated features</span></span>
<span data-ttu-id="7a218-189">Další informace o funkcích, které byly v předchozích verzích odebrány nebo zastaraly, naleznete v tématu [Odebrané nebo zastaralé funkce v předchozích verzích](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).</span><span class="sxs-lookup"><span data-stu-id="7a218-189">To learn more about features that have been removed or deprecated in previous releases, see [Removed or deprecated features in previous releases](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).</span></span>
