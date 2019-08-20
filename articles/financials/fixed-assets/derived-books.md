---
title: Odvozené knihy
description: Tento článek podává přehled o funkci Odvozená kniha.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBookTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 3401
ms.assetid: 862d6450-187b-497f-9822-cce45f2c65a9
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4a649fdbc355b3382bc6c80be03f8b37a06d5226
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/01/2019
ms.locfileid: "1840570"
---
# <a name="derived-books"></a><span data-ttu-id="8be1a-103">Odvozené knihy</span><span class="sxs-lookup"><span data-stu-id="8be1a-103">Derived books</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8be1a-104">Tento článek podává přehled o funkci Odvozená kniha.</span><span class="sxs-lookup"><span data-stu-id="8be1a-104">This article provides an overview of derived book functionality.</span></span>

<span data-ttu-id="8be1a-105">Smyslem odvozených knih je zjednodušit zaúčtování transakcí knih dlouhodobého majetku naplánovaných v pravidelných intervalech.</span><span class="sxs-lookup"><span data-stu-id="8be1a-105">The purpose of derived books is to simplify the posting of fixed asset book transactions that are planned for regular intervals.</span></span>  <span data-ttu-id="8be1a-106">Zvolíte jednu knihu jako primární.</span><span class="sxs-lookup"><span data-stu-id="8be1a-106">You choose one book as the primary book.</span></span> <span data-ttu-id="8be1a-107">Jde obvykle o knihu používanou pro účetní odpisy.</span><span class="sxs-lookup"><span data-stu-id="8be1a-107">This usually is the book that is used for accounting depreciation.</span></span> <span data-ttu-id="8be1a-108">Pak ji připojíte k ostatním knihám, které jsou nastaveny pro zaúčtování transakcí ve stejných intervalech jako primární kniha.</span><span class="sxs-lookup"><span data-stu-id="8be1a-108">You then attach to it other books that are set up to post transactions in the same intervals as the primary book.</span></span> <span data-ttu-id="8be1a-109">Knihy odpisů hodnoty DPH jsou často nastaveny jako odvozené knihy.</span><span class="sxs-lookup"><span data-stu-id="8be1a-109">Tax depreciation books are often set up as derived books.</span></span> 

<span data-ttu-id="8be1a-110">Nejběžnější transakce pro nastavení zaúčtování odvozených knih jsou pořízení, úprava pořízení a likvidace.</span><span class="sxs-lookup"><span data-stu-id="8be1a-110">The most common transactions to set up to post to derived books are acquisitions, acquisition adjustments, and disposals.</span></span> 

## <a name="example"></a><span data-ttu-id="8be1a-111">Příklad</span><span class="sxs-lookup"><span data-stu-id="8be1a-111">Example</span></span>

<span data-ttu-id="8be1a-112">Kniha B a kniha C jsou nastaveny jako odvozené knihy pro knihu A pro typ transakce pořízení.</span><span class="sxs-lookup"><span data-stu-id="8be1a-112">Book B and book C are set up as derived books for book A for the Acquisition transaction type.</span></span> <span data-ttu-id="8be1a-113">V knize A zadáte transakci pořízení majetku 123 s hodnotou 1 500,00.</span><span class="sxs-lookup"><span data-stu-id="8be1a-113">In book A, you enter an acquisition transaction for asset 123 for 1,500.00.</span></span> 

<span data-ttu-id="8be1a-114">Při zaúčtování transakce je vygenerována transakce pořízení a je zaúčtována do majetku 123 pro knihu B a do majetku 123 pro knihu C s hodnotou 1 500,00.</span><span class="sxs-lookup"><span data-stu-id="8be1a-114">When the transaction is posted, an acquisition transaction is generated and posted in asset 123 for book B and in asset 123 for book C for 1,500.00.</span></span> <span data-ttu-id="8be1a-115">Při přípravě transakcí primární knihy k zaúčtování do deníku dlouhodobého majetku lze také zobrazit a upravit transakce odvozených knih odpisů.</span><span class="sxs-lookup"><span data-stu-id="8be1a-115">When you prepare the transactions of the primary book for posting in the fixed asset journal, you can also view and modify the transactions of the derived books.</span></span> <span data-ttu-id="8be1a-116">Při přípravě transakcí primární knihy v jiném deníku nelze zobrazit transakce odvozených hodnot.</span><span class="sxs-lookup"><span data-stu-id="8be1a-116">If you prepare the primary book transactions in another journal, the transactions of the derived value are not displayed.</span></span> <span data-ttu-id="8be1a-117">Avšak zaúčtováním do příslušných účtů a účtovacích vrstev po zaúčtování transakcí primární knihy.</span><span class="sxs-lookup"><span data-stu-id="8be1a-117">However, they are posted to the appropriate accounts and posting layers when you post the primary book transactions.</span></span>

> [!NOTE]                                                                                                                               
> <span data-ttu-id="8be1a-118">Knihy, které jsou nastaveny pro zaúčtování transakcí v intervalech jiných než je interval pro primární knihu, musí být připojeny k dlouhodobému majetku jako samostatné knihy a nikoliv jako odvozené knihy.</span><span class="sxs-lookup"><span data-stu-id="8be1a-118">Books that are set up to post transactions at intervals other than the primary book intervals must be attached to the fixed asset as separate books and not as derived books.</span></span>  

<span data-ttu-id="8be1a-119">Další informace naleznete v tématu [Zaúčtování pomocí odvozených knih](post-derived-value-models.md).</span><span class="sxs-lookup"><span data-stu-id="8be1a-119">For more information, see [Posting with derived books](post-derived-value-models.md).</span></span>



