---
title: Vytvoření účetních struktur
description: Tento průvodce úkoly vás provede vytvořením účetní struktury.
author: aprilolson
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionConfigureAccountStructure, DimensionCreateAccountStructure, DimensionHierarchyAddLevel, DimensionHierarchyConstraintActivate
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8b100d5da6ec26dc386c0c6cb0793245531eb0d8
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916223"
---
# <a name="create-account-structures"></a><span data-ttu-id="0c189-103">Vytvoření účetních struktur</span><span class="sxs-lookup"><span data-stu-id="0c189-103">Create account structures</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0c189-104">Tento průvodce úkoly vás provede vytvořením účetní struktury.</span><span class="sxs-lookup"><span data-stu-id="0c189-104">This task guide steps through creating an account structure.</span></span> <span data-ttu-id="0c189-105">Kroky používají ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="0c189-105">The steps use demo data company USMF.</span></span>

1. <span data-ttu-id="0c189-106">Přejděte na **navigační podokno > Moduly > Hlavní kniha > Účetní osnovy > Struktury > Konfigurovat účetní struktury**.</span><span class="sxs-lookup"><span data-stu-id="0c189-106">Go to **Navigation pane > Modules > General ledger > Chart of accounts > Structures > Configure account structures**.</span></span>
2. <span data-ttu-id="0c189-107">V **podokně akcí** klikněte na **Nové** a otevřete rozbalovací dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="0c189-107">On the **Action pane**, click **New** to open the drop dialog.</span></span>
3. <span data-ttu-id="0c189-108">Do pole **Účetní struktura** zadejte název popisující účel účetní struktury.</span><span class="sxs-lookup"><span data-stu-id="0c189-108">In the **Account structure** field, type a name to describe the purpose of the account structure.</span></span>
4. <span data-ttu-id="0c189-109">Do pole **Popis** zadejte popis specifikující účel účetní struktury.</span><span class="sxs-lookup"><span data-stu-id="0c189-109">In the **Description** field, type a description to specify the purpose of the account structure.</span></span>
5. <span data-ttu-id="0c189-110">Klepněte na volbu **Nový**.</span><span class="sxs-lookup"><span data-stu-id="0c189-110">Click **Create**.</span></span>
6. <span data-ttu-id="0c189-111">V části **Segmenty a povolené hodnoty** klikněte na **Přidat segment**.</span><span class="sxs-lookup"><span data-stu-id="0c189-111">In the **Segments and allowed values**, click **Add segment**.</span></span>
7. <span data-ttu-id="0c189-112">V seznamu dimenzí vyberte dimenzi k přidání do účetní struktury.</span><span class="sxs-lookup"><span data-stu-id="0c189-112">In the dimensions list, select the dimension to add to the account structure.</span></span>
8. <span data-ttu-id="0c189-113">Na konci seznamu klikněte na možnost **Přidat segment**.</span><span class="sxs-lookup"><span data-stu-id="0c189-113">At the end of the list, click **Add segment**.</span></span>
9. <span data-ttu-id="0c189-114">Podle potřeby zopakujte kroky 6 až 9.</span><span class="sxs-lookup"><span data-stu-id="0c189-114">Repeat step 6 to 9 as needed.</span></span>
10. <span data-ttu-id="0c189-115">V části **Podrobnosti povolené hodnoty** vyberte segment k úpravě povolených hodnot.</span><span class="sxs-lookup"><span data-stu-id="0c189-115">In the **Allowed value details** section, select the segment to edit the allowed values.</span></span>
    <span data-ttu-id="0c189-116">Klikněte například na pole **Hlavní účet**.</span><span class="sxs-lookup"><span data-stu-id="0c189-116">For example, click the **Main Account** field.</span></span>  
11. <span data-ttu-id="0c189-117">V poli **Operátor** vyberte možnost, jako je „mezi“ a „zahrnuje“.</span><span class="sxs-lookup"><span data-stu-id="0c189-117">In the **Operator** field, select an option, such as is between and includes.</span></span>
12. <span data-ttu-id="0c189-118">Zadejte hodnotu do pole **Hodnota**.</span><span class="sxs-lookup"><span data-stu-id="0c189-118">In the **Value** field, type a value.</span></span> <span data-ttu-id="0c189-119">Například 600 000.</span><span class="sxs-lookup"><span data-stu-id="0c189-119">For example, 600000.</span></span>  
13. <span data-ttu-id="0c189-120">Zadejte hodnotu do pole **prostřednictvím**.</span><span class="sxs-lookup"><span data-stu-id="0c189-120">In the **through** field, type a value.</span></span> <span data-ttu-id="0c189-121">Například 699 999.</span><span class="sxs-lookup"><span data-stu-id="0c189-121">For example, 699999.</span></span>  
14. <span data-ttu-id="0c189-122">V části **Podrobnosti povolené hodnoty** klikněte na **Použít**.</span><span class="sxs-lookup"><span data-stu-id="0c189-122">In the **Allowed value details** section, click **Apply**.</span></span>
15. <span data-ttu-id="0c189-123">Podle potřeby zopakujte kroky 10 až 15.</span><span class="sxs-lookup"><span data-stu-id="0c189-123">Repeat step 10 to 15 as needed.</span></span>  
16. <span data-ttu-id="0c189-124">V části **Podrobnosti povolené hodnoty** klikněte na **Přidat nová kritéria**.</span><span class="sxs-lookup"><span data-stu-id="0c189-124">In the **Allowed value details** section, click **Add new criteria**.</span></span>
17. <span data-ttu-id="0c189-125">V poli Operátor vyberte možnost, jako je „mezi“ a „zahrnuje“.</span><span class="sxs-lookup"><span data-stu-id="0c189-125">In the Operator field, select an option, such as is between and includes.</span></span>
18. <span data-ttu-id="0c189-126">Zadejte hodnotu do pole **Hodnota**.</span><span class="sxs-lookup"><span data-stu-id="0c189-126">In the **Value** field, type a value.</span></span> <span data-ttu-id="0c189-127">Například 033.</span><span class="sxs-lookup"><span data-stu-id="0c189-127">For example, 033.</span></span>  
19. <span data-ttu-id="0c189-128">Zadejte hodnotu do pole **prostřednictvím**.</span><span class="sxs-lookup"><span data-stu-id="0c189-128">In the **through** field, type a value.</span></span> <span data-ttu-id="0c189-129">Například 034.</span><span class="sxs-lookup"><span data-stu-id="0c189-129">For example, 034.</span></span>  
20. <span data-ttu-id="0c189-130">Klikněte na **Použít**.</span><span class="sxs-lookup"><span data-stu-id="0c189-130">Click **Apply**.</span></span>
21. <span data-ttu-id="0c189-131">V mřížce vyberte segment k úpravě povolených hodnot.</span><span class="sxs-lookup"><span data-stu-id="0c189-131">In the grid, select the segment to edit the allowed values.</span></span> <span data-ttu-id="0c189-132">Například Nákladové středisko.</span><span class="sxs-lookup"><span data-stu-id="0c189-132">For example, Cost Center.</span></span>  
22. <span data-ttu-id="0c189-133">Zadejte hodnotu do pole **Nákladové středisko**.</span><span class="sxs-lookup"><span data-stu-id="0c189-133">In the **CostCenter field**, type a value.</span></span> <span data-ttu-id="0c189-134">Například 007…021.</span><span class="sxs-lookup"><span data-stu-id="0c189-134">For example, 007..021.</span></span>  
23. <span data-ttu-id="0c189-135">V části **Segmenty a povolené hodnoty** klikněte na **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="0c189-135">In the **Segments and allowed values**, click **Add**.</span></span>
24. <span data-ttu-id="0c189-136">Zadejte hodnotu do pole **Hlavní účet**.</span><span class="sxs-lookup"><span data-stu-id="0c189-136">In the **MainAccount** field, type a value.</span></span> <span data-ttu-id="0c189-137">Například 600 000…699 999.</span><span class="sxs-lookup"><span data-stu-id="0c189-137">For example, 600000..699999</span></span>  
25. <span data-ttu-id="0c189-138">V mřížce vyberte segment k úpravě povolených hodnot.</span><span class="sxs-lookup"><span data-stu-id="0c189-138">In the grid, select the segment to edit the allowed values.</span></span> <span data-ttu-id="0c189-139">Například Oddělení.</span><span class="sxs-lookup"><span data-stu-id="0c189-139">For example, Department.</span></span>  
26. <span data-ttu-id="0c189-140">Zadejte hodnotu do pole Oddělení.</span><span class="sxs-lookup"><span data-stu-id="0c189-140">In the Department field, type a value.</span></span> <span data-ttu-id="0c189-141">Například 032.</span><span class="sxs-lookup"><span data-stu-id="0c189-141">For example, 032.</span></span>  
27. <span data-ttu-id="0c189-142">Zadejte hodnotu do pole Nákladové středisko.</span><span class="sxs-lookup"><span data-stu-id="0c189-142">In the CostCenter field, type a value.</span></span> <span data-ttu-id="0c189-143">Například 086.</span><span class="sxs-lookup"><span data-stu-id="0c189-143">For example, 086.</span></span>  
28. <span data-ttu-id="0c189-144">V **podokně akcí** klikněte na možnost **Ověřit**.</span><span class="sxs-lookup"><span data-stu-id="0c189-144">On the **Action pane**, click **Validate**.</span></span>
29. <span data-ttu-id="0c189-145">V **podokně akcí** klikněte na možnost **Aktivovat**.</span><span class="sxs-lookup"><span data-stu-id="0c189-145">On the **Action pane**, click **Activate**.</span></span>
30. <span data-ttu-id="0c189-146">Klepněte na tlačítko **Aktivovat**.</span><span class="sxs-lookup"><span data-stu-id="0c189-146">Click **Activate**.</span></span>

