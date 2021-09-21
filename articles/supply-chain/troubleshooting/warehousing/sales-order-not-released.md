---
title: Prodejní objednávku nebylo možné uvolnit s odchozími skladovými operacemi
description: Existuje několik důvodů, proč se může zobrazit chybová zpráva, že prodejní objednávku nelze uvolnit. Tato stránka vysvětluje, proč a jak tento problém zmírnit.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: fca5ee1bc97545ea4de56d940fdedd320a6cfe84
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475811"
---
# <a name="sales-order-could-not-be-released-with-outbound-warehouse-operations"></a>Prodejní objednávku nebylo možné uvolnit s odchozími skladovými operacemi

## <a name="symptoms"></a>Příznaky

Při práci s odchozími skladovými operacemi se může zobrazit následující chybová zpráva:

> Prodejní objednávku nelze uvolnit.

## <a name="cause"></a>Příčina

K tomuto problému může dojít z několika důvodů. Například je objednávka blokována správou kreditů a není možné vytvářet žádné zásilky, dokud nezadáte platnou poštovní adresu pro všechny prodejní řádky spojené s objednávkou. Alternativně existuje blokování objednávky, které musí být vyřešeno, než bude možné objednávku uvolnit do skladu. Toto pozastavení může být specifické pro objednávku nebo může být na zákaznickém účtu.

## <a name="resolution"></a>Řešení

Přidejte nebo aktualizujte adresu na řádcích prodejní objednávky a objednávky a poté objednávku uvolněte do skladu. Objednávky lze do skladu uvolnit, pouze pokud mají platnou dodací adresu (podle nastavení formátu adresy v modulu **Správa organizace**).

Prozkoumejte pozastavení objednávky a vyřešte problémy. Poté odeberte blokování objednávky nebo zákazníka a uvolněte objednávku do skladu.
