---
title: " Zaokrouhlení odpisu"
description: Tento článek vysvětluje, jak můžete zaokrouhlit částky odpisu dlouhodobého majetku nahoru nebo dolů na nejbližší celé číslo.
author: EvgenyPopovMBS
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: kfend
ms.custom: 265204
ms.search.region: Czech Republic
ms.author: epopov
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 0da441e923458e1401fc5dd89dd867fa7c61cd3f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8889811"
---
# <a name="depreciation-rounding"></a> Zaokrouhlení odpisu

[!include [banner](../includes/banner.md)]

Tento článek vysvětluje, jak můžete zaokrouhlit částky odpisu dlouhodobého majetku nahoru nebo dolů na nejbližší celé číslo. 

Částky odpisu jsou zaokrouhleny nahoru nebo dolů, na základě hodnoty zadané v poli **Zaokrouhlit odpis** a metody zaokrouhlení, která je určena v poli **Metoda zaokrouhlení** na stránce **Knihy odpisů**. Částka odpisu (x) s hodnotou **Zaokrouhlování odpisu** (y), se částka odpisu (z) vypočítá jako x ÷ y. Částka odpisu zaokrouhlená nahoru nebo dolů se počítá jako z × y. Například pro částku odpisu CZK 1 111.11 a hodnotu **Zaokrouhlování odpisu** **1** se částka odpisu vypočte jako CZK 1 111.11 ÷ 1 nebo CZK 1 111.11. Částka odpisu zaokrouhlená nahoru se počítá jako CZK 1 112 × 1 nebo CZK 1 112. Částka odpisu zaokrouhlená dolů se počítá jako CZK 1 111 × 1 nebo CZK 1 111. Následující tabulka uvádí částky odpisů zaokrouhlené nahoru a dolů pro různé částky odpisu a hodnoty **Zaokrouhlení odpisu**.

|Odpisovaná částka (x)|Zaokrouhlení odpisu (y)|Částka odpisu (z = x ÷ y)|Normální metoda zaokrouhlování| Metoda zaokrouhlování dolů|Metoda zaokrouhlování nahoru|
|-----------------------|-----------------------|-----------------------|-----------------------|-----------------------|-----------------------|
|1 111,11 Kč|1|CZK 1 111.11 ÷ 1 = CZK 1 111.11|1 111,1 Kč|1 111,11 Kč je zaokrouhleno nahoru na 1 112 Kč. Výsledná částka odpisu: CZK 1 112 × 1 = CZK 1 112|1 111,11 Kč je zaokrouhleno dolů na 1 111 Kč. Výsledná částka odpisu: CZK 1 111 × 1 = CZK 1 111|
|1 234,5 Kč|10|CZK 1 234.5 ÷ 10 = CZK 123,45|1 235 Kč|123,45 Kč je zaokrouhleno nahoru na 124 Kč. Výsledná částka odpisu: CZK 124 × 10 = CZK 1 240|123,45 Kč je zaokrouhleno dolů na 123 Kč. Výsledná částka odpisu: CZK 123 × 10 = CZK 1 230|





[!INCLUDE[footer-include](../../includes/footer-banner.md)]