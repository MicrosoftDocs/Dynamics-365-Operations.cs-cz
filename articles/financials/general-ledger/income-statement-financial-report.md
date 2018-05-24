---
title: "Finanční sestava výkazu příjmu"
description: "Tento článek popisuje výchozí sestavu pro výsledovky. Popisuje také stavební bloky, které jsou přidruženy k této sestavě."
author: jcart1106
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 12294
ms.assetid: 30820be0-d943-4f8b-8c25-6414ec393b3d
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 9310508082ff710cd040b74519044f5a90c23988
ms.contentlocale: cs-cz
ms.lasthandoff: 05/08/2018

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

[Blog o finančním výkaznictví v Dynamics](http://blogs.msdn.com/b/dynamics_financial_reporting/)




