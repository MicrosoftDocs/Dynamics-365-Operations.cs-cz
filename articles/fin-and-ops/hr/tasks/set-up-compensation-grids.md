--- 
title: "Nastavit kompenzační mřížky"
description: "Kompenzační mřížky umožňují definovat a spravovat struktury plateb pro plány fixní kompenzace."
author: kherr75
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: 33a95e4366dc352f28202155be7fc0b8f4c99e4a
ms.contentlocale: cs-cz
ms.lasthandoff: 07/28/2017

---
# <a name="set-up-compensation-grids"></a>Nastavit kompenzační mřížky

[!include[task guide banner](../../includes/task-guide-banner.md)]

Kompenzační mřížky umožňují definovat a spravovat struktury plateb pro plány fixní kompenzace. Kompenzační mřížky můžete sdílet mezi několika plány nebo zkopírovat při vytvoření nového plánu kompenzace.  Před vytvořením kompenzační mřížky, je nutné nastavit úrovně a referenční body. V tomto příkladu vytvoříme nový typ třídy kompenzační mřížky pomocí ukázkových dat pro úrovně a referenční body. K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.


## <a name="set-up-information-about-the-compensation-grid"></a>Nastavit informace o kompenzační mřížce
1. Přejděte do nabídky Lidské zdroje > Kompenzace > Fixní kompenzace > Kompenzační mřížky.
2. Klikněte na položku Nová.
3. Zadejte hodnotu do pole Mřížka.
4. Zadejte nějakou hodnotu do pole Popis.
5. Vyberte volbu v poli Typ.
6. V poli Nastavení reference zadejte nebo vyberte hodnotu.
7. V poli Měna zadejte nebo vyberte hodnotu.
8. Zadejte hodnotu do pole Měna.
9. Zadejte datum do pole Datum platnosti.

## <a name="add-levels-to-the-compensation-structure"></a>Přidání úrovní do kompenzační struktury
1. Klikněte na možnost Struktura kompenzací.
2. Označte v seznamu vybraný řádek.
3. V poli Úroveň zadejte nebo vyberte hodnotu.
4. Klepněte na možnost Nový.
5. Označte v seznamu vybraný řádek.
6. V poli Úroveň zadejte nebo vyberte hodnotu.
7. Klepněte na možnost Nový.
8. Označte v seznamu vybraný řádek.
9. V poli Úroveň zadejte nebo vyberte hodnotu.
10. Klepněte na možnost Nový.
11. Označte v seznamu vybraný řádek.
12. V poli Úroveň zadejte nebo vyberte hodnotu.
13. Klepněte na možnost Nový.
14. Označte v seznamu vybraný řádek.
15. V poli Úroveň zadejte nebo vyberte hodnotu.

## <a name="fill-in-the-compensation-structure-with-values"></a>Vyplňte hodnoty do kompenzační struktury
1. Označte v seznamu vybraný řádek.
    * V tomto okamžiku lze zadat ručně náhradní hodnoty do každého pole tabulky, nebo lze použít funkci hromadné změny ke snadnému vyplnění více polí a provádění základních výpočtů.  
2. Klikněte na Hromadná změna.
    * U této tabulky nejprve použijeme hodnotu pro středový bod první úrovně ke všem polím v tabulce. To bude základem pro kompenzační matici.  
3. V poli Typ úprav vyberte možnost.
4. Zadejte číslo do pole Částka úpravy.
5. V seznamu označte všechny řádky nebo jejich označení zrušte.
6. Klikněte na Použít na mřížku.
    * Nyní použijeme funkci hromadné změny ke zvýšení částek v jednotlivých úrovních určitým procentem nebo částkou. V tomto příkladu bude mít každá třída rozšíření 12,5 % mezi jejich středními body.  
7. V poli Typ úprav vyberte možnost.
8. Zadejte číslo do pole Částka úpravy.
9. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
10. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
11. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
12. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
13. Klikněte na Použít na mřížku.
14. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
15. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
16. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
17. Klikněte na Použít na mřížku.
18. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
19. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
20. Klikněte na Použít na mřížku.
21. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
22. Klikněte na Použít na mřížku.
    * Nyní použijeme funkci hromadné změny pro úpravu minimálních a maximálních referenčních bodů pro každou úroveň. V tomto příkladu použijeme 50% rozložení, takže minimální referenční bod bude upraven na hodnotou -20 % a maximum bude upraveno na +20 %.  
23. Zadejte číslo do pole Částka úpravy.
24. V poli Referenční bod zadejte nebo vyberte hodnotu.
25. V seznamu označte všechny řádky nebo jejich označení zrušte.
26. Klikněte na Použít na mřížku.
27. Zadejte číslo do pole Částka úpravy.
28. V poli Referenční bod zadejte nebo vyberte hodnotu.
29. V seznamu označte všechny řádky nebo jejich označení zrušte.
30. Klikněte na Použít na mřížku.

