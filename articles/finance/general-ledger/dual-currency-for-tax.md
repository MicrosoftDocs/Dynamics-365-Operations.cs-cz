---
title: Podpora duální měny pro daň
description: Toto téma vysvětluje, jak rozšířit funkci účtování duálních měn v daňové doméně a dopad na výpočet a zaúčtování daně
author: EricWang
manager: Ann Beebe
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2020-01-14
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 2e3e7ff93ca3c6a2266ba0f33c8eac7ceade0d4d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4978586"
---
# <a name="dual-currency-support-for-sales-tax"></a><span data-ttu-id="88345-103">Podpora duální měny pro DPH</span><span class="sxs-lookup"><span data-stu-id="88345-103">Dual currency support for sales tax</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="88345-104">Toto téma vysvětluje, jak rozšířit funkci účtování duálních měn pro DPH a dopad na výpočet, zaúčtování a vypořádání DPH.</span><span class="sxs-lookup"><span data-stu-id="88345-104">This topic explains how to extend dual currency accounting for sales taxes and the impact for sales tax calculations, posting and settlements.</span></span>

<span data-ttu-id="88345-105">Funkce duální měny pro Dynamics 365 Finance byla představena ve verzi 8.1 (říjen 2018).</span><span class="sxs-lookup"><span data-stu-id="88345-105">The Dual currency feature for Dynamics 365 Finance was introduced in version 8.1 (October 2018).</span></span> <span data-ttu-id="88345-106">Mění, jakým způsobem se počítají účtovací položky v měně vykazování.</span><span class="sxs-lookup"><span data-stu-id="88345-106">It changes the way that accounting entries in the reporting currency are calculated.</span></span>

<span data-ttu-id="88345-107">V předchozích verzích byly transakce převedeny na měnu vykazování v následujícím pořadí:</span><span class="sxs-lookup"><span data-stu-id="88345-107">In earlier versions, transactions were converted to the reporting currency in the following sequence:</span></span> 

- <span data-ttu-id="88345-108">Celková transakce byla vypočtena v měně transakce > částka transakce byla převedena na zúčtovací měnu > částka zúčtovací měny byla převedena na měnu vykazování</span><span class="sxs-lookup"><span data-stu-id="88345-108">Transaction total was calculated in the transaction currency > Transaction amount was converted to the accounting currency > Accounting currency amount was converted to the Reporting currency</span></span>

<span data-ttu-id="88345-109">Po povolení duální funkce měny byly transakce převedeny na měnu vykazování v následujícím pořadí:</span><span class="sxs-lookup"><span data-stu-id="88345-109">After enabling the dual currency feature, transactions were converted to the reporting currency in the following sequence:</span></span>

- <span data-ttu-id="88345-110">Částka v měně transakce > Částka v měně pro vykazování</span><span class="sxs-lookup"><span data-stu-id="88345-110">Transaction currency amount > Reporting currency amount</span></span>

<span data-ttu-id="88345-111">Další informace o duální měně naleznete v [Duální měně](dual-currency.md).</span><span class="sxs-lookup"><span data-stu-id="88345-111">For more information about dual currency, please refer to [Dual currency](dual-currency.md).</span></span>

<span data-ttu-id="88345-112">V důsledku podpory duálních měn jsou v modulu Správa funkcí k dispozici dvě nové funkce:</span><span class="sxs-lookup"><span data-stu-id="88345-112">As a consequence of support for dual currencies, two new features are available in feature management:</span></span> 

- <span data-ttu-id="88345-113">Převod DPH (novinka ve verzi 10.0.13)</span><span class="sxs-lookup"><span data-stu-id="88345-113">Sales tax conversion (new in version 10.0.13)</span></span>

<span data-ttu-id="88345-114">Podpora dvojí měny pro DPH zajišťuje, že daně budou vypočítány přesně v měně daně a že zůstatek vyrovnání DPH je vypočítán přesně v zúčtovací měně i v měně vykazování.</span><span class="sxs-lookup"><span data-stu-id="88345-114">Dual currency support for sales taxes ensures that taxes are calculated accurately in the tax currency, and that the sales tax settlement balance is calculated accurately in both the accounting currency and reporting currency.</span></span> 

## <a name="sales-tax-conversion"></a><span data-ttu-id="88345-115">Převod DPH</span><span class="sxs-lookup"><span data-stu-id="88345-115">Sales tax conversion</span></span>

<span data-ttu-id="88345-116">**Parametr převodu DPH** poskytuje dvě možnosti převodu částky daně z transakční měny na daňovou měnu.</span><span class="sxs-lookup"><span data-stu-id="88345-116">The **Sales tax conversion** parameter provides two options to convert tax amount from transaction currency to tax currency.</span></span> 

- <span data-ttu-id="88345-117">Zúčtovací měna: cesta bude "Částka v měně transakce > Částka v zúčtovací měně > Částka v měně daně".</span><span class="sxs-lookup"><span data-stu-id="88345-117">Accounting currency: The path will be "Amount in transaction currency > Amount in accounting currency > Amount in tax currency".</span></span> <span data-ttu-id="88345-118">Typ směnného kurzu zúčtovací měny (konfigurován v nastavení hlavní knihy) bude použit pro převod měny.</span><span class="sxs-lookup"><span data-stu-id="88345-118">The accounting currency exchange rate type (configured in Ledger setup) will be used for the currency conversion.</span></span>
- <span data-ttu-id="88345-119">Měna vykazování: cesta bude "Částka v měně transakce > Částka v měně vykazování > Částka v měně daně".</span><span class="sxs-lookup"><span data-stu-id="88345-119">Reporting currency: The path will be "Amount in transaction currency > Amount in reporting currency > Amount in tax currency".</span></span> <span data-ttu-id="88345-120">Typ směnného kurzu měny vykazování (konfigurován v nastavení hlavní knihy) bude použit pro převod měny.</span><span class="sxs-lookup"><span data-stu-id="88345-120">The reporting currency exchange rate type (configured in Ledger setup) will be used for the currency conversion.</span></span>

### <a name="example"></a><span data-ttu-id="88345-121">Příklad</span><span class="sxs-lookup"><span data-stu-id="88345-121">Example</span></span>

<span data-ttu-id="88345-122">Jedná se o jednoduchý příklad, který demonstruje tyto funkce:</span><span class="sxs-lookup"><span data-stu-id="88345-122">A simple example to demonstrate this functionality is:</span></span>

<span data-ttu-id="88345-123">Nastavení měny pro hlavní knihu a daň</span><span class="sxs-lookup"><span data-stu-id="88345-123">Currency setup for ledger and tax</span></span>

| <span data-ttu-id="88345-124">Měna transakce</span><span class="sxs-lookup"><span data-stu-id="88345-124">Transaction currency</span></span> | <span data-ttu-id="88345-125">Zúčtovací měna</span><span class="sxs-lookup"><span data-stu-id="88345-125">Accounting currency</span></span> | <span data-ttu-id="88345-126">Měna pro vykazování</span><span class="sxs-lookup"><span data-stu-id="88345-126">Reporting currency</span></span> | <span data-ttu-id="88345-127">Měna daně</span><span class="sxs-lookup"><span data-stu-id="88345-127">Tax currency</span></span> |
| -------------------- | ------------------- | ------------------ | ------------ |
| <span data-ttu-id="88345-128">EUR</span><span class="sxs-lookup"><span data-stu-id="88345-128">EUR</span></span>                  | <span data-ttu-id="88345-129">USD</span><span class="sxs-lookup"><span data-stu-id="88345-129">USD</span></span>                 | <span data-ttu-id="88345-130">GBP</span><span class="sxs-lookup"><span data-stu-id="88345-130">GBP</span></span>                | <span data-ttu-id="88345-131">GBP</span><span class="sxs-lookup"><span data-stu-id="88345-131">GBP</span></span>          |

<span data-ttu-id="88345-132">Směnný kurz</span><span class="sxs-lookup"><span data-stu-id="88345-132">Exchange rate</span></span>

| <span data-ttu-id="88345-133">Z měny</span><span class="sxs-lookup"><span data-stu-id="88345-133">From currency</span></span> | <span data-ttu-id="88345-134">Na měnu</span><span class="sxs-lookup"><span data-stu-id="88345-134">To currency</span></span> | <span data-ttu-id="88345-135">Koeficient</span><span class="sxs-lookup"><span data-stu-id="88345-135">Factor</span></span> | <span data-ttu-id="88345-136">Směnný kurz</span><span class="sxs-lookup"><span data-stu-id="88345-136">Exchange rate</span></span> |
| ------------- | ----------- | ------ | ------------- |
| <span data-ttu-id="88345-137">EUR</span><span class="sxs-lookup"><span data-stu-id="88345-137">EUR</span></span>           | <span data-ttu-id="88345-138">USD</span><span class="sxs-lookup"><span data-stu-id="88345-138">USD</span></span>         | <span data-ttu-id="88345-139">1</span><span class="sxs-lookup"><span data-stu-id="88345-139">1</span></span>      | <span data-ttu-id="88345-140">1.11</span><span class="sxs-lookup"><span data-stu-id="88345-140">1.11</span></span>          |
| <span data-ttu-id="88345-141">EUR</span><span class="sxs-lookup"><span data-stu-id="88345-141">EUR</span></span>           | <span data-ttu-id="88345-142">GBP</span><span class="sxs-lookup"><span data-stu-id="88345-142">GBP</span></span>         | <span data-ttu-id="88345-143">1</span><span class="sxs-lookup"><span data-stu-id="88345-143">1</span></span>      | <span data-ttu-id="88345-144">0.83</span><span class="sxs-lookup"><span data-stu-id="88345-144">0.83</span></span>          |
| <span data-ttu-id="88345-145">USD</span><span class="sxs-lookup"><span data-stu-id="88345-145">USD</span></span>           | <span data-ttu-id="88345-146">GBP</span><span class="sxs-lookup"><span data-stu-id="88345-146">GBP</span></span>         | <span data-ttu-id="88345-147">1</span><span class="sxs-lookup"><span data-stu-id="88345-147">1</span></span>      | <span data-ttu-id="88345-148">0.75</span><span class="sxs-lookup"><span data-stu-id="88345-148">0.75</span></span>          |

<span data-ttu-id="88345-149">Výpočet částky daně v různých možnostech parametrů</span><span class="sxs-lookup"><span data-stu-id="88345-149">Tax amount calculation in different parameter options</span></span>

<span data-ttu-id="88345-150">Částka daně = 100 EUR</span><span class="sxs-lookup"><span data-stu-id="88345-150">Tax amount = 100 EUR</span></span>

| <span data-ttu-id="88345-151">Parametry převodu DPH</span><span class="sxs-lookup"><span data-stu-id="88345-151">Sales tax conversion parameters</span></span> | <span data-ttu-id="88345-152">Měna transakce (EUR)</span><span class="sxs-lookup"><span data-stu-id="88345-152">Transaction currency (EUR)</span></span> | <span data-ttu-id="88345-153">Zúčtovací měna (USD)</span><span class="sxs-lookup"><span data-stu-id="88345-153">Accounting currency (USD)</span></span> | <span data-ttu-id="88345-154">Měna vykazování (GBP)</span><span class="sxs-lookup"><span data-stu-id="88345-154">Reporting currency (GBP)</span></span> | <span data-ttu-id="88345-155">Měna daně (GBP)</span><span class="sxs-lookup"><span data-stu-id="88345-155">Tax currency (GBP)</span></span> |
| ------------------------------- | -------------------------- | ------------------------- | ------------------------ | ------------------ |
| <span data-ttu-id="88345-156">Zúčtovací měna</span><span class="sxs-lookup"><span data-stu-id="88345-156">Accounting currency</span></span>             | <span data-ttu-id="88345-157">100</span><span class="sxs-lookup"><span data-stu-id="88345-157">100</span></span>                        | <span data-ttu-id="88345-158">111</span><span class="sxs-lookup"><span data-stu-id="88345-158">111</span></span>                       | <span data-ttu-id="88345-159">83</span><span class="sxs-lookup"><span data-stu-id="88345-159">83</span></span>                       | <span data-ttu-id="88345-160">**83.25**</span><span class="sxs-lookup"><span data-stu-id="88345-160">**83.25**</span></span>          |
| <span data-ttu-id="88345-161">Měna pro vykazování</span><span class="sxs-lookup"><span data-stu-id="88345-161">Reporting currency</span></span>              | <span data-ttu-id="88345-162">100</span><span class="sxs-lookup"><span data-stu-id="88345-162">100</span></span>                        | <span data-ttu-id="88345-163">111</span><span class="sxs-lookup"><span data-stu-id="88345-163">111</span></span>                       | <span data-ttu-id="88345-164">83</span><span class="sxs-lookup"><span data-stu-id="88345-164">83</span></span>                       | <span data-ttu-id="88345-165">**83**</span><span class="sxs-lookup"><span data-stu-id="88345-165">**83**</span></span>             |

<span data-ttu-id="88345-166">Tento parametr lze nakonfigurovat podle potřeby finančního úřadu na základě kompatibility.</span><span class="sxs-lookup"><span data-stu-id="88345-166">This parameter can be configured based on the compliance need from tax authority.</span></span>


### <a name="upgrade-consideration"></a><span data-ttu-id="88345-167">Předpoklady upgradu</span><span class="sxs-lookup"><span data-stu-id="88345-167">Upgrade Consideration</span></span>

<span data-ttu-id="88345-168">Tato funkce bude použita pouze pro nové transakce.</span><span class="sxs-lookup"><span data-stu-id="88345-168">This feature will only apply for new transactions.</span></span> <span data-ttu-id="88345-169">V případě daňové transakce, která je již uložena v tabulce TAXTRANS, ale ještě nebyla vyrovnána, systém nepřepočítá částku daně v daňové měně, protože směnný kurz v určitém časovém bodu zaúčtování daně již chybí.</span><span class="sxs-lookup"><span data-stu-id="88345-169">For tax transaction already saved in TAXTRANS table but not settled yet, system will not recalculate tax amount in tax currency because the exchange rate at time point of posting tax is already missing.</span></span>

<span data-ttu-id="88345-170">Chcete-li zabránit předchozímu scénáři, doporučujeme změnit hodnotu tohoto parametru v novém (čistém) období vyrovnání daně, které neobsahuje žádné transakce nevyrovnané daně.</span><span class="sxs-lookup"><span data-stu-id="88345-170">To prevent preceding scenario, we recommend changing this parameter value in a new (clean) tax settlement period that doesn't contain any unsettled tax transactions.</span></span> <span data-ttu-id="88345-171">Chcete-li tuto hodnotu změnit uprostřed období daňového vyrovnání, spusťte před změnou hodnoty tohoto parametru program "Vyrovnat a zaúčtovat DPH" pro období aktuálního vyrovnání.</span><span class="sxs-lookup"><span data-stu-id="88345-171">To change this value in the middle of a tax settlement period, please run "Settle and post sales tax" program for current tax settlement period before changing this parameter value.</span></span>


## <a name="track-reporting-currency-tax-amount"></a><span data-ttu-id="88345-172">Sledovat částku daně v měně vykazování</span><span class="sxs-lookup"><span data-stu-id="88345-172">Track reporting currency tax amount</span></span>

<span data-ttu-id="88345-173">Do tabulek souvisejících s daní byla přidána tři nová pole pro sledování částek v měně vykazování.</span><span class="sxs-lookup"><span data-stu-id="88345-173">Three new fields were added to tax-related tables to track amounts in the reporting currency.</span></span> <span data-ttu-id="88345-174">Tato pole se nacházejí v tabulkách TAXUNCOMMITTED a TAXTRANS:</span><span class="sxs-lookup"><span data-stu-id="88345-174">These fields are within the TAXUNCOMMITTED and TAXTRANS tables:</span></span>

- <span data-ttu-id="88345-175">TaxAmountRep: částka daně v měně vykazování</span><span class="sxs-lookup"><span data-stu-id="88345-175">TaxAmountRep: tax amount in reporting currency</span></span>
- <span data-ttu-id="88345-176">TaxBaseAmountRep: částka základu v měně vykazování</span><span class="sxs-lookup"><span data-stu-id="88345-176">TaxBaseAmountRep: base amount in reporting currency</span></span>
- <span data-ttu-id="88345-177">TaxInCostPriceRep: neodečitatelná částka v měně vykazování</span><span class="sxs-lookup"><span data-stu-id="88345-177">TaxInCostPriceRep: non-deductible amount in reporting currency</span></span>

<span data-ttu-id="88345-178">U daně uložené pouze v tabulce TAXUNCOMMITTED, ale dosud nezaúčtované, systém přepočítá částku daně v měně vykazování v okamžiku zaúčtování a uloží do tabulky TAXTRANS.</span><span class="sxs-lookup"><span data-stu-id="88345-178">For tax only saved in TAXUNCOMMITTED table but not posted yet, system will recalculate tax amount in reporting currency at the time of posting and save in TAXTRANS table.</span></span>

<span data-ttu-id="88345-179">Tato verze nebude zahrnovat změny v sestavách a formulářích, které zobrazují částku daně v měně vykazování.</span><span class="sxs-lookup"><span data-stu-id="88345-179">This release will not include changes to reports and forms that show the tax amount in the reporting currency.</span></span> <span data-ttu-id="88345-180">Změny v sestavách a formulářích budou dodány v budoucí verzi.</span><span class="sxs-lookup"><span data-stu-id="88345-180">Changes to reports and forms will be delivered in the future release.</span></span>



## <a name="tax-settlement-auto-balance-in-reporting-currency"></a><span data-ttu-id="88345-181">Automatický zůstatek pro vyrovnání daně v měně vykazování</span><span class="sxs-lookup"><span data-stu-id="88345-181">Tax settlement auto-balance in reporting currency</span></span>

<span data-ttu-id="88345-182">Není-li vyrovnání daně v měně vykazování rovnoměrně vyrovnáno, jako například cesta převodu DPH je „zúčtovací měna“ nebo změna směnného kurzu v jednom období vyrovnání daně, systém automaticky vygeneruje účetní položky k úpravě odchylky částky daně a k její kompenzaci na účet realizovaných zisků/ztrát, který je konfigurován v nastavení hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="88345-182">If the tax settlement is not balanced in the reporting currency for certain reason such as the sales tax conversion path is "Accounting currency", or the exchange rate change in a single tax settlement period, then the system will automatically generate accounting entries to adjust the tax amount variance and offset it against realized exchange gain/loss account, which is configured in Ledger setup.</span></span>

<span data-ttu-id="88345-183">Chcete-li předvést tuto funkci pomocí předchozího příkladu, Předpokládejme, že data v tabulce TAXTRANS v okamžiku zaúčtování jsou následující:</span><span class="sxs-lookup"><span data-stu-id="88345-183">Using the the previous example to demonstrate this feature, suppose that the data in TAXTRANS table at the time of posting is as follows.</span></span>

| <span data-ttu-id="88345-184">Parametry převodu DPH</span><span class="sxs-lookup"><span data-stu-id="88345-184">Sales tax conversion parameters</span></span> | <span data-ttu-id="88345-185">Měna transakce (EUR)</span><span class="sxs-lookup"><span data-stu-id="88345-185">Transaction currency (EUR)</span></span> | <span data-ttu-id="88345-186">Zúčtovací měna (USD)</span><span class="sxs-lookup"><span data-stu-id="88345-186">Accounting currency (USD)</span></span> | <span data-ttu-id="88345-187">Měna vykazování (GBP)</span><span class="sxs-lookup"><span data-stu-id="88345-187">Reporting currency (GBP)</span></span> | <span data-ttu-id="88345-188">Měna daně (GBP)</span><span class="sxs-lookup"><span data-stu-id="88345-188">Tax currency (GBP)</span></span> |
| ------------------------------- | -------------------------- | ------------------------- | ------------------------ | ------------------ |
| <span data-ttu-id="88345-189">Zúčtovací měna</span><span class="sxs-lookup"><span data-stu-id="88345-189">Accounting currency</span></span>             | <span data-ttu-id="88345-190">100</span><span class="sxs-lookup"><span data-stu-id="88345-190">100</span></span>                        | <span data-ttu-id="88345-191">111</span><span class="sxs-lookup"><span data-stu-id="88345-191">111</span></span>                       | <span data-ttu-id="88345-192">83</span><span class="sxs-lookup"><span data-stu-id="88345-192">83</span></span>                       | <span data-ttu-id="88345-193">**83.25**</span><span class="sxs-lookup"><span data-stu-id="88345-193">**83.25**</span></span>          |
| <span data-ttu-id="88345-194">Měna pro vykazování</span><span class="sxs-lookup"><span data-stu-id="88345-194">Reporting currency</span></span>              | <span data-ttu-id="88345-195">100</span><span class="sxs-lookup"><span data-stu-id="88345-195">100</span></span>                        | <span data-ttu-id="88345-196">111</span><span class="sxs-lookup"><span data-stu-id="88345-196">111</span></span>                       | <span data-ttu-id="88345-197">83</span><span class="sxs-lookup"><span data-stu-id="88345-197">83</span></span>                       | <span data-ttu-id="88345-198">**83**</span><span class="sxs-lookup"><span data-stu-id="88345-198">**83**</span></span>             |

<span data-ttu-id="88345-199">Při spuštění programu vyrovnání DPH na konci měsíce bude účetní položka vypadat takto:.</span><span class="sxs-lookup"><span data-stu-id="88345-199">When you run the sales tax settlement program at month-end, the accounting entry will be as follows:.</span></span>
#### <a name="scenario-sales-tax-conversion--accounting-currency"></a><span data-ttu-id="88345-200">Scénář: převod DPH = "zúčtovací měna"</span><span class="sxs-lookup"><span data-stu-id="88345-200">Scenario: sales tax conversion = "Accounting currency"</span></span>

| <span data-ttu-id="88345-201">Hlavní účet</span><span class="sxs-lookup"><span data-stu-id="88345-201">Main account</span></span>           | <span data-ttu-id="88345-202">Měna transakce (GBP)</span><span class="sxs-lookup"><span data-stu-id="88345-202">Transaction currency (GBP)</span></span> | <span data-ttu-id="88345-203">Zúčtovací měna (USD)</span><span class="sxs-lookup"><span data-stu-id="88345-203">Accounting currency (USD)</span></span> | <span data-ttu-id="88345-204">Měna vykazování (GBP)</span><span class="sxs-lookup"><span data-stu-id="88345-204">Reporting currency (GBP)</span></span> |
| ---------------------- | -------------------------- | ------------------------- | ------------------------ |
| <span data-ttu-id="88345-205">Závazky / pohledávky daně</span><span class="sxs-lookup"><span data-stu-id="88345-205">Tax Payable/Receivable</span></span> | <span data-ttu-id="88345-206">-83,25</span><span class="sxs-lookup"><span data-stu-id="88345-206">-83.25</span></span>                     | <span data-ttu-id="88345-207">-111</span><span class="sxs-lookup"><span data-stu-id="88345-207">-111</span></span>                      | <span data-ttu-id="88345-208">-83,25</span><span class="sxs-lookup"><span data-stu-id="88345-208">-83.25</span></span>                   |
| <span data-ttu-id="88345-209">Vyrovnání daně</span><span class="sxs-lookup"><span data-stu-id="88345-209">Tax Settlement</span></span>         | <span data-ttu-id="88345-210">83.25</span><span class="sxs-lookup"><span data-stu-id="88345-210">83.25</span></span>                      | <span data-ttu-id="88345-211">111</span><span class="sxs-lookup"><span data-stu-id="88345-211">111</span></span>                       | <span data-ttu-id="88345-212">83.25</span><span class="sxs-lookup"><span data-stu-id="88345-212">83.25</span></span>                    |
| <span data-ttu-id="88345-213">Realizovaný zisk/ztráta</span><span class="sxs-lookup"><span data-stu-id="88345-213">Realized Gain/Loss</span></span>     | <span data-ttu-id="88345-214">0</span><span class="sxs-lookup"><span data-stu-id="88345-214">0</span></span>                          | <span data-ttu-id="88345-215">0</span><span class="sxs-lookup"><span data-stu-id="88345-215">0</span></span>                         | <span data-ttu-id="88345-216">-0,25</span><span class="sxs-lookup"><span data-stu-id="88345-216">-0.25</span></span>                    |
| <span data-ttu-id="88345-217">Závazky / pohledávky daně</span><span class="sxs-lookup"><span data-stu-id="88345-217">Tax Payable/Receivable</span></span> | <span data-ttu-id="88345-218">0</span><span class="sxs-lookup"><span data-stu-id="88345-218">0</span></span>                          | <span data-ttu-id="88345-219">0</span><span class="sxs-lookup"><span data-stu-id="88345-219">0</span></span>                         | <span data-ttu-id="88345-220">0.25</span><span class="sxs-lookup"><span data-stu-id="88345-220">0.25</span></span>                     |

#### <a name="scenario-sales-tax-conversion--reporting-currency"></a><span data-ttu-id="88345-221">Scénář: převod DPH = "měna vykazování"</span><span class="sxs-lookup"><span data-stu-id="88345-221">Scenario: sales tax conversion = "Reporting currency"</span></span>


| <span data-ttu-id="88345-222">Hlavní účet</span><span class="sxs-lookup"><span data-stu-id="88345-222">Main account</span></span>           | <span data-ttu-id="88345-223">Měna transakce (GBP)</span><span class="sxs-lookup"><span data-stu-id="88345-223">Transaction currency (GBP)</span></span> | <span data-ttu-id="88345-224">Zúčtovací měna (USD)</span><span class="sxs-lookup"><span data-stu-id="88345-224">Accounting currency (USD)</span></span> | <span data-ttu-id="88345-225">Měna vykazování (GBP)</span><span class="sxs-lookup"><span data-stu-id="88345-225">Reporting currency (GBP)</span></span> |
| ---------------------- | -------------------------- | ------------------------- | ------------------------ |
| <span data-ttu-id="88345-226">Závazky / pohledávky daně</span><span class="sxs-lookup"><span data-stu-id="88345-226">Tax Payable/Receivable</span></span> | <span data-ttu-id="88345-227">-83</span><span class="sxs-lookup"><span data-stu-id="88345-227">-83</span></span>                        | <span data-ttu-id="88345-228">-110,67</span><span class="sxs-lookup"><span data-stu-id="88345-228">-110.67</span></span>                   | <span data-ttu-id="88345-229">-83</span><span class="sxs-lookup"><span data-stu-id="88345-229">-83</span></span>                      |
| <span data-ttu-id="88345-230">Vyrovnání daně</span><span class="sxs-lookup"><span data-stu-id="88345-230">Tax Settlement</span></span>         | <span data-ttu-id="88345-231">83</span><span class="sxs-lookup"><span data-stu-id="88345-231">83</span></span>                         | <span data-ttu-id="88345-232">110.67</span><span class="sxs-lookup"><span data-stu-id="88345-232">110.67</span></span>                    | <span data-ttu-id="88345-233">83</span><span class="sxs-lookup"><span data-stu-id="88345-233">83</span></span>                       |
| <span data-ttu-id="88345-234">Realizovaný zisk/ztráta</span><span class="sxs-lookup"><span data-stu-id="88345-234">Realized Gain/Loss</span></span>     | <span data-ttu-id="88345-235">0</span><span class="sxs-lookup"><span data-stu-id="88345-235">0</span></span>                          | <span data-ttu-id="88345-236">0.33</span><span class="sxs-lookup"><span data-stu-id="88345-236">0.33</span></span>                      | <span data-ttu-id="88345-237">0</span><span class="sxs-lookup"><span data-stu-id="88345-237">0</span></span>                        |
| <span data-ttu-id="88345-238">Závazky / pohledávky daně</span><span class="sxs-lookup"><span data-stu-id="88345-238">Tax Payable/Receivable</span></span> | <span data-ttu-id="88345-239">0</span><span class="sxs-lookup"><span data-stu-id="88345-239">0</span></span>                          | <span data-ttu-id="88345-240">-0,33</span><span class="sxs-lookup"><span data-stu-id="88345-240">-0.33</span></span>                     | <span data-ttu-id="88345-241">0</span><span class="sxs-lookup"><span data-stu-id="88345-241">0</span></span>                        |



<span data-ttu-id="88345-242">Další informace naleznete v následujících tématech:</span><span class="sxs-lookup"><span data-stu-id="88345-242">For more information, see the following topics:</span></span>

- [<span data-ttu-id="88345-243">Duální měna</span><span class="sxs-lookup"><span data-stu-id="88345-243">Dual currency</span></span>](dual-currency.md)
- [<span data-ttu-id="88345-244">Přehled DPH</span><span class="sxs-lookup"><span data-stu-id="88345-244">Sales tax overview</span></span>](indirect-taxes-overview.md)

