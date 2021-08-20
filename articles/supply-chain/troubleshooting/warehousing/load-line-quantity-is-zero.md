---
title: Dodávku nemůžete potvrdit, protože řádky nákladu mají nulové množství
description: Dodávku nemůžete potvrdit, protože řádky nákladu mají nulové množství.
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
ms.openlocfilehash: 5dc5f8962ba37d21d7ef505fea940dc8767a9d9295588cb0e12e9eebe379a35c
ms.sourcegitcommit: fa5ff2a0822aac16b518a2aea0d3389f79793390
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/07/2021
ms.locfileid: "7012147"
---
# <a name="you-cant-confirm-a-shipment-because-load-lines-have-zero-quantity"></a>Dodávku nemůžete potvrdit, protože řádky nákladu mají nulové množství

Kód chyby: WAX:LoadTableWarningAllLinesZero, WAX2543

## <a name="symptoms"></a>Příznaky

Když se pokusíte potvrdit dodávku, systém zobrazí následující chybovou zprávu:

> Všechny řádky v nákladu %1 mají množství nula.  
> Dodávku pro náklad %1 nebylo možné potvrdit.

Proto nemůžete potvrdit dodání pro zásilku.

## <a name="cause"></a>Příčina

Systém na základě vytvořených ID práce, množství řádku nákladu a procenta snížení dodávky vyhodnotí, zda lze řádek nákladu potvrdit. Pokud systém zjistí, že neexistují žádná ID práce, a pokud je procento snížené dodávky nastaveno na 100 procent, nemůžete dodávku potvrdit.

K tomuto problému může dojít třeba tehdy, když byla práce zrušena a procento snížené dodávky na řádku nákladu je 100 procent.

## <a name="resolution"></a>Řešení

Náklad nebo zásilka je aktuálně ve stavu, kdy se potvrzení zásilky nezdaří. Chcete-li problém opravit, proveďte jeden nebo více z následujících úkolů:

- Zkontrolujte řádky nákladu a ujistěte se, že všechny související práce byly dokončeny na konečném místě přepravy a že množství odpovídá.
- Zkontrolujte řádky nákladu a ujistěte se, že procento a množství podlimitního doručení je v souladu s vybranou prací.

### <a name="review-your-load-lines-to-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a>Zkontrolujte řádky nákladu a ujistěte se, že všechny související práce byly dokončeny na konečném místě přepravy a že množství odpovídá.

Pomocí následujících kroků zkontrolujte řádky nákladu a ujistěte se, že všechny související práce byly dokončeny na konečném místě přepravy a že množství odpovídá.

1. Přejděte na **Řízení skladu \> Náklady \> Všechny náklady**.
1. Otevřete náklad, pro který nelze potvrdit dodávku.
1. Na záložce s náhledem **Řádky nákladu** vyberte řádek nákladu.
1. Poznamenejte si hodnotu pole **Množství vytvořených prací**.
1. V podokně akcí na kartě **Náklady** ve skupině **Související informace** vyberte **Práce**.
1. Ověřte, že práce byla dokončena na konečném místě přepravy a že vybrané množství práce odpovídá vytvořenému množství práce na řádku zatížení.
1. Pokud zjistíte nesoulad, zrušte příslušnou práci, překonfigurujte směrnici o umístění a znovu uvolněte náklad. Pokyny najdete v části [Zásilku nemůžete potvrdit, protože položky nebyly vyzvednuty](picked-quantity-is-not-on-final.md).
1. Tento postup opakujte pro všechny řádky nákladů, abyste se ujistili, že jsou splněna všechna kritéria.

### <a name="review-your-load-lines-to-make-sure-that-the-underdelivery-percentage-and-quantities-are-aligned-with-the-picked-work"></a>Zkontrolujte řádky nákladu a ujistěte se, že procento a množství podlimitního doručení je v souladu s vybranou prací

Pomocí následujícího postupu zkontrolujte řádky nákladu a ujistěte se, že procento a množství podlimitního doručení je v souladu s vybranou prací.

1. Přejděte na **Řízení skladu \> Náklady \> Všechny náklady**.
1. Otevřete náklad, pro který nelze potvrdit dodávku.
1. Na záložce s náhledem **Řádky nákladu** vyberte řádek nákladu, který přesahuje procento pro snížení dodávky.
1. Upravte hodnotu pole **Nedostatečné doručení** nebo **Množství** podle potřeby.

> [!TIP]
> Pokud problém stále není vyřešen, možná budete muset dokončit další vychystávací práce pro související prodejní objednávky nebo objednávky přenosu, dokud nebude dostupné množství v souladu s nákladem nebo zásilkou.
