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
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2019-08-14
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: e420632c248b5b43d4983c5eb483cac580e67f20
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4975551"
---
# <a name="sales-tax-calculation-on-general-journal-lines"></a><span data-ttu-id="58b81-103">Výpočet DPH na řádcích hlavního deníku</span><span class="sxs-lookup"><span data-stu-id="58b81-103">Sales tax calculation on general journal lines</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="58b81-104">V tomto tématu je vysvětleno, jak se počítá DPH pro různé typy účtů (dodavatel, odběratel, hlavní kniha a projekt) na řádcích hlavního deníku.</span><span class="sxs-lookup"><span data-stu-id="58b81-104">This topic explains how sales taxes are calculated for different types of accounts (vendor, customer, ledger, and project) on general journal lines.</span></span>

<span data-ttu-id="58b81-105">Tento proces lze rozdělit do tří kroků:</span><span class="sxs-lookup"><span data-stu-id="58b81-105">The process can be divided into three steps:</span></span>

- <span data-ttu-id="58b81-106">Určete směr DPH.</span><span class="sxs-lookup"><span data-stu-id="58b81-106">Determine the sales tax direction.</span></span>

- <span data-ttu-id="58b81-107">Určete částku DPH, která bude uložena jako dočasná tabulka DPH.</span><span class="sxs-lookup"><span data-stu-id="58b81-107">Determine the sales tax amount that will be stored a temporary sales tax table.</span></span>

- <span data-ttu-id="58b81-108">Určete částku DPH a účet na dokladu.</span><span class="sxs-lookup"><span data-stu-id="58b81-108">Determine the sales tax amount and account on the voucher.</span></span>

## <a name="determine-the-sales-tax-direction"></a><span data-ttu-id="58b81-109">Určení směru DPH</span><span class="sxs-lookup"><span data-stu-id="58b81-109">Determine the sales tax direction</span></span>

<span data-ttu-id="58b81-110">Způsob, jakým je určen směr DPH, závisí na typu účtu v dokladu.</span><span class="sxs-lookup"><span data-stu-id="58b81-110">The way that the sales tax direction is determined depends on the type of account in the voucher.</span></span> <span data-ttu-id="58b81-111">Směr DPH je určen kombinací typu účtu a kódu DPH.</span><span class="sxs-lookup"><span data-stu-id="58b81-111">The sales tax direction is determined by the combination of account type and sales tax code.</span></span> <span data-ttu-id="58b81-112">V následujících oddílech jsou uvedeny podrobnosti o možnostech.</span><span class="sxs-lookup"><span data-stu-id="58b81-112">The following sections the possibilities in more detail.</span></span> 

### <a name="account-type-is-project"></a><span data-ttu-id="58b81-113">Typ účtu je Projekt.</span><span class="sxs-lookup"><span data-stu-id="58b81-113">Account type is Project</span></span>

<span data-ttu-id="58b81-114">Pokud má doklad řádek deníku, u kterého je typ účtu **Projekt**, budou všechny řádky deníku v dokladu používat stejný směr DPH.</span><span class="sxs-lookup"><span data-stu-id="58b81-114">If a voucher has journal line where the account type is **Project**, all the journal lines in the voucher apply the same tax direction.</span></span> <span data-ttu-id="58b81-115">Následující obrázek znázorňuje pravidlo.</span><span class="sxs-lookup"><span data-stu-id="58b81-115">The following illustration shows the rule.</span></span> <span data-ttu-id="58b81-116">Následující body znázorňují možné daňové pokyny pro účty projektu.</span><span class="sxs-lookup"><span data-stu-id="58b81-116">The following points show the possible tax directions for project accounts.</span></span>

<span data-ttu-id="58b81-117">•   Pokud je kód DPH importní DPH, je směr DPH Importní DPH.</span><span class="sxs-lookup"><span data-stu-id="58b81-117">•   If the sales tax code is use tax, then sales tax direction is Use Tax.</span></span>

<span data-ttu-id="58b81-118">•   Pokud je kód DPH Osvobození od daně, je směr Nákup bez daně.</span><span class="sxs-lookup"><span data-stu-id="58b81-118">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="58b81-119">•   Pokud je kód DPH vnitřní DPH, je směr DPH Splatná DPH.</span><span class="sxs-lookup"><span data-stu-id="58b81-119">•   If the sales tax code is intracom VAT, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="58b81-120">•   Pokud je kód DPH stornované účtování, je směr DPH Splatná DPH.</span><span class="sxs-lookup"><span data-stu-id="58b81-120">•   If the sales tax code is reverse charge, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="58b81-121">V opačném případě je směr DPH pohledávka DPH.</span><span class="sxs-lookup"><span data-stu-id="58b81-121">Otherwise, sales tax direction is Sales Tax Receivable.</span></span>

<span data-ttu-id="58b81-122">V následujícím diagramu je pravidlo znázorněno graficky.</span><span class="sxs-lookup"><span data-stu-id="58b81-122">The following diagram illustrates the rule graphically.</span></span>

![Možnosti daňových směrů pro účty projektu](media/Sales-Tax-Direction-Vendor.jpg)

### <a name="account-type-is-vendor"></a><span data-ttu-id="58b81-124">Typ účtu je Dodavatel</span><span class="sxs-lookup"><span data-stu-id="58b81-124">Account type is Vendor</span></span>

<span data-ttu-id="58b81-125">Pokud má doklad řádek deníku, u kterého je typ účtu **Dodavatel**, budou všechny řádky deníku v dokladu používat stejný směr DPH.</span><span class="sxs-lookup"><span data-stu-id="58b81-125">If a voucher has journal line where the account type is **Vendor**, all the journal lines in the voucher apply the same tax direction.</span></span> <span data-ttu-id="58b81-126">Následující body znázorňují možné daňové pokyny pro účty dodavatele.</span><span class="sxs-lookup"><span data-stu-id="58b81-126">The following points show the possible tax directions for vendor accounts.</span></span> 

<span data-ttu-id="58b81-127">•   Pokud je kód DPH importní DPH, je směr DPH Importní DPH.</span><span class="sxs-lookup"><span data-stu-id="58b81-127">•   If the sales tax code is use tax, then sales tax direction is Use Tax.</span></span>

<span data-ttu-id="58b81-128">•   Pokud je kód DPH Osvobození od daně, je směr Nákup bez daně.</span><span class="sxs-lookup"><span data-stu-id="58b81-128">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="58b81-129">•   Pokud je kód DPH vnitřní DPH, je směr DPH Splatná DPH.</span><span class="sxs-lookup"><span data-stu-id="58b81-129">•   If the sales tax code is intracom VAT, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="58b81-130">•   Pokud je kód DPH stornované účtování, je směr DPH Splatná DPH.</span><span class="sxs-lookup"><span data-stu-id="58b81-130">•   If the sales tax code is reverse charge, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="58b81-131">V opačném případě je směr DPH pohledávka DPH.</span><span class="sxs-lookup"><span data-stu-id="58b81-131">Otherwise, sales tax direction is Sales Tax Receivable.</span></span>

<span data-ttu-id="58b81-132">V následujícím diagramu je pravidlo znázorněno graficky.</span><span class="sxs-lookup"><span data-stu-id="58b81-132">The following diagram illustrates the rule graphically.</span></span>

![Možnosti daňových směrů pro účty dodavatele](media/Sales-Tax-Direction-Vendor.jpg)

### <a name="account-type-is-customer"></a><span data-ttu-id="58b81-134">Typ účtu je Zákazník.</span><span class="sxs-lookup"><span data-stu-id="58b81-134">Account type is Customer</span></span>

<span data-ttu-id="58b81-135">Pokud má doklad řádek deníku, u kterého je typ účtu **Zákazník**, budou všechny řádky deníku v dokladu používat stejný směr DPH.</span><span class="sxs-lookup"><span data-stu-id="58b81-135">If a voucher has journal line where the account type is **Customer**, all the journal lines in the voucher apply the same tax direction.</span></span> <span data-ttu-id="58b81-136">Následující body znázorňují možné daňové pokyny pro účty zákazníka.</span><span class="sxs-lookup"><span data-stu-id="58b81-136">The following points show the possible tax directions for customer accounts.</span></span>

<span data-ttu-id="58b81-137">•   Pokud je kód DPH Osvobození od daně, je směr Nákup bez daně.</span><span class="sxs-lookup"><span data-stu-id="58b81-137">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="58b81-138">•   Pokud je kód DPH vnitřní DPH, je směr DPH Pohledávka DPH.</span><span class="sxs-lookup"><span data-stu-id="58b81-138">•   If the sales tax code is intracom VAT, then sales tax direction is Sales Tax Receivable.</span></span>

<span data-ttu-id="58b81-139">•   Pokud je kód DPH stornované účtování, je směr DPH Pohledávka DPH.</span><span class="sxs-lookup"><span data-stu-id="58b81-139">•   If the sales tax code is reverse charge, then sales tax direction is Sales Tax Receivable.</span></span>

<span data-ttu-id="58b81-140">V opačném případě je směr DPH Splatná DPH.</span><span class="sxs-lookup"><span data-stu-id="58b81-140">Otherwise, sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="58b81-141">V následujícím diagramu je pravidlo znázorněno graficky.</span><span class="sxs-lookup"><span data-stu-id="58b81-141">The following diagram illustrates the rule graphically.</span></span>

![Možnosti daňových směrů pro účty zákazníka](media/Sales-Tax-Direction-Customer.jpg)

### <a name="account-type-is-ledger"></a><span data-ttu-id="58b81-143">Typ účtu je Hlavní kniha</span><span class="sxs-lookup"><span data-stu-id="58b81-143">Account type is Ledger</span></span>

<span data-ttu-id="58b81-144">Na následujícím obrázku je znázorněno pravidlo, které platí, pokud má doklad pouze řádky deníku, u nichž je typem účtu **Hlavní kniha**.</span><span class="sxs-lookup"><span data-stu-id="58b81-144">The following illustration shows the rule that applies when a voucher has only journal lines where the account type is **Ledger**.</span></span> <span data-ttu-id="58b81-145">Následující body znázorňují možné daňové pokyny pro účty hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="58b81-145">The following points show the possible tax directions for ledger accounts.</span></span>

<span data-ttu-id="58b81-146">•   Pokud je kód DPH importní DPH, je směr DPH Importní DPH.</span><span class="sxs-lookup"><span data-stu-id="58b81-146">•   If the sales tax code is use tax, then sales tax direction is Use Tax.</span></span>

<span data-ttu-id="58b81-147">•   Pokud je kód DPH Osvobození od daně, je směr Nákup bez daně.</span><span class="sxs-lookup"><span data-stu-id="58b81-147">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="58b81-148">V opačném případě, je-li částka v deníku debetní (kladná), směr DPH je Pohledávka DPH; Pokud je částka deníku kreditní (záporná), směr DPH je Splatná DPH.</span><span class="sxs-lookup"><span data-stu-id="58b81-148">Otherwise, if the journal amount is debit (positive) ,sales tax direction is Sales Tax Receivable; if the journal amount is credit (negative) ,sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="58b81-149">V následujícím diagramu je pravidlo znázorněno graficky.</span><span class="sxs-lookup"><span data-stu-id="58b81-149">The following diagram illustrates the rule graphically.</span></span>

![Možnosti daňových směrů pro účty hlavní knihy](media/Sales-Tax-Direction-Ledger.jpg)

#### <a name="override-the-sales-tax-direction"></a><span data-ttu-id="58b81-151">Přepis směru DPH</span><span class="sxs-lookup"><span data-stu-id="58b81-151">Override the sales tax direction</span></span>

<span data-ttu-id="58b81-152">Směr DPH lze přepsat, pokud doklad obsahuje pouze řádky s typem účtu **hlavní kniha**.</span><span class="sxs-lookup"><span data-stu-id="58b81-152">You can override the sales tax direction when the voucher contains only lines where the account type is **Ledger**.</span></span>

<span data-ttu-id="58b81-153">Přejděte na **Hlavní kniha \> Účtová osnova \> Účty \> Hlavní účty** a vyberte pevnou záložku **Přepisy právnické osoby**.</span><span class="sxs-lookup"><span data-stu-id="58b81-153">Go to **General ledger \> Chart of accounts \> Accounts \> Main accounts**, and select the **Legal entity overrides** FastTab.</span></span>

## <a name="determine-the-sales-tax-amount"></a><span data-ttu-id="58b81-154">Určení částky DPH</span><span class="sxs-lookup"><span data-stu-id="58b81-154">Determine the sales tax amount</span></span>

<span data-ttu-id="58b81-155">Tento oddíl popisuje, jak se vypočítává znak částky DPH.</span><span class="sxs-lookup"><span data-stu-id="58b81-155">This section describes how the sales tax amount sign is calculated.</span></span>

![Stránka transakce DPH](media/sales-tax-amount-sign.jpg)

<span data-ttu-id="58b81-157">V následující tabulce je uvedeno obecné pravidlo pro určení znaménka částek DPH v dočasné tabulce DPH.</span><span class="sxs-lookup"><span data-stu-id="58b81-157">The following table shows the generic rule for determining the sign of sales tax amounts in the temporary sales tax table.</span></span>

| <span data-ttu-id="58b81-158">Částka řádky deníku</span><span class="sxs-lookup"><span data-stu-id="58b81-158">Journal line amount</span></span> | <span data-ttu-id="58b81-159">Směr DPH</span><span class="sxs-lookup"><span data-stu-id="58b81-159">Sales tax direction</span></span>  | <span data-ttu-id="58b81-160">Znak částky DPH</span><span class="sxs-lookup"><span data-stu-id="58b81-160">Sales tax amount sign</span></span> |
|---------------------|----------------------|-----------------------|
| <span data-ttu-id="58b81-161">Kladné</span><span class="sxs-lookup"><span data-stu-id="58b81-161">Positive</span></span>            | <span data-ttu-id="58b81-162">Pohledávky DPH</span><span class="sxs-lookup"><span data-stu-id="58b81-162">Sales Tax Receivable</span></span> | <span data-ttu-id="58b81-163">Kladné</span><span class="sxs-lookup"><span data-stu-id="58b81-163">Positive</span></span>              |
| <span data-ttu-id="58b81-164">Kladné</span><span class="sxs-lookup"><span data-stu-id="58b81-164">Positive</span></span>            | <span data-ttu-id="58b81-165">Splatná DPH</span><span class="sxs-lookup"><span data-stu-id="58b81-165">Sales Tax Payable</span></span>    | <span data-ttu-id="58b81-166">Záporné</span><span class="sxs-lookup"><span data-stu-id="58b81-166">Negative</span></span>              |
| <span data-ttu-id="58b81-167">Záporné</span><span class="sxs-lookup"><span data-stu-id="58b81-167">Negative</span></span>            | <span data-ttu-id="58b81-168">Pohledávky DPH</span><span class="sxs-lookup"><span data-stu-id="58b81-168">Sales Tax Receivable</span></span> | <span data-ttu-id="58b81-169">Záporné</span><span class="sxs-lookup"><span data-stu-id="58b81-169">Negative</span></span>              |
| <span data-ttu-id="58b81-170">Záporné</span><span class="sxs-lookup"><span data-stu-id="58b81-170">Negative</span></span>            | <span data-ttu-id="58b81-171">Splatná DPH</span><span class="sxs-lookup"><span data-stu-id="58b81-171">Sales Tax Payable</span></span>    | <span data-ttu-id="58b81-172">Kladné</span><span class="sxs-lookup"><span data-stu-id="58b81-172">Positive</span></span>              |

<span data-ttu-id="58b81-173">Pro doklady, které mají pouze řádky **Projekt** nebo **Hlavní kniha**, existuje zvláštní pravidlo, když je na řádku **Hlavní kniha** vybrána skupina DPH nebo skupina DPH položky.</span><span class="sxs-lookup"><span data-stu-id="58b81-173">There is a special rule for vouchers that have only **Project** or **Ledger** lines, when a sales tax group or item sales tax group is selected on the **Ledger** line.</span></span> <span data-ttu-id="58b81-174">Toto pravidlo je řízeno povolením funkce nezávislého výpočtu DPH pro hlavní deníky.</span><span class="sxs-lookup"><span data-stu-id="58b81-174">This rule is controlled by Enable independent sales tax calculation feature for general journals.</span></span> <span data-ttu-id="58b81-175">Když je tato funkce vypnutá, částka daně na řádku **hlavní knihy** použije stranu má dáti/dal řádku **projektu**.</span><span class="sxs-lookup"><span data-stu-id="58b81-175">When this feature is turned off, the tax amount of the **Ledger** line uses the debit/credit direction of the **Project** line.</span></span> <span data-ttu-id="58b81-176">Když je tato funkce zapnutá, částka daně na řádku **hlavní knihy** použije vlastní směr má dáti/dal.</span><span class="sxs-lookup"><span data-stu-id="58b81-176">When the feature is turned on, the tax amount of the **Ledger** line uses its own debit/credit direction.</span></span> <span data-ttu-id="58b81-177">V následujících tabulkách jsou uvedena pravidla pro jednotlivé scénáře.</span><span class="sxs-lookup"><span data-stu-id="58b81-177">The following tables show the rule for each scenario.</span></span> 

<span data-ttu-id="58b81-178">**Pravidlo, když je funkce zapnutá**</span><span class="sxs-lookup"><span data-stu-id="58b81-178">**Rule when the feature is turned on**</span></span>

| <span data-ttu-id="58b81-179">Částka řádky deníku projektu</span><span class="sxs-lookup"><span data-stu-id="58b81-179">Journal line amount of project</span></span> | <span data-ttu-id="58b81-180">Směr DPH</span><span class="sxs-lookup"><span data-stu-id="58b81-180">Sales tax direction</span></span>  | <span data-ttu-id="58b81-181">Znak částky DPH</span><span class="sxs-lookup"><span data-stu-id="58b81-181">Sales tax amount sign</span></span> |
|--------------------------------|----------------------|-----------------------|
| <span data-ttu-id="58b81-182">Kladné</span><span class="sxs-lookup"><span data-stu-id="58b81-182">Positive</span></span>                       | <span data-ttu-id="58b81-183">Pohledávky DPH</span><span class="sxs-lookup"><span data-stu-id="58b81-183">Sales Tax Receivable</span></span> | <span data-ttu-id="58b81-184">Kladné</span><span class="sxs-lookup"><span data-stu-id="58b81-184">Positive</span></span>              |
| <span data-ttu-id="58b81-185">Záporné</span><span class="sxs-lookup"><span data-stu-id="58b81-185">Negative</span></span>                       | <span data-ttu-id="58b81-186">Pohledávky DPH</span><span class="sxs-lookup"><span data-stu-id="58b81-186">Sales Tax Receivable</span></span> | <span data-ttu-id="58b81-187">Záporné</span><span class="sxs-lookup"><span data-stu-id="58b81-187">Negative</span></span>              |

<span data-ttu-id="58b81-188">**Pravidlo, když je funkce vypnutá**</span><span class="sxs-lookup"><span data-stu-id="58b81-188">**Rule when the feature is turned off**</span></span>

| <span data-ttu-id="58b81-189">Částka řádky deníku hlavní knihy</span><span class="sxs-lookup"><span data-stu-id="58b81-189">Journal line amount of ledger</span></span>  | <span data-ttu-id="58b81-190">Směr DPH</span><span class="sxs-lookup"><span data-stu-id="58b81-190">Sales tax direction</span></span>  | <span data-ttu-id="58b81-191">Znak částky DPH</span><span class="sxs-lookup"><span data-stu-id="58b81-191">Sales tax amount sign</span></span> |
|--------------------------------|----------------------|-----------------------|
| <span data-ttu-id="58b81-192">Kladné</span><span class="sxs-lookup"><span data-stu-id="58b81-192">Positive</span></span>                       | <span data-ttu-id="58b81-193">Pohledávky DPH</span><span class="sxs-lookup"><span data-stu-id="58b81-193">Sales Tax Receivable</span></span> | <span data-ttu-id="58b81-194">Kladné</span><span class="sxs-lookup"><span data-stu-id="58b81-194">Positive</span></span>              |
| <span data-ttu-id="58b81-195">Záporné</span><span class="sxs-lookup"><span data-stu-id="58b81-195">Negative</span></span>                       | <span data-ttu-id="58b81-196">Pohledávky DPH</span><span class="sxs-lookup"><span data-stu-id="58b81-196">Sales Tax Receivable</span></span> | <span data-ttu-id="58b81-197">Záporné</span><span class="sxs-lookup"><span data-stu-id="58b81-197">Negative</span></span>              |

## <a name="determine-the-sales-tax-amount-and-account-on-the-voucher"></a><span data-ttu-id="58b81-198">Určete částku DPH a účet na dokladu</span><span class="sxs-lookup"><span data-stu-id="58b81-198">Determine the sales tax amount and account on the voucher</span></span>

<span data-ttu-id="58b81-199">Při zaúčtování DPH se hlavní účet načte z profilu účetní skupiny hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="58b81-199">When you post sales taxes, the main account is retrieved from the ledger posting group profile.</span></span> <span data-ttu-id="58b81-200">Pokud jsou DPH pohledávky, systém použije účet pohledávek DPH, který je uveden v profilu.</span><span class="sxs-lookup"><span data-stu-id="58b81-200">When sales taxes are receivable, the system uses the Sales Tax Receivable account that is specified in the profile.</span></span> <span data-ttu-id="58b81-201">Pokud jsou DPH splatné, systém použije účet splatné DPH, který je uveden v profilu.</span><span class="sxs-lookup"><span data-stu-id="58b81-201">For sales taxes that are payable, the system uses Sales Tax Payable account that is specified in the profile.</span></span>

<span data-ttu-id="58b81-202">Následující tabulka zobrazuje obecné pravidlo.</span><span class="sxs-lookup"><span data-stu-id="58b81-202">The following table shows the generic rule.</span></span>

| <span data-ttu-id="58b81-203">Směr DPH</span><span class="sxs-lookup"><span data-stu-id="58b81-203">Sales tax direction</span></span>  | <span data-ttu-id="58b81-204">Znak částky DPH</span><span class="sxs-lookup"><span data-stu-id="58b81-204">Sales tax amount sign</span></span> | <span data-ttu-id="58b81-205">Účet DPH</span><span class="sxs-lookup"><span data-stu-id="58b81-205">Sales tax account</span></span>      | <span data-ttu-id="58b81-206">Částka na dokladu</span><span class="sxs-lookup"><span data-stu-id="58b81-206">Amount on voucher</span></span> |
|----------------------|-----------------------|------------------------|-------------------|
| <span data-ttu-id="58b81-207">Pohledávky DPH</span><span class="sxs-lookup"><span data-stu-id="58b81-207">Sales Tax Receivable</span></span> | <span data-ttu-id="58b81-208">Kladné</span><span class="sxs-lookup"><span data-stu-id="58b81-208">Positive</span></span>              | <span data-ttu-id="58b81-209">Účet pohledávek</span><span class="sxs-lookup"><span data-stu-id="58b81-209">Tax Receivable Account</span></span> | <span data-ttu-id="58b81-210">Kladný (debet)</span><span class="sxs-lookup"><span data-stu-id="58b81-210">Positive (Debit)</span></span>  |
| <span data-ttu-id="58b81-211">Pohledávky DPH</span><span class="sxs-lookup"><span data-stu-id="58b81-211">Sales Tax Receivable</span></span> | <span data-ttu-id="58b81-212">Záporné</span><span class="sxs-lookup"><span data-stu-id="58b81-212">Negative</span></span>              | <span data-ttu-id="58b81-213">Účet pohledávek</span><span class="sxs-lookup"><span data-stu-id="58b81-213">Tax Receivable Account</span></span> | <span data-ttu-id="58b81-214">Záporné (dal)</span><span class="sxs-lookup"><span data-stu-id="58b81-214">Negative(Credit)</span></span>  |
| <span data-ttu-id="58b81-215">Splatná DPH</span><span class="sxs-lookup"><span data-stu-id="58b81-215">Sales Tax Payable</span></span>    | <span data-ttu-id="58b81-216">Kladné</span><span class="sxs-lookup"><span data-stu-id="58b81-216">Positive</span></span>              | <span data-ttu-id="58b81-217">Účet závazků</span><span class="sxs-lookup"><span data-stu-id="58b81-217">Tax Payable Account</span></span>    | <span data-ttu-id="58b81-218">Záporné (dal)</span><span class="sxs-lookup"><span data-stu-id="58b81-218">Negative(Credit)</span></span>  |
| <span data-ttu-id="58b81-219">Splatná DPH</span><span class="sxs-lookup"><span data-stu-id="58b81-219">Sales Tax Payable</span></span>    | <span data-ttu-id="58b81-220">Záporné</span><span class="sxs-lookup"><span data-stu-id="58b81-220">Negative</span></span>              | <span data-ttu-id="58b81-221">Účet závazků</span><span class="sxs-lookup"><span data-stu-id="58b81-221">Tax Payable Account</span></span>    | <span data-ttu-id="58b81-222">Kladný (debet)</span><span class="sxs-lookup"><span data-stu-id="58b81-222">Positive (Debit)</span></span>  |
