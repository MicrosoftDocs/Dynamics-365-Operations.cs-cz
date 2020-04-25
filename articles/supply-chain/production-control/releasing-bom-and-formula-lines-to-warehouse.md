---
title: Uvolnění řádků kusovníku a receptury do skladu
description: Toto téma popisuje proces uvolnění suroviny pro řádky kusovníku a řádky receptury do skladu.
author: johanhoffmann
manager: tfehr
ms.date: 10/30/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysOperationTemplateForm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: dd28e6f96f70c261edc9ba85a9356a704335382b
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/02/2020
ms.locfileid: "3211185"
---
# <a name="release-bom-and-formula-lines-to-the-warehouse"></a>Uvolnění řádků kusovníku a receptury do skladu

[!include [banner](../includes/banner.md)]

Toto téma popisuje proces uvolnění suroviny pro řádky kusovníku a řádky receptury do skladu. Když uvolníte řádek kusovníku nebo receptury do skladu, systém nejdříve určí, zda je materiál již dostupný na vstupním místě pro výrobu v dílenském zařízení materiál, kde bude materiální spotřebován pro výrobní proces.

- Pokud je materiál k dispozici na umístění výrobního vstupu, je vydán z tohoto umístění ihned po přijetí signál pro uvolnění materiálu do skladu.
- Není-li materiál k dispozici na vstupní místě výroby, uvolnění materiálu označuje, že materiál musí být přesunut z místa ve skladu do vstupního místa výroby. Materiál je přesunut prostřednictvím skladové práce pro výdej suroviny. Z tohoto důvodu musí být nakonfigurovány skladové procesy pro výdej suroviny. Další informace naleznete v tématech [Přehled doplnění](../warehousing/replenishment.md) a [Řízení práce ve skladu pomocí šablon práce a směrnic skladového místa](../warehousing/control-warehouse-location-directives.md).

## <a name="methods-for-releasing-bom-and-formula-lines"></a>Metody pro uvolnění řádků kusovníku a receptury

Uvolnění řádků kusovníku a receptury můžete nakonfigurovat tak, aby k němu došlo v rámci uvolnění výrobní zakázky nebo dávkové objednávky. Popřípadě lze uvolnění kontrolovat dávkovou úlohou nebo provést jako ruční interakci.

Metoda, která se používá k uvolnění řádků kusovníku a řádků receptury je řízena parametrem **Uvolnění řádku výroby**. Tento parametr lze najít v **Řízení výroby** \> **Nastavení** \> **Parametry výroby**.

- **Uvolnění řádků kusovníku a řádků receptury jako součást výrobní zakázky nebo dávkové objednávky** – v této metodě se řádky kusovníku a receptury pro výrobní zakázku nebo dávkovou objednávku uvolňují součást procesu uvolnění objednávky. Obvykle se během uvolnění výrobní zakázky nebo dávkové úlohy uvolňují výrobní úlohy dílenským pracovníkům a vytisknout se výrobní doklady. Během tohoto procesu se stav objednávky také změní na **Uvolněno**.
- **Uvolnění řádků kusovníku receptury pomocí dávkové úlohy nebo jako ruční interakce** – v této metodě lze řádky kusovníku a receptury uvolnit pouze prostřednictvím dávkové úlohy **Automaticky uvolnit řádky kusovníku a receptury** nebo ruční interakcí. Chcete-li ručně uvolnit řádky kusovníku a řádky receptury, na stránce se seznamem výrobních zakázek nebo na stránce s podrobnostmi výrobních zakázek v podokně akcí zvolte **Uvolnit do skladu**.

Pro rychlou ukázku, jak uvolnit kusovník a řádky receptury do výroby pomocí dávkové úlohy, uvádí toto krátké video YouTube: [Vydání vyzvednutí výroby ve skladu v dávkách](https://www.youtube.com/watch?v=8urAJn50dQ8).

## <a name="releasing-the-bom-and-formula-lines-by-using-a-batch-job"></a>Uvolnění řádků kusovníku a receptury pomocí dávkové úlohy

Dávková úloha **Automaticky uvolnit řádky kusovníku a receptury** prochází přes vybrané řádky kusovníku a receptury, které mají zbývající množství pro uvolnění. Úloha bere v úvahu pouze objednávky, které mají stav **Uvolněno**, **Zahájeno** nebo **Hlášeno jako dokončené**. Pokud má řádek kusovníku nebo receptury zbývající množství k uvolnění, úloha se uvolní až do množství, které lze pokrýt množstvím, které již bylo fyzicky rezervováno, a množstvím, které je fyzicky k dispozici.

### <a name="example-of-a-batch-job-release"></a>Příklad uvolnění dávkové úlohy

| Scénář | Zbývající množství k uvolnění | Fyzicky rezervované množství | Fyzicky dostupné množství | Množství uvolněné dávkovou úlohou |
|----------|-------------------------------|------------------------------|-------------------------------|------------------------------------|
| 1        | 100                           | 20                           | 90                            | 100                                |
| 2        | 100                           | 20                           | 70                            | 90                                 |
| 3        | 100                           | 0                            | 90                            | 90                                 |
| 4        | 100                           | 0                            | 110                           | 100                                |
| 5        | 100                           | 20                           | 0                             | 20                                 |

### <a name="batch-job-setup"></a>Nastavení dávkové úlohy

V dotazu pro dávkovou úlohu **Automaticky uvolnit řádky kusovníku a receptury** můžete nastavit kritéria filtru a určit, o kolik dní dopředu má úloha hledat řádky, které mají neuvolněné množství. V dotazu pro úlohu v poli **Datum suroviny** použijte funkci **(LessThanDate())** jako kritérium filtru.

Následující obrázek znázorňuje výrobní zakázku, která obsahuje dvě úlohy, 10 a 20, které pokrývá sestavení a balení pro výrobní zakázku. Každá úloha je nastavena na spotřebu množství materiálu. Na tomto obrázku se časový limit uvolnění označený zelenou šipkou pod časovou osou rovná počtu dní zadanému v kritériu **(LessThanDate())**. Například **(LessThanDate(2))** označuje, že úlohu má hledat neuvolněné množství pouze v rámci doby dvou dnů.

![Příklad výrobní zakázky, která má dvě dávkové úlohy](media/bach-job-setup.PNG)

## <a name="releasing-material-per-operation-number-or-in-proportion-to-the-amount-of-finished-goods"></a>Uvolnění materiálu podle čísla operace nebo v poměru k množství dokončeného zboží

Pokud uvolníte materiály pomocí nastavení parametru **Uvolnění na výrobní zakázce** máte dvě možnosti ke kontrole uvolnění materiálu při provádění ručního uvolnění:

- Uvolnit materiál podle čísla operace.
- Uvolnit materiál v poměru k množství dokončeného zboží.

### <a name="release-material-per-operation-number"></a>Uvolnění materiálu podle čísla operace

Chcete-li kontrolovat operace, ke kterým má být uvolněn materiál, použijte stránku **Uvolnit do skladu**.

- Vyberte **Řízení výroby** \> **Výrobní zakázky** \> **Všechny výrobní zakázky**, vyberte výrobní zakázku a pak na kartě **Sklad** zvolte **Uvolnit do skladu**. Poté použijte pole **Od operace č.** a **Do operace č.** k určení rozsahu čísel operací.

Následující obrázek znázorňuje výrobní zakázku, která má dvě operace, 10 a 20. Pokud v tomto příkladu omezíte uvolnění na operaci 10, pouze materiál M9203 bude uvolněn.

![Příklad uvolnění materiálu podle čísla operace](media/two-operations.PNG)

Pro rychlou ukázku vydání materiálu v poměru k množství dokončených výrobků se podívejte na toto krátké video na YouTube o [vylepšení procesu uvolnění výrobní zakázky](https://www.youtube.com/watch?v=Rm3ojAz6Zu0).

### <a name="release-material-in-proportion-to-the-amount-of-finished-goods"></a>Uvolnění materiálu v poměru k množství dokončeného zboží

Můžete uvolnit surovinu pro částečné množství dokončeného zboží nebo ve specifické jednotce.

- Chcete-li uvolnit surovinu pro částečné množství dokončeného zboží, vyberte **Řízení výroby** \> **Výrobní zakázky** \> **Všechny výrobní zakázky**, vyberte výrobní zakázku a pak na kartě **Sklad** zvolte **Uvolnit do skladu**. Poté zadejte množství v poli **Množství**.

    Například výrobní zakázka je vytvořena a naplánována na 1 000 kusů Vedoucí dílny plánuje výrobu 100 kusů. pro další směnu a chce uvolnění materiálů pouze pro tuto směnu. V takovém případě může vedoucí použít pole **Množství** pro uvolnění materiálů pro 100 kusů, který jsou plánovány pro další směnu.

- Chcete-li uvolnit surovinu v konkrétní jednotce, vyberte **Řízení výroby** \> **Výrobní zakázky** \> **Všechny výrobní zakázky**, vyberte výrobní zakázku a pak na kartě **Sklad** zvolte **Uvolnit do skladu**. Pak použijte pole **Jednotka** a vyberte jednotku dokončeného zboží, ve které se má materiál uvolnit.

    Jednotky, které jsou k dispozici, jsou definovány v ID skupiny klasifikace jednotek dokončeného zboží.

    Například dokončené zboží má následující převod jednotek mezi librami a paletami: 1 PL = 100 kg. Chcete-li vytvořit výrobní zakázku na 10 000 kg  dokončeného zboží, můžete uvolnit suroviny pro počet palet, které chcete vyrobit. Vyberte **PL** jako jednotku a vyberte odpovídající číslo v poli **Množství**.
