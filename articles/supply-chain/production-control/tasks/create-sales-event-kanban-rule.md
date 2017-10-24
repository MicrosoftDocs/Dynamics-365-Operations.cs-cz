--- 
title: "Vytvoření kanbanového pravidla události prodeje"
description: "Tento postup se zaměřuje na potřebné nastavení k vytvoření kanbanového pravidla, které se spustí při vytváření prodejní objednávky."
author: ChristianRytt
manager: AnnBe
ms.date: 03/02/2016
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
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: f1f66157b2e74ad1b490e10112cbc121ac9826fb
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-sales-event-kanban-rule"></a>Vytvoření kanbanového pravidla události prodeje

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tento postup se zaměřuje na potřebné nastavení k vytvoření kanbanového pravidla, které se spustí při vytváření prodejní objednávky. Pravidla kanbanové události doplňuje požadavky, které pocházejí z řádků prodejní objednávky. K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF. Je to určeno pro technologa výrobních procesů nebo správce hodnotového proudu, kteří připravují výrobu nového nebo změněného výrobku.




## <a name="create-a-new-kanban-rule"></a>Vytvořit nové kanbanové pravidlo
1. Otevřete Kanbanová pravidla.
2. Klikněte na položku Nová.
3. V poli Strategie doplnění vyberte „Událost“.
    * Výběr události znamená, že kanbanové pravidlo je vyvoláno událostí, například vytvořením řádku prodejní objednávky.   Používá se na oblasti, kde každý kanban by měl pokrývat specifické požadavky.  
4. V poli První aktivita plánu zadejte nebo vyberte hodnotu.
    * Vyberte Poslední sestavení.  
5. Rozbalte sekci Podrobnosti.
6. V poli Produkt zadejte nebo vyberte hodnotu.
    * Vyberte volbu „L0050“.  

## <a name="define-an-event"></a>Definujte událost
1. Rozbalte sekci Události.
2. V poli Události prodeje vyberte možnost „Automatická“.
    * Výběrem automatické události prodeje bude toto kanbanové pravidlo bude aktivováno automaticky při shodě řádku prodeje s umístěním a příjmem produktů. V tomto postupu je produkt L0050 ve skladu 13.  
3. Nastavte minimální množství události na „50“.
    * S minimálním množstvím událostí 50, se bude kanbanové pravidlo pouze spouštět událostmi s množstvím 50 nebo vyšším.  
4. Rozbalte položku výrobního toku.
    * Všimněte si, že místo příjmu je sklad 13. To znamená, že pro toto místo bude spouštěno toto kanbanové pravidlo.  
    * V tomto příkladu řádek prodeje produktu L0050, s množstvím nejméně 50 na skladu 13, se spustí tímto kanbanovým pravidlem.  

## <a name="create-sales-line-to-trigger-event-kanban-rule"></a>Vytvořte řádek prodeje pro aktivaci události kanbanovým pravidlem
1. Přejděte na Všechny prodejní objednávky.
    * Upozornění se zobrazí při uložení kanbanového pravidla, což znamená, že kanbany budou vytvořeny v reálném čase při vytváření prodejní objednávky.  
2. Klikněte na položku Nová.
3. V poli Účet odběratele zadejte nebo vyberte hodnotu.
    * Vyberte například US-003.  
4. Klikněte na tlačítko OK.
5. Do pole Číslo položky zadejte L0050.
6. Zadejte do pole Místo hodnotu „1“.
    * Vyberte Místo 1 neboť Sklad 13 je připojen v Místě 1.  
7. V poli Sklad zadejte nebo vyberte hodnotu.
    * Nastavte sklad na 13.  
8. Nastavte množství na hodnotu 75.
    * Zadejte množství 50 nebo vyšší pro aktivaci vytvořeného kanbanového pravidla.  

## <a name="verify-that-kanban-is-created"></a>Ověřte, že je kanban vytvořen
1. Klikněte na Produkt a dodávka.
2. Klepněte na Zobrazit strom doložení.
    * Všimněte si, že kanban je vytvořen stejným množstvím jako řádek prodeje. Můžete také vidět výdej materiálu vyžadovaný k výrobě L0050. Tento krok je posledním krokem v tomto postupu.  


