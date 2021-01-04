---
title: Přehled konfigurace závazků
description: Tento článek popisuje stránky, které slouží k nastavení základních a volitelných funkcí pro modul Závazky. Dále popisuje postup nastavení, který musíte dokončit dříve, než začnete nastavovat modul Závazky.
author: abruer
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankAccountTable, DeliveryMode, PaymTerm, VendGroup, VendParameters, VendPaymMode, VendTable, DeliveryReason, DeliveryTerms, DestinationCode
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 24671
ms.assetid: 82561fe7-b2d6-464c-9347-79d0ce0f9743
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5eed11cbe73ede71cabf83655fc1d37b1a979a4c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441243"
---
# <a name="configure-accounts-payable-overview"></a><span data-ttu-id="6ecad-104">Přehled konfigurace závazků</span><span class="sxs-lookup"><span data-stu-id="6ecad-104">Configure Accounts payable overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6ecad-105">Tento článek popisuje stránky, které slouží k nastavení základních a volitelných funkcí pro modul Závazky.</span><span class="sxs-lookup"><span data-stu-id="6ecad-105">This article describes the pages that you use to set up basic and optional functionality for Accounts payable.</span></span> <span data-ttu-id="6ecad-106">Dále popisuje postup nastavení, který musíte dokončit dříve, než začnete nastavovat modul Závazky.</span><span class="sxs-lookup"><span data-stu-id="6ecad-106">It also describes setup steps that you must complete before you start to set up Accounts payable.</span></span>

<a name="prerequisites-for-accounts-payable-setup"></a><span data-ttu-id="6ecad-107">Předpoklady k nastavení modulu Závazky</span><span class="sxs-lookup"><span data-stu-id="6ecad-107">Prerequisites for Accounts payable setup</span></span>
----------------------------------------

<span data-ttu-id="6ecad-108">Před nastavením modulu Závazky je nutné provést tyto úkoly:</span><span class="sxs-lookup"><span data-stu-id="6ecad-108">Before you can set up Accounts payable, you must complete the following setup:</span></span>

-   <span data-ttu-id="6ecad-109">V hlavní knize:</span><span class="sxs-lookup"><span data-stu-id="6ecad-109">In General ledger:</span></span>
    -   <span data-ttu-id="6ecad-110">Máte-li v úmyslu používat deníky plateb, nastavte je.</span><span class="sxs-lookup"><span data-stu-id="6ecad-110">If you plan to use payment journals, set up payment journals.</span></span>
    -   <span data-ttu-id="6ecad-111">Pokud máte v úmyslu spouštět vyrovnání kurzových rozdílů, na stránce Měny nastavte kódy měn, na stránce Typy směnného kurzu nastavte typy směnných kurzů a na stránce Směnné kurzy měn nastavte směnné kurzy měn.</span><span class="sxs-lookup"><span data-stu-id="6ecad-111">If you plan to run exchange rate adjustments, set up currency codes on the Currencies page, set up exchange rate types on the Exchange rate types page, and set up currency exchange rates on the Currency exchange rates page.</span></span>
-   <span data-ttu-id="6ecad-112">V modulu Pokladna a banka nastavte bankovní účty, které se mají používat pro metody platby.</span><span class="sxs-lookup"><span data-stu-id="6ecad-112">In Cash and bank management, set up bank accounts to use with methods of payment.</span></span>

## <a name="setup-pages-for-accounts-payable"></a><span data-ttu-id="6ecad-113">Stránky k nastavení modulu Závazky</span><span class="sxs-lookup"><span data-stu-id="6ecad-113">Setup pages for Accounts payable</span></span>

<span data-ttu-id="6ecad-114">Následující stránky slouží k nastavení základních funkcí modulu Závazky pro jednotlivé právní osoby.</span><span class="sxs-lookup"><span data-stu-id="6ecad-114">Use the following pages to set up the basic functionality of Accounts payable for each legal entity.</span></span> <span data-ttu-id="6ecad-115">Stránky jsou uvedeny v doporučeném pořadí nastavení.</span><span class="sxs-lookup"><span data-stu-id="6ecad-115">The pages are listed in the recommended order of setup.</span></span> <span data-ttu-id="6ecad-116">Pro zjednodušení procesu nastavení si můžete z prvních vytvořených záznamů vytvořit šablony.</span><span class="sxs-lookup"><span data-stu-id="6ecad-116">To make the setup process easier, you can create templates from the first records that you create.</span></span> <span data-ttu-id="6ecad-117">Šablona obvykle obsahuje hodnoty pro velký počet polí, které odpovídají funkcím, jež chce organizace implementovat pro určitý typ dodavatelů.</span><span class="sxs-lookup"><span data-stu-id="6ecad-117">In a template, values are typically entered in many fields to reflect the features that the organization wants to implement for a particular type of vendor.</span></span>
1.  <span data-ttu-id="6ecad-118">Stránka Platební podmínky slouží k určení platebních podmínek, které chcete přiřadit prodejním objednávkám, nákupním objednávkám, odběratelům a dodavatelům a které určují data splatnosti faktur.</span><span class="sxs-lookup"><span data-stu-id="6ecad-118">On the Terms of payment page, define the terms of payment that you assign to sales orders, purchase orders, customers, and vendors, and that determine invoice due dates.</span></span> <span data-ttu-id="6ecad-119">Další informace naleznete v tématu [Definování platebních poplatků dodavatele](tasks/define-vendor-payment-fees.md).</span><span class="sxs-lookup"><span data-stu-id="6ecad-119">For more information, see [Define vendor payment fees](tasks/define-vendor-payment-fees.md).</span></span>
2.  <span data-ttu-id="6ecad-120">Stránka Způsob platby – dodavatelé slouží k vytvoření a správě informací o tom, jak organizace platí svým dodavatelům.</span><span class="sxs-lookup"><span data-stu-id="6ecad-120">On the Methods of payment - vendors page, create and maintain information about how the organization pays its vendors.</span></span>
3.  <span data-ttu-id="6ecad-121">Stránka Skupiny dodavatelů slouží k vytváření a údržbě skupin dodavatelů se společnými důležitými parametry pro účtování, vyrovnávání, platby, vykazování a prognózy.</span><span class="sxs-lookup"><span data-stu-id="6ecad-121">On the Vendor groups page, create and maintain groups of vendors that share important parameters for posting, settlement and payment, reporting, and forecasting.</span></span>
4.  <span data-ttu-id="6ecad-122">Stránka Účetní profily dodavatele slouží k určení toho, jak jsou transakce dodavatelů zaúčtovány do hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="6ecad-122">On the Vendor posting profiles page, define how vendor transactions are posted to the general ledger.</span></span>
5.  <span data-ttu-id="6ecad-123">Stránka Parametry závazků slouží k nastavení výchozích parametrů používaných v případě, že pro modul Závazky není zadáno specifičtější nastavení, parametry různých typů funkcí a různé číselné řady.</span><span class="sxs-lookup"><span data-stu-id="6ecad-123">On the Accounts payable parameters page, set up default settings that are applied if a more specific setting isn't specified, parameters for various kinds of functionality, and the various number sequences for Accounts payable.</span></span>
6.  <span data-ttu-id="6ecad-124">Stránka Nastavení formuláře slouží k určení formátu různých dokumentů souvisejících s dodavateli, které organizace používá ke sledování příjemek od dodavatelů a k zadávání důvodů pro toky plateb k dodavatelům.</span><span class="sxs-lookup"><span data-stu-id="6ecad-124">On the Form setup page, define the format of various documents that are related to vendors, and that the organization uses to keep track of receipts from vendors and enter reasons for the flow of payments to vendors.</span></span>
7.  <span data-ttu-id="6ecad-125">Stránka Dodavatelé slouží k vytváření a údržbě účtů dodavatelů a také finančních úřadů, jimž vaše organizace odevzdává výkazy DPH.</span><span class="sxs-lookup"><span data-stu-id="6ecad-125">On the Vendors page, create and maintain vendor accounts, and also the tax authorities that your organization reports sales taxes to.</span></span>

## <a name="optional-setup-pages-for-accounts-payable"></a><span data-ttu-id="6ecad-126">Volitelné stránky pro nastavení závazků</span><span class="sxs-lookup"><span data-stu-id="6ecad-126">Optional setup pages for Accounts payable</span></span>
<span data-ttu-id="6ecad-127">Kromě základních funkcí má modul Závazky další funkce, které lze nastavit.</span><span class="sxs-lookup"><span data-stu-id="6ecad-127">In addition to the basic functionality, Accounts payable has other functionality that you can set up.</span></span>

<span data-ttu-id="6ecad-128">Další stránky pro nastavení jsou uspořádány podle funkcí.</span><span class="sxs-lookup"><span data-stu-id="6ecad-128">The additional setup pages are organized by functionality.</span></span>

<span data-ttu-id="6ecad-129">**Zásady**</span><span class="sxs-lookup"><span data-stu-id="6ecad-129">**Policies**</span></span>
-   <span data-ttu-id="6ecad-130">Stránka Zásada faktur dodavatele slouží k nastavení zásad pro faktury dodavatele.</span><span class="sxs-lookup"><span data-stu-id="6ecad-130">On the Vendor invoice policy page, set up vendor invoice policies.</span></span>

<span data-ttu-id="6ecad-131">**Párování faktur**</span><span class="sxs-lookup"><span data-stu-id="6ecad-131">**Invoice matching**</span></span>

-   <span data-ttu-id="6ecad-132">Stránka Tolerance součtu faktur slouží k nastavení tolerancí pro celkové hodnoty faktur.</span><span class="sxs-lookup"><span data-stu-id="6ecad-132">On the Invoice totals tolerances page, set up tolerances for invoice totals.</span></span>
-   <span data-ttu-id="6ecad-133">Stránka Zásady párování slouží k nastavení zásad dvoucestného a třícestného párování.</span><span class="sxs-lookup"><span data-stu-id="6ecad-133">On the Matching policy page, set up two-way and three-way matching policies.</span></span>
-   <span data-ttu-id="6ecad-134">Stránka Tolerance ceny slouží k nastavení tolerance pro jednotkové ceny.</span><span class="sxs-lookup"><span data-stu-id="6ecad-134">On the Price tolerances page, set up tolerances for unit prices.</span></span>
-   <span data-ttu-id="6ecad-135">Stránka Skupiny tolerance ceny položky slouží k nastavení skupin tolerancí pro ceny položky.</span><span class="sxs-lookup"><span data-stu-id="6ecad-135">On the Item price tolerance groups page, set up tolerance groups for item prices.</span></span>
-   <span data-ttu-id="6ecad-136">Stránka Skupiny tolerance ceny dodavatele slouží k nastavení skupin tolerancí pro ceny dodavatele.</span><span class="sxs-lookup"><span data-stu-id="6ecad-136">On the Vendor price tolerance groups page, set up  tolerance groups for vendor prices.</span></span>
-   <span data-ttu-id="6ecad-137">Stránka Tolerance nákladů slouží k nastavení tolerance pro náklady.</span><span class="sxs-lookup"><span data-stu-id="6ecad-137">On the Charges tolerances page, set up tolerances for charges.</span></span>

<span data-ttu-id="6ecad-138">**Workflow**</span><span class="sxs-lookup"><span data-stu-id="6ecad-138">**Workflow**</span></span>

-   <span data-ttu-id="6ecad-139">Stránka Workflowy závazků slouží k úpravě konfigurace workflowu pro schvalování deníků a nákupních žádanek.</span><span class="sxs-lookup"><span data-stu-id="6ecad-139">On the Accounts payable workflows page, set up workflow configurations for journal approvals and purchase requisitions.</span></span>

<span data-ttu-id="6ecad-140">**Důvody**</span><span class="sxs-lookup"><span data-stu-id="6ecad-140">**Reasons**</span></span>

-   <span data-ttu-id="6ecad-141">Stránka Dodavatel – důvody slouží k nastavení kódů důvodů.</span><span class="sxs-lookup"><span data-stu-id="6ecad-141">On the Vendor reasons page, set up reason codes.</span></span>

<span data-ttu-id="6ecad-142">**Poplatky**</span><span class="sxs-lookup"><span data-stu-id="6ecad-142">**Charges**</span></span>

-   <span data-ttu-id="6ecad-143">Stránka Kód nákladů slouží k nastavení kódů pro náklady, které se používají v nákupních objednávkách.</span><span class="sxs-lookup"><span data-stu-id="6ecad-143">On the Charges code page, set up codes for the charges that are used in purchase orders.</span></span>
-   <span data-ttu-id="6ecad-144">Stránka Skupina nákladů dodavatele slouží k vytvoření a správě skupin nákladů pro dodavatele.</span><span class="sxs-lookup"><span data-stu-id="6ecad-144">On the Vendor charges group page, create and maintain charges groups for vendors.</span></span>
-   <span data-ttu-id="6ecad-145">Stránka Skupiny nákladů zboží slouží k vytváření a správě skupin nákladů pro položky..</span><span class="sxs-lookup"><span data-stu-id="6ecad-145">On the Item charge groups page, create and maintain charges groups for items.</span></span>
-   <span data-ttu-id="6ecad-146">Stránka Automatické doprovodné náklady slouží k určení nákladů, které jsou automaticky přiřazeny k objednávkám.</span><span class="sxs-lookup"><span data-stu-id="6ecad-146">On the Auto charges page, define the charges that are automatically assigned to orders.</span></span>

<span data-ttu-id="6ecad-147">**Doplňkové položky**</span><span class="sxs-lookup"><span data-stu-id="6ecad-147">**Supplementary items**</span></span>

-   <span data-ttu-id="6ecad-148">Stránka Skupiny doplňkových položek – dodavatel slouží k vytváření a správě skupin doplňkových položek pro dodavatele.</span><span class="sxs-lookup"><span data-stu-id="6ecad-148">On the Supplementary item groups - Vendor page, create and maintain supplementary item groups for vendors.</span></span>
-   <span data-ttu-id="6ecad-149">Stránka Skupiny doplňkových položek – zásoby slouží k vytváření a správě skupin doplňkových položek pro položky.</span><span class="sxs-lookup"><span data-stu-id="6ecad-149">On the Supplementary item groups - Inventory page, create and maintain supplementary item groups for items.</span></span>

<span data-ttu-id="6ecad-150">**Distribuce**</span><span class="sxs-lookup"><span data-stu-id="6ecad-150">**Distribution**</span></span>

-   <span data-ttu-id="6ecad-151">Stránka Dodací podmínky slouží k vytvoření a správě podmínek pro převod položky od prodávajícího ke kupujícímu.</span><span class="sxs-lookup"><span data-stu-id="6ecad-151">On the Terms of delivery page, create and maintain the conditions for an item's transfer from seller to buyer.</span></span>
-   <span data-ttu-id="6ecad-152">Stránka Způsoby dodání slouží k vytváření a správě způsobů přepravy, které se používají při doručování objednávky od prodávajícího ke kupujícímu.</span><span class="sxs-lookup"><span data-stu-id="6ecad-152">On the Modes of delivery page, create and maintain the methods of transport that are used when an order is delivered from the seller to the buyer.</span></span>
-   <span data-ttu-id="6ecad-153">Stránka Kódy místa určení slouží k vytváření a správě identifikátorů a popisů míst určení.</span><span class="sxs-lookup"><span data-stu-id="6ecad-153">On the Destination codes page, create and maintain identifiers and descriptions for delivery destinations.</span></span>

<span data-ttu-id="6ecad-154">**Formuláře**</span><span class="sxs-lookup"><span data-stu-id="6ecad-154">**Forms**</span></span>

-   <span data-ttu-id="6ecad-155">Stránka Poznámky na formulářích slouží k vytváření a správě standardního textu, který se zobrazuje na různých stránkách.</span><span class="sxs-lookup"><span data-stu-id="6ecad-155">On the Form notes page, create the standard text that appears on various pages.</span></span>
-   <span data-ttu-id="6ecad-156">Stránka Parametry třídění formuláře slouží k nastavení pořadí řazení požadavků, příjemek, dodacích listů a faktur.</span><span class="sxs-lookup"><span data-stu-id="6ecad-156">On the Form sorting parameters page, set up the sorting order for requisitions, receipt lists, packing slips, and invoices.</span></span>
-   <span data-ttu-id="6ecad-157">Stránka Nastavení správy tisku slouží k nastavení informací správy tisku pro originály a kopie stránek.</span><span class="sxs-lookup"><span data-stu-id="6ecad-157">On the Print management setup page, set up print management information for originals and copies of pages.</span></span>

<span data-ttu-id="6ecad-158">**Platby**</span><span class="sxs-lookup"><span data-stu-id="6ecad-158">**Payments**</span></span>

-   <span data-ttu-id="6ecad-159">Stránka Platební slevy slouží k nastavení a správě podmínek pro získání platebních slev.</span><span class="sxs-lookup"><span data-stu-id="6ecad-159">On the Cash discounts page, set up and manage the terms for obtaining cash discounts.</span></span> <span data-ttu-id="6ecad-160">Kódy platebních slev jsou propojeny s dodavateli a použity v nákupních objednávkách.</span><span class="sxs-lookup"><span data-stu-id="6ecad-160">The cash discount codes are linked to vendors and are applied to purchase orders.</span></span>
-   <span data-ttu-id="6ecad-161">Stránka Platební kalendáře slouží k nastavení platebních kalendářů, které se používají ke správě splátkových plateb dodavatelům.</span><span class="sxs-lookup"><span data-stu-id="6ecad-161">On the Payment schedules page, set up the payment schedules that are used to manage installment payments to vendors.</span></span>
-   <span data-ttu-id="6ecad-162">Stránka Dny platby slouží k určení dnů platby, které se používají k výpočtu dat splatnosti, a k určení dnů platby pro určité dny v týdnu nebo měsíci.</span><span class="sxs-lookup"><span data-stu-id="6ecad-162">On the Payment days page, define the payment days that are used to calculate due dates, and specify payment days for a specific day of the week or month.</span></span>
-   <span data-ttu-id="6ecad-163">Stránka Platební poplatek slouží k vytváření a správě platebních poplatků přiřazených k dodavatelům.</span><span class="sxs-lookup"><span data-stu-id="6ecad-163">On the Payment fee page, create and maintain the payment fees that are associated with vendors.</span></span>
-   <span data-ttu-id="6ecad-164">Stránka Platební instrukce slouží k vytváření a správě platebních instrukcí.</span><span class="sxs-lookup"><span data-stu-id="6ecad-164">On the Payment instruction page, create and maintain payment instructions.</span></span>

<span data-ttu-id="6ecad-165">**Statistika**</span><span class="sxs-lookup"><span data-stu-id="6ecad-165">**Statistics**</span></span>

-   <span data-ttu-id="6ecad-166">Stránka Definice období pro sledování splatnosti slouží k nastavení uživatelem definovaných intervalů, které se používají pro analýzu rozložení splatnosti dodavatelských účtů.</span><span class="sxs-lookup"><span data-stu-id="6ecad-166">On the Aging period definitions page, set up user-defined intervals that are used to analyze the maturity distribution of vendor accounts.</span></span>
-   <span data-ttu-id="6ecad-167">Stránka Odvětví obchodu slouží k vytváření kódů odvětví obchodu (LOB), které jsou přiřazeny k dodavatelům.</span><span class="sxs-lookup"><span data-stu-id="6ecad-167">On the Line of business page, create the line of business (LOB) codes that are assigned to vendors.</span></span>

<span data-ttu-id="6ecad-168">**Daň 1099**</span><span class="sxs-lookup"><span data-stu-id="6ecad-168">**Tax 1099**</span></span>

-   <span data-ttu-id="6ecad-169">Stránka **Pole 1099** slouží k ověření a aktualizaci minimálních částek, které musí být ohlášeny finančnímu úřadu IRS (Internal Revenue Service) v souladu s nejnovějšími požadavky tohoto úřadu.</span><span class="sxs-lookup"><span data-stu-id="6ecad-169">On the **1099 fields** page, verify and update the minimum amounts that must be reported to the Internal Revenue Service (IRS), based on the latest IRS requirements.</span></span>

## <a name="optional-setup-for-other-modules"></a><span data-ttu-id="6ecad-170">**Volitelné nastavení pro jiné moduly**</span><span class="sxs-lookup"><span data-stu-id="6ecad-170">**Optional setup for other modules**</span></span>
<span data-ttu-id="6ecad-171">**Správa organizace**</span><span class="sxs-lookup"><span data-stu-id="6ecad-171">**Organization administration**</span></span>

-   <span data-ttu-id="6ecad-172">Stránka Číselné řady slouží k nastavení skupin číselných řad pro čísla faktur.</span><span class="sxs-lookup"><span data-stu-id="6ecad-172">On the Number sequences page, set up number sequence groups for invoice numbers.</span></span>
-   <span data-ttu-id="6ecad-173">Na následujících stránkách nastavíte informace o adrese:</span><span class="sxs-lookup"><span data-stu-id="6ecad-173">On the following pages, set up address information:</span></span>
    -   <span data-ttu-id="6ecad-174">Nastavení adresy</span><span class="sxs-lookup"><span data-stu-id="6ecad-174">Address setup</span></span>
    -   <span data-ttu-id="6ecad-175">Kódy NAF</span><span class="sxs-lookup"><span data-stu-id="6ecad-175">NAF codes</span></span>
    -   <span data-ttu-id="6ecad-176">Importovat PSČ</span><span class="sxs-lookup"><span data-stu-id="6ecad-176">Import ZIP/postal codes</span></span>

<span data-ttu-id="6ecad-177">**Hlavní kniha**</span><span class="sxs-lookup"><span data-stu-id="6ecad-177">**General ledger**</span></span>

-   <span data-ttu-id="6ecad-178">Stránka Finanční dimenze slouží k nastavení finančních dimenzí.</span><span class="sxs-lookup"><span data-stu-id="6ecad-178">On the Financial dimensions page, set up financial dimensions.</span></span>
-   <span data-ttu-id="6ecad-179">Na následujících stránkách nastavíte informace o daních:</span><span class="sxs-lookup"><span data-stu-id="6ecad-179">On the following pages, set up tax information:</span></span>
    -   <span data-ttu-id="6ecad-180">Kódy DPH</span><span class="sxs-lookup"><span data-stu-id="6ecad-180">Sales tax codes</span></span>
    -   <span data-ttu-id="6ecad-181">Skupiny DPH</span><span class="sxs-lookup"><span data-stu-id="6ecad-181">Sales tax groups</span></span>
    -   <span data-ttu-id="6ecad-182">Skupiny DPH položky</span><span class="sxs-lookup"><span data-stu-id="6ecad-182">Item sales tax groups</span></span>
    -   <span data-ttu-id="6ecad-183">Účetní skupina</span><span class="sxs-lookup"><span data-stu-id="6ecad-183">Account group</span></span>
    -   <span data-ttu-id="6ecad-184">Kódy osvobození od DPH</span><span class="sxs-lookup"><span data-stu-id="6ecad-184">Sales tax exempt codes</span></span>
    -   <span data-ttu-id="6ecad-185">Příslušnosti k dani</span><span class="sxs-lookup"><span data-stu-id="6ecad-185">Sales tax jurisdictions</span></span>
    -   <span data-ttu-id="6ecad-186">Finanční úřady</span><span class="sxs-lookup"><span data-stu-id="6ecad-186">Sales tax authorities</span></span>
    -   <span data-ttu-id="6ecad-187">Období vyrovnání DPH</span><span class="sxs-lookup"><span data-stu-id="6ecad-187">Sales tax settlement periods</span></span>

<span data-ttu-id="6ecad-188">**Pokladna a správa banky**</span><span class="sxs-lookup"><span data-stu-id="6ecad-188">**Cash and bank management**</span></span>

-   <span data-ttu-id="6ecad-189">Stránka Kódy účelu platby slouží k nastavení kódu účelu centrální banky.</span><span class="sxs-lookup"><span data-stu-id="6ecad-189">On the Payment purpose codes page, set up the Central Bank purpose code.</span></span>





