---
title: Zaznamenání faktury dodavatele a spárování s přijatým množstvím
description: Pokud od dodavatele obdržíte fakturu za zboží nebo služby na nákupní objednávce, mohou obchodní procesy vyžadovat, aby zboží nebo služby byly před schválením této faktury k platbě skutečně přijaty.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, PurchEditLines, VendEditInvoice, VendEditInvoiceDefaultQuantityForLinesDropDialog,  VendJournalMatch_PackingSlip, VendInvoiceMatchingDetails
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 66d84f497775ce4f988242dd2b327bf4854faef5
ms.sourcegitcommit: ba1c76497acc9afba85257976f0d4e96836871d1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/04/2019
ms.locfileid: "2890412"
---
# <a name="record-vendor-invoice-and-match-against-received-quantity"></a><span data-ttu-id="0901b-103">Zaznamenání faktury dodavatele a spárování s přijatým množstvím</span><span class="sxs-lookup"><span data-stu-id="0901b-103">Record vendor invoice and match against received quantity</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0901b-104">Pokud od dodavatele obdržíte fakturu za zboží nebo služby na nákupní objednávce, mohou obchodní procesy vyžadovat, aby zboží nebo služby byly před schválením této faktury k platbě skutečně přijaty.</span><span class="sxs-lookup"><span data-stu-id="0901b-104">When you receive an invoice from a vendor for goods or services on a purchase order, the business processes might require that the goods or services be received before the invoice can be approved for payment.</span></span> <span data-ttu-id="0901b-105">Před prvním krokem ověřte, že je vybraný konfigurační klíč Párování faktur.</span><span class="sxs-lookup"><span data-stu-id="0901b-105">Before you begin, make sure that the Invoice matching configuration key is selected.</span></span> 

<span data-ttu-id="0901b-106">Na stránce Parametry závazků zajistěte, že je vybrána možnost Povolit ověření párování faktur, pole Zaúčtovat fakturu s odchylkami je nastaveno na Vyžadovat schválení a pole Zásady párování řádků je nastaveno na Třícestné párování.</span><span class="sxs-lookup"><span data-stu-id="0901b-106">In the Accounts payable parameters page, ensure that the Enable invoice matching validation option is selected, the Post invoice with discrepancies field is set to Require approval, and the Line matching policy field is set to Three-way matching.</span></span>

<span data-ttu-id="0901b-107">Tato procedura používá ukázkovou společnost USMF.</span><span class="sxs-lookup"><span data-stu-id="0901b-107">This procedure uses the USMF demo company.</span></span> <span data-ttu-id="0901b-108">Manažer závazků nebo osoba s rolí vedoucího účetnictví by prováděl tyto kroky.</span><span class="sxs-lookup"><span data-stu-id="0901b-108">The accounts payable manager or accounting manager role would perform these steps.</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="0901b-109">Vytvoření nákupní objednávky</span><span class="sxs-lookup"><span data-stu-id="0901b-109">Create a purchase order</span></span>
1. <span data-ttu-id="0901b-110">Přejděte na Všechny nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="0901b-110">Go to All purchase orders.</span></span>
2. <span data-ttu-id="0901b-111">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="0901b-111">Click New.</span></span>
3. <span data-ttu-id="0901b-112">V poli Účet dodavatele kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="0901b-112">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="0901b-113">Zadejte hodnotu do pole Účet dodavatele.</span><span class="sxs-lookup"><span data-stu-id="0901b-113">In the Vendor account field, type a value.</span></span>
5. <span data-ttu-id="0901b-114">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="0901b-114">Click OK.</span></span>
6. <span data-ttu-id="0901b-115">Klikněte na položku Přidat řádek.</span><span class="sxs-lookup"><span data-stu-id="0901b-115">Click Add line.</span></span>
7. <span data-ttu-id="0901b-116">Zadejte hodnotu do pole Číslo zboží.</span><span class="sxs-lookup"><span data-stu-id="0901b-116">In the Item number field, type a value.</span></span>
8. <span data-ttu-id="0901b-117">V podokně akcí klikněte na položku Nákup.</span><span class="sxs-lookup"><span data-stu-id="0901b-117">On the Action Pane, click Purchase.</span></span>
9. <span data-ttu-id="0901b-118">Klikněte na tlačítko Potvrdit.</span><span class="sxs-lookup"><span data-stu-id="0901b-118">Click Confirm.</span></span>

## <a name="post-a-product-receipt"></a><span data-ttu-id="0901b-119">Zaúčtování příjemky produktu</span><span class="sxs-lookup"><span data-stu-id="0901b-119">Post a product receipt</span></span>
1. <span data-ttu-id="0901b-120">V podokně akcí klikněte na položku Přijmout.</span><span class="sxs-lookup"><span data-stu-id="0901b-120">On the Action Pane, click Receive.</span></span>
2. <span data-ttu-id="0901b-121">Klikněte na položku Příjemka produktu.</span><span class="sxs-lookup"><span data-stu-id="0901b-121">Click Product receipt.</span></span>
3. <span data-ttu-id="0901b-122">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="0901b-122">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="0901b-123">Zadejte hodnotu do pole Příjemka produktu.</span><span class="sxs-lookup"><span data-stu-id="0901b-123">In the Product receipt field, type a value.</span></span>
5. <span data-ttu-id="0901b-124">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="0901b-124">Click OK.</span></span>

## <a name="record-and-match-a-vendor-invoice-to-a-product-receipt"></a><span data-ttu-id="0901b-125">Zaznamenání a párování faktury dodavatele s příjemkou produktu</span><span class="sxs-lookup"><span data-stu-id="0901b-125">Record and match a vendor invoice to a product receipt</span></span>
1. <span data-ttu-id="0901b-126">V podokně akcí klikněte na položku Faktura.</span><span class="sxs-lookup"><span data-stu-id="0901b-126">On the Action Pane, click Invoice.</span></span>
2. <span data-ttu-id="0901b-127">Klikněte na položku Faktura.</span><span class="sxs-lookup"><span data-stu-id="0901b-127">Click Invoice.</span></span>
3. <span data-ttu-id="0901b-128">Zadejte hodnotu do pole Číslo.</span><span class="sxs-lookup"><span data-stu-id="0901b-128">In the Number field, type a value.</span></span>
4. <span data-ttu-id="0901b-129">Kliknutím na Výchozí od: Objednané množství otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="0901b-129">Click Default from: Ordered quantity to open the drop dialog.</span></span>
5. <span data-ttu-id="0901b-130">Vyberte volbu v poli Výchozí množství pro řádky.</span><span class="sxs-lookup"><span data-stu-id="0901b-130">In the Default quantity for lines field, select an option.</span></span>
6. <span data-ttu-id="0901b-131">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="0901b-131">Click OK.</span></span>
7. <span data-ttu-id="0901b-132">Klepněte na tlačítko Ano.</span><span class="sxs-lookup"><span data-stu-id="0901b-132">Click Yes.</span></span>
8. <span data-ttu-id="0901b-133">Klikněte na Spárovat příjemky produktu.</span><span class="sxs-lookup"><span data-stu-id="0901b-133">Click Match product receipts.</span></span>
9. <span data-ttu-id="0901b-134">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="0901b-134">Click OK.</span></span>
10. <span data-ttu-id="0901b-135">V podokně akcí klikněte na položku Přehled.</span><span class="sxs-lookup"><span data-stu-id="0901b-135">On the Action Pane, click Review.</span></span>
11. <span data-ttu-id="0901b-136">Klikněte na položku Párování – podrobnosti.</span><span class="sxs-lookup"><span data-stu-id="0901b-136">Click Matching details.</span></span>

