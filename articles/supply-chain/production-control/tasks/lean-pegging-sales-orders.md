---
title: Doložení z prodejních objednávek štíhlé výroby
description: Tento postup se zaměřuje na ověřování stromu doložení z řádku prodeje, kde položka je vyráběna s kanbany.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, LeanPeggingTree
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8eca21f8bd988ca352c07e839295b3edd9669929
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/29/2021
ms.locfileid: "7580617"
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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]