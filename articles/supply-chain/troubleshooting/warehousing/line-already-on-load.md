---
title: Jedna z linek již je vytížena
description: Tato stránka vysvětluje, proč se vám zobrazila chyba „Jedna z linek již je vytížena. Nelze uvolnit do skladu “a jak problém vyřešit.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 0bdfaed005b9c58f7bd5f87dd6dffe648de47261
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475846"
---
# <a name="one-of-the-lines-is-already-on-a-load"></a>Jedna z linek již je vytížena

## <a name="symptoms"></a>Příznaky

Při práci s budováním vytížení a zásilek se může zobrazit následující chybová zpráva:

> Jedna z linek již je vytížena. Nelze uvolnit do skladu.

Pokud ručně vytvoříte náklady nebo nastavíte proces tak, aby se náklady již vytvořily před zadáním řádku prodejní objednávky, předpokládá se, že následné vydání bude provedeno ručně a že bude použita cesta a hodnocení z nákladu.

V jiném možném scénáři se pokoušíte provést automatické uvolnění do skladu, ale vlnovému procesu se nepodařilo vytvořit práci. Proto je stále vytvořena otevřená zásilka nebo náklad. Tato otevřená zásilka nebo náklad poté blokuje následné pokusy o automatické uvolnění objednávky, dokud otevřenou zásilku nebo náklad nezrušíte nebo ručně nezpracujete vlnu.

## <a name="resolution"></a>Řešení

Můžete uvolnit ze stránky prodejní objednávky nebo automatické uvolnění lze provést ze stránky prodejní objednávky, pouze pokud před vydáním do skladu neexistuje žádný náklad. Po zpracování vlny se náklad automaticky vytvoří.
