---
title: Popis služby pro finanční a provozní aplikace
description: Toto téma poskytuje popis služby pro finanční a provozní aplikace.
author: tomhig
ms.date: 04/27/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: whigginb
ms.search.validFrom: 2021-09-03
ms.openlocfilehash: 26b2821f33ea23dde1fda1d461baa5de1b4f9efc
ms.sourcegitcommit: d70f66a98eff0a2836e3033351b482466bd9c290
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/11/2022
ms.locfileid: "8740645"
---
# <a name="service-description-for-finance-and-operations-apps"></a>Popis služby pro finanční a provozní aplikace

[!include[banner](../includes/banner.md)]

Finanční a provozní aplikace jsou nabídky softwaru jako služby (SaaS) pro plánování podnikových zdrojů (ERP), které jsou postaveny na a pro [Microsoft Azure](https://azure.microsoft.com/overview/what-is-azure/). Služba Finance and Operations poskytuje organizacím funkce ERP, které podporují jejich jedinečné požadavky a pomáhají jim přizpůsobit se neustále se měnícím podnikatelským prostředím, aniž by museli spravovat infrastrukturu. Finanční a provozní aplikace mohou zahrnovat jednu nebo více z následujících oblastí řešení:

- [Dynamics 365 Finance](/dynamics365/finance/)
- [Dynamics 365 Human Resources](/dynamics365/human-resources/)
- [Dynamics 365 Supply Chain Management](/dynamics365/supply-chain/)
- [Dynamics 365 Commerce](/dynamics365/commerce/)
- [Dynamics 365 Project Operations](/dynamics365/project-operations/)

Společně s [business intelligence](/power-bi/fundamentals/power-bi-service-overview), [infrastrukturou](https://azure.microsoft.com/global-infrastructure/), [výpočtem](/azure/service-fabric/service-fabric-overview), a [databázovými službami](https://devblogs.microsoft.com/azure-sql/running-1m-databases-on-azure-sql-for-a-large-saas-provider-microsoft-dynamics-365-and-power-platform/) tyto aplikace umožňují organizacím spouštět podnikové procesy specifické pro dané odvětví a provozovat je. Zákazníci s podporou svého implementačního partnera určují konfiguraci logiky podnikových aplikací, která nejlépe vyhovuje jejich jedinečným obchodním procesům. Funkčnost a obchodní procesy lze zvětšit nebo rozšířit pomocí jednoho nebo kombinace následujících řešení:

- Integrovaná [personalizační zkušenost](personalize-user-experience.md)
- Nástroje [Microsoft Power Platform](../../dev-itpro/power-platform/overview.md)
- [Sada SDK pro vývoj softwaru pro finanční a provozní aplikace](../../dev-itpro/dev-tools/developer-home-page.md) a [automatizace buildu Azure DevOps](../../dev-itpro/dev-tools/developer-home-page.md#build-automation-using-azure) založená na [Visual Studio](https://visualstudio.microsoft.com)
- Řešení od nezávislého dodavatele softwaru (ISV) od [AppSource](https://appsource.microsoft.com/partners)

Na základě požadavků si zákazníci zvolí svůj přístup k řešení. Spolupracují se svým implementačním partnerem na definování, vývoji a testování svého řešení pomocí nástrojů a osvědčených postupů, které jsou součástí [Microsoft Dynamics Lifecycle Services (LCS)](../../dev-itpro/lifecycle-services/lcs.md). Existují čtyři běžné scénáře:

- Standardní konfigurace finančních a provozních operací "po vybalení z krabice" (bez rozšíření)
- Konfigurace finančních a provozních aplikací, která zahrnuje jedno nebo více řešení ISV
- Konfigurace finančních a provozních aplikací, která zahrnuje jedno nebo více rozšíření specifická pro zákazníka
- Konfigurace finančních a provozních aplikací, která zahrnuje kombinaci rozšíření specifických pro zákazníka a jedno nebo více řešení ISV

Organizace se mohou přizpůsobit růstu svého podnikání jednoduchým přidáváním uživatelů a obchodních procesů prostřednictvím jednoduchého a transparentního modelu předplatného. Další informace získáte části [Průvodce licencováním Dynamics 365](https://www.microsoft.com/licensing/docs/view/Microsoft-Dynamics-365).

## <a name="operating-model"></a>Provozní model

Provozní model finančních a provozních aplikací definuje konkrétní role a odpovědnosti pro zákazníka, implementačního partnera a Microsoft během celého životního cyklu služby. Další informace získáte v tématu [Cloudové operace a servis](../../dev-itpro/lifecycle-services/cloud-operations-servicing.md).

### <a name="customer-activities"></a>Aktivity zákazníka

Zákazníci pracují se svým partnerem a [Microsoft FastTrack](/dynamics365/fasttrack/) podle [Průvodce implementací Dynamics 365](https://community.dynamics.com/365/dynamics-365-fasttrack/p/dynamics365implementationguide), rámce [Success by Design](/dynamics365/fasttrack/success-by-design-overview) a nástrojů a šablon osvědčených postupů uvedených v [Lifecycle Services](../../dev-itpro/lifecycle-services/lcs.md) na implementaci jejich řešení. Mezi běžné činnosti patří:

- Správa identity a zabezpečení uživatele
- Definice, vývoj a provoz obchodních procesů
- Definice, vývoj, testování a provoz rozšíření
- Sledování a správa jiných než výrobních nasazení
- Spravujte aktualizace aplikací a ověřujte rozšíření
- Spravujte řešení ISV a integrace třetích stran

### <a name="microsoft-responsibilities"></a>Odpovědnost společnosti Microsoft

Microsoft spravuje službu Finance and Operations a provozních aplikací nasazením, aktivním monitorováním a servisem zákaznických sandboxů a provozních prostředí v rámci předplatného Microsoft SaaS. Tato správa zahrnuje přidělení požadované systémové infrastruktury pro spuštění služby a proaktivní komunikaci se zákazníky o stavu služby. Mezi odpovědnosti patří:

**Správa infrastruktury**
- Zabezpečení a izolace
- Operační systémy a virtualizace
- Servery, úložiště a sítě
- Napájení datového centra, sítě, chlazení

**Správa aplikační platformy**
- Nepřetržité sledování a upozornění na aplikace
- Diagnostika, aktualizace platformy, opravy, aktualizace služeb
- Směrování aplikací, vyvažování zátěže, replikace webu
- Zřizování a správa prostředí
- Správa databáze, vysoká dostupnost (HA)/zotavení po havárii (DR), rozsah, operace
- Výpočet nasazení, vertikálně navýšit kapacitu, vertikálně snížit kapacitu

## <a name="system-configuration"></a>Konfigurace systému

Finanční a provozní aplikace se škálují podle objemu transakcí a zatížení uživatele. Každá implementace zákazníka vytváří jedinečné řešení, které se skládá z následujících prvků:

- **Složení dat** - Jedinečná sada parametrů, které řídí chování, rozložení organizace, strukturu kmenových dat (například finanční a inventární dimenze) a granularitu sledování transakcí.
- **Rozšíření a konfigurace** - Mechanismy rozšíření využívající rozšíření kódu, řešení ISV a jedinečné konfigurace, které zahrnují pracovní toky, integrace a konfigurace sestav.
- **Vzory použití** - Jedinečná kombinace online a dávkového využití spolu se schopností integrace s upstreamovými a downstreamovými systémy pro jednotný tok dat a schopností rozlišovat na základě informací, které zákazníci používají ve svých obchodních procesech.

Microsoft konfiguruje zákaznická provozní prostředí, která jsou dimenzována tak, aby zvládala objemy transakcí a souběžnost uživatelů. Společnost Microsoft odpovídá za následující úkoly:

- Správné přidělování zdrojů provozních prostředí na základě informací o profilování zákazníka v souboru [Nástroj pro odhad předplatného LCS](../../dev-itpro/lifecycle-services/subscription-estimator.md)
- Průběžné monitorování a diagnostika dostupnosti služeb provozních prostředí
- Analýza a řešení problémů s výkonem systému pomocí finančních a provozních aplikací

Aby bylo zajištěno, že je implementace konfigurována pro vysoký výkon, musí zákazníci splnit tyto úkoly:

- Poskytněte přesné informace o používání implementace finančních a provozních aplikací v [nástroji pro odhad předplatného LCS](../../dev-itpro/lifecycle-services/subscription-estimator.md).
- Vytvářejte a testujte rozšíření pro výkon a škálování.
- Vhodně otestujte výkonnost konfigurací dat.
- Zajistěte škálovatelnost provedením [testování výkonu](https://community.dynamics.com/365/b/techtalks/posts/performance-testing-approach-april-30-2018) před spuštěním.

## <a name="onboarding-and-implementation"></a>Onboarding a implementace

Následující tabulka ukazuje typické události při připojování a implementaci.

| Žádost | Očekávaná akce Microsoftu | Očekávaná akce zákazníka/implementačního partnera |
|---|---|---|
| Počáteční nákup nabídky | Projekt LCS je vytvořen po zakoupení nabídky na základě události, kterou spustí zákazník. | Projděte si smlouvu Enterprise (EA) nebo smlouvu s poskytovatelem cloudového řešení (CSP) [obchodní proces](before-you-buy.md). Partner vytvoří pro zákazníka klienta, je-li to relevantní. |
| Doplňkový nákup | Udělte zákazníkovi přístup k doplňku, který byl vybrán během implementace. | Nelze použít |
| Plánování a analýza implementace | Poskytněte v LCS relevantní nástroje, jako například [Modelování podnikových procesů (BPM)](../../dev-itpro/lifecycle-services/bpm-overview.md) a [interoperabilita s Azure DevOps](../../dev-itpro/lifecycle-services/synchronize-bpm-vsts.md). | Proveďte plánování projektu, nastavte Azure DevOps, dokončete zprovoznění systému a nastavte účty správce. |

Další informace viz [Zprovoznění implementačního projektu](../imp-lifecycle/onboard.md).

## <a name="globalization"></a>Globalizace

finanční a provozní aplikace jsou obsluhovány z několika oblastí Azure po celém světě. finanční a provozní aplikace poskytují funkce pro podporu různých zemí/oblastí a rodných jazyků. Další informace viz [Lokalizační a regulační funkce](../../dev-itpro/lcs-solutions/country-region.md#localization-and-regulatory-features).

### <a name="countryregion-specific-considerations"></a>Aspekty nápovědy specifické pro zemi nebo oblast

- Zákazníci v regulovaném odvětví nebo obchodních organizacích, které obchodují se subjekty ve Francii, které vyžadují místní datovou rezidenci, by si měli projít téma [finanční a provozní aplikace ve Francii](../../dev-itpro/deployment/france-local-deployment.md).
- Zákazníci, kteří působí v Číně, by si měli projít téma [Playbook Azure pro Čínu](/azure/china/) a [finanční a provozní aplikace provozované společností 21Vianet v Číně](../../dev-itpro/deployment/china-local-deployment.md).
- Zákazníci, kteří mají provozy v Rusku, by si to měli projít [ruský zákon o lokalizaci osobních údajů](/business-applications-release-notes/october18/dynamics365-finance-operations/russian-regulations-on-prem#when-will-the-cloud-deployment-option-of-dynamics-365-for-finance-and-operations-be-generally-available-for-russia).

### <a name="general-data-protection-regulation-gdpr"></a>Obecné nařízení o ochraně osobních údajů (GDPR)

U finančních a provozních aplikací vystupuje společnost Microsoft jako zpracovatel. Jako zpracovatel údajů poskytují Finance a provoz procesy a funkce, které zákazníkům pomáhají plnit povinnosti GDPR jako správce údajů. Další informace naleznete v tématu [přehled GDPR](../../dev-itpro/gdpr/gdpr-guide.md).

## <a name="environment-and-data-management"></a>Prostředí a správa dat

Tato část popisuje některé typické události prostředí a správy dat, ke kterým dochází ve službě.

### <a name="environment-and-data-management-events-for-production-instances"></a>Události správy prostředí a dat pro provozní instance

LCS poskytuje [samoobslužné nástroje](../../dev-itpro/deployment/infrastructure-stack.md) a [operace přesunu v databázi](../../dev-itpro/database/dbmovement-operations.md) které se používají k provádění úkolů správy prostředí a dat. Několik příkladů:

**Událost:** [Žádost o provozní instanci](../imp-lifecycle/prepare-go-live.md#requesting-the-production-environment)

- Dokončete [Kontrolní seznam uvedení do provozu](../imp-lifecycle/prepare-go-live.md) a odešlete jej týmu [Microsoft FastTrack](/dynamics365/fasttrack/).
- Dokončete [odhadce předplatného LCS](../../dev-itpro/lifecycle-services/subscription-estimator.md) před vyžádáním provozní instance.
- Dokončete všechny implementační úkoly, které jsou uvedeny v [metodologii LCS](../../dev-itpro/lifecycle-services/create-methodology.md).

**Událost:** [Kopírování sandboxové databáze do provozní instance](../../dev-itpro/database/dbmovement-scenario-goldenconfig.md)

- Provádí se pro napodobení uvedení do provozu nebo skutečné uvedení do provozu.

**Událost:** [Režim údržby](../../dev-itpro/sysadmin/maintenance-mode.md)

1. Zapněte režim údržby v LCS.
2. Dokončete požadovanou údržbu.
3. Vypněte Režim údržby v LCS.

### <a name="environment-and-data-management-events-for-non-production-instances"></a>Události správy prostředí a dat pro neprovozní instance

LCS poskytuje [samoobslužné zřizování](../../dev-itpro/deployment/infrastructure-stack.md) a [operace přesunu v databázi](../../dev-itpro/database/dbmovement-operations.md) které se používají k provádění úkolů správy prostředí a dat. Několik příkladů:

**Událost:** [Nasazení nové sandboxové instance](../../dev-itpro/deployment/deployenvironment-newinfrastructure.md)

- Ujistěte se, že byly [naplánovány všechny požadované instance](../imp-lifecycle/environment-planning.md) a že byly zakoupeny příslušné nabídky doplňků.
- Spusťte proces nasazení v LCS.
- Dokončete všechny úkoly, které jsou uvedeny v kontrolních seznamech LCS.
    
>[!NOTE]
>Vývojové sandboxové prostředí je virtuální počítač (VM), který je [nasazen do předplatného Azure zákazníka](../../dev-itpro/dev-tools/access-instances.md) a spravované zákazníkem.

**Událost:** [Kopírování zlaté konfigurační databáze ze sandboxu do provozu](../../dev-itpro/database/dbmovement-scenario-goldenconfig.md)

- Provádí se pro napodobení uvedení do provozu nebo skutečné uvedení do provozu.

**Událost:** [Obnovení zálohy provozního bodu v čase na neprovozní instanci](../../dev-itpro/database/database-pitr-prod-sandbox.md)

- Spusťte možnost [Obnovit databázi](../../dev-itpro/database/database-refresh.md) v LCS.
- Následné kopírování: Odstraňte nebo zamlžte citlivé údaje pomocí skriptů, upravte konfigurace aplikací specifických pro prostředí (například koncové body integrace) a povolte nebo přidejte uživatele. Tyto změny se provádějí použitím [balíčku dat](../../dev-itpro/data-entities/data-entities-data-packages.md#import-a-data-package).

**Událost:** [Obnovení bodu v čase databázového bodu nevýrobní instance](../../dev-itpro/database/database-point-in-time-restore.md)

- Přijměte, že proces nelze vrátit zpět.
- Spusťte operaci obnovení v daném čase v LCS.

**Událost:** Kopírování sandboxové databáze úrovně 2 do vývojového sandboxu pro řešení potíží a [ladění](../../dev-itpro/database/dbmovement-scenario-debugdiag.md)

- Spusťte operaci exportu databáze v LCS v sandboxovém prostředí vrstvy 2.
- Importujte a aktualizujte databázi ve vývojovém prostředí.

## <a name="data-backup-and-retention"></a>Zálohování a uchovávání dat

Databáze pro prostředí financí a provozů v předplatném SaaS jsou chráněny automatickými zálohami. Pro provozní prostředí jsou automatické zálohy uchovávány po dobu 28 dnů, pokud společnost Microsoft neprovede vrácení zpět. U sandboxového prostředí (úroveň 2+) jsou uchovávány po dobu sedmi dnů. Vrácení provozního prostředí zpět lze provést, pokud během jakékoli plánované aktualizace údržby dojde k chybě.

Další informace o automatickém zálohování viz [Automatizované zálohování - Azure SQL Database a spravovaná instance SQL](/azure/azure-sql/database/automated-backups-overview?tabs=single-database).

## <a name="service-activity-responsibilities"></a>Zodpovědnosti aktivity služeb

Následující tabulka popisuje některé typické scénáře a aktivity pro službu. Udává také, zda společnost Microsoft, zákazník nebo společnost Microsoft i zákazník jsou za aktivity odpovědní.

| Aktivita | Odpovědnost společnosti Microsoft | Zodpovědnost zákazníka |
|---|---|---|
| **Zřizování počátečních klientů** | | |
| Upravte velikost předpokládaného zatížení v LCS pomocí nástroje pro odhad předplatného a požádejte o zřízení konkrétních prostředí. | | X |
| Zřiďte všechny provozní a neprovozní instance. | X | |
| Ověřte nasazené provozní a neprovozní instance. | | X |
| **Aktualizace služby** | |
| Aplikujte aktualizace služeb na určené neprovozní a provozní instance. | X | |
| Ručně aplikujte aktualizace služeb z LCS na instance sandboxu. Definujte, vyvíjejte, testujte aktualizaci a poskytněte balíček aktualizace kódu zpět do LCS. | | X |
| Požádejte, aby byly aktualizace rozšíření aplikovány na provozní instanci, a naplánujte jejich aplikaci. | | X |
| Před použitím aktualizací vytvořte zálohu kódu a dat pro provozní instanci. | X | |
| V případě jakéhokoli selhání vraťte provozní instanci zpět do zálohy kódu a dat. | X | |
| **Správa dat (zálohování, obnovení a aktualizace)** | | |
| Zálohujte databázi. | X | |
| Určete vysokou dostupnost a plán zotavení po havárii. | X | |
| Monitorujte výkon provozní instanční databáze. | X | |
| Vylaďte výkon provozní instanční databáze. | X | |
| Proveďte aktualizaci databáze produkčních instancí k určitému bodu v čase do neproduktivní instance. | | X |
| **Aktualizace infrastruktury** | | |
| Naplánujte pravidelné aktualizace infrastruktury. | X | |
| **Škálování nahoru a dolů (uživatelé, úložiště a instance)** | | |
| Zakupte další doplňky pro uživatele a neprovozní doplňky. | | X |
| Aktualizujte změny využití v nástroji LCS Subscription Estimator. | | X |
| Nahlaste všechny závažné problémy s výkonem, které ovlivňují používání služby. | | X |
| Proaktivně spravujte prostředky, které jsou pro příslušnou službu vyžadovány. | X | |
| Vyšetřujte a řešte incidenty. | X | |
| **Zabezpečení (přístup uživatele)** | | |
| Poskytněte uživateli přístup ke službě. | | X |
| Zajistěte přístup k projektu LCS pro správu a provoz instancí, které byly nasazeny prostřednictvím LCS. | | X |
| **Monitorování provozních instancí** | | |
| provozní instance sledujte nepřetržitě. | X | |
| Proaktivně upozorněte zákazníka na incidenty, které se týkají provozní instance. | X | |
| **Správa a monitorování neprovozních instancí** | | |
| Spravujte neprovozní instance pomocí LCS. | | X |
| Monitorujte neprovozní instance. | | X |

## <a name="service-update-strategy"></a>Strategie aktualizace služby

V souladu se [zásadami životního cyklu softwaru](../../dev-itpro/migration-upgrade/versions-update-policy.md) následují finanční a provozní aplikace [zásady moderního životního cyklu společnosti Microsoft](../../dev-itpro/migration-upgrade/versions-update-policy.md#modern-lifecycle-policy), které zahrnují produkty, které jsou průběžně servisovány a podporovány. 

Společnost Microsoft vydává osm aktualizací služeb finančních a provozních aplikací každý rok v následujících měsících:

- Leden
- Únor
- Duben
- Květen
- Červenec
- Srpen
- Říjen
- Listopad

>[!NOTE]
>Duben a říjen jsou hlavní vlny vydání funkcí. Zákazníci mohou pozastavit aktualizaci jednotlivých služeb až na tři po sobě jdoucí aktualizační cykly.

Další informace naleznete v následujících tématech:

- [Přehled aktualizace služby One Version](../../dev-itpro/lifecycle-services/oneversion-overview.md)
- [Konfigurace aktualizací služby prostřednictvím LCS](../../dev-itpro/lifecycle-services/configure-service-updates.md)
- [Pozastavení aktualizací služby prostřednictvím LCS](../../dev-itpro/lifecycle-services/pause-service-updates.md)
- [Informujte se o aktualizacích služeb prostřednictvím LCS](../../dev-itpro/lifecycle-services/notifications-service-updates.md)
- [Nástroje pro regresní testování k ověření aktualizací služeb](../../dev-itpro/perf-test/rsat/rsat-overview.md)
- [Plán a uvolnění aplikace Dynamics 365](https://dynamics.microsoft.com/roadmap/overview/)

## <a name="security-and-administrative-access"></a>Zabezpečení a přístup pro správu

Přístup pro správu k provoznímu prostředí finančních a provozních aplikací je přísně kontrolován a protokolován. Údaje o zákaznících jsou zpracovávány v souladu s [Online podmínkami služeb společnosti Microsoft](https://www.microsoft.com/licensing/terms/productoffering). 

### <a name="customer-administrative-access"></a>Přístup pro správu zákazníků

Správce klienta zákazníka má přístup k provozním nebo neprovozním instancím, jak je popsáno v následující tabulce:

| Typ prostředí | Účel | Úroveň přístupu zákazníka |
|---|---|---|
| **Neprovozní**<br>Sandboxové prostředí 1. úrovně | Neprovozní prostředí, které zákazníci nasazují pro účely vývoje, ukázek nebo školení. | Sandbox 1. úrovně (označovaný také jako cloudové prostředí) je virtuální počítač spravovaný zákazníkem, který je nasazen do předplatného Azure zákazníka od LCS. Protože se jedná o virtuální počítač v zákazníkově předplatném Azure, má zákazník plný přístup pro správce k prostředí prostřednictvím vzdálené plochy. |
| **Neprovozní**<br>Sandbox 2. úrovně (nebo vyšší) | Neprovozní prostředí, které zákazníci nasazují pro testování přijatelnosti uživatelem, integrační testování, školení, fázování nebo jakýkoli jiný scénář před provozem. | Sandboxy úrovně 2 a vyšší jsou nasazeny v předplatném SaaS Finance a provoz. Přístup k databázím Azure SQL database, které jsou přidruženy k neprovoznímu prostředí, je udělován prostřednictvím [přístupu za běhu](../../dev-itpro/database/database-just-in-time-jit-access.md). Přístup ke vzdálené ploše není k dispozici. |
| **Výrobní** | Provozní prostředí je nasazeno, když je projekt [připraven k počátečnímu spuštění](../imp-lifecycle/environment-planning.md#production-system-readiness). | Do předplatného SaaS jsou nasazena provozní prostředí. Veškerý přístup je prostřednictvím prohlížeče, koncových bodů služby nebo LCS. |

### <a name="microsoft-administrative-access"></a>Přístup pro správu společnosti Microsoft

Následující tabulka ukazuje různé úrovně přístupu pro různé správce Microsoft:

| Správce | Data zákazníka |
|---|---|
| Operační tým pro odpovědi<br>(Pouze pro klíčový personál) | Přístup je poskytován prostřednictvím lístku podpory. Přístup je auditován a omezen na dobu trvání činnosti podpory. |
| Služby zákaznické podpory společnosti Microsoft (CSS) | Žádný přímý přístup. Zákazník může pomocí sdílení obrazovky spolupracovat s pracovníky podpory při ladění problémů. |
| Technický | Žádný přímý přístup. Tým odpovědí pro operace může pomocí sdílení obrazovky pracovat s techniky při ladění problémů. |
| Ostatní v Microsoftu | Bez přístupu. |

## <a name="monitoring"></a>Monitorování

Společnost Microsoft investovala do rozsáhlé sady nástrojů pro sledování a diagnostiku provozních instancí zákazníků. Microsoft monitoruje provozní prostředí zákazníků 24 hodin denně, 7 dní v týdnu. Další informace viz [Podpora a monitorování provozu](../imp-lifecycle/production-support-monitoring.md).

| Odpovědnost společnosti Microsoft | Povinnosti zákazníka |
|---|---|
| <ul><li>Sledujte dostupnost služby.</li><li>Průběžně sledujte a upozorňujte pomocí metrik stavu a hlídacích psů na kritické součásti, jako jsou Application Object Server (AOS), Batch, Data Import/Export Framework (DIXF), Commerce a Management Reporter.</li><li>Monitorujte snížení výkonu, které je způsobeno službami infrastruktury (jako např. Azure Active Directory \[Azure AD\] a Azure SQL).</li><li>Pokud společnost Microsoft zjistí, že jeden proces nebo dávková úloha způsobuje aberace, bude tento proces nebo úloha po komunikaci se zákazníkem ukončena.</li></ul> | <ul><li>Monitorujte změny konfigurací a rozšíření aplikací, které mohou způsobit problémy s funkčností a výkonem.</li><li>Chyby aplikace je třeba diagnostikovat pomocí monitorovacích nástrojů. Pomocí těchto nástrojů můžete diagnostikovat aberace výkonu hlášené uživateli.</li><li>Informujte společnost Microsoft, pokud je očekávané zatížení systému nad rámec předpokládaného vrcholového využití.</li><li>Pokud příslušná služba není v provozní instanci k dispozici, může zákazník použít LCS k nahlášení [výpadku výroby](../../dev-itpro/lifecycle-services/report-production-outage.md).</li></ul> |

Odesláním žádostí o podporu online prostřednictvím LCS zákazníci umožní společnosti Microsoft poskytovat rychlé a hluboké technické znalosti nejefektivnějším a nejúčinnějším způsobem. Přestože je k dispozici možnost telefonu, měla by být použita pouze v případě, že možnost online není k dispozici. Další informace naleznete v tématu [Možnosti telefonické podpory](/power-platform/admin/support-overview?toc=%2Fdynamics365%2Ffin-ops-core%2Fdev-itpro%2Ftoc.json&bc=%2Fdynamics365%2Fbreadcrumb%2Ftoc.json#is-there-a-phone-number-i-can-call-to-contact-support).

## <a name="incident-management"></a>Správa incidentů

Společnost Microsoft reaguje na incidenty na základě úrovní závažnosti a řeší je. Úrovně závažnosti incidentů společnosti Microsoft lze změnit během počátečního hodnocení incidentu a podle toho, jak budou k dispozici další informace o dopadu a rozsahu. Pokud je incident zmírněn, jeho závažnost zůstane nezměněna.

Další informace o úrovních závažnosti viz [tato tabulka závažnosti](/power-platform/admin/support-overview#what-is-initial-response-time-and-how-quickly-can-i-expect-to-hear-back-from-someone-after-submitting-my-support-request).

## <a name="business-continuity-through-high-availability-and-disaster-recovery"></a>Provozní kontinuita díky vysoké dostupnosti a zotavení po havárii 

Microsoft poskytuje provozní kontinuitu a zotavení po havárii pro provozní instance finanční a provozní aplikace v případě výpadků celé oblasti Azure. Další informace, včetně cíle doby obnovení služby (RTO) a cíle bodu obnovení (RPO), viz [Kontinuita podnikání a obnova po havárii](../../dev-itpro/sysadmin/business-continuity-disaster-recovery.md).

- **Vysoká dostupnost** - Funkce HA poskytuje způsoby, jak zabránit prostojům způsobeným selháním jednoho uzlu v datovém centru Azure. Cloudová architektura každé služby používá sady dostupnosti Azure pro výpočetní vrstvu k zabránění událostem s jedním bodem selhání. HA pro databáze je poskytována prostřednictvím [funkcí Azure SQL HA](/azure/azure-sql/database/high-availability-sla).
- **Zotavení po havárii** - [Funkce zotavení po havárii Azure](/azure/best-practices-availability-paired-regions) chrání každou službu před výpadky, které obecně ovlivňují celé datové centrum Azure. Zde je několik takových funkcí:

    - Replikace Azure SQL active-geo pro primární databázi (obchodní databáze).
    - Geo-redundantní kopie Azure Blob Storage (která obsahuje přílohy dokumentů) v jiných oblastech Azure.
    - Sekundární oblast pro replikace Azure SQL a Azure Blob Storage.

Pokud se k obnovení provozní instance zákazníka použije zotavení po havárii, Microsoft a zákazník tím splní své zodpovědnosti v oblasti [řízení incidentů](service-description.md#incident-management) odpovědnosti.

Plány a postupy zotavení po havárii společnosti Microsoft jsou pravidelně prověřovány pomocí auditů systému a řízení organizace (SOC). Tyto audity souladu potvrzují technický a procedurální proces DR společnosti Microsoft, včetně aplikace Dynamics 365 Finance a provoz. [Soulad se SOC](/compliance/regulatory/offering-soc-2) zprávy o auditu a všechny ostatní zprávy o shodě jsou k dispozici v [nabídkách pro dodržování předpisů Microsoft Trust Center](/compliance/regulatory/offering-home).

## <a name="finance-and-operations-support-offerings"></a>Podpora pro finanční a provozní aplikace

Technická podpora je k dispozici na trzích, kde jsou nabízeny finanční a provozní služby. [Zkušenosti s podporou](../../dev-itpro/lifecycle-services/lcs-support.md) jsou poskytovány v LCS nebo finančních a provozních aplikacích. Několik příkladů:

- [Hledání problémů](../../dev-itpro/lifecycle-services/issue-search-lcs.md) v LCS
- [Integrovaná technická podpora](../../dev-itpro/lifecycle-services/support-experience.md) ve finančních a provozních aplikacích
- [Podpora díky cloudu](../../dev-itpro/lifecycle-services/cloud-powered-support-lcs.md) v LCS

Microsoft nabízí zákazníkům finančních a provozních aplikací tři plány podpory: Premier, Professional Direct a podpora, která je součástí předplatného. Úroveň podpory se liší podle plánu. Následující tabulka ukazuje srovnání tří plánů.

| Funkce podpory | Premier | Professional Direct | Předplatné |
|---|---|---|---|
| Neomezené odesílání incidentů přestávky/opravy | Ano | Ano | Ano |
| Nepřetržitý přístup přes LCS | Ano | Ano | Ano |
| Doba odezvy na incident | Méně než jednu hodinu | Méně než jednu hodinu | Následující pracovní den |
| Konzultační hodiny | Fondy se získávají na základě dohody. | Ne | Ne |
| Specializovaný správce účtu podpory | Ano | Ne | Ne |
| Specializovaný technik podpory | Zapojeno na základě samostatné dohody | Ne | Ne |

Další informace naleznete v [Přehled podpory](/power-platform/admin/support-overview).

### <a name="process-to-engage-support"></a>Proces zapojení podpory

V případě incidentů, které zahrnují finanční a provozní aplikace, zákazníci odesílají lístky na podporu společnosti Microsoft prostřednictvím LCS. CSS řeší incidenty na základě plánu podpory zákazníka a závažnosti incidentu, jak určil CSS.

### <a name="service-level-agreement"></a>Smlouva úrovně služeb

Společnost Microsoft se zavázala k míře dostupnosti služby 99,9 procent za měsíc. Pokud společnost Microsoft nedosáhne a neudrží úroveň služby pro příslušnou službu, jak je popsáno ve smlouvě o úrovni služeb (SLA), může mít zákazník nárok na kredit ve výši části měsíčních poplatků za tuto službu. Informace o tom, jak zahájit kredit služby, najdete v části „Nároky“ [SLA](https://www.microsoft.com/licensing/docs/view/Service-Level-Agreements-SLA-for-Online-Services).

## <a name="important-resources"></a>Důležité zdroje

- **[Centrum důvěry](https://www.microsoft.com/trust-center)** - Získejte informace o tom, kde jsou uložena finanční a provozní data a další informace o ochraně osobních údajů, dodržování předpisů a bezpečnostních postupech.
- **[Licenční podmínky a dokumentace](https://www.microsoftvolumelicensing.com/)** - Rychlý přístup k licenčním podmínkám a doplňkovým informacím, které jsou relevantní pro používání produktů a služeb, které jsou licencovány prostřednictvím multilicenčních programů společnosti Microsoft.
- **[Licenční podmínky](https://www.microsoft.com/licensing/product-licensing/)** - Prostředky na této stránce definují podmínky pro produkty softwaru a online služeb, které zakoupíte prostřednictvím komerčních licenčních programů společnosti Microsoft.
- **[Zásady životního cyklu společnosti Microsoft](/lifecycle/)** - Tato stránka poskytuje konzistentní a předvídatelné pokyny pro dostupnost podpory po celou dobu životnosti produktu.
- **[Průvodce licencí](https://www.microsoft.com/licensing/docs/view/Microsoft-Dynamics-365)** - Pomocí této příručky se dozvíte více o tom, jak licencovat Dynamics 365.
- **[Zákaznická podpora](https://dynamics.microsoft.com/support/)** - Získejte špičkovou podporu pro své aplikace Dynamics 365.
- **[Dynamics Lifecycle Services](https://lcs.dynamics.com/)** - Spravujte životní cyklus své aplikace a přejděte k předvídatelným, opakovatelným a vysoce kvalitním implementacím.
- **[Příručka pro implementaci Dynamics 365](https://aka.ms/D365ImplementationGuideFlip)** – Příručka pro implementaci Dynamics 365 dokumentuje časem prověřené principy Success by Design a poskytuje normativní pokyny k budování, sestavování, testování a nasazení řešení Dynamics 365.

## <a name="definitions"></a>Definice

### <a name="azure-region"></a>[Oblast Azure](/azure/availability-zones/az-overview#regions)

Geografická oblast, ve které existuje jedno nebo více datových center Azure. Mezi příklady patří USA a Evropa.

### <a name="business-process-modeler-bpm"></a>[Modelování podnikových procesů](../../dev-itpro/lifecycle-services/bpm-overview.md)

Nástroj v LCS, který pomáhá dokončit analýzu mezer shody pro danou implementaci pomocí definic obchodních procesů od American Productivity & Quality Center (APQC), které jsou podporovány ve finančních a provozních aplikacích.

### <a name="cloud-solution-provider"></a>Poskytovatel cloudových řešení

Partner, který je součástí programu Microsoft Cloud Solution Provider (CSP) a který poskytuje zákazníkům cloudové služby s přidanou hodnotou, podporu, jednu fakturu a správu zákazníků ve velkém.

### <a name="customer"></a>Zákazník

Podnikatelský subjekt, který spotřebovává finanční a provozní aplikace a je reprezentován klientem v Office 365.

### <a name="development-environment"></a>Vývojové prostředí

Neprovozní prostředí sandboxu, které se používá k vývoji rozšíření. Zákazníci nasazují toto prostředí do svého vlastního předplatného Azure od LCS. Toto prostředí lze také použít pro demonstrační, školicí nebo jiné testovací úkoly. Je známé také jako [Sandbox 1. vrstvy](../imp-lifecycle/environment-planning.md#tier-1-vs-tier-2-and-higher).

### <a name="downtime"></a>Odstávka

Jakákoli doba, kdy se uživatelé nemohou přihlásit nebo přistupovat ke svému aktivnímu tenantovi z důvodu selhání nevypršené platformy nebo servisní infrastruktury, jak stanoví společnost Microsoft z automatického monitorování stavu a systémových protokolů. Odstávky nezahrnují plánované prostoje, nedostupnost funkcí doplňků služby, nemožnost přístupu ke službě kvůli vašim změnám ve službě ani období, kdy je překročena kapacita jednotky škálování.

### <a name="implementation-partner"></a>Implementační partner

Partner, kterého si zákazník vybere k přizpůsobení, konfiguraci, implementaci a správě svého řešení pro finanční a provozní aplikace.

### <a name="incident"></a>Incident

Problém, se kterým se zákazníci setkávají při používání finanční a provozní služby a že podají lístek na prostřednictvím LCS.

### <a name="microsoft-customer-support-services-css"></a>Služby zákaznické podpory společnosti Microsoft (CSS)

Tým globální podpory společnosti Microsoft, který se věnuje poskytování kvalitních služeb pro finanční a provozní aplikace.

### <a name="microsoft-dynamics-lifecycle-services-lcs"></a>Služby Microsoft Dynamics Lifecycle Services (LCS)

Administrativní portál pro správu životního cyklu finančních a provozních aplikací od zkušební verze přes implementaci až po poprovozní správu a podporu. Další informace naleznete v tématu [Zdroje Lifecycle Services](../../dev-itpro/lifecycle-services/lcs.md).

### <a name="non-production-instance"></a>Neprovozní instance

Jakákoli z následujících instancí služby, kterou zákazník používá k ověření rozšíření a provádění dalších vývojových úkolů:

- **Sandbox 1. úrovně** - Instance vývojáře (hostované zákazníkem)
- **Sandbox 2. úrovně** - Instance standardního přejímacího testu
- **Úrovně sandboxu 3–5** - Doplňkové sandboxy

Další informace o úrovních 2 až 5 viz [Výběr správného prostředí úrovně 2 nebo vyšší](../imp-lifecycle/environment-planning.md#selecting-the-correct-tier-2-or-higher-environment).

### <a name="production-instance"></a>Provozní instance

Prostředí pro finance a provoz, které zákazník používá ke správě svých „živých“ denních transakcí a obchodních procesů.

### <a name="sandbox-environment"></a>Sandboxové prostředí

Neprovozní prostředí, které zákazník používá k předvádění, školení, testům přijetí uživatele, ověřování rozšíření a dalším testovacím úkolům.

### <a name="service"></a>Služba

Všechny základní služby, které jsou součástí finančních a provozních aplikací.

### <a name="service-level-agreement-sla-for-microsoft-online-services"></a>Dohoda o úrovni služeb (SLA) pro online služby společnosti Microsoft

Smlouva SLA se vztahuje na online služby společnosti Microsoft. Další informace o fázích servisní zakázky naleznete v tématu [Smlouvy o úrovni služeb](https://www.microsoft.com/licensing/docs/view/Service-Level-Agreements-SLA-for-Online-Services)..

### <a name="service-update"></a>Aktualizace služby

Služby společnosti Microsoft prostředí pro finance a provoz na konzistentním základě prostřednictvím aktualizací služeb. Zákazníci si nastavují vlastní kalendář aktualizací služeb na základě svých obchodních potřeb. Další informace naleznete v tématu [Často kladené dotazy k aktualizacím služby One Version](../../dev-itpro/lifecycle-services/oneversion-overview.md).

### <a name="success-by-design"></a>[Success by Design](/dynamics365/fasttrack/success-by-design-overview)

Rámec, který systematicky vede implementaci řadou hodnocení v kritických fázích, aby byla zajištěna optimální architektura, zabezpečení, výkon a uživatelské prostředí pro řešení Dynamics 365.

### <a name="user"></a>Uživatel

Jedna osoba, která používá prostředí pro finance a provoz a která je spojena s klientem zákazníka.
