---
title: Plánování pracovního vytížení
description: Toto téma vysvětluje postup při nastavení a plánování kapacity pracovního vytížení pro zaměstnance v určitém skladu nebo pro celý sklad.
author: MarkusFogelberg
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSWorkloadCapacity
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4eac4838a4df8f1f5863f1ce1895e7aded5fb08b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5239271"
---
# <a name="schedule-workload-capacity"></a>Plánování pracovního vytížení

[!include[banner](../includes/banner.md)]

Můžete naplánovat kapacitu pracovního vytížení pro sklady a také projektovat současné i budoucí pracovní vytížení pro pracovníky v jednotlivých skladech. Můžete projektovat pracovní vytížení pro celý sklad, nebo můžete pracovní vytížení projektovat odděleně pro příchozí a odchozí pracovní vytížení.

Aby bylo možné projektování výstupu pracovního vytížení pro vybrané sklady, data hlavního plánování musí být k dispozici pro tyto sklady. Další informace o hlavních plánech naleznete v tématu [Přehled hlavních plánů](../master-planning/master-plans.md).

## <a name="schedule-and-view-workloads-for-a-warehouse"></a>Plánování a zobrazení pracovního vytížení skladu

Pokud chcete naplánovat kapacitu pracovního vytížení pro sklad, vytvořte nastavení pracovního vytížení pro jeden nebo více skladů a poté nastavení pracovního vytížení přidružte k hlavnímu plánu. V nastavení kapacity pracovního vytížení lze definovat limity na základě hmotnosti nebo objemu pro příchozí a odchozí transakce. Můžete také vytvořit více než jedno nastavení pro každý sklad a potom nastavení přidružit k jednotlivým hlavním plánům. Tento přístup můžete například využít v souladu se sezónními změnami stavu zaměstnanců.

Pokud zaměstnanci skladu pracují s transakcemi pro příchozí i odchozí pracovní vytížení, můžete nastavení kapacity skladu nakonfigurovat pro plánování pracovního vytížení v kombinovaném zobrazení.

Abyste mohli plánovat a zobrazovat pracovní vytížení pro sklady, musíte provést následující úkoly:

1. Vytvořte nastavení kapacity pracovního vytížení a definujte limity kapacity pracovního vytížení pro jeden nebo více skladů.
2. Přidružte nastavení kapacity pracovního vytížení k hlavnímu plánu, abyste mohli vytvářet projekce pracovního vytížení a určit, jak dlouho budou tyto projekce platit.

### <a name="create-a-workload-capacity-setup-for-a-warehouse"></a>Vytvoření nastavení kapacity pracovního vytížení pro sklad

1. Vyberte **řízení zásob** \> **nastavení** \> **sledování skladu** \> **Kapacita pracovního vytížení**.
2. V podokně akcí vyberte **nový** k vytvoření nastavení kapacity pracovního vytížení.
3. Na pevné záložce **Sklady** vyberte **Nový**, a potom zadejte hodnoty do řádku, čímž přidružíte sklad k nastavení kapacity pracovního vytížení.
4. Zaškrtněte políčko **kombinované vstupní a výstupní pracovní vytížení**, pokud by sestava **Kapacita pracovního vytížení** měla zobrazit celkové vytížení pro příchozí a odchozí transakce.
5. Na pevné záložce **Typy transakce** vyberte typy příchozích a odchozích transakcí, na které se budou limity pracovního vytížení vztahovat.

    > [!NOTE]
    > Je nutné vybrat alespoň jeden typ transakce pro příchozí i odchozí pracovní vytížení.

#### <a name="define-limits-for-volume-or-weight"></a>Definování limitů objemu nebo hmotnosti

Můžete nastavit limity pro objem či hmotnost podle toho, která omezení jsou relevantní pro zaměstnance skladu. Limity, které zadáte, jsou součástí projekce kapacity pracovního vytížení, kterou najdete v sestavě **Kapacita pracovního vytížení**.

Pro účely projekce informací o objemu a hmotnosti položek musí být pro všechny produkty určen standardní objem jedné skladové položky a hmotnost jedné skladové položky. Pole, která jsou vyžadována, jsou k dispozici v následujících skupinách polí na pevné záložce **správa skladu** stránky **podrobnosti uvolnění produktu**:

- Manipulace
- Fyzické rozměry
- Měření hmotnosti

Pokud tyto informace nejsou správně zadány, zobrazí se zpráva při generování sestavy **Kapacita pracovního zatížení**. Ze sestavy se pak můžete dostat až k chybějícím informacím, které jsou potřeba k projekci budoucího pracovního vytížení.

### <a name="associate-a-workload-capacity-setup-with-a-master-plan"></a>Přidružení nastavení kapacity pracovního vytížení k hlavnímu plánu

1. Vyberte **řízení zásob** \> **Periodicky** \> **pracovní vytížení plánu**.
2. V poli **Hlavní plán** vyberte hlavní plán k použití pro projekce pracovního vytížení.
3. V poli **Počet dní** zadejte počet dní, které má projekce pracovního vytížení pokrývat.
4. V poli **pracovní vytížení** vyberte nastavení pracovního vytížení, které má být přidruženo k hlavnímu plánu.

### <a name="view-workload-capacity"></a>Zobrazení kapacity pracovního vytížení

1. Vyberte **řízení zásob** \> **dotazy a sestavy** \> **sestavy fyzických zásob** \> **kapacita pracovního vytížení**.
2. V poli **Počet sloupců** určete počet sloupců, které chcete zobrazit v sestavě.
3. V poli **typ objednávky** vyberte **plánované a potvrzené**, **plánováno** nebo **potvrzeno** k označení typu objednávek pro plánování v sestavě.
4. V poli **Typ vytížení** výběrem typu vytížení určete, zda má být kapacita pracovního vytížení projektována v paletách, objemu či hmotnosti.
5. V poli **Kapacita pracovního vytížení** vyberte nastavení kapacity pracovního vytížení.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]