---
title: Po zaúčtování z objednávky nelze zrušit dodací list
description: Když jsou pro WMS povoleny procesy výdeje a expedice, nemůžete zrušit dodací list poté, co je zaúčtován z prodejní objednávky. Tato stránka nabízí řešení.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: d20e66e2721560b8409eb63c3546a79adc188c7c
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475849"
---
# <a name="cant-cancel-a-packing-slip-after-its-posted-from-a-sales-order"></a>Po zaúčtování z prodejní objednávky nelze zrušit dodací list

## <a name="symptoms"></a>Příznaky

Když jsou pro pokročilé řízení skladu (WMS) povoleny procesy výdeje a expedice, nemůžete zrušit dodací list poté, co je zaúčtován z prodejní objednávky.

## <a name="resolution"></a>Řešení

Chcete-li opravit zaúčtované dodací listy pro položky, které jsou povoleny pro WMS, musíte zaúčtování provést z nákladu, nikoli přímo z objednávky. Společnost Microsoft vyhodnotila tento problém a zjistila, že jde o omezení funkcí.  

Obecně platí, že u prodejní objednávky, která byla vybrána a odeslána prostřednictvím procesů správy skladu, může být dodací list aktualizován z nákladu nebo dodávky a samotného dokladu prodejní objednávky. Pokud však u prodejní objednávky aktualizujete dodací list z dokladu prodejní objednávky, nelze přesto z nákladu nebo prodejní objednávky provést změnu dodacího listu. Proto doporučujeme použít zaúčtování dodacího listu z nákladu. V takovém případě bude povolen reverz, který musí být proveden z nákladu.
