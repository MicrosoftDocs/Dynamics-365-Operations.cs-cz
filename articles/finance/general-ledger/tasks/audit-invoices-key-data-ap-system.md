---
title: Auditování faktur a klíčových dat pro závazky
description: Tohle téma popisuje, jako auditovat faktury a klíčová data pro závazky.
author: saraschi2
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
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5bb89f0adce41b045b1f573c4c0e841f78b2248c
ms.sourcegitcommit: 95d06006142e6bf83351fb075b413fdc2074d5ee
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/02/2020
ms.locfileid: "3761542"
---
# <a name="audit-invoices-and-key-data-in-accounts-payable"></a><span data-ttu-id="99ac0-103">Auditování faktur a klíčových dat pro závazky</span><span class="sxs-lookup"><span data-stu-id="99ac0-103">Audit invoices and key data in accounts payable</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="99ac0-104">Pokud od dodavatele obdržíte fakturu za zboží nebo služby na nákupní objednávce, mohou obchodní procesy vyžadovat, aby zboží nebo služby byly před schválením této faktury k platbě skutečně přijaty.</span><span class="sxs-lookup"><span data-stu-id="99ac0-104">When you receive an invoice from a vendor for goods or services on a purchase order, the business processes might require that the goods or services be received before the invoice can be approved for payment.</span></span> <span data-ttu-id="99ac0-105">Před prvním krokem ověřte, že je vybraný konfigurační klíč Párování faktur.</span><span class="sxs-lookup"><span data-stu-id="99ac0-105">Before you begin, make sure that the Invoice matching configuration key is selected.</span></span> 

<span data-ttu-id="99ac0-106">Na stránce **Parametry závazků** zajistěte, že je vybrána možnost Povolit ověření párování faktur, pole **Zaúčtovat fakturu s odchylkami** je nastaveno na **Vyžadovat schválení** a pole **Zásady párování řádků** je nastaveno na **Třícestné párování**.</span><span class="sxs-lookup"><span data-stu-id="99ac0-106">In the **Accounts payable parameters** page, ensure that the Enable invoice matching validation option is selected, the **Post invoice with discrepancies** field is set to **Require approval**, and the **Line matching policy** field is set to **Three-way matching**.</span></span>

<span data-ttu-id="99ac0-107">Tato procedura používá ukázkovou společnost USMF.</span><span class="sxs-lookup"><span data-stu-id="99ac0-107">This procedure uses the USMF demo company.</span></span> <span data-ttu-id="99ac0-108">Manažer závazků nebo osoba s rolí vedoucího účetnictví by prováděl tyto kroky.</span><span class="sxs-lookup"><span data-stu-id="99ac0-108">The accounts payable manager or accounting manager role would perform these steps.</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="99ac0-109">Vytvoření nákupní objednávky</span><span class="sxs-lookup"><span data-stu-id="99ac0-109">Create a purchase order</span></span>
1. <span data-ttu-id="99ac0-110">Přejděte na **Všechny nákupní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="99ac0-110">Go to **All purchase orders**.</span></span>
2. <span data-ttu-id="99ac0-111">Klepněte na možnost **Nový**.</span><span class="sxs-lookup"><span data-stu-id="99ac0-111">Click **New**.</span></span>
3. <span data-ttu-id="99ac0-112">Zadejte hodnotu do pole **Účet dodavatele**.</span><span class="sxs-lookup"><span data-stu-id="99ac0-112">In the **Vendor account** field, type a value.</span></span>
4. <span data-ttu-id="99ac0-113">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="99ac0-113">Click **OK**.</span></span>
5. <span data-ttu-id="99ac0-114">Klikněte na **Přidat řádek**.</span><span class="sxs-lookup"><span data-stu-id="99ac0-114">Click **Add line**.</span></span>
6. <span data-ttu-id="99ac0-115">Zadejte hodnotu do pole **Číslo zboží**.</span><span class="sxs-lookup"><span data-stu-id="99ac0-115">In the **Item number** field, type a value.</span></span>
7. <span data-ttu-id="99ac0-116">V podokně akcí klikněte na možnost **Zakoupit**.</span><span class="sxs-lookup"><span data-stu-id="99ac0-116">On the Action Pane, click **Purchase**.</span></span>
8. <span data-ttu-id="99ac0-117">Klikněte na tlačítko **Potvrdit**.</span><span class="sxs-lookup"><span data-stu-id="99ac0-117">Click **Confirm**.</span></span>

## <a name="post-a-product-receipt"></a><span data-ttu-id="99ac0-118">Zaúčtování příjemky produktu</span><span class="sxs-lookup"><span data-stu-id="99ac0-118">Post a product receipt</span></span>
1. <span data-ttu-id="99ac0-119">V podokně akcí klikněte na možnost **Přijmout**.</span><span class="sxs-lookup"><span data-stu-id="99ac0-119">On the Action Pane, click **Receive**.</span></span>
2. <span data-ttu-id="99ac0-120">Klikněte na **Příjemka produktu**.</span><span class="sxs-lookup"><span data-stu-id="99ac0-120">Click **Product receipt**.</span></span>
3. <span data-ttu-id="99ac0-121">Zadejte hodnotu do pole **Příjemka produktu**.</span><span class="sxs-lookup"><span data-stu-id="99ac0-121">In the **Product receipt** field, type a value.</span></span>
4. <span data-ttu-id="99ac0-122">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="99ac0-122">Click **OK**.</span></span>

## <a name="record-and-match-a-vendor-invoice-to-a-product-receipt"></a><span data-ttu-id="99ac0-123">Zaznamenání a párování faktury dodavatele s příjemkou produktu</span><span class="sxs-lookup"><span data-stu-id="99ac0-123">Record and match a vendor invoice to a product receipt</span></span>
1. <span data-ttu-id="99ac0-124">V podokně akcí klikněte na **Faktura > Faktura**.</span><span class="sxs-lookup"><span data-stu-id="99ac0-124">On the Action Pane, click **Invoice > Invoice**.</span></span>
2. <span data-ttu-id="99ac0-125">Zadejte hodnotu do pole **Číslo**.</span><span class="sxs-lookup"><span data-stu-id="99ac0-125">In the **Number** field, type a value.</span></span>
3. <span data-ttu-id="99ac0-126">Kliknutím na **Výchozí od: Objednané množství** otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="99ac0-126">Click **Default from: Ordered quantity** to open the drop dialog.</span></span>
4. <span data-ttu-id="99ac0-127">Vyberte možnost v poli **Výchozí množství pro řádky**.</span><span class="sxs-lookup"><span data-stu-id="99ac0-127">In the **Default quantity for lines** field, select an option.</span></span>
5. <span data-ttu-id="99ac0-128">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="99ac0-128">Click **OK**.</span></span>
6. <span data-ttu-id="99ac0-129">Klepněte na tlačítko **Ano**.</span><span class="sxs-lookup"><span data-stu-id="99ac0-129">Click **Yes**.</span></span>
7. <span data-ttu-id="99ac0-130">Klikněte na **Spárovat příjemky produktu**.</span><span class="sxs-lookup"><span data-stu-id="99ac0-130">Click **Match product receipts**.</span></span>
8. <span data-ttu-id="99ac0-131">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="99ac0-131">Click **OK**.</span></span>
9. <span data-ttu-id="99ac0-132">V podokně akcí klikněte na položku **Přehled**.</span><span class="sxs-lookup"><span data-stu-id="99ac0-132">On the Action Pane, click **Review**.</span></span>
10. <span data-ttu-id="99ac0-133">Klikněte na položku **Podrobnosti párování**.</span><span class="sxs-lookup"><span data-stu-id="99ac0-133">Click **Matching details**.</span></span>

