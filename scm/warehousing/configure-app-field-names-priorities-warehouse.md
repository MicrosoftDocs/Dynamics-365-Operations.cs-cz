---
title: "Konfigurace názvů polí aplikace v aplikaci Warehousing"
description: "Toto téma popisuje, jak definovat a konfigurovat názvy polí aplikace skladu a priority v aplikaci Finance and Operations."
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSMobileAppField, WHSMobileAppFieldPriority
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 269434
ms.assetid: 6cf3d7da-29bb-4d3d-aaf5-544ca9cc2980
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 55c77c5c41b83c6b9d3e04e1e0c6382f23831502
ms.contentlocale: cs-cz
ms.lasthandoff: 08/29/2017

---

# <a name="configure-app-field-names-in-warehousing-app"></a><span data-ttu-id="bf11f-103">Konfigurace názvů polí aplikace v aplikaci Warehousing</span><span class="sxs-lookup"><span data-stu-id="bf11f-103">Configure app field names in Warehousing app</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="bf11f-104">Toto téma popisuje, jak definovat a konfigurovat názvy polí aplikace skladu a priority v aplikaci Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="bf11f-104">This topic describes how to define and configure warehouse app field names and priorities in Finance and Operations.</span></span> 

<span data-ttu-id="bf11f-105">**Poznámka:** Toto téma se vztahuje k funkcím v modulu Řízení skladu.</span><span class="sxs-lookup"><span data-stu-id="bf11f-105">**Note:** This topic applies to features in Warehouse management.</span></span> <span data-ttu-id="bf11f-106">Nevztahuje se na funkce v modulu Řízení zásob.</span><span class="sxs-lookup"><span data-stu-id="bf11f-106">It doesn’t apply to features in Inventory management.</span></span> <span data-ttu-id="bf11f-107">Finance and Operations - Warehousing je aplikace, která slouží k provádění úloh skladu.</span><span class="sxs-lookup"><span data-stu-id="bf11f-107">Finance and Operations - Warehousing is an application that you can use to perform warehouse tasks.</span></span> <span data-ttu-id="bf11f-108">Je možné definovat a konfigurovat názvy polí použitých v aplikaci, jakož i konfigurovat priority, do kterých by měly být přiřazeny názvy polí.</span><span class="sxs-lookup"><span data-stu-id="bf11f-108">You can define and configure the field names that are used in the app, as well as configure the priority to which the field names should be assigned.</span></span> <span data-ttu-id="bf11f-109">Toto téma vysvětluje, jak definovat a konfigurovat tyto názvy polí aplikace skladu a priority, a zároveň způsob jejich použití v aplikaci Finance and Operations - Warehousing.</span><span class="sxs-lookup"><span data-stu-id="bf11f-109">This topic explains how to define and configure these warehouse app field names and priorities, and how they are used in Finance and Operations - Warehousing.</span></span> <span data-ttu-id="bf11f-110">Podrobné informace o konfiguraci připojení k aplikac Finance and Operations - Warehousing naleznete v kurzu [Instalace a konfigurace aplikace Finance and Operations - Warehousing](install-configure-warehousing-app.md).</span><span class="sxs-lookup"><span data-stu-id="bf11f-110">For detailed information about how to configure the connection to Finance and Operations  - Warehousing, refer to the tutorial [Install and configure Finance and Operations - Warehousing](install-configure-warehousing-app.md).</span></span>

<a name="configure-warehouse-app-field-names"></a><span data-ttu-id="bf11f-111">Konfigurace názvů polí aplikace skladu</span><span class="sxs-lookup"><span data-stu-id="bf11f-111">Configure warehouse app field names</span></span>
===================================

<span data-ttu-id="bf11f-112">Použijete-li aplikaci Finance and Operations - Warehousing na svém mobilním zařízení, můžete nakonfigurovat, jakým způsobem se zobrazí metadata na vašem zařízení na stránce **Názvy polí aplikace skladu**.</span><span class="sxs-lookup"><span data-stu-id="bf11f-112">When you use Finance and Operations - Warehousing on your mobile device, you can configure how metadata should be displayed on your device on the **Warehouse app field names** page.</span></span> <span data-ttu-id="bf11f-113">V nové společnosti v aplikaci Finance and Operations vyberte možnost **Vytvořit výchozí nastavení** pro vygenerování názvů všech polí, které budou použity ve workflow skladu na mobilním zařízení, přiřaďte jim upřednostňovaný vstupní režim a typ vstupu.</span><span class="sxs-lookup"><span data-stu-id="bf11f-113">In a new company in Finance and Operations, select **Create default setup** to generate all field names that will be used in the warehouse mobile device workflows, and then assign a preferred input mode and input type to them.</span></span> <span data-ttu-id="bf11f-114">Po vygenerování všech názvů polí můžete vybrat následující možnosti vstupu.</span><span class="sxs-lookup"><span data-stu-id="bf11f-114">After you have generated all field names, you can select the following input options.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bf11f-115">Parametr</span><span class="sxs-lookup"><span data-stu-id="bf11f-115">Option</span></span></th>
<th><span data-ttu-id="bf11f-116">popis</span><span class="sxs-lookup"><span data-stu-id="bf11f-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bf11f-117">Upřednostňovaný režim vstupu</span><span class="sxs-lookup"><span data-stu-id="bf11f-117">Preferred input mode</span></span></td>
<td><span data-ttu-id="bf11f-118">Tato možnost určuje, zda se mají pro zvolený název pole zobrazovat prohledávací pole nebo vstupní pole ručního zadávání.</span><span class="sxs-lookup"><span data-stu-id="bf11f-118">This option defines whether a scanning field or a manual entry input field should be shown for the selected field name.</span></span> <span data-ttu-id="bf11f-119">To je užitečné k rozlišení polí v závislosti na tom, zda se používají pro pole čárové kódy.</span><span class="sxs-lookup"><span data-stu-id="bf11f-119">This is useful to distinguish fields depending on if barcodes are used for the field.</span></span> <span data-ttu-id="bf11f-120"><strong>Poznámka:</strong> Pro názvy polí s upřednostňovaným vstupním režimem nastaveným na <strong>Vyhledávání</strong> můžete zadat informace ručně, pokud není čárový kód čitelný nebo je poškozen.</span><span class="sxs-lookup"><span data-stu-id="bf11f-120"><strong>Note:</strong> For field names with preferred input mode set to <strong>Scanning</strong>, you can enter information manually if the barcode is unreadable or damaged.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bf11f-121">Vstupní typ</span><span class="sxs-lookup"><span data-stu-id="bf11f-121">Input type</span></span></td>
<td><span data-ttu-id="bf11f-122">Tato možnost určuje, jaký typ vstupu má být použit pro název vybraného pole.</span><span class="sxs-lookup"><span data-stu-id="bf11f-122">This option defines what input type should be used for the selected field name.</span></span> <span data-ttu-id="bf11f-123">K dispozici jsou čtyři možnosti:</span><span class="sxs-lookup"><span data-stu-id="bf11f-123">Four options are available:</span></span>
<ul>
<li><span data-ttu-id="bf11f-124"><strong>Výběr</strong> - obsahuje seznam možností k výběru.</span><span class="sxs-lookup"><span data-stu-id="bf11f-124"><strong>Selection</strong> - Contains a list of options to choose from.</span></span> <span data-ttu-id="bf11f-125">Názvy polí s touto možností nejsou upravitelné.</span><span class="sxs-lookup"><span data-stu-id="bf11f-125">Field names with this option are not editable.</span></span></li>
<li><span data-ttu-id="bf11f-126"><strong>Datum</strong> - názvy polí specifikované jako datum zobrazí formát data s popiskem.</span><span class="sxs-lookup"><span data-stu-id="bf11f-126"><strong>Date</strong> - Field names specified as date will show a date format with the label.</span></span> <span data-ttu-id="bf11f-127">To pomáhá pracovníkům skladu zjistit, v jakém formátu zadat datum.</span><span class="sxs-lookup"><span data-stu-id="bf11f-127">This helps warehouse workers see in which format to enter the date.</span></span> <span data-ttu-id="bf11f-128">Názvy polí s touto možností nejsou upravitelné.</span><span class="sxs-lookup"><span data-stu-id="bf11f-128">Field names with this option are not editable.</span></span></li>
<li><span data-ttu-id="bf11f-129"><strong>Alfa</strong> - -je-li tato možnost vybrána, použije se při ručním zadávání informací do aplikace klávesnice zařízení.</span><span class="sxs-lookup"><span data-stu-id="bf11f-129"><strong>Alpha</strong> - If selected, the device keyboard will be used when entering information manually in the app.</span></span> <span data-ttu-id="bf11f-130">Vlastnosti klávesnice lze změnit podle toho, na kterém zařízení se používá.</span><span class="sxs-lookup"><span data-stu-id="bf11f-130">The keyboard experience can be changed depending on which device is used.</span></span></li>
<li><span data-ttu-id="bf11f-131"><strong>Číselný</strong> - pro názvy polí používající pouze číselné vstupy můžete vybrat tuto možnost, chcete-li zobrazit vlastní numerickou klávesnici s vstupní polem místo klávesnice zařízení.</span><span class="sxs-lookup"><span data-stu-id="bf11f-131"><strong>Numeric</strong> - For field names that use numeric input only, you can select this option to display a custom numeric keypad with the input field instead of the device keyboard.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

<a name="configure-warehouse-app-field-priority"></a><span data-ttu-id="bf11f-132">Konfigurace priority pole aplikace skladu</span><span class="sxs-lookup"><span data-stu-id="bf11f-132">Configure warehouse app field priority</span></span>
======================================

<span data-ttu-id="bf11f-133">Na stránce **Priorita pole aplikace skladu** můžete umístit názvy polí do různých skupin priority.</span><span class="sxs-lookup"><span data-stu-id="bf11f-133">On the **Warehouse app field priority** page, you can put field names into different priority groups.</span></span> <span data-ttu-id="bf11f-134">Díky tomu je možné se rozhodnout, jaké informace mají být zobrazeny na hlavní stránce úloh, když pracovníci skladu provádět úlohy pomocí této aplikace.</span><span class="sxs-lookup"><span data-stu-id="bf11f-134">This makes it possible to decide what information should be displayed on the main task page when warehouse workers perform tasks using the app.</span></span> <span data-ttu-id="bf11f-135">Pokud klikněte na možnost **Vytvořit výchozí nastavení**, vygeneruje se výchozí sada skupin priority.</span><span class="sxs-lookup"><span data-stu-id="bf11f-135">If you click **Create default setup**, a default set of priority groups will be generated.</span></span> <span data-ttu-id="bf11f-136">Je možné vytvořit libovolný počet skupin priority podle potřeby, ale pouze tři skupiny priorit se zobrazí na stránce úloh.</span><span class="sxs-lookup"><span data-stu-id="bf11f-136">It is possible to create as many priority groups as needed, but only three priority groups will be shown on the task page.</span></span> <span data-ttu-id="bf11f-137">Když odesílá aplikace Finance and Operations metadata do aplikace, přiřadí každému poli relativní prioritu v závislosti na skupině priority, a aplikace zobrazí první tři skupiny priority obsažené v metadatech na stránce úloh.</span><span class="sxs-lookup"><span data-stu-id="bf11f-137">When Finance and Operations sends metadata to the app, it will assign each field a relative priority depending on its priority group, and the app will display the first three priority groups contained in the metadata on the task page.</span></span> <span data-ttu-id="bf11f-138">Zbývající metadata se zobrazí na sekundární stránce podrobností.</span><span class="sxs-lookup"><span data-stu-id="bf11f-138">The rest of the overflowing metadata will be displayed on a secondary details page.</span></span> <span data-ttu-id="bf11f-139">V následující tabulce je uveden příklad pěti skupin priority.</span><span class="sxs-lookup"><span data-stu-id="bf11f-139">The following table shows an example of five priority groups.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bf11f-140">Skupina priority</span><span class="sxs-lookup"><span data-stu-id="bf11f-140">Priority group</span></span></th>
<th><span data-ttu-id="bf11f-141">Přiřazená pole</span><span class="sxs-lookup"><span data-stu-id="bf11f-141">Assigned fields</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td> <span data-ttu-id="bf11f-142">Priorita 10</span><span class="sxs-lookup"><span data-stu-id="bf11f-142">Priority 10</span></span></td>
<td><ul>
<li><span data-ttu-id="bf11f-143">Zboží</span><span class="sxs-lookup"><span data-stu-id="bf11f-143">Item</span></span></li>
<li><span data-ttu-id="bf11f-144">Množství</span><span class="sxs-lookup"><span data-stu-id="bf11f-144">Quantity</span></span></li>
<li><span data-ttu-id="bf11f-145">Měrná jednotka</span><span class="sxs-lookup"><span data-stu-id="bf11f-145">Unit of measure</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td> <span data-ttu-id="bf11f-146">Priorita 20</span><span class="sxs-lookup"><span data-stu-id="bf11f-146">Priority 20</span></span></td>
<td><ul>
<li><span data-ttu-id="bf11f-147">Pozice seskupení</span><span class="sxs-lookup"><span data-stu-id="bf11f-147">Cluster position</span></span></li>
<li><span data-ttu-id="bf11f-148">Seskupení</span><span class="sxs-lookup"><span data-stu-id="bf11f-148">Cluster</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td> <span data-ttu-id="bf11f-149">Priorita 30</span><span class="sxs-lookup"><span data-stu-id="bf11f-149">Priority 30</span></span></td>
<td><ul>
<li><span data-ttu-id="bf11f-150">Popis položky</span><span class="sxs-lookup"><span data-stu-id="bf11f-150">Item description</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td> <span data-ttu-id="bf11f-151">Priorita 40</span><span class="sxs-lookup"><span data-stu-id="bf11f-151">Priority 40</span></span></td>
<td><ul>
<li><span data-ttu-id="bf11f-152">Konfigurace</span><span class="sxs-lookup"><span data-stu-id="bf11f-152">Configuration</span></span></li>
<li><span data-ttu-id="bf11f-153">Barva</span><span class="sxs-lookup"><span data-stu-id="bf11f-153">Color</span></span></li>
<li><span data-ttu-id="bf11f-154">Velikost</span><span class="sxs-lookup"><span data-stu-id="bf11f-154">Size</span></span></li>
<li><span data-ttu-id="bf11f-155">Styl</span><span class="sxs-lookup"><span data-stu-id="bf11f-155">Style</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td> <span data-ttu-id="bf11f-156">Priorita 50</span><span class="sxs-lookup"><span data-stu-id="bf11f-156">Priority 50</span></span></td>
<td><ul>
<li><span data-ttu-id="bf11f-157">Skl. místo</span><span class="sxs-lookup"><span data-stu-id="bf11f-157">Location</span></span></li>
<li><span data-ttu-id="bf11f-158">Poznávací značka</span><span class="sxs-lookup"><span data-stu-id="bf11f-158">License plate</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

<span data-ttu-id="bf11f-159">Například pokud pracovník skladu provádí úlohu na mobilním zařízení, skutečnost, zda se metadata zobrazí v aplikaci, se skládá z následujících polí:</span><span class="sxs-lookup"><span data-stu-id="bf11f-159">For example, when a warehouse worker is performing a task on a mobile device, if the metadata that will be displayed in the app consists of the following fields:</span></span>

-   <span data-ttu-id="bf11f-160">Zboží</span><span class="sxs-lookup"><span data-stu-id="bf11f-160">Item</span></span>
-   <span data-ttu-id="bf11f-161">Množství</span><span class="sxs-lookup"><span data-stu-id="bf11f-161">Quantity</span></span>
-   <span data-ttu-id="bf11f-162">Měrná jednotka</span><span class="sxs-lookup"><span data-stu-id="bf11f-162">Unit of measure</span></span>
-   <span data-ttu-id="bf11f-163">Popis položky</span><span class="sxs-lookup"><span data-stu-id="bf11f-163">Item description</span></span>
-   <span data-ttu-id="bf11f-164">Velikost a umístění</span><span class="sxs-lookup"><span data-stu-id="bf11f-164">Size and Location</span></span>

<span data-ttu-id="bf11f-165">Na základě nastavení priority pole aplikace skladu ve výše uvedené tabulce se zobrazí na stránce úloh následující 3 řádky informací:</span><span class="sxs-lookup"><span data-stu-id="bf11f-165">Based on the warehouse app field priority set up in the table above, the following 3 rows of information will be displayed on the task page:</span></span>

-   <span data-ttu-id="bf11f-166">Řádek 1: Položka, množství a měrná jednotka</span><span class="sxs-lookup"><span data-stu-id="bf11f-166">Row 1: Item, Quantity, Unit of measure</span></span>
-   <span data-ttu-id="bf11f-167">Řádek 2: Popis položky</span><span class="sxs-lookup"><span data-stu-id="bf11f-167">Row 2: Item description</span></span>
-   <span data-ttu-id="bf11f-168">Řádek 3: Velikost</span><span class="sxs-lookup"><span data-stu-id="bf11f-168">Row 3: Size</span></span>

<span data-ttu-id="bf11f-169">Zbývající metadata, například umístění, se nezobrazí na stránce úloh, ale budou zobrazena na stránce podrobností.</span><span class="sxs-lookup"><span data-stu-id="bf11f-169">The remaining metadata, for example, Location, will not be displayed on the task page, but will be displayed on a details page.</span></span> <span data-ttu-id="bf11f-170">Další informace a příklady uživatelského rozhraní naleznete v příspěvku blogu [Oznámení aplikace Finance and Operations - Warehousing](https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/).</span><span class="sxs-lookup"><span data-stu-id="bf11f-170">To learn more and see examples of the user interface, refer to the blog post [Announcing Finance and Operations - Warehousing](https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/).</span></span>

<a name="see-also"></a><span data-ttu-id="bf11f-171">Viz také</span><span class="sxs-lookup"><span data-stu-id="bf11f-171">See also</span></span>
--------

[<span data-ttu-id="bf11f-172">Instalace a konfigurace aplikace Microsoft Dynamics 365 for Finance and Operations – Warehousing</span><span class="sxs-lookup"><span data-stu-id="bf11f-172">Install and configure Microsoft Dynamics 365 for Finance and Operations – Warehousing</span></span>](install-configure-warehousing-app.md)




