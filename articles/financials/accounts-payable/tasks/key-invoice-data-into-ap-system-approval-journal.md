--- 
title: "Zadání dat faktury do závazků s použitím deníku schválení"
description: "Tento průvodce úkolem popisuje použití registru faktur k vytvoření faktur a použití deníku schválení pro aktualizaci účtů výdajů."
author: abruer
manager: AnnBe
ms.date: 11/15/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 7a921d7987002310d6a7d7fc78457aaa0cf1d990
ms.contentlocale: cs-cz
ms.lasthandoff: 05/08/2018

---
# <a name="key-invoice-data-into-accounts-payable-using-an-approval-journal"></a><span data-ttu-id="e5800-103">Zadání dat faktury do závazků s použitím deníku schválení</span><span class="sxs-lookup"><span data-stu-id="e5800-103">Key invoice data into accounts payable using an approval journal</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e5800-104">Tento průvodce úkolem popisuje použití registru faktur k vytvoření faktur a použití deníku schválení pro aktualizaci účtů výdajů.</span><span class="sxs-lookup"><span data-stu-id="e5800-104">This task guide will show you how to use the invoice register to create invoices and then use the approval journal to update the expense accounts.</span></span>


## <a name="create-and-post-and-invoice"></a><span data-ttu-id="e5800-105">Vytvoření a zaúčtování faktury</span><span class="sxs-lookup"><span data-stu-id="e5800-105">Create and post and invoice</span></span>
1. <span data-ttu-id="e5800-106">Přejděte na Závazky > Faktury > Registr faktur.</span><span class="sxs-lookup"><span data-stu-id="e5800-106">Go to Accounts payable > Invoices > Invoice register.</span></span>
2. <span data-ttu-id="e5800-107">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="e5800-107">Click New.</span></span>
3. <span data-ttu-id="e5800-108">Vyberte název registru faktury, který chcete použít.</span><span class="sxs-lookup"><span data-stu-id="e5800-108">Select the name of the invoice register that you want to use.</span></span>
4. <span data-ttu-id="e5800-109">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="e5800-109">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="e5800-110">Kliknutím na Řádky otevřete registr a zadejte řádky výdajů.</span><span class="sxs-lookup"><span data-stu-id="e5800-110">Click on Lines to open the register and enter expense lines.</span></span>
6. <span data-ttu-id="e5800-111">Vyberte dodavatele.</span><span class="sxs-lookup"><span data-stu-id="e5800-111">Select a vendor.</span></span> <span data-ttu-id="e5800-112">Například zadejte nebo vyberte možnost US-104</span><span class="sxs-lookup"><span data-stu-id="e5800-112">For example, enter or select US-104</span></span>
7. <span data-ttu-id="e5800-113">Zadejte hodnotu do pole Faktura.</span><span class="sxs-lookup"><span data-stu-id="e5800-113">In the Invoice field, type a value.</span></span>
8. <span data-ttu-id="e5800-114">Zadejte hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="e5800-114">In the Description field, type a value.</span></span>
9. <span data-ttu-id="e5800-115">V poli Dobropis zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="e5800-115">In the Credit field, enter a number.</span></span>
10. <span data-ttu-id="e5800-116">V poli Schválil(a) kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="e5800-116">In the Approved by field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="e5800-117">Vyberte schvalujícího a kliknutím na tlačítko Vybrat tohoto schvalovatele vyberte.</span><span class="sxs-lookup"><span data-stu-id="e5800-117">Highlight an approver and click Select to select that approver.</span></span>
12. <span data-ttu-id="e5800-118">Klikněte na položku Zaúčtovat.</span><span class="sxs-lookup"><span data-stu-id="e5800-118">Click Post.</span></span>
13. <span data-ttu-id="e5800-119">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="e5800-119">Close the page.</span></span>
14. <span data-ttu-id="e5800-120">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="e5800-120">Close the page.</span></span>

## <a name="approve-an-invoice"></a><span data-ttu-id="e5800-121">Schválení faktury</span><span class="sxs-lookup"><span data-stu-id="e5800-121">Approve an invoice</span></span>
1. <span data-ttu-id="e5800-122">Přejděte na Závazky > Faktury > Schválení faktury.</span><span class="sxs-lookup"><span data-stu-id="e5800-122">Go to Accounts payable > Invoices > Invoice approval.</span></span>
2. <span data-ttu-id="e5800-123">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="e5800-123">Click New.</span></span>
3. <span data-ttu-id="e5800-124">Vyberte název deníku schválení faktur, který chcete použít.</span><span class="sxs-lookup"><span data-stu-id="e5800-124">Select the name of the invoice approval journal that you want to use.</span></span>
4. <span data-ttu-id="e5800-125">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="e5800-125">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="e5800-126">Kliknutím na položku Řádky zobrazte stránku, kde bude možné vybrat faktury, které chcete schválit.</span><span class="sxs-lookup"><span data-stu-id="e5800-126">Click lines to display a page where you will be able to select the invoices that you want to approve.</span></span>
6. <span data-ttu-id="e5800-127">Výběrem možnosti Hledat doklady zobrazte všechny faktury, které jsou již připraveny ke schválení.</span><span class="sxs-lookup"><span data-stu-id="e5800-127">Select Find Vouchers to display all of the invoices that are ready for approval.</span></span>
7. <span data-ttu-id="e5800-128">Označte fakturu, kterou jste vytvořili.</span><span class="sxs-lookup"><span data-stu-id="e5800-128">Mark the invoice that you created.</span></span>
8. <span data-ttu-id="e5800-129">Klepněte na tlačítko Vybrat.</span><span class="sxs-lookup"><span data-stu-id="e5800-129">Click Select.</span></span>
    * <span data-ttu-id="e5800-130">Doklady vybrané výše, se po výběru přesunou do tohoto seznamu.</span><span class="sxs-lookup"><span data-stu-id="e5800-130">The vouchers that you selected above are moved to this list after you select them.</span></span>  
9. <span data-ttu-id="e5800-131">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="e5800-131">Click OK.</span></span>
10. <span data-ttu-id="e5800-132">Klepnutím na pole číslo účtu přidejte výdajový účet k faktuře.</span><span class="sxs-lookup"><span data-stu-id="e5800-132">Click on the account number field to add an expense account to the invoice.</span></span>
11. <span data-ttu-id="e5800-133">Zadejte číslo účtu a opusťte toto pole.</span><span class="sxs-lookup"><span data-stu-id="e5800-133">Enter an account number and tab off of the field.</span></span> <span data-ttu-id="e5800-134">Například zadejte „600120“.</span><span class="sxs-lookup"><span data-stu-id="e5800-134">For example, enter 600120.</span></span>
12. <span data-ttu-id="e5800-135">Klikněte na položku Zaúčtovat.</span><span class="sxs-lookup"><span data-stu-id="e5800-135">Click Post.</span></span>
13. <span data-ttu-id="e5800-136">Kliknutím na tlačítko Doklad zobrazte položky, které byly zaúčtovány.</span><span class="sxs-lookup"><span data-stu-id="e5800-136">Click Voucher to view the entries that were posted.</span></span>
    * <span data-ttu-id="e5800-137">Účet Faktury čekající na schválení bude stornován a nahrazen údaji skutečného účtu výdajů.</span><span class="sxs-lookup"><span data-stu-id="e5800-137">The Invoice Pending Approval account is reversed and replaced with the actual expense account.</span></span>  


