---
title: Vytvoření mezipodnikového plánu
description: Tato procedura ukazuje, jak vytvořit mezipodnikový plán.
author: ChristianRytt
ms.date: 08/13/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ReqIntercompanyPlanningGroupSetup,  ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7ef1484e6925427454f819a5effdc911f762b48b
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/29/2021
ms.locfileid: "7578265"
---
# <a name="create-an-intercompany-plan"></a>Vytvoření mezipodnikového plánu

[!include [banner](../../includes/banner.md)]

Tato procedura ukazuje, jak vytvořit mezipodnikový plán. K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.

## <a name="set-up-an-intercompany-planning-group"></a>Nastavení skupiny mezipodnikového plánování

1. V **navigačním podokně** přejděte na **Modules > Hlavní plánování > Nastavení > Skupiny mezipodnikového plánování**.
2. Použijte rychlý filtr pro hledání záznamů. Můžete například filtrovat v poli Jméno pomocí hodnoty „10“.
3. Označte na seznamu vybraný řádek.
4. Zvolte **Odstranit**. Tento krok je nezbytný pro účely zkrácení mezipodnikového plánování.   Mezipodnikové plánování spustí hlavní plánování ve všech společnostech ve skupině plánování, počínaje nejnižší sekvencí plánování.  
5. Vyberte **Ano**.
6. Zavřete stránku.

## <a name="create-an-intercompany-master-plan"></a>Vytvoření mezipodnikového hlavního plánu

1. V **navigačním podokně** přejděte na **Modules > Hlavní plánování > Pracovní prostory > Hlavní plánování**.
2. Vyberte **Mezipodnikové hlavní plánování**.  
3. V poli **Skupina mezipodnikového plánování** zvolením tlačítka rozevíracího seznamu otevřete vyhledávání.
4. Vyberte odkaz na vybraném řádku v seznamu. Vyberte skupinu 10 mezipodnikového plánování.  
5. V poli **Počet iterací mezipodnikového plánování** zadejte 2. Skupina 10 mezipodnikového plánování má dva členy. K rozšíření propagace zpoždění ze zdrojové společnosti (USMF) vůči společnosti zákazníka (DEMF) je třeba spustit dvakrát mezipodnikové plánování v obou společnostech dvakrát. První iterace bude rozšiřovat poptávku a identifikovat zpoždění ve zdrojové společnosti (USMF). Druhá iterace rozšíří zpoždění z USMF na DEMF.  
6. V poli **První iterace** vyberte Obnovení.
7. V poli **Další iterace** vyberte "Regenerace".
8. Do pole **Počet vláken** zadejte číslo. To představuje počet paralelních podprocesů použitých pro plánování.  
9. Vyberte **OK**.

## <a name="view-the-result-of-the-plan"></a>Zobrazení výsledku plánování

1. V poli **Plán** zvolením tlačítka rozevíracího seznamu otevřete vyhledávání.
2. Vyberte odkaz na vybraném řádku v seznamu. Vyberte odkaz pro StaticPlan. Musíte být ve společnosti USMF.  
3. Vyberte **Plánované objednávky**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]