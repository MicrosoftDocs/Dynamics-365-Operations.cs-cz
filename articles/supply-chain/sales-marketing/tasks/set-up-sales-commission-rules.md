---
title: Nastavení pravidel prodejních provizí
description: Tento postup popisuje, jak nastavit a povolit výpočet prodejní provize a sledování.
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CommissionCustomerGroup, CommissionItemGroup, CommissionSalesGroup, CommissionSalesMember, DirPartyLookup, CommissionCalc, InventPosting, CustTable, EcoResProductDetailsExtended
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0ed7ec4ca74e4b6863ab2feff7f20de319789038
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "334213"
---
# <a name="set-up-sales-commission-rules"></a>Nastavení pravidel prodejních provizí

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tento postup popisuje, jak nastavit a povolit výpočet prodejní provize a sledování. Procedura zobrazuje postup při vytvoření odběratelů a skupiny provize ze zboží a způsob propojení vybraného odběratele a produktu do odpovídajících skupin. Tyto skupiny jsou použity v nastavení pro výpočet provize k vytvoření kombinace odběratele, zboží a obchodního zástupce, které musí podle prodejní objednávky odpovídat, které opravňují prodejce získat provizi. Vytvoření odběratele a skupin provize ze zboží jsou volitelné, výpočet provize také lze vypočítat jednotlivým odběratelům nebo zboží. Tento postup můžete použít s ukázkovými daty společnosti USMF nebo pomocí vlastních dat.


## <a name="set-up-commission-groups-and-commission-rates"></a>Nastavení skupiny provize a sazeb provizí
1. Přejděte na Prodej a marketing > Provize > Skupiny odběratelů pro provizi.
2. Klikněte na položku Nová.
3. Zadejte hodnotu do pole Skupina.
4. Zadejte hodnotu do pole Název.
5. Klikněte na položku Uložit.
6. Zavřete stránku.
7. Přejděte na Prodej a marketing > Provize > Skupiny zboží.
8. Klikněte na položku Nová.
9. Zadejte hodnotu do pole Skupina.
10. Zadejte hodnotu do pole Název.
11. Zavřete stránku.
12. Přejděte na Prodej a marketing > Provize > Prodejní skupiny.
    * Skupina provizního prodeje určuje zaměstnance v rolích prodejních zástupců, kteří mohou získat provize, když odběratel přidružený ke odpovídající prodejní skupině nakupuje určité položky.  
    * V ukázkové společnosti USMF je prodejní skupina s názvem „Prodejní zástupci USA“.  
13. V podokně akcí klikněte na položku Obecné.
14. Klepněte na Obchodní zástupce.
    * Na stránce Prodejní zástupce se zobrazí seznam osob společnosti z oblasti prodeje, které jsou přidruženy ke konkrétní skupině provize. Můžete přiřadit více prodejních zástupců do stejné skupiny a definovat jejich odpovídající podíl z celkové provize jako procentuální hodnotu. Celková provize sdílená napříč všemi zaměstnanci nesmí překročit 100.  
15. Označte v seznamu vybraný řádek.
16. Klikněte na položku Upravit.
17. Nastavte podíl na provizi na „50“.
18. Klikněte na položku Nová.
19. V poli Název kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
20. Použijte rychlý filtr pro hledání záznamů. Můžete například filtrovat v poli Jméno pomocí hodnoty „Susan Burk“.
21. Klepněte na tlačítko Vybrat.
22. Nastavte podíl na provizi na „50“.
23. Klikněte na položku Uložit.
24. Přejděte na Prodej a marketing > Provize > Výpočet provize.
    * Na stránce výpočtu provize definujete sazbu provize, kterou zaměstnanec obdrží za prodejní transakci, když obsahuje přednastavenou kombinaci odběratele a produktu. Při nastavení sazby provize je nutné zadat základ pro výpočet provize, a zda má zahrnovat nebo vylučovat slevy. Můžete také zadat období platnosti, pokud je sazba provize aktivní.  
25. Klikněte na položku Nová.
26. V poli Kód položky vyberte Skupina.
27. V poli Vztah položky kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
28. V seznamu najděte a vyberte skupinu, kterou jste vytvořili dříve.
29. Klikněte na odkaz na vybraném řádku v seznamu.
30. V poli Kód odběratele vyberte „Skupina“.
31. V poli Vztah odběratele klepnutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
32. V seznamu vyberte skupinu, kterou jste nastavili dříve.
33. V poli Prodejní zástupce klepnutím na tlačítko rozevíracího seznamu otevřete vyhledávání. 
34. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
    * Zachovejte možnost „Před řádkovou slevou“.  
    * Zachovejte možnosti „Výnosu“ jako základ pro výpočet hodnoty provize.    
35. V poli Procento provize je třeba zadat číslo.
36. Klikněte na položku Uložit.

## <a name="setting-up-commission-posting"></a>Nastavení zaúčtování provize
1. Přejděte na Prodej a marketing > Provize > Zaúčtování provize.
    * Provize se vyplácejí zaměstnancům a musí proto být nastaveny pro zajištění správného finančního účtování do příslušných účtů v hlavní knize. To se provádí na stránce zaúčtování provizí. Zkontrolujte nastavení, které je k dispozici pro aktuální společnost. Obvykle jsou částky provize zaúčtovány do vyhrazeného účtu výdajů a jsou vyrovnány do vyhrazených účtů závazků. Pokud nemáte nastavena pravidla zaúčtování provize, systém nedokončí fakturaci prodejní objednávky, která má nárok na provizi.  
2. Zavřete stránku.

## <a name="assign-a-commission-group-to-a-customer-and-a-product"></a>Přiřazení skupiny provize k odběrateli a produktu
1. Přejděte na Prodej a marketing > Odběratelé > Všichni odběratelé.
2. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
3. Klikněte na odkaz na vybraném řádku v seznamu.
4. Klikněte na možnost Upravit.
5. Rozbalte položku Výchozí nastavení prodejních objednávek.
6. V poli Skupina provize klepnutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
7. V seznamu vyberte skupinu, kterou jste vytvořili dříve.
8. V poli Skupina prodeje klepnutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
9. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
10. Klikněte na položku Uložit.
11. Přejděte na možnosti Řízení informací o produktech > Produkty > Uvolněné produkty.
12. Použijte rychlý filtr pro hledání záznamů. Můžete například filtrovat pole Číslo položky pomocí hodnoty „T0020“.
13. Klikněte na odkaz na vybraném řádku v seznamu.
14. Klikněte na možnost Upravit.
15. Rozbalte sekci Prodej.
16. V poli Skupina provize klepnutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
17. V seznamu vyberte skupinu provize, kterou jste vytvořili dříve.

