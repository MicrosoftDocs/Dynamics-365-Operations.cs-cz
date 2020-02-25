---
title: Vytvoření kontrol výkonnosti
description: Tento článek vysvětluje, jak vytvořit kontrolu výkonnosti, a popisuje účel pro každou část kontroly.
author: andreabichsel
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EssWorkspace, HcmDiscussionNewDialog, HcmDiscussion, HcmDiscussionChangeSettings, HcmDiscussionAddGoalDialog, HcmTopicCreate, HcmMeasurementDetailDialog, HcmPerfJournalAdd
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 50ef3f305756f1ab0db895854cd7e1c71237cb48
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008354"
---
# <a name="create-performance-reviews"></a>Vytvoření kontrol výkonnosti



Tento článek vysvětluje, jak vytvořit kontrolu výkonnosti, a popisuje účel pro každou část kontroly. Tato procedura byla vytvořena pomocí ukázkových dat společnosti USMF.

1. Na domovské stránce vyberte pracovní prostor **Samoobsluha pro zaměstnance**.
2. Zvolte **Nová kontrola** a vytvořte novou kontrolu.
3. V poli **Typ kontroly** zadejte nebo vyberte hodnotu.
4. V poli **Období výkonnosti** zadejte nebo vyberte hodnotu.
5. Zadejte datum do pole **Koncové datum**.
6. Vyberte **OK**. Recenzi můžete také vytvořit ze šablony. Toto je nejlepší způsob, jak vytvořit recenzi, protože každá část bude obsahovat informace potřebné k zahájení recenze.  
7. Můžete zobrazit nebo skrýt karty, jako je například karta příloh:

    1. V podokně akcí zvolte **Zobrazit oddíly** a otevřete rozbalovací dialogové okno.
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
18. Výběrem možnosti **Přidat měření** otevřete dialogové okno.
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

    - Záložka s náhledem **Podrobnosti hodnocení** umožňuje zaměstnancům hodnotit sebe a manažerům hodnotit zaměstnance. Pokud jsou použity váhy, hodnota váhy skóre se vypočítá automaticky.  
    - V této části povolte nastavení parametrů pro zobrazení hodnocení zaměstnance.  

31. Zvolte kartu **Podpisy**. Používá-li recenze pracovní postup, podpisy se zobrazí pouze po dokončení pracovního postupu. Pokud není použit žádný pracovní postup, pracovník a manažer jsou zde uvedeni. Požadované zaškrtávací políčko je vybráno na základě nastavení typu recenze.  
32. Zvolte kartu **Obecné**.

    - Doba výkonu vytvoří ve výchozím nastavení počáteční a koncové datum. Tato data lze upravovat.  
    - Stavy řídí přístup k přezkoumání. Stav **Nespuštěno** umožňuje všem uživatelům upravit recenzi. Stav **Probíhající** umožňuje zobrazit a upravit recenze pouze zaměstnancům. Připraveno ke kontrole umožňuje zobrazovat a upravovat recenze pouze správcům. Stav konečná kontrola umožňuje zobrazit recenzi zaměstnanci i manažerovi a upravit ji v případě, že je nastavená v typu recenze. Stav **Dokončeno**, **Odmítnuto** a **Zrušeno** nastavují recenzi jen pro čtení.  

33. Zadejte hodnotu do pole **Přehled**.
34. Zvolte kartu **Kontrola**. S tím, jak recenze prochází jednotlivými stavy, zaměstnanec a manažer můžou přidávat komentáře pro každý cíl nebo kompetenci.  
35. Vyberte kartu **Podpisy** . Pracovník a manažer se mohou podepsat při kontrole. Po dokončení všech požadovaných podpisů je stav změněn na hodnotu **Dokončeno** a nelze provést žádné další změny.  

