---
title: Množství překračuje procento nadměrné dodávky během generování dodacího listu
description: Když vygenerujete dodací list, odchozí náklad obsahuje množství, které přesahuje procento nadměrného doručení.
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
ms.openlocfilehash: 1106322cc3772c1b671b7fa82fb74039c028ba35
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/14/2021
ms.locfileid: "6249070"
---
# <a name="quantity-exceeds-over-delivery-percentage-during-packing-slip-generation"></a>Množství překračuje procento nadměrné dodávky během generování dodacího listu

Kód chyby: SYS24920

## <a name="symptoms"></a>Příznaky

Když vygenerujete dodací list, odchozí náklad obsahuje množství, které přesahuje procento nadměrného doručení.

Když se pokusíte vygenerovat dodací list, systém zobrazí následující chybovou zprávu:

> Navýšení dodávky řádku je %1 procent, ale povolené navýšení je pouze %2 procent.

Proto nemůžete vygenerovat dodací list pro zásilku.

## <a name="cause"></a>Příčina

Vybrané množství pro náklad nebo zásilku je větší než objednané množství a není v rozmezí procenta nadměrného doručení.

## <a name="resolution"></a>Řešení

Náklad nebo zásilka je aktuálně ve stavu, kdy se generování dodacího listu nezdaří. Chcete-li problém opravit, proveďte jeden nebo více z následujících úkolů:

- Upravte množství řádku nákladu.
- Upravte procento navýšení dodávky.
- Proveďte storno a úpravy.

### <a name="adjust-the-load-line-quantity"></a>Upravte množství řádku nákladu

Následujícím postupem upravte množství řádku nákladu.

1. Přejděte na **Řízení skladu \> Náklady \> Všechny náklady**.
1. Vyberte náklad, pro který nelze vygenerovat dodací list.
1. V podokně akcí na kartě  **Odeslat a přijmout** ve skupině  **Stornování** vyberte **Storno potvrzení zásilky**.
1. Na kartě  **Řádky nákladu** vyberte řádek nákladu, který přesahuje procento navýšení dodávky.
1. Vyberte **Snížit vydané množství** a upravte vydané množství.
1. Na kartě  **Detaily řádku** vyberte možnost **Objednat**.
1. Nastavte pole **Množství** na vyskladněné množství (tj. na hodnotu pole **Množství vytvořené prací**), aby mohlo dojít k vygenerování dodacího listu.

### <a name="adjust-the-over-delivery-percentage"></a>Upravte procento navýšení dodávky

Následujícím postupem upravte procento navýšení dodávky.

1. Přejděte na **Pohledávky \> Objednávky \> Všechny objednávky**.
1. Vyberte prodejní objednávku, u které nemůžete zaúčtovat dodací list pro náklad.
1. Na kartě  **Řádky prodejní objednávky** vyberte řádek prodejní objednávky, který přesahuje procento navýšení dodávky.
1. Na kartě  **Detaily řádku** vyberte možnost **Doručení**.
1. Nastavte pole **Navýšení dodávky** na větší procento, které odpovídá množství, které bylo vyskladněno oproti množství naložení, aby mohlo pokračovat generování dodacího listu.

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
