---
title: Vyrovnání postdatovaného šeku pro dodavatele
description: Vyrovnejte postdatovaný šek vydaný dodavateli, když banka provedla transakci šeku poté, co byl šek v prodlení a vyřízen bankou.
author: kweekley
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendPostDatedChecks, LedgerJournalTable, LedgerJournalTransDaily, LedgerTransVoucher
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 89acad0c9421960ff4d07ed8eec798b9068424d5
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5834564"
---
# <a name="settle-a-postdated-check-for-a-vendor"></a><span data-ttu-id="d66f4-103">Vyrovnání postdatovaného šeku pro dodavatele</span><span class="sxs-lookup"><span data-stu-id="d66f4-103">Settle a postdated check for a vendor</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d66f4-104">Vyrovnejte postdatovaný šek vydaný dodavateli, když banka provedla transakci šeku poté, co byl šek v prodlení a vyřízen bankou.</span><span class="sxs-lookup"><span data-stu-id="d66f4-104">Settle a postdated check issued to a vendor when the bank has cleared the check transaction after the check has been overdue and cleared by the bank.</span></span> 

<span data-ttu-id="d66f4-105">Před zahájením tohoto procesu proveďte následující postupy.</span><span class="sxs-lookup"><span data-stu-id="d66f4-105">Complete the following procedures before you start this one.</span></span>

1) <span data-ttu-id="d66f4-106">Nastavení postdatovaných šeků</span><span class="sxs-lookup"><span data-stu-id="d66f4-106">Set up postdated checks</span></span>

2) <span data-ttu-id="d66f4-107">Registrace a zaúčtování postdatovaného šeku pro dodavatele</span><span class="sxs-lookup"><span data-stu-id="d66f4-107">Register and post a postdated check for a vendor</span></span>



<span data-ttu-id="d66f4-108">Role tohoto postupu je Pokladník.</span><span class="sxs-lookup"><span data-stu-id="d66f4-108">The role of this procedure is Treasurer.</span></span> <span data-ttu-id="d66f4-109">Tato procedura používá ukázkovou společnost USMF.</span><span class="sxs-lookup"><span data-stu-id="d66f4-109">This procedure uses the USMF demo company.</span></span>

1. <span data-ttu-id="d66f4-110">Přejděte na Závazky > Platby > Postdatované šeky dodavatele.</span><span class="sxs-lookup"><span data-stu-id="d66f4-110">Go to Accounts payable > Payments > Vendor postdated checks.</span></span>
2. <span data-ttu-id="d66f4-111">Klikněte na možnost Vyrovnat.</span><span class="sxs-lookup"><span data-stu-id="d66f4-111">Click Settle.</span></span>
3. <span data-ttu-id="d66f4-112">Klikněte na možnost Vyrovnat položky clearingu.</span><span class="sxs-lookup"><span data-stu-id="d66f4-112">Click Settle clearing entries.</span></span>
    * <span data-ttu-id="d66f4-113">Vyrovnejte účet dodavatele pro transakci šeku.</span><span class="sxs-lookup"><span data-stu-id="d66f4-113">Settle the vendor account for the check transaction.</span></span>  
4. <span data-ttu-id="d66f4-114">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="d66f4-114">Close the page.</span></span>
5. <span data-ttu-id="d66f4-115">Přejděte do nabídky Hlavní kniha > Položky deníku > Hlavní deníky.</span><span class="sxs-lookup"><span data-stu-id="d66f4-115">Go to General ledger > Journal entries > General journals.</span></span>
6. <span data-ttu-id="d66f4-116">V poli Zobrazit vyberte možnost „Vše“.</span><span class="sxs-lookup"><span data-stu-id="d66f4-116">In the Show field, select 'All'.</span></span>
7. <span data-ttu-id="d66f4-117">Zaškrtněte políčko Zobrazit pouze uživatelem vytvořené položky nebo jeho zaškrtnutí zrušte.</span><span class="sxs-lookup"><span data-stu-id="d66f4-117">Select or clear the Show user-created only check box.</span></span>
8. <span data-ttu-id="d66f4-118">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="d66f4-118">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="d66f4-119">Klikněte na možnost Řádky.</span><span class="sxs-lookup"><span data-stu-id="d66f4-119">Click Lines.</span></span>
10. <span data-ttu-id="d66f4-120">Klikněte na možnost Doklad.</span><span class="sxs-lookup"><span data-stu-id="d66f4-120">Click Voucher.</span></span>
11. <span data-ttu-id="d66f4-121">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="d66f4-121">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]