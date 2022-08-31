---
title: Plánování s nekonečnou kapacitou
description: Tento článek poskytuje informace o plánování nekonečné kapacity pro optimalizaci plánování. Také popisuje aktuální omezení funkcí.
author: t-benebo
ms.date: 08/09/2022
ms.topic: article
ms.search.form: RouteInventProd
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-06-09
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: c6e0190899abb544b559bb5f26ba974155989c3a
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/23/2022
ms.locfileid: "9335308"
---
# <a name="scheduling-with-infinite-capacity"></a>Plánování s nekonečnou kapacitou

[!include [banner](../../includes/banner.md)]

Funkce *Plánování nekonečné kapacity pro optimalizaci plánování* zavádí plánování založené na informacích o trase. Umožňuje vám naplánovat úlohy na základě široké škály nastavení tras. Plánování pro optimalizaci plánování pokrývá často používané nastavení trasy, včetně sekvence provozu trasy nebo požadavků na prostředky operace trasy.

## <a name="turn-the-infinite-capacity-scheduling-feature-on-or-off"></a>Zapnutí nebo vypnutí funkce plánování s nekonečnou kapacitou

Pokud chcete použít tuto funkci, musíte ji zapnout ve svém systému. Od verze Supply Chain Management 10.0.29 je tato funkce ve výchozím nastavení zapnuta. Správci mohou tuto funkci zapnout nebo vypnout vyhledáním funkce *Plánování nekonečné kapacity pro optimalizaci plánování* v pracovním prostoru [Správa funkcí](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Další informace o této funkci naleznete v části [Plánování s výběrem zdrojů na základě schopností](capability-based-scheduling.md).

## <a name="added-functionality"></a>Přidaná funkce

Funkce *Plánování nekonečné kapacity pro optimalizaci plánování* umožňuje plánování úloh založené na informacích o trase. Nastavení trasy lze proto použít k plánování produkčních procesů. Ačkoli tato funkce má některá omezení, která integrované hlavní plánování nemá, podporuje nejběžnější funkce, které jsou vyžadovány pro výrobní scénáře.

Funkce zohledňuje *jednoduché trasy* i *sítě tras*. Pomocí pole **Další** na operaci trasy můžete nastavit složité trasy, které mají více počátečních bodů a více operací, které běží paralelně. Systém při plánování vezme v úvahu složité struktury tras tohoto typu.

Tato funkce navíc podporuje *paralelní operace* v trasách. Pomocí možností *Primární* a *Sekundární* v poli **Priorita** pro operace trasy můžete definovat strukturu trasy, kde jedna operace trasy je primární operace a jiná operace je sekundární. V takovém případě systém při plánování vezme v úvahu strukturu trasy.

Během procesu plánování systém rovněž zohledňuje *požadavky na zdroje*, které jsou specifikovány pro operaci. Systém používá požadavky na zdroje k určení, které prostředky jsou nutné k provedení operace. V současné době funkce *Plánování nekonečné kapacity pro optimalizaci plánování* podporuje následující typy požadavků na zdroje:

- Typ zdroje
- Prostředek
- Skupina prostředků
- Schopnost (Další informace viz [Plánování s výběrem zdrojů na základě schopností](capability-based-scheduling.md).)

> [!NOTE]
>
> - Pokud je prostředků nebo skupina prostředků nastavena na nekonečnou kapacitu, hlavní plánování je bude považovat za nekonečnou kapacitu.
> - Požadavky týkající se lidských zdrojů, jako jsou dovednosti nebo požadavky na certifikát, ještě nejsou podporovány.

Tato funkce také podporuje provozní vlastnosti **Čas nastavení** a **Čas běhu**. Když nastavíte tyto vlastnosti na operaci trasy, proces plánování vytvoří příslušné úlohy nastavení a zpracování.

Stručně řečeno, plánování optimalizace plánování podporuje nejčastěji používané scénáře. Můžete vytvořit trasu, přidat primární a sekundární operace, definovat další operace, přidat požadavky na prostředky a přidat čas nastavení a čas běhu. Systém poté zohlední tyto informace během plánování.

## <a name="limitations"></a>Omezení

Následující omezení platí, když používáte plánování pro optimalizaci plánování:

- Tato funkce podporuje pouze nekonečnou kapacitu.
- Funkce nepodporuje funkci načítání prostředků.
- Funkce nezohledňuje odpad trasy.
- Tato funkce podporuje *Doba trvání* pouze jako výběr primárního zdroje.

Funkce *Plánování nekonečné kapacity pro optimalizaci plánování* se neustále vylepšuje. Microsoft očekává zavedení podpory pro další nastavení plánování v budoucích verzích.
