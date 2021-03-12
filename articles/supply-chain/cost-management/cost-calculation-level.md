---
title: Úroveň výpočtu nákladů
description: Tohle téma popisuje úroveň kusovníku, která se nazývá Úroveň výpočtu nákladů. Tato úroveň kusovníku vylučuje výrobní a dávkové objednávky ze svých výpočtů.
author: AndersGirke
manager: tfehr
ms.date: 04/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-04-23
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: 42088d8c005cf3fc04e768f1b8e8c8ca0b8c6993
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4967715"
---
# <a name="cost-calculation-level"></a><span data-ttu-id="5ebcb-104">Úroveň výpočtu nákladů</span><span class="sxs-lookup"><span data-stu-id="5ebcb-104">Cost calculation level</span></span>

<span data-ttu-id="5ebcb-105">Úroveň kusovníku pojmenovaná jako **Úroveň výpočtu nákladů** vyloučí z výpočtů výrobní a dávkové objednávky.</span><span class="sxs-lookup"><span data-stu-id="5ebcb-105">The bill of materials (BOM) level that is named **Cost calculation level** excludes production orders and batch orders from its calculations.</span></span> <span data-ttu-id="5ebcb-106">Systém používá tuto úroveň, když provádí výpočty nákladů ve verzích výpočtů nákladů.</span><span class="sxs-lookup"><span data-stu-id="5ebcb-106">The system uses this level when it runs cost calculations in costing versions.</span></span> <span data-ttu-id="5ebcb-107">V procesech, jako je přepočet a uzavření zásob, systém místo toho používá úroveň kusovníku **Úroveň stanovení nákladů**.</span><span class="sxs-lookup"><span data-stu-id="5ebcb-107">In processes such as recalculation and inventory close, the system uses the **Costing level** BOM level instead.</span></span>

<span data-ttu-id="5ebcb-108">Následující jednoduchý scénář ukazuje rozdíly mezi úrovněmi kusovníku **Úroveň výpočtu nákladů** a **Úroveň stanovení nákladů**.</span><span class="sxs-lookup"><span data-stu-id="5ebcb-108">The following simple scenario shows the differences between the **Cost calculation level** BOM level and the **Costing level** BOM level.</span></span>

<span data-ttu-id="5ebcb-109">Máte tři produkty: A, B a C. Produkt C je součástí produktu B a produkt B je součástí produktu A.</span><span class="sxs-lookup"><span data-stu-id="5ebcb-109">You have three products: A, B, and C. Product C is the component of product B, and product B is the component of product A.</span></span>

- <span data-ttu-id="5ebcb-110">**Úroveň stanovení nákladů** přiřazuje následující úrovně kusovníku:</span><span class="sxs-lookup"><span data-stu-id="5ebcb-110">**Costing level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="5ebcb-111">**Produkt A:** 0</span><span class="sxs-lookup"><span data-stu-id="5ebcb-111">**Product A:** 0</span></span>
    - <span data-ttu-id="5ebcb-112">**Produkt B:** 1</span><span class="sxs-lookup"><span data-stu-id="5ebcb-112">**Product B:** 1</span></span>
    - <span data-ttu-id="5ebcb-113">**Produkt C:** 2</span><span class="sxs-lookup"><span data-stu-id="5ebcb-113">**Product C:** 2</span></span>

- <span data-ttu-id="5ebcb-114">**Úroveň výpočtu nákladů** přiřazuje následující úrovně kusovníku:</span><span class="sxs-lookup"><span data-stu-id="5ebcb-114">**Cost calculation level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="5ebcb-115">**Produkt A:** 0</span><span class="sxs-lookup"><span data-stu-id="5ebcb-115">**Product A:** 0</span></span>
    - <span data-ttu-id="5ebcb-116">**Produkt B:** 1</span><span class="sxs-lookup"><span data-stu-id="5ebcb-116">**Product B:** 1</span></span>
    - <span data-ttu-id="5ebcb-117">**Produkt C:** 2</span><span class="sxs-lookup"><span data-stu-id="5ebcb-117">**Product C:** 2</span></span>

<span data-ttu-id="5ebcb-118">Poté se vytvoří výrobní objednávka pro produkt C a produkt A se přidá do kusovníku výrobní zakázky.</span><span class="sxs-lookup"><span data-stu-id="5ebcb-118">A production order for product C is then created, and product A is added to the production order BOM.</span></span> <span data-ttu-id="5ebcb-119">Po odhadu objednávky jsou úrovně kusovníku aktualizovány následujícím způsobem:</span><span class="sxs-lookup"><span data-stu-id="5ebcb-119">After the order is estimated, BOM levels are updated in the following way:</span></span>

- <span data-ttu-id="5ebcb-120">**Úroveň stanovení nákladů** přiřazuje následující úrovně kusovníku:</span><span class="sxs-lookup"><span data-stu-id="5ebcb-120">**Costing level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="5ebcb-121">**Produkt B:** 1</span><span class="sxs-lookup"><span data-stu-id="5ebcb-121">**Product B:** 1</span></span>
    - <span data-ttu-id="5ebcb-122">**Produkt C:** 2</span><span class="sxs-lookup"><span data-stu-id="5ebcb-122">**Product C:** 2</span></span>
    - <span data-ttu-id="5ebcb-123">**Produkt A:** 3</span><span class="sxs-lookup"><span data-stu-id="5ebcb-123">**Product A:** 3</span></span>

- <span data-ttu-id="5ebcb-124">**Úroveň výpočtu nákladů** přiřazuje následující úrovně kusovníku:</span><span class="sxs-lookup"><span data-stu-id="5ebcb-124">**Cost calculation level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="5ebcb-125">**Produkt A:** 0</span><span class="sxs-lookup"><span data-stu-id="5ebcb-125">**Product A:** 0</span></span>
    - <span data-ttu-id="5ebcb-126">**Produkt B:** 1</span><span class="sxs-lookup"><span data-stu-id="5ebcb-126">**Product B:** 1</span></span>
    - <span data-ttu-id="5ebcb-127">**Produkt C:** 2</span><span class="sxs-lookup"><span data-stu-id="5ebcb-127">**Product C:** 2</span></span>

<span data-ttu-id="5ebcb-128">Toto chování zajišťuje, že změny v kusovnících výrobní zakázky neovlivní následné výpočty nákladů.</span><span class="sxs-lookup"><span data-stu-id="5ebcb-128">This behavior ensures that changes to production order BOMs don't affect subsequent cost calculations.</span></span>
