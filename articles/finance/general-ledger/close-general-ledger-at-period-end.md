---
title: Uzavření hlavní knihy ke konci období
description: Toto téma popisuje úlohy, které jsou obvykle dokončeny při provádění uzávěrky období pro hlavní knihu.
author: aprilolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerPeriodCloseWorkspace
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14111
ms.assetid: cec9e039-c1a2-482c-bea6-e11d896eea9d
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5cabdce5e23704fbf12e631a138235174ebc5772
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441152"
---
# <a name="close-the-general-ledger-at-period-end"></a><span data-ttu-id="f8d7e-103">Uzavření hlavní knihy ke konci období</span><span class="sxs-lookup"><span data-stu-id="f8d7e-103">Close the general ledger at period end</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f8d7e-104">Toto téma popisuje úlohy, které jsou obvykle dokončeny při provádění uzávěrky období pro hlavní knihu.</span><span class="sxs-lookup"><span data-stu-id="f8d7e-104">This topic describes the tasks that are typically completed when performing a period closing for General ledger.</span></span> 

<span data-ttu-id="f8d7e-105">V hlavní knize můžete provést uzávěrku období nebo roku.</span><span class="sxs-lookup"><span data-stu-id="f8d7e-105">In General ledger, you can complete closing procedures for a period or a year.</span></span> <span data-ttu-id="f8d7e-106">Postupy uzávěrky připravují systém pro nové období.</span><span class="sxs-lookup"><span data-stu-id="f8d7e-106">Closing processes prepare the system for a new period.</span></span> <span data-ttu-id="f8d7e-107">Abyste systém připravili na nový rok, je nutné spustit proces roční uzávěrky.</span><span class="sxs-lookup"><span data-stu-id="f8d7e-107">To prepare the system for a new year, you must run the year end close process.</span></span> <span data-ttu-id="f8d7e-108">Každá organizace má různé postupy a kroky, které provádí na konci období.</span><span class="sxs-lookup"><span data-stu-id="f8d7e-108">Each organization has different processes and steps that it performs for the end of a period.</span></span> <span data-ttu-id="f8d7e-109">Zde jsou některé volitelné kroky pro ukončení období:</span><span class="sxs-lookup"><span data-stu-id="f8d7e-109">Here are some optional steps for period ends:</span></span>

-   <span data-ttu-id="f8d7e-110">Dokončete všechny úlohy pro všechny ostatní moduly, jako jsou například Pohledávky, Závazky a Zásoby.</span><span class="sxs-lookup"><span data-stu-id="f8d7e-110">Complete all the tasks for all other modules, such as Accounts receivable, Accounts payable, and Inventory.</span></span>
-   <span data-ttu-id="f8d7e-111">Ověřte, že všechny deníky jsou zaúčtovány.</span><span class="sxs-lookup"><span data-stu-id="f8d7e-111">Verify that all journals are posted.</span></span>
-   <span data-ttu-id="f8d7e-112">Spusťte přecenění cizí měny pro generování nerealizované částky zisku nebo ztráty.</span><span class="sxs-lookup"><span data-stu-id="f8d7e-112">Run foreign currency revaluation to generate any unrealized gain or loss amounts.</span></span>
-   <span data-ttu-id="f8d7e-113">Vyrovnejte transakce pro každý účet hlavní knihy</span><span class="sxs-lookup"><span data-stu-id="f8d7e-113">Settle transactions for each ledger account.</span></span>
-   <span data-ttu-id="f8d7e-114">Zpracujte všechna požadovaná přidělení.</span><span class="sxs-lookup"><span data-stu-id="f8d7e-114">Process any required allocations.</span></span>
-   <span data-ttu-id="f8d7e-115">Ručně zaúčtujte úpravy po konci období.</span><span class="sxs-lookup"><span data-stu-id="f8d7e-115">Manually post period-end adjustments.</span></span>
-   <span data-ttu-id="f8d7e-116">Zapište transakce do deníku a zkontrolujte sestavu **Deník hlavní knihy**.</span><span class="sxs-lookup"><span data-stu-id="f8d7e-116">Journalize transactions, and review the **Ledger journal** report.</span></span>
-   <span data-ttu-id="f8d7e-117">Proveďte konsolidaci pomocí konsolidační společnosti nebo Finančního výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="f8d7e-117">Perform a consolidation by using a consolidation company or Financial reporting.</span></span>
-   <span data-ttu-id="f8d7e-118">Generujte finanční výkazy konce období pomocí Finančního výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="f8d7e-118">Generate period-end financial statements by using Financial reporting.</span></span>
-   <span data-ttu-id="f8d7e-119">Nastavte období hlavní knihy na **Blokováno**, aby neprobíhalo žádné další zaúčtování.</span><span class="sxs-lookup"><span data-stu-id="f8d7e-119">Set ledger periods to **On hold**, so that no further posting occurs.</span></span> <span data-ttu-id="f8d7e-120">Můžete také omezit období pro určitou skupinu uživatelů, zatímco probíhají aktivity na konci období, abyste získali lepší kontrolu.</span><span class="sxs-lookup"><span data-stu-id="f8d7e-120">You can also restrict a period to a specific user group while period-end activities are occurring, for better control.</span></span> <span data-ttu-id="f8d7e-121">Není vhodné nastavit období na **Trvale zavřeno**, protože uzavřené období nelze znovu otevřít.</span><span class="sxs-lookup"><span data-stu-id="f8d7e-121">It's not a good idea to set periods to **Permanently closed**, because you can't reopen a period that has been closed.</span></span>

<span data-ttu-id="f8d7e-122">Pracovní prostor uzavření finančního období lze použít k uspořádání a sledování úkolů vyžadovaných pro různé procesy na konci období.</span><span class="sxs-lookup"><span data-stu-id="f8d7e-122">The Financial period close workspace can be used to organize and track the tasks required for various period end processes.</span></span> 


<span data-ttu-id="f8d7e-123">Další informace naleznete v následujících tématech:</span><span class="sxs-lookup"><span data-stu-id="f8d7e-123">For more information, see the following topics for more information:</span></span>
- [<span data-ttu-id="f8d7e-124">Pracovní prostor uzavření finančního období</span><span class="sxs-lookup"><span data-stu-id="f8d7e-124">Financial period close workspace</span></span>](financial-period-close-workspace.md) 
- [<span data-ttu-id="f8d7e-125">Roční uzávěrka</span><span class="sxs-lookup"><span data-stu-id="f8d7e-125">Year-end close</span></span>](Year-end-close.md)  
- [<span data-ttu-id="f8d7e-126">Hromadné uzavření finančního období</span><span class="sxs-lookup"><span data-stu-id="f8d7e-126">Mass financial period close</span></span>](tasks/mass-financial-period-close.md)




