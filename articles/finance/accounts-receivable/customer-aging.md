---
title: Sestava sledování prodlení odběratele
description: Sestava sledování prodlení odběratele zobrazuje zůstatky splatné odběrateli, které jsou seřazeny podle časového intervalu nebo období pro sledování splatnosti.
author: JodiChristiansen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 384e44ef07771a174aaed4f8fb893e75b0206da7
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5236979"
---
# <a name="customer-aging-report"></a><span data-ttu-id="1f3ae-103">Sestava sledování prodlení odběratele</span><span class="sxs-lookup"><span data-stu-id="1f3ae-103">Customer aging report</span></span> 

<span data-ttu-id="1f3ae-104">Sestava **sledování prodlení odběratele** zobrazuje zůstatky splatné odběrateli, které jsou seřazeny podle časového intervalu nebo období pro sledování splatnosti.</span><span class="sxs-lookup"><span data-stu-id="1f3ae-104">The **Customer aging** report displays the balances that are due from customers, sorted by date interval, or aging period.</span></span>

<span data-ttu-id="1f3ae-105">Při generování této sestavy se zobrazují následující výchozí parametry.</span><span class="sxs-lookup"><span data-stu-id="1f3ae-105">When you generate this report, the following default parameters are displayed.</span></span> <span data-ttu-id="1f3ae-106">Parametry sestavy slouží k filtrování dat, která se zobrazí v sestavě.</span><span class="sxs-lookup"><span data-stu-id="1f3ae-106">You can use these parameters to filter the data that will be displayed on the report.</span></span> <span data-ttu-id="1f3ae-107">Další informace naleznete v tématu [Nastavení kolekcí](set-up-collections.md).</span><span class="sxs-lookup"><span data-stu-id="1f3ae-107">For more information, see [Set up collections](set-up-collections.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1f3ae-108">Pole</span><span class="sxs-lookup"><span data-stu-id="1f3ae-108">Field</span></span></p></th>
<th><p><span data-ttu-id="1f3ae-109">popis</span><span class="sxs-lookup"><span data-stu-id="1f3ae-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1f3ae-110"><strong>Účtovací klasifikace</strong></span><span class="sxs-lookup"><span data-stu-id="1f3ae-110"><strong>Billing classification</strong></span></span></p></td>
<td><p><span data-ttu-id="1f3ae-111">Vyberte jednu nebo více účtovacích klasifikací, které chcete zahrnout do sestavy.</span><span class="sxs-lookup"><span data-stu-id="1f3ae-111">Select one or more billing classifications to include on the report.</span></span></p>
<div class="alert">

<span data-ttu-id="1f3ae-112">**Poznámka:** Tento ovládací prvek je k dispozici pouze v případě, že je zvolen konfigurační klíč pro <STRONG>veřejný sektor</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="1f3ae-112">**Note:** This control is available only if the <STRONG>Public Sector</STRONG> configuration key is selected.</span></span></P>


</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f3ae-113"><strong>Zahrnout transakce bez účtovací klasifikace</strong></span><span class="sxs-lookup"><span data-stu-id="1f3ae-113"><strong>Include transactions without a billing classification</strong></span></span></p></td>
<td><p><span data-ttu-id="1f3ae-114">Pokud je toto políčko zaškrtnuto, zobrazí se v sestavě všechny transakce, které nemají přiřazenou účtovací klasifikaci.</span><span class="sxs-lookup"><span data-stu-id="1f3ae-114">If this check box is selected, all transactions that do not have a billing classification assigned to them will be displayed on the report.</span></span></p>
<div class="alert">

<span data-ttu-id="1f3ae-115">**Poznámka:** Tento ovládací prvek je k dispozici pouze v případě, že je zvolen konfigurační klíč pro <STRONG>veřejný sektor</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="1f3ae-115">**Note:** This control is available only if the <STRONG>Public sector</STRONG> configuration key is selected.</span></span></P>

</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f3ae-116"><strong>Sledování splatnosti k</strong></span><span class="sxs-lookup"><span data-stu-id="1f3ae-116"><strong>Aging as of</strong></span></span></p></td>
<td><p><span data-ttu-id="1f3ae-117">Zadejte datum použité v aktuálním intervalu prodlení.</span><span class="sxs-lookup"><span data-stu-id="1f3ae-117">Enter the date used on the current aging bucket.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f3ae-118"><strong>Zůstatek k</strong></span><span class="sxs-lookup"><span data-stu-id="1f3ae-118"><strong>Balance as of</strong></span></span></p></td>
<td><p><span data-ttu-id="1f3ae-119">Zadejte datum, k němuž chcete zobrazit zůstatky odběratelů.</span><span class="sxs-lookup"><span data-stu-id="1f3ae-119">Enter the date to view the customer balances for.</span></span> <span data-ttu-id="1f3ae-120">Označuje se také jako datum přerušení transakcí.</span><span class="sxs-lookup"><span data-stu-id="1f3ae-120">This is also known as a cutoff date for transactions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f3ae-121"><strong>Datum zahájení</strong></span><span class="sxs-lookup"><span data-stu-id="1f3ae-121"><strong>Start date</strong></span></span></p></td>
<td><p><span data-ttu-id="1f3ae-122">Zadejte datum ležící v intervalu prvního období nebo období pro sledování splatnosti, které má být zahrnuto do sestavy.</span><span class="sxs-lookup"><span data-stu-id="1f3ae-122">Enter a date that is in the first period interval or aging period to include on the report.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f3ae-123"><strong>Kritéria</strong></span><span class="sxs-lookup"><span data-stu-id="1f3ae-123"><strong>Criteria</strong></span></span></p></td>
<td><p><span data-ttu-id="1f3ae-124">Vyberte typ kalendářního data, na kterém má být sestava založena.</span><span class="sxs-lookup"><span data-stu-id="1f3ae-124">Select the type of date to base the report on.</span></span></p>
<ul>
<li><p><span data-ttu-id="1f3ae-125"><strong>Datum transakce</strong> – datum zaúčtování transakcí.</span><span class="sxs-lookup"><span data-stu-id="1f3ae-125"><strong>Transaction date</strong> – The posting date of the transactions.</span></span> <span data-ttu-id="1f3ae-126">Může to být například datum faktury, které je základem pro výpočet data splatnosti.</span><span class="sxs-lookup"><span data-stu-id="1f3ae-126">For example, this might be an invoice date that is the basis for the calculation of the due date.</span></span></p></li>
<li><p><span data-ttu-id="1f3ae-127"><strong>Datum splatnosti</strong> – datum splatnosti transakcí na základě platebních podmínek.</span><span class="sxs-lookup"><span data-stu-id="1f3ae-127"><strong>Due date</strong> – The due date of the transactions, based on the terms of payment.</span></span></p></li>
<li><p><span data-ttu-id="1f3ae-128"><strong>Datum dokladu</strong> – uživatelem definované datum dokladu, které je základem pro výpočet data splatnosti.</span><span class="sxs-lookup"><span data-stu-id="1f3ae-128"><strong>Document date</strong> – A user-defined document date that is the basis for the calculation of the due date.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f3ae-129"><strong>Definice období pro sledování splatnosti</strong></span><span class="sxs-lookup"><span data-stu-id="1f3ae-129"><strong>Aging period definition</strong></span></span></p></td>
<td><p><span data-ttu-id="1f3ae-130">Vyberte definici období pro sledování splatnosti.</span><span class="sxs-lookup"><span data-stu-id="1f3ae-130">Select an aging period definition.</span></span> <span data-ttu-id="1f3ae-131">Pokud vyberete definici období pro sledování splatnosti, pole <strong>Interval</strong> se nepoužije.</span><span class="sxs-lookup"><span data-stu-id="1f3ae-131">The <strong>Interval</strong> field is not used if you select an aging period definition.</span></span></p>
<p><span data-ttu-id="1f3ae-132">V tištěné sestavě nelze použít definice období pro sledování splatnosti, které mají více než šest období pro sledování splatnosti.</span><span class="sxs-lookup"><span data-stu-id="1f3ae-132">Aging period definitions that have more than six aging periods cannot be used on the printed report.</span></span></p>
<div class="alert">

<span data-ttu-id="1f3ae-133">**Poznámka:** Období pro sledování splatnosti můžete nastavit na stránce <STRONG>Definice období pro sledování splatnosti</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="1f3ae-133">**Note:** You can set up aging periods on the <STRONG>Aging period definitions</STRONG> page.</span></span></P>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f3ae-134"><strong>Tisk popisu období pro sledování splatnosti</strong></span><span class="sxs-lookup"><span data-stu-id="1f3ae-134"><strong>Print aging period description</strong></span></span></p></td>
<td><p><span data-ttu-id="1f3ae-135">Chcete-li zahrnout popisy období pro sledování splatnosti do záhlaví sloupce každého období pro sledování splatnosti, zaškrtněte políčko <strong>Ano</strong>.</span><span class="sxs-lookup"><span data-stu-id="1f3ae-135">Select <strong>Yes</strong> to include aging period descriptions at the top of each aging period column on the report.</span></span> <span data-ttu-id="1f3ae-136">Vyberte <strong>Ne</strong>, pokud chcete sestavu vytisknout bez záhlaví sloupců.</span><span class="sxs-lookup"><span data-stu-id="1f3ae-136">Select <strong>No</strong> to print the report without column headers.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f3ae-137"><strong>Interval</strong></span><span class="sxs-lookup"><span data-stu-id="1f3ae-137"><strong>Interval</strong></span></span></p></td>
<td><p><span data-ttu-id="1f3ae-138">Zadáním počtu jednotek dnů nebo měsíců v každém období definujte použité období.</span><span class="sxs-lookup"><span data-stu-id="1f3ae-138">Define the period to use by entering the number of the day or month units in each period.</span></span> <span data-ttu-id="1f3ae-139">Chcete-li například zobrazit informace o sledování splatnosti podle týdne, zadejte do tohoto pole hodnotu 7 a vyberte možnost <strong>Den</strong> v poli <strong>Den/měsíc</strong>.</span><span class="sxs-lookup"><span data-stu-id="1f3ae-139">For example, to view aging information by week, enter 7 in this field and select <strong>Day</strong> in the <strong>Day/Mth</strong> field.</span></span></p>
<div class="alert">

<span data-ttu-id="1f3ae-140">**Poznámka:** Informace zadané v tomto poli se použijí jen tehdy, když nebyla vybrána definice období pro sledování splatnosti.</span><span class="sxs-lookup"><span data-stu-id="1f3ae-140">**Note:** The information that you enter in this field is used only if you have not selected an aging period definition.</span></span> <span data-ttu-id="1f3ae-141">V opačném případě je směr tisku definován v definici období pro sledování splatnosti.</span><span class="sxs-lookup"><span data-stu-id="1f3ae-141">Otherwise, the printing direction is defined on the aging period definition.</span></span></P>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f3ae-142"><strong>Den/měs.</strong></span><span class="sxs-lookup"><span data-stu-id="1f3ae-142"><strong>Day/Mth</strong></span></span></p></td>
<td><p><span data-ttu-id="1f3ae-143">V poli <strong>Interval</strong> vyberte jednotku <strong>Den</strong> nebo <strong>Měsíc</strong>, která se použije k definování období.</span><span class="sxs-lookup"><span data-stu-id="1f3ae-143">Select the unit, either <strong>Day</strong> or <strong>Month</strong>, that is used to define the period in the <strong>Interval</strong> field.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f3ae-144"><strong>Pokyn pro tisk</strong></span><span class="sxs-lookup"><span data-stu-id="1f3ae-144"><strong>Printing direction</strong></span></span></p></td>
<td><p><span data-ttu-id="1f3ae-145">Vyberte, zda chcete vypočítat zůstatky a vytisknout sestavu sledování prodlení za minulá nebo budoucí období.</span><span class="sxs-lookup"><span data-stu-id="1f3ae-145">Select whether to calculate balances and print the aging report for past or future periods.</span></span> <span data-ttu-id="1f3ae-146">Kalendářní data se vyhodnocují vzhledem k datu, které je vybráno v poli <strong>Zůstatek ke dni</strong>.</span><span class="sxs-lookup"><span data-stu-id="1f3ae-146">The dates are evaluated relative to the date that is selected in the <strong>Balance as on</strong> field.</span></span> <span data-ttu-id="1f3ae-147">Výběrem položky <strong>Vzad</strong> zobrazíte informace o minulých obdobích.</span><span class="sxs-lookup"><span data-stu-id="1f3ae-147">Select <strong>Backward</strong> to show information for past periods.</span></span> <span data-ttu-id="1f3ae-148">Výběrem položky <strong>Vpřed</strong> zobrazíte informace o budoucích obdobích.</span><span class="sxs-lookup"><span data-stu-id="1f3ae-148">Select <strong>Forward</strong> to show information for future periods.</span></span></p>
<div class="alert"><span data-ttu-id="1f3ae-149">
  
<STRONG>Poznámka:</STRONG> Informace zadané v tomto poli se použijí jen tehdy, když nebyla vybrána definice období pro sledování splatnosti.</span><span class="sxs-lookup"><span data-stu-id="1f3ae-149">
  
<STRONG>Note:</STRONG> The information that you enter in this field is used only if you have not selected an aging period definition.</span></span></P>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f3ae-150"><strong>Podrobnosti</strong></span><span class="sxs-lookup"><span data-stu-id="1f3ae-150"><strong>Details</strong></span></span></p></td>
<td><p><span data-ttu-id="1f3ae-151">Zaškrtnutím tohoto políčka vypíšete transakce, které jsou zahrnuté do zůstatků zobrazených v sestavě.</span><span class="sxs-lookup"><span data-stu-id="1f3ae-151">Select to list the transactions that are included in the balances that are shown on the report.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f3ae-152"><strong>Zahrnout částky v měně transakce</strong></span><span class="sxs-lookup"><span data-stu-id="1f3ae-152"><strong>Include amounts in transaction currency</strong></span></span></p></td>
<td><p><span data-ttu-id="1f3ae-153">Zaškrtnutím tohoto políčka zahrnete částky v měně transakce navíc k částkám v zúčtovací měně.</span><span class="sxs-lookup"><span data-stu-id="1f3ae-153">Select to include amounts in the transaction currency in addition to amounts in the accounting currency.</span></span> <span data-ttu-id="1f3ae-154">Pokud toto políčko není zaškrtnuto, zobrazí se v sestavě jen částky v zúčtovací měně.</span><span class="sxs-lookup"><span data-stu-id="1f3ae-154">If this check box is not selected, the amounts on the report are displayed only in the accounting currency.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f3ae-155"><strong>Záporné zůstatek</strong></span><span class="sxs-lookup"><span data-stu-id="1f3ae-155"><strong>Negative balance</strong></span></span></p></td>
<td><p><span data-ttu-id="1f3ae-156">Zaškrtnutím tohoto políčka zahrnete účty odběratelů se zápornými zůstatky.</span><span class="sxs-lookup"><span data-stu-id="1f3ae-156">Select to include customer accounts that have negative balances.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f3ae-157"><strong>Vyloučit účty s nulovým zůstatkem</strong></span><span class="sxs-lookup"><span data-stu-id="1f3ae-157"><strong>Exclude zero balance accounts</strong></span></span></p></td>
<td><p><span data-ttu-id="1f3ae-158">Zaškrtnutím tohoto políčka vyloučíte účty odběratelů s nulovým zůstatkem.</span><span class="sxs-lookup"><span data-stu-id="1f3ae-158">Select to exclude customer accounts that have a zero balance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f3ae-159"><strong>Umístění platby</strong></span><span class="sxs-lookup"><span data-stu-id="1f3ae-159"><strong>Payment positioning</strong></span></span></p></td>
<td><p><span data-ttu-id="1f3ae-160">Zaškrtnutím tohoto políčka zobrazíte platby, které nebyly vyrovnány.</span><span class="sxs-lookup"><span data-stu-id="1f3ae-160">Select to display payments that have not been settled.</span></span> <span data-ttu-id="1f3ae-161">Zobrazují se v prvním sloupci sestavy.</span><span class="sxs-lookup"><span data-stu-id="1f3ae-161">These are displayed in the first column of the report.</span></span></p></td>
</tr>
</tbody>
</table>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]