---
title: Návrh konfigurace pro generování dokumentů ve formátu Excel
description: Toto téma poskytuje informace o tom, jak navrhnout formát elektronického výkaznictví tak, aby vyplnil šablonu Excel, a poté vygenerovat odchozí dokumenty ve formátu Excel.
author: NickSelin
manager: AnnBe
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: EROperationDesigner, ERParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e889b08f10c5d0c95fed7c9e422340706bdd154a
ms.sourcegitcommit: 67ce81c57194afb26a04ae4c0b7509e0efa32afc
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/14/2020
ms.locfileid: "3375806"
---
# <a name="design-a-configuration-for-generating-documents-in-excel-format"></a><span data-ttu-id="97a29-103">Návrh konfigurace pro generování dokumentů ve formátu Excel</span><span class="sxs-lookup"><span data-stu-id="97a29-103">Design a configuration for generating documents in Excel format</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="97a29-104">Můžete navrhnout konfiguraci formátu [elektronického výkaznictví](general-electronic-reporting.md), která má [součást formátu](general-electronic-reporting.md#FormatComponentOutbound) elektronického výkaznictví, kterou můžete nakonfigurovat tak, aby generovala odchozí dokument ve formátu Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="97a29-104">You can design an [Electronic reporting (ER)](general-electronic-reporting.md) format configuration that has an ER [format component](general-electronic-reporting.md#FormatComponentOutbound) that you can configure to generate an outbound document in a Microsoft Excel workbook format.</span></span> <span data-ttu-id="97a29-105">K tomuto účelu musí být použity specifické komponenty formátu elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="97a29-105">Specific ER format components must be used for this purpose.</span></span>

<span data-ttu-id="97a29-106">Chcete-li se o této funkci dozvědět více, postupujte podle kroků v tématu [Návrh konfigurace pro generování sestav ve formátu OPENXML](tasks/er-design-reports-openxml-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="97a29-106">To learn more about this feature, follow the steps in the topic, [Design a configuration for generating reports in OPENXML format](tasks/er-design-reports-openxml-2016-11.md).</span></span>

## <a name="add-a-new-er-format"></a><span data-ttu-id="97a29-107">Přidání nového formátu elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="97a29-107">Add a new ER format</span></span>

<span data-ttu-id="97a29-108">Při přidání nové konfigurace formátu elektronického výkaznictví pro generování odchozího dokument ve formátu sešitu Excel musíte vybrat hodnotu **Excel** pro atribut formátu **Typ formátu** nebo ponechat atribut **Typ formátu** prázdný.</span><span class="sxs-lookup"><span data-stu-id="97a29-108">When you add a new ER format configuration to generate an outbound document in an Excel workbook format, you must either select the **Excel** value for the **Format type** attribute of the format or leave the **Format type** attribute blank.</span></span>

- <span data-ttu-id="97a29-109">Pokud vyberete **Excel**, můžete nakonfigurovat formát tak, aby generoval odchozí dokument pouze ve formátu Excel.</span><span class="sxs-lookup"><span data-stu-id="97a29-109">If you select **Excel**, you can configure the format to generate an outbound document only in Excel format.</span></span>
- <span data-ttu-id="97a29-110">Pokud atribut necháte prázdný, můžete nakonfigurovat formát tak, aby generoval odchozí dokument v libovolném formátu, který je podporován rámcem elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="97a29-110">If you leave the attribute blank, you can configure the format to generate an outbound document in any format that is supported by the ER framework.</span></span>

<span data-ttu-id="97a29-111">Chcete-li nakonfigurovat komponentu formátu elektronického výkaznictví, vyberte v podokně akcí možnost **Návrhář** a otevřete komponentu formátu elektronického výkaznictví pro úpravy v návrháři operací elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="97a29-111">To configure the ER format component of the configuration, select **Designer** on the Action Pane, and open the ER format component for editing in the ER Operation designer.</span></span>

![Stránka Konfigurace](./media/er-excel-format-add-format.png)

## <a name="excel-file-component"></a><span data-ttu-id="97a29-113">Součást souboru Excel</span><span class="sxs-lookup"><span data-stu-id="97a29-113">Excel file component</span></span>

### <a name="manual-entry"></a><span data-ttu-id="97a29-114">Ruční zadání</span><span class="sxs-lookup"><span data-stu-id="97a29-114">Manual entry</span></span>

<span data-ttu-id="97a29-115">Musíte přidat komponentu **Excel\\Soubor** do nakonfigurovaného formátu elektronického výkaznictví pro generování odchozího dokumentu ve formátu Excel.</span><span class="sxs-lookup"><span data-stu-id="97a29-115">You must add an **Excel\\File** component to the configured ER format to generate an outbound document in Excel format.</span></span>

![Součást Excel\Soubor](./media/er-excel-format-add-file-component.png)

<span data-ttu-id="97a29-117">Chcete-li určit rozvržení odchozího dokumentu, připojte sešit aplikace Excel, který má příponu .xlsx k součásti **Excel\\Soubor**, jako šablonu pro odchozí dokumenty.</span><span class="sxs-lookup"><span data-stu-id="97a29-117">To specify the layout of the outbound document, attach an Excel workbook that has the .xlsx extension to the **Excel\\File** component as the template for outbound documents.</span></span>

> [!NOTE]
> <span data-ttu-id="97a29-118">Když ručně připojíte šablonu, musíte použít [typ dokumentu](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types), který byl za tímto účelem nakonfigurován v [parametrech elektronického výkaznictví](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents).</span><span class="sxs-lookup"><span data-stu-id="97a29-118">When you manually attach a template, you must use a [document type](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) that has been configured for that purpose in the [ER parameters](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents).</span></span>

![Přidání přílohy ke komponentě Excel\Soubor](./media/er-excel-format-add-file-component2.png)

<span data-ttu-id="97a29-120">Chcete-li určit, jak bude připojená šablona vyplněna při spuštění konfigurovaného formátu elektronického výkaznictví, musíte přidat vnořené komponenty **List**, **Rozsah** a **Buňka** k součásti **Excel\\Soubor**.</span><span class="sxs-lookup"><span data-stu-id="97a29-120">To specify how the attached template will be filled in when you run the configured ER format, you must add nested **Sheet**, **Range**, and **Cell** components to the **Excel\\File** component.</span></span> <span data-ttu-id="97a29-121">Každá vnořená součást musí být přidružena l položce s názvem Excel.</span><span class="sxs-lookup"><span data-stu-id="97a29-121">Each nested component must be associated with an Excel named item.</span></span>

### <a name="template-import"></a><span data-ttu-id="97a29-122">Import šablony</span><span class="sxs-lookup"><span data-stu-id="97a29-122">Template import</span></span>

<span data-ttu-id="97a29-123">Můžete vybrat možnost **Importovat z Excelu** na kartě podokna akcí **Importovat** a naimportovat novou šablonu do prázdného formátu elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="97a29-123">You can select **Import from Excel** on the **Import** tab of the Action Pane to import a new template into a blank ER format.</span></span> <span data-ttu-id="97a29-124">V tomto příkladu bude součást **Excel\\Soubor** vytvořena automaticky a k ní bude připojena importovaná šablona.</span><span class="sxs-lookup"><span data-stu-id="97a29-124">In this example, an **Excel\\File** component will be created automatically, and the imported template will be attached to it.</span></span> <span data-ttu-id="97a29-125">Všechny požadované komponenty elektronického výkaznictví budou také vytvořeny automaticky na základě nalezených položek s názvem Excel.</span><span class="sxs-lookup"><span data-stu-id="97a29-125">All required ER components will also be created automatically, based on the list of Excel named items that are discovered.</span></span>

![Volba možnosti Importovat z Excelu](./media/er-excel-format-import-template.png)

> [!NOTE]
> <span data-ttu-id="97a29-127">Pokud chcete vytvořit volitelný prvek **List** v editovatelném formátu elektronického výkaznictví, nastavte možnost **Vytvořit prvek formátu listu Excel** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="97a29-127">If you want to create the optional **Sheet** element in the editable ER format, set the **Create Excel Sheet format element** option to **Yes**.</span></span>

## <a name="sheet-component"></a><span data-ttu-id="97a29-128">Komponenta listu</span><span class="sxs-lookup"><span data-stu-id="97a29-128">Sheet component</span></span>

<span data-ttu-id="97a29-129">Komponenta **List** označuje pracovní list přiloženého sešitu aplikace Excel, který musí být vyplněn.</span><span class="sxs-lookup"><span data-stu-id="97a29-129">The **Sheet** component indicates a worksheet of the attached Excel workbook that must be filled in.</span></span> <span data-ttu-id="97a29-130">Název listu v šabloně Excel je definován ve vlastnosti **List** této komponenty.</span><span class="sxs-lookup"><span data-stu-id="97a29-130">The name of the worksheet in an Excel template is defined in the **Sheet** property of this component.</span></span>

> [!NOTE]
> <span data-ttu-id="97a29-131">Tato součást je volitelná pro sešity aplikace Excel, které obsahují jeden list.</span><span class="sxs-lookup"><span data-stu-id="97a29-131">This component is optional for Excel workbooks that contain a single worksheet.</span></span>

<span data-ttu-id="97a29-132">Na kartě **Mapování** návrháře operací elektronického výkaznictví můžete nakonfigurovat vlastnost **Povoleno** pro součást **List** k určení, zda musí být komponenta vložena do vygenerovaného dokumentu:</span><span class="sxs-lookup"><span data-stu-id="97a29-132">On the **Mapping** tab of the ER Operation designer, you can configure the **Enabled** property for a **Sheet** component to specify whether the component must be put in a generated document:</span></span>

- <span data-ttu-id="97a29-133">Pokud je výraz vlastnosti **Povoleno** nakonfigurován pro vrácení hodnoty **True** za běhu, nebo pokud není vůbec nakonfigurován žádný výraz, bude do vygenerovaného dokumentu vložen příslušný list.</span><span class="sxs-lookup"><span data-stu-id="97a29-133">If an expression of the **Enabled** property is configured to return **True** at runtime, or if no expression is configured at all, the appropriate worksheet will be put in the generated document.</span></span>
- <span data-ttu-id="97a29-134">Pokud je výraz vlastnosti **Povoleno** nakonfigurován pro vrácení hodnoty **False** za běhu, vygenerovaný dokument nebude obsahovat pracovní list.</span><span class="sxs-lookup"><span data-stu-id="97a29-134">If an expression of the **Enabled** property is configured to return **False** at runtime, the generated document won't contain a worksheet.</span></span>

![Příklad součásti listu](./media/er-excel-format-sheet-component.png)

## <a name="range-component"></a><span data-ttu-id="97a29-136">Součást rozsahu</span><span class="sxs-lookup"><span data-stu-id="97a29-136">Range component</span></span>

<span data-ttu-id="97a29-137">Součást **Rozsah** označuje rozsah Excelu, který musí být ovládán touto součástí elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="97a29-137">The **Range** component indicates an Excel range that must be controlled by this ER component.</span></span> <span data-ttu-id="97a29-138">Název rozsahu je definován ve vlastnosti **Rozsah aplikace Excel** této komponenty.</span><span class="sxs-lookup"><span data-stu-id="97a29-138">The name of the range is defined in the **Excel range** property of this component.</span></span>

<span data-ttu-id="97a29-139">Vlastnost **Směr replikace** určuje, zda a jak bude rozsah opakován v generovaném dokumentu:</span><span class="sxs-lookup"><span data-stu-id="97a29-139">The **Replication direction** property specifies whether and how the range will be repeated in a generated document:</span></span>

- <span data-ttu-id="97a29-140">Pokud je vlastnost **Směr replikace** nastavena na **Žádná replikace**, příslušný rozsah aplikace Excel nebude ve vygenerovaném dokumentu opakován.</span><span class="sxs-lookup"><span data-stu-id="97a29-140">If the **Replication direction** property is set to **No replication**, the appropriate Excel range won't be repeated in the generated document.</span></span>
- <span data-ttu-id="97a29-141">Pokud je vlastnost **Směr replikace** nastavena na **Vertikální**, příslušný rozsah aplikace Excel bude ve vygenerovaném dokumentu opakován.</span><span class="sxs-lookup"><span data-stu-id="97a29-141">If the **Replication direction** property is set to **Vertical**, the appropriate Excel range will be repeated in the generated document.</span></span> <span data-ttu-id="97a29-142">Každý replikovaný rozsah je umístěn pod původní rozsah v šabloně Excel.</span><span class="sxs-lookup"><span data-stu-id="97a29-142">Every replicated range is put below the original range in an Excel template.</span></span> <span data-ttu-id="97a29-143">Počet opakování je definován počtem záznamů ve zdroji dat typu **Seznam záznamů**, který je vázán na tuto součást elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="97a29-143">The number of repetitions is defined by the number of records in a data source of the **Record list** type that is bound to this ER component.</span></span>
- <span data-ttu-id="97a29-144">Pokud je vlastnost **Směr replikace** nastavena na **Horizontální**, příslušný rozsah aplikace Excel bude ve vygenerovaném dokumentu opakován.</span><span class="sxs-lookup"><span data-stu-id="97a29-144">If the **Replication direction** property is set to **Horizontal**, the appropriate Excel range will be repeated in the generated document.</span></span> <span data-ttu-id="97a29-145">Každý replikovaný rozsah je umístěn napravo od původního rozsahu v šabloně Excel.</span><span class="sxs-lookup"><span data-stu-id="97a29-145">Every replicated range is put to the right of the original range in an Excel template.</span></span> <span data-ttu-id="97a29-146">Počet opakování je definován počtem záznamů ve zdroji dat typu **Seznam záznamů**, který je vázán na tuto součást elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="97a29-146">The number of repetitions is defined by the number of records in a data source of the **Record list** type that is bound to this ER component.</span></span>

<span data-ttu-id="97a29-147">Chcete-li se dozvědět více o horizontální replikaci, postupujte podle kroků v části [Použití vodorovně rozbalovacích oblastí k dynamickému přidání sloupců v tabulkách aplikace Excel](tasks/er-horizontal-1.md).</span><span class="sxs-lookup"><span data-stu-id="97a29-147">To learn more about horizontal replication, follow the steps in [Use horizontally expandable ranges to dynamically add columns in Excel reports](tasks/er-horizontal-1.md).</span></span>

<span data-ttu-id="97a29-148">Součást **Rozsah** může mít další vnořené součásti elektronického výkaznictví, které se používají k zadávání hodnot do příslušných pojmenovaných rozsahů aplikace Excel.</span><span class="sxs-lookup"><span data-stu-id="97a29-148">The **Range** component can have other nested ER components that are used to enter values in the appropriate Excel named ranges.</span></span>

- <span data-ttu-id="97a29-149">Pokud je některá součást skupiny **Text** použita k zadávání hodnot, hodnota se zadává v rozsahu Excelu jako textová hodnota.</span><span class="sxs-lookup"><span data-stu-id="97a29-149">If any component of the **Text** group is used to enter values, the value is entered in an Excel range as a text value.</span></span>

    > [!NOTE]
    > <span data-ttu-id="97a29-150">Tento vzor použijte k formátování zadaných hodnot na základě národního prostředí, které je definováno v aplikaci.</span><span class="sxs-lookup"><span data-stu-id="97a29-150">Use this pattern to format entered values based on the locale that is defined in the application.</span></span>

- <span data-ttu-id="97a29-151">Pokud je součást **Buňka** skupiny **Excel** použita k zadávání hodnot, hodnota se zadává v rozsahu Excelu jako hodnota datového typu, který je definován vazbou součásti **Buňka** (například **Řetězec**, **Skutečný**, nebo **Celé číslo**).</span><span class="sxs-lookup"><span data-stu-id="97a29-151">If the **Cell** component of the **Excel** group is used to enter values, the value is entered in an Excel range as a value of the data type that is defined by the binding of that **Cell** component (for example, **String**, **Real**, or **Integer**).</span></span>

    > [!NOTE]
    > <span data-ttu-id="97a29-152">Tento vzor použijte k povolení aplikace Excel pro formátování zadané hodnoty na základě národního prostředí místního počítače, které otevírá odchozí dokument.</span><span class="sxs-lookup"><span data-stu-id="97a29-152">Use this pattern to enable the Excel application to format entered values based on the locale of the local computer that opens the outbound document.</span></span>

<span data-ttu-id="97a29-153">Na kartě **Mapování** návrháře operací elektronického výkaznictví můžete nakonfigurovat vlastnost **Povoleno** pro součást **Rozsah** k určení, zda musí být komponenta vložena do vygenerovaného dokumentu:</span><span class="sxs-lookup"><span data-stu-id="97a29-153">On the **Mapping** tab of the ER Operation designer, you can configure the **Enabled** property for a **Range** component to specify whether the component must be put in a generated document:</span></span>

- <span data-ttu-id="97a29-154">Pokud je výraz vlastnosti **Povoleno** nakonfigurován pro vrácení hodnoty **True** za běhu, nebo pokud není vůbec nakonfigurován žádný výraz, bude do vygenerovaného dokumentu vyplněn příslušný rozsah.</span><span class="sxs-lookup"><span data-stu-id="97a29-154">If an expression of the **Enabled** property is configured to return **True** at runtime, or if no expression is configured at all, the appropriate range will be filled in in the generated document.</span></span>
- <span data-ttu-id="97a29-155">Pokud je výraz vlastnosti **Povoleno** nakonfigurován pro vrácení hodnoty **False** za běhu a pokud tento rozsah nepředstavuje celé řádky nebo sloupce, nebude do vygenerovaného dokumentu vyplněn příslušný rozsah.</span><span class="sxs-lookup"><span data-stu-id="97a29-155">If an expression of the **Enabled** property is configured to return **False** at runtime, and if this range doesn't represent the entire rows or columns, the appropriate range won't be filled in in the generated document.</span></span>
- <span data-ttu-id="97a29-156">Pokud je výraz vlastnosti **Povoleno** nakonfigurován pro vrácení hodnoty **False** za běhu a pokud tento rozsah představuje celé řádky nebo sloupce, vygenerovaný dokument bude obsahovat tyto řádky a sloupce jako skryté.</span><span class="sxs-lookup"><span data-stu-id="97a29-156">If an expression of the **Enabled** property is configured to return **False** at runtime, and this range represents the entire rows or columns, the generated document will contain those rows and columns as hidden rows and columns.</span></span>

## <a name="cell-component"></a><span data-ttu-id="97a29-157">Součást buňky</span><span class="sxs-lookup"><span data-stu-id="97a29-157">Cell component</span></span>

<span data-ttu-id="97a29-158">Součást **Buňka** se používá k vyplnění pojmenovaných buněk, tvarů a obrázků Excelu.</span><span class="sxs-lookup"><span data-stu-id="97a29-158">The **Cell** component is used to fill in Excel named cells, shapes, and pictures.</span></span> <span data-ttu-id="97a29-159">Chcete-li označit objekt pojmenovaný Excel, který musí být vyplněn součástí elektronické výkaznictví **Buňka**, musíte zadat název tohoto objektu ve vlastnosti **Rozsah aplikace Excel** součásti **Buňka**.</span><span class="sxs-lookup"><span data-stu-id="97a29-159">To indicate an Excel named object that must be filled in by a **Cell** ER component, you must specify the name of that object in the **Excel range** property of the **Cell** component.</span></span>

<span data-ttu-id="97a29-160">Na kartě **Mapování** návrháře operací elektronického výkaznictví můžete nakonfigurovat vlastnost **Povoleno** pro součást **Buňka** k určení, zda ve vygenerovaném dokumentu musí být vyplněn objekt:</span><span class="sxs-lookup"><span data-stu-id="97a29-160">On the **Mapping** tab of the ER Operation designer, you can configure the **Enabled** property for a **Cell** component to specify whether the object must be filled in in a generated document:</span></span>

- <span data-ttu-id="97a29-161">Pokud je výraz vlastnosti **Povoleno** nakonfigurován pro vrácení hodnoty **True** za běhu, nebo pokud není vůbec nakonfigurován žádný výraz, bude do vygenerovaného dokumentu vyplněn příslušný objekt.</span><span class="sxs-lookup"><span data-stu-id="97a29-161">If an expression of the **Enabled** property is configured to return **True** at runtime, or if no expression is configured at all, the appropriate object will be filled in in the generated document.</span></span> <span data-ttu-id="97a29-162">Vazba této součásti **Buňka** určuje hodnotu vloženou do příslušného objektu.</span><span class="sxs-lookup"><span data-stu-id="97a29-162">The binding of this **Cell** component specifies a value that is put in the appropriate object.</span></span>
- <span data-ttu-id="97a29-163">Pokud je výraz vlastnosti **Povoleno** nakonfigurován pro vrácení hodnoty **False** za běhu, příslušný objekt nebude vyplněn ve vygenerovaném dokumentu.</span><span class="sxs-lookup"><span data-stu-id="97a29-163">If an expression of the **Enabled** property is configured to return **False** at runtime, the appropriate object won't be filled in in the generated document.</span></span>

<span data-ttu-id="97a29-164">Když je součást **Buňka** nakonfigurována pro zadávání hodnoty do buňky, může být svázána se zdrojem dat, který vrací hodnotu primitivního datového typu (například **Řetězec**, **Skutečný**, nebo **Celé číslo**).</span><span class="sxs-lookup"><span data-stu-id="97a29-164">When a **Cell** component is configured to enter a value in a cell, it can be bound with a data source that returns the value of a primitive data type (for example, **String**, **Real**, or **Integer**).</span></span> <span data-ttu-id="97a29-165">V tomto případě je hodnota zadána do buňky jako hodnota stejného typu dat.</span><span class="sxs-lookup"><span data-stu-id="97a29-165">In this case, the value is entered in the cell as a value of the same data type.</span></span>

<span data-ttu-id="97a29-166">Když je součást **Buňka** nakonfigurována pro zadávání hodnoty do tvaru Excel, může být svázána se zdrojem dat, který vrací hodnotu primitivního datového typu (například **Řetězec**, **Skutečný**, nebo **Celé číslo**).</span><span class="sxs-lookup"><span data-stu-id="97a29-166">When a **Cell** component is configured to enter a value in an Excel shape, it can be bound with a data source that returns a value of a primitive data type (for example, **String**, **Real**, or **Integer**).</span></span> <span data-ttu-id="97a29-167">V tomto případě je hodnota zadána do tvaru Excel jako text tohoto tvaru.</span><span class="sxs-lookup"><span data-stu-id="97a29-167">In this case, the value is entered in the Excel shape as the text of that shape.</span></span> <span data-ttu-id="97a29-168">Pro hodnoty typů dat, které nejsou **řetězcem**, převod na text se provádí automaticky.</span><span class="sxs-lookup"><span data-stu-id="97a29-168">For values of data types that aren't **String**, the conversion to text is done automatically.</span></span>

> [!NOTE]
> <span data-ttu-id="97a29-169">Můžete nakonfigurovat součást **Buňka** pro vyplnění tvaru pouze v případech, kdy je podporována vlastnost textu tvaru.</span><span class="sxs-lookup"><span data-stu-id="97a29-169">You can configure a **Cell** component to fill in a shape only in cases where a shape text property is supported.</span></span>

<span data-ttu-id="97a29-170">Když je součást **Buňka** nakonfigurována pro zadávání hodnoty do obrázku Excelu, může být svázána se zdrojem dat, který vrací hodnotu primitivního datového typu **Kontejner**, který představuje obrázek v binárním formátu.</span><span class="sxs-lookup"><span data-stu-id="97a29-170">When a **Cell** component is configured to enter a value in an Excel picture, it can be bound with a data source that returns a value of the **Container** data type that represents an image in binary format.</span></span> <span data-ttu-id="97a29-171">V tomto případě je hodnota zadána do obrázku Excelu jako obrázek.</span><span class="sxs-lookup"><span data-stu-id="97a29-171">In this case, the value is entered in the Excel picture as an image.</span></span>

> [!NOTE]
> <span data-ttu-id="97a29-172">Každý obrázek a tvar Excelu je považován za ukotvený svým levým horním rohem ke konkrétní buňce nebo rozsahu Excelu.</span><span class="sxs-lookup"><span data-stu-id="97a29-172">Every Excel picture and shape is considered to be anchored by its upper-left corner to a specific Excel cell or range.</span></span> <span data-ttu-id="97a29-173">Pokud chcete replikovat obrázek nebo tvar aplikace Excel, musíte nakonfigurovat buňku nebo rozsah, do kterých jsou ukotveny, jako replikovanou buňku nebo rozsah.</span><span class="sxs-lookup"><span data-stu-id="97a29-173">If you want to replicate an Excel picture or shape, you must configure the cell or range that it's anchored to as a replicated cell or range.</span></span>

<span data-ttu-id="97a29-174">Chcete-li se dozvědět více o tom, jak vkládat obrázky a tvary, nahlédněte do části [Integrace obrázků a tvarů v generovaných dokumentech pomocí elektronického výkaznictví](electronic-reporting-embed-images-shapes.md).</span><span class="sxs-lookup"><span data-stu-id="97a29-174">To learn more about how to embed images and shapes, see [Embed images and shapes in documents that you generate by using ER](electronic-reporting-embed-images-shapes.md).</span></span>

## <a name="page-break-component"></a><span data-ttu-id="97a29-175">Součást konce stránky</span><span class="sxs-lookup"><span data-stu-id="97a29-175">Page break component</span></span>

<span data-ttu-id="97a29-176">Součást **Konec stránky** vynutí, aby Excel začal na nové stránce.</span><span class="sxs-lookup"><span data-stu-id="97a29-176">The **PageBreak** component forces Excel to start a new page.</span></span> <span data-ttu-id="97a29-177">Tato součást není vyžadována, pokud chcete použít výchozí stránkování aplikace Excel, ale měli byste ji použít, pokud chcete, aby aplikace Excel postupovala podle formátu elektronického výkaznictví pro vytvoření stránkování.</span><span class="sxs-lookup"><span data-stu-id="97a29-177">This component isn't required when you want to use Excel's default paging, but you should use it when you want Excel to follow your ER format to structure paging.</span></span>

## <a name="edit-an-added-er-format"></a><span data-ttu-id="97a29-178">Úprava přidaného formátu elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="97a29-178">Edit an added ER format</span></span>

### <a name="update-a-template"></a><span data-ttu-id="97a29-179">Aktualizace šablony</span><span class="sxs-lookup"><span data-stu-id="97a29-179">Update a template</span></span>

<span data-ttu-id="97a29-180">Můžete vybrat možnost **Aktualizovat z Excelu** na kartě podokna akcí **Importovat** a naimportovat aktualizovanou šablonu do upravitelného formátu elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="97a29-180">You can select **Update from Excel** on the **Import** tab of the Action Pane to import an updated template into an editable ER format.</span></span> <span data-ttu-id="97a29-181">Během tohoto procesu bude šablona vybrané součásti **Excel\\Soubor** nahrazena novou šablonou.</span><span class="sxs-lookup"><span data-stu-id="97a29-181">During this process, a template of the selected **Excel\\File** component will be replaced by a new template.</span></span> <span data-ttu-id="97a29-182">Obsah upravitelného formátu elektronického výkaznictví bude synchronizován s obsahem aktualizované šablony elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="97a29-182">The content of the editable ER format will be synced with the content of the updated ER template.</span></span>

- <span data-ttu-id="97a29-183">Nová komponenta formátu elektronického výkaznictví bude automaticky vytvořena pro každý název Excelu, pokud komponenta formátu elektronického výkaznictví není nalezena v upravitelném formátu.</span><span class="sxs-lookup"><span data-stu-id="97a29-183">A new ER format component will automatically be created for every Excel name if the ER format component isn't found in the editable format.</span></span>
- <span data-ttu-id="97a29-184">Každá součást formátu elektronického výkaznictví bude odstraněna z upravitelného formátu elektronického výkaznictví, pokud pro ni nebude nalezen příslušný název Excelu.</span><span class="sxs-lookup"><span data-stu-id="97a29-184">Every ER format component will be deleted from the editable ER format if the appropriate Excel name isn't found for it.</span></span>

> [!NOTE]
> <span data-ttu-id="97a29-185">Pokud chcete vytvořit volitelný prvek **List** v editovatelném formátu elektronického výkaznictví, nastavte možnost **Vytvořit prvek formátu listu Excel** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="97a29-185">Set the **Create Excel Sheet format element** option to **Yes** if you want to create the optional **Sheet** element in the editable ER format.</span></span>
>
> <span data-ttu-id="97a29-186">Pokud upravitelný formát elektronického výkaznictví původně obsahoval prvky **List**, doporučujeme nastavit možnost **Vytvořit prvek formátu listu Excel** na **Ano** při importu aktualizované šablony.</span><span class="sxs-lookup"><span data-stu-id="97a29-186">If the editable ER format originally contained **Sheet** elements, we recommend that you set the **Create Excel Sheet format element** option to **Yes** when you import an updated template.</span></span> <span data-ttu-id="97a29-187">V opačném případě budou všechny vnořené prvky původního prvku **List** vytvořeny od začátku.</span><span class="sxs-lookup"><span data-stu-id="97a29-187">Otherwise, all nested elements of the original **Sheet** element will be created from scratch.</span></span> <span data-ttu-id="97a29-188">Proto budou všechny vazby znovu vytvořených prvků formátu ztraceny v aktualizovaném formátu elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="97a29-188">Therefore, all bindings of the re-created format elements will be lost in the updated ER format.</span></span>

![Možnost Vytvořit prvek formátu listu Excel v dialogovém okně Aktualizovat z Excelu](./media/er-excel-format-update-template.png)

<span data-ttu-id="97a29-190">Chcete-li se o této funkci dozvědět více, postupujte podle pokynů v části [Úprava formátů elektronického výkaznictví opětovným použitím šablon aplikace Excel](modify-electronic-reporting-format-reapply-excel-template.md).</span><span class="sxs-lookup"><span data-stu-id="97a29-190">To learn more about this feature, follow the steps in [Modify Electronic reporting formats by reapplying Excel templates](modify-electronic-reporting-format-reapply-excel-template.md).</span></span>

## <a name="validate-an-er-format"></a><span data-ttu-id="97a29-191">Ověření formátu elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="97a29-191">Validate an ER format</span></span>

<span data-ttu-id="97a29-192">Při ověření formátu elektronického výkaznictví, který lze upravit, se provede kontrola konzistence, aby se zajistilo, že název Excel bude přítomen v aktuálně používané šabloně Excel.</span><span class="sxs-lookup"><span data-stu-id="97a29-192">When you validate an ER format that can be edited, a consistency check is done to make sure that the Excel name is present in the Excel template that is currently used.</span></span> <span data-ttu-id="97a29-193">O jakýchkoli nesrovnalostech budete informováni.</span><span class="sxs-lookup"><span data-stu-id="97a29-193">You will be notified about any inconsistencies.</span></span> <span data-ttu-id="97a29-194">V případě některých nesrovnalostí bude nabídnuta možnost automaticky opravit problémy.</span><span class="sxs-lookup"><span data-stu-id="97a29-194">For some inconsistencies, the option to automatically fix issues will be offered.</span></span>

![Chybové zprávy ověření](./media/er-excel-format-validate.png)


## <a name="additional-resources"></a><span data-ttu-id="97a29-196">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="97a29-196">Additional resources</span></span>

[<span data-ttu-id="97a29-197">Přehled elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="97a29-197">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="97a29-198">Návrh konfigurace pro generování sestav ve formátu OPENXML</span><span class="sxs-lookup"><span data-stu-id="97a29-198">Design a configuration for generating reports in OPENXML format</span></span>](tasks\er-design-reports-openxml-2016-11.md)

[<span data-ttu-id="97a29-199">Úprava formátů elektronického výkaznictví opětovným použitím šablon aplikace Excel</span><span class="sxs-lookup"><span data-stu-id="97a29-199">Modify Electronic reporting formats by reapplying Excel templates</span></span>](modify-electronic-reporting-format-reapply-excel-template.md)

[<span data-ttu-id="97a29-200">Použití vodorovně rozbalovacích oblastí k dynamickému přidání sloupců v tabulkách aplikace Excel</span><span class="sxs-lookup"><span data-stu-id="97a29-200">Use horizontally expandable ranges to dynamically add columns in Excel reports</span></span>](tasks/er-horizontal-1.md)

[<span data-ttu-id="97a29-201">Integrace obrázků a tvarů v generovaných dokumentech pomocí elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="97a29-201">Embed images and shapes in documents that you generate by using ER</span></span>](electronic-reporting-embed-images-shapes.md)

[<span data-ttu-id="97a29-202">Konfigurace elektronického výkaznictví pro doplňování dat do Power BI</span><span class="sxs-lookup"><span data-stu-id="97a29-202">Configure Electronic reporting (ER) to pull data into Power BI</span></span>](general-electronic-reporting-report-configuration-get-data-powerbi.md)
