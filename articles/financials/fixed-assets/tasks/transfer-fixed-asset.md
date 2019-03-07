---
title: Převedení dlouhodobého majetku
description: Tento průvodce záznamem úloh převede finanční informace pro knihu dlouhodobého majetku z jedné sady finančních dimenzí do nové sady finančních dimenzí.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetTransfer, DimensionLookup, AssetTransferConfirmation
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bb8a5b94d9a0bb510daa2a698524e0c380597991
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "357190"
---
# <a name="transfer-a-fixed-asset"></a>Převedení dlouhodobého majetku

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tento průvodce záznamem úloh převede finanční informace pro knihu dlouhodobého majetku z jedné sady finančních dimenzí do nové sady finančních dimenzí.  Využívá účetní role a ukázková data pro právnické osoby USMF.

1. Přejděte do části Dlouhodobý majetek > Dlouhodobý majetek > Dlouhodobý majetek.
2. V seznamu najděte a vyberte dlouhodobý majetek, který chcete přenést.
3. V podokně akcí klikněte na možnost Dlouhodobý majetek.
4. Klikněte na Převést dlouhodobý majetek.
5. Do pole Datum převodu zadejte datum.
6. Zadejte komentáře popisující převod.
    * Tento seznam zobrazuje všechny knihy pro dlouhodobý majetek.  
7. Označte knihy, které chcete převést do nové sady finančních dimenzí.
    * Tento seznam zobrazuje hodnoty aktuální finanční dimenze pro vybranou knihu.  
    * Zvolte finanční dimenzi, kterou chcete aktualizovat pro vybranou knihu dlouhodobého majetku.  
8. V poli Finanční dimenze kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
    * Podle potřeby nastavte jiné hodnoty finančních dimenzí.  
    * Veškeré hodnoty finanční dimenze se změní, jakmile dojde k převodu, a to podle toho, zda byla zadána hodnota nebo ponechána prázdná. Například pokud je zadána hodnota pro organizační jednotku a hodnota pro finanční dimenze nákladového centra a oddělení ponechána prázdná. Pokud vaše účetní struktura umožňuje prázdné hodnoty pro nákladové centrum a oddělení, převod způsobí, že každý oceňovací model bude mít novou hodnotu pro obchodní jednotku a prázdnou hodnotu nákladové centrum a oddělení.  
9. Klepněte na položku Aktualizovat.
    * Budete moci vytvořit náhled změn před uzavřením převodu.  
    * Zkontrolujte výsledky před přenesením knih dlouhodobého majetku.  
10. Klepněte na položku Převod.

