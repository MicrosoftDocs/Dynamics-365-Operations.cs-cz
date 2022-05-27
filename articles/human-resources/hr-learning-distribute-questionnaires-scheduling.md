---
title: Distribuce dotazníků s použitím plánování
description: Plánování dotazníků umožňuje plánovat a rozdělovat dotazníky mezi více respondentů.
author: twheeloc
ms.date: 10/28/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KMKnowledgeCollectorPlanningTable, KMKnowledgeCollectorPlanningMulti, SysQueryForm, HcmPersonLookup, KMKnowledgeCollectorPlanning, HcmLearningWorkspace
audience: Application User
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c82f688a3d9366e629eedefd876dd5669bd7ed04
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/04/2022
ms.locfileid: "8691631"
---
# <a name="distribute-questionnaires-using-scheduling"></a>Distribuce dotazníků s použitím plánování


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Plánování dotazníků umožňuje plánovat a rozdělovat dotazníky mezi více respondentů. K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.

## <a name="create-a-questionnaire-schedule"></a>Vytvořte plán dotazníku

1. Přejděte na **Dotazník** > **Distribuovat** > **Plány dotazníků**.

2. Klepněte na možnost **Nový**.

3. Zadejte hodnotu do pole **Plánování**.

4. Zadejte hodnotu do pole **Popis**.
    * Nastavte plán na **Anonymní** v případě, že odpověď by měla být zaznamenána bez jmen přiřazených k odpovědi.  
    * Povolení anonymních výsledků musí být v parametrech HR nejprve nastaveno.  

5. V poli **Typ** vyberte typ plánování.  V tomto příkladu použijeme typ **Spokojenost**.

6. Vyhledejte na seznamu požadovaný záznam a vyberte ho.

7. Klikněte na odkaz na vybraném řádku v seznamu.

8. Do pole **Datum** zadejte datum.

9. Rozbalte oddíl **E-mail pro samoobsluhu pro zaměstnance**.

10. Zadejte hodnotu do pole **Předmět**.

    * Příklad: Dotazník k dispozici  

11. Do pole **Text** zadejte text e-mailové zprávy. Všimněte si, že proměnná slouží k nahrazení hodnot v systému.

    * Příklad: Vážený/á %P%, přihlaste se prosím do Samoobsluhy pro zaměstnance a vyplňte dotazník zdraví pracovníků.  Contoso  

12. Klikněte na tlačítko **Uložit**.

## <a name="use-the-setup-details-to-select-the-questionnaires-to-be-answered-as-well-as-any-queries-to-use-to-select-respondents"></a>Použijte Podrobnosti nastavení pro výběr dotazníků, které chcete zodpovědět společně s dotazy, které chcete použít u vybraných respondentů.

1. Klikněte na **Podrobnosti nastavení**.

2. V seznamu vyberte dotaz, který chcete použít k vyhledání systému pro respondenty dotazníku.

    * Příklad: Pracovníci  

3. Klepněte na tlačítko **Zobrazit nebo upravit dotaz** a vyberte tak určité uživatele nebo upravte dotaz a vyhledejte tak osoby odpovídající konkrétním kritériím.

    * Respondenti musí být také uživateli v systému.  

4. V seznamu označte řádek Osoba.

5. V poli **Kritéria** zadejte nebo vyberte hodnotu.

    * Vyberte Julia Funderburk  

6. V seznamu vyberte Julia Funderburk

7. Klikněte na tlačítko **OK**.

8. Klepněte na kartu **Dotazníky**.

9. Ve stromovém zobrazení rozbalte uzel pro typ dotazníku **Průzkum spokojenosti**.

10. Ve stromové struktuře označte "Posouzení zdravotního stavu pracovníků".

11. Klikněte na tlačítko **OK**.

12. Klikněte na **Plánovaná relace odpovědí**.

    * **Plánované relace odpovědí** byly vytvořeny pro jednotlivé vybrané/dotazované uživatele.  

13. Zavřete stránku.

## <a name="start-the-questionnaire-schedule-in-order-to-make-the-questionnaire-available-for-respondents-to-complete"></a>Zahajte plánování dotazníku, pokud chcete zpřístupnit respondentům dotazník k vyplnění.

1. Klikněte na **Funkce**.

2. Klikněte na tlačítko **Spustit**.

3. Klikněte na tlačítko **OK**.

## <a name="send-the-email-to-inform-respondents-of-the-available-questionnaire"></a>Odešlete e-mail informující respondenty o dostupném dotazníku.

1. Klikněte na **Funkce**.

2. Klikněte na **Odeslat e-mail**.

3. Klepněte na možnost **Zrušit**.

## <a name="use-planned-answer-sessions-to-monitor-who-needs-to-complete-the-questionnaire"></a>Použijte Plánované relace odpovědí ke sledování toho, kdo má dotazník vyplnit.

1. Klikněte na **Plánovaná relace odpovědí**.

    * Jakmile budete připraveni ukončit plánovanou relaci, odstraňte veškeré zbývající plánované relace odpovědí.  

2. Klepněte na tlačítko **Odstranit**.

3. Klepněte na tlačítko **Ano**.

4. Zavřete stránku.

## <a name="end-the-schedule-when-all-respondents-have-completed-the-questionnaire-andor-all-remaining-planned-answer-sessions-have-been-deleted"></a>Poté, co dotazník vyplní všichni respondenti nebo jsou odstraněny všechny zbývající plánované relace odpovědí, plán ukončete.

1. Klikněte na **Funkce**.
2. Klepněte na tlačítko **Konec**.
3. Klikněte na tlačítko **OK**.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
