---
title: Co je nového nebo upraveného v aplikaci Dynamics 365 for Talent (10. září 2019)
description: Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 for Talent.
author: Darinkramer
manager: AnnBe
ms.date: 9/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-09-10
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 0aadecd5b37759492f7895ccfda1a777793a08b3
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460560"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-september-10-2019"></a>Co je nového nebo upraveného v aplikaci Dynamics 365 for Talent (10. září 2019)

Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Dynamics 365 for Talent.

## <a name="changes-in-attract"></a>Změny v aplikaci Attract

### <a name="candidate-e-mail-login"></a>Přihlášení kandidáta na e-mail

Kandidáti mohou nyní použít libovolnou e-mailovou adresu k vytvoření účtu a přihlásit se k pracovnímu webu aplikace Talent, aby mohli podávat žádosti o pracovní místa a zjišťovat stav své žádosti. Tato možnost je navíc k již dané schopnosti přihlašovat se na kariérní web aplikace Talent pomocí účtů v sociální síti nebo přihlašovacích údajů organizace.

### <a name="job-activation-and-posting"></a>Aktivace a zveřejnění pracovního místa

Provedli jsme několik změn aktivace a zveřejnění pracovního místa. Pracovní místa je třeba aktivovat před zveřejněním na kariérním webu aplikace Talent nebo externích vývěskách s pracovními místy, včetně LinkedIn nebo Broadbean.

## <a name="changes-in-onboard"></a>Změny v aplikaci Onboard

Tato verze obsahuje dílčí opravy chyb pro aplikaci Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Změny v Core HR

Změny popsané v této části se vztahují na číslo sestavení 8.1.2482. Čísla v závorkách v některých záhlavích se vztahují na čísla podpory v Microsoft Dynamics Lifecycle Services (LCS).

### <a name="you-can-enable-preview-features-in-sandbox-and-trial-environments"></a>Můžete povolit funkce náhledu v izolovaném prostoru a zkušebních prostředích.

Když zřizujete novou instanci aplikace Talent, můžete určit, zda je typem instance Produkce nebo Sandbox. Instance typu Sandbox umožňují dřívější testování nových funkcí. Chcete-li, aby byla jedna z existujících instancí aktualizována na typ instance Sandbox, obraťte se na podporu a inicializujte požadavek na změnu.

Další informace o tom, jak jsou publikovány změny, naleznete v části [Zřízení aplikace Talent](./provisioning-talent.md).

### <a name="platform-update-29"></a>Aktualizace platformy 29

Další podrobnosti o aktualizaci Platform Update 29 naleznete v tématu [Funkce Preview v aktualizaci Platform Update 29 aplikace Dynamics 365 for Finance and Operations (říjen 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-29).

### <a name="new-job-base-entity-available-in-data-management-framework-347202"></a>Nová základní entita Pracovní místo dostupná v architektuře pro správu dat (347202)

V této verzi aplikace je k dispozici nová entita Základní pracovní místo pro import a export dat. 

### <a name="worker-advanced-security-policy-incorrectly-displays-positions-in-position-hierarchy-354868"></a>Zásada pokročilého zabezpečení pracovníka nesprávně zobrazí pozice v hierarchii pozic (354868).

Při tomto vydání se již nebudou zobrazovat otevřené pozice s "prázdným" pracovníkem v případě, že uživatelé mají omezený přístup.

### <a name="job-form-close-box-wont-close-form-in-certain-situations-342467"></a>Pole zavření formuláře pracovního místa nezavře formulář v určitých situacích (342467).

Tato verze obsahuje změnu, která umožňuje ukončit formulář pracovního místa ve všech scénářích.

### <a name="new-case-on-employee-record-is-locked-for-human-resources-manager-role-337111"></a>Nový případ v záznamu zaměstnance je uzamčen pro roli manažera lidských zdrojů (337111).

Tato změna znamená, že formulář správy případu již není při přístupu z formuláře zaměstnance uzamčen.

### <a name="employment-end-date-always-defaults-to-235959-351492"></a>Koncové datum zaměstnání je vždy výchozí na 23:59:59 (351492)

Tato změna umožňuje změnit datum zaměstnání na jinou dobu než 23:59:59 při ručním ukončení zaměstnání.

### <a name="unable-to-set-up-expiration-date-on-an-earning-code-through-data-management-336604"></a>Nelze nastavit datum vypršení platnosti v kódu pro získávání prostřednictvím správy dat (336604)

V této verzi můžete nastavit kódy zisků, jejichž platnost vyprší prostřednictvím entity **PayrollWorkerPositionEarningCodeEntity**.

### <a name="employee-development-analytic-report-doesnt-display-data-348737"></a>Analytická sestava pro rozvoj zaměstnanců nezobrazuje data (348737).

V tomto týdnu byla aktualizována analýza dovedností zaměstnanců, aby poskytovala přesné vykazování.

### <a name="terms-of-employment-datetime-dont-default-to-beginning-of-day-349101"></a>Doba data a času zaměstnání, ne výchozí zahájení dne (349101)

Tato změna má počáteční datum a čas nastaveny na výchozí hodnotu začátku dne a koncové datum/čas jsou nastaveny jako výchozí na konci dne.

### <a name="changing-the-employment-end-date-on-worker-action-form-displays-an-error-354092"></a>Změna koncového data zaměstnání ve formuláři akce pracovníka zobrazí chybu (354092). 

Tato změna opravuje problém při změně koncového data zaměstnání jako součásti akce pracovníka.

### <a name="applying-onboarding-checklists-across-companies-338433"></a>Použití kontrolních seznamů při zprovoznění mezi společnostmi (338433)

Tato verze nyní poskytuje možnost použít kontrolní seznamy pro zaměstnance, kteří jsou zaměstnáni v jiných právnických osobách, než je podepsaná právnická osoba.

## <a name="in-preview"></a>Náhled

### <a name="streamlined-employee-entry-and-navigation"></a>Zjednodušené zadávání zaměstnance a navigace

Tato funkce je nyní k dispozici v prostředích izolovaného prostoru. Chcete-li tuto funkci zapnout, přejděte na **Správa systému > Odkazy > Nastavení > Systémové parametry > Funkce náhledu**. Vyberte **Rozšířený formulář pracovníka a navigace**. To povolí tyto změny pro všechny uživatele. Tuto možnost můžete kdykoli vypnout.

Další informace naleznete v tématu [Zjednodušené zadání zaměstnance a navigace](./streamlined-employee-entry.md).
