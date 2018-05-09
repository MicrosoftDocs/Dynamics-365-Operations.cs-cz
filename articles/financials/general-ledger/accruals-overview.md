---
title: "Přehled časově rozlišených položek"
description: "V tomto článku jsou popsána časová rozlišení a jsou zde také informace o způsobu jejich nastavení a vytvoření transakcí."
author: aprilolson
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerAccuralTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 14131
ms.assetid: 0489b59a-37a7-4a78-87bf-4b597e9efad9
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: b3f989b1e442c35b5bed3c34c9cc6e31de5c4c9e
ms.contentlocale: cs-cz
ms.lasthandoff: 05/08/2018

---

# <a name="accruals-overview"></a><span data-ttu-id="de596-103">Přehled časově rozlišených položek</span><span class="sxs-lookup"><span data-stu-id="de596-103">Accruals overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="de596-104">V tomto článku jsou popsána časová rozlišení a jsou zde také informace o způsobu jejich nastavení a vytvoření transakcí.</span><span class="sxs-lookup"><span data-stu-id="de596-104">This article describes accruals, and provides information about how to set them up and create transactions.</span></span>

<span data-ttu-id="de596-105">Časové rozlišené položky se používají v účtování časového rozlišení ke sledování výnosu, který je uznán v období, kdy je získán – nikoli při přijetí platby, a ke sledování výdajů (náklady), které jsou uznány, když k nim dojde – nikoli při provedení platby.</span><span class="sxs-lookup"><span data-stu-id="de596-105">Accruals are used in accrual accounting to track revenue that is recognized in the period that it's earned in, not when payment is received, and to track expenses (costs) that are recognized when they occur, not when payment is made.</span></span>

## <a name="accrual-schemes"></a><span data-ttu-id="de596-106">Schémata časového rozlišení</span><span class="sxs-lookup"><span data-stu-id="de596-106">Accrual schemes</span></span>
<span data-ttu-id="de596-107">Schémata časově rozlišených položek se používají k nastavení odložených výnosů a nákladů a stejné schéma časového rozlišení lze použít pro výnosy a náklady.</span><span class="sxs-lookup"><span data-stu-id="de596-107">Accrual schemes are used to set up the deferred revenue and costs, and the same accrual scheme can be used for both revenue and costs.</span></span> <span data-ttu-id="de596-108">Časová rozlišení hlavní knihy přerozdělují náklady nebo výnosy řádku deníku, takže náklady a výnosy se rozpoznají v příslušných obdobích.</span><span class="sxs-lookup"><span data-stu-id="de596-108">Ledger accruals redistribute the costs or revenue of a journal line so that the costs and revenues are recognized in the appropriate periods.</span></span> <span data-ttu-id="de596-109">Na stránce **Schémat časového rozlišení** zadáte debetní a kreditní účty, které budou použity po nasazení schématu časového rozlišení.</span><span class="sxs-lookup"><span data-stu-id="de596-109">On the **Accrual scheme** page, you specify the debit and the credit accounts that will be used when the accrual scheme is applied.</span></span>

-   <span data-ttu-id="de596-110">**Má dáti** – hlavní účet, který definujete, nahradí hlavní účet má dáti na řádku dokladu deníku.</span><span class="sxs-lookup"><span data-stu-id="de596-110">**Debit** – The main account that you define will replace the debit main account on the journal voucher line.</span></span> <span data-ttu-id="de596-111">Tento účet se také použije ke stornování časově rozlišených položek podle transakcí časového rozlišení hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="de596-111">This account will also be used for the reversal of the deferral, based on the ledger accrual transactions.</span></span>
-   <span data-ttu-id="de596-112">**Dal** – hlavní účet, který definujete, nahradí hlavní účet dal na řádku dokladu deníku.</span><span class="sxs-lookup"><span data-stu-id="de596-112">**Credit** – the main account that you define will replace the credit main account on the journal voucher line.</span></span> <span data-ttu-id="de596-113">Tento účet se také použije ke stornování časově rozlišených položek podle transakcí časového rozlišení hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="de596-113">This account will also be used for the reversal of the deferral, based on the ledger accrual transactions.</span></span>

<span data-ttu-id="de596-114">Po určení účtů, které chcete použít, můžete určit, jak se číslo dokladu vytváří při vytvoření transakcí časového rozlišení.</span><span class="sxs-lookup"><span data-stu-id="de596-114">After you determine which accounts to use, you can specify how the voucher number is created when accrual transactions are created.</span></span> <span data-ttu-id="de596-115">Můžete také určit, jak často k transakcím dochází, kolikrát se transakce vytváří a kdy se transakce zaúčtovávají.</span><span class="sxs-lookup"><span data-stu-id="de596-115">You can also specify how often the transactions occur, the number of times that the transactions are created, and when the transactions are posted.</span></span> <span data-ttu-id="de596-116">Po vytvoření schématu časového rozlišení ho můžete použít v některých denících pomocí funkce časového rozlišení hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="de596-116">After the accrual scheme has been created, you can use it in some of the journals by using the Ledger accruals function.</span></span>

## <a name="ledger-accruals"></a><span data-ttu-id="de596-117">Časové rozlišení hlavní knihy</span><span class="sxs-lookup"><span data-stu-id="de596-117">Ledger accruals</span></span>
<span data-ttu-id="de596-118">Jakmile vstoupíte do deníku, můžete kliknout na volbu **Časové rozlišení hlavní knihy** v nabídce **Funkce**.</span><span class="sxs-lookup"><span data-stu-id="de596-118">When you enter a journal, you can click **Ledger accruals** on the **Functions** menu.</span></span> <span data-ttu-id="de596-119">Až poté vyberte schéma časového rozlišení, se zobrazí základní částka v deníku, která se rozloží v období podle určení schématu časového rozlišení.</span><span class="sxs-lookup"><span data-stu-id="de596-119">Then, when you select the accrual scheme, you will see the base amount from the journal that will be spread over the period, as determined by the accrual scheme.</span></span> <span data-ttu-id="de596-120">Například pokud provádíte platbu pojištění pro zaměstnance na celý rok v lednu a částka je na 12 000, je nutné rozpoznat tyto náklady každý měsíce.</span><span class="sxs-lookup"><span data-stu-id="de596-120">For example, if you pay an employee's insurance for the whole year in January, and the amount is 12,000, you must recognize that expense each month.</span></span> <span data-ttu-id="de596-121">Můžete vybrat počáteční datum.</span><span class="sxs-lookup"><span data-stu-id="de596-121">You can select the start date.</span></span> <span data-ttu-id="de596-122">Můžete také určit, zda je částka, která je časově rozlišená, založená na účtu nebo protiúčtu.</span><span class="sxs-lookup"><span data-stu-id="de596-122">You can also specify whether the amount that is accrued is based on the account or the offset account.</span></span> <span data-ttu-id="de596-123">Po provedení výběru klikněte na možnost **Transakce** pro zobrazení všech transakcí, které byly vytvořeny na základě schématu časového rozlišení.</span><span class="sxs-lookup"><span data-stu-id="de596-123">After you make your selections, click **Transactions** to view all the transactions that have been created based on the accrual scheme.</span></span> <span data-ttu-id="de596-124">Například pokud rozložíte 12 000 ve výdajích pojištění na rok, zobrazí se 1 000 pro každý měsíc.</span><span class="sxs-lookup"><span data-stu-id="de596-124">For example, if you spread the 12,000 in insurance expenses over the year, you will see 1,000 for each month.</span></span> <span data-ttu-id="de596-125">Po zaúčtování deníku můžete zobrazit transakce použitím stránky dotazu **Transakce dokladu**.</span><span class="sxs-lookup"><span data-stu-id="de596-125">After you post the journal, you can view the transactions by using the **Voucher transactions** inquiry page.</span></span> <span data-ttu-id="de596-126">Pokud schéma časového rozlišení nelze použít (například když se jedná o fakturu prodejní objednávky nebo fakturu nákupní objednávky), můžete připsat předplacenou částku a odepsat částku výdajů.</span><span class="sxs-lookup"><span data-stu-id="de596-126">If an accrual scheme can't be applied (for example, when a sales order invoice or purchase order invoice is involved), you can credit the prepaid amount and debit the expense amount.</span></span> <span data-ttu-id="de596-127">Můžete vybrat **Protiúčet**, když nasazujete schéma časového rozlišení.</span><span class="sxs-lookup"><span data-stu-id="de596-127">You can then select **Offset** when you apply the accrual scheme.</span></span>


<span data-ttu-id="de596-128">Další informace naleznete v tématu [Vytvoření schémat časového rozlišení](tasks/create-accrual-schemes.md) a [Vytvoření transakcí časového rozlišení hlavní knihy](tasks/create-ledger-accrual-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="de596-128">For more information, see [Create accrual schemes](tasks/create-accrual-schemes.md) and [Create ledger accrual transactions](tasks/create-ledger-accrual-transactions.md).</span></span>

