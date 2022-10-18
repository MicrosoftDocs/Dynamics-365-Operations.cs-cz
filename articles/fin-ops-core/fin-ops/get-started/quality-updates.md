---
title: Proaktivní aktualizace kvality
description: Tento článek poskytuje informace o proaktivním doručování aktualizací kvality.
author: rashmansur
ms.date: 09/12/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: rashmim
ms.search.validFrom: 2022-08-19
ms.search.form: ''
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 25306a8ccebb5cd01debc90cf497d4a942840ef4
ms.sourcegitcommit: 43a0fb019bc67c00c39c2778343ba89924c3322c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/12/2022
ms.locfileid: "9671418"
---
# <a name="proactive-quality-updates"></a>Proaktivní aktualizace kvality

[!include[banner](../includes/banner.md)]

Během posledních několika let společnost Microsoft neustále pracuje na tom, co nazýváme [One Version](../../dev-itpro/lifecycle-services/oneversion-overview.md). Premisa One Version je jednoduchá: čím blíže k tomu, abychom měli všichni zákazníci stejnou verzi softwaru, tím vyšší kvalitu můžeme dodat. Problémy najdeme a opravíme jednou a tato řešení dostaneme rychleji do rukou více zákazníků.

Tento předpoklad potvrzují i výsledky: nižší počet incidentů napříč našimi produkty. Když zákazníci nepoužívají stejnou verzi, neustále vidíme, že se jich týkají problémy, pro které je již k dispozici řešení. Již jsme dosáhli velkého pokroku s Dynamics 365 Finance, Dynamics 365 Supply Chain, Dynamics 365 Project Operations a Dynamics 365 Commerce a díky nedávnému technickému pokroku je nyní možné udělat další krok. Následující informace vysvětlují, co budeme dělat, co jsme již udělali, abychom připravili půdu, a jak a kdy zavedeme nové schopnosti bez přerušení.

## <a name="focus-on-quality-updates"></a>Zaměřte se na aktualizace kvality

V současné době nabízíme sedm [aktualizací služeb](public-preview-releases.md) za rok. Například verze 10.0.29 je aktualizace služby. Donedávna bylo osm aktualizací ročně. Jednu aktualizaci jsme však vypustili v reakci na zpětnou vazbu od zákazníků, která odhalila přání vyhnout se změnám ke konci kalendářního roku.

Nebudeme měnit kadenci aktualizací služby. Místo toho se zaměřujeme na náš další krok vpřed na cestě k One Version - *aktualizace kvality*. Atualizace kvality jsou kumulativní sestavení oprav hotfix. Neobsahují nové funkce. V každém okamžiku je celá naše komunita zákazníků rozdělena mezi tři nebo čtyři nejnovější aktualizace služeb. Pro libovolnou aktualizaci služby však lze v rámci skupiny použít desítky verzí aktualizace různé kvality v závislosti na datech, kdy lidé nasadili. V dalším kroku budeme proaktivně vysílat aktualizace kvality. Tento model již používáme pro naše aplikace založené na Dataverse a zaznamenali jsme očekávané výsledky lepší kvality a snížení počtu incidentů podpory.

Snížení počtu závad by samozřejmě mohlo snížit nebo zcela odstranit potřebu aktualizací kvality. Máme za sebou několik iniciativ zaměřených na snížení závad, které vyžadují aktualizace kvality. I když dojde ke snížení užitečného zatížení při aktualizaci kvality, konzistence napříč zákaznickou základnou zlepší podporu, dostane vylepšení pro zákazníky rychleji a sníží frekvenci zákazníků, kteří se setkávají s problémy, pro které již existují řešení.

## <a name="making-proactive-distribution-possible"></a>Umožnění proaktivní distribuce

Již bylo nasazeno několik vylepšení, která umožňují proaktivní doručování aktualizací kvality:

- **Aktualizace téměř nulových prostojů** – Chcete-li prosazovat častější prostředí, je nezbytné, aby byl snížen dopad na dostupnost prostředí, aby byly zachovány smlouvy o úrovni služeb Dynamics 365 (SLA). Aktualizace s téměř nulovými prostoji byla původně zavedena, aby pomohla zlepšit měsíční opravy operačního systému pomocí převzetí služeb při selhání clusteru k aktivaci aktualizované bitové kopie s minimálním narušením. Mechanismus aplikace aktualizací se vylepšuje, aby byl ještě méně rušivý, a bude pokrývat jak záplatování operačního systému, tak nasazení kvalitních aktualizací.

    U interaktivních uživatelů může být aktivní relace přerušena a opakování přejde do nyní aktualizovaného prostředí. Se zavedením [plánování dávek na základě priority](../../dev-itpro/sysadmin/priority-based-batch-scheduling.md), který je nyní k dispozici na základě přihlášení, se plánování dávek a zpracování obnoví a obnoví ihned po aktualizaci. Předtím, než se zákazníci začnou podílet na proaktivní distribuci aktualizací kvality pro svá produkční prostředí, bude pro zákazníky k dispozici prioritní plánování dávek.

- **Temné hodiny** – Temné hodiny jsou definovány pro každou oblast Azure a během období temné hodiny dojde k téměř nulovým aktualizacím prostojů.

## <a name="the-proactive-update-process"></a>Proaktivní proces aktualizace

Nasazení proaktivních aktualizací kvality se bude řídit procesem bezpečného nasazení (SDP). Specifika SDP se budou vyvíjet, ale aktualizace kvality budou zpočátku nasazovány do prostředí sandbox. Proces bude zahájen v prostředích, která se rozhodnou pro včasné nasazení. Jak se procento úspěšně nasazených sandboxů zvyšuje, začne nasazení do produkčních prostředí. Proces bude opět zahájen v prostředích, která se rozhodnou pro včasné nasazení. Naslouchací systémy budou monitorovat systémovou telemetrii a incidenty na Livesite a v případě zjištění jakékoli regrese zastaví zavádění konkrétní verze. Pokud budou zákazníci chtít, budou si stále moci stáhnout aktualizace kvality před proaktivním nasazením.

Aktuální data správy vydání ukazují, že méně než 3 procenta regresí jsou zavedena v aktualizacích kvality. Se zvýšeným zaměřením na eliminaci regrese a vylepšenou SDP bude potenciální dopad regresí dramaticky nižší než zvýšení kvality, kterého se dosáhne rychlejším zavedením oprav u zákazníků v širokém měřítku.

## <a name="process-changes"></a>Zpracovat změny

Před aktivací nasazení proaktivní aktualizace kvality je implementována sada procesních změn:

- **Schéma** – Nástroje zajistí, že kvalitní sestavení aktualizací bude obsahovat pouze změny schématu, které lze použít, když je služba online. Tento přístup pomůže zachovat možnost použít aktualizaci s téměř nulovými prostoji.
- **Zvýšená kontrola změn** – V současné době již existuje další procesní krok ke schválení změn pro zahrnutí do aktualizace kvality. Kontrola v dalším kroku bude zvýšena, aby se snížila možnost regrese. V aktualizacích kvality nejsou povoleny přerušované změny a zvýšená kontrola změn nám pomůže zajistit splnění tohoto cíle.
- **Viditelnost** – Budeme zasílat upozornění prostřednictvím e-mailu a služeb Lifecycle Services (LCS) o nadcházejících proaktivních aktualizacích kvality. Navíc týmy podpory a vedoucí incidentů budou mít přehled o tom, kde byly aktualizace kvality proaktivně nasazeny.
- **Odolnost proti selhání prostřednictvím publikování testovacích verzí** – Publikování testovacích verzí bude ve všech možných případech použito ke hlídání změn kódu opravy chyby aktualizace pro zvýšení kvality nebo se použije publikování testovacích verzí existující funkce relevantní pro opravu. Pokud je po proaktivním nasazení vyžadována záloha nebo vypnutí změny, lze to provést prostřednictvím systému publikování testovacích verzí, aby se předešlo dalším selháním.
- **Označení synchronizace sandboxu** – Méně než 20 procent zákazníků má dnes více sandboxů a jeden sandbox si ponechává nasazený tam, kde se verze shoduje s produkčním řešením, aby pomohli s řešením problémů. Pokud zákazník používá sandbox k testování novější verze, než je jeho produkční verze, bude tento sandbox dostávat aktualizace kvality na novější verzi.

## <a name="what-is-the-rollout-roadmap-for-quality-updates"></a>Jaký je plán zavádění aktualizací kvality?

Očekává se, že distribuce proaktivních aktualizací kvality pro prostředí sandbox začne pro zákazníky veřejného cloudu Azure koncem září nebo října 2022. Zkušební prostředí také začnou dostávat proaktivní nasazení aktualizací v té době. V září bude každému zákazníkovi zasláno upozornění, které ho informuje o očekávaném plánu pro jeho prostředí. Výjimky z proaktivního aktualizovaného distribučního procesu budou povoleny pouze pro zákazníky regulované FDA. Stále pracujeme na tom, jak budou spravována regulovaná prostředí a suverénní a vládní cloudoví zákazníci.

Během příštích šesti měsíců budeme postupně zvyšovat procento sandboxových prostředí, která obdrží proaktivní aktualizace, dokud nebudou zahrnuta všechna určená prostředí a postoupíme k aktualizaci produkčních prostředí. Během tohoto období budeme monitorovat, abychom zajistili, že proces nasazení bude bezproblémový a že dosáhneme cíle nerušivého užitečného zatížení.

Protože zákazníci budou pravidelně dostávat menší užitečné zatížení, očekáváme, že se proces udržování aktuálního stavu zjednoduší. Frekvenci zavádění aktualizací upravíme, jakmile prokážeme schopnost spustit proces bez přerušení. Tento proces již efektivně funguje na naší platformě a aplikacích Dataverse a přináší očekávaná zlepšení kvality služeb. Těšíme se, že uděláme stejný krok vpřed pro finanční a provozní aplikace.

## <a name="when-will-quality-updates-start-for-production-environments"></a>Kdy začnou aktualizace kvality pro produkční prostředí?
V současné době se aktualizace kvality zaměřují pouze na izolované prostory. Tento prostor aktualizujeme od počátečního data provozního prostředí, až budeme mít konkrétnější data a metriky počínaje proaktivními aktualizacemi prostředí sandbox a konče měřením připravenosti provozu.

## <a name="what-is-the-schedule-for-sandbox-proactive-quality-updates"></a>Jaký je plán aktualizací proaktivní kvality sandboxu?
Informace o nočních hodinách pro každý region najdete v článku [Jaká jsou plánovaná okna údržby podle regionů?](../../dev-itpro/deployment/plannedmaintenance-selfservice.md#windows).

### <a name="proactive-quality-update-release-10028"></a>Proaktivní aktualizace kvality, verze: 10.0.28
**Verze aplikace: 10.0.1265.89**
**Odpovídající nejnovější článek znalostní báze: 745340**

| Stanice | Oblasti | Dokončený plán| Připravovaný plán sandboxu
|---|---|---|---|
| Stanice 1 | Kanada střed, Kanada východ, Francie střed, Indie střed, Norsko východ, Švýcarsko západ | 15. září až 18. září 2022 a 19. září až 22. září 2022 | 7. října až 10. října 2022 |
| Stanice 2 | Francie jih, Indie jih, Norsko západ, Švýcarsko sever, Jižní Afrika sever, Austrálie východ, Spojené království jih, SAE sever, Japonsko východ, Austrálie jihovýchod, jihovýchodní Asie | 25. září až 28. září 2022 | 7. října až 10. října 2022 |
| Stanice 3 | Východní Asie, Spojené království západ, Japonsko západ, Brazílie jih, západní Evropa, východ USA, SAE střed | 26. září až 29. září 2022 | 7. října až 10. října 2022 |
| Stanice 4 | Severní Evropa, střední USA, západní USA | 28. září až 1. října 2022 | 7. října až 10. října 2022 |
| Stanice 5 | DoD, Government Community Cloud, Čína | Neplánováno | Neplánováno |

### <a name="proactive-quality-update-release-10029"></a><a name="schedule"></a> Proaktivní aktualizace kvality, verze: 10.0.29
**Verze aplikace: 10.0.1326.70**
**Odpovídající nejnovější článek znalostní báze: 748926**

| Stanice | Oblasti | Připravovaný plán sandboxu
|---|---|---|
| Stanice 1 | Kanada střed, Kanada východ, Francie střed, Indie střed, Norsko východ, Švýcarsko západ | 14. října až 17. října 2022 |
| Stanice 2 | Francie jih, Indie jih, Norsko západ, Švýcarsko sever, Jižní Afrika sever, Austrálie východ, Spojené království jih, SAE sever, Japonsko východ, Austrálie jihovýchod, jihovýchodní Asie | 15. října až 18. října 2022 |
| Stanice 3 | Východní Asie, Spojené království západ, Japonsko západ, Brazílie jih, západní Evropa, východ USA, SAE střed | 16. října až 19. října 2022 |
| Stanice 4 | Severní Evropa, střední USA, západní USA | 17. října až 20. října 2022 |
| Stanice 5 | DoD, Government Community Cloud, Čína | Neplánováno |

> [!IMPORTANT] 
> Pět dní předem společnost Microsoft aktualizuje předchozí plán a odešle e-mailová upozornění do sady prostředí, která mají naplánováno přijímat tyto aktualizace kvality. Předchozí plán platí pouze pro prostředí, která byla upozorněna na nadcházející aktualizaci. Informace o nočních hodinách pro každý region najdete v článku [Jaká jsou plánovaná okna údržby podle regionů?](../../dev-itpro/deployment/plannedmaintenance-selfservice.md#windows).
>
> Pro každou skupinu regionů, popř. *stanice*, kde je aktuálně naplánováno vydání aktualizace kvality, plán ukazuje rozmezí čtyř dnů. Aktualizace kvality začnou pouze v prostředích sandbox. Poté, jak se procento úspěšně nasazených sandboxů zvýší, začne nasazení do produkčních prostředí se zasílanými oznámeními pro zákazníky o pokroku.
> 
> Aktualizace kvality budou vždy probíhat průběžně, což nám umožňuje zaměřit se na sadu prostředí podle plánu a dokončit všechny sady pro stanici do konce čtvrtého dne. To však neznamená, že aktualizace prostředí bude trvat čtyři dny. Znamená to pouze, že nemůžeme předem určit, která sada prostředí bude aktualizována v daný den čtyřdenního rozsahu. Všechny aktualizace budou prováděny během nočních hodin, s téměř nulovými výpadky. Aktualizace definitivně skončí během noci v daném regionu.

## <a name="how-are-the-dark-hours-handled-for-customers-that-have-one-finance-and-operations-apps-instance-but-are-active-in-multiple-time-zones"></a>Jak se řeší noční hodiny u zákazníků, kteří mají jednu instanci finančních a provozních aplikací, ale jsou aktivní ve více časových pásmech? 
Neexistují žádné zvláštní plány mimo noční hodiny, kde existuje instance finančních a provozních aplikací, protože plánujeme zavádět aktualizace kvality minimálně rušivým způsobem s [nZDT](../../dev-itpro/deployment/plannedmaintenance-selfservice.md#what-does-near-zero-downtime-maintenance-mean).

## <a name="what-is-the-current-rollout-cadence-for-proactive-quality-updates"></a>Jaký je aktuální plán zavádění proaktivních aktualizací kvality?
Proaktivní aktualizace kvality (PQU) jsou v současné době nasazovány jednou měsíčně pro každou podporovanou verzi aktualizace služby. Pro vybraná prostředí sandbox je nabízena pouze jedna aktualizace za měsíc, pokud zákazníci nepřejdou na novou verzi aktualizace služby. V takovém případě mohou získat předem naplánované PQU jako součást stávajícího tréninku pro aktualizaci nové služby. Po dokončení celosvětového zavedení v roce 2023 se frekvence těchto aktualizací zvýší. Vždy, když dojde ke změně frekvence vydání, budete informováni alespoň jeden měsíc předem.

## <a name="how-will-microsoft-ensure-the-quality-of-these-updates"></a>Jak společnost Microsoft zajistí kvalitu těchto aktualizací?
Společnost Microsoft se snaží udržet kanál vydání dostatečně efektivní, aby poskytoval malé užitečné zatížení a udržoval nízké náklady na ověřování. Každá oprava v aktualizaci kvality prochází přísným a bezpečným procesem nasazení, který pomáhá zlepšit kvalitu a spolehlivost, a tím snížit dopad na zákazníky. Nasazení proběhne nejprve ve fázích v prostředí sandbox, poté bude následovat produkce. Nasazení nanečisto umožňují správné sledování, aby se zjistilo, zda je další nasazení bezpečné. Zavádění zastavíme, pokud budou zjištěny problémy s každou nasazenou skupinou zákazníků, a zajistíme, aby každý krok zavádění měl dostatek času na to, aby se problémy objevily. U každé nadcházející aktualizace kvality poskytneme přehled o plánu prostřednictvím aktualizací veřejné dokumentace a e-mailů, aby zákazníci mohli plánovat dopředu.

## <a name="can-customers-delay-reschedule-or-pause-a-quality-update"></a>Mohou zákazníci odložit, přeplánovat nebo pozastavit aktualizaci kvality?
Ne. Hlavním cílem kvalitních aktualizací je zajistit, aby se pro naše zákazníky neustále zlepšovaly základy, jako je zabezpečení, soukromí, spolehlivost, dostupnost a výkon. Zpožděním nebo pozastavením aktualizace bude ohrožena bezpečnost, dostupnost a spolehlivost.

## <a name="how-do-i-know-what-set-of-changes-went-into-a-quality-update-payload"></a>Jak mohu zjistit, která sada změn šla do datové části aktualizace kvality?
Následující kroky jsou dočasným řešením, protože nadále pracujeme na poskytování lepšího řešení pro identifikaci seznamu změn, které jdou do datové části aktualizace kvality. 

Použijte KB #745340 pro vydání aktualizace kvality 10.0.28 a související verzi aplikace 10.0.1265.89.

1. V LCS otevřete stránku **Podrobnosti prostředí** pro váš sandbox. 
2. V části **Dostupné aktualizace** vyberte možnost **Zobrazit aktualizaci** a uvidíte nejnovější sestavení aktualizace kvality. 
3. Exportujte sestavení do souboru CSV nebo Microsoft Excel.
4. V exportovaném souboru seřaďte informace podle času (nejstarší jako první) a poté vyhledejte číslo KB 745340 ve sloupci **ID aktualizace**. Nyní byste měli vidět rozdílový seznam znalostní báze.
 
 > [!NOTE]
 > Export do souboru CSV nebo Excel musí proběhnout před aktualizací prostředí. V opačném případě můžete použít prostředí s podobnou konfigurací, které nemá nainstalovanou aktualizaci, a postupujte podle výše uvedených kroků.

[![Příklad prostředí s aktualizací kvality.](./media/how-to-get-kb-list-pqu.png)](./media/how-to-get-kb-list-pqu.png)

## <a name="what-is-the-process-if-a-critical-issue-is-found-after-a-quality-update"></a>Jaký je postup, pokud je po aktualizaci kvality nalezen kritický problém?
Kritický problém nebo regrese je jedna nebo více událostí, které obvykle způsobí, že několik zákazníků bude mít zhoršené fungování u jedné nebo více našich služeb. Tyto problémy mohou způsobit neplánované prostoje včetně nedostupnosti, snížení výkonu a narušení správy služeb. Pokud dojde v důsledku takových regresí k širokému dopadu na zákazníky, zastavíme zavádění kvalitní aktualizace, dokud nebudeme moci komunikovat a problém vyřešit. Další aktualizace kvality bude mít obvykle nezbytnou opravu pro obnovení zavádění.

Pokud je ovlivněno prostředí jednoho zákazníka, obraťte se na podporu společnosti Microsoft a otevřete lístek. Na základě odůvodnění zastavíme zavádění aktualizace kvality do všech ostatních prostředí v tomto projektu, dokud nebude problém opraven.

## <a name="can-customers-still-manually-apply-hotfix-updates-from-lcs"></a>Mohou zákazníci stále ručně používat aktualizace oprav hotfix z LCS?
Ano. Aby byla zajištěna trvalá rovnost s tím, jak opravy hotfix fungují, lze aktualizace oprav hotfix stále aplikovat na zákaznická prostředí v LCS. Je však důležité si uvědomit, že opravy hotfix, které jsou nasazeny jako součást aktualizace kvality, procházejí před nasazením aktualizace standardním SDP. Tím se snižuje riziko regresí kvůli vyšší kvalitě. Pro zvýšení spolehlivosti doporučujeme zvolit kvalitní aktualizaci před ručním použitím oprav hotfix.

## <a name="can-customers-proactively-install-a-quality-update-build-ahead-of-the-schedule"></a>Mohou si zákazníci proaktivně sami nainstalovat aktualizaci kvality ještě před plánem?
Ano. Aktualizaci kvality můžete nainstalovat proaktivně. Společnost Microsoft aktualizaci přeskočí, pokud je aktuální verze sestavení prostředí stejná nebo vyšší než příslušná aktualizace kvality.

## <a name="if-an-environment-has-an-upcoming-scheduled-monthly-service-update-within-a-week-will-it-still-receive-quality-updates"></a>Pokud má prostředí nadcházející plánovanou měsíční aktualizaci služby do týdne, dostane přesto aktualizaci kvality?
- Aktualizace kvality se na produkční prostředí nepoužijí, pokud je do týdne od plánovaného provedení aktualizace kvality naplánována nadcházející aktualizace služby.
- Pokud má prostředí sandbox stejnou nebo vyšší verzi sestavení než nadcházející aktualizace kvality, bude přeskočeno.
- Pokud má produkční prostředí stejnou nebo vyšší verzi sestavení než nadcházející aktualizace kvality, bude přeskočeno.
- Pokud má sandbox stejnou nebo vyšší verzi sestavení kvůli aktualizaci kvality nebo ruční aktualizaci produkce, produkce stále získá plánovanou verzi měsíční aktualizace služby. Pokud nechcete, aby se plánované produkční prostředí aktualizovalo na verzi aktualizace služby, můžete aktualizaci služby z LCS pozastavit. 
- Doporučujeme vám použít nejnovější sestavení aktualizace kvality k otestování změn pro nadcházející aktualizaci služby pro lepší stabilitu a výsledky.

## <a name="if-an-environment-has-an-upcoming-scheduled-action-and-a-scheduled-quality-update-in-the-same-maintenance-window-will-it-still-receive-the-quality-update"></a>Pokud má prostředí nadcházející naplánovanou akci a plánovanou aktualizaci kvality ve stejném okně údržby, bude stále dostávat aktualizaci kvality?
Pokud dojde k nějakému sporu s předem naplánovanou akcí, například PITR (Obnovení k určitému bodu v čase), aktualizace kvality bude přeplánována na další dostupné okno údržby během čtyřdenního okna. Další informace o plánu viz článek [Jaký je plán proaktivních aktualizací kvality?](#schedule). 

## <a name="can-an-environment-be-brought-back-to-its-previous-state-if-there-are-issues-after-a-quality-update-is-applied"></a>Lze prostředí vrátit do předchozího stavu, pokud se po použití aktualizace kvality vyskytnou problémy?
Po použití aktualizace kvality nedochází za žádných okolností k žádnému vrácení. Pro řešení problémů jsou k dispozici pouze možnosti předávání oprav.

## <a name="what-about-fda-regulation-and-gpx"></a>A co regulace FDA a GPX?
Plán pro zákazníky podléhající validaci a regulaci FDA se stále vyvíjí. Brzy očekávejte další aktualizace v tomto prostoru. Prozatím jsou všichni tito zákazníci vyjmuti z aktualizací kvality. Chcete-li zajistit, aby se zákazník musel řídit předpisy FDA, navštivte [Nabídku GPX Microsoft Azure](/azure/compliance/offerings/offering-gxp).

## <a name="what-versions-of-service-updates-are-supported-for-these-quality-updates"></a>Jaké verze aktualizací služeb jsou podporovány pro tyto aktualizace kvality?
Zákazníci se všemi podporovanými verzemi aktualizací služeb mají nárok na aktualizace kvality. 

## <a name="finance-and-operations-apps-deployments-with-retail-components-typically-require-additional-work-in-addition-to-having-to-redeploy-mpos-how-will-these-quality-updates-impact-the-retailsdk"></a>Nasazení finančních a provozních aplikací s maloobchodními komponentami obvykle vyžadují další práci kromě nutnosti znovu nasadit MPOS. Jak tyto aktualizace kvality ovlivní RetailSDK? 
Vzhledem k tomu, že povaha samotné opravy hotfix se nemění v datové části aktualizací kvality, neočekáváme žádný další dopad konkrétně související s maloobchodními komponentami.

## <a name="is-there-any-impact-to-cloud-hosted-environments-che"></a>Má to nějaký dopad na prostředí hostovaná v cloudu (CHE)? 
Prostředí CHE jsou mimo rozsah aktualizací kvality, protože jsou mimo působnost společnosti Microsoft

## <a name="are-there-any-integration-issues-with-microsoft-dataverse"></a>Existují nějaké problémy s integrací s Microsoft Dataverse? 
Nejsou známy žádné problémy integrace aktualizací kvality s Dataverse.

