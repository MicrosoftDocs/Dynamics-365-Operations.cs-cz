---
title: Definování zásad auditu pro zdrojové dokumenty
description: Tento postup popisuje způsob nastavení a spuštění pravidel zásad auditu.
author: ryansandness
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysFieldLookUp, SysPolicyListPage, SysPolicy, AuditPolicyRule, SysQueryForm, SysQueryFieldLookUp, AuditPolicyDateSelection, AuditPolicyAdditionalOption, BatchJob, CaseDetail
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a82c3e8e8787beb309b75b73cda36f4ca8031d6f
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "336789"
---
# <a name="define-audit-policies-for-source-documents"></a>Definování zásad auditu pro zdrojové dokumenty

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tento postup popisuje způsob nastavení a spuštění pravidel zásad auditu. Příklad využívá sestavu výdajů s typem Výdaje hotelu. Tato procedura používá ukázkovou společnost USMF. Role auditora obsahuje dostatečná oprávnění k provedení těchto úloh.

1. Přejděte na pracovní plochu pro Audit > Nastavení > Typ pravidla zásad.
2. Klikněte na položku Nová.
3. Zadejte hodnotu do pole Název pravidla.
4. Zadejte nějakou hodnotu do pole Popis.
5. V poli Název dotazu vyberte řádek Sestava výdajů
6. V poli typ dotazu vyberte Agregovat
7. V poli Právnická osoba vyberte právnickou osobu
8. V poli Odkaz na datum dokumentu vyberte Datum a čas úpravy
9. Klikněte na položku Uložit.
10. Přejděte na pracovní plochu pro Audit > Nastavení > Zásady auditu.
11. Klikněte na položku Nová.
12. Zadejte hodnotu do pole Název.
13. Rozbalte část Organizace zásad.
14. Ve stromovém zobrazení vyberte systém Contoso Entertainment System USA.
15. Klepněte na možnost Přidat.
16. Ve stromovém zobrazení vyberte Contoso Consulting.
17. Klepněte na možnost Přidat.
18. Ve stromovém zobrazení vyberte Contoso Retail USA.
19. Klepněte na možnost Přidat.
20. Sbalte část Organizace zásad.
21. Rozbalte část Pravidla zásad.
22. V seznamu vyhledejte a vyberte pravidlo zásad, které již bylo vytvořeno.
23. Klikněte na Vytvořit pravidlo zásad.
24. Do pole Datum platnosti zadejte datum a čas.
25. Klepněte na tlačítko Filtr.
26. V seznamu vyberte řádek pro kategorii výdajů a nastavte podrobnosti o hotelu
27. V poli Kritéria zadejte nebo vyberte hodnotu.
28. Klikněte na kartu Agregovat.
29. Klepněte na možnost Přidat.
30. V seznamu vyberte hodnotu pole pro Částka transakce
31. V poli Pole zadejte nebo vyberte hodnotu.
32. V poli Agregační funkce vyberte "Součet".
33. Klikněte na kartu Seskupit podle.
34. Klepněte na možnost Přidat.
35. V seznamu vyberte hodnotu Zaměstnanec  
36. Klepněte na možnost Přidat.
37. V seznamu vyberte hodnotu Kategorie výdaje
38. V poli Pole zadejte nebo vyberte hodnotu.
39. Klikněte na kartu Má.
40. Klepněte na možnost Přidat.
41. Vyberte Částka transakce
42. V poli Pole zadejte nebo vyberte hodnotu.
43. V poli Agregační funkce vyberte "Součet".
44. Zadejte hodnotu >2000 do pole Kritéria.
45. Klikněte na tlačítko OK.
46. Klepněte na možnost Test.
47. Do pole Počáteční datum pro výběr dokumentů zadejte datum a čas.
48. Do pole Konečné datum pro výběr dokumentů zadejte datum a čas.
49. Klikněte na Spustit test.
50. V podokně akcí klikněte na možnost Zásady auditu.
51. Klikněte na Další možnosti.
52. Do pole Počáteční datum zadejte datum a čas.
53. Do pole Konečné datum zadejte datum a čas.
54. Klepněte na možnost Dávka.
55. Rozbalte sekci Spustit na pozadí.
56. V poli Dávkové zpracování vyberte hodnotu Ano.
57. Klikněte na tlačítko OK.
58. Přejděte na Pracovní plocha auditu > Auditní případy.
59. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
60. Klikněte na odkaz na vybraném řádku v seznamu.
61. Rozbalte sekci Přidružení.
62. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
63. Klikněte na odkaz na vybraném řádku v seznamu.

