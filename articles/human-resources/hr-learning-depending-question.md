---
title: Nastavení dotazu jako závislého na odpovědi na předcházející otázku
description: Podmíněné otázky umožňují určit, jaké následující otázky budou prezentovány respondentům na základě odpovědi na předchozí otázku.
author: andreabichsel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KMCollection, KMCollectionQuestion, KMCollectionQuestionTree, HcmLearningWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 67dac872d6dc3a5046f5d554b1f185aa6607d193
ms.sourcegitcommit: 18e626c49ccfdb12c1484b985e3a275e51f61320
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/04/2021
ms.locfileid: "5114997"
---
# <a name="make-a-question-dependent-on-the-answer-of-the-previous-question"></a>Nastavení dotazu jako závislého na odpovědi na předcházející otázku



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

