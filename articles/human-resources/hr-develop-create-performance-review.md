---
title: Vytvoření kontrol výkonnosti
description: Tento článek vysvětluje, jak vytvořit kontrolu výkonnosti, a popisuje účel pro každou část kontroly.
author: twheeloc
ms.date: 08/26/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EssWorkspace, HcmDiscussionNewDialog, HcmDiscussion, HcmDiscussionChangeSettings, HcmDiscussionAddGoalDialog, HcmTopicCreate, HcmMeasurementDetailDialog, HcmPerfJournalAdd, HcmEmployeeDevelopmentWorkspace
audience: Application User
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ae2de087f4e345ba826ddbe8a65f917476bd6894
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8872174"
---
# <a name="create-performance-reviews"></a>Vytvoření kontrol výkonnosti


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]


Tento článek vysvětluje, jak vytvořit kontrolu výkonnosti, a popisuje účel pro každou část kontroly. Tato procedura byla vytvořena pomocí ukázkových dat společnosti USMF.

1. Na domovské stránce vyberte pracovní prostor **Samoobsluha pro zaměstnance**.
2. Zvolte **Nová kontrola** a vytvořte novou kontrolu.
3. V poli **Typ kontroly** zadejte nebo vyberte hodnotu.
4. V poli **Období výkonnosti** zadejte nebo vyberte hodnotu.
5. Zadejte datum do pole **Koncové datum**.
6. Vyberte **OK**. Recenzi můžete také vytvořit ze šablony. Toto je nejlepší způsob, jak vytvořit recenzi, protože každá část bude obsahovat informace potřebné k zahájení recenze.  
7. Můžete zobrazit nebo skrýt karty, jako je například karta příloh:

    1. V podokně akcí zvolte **Zobrazit oddíly** a otevřete rozbalovací nabídku dialogového okna.
    1. Zvolte **Ano** nebo **Ne** v poli **Zobrazit přílohy**, chcete-li zobrazit nebo skrýt kartu příloh.
    1. Zvolte **Uložit**.

8. Chcete-li přidat cíl, vyberte možnost **Přidat cíl ke kontrole**. Po dokončení zvolte **OK**.
9. Výběrem možnosti **Přidat kompetenci** otevřete dialogové okno.
10. Zadejte hodnotu do pole **Nadpis**.
11. Do pole **Popis** zadejte `Increase customer skills by working with the support team`.
12. Vyberte **OK**.
13. Vyberte **Sbalit vše**.
14. Vyberte **Rozbalit vše**.
15. Vyberte **Přidat komentář**.
16. Zvolte **Zaúčtovat**.
17. Vyberte kartu **Měření**.
18. Výběrem možnosti **Přidat měření** otevřete nabídku dialogového okna.
19. V poli **Měření** zadejte nebo vyberte hodnotu.
26. Zadejte číslo do pole **Cílová částka**.
20. Vyberte **OK**.
21. Vyberte karu **Aktivity**.
22. Vyberte **přidat**.
23. Zadejte hodnotu do pole **Nadpis**.
24. Zadejte hodnotu do pole **Popis**.
25. Zadejte datum do pole **Počáteční datum**.
26. Do pole **Datum dokončení** zadejte datum.
27. Vyberte možnost **Ano** v poli **Plán rozvoje**.
28. Zadejte hodnotu do pole **Klíčová slova**.
29. Zvolte **Uložit**.
30. Vyberte kartu **Hodnocení**.  

    - Pevná záložka **Podrobnosti hodnocení** umožňuje zaměstnancům hodnotit sebe a manažerům hodnotit zaměstnance. Pokud jsou použity váhy, hodnota váhy skóre se vypočítá automaticky.  
    - Chcete -li zobrazit tuto část, povolte nastavení parametrů pro zobrazování hodnocení zaměstnanců na stránce **Sdílené parametry lidských zdrojů**.  

31. Zvolte kartu **Podpisy**. Používá-li recenze pracovní postup, podpisy se zobrazí pouze po dokončení pracovního postupu. Pokud není použit žádný pracovní postup, pracovník a manažer jsou zde uvedeni. **Požadované** zaškrtávací políčko pro **Odhlášení** je vybráno na základě nastavení typu recenze.  
32. Zvolte kartu **Obecné**.

    - Doba výkonu vytvoří ve výchozím nastavení počáteční a koncové datum. Tato data lze upravovat.  
    - Stavy řídí přístup k přezkoumání. Stav **Nespuštěno** umožňuje všem uživatelům upravit recenzi. Stav **Probíhající** umožňuje zobrazit a upravit recenze pouze zaměstnancům. **Připraveno ke kontrole** umožňuje zobrazovat a upravovat recenze pouze správcům. Stav **Závěrečná recenze** umožňuje zaměstnanci i vedoucímu prohlížet a upravovat recenzi, pokud je v typu recenze vybrána možnost **Povolit úpravy při závěrečné recenzi**. Stavy **Dokončeno** a **Zrušeno** nastavují recenzi jen pro čtení. Pokud je recenze **odmítnuta** a odeslána zpět zaměstnanci, jak zaměstnanec, tak manažer mohou provést nezbytné úpravy, aby je zaměstnanec mohl znovu odeslat.

33. Zadejte hodnotu do pole **Přehled**.
34. Zvolte kartu **Kontrola**. S tím, jak recenze prochází jednotlivými stavy, zaměstnanec a manažer můžou přidávat komentáře pro každý cíl nebo kompetenci.  
35. Vyberte kartu **Podpisy** . Pracovník a manažer se mohou podepsat při kontrole. Po dokončení všech požadovaných podpisů je stav změněn na hodnotu **Dokončeno** a nelze provést žádné další změny.  



[!INCLUDE[footer-include](../includes/footer-banner.md)]
