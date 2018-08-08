--- 
title: "Vytvořit volnou fakturu"
description: "Tento článek ukazuje, jak vytvořit volnou fakturu."
author: mikefalkner
manager: AnnBe
ms.date: 05/29/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: e6f89a6d77ff8e1cd88632df0d9a72915086ee1e
ms.contentlocale: cs-cz
ms.lasthandoff: 08/07/2018

---

# <a name="create-a-free-text-invoice"></a><span data-ttu-id="168f1-103">Vytvořit volnou fakturu</span><span class="sxs-lookup"><span data-stu-id="168f1-103">Create a free text invoice</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="168f1-104">Tento článek ukazuje, jak vytvořit volnou fakturu.</span><span class="sxs-lookup"><span data-stu-id="168f1-104">This article demonstrates how to create a free text invoice.</span></span> <span data-ttu-id="168f1-105">Pro tuto proceduru použijte ukázkovou společnost USMF.</span><span class="sxs-lookup"><span data-stu-id="168f1-105">For this procedure, use the USMF demo company.</span></span>

## <a name="create-a-free-text-invoice"></a><span data-ttu-id="168f1-106">Vytvořit volnou fakturu</span><span class="sxs-lookup"><span data-stu-id="168f1-106">Create a free text invoice</span></span>

1. <span data-ttu-id="168f1-107">Přejděte na Pohledávky > Faktury > Všechny volné faktury.</span><span class="sxs-lookup"><span data-stu-id="168f1-107">Go to Accounts receivable > Invoices > All free text invoices.</span></span>
2. <span data-ttu-id="168f1-108">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="168f1-108">Click New.</span></span>
3. <span data-ttu-id="168f1-109">V poli Účet odběratele vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="168f1-109">In the Customer account field, select a value.</span></span>
    * <span data-ttu-id="168f1-110">Jako výchozí účet faktury bude nastaven stejný účet, jaký byl použit pro účet odběratele.</span><span class="sxs-lookup"><span data-stu-id="168f1-110">The invoice account will default to the same account used for the customer account.</span></span>   
    * <span data-ttu-id="168f1-111">Pokud nebyla faktura zaúčtována, počátečním účetním stavem je Zpracovává se.</span><span class="sxs-lookup"><span data-stu-id="168f1-111">The accounting status starts with In process if the invoice is not posted.</span></span>   
    * <span data-ttu-id="168f1-112">Číslo faktury bude přiřazeno při zaúčtování faktury.</span><span class="sxs-lookup"><span data-stu-id="168f1-112">The invoice number will be assigned when the invoice is posted.</span></span>  
    * <span data-ttu-id="168f1-113">Pokud používáte zmocnění SEPA, ve zmocnění k přímému debetu bude při výběru účtu zákazníka automaticky vyplněno zmocnění.</span><span class="sxs-lookup"><span data-stu-id="168f1-113">If you are using SEPA mandates, the direct debit mandate will be automatically populated with a mandate when you select the customer account.</span></span>  
4. <span data-ttu-id="168f1-114">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="168f1-114">In the Description field, type a value.</span></span>
5. <span data-ttu-id="168f1-115">V poli Hlavní účet zadejte číslo účtu bez dimenze.</span><span class="sxs-lookup"><span data-stu-id="168f1-115">In the Main account field, specify an account number without dimensions.</span></span>
    * <span data-ttu-id="168f1-116">Můžete také zadat jeden nebo více znaků pro hlavní účet a vyhledat účet pomocí vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="168f1-116">You can also enter one or more characters for the main account and use the lookup to find your account.</span></span> <span data-ttu-id="168f1-117">Dimenze zadáte později v této příručce.</span><span class="sxs-lookup"><span data-stu-id="168f1-117">You will enter dimensions later on in this guide.</span></span>  
6. <span data-ttu-id="168f1-118">Rozbalte pevnou záložku Podrobnosti řádku, aby bylo možné přidat dimenze do hlavního účtu.</span><span class="sxs-lookup"><span data-stu-id="168f1-118">Expand the Line details fasttab so you can add dimensions to your main account.</span></span>
7. <span data-ttu-id="168f1-119">Klikněte na záložku Řádek finančních dimenzí.</span><span class="sxs-lookup"><span data-stu-id="168f1-119">Click the Financial dimensions line tab.</span></span>
    * <span data-ttu-id="168f1-120">Dimenze jsou pouze pro vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="168f1-120">The dimensions are for the selected line only.</span></span>    
    * <span data-ttu-id="168f1-121">Skupina prodejní daně je vyplněna z údajů odběratele.</span><span class="sxs-lookup"><span data-stu-id="168f1-121">The sales tax group is populated from the customer.</span></span> <span data-ttu-id="168f1-122">Pokud odběratel nemá skupinu DPH, použije se skupina DPH z hlavního účtu.</span><span class="sxs-lookup"><span data-stu-id="168f1-122">If the customer does not have a sales tax group, the sales tax group from the main account is used.</span></span>  
    * <span data-ttu-id="168f1-123">Skupina DPH položek je vyplněna z hlavního účtu.</span><span class="sxs-lookup"><span data-stu-id="168f1-123">The items sales tax group is populated from the main account.</span></span> <span data-ttu-id="168f1-124">Pokud hlavní účet nemá skupinu DPH položky, použije se skupina DPH položky z parametrů DPH hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="168f1-124">If the main account does not have an item sales tax group, then the item sales tax group in the General ledger sales tax parameters is used.</span></span>    
8. <span data-ttu-id="168f1-125">Zadejte číslo do pole Množství.</span><span class="sxs-lookup"><span data-stu-id="168f1-125">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="168f1-126">Množství je volitelné.</span><span class="sxs-lookup"><span data-stu-id="168f1-126">The quantity is optional.</span></span>  
9. <span data-ttu-id="168f1-127">Zadejte číslo do pole Jednotková cena.</span><span class="sxs-lookup"><span data-stu-id="168f1-127">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="168f1-128">Jednotková cena je volitelná.</span><span class="sxs-lookup"><span data-stu-id="168f1-128">The unit price is optional.</span></span>  
    * <span data-ttu-id="168f1-129">Částka se počítá jako součin množství a jednotkové ceny.</span><span class="sxs-lookup"><span data-stu-id="168f1-129">The amount is calculated as the quantity times the unit price.</span></span> <span data-ttu-id="168f1-130">Výpočet však lze přepsat a zadat vlastní částku.</span><span class="sxs-lookup"><span data-stu-id="168f1-130">However, you can override that calculation and enter an amount.</span></span>  
10. <span data-ttu-id="168f1-131">Kliknutím na položku DPH si můžete zobrazit částku DPH, která byla pro fakturu vypočtena.</span><span class="sxs-lookup"><span data-stu-id="168f1-131">Click on Sales tax to view the sales tax calculated for your invoice.</span></span>
    * <span data-ttu-id="168f1-132">Částky DPH si můžete prohlédnout na této stránce nebo je přepsat na záložce Úprava.</span><span class="sxs-lookup"><span data-stu-id="168f1-132">View the sales tax amounts in this page or you can override the amounts on the Adjustment tab.</span></span>  
11. <span data-ttu-id="168f1-133">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="168f1-133">Click OK.</span></span>
12. <span data-ttu-id="168f1-134">Klepněte na tlačítko Náklady, pokud chcete přidat náklady pro fakturu.</span><span class="sxs-lookup"><span data-stu-id="168f1-134">Click Charges to add a charge to your invoice.</span></span> 
13. <span data-ttu-id="168f1-135">Zadejte hodnotu do pole Kód nákladů.</span><span class="sxs-lookup"><span data-stu-id="168f1-135">In the Charges code field, type a value.</span></span>
14. <span data-ttu-id="168f1-136">Zadejte číslo do pole Hodnota nákladů.</span><span class="sxs-lookup"><span data-stu-id="168f1-136">In the Charges value field, enter a number.</span></span>
15. <span data-ttu-id="168f1-137">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="168f1-137">Close the page.</span></span>
16. <span data-ttu-id="168f1-138">Kliknutím na položku Součty si můžete zobrazit podrobnosti a celkové částky souhrnné faktury.</span><span class="sxs-lookup"><span data-stu-id="168f1-138">Click Totals to view the summary invoice details and totals.</span></span>
17. <span data-ttu-id="168f1-139">Klikněte na tlačítko Zavřít.</span><span class="sxs-lookup"><span data-stu-id="168f1-139">Click Close.</span></span>
18. <span data-ttu-id="168f1-140">Kliknutím na položku Zaúčtovat fakturu zaúčtujte.</span><span class="sxs-lookup"><span data-stu-id="168f1-140">Click Post to post the invoice.</span></span> <span data-ttu-id="168f1-141">Před zaúčtováním je možné akci zrušit.</span><span class="sxs-lookup"><span data-stu-id="168f1-141">You will be able to cancel before you post.</span></span>
    * <span data-ttu-id="168f1-142">Pokud chcete změnit časování tisku faktur: Vyberte možnost Aktuální pro tisk jednotlivých faktur při jejich aktualizaci, nebo vyberte Po pro tisk po aktualizaci všech faktur.</span><span class="sxs-lookup"><span data-stu-id="168f1-142">To change the timing of your invoice printing:  Select Current to print each invoice as it is updated   or  Select After to print after all invoices have been updated.</span></span>  
    * <span data-ttu-id="168f1-143">Pokud chcete změnit způsob, jak chcete kontrolovat úvěrový limit odběratele před zaúčtováním, můžete změnit typ limitu úvěru.</span><span class="sxs-lookup"><span data-stu-id="168f1-143">If you want to change how the customer's credit limit is checked before posting, change the Credit limit type.</span></span>  
    * <span data-ttu-id="168f1-144">Pokud chcete vytisknout fakturu, vyberte možnost Ano.</span><span class="sxs-lookup"><span data-stu-id="168f1-144">If you want to print the invoice, select Yes.</span></span>  
    * <span data-ttu-id="168f1-145">Pokud chcete zaúčtovat fakturu, vyberte možnost Ano.</span><span class="sxs-lookup"><span data-stu-id="168f1-145">If you want to post the invoice, select Yes.</span></span> <span data-ttu-id="168f1-146">Fakturu můžete vytisknout bez zaúčtování.</span><span class="sxs-lookup"><span data-stu-id="168f1-146">You can print the invoice without posting.</span></span>  
19. <span data-ttu-id="168f1-147">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="168f1-147">Click OK.</span></span>

## <a name="copy-lines"></a><span data-ttu-id="168f1-148">Kopírovat řádky</span><span class="sxs-lookup"><span data-stu-id="168f1-148">Copy lines</span></span>
<span data-ttu-id="168f1-149">Chcete-li zkopírovat řádky volné faktury, vyberte jeden nebo více řádků a klikněte na Kopírovat vybrané řádky.</span><span class="sxs-lookup"><span data-stu-id="168f1-149">To copy lines on the free text invoice, select one or more lines and then click Copy selected lines.</span></span> <span data-ttu-id="168f1-150">Můžete určit počet kopií, které chcete vytvořit, a můžete také zkopírovat poznámky a přílohy.</span><span class="sxs-lookup"><span data-stu-id="168f1-150">You can specify the number of copies that you want to make, and you can also copy notes and attachments.</span></span> <span data-ttu-id="168f1-151">Můžete zkopírovat distribuce nebo umožnit jejich opětovné vytvoření při zaúčtování.</span><span class="sxs-lookup"><span data-stu-id="168f1-151">You can copy the distributions or allow them to be recreated when you post.</span></span> <span data-ttu-id="168f1-152">Jakmile zkopírujete řádky, lze podle potřeby upravit informace.</span><span class="sxs-lookup"><span data-stu-id="168f1-152">Once you copy the lines, you can edit the information as needed.</span></span> 

## <a name="create-a-free-text-invoice-from-a-template"></a><span data-ttu-id="168f1-153">Vytvoření volné faktury ze šablony</span><span class="sxs-lookup"><span data-stu-id="168f1-153">Create a free text invoice from a template</span></span>
<span data-ttu-id="168f1-154">Můžete vytvořit volnou fakturu ze šablony.</span><span class="sxs-lookup"><span data-stu-id="168f1-154">You can create a free text invoice from a template.</span></span> <span data-ttu-id="168f1-155">Vyberete-li Nová ze šablony na kartě Faktura, můžete vybrat název šablony a účet odběratele pro novou volnou fakturu.</span><span class="sxs-lookup"><span data-stu-id="168f1-155">When you select New from template from the Invoice tab, you can select a template name and the customer account for the new free text invoice.</span></span> <span data-ttu-id="168f1-156">Lze vybrat také výchozí hodnoty, jako jsou například platební podmínky a způsob platby od odběratele, nebo použít hodnoty, které byly uloženy se šablonou.</span><span class="sxs-lookup"><span data-stu-id="168f1-156">You can also choose to default values such as the terms of payment and method of payment from the customer or use the values that were saved with the template.</span></span> <span data-ttu-id="168f1-157">Bude vytvořena nová volná faktura a můžete upravit hodnoty uvedené faktury.</span><span class="sxs-lookup"><span data-stu-id="168f1-157">A new free text invoice will be created and you can edit the values in that invoice.</span></span> 


