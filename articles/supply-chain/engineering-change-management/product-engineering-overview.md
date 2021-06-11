---
title: Přehled správy technických změn
description: Toto téma poskytuje přehled správy technických změn, která vám pomůže plánovat a spravovat verzování produktu a spravovat životní cykly produktu a technických změn.
author: t-benebo
ms.date: 11/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: d9430fe02abe58f37d2bfd1431b4da61527d0834
ms.sourcegitcommit: 588f8343aaa654309d2ff735fd437dba6acd9d46
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/28/2021
ms.locfileid: "6115042"
---
# <a name="engineering-change-management-overview"></a>Přehled správy technických změn

[!include [banner](../includes/banner.md)]

## <a name="feature-summary"></a>Souhrn funkce

Dnešní výrobci vyžadují silnou správu dat produktu, řízení verzí a správu technických změn, aby uspěli ve světě neustále se snižujících životních cyklů produktů, zvýšených požadavků na kvalitu a spolehlivost a zvýšeného zaměření na bezpečnost produktů.

Správa technických změn přináší strukturu a disciplínu do procesu správy dat produktu a umožňuje, aby byly produkty definovány, uvolňovány a revidovány kontrolovaným způsobem, který je podporován pracovními postupy.Prostřednictvím verzí produktu a správy technických změn můžete dokumentovat, hodnotit dopad a aplikovat technické změny během celého životního cyklu produktu.

Správa technických změn vám pomáhá plánovat a spravovat verzování produktu a spravovat životní cykly produktu a technických změn. Zde je seznam jejich hlavních funkcí:

- Verzování produktu
- Vylepšená funkce uvolňování produktu, která vám umožní udržovat hlavní data produktu v jedné právnické osobě (technická společnost) a publikovat plně nakonfigurovaný uvolněný produkt do jiných právnických společností.
- Pravidla pro ověřování, zda jsou požadované informace zadány před aktivací verze produktu (kontroly připravenosti).
- Vylepšená správa životního cyklu produktu prostřednictvím detailní kontroly nad tím, kdy lze uvolněný produkt použít v konkrétních obchodních procesech.
- Požadavky na technické změny, které jsou podporovány pracovními postupy
- Příkazy k technickým změnám, které jsou podporovány pracovními postupy

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4HE6B]

Předchozí video ([Možnosti správy změn v Dynamics 365 Supply Chain Management](https://youtu.be/N313FqvRuBc)) je součástí [seznamu videí o Finance and Operations](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW), které jsou k dispozici na YouTube.

## <a name="turn-on-the-engineering-change-management-and-version-dimension-features-for-your-system"></a>Zapnutí funkcí správy technických změn a dimenze verzí pro systém

Než budete moci používat funkci správy technických změn, musíte povolit funkci *správy technických změn* a její konfigurační klíč. Pokud chcete také sledovat dimenzi verze produktů v transakcích (volitelně), musíte povolit také funkci *Dimenze verze produktu* a její konfigurační klíč.

Správci mohou funkce zapnout provedením následujících kroků.

1. Přejděte do [Správy funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).
1. Zkontrolovat aktualizace.
1. Zapněte funkci s názvem *Správa technických změn*.
1. Chcete-li ji použít, zapněte také funkci s názvem *Verze dimenze produktu*.

Správci mohou zapnout konfigurační klíče provedením následujících kroků.

1. Uveďte systém do režimu údržby, jak je popsáno v tématu [Režim údržby](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).
1. Přejděte do nabídky **Správa systému \> Nastavení \> Konfigurace licence**.
1. Rozbalte uzel **Obchod**.
1. Povolte konfigurační klíč pro hlavní funkci výběrem zaškrtávacího políčka **Správa technických změn**.
1. Rozbalte uzel **Řízení technických změn** a podle potřeby zaškrtněte nebo zrušte zaškrtnutí následujících políček (v závislosti na funkcích, které chcete použít):

    - **Hledání atributů** - Zaškrtnutím tohoto políčka povolíte [funkce vyhledávání atributů](engineering-attributes-and-search.md). Doporučujeme tuto funkci povolit, ale pokud ji nepoužíváte, můžete toto zaškrtávací políčko zrušit.
    - **Řízení změn pro procesní výrobu** - Toto políčko zaškrtněte, pokud chcete pomocí funkcí správy technických změn spravovat změny ve vzorcích pro procesní výrobu. Pokud vzorce nemusíte spravovat, můžete toto zaškrtávací políčko zrušit. Další informace viz [Spravujte změny v recepturách a jejich látkách](manage-formula-changes.md).

1. Chcete-li také použít dimenzi verze, zaškrtněte také políčko **Dimenze produktu - verze**. (Toto zaškrtávací políčko je dále v seznamu, není vnořeno pod uzlem **Správa technických změn**.)
1. Vypněte režim údržby, jak je popsáno v tématu [Režim údržby](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).

> [!IMPORTANT]
> Od dubna 2022 budou licenční klíče pro jak **Správu technických změn**, tak pro **Rozměr produktu - verze** ve výchozím nastavení povoleny pro všechny nové instalace, ale v případě potřeby je stále budete moci deaktivovat.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
