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
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1562477"
---
# <a name="create-ledger-accrual-transactions"></a><span data-ttu-id="8e3f2-103">Vytvoření transakcí časového rozlišení hlavní knihy</span><span class="sxs-lookup"><span data-stu-id="8e3f2-103">Create ledger accrual transactions</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8e3f2-104">Tento průvodce úkoly vás provede generováním časově rozlišených transakcí hlavní knihy, které vycházejí z údajů schémat časového rozlišení.</span><span class="sxs-lookup"><span data-stu-id="8e3f2-104">This task guide steps through generating ledger accrual transactions that are based on accrual schemes</span></span>

1. <span data-ttu-id="8e3f2-105">Přejděte do nabídky Hlavní kniha > Položky deníku > Hlavní deníky.</span><span class="sxs-lookup"><span data-stu-id="8e3f2-105">Go to General ledger > Journal entries > General journals.</span></span>
2. <span data-ttu-id="8e3f2-106">V rozevíracím seznamu vyhledejte a vyberte požadovaný deník nebo vytvořte nový.</span><span class="sxs-lookup"><span data-stu-id="8e3f2-106">In the list, find and select the desired journal or create a new one.</span></span>
3. <span data-ttu-id="8e3f2-107">Klepnutím přejdete na odkaz v poli Číslo dávky deníku.</span><span class="sxs-lookup"><span data-stu-id="8e3f2-107">Click to follow the link in the Journal batch number field.</span></span>
4. <span data-ttu-id="8e3f2-108">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="8e3f2-108">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="8e3f2-109">Zadejte požadované hodnoty do pole Účet.</span><span class="sxs-lookup"><span data-stu-id="8e3f2-109">In the Account field, specify the desired values.</span></span>
    * <span data-ttu-id="8e3f2-110">V tomto příkladu definujeme výdaje pro pojištění.</span><span class="sxs-lookup"><span data-stu-id="8e3f2-110">In this example, we are defining the expense for the insurance.</span></span> <span data-ttu-id="8e3f2-111">Bude přicházet částka periodických výdajů.</span><span class="sxs-lookup"><span data-stu-id="8e3f2-111">It will be come periodic expense amount.</span></span>  
6. <span data-ttu-id="8e3f2-112">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="8e3f2-112">In the Description field, type a value.</span></span>
7. <span data-ttu-id="8e3f2-113">Do pole Má dáti zadejte čísl.</span><span class="sxs-lookup"><span data-stu-id="8e3f2-113">In the Debit field, enter a number.</span></span>
8. <span data-ttu-id="8e3f2-114">Zadejte požadované hodnoty do pole Protiúčet.</span><span class="sxs-lookup"><span data-stu-id="8e3f2-114">In the Offset account field, specify the desired values.</span></span>
9. <span data-ttu-id="8e3f2-115">Klepněte na možnost Funkce.</span><span class="sxs-lookup"><span data-stu-id="8e3f2-115">Click Functions.</span></span>
10. <span data-ttu-id="8e3f2-116">Klepněte na Časové rozlišení hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="8e3f2-116">Click Ledger accruals.</span></span>
11. <span data-ttu-id="8e3f2-117">V poli Identifikace časového rozlišení klepnutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="8e3f2-117">In the Accrual identification field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="8e3f2-118">V seznamu najděte a vyberte schéma časového rozlišení, které chcete použít.</span><span class="sxs-lookup"><span data-stu-id="8e3f2-118">In the list, find and select the accural scheme you want to apply.</span></span>
13. <span data-ttu-id="8e3f2-119">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="8e3f2-119">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="8e3f2-120">Zadejte datum do pole Počáteční datum.</span><span class="sxs-lookup"><span data-stu-id="8e3f2-120">In the Start date field, enter a date.</span></span>
15. <span data-ttu-id="8e3f2-121">Klikněte na Transakce.</span><span class="sxs-lookup"><span data-stu-id="8e3f2-121">Click Transactions.</span></span>
16. <span data-ttu-id="8e3f2-122">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="8e3f2-122">Close the page.</span></span>
17. <span data-ttu-id="8e3f2-123">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="8e3f2-123">Click OK.</span></span>
18. <span data-ttu-id="8e3f2-124">Klikněte na položku Zaúčtovat.</span><span class="sxs-lookup"><span data-stu-id="8e3f2-124">Click Post.</span></span>

