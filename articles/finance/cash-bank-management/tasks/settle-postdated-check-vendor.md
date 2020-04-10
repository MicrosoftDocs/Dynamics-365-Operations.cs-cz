---
title: Vyrovnání postdatovaného šeku pro dodavatele
description: Vyrovnejte postdatovaný šek vydaný dodavateli, když banka provedla transakci šeku poté, co byl šek v prodlení a vyřízen bankou.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPostDatedChecks, LedgerJournalTable, LedgerJournalTransDaily, LedgerTransVoucher
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ee66bdb93d1252486efc7be25adeb6ee7cc6ce05
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/18/2020
ms.locfileid: "3144227"
---
# <a name="settle-a-postdated-check-for-a-vendor"></a><span data-ttu-id="8fb3d-103">Vyrovnání postdatovaného šeku pro dodavatele</span><span class="sxs-lookup"><span data-stu-id="8fb3d-103">Settle a postdated check for a vendor</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8fb3d-104">Vyrovnejte postdatovaný šek vydaný dodavateli, když banka provedla transakci šeku poté, co byl šek v prodlení a vyřízen bankou.</span><span class="sxs-lookup"><span data-stu-id="8fb3d-104">Settle a postdated check issued to a vendor when the bank has cleared the check transaction after the check has been overdue and cleared by the bank.</span></span> 

<span data-ttu-id="8fb3d-105">Před zahájením tohoto procesu proveďte následující postupy.</span><span class="sxs-lookup"><span data-stu-id="8fb3d-105">Complete the following procedures before you start this one.</span></span>

1) <span data-ttu-id="8fb3d-106">Nastavení postdatovaných šeků</span><span class="sxs-lookup"><span data-stu-id="8fb3d-106">Set up postdated checks</span></span>

2) <span data-ttu-id="8fb3d-107">Registrace a zaúčtování postdatovaného šeku pro dodavatele</span><span class="sxs-lookup"><span data-stu-id="8fb3d-107">Register and post a postdated check for a vendor</span></span>



<span data-ttu-id="8fb3d-108">Role tohoto postupu je Pokladník.</span><span class="sxs-lookup"><span data-stu-id="8fb3d-108">The role of this procedure is Treasurer.</span></span> <span data-ttu-id="8fb3d-109">Tato procedura používá ukázkovou společnost USMF.</span><span class="sxs-lookup"><span data-stu-id="8fb3d-109">This procedure uses the USMF demo company.</span></span>

1. <span data-ttu-id="8fb3d-110">Přejděte na Závazky > Platby > Postdatované šeky dodavatele.</span><span class="sxs-lookup"><span data-stu-id="8fb3d-110">Go to Accounts payable > Payments > Vendor postdated checks.</span></span>
2. <span data-ttu-id="8fb3d-111">Klikněte na možnost Vyrovnat.</span><span class="sxs-lookup"><span data-stu-id="8fb3d-111">Click Settle.</span></span>
3. <span data-ttu-id="8fb3d-112">Klikněte na možnost Vyrovnat položky clearingu.</span><span class="sxs-lookup"><span data-stu-id="8fb3d-112">Click Settle clearing entries.</span></span>
    * <span data-ttu-id="8fb3d-113">Vyrovnejte účet dodavatele pro transakci šeku.</span><span class="sxs-lookup"><span data-stu-id="8fb3d-113">Settle the vendor account for the check transaction.</span></span>  
4. <span data-ttu-id="8fb3d-114">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="8fb3d-114">Close the page.</span></span>
5. <span data-ttu-id="8fb3d-115">Přejděte do nabídky Hlavní kniha > Položky deníku > Hlavní deníky.</span><span class="sxs-lookup"><span data-stu-id="8fb3d-115">Go to General ledger > Journal entries > General journals.</span></span>
6. <span data-ttu-id="8fb3d-116">V poli Zobrazit vyberte možnost „Vše“.</span><span class="sxs-lookup"><span data-stu-id="8fb3d-116">In the Show field, select 'All'.</span></span>
7. <span data-ttu-id="8fb3d-117">Zaškrtněte políčko Zobrazit pouze uživatelem vytvořené položky nebo jeho zaškrtnutí zrušte.</span><span class="sxs-lookup"><span data-stu-id="8fb3d-117">Select or clear the Show user-created only check box.</span></span>
8. <span data-ttu-id="8fb3d-118">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="8fb3d-118">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="8fb3d-119">Klikněte na možnost Řádky.</span><span class="sxs-lookup"><span data-stu-id="8fb3d-119">Click Lines.</span></span>
10. <span data-ttu-id="8fb3d-120">Klikněte na možnost Doklad.</span><span class="sxs-lookup"><span data-stu-id="8fb3d-120">Click Voucher.</span></span>
11. <span data-ttu-id="8fb3d-121">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="8fb3d-121">Close the page.</span></span>

