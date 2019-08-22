---
title: Hromadně vytvořit prodejní nabídky
description: Tento postup ukazuje, jak účinně vytvářet prodejní nabídky nabízející sadu produktů nebo služeb, které mají být zaslány více zákazníkům.
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesQuotationTemplateGroup, SalesQuotationListPage, SalesCreateQuotation, SalesQuotationTable, SysQueryForm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dcf216c65514820dc50486266a79ad1b4d696db3
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/01/2019
ms.locfileid: "1835519"
---
# <a name="mass-create-sales-quotations"></a>Hromadně vytvořit prodejní nabídky

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tento postup ukazuje, jak účinně vytvářet prodejní nabídky nabízející sadu produktů nebo služeb, které mají být zaslány více zákazníkům. Toto hromadné vytvoření nabídky vychází z šablon nabídek. Tento postup můžete použít s ukázkovými daty společnosti USMF nebo pomocí vlastních dat.


## <a name="create-a-quotation-template"></a>Vytvoření šablony nabídek
1. Přejděte na Prodej a marketing > Nastavení > Nabídky > Skupiny šablon.
2. Klikněte na položku Nová.
3. V poli ID skupiny zadejte ID podle vašeho výběru.
4. Zadejte nějakou hodnotu do pole Popis.
5. Klikněte na položku Uložit.
6. Zavřete stránku.
7. Přejděte na Prodej a marketing > Prodejní nabídky > Všechny nabídky.
8. Klikněte na položku Nová.
9. V poli Typ účtu vyberte možnost Odběratel.
10. V poli Účet odběratele zadejte nebo vyberte hodnotu.
11. Klikněte na tlačítko OK.
    * Chcete-li z nabídky vytvořit šablonu, je třeba provést nastavení v záhlaví nabídky. Musíte tak učinit dříve, než do nabídky přidáte řádky.   
12. V podokně akcí klikněte na Možnosti.
13. Klikněte na tlačítko Změnit zobrazení.
14. Klikněte na možnost Zobrazení záhlaví.
15. Rozbalte sekci Nastavení.
16. V poli ID skupiny zboží zadejte nebo vyberte hodnotu.
17. Zadejte hodnotu do pole Název šablony.
18. Vyberte Ano v poli Aktivní.
    * Pouze aktivní šablony lze použít při použití šablony na novou prodejní nabídku.  
19. V podokně akcí klikněte na Možnosti.
20. Klikněte na tlačítko Změnit zobrazení.
21. Klepněte na možnost Řádkové zobrazení.
22. V poli Zboží zadejte nebo vyberte hodnotu.
23. Zadejte hodnotu do pole Zboží.
24. Zavřete stránku.
25. V poli Procento slevy zadejte číslo.
26. Klikněte na Přidat řádek.
27. V poli Zboží zadejte nebo vyberte hodnotu.
28. Zadejte hodnotu do pole Zboží.
29. Zavřete stránku.
30. V poli Jednotková cena zadejte novou cenu nebo změňte stávající.
31. Klikněte na Přidat řádek.
32. V poli Zboží zadejte nebo vyberte hodnotu.
33. Zadejte hodnotu do pole Zboží.
34. Zavřete stránku.
35. Zadejte číslo do pole Množství.
36. V poli Sleva zadejte číslo.
37. Klikněte na položku Uložit.

## <a name="apply-the-template-to-create-a-single-quotation"></a>Použití šablony pro vytvoření jednotlivých nabídek
1. Přejděte na Prodej a marketing > Prodejní nabídky > Všechny nabídky.
    * Všimněte si, že nabídka, kterou jste právě vytvořili, je označena jako šablona.  
2. Klikněte na položku Nová.
3. V poli Typ účtu vyberte možnost Odběratel.
4. V poli Účet odběratele zadejte nebo vyberte hodnotu.
5. Rozbalte sekci Šablona.
6. V poli ID skupiny zboží zadejte nebo vyberte hodnotu.
7. V poli Název šablony nebo vyberte hodnotu.
8. V poli Metoda výpočtu vyberte „Podle hodnot šablony“.
9. Klikněte na tlačítko OK.
    * Nová nabídka byla nyní vytvořena, na základě dat a podmínek šablony.  
10. Zavřete stránku.
11. Zavřete stránku.

## <a name="apply-the-template-to-mass-create-quotations"></a>Použití šablony pro hromadné vytvoření nabídek
1. Přejděte na Prodej a marketing > Prodejní nabídky > Aktualizace nabídky > Hromadné vytvoření nabídek.
2. V poli Typ účtu vyberte možnost Odběratel.
3. V poli ID skupiny zboží zadejte nebo vyberte hodnotu.
4. V poli Název šablony nebo vyberte hodnotu.
5. V poli Metoda výpočtu vyberte „Podle hodnot šablony“.
6. Rozbalte oddíl Záznamy k zahrnutí.
7. Klepněte na tlačítko Filtr.
8. Do pole Kritéria nastavte filtr pro pokrytí rozsahu odběratelů, které chcete zahrnout do tohoto vytvoření hromadné nabídky. Použijte následující formát „Zákazník1…zákazníkN“.
    * Můžete například nastavit filtr na: US-001…US-004  
9. Klikněte na tlačítko OK.
10. Klikněte na tlačítko OK.
11. Přejděte na Prodej a marketing > Prodejní nabídky > Všechny nabídky.
    * Ověřte, zda nabídky byly vytvořeny pro všechny odběratele určené v rutinní hromadné aktualizaci, jak bylo nastaveno ve vybrané šabloně.  

