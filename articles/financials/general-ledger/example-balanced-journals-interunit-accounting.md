---
title: "Vyrovnávací deníky pro mezijednotkové účetnictví"
description: "Tento článek ukazuje, jak je deník automaticky vyrovnán pro výběru možnosti vyrovnávací finanční dimenzi na stránce hlavní knihy."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerParameters
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 15791
ms.assetid: 301bd80e-f8b1-4f12-8194-e6d7de736084
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: f45d180dc8dcafb0579e76b890dd5d516df5b8c0
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---

# <a name="balanced-journals-for-interunit-accounting"></a><span data-ttu-id="11c7b-103">Vyrovnávací deníky pro mezijednotkové účetnictví</span><span class="sxs-lookup"><span data-stu-id="11c7b-103">Balanced journals for interunit accounting</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="11c7b-104">Tento článek ukazuje, jak je deník automaticky vyrovnán pro výběru možnosti vyrovnávací finanční dimenzi na stránce hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="11c7b-104">This article shows how a journal is automatically balanced when a balancing financial dimension is selected on the Ledger page.</span></span> 

<span data-ttu-id="11c7b-105">Pokud účetní zápisy nejsou vyrovnány na úrovni hodnot finančních dimenzí, jsou automaticky vytvořeny další položky účtu za účelem vyrovnání deníku.</span><span class="sxs-lookup"><span data-stu-id="11c7b-105">If account entries don't balance at the level of the financial dimension values, additional account entries are created automatically to balance the journal.</span></span> <span data-ttu-id="11c7b-106">Použijte tyto účetní položky v typech zaúčtování **Mezijednotkové účetnictví – má dáti** a**Mezijednotkové účetnictví – dal** na stránce **Účty pro automatické transakce**.</span><span class="sxs-lookup"><span data-stu-id="11c7b-106">These account entries use the **Interunit - debit** and **Interunit - credit** posting types on the **Accounts for automatic transactions** page to determine the main account.</span></span> <span data-ttu-id="11c7b-107">Například pobočka, tj. druhý segment účtu hlavní knihy, bude vybrána jako vyrovnávací finanční dimenze, a budou vytvořeny následující účetní položky.</span><span class="sxs-lookup"><span data-stu-id="11c7b-107">For example, Branch, which is the second segment of the ledger account, is selected as the balancing financial dimension, and the following accounting entries are about to be created.</span></span>

|                      |           |
|----------------------|-----------|
| <span data-ttu-id="11c7b-108">6100 – MSP – OU\_256</span><span class="sxs-lookup"><span data-stu-id="11c7b-108">6100 – MSP – OU\_256</span></span> | <span data-ttu-id="11c7b-109">100.00 OŘ</span><span class="sxs-lookup"><span data-stu-id="11c7b-109">100.00 DR</span></span> |
| <span data-ttu-id="11c7b-110">6100 – NY – OU\_249</span><span class="sxs-lookup"><span data-stu-id="11c7b-110">6100 – NY – OU\_249</span></span>  | <span data-ttu-id="11c7b-111">100.00 OŘ</span><span class="sxs-lookup"><span data-stu-id="11c7b-111">100.00 DR</span></span> |
| <span data-ttu-id="11c7b-112">2100 – MSP – OU\_256</span><span class="sxs-lookup"><span data-stu-id="11c7b-112">2100 – MSP – OU\_256</span></span> | <span data-ttu-id="11c7b-113">200.00 CR</span><span class="sxs-lookup"><span data-stu-id="11c7b-113">200.00 CR</span></span> |

<span data-ttu-id="11c7b-114">V tomto případě dojde k určení následujících zůstatků:</span><span class="sxs-lookup"><span data-stu-id="11c7b-114">In this case, the following balances are determined:</span></span>

-   <span data-ttu-id="11c7b-115">Pro pobočku MSP = 100,00 CR</span><span class="sxs-lookup"><span data-stu-id="11c7b-115">For Branch MSP = 100.00 CR</span></span>
-   <span data-ttu-id="11c7b-116">Pro pobočku NY = 100,00 DR</span><span class="sxs-lookup"><span data-stu-id="11c7b-116">For Branch NY = 100.00 DR</span></span>

<span data-ttu-id="11c7b-117">Následující účetní položky jsou proto vytvořeny automaticky tak, aby vyrovnaly deník na úrovni hodnot finančních dimenzí.</span><span class="sxs-lookup"><span data-stu-id="11c7b-117">Therefore, the following accounting entries are created automatically to balance the  journal at the level of the financial dimension values.</span></span>

|                                   |           |
|-----------------------------------|-----------|
| <span data-ttu-id="11c7b-118">(Mezijednotkový debit) – MSP – OU\_256</span><span class="sxs-lookup"><span data-stu-id="11c7b-118">(Interunit Debit) – MSP – OU\_256</span></span> | <span data-ttu-id="11c7b-119">100.00 OŘ</span><span class="sxs-lookup"><span data-stu-id="11c7b-119">100.00 DR</span></span> |
| <span data-ttu-id="11c7b-120">(Interunit Credit) – NY – OU\_249</span><span class="sxs-lookup"><span data-stu-id="11c7b-120">(Interunit Credit) – NY – OU\_249</span></span> | <span data-ttu-id="11c7b-121">100.00 CR</span><span class="sxs-lookup"><span data-stu-id="11c7b-121">100.00 CR</span></span> |






