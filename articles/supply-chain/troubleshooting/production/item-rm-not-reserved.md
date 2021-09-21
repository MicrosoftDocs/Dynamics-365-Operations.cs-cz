---
title: Položku RM nelze uvolnit, když je vydána výrobní zakázka
description: 'Při uvolňování výrobní zakázky se může zobrazit chyba: „Položku RM nelze plně rezervovat.“ Zajistěte, aby bylo k dispozici plné množství, nebo si položky rezervujte ručně.'
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 528895252d661bb012f49190c15853989833064d
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475823"
---
# <a name="item-rm-cant-be-fully-reserved-when-a-production-order-is-released"></a>Položku RM nelze plně uvolnit, když je vydána výrobní zakázka

## <a name="symptoms"></a>Příznaky

Pokud nejsou všechny položky řádku kusovníku fyzicky dostupné, když je do skladu uvolněna výrobní zakázka, a zásada **Uvolnění do skladu** je nastavena na *Vyžadovat úplnou rezervaci* ve výrobní zakázce, zobrazí se následující chybová zpráva:

> Položku RM nelze plně rezervovat. Ujistěte se, že je k dispozici celé množství, nebo položky rezervujte ručně, pokud je pole Rezervace na řádku kusovníku nastaveno na Ručně nebo Spuštěno. Výrobní zakázku nebylo možné uvolnit do skladu, protože nebylo možné rezervovat některé materiály.

## <a name="resolution"></a>Řešení

Toto chování je záměrné a funguje podle očekávání. Při řešení tohoto problému postupujte podle pokynů uvedených v chybové zprávě: "Zajistěte, aby bylo k dispozici úplné množství, nebo si položky rezervujte ručně, pokud je pole Rezervace na řádku kusovníku nastaveno na Ručně nebo Spuštěno."
