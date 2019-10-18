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
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6ed76f82532d43a3c05b60b12176fe851e327956
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/27/2019
ms.locfileid: "2175325"
---
# <a name="settle-transactions-between-ledger-accounts"></a><span data-ttu-id="7929d-103">Vyrovnání transakcí mezi účty hlavní knihy</span><span class="sxs-lookup"><span data-stu-id="7929d-103">Settle transactions between ledger accounts</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7929d-104">Tato procedura ukazuje, jak vyrovnat transakce mezi účty hlavní knihy a jak zrušit vyrovnání hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="7929d-104">This procedure shows how to settle transactions between ledger accounts and cancel a ledger settlement.</span></span> <span data-ttu-id="7929d-105">Tato procedura používá data ukázkové společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="7929d-105">This procedure uses the USMF demo data company.</span></span>


## <a name="settle-transaction-between-ledger-accounts"></a><span data-ttu-id="7929d-106">Vyrovnání transakce mezi účty hlavní knihy</span><span class="sxs-lookup"><span data-stu-id="7929d-106">Settle transaction between ledger accounts</span></span>
1. <span data-ttu-id="7929d-107">Přejděte do hlavní knihy > Periodické úkoly > Vyrovnání hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="7929d-107">Go to General ledger > Periodic tasks > Ledger settlements.</span></span>
2. <span data-ttu-id="7929d-108">V seznamu vyhledejte transakce, které chcete vyrovnat.</span><span class="sxs-lookup"><span data-stu-id="7929d-108">In the list, find the transaction that you want to settle.</span></span>
   > [!NOTE]
   > <span data-ttu-id="7929d-109">Zůstatek na účtu musí být nula.</span><span class="sxs-lookup"><span data-stu-id="7929d-109">The amount balance must be zero.</span></span>  
3. <span data-ttu-id="7929d-110">Klepněte na Zahrnout.</span><span class="sxs-lookup"><span data-stu-id="7929d-110">Click Include.</span></span>
4. <span data-ttu-id="7929d-111">Klepněte na možnost Akceptovat.</span><span class="sxs-lookup"><span data-stu-id="7929d-111">Click Accept.</span></span>

## <a name="cancel-a-ledger-settlement"></a><span data-ttu-id="7929d-112">Zrušení vyrovnání hlavní knihy</span><span class="sxs-lookup"><span data-stu-id="7929d-112">Cancel a ledger settlement</span></span>

1. <span data-ttu-id="7929d-113">Přejděte do části Hlavní kniha > Dotazy a sestavy > Předvaha.</span><span class="sxs-lookup"><span data-stu-id="7929d-113">Go to General ledger > Inquiries and reports > Trial balance.</span></span>
2. <span data-ttu-id="7929d-114">Klepnutím na možnost Parametry otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="7929d-114">Click Parameters to open the drop dialog.</span></span>
3. <span data-ttu-id="7929d-115">Klepněte na položku Aktualizovat.</span><span class="sxs-lookup"><span data-stu-id="7929d-115">Click Update.</span></span>
4. <span data-ttu-id="7929d-116">V seznamu vyhledejte účet, který má vyrovnanou transakci.</span><span class="sxs-lookup"><span data-stu-id="7929d-116">In the list, find the account that has the settled transaction.</span></span>
5. <span data-ttu-id="7929d-117">Klepněte na Všechny transakce.</span><span class="sxs-lookup"><span data-stu-id="7929d-117">Click All transactions.</span></span>
6. <span data-ttu-id="7929d-118">Filtr lze použít ke snadnému vyhledání transakce v seznamu.</span><span class="sxs-lookup"><span data-stu-id="7929d-118">Use a filter to easily find the transaction in the list.</span></span>
7. <span data-ttu-id="7929d-119">Klepněte na Vyrovnání hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="7929d-119">Click Ledger settlements.</span></span>
8. <span data-ttu-id="7929d-120">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="7929d-120">In the list, mark the selected row.</span></span>

