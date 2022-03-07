---
title: Vytvoření kanbanového pravidla s použitím události pro minimální úroveň zásob
description: Tento postup se zaměřuje na nastavení potřebné k vytvoření kanbanového pravidlo pomocí události pro minimální úroveň zásob, aby tak bylo jisté, že bude konkrétní produkt v určitém místě vždy k dispozici.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, EcoResProductInformationDialog, EcoResProductDetailsExtended, ReqItemTable, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bd7e02a8a3bf62606c680dad91d46658775138df
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/29/2021
ms.locfileid: "7566616"
---
# <a name="create-a-kanban-rule-using-a-minimum-stock-event"></a>Vytvoření kanbanového pravidla s použitím události pro minimální úroveň zásob

[!include [banner](../../includes/banner.md)]

Tento postup se zaměřuje na nastavení potřebné k vytvoření kanbanového pravidlo pomocí události pro minimální úroveň zásob, aby tak bylo jisté, že bude konkrétní produkt v určitém místě vždy k dispozici. Je vytvořeno kanbanové pravidlo, které při poklesu úrovně zásob pod 200 kusů převede materiál do skladového místa. Spuštěním zpracování události požadavku dojde k vytvoření potřebných kanbanů. Tento úkol byl vytvořen pomocí ukázkových dat společnosti USMF. Tento úkol je určen pro technologa výrobních procesů nebo správce hodnotového proudu, kteří připravují výrobu nového nebo změněného výrobku v prostředí štíhlé výroby.


## <a name="create-a-new-kanban-rule"></a>Vytvořit nové kanbanové pravidlo
1. Přejděte k Řízení informací o produktech > Lean manufacturing > Kanbanová pravidla.
2. Klikněte na položku Nová.
3. V poli Typ vyberte Výběr.
    * Tento typ se používá k vytvoření kanbanů převodu.  
4. V poli Strategie doplnění vyberte „Událost“.
    * Strategie Událost se používá s cílem vytvořit převod kanbanů na základě události. Dále v postupu spustíte kanbany převodu pomocí doplnění skladu.  
5. V poli První aktivita plánu zadejte nebo vyberte hodnotu.
    * Zadejte nebo vyberte ReplenishSpeakerComponents. Tato aktivita převodu má přijímací sklad (výstupní) a umístění 12, což znamená, že materiál se přesune do umístění 12 ve skladu 12.  
6. Rozbalte sekci Podrobnosti.
7. V poli Produkt zadejte nebo vyberte hodnotu.
    * Vyberte volbu „M0007“.  
8. Rozbalte sekci Události.
9. V poli Událost doplnění skladu vyberte „Dávka“.
    * Tímto krokem se vytvoří kanbany pro splnění požadavků na materiál v souvisejícím umístění během zpracování události požadavku.  

## <a name="set-the-minimum-quantity-for-the-item"></a>Nastavení minimálního množství pro zboží
1. Kliknutím přejdete na odkaz v poli Produkt.
2. Kliknutím přejdete na odkaz v poli Číslo položky.
3. Rozbalte okno s fakty Obrázek produktu.
4. V podokně akcí klikněte na položku Plán.
5. Klikněte na Disponibilita položky.
6. Klikněte na položku Nová.
7. Označte v seznamu vybraný řádek.
8. V poli Sklad zadejte nebo vyberte hodnotu.
    * Nastavte sklad na 12.  
9. Nastavte Minimum na "200".

## <a name="run-the-batch-event-creation-job"></a>Spuštění dávkové úlohy pro vytvoření události
1. Přejděte na Řízení výroby > Pravidelné úlohy > Dávkové zpracování kanbanových úloh > Zpracování události požadavku.
2. Klikněte na tlačítko OK.
3. Přejděte k Řízení informací o produktech > Lean manufacturing > Kanbanová pravidla.
4. Klikněte na odkaz na vybraném řádku v seznamu.
    * Vyberte kanbanové pravidlo, které bylo vytvořeno dříve.  
5. Rozbalte sekci Kanbany.
    * Všimněte si, že kanban byl vytvořen pro přenos potřebného materiálu do skladu 12.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]