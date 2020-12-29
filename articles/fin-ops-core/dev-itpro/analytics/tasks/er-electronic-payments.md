---
title: Generování elektronických dokumentů ER pro platby za použití konfigurace formátu
description: Následující postup popisuje, jak uživatel s rolí Správce systému nebo Návrhář elektronického výkaznictví může použít novou konfiguraci formátu pro elektronické výkaznictví a vytvořit tak elektronické doklady pro zpracování plateb.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPaymMode, LedgerJournalTable, LedgerJournalTransVendPaym, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6e88df5c2f92ee2b9b448ba100c8bc4105eddae4
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681726"
---
# <a name="er-generate-electronic-documents-for-payments-using-a-format-configuration"></a><span data-ttu-id="98879-103">Generování elektronických dokumentů ER pro platby za použití konfigurace formátu</span><span class="sxs-lookup"><span data-stu-id="98879-103">ER Generate electronic documents for payments using a format configuration</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="98879-104">Následující postup popisuje, jak uživatel s rolí Správce systému nebo Návrhář elektronického výkaznictví může použít novou konfiguraci formátu pro elektronické výkaznictví a vytvořit tak elektronické doklady pro zpracování plateb.</span><span class="sxs-lookup"><span data-stu-id="98879-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can use a new Electronic reporting (ER) format configuration to generate electronic documents for processing payments.</span></span> <span data-ttu-id="98879-105">Tyto kroky lze provést v rámci vzorové společnosti GBSI.</span><span class="sxs-lookup"><span data-stu-id="98879-105">These steps can be performed in the GBSI sample company.</span></span>

<span data-ttu-id="98879-106">K provedení těchto kroků musíte nejprve dokončit kroky v postupu „Vytvoření konfigurace s formátem platebního dokladu“.</span><span class="sxs-lookup"><span data-stu-id="98879-106">To complete these steps, you must first complete the steps in the "Create a configuration with format of payment document" procedure.</span></span>


## <a name="change-the-configuration-of-the-electronic-payment-method"></a><span data-ttu-id="98879-107">Úprava konfigurace metody elektronické platby</span><span class="sxs-lookup"><span data-stu-id="98879-107">Change the configuration of the electronic payment method</span></span>
1. <span data-ttu-id="98879-108">Přejděte do nabídky Závazky > Nastavení platby > Metody platby.</span><span class="sxs-lookup"><span data-stu-id="98879-108">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
2. <span data-ttu-id="98879-109">V případě potřeby klepnutím rozbalte oddíl Formát souboru.</span><span class="sxs-lookup"><span data-stu-id="98879-109">Toggle the File format section to expand it, if needed.</span></span>
3. <span data-ttu-id="98879-110">Použijte rychlý filtr pro hledání záznamů.</span><span class="sxs-lookup"><span data-stu-id="98879-110">Use the Quick Filter to find records.</span></span> <span data-ttu-id="98879-111">Můžete například filtrovat v poli Metody platby pomocí hodnoty „Elektronicky“.</span><span class="sxs-lookup"><span data-stu-id="98879-111">For example, filter on the Method of payment field with a value of 'Electronic'.</span></span>
4. <span data-ttu-id="98879-112">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="98879-112">Click Edit.</span></span>
5. <span data-ttu-id="98879-113">Vyberte možnost Ano v poli Obecné elektronické výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="98879-113">Set the General electronic reporting field to Yes.</span></span>
    * <span data-ttu-id="98879-114">Vyberte možnost Ano, chcete-li použít pro generování souborů plateb obecný vzor elektronického vykazování.</span><span class="sxs-lookup"><span data-stu-id="98879-114">Select Yes to use the General electronic reporting pattern for payment files generation.</span></span>  
6. <span data-ttu-id="98879-115">V poli Název kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="98879-115">In the Name field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="98879-116">Vyberte konfiguraci formátu BACS (Velká Británie – fiktivní).</span><span class="sxs-lookup"><span data-stu-id="98879-116">Select BACS (UK fictitious) format configuration.</span></span>
8. <span data-ttu-id="98879-117">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="98879-117">Click Save.</span></span>
9. <span data-ttu-id="98879-118">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="98879-118">Close the page.</span></span>

## <a name="test-the-format-of-generated-payment-files"></a><span data-ttu-id="98879-119">Test formátu generovaných souborů platby</span><span class="sxs-lookup"><span data-stu-id="98879-119">Test the format of generated payment files</span></span>
1. <span data-ttu-id="98879-120">Přejděte na Závazky > Platby > Deník plateb.</span><span class="sxs-lookup"><span data-stu-id="98879-120">Go to Accounts payable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="98879-121">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="98879-121">Click New.</span></span>
3. <span data-ttu-id="98879-122">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="98879-122">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="98879-123">V poli Název kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="98879-123">In the Name field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="98879-124">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="98879-124">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="98879-125">Vyberte VendPay.</span><span class="sxs-lookup"><span data-stu-id="98879-125">Select VendPay.</span></span>  
6. <span data-ttu-id="98879-126">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="98879-126">Click Save.</span></span>
7. <span data-ttu-id="98879-127">Klikněte na položku Řádky.</span><span class="sxs-lookup"><span data-stu-id="98879-127">Click Lines.</span></span>
8. <span data-ttu-id="98879-128">Zadejte hodnotu DEMF do pole Společnost.</span><span class="sxs-lookup"><span data-stu-id="98879-128">In the Company field, type 'DEMF'.</span></span>
    * <span data-ttu-id="98879-129">DEMF</span><span class="sxs-lookup"><span data-stu-id="98879-129">DEMF</span></span>  
9. <span data-ttu-id="98879-130">Zadejte hodnotu DE-01001 do pole Účet.</span><span class="sxs-lookup"><span data-stu-id="98879-130">In the Account field, specify the values 'DE-01001'.</span></span>
    * <span data-ttu-id="98879-131">DE – 01001</span><span class="sxs-lookup"><span data-stu-id="98879-131">DE-01001</span></span>  
10. <span data-ttu-id="98879-132">V poli Popis uveďte text Platba.</span><span class="sxs-lookup"><span data-stu-id="98879-132">In the Description field, type 'Payment'.</span></span>
    * <span data-ttu-id="98879-133">Platba</span><span class="sxs-lookup"><span data-stu-id="98879-133">Payment</span></span>  
11. <span data-ttu-id="98879-134">Do pole Má dáti zadejte čísl.</span><span class="sxs-lookup"><span data-stu-id="98879-134">In the Debit field, enter a number.</span></span>
    * <span data-ttu-id="98879-135">1 000</span><span class="sxs-lookup"><span data-stu-id="98879-135">1000</span></span>  
12. <span data-ttu-id="98879-136">Klikněte na kartu Platba.</span><span class="sxs-lookup"><span data-stu-id="98879-136">Click the Payment tab.</span></span>
13. <span data-ttu-id="98879-137">V poli Způsob platby kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="98879-137">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="98879-138">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="98879-138">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="98879-139">Vyberte elektronickou hodnotu.</span><span class="sxs-lookup"><span data-stu-id="98879-139">Select the Electronic value.</span></span>  
15. <span data-ttu-id="98879-140">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="98879-140">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="98879-141">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="98879-141">Click Save.</span></span>
17. <span data-ttu-id="98879-142">Klepněte na Generovat platby.</span><span class="sxs-lookup"><span data-stu-id="98879-142">Click Generate payments.</span></span>
18. <span data-ttu-id="98879-143">V poli Způsob platby kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="98879-143">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="98879-144">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="98879-144">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="98879-145">Vyberte elektronickou hodnotu.</span><span class="sxs-lookup"><span data-stu-id="98879-145">Select the Electronic value.</span></span>  
20. <span data-ttu-id="98879-146">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="98879-146">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="98879-147">Vyberte elektronickou hodnotu.</span><span class="sxs-lookup"><span data-stu-id="98879-147">Select the Electronic value.</span></span>  
21. <span data-ttu-id="98879-148">Zadejte hodnotu do pole Název souboru.</span><span class="sxs-lookup"><span data-stu-id="98879-148">In the File name field, type a value.</span></span>
    * <span data-ttu-id="98879-149">Zadejte například Platby.</span><span class="sxs-lookup"><span data-stu-id="98879-149">For example, type 'payments'.</span></span>  
22. <span data-ttu-id="98879-150">V poli Bankovní účet kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="98879-150">In the Bank account field, click the drop-down button to open the lookup.</span></span>
23. <span data-ttu-id="98879-151">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="98879-151">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="98879-152">Vyberte hodnotu GBSI OPER.</span><span class="sxs-lookup"><span data-stu-id="98879-152">Select the value GBSI OPER.</span></span>  
24. <span data-ttu-id="98879-153">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="98879-153">Click OK.</span></span>
25. <span data-ttu-id="98879-154">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="98879-154">Click OK.</span></span>
    * <span data-ttu-id="98879-155">Analyzujte vytvořený soubor platby ve formátu XML.</span><span class="sxs-lookup"><span data-stu-id="98879-155">Analyze the created payment file in XML format.</span></span> <span data-ttu-id="98879-156">Srovnejte jej s navrženým rozvržením dokumentu a definovanými atributy platební transakce.</span><span class="sxs-lookup"><span data-stu-id="98879-156">Compare it with the designed document layout and defined payment transaction attributes.</span></span>  

