---
title: Vytvoření dotazu s uzavřeným koncem
description: Dotazy s uzavřeným koncem umožňují poskytovat možnosti, ze kterých si respondent může vybírat.
author: andreabichsel
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KMAnswerCollection, KMAnswer, KMQuestion, HcmLearningWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 41e12e6f35237ea125756b502d5cebed58c6bf55
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5790637"
---
# <a name="create-a-closed-ended-question"></a>Vytvoření dotazu s uzavřeným koncem

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Dotazy s uzavřeným koncem umožňují poskytovat možnosti, ze kterých si respondent může vybírat. Nejprve je nutné vytvořit skupinu odpovědí s odpověďmi, a následně vytvořit dotaz, který bude používat skupinu odpovědí. K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.


## <a name="create-an-answer-group"></a>Vytvoření skupiny odpovědí
1. Přejít na Dotazník > Návrh > Skupiny odpovědí.
2. Klikněte na položku Nová.
3. Zadejte hodnotu do pole Skupina odpovědí.
4. Zadejte nějakou hodnotu do pole Popis.
    * Pomocí funkci Náhodně můžete náhodně umístit odpovědi v jiném pořadí pokaždé, když je pro otázku použita skupina odpovědí.  
5. Klepněte na tlačítko Odpověď.
6. Klikněte na položku Nová.
    * Číselná řada určuje pořadí, v němž se zobrazují odpovědí, pokud není pro skupinu odpovědí vybrána možnost Náhodně.  
    * Body můžete přidělit k odpovědím a použít je pro hodnocení dotazníku.  
7. Do pole Body zadejte číslo.
    * Správnou odpověď můžete nechat označit a určit tak, že vybraná odpověď je správná. Tento údaj lze použít pro hodnocení dotazníku.  
8. Zadejte hodnotu do pole Odpověď.
    * Pokračujte ve vytváření možností výběru odpovědí pro skupinu odpovědí.  
9. Klikněte na položku Nová.
10. Do pole Body zadejte číslo.
11. Zadejte hodnotu do pole Odpověď.
12. Klepněte na možnost Nový.
13. Do pole Body zadejte číslo.
14. Zadejte hodnotu do pole Odpověď.
15. Klepněte na možnost Nový.
16. Do pole Body zadejte číslo.
17. Zadejte hodnotu do pole Odpověď.
18. Klepněte na možnost Nový.
19. Do pole Body zadejte číslo.
20. Zadejte hodnotu do pole Odpověď.
21. Zavřete stránku.
22. Zavřete stránku.

## <a name="create-the-question"></a>Vytvoření dotazu
1. Přejít na Dotazník > Návrh > Otázky.
2. Klikněte na položku Nová.
3. Pole Typ slouží k seskupení příbuzných dotazů.
    * Pro dotazy s uzavřeným koncem můžete použít typy vstupu, jako např. Zaškrtávací políčko, Alternativní tlačítko nebo Pole se seznamem.  
4. Vyberte možnost v poli Typ vstupu.
5. V poli Skupina odpovědí zadejte nebo vyberte hodnotu.
6. Zadejte hodnotu do pole Text.



[!INCLUDE[footer-include](../includes/footer-banner.md)]