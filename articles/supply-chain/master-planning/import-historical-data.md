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
# <a name="import-historical-data-for-demand-forecasts"></a>Import historických dat pro prognózy poptávky

[!include [banner](../includes/banner.md)]

K zajištění přesnosti prognózy poptávky je nutné mít tolik historických daty poptávky, kolik můžete získat na jednotlivou položku nebo alokační klíč položky. Pokud historická data poptávky dosud nebyla importována, použijte k jejich importu datovou entitu **Historická externí poptávka** (ReqDemPlanHistoricalExternalDemandEntity) v aplikaci Dynamics 365 Supply Chain Management.

V pracovním prostoru **Správa dat** lze zobrazit přehled všech polí v entitě.

1. Otevřete pracovní prostor **Správa dat**.
2. Vyberte dlaždici **Datové entity**.
3. Vyhledejte seznam entit pro možnost **Historická externí poptávka**.
4. Vyberte **Cílová pole**. Následující pole entit jsou povinná: site (**DeliveringSiteId**), datum (**DemandDate**), množství (**DemandQuantity**) a číslo položky (**ItemNumber**) nebo alokační klíč položky (**ProductAllocationKeyId**).

Pokud chcete používat datovou entitu, musíte mít soubor Microsoft Excel nebo soubor ve formátu CSV, který obsahuje historická data poptávky. Tento příklad ukazuje, jak importovat data ze souboru CSV.

Další informace o tom, jak importovat data, včetně toho, jak vyčistit data po importu, najdete v části [Přehled úloh importu a exportu dat](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md) a jsou to související témata.

Viz také [Generování statistické základní prognózy](generate-statistical-baseline-forecast.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]