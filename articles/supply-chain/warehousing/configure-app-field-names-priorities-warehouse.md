---
title: Konfigurace polí pro mobilní aplikaci Řízení skladu
description: Toto téma popisuje, jak definovat a konfigurovat názvy a priority polí v mobilní aplikaci Řízení skladu.
author: MarkusFogelberg
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSMobileAppField, WHSMobileAppFieldPriority
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269434
ms.assetid: 6cf3d7da-29bb-4d3d-aaf5-544ca9cc2980
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: c6ed726536085b836f4014c59ea8df4755577ab5
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808815"
---
# <a name="configure-fields-for-the-warehouse-management-mobile-app"></a><span data-ttu-id="37c26-103">Konfigurace polí pro mobilní aplikaci Řízení skladu</span><span class="sxs-lookup"><span data-stu-id="37c26-103">Configure fields for the Warehouse Management mobile app</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="37c26-104">Toto téma popisuje, jak definovat a konfigurovat názvy a priority polí v mobilní aplikaci Řízení skladu.</span><span class="sxs-lookup"><span data-stu-id="37c26-104">This topic describes how to define and configure names and priorities of fields shown in the Warehouse Management mobile app.</span></span>

> [!NOTE]
> <span data-ttu-id="37c26-105">Toto téma se vztahuje k funkcím v modulu Řízení skladu.</span><span class="sxs-lookup"><span data-stu-id="37c26-105">This topic applies to features in Warehouse management.</span></span> <span data-ttu-id="37c26-106">Nevztahuje se na funkce v modulu Řízení zásob.</span><span class="sxs-lookup"><span data-stu-id="37c26-106">It doesn’t apply to features in Inventory management.</span></span> <span data-ttu-id="37c26-107">Mobilní aplikace Řízení skladu je aplikace, která slouží k provádění úloh skladu.</span><span class="sxs-lookup"><span data-stu-id="37c26-107">The Warehouse Management mobile app is an application that you can use to perform warehouse tasks.</span></span> <span data-ttu-id="37c26-108">Je možné definovat a konfigurovat názvy polí použitých v aplikaci, jakož i konfigurovat priority, do kterých by měly být přiřazeny názvy polí.</span><span class="sxs-lookup"><span data-stu-id="37c26-108">You can define and configure the field names that are used in the app, as well as configure the priority to which the field names should be assigned.</span></span> <span data-ttu-id="37c26-109">Toto téma vysvětluje, jak definovat a konfigurovat tyto názvy a priority polí mobilní aplikace Řízení skladu, a zároveň způsob jejich použití.</span><span class="sxs-lookup"><span data-stu-id="37c26-109">This topic explains how to define and configure these Warehouse Management mobile app field names and priorities, and how they are used.</span></span>

## <a name="configure-warehouse-app-field-names"></a><span data-ttu-id="37c26-110">Konfigurace názvů polí aplikace skladu</span><span class="sxs-lookup"><span data-stu-id="37c26-110">Configure warehouse app field names</span></span>

<span data-ttu-id="37c26-111">Použijete-li aplikaci Warehousing na svém mobilním zařízení, můžete nakonfigurovat, jakým způsobem se zobrazí metadata na vašem zařízení na stránce **Názvy polí aplikace skladu**.</span><span class="sxs-lookup"><span data-stu-id="37c26-111">When you use Warehousing on your mobile device, you can configure how metadata should be displayed on your device on the **Warehouse app field names** page.</span></span> <span data-ttu-id="37c26-112">V nové společnosti vyberte možnost **Vytvořit výchozí nastavení** pro vygenerování názvů všech polí, které budou použity ve workflow skladu na mobilním zařízení, přiřaďte jim upřednostňovaný vstupní režim a typ vstupu.</span><span class="sxs-lookup"><span data-stu-id="37c26-112">In a new company, select **Create default setup** to generate all field names that will be used in the warehouse mobile device workflows, and then assign a preferred input mode and input type to them.</span></span> <span data-ttu-id="37c26-113">Po vygenerování všech názvů polí můžete vybrat následující možnosti vstupu.</span><span class="sxs-lookup"><span data-stu-id="37c26-113">After you have generated all field names, you can select the following input options.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="37c26-114">Parametr</span><span class="sxs-lookup"><span data-stu-id="37c26-114">Option</span></span></th>
<th><span data-ttu-id="37c26-115">popis</span><span class="sxs-lookup"><span data-stu-id="37c26-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="37c26-116">Upřednostňovaný režim vstupu</span><span class="sxs-lookup"><span data-stu-id="37c26-116">Preferred input mode</span></span></td>
<td><span data-ttu-id="37c26-117">Tato možnost určuje, zda se mají pro zvolený název pole zobrazovat prohledávací pole nebo vstupní pole ručního zadávání.</span><span class="sxs-lookup"><span data-stu-id="37c26-117">This option defines whether a scanning field or a manual entry input field should be shown for the selected field name.</span></span> <span data-ttu-id="37c26-118">To je užitečné k rozlišení polí v závislosti na tom, zda se používají pro pole čárové kódy.</span><span class="sxs-lookup"><span data-stu-id="37c26-118">This is useful to distinguish fields depending on if barcodes are used for the field.</span></span> <span data-ttu-id="37c26-119"><strong>Poznámka:</strong> Pro názvy polí s upřednostňovaným vstupním režimem nastaveným na <strong>Vyhledávání</strong> můžete zadat informace ručně, pokud není čárový kód čitelný nebo je poškozen.</span><span class="sxs-lookup"><span data-stu-id="37c26-119"><strong>Note:</strong> For field names with preferred input mode set to <strong>Scanning</strong>, you can enter information manually if the barcode is unreadable or damaged.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37c26-120">Vstupní typ</span><span class="sxs-lookup"><span data-stu-id="37c26-120">Input type</span></span></td>
<td><span data-ttu-id="37c26-121">Tato možnost určuje, jaký typ vstupu má být použit pro název vybraného pole.</span><span class="sxs-lookup"><span data-stu-id="37c26-121">This option defines what input type should be used for the selected field name.</span></span> <span data-ttu-id="37c26-122">K dispozici jsou čtyři možnosti:</span><span class="sxs-lookup"><span data-stu-id="37c26-122">Four options are available:</span></span>
<ul>
<li><span data-ttu-id="37c26-123"><strong>Výběr </strong> - Obsahuje seznam možností k výběru.</span><span class="sxs-lookup"><span data-stu-id="37c26-123"><strong>Selection</strong> - Contains a list of options to choose from.</span></span> <span data-ttu-id="37c26-124">Názvy polí s touto možností nejsou upravitelné.</span><span class="sxs-lookup"><span data-stu-id="37c26-124">Field names with this option are not editable.</span></span></li>
<li><span data-ttu-id="37c26-125"><strong>Datum</strong> - Názvy polí specifikované jako datum zobrazí formát data s popiskem.</span><span class="sxs-lookup"><span data-stu-id="37c26-125"><strong>Date</strong> - Field names specified as date will show a date format with the label.</span></span> <span data-ttu-id="37c26-126">To pomáhá pracovníkům skladu zjistit, v jakém formátu zadat datum.</span><span class="sxs-lookup"><span data-stu-id="37c26-126">This helps warehouse workers see in which format to enter the date.</span></span> <span data-ttu-id="37c26-127">Názvy polí s touto možností nejsou upravitelné.</span><span class="sxs-lookup"><span data-stu-id="37c26-127">Field names with this option are not editable.</span></span></li>
<li><span data-ttu-id="37c26-128"><strong>Alfa</strong> - Je-li tato možnost vybrána, použije se při ručním zadávání informací do aplikace klávesnice zařízení.</span><span class="sxs-lookup"><span data-stu-id="37c26-128"><strong>Alpha</strong> - If selected, the device keyboard will be used when entering information manually in the app.</span></span> <span data-ttu-id="37c26-129">Vlastnosti klávesnice lze změnit podle toho, na kterém zařízení se používá.</span><span class="sxs-lookup"><span data-stu-id="37c26-129">The keyboard experience can be changed depending on which device is used.</span></span></li>
<li><span data-ttu-id="37c26-130"><strong>Číselný</strong> - Pro názvy polí používající pouze číselné vstupy můžete vybrat tuto možnost, chcete-li zobrazit vlastní numerickou klávesnici s vstupní polem místo klávesnice zařízení.</span><span class="sxs-lookup"><span data-stu-id="37c26-130"><strong>Numeric</strong> - For field names that use numeric input only, you can select this option to display a custom numeric keypad with the input field instead of the device keyboard.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="configure-warehouse-app-field-priority"></a><span data-ttu-id="37c26-131">Konfigurace priority pole aplikace skladu</span><span class="sxs-lookup"><span data-stu-id="37c26-131">Configure warehouse app field priority</span></span>

<span data-ttu-id="37c26-132">Na stránce **Priorita pole aplikace skladu** můžete umístit názvy polí do různých skupin priority.</span><span class="sxs-lookup"><span data-stu-id="37c26-132">On the **Warehouse app field priority** page, you can put field names into different priority groups.</span></span> <span data-ttu-id="37c26-133">Díky tomu je možné se rozhodnout, jaké informace mají být zobrazeny na hlavní stránce úloh, když pracovníci skladu provádět úlohy pomocí této aplikace.</span><span class="sxs-lookup"><span data-stu-id="37c26-133">This makes it possible to decide what information should be displayed on the main task page when warehouse workers perform tasks using the app.</span></span> <span data-ttu-id="37c26-134">Pokud klikněte na možnost **Vytvořit výchozí nastavení**, vygeneruje se výchozí sada skupin priority.</span><span class="sxs-lookup"><span data-stu-id="37c26-134">If you click **Create default setup**, a default set of priority groups will be generated.</span></span> <span data-ttu-id="37c26-135">Je možné vytvořit libovolný počet skupin priority podle potřeby, ale pouze tři skupiny priorit se zobrazí na stránce úloh.</span><span class="sxs-lookup"><span data-stu-id="37c26-135">It is possible to create as many priority groups as needed, but only three priority groups will be shown on the task page.</span></span> <span data-ttu-id="37c26-136">Když systém odesílá metadata do aplikace, přiřadí každému poli relativní prioritu v závislosti na skupině priority, a aplikace zobrazí první tři skupiny priority obsažené v metadatech na stránce úloh.</span><span class="sxs-lookup"><span data-stu-id="37c26-136">When the system sends metadata to the app, it will assign each field a relative priority depending on its priority group, and the app will display the first three priority groups contained in the metadata on the task page.</span></span> <span data-ttu-id="37c26-137">Zbývající metadata se zobrazí na sekundární stránce podrobností.</span><span class="sxs-lookup"><span data-stu-id="37c26-137">The rest of the overflowing metadata will be displayed on a secondary details page.</span></span> <span data-ttu-id="37c26-138">V následující tabulce je uveden příklad pěti skupin priority.</span><span class="sxs-lookup"><span data-stu-id="37c26-138">The following table shows an example of five priority groups.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="37c26-139">Skupina priority</span><span class="sxs-lookup"><span data-stu-id="37c26-139">Priority group</span></span></th>
<th><span data-ttu-id="37c26-140">Přiřazená pole</span><span class="sxs-lookup"><span data-stu-id="37c26-140">Assigned fields</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td> <span data-ttu-id="37c26-141">Priorita 10</span><span class="sxs-lookup"><span data-stu-id="37c26-141">Priority 10</span></span></td>
<td><ul>
<li><span data-ttu-id="37c26-142">Zboží</span><span class="sxs-lookup"><span data-stu-id="37c26-142">Item</span></span></li>
<li><span data-ttu-id="37c26-143">Množství</span><span class="sxs-lookup"><span data-stu-id="37c26-143">Quantity</span></span></li>
<li><span data-ttu-id="37c26-144">Měrná jednotka</span><span class="sxs-lookup"><span data-stu-id="37c26-144">Unit of measure</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td> <span data-ttu-id="37c26-145">Priorita 20</span><span class="sxs-lookup"><span data-stu-id="37c26-145">Priority 20</span></span></td>
<td><ul>
<li><span data-ttu-id="37c26-146">Pozice seskupení</span><span class="sxs-lookup"><span data-stu-id="37c26-146">Cluster position</span></span></li>
<li><span data-ttu-id="37c26-147">Seskupení</span><span class="sxs-lookup"><span data-stu-id="37c26-147">Cluster</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td> <span data-ttu-id="37c26-148">Priorita 30</span><span class="sxs-lookup"><span data-stu-id="37c26-148">Priority 30</span></span></td>
<td><ul>
<li><span data-ttu-id="37c26-149">Popis položky</span><span class="sxs-lookup"><span data-stu-id="37c26-149">Item description</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td> <span data-ttu-id="37c26-150">Priorita 40</span><span class="sxs-lookup"><span data-stu-id="37c26-150">Priority 40</span></span></td>
<td><ul>
<li><span data-ttu-id="37c26-151">Konfigurace</span><span class="sxs-lookup"><span data-stu-id="37c26-151">Configuration</span></span></li>
<li><span data-ttu-id="37c26-152">Barva</span><span class="sxs-lookup"><span data-stu-id="37c26-152">Color</span></span></li>
<li><span data-ttu-id="37c26-153">Velikost</span><span class="sxs-lookup"><span data-stu-id="37c26-153">Size</span></span></li>
<li><span data-ttu-id="37c26-154">Styl</span><span class="sxs-lookup"><span data-stu-id="37c26-154">Style</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td> <span data-ttu-id="37c26-155">Priorita 50</span><span class="sxs-lookup"><span data-stu-id="37c26-155">Priority 50</span></span></td>
<td><ul>
<li><span data-ttu-id="37c26-156">Skl. místo</span><span class="sxs-lookup"><span data-stu-id="37c26-156">Location</span></span></li>
<li><span data-ttu-id="37c26-157">Poznávací značka</span><span class="sxs-lookup"><span data-stu-id="37c26-157">License plate</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

<span data-ttu-id="37c26-158">Například pokud pracovník skladu provádí úlohu na mobilním zařízení, skutečnost, zda se metadata zobrazí v aplikaci, se skládá z následujících polí:</span><span class="sxs-lookup"><span data-stu-id="37c26-158">For example, when a warehouse worker is performing a task on a mobile device, if the metadata that will be displayed in the app consists of the following fields:</span></span>

-   <span data-ttu-id="37c26-159">Zboží</span><span class="sxs-lookup"><span data-stu-id="37c26-159">Item</span></span>
-   <span data-ttu-id="37c26-160">Množství</span><span class="sxs-lookup"><span data-stu-id="37c26-160">Quantity</span></span>
-   <span data-ttu-id="37c26-161">Měrná jednotka</span><span class="sxs-lookup"><span data-stu-id="37c26-161">Unit of measure</span></span>
-   <span data-ttu-id="37c26-162">Popis položky</span><span class="sxs-lookup"><span data-stu-id="37c26-162">Item description</span></span>
-   <span data-ttu-id="37c26-163">Velikost a umístění</span><span class="sxs-lookup"><span data-stu-id="37c26-163">Size and Location</span></span>

<span data-ttu-id="37c26-164">Na základě nastavení priority pole aplikace skladu ve výše uvedené tabulce se zobrazí na stránce úloh následující 3 řádky informací:</span><span class="sxs-lookup"><span data-stu-id="37c26-164">Based on the warehouse app field priority set up in the table above, the following 3 rows of information will be displayed on the task page:</span></span>

-   <span data-ttu-id="37c26-165">Řádek 1: Položka, množství a měrná jednotka</span><span class="sxs-lookup"><span data-stu-id="37c26-165">Row 1: Item, Quantity, Unit of measure</span></span>
-   <span data-ttu-id="37c26-166">Řádek 2: Popis položky</span><span class="sxs-lookup"><span data-stu-id="37c26-166">Row 2: Item description</span></span>
-   <span data-ttu-id="37c26-167">Řádek 3: Velikost</span><span class="sxs-lookup"><span data-stu-id="37c26-167">Row 3: Size</span></span>

<span data-ttu-id="37c26-168">Zbývající metadata, například umístění, se nezobrazí na stránce úloh, ale budou zobrazena na stránce podrobností.</span><span class="sxs-lookup"><span data-stu-id="37c26-168">The remaining metadata, for example, Location, will not be displayed on the task page, but will be displayed on a details page.</span></span> <span data-ttu-id="37c26-169">Další informace a příklady uživatelského rozhraní naleznete v příspěvku blogu [Oznámení aplikace Finance and Operations - Warehousing](https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/).</span><span class="sxs-lookup"><span data-stu-id="37c26-169">To learn more and see examples of the user interface, refer to the blog post [Announcing Finance and Operations - Warehousing](https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/).</span></span>

<a name="additional-resources"></a><span data-ttu-id="37c26-170">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="37c26-170">Additional resources</span></span>
--------

[<span data-ttu-id="37c26-171">Instalace a připojení mobilní aplikace Řízení skladu</span><span class="sxs-lookup"><span data-stu-id="37c26-171">Install and connect the Warehouse Management mobile app</span></span>](../warehousing/install-configure-warehouse-management-app.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]