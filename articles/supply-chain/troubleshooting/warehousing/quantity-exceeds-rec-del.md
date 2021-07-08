---
title: Množství, které se pokoušíte aktualizovat, překračuje přijaté / doručené množství.
description: Když vygenerujete dodací list, odchozí náklad obsahuje vyskladněné množství, které překlačuje množství práce, které bylo vyskladněno a rezervováno pro prodejní objednávku.
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
ms.openlocfilehash: 66d9cd80cc61e00d1d88ab4f59d03054d746cdd9
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/14/2021
ms.locfileid: "6249073"
---
# <a name="quantity-that-youre-trying-to-update-exceeds-the-receiveddelivered-quantity"></a>Množství, které se pokoušíte aktualizovat, překračuje přijaté / doručené množství

Kód chyby: SYS7676

## <a name="symptoms"></a>Příznaky

Když vygenerujete dodací list, odchozí náklad obsahuje vyskladněné množství, které překlačuje množství práce, které bylo vyskladněno a rezervováno pro prodejní objednávku.

Když se pokusíte vygenerovat dodací list, systém zobrazí následující chybovou zprávu:

> Množství, které se pokoušíte aktualizovat, překračuje přijaté či dodané množství.

Proto nemůžete vygenerovat dodací list pro zásilku.

## <a name="cause"></a>Příčina

Vybrané množství práce neodpovídá vytvořenému množství práce na řádku dodávky. Například k tomuto problému může dojít, pokud počet řádků nákladu, počet vytvořených prací nebo vybrané množství není přesný.

## <a name="resolution"></a>Řešení

Náklad nebo zásilka je aktuálně ve stavu, kdy se generování dodacího listu nezdaří. Chcete-li problém opravit, proveďte jeden nebo více z následujících úkolů:

- Zkontrolujte řádky nákladu a ujistěte se, že všechny související práce byly dokončeny na konečném místě přepravy a že množství odpovídá.
- Upravte množství řádku nákladu.
- Stornujte všechny registrace vyskladnění a znovu proveďte vyskladnění.

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a>Zkontrolujte řádky nákladu a ujistěte se, že všechny související práce byly dokončeny na konečném místě přepravy a že množství odpovídá

Pomocí následujících kroků zkontrolujte řádky nákladu a ujistěte se, že všechny související práce byly dokončeny na konečném místě přepravy a že množství odpovídá

1. Přejděte na **Řízení skladu \> Náklady \> Všechny náklady**.
1. Vyberte dodávku, pro kterou nelze vygenerovat odeslání.
1. Na záložce s náhledem **Řádky nákladu** vyberte řádek nákladu.
1. Poznamenejte si hodnotu pole **Množství vytvořených prací**.
1. V podokně akcí na kartě **Náklady** ve skupině **Související informace** vyberte **Práce**.
1. Ověřte, že práce byla dokončena na konečném místě přepravy a že vybrané množství práce odpovídá vytvořenému množství práce na řádku zatížení.
1. Tento postup opakujte pro všechny řádky nákladů, abyste se ujistili, že jsou splněna všechna kritéria.

### <a name="adjust-the-load-line-quantity"></a>Upravte množství řádku nákladu

Následujícím postupem upravte množství řádku nákladu.

1. Přejděte na **Řízení skladu \> Náklady \> Všechny náklady**.
1. Vyberte náklad, pro který nelze vygenerovat dodací list.
1. V podokně akcí na kartě  **Odeslat a přijmout** ve skupině  **Stornování** vyberte **Storno potvrzení zásilky**.
1. Na kartě  **Řádky nákladu** vyberte řádek nákladu položky, která způsobuje problém.
1. Vyberte **Snížit vydané množství** a upravte vydané množství.
1. Nastavte pole **Snížit řádek nákladu** tak, aby odráželo úpravy na řádku nákladu.

### <a name="reverse-all-pick-registrations-and-redo-picking"></a>Stornujte všechny registrace vyskladnění a znovu proveďte vyskladnění

Pokud někdo použil registraci vyzvednutí k uzavření řádku nákladu bez práce, může dojít k rozporu mezi množstvím na řádku nákladu a vyskladněným množstvím. V takovém případě musí být ruční registrace vyskladnění obrácena a vyzvednutí musí být poté dokončeno pomocí mobilní aplikace Warehouse Management.

Chcete-li registraci vyskladnění zrušit, použijte následující postup.

1. Přejděte na **Pohledávky \> Objednávky \> Všechny objednávky**.
1. Vyberte prodejní objednávku, u které nemůžete zaúčtovat dodací list pro náklad.
1. Na kartě  **Řádky prodejní objednávky** vyberte řádek prodejní objednávky, pro kterou byla provedena registrace vyskladnění.
1. Vyberte **Aktualizovat řádek \> Vyskladnit** ke zrušení vyskladnění položek.
