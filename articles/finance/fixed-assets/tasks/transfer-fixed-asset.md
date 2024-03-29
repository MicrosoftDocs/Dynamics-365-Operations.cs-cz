---
title: Převedení dlouhodobého majetku
description: Tento průvodce záznamem úloh převede finanční informace pro knihu dlouhodobého majetku z jedné sady finančních dimenzí do nové sady finančních dimenzí.
author: moaamer
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetTable, AssetTransfer, DimensionLookup, AssetTransferConfirmation
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7c8428467d6e12b6d6af9023980b8cf8738d9294
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/07/2022
ms.locfileid: "8726998"
---
# <a name="transfer-a-fixed-asset"></a>Převedení dlouhodobého majetku

[!include [banner](../../includes/banner.md)]

Tento průvodce záznamem úloh převede finanční informace pro knihu dlouhodobého majetku z jedné sady finančních dimenzí do nové sady finančních dimenzí.  

1. V navigačním podokně přejděte na **Moduly > Dlouhodobý majetek > Dlouhodobý majetek > Dlouhodobý majetek**.
2. V seznamu najděte a vyberte dlouhodobý majetek, který chcete přenést.
3. V podokně akcí klikněte na možnost **Dlouhodobý majetek**.
4. Klikněte na **Převést dlouhodobý majetek**.
5. Do pole **Datum převodu** zadejte datum.
6. Zadejte komentáře popisující převod.
    
    Tento seznam zobrazuje všechny knihy pro dlouhodobý majetek.  
7. Označte knihy, které chcete převést do nové sady finančních dimenzí.
    * Tento seznam zobrazuje hodnoty aktuální finanční dimenze pro vybranou knihu.  
    * Zvolte finanční dimenzi, kterou chcete aktualizovat pro vybranou knihu dlouhodobého majetku.  
8. V poli **Finanční dimenze** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
    * Podle potřeby nastavte jiné hodnoty finančních dimenzí.  
    * Veškeré hodnoty finanční dimenze se změní, jakmile dojde k převodu, a to podle toho, zda byla zadána hodnota nebo ponechána prázdná. Například pokud je zadána hodnota pro organizační jednotku a hodnota pro finanční dimenze nákladového centra a oddělení ponechána prázdná. Pokud vaše účetní struktura umožňuje prázdné hodnoty pro nákladové centrum a oddělení, převod způsobí, že každý oceňovací model bude mít novou hodnotu pro obchodní jednotku a prázdnou hodnotu nákladové centrum a oddělení.  
9. Klikněte na položku **Aktualizovat**.
    * Budete moci vytvořit náhled změn před uzavřením převodu.  
    * Zkontrolujte výsledky před přenesením knih dlouhodobého majetku.  
10. Klikněte na položku **Převod**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
