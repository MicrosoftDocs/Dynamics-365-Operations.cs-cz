--- 
title: "Vytváření předdefinovaných variant produktů"
description: "Tento postup vás provede vytvořením variant produktu pro základní produkt za pomoci kombinací dimenzí produktu."
author: YuyuScheller
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: fd6e6844b5920ba1364fa0fd5865d89d83789973
ms.contentlocale: cs-cz
ms.lasthandoff: 07/28/2017

---
# <a name="create-predefined-product-variants"></a>Vytváření předdefinovaných variant produktů

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tento postup vás provede vytvořením variant produktu pro základní produkt za pomoci kombinací dimenzí produktu. K vytvoření tohoto postupu je použita ukázková společnost USMF.


## <a name="create-a-product-master"></a>Vytvoření základního produktu
1. Přejděte do nabídky Řízení informací o produktech > Produkty > Základní produkty.
2. Klikněte na položku Nová.
3. Zadejte hodnotu do pole Číslo produktu.
    * Ruční zadání čísla produktu je povinné, pouze není-li nastavena číselná řada pro pole čísla produktu. Jinak řečeno tento krok přeskočte, je-li pro dané pole nastavena číselná řada.  
4. Do pole Název produktu zadejte hodnotu.
5. V poli Skupina dimenze produktu zadejte nebo vyberte hodnotu.
    * Vyberte skupinu dimenzí produktu SizeCol (velikost a barva).  
6. Klikněte na tlačítko OK.

## <a name="add-product-dimensions"></a>Přidání dimenzí produktu
1. Klikněte na Dimenze produktu.
    * Tento příklad ukazuje, jak zadávat dimenze produktu ručně. Rovněž je možné vybrat velikost, barvu nebo skupinu stylů, která obsahuje hodnoty dimenze produktu, které chcete použít.  
2. Klikněte na položku Nová.
3. Označte v seznamu vybraný řádek.
4. V poli Velikost zadejte nebo vyberte hodnotu.
5. Zadejte hodnotu do pole Název.
6. Klepněte na možnost Nový.
7. Označte v seznamu vybraný řádek.
8. V poli Velikost zadejte nebo vyberte hodnotu.
9. Zadejte hodnotu do pole Název.
10. Klikněte na kartu Barvy.
11. Klikněte na položku Nová.
12. Označte v seznamu vybraný řádek.
13. V poli Barva zadejte nebo vyberte hodnotu.
14. Zadejte hodnotu do pole Název.
15. Klepněte na možnost Nový.
16. Označte v seznamu vybraný řádek.
17. V poli Barva zadejte nebo vyberte hodnotu.
18. Zadejte hodnotu do pole Název.
19. Klikněte na položku Uložit.
20. Zavřete stránku.

## <a name="generate-product-variants"></a>Vytvoření variant produktů
1. Klikněte na Varianty produktu.
2. Klikněte na Návrhy variant.
3. Klikněte na Vybrat vše.
    * V tomto příkladu jsou vybrány všechny možné varianty. Pokud se použije pouze podmnožina možných kombinací dimenzí produktu pro vytváření variant, můžete vybrat jednotlivé položky.  
4. Klikněte na položku Vytvořit.
    * Popisy je možné generovat pro všechny vaše varianty na základě kombinace hodnot dimenze produktu. Popisy jsou volitelné.  
5. Klikněte na položku Uložit.

