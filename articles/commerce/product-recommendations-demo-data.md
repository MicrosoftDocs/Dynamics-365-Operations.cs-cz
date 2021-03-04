---
title: Vytvoření doporučení s ukázkovými daty
description: Toto téma poskytuje pokyny, jak využívat doporučení Omni kanálu v prostředích s jedním polem na úrovni 1, pomocí předem naplněných a přizpůsobitelných ukázkových dat.
author: bebeale
manager: AnnBe
ms.date: 05/26/2020
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
ms.openlocfilehash: cca6913375eec2565852676f3c1da5a67f71e14f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4410655"
---
# <a name="create-recommendations-with-demo-data"></a>Vytvoření doporučení s ukázkovými daty

[!include [banner](includes/banner.md)]

Toto téma poskytuje pokyny, jak využívat doporučení Omni kanálu v prostředích s jedním polem na úrovni 1, pomocí předem naplněných a přizpůsobitelných ukázkových dat.

Doporučení omnikanálového produktu poskytuje sadu redakčně upravených nebo programově generovaných seznamů produktů. Tyto seznamy lze použít v několika situacích, v závislosti na obchodní potřebě. Další informace o seznamech doporučených produktů naleznete v tématu [Přehled doporučení produktu](product-recommendations.md).

Pro prostředí s vrstvami 2 a vyššími Dynamics 365 jsou doporučení produktu automaticky vypočítána na základě zákaznických dat. Použití ukázkových dat doporučení produktu nezakáže žádné řešení doporučení produktů, které již bylo v daném prostředí zřízeno a žádné náklady související s jeho použitím.

Doporučení produktu na úrovni 1 jsou založena pouze mimo statická ukázková data uložená v souboru .CSV.

## <a name="enabling-product-recommendations-demo-data-in-an-environment"></a>Povolení ukázkových dat doporučení produktu v prostředí
Chcete-li povolit ukázková data pro doporučení produktů, musíte nasadit Náhled rozšíření ukázky Dynamics 365 Commerce do příslušného prostředí. Tím se automaticky povolí ukázková data doporučení produktu.

## <a name="default-demo-data"></a>Výchozí ukázková data
Každé prostředí typu OneBox se dodává s předem nahranými ukázkovými daty doporučení produktu uloženými v souboru ‘reco_demo_data.csv’ odděleném čárkami v Commerce Scale Unit.

Data jsou uspořádána do následujících sloupců.

| Název sloupce         | Povinné          | popis                                                                                                                                 | Možné hodnoty                                                              |
|---------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| RecoList            | :heavy_check_mark: | Konkrétní typ seznamu doporučení produktu, který má ukázkový datový bod generovat.                                                    | <ul><li>RecoBestSelling</li><li>RecoNew</li><li>RecoTrending</li><li>RecoCart</li><li>RecoPeopleAlsoBuy</li></ul> |
| OperatingUnitNumber | :heavy_check_mark: | Specifické číslo provozní jednotky, na které se očekává, že se budou nacházet doporučení produktů.                                        |                                                                              |
| Kategorie            |                    |    Kategorii, pro kterou má být konkrétní seznam vrácen. Není-li zadána žádná kategorie, je seznam určen pouze k hornímu okraji hierarchie navigace.    |                                                                              |
| SeedItemId          |                    |    Pro seznamy, které vyžadují zdroje (RecoPeopleAlsoBuy a RecoCart), by produkt měl obsahovat další produkty.            |                                                                              |
| CustomerId          |                    |    Pro seznamy, které vyžadují identifikátor odběratele (RecoPicks).  Výchozí hodnota 0 se vztahuje na všechny odběratele.          |                                                                              |
| ItemIds             | :heavy_check_mark: | Jeden nebo více produktů, které mají být vráceny jako výsledek, oddělené znakem ‘;’.                                                                  |                                                                              |

## <a name="customize-demo-data"></a>Přizpůsobení ukázkových dat
Můžete upravovat výchozí ukázková data s libovolnými informacemi o produktech a kategoriích konfigurovaných v HQ. Jakmile je CSV aktualizován, budou doporučení produktu vrácená odběratelům okamžitě zohledněna.

Přípona obsahuje datový objekt s názvem 'RecoMockDataset.csv', který vám umožňuje ovládat datovou sadu používanou k napájení výsledků těchto doporučení. Název souboru lze řídit pomocí konfigurace rozšíření pomocí nastavení **ext.Recommendations.DemoFilePath**. Díky tomu můžete mít k dispozici více datových sad, které lze snadno přepínat mezi konfigurací.


```xml
<settings>
    <add name="ext.Recommendations.DemoFilePath" value="RecoMockDataset.csv" />
</settings>
```

## <a name="additional-resources"></a>Další prostředky

[Přehled doporučení produktu](product-recommendations.md)

[Povolení Azure Data Lake Storage v prostředí Dynamics 365 Commerce](enable-adls-environment.md)

[Povolit doporučení produktu](enable-product-recommendations.md)

[Povolení přizpůsobených doporučení](personalized-recommendations.md)

[Odhlášení přizpůsobených doporučení](personalization-gdpr.md)

[Povolit doporučení typu „podobný vzhled“](shop-similar-looks.md)

[Přidání doporučení produktu v POS](product.md)

[Přidání doporučení na obrazovku transakcí](add-recommendations-control-pos-screen.md)

[Úprava výsledků doporučení AI-ML](modify-product-recommendation-results.md)

[Ručně vytvořit uspořádaná doporučení](create-editorial-recommendation-lists.md)

[Často kladené dotazy k doporučení produktu](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]