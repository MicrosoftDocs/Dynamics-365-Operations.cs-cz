---
title: Co je nového nebo upraveného v aplikaci Dynamics 365 Human Resources (03. září 2020)
description: Tohle téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Human Resources k 3. září 2020.
author: andreabichsel
ms.date: 09/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-09-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6d7c3e3070d6c3b8dad7b3ae4d50e928d0060d5892d606cd78bc701c2e7985cb
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6759688"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-september-3-2020"></a>Co je nového nebo upraveného v aplikaci Dynamics 365 Human Resources (3. září 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Dynamics 365 Human Resources. Změny se vztahují na sestavení číslo 8.1.3504. Čísla v závorkách v některých záhlavích se vztahují na čísla podpory pro referenci v Lifecycle Services (LCS).

Další informace o připravovaných funkcích v aplikaci Human Resources najdete v tématu [Přehled o 2. vlně vydání Dynamics 365 Human Resources v roce 2019](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/). Další informace o procesu aktualizaci aplikace Human Resource najdete v tématu [Proces aktualizace](hr-admin-setup-update-process.md).

## <a name="in-this-release"></a>V této vydané verzi

### <a name="new-default-financial-dimensions-grid-and-dialog-pattern-throughout-human-resources-469495"></a>Nová výchozí mřížka finančních dimenzí a vzor dialogu v aplikaci Human Resources (469495)

Nový vzor pro finanční dimenze je nyní k dispozici v následujících oblastech:

- Akce pozice (formulář: **HcmPositionActionDetail**)
- Kódy příjmů mzdy (formulář: **PayrollEarningCode**)

### <a name="entries-dont-appear-in-company-leave-calendar-if-leave-and-absence-calendar-enhancements-arent-enabled-484406"></a>Pokud nejsou povolena vylepšení firemního kalendáře pracovního volna a absencí, ve firemním kalendáři pracovního volna se nezobrazují (484406)

Tato vydaná verze opravuje problém, kdy se ve firemním kalendáři pracovního volna nezobrazují položky pracovního volna. K tomuto problému dochází pouze při deaktivaci možnosti správy funkcí **Vylepšení kalendáře pracovního volna a absencí**.

### <a name="benefitplanemployeeentity-issue-467597"></a>Problém s BenefitPlanEmployeeEntity (467597)

Tato vydaná verze opravuje problém s entitou **BenefitsPlanEmployee**. Při importu registrací pracovníků jsou **Kód pokrytí** a **Kód typu plánu** nyní nastaveny správně. Tento problém způsoboval, že se plány zaměstnaneckých výhod ve formulářích **Plán zaměstnaneckých výhod** a **Otevřená registrace** v samoobsluze zaměstnanců nezobrazují správně.

### <a name="electronic-file-1094-c-output-missing-letter-in-xml-435190"></a>U výstupu elektronického souboru 1094-C chybí písmeno v XML (435190)

Tato změna opravuje problém, kdy ve výstupním souboru 1094-C chybí znak potřebný při odesílání do IRS.

### <a name="employee-variable-compensation-table-mapped-to-fixed-compensation-form-476117"></a>Tabulka variabilní kompenzace zaměstnance mapovaná na formulář fixní kompenzace (476117)

Tato změna zarovná pole fixní kompenzace s formulářem fixní kompenzace. Pole variabilní kompenzace jsou nyní k dispozici pouze ve formuláři variabilní kompenzace.

### <a name="leave-requests-allowed-before-enrollment-if-that-leave-type-has-a-negative-minimum-balance-469917"></a>Pokud má tento typ pracovního volna záporný minimální zůstatek, jsou povoleny žádosti o pracovní volno před zápisem (469917)

Tato změna zakazuje zadávání žádostí o pracovní volno před zápisem plánu, i když má zápis záporný minimální zůstatek. Žádosti můžete zadávat nebo odesílat, pouze když je plán aktivní.

### <a name="document-templates-dont-download-457279"></a>Šablony dokumentů se nestahují (457279)

Díky této změně si nyní můžete stáhnout všechny šablony dokumentů. 

### <a name="data-displays-as-column-headers-instead-of-rows-for-the-pay-rate-field-in-the-compensation-plan-report-476077"></a>Data se zobrazují jako záhlaví sloupců místo řádků pro pole Mzdová sazba v sestavě plánu kompenzace (476077)

Sestava analýzy nyní zobrazuje správné informace pro **Mzdovou sazbu**.

## <a name="in-preview"></a>Náhled

### <a name="human-resources-application-in-teams"></a>Aplikace Human Resources v Teams

Zaměstnanci mohou prohlížet a požadovat pracovní volno v rámci Microsoft Teams. Mohou interagovat s robotem a vytvářet žádosti o dovolenou. Další informace naleznete zde:

- [Dovolená a nepřítomnost zaměstnanců v Microsoft Teams](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) v plánu 1. vlny vydání v Dynamics 365 2020
- [Aplikace Human Resources v Teams](./hr-admin-teams-leave-app.md) v dokumentaci k Human Resources

### <a name="human-resources-app-in-teams-preview-features"></a>Funkce preview aplikace Human Resources v Teams
 
-  **Oznámení**: Odesílatelé a schvalovatelé žádostí o volno budou upozorněni v aplikaci Human Resources v Teams. Schvalovatelé budou moci schválit nebo zamítnout žádosti o volno. Odesílatelé budou upozorněni, pokud byl požadavek schválen nebo zamítnut. Další informace naleznete zde:
   - [Dovolená a nepřítomnost zaměstnanců v Microsoft Teams](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) v plánu 2. vlny vydání v Dynamics 365 2020
   - [Povolení oznámení pro aplikaci Human Resources v Teams](./hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams) v dokumentaci k Human Resources
   - [Zapnutí nebo vypnutí oznámení aplikace Teams pro jednotlivé uživatele](./hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users) v dokumentaci k Human Resources
   - [Oznámení aplikace Teams](./hr-teams-leave-app.md#respond-to-teams-notifications) v dokumentaci k Human Resources
   - [Zobrazení kalendáře pracovního volna vašeho týmu](./hr-teams-leave-app.md#view-your-teams-leave-calendar) v dokumentaci k Human Resources
 
- **Kalendář volna manažera**: Manažeři budou moci vidět schválené a nevyřízené volno pro jejich přímé podřízené v zobrazení kalendáře. Tohle zobrazení umožňuje snadné pochopení, kdy jsou členové jejich týmu mimo práci. Další informace naleznete zde:
   - [Dovolená a nepřítomnost zaměstnanců v Microsoft Teams](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) v plánu 2. vlny vydání v Dynamics 365 2020
   - [Zobrazení kalendáře pracovního volna vašeho týmu](./hr-teams-leave-app.md#view-your-teams-leave-calendar) v dokumentaci k Human Resources

### <a name="configuration-option-to-position-work-items-assigned-to-me-list-477004"></a>Možnost konfigurace pro umístění seznamu Pracovní položky přiřazené mně (477004)

Nyní je k dispozici nová možnost umístění seznamu **Pracovní položky přiřazené mně** v pravém sloupci řídicího panelu. S touto změnou se všechny pracovní položky a seznamy úkolů zobrazí ve stejné oblasti. Povolte tuto funkci zapnutím funkce **Preview – Vylepšené prostředí pracovního postupu** ve správě funkcí. Další informace o zapnutí funkcí Preview naleznete v tématu [Správa funkcí](hr-admin-manage-features.md).

Tato funkce také podporuje možnosti pracovního postupu, které se zobrazují ve formulářích akcí personálu. Možnosti pracovního postupu se také zobrazují nad pevnou záložkou akce pro rychlý přístup. Další informace naleznete zde: 

- [Vylepšení prostředí pracovního postupu pro správu organizace a personálu](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) v plánu Dynamics 365 2020 2. vlna vydání

![Pracovní položky přiřazené mně.](./media/hr-workflow-work-items-assigned-to-me.png)

![Rychlý přístup k položkám pracovního postupu.](./media/hr-workflow-quick-access.png)

## <a name="coming-soon"></a>Již brzy

### <a name="checklist-entities-included-in-dataverse"></a>Položky kontrolního seznamu zahrnuté do Dataverse

Položky kontrolního seznamu pro onboarding, offboarding, převody a obchodní procesy budou v systému Dataverse k dispozici již brzy.

### <a name="benefits-management-reason-codes"></a>Kódy důvodů správy zaměstnaneckých výhod

Kódy důvodů správy zaměstnaneckých výhod budou brzy kombinovány se stávajícími kódy důvodů v aplikaci Human Resources. Pokud jste ve správě zaměstnaneckých výhod vytvořili kódy důvodů, které mají více než 15 znaků, musíte ve správě zaměstnaneckých výhod změnit název kódu důvodu. Formulář **Kódy důvodů** může mít 15 znaků nebo méně. Po aktualizaci názvu se kód důvodu zobrazí pod existujícím formulářem kódu důvodu ve správě personálu. Tato změna bude k dispozici v budoucnu a nebude mít vliv na stávající funkčnost.

## <a name="see-also"></a>Viz také

[Co je nového a co se změnilo v Human Resources](hr-admin-whats-new.md)</br>
[Přehled produktu Dynamics 365 Human Resources vydání 2019 vlny 2](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Aktualizace procesu](hr-admin-setup-update-process.md)</br>
[Správa funkcí](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
