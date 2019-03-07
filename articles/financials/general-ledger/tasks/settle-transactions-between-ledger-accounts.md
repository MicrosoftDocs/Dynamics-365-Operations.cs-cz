---
title: Vyrovnání transakcí mezi účty hlavní knihy
description: Tato procedura ukazuje, jak vyrovnat transakce mezi účty hlavní knihy a jak zrušit vyrovnání hlavní knihy.
author: aprilolson
manager: AnnBe
ms.date: 10/03/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerTransSettlement, LedgerTrialBalanceListPage, LedgerTrialBalanceListPageBalanceParms, LedgerTransAccount, LedgerTransSettled
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4aff64fa1c017f295752e913de7fb320f0662ef8
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "325818"
---
# <a name="settle-transactions-between-ledger-accounts"></a><span data-ttu-id="6b652-103">Vyrovnání transakcí mezi účty hlavní knihy</span><span class="sxs-lookup"><span data-stu-id="6b652-103">Settle transactions between ledger accounts</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6b652-104">Tato procedura ukazuje, jak vyrovnat transakce mezi účty hlavní knihy a jak zrušit vyrovnání hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="6b652-104">This procedure shows how to settle transactions between ledger accounts and cancel a ledger settlement.</span></span> <span data-ttu-id="6b652-105">Tato procedura používá data ukázkové společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="6b652-105">This procedure uses the USMF demo data company.</span></span>


## <a name="settle-transaction-between-ledger-accounts"></a><span data-ttu-id="6b652-106">Vyrovnání transakce mezi účty hlavní knihy</span><span class="sxs-lookup"><span data-stu-id="6b652-106">Settle transaction between ledger accounts</span></span>
1. <span data-ttu-id="6b652-107">Přejděte do hlavní knihy > Periodické úkoly > Vyrovnání hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="6b652-107">Go to General ledger > Periodic tasks > Ledger settlements.</span></span>
2. <span data-ttu-id="6b652-108">V seznamu vyhledejte transakce, které chcete vyrovnat.</span><span class="sxs-lookup"><span data-stu-id="6b652-108">In the list, find the transaction that you want to settle.</span></span>
   > [!NOTE]
   > <span data-ttu-id="6b652-109">Zůstatek na účtu musí být nula.</span><span class="sxs-lookup"><span data-stu-id="6b652-109">The amount balance must be zero.</span></span>  
3. <span data-ttu-id="6b652-110">Klepněte na Zahrnout.</span><span class="sxs-lookup"><span data-stu-id="6b652-110">Click Include.</span></span>
4. <span data-ttu-id="6b652-111">Klepněte na možnost Akceptovat.</span><span class="sxs-lookup"><span data-stu-id="6b652-111">Click Accept.</span></span>

## <a name="cancel-a-ledger-settlement"></a><span data-ttu-id="6b652-112">Zrušení vyrovnání hlavní knihy</span><span class="sxs-lookup"><span data-stu-id="6b652-112">Cancel a ledger settlement</span></span>

1. <span data-ttu-id="6b652-113">Přejděte do části Hlavní kniha > Dotazy a sestavy > Předvaha.</span><span class="sxs-lookup"><span data-stu-id="6b652-113">Go to General ledger > Inquiries and reports > Trial balance.</span></span>
2. <span data-ttu-id="6b652-114">Klepnutím na možnost Parametry otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="6b652-114">Click Parameters to open the drop dialog.</span></span>
3. <span data-ttu-id="6b652-115">Klepněte na položku Aktualizovat.</span><span class="sxs-lookup"><span data-stu-id="6b652-115">Click Update.</span></span>
4. <span data-ttu-id="6b652-116">V seznamu vyhledejte účet, který má vyrovnanou transakci.</span><span class="sxs-lookup"><span data-stu-id="6b652-116">In the list, find the account that has the settled transaction.</span></span>
5. <span data-ttu-id="6b652-117">Klepněte na Všechny transakce.</span><span class="sxs-lookup"><span data-stu-id="6b652-117">Click All transactions.</span></span>
6. <span data-ttu-id="6b652-118">Filtr lze použít ke snadnému vyhledání transakce v seznamu.</span><span class="sxs-lookup"><span data-stu-id="6b652-118">Use a filter to easily find the transaction in the list.</span></span>
7. <span data-ttu-id="6b652-119">Klepněte na Vyrovnání hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="6b652-119">Click Ledger settlements.</span></span>
8. <span data-ttu-id="6b652-120">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="6b652-120">In the list, mark the selected row.</span></span>

