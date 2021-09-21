---
title: Chyba consumptionCost kusovníků hodnoty nákladů při pokusu o ukončení objednávky
description: Při pokusu o ukončení výrobní zakázky se může zobrazit chybová zpráva, která říká, že hodnota spotřeby kusovníku musí být záporná. Tento problém byl vyřešen.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 737329d06022e899df8e4de5a27d76b21480da9e
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475803"
---
# <a name="cant-end-a-production-order-because-of-a-bom-consumptioncost-value-error"></a>Výrobní zakázku nelze ukončit z důvodu chyby hodnoty kusovníku spotřeby

## <a name="symptoms"></a>Příznaky

Když se pokusíte ukončit výrobní zakázku, zobrazí se následující chybová zpráva:

> Výpočet hodnoty consumptionCost kusovníku musí být při vydání ze skladu záporná.

## <a name="resolution"></a>Řešení

Tento problém byl opraven ve verzi 10.0.15.
