---
title: Import historických dat pro prognózy poptávky
description: Pro získání přesných předpovědí poptávky požadujete historická data poptávky na položku nebo alokační klíč položky. Toto téma vysvětluje postup při používání datových entit pro import historických dat poptávky z jakéhokoli systému tak, abyste měli delší historii dat prognózy poptávky.
author: roxanadiaconu
ms.date: 05/10/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.reviewer: kamaybac
ms.assetid: 59c0d269-9db0-48e7-b8c7-9a388781a9ca
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: de380113fe951f75c15f9e5526ad2f1f5cc84334
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/16/2021
ms.locfileid: "5908873"
---
# <a name="import-historical-data-for-demand-forecasts"></a><span data-ttu-id="4924c-104">Import historických dat pro prognózy poptávky</span><span class="sxs-lookup"><span data-stu-id="4924c-104">Import historical data for demand forecasts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4924c-105">K zajištění přesnosti prognózy poptávky je nutné mít tolik historických daty poptávky, kolik můžete získat na jednotlivou položku nebo alokační klíč položky.</span><span class="sxs-lookup"><span data-stu-id="4924c-105">To help guarantee the accuracy of demand forecasts, you must have as much historical demand data as you can get per item or item allocation key.</span></span> <span data-ttu-id="4924c-106">Pokud historická data poptávky dosud nebyla importována, použijte k jejich importu datovou entitu **Historická externí poptávka** (ReqDemPlanHistoricalExternalDemandEntity) v aplikaci Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="4924c-106">If the historical demand data isn't already imported, use the **Historical external demand** (ReqDemPlanHistoricalExternalDemandEntity) data entity in Dynamics 365 Supply Chain Management to import it.</span></span>

<span data-ttu-id="4924c-107">V pracovním prostoru **Správa dat** lze zobrazit přehled všech polí v entitě.</span><span class="sxs-lookup"><span data-stu-id="4924c-107">In the **Data management** workspace, you can see an overview of all the fields in the entity.</span></span>

1. <span data-ttu-id="4924c-108">Otevřete pracovní prostor **Správa dat**.</span><span class="sxs-lookup"><span data-stu-id="4924c-108">Open the **Data management** workspace.</span></span>
2. <span data-ttu-id="4924c-109">Vyberte dlaždici **Datové entity**.</span><span class="sxs-lookup"><span data-stu-id="4924c-109">Select the **Data entities** tile.</span></span>
3. <span data-ttu-id="4924c-110">Vyhledejte seznam entit pro možnost **Historická externí poptávka**.</span><span class="sxs-lookup"><span data-stu-id="4924c-110">Search the entity list for **Historical external demand**.</span></span>
4. <span data-ttu-id="4924c-111">Vyberte **Cílová pole**.</span><span class="sxs-lookup"><span data-stu-id="4924c-111">Select **Target fields**.</span></span> <span data-ttu-id="4924c-112">Následující pole entit jsou povinná: site (**DeliveringSiteId**), datum (**DemandDate**), množství (**DemandQuantity**) a číslo položky (**ItemNumber**) nebo alokační klíč položky (**ProductAllocationKeyId**).</span><span class="sxs-lookup"><span data-stu-id="4924c-112">The following entity fields are mandatory: site (**DeliveringSiteId**), date (**DemandDate**), quantity (**DemandQuantity**), and either item number (**ItemNumber**) or item allocation key (**ProductAllocationKeyId**).</span></span>

<span data-ttu-id="4924c-113">Pokud chcete používat datovou entitu, musíte mít soubor Microsoft Excel nebo soubor ve formátu CSV, který obsahuje historická data poptávky.</span><span class="sxs-lookup"><span data-stu-id="4924c-113">To use the data entity, you must have a Microsoft Excel file or comma-separated values (CSV) file that contains the historical demand data.</span></span> <span data-ttu-id="4924c-114">Tento příklad ukazuje, jak importovat data ze souboru CSV.</span><span class="sxs-lookup"><span data-stu-id="4924c-114">The following example shows how to import the data from a CSV file.</span></span>

<span data-ttu-id="4924c-115">Další informace o tom, jak importovat data, včetně toho, jak vyčistit data po importu, najdete v části [Přehled úloh importu a exportu dat](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md) a jsou to související témata.</span><span class="sxs-lookup"><span data-stu-id="4924c-115">For more information about how to import data, including how to clean up data after an import, see [Data import and export jobs overview](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md) and its related topics.</span></span>

## <a name="example"></a><span data-ttu-id="4924c-116">Příklad</span><span class="sxs-lookup"><span data-stu-id="4924c-116">Example</span></span>

<span data-ttu-id="4924c-117">Jako příklad můžete použít následující soubor:</span><span class="sxs-lookup"><span data-stu-id="4924c-117">You can use the following file as an example.</span></span> <span data-ttu-id="4924c-118">Stáhněte si článek [HistoricalDemandData](/dynamics/s-e/).</span><span class="sxs-lookup"><span data-stu-id="4924c-118">Download the [HistoricalDemandData](/dynamics/s-e/).</span></span> <span data-ttu-id="4924c-119">Tento soubor obsahuje historická data poptávky pro položku D0001.</span><span class="sxs-lookup"><span data-stu-id="4924c-119">This file contains the historical demand data for item D0001.</span></span> <span data-ttu-id="4924c-120">Obsahuje pouze následující povinná pole: site, množství a data poptávky.</span><span class="sxs-lookup"><span data-stu-id="4924c-120">It contains only the following mandatory fields: site, quantity, and the demand date.</span></span>

1. <span data-ttu-id="4924c-121">Vyberte společnost do které chcete importovat historická data.</span><span class="sxs-lookup"><span data-stu-id="4924c-121">Select the company to import the historical demand data into.</span></span>
2. <span data-ttu-id="4924c-122">Otevřete pracovní prostor **Správa dat**.</span><span class="sxs-lookup"><span data-stu-id="4924c-122">Open the **Data management** workspace.</span></span>
3. <span data-ttu-id="4924c-123">Vyberte dlaždici **Import**.</span><span class="sxs-lookup"><span data-stu-id="4924c-123">Select the **Import** tile.</span></span>
4. <span data-ttu-id="4924c-124">Zadejte název projektu importu, například **Import historické poptávky pro položku D0001**.</span><span class="sxs-lookup"><span data-stu-id="4924c-124">Enter a name for the import project, such as **Import historical demand for item D0001**.</span></span>
5. <span data-ttu-id="4924c-125">V poli **Formát zdrojových dat** vyberte formát souboru, který importujete.</span><span class="sxs-lookup"><span data-stu-id="4924c-125">In the **Source data format** field, select the file format of the file that you're importing.</span></span> <span data-ttu-id="4924c-126">K importu souboru HistoricalDemandData v tomto příkladu vyberte **CSV**.</span><span class="sxs-lookup"><span data-stu-id="4924c-126">To import the HistoricalDemandData file for this example, select **CSV**.</span></span>
6. <span data-ttu-id="4924c-127">V poli **Název entity** vyberte **Historická externí poptávka**.</span><span class="sxs-lookup"><span data-stu-id="4924c-127">In the **Entity name** field, select **Historical external demand**.</span></span>
7. <span data-ttu-id="4924c-128">Uložte si soubor do počítače a poté jej odešlete.</span><span class="sxs-lookup"><span data-stu-id="4924c-128">Save the file to your computer, and then upload it.</span></span>
8. <span data-ttu-id="4924c-129">Vyberte **Import**.</span><span class="sxs-lookup"><span data-stu-id="4924c-129">Select **Import**.</span></span>
9. <span data-ttu-id="4924c-130">Automaticky se otevře stránka **Souhrn spuštění**.</span><span class="sxs-lookup"><span data-stu-id="4924c-130">The **Execution summary** page is opened automatically.</span></span> <span data-ttu-id="4924c-131">Ověřte importovaná data na stránce.</span><span class="sxs-lookup"><span data-stu-id="4924c-131">Verify the imported data on the page.</span></span>

<span data-ttu-id="4924c-132">Po importu historických dat poptávky lze generovat prognózu poptávky.</span><span class="sxs-lookup"><span data-stu-id="4924c-132">After you've imported the historical demand data, you can generate a demand forecast.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4924c-133">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="4924c-133">Additional resources</span></span>

[<span data-ttu-id="4924c-134">Generování statistické základní prognózy</span><span class="sxs-lookup"><span data-stu-id="4924c-134">Generate a statistical baseline forecast</span></span>](generate-statistical-baseline-forecast.md)  
[<span data-ttu-id="4924c-135">Přehled úloh importu a exportu dat</span><span class="sxs-lookup"><span data-stu-id="4924c-135">Data import and export jobs overview</span></span>](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]