---
title: Vytvoření volné faktury
description: Toto téma vysvětluje, jak vytvořit volné faktury.
author: mikefalkner
manager: AnnBe
ms.date: 08/24/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 726d4979059417871a00626c55da32fa4286cb53
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4991110"
---
# <a name="create-a-free-text-invoice"></a><span data-ttu-id="5982d-103">Vytvoření volné faktury</span><span class="sxs-lookup"><span data-stu-id="5982d-103">Create a free text invoice</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5982d-104">Toto téma vysvětluje, jak vytvořit volné faktury.</span><span class="sxs-lookup"><span data-stu-id="5982d-104">This topic explains how to create free text invoices.</span></span> <span data-ttu-id="5982d-105">Pro proceduru použijte ukázkovou společnost **USMF**.</span><span class="sxs-lookup"><span data-stu-id="5982d-105">For the procedure, use the **USMF** demo company.</span></span>

## <a name="create-a-free-text-invoice"></a><span data-ttu-id="5982d-106">Vytvořit volnou fakturu</span><span class="sxs-lookup"><span data-stu-id="5982d-106">Create a free text invoice</span></span>

1. <span data-ttu-id="5982d-107">Přejděte na **Pohledávky (nebo Prodejní registr) \> Faktury \> Všechny volné faktury**.</span><span class="sxs-lookup"><span data-stu-id="5982d-107">Go to **Accounts receivable (or Sales Ledger) \> Invoices \> All free text invoices**.</span></span>
2. <span data-ttu-id="5982d-108">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="5982d-108">Select **New**.</span></span>
3. <span data-ttu-id="5982d-109">V poli **Účet odběratele** vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="5982d-109">In the **Customer account** field, select a value.</span></span>

    * <span data-ttu-id="5982d-110">Ve výchozím nastavení se jako účet faktury použije účet, který je zvolen jako účet odběratele.</span><span class="sxs-lookup"><span data-stu-id="5982d-110">By default, the account that is selected as the customer account is used as the invoice account.</span></span>
    * <span data-ttu-id="5982d-111">Pokud nebyla faktura zaúčtována, počátečním účetním stavem je **Zpracovává se**.</span><span class="sxs-lookup"><span data-stu-id="5982d-111">If the invoice isn't posted, the accounting status starts with **In process**.</span></span>
    * <span data-ttu-id="5982d-112">Číslo faktury bude přiřazeno při zaúčtování faktury.</span><span class="sxs-lookup"><span data-stu-id="5982d-112">The invoice number will be assigned when the invoice is posted.</span></span>
    * <span data-ttu-id="5982d-113">Pokud používáte zmocnění SEPA, bude při výběru účtu zákazníka automaticky vyplněno zmocnění.</span><span class="sxs-lookup"><span data-stu-id="5982d-113">If you're using Single Euro Payments Area (SEPA) mandates, the direct debit mandate is automatically entered when you select the customer account.</span></span>

4. <span data-ttu-id="5982d-114">V poli **Popis** zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="5982d-114">In the **Description** field, enter a value.</span></span>
5. <span data-ttu-id="5982d-115">V poli **Hlavní účet** zadejte číslo účtu, které nemá dimenze.</span><span class="sxs-lookup"><span data-stu-id="5982d-115">In the **Main account** field, specify an account number that doesn't have dimensions.</span></span> <span data-ttu-id="5982d-116">Dimenze zadáte později v tomto tématu.</span><span class="sxs-lookup"><span data-stu-id="5982d-116">You will enter dimensions later in this topic.</span></span>

    <span data-ttu-id="5982d-117">Můžete také zadat jeden nebo více znaků pro hlavní účet a vyhledat účet pomocí vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="5982d-117">You can also enter one or more characters for the main account, and use the lookup to find the account.</span></span>

6. <span data-ttu-id="5982d-118">Zvolte pevnou záložku **Podrobnosti řádku**, aby bylo možné přidat dimenze do hlavního účtu.</span><span class="sxs-lookup"><span data-stu-id="5982d-118">Select the **Line details** FastTab to add dimensions to the main account.</span></span>
7. <span data-ttu-id="5982d-119">Zvolte karu **Řádek finančních dimenzí**.</span><span class="sxs-lookup"><span data-stu-id="5982d-119">Select the **Financial dimensions line** tab.</span></span>

    * <span data-ttu-id="5982d-120">Dimenze jsou pouze pro vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="5982d-120">The dimensions are for the selected line only.</span></span>
    * <span data-ttu-id="5982d-121">Výchozí skupina DPH je vyplněna z odběratele.</span><span class="sxs-lookup"><span data-stu-id="5982d-121">The sales tax group is filled in from the customer.</span></span> <span data-ttu-id="5982d-122">Pokud odběratel nemá skupinu DPH, použije se skupina DPH z hlavního účtu.</span><span class="sxs-lookup"><span data-stu-id="5982d-122">If the customer doesn't have a sales tax group, the sales tax group from the main account is used.</span></span>
    * <span data-ttu-id="5982d-123">Skupina DPH položek je vyplněna z hlavního účtu.</span><span class="sxs-lookup"><span data-stu-id="5982d-123">The items sales tax group is filled in from the main account.</span></span> <span data-ttu-id="5982d-124">Pokud hlavní účet nemá skupinu DPH položky, použije se skupina DPH položky určená v parametrech v hlavní knize.</span><span class="sxs-lookup"><span data-stu-id="5982d-124">If the main account doesn't have an item sales tax group, the item sales tax group that is specified in the sales tax parameters in General ledger is used.</span></span>

8. <span data-ttu-id="5982d-125">Volitelné: Zadejte číslo do pole **Množství**.</span><span class="sxs-lookup"><span data-stu-id="5982d-125">Optional: In the **Quantity** field, enter a number.</span></span>
9. <span data-ttu-id="5982d-126">Volitelné: Zadejte číslo do pole **Jednotková cena**.</span><span class="sxs-lookup"><span data-stu-id="5982d-126">Optional: In the **Unit price** field, enter a number.</span></span>

    <span data-ttu-id="5982d-127">Částka se počítá jako součin množství a jednotkové ceny.</span><span class="sxs-lookup"><span data-stu-id="5982d-127">The amount is calculated as the quantity times the unit price.</span></span> <span data-ttu-id="5982d-128">Výpočet však lze přepsat zadáním částky.</span><span class="sxs-lookup"><span data-stu-id="5982d-128">However, you can override that calculation by entering an amount.</span></span>

10. <span data-ttu-id="5982d-129">Zvolte **DPH** pro zobrazení DPH, která bylo pro fakturu vypočtena.</span><span class="sxs-lookup"><span data-stu-id="5982d-129">Select **Sales tax** to view the sales tax that is calculated for the invoice.</span></span>

    <span data-ttu-id="5982d-130">Na této stránce můžete zobrazit částky DPH nebo je můžete přepsat na kartě **Úprava**.</span><span class="sxs-lookup"><span data-stu-id="5982d-130">You can view the sales tax amounts on this page, or you can override the amounts on the **Adjustment** tab.</span></span>

11. <span data-ttu-id="5982d-131">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="5982d-131">Select **OK**.</span></span>
12. <span data-ttu-id="5982d-132">Zvolte **Náklady**, pokud chcete přidat náklady do faktury.</span><span class="sxs-lookup"><span data-stu-id="5982d-132">Select **Charges** to add a charge to the invoice.</span></span>
13. <span data-ttu-id="5982d-133">Zadejte hodnotu do pole **Kód nákladů**.</span><span class="sxs-lookup"><span data-stu-id="5982d-133">In the **Charges code** field, enter a value.</span></span>
14. <span data-ttu-id="5982d-134">Zadejte číslo do pole **Hodnota nákladů**.</span><span class="sxs-lookup"><span data-stu-id="5982d-134">In the **Charges value** field, enter a number.</span></span>
15. <span data-ttu-id="5982d-135">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="5982d-135">Close the page.</span></span>
16. <span data-ttu-id="5982d-136">Zvolte **Součty** pro zobrazení podrobností a celkové částky souhrnné faktury.</span><span class="sxs-lookup"><span data-stu-id="5982d-136">Select **Totals** to view a summary of the invoice details and totals.</span></span>
17. <span data-ttu-id="5982d-137">Vyberte **Zavřít**.</span><span class="sxs-lookup"><span data-stu-id="5982d-137">Select **Close**.</span></span>
18. <span data-ttu-id="5982d-138">Vyberte **Zaúčtovat** pro zaúčtování faktury.</span><span class="sxs-lookup"><span data-stu-id="5982d-138">Select **Post** to post the invoice.</span></span> <span data-ttu-id="5982d-139">Stále budete mít možnost zrušení před skutečným účtováním.</span><span class="sxs-lookup"><span data-stu-id="5982d-139">You will still have an opportunity to cancel before you actually post.</span></span>

    * <span data-ttu-id="5982d-140">Můžete změnit časování tisku faktury.</span><span class="sxs-lookup"><span data-stu-id="5982d-140">You can change the timing of invoice printing.</span></span> <span data-ttu-id="5982d-141">Výběrem **Aktuální** vytisknete jednotlivé faktury při aktualizaci.</span><span class="sxs-lookup"><span data-stu-id="5982d-141">Select **Current** to print each invoice as it's updated.</span></span> <span data-ttu-id="5982d-142">Výběrem **Po** vytisknete všechny faktury po aktualizaci.</span><span class="sxs-lookup"><span data-stu-id="5982d-142">Select **After** to print after all invoices have been updated.</span></span>
    * <span data-ttu-id="5982d-143">Pokud chcete změnit ověření limitu úvěru odběratele před zaúčtováním faktury, změňte hodnoty v **typ limitu úvěru** pole.</span><span class="sxs-lookup"><span data-stu-id="5982d-143">To change how the customer's credit limit is verified before the invoice is posted, change the value in the **Credit limit type** field.</span></span>
    * <span data-ttu-id="5982d-144">Volbou možnosti **Ano** vytisknete fakturu.</span><span class="sxs-lookup"><span data-stu-id="5982d-144">To print the invoice, set the option to **Yes**.</span></span>
    * <span data-ttu-id="5982d-145">Volbou možnosti **Ano** zaúčtujete fakturu.</span><span class="sxs-lookup"><span data-stu-id="5982d-145">To post the invoice, set the option to **Yes**.</span></span> <span data-ttu-id="5982d-146">Fakturu můžete vytisknout bez jejího zaúčtování.</span><span class="sxs-lookup"><span data-stu-id="5982d-146">You can print the invoice without posting it.</span></span>

19. <span data-ttu-id="5982d-147">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="5982d-147">Select **OK**.</span></span>

## <a name="copy-lines"></a><span data-ttu-id="5982d-148">Kopírovat řádky</span><span class="sxs-lookup"><span data-stu-id="5982d-148">Copy lines</span></span>
<span data-ttu-id="5982d-149">Chcete-li zkopírovat řádky volné faktury, vyberte jeden nebo více řádků a zvolte **Kopírovat vybrané řádky**.</span><span class="sxs-lookup"><span data-stu-id="5982d-149">To copy lines on a free text invoice, select one or more lines, and then select **Copy selected lines**.</span></span> <span data-ttu-id="5982d-150">Můžete určit počet kopií, které chcete vytvořit, a můžete také zkopírovat poznámky a přílohy.</span><span class="sxs-lookup"><span data-stu-id="5982d-150">You can specify the number of copies to make, and you can also copy notes and attachments.</span></span> <span data-ttu-id="5982d-151">Můžete buď zkopírovat distribuce nebo umožnit jejich opětovné vytvoření při zaúčtování.</span><span class="sxs-lookup"><span data-stu-id="5982d-151">You can either copy the distributions or let them be re-created when you post.</span></span>

<span data-ttu-id="5982d-152">Jakmile zkopírujete řádky, lze podle potřeby upravit informace.</span><span class="sxs-lookup"><span data-stu-id="5982d-152">After you copy lines, you can edit the information as you require.</span></span>

## <a name="create-a-free-text-invoice-from-a-template"></a><span data-ttu-id="5982d-153">Vytvoření volné faktury ze šablony</span><span class="sxs-lookup"><span data-stu-id="5982d-153">Create a free text invoice from a template</span></span>
<span data-ttu-id="5982d-154">Můžete vytvořit volnou fakturu ze šablony.</span><span class="sxs-lookup"><span data-stu-id="5982d-154">You can create a free text invoice from a template.</span></span> <span data-ttu-id="5982d-155">Vyberete-li **Nová ze šablony** na kartě **Faktura**, můžete vybrat název šablony a účet odběratele pro novou volnou fakturu.</span><span class="sxs-lookup"><span data-stu-id="5982d-155">When you select **New from template** on the **Invoice** tab, you can select a template name and the customer account for the new free text invoice.</span></span> <span data-ttu-id="5982d-156">Výchozí hodnoty, jako jsou například platební podmínky a způsob platby, lze automaticky vyplnit z odběratele, nebo můžete použít hodnoty, které byly uloženy v šabloně.</span><span class="sxs-lookup"><span data-stu-id="5982d-156">Default values, such as the terms of payment and method of payment, can be automatically filled in from the customer, or you can use the values that were saved in the template.</span></span>

<span data-ttu-id="5982d-157">Bude vytvořena nová volná faktura a můžete upravit hodnoty podle potřeby.</span><span class="sxs-lookup"><span data-stu-id="5982d-157">A new free text invoice is created, and you can edit the values as you require.</span></span>
