--- 
title: "Vytvořit položky výpůjček"
description: "Položky výpůjčky jsou záznamy, které vám pomohou sledovat fyzické položky, jako například telefony nebo počítače, které vaše společnost poskytuje pro zaměstnance."
author: kherr75
manager: AnnBe
ms.date: 11/01/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations, Talent
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 429b33366ab9ab705a0f31cb9659f58b41689152
ms.contentlocale: cs-cz
ms.lasthandoff: 04/13/2018

---
# <a name="create-loan-items"></a>Vytvořit položky výpůjček

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

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


