---
title: Dimenze produktu
description: "Existují čtyři dimenze produktu – barva, konfigurace, velikost a styl. Kombinujte dimenze produktu ve skupinách dimenzí a přiřazujte skupiny dimenzí k základním produktům. Kombinace dimenzí produktu určuje způsob definování variant produktu."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
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
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 8854ab94a71cc363bcd073d2df47bc01a243b6cd
ms.lasthandoff: 03/31/2017


---

# <a name="product-dimensions"></a>Dimenze produktu

[!include[banner](../includes/banner.md)]


Existují čtyři dimenze produktu – barva, konfigurace, velikost a styl. Kombinujte dimenze produktu ve skupinách dimenzí a přiřazujte skupiny dimenzí k základním produktům. Kombinace dimenzí produktu určuje způsob definování variant produktu.

Dimenze produktu jsou vlastnosti, které slouží k identifikaci varianty produktu. Kombinace dimenzí produktu slouží k definování variant produktu. Chcete-li vytvořit variantu produktu, je nutné definovat alespoň jednu dimenzi produktu pro základní produkt.
Varianty produktu
----------------

Varianty produktu jsou označovány také jako položky. Položka je hmotný produkt, který není stejný jako služba. Je také možné definovat základní produkt s typem služby. Pomocí typu Služba můžete specifikovat varianty produktu, které obsahují služby. Můžete například určit základní produkt pro konzultační práci a varianty produktu pro práci, kterou zajišťují vyšší konzultanti a nižší konzultanti.

## <a name="product-dimensions"></a>Dimenze produktu
Jsou k dispozici následující dimenze produktu: konfigurace, barva, velikost a styl. Varianty výrobku mohou být generovány na základě hodnot dimenze produktu.

Produktu dimenze hodnot, jako je velikost, barvu a styl může být vytvořena na **velikost**, **barva** a **styl** stránek, které lze přistupovat z následujících umístění: **řízení informací o produktech**&gt;**nastavení**&gt;**dimenze a varianty skupiny**&gt;**velikosti, barvy nebo styly**. Hodnoty dimenze produktu pro konfigurační dimenze jsou obvykle tvořeny pomocí konfigurátoru produktu nebo konfigurátoru založeného na dimenzích. Dimenze produktu se také vytvářejí a udržují na stránce **Dimenze produktu**, která je přístupná z následujících umístění:
-   Klepněte na tlačítko **řízení informací o produktech**&gt;**produkty**&gt;**produktům**. Na **podokno akcí**, klepněte na tlačítko **dimenze produktu**.
-   Klepněte na tlačítko **řízení informací o produktech**&gt;**produkty**&gt;**všechny produkty a základní produkty**. Vyberte základní produkt. Na **podokno akcí**, klepněte na tlačítko **dimenze produktu**.
-   Klepněte na tlačítko **řízení informací o produktech**&gt;**uvolněných produktů**. Vyberte základní produkt. Na **podokno akcí**, klepněte na tlačítko **výrobku**. Ve skupině **Základní produkt** klikněte na **Dimenze produktu**.

Počet variant, které je možné vytvořit pro položku, je omezen počet možných kombinací dimenzí produktu.
| **Tip **                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------|
| Používáte-li na produkt, například na řádku objednávky, vyberete dimenze produktu pro identifikování varianty produktu, se kterou chcete pracovat. |

## <a name="example"></a>Příklad
Společnost prodává džíny. Tato položka, džíny, používá pro dimenzi produktu barvy a velikosti. Džíny se prodávají ve třech různých barvách a šesti různých velikostech. Barvy: Modrá, černá, hnědá Velikosti: XS, S, M, L, XL, XXL Ne všechny velikosti jsou k dispozici ve všech třech barvách. Pokud by byly všechny kombinace dostupné, výsledkem by bylo 18 různých druhů džín. V tomto příkladu se vyrábí pouze těchto devět kombinací variant produktu.

| Barva | Velikost |
|-------|------|
| Modrá  | KŘÍŽKY   |
| Modrá  | S    |
| Modrá  | S    |
| Černá | S    |
| Černá | V    |
| Černá | XL   |
| Hnědá | V    |
| Hnědá | XL   |
| Hnědá | XXL  |






