---
title: "Distribuce a vyplnění dotazníku"
description: "Toto téma vysvětluje, jak distribuovat dotazníky, které navrhnete, takže jsou k dispozici pro osoby nebo skupiny osob, které budou dokončeny."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: KMConnectionType, KMKnowledgeCollectorPlanningTabel, SysEmailParameters
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 17424
ms.assetid: fd8d867a-2446-400a-b91f-ad4085427470
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: a76ec0cd86bcc810b42ae3cd8efd8a584e6c4da3
ms.openlocfilehash: 8e09c6b042d557e3b2d608fb5e278169fc3c1d88
ms.lasthandoff: 03/31/2017


---

# <a name="distribute-and-complete-a-questionnaire"></a>Distribuce a vyplnění dotazníku

Toto téma vysvětluje, jak distribuovat dotazníky, které navrhnete, takže jsou k dispozici pro osoby nebo skupiny osob, které budou dokončeny. 

Existuje několik způsobů distribuce dotazníků:

-   Nastavte dotazník jako aktivní. Dotazník bude poté dostupný všem zaměstnancům, potom není skupina dotazníku nastavena na omezení přístupu k ní.
-   Přiřaďte práva ke skupině dotazníku. Dotazník bude poté dostupný všem členům vybrané skupiny.
-   Vytvořte plánované relace odpovědí. Dotazník bude poté dostupný pouze vybrané osobě.
-   Vytvořte plán. Dotazník bude poté k dispozici více osobám.

## <a name="marking-a-questionnaire-as-active"></a>Nastavení dotazníku jako aktivního
Nastavením **Active** na **Ano** na **dotazníky** stránky, můžete zpřístupnit dotazník pro všechny zaměstnance k dokončení. Respondenti mohou vyplnit dotazník vícekrát. Tato funkce je užitečná, jestliže chcete shromáždit názory neustále po celý rok. Například lze vytvořit dotazník, který zaměstnanci používají k poskytnutí zpětné vazby na obědy v kantýně.

## <a name="questionnaire-groups"></a>Skupiny dotazníků
Můžete nastavit skupiny dotazníků a poté zahrnout respondenty, kterým má být dotazník distribuován. 

Můžete vytvářet skupiny dotazníků z následujících stránek:

-   **Skupiny dotazníků **– Pouze jednotlivci ve skupině dotazníků mohou vyplnit vybraný dotazník. Například vaše cílová skupina jsou dodavatelé, takže můžete vytvořit skupinu dotazníků specifickou pro tyto respondenty.
-   **Členové skupiny dotazníků** – Do skupiny dotazníků lze přidat osoby.

Chcete-li přiřadit skupinu dotazník dotazník, na **dotazníky** klepněte na tlačítko **uživatelská práva**. Po uložení dotazník jako aktivní členové skupiny dotazníku můžete vyplnit dotazník. Tato funkce je užitečné, pokud chcete otestovat dotazníků na vybranou skupinu osob, než hodíte do větší skupiny nebo pokud se chcete zaměřit dotazníku velmi specifické cílové skupině.

## <a name="planned-answer-sessions-in-a-questionnaire"></a>Plánované relace odpovědí v dotazníku
Plánované relace odpovědí jsou dotazníky, pro které jste navrhli a vybrali respondenty. 

**Poznámka:** Než nastavíte plánované relace odpovědí, je nutné navrhnout dotazník. 

Na stránce **Plánovaná relace odpovědí** můžete vytvořit plánovanou relaci odpovědí pro jednotlivé zaměstnance. V seznamu na stránce jsou zobrazeny všechny plánované dotazníky. 

Plánované relace odpovědí se rovněž použijí na stránce **Plány dotazníků**, kde je možné naplánovat dotazníky pro více osob:

-   Zaměstnanci
-   Účastníci kurzu
-   Organizační jednotky

Každá osoba může odpovídat na dotazník pouze jednou.

## <a name="scheduling-a-questionnaire"></a>Plánování dotazníku
Volitelně můžete naplánovat dotazník pro více respondentů.

### <a name="planning-types"></a>Typy plánování

Typy plánů jsou požadovány, pokud chcete plánovat plánované relace odpovědí pro více respondentů. Typy plánů slouží ke klasifikaci plánů dotazníků. Můžete například naplánovat dotazníky pro následující účely:

-   Hodnocení
-   Průzkum
-   Testování

Typy plánování dotazníku pro plán dotazníku je možné určit na stránce **Plány dotazníků**.

### <a name="reference-types-for-questionnaire"></a>Typy odkazů pro dotazník

Typy odkazů slouží k zadání kritérií pro respondenty, které můžete vybrat při plánování dotazníku. 

Stránku **Typy odkazů** lze použít k nastavení typů odkazů pro dotazník. Každý typ odkazu odpovídá tabulce v 365 Microsoft Dynamics pro operace. Když vytváříte plány dotazníků, můžete zadat jednotlivé záznamy do tabulky nebo vybrané záznamy, ke kterým bude dotazník přiřazen. 

Například pokud vyberete tabulku Kurzy, můžete se rozhodnout, kterých konkrétních kurzů se bude dotazník týkat. Při nastavování odkaz pro tabulku kurzů budou k dispozici některá pole a tlačítka na stránce **Kurzy**.

### <a name="questionnaire-schedules"></a>Plány dotazníků

Plány dotazníků lze generovat více plánovaných relací odpovědí pro skupinu uživatelů, v závislosti na typu odkaz. Na vytvoření plánu **plány dotazníků** stránky. Vyberte typ plánu kategorizace plánování a také vybrat typ odkazu, který má být použit k dotazování systému pro konkrétní uživatele. Například pokud nastavíte typ odkazu na kurzy tabulky, můžete vybrat konkrétní kurz v **odkaz** pole. 

Kliknutím na tlačítko **Podrobnosti nastavení** vyberte dotazník a další kritéria. Například zadejte název instruktora jako kritérium, pokud dotazník hodnocení instruktora. Po zadání nastavení detailů systém generuje plánované relace odpovědí pro uživatele, které jsou zahrnuty v dotazu. 

Kliknutím na tlačítko **Plánované relace odpovědí** zobrazíte relace odpovědí pro plán. Můžete pak ručně vytvořit další plánované relace odpovědí nebo odstranit plánované relace odpovědí, které zodpovězeny nebyly. 

Klepněte na tlačítko **funkce**&gt;**spuštění** aby dotazník k dispozici uživatelům v souvisejících plánovaných relací odpovědí. Kliknutím na tlačítko **Odpovědi** zobrazíte dokončené odpovědi v dotazníku. Volitelně můžete zkopírovat nastavení plánu dotazníku, plánované relace odpovědí a odpovědi na nový plán dotazníku.

## <a name="notifying-respondents-about-questionnaires-that-are-available-to-them"></a>Oznámení dostupnosti dotazníků pro respondenty
Při distribuci dotazníku musíte respondenty informovat, že je dotazník k dispozici. 

**Poznámka:** respondenti musí být uživatelé v 365 Microsoft Dynamics pro operace vyplnit dotazník.

### <a name="notifying-respondents-about-a-planned-answer-session"></a>Informování respondentů o plánované relaci odpovědí

Pokud používáte plánovou relaci odpovědí, je nutné to dané osobě oznámit přímo, například telefonicky nebo e-mailem.

### <a name="notifying-respondents-about-a-scheduling"></a>Oznámení plánování respondentům

Na stránce **Plány dotazníků** lze připravit a odeslat e-mail všem respondentům přiřazeným k dotazníku. Zadejte text e-mailu na kartě **E-mail pro samoobsluhu pro zaměstnance**. Po spuštění plánu, klepněte na tlačítko **funkce**&gt;**odeslat e-mailové** vytvoření a odeslání e-mailu respondentům. Respondenti lze přihlásit k webu a vyplnění dotazníku. 

**Poznámka:** Před použitím funkce e-mailu musí správce IT zadat nastavení e-mailu na stránce **Parametry e-mailu**.

## <a name="ending-a-scheduled-questionnaire"></a>Ukončení plánovaného dotazníku
Plánovaný dotazník lze ukončit, jakmile všichni respondenti vyplní jim přiřazené relace odpovědí. Po ukončení plánovaného dotazníku není možné zkopírovat jeho nastavení do nového plánu. 

**Poznámka:** Pokud některý z respondentů nevyplnil dotazník a přesto chcete ukončit plánování, odstraňte nejprve příslušné respondenty ze seznamu na stránce **Plánovaná relace odpovědí**. Poté můžete ukončit plánování.

## <a name="completing-questionnaires"></a>Vyplňování dotazníků
Po návrhu a distribuci dotazníku mohou vybraní respondenti dotazník vyplnit. Dotazníky, které máte k dispozici, můžete vyplnit ze dvou míst:

-   V navigačním podokně klepněte na **dotazníky**&gt;**rozmístit**&gt;**vyplnit dotazník**.
-   V samoobsluze pro zaměstnance klikněte na tlačítko **Dotazníky k vyplnění**.

Dotazníky lze zpřístupnit pro určité uživatele, skupiny uživatelů nebo všechny uživatele na síti.

<a name="see-also"></a>Viz také
--------

[Vytváření dotazníků](design-questionnaires.md)

[Používání dotazníků](questionnaires.md)

[Zobrazení a vyhodnocení výsledků dotazníků](evaluate-questionnaire-results.md)


