---
title: "Úprava formátu elektronického výkaznictví opětovným použitím šablony aplikace Microsoft Excel"
description: "Toto téma poskytuje informace o tom, jak můžete upravit formát elektronického výkaznictví (ER), který se používá ke generování obchodních dokumentů opětovným použitím šablony aplikace Excel."
author: NickSelin
manager: AnnBe
ms.date: 06/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: ERSolutionTable, ERVendorTable, ERWorkspace
audience: Developer, IT Pro, Application user
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 27621
ms.assetid: e3f7960d-2e01-46a7-9ac8-c355ac933cd6
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 2bc175ceec7ee8771e09f1dac4ede7b3fa619322
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---
# <a name="modify-an-electronic-reporting-format-by-reapplying-a-microsoft-excel-template"></a><span data-ttu-id="fd241-103">Úprava formátu elektronického výkaznictví opětovným použitím šablony aplikace Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="fd241-103">Modify an Electronic reporting format by reapplying a Microsoft Excel template</span></span>
<span data-ttu-id="fd241-104">Nástroj elektronického výkaznictví (ER) slouží ke generování obchodních dokumentů v elektronické podobě.</span><span class="sxs-lookup"><span data-stu-id="fd241-104">The Electronic reporting (ER) tool is used to generate business documents in an electronic format.</span></span> <span data-ttu-id="fd241-105">Ke generování obchodních dokumentů musíte vytvořit formátu elektronického výkaznictví a pak použít návrháře elektronického výkaznictví k definování rozvržení obchodního dokument a určení dat, která v něm mají být obsažena.</span><span class="sxs-lookup"><span data-stu-id="fd241-105">To generate a business document, you must create an ER format, and then use the ER designer to define the layout of the business document and specify the data that should be included in it.</span></span> <span data-ttu-id="fd241-106">Poté lze spustit ER formát pro generování obchodního dokumentu.</span><span class="sxs-lookup"><span data-stu-id="fd241-106">You can then run the ER format to generate the business document.</span></span>

<span data-ttu-id="fd241-107">Nástroj elektronického výkaznictví slouží ke generování obchodních dokumentů jako souborů aplikace Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="fd241-107">The ER tool can be used to generate business documents as Microsoft Excel files.</span></span> <span data-ttu-id="fd241-108">Dokument Excel lze použít jako šablonu pro tyto dokumenty.</span><span class="sxs-lookup"><span data-stu-id="fd241-108">You can use an Excel document as a template for these documents.</span></span> <span data-ttu-id="fd241-109">Chcete-li definovat rozvržení dokumentu v návrháři elektronického výkaznictví, můžete importovat obsah dokumentu aplikace Excel, který chcete použít, jako šablonu do definovaného formátu elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="fd241-109">To define the document layout in the ER designer, you can import the contents of the Excel document that you want to use as a template into the defined ER format.</span></span> <span data-ttu-id="fd241-110">Abyste se podrobně seznámili s tímto postupem a procvičili si tento scénář, přehrajte si průvodce záznamem úlohy **Elektronické vykazování – Návrh konfigurace pro generování sestav ve formátu OPENXML** (součást obchodního procesu 7.5.4.3 Získání/vývoj součástí IT služeb/řešení (10677)).</span><span class="sxs-lookup"><span data-stu-id="fd241-110">For more details, and to practice this scenario, play the task guide **ER Design a configuration for generating reports in OPENXML format** (part of the 7.5.4.3 Acquire/Develop IT service/solution components (10677) business process).</span></span>

<span data-ttu-id="fd241-111">Pokud upravíte dokument aplikace Excel, který je použit jako šablona pro obchodní dokument, nová funkce elektronického výkaznictví vám umožní znovu použít aktualizovanou šablonu do formátu elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="fd241-111">If you edit the Excel document that is used as a template for a business document, new ER functionality lets you reapply the updated template to the ER format.</span></span> <span data-ttu-id="fd241-112">Formát ER se pak aktualizuje tak, aby odpovídal aktualizované šabloně.</span><span class="sxs-lookup"><span data-stu-id="fd241-112">The ER format is then updated so that it adheres to the updated template.</span></span> <span data-ttu-id="fd241-113">Abyste se podrobně seznámili s tímto postupem, přehrajte si průvodce záznamem úlohy **Elektronické vykazování – Úprava formátu opětovným použitím šablony aplikace Excel** (součást obchodního procesu 7.5.5.3 Získání/vývoj součástí IT služeb/řešení (10683)).</span><span class="sxs-lookup"><span data-stu-id="fd241-113">For more details about this functionality, play the task guide **ER Modify a format by reapplying an Excel template** (part of the 7.5.5.3 Acquire/Develop IT service/solution components (10683) business process).</span></span> <span data-ttu-id="fd241-114">V rámci kroku průvodce záznamem úlohy, kde importujete aktualizovanou šablonu, použijte jako šablonu upravenou šablonu souboru aplikace Excel sestavy platby s názvem SampleVendPaymWsReport2.</span><span class="sxs-lookup"><span data-stu-id="fd241-114">In the task guide step where you import an updated template, use the modified template of the Payment Report Excel file, SampleVendPaymWsReport2, as a template.</span></span>

