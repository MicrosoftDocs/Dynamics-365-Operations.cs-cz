---
title: Finanční sestavy rozvah
description: Tento článek popisuje výchozí sestavy pro rozvahy. Popisuje také stavební bloky, které jsou přidruženy k těmto sestavám.
author: jcart1106
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FinanicalReports
audience: Application User
ms.reviewer: roschlom
ms.custom: 12274
ms.assetid: 52f78229-f531-4d16-b337-e2628994acb6
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 64e3624b387820bea3bfea9c2a4b2f48b0aa9822
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/04/2021
ms.locfileid: "6189014"
---
# <a name="balance-sheet-financial-reports"></a>Finanční sestavy rozvah

[!include [banner](../includes/banner.md)]

Tento článek popisuje výchozí sestavy pro rozvahy. Popisuje také stavební bloky, které jsou přidruženy k těmto sestavám. 

## <a name="default-balance-sheet-reports"></a>Výchozí finanční sestavy rozvah

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



## <a name="additional-resources"></a>Další zdroje

[Přehled finančního výkaznictví](financial-reporting-getting-started.md)

[Zobrazení finančních sestav](view-financial-reports.md)

[Blog o finančním výkaznictví v Dynamics](https://blogs.msdn.com/b/dynamics_financial_reporting/)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]