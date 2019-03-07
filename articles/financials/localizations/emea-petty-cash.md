---
title: Pokladní hotovost pro východní Evropu
description: Toto téma uvádí informace o funkci pokladní hotovosti, která umožňuje uživatelům v Estonsku, Litvě, České republice, Maďarsku, Lotyšku, Polsku a Rusku provádět hotovostní operace v systému.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RCashBalance, RCashCountStatementForm, RCashPosting, RCashRemainLimit, RCashReportJour_PL, RCashTable, RCashTableBalance, RCashTableCredLimit, RCashTableLastRevaluation, RCashTableTransactions, RCashTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 268504
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.author: v-elgolu
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 77159c0ef8e8046b50fa1dae60423823865e80b5
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "370128"
---
# <a name="petty-cash-for-eastern-europe"></a><span data-ttu-id="b5fb4-103">Pokladní hotovost pro východní Evropu</span><span class="sxs-lookup"><span data-stu-id="b5fb4-103">Petty cash for Eastern Europe</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b5fb4-104">Toto téma uvádí informace o funkci pokladní hotovosti, která umožňuje uživatelům v Estonsku, Litvě, České republice, Maďarsku, Lotyšku, Polsku a Rusku provádět hotovostní operace v systému.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-104">This topic provides information about the petty cash functionality that lets users in Estonia, Lithuania, Czech Republic, Hungary, Latvia, Poland, and Russia reflect cash operations in the system.</span></span>

<span data-ttu-id="b5fb4-105">Funkci pokladní hotovosti můžete používat k automatizaci provozů pro příjmy a výdaje v hotovosti, vytváření primárních dokumentů a tisku souvisejících sestav.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-105">You can use the petty cash functionality to automate operations for receipts and expenditures of cash, the creation of primary documents, and the printing of related reports.</span></span> <span data-ttu-id="b5fb4-106">Funkce pokladní hotovosti umožňuje provádět následující operace:</span><span class="sxs-lookup"><span data-stu-id="b5fb4-106">The petty cash functionality lets you perform the following operations:</span></span>

-   <span data-ttu-id="b5fb4-107">Účtovat příjmy a výdaje dostupných finančních aktiv.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-107">Account the receipt and expenditure of available cash assets.</span></span>
-   <span data-ttu-id="b5fb4-108">Vytvářet a ukládat běžné hotovostní formuláře: hotovostní refundační doklady, hotovostní výdajové doklady a deník registrace pokladních dokladů.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-108">Generate typical cash forms: Cash reimbursement slips, Cash disbursement slips, and a Journal of registration for cash slips.</span></span>
-   <span data-ttu-id="b5fb4-109">Určovat maximální peněžní částky, která je povolena pro operace se zákazníky, dodavateli atd.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-109">Control the maximum cash amount that is allowed for operations with customers, vendors, and so on.</span></span>
-   <span data-ttu-id="b5fb4-110">Vyjadřovat hotovostní operace v různých měnách v systému.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-110">Reflect cash operations in various currencies in the system.</span></span>
-   <span data-ttu-id="b5fb4-111">Převádět částky pokladních operací v cizích měnách na zúčtovací měnu, a zajistit tak účetní vykazování.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-111">Convert the amounts of cash operations in foreign currency to the default currency to provide accounting reporting.</span></span>
-   <span data-ttu-id="b5fb4-112">Generovat sestavu **pokladní hotovosti** a sestavu pokladníka.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-112">Generate a **Cash book** report and a cashier’s report.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="b5fb4-113">Předpoklady</span><span class="sxs-lookup"><span data-stu-id="b5fb4-113">Prerequisites</span></span>
<span data-ttu-id="b5fb4-114">Před použitím funkce pokladní hotovosti je nutné provést následující požadované úkoly:</span><span class="sxs-lookup"><span data-stu-id="b5fb4-114">Before you can use the petty cash functionality, you must complete the following prerequisites:</span></span>

-   <span data-ttu-id="b5fb4-115">Nastavit účty hotovostní zálohy.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-115">Set up cash accounts.</span></span>
-   <span data-ttu-id="b5fb4-116">Nastavit účetní profily pro hotovost.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-116">Set up cash posting profiles.</span></span>
-   <span data-ttu-id="b5fb4-117">Nastavit číselné řady pro číslování hotovostních dokladů.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-117">Set up number sequences for cash document numbering.</span></span>
-   <span data-ttu-id="b5fb4-118">Nastavit výchozí hodnoty a parametry pro parametry pokladny a banky.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-118">Set up default values for Cash and bank management parameters.</span></span>
-   <span data-ttu-id="b5fb4-119">Nastavit názvy hotovostních deníků v hlavní knize.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-119">Set up cash journal names in General ledger.</span></span>

### <a name="set-up-cash-accounts"></a><span data-ttu-id="b5fb4-120">Nastavit účty hotovostní zálohy.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-120">Set up cash accounts</span></span>

<span data-ttu-id="b5fb4-121">Pokud chcete nastavit hotovost, otevřete složku **Pokladna a banka** &gt; **Bankovní účty** &gt; **Pokladní účty** a zadejte následující informace.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-121">To set up a Cash, open **Cash and bank management** &gt; **Bank accounts** &gt; **Cash accounts**, and enter the following information.</span></span>

| <span data-ttu-id="b5fb4-122">Pole</span><span class="sxs-lookup"><span data-stu-id="b5fb4-122">Field</span></span>                 | <span data-ttu-id="b5fb4-123">popis</span><span class="sxs-lookup"><span data-stu-id="b5fb4-123">Description</span></span>                                                                                                          |
|-----------------------|----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5fb4-124">Hotovost</span><span class="sxs-lookup"><span data-stu-id="b5fb4-124">Cash</span></span>                  | <span data-ttu-id="b5fb4-125">Zadejte kód pro označení pokladního účtu (hotovost).</span><span class="sxs-lookup"><span data-stu-id="b5fb4-125">Enter a code to identify the cash account (cash).</span></span>                                                                    |
| <span data-ttu-id="b5fb4-126">Jméno</span><span class="sxs-lookup"><span data-stu-id="b5fb4-126">Name</span></span>                  | <span data-ttu-id="b5fb4-127">Zadejte popis pokladního účtu.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-127">Enter a description of the cash account.</span></span>                                                                             |
| <span data-ttu-id="b5fb4-128">Měna</span><span class="sxs-lookup"><span data-stu-id="b5fb4-128">Currency</span></span>              | <span data-ttu-id="b5fb4-129">Vyberte výchozí kód měny pro hotovostní transakce.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-129">Select the default currency code for cash transactions.</span></span>                                                              |
| <span data-ttu-id="b5fb4-130">Skupina číselné řady</span><span class="sxs-lookup"><span data-stu-id="b5fb4-130">Number sequence group</span></span> | <span data-ttu-id="b5fb4-131">Pokud se musí číslování pokladních dokladů lišit od číslování, které je určeno v parametrech, zadejte kód.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-131">If the numbering of cash documents must differ from the numbering that is specified in the parameters, enter a code.</span></span> |
| <span data-ttu-id="b5fb4-132">Více měn</span><span class="sxs-lookup"><span data-stu-id="b5fb4-132">More currencies</span></span>       | <span data-ttu-id="b5fb4-133">Zaškrtněte toto políčko k povolení měn, které se liší od zúčtovací měny k zaúčtování.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-133">Select this check box to allow currencies that differ from the accounting currency to be posted.</span></span>                     |
| <span data-ttu-id="b5fb4-134">Záporná hotovost</span><span class="sxs-lookup"><span data-stu-id="b5fb4-134">Negative cash</span></span>         | <span data-ttu-id="b5fb4-135">Zaškrtněte toto políčko, pokud chcete povolit záporné peněžní zůstatky v jakékoliv měně.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-135">Select this check box to allow negative cash balances in any currency.</span></span>                                               |

<span data-ttu-id="b5fb4-136">Pokud chcete nastavit pravidla pro kontrolu zůstatku na pokladním účtu, vyberte pokladní účet a poté v podokně akcí na kartě **Pokladní účet** klepněte ve skupině **Limit zůstatku** na **Limit zůstatku**.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-136">To set up cash balance control rules for a cash account, select the cash account, and then, on the Action Pane, on the **Cash account** tab, in the **Balance limit** group, click **Balance limit**.</span></span> <span data-ttu-id="b5fb4-137">Zadejte následující informace.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-137">Enter the following information.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b5fb4-138">Pole</span><span class="sxs-lookup"><span data-stu-id="b5fb4-138">Field</span></span></th>
<th><span data-ttu-id="b5fb4-139">popis</span><span class="sxs-lookup"><span data-stu-id="b5fb4-139">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b5fb4-140">Typ měny</span><span class="sxs-lookup"><span data-stu-id="b5fb4-140">Currency type</span></span></td>
<td><span data-ttu-id="b5fb4-141">Vyberte typ měny:</span><span class="sxs-lookup"><span data-stu-id="b5fb4-141">Select the type of currency:</span></span>
<ul>
<li><span data-ttu-id="b5fb4-142"><strong>Zúčtovací měna</strong> – použijte základní firemní kód měny.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-142"><strong>Accounting currency</strong> – Use the basic company currency code.</span></span></li>
<li><span data-ttu-id="b5fb4-143"><strong>Označená měna</strong> – použijte kód měny, který se liší od základního firemního kódu měny.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-143"><strong>Indicated currency</strong> – Use a currency code that differs from the basic company currency code.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b5fb4-144">Měna</span><span class="sxs-lookup"><span data-stu-id="b5fb4-144">Currency</span></span></td>
<td><span data-ttu-id="b5fb4-145">Pokud jste vybrali <strong>Označená měna</strong> v poli <strong>Typ měny</strong>, vyberte kód měny.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-145">If you selected <strong>Indicated currency</strong> in the <strong>Currency type</strong> field, select a currency code.</span></span> <span data-ttu-id="b5fb4-146">Toto pole není k dispozici, pokud jste vybrali <strong>Zúčtovací měna</strong> v poli <strong>Typ měny</strong>.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-146">This field is unavailable if you selected <strong>Accounting currency</strong> in the <strong>Currency type</strong> field.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b5fb4-147">Typ limitu zůstatku</span><span class="sxs-lookup"><span data-stu-id="b5fb4-147">Balance limit type</span></span></td>
<td><span data-ttu-id="b5fb4-148">Vyberte jednu z dostupných hodnot:</span><span class="sxs-lookup"><span data-stu-id="b5fb4-148">Select one of the available values:</span></span>
<ul>
<li><span data-ttu-id="b5fb4-149"><strong>Maximální</strong> – Nemělo by být povoleno, aby zůstatek v hotovosti překročil částku <strong>limitu zůstatku</strong> pro pokladní účet (horní mez).</span><span class="sxs-lookup"><span data-stu-id="b5fb4-149"><strong>Maximum</strong> – The cash balance should not be allowed to exceed the <strong>Balance limit</strong> amount for the cash account (upper bound).</span></span></li>
<li><span data-ttu-id="b5fb4-150"><strong>Minimální</strong> – Nemělo by být povoleno, aby zůstatek v hotovosti klesl pod částku <strong>limitu zůstatku</strong> pro pokladní účet (dolní mez).</span><span class="sxs-lookup"><span data-stu-id="b5fb4-150"><strong>Minimum</strong> – The cash balance should not be allowed to go below the <strong>Balance limit</strong> amount for the cash account (bottom bound).</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b5fb4-151">Zkontrolovat limit salda</span><span class="sxs-lookup"><span data-stu-id="b5fb4-151">Check balance limit</span></span></td>
<td><span data-ttu-id="b5fb4-152">Vyberte, co se má dít během procesu schvalování pokladních dokladů, jestliže je překročena částka pro <strong>Limit zůstatku</strong> pro pokladní účet:</span><span class="sxs-lookup"><span data-stu-id="b5fb4-152">Select what occurs during the approval process for cash documents if the <strong>Balance limit</strong> amount for the cash account is exceeded:</span></span>
<ul>
<li><span data-ttu-id="b5fb4-153"><strong>Přijmout</strong> – Limit je možné překročit.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-153"><strong>Accept</strong> – The limit can be exceeded.</span></span></li>
<li><span data-ttu-id="b5fb4-154"><strong>Upozornění:</strong> – Limit může být překročen, ale uživatel obdrží zprávu s upozorněním.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-154"><strong>Warning</strong> – The limit can be exceeded, but the user receives a warning message.</span></span> <span data-ttu-id="b5fb4-155">Pokladní doklad je potvrzen nebo schválen.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-155">The cash document is confirmed or approved.</span></span></li>
<li><span data-ttu-id="b5fb4-156"><strong>Chyba</strong> – Limit není možné překročit.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-156"><strong>Error</strong> – The limit can&#39;t be exceeded.</span></span> <span data-ttu-id="b5fb4-157">Uživatel obdrží chybovou zprávu a pokladní doklad není potvrzen nebo schválen.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-157">The user receives an error message, and the cash document isn&#39;t confirmed or approved.</span></span></li>
</ul>
<span data-ttu-id="b5fb4-158">Další informace o procesu schvalování pokladních dokladů naleznete v části &quot;Schvalování platebních transakcí a zaúčtování&quot; dále v tomto tématu.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-158">For more information about the approval process for cash documents, see the &quot;Cash transaction approval and posting&quot; section, later in this topic.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b5fb4-159">Limit salda</span><span class="sxs-lookup"><span data-stu-id="b5fb4-159">Balance limit</span></span></td>
<td><span data-ttu-id="b5fb4-160">Zadejte limit zůstatku na pokladním účtu.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-160">Enter a limit for the cash account balance.</span></span> <span data-ttu-id="b5fb4-161">Částka by měla být v měně, kterou jste zadali.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-161">The amount should be in the currency that you specified.</span></span></td>
</tr>
</tbody>
</table>

### <a name="set-up-cash-posting-profiles"></a><span data-ttu-id="b5fb4-162">Nastavení účetních profilů pro hotovost</span><span class="sxs-lookup"><span data-stu-id="b5fb4-162">Set up cash posting profiles</span></span>

<span data-ttu-id="b5fb4-163">Účetní profily pro hotovost definují zaúčtování do hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-163">Cash posting profiles define postings to the general ledger.</span></span> <span data-ttu-id="b5fb4-164">Chcete-li nastavit účetní profil pro hotovost, přejděte na položky **Pokladna** **a banka** &gt; **Nastavení** &gt; **Účetní profily pro hotovost** a vyberte nebo vytvořte účetní profil.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-164">To set up a cash posting profile, go to **Cash** **and bank management** &gt; **Setup** &gt; **Cash posting profiles**, and select or create a posting profile.</span></span> <span data-ttu-id="b5fb4-165">Zadejte následující informace.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-165">Enter the following information.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b5fb4-166">Pole</span><span class="sxs-lookup"><span data-stu-id="b5fb4-166">Field</span></span></th>
<th><span data-ttu-id="b5fb4-167">popis</span><span class="sxs-lookup"><span data-stu-id="b5fb4-167">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b5fb4-168">Platné pro</span><span class="sxs-lookup"><span data-stu-id="b5fb4-168">Valid for</span></span></td>
<td><span data-ttu-id="b5fb4-169">Vyberte, zda se účetní profil týká konkrétního pokladního účtu všech pokladních účtů:</span><span class="sxs-lookup"><span data-stu-id="b5fb4-169">Select whether the posting profile applies to a specific cash account or all cash accounts:</span></span>
<ul>
<li><span data-ttu-id="b5fb4-170"><strong>Tabulka</strong> – Pokud je řádek účetního profilu pro pokladní účet, tento řádek slouží k zaúčtování hotovostní transakce.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-170"><strong>Table</strong> – If there is a posting profile line for the cash account, that line is used for cash transaction posting.</span></span></li>
<li><span data-ttu-id="b5fb4-171"><strong>Všechny</strong> – neexistuje žádný řádek účetního profilu pro pokladní účet.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-171"><strong>All</strong> – There is no posting profile line for the cash account.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b5fb4-172">Hotovost</span><span class="sxs-lookup"><span data-stu-id="b5fb4-172">Cash</span></span></td>
<td><span data-ttu-id="b5fb4-173">Pokud jste vybrali <strong>Tabulka</strong> v poli <strong>Platné pro</strong>, zadejte pokladní účet.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-173">If you selected <strong>Table</strong> in the <strong>Valid for</strong> field, specify the cash account.</span></span> <span data-ttu-id="b5fb4-174">Toto pole zůstane prázdné, pokud jste vybrali <strong>Vše</strong> v poli <strong>Platné pro</strong>.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-174">This field remains blank if you selected <strong>All</strong> in the <strong>Valid for</strong> field.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b5fb4-175">Účet hlavní knihy</span><span class="sxs-lookup"><span data-stu-id="b5fb4-175">Ledger account</span></span></td>
<td><span data-ttu-id="b5fb4-176">Zadejte číslo účtu hlavní knihy, který chcete použít jako souhrnný účet pro pokladní účet.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-176">Enter the number of the ledger account to use as the summary account for the cash account.</span></span></td>
</tr>
</tbody>
</table>

### <a name="set-up-number-sequences-for-cash-documents"></a><span data-ttu-id="b5fb4-177">Nastavení číselných řad pro pokladní doklady</span><span class="sxs-lookup"><span data-stu-id="b5fb4-177">Set up number sequences for cash documents</span></span>

<span data-ttu-id="b5fb4-178">Chcete-li nastavit číselné řady pro pokladní doklady, přejděte na **Pokladna a banka** &gt; **Nastavení** &gt; **Parametry pokladny a banky**.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-178">To set up number sequences for cash documents, go to **Cash and bank management** &gt; **Setup** &gt; **Cash and bank management parameters**.</span></span> <span data-ttu-id="b5fb4-179">Na kartě **Číselná řada** zadejte kódy číselných řad pro tyto doklady: **Hotovostní refundační doklady**, **Hotovostní výdajové doklady**, **Opravný hotovostní doklad**, **Vyrovnání kurzových rozdílů** a **Číslo výpisu hotovosti**.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-179">On the **Number sequence** tab, specify number sequence codes for the **Cash reimbursement slips**, **Cash disbursement slips**, **Cash correction voucher**, and **Exchange adjustment** documents, and for **Cash report number**.</span></span>

### <a name="set-up-default-values-for-cash-and-bank-management-parameters"></a><span data-ttu-id="b5fb4-180">Nastavení výchozích hodnot a parametrů pro parametry pokladny a banky</span><span class="sxs-lookup"><span data-stu-id="b5fb4-180">Set up default values for Cash and bank management parameters</span></span>

<span data-ttu-id="b5fb4-181">Chcete-li nastavit výchozí hodnoty pro parametry Pokladna a banka pro funkci pokladní hotovosti, přejděte na **Pokladna a banka** &gt; **Nastavení** &gt; **Parametry pokladny a banky**.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-181">To set up default values for Cash and bank management parameters for the petty cash functionality, go to **Cash and bank management** &gt; **Setup** &gt; **Cash and bank management parameters**.</span></span> <span data-ttu-id="b5fb4-182">Na kartě **Hotovost** zadejte následující informace:</span><span class="sxs-lookup"><span data-stu-id="b5fb4-182">On the **Cash** tab, enter the following information.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b5fb4-183">Pole</span><span class="sxs-lookup"><span data-stu-id="b5fb4-183">Field</span></span></th>
<th><span data-ttu-id="b5fb4-184">popis</span><span class="sxs-lookup"><span data-stu-id="b5fb4-184">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b5fb4-185">Hotovost</span><span class="sxs-lookup"><span data-stu-id="b5fb4-185">Cash</span></span></td>
<td><span data-ttu-id="b5fb4-186">Vyberte výchozí pokladní účet v denících.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-186">Select the default cash account in journals.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b5fb4-187">Účtování hotovosti</span><span class="sxs-lookup"><span data-stu-id="b5fb4-187">Cash posting</span></span></td>
<td><span data-ttu-id="b5fb4-188">Zadejte výchozí účetní profil pro hotovost, který se používá, pokud není zadán žádný jiný účetní profil.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-188">Enter the default cash posting profile that is used if no other posting profile is specified.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b5fb4-189">Kontrola použitých dokladů</span><span class="sxs-lookup"><span data-stu-id="b5fb4-189">Check for voucher used</span></span></td>
<td><span data-ttu-id="b5fb4-190">Vyberte, co se stane, pokud budou při kontrole čísla pokladního dokladu nalezena duplicitní čísla:</span><span class="sxs-lookup"><span data-stu-id="b5fb4-190">Select what occurs if duplicate numbers are found during the check of the cash document number:</span></span>
<ul>
<li><span data-ttu-id="b5fb4-191">Zamítnout duplikaci</span><span class="sxs-lookup"><span data-stu-id="b5fb4-191">Reject duplicate</span></span></li>
<li><span data-ttu-id="b5fb4-192">Zamítnout kopie v rámci fiskálního roku</span><span class="sxs-lookup"><span data-stu-id="b5fb4-192">Reject copies within fiscal year</span></span></li>
<li><span data-ttu-id="b5fb4-193">Akceptovat duplicity</span><span class="sxs-lookup"><span data-stu-id="b5fb4-193">Accept duplicates</span></span></li>
<li><span data-ttu-id="b5fb4-194">Upozornit v případě duplicit</span><span class="sxs-lookup"><span data-stu-id="b5fb4-194">Warn in case of duplicates</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b5fb4-195">Zkontrolovat limit operací</span><span class="sxs-lookup"><span data-stu-id="b5fb4-195">Check operations limit</span></span></td>
<td><span data-ttu-id="b5fb4-196">Určete, co se stane při překročení limitu pro operace s protistranami:</span><span class="sxs-lookup"><span data-stu-id="b5fb4-196">Specify what occurs if the limit for operations with counteragents is exceeded:</span></span>
<ul>
<li><span data-ttu-id="b5fb4-197"><strong>Přijmout</strong> – Limit je možné překročit.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-197"><strong>Accept</strong> – The limit can be exceeded.</span></span></li>
<li><span data-ttu-id="b5fb4-198"><strong>Upozornění:</strong> – Limit může být překročen, ale uživatel obdrží zprávu s upozorněním.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-198"><strong>Warning</strong> – The limit can be exceeded, but the user receives a warning message.</span></span> <span data-ttu-id="b5fb4-199">Operace je zaúčtována.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-199">The operation is posted.</span></span></li>
<li><span data-ttu-id="b5fb4-200"><strong>Chyba</strong> – Limit není možné překročit.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-200"><strong>Error</strong> – The limit can&#39;t be exceeded.</span></span> <span data-ttu-id="b5fb4-201">Uživatel obdrží chybovou zprávu a operace není zaúčtována.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-201">The user receives an error message, and the operation isn&#39;t posted.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b5fb4-202">Metoda ověření</span><span class="sxs-lookup"><span data-stu-id="b5fb4-202">Validation method</span></span></td>
<td><span data-ttu-id="b5fb4-203">Vyberte metodu ověření, která slouží ke kontrole množství překročení limitu pro operace:</span><span class="sxs-lookup"><span data-stu-id="b5fb4-203">Select the validation method that is used to control exceeded limit amounts for operations:</span></span>
<ul>
<li><span data-ttu-id="b5fb4-204"><strong>Operace</strong> – ověření se provádí na transakci</span><span class="sxs-lookup"><span data-stu-id="b5fb4-204"><strong>Operation</strong> – Validation is done per transaction</span></span></li>
<li><span data-ttu-id="b5fb4-205"><strong>Dohoda</strong> – ověření se provádí na transakci, která má specifikovanou dohodu s protistranou.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-205"><strong>Agreement</strong> – Validation is done per transaction that has a specified contract with a counteragent.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b5fb4-206">Limit operací</span><span class="sxs-lookup"><span data-stu-id="b5fb4-206">Operations limit</span></span></td>
<td><span data-ttu-id="b5fb4-207">Zadejte maximální částku povolenou pro operace, které mají protistrany v hotovosti.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-207">Enter the maximum amount that is allowed for operations with counteragents in cash.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b5fb4-208">Zaúčtování k dřívějšímu datu</span><span class="sxs-lookup"><span data-stu-id="b5fb4-208">Posting on earlier date</span></span></td>
<td><span data-ttu-id="b5fb4-209">Zaškrtněte toto políčko pro povolení peněžních transakcí, které mají být zaúčtovány před posledním datem peněžní transakce.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-209">Select this check box to enable cash transactions to be posted before the last date of the cash transaction.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b5fb4-210">Dimenze</span><span class="sxs-lookup"><span data-stu-id="b5fb4-210">Dimensions</span></span></td>
<td><span data-ttu-id="b5fb4-211">Zadejte rozměry v polích <strong>Kód oddělení</strong>, <strong>Analytický kód</strong> a <strong>Účel kódu</strong>.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-211">Enter dimensions in the <strong>Department code</strong>, <strong>Analytical code</strong>, and <strong>Purpose code</strong> fields.</span></span> <span data-ttu-id="b5fb4-212">Tyto informace se projeví ve formuláři Tisk pokladních dokladů.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-212">The printing form for cash documents will reflect this information.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b5fb4-213">Použít stav potvrzení</span><span class="sxs-lookup"><span data-stu-id="b5fb4-213">Use confirm status</span></span></td>
<td><span data-ttu-id="b5fb4-214">Toto políčko zaškrtněte, pokud chcete během procesu schvalování pokladních dokladů použít další stav, <strong>Potvrzeno</strong>.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-214">Select this check box to use an additional status, <strong>Confirmed</strong>, during the approval process for cash documents.</span></span> <span data-ttu-id="b5fb4-215">(Další informace naleznete v části &quot;Schválení a zaúčtování platebních transakcí&quot;.)</span><span class="sxs-lookup"><span data-stu-id="b5fb4-215">(For more information, see the &quot;Cash transaction approval and posting&quot; section.)</span></span></td>
</tr>
</tbody>
</table>

### <a name="set-up-cash-journal-names-in-general-ledger"></a><span data-ttu-id="b5fb4-216">Nastavení názvů hotovostních deníků v hlavní knize</span><span class="sxs-lookup"><span data-stu-id="b5fb4-216">Set up cash journal names in General ledger</span></span>

<span data-ttu-id="b5fb4-217">Chcete-li vytvořit deník pro zaúčtování platební transakce, přejděte na **Hlavní kniha** &gt; **Nastavení deníku** &gt; **Názvy deníku** a vytvořte nový záznam.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-217">To create a journal for cash transaction posting, go to **General ledger** &gt; **Journal setup** &gt; **Journal names**, and create a new record.</span></span> <span data-ttu-id="b5fb4-218">V poli **Typ deníku** zadejte **Hotovost**.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-218">In the **Journal type** field, specify **Cash**.</span></span> <span data-ttu-id="b5fb4-219">Definujte další výchozí parametry deníku podle potřeby.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-219">Define other default journal parameters as you require.</span></span>

## <a name="daily-cash-operations-via-a-slip-journal"></a><span data-ttu-id="b5fb4-220">Denní pokladní operace prostřednictvím deníku dokladů</span><span class="sxs-lookup"><span data-stu-id="b5fb4-220">Daily cash operations via a Slip journal</span></span>
<span data-ttu-id="b5fb4-221">Chcete-li vytvořit pokladní doklad prostřednictvím deníku dokladu, přejděte na **Řízení hotovosti a banky** &gt; **Platební transakce** &gt; **Deník** a vytvořte nový deník.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-221">To create a cash document via a Slip journal, go to **Cash and bank management** &gt; **Cash transactions** &gt; **Slip journal**, and create a new journal.</span></span> <span data-ttu-id="b5fb4-222">V podokně akcí klikněte na **Řádky**.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-222">On the Action Pane, click **Lines**.</span></span> <span data-ttu-id="b5fb4-223">Přidejte nový řádek a zadejte následující informace.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-223">Add a new line, and enter the following information.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b5fb4-224">Pole</span><span class="sxs-lookup"><span data-stu-id="b5fb4-224">Field</span></span></th>
<th><span data-ttu-id="b5fb4-225">popis</span><span class="sxs-lookup"><span data-stu-id="b5fb4-225">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b5fb4-226">Datum</span><span class="sxs-lookup"><span data-stu-id="b5fb4-226">Date</span></span></td>
<td><span data-ttu-id="b5fb4-227">Zadejte datum pro transakce.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-227">Enter the date of the transaction.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b5fb4-228">Účet</span><span class="sxs-lookup"><span data-stu-id="b5fb4-228">Account</span></span></td>
<td><span data-ttu-id="b5fb4-229">Vyberte pokladní účet.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-229">Select the cash account.</span></span> <span data-ttu-id="b5fb4-230">Ve výchozím nastavení je pokladní účet specifikován podle parametrů Hotovost a řízení banky.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-230">By default, a cash account is specified in the Cash and bank management parameters.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b5fb4-231">popis</span><span class="sxs-lookup"><span data-stu-id="b5fb4-231">Description</span></span></td>
<td><span data-ttu-id="b5fb4-232">Zadejte vysvětlující text pro použití s transakcí.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-232">Enter explanatory text for the transaction.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b5fb4-233">Má dáti Dal</span><span class="sxs-lookup"><span data-stu-id="b5fb4-233">Debit Credit</span></span></td>
<td><span data-ttu-id="b5fb4-234">Zadejte částku pokladního dokladu do jednoho z těchto polí:</span><span class="sxs-lookup"><span data-stu-id="b5fb4-234">Enter cash document amount in one of these fields:</span></span>
<ul>
<li><span data-ttu-id="b5fb4-235"><strong>Má Dáti</strong> – toto pole slouží k registraci přijaté hotovosti a hotovostního refundačního dokladu.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-235"><strong>Debit</strong> – Use this field to register cash receipts and a Cash reimbursement slip.</span></span></li>
<li><span data-ttu-id="b5fb4-236"><strong>Dal</strong> – toto pole slouží k registraci přijaté hotovosti a hotovostního refundačního dokladu.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-236"><strong>Credit</strong> – Use this field to register cash expenditures and a Cash disbursement slip.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b5fb4-237">Typ protiúčtu Protiúčet</span><span class="sxs-lookup"><span data-stu-id="b5fb4-237">Offset account type Offset account</span></span></td>
<td><span data-ttu-id="b5fb4-238">Vyberte typ a číslo protiúčtu.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-238">Select an offset account type and offset account number.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b5fb4-239">Měna</span><span class="sxs-lookup"><span data-stu-id="b5fb4-239">Currency</span></span></td>
<td><span data-ttu-id="b5fb4-240">Vyberte kód měny pro transakci.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-240">Select the code for the transaction currency.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b5fb4-241">Doklad</span><span class="sxs-lookup"><span data-stu-id="b5fb4-241">Voucher</span></span></td>
<td><span data-ttu-id="b5fb4-242">Toto pole je vyplněno automaticky na základě nastavení deníku.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-242">This field is filled in automatically, based on the journal setup.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b5fb4-243">Číslo objednávky</span><span class="sxs-lookup"><span data-stu-id="b5fb4-243">Order number</span></span></td>
<td><span data-ttu-id="b5fb4-244">Pokud není nastavena žádná číselná řada pro pokladní účet, toto pole je vyplněno automaticky na základě číselné řady, která je určena v parametrech.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-244">If no other number sequence is set up for the cash account, this field is filled in automatically, based on the number sequence that is specified in the parameters.</span></span> <span data-ttu-id="b5fb4-245">V tomto poli můžete podle potřeby ručně zadat číslo objednávky.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-245">You can manually enter an order number in this field as you require.</span></span> <span data-ttu-id="b5fb4-246">Aby se zabránilo nekonzistentnímu číslování pokladních dokladů, platí následující kontrola: číslo pokladního dokladu, který má starší datum operace, nemůže být vyšší než číslo pokladního dokladu, které má pozdější datum operace.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-246">To prevent inconsistence in cash document numbering, the following control is applied: the number of a cash document that has an earlier date of operation can&#39;t be higher than number of a cash document that has a later date of operation.</span></span> <span data-ttu-id="b5fb4-247">Pokud tuto kontrolu nepožadujete, zaškrtněte políčko <strong>Zaúčtování k dřívějšímu datu</strong> v parametrech pokladny a banky.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-247">If you don&#39;t require this control, select the <strong>Posting on earlier date</strong> check box in the Cash and bank management parameters.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b5fb4-248">Stav schválení</span><span class="sxs-lookup"><span data-stu-id="b5fb4-248">Approval status</span></span></td>
<td><span data-ttu-id="b5fb4-249">Stav první transakce je <strong>Žádný</strong>.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-249">The first transaction status is <strong>None</strong>.</span></span> <span data-ttu-id="b5fb4-250">Informace o tom, jak nastavit stav transakce, naleznete v části &quot;Schválení a zaúčtování platebních transakcí&quot;.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-250">For information about how to set the transaction status, See the &quot;Cash transaction approval and posting&quot; section.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b5fb4-251">Typ dokumentu</span><span class="sxs-lookup"><span data-stu-id="b5fb4-251">Document type</span></span></td>
<td><span data-ttu-id="b5fb4-252">Toto pole na kartě <strong>Pokladní doklad</strong> kartu je vyplněno automaticky na základě množství, které jste zadali pro pokladní doklad:</span><span class="sxs-lookup"><span data-stu-id="b5fb4-252">This field on the <strong>Cash order</strong> tab is filled in automatically, based on the amount that you entered for the cash document:</span></span>
<ul>
<li><span data-ttu-id="b5fb4-253"><strong>Hotovostní refundační doklad</strong> – tato hodnota se používá, pokud jste zadali množství do pole <strong>Má Dáti</strong> pro pokladní účet.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-253"><strong>Cash reimbursement slip</strong> – This value is used if you entered an amount in the <strong>Debit</strong> field for the cash account.</span></span></li>
<li><span data-ttu-id="b5fb4-254"><strong>Hotovostní výdajový doklad</strong> – tato hodnota se používá, pokud jste zadali množství do pole <strong>Dal</strong> pro pokladní účet.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-254"><strong>Cash disbursement slip</strong> – This value is used if you entered an amount in the <strong>Credit</strong> field for the cash account</span></span></li>
<li><span data-ttu-id="b5fb4-255"><strong>Oprava</strong> – zadali jste zápornou částku do pole <strong>Má Dáti</strong> nebo <strong>Dal</strong> pro pokladní účet.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-255"><strong>Correction</strong> – You entered a negative amount in either the <strong>Debit</strong> field or the <strong>Credit</strong> field for the cash account.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b5fb4-256">Skupina prodejní daně</span><span class="sxs-lookup"><span data-stu-id="b5fb4-256">Sales tax group</span></span></td>
<td><span data-ttu-id="b5fb4-257">Zadejte skupinu DPH pro výpočet daní z operace.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-257">Specify a sales tax group to calculate taxes on the operation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b5fb4-258">Skupina DPH zboží</span><span class="sxs-lookup"><span data-stu-id="b5fb4-258">Item sales tax group</span></span></td>
<td><span data-ttu-id="b5fb4-259">Zadejte skupinu DPH položky pro výpočet daní z operace.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-259">Specify an item sales tax group to calculate taxes on the operation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b5fb4-260">Důvod</span><span class="sxs-lookup"><span data-stu-id="b5fb4-260">Reason</span></span></td>
<td><span data-ttu-id="b5fb4-261">Na kartě <strong>Pokladní doklad</strong> zadejte text popisující předmět transakce.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-261">On the <strong>Cash order</strong> tab, enter text that describes the transaction subject.</span></span> <span data-ttu-id="b5fb4-262">Tento text bude vytištěn na formuláři zprávy o hotovostním dokladu.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-262">This text will be printed on the cash slip reporting form.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b5fb4-263">Datum dokumentu</span><span class="sxs-lookup"><span data-stu-id="b5fb4-263">Document Date</span></span></td>
<td><span data-ttu-id="b5fb4-264">Zadejte popis, číslo a datum primárního dokladu, který je důvodem pro transakci (například sestavy záloh, faktura nebo objednávka).</span><span class="sxs-lookup"><span data-stu-id="b5fb4-264">Enter the description, number, and date of the primary document that is the reason for the transaction (for example, advance reports, invoice, or order).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b5fb4-265">Typ prodejního zástupce</span><span class="sxs-lookup"><span data-stu-id="b5fb4-265">Representative type</span></span></td>
<td><span data-ttu-id="b5fb4-266">Toto pole může mít následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="b5fb4-266">This field can have the following values:</span></span>
<ul>
<li><span data-ttu-id="b5fb4-267"><strong>Pracovník</strong> – vyhledávací hodnota <strong>Zástupce</strong> obsahuje seznam zaměstnanců, pokud je hodnota v poli <strong>Protiúčet</strong> nastavena na <strong>Hlavní kniha</strong> nebo <strong>Banka</strong>, nebo seznam kontaktních osob protistrany, pokud je v poli <strong>Protiúčet</strong> nastavena hodnota <strong>Zákazník</strong> nebo <strong>Dodavatel</strong>.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-267"><strong>Worker</strong> – The <strong>Representative</strong> lookup contains a list of employees if the <strong>Offset account</strong> field is set to <strong>Ledger</strong> or <strong>Bank</strong>, or a list of the counteragent&#39;s contact persons if the <strong>Offset account</strong> field is set to <strong>Customer</strong> or <strong>Vendor</strong>.</span></span> <span data-ttu-id="b5fb4-268">Při nastavování zástupců přejděte na <strong>Základní</strong> &gt; <strong>Nastavení</strong> &gt; <strong>Kontakty</strong> &gt; <strong>Kontaktní osoba</strong>.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-268">To set up representatives, go to <strong>Basic</strong> &gt; <strong>Setup</strong> &gt; <strong>Contacts</strong> &gt; <strong>Contact person</strong>.</span></span></li>
<li><span data-ttu-id="b5fb4-269"><strong>Ostatní</strong> – vyhledávací hodnota <strong>Zástupce</strong> obsahuje seznam jiných klientů.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-269"><strong>Other</strong> – The <strong>Representative</strong> lookup contains a list of other clients.</span></span> <span data-ttu-id="b5fb4-270">Pokud chcete nastavit příjemce, kteří nejsou uvedeni v tabulce <strong>Zákazníci</strong> nebo <strong>Dodavatelé</strong>, přejděte na <strong>Hlavní kniha</strong> &gt; <strong>Příjemci</strong>.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-270">To set up receivers who don&#39;t appear in the <strong>Customers</strong> or <strong>Vendors</strong> table, go to <strong>General ledger</strong> &gt; <strong>Receivers</strong>.</span></span> <span data-ttu-id="b5fb4-271">Tento typ je dostupný pouze pro Lotyšsko.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-271">This type is available only for Latvia.</span></span> <span data-ttu-id="b5fb4-272">(Měl by být povolen klíč konfigurace <strong>CSELatvia</strong>.)</span><span class="sxs-lookup"><span data-stu-id="b5fb4-272">(The <strong>CSELatvia</strong> configuration key should be enabled.)</span></span></li>
<li><span data-ttu-id="b5fb4-273"><strong>Dodavatel</strong> – vyhledávací hodnota <strong>Zástupce</strong> obsahuje seznam dodavatelů.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-273"><strong>Vendor</strong> – The <strong>Representative</strong> lookup contains a list of vendors.</span></span> <span data-ttu-id="b5fb4-274">Při nastavování dodavatelů přejděte na položky <strong>Závazky</strong> &gt; <strong>Dodavatelé</strong>.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-274">To set up vendors, go to <strong>Accounts payable</strong> &gt; <strong>Vendors</strong>.</span></span></li>
<li><span data-ttu-id="b5fb4-275"><strong>Zákazník</strong> – vyhledávací hodnota <strong>Zástupce</strong> obsahuje seznam zákazníků.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-275"><strong>Customer</strong> – The <strong>Representative</strong> lookup contains a list of customers.</span></span> <span data-ttu-id="b5fb4-276">Při nastavování zákazníků přejděte na položky <strong>Pohledávky</strong> &gt; <strong>Zákazníci</strong>.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-276">To set up customers, go to <strong>Accounts receivable</strong> &gt; <strong>Customers</strong>.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b5fb4-277">Zástupce</span><span class="sxs-lookup"><span data-stu-id="b5fb4-277">Representative</span></span></td>
<td><span data-ttu-id="b5fb4-278">Vyberte zástupce typu, který je uveden v poli <strong>Typ zástupce</strong>.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-278">Select a representative of the type that you specified in the <strong>Representative type</strong> field.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b5fb4-279">Jméno osoby</span><span class="sxs-lookup"><span data-stu-id="b5fb4-279">Name of person</span></span></td>
<td><span data-ttu-id="b5fb4-280">Toto pole je vyplněno automaticky na základě hodnot v poli <strong>Protiúčet</strong> a <strong>Zástupce</strong>.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-280">This field is filled in automatically, based on the <strong>Offset account</strong> and <strong>Representative</strong> fields.</span></span> <span data-ttu-id="b5fb4-281">Tyto informace se projeví ve formuláři pro tisk pokladních dokladů.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-281">The printing form for cash slips will reflect this information.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b5fb4-282">Průkaz totožnosti</span><span class="sxs-lookup"><span data-stu-id="b5fb4-282">Identity card</span></span></td>
<td><span data-ttu-id="b5fb4-283">Toto pole je vyplněno automaticky na základě dat průkazu totožnosti kontaktní osoby (zástupce).</span><span class="sxs-lookup"><span data-stu-id="b5fb4-283">This field is filled in automatically, based on the identity card data for the contact person (representative).</span></span> <span data-ttu-id="b5fb4-284">Pokud je hodnota v poli <strong>Typ protiúčtu</strong> nastavena na <strong>Držitel zálohy</strong> a hodnota v poli <strong>Protiúčet</strong> pole je nastavena na číslo zaměstnance, lze od zaměstnance nebo pro něho provést peněžní příjmy a výdaje.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-284">If the <strong>Offset account type</strong> field is set to <strong>Advance holder</strong>, and the <strong>Offset account</strong> field is set to an employee number, cash receipts or expenditures can be done from or to the employee.</span></span> <span data-ttu-id="b5fb4-285">V tomto případě je pole <strong>Průkaz totožnosti</strong> vyplněno automaticky s využitím dat z průkazu totožnosti z tabulky <strong>Zaměstnanec</strong> (<strong>účtování zaměstnanců</strong> &gt; <strong>Tabulka zaměstnanců</strong>).</span><span class="sxs-lookup"><span data-stu-id="b5fb4-285">In this case the <strong>Identity card</strong> field is filled in automatically by using data for the identity card from the <strong>Employee</strong> table (<strong>Staff accounting</strong> &gt; <strong>Employee table</strong>).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b5fb4-286">Účel</span><span class="sxs-lookup"><span data-stu-id="b5fb4-286">Purpose</span></span></td>
<td><span data-ttu-id="b5fb4-287">V tabulce <strong>Účel</strong> definujte jeden nebo více kódů místa určení částky transakce.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-287">In the <strong>Purpose</strong> table, define one or more destination codes for the transaction amount.</span></span> <span data-ttu-id="b5fb4-288">Vyberte kód místa určení v poli <strong>Účel</strong> a zadejte vysvětlení do pole <strong>Text transakce</strong>.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-288">Select a destination code in the <strong>Purpose</strong> field, and enter an explanation in the <strong>Transaction text</strong> field.</span></span> <span data-ttu-id="b5fb4-289">Do pole <strong>Částka</strong> zadejte částku v měně transakce.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-289">In the <strong>Amount</strong> field, enter an amount in the transaction currency.</span></span> <span data-ttu-id="b5fb4-290">V poli <strong>Procento%</strong> se zobrazuje poměr cílové částky k celkové částce transakce vyjádřený v procentech.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-290">The <strong>Percent</strong> field shows, as a percentage, the ratio of the destination amount to the total transaction amount.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b5fb4-291">Zůstatek</span><span class="sxs-lookup"><span data-stu-id="b5fb4-291">Remainder</span></span></td>
<td><span data-ttu-id="b5fb4-292">Zbývající částka, která je vypočtena.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-292">The remaining amount that is calculated.</span></span> <span data-ttu-id="b5fb4-293">Všimněte si, že celá částka transakce musí být přiřazena ke kódům místa určení.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-293">Note that the whole transaction amount must be assigned to destination codes.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b5fb4-294">Úřední osoby</span><span class="sxs-lookup"><span data-stu-id="b5fb4-294">Officials</span></span></td>
<td><span data-ttu-id="b5fb4-295">Na kartě <strong>Úředníci</strong> zadejte názvy a názvy pro odpovědné osoby: ředitel, hlavní účetní a pokladní.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-295">On the <strong>Officials</strong> tab, specify the names and titles for responsible persons: Director, Chief accountant, and Cashier.</span></span> <span data-ttu-id="b5fb4-296">Hodnoty <strong>Pozice</strong> jsou určeny nastavením úředníků na kartě <strong>Obecné</strong> a <strong>Hlavní kniha</strong> stránky <strong>Úředníci</strong> (<strong>Základní</strong> &gt; <strong>Nastavení</strong> &gt; <strong>Kontakty</strong> &gt; <strong>Úředníci</strong>).</span><span class="sxs-lookup"><span data-stu-id="b5fb4-296">The <strong>Position</strong> values are determined by the setup of officials on the <strong>General</strong> and <strong>Ledger</strong> tabs of the <strong>Officials</strong> page (<strong>Basic</strong> &gt; <strong>Setup</strong> &gt; <strong>Contacts</strong> &gt; <strong>Officials</strong>).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b5fb4-297">Záloha</span><span class="sxs-lookup"><span data-stu-id="b5fb4-297">Prepayment</span></span></td>
<td><span data-ttu-id="b5fb4-298">Toto políčko zaškrtněte, pokud je daná transakce zálohová.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-298">Select this check box if the transaction is a prepayment.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b5fb4-299">Účetní profil</span><span class="sxs-lookup"><span data-stu-id="b5fb4-299">Posting profile</span></span></td>
<td><span data-ttu-id="b5fb4-300">Zadejte krátký název hotovostního účtu.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-300">Enter the posting profile for the cash account.</span></span> <span data-ttu-id="b5fb4-301">Ve výchozím nastavení se používá účetní profil, který je určen v parametrech pokladny a banky.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-301">By default, the posting profile that is specified in the Cash and bank management parameters is used.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b5fb4-302">Účetní profil protiúčtu</span><span class="sxs-lookup"><span data-stu-id="b5fb4-302">Offset posting profile</span></span></td>
<td><span data-ttu-id="b5fb4-303">Zadejte profil zaúčtování vybraného protiúčtu.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-303">Enter the posting profile for the selected offset account.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b5fb4-304">Celková částka</span><span class="sxs-lookup"><span data-stu-id="b5fb4-304">Total amount</span></span></td>
<td><span data-ttu-id="b5fb4-305">Ve skupině polí <strong>Celková částka</strong> v dolní části stránky je v poli <strong>Refundace</strong> uveden součet, který se vypočte pro všechny hotovostní refundační doklady, které jsou zadány v aktuálním deníku, a v poli <strong>Úhr.</strong> se zobrazuje součet pro všechny hotovostní výdajové doklady.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-305">In the <strong>Total amount</strong> field group at the bottom of the page, the <strong>Reimb</strong> field shows the total that is calculated for all Cash reimbursement slips that are entered in the current journal, and the <strong>Disb</strong> field shows the total for all Cash disbursement slips.</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b5fb4-306">Při kontrole položky deníku v podokně akcí klepněte na **Ověřit**.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-306">To check journal entries, on the Action Pane, click **Validate**.</span></span>

## <a name="daily-cash-operations-via-a-general-journal"></a><span data-ttu-id="b5fb4-307">Denní pokladní operace prostřednictvím hlavního deníku</span><span class="sxs-lookup"><span data-stu-id="b5fb4-307">Daily cash operations via a General journal</span></span>
<span data-ttu-id="b5fb4-308">Chcete-li vytvořit platební transakce prostřednictvím hlavního deníku, přejděte na **Hlavní kniha** &gt; **Položky deníku** &gt; **Hlavní deníky**a vytvořte nový deník.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-308">To create a cash transaction via a General journal, go to **General ledger** &gt; **Journal entries** &gt; **General journals**, and create a new journal.</span></span> <span data-ttu-id="b5fb4-309">V podokně akcí klikněte na **Řádky**.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-309">On the Action Pane, click **Lines**.</span></span> <span data-ttu-id="b5fb4-310">Přidejte nový řádek a zadejte následující informace.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-310">Add a new line, and enter the following information.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b5fb4-311">Pole</span><span class="sxs-lookup"><span data-stu-id="b5fb4-311">Field</span></span></th>
<th><span data-ttu-id="b5fb4-312">popis</span><span class="sxs-lookup"><span data-stu-id="b5fb4-312">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b5fb4-313">Datum</span><span class="sxs-lookup"><span data-stu-id="b5fb4-313">Date</span></span></td>
<td><span data-ttu-id="b5fb4-314">Zadejte datum pro transakce.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-314">Enter the date of the transaction.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b5fb4-315">Typ účtu</span><span class="sxs-lookup"><span data-stu-id="b5fb4-315">Account type</span></span></td>
<td><span data-ttu-id="b5fb4-316">Vyberte <strong>Pokladní hotovost</strong>.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-316">Select <strong>Petty cash</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b5fb4-317">Účet</span><span class="sxs-lookup"><span data-stu-id="b5fb4-317">Account</span></span></td>
<td><span data-ttu-id="b5fb4-318">Vyberte číslo pokladního účtu.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-318">Select the cash account number.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b5fb4-319">Text transakce</span><span class="sxs-lookup"><span data-stu-id="b5fb4-319">Transaction text</span></span></td>
<td><span data-ttu-id="b5fb4-320">Zadejte vysvětlující text pro použití s transakcí.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-320">Enter explanatory text for the transaction.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b5fb4-321">Má dáti Dal</span><span class="sxs-lookup"><span data-stu-id="b5fb4-321">Debit Credit</span></span></td>
<td><span data-ttu-id="b5fb4-322">Zadejte částku pokladního dokladu do jednoho z těchto polí:</span><span class="sxs-lookup"><span data-stu-id="b5fb4-322">Enter cash document amount in one of these fields:</span></span>
<ul>
<li><span data-ttu-id="b5fb4-323"><strong>Má Dáti</strong> – toto pole slouží k registraci přijaté hotovosti a hotovostního refundačního dokladu.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-323"><strong>Debit</strong> – Use this field to register cash receipts and a Cash reimbursement slip.</span></span></li>
<li><span data-ttu-id="b5fb4-324"><strong>Dal</strong> – toto pole slouží k registraci přijaté hotovosti a hotovostního refundačního dokladu.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-324"><strong>Credit</strong> – Use this field to register cash expenditures and a Cash disbursement slip.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b5fb4-325">Typ protiúčtu Protiúčet</span><span class="sxs-lookup"><span data-stu-id="b5fb4-325">Offset account type Offset account</span></span></td>
<td><span data-ttu-id="b5fb4-326">Vyberte typ a číslo protiúčtu.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-326">Select an offset account type and offset account number.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b5fb4-327">Měna</span><span class="sxs-lookup"><span data-stu-id="b5fb4-327">Currency</span></span></td>
<td><span data-ttu-id="b5fb4-328">Vyberte kód měny pro transakci.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-328">Select the code for the transaction currency.</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b5fb4-329">Na kartě **Fakturace** můžete zadat účetní profily pro vybraný účet a protiúčet.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-329">On the **Invoice** tab, you can specify posting profiles for the selected account and offset account.</span></span> <span data-ttu-id="b5fb4-330">Pokud je registrovaná transakce placením zálohy, vyberte zaškrtávací políčko **Zálohy** na kartě **Platba**. Ve skupině polí **Zástupce** vyplňte pole stejně jako u řádků deníku dodacích listů, které chcete vytisknout v sestavě **Hotovost**.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-330">If the registered transaction is a prepayment, select the **Prepayment** check box on the **Payment** tab. In the **Representative** field group, fill in the fields as you did for the Slip journal lines to print on the **Cash** report.</span></span> <span data-ttu-id="b5fb4-331">Při kontrole položky deníku v podokně akcí klepněte na **Ověřit**.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-331">To check journal entries, on the Action Pane, click **Validate**.</span></span>

## <a name="cash-transaction-approval-and-posting"></a><span data-ttu-id="b5fb4-332">Schválení a zaúčtování hotovostní transakce</span><span class="sxs-lookup"><span data-stu-id="b5fb4-332">Cash transaction approval and posting</span></span>
<span data-ttu-id="b5fb4-333">Pro hotovostní transakce mohou být použity následující stavy: **žádný**, **potvrzeno**, **schváleno** a **odmítnuto**.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-333">For cash transactions, the following statuses can be applied: **None**, **Confirmed**, **Approved**, and **Rejected**.</span></span> <span data-ttu-id="b5fb4-334">Parametr **použít stav potvrzení** na pevné záložce **Schválení** karty **Hotovost** v okně **Pokladna a banka** &gt; **Nastavení** &gt; **Parametry pokladny a banky** umožňuje aktivovat další dva stavy: **Potvrzeno** a **Odmítnuto**.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-334">A **Use confirm status** parameter on the **Approval** FastTab of the **Cash** tab at **Cash and bank management** &gt; **Setup** &gt; **Cash and bank management parameters** lets you activate two additional statuses: **Confirmed** and **Rejected**.</span></span> <span data-ttu-id="b5fb4-335">Potvrzení je vhodné, když jsou vydávány pokladní doklady a hotovostní příjmy a výdaje, které jsou sdíleny mezi dvěma zaměstnanci: účetní a pokladní.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-335">Confirmation is appropriate when cash documents are issued, and cash receipts or expenditures are shared between two employees: accountant and cashier.</span></span> <span data-ttu-id="b5fb4-336">Funkce **Resetovat stav** změní stav aktuální transakce.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-336">The **Reset status** function changes the current transaction status.</span></span> <span data-ttu-id="b5fb4-337">Z možnosti **Schválené** se stane **potvrzeno** a z možnosti **potvrzeno** se stane **žádný**.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-337">**Approved** becomes **Confirmed**, and **Confirmed** becomes **None**.</span></span> <span data-ttu-id="b5fb4-338">Položky pokladního deníku lze upravit, pouze pokud je stav **žádný**.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-338">Cash journal entries can be edited only when the status is **None**.</span></span> <span data-ttu-id="b5fb4-339">Hotovostní transakce mohou být odmítnuty pouze v případě, že je stav transakce **potvrzeno**.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-339">Cash transactions can be rejected only if the transaction status is **Confirmed**.</span></span> <span data-ttu-id="b5fb4-340">Odmítnuté platební doklady jsou k dispozici v sestavě **Deník registrace pokladních dokladů**, ale neprojeví se v sestavě **Pokladní kniha**.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-340">Rejected cash documents are included on the **Journal of registration of cash documents** report, but they aren't reflected on the **Cash book** report.</span></span> <span data-ttu-id="b5fb4-341">K potvrzení transakce vyberte odpovídající řádek deníku dokladů a klepněte na tlačítko **Schválení dokumentů** &gt; **potvrzení**.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-341">To confirm a transaction, select the corresponding Slip journal line, and then click **Documents approval** &gt; **Confirm**.</span></span> <span data-ttu-id="b5fb4-342">Číslo objednávky je generováno podle určené číselné řady.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-342">An order number is generated, based on the specified number sequence.</span></span> <span data-ttu-id="b5fb4-343">Stav transakce se změní na **potvrzeno** a již nemůžete upravit řádek deníku.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-343">The transaction status is changed to **Confirmed**, and you can no longer edit the journal line.</span></span> <span data-ttu-id="b5fb4-344">Pokladní zůstatek účtu se nezmění.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-344">The cash account balance remains unchanged.</span></span> <span data-ttu-id="b5fb4-345">Pokud chcete pokladní doklad odmítnout, klepněte na tlačítko **Schválení dokumentů** &gt; **odmítnout**.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-345">To reject a cash document, click **Documents approval** &gt; **Reject**.</span></span> <span data-ttu-id="b5fb4-346">Tato možnost je k dispozici pouze pro dokumenty, které mají stav **potvrzeno**.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-346">This option is available only for documents that have **Confirmed** status.</span></span> <span data-ttu-id="b5fb4-347">Ke schválení transakce vyberte odpovídající řádek deníku dokladů a klepněte na tlačítko **Schválení dokumentů** &gt; **Schválit**.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-347">To approve a transaction, select the corresponding Slip journal line, and then click **Documents approval** &gt; **Approve**.</span></span> <span data-ttu-id="b5fb4-348">Stav **Schváleno** znamená, že peněžní prostředky byly přijaty nebo použity.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-348">The **Approved** status indicates that cash funds are received or expended.</span></span> <span data-ttu-id="b5fb4-349">Zůstatek hotovosti se změní.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-349">The cash balance is changed.</span></span> <span data-ttu-id="b5fb4-350">Platební transakci lze zaúčtovat.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-350">The cash transaction can be posted.</span></span> <span data-ttu-id="b5fb4-351">Pokud chcete zrušit stav **schváleno** obnovit stav na **žádný**, klepněte na tlačítko **schválení dokumentů** &gt; **resetovat stav**.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-351">To cancel an **Approved** status and reset the status to **None**, click **Documents approval** &gt; **Reset status**.</span></span> <span data-ttu-id="b5fb4-352">Zaúčtovat lze pouze schválené hotovostní transakce.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-352">Only approved cash transactions can be posted.</span></span> <span data-ttu-id="b5fb4-353">Když chcete zaúčtovat deník, klepněte na **Zaúčtovat** &gt; **Zaúčtovat**.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-353">To post a journal, click **Post** &gt; **Post**.</span></span>

## <a name="print-a-cash-order"></a><span data-ttu-id="b5fb4-354">Tisk platební slevy</span><span class="sxs-lookup"><span data-stu-id="b5fb4-354">Print a cash order</span></span>
<span data-ttu-id="b5fb4-355">Pokud chcete vytisknout pokladní doklad, vyberte řádek deníku dokladů a v podokně akcí klepněte na tlačítko **tisk** &gt; **Sestava pokladního dokladu**.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-355">To print a cash order, select a Slip journal line, and then, on the Action Pane, click **Print** &gt; **Cash order report**.</span></span> <span data-ttu-id="b5fb4-356">Systém generuje tiskový formulář pro hotovostní refundační doklad nebo hotovostní výdajový doklad, podle toho, zda je zadána částka v poli **MD** nebo **Dal** pro vybraný řádek:</span><span class="sxs-lookup"><span data-stu-id="b5fb4-356">The system generates a printing form for either a Cash reimbursement slip or a Cash disbursement slip, depending on whether an amount is entered in the **Debit** field the or **Credit** field for the selected line:</span></span>

-   <span data-ttu-id="b5fb4-357">Pokud je částka v poli **MD**: pokladní refundační doklad</span><span class="sxs-lookup"><span data-stu-id="b5fb4-357">If there is an amount in the **Debit** field: Cash reimbursement slip</span></span>
-   <span data-ttu-id="b5fb4-358">Pokud je částka v poli **Dal**: hotovostní výdajový doklad</span><span class="sxs-lookup"><span data-stu-id="b5fb4-358">If there is an amount in the **Credit** field: Cash disbursement slip</span></span>

<span data-ttu-id="b5fb4-359">Řádky deníku dokladů, které mají stav **potvrzeno**, **schváleno** nebo **odmítnuto** lze vytisknout.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-359">Slip journal lines that have **Confirmed**, **Approved**, or **Rejected** status can be printed.</span></span> <span data-ttu-id="b5fb4-360">Můžete také vytisknout pokladní doklady objednávek na v **řízení hotovosti a banky** &gt; **Dotazy a sestavy** &gt; **Pokladní doklad**.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-360">You can also print cash order documents at **Cash and bank management** &gt; **Inquires and reports** &gt; **Cash order**.</span></span>

## <a name="periodic-tasks"></a><span data-ttu-id="b5fb4-361">Periodické úlohy</span><span class="sxs-lookup"><span data-stu-id="b5fb4-361">Periodic tasks</span></span>
<span data-ttu-id="b5fb4-362">Následující úkoly lze provést v okně **Řízení hotovosti a banky** &gt; **Pravidelné úlohy**.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-362">The following tasks can be performed at **Cash and bank management** &gt; **Periodic tasks**.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b5fb4-363">Periodická úloha</span><span class="sxs-lookup"><span data-stu-id="b5fb4-363">Periodic task</span></span></th>
<th><span data-ttu-id="b5fb4-364">popis</span><span class="sxs-lookup"><span data-stu-id="b5fb4-364">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b5fb4-365">Zkontrolovat limit salda</span><span class="sxs-lookup"><span data-stu-id="b5fb4-365">Check balance limit</span></span></td>
<td><span data-ttu-id="b5fb4-366">Zkontrolujte zůstatek na vybraném hotovostním účtu v určený den a zobrazte výsledek v informační zprávě.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-366">Check the balance for the selected cash account on the specified date, and show the result in an information message.</span></span> <span data-ttu-id="b5fb4-367">Ve výpočtu zůstatku lze počítat pouze schválené transakce.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-367">Only approved transactions can be counted in the balance calculation.</span></span> <span data-ttu-id="b5fb4-368">Transakce, které jsou označeny jako <strong>pro mzdy</strong> nejsou zohledněny.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-368">Transactions that are marked as <strong>For payroll</strong> aren&#39;t considered.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b5fb4-369">Přepočet salda hotovosti</span><span class="sxs-lookup"><span data-stu-id="b5fb4-369">Cash balance recalculation</span></span></td>
<td><span data-ttu-id="b5fb4-370">Pomocí této úlohy se ujistěte, že zůstatky hlavní knihy pro pokladní účty odpovídají zůstatku hotovosti.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-370">Use this task to make sure that the ledger balances for cash accounts fit the cash balance.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b5fb4-371">Vytvoření výpisu hotovosti (pro pouze Polsko)</span><span class="sxs-lookup"><span data-stu-id="b5fb4-371">Cash report creation (for Poland only)</span></span></td>
<td><span data-ttu-id="b5fb4-372">Vytvořte sestavu <strong>hotovosti</strong>.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-372">Create a <strong>Cash</strong> report.</span></span> <span data-ttu-id="b5fb4-373">Číslo sestavy <strong>hotovosti</strong> se generuje na základě číselné řady nastavené pro <strong>číslo sestavy</strong>.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-373">The <strong>Cash</strong> report number is generated based on the number sequence that is set up for <strong>Report number</strong>.</span></span> <span data-ttu-id="b5fb4-374">V dialogovém okně pole pro úkol, v poli <strong>Datum</strong>, zadejte poslední datum, pro které by měla být započítána platební transakce pro <strong>platební</strong> sestavu.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-374">In the dialog box for the task, in the <strong>To date</strong>, specify the last date for which cash transactions should be counted for the <strong>Cash</strong> report.</span></span> <span data-ttu-id="b5fb4-375">Pomocí funkce <strong>filtr</strong> na kartě <strong>Záznamy pro zahrnutí</strong> zadejte další kritéria omezující výběr hotovostních transakcí.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-375">Use the <strong>Filter</strong> function on the <strong>Records to include</strong> tab to specify additional criteria to limit the selection of cash transactions.</span></span> <span data-ttu-id="b5fb4-376">Tato kritéria mohou zahrnovat čísla platebního účtu a kódy měn.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-376">These criteria can include cash account numbers and currency codes.</span></span> <span data-ttu-id="b5fb4-377">V poli <strong>Vytvořit podle</strong> vyberte uživatele, který bude za vytvoření sestavy zodpovědný.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-377">In the <strong>Create by</strong> field, select the user who is responsible for report creation.</span></span> <span data-ttu-id="b5fb4-378">Chcete-li zobrazit <strong>platební</strong> sestavu, která je vytvořená, použijte tlačítko <strong>Pokladní sestavy</strong> na stránce <strong>Pokladní účty</strong>.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-378">To view the <strong>Cash</strong> report that is created, use the <strong>Cash reports</strong> button on the <strong>Cash accounts</strong> page.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b5fb4-379">Hotovost – vyrovnání kurzových rozdílů FIFO a LIFO (pouze Polsko)</span><span class="sxs-lookup"><span data-stu-id="b5fb4-379">Cash - Exchange adjustment FIFO and LIFO (for Poland only)</span></span></td>
<td><span data-ttu-id="b5fb4-380">Vypočítejte úpravu směnného kurzu dle polské normy.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-380">Calculate the exchange adjustment per Polish standards.</span></span> <span data-ttu-id="b5fb4-381">Pomocí funkce <strong>filtr</strong> na kartě <strong>Záznamy pro zahrnutí</strong> zadejte platební účet, pro který chcete úlohu použít.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-381">Use the <strong>Filter</strong> function on the <strong>Records to include</strong> tab to specify the cash account to run the task for.</span></span> <span data-ttu-id="b5fb4-382">Zaškrtněte políčko <strong>Přepočet</strong>, chcete-li provést úplný přepočet rozdílu úpravy směnného kurzu pro všechna otevřená období.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-382">Select the <strong>Recalculation</strong> check box to do a full recalculation of the exchange adjustment difference for all open periods.</span></span> <span data-ttu-id="b5fb4-383">Zde je způsob úpravy kurzových rozdílů při použití metody FIFO a LIFO:</span><span class="sxs-lookup"><span data-stu-id="b5fb4-383">Here is how the exchange adjustment is calculated when the first in, first out (FIFO) and last in, first out (LIFO) methods are used:</span></span>
<ul>
<li><span data-ttu-id="b5fb4-384"><strong>Metoda FIFO</strong> – systém vyhledá výdajovou transakci, která má starší datum transakce (menší číslo objednávky) a vyrovná se s příjmovou transakcí, která má starší datum transakce (menší číslo objednávky).</span><span class="sxs-lookup"><span data-stu-id="b5fb4-384"><strong>FIFO method</strong> – The system searches for an expenditure transaction that has an earlier transaction date (smaller order number) and settles it with a receipt transaction that has an earlier transaction date (smaller order number).</span></span></li>
<li><span data-ttu-id="b5fb4-385"><strong>Metoda LIFO</strong> – systém vyhledá výdajovou transakci, která má pozdější datum transakce (větší číslo objednávky) a vyrovná se s příjmovou transakcí, která má pozdější datum transakce (větší číslo objednávky).</span><span class="sxs-lookup"><span data-stu-id="b5fb4-385"><strong>LIFO method</strong> – The system searches for an expenditure transaction that has a later transaction date (larger order number) and settles it with a receipt transaction that has a later transaction date (larger order number).</span></span></li>
</ul>
<span data-ttu-id="b5fb4-386">Vyrovnaná částka se projeví v poli <strong>Měna vyrovnání</strong> na stránce <strong>Platební transakce</strong>.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-386">The settled amount is reflected in the <strong>Settled currency</strong> field on the <strong>Cash transaction</strong> page.</span></span> <span data-ttu-id="b5fb4-387">Pokud existuje rozdíl v úpravě směnného kurzu, částka se projeví v poli <strong>Částka úpravy směnného kurzu</strong> a vygeneruje se typ dokumentu <strong>Rozdíl směnného kurzu</strong> v tabulce <strong>Platební transakce</strong>.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-387">If there is an exchange adjustment difference, the amount is reflected in the <strong>Exchange adjustment amount</strong> field, and a transaction of the <strong>Exchange rate difference</strong> document type is generated in the <strong>Cash transaction</strong> table.</span></span> <span data-ttu-id="b5fb4-388">Účty hlavní knihy pro transakce zisků a ztrát jsou nastaveny v tabulce <strong>Měna</strong> (<strong>finanční zisk</strong> a <strong>finanční ztráta směnného kurzu</strong>).</span><span class="sxs-lookup"><span data-stu-id="b5fb4-388">Ledger accounts for profit/loss transactions are set in the <strong>Currency</strong> table (<strong>Exchange rate financial profit</strong> and <strong>Exchange rate financial loss</strong>).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b5fb4-389">Přecenění cizí měny – hotovost</span><span class="sxs-lookup"><span data-stu-id="b5fb4-389">Foreign currency revaluation - Cash</span></span></td>
<td><span data-ttu-id="b5fb4-390">Použijte tento úkol pro zajištění dostatečného zůstatku ve výchozí měně v den vykazování, kdy jsou zadány operace v cizích měnách.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-390">Use this task to have an adequate balance in the default currency on the reporting date when the operations are entered in foreign currencies.</span></span> <span data-ttu-id="b5fb4-391">Pomocí funkce <strong>filtr</strong> na kartě <strong>Záznamy pro zahrnutí</strong> zadejte platební účet, pro který chcete úlohu použít.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-391">Use the <strong>Filter</strong> function on the <strong>Records to include</strong> tab to specify the cash account to run the task for.</span></span> <span data-ttu-id="b5fb4-392">V dialogovém okně pro úkol použijte pole <strong>Z měny</strong> a <strong>Na měnu</strong> polí k zadání měn transakce.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-392">In the dialog box for the task, use the <strong>From currency</strong> and <strong>To Currency</strong> fields to specify transaction currencies.</span></span> <span data-ttu-id="b5fb4-393">Systém porovná částky v měně, která byla převedena pomocí směnného kurzu ke zvolenému datu částku ve výchozí měně.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-393">The system compares the amount in the currency that was converted by using exchange rate on the selected date with the amount in the default currency.</span></span> <span data-ttu-id="b5fb4-394">Rozdíl mezi oběma částkami (s výjimkou předchozího vyrovnání kurzových rozdílů) je vypočítaný kurzový rozdíl.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-394">The difference between the two amounts (excluding the previous exchange adjustment) is the calculated exchange adjustment.</span></span> <span data-ttu-id="b5fb4-395">Tato úloha vytvoří schválenou platební transakci typu <strong>vyrovnání kurzových rozdílů</strong>.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-395">This task creates an approved cash transaction of the <strong>Exchange adjustment</strong> type.</span></span> <span data-ttu-id="b5fb4-396">Transakce hlavní knihy je vytvořena pomocí účtu hlavní knihy pro hotovost a účtu hlavní knihy, který je zadán v poli <strong>Nerealizovaný zisk</strong> nebo <strong>Nerealizovaná ztráta</strong> v tabulce <strong>Měna</strong>.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-396">The ledger transaction is formed by using the ledger account for cash and the ledger account that is specified in <strong>Unrealized profit</strong> or <strong>Unrealized loss</strong> in the <strong>Currency</strong> table.</span></span></td>
</tr>
</tbody>
</table>

## <a name="inquiries-and-reports"></a><span data-ttu-id="b5fb4-397">Dotazy a sestavy</span><span class="sxs-lookup"><span data-stu-id="b5fb4-397">Inquiries and reports</span></span>

| <span data-ttu-id="b5fb4-398">Dotaz nebo sestava</span><span class="sxs-lookup"><span data-stu-id="b5fb4-398">Inquiry or report</span></span>                             | <span data-ttu-id="b5fb4-399">popis</span><span class="sxs-lookup"><span data-stu-id="b5fb4-399">Description</span></span>                                                                                                                                                                                                                     |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5fb4-400">Zobrazení hotovostních transakcí</span><span class="sxs-lookup"><span data-stu-id="b5fb4-400">Cash transactions view</span></span>                        | <span data-ttu-id="b5fb4-401">Pro řádek listu deníku použijte tlačítko **dotazy** v podokně akcí k zobrazení transakcí hlavní knihy, zůstatek hotovosti a dalších informací.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-401">For a Slip journal line, use the **Inquiries** button on the Action Pane to view ledger transactions, the cash balance, and other information.</span></span>                                                                                  |
| <span data-ttu-id="b5fb4-402">Hotovostní transakce</span><span class="sxs-lookup"><span data-stu-id="b5fb4-402">Cash transaction</span></span>                              | <span data-ttu-id="b5fb4-403">Pokud chcete zobrazit platební transakce, přejděte na **řízení hotovosti a banky** &gt; **Dotazy a sestavy** &gt; **Platební transakce**.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-403">Go to **Cash and bank management** &gt; **Inquiries and reports** &gt; **Cash transactions** to view cash transactions.</span></span> <span data-ttu-id="b5fb4-404">Pomocí funkce **Filtr** na kartě Záznamy pro zahrnutí zadejte další kritéria omezující výběr hotovostních transakcí.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-404">Use the **Filter** function to specify additional criteria to limit the selection of cash transactions.</span></span> |
| <span data-ttu-id="b5fb4-405">Registrační deník (pro Estonsko, Rusko)</span><span class="sxs-lookup"><span data-stu-id="b5fb4-405">Journal of registration (for Estonia, Russia)</span></span> | <span data-ttu-id="b5fb4-406">Sestava v okně **řízení hotovosti a banky** &gt; **dotazy a sestavy** &gt; **deník registrace** odráží všechny hotovostní refundační a hotovostní výdajové doklady, které byly vydány.</span><span class="sxs-lookup"><span data-stu-id="b5fb4-406">The report at **Cash and bank management** &gt; **Inquiries and reports** &gt; **Journal of registration** reflects all cash reimbursement and cash disbursement slips that have been issued.</span></span>                                   |
| <span data-ttu-id="b5fb4-407">Pokladní kniha (pro Lotyšsko, Litvu, Rusko)</span><span class="sxs-lookup"><span data-stu-id="b5fb4-407">Cash book (for Latvia, Lithuania, Russia)</span></span>     | <span data-ttu-id="b5fb4-408">Sestava v okně **řízení hotovosti a banky** &gt; **dotazy a sestavy** &gt; **pokladní kniha sestavy** odráží skutečné peněžní fond pohyby (příjmy a výdaje).</span><span class="sxs-lookup"><span data-stu-id="b5fb4-408">The report at **Cash and bank management** &gt; **Inquiries and reports** &gt; **Cash book report** reflects actual cash fund movements (receipts and expenditures).</span></span>                                                            |





