---
title: Sledování položky nebo suroviny
description: Tento postup uvádí použití sledování položky k určení, kde bylo zboží nebo suroviny použity nebo jsou používány.
author: sherry-zheng
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventTrackingDimTracing, InventTrackingDimTracingCriteria, InventTrackingItemIdLookup, InventBatchIdLookup, CustTable, SalesLine
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: chuzheng
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 01e945b94017dd95a43e0f089902ffd3ea1298ef230f84d9198031b30e323ef9
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6781919"
---
# <a name="trace-an-item-or-raw-material"></a>Sledování položky nebo suroviny

[!include [banner](../../includes/banner.md)]

Tento postup uvádí použití sledování položky k určení, kde bylo zboží nebo suroviny použity nebo jsou používány. Pomocí tohoto postupu lze identifikovat zboží, vysledovat ho zpět ke zdroji, a potom jej sledovat dopředu přes výrobu a prodeji hotového výrobku. Tento proces použít k analýze ovlivněných odběratelů, dotyčných prodejních objednávek a další. Tato procedura používá data ukázkové společnosti USP2.


## <a name="trace-an-item-backwards-using-a-known-batch-number"></a>Sledujte položky zpětně za použití známého čísla dávky
1. V **Navigačním podokně** přejděte na **Moduly > Řízení zásob > Dotazy a sestavy > Sledovací dimenze > Sledování zboží**.
2. V poli **Číslo položky** vyberte „P9100“.
3. Klikněte na odkaz na vybraném řádku v seznamu.
4. V poli **Dopředu nebo dozadu** vyberte „Dozadu“.
5. V poli **Číslo dávky** vyberte „as-12-344-01“.
6. Klikněte na odkaz na vybraném řádku v seznamu.
7. Klikněte na tlačítko **OK**.

## <a name="identify-an-item-trace-it-forward-and-make-an-analysis"></a>Identifikujte zboží, sledujte ho dopředu a proveďte analýzu

Nejvyšší uzel stromové struktury představuje množství vybraných položek na skladě a dávky. Je nutné rozbalit uzly ve stromu a vyhledat tak položku, u které má být provedeno dopředné sledování.   
1. Ve stromovém zobrazení rozbalte níže popsané uzly a pak vyberte poslední uzel.
    
    Rozbalení „P9100 / 1 / 10 / as-12-344-01 ● 2 sudy ● 7,00 galonů \P9100 ● Vyskladněno ● Prodejní objednávka 000072 ● 22. 12. 2015 ● -1 sud ● -4,00 galony ● Pracoviště = 1, sklad = 10, číslo dávky = as-12-344-01 \P9100 ● Výroba B-000050 ● 9. 12. 2015 ● 7 sudů ● 27,00 galonů ● Pracoviště = 1, sklad = 10, číslo dávky = as-12-344-01 ● Vedlejší produkty: P9101“ a pak vyberte uzel.     
2. Ve stromovém zobrazení rozbalte níže popsaný uzel a pak jej vyberte.
    
    Od uzlu, který jste právě vybrali, rozbalte „M9103 ● Řádek výroby B-000050 ● 9. 12. 2015 ● -160,00 liber ● velikost = 70, barva = OK, pracoviště = 1, sklad = 10, číslo dávky = App01“ a pak vyberte daný uzel.  
3. Klepněte na **Sledovat z uzlu**.
4. Klikněte na **Vpřed**.
5. V **Podokně akcí** klepněte na možnost **Sledování**.
    
    Existuje několik možností sledování, které poskytují informace o odběratelích, a které jsou ovlivněny vámi sledovaným zbožím a prodejními objednávkami souvisejícími s položkou, která byla nebo nebyla zatím expedována.   
6. Klikněte na **Zákazníci**.
7. Zavřete stránku.
8. V **Podokně akcí** klepněte na možnost **Sledování**.
9. Klikněte na **Prodejní objednávky za expedované zboží**.
10. Zavřete stránku.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]