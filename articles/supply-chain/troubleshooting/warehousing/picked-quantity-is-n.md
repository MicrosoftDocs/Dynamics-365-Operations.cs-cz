---
title: Vydané množství není během generování dodacího listu dostatečné
description: Když vygenerujete dodací list, odchozí náklad obsahuje vyskladněné množství, které neodpovídá vytvořenému množství práce na řádku nákladu.
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
ms.openlocfilehash: 361b61690e9e16a690234ed9319478d864c743e7559746654e4868272de13524
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6716461"
---
# <a name="picked-quantity-isnt-sufficient-during-packing-slip-generation"></a>Vydané množství není během generování dodacího listu dostatečné

Kód chyby: SYS54073

## <a name="symptoms"></a>Příznaky

Když vygenerujete dodací list, odchozí náklad obsahuje vyskladněné množství, které neodpovídá vytvořenému množství práce na řádku nákladu.

Když se pokusíte vygenerovat dodací list, systém zobrazí následující chybovou zprávu:

> Hodnota %1 byla vyskladněna, proto nestačí aktualizovat %2, když potom zbývající zůstatek musí být %3.

Proto nemůžete vygenerovat dodací list pro zásilku.

## <a name="cause"></a>Příčina

Dodací list nelze v aktuálním stavu vygenerovat, protože může existovat jedna z následujících podmínek:

- Související práce ještě nebyly vybrány a přesunuty na konečné místo dodání.
- Vybrané množství práce neodpovídá vytvořenému množství práce na řádku dodávky.
- Množství na řádku dodávky, množství vytvořené práce a vyskladněné množství se neshodují.

## <a name="resolution"></a>Řešení

Náklad nebo zásilka je aktuálně ve stavu, kdy se generování dodacího listu nezdaří. Chcete-li problém opravit, proveďte jeden nebo více z následujících úkolů:

- Zkontrolujte řádky nákladu a ujistěte se, že všechny související práce byly dokončeny na konečném místě přepravy a že množství odpovídá.
- Upravte množství řádku nákladu.
- Stornujte všechny registrace vyskladnění a znovu proveďte vyskladnění.

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a>Zkontrolujte řádky nákladu a ujistěte se, že všechny související práce byly dokončeny na konečném místě přepravy a že množství odpovídá

Pomocí následujících kroků zkontrolujte řádky nákladu a ujistěte se, že všechny související práce byly dokončeny na konečném místě přepravy a že množství odpovídá

1. Přejděte na **Řízení skladu \> Náklady \> Všechny náklady**.
1. Vyberte náklad, pro který nelze vygenerovat dodací list.
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

K problému může dojít, protože někdo použil registraci vyskladnění k uzavření řádku nákladu bez práce. V takovém případě musí být ruční registrace vyskladnění obrácena a vyzvednutí musí být poté dokončeno pomocí mobilní aplikace Warehouse Management.

Chcete-li registraci vyskladnění zrušit, použijte následující postup.

1. Přejděte na **Pohledávky \> Objednávky \> Všechny objednávky**.
1. Vyberte prodejní objednávku, u které nemůžete zaúčtovat dodací list pro náklad.
1. Na kartě  **Řádky prodejní objednávky** vyberte řádek prodejní objednávky, pro kterou byla provedena registrace vyskladnění.
1. Vyberte **Aktualizovat řádek \> Vyskladnit** ke zrušení vyskladnění položek.
