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
ms.openlocfilehash: 6813871a4773d39d4abfdecc896a2aa8b320cbe0
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5222088"
---
# <a name="settle-transactions-between-ledger-accounts"></a><span data-ttu-id="f4a68-103">Vyrovnání transakcí mezi účty hlavní knihy</span><span class="sxs-lookup"><span data-stu-id="f4a68-103">Settle transactions between ledger accounts</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f4a68-104">Tato procedura ukazuje, jak vyrovnat transakce mezi účty hlavní knihy a jak zrušit vyrovnání hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="f4a68-104">This procedure shows how to settle transactions between ledger accounts and cancel a ledger settlement.</span></span> <span data-ttu-id="f4a68-105">Tato procedura používá data ukázkové společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="f4a68-105">This procedure uses the USMF demo data company.</span></span>


## <a name="settle-transaction-between-ledger-accounts"></a><span data-ttu-id="f4a68-106">Vyrovnání transakce mezi účty hlavní knihy</span><span class="sxs-lookup"><span data-stu-id="f4a68-106">Settle transaction between ledger accounts</span></span>
1. <span data-ttu-id="f4a68-107">Přejděte do hlavní knihy > Periodické úkoly > Vyrovnání hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="f4a68-107">Go to General ledger > Periodic tasks > Ledger settlements.</span></span>
2. <span data-ttu-id="f4a68-108">V seznamu vyhledejte transakce, které chcete vyrovnat.</span><span class="sxs-lookup"><span data-stu-id="f4a68-108">In the list, find the transaction that you want to settle.</span></span>
   > [!NOTE]
   > <span data-ttu-id="f4a68-109">Zůstatek na účtu musí být nula.</span><span class="sxs-lookup"><span data-stu-id="f4a68-109">The amount balance must be zero.</span></span>  
3. <span data-ttu-id="f4a68-110">Klepněte na Zahrnout.</span><span class="sxs-lookup"><span data-stu-id="f4a68-110">Click Include.</span></span>
4. <span data-ttu-id="f4a68-111">Klepněte na možnost Akceptovat.</span><span class="sxs-lookup"><span data-stu-id="f4a68-111">Click Accept.</span></span>

## <a name="cancel-a-ledger-settlement"></a><span data-ttu-id="f4a68-112">Zrušení vyrovnání hlavní knihy</span><span class="sxs-lookup"><span data-stu-id="f4a68-112">Cancel a ledger settlement</span></span>

1. <span data-ttu-id="f4a68-113">Přejděte do části Hlavní kniha > Dotazy a sestavy > Předvaha.</span><span class="sxs-lookup"><span data-stu-id="f4a68-113">Go to General ledger > Inquiries and reports > Trial balance.</span></span>
2. <span data-ttu-id="f4a68-114">Klepnutím na možnost Parametry otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="f4a68-114">Click Parameters to open the drop dialog.</span></span>
3. <span data-ttu-id="f4a68-115">Klepněte na položku Aktualizovat.</span><span class="sxs-lookup"><span data-stu-id="f4a68-115">Click Update.</span></span>
4. <span data-ttu-id="f4a68-116">V seznamu vyhledejte účet, který má vyrovnanou transakci.</span><span class="sxs-lookup"><span data-stu-id="f4a68-116">In the list, find the account that has the settled transaction.</span></span>
5. <span data-ttu-id="f4a68-117">Klepněte na Všechny transakce.</span><span class="sxs-lookup"><span data-stu-id="f4a68-117">Click All transactions.</span></span>
6. <span data-ttu-id="f4a68-118">Filtr lze použít ke snadnému vyhledání transakce v seznamu.</span><span class="sxs-lookup"><span data-stu-id="f4a68-118">Use a filter to easily find the transaction in the list.</span></span>
7. <span data-ttu-id="f4a68-119">Klepněte na Vyrovnání hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="f4a68-119">Click Ledger settlements.</span></span>
8. <span data-ttu-id="f4a68-120">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="f4a68-120">In the list, mark the selected row.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]