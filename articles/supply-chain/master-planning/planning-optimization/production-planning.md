---
title: Plánování výroby
description: Tento článek popisuje plánování výroby a vysvětluje, jak upravit plánované výrobní zakázky pomocí optimalizace plánování.
author: t-benebo
ms.date: 08/09/2022
ms.topic: article
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-12-15
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 43da249637c44b3f56e8b5e210a0e44d9ac6cb9d
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740542"
---
# <a name="production-planning"></a>Plánování výroby

[!include [banner](../../includes/banner.md)]

Následující video poskytuje krátký úvod k některým konceptům pojednávaným v tomto článku: [Dynamics 365 Supply Chain Management: Vylepšení optimalizace plánování](https://youtu.be/u1pcmZuZBTw).

## <a name="turn-this-feature-on-or-off-for-your-system"></a>Zapnutí nebo vypnutí této funkce ve vašem systému

Pokud chcete použít tuto funkci, musíte ji zapnout ve svém systému. Od verze Supply Chain Management 10.0.29 je tato funkce povinná a nelze ji vypnout. Pokud používáte verzi starší než 10.0.29, mohou správci tuto funkčnost zapnout nebo vypnout vyhledáním funkce *Plánované výrobní zakázky pro optimalizaci plánování* v pracovním prostoru [Správa funkcí](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="planned-production-orders"></a>Plánované výrobní zakázky

Když hlavní plánování vytvoří plánované objednávky pro splnění požadavků, je typ objednávky určen hodnotou pole **Typ plánované objednávky**. Pokud je pole **Plánovaný typ objednávky** nastaveno na *Výroba*, jsou vytvořeny plánované výrobní zakázky. Tyto plánované výrobní zakázky obsahují informace o aktivním kusovníku (BOM) a ID trasy ze souvisejícího výrobního nastavení.

## <a name="requirements-from-boms"></a>Požadavky na kusovníky

Informace o kusovníku se zadávají během hlavního plánování. Výstup plánu zahrnuje dodávku materiálu k pokrytí související materiálové poptávky po výrobě.

Během hlavního plánování se k určení materiálů potřebných pro výrobu použije aktuální aktivní kusovník. Tento krok se provádí na všech úrovních struktury kusovníku, která souvisí s požadovanou výrobní zakázkou. Požadavek na materiál je splněn využitím dostupných zásob na skladě, existujícího dodání na objednávku a schválených plánovaných objednávek. Pokud je kdekoli potřeba další materiál, vytvoří se plánovaná objednávka k pokrytí poptávky.

## <a name="scheduling-during-firming"></a>Plánování během potvrzení

Plánované výrobní zakázky zahrnují ID trasy, které je požadováno pro plánování výroby. Podpora plánování během běhu plánování pro plánované objednávky však čeká na vyřízení. ID trasy se používá k plánování plánovaných výrobních zakázek během zpevňování. Dodací lhůta u plánovaných výrobních zakázek se proto může lišit od dodací lhůty u souvisejících naplánovaných, zpevněných výrobních zakázek, které se z nich generují, jak je popsáno zde:

- **Plánovaná výrobní zakázka** - Dodací lhůta je založena na statické dodací době z uvolněného produktu.
- **Pevná výrobní zakázka** - Dodací lhůta je založena na plánování, které využívá informace o trase a související omezení zdrojů.

## <a name="delays"></a>Zpoždění

Pokud je dodací lhůta pro požadovaný materiál delší než období mezi dnešním datem a datem požadavku na materiál, plánovaná objednávka požadovaného materiálu a související výrobní zakázka se zpozdí. U plánovaných objednávek se zpoždění (ve dnech) počítá na základě doby realizace vydaného produktu. Informace o zpoždění se poté šíří všemi úrovněmi struktury kusovníku. Proto můžete sledovat dopad zpožděné suroviny až k zákaznické prodejní objednávce.

## <a name="modifying-planned-orders"></a>Změna plánovaných objednávek

Když změníte informace o plánované objednávce, zobrazí se následující zpráva: „Dopad manuálních změn na plánované objednávky se neprojeví ve zbytku plánu až do příštího hlavního plánování.“

Pokud chcete změnit informace o plánované objednávce a zjistit dopad na související požadavky na materiál, postupujte podle těchto kroků.

1. Aktualizujte plánovanou objednávku.
2. Schvalte plánovanou objednávku.
3. Spusťte hlavní plánování.

Při spuštění hlavního plánování byste neměli používat filtry, pokud jsou zahrnuty plánované výrobní zakázky. Více informací naleznete v části [Filtry](#filters) v dále v tomto článku.

> [!NOTE]
> Pokud se datum dodání plánované objednávky změní na pozdější datum, může být požadavek navázán na novou plánovanou objednávku. K tomuto chování dochází, když nové datum dodávky způsobí zpoždění pro vázanou poptávku, ale podle nastavení doby předstihu lze zpoždění zabránit.

## <a name="explosion-page"></a>Stránka exploze

Stránku **Exploze** můžete použít pro analýzu poptávky, která je požadována pro konkrétní výrobní zakázku nebo plánovanou výrobní zakázku, související pokrytím a informacemi o fixaci. Informace na stránce **Exploze** se během hlavního plánování aktualizuje. Informace nemůžete aktualizovat přímo ze stránky **Exploze**.

## <a name="filters"></a><a name="filters"></a>Filtry

Abyste zajistili, že hlavní plánování obsahuje informace, které potřebuje k výpočtu správného výsledku, musíte zahrnout všechny produkty, které mají jakýkoli vztah k produktům, do celé struktury kusovníku plánované objednávky. U scénářů plánování, které zahrnují produkci, proto doporučujeme vyhnout se filtrovaným běhům hlavního plánování.

I když jsou závislé podřízené položky automaticky detekovány a zahrnuty do hlavních běhů plánování, když je použit zastaralý hlavní plánovací modul, Optimalizace plánování aktuálně tuto akci neprovede.

Například pokud se k výrobě produktu B použije také jeden šroub ze struktury kusovníku produktu A, musí být do filtru zahrnuty všechny produkty ve struktuře kusovníku produktů A a B. Protože může být složité zajistit, aby všechny produkty byly součástí filtru, doporučujeme, abyste se vyhnuli filtrovaným hlavním plánovacím běhům, když jsou zahrnuty výrobní zakázky. Jinak hlavní plánování poskytne nežádoucí výsledky.

### <a name="reasons-to-avoid-filtered-master-planning-runs"></a>Důvody, proč se vyhnout filtrovaným spuštěním hlavního plánování

Když spustíte filtrované hlavní plánování pro produkt, optimalizace plánování (na rozdíl od zastaralého hlavního plánovacího modulu) nerozpozná všechny dílčí produkty a suroviny ve struktuře kusovníku daného produktu, a proto je nezahrne do běhu hlavního plánování. Přestože optimalizace plánování identifikuje první úroveň ve struktuře kusovníku produktu, nenačte z databáze žádné nastavení produktu (například výchozí typ objednávky nebo pokrytí položky).

V optimalizaci plánování se předem načtou data běhu a použijí se filtry. To znamená, že pokud dílčí produkt nebo surovina obsažená v konkrétním produktu není součástí filtru, informace o něm nebudou pro běh zachyceny. Pokud je dílčí produkt nebo surovina také zahrnuta v jiném produktu, pak filtrovaný běh zahrnující pouze původní produkt a jeho komponenty by odstranil stávající plánovanou poptávku, která byla vytvořena pro tento jiný produkt.

Tato logika může způsobit, že filtrované hlavní plánování vytvoří neočekávané výsledky. V následujících částech jsou uvedeny příklady, které ilustrují neočekávané výsledky, ke kterým může dojít.

### <a name="example-1"></a>Příklad 1

Dokončené zboží *DZ* se skládá z následujících komponent:

- Surovina *S*
- Dílčí produkt *D1*, který se skládá z dílčího produktu *D2*

K dispozici jsou zásoby na skladě suroviny *S*, zatímco dílčí produkt *D1* není skladem.

Když provedete filtrované spuštění hlavního plánování pro dokončené zboží *DZ*, získáte plánovanou výrobní zakázku na dokončené zboží *DZ*, plánovanou nákupní objednávku suroviny *S* a plánovanou nákupní objednávku dílčího produktu *D1*. To je nežádoucí výsledek, protože optimalizace plánování ignorovala stávající nabídku suroviny *S* a to, že dílčí produkt *D1* je třeba vytvořit pomocí dílčího produktu *D2* namísto přímého objednání. Stalo se to proto, že optimalizace plánování má pouze seznam komponent pro dokončené zboží *DZ* bez jakýchkoli souvisejících informací, jako je stávající dodávka komponent nebo jejich výchozí nastavení objednávky.

### <a name="example-2"></a>Příklad 2

Předchozí příklad rozšíříme o další dokončené zboží *DZ2*, které také používá dílčí produkt *D1*. Existuje plánovaná objednávka dokončeného zboží *DZ2* a existuje plánovaná poptávka po všech jeho komponentech, včetně *D1*.

Rozhodnete se překonat nežádoucí výsledky filtrovaného běhu hlavního plánování z předchozího příkladu přidáním všech dílčích produktů a surovin ze struktury kusovníku dokončeného zboží *DZ* k filtru a poté spustit plnou regeneraci.

Když spustíte úplnou regeneraci, systém odstraní všechny existující výsledky pro všechny zahrnuté produkty a poté znovu vytvoří výsledky na základě nových výpočtů. To znamená, že stávající plánovaná poptávka po produktu *D1* je odstraněna a poté znovu vytvořena se započítáním pouze požadavků na dokončené zboží *DZ*, požadavky dokončeného zboží *DZ2* nejsou brány do úvahy. Dojde k tomu proto, že spuštěná optimalizace plánování nepracuje s plánovanou poptávkou dalších plánovaných výrobních zakázek &mdash; používá se pouze plánovaná poptávka generovaná během běhu.

> [!NOTE]
> Pokud je stávající plánovaná objednávka na dokončené zboží *DZ2* ve stavu *Schváleno*, pak bude schválená plánovaná poptávka zahrnuta, i když není nadřazený produkt přidán do filtru.

Proto pokud nepřidáte všechny komponenty dokončeného zboží *DZ*, dokončené zboží *DZ2* a všechny ostatní produkty, jejichž součástí jsou tyto komponenty (společně s jejich komponentami), bude filtrovaný běh hlavního plánování dávat nežádoucí výsledky.

Protože může být složité zajistit, aby všechny produkty byly součástí filtru, doporučujeme, abyste se vyhnuli filtrovaným hlavním plánovacím běhům, když jsou zahrnuty výrobní zakázky.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
