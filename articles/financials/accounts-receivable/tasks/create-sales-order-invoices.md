--- 
title: "Vytváření faktur prodejních objednávek"
description: "Tento průvodce úkolem popisuje zásady fakturace prodejní objednávky, včetně sloučení faktur a dávkového zpracování."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 50c0ee41220461e282aace85f10a0e734a2ab688
ms.contentlocale: cs-cz
ms.lasthandoff: 07/27/2017

---
# <a name="create-sales-order-invoices"></a>Vytváření faktur prodejních objednávek

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tento průvodce úkolem popisuje zásady fakturace prodejní objednávky, včetně sloučení faktur a dávkového zpracování. Tato procedura používá ukázkovou společnost USMF.


## <a name="create-an-invoice-from-a-sales-order"></a>Vytvoření faktury z prodejní objednávky
1. Přejděte na Pohledávky > Objednávky > Dodáno ale bez vyfakturovaných prodejních objednávek
2. Vyberte ze seznamu prodejní objednávku. 
3. V podokně akcí klikněte na položku Faktura.
4. Klikněte na položku Faktura.
    * Všimněte si, že tato prodejní objednávka má přidruženo více dodacích listů. Zde se zobrazí pouze slovo <multiple> namísto čísla dodacího listu.  
5. Rozbalte sekci Parametry.
    * Zaúčtování musí být pro zaúčtování faktury nastaveno na hodnotu Ano. Lze také vypnout zaúčtování fakturu pouze vytisknout. Stejného výsledku však lze dosáhnout pomocí vytvoření faktury proforma namísto faktury.  
    * Tato možnost se využívá pro dávkové úlohy. Dotaz se spustí při spuštění dávkové úlohy.    
6. V poli Tisk vyberte možnost Po.
7. Vyberte možnost Ano pro tisk faktury.
    * Správu tisku umožňuje vytisknout více kopií faktury a také odesílat faktury prostřednictvím e-mailu jako soubor PDF.  
8. Vyberte možnost Souhrn v poli Tisk nákladů.
9. V poli Zkontrolovat limit úvěru vyberte 'Zůstatek'.
10. Klikněte na možnost Zrušit.

## <a name="combine-orders-into-a-single-invoice"></a>Sloučení objednávek do jedné faktury
1. Přejděte na Pohledávky > Objednávky > Všechny prodejní objednávky.
2. Vyhledejte zákazníka, který má více otevřených faktur.
3. Vyberte otevřenou prodejní objednávku.
4. Vyberte jinou otevřenou prodejní objednávku pro stejného odběratele.
5. V podokně akcí klikněte na položku Faktura.
6. Klepněte na Faktura.
7. Rozbalte sekci Parametry.
8. V poli Množství vyberte možnost Vše.
    * Existují dvě faktury, které jsou uvedeny v přehledu. Nyní je sloučíme do jedné faktury.  
9. V poli Souhrnná aktualizace pro vyberte Účet faktury.
10. Klikněte na Účet faktury pro sloučení prodejních objednávky do jedné faktury.
    * Dvě prodejních objednávky jsou nyní sloučeny do jedné faktury.   
11. Klikněte na možnost Zrušit.
12. Klepněte na tlačítko Ano.

## <a name="post-invoices-in-a-batch"></a>Zaúčtování faktur do dávky
1. Přejděte na Pohledávky > Faktury > Dávková fakturace > Faktura.
2. Klepněte na tlačítko Vybrat.
3. Klikněte na tlačítko OK.
4. Klepněte na možnost Dávka.
5. Klepněte na hodnotu Ano, chcete-li povolit dávkové zpracování.
6. Klepněte na tlačítko Opakování.
7. Vyberte Dny
8. Klikněte na tlačítko OK.
9. Klikněte na tlačítko OK.
10. Klikněte na možnost Zrušit.
11. Klepněte na tlačítko Ano.


