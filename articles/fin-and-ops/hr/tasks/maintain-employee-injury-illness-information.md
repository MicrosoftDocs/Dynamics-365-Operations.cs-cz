---
title: Udržování informací o zraněních a onemocněních zaměstnanců
description: Doporučuje se nejprve postupovat podle příručky „Určení zranění a onemocnění“ protože některé se zde uplatňují některé údaje.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRMInjuryIncident, HcmWorkerLookUp
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7324a1ce08bfe07a7ef96f4a733ebd44cd392ba6
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/07/2019
ms.locfileid: "1510398"
---
# <a name="maintain-employee-injury-and-illness-information"></a>Udržování informací o zraněních a onemocněních zaměstnanců

[!include [task guide banner](../../includes/task-guide-banner.md)]

Doporučuje se nejprve postupovat podle příručky „Určení zranění a onemocnění“ protože některé se zde uplatňují některé údaje. 



Tento záznam úlohy popisuje základní postup pro vytvoření případu zranění nebo onemocnění. Kromě sledování podrobností o zranění nebo onemocnění, je také sledovaný stav případu.  Výchozí nastavení případu se stavem „Otevřeno“.  Stav lze spravovat z položky nabídky „Stav případu“ v pruhu aplikace v horní části formuláře.

1. Přejděte na Lidské zdroje > Pracovníci > Zranění a onemocnění > Incidenty zranění nebo onemocnění.
2. Klikněte na položku Nová.
3. Zadejte hodnotu do pole Popis případu.
    * Příklad: Zranění zápěstí  
4. V poli Pracovník zadejte nebo vyberte hodnotu.
    * Příklad: Ahmed Barnett  
5. Zadejte datum a čas do pole Datum a čas incidentu.
    * Příklad: 20. 1. 2016 10:00:00  
6. V poli Typ zranění nebo onemocnění zadejte nebo vyberte hodnotu.
    * Příklad: Zlomenina  
7. V poli Část těla zadejte nebo vyberte hodnotu.
    * Příklad: Zápěstí  
8. V poli Typ výsledku zadejte nebo vyberte hodnotu.
    * Příklad: Léčba  
9. Zadejte datum a čas do pole Datum a čas nahlášení.
    * Datum a čas ohlášené v poli musí být pozdější než datum a čas incidentu.  
10. Zadejte nebo vyberte požadovanou hodnotu u osoby, která vykázala případ.
    * To může být zaměstnanec nebo na jiný důkaz k incidentu.  Příklad: Ahmed Barnett  
11. Rozbalte sekci Incident.
12. Zadejte hodnotu do pole Kde k incidentu došlo.
    * Příklad: Sklad  
13. Vyberte možnost Ano v poli V pracovních prostorách.
    * Pokud incident vznikl v pracovních prostorách, vyberte ano.  
14. Zadejte datum a čas do pole Datum a čas zahájení práce.
    * Zadejte datum a čas, kdy ovlivněný jednotlivec začal pracovat před výskytem incidentu.  
15. Zadejte hodnotu do pole Práce nebo úkol zaměstnance.
    * Zadejte úlohu nebo úkol, který pracovník vykonával při vzniku incidentu.  Příklad: Nakládání krabic  
16. Zadejte hodnotu do pole Příčina incidentu.
    * Zadejte příčinu nebo incident.  Příklad: Uklouznutí na vlhké podlaze  
17. Zadejte nebo vyberte hodnotu do pole Úroveň závažnosti.
18. Zadejte hodnotu do pole Provést akci.
    * Příklad: Rychlé rozlití při úklidu  
19. Zadejte číslo do pole Očekávané dny v pracovní neschopnosti.
    * Zadejte počet dní, po které se očekává, že daná osoba bude v pracovní neschopnosti.  Jakmile se osoba vrátí do práce, aktualizujte pole „Počet dnů pracovní neschopnosti“ skutečným počtem dnů nepřítomnosti.  
20. Rozbalte část Náklady na zranění nebo onemocnění.
21. Klepněte na možnost Přidat.
22. Do pole Datum zadejte datum.
23. V poli Typ nákladů zadejte nebo vyberte hodnotu.
    * Příklad:  Léčení   Můžete také zadat částku a připojit podklady, jako jsou například faktury nebo lékařské potvrzení o nákladech.  
24. Klepněte na možnost Přidat.
25. Do pole Datum zadejte datum.
26. V poli Typ nákladů zadejte nebo vyberte hodnotu.
    * Příklad: Lékař  
27. Rozbalte část Ošetření zranění nebo onemocnění.
28. Klepněte na možnost Přidat.
29. Do pole Datum ošetření zadejte datum a čas.
30. V poli Typ ošetření zadejte nebo vyberte hodnotu.
    * Příklad: Dlaha  
31. Volitelně nastavte v části Návštěva pohotovosti v nemocnici hodnotu Ano.
32. Zadejte hodnotu do pole Poznámky k ošetření.
    * Příklad: Dlaha po dobu 2 týdnů  
33. Do pole Jméno lékaře zadejte hodnotu.
    * Příklad: Dr. Anderson  
34. Zadejte hodnotu do pole Léčebné zařízení a umístění.
    * Příklad: Pohotovost Elm St.   
35. Zadejte hodnotu do pole Podrobnosti o ošetření.
    * Příklad: Rentgenem potvrzená zlomenina, aplikována dlaha  
36. Klikněte na položku Uložit.
    * Stav případu lze kdykoli aktualizovat.  Nastavte případ na stav Probíhá, pokud probíhá zpracování zranění nebo onemocnění.  Jakmile uzavřete incident, můžete pouze přidat nebo odebrat náklady, léčbu nebo evidenci související s incidentem.  Chcete-li upravit informace, případ znovu otevřete.  

