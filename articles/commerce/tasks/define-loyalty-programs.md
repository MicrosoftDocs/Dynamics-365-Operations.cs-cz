---
title: " Definování věrnostních programů"
description: Tato procedura popisuje, jak nastavit věrnostní program pomocí dvou věrnostních úrovní.
author: jashanno
manager: AnnBe
ms.date: 11/14/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4a853287c0795057b09c429ea1c9ad5231e39a33
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4972298"
---
# <a name="define-loyalty-programs"></a> Definování věrnostních programů

[!include [banner](../includes/banner.md)]

Tato procedura popisuje, jak nastavit věrnostní program pomocí dvou věrnostních úrovní. Tato procedura používá data ukázkové společnosti USRT.

1. Přejděte na Retail and Commerce > .. > Věrnostní programy.
2. Klikněte na možnost Nový.
3. Zadejte hodnotu do pole Název.
4. Zadejte nějakou hodnotu do pole Popis.
5. Klikněte na Přidat řádek.
6. Do pole Úroveň zadejte číslo.
7. Do pole Úroveň zadejte název věrnostní úrovně.
8. Zadejte hodnotu do pole Popis.
9. V poli Časový interval kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
    * Tento časový interval musí být rozšířen do budoucna. Pokud je například časový interval vybraný pro zlatou úroveň jeden rok, kterýkoli odběratel, který je oprávněn pro zlatou úroveň, může získat odměny, které jsou zlaté úrovni přiřazeny, po dobu jednoho roku. Pokud se odběratel znovu kvalifikuje pro zlatou úroveň, když je na této úrovni, datum vypršení jeho stavu bude prodlouženo o další rok od data opětovné kvalifikace.  
10. Klikněte na odkaz na vybraném řádku v seznamu.
11. Klikněte na položku Přidat řádek.
12. Do pole Úroveň zadejte číslo.
13. Do pole Úroveň zadejte název věrnostní úrovně.
14. Zadejte hodnotu do pole Popis.
15. V poli Časový interval kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
16. Klikněte na odkaz na vybraném řádku v seznamu.
17. Klikněte na položku Uložit.
18. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
    * Pravidla úrovně definují minimální počet bodů odměny potřebný k získání během časového období pro získání úrovně.  
19. Přepněte rozšíření oddílu Pravidla úrovně.
20. Klikněte na položku Nová.
    * Pro každou úroveň můžete uchovávat více než jedno pravidlo úrovně. Můžete mít například tři různá kritéria pro získání úrovně; útratu 500 USD v jednom měsíci, útratu 1 000 USD během jednoho roku a provedením 20 transakcí za jeden rok. Chcete-li to provést, je nutné vytvořit tři pravidla úrovní.  
21. V poli Bod odměny kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
    * Tento bod věrnostní odměny by měl být neuplatnitelný.  
22. Klikněte na odkaz na vybraném řádku v seznamu.
23. V poli Minimální počet vydaných bodů zadejte číslo.
    * Pokud se na nejnižší věrnostní úroveň mohou kvalifikovat všichni zákazníci pouhou účastí v programu, zadejte hodnotu „0“.  
24. V poli Interval data hodnocení kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
    * Tento časový interval musí být rozšířen do minulosti. K dosažení minimální hodnoty vydaných bodů budou započítány pouze body získaných v tomto časovém intervalu.  
25. Klikněte na odkaz na vybraném řádku v seznamu.
26. Klikněte na položku Uložit.
27. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
28. Klepněte na možnost Nový.
29. V poli Bod odměny kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
30. Klikněte na odkaz na vybraném řádku v seznamu.
31. V poli Minimální počet vydaných bodů zadejte číslo.
32. V poli Interval data hodnocení kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
    * Tento časový interval musí být rozšířen do minulosti.  
33. Klikněte na odkaz na vybraném řádku v seznamu.
34. Klikněte na položku Uložit.
35. Klikněte na možnost Cenové skupiny.
    * Pokud chcete udělit věrnostní slevy odběratelům. je nutné přiřadit jednu nebo více cenových skupin do věrnostního programu a přiřadit cenové skupiny slevám. Je nejvhodnější pro různé entity typů slev nemíchat cenové skupiny.  Například nepoužívejte stejnou cenovou skupinu pro věrnostní slevy a slevu kanálu.  
36. V poli Cenová skupina kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
    * Propojení Cenové skupiny v horní části stránky je pro věrnostní program. Propojení Cenové skupiny na záložce s náhledem Úrovně programu je určeno pouze konkrétní věrnostní úroveň.  
37. Klikněte na odkaz na vybraném řádku v seznamu.
38. Klikněte na položku Uložit.
39. Zavřete stránku.
40. Klikněte na položku Uložit.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]