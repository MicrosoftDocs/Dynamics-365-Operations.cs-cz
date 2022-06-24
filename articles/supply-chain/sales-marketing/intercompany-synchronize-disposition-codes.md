---
title: Synchronizace dispozičních kódů
description: Tento článek vysvětluje synchronizaci dispozičních kódů u mezipodnikových obchodů
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: d347181dd6ba12de0e114d74d43cd46230ba4fb7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8905653"
---
# <a name="synchronize-intercompany-disposition-codes"></a>Synchronizace mezipodnikových dispozičních kódů

[!include [banner](../../includes/banner.md)]

Za účelem podpory mezipodnikových vratek aplikace Microsoft Dynamics 365 Supply Chain Management umožňuje mapovat externě definované dispoziční kódy na odpovídající interní dispoziční kódy. Při vytváření mezipodnikového řetězce musí být dispoziční akce ve dvou společnostech, které jsou navzájem mapovány, stejné. Pokud se liší, proces synchronizace bude neúspěšný.

## <a name="about-disposition-codes-for-three-legged-direct-returns"></a>Dispoziční kódy pro přímé vratky se třemi větvemi

Dispoziční kódy se synchronizují z řádku mezipodnikové prodejní objednávky do řádku původní prodejní objednávky. Synchronizace má však pouze jeden okamžitý účinek na řádek původní prodejní objednávky. Tento účinek znamená, že různé náklady řádku jsou odstraněny na základě dispozičního kódu a různých nákladů, které jsou nastaveny ve společnosti A. Společnost A je společnost, která vytváří vratku.

V případě řetězce přímé dodávky se třemi větvemi jsou na řádku mezipodnikové prodejní objednávky podporovány všechny dispoziční akce. Pokud však je výrobek vracen odběrateli, je důležité potvrdit, že dodací adresa uvedená ve vratce odpovídá dodací adrese odběratele, která je uvedená na původní objednávce.

> [!NOTE]
> U nákupních objednávek dispoziční kódy neexistují. Z toho důvodu musí být synchronizace dispozičních kódů mezipodnikové prodejní objednávky s původní vratkou provedena mezi prodejními objednávkami.

## <a name="replacing-returned-items"></a>Výměna vrácených položek

Když bude vrácená položka vyměněna a ve společnosti B byla již vytvořena objednávka náhrady, nelze vybrat dispoziční kód a ve společnosti A nebude vytvořena další objednávka náhrady.

## <a name="rules-for-intercompany-direct-deliveries"></a>Pravidla pro mezipodnikové přímé dodávky

Následující obecná pravidla platí pro původní vratky ve scénářích zahrnujících mezipodnikové přímé dodávky:

- Pokud se u dispoziční akce obsažené na řádku původní prodejní objednávky jedná o vrácení peněz a likvidaci, vrácení peněz nebo o vrácení odběrateli, použije se dispoziční akce Kredit. Avšak kód akce vrácení odběrateli nastaví čistou částku u stávajícího řádku i u nově synchronizovaného řádku z mezipodnikové prodejní objednávky na 0 (nulu). Dále platí, že likvidované řádky se nikdy nesynchronizují. Když je přidán řádek do mezipodnikové prodejní objednávky, synchronizace neproběhne u prodejní objednávky s kladným množstvím a dispoziční akcí likvidace (například vrácení peněz a likvidace nebo výměna a likvidace).
- Podkladová dispoziční akce vrácení peněz a výměna nebo likvidace a výměna není zrušena. Je zpracována jako dispoziční akce vrácení peněz a výměna nebo likvidace a výměna. Toto pravidlo platí, i když ve společnosti A není vytvořen žádný řádek likvidace a ve společnosti B (která obdržela vrácenou položku), není vytvořena žádná objednávka náhrady. Objednávka náhrady je ve společnosti A vytvořena, jen když se provede aktualizace dodacího listu.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
