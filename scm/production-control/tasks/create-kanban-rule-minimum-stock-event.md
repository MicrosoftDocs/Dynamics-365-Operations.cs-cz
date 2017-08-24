--- 
title: "Vytvoření kanbanového pravidla s použitím události pro minimální úroveň zásob"
description: "Tento postup se zaměřuje na nastavení potřebné k vytvoření kanbanového pravidlo pomocí události pro minimální úroveň zásob, aby tak bylo jisté, že bude konkrétní produkt v určitém místě vždy k dispozici."
author: ChristianRytt
manager: AnnBe
ms.date: 08/24/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: c655f9e2cb3967a44c357f16d18884ec0bc55357
ms.contentlocale: cs-cz
ms.lasthandoff: 07/27/2017

---
# Vytvoření kanbanového pravidla s použitím události pro minimální úroveň zásob

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tento postup se zaměřuje na nastavení potřebné k vytvoření kanbanového pravidlo pomocí události pro minimální úroveň zásob, aby tak bylo jisté, že bude konkrétní produkt v určitém místě vždy k dispozici. Je vytvořeno kanbanové pravidlo, které při poklesu úrovně zásob pod 200 kusů převede materiál do skladového místa. Spuštěním zpracování události požadavku dojde k vytvoření potřebných kanbanů. Tento úkol byl vytvořen pomocí ukázkových dat společnosti USMF. Tento úkol je určen pro technologa výrobních procesů nebo správce hodnotového proudu, kteří připravují výrobu nového nebo změněného výrobku v prostředí štíhlé výroby.


## Vytvořit nové kanbanové pravidlo
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

## Nastavení minimálního množství pro zboží
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

## Spuštění dávkové úlohy pro vytvoření události
1. Přejděte na Řízení výroby > Pravidelné úlohy > Dávkové zpracování kanbanových úloh > Zpracování události požadavku.
2. Klikněte na tlačítko OK.
3. Přejděte k Řízení informací o produktech > Lean manufacturing > Kanbanová pravidla.
4. Klikněte na odkaz na vybraném řádku v seznamu.
    * Vyberte kanbanové pravidlo, které bylo vytvořeno dříve.  
5. Rozbalte sekci Kanbany.
    * Všimněte si, že kanban byl vytvořen pro přenos potřebného materiálu do skladu 12.  


