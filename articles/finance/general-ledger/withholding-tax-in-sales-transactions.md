---
title: Srážková daň v prodejních transakcích
description: Toto téma uvádí kroky, jak se vyhnout výpočtu srážkové daně u vybraných zákazníků. Zákazníkům, kteří ve svých platbách ve váš prospěch určují srážkovou daň, můžete přiřadit výchozí skupinu srážkové daně.
author: roschlom
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 8e11ce10faa9b450b6f36a856b34b06b4ee1838d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5842337"
---
# <a name="withholding-tax-in-sales-transactions"></a><span data-ttu-id="cdf75-104">Srážková daň v prodejních transakcích</span><span class="sxs-lookup"><span data-stu-id="cdf75-104">Withholding tax in sales transactions</span></span>

<span data-ttu-id="cdf75-105">Toto téma uvádí kroky, jak se vyhnout výpočtu srážkové daně u vybraných zákazníků.</span><span class="sxs-lookup"><span data-stu-id="cdf75-105">This topic lists the steps for avoiding the calculation of withholding tax for selected customers.</span></span> <span data-ttu-id="cdf75-106">Zákazníkům, kteří ve svých platbách ve váš prospěch určují srážkovou daň, můžete přiřadit výchozí **Skupinu srážkové daně** na stránce **Odběratelé**.</span><span class="sxs-lookup"><span data-stu-id="cdf75-106">For customers who specify withholding tax in their payments to you, you can assign the default **Withholding tax group** on the **Customers** page.</span></span> 

1. <span data-ttu-id="cdf75-107">Přejděte na **Navigační podokno > Moduly > Pohledávky > Odběratelé > Všichni odběratelé**.</span><span class="sxs-lookup"><span data-stu-id="cdf75-107">Go to **Navigation pane > Modules > Accounts receivable > Customers > All customers**.</span></span>

2. <span data-ttu-id="cdf75-108">Klikněte na příslušný účet odběratele, klikněte na **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="cdf75-108">Click the respective customer account, click **Edit**.</span></span>

3. <span data-ttu-id="cdf75-109">Na kartě **Faktura a doručení** nastavte pole **Vypočítat srážkovou daň** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="cdf75-109">In the **Invoice and delivery** tab, set the **Calculate withholding tax** field to **Yes**.</span></span>

   > [!NOTE] 
   > <span data-ttu-id="cdf75-110">Srážková daň se nebude počítat, pokud není možnost **Vypočítat srážkovou daň** pro tohoto odběratele v zapnutá v hlavních datech.</span><span class="sxs-lookup"><span data-stu-id="cdf75-110">Withholding tax will not be calculated if **Calculate withholding tax** is not switched on for this customer in the master data.</span></span>

4. <span data-ttu-id="cdf75-111">Vyberte skupinu srážkové daně ve **Skupině srážkové daně**.</span><span class="sxs-lookup"><span data-stu-id="cdf75-111">Select a withholding tax group in **Withholding tax group**.</span></span>

5. <span data-ttu-id="cdf75-112">Klikněte na možnost **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="cdf75-112">Click **Save**.</span></span>

<span data-ttu-id="cdf75-113">U položek / služeb, které podléhají srážkové dani, můžete přiřadit výchozí **Skupinu srážkové daně položky** ve volbě **Uvolněné produkty**.</span><span class="sxs-lookup"><span data-stu-id="cdf75-113">For items/services, which are liable to withholding tax, you can assign the default **Item withholding tax group** in **Released Products**.</span></span>

1. <span data-ttu-id="cdf75-114">Klikněte na **Navigační podokno > Moduly > Řízení informací o produktech > Produkty > Vydané produkty**.</span><span class="sxs-lookup"><span data-stu-id="cdf75-114">Go to **Navigation pane > Modules > Product information management > Products > Released products**.</span></span>

2. <span data-ttu-id="cdf75-115">Klikněte na příslušné číslo položky, klikněte na **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="cdf75-115">Click the respective Item number, click **Edit**.</span></span>

3. <span data-ttu-id="cdf75-116">Na kartě **Prodej** klikněte na **Vypočítat srážkovou daň**.</span><span class="sxs-lookup"><span data-stu-id="cdf75-116">In the **Sell** tab, click **Calculate withholding tax**.</span></span>

   > [!NOTE] 
   > <span data-ttu-id="cdf75-117">Srážková daň se nebude počítat, pokud není volba **Vypočítat srážkovou daň** nastavena na **Ano** pro tuto položku na kartě **Prodej** na stránce **Uvolněný produkt**.</span><span class="sxs-lookup"><span data-stu-id="cdf75-117">Withholding tax will not be calculated if **Calculate withholding tax** is not set to **Yes** for this Item in the **Sell** tab on the **Released product** page.</span></span>

4. <span data-ttu-id="cdf75-118">Vyberte položku skupiny srážkové daně v seznamu **Skupina srážkové daně položky**.</span><span class="sxs-lookup"><span data-stu-id="cdf75-118">Select an Item withholding tax group in **Item withholding tax group** list.</span></span>

5. <span data-ttu-id="cdf75-119">Klikněte na možnost **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="cdf75-119">Click **Save**.</span></span>

<span data-ttu-id="cdf75-120">Skupiny srážkové daně a Skupiny srážkové daně položky lze přiřadit pomocí stránky **Prodejní objednávka**.</span><span class="sxs-lookup"><span data-stu-id="cdf75-120">Withholding tax groups and Item withholding tax groups can be assigned using the **Sales order** page.</span></span> 

<span data-ttu-id="cdf75-121">Výchozí skupina srážkové daně a skupina srážkové daně položky se použijí jako výchozí záznamy na řádcích prodejní objednávky při vytváření nové prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="cdf75-121">The default Withholding tax group and Item withholding tax group will be used as default entries on sales order lines when you create a new sales order.</span></span>

<span data-ttu-id="cdf75-122">Srážková daň se vypočítá a zaúčtuje s **Deníkem plateb odběratele**.</span><span class="sxs-lookup"><span data-stu-id="cdf75-122">Withholding tax is calculated and posted with **Customer payment journal**.</span></span> <span data-ttu-id="cdf75-123">Můžete ručně upravit příslušný kód srážkové daně i skutečnou částku srážkové daně na kartě **Srážková daň** na stránce **Vypořádat transakce**.</span><span class="sxs-lookup"><span data-stu-id="cdf75-123">You can manually adjust the applicable withholding tax code, as well as the actual withholding tax amount in the **Withholding tax** tab on the **Settle transactions** page.</span></span>

<span data-ttu-id="cdf75-124">Vypočtená částka srážkové daně bude odečtena z platby odběratele a zaúčtována na **Protiúčet srážkové daně** v souvisejícím dokladu.</span><span class="sxs-lookup"><span data-stu-id="cdf75-124">The calculated withholding tax amount will be deducted from the customer payment and posted to the **Withholding tax offset** account in a related voucher.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]