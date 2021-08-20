---
title: Množství překračuje procento nedostatečné dodávky během generování dodacího listu
description: Když vygenerujete dodací list, odchozí náklad obsahuje množství, které přesahuje procento nedostatečné dodávky.
author: GalynaFedorova
ms.date: 5/31/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSSalesPackingSlipPost,WHSLoadPlanningListPage_WHSSalesPackingSlipPost,WHSLoadPlanningWorkbench_WHSSalesPackingSlipPost
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: ae02846c0ec937ebaff440dc5272a135e16c8aa7355ecc303929e760a54b6627
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6760291"
---
# <a name="quantity-exceeds-under-delivery-percentage-during-packing-slip-generation"></a>Množství překračuje procento nedostatečné dodávky během generování dodacího listu

Kód chyby: SYS24921

## <a name="symptoms"></a>Příznaky

Když vygenerujete dodací list, odchozí náklad obsahuje množství, které přesahuje procento nedostatečné dodávky.

Když se pokusíte vygenerovat dodací list, systém zobrazí následující chybovou zprávu:

> Snížení dodávky řádku je %1 procent, ale povolené snížení je pouze %2 procent.

Proto nemůžete vygenerovat dodací list pro zásilku.

## <a name="cause"></a>Příčina

Vybrané množství pro náklad nebo zásilku je menší než objednané množství a není v rozmezí procenta nedostatečné dodávky.

## <a name="resolution"></a>Řešení

Náklad nebo zásilka je aktuálně ve stavu, kdy se generování dodacího listu nezdaří. Chcete-li problém opravit, proveďte jeden nebo více z následujících úkolů:

- Upravte procento nedostatečné dodávky.
- Proveďte storno a úpravy.

### <a name="adjust-the-under-delivery-percentage"></a>Upravte procento nedostatečné dodávky

Následujícím postupem upravte procento nedostatečné dodávky.

1. Přejděte na **Pohledávky \> Objednávky \> Všechny objednávky**.
1. Vyberte prodejní objednávku, u které nemůžete zaúčtovat dodací list pro náklad.
1. Na kartě  **Řádky prodejní objednávky** vyberte řádek prodejní objednávky, který přesahuje procento nedostatečné dodávky.
1. Na kartě  **Detaily řádku** vyberte možnost **Doručení**.
1. Nastavte pole **Nedostatečná dodávka** na větší procento, které odpovídá množství, které bylo vyskladněno oproti množství naložení, aby mohlo pokračovat generování dodacího listu.

### <a name="reverse-and-make-adjustments"></a>Proveďte storno a úpravy

Stornujte vše, co bylo zaúčtováno pro náklad (například dodací list, potvrzení zásilky a práce), proveďte úpravy prodejní objednávky, znovu vydejte objednávku do skladu a dokončete postup odeslání.

Následujícím postupem zrušíte dodací list.

1. Přejděte na **Řízení skladu \> Náklady \> Všechny náklady**.
1. V podokně akcí na kartě  **Odeslat a přijmout** ve skupině  **Stornování** vyberte **Storno dodacích listů**.

Následujícím postupem stornujete potvrzení zásilky.

1. Přejděte na **Řízení skladu \> Náklady \> Všechny náklady**.
1. V podokně akcí na kartě  **Odeslat a přijmout** ve skupině  **Stornování** vyberte **Storno potvrzení zásilky**.

Storno práce můžete provést následujícím postupem.

1. Přejděte na **Řízení skladu \> Náklady \> Všechny náklady**.
1. V podokně Akce na kartě  **Náklady** ve skupině  **Práce** vyberte  **Stornovat práci**.
