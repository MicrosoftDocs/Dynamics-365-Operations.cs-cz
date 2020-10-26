---
title: Zpracování a sledování zdrojových dat
description: Veškeré zpracování dat se provádí prostřednictvím úloh.
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6a23443c985ac681c8c31956ae5ea3e513337577
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/10/2020
ms.locfileid: "3977544"
---
# <a name="process-and-trace-source-data"></a><span data-ttu-id="51b37-103">Zpracování a sledování zdrojových dat</span><span class="sxs-lookup"><span data-stu-id="51b37-103">Process and trace source data</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="51b37-104">Veškeré zpracování dat se provádí prostřednictvím úloh.</span><span class="sxs-lookup"><span data-stu-id="51b37-104">All data processing is run by jobs.</span></span> <span data-ttu-id="51b37-105">Pro každou úlohu a zprostředkovatele data se vytvoří deník pro dokumentaci spuštěného procesu a položek, které byly zpracovány v aktuální úloze.</span><span class="sxs-lookup"><span data-stu-id="51b37-105">For each job and data provider, a journal is created to document that the process has been run, and that the entries were processed in the current job.</span></span> <span data-ttu-id="51b37-106">Tento postup slouží k nastavení zdroje dat a následnému sledování původu specifických cenových záznamů.</span><span class="sxs-lookup"><span data-stu-id="51b37-106">Use this procedure to set up a data source and then  trace the origin of a specific cost entry.</span></span> <span data-ttu-id="51b37-107">Tento záznam používá v ukázkových datech společnost USP2.</span><span class="sxs-lookup"><span data-stu-id="51b37-107">This recording uses the USP2 demo data company USP2.</span></span> <span data-ttu-id="51b37-108">Před dokončením tohoto úkolu se nezapomeňte podívat na průvodce Tvorba hlavní knihy nákladového účetnictví, Definování jednotek řízení nákladů a Správa zdroje dat pro hlavní knihu nákladového účetnictví.</span><span class="sxs-lookup"><span data-stu-id="51b37-108">Before you complete this task, make sure that you play the following task guides: "Create a cost accounting ledger," "Define cost control units," and "Manage data source for the cost accounting ledger."</span></span>

1. <span data-ttu-id="51b37-109">Přejděte na Nákladové účetnictví > Nastavení hlavní knihy > Hlavní knihy nákladového účetnictví.</span><span class="sxs-lookup"><span data-stu-id="51b37-109">Go to Cost accounting > Ledger setup > Cost accounting ledgers.</span></span>
2. <span data-ttu-id="51b37-110">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="51b37-110">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="51b37-111">Vyberte hlavní knihu nákladového účetnictví, kterou jste předtím vytvořili.</span><span class="sxs-lookup"><span data-stu-id="51b37-111">Select the cost accounting ledger that you created earlier.</span></span>  
3. <span data-ttu-id="51b37-112">Klikněte na Skutečné verze.</span><span class="sxs-lookup"><span data-stu-id="51b37-112">Click Actual versions.</span></span>
4. <span data-ttu-id="51b37-113">V podokně akcí klepněte na možnost Zpracování zdroje dat.</span><span class="sxs-lookup"><span data-stu-id="51b37-113">On the Action Pane, click Source data processing.</span></span>
5. <span data-ttu-id="51b37-114">Klikněte na Deníky převodů položek hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="51b37-114">Click General ledger entry transfer journals.</span></span>
6. <span data-ttu-id="51b37-115">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="51b37-115">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="51b37-116">Klikněte na Položky deníku.</span><span class="sxs-lookup"><span data-stu-id="51b37-116">Click Journal entries.</span></span>
8. <span data-ttu-id="51b37-117">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="51b37-117">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="51b37-118">Klepněte na Položky nákladů.</span><span class="sxs-lookup"><span data-stu-id="51b37-118">Click Cost entries.</span></span>
10. <span data-ttu-id="51b37-119">Klikněte na Zdrojová položka.</span><span class="sxs-lookup"><span data-stu-id="51b37-119">Click Source entry.</span></span>
11. <span data-ttu-id="51b37-120">V podokně akcí klepněte na možnost Zpracování zdroje dat.</span><span class="sxs-lookup"><span data-stu-id="51b37-120">On the Action Pane, click Source data processing.</span></span>
12. <span data-ttu-id="51b37-121">Klikněte na Nastavení hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="51b37-121">Click General ledger.</span></span>
13. <span data-ttu-id="51b37-122">V poli Období fiskálního kalendáře zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="51b37-122">In the Fiscal calendar period field, enter or select a value.</span></span>
    * <span data-ttu-id="51b37-123">V tomto příkladu vyberte Fiskální období 9/2017.</span><span class="sxs-lookup"><span data-stu-id="51b37-123">For this example, select Fiscal 2017 Period 9.</span></span>  
14. <span data-ttu-id="51b37-124">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="51b37-124">Click OK.</span></span>

