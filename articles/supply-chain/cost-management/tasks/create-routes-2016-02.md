--- 
title: "Vytváření postupů (jen ve verzi z února 2016)"
description: "Tato úloha je zaměřena na vytvoření výrobních postupů pro dokončený produkt a polotovar produktu."
author: BibiSp
manager: AnnBe
ms.date: 02/07/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 273ced77a61d485426c0830556e4401e782e86c4
ms.openlocfilehash: 1ba2ae3ad92149636714701448d4dac8296d6613
ms.contentlocale: cs-cz
ms.lasthandoff: 10/24/2017

---
# <a name="create-routes-february-2016-only"></a>Vytváření postupů (jen ve verzi z února 2016)

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tato úloha je zaměřena na vytvoření výrobních postupů pro dokončený produkt a polotovar produktu. Je to pátá úloha v řadě Kalkulace kusovníku. Tento úkol byl vytvořen pomocí ukázkových dat společnosti USMF.


## <a name="create-a-route-for-a-semi-finished-product"></a>Vytvoření postupu pro polotovar produktu
1. Přejděte na možnosti Řízení informací o produktech > Produkty > Uvolněné produkty.
2. Klikněte na odkaz na vybraném řádku v seznamu.
    * Vyberte číslo položky BOM_2.  
3. V podokně akcí klikněte na možnost Analýza.
4. Klikněte na Postup.
5. Klikněte na položku Nová.
6. Klikněte na Postup a verze postupu.
7. Zadejte nějakou hodnotu do pole Popis.
    * Zadejte například ROUTE_2.  
8. V poli Lokalita zadejte nebo vyberte hodnotu.
    * V tomto příkladu zadejte nebo vyberte Pracoviště 1.  
9. Klikněte na tlačítko OK.
10. Klikněte na položku Nová.
11. V poli Operace zadejte nebo vyberte hodnotu.
    * V tomto příkladu vyberte Sestavení.  
12. Do pole Operační čas zadejte číslo.
    * Zadejte například 1. Operační časy jsou často zahrnuté v ceně vypočtené pro položku.  
13. V poli Skupina postupů zadejte nebo vyberte hodnotu.
    * V tomto příkladu vyberte Std.  
14. Klikněte na záložku Nastavení.
15. V poli Kategorie nastavení zadejte nebo vyberte hodnotu.
    * V tomto příkladu vyberte Sestavení.  
16. Klepněte na kartu Časy.
17. Do pole Přípravný čas zadejte číslo.
    * V tomto příkladu zadejte 1. Přípravný čas je často zahrnutý v ceně vypočtené pro položku.  
18. V podokně akcí klikněte na možnost Verze postupu.
19. Klepněte na možnost Schválit.
20. Vyberte Ano v poli Chcete postup také schválit? .
21. Klikněte na tlačítko OK.
22. V podokně akcí klikněte na možnost Verze postupu.
23. Klepněte na tlačítko Aktivovat.
24. Zavřete stránku.
25. Zavřete stránku.

## <a name="create-a-route-for-a-finished-product"></a>Vytvoření postupu pro dokončený produkt
1. Klikněte na odkaz na vybraném řádku v seznamu.
    * Vyberte číslo položky BOM_1.  
2. V podokně akcí klikněte na možnost Analýza.
3. Klikněte na Postup.
4. Klikněte na položku Nová.
5. Klikněte na Postup a verze postupu.
6. Zadejte nějakou hodnotu do pole Popis.
    * Pro tento příklad zadejte ROUTE_1.  
7. V poli Lokalita zadejte nebo vyberte hodnotu.
    * V tomto příkladu zadejte nebo vyberte Pracoviště 1.  
8. Klikněte na tlačítko OK.
9. Klikněte na položku Nová.
10. V poli Operace zadejte nebo vyberte hodnotu.
    * V tomto příkladu vyberte Balení.  
11. Do pole Operační čas zadejte číslo.
    * V tomto příkladu zadejte 1.  
12. V poli Skupina postupů zadejte nebo vyberte hodnotu.
    * V tomto příkladu vyberte Std.  
13. Klikněte na záložku Nastavení.
14. V poli Kategorie nastavení zadejte nebo vyberte hodnotu.
    * V tomto příkladu vyberte Balení.  
15. Klepněte na kartu Časy.
16. Do pole Přípravný čas zadejte číslo.
    * V tomto příkladu zadejte 1.  
17. V podokně akcí klikněte na možnost Verze postupu.
18. Klepněte na možnost Schválit.
19. Klikněte na tlačítko OK.
20. V podokně akcí klikněte na možnost Verze postupu.
21. Klepněte na tlačítko Aktivovat.
22. Zavřete stránku.
23. Zavřete stránku.

## <a name="enable-automatic-consumption-of-setup-time"></a>Aktivace automatické spotřeby přípravného času
1. Přejděte k Řízení výroby > Nastavení > Postupy > Skupiny postupu.
2. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
    * V seznamu vyberte položku Std.  
3. Klikněte na položku Upravit.
4. Vyberte Ano v poli Přípravný čas.
    * Přípravný čas je často zahrnutý v ceně vypočtené pro položku.  
5. Klikněte na položku Uložit.
6. Zavřete stránku.


