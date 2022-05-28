---
title: Sledování průběžných průměrných nákladů pro dimenzi zboží
description: Každá skladová položka má přiřazenou skupinu dimenzí zásob. Průběžná průměrná nákladová cena položky je tedy vypočtena na základě výběru dimenzí zásob, které jsou finančně sledovány.
author: JennySong-SH
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventOnhandItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: 75053
ms.assetid: 68cc00f4-0f7a-4a7d-be90-8f2e0d0563d3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 186109774dbb2795911305ec0bb5b29c7a7a72d9
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/03/2022
ms.locfileid: "8669705"
---
# <a name="track-running-average-cost-per-inventory-dimension"></a>Sledování průběžných průměrných nákladů pro dimenzi zboží

[!include [banner](../includes/banner.md)]

Každá skladová položka má přiřazenou skupinu dimenzí zásob. Průběžná průměrná nákladová cena položky je tedy vypočtena na základě výběru dimenzí zásob, které jsou finančně sledovány.

Existují tři typy dimenzí zásob: produkty, skladiště a sledování. Dimenze produktu zahrnují konfiguraci, velikost a barvu. Dimenze produktu jsou vždy finančně sledovány. Naproti tomu dimenze uskladnění a sledování zahrnují pracoviště, sklad, umístění, stav zásob, registrační značku, číslo dávky a sériové číslo. Můžete vybrat, které dimenze uskladnění a sledování budou finančně sledovány. 

**Příklad 1** 

Pokud je u skupiny dimenzí úložiště, která je připojena k položce, finančně sledován sklad, bude průběžná průměrná nákladová cena vypočtena pro každý sklad. Byly fakturovány následující nákupní objednávky:

-   Nákupní objednávka na 2 kusy v ceně 10,00 USD byla fakturována pro sklad GW.
-   Nákupní objednávka na 3 kusy v ceně 12,00 USD byla fakturována pro sklad GW.
-   Nákupní objednávka na 5 kusy v ceně 15,00 USD byla fakturována pro sklad MW.

Průběžná průměrná nákladová cena ve skladu GW činí 11,20 USD a průběžná průměrná nákladová cena ve skladu MW činí 15,00 USD. K zaúčtování faktury prodejní objednávky dojde pro sklad GW. Hodnota zásob a náklady prodaného zboží (před provedením uzávěrky skladu a bez označení) činí 11,20 USD. Dojde k zaúčtování faktury další prodejní objednávky pro sklad MW. Hodnota zásob a náklady prodaného zboží (před provedením uzávěrky skladu a bez označení) činí 15,00 USD. 

**Příklad 2** Jestliže skupina dimenzí úložiště, která je připojena k položce, je finančně sledována podle skladu, a skupina sledovacích dimenzí je finančně sledována podle čísla dávky, bude průběžná průměrná nákladová cena vypočtena pro každou dávku. 

**Poznámka:** Doporučujeme vždy zobrazit nákladovou cenu se všemi finančními dimenzemi, které se u položky sledují. Byly fakturovány následující nákupní objednávky:

-   Nákupní objednávka na 2 kusy v ceně 10,00 USD byla fakturována pro sklad GW a dávku AAA.
-   Nákupní objednávka na 3 kusy v ceně 12,00 USD byla fakturována pro sklad GW a dávku AAA.
-   Nákupní objednávka na 2 kusy v ceně 15,00 USD byla fakturována pro sklad GW a dávku BBB.

Průběžná průměrná nákladová cena ve skladu GW a dávce AAA činí 11,20 USD a průběžná průměrná nákladová cena ve skladu GW a dávce BBB činí 15,00 USD.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]