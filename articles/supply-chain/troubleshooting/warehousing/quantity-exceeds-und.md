---
title: Dodávku nemůžete potvrdit, protože množství překračuje procento snížení dodávky
description: Dodávku nemůžete potvrdit, protože množství překračuje procento snížení dodávky
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm,WHSContainerCloseDiag_WHSShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: a6a5b1140d1bc5d09a1bc582fb1d2ac9446fae0920cbb9957797dbdea4c684e6
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6760315"
---
# <a name="you-cant-confirm-a-shipment-because-the-quantity-exceeds-the-underdelivery-percentage"></a>Dodávku nemůžete potvrdit, protože množství překračuje procento snížení dodávky

Kód chyby: WAX1686

## <a name="symptoms"></a>Příznaky

Když se pokusíte potvrdit dodávku, systém zobrazí následující chybovou zprávu:

> Dodávku pro náklad %1 nelze potvrdit, protože množství pro položku %2 překračuje procento definované pro snížení dodávky.

Proto nemůžete potvrdit dodání pro zásilku.

## <a name="cause"></a>Příčina

Množství nákladu nebo dodávky bylo vyskladněno pouze částečně. Množství je aktuálně nižší než vyskladněné množství o procento, které je mimo povolené procento pro snížení dodávky.

## <a name="resolution"></a>Rozlišení

Chcete-li problém opravit, proveďte jeden nebo více z následujících úkolů:

- Nastavte množství řádku nákladu.
- Nastavte procenta snížení dodávky.

### <a name="set-the-load-line-quantity"></a>Nastavení množství řádku nákladu

Chcete-li nastavit množství řádku nákladu, postupujte takto.

1. Přejděte na **Řízení skladu \> Náklady \> Všechny náklady**.
1. Vyberte dodávku, pro kterou nelze potvrdit odeslání.
1. Na záložce s náhledem **Řádky nákladu** vyberte řádek nákladu, který přesahuje procento pro snížení dodávky.
1. Na záložce s náhledem **Detaily řádku** vyberte možnost **Objednat**.
1. V poli **Množství** nastavte hodnotu na vyskladněné množství (tj. na hodnotu **Množství vytvořené prací**), aby mohlo dojít k potvrzení dodávky.

### <a name="set-the-underdelivery-percentage"></a>Nastavení procenta snížení dodávky

Chcete-li nastavit procenta snížení dodávky, postupujte takto.

1. Přejděte na **Řízení skladu \> Náklady \> Všechny náklady**.
1. Vyberte dodávku, pro kterou nelze potvrdit odeslání.
1. Na záložce s náhledem **Řádky nákladu** vyberte řádek nákladu, který přesahuje procento pro snížení dodávky.
1. Na záložce s náhledem **Detaily řádku** vyberte možnost **Obecné**.
1. V poli **Snížení dodávky** nastavte hodnotu na větší procento, které odpovídá množství, které bylo vyskladněno oproti množství naložení, aby mohlo dojít k potvrzení dodávky.
