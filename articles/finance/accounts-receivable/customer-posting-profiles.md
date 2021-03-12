---
title: Účetní profily odběratele
description: Účetní profily odběratele řídí zaúčtování transakcí odběratelů do hlavní knihy
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPosting, CustVendExternalItem
audience: Application User
ms.reviewer: roschlom
ms.custom: 24651
ms.assetid: cb82245e-8c02-429c-b36e-8db0e3e6f7e5
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 71134331eae2c25f242915d63d8a4ef1dd33ed3f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4991085"
---
# <a name="customer-posting-profiles"></a><span data-ttu-id="ab3d5-103">Účetní profily odběratele</span><span class="sxs-lookup"><span data-stu-id="ab3d5-103">Customer posting profiles</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ab3d5-104">Účetní profily odběratele řídí zaúčtování transakcí odběratelů do hlavní knihy</span><span class="sxs-lookup"><span data-stu-id="ab3d5-104">Customer posting profiles control the posting of customer transactions to the general ledger.</span></span>

<a name="customer-posting-profiles"></a><span data-ttu-id="ab3d5-105">Účetní profily odběratele</span><span class="sxs-lookup"><span data-stu-id="ab3d5-105">Customer posting profiles</span></span>
-------------------------

<span data-ttu-id="ab3d5-106">Účetní profily odběratelů umožňují přiřazení účtů hlavní knihy a nastavení dokumentů ke všem odběratelům, skupině odběratelů nebo jednomu odběrateli.</span><span class="sxs-lookup"><span data-stu-id="ab3d5-106">Customer posting profiles enable you to assign general ledger accounts and document settings to all customers, a group of customers or a single customer.</span></span> <span data-ttu-id="ab3d5-107">Toto nastavení se použije při vytváření prodejních objednávek, volných faktur, hotovostních plateb, upomínek a oznámení úroků.</span><span class="sxs-lookup"><span data-stu-id="ab3d5-107">These settings will be used when you create sales orders, free text invoices, cash payments, collection letters, and interest notes.</span></span> <span data-ttu-id="ab3d5-108">U některých transakcí je možné vybrat účetní profil, který se odlišuje od účetních profilů nastavených pro transakce na této stránce a má před nimi přednost.</span><span class="sxs-lookup"><span data-stu-id="ab3d5-108">For some transactions, you can select a posting profile that differs from and takes precedence over the posting profiles that are set up for transactions in this page.</span></span> 

<span data-ttu-id="ab3d5-109">Výchozí účetní profil je definován v pevné záložce Hlavní kniha a DPH na straně Parametry pohledávek.</span><span class="sxs-lookup"><span data-stu-id="ab3d5-109">The default posting profile is defined in the Ledger and Sales Tax fasttab on the Accounts receivable parameters page.</span></span> <span data-ttu-id="ab3d5-110">Výchozí účetní profil je poté následně automaticky zahrnut do záhlaví nových dokumentů, kde jej můžete změnit na jiný účetní profil v případě potřeby.</span><span class="sxs-lookup"><span data-stu-id="ab3d5-110">The default posting profile is then included automatically on the header of new documents where you can change it to a different posting profile if needed.</span></span>

<span data-ttu-id="ab3d5-111">Můžete také přiřadit definice účtování k typům účtování transakcí na stránce Definice účtování transakce.</span><span class="sxs-lookup"><span data-stu-id="ab3d5-111">You can also associate posting definitions with transaction posting types in the Transaction posting definitions page.</span></span> <span data-ttu-id="ab3d5-112">Definice účtování řídí účtování transakcí odběratelů do hlavní knihy místo účetních profilů.</span><span class="sxs-lookup"><span data-stu-id="ab3d5-112">Posting definitions control the posting of customer transactions to the general ledger instead of posting profiles.</span></span>

## <a name="creating-a-posting-profile"></a><span data-ttu-id="ab3d5-113">Vytvoření účetního profilu</span><span class="sxs-lookup"><span data-stu-id="ab3d5-113">Creating a posting profile</span></span>
<span data-ttu-id="ab3d5-114">Určete účty hlavní knihy, které jsou použity při zaúčtování transakcí s vybraným účetním profilem.</span><span class="sxs-lookup"><span data-stu-id="ab3d5-114">Specify the ledger accounts that are used in the posting of transactions that use the selected posting profile.</span></span> <span data-ttu-id="ab3d5-115">Vyberte kód účtu a je-li to možné, i číslo účtu nebo skupiny vybraného účetního profilu.</span><span class="sxs-lookup"><span data-stu-id="ab3d5-115">Select an account code and, whenever possible, an account or group number for the selected posting profile.</span></span> <span data-ttu-id="ab3d5-116">V procesu zaúčtování bude nejvhodnější účetní profil pro každou transakci nalezen vyhledáním nejspecifičtější kombinace kódu účtu, čísla účtu nebo kombinace skupiny a čísla s následující prioritou:</span><span class="sxs-lookup"><span data-stu-id="ab3d5-116">In the posting process, the most appropriate posting profile for each transaction is located by searching for the most specific account code, account number, or group and number combination in the following priority:</span></span>

| <span data-ttu-id="ab3d5-117">Hodnota pole **Kód účtu**</span><span class="sxs-lookup"><span data-stu-id="ab3d5-117">**Account code** field value</span></span> | <span data-ttu-id="ab3d5-118">Hodnota pole **Číslo účtu/skupiny**</span><span class="sxs-lookup"><span data-stu-id="ab3d5-118">**Account/Group number** field value</span></span>            | <span data-ttu-id="ab3d5-119">Priorita hledání</span><span class="sxs-lookup"><span data-stu-id="ab3d5-119">Search priority</span></span> |
|------------------------------|-------------------------------------------------|-----------------|
| <span data-ttu-id="ab3d5-120">**Tabulka**</span><span class="sxs-lookup"><span data-stu-id="ab3d5-120">**Table**</span></span>                    | <span data-ttu-id="ab3d5-121">Specifický účet odběratele</span><span class="sxs-lookup"><span data-stu-id="ab3d5-121">Specific customer account</span></span>                       | <span data-ttu-id="ab3d5-122">1</span><span class="sxs-lookup"><span data-stu-id="ab3d5-122">1</span></span>               |
| <span data-ttu-id="ab3d5-123">**Skupina**</span><span class="sxs-lookup"><span data-stu-id="ab3d5-123">**Group**</span></span>                    | <span data-ttu-id="ab3d5-124">Skupina odběratelů, která je přiřazena odběrateli</span><span class="sxs-lookup"><span data-stu-id="ab3d5-124">Customer group that is assigned to the customer</span></span> | <span data-ttu-id="ab3d5-125">2</span><span class="sxs-lookup"><span data-stu-id="ab3d5-125">2</span></span>               |
| <span data-ttu-id="ab3d5-126">**Vše**</span><span class="sxs-lookup"><span data-stu-id="ab3d5-126">**All**</span></span>                      | <span data-ttu-id="ab3d5-127">Prázdné</span><span class="sxs-lookup"><span data-stu-id="ab3d5-127">Blank</span></span>                                           | <span data-ttu-id="ab3d5-128">3</span><span class="sxs-lookup"><span data-stu-id="ab3d5-128">3</span></span>               |

<span data-ttu-id="ab3d5-129">Pokud chcete, aby všechny transakce odběratele měly shodný účetní profil, nastavte pouze jeden účetní profil s hodnotou Vše v poli Kód účtu.</span><span class="sxs-lookup"><span data-stu-id="ab3d5-129">If you want all customer transactions to have the same posting profile, set up only one posting profile with All in the Account code field.</span></span> <span data-ttu-id="ab3d5-130">Zadejte následující hodnoty pro nastavení účetního profilu:</span><span class="sxs-lookup"><span data-stu-id="ab3d5-130">Specify the following values to set up your posting profile:</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="ab3d5-131">Pole</span><span class="sxs-lookup"><span data-stu-id="ab3d5-131">Field</span></span></th>
<th><span data-ttu-id="ab3d5-132">Popis</span><span class="sxs-lookup"><span data-stu-id="ab3d5-132">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ab3d5-133"><strong>Účetní profil</strong></span><span class="sxs-lookup"><span data-stu-id="ab3d5-133"><strong>Posting profile</strong></span></span></td>
<td><span data-ttu-id="ab3d5-134">Zadejte kód účetního profilu.</span><span class="sxs-lookup"><span data-stu-id="ab3d5-134">Enter a code for the posting profile.</span></span> <span data-ttu-id="ab3d5-135">Můžete například vytvořit dva účetní profily a získat jeden účet pro rozvahy odběratele v národní měně a jiný účet pro rozvahy v měně cizí.</span><span class="sxs-lookup"><span data-stu-id="ab3d5-135">For example, you could create two posting profiles to obtain one account for customer balances in the national currency and another for customer balances in a foreign currency.</span></span> <span data-ttu-id="ab3d5-136">Jeden účet byste měli nazvat "národní" a druhý "cizí".</span><span class="sxs-lookup"><span data-stu-id="ab3d5-136">You could call one account National and the other Foreign.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ab3d5-137"><strong>Popis</strong></span><span class="sxs-lookup"><span data-stu-id="ab3d5-137"><strong>Description</strong></span></span></td>
<td><span data-ttu-id="ab3d5-138">Zadejte popis účetního profilu.</span><span class="sxs-lookup"><span data-stu-id="ab3d5-138">Enter a description of the posting profile.</span></span> <span data-ttu-id="ab3d5-139">Používá se jen k lepší identifikace účetního profilu při jeho zobrazení na této stránce.</span><span class="sxs-lookup"><span data-stu-id="ab3d5-139">This is only used to better identify the posting profile when you view it in this page.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ab3d5-140"><strong>Kód účtu</strong></span><span class="sxs-lookup"><span data-stu-id="ab3d5-140"><strong>Account code</strong></span></span></td>
<td><span data-ttu-id="ab3d5-141">Uveďte, zda účetní profil platí pro jednotlivého odběratele, skupinu odběratelů nebo všechny odběratele:</span><span class="sxs-lookup"><span data-stu-id="ab3d5-141">Specify whether the posting profile applies to a single customer, a group of customers, or all customers:</span></span>
<ul>
<li><span data-ttu-id="ab3d5-142"><strong>Tabulka</strong> – Účetní profil platí pro jednoho odběratele.</span><span class="sxs-lookup"><span data-stu-id="ab3d5-142"><strong>Table</strong> – The posting profile applies to a single customer.</span></span> <span data-ttu-id="ab3d5-143">Vyberte účet odběratele v poli Číslo účtu/skupiny.</span><span class="sxs-lookup"><span data-stu-id="ab3d5-143">Select the customer account in the Account/Group number field.</span></span></li>
<li><span data-ttu-id="ab3d5-144"><strong>Skupina</strong> – Účetní profil platí pro skupinu odběratelů.</span><span class="sxs-lookup"><span data-stu-id="ab3d5-144"><strong>Group</strong> – The posting profile applies to a customer group.</span></span> <span data-ttu-id="ab3d5-145">Vyberte skupinu odběratelů v poli Číslo účtu/skupiny.</span><span class="sxs-lookup"><span data-stu-id="ab3d5-145">Select the customer group in the Account/Group number field.</span></span></li>
<li><span data-ttu-id="ab3d5-146"><strong>Vše</strong> – Účetní profil platí pro všechny odběratele.</span><span class="sxs-lookup"><span data-stu-id="ab3d5-146"><strong>All</strong> – The posting profile applies to all customers.</span></span> <span data-ttu-id="ab3d5-147">Pole Číslo účtu/skupiny ponechejte prázdné.</span><span class="sxs-lookup"><span data-stu-id="ab3d5-147">Leave the Account/Group number field blank.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ab3d5-148"><strong>Číslo účtu/skupiny</strong></span><span class="sxs-lookup"><span data-stu-id="ab3d5-148"><strong>Account/Group number</strong></span></span></td>
<td><span data-ttu-id="ab3d5-149">Pokud vyberete možnost Tabulka v poli Kód účtu, zvolte číslo účtu odběratele přiřazeného k účetnímu profilu.</span><span class="sxs-lookup"><span data-stu-id="ab3d5-149">If Table is selected in the Account code field, select the account number of the customer who is associated with the posting profile.</span></span> <span data-ttu-id="ab3d5-150">Pokud je vybrána možnost Skupina, vyberte skupinu odběratelů.</span><span class="sxs-lookup"><span data-stu-id="ab3d5-150">If Group is selected, select the customer group.</span></span> <span data-ttu-id="ab3d5-151">Pokud je vybrána možnost Vše, ponechte toto pole prázdné.</span><span class="sxs-lookup"><span data-stu-id="ab3d5-151">If All is selected, leave this field blank.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ab3d5-152"><strong>Součtový účet</strong></span><span class="sxs-lookup"><span data-stu-id="ab3d5-152"><strong>Summary account</strong></span></span></td>
<td><span data-ttu-id="ab3d5-153">Vyberte účet hlavní knihy, který se má použít jako součtový účet odběratele přiřazených k danému účetnímu profilu.</span><span class="sxs-lookup"><span data-stu-id="ab3d5-153">Select the ledger account that will be used as the customer summary account for the customers who are associated with the posting profile.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ab3d5-154"><strong>Účet vyrovnání</strong></span><span class="sxs-lookup"><span data-stu-id="ab3d5-154"><strong>Settle account</strong></span></span></td>
<td><span data-ttu-id="ab3d5-155">Vyberte účet hlavní knihy likvidity použitý pro prognózy cash-flow.</span><span class="sxs-lookup"><span data-stu-id="ab3d5-155">Select the liquidity ledger account that is used for cash flow forecasts.</span></span> <span data-ttu-id="ab3d5-156">Toto pole se zobrazí pouze v případě, že jsou prognózy cashflow povoleny.</span><span class="sxs-lookup"><span data-stu-id="ab3d5-156">This field will only appear if cash flow forecasts are enabled.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ab3d5-157"><strong>Zálohy DPH</strong></span><span class="sxs-lookup"><span data-stu-id="ab3d5-157"><strong>Sales tax prepayments</strong></span></span></td>
<td><span data-ttu-id="ab3d5-158">Vyberte účet pro zálohové platby daně z prodeje.</span><span class="sxs-lookup"><span data-stu-id="ab3d5-158">Select the account for sales tax for payments that are received in advance.</span></span>
<div class="alert">
<table>
<thead>
<tr class="header">
<th><img src="https://i-technet.sec.s-msft.com/areas/global/content/clear.gif" title="Poznámka" alt="Note" id="alert_note" class="cl_IC101471" /><span data-ttu-id="ab3d5-160"><strong>Poznámka</strong></span><span class="sxs-lookup"><span data-stu-id="ab3d5-160"><strong>Note</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ab3d5-161">Na stránce Parametry pohledávek určete účetní profil, který má být použit při označení platby jako zálohy.</span><span class="sxs-lookup"><span data-stu-id="ab3d5-161">Use the Accounts receivable parameters page to specify the posting profile to use when a payment is marked as a prepayment.</span></span></td>
</tr>
</tbody>
</table>
</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ab3d5-162"><strong>Závazky pro účet slevy</strong></span><span class="sxs-lookup"><span data-stu-id="ab3d5-162"><strong>Liabilities for discount account</strong></span></span></td>
<td><span data-ttu-id="ab3d5-163">Vyberte účet hlavní knihy pro závazky slevy.</span><span class="sxs-lookup"><span data-stu-id="ab3d5-163">Select the ledger account for liabilities of discount.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ab3d5-164"><strong>Posloupnost upomínek</strong></span><span class="sxs-lookup"><span data-stu-id="ab3d5-164"><strong>Collection letter sequence</strong></span></span></td>
<td><span data-ttu-id="ab3d5-165">Vyberte identifikátor posloupnosti upomínek, který má být použit pro odběratele, kterým je přiřazen účetní profil.</span><span class="sxs-lookup"><span data-stu-id="ab3d5-165">Select the identifier of the collection letter sequence to use for customers to whom the posting profile is assigned.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ab3d5-166"><strong>Kód úroku</strong></span><span class="sxs-lookup"><span data-stu-id="ab3d5-166"><strong>Interest code</strong></span></span></td>
<td><span data-ttu-id="ab3d5-167">Vyberte kód úroku, který má být použit pro výpočet úroku pro odběratele, kterým je přiřazen účetní profil.</span><span class="sxs-lookup"><span data-stu-id="ab3d5-167">Select the interest code to use for the calculation of interest for customers to whom the posting profile is assigned.</span></span></td>
</tr>
</tbody>
</table>

### 

### <a name="table-restrictions"></a><span data-ttu-id="ab3d5-168">**Tabulka omezení**</span><span class="sxs-lookup"><span data-stu-id="ab3d5-168">**Table restrictions**</span></span>

<span data-ttu-id="ab3d5-169">Pro transakce s vybraným účetním profilem určete, zda transakce budou vyrovnány automaticky, zda bude vypočten úrok a zda budou vydány upomínky.</span><span class="sxs-lookup"><span data-stu-id="ab3d5-169">For transactions that have the selected posting profile, specify whether transactions will be settled automatically, interest will be calculated, and collection letters will be issued.</span></span> <span data-ttu-id="ab3d5-170">Můžete také vybrat účet, který se použije při uzavření transakcí s vybraným účetním profilem.</span><span class="sxs-lookup"><span data-stu-id="ab3d5-170">You can also select the account that is used when transactions that have the selected posting profile are closed.</span></span>

<span data-ttu-id="ab3d5-171">Zadejte následující hodnoty pro nastavení účetního profilu:</span><span class="sxs-lookup"><span data-stu-id="ab3d5-171">Specify the following values to set up your posting profile:</span></span>

| <span data-ttu-id="ab3d5-172">Pole</span><span class="sxs-lookup"><span data-stu-id="ab3d5-172">Field</span></span>                 | <span data-ttu-id="ab3d5-173">Popis</span><span class="sxs-lookup"><span data-stu-id="ab3d5-173">Description</span></span>                                                                                                                                                                                                                                        |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab3d5-174">**Vyrovnání**</span><span class="sxs-lookup"><span data-stu-id="ab3d5-174">**Settlement**</span></span>        | <span data-ttu-id="ab3d5-175">Tento přepínač vyberte, chcete-li povolit automatické vyrovnání transakcí, které mají tento účetní profil.</span><span class="sxs-lookup"><span data-stu-id="ab3d5-175">Select this toggle to enable automatic settlement of transactions that have this posting profile.</span></span> <span data-ttu-id="ab3d5-176">Není-li tento přepínač zaškrtnutý, je nutné vyrovnat transakce ručně s použitím stránky Vyrovnat otevřené transakce nebo Zadat platby odběratele.</span><span class="sxs-lookup"><span data-stu-id="ab3d5-176">If this toggle is cleared, you must manually settle transactions by using the Settle open transactions page or the Enter customer payments page.</span></span> |
| <span data-ttu-id="ab3d5-177">**Zájmy**</span><span class="sxs-lookup"><span data-stu-id="ab3d5-177">**Interest**</span></span>          | <span data-ttu-id="ab3d5-178">Tento přepínač vyberte, pokud by měl být úrok vypočítán z neuhrazených zůstatků pro účty odběratele s tímto profilem.</span><span class="sxs-lookup"><span data-stu-id="ab3d5-178">Select this toggle if interest should be calculated on outstanding balances for customer accounts that use this profile.</span></span> <span data-ttu-id="ab3d5-179">Pokud není tento přepínač zaškrtnut, úrok se u těchto odběratelů nevypočítá.</span><span class="sxs-lookup"><span data-stu-id="ab3d5-179">If this toggle is cleared, interest will not be calculated for these customers.</span></span>                                           |
| <span data-ttu-id="ab3d5-180">**Upomínka**</span><span class="sxs-lookup"><span data-stu-id="ab3d5-180">**Collection letter**</span></span> | <span data-ttu-id="ab3d5-181">Tento přepínač vyberte, pokud by měly být upomínky generovány pro účty odběratele s tímto profilem.</span><span class="sxs-lookup"><span data-stu-id="ab3d5-181">Select this toggle if collection letters should be generated for customer accounts that use this profile.</span></span> <span data-ttu-id="ab3d5-182">Pokud není tento přepínač zaškrtnut, upomínky nebudou u těchto odběratelů generovány.</span><span class="sxs-lookup"><span data-stu-id="ab3d5-182">If this toggle is cleared, collection letters will not be generated for these customers.</span></span>                                                 |
| <span data-ttu-id="ab3d5-183">**Zavřít**</span><span class="sxs-lookup"><span data-stu-id="ab3d5-183">**Close**</span></span>             | <span data-ttu-id="ab3d5-184">Vyberte jiný účetní profil, na který se chcete přepnout při uzavření transakcí s tímto účetním profilem.</span><span class="sxs-lookup"><span data-stu-id="ab3d5-184">Select a posting profile to change to when transactions that have this posting profile are closed.</span></span> <span data-ttu-id="ab3d5-185">Transakce je považována za uzavřenou, když byla plně vyrovnána.</span><span class="sxs-lookup"><span data-stu-id="ab3d5-185">A transaction is regarded as closed when it has been settled in full.</span></span>                                                                           |



<span data-ttu-id="ab3d5-186">Další informace naleznete v tématu [Přehled plateb odběratele](../cash-bank-management/tasks/customer-payment-overview.md).</span><span class="sxs-lookup"><span data-stu-id="ab3d5-186">For more information, see [Customer payment overview](../cash-bank-management/tasks/customer-payment-overview.md).</span></span>

