--- 
title: "Vytvoření zásad přidělování nákladů a jejich přiřazení jednotce řízení nákladů"
description: "Tento postup slouží k vytváření a přiřazení zásady přidělení nákladů a odpovídajících pravidel k jednotce pro řízení nákladů."
author: YuyuScheller
manager: AnnBe
ms.date: 06/28/2017
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
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 491d8292b7c951be930d2858362c8107caaa76ff
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="create-and-assign-a-cost-allocation-policy-to-a-cost-control-unit"></a>Vytvoření zásad přidělování nákladů a jejich přiřazení jednotce řízení nákladů

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Tento postup slouží k vytváření a přiřazení zásady přidělení nákladů a odpovídajících pravidel k jednotce pro řízení nákladů. Tento záznam používá v ukázkových datech společnost USP2.


## <a name="create-a-policy"></a>Vytvořte zásadu
1. Přejděte na Nákladové účetnictví > Zásady > Zásady přidělení nákladů.
2. Klikněte na položku Nová.
3. Do pole Název zásady zadejte hodnotu.
4. V poli Hierarchie dimenze objektu nákladů zadejte nebo vyberte hodnotu.
    * Vyberte organizaci.  
5. V poli Statistická dimenze zadejte nebo vyberte hodnotu.
6. Klikněte na položku Uložit.

## <a name="create-allocation-rules"></a>Vytvoření pravidel přidělení
1. Klikněte na položku Nová.
2. Označte v seznamu vybraný řádek.
3. V poli Uzel hierarchie dimenze objektu nákladů zadejte nebo vyberte hodnotu.
4. V poli Chování nákladů vyberte Celkem.
5. V poli Základ přidělení zadejte nebo vyberte hodnotu.
6. Klikněte na možnost Nový.
7. Označte na seznamu vybraný řádek.
8. V poli Uzel hierarchie dimenze objektu nákladů zadejte nebo vyberte hodnotu.
9. V poli Chování nákladů vyberte Celkem.
10. V poli Základ přidělení zadejte nebo vyberte hodnotu.
11. Klikněte na možnost Nový.
12. Označte na seznamu vybraný řádek.
13. V poli Uzel hierarchie dimenze objektu nákladů zadejte nebo vyberte hodnotu.
14. V poli Chování nákladů vyberte Celkem.
15. V poli Základ přidělení zadejte nebo vyberte hodnotu.
    * Pokračujte dokud nevytvoříte všechna pravidla.  
16. Klikněte na položku Uložit.

## <a name="assign-the-policy-to-a-cost-control-unit"></a>Přiřazení zásady ke kontrolní jednotce nákladů
1. Klikněte na Přiřazení zásady pro kontrolní jednotky nákladů.
2. Klikněte na položku Nová.
3. Označte v seznamu vybraný řádek.
4. Zadejte datum do pole Platné od data účtování.
    * Pravidla mají časovou platnost. Uživatel nebo systém můžete platnost pravidel ukončit při vytvoření novější verze.  
5. V poli Jednotka řízení nákladů zadejte nebo vyberte hodnotu.
6. Klikněte na položku Uložit.


