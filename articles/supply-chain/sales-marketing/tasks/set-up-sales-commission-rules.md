---
title: Nastavení pravidel prodejních provizí
description: Tento postup popisuje, jak nastavit a povolit výpočet prodejní provize a sledování.
author: omulvad
manager: tfehr
ms.date: 06/21/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CommissionCustomerGroup, CommissionItemGroup, CommissionSalesGroup, CommissionSalesMember, DirPartyLookup, CommissionCalc, InventPosting, CustTable, EcoResProductDetailsExtended, CommissionEmplSalesGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2b1ea016817462269a13e450c8c7576546c7f0eb
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4423738"
---
# <a name="set-up-sales-commission-rules"></a>Nastavení pravidel prodejních provizí

[!include [banner](../../includes/banner.md)]

Tento postup popisuje, jak nastavit a povolit výpočet prodejní provize a sledování. Procedura zobrazuje postup při vytvoření odběratelů a skupiny provize ze zboží a způsob propojení vybraného odběratele a produktu do odpovídajících skupin. Tyto skupiny jsou použity v nastavení pro výpočet provize k vytvoření kombinace odběratele, zboží a obchodního zástupce, které musí podle prodejní objednávky odpovídat, které opravňují prodejce získat provizi. Vytvoření odběratele a skupin provize ze zboží jsou volitelné, výpočet provize také lze vypočítat jednotlivým odběratelům nebo zboží. Tento postup můžete použít s ukázkovými daty společnosti USMF nebo pomocí vlastních dat.


## <a name="set-up-commission-groups-and-commission-rates"></a>Nastavení skupiny provize a sazeb provizí
1. Přejděte na **Navigační podokno > Prodej a marketing > Provize > Skupiny odběratelů pro provizi**.
2. Zvolte **Nové**.
3. Zadejte hodnotu do pole **Skupina**.
4. Zadejte hodnotu do pole **Název**.
5. Zvolte **Uložit**.
6. Zavřete stránku.
7. Přejděte na **Navigační podokno > Prodej a marketing > Provize > Skupiny položek**.
8. Zvolte **Nové**.
9. Zadejte hodnotu do pole **Skupina**.
10. Zadejte hodnotu do pole **Název**.
11. Zvolte **Uložit**.
12. Zavřete stránku.
13. Přejděte na **Prodej a marketing > Provize > Prodejní skupiny**.
    - Skupina provizního prodeje určuje zaměstnance v rolích prodejních zástupců, kteří mohou získat provize, když odběratel přidružený ke odpovídající prodejní skupině nakupuje určité položky.  
    - V ukázkové společnosti USMF je prodejní skupina s názvem „Prodejní zástupci USA“.  
14. V **podokně akcí** klikněte na možnost **Obecné**.
15. Klikněte na **Obchodní zástupce**. Na stránce Prodejní zástupce se zobrazí seznam osob společnosti z oblasti prodeje, které jsou přidruženy ke konkrétní skupině provize. Můžete přiřadit více prodejních zástupců do stejné skupiny a definovat jejich odpovídající podíl z celkové provize jako procentuální hodnotu. Celková provize sdílená napříč všemi zaměstnanci nesmí překročit 100. 
16. Označte na seznamu vybraný řádek.
17. Vyberte možnost **Upravit**.
18. Nastavte **podíl na provizi** na „50“.
19. Klepněte na možnost **Nový**.
20. V poli **Název** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
21. Použijte **rychlý filtr** k hledání záznamů. Můžete například filtrovat v poli Jméno pomocí hodnoty „Susan Burk“.
22. Klepněte na tlačítko **Vybrat**.
23. Nastavte **podíl na provizi** na „50“.
24. Klikněte na možnost **Uložit**.
25. Přejděte na **Prodej a marketing > Provize > Výpočet provize**. Na stránce **Výpočet provize** definujete sazbu provize, kterou zaměstnanec obdrží za prodejní transakci, když obsahuje přednastavenou kombinaci odběratele a produktu. Při nastavení sazby provize je nutné zadat základ pro výpočet provize, a zda má zahrnovat nebo vylučovat slevy. Můžete také zadat období platnosti, pokud je sazba provize aktivní.  
26. Klepněte na možnost **Nový**.
27. V poli **Kód položky** vyberte Skupina.
28. V poli **Vztah položky** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
29. V seznamu najděte a vyberte skupinu, kterou jste vytvořili dříve.
30. V poli **Kód odběratele** vyberte „Skupina“.
31. V poli **Vztah odběratele** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
32. V seznamu vyberte skupinu, kterou jste nastavili dříve.
33. V poli **Prodejní zástupce** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
34. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
    - Zachovejte možnost „Před řádkovou slevou“.  
    - Zachovejte možnosti „Výnosu“ jako základ pro výpočet hodnoty provize.    
35. V poli Procento provize je třeba zadat číslo.
36. Klikněte na možnost **Uložit**.

## <a name="setting-up-commission-posting"></a>Nastavení zaúčtování provize
1. Přejděte na **Navigační podokno > Prodej a marketing > Provize > Zaúčtování provize**. Provize se vyplácejí zaměstnancům a musí proto být nastaveny pro zajištění správného finančního účtování do příslušných účtů v **hlavní knize**. To se provádí na stránce **Zaúčtování provizí**. Zkontrolujte nastavení, které je k dispozici pro aktuální společnost. Obvykle jsou částky provize zaúčtovány do vyhrazeného účtu výdajů a jsou vyrovnány do vyhrazených účtů závazků. Pokud nemáte nastavena pravidla zaúčtování provize, systém nedokončí fakturaci prodejní objednávky, která má nárok na provizi.  
2. Zavřete stránku.

## <a name="assign-a-commission-group-to-a-customer-and-a-product"></a>Přiřazení skupiny provize k odběrateli a produktu
1. Přejděte na **Navigační podokno > Moduly > Prodej a marketing > Zákazníci > Všichni zákazníci**.
2. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
3. Klikněte na odkaz na vybraném řádku v seznamu.
4. Klikněte na možnost **Upravit**.
5. Rozbalte položku **Výchozí nastavení prodejních objednávek**.
6. V poli **Skupina provize** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
7. V seznamu vyberte skupinu, kterou jste vytvořili dříve.
8. V poli **Skupina prodeje** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
9. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
10. Klikněte na možnost **Uložit**.
11. Klikněte na **Navigační podokno > Moduly > Řízení informací o produktech > Produkty > Vydané produkty**.
12. Použijte **rychlý filtr** k hledání záznamů. Můžete například filtrovat pole Číslo položky pomocí hodnoty „T0020“.
13. Klikněte na odkaz na vybraném řádku v seznamu.
14. Klikněte na možnost **Upravit**.
15. Rozbalte sekci **Prodej**.
16. V poli **Skupina provize** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
17. V seznamu vyberte skupinu provize, kterou jste vytvořili dříve.
18. Zvolte **Uložit**.

