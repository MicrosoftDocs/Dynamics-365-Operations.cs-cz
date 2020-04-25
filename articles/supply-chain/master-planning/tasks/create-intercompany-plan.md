---
title: Vytvoření mezipodnikového plánu
description: Tato procedura ukazuje, jak vytvořit mezipodnikový plán.
author: ShylaThompson
manager: tfehr
ms.date: 08/13/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqIntercompanyPlanningGroupSetup,  ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3a64817f140d8a2302b3b2c2d1e55de103a5bb36
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/02/2020
ms.locfileid: "3209690"
---
# <a name="create-an-intercompany-plan"></a>Vytvoření mezipodnikového plánu

[!include [banner](../../includes/banner.md)]

Tato procedura ukazuje, jak vytvořit mezipodnikový plán. K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.


## <a name="set-up-an-intercompany-planning-group"></a>Nastavení skupiny mezipodnikového plánování 
1. V **navigačním podokně** přejděte na **Modules > Hlavní plánování > Nastavení > Skupiny mezipodnikového plánování**. 
2. Použijte rychlý filtr pro hledání záznamů. Můžete například filtrovat v poli Jméno pomocí hodnoty „10“.
3. Označte v seznamu vybraný řádek.
4. Klepněte na tlačítko **Odstranit**. Tento krok je nezbytný pro účely zkrácení mezipodnikového plánování.   Mezipodnikové plánování spustí hlavní plánování ve všech společnostech ve skupině plánování, počínaje nejnižší sekvencí plánování.  
5. Klepněte na tlačítko **Ano**.
6. Zavřete stránku.

## <a name="create-an-intercompany-plan"></a>Vytvoření mezipodnikového plánu
1. V **navigačním podokně** přejděte na **Modules > Hlavní plánování > Pracovní prostory > Hlavní plánování**.
2. Klikněte na **Mezipodnikové hlavní plánování**.  
3. V poli **Skupina mezipodnikového plánování** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
4. Klikněte na odkaz na vybraném řádku v seznamu. Vyberte skupinu 10 mezipodnikového plánování.  
5. V poli **Počet iterací mezipodnikového plánování** zadejte 2. Skupina 10 mezipodnikového plánování má dva členy. K rozšíření propagace zpoždění ze zdrojové společnosti (USMF) vůči společnosti zákazníka (DEMF) je třeba spustit dvakrát mezipodnikové plánování v obou společnostech dvakrát. První iterace bude rozšiřovat poptávku a identifikovat zpoždění ve zdrojové společnosti (USMF). Druhá iterace rozšíří zpoždění z USMF na DEMF.  
6. V poli **První iterace** vyberte Obnovení.
7. V poli **Další iterace** vyberte "Regenerace".
8. Do pole **Počet vláken** zadejte číslo. To představuje počet paralelních podprocesů použitých pro plánování.  
9. Klikněte na tlačítko **OK**.

## <a name="view-the-result-of-the-plan"></a>Zobrazení výsledku plánování
1. V poli **Plán** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
2. Klikněte na odkaz na vybraném řádku v seznamu. Klepněte na odkaz StaticPlan. Musíte být ve společnosti USMF.  
3. Klikněte na **Plánované objednávky**.

