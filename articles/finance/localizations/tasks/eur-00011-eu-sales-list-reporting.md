---
title: EUR-00011 Nastavení sestav souhrnného hlášení EU
description: Tato úloha vás provede přehledem o předpokladech pro vytváření souhrnného hlášení (EU).
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionRepositoryTable, ERSolutionImport, SysQueryForm, SysQueryFieldLookUp,  TaxTable, TaxGroup, TaxItemGroup, TaxCountryRegionParameters, TaxVATNumTable, IntrastatParameters, CustTable, DirPartyQuickCreateForm
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: epopov
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b44d439bf1e991380fb7273a70e1f69f807c8b25
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/27/2019
ms.locfileid: "2175085"
---
# <a name="eur-00011-set-up-eu-sales-list-reporting"></a>EUR-00011 Nastavení sestav souhrnného hlášení EU

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tato úloha vás provede přehledem o předpokladech pro vytváření souhrnného hlášení (EU). Další informace o výkazu se seznamem prodeje v EU včetně případných požadovaných předpokladů naleznete v nápovědě.

Úkol se vztahuje na všechny evropské země/oblasti. Průvodce byl vytvořen použitím ukázkových dat společnosti DEMF a následně Německa jako příklad pro domácí zemi nebo oblast. Průvodce také využívá Portugalsko jako příklad země nebo oblasti EU.

Tyto úkoly jsou určeny pro správce systému.


## <a name="import-electronic-reporting-configurations-for-eu-sales-list-reporting"></a>Import elektronického vykazování konfigurace pro vytváření souhrnného hlášení EU
1. Přejděte do části Správa organizace > Pracovní prostory > Elektronické výkaznictví.
2. Klikněte na možnost Nastavit jako aktivní.
3. Klikněte na možnost Úložiště.
4. Klikněte na možnost Otevřít.
5. V podokně akcí klikněte na Možnosti.
6. Klepněte na možnost Rozšířený filtr či řazení.
7. Klepněte na možnost Přidat.
8. V poli Pole vyberte „Název konfigurace“.
9. Do pole kritéria zadejte hodnotu „Souhrnné hlášení EU (DE)“.
10. Klikněte na tlačítko OK.
11. Klepněte na tlačítko Importovat.
12. Klepněte na tlačítko Ano.
13. V podokně akcí klikněte na Možnosti.
14. Klepněte na možnost Rozšířený filtr či řazení.
15. Klepněte na možnost Resetovat.
16. Klepněte na možnost Přidat.
17. V poli Pole vyberte „Název konfigurace“.
18. Do pole kritéria zadejte hodnotu „Souhrnné hlášení EU podle řádků“.
19. Klikněte na tlačítko OK.
20. Klepněte na tlačítko Importovat.
21. Klepněte na tlačítko Ano.

## <a name="set-up-sales-tax-codes-for-eu-sales-list-reporting"></a>Nastavte kódy DPH pro vytváření souhrnného hlášení EU
1. Přejděte na Daň > Nepřímé daně > DPH > Kódy DPH.
2. Použijte rychlý filtr k filtrování v poli Kód prodejní daně s hodnotou „DPH19“.
3. Rozbalte část nastavení sestavy.
    * Ověřte, zda je vyloučený výběr nastaven na hodnotu Ne.  
    * Pro změnu tohoto nastavení může být nutné odemknout průvodce úkolem.  

## <a name="set-up-sales-tax-groups-for-eu-sales-list-reporting"></a>Nastavte skupiny DPH pro vytváření souhrnného hlášení EU
1. Přejděte na Daň > Nepřímé daně > DPH > Skupiny DPH.
2. Použijte rychlý filtr k filtrování v poli Skupina prodejní daně s hodnotou „AR-DOM“.
3. Klikněte na možnost Upravit.
4. Rozbalte sekci Nastavení.
5. V seznamu vyberte první řádek.
6. Zaškrtněte políčko Osvobozené od daně.
7. V seznamu vyberte druhý řádek.
8. Zaškrtněte políčko Osvobozené od daně.
9. V seznamu vyberte třetí řádek.
10. Zaškrtněte políčko Osvobozené od daně.

## <a name="set-up-item-sales-tax-groups-for-eu-sales-list-reporting"></a>Nastavte položku skupin DPH pro vytváření souhrnného hlášení EU
1. Přejděte na Daň > Nepřímé daně > DPH > Skupiny prodejní daně položky.
2. Použijte rychlý filtr k filtrování v poli Položka prodejní daně s hodnotou „FULL“.
    * Ověřte, zda je výběr Typ vykazování nastaven na hodnotu „Položka“.  
    * Pro změnu hodnoty v tomto poli může být nutné odemknout průvodce úkolem.  
3. Použijte rychlý filtr k filtrování v poli Položka prodejní daně s hodnotou „RED“.
    * Ověřte, zda je výběr Typ vykazování nastaven na hodnotu „Servis“.  
    * Pro změnu hodnoty v tomto poli může být nutné odemknout průvodce úkolem.  

## <a name="set-up-countryregion-parameters-for-eu-sales-list-reporting"></a>Nastavte parametry země/oblasti pro vytváření souhrnného hlášení EU
1. Přejděte na Daň > Nastavení > DPH > Parametry země/oblasti.
2. Klikněte na položku Nová.
3. V poli Země/oblast zadejte „PRT“.
4. V poli Prodejní daň zadejte „PT“.

## <a name="create-tax-exempt-numbers"></a>Vytvořit čísla osvobození od daně
1. Přejděte na Daň > Nastavení > DPH > DIČ.
2. Klikněte na položku Nová.
3. V poli Země/oblast zadejte „PRT“.
4. Do pole DIČ zadejte „PT12345“.

## <a name="set-up-eu-sales-list-reporting-parameters"></a>Nastavit parametry sestav souhrnného hlášení EU
1. Přejděte na Daň > Nastavení > Zahraniční obchod > Parametry zahraničního obchodu.
2. Klepněte na kartu souhrnného hlášení EU.
3. Vyberte možnost Ano v poli převodu nákupů.
4. Rozbalte položku Pravidla zaokrouhlování.
5. Nastavit Pravidlo zaokrouhlování na „0,1“.
6. Vyberte možnost Ano v poli Použít minimální hodnotu.
7. Do pole Počet desetinných míst zadejte „2“.
8. Rozbalte část Elektronické výkaznictví.
9. V poli Mapování formátu souboru vyberte „Souhrnné hlášení EU (DE)“.
10. V poli Mapování formátu sestavy vyberte „Souhrnné hlášení EU podle řádků“.
11. Klepněte na kartu vlastností Země/oblasti.
    * Zkontrolujte, že pole typu Země/oblast je nastaveno na hodnotu „Domácí“ pro zemi nebo oblast Německo.  
    * Pro změnu hodnoty v tomto poli může být nutné odemknout průvodce úkolem.  
12. Klikněte na položku Nová.
13. V poli Země/oblast zadejte „PRT“.
14. V poli Kód Intrastat zadejte „PT“.
15. Do zadávacího pole Země/oblast vyberte položku „EU“.
16. Klikněte na kartu Číselné řady.
    * Ověřte, zda je zadán kód číselné řady pro odkaz „Souhrnného hlášení EU“.  

## <a name="create-a-customer-for-eu-sales-list-reporting-demo-purposes"></a>Vytvořit odběratele pro účely ukázky souhrnného hlášení EU
1. Přejděte na Pohledávky > Zákazníci > Všichni odběratelé.
2. Klikněte na položku Nová.
3. V poli Účet odběratele zadejte „PRT-001“.
4. Do pole Název zadejte „Zákazník z Portugalska“.
5. V poli Skupina odběratelů vyberte „10“.
6. V poli Skupina DPH vyberte položku „AR-DOM“.
7. Do pole DIČ vyberte „PT12345“.
8. V poli Země/oblast zadejte „PRT“.
9. Klikněte na položku Uložit.

