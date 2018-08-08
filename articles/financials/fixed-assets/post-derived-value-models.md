---
title: "Zaúčtování pomocí odvozených knih"
description: "Tento článek popisuje, jak lze používat odvozené knihy."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetBookTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 3421
ms.assetid: f5187c21-eec5-4148-b178-b8a5feff7f23
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: ff1dbf67a53a5639e448da707898b55cd00cba94
ms.contentlocale: cs-cz
ms.lasthandoff: 08/07/2018

---

# <a name="post-with-derived-books"></a><span data-ttu-id="78797-103">Zaúčtování pomocí odvozených knih</span><span class="sxs-lookup"><span data-stu-id="78797-103">Post with derived books</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="78797-104">Tento článek popisuje, jak lze používat odvozené knihy.</span><span class="sxs-lookup"><span data-stu-id="78797-104">This article describes how to use derived books.</span></span>

<span data-ttu-id="78797-105">Jestliže zaúčtujete transakce pro oceňovací model obsahující odvozené knihy, zaúčtují se transakce odvozených knih automaticky z deníků, nákupních objednávek či volných faktur.</span><span class="sxs-lookup"><span data-stu-id="78797-105">When you post transactions for a book that contains derived books, the derived book transactions are posted automatically in journals, purchase orders, or free text invoices.</span></span> <span data-ttu-id="78797-106">Když ale připravíte transakce primární knihy v deníku dlouhodobého majetku, můžete zobrazit a změnit částky odvozených transakcí před jejich zaúčtováním.</span><span class="sxs-lookup"><span data-stu-id="78797-106">However, if you prepare the primary book transactions in the Fixed assets journal, you can view and modify the amounts of the derived transactions before you post them.</span></span>
-   <span data-ttu-id="78797-107">Některé účty, například účet DPH a účty odběratelů nebo dodavatelů, se aktualizují pouze jednou zaúčtováním primární knihy.</span><span class="sxs-lookup"><span data-stu-id="78797-107">Certain accounts, such as sales tax and customer or vendor accounts, are updated only once by postings of the primary book.</span></span> <span data-ttu-id="78797-108">Transakce odvozené knihy jsou zaúčtovány na účtech, které byly definovány pro odvozenou knihu na stránce Účetní profily dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="78797-108">The derived book transactions are posted to the accounts that have been defined for the derived book in the Fixed asset posting profiles page.</span></span>
-   <span data-ttu-id="78797-109">Jako možnost Typ transakce pro odvozené knihy se často používá možnost Pořízení.</span><span class="sxs-lookup"><span data-stu-id="78797-109">Acquisition is often used as the transaction type for the derived books.</span></span> <span data-ttu-id="78797-110">Tuto možnost použijte v případě, že se má kniha a odvozená kniha použít pro dlouhodobý majetek od doby jeho akvizice.</span><span class="sxs-lookup"><span data-stu-id="78797-110">You use this when the book and the derived book should be applied to the fixed asset from the time of the acquisition of the fixed asset.</span></span>
-   <span data-ttu-id="78797-111">Pro typ transakce lze také použít jiné hodnoty.</span><span class="sxs-lookup"><span data-stu-id="78797-111">Other values for the transaction type can also apply.</span></span> <span data-ttu-id="78797-112">Když mají například primární kniha a odvozené knihy stejné intervaly s ohledem na prodej nebo likvidaci, jsou pro nastavení odvozené knihy odpisů k dispozici všechny typy transakcí dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="78797-112">For example, if the primary book and the derived books have the same intervals regarding sale or disposal, all fixed asset transaction types are available for the setup of a derived book.</span></span>

> [!WARNING]
> <span data-ttu-id="78797-113">Odpisy zaúčtované v odvozené knize odpisů budou na stejnou částku, která byla zaúčtována v primární knize.</span><span class="sxs-lookup"><span data-stu-id="78797-113">Depreciation posted in the derived book will be the same amount as was posted for the primary book.</span></span> <span data-ttu-id="78797-114">Pokud se metody odpisu u jednotlivých knih liší, neměly by být vytvářeny transakce odpisů pomocí odvozeného procesu.</span><span class="sxs-lookup"><span data-stu-id="78797-114">If the depreciation methods are different between the books, you should not generate depreciation transactions using the derived process.</span></span> |

## <a name="example"></a><span data-ttu-id="78797-115">Příklad</span><span class="sxs-lookup"><span data-stu-id="78797-115">Example</span></span> 
<span data-ttu-id="78797-116">Níže naleznete informace popisující nastavení transakcí pořízení s funkcí odvozené knihy.</span><span class="sxs-lookup"><span data-stu-id="78797-116">The following information describes how to set up acquisition transactions with the derived book functionality.</span></span>

1.  <span data-ttu-id="78797-117">Vytvořte knihy na stránce Knihy.</span><span class="sxs-lookup"><span data-stu-id="78797-117">Create the books on the Books page.</span></span>
    -   <span data-ttu-id="78797-118">Kniha pro účetnictví: OM 1, aktuální účtovací vrstva</span><span class="sxs-lookup"><span data-stu-id="78797-118">The book for accounting: VM 1, Current posting layer</span></span>
    -   <span data-ttu-id="78797-119">Kniha pro daňové účely: OM 2, účtovací vrstva pro daně</span><span class="sxs-lookup"><span data-stu-id="78797-119">The book for tax purposes: VM 2, Tax posting layer</span></span>

2.  <span data-ttu-id="78797-120">Na virtuálním počítači 1 klikněte na kartu Odvozené knihy. Zvolte virtuální počítač 2 v poli Kniha a Pořízení v poli Typ transakce.</span><span class="sxs-lookup"><span data-stu-id="78797-120">On VM 1, click the Derived books tab. Select VM 2 in the Book field, and Acquisition in the Transaction type field.</span></span>

<span data-ttu-id="78797-121">Knihy lze potom připojit k určitému dlouhodobému majetku.</span><span class="sxs-lookup"><span data-stu-id="78797-121">The books then can be attached to specific fixed assets.</span></span> 

<span data-ttu-id="78797-122">Když je zaúčtováno pořízení pro dlouhodobý majetek s knihou OM 1, pořízení se nezaúčtuje pouze v modelu OM 1, ale také v odvozené knize OM 2.</span><span class="sxs-lookup"><span data-stu-id="78797-122">When an acquisition is posted for a fixed asset with book VM 1, the acquisition is posted not only on VM 1, but also on the derived book VM 2.</span></span> <span data-ttu-id="78797-123">Stav obou knih dlouhodobého majetku je aktualizován na Otevřeno.</span><span class="sxs-lookup"><span data-stu-id="78797-123">The status of both fixed asset books is updated to Open.</span></span>

> [!NOTE]                                                                                                         
> <span data-ttu-id="78797-124">Pokud nepoužíváte odvozené knihy, je nutné zaúčtovat pořízení dlouhodobého majetku pro knihu OM 1 i knihu OM 2.</span><span class="sxs-lookup"><span data-stu-id="78797-124">If you do not use derived books, you must post the acquisition of the fixed asset both for book VM 1 and book VM 2.</span></span>

<span data-ttu-id="78797-125">Další informace naleznete v tématu [Odvozené knihy](derived-books.md)</span><span class="sxs-lookup"><span data-stu-id="78797-125">For more information, see [Derived books](derived-books.md)</span></span>




