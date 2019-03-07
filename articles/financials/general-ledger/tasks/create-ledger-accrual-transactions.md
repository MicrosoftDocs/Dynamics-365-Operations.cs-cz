---
title: Vytvoření transakcí časového rozlišení hlavní knihy
description: Tento průvodce úkoly vás provede generováním časově rozlišených transakcí hlavní knihy, které vycházejí z údajů schémat časového rozlišení.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransDaily, LedgerJournalTransAccrual, LedgerJournalTransAccrualTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4a65bec066bdcb01ce8acf8cfbf2d31611104921
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "330464"
---
# <a name="create-ledger-accrual-transactions"></a><span data-ttu-id="e2b08-103">Vytvoření transakcí časového rozlišení hlavní knihy</span><span class="sxs-lookup"><span data-stu-id="e2b08-103">Create ledger accrual transactions</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e2b08-104">Tento průvodce úkoly vás provede generováním časově rozlišených transakcí hlavní knihy, které vycházejí z údajů schémat časového rozlišení.</span><span class="sxs-lookup"><span data-stu-id="e2b08-104">This task guide steps through generating ledger accrual transactions that are based on accrual schemes</span></span>

1. <span data-ttu-id="e2b08-105">Přejděte do nabídky Hlavní kniha > Položky deníku > Hlavní deníky.</span><span class="sxs-lookup"><span data-stu-id="e2b08-105">Go to General ledger > Journal entries > General journals.</span></span>
2. <span data-ttu-id="e2b08-106">V rozevíracím seznamu vyhledejte a vyberte požadovaný deník nebo vytvořte nový.</span><span class="sxs-lookup"><span data-stu-id="e2b08-106">In the list, find and select the desired journal or create a new one.</span></span>
3. <span data-ttu-id="e2b08-107">Klepnutím přejdete na odkaz v poli Číslo dávky deníku.</span><span class="sxs-lookup"><span data-stu-id="e2b08-107">Click to follow the link in the Journal batch number field.</span></span>
4. <span data-ttu-id="e2b08-108">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="e2b08-108">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="e2b08-109">Zadejte požadované hodnoty do pole Účet.</span><span class="sxs-lookup"><span data-stu-id="e2b08-109">In the Account field, specify the desired values.</span></span>
    * <span data-ttu-id="e2b08-110">V tomto příkladu definujeme výdaje pro pojištění.</span><span class="sxs-lookup"><span data-stu-id="e2b08-110">In this example, we are defining the expense for the insurance.</span></span> <span data-ttu-id="e2b08-111">Bude přicházet částka periodických výdajů.</span><span class="sxs-lookup"><span data-stu-id="e2b08-111">It will be come periodic expense amount.</span></span>  
6. <span data-ttu-id="e2b08-112">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="e2b08-112">In the Description field, type a value.</span></span>
7. <span data-ttu-id="e2b08-113">Do pole Má dáti zadejte čísl.</span><span class="sxs-lookup"><span data-stu-id="e2b08-113">In the Debit field, enter a number.</span></span>
8. <span data-ttu-id="e2b08-114">Zadejte požadované hodnoty do pole Protiúčet.</span><span class="sxs-lookup"><span data-stu-id="e2b08-114">In the Offset account field, specify the desired values.</span></span>
9. <span data-ttu-id="e2b08-115">Klepněte na možnost Funkce.</span><span class="sxs-lookup"><span data-stu-id="e2b08-115">Click Functions.</span></span>
10. <span data-ttu-id="e2b08-116">Klepněte na Časové rozlišení hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="e2b08-116">Click Ledger accruals.</span></span>
11. <span data-ttu-id="e2b08-117">V poli Identifikace časového rozlišení klepnutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="e2b08-117">In the Accrual identification field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="e2b08-118">V seznamu najděte a vyberte schéma časového rozlišení, které chcete použít.</span><span class="sxs-lookup"><span data-stu-id="e2b08-118">In the list, find and select the accural scheme you want to apply.</span></span>
13. <span data-ttu-id="e2b08-119">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="e2b08-119">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="e2b08-120">Zadejte datum do pole Počáteční datum.</span><span class="sxs-lookup"><span data-stu-id="e2b08-120">In the Start date field, enter a date.</span></span>
15. <span data-ttu-id="e2b08-121">Klikněte na Transakce.</span><span class="sxs-lookup"><span data-stu-id="e2b08-121">Click Transactions.</span></span>
16. <span data-ttu-id="e2b08-122">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="e2b08-122">Close the page.</span></span>
17. <span data-ttu-id="e2b08-123">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="e2b08-123">Click OK.</span></span>
18. <span data-ttu-id="e2b08-124">Klikněte na položku Zaúčtovat.</span><span class="sxs-lookup"><span data-stu-id="e2b08-124">Click Post.</span></span>

