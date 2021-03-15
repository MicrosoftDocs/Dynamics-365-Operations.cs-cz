---
title: Co je nového nebo upraveného v aplikaci Dynamics 365 Human Resources (16. září 2020)
description: Tohle téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Human Resources k 16. září 2020.
author: jcart1106
manager: tfehr
ms.date: 09/16/2020
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
ms.author: jcart
ms.search.validFrom: 2020-09-16
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 74a87ddb4ed14042dd4e716ad64bc844a800a0a0
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/03/2021
ms.locfileid: "5111841"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-september-16-2020"></a>Co je nového nebo upraveného v aplikaci Dynamics 365 Human Resources (16. září 2020)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Dynamics 365 Human Resources. Změny se vztahují na sestavení číslo 8.1.3557. Čísla v závorkách vedle některých funkcí se vztahují na čísla podpory pro referenci v Lifecycle Services (LCS).

## <a name="included-in-this-release"></a>Zahrnuté do této verze

-  [Uložená zobrazení - obecná dostupnost](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/finance-operations/finance-operations-crossapp-capabilities/saved-views--general-availability)<br>- Další informace naleznete v tématu [Uložená zobrazení](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/saved-views). 

- Formulář **Akce polohy** má aktualizovanou mřížku dimenzí a nové dialogové okno (469495).

- Pokud nastavíte **Omezte přístup k informacím o pracovníkovi** na ano v možnosti **Rozšířený přístup** v **Sdílené parametry lidských zdrojů**, formuláře zaměstnaneckých výhod nyní zobrazují pouze příslušné pracovníky (393384).

- Nové možnosti generování kalendáře v entitě **WorkCalendar** (477055):<br>- Výchozí čas ukončení<br>- Výchozí čas zahájení<br>- Je pátek pracovní den<br>- Je pondělí pracovní den<br>- Je sobota pracovní den<br>- Je neděle pracovní den<br>- Je čtvrtek pracovní den<br>- Je úterý pracovní den<br>- Je středa pracovní den<br>- ID svátku pracovního kalendáře

- Entita **LeaveBankTransactionV1** nyní obsahuje kód příčiny (477823).

- Nyní můžete ukládat záznamy úkolů (492923).

- Data jsou nyní úspěšně publikována z **HCMWorkerContactEntity** (427620).

- Pevná záložka **Kompenzace** se nyní zobrazí pro typ pracovníka dodavatele ve formuláři **Akce pracovníků** (482494).

- Pole **Úroveň** a **Plán** jsou nyní povinná, pokud nastavíte **Pevná kompenzace**. Pokud necháte tato pole nevyplněná (482497), zobrazí se chybová zpráva.

- Pole **Typ plánu** v položce **Zaměstnanecké výhody** je nyní rozevírací seznam (488768).

- Správci systému nyní dostanou oznámení, pokud je vlastní pole odstraněno z Human Resources (481408).

- Během procesu ukončení zaměstnance se Human Resources chová podle očekávání a po zdání uzamčení nezmění vybranou společnost (479877). 

- Manažeři již nemohou přidat sloupec s číslem prostřednictvím personalizace (485317).

- Manažeři již nemohou odstranit filtr datového rozsahu z vypršení platnosti identifikačních čísel (485321).

- Když je pole **Nadřízená pozice** je prázdné, podrobnosti o pozici se stále zobrazují, když umístíte ukazatel myši na pozici (433328).

- Zaměstnanci si nyní mohou zobrazit informace o plánu výhod v samoobslužné službě pro zaměstnance (481676).

- Zaměstnanci nyní mohou zobrazit všechny registrované kurzy (429048).

- Nyní můžete omezit možnosti zobrazení pro stránku **Profesionální certifikáty**. Možnosti zobrazení můžete omezit na aktuální právnickou osobu, podle stavu pracovníka a podle typu pracovníka (451501). 


## <a name="in-preview"></a>Náhled

### <a name="human-resources-app-in-teams"></a>Aplikace Human Resources v Teams

Zaměstnanci mohou prohlížet a požadovat pracovní volno v rámci Microsoft Teams. Mohou interagovat s robotem a vytvářet žádosti o dovolenou. Další informace naleznete zde:

- [Dovolená a nepřítomnost zaměstnanců v Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) v plánu 1. vlny vydání v Dynamics 365 2020
- [Aplikace Human Resources v Teams](https://go.microsoft.com/fwlink/?linkid=2127841) v dokumentaci k Human Resources

### <a name="human-resources-app-in-teams-preview-features"></a>Funkce preview aplikace Human Resources v Teams
 
-  **Oznámení**: Odesílatelé a schvalovatelé žádostí o volno budou upozorněni v aplikaci Human Resources v Teams. Schvalovatelé mohou schválit nebo zamítnout žádosti o volno. Odesílatelé budou upozorněni, pokud byl požadavek schválen nebo zamítnut. Další informace naleznete zde:
   - [Dovolená a nepřítomnost zaměstnanců v Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) v plánu 2. vlny vydání v Dynamics 365 2020
   - [Povolení oznámení pro aplikaci Human Resources v Teams](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-teams-leave-app#enable-notifications-for-the-human-resources-app-in-teams) v dokumentaci k Human Resources
   - [Zapnutí nebo vypnutí oznámení aplikace Teams pro jednotlivé uživatele](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-teams-leave-app#turn-teams-notifications-on-or-off-for-individual-users) v dokumentaci k Human Resources
   - [Oznámení aplikace Teams](https://docs.microsoft.com/dynamics365/human-resources/hr-teams-leave-app#teams-notifications) v dokumentaci k Human Resources
   - [Zobrazení kalendáře pracovního volna vašeho týmu](https://docs.microsoft.com/dynamics365/human-resources/hr-teams-leave-app#view-your-teams-leave-calendar) v dokumentaci k Human Resources
 
- **Kalendář volna manažera**: Manažeři mohou vidět schválené a nevyřízené volno pro jejich přímé podřízené v zobrazení kalendáře. Tohle zobrazení umožňuje snadné pochopení, kdy jsou členové jejich týmu mimo práci. Další informace naleznete zde:
   - [Dovolená a nepřítomnost zaměstnanců v Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) v plánu 2. vlny vydání v Dynamics 365 2020
   - [Zobrazení kalendáře pracovního volna vašeho týmu](https://docs.microsoft.com/dynamics365/human-resources/hr-teams-leave-app#view-your-teams-leave-calendar) v dokumentaci k Human Resources

### <a name="configuration-option-to-position-work-items-assigned-to-me-list-477004"></a>Možnost konfigurace pro umístění seznamu Pracovní položky přiřazené mně (477004)

Nyní je k dispozici nová možnost umístění seznamu **Pracovní položky přiřazené mně** v pravém sloupci řídicího panelu. S touto změnou se všechny pracovní položky a seznamy úkolů zobrazí ve stejné oblasti. Povolte tuto funkci zapnutím funkce **Preview – Vylepšené prostředí pracovního postupu** ve správě funkcí. Další informace o zapnutí funkcí Preview naleznete v tématu [Správa funkcí](hr-admin-manage-features.md).

Tato funkce také podporuje možnosti pracovního postupu, které se zobrazují ve formulářích akcí personálu. Možnosti pracovního postupu se také zobrazují nad pevnou záložkou akce pro rychlý přístup. Další informace naleznete zde: 

- [Vylepšení prostředí pracovního postupu pro správu organizace a personálu](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) v plánu Dynamics 365 2020 2. vlna vydání

![Pracovní položky přiřazené mně](./media/hr-workflow-work-items-assigned-to-me.png)

![Rychlý přístup k položkám pracovního postupu](./media/hr-workflow-quick-access.png)

### <a name="leave-and-absence-calendar"></a>Kalendář pracovního volna a absence

Toto vydání obsahuje další možnosti kalendáře pro kalendáře dovolené a nepřítomnosti. Další informace naleznete v tématu [Zobrazení kalendáře týmu a společnosti](https://docs.microsoft.com/dynamics365/human-resources/hr-employee-self-service-calendar).

## <a name="coming-soon"></a>Již brzy

### <a name="checklist-entities-included-in-dataverse"></a>Položky kontrolního seznamu zahrnuté do Dataverse

Položky kontrolního seznamu pro onboarding, offboarding, převody a obchodní procesy budou v systému Dataverse k dispozici již brzy.

### <a name="benefits-management-reason-codes"></a>Kódy důvodů správy zaměstnaneckých výhod

Kódy důvodů správy zaměstnaneckých výhod budou brzy kombinovány se stávajícími kódy důvodů v aplikaci Human Resources. Pokud jste ve správě zaměstnaneckých výhod vytvořili kódy důvodů, které mají více než 15 znaků, musíte ve správě zaměstnaneckých výhod změnit název kódu důvodu. Formulář **Kódy důvodů** může mít 15 znaků nebo méně. Po aktualizaci názvu se kód důvodu zobrazí pod existujícím formulářem kódu důvodu ve správě personálu. Tato změna bude k dispozici v budoucnu a nebude mít vliv na stávající funkčnost.

## <a name="see-also"></a>Viz také

[Co je nového a co se změnilo v Human Resources](hr-admin-whats-new.md)</br>
[Přehled produktu Dynamics 365 Human Resources vydání 2019 vlny 2](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Aktualizace procesu](hr-admin-setup-update-process.md)</br>
[Správa funkcí](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]