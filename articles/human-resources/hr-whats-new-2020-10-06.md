---
title: Co je nového nebo upraveného v aplikaci Dynamics 365 Human Resources (6. října 2020)
description: Tohle téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Human Resources k 6. říjnu 2020.
author: jcart1106
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2020-10-06
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 090533a4391488f4ec0929dd4866e55a478ee6e639563ad37a6819592e91b23c
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6739196"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-october-6-2020"></a>Co je nového nebo upraveného v aplikaci Dynamics 365 Human Resources (6. října 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Tohle téma popisuje funkce, které jsou nové, byly změněny nebo se brzy objeví v aplikaci Dynamics 365 Human Resources. Další informace o našem procesu aktualizaci a plánu najdete v tématu [Proces aktualizace](hr-admin-setup-update-process.md).

Další informace o nových funkcích a jejich očekávaných obecných datech dostupnosti najdete v tématu [Přehled 2. vlny vydání Dynamics 365 Human Resources v roce 2020](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>V této vydané verzi

Tato verze obsahuje následující nové funkce a opravené chyby. Změny se vztahují na sestavení číslo 8.1.3636.

### <a name="new-features"></a>Nové funkce

V této verzi je všeobecně dostupná následující funkce.

| Funkce | Plán vydání | Dokumentace |
| --- | --- | --- |
| Další informace o kalendářích pracovního volna | [Získejte další informace v zobrazeních kalendářů pracovního volna](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/provide-additional-insight-leave-calendar-views) | [Zobrazení kalendáře týmu a společnosti](hr-employee-self-service-calendar.md) |

### <a name="bug-fixes"></a>Opravy chyb

Tato verze obsahuje následující opravy chyb.

>[!NOTE]
> Naším cílem je k vám dostat tyto informace co nejdříve. Mohou existovat aktualizace tohoto tématu zahrnující opravy chyb, které se dostaly do sestavení poté, co bylo toto téma původně publikováno.

| Číslo problému | Výdej | popis |
| --- | --- | --- |
| 448806 | **Výchozí typ identifikace** je exportován jako **RecID** v parametrech HCM | Tato změna entity parametrů lidských zdrojů přidá další sloupec, který zobrazí **Výchozí typ identifikace**. |
| 492923 | Záznamy úkolů se neukládají ve službě Lifecycle Services (LCS) | Záznamy úkolů lze nyní uložit v LCS. |
| 429950 | Opravená kompenzace nevyprší správně při změně pozice | Při změně pozice pracovníka na stránce **Převod pracovníka** bylo koncové datum kompenzace stanoveno jeden den před koncem pozice. Koncové datum kompenzace je nyní stejné jako koncové datum pozice. |
| 467214 | **Analýza stálého platu** se zobrazí, pouze pokud je **Název převodu mzdové sazby** nastaven na **Roční** | Analýza stálého platu s jiným názvem než **Roční** se v nezobrazila v analýze kompenzace. S touto aktualizací nyní analýza kompenzace používá všechny převody mzdových sazeb. Při spouštění sestavy podle parametru **Hodinově** nebo **Mzda** je jakákoli konverze mzdových sazeb, která používá jiné než hodinové období, zahrnuta ve filtru **Mzda**. Pouze mzdové sazby s obdobím typu **Hodinově** jsou zahrnuty ve filtru **Hodinově**. |
| 482464 | Při zobrazení **recenzí** se zobrazení **Podrobnosti** po použití filtru nezmění na zobrazení mřížky | Po použití filtru se mřížka recenzí zobrazí podle očekávání. |
| 483184 | Aplikace Human Resources nevytváří časové rozlišení pracovního volna, když vyberete **Základní úroveň** jako **Upravené počáteční datum** v záznamu **Opustit registraci** |**Upravené počáteční datum** je naplněno a použito při generování časového rozlišení pracovního volna.  |
| 509731 | Žádost o volno pro pracovníka s budoucím ukončením pracovního poměru způsobuje problém, pokud požádá o volno po datu ukončení | Žádosti o volno lze nyní odeslat zaměstnancům s budoucím datem ukončení pracovního poměru, pokud je požadavek před datem ukončení. |
| 510716 | Analýza kompenzace zahrnuje mužské i ženské zaměstnance pro **Průměrná hodinová mzda mužů** | V analýze kompenzace zahrnovala **Průměrná hodinová mzda mužů** v **Demografické analýze kompenzace** zahrnovala průměrný plat žen. Nyní zahrnuje pouze muže. |
| 511348 | Samoobsluha zaměstnaneckých výhod by měla zobrazovat pouze plány výhod platné od dnešního dne do konce období zaměstnaneckých výhod | Plány zaměstnaneckých výhod s vypršenou platností byly zobrazeny zaměstnancům na stránce **Registrace zaměstnaneckých výhod**. Tato oprava tyto plány odstraní. |
| 512706 | Nastavte následující pole pouze pro čtení:<ul><li>BenefitPlanEmployeeEntity</li><li>EnrollmentConfirmed</li><li>EnrollmentConfirmedBy</li><li>EnrollmentConfirmedDateTime | Tlačítka **Přidat** a **Odebrat** pro podrobnosti dimenzí byla po dokončení akce nesprávně povolena. Tato aktualizace stránky **Podrobnosti akce pozice** změní pole na neupravitelná po dokončení dané akce. |

## <a name="in-preview"></a>Náhled

Verze Preview obsahuje následující nové funkce. Další informace o zapnutí a vypnutí funkcí naleznete v tématu [Správa funkcí](hr-admin-manage-features.md).

| Funkce | Plán vydání | Dokumentace |
| --- | --- | --- |
| Aplikace Human Resources v Microsoft Teams | [Dovolená a nepřítomnost zaměstnanců v Microsoft Teams](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [Aplikace Human Resources v Teams](./hr-admin-teams-leave-app.md)<br>[Správa žádostí o dovolenou v aplikaci Teams](hr-teams-leave-app.md) |
| Vylepšené požadavky a schválení pracovního toku | [Vylepšení prostředí pracovního postupu pro správu organizace a personálu](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) | [Možnost konfigurace pro umístění seznamu Pracovní položky přiřazené mně](./hr-whats-new-2020-09-03.md#configuration-option-to-position-work-items-assigned-to-me-list-477004) |
| Virtuální entity v Dataverse pro Human Resources | [Rozšíření základních dat Dynamics 365 Human Resources v Dataverse](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/expand-dynamics-365-human-resources-core-data-common-data-service) | [Konfigurace virtuálních entit Dataverse](hr-admin-integration-common-data-service-virtual-entities.md) |

## <a name="coming-soon"></a>Již brzy

Následující nové funkce jsou naplánovány do budoucích vydání:

- **Entity kontrolního seznamu zahrnuté v Dataverse**: Položky kontrolního seznamu pro zprovoznění, zrušení zprovoznění, převody a obchodní procesy budou v Dataverse k dispozici již brzy.

- **Kódy důvodů správy zaměstnaneckých výhod**: Kódy důvodů správy zaměstnaneckých výhod budou brzy kombinovány se stávajícími kódy důvodů v aplikaci Human Resources. Pokud jste ve správě zaměstnaneckých výhod vytvořili kódy důvodů, které mají více než 15 znaků, musíte ve správě zaměstnaneckých výhod změnit název kódu důvodu. Formulář **Kódy důvodů** může mít 15 znaků nebo méně. Po aktualizaci názvu se kód důvodu zobrazí pod existujícím formulářem kódu důvodu ve správě personálu. Tato změna bude k dispozici v budoucnu a nebude mít vliv na stávající funkčnost.

- **Vlastní odkazy v samoobsluze pro manažery**: Abychom podpořili manažery, rozšiřujeme možnosti samoobsluhy pro manažery. Přidáváme možnost přidat vlastní odkazy na kartě **Můj tým**. Tato funkce je podobná funkci vlastních odkazů na kartě **Moje informace** v samoobsluze pro zaměstnance. Další informace naleznete v tématu [Vlastní odkazy v samoobsluze pro manažery](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/custom-links-manager-self-service).

Úplný seznam plánovaných funkcí a plánovaných verzí najdete v části [Přehled o 2. vlně vydání Dynamics 365 Human Resources v roce 2019](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/).

## <a name="additional-resources"></a>Další prostředky

[Co je nového a co se změnilo v Human Resources](hr-admin-whats-new.md)</br>
[Přehled produktu Dynamics 365 Human Resources vydání 2020 vlny 2](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/)</br>
[Aktualizace procesu](hr-admin-setup-update-process.md)</br>
[Správa funkcí](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]