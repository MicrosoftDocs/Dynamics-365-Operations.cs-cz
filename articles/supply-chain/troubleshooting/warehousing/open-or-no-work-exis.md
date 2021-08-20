---
title: Zásilku nemůžete potvrdit z důvodu nedokončené nebo chybějící práce
description: Zásilku nemůžete potvrdit z důvodu nedokončené nebo chybějící práce
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm, WHSContainerCloseDiag_WHSShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 59def4427f9fff32fd3839bb9f9b5d5cccdc7720f92a84f1af3adad596d8b352
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6730051"
---
# <a name="you-cant-confirm-a-shipment-because-of-incomplete-or-missing-work"></a>Zásilku nemůžete potvrdit z důvodu nedokončené nebo chybějící práce

Kód chyby: WAX515

## <a name="symptoms"></a>Příznaky

Když se pokusíte potvrdit dodávku, systém zobrazí následující chybovou zprávu:

> Expedici pro vytížení %1 nebylo možné potvrdit, protože musí být dokončena veškerá práce pro vytížení.

Proto nemůžete potvrdit dodání pro zásilku.

## <a name="cause"></a>Příčina

Náklad nebo zásilka je aktuálně ve stavu, kdy se potvrzení zásilky nezdaří. Než budete moci zásilku potvrdit, pro dodávku musí existovat alespoň nějaká práce a veškerá tato práce musí mít stav *Uzavřeno* nebo *Zrušeno*.

## <a name="resolution"></a>Rozlišení

Zkontrolujte související prodejní objednávky nebo objednávky přenosu pro dodávku nebo zásilku a ujistěte se, že všechny související práce byly dokončeny nebo zrušeny.

Se zásilkami a dodávkami můžete pracovat na několika stránkách. V následujících podsekcích je uvedeno několik příkladů.

### <a name="all-loads-page"></a>Stránka se všemi zásilkami

1. Přejděte na **Řízení skladu \> Náklady \> Všechny náklady**.
1. Vyberte dodávku, pro kterou nelze potvrdit odeslání.
1. V podokně akcí na kartě **Náklady** ve skupině **Související informace** vyberte **Práce**.
1. Zkontrolujte stav každého pracovního ID. Sleddujte každé ID práce, které nemá stav *Uzavřeno* nebo *Zrušeno*.
1. Když má každé ID práce status *Uzavřeno* nebo *Zrušeno*, zkuste zásilku potvrdit znovu.

### <a name="all-shipments-page"></a>Stránka se všemi dodávkami

1. Přejděte na **Řízení skladu \> Dodávky \> Všechny dodávky**.
1. Vyberte dodávku, kterou nelze potvrdit.
1. V podokně akcí na kartě **Dodávky** ve skupině **Práce** vyberte **Podrobnosti práce**.
1. Zkontrolujte stav každého pracovního ID. Sleddujte každé ID práce, které nemá stav *Uzavřeno* nebo *Zrušeno*.
1. Když má každé ID práce status *Uzavřeno* nebo *Zrušeno*, zkuste zásilku potvrdit znovu.

### <a name="all-work-page"></a>Stránka se všemi prácemi

1. Přejděte do **Řízení skladu \> Práce\> Všechny práce**.
1. Vyberte práci pro číslo objednávky, u které nelze zásilku potvrdit.
1. V podokně akcí na kartě **Dodávky** ve skupině **Dodávky** vyberte **Potvrdit dodávku**.
1. Zkontrolujte stav každého pracovního ID. Sleddujte každé ID práce, které nemá stav *Uzavřeno* nebo *Zrušeno*.
1. Když má každé ID práce status *Uzavřeno* nebo *Zrušeno*, zkuste zásilku potvrdit znovu.
