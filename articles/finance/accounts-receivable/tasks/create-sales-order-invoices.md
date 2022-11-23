---
title: Vytváření faktur prodejních objednávek
description: Tento článek popisuje zásady fakturace prodejní objednávky, včetně sloučení faktur a dávkového zpracování.
author: ShivamPandey-msft
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesTableListPage, SalesEditLines,  SysQueryForm, SysRecurrence
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3ff76eac54da6621d999d9b629fac920ba8de294
ms.sourcegitcommit: 9c4638c4bb5b5f8adc7508542a0a2c3e1de5190c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/15/2022
ms.locfileid: "9778377"
---
# <a name="create-sales-order-invoices"></a>Vytváření faktur prodejních objednávek

[!include [banner](../../includes/banner.md)]

Tento článek popisuje zásady fakturace prodejní objednávky, včetně sloučení faktur a dávkového zpracování. Tato procedura používá ukázkovou společnost USMF.


## <a name="create-an-invoice-from-a-sales-order"></a>Vytvoření faktury z prodejní objednávky
1. Přejděte na **Navigační podokno > Moduly > Pohledávky > Objednávky > Dodáno ale bez vyfakturovaných prodejních objednávek**.
2. Vyberte ze seznamu prodejní objednávku. 
3. V **Podokně akcí** klikněte na **Faktura > Generovat > Faktura**. Všimněte si, že tato prodejní objednávka má přidruženo více dodacích listů. Zde se zobrazí pouze slovo *více* namísto čísla dodacího listu.  
4. Rozbalte sekci **Parametry**.
    - Zaúčtování musí být pro zaúčtování faktury nastaveno na hodnotu **Ano**. Lze také vypnout zaúčtování fakturu pouze vytisknout. Stejného výsledku však lze dosáhnout pomocí vytvoření faktury proforma namísto faktury.  
    - Tato možnost se využívá pro dávkové úlohy. Dotaz se spustí při spuštění dávkové úlohy.
5. V poli **Tisk** vyberte možnost **Po**.
6. Vyberte možnost **Ano** pro **Tisk faktury**. Správu tisku umožňuje vytisknout více kopií faktury a také odesílat faktury prostřednictvím e-mailu jako soubor PDF.  
7. Vyberte možnost **Souhrn** v poli **Tisk nákladů**.
8. V poli **Zkontrolovat limit** úvěru vyberte **Zůstatek**.
9. Klepněte na možnost **Zrušit**.

## <a name="combine-orders-into-a-single-invoice"></a>Sloučení objednávek do jedné faktury
1. Přejděte na **Navigační podokno > Moduly > Pohledávky > Objednávky > Všechny prodejní objednávky**.
2. Vyhledejte zákazníka, který má více otevřených faktur.
3. Vyberte více otevřených prodejních objednávek od stejného odběratele.
4. V **Podokně akcí** klikněte na **Faktura > Generovat > Faktura**.
5. Rozbalte sekci **Parametry**.
6. V poli **Množství** vyberte možnost **Vše**. Existují dvě faktury, které jsou uvedeny v přehledu. Nyní je sloučíme do jedné faktury.  
7. V poli **Souhrnná aktualizace pro** vyberte **Účet faktury**.
8. Klikněte na **Uspořádat** pro sloučení prodejních objednávky do jedné faktury. Dvě prodejních objednávky jsou nyní sloučeny do jedné faktury.   
9. Klepněte na možnost **Zrušit**.
10. Klepněte na tlačítko **Ano**.

## <a name="post-invoices-in-a-batch"></a>Zaúčtování faktur do dávky
1. Přejděte na **Navigační podokno > Moduly > Pohledávky > Faktury > Dávková fakturace > Faktura**.
2. Klepněte na tlačítko **Vybrat**.
3. Klikněte na tlačítko **OK**.
4. Klepněte na možnost **Dávka**.
5. Vyberte možnost **Ano** v části **Dávkové zpracování**.
6. Klikněte na **Opakování**.
7. Vyberte **Dny**.
8. Klikněte na tlačítko **OK**.
9. Klikněte na tlačítko **OK**.
10. Klepněte na možnost **Zrušit**.
11. Klepněte na tlačítko **Ano**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
