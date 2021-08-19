---
title: Zobrazí se výzva k uložení nastavení pokrytí položky, i když jste neprovedli žádné změny
description: Zobrazí se výzva k uložení nastavení pokrytí položky, i když jste neprovedli žádné změny.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: DataManagementWorkspace_
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: angarmas
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 29ee23164430f219ff3d0c94216a8be43f480ce309f6cdac3dac6ed5b6d030af
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6730075"
---
# <a name="youre-prompted-to-save-item-coverage-settings-even-though-you-made-no-changes"></a>Zobrazí se výzva k uložení nastavení pokrytí položky, i když jste neprovedli žádné změny

Číslo článku znalostní báze: 4615588

## <a name="symptoms"></a>Příznaky

V některých scénářích se může zobrazit následující zpráva po otevření stránky **Pokrytí položky** po importu položek pomocí entity *Pokrytí položky V2*:

> Chcete před zavřením uložit změny?

Tuto zprávu obdržíte, i když jste neprovedli žádné změny.

## <a name="resolution"></a>Řešení

Stránka **Pokrytí položky** obsahuje složitou výchozí logiku, která může způsobit, že se zpráva zobrazí poté, co byly v databázi nedávno provedeny přímé změny, například prostřednictvím importu entity. Například pole entity `AREGENERALSETTINGSOVERRIDDEN` je nastaveno na *Ne*, ale importujete soubor, který poskytuje nové nebo upravené hodnoty pro pole, jako je `PRODUCTCOVERAGEGROUPID` a/nebo `VENDORACCOUNTNUMBER`. V tomto případě, jelikož je pole `AREGENERALSETTINGSOVERRIDDEN` nastaveno na *Ne*, hodnoty se automaticky vymažou z polí, když otevřete stránku **Pokrytí položky** poprvé po importu. Pokud změny uložíte podle pokynů v okně se zprávou, uloží se do databáze. Jinak obdržíte stejnou zprávu při příštím otevření stránky.

Chcete-li zabránit tomuto chování, ale také zahrnout hodnoty pro pole, jako je `PRODUCTCOVERAGEGROUPID` prostřednictvím importu entity, nastavte `AREGENERALSETTINGSOVERRIDDEN` na *Ano* při importu.
