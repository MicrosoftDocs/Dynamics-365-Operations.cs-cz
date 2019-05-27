---
title: Vytvoření organizační hierarchie vykazování
description: Pomocí tohoto postupu vytvořte hierarchii sestavy pro vykazování v organizaci.
author: ShylaThompson
manager: AnnBe
ms.date: 10/30/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d9a06a67f851e4a73df90f999683d5ea27f38e66
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1543926"
---
# <a name="create-an-organization-report-hierarchy"></a><span data-ttu-id="b6eea-103">Vytvoření organizační hierarchie vykazování</span><span class="sxs-lookup"><span data-stu-id="b6eea-103">Create an organization report hierarchy</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b6eea-104">Pomocí tohoto postupu vytvořte hierarchii sestavy pro vykazování v organizaci.</span><span class="sxs-lookup"><span data-stu-id="b6eea-104">Use this procedure to create a report hierarchy for organization reporting.</span></span> <span data-ttu-id="b6eea-105">Účelem tohoto záznamu je provést vás hierarchií dimenze, abyste mohli pokračovat až do vytvoření struktury vykazování v celé organizaci.</span><span class="sxs-lookup"><span data-stu-id="b6eea-105">The purpose of this recording is to guide you through the dimension hierarchy so that you can continue until the whole organization reporting structure is created.</span></span> <span data-ttu-id="b6eea-106">Tento záznam používá v ukázkových datech společnost USP2.</span><span class="sxs-lookup"><span data-stu-id="b6eea-106">This recording uses the USP2 demo data company.</span></span>

1. <span data-ttu-id="b6eea-107">Přejděte na Nákladové účetnictví > Dimenze > Hierarchie dimenzí.</span><span class="sxs-lookup"><span data-stu-id="b6eea-107">Go to Cost accounting > Dimensions > Dimension hierarchies.</span></span>
2. <span data-ttu-id="b6eea-108">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="b6eea-108">Click New.</span></span>
3. <span data-ttu-id="b6eea-109">V poli HierarchyTypeComboBox vyberte Hierarchie klasifikace dimenzí.</span><span class="sxs-lookup"><span data-stu-id="b6eea-109">In the HierarchyTypeComboBox field, select 'Dimension classification hierarchy'.</span></span>
    * <span data-ttu-id="b6eea-110">Vyberte Hierarchie klasifikace dimenzí.</span><span class="sxs-lookup"><span data-stu-id="b6eea-110">Select Dimension classification hierarchy.</span></span> <span data-ttu-id="b6eea-111">Typ Hierarchie klasifikace dimenzí se používá k definování pravidel pro účely vykazování.</span><span class="sxs-lookup"><span data-stu-id="b6eea-111">The Dimension classification hierarchy type is used to define rules and for reporting purposes.</span></span> <span data-ttu-id="b6eea-112">Podporuje všechny dimenze, například objekty nákladů, prvky nákladů a statistické dimenze.</span><span class="sxs-lookup"><span data-stu-id="b6eea-112">It supports all dimensions, such as cost objects, cost elements, and statistical dimensions.</span></span>  
4. <span data-ttu-id="b6eea-113">Klikněte na položku Vytvořit.</span><span class="sxs-lookup"><span data-stu-id="b6eea-113">Click Create.</span></span>
5. <span data-ttu-id="b6eea-114">Do pole Název hierarchie dimenze zadejte hodnotu Organizace USP2.</span><span class="sxs-lookup"><span data-stu-id="b6eea-114">In the Dimension hierarchy name field, type 'Oganization USP2'.</span></span>
6. <span data-ttu-id="b6eea-115">V poli Dimenze zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="b6eea-115">In the Dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="b6eea-116">Vyberte Nákladová střediska.</span><span class="sxs-lookup"><span data-stu-id="b6eea-116">Select Cost centers.</span></span>  
7. <span data-ttu-id="b6eea-117">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="b6eea-117">Click Save.</span></span>
8. <span data-ttu-id="b6eea-118">Klikněte na Zobrazit hierarchii.</span><span class="sxs-lookup"><span data-stu-id="b6eea-118">Click View hierarchy.</span></span>
9. <span data-ttu-id="b6eea-119">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="b6eea-119">Click New.</span></span>
10. <span data-ttu-id="b6eea-120">Do pole Název uzlu zadejte CEO.</span><span class="sxs-lookup"><span data-stu-id="b6eea-120">In the Node name field, type 'CEO'.</span></span>
11. <span data-ttu-id="b6eea-121">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="b6eea-121">Click Save.</span></span>
12. <span data-ttu-id="b6eea-122">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="b6eea-122">Click New.</span></span>
13. <span data-ttu-id="b6eea-123">Do pole Název uzlu zadejte Nákladové středisko CEO.</span><span class="sxs-lookup"><span data-stu-id="b6eea-123">In the Node name field, type 'CEO cost centers'.</span></span>
14. <span data-ttu-id="b6eea-124">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="b6eea-124">Click Save.</span></span>
15. <span data-ttu-id="b6eea-125">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="b6eea-125">Click New.</span></span>
16. <span data-ttu-id="b6eea-126">Do pole Název uzlu zadejte Východní oblast.</span><span class="sxs-lookup"><span data-stu-id="b6eea-126">In the Node name field, type 'Region East'.</span></span>
17. <span data-ttu-id="b6eea-127">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="b6eea-127">Click Save.</span></span>
18. <span data-ttu-id="b6eea-128">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="b6eea-128">Click New.</span></span>
19. <span data-ttu-id="b6eea-129">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="b6eea-129">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="b6eea-130">V poli Od členu dimenze zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="b6eea-130">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="b6eea-131">Vyberte člena dimenze odpovídajícího uzlu.</span><span class="sxs-lookup"><span data-stu-id="b6eea-131">Select the dimension member that corresponds to the node.</span></span>  
21. <span data-ttu-id="b6eea-132">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="b6eea-132">Click Save.</span></span>
22. <span data-ttu-id="b6eea-133">Ve stromovém zobrazení vyberte Organizace USP2\CEO\Nákladová střediska CEO.</span><span class="sxs-lookup"><span data-stu-id="b6eea-133">In the tree, select 'Oganization USP2\CEO\CEO cost centers'.</span></span>
23. <span data-ttu-id="b6eea-134">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="b6eea-134">Click New.</span></span>
24. <span data-ttu-id="b6eea-135">Do pole Název uzlu zadejte Západní oblast.</span><span class="sxs-lookup"><span data-stu-id="b6eea-135">In the Node name field, type 'Region West'.</span></span>
25. <span data-ttu-id="b6eea-136">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="b6eea-136">Click Save.</span></span>
26. <span data-ttu-id="b6eea-137">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="b6eea-137">Click New.</span></span>
27. <span data-ttu-id="b6eea-138">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="b6eea-138">In the list, mark the selected row.</span></span>
28. <span data-ttu-id="b6eea-139">V poli Od členu dimenze zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="b6eea-139">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="b6eea-140">Vyberte člena dimenze odpovídajícího uzlu.</span><span class="sxs-lookup"><span data-stu-id="b6eea-140">Select the dimension member that corresponds to the node.</span></span>  
29. <span data-ttu-id="b6eea-141">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="b6eea-141">Click Save.</span></span>
30. <span data-ttu-id="b6eea-142">Ve stromovém zobrazení vyberte Organizace USP2\CEO.</span><span class="sxs-lookup"><span data-stu-id="b6eea-142">In the tree, select 'Oganization USP2\CEO'.</span></span>
31. <span data-ttu-id="b6eea-143">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="b6eea-143">Click New.</span></span>
32. <span data-ttu-id="b6eea-144">Do pole Název uzlu zadejte Nákladové středisko CFO.</span><span class="sxs-lookup"><span data-stu-id="b6eea-144">In the Node name field, type 'CFO cost centers'.</span></span>
33. <span data-ttu-id="b6eea-145">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="b6eea-145">Click Save.</span></span>
34. <span data-ttu-id="b6eea-146">Klikněte na možnost Nový.</span><span class="sxs-lookup"><span data-stu-id="b6eea-146">Click New.</span></span>
35. <span data-ttu-id="b6eea-147">Do pole Název uzlu zadejte Marketingová kampaň.</span><span class="sxs-lookup"><span data-stu-id="b6eea-147">In the Node name field, type 'Marketing campa'.</span></span>
36. <span data-ttu-id="b6eea-148">Do pole Název uzlu zadejte Marketingová kampaň.</span><span class="sxs-lookup"><span data-stu-id="b6eea-148">In the Node name field, type 'Marketing campaign'.</span></span>
37. <span data-ttu-id="b6eea-149">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="b6eea-149">Click Save.</span></span>
38. <span data-ttu-id="b6eea-150">Klikněte na možnost Nový.</span><span class="sxs-lookup"><span data-stu-id="b6eea-150">Click New.</span></span>
39. <span data-ttu-id="b6eea-151">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="b6eea-151">In the list, mark the selected row.</span></span>
40. <span data-ttu-id="b6eea-152">V poli Od členu dimenze zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="b6eea-152">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="b6eea-153">Vyberte člena dimenze odpovídajícího uzlu.</span><span class="sxs-lookup"><span data-stu-id="b6eea-153">Select the dimension member that corresponds to the node.</span></span>  
41. <span data-ttu-id="b6eea-154">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="b6eea-154">Click Save.</span></span>
42. <span data-ttu-id="b6eea-155">Ve stromovém zobrazení vyberte Organizace USP2\CEO\Nákladová střediska CFO.</span><span class="sxs-lookup"><span data-stu-id="b6eea-155">In the tree, select 'Organization USP2\CEO\CFO cost centers'.</span></span>
43. <span data-ttu-id="b6eea-156">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="b6eea-156">Click New.</span></span>
44. <span data-ttu-id="b6eea-157">Do pole Název uzlu zadejte Veletrhy.</span><span class="sxs-lookup"><span data-stu-id="b6eea-157">In the Node name field, type 'Trade shows'.</span></span>
45. <span data-ttu-id="b6eea-158">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="b6eea-158">Click Save.</span></span>
46. <span data-ttu-id="b6eea-159">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="b6eea-159">Click New.</span></span>
47. <span data-ttu-id="b6eea-160">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="b6eea-160">In the list, mark the selected row.</span></span>
48. <span data-ttu-id="b6eea-161">V poli Od členu dimenze zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="b6eea-161">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="b6eea-162">Vyberte člena dimenze odpovídajícího uzlu.</span><span class="sxs-lookup"><span data-stu-id="b6eea-162">Select the dimension member that corresponds to the node.</span></span>  
49. <span data-ttu-id="b6eea-163">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="b6eea-163">Click Save.</span></span>
50. <span data-ttu-id="b6eea-164">Ve stromovém zobrazení vyberte Organizace USP2\CEO.</span><span class="sxs-lookup"><span data-stu-id="b6eea-164">In the tree, select 'Oganization USP2\CEO'.</span></span>
51. <span data-ttu-id="b6eea-165">Do pole Název uzlu zadejte Nákladové středisko CIO.</span><span class="sxs-lookup"><span data-stu-id="b6eea-165">In the Node name field, type 'CIO cost centers'.</span></span>
52. <span data-ttu-id="b6eea-166">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="b6eea-166">Click Save.</span></span>
53. <span data-ttu-id="b6eea-167">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="b6eea-167">Click New.</span></span>
54. <span data-ttu-id="b6eea-168">Do pole Název uzlu zadejte Kontaktní střediska.</span><span class="sxs-lookup"><span data-stu-id="b6eea-168">In the Node name field, type 'Call centers'.</span></span>
55. <span data-ttu-id="b6eea-169">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="b6eea-169">Click Save.</span></span>
56. <span data-ttu-id="b6eea-170">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="b6eea-170">Click New.</span></span>
57. <span data-ttu-id="b6eea-171">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="b6eea-171">In the list, mark the selected row.</span></span>
58. <span data-ttu-id="b6eea-172">V poli Od členu dimenze zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="b6eea-172">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="b6eea-173">Vyberte člena dimenze odpovídajícího uzlu.</span><span class="sxs-lookup"><span data-stu-id="b6eea-173">Select the dimension member that corresponds to the node.</span></span>  
59. <span data-ttu-id="b6eea-174">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="b6eea-174">Click Save.</span></span>

