---
title: Elektronické vykazování – Mapování komponent vytvořeného formátu na prvky datového modelu (listopad 2016)
description: Toto téma popisuje, jak mapovat prvky datového modelu na komponenty vytvořené konfigurace elektronického výkaznictví (ER).
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1e3d6bcf229f9020ff4dd0479e486f465ffd6383
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570833"
---
# <a name="er-map-components-of-the-created-format-to-data-model-elements-november-2016"></a><span data-ttu-id="c7c30-103">Elektronické vykazování – Mapování komponent vytvořeného formátu na prvky datového modelu (listopad 2016)</span><span class="sxs-lookup"><span data-stu-id="c7c30-103">ER Map components of the created format to data model elements (November 2016)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c7c30-104">Následující postup popisuje, jak uživatel s rolí Správce systému nebo Návrhář elektronického výkaznictví může mapovat prvky datového modelu na komponenty vytvořené konfigurace elektronického výkaznictví, která určuje formát elektronického dokumentu obchodní doménu pro platby.</span><span class="sxs-lookup"><span data-stu-id="c7c30-104">The following procedure shows how a user in either the System administrator or Electronic reporting developer role can map data model elements to components of the created Electronic reporting (ER) configuration, which defines an electronic document format for the payments business domain.</span></span> <span data-ttu-id="c7c30-105">Tento formát bude využit později s cílem vygenerovat elektronické dokumenty pro zpracování plateb.</span><span class="sxs-lookup"><span data-stu-id="c7c30-105">This format will be used later to generate electronic documents for processing payments.</span></span> <span data-ttu-id="c7c30-106">V tomto příkladu vytvoříte konfiguraci formátu pro vzorovou společnost ‘Litware, Inc.’.</span><span class="sxs-lookup"><span data-stu-id="c7c30-106">In this example, you will create a format configuration for the sample company, 'Litware, Inc.'.</span></span> <span data-ttu-id="c7c30-107">Tyto kroky lze provést v každé společnosti, protože konfigurace ER jsou sdíleny všemi společnostmi.</span><span class="sxs-lookup"><span data-stu-id="c7c30-107">These steps can be performed in any company as ER configurations are shared for all companies.</span></span> <span data-ttu-id="c7c30-108">K provedení těchto kroků musíte nejprve dokončit kroky Průvodce záznamem úloh „Vytvoření konfigurace formátu“.</span><span class="sxs-lookup"><span data-stu-id="c7c30-108">To complete these steps, you must first complete the steps in the "Create a format configuration" task guide.</span></span>


## <a name="select-a-format-configuration"></a><span data-ttu-id="c7c30-109">Zvolte konfiguraci formátu</span><span class="sxs-lookup"><span data-stu-id="c7c30-109">Select a format configuration</span></span>
1. <span data-ttu-id="c7c30-110">Přejděte do části Správa organizace > Pracovní prostory > Elektronické výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="c7c30-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="c7c30-111">Klikněte na Konfigurace výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="c7c30-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="c7c30-112">Ve stromovém zobrazení rozbalte možnost „Platby (zjednodušený model)“.</span><span class="sxs-lookup"><span data-stu-id="c7c30-112">In the tree, expand 'Payments (simplified model)'.</span></span>
4. <span data-ttu-id="c7c30-113">Ve stromovém zobrazení vyberte možnost „Platby (zjednodušený model)\BACS (Velká Británie – fiktivní)“.</span><span class="sxs-lookup"><span data-stu-id="c7c30-113">In the tree, select 'Payments (simplified model)\BACS (UK fictitious)'.</span></span>
5. <span data-ttu-id="c7c30-114">Klikněte na možnost Návrhář.</span><span class="sxs-lookup"><span data-stu-id="c7c30-114">Click Designer.</span></span>

## <a name="map-format-components-to-data-model-elements"></a><span data-ttu-id="c7c30-115">Mapování součástí formátu na prvky datového modelu</span><span class="sxs-lookup"><span data-stu-id="c7c30-115">Map format components to data model elements</span></span>
1. <span data-ttu-id="c7c30-116">Klikněte na Rozbalit/sbalit.</span><span class="sxs-lookup"><span data-stu-id="c7c30-116">Click Expand/collapse.</span></span>
2. <span data-ttu-id="c7c30-117">Klikněte na kartu Mapování.</span><span class="sxs-lookup"><span data-stu-id="c7c30-117">Click the Mapping tab.</span></span>
3. <span data-ttu-id="c7c30-118">Ve stromovém zobrazení rozbalte „model“.</span><span class="sxs-lookup"><span data-stu-id="c7c30-118">In the tree, expand 'model'.</span></span>
4. <span data-ttu-id="c7c30-119">Ve stromové struktuře vyberte 'Xml\Zpráva\ProcessingDate\DateTime'.</span><span class="sxs-lookup"><span data-stu-id="c7c30-119">In the tree, select 'Xml\Message\ProcessingDate\DateTime'.</span></span>
5. <span data-ttu-id="c7c30-120">Ve stromové struktuře zvolte 'model\ProcessingDateTime'.</span><span class="sxs-lookup"><span data-stu-id="c7c30-120">In the tree, select 'model\ProcessingDateTime'.</span></span>
6. <span data-ttu-id="c7c30-121">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="c7c30-121">Click Bind.</span></span>
7. <span data-ttu-id="c7c30-122">Ve stromové struktuře vyberte 'Xml\Zpráva\MessageId\Řetězec'.</span><span class="sxs-lookup"><span data-stu-id="c7c30-122">In the tree, select 'Xml\Message\MessageId\String'.</span></span>
8. <span data-ttu-id="c7c30-123">Ve stromové struktuře vyberte 'model\MessageIdentification'.</span><span class="sxs-lookup"><span data-stu-id="c7c30-123">In the tree, select 'model\MessageIdentification'.</span></span>
9. <span data-ttu-id="c7c30-124">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="c7c30-124">Click Bind.</span></span>
10. <span data-ttu-id="c7c30-125">Ve stromovém zobrazení rozbalte „model\Platby“.</span><span class="sxs-lookup"><span data-stu-id="c7c30-125">In the tree, expand 'model\Payments'.</span></span>
11. <span data-ttu-id="c7c30-126">Ve stromové struktuře vyberte 'Xml\Zpráva\Platby\Položka\Částka\Řetězec'.</span><span class="sxs-lookup"><span data-stu-id="c7c30-126">In the tree, select 'Xml\Message\Payments\Item\Amount\String'.</span></span>
12. <span data-ttu-id="c7c30-127">Ve stromové struktuře zvolte 'model\Platby\InstructedAmount'.</span><span class="sxs-lookup"><span data-stu-id="c7c30-127">In the tree, select 'model\Payments\InstructedAmount'.</span></span>
13. <span data-ttu-id="c7c30-128">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="c7c30-128">Click Bind.</span></span>
14. <span data-ttu-id="c7c30-129">Ve stromové struktuře vyberte 'Xml\Zpráva\Platby\Položka\TransDate\DateTime'.</span><span class="sxs-lookup"><span data-stu-id="c7c30-129">In the tree, select 'Xml\Message\Payments\Item\TransDate\DateTime'.</span></span>
15. <span data-ttu-id="c7c30-130">Ve stromové struktuře vyberte 'model\Platby\TransactionDate'.</span><span class="sxs-lookup"><span data-stu-id="c7c30-130">In the tree, select 'model\Payments\TransactionDate'.</span></span>
16. <span data-ttu-id="c7c30-131">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="c7c30-131">Click Bind.</span></span>
17. <span data-ttu-id="c7c30-132">Ve stromové struktuře vyberte 'Xml\Zpráva\Platby\Položka\Popis\Řetězec'</span><span class="sxs-lookup"><span data-stu-id="c7c30-132">In the tree, select 'Xml\Message\Payments\Item\Description\String'.</span></span>
18. <span data-ttu-id="c7c30-133">Ve stromovém zobrazení vyberte „model\Platby\Popis“.</span><span class="sxs-lookup"><span data-stu-id="c7c30-133">In the tree, select 'model\Payments\Description'.</span></span>
19. <span data-ttu-id="c7c30-134">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="c7c30-134">Click Bind.</span></span>
20. <span data-ttu-id="c7c30-135">Ve stromové struktuře vyberte 'Xml\Zpráva\Platby\Položka\Měna\Řetězec'</span><span class="sxs-lookup"><span data-stu-id="c7c30-135">In the tree, select 'Xml\Message\Payments\Item\Currency\String'.</span></span>
21. <span data-ttu-id="c7c30-136">Ve stromovém zobrazení vyberte „model\Platby\Měna“.</span><span class="sxs-lookup"><span data-stu-id="c7c30-136">In the tree, select 'model\Payments\Currency'.</span></span>
22. <span data-ttu-id="c7c30-137">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="c7c30-137">Click Bind.</span></span>
23. <span data-ttu-id="c7c30-138">Ve stromové struktuře vyberte 'Xml\Zpráva\Platby\Položka\Id'</span><span class="sxs-lookup"><span data-stu-id="c7c30-138">In the tree, select 'Xml\Message\Payments\Item\Id'.</span></span>
24. <span data-ttu-id="c7c30-139">Ve stromové struktuře vyberte 'model\Platby\End2EndID'.</span><span class="sxs-lookup"><span data-stu-id="c7c30-139">In the tree, select 'model\Payments\End2EndID'.</span></span>
25. <span data-ttu-id="c7c30-140">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="c7c30-140">Click Bind.</span></span>
26. <span data-ttu-id="c7c30-141">Ve stromovém zobrazení rozbalte „model\Platby\Věřitel“.</span><span class="sxs-lookup"><span data-stu-id="c7c30-141">In the tree, expand 'model\Payments\Creditor'.</span></span>
27. <span data-ttu-id="c7c30-142">Ve stromovém zobrazení rozbalte „model\Platby\Věřitel\Účet“.</span><span class="sxs-lookup"><span data-stu-id="c7c30-142">In the tree, expand 'model\Payments\Creditor\Account'.</span></span>
28. <span data-ttu-id="c7c30-143">Ve stromovém zobrazení rozbalte „model\Platby\Věřitel\Zástupce“.</span><span class="sxs-lookup"><span data-stu-id="c7c30-143">In the tree, expand 'model\Payments\Creditor\Agent'.</span></span>
29. <span data-ttu-id="c7c30-144">Ve stromové struktuře vyberte 'Xml\Zpráva\Platby\Položka\Dodavatel\Název\Řetězec'.</span><span class="sxs-lookup"><span data-stu-id="c7c30-144">In the tree, select 'Xml\Message\Payments\Item\Vendor\Name\String'.</span></span>
30. <span data-ttu-id="c7c30-145">Ve stromovém zobrazení vyberte „model\Platby\Věřitel\Název“.</span><span class="sxs-lookup"><span data-stu-id="c7c30-145">In the tree, select 'model\Payments\Creditor\Name'.</span></span>
31. <span data-ttu-id="c7c30-146">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="c7c30-146">Click Bind.</span></span>
32. <span data-ttu-id="c7c30-147">Ve stromové struktuře vyberte 'Xml\Zpráva\Platby\Položka\Dodavatel\Banka\RoutingNumber\Řetězec'</span><span class="sxs-lookup"><span data-stu-id="c7c30-147">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber\String'.</span></span>
33. <span data-ttu-id="c7c30-148">Ve stromové struktuře vyberte 'model\Platby\Věřitel\Agent\RoutingNumber'.</span><span class="sxs-lookup"><span data-stu-id="c7c30-148">In the tree, select 'model\Payments\Creditor\Agent\RoutingNumber'.</span></span>
34. <span data-ttu-id="c7c30-149">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="c7c30-149">Click Bind.</span></span>
35. <span data-ttu-id="c7c30-150">Ve stromové struktuře vyberte 'Xml\Zpráva\Platby\Položka\Dodavatel\Banka\AccountNumber\Řetězec':</span><span class="sxs-lookup"><span data-stu-id="c7c30-150">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\AccountNumber\String'.</span></span>
36. <span data-ttu-id="c7c30-151">Ve stromovém zobrazení vyberte „model\Platby\Věřitel\Účet\Číslo“.</span><span class="sxs-lookup"><span data-stu-id="c7c30-151">In the tree, select 'model\Payments\Creditor\Account\Number'.</span></span>
37. <span data-ttu-id="c7c30-152">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="c7c30-152">Click Bind.</span></span>
38. <span data-ttu-id="c7c30-153">Ve stromové struktuře vyberte 'Xml\Zpráva\Platby\Položka\Plátce\Název\Řetězec'</span><span class="sxs-lookup"><span data-stu-id="c7c30-153">In the tree, select 'Xml\Message\Payments\Item\Payer\Name\String'.</span></span>
39. <span data-ttu-id="c7c30-154">Ve stromovém zobrazení rozbalte „model\Platby\Dlužník“.</span><span class="sxs-lookup"><span data-stu-id="c7c30-154">In the tree, expand 'model\Payments\Debtor'.</span></span>
40. <span data-ttu-id="c7c30-155">Ve stromovém zobrazení rozbalte „model\Platby\Dlužník\Účet“.</span><span class="sxs-lookup"><span data-stu-id="c7c30-155">In the tree, expand 'model\Payments\Debtor\Account'.</span></span>
41. <span data-ttu-id="c7c30-156">Ve stromovém zobrazení rozbalte „model\Platby\Dlužník\Zástupce“.</span><span class="sxs-lookup"><span data-stu-id="c7c30-156">In the tree, expand 'model\Payments\Debtor\Agent'.</span></span>
42. <span data-ttu-id="c7c30-157">Ve stromovém zobrazení vyberte „model\Platby\Dlužník\Název“.</span><span class="sxs-lookup"><span data-stu-id="c7c30-157">In the tree, select 'model\Payments\Debtor\Name'.</span></span>
43. <span data-ttu-id="c7c30-158">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="c7c30-158">Click Bind.</span></span>
44. <span data-ttu-id="c7c30-159">Ve stromové struktuře vyberte 'Xml\Zpráva\Platby\Položka\Plátce\Banka\RoutingNumber\Řetězec'</span><span class="sxs-lookup"><span data-stu-id="c7c30-159">In the tree, select 'Xml\Message\Payments\Item\Payer\Bank\RoutingNumber\String'.</span></span>
45. <span data-ttu-id="c7c30-160">Ve stromové struktuře vyberte 'model\Plátce\Dlužník\Agent\RoutingNumber'.</span><span class="sxs-lookup"><span data-stu-id="c7c30-160">In the tree, select 'model\Payments\Debtor\Agent\RoutingNumber'.</span></span>
46. <span data-ttu-id="c7c30-161">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="c7c30-161">Click Bind.</span></span>
47. <span data-ttu-id="c7c30-162">Ve stromové struktuře vyberte 'Xml\Zpráva\Platby\Položka\Plátce\Banka\AccountNumber\Řetězec'</span><span class="sxs-lookup"><span data-stu-id="c7c30-162">In the tree, select 'Xml\Message\Payments\Item\Payer\Bank\AccountNumber\String'.</span></span>
48. <span data-ttu-id="c7c30-163">Ve stromovém zobrazení vyberte „model\Platby\Dlužník\Účet\Číslo“.</span><span class="sxs-lookup"><span data-stu-id="c7c30-163">In the tree, select 'model\Payments\Debtor\Account\Number'.</span></span>
49. <span data-ttu-id="c7c30-164">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="c7c30-164">Click Bind.</span></span>
50. <span data-ttu-id="c7c30-165">Ve stromové struktuře vyberte 'Xml\Zpráva\Platby\Položka'.</span><span class="sxs-lookup"><span data-stu-id="c7c30-165">In the tree, select 'Xml\Message\Payments\Item'.</span></span>
51. <span data-ttu-id="c7c30-166">Ve stromovém zobrazení vyberte „model\Platby“.</span><span class="sxs-lookup"><span data-stu-id="c7c30-166">In the tree, select 'model\Payments'.</span></span>
52. <span data-ttu-id="c7c30-167">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="c7c30-167">Click Bind.</span></span>
53. <span data-ttu-id="c7c30-168">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="c7c30-168">Click Save.</span></span>

## <a name="validate-format-mapping"></a><span data-ttu-id="c7c30-169">Ověření mapování formátu</span><span class="sxs-lookup"><span data-stu-id="c7c30-169">Validate format mapping</span></span>
1. <span data-ttu-id="c7c30-170">Klikněte na tlačítko Ověřit.</span><span class="sxs-lookup"><span data-stu-id="c7c30-170">Click Validate.</span></span>
    * <span data-ttu-id="c7c30-171">Ověřte nové mapování, abyste se ujistili, že všechny vazby jsou v pořádku.</span><span class="sxs-lookup"><span data-stu-id="c7c30-171">Validate the new mapping to ensure that all bindings are okay.</span></span>  
2. <span data-ttu-id="c7c30-172">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="c7c30-172">Close the page.</span></span>

## <a name="change-status-of-the-current-version-of-format-configuration"></a><span data-ttu-id="c7c30-173">Změna stavu aktuální verze konfigurace formátu</span><span class="sxs-lookup"><span data-stu-id="c7c30-173">Change status of the current version of format configuration</span></span>
<span data-ttu-id="c7c30-174">V dalších krocích změníte stav konfigurace formátu ze stavu Návrh na stav Dokončeno, aby byla dostupná pro generování platebních dokumentů.</span><span class="sxs-lookup"><span data-stu-id="c7c30-174">In the next steps, you'll change the status of the format configuration from Draft to Completed to make it available for payment document generation.</span></span>  
1. <span data-ttu-id="c7c30-175">Klikněte na položku Změnit stav.</span><span class="sxs-lookup"><span data-stu-id="c7c30-175">Click Change status.</span></span>
2. <span data-ttu-id="c7c30-176">Klikněte na tlačítko Dokončit.</span><span class="sxs-lookup"><span data-stu-id="c7c30-176">Click Complete.</span></span>
3. <span data-ttu-id="c7c30-177">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="c7c30-177">In the Description field, type a value.</span></span>
    * <span data-ttu-id="c7c30-178">Například 'verze 1'.</span><span class="sxs-lookup"><span data-stu-id="c7c30-178">For example, 'version 1'.</span></span>  
4. <span data-ttu-id="c7c30-179">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="c7c30-179">Click OK.</span></span>
5. <span data-ttu-id="c7c30-180">Vyberte dokončenou verzi aktuální konfigurace.</span><span class="sxs-lookup"><span data-stu-id="c7c30-180">Select completed version of the current configuration.</span></span>
    * <span data-ttu-id="c7c30-181">Všimněte si, že je konfigurace uložena jako dokončená verze 1.1: verze 1 formátu založeného na verzi 1 datového modelu.</span><span class="sxs-lookup"><span data-stu-id="c7c30-181">Note that the configuration is saved as completed version 1.1: version 1 of the format based on the version 1 of the data model.</span></span>  

## <a name="define-effective-date-for-completed-version-of-format"></a><span data-ttu-id="c7c30-182">Definování data účinnosti dokončené verze formátu</span><span class="sxs-lookup"><span data-stu-id="c7c30-182">Define effective date for completed version of format</span></span>
<span data-ttu-id="c7c30-183">Každou verzi formátu lze konfigurovat jako dostupnou pro použití od určitého data.</span><span class="sxs-lookup"><span data-stu-id="c7c30-183">Each format version can be configured as available for usage starting from a certain date.</span></span> <span data-ttu-id="c7c30-184">Je-li více než jedna verze formátu aktivní ke konkrétnímu datu, k použití bude vybrán nejnovější formát (na základě čísla verze).</span><span class="sxs-lookup"><span data-stu-id="c7c30-184">When more than one format version is active on a certain date, the latest format (based on version number) will be selected for usage.</span></span> <span data-ttu-id="c7c30-185">Pro výběr správné verze se používá hodnota data relace.</span><span class="sxs-lookup"><span data-stu-id="c7c30-185">The session date value is used for proper version selection.</span></span>  

## <a name="restrict-access-to-created-format-from-companies"></a><span data-ttu-id="c7c30-186">Omezení přístupu k vytvořenému formátu ze společností</span><span class="sxs-lookup"><span data-stu-id="c7c30-186">Restrict access to created format from companies</span></span>
1. <span data-ttu-id="c7c30-187">Rozbalte oddíl Kódy ISO zemí/oblastí.</span><span class="sxs-lookup"><span data-stu-id="c7c30-187">Expand the ISO Country/region codes section.</span></span>
    * <span data-ttu-id="c7c30-188">Označením konkrétní země/oblasti, ve které lze formát použít, lze omezit přístup ke každému formátu.</span><span class="sxs-lookup"><span data-stu-id="c7c30-188">Each format access can be restricted by identifying particular countries/regions in which a format is applicable.</span></span> <span data-ttu-id="c7c30-189">Pokud je seznam zemí/oblastí pro určitý formát prázdný, lze použít tento formát v jakékoli společnosti.</span><span class="sxs-lookup"><span data-stu-id="c7c30-189">When the list of countries/regions for particular format is empty, this format can be used in any company.</span></span> <span data-ttu-id="c7c30-190">Pokud jsou do tohoto seznamu zemí/oblastí vloženy některé kódy země/oblasti ISO, lze použít tento formát pouze ve společnostech, které mají primární adresu v této zemi/regionu.</span><span class="sxs-lookup"><span data-stu-id="c7c30-190">When some ISO country/region codes are inserted in the list of countries/regions, the format can only be use in companies if the primary address is in the country/region.</span></span>  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]