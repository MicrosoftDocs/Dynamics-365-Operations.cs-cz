---
title: "Přehled směnného kurzu DPH"
description: "Toto téma obsahuje informace o směnných kurzech pro výpočet DPH. Směnný kurz, který se používá k výpočtu DPH, může být odlišný od směnného kurzu, který organizace používá pro funkce účetnictví. Při zaúčtování dokumentu v cizí měně jsou zaúčtovány všechny vzniklé kurzové rozdíly do konkrétních účtů hlavní knihy."
author: ShylaThompson
manager: AnnBe
ms.date: 04/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ExchangeRateCurrencyPairCalculationRules, LedgerParameters, SalesTaxExchangeRateType, TaxTmpWorkTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 272703
ms.assetid: 2d1fad67-8234-49cc-b009-0f3cc29f5886
ms.search.region: Czech Republic, Hungary, Poland
ms.author: mrolecki
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: f6a1bd580de0a2c40ce3a407c0fd056cae98bfee
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="vat-exchange-rate-overview"></a><span data-ttu-id="b53c8-105">Přehled směnného kurzu DPH</span><span class="sxs-lookup"><span data-stu-id="b53c8-105">VAT exchange rate overview</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="b53c8-106">Toto téma obsahuje informace o směnných kurzech pro výpočet DPH.</span><span class="sxs-lookup"><span data-stu-id="b53c8-106">This topic provides information about exchange rates for the VAT calculation.</span></span> <span data-ttu-id="b53c8-107">Směnný kurz, který se používá k výpočtu DPH, může být odlišný od směnného kurzu, který organizace používá pro funkce účetnictví.</span><span class="sxs-lookup"><span data-stu-id="b53c8-107">The exchange rate that is used for VAT calculation can differ from the exchange rate that is used for company accounting functions.</span></span> <span data-ttu-id="b53c8-108">Při zaúčtování dokumentu v cizí měně jsou zaúčtovány všechny vzniklé kurzové rozdíly do konkrétních účtů hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="b53c8-108">When a document in a foreign currency is posted, any exchange rate differences that occur are posted to specific ledger accounts.</span></span>

<span data-ttu-id="b53c8-109">Vaše organizace může vybrat směnný kurz, který používá, pro výpočet daně z přidané hodnoty (DPH) pro výkazy DPH.</span><span class="sxs-lookup"><span data-stu-id="b53c8-109">Your organization can select the exchange rate that it uses to calculate value-added tax (VAT) for VAT statements.</span></span> <span data-ttu-id="b53c8-110">Tento směnný kurz může být odlišný od směnného kurzu, který organizace používá pro funkce účetnictví společnosti.</span><span class="sxs-lookup"><span data-stu-id="b53c8-110">This exchange rate can differ from the exchange rate that your organization uses for company accounting functions.</span></span> <span data-ttu-id="b53c8-111">Funkce účetnictví zahrnují přípravu následujících dokumentů souvisejících s daněmi:</span><span class="sxs-lookup"><span data-stu-id="b53c8-111">Accounting functions include the preparation of the following tax-related documents:</span></span>

-   <span data-ttu-id="b53c8-112">Faktury</span><span class="sxs-lookup"><span data-stu-id="b53c8-112">Invoices</span></span>
-   <span data-ttu-id="b53c8-113">Volné faktury</span><span class="sxs-lookup"><span data-stu-id="b53c8-113">Free text invoices</span></span>
-   <span data-ttu-id="b53c8-114">Nákupní objednávky</span><span class="sxs-lookup"><span data-stu-id="b53c8-114">Purchase orders</span></span>
-   <span data-ttu-id="b53c8-115">Faktury projektu</span><span class="sxs-lookup"><span data-stu-id="b53c8-115">Project invoices</span></span>
-   <span data-ttu-id="b53c8-116">Dobropisy</span><span class="sxs-lookup"><span data-stu-id="b53c8-116">Credit notes</span></span>
-   <span data-ttu-id="b53c8-117">Opravné faktury</span><span class="sxs-lookup"><span data-stu-id="b53c8-117">Corrective invoices</span></span>

<span data-ttu-id="b53c8-118">Při zaúčtování dokumentu, který používá cizí měnu, jsou zaúčtovány všechny vzniklé kurzové rozdíly do konkrétních účtů hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="b53c8-118">When you post a document that uses a foreign currency, any exchange rate differences that occur are posted to specific ledger accounts.</span></span>

<a name="prerequisites"></a><span data-ttu-id="b53c8-119">Požadavky</span><span class="sxs-lookup"><span data-stu-id="b53c8-119">Prerequisites</span></span>
=============

<span data-ttu-id="b53c8-120">Než budete moci použít tuto funkci, musíte nakonfigurovat systém.</span><span class="sxs-lookup"><span data-stu-id="b53c8-120">Before you can use this functionality, you must configure the system.</span></span>

1.  <span data-ttu-id="b53c8-121">Vytvořte typy směnných kurzů a nastavte směnné kurzy pro DPH pomocí možností **Hlavní kniha** &gt; **Měny** &gt; **Typy směnných kurzů**.</span><span class="sxs-lookup"><span data-stu-id="b53c8-121">Create exchange rate types and set up exchange rates for the sales tax at **General ledger** &gt; **Currencies** &gt; **Exchange rate types**.</span></span> <span data-ttu-id="b53c8-122">Můžete definovat tolik typů směnných kurzů a tolik směnných kurzů pro páry měn, kolik potřebujete.</span><span class="sxs-lookup"><span data-stu-id="b53c8-122">You can define as many exchange rate types and as many exchange rates for pairs of currencies as you require.</span></span>
2.  <span data-ttu-id="b53c8-123">Povolte výpočet směnných kurzů DPH zapnutím parametru **Bankovní směnný kurz** a definováním typů směnných kurzů pohledávek DPH a závazků DPH v parametrech **Hlavní kniha** &gt; **Nastavení hlavní knihy** &gt; **Parametry hlavní knihy**.</span><span class="sxs-lookup"><span data-stu-id="b53c8-123">Enable the calculation of VAT exchange rates by turning on the **Bank exchange rate** parameter, and by defining sales tax receivable and sales tax payable exchange rate types, at **General ledger** &gt; **Ledger setup** &gt; **General ledger parameters**.</span></span>
3.  <span data-ttu-id="b53c8-124">Nastavte typy směnných kurzů měny pro určité prodejní a nákupní typy transakcí v možnostech **Hlavní kniha** &gt; **Měny** &gt;**Typy směnného kurzu pro prodejní daň**.</span><span class="sxs-lookup"><span data-stu-id="b53c8-124">Set up currency exchange rate types for specific sales and purchase transaction types at **General ledger** &gt; **Currencies** &gt; **Currency exchange rate types for sales tax**.</span></span>
4.  <span data-ttu-id="b53c8-125">Nastavte rozdíl mezi závazky DPH a pohledávkami DPH a rozdíl protiúčtů ve skupinách zaúčtování hlavní knihy v možnostech **Daň** &gt; **Nastavení** &gt; **DPH** &gt; **Skupiny zaúčtování hlavní knihy**.</span><span class="sxs-lookup"><span data-stu-id="b53c8-125">Set up sales tax receivable and sales tax payable difference and difference offset accounts in the ledger posting groups at **Tax** &gt; **Setup** &gt; **Sales tax** &gt; **Ledger posting groups**.</span></span>
5.  <span data-ttu-id="b53c8-126">Volitelné: Nastavte pravidlo výpočtu směnného kurzu pro pár měny v možnostech **Hlavní kniha** &gt; **Měny** &gt; **Pravidla výpočtu směnného kurzu pro páry měn**.</span><span class="sxs-lookup"><span data-stu-id="b53c8-126">Optional: Set up an exchange rate calculation rule for a currency pair at **General ledger** &gt; **Currencies** &gt; **Exchange rate calculation rules for currency pairs**.</span></span> <span data-ttu-id="b53c8-127">Pravidla výpočtu směnného kurzu se používají k převodu částek DPH pro prodejní faktury v cizí měně na částky DPH v cílové měně.</span><span class="sxs-lookup"><span data-stu-id="b53c8-127">The exchange rate calculation rules are used to convert VAT amounts for foreign currency sales invoices to VAT amounts in a destination currency.</span></span>

<a name="overview"></a><span data-ttu-id="b53c8-128">Přehled</span><span class="sxs-lookup"><span data-stu-id="b53c8-128">Overview</span></span>
========

<span data-ttu-id="b53c8-129">Po dokončení konfigurace systému pro použití směnných kurzů DPH, pokud je nutné zadat dokument nebo vytvořit objednávku používající cizí měnu, lze použít stránku **Transakce DPH** pro nastavení hodnoty **Datum rejstříku DPH** k vyzvednutí a nastavení výchozí hodnoty **Směnný kurz DPH**.</span><span class="sxs-lookup"><span data-stu-id="b53c8-129">After you've configured the system to use VAT exchange rates, if you must enter a document or create an order that uses a foreign currency, you can use **Sales tax transactions** page to set the **Date of VAT register** value to pick up and set the default **Sales tax exchange rate** value.</span></span> <span data-ttu-id="b53c8-130">Obě pole lze upravovat.</span><span class="sxs-lookup"><span data-stu-id="b53c8-130">You can edit both fields.</span></span> <span data-ttu-id="b53c8-131">Můžete také použít pole **Původ opravené částky (směnný kurz DPH)** nebo **Opravená částka DPH (směnný kurz DPH)** pro zadání skutečných částek DPH v místní měně, která je uvedena v externím dokumentu.</span><span class="sxs-lookup"><span data-stu-id="b53c8-131">You can also use the **Adjusted amount origin (VAT exchange rate)** or **Adjusted sales tax amount (VAT exchange rate)** field to enter actual VAT amounts in the local currency that is stated in an external document.</span></span> <span data-ttu-id="b53c8-132">Při kontrole účetnictví můžete zobrazit částky rozdílu DPH na stránce **Dílčí hlavní kniha**.</span><span class="sxs-lookup"><span data-stu-id="b53c8-132">When you review the accounting, you can view sales tax difference amounts on the **Subledger journal** page.</span></span> <span data-ttu-id="b53c8-133">Při zaúčtování dokumentu můžete zobrazit jakékoliv rozdíly v částkách DPH způsobené rozdílem mezi směnným kurzem měny DPH a směnným kurzem účetnictví vaší organizace, které jsou zaúčtovány do účtů hlavní knihy, které jste nakonfigurovali.</span><span class="sxs-lookup"><span data-stu-id="b53c8-133">When a document is posted, for transactions that are posted to the general ledger accounts that you've configured, you can view any differences in sales tax amounts that are caused by the difference between the VAT currency exchange rate and the accounting currency exchange rate for your organization.</span></span>





