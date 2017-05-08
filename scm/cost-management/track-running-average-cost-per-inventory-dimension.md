---
title: "Sledování průběžných průměrných nákladů pro dimenzi zboží"
description: "Každá skladová položka má přiřazenou skupinu dimenzí zásob. Průběžná průměrná nákladová cena položky je tedy vypočtena na základě výběru dimenzí zásob, které jsou finančně sledovány."
author: YuyuScheller
manager: AnnBe
ms.date: 2016-03-31 12 - 51 - 05
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventOnhandItem
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 75053
ms.assetid: 68cc00f4-0f7a-4a7d-be90-8f2e0d0563d3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: f464f94632f7114da5a9cbf34036e4fcb87bcd02
ms.lasthandoff: 03/29/2017


---

# <a name="tracking-running-average-cost-per-inventory-dimension"></a>Sledování průběžných průměrných nákladů pro dimenzi zboží

Každá skladová položka má přiřazenou skupinu dimenzí zásob. Průběžná průměrná nákladová cena položky je tedy vypočtena na základě výběru dimenzí zásob, které jsou finančně sledovány.

Existují tři typy dimenzí zásob: produkty, skladiště a sledování. Dimenze produktu zahrnují konfiguraci, velikost a barvu. Dimenze produktu jsou vždy finančně sledovány. Naproti tomu dimenze uskladnění a sledování zahrnují pracoviště, sklad, umístění, stav zásob, registrační značku, číslo dávky a sériové číslo. Můžete vybrat, které dimenze uskladnění a sledování budou finančně sledovány. **Příklad 1** Pokud je u skupiny dimenzí úložiště, která je připojena k položce, finančně sledován sklad, bude průběžná průměrná nákladová cena vypočtena pro každý sklad. Byly fakturovány následující nákupní objednávky:

-   Nákupní objednávka na 2 kusy v ceně 10,00 USD byla fakturována pro sklad GW.
-   Nákupní objednávka na 3 kusy v ceně 12,00 USD byla fakturována pro sklad GW.
-   Nákupní objednávka na 5 kusy v ceně 15,00 USD byla fakturována pro sklad MW.

Průběžná průměrná nákladová cena ve skladu GW činí 11,20 USD a průběžná průměrná nákladová cena ve skladu MW činí 15,00 USD. K zaúčtování faktury prodejní objednávky dojde pro sklad GW. Hodnota zásob a náklady prodaného zboží (před provedením uzávěrky skladu a bez označení) činí 11,20 USD. Dojde k zaúčtování faktury další prodejní objednávky pro sklad MW. Hodnota zásob a náklady prodaného zboží (před provedením uzávěrky skladu a bez označení) činí 15,00 USD. **Příklad 2** Jestliže skupina dimenzí úložiště, která je připojena k položce, je finančně sledována podle skladu, a skupina sledovacích dimenzí je finančně sledována podle čísla dávky, bude průběžná průměrná nákladová cena vypočtena pro každou dávku. **Poznámka:** Doporučujeme vždy zobrazit nákladovou cenu se všemi finančními dimenzemi, které se u položky sledují. Byly fakturovány následující nákupní objednávky:

-   Nákupní objednávka na 2 kusy v ceně 10,00 USD byla fakturována pro sklad GW a dávku AAA.
-   Nákupní objednávka na 3 kusy v ceně 12,00 USD byla fakturována pro sklad GW a dávku AAA.
-   Nákupní objednávka na 2 kusy v ceně 15,00 USD byla fakturována pro sklad GW a dávku BBB.

Průběžná průměrná nákladová cena ve skladu GW a dávce AAA činí 11,20 USD a průběžná průměrná nákladová cena ve skladu GW a dávce BBB činí 15,00 USD.

