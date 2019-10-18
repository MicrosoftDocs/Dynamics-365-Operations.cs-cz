---
title: Výpočet DPH na řádcích hlavního deníku
description: V tomto tématu je vysvětleno, jak se počítá DPH pro různé typy účtů (dodavatel, odběratel, hlavní kniha a projekt) na řádcích hlavního deníku.
author: EricWang
manager: Ann Beebe
ms.date: 08/14/2019
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
ms.search.validFrom: 2019-08-14
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 354076dbc14f34b83d1cd24f591874b9af856af1
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186295"
---
# <a name="sales-tax-calculation-on-general-journal-lines"></a><span data-ttu-id="00a90-103">Výpočet DPH na řádcích hlavního deníku</span><span class="sxs-lookup"><span data-stu-id="00a90-103">Sales tax calculation on general journal lines</span></span>
[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="00a90-104">V tomto tématu je vysvětleno, jak se počítá DPH pro různé typy účtů (dodavatel, odběratel, hlavní kniha a projekt) na řádcích hlavního deníku.</span><span class="sxs-lookup"><span data-stu-id="00a90-104">This topic explains how sales taxes are calculated for different types of accounts (vendor, customer, ledger, and project) on general journal lines.</span></span>

<span data-ttu-id="00a90-105">Tento proces lze rozdělit do tří kroků:</span><span class="sxs-lookup"><span data-stu-id="00a90-105">The process can be divided into three steps:</span></span>

- <span data-ttu-id="00a90-106">Určete směr DPH.</span><span class="sxs-lookup"><span data-stu-id="00a90-106">Determine the sales tax direction.</span></span>

- <span data-ttu-id="00a90-107">Určete částku DPH, která bude uložena jako dočasná tabulka DPH.</span><span class="sxs-lookup"><span data-stu-id="00a90-107">Determine the sales tax amount that will be stored a temporary sales tax table.</span></span>

- <span data-ttu-id="00a90-108">Určete částku DPH a účet na dokladu.</span><span class="sxs-lookup"><span data-stu-id="00a90-108">Determine the sales tax amount and account on the voucher.</span></span>

## <a name="determine-the-sales-tax-direction"></a><span data-ttu-id="00a90-109">Určení směru DPH</span><span class="sxs-lookup"><span data-stu-id="00a90-109">Determine the sales tax direction</span></span>

<span data-ttu-id="00a90-110">Způsob, jakým je určen směr DPH, závisí na typu účtu v dokladu.</span><span class="sxs-lookup"><span data-stu-id="00a90-110">The way that the sales tax direction is determined depends on the type of account in the voucher.</span></span> <span data-ttu-id="00a90-111">Směr DPH je určen kombinací typu účtu a kódu DPH.</span><span class="sxs-lookup"><span data-stu-id="00a90-111">The sales tax direction is determined by the combination of account type and sales tax code.</span></span> <span data-ttu-id="00a90-112">V následujících oddílech jsou uvedeny podrobnosti o možnostech.</span><span class="sxs-lookup"><span data-stu-id="00a90-112">The following sections the possibilities in more detail.</span></span> 

### <a name="account-type-is-project"></a><span data-ttu-id="00a90-113">Typ účtu je Projekt.</span><span class="sxs-lookup"><span data-stu-id="00a90-113">Account type is Project</span></span>

<span data-ttu-id="00a90-114">Pokud má doklad řádek deníku, u kterého je typ účtu **Projekt**, budou všechny řádky deníku v dokladu používat stejný směr DPH.</span><span class="sxs-lookup"><span data-stu-id="00a90-114">If a voucher has journal line where the account type is **Project**, all the journal lines in the voucher apply the same tax direction.</span></span> <span data-ttu-id="00a90-115">Následující obrázek znázorňuje pravidlo.</span><span class="sxs-lookup"><span data-stu-id="00a90-115">The following illustration shows the rule.</span></span> <span data-ttu-id="00a90-116">Následující body znázorňují možné daňové pokyny pro účty projektu.</span><span class="sxs-lookup"><span data-stu-id="00a90-116">The following points show the possible tax directions for project accounts.</span></span>

<span data-ttu-id="00a90-117">•   Pokud je kód DPH importní DPH, je směr DPH Importní DPH.</span><span class="sxs-lookup"><span data-stu-id="00a90-117">•   If the sales tax code is use tax, then sales tax direction is Use Tax.</span></span>

<span data-ttu-id="00a90-118">•   Pokud je kód DPH Osvobození od daně, je směr Nákup bez daně.</span><span class="sxs-lookup"><span data-stu-id="00a90-118">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="00a90-119">•   Pokud je kód DPH vnitřní DPH, je směr DPH Splatná DPH.</span><span class="sxs-lookup"><span data-stu-id="00a90-119">•   If the sales tax code is intracom VAT, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="00a90-120">•   Pokud je kód DPH stornované účtování, je směr DPH Splatná DPH.</span><span class="sxs-lookup"><span data-stu-id="00a90-120">•   If the sales tax code is reverse charge, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="00a90-121">V opačném případě je směr DPH pohledávka DPH.</span><span class="sxs-lookup"><span data-stu-id="00a90-121">Otherwise, sales tax direction is Sales Tax Receivable.</span></span>

<span data-ttu-id="00a90-122">V následujícím diagramu je pravidlo znázorněno graficky.</span><span class="sxs-lookup"><span data-stu-id="00a90-122">The following diagram illustrates the rule graphically.</span></span>

![Možnosti daňových směrů pro účty projektu](media/Sales-Tax-Direction-Vendor.jpg)

### <a name="account-type-is-vendor"></a><span data-ttu-id="00a90-124">Typ účtu je Dodavatel</span><span class="sxs-lookup"><span data-stu-id="00a90-124">Account type is Vendor</span></span>

<span data-ttu-id="00a90-125">Pokud má doklad řádek deníku, u kterého je typ účtu **Dodavatel**, budou všechny řádky deníku v dokladu používat stejný směr DPH.</span><span class="sxs-lookup"><span data-stu-id="00a90-125">If a voucher has journal line where the account type is **Vendor**, all the journal lines in the voucher apply the same tax direction.</span></span> <span data-ttu-id="00a90-126">Následující body znázorňují možné daňové pokyny pro účty dodavatele.</span><span class="sxs-lookup"><span data-stu-id="00a90-126">The following points show the possible tax directions for vendor accounts.</span></span> 

<span data-ttu-id="00a90-127">•   Pokud je kód DPH Osvobození od daně, je směr Nákup bez daně.</span><span class="sxs-lookup"><span data-stu-id="00a90-127">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="00a90-128">•   Pokud je kód DPH vnitřní DPH, je směr DPH Pohledávka DPH.</span><span class="sxs-lookup"><span data-stu-id="00a90-128">•   If the sales tax code is intracom VAT, then sales tax direction is Sales Tax Receivable.</span></span>

<span data-ttu-id="00a90-129">•   Pokud je kód DPH stornované účtování, je směr DPH Pohledávka DPH.</span><span class="sxs-lookup"><span data-stu-id="00a90-129">•   If the sales tax code is reverse charge, then sales tax direction is Sales Tax Receivable.</span></span>


<span data-ttu-id="00a90-130">V opačném případě je směr DPH Splatná DPH.</span><span class="sxs-lookup"><span data-stu-id="00a90-130">Otherwise, sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="00a90-131">V následujícím diagramu je pravidlo znázorněno graficky.</span><span class="sxs-lookup"><span data-stu-id="00a90-131">The following diagram illustrates the rule graphically.</span></span>

![Možnosti daňových směrů pro účty dodavatele](media/Sales-Tax-Direction-Vendor.jpg)

### <a name="account-type-is-customer"></a><span data-ttu-id="00a90-133">Typ účtu je Zákazník.</span><span class="sxs-lookup"><span data-stu-id="00a90-133">Account type is Customer</span></span>

<span data-ttu-id="00a90-134">Pokud má doklad řádek deníku, u kterého je typ účtu **Zákazník**, budou všechny řádky deníku v dokladu používat stejný směr DPH.</span><span class="sxs-lookup"><span data-stu-id="00a90-134">If a voucher has journal line where the account type is **Customer**, all the journal lines in the voucher apply the same tax direction.</span></span> <span data-ttu-id="00a90-135">Následující body znázorňují možné daňové pokyny pro účty zákazníka.</span><span class="sxs-lookup"><span data-stu-id="00a90-135">The following points show the possible tax directions for customer accounts.</span></span>

<span data-ttu-id="00a90-136">•   Pokud je kód DPH importní DPH, je směr DPH Importní DPH.</span><span class="sxs-lookup"><span data-stu-id="00a90-136">•   If the sales tax code is use tax, then sales tax direction is Use Tax.</span></span>

<span data-ttu-id="00a90-137">•   Pokud je kód DPH Osvobození od daně, je směr Nákup bez daně.</span><span class="sxs-lookup"><span data-stu-id="00a90-137">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="00a90-138">•   Pokud je kód DPH vnitřní DPH, je směr DPH Splatná DPH.</span><span class="sxs-lookup"><span data-stu-id="00a90-138">•   If the sales tax code is intracom VAT, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="00a90-139">•   Pokud je kód DPH stornované účtování, je směr DPH Splatná DPH.</span><span class="sxs-lookup"><span data-stu-id="00a90-139">•   If the sales tax code is reverse charge, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="00a90-140">V opačném případě je směr DPH pohledávka DPH.</span><span class="sxs-lookup"><span data-stu-id="00a90-140">Otherwise, sales tax direction is Sales Tax Receivable.</span></span>

<span data-ttu-id="00a90-141">V následujícím diagramu je pravidlo znázorněno graficky.</span><span class="sxs-lookup"><span data-stu-id="00a90-141">The following diagram illustrates the rule graphically.</span></span>

![Možnosti daňových směrů pro účty zákazníka](media/Sales-Tax-Direction-Customer.jpg)

### <a name="account-type-is-ledger"></a><span data-ttu-id="00a90-143">Typ účtu je Hlavní kniha</span><span class="sxs-lookup"><span data-stu-id="00a90-143">Account type is Ledger</span></span>

<span data-ttu-id="00a90-144">Na následujícím obrázku je znázorněno pravidlo, které platí, pokud má doklad pouze řádky deníku, u nichž je typem účtu **Hlavní kniha**.</span><span class="sxs-lookup"><span data-stu-id="00a90-144">The following illustration shows the rule that applies when a voucher has only journal lines where the account type is **Ledger**.</span></span> <span data-ttu-id="00a90-145">Následující body znázorňují možné daňové pokyny pro účty hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="00a90-145">The following points show the possible tax directions for ledger accounts.</span></span>

<span data-ttu-id="00a90-146">•   Pokud je kód DPH importní DPH, je směr DPH Importní DPH.</span><span class="sxs-lookup"><span data-stu-id="00a90-146">•   If the sales tax code is use tax, then sales tax direction is Use Tax.</span></span>

<span data-ttu-id="00a90-147">•   Pokud je kód DPH Osvobození od daně, je směr Nákup bez daně.</span><span class="sxs-lookup"><span data-stu-id="00a90-147">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="00a90-148">V opačném případě, je-li částka v deníku debetní (kladná), směr DPH je Pohledávka DPH; Pokud je částka deníku kreditní (záporná), směr DPH je Splatná DPH.</span><span class="sxs-lookup"><span data-stu-id="00a90-148">Otherwise, if the journal amount is debit (positive) ,sales tax direction is Sales Tax Receivable; if the journal amount is credit (negative) ,sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="00a90-149">V následujícím diagramu je pravidlo znázorněno graficky.</span><span class="sxs-lookup"><span data-stu-id="00a90-149">The following diagram illustrates the rule graphically.</span></span>

![Možnosti daňových směrů pro účty hlavní knihy](media/Sales-Tax-Direction-Ledger.jpg)

#### <a name="override-the-sales-tax-direction"></a><span data-ttu-id="00a90-151">Přepis směru DPH</span><span class="sxs-lookup"><span data-stu-id="00a90-151">Override the sales tax direction</span></span>

<span data-ttu-id="00a90-152">Směr DPH lze přepsat, pokud doklad obsahuje pouze řádky s typem účtu **hlavní kniha**.</span><span class="sxs-lookup"><span data-stu-id="00a90-152">You can override the sales tax direction when the voucher contains only lines where the account type is **Ledger**.</span></span>

<span data-ttu-id="00a90-153">Přejděte na **Hlavní kniha \> Účtová osnova \> Účty \> Hlavní účty** a vyberte pevnou záložku **Přepisy právnické osoby**.</span><span class="sxs-lookup"><span data-stu-id="00a90-153">Go to **General ledger \> Chart of accounts \> Accounts \> Main accounts**, and select the **Legal entity overrides** FastTab.</span></span>

## <a name="determine-the-sales-tax-amount"></a><span data-ttu-id="00a90-154">Určení částky DPH</span><span class="sxs-lookup"><span data-stu-id="00a90-154">Determine the sales tax amount</span></span>

<span data-ttu-id="00a90-155">Tento oddíl popisuje, jak se vypočítává znak částky DPH.</span><span class="sxs-lookup"><span data-stu-id="00a90-155">This section describes how the sales tax amount sign is calculated.</span></span>

![Stránka transakce DPH](media/sales-tax-amount-sign.jpg)

<span data-ttu-id="00a90-157">V následující tabulce je uvedeno obecné pravidlo pro určení znaménka částek DPH v dočasné tabulce DPH.</span><span class="sxs-lookup"><span data-stu-id="00a90-157">The following table shows the generic rule for determining the sign of sales tax amounts in the temporary sales tax table.</span></span>

| <span data-ttu-id="00a90-158">Částka řádky deníku</span><span class="sxs-lookup"><span data-stu-id="00a90-158">Journal line amount</span></span> | <span data-ttu-id="00a90-159">Směr DPH</span><span class="sxs-lookup"><span data-stu-id="00a90-159">Sales tax direction</span></span>  | <span data-ttu-id="00a90-160">Znak částky DPH</span><span class="sxs-lookup"><span data-stu-id="00a90-160">Sales tax amount sign</span></span> |
|---------------------|----------------------|-----------------------|
| <span data-ttu-id="00a90-161">Kladné</span><span class="sxs-lookup"><span data-stu-id="00a90-161">Positive</span></span>            | <span data-ttu-id="00a90-162">Pohledávky DPH</span><span class="sxs-lookup"><span data-stu-id="00a90-162">Sales Tax Receivable</span></span> | <span data-ttu-id="00a90-163">Kladné</span><span class="sxs-lookup"><span data-stu-id="00a90-163">Positive</span></span>              |
| <span data-ttu-id="00a90-164">Kladné</span><span class="sxs-lookup"><span data-stu-id="00a90-164">Positive</span></span>            | <span data-ttu-id="00a90-165">Splatná DPH</span><span class="sxs-lookup"><span data-stu-id="00a90-165">Sales Tax Payable</span></span>    | <span data-ttu-id="00a90-166">Záporné</span><span class="sxs-lookup"><span data-stu-id="00a90-166">Negative</span></span>              |
| <span data-ttu-id="00a90-167">Záporné</span><span class="sxs-lookup"><span data-stu-id="00a90-167">Negative</span></span>            | <span data-ttu-id="00a90-168">Pohledávky DPH</span><span class="sxs-lookup"><span data-stu-id="00a90-168">Sales Tax Receivable</span></span> | <span data-ttu-id="00a90-169">Záporné</span><span class="sxs-lookup"><span data-stu-id="00a90-169">Negative</span></span>              |
| <span data-ttu-id="00a90-170">Záporné</span><span class="sxs-lookup"><span data-stu-id="00a90-170">Negative</span></span>            | <span data-ttu-id="00a90-171">Splatná DPH</span><span class="sxs-lookup"><span data-stu-id="00a90-171">Sales Tax Payable</span></span>    | <span data-ttu-id="00a90-172">Kladné</span><span class="sxs-lookup"><span data-stu-id="00a90-172">Positive</span></span>              |

<span data-ttu-id="00a90-173">Pro doklady, které mají pouze řádky **Projekt** nebo **Hlavní kniha**, existuje zvláštní pravidlo, když je na řádku **Hlavní kniha** vybrána skupina DPH nebo skupina DPH položky.</span><span class="sxs-lookup"><span data-stu-id="00a90-173">There is a special rule for vouchers that have only **Project** or **Ledger** lines, when a sales tax group or item sales tax group is selected on the **Ledger** line.</span></span> <span data-ttu-id="00a90-174">Toto pravidlo je řízeno povolením funkce nezávislého výpočtu DPH pro hlavní deníky.</span><span class="sxs-lookup"><span data-stu-id="00a90-174">This rule is controlled by Enable independent sales tax calculation feature for general journals.</span></span> <span data-ttu-id="00a90-175">Když je tato funkce vypnutá, částka daně na řádku **hlavní knihy** použije stranu má dáti/dal řádku **projektu**.</span><span class="sxs-lookup"><span data-stu-id="00a90-175">When this feature is turned off, the tax amount of the **Ledger** line uses the debit/credit direction of the **Project** line.</span></span> <span data-ttu-id="00a90-176">Když je tato funkce zapnutá, částka daně na řádku **hlavní knihy** použije vlastní směr má dáti/dal.</span><span class="sxs-lookup"><span data-stu-id="00a90-176">When the feature is turned on, the tax amount of the **Ledger** line uses its own debit/credit direction.</span></span> <span data-ttu-id="00a90-177">V následujících tabulkách jsou uvedena pravidla pro jednotlivé scénáře.</span><span class="sxs-lookup"><span data-stu-id="00a90-177">The following tables show the rule for each scenario.</span></span> 

<span data-ttu-id="00a90-178">**Pravidlo, když je funkce zapnutá**</span><span class="sxs-lookup"><span data-stu-id="00a90-178">**Rule when the feature is turned on**</span></span>

| <span data-ttu-id="00a90-179">Částka řádky deníku projektu</span><span class="sxs-lookup"><span data-stu-id="00a90-179">Journal line amount of project</span></span> | <span data-ttu-id="00a90-180">Směr DPH</span><span class="sxs-lookup"><span data-stu-id="00a90-180">Sales tax direction</span></span>  | <span data-ttu-id="00a90-181">Znak částky DPH</span><span class="sxs-lookup"><span data-stu-id="00a90-181">Sales tax amount sign</span></span> |
|--------------------------------|----------------------|-----------------------|
| <span data-ttu-id="00a90-182">Kladné</span><span class="sxs-lookup"><span data-stu-id="00a90-182">Positive</span></span>                       | <span data-ttu-id="00a90-183">Pohledávky DPH</span><span class="sxs-lookup"><span data-stu-id="00a90-183">Sales Tax Receivable</span></span> | <span data-ttu-id="00a90-184">Kladné</span><span class="sxs-lookup"><span data-stu-id="00a90-184">Positive</span></span>              |
| <span data-ttu-id="00a90-185">Záporné</span><span class="sxs-lookup"><span data-stu-id="00a90-185">Negative</span></span>                       | <span data-ttu-id="00a90-186">Pohledávky DPH</span><span class="sxs-lookup"><span data-stu-id="00a90-186">Sales Tax Receivable</span></span> | <span data-ttu-id="00a90-187">Záporné</span><span class="sxs-lookup"><span data-stu-id="00a90-187">Negative</span></span>              |

<span data-ttu-id="00a90-188">**Pravidlo, když je funkce vypnutá**</span><span class="sxs-lookup"><span data-stu-id="00a90-188">**Rule when the feature is turned off**</span></span>

| <span data-ttu-id="00a90-189">Částka řádky deníku hlavní knihy</span><span class="sxs-lookup"><span data-stu-id="00a90-189">Journal line amount of ledger</span></span>  | <span data-ttu-id="00a90-190">Směr DPH</span><span class="sxs-lookup"><span data-stu-id="00a90-190">Sales tax direction</span></span>  | <span data-ttu-id="00a90-191">Znak částky DPH</span><span class="sxs-lookup"><span data-stu-id="00a90-191">Sales tax amount sign</span></span> |
|--------------------------------|----------------------|-----------------------|
| <span data-ttu-id="00a90-192">Kladné</span><span class="sxs-lookup"><span data-stu-id="00a90-192">Positive</span></span>                       | <span data-ttu-id="00a90-193">Pohledávky DPH</span><span class="sxs-lookup"><span data-stu-id="00a90-193">Sales Tax Receivable</span></span> | <span data-ttu-id="00a90-194">Kladné</span><span class="sxs-lookup"><span data-stu-id="00a90-194">Positive</span></span>              |
| <span data-ttu-id="00a90-195">Záporné</span><span class="sxs-lookup"><span data-stu-id="00a90-195">Negative</span></span>                       | <span data-ttu-id="00a90-196">Pohledávky DPH</span><span class="sxs-lookup"><span data-stu-id="00a90-196">Sales Tax Receivable</span></span> | <span data-ttu-id="00a90-197">Záporné</span><span class="sxs-lookup"><span data-stu-id="00a90-197">Negative</span></span>              |

## <a name="determine-the-sales-tax-amount-and-account-on-the-voucher"></a><span data-ttu-id="00a90-198">Určete částku DPH a účet na dokladu</span><span class="sxs-lookup"><span data-stu-id="00a90-198">Determine the sales tax amount and account on the voucher</span></span>

<span data-ttu-id="00a90-199">Při zaúčtování DPH se hlavní účet načte z profilu účetní skupiny hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="00a90-199">When you post sales taxes, the main account is retrieved from the ledger posting group profile.</span></span> <span data-ttu-id="00a90-200">Pokud jsou DPH pohledávky, systém použije účet pohledávek DPH, který je uveden v profilu.</span><span class="sxs-lookup"><span data-stu-id="00a90-200">When sales taxes are receivable, the system uses the Sales Tax Receivable account that is specified in the profile.</span></span> <span data-ttu-id="00a90-201">Pokud jsou DPH splatné, systém použije účet splatné DPH, který je uveden v profilu.</span><span class="sxs-lookup"><span data-stu-id="00a90-201">For sales taxes that are payable, the system uses Sales Tax Payable account that is specified in the profile.</span></span>

<span data-ttu-id="00a90-202">Následující tabulka zobrazuje obecné pravidlo.</span><span class="sxs-lookup"><span data-stu-id="00a90-202">The following table shows the generic rule.</span></span>

| <span data-ttu-id="00a90-203">Směr DPH</span><span class="sxs-lookup"><span data-stu-id="00a90-203">Sales tax direction</span></span>  | <span data-ttu-id="00a90-204">Znak částky DPH</span><span class="sxs-lookup"><span data-stu-id="00a90-204">Sales tax amount sign</span></span> | <span data-ttu-id="00a90-205">Účet DPH</span><span class="sxs-lookup"><span data-stu-id="00a90-205">Sales tax account</span></span>      | <span data-ttu-id="00a90-206">Částka na dokladu</span><span class="sxs-lookup"><span data-stu-id="00a90-206">Amount on voucher</span></span> |
|----------------------|-----------------------|------------------------|-------------------|
| <span data-ttu-id="00a90-207">Pohledávky DPH</span><span class="sxs-lookup"><span data-stu-id="00a90-207">Sales Tax Receivable</span></span> | <span data-ttu-id="00a90-208">Kladné</span><span class="sxs-lookup"><span data-stu-id="00a90-208">Positive</span></span>              | <span data-ttu-id="00a90-209">Účet pohledávek</span><span class="sxs-lookup"><span data-stu-id="00a90-209">Tax Receivable Account</span></span> | <span data-ttu-id="00a90-210">Kladný (debet)</span><span class="sxs-lookup"><span data-stu-id="00a90-210">Positive (Debit)</span></span>  |
| <span data-ttu-id="00a90-211">Pohledávky DPH</span><span class="sxs-lookup"><span data-stu-id="00a90-211">Sales Tax Receivable</span></span> | <span data-ttu-id="00a90-212">Záporné</span><span class="sxs-lookup"><span data-stu-id="00a90-212">Negative</span></span>              | <span data-ttu-id="00a90-213">Účet pohledávek</span><span class="sxs-lookup"><span data-stu-id="00a90-213">Tax Receivable Account</span></span> | <span data-ttu-id="00a90-214">Záporné (dal)</span><span class="sxs-lookup"><span data-stu-id="00a90-214">Negative(Credit)</span></span>  |
| <span data-ttu-id="00a90-215">Splatná DPH</span><span class="sxs-lookup"><span data-stu-id="00a90-215">Sales Tax Payable</span></span>    | <span data-ttu-id="00a90-216">Kladné</span><span class="sxs-lookup"><span data-stu-id="00a90-216">Positive</span></span>              | <span data-ttu-id="00a90-217">Účet závazků</span><span class="sxs-lookup"><span data-stu-id="00a90-217">Tax Payable Account</span></span>    | <span data-ttu-id="00a90-218">Záporné (dal)</span><span class="sxs-lookup"><span data-stu-id="00a90-218">Negative(Credit)</span></span>  |
| <span data-ttu-id="00a90-219">Splatná DPH</span><span class="sxs-lookup"><span data-stu-id="00a90-219">Sales Tax Payable</span></span>    | <span data-ttu-id="00a90-220">Záporné</span><span class="sxs-lookup"><span data-stu-id="00a90-220">Negative</span></span>              | <span data-ttu-id="00a90-221">Účet závazků</span><span class="sxs-lookup"><span data-stu-id="00a90-221">Tax Payable Account</span></span>    | <span data-ttu-id="00a90-222">Kladný (debet)</span><span class="sxs-lookup"><span data-stu-id="00a90-222">Positive (Debit)</span></span>  |
