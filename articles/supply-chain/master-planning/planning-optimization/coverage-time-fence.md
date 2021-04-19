---
title: Ochranná doba disponibility
description: Toto téma popisuje, jak nastavit ochranné lhůty disponibility, když používáte optimalizaci plánování. Ochranná lhůta disponibility označuje váš plánovací horizont a limit.
author: ChristianRytt
ms.date: 01/18/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqGroup, ReqItemTable, ReqPlanSched
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2021-01-18
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: dcb35eda718ea9b7573d8e994aa45216f8bd30a5
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5836559"
---
# <a name="coverage-time-fences"></a>Ochranná doba disponibility

Toto téma popisuje, jak nastavit *ochranné lhůty* disponibility, když používáte optimalizaci plánování. Plánovači mohou definovat horizont plánování (ochranná lhůta disponibility ve dnech) a vyloučit nabídku a poptávku, které přesahují tento horizont. Ochranné lhůty disponibility proto pomáhají předcházet „šumu“, který je způsoben návrhy dodávek, na které nemusíte měsíce reagovat. Mezi příklady patří prognóza pro příští rok a objednávky zákazníků, které jsou umístěny daleko za běžnou dodací lhůtu.

Ochranná lhůta disponibility je počet dní po dnešním datu (nebo přesněji datum, kdy provedete plánovací běh), kdy je vyloučena nabídka a poptávka. Abyste se vyhnuli zpožděním, musíte zajistit, aby časový limit disponibility byl delší než celková doba realizace. Výchozí systémová hodnota je 100 dní.

Ochranné lhůty disponibility můžete určit na každé z následujících úrovní:

- **Skupina disponibility** - Pro každou skupinu disponibility můžete nastavit výchozí časový limit disponibility.
- **disponibilita položky** - Můžete přepsat časový plot disponibility, který je zděděn od skupiny disponibility, která je přiřazena k položce.
- **Hlavní plán** - Můžete přepsat ochranné lhůty disponibility, které jsou zděděny ze skupiny disponibility a nastavení disponibility položky.

Následující části vysvětlují, jak určit skupinu disponibility na každé úrovni.

## <a name="set-a-coverage-time-fence-for-a-coverage-group"></a>Nastavení ochranné lhůty disponibility schválené žádosti pro skupinu disponibility

Když určíte časový limit disponibility pro skupinu disponibility, nastavení se použije pro všechny položky (produkty), které do této skupiny patří. Můžete však přepsat nastavení pro konkrétní položky nebo konkrétní hlavní plány.

Chcete-li určit časové ohraničení disponibility pro skupinu disponibility, postupujte takto.

1. Přejděte na **Hlavní plánování \> Nastavení \> Disponibilita \> Skupiny disponibility**.
1. Vyberte existující skupinu disponibility v seznamu, nebo vytvořte novou skupinu disponibility.
1. Na kartě s náhledem **Obecné** nastavte pole **Ochranná lhůta disponibility (dny)** na počet dní, které chcete použít jako ochrannou lhůtu disponibility pro skupinu disponibility.

## <a name="set-a-coverage-time-fence-for-a-specific-item"></a>Nastavení ochranné lhůty disponibility pro konkrétní položku.

Každá položka (produkt) patří do skupiny disponibility. Pokud položce není výslovně přiřazena žádná skupina disponibility, použije se výchozí skupina disponibility. Každá položka zdědí ochrannou lhůtu disponibility ze své skupiny disponibility. Tuto ochrannou lhůtu však můžete podle potřeby přepsat pro konkrétní položky.

Chcete-li určit časové ohraničení disponibility pro konkrétní položku, postupujte následovně.

1. Přejděte na **Řízení informací o produktech \> Produkty \> Uvolněné produkty**.
1. V mřížce vyberte produkt.
1. V podokně akcí na kartě **Plán** ve skupině **Disponibilita** vyberte **Disponibilita položky**.
1. Na stránce **Disponibilita položky** na kartě **Přehled** vyberte nebo vytvořte řádek pro web, kde chcete nastavit ochrannou lhůtu disponibility.
1. Vyberte kartu **Obecné** k otevření nastavení pro vybraný web.
1. Zaškrtněte políčko **Přepsat skupinu disponibility**.
1. Nastavte pole **Ochranná lhůta disponibility (dny)** na počet dní, které chcete použít jako ochrannou lhůtu disponibility pro skupinu disponibility.

## <a name="set-a-coverage-time-fence-for-a-specific-master-plan"></a>Nastavení ochranné lhůty disponibility pro konkrétní hlavní plán.

Ochrannou lhůtu disponibility můžete určit na úrovni hlavního plánu: Tímto způsobem definujete počet dní, které výpočet hlavního plánu pokrývá pro hlavní plán. Toto nastavení přepíše všechna nastavení času disponibility, která byla definována pro každou relevantní položku a skupinu disponibility.

Chcete-li určit časové ohraničení disponibility pro konkrétní hlavní plán, postupujte následovně.

1. Přejděte na **Hlavní plánování \> Nastavení \> Plány \> Hlavní plány**.
1. Vyberte v seznamu existující hlavní plán nebo vytvořte nový hlavní plán.
1. Na kartě s náhledem **Ochranné lhůty ve dnech** nastavte možnost **Disponibilita** na *Ano*. Pak v poli pod možností zadejte počet dní, které chcete použít jako ochrannou lhůtu disponibility pro hlavní plán.

## <a name="considerations-for-coverage-time-fences"></a>Úvahy o ochranných lhůtách disponibility

Při nastavování ochranných lhůt disponibility zvažte následující body:

- Ochranné lhůty disponibility ovlivňují pouze vstupní data pro hlavní plánování. Pokud dojde ke zpožděním, výsledné plánované objednávky mohou mít datum, které je po dnešním datu plus ochranná lhůta disponibility.
- Ochranné lhůty disponibility jsou uvedeny v kalendářních dnech. Kalendáře, které používají pracovní dny, neovlivní výpočet ochranné lhůty. Například týden je vždy považován za sedm dní, i když jsou víkendy v kalendáři pracovní doby nastaveny jako zavřené dny.
- Transakce požadavků nebudou generovány pro žádnou nabídku a poptávku, která spadá mimo ochrannou lhůtu disponibility.
- Pokud jakákoli schválená nabídka a poptávka spadá mimo ochrannou lhůtu disponibility, nebude načtena do modulu. Proto nespustí žádné doplňování a nebudou se počítat zpoždění. Tato nabídka a poptávka by však neměla být ze systému vymazána.
- Změny množství bezpečných zásob (od minimálních klíčů) budou ignorovány, pokud spadnou mimo ochrannou lhůtu disponibility.
- Mezipodniková poptávka bude ignorována, pokud požadované datum odeslání, které je vypočítáno, není uvnitř ochranné lhůty disponibility. U integrovaného hlavního plánování není mezipodniková poptávka omezena ochrannou lhůtou disponibility.
- Předpovědi poptávky budou ignorovány, pokud datum rozpočtu není uvnitř ochranné lhůty disponibility. U integrovaného hlavního plánování nejsou prognózy poptávky omezeny ochrannou lhůtou disponibility.
- Optimalizace plánování zohledňuje časové pásmo. Zvažuje časové pásmo na místech nabídky a poptávky a čas plánování. Například hlavní plánování je spuštěno v 11:00 dne 15. října z webu v Dánsku (GMT + 1 časové pásmo) a je použita ochranná lhůta disponibility deset dnů. V takovém případě je nabídka a poptávka ze stránky v Seattlu (časové pásmo GMT-8) zahrnuta na 2:00 25. října (= deset 24 hodinových dní po spuštění hlavního plánování, minus časový rozdíl devíti hodin). Všimněte si, že vestavěný hlavní plánovací modul bere v úvahu pouze datum ochranné lhůty. Výsledek se proto může lišit.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]