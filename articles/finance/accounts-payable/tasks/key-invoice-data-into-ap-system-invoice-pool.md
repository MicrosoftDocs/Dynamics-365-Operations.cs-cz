---
title: Zadání dat faktury do systému závazků s použitím evidence faktur
description: Tohle téma popisuje použití registru faktur k vytváření faktur.
author: abruer
manager: AnnBe
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 670dd2ec15aa26791758ec4bea2b431482499436
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5227153"
---
# <a name="key-invoice-data-into-the-ap-system-using-invoice-pool"></a><span data-ttu-id="bde36-103">Zadání dat faktury do systému závazků s použitím evidence faktur</span><span class="sxs-lookup"><span data-stu-id="bde36-103">Key invoice data into the AP system using invoice pool</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bde36-104">Tohle téma popisuje použití registru faktur k vytváření faktur.</span><span class="sxs-lookup"><span data-stu-id="bde36-104">This topic describes how to use the invoice register to create invoices.</span></span> <span data-ttu-id="bde36-105">Potom použije evidenci faktur pro spárování faktury s nákupní objednávkou a dokončení výdajů na stránce faktury dodavatele.</span><span class="sxs-lookup"><span data-stu-id="bde36-105">Then use the invoice pool to match the invoice to a purchase order and finalize the expense in the vendor invoice page.</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="bde36-106">Vytvoření nákupní objednávky</span><span class="sxs-lookup"><span data-stu-id="bde36-106">Create a purchase order</span></span>
1. <span data-ttu-id="bde36-107">V navigačním podokně přejděte na **Moduly > Závazky > Nákupní objednávky > Nákupní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="bde36-107">In the navigation pane, go to **Modules > Accounts payable > Purchase orders > Purchase orders**.</span></span>
2. <span data-ttu-id="bde36-108">Klepnutím na možnost **Nová** vytvořte novou objednávku.</span><span class="sxs-lookup"><span data-stu-id="bde36-108">Select **New** to create a purchase order.</span></span>
3. <span data-ttu-id="bde36-109">V poli **Účet dodavatele** v rozevíracím seznamu vyberte dodavatele.</span><span class="sxs-lookup"><span data-stu-id="bde36-109">In the **Vendor account** field, select a vendor for the drop-down list.</span></span> <span data-ttu-id="bde36-110">Vyberte například dodavatele **1001**.</span><span class="sxs-lookup"><span data-stu-id="bde36-110">For example, select vendor **1001**.</span></span>
4. <span data-ttu-id="bde36-111">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="bde36-111">Select **OK**.</span></span>
5. <span data-ttu-id="bde36-112">V poli **Číslo položky** vyberte z rozevíracího seznamu číslo položky služeb.</span><span class="sxs-lookup"><span data-stu-id="bde36-112">In the **Item number** field, select the services item number in the drop-down list.</span></span> <span data-ttu-id="bde36-113">Vyberte například **S0001**.</span><span class="sxs-lookup"><span data-stu-id="bde36-113">For example, select **S0001**.</span></span> <span data-ttu-id="bde36-114">Čistá částka je 75,00.</span><span class="sxs-lookup"><span data-stu-id="bde36-114">The net amount is 75.00.</span></span>  <span data-ttu-id="bde36-115">Jedná se o částku, která se očekává na faktuře.</span><span class="sxs-lookup"><span data-stu-id="bde36-115">That is the amount that we will expect on the invoice.</span></span>  
6. <span data-ttu-id="bde36-116">V podokně akcí klikněte na možnost **Zakoupit**.</span><span class="sxs-lookup"><span data-stu-id="bde36-116">On the action pane, select **Purchase**.</span></span>
7. <span data-ttu-id="bde36-117">Vyberte **Potvrdit**.</span><span class="sxs-lookup"><span data-stu-id="bde36-117">Select **Confirm**.</span></span>

## <a name="create-and-post-and-invoice"></a><span data-ttu-id="bde36-118">Vytvoření a zaúčtování faktury</span><span class="sxs-lookup"><span data-stu-id="bde36-118">Create and post and invoice</span></span>
1. <span data-ttu-id="bde36-119">V navigačním podokně přejděte na **Moduly > Závazky > Faktury > Registr faktur**.</span><span class="sxs-lookup"><span data-stu-id="bde36-119">In the navigation pane, go to **Modules > Accounts payable > Invoices > Invoice register**.</span></span>
2. <span data-ttu-id="bde36-120">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="bde36-120">Select **New**.</span></span>
3. <span data-ttu-id="bde36-121">Otevřete vyhledávání a vyberte název registru faktury, který chcete použít.</span><span class="sxs-lookup"><span data-stu-id="bde36-121">Open the lookup to select the name of the invoice register that you want to use.</span></span>
4. <span data-ttu-id="bde36-122">Vyberte název registru faktury, který chcete použít.</span><span class="sxs-lookup"><span data-stu-id="bde36-122">Select the name of the invoice register that you want to use.</span></span>
5. <span data-ttu-id="bde36-123">Kliknutím na **Řádky** otevřete registr a zadejte řádky výdajů.</span><span class="sxs-lookup"><span data-stu-id="bde36-123">Select **Lines** to open the register and enter expense lines.</span></span>
6. <span data-ttu-id="bde36-124">Ve vyhledávání vyberte dodavatele.</span><span class="sxs-lookup"><span data-stu-id="bde36-124">In the lookup, select a vendor.</span></span> <span data-ttu-id="bde36-125">Vyberte například dodavatele **1001**.</span><span class="sxs-lookup"><span data-stu-id="bde36-125">For example, select vendor **1001**.</span></span>
7. <span data-ttu-id="bde36-126">Do pole **Faktura** zadejte číslo faktury.</span><span class="sxs-lookup"><span data-stu-id="bde36-126">In the **Invoice** field, enter the invoice number.</span></span>
8. <span data-ttu-id="bde36-127">Zadejte hodnotu do pole **Popis**.</span><span class="sxs-lookup"><span data-stu-id="bde36-127">In the **Description** field, type a value.</span></span>
9. <span data-ttu-id="bde36-128">V poli **Dobropis** zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="bde36-128">In the **Credit** field, enter a number.</span></span>
10. <span data-ttu-id="bde36-129">V poli **Nákupní objednávka** otevřete rozevírací seznam a vyberte nákupní objednávku, kterou jste dříve vytvořili.</span><span class="sxs-lookup"><span data-stu-id="bde36-129">In the **Purchase order** field, open the drop-down list to select the purchase order that you created earlier.</span></span>
11. <span data-ttu-id="bde36-130">V poli **Schválil/a** zvýrazněte schvalujícího v rozevíracím seznamu a kliknutím na tlačítko **Vybrat** vyberte tohoto schvalujícího.</span><span class="sxs-lookup"><span data-stu-id="bde36-130">In the **Approved by** field, highlight an approver in the drop-down list and click **Select** to select that approver.</span></span>
12. <span data-ttu-id="bde36-131">Zvolte **Zaúčtovat**.</span><span class="sxs-lookup"><span data-stu-id="bde36-131">Select **Post**.</span></span>

## <a name="open-an-invoice-from-the-pool-and-match-it-to-a-purchase-order-to-complete-the-invoice-process"></a><span data-ttu-id="bde36-132">otevřete fakturu z evidence a spárujte ji s nákupní objednávkou pro dokončení procesu fakturace</span><span class="sxs-lookup"><span data-stu-id="bde36-132">Open an invoice from the pool and match it to a purchase order to complete the invoice process</span></span>
1. <span data-ttu-id="bde36-133">V navigačním podokně přejděte na **Moduly > Závazky > Faktury > Evidence faktur**.</span><span class="sxs-lookup"><span data-stu-id="bde36-133">In the navigation pane, go to **Modules > Accounts payable > Invoices > Invoice pool**.</span></span>
2. <span data-ttu-id="bde36-134">Kliknutím na možnost **Nákupní objednávka** vytvořte fakturu dodavatele z faktury v evidenci.</span><span class="sxs-lookup"><span data-stu-id="bde36-134">Select **Purchase order** to create a vendor invoice from the invoice in the pool.</span></span>
3. <span data-ttu-id="bde36-135">Vyberte fakturu, kterou chcete zkontrolovat.</span><span class="sxs-lookup"><span data-stu-id="bde36-135">Select the invoice that you want to review.</span></span>
4. <span data-ttu-id="bde36-136">Kliknutím na možnost **Aktualizovat stav párování** dokončete párování.</span><span class="sxs-lookup"><span data-stu-id="bde36-136">Select **Update match status** to complete the matching.</span></span>
5. <span data-ttu-id="bde36-137">V podokně akcí vyberte **Možnosti**.</span><span class="sxs-lookup"><span data-stu-id="bde36-137">On the action pane, select **Options**.</span></span>
6. <span data-ttu-id="bde36-138">Vyberte **Změnit zobrazení**.</span><span class="sxs-lookup"><span data-stu-id="bde36-138">Select **Change view**.</span></span>
7. <span data-ttu-id="bde36-139">Vyberte **Zobrazení mřížky**.</span><span class="sxs-lookup"><span data-stu-id="bde36-139">Select **Grid view**.</span></span>
8. <span data-ttu-id="bde36-140">Zvolte **Zaúčtovat**.</span><span class="sxs-lookup"><span data-stu-id="bde36-140">Select **Post**.</span></span>
9. <span data-ttu-id="bde36-141">Zavřete formulář.</span><span class="sxs-lookup"><span data-stu-id="bde36-141">Close the form.</span></span>
10. <span data-ttu-id="bde36-142">V navigačním podokně přejděte na **Moduly > Závazky > Dodavatelé > Dodavatelé**.</span><span class="sxs-lookup"><span data-stu-id="bde36-142">In the navigation pane, go to **Modules > Accounts payable > Vendors > Vendors**.</span></span>
11. <span data-ttu-id="bde36-143">Vyberte dodavatele, který se nacházel na nákupní objednávce.</span><span class="sxs-lookup"><span data-stu-id="bde36-143">Select the vendor that was on the purchase order.</span></span> <span data-ttu-id="bde36-144">Vyberte například dodavatele **1001**.</span><span class="sxs-lookup"><span data-stu-id="bde36-144">For example, select vendor **1001**.</span></span>
12. <span data-ttu-id="bde36-145">V podokně akcí vyberte možnost **Dodavatel**.</span><span class="sxs-lookup"><span data-stu-id="bde36-145">On the action pane, select **Vendor**.</span></span>
13. <span data-ttu-id="bde36-146">Vyberte **Transakce**.</span><span class="sxs-lookup"><span data-stu-id="bde36-146">Select **Transactions**.</span></span>
14. <span data-ttu-id="bde36-147">Vyberte fakturu, kterou jste vytvořili.</span><span class="sxs-lookup"><span data-stu-id="bde36-147">Select the invoice that you created.</span></span> <span data-ttu-id="bde36-148">Časové rozlišení registru faktur bylo stornováno a zaúčtováno na příslušný účet výdajů.</span><span class="sxs-lookup"><span data-stu-id="bde36-148">The invoice register accrual was reversed and posted to the appropriate expense account.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]