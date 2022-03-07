---
title: Zbývající fyzické množství v jednotce nesmí být nula
description: Když vygenerujete dodací list, data, která se do něj dodávají, mají nenulové množství zásob, ale nulové množství prodeje.
author: GalynaFedorova
ms.date: 5/31/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadPlanningListPage_WHSSalesPackingSlipPost, WHSLoadTable_WHSSalesPackingSlipPost
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: bfd381160bcfd1e6e5489e16cc22178b8a5142ee
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/14/2021
ms.locfileid: "6248770"
---
# <a name="physical-remaining-quantity-in-the-unit-must-not-be-zero"></a>Zbývající fyzické množství v jednotce nesmí být nula

Kód chyby: SYS19591

## <a name="symptoms"></a>Příznaky

Když vygenerujete dodací list, data, která se do něj dodávají, mají nenulové množství zásob, ale nulové množství prodeje.

Když se pokusíte vygenerovat dodací list, systém zobrazí následující chybovou zprávu:

> Fyzický zůstatek v jednotce %1 nesmí být roven nule.

Proto nemůžete vygenerovat dodací list pro zásilku.

## <a name="cause"></a>Příčina

Systém vyhodnotí zbývající fyzické množství v skladové jednotce a zbývající fyzické množství v přepravní jednotce. Pokud systém zjistí, že zbývající fyzické množství v přepravní jednotce je 0 (nula), ale fyzické zbývající množství v jednotce zásob není 0, nemůžete vygenerovat dodací list. Například k tomuto problému může dojít, pokud se prodejní jednotka a jednotka zásob u položky liší a převod mezi jednotkami není přesný.

## <a name="resolution"></a>Řešení

Náklad nebo zásilka je aktuálně ve stavu, kdy se generování dodacího listu nezdaří. Chcete-li problém opravit, proveďte jeden nebo více z následujících úkolů:

- Zkontrolujte řádky nákladu a ujistěte se, že všechny související práce byly dokončeny na konečném místě přepravy a že množství odpovídá.
- Zkontrolujte řádky nákladu a proveďte úpravy, abyste zajistili, že množství lze čistě převést bez problémů se zaokrouhlováním.
- Zkontrolujte řádky nákladu a proveďte úpravy, abyste se ujistili, že jednotka a množství jsou zarovnány s desetinnou přesností jednotky.
- Ujistěte se, že měrná jednotka zásob je menší než měrná jednotka prodeje.

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a>Zkontrolujte řádky nákladu a ujistěte se, že všechny související práce byly dokončeny na konečném místě přepravy a že množství odpovídá

Pomocí následujících kroků zkontrolujte řádky nákladu a ujistěte se, že všechny související práce byly dokončeny na konečném místě přepravy a že množství odpovídá

1. Přejděte na **Řízení skladu \> Náklady \> Všechny náklady**.
1. Vyberte dodávku, pro kterou nelze potvrdit odeslání.
1. Na záložce s náhledem **Řádky nákladu** vyberte řádek nákladu.
1. Poznamenejte si hodnotu pole **Množství vytvořených prací**.
1. V podokně akcí na kartě **Náklady** ve skupině **Související informace** vyberte **Práce**.
1. Ověřte, že práce byla dokončena na konečném místě přepravy a že vybrané množství práce odpovídá vytvořenému množství práce na řádku zatížení.
1. Tento postup opakujte pro všechny řádky nákladů, abyste se ujistili, že jsou splněna všechna kritéria.

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-quantity-can-be-cleanly-converted-without-rounding-issues"></a>Zkontrolujte řádky nákladu a proveďte úpravy, abyste zajistili, že množství lze čistě převést bez problémů se zaokrouhlováním

Pomocí následujícího postupu zkontrolujte řádky nákladu a proveďte úpravy, abyste zajistili, že množství lze čistě převést bez problémů se zaokrouhlováním.

1. Přejděte na **Řízení skladu \> Náklady \> Všechny náklady**.
1. Vyberte náklad, pro který nelze vygenerovat dodací list.
1. V podokně akcí na kartě  **Odeslat a přijmout** ve skupině  **Stornování** vyberte **Storno potvrzení zásilky**.
1. Na kartě  **Řádky nákladu** vyberte řádek nákladu, který přesahuje navýšení dodávky.
1. Vyberte **Snížit vydané množství** a upravte vydané množství.
1. Na kartě  **Detaily řádku** vyberte možnost **Objednat**.
1. Nastavte pole **Množství** na vyskladněné množství (tj. na hodnotu pole **Množství vytvořené prací**), aby mohlo dojít k vygenerování dodacího listu.

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-unit-and-quantity-are-aligned-with-the-decimal-precision-of-the-unit"></a>Zkontrolujte řádky nákladu a proveďte úpravy, abyste se ujistili, že jednotka a množství jsou zarovnány s desetinnou přesností jednotky

Následujícím způsobem zkontrolujte řádky nákladu a proveďte úpravy, abyste se ujistili, že jednotka a množství jsou zarovnány s desetinnou přesností jednotky

1. Přejděte na **Řízení skladu \> Náklady \> Všechny náklady**.
1. Vyberte náklad, pro který nelze vygenerovat dodací list.
1. Na záložce s náhledem **Řádky nákladu** vyberte řádek nákladu položky, která způsobuje problém. Poznamenejte si hodnotu pole **Množství** a **Jednotka**.
1. Přejděte do nabídky **Správa organizace \> Jednotky \> Jednotky**.
1. Vyberte jednotku, pro kterou nelze vygenerovat dodací list.
1. Upravte hodnotu pole **Desetinná přesnost** podle potřeby.

### <a name="make-sure-that-the-inventory-unit-of-measure-is-smaller-than-the-sales-unit-of-measure"></a>Ujistěte se, že měrná jednotka zásob je menší než měrná jednotka prodeje

Ujistěte se, že měrná jednotka zásob je menší než měrná jednotka prodeje. Zvažte rekonfiguraci měrné jednotky pro položku podle potřeby.
