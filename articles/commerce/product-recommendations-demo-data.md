---
title: Získání doporučení produktu pomocí ukázkových dat
description: Tento dokument poskytuje pokyny, jak využívat doporučení Omni kanálu v prostředích s jedním polem na úrovni 1, pomocí předem naplněných a přizpůsobitelných ukázkových dat.
author: bebeale
manager: AnnBe
ms.date: 10/01/19
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: RetailStoreTable, RetailTillLayout
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 1456feb0665b6ec79a36a3704f17da80ffd759a0
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042773"
---
# <a name="get-product-recommendations-using-demo-data"></a><span data-ttu-id="dcc00-103">Získání doporučení produktu pomocí ukázkových dat</span><span class="sxs-lookup"><span data-stu-id="dcc00-103">Get product recommendations using demo data</span></span>
<span data-ttu-id="dcc00-104">Tento dokument poskytuje pokyny, jak využívat doporučení Omni kanálu v prostředích s jedním polem na úrovni 1, pomocí předem naplněných a přizpůsobitelných ukázkových dat.</span><span class="sxs-lookup"><span data-stu-id="dcc00-104">This document provides guidance on how to leverage omni-channel product recommendations in Tier-1 single box environments using pre-populated, customizable demo data.</span></span>

<span data-ttu-id="dcc00-105">Doporučení omnikanálového produktu poskytuje sadu redakčně upravených nebo programově generovaných seznamů produktů.</span><span class="sxs-lookup"><span data-stu-id="dcc00-105">Omni-channel product recommendations provide a set of editorially curated or programmatically generated list of products.</span></span> <span data-ttu-id="dcc00-106">Tyto seznamy lze použít v několika situacích, v závislosti na obchodní potřebě.</span><span class="sxs-lookup"><span data-stu-id="dcc00-106">These lists can be used in several scenarios, depending on the business need.</span></span> <span data-ttu-id="dcc00-107">Další informace o seznamech doporučených produktů naleznete v tématu [Přehled doporučení produktu](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="dcc00-107">For more information about product recommendation lists, see [Product recommendations overview](product-recommendations.md).</span></span>

<span data-ttu-id="dcc00-108">Pro prostředí s vrstvami 2 a vyššími Dynamics 365 jsou doporučení produktu automaticky vypočítána na základě zákaznických dat.</span><span class="sxs-lookup"><span data-stu-id="dcc00-108">For Tier-2 and higher Dynamics 365 environments, product recommendations are automatically computed based on customer data.</span></span> <span data-ttu-id="dcc00-109">Použití ukázkových dat doporučení produktu nezakáže žádné řešení doporučení produktů, které již bylo v daném prostředí zřízeno a žádné náklady související s jeho použitím.</span><span class="sxs-lookup"><span data-stu-id="dcc00-109">Using product recommendations demo data does not disable any product recommendations solution already provisioned in the environment and any costs associated with its usage.</span></span>

<span data-ttu-id="dcc00-110">Doporučení produktu na úrovni 1 jsou založena pouze mimo statická ukázková data uložená v souboru .CSV.</span><span class="sxs-lookup"><span data-stu-id="dcc00-110">For Tier-1 environments, product recommendations are based only off the static demo data stored in a .csv file.</span></span>

## <a name="enabling-product-recommendations-demo-data-in-an-environment"></a><span data-ttu-id="dcc00-111">Povolení ukázkových dat doporučení produktu v prostředí</span><span class="sxs-lookup"><span data-stu-id="dcc00-111">Enabling product recommendations demo data in an environment</span></span>
<span data-ttu-id="dcc00-112">Chcete-li povolit ukázková data pro odoporučení produktu, musíte nasadit Náhled rozšíření ukázky Dynamics 365 Commerce do příslušného prostředí.</span><span class="sxs-lookup"><span data-stu-id="dcc00-112">To enable product recommensations demo date, you need to deploy the Dynamics 365 Commerce Preview Demo Extension to the respective environment.</span></span> <span data-ttu-id="dcc00-113">Tím se automaticky povolí ukázková data doporučení produktu.</span><span class="sxs-lookup"><span data-stu-id="dcc00-113">Doing so automatically enables product recommendations demo data.</span></span>

## <a name="default-demo-data"></a><span data-ttu-id="dcc00-114">Výchozí ukázková data</span><span class="sxs-lookup"><span data-stu-id="dcc00-114">Default demo data</span></span>
<span data-ttu-id="dcc00-115">Každé prostředí typu OneBox se dodává s předem nahranými ukázkovými daty doporučení produktu uloženými v souboru ‘reco_demo_data.csv’ odděleném čárkami v jednotce škálování aplikace Commerce.</span><span class="sxs-lookup"><span data-stu-id="dcc00-115">Each Onebox type environment comes with a preloaded set of product recommendations demo data stored in the coma separated ‘reco_demo_data.csv’ file, located on the Commerce Scale Unit.</span></span>

<span data-ttu-id="dcc00-116">Data jsou uspořádána do následujících sloupců.</span><span class="sxs-lookup"><span data-stu-id="dcc00-116">The data is structured along the following columns.</span></span>

| <span data-ttu-id="dcc00-117">Název sloupce</span><span class="sxs-lookup"><span data-stu-id="dcc00-117">Column name</span></span>         | <span data-ttu-id="dcc00-118">Povinné</span><span class="sxs-lookup"><span data-stu-id="dcc00-118">Mandatory</span></span>          | <span data-ttu-id="dcc00-119">Popis</span><span class="sxs-lookup"><span data-stu-id="dcc00-119">Description</span></span>                                                                                                                                 | <span data-ttu-id="dcc00-120">Možné hodnoty</span><span class="sxs-lookup"><span data-stu-id="dcc00-120">Possible Values</span></span>                                                              |
|---------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="dcc00-121">RecoList</span><span class="sxs-lookup"><span data-stu-id="dcc00-121">RecoList</span></span>            | :heavy_check_mark: | <span data-ttu-id="dcc00-123">Konkrétní typ seznamu doporučení produktu, který má ukázkový datový bod generovat.</span><span class="sxs-lookup"><span data-stu-id="dcc00-123">The specific product recommendation list type that the demo data point is to generate.</span></span>                                                    | <ul><li><span data-ttu-id="dcc00-124">RecoBestSelling</span><span class="sxs-lookup"><span data-stu-id="dcc00-124">RecoBestSelling</span></span></li><li><span data-ttu-id="dcc00-125">RecoNew</span><span class="sxs-lookup"><span data-stu-id="dcc00-125">RecoNew</span></span></li><li><span data-ttu-id="dcc00-126">RecoTrending</span><span class="sxs-lookup"><span data-stu-id="dcc00-126">RecoTrending</span></span></li><li><span data-ttu-id="dcc00-127">RecoCart</span><span class="sxs-lookup"><span data-stu-id="dcc00-127">RecoCart</span></span></li><li><span data-ttu-id="dcc00-128">RecoPeopleAlsoBuy</span><span class="sxs-lookup"><span data-stu-id="dcc00-128">RecoPeopleAlsoBuy</span></span></li></ul> |
| <span data-ttu-id="dcc00-129">OperatingUnitNumber</span><span class="sxs-lookup"><span data-stu-id="dcc00-129">OperatingUnitNumber</span></span> | :heavy_check_mark: | <span data-ttu-id="dcc00-131">Specifické číslo provozní jednotky, na které se očekává, že se budou nacházet doporučení produktů.</span><span class="sxs-lookup"><span data-stu-id="dcc00-131">The specific operating unit number where product recommendations are expected to be   surfaced.</span></span>                                        |                                                                              |
| <span data-ttu-id="dcc00-132">Kategorie</span><span class="sxs-lookup"><span data-stu-id="dcc00-132">Category</span></span>            |                    |    <span data-ttu-id="dcc00-133">Kategorii, pro kterou má být konkrétní seznam vrácen.</span><span class="sxs-lookup"><span data-stu-id="dcc00-133">The category the specific list should be returned for.</span></span> <span data-ttu-id="dcc00-134">Není-li zadána žádná kategorie, je seznam určen pouze k hornímu okraji hierarchie navigace.</span><span class="sxs-lookup"><span data-stu-id="dcc00-134">If no category is specified, the list is for top of navigation hierarchy only.</span></span>    |                                                                              |
| <span data-ttu-id="dcc00-135">SeedItemId</span><span class="sxs-lookup"><span data-stu-id="dcc00-135">SeedItemId</span></span>          |                    |    <span data-ttu-id="dcc00-136">Pro seznamy, které vyžadují zdroje (RecoPeopleAlsoBuy a RecoCart), by produkt měl obsahovat další produkty.</span><span class="sxs-lookup"><span data-stu-id="dcc00-136">For lists that require seed (RecoPeopleAlsoBuy and RecoCart), the product those lists should show additional products for.</span></span>            |                                                                              |
| <span data-ttu-id="dcc00-137">ItemIds</span><span class="sxs-lookup"><span data-stu-id="dcc00-137">ItemIds</span></span>             | :heavy_check_mark: | <span data-ttu-id="dcc00-139">Jeden nebo více produktů, které mají být vráceny jako výsledek, oddělené znakem ‘;’.</span><span class="sxs-lookup"><span data-stu-id="dcc00-139">One or more products to be returned as the result, separated by ‘;’.</span></span>                                                                  |                                                                              |

## <a name="customize-demo-data"></a><span data-ttu-id="dcc00-140">Přizpůsobení ukázkových dat</span><span class="sxs-lookup"><span data-stu-id="dcc00-140">Customize demo data</span></span>
<span data-ttu-id="dcc00-141">Můžete upravovat výchozí ukázková data s libovolnými informacemi o produktech a kategoriích konfigurovaných v HQ.</span><span class="sxs-lookup"><span data-stu-id="dcc00-141">You can edit the default demo data with any product and category information configured in HQ.</span></span> <span data-ttu-id="dcc00-142">Jakmile je CSV aktualizován, budou doporučení produktu vrácená odběratelům okamžitě zohledněna.</span><span class="sxs-lookup"><span data-stu-id="dcc00-142">Once you update the .csv, the product recommendations that are returned to customers will immediately reflect the changes.</span></span>

<span data-ttu-id="dcc00-143">Přípona obsahuje datový objekt s názvem 'RecoMockDataset.csv', který vám umožňuje ovládat datovou sadu používanou k napájení výsledků těchto doporučení.</span><span class="sxs-lookup"><span data-stu-id="dcc00-143">The extension contains a datafile called 'RecoMockDataset.csv' which allows you to control the dataset used to power the mock recommendations results.</span></span> <span data-ttu-id="dcc00-144">Název souboru lze řídit pomocí konfigurace rozšíření pomocí nastavení **ext.Recommendations.DemoFilePath**.</span><span class="sxs-lookup"><span data-stu-id="dcc00-144">The file name can be controlled through extension configuration using the **ext.Recommendations.DemoFilePath** setting.</span></span> <span data-ttu-id="dcc00-145">Díky tomu můžete mít k dispozici více datových sad, které lze snadno přepínat mezi konfigurací.</span><span class="sxs-lookup"><span data-stu-id="dcc00-145">This enables you to have multiple datasets available that can be switched between easily through configuration.</span></span>


```xml
<settings>
    <add name="ext.Recommendations.DemoFilePath" value="RecoMockDataset.csv" />
</settings>
```

## <a name="additional-resources"></a><span data-ttu-id="dcc00-146">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="dcc00-146">Additional Resources</span></span>

[<span data-ttu-id="dcc00-147">Přehled doporučení produktu</span><span class="sxs-lookup"><span data-stu-id="dcc00-147">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="dcc00-148">Plánování prostředí</span><span class="sxs-lookup"><span data-stu-id="dcc00-148">Environment planning</span></span>](../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md)
