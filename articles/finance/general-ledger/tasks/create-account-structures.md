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
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ed8ce37ab642277ff843e6320a880fac40d41acb
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5235782"
---
# <a name="create-account-structures"></a><span data-ttu-id="851fe-103">Vytvoření účetních struktur</span><span class="sxs-lookup"><span data-stu-id="851fe-103">Create account structures</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="851fe-104">Tento průvodce úkoly vás provede vytvořením účetní struktury.</span><span class="sxs-lookup"><span data-stu-id="851fe-104">This task guide steps through creating an account structure.</span></span> <span data-ttu-id="851fe-105">Kroky používají ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="851fe-105">The steps use demo data company USMF.</span></span>

1. <span data-ttu-id="851fe-106">Přejděte na **navigační podokno > Moduly > Hlavní kniha > Účetní osnovy > Struktury > Konfigurovat účetní struktury**.</span><span class="sxs-lookup"><span data-stu-id="851fe-106">Go to **Navigation pane > Modules > General ledger > Chart of accounts > Structures > Configure account structures**.</span></span>
2. <span data-ttu-id="851fe-107">V **podokně akcí** klikněte na **Nové** a otevřete rozbalovací dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="851fe-107">On the **Action pane**, click **New** to open the drop dialog.</span></span>
3. <span data-ttu-id="851fe-108">Do pole **Účetní struktura** zadejte název popisující účel účetní struktury.</span><span class="sxs-lookup"><span data-stu-id="851fe-108">In the **Account structure** field, type a name to describe the purpose of the account structure.</span></span>
4. <span data-ttu-id="851fe-109">Do pole **Popis** zadejte popis specifikující účel účetní struktury.</span><span class="sxs-lookup"><span data-stu-id="851fe-109">In the **Description** field, type a description to specify the purpose of the account structure.</span></span>
5. <span data-ttu-id="851fe-110">Klepněte na volbu **Nový**.</span><span class="sxs-lookup"><span data-stu-id="851fe-110">Click **Create**.</span></span>
6. <span data-ttu-id="851fe-111">V části **Segmenty a povolené hodnoty** klikněte na **Přidat segment**.</span><span class="sxs-lookup"><span data-stu-id="851fe-111">In the **Segments and allowed values**, click **Add segment**.</span></span>
7. <span data-ttu-id="851fe-112">V seznamu dimenzí vyberte dimenzi k přidání do účetní struktury.</span><span class="sxs-lookup"><span data-stu-id="851fe-112">In the dimensions list, select the dimension to add to the account structure.</span></span>
8. <span data-ttu-id="851fe-113">Na konci seznamu klikněte na možnost **Přidat segment**.</span><span class="sxs-lookup"><span data-stu-id="851fe-113">At the end of the list, click **Add segment**.</span></span>
9. <span data-ttu-id="851fe-114">Podle potřeby zopakujte kroky 6 až 9.</span><span class="sxs-lookup"><span data-stu-id="851fe-114">Repeat step 6 to 9 as needed.</span></span>
10. <span data-ttu-id="851fe-115">V části **Podrobnosti povolené hodnoty** vyberte segment k úpravě povolených hodnot.</span><span class="sxs-lookup"><span data-stu-id="851fe-115">In the **Allowed value details** section, select the segment to edit the allowed values.</span></span>
    <span data-ttu-id="851fe-116">Klikněte například na pole **Hlavní účet**.</span><span class="sxs-lookup"><span data-stu-id="851fe-116">For example, click the **Main Account** field.</span></span>  
11. <span data-ttu-id="851fe-117">V poli **Operátor** vyberte možnost, jako je „mezi“ a „zahrnuje“.</span><span class="sxs-lookup"><span data-stu-id="851fe-117">In the **Operator** field, select an option, such as is between and includes.</span></span>
12. <span data-ttu-id="851fe-118">Zadejte hodnotu do pole **Hodnota**.</span><span class="sxs-lookup"><span data-stu-id="851fe-118">In the **Value** field, type a value.</span></span> <span data-ttu-id="851fe-119">Například 600 000.</span><span class="sxs-lookup"><span data-stu-id="851fe-119">For example, 600000.</span></span>  
13. <span data-ttu-id="851fe-120">Zadejte hodnotu do pole **prostřednictvím**.</span><span class="sxs-lookup"><span data-stu-id="851fe-120">In the **through** field, type a value.</span></span> <span data-ttu-id="851fe-121">Například 699 999.</span><span class="sxs-lookup"><span data-stu-id="851fe-121">For example, 699999.</span></span>  
14. <span data-ttu-id="851fe-122">V části **Podrobnosti povolené hodnoty** klikněte na **Použít**.</span><span class="sxs-lookup"><span data-stu-id="851fe-122">In the **Allowed value details** section, click **Apply**.</span></span>
15. <span data-ttu-id="851fe-123">Podle potřeby zopakujte kroky 10 až 15.</span><span class="sxs-lookup"><span data-stu-id="851fe-123">Repeat step 10 to 15 as needed.</span></span>  
16. <span data-ttu-id="851fe-124">V části **Podrobnosti povolené hodnoty** klikněte na **Přidat nová kritéria**.</span><span class="sxs-lookup"><span data-stu-id="851fe-124">In the **Allowed value details** section, click **Add new criteria**.</span></span>
17. <span data-ttu-id="851fe-125">V poli Operátor vyberte možnost, jako je „mezi“ a „zahrnuje“.</span><span class="sxs-lookup"><span data-stu-id="851fe-125">In the Operator field, select an option, such as is between and includes.</span></span>
18. <span data-ttu-id="851fe-126">Zadejte hodnotu do pole **Hodnota**.</span><span class="sxs-lookup"><span data-stu-id="851fe-126">In the **Value** field, type a value.</span></span> <span data-ttu-id="851fe-127">Například 033.</span><span class="sxs-lookup"><span data-stu-id="851fe-127">For example, 033.</span></span>  
19. <span data-ttu-id="851fe-128">Zadejte hodnotu do pole **prostřednictvím**.</span><span class="sxs-lookup"><span data-stu-id="851fe-128">In the **through** field, type a value.</span></span> <span data-ttu-id="851fe-129">Například 034.</span><span class="sxs-lookup"><span data-stu-id="851fe-129">For example, 034.</span></span>  
20. <span data-ttu-id="851fe-130">Klikněte na **Použít**.</span><span class="sxs-lookup"><span data-stu-id="851fe-130">Click **Apply**.</span></span>
21. <span data-ttu-id="851fe-131">V mřížce vyberte segment k úpravě povolených hodnot.</span><span class="sxs-lookup"><span data-stu-id="851fe-131">In the grid, select the segment to edit the allowed values.</span></span> <span data-ttu-id="851fe-132">Například Nákladové středisko.</span><span class="sxs-lookup"><span data-stu-id="851fe-132">For example, Cost Center.</span></span>  
22. <span data-ttu-id="851fe-133">Zadejte hodnotu do pole **Nákladové středisko**.</span><span class="sxs-lookup"><span data-stu-id="851fe-133">In the **CostCenter field**, type a value.</span></span> <span data-ttu-id="851fe-134">Například 007…021.</span><span class="sxs-lookup"><span data-stu-id="851fe-134">For example, 007..021.</span></span>  
23. <span data-ttu-id="851fe-135">V části **Segmenty a povolené hodnoty** klikněte na **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="851fe-135">In the **Segments and allowed values**, click **Add**.</span></span>
24. <span data-ttu-id="851fe-136">Zadejte hodnotu do pole **Hlavní účet**.</span><span class="sxs-lookup"><span data-stu-id="851fe-136">In the **MainAccount** field, type a value.</span></span> <span data-ttu-id="851fe-137">Například 600 000…699 999.</span><span class="sxs-lookup"><span data-stu-id="851fe-137">For example, 600000..699999</span></span>  
25. <span data-ttu-id="851fe-138">V mřížce vyberte segment k úpravě povolených hodnot.</span><span class="sxs-lookup"><span data-stu-id="851fe-138">In the grid, select the segment to edit the allowed values.</span></span> <span data-ttu-id="851fe-139">Například Oddělení.</span><span class="sxs-lookup"><span data-stu-id="851fe-139">For example, Department.</span></span>  
26. <span data-ttu-id="851fe-140">Zadejte hodnotu do pole Oddělení.</span><span class="sxs-lookup"><span data-stu-id="851fe-140">In the Department field, type a value.</span></span> <span data-ttu-id="851fe-141">Například 032.</span><span class="sxs-lookup"><span data-stu-id="851fe-141">For example, 032.</span></span>  
27. <span data-ttu-id="851fe-142">Zadejte hodnotu do pole Nákladové středisko.</span><span class="sxs-lookup"><span data-stu-id="851fe-142">In the CostCenter field, type a value.</span></span> <span data-ttu-id="851fe-143">Například 086.</span><span class="sxs-lookup"><span data-stu-id="851fe-143">For example, 086.</span></span>  
28. <span data-ttu-id="851fe-144">V **podokně akcí** klikněte na možnost **Ověřit**.</span><span class="sxs-lookup"><span data-stu-id="851fe-144">On the **Action pane**, click **Validate**.</span></span>
29. <span data-ttu-id="851fe-145">V **podokně akcí** klikněte na možnost **Aktivovat**.</span><span class="sxs-lookup"><span data-stu-id="851fe-145">On the **Action pane**, click **Activate**.</span></span>
30. <span data-ttu-id="851fe-146">Klepněte na tlačítko **Aktivovat**.</span><span class="sxs-lookup"><span data-stu-id="851fe-146">Click **Activate**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]