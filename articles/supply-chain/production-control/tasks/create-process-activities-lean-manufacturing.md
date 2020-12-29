---
title: Vytváření aktivit procesu pro lean manufacturing
description: Vytvořte aktivitu procesu pro lean manufacturing.
author: cvocph
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityWizard, LeanWorkCellLookup, InventLocationIdLookup, PlanActivityDetails, KanbanJobPickingListPart
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3cb096eb25fa449b521c370bcb1677e38e399658
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4423530"
---
# <a name="create-process-activities-for-lean-manufacturing"></a>Vytváření aktivit procesu pro lean manufacturing

[!include [banner](../../includes/banner.md)]

Vytvořte aktivitu procesu pro lean manufacturing. 

Požadavky: 

1. Je nutné vytvořit výrobní tok a verzi, která není aktivní.

2. Musí být vytvořena pracovní buňka.


## <a name="find-the-production-flow-version"></a>Najděte verzi výrobního toku
1. Přejděte na Řízení výroby > Nastavení > Tok štíhlé výroby > Výrobního toky.
2. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
3. Klikněte na odkaz na vybraném řádku v seznamu.

## <a name="create-a-new-activity"></a>Vytvořte novou aktivitu
1. Klepněte na aktivity.
    * Ujistěte se, že vybraný výrobní tok má verzi v konceptu a tuto verzi vyberte.  
2. Klepněte na Vytvořit novou aktivitu plánu.
3. Klepněte na tlačítko Další.
4. Zadejte hodnotu do pole Název.
5. Zadejte hodnotu do pole Název.
    * Nezapomeňte, že název musí být jedinečný pro všechny verze daného výrobního toku.  
6. V poli Množství procesu zadejte číslo.
    * Všimněte si, že bez ohledu na to, jaké množství úloh bude zpracováno, toto je minimální množství na úlohu pro výpočet nákladů na práci. Pokud se množství úlohy liší od tohoto množství, bude vytvořena odchylka nákladů práce.  
7. Klepněte na tlačítko Další.

## <a name="select-the-work-cell"></a>Vyberte pracovní buňku
1. V poli Pracovní buňka kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
2. Klikněte na odkaz na vybraném řádku v seznamu.

## <a name="define-the-inventory-updates"></a>Definujte aktualizace zásob
1. Zaškrtněte políčko Aktualizovat příjem na skladě nebo jeho zaškrtnutí zrušte.
    * Pokud hodnota Aktualizovat zásoby na skladě = Ne, můžete definovat aktivity pro příjem polotovaru (aktivita nedosáhne další úrovně kusovníku).    Můžete vybrat také využívání polotovarů.  

## <a name="define-the-picking-activities"></a>Definujte aktivity výdeje
1. Klepněte na tlačítko Další.
2. Označte v seznamu vybraný řádek.
    * Je vytvořena výchozí aktivita pro vstupní místo vybrané pracovní buňky.  
3. Klepněte na možnost Přidat.
    * Můžete vytvořit další aktivity výdeje pro konkrétní produkty, které nejsou rozfázovány ve vstupní aktivitě pracovní buňky.  
4. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
5. Zadejte hodnotu do pole Číslo zboží.
6. V poli Sklad kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
    * S touto definicí všechny materiály spotřebovávány při aktivitě jsou vydány z výchozího vstupního skladu a skladového místa s výjimkou položky, která je definována v druhé aktivitě výdeje. Tato položka bude vydána z jiného skladu a umístění.  
7. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
8. Klikněte na odkaz na vybraném řádku v seznamu.
9. Zaškrtněte políčko Registrovat odpad nebo jeho zaškrtnutí zrušte.
10. Klepněte na tlačítko Další.

## <a name="define-the-activity-times"></a>Definujte čas aktivity
1. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
    * Je požadována definice modulu Runtime. Modul Runtime se používá k výpočtu nákladů a doby propustnosti kanbanových úloh. Moduly Runtime nejsou používány k výpočtu vytížení kapacity a spotřeby, to je počítáno podle času cyklu, odvozeného z úlohy verze výrobního toku.  
2. Do pole Čas zadejte číslo.
3. Zadejte hodnotu do pole Jednotka.
4. Vyberte jednotku času.
5. V poli Podle množství zadejte číslo.
6. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
    * Časy čekání jsou volitelné.  
7. Do pole Čas zadejte číslo.
8. Zadejte hodnotu do pole Jednotka.
9. Vyberte jednotku času.
10. V poli Podle množství zadejte číslo.
11. Klepněte na tlačítko Další.
12. Klepněte na tlačítko Dokončit.
13. Zavřete stránku.

