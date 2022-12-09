---
title: Odstraněné nebo zastaralé funkce platformy
description: Tento článek popisuje funkce, které byly odebrány nebo u nichž se plánuje odstranění z aktualizací platformy finančních a provozních aplikací.
author: sericks007
ms.date: 08/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2020-02-29
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 6283e07b87dc169d3cbaa71a371839ab9b2d6150
ms.sourcegitcommit: ee13b854cbd52a3aa33e2449a296aed775862594
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/21/2022
ms.locfileid: "9799029"
---
# <a name="removed-or-deprecated-platform-features"></a>Odstraněné nebo zastaralé funkce platformy

[!include [banner](../includes/banner.md)]

Tento článek popisuje funkce, které byly odebrány nebo u nichž se plánuje odstranění z aktualizací platformy finančních a provozních aplikací.

- *Odstraněná* funkce již není k dispozici v produktu.
- *Zastaralá* funkce není v aktivním nasazení a v budoucí aktualizaci může být odstraněna.

Tento seznam je určen k tomu, aby vám pomohl zvážit tyto odstraněné a zastaralé funkce při svém plánování. 

Podrobné informace o objektech v finančních a provozních aplikacích lze nalézt v části [Sestavy technických informací](/dynamics/s-e/global/axtechrefrep_61). Můžete srovnat různé verze těchto sestav a zjistíte, které objekty se změnily nebo byly odstraněny v každé z verzí finančních a provozních aplikací.

## <a name="feature-deprecation-effective-august-2022"></a>Oznámení o ukončení podpory funkce od srpna 2022

### <a name="lifecycle-services-lcs-features-deprecated-in-august-2022"></a>Funkce Lifecycle Services (LCS) byly ukončeny v srpnu 2022

Jako součást pracovního úsilí [platformy One Dynamics One](/dynamics365-release-plan/2022wave2/finance-operations/finance-operations-crossapp-capabilities/one-dynamics-one-platform) jsou následující funkce LCS zastaralé.

| Název funkce | Používá se s AX 2012? | Používá se s finančními a provozními aplikacemi? | Nahrazeno jinou funkcí? |
|--------------|--------------------|----------------------------------------|------------------------------|
| Hlášení | Ano | Ano | Ano: Na stránkách jednotlivých projektů a prostředí existují bannery pro upozornění. |
| Správce konfigurace | Ano | Číslo | Číslo |
| Analýza výpisu stavu systému | Ano | Číslo | Číslo |
| Zpětná vazba a chyby | Ano | Ano | Číslo |
| Moje předplatné | Ano | Ano | Číslo |
| Office 365 | Ano | Ano | Ano: Portál pro správu Azure Active Directory nebo Microsoft. |
| Analýza dopadů | Číslo | Ano | Číslo |
| Odhad celkového ekonomického dopadu | Číslo | Ano | Číslo |
| Servisní požadavky | Číslo | Ano | Ano: [Samoobslužná nasazení](../deployment/infrastructure-stack.md) |
| Integrace SharePoint | Ano | Ano | Číslo |
| Správce konfigurace a dat | Číslo | Ano | Číslo |
| Datové balíčky procesu | Číslo | Ano | Ano: [Platforma importu a exportu dat (DIXF)](/dynamics365/fin-ops-core/dev-itpro/data-entities/data-import-export-job) |
| Upgrade prostředí | Číslo | Ano | Ano: Jsou k dispozici aktualizace služby [Jedna verze](../lifecycle-services/oneversion-overview.md). |
| Odhad infrastruktury | Ano | Číslo | Číslo |
| Stanovení velikosti licence | Ano | Číslo | Číslo |
| Analýza rozsahu užívání | Ano | Číslo | Číslo |
| Analýza úprav | Ano | Číslo | Číslo |
| Diagnostika systému | Ano | Ano | Číslo |
| Správa Visio k modelování podnikových procesů | Ano | Ano | Číslo |
| Správa cloudového prostředí AX 2012 | Ano | Číslo | Číslo |
| Konektory RDFE Azure | Ano | Ano | Číslo |
| Verze AX 2012 | Ano | Číslo | Číslo |
| Pracovní položky uložené v úložišti LCS | Ano | Ano | Číslo |
| Požadavky na opravu hotfix | Ano | Ano | Číslo |


### <a name="transport-layer-security-tls-rsa-cipher-suites"></a>Šifrovací sady RSA Transport Layer Security (TLS)

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Abychom vyhověli našim aktuálním bezpečnostním protokolům, odstraňujeme následující seznam šifrovacích sad.<br><br>TLS_RSA_WITH_AES_256_GCM_SHA384<br>TLS_RSA_WITH_AES_128_GCM_SHA256<br>TLS_RSA_WITH_AES_256_CBC_SHA256<br>TLS_RSA_WITH_AES_128_CBC_SHA256<br>TLS_RSA_WITH_AES_256_CBC_SHA<br>TLS_RSA_WITH_AES_256_CBC_SHA  |
| **Nahrazeno jinou funkcí?**   | Od ledna 2023 mohou zákazníci využívat pouze naše [standardní šifrovací sady](/power-platform/admin/server-cipher-tls-requirements). Tato změna ovlivní vaše klienty a servery, které komunikují s našimi servery, například může mít dopad na vaše integrace třetích stran, které nejsou v souladu s našimi standardními šifrovacími sadami. |
| **Ovlivněné oblasti produktu**         | Finanční a provozní aplikace |
| **Možnost nasazení**              | Nasazení v cloudu |
| **Stav**                         | Zastaralé. Zákazníci musí upgradovat své servery do ledna 2023. Další informace o konfiguraci pořadí šifrovací sady TLS viz [Správa Transport Layer Security (TLS)](/windows-server/security/tls/manage-tls).  |


## <a name="feature-deprecation-effective-june-2022"></a>Oznámení o ukončení podpory funkce od června 2022

### <a name="finance-and-operations-dynamics-365-mobile-application-and-mobile-platform"></a>Finanční a provozní mobilní aplikace (Dynamics 365) a mobilní platforma 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Ukončujeme podporu finanční a provozní mobilní aplikace (Dynamics 365) a příslušné platformy za účelem konsolidace do jediné mobilní platformy, kterou je Power Apps. |
| **Nahrazeno jinou funkcí?**   | Ano, mobilní prostředí s daty finanční a provozní aplikace lze sestavit pomocí integrace Power Platform. Více podrobností najdete v tomto [blogovém příspěvku](https://cloudblogs.microsoft.com/dynamics365/it/2022/06/03/finance-and-operations-dynamics-365-mobile-app-to-be-deprecated/) a článku [Vytváření mobilních prostředí](../power-platform/build-mobile-experiences.md). |
| **Ovlivněné oblasti produktu**         | Finanční a provozní aplikace |
| **Možnost nasazení**              | Vše |
| **Stav**                         | Zastaralé. Datum ukončení podpory je plánováno na říjen 2024. |


## <a name="platform-updates-for-version-10029-of-finance-and-operations-apps"></a>Aktualizace platformy pro verze 10.0.29 finančních a provozních aplikací

### <a name="panorama-tab-style"></a>Styl karty Panorama

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Vodorovně se posouvající stránky se zarovnávají podle zastaralých vzorů rozložení, které mají známé problémy s použitelností a přístupností.  |
| **Nahrazeno jinou funkcí?**   | Ne, ale jiné styly karet jsou stále k dispozici. |
| **Ovlivněné oblasti produktu**         | Webový klient |
| **Možnost nasazení**              | Vše |
| **Stav**                         | Zastaralé. |


## <a name="feature-deprecation-effective-april-2022"></a>Oznámení o ukončení podpory funkce od dubna 2022

### <a name="xml-url-resolution-in-data-management"></a>Rozlišení URL XML ve správě dat 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Odstraňujeme podporu pro rozlišení URL XML, protože to bylo identifikováno jako potenciální bezpečnostní chyba. To znamená, že externí zdroje přidružené k souborům XML již nebudou řešeny.  |
| **Nahrazeno jinou funkcí?**   | Číslo |
| **Ovlivněné oblasti produktu**         | Finanční a provozní aplikace |
| **Možnost nasazení**              | Vše |
| **Stav**                         | Zastaralé. |

## <a name="feature-deprecation-effective-march-14-2022"></a>Oznámení o ukončení podpory funkce od 14. května 2022

### <a name="xslt-scripting-in-data-management"></a>Skriptování XSLT ve Správě dat

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Podpora skriptování XSLT ve Správě dat je označena jako zastaralá, aby se zlepšilo zabezpečení a ochrana dat ve finančních a provozních aplikacích.  |
| **Nahrazeno jinou funkcí?**   | Číslo Zákazníci a nezávislí dodavatelé softwaru by měli zvážit opětovnou implementaci svých řešení založených na jazyce X++ namísto skriptování XSLT. |
| **Ovlivněné oblasti produktu**         | Finanční a provozní aplikace |
| **Možnost nasazení**              | Vše |
| **Stav**                         | Zastaralé <br><br>**Výjimka:** Zákazníci, kteří aktuálně používají skriptování XLST. Mohou jej nadále používat, dokud neaktualizují na verzi 10.0.30 nebo novější. Pro dřívější verze platnost výjimky vyprší 31. ledna 2023. Zákazníci s touto výjimkou obdrželi upozornění v Centru zpráv dostupném v Centru pro správu Microsoft 365. |

## <a name="feature-removal-effective-october-2021"></a>Odstranění funkce platné od října 2021

### <a name="microsoft-azure-sql-reports-in-lifecycle-services-lcs"></a>Sestavy Microsoft Azure SQL ve službě Lifecycle Services (LCS)

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Všechny aktivity a monitorování budou prováděny interně, podle platformy a prostřednictvím automatizace. Nebude vyžadován žádný ruční zásah.|
| **Nahrazeno jinou funkcí?**   | Ano, nyní existuje automatizovaný systém, který činí tyto funkce zastaralými. |
| **Ovlivněné oblasti produktu**         | Sestavy SQL: Current DTU, Current DTU Details, Get Lock Details, List of Current Plan Guide, Get List of Query ID’s, Get the SQL query plan for a given Plan ID, Get query plans and execution status, Get throttle config, Get wait stats, List most expensive queries |
| **Možnost nasazení**              | Nasazení v cloudu: Ovlivňuje provozní prostředí spravovaná společností Microsoft a prostředí sandbox Tier 2 až Tier 5. |
| **Stav**                         | Odebráno |

### <a name="azure-sql-actions-in-lcs"></a>Akce Azure SQL v LCS

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | V LCS ukončujeme podporu některých akcí SQL. Všechny aktivity a monitorování budou prováděny interně, podle platformy a prostřednictvím automatizace. Nebude vyžadován žádný ruční zásah. |
| **Nahrazeno jinou funkcí?**   | Ano, nyní existuje automatizovaný systém, který činí tyto funkce zastaralými. |
| **Ovlivněné oblasti produktu**         | Akce SQL: Create a plan guide to force Plan ID, Create a plan guide to add table hints, Remove Plan guide, Disable/Enable page locks and lock escalation, Update statistics on a table, Rebuild Index, Create Index |
| **Možnost nasazení**              | Nasazení v cloudu: Ovlivňuje provozní prostředí spravovaná společností Microsoft a prostředí sandbox Tier 2 až Tier 5. |
| **Stav**                         | Odebráno |


## <a name="feature-deprecation-effective-october-2021"></a>Oznámení o ukončení podpory funkce od října 2021

### <a name="show-related-document-attachments-feature"></a>Funkce „Zobrazit přílohy souvisejících dokumentů“

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Funkce vracela neočekávané výsledky. |
| **Nahrazeno jinou funkcí?**   | Ne. Jakékoli další plány týkající se této funkce budou sděleny prostřednictvím našeho standardního procesu zveřejnění vlny vydání. |
| **Ovlivněné oblasti produktu**         | Webový klient – prostředí s přílohami dokumentů |
| **Možnost nasazení**              | Vše |
| **Stav**                         | Zastaralé  |

## <a name="platform-updates-for-version-10023-of-finance-and-operations-apps"></a>Aktualizace platformy pro verze 10.0.23 finančních a provozních aplikací

### <a name="ondbsynchronize-event"></a>Událost OnDBSynchronize

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Neexistuje žádný ovládací prvek pro provedení této události. |
| **Nahrazeno jinou funkcí?**   | Ano, přesuňte stávající přihlášené metody událostí **OnDBSynchronize** do rozšířené třídy SysSetup. |
| **Ovlivněné oblasti produktu**         | Synchronizace databáze |
| **Možnost nasazení**              | Vše |
| **Stav**                         | Zastaralé. Plánované datum odstranění je říjen 2022. |


### <a name="systemnotificationsmanageraddnotification-api"></a>SystemNotificationsManager.AddNotification API

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Microsoft vyžaduje další parametry při přidávání oznámení. |
| **Nahrazeno jinou funkcí?**   | Ano, API **SystemNotificationsManager.AddSystemNotification()**. Toto rozhraní API vyžaduje, abyste pro generovaná oznámení explicitně nastavili ExpirationDateTime a RuleID. |
| **Ovlivněné oblasti produktu**         | Webový klient |
| **Možnost nasazení**              | Vše |
| **Stav**                         | Zastaralé. Plánované datum odstranění je duben 2023. |

## <a name="platform-updates-for-version-10021-of-finance-and-operations-apps"></a>Aktualizace platformy pro verze 10.0.21 finančních a provozních aplikací

### <a name="skype-for-business-online-support"></a>Podpora aplikace Online Skype pro firmy

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Online Skype pro firmy byl vyřazen. Další informace najdete v tématu [Služba Online Skype pro firmy byla vyřazena](https://techcommunity.microsoft.com/t5/microsoft-teams-blog/the-skype-for-business-online-service-has-retired/ba-p/2596601). |
| **Nahrazeno jinou funkcí?**   | Aktuálně ne, i když v budoucnu můžeme zvážit přidání přítomnosti z Teams.|
| **Ovlivněné oblasti produktu**         | Webový klient |
| **Možnost nasazení**              | Vše |
| **Stav**                         | Zastaralé. Nastavení **Skype povolen** bylo od vydání 10.0.21 vypnuto. Odstranění tohoto nastavení je naplánováno na duben 2022; tato funkce však přestane fungovat poté, co tým Skype službu vypne. |
 
## <a name="feature-deprecation-effective-august-2021"></a>Oznámení o ukončení podpory funkce od srpna 2021

### <a name="microsoft-azure-sql-reports-in-lifecycle-services-lcs"></a>Sestavy Microsoft Azure SQL ve službě Lifecycle Services (LCS)

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Všechny aktivity a monitorování budou prováděny interně, podle platformy a prostřednictvím automatizace. Nebude vyžadován žádný ruční zásah.|
| **Nahrazeno jinou funkcí?**   | Ano, nyní existuje automatizovaný systém, který činí tyto funkce zastaralými. |
| **Ovlivněné oblasti produktu**         | Sestavy SQL: Current DTU, Current DTU Details, Get Lock Details, List of Current Plan Guide, Get List of Query ID’s, Get the SQL query plan for a given Plan ID, Get query plans and execution status, Get throttle config, Get wait stats, List most expensive queries |
| **Možnost nasazení**              | Nasazení v cloudu: Ovlivňuje provozní prostředí spravovaná společností Microsoft a prostředí sandbox Tier 2 až Tier 5. |
| **Stav**                         | Zastaralé: Plánované datum odstranění v říjnu 2021. |

### <a name="azure-sql-actions-in-lcs"></a>Akce Azure SQL v LCS

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | V LCS ukončujeme podporu některých akcí SQL. Všechny aktivity a monitorování budou prováděny interně, podle platformy a prostřednictvím automatizace. Nebude vyžadován žádný ruční zásah. |
| **Nahrazeno jinou funkcí?**   | Ano, nyní existuje automatizovaný systém, který činí tyto funkce zastaralými. |
| **Ovlivněné oblasti produktu**         | Akce SQL: Create a plan guide to force Plan ID, Create a plan guide to add table hints, Remove Plan guide, Disable/Enable page locks and lock escalation, Update statistics on a table, Rebuild Index, Create Index |
| **Možnost nasazení**              | Nasazení v cloudu: Ovlivňuje provozní prostředí spravovaná společností Microsoft a prostředí sandbox Tier 2 až Tier 5. |
| **Stav**                         | Zastaralé: Plánované datum odstranění v říjnu 2021. |

## <a name="feature-deprecation-effective-may-2021"></a>Oznámení o ukončení podpory funkce od května 2021

### <a name="globalization-portal-in-lifecycle-services-lcs"></a>Portál globalizace Lifecycle Services (LCS)

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Ukončujeme podporu portálu globalizace v LCS, protože tuto funkci nahradily další služby založené na LCS. |
| **Nahrazeno jinou funkcí?**   | Ano, tato funkce je nahrazena funkcemi LCS [Hledání problému](../lifecycle-services/issue-search-lcs.md) a [Služba odesílání regulačních výstrah Dynamics](../lcs-solutions/submit-localization-alerts.md). |
| **Ovlivněné oblasti produktu**         | Portál globalizace v LCS|
| **Možnost nasazení**              | Cloudové nasazení |
| **Stav**                         | Zastaralé: Plánované datum odstranění v květnu 2022. |


## <a name="feature-removed-effective-january-28-2021"></a>Funkce odstraněna s účinností od 28. ledna 2021

### <a name="batch-job-to-handle-sql-index-defragmentation"></a>Dávková úloha pro zpracování defragmentace SQL indexu

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Abychom snížili režii provozu, monitorování a údržby správy indexu zákazníky, byla tato funkce odstraněna. |
| **Nahrazeno jinou funkcí?**   | Do budoucna budou údržbu indexu provádět služby společnosti Microsoft. K tomu bude docházet nepřetržitě, aniž by to ovlivnilo pracovní vytížení uživatele. |
| **Ovlivněné oblasti produktu**         | Finanční a provozní aplikace|
| **Možnost nasazení**              | Nasazení v cloudu - ovlivňuje provozní prostředí spravovaná společností Microsoft a prostředí sandbox Tier 2 až Tier 5. |
| **Stav**                         | Tato funkce byla odstraněna. |


## <a name="platform-updates-for-version-10017-of-finance-and-operations-apps"></a>Aktualizace platformy pro verze 10.0.17 finančních a provozních aplikací


### <a name="visual-studio-2015"></a>Visual Studio 2015

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Chcete-li podporovat nejnovější verze Visual Studio, je třeba provést určité změny v rozšířeních X ++ pro Visual Studio. Tyto změny nejsou kompatibilní s Visual Studio 2015. |
| **Nahrazeno jinou funkcí?**   | Visual Studio 2017 nahradí Visual Studio 2015 jako nasazená a požadovaná verze. |
| **Ovlivněné oblasti produktu**         | Vývojové nástroje Visual Studio |
| **Možnost nasazení**              | Vše |
| **Stav**                         | Zastaralé: Po aktualizaci budou předchozí nástroje X++ odebrány z Visual Studio 2015 a aktualizované nástroje se nebudou instalovat ve Visual Studio 2015. Na hostovaná sestavení to nemá žádný dopad. U sestavování virtuálních počítačů je nutné ručně aktualizovat kanál sestavení (definice sestavení), aby se změnila závislost z MSBuild 14.0 (Visual Studio 2015) na MSBuild 15.0 (Visual Studio 2017), jak je popsáno v části [Aktualizace staršího kanálu v Azure Pipelines](../dev-tools/pipeline-msbuild-update.md). |

### <a name="user-avatar"></a>Uživatelský avatar 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Avatar uživatele, který se zobrazuje na pravé straně navigačního panelu, byl načten pomocí rozhraní API z ovládacího prvku záhlaví Dynamics 365, jehož podpora byla ukončena. |
| **Nahrazeno jinou funkcí?**   | Uživatelé místo toho uvidí své iniciály v kruhu na navigačním panelu. Toto je stejný vizuál, jaký se aktuálně používá na vývojových počítačích. |
| **Ovlivněné oblasti produktu**         | Webový klient |
| **Možnost nasazení**              | Vše |
| **Stav**                         | Odstraněno od verze 10.0.17. |

### <a name="enterprise-portal-ep-deprecation"></a>Ukončení podpory portálu Enterprise (EP)  

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Artefakty metadat spojené s Dynamics AX 2012 Enterprise Portal (EP) byly vyřazeny, protože finanční a provozní aplikace nikdy nepodporovaly EP. |
| **Nahrazeno jinou funkcí?**   | Číslo |
| **Ovlivněné oblasti produktu**         | Webový klient |
| **Možnost nasazení**              | Vše |
| **Stav**                         | Zastaralé: Ve vydání z října 2021 je naplánováno odstranění všech kódů EP. |

## <a name="deprecation-effective-december-2020"></a>Oznámení o ukončení podpory od prosince 2020

### <a name="internet-explorer-11-support-for-dynamics-365-is-deprecated"></a>Podpora aplikace Internet Explorer 11 pro Dynamics 365 je zastaralá

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | S platností od prosince 2020 je aplikace Microsoft Internet Explorer 11 označena jako zastaralá u všech produktů Dynamics 365 Dynamics Lifecycle Services (LCS) a Internet Explorer 11 nebude po srpnu 2021 podporován.<br><br>To bude mít dopad na zákazníky, kteří používají produkty Dynamics 365 a LCS, které jsou navrženy pro použití prostřednictvím rozhraní Internet Explorer 11. Po srpnu 2021 nebude Internet Explorer 11 podporován pro takové produkty Dynamics 365 a LCS. |
| **Nahrazeno jinou funkcí?**   | Doporučujeme zákazníkům přejít na Microsoft Edge.|
| **Ovlivněné oblasti produktu**         | Všechny produkty Dynamics 365 a LCS |
| **Možnost nasazení**              | Vše|
| **Stav**                         | Zastaralé: Internet Explorer 11 nebude podporován po srpnu 2021.|

## <a name="platform-updates-for-version-10015-of-finance-and-operations-apps"></a>Aktualizace platformy pro verze 10.0.15 finančních a provozních aplikací

### <a name="visual-studio-add-in-to-apply-metadata-hotfixes"></a>Doplněk sady Visual Studio pro použití oprav hotfix metadat

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Opravy hotfix metadat už nejsou podporovány u aktualizací služeb [One Version](../../fin-ops/get-started/one-version.md), které byly zavedeny v červenci 2018 s verzí 8.1. |
| **Nahrazeno jinou funkcí?**   | Pro podporované verze nejsou k dispozici jednotlivé opravy hotfix metadat. Místo toho se použijí kumulativní aktualizace pro zvýšení kvality. |
| **Ovlivněné oblasti produktu**         | Doplňky sady Visual Studio |
| **Možnost nasazení**              | Virtuální počítae pro vývoj |
| **Stav**                         | Od verzei 10.0.15 už tento doplněk není součástí nástrojů sady Visual Studio. |


## <a name="platform-updates-for-version-10014-of-finance-and-operations-apps"></a>Aktualizace platformy pro verze 10.0.14 finančních a provozních aplikací

### <a name="online-users-page"></a>Stránka online uživatelů 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Toto je starší stránka, která byla vytvořena pro předchozí architekturu klient/server. Informace na této stránce nejsou vždy přesné, což může být matoucí a zavádějící. |
| **Nahrazeno jinou funkcí?**   | V budoucí aktualizaci poskytneme novou stránku.|
| **Ovlivněné oblasti produktu**         | Správa systému |
| **Možnost nasazení**              | Vše |
| **Stav**                         | Do října 2021 bude tento formulář odstraněn.   |


## <a name="platform-updates-for-version-10013-of-finance-and-operations-apps"></a>Aktualizace platformy pro verze 10.0.13 finančních a provozních aplikací


### <a name="custom-code-defined-in-ssrs-report-properties"></a>Vlastní kód definovaný ve vlastnostech sestavy SSRS 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Obecně lze říci, že vlastní kód nabízí omezené výhody a zároveň vyžaduje značné zdroje a podporu pro výpočet. Vlastní kód je primárně používán autory sestav k volání veřejných metod z vlastní sestavy kódu. Služba hostovaná v cloudu však nepodporuje odkazy na vlastní sestavení pro zprávy SSRS. |
| **Nahrazeno jinou funkcí?**   | Autoři sestav se mohou rozhodnout pokračovat v odkazování na veřejná rozhraní .NET API pro operace Math, Převod a Formát z libovolného výrazu textového pole. Další informace naleznete v tématu [Přidání kódu do sestavy (SSRS)](/sql/reporting-services/report-design/add-code-to-a-report-ssrs).  |
| **Ovlivněné oblasti produktu**         | Podmnožina návrhů sestav aplikací definovaných v RDL, kterě obsahují vlastní kód. |
| **Možnost nasazení**              | Vše |
| **Stav**                         | U verzí novějších než 10.0.13 kompilátor začne vydávat varování pro případy, kdy je v definici sestavy SSRS detekován vlastní kód. Chcete-li problém vyřešit, otevřete definici návrhu sestavy a odeberte všechny artefakty vlastního kódu. Toto varování bude v budoucí aktualizaci nahrazeno chybou kompilátoru.   |

### <a name="upgrade-of-three-jquery-component-libraries"></a>Upgrade tří knihoven komponent jQuery 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Jsou aktualizovány tři knihovny komponent jQuery pro opravy zabezpečení a udržování měny.   
| **Nahrazeno jinou funkcí?**   | Ovlivněny jsou následující knihovny: jQuery (do verze 3.5.0 od verze 2.1.4), jQuery UI (do verze 1.12.1 od verze 1.11.4), jQuery qTip (do verze 3.0.3 od verze 2.2.1). Pokyny pro migraci poskytuje online jQuery.  |
| **Ovlivněné oblasti produktu**         | Rozšiřitelné ovládací prvky, konkrétně vlastní kód JavaScript využívající zastaralá nebo odstraněná rozhraní API. |
| **Možnost nasazení**              | Vše |
| **Stav**                         | V aktualzaci 10.0.13/Platform update 37 mohou zákazníci volitelně přecházet k nejnovějším knihovnám povolením funkce Upgradovat tři knihovny komponent jQuery. Přechod na nové knihovny bude povinný s vydáním z dubna 2021, aby byl k dispozici čas na migraci příslušných rozhraní API.   |

### <a name="existing-grid-controlforcelegacygrid-api"></a>Existující API pro ovládací prvek mřížky / forceLegacyGrid ()

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Stávající ovládací prvek mřížky se nahrazuje novým ovládacím prvkem mřížky. |
| **Nahrazeno jinou funkcí?**   | [Nový ovládací prvek mřížky](../..//fin-ops/get-started/grid-capabilities.md) |
| **Ovlivněné oblasti produktu**         | Webový klient |
| **Možnost nasazení**              | Vše |
| **Stav**                         | Ve verzi 10.0.13 je nový ovládací prvek mřížky obecně k dispozici a zákazníci mohou tuto funkci volitelně zapnout. Nové řízení mřížky bude ve výchozím nastavení zapnuto ve vydáním z října 2021 a v současné době je cílené tak, aby bylo povinné v dubnu 2022. Jakmile bude nový ovládací prvek mřížky povinný, rozhraní API **forceLegacyGrid()** přestane být respektováno. |

### <a name="personalization-without-saved-views"></a>Přizpůsobení bez uložených pohledů 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Podsystém personalizace byl přepracován funkcí uložených pohledů, takže má lepší výkon a nabízí další možnosti. |
| **Nahrazeno jinou funkcí?**   | Uložená zobrazení |
| **Ovlivněné oblasti produktu**         | Webový klient |
| **Možnost nasazení**              | Vše |
| **Stav**                         | Ve verzi 10.0.13 / Platform Update 37 je funkce uložených pohledů obecně k dispozici a zákazníci ji mohou volitelně zapnout. Funkce uložených pohledů začne být povinný od vydání z října 2021. |


## <a name="platform-updates-for-version-10012-of-finance-and-operations-apps"></a>Aktualizace platformy pro verze 10.0.12 finančních a provozních aplikací

### <a name="grid-or-group-control-form-extensions-containing-invalid-field-references"></a>Rozšíření formuláře ovládacího prvku mřížky nebo skupiny obsahující neplatné odkazy na pole

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Vlastnost datové skupiny v mřížce nebo skupinových ovládacích prvcích se používá k automatickému zobrazení všech polí skupiny polí. Ovládací prvek mřížky nebo skupiny přidaný pomocí rozšíření může obsahovat pole, která již nejsou definována ve skupině polí, nebo to mohou být chybějící pole, která jsou definována ve skupině polí. To může způsobit nekonzistentní chování za běhu. Aktualizace platformy pro verze 10.0.12 finančních a provozních aplikací nyní kategorizují tento problém jako *varování* kompilátoru. Chcete-li tento problém vyřešit, otevřete rozšíření formuláře a uložte je.
| **Nahrazeno jinou funkcí?**   | Toto varování kompilátoru bude v budoucí aktualizaci nahrazeno chybou kompilátoru. |
| **Ovlivněné oblasti produktu**         | Vývojové nástroje Visual Studio |
| **Možnost nasazení**              | Vše |
| **Stav**                         | Varování kompilátoru je chybou kompilátoru v aktualizacích platformy pro verze 10.0.12 finančních a provozních aplikací. |

## <a name="platform-updates-for-version-10011-of-finance-and-operations-apps"></a>Aktualizace platformy pro verze 10.0.11 finančních a provozních aplikací

### <a name="explicit-safe-lists-for-self-service-environments"></a>Explicitní bezpečné seznamy pro samoobslužná prostředí

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Proces přesunu IP do bezpečných seznamů se změnil. Samoobsluha již nepodporuje bezpečné seznamy IP. |
| **Nahrazeno jinou funkcí?**   | Další informace získáte v tématu [Konfigurace podmíněného přístupu Azure Active Directory](/appcenter/general/configuring-aad-conditional-access).|
| **Ovlivněné oblasti produktu**         | Zabezpečení |
| **Možnost nasazení**              | Cloud |
| **Stav**                         | Zastaralé: Tato funkce je plně zastaralá pro samoobslužná nasazení. |

### <a name="visual-studio-2015"></a>Visual Studio 2015

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Chcete-li podporovat nejnovější verze Visual Studio, je třeba provést určité změny v rozšířeních X ++ pro Visual Studio. Tyto změny nejsou kompatibilní s Visual Studio 2015. |
| **Nahrazeno jinou funkcí?**   | Visual Studio 2017 nahradí Visual Studio 2015 jako nasazená a požadovaná verze. |
| **Ovlivněné oblasti produktu**         | Vývojové nástroje Visual Studio |
| **Možnost nasazení**              | Vše |
| **Stav**                         | Virtuální počítače nasazené na verzi 10.0.13 (Platform update 37) nebo novější obsahují Visual Studio 2017. Verze 10.0.16 (Platform update 40) je finální vydání s podporou pro Visual Studio 2015. Virtuální stroje pouze s verzí Visual Studio 2015 nebude možné aktualizovat na verzi 10.0.17 (Platform update 41). |

### <a name="field-groups-containing-invalid-field-references"></a>Skupiny polí obsahující neplatné odkazy na pole

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Skupiny polí v definicích metadat tabulky mohou obsahovat odkazy na pole, které nejsou platné. Při nasazení těchto skupin polí to může způsobit chyby runtime ve Financial Reporting a Microsoft SQL Server Reporting Services (SSRS). Aktualizace platformy 23 zavedla *upozornění* kompilátoru, které umožnilo adresovat tento problém s metadaty. Aktualizace platformy pro verze 10.0.11 finančních a provozních aplikací kategorizují tento problém jako *chybu* kompilátoru.<p>Chcete-li opravit problém, postupujte následovně.</p><ol><li>Odeberte neplatný odkaz na pole z definice skupiny pole tabulky.</li><li>Překompilujte.</li><li>Zkontrolujte, zda jsou řešeny všechny chyby.</li></ol> |
| **Nahrazeno jinou funkcí?**   | Tato chyba kompilátoru trvale nahrazuje upozornění kompilátoru.  |
| **Ovlivněné oblasti produktu**         | Vývojové nástroje Visual Studio |
| **Možnost nasazení**              | Vše |
| **Stav**                         | Zastaralé: Upozornění kompilátoru představuje chybu kompilátoru u aktualizací platformy pro verze 10.0.11 finančních a provozních aplikací. |

### <a name="isv-licenses-created-by-using-the-sha1-hashing-algorithm"></a>Licence ISV vytvořené pomocí algoritmu hash SHA1

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Proces vytvoření licencí nezávislého softwaru dodavatele (ISV) se změnil. Další informace naleznete v tématu [Správa licencí nezávislého dodavatele softwaru (ISV)](../dev-tools/isv-licensing.md#appendix-create-self-signed-certificates-for-test-purposes). |
| **Nahrazeno jinou funkcí?**   | Ano. Vytvoření licencí pomocí prostředí Windows PowerShell. |
| **Ovlivněné oblasti produktu**         | Vývojové nástroje Visual Studio |
| **Možnost nasazení**              | Vše |
| **Stav**                         | Zastaralé: licence ISV, které byly vytvořeny pomocí algoritmu hash SHA1. Tento algoritmus závisí na certifikátech, které byly vytvořeny pomocí nástroje MakeCert, a tento nástroj se již nepoužívá.<br><br>Zastaralé: použití algoritmu SHA1 pro účely zabezpečení nebo vytřídění. Algoritmus SHA1 přestane fungovat v na začátku roku 2021. Proto by již neměl být používán.<br><br>Odebráno: podpora pro příchozí nebo odchozí požadavky zabezpečení TLS 1.0 a TLS 1.1. |

## <a name="platform-update-32"></a>Platform update 32

### <a name="workflow-request-change-dialog-box-no-longer-includes-user-selection-drop-down-list"></a>Dialogové okno pro změnu požadavku workflowu již neobsahuje rozevírací seznam pro výběr uživatele.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Jednalo se o bezpečnostní problém, protože požadavek na změnu mohl být odeslán nežádoucímu uživateli. Šlo také o problém s využitelností, protože aplikace nutila uživatele určit, kdo je původce workflowu, a ručně jej vybrat.  |
| **Nahrazeno jinou funkcí?**   | Ne |
| **Ovlivněné oblasti produktu**         | Workflow |
| **Možnost nasazení**              | Vše |
| **Stav**                         | Rozevírací seznam pro výběr uživatelů byl odebrán z dialogového okna pro změnu požadavku v aktualizaci platformy 32. Požadavky na změnu požadavku budou automaticky odeslány původci, jak bylo zamýšleno. Další informace o této funkci naleznete v tématu [Akce v procesech schválení workflow](../../fin-ops/organization-administration/workflow-actions.md?toc=%2fdynamics365%2fcommerce%2ftoc.json#request-change). |

### <a name="embedded-drill-through-links-are-no-longer-supported-in-paginated-documents-rendered-by-the-cloud-hosted-service"></a>Vložené odkazy na procházení k podrobnostem již nejsou podporovány ve stránkovaných dokumentech vykreslených službou hostovanou v cloudu 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Adresy URL pro navigaci vložené do dokumentů vykreslených službou mohou obsahovat citlivé obchodní údaje. Odebíráme podporu vložených odkazů na procházení k podrobnostem coby bezpečnostní opatření pro další ochranu dat zákazníka. V důsledku této změny si uživatelé také užijí lepšího výkonu při interaktivním vytváření dokumentů.  |
| **Nahrazeno jinou funkcí?**   | Ne |
| **Ovlivněné oblasti produktu**         | Vykazování |
| **Možnost nasazení**              | Vše |
| **Stav**                         | Tato funkce je aktivně odebírána ze služby.<br><br>Moderní klient nabízí řadu možností pro vytváření zobrazení s automaticky generovanými odkazy, které pomáhají při navigaci v aplikaci. Stránkované dokumenty vykreslené službou jsou doporučeny pro externí sdělení, které jsou zasílány e-mailem, archivovány a vytištěny pro příjemce. Zlepšili jsme prostředí pro zobrazení náhledu dokumentů přímo v prohlížeči, které nabízí přímý přístup k místním tiskárnám. Další informace naleznete v tématu [Náhled dokumentů PDF pomocí integrovaného prohlížeče](../analytics/preview-pdf-documents.md). |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Předchozí oznámení o odebraných nebo zastaralých funkcích
Další informace o funkcích, které byly v předchozích verzích odebrány nebo zastaraly, naleznete v tématu [Odebrané nebo zastaralé funkce v předchozích verzích](../migration-upgrade/deprecated-features.md).



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

