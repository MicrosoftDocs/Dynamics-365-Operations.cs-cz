---
title: "Finanční sestava výkazu příjmu"
description: "Tento článek popisuje výchozí sestavu pro výsledovky. Popisuje také stavební bloky, které jsou přidruženy k této sestavě."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 12294
ms.assetid: 30820be0-d943-4f8b-8c25-6414ec393b3d
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: a57badea794667888aebb6b1653c187909afd3b1
ms.contentlocale: cs-cz
ms.lasthandoff: 04/25/2017


---

# <a name="income-statement-financial-report"></a>Finanční sestava výkazu příjmu

[!include[banner](../includes/banner.md)]


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

 

<a name="see-also"></a>Viz také
--------

[Finanční výkaznictví](financial-reporting-getting-started.md)

[Zobrazit finanční sestavy](view-financial-reports.md)

[Blog o finančním výkaznictví v Dynamics](http://blogs.msdn.com/b/dynamics_financial_reporting/)




