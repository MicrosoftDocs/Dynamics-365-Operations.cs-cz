---
title: Definice sestavy v návrháři finanční sestavy
description: Tento článek obsahuje informace o definicích sestavy.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: kfend
ms.custom: 59131
ms.assetid: 966a3f1d-c59c-4a84-acd4-5bb7e65144c8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 073df430892e01d4842b2af147b0ae2765b1c66a
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570335"
---
# <a name="report-definitions-in-financial-report-designer"></a><span data-ttu-id="3008c-103">Definice sestavy v návrháři finanční sestavy</span><span class="sxs-lookup"><span data-stu-id="3008c-103">Report definitions in financial report designer</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3008c-104">Tento článek obsahuje informace o definicích sestavy.</span><span class="sxs-lookup"><span data-stu-id="3008c-104">This article provides information about report definitions.</span></span> <span data-ttu-id="3008c-105">Definice sestavy představuje součást sestavy (nebo stavební blok), který využívá definici řádku, definici sloupce a volitelně definici stromu výkaznictví pro vytvoření sestavy.</span><span class="sxs-lookup"><span data-stu-id="3008c-105">A report definition is a report component (or building block) that uses a row definition, a column definition, and an optional reporting tree definition to create a report.</span></span> <span data-ttu-id="3008c-106">Definice sestavy také poskytuje možnosti a nastavení pro přizpůsobení sestavy.</span><span class="sxs-lookup"><span data-stu-id="3008c-106">A report definition also provides options and settings that for customizing a report.</span></span> 

<span data-ttu-id="3008c-107">Definice sestavy představuje součást sestavy (nebo stavební blok), který využívá definici řádku, definici sloupce a volitelně definici stromu výkaznictví pro vytvoření sestavy.</span><span class="sxs-lookup"><span data-stu-id="3008c-107">A report definition is a report component (or building block) that uses a row definition, a column definition, and an optional reporting tree definition to create a report.</span></span> <span data-ttu-id="3008c-108">Definice sestavy nabízí také další možnosti a nastavení, které můžete použít pro přizpůsobení sestavy.</span><span class="sxs-lookup"><span data-stu-id="3008c-108">A report definition also provides options and settings that you can use to customize a report.</span></span> <span data-ttu-id="3008c-109">Po vytvoření definic řádků a sloupců je nutno je zkombinovat do definice sestavy.</span><span class="sxs-lookup"><span data-stu-id="3008c-109">After you define row definitions and column definitions, you must combine them in a report definition.</span></span> <span data-ttu-id="3008c-110">V tomto okamžiku můžete také definovat další aspekty definic, například úroveň podrobností a datum sestavy.</span><span class="sxs-lookup"><span data-stu-id="3008c-110">At this point, you also define other aspects of the definitions, such as the detail level and report date.</span></span> <span data-ttu-id="3008c-111">Poté můžete sestavu uložit a vygenerovat.</span><span class="sxs-lookup"><span data-stu-id="3008c-111">You can then save and generate a report.</span></span> <span data-ttu-id="3008c-112">Finanční výkaznictví nabízí následující úrovně podrobností:</span><span class="sxs-lookup"><span data-stu-id="3008c-112">Financial reporting offers the following levels of detail:</span></span>

- <span data-ttu-id="3008c-113">Finanční</span><span class="sxs-lookup"><span data-stu-id="3008c-113">Financial</span></span>
- <span data-ttu-id="3008c-114">Finanční a účetní</span><span class="sxs-lookup"><span data-stu-id="3008c-114">Financial and Account</span></span>
- <span data-ttu-id="3008c-115">Finanční, účetní a transakční</span><span class="sxs-lookup"><span data-stu-id="3008c-115">Financial, Account, and Transaction</span></span>

<span data-ttu-id="3008c-116">V závislosti na tom, jak jsou data v systému Microsoft Dynamics ERP uložena, však v sestavách nemusejí být dostupné podrobnosti transakcí.</span><span class="sxs-lookup"><span data-stu-id="3008c-116">However, depending on how data is stored in the Microsoft Dynamics ERP system, transaction details might not be available in reports.</span></span>

## <a name="create-a-report-definition"></a><span data-ttu-id="3008c-117">Vytvoření definice sestavy</span><span class="sxs-lookup"><span data-stu-id="3008c-117">Create a report definition</span></span>
1. <span data-ttu-id="3008c-118">V Návrháři sestav v nabídce **Soubor** klikněte na tlačítko **Nový** a vyberte možnost **Definice sestavy**.</span><span class="sxs-lookup"><span data-stu-id="3008c-118">In Report Designer, on the **File** menu, click **New**, and then select **Report Definition**.</span></span>
2. <span data-ttu-id="3008c-119">Zadejte příslušné informace na kartách **Sestava**, **Výstup a distribuce**, **Záhlaví a zápatí** a **Nastavení**.</span><span class="sxs-lookup"><span data-stu-id="3008c-119">Specify the appropriate information on the **Report**, **Output and Distribution**, **Headers and Footers**, and **Settings** tabs.</span></span>

## <a name="contents-of-a-report-definition"></a><span data-ttu-id="3008c-120">Obsah definice sestavy</span><span class="sxs-lookup"><span data-stu-id="3008c-120">Contents of a report definition</span></span>
<span data-ttu-id="3008c-121">Následující tabulka popisuje karty v definici sestavy a způsob použití těchto informací.</span><span class="sxs-lookup"><span data-stu-id="3008c-121">The following table describes the tabs in a report definition and how the information is used.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="3008c-122">TAB</span><span class="sxs-lookup"><span data-stu-id="3008c-122">Tab</span></span></th>
<th><span data-ttu-id="3008c-123">Popis</span><span class="sxs-lookup"><span data-stu-id="3008c-123">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3008c-124">Sestava</span><span class="sxs-lookup"><span data-stu-id="3008c-124">Report</span></span></td>
<td><span data-ttu-id="3008c-125">Umožňuje vytvořit sestavu, konfigurovat sestavu nebo změnit existující sestavu.</span><span class="sxs-lookup"><span data-stu-id="3008c-125">Create a report, configure a report, or modify an existing report.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3008c-126">Výstup a distribuce</span><span class="sxs-lookup"><span data-stu-id="3008c-126">Output and Distribution</span></span></td>
<td><span data-ttu-id="3008c-127">Umožňuje změnit typ výstupu a cílové umístění sestavy.</span><span class="sxs-lookup"><span data-stu-id="3008c-127">Change the output type and destination of the report.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3008c-128">Záhlaví a zápatí</span><span class="sxs-lookup"><span data-stu-id="3008c-128">Headers and Footers</span></span></td>
<td><span data-ttu-id="3008c-129">Umožňuje definovat a naformátovat záhlaví a zápatí sestavy.</span><span class="sxs-lookup"><span data-stu-id="3008c-129">Define and format the headers and footers for the report.</span></span> <span data-ttu-id="3008c-130">Například můžete přidat text a obrázky pro záhlaví nebo zápatí.</span><span class="sxs-lookup"><span data-stu-id="3008c-130">For example, you can add text or images to the header or footer.</span></span> <span data-ttu-id="3008c-131">Finanční výkaznictví podporuje soubory BMP, JPG a PNG jako obrázky.</span><span class="sxs-lookup"><span data-stu-id="3008c-131">Financial reporting supports .bmp, .jpg, and .png files for images.</span></span> <span data-ttu-id="3008c-132">Můžete také přidat kódy automatického textu a vložit tak další informace, například název společnosti, název sestavy nebo číslo stránky.</span><span class="sxs-lookup"><span data-stu-id="3008c-132">You can also add autotext codes to insert other information, such as a company name, report name, or page number.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3008c-133">Nastavení</span><span class="sxs-lookup"><span data-stu-id="3008c-133">Settings</span></span></td>
<td><span data-ttu-id="3008c-134">Zadejte nastavení definice sestavy, například následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="3008c-134">Specify report definition settings, such as the following settings:</span></span>
<ul>
<li><span data-ttu-id="3008c-135">Formátování a částky ze zaokrouhlení</span><span class="sxs-lookup"><span data-stu-id="3008c-135">Formatting and rounding amounts</span></span></li>
<li><span data-ttu-id="3008c-136">Formát sestavy podrobností</span><span class="sxs-lookup"><span data-stu-id="3008c-136">Format detail reports</span></span></li>
<li><span data-ttu-id="3008c-137">Formátování organizačního stromu</span><span class="sxs-lookup"><span data-stu-id="3008c-137">Format reporting trees</span></span></li>
<li><span data-ttu-id="3008c-138">Generování sestavy výjimek</span><span class="sxs-lookup"><span data-stu-id="3008c-138">Generate an exception report</span></span></li>
<li><span data-ttu-id="3008c-139">Určit převod měny</span><span class="sxs-lookup"><span data-stu-id="3008c-139">Specify currency conversion</span></span></li>
<li><span data-ttu-id="3008c-140">Podrobnosti o mezisoučtu a filtrování podrobností účtů.</span><span class="sxs-lookup"><span data-stu-id="3008c-140">Subtotal and filter account details</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a><span data-ttu-id="3008c-141">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="3008c-141">Additional resources</span></span>

[<span data-ttu-id="3008c-142">Finanční výkaznictví</span><span class="sxs-lookup"><span data-stu-id="3008c-142">Financial reporting</span></span>](financial-reporting-intro.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]