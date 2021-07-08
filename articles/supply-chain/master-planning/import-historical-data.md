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
ms.openlocfilehash: 0b04ee246d4c28e934407ccb92d792692cc4347d
ms.sourcegitcommit: cbbb35c71ab4ff1ae08fa4f7cc97019b207246be
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/23/2021
ms.locfileid: "6301643"
---
# <a name="import-historical-data-for-demand-forecasts"></a><span data-ttu-id="046c0-104">Import historických dat pro prognózy poptávky</span><span class="sxs-lookup"><span data-stu-id="046c0-104">Import historical data for demand forecasts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="046c0-105">K zajištění přesnosti prognózy poptávky je nutné mít tolik historických daty poptávky, kolik můžete získat na jednotlivou položku nebo alokační klíč položky.</span><span class="sxs-lookup"><span data-stu-id="046c0-105">To help guarantee the accuracy of demand forecasts, you must have as much historical demand data as you can get per item or item allocation key.</span></span> <span data-ttu-id="046c0-106">Pokud historická data poptávky dosud nebyla importována, použijte k jejich importu datovou entitu **Historická externí poptávka** (ReqDemPlanHistoricalExternalDemandEntity) v aplikaci Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="046c0-106">If the historical demand data isn't already imported, use the **Historical external demand** (ReqDemPlanHistoricalExternalDemandEntity) data entity in Dynamics 365 Supply Chain Management to import it.</span></span>

<span data-ttu-id="046c0-107">V pracovním prostoru **Správa dat** lze zobrazit přehled všech polí v entitě.</span><span class="sxs-lookup"><span data-stu-id="046c0-107">In the **Data management** workspace, you can see an overview of all the fields in the entity.</span></span>

1. <span data-ttu-id="046c0-108">Otevřete pracovní prostor **Správa dat**.</span><span class="sxs-lookup"><span data-stu-id="046c0-108">Open the **Data management** workspace.</span></span>
2. <span data-ttu-id="046c0-109">Vyberte dlaždici **Datové entity**.</span><span class="sxs-lookup"><span data-stu-id="046c0-109">Select the **Data entities** tile.</span></span>
3. <span data-ttu-id="046c0-110">Vyhledejte seznam entit pro možnost **Historická externí poptávka**.</span><span class="sxs-lookup"><span data-stu-id="046c0-110">Search the entity list for **Historical external demand**.</span></span>
4. <span data-ttu-id="046c0-111">Vyberte **Cílová pole**.</span><span class="sxs-lookup"><span data-stu-id="046c0-111">Select **Target fields**.</span></span> <span data-ttu-id="046c0-112">Následující pole entit jsou povinná: site (**DeliveringSiteId**), datum (**DemandDate**), množství (**DemandQuantity**) a číslo položky (**ItemNumber**) nebo alokační klíč položky (**ProductAllocationKeyId**).</span><span class="sxs-lookup"><span data-stu-id="046c0-112">The following entity fields are mandatory: site (**DeliveringSiteId**), date (**DemandDate**), quantity (**DemandQuantity**), and either item number (**ItemNumber**) or item allocation key (**ProductAllocationKeyId**).</span></span>

<span data-ttu-id="046c0-113">Pokud chcete používat datovou entitu, musíte mít soubor Microsoft Excel nebo soubor ve formátu CSV, který obsahuje historická data poptávky.</span><span class="sxs-lookup"><span data-stu-id="046c0-113">To use the data entity, you must have a Microsoft Excel file or comma-separated values (CSV) file that contains the historical demand data.</span></span> <span data-ttu-id="046c0-114">Tento příklad ukazuje, jak importovat data ze souboru CSV.</span><span class="sxs-lookup"><span data-stu-id="046c0-114">The following example shows how to import the data from a CSV file.</span></span>

<span data-ttu-id="046c0-115">Další informace o tom, jak importovat data, včetně toho, jak vyčistit data po importu, najdete v části [Přehled úloh importu a exportu dat](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md) a jsou to související témata.</span><span class="sxs-lookup"><span data-stu-id="046c0-115">For more information about how to import data, including how to clean up data after an import, see [Data import and export jobs overview](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md) and its related topics.</span></span>

<span data-ttu-id="046c0-116">Viz také [Generování statistické základní prognózy](generate-statistical-baseline-forecast.md).</span><span class="sxs-lookup"><span data-stu-id="046c0-116">See also [Generate a statistical baseline forecast](generate-statistical-baseline-forecast.md).</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]