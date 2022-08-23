---
title: Odstraněné nebo zastaralé funkce v aplikaci Dynamics 365 Supply Chain Management
description: Tento článek popisuje funkce, které byly odebrány nebo u nichž se plánuje odstranění v Dynamics 365 Supply Chain Management.
author: kamaybac
ms.date: 06/29/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: f70d05f5663d8249b2435ad353421c278692a9ac
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/02/2022
ms.locfileid: "9218795"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-supply-chain-management"></a>Odstraněné nebo zastaralé funkce v aplikaci Dynamics 365 Supply Chain Management

[!include [banner](../includes/banner.md)]

Tento článek bude aktualizováno podle nově odebraných nebo zastaralých funkcí pro Dynamics 365 Supply Chain Management.

- *Odstraněná* funkce již není k dispozici v produktu.
- *Zastaralá* funkce není v aktivním nasazení a v budoucí aktualizaci může být odstraněna.

Tento seznam je určen k tomu, aby vám pomohl zvážit tyto odstraněné a zastaralé funkce při svém plánování.

> [!NOTE]
> Podrobné informace o objektech v finančních a provozních aplikacích lze nalézt v části [Sestavy technických informací](/dynamics/s-e/). Můžete srovnat různé verze těchto sestav a zjistíte, které objekty se změnily nebo byly odstraněny v každé z verzí finančních a provozních aplikací.

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10029-release"></a>Odebrané nebo zastaralé funkce ve verzi Supply Chain Management 10.0.29

### <a name="stock-transfer-orders-that-have-tax-on-the-transfer-price"></a>Skladové převodní příkazy s daní na mezipodnikové ceně

| &nbsp;  | &nbsp;  |
|---|---|
| **Důvod pro zrušení/odstranění** | Funkce [Příkazy k převodu akcií, které mají daň z převodní ceny](../../finance/localizations/apac-ind-gst-stock-transfer-transactions.md) je nahrazena funkcí [Příkazy k převodu akcií pro Indii](../../finance/localizations/apac-ind-stock-transfer.md). |
| **Nahrazeno jinou funkcí?**   | Ano, funkce [Příkazy k převodu akcií, které mají daň z převodní ceny](../../finance/localizations/apac-ind-gst-stock-transfer-transactions.md) je nahrazena funkcí [Příkazy k převodu akcií pro Indii](../../finance/localizations/apac-ind-stock-transfer.md). |
| **Ovlivněné oblasti produktu** | Supply Chain Management – zásoby |
| **Možnost nasazení** | Cloudové a místní nasazení |
| **Stav** | <p>Probíhá zastarávání. Funkce *Příkazy k převodu akcií, které mají daň z převodní ceny* nebude podporována opravami chyb a bezpečnostními opravami.</p><p>Po dubnu 2023 budou zákazníci požádáni, aby používali ve výchozím stavu vylepšenou funkci *Příkazy k převodu akcií pro Indii*. Po říjnu 2023 nebude funkce *Příkazy k převodu akcií, které mají daň z převodní ceny* již k dispozici a zákazníci budou požádáni, aby přešli na vylepšenou funkci *Příkazy k převodu akcií pro Indii*.</p><p>Více informací viz [Příkazy k převodu akcií pro Indii](../../finance/localizations/apac-ind-stock-transfer.md).</p> |

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10019-release"></a>Odebrané nebo zastaralé funkce ve verzi Supply Chain Management 10.0.19

### <a name="job-card-device"></a>Zařízení úkolového lístku

| &nbsp;  | &nbsp;  |
|---|---|
| **Důvod pro zrušení/odstranění** | [Zařízení úkolového lístku](../production-control/config-job-card-device.md) je nahrazeno novým [rozhraním pro provádění výrobního provozu](../production-control/production-floor-execution-configure.md). |
| **Nahrazeno jinou funkcí?**   | Ano, [zařízení úkolového lístku](../production-control/config-job-card-device.md) je nahrazeno novým [rozhraním pro provádění výrobního provozu](../production-control/production-floor-execution-configure.md). |
| **Ovlivněné oblasti produktu** | Supply Chain Management – řízení výroby |
| **Možnost nasazení** | Cloudové a místní nasazení |
| **Stav** | Zastaralé. Zařízení úkolového lístku obdrží podporu s opravami chyb a zabezpečení, ale vylepšení funkcí již nebudou poskytována. Po dubnu 2022 již nebude zařízení úkolového lístku podporováno a zákazníci budou požádáni, aby přešli na nové rozhraní pro provádění výrobního provozu. |

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10018-release"></a>Odebrané nebo zastaralé funkce ve verzi Supply Chain Management 10.0.18

### <a name="supply-chain-management--warehousing-the-warehouse-app"></a><a name="wma"></a>Supply Chain Management – řízení skladu (aplikace skladu)

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | S platností od dubna 2021 je aplikace *Supply Chain Management – řízení skladu* (aplikace skladu) zastaralá a po dubnu 2022 nebude podporována. Nyní je nahrazena *mobilní aplikací Řízení skladu*, která byla vydán s verzí 10.0.17 aplikace Supply Chain Management. Nová aplikace je úplnou náhradou, ale používá stejný základní rámec, což usnadňuje migraci. V případě potřeby lze tyto dvě aplikace použít vedle sebe, aby si uživatelé postupně zvykli používat novou aplikaci.<br><br>Další informace, jak konfigurovat novou mobilní aplikaci Řízení skladu, viz témata [Mobilní aplikace Řízení skladu](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/warehouse-management-mobile-application) a [Instalace a připojení mobilní aplikace Řízení skladu](../warehousing/install-configure-warehouse-management-app.md). |
| **Nahrazeno jinou funkcí?**   | Ano, nahrazeno novou mobilní aplikací Řízení skladu. |
| **Ovlivněné oblasti produktu**         | Supply Chain Management – aplikace skladu |
| **Možnost nasazení**              | Cloudové a místní nasazení |
| **Stav**                         | Zastaralé. Aplikace skladu obdrží podporu s opravami chyb a zabezpečení, ale vylepšení funkcí již nebudou poskytována. Po dubnu 2022 již nebude stará aplikace skladu podporována a zákazníci budou požádáni, aby se přesunuli do nové mobilní aplikace Řízení skladu. Stará aplikace skladu bude poté odstraněna z obchodů Microsoft Store a Google Play.  |

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10015-release"></a>Odebrané nebo zastaralé funkce ve verzi Supply Chain Management 10.0.15

### <a name="internet-explorer-11-support-for-dynamics-365-is-deprecated"></a>Podpora aplikace Internet Explorer 11 pro Dynamics 365 je zastaralá

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | S platností od prosince 2020 je podpora aplikace Microsoft Internet Explorer 11 zastaralá pro všechny produkty Dynamics 365 a Internet Explorer 11 nebude podporován po srpnu 2021.<br><br>To bude mít dopad na zákazníky, kteří používají produkty Dynamics 365, které jsou navrženy pro použití prostřednictvím rozhraní Internet Explorer 11. Po srpnu 2021 nebude Internet Explorer 11 podporován pro takové produkty Dynamics 365. |
| **Nahrazeno jinou funkcí?**   | Doporučujeme zákazníkům přejít na Microsoft Edge.|
| **Ovlivněné oblasti produktu**         | Všechny produkty Dynamics 365 |
| **Možnost nasazení**              | Vše|
| **Stav**                         | Zastaralé. Internet Explorer 11 nebude podporován po srpnu 2021.|

### <a name="use-of-built-in-supply-chain-management-master-planning-engine-for-manufacturing-scenarios"></a>Použití integrovaného modulu hlavního plánování Supply Chain Management pro scénáře výroby

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Pro zvýšení výkonu a minimalizaci zatížení databáze SQL během hlavních plánovacích relací je vestavěný hlavní plánovací modul Supply Chain Management nahrazen optimalizací plánování. Optimalizace plánování umožňuje rychlé spouštění plánů, které lze provádět i během úředních hodin. To umožňuje plánovačům okamžitě reagovat na změny poptávky nebo parametrů plánování. |
| **Nahrazeno jinou funkcí?**   | Ano, optimalizace plánování nahradí předdefinovaný hlavní modul plánování Supply Chain Management. |
| **Ovlivněné oblasti produktu**         | Supply Chain Management - hlavní plánování |
| **Možnost nasazení**              | Pouze cloud. Všimněte si, že optimalizace plánování není podporována u místních nasazení. |
| **Stav**                         | Zastaralé. Do 1. dubna 2022 nebudou scénáře výroby dále podporovány v integrovaném modulu hlavního plánování Supply Chain Management. K tomuto datu Microsoft zastaví veškerý aktivní vývoj výrobních scénářů pro vestavěný plánovací modul, nevydá žádné nové funkce a bude vydávat pouze opravy kritických chyb. Po tomto datu musí všechny společnosti, které vyžadují podporu pro výrobní scénáře, používat pro své výpočty hlavního plánování aplikace Optimalizace plánování. Očekává se, že Optimalizace plánování bude plně podporovat výrobní scénáře do října 2022. Další informace naleznete v tématu [Dokumentace optimalizace plánování](../master-planning/planning-optimization/planning-optimization-overview.md).<br><br>Společnosti s místním nasazením Supply Chain Management mohou i nadále používat vestavěný hlavní plánovací modul pro scénáře výroby po dubnu 2022. Nebudou však poskytována žádná další vylepšení funkcí. |

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10011-release"></a>Odebrané nebo zastaralé funkce ve verzi Supply Chain Management 10.0.11

### <a name="use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios"></a>Použití integrovaného modulu hlavního plánování Supply Chain Management pro scénáře distribuce

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Pro zvýšení výkonu a minimalizaci zatížení databáze SQL během hlavních plánovacích relací je vestavěný hlavní plánovací modul Supply Chain Management nahrazen optimalizací plánování. Optimalizace plánování umožňuje rychlé spouštění plánů, které lze provádět i během úředních hodin. To umožňuje plánovačům okamžitě reagovat na změny poptávky nebo parametrů plánování. |
| **Nahrazeno jinou funkcí?**   | Ano, optimalizace plánování nahradí předdefinovaný hlavní modul plánování Supply Chain Management. |
| **Ovlivněné oblasti produktu**         | Supply Chain Management - hlavní plánování |
| **Možnost nasazení**              | Pouze cloud. Všimněte si, že optimalizace plánování není podporována u místních nasazení. |
| **Stav**                         | Zastaralé. Do 1 dubna 2021 nebudou scénáře distribuce dále podporovány v integrovaném modulu hlavního plánování Dynamics 365 Supply Chain Management. U distribučních scénářů musí zákazníci pro výpočet hlavního plánování použít Optimalizaci plánování. Další informace naleznete v tématu [Dokumentace optimalizace plánování](../master-planning/planning-optimization/planning-optimization-overview.md). Zákazníci s místním nasazením Dynamics 365 Supply Chain Management mohou i nadále používat hlavní plánovací modul Supply Chain Management pro scénáře distribuce po dubnu 2021. Nebudou však poskytována žádná další vylepšení funkcí. |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Předchozí oznámení o odebraných nebo zastaralých funkcích

Další informace o funkcích, které byly v předchozích verzích odebrány nebo zastaraly, naleznete v tématu [Odebrané nebo zastaralé funkce v předchozích verzích](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

