---
title: Vytvoření základní prognózy
description: Plánovač výroby může vytvořit základní prognózu pomocí modelů prognózování časových řad nebo zkopírováním historické poptávky.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqIntercompanyPlanningGroupSetup, ReqIntercompanyPlanningGroupAllocKeys, ReqDemPlanForecastParameters, ReqDemPlanCreateForecastDialog, SysQueryForm, ReqDemPlanForecastViewer
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f777503c6161376afc933322b5d60054e2468b34
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4983409"
---
# <a name="create-a-baseline-forecast"></a>Vytvoření základní prognózy

[!include [banner](../../includes/banner.md)]

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

## <a name="set-up-the-demand-forecasting-parameters"></a>Nastavení parametrů prognózy poptávky
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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]