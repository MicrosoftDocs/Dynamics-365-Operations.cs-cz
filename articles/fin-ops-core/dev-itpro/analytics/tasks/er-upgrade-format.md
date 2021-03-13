---
title: Elektronické výkaznictví - Upgrade formátu přijetím nové základní verze tohoto formátu
description: Toto téma popisuje, jak udržovat konfigurace formátu pro elektronické výkaznictví (ER).
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b76fb09ff961a3100b6a4bf890c1b12e6a0a2771
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092559"
---
# <a name="er-upgrade-your-format-by-adopting-a-new-base-version-of-that-format"></a><span data-ttu-id="035a6-103">Elektronické výkaznictví - Upgrade formátu přijetím nové základní verze tohoto formátu</span><span class="sxs-lookup"><span data-stu-id="035a6-103">ER Upgrade your format by adopting a new, base version of that format</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="035a6-104">Následující postup popisuje, jak uživatel s rolí Správce systému nebo Návrhář elektronického výkaznictví může spravovat konfiguraci formátu pro elektronické výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="035a6-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can maintain an Electronic reporting (ER) format configuration.</span></span> <span data-ttu-id="035a6-105">Tento odstavec vysvětluje, jakým způsobem lze vytvořit vlastní verzi formátu na základě formátu přijatého od poskytovatele konfigurace.</span><span class="sxs-lookup"><span data-stu-id="035a6-105">This procedure explains how a custom version of a format can be created based on the format received from a configuration provider (CP).</span></span> <span data-ttu-id="035a6-106">Také popisuje, jak přejmout novou základní verzi tohoto formátu.</span><span class="sxs-lookup"><span data-stu-id="035a6-106">It also explains how to adopt a new, base version of that format.</span></span>

<span data-ttu-id="035a6-107">K provedení těchto kroků musíte nejprve dokončit jednotlivé kroky v postupech "Vytvoření poskytovatele konfigurace a jeho označení jako aktivního" a "Použití vytvořeného formát pro generování elektronických dokumentů pro platby".</span><span class="sxs-lookup"><span data-stu-id="035a6-107">To complete these steps, you must first complete the steps in the "Create a configuration provider and mark it as active" and "Use created format to generate electronic documents for payments" procedures.</span></span> <span data-ttu-id="035a6-108">Tyto kroky lze provést v rámci společnosti GBSI.</span><span class="sxs-lookup"><span data-stu-id="035a6-108">These steps can be performed in the GBSI company.</span></span>

## <a name="select-format-configuration-for-customization"></a><span data-ttu-id="035a6-109">Výběr konfigurace formátu pro přizpůsobení</span><span class="sxs-lookup"><span data-stu-id="035a6-109">Select format configuration for customization</span></span>
1. <span data-ttu-id="035a6-110">Přejděte do části Správa organizace > Pracovní prostory > Elektronické výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="035a6-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>

    <span data-ttu-id="035a6-111">V tomto příkladu bude vzorová společnost Litware, Inc. (https://www.litware.com) bude sloužit jako poskytovatel konfigurace, který podporuje konfiguraci formátu pro elektronické platby pro určitou zemi.</span><span class="sxs-lookup"><span data-stu-id="035a6-111">In this example, sample company Litware, Inc. (https://www.litware.com) will act as a configuration provider that supports format configurations for electronic payments for a particular country.</span></span>    <span data-ttu-id="035a6-112">Vzorová společnost Proseware, Inc. (http://www.proseware.com) bude jednat jako příjemce konfigurace formátu, který Litware, Inc. poskytl.</span><span class="sxs-lookup"><span data-stu-id="035a6-112">Sample company Proseware, Inc. (http://www.proseware.com) will act as a consumer of the format configuration that Litware, Inc. provided.</span></span> <span data-ttu-id="035a6-113">Proseware, Inc. používá formáty v určitých oblastech v zemi.</span><span class="sxs-lookup"><span data-stu-id="035a6-113">Proseware, Inc. uses formats in certain regions of that country.</span></span>  
2. <span data-ttu-id="035a6-114">Klikněte na Konfigurace výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="035a6-114">Click Reporting configurations.</span></span>
3. <span data-ttu-id="035a6-115">Klepněte na tlačítko Zobrazit filtry.</span><span class="sxs-lookup"><span data-stu-id="035a6-115">Click Show filters.</span></span>
4. <span data-ttu-id="035a6-116">Použijte následující filtry: Do pole „Název" zadejte hodnotu filtru BACS (Velká Británie – fiktivní) a použijte operátor filtru „začíná na".</span><span class="sxs-lookup"><span data-stu-id="035a6-116">Apply the following filters: Enter a filter value of "BACS (UK fictitious)" on the "Name" field using the "begins with" filter operator.</span></span>
  
    <span data-ttu-id="035a6-117">Vybraná konfigurace formátu BACS (Velká Británie – fiktivní) je ve vlastnictví poskytovatele Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="035a6-117">The selected format configuration BACS (UK fictitious) is owned by provider Litware, Inc.</span></span>  

5. <span data-ttu-id="035a6-118">Klepněte na tlačítko Zobrazit filtry.</span><span class="sxs-lookup"><span data-stu-id="035a6-118">Click Show filters.</span></span>
6. <span data-ttu-id="035a6-119">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="035a6-119">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="035a6-120">Verze formátu se stavem Dokončeno bude použita společností Proseware, Inc. pro přizpůsobení.</span><span class="sxs-lookup"><span data-stu-id="035a6-120">The version of the format with the status of Completed will be used by Proseware, Inc. for customization.</span></span>  

## <a name="create-a-new-configuration-for-your-custom-format-of-electronic-document"></a><span data-ttu-id="035a6-121">Vytvoření nové konfigurace pro vlastní formát elektronického dokumentu</span><span class="sxs-lookup"><span data-stu-id="035a6-121">Create a new configuration for your custom format of electronic document</span></span>
<span data-ttu-id="035a6-122">Proseware, Inc. přijala verzi 1.1 konfigurace BACS (Velká Británie – fiktivní), která obsahuje původní formát pro generování dokumentů elektronických plateb od společnosti Litware, Inc. v souladu se svým předplatným služby.</span><span class="sxs-lookup"><span data-stu-id="035a6-122">Proseware, Inc. received version 1.1 of BACS (UK fictitious) configuration that contains the initial format to generate electronic payment documents from Litware, Inc. in accordance to their service subscription.</span></span> <span data-ttu-id="035a6-123">Proseware, Inc. chce začít používat tuto konfiguraci jako standard pro svou zemi, ale pro splnění zvláštních místních požadavků jsou požadována některá přizpůsobení.</span><span class="sxs-lookup"><span data-stu-id="035a6-123">Proseware, Inc. wants to start using this as a standard for their country but some customization is required to support specific regional requirements.</span></span> <span data-ttu-id="035a6-124">Proseware, Inc. chce také udržovat možnost upgradu vlastního formátu ihned, jakmile je k dispozici její nová verze (se změnami pro soulad s novými požadavky specifickými pro zemi) od společnosti Litware, Inc. a chtějí provést tento upgrade s co nejnižší cenou.</span><span class="sxs-lookup"><span data-stu-id="035a6-124">Proseware, Inc. also wants to keep the ability to upgrade a custom format as soon as a new version of it (with changes to support new country-specific requirements) comes from Litware, Inc. and they want to perform this upgrade with the lowest cost.</span></span>  

<span data-ttu-id="035a6-125">Aby to bylo možné, Proseware, Inc., potřebuje vytvořit konfiguraci pomocí konfigurace Litware, Inc. BACS (Velká Británie – fiktivní) jako její základ.</span><span class="sxs-lookup"><span data-stu-id="035a6-125">To do this, Proseware, Inc. needs to create a configuration using the Litware, Inc. configuration BACS (UK fictitious) as a base.</span></span>  

1. <span data-ttu-id="035a6-126">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="035a6-126">Close the page.</span></span>
2. <span data-ttu-id="035a6-127">Vyberte Proseware, Inc. a nastavte ji jako aktivního zprostředkovatele.</span><span class="sxs-lookup"><span data-stu-id="035a6-127">Select Proseware, Inc. to make it an active provider.</span></span>
3. <span data-ttu-id="035a6-128">Klikněte na možnost Nastavit jako aktivní.</span><span class="sxs-lookup"><span data-stu-id="035a6-128">Click Set active.</span></span>
4. <span data-ttu-id="035a6-129">Klikněte na Konfigurace výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="035a6-129">Click Reporting configurations.</span></span>
5. <span data-ttu-id="035a6-130">Ve stromovém zobrazení rozbalte možnost „Platby (zjednodušený model)“.</span><span class="sxs-lookup"><span data-stu-id="035a6-130">In the tree, expand 'Payments (simplified model)'.</span></span>
6. <span data-ttu-id="035a6-131">Ve stromovém zobrazení vyberte možnost „Platby (zjednodušený model)\BACS (Velká Británie – fiktivní)“.</span><span class="sxs-lookup"><span data-stu-id="035a6-131">In the tree, select 'Payments (simplified model)\BACS (UK fictitious)'.</span></span>

    <span data-ttu-id="035a6-132">VVyberte konfiguraci BACS (Velká Británie – fiktivní) od Litware, Inc. Proseware, Inc. použije verzi 1.1 jako základ pro vlastní verzi.</span><span class="sxs-lookup"><span data-stu-id="035a6-132">Select the BACS (UK fictitious) configuration from Litware, Inc. Proseware, Inc. will use version 1.1 as a base for the custom version.</span></span>  

7. <span data-ttu-id="035a6-133">Kliknutím na možnost Vytvořit konfiguraci otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="035a6-133">Click Create configuration to open the drop dialog.</span></span>

    <span data-ttu-id="035a6-134">To vám umožňuje vytvořit novou konfiguraci pro vlastní formát platby.</span><span class="sxs-lookup"><span data-stu-id="035a6-134">This lets you create a new configuration for a custom payment format.</span></span>  

8. <span data-ttu-id="035a6-135">Do pole Nový zadejte hodnotu „Odvodit z názvu: BACS (Velká Británie – fiktivní), Litware, Inc.“.</span><span class="sxs-lookup"><span data-stu-id="035a6-135">In the New field, enter 'Derive from Name: BACS (UK fictitious), Litware, Inc.'.</span></span>

    <span data-ttu-id="035a6-136">Výběrem možnosti Odvodit můžete potvrdit použití formátu BACS (Velká Británie – fiktivní) jako základ pro vytváření vlastní verze.</span><span class="sxs-lookup"><span data-stu-id="035a6-136">Select the Derive option to confirm the usage of BACS (UK fictitious) as the base for creating the custom version.</span></span>  

9. <span data-ttu-id="035a6-137">Do pole Název zadejte „BACS (Velká Británie – fiktivní vlastní)“.</span><span class="sxs-lookup"><span data-stu-id="035a6-137">In the Name field, type 'BACS (UK fictitious custom)'.</span></span>
10. <span data-ttu-id="035a6-138">Do pole Popis zadejte Platba dodavatele BACS (Velká Británie – fiktivní vlastní).</span><span class="sxs-lookup"><span data-stu-id="035a6-138">In the Description field, type 'BACS vendor payment (UK fictitious custom)'.</span></span>

    <span data-ttu-id="035a6-139">Aktivní poskytovatel konfigurace (Proseware, Inc.) se zadá automaticky v tomto poli.</span><span class="sxs-lookup"><span data-stu-id="035a6-139">The active configuration provider (Proseware, Inc.) is automatically entered here.</span></span> <span data-ttu-id="035a6-140">Tento zprostředkovatel bude moci udržovat tuto konfiguraci.</span><span class="sxs-lookup"><span data-stu-id="035a6-140">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="035a6-141">Jiní poskytovatelé mohou použít tuto konfiguraci, ale nebudou moci ji spravovat.</span><span class="sxs-lookup"><span data-stu-id="035a6-141">Other providers can use this configuration, but will not be able to maintain it.</span></span>  

11. <span data-ttu-id="035a6-142">Klepněte na možnost Vytvořit konfiguraci.</span><span class="sxs-lookup"><span data-stu-id="035a6-142">Click Create configuration.</span></span>

## <a name="customize-your-format-for-the-electronic-document"></a><span data-ttu-id="035a6-143">Přizpůsobení formátu elektronického dokumentu</span><span class="sxs-lookup"><span data-stu-id="035a6-143">Customize your format for the electronic document</span></span>
1. <span data-ttu-id="035a6-144">Klikněte na možnost Návrhář.</span><span class="sxs-lookup"><span data-stu-id="035a6-144">Click Designer.</span></span>
2. <span data-ttu-id="035a6-145">Klikněte na Rozbalit/sbalit.</span><span class="sxs-lookup"><span data-stu-id="035a6-145">Click Expand/collapse.</span></span>
3. <span data-ttu-id="035a6-146">Klikněte na Rozbalit/sbalit.</span><span class="sxs-lookup"><span data-stu-id="035a6-146">Click Expand/collapse.</span></span>
4. <span data-ttu-id="035a6-147">Ve stromové struktuře vyberte 'Xml\Zpráva\Platby\Položka\Dodavatel\Banka'.</span><span class="sxs-lookup"><span data-stu-id="035a6-147">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank'.</span></span>
5. <span data-ttu-id="035a6-148">Klepnutím na možnost Přidat otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="035a6-148">Click Add to open the drop dialog.</span></span>
6. <span data-ttu-id="035a6-149">Ve stromovém zobrazení vyberte „XML\Prvek“.</span><span class="sxs-lookup"><span data-stu-id="035a6-149">In the tree, select 'XML\Element'.</span></span>
7. <span data-ttu-id="035a6-150">Do pole Název zadejte IBAN.</span><span class="sxs-lookup"><span data-stu-id="035a6-150">In the Name field, type 'IBAN'.</span></span>
8. <span data-ttu-id="035a6-151">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="035a6-151">Click OK.</span></span>
9. <span data-ttu-id="035a6-152">Ve stromové struktuře vyberte 'Xml\Zpráva\Platby\Položka\Dodavatel\Banka\IBAN'.</span><span class="sxs-lookup"><span data-stu-id="035a6-152">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\IBAN'.</span></span>
10. <span data-ttu-id="035a6-153">Klepnutím na možnost Přidat otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="035a6-153">Click Add to open the drop dialog.</span></span>
11. <span data-ttu-id="035a6-154">Ve stromovém zobrazení vyberte „Text\Řetězec“.</span><span class="sxs-lookup"><span data-stu-id="035a6-154">In the tree, select 'Text\String'.</span></span>
12. <span data-ttu-id="035a6-155">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="035a6-155">Click OK.</span></span>
13. <span data-ttu-id="035a6-156">Ve stromové struktuře vyberte 'Xml\Zpráva\Platby\Položka\Dodavatel\Název\Řetězec'.</span><span class="sxs-lookup"><span data-stu-id="035a6-156">In the tree, select 'Xml\Message\Payments\Item\Vendor\Name\String'.</span></span>
14. <span data-ttu-id="035a6-157">Zadejte 60 do pole Maximální délka.</span><span class="sxs-lookup"><span data-stu-id="035a6-157">In the Maximum length field, enter '60'.</span></span>
15. <span data-ttu-id="035a6-158">Klikněte na kartu Mapování.</span><span class="sxs-lookup"><span data-stu-id="035a6-158">Click the Mapping tab.</span></span>
16. <span data-ttu-id="035a6-159">Ve stromovém zobrazení rozbalte „model“.</span><span class="sxs-lookup"><span data-stu-id="035a6-159">In the tree, expand 'model'.</span></span>
17. <span data-ttu-id="035a6-160">Ve stromovém zobrazení rozbalte „model\Platby“.</span><span class="sxs-lookup"><span data-stu-id="035a6-160">In the tree, expand 'model\Payments'.</span></span>
18. <span data-ttu-id="035a6-161">Ve stromovém zobrazení rozbalte „model\Platby\Věřitel“.</span><span class="sxs-lookup"><span data-stu-id="035a6-161">In the tree, expand 'model\Payments\Creditor'.</span></span>
19. <span data-ttu-id="035a6-162">Ve stromovém zobrazení rozbalte „model\Platby\Věřitel\Účet“.</span><span class="sxs-lookup"><span data-stu-id="035a6-162">In the tree, expand 'model\Payments\Creditor\Account'.</span></span>
20. <span data-ttu-id="035a6-163">Ve stromové struktuře vyberte 'model\Platby\Věřitel\Účet\IBAN'.</span><span class="sxs-lookup"><span data-stu-id="035a6-163">In the tree, select 'model\Payments\Creditor\Account\IBAN'.</span></span>
21. <span data-ttu-id="035a6-164">Ve stromové struktuře vyberte 'Xml\Zpráva\Platby\Položka =  model.Platby\Dodavatel\Banka\IBAN\Řetězec'.</span><span class="sxs-lookup"><span data-stu-id="035a6-164">In the tree, select 'Xml\Message\Payments\Item =  model.Payments\Vendor\Bank\IBAN\String'.</span></span>
22. <span data-ttu-id="035a6-165">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="035a6-165">Click Bind.</span></span>
23. <span data-ttu-id="035a6-166">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="035a6-166">Click Save.</span></span>

## <a name="validate-the-customized-format"></a><span data-ttu-id="035a6-167">Ověření přizpůsobeného formátu</span><span class="sxs-lookup"><span data-stu-id="035a6-167">Validate the customized format</span></span>
1. <span data-ttu-id="035a6-168">Klikněte na tlačítko Ověřit.</span><span class="sxs-lookup"><span data-stu-id="035a6-168">Click Validate.</span></span>

    <span data-ttu-id="035a6-169">Ověřte změny v přizpůsobeném rozvržení formátu a změnách v mapování dat a ujistěte se tak, že jsou všechny vazby v pořádku.</span><span class="sxs-lookup"><span data-stu-id="035a6-169">Validate the customized format layout and data mapping changes to make sure that all bindings are okay.</span></span>  

2. <span data-ttu-id="035a6-170">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="035a6-170">Close the page.</span></span>

## <a name="change-the-status-of-the-current-version-of-the-custom-format-configuration"></a><span data-ttu-id="035a6-171">Změna stavu aktuální verze vlastní konfigurace formátu</span><span class="sxs-lookup"><span data-stu-id="035a6-171">Change the status of the current version of the custom format configuration</span></span>
<span data-ttu-id="035a6-172">Změňte stav navržené konfigurace formátu z Návrh na Dokončeno, aby byla konfigurace dostupná pro generování platebního dokumentu.</span><span class="sxs-lookup"><span data-stu-id="035a6-172">Change the status of the designed format configuration from Draft to Completed to make it available for payment document generation.</span></span>  

1. <span data-ttu-id="035a6-173">Klikněte na položku Změnit stav.</span><span class="sxs-lookup"><span data-stu-id="035a6-173">Click Change status.</span></span>

    <span data-ttu-id="035a6-174">Všimněte si, že je aktuální verze vybrané konfigurace ve stavu Koncept.</span><span class="sxs-lookup"><span data-stu-id="035a6-174">Note that the current version of the selected configuration is in Draft status.</span></span>  

2. <span data-ttu-id="035a6-175">Klikněte na tlačítko Dokončit.</span><span class="sxs-lookup"><span data-stu-id="035a6-175">Click Complete.</span></span>
3. <span data-ttu-id="035a6-176">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="035a6-176">In the Description field, type a value.</span></span>
4. <span data-ttu-id="035a6-177">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="035a6-177">Click OK.</span></span>
5. <span data-ttu-id="035a6-178">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="035a6-178">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="035a6-179">Všimněte si, že je vytvořená konfigurace uložena jako dokončená verze 1.1.1.</span><span class="sxs-lookup"><span data-stu-id="035a6-179">Note that the created configuration is saved as completed version 1.1.1.</span></span> <span data-ttu-id="035a6-180">To znamená, že se jedná o 1. verzi vlastního formátu BACS (Velká Británie – fiktivní vlastní), která je založena na 1. verzi formátu BACS (Velká Británie – fiktivní), která je založena na 1. verzi datového modelu Platby (zjednodušený model).</span><span class="sxs-lookup"><span data-stu-id="035a6-180">This means it is version 1 of the custom BACS (UK fictitious custom) format, which is based on version 1 of the BACS (UK fictitious) format, which is based on version 1 of the Payments (simplified model) data model.</span></span>  

## <a name="test-the-customized-format-to-generate-payment-files"></a><span data-ttu-id="035a6-181">Test vlastního formátu pro generování souborů plateb</span><span class="sxs-lookup"><span data-stu-id="035a6-181">Test the customized format to generate payment files</span></span>
<span data-ttu-id="035a6-182">Postupujte podle kroků v postupu „Použití vytvořeného formátu pro generování elektronických dokumentů pro platby“ v rámci paralelní relace Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="035a6-182">Complete the steps in the "Use created format to generate electronic documents for payments" procedure in a parallel Finance and Operations session.</span></span> <span data-ttu-id="035a6-183">Vyberte formát BACS (Velká Británie – fiktivní vlastní) v parametrech metody elektronické platby.</span><span class="sxs-lookup"><span data-stu-id="035a6-183">Select the BACS (UK fictitious custom) format in electronic payment method parameters.</span></span> <span data-ttu-id="035a6-184">Zkontrolujte, že vytvořený soubor platby obsahuje nedávno uvedený uzel XML představující kód IBAN v souladu s místními požadavky.</span><span class="sxs-lookup"><span data-stu-id="035a6-184">Make sure that the created payment file contains the recently introduced XML node presenting IBAN code in accordance to regional requirements.</span></span>  

## <a name="update-the-existing-country-specific-configuration"></a><span data-ttu-id="035a6-185">Aktualizace existující konfigurace specifické pro zemi</span><span class="sxs-lookup"><span data-stu-id="035a6-185">Update the existing country-specific configuration</span></span>
<span data-ttu-id="035a6-186">Litware, Inc. musí aktualizovat konfiguraci BACS (Velká Británie – fiktivní) a přijmout nové požadavky země, aby mohla spravovat formát elektronického dokumentu.</span><span class="sxs-lookup"><span data-stu-id="035a6-186">Litware, Inc. needs to update the BACS (UK fictitious) configuration and adopt new country requirements for managing the format of the electronic document.</span></span> <span data-ttu-id="035a6-187">Později se toto stane součástí nové verze této konfigurace, která bude nabízena odběratelům služby, včetně společnosti Proseware, Inc.</span><span class="sxs-lookup"><span data-stu-id="035a6-187">Later, this will be enclosed in a new version of this configuration that will be offered for service subscribers, including Proseware, Inc.</span></span>  

<span data-ttu-id="035a6-188">Ve skutečném procesu poskytování služeb lze každou novou verzi BACS (Velká Británie – fiktivní) importovat společností Proseware, Inc. z úložiště souborů LCS poskytovatele Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="035a6-188">In real service provision related processes, each new version of BACS (UK fictitious) can be imported by Proseware, Inc. from Litware, Inc. configurations' LCS repository.</span></span> <span data-ttu-id="035a6-189">V tomto procesu budeme simulovat tento krok aktualizováním BACS (Velká Británie – fiktivní) jménem poskytovatele služby.</span><span class="sxs-lookup"><span data-stu-id="035a6-189">In this procedure we will simulate this by updating BACS (UK fictitious) on behalf of a service provider.</span></span>  

1. <span data-ttu-id="035a6-190">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="035a6-190">Close the page.</span></span>
2. <span data-ttu-id="035a6-191">Vyberte poskytovatele Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="035a6-191">Select Litware, inc. provider.</span></span>
3. <span data-ttu-id="035a6-192">Klikněte na možnost Nastavit jako aktivní.</span><span class="sxs-lookup"><span data-stu-id="035a6-192">Click Set active.</span></span>
4. <span data-ttu-id="035a6-193">Klikněte na Konfigurace výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="035a6-193">Click Reporting configurations.</span></span>
5. <span data-ttu-id="035a6-194">Ve stromovém zobrazení rozbalte možnost „Platby (zjednodušený model)“.</span><span class="sxs-lookup"><span data-stu-id="035a6-194">In the tree, expand 'Payments (simplified model)'.</span></span>
6. <span data-ttu-id="035a6-195">Ve stromovém zobrazení vyberte možnost „Platby (zjednodušený model)\BACS (Velká Británie – fiktivní)“.</span><span class="sxs-lookup"><span data-stu-id="035a6-195">In the tree, select 'Payments (simplified model)\BACS (UK fictitious)'.</span></span>

    <span data-ttu-id="035a6-196">Verze návrhu vlastněná poskytovatelem Litware, Inc. BACS (Velká Británie – fiktivní) bude zvolena pro zavedení změn podporujících nové požadavky specifické pro zemi.</span><span class="sxs-lookup"><span data-stu-id="035a6-196">The draft version owned by Litware, Inc. provider BACS (UK fictitious) is selected to bring in changes to support new country-specific requirements.</span></span>  

## <a name="localize-the-base-format-of-the-electronic-document"></a><span data-ttu-id="035a6-197">Lokalizace základního formátu elektronického dokumentu</span><span class="sxs-lookup"><span data-stu-id="035a6-197">Localize the base format of the electronic document</span></span>
<span data-ttu-id="035a6-198">Předpokládejme, že existují nové požadavky specifické pro zemi, které má Litware Inc. podporovat:</span><span class="sxs-lookup"><span data-stu-id="035a6-198">Assume that there are new country-specific requirements to be supported by Litware, Inc.:</span></span>  

- <span data-ttu-id="035a6-199">Hodnota kódu SWIFT banky věřitele v každé platební transakci.</span><span class="sxs-lookup"><span data-stu-id="035a6-199">A value for the creditor's bank SWIFT code in each payment transaction.</span></span>
- <span data-ttu-id="035a6-200">Limit 100 znaků pro délku textu s názvem dodavatele při generování souboru.</span><span class="sxs-lookup"><span data-stu-id="035a6-200">A limit of 100 characters for the length of text for the vendor's name in a generating file.</span></span>  
- <span data-ttu-id="035a6-201">Nové požadavky specifické pro zemi</span><span class="sxs-lookup"><span data-stu-id="035a6-201">New country-specific requirements</span></span>  
- <span data-ttu-id="035a6-202">Vyberte pracovní verzi požadované konfigurace pro zavedení požadovaných změn.</span><span class="sxs-lookup"><span data-stu-id="035a6-202">Select the draft version of the desired configuration to introduce required changes.</span></span>  


1. <span data-ttu-id="035a6-203">Klikněte na možnost Návrhář.</span><span class="sxs-lookup"><span data-stu-id="035a6-203">Click Designer.</span></span>
2. <span data-ttu-id="035a6-204">Klikněte na Rozbalit/sbalit.</span><span class="sxs-lookup"><span data-stu-id="035a6-204">Click Expand/collapse.</span></span>
3. <span data-ttu-id="035a6-205">Klikněte na Rozbalit/sbalit.</span><span class="sxs-lookup"><span data-stu-id="035a6-205">Click Expand/collapse.</span></span>
4. <span data-ttu-id="035a6-206">Ve stromové struktuře vyberte 'Xml\Zpráva\Platby\Položka\Dodavatel\Banka'.</span><span class="sxs-lookup"><span data-stu-id="035a6-206">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank'.</span></span>
5. <span data-ttu-id="035a6-207">Klepnutím na možnost Přidat otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="035a6-207">Click Add to open the drop dialog.</span></span>
6. <span data-ttu-id="035a6-208">Ve stromovém zobrazení vyberte „XML\Prvek“.</span><span class="sxs-lookup"><span data-stu-id="035a6-208">In the tree, select 'XML\Element'.</span></span>
7. <span data-ttu-id="035a6-209">Do pole Název zadejte SWIFT.</span><span class="sxs-lookup"><span data-stu-id="035a6-209">In the Name field, type 'SWIFT'.</span></span>
8. <span data-ttu-id="035a6-210">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="035a6-210">Click OK.</span></span>
9. <span data-ttu-id="035a6-211">Ve stromové struktuře vyberte 'Xml\Zpráva\Platby\Položka\Dodavatel\Banka\SWIFT'.</span><span class="sxs-lookup"><span data-stu-id="035a6-211">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\SWIFT'.</span></span>
10. <span data-ttu-id="035a6-212">Klepnutím na možnost Přidat otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="035a6-212">Click Add to open the drop dialog.</span></span>
11. <span data-ttu-id="035a6-213">Ve stromovém zobrazení vyberte „Text\Řetězec“.</span><span class="sxs-lookup"><span data-stu-id="035a6-213">In the tree, select 'Text\String'.</span></span>
12. <span data-ttu-id="035a6-214">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="035a6-214">Click OK.</span></span>
13. <span data-ttu-id="035a6-215">Ve stromové struktuře vyberte 'Xml\Zpráva\Platby\Položka\Dodavatel\Název\Řetězec'.</span><span class="sxs-lookup"><span data-stu-id="035a6-215">In the tree, select 'Xml\Message\Payments\Item\Vendor\Name\String'.</span></span>
14. <span data-ttu-id="035a6-216">Zadejte 100 do pole Maximální délka.</span><span class="sxs-lookup"><span data-stu-id="035a6-216">In the Maximum length field, enter '100'.</span></span>
15. <span data-ttu-id="035a6-217">Klikněte na kartu Mapování.</span><span class="sxs-lookup"><span data-stu-id="035a6-217">Click the Mapping tab.</span></span>
16. <span data-ttu-id="035a6-218">Ve stromovém zobrazení rozbalte „model“.</span><span class="sxs-lookup"><span data-stu-id="035a6-218">In the tree, expand 'model'.</span></span>
17. <span data-ttu-id="035a6-219">Ve stromovém zobrazení rozbalte „model\Platby“.</span><span class="sxs-lookup"><span data-stu-id="035a6-219">In the tree, expand 'model\Payments'.</span></span>
18. <span data-ttu-id="035a6-220">Ve stromovém zobrazení rozbalte „model\Platby\Věřitel“.</span><span class="sxs-lookup"><span data-stu-id="035a6-220">In the tree, expand 'model\Payments\Creditor'.</span></span>
19. <span data-ttu-id="035a6-221">Ve stromovém zobrazení rozbalte „model\Platby\Věřitel\Zástupce“.</span><span class="sxs-lookup"><span data-stu-id="035a6-221">In the tree, expand 'model\Payments\Creditor\Agent'.</span></span>
20. <span data-ttu-id="035a6-222">Ve stromové struktuře vyberte 'model\Platby\Věřitel\Agent\SWIFT'.</span><span class="sxs-lookup"><span data-stu-id="035a6-222">In the tree, select 'model\Payments\Creditor\Agent\SWIFT'.</span></span>
21. <span data-ttu-id="035a6-223">Ve stromové struktuře vyberte 'Xml\Zpráva\Platby\Položka =  model.Platby\Dodavatel\Banka\SWIFT\String'.</span><span class="sxs-lookup"><span data-stu-id="035a6-223">In the tree, select 'Xml\Message\Payments\Item =  model.Payments\Vendor\Bank\SWIFT\String'.</span></span>
22. <span data-ttu-id="035a6-224">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="035a6-224">Click Bind.</span></span>
23. <span data-ttu-id="035a6-225">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="035a6-225">Click Save.</span></span>

## <a name="validate-the-localized-format"></a><span data-ttu-id="035a6-226">Ověření lokalizovaného formátu</span><span class="sxs-lookup"><span data-stu-id="035a6-226">Validate the localized format</span></span>
1. <span data-ttu-id="035a6-227">Klikněte na tlačítko Ověřit.</span><span class="sxs-lookup"><span data-stu-id="035a6-227">Click Validate.</span></span>
2. <span data-ttu-id="035a6-228">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="035a6-228">Close the page.</span></span>

## <a name="change-the-status-of-the-current-version-of-the-base-format-configuration"></a><span data-ttu-id="035a6-229">Změna stavu aktuální verze konfigurace základního formátu</span><span class="sxs-lookup"><span data-stu-id="035a6-229">Change the status of the current version of the base format configuration</span></span>
<span data-ttu-id="035a6-230">Změňte stav aktualizované konfigurace základní formátu z Návrh na Dokončeno, aby byla k dispozici pro generování platebních dokladů a aktualizace konfigurace formátu, které jsou od ní odvozeny.</span><span class="sxs-lookup"><span data-stu-id="035a6-230">Change the status of the updated base format configuration from Draft to Completed to make it available for generation of payment documents and updates of format configurations derived from it.</span></span>  

1. <span data-ttu-id="035a6-231">Klikněte na položku Změnit stav.</span><span class="sxs-lookup"><span data-stu-id="035a6-231">Click Change status.</span></span>

    <span data-ttu-id="035a6-232">Všimněte si, že je aktuální verze vybrané konfigurace ve stavu Koncept.</span><span class="sxs-lookup"><span data-stu-id="035a6-232">Note that the current version of the selected configuration is in Draft status.</span></span>  

2. <span data-ttu-id="035a6-233">Klikněte na tlačítko Dokončit.</span><span class="sxs-lookup"><span data-stu-id="035a6-233">Click Complete.</span></span>
3. <span data-ttu-id="035a6-234">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="035a6-234">In the Description field, type a value.</span></span>
4. <span data-ttu-id="035a6-235">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="035a6-235">Click OK.</span></span>
5. <span data-ttu-id="035a6-236">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="035a6-236">In the list, find and select the desired record.</span></span>

## <a name="change-the-base-version-for-the-custom-format-configuration"></a><span data-ttu-id="035a6-237">Změna základní verze konfigurace vlastního formátu</span><span class="sxs-lookup"><span data-stu-id="035a6-237">Change the base version for the custom format configuration</span></span>

<span data-ttu-id="035a6-238">Proseware, Inc. je informován, že je k dispozici nová verze 1.2 konfigurace BACS (Velká Británie – fiktivní) pro generování dokumentů elektronických plateb podle naposledy ohlášených požadavků specifických pro zemi.</span><span class="sxs-lookup"><span data-stu-id="035a6-238">Proseware, Inc. is informed that a new version 1.2 of BACS (UK fictitious) configuration is available to generate electronic payment documents in accordance to recently announced country-specific requirements.</span></span> <span data-ttu-id="035a6-239">Proseware, Inc. chce začít ji používat jako standard pro danou zemi.</span><span class="sxs-lookup"><span data-stu-id="035a6-239">Proseware, Inc. wants to start using it as a standard for the country.</span></span>  

<span data-ttu-id="035a6-240">Aby to bylo možné, Proseware, Inc. musí změnit základní verzi konfigurace pro vlastní konfiguraci BACS (Velká Británie – fiktivní vlastní).</span><span class="sxs-lookup"><span data-stu-id="035a6-240">To do this, Proseware, Inc. needs to change the base configuration version for the custom configuration BACS (UK fictitious custom).</span></span> <span data-ttu-id="035a6-241">Namísto verze 1.1 BACS (Velká Británie – fiktivní) použije novou verzi 1.2.</span><span class="sxs-lookup"><span data-stu-id="035a6-241">Instead of version 1.1 of BACS (UK fictitious) use new version 1.2.</span></span>  

1. <span data-ttu-id="035a6-242">Přejděte do části Správa organizace > Pracovní prostory > Elektronické výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="035a6-242">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="035a6-243">Vyberte Proseware, Inc. jako zprostředkovatele a označte ho jako aktivního.</span><span class="sxs-lookup"><span data-stu-id="035a6-243">Select the Proseware, Inc. provider to mark it as active.</span></span>
3. <span data-ttu-id="035a6-244">Klikněte na možnost Nastavit jako aktivní.</span><span class="sxs-lookup"><span data-stu-id="035a6-244">Click Set active.</span></span>
4. <span data-ttu-id="035a6-245">Klikněte na Konfigurace výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="035a6-245">Click Reporting configurations.</span></span>
5. <span data-ttu-id="035a6-246">Ve stromovém zobrazení rozbalte možnost „Platby (zjednodušený model)“.</span><span class="sxs-lookup"><span data-stu-id="035a6-246">In the tree, expand 'Payments (simplified model)'.</span></span>
6. <span data-ttu-id="035a6-247">Ve stromovém zobrazení rozbalte možnost „Platby (zjednodušený model)\BACS (Velká Británie – fiktivní)“.</span><span class="sxs-lookup"><span data-stu-id="035a6-247">In the tree, expand 'Payments (simplified model)\BACS (UK fictitious)'.</span></span>
7. <span data-ttu-id="035a6-248">Ve stromovém zobrazení vyberte možnost „Platby (zjednodušený model)\BACS (Velká Británie – fiktivní)\BACS (Velká Británie – fiktivní vlastní)“.</span><span class="sxs-lookup"><span data-stu-id="035a6-248">In the tree, select 'Payments (simplified model)\BACS (UK fictitious)\BACS (UK fictitious custom)'.</span></span>

    <span data-ttu-id="035a6-249">Vyberte konfiguraci BACS (Velká Británie – fiktivní vlastní), která je ve vlastnictví Proseware, Inc.</span><span class="sxs-lookup"><span data-stu-id="035a6-249">Select the BACS (UK fictitious custom) configuration, which is owned by Proseware, Inc.</span></span>  

    <span data-ttu-id="035a6-250">Použijte pracovní verzi vybrané konfigurace pro zavedení požadovaných změn.</span><span class="sxs-lookup"><span data-stu-id="035a6-250">Use the draft version of the selected configuration to introduce required changes.</span></span>  

8. <span data-ttu-id="035a6-251">Klepněte na Přeskládání.</span><span class="sxs-lookup"><span data-stu-id="035a6-251">Click Rebase.</span></span>

    <span data-ttu-id="035a6-252">Vyberte novou verzi 1.2 základní konfigurace, která bude použita jako nový základ pro aktualizaci konfigurace.</span><span class="sxs-lookup"><span data-stu-id="035a6-252">Select the new version 1.2 of the base configuration to be applied as a new base for updating the configuration.</span></span>  

9. <span data-ttu-id="035a6-253">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="035a6-253">Click OK.</span></span>

    <span data-ttu-id="035a6-254">Všimněte si, že byly zjištěny některé konflikty během slučování vlastní verze a nové základní verze, jako jsou změny formátu, které nelze sloučit automaticky.</span><span class="sxs-lookup"><span data-stu-id="035a6-254">Note that some conflicts have been discovered between merging the custom version and a new base version representing some format changes that can't be merged automatically.</span></span>  

## <a name="resolve-rebase-conflicts"></a><span data-ttu-id="035a6-255">Řešení konfliktů přeskládání</span><span class="sxs-lookup"><span data-stu-id="035a6-255">Resolve rebase conflicts</span></span>
1. <span data-ttu-id="035a6-256">Klikněte na možnost Návrhář.</span><span class="sxs-lookup"><span data-stu-id="035a6-256">Click Designer.</span></span>
    
    <span data-ttu-id="035a6-257">Povšimněte si změn v limitu délky textu s názvem dodavatele, které nelze provést automaticky.</span><span class="sxs-lookup"><span data-stu-id="035a6-257">Note that changes to the vendor's name text length limit couldn't be resolved automatically.</span></span> <span data-ttu-id="035a6-258">Tyto informace jsou uvedeny v seznamu konfliktů.</span><span class="sxs-lookup"><span data-stu-id="035a6-258">Therefore, this is presented in a conflicts list.</span></span> <span data-ttu-id="035a6-259">Pro každý konflikt typu Aktualizace existují tyto možnosti: - Použít předchozí základní hodnotu (tlačítko v horní části mřížky) a vyvolat předchozí hodnotu základní verze (0 v tomto případě).</span><span class="sxs-lookup"><span data-stu-id="035a6-259">For each conflict of type Update, the following options are available:  - Apply a prior base value (button on top of the grid) to bring in the previous base version value (0 in our case).</span></span>  <span data-ttu-id="035a6-260">- Použít základní hodnotu (tlačítko v horní části mřížky) a vyvolat novou hodnotu základní verze (100 v tomto případě).</span><span class="sxs-lookup"><span data-stu-id="035a6-260">- Apply a base value (button on top of the grid) to bring in the new base version value (100 in our case).</span></span>  <span data-ttu-id="035a6-261">- Udržujte vlastní hodnotu (vlastní) (60 v tomto případě).</span><span class="sxs-lookup"><span data-stu-id="035a6-261">- Keep your own (custom) value (60 in our case).</span></span>  <span data-ttu-id="035a6-262">Kliknutím na tlačítko Použít použijte pro délku s textovým názvem dodavatele limit 100 znaků (pro konkrétní zemi).</span><span class="sxs-lookup"><span data-stu-id="035a6-262">Click Apply base value to apply a country-specific limit of 100 characters for vendor's name text length.</span></span>  

    <span data-ttu-id="035a6-263">Všimněte si, že Proseware, Inc. and Litware, Inc mají vlastní a místní verze formátu využívající kódy IBAN a SWIFT se souvisejícími součástmi, které jsou automaticky sloučeny v rámci správy formátu.</span><span class="sxs-lookup"><span data-stu-id="035a6-263">Note that Proseware, Inc. and Litware, Inc. have custom and local versions of this format using IBAN and SWIFT codes with related components that are automatically merged in the managing format.</span></span>  

2. <span data-ttu-id="035a6-264">Klikněte na Použít základní hodnotu.</span><span class="sxs-lookup"><span data-stu-id="035a6-264">Click Apply base value.</span></span>

    <span data-ttu-id="035a6-265">Kliknutím na tlačítko Použít použijte pro názvy dodavatele limit 100 znaků (pro konkrétní zemi).</span><span class="sxs-lookup"><span data-stu-id="035a6-265">Click Apply base value to apply the country-specific limit of 100 characters for vendor names.</span></span>  

3. <span data-ttu-id="035a6-266">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="035a6-266">Click Save.</span></span>

    <span data-ttu-id="035a6-267">Uložením formátu dojde k odstranění vyřešených konfliktů ze seznamu konfliktů.</span><span class="sxs-lookup"><span data-stu-id="035a6-267">Saving the format will remove resolved conflicts from the conflicts list.</span></span>  

4. <span data-ttu-id="035a6-268">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="035a6-268">Close the page.</span></span>

## <a name="change-the-status-of-the-new-version-of-the-custom-format-configuration"></a><span data-ttu-id="035a6-269">Změna stavu nové verze vlastní konfigurace formátu</span><span class="sxs-lookup"><span data-stu-id="035a6-269">Change the status of the new version of the custom format configuration</span></span>
1. <span data-ttu-id="035a6-270">Klikněte na položku Změnit stav.</span><span class="sxs-lookup"><span data-stu-id="035a6-270">Click Change status.</span></span>

    <span data-ttu-id="035a6-271">Změňte stav aktualizované vlastní konfigurace formátu z Koncept na Dokončeno.</span><span class="sxs-lookup"><span data-stu-id="035a6-271">Change the status of the updated, custom format configuration from Draft to Completed.</span></span> <span data-ttu-id="035a6-272">To zpřístupní konfiguraci formátu pro generování platebních dokumentů.</span><span class="sxs-lookup"><span data-stu-id="035a6-272">This will make the format configuration available for generating payment documents.</span></span> <span data-ttu-id="035a6-273">Všimněte si, že je aktuální verze vybrané konfigurace ve stavu Koncept.</span><span class="sxs-lookup"><span data-stu-id="035a6-273">Note that the current version of the selected configuration is in Draft status.</span></span>  

2. <span data-ttu-id="035a6-274">Klikněte na tlačítko Dokončit.</span><span class="sxs-lookup"><span data-stu-id="035a6-274">Click Complete.</span></span>
3. <span data-ttu-id="035a6-275">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="035a6-275">In the Description field, type a value.</span></span>
4. <span data-ttu-id="035a6-276">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="035a6-276">Click OK.</span></span>

    <span data-ttu-id="035a6-277">Všimněte si, že vytvořená konfigurace je uložena jako dokončená verze 1.2.2: 2. verze základního formátu BACS (Velká Británie – fiktivní vlastní), který je založen na 2. verzi základního formátu BACS (Velká Británie – fiktivní), která je založena na modelu dat 1. verze plateb (zjednodušený model).</span><span class="sxs-lookup"><span data-stu-id="035a6-277">Note that the created configuration is saved as completed version 1.2.2: version 2 of base BACS (UK fictitious custom) format, which is based on version 2 of base BACS (UK fictitious) format, which is based on version 1 of Payments (simplified model) data model.</span></span>  

## <a name="test-the-customized-format-for-payment-files-generation"></a><span data-ttu-id="035a6-278">Test vlastního formátu pro generování souborů plateb</span><span class="sxs-lookup"><span data-stu-id="035a6-278">Test the customized format for payment files generation</span></span>
<span data-ttu-id="035a6-279">Postupujte podle kroků v postupu „Použití vytvořeného formátu pro generování elektronických dokumentů pro platby“ v rámci paralelní relace Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="035a6-279">Complete the steps in the "Use created format to generate electronic documents for payments" procedure in parallel Finance and Operations session.</span></span> <span data-ttu-id="035a6-280">Vyberte vytvořený formát 'BACS (Velká Británie – fiktivní vlastní)' v parametrech metody elektronické platby.</span><span class="sxs-lookup"><span data-stu-id="035a6-280">Select the created 'BACS (UK fictitious custom)' format in electronic payment method parameters.</span></span> <span data-ttu-id="035a6-281">Zkontrolujte, že vytvořený soubor platby obsahuje nedávno uvedený uzel XML společností by Proseware, Inc. představující kód účtu IBAN v souladu s místními požadavky.</span><span class="sxs-lookup"><span data-stu-id="035a6-281">Make sure that the created payment file contains recently introduced by Proseware, Inc. XML node presenting IBAN account code in accordance to regional requirements.</span></span> <span data-ttu-id="035a6-282">Soubor by rovněž měl obsahovat nedávno uvedených uzel XML uvedený společností Litware, Inc. představující bankovní kód SWIFT podle požadavků země.</span><span class="sxs-lookup"><span data-stu-id="035a6-282">The file also should contain the recently introduced by Litware, Inc. XML node presenting SWIFT bank code in accordance to country requirements.</span></span>  

