---
title: Definování platebních poplatků dodavatelů
description: Nastavte poplatky pro platby dodavatelů.
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPaymFee, VendPaymModeFee, BankAccountTableLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0705cdae069b687a141b0a85280eaed0fa207a89
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5227249"
---
# <a name="define-vendor-payment-fees"></a><span data-ttu-id="1dc89-103">Definování platebních poplatků dodavatelů</span><span class="sxs-lookup"><span data-stu-id="1dc89-103">Define vendor payment fees</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1dc89-104">Nastavte poplatky pro platby dodavatelů.</span><span class="sxs-lookup"><span data-stu-id="1dc89-104">Set up vendor payment fees.</span></span> <span data-ttu-id="1dc89-105">Tento úkol používá ukázkovou společnost USMF.</span><span class="sxs-lookup"><span data-stu-id="1dc89-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="1dc89-106">Přejděte do nabídky Závazky > Nastavení platby > Platební poplatek.</span><span class="sxs-lookup"><span data-stu-id="1dc89-106">Go to Accounts payable > Payment setup > Payment fee.</span></span>
2. <span data-ttu-id="1dc89-107">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="1dc89-107">Click New.</span></span>
3. <span data-ttu-id="1dc89-108">Zadejte hodnotu do pole ID poplatku.</span><span class="sxs-lookup"><span data-stu-id="1dc89-108">In the Fee ID field, type a value.</span></span>
    * <span data-ttu-id="1dc89-109">ID poplatku by mělo nabízet popis v případě, že bude tento poplatek použit (například "EFT_Fee").</span><span class="sxs-lookup"><span data-stu-id="1dc89-109">The Fee ID should describe when this fee will be used, such as "EFT_Fee".</span></span>  
4. <span data-ttu-id="1dc89-110">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="1dc89-110">In the Name field, type a value.</span></span>
5. <span data-ttu-id="1dc89-111">Zadejte hodnotu do pole Popis poplatku.</span><span class="sxs-lookup"><span data-stu-id="1dc89-111">In the Fee description field, type a value.</span></span>
    * <span data-ttu-id="1dc89-112">Přidejte popis a poskytněte tak více podrobností o tom, kdy je poplatek vyměřen.</span><span class="sxs-lookup"><span data-stu-id="1dc89-112">Add a description to provide more detail on when the fee is assessed.</span></span>  
6. <span data-ttu-id="1dc89-113">V poli Náklady vyberte dodavatele nebo hlavní knihu.</span><span class="sxs-lookup"><span data-stu-id="1dc89-113">In the Charge field, select either Vendor or Ledger.</span></span>
    * <span data-ttu-id="1dc89-114">Hlavní kniha se používá, pokud bude poplatek zanesen do výdajů pro vaši organizaci.</span><span class="sxs-lookup"><span data-stu-id="1dc89-114">Ledger is used when the fee will be expensed to your organization.</span></span>  <span data-ttu-id="1dc89-115">Dodavatel se používá, pokud bude poplatek zanesen dodavateli.</span><span class="sxs-lookup"><span data-stu-id="1dc89-115">Vendor is used when the fee will be assessed to the vendor.</span></span>  
7. <span data-ttu-id="1dc89-116">Zadejte hlavní účet, pokud budou poplatky zaneseny.</span><span class="sxs-lookup"><span data-stu-id="1dc89-116">Enter a main account for where the fee will be expensed.</span></span>
    * <span data-ttu-id="1dc89-117">Tato volba je k dispozici pouze tehdy, pokud jako možnost Náklady vyberete Hlavní kniha.</span><span class="sxs-lookup"><span data-stu-id="1dc89-117">This option is only available when selecting Ledger as the Charge option.</span></span>  
8. <span data-ttu-id="1dc89-118">Vyberte deník, u kterého lze použít tento poplatek.</span><span class="sxs-lookup"><span data-stu-id="1dc89-118">Select the journal on which this fee can be used.</span></span> 
    * <span data-ttu-id="1dc89-119">Pro platební poplatky dodavatele vyberte deník Úhrady dodavateli.</span><span class="sxs-lookup"><span data-stu-id="1dc89-119">For a vendor payment fee, you would select the journal 'Vendor disbursement.'</span></span>  
9. <span data-ttu-id="1dc89-120">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="1dc89-120">Click Save.</span></span>
10. <span data-ttu-id="1dc89-121">Klikněte na Nastavení platebního poplatku.</span><span class="sxs-lookup"><span data-stu-id="1dc89-121">Click Payment fee setup.</span></span>
    * <span data-ttu-id="1dc89-122">Pokračujte k nastavení platebních poplatků a definujte, kdy má poplatek být upraven na výchozí pro deník, který jste vybrali.</span><span class="sxs-lookup"><span data-stu-id="1dc89-122">Continue to the Payment fee setup to define when the fee should default onto the journal you selected.</span></span>  
11. <span data-ttu-id="1dc89-123">Vyberte možnost Tabulka, Skupina nebo Vše.</span><span class="sxs-lookup"><span data-stu-id="1dc89-123">Select either Table, Group or All.</span></span>
    * <span data-ttu-id="1dc89-124">Tabulka slouží k výběru jednoho bankovního účtu, Skupina slouží k výběru bankovní skupiny a Vše umožňuje použití tohoto nastavení poplatků pro všechny bankovní účty</span><span class="sxs-lookup"><span data-stu-id="1dc89-124">Table is used to select a single bank account, Group is used to select a bank group, and All is to use this fee setup for all bank accounts</span></span>  
12. <span data-ttu-id="1dc89-125">Vyberte bankovní účet nebo bankovní skupinu.</span><span class="sxs-lookup"><span data-stu-id="1dc89-125">Select either a bank group or a bank account.</span></span>
    * <span data-ttu-id="1dc89-126">Vyhledávání zobrazí bankovní skupinu, pokud jste vybrali možnost Skupina, a bude popisovat bankovní účty, jestliže jste vybrali Tabulka.</span><span class="sxs-lookup"><span data-stu-id="1dc89-126">The lookup will show bank group if you selected Group, and will show bank accounts if you selected Table.</span></span>  
13. <span data-ttu-id="1dc89-127">Vyberte metodu platby, pro kterou se vyhodnotí tento poplatek.</span><span class="sxs-lookup"><span data-stu-id="1dc89-127">Select the method of payment for when this fee will be assessed.</span></span>
14. <span data-ttu-id="1dc89-128">Vyberte specifikaci platby pro vybraný způsob platby.</span><span class="sxs-lookup"><span data-stu-id="1dc89-128">Select the Payment specification for the selected method of payment.</span></span>
    * <span data-ttu-id="1dc89-129">Specifikace platby se používají pro platbu metodou elektronického převodu finančních prostředků.</span><span class="sxs-lookup"><span data-stu-id="1dc89-129">The Payment specification is used with electronic fund transfer methods of payment.</span></span>  
15. <span data-ttu-id="1dc89-130">Určete, zda poplatek budou procenta, částka nebo interval.</span><span class="sxs-lookup"><span data-stu-id="1dc89-130">Select whether the fee is a percentage, amount or interval.</span></span>
16. <span data-ttu-id="1dc89-131">Zadejte procento nebo částku poplatku.</span><span class="sxs-lookup"><span data-stu-id="1dc89-131">Enter the percentage or amount of the fee.</span></span>
    * <span data-ttu-id="1dc89-132">Pokud je Poplatek procentuální hodnotu, zadejte procento.</span><span class="sxs-lookup"><span data-stu-id="1dc89-132">If the Fee is a percentage, enter the percentage.</span></span> <span data-ttu-id="1dc89-133">Pokud ke Poplatek částkou, zadejte částku poplatku.</span><span class="sxs-lookup"><span data-stu-id="1dc89-133">If the Fee is an amount, enter the amount of the fee.</span></span> <span data-ttu-id="1dc89-134">U poplatku ve formě intervalu použijte kartu Interval pro definování vrstvených poplatků.</span><span class="sxs-lookup"><span data-stu-id="1dc89-134">If the Fee is an interval, use the Interval tab to defined the tiered fees.</span></span>  
17. <span data-ttu-id="1dc89-135">V poli Měna poplatku vyberte měnu, v níž bude poplatek vyměřen.</span><span class="sxs-lookup"><span data-stu-id="1dc89-135">In the Fee currency field, select the currency in which the fee will be assessed.</span></span>
    * <span data-ttu-id="1dc89-136">Tato měna je pro poplatek.</span><span class="sxs-lookup"><span data-stu-id="1dc89-136">This currency is for the fee.</span></span> <span data-ttu-id="1dc89-137">Měna platby slouží k definování toho, kdy se pravidla poplatku musí vyhodnotit na základě měny platby.</span><span class="sxs-lookup"><span data-stu-id="1dc89-137">The payment currency is used to define when the fee rule should be assessed based on the payment's currency.</span></span> <span data-ttu-id="1dc89-138">Například vaše banka může účtovat poplatek, když je provedena platba v EUR, ale pro všechny ostatní platby není určen poplatek.</span><span class="sxs-lookup"><span data-stu-id="1dc89-138">For example, your bank may charge a fee when a payment is made in EUR, but all other payments aren't assessed a fee.</span></span>  
18. <span data-ttu-id="1dc89-139">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="1dc89-139">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]