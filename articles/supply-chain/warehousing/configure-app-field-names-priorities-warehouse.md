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
ms.openlocfilehash: a3251368e92eb2e24eb9e64bb615027d038ff660
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/30/2019
ms.locfileid: "2251078"
---
# <a name="configure-app-field-names-in-warehousing-app"></a><span data-ttu-id="651e5-103">Konfigurace názvů polí aplikace v aplikaci Warehousing</span><span class="sxs-lookup"><span data-stu-id="651e5-103">Configure app field names in Warehousing app</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="651e5-104">Toto téma popisuje, jak definovat a konfigurovat názvy polí aplikace skladu a priority v aplikaci Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="651e5-104">This topic describes how to define and configure warehouse app field names and priorities in Dynamics 365 Supply Chain Management.</span></span> 

<span data-ttu-id="651e5-105">**Poznámka:** Toto téma se vztahuje k funkcím v modulu Řízení skladu.</span><span class="sxs-lookup"><span data-stu-id="651e5-105">**Note:** This topic applies to features in Warehouse management.</span></span> <span data-ttu-id="651e5-106">Nevztahuje se na funkce v modulu Řízení zásob.</span><span class="sxs-lookup"><span data-stu-id="651e5-106">It doesn’t apply to features in Inventory management.</span></span> <span data-ttu-id="651e5-107">Warehousing je aplikace, která slouží k provádění úloh skladu.</span><span class="sxs-lookup"><span data-stu-id="651e5-107">Warehousing is an application that you can use to perform warehouse tasks.</span></span> <span data-ttu-id="651e5-108">Je možné definovat a konfigurovat názvy polí použitých v aplikaci, jakož i konfigurovat priority, do kterých by měly být přiřazeny názvy polí.</span><span class="sxs-lookup"><span data-stu-id="651e5-108">You can define and configure the field names that are used in the app, as well as configure the priority to which the field names should be assigned.</span></span> <span data-ttu-id="651e5-109">Toto téma vysvětluje, jak definovat a konfigurovat tyto názvy polí aplikace skladu a priority, a zároveň způsob jejich použití v aplikaci Warehousing.</span><span class="sxs-lookup"><span data-stu-id="651e5-109">This topic explains how to define and configure these warehouse app field names and priorities, and how they are used in Warehousing.</span></span> <span data-ttu-id="651e5-110">Podrobné informace o konfiguraci připojení k aplikaci Warehousing naleznete v kurzu [Instalace a konfigurace aplikace Finance and Operations - Warehousing](install-configure-warehousing-app.md).</span><span class="sxs-lookup"><span data-stu-id="651e5-110">For detailed information about how to configure the connection to FWarehousing, refer to the tutorial [Install and configure Warehousing](install-configure-warehousing-app.md).</span></span>

## <a name="configure-warehouse-app-field-names"></a><span data-ttu-id="651e5-111">Konfigurace názvů polí aplikace skladu</span><span class="sxs-lookup"><span data-stu-id="651e5-111">Configure warehouse app field names</span></span>

<span data-ttu-id="651e5-112">Použijete-li aplikaci Warehousing na svém mobilním zařízení, můžete nakonfigurovat, jakým způsobem se zobrazí metadata na vašem zařízení na stránce **Názvy polí aplikace skladu**.</span><span class="sxs-lookup"><span data-stu-id="651e5-112">When you use Warehousing on your mobile device, you can configure how metadata should be displayed on your device on the **Warehouse app field names** page.</span></span> <span data-ttu-id="651e5-113">V nové společnosti vyberte možnost **Vytvořit výchozí nastavení** pro vygenerování názvů všech polí, které budou použity ve workflow skladu na mobilním zařízení, přiřaďte jim upřednostňovaný vstupní režim a typ vstupu.</span><span class="sxs-lookup"><span data-stu-id="651e5-113">In a new company, select **Create default setup** to generate all field names that will be used in the warehouse mobile device workflows, and then assign a preferred input mode and input type to them.</span></span> <span data-ttu-id="651e5-114">Po vygenerování všech názvů polí můžete vybrat následující možnosti vstupu.</span><span class="sxs-lookup"><span data-stu-id="651e5-114">After you have generated all field names, you can select the following input options.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="651e5-115">Parametr</span><span class="sxs-lookup"><span data-stu-id="651e5-115">Option</span></span></th>
<th><span data-ttu-id="651e5-116">popis</span><span class="sxs-lookup"><span data-stu-id="651e5-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="651e5-117">Upřednostňovaný režim vstupu</span><span class="sxs-lookup"><span data-stu-id="651e5-117">Preferred input mode</span></span></td>
<td><span data-ttu-id="651e5-118">Tato možnost určuje, zda se mají pro zvolený název pole zobrazovat prohledávací pole nebo vstupní pole ručního zadávání.</span><span class="sxs-lookup"><span data-stu-id="651e5-118">This option defines whether a scanning field or a manual entry input field should be shown for the selected field name.</span></span> <span data-ttu-id="651e5-119">To je užitečné k rozlišení polí v závislosti na tom, zda se používají pro pole čárové kódy.</span><span class="sxs-lookup"><span data-stu-id="651e5-119">This is useful to distinguish fields depending on if barcodes are used for the field.</span></span> <span data-ttu-id="651e5-120"><strong>Poznámka:</strong> Pro názvy polí s upřednostňovaným vstupním režimem nastaveným na <strong>Vyhledávání</strong> můžete zadat informace ručně, pokud není čárový kód čitelný nebo je poškozen.</span><span class="sxs-lookup"><span data-stu-id="651e5-120"><strong>Note:</strong> For field names with preferred input mode set to <strong>Scanning</strong>, you can enter information manually if the barcode is unreadable or damaged.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="651e5-121">Vstupní typ</span><span class="sxs-lookup"><span data-stu-id="651e5-121">Input type</span></span></td>
<td><span data-ttu-id="651e5-122">Tato možnost určuje, jaký typ vstupu má být použit pro název vybraného pole.</span><span class="sxs-lookup"><span data-stu-id="651e5-122">This option defines what input type should be used for the selected field name.</span></span> <span data-ttu-id="651e5-123">K dispozici jsou čtyři možnosti:</span><span class="sxs-lookup"><span data-stu-id="651e5-123">Four options are available:</span></span>
<ul>
<li><span data-ttu-id="651e5-124"><strong>Výběr </strong> - Obsahuje seznam možností k výběru.</span><span class="sxs-lookup"><span data-stu-id="651e5-124"><strong>Selection</strong> - Contains a list of options to choose from.</span></span> <span data-ttu-id="651e5-125">Názvy polí s touto možností nejsou upravitelné.</span><span class="sxs-lookup"><span data-stu-id="651e5-125">Field names with this option are not editable.</span></span></li>
<li><span data-ttu-id="651e5-126"><strong>Datum</strong> - Názvy polí specifikované jako datum zobrazí formát data s popiskem.</span><span class="sxs-lookup"><span data-stu-id="651e5-126"><strong>Date</strong> - Field names specified as date will show a date format with the label.</span></span> <span data-ttu-id="651e5-127">To pomáhá pracovníkům skladu zjistit, v jakém formátu zadat datum.</span><span class="sxs-lookup"><span data-stu-id="651e5-127">This helps warehouse workers see in which format to enter the date.</span></span> <span data-ttu-id="651e5-128">Názvy polí s touto možností nejsou upravitelné.</span><span class="sxs-lookup"><span data-stu-id="651e5-128">Field names with this option are not editable.</span></span></li>
<li><span data-ttu-id="651e5-129"><strong>Alfa</strong> - Je-li tato možnost vybrána, použije se při ručním zadávání informací do aplikace klávesnice zařízení.</span><span class="sxs-lookup"><span data-stu-id="651e5-129"><strong>Alpha</strong> - If selected, the device keyboard will be used when entering information manually in the app.</span></span> <span data-ttu-id="651e5-130">Vlastnosti klávesnice lze změnit podle toho, na kterém zařízení se používá.</span><span class="sxs-lookup"><span data-stu-id="651e5-130">The keyboard experience can be changed depending on which device is used.</span></span></li>
<li><span data-ttu-id="651e5-131"><strong>Číselný</strong> - Pro názvy polí používající pouze číselné vstupy můžete vybrat tuto možnost, chcete-li zobrazit vlastní numerickou klávesnici s vstupní polem místo klávesnice zařízení.</span><span class="sxs-lookup"><span data-stu-id="651e5-131"><strong>Numeric</strong> - For field names that use numeric input only, you can select this option to display a custom numeric keypad with the input field instead of the device keyboard.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="configure-warehouse-app-field-priority"></a><span data-ttu-id="651e5-132">Konfigurace priority pole aplikace skladu</span><span class="sxs-lookup"><span data-stu-id="651e5-132">Configure warehouse app field priority</span></span>

<span data-ttu-id="651e5-133">Na stránce **Priorita pole aplikace skladu** můžete umístit názvy polí do různých skupin priority.</span><span class="sxs-lookup"><span data-stu-id="651e5-133">On the **Warehouse app field priority** page, you can put field names into different priority groups.</span></span> <span data-ttu-id="651e5-134">Díky tomu je možné se rozhodnout, jaké informace mají být zobrazeny na hlavní stránce úloh, když pracovníci skladu provádět úlohy pomocí této aplikace.</span><span class="sxs-lookup"><span data-stu-id="651e5-134">This makes it possible to decide what information should be displayed on the main task page when warehouse workers perform tasks using the app.</span></span> <span data-ttu-id="651e5-135">Pokud klikněte na možnost **Vytvořit výchozí nastavení**, vygeneruje se výchozí sada skupin priority.</span><span class="sxs-lookup"><span data-stu-id="651e5-135">If you click **Create default setup**, a default set of priority groups will be generated.</span></span> <span data-ttu-id="651e5-136">Je možné vytvořit libovolný počet skupin priority podle potřeby, ale pouze tři skupiny priorit se zobrazí na stránce úloh.</span><span class="sxs-lookup"><span data-stu-id="651e5-136">It is possible to create as many priority groups as needed, but only three priority groups will be shown on the task page.</span></span> <span data-ttu-id="651e5-137">Když systém odesílá metadata do aplikace, přiřadí každému poli relativní prioritu v závislosti na skupině priority, a aplikace zobrazí první tři skupiny priority obsažené v metadatech na stránce úloh.</span><span class="sxs-lookup"><span data-stu-id="651e5-137">When the system sends metadata to the app, it will assign each field a relative priority depending on its priority group, and the app will display the first three priority groups contained in the metadata on the task page.</span></span> <span data-ttu-id="651e5-138">Zbývající metadata se zobrazí na sekundární stránce podrobností.</span><span class="sxs-lookup"><span data-stu-id="651e5-138">The rest of the overflowing metadata will be displayed on a secondary details page.</span></span> <span data-ttu-id="651e5-139">V následující tabulce je uveden příklad pěti skupin priority.</span><span class="sxs-lookup"><span data-stu-id="651e5-139">The following table shows an example of five priority groups.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="651e5-140">Skupina priority</span><span class="sxs-lookup"><span data-stu-id="651e5-140">Priority group</span></span></th>
<th><span data-ttu-id="651e5-141">Přiřazená pole</span><span class="sxs-lookup"><span data-stu-id="651e5-141">Assigned fields</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td> <span data-ttu-id="651e5-142">Priorita 10</span><span class="sxs-lookup"><span data-stu-id="651e5-142">Priority 10</span></span></td>
<td><ul>
<li><span data-ttu-id="651e5-143">Zboží</span><span class="sxs-lookup"><span data-stu-id="651e5-143">Item</span></span></li>
<li><span data-ttu-id="651e5-144">Množství</span><span class="sxs-lookup"><span data-stu-id="651e5-144">Quantity</span></span></li>
<li><span data-ttu-id="651e5-145">Měrná jednotka</span><span class="sxs-lookup"><span data-stu-id="651e5-145">Unit of measure</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td> <span data-ttu-id="651e5-146">Priorita 20</span><span class="sxs-lookup"><span data-stu-id="651e5-146">Priority 20</span></span></td>
<td><ul>
<li><span data-ttu-id="651e5-147">Pozice seskupení</span><span class="sxs-lookup"><span data-stu-id="651e5-147">Cluster position</span></span></li>
<li><span data-ttu-id="651e5-148">Seskupení</span><span class="sxs-lookup"><span data-stu-id="651e5-148">Cluster</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td> <span data-ttu-id="651e5-149">Priorita 30</span><span class="sxs-lookup"><span data-stu-id="651e5-149">Priority 30</span></span></td>
<td><ul>
<li><span data-ttu-id="651e5-150">Popis položky</span><span class="sxs-lookup"><span data-stu-id="651e5-150">Item description</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td> <span data-ttu-id="651e5-151">Priorita 40</span><span class="sxs-lookup"><span data-stu-id="651e5-151">Priority 40</span></span></td>
<td><ul>
<li><span data-ttu-id="651e5-152">Konfigurace</span><span class="sxs-lookup"><span data-stu-id="651e5-152">Configuration</span></span></li>
<li><span data-ttu-id="651e5-153">Barva</span><span class="sxs-lookup"><span data-stu-id="651e5-153">Color</span></span></li>
<li><span data-ttu-id="651e5-154">Velikost</span><span class="sxs-lookup"><span data-stu-id="651e5-154">Size</span></span></li>
<li><span data-ttu-id="651e5-155">Styl</span><span class="sxs-lookup"><span data-stu-id="651e5-155">Style</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td> <span data-ttu-id="651e5-156">Priorita 50</span><span class="sxs-lookup"><span data-stu-id="651e5-156">Priority 50</span></span></td>
<td><ul>
<li><span data-ttu-id="651e5-157">Skl. místo</span><span class="sxs-lookup"><span data-stu-id="651e5-157">Location</span></span></li>
<li><span data-ttu-id="651e5-158">Poznávací značka</span><span class="sxs-lookup"><span data-stu-id="651e5-158">License plate</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

<span data-ttu-id="651e5-159">Například pokud pracovník skladu provádí úlohu na mobilním zařízení, skutečnost, zda se metadata zobrazí v aplikaci, se skládá z následujících polí:</span><span class="sxs-lookup"><span data-stu-id="651e5-159">For example, when a warehouse worker is performing a task on a mobile device, if the metadata that will be displayed in the app consists of the following fields:</span></span>

-   <span data-ttu-id="651e5-160">Zboží</span><span class="sxs-lookup"><span data-stu-id="651e5-160">Item</span></span>
-   <span data-ttu-id="651e5-161">Množství</span><span class="sxs-lookup"><span data-stu-id="651e5-161">Quantity</span></span>
-   <span data-ttu-id="651e5-162">Měrná jednotka</span><span class="sxs-lookup"><span data-stu-id="651e5-162">Unit of measure</span></span>
-   <span data-ttu-id="651e5-163">Popis položky</span><span class="sxs-lookup"><span data-stu-id="651e5-163">Item description</span></span>
-   <span data-ttu-id="651e5-164">Velikost a umístění</span><span class="sxs-lookup"><span data-stu-id="651e5-164">Size and Location</span></span>

<span data-ttu-id="651e5-165">Na základě nastavení priority pole aplikace skladu ve výše uvedené tabulce se zobrazí na stránce úloh následující 3 řádky informací:</span><span class="sxs-lookup"><span data-stu-id="651e5-165">Based on the warehouse app field priority set up in the table above, the following 3 rows of information will be displayed on the task page:</span></span>

-   <span data-ttu-id="651e5-166">Řádek 1: Položka, množství a měrná jednotka</span><span class="sxs-lookup"><span data-stu-id="651e5-166">Row 1: Item, Quantity, Unit of measure</span></span>
-   <span data-ttu-id="651e5-167">Řádek 2: Popis položky</span><span class="sxs-lookup"><span data-stu-id="651e5-167">Row 2: Item description</span></span>
-   <span data-ttu-id="651e5-168">Řádek 3: Velikost</span><span class="sxs-lookup"><span data-stu-id="651e5-168">Row 3: Size</span></span>

<span data-ttu-id="651e5-169">Zbývající metadata, například umístění, se nezobrazí na stránce úloh, ale budou zobrazena na stránce podrobností.</span><span class="sxs-lookup"><span data-stu-id="651e5-169">The remaining metadata, for example, Location, will not be displayed on the task page, but will be displayed on a details page.</span></span> <span data-ttu-id="651e5-170">Další informace a příklady uživatelského rozhraní naleznete v příspěvku blogu [Oznámení aplikace Finance and Operations - Warehousing](https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/).</span><span class="sxs-lookup"><span data-stu-id="651e5-170">To learn more and see examples of the user interface, refer to the blog post [Announcing Finance and Operations - Warehousing](https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/).</span></span>

<a name="additional-resources"></a><span data-ttu-id="651e5-171">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="651e5-171">Additional resources</span></span>
--------

[<span data-ttu-id="651e5-172">Instalace a konfigurace Microsoft Dynamics 365 for Finance and Operations – Sklady</span><span class="sxs-lookup"><span data-stu-id="651e5-172">Install and configure Microsoft Dynamics 365 for Finance and Operations – Warehousing</span></span>](install-configure-warehousing-app.md)
