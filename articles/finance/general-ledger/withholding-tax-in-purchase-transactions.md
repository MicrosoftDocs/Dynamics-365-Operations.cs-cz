---
title: Srážková daň v nákupních transakcích
description: U prodejců, kteří podléhají srážkové dani, můžete přiřadit výchozí **Skupinu srážkové daně** na stránce **Všichni dodavatelé**.
author: roschlom
manager: AnnBe
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2020-01-12
ms.dyn365.ops.version: AX 10.0.16
ms.openlocfilehash: 06997e2d6b47d867e014a7d493d91015c78a5e04
ms.sourcegitcommit: 630a0b3f800f36ced49b79156dd52132904fef75
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/25/2021
ms.locfileid: "5060709"
---
# <a name="withholding-tax-in-purchase-transactions"></a><span data-ttu-id="9f23e-103">Srážková daň v nákupních transakcích</span><span class="sxs-lookup"><span data-stu-id="9f23e-103">Withholding tax in purchase transactions</span></span>

<span data-ttu-id="9f23e-104">U prodejců, kteří podléhají srážkové dani, můžete přiřadit výchozí **Skupinu srážkové daně** na stránce **Všichni dodavatelé**.</span><span class="sxs-lookup"><span data-stu-id="9f23e-104">For vendors who are liable to withholding tax, you can assign the default **Withholding tax group** on the **All vendors** page.</span></span>

1. <span data-ttu-id="9f23e-105">Přejděte na **Navigační podokno > Moduly > Závazky > Dodavatelé > Všichni dodavatelé**.</span><span class="sxs-lookup"><span data-stu-id="9f23e-105">Go to **Navigation pane > Modules > Accounts payable > Vendors > All vendors**.</span></span>

2. <span data-ttu-id="9f23e-106">Klikněte na příslušný účet dodavatele, klikněte na **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="9f23e-106">Click the respective Vendor account, click **Edit**.</span></span>

3. <span data-ttu-id="9f23e-107">Na kartě **Faktura a doručení** nastavte pole **Vypočítat srážkovou daň** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="9f23e-107">In **Invoice and delivery** tab, set the **Calculate withholding tax** field to **Yes**.</span></span>

   > [!NOTE] 
   > <span data-ttu-id="9f23e-108">Srážková daň se nebude počítat, pokud není možnost **Vypočítat srážkovou daň** pro tohoto dodavatele v datech zapnutá.</span><span class="sxs-lookup"><span data-stu-id="9f23e-108">Withholding tax will not be calculated if **Calculate withholding tax** is not switched on for this vendor in the data.</span></span>

4. <span data-ttu-id="9f23e-109">Vyberte skupinu srážkové daně ve **Skupině srážkové daně**.</span><span class="sxs-lookup"><span data-stu-id="9f23e-109">Select a withholding tax group in **Withholding tax group**.</span></span>

5. <span data-ttu-id="9f23e-110">Klikněte na možnost **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="9f23e-110">Click **Save**.</span></span>

<span data-ttu-id="9f23e-111">U položek / služeb, které podléhají srážkové dani, můžete přiřadit výchozí **Skupinu srážkové daně položky** ve volbě **Uvolněné produkty**.</span><span class="sxs-lookup"><span data-stu-id="9f23e-111">For items/services which are liable to withholding tax, you can assign the default **Item withholding tax group** in **Released Products**.</span></span>

1. <span data-ttu-id="9f23e-112">Klikněte na **Navigační podokno > Moduly > Řízení informací o produktech > Produkty > Vydané produkty**.</span><span class="sxs-lookup"><span data-stu-id="9f23e-112">Go to **Navigation pane > Modules > Product information management > Products > Released products**.</span></span>

2. <span data-ttu-id="9f23e-113">Klikněte na příslušné číslo položky, klikněte na **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="9f23e-113">Click the respective Item number, click **Edit**.</span></span>

3. <span data-ttu-id="9f23e-114">Na kartě **Nákup** klikněte na **Vypočítat srážkovou daň**.</span><span class="sxs-lookup"><span data-stu-id="9f23e-114">In **Purchase** tab, click **Calculate withholding tax**.</span></span>

   > [!NOTE] 
   > <span data-ttu-id="9f23e-115">Srážková daň se nebude počítat, pokud není volba **Vypočítat srážkovou daň** nastavena na **Ano** pro tuto položku na kartě **Nákup** na stránce **Uvolněný produkt**.</span><span class="sxs-lookup"><span data-stu-id="9f23e-115">Withholding tax will not be calculated if **Calculate withholding tax** isn't set to **Yes** for this Item in the **Purchase** tab on the **Released product** page.</span></span>

4. <span data-ttu-id="9f23e-116">Vyberte položku skupiny srážkové daně v seznamu **Skupina srážkové daně položky**.</span><span class="sxs-lookup"><span data-stu-id="9f23e-116">Select an item withholding tax group in **Item withholding tax group** list.</span></span>

5. <span data-ttu-id="9f23e-117">Klikněte na možnost **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="9f23e-117">Click **Save**.</span></span>

<span data-ttu-id="9f23e-118">Skupiny srážkové daně a Skupiny srážkové daně položky lze přiřadit na stránkách:</span><span class="sxs-lookup"><span data-stu-id="9f23e-118">Withholding tax groups and Item withholding tax groups can be assigned in pages:</span></span> 

- <span data-ttu-id="9f23e-119">**Nákupní objednávka**</span><span class="sxs-lookup"><span data-stu-id="9f23e-119">**Purchase order**</span></span>
- <span data-ttu-id="9f23e-120">**Faktury dodavatele**</span><span class="sxs-lookup"><span data-stu-id="9f23e-120">**Vendor invoice**</span></span>
- <span data-ttu-id="9f23e-121">**Deník faktur**</span><span class="sxs-lookup"><span data-stu-id="9f23e-121">**Invoice journal**</span></span>

<span data-ttu-id="9f23e-122">Výchozí skupina srážkové daně a skupina srážkové daně položky budou při vytváření **Nákupních objednávek** a/nebo **Nevyřízených faktur dodavatele** přeneseny do řádků.</span><span class="sxs-lookup"><span data-stu-id="9f23e-122">The default Withholding tax group and Item withholding tax group will be carried into the lines when creating **Purchase orders** and/or **Pending Vendor invoices**.</span></span> <span data-ttu-id="9f23e-123">Pro **Deník faktur dodavatele** můžete zapnout možnost **Vypočítat srážkovou daň** a vybrat **Skupinu srážkové daně položky** na kartě **Obecné** v deníku.</span><span class="sxs-lookup"><span data-stu-id="9f23e-123">For **Vendor invoice journal**, you can switch on **Calculate withholding tax** and select **Item withholding tax group** in the **General** tab in the journal.</span></span>

<span data-ttu-id="9f23e-124">Dočasná částka srážkové daně je k dispozici v poli **Upravená srážková daň** na kartě **Součty** na stránce **Nákupní objednávka**.</span><span class="sxs-lookup"><span data-stu-id="9f23e-124">The temporary amount of withholding tax is available in the field **Adjusted withholding tax** of the **Totals** tab on the **Purchase order** page.</span></span>

![V nákupní objednávce je zahrnuta srážková daň](media/withholding-tax-adjusted.png)

<span data-ttu-id="9f23e-126">Srážková daň se počítá v **Deníku plateb dodavatele**.</span><span class="sxs-lookup"><span data-stu-id="9f23e-126">Withholding tax is calculated on **Vendor payment journal**.</span></span> <span data-ttu-id="9f23e-127">Můžete ručně upravit příslušné kódy srážkové daně i skutečné částky srážkové daně na kartě **Srážková daň** na stránce **Vypořádat transakce**.</span><span class="sxs-lookup"><span data-stu-id="9f23e-127">You can manually adjust the applicable withholding tax codes as well as the actual withholding tax amounts in the **Withholding tax** tab on the **Settle transactions** page.</span></span>

![Srážky lze ručně upravit na stránce Vyrovnat transakce](media/withholding-tax-vendor-payment-tab.png)

<span data-ttu-id="9f23e-129">Odvozená částka srážkové daně bude odečtena z platby dodavatele a zaúčtována na **Účet srážkové daně** v souvisejícím dokladu.</span><span class="sxs-lookup"><span data-stu-id="9f23e-129">The derived withholding tax amount will be deducted from the vendor payment and posted to the **Withholding tax account** in a related voucher.</span></span>

![Účet srážkové daně zobrazující související dokument](media/withholding-tax-adjusted.png)
