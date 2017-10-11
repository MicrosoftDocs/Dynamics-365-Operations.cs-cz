--- 
title: "Vytvoření základní prognózy"
description: "Plánovač výroby může vytvořit základní prognózu pomocí modelů prognózování časových řad nebo zkopírováním historické poptávky."
author: YuyuScheller
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: c94a9766319531bd8285cca04003225709ce2113
ms.contentlocale: cs-cz
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-baseline-forecast"></a>Vytvoření základní prognózy

[!include[task guide banner](../../includes/task-guide-banner.md)]

Plánovač výroby může vytvořit základní prognózu pomocí modelů prognózování časových řad nebo zkopírováním historické poptávky. Tento postup popisuje, jak zkopírováním historické poptávky vytvořit základní prognózu pro všechny produkty použitím jednoho alokačního klíče položky. 


## <a name="set-up-an-item-allocation-key"></a>Nastavení alokačního klíče
1. Přejděte na Hlavní plánování > Nastavení > Skupiny mezipodnikového plánování.
2. Použijte rychlý filtr pro hledání záznamů. Můžete například filtrovat v poli Jméno pomocí hodnoty „10“.
    * Prognóza poptávky se provádí mezi právnickými osobami. Proto je nutné nastavit všechny společnosti, pro které chcete vygenerovat prognózy v jedné skupině mezipodnikového plánování.  
3. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
4. Klikněte na Alokační klíče položek.
    * Vyberte všechny alokační klíče položky, pro které chcete vytvořit prognózy.  
5. Označte v seznamu vybraný řádek.
    * Vyberte alokační klíč položky D_Aloc.  
6. Klepněte na >.
7. Zavřete stránku.
8. Zavřete stránku.

## <a name="set-up-the-demand-forecasting-paramters"></a>Nastavení parametrů prognózy poptávky
1. Přejděte na Hlavní plánování > Nastavení > Prognóza poptávky > Parametry tvorby prognóz poptávky.
2. Rozbalte část Parametry algoritmu prognózy.
3. V poli Strategie generování prognózy vyberte "Kopírování mezi historickými poptávkami".
4. Klikněte na položku Uložit.

## <a name="create-a-baseline-forecast"></a>Vytvoření základní prognózy
1. Přejděte na Hlavní plánování > Prognózování > Prognóza poptávky > Generovat statistickou základní prognózu.
2. Zadejte datum do pole Od data.
    * Pokud prodejní objednávky začínají od 1. ledna 2015, zadejte toto datum. V opačném případě zadejte nejdřívější datum prodejních objednávek.  
3. Do pole Do data zadejte datum.
    * Zadejte poslední datum prodejních objednávek (např. '2015-03-31').  
4. Zadejte datum do pole Od data.
    * Zadejte '2015-04-01'. Toto datum se vypočítá automaticky jako počáteční datum následujícího intervalu prognózy.  
5. Rozbalte oddíl Záznamy k zahrnutí.
6. Klepněte na tlačítko Filtr.
7. Označte v seznamu vybraný řádek.
    * Označte řádek, kde pole = skupina mezipodnikového plánování.  
8. Zadejte hodnotu do pole Kritéria.
    * Zadejte skupinu vnitropodnikového plánování, například „10“, kterou používáte v prvním úkolu.  
9. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
    * Vyberte řádek, kde pole = alokační klíč položky.  
10. Zadejte hodnotu do pole Kritéria.
11. Klikněte na tlačítko OK.
12. Rozbalte sekci Rozšířené parametry.
13. V poli Interval prognózy vyberte Měsíc.
14. V poli Horizont prognózy zadejte „3“.
15. V poli Ochranná doba zablokování zadejte číslo 1.
16. Klikněte na tlačítko OK.

## <a name="visualize-the-demand-forecast"></a>Vizualizace prognózy poptávky
1. Přejděte na Hlavní plánování > Prognózování > Prognóza poptávky > Upravená prognóza poptávky.
2. V tabulce agregovaného zobrazení vyberte buňku na řádku 1, ve sloupci 2. Jedná se o druhé měsíc, pro který jste vytvořili prognózu.
3. Nastavte QtyCell na '400'.
    * V buňce zadejte jiné číslo než to, který bylo předvídáno, například 400.  
4. Právě jste provedli ruční úpravu prognózy. Všimněte si grafické indikace v dalším kroku.
5. Klikněte na Podrobnosti o řádcích prognózy.
    * Na této stránce můžete zobrazit hodnoty přesnosti, historické poptávky a prognózu. Podle potřeby můžete upravit také prognózu.  

