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
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8220bacc8d683163e97956ec59a5af929b04319c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994408"
---
# <a name="settle-transactions-between-ledger-accounts"></a><span data-ttu-id="9196a-103">Vyrovnání transakcí mezi účty hlavní knihy</span><span class="sxs-lookup"><span data-stu-id="9196a-103">Settle transactions between ledger accounts</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9196a-104">Tato procedura ukazuje, jak vyrovnat transakce mezi účty hlavní knihy a jak zrušit vyrovnání hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="9196a-104">This procedure shows how to settle transactions between ledger accounts and cancel a ledger settlement.</span></span> <span data-ttu-id="9196a-105">Tato procedura používá data ukázkové společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="9196a-105">This procedure uses the USMF demo data company.</span></span>


## <a name="settle-transaction-between-ledger-accounts"></a><span data-ttu-id="9196a-106">Vyrovnání transakce mezi účty hlavní knihy</span><span class="sxs-lookup"><span data-stu-id="9196a-106">Settle transaction between ledger accounts</span></span>
1. <span data-ttu-id="9196a-107">Přejděte do hlavní knihy > Periodické úkoly > Vyrovnání hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="9196a-107">Go to General ledger > Periodic tasks > Ledger settlements.</span></span>
2. <span data-ttu-id="9196a-108">V seznamu vyhledejte transakce, které chcete vyrovnat.</span><span class="sxs-lookup"><span data-stu-id="9196a-108">In the list, find the transaction that you want to settle.</span></span>
   > [!NOTE]
   > <span data-ttu-id="9196a-109">Zůstatek na účtu musí být nula.</span><span class="sxs-lookup"><span data-stu-id="9196a-109">The amount balance must be zero.</span></span>  
3. <span data-ttu-id="9196a-110">Klepněte na Zahrnout.</span><span class="sxs-lookup"><span data-stu-id="9196a-110">Click Include.</span></span>
4. <span data-ttu-id="9196a-111">Klepněte na možnost Akceptovat.</span><span class="sxs-lookup"><span data-stu-id="9196a-111">Click Accept.</span></span>

## <a name="cancel-a-ledger-settlement"></a><span data-ttu-id="9196a-112">Zrušení vyrovnání hlavní knihy</span><span class="sxs-lookup"><span data-stu-id="9196a-112">Cancel a ledger settlement</span></span>

1. <span data-ttu-id="9196a-113">Přejděte do části Hlavní kniha > Dotazy a sestavy > Předvaha.</span><span class="sxs-lookup"><span data-stu-id="9196a-113">Go to General ledger > Inquiries and reports > Trial balance.</span></span>
2. <span data-ttu-id="9196a-114">Klepnutím na možnost Parametry otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="9196a-114">Click Parameters to open the drop dialog.</span></span>
3. <span data-ttu-id="9196a-115">Klepněte na položku Aktualizovat.</span><span class="sxs-lookup"><span data-stu-id="9196a-115">Click Update.</span></span>
4. <span data-ttu-id="9196a-116">V seznamu vyhledejte účet, který má vyrovnanou transakci.</span><span class="sxs-lookup"><span data-stu-id="9196a-116">In the list, find the account that has the settled transaction.</span></span>
5. <span data-ttu-id="9196a-117">Klepněte na Všechny transakce.</span><span class="sxs-lookup"><span data-stu-id="9196a-117">Click All transactions.</span></span>
6. <span data-ttu-id="9196a-118">Filtr lze použít ke snadnému vyhledání transakce v seznamu.</span><span class="sxs-lookup"><span data-stu-id="9196a-118">Use a filter to easily find the transaction in the list.</span></span>
7. <span data-ttu-id="9196a-119">Klepněte na Vyrovnání hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="9196a-119">Click Ledger settlements.</span></span>
8. <span data-ttu-id="9196a-120">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="9196a-120">In the list, mark the selected row.</span></span>

