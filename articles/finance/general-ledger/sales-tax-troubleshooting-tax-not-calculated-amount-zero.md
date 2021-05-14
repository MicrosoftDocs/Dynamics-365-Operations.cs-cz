---
title: Daň se nevypočítá nebo je částka daně nulová
description: Toto téma poskytuje informace o řešení potíží, které mohou pomoci, když je částka daně 0 (nula) nebo se daň nevypočítá.
author: shtao
ms.date: 04/01/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: ead979081692d4dcee9812c89f5f10c7879d3f7e
ms.sourcegitcommit: 57668404d61359b33e0c0280f2f7c4eb829b1ed2
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/27/2021
ms.locfileid: "5947608"
---
# <a name="tax-isnt-calculated-or-the-tax-amount-is-zero"></a><span data-ttu-id="6bf87-103">Daň se nevypočítá nebo je částka daně nulová</span><span class="sxs-lookup"><span data-stu-id="6bf87-103">Tax isn't calculated or the tax amount is zero</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6bf87-104">Transakce může mít částku řádku, která není 0 (nula), ale buď se nevypočítá daň, nebo vypočítaná částka daně je 0.</span><span class="sxs-lookup"><span data-stu-id="6bf87-104">A transaction might have a line amount that isn't 0 (zero), but either tax isn't calculated or the calculated tax amount is 0.</span></span> <span data-ttu-id="6bf87-105">Chcete-li tento problém vyřešit, postupujte podle pokynů v následujících částech.</span><span class="sxs-lookup"><span data-stu-id="6bf87-105">To troubleshoot this issue, follow the steps in the following sections as required.</span></span>

## <a name="verify-that-tax-codes-are-correctly-selected-by-the-transaction"></a><span data-ttu-id="6bf87-106">Ověřte, zda jsou transakcí správně vybrány daňové kódy</span><span class="sxs-lookup"><span data-stu-id="6bf87-106">Verify that tax codes are correctly selected by the transaction</span></span>

<span data-ttu-id="6bf87-107">Pokud transakce nevybírá správné daňové kódy nebo nevybírá žádné daňové kódy, daně z ní nebudou vypočítány.</span><span class="sxs-lookup"><span data-stu-id="6bf87-107">If the transaction doesn't select the correct tax codes, or if it doesn't select any tax codes, taxes won't be calculated on it.</span></span> <span data-ttu-id="6bf87-108">Podle následujícího postupu ověřte, zda jsou transakcí správně vybrány daňové kódy.</span><span class="sxs-lookup"><span data-stu-id="6bf87-108">Follow these steps to verify that tax codes are correctly selected by the transaction.</span></span> 

1. <span data-ttu-id="6bf87-109">Na řádku transakce na záložce s náhledem **Detaily řádku** na kartě **Nastavení** v části **DPH** ověřte, zda jsou v polích **Skupina DPH položky** a **Skupina DPH** vybrané správné daňové skupiny.</span><span class="sxs-lookup"><span data-stu-id="6bf87-109">On the transaction line, on the **Line details** FastTab, on the **Setup** tab, in the **Sales tax** section, verify that the correct tax groups are selected in the **Item sales tax group** and **Sales tax group** fields.</span></span> <span data-ttu-id="6bf87-110">Pokud nejsou vybrány správné daňové skupiny, vyberte je.</span><span class="sxs-lookup"><span data-stu-id="6bf87-110">If the correct tax groups aren't selected, select them.</span></span>

    <span data-ttu-id="6bf87-111">[![Pole Skupina DPH zboží a Skupina DPH](./media/tax-not-calculated-tax-amount-zero-Picture1.png)](./media/tax-not-calculated-tax-amount-zero-Picture1.png)</span><span class="sxs-lookup"><span data-stu-id="6bf87-111">[![Item sales tax group and Sales tax group fields](./media/tax-not-calculated-tax-amount-zero-Picture1.png)](./media/tax-not-calculated-tax-amount-zero-Picture1.png)</span></span>

2. <span data-ttu-id="6bf87-112">Přejděte k nabídce **Daň** \> **Nepřímé daně** \> **DPH** \> **Skupiny DPH**.</span><span class="sxs-lookup"><span data-stu-id="6bf87-112">Go to **Tax** \> **Indirect taxes** \> **Sales tax** \> **Sales tax groups**.</span></span>
3. <span data-ttu-id="6bf87-113">Vyberte příslušnou skupinu DPH a poté si na záložce s náhledem **Nastavení** poznamenejte kód DPH v poli **Kód DPH**.</span><span class="sxs-lookup"><span data-stu-id="6bf87-113">Select the appropriate sales tax group, and then, on the **Setup** FastTab, make a note of the tax code in the **Sales tax code** field.</span></span>

    <span data-ttu-id="6bf87-114">[![Stránka Skupiny DPH](./media/tax-not-calculated-tax-amount-zero-Picture2.png)](./media/tax-not-calculated-tax-amount-zero-Picture2.png)</span><span class="sxs-lookup"><span data-stu-id="6bf87-114">[![Sales tax groups page](./media/tax-not-calculated-tax-amount-zero-Picture2.png)](./media/tax-not-calculated-tax-amount-zero-Picture2.png)</span></span>

4. <span data-ttu-id="6bf87-115">Přejděte k nabídce **Daň** \> **Nepřímé daně** \> **DPH** \> **Skupiny DPH položky**.</span><span class="sxs-lookup"><span data-stu-id="6bf87-115">Go to **Tax** \> **Indirect taxes** \> **Sales tax** \> **Item sales tax groups**.</span></span>
5. <span data-ttu-id="6bf87-116">Vyberte příslušnou skupinu DPH položky a poté na záložce s náhledem **Nastavení** ověřte, že daňový kód v poli **Kód DPH** odpovídá daňovému kódu skupiny DPH.</span><span class="sxs-lookup"><span data-stu-id="6bf87-116">Select the appropriate item sales tax group, and then, on the **Setup** FastTab, verify that the tax code in the **Sales tax code** field matches the tax code of the sales tax group.</span></span>

    <span data-ttu-id="6bf87-117">[![Stránka Skupiny DPH položky](./media/tax-not-calculated-tax-amount-zero-Picture3.png)](./media/tax-not-calculated-tax-amount-zero-Picture3.png)</span><span class="sxs-lookup"><span data-stu-id="6bf87-117">[![Item sales tax groups page](./media/tax-not-calculated-tax-amount-zero-Picture3.png)](./media/tax-not-calculated-tax-amount-zero-Picture3.png)</span></span>

6. <span data-ttu-id="6bf87-118">Pokud se daňové kódy neshodují, aktualizujte kód DPH pro jednu ze skupin.</span><span class="sxs-lookup"><span data-stu-id="6bf87-118">If the tax codes don't match, update the sales tax code for one of the groups.</span></span>

## <a name="verify-that-the-selected-tax-codes-arent-exempt-and-that-they-have-the-correct-tax-rate-value"></a><span data-ttu-id="6bf87-119">Ověřte, zda vybrané daňové kódy nejsou osvobozeny a zda mají správnou hodnotu sazby daně</span><span class="sxs-lookup"><span data-stu-id="6bf87-119">Verify that the selected tax codes aren't exempt and that they have the correct tax rate value</span></span>

<span data-ttu-id="6bf87-120">Pokud jsou daňové kódy osvobozeny, nebo pokud je sazba daně 0 (nula), bude výsledek výpočtu daně 0.</span><span class="sxs-lookup"><span data-stu-id="6bf87-120">If the tax codes are exempt, or if the tax rate is 0 (zero), the tax calculation result will be 0.</span></span> <span data-ttu-id="6bf87-121">Postupujte podle těchto pokynů, abyste zjistili, zda jsou vybrané daňové kódy osvobozeny, a ověřte, zda se na ně vztahuje správná sazba daně.</span><span class="sxs-lookup"><span data-stu-id="6bf87-121">Follow these steps to determine whether the selected tax codes are exempt and to verify that the correct tax rate is applied to them.</span></span>

1. <span data-ttu-id="6bf87-122">Přejděte k nabídce **Daň** \> **Nepřímé daně** \> **DPH** \> **Skupiny DPH**.</span><span class="sxs-lookup"><span data-stu-id="6bf87-122">Go to **Tax** \> **Indirect taxes** \> **Sales tax** \> **Sales tax groups**.</span></span>
2. <span data-ttu-id="6bf87-123">Vyberte příslušnou skupinu DPH a poté na záložce s náhledem **Nastavení** ověřte, že není zaškrtnuto políčko **Osvobození**.</span><span class="sxs-lookup"><span data-stu-id="6bf87-123">Select the appropriate sales tax group, and then, on the **Setup** FastTab, verify that the **Exempt** check box is cleared.</span></span> <span data-ttu-id="6bf87-124">Pokud je vybráno, vymažte jej.</span><span class="sxs-lookup"><span data-stu-id="6bf87-124">If it's selected, clear it.</span></span>

    <span data-ttu-id="6bf87-125">[![Zaškrtávací políčko Osvobození na stránce Skupiny DPH](./media/tax-not-calculated-tax-amount-zero-Picture4.png)](./media/tax-not-calculated-tax-amount-zero-Picture4.png)</span><span class="sxs-lookup"><span data-stu-id="6bf87-125">[![Exempt check box on the Sales tax groups page](./media/tax-not-calculated-tax-amount-zero-Picture4.png)](./media/tax-not-calculated-tax-amount-zero-Picture4.png)</span></span>

3. <span data-ttu-id="6bf87-126">Přejděte k nabídce **Daň** \> **Nepřímé daně** \> **DPH** \> **Kódy DPH**.</span><span class="sxs-lookup"><span data-stu-id="6bf87-126">Go to **Tax** \> **Indirect taxes** \> **Sales tax** \> **Sales tax codes**.</span></span>
4. <span data-ttu-id="6bf87-127">Vyberte příslušný kód DPH a poté ověřte, zda není sazba daně v poli **Hodnota** nastavena na 0 (nula).</span><span class="sxs-lookup"><span data-stu-id="6bf87-127">Select the appropriate sales tax code, and then verify that the tax rate value in the **Value** field isn't 0 (zero).</span></span> <span data-ttu-id="6bf87-128">Pokud je 0, aktualizujte pole tak, aby bylo nastaveno na správnou sazbu daně.</span><span class="sxs-lookup"><span data-stu-id="6bf87-128">If it's 0, update the field so that it's set to the correct tax rate.</span></span>

    <span data-ttu-id="6bf87-129">[![Pole Hodnota na stránce Hodnoty kódu DPH](./media/tax-not-calculated-tax-amount-zero-Picture5.png)](./media/tax-not-calculated-tax-amount-zero-Picture5.png)</span><span class="sxs-lookup"><span data-stu-id="6bf87-129">[![Value field on the Sales tax code values page](./media/tax-not-calculated-tax-amount-zero-Picture5.png)](./media/tax-not-calculated-tax-amount-zero-Picture5.png)</span></span>

## <a name="determine-whether-zero-is-the-correct-tax-amount"></a><span data-ttu-id="6bf87-130">Zjistěte, zda nula je správná částka daně</span><span class="sxs-lookup"><span data-stu-id="6bf87-130">Determine whether zero is the correct tax amount</span></span>

<span data-ttu-id="6bf87-131">V některých scénářích je částka daně 0 (nula) správná.</span><span class="sxs-lookup"><span data-stu-id="6bf87-131">In some scenarios, a tax amount of 0 (zero) is correct.</span></span> <span data-ttu-id="6bf87-132">Pomocí těchto kroků zjistíte, zda 0 je správná částka daně pro vaši transakci.</span><span class="sxs-lookup"><span data-stu-id="6bf87-132">Follow these steps to determine whether 0 is the correct tax amount for your transaction.</span></span>

1. <span data-ttu-id="6bf87-133">Přejděte k nabídce **Hlavní kniha** \> **Nastavení hlavní knihy** \> **Parametry hlavní knihy**.</span><span class="sxs-lookup"><span data-stu-id="6bf87-133">Go to **General ledger** \> **Ledger setup** \> **General ledger parameters**.</span></span>
2. <span data-ttu-id="6bf87-134">Na kartě **DPH** v poli **Metoda výpočtu** ověřte, že je vybrána možnost **Celkem**.</span><span class="sxs-lookup"><span data-stu-id="6bf87-134">On the **Sales tax** tab, in the **Calculation method** field, verify that **Total** is selected.</span></span>

    <span data-ttu-id="6bf87-135">[![Pole Metoda výpočtu na stránce Parametry hlavní knihy](./media/tax-not-calculated-tax-amount-zero-Picture6.png)](./media/tax-not-calculated-tax-amount-zero-Picture6.png)</span><span class="sxs-lookup"><span data-stu-id="6bf87-135">[![Calculation method field on the General ledger parameters page](./media/tax-not-calculated-tax-amount-zero-Picture6.png)](./media/tax-not-calculated-tax-amount-zero-Picture6.png)</span></span>

3. <span data-ttu-id="6bf87-136">Přejděte k nabídce **Daň** \> **Nepřímé daně** \> **DPH** \> **Kódy DPH**.</span><span class="sxs-lookup"><span data-stu-id="6bf87-136">Go to **Tax** \> **Indirect taxes** \> **Sales tax** \> **Sales tax codes**.</span></span>
4. <span data-ttu-id="6bf87-137">Vyberte příslušný kód DPH, vyberte možnost **Výpočet** \> **Základ marže** a ověřte, zda je základ marže nastaven na hodnotu **Čistá částka zůstatku faktury** nebo **Celková fakturovaná částka, včetně částek DPH**.</span><span class="sxs-lookup"><span data-stu-id="6bf87-137">Select the appropriate sales tax code, select **Calculation** \> **Marginal base**, and verify that the marginal base is set to **Net amount of invoice balance** or **Invoice total incl. other sales tax amounts**.</span></span> <span data-ttu-id="6bf87-138">Další informace viz [Celková fakturovaná částka, včetně částek DPH](marginal-base-field.md#invoice-total-incl-other-sales-tax-amounts).</span><span class="sxs-lookup"><span data-stu-id="6bf87-138">For more information, see the [Invoice total incl. other sales tax amounts](marginal-base-field.md#invoice-total-incl-other-sales-tax-amounts).</span></span>
5. <span data-ttu-id="6bf87-139">Pokud jsou v krocích 2 a 4 nastaveny správné hodnoty, určete, zda je celková částka transakce 0 (nula).</span><span class="sxs-lookup"><span data-stu-id="6bf87-139">If the correct values are set in steps 2 and 4, determine whether the total amount of the transaction is 0 (zero).</span></span> <span data-ttu-id="6bf87-140">Pokud je celková částka 0, je očekávaným výsledkem částka daně 0.</span><span class="sxs-lookup"><span data-stu-id="6bf87-140">If the total amount is 0, a tax amount of 0 is the expected result.</span></span> <span data-ttu-id="6bf87-141">Protože výpočet daně je založen na celkové částce zůstatku faktury a tato částka není řádek po řádku, bude částka daně 0 po výpočtu daně přidělena každému řádku.</span><span class="sxs-lookup"><span data-stu-id="6bf87-141">Because the tax calculation is based on the total amount of the invoice balance, and that amount isn't line by line, the tax amount of 0 will be allocated to each line after the tax calculation.</span></span>

## <a name="determine-whether-customization-exists"></a><span data-ttu-id="6bf87-142">Zjištění, zda existuje přizpůsobení</span><span class="sxs-lookup"><span data-stu-id="6bf87-142">Determine whether customization exists</span></span>

<span data-ttu-id="6bf87-143">Pokud jste dokončili kroky v předchozích částech, ale problém se vám nepodařilo vyřešit, zjistěte, zda existuje přizpůsobení.</span><span class="sxs-lookup"><span data-stu-id="6bf87-143">If you've completed the steps in the previous sections but have found no issue, determine whether customization exists.</span></span> <span data-ttu-id="6bf87-144">Pokud neexistuje žádné přizpůsobení, vytvořte požadavek na službu Microsoft pro další podporu.</span><span class="sxs-lookup"><span data-stu-id="6bf87-144">If no customization exists, create a Microsoft service request for further support.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
