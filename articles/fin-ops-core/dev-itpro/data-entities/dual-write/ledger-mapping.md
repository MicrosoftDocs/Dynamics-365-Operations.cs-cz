---
title: Integrovaná hlavní kniha
description: Toto téma popisuje integraci dat hlavní knihy mezi aplikacemi Finance and Operations a ostatními aplikacemi Dynamics 365 používajícími Common Data Service.
author: robinarh
manager: AnnBe
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ''
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 6bf1c554f56c1424da9fde98f67f80a6b7c95461
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019679"
---
# <a name="integrated-ledger"></a><span data-ttu-id="ba4b5-103">Integrovaná hlavní kniha</span><span class="sxs-lookup"><span data-stu-id="ba4b5-103">Integrated ledger</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="ba4b5-104">V obchodní aplikaci definují data hlavní knihy základní nastavení pro to, jak společnost podniká.</span><span class="sxs-lookup"><span data-stu-id="ba4b5-104">In a business application, ledger data defines the core set up for how a company does business.</span></span> <span data-ttu-id="ba4b5-105">Data hlavní knihy například popisují fiskální rok, podle kterého se společnost řídí, měny, ve kterých provádí transakce, a účty, které používá.</span><span class="sxs-lookup"><span data-stu-id="ba4b5-105">For example, ledger data describes the fiscal year the company follows, the currencies it transacts in, and the accounts it uses.</span></span> <span data-ttu-id="ba4b5-106">Toto téma popisuje integraci těchto základních finančních dat.</span><span class="sxs-lookup"><span data-stu-id="ba4b5-106">This topic describes the integration of this core financial data.</span></span>

## <a name="templates"></a><span data-ttu-id="ba4b5-107">Šablony</span><span class="sxs-lookup"><span data-stu-id="ba4b5-107">Templates</span></span>

<span data-ttu-id="ba4b5-108">Data hlavní knihy zahrnují mapy kolekce entit základních financí, které pracují společně během interakce s daty odběratele, jak je uvedeno v následující tabulce.</span><span class="sxs-lookup"><span data-stu-id="ba4b5-108">Ledger data includes a collection of core financial entity maps that work together during data interaction, as shown in the following table.</span></span>

<span data-ttu-id="ba4b5-109">Aplikace Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="ba4b5-109">Finance and Operations apps</span></span>      | <span data-ttu-id="ba4b5-110">Jiné aplikace Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="ba4b5-110">Other Dynamics 365 apps</span></span>
---------------------------------|---------------------------------
<span data-ttu-id="ba4b5-111">Měny</span><span class="sxs-lookup"><span data-stu-id="ba4b5-111">Currencies</span></span>                       | <span data-ttu-id="ba4b5-112">transactioncurrencies</span><span class="sxs-lookup"><span data-stu-id="ba4b5-112">transactioncurrencies</span></span>
<span data-ttu-id="ba4b5-113">FiscalCalendar</span><span class="sxs-lookup"><span data-stu-id="ba4b5-113">FiscalCalendar</span></span>                   | <span data-ttu-id="ba4b5-114">msdyn\_fiscalcalendars</span><span class="sxs-lookup"><span data-stu-id="ba4b5-114">msdyn\_fiscalcalendars</span></span>
<span data-ttu-id="ba4b5-115">FiscalCalendarYear</span><span class="sxs-lookup"><span data-stu-id="ba4b5-115">FiscalCalendarYear</span></span>               | <span data-ttu-id="ba4b5-116">msdyn\_fiscalcalendaryears</span><span class="sxs-lookup"><span data-stu-id="ba4b5-116">msdyn\_fiscalcalendaryears</span></span>
<span data-ttu-id="ba4b5-117">ExchRateType</span><span class="sxs-lookup"><span data-stu-id="ba4b5-117">ExchRateType</span></span>                     | <span data-ttu-id="ba4b5-118">msdyn\_exchangeratetypes</span><span class="sxs-lookup"><span data-stu-id="ba4b5-118">msdyn\_exchangeratetypes</span></span>
<span data-ttu-id="ba4b5-119">ExchangeRateCurrencyPair</span><span class="sxs-lookup"><span data-stu-id="ba4b5-119">ExchangeRateCurrencyPair</span></span>         | <span data-ttu-id="ba4b5-120">msdyn\_currencyexchangeratepairs</span><span class="sxs-lookup"><span data-stu-id="ba4b5-120">msdyn\_currencyexchangeratepairs</span></span>
<span data-ttu-id="ba4b5-121">FiscalPeriodEntity</span><span class="sxs-lookup"><span data-stu-id="ba4b5-121">FiscalPeriodEntity</span></span>               | <span data-ttu-id="ba4b5-122">msdyn\_fiscalcalendarperiods</span><span class="sxs-lookup"><span data-stu-id="ba4b5-122">msdyn\_fiscalcalendarperiods</span></span>
<span data-ttu-id="ba4b5-123">MainAccountCategory</span><span class="sxs-lookup"><span data-stu-id="ba4b5-123">MainAccountCategory</span></span>              | <span data-ttu-id="ba4b5-124">msdyn\_mainaccountcategory</span><span class="sxs-lookup"><span data-stu-id="ba4b5-124">msdyn\_mainaccountcategory</span></span>
<span data-ttu-id="ba4b5-125">MainAccount</span><span class="sxs-lookup"><span data-stu-id="ba4b5-125">MainAccount</span></span>                      | <span data-ttu-id="ba4b5-126">msdyn\_mainaccounts</span><span class="sxs-lookup"><span data-stu-id="ba4b5-126">msdyn\_mainaccounts</span></span>
<span data-ttu-id="ba4b5-127">Hlavní kniha</span><span class="sxs-lookup"><span data-stu-id="ba4b5-127">Ledger</span></span>                           | <span data-ttu-id="ba4b5-128">msdyn\_ledgers</span><span class="sxs-lookup"><span data-stu-id="ba4b5-128">msdyn\_ledgers</span></span>
<span data-ttu-id="ba4b5-129">ExchangeRates</span><span class="sxs-lookup"><span data-stu-id="ba4b5-129">ExchangeRates</span></span>                    | <span data-ttu-id="ba4b5-130">msdyn\_currencyexchangerates</span><span class="sxs-lookup"><span data-stu-id="ba4b5-130">msdyn\_currencyexchangerates</span></span>
<span data-ttu-id="ba4b5-131">FinancialCalendarPeriod</span><span class="sxs-lookup"><span data-stu-id="ba4b5-131">FinancialCalendarPeriod</span></span>          | <span data-ttu-id="ba4b5-132">msdyn\_fiscalcalendarperiods</span><span class="sxs-lookup"><span data-stu-id="ba4b5-132">msdyn\_fiscalcalendarperiods</span></span>
<span data-ttu-id="ba4b5-133">DimensionAttributeEntity</span><span class="sxs-lookup"><span data-stu-id="ba4b5-133">DimensionAttributeEntity</span></span>         | <span data-ttu-id="ba4b5-134">msdyn\_dimensionattributes.md</span><span class="sxs-lookup"><span data-stu-id="ba4b5-134">msdyn\_dimensionattributes.md</span></span>
<span data-ttu-id="ba4b5-135">DimensionIntegrationFormatEntity</span><span class="sxs-lookup"><span data-stu-id="ba4b5-135">DimensionIntegrationFormatEntity</span></span> | <span data-ttu-id="ba4b5-136">msdyn\_financialdimensionformats.md</span><span class="sxs-lookup"><span data-stu-id="ba4b5-136">msdyn\_financialdimensionformats.md</span></span>
<span data-ttu-id="ba4b5-137">LedgerChartOfAccounts</span><span class="sxs-lookup"><span data-stu-id="ba4b5-137">LedgerChartOfAccounts</span></span>            | <span data-ttu-id="ba4b5-138">msdyn\_chartofaccounts.md</span><span class="sxs-lookup"><span data-stu-id="ba4b5-138">msdyn\_chartofaccounts.md</span></span>


[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Currency](includes/Currencies-transactioncurrencies.md)]

[!include [Fiscal calendar](includes/FiscalCalendar-msdyn-fiscalcalendars.md)]

[!include [Fiscal calendar year](includes/FiscalCalendarYear-msdyn-fiscalcalendaryears.md)]

[!include [Exchange rate types](includes/ExchRateType-msdyn-exchangeratetypes.md)]

[!include [Exchange rate pair](includes/ExchangeRateCurrencyPair-msdyn-currencyexchangeratepairs.md)]

[!include [Ledger fiscal periods](includes/FiscalPeriodEntity-msdyn-fiscalcalendarperiods.md)]

[!include [Main account category](includes/MainAccountCategory-msdyn-mainaccountcategory.md)]

[!include [Main account](includes/MainAccount-msdyn-mainaccounts.md)]

[!include [Ledger](includes/Ledger-msdyn-ledgers.md)]

[!include [Exchange rates](includes/ExchangeRates-msdyn-currencyexchangerates.md)]

[!include [Financial Calendar Period](includes/FiscalPeriodEntity-msdyn-fiscalcalendarperiods.md)]

[!include [Dimension attribute](includes/DimensionAttributeEntity-msdyn-dimensionattributes.md)]

[!include [Dimension integration format](includes/DimensionIntegrationFormatEntity-msdyn-financialdimensionformats.md)]

[!include [Chart Of Account](includes/LedgerChartOfAccounts-msdyn-chartofaccounts.md)]




