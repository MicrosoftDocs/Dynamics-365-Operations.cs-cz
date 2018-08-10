---
title: "Vytvoření nové zakázky na doplnění stavu zásob dodávky"
description: "Tato procedura ukazuje, jak vytvořit objednávku doplnění stavu zásob dodávky, kde můžete sledovat očekávanou dodávku od dodavatele do skladu dodávky."
author: mkirknel
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: f7f8005ec9e723c94d53e6ab81f04ee388c83faa
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-consignment-replenishment-order"></a>Vytvoření nové zakázky na doplnění stavu zásob dodávky

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tato procedura ukazuje, jak vytvořit objednávku doplnění stavu zásob dodávky, kde můžete sledovat očekávanou dodávku od dodavatele do skladu dodávky. Také ukazuje, jak zaznamenávat příjem produktů tak, aby byla zásoba dodávky registrována jako zásoby na skladě ve vlastnictví dodavatele. Tuto proceduru obvykle provádí zásobovací pracovník. Tohoto průvodce můžete použít s ukázkových dat společnosti USMF. Tato procedura je určena pro funkci, která byla přidána do aplikace Dynamics 365 for Operations, verze 1611.




## <a name="create-a-consignment-replenishment-order"></a>Vytvoření nové zakázky na doplnění stavu zásob dodávky
1. Přejděte do nabídky Zásobování a zdroje > Zásilka > Zakázky na doplnění stavu zásob dodávky.
2. Klikněte na položku Nová.
3. V poli Účet dodavatele vyberte dodavatele US-104.
    * Je nutné vybrat dodavatele, který je registrován jako vlastník na stránce Vlastníci zásob.  
4. Klikněte na tlačítko OK.
5. Klikněte na položku Přidat řádek.
6. Do pole Číslo položky zadejte M9211CI.
    * Je nutné vybrat položku, která je nastavena pro zásoby dodávky.  
7. Zadejte číslo do pole Množství.
8. Zadejte datum do pole Požadované datum dodání.
    * Požadované a potvrzené datum používá modul MRP pro očekávané přijetí zboží.  
9. Zadejte datum do pole Potvrzené datum dodání.
10. Rozbalte sekci Podrobnosti řádku.
11. Klepněte na kartu Dimenze zásob.
12. Chcete-li zobrazit vlastníka v poli Vlastník dimenze zásob, aktualizujte stránku.
    * Dodavatel US-104 je nyní uveden jako vlastník.  

## <a name="check-the-inventory-transaction-status"></a>Zkontrolujte stav transakce zásob.
1. Klepněte na položku Zásoby.
2. Klikněte na Transakce.
3. Označte v seznamu vybraný řádek.
    * Všimněte si, že pole Příjem je nastaveno na Objednáno.  
4. Zavřete stránku.

## <a name="receive-items"></a>Přijmout položky
1. Klikněte na položku Příjemka produktu.
2. Zadejte hodnotu do pole Externí příjemka produktu.
3. Do pole Množství zadejte číslo, které je nižší než číslo, které je zde uvedeno.
4. Klikněte na tlačítko OK.

## <a name="check-the-on-hand-inventory"></a>Zkontrolujte množství na skladě.
1. Klepněte na položku Zásoby.
2. Klikněte na Na skladě.
3. Klepněte na tlačítko Přehled.
    * Položky, které byly přijaty jako zásoby dodávky ve vlastnictví dodavatele, jsou k dispozici na skladě. Zbývající množství na objednávce doplnění stavu zásob dodávky je uvedeno v poli Celkem objednáno.  
4. Zavřete stránku.
5. Klikněte na tlačítko Zavřít.

