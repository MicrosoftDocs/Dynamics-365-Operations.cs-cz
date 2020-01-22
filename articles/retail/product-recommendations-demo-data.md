---
title: Ukázková data doporučení produktu pro omnikanál
description: Cílem tohoto dokumentu je poskytnou pokyny, jak využívat doporučení Omni kanálu v prostředích s jedním polem na úrovni 1, pomocí předem naplněných a přizpůsobitelných ukázkových dat.
author: bebeale
manager: AnnBe
ms.date: 12/1/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-07-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 31aa5dbd2fa814fd572024a4ae36b9d9b46a2fb0
ms.sourcegitcommit: 398c0652acde12c953de007d06055456d6e0a516
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/02/2019
ms.locfileid: "2872319"
---
# <a name="omni-channel-product-recommendations-demo-data"></a><span data-ttu-id="c6e8f-103">Ukázková data doporučení produktu pro omnikanál</span><span class="sxs-lookup"><span data-stu-id="c6e8f-103">Omni-channel product recommendations demo data</span></span>

<span data-ttu-id="c6e8f-104">Cílem tohoto dokumentu je poskytnou pokyny, jak využívat doporučení Omni kanálu v prostředích s jedním polem na úrovni 1, pomocí předem naplněných a přizpůsobitelných ukázkových dat.</span><span class="sxs-lookup"><span data-stu-id="c6e8f-104">This document aims to provide guidance on how to leverage omni-channel product recommendations in Tier-1 single box environments using pre-populated, customizable demo data.</span></span>

<span data-ttu-id="c6e8f-105">Doporučení omnikanálového produktu poskytuje sadu redakčně upravených nebo programově generovaných uspořádaných seznamů produktů.</span><span class="sxs-lookup"><span data-stu-id="c6e8f-105">Omni-channel product recommendations provide a set of editorially curated or programmatically generated ordered list of products.</span></span> <span data-ttu-id="c6e8f-106">Tyto seznamy lze použít v několika situacích, v závislosti na obchodní potřebě.</span><span class="sxs-lookup"><span data-stu-id="c6e8f-106">These lists can be used in several scenarios, depending on the business need.</span></span> <span data-ttu-id="c6e8f-107">Další informace o seznamech doporučených produktů naleznete v tématu [Přehled doporučení produktu.](../commerce/product-recommendations.md)</span><span class="sxs-lookup"><span data-stu-id="c6e8f-107">For more information about product recommendation lists, see [Product recommendations overview.](../commerce/product-recommendations.md)</span></span>

<span data-ttu-id="c6e8f-108">Pro prostředí s vrstvami 2 a vyššími Dynamics jsou doporučení produktu automaticky vypočítána na základě zákaznických dat.</span><span class="sxs-lookup"><span data-stu-id="c6e8f-108">For Tier-2 and higher Dynamics Environments product recommendations are automatically computed based on customer data.</span></span>
<span data-ttu-id="c6e8f-109">Použití ukázkových dat doporučení produktu nezakáže žádné řešení doporučení produktů, které již bylo v daném prostředí zřízeno a žádné náklady související s jeho použitím.</span><span class="sxs-lookup"><span data-stu-id="c6e8f-109">Using product recommendations demo data does not disable any product recommendations solution already provisioned in the environment and any costs associated with its usage.</span></span>

<span data-ttu-id="c6e8f-110">Doporučení produktu na úrovni 1 jsou založena pouze mimo statická ukázková data uložená v souboru CSV.</span><span class="sxs-lookup"><span data-stu-id="c6e8f-110">For Tier-1 environments product recommendations are based only off the static demo data stored in a csv file.</span></span>

## <a name="enabling-product-recommendations-demo-data-in-an-environment"></a><span data-ttu-id="c6e8f-111">Povolení ukázkových dat doporučení produktu v prostředí</span><span class="sxs-lookup"><span data-stu-id="c6e8f-111">Enabling product recommendations demo data in an environment</span></span>

<span data-ttu-id="c6e8f-112">Je nutné, aby zákazníci nasadili **Náhled rozšíření ukázky Dynamics 365 Commerce** do příslušného prostředí, které automaticky povolí ukázková data doporučení produktu.</span><span class="sxs-lookup"><span data-stu-id="c6e8f-112">Customers need to deploy the **Dynamics 365 Commerce Preview Demo Extension** to the respective environment, which automatically enables product recommendations demo data.</span></span>

## <a name="default-demo-data"></a><span data-ttu-id="c6e8f-113">Výchozí ukázková data</span><span class="sxs-lookup"><span data-stu-id="c6e8f-113">Default demo data</span></span>
<span data-ttu-id="c6e8f-114">Každé prostředí typu OneBox se dodává s předem nahranými ukázkovými daty doporučení produktu uloženými v souboru **reco_demo_data. csv** odděleném čárkami ve stejné složce jako tento dokument na serveru Retail.</span><span class="sxs-lookup"><span data-stu-id="c6e8f-114">Each Onebox type environment comes with a preloaded set of product recommendations demo data stored in the coma separated **‘reco_demo_data.csv’** file, located in the same folder as this document on Retail Server.</span></span>

<span data-ttu-id="c6e8f-115">Tyto údaje jsou uspořádány do následujících sloupců</span><span class="sxs-lookup"><span data-stu-id="c6e8f-115">This data is structured along the following columns</span></span>

| <span data-ttu-id="c6e8f-116">Název sloupce</span><span class="sxs-lookup"><span data-stu-id="c6e8f-116">Column name</span></span>         | <span data-ttu-id="c6e8f-117">Povinné</span><span class="sxs-lookup"><span data-stu-id="c6e8f-117">Mandatory</span></span>          | <span data-ttu-id="c6e8f-118">Popis</span><span class="sxs-lookup"><span data-stu-id="c6e8f-118">Description</span></span>                                                                                                                                 | <span data-ttu-id="c6e8f-119">Možné hodnoty</span><span class="sxs-lookup"><span data-stu-id="c6e8f-119">Possible Values</span></span>                                                              |
|---------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="c6e8f-120">RecoList</span><span class="sxs-lookup"><span data-stu-id="c6e8f-120">RecoList</span></span>            | :heavy_check_mark: | <span data-ttu-id="c6e8f-122">Konkrétní typ seznamu doporučení produktu, který má ukázkový datový bod generovat.</span><span class="sxs-lookup"><span data-stu-id="c6e8f-122">The specific product   recommendation list type that the demo data point is to generate.</span></span>                                                    | <ul><li><span data-ttu-id="c6e8f-123">RecoBestSelling</span><span class="sxs-lookup"><span data-stu-id="c6e8f-123">RecoBestSelling</span></span></li><li><span data-ttu-id="c6e8f-124">RecoNew</span><span class="sxs-lookup"><span data-stu-id="c6e8f-124">RecoNew</span></span></li><li><span data-ttu-id="c6e8f-125">RecoTrending</span><span class="sxs-lookup"><span data-stu-id="c6e8f-125">RecoTrending</span></span></li><li><span data-ttu-id="c6e8f-126">RecoCart</span><span class="sxs-lookup"><span data-stu-id="c6e8f-126">RecoCart</span></span></li><li><span data-ttu-id="c6e8f-127">RecoPeopleAlsoBuy</span><span class="sxs-lookup"><span data-stu-id="c6e8f-127">RecoPeopleAlsoBuy</span></span></li></ul> |
| <span data-ttu-id="c6e8f-128">OperatingUnitNumber</span><span class="sxs-lookup"><span data-stu-id="c6e8f-128">OperatingUnitNumber</span></span> | :heavy_check_mark: | <span data-ttu-id="c6e8f-130">Specifické číslo provozní jednotky, na které se očekává, že se budou nacházet doporučení produktů.</span><span class="sxs-lookup"><span data-stu-id="c6e8f-130">The specific   operating unit number where product recommendations are expected to be   surfaced in.</span></span>                                        |                                                                              |
| <span data-ttu-id="c6e8f-131">Kategorie</span><span class="sxs-lookup"><span data-stu-id="c6e8f-131">Category</span></span>            |                    |    <span data-ttu-id="c6e8f-132">Kategorii, pro kterou má být konkrétní seznam vrácen.</span><span class="sxs-lookup"><span data-stu-id="c6e8f-132">The category the   specific list should be returned for.</span></span> <span data-ttu-id="c6e8f-133">Není-li zadána žádná kategorie, je seznam určen pouze k hornímu okraji hierarchie navigace.</span><span class="sxs-lookup"><span data-stu-id="c6e8f-133">If no category is specified, list is   for top of navigation hierarchy only.</span></span>    |                                                                              |
| <span data-ttu-id="c6e8f-134">SeedItemId</span><span class="sxs-lookup"><span data-stu-id="c6e8f-134">SeedItemId</span></span>          |                    |    <span data-ttu-id="c6e8f-135">Pro seznamy, které vyžadují zdroje (RecoPeopleAlsoBuy a RecoCart), by produkt měl obsahovat další produkty.</span><span class="sxs-lookup"><span data-stu-id="c6e8f-135">For lists that   require seed (RecoPeopleAlsoBuy and RecoCart) the product those lists should   show additional products for.</span></span>            |                                                                              |
| <span data-ttu-id="c6e8f-136">ItemIds</span><span class="sxs-lookup"><span data-stu-id="c6e8f-136">ItemIds</span></span>             | :heavy_check_mark: | <span data-ttu-id="c6e8f-138">Jeden nebo více produktů, které mají být vráceny jako výsledek, oddělené znakem **;**.</span><span class="sxs-lookup"><span data-stu-id="c6e8f-138">One or more products   to be returned as the result, separated by **‘;’**.</span></span>                                                                  |                                                                              |


## <a name="customize-demo-data"></a><span data-ttu-id="c6e8f-139">Přizpůsobení ukázkových dat</span><span class="sxs-lookup"><span data-stu-id="c6e8f-139">Customize demo data</span></span>
<span data-ttu-id="c6e8f-140">Zákazníci mohou upravovat výchozí ukázková data s libovolnými informacemi o produktech a kategoriích konfigurovaných v HQ.</span><span class="sxs-lookup"><span data-stu-id="c6e8f-140">Customers can edit the default demo data with any product and category information that is configured in HQ.</span></span> <span data-ttu-id="c6e8f-141">Jakmile je CSV aktualizován, budou doporučení produktu vrácená odběratelům okamžitě zohledněna.</span><span class="sxs-lookup"><span data-stu-id="c6e8f-141">Once the CSV is updated, the Product Recommendations returned to customers will immediately reflect the changes.</span></span>

<span data-ttu-id="c6e8f-142">Přípona obsahuje datový objekt s názvem RecoMockDataset.csv, který umožňuje odběrateli ovládat datovou sadu používanou k napájení výsledků těchto doporučení.</span><span class="sxs-lookup"><span data-stu-id="c6e8f-142">The extension contains a datafile called RecoMockDataset.csv which allows the customer to control the dataset used to power the mock recommendations results.</span></span> <span data-ttu-id="c6e8f-143">Název souboru lze řídit pomocí konfigurace rozšíření pomocí nastavení **ext.Recommendations.DemoFilePath**.</span><span class="sxs-lookup"><span data-stu-id="c6e8f-143">The file name can be controlled through extension configuration using the **ext.Recommendations.DemoFilePath** setting.</span></span> <span data-ttu-id="c6e8f-144">Díky tomu mohou mít zákazníci k dispozici více datových sad, které lze snadno přepínat mezi konfigurací.</span><span class="sxs-lookup"><span data-stu-id="c6e8f-144">This enables the customers to have multiple datasets available that can be switched between easily through configuration.</span></span>

```
  <settings>
    <add name="ext.Recommendations.DemoFilePath" value="RecoMockDataset.csv" />
  </settings>
```

## <a name="additional-resources"></a><span data-ttu-id="c6e8f-145">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="c6e8f-145">Additional resources</span></span>

[<span data-ttu-id="c6e8f-146">Přehled doporučení produktu</span><span class="sxs-lookup"><span data-stu-id="c6e8f-146">Product recommendations overview</span></span>](../commerce/product-recommendations.md)

[<span data-ttu-id="c6e8f-147">Plánování prostředí</span><span class="sxs-lookup"><span data-stu-id="c6e8f-147">Environment planning</span></span>](../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md)
