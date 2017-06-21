---
title: Dimenze produktu
description: "Existují čtyři dimenze produktu – barva, konfigurace, velikost a styl. Kombinujte dimenze produktu ve skupinách dimenzí a přiřazujte skupiny dimenzí k základním produktům. Kombinace dimenzí produktu určuje způsob definování variant produktu."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductDimension, EcoResProductDimensionGroup, EcoResProductMasterDimension, RetailEcoResColor, RetailEcoResSize, RetailEcoResStyle
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19171
ms.assetid: 81fa3709-4ab8-4fbf-9806-359892a05985
ms.search.region: Global
ms.search.industry: Retail
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 7e6409db92b929eebca70d6d0176dd9b54a5f9b9
ms.contentlocale: cs-cz
ms.lasthandoff: 05/25/2017


---

# <a name="product-dimensions"></a>Dimenze produktu

[!include[banner](../includes/banner.md)]


Existují čtyři dimenze produktu – barva, konfigurace, velikost a styl. Kombinujte dimenze produktu ve skupinách dimenzí a přiřazujte skupiny dimenzí k základním produktům. Kombinace dimenzí produktu určuje způsob definování variant produktu.

Dimenze produktu jsou vlastnosti, které slouží k identifikaci varianty produktu. Kombinace dimenzí produktu slouží k definování variant produktu. Chcete-li vytvořit variantu produktu, je nutné definovat alespoň jednu dimenzi produktu pro základní produkt.
Varianty produktu
----------------

Varianty produktu jsou označovány také jako položky. Položka je hmotný produkt, který není stejný jako služba. Je také možné definovat základní produkt s typem Servis. Pomocí typu Služba můžete specifikovat varianty produktu, které obsahují služby. Můžete například určit základní produkt pro konzultační práci a varianty produktu pro práci, kterou zajišťují vyšší konzultanti a nižší konzultanti.

## <a name="product-dimensions"></a>Dimenze produktu
K dispozici jsou následující dimenze produktu: konfigurace, barva, velikost a styl. Varianty produktu lze generovat na základě hodnot dimenzí produktu.

Hodnoty dimenze produktu, jako například Velikost, Barva a Styl, lze vytvořit na stránce **Velikost**, **Barva** a **Styl**, které jsou přístupné z následujících umístění: **Řízení informací o produktech** &gt; **Nastavení** &gt; **Dimenze a varianty skupiny** &gt; **Velikosti, barvy nebo styly**. Hodnoty dimenze produktu pro konfigurační dimenze jsou obvykle tvořeny pomocí konfigurátoru produktu nebo konfigurátoru založeného na dimenzích. Dimenze produktu se také vytvářejí a udržují na stránce **Dimenze produktu**, která je přístupná z následujících umístění:
-   Klikněte na **Řízení informací o produktech** &gt; **Produkty** &gt; **Základní produkty**. V **podokně akcí** klikněte na možnost **Dimenze produktu**.
-   Klikněte na **Řízení informací o produktech** &gt; **Produkty** &gt; **Všechny produkty a základní produkty**. Vyberte základní produkt. V **podokně akcí** klikněte na možnost **Dimenze produktu**.
-   Klikněte na možnosti **Řízení informací o produktech** &gt; **Uvolněné produkty**. Vyberte základní produkt. V **podokně akcí** klikněte na **Produkt**. Ve skupině **Základní produkt** klikněte na **Dimenze produktu**.

Počet variant, které je možné vytvořit pro položku, je omezen počet možných kombinací dimenzí produktu.
| **Tip**                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------|
| Používáte-li na produkt, například na řádku objednávky, vyberete dimenze produktu pro identifikování varianty produktu, se kterou chcete pracovat. |

## <a name="example"></a>Příklad
Společnost prodává džíny. Tato položka, džíny, používá pro dimenzi produktu barvy a velikosti. Džíny se prodávají ve třech různých barvách a šesti různých velikostech. Barvy: Modrá, černá, hnědá Velikosti: XS, S, M, L, XL, XXL Ne všechny velikosti jsou k dispozici ve všech třech barvách. Pokud by byly všechny kombinace dostupné, výsledkem by bylo 18 různých druhů džín. V tomto příkladu se vyrábí pouze těchto devět kombinací variant produktu.

| Barva | Velikost |
|-------|------|
| Modrá  | XS   |
| Modrá  | S    |
| Modrá  | S    |
| Černá | S    |
| Černá | V    |
| Černá | XL   |
| Hnědá | V    |
| Hnědá | XL   |
| Hnědá | XXL  |






