---
title: Zásilku nemůžete potvrdit kvůli problému s kalendářem
description: Zásilku nemůžete potvrdit kvůli problému s kalendářem
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 8aae45beeef1934760d620874897f46a1cf901995e2b83e148a1d56898d9c717
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6735937"
---
# <a name="you-cant-confirm-a-shipment-because-of-an-issue-with-the-calendar"></a>Zásilku nemůžete potvrdit kvůli problému s kalendářem

Kód chyby: TRX2716

## <a name="symptoms"></a>Příznaky

Když se pokusíte potvrdit dodávku, systém zobrazí následující chybovou zprávu:

> Typ kalendáře %1 vyžaduje, aby byla schůzka %2 zaregistrována a zarezervována.

Proto nemůžete potvrdit dodání pro zásilku.

## <a name="cause"></a>Příčina

Aktivní události pro načtení existují. Například existuje pravidlo, které vyžaduje přihlášení řidiče. Náklad je proto aktuálně ve stavu, kdy se potvrzení zásilky nezdaří.

## <a name="resolution"></a>Rozlišení

Musíte prozkoumat a opravit všechny problémy s aktivními událostmi, které jsou spojeny s nákladem.

1. Přejděte na **Řízení skladu \> Náklady \> Všechny náklady**.
1. Vyberte dodávku, pro kterou nelze potvrdit odeslání.
1. V podokně akcí na kartě **Přeprava** ve skupině **Události** vyberte **Plánování událostí**.
1. Proveďte jeden z následujících kroků:

    - Ujistěte se, že check-in/check-out řidiče pro událost dokončen.
    - Dokončete nebo zrušte schůzku.
    - Zakažte možnost **Vyžaduje se přihlášení řidiče** souvisejícího pravidla události.
