---
title: Proaktivní aktualizace kvality
description: Tento článek poskytuje informace o proaktivním doručování aktualizací kvality.
author: rashmansur
ms.date: 08/23/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: rashmim
ms.search.validFrom: 2022-08-19
ms.search.form: ''
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 9d81cb15e9a127e7bea7ad9b5e0f50a1ee543f71
ms.sourcegitcommit: 78e85ad49634cd31459fdb7325cb273352bf1501
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/23/2022
ms.locfileid: "9338129"
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
- **Záložní verze** – Pro seskupení všech změn v proaktivní aktualizaci kvality bude použito testování. Je-li po proaktivním nasazení vyžadována záloha, lze ji provést prostřednictvím systému testování.
- **Označení synchronizace sandboxu** – Méně než 20 procent zákazníků má dnes více sandboxů a jeden sandbox si ponechává nasazený tam, kde se verze shoduje s produkčním řešením, aby pomohli s řešením problémů. V blízké budoucnosti zavedeme možnost pro zákazníky specifikovat sandboxové prostředí, které by nemělo dostávat nasazení proaktivní aktualizace kvality spolu s jinými sandboxy, ale místo toho by je mělo obdržet později spolu s produkčním prostředím. Všimněte si, že pokud zákazník používá sandbox k testování novější verze, než je jeho produkční verze, bude tento sandbox dostávat aktualizace kvality na novější verzi.
- 
## <a name="when-will-proactive-quality-updates-start"></a>Kdy začnou proaktivní aktualizace kvality?

Očekává se, že distribuce proaktivních aktualizací kvality pro prostředí sandbox začne pro zákazníky veřejného cloudu Azure koncem září nebo října 2022. Zkušební prostředí také začnou dostávat proaktivní nasazení aktualizací v té době. V září bude každému zákazníkovi zasláno upozornění, které ho informuje o očekávaném plánu pro jeho prostředí. Výjimky z proaktivního aktualizovaného distribučního procesu budou povoleny pouze pro zákazníky regulované FDA. Stále pracujeme na tom, jak budou spravována regulovaná prostředí a suverénní a vládní cloudoví zákazníci.

Během příštích šesti měsíců budeme postupně zvyšovat procento sandboxových prostředí, která obdrží proaktivní aktualizace, dokud nebudou zahrnuta všechna určená prostředí a postoupíme k aktualizaci produkčních prostředí. Během tohoto období budeme monitorovat, abychom zajistili, že proces nasazení bude bezproblémový a že dosáhneme cíle nerušivého užitečného zatížení.

Protože zákazníci budou pravidelně dostávat menší užitečné zatížení, očekáváme, že se proces udržování aktuálního stavu zjednoduší. Frekvenci zavádění aktualizací upravíme, jakmile prokážeme schopnost spustit proces bez přerušení. Tento proces již efektivně funguje na naší platformě a aplikacích Dataverse a přináší očekávaná zlepšení kvality služeb. Těšíme se, že uděláme stejný krok vpřed pro finanční a provozní aplikace.
