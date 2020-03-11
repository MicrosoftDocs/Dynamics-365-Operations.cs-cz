---
title: Podpora duální měny pro daň
description: Toto téma vysvětluje, jak rozšířit funkci účtování duálních měn v daňové doméně a dopad na výpočet a zaúčtování daně
author: EricWang
manager: Ann Beebe
ms.date: 12/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2020-01-14
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: c9318f518135bf7aa545cdb5ddd2e68c54a6d211
ms.sourcegitcommit: bcc8cba8905ed51797d36e1712d7360452cfc5c5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/27/2020
ms.locfileid: "3090557"
---
# <a name="dual-currency-support-for-sales-tax"></a><span data-ttu-id="30c24-103">Podpora duální měny pro DPH</span><span class="sxs-lookup"><span data-stu-id="30c24-103">Dual currency support for sales tax</span></span>
[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="30c24-104">Toto téma vysvětluje, jak rozšířit funkci účtování duálních měn pro DPH a dopad na výpočet, zaúčtování a vypořádání DPH.</span><span class="sxs-lookup"><span data-stu-id="30c24-104">This topic explains how to extend dual currency accounting for sales taxes and the impact for sales tax calculations, posting and settlements.</span></span>

<span data-ttu-id="30c24-105">Funkce duální měny pro Dynamics 365 Finance byla představena ve verzi 8.1 (říjen 2018).</span><span class="sxs-lookup"><span data-stu-id="30c24-105">The Dual currency feature for Dynamics 365 Finance was introduced in version 8.1 (October 2018).</span></span> <span data-ttu-id="30c24-106">Mění, jakým způsobem se počítají účtovací položky v měně vykazování.</span><span class="sxs-lookup"><span data-stu-id="30c24-106">It changes the way that accounting entries in the reporting currency are calculated.</span></span>

<span data-ttu-id="30c24-107">V předchozích verzích byly transakce převedeny na měnu vykazování v následujícím pořadí:</span><span class="sxs-lookup"><span data-stu-id="30c24-107">In earlier versions, transactions were converted to the reporting currency in the following sequence:</span></span> 

<span data-ttu-id="30c24-108">Celková transakce byla vypočtena v měně transakce > částka transakce byla převedena na zúčtovací měnu > částka zúčtovací měny byla převedena na měnu vykazování</span><span class="sxs-lookup"><span data-stu-id="30c24-108">Transaction total was calculated in the transaction currency > Transaction amount was converted to the accounting currency > Accounting currency amount was converted to the Reporting currency</span></span>

<span data-ttu-id="30c24-109">Po povolení duální funkce měny byly transakce převedeny na měnu vykazování v následujícím pořadí:</span><span class="sxs-lookup"><span data-stu-id="30c24-109">After enabling the dual currency feature, transactions were converted to the reporting currency in the following sequence:</span></span>

- <span data-ttu-id="30c24-110">Částka v měně transakce > Částka v měně pro vykazování</span><span class="sxs-lookup"><span data-stu-id="30c24-110">Transaction currency amount > Reporting currency amount</span></span>

<span data-ttu-id="30c24-111">Další informace o duální měně naleznete v [Duální měně](dual-currency.md).</span><span class="sxs-lookup"><span data-stu-id="30c24-111">For more information about dual currency, please refer to [Dual currency](dual-currency.md).</span></span>

<span data-ttu-id="30c24-112">V důsledku podpory duálních měn jsou v modulu Správa funkcí k dispozici dvě nové funkce:</span><span class="sxs-lookup"><span data-stu-id="30c24-112">As a consequence of support for dual currencies, two new features are available in feature management:</span></span> 

- <span data-ttu-id="30c24-113">Převod DPH (zavedeno ve verzi 10.0.9)</span><span class="sxs-lookup"><span data-stu-id="30c24-113">Sales tax conversion (Release in version 10.0.9)</span></span>
- <span data-ttu-id="30c24-114">Automatický zůstatek pro vyrovnání daně v měně vykazování (zavedeno ve verzi 10.0.11)</span><span class="sxs-lookup"><span data-stu-id="30c24-114">Tax settlement auto balance in reporting currency (Release in version 10.0.11)</span></span>

<span data-ttu-id="30c24-115">Podpora dvojí měny pro DPH zajišťuje, že daně budou vypočítány přesně v měně daně a že zůstatek vyrovnání DPH je vypočítán přesně v zúčtovací měně i v měně vykazování.</span><span class="sxs-lookup"><span data-stu-id="30c24-115">Dual currency support for sales taxes ensures that taxes are calculated accurately in the tax currency, and that the sales tax settlement balance is calculated accurately in both the accounting currency and reporting currency.</span></span> 

<span data-ttu-id="30c24-116">Nové funkce jsou aktuálně zpřístupněny pro soukromé náhledy zákazníků.</span><span class="sxs-lookup"><span data-stu-id="30c24-116">The new features are currently enabled for private preview customers.</span></span> <span data-ttu-id="30c24-117">Chcete-li tyto funkce povolit, vyvolejte požadavek na službu prostřednictvím odpovídajících kanálů společnosti Microsoft.</span><span class="sxs-lookup"><span data-stu-id="30c24-117">To enable the features, raise a service request through corresponding channels to Microsoft.</span></span>

## <a name="sales-tax-conversion"></a><span data-ttu-id="30c24-118">Převod DPH</span><span class="sxs-lookup"><span data-stu-id="30c24-118">Sales tax conversion</span></span>

<span data-ttu-id="30c24-119">**Parametr převodu DPH** poskytuje dvě možnosti převodu částky daně z transakční měny na daňovou měnu.</span><span class="sxs-lookup"><span data-stu-id="30c24-119">The **Sales tax conversion** parameter provides two options to convert tax amount from transaction currency to tax currency.</span></span> 

- <span data-ttu-id="30c24-120">Zúčtovací měna: cesta bude "Částka v měně transakce > Částka v zúčtovací měně > Částka v měně daně".</span><span class="sxs-lookup"><span data-stu-id="30c24-120">Accounting currency: The path will be "Amount in transaction currency > Amount in accounting currency > Amount in tax currency".</span></span> <span data-ttu-id="30c24-121">Typ směnného kurzu zúčtovací měny (konfigurován v nastavení hlavní knihy) bude použit pro převod měny.</span><span class="sxs-lookup"><span data-stu-id="30c24-121">The accounting currency exhange rate type (configured in Ledger setup) will be used for the currency conversion.</span></span>
- <span data-ttu-id="30c24-122">Měna vykazování: cesta bude "Částka v měně transakce > Částka v měně vykazování > Částka v měně daně".</span><span class="sxs-lookup"><span data-stu-id="30c24-122">Reporting currency: The path will be "Amount in transaction currency > Amount in reporting currency > Amount in tax currency".</span></span> <span data-ttu-id="30c24-123">Typ směnného kurzu měny vykazování (konfigurován v nastavení hlavní knihy) bude použit pro převod měny.</span><span class="sxs-lookup"><span data-stu-id="30c24-123">The reporting currency exhange rate type (configured in Ledger setup) will be used for the currency conversion.</span></span>

### <a name="example"></a><span data-ttu-id="30c24-124">Příklad</span><span class="sxs-lookup"><span data-stu-id="30c24-124">Example</span></span>

<span data-ttu-id="30c24-125">Jedná se o jednoduchý příklad, který demonstruje tyto funkce:</span><span class="sxs-lookup"><span data-stu-id="30c24-125">A simple example to demonstrate this functionality is:</span></span>

<span data-ttu-id="30c24-126">Nastavení měny pro hlavní knihu a daň</span><span class="sxs-lookup"><span data-stu-id="30c24-126">Currency setup for ledger and tax</span></span>

| <span data-ttu-id="30c24-127">Měna transakce</span><span class="sxs-lookup"><span data-stu-id="30c24-127">Transaction currency</span></span> | <span data-ttu-id="30c24-128">Zúčtovací měna</span><span class="sxs-lookup"><span data-stu-id="30c24-128">Accounting currency</span></span> | <span data-ttu-id="30c24-129">Měna pro vykazování</span><span class="sxs-lookup"><span data-stu-id="30c24-129">Reporting currency</span></span> | <span data-ttu-id="30c24-130">Měna daně</span><span class="sxs-lookup"><span data-stu-id="30c24-130">Tax currency</span></span> |
| -------------------- | ------------------- | ------------------ | ------------ |
| <span data-ttu-id="30c24-131">EUR</span><span class="sxs-lookup"><span data-stu-id="30c24-131">EUR</span></span>                  | <span data-ttu-id="30c24-132">USD</span><span class="sxs-lookup"><span data-stu-id="30c24-132">USD</span></span>                 | <span data-ttu-id="30c24-133">GBP</span><span class="sxs-lookup"><span data-stu-id="30c24-133">GBP</span></span>                | <span data-ttu-id="30c24-134">GBP</span><span class="sxs-lookup"><span data-stu-id="30c24-134">GBP</span></span>          |

<span data-ttu-id="30c24-135">Směnný kurz</span><span class="sxs-lookup"><span data-stu-id="30c24-135">Exchange rate</span></span>

| <span data-ttu-id="30c24-136">Z měny</span><span class="sxs-lookup"><span data-stu-id="30c24-136">From currency</span></span> | <span data-ttu-id="30c24-137">Na měnu</span><span class="sxs-lookup"><span data-stu-id="30c24-137">To currency</span></span> | <span data-ttu-id="30c24-138">Koeficient</span><span class="sxs-lookup"><span data-stu-id="30c24-138">Factor</span></span> | <span data-ttu-id="30c24-139">Směnný kurz</span><span class="sxs-lookup"><span data-stu-id="30c24-139">Exchange rate</span></span> |
| ------------- | ----------- | ------ | ------------- |
| <span data-ttu-id="30c24-140">EUR</span><span class="sxs-lookup"><span data-stu-id="30c24-140">EUR</span></span>           | <span data-ttu-id="30c24-141">USD</span><span class="sxs-lookup"><span data-stu-id="30c24-141">USD</span></span>         | <span data-ttu-id="30c24-142">1</span><span class="sxs-lookup"><span data-stu-id="30c24-142">1</span></span>      | <span data-ttu-id="30c24-143">1.11</span><span class="sxs-lookup"><span data-stu-id="30c24-143">1.11</span></span>          |
| <span data-ttu-id="30c24-144">EUR</span><span class="sxs-lookup"><span data-stu-id="30c24-144">EUR</span></span>           | <span data-ttu-id="30c24-145">GBP</span><span class="sxs-lookup"><span data-stu-id="30c24-145">GBP</span></span>         | <span data-ttu-id="30c24-146">1</span><span class="sxs-lookup"><span data-stu-id="30c24-146">1</span></span>      | <span data-ttu-id="30c24-147">0.83</span><span class="sxs-lookup"><span data-stu-id="30c24-147">0.83</span></span>          |
| <span data-ttu-id="30c24-148">USD</span><span class="sxs-lookup"><span data-stu-id="30c24-148">USD</span></span>           | <span data-ttu-id="30c24-149">GBP</span><span class="sxs-lookup"><span data-stu-id="30c24-149">GBP</span></span>         | <span data-ttu-id="30c24-150">1</span><span class="sxs-lookup"><span data-stu-id="30c24-150">1</span></span>      | <span data-ttu-id="30c24-151">0.75</span><span class="sxs-lookup"><span data-stu-id="30c24-151">0.75</span></span>          |

<span data-ttu-id="30c24-152">Výpočet částky daně v různých možnostech parametrů</span><span class="sxs-lookup"><span data-stu-id="30c24-152">Tax amount calculation in different parameter options</span></span>

<span data-ttu-id="30c24-153">Částka daně = 100 EUR</span><span class="sxs-lookup"><span data-stu-id="30c24-153">Tax amount = 100 EUR</span></span>

| <span data-ttu-id="30c24-154">Parametry převodu DPH</span><span class="sxs-lookup"><span data-stu-id="30c24-154">Sales tax conversion parameters</span></span> | <span data-ttu-id="30c24-155">Měna transakce (EUR)</span><span class="sxs-lookup"><span data-stu-id="30c24-155">Transaction currency (EUR)</span></span> | <span data-ttu-id="30c24-156">Zúčtovací měna (USD)</span><span class="sxs-lookup"><span data-stu-id="30c24-156">Accounting currency (USD)</span></span> | <span data-ttu-id="30c24-157">Měna vykazování (GBP)</span><span class="sxs-lookup"><span data-stu-id="30c24-157">Reporting currency (GBP)</span></span> | <span data-ttu-id="30c24-158">Měna daně (GBP)</span><span class="sxs-lookup"><span data-stu-id="30c24-158">Tax currency (GBP)</span></span> |
| ------------------------------- | -------------------------- | ------------------------- | ------------------------ | ------------------ |
| <span data-ttu-id="30c24-159">Zúčtovací měna</span><span class="sxs-lookup"><span data-stu-id="30c24-159">Accounting currency</span></span>             | <span data-ttu-id="30c24-160">100</span><span class="sxs-lookup"><span data-stu-id="30c24-160">100</span></span>                        | <span data-ttu-id="30c24-161">111</span><span class="sxs-lookup"><span data-stu-id="30c24-161">111</span></span>                       | <span data-ttu-id="30c24-162">83</span><span class="sxs-lookup"><span data-stu-id="30c24-162">83</span></span>                       | <span data-ttu-id="30c24-163">**83.25**</span><span class="sxs-lookup"><span data-stu-id="30c24-163">**83.25**</span></span>          |
| <span data-ttu-id="30c24-164">Měna pro vykazování</span><span class="sxs-lookup"><span data-stu-id="30c24-164">Reporting currency</span></span>              | <span data-ttu-id="30c24-165">100</span><span class="sxs-lookup"><span data-stu-id="30c24-165">100</span></span>                        | <span data-ttu-id="30c24-166">111</span><span class="sxs-lookup"><span data-stu-id="30c24-166">111</span></span>                       | <span data-ttu-id="30c24-167">83</span><span class="sxs-lookup"><span data-stu-id="30c24-167">83</span></span>                       | <span data-ttu-id="30c24-168">**83**</span><span class="sxs-lookup"><span data-stu-id="30c24-168">**83**</span></span>             |

<span data-ttu-id="30c24-169">Tento parametr lze nakonfigurovat podle potřeby finančního úřadu na základě kompatibility.</span><span class="sxs-lookup"><span data-stu-id="30c24-169">This parameter can be configured based on the compliance need from tax authority.</span></span>


### <a name="upgrade-consideration"></a><span data-ttu-id="30c24-170">Předpoklady upgradu</span><span class="sxs-lookup"><span data-stu-id="30c24-170">Upgrade Consideration</span></span>

<span data-ttu-id="30c24-171">Tato funkce bude použita pouze pro nové transakce.</span><span class="sxs-lookup"><span data-stu-id="30c24-171">This feature will only apply for new transactions.</span></span> <span data-ttu-id="30c24-172">V případě daňové transakce, která je již uložena v tabulce TAXTRANS, ale ještě nebyla vyrovnána, systém nepřepočítá částku daně v daňové měně, protože směnný kurz v určitém časovém bodu zaúčtování daně již chybí.</span><span class="sxs-lookup"><span data-stu-id="30c24-172">For tax transaction already saved in TAXTRANS table but not settled yet, system will not recalculate tax amount in tax currency because the exchange rate at time point of posting tax is already missing.</span></span>

<span data-ttu-id="30c24-173">Chcete-li zabránit předchozímu scénáři, doporučujeme změnit hodnotu tohoto parametru v novém (čistém) období vyrovnání daně, které neobsahuje žádné transakce nevyrovnané daně.</span><span class="sxs-lookup"><span data-stu-id="30c24-173">To prevent preceding scenario, we recommend changing this parameter value in a new (clean) tax settlement period that doesn't contain any unsettled tax transactions.</span></span> <span data-ttu-id="30c24-174">Chcete-li tuto hodnotu změnit uprostřed období daňového vyrovnání, spusťte před změnou hodnoty tohoto parametru program "Vyrovnat a zaúčtovat DPH" pro období aktuálního vyrovnání.</span><span class="sxs-lookup"><span data-stu-id="30c24-174">To change this value in the middle of a tax settlement period, please run "Settle and post sales tax" program for current tax settlement period before changing this parameter value.</span></span>


## <a name="track-reporting-currency-tax-amount"></a><span data-ttu-id="30c24-175">Sledovat částku daně v měně vykazování</span><span class="sxs-lookup"><span data-stu-id="30c24-175">Track reporting currency tax amount</span></span>

<span data-ttu-id="30c24-176">Do tabulek souvisejících s daní byla přidána tři nová pole pro sledování částek v měně vykazování.</span><span class="sxs-lookup"><span data-stu-id="30c24-176">Three new fields were added to tax-related tables to track amounts in the reporting currency.</span></span> <span data-ttu-id="30c24-177">Tato pole se nacházejí v tabulkách TAXUNCOMMITTED a TAXTRANS:</span><span class="sxs-lookup"><span data-stu-id="30c24-177">These fields are within the TAXUNCOMMITTED and TAXTRANS tables:</span></span>

- <span data-ttu-id="30c24-178">TaxAmountRep: částka daně v měně vykazování</span><span class="sxs-lookup"><span data-stu-id="30c24-178">TaxAmountRep: tax amount in reporting currency</span></span>
- <span data-ttu-id="30c24-179">TaxBaseAmountRep: částka základu v měně vykazování</span><span class="sxs-lookup"><span data-stu-id="30c24-179">TaxBaseAmountRep: base amount in reporting currency</span></span>
- <span data-ttu-id="30c24-180">TaxInCostPriceRep: neodečitatelná částka v měně vykazování</span><span class="sxs-lookup"><span data-stu-id="30c24-180">TaxInCostPriceRep: non-deductible amount in reporting currency</span></span>

<span data-ttu-id="30c24-181">U daně uložené pouze v tabulce TAXUNCOMMITTED, ale dosud nezaúčtované, systém přepočítá částku daně v měně vykazování v okamžiku zaúčtování a uloží do tabulky TAXTRANS.</span><span class="sxs-lookup"><span data-stu-id="30c24-181">For tax only saved in TAXUNCOMMITTED table but not posted yet, system will recalculate tax amount in reporting currency at the time of posting and save in TAXTRANS table.</span></span>

<span data-ttu-id="30c24-182">Tato verze nebude zahrnovat změny v sestavách a formulářích, které zobrazují částku daně v měně vykazování.</span><span class="sxs-lookup"><span data-stu-id="30c24-182">This release will not include changes to reports and forms that show the tax amount in the reporting currency.</span></span> <span data-ttu-id="30c24-183">Změny v sestavách a formulářích budou dodány v budoucí verzi.</span><span class="sxs-lookup"><span data-stu-id="30c24-183">Changes to reports and forms will be delivered in the future release.</span></span>



## <a name="tax-settlement-auto-balance-in-reporting-currency"></a><span data-ttu-id="30c24-184">Automatický zůstatek pro vyrovnání daně v měně vykazování</span><span class="sxs-lookup"><span data-stu-id="30c24-184">Tax settlement auto-balance in reporting currency</span></span>

<span data-ttu-id="30c24-185">Není-li vyrovnání daně v měně vykazování rovnoměrně vyrovnáno, jako například cesta převodu DPH je "zúčtovací měna" nebo změna směnného kurzu v jednom období vyrovnání daně, systém automaticky vygeneruje účetní položky k úpravě odchylky částky daně a k její kompenzaci na účet realizovaných zisků/ztrát, který je konfigurován v nastavení hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="30c24-185">If the tax settlement is not balanced in the reporting currency for certain reason such as the sales tax conversion path is "Accounting currency", or the exchange rate change in a single tax settlement period, thebn the system will automatically generate accounting entries to adjust the tax amount variance and offset it against realized exchange gain/loss account, which is configured in Ledger setup.</span></span>

<span data-ttu-id="30c24-186">Chcete-li předvést tuto funkci pomocí předchozího příkladu, Předpokládejme, že data v tabulce TAXTRANS v okamžiku zaúčtování jsou následující:</span><span class="sxs-lookup"><span data-stu-id="30c24-186">Using the the previous example to demonstrate this feature, suppose that the data in TAXTRANS table at the time of posting is as follows.</span></span>

| <span data-ttu-id="30c24-187">Parametry převodu DPH</span><span class="sxs-lookup"><span data-stu-id="30c24-187">Sales tax conversion parameters</span></span> | <span data-ttu-id="30c24-188">Měna transakce (EUR)</span><span class="sxs-lookup"><span data-stu-id="30c24-188">Transaction currency (EUR)</span></span> | <span data-ttu-id="30c24-189">Zúčtovací měna (USD)</span><span class="sxs-lookup"><span data-stu-id="30c24-189">Accounting currency (USD)</span></span> | <span data-ttu-id="30c24-190">Měna vykazování (GBP)</span><span class="sxs-lookup"><span data-stu-id="30c24-190">Reporting currency (GBP)</span></span> | <span data-ttu-id="30c24-191">Měna daně (GBP)</span><span class="sxs-lookup"><span data-stu-id="30c24-191">Tax currency (GBP)</span></span> |
| ------------------------------- | -------------------------- | ------------------------- | ------------------------ | ------------------ |
| <span data-ttu-id="30c24-192">Zúčtovací měna</span><span class="sxs-lookup"><span data-stu-id="30c24-192">Accounting currency</span></span>             | <span data-ttu-id="30c24-193">100</span><span class="sxs-lookup"><span data-stu-id="30c24-193">100</span></span>                        | <span data-ttu-id="30c24-194">111</span><span class="sxs-lookup"><span data-stu-id="30c24-194">111</span></span>                       | <span data-ttu-id="30c24-195">83</span><span class="sxs-lookup"><span data-stu-id="30c24-195">83</span></span>                       | <span data-ttu-id="30c24-196">**83.25**</span><span class="sxs-lookup"><span data-stu-id="30c24-196">**83.25**</span></span>          |
| <span data-ttu-id="30c24-197">Měna pro vykazování</span><span class="sxs-lookup"><span data-stu-id="30c24-197">Reporting currency</span></span>              | <span data-ttu-id="30c24-198">100</span><span class="sxs-lookup"><span data-stu-id="30c24-198">100</span></span>                        | <span data-ttu-id="30c24-199">111</span><span class="sxs-lookup"><span data-stu-id="30c24-199">111</span></span>                       | <span data-ttu-id="30c24-200">83</span><span class="sxs-lookup"><span data-stu-id="30c24-200">83</span></span>                       | <span data-ttu-id="30c24-201">**83**</span><span class="sxs-lookup"><span data-stu-id="30c24-201">**83**</span></span>             |

<span data-ttu-id="30c24-202">Při spuštění programu vyrovnání DPH na konci měsíce bude účetní položka vypadat takto:.</span><span class="sxs-lookup"><span data-stu-id="30c24-202">When you run the sales tax settlement program at month-end, the accounting entry will be as follows:.</span></span>
#### <a name="scenario-sales-tax-conversion--accounting-currency"></a><span data-ttu-id="30c24-203">Scénář: převod DPH = "zúčtovací měna"</span><span class="sxs-lookup"><span data-stu-id="30c24-203">Scenario: sales tax conversion = "Accounting currency"</span></span>

| <span data-ttu-id="30c24-204">Hlavní účet</span><span class="sxs-lookup"><span data-stu-id="30c24-204">Main account</span></span>           | <span data-ttu-id="30c24-205">Měna transakce (GBP)</span><span class="sxs-lookup"><span data-stu-id="30c24-205">Transaction currency (GBP)</span></span> | <span data-ttu-id="30c24-206">Zúčtovací měna (USD)</span><span class="sxs-lookup"><span data-stu-id="30c24-206">Accounting currency (USD)</span></span> | <span data-ttu-id="30c24-207">Měna vykazování (GBP)</span><span class="sxs-lookup"><span data-stu-id="30c24-207">Reporting currency (GBP)</span></span> |
| ---------------------- | -------------------------- | ------------------------- | ------------------------ |
| <span data-ttu-id="30c24-208">Závazky / pohledávky daně</span><span class="sxs-lookup"><span data-stu-id="30c24-208">Tax Payable/Receivable</span></span> | <span data-ttu-id="30c24-209">-83,25</span><span class="sxs-lookup"><span data-stu-id="30c24-209">-83.25</span></span>                     | <span data-ttu-id="30c24-210">-111</span><span class="sxs-lookup"><span data-stu-id="30c24-210">-111</span></span>                      | <span data-ttu-id="30c24-211">-83,25</span><span class="sxs-lookup"><span data-stu-id="30c24-211">-83.25</span></span>                   |
| <span data-ttu-id="30c24-212">Vyrovnání daně</span><span class="sxs-lookup"><span data-stu-id="30c24-212">Tax Settlement</span></span>         | <span data-ttu-id="30c24-213">83.25</span><span class="sxs-lookup"><span data-stu-id="30c24-213">83.25</span></span>                      | <span data-ttu-id="30c24-214">111</span><span class="sxs-lookup"><span data-stu-id="30c24-214">111</span></span>                       | <span data-ttu-id="30c24-215">83.25</span><span class="sxs-lookup"><span data-stu-id="30c24-215">83.25</span></span>                    |
| <span data-ttu-id="30c24-216">Realizovaný zisk/ztráta</span><span class="sxs-lookup"><span data-stu-id="30c24-216">Realized Gain/Loss</span></span>     | <span data-ttu-id="30c24-217">0</span><span class="sxs-lookup"><span data-stu-id="30c24-217">0</span></span>                          | <span data-ttu-id="30c24-218">0</span><span class="sxs-lookup"><span data-stu-id="30c24-218">0</span></span>                         | <span data-ttu-id="30c24-219">-0,25</span><span class="sxs-lookup"><span data-stu-id="30c24-219">-0.25</span></span>                    |
| <span data-ttu-id="30c24-220">Závazky / pohledávky daně</span><span class="sxs-lookup"><span data-stu-id="30c24-220">Tax Payable/Receivable</span></span> | <span data-ttu-id="30c24-221">0</span><span class="sxs-lookup"><span data-stu-id="30c24-221">0</span></span>                          | <span data-ttu-id="30c24-222">0</span><span class="sxs-lookup"><span data-stu-id="30c24-222">0</span></span>                         | <span data-ttu-id="30c24-223">0.25</span><span class="sxs-lookup"><span data-stu-id="30c24-223">0.25</span></span>                     |

#### <a name="scenario-sales-tax-conversion--reporting-currency"></a><span data-ttu-id="30c24-224">Scénář: převod DPH = "měna vykazování"</span><span class="sxs-lookup"><span data-stu-id="30c24-224">Scenario: sales tax conversion = "Reporting currency"</span></span>


| <span data-ttu-id="30c24-225">Hlavní účet</span><span class="sxs-lookup"><span data-stu-id="30c24-225">Main account</span></span>           | <span data-ttu-id="30c24-226">Měna transakce (GBP)</span><span class="sxs-lookup"><span data-stu-id="30c24-226">Transaction currency (GBP)</span></span> | <span data-ttu-id="30c24-227">Zúčtovací měna (USD)</span><span class="sxs-lookup"><span data-stu-id="30c24-227">Accounting currency (USD)</span></span> | <span data-ttu-id="30c24-228">Měna vykazování (GBP)</span><span class="sxs-lookup"><span data-stu-id="30c24-228">Reporting currency (GBP)</span></span> |
| ---------------------- | -------------------------- | ------------------------- | ------------------------ |
| <span data-ttu-id="30c24-229">Závazky / pohledávky daně</span><span class="sxs-lookup"><span data-stu-id="30c24-229">Tax Payable/Receivable</span></span> | <span data-ttu-id="30c24-230">-83</span><span class="sxs-lookup"><span data-stu-id="30c24-230">-83</span></span>                        | <span data-ttu-id="30c24-231">-110,67</span><span class="sxs-lookup"><span data-stu-id="30c24-231">-110.67</span></span>                   | <span data-ttu-id="30c24-232">-83</span><span class="sxs-lookup"><span data-stu-id="30c24-232">-83</span></span>                      |
| <span data-ttu-id="30c24-233">Vyrovnání daně</span><span class="sxs-lookup"><span data-stu-id="30c24-233">Tax Settlement</span></span>         | <span data-ttu-id="30c24-234">83</span><span class="sxs-lookup"><span data-stu-id="30c24-234">83</span></span>                         | <span data-ttu-id="30c24-235">110.67</span><span class="sxs-lookup"><span data-stu-id="30c24-235">110.67</span></span>                    | <span data-ttu-id="30c24-236">83</span><span class="sxs-lookup"><span data-stu-id="30c24-236">83</span></span>                       |
| <span data-ttu-id="30c24-237">Realizovaný zisk/ztráta</span><span class="sxs-lookup"><span data-stu-id="30c24-237">Realized Gain/Loss</span></span>     | <span data-ttu-id="30c24-238">0</span><span class="sxs-lookup"><span data-stu-id="30c24-238">0</span></span>                          | <span data-ttu-id="30c24-239">0.33</span><span class="sxs-lookup"><span data-stu-id="30c24-239">0.33</span></span>                      | <span data-ttu-id="30c24-240">0</span><span class="sxs-lookup"><span data-stu-id="30c24-240">0</span></span>                        |
| <span data-ttu-id="30c24-241">Závazky / pohledávky daně</span><span class="sxs-lookup"><span data-stu-id="30c24-241">Tax Payable/Receivable</span></span> | <span data-ttu-id="30c24-242">0</span><span class="sxs-lookup"><span data-stu-id="30c24-242">0</span></span>                          | <span data-ttu-id="30c24-243">-0,33</span><span class="sxs-lookup"><span data-stu-id="30c24-243">-0.33</span></span>                     | <span data-ttu-id="30c24-244">0</span><span class="sxs-lookup"><span data-stu-id="30c24-244">0</span></span>                        |



<span data-ttu-id="30c24-245">Další informace naleznete v následujících tématech:</span><span class="sxs-lookup"><span data-stu-id="30c24-245">For more information, see the following topics:</span></span>

- [<span data-ttu-id="30c24-246">Duální měna</span><span class="sxs-lookup"><span data-stu-id="30c24-246">Dual currency</span></span>](dual-currency.md)
- [<span data-ttu-id="30c24-247">Přehled DPH</span><span class="sxs-lookup"><span data-stu-id="30c24-247">Sales tax overview</span></span>](indirect-taxes-overview.md)

