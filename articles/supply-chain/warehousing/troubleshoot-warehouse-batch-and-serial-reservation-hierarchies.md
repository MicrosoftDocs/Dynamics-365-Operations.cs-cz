---
title: Odstraňování problémů s hierarchiemi dávkových a sériových rezervací ve skladu
description: Toto téma popisuje, jak řešit běžné problémy, s nimiž se můžete setkat při práci s hierarchiemi rezervací, které používají dávkové nebo sériové dimenze.
author: perlynne
ms.date: 3/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 3/12/2021
ms.openlocfilehash: a2b6f76aba22c24c07a2727b2eb8752f6ce763654403d47e34932a21a776dccb
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6748636"
---
# <a name="troubleshoot-warehouse-batch-and-serial-reservation-hierarchies"></a>Odstraňování problémů s hierarchiemi dávkových a sériových rezervací ve skladu

[!include [banner](../includes/banner.md)]

Toto téma popisuje, jak řešit běžné problémy, s nimiž se můžete setkat při práci s hierarchiemi rezervací, které používají dávkové nebo sériové dimenze.

Další informace viz [Flexibilní zásada rezervace dimenze na úrovni skladu](flexible-warehouse-level-dimension-reservation.md).

Hierarchie rezervací položky určuje požadavek na dimenze úložiště, které musí být splněny, aby bylo možné přiřadit skladové místo objednávce poptávky. Tyto dimenze lze popsat jako *dimenze nad skladovým místem* pro všechny dimenze, které musí být splněny před přiřazením skladového místa, a *dimenze pod skladovým umístěním* pro dimenze, které lze přidělit po přiřazení skladového místa objednávce poptávky. Tyto hierarchie rezervací jsou také známé jako hierarchie rezervací *batch-above* a *batch-below* nebo *serial-above* a *serial below*.

Zásoby lze úspěšně přidělit pouze v případě, že v dimenzích nad skladovým místem nejsou žádné mezery. Například v hierarchii rezervací *batch-above* očekáváte, že na objednávce poptávky budou zadány dimenze **Lokalita**, **Sklad,** a **Číslo dávky**. Pokud některá z těchto dimenzí chybí, proces přidělení selže. Naproti tomu v hierarchii rezervací *batch-below* nebo *serial-below* může být na objednávce poptávky uvedeno číslo dávky nebo sériové číslo, ale proces přidělování to nevyžaduje.

## <a name="i-receive-the-following-error-message-to-be-assigned-to-wave-load-lines-must-specify-the-dimensions-above-the-location-to-assign-these-dimensions-reserve-and-recreate-the-load-line"></a>Zobrazuje se následující chybová zpráva: „Aby bylo možné přiřadit vlně, musí řádky nákladu určit rozměry nad umístěním. Chcete-li přiřadit tyto rozměry, zarezervujte a znovu vytvořte řádek nákladu. “

### <a name="issue-description"></a>Popis problému

Pokud používáte položku, která má hierarchii rezervací *batch-above*, příkaz **Uvolnit do skladu** na stránce **Pracovní plocha plánování nákladu** nefunguje, pokus se pokusíte uvolnit náklad pro částečné množství. Zobrazí se tato chybová zpráva a pro částečné množství se nevytvoří žádná práce.

Pokud však použijete položku, která má hierarchii rezervací *batch-below*, můžete uvolnit náklad pro částečné množství ze stránky **Pracovní plocha plánování nákladu**.

### <a name="issue-cause"></a>Příčina problému

Když je některá dimenze nad dimenzí **Skladové místo** v hierarchii rezervací, musí být zadána před uvolněním do skladu. Částečná množství nelze uvolnit, pokud není zadána jedna či více dimenzí nad **skladovým místem**.

## <a name="the-auto-reservation-prompt-for-a-batch-number-is-triggered-even-though-there-is-available-inventory"></a>Aktivuje se výzva k automatické rezervaci čísla dávky, i když jsou k dispozici zásoby.

### <a name="issue-description"></a>Popis problému

Když používáte položku, která má hierarchii rezervací *batch-above* ve skladu, který nemá povolené procesy skladu a je povolena automatická rezervace, zobrazí se výzva k automatické rezervaci čísla dávky, i když je pro vyzvednutí k dispozici pouze jedna dávka.

Když však použijete stejnou položku ve skladu, kde jsou povoleny procesy skladu, výzva k automatické rezervaci se nezobrazí.

### <a name="issue-cause"></a>Příčina problému

Pokud je hierarchie rezervací definována jako *batch-above* nebo *serial-above*, odkazovaná dimenze (**Číslo dávky** nebo **Sériové číslo**) musí být vždy uvedeno na objednávkách poptávky. Procesy skladu mohou být schopny doplnit informace, pokud je k dispozici jedna dávka nebo sériové číslo. Protože však sklad nemá povoleny procesy skladu, musí uživatel vždy zadat všechny dimenze nad **skladovým místem**.

## <a name="slotting-templates-that-have-the-consider-on-hand-slot-criterion-dont-consider-current-on-hand-inventory-for-batch-enabled-items"></a>Šablony slottingu, které mají kritérium slotu Zohlednění stavu na skladě, nezohledňují aktuální zásoby na skladě pro položky s povolenou dávkou.

Další informace viz [Skladový slotting](warehouse-slotting.md).

### <a name="issue-description"></a>Popis problému

Šablony slottingu, které mají kritérium slotu *Zohlednění stavu na skladě*, nezohledňují aktuální zásoby na skladě pro položky *batch-above*. Zvažují to pouze v případě, že je na řádku prodejní objednávky uvedeno číslo dávky.

Když však použijete položky *batch-below*, aktuální zásoby na skladu jsou očekávány.

### <a name="issue-cause"></a>Příčina problému

Záhlaví šablony slottingu lze definovat pro strategii poptávky *Objednáno*, *Rezervováno* nebo *Uvolněno*. Pro strategii poptávky *Objednáno* platí stejné požadavky na hierarchii rezervací, jaké platí pro rezervaci nebo uvolnění do procesů skladu. Proto pro položky, které mají hierarchii reservací *batch-above* a *serial-below*, musí být na objednávce poptávky (prodej nebo převod) zadáno číslo dávky nebo sériové číslo. Případně strategie poptávky *Rezervováno* lze použít k výběru čísla dávky nebo sériového čísla před generováním poptávky skladového slottingu.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
