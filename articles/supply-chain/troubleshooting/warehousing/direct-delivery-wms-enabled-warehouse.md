---
title: Přímé doručení nelze zpracovat pro sklad s podporou WMS
description: Pokud má sklad povolený WMS, nepodporuje přímé doručení. Chcete-li použít přímé doručení, musíte vybrat položku a sklad, který nespadá do WMS.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 090e17091e9fb92c2065679bb9b04637214e2eea
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475848"
---
# <a name="direct-delivery-not-able-to-process-for-wms-enabled-warehouse"></a>Přímé doručení nelze zpracovat pro sklad s podporou WMS

## <a name="symptoms"></a>Příznaky

Pokud je položka přidána na prodejní řádek pro přímé dodání ze skladu, který má povolenou správu skladu (WMS), při aktualizaci prodejní linky se zobrazí následující chybová zpráva:

> Přímé doručení není možné zpracovat pro sklad 1%, protože má povolenou správu skladu. Zadejte prosím jiný sklad, který nemá povolenou správu skladu.

## <a name="resolution"></a>Řešení

Společnost Microsoft vyhodnotila tento problém a zjistila, že jde o omezení funkcí. V současné době WMS nepodporuje přímé doručování. Chcete-li tedy použít přímé doručení, musíte vybrat položku a sklad, který nespadá do WMS.
