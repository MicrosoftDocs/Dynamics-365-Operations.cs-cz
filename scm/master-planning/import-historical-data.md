---
title: "Import historických dat pro prognózy poptávky"
description: "Pro získání přesných předpovědí poptávky požadujete historická data poptávky na položku nebo alokační klíč položky. Toto téma vysvětluje postup při používání datových entit pro import historických dat poptávky z jakéhokoli systému tak, abyste měli delší historii dat prognózy poptávky."
author: YuyuScheller
manager: AnnBe
ms.date: 05/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.assetid: 59c0d269-9db0-48e7-b8c7-9a388781a9ca
ms.search.region: Global
ms.author: roxanad
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 0d1e2b9a51c2d7a7c30c2458b7babf8ac5c08118
ms.contentlocale: cs-cz
ms.lasthandoff: 05/25/2017


---

# <a name="import-historical-data-for-demand-forecasts"></a>Import historických dat pro prognózy poptávky

[!include[banner](../includes/banner.md)]

K zajištění přesnosti prognózy poptávky je nutné mít tolik historických daty poptávky, kolik můžete získat na jednotlivou položku nebo alokační klíč položky. Pokud historická data poptávky dosud nebyla importována, použijte k jejich importu datovou entitu **Historická externí poptávka** (ReqDemPlanHistoricalExternalDemandEntity) v aplikaci Microsoft Dynamics 365 for Operations.

V pracovním prostoru **Správa dat** lze zobrazit přehled všech polí v entitě.

1. Otevřete pracovní prostor **Správa dat**.
2. Klikněte na dlaždici **Datové entity**.
3. Vyhledejte seznam entit pro možnost **Historická externí poptávka**.
4. Klikněte na **Cílová pole**. Následující pole entit jsou povinná: site (**DeliveringSiteId**), datum (**DemandDate**), množství (****) a číslo položky (****) nebo alokační klíč položky (**ProductAllocationKeyId**).

Pokud chcete používat datovou entitu, musíte mít soubor Microsoft Excel nebo soubor ve formátu CSV, který obsahuje historická data poptávky. Tento příklad ukazuje, jak importovat data ze souboru CSV.

## <a name="example"></a>Příklad

Jako příklad můžete použít následující soubor: Stáhněte si článek [HistoricalDemandData](https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/365OperationsDemandForecast). Tento soubor obsahuje historická data poptávky pro položku D0001. Obsahuje pouze následující povinná pole: site, množství a data poptávky.

1. Vyberte společnost do které chcete importovat historická data.
2. Otevřete pracovní prostor **Správa dat**.
3. Klikněte na dlaždici **Import**.
4. Zadejte název projektu importu, například **Import historické poptávky pro položku D0001**.
5. V poli **Formát zdrojových dat** vyberte formát souboru, který importujete. K importu souboru HistoricalDemandData v tomto příkladu vyberte **CSV**.
6. V poli **Název entity** vyberte **Historická externí poptávka**.
7. Uložte si soubor do počítače a poté jej odešlete.
8. Klikněte na **Importovat**.
9. Automaticky se otevře stránka **Souhrn spuštění**. Ověřte importovaná data na stránce.

Po importu historických dat poptávky lze generovat prognózu poptávky.

## <a name="see-also"></a>Viz také

[Generování statistické základní prognózy](generate-statistical-baseline-forecast.md)
