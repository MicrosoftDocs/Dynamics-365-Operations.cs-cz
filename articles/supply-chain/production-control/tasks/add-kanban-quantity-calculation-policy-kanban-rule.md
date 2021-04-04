---
title: Přidání zásad výpočtu kanbanového množství ke kanbanovému pravidlu
description: Tento postup se zaměřuje na vytváření zásad výpočtu kanbanového množství a jejich přidání do kanbanového pravidla pro optimalizaci velikosti a množství kanbanu.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanQuantityPolicy, KanbanRules, KanbanQuantityCalculation
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a32753701c9e06c46ed9b2a9c4b0329f62f15597
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5255462"
---
# <a name="add-a-kanban-quantity-calculation-policy-to-a-kanban-rule"></a>Přidání zásad výpočtu kanbanového množství ke kanbanovému pravidlu

[!include [banner](../../includes/banner.md)]

Tento postup se zaměřuje na vytváření zásad výpočtu kanbanového množství a jejich přidání do kanbanového pravidla pro optimalizaci velikosti a množství kanbanu. K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF. Tento postup je určen pro vedoucího hodnotového proudu. Tento postup je nezbytným předpokladem vytvoření postupu pro výpočet návrhů kanbanového množství. 


## <a name="create-a-kanban-quantity-calculation-policy"></a>Vytvoření zásady pro výpočet kanbanového množství
1. Přejít na Řízení výroby > Pravidelné úlohy > Výpočet kanbanového množství > Zásady pro výpočet kanbanového množství.
2. Klikněte na položku Nová.
3. Zadejte hodnotu do pole Název.
    * Například zadejte Speaker2016.  
4. V poli Hlavní plán kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
5. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
    * Vyberte StaticPlan pro výpočet poptávky.  
6. Klikněte na odkaz na vybraném řádku v seznamu.
7. Klikněte na položku Uložit.
8. Zadejte 1 do pole Minimální kanbanové množství.
    * Toto je další číslo kanbanu, které je zahrnuto do výpočtu kanbanového množství.  
9. Nastavte Bezpečnostní koeficient na 1.
    * Toto je koeficient používaný k výpočtu dodatečného množství pojistných zásob.  
10. V poli Počet dní předem zadejte číslo 30.
    * Toto je počet dní předcházejících výpočtu kanbanového množství, kde je ve výpočtu zahrnuta poptávka.  
11. V poli Počet dní po zadejte číslo 30.
    * Toto je počet dní dopředu od data výpočtu kanbanového množství, kde je ve výpočtu zahrnuta poptávka.  Vzorec použitý pro výpočet se zobrazí a bude obsahovat skutečné hodnoty. Například: Kanbanové množství = ((průměrná denní poptávka x doba realizace x 2.00) / množství produktu na manipulační jednotku) + 1  
12. Zavřete stránku.

## <a name="add-the-kanban-quantity-calculation-policy-to-a-kanban-rule"></a>Přidání zásady pro výpočet kanbanového množství ke kanbanovému pravidlu
1. Přejděte k Řízení informací o produktech > Lean manufacturing > Kanbanová pravidla.
2. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
    * Vyberte kanbanové pravidlo 000020 v tomto postupu.  
3. Klikněte na odkaz na vybraném řádku v seznamu.
4. Přepněte rozšíření oddílu Zásady pro výpočet kanbanového množství.
5. Klepněte na možnost Přidat.
    * Přidejte zásady výpočtu kanbanového množství, které jste právě vytvořili v předchozím podúkolu.  
6. Označte v seznamu vybraný řádek.
7. V poli Název kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
8. Klikněte na odkaz na vybraném řádku v seznamu.
    * Vyberte zásadu Speaker2016, kterou jste právě vytvořili v předchozím podúkolu.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]