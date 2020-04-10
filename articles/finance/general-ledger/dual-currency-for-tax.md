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
ms.openlocfilehash: 863403dc3b2444f00f0cac27a494fc49d3d70de7
ms.sourcegitcommit: 34e543e807ac8790597f522fe3b4f0266cf4ee56
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/24/2020
ms.locfileid: "3161585"
---
# <a name="dual-currency-support-for-sales-tax"></a><span data-ttu-id="68183-103">Podpora duální měny pro DPH</span><span class="sxs-lookup"><span data-stu-id="68183-103">Dual currency support for sales tax</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="68183-104">Toto téma vysvětluje, jak rozšířit funkci účtování duálních měn pro DPH a dopad na výpočet, zaúčtování a vypořádání DPH.</span><span class="sxs-lookup"><span data-stu-id="68183-104">This topic explains how to extend dual currency accounting for sales taxes and the impact for sales tax calculations, posting and settlements.</span></span>

<span data-ttu-id="68183-105">Funkce duální měny pro Dynamics 365 Finance byla představena ve verzi 8.1 (říjen 2018).</span><span class="sxs-lookup"><span data-stu-id="68183-105">The Dual currency feature for Dynamics 365 Finance was introduced in version 8.1 (October 2018).</span></span> <span data-ttu-id="68183-106">Mění, jakým způsobem se počítají účtovací položky v měně vykazování.</span><span class="sxs-lookup"><span data-stu-id="68183-106">It changes the way that accounting entries in the reporting currency are calculated.</span></span>

<span data-ttu-id="68183-107">V předchozích verzích byly transakce převedeny na měnu vykazování v následujícím pořadí:</span><span class="sxs-lookup"><span data-stu-id="68183-107">In earlier versions, transactions were converted to the reporting currency in the following sequence:</span></span> 

- <span data-ttu-id="68183-108">Celková transakce byla vypočtena v měně transakce > částka transakce byla převedena na zúčtovací měnu > částka zúčtovací měny byla převedena na měnu vykazování</span><span class="sxs-lookup"><span data-stu-id="68183-108">Transaction total was calculated in the transaction currency > Transaction amount was converted to the accounting currency > Accounting currency amount was converted to the Reporting currency</span></span>

<span data-ttu-id="68183-109">Po povolení duální funkce měny byly transakce převedeny na měnu vykazování v následujícím pořadí:</span><span class="sxs-lookup"><span data-stu-id="68183-109">After enabling the dual currency feature, transactions were converted to the reporting currency in the following sequence:</span></span>

- <span data-ttu-id="68183-110">Částka v měně transakce > Částka v měně pro vykazování</span><span class="sxs-lookup"><span data-stu-id="68183-110">Transaction currency amount > Reporting currency amount</span></span>

<span data-ttu-id="68183-111">Další informace o duální měně naleznete v [Duální měně](dual-currency.md).</span><span class="sxs-lookup"><span data-stu-id="68183-111">For more information about dual currency, please refer to [Dual currency](dual-currency.md).</span></span>

<span data-ttu-id="68183-112">V důsledku podpory duálních měn jsou v modulu Správa funkcí k dispozici dvě nové funkce:</span><span class="sxs-lookup"><span data-stu-id="68183-112">As a consequence of support for dual currencies, two new features are available in feature management:</span></span> 

- <span data-ttu-id="68183-113">Převod DPH (zavedeno ve verzi 10.0.9)</span><span class="sxs-lookup"><span data-stu-id="68183-113">Sales tax conversion (Release in version 10.0.9)</span></span>
- <span data-ttu-id="68183-114">Automatický zůstatek pro vyrovnání daně v měně vykazování (zavedeno ve verzi 10.0.11)</span><span class="sxs-lookup"><span data-stu-id="68183-114">Tax settlement auto balance in reporting currency (Release in version 10.0.11)</span></span>

<span data-ttu-id="68183-115">Podpora dvojí měny pro DPH zajišťuje, že daně budou vypočítány přesně v měně daně a že zůstatek vyrovnání DPH je vypočítán přesně v zúčtovací měně i v měně vykazování.</span><span class="sxs-lookup"><span data-stu-id="68183-115">Dual currency support for sales taxes ensures that taxes are calculated accurately in the tax currency, and that the sales tax settlement balance is calculated accurately in both the accounting currency and reporting currency.</span></span> 

## <a name="sales-tax-conversion"></a><span data-ttu-id="68183-116">Převod DPH</span><span class="sxs-lookup"><span data-stu-id="68183-116">Sales tax conversion</span></span>

<span data-ttu-id="68183-117">**Parametr převodu DPH** poskytuje dvě možnosti převodu částky daně z transakční měny na daňovou měnu.</span><span class="sxs-lookup"><span data-stu-id="68183-117">The **Sales tax conversion** parameter provides two options to convert tax amount from transaction currency to tax currency.</span></span> 

- <span data-ttu-id="68183-118">Zúčtovací měna: cesta bude "Částka v měně transakce > Částka v zúčtovací měně > Částka v měně daně".</span><span class="sxs-lookup"><span data-stu-id="68183-118">Accounting currency: The path will be "Amount in transaction currency > Amount in accounting currency > Amount in tax currency".</span></span> <span data-ttu-id="68183-119">Typ směnného kurzu zúčtovací měny (konfigurován v nastavení hlavní knihy) bude použit pro převod měny.</span><span class="sxs-lookup"><span data-stu-id="68183-119">The accounting currency exhange rate type (configured in Ledger setup) will be used for the currency conversion.</span></span>
- <span data-ttu-id="68183-120">Měna vykazování: cesta bude "Částka v měně transakce > Částka v měně vykazování > Částka v měně daně".</span><span class="sxs-lookup"><span data-stu-id="68183-120">Reporting currency: The path will be "Amount in transaction currency > Amount in reporting currency > Amount in tax currency".</span></span> <span data-ttu-id="68183-121">Typ směnného kurzu měny vykazování (konfigurován v nastavení hlavní knihy) bude použit pro převod měny.</span><span class="sxs-lookup"><span data-stu-id="68183-121">The reporting currency exhange rate type (configured in Ledger setup) will be used for the currency conversion.</span></span>

### <a name="example"></a><span data-ttu-id="68183-122">Příklad</span><span class="sxs-lookup"><span data-stu-id="68183-122">Example</span></span>

<span data-ttu-id="68183-123">Jedná se o jednoduchý příklad, který demonstruje tyto funkce:</span><span class="sxs-lookup"><span data-stu-id="68183-123">A simple example to demonstrate this functionality is:</span></span>

<span data-ttu-id="68183-124">Nastavení měny pro hlavní knihu a daň</span><span class="sxs-lookup"><span data-stu-id="68183-124">Currency setup for ledger and tax</span></span>

| <span data-ttu-id="68183-125">Měna transakce</span><span class="sxs-lookup"><span data-stu-id="68183-125">Transaction currency</span></span> | <span data-ttu-id="68183-126">Zúčtovací měna</span><span class="sxs-lookup"><span data-stu-id="68183-126">Accounting currency</span></span> | <span data-ttu-id="68183-127">Měna pro vykazování</span><span class="sxs-lookup"><span data-stu-id="68183-127">Reporting currency</span></span> | <span data-ttu-id="68183-128">Měna daně</span><span class="sxs-lookup"><span data-stu-id="68183-128">Tax currency</span></span> |
| -------------------- | ------------------- | ------------------ | ------------ |
| <span data-ttu-id="68183-129">EUR</span><span class="sxs-lookup"><span data-stu-id="68183-129">EUR</span></span>                  | <span data-ttu-id="68183-130">USD</span><span class="sxs-lookup"><span data-stu-id="68183-130">USD</span></span>                 | <span data-ttu-id="68183-131">GBP</span><span class="sxs-lookup"><span data-stu-id="68183-131">GBP</span></span>                | <span data-ttu-id="68183-132">GBP</span><span class="sxs-lookup"><span data-stu-id="68183-132">GBP</span></span>          |

<span data-ttu-id="68183-133">Směnný kurz</span><span class="sxs-lookup"><span data-stu-id="68183-133">Exchange rate</span></span>

| <span data-ttu-id="68183-134">Z měny</span><span class="sxs-lookup"><span data-stu-id="68183-134">From currency</span></span> | <span data-ttu-id="68183-135">Na měnu</span><span class="sxs-lookup"><span data-stu-id="68183-135">To currency</span></span> | <span data-ttu-id="68183-136">Koeficient</span><span class="sxs-lookup"><span data-stu-id="68183-136">Factor</span></span> | <span data-ttu-id="68183-137">Směnný kurz</span><span class="sxs-lookup"><span data-stu-id="68183-137">Exchange rate</span></span> |
| ------------- | ----------- | ------ | ------------- |
| <span data-ttu-id="68183-138">EUR</span><span class="sxs-lookup"><span data-stu-id="68183-138">EUR</span></span>           | <span data-ttu-id="68183-139">USD</span><span class="sxs-lookup"><span data-stu-id="68183-139">USD</span></span>         | <span data-ttu-id="68183-140">1</span><span class="sxs-lookup"><span data-stu-id="68183-140">1</span></span>      | <span data-ttu-id="68183-141">1.11</span><span class="sxs-lookup"><span data-stu-id="68183-141">1.11</span></span>          |
| <span data-ttu-id="68183-142">EUR</span><span class="sxs-lookup"><span data-stu-id="68183-142">EUR</span></span>           | <span data-ttu-id="68183-143">GBP</span><span class="sxs-lookup"><span data-stu-id="68183-143">GBP</span></span>         | <span data-ttu-id="68183-144">1</span><span class="sxs-lookup"><span data-stu-id="68183-144">1</span></span>      | <span data-ttu-id="68183-145">0.83</span><span class="sxs-lookup"><span data-stu-id="68183-145">0.83</span></span>          |
| <span data-ttu-id="68183-146">USD</span><span class="sxs-lookup"><span data-stu-id="68183-146">USD</span></span>           | <span data-ttu-id="68183-147">GBP</span><span class="sxs-lookup"><span data-stu-id="68183-147">GBP</span></span>         | <span data-ttu-id="68183-148">1</span><span class="sxs-lookup"><span data-stu-id="68183-148">1</span></span>      | <span data-ttu-id="68183-149">0.75</span><span class="sxs-lookup"><span data-stu-id="68183-149">0.75</span></span>          |

<span data-ttu-id="68183-150">Výpočet částky daně v různých možnostech parametrů</span><span class="sxs-lookup"><span data-stu-id="68183-150">Tax amount calculation in different parameter options</span></span>

<span data-ttu-id="68183-151">Částka daně = 100 EUR</span><span class="sxs-lookup"><span data-stu-id="68183-151">Tax amount = 100 EUR</span></span>

| <span data-ttu-id="68183-152">Parametry převodu DPH</span><span class="sxs-lookup"><span data-stu-id="68183-152">Sales tax conversion parameters</span></span> | <span data-ttu-id="68183-153">Měna transakce (EUR)</span><span class="sxs-lookup"><span data-stu-id="68183-153">Transaction currency (EUR)</span></span> | <span data-ttu-id="68183-154">Zúčtovací měna (USD)</span><span class="sxs-lookup"><span data-stu-id="68183-154">Accounting currency (USD)</span></span> | <span data-ttu-id="68183-155">Měna vykazování (GBP)</span><span class="sxs-lookup"><span data-stu-id="68183-155">Reporting currency (GBP)</span></span> | <span data-ttu-id="68183-156">Měna daně (GBP)</span><span class="sxs-lookup"><span data-stu-id="68183-156">Tax currency (GBP)</span></span> |
| ------------------------------- | -------------------------- | ------------------------- | ------------------------ | ------------------ |
| <span data-ttu-id="68183-157">Zúčtovací měna</span><span class="sxs-lookup"><span data-stu-id="68183-157">Accounting currency</span></span>             | <span data-ttu-id="68183-158">100</span><span class="sxs-lookup"><span data-stu-id="68183-158">100</span></span>                        | <span data-ttu-id="68183-159">111</span><span class="sxs-lookup"><span data-stu-id="68183-159">111</span></span>                       | <span data-ttu-id="68183-160">83</span><span class="sxs-lookup"><span data-stu-id="68183-160">83</span></span>                       | <span data-ttu-id="68183-161">**83.25**</span><span class="sxs-lookup"><span data-stu-id="68183-161">**83.25**</span></span>          |
| <span data-ttu-id="68183-162">Měna pro vykazování</span><span class="sxs-lookup"><span data-stu-id="68183-162">Reporting currency</span></span>              | <span data-ttu-id="68183-163">100</span><span class="sxs-lookup"><span data-stu-id="68183-163">100</span></span>                        | <span data-ttu-id="68183-164">111</span><span class="sxs-lookup"><span data-stu-id="68183-164">111</span></span>                       | <span data-ttu-id="68183-165">83</span><span class="sxs-lookup"><span data-stu-id="68183-165">83</span></span>                       | <span data-ttu-id="68183-166">**83**</span><span class="sxs-lookup"><span data-stu-id="68183-166">**83**</span></span>             |

<span data-ttu-id="68183-167">Tento parametr lze nakonfigurovat podle potřeby finančního úřadu na základě kompatibility.</span><span class="sxs-lookup"><span data-stu-id="68183-167">This parameter can be configured based on the compliance need from tax authority.</span></span>


### <a name="upgrade-consideration"></a><span data-ttu-id="68183-168">Předpoklady upgradu</span><span class="sxs-lookup"><span data-stu-id="68183-168">Upgrade Consideration</span></span>

<span data-ttu-id="68183-169">Tato funkce bude použita pouze pro nové transakce.</span><span class="sxs-lookup"><span data-stu-id="68183-169">This feature will only apply for new transactions.</span></span> <span data-ttu-id="68183-170">V případě daňové transakce, která je již uložena v tabulce TAXTRANS, ale ještě nebyla vyrovnána, systém nepřepočítá částku daně v daňové měně, protože směnný kurz v určitém časovém bodu zaúčtování daně již chybí.</span><span class="sxs-lookup"><span data-stu-id="68183-170">For tax transaction already saved in TAXTRANS table but not settled yet, system will not recalculate tax amount in tax currency because the exchange rate at time point of posting tax is already missing.</span></span>

<span data-ttu-id="68183-171">Chcete-li zabránit předchozímu scénáři, doporučujeme změnit hodnotu tohoto parametru v novém (čistém) období vyrovnání daně, které neobsahuje žádné transakce nevyrovnané daně.</span><span class="sxs-lookup"><span data-stu-id="68183-171">To prevent preceding scenario, we recommend changing this parameter value in a new (clean) tax settlement period that doesn't contain any unsettled tax transactions.</span></span> <span data-ttu-id="68183-172">Chcete-li tuto hodnotu změnit uprostřed období daňového vyrovnání, spusťte před změnou hodnoty tohoto parametru program "Vyrovnat a zaúčtovat DPH" pro období aktuálního vyrovnání.</span><span class="sxs-lookup"><span data-stu-id="68183-172">To change this value in the middle of a tax settlement period, please run "Settle and post sales tax" program for current tax settlement period before changing this parameter value.</span></span>


## <a name="track-reporting-currency-tax-amount"></a><span data-ttu-id="68183-173">Sledovat částku daně v měně vykazování</span><span class="sxs-lookup"><span data-stu-id="68183-173">Track reporting currency tax amount</span></span>

<span data-ttu-id="68183-174">Do tabulek souvisejících s daní byla přidána tři nová pole pro sledování částek v měně vykazování.</span><span class="sxs-lookup"><span data-stu-id="68183-174">Three new fields were added to tax-related tables to track amounts in the reporting currency.</span></span> <span data-ttu-id="68183-175">Tato pole se nacházejí v tabulkách TAXUNCOMMITTED a TAXTRANS:</span><span class="sxs-lookup"><span data-stu-id="68183-175">These fields are within the TAXUNCOMMITTED and TAXTRANS tables:</span></span>

- <span data-ttu-id="68183-176">TaxAmountRep: částka daně v měně vykazování</span><span class="sxs-lookup"><span data-stu-id="68183-176">TaxAmountRep: tax amount in reporting currency</span></span>
- <span data-ttu-id="68183-177">TaxBaseAmountRep: částka základu v měně vykazování</span><span class="sxs-lookup"><span data-stu-id="68183-177">TaxBaseAmountRep: base amount in reporting currency</span></span>
- <span data-ttu-id="68183-178">TaxInCostPriceRep: neodečitatelná částka v měně vykazování</span><span class="sxs-lookup"><span data-stu-id="68183-178">TaxInCostPriceRep: non-deductible amount in reporting currency</span></span>

<span data-ttu-id="68183-179">U daně uložené pouze v tabulce TAXUNCOMMITTED, ale dosud nezaúčtované, systém přepočítá částku daně v měně vykazování v okamžiku zaúčtování a uloží do tabulky TAXTRANS.</span><span class="sxs-lookup"><span data-stu-id="68183-179">For tax only saved in TAXUNCOMMITTED table but not posted yet, system will recalculate tax amount in reporting currency at the time of posting and save in TAXTRANS table.</span></span>

<span data-ttu-id="68183-180">Tato verze nebude zahrnovat změny v sestavách a formulářích, které zobrazují částku daně v měně vykazování.</span><span class="sxs-lookup"><span data-stu-id="68183-180">This release will not include changes to reports and forms that show the tax amount in the reporting currency.</span></span> <span data-ttu-id="68183-181">Změny v sestavách a formulářích budou dodány v budoucí verzi.</span><span class="sxs-lookup"><span data-stu-id="68183-181">Changes to reports and forms will be delivered in the future release.</span></span>



## <a name="tax-settlement-auto-balance-in-reporting-currency"></a><span data-ttu-id="68183-182">Automatický zůstatek pro vyrovnání daně v měně vykazování</span><span class="sxs-lookup"><span data-stu-id="68183-182">Tax settlement auto-balance in reporting currency</span></span>

<span data-ttu-id="68183-183">Není-li vyrovnání daně v měně vykazování rovnoměrně vyrovnáno, jako například cesta převodu DPH je "zúčtovací měna" nebo změna směnného kurzu v jednom období vyrovnání daně, systém automaticky vygeneruje účetní položky k úpravě odchylky částky daně a k její kompenzaci na účet realizovaných zisků/ztrát, který je konfigurován v nastavení hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="68183-183">If the tax settlement is not balanced in the reporting currency for certain reason such as the sales tax conversion path is "Accounting currency", or the exchange rate change in a single tax settlement period, thebn the system will automatically generate accounting entries to adjust the tax amount variance and offset it against realized exchange gain/loss account, which is configured in Ledger setup.</span></span>

<span data-ttu-id="68183-184">Chcete-li předvést tuto funkci pomocí předchozího příkladu, Předpokládejme, že data v tabulce TAXTRANS v okamžiku zaúčtování jsou následující:</span><span class="sxs-lookup"><span data-stu-id="68183-184">Using the the previous example to demonstrate this feature, suppose that the data in TAXTRANS table at the time of posting is as follows.</span></span>

| <span data-ttu-id="68183-185">Parametry převodu DPH</span><span class="sxs-lookup"><span data-stu-id="68183-185">Sales tax conversion parameters</span></span> | <span data-ttu-id="68183-186">Měna transakce (EUR)</span><span class="sxs-lookup"><span data-stu-id="68183-186">Transaction currency (EUR)</span></span> | <span data-ttu-id="68183-187">Zúčtovací měna (USD)</span><span class="sxs-lookup"><span data-stu-id="68183-187">Accounting currency (USD)</span></span> | <span data-ttu-id="68183-188">Měna vykazování (GBP)</span><span class="sxs-lookup"><span data-stu-id="68183-188">Reporting currency (GBP)</span></span> | <span data-ttu-id="68183-189">Měna daně (GBP)</span><span class="sxs-lookup"><span data-stu-id="68183-189">Tax currency (GBP)</span></span> |
| ------------------------------- | -------------------------- | ------------------------- | ------------------------ | ------------------ |
| <span data-ttu-id="68183-190">Zúčtovací měna</span><span class="sxs-lookup"><span data-stu-id="68183-190">Accounting currency</span></span>             | <span data-ttu-id="68183-191">100</span><span class="sxs-lookup"><span data-stu-id="68183-191">100</span></span>                        | <span data-ttu-id="68183-192">111</span><span class="sxs-lookup"><span data-stu-id="68183-192">111</span></span>                       | <span data-ttu-id="68183-193">83</span><span class="sxs-lookup"><span data-stu-id="68183-193">83</span></span>                       | <span data-ttu-id="68183-194">**83.25**</span><span class="sxs-lookup"><span data-stu-id="68183-194">**83.25**</span></span>          |
| <span data-ttu-id="68183-195">Měna pro vykazování</span><span class="sxs-lookup"><span data-stu-id="68183-195">Reporting currency</span></span>              | <span data-ttu-id="68183-196">100</span><span class="sxs-lookup"><span data-stu-id="68183-196">100</span></span>                        | <span data-ttu-id="68183-197">111</span><span class="sxs-lookup"><span data-stu-id="68183-197">111</span></span>                       | <span data-ttu-id="68183-198">83</span><span class="sxs-lookup"><span data-stu-id="68183-198">83</span></span>                       | <span data-ttu-id="68183-199">**83**</span><span class="sxs-lookup"><span data-stu-id="68183-199">**83**</span></span>             |

<span data-ttu-id="68183-200">Při spuštění programu vyrovnání DPH na konci měsíce bude účetní položka vypadat takto:.</span><span class="sxs-lookup"><span data-stu-id="68183-200">When you run the sales tax settlement program at month-end, the accounting entry will be as follows:.</span></span>
#### <a name="scenario-sales-tax-conversion--accounting-currency"></a><span data-ttu-id="68183-201">Scénář: převod DPH = "zúčtovací měna"</span><span class="sxs-lookup"><span data-stu-id="68183-201">Scenario: sales tax conversion = "Accounting currency"</span></span>

| <span data-ttu-id="68183-202">Hlavní účet</span><span class="sxs-lookup"><span data-stu-id="68183-202">Main account</span></span>           | <span data-ttu-id="68183-203">Měna transakce (GBP)</span><span class="sxs-lookup"><span data-stu-id="68183-203">Transaction currency (GBP)</span></span> | <span data-ttu-id="68183-204">Zúčtovací měna (USD)</span><span class="sxs-lookup"><span data-stu-id="68183-204">Accounting currency (USD)</span></span> | <span data-ttu-id="68183-205">Měna vykazování (GBP)</span><span class="sxs-lookup"><span data-stu-id="68183-205">Reporting currency (GBP)</span></span> |
| ---------------------- | -------------------------- | ------------------------- | ------------------------ |
| <span data-ttu-id="68183-206">Závazky / pohledávky daně</span><span class="sxs-lookup"><span data-stu-id="68183-206">Tax Payable/Receivable</span></span> | <span data-ttu-id="68183-207">-83,25</span><span class="sxs-lookup"><span data-stu-id="68183-207">-83.25</span></span>                     | <span data-ttu-id="68183-208">-111</span><span class="sxs-lookup"><span data-stu-id="68183-208">-111</span></span>                      | <span data-ttu-id="68183-209">-83,25</span><span class="sxs-lookup"><span data-stu-id="68183-209">-83.25</span></span>                   |
| <span data-ttu-id="68183-210">Vyrovnání daně</span><span class="sxs-lookup"><span data-stu-id="68183-210">Tax Settlement</span></span>         | <span data-ttu-id="68183-211">83.25</span><span class="sxs-lookup"><span data-stu-id="68183-211">83.25</span></span>                      | <span data-ttu-id="68183-212">111</span><span class="sxs-lookup"><span data-stu-id="68183-212">111</span></span>                       | <span data-ttu-id="68183-213">83.25</span><span class="sxs-lookup"><span data-stu-id="68183-213">83.25</span></span>                    |
| <span data-ttu-id="68183-214">Realizovaný zisk/ztráta</span><span class="sxs-lookup"><span data-stu-id="68183-214">Realized Gain/Loss</span></span>     | <span data-ttu-id="68183-215">0</span><span class="sxs-lookup"><span data-stu-id="68183-215">0</span></span>                          | <span data-ttu-id="68183-216">0</span><span class="sxs-lookup"><span data-stu-id="68183-216">0</span></span>                         | <span data-ttu-id="68183-217">-0,25</span><span class="sxs-lookup"><span data-stu-id="68183-217">-0.25</span></span>                    |
| <span data-ttu-id="68183-218">Závazky / pohledávky daně</span><span class="sxs-lookup"><span data-stu-id="68183-218">Tax Payable/Receivable</span></span> | <span data-ttu-id="68183-219">0</span><span class="sxs-lookup"><span data-stu-id="68183-219">0</span></span>                          | <span data-ttu-id="68183-220">0</span><span class="sxs-lookup"><span data-stu-id="68183-220">0</span></span>                         | <span data-ttu-id="68183-221">0.25</span><span class="sxs-lookup"><span data-stu-id="68183-221">0.25</span></span>                     |

#### <a name="scenario-sales-tax-conversion--reporting-currency"></a><span data-ttu-id="68183-222">Scénář: převod DPH = "měna vykazování"</span><span class="sxs-lookup"><span data-stu-id="68183-222">Scenario: sales tax conversion = "Reporting currency"</span></span>


| <span data-ttu-id="68183-223">Hlavní účet</span><span class="sxs-lookup"><span data-stu-id="68183-223">Main account</span></span>           | <span data-ttu-id="68183-224">Měna transakce (GBP)</span><span class="sxs-lookup"><span data-stu-id="68183-224">Transaction currency (GBP)</span></span> | <span data-ttu-id="68183-225">Zúčtovací měna (USD)</span><span class="sxs-lookup"><span data-stu-id="68183-225">Accounting currency (USD)</span></span> | <span data-ttu-id="68183-226">Měna vykazování (GBP)</span><span class="sxs-lookup"><span data-stu-id="68183-226">Reporting currency (GBP)</span></span> |
| ---------------------- | -------------------------- | ------------------------- | ------------------------ |
| <span data-ttu-id="68183-227">Závazky / pohledávky daně</span><span class="sxs-lookup"><span data-stu-id="68183-227">Tax Payable/Receivable</span></span> | <span data-ttu-id="68183-228">-83</span><span class="sxs-lookup"><span data-stu-id="68183-228">-83</span></span>                        | <span data-ttu-id="68183-229">-110,67</span><span class="sxs-lookup"><span data-stu-id="68183-229">-110.67</span></span>                   | <span data-ttu-id="68183-230">-83</span><span class="sxs-lookup"><span data-stu-id="68183-230">-83</span></span>                      |
| <span data-ttu-id="68183-231">Vyrovnání daně</span><span class="sxs-lookup"><span data-stu-id="68183-231">Tax Settlement</span></span>         | <span data-ttu-id="68183-232">83</span><span class="sxs-lookup"><span data-stu-id="68183-232">83</span></span>                         | <span data-ttu-id="68183-233">110.67</span><span class="sxs-lookup"><span data-stu-id="68183-233">110.67</span></span>                    | <span data-ttu-id="68183-234">83</span><span class="sxs-lookup"><span data-stu-id="68183-234">83</span></span>                       |
| <span data-ttu-id="68183-235">Realizovaný zisk/ztráta</span><span class="sxs-lookup"><span data-stu-id="68183-235">Realized Gain/Loss</span></span>     | <span data-ttu-id="68183-236">0</span><span class="sxs-lookup"><span data-stu-id="68183-236">0</span></span>                          | <span data-ttu-id="68183-237">0.33</span><span class="sxs-lookup"><span data-stu-id="68183-237">0.33</span></span>                      | <span data-ttu-id="68183-238">0</span><span class="sxs-lookup"><span data-stu-id="68183-238">0</span></span>                        |
| <span data-ttu-id="68183-239">Závazky / pohledávky daně</span><span class="sxs-lookup"><span data-stu-id="68183-239">Tax Payable/Receivable</span></span> | <span data-ttu-id="68183-240">0</span><span class="sxs-lookup"><span data-stu-id="68183-240">0</span></span>                          | <span data-ttu-id="68183-241">-0,33</span><span class="sxs-lookup"><span data-stu-id="68183-241">-0.33</span></span>                     | <span data-ttu-id="68183-242">0</span><span class="sxs-lookup"><span data-stu-id="68183-242">0</span></span>                        |



<span data-ttu-id="68183-243">Další informace naleznete v následujících tématech:</span><span class="sxs-lookup"><span data-stu-id="68183-243">For more information, see the following topics:</span></span>

- [<span data-ttu-id="68183-244">Duální měna</span><span class="sxs-lookup"><span data-stu-id="68183-244">Dual currency</span></span>](dual-currency.md)
- [<span data-ttu-id="68183-245">Přehled DPH</span><span class="sxs-lookup"><span data-stu-id="68183-245">Sales tax overview</span></span>](indirect-taxes-overview.md)

