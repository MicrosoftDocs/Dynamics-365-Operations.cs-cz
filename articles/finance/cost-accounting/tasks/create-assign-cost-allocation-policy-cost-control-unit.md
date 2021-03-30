---
title: Vytvoření zásad přidělování nákladů a jejich přiřazení jednotce řízení nákladů
description: Tento postup slouží k vytváření a přiřazení zásady přidělení nákladů a odpovídajících pravidel k jednotce pro řízení nákladů.
author: ShylaThompson
manager: AnnBe
ms.date: 06/28/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMCostAccountingLedgerPolicyAssignment
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b22dba0106721c095e6ce2e9b76cb9f5267e1c28
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5208720"
---
# <a name="create-and-assign-a-cost-allocation-policy-to-a-cost-control-unit"></a>Vytvoření zásad přidělování nákladů a jejich přiřazení jednotce řízení nákladů

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]