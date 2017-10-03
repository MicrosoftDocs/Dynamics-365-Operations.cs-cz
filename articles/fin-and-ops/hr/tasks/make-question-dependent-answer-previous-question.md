--- 
title: "Nastavení dotazu jako závislého na odpovědi na předcházející otázku"
description: "Podmíněné otázky umožňují určit, jaké následující otázky budou prezentovány respondentům na základě odpovědi na předchozí otázku."
author: twheeloc
manager: AnnBe
ms.date: 02/12/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 6e532241d719aa013fcbc0c03f88fbda9cc06b99
ms.contentlocale: cs-cz
ms.lasthandoff: 07/27/2017

---
# <a name="make-a-question-dependent-on-the-answer-of-the-previous-question"></a>Nastavení dotazu jako závislého na odpovědi na předcházející otázku

[!include[task guide banner](../../includes/task-guide-banner.md)]

Podmíněné otázky umožňují určit, jaké následující otázky budou prezentovány respondentům na základě odpovědi na předchozí otázku. Například pokud je dotaz "Máte raději kávu nebo čaj?", je možné logickou následnou otázku určit v závislosti na tom, zda respondent vybere jako odpověď kávu nebo čaj. K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.


## <a name="find-the-existing-questionnaire"></a>Vyhledání existujícího dotazníku
1. Přejděte na Dotazník > Návrh > Dotazníky.
2. Na seznamu vyberte dotazník WorkFH.

## <a name="add-all-questions-and-sub-questions-to-the-questionnaire"></a>Přidání všech otázek a dílčích otázek do dotazníku
1. Klepněte na tlačítko Dotazy.
2. Klikněte na položku Nová.
3. V poli Otázka vyberte otázku číslo 00016.
4. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
5. Klikněte na odkaz na vybraném řádku v seznamu.
6. Klikněte na položku Uložit.
7. Zavřete stránku.

## <a name="set-the-questionnaire-sequence-to-conditional-and-make-the-question-dependent-on-the-appropriate-question"></a>Nastavte pořadí dotazníků na podmíněné a nastavte otázku tak, aby byla závislá na odpovídající otázce
1. Klikněte na položku Upravit.
2. Rozbalte sekci Nastavení.
3. V poli Pořadí otázek vyberte Podmíněné.
4. Klikněte na Podmíněná otázka.
5. Ve stromovém zobrazení vyberte "Otázky/Vysvětlete, proč jste odpověděli na předchozí otázku tak, jak jste odpověděli".
6. V poli Prvotní otázka vyberte otázku 00009.
7. Klikněte na odkaz na vybraném řádku v seznamu.
8. V poli Odpověď zadejte pořadové ID odpovědi pro možnosti odpovědí, na kterých má být otázka závislá. Pro první možnost odpovědi zadejte například 1.
9. Klepněte na tlačítko Uložit.
10. Ve stromovém zobrazení vyberte "Otázky\Jsem placen(a) odpovídajícím způsobem za prováděnou práci".
    * Mějte na paměti, že strom otázek se aktualizuje a odráží závislosti.  


