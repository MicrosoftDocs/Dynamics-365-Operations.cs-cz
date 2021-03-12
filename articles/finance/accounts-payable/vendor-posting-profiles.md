---
title: Účetní profil dodavatele
description: Účetní profil dodavatele řídí zaúčtování transakcí dodavatelů do hlavní knihy
author: abruer
manager: AnnBe
ms.date: 06/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPosting
audience: Application User
ms.reviewer: roschlom
ms.custom: 24691
ms.assetid: 18def866-7655-4f0b-b299-eec83098d23a
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8b6447228f00d91fd2dddd43c1ceb57dff0c6df9
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4979182"
---
# <a name="vendor-posting-profiles"></a><span data-ttu-id="e1251-103">Účetní profil dodavatele</span><span class="sxs-lookup"><span data-stu-id="e1251-103">Vendor posting profiles</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e1251-104">Účetní profil dodavatele řídí zaúčtování transakcí dodavatelů do hlavní knihy</span><span class="sxs-lookup"><span data-stu-id="e1251-104">Vendor posting profiles control the posting of vendor transactions to the general ledger.</span></span>

<a name="vendor-posting-profiles"></a><span data-ttu-id="e1251-105">Účetní profil dodavatele</span><span class="sxs-lookup"><span data-stu-id="e1251-105">Vendor posting profiles</span></span>
-----------------------

<span data-ttu-id="e1251-106">Účetní profily dodavatelů umožňují přiřazení účtů hlavní knihy a nastavení dokumentů ke všem dodavatelům, skupině dodavatelů nebo jednomu dodavateli.</span><span class="sxs-lookup"><span data-stu-id="e1251-106">Vendor posting profiles enable you to assign general ledger accounts and document settings to all vendors, a group of vendors, or a single vendor.</span></span> <span data-ttu-id="e1251-107">Toto nastavení se použije při vytváření nákupních objednávek, faktur dodavatele a plateb v hotovosti.</span><span class="sxs-lookup"><span data-stu-id="e1251-107">These settings will be used when you create purchase orders, vendor invoices, and cash payments.</span></span> <span data-ttu-id="e1251-108">U některých transakcí je možné vybrat účetní profil, který se odlišuje od účetních profilů nastavených pro transakce na této stránce a má před nimi přednost.</span><span class="sxs-lookup"><span data-stu-id="e1251-108">For some transactions, you can select a posting profile that differs from and takes precedence over the posting profiles that are set up for transactions on this page.</span></span> <span data-ttu-id="e1251-109">Výchozí účetní profil je definován na záložce s náhledem **Hlavní kniha a DPH** na stránce **Parametry závazků**.</span><span class="sxs-lookup"><span data-stu-id="e1251-109">The default posting profile is defined on the **Ledger and Sales Tax** FastTab on the **Accounts payable parameters** page.</span></span> <span data-ttu-id="e1251-110">Výchozí účetní profil je poté následně automaticky zahrnut do záhlaví nových dokumentů, kde jej můžete změnit na jiný účetní profil v případě potřeby.</span><span class="sxs-lookup"><span data-stu-id="e1251-110">The default posting profile is then included automatically on the header of new documents where you can change it to a different posting profile, if needed.</span></span>

<span data-ttu-id="e1251-111">Můžete také přiřadit definice účtování k typům účtování transakcí na stránce **Definice účtování transakce**.</span><span class="sxs-lookup"><span data-stu-id="e1251-111">You can also associate posting definitions with transaction posting types on the **Transaction posting definitions** page.</span></span> <span data-ttu-id="e1251-112">Definice účtování určují zaúčtování transakcí dodavatelů do hlavní knihy místo účetních profilů.</span><span class="sxs-lookup"><span data-stu-id="e1251-112">Posting definitions control the posting of vendor transactions to the general ledger instead of posting profiles.</span></span>

## <a name="creating-a-posting-profile"></a><span data-ttu-id="e1251-113">Vytvoření účetního profilu</span><span class="sxs-lookup"><span data-stu-id="e1251-113">Creating a posting profile</span></span>
### <a name="setup"></a><span data-ttu-id="e1251-114">**Nastavení**</span><span class="sxs-lookup"><span data-stu-id="e1251-114">**Setup**</span></span>

<span data-ttu-id="e1251-115">Určete účty hlavní knihy, které jsou použity při zaúčtování transakcí s vybraným účetním profilem.</span><span class="sxs-lookup"><span data-stu-id="e1251-115">Specify the ledger accounts that are used in the posting of transactions that use the selected posting profile.</span></span> <span data-ttu-id="e1251-116">Vyberte kód účtu a je-li to možné, i číslo účtu nebo skupiny vybraného účetního profilu.</span><span class="sxs-lookup"><span data-stu-id="e1251-116">Select an account code and, whenever possible, an account or group number for the selected posting profile.</span></span> <span data-ttu-id="e1251-117">V procesu zaúčtování bude nejvhodnější účetní profil pro každou transakci nalezen vyhledáním nejspecifičtější kombinace kódu účtu, čísla účtu nebo kombinace skupiny a čísla s následující prioritou.</span><span class="sxs-lookup"><span data-stu-id="e1251-117">In the posting process, the most appropriate posting profile for each transaction is located by searching for the most specific account code, account number, or group and number combination in the following priority.</span></span>

| <span data-ttu-id="e1251-118">Hodnota pole **Kód účtu**</span><span class="sxs-lookup"><span data-stu-id="e1251-118">**Account code** field value</span></span> | <span data-ttu-id="e1251-119">Hodnota pole **Číslo účtu/skupiny**</span><span class="sxs-lookup"><span data-stu-id="e1251-119">**Account/Group number** field value</span></span>        | <span data-ttu-id="e1251-120">Priorita hledání</span><span class="sxs-lookup"><span data-stu-id="e1251-120">Search priority</span></span> |
|------------------------------|---------------------------------------------|-----------------|
| <span data-ttu-id="e1251-121">**Tabulka**</span><span class="sxs-lookup"><span data-stu-id="e1251-121">**Table**</span></span>                    | <span data-ttu-id="e1251-122">Konkrétní účet dodavatele</span><span class="sxs-lookup"><span data-stu-id="e1251-122">Specific vendor account</span></span>                     | <span data-ttu-id="e1251-123">1</span><span class="sxs-lookup"><span data-stu-id="e1251-123">1</span></span>               |
| <span data-ttu-id="e1251-124">**Seskupit**</span><span class="sxs-lookup"><span data-stu-id="e1251-124">**Group**</span></span>                    | <span data-ttu-id="e1251-125">Skupina dodavatelů, která je přiřazena dodavateli</span><span class="sxs-lookup"><span data-stu-id="e1251-125">Vendor group that is assigned to the vendor</span></span> | <span data-ttu-id="e1251-126">2</span><span class="sxs-lookup"><span data-stu-id="e1251-126">2</span></span>               |
| <span data-ttu-id="e1251-127">**Vše**</span><span class="sxs-lookup"><span data-stu-id="e1251-127">**All**</span></span>                      | <span data-ttu-id="e1251-128">Formulář</span><span class="sxs-lookup"><span data-stu-id="e1251-128">Blank</span></span>                                       | <span data-ttu-id="e1251-129">3</span><span class="sxs-lookup"><span data-stu-id="e1251-129">3</span></span>               |

<span data-ttu-id="e1251-130">Pokud chcete, aby všechny transakce dodavatele měly shodný účetní profil, nastavte pouze jeden účetní profil s hodnotou **Vše** v poli **Kód účtu**.</span><span class="sxs-lookup"><span data-stu-id="e1251-130">If you want all vendor transactions to have the same posting profile, set up only one posting profile with **All** in the **Account code** field.</span></span> <span data-ttu-id="e1251-131">Zadejte následující hodnoty pro nastavení účetního profilu.</span><span class="sxs-lookup"><span data-stu-id="e1251-131">Specify the following values to set up your posting profile.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e1251-132">Pole</span><span class="sxs-lookup"><span data-stu-id="e1251-132">Field</span></span></th>
<th><span data-ttu-id="e1251-133">Popis</span><span class="sxs-lookup"><span data-stu-id="e1251-133">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e1251-134"><strong>Účetní profil</strong></span><span class="sxs-lookup"><span data-stu-id="e1251-134"><strong>Posting profile</strong></span></span></td>
<td><span data-ttu-id="e1251-135">Zadejte kód účetního profilu.</span><span class="sxs-lookup"><span data-stu-id="e1251-135">Enter a code for the posting profile.</span></span> <span data-ttu-id="e1251-136">Můžete například vytvořit dva účetní profily a získat jeden účet pro rozvahy dodavatele v národní měně a jiný účet pro rozvahy v měně cizí.</span><span class="sxs-lookup"><span data-stu-id="e1251-136">For example, you could create two posting profiles to obtain one account for vendor balances in the national currency and another for vendor balances in a foreign currency.</span></span> <span data-ttu-id="e1251-137">Jeden účet byste měli nazvat "národní" a druhý "cizí".</span><span class="sxs-lookup"><span data-stu-id="e1251-137">You could call one account National and the other Foreign.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e1251-138"><strong>Popis</strong></span><span class="sxs-lookup"><span data-stu-id="e1251-138"><strong>Description</strong></span></span></td>
<td><span data-ttu-id="e1251-139">Zadejte popis účetního profilu.</span><span class="sxs-lookup"><span data-stu-id="e1251-139">Enter a description of the posting profile.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e1251-140"><strong>Kód účtu</strong></span><span class="sxs-lookup"><span data-stu-id="e1251-140"><strong>Account code</strong></span></span></td>
<td><span data-ttu-id="e1251-141">Zadejte, zda se účetní profil týká specifického dodavatele, skupiny dodavatelů nebo všech dodavatelů:</span><span class="sxs-lookup"><span data-stu-id="e1251-141">Specify whether the posting profile applies to a specific vendor, a group of vendors, or all vendors:</span></span>
<ul>
<li><span data-ttu-id="e1251-142"><strong>Tabulka</strong> – Účetní profil platí pro jednoho dodavatele.</span><span class="sxs-lookup"><span data-stu-id="e1251-142"><strong>Table</strong> – The posting profile applies to a single vendor.</span></span> <span data-ttu-id="e1251-143">Vyberte účet dodavatele v poli <strong>Číslo účtu/skupiny</strong>.</span><span class="sxs-lookup"><span data-stu-id="e1251-143">Select the vendor account in the <strong>Account/Group number</strong> field.</span></span></li>
<li><span data-ttu-id="e1251-144"><strong>Skupina</strong> – Účetní profil platí pro skupinu dodavatelů.</span><span class="sxs-lookup"><span data-stu-id="e1251-144"><strong>Group</strong> – The posting profile applies to a vendor group.</span></span> <span data-ttu-id="e1251-145">Vyberte skupinu dodavatelů v poli <strong>Číslo účtu/skupiny</strong>.</span><span class="sxs-lookup"><span data-stu-id="e1251-145">Select the vendor group in the <strong>Account/Group number</strong> field.</span></span></li>
<li><span data-ttu-id="e1251-146"><strong>Vše</strong> – Účetní profil platí pro všechny dodavatele.</span><span class="sxs-lookup"><span data-stu-id="e1251-146"><strong>All</strong> – The posting profile applies to all vendors.</span></span> <span data-ttu-id="e1251-147">Pole <strong>Číslo účtu/skupiny</strong> ponechejte prázdné.</span><span class="sxs-lookup"><span data-stu-id="e1251-147">Leave the <strong>Account/Group number</strong> field blank.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e1251-148"><strong>Číslo účtu/skupiny</strong></span><span class="sxs-lookup"><span data-stu-id="e1251-148"><strong>Account/Group number</strong></span></span></td>
<td><span data-ttu-id="e1251-149">Pokud vyberete možnost <strong>Tabulka</strong> v poli <strong>Kód účtu</strong>, zvolte číslo účtu dodavatele přiřazeného k účetnímu profilu.</span><span class="sxs-lookup"><span data-stu-id="e1251-149">If <strong>Table</strong> is selected in the <strong>Account code</strong> field, select the account number of the vendor that is associated with the posting profile.</span></span> <span data-ttu-id="e1251-150">Pokud vyberete možnost <strong>Skupina</strong>, zvolte skupinu dodavatelů.</span><span class="sxs-lookup"><span data-stu-id="e1251-150">If <strong>Group</strong> is selected, select a vendor group.</span></span> <span data-ttu-id="e1251-151">Pokud je vybrána možnost <strong>Vše</strong>, ponechte toto pole prázdné.</span><span class="sxs-lookup"><span data-stu-id="e1251-151">If <strong>All</strong> is selected, leave this field blank.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e1251-152"><strong>Součtový účet</strong></span><span class="sxs-lookup"><span data-stu-id="e1251-152"><strong>Summary account</strong></span></span></td>
<td><span data-ttu-id="e1251-153">Vyberte účet hlavní knihy, který se má použít jako součtový účet pro dodavatele, se kterým účetní profil souvisí.</span><span class="sxs-lookup"><span data-stu-id="e1251-153">Select the ledger account that will be used as the summary account for the vendors that the posting profile relates to.</span></span> <span data-ttu-id="e1251-154">Bude označen parametr <strong>Nepovolit ruční zadávání</strong> pro tento hlavní účet.</span><span class="sxs-lookup"><span data-stu-id="e1251-154">The <strong>Do not allow manual entry</strong> parameter for this main account will be marked.</span></span> <span data-ttu-id="e1251-155">Pokud následně tento účet odeberete z účetního profilu, ověřte nastavení možnost i<strong>Nepovolit ruční zadávání</strong> na stránce <strong>Hlavní účty</strong>.</span><span class="sxs-lookup"><span data-stu-id="e1251-155">If you subsequently remove this account from the posting profile, validate the <strong>Do not allow manual entry</strong> setting on the <strong>Main accounts</strong> page.</span></span> 
<p><span data-ttu-id="e1251-156"><strong>Poznámka:</strong> Je-li na stránce <strong>Parametry hlavní knihy</strong> vybrána možnost <strong>Použít definice účtování</strong>, použije se místo souhrnného účtu definici účtování transakce pro faktury dodavatele.</span><span class="sxs-lookup"><span data-stu-id="e1251-156"><strong>Note:</strong> If the <strong>Use posting definitions</strong> option is selected on the <strong>General ledger parameters</strong> page, the transaction posting definition for vendor invoices is used instead of the summary account.</span></span></p>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="e1251-157"><strong>Účet vyrovnání</strong></span><span class="sxs-lookup"><span data-stu-id="e1251-157"><strong>Settle account</strong></span></span></td>
<td><span data-ttu-id="e1251-158">Vyberte účet hlavní knihy likvidity použitý pro prognózy cash-flow.</span><span class="sxs-lookup"><span data-stu-id="e1251-158">Select the liquidity ledger account that is used for cash flow forecasts.</span></span> <span data-ttu-id="e1251-159">Toto pole je k dispozici, pouze když je povolena prognóza cashflow.</span><span class="sxs-lookup"><span data-stu-id="e1251-159">This fields is only available when cash flow forecasting is enabled.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e1251-160"><strong>Zálohy DPH</strong></span><span class="sxs-lookup"><span data-stu-id="e1251-160"><strong>Sales tax prepayments</strong></span></span></td>
<td><span data-ttu-id="e1251-161">Vyberte účet pro zálohy na platby DPH.</span><span class="sxs-lookup"><span data-stu-id="e1251-161">Select the account for sales tax payments that are received in advance.</span></span>
<p><span data-ttu-id="e1251-162"><strong>Poznámka:</strong> Účetní profil používaný při označení platby jako zálohy je vybrán v poli <strong>Účetní profil</strong> s polem <strong>Zálohový doklad deníku</strong> v oblasti <strong>Hlavní kniha a DPH</strong> na stránce <strong>Parametry závazků</strong>.</span><span class="sxs-lookup"><span data-stu-id="e1251-162"><strong>Note:</strong> The posting profile that is used when the payment is marked as a prepayment is selected in the <strong>Posting</strong> profile with <strong>Prepayment journal voucher</strong> field in the <strong>Ledger and sales tax</strong> area on the <strong>Accounts payable parameters</strong> page.</span></span></p>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="e1251-163"><strong>Doručení</strong></span><span class="sxs-lookup"><span data-stu-id="e1251-163"><strong>Arrival</strong></span></span></td>
<td><span data-ttu-id="e1251-164">Vyberte účet hlavní knihy, do kterého jsou zaúčtovány informace o neschválených fakturách dodavatele.</span><span class="sxs-lookup"><span data-stu-id="e1251-164">Select the ledger account that information about unapproved vendor invoices is posted to.</span></span> <span data-ttu-id="e1251-165">Informace jsou zaznamenány do deníku registrů faktur.</span><span class="sxs-lookup"><span data-stu-id="e1251-165">The information is entered in the Invoice register journal.</span></span> <span data-ttu-id="e1251-166">Uživatel například zadá zcela základní informace o fakturách dodavatele, když byly přijaty do registru faktur.</span><span class="sxs-lookup"><span data-stu-id="e1251-166">For example, a user enters very basic information about vendor invoices when they are received in the invoice register.</span></span> <span data-ttu-id="e1251-167">Když je registr faktur zaúčtován, transakce jsou zaúčtovány na účet, který je zadán zde, a do pole <strong>Protiúčet</strong>.</span><span class="sxs-lookup"><span data-stu-id="e1251-167">When the invoice register is posted, the transactions are posted to the account that is entered here and in the <strong>Offset account</strong> field.</span></span> <span data-ttu-id="e1251-168">Když jsou faktury schváleny, dluh je přenesen z účtu doručení do souhrnného účtu dodavatele.</span><span class="sxs-lookup"><span data-stu-id="e1251-168">When the invoices are approved, the debt is transferred from the arrival account to the vendor summary account.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e1251-169"><strong>Protiúčet</strong></span><span class="sxs-lookup"><span data-stu-id="e1251-169"><strong>Offset account</strong></span></span></td>
<td><span data-ttu-id="e1251-170">Vyberte účet hlavní knihy, který je používán pro vyrovnání neschválených faktur dodavatele, které jsou aktualizovány pomocí registru faktur.</span><span class="sxs-lookup"><span data-stu-id="e1251-170">Select the ledger account that is used for offsetting unapproved vendor invoices that are updated by using the invoice register.</span></span> <span data-ttu-id="e1251-171">Protiúčet plní funkci protiúčtu pro transakce, které jsou zaúčtovány na účty doručení.</span><span class="sxs-lookup"><span data-stu-id="e1251-171">The offset account acts as the offset account for transactions that are posted to arrival accounts.</span></span> <span data-ttu-id="e1251-172">Proto bude účet obsahovat nákupy dodavatele, které dosud nebyly schváleny.</span><span class="sxs-lookup"><span data-stu-id="e1251-172">Therefore, the account contains vendor purchases that have not yet been approved.</span></span></td>
</tr>
</tbody>
</table>


### <a name="table-restrictions"></a><span data-ttu-id="e1251-173">**Tabulka omezení**</span><span class="sxs-lookup"><span data-stu-id="e1251-173">**Table restrictions**</span></span>

<span data-ttu-id="e1251-174">Pro transakce s vybraným účetním profilem určete, zda transakce budou vyrovnány automaticky, zda bude vypočten úrok a zda budou vydány upomínky.</span><span class="sxs-lookup"><span data-stu-id="e1251-174">For transactions that have the selected posting profile, specify whether transactions will be settled automatically, interest will be calculated, and collection letters will be issued.</span></span> <span data-ttu-id="e1251-175">Můžete také vybrat účet, který se použije při uzavření transakcí s vybraným účetním profilem.</span><span class="sxs-lookup"><span data-stu-id="e1251-175">You can also select the account that is used when transactions that have the selected posting profile are closed.</span></span>

<span data-ttu-id="e1251-176">Zadání následujících hodnot pro nastavení účetního profilu</span><span class="sxs-lookup"><span data-stu-id="e1251-176">Specify the following values to set up your posting profile</span></span>

| <span data-ttu-id="e1251-177">Pole</span><span class="sxs-lookup"><span data-stu-id="e1251-177">Field</span></span>          | <span data-ttu-id="e1251-178">Popis</span><span class="sxs-lookup"><span data-stu-id="e1251-178">Description</span></span>                                                                                                                                                                                                    |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1251-179">**Vyrovnání**</span><span class="sxs-lookup"><span data-stu-id="e1251-179">**Settlement**</span></span> | <span data-ttu-id="e1251-180">Tuto možnost vyberte, chcete-li povolit automatické vyrovnání transakcí, které mají tento účetní profil.</span><span class="sxs-lookup"><span data-stu-id="e1251-180">Select this option to enable automatic settlement of transactions that have this posting profile.</span></span> <span data-ttu-id="e1251-181">Není-li toto políčko zaškrtnuto, je nutné vyrovnat transakce ručně s použitím stránky **Vyrovnat otevřené transakce**.</span><span class="sxs-lookup"><span data-stu-id="e1251-181">If this option is cleared, you must manually settle transactions by using the **Settle open transactions** page.</span></span> |
| <span data-ttu-id="e1251-182">Tlačítko **Zrušit**</span><span class="sxs-lookup"><span data-stu-id="e1251-182">**Cancel**</span></span>     | <span data-ttu-id="e1251-183">Tuto možnost vyberte, chcete-li mít možnost zrušit transakce, které mají tento účetní profil.</span><span class="sxs-lookup"><span data-stu-id="e1251-183">Select this option if you want to be able to cancel transactions that have this posting profile.</span></span>                                                                                                               |
| <span data-ttu-id="e1251-184">**Zavřít**</span><span class="sxs-lookup"><span data-stu-id="e1251-184">**Close**</span></span>      | <span data-ttu-id="e1251-185">Vyberte jiný účetní profil, na který se chcete přepnout při uzavření transakcí s tímto účetním profilem.</span><span class="sxs-lookup"><span data-stu-id="e1251-185">Select a posting profile to change to when transactions that have this posting profile are closed.</span></span> <span data-ttu-id="e1251-186">Transakce je považována za uzavřenou, když byla plně vyrovnána.</span><span class="sxs-lookup"><span data-stu-id="e1251-186">A transaction is regarded as closed when it has been settled in full.</span></span>                                       |
