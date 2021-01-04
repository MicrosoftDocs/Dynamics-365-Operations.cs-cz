---
title: Platby částečných částek dodavatelem
description: Někdy provedete platbu dodavateli, která je nižší než částka faktury. Tento článek popisuje různé možnosti pro zvládnutí této situace.
author: abruer
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14321
ms.assetid: 9a17075e-5325-4d55-a1e5-1791b8c460a0
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 89e025977a0dcd40e35f17448a7b0ebde08cb6c8
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4440991"
---
# <a name="vendor-payments-for-a-partial-amount"></a><span data-ttu-id="02ebb-104">Platby částečných částek dodavatelem</span><span class="sxs-lookup"><span data-stu-id="02ebb-104">Vendor payments for a partial amount</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="02ebb-105">Někdy provedete platbu dodavateli, která je nižší než částka faktury.</span><span class="sxs-lookup"><span data-stu-id="02ebb-105">Sometimes, you might make a payment to a vendor that is less than the amount of an invoice.</span></span> <span data-ttu-id="02ebb-106">Tento článek popisuje různé možnosti pro zvládnutí této situace.</span><span class="sxs-lookup"><span data-stu-id="02ebb-106">This article describes the various options for handling this situation.</span></span> <span data-ttu-id="02ebb-107">Dostupné možnosti závisí na daných obchodních požadavcích a konfiguraci.</span><span class="sxs-lookup"><span data-stu-id="02ebb-107">The options that are available to you depend on your business requirements and configuration.</span></span> 

<a name="cash-discount-amounts"></a><span data-ttu-id="02ebb-108">Částka platebních slev</span><span class="sxs-lookup"><span data-stu-id="02ebb-108">Cash discount amounts</span></span>
---------------------

<span data-ttu-id="02ebb-109">Dodavatel vám může nabídnout platební slevu za úhradu faktury před datem splatnosti.</span><span class="sxs-lookup"><span data-stu-id="02ebb-109">A vendor can offer you a cash discount for paying an invoice before the due date.</span></span> <span data-ttu-id="02ebb-110">Například zadáte fakturu na částku 100,00, která určuje 2% platební slevu, pokud bude faktura zaplacena do 10 dní.</span><span class="sxs-lookup"><span data-stu-id="02ebb-110">For example, you enter an invoice for 100.00 that specifies a 2-percent cash discount if the invoice is paid within 10 days.</span></span> <span data-ttu-id="02ebb-111">Doba splatnosti dle podmínek je 30 dnů.</span><span class="sxs-lookup"><span data-stu-id="02ebb-111">The due date terms are 30 days.</span></span> <span data-ttu-id="02ebb-112">Pokud návrh platby používá jako kritérium pro výběr faktury platební slevu a k aktivaci návrhu dojde v den platební slevy nebo dříve, faktura se vybere k platbě a vytvoří se platba v částce 98,00.</span><span class="sxs-lookup"><span data-stu-id="02ebb-112">If a payment proposal uses the cash discount as a criterion for selecting an invoice, and if the proposal is run on or before the cash discount date, the invoice is selected for payment, and the payment is created for 98.00.</span></span> <span data-ttu-id="02ebb-113">Platební slevy lze také uplatnit jako ručně vytvořenou jednorázovou platbu.</span><span class="sxs-lookup"><span data-stu-id="02ebb-113">A cash discount can also be taken for a one-off payment that was created manually.</span></span>

## <a name="partial-payments-with-cash-discounts"></a><span data-ttu-id="02ebb-114">Částečné platby s platebními slevami</span><span class="sxs-lookup"><span data-stu-id="02ebb-114">Partial payments with cash discounts</span></span>
<span data-ttu-id="02ebb-115">Když provedete částečnou úhradu, můžete plánovat uskutečnění další částečné platby k úplnému vyrovnání faktury.</span><span class="sxs-lookup"><span data-stu-id="02ebb-115">When you make a partial payment, you might plan to make an additional partial payment to fully settle the invoice.</span></span> <span data-ttu-id="02ebb-116">Chcete-li aplikovat platební slevu za částečnou platbu, je nutné nastavit možnost **Vypočítat platební slevy pro částečné platby** na hodnotu **Ano** na stránce **Parametry pohledávky**.</span><span class="sxs-lookup"><span data-stu-id="02ebb-116">To take a cash discount for a partial payment, you must set the **Calculate cash discounts for partial payments** option to **Yes** on the **Account payable parameters** page.</span></span> 

<span data-ttu-id="02ebb-117">Například můžete přijmout platební slevu 2 %, pokud bude faktura proplacena do 10 dnů po vydání.</span><span class="sxs-lookup"><span data-stu-id="02ebb-117">For example, you receive a 2-percent cash discount if the invoice is paid within 10 days after it's issued.</span></span> <span data-ttu-id="02ebb-118">Je zaúčtována faktura na 100,00.</span><span class="sxs-lookup"><span data-stu-id="02ebb-118">An invoice is posted for 100.00.</span></span> <span data-ttu-id="02ebb-119">Pokud provedete platbu ve výši 49,00 do 10 dnů, zadáte do deníku plateb částku Má dáti ve výši 49,00.</span><span class="sxs-lookup"><span data-stu-id="02ebb-119">If you make a payment of 49.00 within 10 days, you enter a debit of 49.00 in a payment journal.</span></span> <span data-ttu-id="02ebb-120">Při vyrovnání částečné platby na stránce **Vyrovnat otevřené transakce** bude uvedena hodnota **1,00** v poli **Částka platební slevy k přijetí**.</span><span class="sxs-lookup"><span data-stu-id="02ebb-120">When you settle the partial payment on the **Settle open transactions** page, **1.00** appears in the **Cash discount amount to take** field.</span></span> 

> [!NOTE] 
> <span data-ttu-id="02ebb-121">Pokud zadáte částečnou platbu a ponecháte úplnou fakturovanou částku v poli **Částka k vyrovnání**, pole **Částka platební slevy k přijetí** bude automaticky přepočítáno při zaúčtování transakcí.</span><span class="sxs-lookup"><span data-stu-id="02ebb-121">If you enter a partial payment and leave the full invoice amount in the **Amount to settle** field, the **Cash discount amount to take** field is automatically recalculated when you post the transactions.</span></span>

## <a name="credit-notes-with-cash-discounts"></a><span data-ttu-id="02ebb-122">Dobropisy s platebními slevami</span><span class="sxs-lookup"><span data-stu-id="02ebb-122">Credit notes with cash discounts</span></span>
<span data-ttu-id="02ebb-123">Můžete vrátit některé položky na faktuře a přijmout dobropis.</span><span class="sxs-lookup"><span data-stu-id="02ebb-123">You might return some of the items on an invoice and receive a credit note.</span></span> <span data-ttu-id="02ebb-124">Pokud pro původní fakturu byla využita platební sleva, můžete odečíst hodnotu slevy a přijmout refundaci pro správnou částku.</span><span class="sxs-lookup"><span data-stu-id="02ebb-124">If a cash discount was taken on the original invoice, you can subtract the value of the discount and receive a refund for the correct amount.</span></span> <span data-ttu-id="02ebb-125">Pokud je možnost **Vypočítat platební slevy pro dobropisy** nastavena na hodnotu **Ano** na stránce **Parametry závazků**, sleva je automaticky vypočtena pro dobropis.</span><span class="sxs-lookup"><span data-stu-id="02ebb-125">If the **Calculate cash discounts for credit notes** option is set to **Yes** on the **Accounts payable parameters** page, the discount is automatically calculated for the credit note.</span></span> 

<span data-ttu-id="02ebb-126">Například můžete přijmout platební slevu 2 %, pokud bude faktura proplacena do 10 dnů po vydání.</span><span class="sxs-lookup"><span data-stu-id="02ebb-126">For example, you receive a 2-percent cash discount if the invoice is paid within 10 days after it's issued.</span></span> <span data-ttu-id="02ebb-127">Je zaúčtována faktura na 100,00.</span><span class="sxs-lookup"><span data-stu-id="02ebb-127">An invoice for 100.00 is posted.</span></span> <span data-ttu-id="02ebb-128">Pokud vrátíte zboží a obdržíte dobropis, můžete zadat dobropis za celou částku původní faktury (100,00) spolu s dvouprocentní platební slevou, která je v dobropisu také určena.</span><span class="sxs-lookup"><span data-stu-id="02ebb-128">If you return the goods and receive a credit note, you can enter the credit note for the full amount of the original invoice, 100.00, together with the 2-percent cash discount that is also defined on the credit memo.</span></span>  <span data-ttu-id="02ebb-129">Při prohlížení dobropisu na stránce **Vyrovnat transakce** se zobrazí částka **98,00** v poli **Částka k vyrovnání** a částka **-2,00** v poli **Částka platební slevy**.</span><span class="sxs-lookup"><span data-stu-id="02ebb-129">When you view the credit note on the **Settle transactions** page, **98.00** appears in the **Amount to settle** field, and **-2.00** appears in the **Cash discount amount** field.</span></span> <span data-ttu-id="02ebb-130">Částka slevy je zaúčtována na účet platební slevy.</span><span class="sxs-lookup"><span data-stu-id="02ebb-130">The discount amount is posted to a cash discount account.</span></span>

## <a name="overpaymentunderpayment-amounts"></a><span data-ttu-id="02ebb-131">Částky přeplatku nebo nedoplatku</span><span class="sxs-lookup"><span data-stu-id="02ebb-131">Overpayment/underpayment amounts</span></span>
<span data-ttu-id="02ebb-132">Můžete provést částečnou úhradu, když je částka, která musí být vyrovnána, příliš malá.</span><span class="sxs-lookup"><span data-stu-id="02ebb-132">You might make a partial payment where the amount that must still be settled is very small.</span></span> <span data-ttu-id="02ebb-133">Například faktura dodavatele je pro 1 000,00 a vy platíte 999,90</span><span class="sxs-lookup"><span data-stu-id="02ebb-133">For example, the vendor invoice is for 1,000.00, and you pay 999.90.</span></span> <span data-ttu-id="02ebb-134">Je-li zůstatek nižší než částka zadaná pro přeplatky nebo nedoplatky na stránce **Parametry závazků**, rozdíl se automaticky zaúčtuje na účet hlavní knihy pro přeplatky a nedoplatky.</span><span class="sxs-lookup"><span data-stu-id="02ebb-134">If the remaining amount is less than the amount that is specified for overpayments or underpayments on the **Accounts payable parameters** page, the difference is automatically posted to an overpayment/underpayment ledger account.</span></span>


<span data-ttu-id="02ebb-135">Další informace naleznete v tématu [Přehled plateb dodavatele](../cash-bank-management/tasks/vendor-payment-overview.md).</span><span class="sxs-lookup"><span data-stu-id="02ebb-135">For more information, see [Vendor payment overview](../cash-bank-management/tasks/vendor-payment-overview.md).</span></span>
