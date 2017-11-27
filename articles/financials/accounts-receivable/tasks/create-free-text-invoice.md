--- 
title: "Vytvořit volnou fakturu"
description: "Tento průvodce úkolem ukazuje vytvoření volné faktury."
author: mikefalkner
manager: AnnBe
ms.date: 10/26/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ef3cad6538d9efbd1c1881f4b7d771382d9b1ba8
ms.openlocfilehash: 87e293008fd748aa0dcc6b3caa94a4889bed35de
ms.contentlocale: cs-cz
ms.lasthandoff: 10/26/2017

---
# <a name="create-a-free-text-invoice"></a><span data-ttu-id="82ad5-103">Vytvořit volnou fakturu</span><span class="sxs-lookup"><span data-stu-id="82ad5-103">Create a free text invoice</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="82ad5-104">Tento průvodce úkolem ukazuje vytvoření volné faktury.</span><span class="sxs-lookup"><span data-stu-id="82ad5-104">This task guide demonstrates creating a free text invoice.</span></span> <span data-ttu-id="82ad5-105">Tento úkol používá ukázkovou společnost USMF.</span><span class="sxs-lookup"><span data-stu-id="82ad5-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="82ad5-106">Přejděte na Pohledávky > Faktury > Všechny volné faktury.</span><span class="sxs-lookup"><span data-stu-id="82ad5-106">Go to Accounts receivable > Invoices > All free text invoices.</span></span>
2. <span data-ttu-id="82ad5-107">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="82ad5-107">Click New.</span></span>
3. <span data-ttu-id="82ad5-108">V poli Účet odběratele vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="82ad5-108">In the Customer account field, select a value.</span></span>
    * <span data-ttu-id="82ad5-109">Jako výchozí účet faktury bude nastaven stejný účet, jaký byl použit pro účet odběratele.</span><span class="sxs-lookup"><span data-stu-id="82ad5-109">The invoice account will default to the same account used for the customer account.</span></span>   
    * <span data-ttu-id="82ad5-110">Pokud nebyla faktura zaúčtována, počátečním účetním stavem je Zpracovává se.</span><span class="sxs-lookup"><span data-stu-id="82ad5-110">The accounting status starts with In process if the invoice is not posted.</span></span>   
    * <span data-ttu-id="82ad5-111">Číslo faktury bude přiřazeno při zaúčtování faktury.</span><span class="sxs-lookup"><span data-stu-id="82ad5-111">The invoice number will be assigned when the invoice is posted.</span></span>  
    * <span data-ttu-id="82ad5-112">Pokud používáte zmocnění SEPA, ve zmocnění k přímému debetu bude při výběru účtu zákazníka automaticky vyplněno zmocnění.</span><span class="sxs-lookup"><span data-stu-id="82ad5-112">If you are using SEPA mandates, the direct debit mandate will be automatically populated with a mandate when you select the customer account.</span></span>  
4. <span data-ttu-id="82ad5-113">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="82ad5-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="82ad5-114">V poli Hlavní účet zadejte číslo účtu bez dimenze.</span><span class="sxs-lookup"><span data-stu-id="82ad5-114">In the Main account field, specify an account number without dimensions.</span></span>
    * <span data-ttu-id="82ad5-115">Můžete také zadat jeden nebo více znaků pro hlavní účet a vyhledat účet pomocí vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="82ad5-115">You can also enter one or more characters for the main account and use the lookup to find your account.</span></span> <span data-ttu-id="82ad5-116">Dimenze zadáte později v této příručce.</span><span class="sxs-lookup"><span data-stu-id="82ad5-116">You will enter dimensions later on in this guide.</span></span>  
6. <span data-ttu-id="82ad5-117">Rozbalte pevnou záložku Podrobnosti řádku, aby bylo možné přidat dimenze do hlavního účtu.</span><span class="sxs-lookup"><span data-stu-id="82ad5-117">Expand the Line details fasttab so you can add dimensions to your main account.</span></span>
7. <span data-ttu-id="82ad5-118">Klikněte na záložku Řádek finančních dimenzí.</span><span class="sxs-lookup"><span data-stu-id="82ad5-118">Click the Financial dimensions line tab.</span></span>
    * <span data-ttu-id="82ad5-119">Dimenze jsou pouze pro vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="82ad5-119">The dimensions are for the selected line only.</span></span>    
    * <span data-ttu-id="82ad5-120">Skupina prodejní daně je vyplněna z údajů odběratele.</span><span class="sxs-lookup"><span data-stu-id="82ad5-120">The sales tax group is populated from the customer.</span></span> <span data-ttu-id="82ad5-121">Pokud odběratel nemá skupinu DPH, použije se skupina DPH z hlavního účtu.</span><span class="sxs-lookup"><span data-stu-id="82ad5-121">If the customer does not have a sales tax group, the sales tax group from the main account is used.</span></span>  
    * <span data-ttu-id="82ad5-122">Skupina DPH položek je vyplněna z hlavního účtu.</span><span class="sxs-lookup"><span data-stu-id="82ad5-122">The items sales tax group is populated from the main account.</span></span> <span data-ttu-id="82ad5-123">Pokud hlavní účet nemá skupinu DPH položky, použije se skupina DPH položky z parametrů DPH hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="82ad5-123">If the main account does not have an item sales tax group, then the item sales tax group in the General ledger sales tax parameters is used.</span></span>    
8. <span data-ttu-id="82ad5-124">Zadejte číslo do pole Množství.</span><span class="sxs-lookup"><span data-stu-id="82ad5-124">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="82ad5-125">Množství je volitelné.</span><span class="sxs-lookup"><span data-stu-id="82ad5-125">The quantity is optional.</span></span>  
9. <span data-ttu-id="82ad5-126">Zadejte číslo do pole Jednotková cena.</span><span class="sxs-lookup"><span data-stu-id="82ad5-126">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="82ad5-127">Jednotková cena je volitelná.</span><span class="sxs-lookup"><span data-stu-id="82ad5-127">The unit price is optional.</span></span>  
    * <span data-ttu-id="82ad5-128">Částka se počítá jako součin množství a jednotkové ceny.</span><span class="sxs-lookup"><span data-stu-id="82ad5-128">The amount is calculated as the quantity times the unit price.</span></span> <span data-ttu-id="82ad5-129">Výpočet však lze přepsat a zadat vlastní částku.</span><span class="sxs-lookup"><span data-stu-id="82ad5-129">However, you can override that calculation and enter an amount.</span></span>  
10. <span data-ttu-id="82ad5-130">Kliknutím na položku DPH si můžete zobrazit částku DPH, která byla pro fakturu vypočtena.</span><span class="sxs-lookup"><span data-stu-id="82ad5-130">Click on Sales tax to view the sales tax calculated for your invoice.</span></span>
    * <span data-ttu-id="82ad5-131">Částky DPH si můžete prohlédnout na této stránce nebo je přepsat na záložce Úprava.</span><span class="sxs-lookup"><span data-stu-id="82ad5-131">View the sales tax amounts in this page or you can override the amounts on the Adjustment tab.</span></span>  
11. <span data-ttu-id="82ad5-132">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="82ad5-132">Click OK.</span></span>
12. <span data-ttu-id="82ad5-133">Klepněte na tlačítko Náklady, pokud chcete přidat náklady pro fakturu.</span><span class="sxs-lookup"><span data-stu-id="82ad5-133">Click Charges to add a charge to your invoice.</span></span> 
13. <span data-ttu-id="82ad5-134">Zadejte hodnotu do pole Kód nákladů.</span><span class="sxs-lookup"><span data-stu-id="82ad5-134">In the Charges code field, type a value.</span></span>
14. <span data-ttu-id="82ad5-135">Zadejte číslo do pole Hodnota nákladů.</span><span class="sxs-lookup"><span data-stu-id="82ad5-135">In the Charges value field, enter a number.</span></span>
15. <span data-ttu-id="82ad5-136">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="82ad5-136">Close the page.</span></span>
16. <span data-ttu-id="82ad5-137">Kliknutím na položku Součty si můžete zobrazit podrobnosti a celkové částky souhrnné faktury.</span><span class="sxs-lookup"><span data-stu-id="82ad5-137">Click Totals to view the summary invoice details and totals.</span></span>
17. <span data-ttu-id="82ad5-138">Klikněte na tlačítko Zavřít.</span><span class="sxs-lookup"><span data-stu-id="82ad5-138">Click Close.</span></span>
18. <span data-ttu-id="82ad5-139">Kliknutím na položku Zaúčtovat fakturu zaúčtujte.</span><span class="sxs-lookup"><span data-stu-id="82ad5-139">Click Post to post the invoice.</span></span> <span data-ttu-id="82ad5-140">Před zaúčtováním je možné akci zrušit.</span><span class="sxs-lookup"><span data-stu-id="82ad5-140">You will be able to cancel before you post.</span></span>
    * <span data-ttu-id="82ad5-141">Pokud chcete změnit časování tisku faktur: Vyberte možnost Aktuální pro tisk jednotlivých faktur při jejich aktualizaci, nebo vyberte Po pro tisk po aktualizaci všech faktur.</span><span class="sxs-lookup"><span data-stu-id="82ad5-141">To change the timing of your invoice printing:  Select Current to print each invoice as it is updated   or  Select After to print after all invoices have been updated.</span></span>  
    * <span data-ttu-id="82ad5-142">Pokud chcete změnit způsob, jak chcete kontrolovat úvěrový limit odběratele před zaúčtováním, můžete změnit typ limitu úvěru.</span><span class="sxs-lookup"><span data-stu-id="82ad5-142">If you want to change how the customer's credit limit is checked before posting, change the Credit limit type.</span></span>  
    * <span data-ttu-id="82ad5-143">Pokud chcete vytisknout fakturu, vyberte možnost Ano.</span><span class="sxs-lookup"><span data-stu-id="82ad5-143">If you want to print the invoice, select Yes.</span></span>  
    * <span data-ttu-id="82ad5-144">Pokud chcete zaúčtovat fakturu, vyberte možnost Ano.</span><span class="sxs-lookup"><span data-stu-id="82ad5-144">If you want to post the invoice, select Yes.</span></span> <span data-ttu-id="82ad5-145">Fakturu můžete vytisknout bez zaúčtování.</span><span class="sxs-lookup"><span data-stu-id="82ad5-145">You can print the invoice without posting.</span></span>  
19. <span data-ttu-id="82ad5-146">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="82ad5-146">Click OK.</span></span>


