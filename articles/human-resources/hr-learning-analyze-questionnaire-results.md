---
title: Analýza výsledků dotazníku
description: Statistiky dotazníku slouží k výpočtu průměrné hodnoty, součtů a procentuální hodnoty na základě demografických údajů.
author: twheeloc
ms.date: 08/26/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KMQuestionnaireStatistics, KMQuestionnaireStatisticsLine, HcmLearningWorkspace
audience: Application User
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1da18dd32363308438b7f9da5b2e04e119e840cb
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/04/2022
ms.locfileid: "8692912"
---
# <a name="analyzing-questionnaire-results"></a>Analýza výsledků dotazníku


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Statistiky dotazníku slouží k výpočtu průměrné hodnoty, součtů a procentuální hodnoty na základě demografických údajů. Chcete-li celý postup spustit, přejděte na **Dotazník** > **Zobrazit a analyzovat výsledky** > **Statistiky dotazníků**. K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.


## <a name="create-a-questionnaire-statistics-record"></a>Vytvoření záznamu statistik pro dotazník
1. Přejděte na **Statistika dotazníků**.
2. Klepněte na možnost **Nový**.
3. Označte v seznamu vybraný řádek.
4. Zadejte hodnotu do pole **Statistika**.
5. Zadejte hodnotu do pole **Popis**.
6. V poli **Dotazník** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
7. Klikněte na odkaz na vybraném řádku v seznamu.
8. Klepněte na kartu **Obecné**.
    * Vyberte, zda chcete zahrnout anonymní výsledky nebo výsledky pracovníků, kontaktů a uchazečů.  
9. Zaškrtněte políčko **Pracovník** nebo jeho zaškrtnutí zrušte.
    * Pokud budete výsledky prohlížet podle služebního věku nebo věku, zadejte intervaly, které chcete používat k seskupování výsledků.  
    * Zadáním 5 pro věkový interval způsobíte seskupení výsledků na základě věkového intervalu pěti let.  
10. V poli **Věk** zadejte číslo.
    * Vyberte, zda chcete spustit výpočet v rámci celého dotazníku, pro každou skupinu výsledků, pro každou otázku nebo pro každý řádek dotazů.  
    * Vyberte, jak si přejete seskupit výsledky.  
    * Například při výpočtu průměrných bodů za otázku můžete zobrazit otázky, které jsou seskupeny podle hodnoty Skupina výsledků.  
    * Vyberte data, na kterých chcete založit výpočet.  
    * Pokud například chcete zobrazit průměrné získané procento v dotazníku mezi pracovníci ve srovnání s průměrným počtem bodů obdržených vašimi pracovníky.  
11. Klikněte na kartu **Rozsah**.
    * Používejte rozsahy pro omezení sady výsledků pouze na ty, které splňují kritéria rozsahu.  
12. Klikněte na kartu **Seskupení podle**.
    * Seskupení slouží k určení toho, jak mají být výsledky zobrazeny.  
    * Například můžete seskupit výsledky podle pohlaví a pak podle věku.  
13. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
    * Přesuňte seskupení do **vybrané** strany a umístěte je požadovaným způsobem.  

## <a name="execute-the-statistics-calculation"></a>Provedení výpočtu statistik
1. Klikněte na tlačítko **Spustit**.
    * Vyberte funkce výpočtu, které chcete provést u výsledků.  
    * Můžete například vytvořit výpočet procentuálního průměru v rámci dotazníku pro vybraná seskupení, nebo celkové body v rámci skupiny výsledků pro vybraná seskupení.  
2. Zaškrtněte nebo zrušte zaškrtnutí políčka **Odstranit předchozí výběry**.
3. Klikněte na tlačítko **OK**.

## <a name="view-the-results-of-the-questionnaire-statistics-run"></a>Zobrazte výsledky provedené statistiky dotazníku.
1. Klikněte na možnost **Výsledky**.
2. Klikněte na možnost **Výsledky**.
3. Zavřete stránku.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
