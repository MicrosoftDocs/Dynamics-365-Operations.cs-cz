---
title: Udržování informací o zraněních a onemocněních zaměstnanců
description: Tento úkol popisuje, jak vytvořit případ zranění nebo nemoci.
author: twheeloc
ms.date: 11/03/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: HRMInjuryIncident, HcmWorkerLookUp, HcmPersonnelManagementWorkspace
audience: Application User
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 36c25626bcc828a2d341d4ce4c9fe8fdcd4e6583
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/04/2022
ms.locfileid: "8688515"
---
# <a name="maintain-employee-injury-and-illness-information"></a>Udržování informací o zraněních a onemocněních zaměstnanců


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Doporučuje se nejprve postupovat podle příručky „Určení zranění a onemocnění“ protože některé se zde uplatňují některé údaje. 



Tento záznam úlohy popisuje základní postup pro vytvoření případu zranění nebo onemocnění. Kromě podrobností o zranění nebo nemoci je sledován stav případu. Ve výchozím nastavení mají případy stav **Otevřeno**. Stav můžete spravovat z položky nabídky **Stav případu** v horní části stránky.

1. Přejděte na **Lidské zdroje \> Pracovníci \> Zranění a onemocnění \> Incidenty zranění nebo onemocnění**.
2. Zvolte **Nové**.
3. Do pole **Popis případu** zadejte hodnotu (například **Zranění zápěstí**).
4. Do pole **Pracovník** zadejte nebo vyberte hodnotu (například **Ana Bowman**).
5. Do pole **Datum a čas incidentu** zadejte datum a čas (například 20. ledna 2016 v 10:00).
6. V poli **Typ zranění nebo onemocnění** zadejte nebo vyberte hodnotu (např. **Zlomenina**).
7. Do pole **Část těla** zadejte nebo vyberte hodnotu (například **Zápěstí**).
8. V poli **Typ výsledku** zadejte nebo vyberte hodnotu (např. **Terapie**).
9. Zadejte datum a čas do pole **Datum a čas nahlášení**.

    Datum a čas nahlášení v poli musí být pozdější než datum a čas incidentu.

10. Zadejte nebo vyberte požadovanou hodnotu (např. **Ana Bowman**) v poli **Osoba, která vykázala případ**.

    Konkrétní osoba může být zaměstnanec nebo jiný svědek incidentu.

11. V sekci **Incident** v poli **Kde k incidentu došlo** zadejte hodnotu (např. **Sklad**).
12. V poli **V pracovních prostorách** vyberte **Ano**, pokud k události došlo na pracovišti.
13. V poli **Datum a čas zahájení práce** zadejte datum a čas, kdy postižená osoba začala pracovat před tím, než k incidentu došlo.
14. V poli **Zaměstnanecká práce nebo úkol** zadejte práci nebo úkol, který pracovník vykonával, když k incidentu došlo (např. **Nakládání krabic**). 
15. V poli **Příčina incidentu** zadejte příčinu incidentu (např. **Uklouzl na mokré podlaze**).
16. Zadejte nebo vyberte hodnotu do pole **Úroveň závažnosti**.
17. V poli **Je třeba podniknout opatření** zadejte hodnotu (např. **Rozlité látky okamžitě ukliďte**).
18. V poli **Očekávané dny mimo práci** zadejte počet dní, po které má být jednotlivec mimo práci.

    Jakmile se osoba vrátí do práce, aktualizujte pole **Počet dnů pracovní neschopnosti** skutečným počtem dnů nepřítomnosti dané osoby.

19. V části **Náklady na zranění nebo onemocnění** vyberte **Přidat**.
20. Do pole **Datum** zadejte datum.
21. V poli **Typ nákladu** zadejte nebo vyberte hodnotu (např. **Terapie**).

    Můžete také zadat částku a připojit podpůrné podklady k nákladům (například faktury nebo lékařské potvrzení).

22. Vyberte **přidat**.
23. Do pole **Datum** zadejte datum.
24. V poli **Typ nákladu** zadejte nebo vyberte hodnotu (např. **Doktor**).
25. V části **Ošetření zranění nebo onemocnění** vyberte **Přidat**.
26. Do pole **Datum ošetření** zadejte datum a čas.
27. V poli **Typ ošetření** zadejte nebo vyberte hodnotu (např. **Dlaha**).
28. Volitelné: Nastavte sekci **Návštěva pohotovosti v nemocnici** na hodnotu **Ano**.
29. V poli **Poznámky k ošetření** zadejte nebo vyberte hodnotu (např. **Dlaha na 2 týdny**).
30. Do pole **Jméno lékaře** zadejte hodnotu (například **Dr. Anderson**).
31. Do pole **Zdravotnícké zařízení a umístění** zadejte hodnotu (např. **Pohotovost Jičín**).
32. Do pole **Podrobnosti o léčbě** zadejte hodnotu (např. **Rentgen potvrzuje zlomeninu, nosit dlahu**).
33. Zvolte možnost **Uložit**.

Stav případu lze kdykoli aktualizovat. Pokud probíhá zpracování zranění nebo onemocnění, nastavte stav na **Probíhá**. Po uzavření incidentu můžete pouze přidat nebo odebrat náklady, léčbu nebo evidenci související s incidentem. Chcete-li změnit další informace, musíte znovu otevřít případ.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
