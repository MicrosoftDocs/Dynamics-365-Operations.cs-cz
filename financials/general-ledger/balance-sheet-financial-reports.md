---
title: "Finanční sestavy rozvah"
description: "Tento článek popisuje výchozí sestavy pro rozvahy. Popisuje také stavební bloky, které jsou přidruženy k těmto sestavám."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 12274
ms.assetid: 52f78229-f531-4d16-b337-e2628994acb6
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 1cb7ef4b1b08caff39f0693eef6743bbe5d3892e
ms.contentlocale: cs-cz
ms.lasthandoff: 05/25/2017


---

# <a name="balance-sheet-financial-reports"></a>Finanční sestavy rozvah

[!include[banner](../includes/banner.md)]


Tento článek popisuje výchozí sestavy pro rozvahy. Popisuje také stavební bloky, které jsou přidruženy k těmto sestavám. 

<a name="default-balance-sheet-reports"></a>Výchozí finanční sestavy rozvah
-----------------------------

Existují dvě výchozí finanční sestavy rozvah. V jedné sestavě jsou oddíly nad sebou. Ve druhé jsou oddíly vedle sebe.

| Výchozí sestava                       | Jak funguje                                                                                                                           |
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| Rozvaha – výchozí              | Poskytuje přehled finanční pozice organizace pro rok.                                                                 |
| Rozvaha vedle sebe – výchozí | Poskytuje přehled finanční pozice organizace pro rok. Aktiva a pasiva a jmění akcionářů jsou vedle sebe. |

## <a name="building-blocks"></a>Stavební bloky
Finanční sestavy rozvahy používají následující stavební bloky.

| Výchozí sestava                       | Definice řádku                       | Definice sloupce             |
|--------------------------------------|--------------------------------------|-------------------------------|
| Rozvaha – výchozí              | Rozvaha – výchozí              | Od začátku roku a odchylka – výchozí    |
| Rozvaha vedle sebe – výchozí | Rozvaha vedle sebe – výchozí | Sloupec od začátku roku – výchozí |

### <a name="row-definition"></a>Definice řádku

Definice řádku pro obě sestavy rozvahy obsahují oddíly pro každou součást tradiční rozvahy. Sestava vedle sebe obsahuje zalomení sloupce, takže odpovědnosti a vlastní jmění společnosti se zobrazují vedle majetku. Dimenze kategorie hlavního účtu se používá k vytvoření obou definic řádku. Z toho vyplývá, že každý může generovat sestavy bez nutnosti provádět změny.

### <a name="column-definition"></a>Definice sloupce

Definice sloupců obsahují různé typy sloupců, které poskytují různé úrovně podrobností a finanční údaje.

-   **Od začátku roku a odchylka – výchozí typy sloupce:**
    -   **DESC** – popis z definice řádku
    -   **FD** – Finanční data od začátku roku pro aktuální rok
    -   **FD** – Finanční data od začátku roku pro minulý rok
    -   **CALC** – odchylky od odečtení minulého roku z tohoto roku

<!-- -->

-   **Sloupec od začátku roku – výchozí:**
    -   **DESC** – popis z definice řádku
    -   **FD** – Finanční data od začátku roku pro aktuální rok

 

<a name="see-also"></a>Viz také
--------

[Finanční výkaznictví](financial-reporting-getting-started.md)

[Zobrazit finanční sestavy](view-financial-reports.md)

[Blog o finančním výkaznictví v Dynamics](http://blogs.msdn.com/b/dynamics_financial_reporting/)




