---
title: Distribuce a plánování dotazníků
description: Tento článek vysvětluje, jak distribuovat dotazníky, které navrhnete, aby byly k dispozici osobě nebo skupině osob, které je mají vyplnit.
author: twheeloc
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: KMConnectionType, KMKnowledgeCollectorPlanningTabel, SysEmailParameters, HcmLearningWorkspace
audience: Application User
ms.custom: 17424
ms.assetid: fd8d867a-2446-400a-b91f-ad4085427470
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 91b2c94c74fd51765a2545424504149fff1f4bfd
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8908854"
---
# <a name="distribute-and-schedule-questionnaires"></a>Distribuce a plánování dotazníků


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tento článek vysvětluje, jak distribuovat dotazníky, které navrhnete, aby byly k dispozici osobě nebo skupině osob, které je mají vyplnit. 

Existuje několik způsobů distribuce dotazníků:

-   Nastavte dotazník jako **Aktivní**. Dotazník bude poté dostupný všem zaměstnancům, potom není skupina dotazníku nastavena na omezení přístupu k ní.
-   Přiřaďte práva ke skupině dotazníku. Dotazník bude poté dostupný všem členům vybrané skupiny.
-   Vytvořte plánované relace odpovědí. Dotazník bude poté dostupný pouze vybrané osobě.
-   Vytvořte plán. Dotazník bude poté k dispozici více osobám.

## <a name="marking-a-questionnaire-as-active"></a>Nastavení dotazníku jako aktivního

Nastavením pole **Aktivní** na možnost **Ano** na stránce **Dotazníky** bude dotazník dostupný pro všechny zaměstnance k vyplnění. Respondenti mohou vyplnit dotazník více než jednou. Tato funkce je užitečná, pokud chcete získávat průběžnou zpětnou vazbu v průběhu roku. Například lze vytvořit dotazník, který zaměstnanci používají k poskytnutí zpětné vazby na obědy v kantýně.

## <a name="questionnaire-groups"></a>Skupiny dotazníků

Můžete nastavit skupiny dotazníků a poté zahrnout respondenty, kterým má být dotazník distribuován. 

Můžete vytvářet skupiny dotazníků z následujících stránek:

-   **Skupiny dotazníků**– Pouze jednotlivci ve skupině dotazníků mohou vyplnit vybraný dotazník. Například vaše cílová skupina jsou dodavatelé, takže můžete vytvořit skupinu dotazníků specifickou pro tyto respondenty.
-   **Členové skupiny dotazníků** – Do skupiny dotazníků lze přidat osoby.

Chcete-li přiřadit skupinu dotazníků k dotazníku, na stránce **Dotazníky** klikněte na možnost **Uživatelská práva**. Po uložení dotazníku jako aktivního mohou členové skupiny dotazníků vyplnit dotazník. Tato funkce je užitečná, pokud chcete otestovat dotazník ve vybrané skupině osob, než jej předáte větší skupině, nebo pokud chcete zaměřit dotazník na velmi specifickou cílovou skupinu.

## <a name="planned-answer-sessions-in-a-questionnaire"></a>Plánované relace odpovědí v dotazníku

Plánované relace odpovědí jsou dotazníky, pro které jste navrhli a vybrali respondenty. 

> [!NOTE]
> Než nastavíte plánované relace odpovědí, je nutné navrhnout dotazník. 

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

Stránku **Typy odkazů** lze použít k nastavení typů odkazů pro dotazník. Každý typ odkazu odpovídá tabulce v aplikaci Microsoft Dynamics 365 Finance. Když vytváříte plány dotazníků, můžete zadat jednotlivé záznamy do tabulky nebo vybrané záznamy, ke kterým bude dotazník přiřazen. 

Například pokud vyberete tabulku Kurzy, můžete se rozhodnout, kterých konkrétních kurzů se bude dotazník týkat. Při nastavování odkaz pro tabulku kurzů budou k dispozici některá pole a tlačítka na stránce **Kurzy**.

### <a name="questionnaire-schedules"></a>Plány dotazníků

Plány dotazníků slouží ke generování několika plánovaných relací odpovědí pro skupinu uživatelů, podle typu odkazu. Vytvořte plán na stránce **Plány dotazníků**. Vyberte typ plánování pro kategorizaci plánu a také vyberte typ odkazu, který má být použit pro dotaz na systém pro konkrétní uživatele. Například při nastavení typu odkazu na tabulku kurzů můžete vybrat konkrétní kurz v poli **Odkaz**. 

Kliknutím na tlačítko **Podrobnosti nastavení** vyberte dotazník a další kritéria. Například pokud dotazník slouží k hodnocení instruktora, zadejte jako kritérium jméno instruktora. Po zadání podrobností nastavení systém vygeneruje plánované relace odpovědí pro uživatele, kteří jsou zahrnuty do dotazu. 

Kliknutím na tlačítko **Plánované relace odpovědí** zobrazíte relace odpovědí pro plán. Můžete pak ručně vytvořit další plánované relace odpovědí nebo odstranit plánované relace odpovědí, které zodpovězeny nebyly. 

Klikněte na tlačítko **Funkce** &gt; **Spustit**, chcete-li dotazník zpřístupnit pro uživatele v souvisejících plánovaných relacích odpovědí. Kliknutím na tlačítko **Odpovědi** zobrazíte dokončené odpovědi v dotazníku. Volitelně můžete zkopírovat nastavení plánu dotazníku, plánované relace odpovědí a odpovědi na nový plán dotazníku.

## <a name="notifying-respondents-about-questionnaires-that-are-available-to-them"></a>Oznámení dostupnosti dotazníků pro respondenty
Při distribuci dotazníku musíte respondenty informovat, že je dotazník k dispozici. 

### <a name="notifying-respondents-about-a-planned-answer-session"></a>Informování respondentů o plánované relaci odpovědí

Pokud používáte plánovou relaci odpovědí, je nutné to dané osobě oznámit přímo, například telefonicky nebo e-mailem.

### <a name="notifying-respondents-about-a-scheduling"></a>Oznámení plánování respondentům

Na stránce **Plány dotazníků** lze připravit a odeslat e-mail všem respondentům přiřazeným k dotazníku. Zadejte text e-mailu na kartě **E-mail pro samoobsluhu pro zaměstnance** kartu. Po spuštění plánu klikněte na **Funkce** &gt; **Odeslat e-mail** pro vygenerování a odeslání e-mailu respondentům. Respondenti se pak mohou přihlásit na webové stránce a vyplnit dotazník. 

> [!NOTE]
> Před použitím funkce e-mailu musí správce IT zadat nastavení e-mailu na stránce **Parametry e-mailu**.

## <a name="ending-a-scheduled-questionnaire"></a>Ukončení plánovaného dotazníku

Plánovaný dotazník lze ukončit, jakmile všichni respondenti vyplní jim přiřazené relace odpovědí. Po ukončení plánovaného dotazníku není možné zkopírovat jeho nastavení do nového plánu. 

> [!NOTE]
>   Pokud některý z respondentů nevyplnil dotazník a přesto chcete ukončit plánování, odstraňte nejprve příslušné respondenty ze seznamu na stránce **Plánovaná relace odpovědí**. Poté můžete ukončit plánování.

## <a name="completing-questionnaires"></a>Vyplňování dotazníků

Po návrhu a distribuci dotazníku mohou vybraní respondenti dotazník vyplnit. Dotazníky, které máte k dispozici, můžete vyplnit ze dvou míst:

-   V navigačním podokně klikněte na možnost **Dotazníky** &gt; **Distribuovat** &gt; **Vyplnit dotazník**.
-   V samoobsluze pro zaměstnance klikněte na tlačítko **Dotazníky k vyplnění**.

Dotazníky lze zpřístupnit pro určité uživatele, skupiny uživatelů nebo všechny uživatele na síti.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
