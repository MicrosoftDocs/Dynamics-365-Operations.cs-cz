---
title: Ukázková data doporučení produktu pro omnikanál
description: Cílem tohoto dokumentu je poskytnou pokyny, jak využívat doporučení Omni kanálu v prostředích s jedním polem na úrovni 1, pomocí předem naplněných a přizpůsobitelných ukázkových dat.
author: bebeale
manager: AnnBe
ms.date: 10/1/2019
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
ms.openlocfilehash: 81af4c1bb7828c9b346a3ef514d8657e853dcefb
ms.sourcegitcommit: c526cfd1f823df1ff33ded95e599a72f0a15cc5a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/27/2019
ms.locfileid: "2225679"
---
# <a name="omni-channel-product-recommendations-demo-data"></a>Ukázková data doporučení produktu pro omnikanál

Cílem tohoto dokumentu je poskytnou pokyny, jak využívat doporučení Omni kanálu v prostředích s jedním polem na úrovni 1, pomocí předem naplněných a přizpůsobitelných ukázkových dat.

Doporučení omnikanálového produktu poskytuje sadu redakčně upravených nebo programově generovaných uspořádaných seznamů produktů. Tyto seznamy lze použít v několika situacích, v závislosti na obchodní potřebě. Další informace o seznamech doporučených produktů naleznete v tématu [Přehled doporučení produktu.](product-recommendaitons-overview.md)

Pro prostředí s vrstvami 2 a vyššími Dynamics jsou doporučení produktu automaticky vypočítána na základě zákaznických dat.
Použití ukázkových dat doporučení produktu nezakáže žádné řešení doporučení produktů, které již bylo v daném prostředí zřízeno a žádné náklady související s jeho použitím.

Doporučení produktu na úrovni 1 jsou založena pouze mimo statická ukázková data uložená v souboru CSV.

## <a name="enabling-product-recommendations-demo-data-in-an-environment"></a>Povolení ukázkových dat doporučení produktu v prostředí

Je nutné, aby zákazníci nasadili **Náhled rozšíření ukázky Dynamics 365 Commerce** do příslušného prostředí, které automaticky povolí ukázková data doporučení produktu.

## <a name="default-demo-data"></a>Výchozí ukázková data
Každé prostředí typu OneBox se dodává s předem nahranými ukázkovými daty doporučení produktu uloženými v souboru **reco_demo_data. csv** odděleném čárkami ve stejné složce jako tento dokument na serveru Retail.

Tyto údaje jsou uspořádány do následujících sloupců

| Název sloupce         | Povinné          | Popis                                                                                                                                 | Možné hodnoty                                                              |
|---------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| RecoList            | :heavy_check_mark: | Konkrétní typ seznamu doporučení produktu, který má ukázkový datový bod generovat.                                                    | <ul><li>RecoBestSelling</li><li>RecoNew</li><li>RecoTrending</li><li>RecoCart</li><li>RecoPeopleAlsoBuy</li></ul> |
| OperatingUnitNumber | :heavy_check_mark: | Specifické číslo provozní jednotky, na které se očekává, že se budou nacházet doporučení produktů.                                        |                                                                              |
| Kategorie            |                    |    Kategorii, pro kterou má být konkrétní seznam vrácen. Není-li zadána žádná kategorie, je seznam určen pouze k hornímu okraji hierarchie navigace.    |                                                                              |
| SeedItemId          |                    |    Pro seznamy, které vyžadují zdroje (RecoPeopleAlsoBuy a RecoCart), by produkt měl obsahovat další produkty.            |                                                                              |
| ItemIds             | :heavy_check_mark: | Jeden nebo více produktů, které mají být vráceny jako výsledek, oddělené znakem **;**.                                                                  |                                                                              |


## <a name="customize-demo-data"></a>Přizpůsobení ukázkových dat
Zákazníci mohou upravovat výchozí ukázková data s libovolnými informacemi o produktech a kategoriích konfigurovaných v HQ. Jakmile je CSV aktualizován, budou doporučení produktu vrácená odběratelům okamžitě zohledněna.

Přípona obsahuje datový objekt s názvem RecoMockDataset.csv, který umožňuje odběrateli ovládat datovou sadu používanou k napájení výsledků těchto doporučení. Název souboru lze řídit pomocí konfigurace rozšíření pomocí nastavení **ext.Recommendations.DemoFilePath**. Díky tomu mohou mít zákazníci k dispozici více datových sad, které lze snadno přepínat mezi konfigurací.

```
  <settings>
    <add name="ext.Recommendations.DemoFilePath" value="RecoMockDataset.csv" />
  </settings>
```

## <a name="additional-resources"></a>Další zdroje

[Přehled doporučení produktu](product-recommendations-overview.md)

[Plánování prostředí](environment-planning.md)
