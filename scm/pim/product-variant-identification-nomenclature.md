---
title: "Produkt číslo nomenklatury"
description: "Toto téma popisuje, jak lze nastavit číslo klasifikace výrobků nahradit pevný formát [produktu předlohy - konfigurace - velikost - Barva - Styl číslování], cílené formátem, který obsahuje číslo hlavního produktu, aktivní dimenze produktu a oddělovače textu dle vašeho výběru. Můžete také vytvořit názvosloví k identifikaci konfigurací, které jsou vytvořeny konfigurátorem produktu založeném na omezeních. Tato názvosloví můžou obsahovat atributy podle vašeho výběru."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: EcoResNomenclature, EcoResProductDimensionGroup, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelDetails
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 220104
ms.assetid: 31c9efb4-b5f6-4af3-b884-8f1e128469bd
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: 58afcd62e7ef317e624fd26d198c2606bf53e6a5
ms.lasthandoff: 03/31/2017


---

# <a name="product-number-nomenclature"></a>Produkt číslo nomenklatury

[!include[banner](../includes/banner.md)]


Toto téma popisuje, jak lze nastavit číslo klasifikace výrobků nahradit pevný formát [produktu předlohy - konfigurace - velikost - Barva - Styl číslování], cílené formátem, který obsahuje číslo hlavního produktu, aktivní dimenze produktu a oddělovače textu dle vašeho výběru. Můžete také vytvořit názvosloví k identifikaci konfigurací, které jsou vytvořeny konfigurátorem produktu založeném na omezeních. Tato názvosloví můžou obsahovat atributy podle vašeho výběru.

Nové názvosloví čísel variant produktu vám umožňuje zahrnout segmenty do identifikátorů variant produktu. Tyto segmenty mohou obsahovat číslo hlavního produktu, dimenze produktu, číselné řady, konstanty textu a atributy. Tato funkce umožňuje rychle najít konkrétní variantu produktu, když vytváříte nákupní nebo prodejní objednávku.

## <a name="nomenclature-of-predefined-product-variants"></a>Názvosloví předdefinovaných variant produktu
Varianty produktu jsou generovány pro hlavní produkty podle jedné ze tří technologií konfigurace:

-   Předem definované varianty
-   Založené na omezeních
-   Založené na dimenzi

Každá varianta produktu má číslo a názvosloví identifikace variant produktu umožňuje vybrat segmenty, které budou zahrnuty do každého čísla varianty produktu. Můžete vybrat následující segmenty na stránce **Názvosloví produktu**.

-   Číslo základního produktu
-   Hodnota číselné řady
-   Textová konstanta
-   Dimenze produktu
    -   Konfigurace
    -   Barva
    -   Velikost
    -   Styl

Po definování názvosloví identifikace varianty produktu může být produkt přidružen ke skupině dimenzí produktu. Produkty odkazování na tuto skupinu dimenzí produktu v důsledku toho budou přiřazena čísla variant produktů podle klasifikace. Také je možné přiřadit názvosloví identifikace varianty produktu přímo hlavnímu produktu. V takovém případě budou variantám produktu náležejícím tomuto hlavnímu produktu přiřazena čísla varianty produktu dle daného názvosloví.

### <a name="example"></a>Příklad

Tričko (TS1234) se vyrábí ve 3 různých velikostech (S, M, L), 4 různých barvách (červená, zelená, modrá, žlutá) a 2 stylech (Polo, V), což dohromady tvoří celkový počet 24 variant produktu. Názvosloví identifikace variant produktů je vytvořeno s následujícími segmenty:

1.  Číslo základního produktu
2.  Textová konstanta: '-'
3.  Barva
4.  Textová konstanta: '-'
5.  Velikost
6.  Textová konstanta: '-'
7.  Styl

Číslo varianty produktu pro červené, malé, Polo bude: TS1234 červená-malá-Polo.

## <a name="nomenclature-of-constraintbased-configurations"></a>Klasifikace constraintbased konfigurace
Pro omezení na základě konfigurace mohou být sestaveny vyhrazené nomenklatury pro konfigurační dimenze produktu. Můžete vybrat následující segmenty na stránce **Názvosloví produktu**.

-   Hodnota číselné řady
-   Textová konstanta
-   Hodnota atributu 

Jednotlivé komponenty v modelu konfigurace produktu můžou mít vlastní názvosloví konfigurace. Lze použít pouze atributy, které patří ke komponentě. Nejsou k dispozici atributy z dílčích komponent nebo požadavky uživatelů.

### <a name="example"></a>Příklad

Model konfigurace produktu má kořenovou komponentu se dvěma atributy.

-   Materiál (plast, dřevo, ocel.)
-   Délka (10... 100)

Názvosloví konfigurace je definováno pomocí následujících segmentů:

1.  Hodnota atributu: materiál
2.  Textová konstanta: 'AAA'
3.  Hodnota atributu: délka

ID konfigurace pro dřevěný materiál o délce 78 bude mít následující ID konfigurace: WoodAAA78.

## <a name="nomenclature-of-dimensionbased-configurations"></a>Klasifikace dimensionbased konfigurace
Pro konfigurace založené na dimenzích mohou být sestaveny vyhrazené nomenklatury pro konfigurační dimenze produktu. Můžete vybrat následující segmenty na stránce **Názvosloví produktu**.

-   Hodnota číselné řady
-   Textová konstanta
-   Položka konfigurační skupiny

Názvosloví konfigurace lze definovat pro kusovníky (BOM).

### <a name="example"></a>Příklad

Kusovník má 4 řádky, které jsou rozděleny do 2 konfiguračních skupin.

-   Řádek kusovníku: M0007, standardní skříň
    -   Skupina konfigurace: Skříň
-   Řádek kusovníku: M0008, vysoká koncová skříň
    -   Skupina konfigurace: Skříň
-   Řádek kusovníku: M0021, přední potah mřížky
    -   Skupina konfigurace: Přední mřížka
-   Řádek kusovníku: M0022, přední kovová mřížka
    -   Skupina konfigurace: Přední mřížka

Názvosloví konfigurace je definováno pomocí následujících segmentů:

1.  Skupina konfigurace: Skříň
2.  Textová konstanta: '&'
3.  Skupina konfigurace: Přední mřížka

ID souboru s mřížkou účtované na látkový standardních bude konfigurace: M0007 & M0021.

## <a name="nomenclature-of-a-combination-of-product-variants-and-configurations"></a>Názvosloví kombinace variant a konfigurací produktu
Při použití technologie konfigurace založené na omezeních nebo založené na dimenzích ke konfiguraci variant produktu pro základní produkt mohou varianty produktu získat čísla variant produktu, zahrnující názvosloví z konfigurační dimenze. Chcete-li nakonfigurovat varianty, postupujte takto:

1.  Definujte názvosloví čísel variant produktů, které zahrnuje konfigurační dimenzi na stránce **Klasifikace produktu**.
2.  Toto názvosloví přiřaďte skupině dimenze produktu s dimenzí konfigurace.
3.  Definujte názvosloví konfigurace pro komponenty nebo kusovníky, které budou použity ke konfiguraci variant produktu.

### <a name="example-for-constraint-based-configurations"></a>Příklad konfigurací založených na omezeních

V tomto příkladu můžete používat číslo varianty produktu, která se skládá z následujících segmentů:

1.  Číslo základního produktu
2.  Textová konstanta "\_"
3.  Konfigurace

Názvosloví konfigurace může sestávat z následujících segmentů:

1.  Hodnota atributu: materiál
2.  Textová konstanta: 'AAA'
3.  Hodnota atributu: délka

Pro segmenty můžete zadat následující hodnoty:

-   Číslo základního produktu = M0099
-   Materiál = plast
-   Délka = 12

Číslo varianty produktu se změní na: M0099\_PlasticAAA12.

### <a name="example-for-dimension-based-configurations"></a>Příklad konfigurací založených na dimenzích

V tomto příkladu můžete používat číslo varianty produktu, která se skládá z následujících segmentů:

1.  Číslo základního produktu
2.  Textová konstanta: '//'
3.  Konfigurace

Názvosloví konfigurace může sestávat z následujících segmentů:

1.  Skupina konfigurace: Skříň
2.  Textová konstanta: '&'
3.  Skupina konfigurace: Přední mřížka

Pro segmenty můžete zadat následující hodnoty:

-   Číslo základního produktu = D0123
-   Skříň = M0008
-   Přední mřížka = M0022

Číslo varianty produktu bude: D0123//M0008&M0022.

## <a name="numbering-conflicts"></a>Číslování konfliktů
Je možné nastavit názvosloví čísel variant produktů, které nevytvoří čísla variant jedinečných produktů. K tomu může dojít například, když jedna aktivní dimenze produktu není součástí názvosloví pro základní produkt využívající technologii konfigurace předem definované varianty. Konflikty jsou zvládány různě pro různé technologie konfigurace.

### <a name="predefined-variants"></a>Předem definované varianty

Pokud se pokusíte automaticky nebo ručně generovat varianty produktu, kde jeden nebo více končí stejným číslem varianty produktu, dojde k chybě. Aby k tomu nedošlo, použijte všechny aktivní dimenze produktu ve skupině dimenzí produktu, nebo zahrňte číselnou řadu pro zajištění jedinečnosti variant čísel produktů.

### <a name="constraint-based-configurations"></a>Konfigurace založené na omezeních

V závislosti na názvosloví se systém může pokusit přiřadit nejedinečné číslo varianty produktu ke konfiguraci. V tomto případě systém použije číselnou řadu pro konfigurační dimenze jako číslo varianty produktu. Pokud k tomu dojde, zobrazí se upozornění. Aby k tomu nedošlo, je třeba zahrnout dostatek atributů do názvosloví pro zajištění jedinečnosti a zajistit, aby byla volba **Opakovaně** zapnuta pro komponentu.

### <a name="dimension-based-configurations"></a>Konfigurace založené na dimenzích

Proces konfigurace zahrnuje krok, ve kterém systém navrhne hodnotu konfigurace podle klasifikace. V tomto kroku můžete ručně změnit hodnotu konfigurace. Po uložení konfigurace systém nejprve zkontroluje, zda je hodnota konfigurace jedinečná. V opačném případě se zobrazí chyba. Chcete-li uložit konfiguraci, musíte zadat jedinečnou hodnotu konfigurace.



<a name="see-also"></a>Viz také
--------

[Vytvořit číselné klasifikace výrobků pro varianty produktu předdefinované (úkol guide)](http://ax.help.dynamics.com/en/wiki/create-a-product-number-nomenclature-for-predefined-product-variants/)

[Vytvořit číselné klasifikace výrobků pro varianty produktu nakonfigurované (úkol guide)](http://ax.help.dynamics.com/en/wiki/create-a-product-number-nomenclature-for-configured-product-variants/)




