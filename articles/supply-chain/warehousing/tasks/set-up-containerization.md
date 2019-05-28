---
title: Nastavení vytváření kontejnerů
description: Tento postup popisuje postup automatizace vytváření kontejnerů vytížení v modulu Řízení skladu.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWaveTemplateTable, InventLocationIdLookup, WHSContainerType, WHSContainerGroup, WHSContainerizationTable, WHSContainerizationBreak, WHSCreateContainerBreak
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 56fc6adc2a0eeb5b824089ff4b1b781f3a99a34c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1558049"
---
# <a name="set-up-containerization"></a>Nastavení vytváření kontejnerů

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tento postup popisuje postup automatizace vytváření kontejnerů vytížení v modulu Řízení skladu. Automatické vytváření kontejnerů vytvoří kontejnery a výdejovou práci pro dodávky při zpracování vlny, a řádky práce lze rozdělit na množství, které se vejde do kontejnerů. To pomáhá pracovníkům skladu vyzvednout položky přímo do zvoleného kontejneru. Ve srovnání s procesem ručního balení jsou úlohy, jako je vytváření kontejnerů, přiřazování položek nebo uzavření kontejnerů automatizované systémem. Tento postup používá ukázkovou společnost USMF a provádí jej vedoucí skladu.


## <a name="set-up-a-wave-template"></a>Nastavení šablony vlny
1. Přejděte do nabídky Řízení skladu > Nastavení > Vlny > Šablony vlny.
2. Klikněte na položku Nová.
3. Zadejte hodnotu do pole Název šablony vlny.
4. Zadejte hodnotu do pole Popis šablony vlny.
5. V poli Lokalita zadejte nebo vyberte hodnotu.
6. V poli Sklad zadejte nebo vyberte hodnotu.
7. Rozbalte sekci Způsoby.
    * Podokno Vybrané metody bude obsahovat metody pro vybraný typ šablony vlny. Šablona vlny musí zahrnovat metodu rozdělení do kontejnerů.  
8. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
9. Zadejte hodnotu do pole Kód kroku vlny.
    * Zadejte kód kroku vlny pro přidaný způsob, který může být tvořen libovolným kódem. Je možné přidat metodu vícekrát a přiřadit různé kódy kroku vlny. K tomu vyberte na stránce Metody zpracování vlny možnost Opakovatelné pro tuto metodu.  
10. Klikněte na položku Uložit.
11. Zavřete stránku.

## <a name="set-up-a-container-type"></a>Nastavení typu kontejneru
1. Přejděte na Řízení skladu > Nastavení > Kontejnery > Typy kontejnerů.
    * Kontejnery můžete definovat na stránce Typy kontejneru. Můžete konfigurovat fyzické dimenze kontejnerů, včetně hmotnosti obalu, maximální hmotnosti, maximálního objemu, délky, šířky a výšky. V tomto příkladu máme tři různé velikosti balení.  
2. Klikněte na položku Nová.
3. Zadejte hodnotu do pole Typ kódu kontejneru.
4. V poli Váha obalu zadejte číslo.
5. Zadejte číslo do pole Maximální hmotnost.
6. V poli Objem zadejte číslo.
7. Do pole Délka zadejte číslo.
8. V poli Šířka zadejte číslo.
9. V poli Výška zadejte číslo.
10. Zadejte nějakou hodnotu do pole Popis.
11. Klikněte na položku Uložit.
12. Klikněte na položku Nová.
13. Zadejte hodnotu do pole Typ kódu kontejneru.
14. Zadejte nějakou hodnotu do pole Popis.
15. V poli Váha obalu zadejte číslo.
16. Zadejte číslo do pole Maximální hmotnost.
17. V poli Objem zadejte číslo.
18. Do pole Délka zadejte číslo.
19. V poli Šířka zadejte číslo.
20. V poli Výška zadejte číslo.
21. Klikněte na položku Uložit.
22. Klikněte na položku Nová.
23. Zadejte hodnotu do pole Typ kódu kontejneru.
24. Zadejte nějakou hodnotu do pole Popis.
25. V poli Váha obalu zadejte číslo.
26. Zadejte číslo do pole Maximální hmotnost.
27. V poli Objem zadejte číslo.
28. Do pole Délka zadejte číslo.
29. V poli Šířka zadejte číslo.
30. V poli Výška zadejte číslo.
31. Klikněte na položku Uložit.
32. Zavřete stránku.

## <a name="set-up-a-container-group"></a>Nastavení skupin kontejneru
1. Přejděte na Řízení skladu > Nastavení > Kontejnery > Skupiny kontejnerů.
2. Klikněte na položku Nová.
    * Můžete nastavit skupiny kontejnerů logických skupin. Pro každou skupinu můžete určit pořadí, v němž mají být zabaleny kontejnery a procento zaplnění kontejnerů. Dimenze velikosti se používá k určení, zda bude pasovat do kontejneru. Použije se kontejner, který nejlépe odpovídá dimenzím velikosti. Pokud máte více typů kontejnerů ve skupině, doporučujeme, abyste uspořádali pořadí podle velikosti tak, aby největší kontejner byl první (číslo 1 v číselné řadě) a nejmenší kontejner byl poslední.    
3. Zadejte hodnotu do pole ID skupiny kontejnerů.
4. Zadejte nějakou hodnotu do pole Popis.
5. Klepněte na možnost Nový.
6. Označte v seznamu vybraný řádek.
7. V poli Typ kontejneru zadejte nebo vyberte hodnotu.
8. Klepněte na možnost Nový.
9. Označte na seznamu vybraný řádek.
10. V poli Typ kontejneru zadejte nebo vyberte hodnotu.
11. Klepněte na možnost Nový.
12. Označte na seznamu vybraný řádek.
13. V poli Typ kontejneru zadejte nebo vyberte hodnotu.
14. Klikněte na položku Uložit.
15. Zavřete stránku.

## <a name="set-up-a-container-build-template"></a>Nastavení šablony sestavení kontejneru
1. Přejděte na Řízení skladu > Nastavení > Kontejnery > Šablony sestavení kontejneru.
2. Klikněte na položku Nová.
    * Šablona sestavení kontejneru je založena na tom, které procesy rozdělení do kontejnerů proběhnou. Každá šablona sestavení kontejneru definuje jeden proces rozdělení do kontejnerů, který šablona vlny použije. Možnosti Upravit dotaz umožňuje definovat podmínky, pro které budou vybrané šablony zpracovány. Například můžete spustit rozdělení do kontejnerů jen pro určité odběratele, produkty nebo sklady, nebo můžete přidat odpovídající rozsahy dotazu do šablony. Pole Kód kroku vlny popisuje, jak je šablona sestavení kontejneru propojena s kroky v šabloně vlny. Při spuštění vlny určuje, které šablony sestavení kontejneru se používají k zahájení rozdělení do kontejnerů. Pole Základní typy dotazů určuje, co bude zabaleno, a na čem založit dotaz filtru.  
3. Označte v seznamu vybraný řádek.
4. Zadejte hodnotu do pole ID šablony kontejneru.
5. V poli ID skupiny kontejnerů zadejte nebo vyberte hodnotu.
6. Zadejte hodnotu do pole Kód kroku vlny.
7. Zaškrtněte políčko Povolit rozdělení výdeje.
8. Klikněte na položku Uložit.
9. Klikněte na Omezení kombinování obsahu kontejnerů.
    * Přerušení smíšené logiky umožňuje nastavit pravidla pro řádky přidělení balení do kontejnerů. Například pokud chcete přidat pole Číslo položky, když jsou položky přiřazeny do kontejnerů, bude při vygenerování nového čísla položky vytvořen nový kontejner. To zabrání pracovníkům přibalit přidělovací řádky pro dva různé zákazníky do stejného kontejneru.  
10. Klikněte na položku Nová.
11. Vyberte volbu v poli Tabulka.
12. V poli Výběr pole zadejte nebo vyberte hodnotu.
13. Klikněte na tlačítko OK.

