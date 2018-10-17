--- 
title: "Auditování faktur a klíčových dat v systému závazků"
description: "Pokud od dodavatele obdržíte fakturu za zboží nebo služby na nákupní objednávce, mohou obchodní procesy vyžadovat, aby zboží nebo služby byly před schválením této faktury k platbě skutečně přijaty."
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchTable, PurchCreateOrder, PurchEditLines, VendEditInvoice, VendEditInvoiceDefaultQuantityForLinesDropDialog,  VendJournalMatch_PackingSlip, VendInvoiceMatchingDetails
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 70a7a1f7d7a8221a72addfbee1d21f813df4eb46
ms.contentlocale: cs-cz
ms.lasthandoff: 09/14/2018

---
# <a name="audit-invoices-and-key-data-in-ap-system"></a><span data-ttu-id="be769-103">Auditování faktur a klíčových dat v systému závazků</span><span class="sxs-lookup"><span data-stu-id="be769-103">Audit invoices and key data in AP system</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="be769-104">Pokud od dodavatele obdržíte fakturu za zboží nebo služby na nákupní objednávce, mohou obchodní procesy vyžadovat, aby zboží nebo služby byly před schválením této faktury k platbě skutečně přijaty.</span><span class="sxs-lookup"><span data-stu-id="be769-104">When you receive an invoice from a vendor for goods or services on a purchase order, the business processes might require that the goods or services be received before the invoice can be approved for payment.</span></span> <span data-ttu-id="be769-105">Před prvním krokem ověřte, že je vybraný konfigurační klíč Párování faktur.</span><span class="sxs-lookup"><span data-stu-id="be769-105">Before you begin, make sure that the Invoice matching configuration key is selected.</span></span> 

<span data-ttu-id="be769-106">Na stránce Parametry závazků zajistěte, že je vybrána možnost Povolit ověření párování faktur, pole Zaúčtovat fakturu s odchylkami je nastaveno na Vyžadovat schválení a pole Zásady párování řádků je nastaveno na Třícestné párování.</span><span class="sxs-lookup"><span data-stu-id="be769-106">In the Accounts payable parameters page, ensure that the Enable invoice matching validation option is selected, the Post invoice with discrepancies field is set to Require approval, and the Line matching policy field is set to Three-way matching.</span></span>

<span data-ttu-id="be769-107">Tato procedura používá ukázkovou společnost USMF.</span><span class="sxs-lookup"><span data-stu-id="be769-107">This procedure uses the USMF demo company.</span></span> <span data-ttu-id="be769-108">Manažer závazků nebo osoba s rolí vedoucího účetnictví by prováděl tyto kroky.</span><span class="sxs-lookup"><span data-stu-id="be769-108">The accounts payable manager or accounting manager role would perform these steps.</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="be769-109">Vytvoření nákupní objednávky</span><span class="sxs-lookup"><span data-stu-id="be769-109">Create a purchase order</span></span>
1. <span data-ttu-id="be769-110">Přejděte na Všechny nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="be769-110">Go to All purchase orders.</span></span>
2. <span data-ttu-id="be769-111">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="be769-111">Click New.</span></span>
3. <span data-ttu-id="be769-112">V poli Účet dodavatele kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="be769-112">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="be769-113">Zadejte hodnotu do pole Účet dodavatele.</span><span class="sxs-lookup"><span data-stu-id="be769-113">In the Vendor account field, type a value.</span></span>
5. <span data-ttu-id="be769-114">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="be769-114">Click OK.</span></span>
6. <span data-ttu-id="be769-115">Klikněte na položku Přidat řádek.</span><span class="sxs-lookup"><span data-stu-id="be769-115">Click Add line.</span></span>
7. <span data-ttu-id="be769-116">Zadejte hodnotu do pole Číslo zboží.</span><span class="sxs-lookup"><span data-stu-id="be769-116">In the Item number field, type a value.</span></span>
8. <span data-ttu-id="be769-117">V podokně akcí klikněte na položku Nákup.</span><span class="sxs-lookup"><span data-stu-id="be769-117">On the Action Pane, click Purchase.</span></span>
9. <span data-ttu-id="be769-118">Klikněte na tlačítko Potvrdit.</span><span class="sxs-lookup"><span data-stu-id="be769-118">Click Confirm.</span></span>

## <a name="post-a-product-receipt"></a><span data-ttu-id="be769-119">Zaúčtování příjemky produktu</span><span class="sxs-lookup"><span data-stu-id="be769-119">Post a product receipt</span></span>
1. <span data-ttu-id="be769-120">V podokně akcí klikněte na položku Přijmout.</span><span class="sxs-lookup"><span data-stu-id="be769-120">On the Action Pane, click Receive.</span></span>
2. <span data-ttu-id="be769-121">Klikněte na položku Příjemka produktu.</span><span class="sxs-lookup"><span data-stu-id="be769-121">Click Product receipt.</span></span>
3. <span data-ttu-id="be769-122">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="be769-122">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="be769-123">Zadejte hodnotu do pole Příjemka produktu.</span><span class="sxs-lookup"><span data-stu-id="be769-123">In the Product receipt field, type a value.</span></span>
5. <span data-ttu-id="be769-124">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="be769-124">Click OK.</span></span>

## <a name="record-and-match-a-vendor-invoice-to-a-product-receipt"></a><span data-ttu-id="be769-125">Zaznamenání a párování faktury dodavatele s příjemkou produktu</span><span class="sxs-lookup"><span data-stu-id="be769-125">Record and match a vendor invoice to a product receipt</span></span>
1. <span data-ttu-id="be769-126">V podokně akcí klikněte na položku Faktura.</span><span class="sxs-lookup"><span data-stu-id="be769-126">On the Action Pane, click Invoice.</span></span>
2. <span data-ttu-id="be769-127">Klikněte na položku Faktura.</span><span class="sxs-lookup"><span data-stu-id="be769-127">Click Invoice.</span></span>
3. <span data-ttu-id="be769-128">Zadejte hodnotu do pole Číslo.</span><span class="sxs-lookup"><span data-stu-id="be769-128">In the Number field, type a value.</span></span>
4. <span data-ttu-id="be769-129">Kliknutím na Výchozí od: Objednané množství otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="be769-129">Click Default from: Ordered quantity to open the drop dialog.</span></span>
5. <span data-ttu-id="be769-130">Vyberte volbu v poli Výchozí množství pro řádky.</span><span class="sxs-lookup"><span data-stu-id="be769-130">In the Default quantity for lines field, select an option.</span></span>
6. <span data-ttu-id="be769-131">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="be769-131">Click OK.</span></span>
7. <span data-ttu-id="be769-132">Klepněte na tlačítko Ano.</span><span class="sxs-lookup"><span data-stu-id="be769-132">Click Yes.</span></span>
8. <span data-ttu-id="be769-133">Klikněte na Spárovat příjemky produktu.</span><span class="sxs-lookup"><span data-stu-id="be769-133">Click Match product receipts.</span></span>
9. <span data-ttu-id="be769-134">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="be769-134">Click OK.</span></span>
10. <span data-ttu-id="be769-135">V podokně akcí klikněte na položku Přehled.</span><span class="sxs-lookup"><span data-stu-id="be769-135">On the Action Pane, click Review.</span></span>
11. <span data-ttu-id="be769-136">Klikněte na položku Párování – podrobnosti.</span><span class="sxs-lookup"><span data-stu-id="be769-136">Click Matching details.</span></span>


