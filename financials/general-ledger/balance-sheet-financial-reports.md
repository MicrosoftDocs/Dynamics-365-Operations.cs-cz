---
title: "Finanční sestavy rozvah"
description: "Tento článek popisuje výchozích sestav rozvahy. Popisuje také stavební bloky, které jsou přidruženy k tyto zprávy."
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
ms.custom: 12274
ms.assetid: 52f78229-f531-4d16-b337-e2628994acb6
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 664d32c2bfecb50e24fd48a66ab5b34cef6c09a3
ms.lasthandoff: 03/31/2017


---

# <a name="balance-sheet-financial-reports"></a>Finanční sestavy rozvah

[!include[banner](../includes/banner.md)]


Tento článek popisuje výchozích sestav rozvahy. Popisuje také stavební bloky, které jsou přidruženy k tyto zprávy. 

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

[Financial reporting](financial-reporting-getting-started.md)

[View financial reports](view-financial-reports.md)

[Finanční vykazování blogu Dynamics](http://blogs.msdn.com/b/dynamics_financial_reporting/)




