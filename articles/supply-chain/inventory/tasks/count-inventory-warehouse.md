---
title: "Inventura zásob ve skladu"
description: "Tento postup vás provede procesem vytvoření a zaúčtování deníku inventury zásob za účelem spočítání specifického zboží v jednom umístění ve skladu."
author: MarkusFogelberg
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: fa72cb0d651f5e60797fa41f6e2b2cf1891730b5
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="count-inventory-in-a-warehouse"></a>Inventura zásob ve skladu

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tento postup vás provede procesem vytvoření a zaúčtování deníku inventury zásob za účelem spočítání specifického zboží v jednom umístění ve skladu. Tento postup lze použít pro funkce „základního uskladnění“, dostupného v modulu Řízení zásob, ne pro funkce uskladnění, které jsou k dispozici v modulu Řízení skladu. Tento proces můžete projít pomocí ukázkových dat společnosti USMF nebo pomocí vlastních dat. Používáte-li vlastní data, ujistěte se, že máte nastaveny produkty a umístění a že jste vytvořili název deníku zásob pro deníky inventury. Inventuru skladu běžně provádí zaměstnanec skladu.


## <a name="create-an-inventory-counting-journal"></a>Vytvořte deník inventur zásob
1. Přejděte do Řízení zásob > Položky deníku > Inventura zboží > Inventura.
2. Klikněte na položku Nová.
3. V poli Název kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
4. V seznamu klepněte na název deníku inventury skladu, který chcete použít
    * Některá další pole budou vyplněna na základě nastavení názvu deníku inventur zásob, který jste vybrali.  
5. V poli Pracovník klepnutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
6. Ze seznamu vyberte pracovníka, kterého chcete použít.
7. Klepněte na tlačítko Vybrat.
8. Klikněte na tlačítko OK.

## <a name="create-journal-lines"></a>Vytvoření řádků deníku
1. Klikněte na položku Nová.
2. V poli Číslo zboží kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
3. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
    * Používáte-li ukázková data společnosti USMF, vyberte hodnotu „A0001“.  
4. V poli Lokalita kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
5. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
    * Používáte-li ukázková data společnosti USMF, vyberte web „2“.  
6. V poli Sklad kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
7. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
    * Používáte-li ukázková data společnosti USMF, vyberte sklad „24“.  
8. V poli Umístění kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
9. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
    * Používáte-li ukázková data společnosti USMF, vyberte umístění „BULK-001“.  
10. Zadejte číslo do pole Spočteno.
    * Pokud zadáte číslo inventury, které se liší od čísla uvedeného v poli Na skladě, pole množství se aktualizuje a zobrazí odchylku.  
11. Klikněte na položku Uložit.

## <a name="post-the-inventory-counting-journal"></a>Zaúčtujte deník inventury zásob
1. Klikněte na položku Zaúčtovat.
    * Když tento deník inventury skladu zaúčtujete, a zaúčtovaná částka se bude lišit od částky nahlášené v poli Na skladě, zaúčtuje se příjem nebo výdej zásob, změní se úroveň a hodnota zásob a vygeneruje se transakce hlavní knihy.  
2. Klikněte na tlačítko OK.

## <a name="view-inventory-transactions"></a>Zobrazit skladové transakce
1. Klepněte na položku Zásoby.
2. Klikněte na Transakce.
    * V tomto poli se zobrazí všechny související transakce vytvořené při zaúčtování deníku inventury zásob.   

