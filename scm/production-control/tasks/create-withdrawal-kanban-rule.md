--- 
title: "Vytvoření nového kanbanového pravidla odběru"
description: "Tento postup popisuje nastavení, které je třeba pro vytvoření kanbanového pravidla výběru pro převod materiálu v prostředí štíhlé výroby."
author: ChristianRytt
manager: AnnBe
ms.date: 06/20/2016
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
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: c3172f5c932b94b2a9e442286eb61159286297fb
ms.contentlocale: cs-cz
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-withdrawal-kanban-rule"></a>Vytvoření nového kanbanového pravidla odběru

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tento postup popisuje nastavení, které je třeba pro vytvoření kanbanového pravidla výběru pro převod materiálu v prostředí štíhlé výroby. K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF. Tento postup je určen pro technologa výrobních procesů nebo správce hodnotového proudu, kteří připravují doplnění nového nebo změněného materiálu.


## <a name="create-new-kanban-rule"></a>Vytvořit nové kanbanové pravidlo
1. Otevřete Kanbanová pravidla.
2. Klikněte na položku Nová.
3. V poli Typ vyberte Výběr.
    * Typ Výběr se používá pro kanbanová pravidla zaměřená na převod materiálu nebo zboží.  
4. V poli První aktivita plánu zadejte nebo vyberte hodnotu.
    * Vyberte ReplenishSpeakerComponents.   Tato aktivita je nastavena na přesun součástí ze skladu 11 v umístění 11 do skladu 12 v umístění 12.  
5. V poli Produkt zadejte nebo vyberte hodnotu.
    * Vyberte volbu „M0007“.  
6. Do pole Doba realizace zadejte číslo.
    * Například 60.  
7. V poli Měrná jednotka zadejte nebo vyberte hodnotu.
    * Například Minuty.  

## <a name="set-quantities-for-kanban"></a>Nastavte množství pro kanban
1. Nastavte výchozí množství na „5“.
    * Jedná se o množství, které bude přeneseno pro každý kanban.  
2. Zadejte 2 do pole Pevné kanbanové množství.
    * To je počet kanbanů, které mají být aktivní. V tomto případě 2 kanbany přenáší vždy každý 5.  
3. V poli Minimální hranice výstrahy zadejte hodnotu „1“.
    * Slouží ke sledování minimálního množství plných kanbanů, které mají být na místě určení. Toto se například používá na přehled kanbanového množství.  
4. V poli Maximální hranice výstrahy zadejte hodnotu „2“.
    * Slouží ke sledování maximálního množství plných kanbanů, které mají být na místě určení. Toto se například používá na přehled kanbanového množství.  

## <a name="create-kanbans"></a>Vytvořit kanbany
1. Klikněte na položku Uložit.
    * Kanbanové pravidlo je třeba uložit, aby bylo možné vytvořit kanbany.  
2. Klepněte na možnost Přidat.
    * Všimněte si, že neexistují žádné aktivní kanbany, protože navrhovaný „Počet nových kanbanů“ je 2. Toto se rovná „Pevnému kanbanovému množství“.  
3. Klikněte na položku Vytvořit.
    * Dojde k vytvoření 2 kanbanů.  
    * Všimněte si, že 2 kanbany po 5 byly vytvořeny pro toto kanbanové pravidlo výběru.  Tento krok je posledním krokem v tomto postupu.  


