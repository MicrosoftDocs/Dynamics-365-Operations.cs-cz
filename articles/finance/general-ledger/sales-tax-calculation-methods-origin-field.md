---
title: Metody výpočtu DPH v poli Zdroj
description: Tento článek vysvětluje možnosti v poli Zdroj na stránce Kódy DPH, a postup výpočtu DPH na základě vybrané možnosti pro kód DPH.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
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
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a9ad362b4befac4a8da14fff0bc6bc8b938d30bc
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4978553"
---
# <a name="sales-tax-calculation-methods-in-the-origin-field"></a><span data-ttu-id="90b4e-103">Metody výpočtu DPH v poli Zdroj</span><span class="sxs-lookup"><span data-stu-id="90b4e-103">Sales tax calculation methods in the Origin field</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="90b4e-104">Tento článek vysvětluje možnosti v poli Zdroj na stránce Kódy DPH, a postup výpočtu DPH na základě vybrané možnosti pro kód DPH.</span><span class="sxs-lookup"><span data-stu-id="90b4e-104">This article explains the options in the Origin field on the sales tax codes page and how sales tax is calculated based on the selected option for a sales tax code.</span></span>

<span data-ttu-id="90b4e-105">Pro každý vytvořený kód DPH na stránce Kódy DPH je nutné vybrat metodu výpočtu, která je použita pro částku základu daně v poli Zdroj.</span><span class="sxs-lookup"><span data-stu-id="90b4e-105">For each sales tax code that you create in the Sales tax codes page, you must select the method of calculation to apply to the tax base amount in the Origin field.</span></span>

## <a name="percentage-of-net-amount"></a><span data-ttu-id="90b4e-106">Procento z čisté částky</span><span class="sxs-lookup"><span data-stu-id="90b4e-106">Percentage of net amount</span></span>
<span data-ttu-id="90b4e-107">Metoda výpočtu Procento z čisté částky je výchozí hodnotou v poli Zdroj.</span><span class="sxs-lookup"><span data-stu-id="90b4e-107">The Percentage of net amount calculation method is the default value in the Origin field.</span></span> <span data-ttu-id="90b4e-108">DPH se počítá jako procento z částky nákupu nebo prodeje bez všech jiných DPH.</span><span class="sxs-lookup"><span data-stu-id="90b4e-108">The sales tax is calculated as a percentage of the purchase or sales amount, excluding any other sales taxes.</span></span>
### <a name="example"></a><span data-ttu-id="90b4e-109">Příklad</span><span class="sxs-lookup"><span data-stu-id="90b4e-109">Example</span></span>

<span data-ttu-id="90b4e-110">Sazba daně je 25%.</span><span class="sxs-lookup"><span data-stu-id="90b4e-110">The tax rate is 25%.</span></span> <span data-ttu-id="90b4e-111">Řádek faktury zobrazuje množství 10 položek po $1,00 za kus a odběrateli je poskytnuta desetiprocentní řádková sleva.</span><span class="sxs-lookup"><span data-stu-id="90b4e-111">The invoice line shows a quantity of 10 items at 1.00 each, and the customer is allowed a 10% line discount.</span></span> <span data-ttu-id="90b4e-112">Čistá částka: (10 × 1,00) -10 % = 9,00 DPH: 9,00 x 25 % = 2,25 Celková částka: 9,00 + 2,25 = 11,25</span><span class="sxs-lookup"><span data-stu-id="90b4e-112">Net amount: (10 x 1.00) -10% = 9.00 Sales tax: 9.00 x 25% = 2.25 Total amount: 9.00 + 2.25 = 11.25</span></span>

## <a name="percentage-of-gross-amount"></a><span data-ttu-id="90b4e-113"> Procento z hrubé částky</span><span class="sxs-lookup"><span data-stu-id="90b4e-113">Percentage of gross amount</span></span>
<span data-ttu-id="90b4e-114">Pokud vyberete metodu Procento z hrubé částky, DPH bude vypočteno jako procento z hrubé částky prodeje.</span><span class="sxs-lookup"><span data-stu-id="90b4e-114">If you select the Percentage of gross amount method, the sales tax is calculated as a percentage of the gross sales amount.</span></span> <span data-ttu-id="90b4e-115">Hrubá částka je čistá částka na řádku plus všechny daně a poplatky pro řádek kromě jedné daně, kde Zdroj = procento z hrubé částky.</span><span class="sxs-lookup"><span data-stu-id="90b4e-115">The gross amount is the line net amount plus all taxes and fees for the line except the one tax with Origin = Percentage of gross amount.</span></span>
### <a name="example"></a><span data-ttu-id="90b4e-116">Příklad</span><span class="sxs-lookup"><span data-stu-id="90b4e-116">Example</span></span>

<span data-ttu-id="90b4e-117">Daňový úřad na položku uložil zvláštní cla.</span><span class="sxs-lookup"><span data-stu-id="90b4e-117">The tax authority has imposed special duties on an item.</span></span> <span data-ttu-id="90b4e-118">Částky cla se před výpočtem DPH přičtou k čisté částce.</span><span class="sxs-lookup"><span data-stu-id="90b4e-118">The duty amounts are added to the net amount before sales tax is calculated.</span></span> <span data-ttu-id="90b4e-119">Použijme následující kódy DPH:</span><span class="sxs-lookup"><span data-stu-id="90b4e-119">Given the following sales tax codes:</span></span>
-   <span data-ttu-id="90b4e-120">CLO 1 = 10% s pomocí metody výpočtu procenta z čisté částky</span><span class="sxs-lookup"><span data-stu-id="90b4e-120">DUTY 1 = 10%, using the Percentage of net amount calculation method</span></span>
-   <span data-ttu-id="90b4e-121">CLO 2 = 20% s pomocí metody výpočtu procenta z čisté částky</span><span class="sxs-lookup"><span data-stu-id="90b4e-121">DUTY 2 = 20%, using the Percentage of net amount calculation method</span></span>
-   <span data-ttu-id="90b4e-122">DPH = 25% s pomocí metody výpočtu procenta z hrubé částky</span><span class="sxs-lookup"><span data-stu-id="90b4e-122">SALESTAX = 25%, using the Percentage of gross amount calculation method</span></span>

<span data-ttu-id="90b4e-123">Pokud je čistá částka 10,00, pak CLO 1 = 1,00 (10,00 x 10 %) a CLO 2 = 2,00 (10,00 x 20 %).</span><span class="sxs-lookup"><span data-stu-id="90b4e-123">If the net amount is 10.00, then DUTY 1 is 1.00 (10.00 x 10%) and DUTY 2 = 2.00 (10.00 x 20%).</span></span> <span data-ttu-id="90b4e-124">Částky budou vypadat následovně: Hrubá částka: Čistá částka + Částka cla 1 + částka cla 2 (10,00 + 1,00 + 2,00) = 13,00 DPH = 13,00 x 25 % = 3,25 Celkové clo a DPH: 1,00 + 2,00 + 3,25 = 6,25 Celková částka: 10,00 + 6,25 = 16,25</span><span class="sxs-lookup"><span data-stu-id="90b4e-124">The amounts would be as follows: Gross amount: Net amount + DUTY 1 amount + DUTY 2 amount (10.00 + 1.00 + 2.00) = 13.00 SALESTAX = 13.00 x 25% = 3.25 Total DUTIES and SALESTAX: 1.00 + 2.00 + 3.25 = 6.25 Total amount: 10.00 + 6.25 = 16.25</span></span>

| <span data-ttu-id="90b4e-125">**Poznámka**</span><span class="sxs-lookup"><span data-stu-id="90b4e-125">**Note**</span></span>                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90b4e-126">Pro transakci lze použít pouze jeden daňový kód, kde Zdroj = procento z hrubé částky.</span><span class="sxs-lookup"><span data-stu-id="90b4e-126">Only one tax code with Origin = Percentage of gross amount can be used for a transaction.</span></span> <span data-ttu-id="90b4e-127">Je-li více než jeden takový kód daně určen pro transakci, zobrazí se chyba a DPH nemůže být vypočítána.</span><span class="sxs-lookup"><span data-stu-id="90b4e-127">If more than one such tax code is determined for a transaction an error will be displayed that sales tax cannot be calculated.</span></span> |


<a name="percentage-of-sales-tax"></a><span data-ttu-id="90b4e-128">Procento DPH</span><span class="sxs-lookup"><span data-stu-id="90b4e-128">Percentage of sales tax</span></span>
-----------------------

<span data-ttu-id="90b4e-129">Vyberete-li v poli Zdroj hodnotu Procento DPH, DPH se vypočítá jako procento z DPH vybrané v části Prodejní daň v poli DPH.</span><span class="sxs-lookup"><span data-stu-id="90b4e-129">When you select Percentage of sales tax in the Origin field, sales tax is calculated as a percentage of the sales tax that is selected in the Sales tax on sales tax field.</span></span> <span data-ttu-id="90b4e-130">DPH, která je vybrána v části Prodejní daň v poli DPH se vypočítá jako první.</span><span class="sxs-lookup"><span data-stu-id="90b4e-130">The sales tax that is selected in the Sales tax on sales tax field is calculated first.</span></span> <span data-ttu-id="90b4e-131">Druhá DPH bude vypočítána následovně na základě první částky DPH.</span><span class="sxs-lookup"><span data-stu-id="90b4e-131">The second sales tax is then calculated based on the first sales tax amount.</span></span>
### <a name="example"></a><span data-ttu-id="90b4e-132">Příklad</span><span class="sxs-lookup"><span data-stu-id="90b4e-132">Example</span></span>

<span data-ttu-id="90b4e-133">Použijme následující kódy DPH:</span><span class="sxs-lookup"><span data-stu-id="90b4e-133">Given the following sales tax codes:</span></span>
-   <span data-ttu-id="90b4e-134">CLO 1 = 10% s pomocí metody Procento z čisté částky</span><span class="sxs-lookup"><span data-stu-id="90b4e-134">DUTY 1 = 10%, using the Percentage of net amount method</span></span>
-   <span data-ttu-id="90b4e-135">CLO 2 = 20 % pomocí metody Procento z DPH s vybranou možností Clo 1 v části Prodejní daň v poli DPH</span><span class="sxs-lookup"><span data-stu-id="90b4e-135">DUTY 2 = 20%, using the Percentage of sales tax method, with Duty 1 in the Sales tax on sales tax field</span></span>
-   <span data-ttu-id="90b4e-136">DPH = 25% s pomocí metody Procento z hrubé částky</span><span class="sxs-lookup"><span data-stu-id="90b4e-136">SALESTAX = 25%, using the Percentage of gross amount method</span></span>

<span data-ttu-id="90b4e-137">Čistá částka: 10,00 Clo 1: 10,00 x 10 % = 1,00 Clo 2: 1,00 x 20 % = 0,20 Hrubá částka: 10,00 + 1,00 + 0,20 = 11,20 DPH: 11,20 x 25 % = 2,80 Celkové clo a DPH: 1,00 + 0,20 + 2,80 = 4,00 Celková částka: 10,00 + 4,00 = 14,00</span><span class="sxs-lookup"><span data-stu-id="90b4e-137">Net amount: 10.00 DUTY 1: 10.00 x 10% = 1.00 DUTY 2: 1.00 x 20% = 0.20 Gross amount: 10.00 + 1.00 + 0.20 = 11.20 SALESTAX: 11.20 x 25% = 2.80 Total DUTIES and SALESTAX: 1.00 + 0.20 + 2.80 = 4.00 Total amount: 10.00 + 4.00 = 14.00</span></span>

| <span data-ttu-id="90b4e-138">**Poznámka**</span><span class="sxs-lookup"><span data-stu-id="90b4e-138">**Note**</span></span>                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90b4e-139">Při výpočtu daně není možné použít více úrovní daně.</span><span class="sxs-lookup"><span data-stu-id="90b4e-139">Multilevel tax on tax calculations are not possible.</span></span> <span data-ttu-id="90b4e-140">Daň nelze vypočítat na základě DPH, které je již vypočteno na základě jiné daně.</span><span class="sxs-lookup"><span data-stu-id="90b4e-140">A tax cannot be calculated based on a tax which already is calculated based on another tax.</span></span> <span data-ttu-id="90b4e-141">U transakce lze vypočítat více jednotlivých úrovní daně u kódů daně.</span><span class="sxs-lookup"><span data-stu-id="90b4e-141">Multiple single level tax on tax codes can be calculated on a transaction.</span></span> |

## <a name="amount-per-unit"></a><span data-ttu-id="90b4e-142"> Částka za jednotku</span><span class="sxs-lookup"><span data-stu-id="90b4e-142">Amount per unit</span></span>
<span data-ttu-id="90b4e-143">Vyberete-li částky za jednotku v poli Zdroj, DPH se vypočítá jako pevná částka za jednotku vynásobená množstvím zadaným na řádku dokladu.</span><span class="sxs-lookup"><span data-stu-id="90b4e-143">When you select Amount per unit in the Origin field, sales tax is calculated as a fixed amount per unit multiplied with the quantity entered on the document line.</span></span> <span data-ttu-id="90b4e-144">Jednotka musí být zvolena v poli Jednotka.</span><span class="sxs-lookup"><span data-stu-id="90b4e-144">A unit has to be selected in the Unit field.</span></span> <span data-ttu-id="90b4e-145">Částka na jednotku je uvedena na stránce Hodnoty kódu DPH.</span><span class="sxs-lookup"><span data-stu-id="90b4e-145">The amount per unit is specified in the Sales tax code values page.</span></span>
### <a name="example"></a><span data-ttu-id="90b4e-146">Příklad</span><span class="sxs-lookup"><span data-stu-id="90b4e-146">Example</span></span>

<span data-ttu-id="90b4e-147">Kód DPH je nastaven jako: 1,20 USD za jednotku = balení Na řádku prodejní faktury je prodáno 25 balení položky DPH bude vypočtena jako hodnota 25 x 1,20 = 30,00</span><span class="sxs-lookup"><span data-stu-id="90b4e-147">Sales tax code is set up as: USD 1.20 per unit = box On a sales invoice line 25 boxes of an item are sold Sales tax is calculated as 25 x 1.20 = 30.00</span></span>

| <span data-ttu-id="90b4e-148">**Poznámka**</span><span class="sxs-lookup"><span data-stu-id="90b4e-148">**Note**</span></span>                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90b4e-149">Je-li transakce zadána u jiné jednotky než jednotky zadané v kódu prodejní daně, převede se automaticky podle pravidel převodů jednotek, které jsou nastaveny na stránce Převody jednotek.</span><span class="sxs-lookup"><span data-stu-id="90b4e-149">If the transaction is entered in different unit than the unit specified on the sales tax code, it is converted automatically based on the unit conversions that are set up in the Unit conversions page.</span></span> |

###  <a name="amount-per-unit-additional-option"></a><span data-ttu-id="90b4e-150"> Částka za jednotku, doplňková možnost</span><span class="sxs-lookup"><span data-stu-id="90b4e-150">Amount per unit, additional option</span></span>

<span data-ttu-id="90b4e-151">Na kartě Výpočet můžete určit, zda je daň vypočítaná jako částka na jednotku před dalšími kódy DPH, a přidána k čisté částce před vypočítáním ostatních kódů DPH, kde Zdroj = procento z čisté částky.</span><span class="sxs-lookup"><span data-stu-id="90b4e-151">On the Calculation tab, you can select whether an amount per unit calculated tax is calculated before other tax codes and added to the net amount before other tax codes with Origin = Percentage of net amount are calculated.</span></span>

### <a name="examples"></a><span data-ttu-id="90b4e-152">Příklad</span><span class="sxs-lookup"><span data-stu-id="90b4e-152">Examples</span></span>

<span data-ttu-id="90b4e-153">Předpokládejme, že vypočítáme 2 kódy daně u transakce:</span><span class="sxs-lookup"><span data-stu-id="90b4e-153">Assume we calculate 2 tax codes on a transaction:</span></span>

-   <span data-ttu-id="90b4e-154">CLO: Původ = částka za jednotku a prodejní daň, hodnota je nastavena na 5,00 za jednotku = kusy</span><span class="sxs-lookup"><span data-stu-id="90b4e-154">DUTY: Origin = Amount per unit and a sales tax, the value is set to 5.00 per unit = pcs</span></span>
-   <span data-ttu-id="90b4e-155">DPH: Původ = jak je uvedeno v následujících příkladech, hodnota je nastavena na hodnotu 25 %</span><span class="sxs-lookup"><span data-stu-id="90b4e-155">SALESTAX: Origin = as shown in the examples below, the value is set to 25%</span></span>

<span data-ttu-id="90b4e-156">Prodáme 1 kus položky za jednotkovou cenu ve výši 10,00</span><span class="sxs-lookup"><span data-stu-id="90b4e-156">We sell 1 piece of an item at a unit price of 10.00</span></span>
#### <a name="example-1"></a><span data-ttu-id="90b4e-157">Příklad 1</span><span class="sxs-lookup"><span data-stu-id="90b4e-157">Example 1</span></span>

<span data-ttu-id="90b4e-158">DPH: Původ = metoda Procento z hrubé částky Možnost Výpočet před DPH nemá žádný vliv, protože DPH se počítá jako procento z hrubé částky.</span><span class="sxs-lookup"><span data-stu-id="90b4e-158">SALESTAX: Origin = Percentage of gross amount method The Calculate before sales tax option has no effect, because SALESTAX is calculated as a percentage of the gross amount.</span></span> <span data-ttu-id="90b4e-159">CLO: 1 x 5,00 = 5,00 Hrubá částka: 10,00 + 5,00 = 15,00 DPH: 15,00 x 25 % = 3,75 Celková částka DPH: 5,00 + 3,75 = 8,75 Celková částka: 10,00 + 8,75 = 18,75</span><span class="sxs-lookup"><span data-stu-id="90b4e-159">DUTY: 1 x 5.00 = 5.00 Gross amount: 10.00 + 5.00 = 15.00 SALESTAX: 15.00 x 25% = 3.75 Total sales tax: 5.00 + 3.75 = 8.75 Total amount: 10.00 + 8.75 = 18.75</span></span>

#### <a name="example-2"></a><span data-ttu-id="90b4e-160">Příklad 2</span><span class="sxs-lookup"><span data-stu-id="90b4e-160">Example 2</span></span>

<span data-ttu-id="90b4e-161">DPH: Původ = procento z čisté částky Možnost Výpočet před DPH není vybrána pro výpočet cla.</span><span class="sxs-lookup"><span data-stu-id="90b4e-161">SALESTAX: Origin = Percentage of net amount The Calculate before sales tax option is not selected for the DUTY calculation.</span></span> <span data-ttu-id="90b4e-162">Čistá částka: 10,00 Clo: 1 x 5,00 = 5,00 DPH: 10,00 x 25 % = 2,50 Celková částka DPH: 5,00 + 2,50 = 7,50 Celková částka: 10,00 + 7,50 = 17,50</span><span class="sxs-lookup"><span data-stu-id="90b4e-162">Net amount: 10.00 DUTY: 1 x 5.00 = 5.00 SALESTAX: 10.00 x 25% = 2.50 Total sales tax: 5.00 + 2.50 = 7.50 Total amount: 10.00 + 7.50 = 17.50</span></span>

#### <a name="example-3"></a><span data-ttu-id="90b4e-163">Příklad 3</span><span class="sxs-lookup"><span data-stu-id="90b4e-163">Example 3</span></span>

<span data-ttu-id="90b4e-164">DPH: Původ = procento z čisté částky Možnost Výpočet před DPH je vybrána pro výpočet cla.</span><span class="sxs-lookup"><span data-stu-id="90b4e-164">SALESTAX: Origin = Percentage of net amount The Calculate before sales tax option is selected for the DUTY calculation.</span></span> <span data-ttu-id="90b4e-165">Čistá částka: 10,00 Clo: 1 x 5,00 = 5,00 DPH: (10,00 + 5,00) x 25 % = 3,75 Celková částka DPH: 5,00 + 3,75 = 8,75 Celková částka: 10,00 + 8,75 = 18,75</span><span class="sxs-lookup"><span data-stu-id="90b4e-165">Net amount: 10.00 DUTY: 1 x 5.00 = 5.00 SALESTAX: (10.00 + 5.00) x 25% = 3.75 Total sales tax: 5.00 + 3.75 = 8.75 Total amount: 10.00 + 8.75 = 18.75</span></span>

#### <a name="example-4"></a><span data-ttu-id="90b4e-166">Příklad 4</span><span class="sxs-lookup"><span data-stu-id="90b4e-166">Example 4</span></span>

<span data-ttu-id="90b4e-167">Výsledek příkladu 3 a příkladu 1 je stejný, protože se počítá pouze s jedním clem.</span><span class="sxs-lookup"><span data-stu-id="90b4e-167">The result of Example 3 and Example 1 is the same, because there is only one duty.</span></span> <span data-ttu-id="90b4e-168">Předpokládejme, že máte dvě cla, a pouze jedno z nich je součástí čisté částky pro výpočet DPH: Clo 1: 5,00, pomocí metody Částka za jednotku a možnost Výpočet před DPH je vybrána Clo 2: 2,50, pomocí metody Částka za jednotku a možnost Výpočet před DPH není vybrána DPH: 25 %, pomocí metody Procento čisté částky Čistá částka: 10,00 Clo 1: 1 x 5,00 = 5,00 Clo 2: 1 x 2,50 = 2,50 Čistá částka podléhá DPH: 10,00 + 5,00 = 15,00 DPH: 15,00 x 25 % = 3,75 Celková DPH včetně cel: 5,00 + 2,50 + 3,75 = 11,25 Celková částka: 10,00 + 11,25 = 21,25 DPH 25 % je vypočítáno pro součet čisté částky (10,00) + cla 1 (5,00) = 15,00.</span><span class="sxs-lookup"><span data-stu-id="90b4e-168">Assume that you have two DUTIES, and only one of them is included in the net amount for the sales tax calculation: DUTY 1: 5.00, using the Amount per unit method, and the Calculate before sales tax option is selected DUTY 2: 2.50, using the Amount per unit method, and the Calculate before sales tax option is not selected Sales tax: 25%, using the Percentage of net amount method Net amount: 10.00 DUTY 1: 1 x 5.00 = 5.00 DUTY 2: 1 x 2.50 = 2.50 Net amount subject to sales tax: 10.00 + 5.00 = 15.00 SALESTAX: 15.00 x 25% = 3.75 Total sales taxes, including duties: 5.00 + 2.50 + 3.75 = 11.25 Total amount: 10.00 + 11.25 = 21.25 The 25% SALESTAX is calculated for the sum of the net amount (10.00) + DUTY 1 (5.00) = 15.00.</span></span> <span data-ttu-id="90b4e-169">Clo 2 je k částce daně přičteno po výpočtu DPH.</span><span class="sxs-lookup"><span data-stu-id="90b4e-169">DUTY 2 is added to the tax amount after the sales tax is calculated.</span></span>

## <a name="calculated-percentage-of-net-amount"></a><span data-ttu-id="90b4e-170"> Vypočtené procento čisté částky</span><span class="sxs-lookup"><span data-stu-id="90b4e-170">Calculated percentage of net amount</span></span>
<span data-ttu-id="90b4e-171">Vypočtené procento čisté částky řídí výpočet daně jiným způsobem v závislosti na nastavení parametru Částky včetně DPH pro deník nebo doklad.</span><span class="sxs-lookup"><span data-stu-id="90b4e-171">The Calculated percentage of net amount handles tax calculation differently depending on the setting of the Amounts include sales tax parameter for the document or journal.</span></span>
### <a name="example-1"></a><span data-ttu-id="90b4e-172">Příklad 1</span><span class="sxs-lookup"><span data-stu-id="90b4e-172">Example 1</span></span>

<span data-ttu-id="90b4e-173">Dokument / deník je nastaven na Částky včetně DPH = Ano Částka řádku transakce: 10,00 Sazba daně: 25 % DPH: Částka řádku transakce x sazba daně (10,00 x 25 %) = 2,50 Částka základu daně (původ částky): Částka řádku transakce - prodejní daň (10,00 - 2,50) = 7,50</span><span class="sxs-lookup"><span data-stu-id="90b4e-173">Document / journal is set to Amounts include sales tax = Yes Transaction line amount: 10.00 Tax rate: 25% Sales tax: Transaction line amount x tax rate (10.00 x 25%) = 2.50 Tax base amount (origin amount): Transaction line amount - Sales tax (10.00 - 2.50) = 7.50</span></span>

### <a name="example-2"></a><span data-ttu-id="90b4e-174">Příklad 2</span><span class="sxs-lookup"><span data-stu-id="90b4e-174">Example 2</span></span>

<span data-ttu-id="90b4e-175">Dokument / deník je nastaven na Částky včetně DPH = Ne Částka řádku transakce: 10,00 Sazba daně: 25 % DPH: (Částka řádku transakce x sazba daně) / (100 - sazba daně) (10,00 x 25 %) / (100 % - 25 %) = 3,33 Částka základu daně (původ částky): Částka řádku transakce = 10,00</span><span class="sxs-lookup"><span data-stu-id="90b4e-175">Document / journal is set to Amounts include sales tax = No Transaction line amount: 10.00 Tax rate: 25% Sales tax: (Transaction line amount x tax rate) / (100 - tax rate) (10.00 x 25%) / (100% - 25%) = 3.33 Tax base amount (origin amount): Transaction line amount = 10.00</span></span>



<a name="additional-resources"></a><span data-ttu-id="90b4e-176">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="90b4e-176">Additional resources</span></span>
--------

[<span data-ttu-id="90b4e-177">Sazby DPH na základě polí Základ marže a Metody výpočtu</span><span class="sxs-lookup"><span data-stu-id="90b4e-177">Sales tax rates based on the Marginal base and Calculation methods</span></span>](marginal-base-field.md)

[<span data-ttu-id="90b4e-178">Možnosti výpočtu celé částky a intervalu pro kódy daně z prodeje</span><span class="sxs-lookup"><span data-stu-id="90b4e-178">Whole amount and Interval calculation options for sales tax codes</span></span>](whole-amount-interval-options-sales-tax-codes.md)



