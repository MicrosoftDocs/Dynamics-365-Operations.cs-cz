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
ms.openlocfilehash: 801778fc8f04b106bf168a3dcd5a89767a837740
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/13/2021
ms.locfileid: "7344257"
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
