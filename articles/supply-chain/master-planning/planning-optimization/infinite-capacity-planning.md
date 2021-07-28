---
title: Plánování s nekonečnou kapacitou
description: Toto téma poskytuje informace o plánování nekonečné kapacity pro optimalizaci plánování. Také popisuje aktuální omezení funkcí.
author: crytt
ms.date: 6/9/2021
ms.topic: article
ms.search.form: RouteInventProd
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-06-09
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8c493522ea55dd7e69c0133aceef43a3e59021c3
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/06/2021
ms.locfileid: "6361325"
---
# <a name="scheduling-with-infinite-capacity"></a>Plánování s nekonečnou kapacitou

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]

Funkce *Plánování nekonečné kapacity pro optimalizaci plánování* zavádí plánování založené na informacích o trase. Umožňuje vám naplánovat úlohy na základě široké škály nastavení tras. Plánování pro optimalizaci plánování pokrývá často používané nastavení trasy, včetně sekvence provozu trasy nebo požadavků na prostředky operace trasy.

## <a name="turn-on-the-infinite-capacity-scheduling-feature"></a>Zapnutí funkci plánování s nekonečnou kapacitou

Pokud váš systém ještě neobsahuje funkci popsanou v tomto tématu, otevřete pracovní prostor [Správa funkcí](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) a zapněte funkci *Plánování s neomezenou kapacitou pro optimalizaci plánování*.

## <a name="added-functionality"></a>Přidaná funkce

Funkce *Plánování nekonečné kapacity pro optimalizaci plánování* umožňuje plánování úloh založené na informacích o trase. Nastavení trasy lze proto použít k plánování produkčních procesů. Ačkoli tato funkce má některá omezení, která integrované hlavní plánování nemá, podporuje nejběžnější funkce, které jsou vyžadovány pro výrobní scénáře.

Funkce zohledňuje *jednoduché trasy* i *sítě tras*. Pomocí pole **Další** na operaci trasy můžete nastavit složité trasy, které mají více počátečních bodů a více operací, které běží paralelně. Systém při plánování vezme v úvahu složité struktury tras tohoto typu.

Tato funkce navíc podporuje *paralelní operace* v trasách. Pomocí možností *Primární* a *Sekundární* v poli **Priorita** pro operace trasy můžete definovat strukturu trasy, kde jedna operace trasy je primární operace a jiná operace je sekundární. V takovém případě systém při plánování vezme v úvahu strukturu trasy.

Během procesu plánování systém rovněž zohledňuje *požadavky na zdroje*, které jsou specifikovány pro operaci. Systém používá požadavky na zdroje k určení, které prostředky jsou nutné k provedení operace. V současné době funkce *Plánování nekonečné kapacity pro optimalizaci plánování* podporuje následující typy požadavků na zdroje:

- Typ zdroje
- Prostředek
- Skupina prostředků
- Schopnost

> [!NOTE]
> Požadavky týkající se lidských zdrojů, jako jsou dovednosti nebo požadavky na certifikát, ještě nejsou podporovány.

Tato funkce také podporuje provozní vlastnosti **Čas nastavení** a **Čas běhu**. Když nastavíte tyto vlastnosti na operaci trasy, proces plánování vytvoří příslušné úlohy nastavení a zpracování.

Stručně řečeno, plánování optimalizace plánování podporuje nejčastěji používané scénáře. Můžete vytvořit trasu, přidat primární a sekundární operace, definovat další operace, přidat požadavky na prostředky a přidat čas nastavení a čas běhu. Systém poté zohlední tyto informace během plánování.

## <a name="limitations"></a>Omezení

Následující omezení platí, když používáte plánování pro optimalizaci plánování:

- Tato funkce podporuje pouze plánování úloh. Nastavení související s plánováním operací se během plánování nezohledňují bez ohledu na metodu plánování v hlavních plánech.
- Tato funkce podporuje pouze nekonečnou kapacitu.
- Funkce nepodporuje funkci načítání prostředků.
- Funkce nezohledňuje odpad trasy.
- Tato funkce podporuje *Doba trvání* pouze jako výběr primárního zdroje.

Funkce *Plánování nekonečné kapacity pro optimalizaci plánování* se neustále vylepšuje. Microsoft očekává zavedení podpory pro další nastavení plánování v budoucích verzích.
