---
title: Zadání počátečních zůstatků mezd
description: Toto téma popisuje postup při zadávání počátečních zůstatků pro kódy příjmů, srážky, odměny a daně. Tyto informace jsou důležité pro partnery při migraci nebo přenosu dat pro novou implementaci mezd z jiného systému.
author: andreabichsel
manager: AnnBe
ms.date: 11/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: 20931
ms.assetid: b48b1cb2-6e66-467e-9c0e-09b6a4aeb9fe
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 209636d6416a784d298bcfb134f5486c1f5cf202
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2021
ms.locfileid: "5568538"
---
# <a name="enter-payroll-beginning-balances"></a><span data-ttu-id="404a3-104">Zadání počátečních zůstatků mezd</span><span class="sxs-lookup"><span data-stu-id="404a3-104">Enter payroll beginning balances</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="404a3-105">Toto téma popisuje postup při zadávání počátečních zůstatků pro kódy příjmů, srážky, odměny a daně.</span><span class="sxs-lookup"><span data-stu-id="404a3-105">The topic describes the steps for entering beginning balances for earning codes, deductions, benefits, and taxes.</span></span> <span data-ttu-id="404a3-106">Tyto informace jsou důležité pro partnery, kteří přenášejí data pro novou implementaci mezd z jiného systému.</span><span class="sxs-lookup"><span data-stu-id="404a3-106">This information is valuable for partners who transfer data for a new Payroll implementation from another system.</span></span> <span data-ttu-id="404a3-107">V rámci přípravy na zadání počátečních zůstatků mezd ověřujeme následující údaje:</span><span class="sxs-lookup"><span data-stu-id="404a3-107">To prepare to enter beginning payroll balances, we verify the following information:</span></span>

- <span data-ttu-id="404a3-108">Záznamy zaměstnance jsou zadané a dostupné v systému.</span><span class="sxs-lookup"><span data-stu-id="404a3-108">Employee records are entered and available in the system</span></span>
- <span data-ttu-id="404a3-109">Následující údaje jsou nastaveny a přiřazeny zaměstnancům:</span><span class="sxs-lookup"><span data-stu-id="404a3-109">The following data is set up and assigned to employees:</span></span>

    - <span data-ttu-id="404a3-110">Platební cykly a platební období</span><span class="sxs-lookup"><span data-stu-id="404a3-110">Pay cycles and pay periods</span></span>
    - <span data-ttu-id="404a3-111">Kódy příjmů</span><span class="sxs-lookup"><span data-stu-id="404a3-111">Earning codes</span></span>
    - <span data-ttu-id="404a3-112">Daně</span><span class="sxs-lookup"><span data-stu-id="404a3-112">Taxes</span></span>
    - <span data-ttu-id="404a3-113">Výhody a srážky</span><span class="sxs-lookup"><span data-stu-id="404a3-113">Benefits and deductions</span></span>

- <span data-ttu-id="404a3-114">Společnost by měla zvolit datum, kdy lze nastavit počáteční zůstatky mezd.</span><span class="sxs-lookup"><span data-stu-id="404a3-114">The company should have chosen a date where payroll beginning balances can be set.</span></span>
- <span data-ttu-id="404a3-115">Informace byla získána na základě všech výdělků, zaměstnaneckých výhod / odpočtů, příspěvků na zaměstnanecké výhody, daní zaměstnanců a daních zaměstnavatelů a jejich částek od začátku roku ze zastaralého systému.</span><span class="sxs-lookup"><span data-stu-id="404a3-115">Information was gathered on all earnings, benefits/deductions, benefit contributions, employee taxes, and employer taxes and their YTD amounts from the legacy system.</span></span>

<span data-ttu-id="404a3-116">Při plánování zadávání počátečních zůstatků zvažte, jak podrobná mají data být.</span><span class="sxs-lookup"><span data-stu-id="404a3-116">As you plan to enter beginning balances, consider how detailed the data needs to be.</span></span> <span data-ttu-id="404a3-117">Většina firem zadává jednu konsolidovanou částku od začátku roku.</span><span class="sxs-lookup"><span data-stu-id="404a3-117">Most businesses enter a single, consolidated year-to-date amount.</span></span> <span data-ttu-id="404a3-118">Pokud jsou však potřeba podrobnější informace, lze zůstatky zadávat v přírůstcích po čtyřech.</span><span class="sxs-lookup"><span data-stu-id="404a3-118">However if more detailed information is needed, balances can be entered in quarterly increments.</span></span> <span data-ttu-id="404a3-119">Rozhodování o tom, jaká úroveň podrobností je potřeba, určuje, kolik ručních výkazů mezd musí být vytvořeno pro každého zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="404a3-119">Deciding the level of detail that's needed determines how many manual pay statements must be created for each worker.</span></span> <span data-ttu-id="404a3-120">U jednotlivé částky od začátku roku je potřeba pouze jeden ruční výkaz pro každého zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="404a3-120">For a single year-to-date amount, only one manual statement is needed for each employee.</span></span> <span data-ttu-id="404a3-121">K tomu použijte dosud realizované částky z výpisu konečné platby z předchozího systému jako částku zadanou do nového mzdového systému.</span><span class="sxs-lookup"><span data-stu-id="404a3-121">To do this, use year-to-date amounts from the final pay statement from the previous system as the amount entered in the new payroll system.</span></span>

<span data-ttu-id="404a3-122">Následující příklad ukazuje, jak zadat počáteční zůstatky mezd zaměstnance, včetně kódů příjmů, odměn odpočitatelných položek a daně.</span><span class="sxs-lookup"><span data-stu-id="404a3-122">The following example shows how you can enter employee payroll beginning balances, including earning codes, benefits/deductions, and taxes.</span></span> <span data-ttu-id="404a3-123">V praxi byste měli položku řádku pro každý kód příjmů, odpočtu na zaměstnanecké výhody, příspěvku na zaměstnaneckou výhodu, daně pro zaměstnance a zaměstnavatele s dosud zadanou částkou od začátku roku.</span><span class="sxs-lookup"><span data-stu-id="404a3-123">In a real-world example you would have a line item for each earning code, benefit deduction, benefit contribution, employee tax and employer tax with the amount entered being the year-to-date amount.</span></span> <span data-ttu-id="404a3-124">Pomocí tohoto seznamu kódů a částek postupujte podle pokynů pro vytvoření ručního výkazu příjmů a plateb s vypnutým účetnictvím pro přenesení počátečních zůstatků za účelem výpočtu mezd.</span><span class="sxs-lookup"><span data-stu-id="404a3-124">Using that list of codes and amounts, follow the steps for creating a manual earning and pay statement with accounting disabled to bring over beginning balances for payroll purposes.</span></span> <span data-ttu-id="404a3-125">Vzhledem k tomu, že nebudete chtít tento výkaz počátečního zůstatku zaúčtovat do hlavní knihy, zakážete účetnictví.</span><span class="sxs-lookup"><span data-stu-id="404a3-125">You disable accounting because you won't want to post this beginning balance pay statement to your general ledger.</span></span> <span data-ttu-id="404a3-126">Tak to probíhalo v zastaralém systému a bylo přeneseno do nového systému při nastavování počátečních zůstatků v hlavní knize.</span><span class="sxs-lookup"><span data-stu-id="404a3-126">That was done in the legacy system and will come over to the new system when you set beginning balances in General ledger.</span></span>

### <a name="a-how-to-set-up-earnings-codes-to-be-used-on-payroll-beginning-balances"></a><span data-ttu-id="404a3-127">A.</span><span class="sxs-lookup"><span data-stu-id="404a3-127">A.</span></span> <span data-ttu-id="404a3-128">Jak nastavit kódy příjmů pro použití v mzdovém systému počátečních zůstatků</span><span class="sxs-lookup"><span data-stu-id="404a3-128">How to set up earnings codes to be used on payroll beginning balances</span></span>

<span data-ttu-id="404a3-129">Pokud zadáváte počáteční zůstatky mezd, ujistěte se, že kódy příjmů, které budete používat, jsou nakonfigurovány s povolenou možností "Úpravy příjmů výkazu sazby".</span><span class="sxs-lookup"><span data-stu-id="404a3-129">When you enter payroll beginning balances, be sure the earning codes that you will be using are configured with the "Allow editing of earning statement rates" option enabled.</span></span> <span data-ttu-id="404a3-130">To vám umožní zadat ručně částku ze systému ze starší verze.</span><span class="sxs-lookup"><span data-stu-id="404a3-130">This will allow you to manually key the amount from the legacy system.</span></span> 

### <a name="b-create-earnings-statement-for-an-employee-to-have-a-beginning-balance"></a><span data-ttu-id="404a3-131">B.</span><span class="sxs-lookup"><span data-stu-id="404a3-131">B.</span></span> <span data-ttu-id="404a3-132">Vytvoření výkazu příjmů pro zaměstnance tak, aby obsahoval počáteční zůstatek</span><span class="sxs-lookup"><span data-stu-id="404a3-132">Create earnings statement for an employee to have a beginning balance</span></span>

<span data-ttu-id="404a3-133">Tento krok ručně vytvoří mzdový výkaz pro každého zaměstnance za poslední platební období v systému ze starší verze, což vytvoří řádky výkazu příjmů v novém mzdového systému.</span><span class="sxs-lookup"><span data-stu-id="404a3-133">This step manually creates an earnings statement for each worker for the last pay period of the legacy system, which creates the earning statement lines in the new payroll system.</span></span> <span data-ttu-id="404a3-134">Zadejte jeden řádek pro na kód příjmu a částku a hodiny od začátku roku.</span><span class="sxs-lookup"><span data-stu-id="404a3-134">Enter one line per earning code and the YTD amount and hours.</span></span> <span data-ttu-id="404a3-135">Ukázkové kroky:</span><span class="sxs-lookup"><span data-stu-id="404a3-135">The sample steps are as follows:</span></span>

1. <span data-ttu-id="404a3-136">Otevřete stránku **Výkazy všech příjmů** a klepněte na tlačítko **Nový**.</span><span class="sxs-lookup"><span data-stu-id="404a3-136">Open the **All earnings statements** page and click **New**.</span></span>

    <span data-ttu-id="404a3-137">Zadejte následující:</span><span class="sxs-lookup"><span data-stu-id="404a3-137">Enter the following:</span></span> 

    | <span data-ttu-id="404a3-138">Pole</span><span class="sxs-lookup"><span data-stu-id="404a3-138">Field</span></span>      | <span data-ttu-id="404a3-139">Hodnota</span><span class="sxs-lookup"><span data-stu-id="404a3-139">Value</span></span>                 |
    |------------|-----------------------|
    | <span data-ttu-id="404a3-140">Pracovní podproces</span><span class="sxs-lookup"><span data-stu-id="404a3-140">Worker</span></span>     | <span data-ttu-id="404a3-141">Michael Redmond</span><span class="sxs-lookup"><span data-stu-id="404a3-141">Michael Redmond</span></span>       |
    | <span data-ttu-id="404a3-142">Platební cyklus</span><span class="sxs-lookup"><span data-stu-id="404a3-142">Pay cycle</span></span>  | <span data-ttu-id="404a3-143">sm</span><span class="sxs-lookup"><span data-stu-id="404a3-143">sm</span></span>                    |
    | <span data-ttu-id="404a3-144">Mzdové období</span><span class="sxs-lookup"><span data-stu-id="404a3-144">Pay period</span></span> | <span data-ttu-id="404a3-145">6/16/2017 - 6/30/2017</span><span class="sxs-lookup"><span data-stu-id="404a3-145">6/16/2017 - 6/30/2017</span></span> |

2. <span data-ttu-id="404a3-146">Na kartě **Řádek výkazu příjmů** zadejte následující:</span><span class="sxs-lookup"><span data-stu-id="404a3-146">In the **Earnings statement line** tab, enter the following:</span></span>

    <span data-ttu-id="404a3-147">Řádek 1: karta **Řádek výkazu příjmů**</span><span class="sxs-lookup"><span data-stu-id="404a3-147">Line 1: **Earning statement line** tab</span></span>

    | <span data-ttu-id="404a3-148">Pole</span><span class="sxs-lookup"><span data-stu-id="404a3-148">Field</span></span>            | <span data-ttu-id="404a3-149">Hodnota</span><span class="sxs-lookup"><span data-stu-id="404a3-149">Value</span></span>       |
    |------------------|-------------|
    | <span data-ttu-id="404a3-150">Kód příjmů</span><span class="sxs-lookup"><span data-stu-id="404a3-150">Earnings code</span></span>    | <span data-ttu-id="404a3-151">Standardní mzda</span><span class="sxs-lookup"><span data-stu-id="404a3-151">Regular pay</span></span> |
    | <span data-ttu-id="404a3-152">Množství</span><span class="sxs-lookup"><span data-stu-id="404a3-152">Quantity</span></span>         | <span data-ttu-id="404a3-153">1.00</span><span class="sxs-lookup"><span data-stu-id="404a3-153">1.00</span></span>        |
    | <span data-ttu-id="404a3-154">Kurz</span><span class="sxs-lookup"><span data-stu-id="404a3-154">Rate</span></span>             | <span data-ttu-id="404a3-155">30,000</span><span class="sxs-lookup"><span data-stu-id="404a3-155">30,000</span></span>      |
    | <span data-ttu-id="404a3-156">Karta Detaily řádku</span><span class="sxs-lookup"><span data-stu-id="404a3-156">Line details tab</span></span> |             |
    | <span data-ttu-id="404a3-157">Ruční</span><span class="sxs-lookup"><span data-stu-id="404a3-157">Manual</span></span>           | <span data-ttu-id="404a3-158">(označeno)</span><span class="sxs-lookup"><span data-stu-id="404a3-158">(marked)</span></span>    |

    <span data-ttu-id="404a3-159">Řádek 2: karta **Řádek výkazu příjmů**</span><span class="sxs-lookup"><span data-stu-id="404a3-159">Line 2: **Earning statement line** tab</span></span>

    | <span data-ttu-id="404a3-160">Pole</span><span class="sxs-lookup"><span data-stu-id="404a3-160">Field</span></span>            | <span data-ttu-id="404a3-161">Hodnota</span><span class="sxs-lookup"><span data-stu-id="404a3-161">Value</span></span>    |
    |------------------|----------|
    | <span data-ttu-id="404a3-162">Kód příjmů</span><span class="sxs-lookup"><span data-stu-id="404a3-162">Earnings code</span></span>    | <span data-ttu-id="404a3-163">Prémie</span><span class="sxs-lookup"><span data-stu-id="404a3-163">Bonus</span></span>    |
    | <span data-ttu-id="404a3-164">Množství</span><span class="sxs-lookup"><span data-stu-id="404a3-164">Quantity</span></span>         | <span data-ttu-id="404a3-165">1.0000</span><span class="sxs-lookup"><span data-stu-id="404a3-165">1.0000</span></span>   |
    | <span data-ttu-id="404a3-166">Kurz</span><span class="sxs-lookup"><span data-stu-id="404a3-166">Rate</span></span>             | <span data-ttu-id="404a3-167">4250.00</span><span class="sxs-lookup"><span data-stu-id="404a3-167">4250.00</span></span>  |
    | <span data-ttu-id="404a3-168">Karta Detaily řádku</span><span class="sxs-lookup"><span data-stu-id="404a3-168">Line details tab</span></span> |          |
    | <span data-ttu-id="404a3-169">Ruční</span><span class="sxs-lookup"><span data-stu-id="404a3-169">Manual</span></span>           | <span data-ttu-id="404a3-170">(označeno)</span><span class="sxs-lookup"><span data-stu-id="404a3-170">(marked)</span></span> |

    <span data-ttu-id="404a3-171">Řádek 3: karta **Řádek výkazu příjmů**</span><span class="sxs-lookup"><span data-stu-id="404a3-171">Line 3: **Earning statement line** tab</span></span>

    | <span data-ttu-id="404a3-172">Pole</span><span class="sxs-lookup"><span data-stu-id="404a3-172">Field</span></span>           | <span data-ttu-id="404a3-173">Hodnota</span><span class="sxs-lookup"><span data-stu-id="404a3-173">Value</span></span>      |
    |-----------------|------------|
    | <span data-ttu-id="404a3-174">Kód příjmů</span><span class="sxs-lookup"><span data-stu-id="404a3-174">Earnings code</span></span>   | <span data-ttu-id="404a3-175">Komise</span><span class="sxs-lookup"><span data-stu-id="404a3-175">Commission</span></span> |
    | <span data-ttu-id="404a3-176">Množství</span><span class="sxs-lookup"><span data-stu-id="404a3-176">Quantity</span></span>        | <span data-ttu-id="404a3-177">1.0000</span><span class="sxs-lookup"><span data-stu-id="404a3-177">1.0000</span></span>     |
    | <span data-ttu-id="404a3-178">Kurz</span><span class="sxs-lookup"><span data-stu-id="404a3-178">Rate</span></span>            | <span data-ttu-id="404a3-179">!,299.00</span><span class="sxs-lookup"><span data-stu-id="404a3-179">!,299.00</span></span>   |
    | <span data-ttu-id="404a3-180">Kurz</span><span class="sxs-lookup"><span data-stu-id="404a3-180">Rate</span></span>            | <span data-ttu-id="404a3-181">1,299.00</span><span class="sxs-lookup"><span data-stu-id="404a3-181">1,299.00</span></span>   |
    | <span data-ttu-id="404a3-182">Karta Detaily řádku</span><span class="sxs-lookup"><span data-stu-id="404a3-182">Line detail tab</span></span> |            |
    | <span data-ttu-id="404a3-183">Ruční</span><span class="sxs-lookup"><span data-stu-id="404a3-183">Manual</span></span>          | <span data-ttu-id="404a3-184">(označeno)</span><span class="sxs-lookup"><span data-stu-id="404a3-184">(Marked)</span></span>   |

    > [!NOTE]
    > <span data-ttu-id="404a3-185">Nastavení posuvníku **Ruční** na hodnotu **Ano** v poli **Podrobnosti řádku** pro každý řádek výkazu příjmů je klíčem pro počáteční zůstatky mezd zadané pro každého zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="404a3-185">Setting the **Manual** slider to **Yes** in the **Line Details** tab for each earnings statement line is key to have payroll beginning balances entered for each worker.</span></span>

3. <span data-ttu-id="404a3-186">V podokně **akce** klepněte na tlačítko **Uvolnění výkazu příjmů** USA FED ER FICA.</span><span class="sxs-lookup"><span data-stu-id="404a3-186">On the **Action** pane, click **Release earnings statement** USA-FED-ER-FICA.</span></span>
4. <span data-ttu-id="404a3-187">V podokně **akce** klepněte na **Platební příkaz** pro otevření stránky **Generovat platební výkazy** stránky a nastavte následující:</span><span class="sxs-lookup"><span data-stu-id="404a3-187">On the **Action** pane click **Pay statement** to open the **Generate pay statements** page and set the following:</span></span>

    | <span data-ttu-id="404a3-188">Pole</span><span class="sxs-lookup"><span data-stu-id="404a3-188">Field</span></span>              | <span data-ttu-id="404a3-189">Hodnota</span><span class="sxs-lookup"><span data-stu-id="404a3-189">Value</span></span>     |
    |--------------------|-----------|
    | <span data-ttu-id="404a3-190">Datum platby</span><span class="sxs-lookup"><span data-stu-id="404a3-190">Payment date</span></span>       | <span data-ttu-id="404a3-191">30. 6. 2017</span><span class="sxs-lookup"><span data-stu-id="404a3-191">6/30/2017</span></span> |
    | <span data-ttu-id="404a3-192">Typ cyklu plateb</span><span class="sxs-lookup"><span data-stu-id="404a3-192">Payment run type</span></span>   | <span data-ttu-id="404a3-193">Ruční</span><span class="sxs-lookup"><span data-stu-id="404a3-193">Manual</span></span>    |
    | <span data-ttu-id="404a3-194">Zakázat účetnictví</span><span class="sxs-lookup"><span data-stu-id="404a3-194">Disable accounting</span></span> |   <span data-ttu-id="404a3-195">Ano</span><span class="sxs-lookup"><span data-stu-id="404a3-195">Yes</span></span>     |

    > [!NOTE] 
    > <span data-ttu-id="404a3-196">To je dostupné pouze, když je typ spuštění platby ručně a uživatel chce zakázat účtování ve spuštění platů.</span><span class="sxs-lookup"><span data-stu-id="404a3-196">This is only available when the payment run type is manual and wherein the user want to disable accounting on the pay run.</span></span>

    <span data-ttu-id="404a3-197">Klikněte na tlačítko **OK** a zavřete **Infolog**.</span><span class="sxs-lookup"><span data-stu-id="404a3-197">Click **OK** and close the **Infolog**.</span></span>

#### <a name="why-the-disable-accounting-slider-needs-to-set-to-yes-when-generating-pay-statements"></a><span data-ttu-id="404a3-198">Proč musí být při generování výkazů mezd posuvník na hodnotě Zakázat účtování nastavený na Ano?</span><span class="sxs-lookup"><span data-stu-id="404a3-198">Why the Disable Accounting slider needs to set to Yes when generating pay statements?</span></span>

<span data-ttu-id="404a3-199">Nastavením posuvníku na hodnotu **Ano** se zabrání distribuci řádků ve výkazu mezd a jejich rozúčtování do hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="404a3-199">Setting the slider to **Yes** prevents lines in the pay statement from being distributed to General ledger.</span></span> <span data-ttu-id="404a3-200">Pokud byly zadány účetní zůstatky ze systému ze staršího systému, byly částky v hlavní knize aktualizovány dříve.</span><span class="sxs-lookup"><span data-stu-id="404a3-200">General ledger amounts were updating earlier when account balances from the legacy system were entered.</span></span> <span data-ttu-id="404a3-201">Zadání počátečních zůstatků pro zpracování mezd umožňuje generovat sestavy, které budou zahrnovat informace z předchozích let a identifikovat limity pro účely zaměstnaneckých výhod a daní.</span><span class="sxs-lookup"><span data-stu-id="404a3-201">Entering beginning balances for Payroll lets you generate reports that include information from prior years, as well as for identifying limits for benefit and tax purposes.</span></span>

### <a name="c-create-pay-statements-for-employees"></a><span data-ttu-id="404a3-202">C.</span><span class="sxs-lookup"><span data-stu-id="404a3-202">C.</span></span> <span data-ttu-id="404a3-203">Vytvoření výkazů plateb pro zaměstnance</span><span class="sxs-lookup"><span data-stu-id="404a3-203">Create pay statements for employees</span></span>

<span data-ttu-id="404a3-204">Po generování výkazů mezd, které mají počáteční zůstatky, je nutné ověřit, že výkazy mezd přesně odpovídají mzdovým datům.</span><span class="sxs-lookup"><span data-stu-id="404a3-204">After you generate pay statements that have beginning balances, you must verify that the pay statements accurately reflect payroll data.</span></span> <span data-ttu-id="404a3-205">Je také nutné ručně aktualizovat informace o zaměstnaneckých výhodách a daních tak, aby odpovídaly hodnotám v předchozím mzdovém systému.</span><span class="sxs-lookup"><span data-stu-id="404a3-205">You must also manually update the benefit and taxes information to match the values in the previous payroll system.</span></span> <span data-ttu-id="404a3-206">Po ověření, že částky z předchozího systému mezd odpovídají částkám v aktuálním výkazu mezd, musíte dokončit výkazy mezd.</span><span class="sxs-lookup"><span data-stu-id="404a3-206">After you verify that the amounts from the previous payroll system match the amounts on the current pay statements, you must finalize the pay statements.</span></span>

1. <span data-ttu-id="404a3-207">Otevřete stránku **všechny platební příkazy**.</span><span class="sxs-lookup"><span data-stu-id="404a3-207">Open the **All pay statements** page.</span></span>
2. <span data-ttu-id="404a3-208">Zvýraznění posledního generovaného mzdového výpisu pro Michaela Redmonda</span><span class="sxs-lookup"><span data-stu-id="404a3-208">Highlight the last generated pay statement for Michael Redmond</span></span>
3. <span data-ttu-id="404a3-209">Kliknutím na tlačítko **upravit** otevřete stránku **mzdový výkaz**.</span><span class="sxs-lookup"><span data-stu-id="404a3-209">Click **Edit** to open the **Pay statement** page.</span></span>
4. <span data-ttu-id="404a3-210">Otevřete kartu **Odpočty zaměstnaneckých výhod** a zadejte následující:</span><span class="sxs-lookup"><span data-stu-id="404a3-210">Open the **Benefit deductions** tab and enter the following:</span></span>

    | <span data-ttu-id="404a3-211">Pole</span><span class="sxs-lookup"><span data-stu-id="404a3-211">Field</span></span>             | <span data-ttu-id="404a3-212">Hodnota</span><span class="sxs-lookup"><span data-stu-id="404a3-212">Value</span></span>            |
    |-------------------|------------------|
    | <span data-ttu-id="404a3-213">Zam. výhoda</span><span class="sxs-lookup"><span data-stu-id="404a3-213">Benefit</span></span>           | <span data-ttu-id="404a3-214">Částka odpočtu</span><span class="sxs-lookup"><span data-stu-id="404a3-214">Deduction amount</span></span> |
    | <span data-ttu-id="404a3-215">401K</span><span class="sxs-lookup"><span data-stu-id="404a3-215">401K</span></span>              | <span data-ttu-id="404a3-216">Účast</span><span class="sxs-lookup"><span data-stu-id="404a3-216">Participate</span></span>      |
    | <span data-ttu-id="404a3-217">Zubní</span><span class="sxs-lookup"><span data-stu-id="404a3-217">Dental</span></span>            | <span data-ttu-id="404a3-218">SubSp</span><span class="sxs-lookup"><span data-stu-id="404a3-218">SubSp</span></span>            |
    | <span data-ttu-id="404a3-219">Útrata za péči</span><span class="sxs-lookup"><span data-stu-id="404a3-219">Dep care spending</span></span> | <span data-ttu-id="404a3-220">Účast</span><span class="sxs-lookup"><span data-stu-id="404a3-220">Participate</span></span>      |
    | <span data-ttu-id="404a3-221">Vize</span><span class="sxs-lookup"><span data-stu-id="404a3-221">Vision</span></span>            | <span data-ttu-id="404a3-222">SupSp</span><span class="sxs-lookup"><span data-stu-id="404a3-222">SupSp</span></span>            |

5. <span data-ttu-id="404a3-223">Na kartě **Odpočty zaměstnaneckých výhod** zadejte následující:</span><span class="sxs-lookup"><span data-stu-id="404a3-223">In the **Benefit contributions** tab and enter the following:</span></span>

    | <span data-ttu-id="404a3-224">Pole</span><span class="sxs-lookup"><span data-stu-id="404a3-224">Field</span></span>   | <span data-ttu-id="404a3-225">Hodnota</span><span class="sxs-lookup"><span data-stu-id="404a3-225">Value</span></span>               |
    |---------|---------------------|
    | <span data-ttu-id="404a3-226">Zam. výhoda</span><span class="sxs-lookup"><span data-stu-id="404a3-226">Benefit</span></span> | <span data-ttu-id="404a3-227">Částka příspěvku</span><span class="sxs-lookup"><span data-stu-id="404a3-227">Contribution amount</span></span> |
    | <span data-ttu-id="404a3-228">401K</span><span class="sxs-lookup"><span data-stu-id="404a3-228">401K</span></span>    | <span data-ttu-id="404a3-229">Účast</span><span class="sxs-lookup"><span data-stu-id="404a3-229">Participate</span></span>         |
    | <span data-ttu-id="404a3-230">Zubní</span><span class="sxs-lookup"><span data-stu-id="404a3-230">Dental</span></span>  | <span data-ttu-id="404a3-231">SubSp</span><span class="sxs-lookup"><span data-stu-id="404a3-231">SubSp</span></span>               |
    | <span data-ttu-id="404a3-232">Vize</span><span class="sxs-lookup"><span data-stu-id="404a3-232">Vision</span></span>  | <span data-ttu-id="404a3-233">SubSp</span><span class="sxs-lookup"><span data-stu-id="404a3-233">SubSp</span></span>               |

6. <span data-ttu-id="404a3-234">Na kartě **Daňové odpočty** zadejte následující:</span><span class="sxs-lookup"><span data-stu-id="404a3-234">In the **Tax deductions** tab, enter the following:</span></span>

    | <span data-ttu-id="404a3-235">Pole</span><span class="sxs-lookup"><span data-stu-id="404a3-235">Field</span></span>           | <span data-ttu-id="404a3-236">Hodnota</span><span class="sxs-lookup"><span data-stu-id="404a3-236">Value</span></span>            |
    |-----------------|------------------|
    | <span data-ttu-id="404a3-237">Kód daně</span><span class="sxs-lookup"><span data-stu-id="404a3-237">Tax code</span></span>        | <span data-ttu-id="404a3-238">Částka odpočtu</span><span class="sxs-lookup"><span data-stu-id="404a3-238">Deduction amount</span></span> |
    | <span data-ttu-id="404a3-239">USA FED ER FICA</span><span class="sxs-lookup"><span data-stu-id="404a3-239">USA-FED-ER-FICA</span></span> | <span data-ttu-id="404a3-240">1600.00</span><span class="sxs-lookup"><span data-stu-id="404a3-240">1600.00</span></span>          |
    | <span data-ttu-id="404a3-241">USA FED ER MEDI</span><span class="sxs-lookup"><span data-stu-id="404a3-241">USA-FED-ER-MEDI</span></span> | <span data-ttu-id="404a3-242">825.75</span><span class="sxs-lookup"><span data-stu-id="404a3-242">825.75</span></span>           |

7. <span data-ttu-id="404a3-243">Na kartě **Daňové příspěvky** zadejte následující:</span><span class="sxs-lookup"><span data-stu-id="404a3-243">In the **Tax contributions** tab enter the following:</span></span>
8. <span data-ttu-id="404a3-244">Klikněte na tlačítko **Vypočítat.**</span><span class="sxs-lookup"><span data-stu-id="404a3-244">Click **Calculate**.</span></span>

    > [!IMPORTANT] 
    > <span data-ttu-id="404a3-245">Ověřte celkové částky výkazu mezd, aby odpovídaly hodnotě od počátku roku systému ze starší verze pracovníka.</span><span class="sxs-lookup"><span data-stu-id="404a3-245">Validate the totals of the pay statement that they match the YTD of the legacy system for the worker.</span></span> <span data-ttu-id="404a3-246">Můžete chtít zablokovat dokončení v dalším kroku, abyste mohli provést komplexní ověřování všech výkazů mezd celkem.</span><span class="sxs-lookup"><span data-stu-id="404a3-246">You may want to hold off on finalizing in the next step to do some overall validating of all pay statements in aggregate.</span></span> <span data-ttu-id="404a3-247">Po ověření spusťte všechny výkazy mezd a dokončete je.</span><span class="sxs-lookup"><span data-stu-id="404a3-247">Once validated run through all the pay statements and finalize them.</span></span>

<span data-ttu-id="404a3-248">Stejný postup lze provést v přírůstcích po čtvrtletí, pokud je to potřeba u všech předchozích kvartálů v každém období.</span><span class="sxs-lookup"><span data-stu-id="404a3-248">The same process can be done in quarter increments if necessary for all prior quarters in each year.</span></span> <span data-ttu-id="404a3-249">To je potřeba, pouze pokud zákazník musí zobrazit data podle čtvrtletí bez návratu zpět do systému ze starší verze.</span><span class="sxs-lookup"><span data-stu-id="404a3-249">This is only needed if the customer needs to see the data by quarter without going back to the legacy system.</span></span>

## <a name="if-you-make-a-mistake-entering-beginning-balances-for-an-employee"></a><span data-ttu-id="404a3-250">Pokud uděláte chybu při zadávání počátečních zůstatků pro zaměstnance</span><span class="sxs-lookup"><span data-stu-id="404a3-250">If you make a mistake Entering Beginning Balances for an Employee</span></span>

<span data-ttu-id="404a3-251">Je možné stornovat a znovu zadávat transakce.</span><span class="sxs-lookup"><span data-stu-id="404a3-251">It is possible to reverse and reenter transactions.</span></span> <span data-ttu-id="404a3-252">Chcete-li transakci stornovat, vše, co je nutné provést, je provést následující kroky na stránce **všechny platební příkazy**.</span><span class="sxs-lookup"><span data-stu-id="404a3-252">To reverse the transaction, all you have to do is to complete the follow steps on the **All pay statements** page.</span></span>

1. <span data-ttu-id="404a3-253">Klepněte na tlačítko **stornovat**.</span><span class="sxs-lookup"><span data-stu-id="404a3-253">Click **Reverse**.</span></span>
2. <span data-ttu-id="404a3-254">Klepněte na tlačítko **Ano** po zobrazení zprávy "Při stornování tohoto výkazu mezd se vytvoří storno platby pro vyrovnání v tomto výkazu mezd.</span><span class="sxs-lookup"><span data-stu-id="404a3-254">Click **Yes** when the message "When you reverse this pay statement, a reversing pay statement will be created to offset this pay statement.</span></span> <span data-ttu-id="404a3-255">Nelze upravit žádný výkaz mezd.</span><span class="sxs-lookup"><span data-stu-id="404a3-255">Neither pay statement can be edited.</span></span> <span data-ttu-id="404a3-256">Chcete stornovat tento výkaz mezd?"</span><span class="sxs-lookup"><span data-stu-id="404a3-256">Do you want to reverse this pay statement?"</span></span> <span data-ttu-id="404a3-257">.</span><span class="sxs-lookup"><span data-stu-id="404a3-257">displays.</span></span> 

<span data-ttu-id="404a3-258">Po stornování výkazu mezd můžete generovat nový výkaz mezd pracovníka na základě předtím vytvořeného výkazu mezd.</span><span class="sxs-lookup"><span data-stu-id="404a3-258">After you reverse the pay statement, you can generate a new pay statement for the worker from the earnings statement that you created previously.</span></span> <span data-ttu-id="404a3-259">Je nutné opravit jakékoli nesprávné řádky ve výkazu zisků předtím, než budete generovat nový výkaz mezd, a následně generovat nové výkazy mezd se správnými částkami.</span><span class="sxs-lookup"><span data-stu-id="404a3-259">Be sure to fix any incorrect lines on the earnings statement before you generate the new pay statement, and then generate new pay statements with the correct amounts.</span></span> 


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]