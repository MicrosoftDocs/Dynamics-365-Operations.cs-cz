---
title: "Import historických dat pro prognózy poptávky"
description: "Pro získání přesných předpovědí poptávky požadujete historická data poptávky na položku nebo alokační klíč položky. Toto téma vysvětluje postup při používání datových entit pro import historických dat poptávky z jakéhokoli systému tak, abyste měli delší historii dat prognózy poptávky."
author: roxanadiaconu
manager: AnnBe
ms.date: 05/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.assetid: 59c0d269-9db0-48e7-b8c7-9a388781a9ca
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: b9ab10209eb3c69f754ad3e54066dde5880349aa
ms.contentlocale: cs-cz
ms.lasthandoff: 04/13/2018

---

# <a name="import-historical-data-for-demand-forecasts"></a><span data-ttu-id="58be8-104">Import historických dat pro prognózy poptávky</span><span class="sxs-lookup"><span data-stu-id="58be8-104">Import historical data for demand forecasts</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="58be8-105">K zajištění přesnosti prognózy poptávky je nutné mít tolik historických daty poptávky, kolik můžete získat na jednotlivou položku nebo alokační klíč položky.</span><span class="sxs-lookup"><span data-stu-id="58be8-105">To help guarantee the accuracy of demand forecasts, you must have as much historical demand data as you can get per item or item allocation key.</span></span> <span data-ttu-id="58be8-106">Pokud historická data poptávky dosud nebyla importována, použijte k jejich importu datovou entitu **Historická externí poptávka** (ReqDemPlanHistoricalExternalDemandEntity) v aplikaci Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="58be8-106">If the historical demand data isn't already imported, use the **Historical external demand** (ReqDemPlanHistoricalExternalDemandEntity) data entity in Microsoft Dynamics 365 for Finance and Operations to import it.</span></span>

<span data-ttu-id="58be8-107">V pracovním prostoru **Správa dat** lze zobrazit přehled všech polí v entitě.</span><span class="sxs-lookup"><span data-stu-id="58be8-107">In the **Data management** workspace, you can see an overview of all the fields in the entity.</span></span>

1. <span data-ttu-id="58be8-108">Otevřete pracovní prostor **Správa dat**.</span><span class="sxs-lookup"><span data-stu-id="58be8-108">Open the **Data management** workspace.</span></span>
2. <span data-ttu-id="58be8-109">Klikněte na dlaždici **Datové entity**.</span><span class="sxs-lookup"><span data-stu-id="58be8-109">Click the **Data entities** tile.</span></span>
3. <span data-ttu-id="58be8-110">Vyhledejte seznam entit pro možnost **Historická externí poptávka**.</span><span class="sxs-lookup"><span data-stu-id="58be8-110">Search the entity list for **Historical external demand**.</span></span>
4. <span data-ttu-id="58be8-111">Klikněte na **Cílová pole**.</span><span class="sxs-lookup"><span data-stu-id="58be8-111">Click **Target fields**.</span></span> <span data-ttu-id="58be8-112">Následující pole entit jsou povinná: site (**DeliveringSiteId**), datum (**DemandDate**), množství (**DemandQuantity**) a číslo položky (**ItemNumber**) nebo alokační klíč položky (**ProductAllocationKeyId**).</span><span class="sxs-lookup"><span data-stu-id="58be8-112">The following entity fields are mandatory: site (**DeliveringSiteId**), date (**DemandDate**), quantity (**DemandQuantity**), and either item number (**ItemNumber**) or item allocation key (**ProductAllocationKeyId**).</span></span>

<span data-ttu-id="58be8-113">Pokud chcete používat datovou entitu, musíte mít soubor Microsoft Excel nebo soubor ve formátu CSV, který obsahuje historická data poptávky.</span><span class="sxs-lookup"><span data-stu-id="58be8-113">To use the data entity, you must have a Microsoft Excel file or comma-separated values (CSV) file that contains the historical demand data.</span></span> <span data-ttu-id="58be8-114">Tento příklad ukazuje, jak importovat data ze souboru CSV.</span><span class="sxs-lookup"><span data-stu-id="58be8-114">The following example shows how to import the data from a CSV file.</span></span>

## <a name="example"></a><span data-ttu-id="58be8-115">Příklad</span><span class="sxs-lookup"><span data-stu-id="58be8-115">Example</span></span>

<span data-ttu-id="58be8-116">Jako příklad můžete použít následující soubor:</span><span class="sxs-lookup"><span data-stu-id="58be8-116">You can use the following file as an example.</span></span> <span data-ttu-id="58be8-117">Stáhněte si článek [HistoricalDemandData](https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/365OperationsDemandForecast).</span><span class="sxs-lookup"><span data-stu-id="58be8-117">Download the [HistoricalDemandData](https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/365OperationsDemandForecast).</span></span> <span data-ttu-id="58be8-118">Tento soubor obsahuje historická data poptávky pro položku D0001.</span><span class="sxs-lookup"><span data-stu-id="58be8-118">This file contains the historical demand data for item D0001.</span></span> <span data-ttu-id="58be8-119">Obsahuje pouze následující povinná pole: site, množství a data poptávky.</span><span class="sxs-lookup"><span data-stu-id="58be8-119">It contains only the following mandatory fields: site, quantity, and the demand date.</span></span>

1. <span data-ttu-id="58be8-120">Vyberte společnost do které chcete importovat historická data.</span><span class="sxs-lookup"><span data-stu-id="58be8-120">Select the company to import the historical demand data into.</span></span>
2. <span data-ttu-id="58be8-121">Otevřete pracovní prostor **Správa dat**.</span><span class="sxs-lookup"><span data-stu-id="58be8-121">Open the **Data management** workspace.</span></span>
3. <span data-ttu-id="58be8-122">Klikněte na dlaždici **Import**.</span><span class="sxs-lookup"><span data-stu-id="58be8-122">Click the **Import** tile.</span></span>
4. <span data-ttu-id="58be8-123">Zadejte název projektu importu, například **Import historické poptávky pro položku D0001**.</span><span class="sxs-lookup"><span data-stu-id="58be8-123">Enter a name for the import project, such as **Import historical demand for item D0001**.</span></span>
5. <span data-ttu-id="58be8-124">V poli **Formát zdrojových dat** vyberte formát souboru, který importujete.</span><span class="sxs-lookup"><span data-stu-id="58be8-124">In the **Source data format** field, select the file format of the file that you're importing.</span></span> <span data-ttu-id="58be8-125">K importu souboru HistoricalDemandData v tomto příkladu vyberte **CSV**.</span><span class="sxs-lookup"><span data-stu-id="58be8-125">To import the HistoricalDemandData file for this example, select **CSV**.</span></span>
6. <span data-ttu-id="58be8-126">V poli **Název entity** vyberte **Historická externí poptávka**.</span><span class="sxs-lookup"><span data-stu-id="58be8-126">In the **Entity name** field, select **Historical external demand**.</span></span>
7. <span data-ttu-id="58be8-127">Uložte si soubor do počítače a poté jej odešlete.</span><span class="sxs-lookup"><span data-stu-id="58be8-127">Save the file to your computer, and then upload it.</span></span>
8. <span data-ttu-id="58be8-128">Klikněte na **Importovat**.</span><span class="sxs-lookup"><span data-stu-id="58be8-128">Click **Import**.</span></span>
9. <span data-ttu-id="58be8-129">Automaticky se otevře stránka **Souhrn spuštění**.</span><span class="sxs-lookup"><span data-stu-id="58be8-129">The **Execution summary** page is opened automatically.</span></span> <span data-ttu-id="58be8-130">Ověřte importovaná data na stránce.</span><span class="sxs-lookup"><span data-stu-id="58be8-130">Verify the imported data on the page.</span></span>

<span data-ttu-id="58be8-131">Po importu historických dat poptávky lze generovat prognózu poptávky.</span><span class="sxs-lookup"><span data-stu-id="58be8-131">After you've imported the historical demand data, you can generate a demand forecast.</span></span>

## <a name="see-also"></a><span data-ttu-id="58be8-132">Viz také</span><span class="sxs-lookup"><span data-stu-id="58be8-132">See also</span></span>

[<span data-ttu-id="58be8-133">Generování statistické základní prognózy</span><span class="sxs-lookup"><span data-stu-id="58be8-133">Generate a statistical baseline forecast</span></span>](generate-statistical-baseline-forecast.md)

