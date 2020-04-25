---
title: Doložení z prodejních objednávek štíhlé výroby
description: Tento postup se zaměřuje na ověřování stromu doložení z řádku prodeje, kde položka je vyráběna s kanbany.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, LeanPeggingTree
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e429fef6101f611d7a2c1b5323d6fe1e39d1cdd3
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/02/2020
ms.locfileid: "3206995"
---
# <a name="lean-pegging-from-sales-orders"></a>Doložení z prodejních objednávek štíhlé výroby

[!include [banner](../../includes/banner.md)]

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

