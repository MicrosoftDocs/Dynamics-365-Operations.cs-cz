---
title: Nelze vložit aktivní verzi kusovníku a čísla trasy
description: Pokud jsou již definovány výchozí pracoviště a sklad pro vybraný produkt, nebudete vyzváni k vložení čísel kusovníku a postupu.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 241618d70f01c85df946a48493f5d84e0964218e
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475749"
---
# <a name="cant-insert-bill-of-material-and-route-when-creating-a-new-production-order"></a>Při vytváření nové výrobní zakázky nelze vložit kusovník a trasu

## <a name="symptoms"></a>Příznaky

Když vytvoříte novou výrobní zakázku, po zadání čísla položky jsou pole **Pracoviště** a **Sklad** automaticky nastavena na výchozí pracoviště a sklad, které jsou definovány na stránce **Výchozí nastavení objednávky** pro položku dokončeného zboží. Kromě toho se automaticky zadává aktivní číslo kusovníku a číslo trasy, takže neobdržíte následující zprávu, která vás vyzve k zadání těchto hodnot:

> Vložit aktivní verzi pro kusovník a postup?

## <a name="resolution"></a>Řešení

Pokud vyberete produkt, pro který jsou pracoviště a sklad již definovány na stránce **Výchozí nastavení objednávky**, nebudete vyzváni k vložení čísel kusovníku a postupu. Zobrazí se výzva, pouze pokud tyto hodnoty nejsou pro vybraný produkt definovány.
