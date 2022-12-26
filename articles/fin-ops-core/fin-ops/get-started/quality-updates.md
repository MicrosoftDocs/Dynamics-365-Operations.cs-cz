---
title: Proaktivní aktualizace kvality
description: Tento článek poskytuje informace o proaktivním doručování aktualizací kvality.
author: rashmansur
ms.date: 11/07/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: rashmim
ms.search.validFrom: 2022-08-19
ms.search.form: ''
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 7d8de017c54a13a9935d74d33a57813922c9f823
ms.sourcegitcommit: 8aee31d6dffabe13969dd5b9de4e0bf95f53e67e
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/19/2022
ms.locfileid: "9887123"
---
# <a name="proactive-quality-updates"></a>Proaktivní aktualizace kvality

[!include[banner](../includes/banner.md)]

Během posledních několika let společnost Microsoft neustále pracuje na tom, co nazýváme [One Version](../../dev-itpro/lifecycle-services/oneversion-overview.md). Premisa One Version je jednoduchá: čím blíže k tomu, abychom měli všichni zákazníci stejnou verzi softwaru, tím vyšší kvalitu můžeme dodat. Problémy najdeme a opravíme jednou a tato řešení dostaneme rychleji do rukou více zákazníků.

Tento předpoklad potvrzují i výsledky: nižší počet incidentů napříč našimi produkty. Když zákazníci nepoužívají stejnou verzi, neustále vidíme, že se jich týkají problémy, pro které je již k dispozici řešení. Již jsme dosáhli velkého pokroku s Dynamics 365 Finance, Dynamics 365 Supply Chain, Dynamics 365 Project Operations a Dynamics 365 Commerce a díky nedávnému technickému pokroku je nyní možné udělat další krok. Následující informace vysvětlují, co budeme dělat, co jsme již udělali, abychom připravili půdu, a jak a kdy zavedeme nové schopnosti bez přerušení.

## <a name="what-you-need-to-know"></a>Co potřebujete vědět

- Proaktivní aktualizace kvality (PQU) jsou aplikovány na měsíční bázi.
- Výjimky pro proaktivní aktualizace kvality jsou povoleny pouze pro zákazníky, kteří jsou regulováni americkým Úřadem pro kontrolu potravin a léčiv (FDA).
- Proaktivní aktualizace kvality nikdy nesníží úroveň prostředí ani automaticky neupgradují z jedné verze aktualizace služby na druhou. 
- Microsoft určuje, jak budou spravovány proaktivní aktualizace kvality pro regulovaná prostředí a pro suverénní a vládní cloudové zákazníky.
- Oznámení související s proaktivními aktualizacemi kvality jsou zveřejňována v [Centru zpráv Microsoft 365](https://admin.microsoft.com/AdminPortal/).
- Pět dní před tím, než je na prostředí aplikována proaktivní aktualizace kvality, jsou zákazníci upozorněni, že k aktualizaci dojde.
- Zákazníci nemohou zrušit nebo odložit proaktivní aktualizace kvality.
- Proaktivní aktualizace kvality se instalují během [plánovaného okna údržby](../../dev-itpro/deployment/plannedmaintenance-selfservice.md#windows) dle regionu.
- Aktualizace kvality jsou navrženy tak, aby měly nízké riziko problémů nebo regresí, a to je podporováno daty společnosti Microsoft.
- Společnost Microsoft doporučuje cílené testování na konkrétní problémy nebo konkrétní opravy hotfix související s proaktivní aktualizací kvality.
- VŠECHNYA prostředí sandbox, kromě těch, která mají z regulačních důvodů časově omezenou výjimku, budou zavedena do 7. ledna 2023.
- Provozní onboarding proaktivních aktualizací kvality začne 21. ledna 2023. 
- Provozní onboarding bude zahájen pouze u projektů Lifecycle Services, které mají integrovaná prostředí sandbox a zatím jsou jim proaktivní aktualizace kvality doručovány v pravidelném rytmu pro všechny podporované verze aktualizací služeb. To platí pouze pro zákaznická prostředí, kterým nebyly poskytnuty žádné výjimky z regulačních nebo jiných právních důvodů.
- Úplný plán proaktivních aktualizací kvality pro prostředí sandbox a provozní prostředí v průběhu roku 2023 naleznete níže.
- U každé aktualizace služby probíhá nebo je plánováno zahájení alespoň jedné série vydání proaktivních aktualizací kvality. Jakmile jsou vaše prostředí zapojena do procesu proaktivních aktualizací kvality a přejdete na novější verzi aktualizace služby, můžete obdržet předem naplánované proaktivní aktualizace kvality pro všechna z nich. Pokud plánujete upgradovat na novější verzi aktualizace služby, prohlédněte si plán, kde zjistíte, kdy jsou naplánovány proaktivní aktualizace kvality pro danou aktualizaci služby. 

> [!Note]
> Prostředí sandbox standardního testu výkonu (tier4) nebo prémiového testu výkonu (tier5) a provozní prostředí obdrží proaktivní aktualizace služby o víkendech. 

## <a name="focus-on-quality-updates"></a>Zaměřte se na aktualizace kvality

V současné době nabízíme sedm [aktualizací služeb](public-preview-releases.md) za rok. Například verze 10.0.29 je aktualizace služby. Donedávna bylo osm aktualizací ročně. Jednu aktualizaci jsme však vypustili v reakci na zpětnou vazbu od zákazníků, která odhalila přání vyhnout se změnám ke konci kalendářního roku.

Nebudeme měnit kadenci aktualizací služby. Místo toho se zaměřujeme na náš další krok vpřed na cestě k One Version - *aktualizace kvality*. Atualizace kvality jsou kumulativní sestavení oprav hotfix. Neobsahují nové funkce. V každém okamžiku je celá naše komunita zákazníků rozdělena mezi tři nebo čtyři nejnovější aktualizace služeb. Pro libovolnou aktualizaci služby však lze v rámci skupiny použít desítky verzí aktualizace různé kvality v závislosti na datech, kdy lidé nasadili. V dalším kroku budeme proaktivně vysílat aktualizace kvality. Tento model již používáme pro naše aplikace založené na Dataverse a zaznamenali jsme očekávané výsledky lepší kvality a snížení počtu incidentů podpory.

Snížení počtu závad by samozřejmě mohlo snížit nebo zcela odstranit potřebu aktualizací kvality. Máme za sebou několik iniciativ zaměřených na snížení závad, které vyžadují aktualizace kvality. I když dojde ke snížení užitečného zatížení při aktualizaci kvality, konzistence napříč zákaznickou základnou zlepší podporu, dostane vylepšení pro zákazníky rychleji a sníží frekvenci zákazníků, kteří se setkávají s problémy, pro které již existují řešení.

## <a name="making-proactive-distribution-possible"></a>Umožnění proaktivní distribuce

Již bylo nasazeno několik vylepšení, která umožňují proaktivní doručování aktualizací kvality:

- **Aktualizace téměř nulových prostojů** – Chcete-li prosazovat častější prostředí, je nezbytné, aby byl snížen dopad na dostupnost prostředí, aby byly zachovány smlouvy o úrovni služeb Dynamics 365 (SLA). Aktualizace s téměř nulovými prostoji byla původně zavedena, aby pomohla zlepšit měsíční opravy operačního systému pomocí převzetí služeb při selhání clusteru k aktivaci aktualizované bitové kopie s minimálním narušením. Mechanismus aplikace aktualizací se vylepšuje, aby byl ještě méně rušivý, a bude pokrývat jak záplatování operačního systému, tak nasazení kvalitních aktualizací.

    U interaktivních uživatelů může být aktivní relace přerušena a opakování přejde do nyní aktualizovaného prostředí. Se zavedením [plánování dávek na základě priority](../../dev-itpro/sysadmin/priority-based-batch-scheduling.md) se plánování dávek a zpracování obnoví a obnoví ihned po aktualizaci. Předtím, než se zákazníci začnou podílet na proaktivní distribuci aktualizací kvality pro svá produkční prostředí, bude pro zákazníky k dispozici prioritní plánování dávek.

- **Temné hodiny** – Temné hodiny jsou definovány pro každou oblast Azure a během období temné hodiny dojde k téměř nulovým aktualizacím prostojů.

## <a name="the-proactive-update-process"></a>Proaktivní proces aktualizace

Nasazení proaktivních aktualizací kvality se bude řídit procesem bezpečného nasazení (SDP). Specifika SDP se budou vyvíjet, ale aktualizace kvality budou zpočátku nasazovány do prostředí sandbox. Jak se procento úspěšně nasazených sandboxů zvyšuje, začne nasazení do produkčních prostředí. Naslouchací systémy budou monitorovat systémovou telemetrii a incidenty na Livesite a v případě zjištění jakékoli regrese zastaví zavádění konkrétní verze. Pokud budou zákazníci chtít, budou si stále moci stáhnout aktualizace kvality před proaktivním nasazením.

Aktuální data správy vydání ukazují, že méně než 3 procenta regresí jsou zavedena v aktualizacích kvality. Se zvýšeným zaměřením na eliminaci regrese a vylepšenou SDP bude potenciální dopad regresí dramaticky nižší než zvýšení kvality, kterého se dosáhne rychlejším zavedením oprav u zákazníků v širokém měřítku.

## <a name="process-changes"></a>Zpracovat změny

Před aktivací nasazení proaktivní aktualizace kvality je implementována sada procesních změn:

- **Schéma** – Nástroje zajistí, že kvalitní sestavení aktualizací bude obsahovat pouze změny schématu, které lze použít, když je služba online. Tento přístup pomůže zachovat možnost použít aktualizaci s téměř nulovými prostoji.
- **Zvýšená kontrola změn** – V současné době již existuje další procesní krok ke schválení změn pro zahrnutí do aktualizace kvality. Kontrola v dalším kroku bude zvýšena, aby se snížila možnost regrese. V aktualizacích kvality nejsou povoleny přerušované změny a zvýšená kontrola změn nám pomůže zajistit splnění tohoto cíle.
- **Viditelnost** – upozornění jsou posílána prostřednictvím centra pro správce, Lifecycle Services a dalších dostupných kanálů o nadcházejících proaktivních aktualizacích kvality. Navíc týmy podpory a vedoucí incidentů budou mít přehled o tom, kde byly aktualizace kvality proaktivně nasazeny.

    > [!NOTE]
    > Tým Microsoft Communications vyšetřuje pokračující degradaci e-mailových nástrojů, které brání doručování e-mailových upozornění. Prosím pokračujte ve sledování Centra zpráv Microsoft 365 pro zprávy týkající se onboardingu a oznámení.

- **Odolnost proti selhání prostřednictvím publikování testovacích verzí** – Publikování testovacích verzí bude ve všech možných případech použito ke hlídání změn kódu opravy chyby aktualizace pro zvýšení kvality nebo se použije publikování testovacích verzí existující funkce relevantní pro opravu. Pokud je po proaktivním nasazení vyžadována záloha nebo vypnutí změny, lze to provést prostřednictvím systému publikování testovacích verzí, aby se předešlo dalším selháním.
- **Označení synchronizace s prostředím sandbox** – Postupná aktualizace na izolované prostředí sandbox dle výběru spolu s provozním prostředím není v současné době podporována. Všechna prostředí sandboxy úrovně 2 a 3 obdrží proaktivní aktualizace nejméně 7 dní před provozním prostředím v projektu Lifecycle Services. Opět to platí pouze pro zákaznická prostředí, kterým nejsou poskytnuty žádné výjimky z regulačních nebo jiných právních důvodů.

## <a name="what-is-the-rollout-roadmap-for-quality-updates"></a>Jaký je plán zavádění aktualizací kvality?

Očekává se, že distribuce proaktivních aktualizací kvality pro prostředí sandbox začne pro zákazníky veřejného cloudu Azure v září 2022. Do 1. ledna 2023 dokončíme onboarding 99 % prostředí sandbox do proaktivních aktualizací kvality.

Výjimky z proaktivního aktualizovaného distribučního procesu jsou povoleny pouze pro zákazníky regulované FDA. Stále pracujeme na tom, jak budou spravována regulovaná prostředí a suverénní a vládní cloudoví zákazníci. 

Protože zákazníci budou pravidelně dostávat menší užitečné zatížení, očekáváme, že se proces udržování aktuálního stavu zjednoduší. Frekvenci zavádění aktualizací upravíme, jakmile prokážeme schopnost spustit proces bez přerušení. Tento proces již efektivně funguje na naší platformě a aplikacích Dataverse a přináší očekávaná zlepšení kvality služeb. Stejný krok vpřed učiníme pro pro finanční a provozní aplikace.


## <a name="when-will-quality-updates-start-for-production-environments"></a>Kdy začnou aktualizace kvality pro produkční prostředí?
Během prvních několika měsíců roku 2023, počínaje 15. lednem, začneme s onboardingem provozních prostředí na proaktivní aktualizace a postupně budeme zvyšovat procento provozních prostředí, která získávají proaktivní aktualizace. Zaměříme se pouze na provozní prostředí v projektu Lifecycle Services, který již má integrovaná prostředí sandbox, aby bylo možné přijímat proaktivní aktualizace. Před aktualizací budou zákazníci s integrovaným provozním prostředím informováni prostřednictvím centra zpráv nebo banneru Lifecycle Services. Úplný plán proaktivních aktualizací kvality pro prostředí sandbox a provozní prostředí v průběhu roku 2023 naleznete níže.

## <a name="what-is-the-schedule-for-sandbox-proactive-quality-updates"></a>Jaký je plán aktualizací proaktivní kvality sandboxu?
Informace o nočních hodinách pro každý region najdete v článku [Jaká jsou plánovaná okna údržby podle regionů?](../../dev-itpro/deployment/plannedmaintenance-selfservice.md#windows).

### <a name="proactive-quality-update-release-10029"></a><a name="schedule"></a> Proaktivní aktualizace kvality, verze: 10.0.29
**Verze aplikace: 10.0.1326.70**  
**Odpovídající nejnovější článek znalostní báze: 750332**

| Stanice | Oblasti | Dokončený plán | Připravovaný plán sandboxu|
|---|---|---|---|
| Stanice 1 | Kanada střed, Kanada východ, Francie střed, Indie střed, Norsko východ, Švýcarsko západ | 14. října až 17. října 2022, 2. listopadu až 5. listopadu 2022, 13. listopadu až 16. listopadu 2022, 5. prosince až 8. prosince 2022 | 2. ledna až 5. ledna 2023 |
| Stanice 2 | Francie jih, Indie jih, Norsko západ, Švýcarsko sever, Jižní Afrika sever, Austrálie východ, Spojené království jih, SAE sever, Japonsko východ, Austrálie jihovýchod, jihovýchodní Asie | 15. října až 18. října 2022, 2. listopadu až 5. listopadu 2022, 13. listopadu až 16. listopadu 2022, 5. prosince až 8. prosince 2022 | 2. ledna až 5. ledna 2023 |
| Stanice 3 | Východní Asie, Spojené království západ, Japonsko západ, Brazílie jih, západní Evropa, východ USA, SAE střed | 16. října až 19. října 2022, 2. listopadu až 5. listopadu 2022, 13. listopadu až 16. listopadu 2022, 5. prosince až 8. prosince 2022 | 2. ledna až 5. ledna 2023 |
| Stanice 4 | Severní Evropa, střední USA, západní USA | 17. října až 20. října 2022, 2. listopadu až 5. listopadu 2022, 15. listopadu až 18. listopadu 2022, 5. prosince až 8. prosince 2022 | 2. ledna až 5. ledna 2023 |
| Stanice 5 | DoD, Government Community Cloud, Čína | Neplánováno | Neplánováno |

### <a name="proactive-quality-update-release-10030"></a><a name="schedule"></a> Proaktivní aktualizace kvality, verze: 10.0.30
**Verze aplikace: 10.0.1362.77**
**Odpovídající nejnovější článek znalostní báze: 767597**

| Stanice | Oblasti | Dokončený plán | Připravovaný plán sandboxu |
|---|---|---|---|
| Stanice 1 | Kanada střed, Kanada východ, Francie střed, Indie střed, Norsko východ, Švýcarsko západ | 1. prosince až 4. prosince 2022 |  13. prosince až 16. prosince 2022 | 
| Stanice 2 | Francie jih, Indie jih, Norsko západ, Švýcarsko sever, Jižní Afrika sever, Austrálie východ, Spojené království jih, SAE sever, Japonsko východ, Austrálie jihovýchod, jihovýchodní Asie | 2. prosince až 5. prosince 2022 |  13. prosince až 16. prosince 2022 | 
| Stanice 3 | Východní Asie, Spojené království západ, Japonsko západ, Brazílie jih, severní Evropa, východ USA, SAE střed | 3. prosince až 6. prosince 2022 |  13. prosince až 16. prosince 2022 | 
| Stanice 4 | Západní Evropa, střední USA, západní USA | 4. prosince až 7. prosince 2022 |  13. prosince až 16. prosince 2022 | 
| Stanice 5 | DoD, Government Community Cloud, Čína | Neplánováno | Neplánováno |

### <a name="proactive-quality-update-calendar-year-2023-schedule"></a><a name="schedule"></a> Harmonogram kalendářního roku 2023 proaktivních aktualizací kvality

#### <a name="stations-to-region-mapping"></a><a name="Stations-Regions"></a> Mapování stanic na oblasti

| Stanice | Oblasti |
|---|---|
| Stanice 1 | Bude určeno |
| Stanice 2 | Kanada střed, Kanada východ, Francie střed, Indie střed, Norsko východ, Švýcarsko západ |
| Stanice 3 | Francie jih, Indie jih, Norsko západ, Švýcarsko sever, Jižní Afrika sever, Austrálie východ, Spojené království jih, SAE sever, Japonsko východ, Austrálie jihovýchod, jihovýchodní Asie |
| Stanice 4 | Východní Asie, Spojené království západ, Japonsko západ, Brazílie jih, severní Evropa, východ USA, SAE střed |
| Stanice 5 | Západní Evropa, střední USA, západní USA |
| Stanice 6 | DoD, Government Community Cloud, Čína |


> [!IMPORTANT]
> Toto je plán vysoké úrovně na rok 2023. Pro konkrétnější harmonogram se podívejte na ukázku níže pro leden 10.0.30 Release-2. Přesný plán a verze aplikací budou aktualizovány 7 dní před zahájením série aktualizací kvality.

> [!Note]
> Aktualizaci pro sérii 10.0.30 Release-2 obdrží pouze integrovaná provozní prostředí, integrovaná prostředí obdrží explicitní sdělení.

| Série aktualizací kvality | Vydání | Doba trvání série |
|---|---|---|
| 10.0.30 Release-2 | 16. prosince 2022 | 2. ledna až 29. ledna 2023 |
| 10.0.30 Release-3 | 13. ledna 2023 | 30. ledna až 25. února 2023 |
| 10.0.30 Release-4 | 24. února 2023 | 6. března až 8. dubna 2023 |
| 10.0.31 Release-1 | 3. února 2023 | 13. února 2023 až 18. března 2023|
| 10.0.31 Release-2 | 3. března 2023 | 13. března 2023 až 15. dubna 2023|
| 10.0.31 Release-3 | 14. dubna 2023 | 24. dubna 2023 až 27. května 2023|
| 10.0.32 Release-1 | 31. března 2023 | 10. dubna 2023 až 13. května 2023|
| 10.0.32 Release-2 | 28. dubna 2023 | 8. května 2023 až 10. června 2023|
| 10.0.32 Release-3 | 26. května 2023 | 5. června 2023 až 8. července 2023|
| 10.0.33 Release-1 | 28. dubna 2023 | 8. května 2023 až 10. června 2023|
| 10.0.33 Release-2 | 26. května 2023 | 5. června 2023 až 8. července 2023|
| 10.0.33 Release-3 | 14. července 2023 | 24. července 2023 až 26. srpna 2023|
| 10.0.34 Release-1 | 23. června 2023 | 3. července 2023 až 5. srpna 2023|
| 10.0.34 Release-2 | 21. července 2023 | 31. července 2023 až 2. září 2023|
| 10.0.34 Release-3 | 1. září 2023 | 11. září 2023 až 14. října 2023|
| 10.0.35 Release-1 | 28. července 2023 | 7. srpna 2023 až 9. září 2023|
| 10.0.35 Release-2 | 25. srpna 2023 | 4. září 2023 až 7. října 2023|
| 10.0.35 Release-3 | 20. října 2023 | 30. října 2023 až 16. prosince 2023|
| 10.0.36 Release-1 | 29. září 2023 | 9. října 2023 až 11. listopadu 2023|
| 10.0.36 Release-2 | 27. října 2023 | 6. listopadu 2023 až 16. prosince 2023|
| 10.0.36 Release-3 | 12. ledna 2024 | 22. ledna 2023 až 24. února 2024|
| 10.0.37 Release-1 | 3. listopadu 2023 | 13. listopadu 2023 až 6. ledna 2024|
| 10.0.37 Release-2 | 30. prosince 2023 | 8. ledna 2024 až 10. února 2024|
| 10.0.37 Release-3 | 27. ledna 2024 | 5. února 2024 až 9. března 2024|
| 10.0.37 Release-4 | 23. února 2024 | 4. března 2024 až 6. dubna 2024|

### <a name="proactive-quality-update-upcoming-10030-release-2-train-schedule"></a><a name="schedule"></a> Proaktivní aktualizace kvality pro plán série 10.0.30 Release-2
**Verze aplikace: 10.0.1362.99**

| Stanice | Připravovaný plán sandboxu | nadcházející provozní plán |
|---|---|---|
| Stanice 1 | Není k dispozici | Není k dispozici |
| Stanice 2 | 2. ledna až 5. ledna 2023 | 21. ledna až 22. ledna 2023 |
| Stanice 3 | 3. ledna až 6. ledna 2023 | 28. ledna až 29. ledna 2023 |
| Stanice 4 | 9. ledna až 12. ledna 2023 | Není k dispozici |
| Stanice 5 | 16. ledna až 19. ledna 2023 | Není k dispozici |
| Stanice 6 | Není k dispozici | Není k dispozici |

> [!IMPORTANT] 
> Pět dní předem společnost Microsoft aktualizuje předchozí plán a odešle upozornění do sady prostředí, která mají naplánováno přijímat tyto aktualizace kvality. Předchozí plán platí pouze pro prostředí, která byla upozorněna na nadcházející aktualizaci. Informace o nočních hodinách pro každý region najdete v článku [Jaká jsou plánovaná okna údržby podle regionů?](../../dev-itpro/deployment/plannedmaintenance-selfservice.md#windows).
>
> Pro každou skupinu regionů, popř. *stanice*, kde je aktuálně naplánováno vydání aktualizace kvality, plán ukazuje rozmezí čtyř dnů. Aktualizace kvality začnou pouze v prostředích sandbox. Poté, jak se procento úspěšně nasazených sandboxů zvýší, začne nasazení do produkčních prostředí se zasílanými oznámeními pro zákazníky o pokroku.
> 
> Aktualizace kvality budou vždy probíhat průběžně, což nám umožňuje zaměřit se na sadu prostředí podle plánu a dokončit všechny sady pro stanici do konce čtvrtého dne. To však neznamená, že aktualizace prostředí bude trvat čtyři dny. Znamená to pouze, že nemůžeme předem určit, která sada prostředí bude aktualizována v daný den čtyřdenního rozsahu. Všechny aktualizace budou prováděny během nočních hodin, s téměř nulovými výpadky. Aktualizace definitivně skončí během noci v daném regionu.

## <a name="how-are-the-dark-hours-handled-for-customers-that-have-one-finance-and-operations-apps-instance-but-are-active-in-multiple-time-zones"></a>Jak se řeší noční hodiny u zákazníků, kteří mají jednu instanci finančních a provozních aplikací, ale jsou aktivní ve více časových pásmech? 
Neexistují žádné zvláštní plány mimo noční hodiny, kde existuje instance finančních a provozních aplikací, protože plánujeme zavádět aktualizace kvality minimálně rušivým způsobem s [nZDT](../../dev-itpro/deployment/plannedmaintenance-selfservice.md#what-does-near-zero-downtime-maintenance-mean).

## <a name="what-is-the-current-rollout-cadence-for-proactive-quality-updates"></a>Jaký je aktuální plán zavádění proaktivních aktualizací kvality?
Proaktivní aktualizace kvality (PQU) jsou v současné době nasazovány jednou měsíčně pro každou podporovanou verzi aktualizace služby. Pro vybraná prostředí sandbox je nabízena pouze jedna aktualizace za měsíc, pokud zákazníci nepřejdou na novou verzi aktualizace služby. V takovém případě mohou získat předem naplánované proaktivní aktualizace kvality jako součást stávající série pro novou aktualizaci služby. Po dokončení celosvětového zavedení v roce 2023 se frekvence těchto aktualizací zvýší. Vždy, když dojde ke změně frekvence vydání, budete informováni alespoň jeden měsíc předem.

## <a name="how-will-microsoft-ensure-the-quality-of-these-updates"></a>Jak společnost Microsoft zajistí kvalitu těchto aktualizací?
Společnost Microsoft se snaží udržet kanál vydání dostatečně efektivní, aby poskytoval malé užitečné zatížení a udržoval nízké náklady na ověřování. Každá oprava v aktualizaci kvality prochází přísným a bezpečným procesem nasazení, který pomáhá zlepšit kvalitu a spolehlivost, a tím snížit dopad na zákazníky. Nasazení proběhne nejprve ve fázích v prostředí sandbox, poté bude následovat produkce. Nasazení nanečisto umožňují správné sledování, aby se zjistilo, zda je další nasazení bezpečné. Zavádění zastavíme, pokud budou zjištěny problémy s každou nasazenou skupinou zákazníků, a zajistíme, aby každý krok zavádění měl dostatek času na to, aby se problémy objevily. U každé nadcházející aktualizace kvality poskytneme přehled o plánu prostřednictvím aktualizací veřejné dokumentace a e-mailů, aby zákazníci mohli plánovat dopředu.

## <a name="can-customers-delay-reschedule-or-pause-a-quality-update"></a>Mohou zákazníci odložit, přeplánovat nebo pozastavit aktualizaci kvality?
Ne. Hlavním cílem kvalitních aktualizací je zajistit, aby se pro naše zákazníky neustále zlepšovaly základy, jako je zabezpečení, soukromí, spolehlivost, dostupnost a výkon. Zpožděním nebo pozastavením aktualizace bude ohrožena bezpečnost, dostupnost a spolehlivost.

## <a name="how-do-i-know-what-set-of-changes-went-into-a-quality-update-payload"></a>Jak mohu zjistit, která sada změn šla do datové části aktualizace kvality?
Podle níže uvedených kroků identifikujte seznam změn, které jdou do datové části aktualizace kvality. 

Použijte sérii aktualizace kvality 10.0.28 a související verzi aplikace 10.0.1265.89.

1. V Lifecycle Services otevřete stránku **Podrobnosti prostředí** pro váš sandbox. 
2. V části **Dostupné aktualizace** vyberte možnost **Zobrazit aktualizaci** a uvidíte nejnovější sestavení aktualizace kvality. 
3. Exportujte sestavení do souboru CSV nebo Microsoft Excel.
4. V exportovaném souboru filtrujte a vyberte **Verze sestavení**, která je menší nebo rovna číslu sestavení 10.0.1265.89. Nyní byste měli vidět rozdílovou datovou část.
 
> [!NOTE]
> Export do souboru CSV nebo Excel musí proběhnout před aktualizací prostředí. V opačném případě můžete použít prostředí s podobnou konfigurací, které nemá nainstalovanou aktualizaci, a postupujte podle výše uvedených kroků.

[![Příklad prostředí s aktualizací kvality.](./media/how-to-get-kb-list-pqu.png)](./media/how-to-get-kb-list-pqu.png)

## <a name="what-is-the-process-if-a-critical-issue-is-found-after-a-quality-update"></a>Jaký je postup, pokud je po aktualizaci kvality nalezen kritický problém?
Kritický problém nebo regrese je jedna nebo více událostí, které obvykle způsobí, že několik zákazníků bude mít zhoršené fungování u jedné nebo více našich služeb. Tyto problémy mohou způsobit neplánované prostoje včetně nedostupnosti, snížení výkonu a narušení správy služeb. Pokud dojde v důsledku takových regresí k širokému dopadu na zákazníky, zastavíme zavádění kvalitní aktualizace, dokud nebudeme moci komunikovat a problém vyřešit. Další aktualizace kvality bude mít obvykle nezbytnou opravu pro obnovení zavádění.

Pokud je ovlivněno prostředí jednoho zákazníka, obraťte se na podporu společnosti Microsoft a otevřete lístek. Na základě odůvodnění zastavíme zavádění aktualizace kvality do všech ostatních prostředí v tomto projektu, dokud nebude problém opraven.

## <a name="can-customers-still-manually-apply-hotfix-updates-from-lifecycle-services"></a>Mohou zákazníci stále ručně používat aktualizace oprav hotfix z Lifecycle Services?
Ano. Aby byla zajištěna trvalá rovnost s tím, jak opravy hotfix fungují, lze aktualizace oprav hotfix stále aplikovat na zákaznická prostředí v Lifecycle Services. Je však důležité si uvědomit, že opravy hotfix, které jsou nasazeny jako součást aktualizace kvality, procházejí před nasazením aktualizace standardním SDP. Tím se snižuje riziko regresí kvůli vyšší kvalitě. Pro zvýšení spolehlivosti doporučujeme zvolit kvalitní aktualizaci před ručním použitím oprav hotfix.

## <a name="can-customers-proactively-install-a-quality-update-build-ahead-of-the-schedule"></a>Mohou si zákazníci proaktivně sami nainstalovat aktualizaci kvality ještě před plánem?
Ano. Aktualizaci kvality můžete nainstalovat proaktivně. Společnost Microsoft aktualizaci přeskočí, pokud je aktuální verze sestavení prostředí stejná nebo vyšší než příslušná aktualizace kvality.

## <a name="if-an-environment-has-an-upcoming-scheduled-monthly-service-update-within-a-week-will-it-still-receive-quality-updates"></a>Pokud má prostředí nadcházející plánovanou měsíční aktualizaci služby do týdne, dostane přesto aktualizaci kvality?
- Aktualizace kvality se na produkční prostředí nepoužijí, pokud je do týdne od plánovaného provedení aktualizace kvality naplánována nadcházející aktualizace služby.
- Pokud má prostředí sandbox stejnou nebo vyšší verzi sestavení než nadcházející aktualizace kvality, bude přeskočeno.
- Pokud má produkční prostředí stejnou nebo vyšší verzi sestavení než nadcházející aktualizace kvality, bude přeskočeno.
- Pokud má sandbox stejnou nebo vyšší verzi sestavení kvůli aktualizaci kvality nebo ruční aktualizaci produkce, produkce stále získá plánovanou verzi měsíční aktualizace služby. Pokud nechcete, aby se plánované produkční prostředí aktualizovalo na verzi aktualizace služby, můžete aktualizaci služby z Lifecycle Services pozastavit. 
- Doporučujeme vám použít nejnovější sestavení aktualizace kvality k otestování změn pro nadcházející aktualizaci služby pro lepší stabilitu a výsledky.

## <a name="if-an-environment-has-an-upcoming-scheduled-action-and-a-scheduled-quality-update-in-the-same-maintenance-window-will-it-still-receive-the-quality-update"></a>Pokud má prostředí nadcházející naplánovanou akci a plánovanou aktualizaci kvality ve stejném okně údržby, bude stále dostávat aktualizaci kvality?
Pokud dojde k nějakému sporu s předem naplánovanou akcí, například PITR (Obnovení k určitému bodu v čase), aktualizace kvality bude přeplánována na další dostupné okno údržby během čtyřdenního okna. Další informace o plánu viz článek [Jaký je plán proaktivních aktualizací kvality?](#schedule). 

## <a name="can-an-environment-be-brought-back-to-its-previous-state-if-there-are-issues-after-a-quality-update-is-applied"></a>Lze prostředí vrátit do předchozího stavu, pokud se po použití aktualizace kvality vyskytnou problémy?
Po použití aktualizace kvality nedochází za žádných okolností k žádnému vrácení. Pro řešení problémů jsou k dispozici pouze možnosti předávání oprav.

## <a name="what-about-fda-regulation-and-gxp"></a>A co regulace FDA a GxP?
Plán pro zákazníky podléhající validaci a regulaci FDA se stále vyvíjí. Brzy očekávejte další aktualizace v tomto prostoru. Prozatím jsou všichni tito zákazníci vyjmuti z aktualizací kvality. Chcete-li zajistit, aby se zákazník musel řídit předpisy FDA, navštivte [Nabídku GxP Microsoft Azure](/azure/compliance/offerings/offering-gxp).

## <a name="what-versions-of-service-updates-are-supported-for-these-quality-updates"></a>Jaké verze aktualizací služeb jsou podporovány pro tyto aktualizace kvality?
Zákazníci se všemi podporovanými verzemi aktualizací služeb mají nárok na aktualizace kvality. 

## <a name="finance-and-operations-apps-deployments-with-retail-components-typically-require-additional-work-in-addition-to-having-to-redeploy-mpos-how-will-these-quality-updates-impact-the-retail-sdk"></a>Nasazení finančních a provozních aplikací s maloobchodními komponentami obvykle vyžadují další práci kromě nutnosti znovu nasadit MPOS. Jak tyto aktualizace kvality ovlivní Retail SDK? 
Vzhledem k tomu, že povaha samotné opravy hotfix se nemění v datové části aktualizací kvality, neočekáváme žádný další dopad konkrétně související s maloobchodními komponentami.

## <a name="is-there-any-impact-to-cloud-hosted-environments-che"></a>Má to nějaký dopad na prostředí hostovaná v cloudu (CHE)? 
Prostředí CHE jsou mimo rozsah aktualizací kvality, protože jsou mimo působnost společnosti Microsoft.

## <a name="are-there-any-integration-issues-with-microsoft-dataverse"></a>Existují nějaké problémy s integrací s Microsoft Dataverse? 
Nejsou známy žádné problémy integrace aktualizací kvality s Dataverse.

