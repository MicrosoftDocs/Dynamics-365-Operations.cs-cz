---
title: Odstraněné nebo zastaralé funkce v aplikaci Dynamics 365 Supply Chain Management
description: Toto téma popisuje funkce, které byly odebrány nebo u nichž se plánuje odstranění v Dynamics 365 Supply Chain Management.
author: kamaybac
ms.date: 04/27/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: a7a06b5476302e43d107c448c139c235ea57b05b
ms.sourcegitcommit: 57668404d61359b33e0c0280f2f7c4eb829b1ed2
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/27/2021
ms.locfileid: "5947537"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-supply-chain-management"></a>Odstraněné nebo zastaralé funkce v aplikaci Dynamics 365 Supply Chain Management

[!include [banner](../includes/banner.md)]

Toto téma bude aktualizováno podle nově odebraných nebo zastaralých funkcí pro Dynamics 365 Supply Chain Management.

- *Odstraněná* funkce již není k dispozici v produktu.
- *Zastaralá* funkce není v aktivním nasazení a v budoucí aktualizaci může být odstraněna.

Tento seznam je určen k tomu, aby vám pomohl zvážit tyto odstraněné a zastaralé funkce při svém plánování.

> [!NOTE]
> Podrobné informace o objektech v aplikacích Finance and Operations lze nalézt v části [Sestavy technických informací](/dynamics/s-e/). Můžete srovnat různé verze těchto sestav a zjistíte, které objekty se změnily nebo byly odstraněny v každé z verzí aplikací Finance and Operations.


## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10019-release"></a>Odebrané nebo zastaralé funkce ve verzi Supply Chain Management 10.0.19

### <a name="job-card-device"></a>Zařízení úkolového lístku

|   |   |
|---|---|
| **Důvod pro zrušení/odstranění** | [Zařízení úkolového lístku](../production-control/config-job-card-device.md) je nahrazeno novým [rozhraním pro provádění výrobního provozu](../production-control/production-floor-execution-configure.md). |
| **Nahrazeno jinou funkcí?**   | Ano, [zařízení úkolového lístku](../production-control/config-job-card-device.md) je nahrazeno novým [rozhraním pro provádění výrobního provozu](../production-control/production-floor-execution-configure.md). |
| **Ovlivněné oblasti produktu** | Supply Chain Management – řízení výroby |
| **Možnost nasazení** | Cloudové a místní nasazení |
| **Stav** | Zastaralé. Zařízení úkolového lístku obdrží podporu s opravami chyb a zabezpečení, ale vylepšení funkcí již nebudou poskytována. Po dubnu 2022 již nebude zařízení úkolového lístku podporováno a zákazníci budou požádáni, aby přešli na nové rozhraní pro provádění výrobního provozu. |

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10018-release"></a>Odebrané nebo zastaralé funkce ve verzi Supply Chain Management 10.0.18

### <a name="dynamics-365-for-finance-and-operations---warehousing-the-warehouse-app"></a>Dynamics 365 for Finance and Operations – sklady (aplikace skladu)

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | S platností od dubna 2021 je aplikace *Dynamics 365 for Finance and Operations – sklady* (aplikace skladu) zastaralá a po dubnu 2022 nebude podporována. Nyní je nahrazena *mobilní aplikací Řízení skladu*, která byla vydán s verzí 10.0.17 aplikace Supply Chain Management. Nová aplikace je úplnou náhradou, ale používá stejný základní rámec, což usnadňuje migraci. V případě potřeby lze tyto dvě aplikace použít vedle sebe, aby si uživatelé postupně zvykli používat novou aplikaci.<br><br>Další informace, jak konfigurovat novou mobilní aplikaci Řízení skladu, viz témata [Mobilní aplikace Řízení skladu](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/warehouse-management-mobile-application) a [Instalace a připojení mobilní aplikace Řízení skladu](../warehousing/install-configure-warehouse-management-app.md). |
| **Nahrazeno jinou funkcí?**   | Ano, nahrazeno novou mobilní aplikací Řízení skladu. |
| **Ovlivněné oblasti produktu**         | Supply Chain Management – aplikace skladu |
| **Možnost nasazení**              | Cloudové a místní nasazení |
| **Stav**                         | Zastaralé. Aplikace skladu obdrží podporu s opravami chyb a zabezpečení, ale vylepšení funkcí již nebudou poskytována. Po dubnu 2022 již nebude stará aplikace skladu podporována a zákazníci budou požádáni, aby se přesunuli do nové mobilní aplikace Řízení skladu. Stará aplikace skladu bude poté odstraněna z obchodů Microsoft Store a Google Play.  |

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10015-release"></a>Odebrané nebo zastaralé funkce ve verzi Supply Chain Management 10.0.15

### <a name="internet-explorer-11-support-for-dynamics-365-is-deprecated"></a>Podpora aplikace Internet Explorer 11 pro Dynamics 365 je zastaralá

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | S platností od prosince 2020 je podpora aplikace Microsoft Internet Explorer 11 zastaralá pro všechny produkty Dynamics 365 a Internet Explorer 11 nebude podporován po srpnu 2021.<br><br>To bude mít dopad na zákazníky, kteří používají produkty Dynamics 365, které jsou navrženy pro použití prostřednictvím rozhraní Internet Explorer 11. Po srpnu 2021 nebude Internet Explorer 11 podporován pro takové produkty Dynamics 365. |
| **Nahrazeno jinou funkcí?**   | Doporučujeme zákazníkům přejít na Microsoft Edge.|
| **Ovlivněné oblasti produktu**         | Všechny produkty Dynamics 365 |
| **Možnost nasazení**              | Vše|
| **Stav**                         | Zastaralé. Internet Explorer 11 nebude podporován po srpnu 2021.|

### <a name="use-of-built-in-supply-chain-management-master-planning-engine-for-manufacturing-scenarios"></a>Použití integrovaného modulu hlavního plánování Supply Chain Management pro scénáře výroby

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Pro zvýšení výkonu a minimalizaci zatížení databáze SQL během hlavních plánovacích relací je vestavěný hlavní plánovací modul Supply Chain Management nahrazen optimalizací plánování. Optimalizace plánování umožňuje rychlé spouštění plánů, které lze provádět i během úředních hodin. To umožňuje plánovačům okamžitě reagovat na změny poptávky nebo parametrů plánování. |
| **Nahrazeno jinou funkcí?**   | Ano, optimalizace plánování nahradí předdefinovaný hlavní modul plánování Supply Chain Management. |
| **Ovlivněné oblasti produktu**         | Supply Chain Management - hlavní plánování |
| **Možnost nasazení**              | Pouze cloud. Všimněte si, že optimalizace plánování není podporována u místních nasazení. |
| **Stav**                         | Zastaralé. Do 1. dubna 2022 nebudou scénáře výroby dále podporovány v integrovaném modulu hlavního plánování Dynamics 365 Supply Chain Management. U výrobních scénářů musí zákazníci pro výpočet hlavního plánování použít Optimalizaci plánování. Další informace naleznete v tématu [Dokumentace optimalizace plánování](../master-planning/planning-optimization/planning-optimization-overview.md). Zákazníci s místním nasazením Dynamics 365 Supply Chain Management mohou i nadále používat hlavní plánovací modul Supply Chain Management pro scénáře výroby po dubnu 2022. Nebudou však poskytována žádná další vylepšení funkcí. |

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10011-release"></a>Odebrané nebo zastaralé funkce ve verzi Supply Chain Management 10.0.11

### <a name="use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios"></a>Použití integrovaného modulu hlavního plánování Supply Chain Management pro scénáře distribuce

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Pro zvýšení výkonu a minimalizaci zatížení databáze SQL během hlavních plánovacích relací je vestavěný hlavní plánovací modul Supply Chain Management nahrazen optimalizací plánování. Optimalizace plánování umožňuje rychlé spouštění plánů, které lze provádět i během úředních hodin. To umožňuje plánovačům okamžitě reagovat na změny poptávky nebo parametrů plánování. |
| **Nahrazeno jinou funkcí?**   | Ano, optimalizace plánování nahradí předdefinovaný hlavní modul plánování Supply Chain Management. |
| **Ovlivněné oblasti produktu**         | Supply Chain Management - hlavní plánování |
| **Možnost nasazení**              | Pouze cloud. Všimněte si, že optimalizace plánování není podporována u místních nasazení. |
| **Stav**                         | Zastaralé. Do 1 dubna 2021 nebudou scénáře distribuce dále podporovány v integrovaném modulu hlavního plánování Dynamics 365 Supply Chain Management. U distribučních scénářů musí zákazníci pro výpočet hlavního plánování použít Optimalizaci plánování. Další informace naleznete v tématu [Dokumentace optimalizace plánování](../master-planning/planning-optimization/planning-optimization-overview.md). Zákazníci s místním nasazením Dynamics 365 Supply Chain Management mohou i nadále používat hlavní plánovací modul Supply Chain Management pro scénáře distribuce po dubnu 2021. Nebudou však poskytována žádná další vylepšení funkcí. |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Předchozí oznámení o odebraných nebo zastaralých funkcích

Další informace o funkcích, které byly v předchozích verzích odebrány nebo zastaraly, naleznete v tématu [Odebrané nebo zastaralé funkce v předchozích verzích](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
