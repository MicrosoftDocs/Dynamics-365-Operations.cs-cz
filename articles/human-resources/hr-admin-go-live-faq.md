---
title: Často kladené dotazy týkající se ostrého nasazení
description: Toto téma uvádí často kladené otázky o tom, jak převést projekt implementace Dynamics 365 Human Resources do živého provozu.
author: rachel-profitt
manager: tfehr
ms.date: 10/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c5041d515b261bb3e4b14885e0ec0ce788edf729
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/03/2021
ms.locfileid: "5111763"
---
# <a name="go-live-faq"></a>Často kladené dotazy týkající se ostrého nasazení 

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Toto téma uvádí často kladené otázky o tom, jak převést projekt implementace Dynamics 365 Human Resources do živého provozu. 

## <a name="when-can-i-configure-and-request-my-production-environment"></a>Kdy mohu nakonfigurovat a požádat o své provozní prostředí? 

Provozní prostředí je obvykle nasazeno po splnění následujících kritérií:

- Všechna přizpůsobení jsou kompletní.
- Uživatelské akceptační testování (UAT) je dokončeno.
- Zákazník se odhlásil od řešení.
- Pro spuštění nejsou žádné problémy s blokováním. 

Pokud jsou v této fázi kvalifikovaní zákazníci, tým Microsoft FastTrack bude spolupracovat s projektovým týmem, aby provedli test naživo. 

## <a name="what-are-the-prerequisites-to-deploying-a-production-environment"></a>Jaké jsou předpoklady pro nasazení produkčního prostředí? 

Seznam předpokladů najdete v části  [Připravte se na přechod do živého provozu](hr-admin-go-live-prepare.md). 

## <a name="what-is-a-go-live-assessment"></a>Co je to test naživo?  

Test naživo je součástí  [Programu Microsoft FastTrack](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/fasttrack-dynamics-365-overview). Během této kontroly architekt řešení posoudí, zda je implementační projekt připraven na úspěšné vyjmutí a spuštění. Tato kontrola je povinná pro každý implementační projekt, než budete moci požádat o uvedení do provozu v produkčním prostředí. 

## <a name="our-sandbox-environments-are-deployed-in-the-central-us-datacenter-we-want-our-production-environments-to-be-deployed-in-the-west-us-datacenter-can-i-select-west-us-as-the-datacenter-in-my-production-configuration"></a>Naše prostředí Sandbox jsou nasazena v datovém centru ve střední USA. Chceme, aby naše produkční prostředí byla nasazena v datovém centru na západě USA. Mohu ve své produkční konfiguraci vybrat jako datové centrum Západ USA? 

LCS vás neomezuje ve výběru jiného datového centra při nasazení prostředí lidských zdrojů, ale důrazně doporučujeme nevybírat jiné datové centrum.  

Pokud chcete, aby se vaše produkční prostředí nacházelo v západoamerickém datovém centru, měli byste nejprve znovu nasadit prostředí sandboxu do západoamerického datového centra, otestovat je a odhlásit se. 

Informace o výběru správného datového centra najdete v části [Síťové požadavky](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/system-requirements#network-requirements). 

## <a name="what-level-of-access-do-i-have-to-the-azure-resources-for-my-human-resources-environments"></a>Jakou úroveň přístupu mám k prostředkům Azure pro mé prostředí lidských zdrojů?  

Přístup do prostředí lidských zdrojů je omezený. Nelze získat přístup k virtuálnímu počítači (VM) nebo Microsoft Internet Information Services (IIS). Také nemůžete získat přístup k databázi prostřednictvím Microsoft SQL Server Management Studio. 

I když nemůžete získat přístup ke svým prostředkům Azure nebo prostředí Dynamics 365 Human Resources přímo, existují další funkce, které můžete použít pro přístup k vašim datům:

- Můžete nasadit databázi Azure SQL ve vašem vlastním klientovi Azure a k synchronizaci dat použít funkci Bring Your Own Database (BYOD). Další informace viz [Použití vlastní databáze (BYOD)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database).

- Můžete použít integraci Dataverse pro synchronizaci vybraných entit s databází Dataverse. Další informace naleznete v části [Tabulky Dataverse](hr-developer-entities.md). 

## <a name="how-often-is-my-production-database-backed-up"></a>Jak často je moje produkční databáze zálohována? 

Databáze jsou chráněny automatickým zálohováním na následujících frekvencích:

| Typ zálohy | Četnost |
| --- | --- |
| Úplná záloha databáze | Týdně |
| Rozdílová záloha databáze | Každých 12-24 hodin |
| Záloha protokolu transakcí | Každých 5 až 10 minut |

Microsoft si ponechává dostatečné zálohy, aby umožnil Point in Time Restore (PITR) během posledních 14 dnů. 

Další informace naleznete v tématu  [Další informace týkající se automatické zálohy databáze SQL](https://docs.microsoft.com/azure/azure-sql/database/automated-backups-overview?tabs=single-database). 

## <a name="can-i-request-a-copy-of-the-backup-of-my-production-database"></a>Mohu požádat o kopii zálohy mé produkční databáze? 

Č. Můžete však odeslat požadavek na aktualizaci databáze, abyste zkopírovali produkční prostředí do prostředí Sandbox. Můžete nasadit databázi Azure SQL ve vašem vlastním klientovi Azure a k synchronizaci dat použít funkci BYOD z vašeho provozního prostředí. Další informace viz [Použití vlastní databáze (BYOD)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database). 

## <a name="how-do-i-move-my-sandbox-environment-to-production-for-go-live"></a>Jak přesunu své prostředí Sandbox do produkce pro spuštění? 

Protože funkce kopírování není k dispozici pro přesun vašeho prostředí ze Sandbox do produkčního prostředí, musíte k přesunu dat do produkčního prostředí použít datové balíčky.  

Během celého projektu doporučujeme udržovat jasný seznam entit nakonfigurovaných ve vašem sandboxu. Poté otestujte proces vyjmutí a migrace veškerých datových balíčků potřebných k uvedení do provozu. Až budete připraveni k provozu, musíte ručně přesunout všechny datové balíčky do produkčního prostředí. 

## <a name="what-should-i-do-if-my-production-environment-is-down"></a>Co mám dělat, když je moje produkční prostředí nefunkční? 

Chcete-li nahlásit výpadek produkčního prostředí, postupujte podle postupu popsaného v [Nahlásit výpadek produkce](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/report-production-outage). 

 ## <a name="see-also"></a>Viz také

 [Příprava pro ostré nasazení](hr-admin-go-live-prepare.md)
