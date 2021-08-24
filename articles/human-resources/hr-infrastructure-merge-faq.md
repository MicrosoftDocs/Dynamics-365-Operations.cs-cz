---
title: Často kladené dotazy ke sloučení infrastruktiry Dynamics 365 Human Resources
description: Toto téma odpovídá na často kladené otázky o sloučení infrastruktury pro aplikace Microsoft Dynamics 365 Human Resources a Finance and Operations.
author: rachel-profitt
ms.date: 07/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 537917e9a987d701a0c96dfb7592e124e09bb748e4f2f52d39f8d97000c70ae3
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6711994"
---
# <a name="dynamics-365-human-resources-infrastructure-merge-faq"></a>Často kladené dotazy ke sloučení infrastruktiry Dynamics 365 Human Resources

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Toto téma odpovídá na často kladené otázky o sloučení infrastruktury pro aplikace Microsoft Dynamics 365 Human Resources a Finance and Operations.

## <a name="what-is-the-dynamics-365-human-resources-infrastructure-merge"></a>Co je sloučení infrastruktury Dynamics 365 Human Resources?

Dynamics 365 Human Resources je samostatná aplikace, která používá jinou infrastrukturu než ostatní aplikace Finance and Operations, jako např. Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce a Dynamics 365 Project Operations. Sloučení infrastruktury přenese Dynamics 365 Human Resources do stejné infrastruktury jako ostatní aplikace Finance and Operations.

## <a name="value-and-benefits-of-the-infrastructure-merge"></a>Hodnota a výhody sloučení infrastruktury

### <a name="my-organization-uses-dynamics-365-human-resources-to-manage-its-hr-operations-what-benefits-will-we-see-from-these-changes"></a>Moje organizace používá Dynamics 365 Human Resources pro řízení svých HR operací. Jaké výhody uvidíme z těchto změn?

- Tyto změny eliminují několik sad možností lidských zdrojů (HR) v Dynamics 365.
- Poskytují rozšiřitelnost Microsoft Power Platform i způsob, jak rozšířit obchodní logiku a možnosti funkcí.
- Přinášejí soulad mezi Dynamics 365 Human Resources a dalšími aplikacemi Finance and Operations z hlediska správy životního cyklu aplikací (ALM), Microsoft Dynamics Lifecycle Services (LCS), geografické dostupnosti, rozšiřitelnosti a další.
- Umožní vám využívat sdílené služby a nástroje a pomáhají snižovat náklady.

### <a name="my-organization-uses-dynamics-365-human-resources-in-dynamics-365-finance-supply-chain-management-commerce-or-project-operations-what-benefits-will-we-see-from-these-changes"></a>Moje organizace používá Dynamics 365 Human Resources v Dynamics 365 Finance, Supply Chain Management, Commerce či Project Operations. Jaké výhody uvidíme z těchto změn?

Možnosti a investice do Dynamics 365 Human Resources nyní budou k dispozici zákazníkům, kteří používají HR modul v systému Dynamics 365 Finance. Některé z těchto funkcí zahrnují správu dovolené a nepřítomnosti, správu výhod a správu úkolů.

### <a name="will-i-lose-any-features-or-capabilities-that-i-currently-use"></a>Ztratím nějaké funkce nebo funkce, které aktuálně používám?

Mezi Dynamics 365 Human Resources a HR modul v aplikacích Finance and Operations bude funkční parita. Dynamics 365 Human Resources bude mít přednost u podobných funkcí. Další informace naleznete v tématu [Přehled správy funkcí](../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="will-the-experience-change-for-my-users"></a>Změní se prostředí pro mé uživatele?

Nové funkce HR budou spravovány prostřednictvím správy funkcí. Zákazníci se rozhodnou, zda je chtějí převzít. V některých případech mohou být možnosti upraveny. V těchto případech bude poskytnuta dokumentace.

### <a name="how-does-this-change-affect-me-if-i-am-an-existing-customer-and-i-use-both-the-hr-module-on-the-finance-and-operations-infrastructure-and-dynamics-365-human-resources-through-custom-integrations"></a>Jak na mě tato změna zapůsobí, pokud jsem stávající zákazník a používám jak HR modul v infrastruktuře Finance and Operations, tak i Dynamics 365 Human Resources prostřednictvím vlastních integrací?

Vlastní integrace mezi Dynamics 365 Human Resources a HR modulem v Dynamics 365 Finance již nebude vyžadována. Všechna data o lidských zdrojích budou umístěna ve stejné databázi jako ostatní aplikace Finance and Operations.

## <a name="migration-from-dynamics-365-human-resources-to-finance-and-operations-apps"></a>Migrace z Dynamics 365 Human Resources do aplikací Finance and Operations

### <a name="my-organization-uses-dynamics-365-human-resources-to-manage-hr-operations-what-do-we-have-to-plan-for-to-migrate-to-the-new-experience"></a>Moje organizace používá Dynamics 365 Human Resources pro řízení HR operací. Co musíme naplánovat pro migraci na nové prostředí?

Pokud vaše organizace používá Dynamics 365 Human Resources, ale nepoužívá žádné jiné aplikace Finance and Operations, vaše prostředí Human Resources bude migrováno na novou infrastrukturu. Velká část tohoto procesu migrace bude automatizována. Budou zavedeny procesy pro migraci vaší databáze a její synchronizaci s novou infrastrukturou.

Kromě toho budou k dispozici nástroje, abyste mohli před migrací produkčního prostředí otestovat proces migrace a ověřit svá data a zkušenosti.

Pokud vaše organizace používá Dynamics 365 Human Resources a další aplikace Finance and Operations, měli byste si naplánovat více času na ověření, abyste zajistili, že jsou vaše data správně migrována do nového prostředí. Migrace na novou infrastrukturu sloučí data z vašeho prostředí lidských zdrojů s prostředím Finance and Operations. Budou zavedeny nástroje pro automatizaci co nejvíce procesu slučování dat. Instance konfliktních dat však budou vyžadovat vstup uživatele k definování, jak by měl být konflikt vyřešen. Uživatelé a správci budou muset spravovat mapování dat tam, kde dochází ke konfliktům, a před migrací produkčního prostředí otestovat migraci v sandboxobých prostředích.

### <a name="my-organization-uses-dynamics-365-human-resources-in-dynamics-365-finance-supply-chain-management-commerce-or-project-operations-what-do-we-have-to-plan-for-to-migrate-to-the-new-experience"></a>Moje organizace používá Dynamics 365 Human Resources v Dynamics 365 Finance, Supply Chain Management, Commerce či Project Operations. Co musíme naplánovat pro migraci na nové prostředí?

Pro organizace, které používají modul HR v aplikacích Finance and Operations, nová funkce z Dynamics 365 Human Resources bude aplikována na vaše prostředí prostřednictvím standardního procesu aktualizace One Version. Můžete očekávat, že se nová funkce ve vašem prostředí zobrazí, jakmile bude k dispozici v každé aktualizaci. Zapnutí nových funkcí můžete provést prostřednictvím Správy funkcí. Měli byste však plánovat ověření těchto funkcí. Postupujte podle procesů, které máte zavedeny pro ověřování dalších aktualizací vašeho prostředí. Další informace o způsobu použití aktualizací Finance and Operations viz [Přehled One Version](../fin-ops-core/dev-itpro/lifecycle-services/oneversion-overview.md).

### <a name="when-will-my-organization-be-migrated"></a>Kdy bude moje organizace migrována?

Migrace pro každou organizaci bude záviset na její aktuální konfiguraci a připravenosti k migraci na novou infrastrukturu. Tato data se mohou změnit.

- Organizace, které aktuálně používají modul HR v aplikacích Finance and Operations obdrží funkci HR pro Dynamics 365 Human Resources jako součást běžného procesu aktualizace One Version. Nové funkce by měly být obecně dostupné začátkem října 2021.
- Organizace, které aktuálně používají pouze Dynamics 365 Human Resources, budou mít přístup k nástrojům pro migraci, aby mohli začít testovat a zahájit migraci od poloviny roku 2022. Datum, do kterého musí být dokončena migrace na novou infrastrukturu, ještě nebylo stanoveno. Bude to však alespoň jeden rok po datu, kdy budou k dispozici nástroje pro migraci.
- Organizace, které aktuálně používají Dynamics 365 Human Resources i další aplikace Finance and Operations, budou mít přístup k nástrojům pro migraci, aby mohli začít testovat a zahájit migraci od podzimu roku 2022. Datum, do kterého musí být dokončena migrace na novou infrastrukturu, ještě nebylo stanoveno. Bude to však alespoň jeden rok po datu, kdy budou k dispozici nástroje pro migraci.

Další informace o nových funkcích pro Dynamics 365 Human Resources viz [Co je nového nebo se změnilo v Human Resources](./hr-admin-whats-new.md).

### <a name="i-am-using-new-capabilities-that-are-available-only-in-dynamics-365-human-resources-such-as-leave-and-absence-and-benefits-management-will-these-capabilities-now-be-available-in-the-human-resources-module-on-the-finance-and-operations-infrastructure-too"></a>Používám nové funkce, které jsou k dispozici pouze v systému Dynamics 365 Human Resources (jako **Dovolená a nepřítomnost** a **Správa výhod**). Budou tyto funkce nyní k dispozici v modulu Human Resources také v infrastruktuře Finance and Operations?

Ano, všechny moduly z Dynamics 365 Human Resources budou fungovat tak, jako v aplikacích Finance and Operations a bude existovat 100% parita funkcí. V rámci celkové migrační strategie pro zákazníky, kteří v současnosti tyto funkce v HR využívají, budou data zákazníků migrována tak, aby i nadále fungovala v infrastruktuře Finance and Operations.

### <a name="i-use-the-new-dynamics-365-human-resources-benefits-management-capabilities-ive-built-custom-integrations-with-the-hr-module-on-the-finance-and-operations-infrastructure-so-that-i-can-take-advantage-of-the-payroll-capabilities-by-using-benefits-data-will-these-custom-integrations-be-required-going-forward"></a>Používám nové možnosti správy zaměstnaneckých výhod Dynamics 365 Human Resources. Postavil jsem vlastní integraci s HR modulem v infrastruktuře Finance and Operations, abych mohl využívat možnosti mezd pomocí údajů o zaměstnaneckých výhodách. Budou tyto vlastní integrace vyžadovány i nadále?

V rámci sloučení infrastruktury jsou HR data přenesena do stejné databáze jako ostatní aplikace Finance and Operations. Integrace mezi moduly v aplikacích Finance and Operations již nebudou vyžadovány.

### <a name="my-organization-uses-one-or-more-isv-solutions-with-dynamics-365-human-resources-will-our-isv-solutions-be-migrated-automatically"></a>Moje organizace používá jedno nebo více řešení ISV s Dynamics 365 Human Resources. Budou naše řešení ISV migrována automaticky?

Migrace pro každé nezávislé řešení dodavatele softwaru (ISV) se bude lišit v závislosti na integrační metodě řešení. Microsoft bude úzce spolupracovat s nezávislými dodavateli softwaru, aby zajistil hladký přechod na novou infrastrukturu.

### <a name="my-organization-uses-linkedin-talent-hub-integration-with-dynamics-365-human-resources-will-this-integration-continue-to-work-after-the-infrastructure-change-is-completed"></a>Moje organizace používá integraci LinkedIn Talent Hub s Dynamics 365 Human Resources. Bude tato integrace fungovat i po dokončení změny infrastruktury?

Ano, integrace LinkedIn Talent Hub bude fungovat i po migraci na novou infrastrukturu.

### <a name="my-organization-uses-the-human-resources-app-for-teams-will-the-app-continue-to-work-after-the-infrastructure-change-is-completed"></a>Moje organizace používá aplikaci Human Resources pro Teams. Bude tato aplikace fungovat i po dokončení změny infrastruktury?

Ano, Human Resources pro Teams bude fungovat i po migraci na novou infrastrukturu.

### <a name="my-organization-has-configured-custom-security-in-dynamics-365-human-resources-will-our-custom-security-still-be-applied-after-the-infrastructure-change-is-completed"></a>Moje organizace nakonfigurovala vlastní zabezpečení v Dynamics 365 Human Resources. Bude naše vlastní zabezpečení použito i po dokončení změny infrastruktury?

Ano, do konfigurace migrace dat na novou infrastrukturu budou zahrnuty vlastní konfigurace zabezpečení.

### <a name="we-are-using-data-integrator-to-move-data-between-dynamics-365-human-resources-and-finance-and-operations-apps-how-will-the-data-that-is-currently-being-integrated-be-affected"></a>Používáme integrátor dat pro přesun dat mezi aplikacemi Dynamics 365 Human Resources a Finance and Operations. Jak to ovlivní data, která se aktuálně integrují?

HR data, která jsou aktuálně řízena v Dynamics 365 Human Resources jsou synchronizována s Dataverse. Integrátor dat lze poté použít pro jednosměrnou synchronizaci s aplikacemi Finance and Operations. Po migraci na novou infrastrukturu budou data HR nativní pro aplikace Finance and Operations. K synchronizaci dat mezi aplikacemi Finance and Operations a Human Resources již nebude vyžadován datový integrátor.

Aktuální nativní datové tabulky Dataverse pro Human Resources budou i nadále synchronizovat data z prostředí na nové infrastruktuře. Entity budou převedeny na podporu duálního zápisu. Jakékoli další integrace dat, které jsou konfigurovány pomocí integrátoru dat proti těmto tabulkám pro jiné aplikace Dynamics 365, budou i nadále fungovat tak, jak jsou aktuálně nakonfigurovány.

### <a name="we-are-using-dual-write-to-move-hr-data-between-dataverse-and-other-finance-and-operations-apps-how-will-the-data-that-is-currently-being-integrated-be-affected-by-the-migration-to-the-new-infrastructure"></a>K přenosu dat HR mezi Dataverse a dalšími aplikacemi Finance and Operations používáme duální zápis. Jak migrace na novou infrastrukturu ovlivní data, která se aktuálně integrují?

Data HR budou nativní pro aplikace Finance and Operations v prostředí v nové infrastruktuře. Duální zápis bude poté použit k přesunu dat HR mezi novým prostředím a prostředím Dataverse.

### <a name="we-have-built-custom-integrations-from-dynamics-365-human-resources-to-one-or-more-external-systems-will-we-have-to-develop-new-integrations-after-the-infrastructure-change-is-completed"></a>Vytvořili jsme vlastní integrace z Dynamics 365 Human Resources do jednoho nebo více externích systémů. Budeme muset vyvíjet nové integrace i po dokončení změny infrastruktury?

Záleží na koncovém bodě integrace. Další informace o integračních technologiích, které jsou k dispozici v aplikacích Finance and Operations a o tom, jak vybrat nejlepší integrační technologii, viz [Přehled integrace](../fin-ops-core/dev-itpro/data-entities/integration-overview.md).

### <a name="we-have-extended-dataverse-for-dynamics-365-human-resources-will-these-extensions-be-migrated-automatically"></a>Rozšířili jsme Dataverse pro Dynamics 365 Human Resources. Budou tato rozšíření migrována automaticky?

Pokud jsou prostředí Dynamics 365 Human Resources a Finance and Operations, která budou spojena v prostředí na nové infrastruktuře, připojena ke stejnému prostředí Dataverse, budou obě aplikace nadále připojeny ke stejnému prostředí Dataverse po migraci. U žádného rozšíření Dataverse proto není nutná žádná migrace.

Pokud jsou však prostředí Dynamics 365 Human Resources a Finance and Operations aktuálně spojena do oddělených prostředí Dataverse, obě prostředí Dataverse bude třeba zkombinovat, aby byly připojeny k jednomu prostředí na nové infrastruktuře. Pro tuto migraci Dataverse mohou být tabulky Dataverse, které jsou standardem řešení Human Resources, připojeny a znovu synchronizovány s novým prostředím Dataverse. Žádná rozšíření prostředí Dataverse nebudou migrována automaticky, ale musí být znovu nasazena v novém prostředí. Ke správě svých rozšíření Dataverse doporučujeme použít spravovaná řešení. Další informace viz [Úvod do řešení](https://docs.microsoft.com/powerapps/developer/data-platform/introduction-solutions).

### <a name="we-have-configured-microsoft-power-automate-flows-andor-microsoft-power-apps-to-work-with-dynamics-365-human-resources-will-these-microsoft-power-platform-components-be-migrated-and-work-automatically-after-the-infrastructure-change-is-completed"></a>Nakonfigurovali jsme toky Microsoft Power Automate a/nebo Microsoft Power Apps pro práci s Dynamics 365 Human Resources. Budou tyto komponenty Microsoft Power Platform migrovány a fungují automaticky po dokončení změny infrastruktury?

Power Apps, toky Power Automate a další přizpůsobení Microsoft Power Platform se podobají rozšířením Dataverse. Zda fungují automaticky po migraci na novou infrastrukturu, závisí na tom, zda jsou aplikace Human Resources a Finance and Operations připojeny ke stejnému prostředí Power Apps před migrací.

Pokud jsou aplikace aktuálně připojeny ke stejnému prostředí Power Apps, budou s tímto prostředím Power Apps i nadále spojeny po migraci na novou infrastrukturu. V tomto případě Power Apps, toky Power Automate a další přizpůsobení Microsoft Power Platform budou i nadále fungovat bez jakékoli další konfigurace. Ke správě svých rozšíření aplikací v Dataverse doporučujeme použít spravovaná řešení. Další informace viz [Úvod do řešení](https://docs.microsoft.com/powerapps/developer/data-platform/introduction-solutions).

Pokud však aplikace Human Resources a Finance and Operations jsou připojeny k samostatným prostředím Power Apps, bude nutné je v rámci migrace kombinovat. Tento úkol bude vyžadovat, aby byla jakákoliv přizpůsobení Power Apps a další přizpůsobení znovu nasazena v novém prostředí.

### <a name="we-have-enabled-dataverse-virtual-tables-for-dynamics-365-human-resources-what-will-happen-to-these-tables-during-the-migration"></a>Povolili jsme virtuální tabulky Dataverse pro Dynamics 365 Human Resources. Co se stane s těmito tabulkami během migrace?

Po migraci, pokud prostředí na nové infrastruktuře zůstane připojeno k prostředí Dataverse, které je aktuálně připojeno k Dynamics 365 Human Resources, vitruální tabulky Dataverse, které byly vygenerovány v tomto prostředí, budou i nadále fungovat bez jakékoli další konfigurace.

Pokud je však prostředí na nové infrastruktuře připojeno k jinému prostředí Dataverse po migraci, bude nutné virtuální tabulky znovu vygenerovat v novém prostředí Dataverse.

### <a name="we-have-developed-an-integration-by-using-the-applicant-tracking-system-ats-api-payroll-api-dataverse-virtual-tables-for-dynamics-365-human-resources-or-other-entities-in-the-dataverse-web-api-will-these-integrations-continue-to-work-after-the-infrastructure-change-is-completed"></a>Integraci jsme vyvinuli pomocí API Applicant Tracking System (ATS), Payroll API, virtuálních tabulek Dataverse pro Dynamics 365 Human Resources nebo jiných entit v Dataverse Web API. Budou tyto integrace fungovat i po dokončení změny infrastruktury?

Po migraci, pokud prostředí na nové infrastruktuře zůstane připojeno k prostředí Dataverse, které je aktuálně připojeno k Dynamics 365 Human Resources, jakékoliv integrace, které byly vyvinuty pomocí Dataverse Web API, budou i nadále fungovat po dokončení migrace.

Pokud je však prostředí na nové infrastruktuře po migraci připojeno k jinému prostředí Dataverse, jakékoliv integrace, které byly vyvinuty pomocí Dataverse Web API, bude třeba znovu nakonfigurovat, aby se mohly připojit k novému prostředí Dataverse.

### <a name="is-there-an-impact-on-the-azure-region-when-my-environment-is-migrated"></a>Existuje při migraci mého prostředí dopad na oblast Azure?

Očekává se, že vaše prostředí Human Resources během migrace obvykle zůstane ve stejné oblasti Azure. Jedinou výjimku nastane, pokud bude prostředí Human Resources sloučeno s prostředím Finance and Operations, které je v jiné oblasti. V tomto případě bude prostředí Human Resources migrováno do oblasti Azure, kde je prostředí Finance and Operations.

### <a name="my-organization-depends-on-workflows-in-dynamics-365-human-resources-for-one-or-more-business-processes-will-the-workflows-be-migrated-automatically"></a>Moje organizace závisí na pracovních postupech v Dynamics 365 Human Resources pro jeden nebo více obchodních procesů. Budou pracovní postupy migrovány automaticky?

Ano, budou migrovány konfigurace pracovního postupu, historie pracovního postupu a aktuální pracovní postupy v procesu.

### <a name="what-training-and-resources-will-be-available-to-help-with-the-migration-process"></a>Jaké školení a zdroje budou k dispozici na pomoc s procesem migrace?

K podrobnému popisu každého kroku procesu migrace bude poskytnuta úplná dokumentace. Podle potřeby mohou být k dispozici také další zdroje pro školení, jako jsou videa a workshopy.

### <a name="my-organization-has-created-saved-views-in-dynamics-365-human-resources-to-improve-the-usability-of-the-interface-will-the-saved-views-be-migrated-automatically"></a>Moje organizace vytvořila Uložená zobrazení v Dynamics 365 Human Resources, aby zlepšila použitelnost rozhraní. Budou Uložená zobrazení migrována automaticky?

Ano, uložená zobrazení budou migrována do nové infrastruktury.

### <a name="we-are-using-ceridian-with-dynamics-365-human-resources-will-the-ceridian-integration-be-available-after-the-infrastructure-change-is-completed"></a>Používáme Ceridian s Dynamics 365 Human Resources. Budou integrace Ceridian k dispozici i po dokončení změny infrastruktury? 

Integrace s Ceridianem bude migrována na integraci založenou na mzdovém API. Integrace založená na souborech, která aktuálně existuje v Dynamics 365 Human Resources, nebude migrována do infrastruktury Finance and Operations. Další informace viz [Úvod k Payroll API](./hr-admin-integration-payroll-api-introduction.md).

### <a name="how-will-the-migration-affect-the-service-update-process"></a>Jak ovlivní migrace proces aktualizace služby?

Po migraci budou mít zákazníci mnohem větší flexibilitu, pokud jde o ALM a aktualizace služeb. Aktualizace služeb již nebudou automaticky použity v prostředích Human Resources. Místo toho bude služba sledovat procesy a funkce aktualizace služby One Version. Proto budou možnosti konfigurace aktualizací dostupné prostřednictvím LCS. Další informace naleznete v tématu [Přehled One Version](../fin-ops-core/dev-itpro/lifecycle-services/oneversion-overview.md).

### <a name="how-will-the-migration-affect-my-lcs-project-for-dynamics-365-human-resources"></a>Jak ovlivní migrace můj projekt LCS pro Dynamics 365 Human Resources?

Migrace na novou infrastrukturu přesune správu vašich prostředí Dynamics 365 Human Resources do projektu implementace LCS. Pokud migrace slučuje Dynamics 365 Human Resources se stávajícím prostředím Finance and Operations, bude váš projekt LCS Human Resources sloučen do projektu implementace LCS pro aplikaci Finance and Operations. Pokud aktuálně používáte pouze Dynamics 365 Human Resources, bude vytvořen nový projekt implementace LCS a váš stávající projekt LCS Human Resources bude migrován do nového projektu.

Nový projekt bude mít stejný typ projektu, který používají aplikace Finance and Operations. Bude mít stejné funkce pro správu prostředí. Další informace naleznete v tématu [Zdroje Lifecycle Services](../fin-ops-core/dev-itpro/lifecycle-services/lcs.md).

### <a name="we-have-linked-our-task-recordings-to-the-business-process-modeler-in-human-resources-how-will-the-business-process-modeler-be-migrated-and-merged-into-lcs"></a>Propojili jsme naše záznamy úkolů s Business Process Modeler v Human Resources. Jak bude produkt Business Process Modeler migrován a sloučen do LCS?

Knihovny obchodních procesů pro projekt LCS budou migrovány do nového projektu LCS pro Human Resources.

### <a name="my-organization-currently-uses-only-dynamics-365-human-resources-what-resources-are-available-so-that-we-can-learn-more-about-the-development-capabilities-after-the-infrastructure-change-is-completed"></a>Moje organizace aktuálně používá pouze Dynamics 365 Human Resources. Jaké zdroje jsou k dispozici, abychom se mohli po dokončení změny infrastruktury dozvědět více o možnostech vývoje?

Možnosti rozšiřitelnosti Microsoft Power Platform a možnosti rozšiřitelnosti Finance and Operations budou k dispozici a lze je použít pro vývoj. Další informace viz [Vytvořte a přizpůsobte domovskou stránku](../fin-ops-core/dev-itpro/dev-tools/developer-home-page.md).

### <a name="we-have-enabled-features-in-dynamics-365-human-resources-will-these-features-be-enabled-automatically-during-the-migration"></a>Povolili jsme funkce v Dynamics 365 Human Resources. Budou tyto funkce během migrace povoleny automaticky?

Zda je funkce v nové infrastruktuře povolena automaticky, bude pro každou funkci určeno samostatně. Tyto informace budou zahrnuty v dokumentaci funkcí.

### <a name="what-happens-to-my-byod-database-during-the-migration"></a>Co se stane s mojí databází BYOD během migrace?

Konfigurace importu a exportu pro přenesení vlastní databáze (BYOD) budou migrovány do nové infrastruktury.

### <a name="what-happens-to-my-azure-data-lake-during-the-migration"></a>Co se stane s mojí Azure Data Lake během migrace?

Jakýkoli export, který je aktuálně nakonfigurován pro Azure Data Lake Storage v aplikacích Finance and Operations, budou po migraci udržovat stejnou konfiguraci.

### <a name="we-are-currently-using-dynamics-ax-2012-will-the-upgrade-tools-that-are-currently-available-be-used-to-upgrade-the-hr-module-in-ax-2012-to-dynamics-365-human-resources"></a>Momentálně používáme Dynamics AX 2012. Budou použity nástroje pro upgrade, které jsou aktuálně k dispozici, k upgradu modulu HR v AX 2012 na Dynamics 365 Human Resources?

Ano. Dynamics 365 Human Resources bude zahrnuto do sloučené databáze a infrastruktury pro aplikace Finance and Operations. Upgrade z Dynamics AX 2012 na Dynamics 365 Human Resources použije stejnou cestu k upgradu a nástroje, které se používají k upgradu na nejnovější verzi aplikací Finance and Operations.

### <a name="we-use-document-handling-with-dynamics-365-human-resources-what-will-happen-to-the-documents-during-the-migration"></a>Používáme zpracování dokumentů s Dynamics 365 Human Resources. Co se stane s dokumenty během migrace?

Dokumenty zůstanou ve stávajícím úložišti dokumentů. Budou přemapovány do prostředí v nové infrastruktuře.

### <a name="what-happens-to-the-batch-jobs-that-we-have-configured-in-dynamics-365-human-resources-after-the-migration"></a>Co se stane s dávkovými úlohami, které jsme nakonfigurovali v Dynamics 365 Human Resources po migraci?

Příslušné dávkové úlohy budou automaticky přeneseny do nové infrastruktury.

## <a name="licensing-impact"></a>Dopad licencování

Tato dokumentace nenahrazuje ani nenahrazuje žádnou právní dokumentaci pokrývající užívací práva.

### <a name="my-organization-uses-dynamics-365-human-resources-to-manage-its-hr-operations-does-our-licensing-or-cost-change"></a>Moje organizace používá Dynamics 365 Human Resources pro řízení svých HR operací. Mění se naše licence nebo náklady?

Zákazníci, kteří zakoupili licence Dynamics 365 Human Resources, nebudou ovlivněni. U těchto zákazníků neexistuje migrace licencí. Dodatečná sandboxová skladová jednotka (SKU), která byla specifická pro Human Resources, již nebude použitelná. Místo toho se zákazníci mohou rozhodnout koupit sandbox vrstvy 2 aplikací Finance and Operations za mírně nižší cenu. Stávající zákazníci, kteří si zakoupili sanbox Human Resources, budou migrováni na sandbox vrstvy 2 aplikací Finance and Operations bez dalších nákladů.

### <a name="my-organization-uses-dynamics-365-human-resources-in-dynamics-365-finance-supply-chain-management-commerce-or-project-operations-does-my-licensing-or-cost-change"></a>Moje organizace používá Dynamics 365 Human Resources v Dynamics 365 Finance, Supply Chain Management, Commerce či Project Operations. Mění se moje licence nebo náklady?

Stávající uživatelé aplikací Dynamics 365 a uživatelé samostatných aplikací Dynamics 365 Finance, Supply Chain Management, Commerce a Project Operations, mají přístup k Human Resources jakožto součást těchto licencí do února 2025 nebo do vypršení platnosti stávající licenční smlouvy podle toho, co nastane dříve. Můžete se rozhodnout přejít na licence Human Resources dříve, pokud vám to pomůže dosáhnout lepších úspor nákladů. Od února 2025 musí všichni stávající zákazníci CSP a EA nasadit modul HR a zakoupit si licence Human Resources, aby mohli využívat výhod nových funkcí, které přinášejí aplikace Finance and Operations.

### <a name="my-organization-is-live-with-dynamics-365-finance-supply-chain-management-commerce-or-project-operations-will-we-be-required-to-purchase-an-additional-environment-to-support-the-infrastructure-merge"></a>Moje organizace používá Dynamics 365 Finance, Supply Chain Management, Commerce či Project Operations. Budeme povinni zakoupit další prostředí na podporu sloučení infrastruktury?

K podpoře změny infrastruktury se nevyžadují další prostředí.

### <a name="where-should-i-go-if-i-have-additional-questions-about-product-licensing"></a>Na koho se mám obrátit, pokud mám další dotazy týkající se licencování produktů?

Pokud máte otázky týkající se licencí, najdete další informace na [Biz Apps Hub - ceny a licence D365](https://businessapplications.transform.microsoft.com/resources/pricing-and-licensing?tab=grandfathering). Pokud tyto informace nepomohou vyřešit váš problém, otevřete požadavek pomocí LicenseQ.
