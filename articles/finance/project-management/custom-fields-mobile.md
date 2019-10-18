---
title: Implementace vlastních polí pro mobilní aplikaci Microsoft Dynamics 365 Project Timesheet na systéech iOS a Android
description: Toto téma poskytuje běžné vzory pro použití rozšíření k implementaci vlastních polí.
author: KimANelson
manager: AnnBe
ms.date: 05/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.dyn365.ops.version: 10.0.3
ms.search.validFrom: 2019-05-29
ms.openlocfilehash: 4343c875da05641c57b7784bf52f1c814dd26d20
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174782"
---
# <a name="implement-custom-fields-for-the-microsoft-dynamics-365-project-timesheet-mobile-app-on-ios-and-android"></a><span data-ttu-id="ca8bf-103">Implementace vlastních polí pro mobilní aplikaci Microsoft Dynamics 365 Project Timesheet na systéech iOS a Android</span><span class="sxs-lookup"><span data-stu-id="ca8bf-103">Implement custom fields for the Microsoft Dynamics 365 Project Timesheet mobile app on iOS and Android</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ca8bf-104">Toto téma poskytuje běžné vzory pro použití rozšíření k implementaci vlastních polí.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-104">This topic provides common patterns for using extensions to implement custom fields.</span></span> <span data-ttu-id="ca8bf-105">Jsou zde pokryta následující témata:</span><span class="sxs-lookup"><span data-stu-id="ca8bf-105">The following topics are covered:</span></span>

- <span data-ttu-id="ca8bf-106">Různé datové typy, které rozhraní vlastních polí podporuje</span><span class="sxs-lookup"><span data-stu-id="ca8bf-106">The various data types that the custom field framework supports</span></span>
- <span data-ttu-id="ca8bf-107">Jak v záznamech časového rozvrhu zobrazit pole jen pro čtení nebo upravitelná pole a uložit hodnoty zadané uživatelem zpět do databáze</span><span class="sxs-lookup"><span data-stu-id="ca8bf-107">How to show read-only or editable fields on timesheet entries, and save user-provided values back to the database</span></span>
- <span data-ttu-id="ca8bf-108">Jak zobrazit pole určená jen pro čtení v záhlaví časového rozvrhu</span><span class="sxs-lookup"><span data-stu-id="ca8bf-108">How to show read-only fields on the timesheet header</span></span>
- <span data-ttu-id="ca8bf-109">Jak integrovat jinou vlastní obchodní logiku pro zadávání výchozích hodnot v polích a provádět další ověření</span><span class="sxs-lookup"><span data-stu-id="ca8bf-109">How to integrate other custom business logic to enter default values in fields and do additional validation</span></span>

## <a name="audience"></a><span data-ttu-id="ca8bf-110">Cílová skupina</span><span class="sxs-lookup"><span data-stu-id="ca8bf-110">Audience</span></span>

<span data-ttu-id="ca8bf-111">Toto téma je určeno pro vývojáře, kteří integrují svá vlastní pole do mobilní aplikace Microsoft Dynamics 365 Project Timesheet, která je k dispozici pro systémy Apple iOS a Google Android.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-111">This topic is intended for developers who are integrating their custom fields into the Microsoft Dynamics 365 Project Timesheet mobile application that is available for Apple iOS and Google Android.</span></span> <span data-ttu-id="ca8bf-112">Předpokladem je, že čtenáři jsou obeznámeni s vývojem X ++ a funkcionalitou časových rozvrhů projektu.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-112">The assumption is that readers are familiar with X++ development and project timesheet functionality.</span></span>

## <a name="data-contract--tstimesheetcustomfield-x-class"></a><span data-ttu-id="ca8bf-113">Kontrakt dat – třída TSTimesheetCustomField X + +</span><span class="sxs-lookup"><span data-stu-id="ca8bf-113">Data contract – TSTimesheetCustomField X++ class</span></span>

<span data-ttu-id="ca8bf-114">Třída **TSTimesheetCustomField** je třídou kontraktu dat X ++, která představuje informace o vlastním poli pro funkcionalitu časového rozvrhu.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-114">The **TSTimesheetCustomField** class is the X++ data contract class that represents information about a custom field for timesheet functionality.</span></span> <span data-ttu-id="ca8bf-115">Seznamy objektů vlastního pole jsou předány jak na kontrakt dat TSTimesheetDetails, tak na kontrakt dat TSTimesheetEntry pro zobrazení vlastních polí v mobilní aplikaci.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-115">Lists of the custom field objects are passed on both the TSTimesheetDetails data contract and the TSTimesheetEntry data contract to show custom fields in the mobile app.</span></span>

- <span data-ttu-id="ca8bf-116">**TSTimesheetDetails** – Kontrakt záhlaví časového rozvrhu.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-116">**TSTimesheetDetails** - The timesheet header contract.</span></span>
- <span data-ttu-id="ca8bf-117">**TSTimesheetEntry** – Kontrakt transakce časového rozvrhu</span><span class="sxs-lookup"><span data-stu-id="ca8bf-117">**TSTimesheetEntry** - The timesheet transaction contract.</span></span> <span data-ttu-id="ca8bf-118">Skupiny těchto objektů, které mají stejné informace o projektu a hodnotu **timesheetLineRecId** tvoří jeden řádek.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-118">Groups of these objects that have the same project information and **timesheetLineRecId** value constitute a line.</span></span>

### <a name="fieldbasetype-types"></a><span data-ttu-id="ca8bf-119">fieldBaseType (typy)</span><span class="sxs-lookup"><span data-stu-id="ca8bf-119">fieldBaseType (Types)</span></span>

<span data-ttu-id="ca8bf-120">Vlastnost **FieldBaseType** na objektu **TsTimesheetCustom** určuje typ pole, které se zobrazí v aplikaci.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-120">The **FieldBaseType** property on the **TsTimesheetCustom** object determines the type of the field that appears in the app.</span></span> <span data-ttu-id="ca8bf-121">Jsou podporovány následující **typy** hodnot.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-121">The following **Types** values that are supported.</span></span>

| <span data-ttu-id="ca8bf-122">Hodnota typů</span><span class="sxs-lookup"><span data-stu-id="ca8bf-122">Types value</span></span> | <span data-ttu-id="ca8bf-123">Typ</span><span class="sxs-lookup"><span data-stu-id="ca8bf-123">Type</span></span>              | <span data-ttu-id="ca8bf-124">Poznámky</span><span class="sxs-lookup"><span data-stu-id="ca8bf-124">Notes</span></span> |
|-------------|-------------------|-------|
| <span data-ttu-id="ca8bf-125">0</span><span class="sxs-lookup"><span data-stu-id="ca8bf-125">0</span></span>           | <span data-ttu-id="ca8bf-126">Řetězec (a výčet)</span><span class="sxs-lookup"><span data-stu-id="ca8bf-126">String (and Enum)</span></span> | <span data-ttu-id="ca8bf-127">Pole se zobrazí jako textové pole.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-127">The field appears as a text field.</span></span> |
| <span data-ttu-id="ca8bf-128">1</span><span class="sxs-lookup"><span data-stu-id="ca8bf-128">1</span></span>           | <span data-ttu-id="ca8bf-129">Celé číslo</span><span class="sxs-lookup"><span data-stu-id="ca8bf-129">Integer</span></span>           | <span data-ttu-id="ca8bf-130">Hodnota se zobrazí jako číslo bez desetinných míst.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-130">The value is shown as a number without decimal places.</span></span> |
| <span data-ttu-id="ca8bf-131">2</span><span class="sxs-lookup"><span data-stu-id="ca8bf-131">2</span></span>           | <span data-ttu-id="ca8bf-132">Reálný</span><span class="sxs-lookup"><span data-stu-id="ca8bf-132">Real</span></span>              | <span data-ttu-id="ca8bf-133">Hodnota se zobrazí jako číslo s desetinnými místy.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-133">The value is shown as a number that has decimal places.</span></span><p><span data-ttu-id="ca8bf-134">Chcete-li v aplikaci zobrazit reálnou hodnotu jako měnu, použijte vlastnost **fieldExtenededType**.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-134">To show the real value as a currency in the app, use the **fieldExtenededType** property.</span></span> <span data-ttu-id="ca8bf-135">Pomocí vlastnosti **numberOfDecimals** můžete nastavit počet zobrazených desetinných míst.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-135">You can use the **numberOfDecimals** property to set the number of decimal places that are shown.</span></span></p> |
| <span data-ttu-id="ca8bf-136">3</span><span class="sxs-lookup"><span data-stu-id="ca8bf-136">3</span></span>           | <span data-ttu-id="ca8bf-137">Datum</span><span class="sxs-lookup"><span data-stu-id="ca8bf-137">Date</span></span>              | <span data-ttu-id="ca8bf-138">Formáty data jsou určeny nastavením **formátu data, času a čísel** uživatele, které je uvedeno v části **Předvolby jazyka a země/oblasti** pod volbou **Možnost uživatele**.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-138">Date formats are determined by the user's **Date, times, and number format** setting that is specified under **Language and country/region preference** in **User options**.</span></span> |
| <span data-ttu-id="ca8bf-139">4</span><span class="sxs-lookup"><span data-stu-id="ca8bf-139">4</span></span>           | <span data-ttu-id="ca8bf-140">Logická hodnota</span><span class="sxs-lookup"><span data-stu-id="ca8bf-140">Boolean</span></span>           | |
| <span data-ttu-id="ca8bf-141">15</span><span class="sxs-lookup"><span data-stu-id="ca8bf-141">15</span></span>          | <span data-ttu-id="ca8bf-142">GUID</span><span class="sxs-lookup"><span data-stu-id="ca8bf-142">GUID</span></span>              | |
| <span data-ttu-id="ca8bf-143">16</span><span class="sxs-lookup"><span data-stu-id="ca8bf-143">16</span></span>          | <span data-ttu-id="ca8bf-144">Int64</span><span class="sxs-lookup"><span data-stu-id="ca8bf-144">Int64</span></span>             | |

- <span data-ttu-id="ca8bf-145">Není-li na objektu **TSTimesheetCustomField** zadána vlastnost **stringOptions**, je uživateli poskytnuto pole s volným textem.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-145">If the **stringOptions** property isn't provided on the **TSTimesheetCustomField** object, a free-text field is provided to the user.</span></span>

    <span data-ttu-id="ca8bf-146">Vlastnost **stringLength** lze použít k nastavení maximální délky řetězce, kterou mohou uživatelé zadat.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-146">The **stringLength** property can be used to set the maximum string length that users can enter.</span></span>

- <span data-ttu-id="ca8bf-147">Je- li vlastnost **stringOptions** zadána na objektu **TSTimesheetCustomField**, budou tyto prvky seznamu jediné hodnoty, které mohou uživatelé vybrat pomocí tlačítek možností (přepínačů).</span><span class="sxs-lookup"><span data-stu-id="ca8bf-147">If the **stringOptions** property is provided on the **TSTimesheetCustomField** object, those list elements are the only values that users can select by using option buttons (radio buttons).</span></span>

    <span data-ttu-id="ca8bf-148">V tomto případě může pole řetězce sloužit jako hodnota výčtu pro účely zadání uživatele.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-148">In this case, the string field can act as an enum value for the purpose of user entry.</span></span> <span data-ttu-id="ca8bf-149">Chcete-li hodnotu uložit do databáze jako výčet, před uložením do databáze pomocí chain of command ručně, namapujte hodnotu řetězce zpět na hodnotu výčtu (příklad naleznete dále v tomto tématu v části „Použití chain of command v třídě TSTimesheetEntryService pro uložení záznamu časového rozvrhu z aplikace zpět do databáze“).</span><span class="sxs-lookup"><span data-stu-id="ca8bf-149">To save the value to the database as an enum, manually map the string value back to the enum value before you save to the database by using chain of command (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</span></span>

### <a name="fieldextendedtype-tscustomfieldextendedtype"></a><span data-ttu-id="ca8bf-150">fieldExtendedType (TSCustomFieldExtendedType)</span><span class="sxs-lookup"><span data-stu-id="ca8bf-150">fieldExtendedType (TSCustomFieldExtendedType)</span></span>

<span data-ttu-id="ca8bf-151">Tato vlastnost slouží k formátování reálných hodnot jako měny.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-151">You can use this property to format real values as currency.</span></span> <span data-ttu-id="ca8bf-152">Tento přístup je použitelný pouze v případě, že hodnota **fieldBaseType** je **reálná**.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-152">This approach is applicable only when the **fieldBaseType** value is **Real**.</span></span>

- <span data-ttu-id="ca8bf-153">**TSCustomFieldExtendedType: None** – Není použito žádné formátování.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-153">**TSCustomFieldExtendedType:None** – No formatting is applied.</span></span>
- <span data-ttu-id="ca8bf-154">**TSCustomFieldExtendedType::Currency** – Naformátuje hodnotu jako měnu.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-154">**TSCustomFieldExtendedType::Currency** – Format the value as currency.</span></span>

    <span data-ttu-id="ca8bf-155">Je-li formátování měny aktivní, pole **stringValue** lze použít k předání kódu měny, který by měl být zobrazen v aplikaci.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-155">When currency formatting is active, the **stringValue** field can be used pass the currency code that should be shown in the app.</span></span> <span data-ttu-id="ca8bf-156">Hodnota je pouze pro čtení.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-156">The value is a read-only value.</span></span>

    <span data-ttu-id="ca8bf-157">Pole **realValue** obsahuje peněžní částku, která má být uložena do databáze.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-157">The **realValue** field contains the money amount that should be saved to the database.</span></span>

### <a name="fieldsection-tscustomfieldsection"></a><span data-ttu-id="ca8bf-158">fieldSection (TSCustomFieldSection)</span><span class="sxs-lookup"><span data-stu-id="ca8bf-158">fieldSection (TSCustomFieldSection)</span></span>

<span data-ttu-id="ca8bf-159">Pomocí této vlastnosti můžete určit, kde se má vlastní pole zobrazit v aplikaci.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-159">You can use this property specify where the custom field should appear in the app.</span></span>

- <span data-ttu-id="ca8bf-160">**TSCustomFieldSection::Header** – Pole se zobrazí v části **Zobrazit více podrobností** v aplikaci.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-160">**TSCustomFieldSection::Header** – The field will appear in the **View more details** section in the app.</span></span> <span data-ttu-id="ca8bf-161">Tato pole jsou vždy pouze ke čtení.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-161">These fields are always read-only.</span></span>
- <span data-ttu-id="ca8bf-162">**TSCustomFieldSection::Line** – Pole se zobrazí po všech předdefinovaných polí řádků v záznamech časového rozvrhu.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-162">**TSCustomFieldSection::Line** – The field will appear after all the out-of-box line fields on timesheet entries.</span></span> <span data-ttu-id="ca8bf-163">Tato pole mohou být upravitelná nebo jen pro čtení.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-163">These fields can be either editable or read-only.</span></span>

### <a name="fieldname-fieldnameshort"></a><span data-ttu-id="ca8bf-164">fieldName (FieldNameShort)</span><span class="sxs-lookup"><span data-stu-id="ca8bf-164">fieldName (FieldNameShort)</span></span>

<span data-ttu-id="ca8bf-165">Tato vlastnost identifikuje pole, když hodnoty, které aplikace poskytuje, jsou uloženy zpět do databáze.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-165">This property identifies the field when values that the app provides are saved back to the database.</span></span>

### <a name="tablename-tablenameshort"></a><span data-ttu-id="ca8bf-166">tableName (TableNameShort)</span><span class="sxs-lookup"><span data-stu-id="ca8bf-166">tableName (TableNameShort)</span></span>

<span data-ttu-id="ca8bf-167">Tato vlastnost identifikuje pole, když hodnoty, které aplikace poskytuje, jsou uloženy zpět do databáze.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-167">This property identifies the field when values that the app provides are saved back to the database.</span></span>

### <a name="iseditable-noyes"></a><span data-ttu-id="ca8bf-168">isEditable (NoYes)</span><span class="sxs-lookup"><span data-stu-id="ca8bf-168">isEditable (NoYes)</span></span>

<span data-ttu-id="ca8bf-169">Chcete-li určit, že pole v části záznamu časového rozvrhu by mělo být pro uživatele upravitelné, nastavte tuto vlastnost na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-169">Set this property to **Yes** to specify that the field in the timesheet entry section should be editable by users.</span></span> <span data-ttu-id="ca8bf-170">Nastavením vlastnosti na **Ne** nastavíte pole jen pro čtení.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-170">Set the property to **No** to make the field read-only.</span></span>

### <a name="ismandatory-noyes"></a><span data-ttu-id="ca8bf-171">isMandatory (NoYes)</span><span class="sxs-lookup"><span data-stu-id="ca8bf-171">isMandatory (NoYes)</span></span>

<span data-ttu-id="ca8bf-172">Chcete-li určit, že pole v části záznamu časového rozvrhu by mělo být pro uživatele povinné, nastavte tuto vlastnost na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-172">Set this property to **Yes** to specify that the field in the timesheet entry section should be mandatory.</span></span>

### <a name="label-str"></a><span data-ttu-id="ca8bf-173">label (str)</span><span class="sxs-lookup"><span data-stu-id="ca8bf-173">label (str)</span></span>

<span data-ttu-id="ca8bf-174">Tato vlastnost určuje popisek zobrazený vedle pole v aplikaci.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-174">This property specifies the label that is shown next the field in the app.</span></span>

### <a name="stringoptions-list-of-strings"></a><span data-ttu-id="ca8bf-175">stringOptions (List of Strings)</span><span class="sxs-lookup"><span data-stu-id="ca8bf-175">stringOptions (List of Strings)</span></span>

<span data-ttu-id="ca8bf-176">Tuto vlastnost lze použít pouze tehdy, když je **fieldBaseType** nasteveno na **Řetězec**.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-176">This property is applicable only when **fieldBaseType** is set to **String**.</span></span> <span data-ttu-id="ca8bf-177">Když je nastavena hodnota **stringOptions**, hodnoty řetězců, které jsou k dispozici pro výběr prostřednictvím tlačítek možností (přepínačů), jsou určeny řetězci v seznamu.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-177">If **stringOptions** is set, the string values that are available for selection via option buttons (radio buttons) are specified by the strings in the list.</span></span> <span data-ttu-id="ca8bf-178">Nejsou-li zadány žádné řetězce, bude záznam s volným textem v poli řetězce povolen (příklad naleznete dále v tomto tématu v části „Použití chain of command v třídě TSTimesheetEntryService pro uložení záznamu časového rozvrhu z aplikace zpět do databáze“).</span><span class="sxs-lookup"><span data-stu-id="ca8bf-178">If no strings are provided, free-text entry in the string field is allowed (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</span></span>

### <a name="stringlength-int"></a><span data-ttu-id="ca8bf-179">stringLength (int)</span><span class="sxs-lookup"><span data-stu-id="ca8bf-179">stringLength (int)</span></span>

<span data-ttu-id="ca8bf-180">Tato vlastnost určuje maximální délku pole řetězců.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-180">This property specifies the maximum length for a string field.</span></span> <span data-ttu-id="ca8bf-181">Lze ji použít pouze tehdy, když je **fieldBaseType** nasteveno na **Řetězec**.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-181">It's applicable only when **fieldBaseType** is set to **String**.</span></span>

### <a name="numberofdecimals-int"></a><span data-ttu-id="ca8bf-182">numberOfDecimals (int)</span><span class="sxs-lookup"><span data-stu-id="ca8bf-182">numberOfDecimals (int)</span></span>

<span data-ttu-id="ca8bf-183">Tato vlastnost určuje počet desetinných míst, která se zobrazí u reálného pole.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-183">This property specifies the number of decimal places that are shown for a real field.</span></span> <span data-ttu-id="ca8bf-184">Lze ji použít pouze tehdy, když je **fieldBaseType** nasteveno na **Reálný**.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-184">It's applicable only when **fieldBaseType** is set to **Real**.</span></span>

### <a name="ordersequence-int"></a><span data-ttu-id="ca8bf-185">orderSequence (int)</span><span class="sxs-lookup"><span data-stu-id="ca8bf-185">orderSequence (int)</span></span>

<span data-ttu-id="ca8bf-186">Tato vlastnost řídí pořadí, ve kterém se vlastní pole zobrazí v aplikaci v případě, že je zadáno více než jedno vlastní pole.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-186">This property controls the order in which the custom fields are shown in the app when more than one custom field is specified.</span></span> <span data-ttu-id="ca8bf-187">Pole s nižšími čísly jsou zobrazena jako první.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-187">Fields that have lower numbers are shown first.</span></span>

### <a name="booleanvalue-boolean"></a><span data-ttu-id="ca8bf-188">booleanValue (boolean)</span><span class="sxs-lookup"><span data-stu-id="ca8bf-188">booleanValue (boolean)</span></span>

<span data-ttu-id="ca8bf-189">U polí typu **Logická hodnota** předává tato vlastnost logickou hodnotu pole mezi serverem a aplikací.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-189">For fields of the **Boolean** type, this property passes the Boolean value of the field between the server and the app.</span></span>

### <a name="guidvalue-guid"></a><span data-ttu-id="ca8bf-190">guidValue (guid)</span><span class="sxs-lookup"><span data-stu-id="ca8bf-190">guidValue (guid)</span></span>

<span data-ttu-id="ca8bf-191">U polí typu **GUID** předává tato vlastnost hodnotu identifikátoru GUID pole mezi serverem a aplikací.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-191">For fields of the **GUID** type, this property passes the globally unique identifier (GUID) value of the field between the server and the app.</span></span>

### <a name="int64value-int64"></a><span data-ttu-id="ca8bf-192">int64Value (Int64)</span><span class="sxs-lookup"><span data-stu-id="ca8bf-192">int64Value (int64)</span></span>

<span data-ttu-id="ca8bf-193">U polí typu **Int64** předává tato vlastnost hodnotu Int64 pole mezi serverem a aplikací.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-193">For fields of the **Int64** type, this property passes the int64 value of the field between the server and the app.</span></span>

### <a name="intvalue-int"></a><span data-ttu-id="ca8bf-194">intValue (int)</span><span class="sxs-lookup"><span data-stu-id="ca8bf-194">intValue (int)</span></span>

<span data-ttu-id="ca8bf-195">U polí typu **Int** předává tato vlastnost hodnotu int pole mezi serverem a aplikací.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-195">For fields of the **Int** type, this property passes the int value of the field between the server and the app.</span></span>

### <a name="realvalue-real"></a><span data-ttu-id="ca8bf-196">realValue (Real)</span><span class="sxs-lookup"><span data-stu-id="ca8bf-196">realValue (real)</span></span>

<span data-ttu-id="ca8bf-197">U polí typu **Reálné** předává tato vlastnost reálnou hodnotu pole mezi serverem a aplikací.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-197">For fields of the **Real** type, this property passes the real value of the field between the server and the app .</span></span>

### <a name="stringvalue-str"></a><span data-ttu-id="ca8bf-198">stringValue (str)</span><span class="sxs-lookup"><span data-stu-id="ca8bf-198">stringValue (str)</span></span>

<span data-ttu-id="ca8bf-199">U polí typu **Řetězec** předává tato vlastnost hodnotu řetězce pole mezi serverem a aplikací.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-199">For fields of the **String** type, this property passes the string value of the field between the server and the app.</span></span> <span data-ttu-id="ca8bf-200">Používá se také pro pole typu **Reálné**, která jsou formátována jako měna.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-200">It's also used for fields of the **Real** type that are formatted as currency.</span></span> <span data-ttu-id="ca8bf-201">Pro tato pole se vlastnost používá k předání kódu měny do aplikace.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-201">For those fields, the property is used to pass the currency code to the app.</span></span>

### <a name="datevalue-date"></a><span data-ttu-id="ca8bf-202">dateValue (date)</span><span class="sxs-lookup"><span data-stu-id="ca8bf-202">dateValue (date)</span></span>

<span data-ttu-id="ca8bf-203">U polí typu **Datum** předává tato vlastnost hodnotu data pole mezi serverem a aplikací.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-203">For fields of the **Date** type, this property passes the date value of the field between the server and the app.</span></span>

## <a name="show-and-save-a-custom-field-in-the-timesheet-entry-section"></a><span data-ttu-id="ca8bf-204">Zobrazení a uložení vlastního pole v části záznamu časového rozvrhu</span><span class="sxs-lookup"><span data-stu-id="ca8bf-204">Show and save a custom field in the timesheet entry section</span></span>

<span data-ttu-id="ca8bf-205">Níže je snímek obrazovky z mobilní aplikace zobrazující vytvoření záznamu časového rozvrhu.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-205">Below is a screenshot from the mobile app of a timesheet entry creation.</span></span> <span data-ttu-id="ca8bf-206">Zobrazuje předpřipravená pole a vlastní pole v části časového záznamu s názvem Testovací řetězec s již nastavenou hodnotou výčtu Druhá možnost.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-206">It shows the out-of-box fields and a custom field in the "Time entry" section called "Test string" with an enum value of "Second option" already set.</span></span>

![Vlastní pole testovacího řetězce v aplikaci](media/timesheet-entry.jpg)



<span data-ttu-id="ca8bf-208">Níže je snímek obrazovky z mobilní aplikace zobrazující uživatele, který vybere jednu z možností výčtu dostupných pro vlastní pole Testovací řetězec.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-208">Below is a screenshot from the mobile app of the user selecting one of the enum options available for the "Test string" custom field.</span></span>  <span data-ttu-id="ca8bf-209">Tyto dvě možnosti jsou První možnost a Druhá možnost, které jsou zobrazeny jako přepínací tlačítka.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-209">The two options are "First option" and "Second option" shown as radio buttons.</span></span> <span data-ttu-id="ca8bf-210">Aktuálně je vybrána druhá možnost.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-210">The second option is currently selected.</span></span>

![Tlačítka možností (přepínače) pro vlastní pole Testovací řetězec](media/enum-option.jpg)



### <a name="extend-the-tstimesheetline-table-so-that-it-has-a-custom-field"></a><span data-ttu-id="ca8bf-212">Rozšíření tabulky TSTimesheetLine tak, aby obsahovala vlastní pole</span><span class="sxs-lookup"><span data-stu-id="ca8bf-212">Extend the TSTimesheetLine table so that it has a custom field</span></span>

<span data-ttu-id="ca8bf-213">V typických scénářích je pravděpodobné, že data pro vlastní pole v části záznamu časového rozvrhu budou uložena do tabulky TSTimesheetLine.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-213">In typical scenarios, it's likely that the data for a custom field in the timesheet entry section will be saved to the TSTimesheetLine table.</span></span> <span data-ttu-id="ca8bf-214">Lze však použít i jiné tabulky, pokud je možné data načíst na základě poskytnutého záznamu TSTimesheetTrans, nebo pokud nemá specifický kontext záznamu (pokud je například pole v parametrech projektu nastaveno na hodnotu jen pro čtení).</span><span class="sxs-lookup"><span data-stu-id="ca8bf-214">However, other tables can be used if the data can be retrieved based on a TSTimesheetTrans record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</span></span>

<span data-ttu-id="ca8bf-215">Všimněte si, že vlastní pole nemusí mít žádné podpůrné záznamy databáze.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-215">Note that custom fields don't have to have any backing database records.</span></span> <span data-ttu-id="ca8bf-216">Lze je dynamicky generovat na základě logiky X ++.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-216">They can be dynamically generated based on X++ logic.</span></span> <span data-ttu-id="ca8bf-217">Tento přístup může být užitečný ve scénářích jen pro čtení (nahlédněte do části „Použití chain of command v třídě TSTimesheetDetails a metodě buildCustomFieldListForHeader pro vyplnění podrobností časového rozvrhu, kde je uveden přiklad dynamicky generovaných hodnot vlastních polí).</span><span class="sxs-lookup"><span data-stu-id="ca8bf-217">This approach can be useful in read-only scenarios (see the “Use chain of command on the TSTimesheetDetails class, buildCustomFieldListForHeader method to fill in timesheet details” section for an example of dynamically generated custom field values.)</span></span>

<span data-ttu-id="ca8bf-218">Níže je snímek obrazovky stromu aplikačních objektů z aplikace Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-218">Below is a screenshot from Visual Studio of the Application Object Tree.</span></span> <span data-ttu-id="ca8bf-219">Zobrazuje rozšíření tabulky TSTimesheetLine s polem TestLineString přidaným jako vlastní pole.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-219">It shows an extension of the TSTimesheetLine table with the TestLineString field added as a custom field.</span></span>

![Řetězec řádku](media/b6756b4a3fc5298093327a088a7710fd.png)

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-timesheet-entry-section"></a><span data-ttu-id="ca8bf-221">Použití chain of command v metodě buildCustomFieldList třídy TSTimesheetSettings pro zobrazení pole v části záznamu časového rozvrhu</span><span class="sxs-lookup"><span data-stu-id="ca8bf-221">Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the timesheet entry section</span></span>

<span data-ttu-id="ca8bf-222">Tento kód řídí nastavení zobrazení pro pole v aplikaci.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-222">This code controls the display settings for the field in the app.</span></span> <span data-ttu-id="ca8bf-223">Například řídí typ pole, popisek, zda je pole povinné a v jaké části se pole zobrazí.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-223">For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</span></span>

<span data-ttu-id="ca8bf-224">V následujícím příkladu je pole řetězce uvedeno v časových záznamech.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-224">The following example shows a string field on time entries.</span></span> <span data-ttu-id="ca8bf-225">Toto pole obsahuje dvě možnosti, **První možnost** a **Druhá možnost**, které jsou k dispozici prostřednictvím tlačítek možností (přepínačů).</span><span class="sxs-lookup"><span data-stu-id="ca8bf-225">This field has two options, **First option** and **Second option**, that are available via option buttons (radio buttons).</span></span> <span data-ttu-id="ca8bf-226">Pole v aplikaci je přidruženo k poli **TestLineString**, které je přidáno do tabulky TSTimesheetLine.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-226">The field in the app is associated with the **TestLineString** field that is added to the TSTimesheetLine table.</span></span>

<span data-ttu-id="ca8bf-227">Všimněte si použití metody **TSTimesheetCustomField::newFromMetatdata()** pro zjednodušení inicializace vlastností vlastních polí: **fieldBaseType**, **tableName**, **fieldname**, **label**, **isEditable**, **isMandatory**, **stringLength**, and **numberOfDecimals**.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-227">Note the use of the **TSTimesheetCustomField::newFromMetatdata()** method to simplify the initialization of the custom field properties: **fieldBaseType**, **tableName**, **fieldname**, **label**, **isEditable**, **isMandatory**, **stringLength**, and **numberOfDecimals**.</span></span> <span data-ttu-id="ca8bf-228">Tyto parametry lze také nastavit ručně podle potřeby.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-228">You can also set these parameters manually, as you prefer.</span></span>

```
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('Second option');
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforentry-method-of-the-tstimesheetentry-class-to-enter-values-in-a-timesheet-entry"></a><span data-ttu-id="ca8bf-229">Použití chain of command v metodě buildCustomFieldListForEntry třídy TSTimesheetEntry pro zadání hodnot v záznamu časového rozvrhu</span><span class="sxs-lookup"><span data-stu-id="ca8bf-229">Use chain of command on the buildCustomFieldListForEntry method of the TSTimesheetEntry class to enter values in a timesheet entry</span></span>

<span data-ttu-id="ca8bf-230">Metoda **buildCustomFieldListForEntry** slouží k zadávání hodnot do uložených řádků časového rozvrhu v mobilní aplikaci.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-230">The **buildCustomFieldListForEntry** method is used to enter values on the saved timesheet lines in the mobile app.</span></span> <span data-ttu-id="ca8bf-231">Bere záznam TSTimesheetTrans jako parametr.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-231">It takes a TSTimesheetTrans record as a parameter.</span></span> <span data-ttu-id="ca8bf-232">Pole z tohoto záznamu lze použít k vyplnění hodnoty vlastního pole v aplikaci.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-232">Fields from that record can be used to fill in the custom field value in the app.</span></span>

```
...
[ExtensionOf(classStr(TsTimesheetEntry))]
final class TsTimesheetEntry_Extension
{
    protected List buildCustomFieldListForEntry(TSTimesheetTrans _tsTimesheetTrans)
    {
        List customFieldList = next buildCustomFieldListForEntry(_tsTimesheetTrans);
        TSTimesheetLine tsTimesheetLine = _tsTimesheetTrans.timesheetLine();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        tsTimesheetCustomField.parmStringValue(tsTimesheetLine.TestLineString);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('second option;);
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-tstimesheetentryservice-class-to-save-a-timesheet-entry-from-the-app-back-to-the-database"></a><span data-ttu-id="ca8bf-233">Použití chain of command v třídě TSTimesheetEntryService pro uložení záznamu časového rozvrhu z aplikace zpět do databáze</span><span class="sxs-lookup"><span data-stu-id="ca8bf-233">Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database</span></span>

<span data-ttu-id="ca8bf-234">Chcete-li uložit vlastní pole zpět do databáze v typickém použití, je nutné rozšířit více metod:</span><span class="sxs-lookup"><span data-stu-id="ca8bf-234">To save a custom field back to the database in typical usage, you must extend multiple methods:</span></span>

- <span data-ttu-id="ca8bf-235">Metoda **timesheetLineNeedsUpdating** slouží k určení, zda byl záznam řádku uživatelem v aplikaci změněn a musí být uložen do databáze.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-235">The **timesheetLineNeedsUpdating** method is used to determine whether the line record has been changed by the user in the app and must be saved to the database.</span></span> <span data-ttu-id="ca8bf-236">Pokud není problémem výkonnost, lze tuto metodu zjednodušit, aby vždy vracela hodnotu **true**.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-236">If performance isn't a concern, this method can be simplified so that it always returns **true**.</span></span>
- <span data-ttu-id="ca8bf-237">Metody **populateTimesheetLineFromEntryDuringCreate** a **populateTimesheetLineFromEntryDuringUpdate** mohou být rozšířeny tak, aby do databázového záznamu TSTimesheetLine zadávaly hodnoty z TSTimesheetEntry ze zadaného záznamu kontraktu dat.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-237">The **populateTimesheetLineFromEntryDuringCreate** and **populateTimesheetLineFromEntryDuringUpdate** methods can be extended so that they enter values in the TSTimesheetLine database record from the TSTimesheetEntry data contract record that is provided.</span></span> <span data-ttu-id="ca8bf-238">V následujícím příkladu si všimněte, jak se provádí mapování mezi polem databáze a polem záznamu ručně pomocí kódu X ++.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-238">In the example that follows, notice how the mapping between the database field and the entry field is manually done via X++ code.</span></span>
- <span data-ttu-id="ca8bf-239">Metodu **populateTimesheetWeekFromEntry** lze rovněž rozšířit, pokud vlastní pole, které je mapováno na objekt **TSTimesheetEntry**, musí zapisovat zpět do tabulky tabulky databáze TSTimesheetLineweek.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-239">The **populateTimesheetWeekFromEntry** method can also be extended if the custom field that is mapped to the **TSTimesheetEntry** object must write back to the TSTimesheetLineweek database table.</span></span>

> [!NOTE]
> <span data-ttu-id="ca8bf-240">Následující příklad ukládá hodnotu **firstOption** nebo **secondOption** vybranou uživatelem do databáze jako neupravenou hodnotu řetězce.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-240">The following example saves the **firstOption** or **secondOption** value that the user selects to the database as a raw string value.</span></span> <span data-ttu-id="ca8bf-241">Je-li pole databáze typem pole **Výčet**, lze tyto hodnoty ručně namapovat na hodnotu výčtu a poté je uložit do pole výčtu v tabulce databáze.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-241">If the database field is a field of the **Enum** type, those values can be manually mapped to an enum value and then saved to an enum field on the database table.</span></span>

```
...
[ExtensionOf(classStr(TSTimesheetEntryService))]
final class TSTimesheetEntryService_Extension
{
    protected boolean timesheetLineNeedsUpdating(TSTimesheetLine _tsTimesheetLine,
    TsTimesheetEntry _tsTimesheetEntry)
    {
        boolean ret = next timesheetLineNeedsUpdating(_tsTimesheetLine,
        _tsTimesheetEntry);
        if (!ret)
        {
            */ Loop through custom fields to see if value needs updating*/
            ListEnumerator enumerator =  _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    */ If Custom field value for TestLineString field has changed, We need to update the timesheet line.*/
                    if (_tsTimesheetLine.TestLineString != customField.parmStringValue())
                    {
                        ret = true;
                    }
                }
            }
        }
        return ret;
    }
    protected void populateTimesheetLineFromEntryDuringCreate(TSTimesheetLine
    _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
    {
        next populateTimesheetLineFromEntryDuringCreate(_tsTimesheetLine,
        _tsTimesheetEntry);
        this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
        _tsTimesheetEntry);
        }
        protected void populateTimesheetLineFromEntryDuringUpdate(TSTimesheetLine
        \_tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            next populateTimesheetLineFromEntryDuringUpdate(_tsTimesheetLine,
            _tsTimesheetEntry);
            this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
            _tsTimesheetEntry);
        }
        private void populateTimesheetLineFromCustomFields(TSTimesheetLine
        _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            ListEnumerator enumerator =
            _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    _tsTimesheetLine.TestLineString = customField.parmStringValue();
                }
            }
        }
    }
...
```

## <a name="show-a-custom-field-in-the-timesheet-header-section"></a><span data-ttu-id="ca8bf-242">Zobrazení vlastního pole v části záhlaví časového rozvrhu</span><span class="sxs-lookup"><span data-stu-id="ca8bf-242">Show a custom field in the timesheet header section</span></span>

<span data-ttu-id="ca8bf-243">Níže je uveden snímek obrazovky z mobilní aplikace uživatele, který si prohlíží časový rozvrh.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-243">Below is a screenshot from the mobile app of a user viewing a timesheet.</span></span> <span data-ttu-id="ca8bf-244">Tlačítko Další informace bylo vybráno v pravém horním rohu k zobrazení možnosti Zobrazit další podrobnosti.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-244">The "More information" button has been selected in the upper-right corner to show the "View more details" option.</span></span>  

![Příkaz Zobrazit další podrobnosti](media/show-more.png)



<span data-ttu-id="ca8bf-246">Níže je uveden snímek obrazovky z mobilní aplikace s částí časového rozvrhu Další.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-246">Below is a screenshot from the mobile app showing the “More” section of a timesheet.</span></span> <span data-ttu-id="ca8bf-247">Do části záhlaví časového rozvrhu bylo přidáno vlastní pole s názvem Míra využití tohoto časového rozvrhu (vypočítané vlastní pole).</span><span class="sxs-lookup"><span data-stu-id="ca8bf-247">A custom field called “Utilization rate of this timesheet (computed custom field)” has been added to the timesheet header section.</span></span> <span data-ttu-id="ca8bf-248">U vlastního pole je nastavena hodnota 0,667 jen pro čtení.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-248">A read-only value of "0.667" is set on the custom field.</span></span>

![Část Další](media/more-section.jpg)



### <a name="extend-the-tstimesheettable-table-so-that-it-has-a-custom-field"></a><span data-ttu-id="ca8bf-250">Rozšíření tabulky TSTimesheetTable tak, aby obsahovala vlastní pole</span><span class="sxs-lookup"><span data-stu-id="ca8bf-250">Extend the TSTimesheetTable table so that it has a custom field</span></span>

<span data-ttu-id="ca8bf-251">V typických scénářích je pravděpodobné, že data pro vlastní pole v části záhlaví budou načtena z tabulky TSTimesheetHeader.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-251">In typical scenarios, it's likely that the data for a custom field in the header section will be pulled from the TSTimesheetHeader table.</span></span> <span data-ttu-id="ca8bf-252">Lze však použít i jiné tabulky, pokud je možné data načíst na základě poskytnutého záznamu TSTimesheetTable, nebo pokud nemá specifický kontext záznamu (pokud je například pole v parametrech projektu nastaveno na hodnotu jen pro čtení).</span><span class="sxs-lookup"><span data-stu-id="ca8bf-252">However, other tables can be used if the data can be retrieved based on a TSTimesheetTable record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</span></span>

<span data-ttu-id="ca8bf-253">Všimněte si, že vlastní pole nemusí mít žádné podpůrné záznamy databáze.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-253">Note that custom fields don't have to have any backing database records.</span></span> <span data-ttu-id="ca8bf-254">Lze je dynamicky generovat na základě logiky X ++.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-254">They can be dynamically generated based on X++ logic.</span></span> <span data-ttu-id="ca8bf-255">Tento přístup je uveden v následujícím příkladu.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-255">The example that follows shows this approach.</span></span>

<span data-ttu-id="ca8bf-256">Pole v části záhlaví jsou v aplikaci vždy jen pro čtení.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-256">Fields in the header section are always read-only in the app.</span></span>

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-header-section"></a><span data-ttu-id="ca8bf-257">Použití chain of command v metodě buildCustomFieldList třídy TSTimesheetSettings pro zobrazení pole v části header</span><span class="sxs-lookup"><span data-stu-id="ca8bf-257">Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the header section</span></span>

<span data-ttu-id="ca8bf-258">Tento kód řídí nastavení zobrazení pro pole v aplikaci.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-258">This code controls the display settings for the field in the app.</span></span> <span data-ttu-id="ca8bf-259">Například řídí typ pole, popisek, zda je pole povinné a v jaké části se pole zobrazí.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-259">For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</span></span>

<span data-ttu-id="ca8bf-260">Následující příklad ukazuje vypočítanou hodnotu v části záhlaví v aplikaci.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-260">The following example shows a computed value in the header section in the app.</span></span>

```
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforheader-method-of-the-tstimesheetdetails-class-to-fill-in-timesheet-details"></a><span data-ttu-id="ca8bf-261">Použití chain of command v metodě buildCustomFieldListForHeader třídy TSTimesheetDetails pro vyplnění podrobností časového rozvrhu</span><span class="sxs-lookup"><span data-stu-id="ca8bf-261">Use chain of command on the buildCustomFieldListForHeader method of the TSTimesheetDetails class to fill in timesheet details</span></span>

<span data-ttu-id="ca8bf-262">Metoda **buildCustomFieldListForHeader** slouží k vyplnění podrobností záhlaví časového rozvrhu v mobilní aplikaci.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-262">The **buildCustomFieldListForHeader** method is used to fill in the timesheet header details in the mobile app.</span></span> <span data-ttu-id="ca8bf-263">Bere záznam TSTimesheetTable jako parametr.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-263">It takes a TSTimesheetTable record as a parameter.</span></span> <span data-ttu-id="ca8bf-264">Pole z tohoto záznamu lze použít k vyplnění hodnoty vlastního pole v aplikaci.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-264">Fields from that record can be used to fill in the custom field value in the app.</span></span> <span data-ttu-id="ca8bf-265">Následující příklad nečte žádné hodnoty z databáze.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-265">The following example doesn't read any values from the database.</span></span> <span data-ttu-id="ca8bf-266">Místo toho používá logiku X ++ k vygenerování vypočtené hodnoty, která je pak zobrazena v aplikaci.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-266">Instead, it uses X++ logic to generate a computed value that is then shown in the app.</span></span>


```
...
[ExtensionOf(classStr(TSTimesheetDetails))]
final class TSTimesheetDetails_Extension
{
    protected List buildCustomFieldListForHeader(TSTimesheetTable
    _tsTimesheetTable)
    {
        List customFieldList = next buildCustomFieldListForHeader(_tsTimesheetTable);
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        real utilizationRate = 0;
        if (_tsTimesheetTable.totalHours() != 0)
        {
            utilizationRate = _tsTimesheetTable.totalHoursBillable() /
            _tsTimesheetTable.totalHours();
        }
        tsTimesheetCustomField.parmRealValue(utilizationRate);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

## <a name="other-configurabilityextensibility-opportunities"></a><span data-ttu-id="ca8bf-267">Další možnosti konfigurovatelnosti a rozšiřitelnosti</span><span class="sxs-lookup"><span data-stu-id="ca8bf-267">Other configurability/extensibility opportunities</span></span>

### <a name="adding-additional-validation-for-the-app"></a><span data-ttu-id="ca8bf-268">Přidání dalšího ověřování pro aplikaci</span><span class="sxs-lookup"><span data-stu-id="ca8bf-268">Adding additional validation for the app</span></span>

<span data-ttu-id="ca8bf-269">Existující logika pro funkci časového rozvrhu na úrovni databáze bude stále fungovat očekávaným způsobem.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-269">Existing logic for timesheet functionality at the database level will still work as expected.</span></span> <span data-ttu-id="ca8bf-270">Chcete-li přerušit dokončení operací uložení nebo odeslání a zobrazit určitou chybovou zprávu, můžete ke kódu přidat **throw error("message to user")** prostřednictvím rozšíření chain of command.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-270">To interrupt the completion of save or submit operations and show a specific error message, you can add **throw error("message to user")** to the code via a chain of command extension.</span></span> <span data-ttu-id="ca8bf-271">Zde jsou tři příklady užitečných metod rozšiřitelnosti:</span><span class="sxs-lookup"><span data-stu-id="ca8bf-271">Here are three examples of useful extensible methods:</span></span>

- <span data-ttu-id="ca8bf-272">Pokud **validateWrite** v tabulce TSTimesheetLine vrátí během operace uložení hodnotu **false** pro řádek časového rozvrhu, zobrazí se v mobilní aplikaci chybová zpráva.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-272">If **validateWrite** on the TSTimesheetLine table returns **false** during a save operation for a timesheet line, an error message is shown in the mobile app.</span></span>
- <span data-ttu-id="ca8bf-273">Pokud **validateSubmit** v tabulce TSTimesheetTable vrátí během odeslání časového rozvrhu v aplikaci hodnotu **false**, zobrazí se uživateli chybová zpráva.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-273">If **validateSubmit** on the TSTimesheetTable table returns **false** during timesheet submission in the app, an error message is shown to the user.</span></span>
- <span data-ttu-id="ca8bf-274">Logika, která vyplňuje pole (například **Vlastnost řádku**) během metody **insert** v tabulce TSTimesheetLine, bude stále spuštěna.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-274">Logic that fills in fields (for example, **Line Property**) during the **insert** method on the TSTimesheetLine table will still run.</span></span>

### <a name="hiding-and-marking-out-of-box-fields-as-read-only-via-configuration"></a><span data-ttu-id="ca8bf-275">Skrytí a označení předdefinovaných polí jako jen pro čtení pomocí konfigurace</span><span class="sxs-lookup"><span data-stu-id="ca8bf-275">Hiding and marking out-of-box fields as read-only via configuration</span></span>

<span data-ttu-id="ca8bf-276">Z parametrů projektu můžete změnit předdefinovaná pole na jen pro čtení nebo skrytá v mobilní aplikaci.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-276">From the project parameters, you can make out-of-box fields read-only or hidden in the mobile app.</span></span> <span data-ttu-id="ca8bf-277">Nastavte možnosti v části **Mobilní časové rozvrhy** na kartě **Časový rozvrh** na stránce **Parametry modulu Řízení a účetnictví projektu**.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-277">Set the options in the **Mobile timesheets** section on the **Timesheet** tab of the **Project management and accounting parameters** page.</span></span>

![Parametry projektu](media/5753b8ecccd1d8bb2b002dd538b3f762.png)

### <a name="changing-the-activities-that-are-available-for-selection-via-extensions"></a><span data-ttu-id="ca8bf-279">Změna aktivit, které jsou k dispozici pro výběr prostřednictvím rozšíření</span><span class="sxs-lookup"><span data-stu-id="ca8bf-279">Changing the activities that are available for selection via extensions</span></span>

<span data-ttu-id="ca8bf-280">Aktivity, které jsou k dispozici pro výběr pro projekt, jsou vyplněny pomocí metod **getActivitiesForProject()** a **getActivityQuery()** ve třídě **TsTimesheetProjectService**.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-280">The activities that are available for selection for a project are filled in via the **getActivitiesForProject()** and **getActivityQuery()** methods in the **TsTimesheetProjectService** class.</span></span> <span data-ttu-id="ca8bf-281">Pomocí chain of command můžete toto chování změnit tak, aby vyhovovalo vašemu obchodnímu scénáři pro aktivity, které jsou k dispozici pro výběr pro určitý projekt.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-281">You can use chain of command to change this behavior to match your business scenario for the activities that are available for selection for a specific project.</span></span>

### <a name="entering-a-default-project-category-on-timesheet-entries"></a><span data-ttu-id="ca8bf-282">Zadání výchozí kategorie projektu do záznamů časového rozvrhu</span><span class="sxs-lookup"><span data-stu-id="ca8bf-282">Entering a default project category on timesheet entries</span></span>

<span data-ttu-id="ca8bf-283">Zadání výchozí kategorie projektu do záznamů časového rozvrhu se uskutečňuje na třech úrovních.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-283">Entry of a default project category on timesheet entries occurs at three levels.</span></span> <span data-ttu-id="ca8bf-284">Pomocí chain of command můžete rozšířit chování na některé nebo všechny tyto úrovně a dosáhnout požadovaného chování.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-284">You can use chain of command to extend the behavior at any or all of these levels to achieve the desired behavior.</span></span> <span data-ttu-id="ca8bf-285">Použije se následující hierarchie:</span><span class="sxs-lookup"><span data-stu-id="ca8bf-285">The following hierarchy is used:</span></span>

1. <span data-ttu-id="ca8bf-286">Aplikace se pokusí vložit výchozí kategorii ze zdroje projektu.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-286">The app tries to put the default category from the project resource.</span></span> <span data-ttu-id="ca8bf-287">Tato výchozí kategorie se nastavuje v metodách **getCurrentUserResource** a **getDelegatedResourcesForCurrentUser** ve třídě **TSTimesheetSettingsService**.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-287">This default category is set in the **getCurrentUserResource** and **getDelegatedResourcesForCurrentUser** methods in the **TSTimesheetSettingsService** class.</span></span>
2. <span data-ttu-id="ca8bf-288">Není-li výchozí kategorie zadána na úrovni zdroje projektu, aplikace se pokusí ji načíst z aktivity projektu.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-288">If the default category isn't provided at the project resource level, the app tries to pull it from the project activity.</span></span> <span data-ttu-id="ca8bf-289">Tato výchozí kategorie se nastavuje v metodě **getActivitiesForProject** ve třídě **TSTimesheetProjectService**.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-289">This default category is set in the **getActivitiesForProject** method in the **TSTimesheetProjectService** class.</span></span>
3. <span data-ttu-id="ca8bf-290">Není-li výchozí kategorie zadána na úrovni aktivity projektu, vezme se výchozí kategorie z parametrů projektu.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-290">If the default category isn't provided at the project activity level, the default category it taken from the project parameters.</span></span> <span data-ttu-id="ca8bf-291">Tato výchozí kategorie se nastavuje v metodě **getProjectDetailsbyRule** ve třídě **TSTimesheetProjectService**.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-291">This default category is set in the **getProjectDetailsbyRule** method in the **TSTimesheetProjectService** class.</span></span>
