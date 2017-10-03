--- 
title: "Vytvoření modelu konfigurace produktu"
description: "Tento postup popisuje způsob vytvoření modelu konfigurace produktu a zadání základních informací, jako například atributy a dílčí komponenty."
author: BibiSp
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: da8dd3bbc350c29ce1f7dc22ab3914dfee4b967c
ms.contentlocale: cs-cz
ms.lasthandoff: 07/28/2017

---
# <a name="create-a-product-configuration-model"></a>Vytvoření modelu konfigurace produktu

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tento postup popisuje způsob vytvoření modelu konfigurace produktu a zadání základních informací, jako například atributy a dílčí komponenty. K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.


## <a name="create-a-product-model"></a>Vytvoření modelu výrobku
1. Klepněte na Definice modelu varianty produktu.
2. Klepněte na Modely konfigurace produktu.
3. Klepněte na možnost Nový.
4. Zadejte hodnotu do pole Název.
5. Zadejte nějakou hodnotu do pole Popis.
6. Vyberte volbu v poli Strategie řešitele.
    * Strategie řešitele určuje způsob zpracování omezení v modelu konfigurace produktu založeného na omezeních. Tento výběr může mít vliv na výkon modelu konfigurace produktu.  
7. Zadejte hodnotu do pole Název.
    * Kořenová komponenta představuje model konfigurace produktu, ale lze ji použít také v jiných modelech výrobků.  
8. Klikněte na tlačítko OK.
9. V poli Znovu použít konfigurace vyberte možnost.
    * Je-li parametr opakovaného použití konfigurace nastaven na hodnotu Ano, systém zkontroluje v každé konfigurační relaci, zda byla nalezena identická konfigurace, a pokud byla nalezena přesná shoda, použije ji znovu.  

## <a name="add-attributes"></a>Přidat atributy
1. Rozbalte sekci Atributy.
2. Klepněte na možnost Přidat.
3. Označte v seznamu vybraný řádek.
4. Zadejte hodnotu do pole Název.
5. Do pole Název řešitele zadejte hodnotu.
    * Název řešitele je používán řešitelem omezení konfigurátoru výrobku. Nesmí obsahovat mezery ani speciální znaky kromě _ (podtržítko).  
6. Zadejte nějakou hodnotu do pole Popis.
    * Text popis se zobrazí uživateli konfigurace, a může proto sloužit jako pomoc při výběru správné hodnoty atributu.  
7. V poli Typ atributu zadejte nebo vyberte hodnotu.
    * Typ atributu určuje, které hodnoty jsou pro atribut k dispozici.  
8. Zaškrtněte políčko položky Zahrnout do opakovaného použití.
    * Tato možnost je k dispozici pouze v případě, že je vybrána možnost Znovu použít konfigurace. Zaškrtávací políčko Zahrnutí atributu do opětovného použití znamená, že tento atribut bude zvážen, když bude systém hledat přesnou shodu.  

## <a name="add-subcomponents"></a>Přidat dílčí komponenty
1. Rozbalte sekci Dílčí komponenty.
2. Klepněte na možnost Přidat.
3. Označte v seznamu vybraný řádek.
4. Zadejte hodnotu do pole Název.
5. Do pole Název řešitele zadejte hodnotu.
6. Zadejte nějakou hodnotu do pole Popis.
7. V poli Komponenty zadejte nebo vyberte hodnotu.
    * Každý dílčí komponent musí odkazovat na definici komponenty. Tento návrh podporuje opakované použití komponent a zajišťuje, že po definování komponenty ji je možné použít v mnoha modelech výrobků.  
8. Klikněte na položku Uložit.
9. Klepněte na podrobnosti řádku kusovníku.
    * Formulář Podrobnosti řádku Kusovníku umožňuje uživatelům vybrat požadované vlastnosti pro dílčí komponentu. Všechny vlastnosti mohou mít stanovenou pevnou hodnotu nebo namapovanou hodnotu k atributu. Mapování na atribut má za výsledek, že vlastnosti řádku kusovníku získají odlišné hodnoty v závislosti na výběru konfigurace.  
10. V poli Číslo zboží zadejte nebo vyberte hodnotu.
    * Každý dílčí představuje základní konfigurovatelný produkt s technologií konfigurace založenou na omezeních. Odkaz je vytvořen prostřednictvím čísla položky.  
11. Zaškrtněte políčko položky Nastavit.
12. Vyberte možnost Ano v poli Výpočet.
    * Možnost nastavení výpočtu zajišťuje, že výrobek bude zahrnut při spuštění výpočtu nákladů pro produkt.  
13. Klikněte na záložku Nastavení.
14. Zaškrtněte políčko položky Nastavit.
15. Zadejte číslo do pole Množství.
    * Pole množství určuje, kolik tohoto produktu bude spotřebováno v konfigurovaném produktu.  
16. Zaškrtněte políčko položky Nastavit.
17. V poli Podle sérií zadejte číslo.
18. Klikněte na tlačítko OK.


