---
title: Konfigurace názvů polí aplikace v aplikaci Warehousing
description: Toto téma popisuje, jak definovat a konfigurovat názvy polí aplikace skladu a priority v aplikaci Dynamics 365 Supply Chain Management.
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSMobileAppField, WHSMobileAppFieldPriority
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 269434
ms.assetid: 6cf3d7da-29bb-4d3d-aaf5-544ca9cc2980
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 11f6c96cc07c63d2c0c6a94385916b3396a77ed5
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/18/2019
ms.locfileid: "2814966"
---
# <a name="configure-app-field-names-in-warehousing-app"></a><span data-ttu-id="34bb8-103">Konfigurace názvů polí aplikace v aplikaci Warehousing</span><span class="sxs-lookup"><span data-stu-id="34bb8-103">Configure app field names in Warehousing app</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="34bb8-104">Toto téma popisuje, jak definovat a konfigurovat názvy polí aplikace skladu a priority v aplikaci Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="34bb8-104">This topic describes how to define and configure warehouse app field names and priorities in Dynamics 365 Supply Chain Management.</span></span> 

> [!NOTE]
> <span data-ttu-id="34bb8-105">Toto téma se vztahuje k funkcím v modulu Řízení skladu.</span><span class="sxs-lookup"><span data-stu-id="34bb8-105">This topic applies to features in Warehouse management.</span></span> <span data-ttu-id="34bb8-106">Nevztahuje se na funkce v modulu Řízení zásob.</span><span class="sxs-lookup"><span data-stu-id="34bb8-106">It doesn’t apply to features in Inventory management.</span></span> <span data-ttu-id="34bb8-107">Warehousing je aplikace, která slouží k provádění úloh skladu.</span><span class="sxs-lookup"><span data-stu-id="34bb8-107">Warehousing is an application that you can use to perform warehouse tasks.</span></span> <span data-ttu-id="34bb8-108">Je možné definovat a konfigurovat názvy polí použitých v aplikaci, jakož i konfigurovat priority, do kterých by měly být přiřazeny názvy polí.</span><span class="sxs-lookup"><span data-stu-id="34bb8-108">You can define and configure the field names that are used in the app, as well as configure the priority to which the field names should be assigned.</span></span> <span data-ttu-id="34bb8-109">Toto téma vysvětluje, jak definovat a konfigurovat tyto názvy polí aplikace skladu a priority, a zároveň způsob jejich použití v aplikaci Warehousing.</span><span class="sxs-lookup"><span data-stu-id="34bb8-109">This topic explains how to define and configure these warehouse app field names and priorities, and how they are used in Warehousing.</span></span> <span data-ttu-id="34bb8-110">Podrobné informace o konfiguraci připojení k aplikaci Warehousing naleznete v kurzu [Přehled instalace a konfigurace aplikace Warehousing](install-configure-warehousing-app.md).</span><span class="sxs-lookup"><span data-stu-id="34bb8-110">For detailed information about how to configure the connection to FWarehousing, refer to the tutorial [Install and configure the Warehousing app overview](install-configure-warehousing-app.md).</span></span>

## <a name="configure-warehouse-app-field-names"></a><span data-ttu-id="34bb8-111">Konfigurace názvů polí aplikace skladu</span><span class="sxs-lookup"><span data-stu-id="34bb8-111">Configure warehouse app field names</span></span>

<span data-ttu-id="34bb8-112">Použijete-li aplikaci Warehousing na svém mobilním zařízení, můžete nakonfigurovat, jakým způsobem se zobrazí metadata na vašem zařízení na stránce **Názvy polí aplikace skladu**.</span><span class="sxs-lookup"><span data-stu-id="34bb8-112">When you use Warehousing on your mobile device, you can configure how metadata should be displayed on your device on the **Warehouse app field names** page.</span></span> <span data-ttu-id="34bb8-113">V nové společnosti vyberte možnost **Vytvořit výchozí nastavení** pro vygenerování názvů všech polí, které budou použity ve workflow skladu na mobilním zařízení, přiřaďte jim upřednostňovaný vstupní režim a typ vstupu.</span><span class="sxs-lookup"><span data-stu-id="34bb8-113">In a new company, select **Create default setup** to generate all field names that will be used in the warehouse mobile device workflows, and then assign a preferred input mode and input type to them.</span></span> <span data-ttu-id="34bb8-114">Po vygenerování všech názvů polí můžete vybrat následující možnosti vstupu.</span><span class="sxs-lookup"><span data-stu-id="34bb8-114">After you have generated all field names, you can select the following input options.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="34bb8-115">Parametr</span><span class="sxs-lookup"><span data-stu-id="34bb8-115">Option</span></span></th>
<th><span data-ttu-id="34bb8-116">popis</span><span class="sxs-lookup"><span data-stu-id="34bb8-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="34bb8-117">Upřednostňovaný režim vstupu</span><span class="sxs-lookup"><span data-stu-id="34bb8-117">Preferred input mode</span></span></td>
<td><span data-ttu-id="34bb8-118">Tato možnost určuje, zda se mají pro zvolený název pole zobrazovat prohledávací pole nebo vstupní pole ručního zadávání.</span><span class="sxs-lookup"><span data-stu-id="34bb8-118">This option defines whether a scanning field or a manual entry input field should be shown for the selected field name.</span></span> <span data-ttu-id="34bb8-119">To je užitečné k rozlišení polí v závislosti na tom, zda se používají pro pole čárové kódy.</span><span class="sxs-lookup"><span data-stu-id="34bb8-119">This is useful to distinguish fields depending on if barcodes are used for the field.</span></span> <span data-ttu-id="34bb8-120"><strong>Poznámka:</strong> Pro názvy polí s upřednostňovaným vstupním režimem nastaveným na <strong>Vyhledávání</strong> můžete zadat informace ručně, pokud není čárový kód čitelný nebo je poškozen.</span><span class="sxs-lookup"><span data-stu-id="34bb8-120"><strong>Note:</strong> For field names with preferred input mode set to <strong>Scanning</strong>, you can enter information manually if the barcode is unreadable or damaged.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34bb8-121">Vstupní typ</span><span class="sxs-lookup"><span data-stu-id="34bb8-121">Input type</span></span></td>
<td><span data-ttu-id="34bb8-122">Tato možnost určuje, jaký typ vstupu má být použit pro název vybraného pole.</span><span class="sxs-lookup"><span data-stu-id="34bb8-122">This option defines what input type should be used for the selected field name.</span></span> <span data-ttu-id="34bb8-123">K dispozici jsou čtyři možnosti:</span><span class="sxs-lookup"><span data-stu-id="34bb8-123">Four options are available:</span></span>
<ul>
<li><span data-ttu-id="34bb8-124"><strong>Výběr </strong> - Obsahuje seznam možností k výběru.</span><span class="sxs-lookup"><span data-stu-id="34bb8-124"><strong>Selection</strong> - Contains a list of options to choose from.</span></span> <span data-ttu-id="34bb8-125">Názvy polí s touto možností nejsou upravitelné.</span><span class="sxs-lookup"><span data-stu-id="34bb8-125">Field names with this option are not editable.</span></span></li>
<li><span data-ttu-id="34bb8-126"><strong>Datum</strong> - Názvy polí specifikované jako datum zobrazí formát data s popiskem.</span><span class="sxs-lookup"><span data-stu-id="34bb8-126"><strong>Date</strong> - Field names specified as date will show a date format with the label.</span></span> <span data-ttu-id="34bb8-127">To pomáhá pracovníkům skladu zjistit, v jakém formátu zadat datum.</span><span class="sxs-lookup"><span data-stu-id="34bb8-127">This helps warehouse workers see in which format to enter the date.</span></span> <span data-ttu-id="34bb8-128">Názvy polí s touto možností nejsou upravitelné.</span><span class="sxs-lookup"><span data-stu-id="34bb8-128">Field names with this option are not editable.</span></span></li>
<li><span data-ttu-id="34bb8-129"><strong>Alfa</strong> - Je-li tato možnost vybrána, použije se při ručním zadávání informací do aplikace klávesnice zařízení.</span><span class="sxs-lookup"><span data-stu-id="34bb8-129"><strong>Alpha</strong> - If selected, the device keyboard will be used when entering information manually in the app.</span></span> <span data-ttu-id="34bb8-130">Vlastnosti klávesnice lze změnit podle toho, na kterém zařízení se používá.</span><span class="sxs-lookup"><span data-stu-id="34bb8-130">The keyboard experience can be changed depending on which device is used.</span></span></li>
<li><span data-ttu-id="34bb8-131"><strong>Číselný</strong> - Pro názvy polí používající pouze číselné vstupy můžete vybrat tuto možnost, chcete-li zobrazit vlastní numerickou klávesnici s vstupní polem místo klávesnice zařízení.</span><span class="sxs-lookup"><span data-stu-id="34bb8-131"><strong>Numeric</strong> - For field names that use numeric input only, you can select this option to display a custom numeric keypad with the input field instead of the device keyboard.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="configure-warehouse-app-field-priority"></a><span data-ttu-id="34bb8-132">Konfigurace priority pole aplikace skladu</span><span class="sxs-lookup"><span data-stu-id="34bb8-132">Configure warehouse app field priority</span></span>

<span data-ttu-id="34bb8-133">Na stránce **Priorita pole aplikace skladu** můžete umístit názvy polí do různých skupin priority.</span><span class="sxs-lookup"><span data-stu-id="34bb8-133">On the **Warehouse app field priority** page, you can put field names into different priority groups.</span></span> <span data-ttu-id="34bb8-134">Díky tomu je možné se rozhodnout, jaké informace mají být zobrazeny na hlavní stránce úloh, když pracovníci skladu provádět úlohy pomocí této aplikace.</span><span class="sxs-lookup"><span data-stu-id="34bb8-134">This makes it possible to decide what information should be displayed on the main task page when warehouse workers perform tasks using the app.</span></span> <span data-ttu-id="34bb8-135">Pokud klikněte na možnost **Vytvořit výchozí nastavení**, vygeneruje se výchozí sada skupin priority.</span><span class="sxs-lookup"><span data-stu-id="34bb8-135">If you click **Create default setup**, a default set of priority groups will be generated.</span></span> <span data-ttu-id="34bb8-136">Je možné vytvořit libovolný počet skupin priority podle potřeby, ale pouze tři skupiny priorit se zobrazí na stránce úloh.</span><span class="sxs-lookup"><span data-stu-id="34bb8-136">It is possible to create as many priority groups as needed, but only three priority groups will be shown on the task page.</span></span> <span data-ttu-id="34bb8-137">Když systém odesílá metadata do aplikace, přiřadí každému poli relativní prioritu v závislosti na skupině priority, a aplikace zobrazí první tři skupiny priority obsažené v metadatech na stránce úloh.</span><span class="sxs-lookup"><span data-stu-id="34bb8-137">When the system sends metadata to the app, it will assign each field a relative priority depending on its priority group, and the app will display the first three priority groups contained in the metadata on the task page.</span></span> <span data-ttu-id="34bb8-138">Zbývající metadata se zobrazí na sekundární stránce podrobností.</span><span class="sxs-lookup"><span data-stu-id="34bb8-138">The rest of the overflowing metadata will be displayed on a secondary details page.</span></span> <span data-ttu-id="34bb8-139">V následující tabulce je uveden příklad pěti skupin priority.</span><span class="sxs-lookup"><span data-stu-id="34bb8-139">The following table shows an example of five priority groups.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="34bb8-140">Skupina priority</span><span class="sxs-lookup"><span data-stu-id="34bb8-140">Priority group</span></span></th>
<th><span data-ttu-id="34bb8-141">Přiřazená pole</span><span class="sxs-lookup"><span data-stu-id="34bb8-141">Assigned fields</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td> <span data-ttu-id="34bb8-142">Priorita 10</span><span class="sxs-lookup"><span data-stu-id="34bb8-142">Priority 10</span></span></td>
<td><ul>
<li><span data-ttu-id="34bb8-143">Zboží</span><span class="sxs-lookup"><span data-stu-id="34bb8-143">Item</span></span></li>
<li><span data-ttu-id="34bb8-144">Množství</span><span class="sxs-lookup"><span data-stu-id="34bb8-144">Quantity</span></span></li>
<li><span data-ttu-id="34bb8-145">Měrná jednotka</span><span class="sxs-lookup"><span data-stu-id="34bb8-145">Unit of measure</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td> <span data-ttu-id="34bb8-146">Priorita 20</span><span class="sxs-lookup"><span data-stu-id="34bb8-146">Priority 20</span></span></td>
<td><ul>
<li><span data-ttu-id="34bb8-147">Pozice seskupení</span><span class="sxs-lookup"><span data-stu-id="34bb8-147">Cluster position</span></span></li>
<li><span data-ttu-id="34bb8-148">Seskupení</span><span class="sxs-lookup"><span data-stu-id="34bb8-148">Cluster</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td> <span data-ttu-id="34bb8-149">Priorita 30</span><span class="sxs-lookup"><span data-stu-id="34bb8-149">Priority 30</span></span></td>
<td><ul>
<li><span data-ttu-id="34bb8-150">Popis položky</span><span class="sxs-lookup"><span data-stu-id="34bb8-150">Item description</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td> <span data-ttu-id="34bb8-151">Priorita 40</span><span class="sxs-lookup"><span data-stu-id="34bb8-151">Priority 40</span></span></td>
<td><ul>
<li><span data-ttu-id="34bb8-152">Konfigurace</span><span class="sxs-lookup"><span data-stu-id="34bb8-152">Configuration</span></span></li>
<li><span data-ttu-id="34bb8-153">Barva</span><span class="sxs-lookup"><span data-stu-id="34bb8-153">Color</span></span></li>
<li><span data-ttu-id="34bb8-154">Velikost</span><span class="sxs-lookup"><span data-stu-id="34bb8-154">Size</span></span></li>
<li><span data-ttu-id="34bb8-155">Styl</span><span class="sxs-lookup"><span data-stu-id="34bb8-155">Style</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td> <span data-ttu-id="34bb8-156">Priorita 50</span><span class="sxs-lookup"><span data-stu-id="34bb8-156">Priority 50</span></span></td>
<td><ul>
<li><span data-ttu-id="34bb8-157">Skl. místo</span><span class="sxs-lookup"><span data-stu-id="34bb8-157">Location</span></span></li>
<li><span data-ttu-id="34bb8-158">Poznávací značka</span><span class="sxs-lookup"><span data-stu-id="34bb8-158">License plate</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

<span data-ttu-id="34bb8-159">Například pokud pracovník skladu provádí úlohu na mobilním zařízení, skutečnost, zda se metadata zobrazí v aplikaci, se skládá z následujících polí:</span><span class="sxs-lookup"><span data-stu-id="34bb8-159">For example, when a warehouse worker is performing a task on a mobile device, if the metadata that will be displayed in the app consists of the following fields:</span></span>

-   <span data-ttu-id="34bb8-160">Zboží</span><span class="sxs-lookup"><span data-stu-id="34bb8-160">Item</span></span>
-   <span data-ttu-id="34bb8-161">Množství</span><span class="sxs-lookup"><span data-stu-id="34bb8-161">Quantity</span></span>
-   <span data-ttu-id="34bb8-162">Měrná jednotka</span><span class="sxs-lookup"><span data-stu-id="34bb8-162">Unit of measure</span></span>
-   <span data-ttu-id="34bb8-163">Popis položky</span><span class="sxs-lookup"><span data-stu-id="34bb8-163">Item description</span></span>
-   <span data-ttu-id="34bb8-164">Velikost a umístění</span><span class="sxs-lookup"><span data-stu-id="34bb8-164">Size and Location</span></span>

<span data-ttu-id="34bb8-165">Na základě nastavení priority pole aplikace skladu ve výše uvedené tabulce se zobrazí na stránce úloh následující 3 řádky informací:</span><span class="sxs-lookup"><span data-stu-id="34bb8-165">Based on the warehouse app field priority set up in the table above, the following 3 rows of information will be displayed on the task page:</span></span>

-   <span data-ttu-id="34bb8-166">Řádek 1: Položka, množství a měrná jednotka</span><span class="sxs-lookup"><span data-stu-id="34bb8-166">Row 1: Item, Quantity, Unit of measure</span></span>
-   <span data-ttu-id="34bb8-167">Řádek 2: Popis položky</span><span class="sxs-lookup"><span data-stu-id="34bb8-167">Row 2: Item description</span></span>
-   <span data-ttu-id="34bb8-168">Řádek 3: Velikost</span><span class="sxs-lookup"><span data-stu-id="34bb8-168">Row 3: Size</span></span>

<span data-ttu-id="34bb8-169">Zbývající metadata, například umístění, se nezobrazí na stránce úloh, ale budou zobrazena na stránce podrobností.</span><span class="sxs-lookup"><span data-stu-id="34bb8-169">The remaining metadata, for example, Location, will not be displayed on the task page, but will be displayed on a details page.</span></span> <span data-ttu-id="34bb8-170">Další informace a příklady uživatelského rozhraní naleznete v příspěvku blogu [Oznámení aplikace Finance and Operations - Warehousing](https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/).</span><span class="sxs-lookup"><span data-stu-id="34bb8-170">To learn more and see examples of the user interface, refer to the blog post [Announcing Finance and Operations - Warehousing](https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/).</span></span>

<a name="additional-resources"></a><span data-ttu-id="34bb8-171">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="34bb8-171">Additional resources</span></span>
--------

[<span data-ttu-id="34bb8-172">Přehled instalace a konfigurace aplikace Warehousing</span><span class="sxs-lookup"><span data-stu-id="34bb8-172">Install and configure the Warehousing app overview</span></span>](install-configure-warehousing-app.md)
