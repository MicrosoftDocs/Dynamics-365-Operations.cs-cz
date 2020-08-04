---
title: Odstraněné nebo zastaralé funkce v aplikaci Dynamics 365 Supply Chain Management
description: Toto téma popisuje funkce, které byly odebrány nebo u nichž se plánuje odstranění v Dynamics 365 Supply Chain Management.
author: kamaybac
manager: tfehr
ms.date: 04/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 07f37488747766dcca96884e204339b425bbd201
ms.sourcegitcommit: f64fce03ec52f844b05a9e8cac286cb201385002
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/16/2020
ms.locfileid: "3597109"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-supply-chain-management"></a>Odstraněné nebo zastaralé funkce v aplikaci Dynamics 365 Supply Chain Management

[!include [banner](../includes/banner.md)]

Toto téma bude aktualizováno podle nově odebraných nebo zastaralých funkcí pro Dynamics 365 Supply Chain Management.

- *Odstraněná* funkce již není k dispozici v produktu.
- *Zastaralá* funkce není v aktivním nasazení a v budoucí aktualizaci může být odstraněna.

Tento seznam je určen k tomu, aby vám pomohl zvážit tyto odstraněné a zastaralé funkce při svém plánování.

> [!NOTE]
> Podrobné informace o objektech v aplikacích Finance and Operations lze nalézt v části [Sestavy technických informací](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep). Můžete srovnat různé verze těchto sestav a zjistíte, které objekty se změnily nebo byly odstraněny v každé z verzí aplikací Finance and Operations.

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10011-release"></a>Odebrané nebo zastaralé funkce ve verzi Supply Chain Management 10.0.11

### <a name="use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios"></a>Použití integrovaného modulu hlavního plánování Supply Chain Management pro scénáře distribuce

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Pro zvýšení výkonu a minimalizaci zatížení databáze SQL během hlavních plánovacích relací je vestavěný hlavní plánovací modul Supply Chain Management nahrazen optimalizací plánování. Optimalizace plánování umožňuje rychlé spouštění plánů, které lze provádět i během úředních hodin. To umožňuje plánovačům okamžitě reagovat na změny poptávky nebo parametrů plánování. |
| **Nahrazeno jinou funkcí?**   | Ano, optimalizace plánování nahradí předdefinovaný hlavní modul plánování Supply Chain Management. |
| **Ovlivněné oblasti produktu**         | Supply Chain Management - hlavní plánování |
| **Možnost nasazení**              | Pouze cloud. Všimněte si, že optimalizace plánování není podporována u místních nasazení. |
| **Stav**                         | Zastaralé. Od dubna April 2021 nebudou scénáře distribuce dále podporovány v integrovaném modulu hlavního plánování Dynamics 365 Supply Chain Management. U distribučních scénářů musí zákazníci pro výpočet hlavního plánování použít Optimalizaci plánování. Další informace naleznete v tématu [Dokumentace optimalizace plánování](https://go.microsoft.com/fwlink/?linkid=2105830). Zákazníci s místním nasazením Dynamics 365 Supply Chain Management mohou i nadále používat hlavní plánovací modul Supply Chain Management pro scénáře distribuce po dubnu 2021. Nebudou však poskytována žádná další vylepšení funkcí. |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Předchozí oznámení o odebraných nebo zastaralých funkcích

Další informace o funkcích, které byly v předchozích verzích odebrány nebo zastaraly, naleznete v tématu [Odebrané nebo zastaralé funkce v předchozích verzích](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).
