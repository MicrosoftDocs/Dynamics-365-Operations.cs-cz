---
title: Dodávku nemůžete potvrdit, protože množství překračuje procento navýšení dodávky
description: Dodávku nemůžete potvrdit, protože množství překračuje procento navýšení dodávky
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
ms.openlocfilehash: b25050572662afebbeaa39fa5a96e70cef618ac671dceba189fab1315480ede2
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6755148"
---
# <a name="you-cant-confirm-a-shipment-because-the-quantity-exceeds-the-overdelivery-percentage"></a>Dodávku nemůžete potvrdit, protože množství překračuje procento navýšení dodávky

Kód chyby: WAX1687

## <a name="symptoms"></a>Příznaky

Když se pokusíte potvrdit dodávku, systém zobrazí následující chybovou zprávu:

> Dodávku pro náklad %1 nelze potvrdit, protože množství pro položku %2 překračuje procento definované pro navýšení dodávky.

Proto nemůžete potvrdit dodání pro zásilku.

## <a name="cause"></a>Příčina

Množství nákladu nebo dodávky bylo vyskladněno pouze částečně. Množství aktuálně převyšuje vybrané množství o procento, které je mimo povolené procento pro navýšení dodávky.

## <a name="resolution"></a>Rozlišení

Chcete-li problém opravit, proveďte jeden nebo více z následujících úkolů:

- Nastavte množství řádku nákladu.
- Nastavte procento navýšení dodávky.

### <a name="set-the-load-line-quantity"></a>Nastavení množství řádku nákladu

Chcete-li nastavit množství řádku nákladu, postupujte takto.

1. Přejděte na **Řízení skladu \> Náklady \> Všechny náklady**.
1. Vyberte dodávku, pro kterou nelze potvrdit odeslání.
1. Na záložce s náhledem **Řádky nákladu** vyberte řádek nákladu, který přesahuje procento pro navýšení dodávky.
1. Na záložce s náhledem **Detaily řádku** vyberte možnost **Objednat**.
1. V poli **Množství** nastavte hodnotu na vyskladněné množství (tj. na hodnotu **Množství vytvořené prací**), aby mohlo dojít k potvrzení dodávky.

### <a name="set-the-overdelivery-percentage"></a>Nastavení procenta navýšení dodávky

Chcete-li nastavit procenta snížení dodávky, postupujte takto.

1. Přejděte na **Řízení skladu \> Náklady \> Všechny náklady**.
1. Vyberte dodávku, pro kterou nelze potvrdit odeslání.
1. Na záložce s náhledem **Řádky nákladu** vyberte řádek nákladu, který přesahuje procento pro navýšení dodávky.
1. Na záložce s náhledem **Detaily řádku** vyberte možnost **Obecné**.
1. V poli **Navýšení dodávky** nastavte hodnotu na větší procento, které odpovídá množství, které bylo vybráno oproti množství naložení, aby mohlo dojít k potvrzení dodávky.
