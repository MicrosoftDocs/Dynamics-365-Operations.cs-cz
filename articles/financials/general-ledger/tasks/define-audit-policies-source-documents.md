--- 
title: "Definování zásad auditu pro zdrojové dokumenty"
description: "Tento postup popisuje způsob nastavení a spuštění pravidel zásad auditu."
author: ryansandness
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysPolicySourceDocumentRuleType, SysFieldLookUp, SysPolicyListPage, SysPolicy, AuditPolicyRule, SysQueryForm, SysQueryFieldLookUp, AuditPolicyDateSelection, AuditPolicyAdditionalOption, BatchJob, CaseDetail
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: a82c3e8e8787beb309b75b73cda36f4ca8031d6f
ms.contentlocale: cs-cz
ms.lasthandoff: 09/14/2018

---
# <a name="define-audit-policies-for-source-documents"></a><span data-ttu-id="d57be-103">Definování zásad auditu pro zdrojové dokumenty</span><span class="sxs-lookup"><span data-stu-id="d57be-103">Define audit policies for source documents</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d57be-104">Tento postup popisuje způsob nastavení a spuštění pravidel zásad auditu.</span><span class="sxs-lookup"><span data-stu-id="d57be-104">This procedure shows how to set up and run audit policy rules.</span></span> <span data-ttu-id="d57be-105">Příklad využívá sestavu výdajů s typem Výdaje hotelu.</span><span class="sxs-lookup"><span data-stu-id="d57be-105">The example uses expense reports with the hotel expense type.</span></span> <span data-ttu-id="d57be-106">Tato procedura používá ukázkovou společnost USMF.</span><span class="sxs-lookup"><span data-stu-id="d57be-106">This procedure uses the USMF demo company.</span></span> <span data-ttu-id="d57be-107">Role auditora obsahuje dostatečná oprávnění k provedení těchto úloh.</span><span class="sxs-lookup"><span data-stu-id="d57be-107">The auditor role contains the correct permissions in order to perform these tasks.</span></span>

1. <span data-ttu-id="d57be-108">Přejděte na pracovní plochu pro Audit > Nastavení > Typ pravidla zásad.</span><span class="sxs-lookup"><span data-stu-id="d57be-108">Go to Audit workbench > Setup > Policy rule type.</span></span>
2. <span data-ttu-id="d57be-109">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="d57be-109">Click New.</span></span>
3. <span data-ttu-id="d57be-110">Zadejte hodnotu do pole Název pravidla.</span><span class="sxs-lookup"><span data-stu-id="d57be-110">In the Rule name field, type a value.</span></span>
4. <span data-ttu-id="d57be-111">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="d57be-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="d57be-112">V poli Název dotazu vyberte řádek Sestava výdajů</span><span class="sxs-lookup"><span data-stu-id="d57be-112">In the Query name field, select Expense report line</span></span>
6. <span data-ttu-id="d57be-113">V poli typ dotazu vyberte Agregovat</span><span class="sxs-lookup"><span data-stu-id="d57be-113">In the query type field, select Aggregate</span></span>
7. <span data-ttu-id="d57be-114">V poli Právnická osoba vyberte právnickou osobu</span><span class="sxs-lookup"><span data-stu-id="d57be-114">In the Legal entity field, select Legal entity</span></span>
8. <span data-ttu-id="d57be-115">V poli Odkaz na datum dokumentu vyberte Datum a čas úpravy</span><span class="sxs-lookup"><span data-stu-id="d57be-115">In the Document date reference field, select Modified date and time</span></span>
9. <span data-ttu-id="d57be-116">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="d57be-116">Click Save.</span></span>
10. <span data-ttu-id="d57be-117">Přejděte na pracovní plochu pro Audit > Nastavení > Zásady auditu.</span><span class="sxs-lookup"><span data-stu-id="d57be-117">Go to Audit workbench > Setup > Audit policies.</span></span>
11. <span data-ttu-id="d57be-118">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="d57be-118">Click New.</span></span>
12. <span data-ttu-id="d57be-119">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="d57be-119">In the Name field, type a value.</span></span>
13. <span data-ttu-id="d57be-120">Rozbalte část Organizace zásad.</span><span class="sxs-lookup"><span data-stu-id="d57be-120">Expand the Policy organizations section.</span></span>
14. <span data-ttu-id="d57be-121">Ve stromovém zobrazení vyberte systém Contoso Entertainment System USA.</span><span class="sxs-lookup"><span data-stu-id="d57be-121">In the tree, select 'Contoso Entertainment System USA'.</span></span>
15. <span data-ttu-id="d57be-122">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="d57be-122">Click Add.</span></span>
16. <span data-ttu-id="d57be-123">Ve stromovém zobrazení vyberte Contoso Consulting.</span><span class="sxs-lookup"><span data-stu-id="d57be-123">In the tree, select 'Contoso Consulting USA'.</span></span>
17. <span data-ttu-id="d57be-124">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="d57be-124">Click Add.</span></span>
18. <span data-ttu-id="d57be-125">Ve stromovém zobrazení vyberte Contoso Retail USA.</span><span class="sxs-lookup"><span data-stu-id="d57be-125">In the tree, select 'Contoso Retail USA'.</span></span>
19. <span data-ttu-id="d57be-126">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="d57be-126">Click Add.</span></span>
20. <span data-ttu-id="d57be-127">Sbalte část Organizace zásad.</span><span class="sxs-lookup"><span data-stu-id="d57be-127">Collapse the Policy organizations section.</span></span>
21. <span data-ttu-id="d57be-128">Rozbalte část Pravidla zásad.</span><span class="sxs-lookup"><span data-stu-id="d57be-128">Expand the Policy rules section.</span></span>
22. <span data-ttu-id="d57be-129">V seznamu vyhledejte a vyberte pravidlo zásad, které již bylo vytvořeno.</span><span class="sxs-lookup"><span data-stu-id="d57be-129">In the list, find and select the Policy Rule that was created previously.</span></span>
23. <span data-ttu-id="d57be-130">Klikněte na Vytvořit pravidlo zásad.</span><span class="sxs-lookup"><span data-stu-id="d57be-130">Click Create policy rule.</span></span>
24. <span data-ttu-id="d57be-131">Do pole Datum platnosti zadejte datum a čas.</span><span class="sxs-lookup"><span data-stu-id="d57be-131">In the Effective date field, enter a date and time.</span></span>
25. <span data-ttu-id="d57be-132">Klepněte na tlačítko Filtr.</span><span class="sxs-lookup"><span data-stu-id="d57be-132">Click Filter.</span></span>
26. <span data-ttu-id="d57be-133">V seznamu vyberte řádek pro kategorii výdajů a nastavte podrobnosti o hotelu</span><span class="sxs-lookup"><span data-stu-id="d57be-133">In the list, select the row for Expense category, and set the details to Hotel</span></span>
27. <span data-ttu-id="d57be-134">V poli Kritéria zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="d57be-134">In the Criteria field, enter or select a value.</span></span>
28. <span data-ttu-id="d57be-135">Klikněte na kartu Agregovat.</span><span class="sxs-lookup"><span data-stu-id="d57be-135">Click the Aggregate tab.</span></span>
29. <span data-ttu-id="d57be-136">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="d57be-136">Click Add.</span></span>
30. <span data-ttu-id="d57be-137">V seznamu vyberte hodnotu pole pro Částka transakce</span><span class="sxs-lookup"><span data-stu-id="d57be-137">In the list, select a field value of Transaction amount</span></span>
31. <span data-ttu-id="d57be-138">V poli Pole zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="d57be-138">In the Field field, enter or select a value.</span></span>
32. <span data-ttu-id="d57be-139">V poli Agregační funkce vyberte "Součet".</span><span class="sxs-lookup"><span data-stu-id="d57be-139">In the AggregateFunction field, select 'Sum'.</span></span>
33. <span data-ttu-id="d57be-140">Klikněte na kartu Seskupit podle.</span><span class="sxs-lookup"><span data-stu-id="d57be-140">Click the Group by tab.</span></span>
34. <span data-ttu-id="d57be-141">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="d57be-141">Click Add.</span></span>
35. <span data-ttu-id="d57be-142">V seznamu vyberte hodnotu Zaměstnanec </span><span class="sxs-lookup"><span data-stu-id="d57be-142">In the list, select a value of Employee</span></span> 
36. <span data-ttu-id="d57be-143">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="d57be-143">Click Add.</span></span>
37. <span data-ttu-id="d57be-144">V seznamu vyberte hodnotu Kategorie výdaje</span><span class="sxs-lookup"><span data-stu-id="d57be-144">In the list, select a value of Expense category</span></span>
38. <span data-ttu-id="d57be-145">V poli Pole zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="d57be-145">In the Field field, enter or select a value.</span></span>
39. <span data-ttu-id="d57be-146">Klikněte na kartu Má.</span><span class="sxs-lookup"><span data-stu-id="d57be-146">Click the Having tab.</span></span>
40. <span data-ttu-id="d57be-147">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="d57be-147">Click Add.</span></span>
41. <span data-ttu-id="d57be-148">Vyberte Částka transakce</span><span class="sxs-lookup"><span data-stu-id="d57be-148">Select Transaction amount</span></span>
42. <span data-ttu-id="d57be-149">V poli Pole zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="d57be-149">In the Field field, enter or select a value.</span></span>
43. <span data-ttu-id="d57be-150">V poli Agregační funkce vyberte "Součet".</span><span class="sxs-lookup"><span data-stu-id="d57be-150">In the AggregateFunction field, select 'Sum'.</span></span>
44. <span data-ttu-id="d57be-151">Zadejte hodnotu >2000 do pole Kritéria.</span><span class="sxs-lookup"><span data-stu-id="d57be-151">In the Criteria field, type '>2000'.</span></span>
45. <span data-ttu-id="d57be-152">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="d57be-152">Click OK.</span></span>
46. <span data-ttu-id="d57be-153">Klepněte na možnost Test.</span><span class="sxs-lookup"><span data-stu-id="d57be-153">Click Test.</span></span>
47. <span data-ttu-id="d57be-154">Do pole Počáteční datum pro výběr dokumentů zadejte datum a čas.</span><span class="sxs-lookup"><span data-stu-id="d57be-154">In the Document selection starting date field, enter a date and time.</span></span>
48. <span data-ttu-id="d57be-155">Do pole Konečné datum pro výběr dokumentů zadejte datum a čas.</span><span class="sxs-lookup"><span data-stu-id="d57be-155">In the Document selection ending date field, enter a date and time.</span></span>
49. <span data-ttu-id="d57be-156">Klikněte na Spustit test.</span><span class="sxs-lookup"><span data-stu-id="d57be-156">Click Run test.</span></span>
50. <span data-ttu-id="d57be-157">V podokně akcí klikněte na možnost Zásady auditu.</span><span class="sxs-lookup"><span data-stu-id="d57be-157">On the Action Pane, click Audit policy.</span></span>
51. <span data-ttu-id="d57be-158">Klikněte na Další možnosti.</span><span class="sxs-lookup"><span data-stu-id="d57be-158">Click Additional options.</span></span>
52. <span data-ttu-id="d57be-159">Do pole Počáteční datum zadejte datum a čas.</span><span class="sxs-lookup"><span data-stu-id="d57be-159">In the Starting date field, enter a date and time.</span></span>
53. <span data-ttu-id="d57be-160">Do pole Konečné datum zadejte datum a čas.</span><span class="sxs-lookup"><span data-stu-id="d57be-160">In the Ending date field, enter a date and time.</span></span>
54. <span data-ttu-id="d57be-161">Klepněte na možnost Dávka.</span><span class="sxs-lookup"><span data-stu-id="d57be-161">Click Batch.</span></span>
55. <span data-ttu-id="d57be-162">Rozbalte sekci Spustit na pozadí.</span><span class="sxs-lookup"><span data-stu-id="d57be-162">Expand the Run in the background section.</span></span>
56. <span data-ttu-id="d57be-163">V poli Dávkové zpracování vyberte hodnotu Ano.</span><span class="sxs-lookup"><span data-stu-id="d57be-163">Select Yes in the Batch processing field.</span></span>
57. <span data-ttu-id="d57be-164">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="d57be-164">Click OK.</span></span>
58. <span data-ttu-id="d57be-165">Přejděte na Pracovní plocha auditu > Auditní případy.</span><span class="sxs-lookup"><span data-stu-id="d57be-165">Go to Audit workbench > Audit cases.</span></span>
59. <span data-ttu-id="d57be-166">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="d57be-166">In the list, find and select the desired record.</span></span>
60. <span data-ttu-id="d57be-167">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="d57be-167">In the list, click the link in the selected row.</span></span>
61. <span data-ttu-id="d57be-168">Rozbalte sekci Přidružení.</span><span class="sxs-lookup"><span data-stu-id="d57be-168">Expand the Associations section.</span></span>
62. <span data-ttu-id="d57be-169">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="d57be-169">In the list, find and select the desired record.</span></span>
63. <span data-ttu-id="d57be-170">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="d57be-170">In the list, click the link in the selected row.</span></span>


