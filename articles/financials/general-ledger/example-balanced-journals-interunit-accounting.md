---
title: Vyrovnávací deníky pro mezijednotkové účetnictví
description: Tento článek ukazuje, jak je deník automaticky vyrovnán pro výběru možnosti vyrovnávací finanční dimenzi na stránce hlavní knihy.
author: ShylaThompson
manager: AnnBe
ms.date: 10/30/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerParameters
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 15791
ms.assetid: 301bd80e-f8b1-4f12-8194-e6d7de736084
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5b596a2332a9ada01df7b4e718a79eb624ee52fc
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1549097"
---
# <a name="balanced-journals-for-interunit-accounting"></a><span data-ttu-id="05cf3-103">Vyrovnávací deníky pro mezijednotkové účetnictví</span><span class="sxs-lookup"><span data-stu-id="05cf3-103">Balanced journals for interunit accounting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="05cf3-104">Tento článek ukazuje, jak je deník automaticky vyrovnán pro výběru možnosti vyrovnávací finanční dimenzi na stránce hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="05cf3-104">This article shows how a journal is automatically balanced when a balancing financial dimension is selected on the Ledger page.</span></span> 

<span data-ttu-id="05cf3-105">Pokud účetní zápisy nejsou vyrovnány na úrovni hodnot finančních dimenzí, jsou automaticky vytvořeny další položky účtu za účelem vyrovnání deníku.</span><span class="sxs-lookup"><span data-stu-id="05cf3-105">If account entries don't balance at the level of the financial dimension values, additional account entries are created automatically to balance the journal.</span></span> <span data-ttu-id="05cf3-106">Použijte tyto účetní položky v typech zaúčtování **Mezijednotkové účetnictví – má dáti** a**Mezijednotkové účetnictví – dal** na stránce **Účty pro automatické transakce**.</span><span class="sxs-lookup"><span data-stu-id="05cf3-106">These account entries use the **Interunit - debit** and **Interunit - credit** posting types on the **Accounts for automatic transactions** page to determine the main account.</span></span> <span data-ttu-id="05cf3-107">Například Obchodní jednotka, tj. druhý segment účtu hlavní knihy, bude vybrána jako vyrovnávací finanční dimenze, a budou vytvořeny následující účetní položky.</span><span class="sxs-lookup"><span data-stu-id="05cf3-107">For example, Business Unit, which is the second segment of the ledger account, is selected as the balancing financial dimension, and the following accounting entries are about to be created.</span></span>

|                      |           |
|----------------------|-----------|
| <span data-ttu-id="05cf3-108">6100 – MSP – OU\_256</span><span class="sxs-lookup"><span data-stu-id="05cf3-108">6100 – MSP – OU\_256</span></span> | <span data-ttu-id="05cf3-109">100.00 OŘ</span><span class="sxs-lookup"><span data-stu-id="05cf3-109">100.00 DR</span></span> |
| <span data-ttu-id="05cf3-110">6100 – NY – OU\_249</span><span class="sxs-lookup"><span data-stu-id="05cf3-110">6100 – NY – OU\_249</span></span>  | <span data-ttu-id="05cf3-111">100.00 OŘ</span><span class="sxs-lookup"><span data-stu-id="05cf3-111">100.00 DR</span></span> |
| <span data-ttu-id="05cf3-112">2100 – MSP – OU\_256</span><span class="sxs-lookup"><span data-stu-id="05cf3-112">2100 – MSP – OU\_256</span></span> | <span data-ttu-id="05cf3-113">200.00 CR</span><span class="sxs-lookup"><span data-stu-id="05cf3-113">200.00 CR</span></span> |

<span data-ttu-id="05cf3-114">V tomto případě dojde k určení následujících zůstatků:</span><span class="sxs-lookup"><span data-stu-id="05cf3-114">In this case, the following balances are determined:</span></span>

-   <span data-ttu-id="05cf3-115">Pro obchodní jednotku MSP = 100.00 CR</span><span class="sxs-lookup"><span data-stu-id="05cf3-115">For Business Unit MSP = 100.00 CR</span></span>
-   <span data-ttu-id="05cf3-116">Pro obchodní jednotku NY = 100.00 DR</span><span class="sxs-lookup"><span data-stu-id="05cf3-116">For Business Unit NY = 100.00 DR</span></span>

<span data-ttu-id="05cf3-117">Následující účetní položky jsou proto vytvořeny automaticky tak, aby vyrovnaly deník na úrovni hodnot finančních dimenzí.</span><span class="sxs-lookup"><span data-stu-id="05cf3-117">Therefore, the following accounting entries are created automatically to balance the  journal at the level of the financial dimension values.</span></span>

|                                   |           |
|-----------------------------------|-----------|
| <span data-ttu-id="05cf3-118">(Mezijednotkový debit) – MSP – OU\_256</span><span class="sxs-lookup"><span data-stu-id="05cf3-118">(Interunit Debit) – MSP – OU\_256</span></span> | <span data-ttu-id="05cf3-119">100.00 OŘ</span><span class="sxs-lookup"><span data-stu-id="05cf3-119">100.00 DR</span></span> |
| <span data-ttu-id="05cf3-120">(Interunit Credit) – NY – OU\_249</span><span class="sxs-lookup"><span data-stu-id="05cf3-120">(Interunit Credit) – NY – OU\_249</span></span> | <span data-ttu-id="05cf3-121">100.00 CR</span><span class="sxs-lookup"><span data-stu-id="05cf3-121">100.00 CR</span></span> |





