--- 
title: "Doložení z prodejních objednávek štíhlé výroby"
description: "Tento postup se zaměřuje na ověřování stromu doložení z řádku prodeje, kde položka je vyráběna s kanbany."
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
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 3aa8cd2c0be56875904158f041cf120c466d9e9a
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="lean-pegging-from-sales-orders"></a>Doložení z prodejních objednávek štíhlé výroby

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tento postup se zaměřuje na ověřování stromu doložení z řádku prodeje, kde položka je vyráběna s kanbany. Po ověření stromu doložení jsou plánovány všechny kanbanové úlohy. To je užitečné pro objednávky scénáře, kde pořadí příjemce musí zajistit, aby bylo možné výrobu spustit přímo. K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF. Tento postup je určen pro rozšířenou objednávku příjemce pracující ve štíhlé společnosti.


## <a name="create-a-sales-order-for-a-kanban-controlled-item"></a>Vytvořte prodejní objednávky pro položku řízenou kanbanem
1. Přejděte na Všechny prodejní objednávky.
2. Klikněte na položku Nová.
3. V poli Účet odběratele zadejte nebo vyberte hodnotu.
    * Použití US-001.  
4. Klikněte na tlačítko OK.
5. Do pole Číslo položky zadejte L0001.
6. Nastavte množství na hodnotu 30.
    * Je důležité, aby množství bylo vyšší než 24 za účelem aktivace pravidla kanbanové události.  

## <a name="open-a-pegging-tree"></a>Otevřete strom doložení 
1. Klikněte na Produkt a dodávka.
2. Klepněte na Zobrazit strom doložení.
    * Všimněte si, že strom doložení zobrazuje všechny úrovně doložení pro řádek prodejní objednávky. V tomto případě existují dvě úrovně kanbanů a všechny potřebné součásti.  

## <a name="plan-the-pegging-tree"></a>Naplánovat strom doložení
1. Ve stromovém zobrazení vyberte „Řádek prodeje 000832\Kanban 000558“.
2. Rozbalte část Kanbanové úlohy.
    * Všimněte si, že stav úlohy pro kanbanovou úlohu je Nenaplánováno.  
3. Klikněte na Naplánovat celý strom doložení.
    * Tímto naplánujete všechny kanbanové úlohy ve stromu doložení, změníte stav úlohy z Není plánováno na Plánováno.  
4. Aktualizujte stránku.
    * Všimněte si, že stav kanbanové úlohy se změní z Nenaplánováno na Naplánováno.  
5. Ve stromovém zobrazení vyberte „Řádek prodeje 000832\Kanban 000558\Výdej pro L0001\Kanban 000559“.
    * Úloha pro druhý kanban je také plánována, protože celý strom doložení je plánován. Všimněte si, že stav kanbanové úlohy bude změněn z Nenaplánováno na Naplánováno.  


