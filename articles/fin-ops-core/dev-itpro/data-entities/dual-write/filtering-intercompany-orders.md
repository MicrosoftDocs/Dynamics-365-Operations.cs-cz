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
# <a name="filter-intercompany-orders-to-avoid-synchronizing-orders-and-orderlines"></a><span data-ttu-id="e1d54-103">Filtrování mezipodnikových objednávek pro zabránění synchronizace objednávek a řádků objednávek</span><span class="sxs-lookup"><span data-stu-id="e1d54-103">Filter intercompany orders to avoid synchronizing Orders and OrderLines</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e1d54-104">Mezipodnikové objednávky lze filtrovat a zabránit tak provedení synchronizace entit **Objednávky** a **Řádky objednávek**.</span><span class="sxs-lookup"><span data-stu-id="e1d54-104">You can filter intercompany orders to avoid synchronizing the **Orders** and **OrderLines** entities.</span></span> <span data-ttu-id="e1d54-105">V některých scénářích nejsou podrobnosti mezipodnikové objednávky v aplikaci pro zapojení zákazníků nutné.</span><span class="sxs-lookup"><span data-stu-id="e1d54-105">In some scenarios, the intercompany order details are not necessary in customer engagement app.</span></span>

<span data-ttu-id="e1d54-106">Každá standardní entita Common Data Service je rozšířena o odkazy na pole **Mezipodniková objednávka**, a mapy duálního zápisu jsou upraveny tak, aby odkazovaly na další pole ve filtrech.</span><span class="sxs-lookup"><span data-stu-id="e1d54-106">Each of the standard Common Data Service entities is extended with references to the **IntercompanyOrder** field, and the dual-write maps are modified to refer to the additional fields in the filters.</span></span> <span data-ttu-id="e1d54-107">Důsledkem je fakt, že mezipodnikové objednávky již nejsou synchronizovány.</span><span class="sxs-lookup"><span data-stu-id="e1d54-107">The result is that the intercompany orders are no longer synchronized.</span></span> <span data-ttu-id="e1d54-108">Tento proces se vyhne vzniku zbytečných dat v aplikaci pro zapojení zákazníků.</span><span class="sxs-lookup"><span data-stu-id="e1d54-108">This process avoids unnecessary data in the customer engagement app.</span></span>

1. <span data-ttu-id="e1d54-109">Přidejte odkaz na pole **Mezipodniková objednávka** do **Záhlaví objednávky prodeje CDS**.</span><span class="sxs-lookup"><span data-stu-id="e1d54-109">Add a reference to **IntercompanyOrder** to **CDS Sales Order Headers**.</span></span> <span data-ttu-id="e1d54-110">Pole se vyplňuje pouze u mezipodnikových objednávek.</span><span class="sxs-lookup"><span data-stu-id="e1d54-110">It is populated on only intercompany orders.</span></span> <span data-ttu-id="e1d54-111">Pole **Mezipodniková objednávka** je k dispozici v tabulce **SalesTable**.</span><span class="sxs-lookup"><span data-stu-id="e1d54-111">The field **IntercompanyOrder** is available in **SalesTable**.</span></span>

    :::image type="content" source="media/filter-sales-order-header-field-display.png" alt-text="Mapovat fázování na cíl, SalesOrderHeader":::
    
2. <span data-ttu-id="e1d54-113">Po rozšíření **Záhlaví objednávky prodeje CDS** je v mapování k dispozici pole **Mezipodniková objednávka**.</span><span class="sxs-lookup"><span data-stu-id="e1d54-113">After **CDS Sales Order Headers** is extended, the **IntercompanyOrder** field is available in the mapping.</span></span> <span data-ttu-id="e1d54-114">Použijte filtr s řetězcem `INTERCOMPANYORDER == ""` ve funkci řetězce dotazu.</span><span class="sxs-lookup"><span data-stu-id="e1d54-114">Apply a filter with `INTERCOMPANYORDER == ""` as the query string.</span></span>

    :::image type="content" source="media/filter-sales-order-header.png" alt-text="Záhlaví prodejních objednávek, upravit dotaz":::

3. <span data-ttu-id="e1d54-116">Přidejte odkaz na pole **IntercompanyInventTransId** do **Řádků prodejní objednávky CDS**.</span><span class="sxs-lookup"><span data-stu-id="e1d54-116">Add a reference to **IntercompanyInventTransId** to **CDS Sales Order Lines**.</span></span>  <span data-ttu-id="e1d54-117">Pole se vyplňuje pouze u mezipodnikových objednávek.</span><span class="sxs-lookup"><span data-stu-id="e1d54-117">It is populated on only intercompany orders.</span></span> <span data-ttu-id="e1d54-118">Pole **InterCompanyInventTransID** je k dispozici v tabulce **SalesLine**.</span><span class="sxs-lookup"><span data-stu-id="e1d54-118">The field **InterCompanyInventTransID** is available in **SalesLine**.</span></span>

    :::image type="content" source="media/filter-sales-order-line-field-display.png" alt-text="Mapovat fázování na cíl, SalesOrderLine":::

4. <span data-ttu-id="e1d54-120">Po rozšíření **Řádků objednávky prodeje CDS** je v mapování k dispozici pole **IntercompanyInventTransId**.</span><span class="sxs-lookup"><span data-stu-id="e1d54-120">After **CDS Sales Order Lines** is extended, the **IntercompanyInventTransId** field is available in the mapping.</span></span> <span data-ttu-id="e1d54-121">Použijte filtr s řetězcem `INTERCOMPANYINVENTTRANSID == ""` ve funkci řetězce dotazu.</span><span class="sxs-lookup"><span data-stu-id="e1d54-121">Apply a filter with `INTERCOMPANYINVENTTRANSID == ""` as the query string.</span></span>

    :::image type="content" source="media/filter-sales-order-lines.png" alt-text="Řádky prodejní objednávky, upravit dotaz":::

5. <span data-ttu-id="e1d54-123">Rozšiřte položky **Záhlaví prodejní faktury V2** a **Řádky prodejní faktury V2** stejným způsobem, jakým jste rozšířili entity Common Data Service v krocích 1 a 2.</span><span class="sxs-lookup"><span data-stu-id="e1d54-123">Extend **Sales Invoice Header V2** and **Sales Invoice Lines V2** in the same way you extended the Common Data Service entities in steps 1 and 2.</span></span> <span data-ttu-id="e1d54-124">Poté přidejte dotazy na filtr.</span><span class="sxs-lookup"><span data-stu-id="e1d54-124">Then add the filter queries.</span></span> <span data-ttu-id="e1d54-125">Řetězec filtru pro **Záhlaví prodejní faktury V2** je `(INTERCOMPANYORDER == "") && (SALESORDERNUMBER != "")`.</span><span class="sxs-lookup"><span data-stu-id="e1d54-125">The filter string for **Sales Invoice Header V2** is `(INTERCOMPANYORDER == "") && (SALESORDERNUMBER != "")`.</span></span> <span data-ttu-id="e1d54-126">Řetězec filtru pro **Řádky prodejní faktury V2** je `INTERCOMPANYINVENTTRANSID == ""`.</span><span class="sxs-lookup"><span data-stu-id="e1d54-126">The filter string for **Sales Invoice Lines V2** is `INTERCOMPANYINVENTTRANSID == ""`.</span></span>

    :::image type="content" source="media/filter-sales-invoice-header-field-display.png" alt-text="Mapovat fázování na cíl, záhlaví prodejní faktury":::

    :::image type="content" source="media/filter-sales-invoice-header-filter.png" alt-text="Záhlaví prodejních faktur, upravit dotaz":::

    :::image type="content" source="media/filter-sales-invoice-lines-filter.png" alt-text="Řádky prodejních faktur, upravit dotaz":::

6. <span data-ttu-id="e1d54-130">Entita **Nabídky** nemá mezipodnikový vztah.</span><span class="sxs-lookup"><span data-stu-id="e1d54-130">The **Quotations** entity doesn't have an intercompany relationship.</span></span> <span data-ttu-id="e1d54-131">Pokud někdo vytvoří nabídku pro jednoho z vašich mezipodnikových zákazníků, můžete všechny tyto zákazníky spojit do jedné skupiny zákazníků pomocí pole **CustGroup**.</span><span class="sxs-lookup"><span data-stu-id="e1d54-131">If someone creates a quote for one of your intercompany customers, you can put all of these customers in one customer group by using the **CustGroup** field.</span></span>  <span data-ttu-id="e1d54-132">Záhlaví a řádky lze rozšířit a přidat k nim pole **CustGroup** a poté filtrovat, aby tato skupina nebyla zahrnuta.</span><span class="sxs-lookup"><span data-stu-id="e1d54-132">Header and lines can be extended to add the **CustGroup** field and then filter to not include this group.</span></span>

    :::image type="content" source="media/filter-cust-group.png" alt-text="Mapovat fázování na cíl, záhlaví prodejní nabídky":::

7. <span data-ttu-id="e1d54-134">Poté, co rozšíříte entitu **Nabídka**, použijte filtr s řetězcem `CUSTGROUP !=  "<company>"` ve funkci řetězce dotazu.</span><span class="sxs-lookup"><span data-stu-id="e1d54-134">After you extent the **Quotations** entity, apply a filter with `CUSTGROUP !=  "<company>"` as the query string.</span></span>

    :::image type="content" source="media/filter-cust-group-edit.png" alt-text="Záhlaví prodejní nabídky, upravit dotaz":::
