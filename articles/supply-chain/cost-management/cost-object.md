---
title: "Nákladové objekty"
description: "Tento článek poskytuje informace o nákladových objektech a vysvětluje, jakým způsobem se kumulují náklady a množství. Nákladový objekt je entita, pro kterou se kumulují náklady a množství. Entita nákladového objektu může být produkt a varianty produktu, například varianty pro styl a barvu."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 19451
ms.assetid: ec776b98-813a-490d-848f-468452d98fac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 69eeb90387ca5765c163c7d482295ea104cc078c
ms.openlocfilehash: 2549ace837fcdfb9f927e6b486b6a94566bcbbd2
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---

# <a name="cost-objects"></a>Nákladové objekty

[!include[banner](../includes/banner.md)]


Tento článek poskytuje informace o nákladových objektech a vysvětluje, jakým způsobem se kumulují náklady a množství. Nákladový objekt je entita, pro kterou se kumulují náklady a množství. Entita nákladového objektu může být produkt a varianty produktu, například varianty pro styl a barvu.  

## <a name="cost-objects"></a>Nákladové objekty

Stránka **Nákladové objekty** obsahuje všechny nákladové objekty, které jsou registrovány v produktu. Nákladové objekty jsou definovány dle údajů z následujících zdrojů:

-   Produkt
-   Skupina dimenzí produktů
-   Skupina dimenze úložiště
-   Skupina sledovací dimenze

**Poznámka:** Nákladový objekt představuje nákladový prvek pouze typu **Přímý materiál**. Nákladový objekt a objektu zásob se liší způsobem, že nákladový objekt je definován podle dimenzí zásob, které jsou vybrány pro finanční zásoby. Například zboží má následující konfiguraci:

-   **Web:** Fyzické zásoby = Ano, Finanční zásoby = Ano
-   **Sklad:** Fyzické zásoby = Ano, Finanční zásoby = Ne
-   **Č. dávky:** Fyzické zásoby = Ano, Finanční zásoby = Ne

Následující tabulka zobrazuje, co je nákladový objekt a co je objekt zásob.

| Typ objektu      | Číslo zboží | Lokalita | Sklad | Č. dávky |
|------------------|-------------|------|-----------|-----------|
| Nákladový objekt      |  linka           |  linka    |           |           |
| Objekt zásob |  linka           |  linka    |   linka        |  linka         |

## <a name="accumulation-of-costs-and-quantities"></a>Kumulace nákladů a množství
-   Hodnota v poli **Hodnota** je součet následujících hodnot:
    -   Fyzická částka nákladů
    -   Částka finančních nákladů
    -   Množství úprav
-   Hodnota v poli **Množství** je součet následujících hodnot:
    -   Přijato
    -   Odečteno
    -   Zaúčtované mn.
-   Pole **Průměrné náklady na jednotku** je vypočítané. Hodnota se vypočítá jako podíl hodnoty pole **Hodnota** a hodnoty pole **Množství**.

**Poznámka:** Parametr **Zahrnovat fyzickou hodnotu **nemá žádný vliv na předchozí výpočty.

<a name="see-also"></a>Viz také
--------

[Skupina dimenzí produktů](https://technet.microsoft.com/en-us/library/aa499382.aspx)

[Skupina dimenze úložiště](https://technet.microsoft.com/en-us/library/hh209317.aspx)

[Skupina sledovací dimenze](https://technet.microsoft.com/en-us/library/hh209465.aspx)

[Co je nového a co se změnilo](../../fin-and-ops/get-started/whats-new-changed.md)

[Položky nákladů](cost-entries.md)




