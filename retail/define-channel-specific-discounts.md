---
title: "Definovat slevy specifické pro kanál"
description: "Maloobchodní prodejci často nastavují různé slevy v různých kanálech. Toto téma popisuje koncepty, které je nutné znát k vytvoření slevy pro konkrétní kanál."
author: josaw1
manager: AnnBe
ms.date: 2015-12-04 02 - 13 - 00
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: RetailAffiliationPriceGroup, RetailCatalogPriceGroup, RetailChannelPriceGroup, RetailDiscountPriceGroup, RetailDiscountPricingWorkspace, RetailPeriodicDiscount, RetailStoreItemPriceList, RetailStoreTable
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 16401
ms.assetid: d807fd51-86aa-47a0-8e00-6c5ddd21ff6b
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: b21fd97426b331726c12ea29f89817a46dd445c3
ms.openlocfilehash: b2f59db59ea49925c3bb5e1d75beee95191220d0
ms.lasthandoff: 03/31/2017


---

# <a name="define-channel-specific-discounts"></a>Definovat slevy specifické pro kanál

Maloobchodní prodejci často nastavují různé slevy v různých kanálech. Toto téma popisuje koncepty, které je nutné znát k vytvoření slevy pro konkrétní kanál. 

<a name="channel-specific-discounts"></a>Slevy specifické pro kanál
--------------------------

Prodejci často nabízejí různé slevy v různých kanálech. To se může provést na adresu místní tržní podmínky nebo řešit konkurenčních prodejců.

Prodej a obchodování v 365 Microsoft Dynamics pro operace používá k definování specifické pro kanál slevy cenové skupiny. Cenové skupiny lze přiřadit následujícím entitám (jedné entitě nebo více entitám): kanály, katalogy, umístění a věrnostní programy. V tomto článku jsou popsány kanály, ale stejné principy se týkají také slevových katalogů, slev podle umístění a věrnostních slev.

## <a name="price-groups"></a>Cenové skupiny
\[Titulek id = "Příloha\_256084" Zarovnat = "alignnone" width = "640"\][![cena skupiny](./media/price-groups-1024x608.png)](./media/price-groups.png) pro maloobchodní ceny propojení skupiny\[/titulek\]

Diagram uvedený výše znázorňuje vztah mezi subjekty, které mohou být v transakci (kanál, katalog, umístění, Zákazník, věrnostní karty) a různé typy slev, které lze konfigurovat. Všechny transakce dojít do kanálu, kanál je zaručena v transakci. Zbývající entity jsou volitelné. Na všech stránkách hlavních dat se nachází odkaz na související stránku cenové skupiny, na které si můžete prohlédnout cenové skupiny a v případě potřeby přidat další. Cenové skupiny se používá k propojení čtyři různé typy entit, slevy, úpravy cen a obchodních dohod. Doporučujeme naplánovat strategii jak bude název vaší cenové skupiny k jejich uspořádání. Jednou z možností by bylo použít písmeno nebo číslo předponu nebo příponu, chcete-li rozlišit různé typy. Například 1-xxxxx kanálu cenové skupiny a 2-xxxxx pro katalog cenové skupiny. Existují čtyři stránky s dotazy – každá z nich je zaměřená na maloobchodní entity, které mohou mít přidrženy slevy.

-   **Cenové skupiny maloobchodní sítě **– Na této stránce je uveden seznam kanálů a slev propojených pro každou cenovou skupinu.
-   **Skupiny katalogových cen**– Na této stránce je uveden seznam katalogů a slev propojených pro každou cenovou skupinu.
-   **Věrnostní cenové skupiny**– Na této stránce je uveden seznam věrnostních programů a slev propojených pro každou cenovou skupinu.
-   **Cenové skupiny umístění **– Na této stránce je uveden seznam umístění a slev propojených pro každou cenovou skupinu.

## <a name="example-channel-discount-set-up"></a>Příklad nastavení slevy pro kanál
Na následujícím příkladu jsou znázorněny úkoly zahrnuté do nastavování slevy pro kanál.

1.  V tomto příkladu máte kanál nazvaný **Houston** a chystáte se vytvořit novou slevu nazvanou **Zpět do školy**.
2.  Vzhledem k tomu, že strategie cen a slev zahrnuje možnost slev pro kanál, při vytvoření kanálu vždy vytvoříte cenovou skupinu specifickou pro kanál.
3.  Máte cenovou skupinu **Houston-CS**, která je přiřazena ke kanálu **Houston**.
4.  Po vytvoření nové slevy  **Zpět do školy** je nutné kliknout na tlačítko **Cenové skupiny** v horní části stránky **Sleva**. Otevře se stránka **Skupiny slevových cen**. Poté klikněte na tlačítko **Nový** a vyberte cenovou skupinu **Houston-CS**.
5.  Nyní můžete povolit slevu a zadat ji do kanálu.

 

<a name="see-also"></a>Viz také
--------

[Price adjustments and discounts](price-adjustments-discounts.md)


