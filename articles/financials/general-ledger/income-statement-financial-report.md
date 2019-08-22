---
title: Finanční sestava výkazu příjmu
description: Tento článek popisuje výchozí sestavu pro výsledovky. Popisuje také stavební bloky, které jsou přidruženy k této sestavě.
author: jcart1106
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 12294
ms.assetid: 30820be0-d943-4f8b-8c25-6414ec393b3d
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b7c5d27d43b287aef87f5ead7f469d5465dd2dcb
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/01/2019
ms.locfileid: "1839080"
---
# <a name="income-statement-financial-report"></a>Finanční sestava výkazu příjmu

[!include [banner](../includes/banner.md)]

Tento článek popisuje výchozí sestavu pro výsledovky. Popisuje také stavební bloky, které jsou přidruženy k této sestavě. 

<a name="default-income-statement-report"></a>Výchozí sestava výkazu příjmu
-------------------------------

| Výchozí sestava             | Jak funguje                                                                                              |
|----------------------------|-----------------------------------------------------------------------------------------------------------|
| Výkaz příjmu – výchozí | Umožňuje zobrazit ziskovost organizace za aktuální období a také od začátku roku. |

## <a name="building-blocks"></a>Stavební bloky
Finanční sestava výkazu příjmu používá následující stavební bloky.

| Výchozí sestava             | Definice řádku                     | Definice sloupce          |
|----------------------------|------------------------------------|----------------------------|
| Výkaz příjmu – výchozí | Souhrnný výkazu příjmu – výchozí | Periodický a od začátku roku – výchozí |

### <a name="row-definition"></a>Definice řádku

Definice řádku Souhrnný výkazu příjmu – výchozí obsahuje oddíl pro každou část tradičního výkazu příjmu. Dimenze kategorie hlavního účtu se používá k vytvoření této definice řádku. Z toho vyplývá, že každý může generovat sestavu bez nutnosti provádět změny.

### <a name="column-definition"></a>Definice sloupce

Definice sloupců obsahují různé typy sloupců, které poskytují různé úrovně podrobností a finanční údaje.

-   **Periodický a od začátku roku – výchozí typy sloupce:**
    -   **DESC** – popis z definice řádku
    -   **FD** – finanční údaje pro aktuální období
    -   **FD** – finanční údaje od začátku roku



<a name="additional-resources"></a>Další zdroje
--------

[Finanční výkaznictví](financial-reporting-getting-started.md)

[Zobrazení finančních sestav](view-financial-reports.md)

[Blog o finančním výkaznictví v Dynamics](https://blogs.msdn.com/b/dynamics_financial_reporting/)



