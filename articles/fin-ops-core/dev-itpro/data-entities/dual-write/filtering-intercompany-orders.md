---
title: Filtrování mezipodnikových objednávek pro zabránění synchronizace objednávek a řádků objednávek
description: Tento článek vysvětluje, jak filtrovat mezipodnikové objednávky tak, aby se entity Orders a OrderLines nesynchronizovaly.
author: negudava
ms.date: 11/09/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: negudava
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 47d5cc358165d9a870892e0d026948d65343e5f7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8910344"
---
# <a name="filter-intercompany-orders-to-avoid-syncing-orders-and-orderlines"></a>Filtrování mezipodnikových objednávek pro zabránění synchronizace objednávek a řádků objednávek

[!include [banner](../../includes/banner.md)]

Mezipodnikové objednávky lze filtrovat a zabránit tak provedení synchronizace entit **Orders** a **OrderLines**. V některých scénářích nejsou podrobnosti mezipodnikové objednávky v aplikaci pro zapojení zákazníků požadovány.

Každá standardní tabulka Dataverse je rozšířena o odkazy na sloupec **Mezipodniková objednávka**, a mapy duálního zápisu jsou upraveny tak, aby odkazovaly na další sloupce ve filtrech. Mezipodnikové objednávky se proto již nesynchronizují. Tento proces pomáhá při prevenci vzniku zbytečných dat v aplikaci Customer Engagement.

1. Prodlužte tabulku **Záhlaví objednávky prodeje CDS** přidáním odkazu na sloupec **Mezipodniková objednávka**. Tento sloupec se vyplňuje pouze u mezipodnikových objednávek. Sloupec **Mezipodniková objednávka** je k dispozici v tabulce **SalesTable**.

    :::image type="content" source="media/filter-sales-order-header-field-display.png" alt-text="Namapujte fázování na cílovou stránku pro záhlaví prodejní objednávky CDS.":::

2. Po rozšíření **Záhlaví objednávky prodeje CDS** je v mapování k dispozici sloupec **Mezipodniková objednávka**. Použijte filtr s řetězcem `INTERCOMPANYORDER == ""` ve funkci řetězce dotazu.

    :::image type="content" source="media/filter-sales-order-header.png" alt-text="Dialogové okno Upravit dotaz pro záhlaví prodejní objednávky CDS.":::

3. Prodlužte tabulku **řádky objednávky prodeje CDS** přidáním odkazu na sloupec **IntercompanyInventTransId**. Tento sloupec se vyplňuje pouze u mezipodnikových objednávek. Sloupec **InterCompanyInventTransId** je k dispozici v tabulce **SalesLine**.

    :::image type="content" source="media/filter-sales-order-line-field-display.png" alt-text="Namapujte fázování na cílovou stránku pro řádky prodejní objednávky CDS.":::

4. Po rozšíření **Řádků objednávky prodeje CDS** je v mapování k dispozici sloupec **IntercompanyInventTransId**. Použijte filtr s řetězcem `INTERCOMPANYINVENTTRANSID == ""` ve funkci řetězce dotazu.

    :::image type="content" source="media/filter-sales-order-lines.png" alt-text="Dialogové okno Upravit dotaz pro řádky prodejní objednávky CDS.":::

5. Opakujte kroky 1 a 2 pro rozšíření tabulky **Záhlaví prodejní faktury V2** a přidejte dotaz na filtr. V tomto případě použijte `(INTERCOMPANYORDER == "") && (SALESORDERNUMBER != "")` jako řetězec dotazu pro filtr.

    :::image type="content" source="media/filter-sales-invoice-header-field-display.png" alt-text="Namapujte fázování na cílovou stránku pro záhlaví prodejní faktury V2.":::

    :::image type="content" source="media/filter-sales-invoice-header-filter.png" alt-text="Dialogové okno Upravit dotaz pro záhlaví prodejní objednávky V2.":::

6. Opakujte kroky 3 a 4 pro rozšíření tabulky **Řádky prodejní faktury V2** a přidejte dotaz na filtr. V tomto případě použijte `INTERCOMPANYINVENTTRANSID == ""` jako řetězec dotazu pro filtr.

    :::image type="content" source="media/filter-sales-invoice-lines-filter.png" alt-text="Dialogové okno Upravit dotaz pro řádky prodejní objednávky V2.":::

7. Tabulka **Nabídky** nemá mezipodnikový vztah. Pokud někdo vytvoří nabídku pro jednoho z vašich mezipodnikových zákazníků, můžete všechny tyto zákazníky spojit do jedné skupiny zákazníků pomocí sloupce **CustGroup**. Záhlaví a řádky můžete rozšířit přidáním sloupce **CustGroup** a poté filtrujte, aby skupina nebyla zahrnuta.

    :::image type="content" source="media/filter-cust-group.png" alt-text="Mapování fázování na cílovou stránku pro záhlaví prodejní nabídky CDS.":::

8. Poté, co rozšíříte entitu **Nabídky**, použijte filtr s řetězcem `CUSTGROUP != "<company>"` ve funkci řetězce dotazu.

    :::image type="content" source="media/filter-cust-group-edit.png" alt-text="Dialogové okno Upravit dotaz pro záhlaví prodejní nabídky CDS.":::


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]