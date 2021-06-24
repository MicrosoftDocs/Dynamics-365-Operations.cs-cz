---
title: Nastavení a zpracování opakovaných faktur
description: Tento článek vysvětluje, jak lze nastavit a zpracovat opakované faktury. Opakované faktury lze použít, pokud musíte pravidelně fakturovat odběrateli stejnou částku.
author: ShivamPandey-msft
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustInvoiceTemplate
audience: Application User
ms.reviewer: roschlom
ms.custom: 14011
ms.assetid: 9cc37003-adf1-413d-b2b2-2badcf512e3b
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 834dc64ce531fb614bc7836e0def16f27ecf5e18
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/04/2021
ms.locfileid: "6188631"
---
# <a name="set-up-and-process-recurring-invoices"></a><span data-ttu-id="7cdb4-104">Nastavení a zpracování opakovaných faktur</span><span class="sxs-lookup"><span data-stu-id="7cdb4-104">Set up and process recurring invoices</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7cdb4-105">Tento článek vysvětluje, jak lze nastavit a zpracovat opakované faktury.</span><span class="sxs-lookup"><span data-stu-id="7cdb4-105">This article explains how to set up and process recurring invoices.</span></span> <span data-ttu-id="7cdb4-106">Opakované faktury lze použít, pokud musíte pravidelně fakturovat odběrateli stejnou částku.</span><span class="sxs-lookup"><span data-stu-id="7cdb4-106">You can use recurring invoices if you must invoice customers for the same amount on a regular basis.</span></span>

## <a name="create-a-recurring-free-text-invoice-template"></a><span data-ttu-id="7cdb4-107">Vytvoření šablony pro opakovanou volnou fakturu</span><span class="sxs-lookup"><span data-stu-id="7cdb4-107">Create a recurring free text invoice template</span></span>

<span data-ttu-id="7cdb4-108">Pro fakturaci odběratelů za stejné služby v pravidelných intervalech je nutné definovat šablonu volné faktury, kterou lze opakovaně použít k vytvoření faktur.</span><span class="sxs-lookup"><span data-stu-id="7cdb4-108">To invoice customers for the same services on a regular basis, you must define a free text invoice template that can be reused to create the invoices.</span></span> <span data-ttu-id="7cdb4-109">V šabloně jsou uvedeny následující informace:</span><span class="sxs-lookup"><span data-stu-id="7cdb4-109">This template contains the following information:</span></span>

-   <span data-ttu-id="7cdb4-110">Informace v záhlaví, jako jsou daňové skupiny, platební podmínky a způsob platby</span><span class="sxs-lookup"><span data-stu-id="7cdb4-110">Header information, such as tax groups, terms of payment, and the method of payment</span></span>
-   <span data-ttu-id="7cdb4-111">Informace o řádku, například popis služby, účty výnosů, jednotková cena a fakturovaná částka</span><span class="sxs-lookup"><span data-stu-id="7cdb4-111">Line information, such as the service description, revenue accounts, unit price, and invoice amount</span></span>
-   <span data-ttu-id="7cdb4-112">Náklady na dodání nebo zpracování</span><span class="sxs-lookup"><span data-stu-id="7cdb4-112">Charges for shipping or handling</span></span>
-   <span data-ttu-id="7cdb4-113">Rozúčtování společně s informacemi o finanční dimenzi, například nákladových střediscích nebo obchodních jednotkách</span><span class="sxs-lookup"><span data-stu-id="7cdb4-113">Accounting distributions together with financial dimension information, such as cost centers and business units</span></span>

<span data-ttu-id="7cdb4-114">V důsledku vytváříte celou fakturu a ukládáte ji jako šablonu.</span><span class="sxs-lookup"><span data-stu-id="7cdb4-114">In effect, you're creating an entire invoice and saving it as a template.</span></span> <span data-ttu-id="7cdb4-115">Šablony můžete nastavit pomocí stránky **Opakované faktury**.</span><span class="sxs-lookup"><span data-stu-id="7cdb4-115">You can set up the templates using the **Recurring invoices** page.</span></span>

## <a name="assign-a-free-text-invoice-template-to-a-customer-and-enter-recurrence-details"></a><span data-ttu-id="7cdb4-116">Přiřazení šablony volné faktury odběrateli a zadání podrobností o opakování</span><span class="sxs-lookup"><span data-stu-id="7cdb4-116">Assign a free text invoice template to a customer and enter recurrence details</span></span>
<span data-ttu-id="7cdb4-117">Po vytvoření šablony je nutné přiřadit šablonu zákazníkům, kterým má být vystavena.</span><span class="sxs-lookup"><span data-stu-id="7cdb4-117">After the template is created, you must assign the template to the customers that you want to invoice.</span></span> <span data-ttu-id="7cdb4-118">Dále zadejte, kdy a jak často se má fakturovat.</span><span class="sxs-lookup"><span data-stu-id="7cdb4-118">Additionally, you must specify when and how often the invoice will be used.</span></span> <span data-ttu-id="7cdb4-119">Šablony můžete přiřadit na kartě **Faktury** na stránce **Odběratelé**.</span><span class="sxs-lookup"><span data-stu-id="7cdb4-119">You can assign the templates on the **Invoice** tab of the **Customers** page.</span></span> <span data-ttu-id="7cdb4-120">Přidejte šablonu do seznamu a aktualizujte následující informace:</span><span class="sxs-lookup"><span data-stu-id="7cdb4-120">Add the template to the list, and update the following information:</span></span>

-   <span data-ttu-id="7cdb4-121">Počáteční datum a případně koncové datum pro opakování účtování</span><span class="sxs-lookup"><span data-stu-id="7cdb4-121">The start date and, optionally, the end date for the recurring billing</span></span>
-   <span data-ttu-id="7cdb4-122">Frekvence opakování fakturace (například každý den nebo jednou za měsíc)</span><span class="sxs-lookup"><span data-stu-id="7cdb4-122">The frequency of the recurring billing (for example, every day or once a month)</span></span>
-   <span data-ttu-id="7cdb4-123">Maximální částka účtování (pokud jsou tyto informace požadovány)</span><span class="sxs-lookup"><span data-stu-id="7cdb4-123">The maximum billing amount (if this information is required)</span></span>

<span data-ttu-id="7cdb4-124">Zákazník může mít více šablon, které mají různé intervaly.</span><span class="sxs-lookup"><span data-stu-id="7cdb4-124">A customer can have multiple templates that have different frequencies.</span></span>

## <a name="generate-the-recurring-invoices"></a><span data-ttu-id="7cdb4-125">Generování opakovaných faktur</span><span class="sxs-lookup"><span data-stu-id="7cdb4-125">Generate the recurring invoices</span></span>
<span data-ttu-id="7cdb4-126">Na stránce **Opakované faktury** je úkol, který zpracovává šablony opakovaných faktur.</span><span class="sxs-lookup"><span data-stu-id="7cdb4-126">On the **Recurring invoices** page, there is a task that processes recurring invoice templates.</span></span> <span data-ttu-id="7cdb4-127">Určete datum faktury a šablonu, ze které se mají faktury generovat.</span><span class="sxs-lookup"><span data-stu-id="7cdb4-127">You specify the invoice date and the template to generate the invoices from.</span></span> <span data-ttu-id="7cdb4-128">Faktury budou generovány a každé skupině zpracovaných faktur se přiřadí jedno ID opakování.</span><span class="sxs-lookup"><span data-stu-id="7cdb4-128">Invoices will be generated and assigned a single recurrence ID number for each group of invoices that is processed.</span></span>

## <a name="post-recurring-free-text-invoices"></a><span data-ttu-id="7cdb4-129">Zaúčtování opakovaných volných faktur</span><span class="sxs-lookup"><span data-stu-id="7cdb4-129">Post recurring free text invoices</span></span>

<span data-ttu-id="7cdb4-130">Po vygenerování opakovaných faktur se ID opakování faktury objeví v zaúčtování úloh stránce **Opakované faktury**.</span><span class="sxs-lookup"><span data-stu-id="7cdb4-130">After recurring invoices are generated, the invoice recurrence IDs appear in a posting task on the **Recurring invoices** page.</span></span> <span data-ttu-id="7cdb4-131">Všechny faktury se stejným ID opakování si můžete prohlédnout kliknutím na odkaz.</span><span class="sxs-lookup"><span data-stu-id="7cdb4-131">You can view all of the invoices for a recurrence ID by clicking the link.</span></span> <span data-ttu-id="7cdb4-132">Během kontroly faktur podle ID opakování lze jednotlivé faktury odstranit.</span><span class="sxs-lookup"><span data-stu-id="7cdb4-132">During your review of the invoices for the recurrence ID, you can delete individual invoices.</span></span> <span data-ttu-id="7cdb4-133">Nastavení opakování se u šablony odběratele obnoví, aby se mohla znovu generovat později.</span><span class="sxs-lookup"><span data-stu-id="7cdb4-133">The customer's recurrence settings will be reset for that template, so that it can be regenerated later.</span></span> <span data-ttu-id="7cdb4-134">Zaúčtovat můžete jednu, více nebo všechny faktury pro ID opakování.</span><span class="sxs-lookup"><span data-stu-id="7cdb4-134">You can post one, many, or all of the invoices for a recurrence ID.</span></span> <span data-ttu-id="7cdb4-135">Jsou-li workflowy povolené, je nutné před zaúčtováním faktury kliknout na tlačítko **Odeslat**.</span><span class="sxs-lookup"><span data-stu-id="7cdb4-135">If workflows are enabled, you must click **Submit** before you can post the invoices.</span></span>

## <a name="print-recurring-free-text-invoices"></a><span data-ttu-id="7cdb4-136">Tisk opakovaných volných faktur</span><span class="sxs-lookup"><span data-stu-id="7cdb4-136">Print recurring free text invoices</span></span>

<span data-ttu-id="7cdb4-137">Po zaúčtování opakované faktury můžete faktury vytisknout ze stránky se seznamem volných faktur.</span><span class="sxs-lookup"><span data-stu-id="7cdb4-137">After recurring invoices are posted, you can print the invoices from the free text invoice list page.</span></span> <span data-ttu-id="7cdb4-138">Lze vytisknout vybrané faktury nebo vybrat rozsah faktur k tisku.</span><span class="sxs-lookup"><span data-stu-id="7cdb4-138">You can print the invoices that are selected, or you can select a range of invoices to print.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]