--- 
title: "Vytvoření mezipodnikového plánu"
description: "Tato procedura ukazuje, jak vytvořit mezipodnikový plán."
author: YuyuScheller
manager: AnnBe
ms.date: 11/11/2016
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
ms.openlocfilehash: 7c7f466add55fb9a24c3fb8f1f92df712a8622e3
ms.contentlocale: cs-cz
ms.lasthandoff: 07/27/2017

---
# <a name="create-an-intercompany-plan"></a>Vytvoření mezipodnikového plánu

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tato procedura ukazuje, jak vytvořit mezipodnikový plán. K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.


## <a name="set-up-an-intercompany-planning-group"></a>Nastavení skupiny mezipodnikového plánování 
1. Přejděte na Skupiny mezipodnikového plánování.
    * Hlavní plánování > Nastavení > Skupiny mezipodnikového plánování  
2. Použijte rychlý filtr pro hledání záznamů. Můžete například filtrovat v poli Jméno pomocí hodnoty „10“.
3. Označte v seznamu vybraný řádek.
4. Klepněte na tlačítko Odstranit.
    * Tento krok je nezbytný pro účely zkrácení mezipodnikového plánování.   Mezipodnikové plánování spustí hlavní plánování ve všech společnostech ve skupině plánování, počínaje nejnižší sekvencí plánování.  
5. Klepněte na tlačítko Ano.
6. Zavřete stránku.

## <a name="create-an-intercompany-plan"></a>Vytvoření mezipodnikového plánu
1. Klikněte na Mezipodnikové hlavní plánování.
    * Jedná se o pracovní prostor hlavního plánování.  
2. V poli Skupina mezipodnikového plánování kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
3. Klikněte na odkaz na vybraném řádku v seznamu.
    * Vyberte skupinu 10 mezipodnikového plánování.  
4. V poli Počet iterací mezipodnikového plánování zadejte 2.
    * Skupina 10 mezipodnikového plánování má dva členy. K rozšíření propagace zpoždění ze zdrojové společnosti (USMF) vůči společnosti zákazníka (DEMF) je třeba spustit dvakrát mezipodnikové plánování v obou společnostech dvakrát. První iterace bude rozšiřovat poptávku a identifikovat zpoždění ve zdrojové společnosti (USMF). Druhá iterace rozšíří zpoždění z USMF na DEMF.  
5. Vyberte volbu v poli První iterace.
6. V poli První iterace vyberte Obnovení.
7. V poli Další iterace vyberte "Regenerace".
8. Do pole Počet vláken zadejte číslo.
    * To představuje počet paralelních podprocesů použitých pro plánování.  
9. Klikněte na tlačítko OK.

## <a name="view-the-result-of-the-plan"></a>Zobrazení výsledku plánování
1. V poli Plán kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
2. Klikněte na odkaz na vybraném řádku v seznamu.
    * Klepněte na odkaz StaticPlan. Musíte být ve společnosti USMF.  
3. Klikněte na Plánované objednávky.

