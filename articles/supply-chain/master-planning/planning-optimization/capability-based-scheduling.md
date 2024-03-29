---
title: Plánování s výběrem prostředků na základě schopností
description: Tento článek popisuje výběr prostředků během plánování s nekonečnou kapacitou, když zadáte schopnosti jako požadavky na prostředky pro operaci.
author: t-benebo
ms.date: 08/09/2022
ms.topic: article
ms.search.form: RouteInventProd, WrkCtrTable, WrkCtrCapability
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-09-03
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 176f40ad8cd1aa1831bbe50c0ebd91ec0cc3bc89
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/03/2022
ms.locfileid: "9739891"
---
# <a name="scheduling-with-resource-selection-based-on-capability"></a>Plánování s výběrem prostředků na základě schopností

[!include [banner](../../includes/banner.md)]

Zadáním požadavků na prostředky pro operaci výrobního postupu definujete, co je nutné k provedení této operace. Operace může například vyžadovat konkrétní prostředek nebo skupinu prostředků nebo kombinaci dovedností či schopností. Tento článek popisuje výběr prostředků během plánování s nekonečnou kapacitou, když zadáte schopnosti jako požadavky na prostředky pro operaci.

## <a name="turn-the-capability-based-scheduling-feature-on-or-off"></a>Zapnutí nebo vypnutí funkce plánování na základě schopností

Pokud chcete použít tuto funkci, musíte ji zapnout ve svém systému. Od verze Supply Chain Management 10.0.29 je tato funkce ve výchozím nastavení zapnuta. Správci mohou tuto funkci zapnout nebo vypnout vyhledáním funkce *Plánování nekonečné kapacity pro optimalizaci plánování* v pracovním prostoru [Správa funkcí](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Další informace o této funkci viz [Plánování s nekonečnou kapacitou](infinite-capacity-planning.md).

## <a name="capability-based-scheduling"></a>Plánování na základě schopností

Schopnost je způsobilost provozních prostředků provádět určitou aktivitu. K jednomu provoznímu prostředku můžete přiřadit více než jednu schopnost, a jednu schopnost můžete přiřadit více prostředkům. Schopnosti lze přiřadit ke všem typům prostředků, například k nástrojům, dodavatelům, strojům, umístěním, zařízením a lidským prostředkům.

Když zadáte schopnosti jako požadavky na prostředky, můžete alokaci prostředků odložit, dokud nejsou naplánovány objednávky. Namísto přiřazení konkrétních prostředků nebo skupin prostředků k operaci postupu můžete definovat schopnosti, které jsou pro každou operaci postupu vyžadovány. Poté během plánování systém spáruje požadované schopnosti se schopnostmi, které jsou definovány pro prostředky. Systém vybírá pouze prostředky, které splňují požadavky.

Chcete-li přiřadit schopnosti k provoznímu prostředku, použijte záložku **Schopnosti** na stránce **Prostředky**. Chcete-li přiřadit prostředky ke schopnosti, použijte záložku **Prostředky** na stránce **Schopnosti prostředku**. Obě stránky jsou přístupné v části **Řízení výroby \> Nastavení \> Prostředky** v navigačním podokně. Obě záložky obsahují mřížku, která uvádí seznam prostředků, které jsou přidruženy k vybranému prostředku nebo schopnosti. Obě záložky také obsahují panel nástrojů, který můžete použít k přidání, odebrání a úpravě řádků v mřížce. Mřížka obsahuje následující sloupce:

- **Prostředek** nebo **Schopnost** – Vyberte prostředek nebo schopnost, která je přiřazena řádkem.
- **Popis** – Zadejte stručný popis prostředku nebo schopnosti.
- **Platný** – Zadejte první datum, kdy se použije přiřazení prostředku nebo schopnosti. Během plánování systém nebude používat prostředek nebo schopnost, které mají přiřazení schopnosti s prošlou platností, i když tento prostředek jinak splňuje požadavky.
- **Vypršení platnosti** – Zadejte poslední datum, kdy se použije přiřazení prostředku nebo schopnosti. Během plánování systém nebude používat prostředek nebo schopnost, které mají přiřazení schopnosti s prošlou platností, i když tento prostředek jinak splňuje požadavky.
- **Úroveň** – Určete úroveň způsobilosti, kterou musí prostředek pro danou schopnost mít. Když poté zadáte hodnotu **Minimální potřebná úroveň** pro požadavek na prostředek nebo schopnost, plánovací modul bere během výběru prostředku bere do úvahy úroveň způsobilosti. Systém vybere pouze prostředky, které mají požadovanou schopnost na úrovni, která se rovná nebo je větší než minimální úroveň zadaná v požadavku na prostředek.
- **Priorita** – Toto pole zatím Optimalizace plánování nepoužívá. Pokud však používáte vestavěný zastaralý modul hlavního plánování, můžete pole **Priorita** použít v přiřazení prostředku nebo schopnosti k definování priority prostředku. Pokud je poté vybraná *Priorita* v poli **Výběr primárního prostředku** na stránce **Parametry plánování**, systém během plánování jako první vybere prostředek, který má nejvyšší prioritu (tj. nejnižší číselnou hodnotu v poli **Priorita**).

## <a name="example"></a>Příklad

Tento příklad ukazuje, jak modul plánování volí prostředky na základě schopností.

Výrobní postup má pět operací: *10*, *20*, *30*, *40* a *50*. Každá operace postupu vyžaduje prostředek, který má jiné schopnosti. Například operace postupu *10* vyžaduje prostředek, který má schopnost sestavit reproduktor (*0050 Spkr Assembly*) a schopnost zpracovávat dřevo (*1010 Wood capabilities*). Operace provozu *50* vyžaduje prostředek, který má schopnost zabalit produkt (*0070 Packing capability*).

![Schopnosti použité pro plánování.](media/capability-based-scheduling.png "Schopnosti použité pro plánování.")

Během plánování vyhledává modul prostředky, které splňují provozní požadavky. Například plánovací modul vybere prostředek *00101* k provedení operace *10*, protože tento prostředek je prvním nalezeným prostředkem, který má obě požadované schopnosti. Plánovací modul vybere prostředek *00301* k provedení operace *50*, protože tento prostředek je jediným prostředkem, který má schopnost zabalit zboží.

Dále zvažte, jak bude tento příklad ovlivněn používáním úrovní způsobilosti:

- Operace *10* vyžaduje minimální úroveň způsobilosti *7* pro schopnost *0059 Assembly*.
- Prostředek *00101* má úroveň způsobilosti *5* pro schopnost *0059 Assembly*.
- Prostředek *00102* má úroveň způsobilosti *10* pro schopnost *0059 Assembly*.

V tomto případě během plánování s nekonečnou kapacitou modul plánování vybere prostředek *00102* k provedení operace *10*, protože tento prostředek má na rozdíl od prostředku *00101* požadovanou úroveň způsobilosti pro danou schopnost.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
