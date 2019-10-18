---
title: Zpracování fakturace
description: Toto téma obsahuje informace o zpracování faktur pro východní Evropu.
author: v-kikozl
manager: AnnBe
ms.date: 07/21/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustParameters, VendParameters
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.author: v-kikozl
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 945b082528109f6f8c9292d2388749bebd4cfba4
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/27/2019
ms.locfileid: "2175687"
---
# <a name="invoice-processing"></a><span data-ttu-id="70726-103">Zpracování fakturace</span><span class="sxs-lookup"><span data-stu-id="70726-103">Invoice processing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="70726-104">Toto téma stručně popisuje některé scénáře specifické pro určité země, jako je například intrakomunitární daň z přidané hodnoty (DPH) a odložená daň.</span><span class="sxs-lookup"><span data-stu-id="70726-104">This topic briefly describes some country-specific scenarios, such as intra-community value-added tax (VAT) and deferred tax.</span></span> <span data-ttu-id="70726-105">Právní požadavky pro některé evropské země mají vliv na proces fakturace.</span><span class="sxs-lookup"><span data-stu-id="70726-105">Legal requirements for some European countries affect the invoicing process.</span></span> <span data-ttu-id="70726-106">Toto téma poskytuje také informace o zpracování faktur odběratelů a dodavatelů pro tyto země.</span><span class="sxs-lookup"><span data-stu-id="70726-106">This topic provides also an information about how customer and vendor invoices are processed for these countries.</span></span> 
<table>
<thead>
<tr>
<th><span data-ttu-id="70726-107">Scénář</span><span class="sxs-lookup"><span data-stu-id="70726-107">Scenario</span></span></th>
<th><span data-ttu-id="70726-108">Země</span><span class="sxs-lookup"><span data-stu-id="70726-108">Countries</span></span></th>
<th><span data-ttu-id="70726-109">Popis změn funkcí</span><span class="sxs-lookup"><span data-stu-id="70726-109">Description of the functionality changes</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="70726-110"> Data pohledávek a závazků pro DPH</span><span class="sxs-lookup"><span data-stu-id="70726-110">Accounts receivable and Accounts payable dates for VAT</span></span></td>
<td><span data-ttu-id="70726-111">Česká republika, Polsko</span><span class="sxs-lookup"><span data-stu-id="70726-111">Czech Republic, Poland</span></span></td>
<td>
<p><span data-ttu-id="70726-112">Při nákupu zboží ze zemí Evropské unie (EU) existuje povinnost vlastního vyměření DPH:</span><span class="sxs-lookup"><span data-stu-id="70726-112">When goods are purchased from European Union (EU) countries, there is an obligation of self-assessment of VAT:</span></span></p>
<ul>
<li><span data-ttu-id="70726-113">DPH na výstupu musí být zaplacena v období DPH, kdy byla vystavena faktura (datum dokumentu).</span><span class="sxs-lookup"><span data-stu-id="70726-113">The output VAT must be paid in a VAT period where the invoice was issued (document date).</span></span></li>
<li><span data-ttu-id="70726-114">DPH na vstupu nemůže být odečtena před přijetím dokumentu (datum registrace DPH).</span><span class="sxs-lookup"><span data-stu-id="70726-114">The input VAT can’t be deducted before the document receipt (VAT register date).</span></span></li>
</ul>
<p><span data-ttu-id="70726-115">Pro podporu tohoto scénáře musí být nakonfigurována následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="70726-115">The following settings should be configured to support this scenario:</span></span></p>
<ul>
<li><span data-ttu-id="70726-116">Na stránce <strong>Parametry závazků</strong> povolte parametry <strong>DPH intrakomunitárního plnění</strong> a <strong>Datum dokumentu pro intrakomunitární DPH</strong>.</span><span class="sxs-lookup"><span data-stu-id="70726-116">On the <strong>Accounts payable parameters</strong> page, enable the <strong>Intra-community VAT</strong> and <strong>Document date for intra-community VAT</strong> parameters.</span></span></li>
<li><span data-ttu-id="70726-117">Nastavte dva kódy daně z přidané hodnoty: jeden, který má kladné procento daně z přidané hodnoty, a druhý, který má záporné procento daně z přidané hodnoty.</span><span class="sxs-lookup"><span data-stu-id="70726-117">Set up two sales tax codes, one that has a positive sales tax percentage and one that has a negative sales tax percentage.</span></span></li>
<li><span data-ttu-id="70726-118">Nastavte skupinu daně z přidané hodnoty obsahující kladné i záporné kódy daně z přidané hodnoty.</span><span class="sxs-lookup"><span data-stu-id="70726-118">Set up a sales tax group that includes both the positive and negative sales tax codes.</span></span> <span data-ttu-id="70726-119">Pro záporný kód daně z přidané hodnoty nastavte parametr <strong>DPH intrakomunitárního plnění</strong> na <strong>Ano</strong>.</span><span class="sxs-lookup"><span data-stu-id="70726-119">For the negative sales tax code, set the <strong>Intracommunity VAT</strong> parameter to <strong>Yes</strong>.</span></span></li>
</ul>
<p><span data-ttu-id="70726-120">Po úspěšném nastavení budou mít nákupy dvě zaúčtované transakce DPH:</span><span class="sxs-lookup"><span data-stu-id="70726-120">After successful setup, purchases will have two posted sales tax transactions:</span></span></p>
<ul>
<li><span data-ttu-id="70726-121">Pozitivní transakci, která má charakter <strong>pohledávky DPH</strong>, a datum registrace DPH, které je shodné s datem stránky zaúčtování faktury.</span><span class="sxs-lookup"><span data-stu-id="70726-121">A positive transaction that has a direction of <strong>sales tax receivable</strong> and a VAT register date that equals the date from the invoice posting page.</span></span></li>
<li><span data-ttu-id="70726-122">Negativní transakci, která má charakter <strong>závazku DPH</strong>, a datum registrace DPH, které je shodné s datem dokumentu.</span><span class="sxs-lookup"><span data-stu-id="70726-122">A negative transaction that has a direction of <strong>sales tax payable</strong> and a VAT register date that equals the document date.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="70726-123">Změňte datum prodejního dokladu.</span><span class="sxs-lookup"><span data-stu-id="70726-123">Modify a sales document date.</span></span></td>
<td><span data-ttu-id="70726-124">Všechny východoevropské země</span><span class="sxs-lookup"><span data-stu-id="70726-124">All Eastern European countries</span></span></td>
<td><p><span data-ttu-id="70726-125">Můžete změnit pole <strong>Datum dokladu</strong> na projektové faktuře.</span><span class="sxs-lookup"><span data-stu-id="70726-125">You can modify the <strong>Document date</strong> field on a project invoice.</span></span> <span data-ttu-id="70726-126">Toto datum se zobrazuje na vytištěné faktuře.</span><span class="sxs-lookup"><span data-stu-id="70726-126">This date appears on the printed invoice.</span></span></p>
<p><span data-ttu-id="70726-127">Na stránkách <strong>Zaúčtování faktury</strong> a <strong>Volná faktura</strong> existuje pole <strong>Datum dokumentu</strong>.</span><span class="sxs-lookup"><span data-stu-id="70726-127">There is also a <strong>Document date</strong> field on the <strong>Posting invoice</strong> and <strong>Free text invoice</strong> pages.</span></span> <span data-ttu-id="70726-128">Po zaúčtování faktury se datum dokumentu zobrazí v záhlaví faktury.</span><span class="sxs-lookup"><span data-stu-id="70726-128">After you post an invoice, the document date appears on the invoice header.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="70726-129">Datum dokumentu pro směnné kurzy</span><span class="sxs-lookup"><span data-stu-id="70726-129">Document date for exchange rates</span></span></td>
<td><span data-ttu-id="70726-130">Polsko, Maďarsko, Česká republika,</span><span class="sxs-lookup"><span data-stu-id="70726-130">Poland, Hungary, Czech Republic</span></span></td>
<td>
<p><span data-ttu-id="70726-131">Legislativa obsahuje různá pravidla pro výběr platných směnných kurzů pro obchodní transakce.</span><span class="sxs-lookup"><span data-stu-id="70726-131">Legislation provides different rules for selecting valid exchange rates for business transactions.</span></span> <span data-ttu-id="70726-132">V poli <strong>Datum směnného kurzu</strong> na stránkách <strong>Parametry pohledávek</strong> a <strong>Parametry závazků</strong> můžete vybrat datum, které má být použito pro částky ve výpočtu zúčtovací měny na nákupních a prodejních dokumentech.</span><span class="sxs-lookup"><span data-stu-id="70726-132">In the <strong>Exchange rate date</strong> field on the <strong>Accounts receivable parameters</strong> and <strong>Accounts payable parameters</strong> pages, you can select the date that should be used for amounts in the accounting currency calculation on purchase and sales documents.</span></span> <span data-ttu-id="70726-133">Při zadávání dat systém načte směnný kurz pro transakci na základě tohoto parametru.</span><span class="sxs-lookup"><span data-stu-id="70726-133">During data entry, the system retrieves the exchange rate for the transaction, based on this parameter.</span></span></p>
<blockquote>[!NOTE]<br><span data-ttu-id="70726-134">Když nastavíte pole <strong>Datum směnného kurzu</strong> na <strong>Datum dokumentu (pouze pro obchod EU)</strong>, systém použije skupinu DPH.</span><span class="sxs-lookup"><span data-stu-id="70726-134">When you set the <strong>Exchange rate date</strong> field to <strong>Document date (for EU trade only)</strong>, the system uses the sales tax group.</span></span> <span data-ttu-id="70726-135">Pro skupinu DPH existuje parametr <strong>Obchod EU</strong> na kartě <strong>Hlavní</strong>. Pokud je možnost <strong>Obchod EU</strong> nastavena na <strong>Ano</strong> pro skupinu DPH a pokud je tato skupina DPH v záhlaví dokumentu, systém načte směnný kurz, který je založený na datu dokumentu.</span><span class="sxs-lookup"><span data-stu-id="70726-135">For the sales tax group, there is a <strong>EU trade</strong> parameter on the <strong>General</strong> tab. If the <strong>EU trade</strong> option is set to <strong>Yes</strong> for the sales tax group, and if this sales tax group exists on the header of the document, the system retrieves the exchange rate based on the document date.</span></span> <span data-ttu-id="70726-136">Pokud je možnost <strong>Obchod EU</strong> nastavena na <strong>Ne</strong> pro tuto skupinu DPH, systém načte směnný kurz podle data zaúčtování dokladu.</span><span class="sxs-lookup"><span data-stu-id="70726-136">If the <strong>EU trade</strong> option is set to <strong>No</strong> for this sales tax group, the system retrieves the exchange rate based on the posting date of the document.</span></span></blockquote>
</td>
</tr>
<tr>
<td><span data-ttu-id="70726-137">Data obchodů, data registrace DPH a dokument a kontrol dat DPH</span><span class="sxs-lookup"><span data-stu-id="70726-137">Trade dates, VAT register dates, and document and VAT date control</span></span></td>
<td><span data-ttu-id="70726-138">Polsko, Maďarsko, Česká republika,</span><span class="sxs-lookup"><span data-stu-id="70726-138">Poland, Hungary, Czech Republic</span></span></td>
<td>
<p><span data-ttu-id="70726-139">Datum prodeje a datum příjmu dokumentu jsou povinné pro vykazování DPH:</span><span class="sxs-lookup"><span data-stu-id="70726-139">The sales date and the document receipt date are required for VAT reporting:</span></span></p>
<ul>
<li><span data-ttu-id="70726-140">Datum prodeje je datum plnění transakce v pohledávkách.</span><span class="sxs-lookup"><span data-stu-id="70726-140">The sales date is the fulfilment date of the transaction in Accounts receivable.</span></span></li>
<li><span data-ttu-id="70726-141">Datum příjmu dokumentů je datum dokazující práva nárokovat odpočet DPH v závazcích.</span><span class="sxs-lookup"><span data-stu-id="70726-141">The document receipt date is a date that demonstrates the rights to claim a VAT deduction in Accounts payable.</span></span> <span data-ttu-id="70726-142">Každý dokument, který je přijat, obsahuje datum pro účely auditu.</span><span class="sxs-lookup"><span data-stu-id="70726-142">Each document that is received has a date for audit purposes.</span></span></li>
</ul>
<p><span data-ttu-id="70726-143">Maďarská funkce pro termíny dat, česká funkce pro data plnění a polská funkce pro datum registrace DPH obsahují požadavek na vykazování informace o dani, která je založena na datu lišícím se od data zaúčtování.</span><span class="sxs-lookup"><span data-stu-id="70726-143">The Hungarian functionality for date deadlines, the Czech Republic functionality for fulfill dates, and the Polish functionality for the VAT register date include the requirement for tax information reporting that is based on a date that differs from the posting date.</span></span></p>
<p><span data-ttu-id="70726-144">Pole <strong>Datum registrace DPH</strong> podporuje tento požadavek a zobrazuje se na více než 20 stránkách.</span><span class="sxs-lookup"><span data-stu-id="70726-144">The <strong>Date of VAT register</strong> field supports this requirement and appears on more than 20 pages.</span></span> <span data-ttu-id="70726-145">Tyto stránky obsahují deníky, prodejní objednávky, nákupní objednávky, volné faktury, deníky faktur dodavatele a projektové faktury.</span><span class="sxs-lookup"><span data-stu-id="70726-145">These pages include journals, sales orders, purchase orders, free-text invoices, vendor invoice journals, and project invoices.</span></span> <span data-ttu-id="70726-146">Když aktualizujete nebo zaúčtujete dokumenty, všechny daně se zaúčtují pomocí příslušného data registrace DPH a toto datum bude obsaženo na stránkách, jako jsou například stránky deníků faktur odběratele a dodavatele.</span><span class="sxs-lookup"><span data-stu-id="70726-146">When you update or post the documents, all taxes are posted by using the corresponding date of the VAT register, and the date is included on pages such as the customer and vendor invoice journals pages.</span></span></p>
<p><span data-ttu-id="70726-147">Konkrétně pro Českou republiku pole <strong>Datum registrace DPH</strong> může být ponecháno při zaúčtování prázdné, v případě zaúčtování odložené DPH.</span><span class="sxs-lookup"><span data-stu-id="70726-147">Specifically, for the Czech Republic, the <strong>VAT register date</strong> field can be blank during posting, in the event of postponed VAT posting.</span></span> <span data-ttu-id="70726-148">V opačném případě je toto pole povinné a musí být vyplněno.</span><span class="sxs-lookup"><span data-stu-id="70726-148">Otherwise, the field is mandatory and must be filled in.</span></span></p>
<p><span data-ttu-id="70726-149">Lze nastavit parametry ověření data na stránce <strong>Skupiny DPH</strong>:</span><span class="sxs-lookup"><span data-stu-id="70726-149">Date validation parameters can be set on the <strong>Sales tax groups</strong> page:</span></span></p>
<ul>
<li><span data-ttu-id="70726-150">Parametry <strong>Datum vyplnění registrace DPH</strong> a <strong>Vyplnění data prodeje</strong> se používají jako výchozí metoda pro vyplnění příslušných dat.</span><span class="sxs-lookup"><span data-stu-id="70726-150">The <strong>Date of VAT register filling</strong> and <strong>Sales date filling</strong> parameters are used as a default filling method for appropriate dates.</span></span> <span data-ttu-id="70726-151">K dispozici je rovněž ruční zadání a několik metod automatizovaného zadání.</span><span class="sxs-lookup"><span data-stu-id="70726-151">Manual input and several automated input methods are also available.</span></span></li>
<li><span data-ttu-id="70726-152">Pole <strong>Povinné datum prodeje</strong> udává, zda je nutné zadat datum prodeje před zaúčtování prodejní faktury.</span><span class="sxs-lookup"><span data-stu-id="70726-152">The <strong>Mandatory sales date</strong> field indicates whether the sales date must be entered before a sales invoice is posted.</span></span></li>
</ul>
<p><span data-ttu-id="70726-153">Na stránce <strong>Transakce registru DPH</strong> můžete vyplnit prázdná data pro registr DPH pro zaúčtované daňové transakce.</span><span class="sxs-lookup"><span data-stu-id="70726-153">On the <strong>VAT Register transactions</strong> page, you can fill in blank dates for the VAT register for posted tax transactions.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="70726-154">Data registrace DPH, která zahrnují odloženou daň</span><span class="sxs-lookup"><span data-stu-id="70726-154">VAT register dates that include deferred tax</span></span></td>
<td><span data-ttu-id="70726-155">Maďarsko</span><span class="sxs-lookup"><span data-stu-id="70726-155">Hungary</span></span></td>
<td>
<p><span data-ttu-id="70726-156">Maďarské daňové předpisy vyžadují, aby faktury byly vytvářeny buď v okamžiku plnění nebo ne později než 15 dnů po plnění.</span><span class="sxs-lookup"><span data-stu-id="70726-156">Hungary tax regulations require that invoices be created at either the time of fulfilment or no later than 15 days after fulfilment.</span></span></p>
<p><span data-ttu-id="70726-157">Datum plnění je buď datum, kdy byly poskytnuty objednané služby, nebo datum, kdy byly dodány objednané položky.</span><span class="sxs-lookup"><span data-stu-id="70726-157">The fulfilment date is either the date when the ordered services were provided or the date when ordered items were delivered.</span></span> <span data-ttu-id="70726-158">Při aktualizaci nebo zaúčtování dokladů se zaúčtují všechny daně s použitím odpovídajícího data registrace DPH a toto datum se zobrazí na příslušných stránkách.</span><span class="sxs-lookup"><span data-stu-id="70726-158">When you update or post the documents, all taxes are posted by using the corresponding date of the VAT register, and the date appears on relevant pages.</span></span> <span data-ttu-id="70726-159">Dále právní předpisy vyžadují, aby DPH při souvislých dodávkách služeb, jako je například pronájem, leasing, konzultace a topení, splňovalo následující kritéria:</span><span class="sxs-lookup"><span data-stu-id="70726-159">Additionally, regulations require that VAT on continuous delivery of services, such as renting, leasing, consulting, and heating, meet the following criteria:</span></span></p>
<ul>
<li><span data-ttu-id="70726-160">DPH musí být zaúčtováno na vyhrazený účet hlavní knihy v datum fakturace.</span><span class="sxs-lookup"><span data-stu-id="70726-160">VAT must be posted to a dedicated general ledger account on the invoice date.</span></span></li>
<li><span data-ttu-id="70726-161">DPH je nutné převést ze speciálních účtů na účet pohledávek DPH nebo na účet závazků a musí být zahrnuto do sestavy DPH v den splatnosti.</span><span class="sxs-lookup"><span data-stu-id="70726-161">VAT must be transferred from the special accounts to a sales tax receivable account or a payable account, and must be included in the VAT report on the due date.</span></span></li>
</ul>
<p><span data-ttu-id="70726-162">Abyste splnili tyto požadavky, můžete převést zaúčtování do hlavní knihy na účet odložené příchozí daně a účet odchozí odložené daně.</span><span class="sxs-lookup"><span data-stu-id="70726-162">To support these requirements, you can transfer General ledger postings to the Deferred incoming tax account and the Deferred outgoing tax account.</span></span> <span data-ttu-id="70726-163">Musíte však nejprve dokončit následující předpoklady:</span><span class="sxs-lookup"><span data-stu-id="70726-163">However, you must first complete the following prerequisites:</span></span></p>
<ul>
<li><span data-ttu-id="70726-164">Nastavte účty hlavní knihy pro odložené DPH závazky a pohledávky ve skupinách zaúčtování hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="70726-164">Set up the Deferred VAT Payable and Deferred VAT Receivable ledger accounts in ledger posting groups.</span></span></li>
<li><span data-ttu-id="70726-165">Povolte parametr <strong>Odložená DPH</strong> pro skupiny DPH položky.</span><span class="sxs-lookup"><span data-stu-id="70726-165">Enable the <strong>Deferred VAT</strong> parameter for item sales tax groups.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="70726-166"> Povinné datum DPH</span><span class="sxs-lookup"><span data-stu-id="70726-166">Mandatory VAT date</span></span></td>
<td><span data-ttu-id="70726-167">Polsko</span><span class="sxs-lookup"><span data-stu-id="70726-167">Poland</span></span></td>
<td>
<p><span data-ttu-id="70726-168">Můžete vyžadovat, aby datum registrace DPH bylo zahrnuto do záznamů transakcí nákupu a prodeje.</span><span class="sxs-lookup"><span data-stu-id="70726-168">You can require that the date of the VAT register be included in purchase and sales transaction records.</span></span> <span data-ttu-id="70726-169">Datum registrace DPH lze tedy zaznamenat před zaúčtováním transakce.</span><span class="sxs-lookup"><span data-stu-id="70726-169">Therefore, the date of the VAT register can be captured before a transaction is posted.</span></span> <span data-ttu-id="70726-170">Tato funkce umožňuje, že nemusíte pracovat s více transakcemi na konci období.</span><span class="sxs-lookup"><span data-stu-id="70726-170">This functionality helps you avoid having to handle multiple transactions at the end of the period.</span></span></p>
<p><span data-ttu-id="70726-171">Můžete nastavit pole <strong>Datum registrace DPH</strong> jako povinné při zaúčtování transakcí odběratele nebo dodavatele.</span><span class="sxs-lookup"><span data-stu-id="70726-171">You can make the <strong>Date of VAT register</strong> field mandatory when customer or vendor transactions are posted.</span></span> <span data-ttu-id="70726-172">Chcete-li tak učinit, povolte možnost <strong>Datum DPH je požadováno</strong> pro související účet odběratele nebo dodavatele.</span><span class="sxs-lookup"><span data-stu-id="70726-172">To make this field mandatory, enable the <strong>VAT date is required</strong> option for the related customer or vendor account.</span></span></p>
</td>
</tr>
</tbody>
</table>
