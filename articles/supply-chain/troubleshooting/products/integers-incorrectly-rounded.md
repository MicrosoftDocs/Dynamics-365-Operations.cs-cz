---
title: Při výpočtu modelů konfigurace produktu jsou nesprávně zaokrouhlena celá čísla
description: Při výpočtu modelů konfigurace produktu jsou nesprávně zaokrouhlena celá čísla. Opravte problém přidaným desetinným atributem a výpočtem.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: b17145d7d17cb784fe11b3fbf65ddf5aa5530f27
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475815"
---
# <a name="integers-incorrectly-rounded-when-product-configuration-models-are-calculated"></a>Při výpočtu modelů konfigurace produktu jsou nesprávně zaokrouhlena celá čísla

## <a name="symptoms"></a>Příznaky

K tomuto problému může dojít, když provedete následující řadu akcí:

1. Na produkčním konfiguračním modelu nastavte tyto atributy:

    - Vstup (celé číslo)
    - Procento (desetinné)
    - Výsledek (celé číslo)

2. Vytvořte výpočet, který má následující výraz:

    *Výsledek* = *Vstup* × *Procento* ÷ 100

V takovém případě není výsledek celého čísla vždy správně zaokrouhlený. Pokud je například vstup 1 000 a procento je 2,40, očekáváte celočíselný výsledek 24, protože 2,40 procenta z 1 000 je 24 (nebo 24,00 v desítkové formě). Místo toho je výsledek zobrazen jako 23. Když je však procento 2,39, výpočet se zaokrouhlí na 24 místo 23. Když je procento 2,5 výpočet se zaokrouhlí na 25 podle očekávání.

## <a name="cause"></a>Příčina

K tomuto problému dochází kvůli způsobu, jakým Microsoft Solver Foundation interně představuje čísla pomocí zlomků. V předchozím příkladu je výsledek výpočtu, kde je procento 2,40, reprezentován jako 27021597764222975 ÷ 1125899906842624 = 23,99999999999999911182158029987476766109466552734375. Když .NET převede tuto hodnotu na celé číslo, vrátí 23.

## <a name="resolution"></a>Řešení

Toto chování se nezmění, protože na něm závisí jiné scénáře. V předchozím příkladu můžete problém vyřešit zavedením dalšího desetinného atributu a výpočtů.

Například můžete nastavit na produkčním konfiguračním modelu následující atributy:

- Vstup (celé číslo)
- Procento (desetinné)
- ResultDecimal (desetinné)
- ResultInteger (celé číslo)

Poté můžete přidat následující výpočty:

- *ResultDecimal* = *Vstup* × *Procento* ÷ 100
- *ResultInteger* = *ResultDecimal*
