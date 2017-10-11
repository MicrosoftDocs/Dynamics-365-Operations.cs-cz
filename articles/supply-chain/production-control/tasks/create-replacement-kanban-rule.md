--- 
title: "Vytvoření nahrazujícího kanbanového pravidla"
description: "Tento postup se zaměřuje na nahrazení existujícího kanbanového pravidla za nové kanbanové pravidlo k určitému datu."
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
ms.openlocfilehash: 58b12edbbdcf77429c32193dfd850bc53f4c26a8
ms.contentlocale: cs-cz
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-replacement-kanban-rule"></a>Vytvoření nahrazujícího kanbanového pravidla

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tento postup se zaměřuje na nahrazení existujícího kanbanového pravidla za nové kanbanové pravidlo k určitému datu. To je užitečné, pokud je potřeba změny v pravidlech výrobního toku nebo doplnění spravovat nebo naplánovat. Použitá ukázková data společnosti USMF k vytvoření postupu. Tento postup je určen pro technologa výrobních procesů nebo správce hodnotového proudu, kteří připravují výrobu změněného výrobního toku nebo nového pravidla doplnění. Tato úloha nahradí kanbanové pravidlo 000022 za nové pravidlo a zvýší maximální množství z 48 na 100 pro nové pravidlo.


## <a name="select-a-kanban-rule-to-replace"></a>Výběr kanbanového pravidla, které chcete nahradit
1. Otevřete Kanbanová pravidla.
2. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
    * Vyberte kanbanové pravidlo 000022.  

## <a name="create-a-replacement-kanban-rule"></a>Vytvoření nahrazujícího kanbanového pravidla
1. Klikněte na Nahradit kanbanové pravidlo.
2. Do pole Datum platnosti zadejte datum a čas.
    * Vyberte datum v budoucnosti, jako například jeden týden ode dneška. Jedná se o datum a čas, kdy se nové kanbanové pravidlo stane aktivní a nahradí původní kanbanové pravidlo.  
    * Pokud kanbanové pravidlo změní cestu ve výrobním toku, lze vybrat jinou aktivitu.  V tomto postupu doporučujeme zachovat aktivitu beze změny.  
3. Klikněte na tlačítko OK.
    * Všimněte si, že dojde k vytvoření nového kanbanového pravidla, které nahradí kanbanové pravidlo 000022.  
    * Platné datum je nastaveno podle data vybraného při nahrazení kanbanového pravidla.  
4. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
    * Vyberte nahrazené kanbanové pravidlo 000022.  
    * Povšimněte si, že nahrazené kanbanové pravidlo má stejné datum, jako datum vypršení platnosti, protože se jedná o datum, kdy platnost vyprší.  
5. Vyberte ze seznamu řádek 1.
    * Vyberte nové kanbanové pravidlo na začátku na seznamu. Jedná se o kanbanové pravidlo s nejvyšším číslem kanbanového pravidla.  
6. Klikněte na odkaz na vybraném řádku v seznamu.
    * Klikněte na číslo kanbanového pravidla a otevřete tak kanbanové pravidlo.  

## <a name="modify-maximum-quantity-for-the-replacement-kanban-rule"></a>Úprava maximálního množství pro náhradní kanbanové pravidlo
1. Nastavte Maximální množství na „100“.
    * Rozbalte pevnou záložku Množství a prohlédněte si pole Maximální množství. Změna maximálního množství na hodnotu 100 vám umožní zpracovat až 100 kanbanů.    Tento krok je posledním krokem v tomto postupu.  

