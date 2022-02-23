---
title: Co je nového nebo změněného v aplikaci Dynamics 365 Human Resources (14. května 2020)
description: Tohle téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Human Resources k 14. květnu 2020.
author: Darinkramer
manager: AnnBe
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-05-14
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 76ca497cc7fabf737c8a0ee71363f22fd4201ea8
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528490"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-14-2020"></a>Co je nového nebo změněného v aplikaci Dynamics 365 Human Resources (14. května 2020)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Dynamics 365 Human Resources. Změny se vztahují na sestavení číslo 8.1.3244. Čísla v závorkách v některých záhlavích se vztahují na čísla podpory pro referenci v Lifecycle Services (LCS).

## <a name="platform-changes"></a>Změny platformy

Změny platformy jsou součástí vydání tohoto týdne. Další informace naleznete v části [Aktualizace platformy pro verze 10.0.10 aplikací Finance and Operations (květen 2020)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-update-34). Tato verze obsahuje opravy chyb a změny uložených zobrazení.
 
## <a name="ensure-common-data-service-picklists-are-consistent-with-leave-enums-436343"></a>Zajistěte, že rozevírací seznamy Common Data Service jsou shodné s výčty volna (436343)

Rozevírací seznamy Common Data Service jsou nyní shodné s výčty volna.

## <a name="allow-users-to-configure-leave-request-workflow-based-on-the-request-amount-300044"></a>Umožněte uživatelům konfigurovat pracovní postup žádosti o volno na základě požadované délky (300044)

Uživatelé mohou nakonfigurovat pracovní postupy žádosti o volno na základě požadovaných délek.
 
## <a name="new-worker-form-exposes-data-through-the-view-menu-when-advanced-security-is-enabled-403185"></a>Nový formulář pracovníka vystaví data prostřednictvím nabídky Zobrazit, pokud je povoleno rozšířené zabezpečení (403185)

Toto vydání opravuje, jak funguje zobrazení pracovníků napříč právnickými osobami, když je povolen pokročilý přístup a pracovníci v jiných společnostech jsou přístupní.

## <a name="allow-running-leave-accruals-for-a-single-plan-or-a-single-company-318844"></a>Povolení spuštění časového rozlišení volna pro jeden plán nebo pro jednu společnost (318844)

S touto změnou můžete spouštět časová rozlišení pro společnost nebo plán.
 
## <a name="show-the-positions-full-time-equivalent-fte-in-the-enrolled-workers-form-414658"></a>Zobrazení ekvivalentu plného úvazku ve formuláři registrovaných pracovníků (414658)

Hodnota ekvivalentu plného úvazku z pozice pracovníka určuje míru časového rozlišení pracovníka, když je na typu volna povolena možnost ekvivalentu plného úvazku. Toto pole je nyní zahrnuto ve formuláři **Registrovaní pracovníci** a v dialogovém okně **Hromadná registrace**.

## <a name="add-leave-balance-expiration-batch-job-431266"></a>Přidat dávkovou úlohu vypršení platnosti zůstatku volna (431266)

Nyní je k dispozici nová dávková úloha, která se spouští denně. Snižuje zbývající zůstatek volna, když nastanou data vypršení platnosti.

## <a name="exporting-personal-contacts-for-an-employee-using-the-worker-personal-contact-person-entity-doesnt-export-personal-contacts-with-the-parent-relationship-type-345893"></a>Export osobních kontaktů zaměstnance pomocí entity kontaktní osoby pracovníka neexportuje osobní kontakty s typem nadřazeného vztahu (345893)

Datová entita **Kontaktní osoba pracovníka** (**HcmPersonalContactPersonEntity** v DMF a **PersonalContactPerson** v OData) nemohla exportovat osobní kontakty, které mají typ vztahu **Nadřazený**. Tento problém je opraven u osobních kontaktů vytvořených po této změně. Existující osobní kontakty typu **Nadřazený** budou opraveny v pozdějším vydání.

## <a name="reason-codes-display-across-different-scenarios-when-theyre-marked-as-leave-and-absence-and-the-streamlined-employee-form-is-enabled-434163"></a>Kódy důvodů se zobrazují v různých scénářích, když jsou označeny jako Pracovní volno a absence a je aktivován zjednodušený formulář zaměstnance (434163)

Tato změna omezuje kódy důvodů pouze na kódy pracovního volna a absence, pokud povolíte zjednodušené zadávání zaměstnanců.

## <a name="the-preview-feature-assign-a-leave-plan-to-employees-in-the-future-displays-error-433555"></a>Funkce Preview s názvem Přiřadit zaměstnancům plán volna v budoucnu zobrazí chybu (433555)

Tato změna opravuje chybu, pokud má plán pracovního volna přiřazené dva typy pracovního volna a pokusíte se o přiřazení zaměstnance.

## <a name="getting-started-banner-appears-for-all-users-441731"></a>Pro všechny uživatele se zobrazí banner Začínáme (441731)

Při této změně je banner Začínáme skryt pro uživatele, kteří nejsou správci systému nebo správci dat. 

## <a name="the-common-data-service-worker-address-entity-works-differently-in-terms-of-date-time-effective-dates-in-human-resources-425071"></a>Entita adresy pracovníka v Common Data Service pracuje odlišně, pokud jde o data účinnosti data v Human Resources (425071)

Tato změna udržuje informace o adrese v souladu v určitých scénářích na základě údajů adresy.

## <a name="unable-to-add-an-attachment-to-an-approved-leave-request-425407"></a>Nelze přidat přílohu ke schválené žádosti o pracovní volno (425407)

Díky vydání tohoto týdne můžete přidávat přílohy ke schváleným žádostem o pracovní volno, aniž byste museli žádost o pracovní volno měnit.

## <a name="in-preview"></a>Náhled

## <a name="leave-suspension"></a>Pozastavit pracovní volno

Můžete přerušit pracovní volno a absenci v Human Resources pro zaměstnance. Pozastavením volna se zastaví časové rozlišení volna pro vybrané typy pracovního volna. Pokud k přerušení dojde po zpracování časového rozlišení, pozastavením volna se vytvoří průběžná Úprava zůstatku zaměstnance. Další informace naleznete v části [Přerušení pracovního volna](hr-leave-and-absence-suspend-leave.md).

## <a name="update-user-experience-to-indicate-that-accrual-is-suspended-429550"></a>Aktualizujte uživatelské prostředí, abyste naznačili, že akruální účet je pozastaven (429550)

Uživatelská zkušenost nyní naznačuje, že přírůstek byl pro plán pozastaven.

## <a name="suspend-leave-accrual-for-specified-leave-types-272447"></a>Pozastavení časového limitu pro vybrané typy dovolené (272447)

V této verzi může HR vytvořit pravidlo pro pozastavení přírůstků dovolené pro zaměstnance s požadavky na dovolenou zadanými pro neplacenou dovolenou. Neplacená dovolená může být zadána, ale nemusí. Dovolenou můžete pozastavit na základě jiného typu dovolené.

## <a name="dmf-entity-available-for-accrual-suspensions-429549"></a>Entita DMF je k dispozici pro akruální pozastavení (429549)

Entita DMF je nyní k dispozici pro akruální pozastavení

## <a name="add-reason-code-to-accrual-suspensions-429547"></a>Přidejte kód příčiny pro akruální pozastavení (429547)

K akruálnímu pozastavení byly přidány kódy důvodů.

## <a name="begin-transitioning-from-human-resources-parameters-to-leave-and-absence-parameters"></a>Začněte přechod z parametrů lidských zdrojů na parametry dovolené a nepřítomnosti

Tato verze začíná kombinovat parametry lidských zdrojů s parametry dovolené a nepřítomnosti.

## <a name="carry-forward-rules"></a>Pravidla pro převod do dalšího období

Můžete určit typ převodu pracovního volna do dalšího období pro převod zůstatků, kde byly převedeny úpravy převodu do dalšího období. Pokud například zaměstnanec přenese deset dní dopředu, můžete pro tyto 10 dny vybrat jiný typ pracovního volna. Další informace naleznete v tématu [Konfigurace typů pracovního volna a absence](hr-leave-and-absence-types.md).

## <a name="see-also"></a>Viz také

[Co je nového a co se změnilo v Human Resources](hr-admin-whats-new.md)</br>
[Přehled produktu Dynamics 365 Human Resources vydání 2019 vlny 2](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Aktualizace procesu](hr-admin-setup-update-process.md)</br>
[Správa funkcí](hr-admin-manage-features.md)