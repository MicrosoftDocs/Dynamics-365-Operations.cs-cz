---
title: Daň je v dokladu zaúčtovaná na nesprávný účet hlavní knihy
description: Toto téma poskytuje informace o řešení potíží, které mohou pomoci při zaúčtování daně na nesprávný účet hlavní knihy v dokladu.
author: qire
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 3d197046bd547757f32712a50949b41897f6fedf
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020084"
---
# <a name="tax-is-posted-to-the-wrong-ledger-account-in-the-voucher"></a><span data-ttu-id="a928c-103">Daň je v dokladu zaúčtovaná na nesprávný účet hlavní knihy</span><span class="sxs-lookup"><span data-stu-id="a928c-103">Tax is posted to the wrong ledger account in the voucher</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a928c-104">Daň se může během zaúčtování zaúčtovat na nesprávný účet hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="a928c-104">During posting, tax might be posted to the wrong ledger account in the voucher.</span></span> <span data-ttu-id="a928c-105">Chcete-li tento problém vyřešit, postupujte podle pokynů v následujících částech.</span><span class="sxs-lookup"><span data-stu-id="a928c-105">To troubleshoot this issue, follow the steps in the following sections as required.</span></span> <span data-ttu-id="a928c-106">Příklady v tomto tématu používají jako obchodní dokument prodejní objednávku.</span><span class="sxs-lookup"><span data-stu-id="a928c-106">The examples in this topic use a sales order as the business document.</span></span>

## <a name="find-the-tax-code-of-the-incorrectly-posted-tax-transaction"></a><span data-ttu-id="a928c-107">Najděte daňový kód nesprávně zaúčtované daňové transakce</span><span class="sxs-lookup"><span data-stu-id="a928c-107">Find the tax code of the incorrectly posted tax transaction</span></span>

1. <span data-ttu-id="a928c-108">Na stránce **Transakce dokladu** vyberte transakci, se kterou chcete pracovat, a poté vyberte možnost **Zaúčtování DPH**.</span><span class="sxs-lookup"><span data-stu-id="a928c-108">On the **Voucher transactions** page, select the transaction that you want to work with, and then select **Posted sales tax**.</span></span>

    <span data-ttu-id="a928c-109">[![Tlačítko Zaúčtování DPH na stránce Transakce dokladu](./media/tax-posted-to-wrong-ledger-account-Picture1.png)](./media/tax-posted-to-wrong-ledger-account-Picture1.png)</span><span class="sxs-lookup"><span data-stu-id="a928c-109">[![Posted sales tax button on the Voucher transactions page](./media/tax-posted-to-wrong-ledger-account-Picture1.png)](./media/tax-posted-to-wrong-ledger-account-Picture1.png)</span></span>

2. <span data-ttu-id="a928c-110">Zkontrolujte hodnotu v poli **Kód DPH**.</span><span class="sxs-lookup"><span data-stu-id="a928c-110">Review the value in the **Sales tax code** field.</span></span> <span data-ttu-id="a928c-111">V tomto příkladu je hodnota **DPH 19**.</span><span class="sxs-lookup"><span data-stu-id="a928c-111">In this example, it's **VAT 19**.</span></span>

    <span data-ttu-id="a928c-112">[![Pole Kód DPH na stránce Zaúčtování DPH](./media/tax-posted-to-wrong-ledger-account-Picture2.png)](./media/tax-posted-to-wrong-ledger-account-Picture2.png)</span><span class="sxs-lookup"><span data-stu-id="a928c-112">[![Sales tax code field on the Posted sales tax page](./media/tax-posted-to-wrong-ledger-account-Picture2.png)](./media/tax-posted-to-wrong-ledger-account-Picture2.png)</span></span>

## <a name="check-the-ledger-posting-group-of-the-tax-code"></a><span data-ttu-id="a928c-113">Zkontrolujte skupinu účtování hlavní knihy kvůli daňovému kódu</span><span class="sxs-lookup"><span data-stu-id="a928c-113">Check the ledger posting group of the tax code</span></span>

1. <span data-ttu-id="a928c-114">Přejděte k nabídce **Daň** \> **Nepřímé daně** \> **DPH** \> **Kódy DPH**.</span><span class="sxs-lookup"><span data-stu-id="a928c-114">Go to **Tax** \> **Indirect taxes** \> **Sales tax** \> **Sales tax codes**.</span></span>
2. <span data-ttu-id="a928c-115">Najděte a vyberte daňový kód a poté zkontrolujte hodnotu v poli **Skupina účtování hlavní knihy**.</span><span class="sxs-lookup"><span data-stu-id="a928c-115">Find and select the tax code, and then review the value in the **Ledger posting group** field.</span></span> <span data-ttu-id="a928c-116">V tomto příkladu je hodnota **DPH**.</span><span class="sxs-lookup"><span data-stu-id="a928c-116">In this example, it's **VAT**.</span></span>

    <span data-ttu-id="a928c-117">[![Pole Skupina zaúčtování hl. knihy na stránce Kódy DPH](./media/tax-posted-to-wrong-ledger-account-Picture3.png)](./media/tax-posted-to-wrong-ledger-account-Picture3.png)</span><span class="sxs-lookup"><span data-stu-id="a928c-117">[![Ledger posting group field on the Sales tax codes page](./media/tax-posted-to-wrong-ledger-account-Picture3.png)](./media/tax-posted-to-wrong-ledger-account-Picture3.png)</span></span>

3. <span data-ttu-id="a928c-118">Hodnota v poli **Skupina zaúčtování hl. knihy** je prázdná.</span><span class="sxs-lookup"><span data-stu-id="a928c-118">The value in the **Ledger posting group** field is a link.</span></span> <span data-ttu-id="a928c-119">Chcete-li zobrazit podrobnosti o konfiguraci skupiny, vyberte odkaz.</span><span class="sxs-lookup"><span data-stu-id="a928c-119">To view the details of the group's configuration, select the link.</span></span> <span data-ttu-id="a928c-120">Případně vyberte a podržte (nebo klikněte pravým tlačítkem) v poli a poté vyberte **Zobrazit podrobnosti**.</span><span class="sxs-lookup"><span data-stu-id="a928c-120">Alternatively, select and hold (or right-click) in the field, and then select **View details**.</span></span>

    <span data-ttu-id="a928c-121">[![Příkaz Zobrazit podrobnosti](./media/tax-posted-to-wrong-ledger-account-Picture4.png)](./media/tax-posted-to-wrong-ledger-account-Picture4.png)</span><span class="sxs-lookup"><span data-stu-id="a928c-121">[![View details command](./media/tax-posted-to-wrong-ledger-account-Picture4.png)](./media/tax-posted-to-wrong-ledger-account-Picture4.png)</span></span>

4. <span data-ttu-id="a928c-122">V poli **DPH na výstup** ověřte správnost čísla účtu podle typu transakce.</span><span class="sxs-lookup"><span data-stu-id="a928c-122">In the **Sales tax payable** field, verify that the account number is correct, according to the transaction type.</span></span> <span data-ttu-id="a928c-123">Pokud není správné, vyberte správný účet k zaúčtování.</span><span class="sxs-lookup"><span data-stu-id="a928c-123">If it isn't, select the correct account to post to.</span></span> <span data-ttu-id="a928c-124">V tomto příkladu by měla být DPH prodejní objednávky zaúčtována na účet závazků DPH 222200.</span><span class="sxs-lookup"><span data-stu-id="a928c-124">In this example, the sales tax of the sales order should be posted to sales tax payable account 222200.</span></span>

    <span data-ttu-id="a928c-125">[![Pole Splatná DPH na stránce Skupiny zaúčtování hlavní knihy](./media/tax-posted-to-wrong-ledger-account-Picture5.png)](./media/tax-posted-to-wrong-ledger-account-Picture5.png)</span><span class="sxs-lookup"><span data-stu-id="a928c-125">[![Sales tax payable field on the Ledger posting groups page](./media/tax-posted-to-wrong-ledger-account-Picture5.png)](./media/tax-posted-to-wrong-ledger-account-Picture5.png)</span></span>

    <span data-ttu-id="a928c-126">Následující tabulka poskytuje informace o jednotlivých polích na stránce **Skupiny zaúčtování hlavní knihy**.</span><span class="sxs-lookup"><span data-stu-id="a928c-126">The following table provides information about each field on the **Ledger posting groups** page.</span></span>

    | <span data-ttu-id="a928c-127">Pole</span><span class="sxs-lookup"><span data-stu-id="a928c-127">Field</span></span>                  | <span data-ttu-id="a928c-128">popis</span><span class="sxs-lookup"><span data-stu-id="a928c-128">Description</span></span> |
    |------------------------|-------------|
    | <span data-ttu-id="a928c-129">Splatné DPH</span><span class="sxs-lookup"><span data-stu-id="a928c-129">Sales tax payable</span></span>      | <span data-ttu-id="a928c-130">Hlavní účet pro odchozí DPH (DPH splatnou finančnímu úřadu).</span><span class="sxs-lookup"><span data-stu-id="a928c-130">The main account for outgoing sales taxes that are payable to the tax authority.</span></span> |
    | <span data-ttu-id="a928c-131">DPH na vstupu</span><span class="sxs-lookup"><span data-stu-id="a928c-131">Sales tax receivable</span></span>   | <span data-ttu-id="a928c-132">Hlavní účet pro příchozí DPH (DPH přijímanou od finančního úřadu).</span><span class="sxs-lookup"><span data-stu-id="a928c-132">The main account for incoming taxes that are received from the tax authority.</span></span> |
    | <span data-ttu-id="a928c-133">Importní DPH – výdaj</span><span class="sxs-lookup"><span data-stu-id="a928c-133">Use tax expense</span></span>        | <span data-ttu-id="a928c-134">Hlavní účet, který se používá k zaúčtování odpočitatelné importní daně, kterou dodavatelé nevyžadují ani nehlásí daňovému úřadu jako součást daně ze zboží a služeb v Evropské unii (EU) / harmonizované DPH (HST).</span><span class="sxs-lookup"><span data-stu-id="a928c-134">The main account that is used to post deductible use taxes that vendors don't claim or report to the tax authority as part of European Union (EU) reverse charge Goods and Services Tax (GST)/Harmonized Sales Tax (HST).</span></span> <span data-ttu-id="a928c-135">**Importní daň** musí být vybrána pro kód DPH ve skupině DPH, která je použitá v transakci.</span><span class="sxs-lookup"><span data-stu-id="a928c-135">**Use tax** must be selected for the sales tax code in the sales tax group that is used in the transaction.</span></span> <span data-ttu-id="a928c-136">Toto pole nebude k dispozici v případě, že je vybrána možnost **Použít daňové předpisy pro DPH** na stránce **Parametry hlavní knihy**.</span><span class="sxs-lookup"><span data-stu-id="a928c-136">This field isn't available if **Apply sales tax taxation rules** is selected on the **General ledger parameters** page.</span></span> |
    | <span data-ttu-id="a928c-137">Splatná importní DPH</span><span class="sxs-lookup"><span data-stu-id="a928c-137">Use tax payable</span></span>        | <span data-ttu-id="a928c-138">Hlavní účet, který se používá k účtování příchozích importních daní, které se platí finančním úřadům.</span><span class="sxs-lookup"><span data-stu-id="a928c-138">The main account that is used to post incoming use taxes that are payable to tax authorities.</span></span> |
    | <span data-ttu-id="a928c-139">Účet vyrovnání</span><span class="sxs-lookup"><span data-stu-id="a928c-139">Settlement account</span></span>     | <span data-ttu-id="a928c-140">Hlavní účet, který se používá k zaúčtování čistého zůstatku účtů hlavní knihy, které jsou specifikovány v polích **Splatná importní DPH** a **Pohledávka DPH**.</span><span class="sxs-lookup"><span data-stu-id="a928c-140">The main account that is used to post the net balance of the ledger accounts that are specified in the **Use tax payable** and **Sales tax receivable** fields.</span></span> |
    | <span data-ttu-id="a928c-141">Platební sleva dodavatele</span><span class="sxs-lookup"><span data-stu-id="a928c-141">Vendor cash discount</span></span>   | <span data-ttu-id="a928c-142">Hlavní účet, který se používá pro zaúčtování slevy v hotovosti pro kódy DPH, které jsou přidružené k této skupině zaúčtování hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="a928c-142">The main account that is used to post a cash discount for sales tax codes that are associated with this ledger posting group.</span></span> |
    | <span data-ttu-id="a928c-143">Platební sleva odběratele</span><span class="sxs-lookup"><span data-stu-id="a928c-143">Customer case discount</span></span> | <span data-ttu-id="a928c-144">Hlavní účet, který se používá pro zaúčtování slevy v hotovosti pro kódy DPH, které jsou přidružené k této skupině zaúčtování hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="a928c-144">The main account that is used to post a cash discount for sales tax codes that are associated with this ledger posting group.</span></span> |

    <span data-ttu-id="a928c-145">Více informací naleznete v tématu [Nastavení účetních skupin pro DPH](tasks/set-up-ledger-posting-groups-sales-tax.md).</span><span class="sxs-lookup"><span data-stu-id="a928c-145">For more information, see, [Set up Ledger posting groups for sales tax](tasks/set-up-ledger-posting-groups-sales-tax.md)</span></span>

## <a name="debug-in-code-to-check-ledger-dimensions"></a><span data-ttu-id="a928c-146">Ladění kódu pro kontrolu dimenzí hlavní knihy</span><span class="sxs-lookup"><span data-stu-id="a928c-146">Debug in code to check ledger dimensions</span></span>

<span data-ttu-id="a928c-147">V kódu je účet zaúčtování určen dimenzí hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="a928c-147">In the code, the posting account is determined by the ledger dimension.</span></span> <span data-ttu-id="a928c-148">Dimenze hlavní knihy uloží ID záznamu účtu do databáze.</span><span class="sxs-lookup"><span data-stu-id="a928c-148">The ledger dimension saves the record ID of an account in the database.</span></span>

1. <span data-ttu-id="a928c-149">U prodejní objednávky přidejte zarážku u metod **Tax::saveAndPost()** a **Tax::post()**.</span><span class="sxs-lookup"><span data-stu-id="a928c-149">For a sales order, add a breakpoint at the **Tax::saveAndPost()** and **Tax::post()** methods.</span></span> <span data-ttu-id="a928c-150">Věnujte pozornost hodnotě **\_LedgerDimension**.</span><span class="sxs-lookup"><span data-stu-id="a928c-150">Pay attention to the value of **\_ledgerDimension**.</span></span>

    <span data-ttu-id="a928c-151">[![Ukázka kódu prodejní objednávky, která má zarážku](./media/tax-posted-to-wrong-ledger-account-Picture6.png)](./media/tax-posted-to-wrong-ledger-account-Picture6.png)</span><span class="sxs-lookup"><span data-stu-id="a928c-151">[![Sales order code sample that has a breakpoint](./media/tax-posted-to-wrong-ledger-account-Picture6.png)](./media/tax-posted-to-wrong-ledger-account-Picture6.png)</span></span>

    <span data-ttu-id="a928c-152">U nákupní objednávky přidejte zarážku u metod **TaxPost::saveAndPost()** a **TaxPost::postToTaxTrans()**.</span><span class="sxs-lookup"><span data-stu-id="a928c-152">For a purchase order, add a breakpoint at the **TaxPost::saveAndPost()** and **TaxPost::postToTaxTrans()** methods.</span></span> <span data-ttu-id="a928c-153">Věnujte pozornost hodnotě **\_LedgerDimension**.</span><span class="sxs-lookup"><span data-stu-id="a928c-153">Pay attention to the value of **\_ledgerDimension**.</span></span>

    <span data-ttu-id="a928c-154">[![Ukázka kódu prodejní objednávky, která má zarážku](./media/tax-posted-to-wrong-ledger-account-Picture7.png)](./media/tax-posted-to-wrong-ledger-account-Picture7.png)</span><span class="sxs-lookup"><span data-stu-id="a928c-154">[![Purchase order code sample that has a breakpoint](./media/tax-posted-to-wrong-ledger-account-Picture7.png)](./media/tax-posted-to-wrong-ledger-account-Picture7.png)</span></span>

2. <span data-ttu-id="a928c-155">Spuštěním následujícího dotazu SQL vyhledejte zobrazenou hodnotu účtu v databázi na základě ID záznamu uloženého dimenzí hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="a928c-155">Run the following SQL query to find the display value of the account in the database, based on the record ID that is saved by the ledger dimension.</span></span>

    ```sql
    select * from DIMENSIONATTRIBUTEVALUECOMBINATION where recid={the value of _ledgerDimension}
    ```

    <span data-ttu-id="a928c-156">[![Zobrazená hodnota ID záznamu](./media/tax-posted-to-wrong-ledger-account-Picture8.png)](./media/tax-posted-to-wrong-ledger-account-Picture8.png)</span><span class="sxs-lookup"><span data-stu-id="a928c-156">[![Display value of the record ID](./media/tax-posted-to-wrong-ledger-account-Picture8.png)](./media/tax-posted-to-wrong-ledger-account-Picture8.png)</span></span>

3. <span data-ttu-id="a928c-157">Prozkoumejte zásobník volání a zjistěte, kde je přiřazena hodnota **ledgerDimension**.</span><span class="sxs-lookup"><span data-stu-id="a928c-157">Examine the callstack to find where the **_ledgerDimension** value is assigned.</span></span> <span data-ttu-id="a928c-158">Hodnota je obvykle od **TmpTaxWorkTrans**.</span><span class="sxs-lookup"><span data-stu-id="a928c-158">Usually, the value is from **TmpTaxWorkTrans**.</span></span> <span data-ttu-id="a928c-159">V tomto případě byste měli přidat zarážku na **TmpTaxWorkTrans::insert()** a **TmpTaxWorkTrans::update()**, abyste zjistili, kde je přiřazená hodnota.</span><span class="sxs-lookup"><span data-stu-id="a928c-159">In this case, you should add a breakpoint at **TmpTaxWorkTrans::insert()** and **TmpTaxWorkTrans::update()** to find where the value assigned.</span></span>

## <a name="determine-whether-customization-exists"></a><span data-ttu-id="a928c-160">Zjištění, zda existuje přizpůsobení</span><span class="sxs-lookup"><span data-stu-id="a928c-160">Determine whether customization exists</span></span>

<span data-ttu-id="a928c-161">Pokud jste dokončili kroky v předchozích částech, ale problém se vám nepodařilo vyřešit, zjistěte, zda existuje přizpůsobení.</span><span class="sxs-lookup"><span data-stu-id="a928c-161">If you've completed the steps in the previous sections but have found no issue, determine whether customization exists.</span></span> <span data-ttu-id="a928c-162">Pokud neexistuje žádné přizpůsobení, vytvořte požadavek na službu Microsoft pro další podporu.</span><span class="sxs-lookup"><span data-stu-id="a928c-162">If no customization exists, create a Microsoft service request for further support.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
