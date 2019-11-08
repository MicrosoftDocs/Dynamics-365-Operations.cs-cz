---
title: Vytvoření zásad shrnutí nákladů
description: Tento postup popisuje způsob vytvoření zásad shrnutí nákladů a vytváření pravidel zásad.
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: facffeaf8d880bad01877b420197e29b6791ebbf
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/27/2019
ms.locfileid: "2187767"
---
# <a name="create-a-cost-rollup-policy"></a>Vytvoření zásad shrnutí nákladů

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tento postup popisuje způsob vytvoření zásad shrnutí nákladů a vytváření pravidel zásad. Jako ukázková data pro tento postup slouží data USP2.


## <a name="create-a-policy"></a>Vytvořte zásadu
1. Přejděte na Nákladové účetnictví > Zásady > Zásady shrnutí nákladů.
2. Klikněte na položku Nová.
3. Do pole Název zásady zadejte hodnotu.
4. Zadejte nějakou hodnotu do pole Popis.
5. V poli Hierarchie dimenze objektu nákladů zadejte nebo vyberte hodnotu.
    * Vyberte Shrnutí nákladů CC.  
6. V poli Hierarchie dimenze prvku nákladů zadejte nebo vyberte hodnotu.
    * Vyberte Shrnutí nákladů CC.  
7. Klikněte na položku Uložit.

## <a name="create-rules-for-the-cost-rollup-policy"></a>Vytvoření pravidla pro zásady shrnutí nákladů
1. Klikněte na položku Nová.
2. Označte v seznamu vybraný řádek.
3. V poli Uzel hierarchie dimenze objektu nákladů zadejte nebo vyberte hodnotu.
    * Vyberte 007.  
4. V poli Uzel hierarchie dimenze prvku nákladů zadejte nebo vyberte hodnotu.
    * Vyberte Shrnutí nákladů CE.  
5. V poli Prvek druhotných nákladů zadejte nebo vyberte hodnotu.
    * V tomto příkladu namapujte sekundární nákladový prvek CC-007 na nákladové středisko.  
6. Klikněte na položku Nová.
7. Označte v seznamu vybraný řádek.
8. V poli Uzel hierarchie dimenze objektu nákladů zadejte nebo vyberte hodnotu.
    * Vyberte 008.  
9. V poli Uzel hierarchie dimenze prvku nákladů zadejte nebo vyberte hodnotu.
    * Vyberte Shrnutí nákladů CE.  
10. V poli Prvek druhotných nákladů zadejte nebo vyberte hodnotu.
    * V tomto příkladu namapujte sekundární nákladový prvek CC-008 na nákladové středisko.  
11. Klikněte na položku Nová.
12. Označte v seznamu vybraný řádek.
13. V poli Uzel hierarchie dimenze objektu nákladů zadejte nebo vyberte hodnotu.
    * Vyberte 009.  
14. V poli Uzel hierarchie dimenze prvku nákladů zadejte nebo vyberte hodnotu.
    * Vyberte Shrnutí nákladů CE.  
15. V poli Prvek druhotných nákladů zadejte nebo vyberte hodnotu.
    * V tomto příkladu namapujte sekundární nákladový prvek CC-009 na nákladové středisko.  
    * Pokračujte, dokud všechna nákladová střediska nejsou namapována na odpovídajících sekundární prvky nákladů.  
16. Klikněte na položku Uložit.
