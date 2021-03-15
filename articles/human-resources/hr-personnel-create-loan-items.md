---
title: Vytvořit položky výpůjček
description: Položky výpůjčky jsou záznamy, které vám pomohou sledovat fyzické položky, jako například telefony nebo počítače, které vaše společnost poskytuje pro zaměstnance.
author: andreabichsel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmLoanType, DefaultDashboard, HcmLoanItem, HcmWorkerLookUp, HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7da578c57be57b55e9175600461549416faa1298
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/06/2021
ms.locfileid: "5130342"
---
# <a name="create-loan-items"></a>Vytvořit položky výpůjček



Položky výpůjčky jsou záznamy, které vám pomohou sledovat fyzické položky, jako například telefony nebo počítače, které vaše společnost poskytuje pro zaměstnance. Každá fyzická položka musí mít odpovídající položku výpůjčky. Každý záznam zapůjčené položky by měl obsahovat popis zapůjčené věci, kdo je za zapůjčení odpovědný a počet dní, které jsou pro půjčku stanoveny. Můžete vytvořit více položek výpůjčky, například klíčů, přístupových karet nebo stejnokrojů současně. K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.


## <a name="create-loan-types"></a>Vytvoření typů výpůjčky
1. Přejděte na Lidské zdroje > Pracovníci > Položky výpůjčky > Typy výpůjčky.
2. Klikněte na položku Nová.
3. Zadejte hodnotu do pole Typ výpůjčky.
4. Zadejte nějakou hodnotu do pole Popis.
5. Zadejte počet dní, který mohou být zapůjčené položky podle tohoto typu půjčky po splatnosti. 
6. Klikněte na položku Uložit.
7. Zavřete stránku.
8. Aktualizujte stránku.

## <a name="create-loan-items"></a>Vytvoření položek výpůjčky
1. Přejděte na Lidské zdroje > Pracovníci > Položky výpůjčky > Položky výpůjčky.
2. Klikněte na Vytvořit položky výpůjček.
3. Do pole Množství zadejte číslo.
4. Zadejte nějakou hodnotu do pole Popis.
5. V poli Typ výpůjčky kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
6. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
7. Klikněte na odkaz na vybraném řádku v seznamu.
8. Zadejte počet dnů, po které může být položka zapůjčena.
    * Výchozí hodnota pole Plánovaný návrat na stránce Vypůjčené vybavení se vypočítá jako součet aktuálního data a tohoto čísla.  
9. V poli Zodpovědná osoba kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
10. Klepněte na tlačítko Vybrat.
11. Zadejte číslo do pole Počáteční hodnota.
12. V poli Interval zadejte požadované číslo.
13. Zadejte hodnotu do pole Formát.
    * Pokud má například počáteční číslo položky výpůjčky hodnotu 10, zadejte do pole Formát dva číselné symboly.  
14. Klikněte na tlačítko OK.
15. Aktualizujte stránku.



[!INCLUDE[footer-include](../includes/footer-banner.md)]