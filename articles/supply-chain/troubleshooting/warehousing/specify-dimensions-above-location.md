---
title: Nelze uvolnit zatížení pro částečné množství s hierarchií nad dávkami
description: Při použití položky s hierarchií rezervací nad dávkou musí řádky načtení určit rozměry nad místem, aby mohly být přiděleny zásoby.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: eb7e71cc271903cb689c33777b72862246f2dd42
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475771"
---
# <a name="cant-release-a-load-for-partial-quantity-with-batch-above-reservation-hierarchy"></a>Nelze uvolnit zatížení pro částečné množství s hierarchií rezervací nad dávkami

## <a name="symptoms"></a>Příznaky

Pokud používáte položku, která má hierarchii rezervací *batch-above*, příkaz **Uvolnit do skladu** na stránce **Pracovní plocha plánování nákladu** nefunguje, pokus se pokusíte uvolnit náklad pro částečné množství. Zobrazí se následující chybová zpráva:

> Aby bylo možné přiřadit vlně, musí řádky nákladu určit dimenze nad umístěním. Chcete-li přiřadit tyto dimenze, zarezervujte a znovu vytvořte řádek nákladu.

Pokud však použijete položku, která má hierarchii rezervací *batch-below*, můžete uvolnit náklad pro částečné množství ze stránky **Pracovní plocha plánování nákladu**.

## <a name="cause"></a>Příčina

Když je některá dimenze nad dimenzí **Skladové místo** v hierarchii rezervací, musí být zadána před uvolněním do skladu. Zásoby lze úspěšně přidělit pouze v případě, že v dimenzích nad skladovým místem nejsou žádné mezery.

## <a name="resolution"></a>Řešení

Zajistěte, aby všechny výše uvedené dimenze **Místo** byly přiřazeny rezervací a obnovením řádku nákladu.
