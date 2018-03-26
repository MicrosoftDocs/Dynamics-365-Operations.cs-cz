---
title: "Názvosloví čísel a názvů variant produktu"
description: "Toto téma popisuje, jak nastavit názvosloví pro čísla produktu, které nahradí opravený formát [základní produkt - konfigurace – velikost – barva – styl]."
author: roxanadiaconu
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResNomenclature, EcoResProductDimensionGroup, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 220104
ms.assetid: 3fe69fb7-5c32-423c-98a8-2f53186cda68
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: 72d4ff5e1311005d3bf43a13e28208cd9b3d1457
ms.openlocfilehash: 6a620f2a0105d578d419d3aac816c7d78fbf3e46
ms.contentlocale: cs-cz
ms.lasthandoff: 03/07/2018

---

# <a name="nomenclature-of-product-variant-numbers-and-names"></a>Názvosloví čísel a názvů variant produktu

[!include[banner](../includes/banner.md)]

Toto téma popisuje, jak nastavit názvosloví pro čísla produktu, které nahradí opravený formát [základní produkt - konfigurace – velikost – barva – styl]. Nové názvosloví má cílený formát, který zahrnuje číslo základního produktu, rozměry aktivního produktu a textové oddělovače podle vašeho výběru. Můžete také vytvořit názvosloví pro názvy produktů. A konečně můžete také vytvořit názvosloví k identifikaci konfigurací, které jsou vytvořeny konfigurátorem produktu založeném na omezeních. Tato názvosloví můžou obsahovat atributy podle vašeho výběru.

Nová názvosloví pro čísla variant produktu a názvy variant produktu umožňují zahrnout segmenty do identifikátorů variant produktu. Tyto segmenty mohou obsahovat číslo a název základního produktu, ID a názvy dimenzí produktu, číselné řady, konstanty textu a atributy. Tato funkce umožňuje rychle najít konkrétní variantu produktu, když vytváříte nákupní nebo prodejní objednávku. Názvosloví pro čísla variant produktu i názvy variant produktu se vytváří na stránce **Názvosloví produktu**. Tuto stránku otevřete tak, že kliknete na **Správa informací o produktu** &gt; **Nastavení**.

## <a name="nomenclature-of-predefined-product-variants"></a>Názvosloví předdefinovaných variant produktu
Varianty produktu jsou generovány pro hlavní produkty podle jedné ze tří technologií konfigurace:

-   Předem definované varianty
-   Založené na omezeních
-   Založené na dimenzi

Každá varianta produktu má číslo a název a názvosloví identifikace variant produktu umožňuje vybrat segmenty, které budou zahrnuty do každého čísla nebo názvu varianty produktu. Můžete vybrat následující segmenty na stránce **Názvosloví produktu**:

-   Číslo základního produktu
-   Název základního produktu
-   Hodnota číselné řady
-   Textová konstanta
-   Dimenze produktu
    -   ID nebo název konfigurace
    -   ID nebo název barvy
    -   ID nebo název velikosti
    -   ID nebo název stylu

Po definování názvosloví čísel identifikace varianty produktu může být produkt přidružen ke skupině dimenzí produktu. Všem základním produktům, které odkazují na tuto skupinu dimenzí produktu, pak budou přiřazena čísla variant produktů podle klasifikace. Názvosloví pro názvy variant produktu ale nelze přidružit skupinám dimenzí produktu. Můžete také přiřadit názvosloví pro identifikaci variant produktu přímo základnímu produktu. V takovém případě budou variantám produktu, které patří k základnímu produktu, přiřazena čísla a názvy variant produktu podle určených názvosloví.

### <a name="example"></a>Příklad

Tričko (TS1234) se vyrábí ve třech velikostech (S, M, L), čtyřech barvách (červená, zelená, modrá a žlutá) a dvou stylech (Polo, V). Proto může existovat 24 variant produktu (= 3 x 4 x 2). Vytvoříte názvosloví čísel variant produktů, které obsahuje následující segmenty:

1.  Číslo základního produktu
2.  Textová konstanta: "-"
3.  Barva
4.  Textová konstanta: "-"
5.  Velikost
6.  Textová konstanta: "-"
7.  Styl

V tomto případě bude číslo varianty produktu pro červené, malé polo tričko: TS1234-Red-Small-Polo.

## <a name="nomenclature-of-constraint-based-configurations"></a>Názvosloví konfigurací založených na dimenzích
Pro konfigurace založené na omezeních můžete vytvořit vyhrazené názvosloví pro dimenzi konfiguračního produktu. Můžete vybrat následující segmenty na stránce **Názvosloví produktu**:

-   Hodnota číselné řady
-   Textová konstanta
-   Hodnota atributu

Jednotlivé komponenty v modelu konfigurace produktu můžou mít vlastní názvosloví konfigurace. Lze použít pouze atributy, které patří ke komponentě. Nemohou být použity atributy z dílčích komponent nebo požadavky uživatelů.

### <a name="example"></a>Příklad

Model konfigurace produktu má kořenovou komponentu se dvěma atributy:

-   Materiál (plast, dřevo, ocel.)
-   Délka (10... 100)

Vytvoříte názvosloví konfigurace, které obsahuje následující segmenty:

1.  Hodnota atributu: materiál
2.  Textová konstanta: "AAA"
3.  Hodnota atributu: délka

V takovém případě bude ID konfigurace dřevěného materiálu, který má délku 78, WoodAAA78.

## <a name="nomenclature-of-dimension-based-configurations"></a>Názvosloví konfigurací založených na dimenzích
Pro konfigurace založené na dimenzích můžete vytvořit vyhrazené názvosloví pro dimenzi konfiguračního produktu. Můžete vybrat následující segmenty na stránce **Názvosloví produktu**:

-   Hodnota číselné řady
-   Textová konstanta
-   Položka konfigurační skupiny

Můžete definovat názvosloví konfigurace pro kusovníky (BOM).

### <a name="example"></a>Příklad

Kusovník má čtyři řádky kusovníku, které jsou rozděleny do dvou konfiguračních skupin:

-   Řádek kusovníku: M0007, standardní skříň
    -   Skupina konfigurace: Skříň
-   Řádek kusovníku: M0008, vysoká koncová skříň
    -   Skupina konfigurace: Skříň
-   Řádek kusovníku: M0021, přední potah mřížky
    -   Skupina konfigurace: Přední mřížka
-   Řádek kusovníku: M0022, přední kovová mřížka
    -   Skupina konfigurace: Přední mřížka

Vytvoříte názvosloví konfigurace, které obsahuje následující segmenty:

1.  Skupina konfigurace: Skříň
2.  Textová konstanta: "&"
3.  Skupina konfigurace: Přední mřížka

V tomto případě bude ID konfigurace standardní skříně s přední látkovou mřížkou M0007&M0021.

## <a name="nomenclature-for-a-combination-of-product-variants-and-configurations"></a>Názvosloví kombinace variant a konfigurací produktu
Při použití technologie konfigurace založené na omezeních nebo na dimenzích ke konfiguraci variant produktu pro základní produkt mohou čísla variant produktu zahrnovat čísla variant produktu z konfigurační dimenze. Chcete-li nakonfigurovat varianty, postupujte následovně.

1.  Na stránce **Názvosloví produktu** definujte názvosloví čísel variant produktů, které zahrnuje konfigurační dimenzi.
2.  Toto názvosloví přiřaďte skupině dimenze produktu s dimenzí konfigurace.
3.  Definujte názvosloví konfigurace pro komponenty nebo kusovníky, které budou použity ke konfiguraci variant produktu.

Můžete také vytvořit názvosloví pro názvy variant produktů. Názvy variant produktů lze nakonfigurovat tak, aby zahrnovaly ID nebo název konfigurace.

### <a name="example-for-constraint-based-configurations"></a>Příklad konfigurací založených na omezeních

V tomto příkladu můžete používat číslo varianty produktu, která se skládá z následujících segmentů:

1.  Číslo základního produktu
2.  Textová konstanta "\_"
3.  Konfigurace

Názvosloví konfigurace sestává z následujících segmentů:

1.  Hodnota atributu: materiál
2.  Textová konstanta: "AAA"
3.  Hodnota atributu: délka

Pro segmenty můžete zadat následující hodnoty:

-   Číslo základního produktu = **M0099**
-   Materiál = **plast**
-   Délka = **12**

V tomto případě bude číslo varianty produktu M0099\_PlasticAAA12.

### <a name="example-for-dimension-based-configurations"></a>Příklad konfigurací založených na dimenzích

V tomto příkladu můžete používat číslo varianty produktu, která se skládá z následujících segmentů:

1.  Číslo základního produktu
2.  Textová konstanta: "//"
3.  Konfigurace

Názvosloví konfigurace sestává z následujících segmentů:

1.  Skupina konfigurace: Skříň
2.  Textová konstanta: "&"
3.  Skupina konfigurace: Přední mřížka

Pro segmenty můžete zadat následující hodnoty:

-   Číslo základního produktu = **D0123**
-   Skříň = **M0008**
-   Přední mřížka = **M0022**

V tomto případě bude číslo varianty produktu D0123//M0008&M0022.

## <a name="numbering-conflicts"></a>Číslování konfliktů
V některých případech nemusí názvosloví čísel variant produktů, které nastavíte, vytvářet čísla variant jedinečných produktů. Čísla nebudou jedinečná například, když jedna aktivní dimenze produktu není součástí názvosloví pro základní produkt využívající technologii konfigurace předem definované varianty. Způsob, kterým budete řešit konflikty je různý, podle technologie konfigurace.

### <a name="predefined-variants"></a>Předem definované varianty

Pokud se pokusíte automaticky nebo ručně vytvořit varianty produktu, kde jeden nebo více končí stejným číslem varianty produktu, dojde k chybě. Této situaci se lze vyhnout tak, že budete ve skupině dimenzí produktu používat všechny aktivní dimenze produktu. Alternativně zahrňte číselnou řadu, což vám pomůže zaručit jedinečnost čísel variat produktu.

### <a name="constraint-based-configurations"></a>Konfigurace založené na omezeních

V závislosti na názvosloví se systém může pokusit přiřadit nejedinečné číslo varianty produktu ke konfiguraci. V takovém případě systém používá číselnou řadu pro konfigurační dimenzi jako číslo varianty produktu. V takovém případě bude zobrazena varovná zpráva. Této situaci se lze vyhnout tak, že do názvosloví zahrnete dostatek produktů, které pomohou zaručit jedinečná čísla variant produktu. Měli byste také zajistit, že je pro komponentu zapnutá možnost **Opakované použití**.

### <a name="dimension-based-configurations"></a>Konfigurace založené na dimenzích

Během jednoho kroku procesu konfigurace systém navrhne hodnotu konfigurace podle klasifikace. V tomto kroku můžete ručně změnit hodnotu konfigurace. Po uložení konfigurace systém zkontroluje, zda je hodnota konfigurace jedinečná. Není-li hodnota, kterou jste zadali jedinečná, zobrazí se chybová zpráva. Chcete-li uložit konfiguraci, musíte zadat jedinečnou hodnotu konfigurace.

<a name="see-also"></a>Viz také
--------

[Vytvoření názvosloví čísel produktů pro předdefinované varianty produktu](tasks/create-product-number-nomenclature-predefined-variants-2016-11.md)

[Vytvoření názvosloví čísel produktů pro nakonfigurované varianty produktu](tasks/create-product-number-nomenclature-product-variants_2016_11.md)


