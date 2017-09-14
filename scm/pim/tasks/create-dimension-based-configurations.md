--- 
title: "Vytváření konfigurací založených na dimenzích"
description: "Tento postup popisuje, jak definovat konfiguraci produktu založeného na dimenzích."
author: YuyuScheller
manager: AnnBe
ms.date: 06/21/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 6dd2aa1ebc713287120106a9d1ec7dc15c24def9
ms.openlocfilehash: d6ea85cedbb96266f82e0a4ec1ad17f3ba829322
ms.contentlocale: cs-cz
ms.lasthandoff: 09/14/2017

---
# <a name="create-dimension-based-configurations"></a><span data-ttu-id="02ec1-103">Vytváření konfigurací založených na dimenzích</span><span class="sxs-lookup"><span data-stu-id="02ec1-103">Create dimension-based configurations</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="02ec1-104">Tento postup popisuje, jak definovat konfiguraci produktu založeného na dimenzích.</span><span class="sxs-lookup"><span data-stu-id="02ec1-104">This procedure shows how to define a configuration for a dimension-based product.</span></span> <span data-ttu-id="02ec1-105">Jedná se o poslední postup v sérii, který vysvětluje vytvoření kombinací konfigurace založené na dimenzích.</span><span class="sxs-lookup"><span data-stu-id="02ec1-105">This is the last procedure in the series that explains how to build combinations for dimension-based configuration.</span></span> <span data-ttu-id="02ec1-106">Spuštění tohoto postupu je závislé na datu vytvořeném v předchozích sedmi záznamech.</span><span class="sxs-lookup"><span data-stu-id="02ec1-106">The execution of this procedure is dependent on the data created in the previous seven recordings.</span></span> <span data-ttu-id="02ec1-107">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="02ec1-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="find-the-dimension-based-product-master"></a><span data-ttu-id="02ec1-108">Vyhledání hlavního produktu založeného na dimenzích</span><span class="sxs-lookup"><span data-stu-id="02ec1-108">Find the dimension-based product master</span></span>
1. <span data-ttu-id="02ec1-109">Klikněte na možnost Údržba uvolněného produktu.</span><span class="sxs-lookup"><span data-stu-id="02ec1-109">Click Released product maintenance.</span></span>
2. <span data-ttu-id="02ec1-110">Klepněte na možnost Uvolněné produkty.</span><span class="sxs-lookup"><span data-stu-id="02ec1-110">Click Released products.</span></span>
3. <span data-ttu-id="02ec1-111">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="02ec1-111">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="02ec1-112">Vyberte základní produkt založený na dimenzích, který jste vytvořili v prvním záznamu v tomto pořadí 8 záznamů.</span><span class="sxs-lookup"><span data-stu-id="02ec1-112">Select the dimension-based product master that you created in the first recording in this sequence of 8 recordings.</span></span>  

## <a name="create-configurations"></a><span data-ttu-id="02ec1-113">Vytvoření konfigurací</span><span class="sxs-lookup"><span data-stu-id="02ec1-113">Create configurations</span></span>
1. <span data-ttu-id="02ec1-114">V podokně akcí Analýza klikněte na položku Udržovat konfigurace.</span><span class="sxs-lookup"><span data-stu-id="02ec1-114">On the Engineering Action Pane, click Maintain configurations.</span></span>
2. <span data-ttu-id="02ec1-115">Klikněte na Konfigurovat.</span><span class="sxs-lookup"><span data-stu-id="02ec1-115">Click Configure.</span></span>
3. <span data-ttu-id="02ec1-116">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="02ec1-116">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="02ec1-117">V poli Číslo zboží zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="02ec1-117">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="02ec1-118">Vyberte některou z položek v první konfigurační skupině.</span><span class="sxs-lookup"><span data-stu-id="02ec1-118">Select any of the items in the first configuration group.</span></span>  
5. <span data-ttu-id="02ec1-119">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="02ec1-119">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="02ec1-120">V poli Číslo zboží zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="02ec1-120">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="02ec1-121">Vyberte některou z položek ve druhé konfigurační skupině.</span><span class="sxs-lookup"><span data-stu-id="02ec1-121">Select any item from the second configuration group.</span></span>  
7. <span data-ttu-id="02ec1-122">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="02ec1-122">Click OK.</span></span>
8. <span data-ttu-id="02ec1-123">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="02ec1-123">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="02ec1-124">Zadejte hodnotu do pole Konfigurace.</span><span class="sxs-lookup"><span data-stu-id="02ec1-124">In the Configuration field, type a value.</span></span>
    * <span data-ttu-id="02ec1-125">Zadejte název konfigurace, který vám usnadní identifikaci konfigurace.</span><span class="sxs-lookup"><span data-stu-id="02ec1-125">Enter a configuration name that will make it easy to identify the configuration.</span></span>  
10. <span data-ttu-id="02ec1-126">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="02ec1-126">In the Description field, type a value.</span></span>
    * <span data-ttu-id="02ec1-127">Zadejte popis konfigurace vysvětlující její obsahuj.</span><span class="sxs-lookup"><span data-stu-id="02ec1-127">Enter a description of the configuration to explain what it contains.</span></span>  
11. <span data-ttu-id="02ec1-128">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="02ec1-128">Click OK.</span></span>


