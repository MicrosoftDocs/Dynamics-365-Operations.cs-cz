---
title: Aktualizace plánovaných objednávek trvá dlouho
description: Při aktualizaci požadovaného množství anebo data dodání u plánované objednávky uložení aktualizace obvykle trvá alespoň 30 sekund na objednávku
author: ChristianRytt
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: ccf3305cc18ea0ccf2ac3e9ca0dd507fd12a9da7
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475809"
---
# <a name="planned-orders-take-a-long-time-to-update"></a>Aktualizace plánovaných objednávek trvá dlouho

## <a name="symptoms"></a>Příznaky

Při aktualizaci požadovaného množství anebo data dodání u plánované objednávky uložení aktualizace obvykle trvá alespoň 30 sekund na objednávku.

## <a name="resolution"></a>Řešení

Toto je známý problém s integrovaným modulem hlavního plánování. Je to způsobeno podkladovým automatickým rozpadem skrz strukturu kusovníku během úprav. Tomuto problému se věnuje optimalizace plánování, kde plánovač může aktualizovat a schválit příslušné objednávky a v případě potřeby spustit plánovací běh k aktualizaci plánovaných objednávek pro podkladovou strukturu kusovníku.

Jedním ze způsobů, jak zlepšit výkon pomocí integrovaného modulu hlavního plánování, je provést následující kroky:

1. Přejděte na **Hlavní plánování \> Nastavení \> Plány \> Hlavní plány**.
1. Vyberte plán.
1. Rozbalte záložku s náhledem **Ochranné doby ve dnech**.
1. Nastavte **Rozpad** na *Ano* a nastavte pole pod tímto nastavením na 0 (nula).

> [!NOTE]
> Tím se omezí doba rozpadů provedených pro tento hlavní plán na jeden den.
