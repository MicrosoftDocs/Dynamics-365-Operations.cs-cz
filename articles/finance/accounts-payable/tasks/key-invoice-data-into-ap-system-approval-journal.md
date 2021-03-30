---
title: Zadání dat faktury do závazků s použitím deníku schválení
description: Tohle téma popisuje použití registru faktur k vytvoření faktur a použití deníku schválení pro aktualizaci účtů výdajů.
author: abruer
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransInvoiceRegister, HcmWorkerLookUp, LedgerJournalTransApprove, LedgerJournalTransApproveFetchVouchers, LedgerTransVoucher
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f0fee32d9fd1ab89b1a8cedb2e1965674586d4e7
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5227177"
---
# <a name="key-invoice-data-into-accounts-payable-using-an-approval-journal"></a><span data-ttu-id="8e698-103">Zadání dat faktury do závazků s použitím deníku schválení</span><span class="sxs-lookup"><span data-stu-id="8e698-103">Key invoice data into accounts payable using an approval journal</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8e698-104">Tohle téma popisuje použití registru faktur k vytvoření faktur a použití deníku schválení pro aktualizaci účtů výdajů.</span><span class="sxs-lookup"><span data-stu-id="8e698-104">This topic explains how to use the invoice register to create invoices and then use the approval journal to update the expense accounts.</span></span>

## <a name="create-and-post-and-invoice"></a><span data-ttu-id="8e698-105">Vytvoření a zaúčtování faktury</span><span class="sxs-lookup"><span data-stu-id="8e698-105">Create and post and invoice</span></span>
1. <span data-ttu-id="8e698-106">V navigačním podokně přejděte na **Moduly > Závazky > Faktury > Registr faktur**.</span><span class="sxs-lookup"><span data-stu-id="8e698-106">In the navigation pan, go to **Modules > Accounts payable > Invoices > Invoice register**.</span></span>
2. <span data-ttu-id="8e698-107">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="8e698-107">Select **New**.</span></span>
3. <span data-ttu-id="8e698-108">Vyberte název registru faktury, který chcete použít.</span><span class="sxs-lookup"><span data-stu-id="8e698-108">Select the name of the invoice register that you want to use.</span></span>
4. <span data-ttu-id="8e698-109">Kliknutím na **Řádky** otevřete registr a zadejte řádky výdajů.</span><span class="sxs-lookup"><span data-stu-id="8e698-109">Select **Lines** to open the register and enter expense lines.</span></span>
5. <span data-ttu-id="8e698-110">Vyberte dodavatele.</span><span class="sxs-lookup"><span data-stu-id="8e698-110">Select a vendor.</span></span> <span data-ttu-id="8e698-111">Například zadejte nebo vyberte možnost `US-104`.</span><span class="sxs-lookup"><span data-stu-id="8e698-111">For example, enter or select `US-104`.</span></span>
6. <span data-ttu-id="8e698-112">Zadejte hodnotu do pole **Faktura**.</span><span class="sxs-lookup"><span data-stu-id="8e698-112">In the **Invoice** field, type a value.</span></span>
7. <span data-ttu-id="8e698-113">Zadejte hodnotu do pole **Popis**.</span><span class="sxs-lookup"><span data-stu-id="8e698-113">In the **Description** field, type a value.</span></span>
8. <span data-ttu-id="8e698-114">V poli **Dobropis** zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="8e698-114">In the **Credit** field, enter a number.</span></span>
9. <span data-ttu-id="8e698-115">V poli **Schválil/a** vyberte z rozevírací nabídky schvalovatele.</span><span class="sxs-lookup"><span data-stu-id="8e698-115">In the **Approved by** field, select an approver from the drop-down menu.</span></span>
10. <span data-ttu-id="8e698-116">Zvolte **Zaúčtovat**.</span><span class="sxs-lookup"><span data-stu-id="8e698-116">Select **Post**.</span></span>

## <a name="approve-an-invoice"></a><span data-ttu-id="8e698-117">Schválení faktury</span><span class="sxs-lookup"><span data-stu-id="8e698-117">Approve an invoice</span></span>
1. <span data-ttu-id="8e698-118">V navigačním podokně přejděte na **Moduly > Závazky > Faktury > Schvalovatel faktury**.</span><span class="sxs-lookup"><span data-stu-id="8e698-118">In the navigation pane, go to **Modules > Accounts payable > Invoices > Invoice approval**.</span></span>
2. <span data-ttu-id="8e698-119">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="8e698-119">Select **New**.</span></span>
3. <span data-ttu-id="8e698-120">Vyberte název deníku schválení faktur, který chcete použít.</span><span class="sxs-lookup"><span data-stu-id="8e698-120">Select the name of the invoice approval journal that you want to use.</span></span>
4. <span data-ttu-id="8e698-121">Výběrem položky **Řádky** zobrazte stránku, kde bude možné vybrat faktury, které chcete schválit.</span><span class="sxs-lookup"><span data-stu-id="8e698-121">Select **Lines** to display a page where you will be able to select the invoices that you want to approve.</span></span>
5. <span data-ttu-id="8e698-122">Výběrem možnosti **Hledat doklady** zobrazte všechny faktury, které jsou již připraveny ke schválení.</span><span class="sxs-lookup"><span data-stu-id="8e698-122">Select **Find Vouchers** to display all of the invoices that are ready for approval.</span></span>
6. <span data-ttu-id="8e698-123">Označte fakturu, kterou jste vytvořili, a poté kliknětena tlačítko **Vybrat**.</span><span class="sxs-lookup"><span data-stu-id="8e698-123">Mark the invoice that you created, then click **Select**.</span></span> <span data-ttu-id="8e698-124">Doklady vybrané výše, se po výběru přesunou do tohoto seznamu.</span><span class="sxs-lookup"><span data-stu-id="8e698-124">The vouchers that you selected above are moved to this list after you select them.</span></span>  
7. <span data-ttu-id="8e698-125">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="8e698-125">Select **OK**.</span></span>
8. <span data-ttu-id="8e698-126">Vyberte pole s **číslem účtu** přidejte výdajový účet k faktuře.</span><span class="sxs-lookup"><span data-stu-id="8e698-126">Select the **account number** field to add an expense account to the invoice.</span></span>
9. <span data-ttu-id="8e698-127">Zadejte číslo účtu a opusťte toto pole.</span><span class="sxs-lookup"><span data-stu-id="8e698-127">Enter an account number and tab off of the field.</span></span> <span data-ttu-id="8e698-128">Zadejte například `600120`.</span><span class="sxs-lookup"><span data-stu-id="8e698-128">For example, enter `600120`.</span></span>
10. <span data-ttu-id="8e698-129">Zvolte **Zaúčtovat**.</span><span class="sxs-lookup"><span data-stu-id="8e698-129">Select **Post**.</span></span>
11. <span data-ttu-id="8e698-130">Výběrem možnosti **Doklad** zobrazte položky, které byly zaúčtovány.</span><span class="sxs-lookup"><span data-stu-id="8e698-130">Select **Voucher** to view the entries that were posted.</span></span> <span data-ttu-id="8e698-131">Účet Faktury čekající na schválení bude stornován a nahrazen údaji skutečného účtu výdajů.</span><span class="sxs-lookup"><span data-stu-id="8e698-131">The Invoice Pending Approval account is reversed and replaced with the actual expense account.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]