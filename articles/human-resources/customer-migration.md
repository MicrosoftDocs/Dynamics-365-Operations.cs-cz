---
title: Časté otázky k zákaznické migraci Human Resources
description: Tento článek odpovídá na často kladené otázky o migraci Microsoft Dynamics 365 Human Resources do sloučené infrastruktury financí a provozu.
author: twheeloc
ms.date: 07/06/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8a6f883da07bd1d3a6b0379f1582dc8556e166ff
ms.sourcegitcommit: 9310c943ac76896663e5604209034da9f8d6139c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/14/2022
ms.locfileid: "9151076"
---
# <a name="human-resources-customer-migration"></a>Zákaznická migrace Human Resources

## <a name="how-should-dynamics-365-human-resources-customers-plan-to-move-to-the-finance-and-operations-infrastructure"></a>Jak by měli zákazníci Dynamics 365 Human Resources plánovat přejít na finanční a provozní infrastrukturu?

Dvě kategorie zákazníků Microsoft Dynamics 365 Human Resources budou ovlivněny a budou muset provést změny, aby zajistily, že budou využívat nejnovější finanční a provozní infrastrukturu:

- Zákazníci, kteří používají Dynamics 365 Human Resources a nemají žádné další provozní aplikace z Dynamics 365
- Zákazníci, kteří používají Dynamics 365 Human Resources i Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce nebo Dynamics 365 Project Operations

Bez ohledu na kategorii, do které zákazníci patří, budou muset přesunout data do nově vytvořeného prostředí finanční a provozní infrastruktury a ověřit, že sloučení bylo úspěšně dokončeno.

Do budoucna bude aplikace Dynamics 365 Human Resources mít své vlastní finanční a provozní prostředí, které je oddělené od ostatních provozních aplikací. Zákazníci tak budou moci využívat možnosti rozšiřitelnosti, aniž by museli slučovat svá aktuální data. Společnost Microsoft poskytne nástroje a prostředí sandbox, které mohou zákazníci použít k testování a ověřování migrace dat před přechodem do produkčního prostředí. Nástroje umožní téměř automatizovaný proces a budou k dispozici od srpna do listopadu 2022.

Zákazníci, kteří používají jiné aplikace ve finanční a provozní infrastruktuře, budou mít možnost sloučit svá data Human Resources se stávajícím prostředím. 

## <a name="when-will-customers-be-moved-to-the-finance-and-operations-infrastructure"></a>Kdy budou zákazníci přesunuti na finanční a provozní infrastrukturu?

Přechod pro jednotlivé společnosti bude záviset na aktuální konfiguraci společnosti a připravenosti k přechodu na finanční a provozní infrastrukturu. Doporučujeme, aby zákazníci spolupracovali se svým partnerem Microsoft a určili nejlepší cestu vpřed.

- Organizace, které používají modul **Human Resources** v Dynamics 365 Finance, budou moci aktivovat nové funkce z Dynamics 365 Human Resources jako součást pravidelného procesu aktualizace jedné verze. Nové funkce by měly být obecně dostupné od ledna 2022.
- Organizace, které používají Dynamics 365 Human Resources, budou mít přístup k nástrojům, které mohou použít k dokončení sloučení infrastruktury. Společnost Microsoft bude na přechodu spolupracovat se zákazníky, aby zabránila jakémukoli přerušení služby. Zákazníci budou mít na provedení přechodu 12 až 18 měsíců, počínaje okamžikem, kdy budou k dispozici nástroje pro migraci.
- Organizace, které využívají Dynamics 365 Human Resources i modul **Human Resources**, mohou přesunout samostatnou infrastrukturu Human Resources do finanční a provozní infrastruktury. Další možností je použít slučovací nástroj k převedení prostředí do jednoho prostředí. Neexistuje žádný požadavek ani časový rámec pro sloučení těchto dvou prostředí.

Pro aktuální informace pravidelně kontrolujte [plány vydání](/dynamics365/release-plans/).

## <a name="will-customers-still-need-custom-integrations-between-dynamics-365-human-resources-and-the-human-resources-module"></a>Budou zákazníci stále potřebovat vlastní integraci mezi Dynamics 365 Human Resources a modulem Human Resources?

- Zákazníci, kteří mají Dynamics 365 Human Resources i další prostředí finanční a provozní infrastruktury, která jsou v současnosti integrována, budou muset po sloučení pokračovat v integraci těchto dvou prostředí.
- Zákazníci, kteří se rozhodli ponechat si prostředí Dynamics 365 Human Resources oddělené od stávajícího prostředí finančních a provozních aplikací, budou muset pokračovat v integraci těchto prostředí, aby byla data dostupná v obou prostředích.
- Zákazníci mohou nadále používat Integrátor dat ke kopírování dat mezi těmito dvěma prostředími. Zákazníci, kteří po migraci sloučí data do jednoho prostředí, již nebudou muset data integrovat, protože všechna data budou v jediné databázi.

## <a name="will-customer-isv-solutions-automatically-be-migrated"></a>Budou řešení ISV zákazníka automaticky migrována?

Migrace pro každé nezávislé řešení dodavatele softwaru (ISV) se bude lišit v závislosti na integrační metodě řešení. Společnost Microsoft bude úzce spolupracovat s nezávislými dodavateli softwaru, aby pomohla zajistil hladký přechod na finanční a provozní infrastrukturu. Mnoho řešení ISV je postaveno na Dataverse s využitím schopností Microsoft Power Platform. Tato řešení závisí na integraci Dataverse mezi prostředím Dynamics 365 Human Resources a prostředím Dataverse. Integrace Dataverse je v rámci slučování infrastruktury zastaralá. Ve finanční a provozní infrastruktuře jsou plánovány nové mapy s duálním zápisem, které nahradí funkčnost integrace Dataverse.

## <a name="how-will-the-data-integrator-that-moves-data-between-dynamics-365-human-resources-and-other-dynamics-365-apps-be-affected"></a>Jak bude Integrátor dat, který přesouvá data mezi Dynamics 365 Human Resources a dalšími aplikacemi Dynamics 365, ovlivněn?

Poté, co zákazníci přejdou na finanční a provozní infrastrukturu, budou muset pokračovat v integraci dat mezi těmito dvěma prostředími. Zákazníci mohou k provádění těchto úloh migrace dat nadále používat integrátor dat. Zákazníci, kteří si plánují ponechat si prostředí Dynamics 365 Human Resources oddělené od stávajícího prostředí finančních a provozních aplikací, budou muset pokračovat v integraci dat mezi těmito dvěma prostředími. Pro zákazníky, kteří sloučí dvě prostředí do jednoho prostředí, již nebude nutná integrace mezi těmito dvěma prostředími.

## <a name="how-will-data-be-moved-between-dynamics-365-human-resources-on-the-finance-and-operations-infrastructure-and-dataverse-after-the-migration"></a>Jak budou po migraci přesouvána data mezi Dynamics 365 Human Resources na finanční a provozní infrastruktuře a Dataverse?

Aktuální integrace Dataverse mezi Dynamics 365 Human Resources a Dataverse je zastaralá jako součást finanční a provozní infrastruktury. Plánuje se zavedení map s duálním zápisem, které by mapovaly finanční a provozní entity na tabulky Dataverse. Zákazníci se budou muset rozhodnout, které mapy s duálním zápisem jsou potřebné pro jejich implementaci. Doporučujeme, aby se pro integrace a řešení ISV používaly virtuální tabulky, pokud neexistuje konkrétní obchodní potřeba duplikovat data v Dataverse pro provozování obchodní logiky.

## <a name="how-does-the-migration-affect-dataverse-extensions-for-dynamics-365-human-resources"></a>Jak ovlivní migrace rozšíření Dataverse pro Dynamics 365 Human Resources?

Zákazníci budou muset před migrací svého produkčního prostředí migrovat do prostředí sandbox. Když zákazníci migrují své prostředí sandbox, budou si muset vytvořit kopii svého prostředí Dataverse pro připojení k novému prostředí migrace financí a provozu. Doporučujeme, aby si zákazník zkopíroval data i řešení pro prostředí tak, aby odpovídaly aktuálnímu produkčnímu prostředí zákazníka.

Když jsou zákazníci připraveni migrovat produkční prostředí Dynamics 365 Human Resources, Microsoft automaticky migruje databázi a úložiště objektů blob Azure. Migrovaná databáze a úložiště namíří nové prostředí ve finanční a provozní infrastruktuře na stejné produkční prostředí Dataverse. Než bude možné pokračovat v kopírování dat Dataverse, zákazníci budou muset aktivovat všechny mapy s duálním zápisem, které jsou nutné pro jejich integrace, rozšíření a řešení ISV, která jsou postavena na Dataverse.

## <a name="will-microsoft-power-platform-components-that-were-built-for-dynamics-365-human-resources-automatically-work-after-the-infrastructure-migration-is-completed"></a>Budou komponenty Microsoft Power Platform, které byly vytvořeny pro Dynamics 365 Human Resources, automaticky fungovat po dokončení migrace infrastruktury?

Aplikace, které jsou vytvořeny v Power Apps, toky, které jsou vytvořeny v Power Automate, a další přizpůsobení Microsoft Power Platform jsou jako rozšíření Dataverse. Během migrace zákaznických produkčních prostředí nedochází k žádnému dopadu na prostředí Dataverse, včetně všech rozšíření. Aplikace, toky a další přizpůsobení Power Microsoft Platform by měly nadále fungovat bez nutnosti další konfigurace.

## <a name="what-will-happen-to-dataverse-virtual-table-entities-for-dynamics-365-human-resources-during-the-migration"></a>Co se během migrace stane s entitami virtuální tabulky Dataverse pro Dynamics 365 Human Resources?

Když zákazníci migrují prostředí Dynamics 365 Human Resources do finanční a provozní infrastruktury, prostředí zůstane spojeno s prostředím Dataverse, které je aktuálně připojeno k Dynamics 365 Human Resources. Virtuální tabulky Dataverse, které byly vygenerovány v prostředí, budou i nadále fungovat bez nutnosti jakékoli další konfigurace. Virtuální tabulky může být nutné znovu vygenerovat v prostředí Dataverse, které je propojeno se stávajícím finančním a provozním prostředím zákazníka.

## <a name="how-will-an-integration-that-uses-the-applicant-tracking-system-ats-api-payroll-api-dataverse-virtual-tables-for-dynamics-365-human-resources-or-other-entities-in-the-dataverse-web-api-work-after-the-infrastructure-merge-is-completed"></a>Jak bude fungovat integrace, která využívá API systému sledování žadatelů (ATS), API mezd, virtuální tabulky Dataverse pro Dynamics 365 Human Resources nebo jiné entity ve webovém rozhraní API Dataverse, po dokončení sloučení infrastruktury?

Když zákazníci migrují prostředí Dynamics 365 Human Resources do finanční a provozní infrastruktury, prostředí zůstane spojeno s prostředím Dataverse, které je aktuálně připojeno k Dynamics 365 Human Resources. Jakékoli integrace, které byly vyvinuty proti webovému rozhraní API Dataverse, budou fungovat i po dokončení migrace.

## <a name="our-organization-has-configured-custom-security-in-dynamics-365-human-resources-will-it-still-be-applied-after-the-infrastructure-migration-is-completed"></a>Naše organizace nakonfigurovala vlastní zabezpečení v Dynamics 365 Human Resources. Bude použito i po dokončení migrace infrastruktury?

Ano, do konfigurace migrace dat budou zahrnuty vlastní konfigurace zabezpečení.

## <a name="will-workflows-in-dynamics-365-human-resources-automatically-be-migrated"></a>Budou pracovní postupy v Dynamics 365 Human Resources automaticky migrovány?

Ano, do sloučené infrastruktury budou migrovány konfigurace pracovního postupu, historie pracovního postupu a aktuální pracovní postupy v procesu.

## <a name="will-saved-views-in-dynamics-365-human-resources-automatically-be-migrated"></a>Budou uložená zobrazení v Dynamics 365 Human Resources migrována automaticky?

Ano, uložená zobrazení budou migrována do sloučené infrastruktury.

## <a name="will-features-that-are-enabled-in-dynamics-365-human-resources-automatically-be-available-after-the-infrastructure-merge"></a>Budou funkce, které jsou aktivní v Dynamics 365 Human Resources, automaticky k dispozici po sloučení infrastruktury?

- Pro zákazníky, kteří používají modul **Human Resources**, funkce, které jsou dostupné pouze v Dynamics 365 Human Resources, budou spravováno prostřednictvím správy funkcí. Tyto funkce obvykle nejsou ve výchozím nastavení aktivní. Všechny funkce, které musí být ve výchozím nastavení aktivní, budou zdokumentovány.
- Pro zákazníky, kteří používají Dynamics 365 Human Resources, budou funkce dostupné v infrastruktuře. Všechny funkce, které nejsou k dispozici, budou zdokumentovány. Každý klíč správy funkcí, který je aktivní v aktuálním prostředí Dynamics 365 Human Resources, bude aktivní ve sloučené infrastruktuře. Další informace naleznete v tématu [Přehled správy funkcí](/fin-ops/get-started/feature-management-overview.md).

## <a name="what-happens-to-byod-databases-during-the-migration"></a>Co se stane s mojí databází BYOD během migrace?

Konfigurace importu a exportu pro přenesení vlastní databáze (BYOD) budou migrovány do finanční a provozní infrastruktury.

## <a name="is-there-an-impact-on-the-azure-region-when-the-customer-environment-is-migrated"></a>Existuje při migraci prostředí zákazníka dopad na oblast Azure?

Prostředí Dynamics 365 Human Resources zůstane po migraci ve stejné oblasti Azure. Pokud existuje požadavek na přesun prostředí do jiné oblasti Azure, zákazníci budou muset po dokončení migrace migrovat do nové oblasti podle standardních kroků.

## <a name="what-happens-to-azure-data-lakes-during-the-migration"></a>Co se stane s datovými jezery Azure během migrace?

Jakýkoli export, který je aktuálně nakonfigurován pro Azure Data Lake ve finančních a provozních aplikacích, bude po migraci udržovat stejnou konfiguraci.

> [!NOTE]
> Aby bylo možné pokračovat v zápisu dat z prostředí Human Resources do Dataverse, bude nutné aktivovat mapy s duálním zápisem.

Zákazníci, kteří chtějí exportovat data Human Resources do datového jezera, mohou tuto funkci aktivovat po dokončení migrace na finanční a provozní infrastrukturu. Více informací viz [Datová jezera – Azure Architecture Center](/azure/architecture/data-guide/scenarios/data-lake).

Zákazníci mohou ke stejnému datovému jezeru propojit více finančních a provozních prostředí. Každé prostředí však bude ukazovat na jinou složku a kontejner. Zákazníci, kteří plánují sloučení prostředí později, by měli svůj přístup pečlivě naplánovat.
 
## <a name="what-migration-will-be-required-if-a-customer-is-currently-using-the-human-resources-module"></a>Jaká migrace bude vyžadována, pokud zákazník aktuálně používá modul Human Resources?

Zákazníci, kteří používají modul **Human Resources**, budou mít nové funkce z Dynamics 365 Human Resources aplikovány na prostředí prostřednictvím standardního procesu aktualizace One Version. Zákazníci mohou očekávat, že se nová funkce v prostředí zobrazí, jakmile bude k dispozici v každé aktualizaci. Zákazníci mohou k aktivaci funkcí použít správu funkcí. Zákazníci by si měli naplánovat ověření těchto nových funkcí pomocí procesů, které již mají zavedeny a které používají k ověření dalších aktualizací svého prostředí.

## <a name="what-will-happen-to-custom-integrations-to-external-systems"></a>Co se stane s vlastní integrací do externích systémů?

Zákazníci budou muset migrovat své integrace do finančního a provozního prostředí. Protože koncový bod tohoto prostředí je odlišný, zákazníci možná budou muset aktualizovat nebo změnit integrace tak, aby ukazovaly na nové prostředí. Tento úkol bude primárně ruční proces a požadované změny budou záviset na architektuře integrace. Zákazníci by měli spolupracovat se svým partnerem Microsoft, aby určili nejlepší přístup k přesunu integrací.

## <a name="what-will-happen-to-microsoft-power-platform-dataverse-extensions-if-customers-merge-a-dynamics-365-human-resources-environment-with-an-existing-finance-and-operations-environment"></a>Co se stane s rozšířeními Microsoft Power Platform (Dataverse), pokud zákazníci sloučí prostředí Dynamics 365 Human Resources se stávajícím finančním a provozním prostředím?

Pokud se zákazníci rozhodnou sloučit prostředí Dynamics 365 Human Resources a stávající finanční a provozní prostředí do jediné instance Dataverse po migraci, jejich prostředí Dataverse musí být kombinována jako součást procesu sloučení. Tento úkol bude vyžadovat, aby byly všechny aplikace vytvořené pomocí Power Apps a všechna další přizpůsobení, znovu nasazeny v novém prostředí.

## <a name="what-will-happen-to-documents-during-the-migration"></a>Co se stane s dokumenty během migrace?

Když zákazníci migrují prostředí Dynamics 365 Human Resources do finanční a provozní infrastruktury, dokumenty zůstanou ve stávajícím úložišti dokumentů a budou automaticky mapovány do nového prostředí ve finanční a provozní infrastruktuře.

V budoucí verzi budou poskytnuty nové datové entity. Po provedení této změny zákazníci, kteří se rozhodnou sloučit prostředí Dynamics 365 Human Resources se stávajícím finančním a provozním prostředím, pak budou moci exportovat dokumenty a přesunout je do stávajícího prostředí.

## <a name="after-the-migration-what-happens-to-the-batch-jobs-that-were-configured-in-dynamics-365-human-resources"></a>Co se stane s dávkovými úlohami, které byly nakonfigurovány v Dynamics 365 Human Resources, po migraci?

Dávkové úlohy bude nutné překonfigurovat ve finančním a provozním prostředí. Zákazníci budou muset vyhodnotit každou dávkovou úlohu a porovnat ji s aktuálním seznamem dávkových úloh ve finančním a provozním prostředí. Zákazníci by také měli analyzovat celkový plán dávek, když sloučí dvě sady dávkových úloh, aby určili, zda by měly být provedeny změny v plánu dávek, prioritách nebo skupinách dávek.

## <a name="how-will-the-migration-affect-the-lcs-project-for-dynamics-365-human-resources"></a>Jak ovlivní migrace můj projekt LCS pro Dynamics 365 Human Resources?

Zákazníci budou muset vytvořit nový projekt Microsoft Dynamics Lifecycle Service (LCS) a budou muset vybrat finanční a provozní aplikace jako produkt a **Implementace** jako typ projektu. Při vytvoření projektu LCS je navíc k dispozici nové pole pro typ dílčího projektu. Zákazníci si budou muset vybrat možnost pro migraci Dynamics 365 Human Resources za účelem migrace stávajícího projektu Human Resources LCS do finanční a provozní infrastruktury.

Vlastnosti finančních a provozních projektů LCS se liší od rysů projektů Human Resources LCS.

Aby byli noví zákazníci spuštěni, budou muset splnit následující úkoly:

- Provést onboarding projektu.
- Provést metodiku.
- Vyplnit nástroj pro posouzení předplatného.
- Dokončit proces připravenosti ke spuštění.

## <a name="how-will-the-business-process-modeler-be-migrated"></a>Jak bude Modelování podnikových procesů migrováno?

Zákazníci budou muset exportovat svou knihovnu modelování podnikových procesů z projektu Human Resources LCS a importovat ji do projektu LCS financí a provozu. Zákazníci navíc budou muset aktualizovat nastavení nápovědy v aplikaci tak, aby ukazovala na nový projekt LCS.

## <a name="how-will-the-service-update-process-be-affected-by-the-migration"></a>Jak ovlivní migrace proces aktualizace služby?

Po migraci budou mít zákazníci mnohem větší flexibilitu, pokud jde o správu životního cyklu aplikace (ALM) a aktualizaci služeb. Aktualizace služeb již nebudou automaticky použity v prostředích Human Resources. Místo toho se služba bude řídit procesy a funkcemi aktualizace služby One Version a budou povoleny možnosti konfigurace pro aktualizace prostřednictvím LCS.

## <a name="will-customers-be-eligible-for-fasttrack-assistance-with-the-infrastructure-merge"></a>Budou mít zákazníci nárok na pomoc FastTrack se sloučením infrastruktury?

Microsoft stále definuje, jaké nástroje a zdroje budou dostupné z FastTrack, aby pomohly se sloučením.

## <a name="licensing-impact"></a>Dopad licencování

Další informace o ovlivnění licencí viz [Časté dotazy o sloučení infrastruktury Dynamics 365 Human Resources](hr-infrastructure-merge-faq.md#licensing-impact).
