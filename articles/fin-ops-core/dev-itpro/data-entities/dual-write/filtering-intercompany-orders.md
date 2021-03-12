---
title: Filtrování mezipodnikových objednávek pro zabránění synchronizace objednávek a řádků objednávek
description: Toto téma vysvětluje, jak filtrovat mezipodnikové objednávky tak, aby se entity Orders a OrderLines nesynchronizovaly.
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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: negudava
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: 342db8c1b4337145bfd61f5698ff6de25434a400
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/19/2020
ms.locfileid: "4796599"
---
# <a name="filter-intercompany-orders-to-avoid-syncing-orders-and-orderlines"></a><span data-ttu-id="3cf0e-103">Filtrování mezipodnikových objednávek pro zabránění synchronizace objednávek a řádků objednávek</span><span class="sxs-lookup"><span data-stu-id="3cf0e-103">Filter intercompany orders to avoid syncing Orders and OrderLines</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3cf0e-104">Mezipodnikové objednávky lze filtrovat a zabránit tak provedení synchronizace entit **Orders** a **OrderLines**.</span><span class="sxs-lookup"><span data-stu-id="3cf0e-104">You can filter intercompany orders so that the **Orders** and **OrderLines** tables aren't synced.</span></span> <span data-ttu-id="3cf0e-105">V některých scénářích nejsou podrobnosti mezipodnikové objednávky v aplikaci pro zapojení zákazníků požadovány.</span><span class="sxs-lookup"><span data-stu-id="3cf0e-105">In some scenarios, the intercompany order details aren't required in a customer engagement app.</span></span>

<span data-ttu-id="3cf0e-106">Každá standardní tabulka Dataverse je rozšířena o odkazy na sloupec **Mezipodniková objednávka**, a mapy duálního zápisu jsou upraveny tak, aby odkazovaly na další sloupce ve filtrech.</span><span class="sxs-lookup"><span data-stu-id="3cf0e-106">Each standard Dataverse table is extended through references to the **IntercompanyOrder** column, and the dual-write maps are modified so that they refer to the additional columns in the filters.</span></span> <span data-ttu-id="3cf0e-107">Mezipodnikové objednávky se proto již nesynchronizují.</span><span class="sxs-lookup"><span data-stu-id="3cf0e-107">Therefore, the intercompany orders are no longer synced.</span></span> <span data-ttu-id="3cf0e-108">Tento proces pomáhá při prevenci vzniku zbytečných dat v aplikaci Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="3cf0e-108">This process helps prevent unnecessary data in the customer engagement app.</span></span>

1. <span data-ttu-id="3cf0e-109">Prodlužte tabulku **Záhlaví objednávky prodeje CDS** přidáním odkazu na sloupec **Mezipodniková objednávka**.</span><span class="sxs-lookup"><span data-stu-id="3cf0e-109">Extend the **CDS Sales Order Headers** table by adding a reference to the **IntercompanyOrder** column.</span></span> <span data-ttu-id="3cf0e-110">Tento sloupec se vyplňuje pouze u mezipodnikových objednávek.</span><span class="sxs-lookup"><span data-stu-id="3cf0e-110">This column is filled in only on intercompany orders.</span></span> <span data-ttu-id="3cf0e-111">Sloupec **Mezipodniková objednávka** je k dispozici v tabulce **SalesTable**.</span><span class="sxs-lookup"><span data-stu-id="3cf0e-111">The **IntercompanyOrder** column is available in the **SalesTable** table.</span></span>

    :::image type="content" source="media/filter-sales-order-header-field-display.png" alt-text="Namapujte fázování na cílovou stránku pro záhlaví prodejní objednávky CDS":::

2. <span data-ttu-id="3cf0e-113">Po rozšíření **Záhlaví objednávky prodeje CDS** je v mapování k dispozici sloupec **Mezipodniková objednávka**.</span><span class="sxs-lookup"><span data-stu-id="3cf0e-113">After **CDS Sales Order Headers** is extended, the **IntercompanyOrder** column is available in the mapping.</span></span> <span data-ttu-id="3cf0e-114">Použijte filtr s řetězcem `INTERCOMPANYORDER == ""` ve funkci řetězce dotazu.</span><span class="sxs-lookup"><span data-stu-id="3cf0e-114">Apply a filter that has `INTERCOMPANYORDER == ""` as the query string.</span></span>

    :::image type="content" source="media/filter-sales-order-header.png" alt-text="Dialogové okno Upravit dotaz pro záhlaví prodejní objednávky CDS":::

3. <span data-ttu-id="3cf0e-116">Prodlužte tabulku **řádky objednávky prodeje CDS** přidáním odkazu na sloupec **IntercompanyInventTransId**.</span><span class="sxs-lookup"><span data-stu-id="3cf0e-116">Extend the **CDS Sales Order Lines** table by adding a reference to the **IntercompanyInventTransId** column.</span></span> <span data-ttu-id="3cf0e-117">Tento sloupec se vyplňuje pouze u mezipodnikových objednávek.</span><span class="sxs-lookup"><span data-stu-id="3cf0e-117">This column is filled in only on intercompany orders.</span></span> <span data-ttu-id="3cf0e-118">Sloupec **InterCompanyInventTransId** je k dispozici v tabulce **SalesLine**.</span><span class="sxs-lookup"><span data-stu-id="3cf0e-118">The **InterCompanyInventTransId** column is available in the **SalesLine** table.</span></span>

    :::image type="content" source="media/filter-sales-order-line-field-display.png" alt-text="Namapujte fázování na cílovou stránku pro řádky prodejní objednávky CDS":::

4. <span data-ttu-id="3cf0e-120">Po rozšíření **Řádků objednávky prodeje CDS** je v mapování k dispozici sloupec **IntercompanyInventTransId**.</span><span class="sxs-lookup"><span data-stu-id="3cf0e-120">After **CDS Sales Order Lines** is extended, the **IntercompanyInventTransId** column is available in the mapping.</span></span> <span data-ttu-id="3cf0e-121">Použijte filtr s řetězcem `INTERCOMPANYINVENTTRANSID == ""` ve funkci řetězce dotazu.</span><span class="sxs-lookup"><span data-stu-id="3cf0e-121">Apply a filter that has `INTERCOMPANYINVENTTRANSID == ""` as the query string.</span></span>

    :::image type="content" source="media/filter-sales-order-lines.png" alt-text="Dialogové okno Upravit dotaz pro řádky prodejní objednávky CDS":::

5. <span data-ttu-id="3cf0e-123">Opakujte kroky 1 a 2 pro rozšíření tabulky **Záhlaví prodejní faktury V2** a přidejte dotaz na filtr.</span><span class="sxs-lookup"><span data-stu-id="3cf0e-123">Repeat steps 1 and 2 to extend the **Sales Invoice Header V2** table and add a filter query.</span></span> <span data-ttu-id="3cf0e-124">V tomto případě použijte `(INTERCOMPANYORDER == "") && (SALESORDERNUMBER != "")` jako řetězec dotazu pro filtr.</span><span class="sxs-lookup"><span data-stu-id="3cf0e-124">In this case, use `(INTERCOMPANYORDER == "") && (SALESORDERNUMBER != "")` as the query string for the filter.</span></span>

    :::image type="content" source="media/filter-sales-invoice-header-field-display.png" alt-text="Namapujte fázování na cílovou stránku pro záhlaví prodejní faktury V2":::

    :::image type="content" source="media/filter-sales-invoice-header-filter.png" alt-text="Dialogové okno Upravit dotaz pro záhlaví prodejní objednávky V2":::

6. <span data-ttu-id="3cf0e-127">Opakujte kroky 3 a 4 pro rozšíření tabulky **Řádky prodejní faktury V2** a přidejte dotaz na filtr.</span><span class="sxs-lookup"><span data-stu-id="3cf0e-127">Repeat steps 3 and 4 to extend the **Sales Invoice Lines V2** table and add a filter query.</span></span> <span data-ttu-id="3cf0e-128">V tomto případě použijte `INTERCOMPANYINVENTTRANSID == ""` jako řetězec dotazu pro filtr.</span><span class="sxs-lookup"><span data-stu-id="3cf0e-128">In this case, use `INTERCOMPANYINVENTTRANSID == ""` as the query string for the filter.</span></span>

    :::image type="content" source="media/filter-sales-invoice-lines-filter.png" alt-text="Dialogové okno Upravit dotaz pro řádky prodejní objednávky V2":::

7. <span data-ttu-id="3cf0e-130">Tabulka **Nabídky** nemá mezipodnikový vztah.</span><span class="sxs-lookup"><span data-stu-id="3cf0e-130">The **Quotations** table doesn't have an intercompany relationship.</span></span> <span data-ttu-id="3cf0e-131">Pokud někdo vytvoří nabídku pro jednoho z vašich mezipodnikových zákazníků, můžete všechny tyto zákazníky spojit do jedné skupiny zákazníků pomocí sloupce **CustGroup**.</span><span class="sxs-lookup"><span data-stu-id="3cf0e-131">If someone creates a quotation for one of your intercompany customers, you can use the **CustGroup** column to put all those customers into one customer group.</span></span> <span data-ttu-id="3cf0e-132">Záhlaví a řádky můžete rozšířit přidáním sloupce **CustGroup** a poté filtrujte, aby skupina nebyla zahrnuta.</span><span class="sxs-lookup"><span data-stu-id="3cf0e-132">You can extend the header and lines by adding the **CustGroup** column, and then filter so that the group isn't included.</span></span>

    :::image type="content" source="media/filter-cust-group.png" alt-text="Mapování fázování na cílovou stránku pro záhlaví prodejní nabídky CDS":::

8. <span data-ttu-id="3cf0e-134">Poté, co rozšíříte entitu **Nabídky**, použijte filtr s řetězcem `CUSTGROUP != "<company>"` ve funkci řetězce dotazu.</span><span class="sxs-lookup"><span data-stu-id="3cf0e-134">After **Quotations** is extended, apply a filter that has `CUSTGROUP != "<company>"` as the query string.</span></span>

    :::image type="content" source="media/filter-cust-group-edit.png" alt-text="Dialogové okno Upravit dotaz pro záhlaví prodejní nabídky CDS":::
