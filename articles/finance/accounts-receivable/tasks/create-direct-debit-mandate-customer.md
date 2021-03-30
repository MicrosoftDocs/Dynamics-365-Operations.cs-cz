---
title: Vytvoření zmocnění k přímému debetu pro odběratele
description: Tento průvodce úkolem ukazuje, jak vytvořit zmocnění k přímému debetu a použít je ve faktuře.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, CustBankAccounts, BankAccountTable, CustPaymMode, CustDirectDebitMandate, BankAccountTableLookUp, SrsReportViewerForm,  LogisticsAddressCityLookup, CustFreeInvoice, CustTableLookup
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ef9beae6769c361680832d81ddda00e1237d3297
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5241627"
---
# <a name="create-a-direct-debit-mandate-for-a-customer"></a><span data-ttu-id="0bde4-103">Vytvoření zmocnění k přímému debetu pro odběratele</span><span class="sxs-lookup"><span data-stu-id="0bde4-103">Create a direct debit mandate for a customer</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0bde4-104">Tento průvodce úkolem ukazuje, jak vytvořit zmocnění k přímému debetu a použít je ve faktuře.</span><span class="sxs-lookup"><span data-stu-id="0bde4-104">This task guide demonstrates how to create a direct debit mandate and use it on an invoice.</span></span>


## <a name="create-a-bank-account"></a><span data-ttu-id="0bde4-105">Vytvoření bankovního účtu</span><span class="sxs-lookup"><span data-stu-id="0bde4-105">Create a bank account</span></span>
1. <span data-ttu-id="0bde4-106">V **navigační podokně** přejděte na **Moduly > Pohledávky > Odběratelé > Všichni odběratelé**.</span><span class="sxs-lookup"><span data-stu-id="0bde4-106">In the **Navigation pane**, go to **Modules > Accounts receivable > Customers > All customers**.</span></span>
2. <span data-ttu-id="0bde4-107">V seznamu vyberte záznam.</span><span class="sxs-lookup"><span data-stu-id="0bde4-107">In the list, select a record.</span></span> <span data-ttu-id="0bde4-108">Vyberte například US-001.</span><span class="sxs-lookup"><span data-stu-id="0bde4-108">For example, select US-001</span></span>
3. <span data-ttu-id="0bde4-109">V podokně akcí klikněte na možnost **Odběratel**.</span><span class="sxs-lookup"><span data-stu-id="0bde4-109">On the Action Pane, click **Customer**.</span></span>
4. <span data-ttu-id="0bde4-110">Klikněte na možnost **Bankovní účty**.</span><span class="sxs-lookup"><span data-stu-id="0bde4-110">Click **Bank accounts**.</span></span>
5. <span data-ttu-id="0bde4-111">Klepněte na možnost **Nový**.</span><span class="sxs-lookup"><span data-stu-id="0bde4-111">Click **New**.</span></span>
6. <span data-ttu-id="0bde4-112">Zadejte hodnotu do pole **Bankovní účet**.</span><span class="sxs-lookup"><span data-stu-id="0bde4-112">In the **Bank account** field, type a value.</span></span>
7. <span data-ttu-id="0bde4-113">Zadejte hodnotu do pole **Název**.</span><span class="sxs-lookup"><span data-stu-id="0bde4-113">In the **Name** field, type a value.</span></span>
8. <span data-ttu-id="0bde4-114">Zadejte hodnotu do pole **IBAN**.</span><span class="sxs-lookup"><span data-stu-id="0bde4-114">In the **IBAN** field, type a value.</span></span>
9. <span data-ttu-id="0bde4-115">Zadejte hodnotu do pole **Měna**.</span><span class="sxs-lookup"><span data-stu-id="0bde4-115">In the **Currency** field, type a value.</span></span>
10. <span data-ttu-id="0bde4-116">Klikněte na možnost **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="0bde4-116">Click **Save**.</span></span>
11. <span data-ttu-id="0bde4-117">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="0bde4-117">Close the page.</span></span>
12. <span data-ttu-id="0bde4-118">V **navigačním podokně** přejděte na **Moduly > Správa hotovosti a banky > Bankovní účty > Bankovní účty**.</span><span class="sxs-lookup"><span data-stu-id="0bde4-118">In the **Navigation pane**, go to **Modules > Cash and bank management > Bank accounts > Bank accounts**.</span></span>
13. <span data-ttu-id="0bde4-119">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="0bde4-119">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="0bde4-120">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="0bde4-120">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="0bde4-121">Klikněte na možnost **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="0bde4-121">Click **Edit**.</span></span>
16. <span data-ttu-id="0bde4-122">Rozbalte záložku s náhledem **Další identifikace**.</span><span class="sxs-lookup"><span data-stu-id="0bde4-122">Expand the **Additional identification** fastTab.</span></span>
17. <span data-ttu-id="0bde4-123">Zadejte hodnotu do pole **ID přímého debetu**.</span><span class="sxs-lookup"><span data-stu-id="0bde4-123">In the **Direct debit ID** field, type a value.</span></span>
18. <span data-ttu-id="0bde4-124">Zadejte hodnotu do pole **IBAN**.</span><span class="sxs-lookup"><span data-stu-id="0bde4-124">In the **IBAN** field, type a value.</span></span>
19. <span data-ttu-id="0bde4-125">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="0bde4-125">Close the page.</span></span>
20. <span data-ttu-id="0bde4-126">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="0bde4-126">Close the page.</span></span>

## <a name="define-the-electronic-payment-method"></a><span data-ttu-id="0bde4-127">Definování metody elektronické platby</span><span class="sxs-lookup"><span data-stu-id="0bde4-127">Define the electronic payment method</span></span>
1. <span data-ttu-id="0bde4-128">V **navigačním podokně** přejděte na **Moduly > Pohledávky > Nastavení plateb > Metody platby**.</span><span class="sxs-lookup"><span data-stu-id="0bde4-128">In the **Navigation pane**, go to **Modules > Accounts receivable > Payments setup > Methods of payment**.</span></span>
2. <span data-ttu-id="0bde4-129">Klepněte na možnost **Nový**.</span><span class="sxs-lookup"><span data-stu-id="0bde4-129">Click **New**.</span></span>
3. <span data-ttu-id="0bde4-130">V poli **Způsob platby** zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="0bde4-130">In the **Method of payment** field, type a value.</span></span>
4. <span data-ttu-id="0bde4-131">Zadejte hodnotu do pole **Popis**.</span><span class="sxs-lookup"><span data-stu-id="0bde4-131">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="0bde4-132">V poli **Typ platby** zadejte „Elektronická platba“.</span><span class="sxs-lookup"><span data-stu-id="0bde4-132">In the **Payment type** field, enter 'Electronic payment'.</span></span> <span data-ttu-id="0bde4-133">Typ platby pro metodu platby „zmocnění k přímému debetu“ musí být elektronická platba.</span><span class="sxs-lookup"><span data-stu-id="0bde4-133">The payment type for a direct debit mandate method of payment must be Electronic payment.</span></span>
6. <span data-ttu-id="0bde4-134">Vyberte možnost Ano v poli **Požadovat zmocnění**.</span><span class="sxs-lookup"><span data-stu-id="0bde4-134">Select Yes in the **Require mandate** field.</span></span>
7. <span data-ttu-id="0bde4-135">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="0bde4-135">Close the page.</span></span>

## <a name="add-a-direct-debit-mandate-to-a-customer"></a><span data-ttu-id="0bde4-136">Přidejte zmocnění k přímému debetu zákazníkovi.</span><span class="sxs-lookup"><span data-stu-id="0bde4-136">Add a direct debit mandate to a customer.</span></span>
1. <span data-ttu-id="0bde4-137">V **navigační podokně** přejděte na **Moduly > Pohledávky > Odběratelé > Všichni odběratelé**.</span><span class="sxs-lookup"><span data-stu-id="0bde4-137">In the **Navigation pane**, go to **Modules > Accounts receivable > Customers > All customers**.</span></span>
2. <span data-ttu-id="0bde4-138">V seznamu vyberte záznam.</span><span class="sxs-lookup"><span data-stu-id="0bde4-138">In the list, select a record.</span></span> <span data-ttu-id="0bde4-139">Vyberte například US-001.</span><span class="sxs-lookup"><span data-stu-id="0bde4-139">For example, select US-001</span></span>
3. <span data-ttu-id="0bde4-140">Klikněte na možnost **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="0bde4-140">Click **Edit**.</span></span>
4. <span data-ttu-id="0bde4-141">Rozbalte záložku s náhledem **Výchozí nastavení plateb**.</span><span class="sxs-lookup"><span data-stu-id="0bde4-141">Expand the **Payment defaults** fastTab.</span></span>
5. <span data-ttu-id="0bde4-142">V poli **Metody platby** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="0bde4-142">In the **Method of payment** field, enter or select a value.</span></span>
6. <span data-ttu-id="0bde4-143">Rozbalte záložku s náhledem **Výchozí nastavení plateb**.</span><span class="sxs-lookup"><span data-stu-id="0bde4-143">Expand the **Payment defaults** fastTab.</span></span>
7. <span data-ttu-id="0bde4-144">Rozbalte záložku s náhledem **Zmocnění k přímému debetu**.</span><span class="sxs-lookup"><span data-stu-id="0bde4-144">Expand the **Direct debit mandates** fastTab.</span></span>
8. <span data-ttu-id="0bde4-145">Klikněte na tlačítko **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="0bde4-145">Click **Add**.</span></span>
9. <span data-ttu-id="0bde4-146">V poli **Bankovní účet** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="0bde4-146">In the **Bank account** field, enter or select a value.</span></span>
10. <span data-ttu-id="0bde4-147">V poli **Bankovní účet věřitele** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="0bde4-147">In the **Creditor bank account** field, enter or select a value.</span></span>
11. <span data-ttu-id="0bde4-148">V poli **Četnost plateb** zadejte počet plateb, u kterých očekáváte, že budou zpracovány pro zmocnění.</span><span class="sxs-lookup"><span data-stu-id="0bde4-148">In the **Payment frequency** field, enter the number of payments that you expect to process for this mandate.</span></span>
12. <span data-ttu-id="0bde4-149">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="0bde4-149">Click **OK**.</span></span>
13. <span data-ttu-id="0bde4-150">Klepněte na položku **Tisk**.</span><span class="sxs-lookup"><span data-stu-id="0bde4-150">Click **Print**.</span></span>
14. <span data-ttu-id="0bde4-151">Klikněte na **Sestava zmocnění**.</span><span class="sxs-lookup"><span data-stu-id="0bde4-151">Click **Mandate report**.</span></span>
15. <span data-ttu-id="0bde4-152">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="0bde4-152">Close the page.</span></span>
16. <span data-ttu-id="0bde4-153">Klikněte na možnost **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="0bde4-153">Click **Edit**.</span></span>
17. <span data-ttu-id="0bde4-154">Do pole **Datum podpisu** zadejte datum.</span><span class="sxs-lookup"><span data-stu-id="0bde4-154">In the **Signature date** field, enter a date.</span></span>
18. <span data-ttu-id="0bde4-155">Klepněte na tlačítko **Ano**.</span><span class="sxs-lookup"><span data-stu-id="0bde4-155">Click **Yes**.</span></span>
19. <span data-ttu-id="0bde4-156">Zadejte místo podpisu zmocnění.</span><span class="sxs-lookup"><span data-stu-id="0bde4-156">Enter the location where the mandate was signed.</span></span>
20. <span data-ttu-id="0bde4-157">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="0bde4-157">Click **OK**.</span></span>
21. <span data-ttu-id="0bde4-158">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="0bde4-158">Close the page.</span></span>

## <a name="create-a-free-text-invoice-with-mandate"></a><span data-ttu-id="0bde4-159">Vytvoření volné faktury se zmocněním</span><span class="sxs-lookup"><span data-stu-id="0bde4-159">Create a free text invoice with mandate</span></span>
1. <span data-ttu-id="0bde4-160">V **podokně navigace** přejděte na **Moduly > Pohledávky > Faktury > Všechny otevřené faktury**.</span><span class="sxs-lookup"><span data-stu-id="0bde4-160">In the **Navigation pane**, go to **Modules > Accounts receivable > Invoices > All free text invoices**.</span></span>
2. <span data-ttu-id="0bde4-161">Klepněte na možnost **Nový**.</span><span class="sxs-lookup"><span data-stu-id="0bde4-161">Click **New**.</span></span>
3. <span data-ttu-id="0bde4-162">Vyberte odběratele, pro kterého jste vybrali zmocnění.</span><span class="sxs-lookup"><span data-stu-id="0bde4-162">Select the customer that you added the mandate to.</span></span>
4. <span data-ttu-id="0bde4-163">V poli **ID zmocnění k přímému debetu** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="0bde4-163">In the **Direct debit mandate ID** field, enter or select a value.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]