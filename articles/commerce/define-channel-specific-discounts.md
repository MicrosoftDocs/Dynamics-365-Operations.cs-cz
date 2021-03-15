---
title: Definovat slevy specifické pro kanál
description: Maloobchodní prodejci často nastavují různé slevy v různých kanálech. Toto téma popisuje koncepty, které je nutné znát k vytvoření slevy pro konkrétní kanál.
author: scott-tucker
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailAffiliationPriceGroup, RetailCatalogPriceGroup, RetailChannelPriceGroup, RetailDiscountPriceGroup, RetailDiscountPricingWorkspace, RetailPeriodicDiscount, RetailStoreItemPriceList, RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.custom: 16401
ms.assetid: d807fd51-86aa-47a0-8e00-6c5ddd21ff6b
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 990c0d0b4b89420094dc86552b3e07717e5c7056
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4991383"
---
# <a name="define-channel-specific-discounts"></a>Definování slev specifických pro kanál

[!include [banner](includes/banner.md)]

Toto téma popisuje koncepty, které je nutné znát k vytvoření slevy pro konkrétní kanál.

## <a name="channel-specific-discounts"></a>Slevy specifické pro kanál

Maloobchodní prodejci často nabízejí různé slevy v různých kanálech. Činí tak z důvodu přizpůsobení místním tržním podmínkám nebo v rámci konkurenčního souboje s jinými maloobchodními prodejci.

Commerce používá cenové skupiny pro definování slev specifických pro kanál. Cenové skupiny lze přiřadit následujícím entitám (jedné entitě nebo více entitám): kanály, katalogy, umístění a věrnostní programy. V tomto článku jsou popsány kanály, ale stejné principy se týkají také slevových katalogů, slev podle umístění a věrnostních slev.

## <a name="price-groups"></a>Cenové skupiny

[![Cenové skupiny](./media/price-groups-1024x608.png)](./media/price-groups.png)

Ve výše uvedeném diagramu je znázorněn vztah mezi entitami, které mohou být v transakci (kanál, katalog, umístění, odběratel, věrnostní karta), a různými typy slev, které lze konfigurovat. Ke všem transakcím dochází v kanálu, takže přítomnost kanálu v transakci je zaručena. Zbývající entity jsou volitelné. Na všech stránkách hlavních dat se nachází odkaz na související stránku cenové skupiny, na které si můžete prohlédnout cenové skupiny a v případě potřeby přidat další. Cenová skupina se používá k propojení čtyř typů entit se slevami, úpravami cen a obchodními smlouvami. Doporučujeme, abyste si naplánovali princip, jakým budete cenové skupiny pojmenovávat, aby se vám dobře spravovaly. Jednou z možností je použít písmeno či číslo jako předponu nebo příponu, podle které bude možné rozlišit různé typy. Název ve formátu „1-xxxxx“ může například odkazovat na cenové skupiny pro kanály a název ve formátu „2-xxxxx“ na cenové skupiny pro katalog. Existují čtyři stránky s dotazy – každá z nich je zaměřená na entity commerce, které mohou mít přidruženy slevy.

- **Cenové skupiny kanálů** – Na této stránce je uveden seznam kanálů a slev propojených pro každou cenovou skupinu.
- **Skupiny katalogových cen** – Na této stránce je uveden seznam katalogů a slev propojených pro každou cenovou skupinu.
- **Věrnostní cenové skupiny** – Na této stránce je uveden seznam věrnostních programů a slev propojených pro každou cenovou skupinu.
- **Cenové skupiny umístění** – Na této stránce je uveden seznam umístění a slev propojených pro každou cenovou skupinu.

## <a name="example-channel-discount-set-up"></a>Příklad nastavení slevy pro kanál

Na následujícím příkladu jsou znázorněny úkoly zahrnuté do nastavování slevy pro kanál.

1. V tomto příkladu máte kanál nazvaný **Houston** a chystáte se vytvořit novou slevu nazvanou **Zpět do školy**.
2. Vzhledem k tomu, že strategie cen a slev zahrnuje možnost slev pro kanál, při vytvoření kanálu vždy vytvoříte cenovou skupinu specifickou pro kanál.
3. Máte cenovou skupinu **Houston-CS**, která je přiřazena ke kanálu **Houston**.
4. Po vytvoření nové slevy  **Zpět do školy** je nutné kliknout na tlačítko **Cenové skupiny** v horní části stránky **Sleva**. Otevře se stránka **Skupiny slevových cen**. Poté klikněte na tlačítko **Nový** a vyberte cenovou skupinu **Houston-CS**.
5. Nyní můžete povolit slevu a zadat ji do kanálu.

## <a name="additional-resources"></a>Další zdroje

[Úpravy ceny a slevy](price-adjustments-discounts.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]