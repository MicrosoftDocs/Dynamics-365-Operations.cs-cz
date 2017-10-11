--- 
title: "Vytvoření kusovníku pro základní produkt založený na dimenzích"
description: "V tomto postupu je vhodné mít dokončené 4 předchozí průvodce v tomto pořadí z osmi záznamů."
author: YuyuScheller
manager: AnnBe
ms.date: 06/21/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: ae42eb317368fe14b043bc375f04cb11aaba8d5a
ms.contentlocale: cs-cz
ms.lasthandoff: 07/28/2017

---
# <a name="create-a-bill-of-materials-for-a-dimension-based-product-master"></a>Vytvoření kusovníku pro základní produkt založený na dimenzích

[!include[task guide banner](../../includes/task-guide-banner.md)]

V tomto postupu je vhodné mít dokončené 4 předchozí průvodce v tomto pořadí z osmi záznamů. První 4 záznamy jsou věnovány nastavení data potřebného k dokončení tohoto postupu. K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF. Tento úkol obvykle zpracovává návrhář produktu.


## <a name="select-the-product"></a>Výběr produktu
1. Klikněte na možnost Údržba uvolněného produktu.
2. Klepněte na možnost Uvolněné produkty.
3. Označte v seznamu vybraný řádek.
    * Vyhledejte uvolněný základní produkt s konfigurací založenou na dimenzích, kterou jste vytvořili v rámci příručky pro první úlohy v tomto pořadí.  
4. V podokně akcí klikněte na možnost Analýza.
5. Klepněte na Verze kusovníku.

## <a name="create-new-bom-and-bom-version"></a>Vytvoření nového kusovníku a verze kusovníku
1. Klikněte na položku Nová.
2. Klikněte na Kusovník a verze kusovníku.
3. Zadejte hodnotu do pole Název.
    * Nastavení pracoviště  
    * V tomto postupu nebudeme nastavovat konkrétní pracoviště pro kusovník.  
4. Klikněte na tlačítko OK.
5. Klikněte na položku Nová.
    * V tomto postupu přidáme čtyři řádky do kusovníku. Dva řádky představují možnosti pro kabel a dva řádky představují možnosti pro kabinet.  
6. Označte v seznamu vybraný řádek.
7. V poli Číslo zboží zadejte nebo vyberte hodnotu.
    * Vyberte číslo položky A0001, kabely HDMI 6'.  
8. V poli Konfigurační skupina zadejte nebo vyberte hodnotu.
    * Vyberte skupinu konfigurace kabelu vytvořenou v příručce 4 v tomto pořadí.  
9. Klikněte na položku Nová.
    * Vyberte číslo položky A0002, kabely HDMI 12'.  
10. Označte v seznamu vybraný řádek.
11. V poli Číslo zboží zadejte nebo vyberte hodnotu.
12. V poli Konfigurační skupina zadejte nebo vyberte hodnotu.
    * Vyberte znovu skupinu konfigurace kabelu.  
13. Klikněte na položku Nová.
14. Označte v seznamu vybraný řádek.
15. V poli Číslo zboží zadejte nebo vyberte hodnotu.
    * Výběr číslo položky D0002 kabinet.  
16. V poli Konfigurační skupina zadejte nebo vyberte hodnotu.
    * Vyberte skupinu konfigurace kabinetu pro tento řádek kusovníku.  
17. Klikněte na položku Nová.
18. Označte v seznamu vybraný řádek.
19. V poli Číslo zboží zadejte nebo vyberte hodnotu.
    * Vyberte číslo položky M0007 standardní kabinet jako poslední řádek kusovníku.  
20. V poli Konfigurační skupina zadejte nebo vyberte hodnotu.
    * Vyberte skupinu konfigurace kabinetu pro poslední řádek kusovníku.  

## <a name="approve-and-activate"></a>Schválit a aktivovat
1. Zavřete stránku.
2. Klepněte na možnost Schválit.
3. V poli Schválil(a) zadejte nebo vyberte hodnotu.
4. Vyberte Ano v poli Chcete kusovník také schválit? .
5. Klikněte na tlačítko OK.
6. Klepněte na tlačítko Aktivovat.

