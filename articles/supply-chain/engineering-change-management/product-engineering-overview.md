---
title: Přehled správy technických změn
description: Toto téma poskytuje přehled správy technických změn, která vám pomůže plánovat a spravovat verzování produktu a spravovat životní cykly produktu a technických změn.
author: t-benebo
manager: tfehr
ms.date: 11/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: b081cd8d56217b8cf76db824c29482d453fc9ea3
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "5001941"
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

## <a name="turn-on-engineering-change-management-for-your-system"></a>Zapněte pro svůj systém správu technických změn

Nejprve zapněte správu technických změn podle těchto kroků.

1. Přejděte na [Správu funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).
1. Zkontrolovat aktualizace.
1. Zapněte funkci s názvem **Správa technických změn**.

Dále zapněte konfigurační klíč **Správa technických změn** podle těchto kroků.

1. Uveďte systém do režimu údržby, jak je popsáno v tématu [Režim údržby](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).
1. Přejděte do nabídky **Správa systému \> Nastavení \> Konfigurace licence**.
1. Rozbalte uzel **Obchod** a vyberte zaškrtávací políčko **Řízení technických změn**.
1. Vypněte režim údržby, jak je popsáno v tématu [Režim údržby](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).
