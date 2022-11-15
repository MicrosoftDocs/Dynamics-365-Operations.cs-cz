---
title: Plánování řízené poptávkou
description: Článek popisuje, jak generovat plánované objednávky pro položky, které jsou nastaveny jako oddělovací body.
author: t-benebo
ms.date: 06/30/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-06-30
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 8ba9a6d24923b66259bc8b6cc688ec667cb000de
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740295"
---
# <a name="demand-driven-planning"></a>Plánování řízené poptávkou

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

Článek popisuje, jak generovat plánované objednávky pro položky, které jsou nastaveny jako oddělovací body.

## <a name="net-flow-and-qualified-demand"></a>Čistý tok a kvalifikovaná poptávka

Během hlavního plánování systém aplikuje koncept *síťového toku* ke stanovení efektivního množství na skladě na základě skutečné zásoby na skladě plus zásoby, která je na objednávku (existující objednávky dodávek, které ještě nebyly přijaty), mínus to, co se nazývá *kvalifikovaná poptávka* (kvalifikovaný nadcházející prodej), jak je znázorněno na následujícím obrázku. Když systém zjišťuje, do jaké vyrovnávací zóny položka patří a jaké by mělo být objednané množství, vyhodnocuje čistý tok, nikoli skutečnou skladovou zásobu.

![Příklad grafu výpočtu čistého toku.](media/ddmrp-net-flow-example.png "Příklad grafu výpočtu čistého toku")

Když je plánovaná objednávka spuštěna během plánovacího běhu, objednané množství bude maximální úroveň mínus čistý tok. K přiřazení priority objednávky systém používá funkci [plánování na základě priorit](priority-based-planning.md) namísto dat požadavků. Plánování materiálových požadavků řízené poptávkou (DDMRP) přiřazuje prioritu plánované objednávce na základě objednaného množství jako procento maximální zásoby. Na předchozím obrázku je objednané množství 53 % z maximálního množství. Proto bude priorita pro doplnění objednávky 53. (Pro kontext, 0 je nejvyšší priorita a 100 je nejnižší priorita.)

*Kvalifikovaná poptávka* je poptávka po splatnosti plus dnešní poptávka plus kvalifikované nárůsty objednávek v budoucnu. Následující obrázek ukazuje příklad úrovní poptávky pro dnešek (12. června) a následující tři dny. DDMRP vám umožňuje nastavit práh špičky objednávek k identifikaci poptávky, která překračuje běžná očekávání. Pokud je prahová hodnota nastavena na 25 kusů, dvě budoucí data uvedená na obrázku budou považována za špičky objednávky. Musíte přiřadit práh špičky objednávky pro každý produkt jednotlivě pomocí jeho stránky **Disponibilita položky**, jak je popsáno v části [Nastavení vyrovnávacích zásob pro položku bodu oddělení](ddmrp-buffer-profile-and-levels.md#set-up-buffers).

![Příklad grafu výpočtu kvalifikované poptávky.](media/ddmrp-net-qualified-demand-example.png "Příklad grafu výpočtu kvalifikované poptávky")

Za předpokladu, že neexistuje žádná poptávka po splatnosti, můžete nyní přidat dnešní poptávku (18) k množství dvou špiček objednávek (29 a 26), abyste získali kvalifikovanou poptávku 73. I když existuje poptávka na 23. června, všimněte si, že není zahrnuta ve výpočtu čistého toku, protože DDMRP spouští plánovanou objednávku jinak než tradiční skupiny pokrytí plánování.

## <a name="generating-planned-orders-with-ddmrp"></a>Generování plánovaných objednávek pomocí DDMRP

Během běhu plánování systém vytvoří novou plánovanou objednávku, pokud čistý tok položky klesne pod bod změny objednávky. Když používáte DDMRP, obvykle budete provádět plánovací běh každý den. Proto v podstatě jednou denně kontrolujete své zásoby, abyste zjistili, které položky je třeba doplnit.

Následující ilustrace ukazuje příklad situace, kdy máte objednávku na 18 kusů 20. června, 29 kusů 21. června, 26 kusů 22. června a 20 kusů 23. června. Protože je práh špičky nastaven na 25 kusů, dvě z těchto objednávek jsou označeny jako špičky. K dispozici je 220 kusů tohoto zboží.

![Příklad plánování 1.](media/ddmrp-planning-example-1.png "Příklad plánování 1")

Pokud nyní spustíte hlavní plánování, vygeneruje plánovanou objednávku, pokud se zjistí, že čistý tok klesne pod bod změny objednávky (v tomto příkladu 219 kusů).

![Příklad plánování 2.](media/ddmrp-planning-example-2.png "Příklad plánování 2")

Tento příklad vytvoří plánovanou nákupní objednávku pro množství 130, které se rovná maximální úrovni mínus čistý tok. Plánované objednávce je přiřazena priorita 53,07 na základě jejího procenta z maximálního množství. Protože tyto hodnoty byly nalezeny 20. června, systém vytvoří plánovanou objednávku s datem 20. června plus oddělenou dodací lhůtu pro položku (v tomto příkladu pět pracovních dnů). Proto, protože pět pracovních dnů je jeden týden ode dneška, je plánovaná objednávka datována 27. června.

> [!NOTE]
> Hlavní plánování počítá pouze oddělené položky pomocí DDMRP. Všechny ostatní položky jsou vypočteny pomocí standardního plánování požadavků na materiál (MRP).
