---
title: Specifikace DPH podle sestavy transakce hlavní knihy
description: V tomto tématu je vysvětleno použití specifikace DPH podle sestavy transakce hlavní knihy k zobrazení a tisku informací o transakcích hlavní knihy, pro které se počítá DPH.
author: ericwang
manager: Ann Beebe
ms.date: 08/19/2019
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
ms.search.validFrom: 2019-08-19
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: b90ae491605bf59b93137936a2804c4b84c6e1b7
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5204875"
---
# <a name="sales-tax-specification-by-ledger-transaction-report"></a><span data-ttu-id="a705d-103">Specifikace DPH podle sestavy transakce hlavní knihy</span><span class="sxs-lookup"><span data-stu-id="a705d-103">Sales tax specification by ledger transaction report</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="a705d-104">V tomto tématu je vysvětleno použití **specifikace DPH podle sestavy transakce hlavní knihy** k zobrazení a tisku informací o transakcích hlavní knihy, pro které se počítá DPH.</span><span class="sxs-lookup"><span data-stu-id="a705d-104">This topic explains how to use the **Sales tax specification by ledger transaction** report to view and print information about ledger transactions that sales tax is calculated for.</span></span>

## <a name="tax-accounts-vs-non-tax-accounts"></a><span data-ttu-id="a705d-105">Daňové účty vs. nedaňové účty</span><span class="sxs-lookup"><span data-stu-id="a705d-105">Tax accounts vs. non-tax accounts</span></span>

<span data-ttu-id="a705d-106">Sestava **Specifikace DPH podle transakce hlavní knihy** zobrazuje daňové transakce pro daňové účty i pro nedaňové účty.</span><span class="sxs-lookup"><span data-stu-id="a705d-106">The **Sales tax specification by ledger transaction** report shows tax transactions for both tax accounts and non-tax accounts.</span></span> <span data-ttu-id="a705d-107">Tyto účty jsou rozděleny do kategorií následujícím způsobem:</span><span class="sxs-lookup"><span data-stu-id="a705d-107">These accounts are categorized in the following way:</span></span>

- <span data-ttu-id="a705d-108">**Daňový účet** – účet je považován za daňový účet při zaúčtování daňové transakce a hlavní účet na řádku deníku **DPH** je daňový účet, jako je například účet závazků DPH nebo účet pohledávek DPH.</span><span class="sxs-lookup"><span data-stu-id="a705d-108">**Tax account** – An account is considered a tax account when a tax transaction is posted, and the main account on the **Sales Tax** journal line is a tax account, such as a sales tax payable account or a sales tax receivable account.</span></span>
- <span data-ttu-id="a705d-109">**Nedaňový účet** – účet je považován za nedaňový účet při zaúčtování daňové transakce a hlavní účet v původní transakci je nedaňový účet, jako je například účet výnosů nebo účet výdajů.</span><span class="sxs-lookup"><span data-stu-id="a705d-109">**Non-tax account** – An account is considered a non-tax account when a tax transaction is posted, and the main account on the original transaction is a non-tax account, such as a revenue account or an expense account.</span></span>

<span data-ttu-id="a705d-110">U daňových účtů je **původní zdroj** **pohledávky DPH** a sloupce **Splatná DPH** v sestavě zobrazují hodnotu **0** (nula).</span><span class="sxs-lookup"><span data-stu-id="a705d-110">For tax accounts, the **Origin**, **Sales tax receivable**, and **Sales tax payable** columns on the report show **0** (zero).</span></span> <span data-ttu-id="a705d-111">U nedaňových účtů jsou v těchto sloupcích zobrazeny částky.</span><span class="sxs-lookup"><span data-stu-id="a705d-111">For non-tax accounts, those columns show amounts.</span></span>

## <a name="filtering-the-data-on-the-report"></a><span data-ttu-id="a705d-112">Filtrování dat v sestavě</span><span class="sxs-lookup"><span data-stu-id="a705d-112">Filtering the data on the report</span></span>

<span data-ttu-id="a705d-113">Při generování sestavy jsou k dispozici následující výchozí pole.</span><span class="sxs-lookup"><span data-stu-id="a705d-113">When you generate the report, the following default fields are available.</span></span> <span data-ttu-id="a705d-114">Tato pole slouží k filtrování dat, která se zobrazí v sestavě.</span><span class="sxs-lookup"><span data-stu-id="a705d-114">You can use these fields to filter the data that is shown on the report.</span></span>

| <span data-ttu-id="a705d-115">Pole</span><span class="sxs-lookup"><span data-stu-id="a705d-115">Field</span></span>                      | <span data-ttu-id="a705d-116">Popis</span><span class="sxs-lookup"><span data-stu-id="a705d-116">Description</span></span> |
|----------------------------|-------------|
| <span data-ttu-id="a705d-117">Datum</span><span class="sxs-lookup"><span data-stu-id="a705d-117">Date</span></span>                       | <span data-ttu-id="a705d-118">Pomocí polí v sekcích **Od** a **Do** definujte rozsah daňových transakcí.</span><span class="sxs-lookup"><span data-stu-id="a705d-118">Use the fields in the **From** and **To** sections to define a date range for the tax transactions.</span></span> |
| <span data-ttu-id="a705d-119">Hlavní účet</span><span class="sxs-lookup"><span data-stu-id="a705d-119">Main account</span></span>               | <span data-ttu-id="a705d-120">Pomocí polí v sekcích **Od** a **Do** definujte rozsah hlavních účtů.</span><span class="sxs-lookup"><span data-stu-id="a705d-120">Use the fields in the **From** and **To** sections to define a range of main accounts.</span></span> |
| <span data-ttu-id="a705d-121">Kód DPH</span><span class="sxs-lookup"><span data-stu-id="a705d-121">Sales tax code</span></span>             | <span data-ttu-id="a705d-122">Pomocí polí v sekcích **Od** a **Do** definujte rozsah kódů DPH.</span><span class="sxs-lookup"><span data-stu-id="a705d-122">Use the fields in the **From** and **To** sections to define a range of sales tax codes.</span></span> |
| <span data-ttu-id="a705d-123">Seskupení</span><span class="sxs-lookup"><span data-stu-id="a705d-123">Grouping</span></span>                   | <span data-ttu-id="a705d-124">Vyberte, zda má být sestava seskupena podle účtu hlavní knihy nebo kódu DPH.</span><span class="sxs-lookup"><span data-stu-id="a705d-124">Select whether the report should be grouped by ledger account or sales tax code.</span></span> |
| <span data-ttu-id="a705d-125">Mezisoučet podle kódu DPH/DPH</span><span class="sxs-lookup"><span data-stu-id="a705d-125">Subtotal by sales tax code</span></span> | <span data-ttu-id="a705d-126">Chcete-li zobrazit mezisoučty podle kódu DPH, nastavte tuto možnost na hodnotu **Ano**.</span><span class="sxs-lookup"><span data-stu-id="a705d-126">Set this option to **Yes** to show subtotals by sales tax code.</span></span> |
| <span data-ttu-id="a705d-127">Pouze součty</span><span class="sxs-lookup"><span data-stu-id="a705d-127">Totals only</span></span>                | <span data-ttu-id="a705d-128">Chcete-li zobrazit pouze součty, nastavte tuto možnost na hodnotu **Ano**.</span><span class="sxs-lookup"><span data-stu-id="a705d-128">Set this option to **Yes** to show only totals.</span></span> |
| <span data-ttu-id="a705d-129">Pouze hlavní účty</span><span class="sxs-lookup"><span data-stu-id="a705d-129">Main accounts only</span></span>         | <span data-ttu-id="a705d-130">Chcete-li do sestavy zahrnout pouze hlavní účty, nastavte tuto možnost na hodnotu **Ano**.</span><span class="sxs-lookup"><span data-stu-id="a705d-130">Set this option to **Yes** to include only main accounts on the report.</span></span> |

## <a name="showing-only-non-tax-accounts-on-the-report"></a><span data-ttu-id="a705d-131">Zobrazení pouze nedaňových účtů v sestavě</span><span class="sxs-lookup"><span data-stu-id="a705d-131">Showing only non-tax accounts on the report</span></span>

<span data-ttu-id="a705d-132">Chcete-li v sestavě zobrazit pouze nedaňové účty, nastavte podmínku filtru, například hvězdičku (\*), jak je znázorněno na následujícím obrázku.</span><span class="sxs-lookup"><span data-stu-id="a705d-132">To show only non-tax accounts on the report, set up a filter condition, such as an asterisk (\*), as shown in the following illustration.</span></span>

![Sestava zobrazující nedaňové účty](media/taxspecperledgertrans.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]