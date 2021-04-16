---
title: Definování zásad auditu pro zdrojové dokumenty
description: Toto téma vysvětluje způsob nastavení a spuštění pravidel zásad auditu.
author: panolte
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysFieldLookUp, SysPolicyListPage, SysPolicy, AuditPolicyRule, SysQueryForm, SysQueryFieldLookUp, AuditPolicyDateSelection, AuditPolicyAdditionalOption, BatchJob, CaseDetail
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 62ebe3d6ba1208bd5f9a2082969b1960c413c152
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5836954"
---
# <a name="define-audit-policies-for-source-documents"></a>Definování zásad auditu pro zdrojové dokumenty

[!include [banner](../../includes/banner.md)]

Toto téma vysvětluje způsob nastavení a spuštění pravidel zásad auditu. Příklad využívá sestavu výdajů s typem Výdaje hotelu. Tato procedura používá ukázkovou společnost USMF. Role auditora obsahuje dostatečná oprávnění k provedení těchto úloh.

1. V navigačním podokně přejděte na **Moduly > Pracovní plocha auditu > Nastavení > Typ pravidla zásad**.
2. Zvolte **Nové**.
3. Zadejte hodnotu do pole **Název pravidla**.
4. Zadejte hodnotu do pole **Popis**.
5. V poli **Název dotazu** vyberte **Řádek sestavy výdajů**
6. V poli **Typ dotazu** vyberte **Agregovat**
7. V poli **Právnická osoba** vyberte **právnickou osobu**
8. V poli **Odkaz na datum dokumentu** vyberte **Datum a čas úpravy**
9. Zvolte **Uložit**.
10. V navigačním podokně přejděte na **Moduly > Pracovní plocha auditu > Nastavení > Zásady auditu**.
11. Zvolte **Nové**.
12. Zadejte hodnotu do pole **Název**.
13. Rozbalte část **Organizace zásad**.
14. Ve stromovém zobrazení vyberte **Contoso Entertainment System USA** a pak zvolte **Přidat**.
15. Ve stromovém zobrazení vyberte **Contoso Consulting USA** a pak zvolte **Přidat**.
16. Ve stromovém zobrazení vyberte **Contoso Retail USA** a pak zvolte **Přidat**.
17. Sbalte část **Organizace zásad**.
18. Rozbalte část **Pravidla zásad**.
19. V seznamu vyhledejte a vyberte pravidlo zásad, které již bylo vytvořeno.
20. Vyberte **Vytvořit pravidlo zásad**.
21. Do pole **Datum platnosti** zadejte datum a čas.
22. Vyberte **Filtr**.
23. V seznamu vyberte řádek pro **kategorii výdajů** a nastavte podrobnosti o **hotelu**.
24. V poli **Kritéria** zadejte nebo vyberte hodnotu.
25. Vyberte karu **Agregovat**.
26. Vyberte **přidat**.
27. V seznamu vyberte hodnotu pole **Částka transakce**.
28. V poli **Pole** zadejte nebo vyberte hodnotu.
29. V poli **Agregační funkce** vyberte **Součet**.
30. Vyberte kartu **Seskupit podle**.
31. Vyberte **přidat**.
32. V seznamu vyberte hodnotu **Zaměstnanec**.
33. Vyberte **přidat**.
34. V seznamu vyberte hodnotu **Kategorie výdaje**.
35. V poli **Pole** zadejte nebo vyberte hodnotu.
36. Vyberte kartu **Má**.
37. Vyberte **přidat**.
38. Vyberte **Částka transakce**.
39. V poli **Pole** zadejte nebo vyberte hodnotu.
40. V poli **Agregační funkce** vyberte **Součet**.
41. Zadejte hodnotu `>2000` do pole **Kritéria**.
42. Vyberte **OK**.
43. Vyberte **Test**.
44. Do pole **Počáteční datum pro výběr dokumentů** zadejte datum a čas.
45. Do pole **Konečné datum pro výběr dokumentů** zadejte datum a čas.
46. Vyberte **Spustit test**.
47. V podokně akcí zvolte **Zásady auditu**.
48. Vyberte **Další možnosti**.
49. Do pole **Počáteční datum** zadejte datum a čas.
50. Do pole **Koncové datum** zadejte datum a čas.
51. Vyberte **Dávka**.
52. Rozbalte sekci **Spustit na pozadí**.
53. V poli **Dávkové zpracování** vyberte hodnotu **Ano**.
54. Vyberte **OK**.
55. V navigačním podokně přejděte na **Moduly > Pracovní plocha auditu > Nastavení > Případy auditu**.
56. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
57. Rozbalte sekci **Přidružení**.
58. Vyhledejte na seznamu požadovaný záznam a vyberte ho.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]