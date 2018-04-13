--- 
title: "Zadání dat faktury do systému závazků s použitím evidence faktur"
description: "Tento průvodce úkolem popisuje postup použití registru faktur k vytvoření faktur."
author: abruer
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 96040b1c1ba130f773ba0defbf7bf1dcebedfc13
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="key-invoice-data-into-the-ap-system-using-invoice-pool"></a>Zadání dat faktury do systému závazků s použitím evidence faktur

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Tento průvodce úkolem popisuje postup použití registru faktur k vytvoření faktur.  Potom použije evidenci faktur pro spárování faktury s nákupní objednávkou a dokončení výdajů na stránce faktury dodavatele.


## <a name="create-a-purchase-order"></a>Vytvoření nákupní objednávky
1. Přejděte na Závazky > Nákupní objednávky > Nákupní objednávky.
2. Klepnutím na příkaz Nový vytvořte nákupní objednávku.
3. V poli Účet dodavatele kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
4. Vyberte dodavatele ze seznamu. Příklad dodavatele 1001.
5. Klepněte na tlačítko OK.
6. V poli Číslo zboží kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
7. najděte v seznamu číslo položky služby. Vyberte například S0001.
8. Klepněte číslo položky a vyberte je.
    * Čistá částka je 75,00.  Jedná se o částku, která se očekává na faktuře.  
9. V podokně akcí klikněte na možnost Zakoupit.
10. Klikněte na tlačítko Potvrdit.

## <a name="create-and-post-and-invoice"></a>Vytvoření a zaúčtování faktury
1. Přejděte na Závazky > Faktury > Registr faktur.
2. Klikněte na položku Nová.
3. Otevřete vyhledávání a vyberte název registru faktury, který chcete použít.
4. Vyberte název registru faktury, který chcete použít.
5. Kliknutím na Řádky otevřete registr a zadejte řádky výdajů.
6. Ve vyhledávání vyberte dodavatele. Například klepněte na dodavatele 1001.
7. Do pole Faktura zadejte číslo faktury.
8. Zadejte hodnotu do pole Popis.
9. V poli Dobropis zadejte číslo.
10. V poli Nákupní objednávka kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
11. Vyberte nákupní objednávku, kterou jste vytvořili dříve.
12. V poli Schválil(a) kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
13. Vyberte schvalujícího a kliknutím na tlačítko Vybrat tohoto schvalovatele vyberte.
14. Klikněte na položku Zaúčtovat.
15. Zavřete formulář.
16. Zavřete formulář.

## <a name="open-an-invoice-from-the-pool-and-match-it-to-a-purchase-order-to-complete-the-invoice-process"></a>otevřete fakturu z evidence a spárujte ji s nákupní objednávkou pro dokončení procesu fakturace
1. Přejděte na Závazky > Faktury > Evidence faktur.
2. Kliknutím na nákupní objednávku vytvořte fakturu dodavatele z faktury v evidenci.
3. Vyberte fakturu, kterou chcete zkontrolovat.
4. Klepnutím na tlačítko Aktualizovat stav párování dokončete párování.
5. V podokně akcí klikněte na Možnosti.
6. Klikněte na tlačítko Změnit zobrazení.
7. Klikněte na Zobrazení mřížky.
8. Klikněte na položku Zaúčtovat.
9. Zavřete formulář.
10. Přejděte do části Závazky > Dodavatelé > Dodavatelé.
11. Vyberte dodavatele, který se nacházel na nákupní objednávce. Vyberte například dodavatele 1001.
12. Klikněte na odkaz na vybraném řádku v seznamu.
13. V podokně akcí klikněte na možnost Dodavatel.
14. Klikněte na Transakce.
15. Vyberte fakturu, kterou jste vytvořili.
    * Časové rozlišení registru faktur bylo stornováno a zaúčtováno na příslušný účet výdajů.  


