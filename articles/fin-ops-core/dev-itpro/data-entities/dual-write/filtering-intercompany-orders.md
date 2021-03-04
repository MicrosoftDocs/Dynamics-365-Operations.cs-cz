---
title: Filtrování mezipodnikových objednávek pro zabránění synchronizace objednávek a řádků objednávek
description: Toto téma popisuje, jakým způsobem pracuje filtrování mezipodnikových objednávek pro zabránění synchronizace objednávek a řádků objednávek.
author: negudava
manager: tfehr
ms.date: 11/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: negudava
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: 6c5e1e2467673badd20366d3bd8e1b93b8078b26
ms.sourcegitcommit: 0eb33909a419d526eb84b4e4b64d3595d01731ef
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/08/2020
ms.locfileid: "4701026"
---
# <a name="filter-intercompany-orders-to-avoid-synchronizing-orders-and-orderlines"></a>Filtrování mezipodnikových objednávek pro zabránění synchronizace objednávek a řádků objednávek

[!include [banner](../../includes/banner.md)]

Mezipodnikové objednávky lze filtrovat a zabránit tak provedení synchronizace entit **Objednávky** a **Řádky objednávek**. V některých scénářích nejsou podrobnosti mezipodnikové objednávky v aplikaci pro zapojení zákazníků nutné.

Každá standardní entita Common Data Service je rozšířena o odkazy na pole **Mezipodniková objednávka**, a mapy duálního zápisu jsou upraveny tak, aby odkazovaly na další pole ve filtrech. Důsledkem je fakt, že mezipodnikové objednávky již nejsou synchronizovány. Tento proces se vyhne vzniku zbytečných dat v aplikaci pro zapojení zákazníků.

1. Přidejte odkaz na pole **Mezipodniková objednávka** do **Záhlaví objednávky prodeje CDS**. Pole se vyplňuje pouze u mezipodnikových objednávek. Pole **Mezipodniková objednávka** je k dispozici v tabulce **SalesTable**.

    :::image type="content" source="media/filter-sales-order-header-field-display.png" alt-text="Mapovat fázování na cíl, SalesOrderHeader":::
    
2. Po rozšíření **Záhlaví objednávky prodeje CDS** je v mapování k dispozici pole **Mezipodniková objednávka**. Použijte filtr s řetězcem `INTERCOMPANYORDER == ""` ve funkci řetězce dotazu.

    :::image type="content" source="media/filter-sales-order-header.png" alt-text="Záhlaví prodejních objednávek, upravit dotaz":::

3. Přidejte odkaz na pole **IntercompanyInventTransId** do **Řádků prodejní objednávky CDS**.  Pole se vyplňuje pouze u mezipodnikových objednávek. Pole **InterCompanyInventTransID** je k dispozici v tabulce **SalesLine**.

    :::image type="content" source="media/filter-sales-order-line-field-display.png" alt-text="Mapovat fázování na cíl, SalesOrderLine":::

4. Po rozšíření **Řádků objednávky prodeje CDS** je v mapování k dispozici pole **IntercompanyInventTransId**. Použijte filtr s řetězcem `INTERCOMPANYINVENTTRANSID == ""` ve funkci řetězce dotazu.

    :::image type="content" source="media/filter-sales-order-lines.png" alt-text="Řádky prodejní objednávky, upravit dotaz":::

5. Rozšiřte položky **Záhlaví prodejní faktury V2** a **Řádky prodejní faktury V2** stejným způsobem, jakým jste rozšířili entity Common Data Service v krocích 1 a 2. Poté přidejte dotazy na filtr. Řetězec filtru pro **Záhlaví prodejní faktury V2** je `(INTERCOMPANYORDER == "") && (SALESORDERNUMBER != "")`. Řetězec filtru pro **Řádky prodejní faktury V2** je `INTERCOMPANYINVENTTRANSID == ""`.

    :::image type="content" source="media/filter-sales-invoice-header-field-display.png" alt-text="Mapovat fázování na cíl, záhlaví prodejní faktury":::

    :::image type="content" source="media/filter-sales-invoice-header-filter.png" alt-text="Záhlaví prodejních faktur, upravit dotaz":::

    :::image type="content" source="media/filter-sales-invoice-lines-filter.png" alt-text="Řádky prodejních faktur, upravit dotaz":::

6. Entita **Nabídky** nemá mezipodnikový vztah. Pokud někdo vytvoří nabídku pro jednoho z vašich mezipodnikových zákazníků, můžete všechny tyto zákazníky spojit do jedné skupiny zákazníků pomocí pole **CustGroup**.  Záhlaví a řádky lze rozšířit a přidat k nim pole **CustGroup** a poté filtrovat, aby tato skupina nebyla zahrnuta.

    :::image type="content" source="media/filter-cust-group.png" alt-text="Mapovat fázování na cíl, záhlaví prodejní nabídky":::

7. Poté, co rozšíříte entitu **Nabídka**, použijte filtr s řetězcem `CUSTGROUP !=  "<company>"` ve funkci řetězce dotazu.

    :::image type="content" source="media/filter-cust-group-edit.png" alt-text="Záhlaví prodejní nabídky, upravit dotaz":::


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]