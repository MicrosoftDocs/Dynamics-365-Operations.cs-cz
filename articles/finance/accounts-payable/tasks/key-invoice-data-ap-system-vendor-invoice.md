---
title: Zadání dat faktur do systému závazků pomocí faktury dodavatele
description: Tento průvodce záznamem úloh vám pomůže vytvořit fakturu dodavatele z nákupní objednávky a zobrazit si výsledky párování nákupní objednávky, příjemky a faktury (třícestné párování).
author: abruer
manager: AnnBe
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, PurchEditLines, VendEditInvoice, InventItemIdLookupSimple, VendInvoiceMatchingDetails
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 22df9b71c6809e7633b7d573e6992be9d868cbac
ms.sourcegitcommit: 9168621ca9b5061c65f3e05dbc5918b6a11d53d5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/31/2020
ms.locfileid: "3000202"
---
# <a name="key-invoice-data-in-ap-using-a-vendor-invoice"></a><span data-ttu-id="0edfd-103">Zadání dat faktur do systému závazků pomocí faktury dodavatele</span><span class="sxs-lookup"><span data-stu-id="0edfd-103">Key invoice data in AP using a vendor invoice</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0edfd-104">Tento průvodce záznamem úloh vám pomůže vytvořit fakturu dodavatele z nákupní objednávky a zobrazit si výsledky párování nákupní objednávky, příjemky a faktury (třícestné párování).</span><span class="sxs-lookup"><span data-stu-id="0edfd-104">This task guide will help you create a vendor invoice from a purchase order and view the results of matching the purchase order, receipt, and invoice (3 way matching).</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="0edfd-105">Vytvoření nákupní objednávky</span><span class="sxs-lookup"><span data-stu-id="0edfd-105">Create a purchase order</span></span>
1. <span data-ttu-id="0edfd-106">V navigačním podokně přejděte na **Moduly > Závazky > Nákupní objednávky > Všechny nákupní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="0edfd-106">In the Navigation pane, go to **Modules > Accounts payable > Purchase orders > All purchase orders**.</span></span>
2. <span data-ttu-id="0edfd-107">Klepněte na možnost **Nový**.</span><span class="sxs-lookup"><span data-stu-id="0edfd-107">Click **New**.</span></span>
3. <span data-ttu-id="0edfd-108">V poli **Účet dodavatele** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="0edfd-108">In the **Vendor account** field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="0edfd-109">Najděte dodavatele, kterého chcete vybrat.</span><span class="sxs-lookup"><span data-stu-id="0edfd-109">Find a vendor to select.</span></span> <span data-ttu-id="0edfd-110">Například přejděte na US-104.</span><span class="sxs-lookup"><span data-stu-id="0edfd-110">For example, scroll down to US-104.</span></span>
5. <span data-ttu-id="0edfd-111">Vyberte dodavatele US-104.</span><span class="sxs-lookup"><span data-stu-id="0edfd-111">Select vendor US-104.</span></span>
6. <span data-ttu-id="0edfd-112">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="0edfd-112">Click **OK**.</span></span>
7. <span data-ttu-id="0edfd-113">V poli **Číslo položky** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="0edfd-113">In the **Item number** field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="0edfd-114">Vyberte skladovou položku.</span><span class="sxs-lookup"><span data-stu-id="0edfd-114">Select an inventory item.</span></span> <span data-ttu-id="0edfd-115">Například vyberte číslo položky 1000.</span><span class="sxs-lookup"><span data-stu-id="0edfd-115">For example, select item number 1000.</span></span>
9. <span data-ttu-id="0edfd-116">Rozbalte pevnou záložku **Podrobnosti řádku**.</span><span class="sxs-lookup"><span data-stu-id="0edfd-116">Expand the **Line details** fastTab.</span></span>
10. <span data-ttu-id="0edfd-117">Klikněte na kartu **Nastavení**. Zásady párování je možné přepsat a párování nepoužít, nebo použít dvoucestné či třícestné párování.</span><span class="sxs-lookup"><span data-stu-id="0edfd-117">Click the **Setup** tab. You can override the matching policy to use no matching, 2-way matching, or 3-way matching.</span></span>  
11. <span data-ttu-id="0edfd-118">V podokně akcí klikněte na možnost **Zakoupit**.</span><span class="sxs-lookup"><span data-stu-id="0edfd-118">On the Action Pane, click **Purchase**.</span></span>
12. <span data-ttu-id="0edfd-119">Klikněte na tlačítko **Potvrdit**.</span><span class="sxs-lookup"><span data-stu-id="0edfd-119">Click **Confirm**.</span></span>

## <a name="receive-the-products"></a><span data-ttu-id="0edfd-120">Příjem produktů</span><span class="sxs-lookup"><span data-stu-id="0edfd-120">Receive the products</span></span>
1. <span data-ttu-id="0edfd-121">V podokně akcí klikněte na možnost **Přijmout**.</span><span class="sxs-lookup"><span data-stu-id="0edfd-121">On the Action Pane, click **Receive**.</span></span>
2. <span data-ttu-id="0edfd-122">Klikněte na **Příjemka produktu**.</span><span class="sxs-lookup"><span data-stu-id="0edfd-122">Click **Product receipt**.</span></span>
3. <span data-ttu-id="0edfd-123">V poli **Příjemka produktu** zadejte číslo příjemky produktu.</span><span class="sxs-lookup"><span data-stu-id="0edfd-123">In the **Product receipt** field, enter the product receipt number.</span></span> <span data-ttu-id="0edfd-124">Zadejte například PR123.</span><span class="sxs-lookup"><span data-stu-id="0edfd-124">For example, enter PR123.</span></span>
4. <span data-ttu-id="0edfd-125">Kliknutím na tlačítko **OK** zaúčtujte příjemku produktu.</span><span class="sxs-lookup"><span data-stu-id="0edfd-125">Click **OK** to post the product receipt.</span></span>
5. <span data-ttu-id="0edfd-126">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="0edfd-126">Close the page.</span></span>

## <a name="create-a-vendor-invoice"></a><span data-ttu-id="0edfd-127">Vytvoření faktury dodavatele</span><span class="sxs-lookup"><span data-stu-id="0edfd-127">Create a vendor invoice</span></span>
1. <span data-ttu-id="0edfd-128">V navigačním podokně přejděte na **Moduly > Závazky > Nákupní objednávky > Přijaté nákupní objednávky, které nejsou fakturované**.</span><span class="sxs-lookup"><span data-stu-id="0edfd-128">In the Navigation pane, go to **Modules > Accounts payable > Purchase orders > Purchase orders received but not invoiced**.</span></span>
2. <span data-ttu-id="0edfd-129">Vyberte nákupní objednávku, kterou jste vytvořili.</span><span class="sxs-lookup"><span data-stu-id="0edfd-129">Select the purchase order that you created.</span></span>
3. <span data-ttu-id="0edfd-130">V podokně akcí klikněte na možnost **Faktura**.</span><span class="sxs-lookup"><span data-stu-id="0edfd-130">On the Action Pane, click **Invoice**.</span></span>
4. <span data-ttu-id="0edfd-131">Klikněte na **Faktura**.</span><span class="sxs-lookup"><span data-stu-id="0edfd-131">Click **Invoice**.</span></span>
5. <span data-ttu-id="0edfd-132">Do pole **Číslo** zadejte číslo faktury.</span><span class="sxs-lookup"><span data-stu-id="0edfd-132">In the **Number** field, enter the invoice number.</span></span>
6. <span data-ttu-id="0edfd-133">Do pole **Popis faktury** zadejte nějakou hodnotu.</span><span class="sxs-lookup"><span data-stu-id="0edfd-133">In the **Invoice description** field, type a value.</span></span>
7. <span data-ttu-id="0edfd-134">Zadejte datum do pole **Datum faktury**.</span><span class="sxs-lookup"><span data-stu-id="0edfd-134">In the **Invoice date** field, enter a date.</span></span>
8. <span data-ttu-id="0edfd-135">Zadejte číslo 1200 do pole **Jednotková cena**.</span><span class="sxs-lookup"><span data-stu-id="0edfd-135">In the **Unit price** field, enter 1200.</span></span>
9. <span data-ttu-id="0edfd-136">Klikněte na **Přidat řádek**.</span><span class="sxs-lookup"><span data-stu-id="0edfd-136">Click **Add line**.</span></span>
10. <span data-ttu-id="0edfd-137">V poli **Číslo položky** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="0edfd-137">In the **Item number** field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="0edfd-138">V seznamu najděte číslo položky pro instalační náklady.</span><span class="sxs-lookup"><span data-stu-id="0edfd-138">In the list, find the installation charge item number.</span></span> <span data-ttu-id="0edfd-139">Například S0001</span><span class="sxs-lookup"><span data-stu-id="0edfd-139">For example, S0001</span></span>
12. <span data-ttu-id="0edfd-140">Vyberte číslo položky pro instalační náklady.</span><span class="sxs-lookup"><span data-stu-id="0edfd-140">Select the installation charge item number.</span></span> <span data-ttu-id="0edfd-141">Všimněte si, že od okamžiku, kdy jste změny provedli, nebylo provedeno párování.</span><span class="sxs-lookup"><span data-stu-id="0edfd-141">Note that matching has not been performed since you made the changes.</span></span>  
13. <span data-ttu-id="0edfd-142">Klikněte na **Aktualizovat stav párování**.</span><span class="sxs-lookup"><span data-stu-id="0edfd-142">Click **Update match status**.</span></span>
14. <span data-ttu-id="0edfd-143">V podokně akcí klikněte na položku **Přehled**.</span><span class="sxs-lookup"><span data-stu-id="0edfd-143">On the Action Pane, click **Review**.</span></span>
15. <span data-ttu-id="0edfd-144">Klikněte na položku **Podrobnosti párování**.</span><span class="sxs-lookup"><span data-stu-id="0edfd-144">Click **Matching details**.</span></span> <span data-ttu-id="0edfd-145">Nový řádek se službami se nemusí párovat a stav tak uvádí Neprovedeno.</span><span class="sxs-lookup"><span data-stu-id="0edfd-145">The new line with services does not need to be matched so the status stays "Not performed".</span></span>  
16. <span data-ttu-id="0edfd-146">Vyberte příjemku produktu pro skladovou položku, kterou jste obdrželi.</span><span class="sxs-lookup"><span data-stu-id="0edfd-146">Select the product receipt for the inventory item that you received.</span></span> <span data-ttu-id="0edfd-147">Řádek s příjemkou produktu byl spárován, ale neodpovídá množství nebo cena, a proto došlo k chybě.</span><span class="sxs-lookup"><span data-stu-id="0edfd-147">The line with the product receipt was matched but there is a mismatch of quantity or price so it fails.</span></span>  
17. <span data-ttu-id="0edfd-148">Zadejte číslo do pole **Jednotková cena**.</span><span class="sxs-lookup"><span data-stu-id="0edfd-148">In the **Unit price** field, enter a number.</span></span> <span data-ttu-id="0edfd-149">Když nyní odpovídá jednotková cena, stav se aktualizuje na Úspěch.</span><span class="sxs-lookup"><span data-stu-id="0edfd-149">Now that the unit price matches, the status is updated to Passed.</span></span> <span data-ttu-id="0edfd-150">Pokud zásady umožňují nesrovnalosti nebo pokud párování plní pouze funkci upozornění, lze fakturu přesto zaúčtovat.</span><span class="sxs-lookup"><span data-stu-id="0edfd-150">If your policy allows discrepancies or if matching is only a warning, you can still post the invoice.</span></span>  
18. <span data-ttu-id="0edfd-151">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="0edfd-151">Close the page.</span></span>
19. <span data-ttu-id="0edfd-152">Klikněte na možnost **Zaúčtovat**.</span><span class="sxs-lookup"><span data-stu-id="0edfd-152">Click **Post**.</span></span>
20. <span data-ttu-id="0edfd-153">Zavřete formulář.</span><span class="sxs-lookup"><span data-stu-id="0edfd-153">Close the form.</span></span> <span data-ttu-id="0edfd-154">Všimněte si, že nákupní objednávka již není uvedena jako přijatá a nefakturovaná.</span><span class="sxs-lookup"><span data-stu-id="0edfd-154">Note that the purchase order is no longer listed as received but not invoiced.</span></span>  

