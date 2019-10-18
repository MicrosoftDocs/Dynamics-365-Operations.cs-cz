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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 179e8a20dd65847f90872ae0e56b3e4991a6b00e
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/27/2019
ms.locfileid: "2184984"
---
# <a name="er-generate-electronic-documents-for-payments-using-a-format-configuration"></a><span data-ttu-id="c8d72-103">Generování elektronických dokumentů ER pro platby za použití konfigurace formátu</span><span class="sxs-lookup"><span data-stu-id="c8d72-103">ER Generate electronic documents for payments using a format configuration</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c8d72-104">Následující postup popisuje, jak uživatel s rolí Správce systému nebo Návrhář elektronického výkaznictví může použít novou konfiguraci formátu pro elektronické výkaznictví a vytvořit tak elektronické doklady pro zpracování plateb.</span><span class="sxs-lookup"><span data-stu-id="c8d72-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can use a new Electronic reporting (ER) format configuration to generate electronic documents for processing payments.</span></span> <span data-ttu-id="c8d72-105">Tyto kroky lze provést v rámci vzorové společnosti GBSI.</span><span class="sxs-lookup"><span data-stu-id="c8d72-105">These steps can be performed in the GBSI sample company.</span></span>

<span data-ttu-id="c8d72-106">K provedení těchto kroků musíte nejprve dokončit jednotlivé kroky v postupu "Vytvoření konfigurace s formátem platebního dokladu".</span><span class="sxs-lookup"><span data-stu-id="c8d72-106">To complete these steps, you must first complete the steps in the “Create a configuration with format of payment document” procedure.</span></span>


## <a name="change-the-configuration-of-the-electronic-payment-method"></a><span data-ttu-id="c8d72-107">Úprava konfigurace metody elektronické platby</span><span class="sxs-lookup"><span data-stu-id="c8d72-107">Change the configuration of the electronic payment method</span></span>
1. <span data-ttu-id="c8d72-108">Přejděte do nabídky Závazky > Nastavení platby > Metody platby.</span><span class="sxs-lookup"><span data-stu-id="c8d72-108">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
2. <span data-ttu-id="c8d72-109">V případě potřeby klepnutím rozbalte oddíl Formát souboru.</span><span class="sxs-lookup"><span data-stu-id="c8d72-109">Toggle the File format section to expand it, if needed.</span></span>
3. <span data-ttu-id="c8d72-110">Použijte rychlý filtr pro hledání záznamů.</span><span class="sxs-lookup"><span data-stu-id="c8d72-110">Use the Quick Filter to find records.</span></span> <span data-ttu-id="c8d72-111">Můžete například filtrovat v poli Metody platby pomocí hodnoty „Elektronicky“.</span><span class="sxs-lookup"><span data-stu-id="c8d72-111">For example, filter on the Method of payment field with a value of 'Electronic'.</span></span>
4. <span data-ttu-id="c8d72-112">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="c8d72-112">Click Edit.</span></span>
5. <span data-ttu-id="c8d72-113">Vyberte možnost Ano v poli Obecné elektronické výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="c8d72-113">Set the General electronic reporting field to Yes.</span></span>
    * <span data-ttu-id="c8d72-114">Vyberte možnost Ano, chcete-li použít pro generování souborů plateb obecný vzor elektronického vykazování.</span><span class="sxs-lookup"><span data-stu-id="c8d72-114">Select Yes to use the General electronic reporting pattern for payment files generation.</span></span>  
6. <span data-ttu-id="c8d72-115">V poli Název kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="c8d72-115">In the Name field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="c8d72-116">Vyberte konfiguraci formátu BACS (Velká Británie – fiktivní).</span><span class="sxs-lookup"><span data-stu-id="c8d72-116">Select BACS (UK fictitious) format configuration.</span></span>
8. <span data-ttu-id="c8d72-117">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="c8d72-117">Click Save.</span></span>
9. <span data-ttu-id="c8d72-118">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="c8d72-118">Close the page.</span></span>

## <a name="test-the-format-of-generated-payment-files"></a><span data-ttu-id="c8d72-119">Test formátu generovaných souborů platby</span><span class="sxs-lookup"><span data-stu-id="c8d72-119">Test the format of generated payment files</span></span>
1. <span data-ttu-id="c8d72-120">Přejděte na Závazky > Platby > Deník plateb.</span><span class="sxs-lookup"><span data-stu-id="c8d72-120">Go to Accounts payable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="c8d72-121">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="c8d72-121">Click New.</span></span>
3. <span data-ttu-id="c8d72-122">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="c8d72-122">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="c8d72-123">V poli Název kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="c8d72-123">In the Name field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="c8d72-124">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="c8d72-124">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="c8d72-125">Vyberte VendPay.</span><span class="sxs-lookup"><span data-stu-id="c8d72-125">Select VendPay.</span></span>  
6. <span data-ttu-id="c8d72-126">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="c8d72-126">Click Save.</span></span>
7. <span data-ttu-id="c8d72-127">Klikněte na položku Řádky.</span><span class="sxs-lookup"><span data-stu-id="c8d72-127">Click Lines.</span></span>
8. <span data-ttu-id="c8d72-128">Zadejte hodnotu DEMF do pole Společnost.</span><span class="sxs-lookup"><span data-stu-id="c8d72-128">In the Company field, type 'DEMF'.</span></span>
    * <span data-ttu-id="c8d72-129">DEMF</span><span class="sxs-lookup"><span data-stu-id="c8d72-129">DEMF</span></span>  
9. <span data-ttu-id="c8d72-130">Zadejte hodnotu DE-01001 do pole Účet.</span><span class="sxs-lookup"><span data-stu-id="c8d72-130">In the Account field, specify the values 'DE-01001'.</span></span>
    * <span data-ttu-id="c8d72-131">DE – 01001</span><span class="sxs-lookup"><span data-stu-id="c8d72-131">DE-01001</span></span>  
10. <span data-ttu-id="c8d72-132">V poli Popis uveďte text Platba.</span><span class="sxs-lookup"><span data-stu-id="c8d72-132">In the Description field, type 'Payment'.</span></span>
    * <span data-ttu-id="c8d72-133">Platba</span><span class="sxs-lookup"><span data-stu-id="c8d72-133">Payment</span></span>  
11. <span data-ttu-id="c8d72-134">Do pole Má dáti zadejte čísl.</span><span class="sxs-lookup"><span data-stu-id="c8d72-134">In the Debit field, enter a number.</span></span>
    * <span data-ttu-id="c8d72-135">1 000</span><span class="sxs-lookup"><span data-stu-id="c8d72-135">1000</span></span>  
12. <span data-ttu-id="c8d72-136">Klikněte na kartu Platba.</span><span class="sxs-lookup"><span data-stu-id="c8d72-136">Click the Payment tab.</span></span>
13. <span data-ttu-id="c8d72-137">V poli Způsob platby kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="c8d72-137">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="c8d72-138">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="c8d72-138">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="c8d72-139">Vyberte elektronickou hodnotu.</span><span class="sxs-lookup"><span data-stu-id="c8d72-139">Select the Electronic value.</span></span>  
15. <span data-ttu-id="c8d72-140">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="c8d72-140">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="c8d72-141">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="c8d72-141">Click Save.</span></span>
17. <span data-ttu-id="c8d72-142">Klepněte na Generovat platby.</span><span class="sxs-lookup"><span data-stu-id="c8d72-142">Click Generate payments.</span></span>
18. <span data-ttu-id="c8d72-143">V poli Způsob platby kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="c8d72-143">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="c8d72-144">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="c8d72-144">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="c8d72-145">Vyberte elektronickou hodnotu.</span><span class="sxs-lookup"><span data-stu-id="c8d72-145">Select the Electronic value.</span></span>  
20. <span data-ttu-id="c8d72-146">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="c8d72-146">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="c8d72-147">Vyberte elektronickou hodnotu.</span><span class="sxs-lookup"><span data-stu-id="c8d72-147">Select the Electronic value.</span></span>  
21. <span data-ttu-id="c8d72-148">Zadejte hodnotu do pole Název souboru.</span><span class="sxs-lookup"><span data-stu-id="c8d72-148">In the File name field, type a value.</span></span>
    * <span data-ttu-id="c8d72-149">Zadejte například Platby.</span><span class="sxs-lookup"><span data-stu-id="c8d72-149">For example, type 'payments'.</span></span>  
22. <span data-ttu-id="c8d72-150">V poli Bankovní účet kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="c8d72-150">In the Bank account field, click the drop-down button to open the lookup.</span></span>
23. <span data-ttu-id="c8d72-151">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="c8d72-151">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="c8d72-152">Vyberte hodnotu GBSI OPER.</span><span class="sxs-lookup"><span data-stu-id="c8d72-152">Select the value GBSI OPER.</span></span>  
24. <span data-ttu-id="c8d72-153">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="c8d72-153">Click OK.</span></span>
25. <span data-ttu-id="c8d72-154">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="c8d72-154">Click OK.</span></span>
    * <span data-ttu-id="c8d72-155">Analyzujte vytvořený soubor platby ve formátu XML.</span><span class="sxs-lookup"><span data-stu-id="c8d72-155">Analyze the created payment file in XML format.</span></span> <span data-ttu-id="c8d72-156">Srovnejte jej s navrženým rozvržením dokumentu a definovanými atributy platební transakce.</span><span class="sxs-lookup"><span data-stu-id="c8d72-156">Compare it with the designed document layout and defined payment transaction attributes.</span></span>  

