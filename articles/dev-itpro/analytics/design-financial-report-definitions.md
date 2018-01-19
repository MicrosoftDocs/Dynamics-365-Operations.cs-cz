---
title: "Definice sestavy v návrháři finanční sestavy"
description: "Tento článek obsahuje informace o definicích sestavy. Definice sestavy představuje součást sestavy (nebo stavební blok), který využívá definici řádku, definici sloupce a volitelně definici stromu výkaznictví pro vytvoření sestavy. Definice sestavy také poskytuje možnosti a nastavení pro přizpůsobení sestavy."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 59131
ms.assetid: 966a3f1d-c59c-4a84-acd4-5bb7e65144c8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: ceea24519d641c676521771cee274feb64ca7783
ms.openlocfilehash: e16471e6570989b678b1856a8199796084c38bc7
ms.contentlocale: cs-cz
ms.lasthandoff: 01/19/2018

---

# <a name="report-definitions-in-financial-report-designer"></a><span data-ttu-id="75c0d-105">Definice sestavy v návrháři finanční sestavy</span><span class="sxs-lookup"><span data-stu-id="75c0d-105">Report definitions in financial report designer</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="75c0d-106">Tento článek obsahuje informace o definicích sestavy.</span><span class="sxs-lookup"><span data-stu-id="75c0d-106">This article provides information about report definitions.</span></span> <span data-ttu-id="75c0d-107">Definice sestavy představuje součást sestavy (nebo stavební blok), který využívá definici řádku, definici sloupce a volitelně definici stromu výkaznictví pro vytvoření sestavy.</span><span class="sxs-lookup"><span data-stu-id="75c0d-107">A report definition is a report component (or building block) that uses a row definition, a column definition, and an optional reporting tree definition to create a report.</span></span> <span data-ttu-id="75c0d-108">Definice sestavy také poskytuje možnosti a nastavení pro přizpůsobení sestavy.</span><span class="sxs-lookup"><span data-stu-id="75c0d-108">A report definition also provides options and settings that for customizing a report.</span></span> 

<span data-ttu-id="75c0d-109">Definice sestavy představuje součást sestavy (nebo stavební blok), který využívá definici řádku, definici sloupce a volitelně definici stromu výkaznictví pro vytvoření sestavy.</span><span class="sxs-lookup"><span data-stu-id="75c0d-109">A report definition is a report component (or building block) that uses a row definition, a column definition, and an optional reporting tree definition to create a report.</span></span> <span data-ttu-id="75c0d-110">Definice sestavy nabízí také další možnosti a nastavení, které můžete použít pro přizpůsobení sestavy.</span><span class="sxs-lookup"><span data-stu-id="75c0d-110">A report definition also provides options and settings that you can use to customize a report.</span></span> <span data-ttu-id="75c0d-111">Po vytvoření definic řádků a sloupců je nutno je zkombinovat do definice sestavy.</span><span class="sxs-lookup"><span data-stu-id="75c0d-111">After you define row definitions and column definitions, you must combine them in a report definition.</span></span> <span data-ttu-id="75c0d-112">V tomto okamžiku můžete také definovat další aspekty definic, například úroveň podrobností a datum sestavy.</span><span class="sxs-lookup"><span data-stu-id="75c0d-112">At this point, you also define other aspects of the definitions, such as the detail level and report date.</span></span> <span data-ttu-id="75c0d-113">Poté můžete sestavu uložit a vygenerovat.</span><span class="sxs-lookup"><span data-stu-id="75c0d-113">You can then save and generate a report.</span></span> <span data-ttu-id="75c0d-114">Finanční výkaznictví nabízí následující úrovně podrobností:</span><span class="sxs-lookup"><span data-stu-id="75c0d-114">Financial reporting offers the following levels of detail:</span></span>

-   <span data-ttu-id="75c0d-115">Finanční</span><span class="sxs-lookup"><span data-stu-id="75c0d-115">Financial</span></span>
-   <span data-ttu-id="75c0d-116">Finanční a účetní</span><span class="sxs-lookup"><span data-stu-id="75c0d-116">Financial and Account</span></span>
-   <span data-ttu-id="75c0d-117">Finanční, účetní a transakční</span><span class="sxs-lookup"><span data-stu-id="75c0d-117">Financial, Account, and Transaction</span></span>

<span data-ttu-id="75c0d-118">V závislosti na tom, jak jsou data v systému Microsoft Dynamics ERP uložena, však v sestavách nemusejí být dostupné podrobnosti transakcí.</span><span class="sxs-lookup"><span data-stu-id="75c0d-118">However, depending on how data is stored in the Microsoft Dynamics ERP system, transaction details might not be available in reports.</span></span>

## <a name="create-a-report-definition"></a><span data-ttu-id="75c0d-119">Vytvoření definice sestavy</span><span class="sxs-lookup"><span data-stu-id="75c0d-119">Create a report definition</span></span>
1.  <span data-ttu-id="75c0d-120">V Návrháři sestav v nabídce **Soubor** klikněte na tlačítko **Nový** a vyberte možnost **Definice sestavy**.</span><span class="sxs-lookup"><span data-stu-id="75c0d-120">In Report Designer, on the **File** menu, click **New**, and then select **Report Definition**.</span></span>
2.  <span data-ttu-id="75c0d-121">Zadejte příslušné informace na kartách **Sestava**, **Výstup a distribuce**, **Záhlaví a zápatí** a **Nastavení**.</span><span class="sxs-lookup"><span data-stu-id="75c0d-121">Specify the appropriate information on the **Report**, **Output and Distribution**, **Headers and Footers**, and **Settings** tabs.</span></span>

## <a name="contents-of-a-report-definition"></a><span data-ttu-id="75c0d-122">Obsah definice sestavy</span><span class="sxs-lookup"><span data-stu-id="75c0d-122">Contents of a report definition</span></span>
<span data-ttu-id="75c0d-123">Následující tabulka popisuje karty v definici sestavy a způsob použití těchto informací.</span><span class="sxs-lookup"><span data-stu-id="75c0d-123">The following table describes the tabs in a report definition and how the information is used.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="75c0d-124">TAB</span><span class="sxs-lookup"><span data-stu-id="75c0d-124">Tab</span></span></th>
<th><span data-ttu-id="75c0d-125">Popis</span><span class="sxs-lookup"><span data-stu-id="75c0d-125">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="75c0d-126">Sestava</span><span class="sxs-lookup"><span data-stu-id="75c0d-126">Report</span></span></td>
<td><span data-ttu-id="75c0d-127">Umožňuje vytvořit sestavu, konfigurovat sestavu nebo změnit existující sestavu.</span><span class="sxs-lookup"><span data-stu-id="75c0d-127">Create a report, configure a report, or modify an existing report.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="75c0d-128">Výstup a distribuce</span><span class="sxs-lookup"><span data-stu-id="75c0d-128">Output and Distribution</span></span></td>
<td><span data-ttu-id="75c0d-129">Umožňuje změnit typ výstupu a cílové umístění sestavy.</span><span class="sxs-lookup"><span data-stu-id="75c0d-129">Change the output type and destination of the report.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="75c0d-130">Záhlaví a zápatí</span><span class="sxs-lookup"><span data-stu-id="75c0d-130">Headers and Footers</span></span></td>
<td><span data-ttu-id="75c0d-131">Umožňuje definovat a naformátovat záhlaví a zápatí sestavy.</span><span class="sxs-lookup"><span data-stu-id="75c0d-131">Define and format the headers and footers for the report.</span></span> <span data-ttu-id="75c0d-132">Například můžete přidat text a obrázky pro záhlaví nebo zápatí.</span><span class="sxs-lookup"><span data-stu-id="75c0d-132">For example, you can add text or images to the header or footer.</span></span> <span data-ttu-id="75c0d-133">Finanční výkaznictví podporuje soubory BMP, JPG a PNG jako obrázky.</span><span class="sxs-lookup"><span data-stu-id="75c0d-133">Financial reporting supports .bmp, .jpg, and .png files for images.</span></span> <span data-ttu-id="75c0d-134">Můžete také přidat kódy automatického textu a vložit tak další informace, například název společnosti, název sestavy nebo číslo stránky.</span><span class="sxs-lookup"><span data-stu-id="75c0d-134">You can also add autotext codes to insert other information, such as a company name, report name, or page number.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="75c0d-135">Nastavení</span><span class="sxs-lookup"><span data-stu-id="75c0d-135">Settings</span></span></td>
<td><span data-ttu-id="75c0d-136">Zadejte nastavení definice sestavy, například následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="75c0d-136">Specify report definition settings, such as the following settings:</span></span>
<ul>
<li><span data-ttu-id="75c0d-137">Formátování a částky ze zaokrouhlení</span><span class="sxs-lookup"><span data-stu-id="75c0d-137">Formatting and rounding amounts</span></span></li>
<li><span data-ttu-id="75c0d-138">Formát sestavy podrobností</span><span class="sxs-lookup"><span data-stu-id="75c0d-138">Format detail reports</span></span></li>
<li><span data-ttu-id="75c0d-139">Formátování organizačního stromu</span><span class="sxs-lookup"><span data-stu-id="75c0d-139">Format reporting trees</span></span></li>
<li><span data-ttu-id="75c0d-140">Generování sestavy výjimek</span><span class="sxs-lookup"><span data-stu-id="75c0d-140">Generate an exception report</span></span></li>
<li><span data-ttu-id="75c0d-141">Určení převodu měny</span><span class="sxs-lookup"><span data-stu-id="75c0d-141">Specify currency conversion</span></span></li>
<li><span data-ttu-id="75c0d-142">Mezisoučty a filtrování podrobností účtu</span><span class="sxs-lookup"><span data-stu-id="75c0d-142">Subtotal and filter account details</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



<a name="see-also"></a><span data-ttu-id="75c0d-143">Viz také</span><span class="sxs-lookup"><span data-stu-id="75c0d-143">See also</span></span>
--------

[<span data-ttu-id="75c0d-144">Finanční výkaznictví</span><span class="sxs-lookup"><span data-stu-id="75c0d-144">Financial reporting</span></span>](financial-reporting-intro.md)




