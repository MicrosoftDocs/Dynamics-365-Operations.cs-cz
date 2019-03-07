---
title: Vytvoření účetních struktur
description: Tento průvodce úkoly vás provede vytvořením účetní struktury.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionConfigureAccountStructure, DimensionCreateAccountStructure, DimensionHierarchyAddLevel, DimensionHierarchyConstraintActivate
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a7dd71cc072d49f47b1d77d3a688984cd4aaa624
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "356385"
---
# <a name="create-account-structures"></a><span data-ttu-id="802ca-103">Vytvoření účetních struktur</span><span class="sxs-lookup"><span data-stu-id="802ca-103">Create account structures</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="802ca-104">Tento průvodce úkoly vás provede vytvořením účetní struktury.</span><span class="sxs-lookup"><span data-stu-id="802ca-104">This task guide steps through creating an account structure.</span></span> <span data-ttu-id="802ca-105">Kroky používají ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="802ca-105">The steps use demo data company USMF.</span></span>

1. <span data-ttu-id="802ca-106">Přejděte do části Hlavní kniha > Účtová osnova > Struktury > Konfigurovat účetní struktury.</span><span class="sxs-lookup"><span data-stu-id="802ca-106">Go to General ledger > Chart of accounts > Structures > Configure account structures.</span></span>
2. <span data-ttu-id="802ca-107">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="802ca-107">Click New to open the drop dialog.</span></span>
3. <span data-ttu-id="802ca-108">Do pole Účetní struktura zadejte název popisující účel účetní struktury.</span><span class="sxs-lookup"><span data-stu-id="802ca-108">In the Account structure field, type a name to describe the purpose of the account structure.</span></span>
4. <span data-ttu-id="802ca-109">Do pole Popis zadejte popis specifikující účel účetní struktury.</span><span class="sxs-lookup"><span data-stu-id="802ca-109">In the Description field, type a description to specify the purpose of the account structure.</span></span>
5. <span data-ttu-id="802ca-110">Klepněte na volbu Nový.</span><span class="sxs-lookup"><span data-stu-id="802ca-110">Click Create.</span></span>
6. <span data-ttu-id="802ca-111">Klepněte na Přidat segment.</span><span class="sxs-lookup"><span data-stu-id="802ca-111">Click Add segment.</span></span>
7. <span data-ttu-id="802ca-112">V seznamu dimenzí vyberte dimenzi k přidání do účetní struktury.</span><span class="sxs-lookup"><span data-stu-id="802ca-112">In the Dimensions list, select the dimension to add to the account structure.</span></span>
8. <span data-ttu-id="802ca-113">Klepněte na Přidat segment.</span><span class="sxs-lookup"><span data-stu-id="802ca-113">Click Add segment.</span></span>
9. <span data-ttu-id="802ca-114">Klepněte na Přidat segment.</span><span class="sxs-lookup"><span data-stu-id="802ca-114">Click Add segment.</span></span>
10. <span data-ttu-id="802ca-115">V seznamu dimenzí vyberte dimenzi k přidání do účetní struktury.</span><span class="sxs-lookup"><span data-stu-id="802ca-115">In the Dimensions list, select the dimension to add to the account structure.</span></span>
11. <span data-ttu-id="802ca-116">Klepněte na Přidat segment.</span><span class="sxs-lookup"><span data-stu-id="802ca-116">Click Add segment.</span></span>
12. <span data-ttu-id="802ca-117">Klepněte na Přidat segment.</span><span class="sxs-lookup"><span data-stu-id="802ca-117">Click Add segment.</span></span>
13. <span data-ttu-id="802ca-118">V seznamu dimenzí vyberte dimenzi k přidání do účetní struktury.</span><span class="sxs-lookup"><span data-stu-id="802ca-118">In the Dimensions list, select the dimension to add to the account structure.</span></span>
14. <span data-ttu-id="802ca-119">Klepněte na Přidat segment.</span><span class="sxs-lookup"><span data-stu-id="802ca-119">Click Add segment.</span></span>
15. <span data-ttu-id="802ca-120">V mřížce vyberte segment k úpravě povolených hodnot.</span><span class="sxs-lookup"><span data-stu-id="802ca-120">In the grid, select the segment to edit the allowed values.</span></span>
    * <span data-ttu-id="802ca-121">Klepněte například na položku v hlavním účtu.</span><span class="sxs-lookup"><span data-stu-id="802ca-121">For example, click in Main Account.</span></span>  
16. <span data-ttu-id="802ca-122">V poli Operátor vyberte možnost, jako je „mezi“ a „zahrnuje“.</span><span class="sxs-lookup"><span data-stu-id="802ca-122">In the Operator field, select an option, such as is between and includes.</span></span>
17. <span data-ttu-id="802ca-123">Zadejte hodnotu do pole Hodnota.</span><span class="sxs-lookup"><span data-stu-id="802ca-123">In the Value field, type a value.</span></span>
    * <span data-ttu-id="802ca-124">Například 600 000.</span><span class="sxs-lookup"><span data-stu-id="802ca-124">For example, 600000.</span></span>  
18. <span data-ttu-id="802ca-125">Zadejte hodnotu do pole „prostřednictvím“.</span><span class="sxs-lookup"><span data-stu-id="802ca-125">In the through field, type a value.</span></span>
    * <span data-ttu-id="802ca-126">Například 699 999.</span><span class="sxs-lookup"><span data-stu-id="802ca-126">For example, 699999.</span></span>  
19. <span data-ttu-id="802ca-127">Klepněte na možnost Použít.</span><span class="sxs-lookup"><span data-stu-id="802ca-127">Click Apply.</span></span>
20. <span data-ttu-id="802ca-128">V mřížce vyberte segment k úpravě povolených hodnot.</span><span class="sxs-lookup"><span data-stu-id="802ca-128">In the grid, select the segment to edit the allowed values.</span></span>
    * <span data-ttu-id="802ca-129">Například Oddělení.</span><span class="sxs-lookup"><span data-stu-id="802ca-129">For example, Department.</span></span>  
21. <span data-ttu-id="802ca-130">V poli Operátor vyberte možnost, jako je „mezi“ a „zahrnuje“.</span><span class="sxs-lookup"><span data-stu-id="802ca-130">In the Operator field, select an option, such as is between and includes.</span></span>
22. <span data-ttu-id="802ca-131">Zadejte hodnotu do pole Hodnota.</span><span class="sxs-lookup"><span data-stu-id="802ca-131">In the Value field, type a value.</span></span>
    * <span data-ttu-id="802ca-132">Například 022.</span><span class="sxs-lookup"><span data-stu-id="802ca-132">For example, 022.</span></span>  
23. <span data-ttu-id="802ca-133">Zadejte hodnotu do pole „prostřednictvím“.</span><span class="sxs-lookup"><span data-stu-id="802ca-133">In the through field, type a value.</span></span>
    * <span data-ttu-id="802ca-134">Například 031.</span><span class="sxs-lookup"><span data-stu-id="802ca-134">For example, 031.</span></span>  
24. <span data-ttu-id="802ca-135">Klepněte na Přidat nová kritéria.</span><span class="sxs-lookup"><span data-stu-id="802ca-135">Click Add new criteria.</span></span>
25. <span data-ttu-id="802ca-136">V poli Operátor vyberte možnost, jako je „mezi“ a „zahrnuje“.</span><span class="sxs-lookup"><span data-stu-id="802ca-136">In the Operator field, select an option, such as is between and includes.</span></span>
26. <span data-ttu-id="802ca-137">Zadejte hodnotu do pole Hodnota.</span><span class="sxs-lookup"><span data-stu-id="802ca-137">In the Value field, type a value.</span></span>
    * <span data-ttu-id="802ca-138">Například 033.</span><span class="sxs-lookup"><span data-stu-id="802ca-138">For example, 033.</span></span>  
27. <span data-ttu-id="802ca-139">Zadejte hodnotu do pole „prostřednictvím“.</span><span class="sxs-lookup"><span data-stu-id="802ca-139">In the through field, type a value.</span></span>
    * <span data-ttu-id="802ca-140">Například 034.</span><span class="sxs-lookup"><span data-stu-id="802ca-140">For example, 034.</span></span>  
28. <span data-ttu-id="802ca-141">Klepněte na možnost Použít.</span><span class="sxs-lookup"><span data-stu-id="802ca-141">Click Apply.</span></span>
29. <span data-ttu-id="802ca-142">V mřížce vyberte segment k úpravě povolených hodnot.</span><span class="sxs-lookup"><span data-stu-id="802ca-142">In the grid, select the segment to edit the allowed values.</span></span>
    * <span data-ttu-id="802ca-143">Například Nákladové středisko.</span><span class="sxs-lookup"><span data-stu-id="802ca-143">For example, Cost Center.</span></span>  
30. <span data-ttu-id="802ca-144">Zadejte hodnotu do pole Nákladové středisko.</span><span class="sxs-lookup"><span data-stu-id="802ca-144">In the CostCenter field, type a value.</span></span>
    * <span data-ttu-id="802ca-145">Například 007…021.</span><span class="sxs-lookup"><span data-stu-id="802ca-145">For example, 007..021.</span></span>  
31. <span data-ttu-id="802ca-146">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="802ca-146">Click Add.</span></span>
32. <span data-ttu-id="802ca-147">Zadejte hodnotu do pole Hlavní účet.</span><span class="sxs-lookup"><span data-stu-id="802ca-147">In the MainAccount field, type a value.</span></span>
    * <span data-ttu-id="802ca-148">Například 600 000…699 999.</span><span class="sxs-lookup"><span data-stu-id="802ca-148">For example, 600000..699999</span></span>  
33. <span data-ttu-id="802ca-149">V mřížce vyberte segment k úpravě povolených hodnot.</span><span class="sxs-lookup"><span data-stu-id="802ca-149">In the grid, select the segment to edit the allowed values.</span></span>
    * <span data-ttu-id="802ca-150">Například Oddělení.</span><span class="sxs-lookup"><span data-stu-id="802ca-150">For example, Department.</span></span>  
34. <span data-ttu-id="802ca-151">Zadejte hodnotu do pole Oddělení.</span><span class="sxs-lookup"><span data-stu-id="802ca-151">In the Department field, type a value.</span></span>
    * <span data-ttu-id="802ca-152">Například 032.</span><span class="sxs-lookup"><span data-stu-id="802ca-152">For example, 032.</span></span>  
35. <span data-ttu-id="802ca-153">Zadejte hodnotu do pole Nákladové středisko.</span><span class="sxs-lookup"><span data-stu-id="802ca-153">In the CostCenter field, type a value.</span></span>
    * <span data-ttu-id="802ca-154">Například 086.</span><span class="sxs-lookup"><span data-stu-id="802ca-154">For example, 086.</span></span>  
36. <span data-ttu-id="802ca-155">Klikněte na tlačítko Ověřit.</span><span class="sxs-lookup"><span data-stu-id="802ca-155">Click Validate.</span></span>
37. <span data-ttu-id="802ca-156">Klepněte na tlačítko Aktivovat.</span><span class="sxs-lookup"><span data-stu-id="802ca-156">Click Activate.</span></span>
38. <span data-ttu-id="802ca-157">Klepněte na tlačítko Aktivovat.</span><span class="sxs-lookup"><span data-stu-id="802ca-157">Click Activate.</span></span>

