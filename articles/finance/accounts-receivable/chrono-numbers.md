---
title: Chronologické číslování dokumentů a dokladů
description: Toto téma vysvětluje, jak nastavit a používat chronologická čísla pro příslušné dokumenty a související doklady.
author: ikond
ms.date: 02/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: NumberSequenceGroup
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 401195
ms.search.region: Global
ms.author: ilyako
ms.search.validFrom: 2021-03-15
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: fe533052b0e5b04a7d27b954ba644761c631d6d7
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838854"
---
# <a name="numbering-documents-and-vouchers-chronologically"></a><span data-ttu-id="72803-103">Chronologické číslování dokumentů a dokladů</span><span class="sxs-lookup"><span data-stu-id="72803-103">Numbering documents and vouchers chronologically</span></span>

[!include [banner](../includes/banner.md)]


<span data-ttu-id="72803-104">V některých zemích existuje zákonný požadavek na číslování dokumentů a souvisejících dokladů v chronologickém pořadí.</span><span class="sxs-lookup"><span data-stu-id="72803-104">In some countries, there is a legal requirement to number documents and related vouchers in chronological order.</span></span> <span data-ttu-id="72803-105">Chronologie musí být podporována obdobími.</span><span class="sxs-lookup"><span data-stu-id="72803-105">The chronology must be supported by periods.</span></span> <span data-ttu-id="72803-106">Všechna čísla, která patří do dřívějších období, musí být menší než čísla, která patří do pozdějších období.</span><span class="sxs-lookup"><span data-stu-id="72803-106">All of the numbers that belong to earlier periods must be less than the numbers that belong to later periods.</span></span> <span data-ttu-id="72803-107">Pro splnění tohoto požadavku byla implementována funkce chronologického číslování.</span><span class="sxs-lookup"><span data-stu-id="72803-107">To meet this requirement, chronological numbering functionality has been implemented.</span></span> <span data-ttu-id="72803-108">Toto téma vysvětluje, jak konfigurovat a používat chronologická čísla pro příslušné dokumenty a související doklady.</span><span class="sxs-lookup"><span data-stu-id="72803-108">This topic explains how to configure and use chronological numbers for applicable documents and related vouchers.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="72803-109">Předpoklady</span><span class="sxs-lookup"><span data-stu-id="72803-109">Prerequisites</span></span>

<span data-ttu-id="72803-110">V pracovním prostoru Správa funkcí zapněte funkci **Chronologické číslování**:</span><span class="sxs-lookup"><span data-stu-id="72803-110">In the Feature management workspace, turn on the **Chronological numbering** feature.</span></span> <span data-ttu-id="72803-111">Další informace naleznete v tématu [Přehled správy funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="72803-111">For more information, see [Feature management overview](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>

## <a name="configure-chronological-numbering"></a><span data-ttu-id="72803-112">Konfigurace chronologického číslování</span><span class="sxs-lookup"><span data-stu-id="72803-112">Configure chronological numbering</span></span>

<span data-ttu-id="72803-113">Chronologické číslování má vliv na následující dokumenty.</span><span class="sxs-lookup"><span data-stu-id="72803-113">Chronological numbering affects the following documents.</span></span>

<span data-ttu-id="72803-114">**Pohledávky**</span><span class="sxs-lookup"><span data-stu-id="72803-114">**Accounts receivable**</span></span>
- <span data-ttu-id="72803-115">Faktura zákazníka</span><span class="sxs-lookup"><span data-stu-id="72803-115">Customer invoice</span></span>
- <span data-ttu-id="72803-116">Doklad faktury odběratele</span><span class="sxs-lookup"><span data-stu-id="72803-116">Customer invoice voucher</span></span>
- <span data-ttu-id="72803-117">Prodejní dobropis</span><span class="sxs-lookup"><span data-stu-id="72803-117">Sales credit note</span></span>
- <span data-ttu-id="72803-118">Doklad prodejního dobropisu</span><span class="sxs-lookup"><span data-stu-id="72803-118">Sales credit note voucher</span></span>
- <span data-ttu-id="72803-119">Volné faktury</span><span class="sxs-lookup"><span data-stu-id="72803-119">Free text invoice</span></span>
- <span data-ttu-id="72803-120">Doklad volné faktury</span><span class="sxs-lookup"><span data-stu-id="72803-120">Free text invoice voucher</span></span>
- <span data-ttu-id="72803-121">Dobropis s volným textem</span><span class="sxs-lookup"><span data-stu-id="72803-121">Free text credit note</span></span>
- <span data-ttu-id="72803-122">Úplný text dobropisu dokladu</span><span class="sxs-lookup"><span data-stu-id="72803-122">Free text credit note voucher</span></span>
- <span data-ttu-id="72803-123">Dodací list</span><span class="sxs-lookup"><span data-stu-id="72803-123">Packing slip</span></span>
- <span data-ttu-id="72803-124">Doklad dodacího listu</span><span class="sxs-lookup"><span data-stu-id="72803-124">Packing slip voucher</span></span>
- <span data-ttu-id="72803-125">Doklad o opravě dodacího listu</span><span class="sxs-lookup"><span data-stu-id="72803-125">Packing slip correction voucher</span></span>
- <span data-ttu-id="72803-126">Doklad oznámení úroků</span><span class="sxs-lookup"><span data-stu-id="72803-126">Interest note voucher</span></span>
- <span data-ttu-id="72803-127">Doklad upomínky</span><span class="sxs-lookup"><span data-stu-id="72803-127">Collection letter voucher</span></span>

<span data-ttu-id="72803-128">**Závazky**</span><span class="sxs-lookup"><span data-stu-id="72803-128">**Accounts payable**</span></span>
- <span data-ttu-id="72803-129">Doklad faktury</span><span class="sxs-lookup"><span data-stu-id="72803-129">Invoice voucher</span></span>
- <span data-ttu-id="72803-130">Doklad dobropisu</span><span class="sxs-lookup"><span data-stu-id="72803-130">Credit note voucher</span></span>
- <span data-ttu-id="72803-131">Doklad příjemky produktu</span><span class="sxs-lookup"><span data-stu-id="72803-131">Product receipt voucher</span></span>

<span data-ttu-id="72803-132">**Správa projektu**</span><span class="sxs-lookup"><span data-stu-id="72803-132">**Project management**</span></span>
- <span data-ttu-id="72803-133">Faktura</span><span class="sxs-lookup"><span data-stu-id="72803-133">Invoice</span></span>
- <span data-ttu-id="72803-134">Doklad faktury</span><span class="sxs-lookup"><span data-stu-id="72803-134">Invoice voucher</span></span>
- <span data-ttu-id="72803-135">Dobropis</span><span class="sxs-lookup"><span data-stu-id="72803-135">Credit note</span></span>
- <span data-ttu-id="72803-136">Doklad dobropisu</span><span class="sxs-lookup"><span data-stu-id="72803-136">Credit note voucher</span></span> 

### <a name="define-number-sequences"></a><span data-ttu-id="72803-137">Definice číselných řad</span><span class="sxs-lookup"><span data-stu-id="72803-137">Define number sequences</span></span>

<span data-ttu-id="72803-138">Chcete-li definovat číselné řady, přejděte na **Správa organizace** > **Číselné řady** > **Číselné řady**.</span><span class="sxs-lookup"><span data-stu-id="72803-138">To define number sequences, go to **Organization administration** > **Number sequences** > **Number sequences**.</span></span> <span data-ttu-id="72803-139">Můžete definovat tolik číselných sekvencí, kolik je požadováno pro pokrytí ovlivněných období pro požadované dokumenty.</span><span class="sxs-lookup"><span data-stu-id="72803-139">You can define as many number sequences as required to cover the affected periods for required documents.</span></span> 

<span data-ttu-id="72803-140">Zadejte společnost pro každou číselnou řadu.</span><span class="sxs-lookup"><span data-stu-id="72803-140">Specify a company for each number sequence.</span></span> <span data-ttu-id="72803-141">Segmenty číselných sekvencí musí být definovány tak, aby tvořily chronologické pořadí pro období.</span><span class="sxs-lookup"><span data-stu-id="72803-141">The segments of the number sequences must be defined so that they provide chronological order for periods.</span></span> <span data-ttu-id="72803-142">Názvy segmentů mohou například obsahovat speciální předponu, která identifikuje konkrétní období.</span><span class="sxs-lookup"><span data-stu-id="72803-142">For example, the segment names can contain a special prefix that identifies a specific period.</span></span>

![Nastavení číselných řad](media/chrono-num-sequence.jpg)

### <a name="configure-number-sequence-groups"></a><span data-ttu-id="72803-144">Konfigurace skupin číselných řad</span><span class="sxs-lookup"><span data-stu-id="72803-144">Configure number sequence groups</span></span>

<span data-ttu-id="72803-145">Chcete-li konfigurovat skupiny číselných řad, přejděte na **Pohledávky** > **Nastavení** > **Parametry pohledávek**.</span><span class="sxs-lookup"><span data-stu-id="72803-145">To configure number sequence groups, go to **Accounts receivable** > **Setup** > **Accounts receivable parameters**.</span></span> <span data-ttu-id="72803-146">Na kartě **Číselné řady** definujte tolik skupin číselných sekvencí, kolik je potřeba k pokrytí ovlivněných období.</span><span class="sxs-lookup"><span data-stu-id="72803-146">On the **Number sequences** tab, define as many number sequences groups as required to cover the affected periods.</span></span> 

<span data-ttu-id="72803-147">Pro každou skupinu v části **Odkaz** vyberte jeden z podporovaných odkazů na dokumenty a v části **Kód číselné řady** zadejte číselnou řadu, která byla dříve vytvořena pro příslušné období.</span><span class="sxs-lookup"><span data-stu-id="72803-147">For each group, in the **Reference** section, select one of the supported document references, and in the **Number sequence code** field, refer to a number sequence that was previously created for the related period.</span></span>

![Nastavení skupiny číselných řad](media/chrono-num-sequence-group.jpg)

<span data-ttu-id="72803-149">Podobně nakonfigurujte skupiny číselných řad v modulech **Pohledávky** a **Řízení projektů a účetnictví**.</span><span class="sxs-lookup"><span data-stu-id="72803-149">Similarly, configure number sequence groups in **Accounts payable** and **Project management and accounting** modules.</span></span>

### <a name="configure-number-sequence-groups-chronology"></a><span data-ttu-id="72803-150">Konfigurace chronologie skupin číselných řad</span><span class="sxs-lookup"><span data-stu-id="72803-150">Configure number sequence groups chronology</span></span>

<span data-ttu-id="72803-151">Chcete-li nakonfigurovat chronologii skupin číselných řad, přejděte na **Správa organizace** > **Číselné řady** > **Skupiny chronologických číselných řad**.</span><span class="sxs-lookup"><span data-stu-id="72803-151">To configure number sequence groups chronology, go to **Organization administration** > **Number sequences** > **Chronological number sequence groups**.</span></span> <span data-ttu-id="72803-152">Definujte podmínky použitelnosti pro skupiny číselných sekvencí.</span><span class="sxs-lookup"><span data-stu-id="72803-152">Define the applicability conditions for number sequence groups.</span></span>

![Nastavení chronologických čísel](media/chrono-num-sequence-group-period.jpg)

| <span data-ttu-id="72803-154">Pole</span><span class="sxs-lookup"><span data-stu-id="72803-154">Field</span></span>            | <span data-ttu-id="72803-155">popis</span><span class="sxs-lookup"><span data-stu-id="72803-155">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72803-156">Účinné:</span><span class="sxs-lookup"><span data-stu-id="72803-156">Effective</span></span>  | <span data-ttu-id="72803-157">Datum zahájení použitelnosti skupiny číselných řad.</span><span class="sxs-lookup"><span data-stu-id="72803-157">The start date of number sequence group applicability.</span></span> |
| <span data-ttu-id="72803-158">Vypršení platnosti</span><span class="sxs-lookup"><span data-stu-id="72803-158">Expiration</span></span>      | <span data-ttu-id="72803-159">Koncové datum použitelnosti skupiny číselných řad.</span><span class="sxs-lookup"><span data-stu-id="72803-159">The end date of number sequence group applicability.</span></span> <span data-ttu-id="72803-160">Pokud není použito žádné datum ukončení, vyberte **Nikdy**.</span><span class="sxs-lookup"><span data-stu-id="72803-160">If no end date is applied, select **Never**.</span></span> |
| <span data-ttu-id="72803-161">Skupina číselné řady</span><span class="sxs-lookup"><span data-stu-id="72803-161">Number sequence group</span></span> | <span data-ttu-id="72803-162">Skupina číselných řad, která bude použita ke generování čísel dokumentů během období.</span><span class="sxs-lookup"><span data-stu-id="72803-162">Number sequence group that will be used to generate document numbers during the period.</span></span> |
| <span data-ttu-id="72803-163">Původní skupina číselných řad</span><span class="sxs-lookup"><span data-stu-id="72803-163">Original number sequence group</span></span> | <span data-ttu-id="72803-164">Tento kód skupiny číselných sekvencí se používá pro další filtrování pro případy, kdy dokumenty již mají přiřazenou konkrétní *trvalou* skupinu číselných řad.</span><span class="sxs-lookup"><span data-stu-id="72803-164">This number sequence group code is used for additional filtering for the cases when documents already have a specific *permanent* number sequence group assigned.</span></span> <span data-ttu-id="72803-165">Prázdná hodnota se považuje za konkrétní hodnotu.</span><span class="sxs-lookup"><span data-stu-id="72803-165">An empty value is considered a specific value.</span></span> <span data-ttu-id="72803-166">Pokud potřebujete ignorovat předběžně přiřazenou skupinu, použijte **Výchozí** možnost pro toto nastavení.</span><span class="sxs-lookup"><span data-stu-id="72803-166">If you need to ignore a preliminary assigned group, use the **Default** option for this setup.</span></span> |
| <span data-ttu-id="72803-167">Výchozí</span><span class="sxs-lookup"><span data-stu-id="72803-167">Default</span></span> | <span data-ttu-id="72803-168">Pokud je zapnuto, systém ignoruje předběžně přiřazenou skupinu čísel dokumentů a pro analýzu použitelnosti používá pouze počáteční a koncová data období.</span><span class="sxs-lookup"><span data-stu-id="72803-168">If turned on, the system ignores the preliminary assigned document number sequence group and uses only the periods start and end dates for applicability analysis.</span></span> <span data-ttu-id="72803-169">Pokud je vypnuto, systém používá pro výběr celou kombinaci **Platnost** + **Vypršení** + **Původní skupina číselných řad**.</span><span class="sxs-lookup"><span data-stu-id="72803-169">If turned off, the system uses the full combination **Effective** + **Expiration** + **Original number sequence group** for selection.</span></span> |

## <a name="document-posting"></a><span data-ttu-id="72803-170">Zaúčtování dokumentu</span><span class="sxs-lookup"><span data-stu-id="72803-170">Document posting</span></span>
<span data-ttu-id="72803-171">Když zaúčtujete dokument, je dokumentu přiřazena příslušná skupina číselných řad na základě data zaúčtování dokumentu a poté je použita ke generování čísla dokumentu na základě zjištěné číselné řady.</span><span class="sxs-lookup"><span data-stu-id="72803-171">When you post a document, the appropriate number sequence group is assigned to the document, based on document's posting date, and then used to generate a document number based on the detected number sequence.</span></span> <span data-ttu-id="72803-172">Systém poskytuje zprávu týkající se přiřazení skupiny číselných řad.</span><span class="sxs-lookup"><span data-stu-id="72803-172">The system provides a message regarding the number sequence group assignment.</span></span>

![Číslo dokumentu](media/chrono-num-sequence-fti.jpg)

> [!NOTE]
> <span data-ttu-id="72803-174">V některých zemích již existuje specifická logika pro číslování dokumentů.</span><span class="sxs-lookup"><span data-stu-id="72803-174">For some countries, there is a specific logic already implemented for document numbering.</span></span> <span data-ttu-id="72803-175">V takovém případě logika konkrétní země přepíše funkci **Chronologické číslování**.</span><span class="sxs-lookup"><span data-stu-id="72803-175">In this case, country-specific logic will override the **Chronological numbering** feature.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
