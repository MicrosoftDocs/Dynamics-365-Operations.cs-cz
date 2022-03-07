---
title: Zásilku nemůžete potvrdit, protože zákazník je blokován
description: Zásilku nemůžete potvrdit, protože zákazník je blokován.
author: GalynaFedorova
ms.date: 07/30/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-07-30
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 82b28e7cfd8c88e453cdd09398f5a92f605eab15a17d33defa0b9729a53c05b6
ms.sourcegitcommit: fa5ff2a0822aac16b518a2aea0d3389f79793390
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/07/2021
ms.locfileid: "7012145"
---
# <a name="you-cant-confirm-a-shipment-because-the-customer-is-on-hold"></a>Zásilku nemůžete potvrdit, protože zákazník je blokován

Kód chyby: WAX:CustomerOnHoldShipmentCannotBeConfirmed

## <a name="symptoms"></a>Příznaky

Když se pokusíte potvrdit dodávku, systém zobrazí následující chybovou zprávu:

> Dodávku %1 nelze potvrdit, protože zákazník je blokován pro %2.

Proto nemůžete potvrdit dodání pro zásilku.

## <a name="cause"></a>Příčina

Zákaznický účet vytížení nebo zásilky je blokován. Stav zákazníka proto nedovoluje zásilku potvrdit.

## <a name="resolution"></a>Řešení

K odblokování zákaznického účtu použijte následující postup.

1. Přejděte na **Pohledávky \> Odběratelé \> Všichni odběratelé**.
1. Otevřete zákaznický účet, u kterého nelze potvrdit zásilku.
1. Na záložce **Kredit a inkasa** nastavte pole **Blokované fakturace a dodávky** na *Ne*.
1. Tento postup opakujte pro všechny blokované zákazníky u vytížení.
