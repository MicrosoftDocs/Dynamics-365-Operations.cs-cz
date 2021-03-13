---
title: Definování zásad auditu pro zdrojové dokumenty
description: Toto téma vysvětluje způsob nastavení a spuštění pravidel zásad auditu.
author: panolte
manager: AnnBe
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysFieldLookUp, SysPolicyListPage, SysPolicy, AuditPolicyRule, SysQueryForm, SysQueryFieldLookUp, AuditPolicyDateSelection, AuditPolicyAdditionalOption, BatchJob, CaseDetail
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e020a9e82ff18055e40e3e0ddc7bbed1068c886c
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/16/2021
ms.locfileid: "5021422"
---
# <a name="define-audit-policies-for-source-documents"></a><span data-ttu-id="c26ac-103">Definování zásad auditu pro zdrojové dokumenty</span><span class="sxs-lookup"><span data-stu-id="c26ac-103">Define audit policies for source documents</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c26ac-104">Toto téma vysvětluje způsob nastavení a spuštění pravidel zásad auditu.</span><span class="sxs-lookup"><span data-stu-id="c26ac-104">This topic explains how to set up and run audit policy rules.</span></span> <span data-ttu-id="c26ac-105">Příklad využívá sestavu výdajů s typem Výdaje hotelu.</span><span class="sxs-lookup"><span data-stu-id="c26ac-105">The example uses expense reports with the hotel expense type.</span></span> <span data-ttu-id="c26ac-106">Tato procedura používá ukázkovou společnost USMF.</span><span class="sxs-lookup"><span data-stu-id="c26ac-106">This procedure uses the USMF demo company.</span></span> <span data-ttu-id="c26ac-107">Role auditora obsahuje dostatečná oprávnění k provedení těchto úloh.</span><span class="sxs-lookup"><span data-stu-id="c26ac-107">The auditor role contains the correct permissions in order to perform these tasks.</span></span>

1. <span data-ttu-id="c26ac-108">V navigačním podokně přejděte na **Moduly > Pracovní plocha auditu > Nastavení > Typ pravidla zásad**.</span><span class="sxs-lookup"><span data-stu-id="c26ac-108">In the navigation pane, go to **Modules > Audit workbench > Setup > Policy rule type**.</span></span>
2. <span data-ttu-id="c26ac-109">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="c26ac-109">Select **New**.</span></span>
3. <span data-ttu-id="c26ac-110">Zadejte hodnotu do pole **Název pravidla**.</span><span class="sxs-lookup"><span data-stu-id="c26ac-110">In the **Rule name** field, type a value.</span></span>
4. <span data-ttu-id="c26ac-111">Zadejte hodnotu do pole **Popis**.</span><span class="sxs-lookup"><span data-stu-id="c26ac-111">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="c26ac-112">V poli **Název dotazu** vyberte **Řádek sestavy výdajů**</span><span class="sxs-lookup"><span data-stu-id="c26ac-112">In the **Query name** field, select **Expense report line**</span></span>
6. <span data-ttu-id="c26ac-113">V poli **Typ dotazu** vyberte **Agregovat**</span><span class="sxs-lookup"><span data-stu-id="c26ac-113">In the **query type** field, select **Aggregate**</span></span>
7. <span data-ttu-id="c26ac-114">V poli **Právnická osoba** vyberte **právnickou osobu**</span><span class="sxs-lookup"><span data-stu-id="c26ac-114">In the **Legal entity** field, select **Legal entity**</span></span>
8. <span data-ttu-id="c26ac-115">V poli **Odkaz na datum dokumentu** vyberte **Datum a čas úpravy**</span><span class="sxs-lookup"><span data-stu-id="c26ac-115">In the **Document date reference** field, select **Modified date and time**</span></span>
9. <span data-ttu-id="c26ac-116">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="c26ac-116">Select **Save**.</span></span>
10. <span data-ttu-id="c26ac-117">V navigačním podokně přejděte na **Moduly > Pracovní plocha auditu > Nastavení > Zásady auditu**.</span><span class="sxs-lookup"><span data-stu-id="c26ac-117">In the navigation pane, go to **Modules > Audit workbench > Setup > Audit policies**.</span></span>
11. <span data-ttu-id="c26ac-118">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="c26ac-118">Select **New**.</span></span>
12. <span data-ttu-id="c26ac-119">Zadejte hodnotu do pole **Název**.</span><span class="sxs-lookup"><span data-stu-id="c26ac-119">In the **Name** field, type a value.</span></span>
13. <span data-ttu-id="c26ac-120">Rozbalte část **Organizace zásad**.</span><span class="sxs-lookup"><span data-stu-id="c26ac-120">Expand the **Policy organizations** section.</span></span>
14. <span data-ttu-id="c26ac-121">Ve stromovém zobrazení vyberte **Contoso Entertainment System USA** a pak zvolte **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="c26ac-121">In the tree, select **Contoso Entertainment System USA**, then select **Add**.</span></span>
15. <span data-ttu-id="c26ac-122">Ve stromovém zobrazení vyberte **Contoso Consulting USA** a pak zvolte **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="c26ac-122">In the tree, select **Contoso Consulting USA**, then select **Add**.</span></span>
16. <span data-ttu-id="c26ac-123">Ve stromovém zobrazení vyberte **Contoso Retail USA** a pak zvolte **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="c26ac-123">In the tree, select **Contoso Retail USA**, then select **Add**.</span></span>
17. <span data-ttu-id="c26ac-124">Sbalte část **Organizace zásad**.</span><span class="sxs-lookup"><span data-stu-id="c26ac-124">Collapse the **Policy organizations** section.</span></span>
18. <span data-ttu-id="c26ac-125">Rozbalte část **Pravidla zásad**.</span><span class="sxs-lookup"><span data-stu-id="c26ac-125">Expand the **Policy rules** section.</span></span>
19. <span data-ttu-id="c26ac-126">V seznamu vyhledejte a vyberte pravidlo zásad, které již bylo vytvořeno.</span><span class="sxs-lookup"><span data-stu-id="c26ac-126">In the list, find and select the Policy Rule that was created previously.</span></span>
20. <span data-ttu-id="c26ac-127">Vyberte **Vytvořit pravidlo zásad**.</span><span class="sxs-lookup"><span data-stu-id="c26ac-127">Select **Create policy rule**.</span></span>
21. <span data-ttu-id="c26ac-128">Do pole **Datum platnosti** zadejte datum a čas.</span><span class="sxs-lookup"><span data-stu-id="c26ac-128">In the **Effective date** field, enter a date and time.</span></span>
22. <span data-ttu-id="c26ac-129">Vyberte **Filtr**.</span><span class="sxs-lookup"><span data-stu-id="c26ac-129">Select **Filter**.</span></span>
23. <span data-ttu-id="c26ac-130">V seznamu vyberte řádek pro **kategorii výdajů** a nastavte podrobnosti o **hotelu**.</span><span class="sxs-lookup"><span data-stu-id="c26ac-130">In the list, select the row for **Expense category**, and set the details to **Hotel**.</span></span>
24. <span data-ttu-id="c26ac-131">V poli **Kritéria** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="c26ac-131">In the **Criteria** field, enter or select a value.</span></span>
25. <span data-ttu-id="c26ac-132">Vyberte karu **Agregovat**.</span><span class="sxs-lookup"><span data-stu-id="c26ac-132">Select the **Aggregate** tab.</span></span>
26. <span data-ttu-id="c26ac-133">Vyberte **přidat**.</span><span class="sxs-lookup"><span data-stu-id="c26ac-133">Select **Add**.</span></span>
27. <span data-ttu-id="c26ac-134">V seznamu vyberte hodnotu pole **Částka transakce**.</span><span class="sxs-lookup"><span data-stu-id="c26ac-134">In the list, select a field value of **Transaction amount**.</span></span>
28. <span data-ttu-id="c26ac-135">V poli **Pole** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="c26ac-135">In the **Field** field, enter or select a value.</span></span>
29. <span data-ttu-id="c26ac-136">V poli **Agregační funkce** vyberte **Součet**.</span><span class="sxs-lookup"><span data-stu-id="c26ac-136">In the **AggregateFunction** field, select **Sum**.</span></span>
30. <span data-ttu-id="c26ac-137">Vyberte kartu **Seskupit podle**.</span><span class="sxs-lookup"><span data-stu-id="c26ac-137">Select the **Group by** tab.</span></span>
31. <span data-ttu-id="c26ac-138">Vyberte **přidat**.</span><span class="sxs-lookup"><span data-stu-id="c26ac-138">Select **Add**.</span></span>
32. <span data-ttu-id="c26ac-139">V seznamu vyberte hodnotu **Zaměstnanec**.</span><span class="sxs-lookup"><span data-stu-id="c26ac-139">In the list, select a value of **Employee** .</span></span>
33. <span data-ttu-id="c26ac-140">Vyberte **přidat**.</span><span class="sxs-lookup"><span data-stu-id="c26ac-140">Select **Add**.</span></span>
34. <span data-ttu-id="c26ac-141">V seznamu vyberte hodnotu **Kategorie výdaje**.</span><span class="sxs-lookup"><span data-stu-id="c26ac-141">In the list, select a value of **Expense category**.</span></span>
35. <span data-ttu-id="c26ac-142">V poli **Pole** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="c26ac-142">In the **Field** field, enter or select a value.</span></span>
36. <span data-ttu-id="c26ac-143">Vyberte kartu **Má**.</span><span class="sxs-lookup"><span data-stu-id="c26ac-143">Select the **Having** tab.</span></span>
37. <span data-ttu-id="c26ac-144">Vyberte **přidat**.</span><span class="sxs-lookup"><span data-stu-id="c26ac-144">Select **Add**.</span></span>
38. <span data-ttu-id="c26ac-145">Vyberte **Částka transakce**.</span><span class="sxs-lookup"><span data-stu-id="c26ac-145">Select **Transaction amount**.</span></span>
39. <span data-ttu-id="c26ac-146">V poli **Pole** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="c26ac-146">In the **Field** field, enter or select a value.</span></span>
40. <span data-ttu-id="c26ac-147">V poli **Agregační funkce** vyberte **Součet**.</span><span class="sxs-lookup"><span data-stu-id="c26ac-147">In the **AggregateFunction** field, select **Sum**.</span></span>
41. <span data-ttu-id="c26ac-148">Zadejte hodnotu `>2000` do pole **Kritéria**.</span><span class="sxs-lookup"><span data-stu-id="c26ac-148">In the **Criteria** field, type `>2000`.</span></span>
42. <span data-ttu-id="c26ac-149">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="c26ac-149">Select **OK**.</span></span>
43. <span data-ttu-id="c26ac-150">Vyberte **Test**.</span><span class="sxs-lookup"><span data-stu-id="c26ac-150">Select **Test**.</span></span>
44. <span data-ttu-id="c26ac-151">Do pole **Počáteční datum pro výběr dokumentů** zadejte datum a čas.</span><span class="sxs-lookup"><span data-stu-id="c26ac-151">In the **Document selection starting date** field, enter a date and time.</span></span>
45. <span data-ttu-id="c26ac-152">Do pole **Konečné datum pro výběr dokumentů** zadejte datum a čas.</span><span class="sxs-lookup"><span data-stu-id="c26ac-152">In the **Document selection ending date** field, enter a date and time.</span></span>
46. <span data-ttu-id="c26ac-153">Vyberte **Spustit test**.</span><span class="sxs-lookup"><span data-stu-id="c26ac-153">Select **Run test**.</span></span>
47. <span data-ttu-id="c26ac-154">V podokně akcí zvolte **Zásady auditu**.</span><span class="sxs-lookup"><span data-stu-id="c26ac-154">On the Action Pane, select **Audit policy**.</span></span>
48. <span data-ttu-id="c26ac-155">Vyberte **Další možnosti**.</span><span class="sxs-lookup"><span data-stu-id="c26ac-155">Select **Additional options**.</span></span>
49. <span data-ttu-id="c26ac-156">Do pole **Počáteční datum** zadejte datum a čas.</span><span class="sxs-lookup"><span data-stu-id="c26ac-156">In the **Starting date** field, enter a date and time.</span></span>
50. <span data-ttu-id="c26ac-157">Do pole **Koncové datum** zadejte datum a čas.</span><span class="sxs-lookup"><span data-stu-id="c26ac-157">In the **Ending date** field, enter a date and time.</span></span>
51. <span data-ttu-id="c26ac-158">Vyberte **Dávka**.</span><span class="sxs-lookup"><span data-stu-id="c26ac-158">Select **Batch**.</span></span>
52. <span data-ttu-id="c26ac-159">Rozbalte sekci **Spustit na pozadí**.</span><span class="sxs-lookup"><span data-stu-id="c26ac-159">Expand the **Run in the background** section.</span></span>
53. <span data-ttu-id="c26ac-160">V poli **Dávkové zpracování** vyberte hodnotu **Ano**.</span><span class="sxs-lookup"><span data-stu-id="c26ac-160">Select **Yes** in the **Batch processing** field.</span></span>
54. <span data-ttu-id="c26ac-161">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="c26ac-161">Select **OK**.</span></span>
55. <span data-ttu-id="c26ac-162">V navigačním podokně přejděte na **Moduly > Pracovní plocha auditu > Nastavení > Případy auditu**.</span><span class="sxs-lookup"><span data-stu-id="c26ac-162">In the navigation pane, go to **Modules > Audit workbench > Audit cases**.</span></span>
56. <span data-ttu-id="c26ac-163">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="c26ac-163">In the list, find and select the desired record.</span></span>
57. <span data-ttu-id="c26ac-164">Rozbalte sekci **Přidružení**.</span><span class="sxs-lookup"><span data-stu-id="c26ac-164">Expand the **Associations** section.</span></span>
58. <span data-ttu-id="c26ac-165">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="c26ac-165">In the list, find and select the desired record.</span></span>

