---
title: Nákladové objekty
description: Tento článek poskytuje informace o nákladových objektech a vysvětluje, jakým způsobem se kumulují náklady a množství. Nákladový objekt je entita, pro kterou se kumulují náklady a množství. Entita nákladového objektu může být produkt a varianty produktu, například varianty pro styl a barvu.
author: JennySong-SH
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19451
ms.assetid: ec776b98-813a-490d-848f-468452d98fac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 93220208384ccb1a3cc8ff43d83577293e1f029e
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/03/2022
ms.locfileid: "8672451"
---
# <a name="cost-objects"></a>Nákladové objekty

[!include [banner](../includes/banner.md)]

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

**Poznámka:** Parametr **Zahrnovat fyzickou hodnotu** nemá žádný vliv na předchozí výpočty.

## <a name="additional-resources"></a>Další zdroje

[Skupina dimenzí produktů](/dynamicsax-2012/appuser-itpro/about-product-dimensions)

[Skupina dimenze úložiště](/dynamicsax-2012//storage-dimension-groups-form)

[Skupina sledovací dimenze](/dynamicsax-2012//tracking-dimension-groups-form)

[Co je nového a co se změnilo](../../fin-ops-core/fin-ops/get-started/whats-new-changed.md)

[Položky nákladů](cost-entries.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]