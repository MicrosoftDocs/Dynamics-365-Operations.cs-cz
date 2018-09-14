--- 
title: "Nastavit zásady faktur dodavatele"
description: "Zásady faktur dodavatele se spouští při zaúčtování faktury dodavatele na stránce Faktura dodavatele, a při otevření stránky s porušením zásad faktury dodavatele."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendParameters,  SysPolicyListPage, SysPolicyParameters, SysPolicySourceDocumentRuleType, SysPolicy, SysPolicySourceDocumentRule, SysQueryForm, SysQueryTableLookUp, SysQueryPrefixLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: b424eee7c91ef1085c98828c0d5e5cf674717a81
ms.contentlocale: cs-cz
ms.lasthandoff: 09/14/2018

---
# <a name="set-up-vendor-invoice-policies"></a><span data-ttu-id="59277-103">Nastavit zásady faktur dodavatele</span><span class="sxs-lookup"><span data-stu-id="59277-103">Set up vendor invoice policies</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="59277-104">Zásady faktur dodavatele se spouští při zaúčtování faktury dodavatele na stránce Faktura dodavatele, a při otevření stránky s porušením zásad faktury dodavatele.</span><span class="sxs-lookup"><span data-stu-id="59277-104">Vendor invoice policies are run when you post a vendor invoice by using the Vendor invoice page and when you open the vendor invoice Policy violations page.</span></span> <span data-ttu-id="59277-105">Můžete také konfigurovat workflow faktury dodavatele tak, aby spustila zásady faktury dodavatele při každém odeslání faktury do workflowu.</span><span class="sxs-lookup"><span data-stu-id="59277-105">You can also configure the vendor invoice workflow to run vendor invoice policies every time that you submit an invoice to workflow.</span></span> 

<span data-ttu-id="59277-106">Zásady faktur dodavatele se nevztahují na faktury, které byly vytvořeny v registru faktur a deníku faktur.</span><span class="sxs-lookup"><span data-stu-id="59277-106">Vendor invoice policies do not apply to invoices that were created in the invoice register or invoice journal.</span></span> 

<span data-ttu-id="59277-107">Ověření párování faktur nepoužívá zásady faktur dodavatele, ale namísto toho nastaví údaje na stránce s parametry závazků.</span><span class="sxs-lookup"><span data-stu-id="59277-107">Invoice matching validation does not use vendor invoice policies, but is instead set up in the Accounts payable parameters page.</span></span>

<span data-ttu-id="59277-108">Tento záznam používá ukázkovou společnost USMF.</span><span class="sxs-lookup"><span data-stu-id="59277-108">This recording uses the USMF demo company.</span></span> <span data-ttu-id="59277-109">Manažer závazků nebo osoba s rolí vedoucího účetnictví by prováděl tyto kroky.</span><span class="sxs-lookup"><span data-stu-id="59277-109">The accounts payable manager or accounting manager role would perform these steps.</span></span> <span data-ttu-id="59277-110">Před prvním krokem ověřte, že je vybraný konfigurační klíč Párování faktur.</span><span class="sxs-lookup"><span data-stu-id="59277-110">Before you begin, make sure that the Invoice matching configuration key is selected.</span></span>


## <a name="prepare-to-create-vendor-invoice-policies"></a><span data-ttu-id="59277-111">Příprava na vytvoření zásad faktur dodavatele</span><span class="sxs-lookup"><span data-stu-id="59277-111">Prepare to create vendor invoice policies</span></span>
1. <span data-ttu-id="59277-112">Přejděte do nabídky Závazky > Nastavení > Parametry závazků.</span><span class="sxs-lookup"><span data-stu-id="59277-112">Go to Accounts payable > Setup > Accounts payable parameters.</span></span>
2. <span data-ttu-id="59277-113">Klikněte na kartu Ověření faktury.</span><span class="sxs-lookup"><span data-stu-id="59277-113">Click the Invoice validation tab.</span></span>
3. <span data-ttu-id="59277-114">Zaškrtněte nebo zrušte označení pole Automaticky aktualizovat stav záhlaví faktury.</span><span class="sxs-lookup"><span data-stu-id="59277-114">Select or clear the Automatically update invoice header status check box.</span></span>
4. <span data-ttu-id="59277-115">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="59277-115">Click OK.</span></span>
5. <span data-ttu-id="59277-116">V poli Zaúčtovat fakturu s odchylkami: vyberte požadovanou možnost.</span><span class="sxs-lookup"><span data-stu-id="59277-116">In the Post invoice with discrepancies field, select an option.</span></span>
6. <span data-ttu-id="59277-117">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="59277-117">Close the page.</span></span>
7. <span data-ttu-id="59277-118">Přejděte na Závazky > Nastavení zásad > Zásady faktur dodavatele.</span><span class="sxs-lookup"><span data-stu-id="59277-118">Go to Accounts payable > Policy setup > Vendor invoice policies.</span></span>
8. <span data-ttu-id="59277-119">Klikněte na Parametry.</span><span class="sxs-lookup"><span data-stu-id="59277-119">Click Parameters.</span></span>
9. <span data-ttu-id="59277-120">Klepněte na tlačítko btnAdd.</span><span class="sxs-lookup"><span data-stu-id="59277-120">Click btnAdd.</span></span>
10. <span data-ttu-id="59277-121">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="59277-121">Close the page.</span></span>

## <a name="create-policy-rule-types-for-vendor-invoices"></a><span data-ttu-id="59277-122">Vytvoření nebo aktualizace typů pro faktury dodavatele</span><span class="sxs-lookup"><span data-stu-id="59277-122">Create policy rule types for vendor invoices</span></span>
1. <span data-ttu-id="59277-123">Přejděte na Závazky > Nastavení zásad > Typy pravidel zásad pro faktury dodavatele.</span><span class="sxs-lookup"><span data-stu-id="59277-123">Go to Accounts payable > Policy setup > Vendor invoice policy rule types.</span></span>
2. <span data-ttu-id="59277-124">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="59277-124">Click New.</span></span>
3. <span data-ttu-id="59277-125">Zadejte hodnotu do pole Název pravidla.</span><span class="sxs-lookup"><span data-stu-id="59277-125">In the Rule name field, type a value.</span></span>
4. <span data-ttu-id="59277-126">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="59277-126">In the Description field, type a value.</span></span>
5. <span data-ttu-id="59277-127">V poli Název dotazu kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="59277-127">In the Query name field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="59277-128">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="59277-128">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="59277-129">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="59277-129">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="59277-130">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="59277-130">Click Save.</span></span>
9. <span data-ttu-id="59277-131">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="59277-131">Close the page.</span></span>

## <a name="define-a-vendor-invoice-policy"></a><span data-ttu-id="59277-132">Definování zásad faktur dodavatele</span><span class="sxs-lookup"><span data-stu-id="59277-132">Define a vendor invoice policy</span></span>
1. <span data-ttu-id="59277-133">Přejděte na Závazky > Nastavení zásad > Zásady faktur dodavatele.</span><span class="sxs-lookup"><span data-stu-id="59277-133">Go to Accounts payable > Policy setup > Vendor invoice policies.</span></span>
2. <span data-ttu-id="59277-134">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="59277-134">Click New.</span></span>
3. <span data-ttu-id="59277-135">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="59277-135">In the Name field, type a value.</span></span>
4. <span data-ttu-id="59277-136">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="59277-136">In the Description field, type a value.</span></span>
5. <span data-ttu-id="59277-137">Rozbalte nebo sbalte část Organizace zásad.</span><span class="sxs-lookup"><span data-stu-id="59277-137">Expand or collapse the Policy organizations section.</span></span>
6. <span data-ttu-id="59277-138">Ve stromovém zobrazení vyberte systém Contoso Entertainment System USA.</span><span class="sxs-lookup"><span data-stu-id="59277-138">In the tree, select 'Contoso Entertainment System USA'.</span></span>
7. <span data-ttu-id="59277-139">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="59277-139">Click Add.</span></span>
8. <span data-ttu-id="59277-140">Rozbalte nebo sbalte část Pravidla zásad.</span><span class="sxs-lookup"><span data-stu-id="59277-140">Expand or collapse the Policy rules section.</span></span>
9. <span data-ttu-id="59277-141">Klikněte na Vytvořit pravidlo zásad.</span><span class="sxs-lookup"><span data-stu-id="59277-141">Click Create policy rule.</span></span>
10. <span data-ttu-id="59277-142">Zadejte hodnotu do pole Popis pravidla zásad.</span><span class="sxs-lookup"><span data-stu-id="59277-142">In the Policy rule description field, type a value.</span></span>
11. <span data-ttu-id="59277-143">Klepněte na tlačítko Filtr.</span><span class="sxs-lookup"><span data-stu-id="59277-143">Click Filter.</span></span>
12. <span data-ttu-id="59277-144">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="59277-144">Click Add.</span></span>
13. <span data-ttu-id="59277-145">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="59277-145">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="59277-146">V poli Tabulka kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="59277-146">In the Table field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="59277-147">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="59277-147">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="59277-148">V poli Odvozená tabulka kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="59277-148">In the Derived table field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="59277-149">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="59277-149">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="59277-150">V poli Pole kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="59277-150">In the Field field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="59277-151">Zadejte hodnotu do pole Pole.</span><span class="sxs-lookup"><span data-stu-id="59277-151">In the Field field, type a value.</span></span>
20. <span data-ttu-id="59277-152">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="59277-152">Close the page.</span></span>
21. <span data-ttu-id="59277-153">Zadejte hodnotu do pole Kritéria.</span><span class="sxs-lookup"><span data-stu-id="59277-153">In the Criteria field, type a value.</span></span>
22. <span data-ttu-id="59277-154">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="59277-154">Click OK.</span></span>
23. <span data-ttu-id="59277-155">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="59277-155">Click OK.</span></span>
24. <span data-ttu-id="59277-156">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="59277-156">Close the page.</span></span>
25. <span data-ttu-id="59277-157">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="59277-157">Close the page.</span></span>


