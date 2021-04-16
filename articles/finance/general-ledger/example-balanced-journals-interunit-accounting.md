---
title: Vyrovnávací deníky pro mezijednotkové účetnictví
description: Tento článek ukazuje, jak je deník automaticky vyrovnán pro výběru možnosti vyrovnávací finanční dimenzi na stránce hlavní knihy.
author: ShylaThompson
ms.date: 10/30/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerParameters
audience: Application User
ms.reviewer: roschlom
ms.custom: 15791
ms.assetid: 301bd80e-f8b1-4f12-8194-e6d7de736084
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a5a926adcc631ec286f37796713466eb0144494c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818385"
---
# <a name="balanced-journals-for-interunit-accounting"></a><span data-ttu-id="bc177-103">Vyrovnávací deníky pro mezijednotkové účetnictví</span><span class="sxs-lookup"><span data-stu-id="bc177-103">Balanced journals for interunit accounting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bc177-104">Tento článek ukazuje, jak je deník automaticky vyrovnán pro výběru možnosti vyrovnávací finanční dimenzi na stránce hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="bc177-104">This article shows how a journal is automatically balanced when a balancing financial dimension is selected on the Ledger page.</span></span> 

<span data-ttu-id="bc177-105">Pokud účetní zápisy nejsou vyrovnány na úrovni hodnot finančních dimenzí, jsou automaticky vytvořeny další položky účtu za účelem vyrovnání deníku.</span><span class="sxs-lookup"><span data-stu-id="bc177-105">If account entries don't balance at the level of the financial dimension values, additional account entries are created automatically to balance the journal.</span></span> <span data-ttu-id="bc177-106">Použijte tyto účetní položky v typech zaúčtování **Mezijednotkové účetnictví – má dáti** a **Mezijednotkové účetnictví – dal** na stránce **Účty pro automatické transakce**.</span><span class="sxs-lookup"><span data-stu-id="bc177-106">These account entries use the **Interunit - debit** and **Interunit - credit** posting types on the **Accounts for automatic transactions** page to determine the main account.</span></span> <span data-ttu-id="bc177-107">Například Obchodní jednotka, tj. druhý segment účtu hlavní knihy, bude vybrána jako vyrovnávací finanční dimenze, a budou vytvořeny následující účetní položky.</span><span class="sxs-lookup"><span data-stu-id="bc177-107">For example, Business Unit, which is the second segment of the ledger account, is selected as the balancing financial dimension, and the following accounting entries are about to be created.</span></span>

| &nbsp;               | &nbsp;    |
|----------------------|-----------|
| <span data-ttu-id="bc177-108">6100 – MSP – OU\_256</span><span class="sxs-lookup"><span data-stu-id="bc177-108">6100 – MSP – OU\_256</span></span> | <span data-ttu-id="bc177-109">100.00 OŘ</span><span class="sxs-lookup"><span data-stu-id="bc177-109">100.00 DR</span></span> |
| <span data-ttu-id="bc177-110">6100 – NY – OU\_249</span><span class="sxs-lookup"><span data-stu-id="bc177-110">6100 – NY – OU\_249</span></span>  | <span data-ttu-id="bc177-111">100.00 OŘ</span><span class="sxs-lookup"><span data-stu-id="bc177-111">100.00 DR</span></span> |
| <span data-ttu-id="bc177-112">2100 – MSP – OU\_256</span><span class="sxs-lookup"><span data-stu-id="bc177-112">2100 – MSP – OU\_256</span></span> | <span data-ttu-id="bc177-113">200.00 CR</span><span class="sxs-lookup"><span data-stu-id="bc177-113">200.00 CR</span></span> |

<span data-ttu-id="bc177-114">V tomto případě dojde k určení následujících zůstatků:</span><span class="sxs-lookup"><span data-stu-id="bc177-114">In this case, the following balances are determined:</span></span>

-   <span data-ttu-id="bc177-115">Pro obchodní jednotku MSP = 100.00 CR</span><span class="sxs-lookup"><span data-stu-id="bc177-115">For Business Unit MSP = 100.00 CR</span></span>
-   <span data-ttu-id="bc177-116">Pro obchodní jednotku NY = 100.00 DR</span><span class="sxs-lookup"><span data-stu-id="bc177-116">For Business Unit NY = 100.00 DR</span></span>

<span data-ttu-id="bc177-117">Následující účetní položky jsou proto vytvořeny automaticky tak, aby vyrovnaly deník na úrovni hodnot finančních dimenzí.</span><span class="sxs-lookup"><span data-stu-id="bc177-117">Therefore, the following accounting entries are created automatically to balance the  journal at the level of the financial dimension values.</span></span>

| &nbsp;                            | &nbsp;    |
|-----------------------------------|-----------|
| <span data-ttu-id="bc177-118">(Mezijednotkový debit) – MSP – OU\_256</span><span class="sxs-lookup"><span data-stu-id="bc177-118">(Interunit Debit) – MSP – OU\_256</span></span> | <span data-ttu-id="bc177-119">100.00 OŘ</span><span class="sxs-lookup"><span data-stu-id="bc177-119">100.00 DR</span></span> |
| <span data-ttu-id="bc177-120">(Interunit Credit) – NY – OU\_249</span><span class="sxs-lookup"><span data-stu-id="bc177-120">(Interunit Credit) – NY – OU\_249</span></span> | <span data-ttu-id="bc177-121">100.00 CR</span><span class="sxs-lookup"><span data-stu-id="bc177-121">100.00 CR</span></span> |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]