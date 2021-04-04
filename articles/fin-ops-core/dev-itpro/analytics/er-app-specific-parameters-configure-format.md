---
title: Konfigurace formátů ER pro použití parametrů zadaných pro právnickou osobu
description: V tomto tématu je vysvětleno, jak lze konfigurovat formáty elektronického vykazování (ER) pro použití parametrů zadaných pro právnickou osobu.
author: NickSelin
manager: AnnBe
ms.date: 10/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner, ERLookupDesigner, ERComponentLookupStructureEditing
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: Release 8.1.3
ms.openlocfilehash: 9253191f9cd10e0b3c87d61991598f9b791c35d9
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570727"
---
# <a name="configure-er-formats-to-use-parameters-that-are-specified-per-legal-entity"></a><span data-ttu-id="45ceb-103">Konfigurace formátů ER pro použití parametrů zadaných pro právnickou osobu</span><span class="sxs-lookup"><span data-stu-id="45ceb-103">Configure ER formats to use parameters that are specified per legal entity</span></span>

[!include[banner](../includes/banner.md)]

## <a name="overview"></a><span data-ttu-id="45ceb-104">Přehled</span><span class="sxs-lookup"><span data-stu-id="45ceb-104">Overview</span></span>

<span data-ttu-id="45ceb-105">V mnoha formátech elektronického výkaznictví (ER), které budete navrhovat, je nutné filtrovat data pomocí sady hodnot, které jsou specifické pro jednotlivé právnické osoby vaší instance (například sada kódů daní k filtrování daňových transakcí).</span><span class="sxs-lookup"><span data-stu-id="45ceb-105">In many of the Electronic reporting (ER) formats that you will design, you must filter data by using a set of values that are specific to each legal entity of your instance (for example, a set of tax codes to filter tax transactions).</span></span> <span data-ttu-id="45ceb-106">V současné době, když je filtrování tohoto typu konfigurováno ve formátu ER, jsou hodnoty, které jsou závislé na právnické osobě (například kódy daně), použity ve výrazech formátu ER pro určení pravidel filtrování dat.</span><span class="sxs-lookup"><span data-stu-id="45ceb-106">Currently, when filtering of this type is configured in an ER format, values that are dependent on the legal entity (for example, tax codes) are used in expressions of the ER format to specify data filtering rules.</span></span> <span data-ttu-id="45ceb-107">Proto je formát ER vytvořen tak, aby byl specifický pro právnickou osobu a aby generoval požadované sestavy, musíte vytvořit odvozené kopie původního formátu ER pro každou právnickou osobu, kde je nutné spustit formát ER.</span><span class="sxs-lookup"><span data-stu-id="45ceb-107">Therefore, the ER format is made legal entity–specific, and to generate the required reports, you must create derived copies of the original ER format for each legal entity where you have to run the ER format.</span></span> <span data-ttu-id="45ceb-108">Každý odvozený formát ER je nutné upravit tak, aby do něj bylo možné převést specifické hodnoty právnické osoby, a to podle toho, zda byla aktualizována původní (základní) verze, exportována z testovacího prostředí a importována do provozního prostředí v okamžiku, kdy musí být nasazena k použití v produkci atd.</span><span class="sxs-lookup"><span data-stu-id="45ceb-108">Each derived ER format must be edited to bring legal entity–specific values into it, rebased whenever the original (base) version has been updated, exported from a test environment and imported into a production environment when it must be deployed for production use, and so on.</span></span> <span data-ttu-id="45ceb-109">Proto je údržba tohoto typu konfigurovaného řešení ER poměrně složitá a časově náročná z několika důvodů:</span><span class="sxs-lookup"><span data-stu-id="45ceb-109">Therefore, maintenance of this type of configured ER solution is quite complex and time-consuming for several reasons:</span></span>

-   <span data-ttu-id="45ceb-110">Čím více je právnických osob, tím více konfigurací ER je nutné spravovat.</span><span class="sxs-lookup"><span data-stu-id="45ceb-110">The more legal entities there are, the more ER format configurations must be maintained.</span></span>
-   <span data-ttu-id="45ceb-111">Údržba konfigurací ER vyžaduje, aby měli uživatelé společnosti znalost elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="45ceb-111">Maintenance of ER configurations requires that business users have ER knowledge.</span></span>

<span data-ttu-id="45ceb-112">Funkce pro specifické parametry aplikace ER umožňují uživatelům konfigurovat filtrování dat ve formátu ER tak, aby bylo založeno na sadě abstraktních pravidel.</span><span class="sxs-lookup"><span data-stu-id="45ceb-112">The ER application-specific parameters feature lets power users configure data filtering in an ER format so that it's based on a set of abstract rules.</span></span> <span data-ttu-id="45ceb-113">Tuto sadu pravidel lze nakonfigurovat tak, aby používala zdroje dat, které jsou k dispozici ve formátu ER.</span><span class="sxs-lookup"><span data-stu-id="45ceb-113">This set of rules can be configured to use the data sources that are available in an ER format.</span></span> <span data-ttu-id="45ceb-114">Obchodní uživatelé pak mohou specifikovat skutečná pravidla nad rámec ER pomocí uživatelského rozhraní (UI), které je generováno automaticky na základě nastavení odpovídajícího formátu ER a aktuálních dat právnické osoby, k nimž budou mít přístup zdroje dat formátu ER.</span><span class="sxs-lookup"><span data-stu-id="45ceb-114">Business users can then specify real rules beyond the ER framework by using the user interface (UI) that is automatically generated based on the settings of the corresponding ER format and the current legal entity data that will be accessed by the ER format's data sources.</span></span> <span data-ttu-id="45ceb-115">Sadu pravidel specifikovanou pro formát ER lze exportovat z aktuální právnické osoby instance Dynamics 365 Finance (Finance).</span><span class="sxs-lookup"><span data-stu-id="45ceb-115">The set of rules that is specified for an ER format can be exported from the current legal entity of the Dynamics 365 Finance (Finance) instance.</span></span> <span data-ttu-id="45ceb-116">Poté ji lze importovat do jiné právnické osoby se stejnou nebo jinou instancí aplikace Finance jako sadu pravidel pro stejný formát ER.</span><span class="sxs-lookup"><span data-stu-id="45ceb-116">It can then be imported into another legal entity of either the same Finance instance or a different instance as a set of rules for the same ER format.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="45ceb-117">Předpoklady</span><span class="sxs-lookup"><span data-stu-id="45ceb-117">Prerequisites</span></span>

<span data-ttu-id="45ceb-118">Pokud chcete dokončit příklady v tomto tématu, musíte mít přístup k instanci služeb Regulatory Configuration Services (RCS), který byl zřízen pro stejného klienta jako Finance and Operations, pro jednu z následujících rolí:</span><span class="sxs-lookup"><span data-stu-id="45ceb-118">To complete the examples in this topic, you must have access to the instance of Regulatory Configuration Services (RCS) that has been provisioned for the same tenant as Finance for one of the following roles:</span></span>

- <span data-ttu-id="45ceb-119">Návrhář elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="45ceb-119">Electronic reporting developer</span></span>
- <span data-ttu-id="45ceb-120">Funkční konzultant elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="45ceb-120">Electronic reporting functional consultant</span></span>
- <span data-ttu-id="45ceb-121">Správce systému</span><span class="sxs-lookup"><span data-stu-id="45ceb-121">System administrator</span></span>

<span data-ttu-id="45ceb-122">Doporučujeme dokončit kroky v tématu [Podpora parametrizovaných volání zdrojů dat ER typu VYPOčíTANé POLE](er-calculated-field-type.md).</span><span class="sxs-lookup"><span data-stu-id="45ceb-122">We recommend that you complete the steps in the [Support parameterized calls of ER data sources of CALCULATED FIELD type](er-calculated-field-type.md) topic.</span></span> <span data-ttu-id="45ceb-123">Pokud jste již tyto kroky splnili, můžete vynechat kroky v části **Import konfigurací ER do RCS**, který následuje.</span><span class="sxs-lookup"><span data-stu-id="45ceb-123">If you've already completed those steps, you can skip the steps in the **Import ER configurations into RCS** section that follows.</span></span>

## <a name="import-er-configurations-into-rcs"></a><span data-ttu-id="45ceb-124">Import konfigurací ER do RSC</span><span class="sxs-lookup"><span data-stu-id="45ceb-124">Import ER configurations into RCS</span></span>

<span data-ttu-id="45ceb-125">Ze [služby Stažení softwaru](https://go.microsoft.com/fwlink/?linkid=851448) si můžete stáhnout soubor **Podpora parametrizovaných volání zdrojů dat ER typu VYPOčíTANéHO POLE**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-125">From [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=851448), download the **Support parameterized calls of ER data sources of CALCULATED FIELD type** zip file.</span></span> <span data-ttu-id="45ceb-126">Tento soubor zip obsahuje následující konfigurace ER, které je nutné extrahovat a uložit místně.</span><span class="sxs-lookup"><span data-stu-id="45ceb-126">This zip file contains the following ER configurations that must be extracted and stored locally.</span></span>

| <span data-ttu-id="45ceb-127">**Popis obsahu**</span><span class="sxs-lookup"><span data-stu-id="45ceb-127">**Content description**</span></span>                        | <span data-ttu-id="45ceb-128">**Název souboru**</span><span class="sxs-lookup"><span data-stu-id="45ceb-128">**File name**</span></span>                                        |
|------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="45ceb-129">Ukázkový soubor konfigurace **Model dat elektronického výkaznictví**</span><span class="sxs-lookup"><span data-stu-id="45ceb-129">Sample **ER data model** configuration file</span></span>    | <span data-ttu-id="45ceb-130">Model pro informace o volání s parametry calls.version.1.xml</span><span class="sxs-lookup"><span data-stu-id="45ceb-130">Model to learn parameterized calls.version.1.xml</span></span>     |
| <span data-ttu-id="45ceb-131">Ukázkový soubor konfigurace **Metadata ER**</span><span class="sxs-lookup"><span data-stu-id="45ceb-131">Sample **ER metadata** configuration file</span></span>      | <span data-ttu-id="45ceb-132">Metadata pro informace o volání s parametry calls.version.1.xml</span><span class="sxs-lookup"><span data-stu-id="45ceb-132">Metadata to learn parameterized calls.version.1.xml</span></span>  |
| <span data-ttu-id="45ceb-133">Ukázkový soubor konfigurace **Mapování modelu ER**</span><span class="sxs-lookup"><span data-stu-id="45ceb-133">Sample **ER model mapping** configuration file</span></span> | <span data-ttu-id="45ceb-134">Mapování pro informace o volání s parametry calls.version.1.1.xml</span><span class="sxs-lookup"><span data-stu-id="45ceb-134">Mapping to learn parameterized calls.version.1.1.xml</span></span> |
| <span data-ttu-id="45ceb-135">Ukázková konfigurace **Formát ER**</span><span class="sxs-lookup"><span data-stu-id="45ceb-135">Sample **ER format** configuration</span></span>             | <span data-ttu-id="45ceb-136">Formát pro informace o volání s parametry calls.version.1.1.xml</span><span class="sxs-lookup"><span data-stu-id="45ceb-136">Format to learn parameterized calls.version.1.1.xml</span></span>  |

<span data-ttu-id="45ceb-137">Dále se přihlaste k instanci RCS.</span><span class="sxs-lookup"><span data-stu-id="45ceb-137">Next, sign in to your RCS instance.</span></span>

<span data-ttu-id="45ceb-138">V tomto příkladu vytvoříte konfiguraci pro vzorovou společnost Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="45ceb-138">In this example, you will create a configuration for the Litware, Inc sample company.</span></span> <span data-ttu-id="45ceb-139">K provedení kroků v tomto postupu musíte nejprve dokončit postup [Vytvoření poskytovatele konfigurace a jeho označení jako aktivního](tasks/er-configuration-provider-mark-it-active-2016-11.md) v RCS.</span><span class="sxs-lookup"><span data-stu-id="45ceb-139">Before you can complete this procedure, you must complete the steps in the [Create a configuration provider and mark it as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) topic in RCS.</span></span>

1.  <span data-ttu-id="45ceb-140">Na výchozím řídicím panelu vyberte **Elektronické vykazování**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-140">On the default dashboard, select **Electronic reporting**.</span></span>
2.  <span data-ttu-id="45ceb-141">Vyberte **Konfigurace vykazování**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-141">Select **Reporting configurations**.</span></span>
3.  <span data-ttu-id="45ceb-142">Importujte konfigurace ER, které jste předtím stáhli do RCS, v následujícím pořadí: datový model, metadata, mapování modelu a formát.</span><span class="sxs-lookup"><span data-stu-id="45ceb-142">Import the ER configurations that you downloaded earlier into RCS, in the following order: data model, metadata, model mapping, and format.</span></span> <span data-ttu-id="45ceb-143">Pro každou konfiguraci ER postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="45ceb-143">For each ER configuration, follow these steps:</span></span>

    1.  <span data-ttu-id="45ceb-144">Vyberte **Exchange**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-144">Select **Exchange**.</span></span>
    2.  <span data-ttu-id="45ceb-145">Vyberte **Načíst ze souboru XML**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-145">Select **Load from XML file**.</span></span>
    3.  <span data-ttu-id="45ceb-146">Zvolte **Procházet** a vyberte soubor pro požadovanou konfiguraci elektronického výkaznictví ve formátu XML.</span><span class="sxs-lookup"><span data-stu-id="45ceb-146">Select **Browse** to select the file for the required ER configuration in XML format.</span></span>
    4.  <span data-ttu-id="45ceb-147">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-147">Select **OK**.</span></span>

## <a name="review-the-er-solution-that-is-provided"></a><span data-ttu-id="45ceb-148">Kontrola poskytnutého řešení ER</span><span class="sxs-lookup"><span data-stu-id="45ceb-148">Review the ER solution that is provided</span></span>

1.  <span data-ttu-id="45ceb-149">Ve stromu konfigurace rozbalte obsah položky **Model pro seznámení s parametrizovanými voláními**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-149">In the configuration tree, expand the contents of the **Model to learn parameterized calls** item.</span></span>
2.  <span data-ttu-id="45ceb-150">Vyberte položku **Formát pro učení parametrizovaných volání**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-150">Select the **Format to learn parameterized calls** item.</span></span>
3.  <span data-ttu-id="45ceb-151">Vyberte možnost **Návrhář**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-151">Select **Designer**.</span></span>
4.  <span data-ttu-id="45ceb-152">Vyberte **Rozbalit/sbalit**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-152">Select **Expand/Collapse**.</span></span>

    <span data-ttu-id="45ceb-153">Formát ER **Formát pro učení parametrizovaných volání** je navržen tak, aby vygeneroval daňový výkaz ve formátu XML, který představuje několik úrovní zdanění (pravidelná, redukovaná a žádná).</span><span class="sxs-lookup"><span data-stu-id="45ceb-153">The **Format to learn parameterized calls** ER format is designed to generate a tax statement in XML format that presents several levels of taxation (regular, reduced, and none).</span></span> <span data-ttu-id="45ceb-154">Každá úroveň má různý počet podrobností.</span><span class="sxs-lookup"><span data-stu-id="45ceb-154">Each level has a different number of details.</span></span>

    ![Stránka návrháře operace ER](./media/RCS-AppSpecParms-ReviewFormat.PNG)

5.  <span data-ttu-id="45ceb-156">Na kartě **Mapování** rozbalte položky **Model**, **Data** a **Souhrn**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-156">On the **Mapping** tab, expand the **Model**, **Data**, and **Summary** items.</span></span>

    <span data-ttu-id="45ceb-157">Zdroj dat **Model.Data.Summary** vrátí seznam daňových transakcí.</span><span class="sxs-lookup"><span data-stu-id="45ceb-157">The **Model.Data.Summary** data source returns the list of tax transactions.</span></span> <span data-ttu-id="45ceb-158">Tyto transakce jsou sumarizovány v seznamu podle kódu DPH.</span><span class="sxs-lookup"><span data-stu-id="45ceb-158">These transactions are summarized by tax code.</span></span> <span data-ttu-id="45ceb-159">Pro tento zdroj dat bylo nakonfigurováno vypočítané pole **Model.Data.Summary.Level**, které vrací kód úrovně zdanění jednotlivých souhrnných záznamů.</span><span class="sxs-lookup"><span data-stu-id="45ceb-159">For this data source, the **Model.Data.Summary.Level** calculated field has been configured to return the code for the taxation level of each summarized record.</span></span> <span data-ttu-id="45ceb-160">Pro jakýkoli kód zdanění, který lze načíst ze zdroje dat **Model.Data.Summary** v době běhu, vrátí vypočtené pole kód úrovně zdanění (**Běžný**, **Redukovaný**, **Žádný** nebo **Ostatní**) jako textovou hodnotu.</span><span class="sxs-lookup"><span data-stu-id="45ceb-160">For any tax code that can be retrieved from the **Model.Data.Summary** data source at runtime, the calculated field returns the taxation level code (**Regular**, **Reduced**, **None**, or **Other**) as a text value.</span></span> <span data-ttu-id="45ceb-161">Vypočtené pole **Model.Data.Summary.Level** se použije k filtrování záznamů zdroje dat **Model.Data.Summary** a zadání filtrovaných dat do každého prvku XML, který představuje úroveň zdanění pomocí polí **Model.Data2.Level1**, **Model.Data2.Level2** a **Model.Data2.Level3**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-161">The **Model.Data.Summary.Level** calculated field is used to filter records of the **Model.Data.Summary** data source and enter the filtered data in each XML element that represents a taxation level by using the **Model.Data2.Level1**, **Model.Data2.Level2**, and **Model.Data2.Level3** fields.</span></span>

    ![Stránka návrháře operace ER](./media/RCS-AppSpecParms-ReviewFormat-Data2Fld.PNG)

    <span data-ttu-id="45ceb-163">Vypočítané pole **Model.Data.Summary.Level** je nakonfigurováno tak, aby obsahovalo výraz ER.</span><span class="sxs-lookup"><span data-stu-id="45ceb-163">The **Model.Data.Summary.Level** calculated field has been configured so that it contains an ER expression.</span></span> <span data-ttu-id="45ceb-164">Všimněte si, že do této konfigurace jsou zakódovány kódy daní (**VAT19**, **InVAT19**, **VAT7**, **InVAT7**, **THIRD** a **InVAT0**).</span><span class="sxs-lookup"><span data-stu-id="45ceb-164">Note that tax codes (**VAT19**, **InVAT19**, **VAT7**, **InVAT7**, **THIRD**, and **InVAT0**) are hardcoded into this configuration.</span></span> <span data-ttu-id="45ceb-165">Tento formát ER je závislý na právnické osobě, kde byly tyto kódy daně nakonfigurovány.</span><span class="sxs-lookup"><span data-stu-id="45ceb-165">Therefore, this ER format is dependent on the legal entity where these tax codes were configured.</span></span>

    ![Stránka návrháře operace ER](./media/RCS-AppSpecParms-ReviewFormat-LevelFld.PNG)

    <span data-ttu-id="45ceb-167">Chcete-li podporovat jinou sadu kódů daní pro každou právnickou osobu, je nutné provést následující kroky:</span><span class="sxs-lookup"><span data-stu-id="45ceb-167">To support a different set of tax codes for each legal entity, you must follow these steps:</span></span>

    - <span data-ttu-id="45ceb-168">Vytvoření odvozené verze formátu ER pro každou právnickou osobu.</span><span class="sxs-lookup"><span data-stu-id="45ceb-168">Create a derived version of the ER format for each legal entity.</span></span>
    - <span data-ttu-id="45ceb-169">Aktualizujte kódy DPH ve vypočteném poli **Model.Data.Summary.Level** na základě nastavení právnické osoby.</span><span class="sxs-lookup"><span data-stu-id="45ceb-169">Update the tax codes in the **Model.Data.Summary.Level** calculated field, based on the legal entity setting.</span></span>

6.  <span data-ttu-id="45ceb-170">Zavřete stránku **Návrhář formátu**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-170">Close the **Format designer** page.</span></span>

## <a name="create-a-derived-format"></a><span data-ttu-id="45ceb-171">Vytvoření odvozeného formátu</span><span class="sxs-lookup"><span data-stu-id="45ceb-171">Create a derived format</span></span>

<span data-ttu-id="45ceb-172">Dále použijete funkci parametrů specifickou podle aplikace ER na podporu různých sad kódů daní pro každou právnickou osobu v jednoduchém formátu ER.</span><span class="sxs-lookup"><span data-stu-id="45ceb-172">Next, you will use the ER application-specific parameters feature to support a different set of tax codes for each legal entity in a single ER format.</span></span>

1.  <span data-ttu-id="45ceb-173">Ve stromu konfigurace rozbalte obsah položky **Model pro seznámení s parametrizovanými voláními**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-173">In the configuration tree, expand the contents of the **Model to learn parameterized calls** item.</span></span>
2.  <span data-ttu-id="45ceb-174">Vyberte položku **Formát pro učení parametrizovaných volání**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-174">Select the **Format to learn parameterized calls** item.</span></span>
3.  <span data-ttu-id="45ceb-175">Vyberte **Vytvořit konfiguraci**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-175">Select **Create configuration**.</span></span>
4.  <span data-ttu-id="45ceb-176">Vyberte možnost **Odvozeno od názvu: Formát pro informace o parametrizovaných volání, Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-176">Select the **Derive from Name: Format to learn parameterized calls, Microsoft** option.</span></span>
5.  <span data-ttu-id="45ceb-177">Do pole **Název** zadejte **Formát pro učení vyhledání dat LE**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-177">In the **Name** field, enter **Format to learn how to lookup LE data**.</span></span>
6.  <span data-ttu-id="45ceb-178">Vyberte **Vytvořit konfiguraci**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-178">Select **Create configuration**.</span></span>

## <a name="configure-a-derived-format"></a><span data-ttu-id="45ceb-179">Konfigurace odvozeného formátu</span><span class="sxs-lookup"><span data-stu-id="45ceb-179">Configure a derived format</span></span>

### <a name="add-a-format-enumeration"></a><span data-ttu-id="45ceb-180">Přidání výčtu formátu</span><span class="sxs-lookup"><span data-stu-id="45ceb-180">Add a format enumeration</span></span>

<span data-ttu-id="45ceb-181">Dále přidáte nový výčet formátu ER.</span><span class="sxs-lookup"><span data-stu-id="45ceb-181">Next, you will add a new ER format enumeration.</span></span> <span data-ttu-id="45ceb-182">Hodnoty tohoto formátu budou prezentovány obchodním uživatelům, kteří budou používat sady kódů daní, které jsou závislé na právnické osobě pro různé úrovně zdanění, které jsou použity ve formátu ER.</span><span class="sxs-lookup"><span data-stu-id="45ceb-182">The values of this format enumeration will be presented to business users, who will specify legal entity–dependent sets of tax codes for the various taxation levels that are used in the ER format.</span></span>

1.  <span data-ttu-id="45ceb-183">Vyberte možnost **Návrhář**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-183">Select **Designer**.</span></span>
2.  <span data-ttu-id="45ceb-184">Vyberte **Vyčíslení formátu**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-184">Select **Format enumerations**.</span></span>
3.  <span data-ttu-id="45ceb-185">Vyberte **přidat**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-185">Select **Add**.</span></span>
4.  <span data-ttu-id="45ceb-186">Do pole **Název** zadejte **Seznam úrovní zdanění**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-186">In the **Name** field, enter **List of taxation levels**.</span></span>
5.  <span data-ttu-id="45ceb-187">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-187">Select **Save**.</span></span>
6.  <span data-ttu-id="45ceb-188">Na kartě **Hodnoty vyčíslení formátu** vyberte možnost **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-188">On the **Format enumeration values** tab, select **Add**.</span></span>
7.  <span data-ttu-id="45ceb-189">Do pole **Název** zadejte **Běžné zdanění**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-189">In the **Name** field, enter **Regular taxation**.</span></span>
8.  <span data-ttu-id="45ceb-190">Znovu vyberte **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-190">Select **Add** again.</span></span>
9.  <span data-ttu-id="45ceb-191">Do pole **Název** zadejte **Redukované zdanění**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-191">In the **Name** field, enter **Reduced taxation**.</span></span>
10. <span data-ttu-id="45ceb-192">Znovu vyberte **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-192">Select **Add** again.</span></span>
11. <span data-ttu-id="45ceb-193">Do pole **Název** zadejte **Žádné zdanění**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-193">In the **Name** field, enter **No taxation**.</span></span>
12. <span data-ttu-id="45ceb-194">Znovu vyberte **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-194">Select **Add** again.</span></span>
13. <span data-ttu-id="45ceb-195">Do pole **Název** zadejte **Jiné**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-195">In the **Name** field, enter **Other**.</span></span>

    ![Stránka návrháře operace ER](./media/RCS-AppSpecParms-ConfigureFormat-Enum.PNG)

    <span data-ttu-id="45ceb-197">Vzhledem k tomu, že obchodní uživatelé mohou používat různé sady kódů daní závislé na právnické osobě, doporučujeme překládat hodnoty tohoto výčtu do jazyků konfigurovaných jako preferované jazyky pro tyto uživatele v modulu finance.</span><span class="sxs-lookup"><span data-stu-id="45ceb-197">Because the business users might use different languages to specify legal entity–dependent sets of tax codes, we recommend that you translate the values of this enumeration into the languages that are configured as the preferred languages for those users in Finance.</span></span>

14. <span data-ttu-id="45ceb-198">Vyberte záznam **žádné zdanění**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-198">Select the **No taxation** record.</span></span>
15. <span data-ttu-id="45ceb-199">Klikněte do pole **Popisek**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-199">Click in the **Label** field.</span></span>
16. <span data-ttu-id="45ceb-200">Vyberte **Přeložit**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-200">Select **Translate**.</span></span>
17. <span data-ttu-id="45ceb-201">V podokně **Překlad textu** do pole **ID popisku** zadejte **LBL_LEVELENUM_NO**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-201">In the **Text translation** pane, in the **Label Id** field, enter **LBL_LEVELENUM_NO**.</span></span>
18. <span data-ttu-id="45ceb-202">Do pole **Text ve výchozím jazyce** zadejte **žádné zdanění**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-202">In the **Text in default language** field, enter **No taxation**.</span></span>
19. <span data-ttu-id="45ceb-203">V poli **Jazyk** vyberte **DE**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-203">In the **Language** field, select **DE**.</span></span>
20. <span data-ttu-id="45ceb-204">Do pole **přeložený text** napište **keine Besteuerung**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-204">In the **Translated text** field, enter **keine Besteuerung**.</span></span>
21. <span data-ttu-id="45ceb-205">Vyberte **Přeložit**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-205">Select **Translate**.</span></span>

    ![Stránka návrháře operace ER](./media/RCS-AppSpecParms-ConfigureFormat-EnumTranslate.PNG)

22. <span data-ttu-id="45ceb-207">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-207">Select **Save**.</span></span>
23. <span data-ttu-id="45ceb-208">Zavřete stránku **Vyčíslení formátu**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-208">Close the **Format enumerations** page.</span></span>

### <a name="add-a-new-lookup-data-source"></a><span data-ttu-id="45ceb-209">Přidání nového zdroje dat vyhledávání</span><span class="sxs-lookup"><span data-stu-id="45ceb-209">Add a new lookup data source</span></span>

<span data-ttu-id="45ceb-210">Dále přidáte nový zdroj dat, který určuje, jakým způsobem budou obchodní uživatelé určovat pravidla závislá na právnické osobě, aby byla pro jednotlivé souhrnné záznamy transakcí rozpoznána správná úroveň zdanění.</span><span class="sxs-lookup"><span data-stu-id="45ceb-210">Next, you will add a new data source to specify how business users will specify legal entity–dependent rules to recognize the correct taxation level for each summarized transaction record.</span></span>

1.  <span data-ttu-id="45ceb-211">Na kartě **Mapování** vyberte **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-211">On the **Mapping** tab, select **Add**.</span></span>
2.  <span data-ttu-id="45ceb-212">Vyberte **Vyčíslení formátu\Lookup**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-212">Select **Format enumeration\Lookup**.</span></span>

    <span data-ttu-id="45ceb-213">Právě jste zjistili, že každé pravidlo, které obchodní uživatelé zadá za účelem uznání úrovně zdanění, vrátí hodnotu výčtu formátu ER.</span><span class="sxs-lookup"><span data-stu-id="45ceb-213">You just identified that each rule that business users specify for taxation level recognition will return a value of an ER format enumeration.</span></span> <span data-ttu-id="45ceb-214">Všimněte si, že k typu zdroje dat **Vyhledávání** lze přejít v části **Datový model** a z bloků **Dynamics 365 for Operations** navíc k bloku **Vyčíslení formátu**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-214">Notice that the **Lookup** data source type can be accessed under the **Data model** and **Dynamics 365 for Operations** blocks in addition to the **Format enumeration** block.</span></span> <span data-ttu-id="45ceb-215">Proto výčty datových modelů ER a výčty aplikací lze použít k určení typu hodnot, které jsou vraceny pro zdroje dat tohoto typu.</span><span class="sxs-lookup"><span data-stu-id="45ceb-215">Therefore, ER data model enumerations and application enumerations can be used to specify the type of values that is are returned for data sources of that type.</span></span>
    
3.  <span data-ttu-id="45ceb-216">Do pole **Název** zadejte **Selektor**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-216">In the **Name** field, enter **Selector**.</span></span>
4.  <span data-ttu-id="45ceb-217">Do pole **Vyčíslení formátu** zadejte **Seznam úrovní zdanění**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-217">In the **Format enumeration** field, select **List of taxation levels**.</span></span>

    <span data-ttu-id="45ceb-218">Právě jste zadali, že pro každé pravidlo, které je zadáno v tomto zdroji dat, musí obchodní uživatel vybrat jednu z hodnot **seznamu výčtů formátu daňové úrovně** jako vrácenou hodnotu.</span><span class="sxs-lookup"><span data-stu-id="45ceb-218">You just specified that, for each rule that is specified in this data source, a business user must select one of the values of the **List of taxation levels** format enumeration as a returned value.</span></span>
    
5.  <span data-ttu-id="45ceb-219">Vyberte **upravit vyhledávání**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-219">Select **Edit lookup**.</span></span>
6.  <span data-ttu-id="45ceb-220">Vyberte **Sloupce**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-220">Select **Columns**.</span></span>
7.  <span data-ttu-id="45ceb-221">Rozbalte položku **Model**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-221">Expand the **Model** item.</span></span>
8.  <span data-ttu-id="45ceb-222">Rozbalte položku **Data**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-222">Expand the **Data** item.</span></span>
9.  <span data-ttu-id="45ceb-223">Rozbalte položku **Daň**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-223">Expand the **Tax** item.</span></span>
10. <span data-ttu-id="45ceb-224">Vyberte položku **Model.Data.Tax.Code**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-224">Select the **Model.Data.Tax.Code** item.</span></span>
11. <span data-ttu-id="45ceb-225">Klepněte na tlačítko **přidat** (šipka vpravo).</span><span class="sxs-lookup"><span data-stu-id="45ceb-225">Select the **Add** button (the right arrow).</span></span>

    ![Stránka návrháře operace ER](./media/RCS-AppSpecParms-ConfigureFormat-Lookup1.PNG)

    <span data-ttu-id="45ceb-227">Právě jste zadali, že pro každé pravidlo, které je zadáno v tomto zdroji dat pro rozpoznání úrovně zdanění, musí obchodní uživatel vybrat jeden z daňových kódů jako podmínku.</span><span class="sxs-lookup"><span data-stu-id="45ceb-227">You just specified that, for each rule that is specified in this data source for taxation level recognition, a business user must select one of the tax codes as a condition.</span></span> <span data-ttu-id="45ceb-228">Seznam kódů daní, které může obchodní uživatel vybrat, bude vrácen zdrojem dat **Model.Data.Tax**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-228">The list of tax codes that the business user can select will be returned by the **Model.Data.Tax** data source.</span></span> <span data-ttu-id="45ceb-229">Vzhledem k tomu, že tento zdroj dat obsahuje pole **Název**, zobrazí se název kódu daně pro každou hodnotu kódu daně ve vyhledávání, které je prezentováno obchodnímu uživateli.</span><span class="sxs-lookup"><span data-stu-id="45ceb-229">Because this data source contains the **Name** field, the name of the tax code will be shown for each tax code value in the lookup that is presented to the business user.</span></span>
    
12. <span data-ttu-id="45ceb-230">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-230">Select **OK**.</span></span>

    ![Stránka návrháře operace ER](./media/RCS-AppSpecParms-ConfigureFormat-Lookup2.PNG)

    <span data-ttu-id="45ceb-232">Obchodní uživatelé mohou přidat více pravidel jako záznamy tohoto datového zdroje.</span><span class="sxs-lookup"><span data-stu-id="45ceb-232">Business users can add multiple rules as records of this data source.</span></span> <span data-ttu-id="45ceb-233">Každý záznam bude očíslován kódem řádku.</span><span class="sxs-lookup"><span data-stu-id="45ceb-233">Each record will be numbered by a line code.</span></span> <span data-ttu-id="45ceb-234">Pravidla budou vyhodnocována v pořadí podle rostoucího čísla řádku.</span><span class="sxs-lookup"><span data-stu-id="45ceb-234">Rules will be evaluated in order of increasing line number.</span></span>

    <span data-ttu-id="45ceb-235">Protože jste vybrali pole **kód daně** jako podmínku pro pravidla v tomto vyhledávacím zdroji dat a protože **kód daně** je nastaven jako pole datového typu **řetězec**, bude každé pravidlo vyhodnoceno za běhu porovnáním kódu daně, který je předán zdroji dat s kódem daně, který je definován v tomto záznamu zdroje dat.</span><span class="sxs-lookup"><span data-stu-id="45ceb-235">Because you selected the **Tax code** field as a condition for rules in this lookup data source, and because **Tax code** is set up as a field of the **String** data type, each rule will be evaluated at runtime by comparing the tax code that is passed to the data source with the tax code that is defined in this record of the data source.</span></span>

    <span data-ttu-id="45ceb-236">Při nalezení pravidla, které splňuje konfigurovanou podmínku, vrátí tento zdroj dat vyhledávací hodnotu pravidla, které je definováno v poli **výsledek vyhledávání**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-236">When a rule that satisfies the configured condition is found, this data source returns the lookup value of the rule that is defined in the **Lookup result** field.</span></span> <span data-ttu-id="45ceb-237">Pokud není nalezeno žádné pravidlo, je vyvolána výjimka pro upozornění uživatele, že aktuální zdroj dat nemůže vrátit správnou hodnotu.</span><span class="sxs-lookup"><span data-stu-id="45ceb-237">If no rule is found, an exception is thrown to notify the user that the current data source can't return a correct value.</span></span>

13. <span data-ttu-id="45ceb-238">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-238">Select **Save**.</span></span>
14. <span data-ttu-id="45ceb-239">Zavřete stránku **Návrhář vyhledávání**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-239">Close the **Lookup designer** page.</span></span>
15. <span data-ttu-id="45ceb-240">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-240">Select **OK**.</span></span>

    <span data-ttu-id="45ceb-241">Všimněte si, že jste přidali nový zdroj dat, který vrátí úroveň zdanění jako hodnotu **seznamu úrovní zdanění** pro jakýkoliv daňový kód, který je předán zdroji dat, jako argument parametru **kód** datového typu **řetězec**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-241">Notice that you added a new data source that will return the taxation level as the value of the **List of taxation levels** format enumeration for any tax code that is passed to the data source as the argument of the **Code** parameter of the **String** data type.</span></span>
    
    ![Stránka návrháře operace ER](./media/RCS-AppSpecParms-ConfigureFormat-SelectorFld.PNG)

    <span data-ttu-id="45ceb-243">Všimněte si, že vyhodnocení konfigurovaných pravidel závisí na datovém typu polí, která byla vybrána pro definování podmínek těchto pravidel.</span><span class="sxs-lookup"><span data-stu-id="45ceb-243">Note that the evaluation of configured rules depends on the data type of the fields that have been selected to define conditions of those rules.</span></span> <span data-ttu-id="45ceb-244">Pokud vyberete pole, které je konfigurováno jako pole datového typu **Číselný** nebo **Datum**, kritéria se budou lišit od kritérií, která byla popsána dříve pro datový typ **řetězec**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-244">When you select a field that is configured as a field of either the **Numeric** or **Date** data type, the criteria will differ from the criteria that were described earlier for the **String** data type.</span></span> <span data-ttu-id="45ceb-245">U **číselného** a **datového** pole musí být pravidlo specifikováno jako rozsah hodnot.</span><span class="sxs-lookup"><span data-stu-id="45ceb-245">For **Numeric** and **Date** fields, the rule must be specified as a range of values.</span></span> <span data-ttu-id="45ceb-246">Pokud je hodnota předaná zdroji dat v nakonfigurovaném rozsahu, bude podmínka pravidla považována za splněnou.</span><span class="sxs-lookup"><span data-stu-id="45ceb-246">The condition of the rule will then be considered satisfied when a value that is passed to the data source is in the configured range.</span></span>
    
    <span data-ttu-id="45ceb-247">Následující obrázek znázorňuje příklad tohoto typu nastavení.</span><span class="sxs-lookup"><span data-stu-id="45ceb-247">The following illustration shows an example of this type of setup.</span></span> <span data-ttu-id="45ceb-248">Kromě pole **Model.Data.Tax.Code** datového typu **ŘEtězec** je použito pole **Model.Tax.Summary.Base** datového typu **Real** k určení podmínek pro zdroj dat vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="45ceb-248">In addition to the **Model.Data.Tax.Code** field of the **String** data type, the **Model.Tax.Summary.Base** field of the **Real** data type is used to specify conditions for a lookup data source.</span></span>
    
    ![Stránka návrháře operace ER](./media/RCS-AppSpecParms-ConfigureFormat-SelectorFld2.PNG)

    <span data-ttu-id="45ceb-250">Protože jsou pro tento zdroj dat vyhledávání vybraná pole **Model.Data.Tax.Code** a **Model.Tax.Summary.Base**, každé pravidlo tohoto zdroje dat bude konfigurováno následovně:</span><span class="sxs-lookup"><span data-stu-id="45ceb-250">Because the **Model.Data.Tax.Code** and **Model.Tax.Summary.Base** fields are selected for this lookup data source, each rule of this data source will be configured in the following way:</span></span>
    
    -   <span data-ttu-id="45ceb-251">V seznamu, který je zobrazen, musí být jako vrácená hodnota vybrané vyčíslení formátu **Seznam úrovní zdanění**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-251">In the list that is presented, the value of the **List of taxation levels** format enumeration must be selected as a returned value.</span></span>
    -   <span data-ttu-id="45ceb-252">Kód daně musí být zadán jako podmínka tohoto pravidla.</span><span class="sxs-lookup"><span data-stu-id="45ceb-252">The tax code must be entered as a condition of this rule.</span></span> <span data-ttu-id="45ceb-253">Jsou použitelné pouze kódy daní, které jsou poskytnuty zdrojem dat **Model.Data.Tax**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-253">Only tax codes that are provided by the **Model.Data.Tax** data source are applicable.</span></span>
    -   <span data-ttu-id="45ceb-254">Minimální a maximální hodnoty částky základu daně musí být zadány jako podmínky tohoto pravidla.</span><span class="sxs-lookup"><span data-stu-id="45ceb-254">Minimum and maximum values of the tax base amount must be entered as conditions of this rule.</span></span>

    <span data-ttu-id="45ceb-255">Zde je, jak bude každé pravidlo tohoto zdroje dat vyhodnoceno za běhu:</span><span class="sxs-lookup"><span data-stu-id="45ceb-255">Here is how each rule of this data source will be evaluated at runtime:</span></span>
    -   <span data-ttu-id="45ceb-256">Rovná se kód datového typu **řetězec**, který byl předán do tohoto zdroje dat, shodný s kódem daně pravidla?</span><span class="sxs-lookup"><span data-stu-id="45ceb-256">Does the code of the **String** data type that was passed to this data source equal the tax code of a rule?</span></span>
    -   <span data-ttu-id="45ceb-257">Spadá hodnota **skutečného** datového typu, který byl předán do tohoto zdroje dat, do rozmezí mezi specifickou minimální a maximální hodnotou?</span><span class="sxs-lookup"><span data-stu-id="45ceb-257">Does the value of the **Real** data type that was passed to this data source fall between specific minimum and maximum values?</span></span>

    <span data-ttu-id="45ceb-258">Pravidlo bude považováno za použitelné, pokud budou splněny obě podmínky.</span><span class="sxs-lookup"><span data-stu-id="45ceb-258">A rule will be considered applicable when both conditions are satisfied.</span></span>

### <a name="translate-the-label-of-the-lookup-data-source-that-was-added"></a><span data-ttu-id="45ceb-259">Převést popisek pro vyhledávací zdroj dat, který byl přidán</span><span class="sxs-lookup"><span data-stu-id="45ceb-259">Translate the label of the lookup data source that was added</span></span>

<span data-ttu-id="45ceb-260">Vzhledem k tomu, že obchodní uživatelé mohou používat různé sady kódů daní závislé na právnické osobě, doporučujeme překládat popisek jakéhokoli zdroje dat vyhledávání, který přidáte, aby byl prezentován v preferovaném jazyce každého uživatele na odpovídající stránce.</span><span class="sxs-lookup"><span data-stu-id="45ceb-260">Because business users might use different languages to specify legal entity–dependent sets of tax codes, we recommend that you translate the label of any lookup data source that you add, so that it's presented in each user's preferred language on the corresponding page.</span></span>

1.  <span data-ttu-id="45ceb-261">Vyberte zdroj dat **Model.Data.Selector**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-261">Select the **Model.Data.Selector** data source.</span></span>
2.  <span data-ttu-id="45ceb-262">Vyberte možnost **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-262">Select **Edit**.</span></span>
3.  <span data-ttu-id="45ceb-263">Klikněte do pole **Popisek**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-263">Click in the **Label** field.</span></span>
4.  <span data-ttu-id="45ceb-264">Vyberte **Přeložit**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-264">Select **Translate**.</span></span>
5.  <span data-ttu-id="45ceb-265">V podokně **Překlad textu** do pole **ID popisku** zadejte **LBL_SELECTOR_DS**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-265">In the **Text translation** pane, in the **Label Id** field, enter **LBL_SELECTOR_DS**.</span></span>
6.  <span data-ttu-id="45ceb-266">Do pole **Text ve výchozím jazyce** zadejte volbu **Vybrat úroveň daně podle kódu daně**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-266">In the **Text in default language** field, enter **Select tax level by tax code**.</span></span>
7.  <span data-ttu-id="45ceb-267">V poli **Jazyk** vyberte **DE**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-267">In the **Language** field, select **DE**.</span></span>
8.  <span data-ttu-id="45ceb-268">Do pole **přeložený text** zadejte **Steuerebene für Steuerkennzeichen auswählen**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-268">In the **Translated text** field, enter **Steuerebene für Steuerkennzeichen auswählen**.</span></span>
9.  <span data-ttu-id="45ceb-269">Vyberte **Přeložit**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-269">Select **Translate**.</span></span>
10. <span data-ttu-id="45ceb-270">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-270">Select **OK**.</span></span>

    ![Stránka návrháře operace ER](./media/RCS-AppSpecParms-ConfigureFormat-SelectorFldTranslate.PNG)

### <a name="add-a-new-field-to-consume-the-configured-lookup"></a><span data-ttu-id="45ceb-272">Přidání nového pole ke spotřebování nakonfigurovaného vyhledávání</span><span class="sxs-lookup"><span data-stu-id="45ceb-272">Add a new field to consume the configured lookup</span></span>

1.  <span data-ttu-id="45ceb-273">Rozbalte položku **Model.Data**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-273">Expand the **Model.Data** item.</span></span>
2.  <span data-ttu-id="45ceb-274">Vyberte položku **Model.Data.Summary**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-274">Select the **Model.Data.Summary** item.</span></span>
3.  <span data-ttu-id="45ceb-275">Vyberte **přidat**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-275">Select **Add**.</span></span>
4.  <span data-ttu-id="45ceb-276">Vyberte **Funkce/vypočítané pole**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-276">Select **Functions/Calculated field**.</span></span>
5.  <span data-ttu-id="45ceb-277">Do pole **Název** zadejte **LevelByLookup**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-277">In the **Name** field, enter **LevelByLookup**.</span></span>
6.  <span data-ttu-id="45ceb-278">Vyberte možnost **Upravit vzorec**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-278">Select **Edit formula**.</span></span>
7.  <span data-ttu-id="45ceb-279">Do **pole Receptura** zadejte **Model.Selector(Model.Data.Summary.Code)**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-279">In the **Formula field**, enter **Model.Selector(Model.Data.Summary.Code)**.</span></span>
8.  <span data-ttu-id="45ceb-280">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-280">Select **Save**.</span></span>

    ![Stránka návrháře operace ER](./media/RCS-AppSpecParms-ConfigureFormat-AddLevelByLookupFld.PNG)

9.  <span data-ttu-id="45ceb-282">Zavřete stránku **Editor vzorců**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-282">Close the **Formula editor** page.</span></span>
10. <span data-ttu-id="45ceb-283">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-283">Select **OK**.</span></span>

    ![Stránka návrháře operace ER](./media/RCS-AppSpecParms-ConfigureFormat-AddLevelByLookupFld2.PNG)

    <span data-ttu-id="45ceb-285">Všimněte si, že vypočtené pole **LevelByLookup**, které jste přidali, vrátí daňovou úroveň jako hodnotu **seznamu úrovní zdanění** pro každý záznam sumarizovaných daňových transakcí.</span><span class="sxs-lookup"><span data-stu-id="45ceb-285">Notice that the **LevelByLookup** calculated field that you added will return the taxation level as the value of the **List of taxation levels** format enumeration for each summarized tax transactions record.</span></span> <span data-ttu-id="45ceb-286">Kód daně záznamu bude předán do zdroje dat vyhledávání **Model.Selector** a sada pravidel pro tento zdroj dat bude použita při výběru správné úrovně zdanění.</span><span class="sxs-lookup"><span data-stu-id="45ceb-286">The tax code of the record will be passed to the **Model.Selector** lookup data source, and the set of rules for this data source will be used to select the correct taxation level.</span></span>

### <a name="add-a-new-format-enumeration-based-data-source"></a><span data-ttu-id="45ceb-287">Přidání nového zdroje dat na základě vyčíslení formátu</span><span class="sxs-lookup"><span data-stu-id="45ceb-287">Add a new format enumeration-based data source</span></span>

<span data-ttu-id="45ceb-288">Dále přidáte nový zdroj dat, který odkazuje na vyčíslení formát, který jste přidali dříve.</span><span class="sxs-lookup"><span data-stu-id="45ceb-288">Next, you will add a new data source that refers to the format enumeration that you added earlier.</span></span> <span data-ttu-id="45ceb-289">Hodnoty tohoto zdroje dat budou později použity ve výrazu formátu ER.</span><span class="sxs-lookup"><span data-stu-id="45ceb-289">Values of this data source will be used in an ER format expression later.</span></span>

1.  <span data-ttu-id="45ceb-290">Vyberte **Přidat kořen**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-290">Select **Add root**.</span></span>
2.  <span data-ttu-id="45ceb-291">Vyberte **Vyčíslení formátu\Enumeration**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-291">Select **Format enumerations\Enumeration**.</span></span>
3.  <span data-ttu-id="45ceb-292">Do pole **Název** zadejte **TaxationLevel**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-292">In the **Name** field, enter **TaxationLevel**.</span></span>
4.  <span data-ttu-id="45ceb-293">Do pole **Vyčíslení formátu** zadejte **Seznam úrovní zdanění**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-293">In the **Format enumeration** field, select **List of taxation levels**.</span></span>
5.  <span data-ttu-id="45ceb-294">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-294">Select **Save**.</span></span>

### <a name="modify-an-existing-field-to-start-to-use-the-lookup"></a><span data-ttu-id="45ceb-295">Úprava existujícího pole, aby bylo možné začít používat vyhledávání</span><span class="sxs-lookup"><span data-stu-id="45ceb-295">Modify an existing field to start to use the lookup</span></span>

<span data-ttu-id="45ceb-296">Dále upravíte existující vypočtené pole tak, aby používalo konfigurovaný vyhledávací zdroj dat k vrácení správné hodnoty úrovně zdanění v závislosti na kódu daně.</span><span class="sxs-lookup"><span data-stu-id="45ceb-296">Next, you will modify the existing calculated field so that it uses the configured lookup data source to return the correct taxation level value, depending on the tax code.</span></span>

1.  <span data-ttu-id="45ceb-297">Vyberte položku **Model.Data.Summary.Level**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-297">Select the **Model.Data.Summary.Level** item.</span></span>
2.  <span data-ttu-id="45ceb-298">Vyberte možnost **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-298">Select **Edit**.</span></span>
3.  <span data-ttu-id="45ceb-299">Vyberte možnost **Upravit vzorec**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-299">Select **Edit formula**.</span></span>

    <span data-ttu-id="45ceb-300">Všimněte si, že aktuální výraz pole **Model.Data.Summary.Level** obsahuje následující kódy pevně zakódovaných daní:</span><span class="sxs-lookup"><span data-stu-id="45ceb-300">Notice that the current expression of the **Model.Data.Summary.Level** field includes the following hard-coded tax codes:</span></span>
    
    <span data-ttu-id="45ceb-301">CASE (@.Code, "VAT19", "Regular", "InVAT19", "Regular", "VAT7", "Reduced", "InVAT7", "Reduced", "THIRD", "None", "InVAT0", "None", "Other")</span><span class="sxs-lookup"><span data-stu-id="45ceb-301">CASE (@.Code, "VAT19", "Regular", "InVAT19", "Regular", "VAT7", "Reduced", "InVAT7", "Reduced", "THIRD", "None", "InVAT0", "None", "Other")</span></span>

4.  <span data-ttu-id="45ceb-302">Do pole **Formula** Receptura zadejte **CASE(@.LevelByLookup, TaxationLevel.'Regular taxation', "Regular", TaxationLevel.'Reduced taxation', "Reduced", TaxationLevel.'No taxation', "None", "Other")**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-302">In the **Formula** field, enter **CASE(@.LevelByLookup, TaxationLevel.'Regular taxation', "Regular", TaxationLevel.'Reduced taxation', "Reduced", TaxationLevel.'No taxation', "None", "Other")**.</span></span>

    ![Stránka návrháře operace ER](./media/RCS-AppSpecParms-ConfigureFormat-ChangeLookupFld.PNG)
    
    <span data-ttu-id="45ceb-304">Všimněte si, že výraz v poli **Model.Data.Summary.Level** bude nyní vracet úroveň zdanění na základě kódu daně aktuálního záznamu a sady pravidel, které uživatel obchodního pravidla konfiguruje ve zdroji dat vyhledávání **Model.Data.Summary.Level**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-304">Notice that the expression of the **Model.Data.Summary.Level** field will now return the taxation level, based on the tax code of the current record and the set of rules that that a business user configures in the **Model.Data.Selector** lookup data source.</span></span>
    
5.  <span data-ttu-id="45ceb-305">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-305">Select **Save**.</span></span>
6.  <span data-ttu-id="45ceb-306">Zavřete stránku **Návrhář vzorce**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-306">Close **Formula designer** page.</span></span>
7.  <span data-ttu-id="45ceb-307">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-307">Select **OK**.</span></span>
8.  <span data-ttu-id="45ceb-308">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-308">Select **Save**.</span></span>
9.  <span data-ttu-id="45ceb-309">Zavřete stránku **návrháře formátu**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-309">Close **Format designer** page.</span></span>

## <a name="complete-the-draft-version-of-a-derived-format"></a><span data-ttu-id="45ceb-310">Dokončete koncept odvozeného formátu</span><span class="sxs-lookup"><span data-stu-id="45ceb-310">Complete the draft version of a derived format</span></span>

1.  <span data-ttu-id="45ceb-311">Na pevné záložce **Verze** vyberte možnost **Stav změny**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-311">On the **Versions** fast tab, select **Change status**.</span></span>
2.  <span data-ttu-id="45ceb-312">Zvolte **Dokončit**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-312">Select **Complete**.</span></span>
3.  <span data-ttu-id="45ceb-313">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-313">Select **OK**.</span></span>

## <a name="export-completed-version-of-modified-format"></a><span data-ttu-id="45ceb-314">Exportujte dokončenou verzi modifikovaného formátu</span><span class="sxs-lookup"><span data-stu-id="45ceb-314">Export completed version of modified format</span></span>

1.  <span data-ttu-id="45ceb-315">Ve stromu konfigurace vyberte položku **Formát pro ověření, jak vyhledat data LE**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-315">In the configuration tree, select the **Format to learn how to lookup LE data** item.</span></span>
2.  <span data-ttu-id="45ceb-316">Na pevné záložce **Verze** vyberte záznam se stavem **Dokončeno**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-316">On the **Versions** fast tab, select the record that has a status of **Completed**.</span></span>
3.  <span data-ttu-id="45ceb-317">Vyberte **Exchange**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-317">Select **Exchange**.</span></span>
4.  <span data-ttu-id="45ceb-318">Vyberte **Exportovat jako soubor XML**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-318">Select **Export as XML file**.</span></span>
5.  <span data-ttu-id="45ceb-319">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-319">Select **OK**.</span></span>
6.  <span data-ttu-id="45ceb-320">Webový prohlížeč stáhne soubor **Formát k zjištění, jak vyhledat data LE**.</span><span class="sxs-lookup"><span data-stu-id="45ceb-320">The web browser downloads a **Format to learn how to lookup LE data.xml** file.</span></span> <span data-ttu-id="45ceb-321">Tento soubor si uložte místně.</span><span class="sxs-lookup"><span data-stu-id="45ceb-321">Store this file locally.</span></span>

<span data-ttu-id="45ceb-322">Chcete-li se dozvědět, jak vyhledat formát **Formát k zjištění, jak vyhledat data LE**, zopakujte kroky v tomto oddílu a uložte si místně následující soubory.</span><span class="sxs-lookup"><span data-stu-id="45ceb-322">Repeat steps in this section for parent items of the **Format to learn how to lookup LE data** format, and store the following files locally:</span></span>

-   <span data-ttu-id="45ceb-323">Format to learn parameterized calls.xml</span><span class="sxs-lookup"><span data-stu-id="45ceb-323">Format to learn parameterized calls.xml</span></span>
-   <span data-ttu-id="45ceb-324">Mapping to learn parameterized calls.xml</span><span class="sxs-lookup"><span data-stu-id="45ceb-324">Mapping to learn parameterized calls.xml</span></span>
-   <span data-ttu-id="45ceb-325">Model to learn parameterized calls.xml</span><span class="sxs-lookup"><span data-stu-id="45ceb-325">Model to learn parameterized calls.xml</span></span>

<span data-ttu-id="45ceb-326">Pokud chcete zjistit, jak používat konfigurovaný formát ER **Formát k zjištění, jak vyhledávat data LE** pro nastavení sad daňových kódů závislých na právnické osobě k filtrování daňových transakcí podle různých úrovní zdanění, dokončete kroky v tématu [Nastavení parametrů formátu ER podle právnické osoby](er-app-specific-parameters-set-up.md).</span><span class="sxs-lookup"><span data-stu-id="45ceb-326">To learn how to use the configured **Format to learn how to lookup LE data** ER format to set up legal entity–dependent sets of tax codes to filter tax transactions by different taxation levels, complete the steps in the [Set up the parameters of an ER format per legal entity](er-app-specific-parameters-set-up.md) topic.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="45ceb-327">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="45ceb-327">Additional resources</span></span>

[<span data-ttu-id="45ceb-328">Návrhář receptur v elektronickém výkaznictví</span><span class="sxs-lookup"><span data-stu-id="45ceb-328">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="45ceb-329">Nastavení parametrů formátu ER podle právnické osoby</span><span class="sxs-lookup"><span data-stu-id="45ceb-329">Set up the parameters of an ER format per legal entity</span></span>](er-app-specific-parameters-set-up.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]