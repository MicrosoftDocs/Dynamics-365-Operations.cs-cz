---
title: Vytvoření zásad chování nákladů a jejich přiřazení jednotce řízení nákladů
description: Chování nákladů je klasifikace nákladů jako fixních nebo variabilních.
author: ShylaThompson
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CAMCostBehaviorRule
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 77e79b4959d546fd04c9705220c7f7a4c4a0ffd0621a66553adbe1a85b6cce39
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6712260"
---
# <a name="create-and-assign-a-cost-behavior-policy-to-a-cost-control-unit"></a>Vytvoření zásad chování nákladů a jejich přiřazení jednotce řízení nákladů

[!include [banner](../../includes/banner.md)]

Chování nákladů je klasifikace nákladů jako fixních nebo variabilních. Zásady a odpovídající pravila musí být přiděleny jednotce řízení nákladů, aby mohly zásady vstoupit v platnost. Tento postup slouží k vytváření zásady a její přidělení k jednotce pro řízení nákladů.


## <a name="create-a-cost-behavior-hierarchy"></a>Vytvoření hierarchie chování nákladů
1. Přejděte na Nákladové účetnictví > Dimenze > Hierarchie dimenzí.
2. Klikněte na položku Nová.
3. Klikněte na položku Vytvořit.
4. V poli Název hierarchie dimenzí zadejte Hierarchie chování nákladů.
5. V poli Dimenze zadejte nebo vyberte hodnotu.
    * Vyberte Prvky nákladů.  
6. Klikněte na položku Uložit.
7. Klikněte na Zobrazit hierarchii.
8. Klikněte na položku Nová.
9. Do pole Název uzlu zadejte hodnotu.
    * Zadejte Pevné náklady.  
10. Ve stromové struktuře vyberte Hierarchie chování nákladů.
11. Klikněte na položku Nová.
12. Do pole Název uzlu zadejte hodnotu.
    * Zadejte variabilní náklady.  
13. Klikněte na položku Uložit.
14. Ve stromové struktuře vyberte Hierarchie chování nákladů\Pevné náklady.
15. Klikněte na položku Nová.
16. Označte v seznamu vybraný řádek.
17. V poli Od členu dimenze zadejte nebo vyberte hodnotu.
    * Rozsah členů dimenze může obsahovat mezery, ale členové se nesmí překrývat.  
18. V poli Po člen dimenze zadejte nebo vyberte hodnotu.
    * Rozsah členů dimenze může obsahovat mezery, ale členové se nesmí překrývat.  
19. Ve stromové struktuře vyberte Hierarchie chování nákladů\Variabilní náklady.
20. Klikněte na položku Nová.
21. Označte v seznamu vybraný řádek.
22. V poli Od členu dimenze zadejte nebo vyberte hodnotu.
    * Rozsah členů dimenze může obsahovat mezery, ale členové se nesmí překrývat.  
23. V poli Po člen dimenze zadejte nebo vyberte hodnotu.
    * Rozsah členů dimenze může obsahovat mezery, ale členové se nesmí překrývat.  
24. Klikněte na položku Uložit.

## <a name="create-the-policy-and-rules"></a>Vytvoření zásad a pravidel
1. Přejděte na Nákladové účetnictví > Zásady > Zásady chování nákladů.
2. Klikněte na položku Nová.
3. Do pole Název zásady zadejte hodnotu.
4. V poli Hierarchie dimenze prvku nákladů zadejte nebo vyberte hodnotu.
    * Vyberte hierarchii zásady, kterou jste právě vytvořili.  
5. V poli Hierarchie dimenze objektu nákladů zadejte nebo vyberte hodnotu.
    * Vyberte organizaci.  
6. Klikněte na položku Uložit.
7. Klikněte na položku Nová.
8. Označte v seznamu vybraný řádek.
9. V poli Uzel hierarchie dimenze prvku nákladů zadejte nebo vyberte hodnotu.
    * Rozbalte hierarchii a vyberte Variabilní náklady.  
10. V poli Uzel hierarchie dimenze objektu nákladů zadejte nebo vyberte hodnotu.
    * Výchozí procentuální hodnota proměnné je 100 procent.  
11. Klikněte na Přiřazení zásady pro kontrolní jednotky nákladů.
12. Klikněte na položku Nová.
13. Označte v seznamu vybraný řádek.
14. Zadejte datum do pole Platné od data účtování.
    * Pravidla jsou platná od data a platnost pravidla může ukončit uživatel nebo systém v případě vytvoření novější verze.  
15. V poli Jednotka řízení nákladů zadejte nebo vyberte hodnotu.
16. Klikněte na položku Uložit.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]