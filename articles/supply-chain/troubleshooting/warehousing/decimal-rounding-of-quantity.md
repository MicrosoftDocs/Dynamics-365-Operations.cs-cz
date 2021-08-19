---
title: Desetinné zaokrouhlování množství fyzické aktualizace je nesprávné
description: Když vygenerujete dodací list, odchozí náklad obsahuje množství, které neodpovídá přesnosti na počet desetinných míst, který je definován v jednotce.
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
ms.openlocfilehash: ddfac7106eb0e8b934516ca10e3950891d10910a2ccdef1868faf25812243159
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6726554"
---
# <a name="decimal-rounding-of-the-physical-updating-quantity-is-incorrect"></a>Desetinné zaokrouhlování množství fyzické aktualizace je nesprávné

Kód chyby: SYS19589

## <a name="symptoms"></a>Příznaky

Když vygenerujete dodací list, odchozí náklad obsahuje množství, které neodpovídá přesnosti na počet desetinných míst, který je definován v jednotce.

Když se pokusíte vygenerovat dodací list, systém zobrazí následující chybovou zprávu:

> Desetinné zaokrouhlení fyzicky aktualizovaného množství v jednotce %1 je nesprávné.

Proto nemůžete vygenerovat dodací list pro zásilku.

## <a name="cause"></a>Příčina

Systém vyhodnotí, zda desetinné zaokrouhlení přepravního množství odpovídá přesnosti na desetinná místa, která je definována pro přepravní jednotku. Když systém zaokrouhlí množství zásilky na zadaný počet desetinných míst, pokud zjistí, že zaokrouhlené množství zásilky neodpovídá skutečnému množství zásilky, nelze vygenerovat dodací list. Například k tomuto problému může dojít, pokud je prodejní množství 1,75 kilogramu (kg), ale desetinná přesnost je nastavena na *1*.

## <a name="resolution"></a>Řešení

Náklad nebo zásilka je aktuálně ve stavu, kdy se generování dodacího listu nezdaří. Chcete-li problém opravit, proveďte jeden nebo více z následujících úkolů:

- Zkontrolujte řádky nákladu a proveďte úpravy, abyste zajistili, že množství lze čistě převést bez desetinných čísel a jakýchkoli dalších problémů se zaokrouhlováním.
- Zkontrolujte řádky nákladu a proveďte úpravy, abyste se ujistili, že jednotka a množství jsou zarovnány s desetinnou přesností jednotky.

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-quantity-can-be-cleanly-converted-without-decimal-numbers-and-any-other-rounding-issues"></a>Zkontrolujte řádky nákladu a proveďte úpravy, abyste zajistili, že množství lze čistě převést bez desetinných čísel a jakýchkoli dalších problémů se zaokrouhlováním

Pomocí následujícího postupu zkontrolujte řádky nákladu a proveďte úpravy, abyste zajistili, že množství lze čistě převést bez desetinných čísel a jakýchkoli dalších problémů se zaokrouhlováním.

1. Přejděte na **Řízení skladu \> Náklady \> Všechny náklady**.
1. Vyberte náklad, pro který nelze vygenerovat dodací list.
1. V podokně akcí na kartě  **Odeslat a přijmout** ve skupině  **Stornování** vyberte **Storno potvrzení zásilky**.
1. Na kartě  **Řádky nákladu** vyberte řádek nákladu položky, která způsobuje problém.
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
