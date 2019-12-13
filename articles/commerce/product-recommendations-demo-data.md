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
ms.openlocfilehash: af8a30e69d9ed143e045950efdcece207f6da14c
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697927"
---
# <a name="get-product-recommendations-using-demo-data"></a>Získání doporučení produktu pomocí ukázkových dat
Tento dokument poskytuje pokyny, jak využívat doporučení Omni kanálu v prostředích s jedním polem na úrovni 1, pomocí předem naplněných a přizpůsobitelných ukázkových dat.

Doporučení omnikanálového produktu poskytuje sadu redakčně upravených nebo programově generovaných seznamů produktů. Tyto seznamy lze použít v několika situacích, v závislosti na obchodní potřebě. Další informace o seznamech doporučených produktů naleznete v tématu [Přehled doporučení produktu](product-recommendations.md).

Pro prostředí s vrstvami 2 a vyššími Dynamics 365 jsou doporučení produktu automaticky vypočítána na základě zákaznických dat. Použití ukázkových dat doporučení produktu nezakáže žádné řešení doporučení produktů, které již bylo v daném prostředí zřízeno a žádné náklady související s jeho použitím.

Doporučení produktu na úrovni 1 jsou založena pouze mimo statická ukázková data uložená v souboru .CSV.

## <a name="enabling-product-recommendations-demo-data-in-an-environment"></a>Povolení ukázkových dat doporučení produktu v prostředí
Chcete-li povolit ukázková data pro odoporučení produktu, musíte nasadit Náhled rozšíření ukázky Dynamics 365 Commerce do příslušného prostředí. Tím se automaticky povolí ukázková data doporučení produktu.

## <a name="default-demo-data"></a>Výchozí ukázková data
Každé prostředí typu OneBox se dodává s předem nahranými ukázkovými daty doporučení produktu uloženými v souboru ‘reco_demo_data.csv’ odděleném čárkami na serveru Retail.

Data jsou uspořádána do následujících sloupců.

| Název sloupce         | Povinné          | Popis                                                                                                                                 | Možné hodnoty                                                              |
|---------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| RecoList            | :heavy_check_mark: | Konkrétní typ seznamu doporučení produktu, který má ukázkový datový bod generovat.                                                    | <ul><li>RecoBestSelling</li><li>RecoNew</li><li>RecoTrending</li><li>RecoCart</li><li>RecoPeopleAlsoBuy</li></ul> |
| OperatingUnitNumber | :heavy_check_mark: | Specifické číslo provozní jednotky, na které se očekává, že se budou nacházet doporučení produktů.                                        |                                                                              |
| Kategorie            |                    |    Kategorii, pro kterou má být konkrétní seznam vrácen. Není-li zadána žádná kategorie, je seznam určen pouze k hornímu okraji hierarchie navigace.    |                                                                              |
| SeedItemId          |                    |    Pro seznamy, které vyžadují zdroje (RecoPeopleAlsoBuy a RecoCart), by produkt měl obsahovat další produkty.            |                                                                              |
| ItemIds             | :heavy_check_mark: | Jeden nebo více produktů, které mají být vráceny jako výsledek, oddělené znakem ‘;’.                                                                  |                                                                              |

## <a name="customize-demo-data"></a>Přizpůsobení ukázkových dat
Můžete upravovat výchozí ukázková data s libovolnými informacemi o produktech a kategoriích konfigurovaných v HQ. Jakmile je CSV aktualizován, budou doporučení produktu vrácená odběratelům okamžitě zohledněna.

Přípona obsahuje datový objekt s názvem 'RecoMockDataset.csv', který vám umožňuje ovládat datovou sadu používanou k napájení výsledků těchto doporučení. Název souboru lze řídit pomocí konfigurace rozšíření pomocí nastavení **ext.Recommendations.DemoFilePath**. Díky tomu můžete mít k dispozici více datových sad, které lze snadno přepínat mezi konfigurací.


```
  <settings>
    <add name="ext.Recommendations.DemoFilePath" value="RecoMockDataset.csv" />
  </settings>
```

## <a name="additional-resources"></a>Další zdroje

[Přehled doporučení produktu](product-recommendations.md)

[Plánování prostředí](../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md)
