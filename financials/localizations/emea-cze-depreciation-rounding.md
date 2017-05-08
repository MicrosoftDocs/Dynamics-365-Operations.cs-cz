---
title: " Zaokrouhlení odpisu"
description: "Toto téma vysvětluje, jak můžete zaokrouhlit částky odpisu dlouhodobého majetku nahoru nebo dolů na nejbližší celé číslo."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 265204
ms.assetid: 3e535ac3-f5de-47cc-ba7b-40c9857a9460
ms.search.region: Czech Republic
ms.author: epopov
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 6bb98cc72c2ec0c1551412dd39d5bea3ce10e2cd
ms.openlocfilehash: 26840ba4856b6e137acdf0d1e90d7a76374a3439
ms.lasthandoff: 03/31/2017


---

# <a name="depreciation-rounding"></a> Zaokrouhlení odpisu

[!include[banner](../includes/banner.md)]


Toto téma vysvětluje, jak můžete zaokrouhlit částky odpisu dlouhodobého majetku nahoru nebo dolů na nejbližší celé číslo. 

Částky odpisu jsou zaokrouhleny nahoru nebo dolů, na základě hodnoty zadané v poli **Zaokrouhlit odpis** a metody zaokrouhlení, která je určena v poli **Metoda zaokrouhlení** na stránce **Knihy odpisů**. Částka odpisu (x) s hodnotou **Zaokrouhlování odpisu** (y), se částka odpisu (z) vypočítá jako x ÷ y. Částka odpisu zaokrouhlená nahoru nebo dolů se počítá jako z × y. Například pro částku odpisu CZK 1 111.11 a hodnotu **Zaokrouhlování odpisu** **1** se částka odpisu vypočte jako CZK 1 111.11 ÷ 1 nebo CZK 1 111.11. Částka odpisu zaokrouhlená nahoru se počítá jako CZK 1 112 × 1 nebo CZK 1 112. Částka odpisu zaokrouhlená dolů se počítá jako CZK 1 111 × 1 nebo CZK 1 111. Následující tabulka uvádí částky odpisů zaokrouhlené nahoru a dolů pro různé částky odpisu a hodnoty **Zaokrouhlení odpisu**.

|Odpisovaná částka (x)|Zaokrouhlení odpisu (y)|Částka odpisu (z = x ÷ y)|Normální metoda zaokrouhlování| Metoda zaokrouhlování dolů|Metoda zaokrouhlování nahoru|
|-----------------------|-----------------------|-----------------------|-----------------------|-----------------------|-----------------------|
|1 111,11 Kč|1|CZK 1 111.11 ÷ 1 = CZK 1 111.11|1 111,1 Kč|1 111,11 Kč je zaokrouhleno nahoru na 1 112 Kč. Výsledná částka odpisu: CZK 1 112 × 1 = CZK 1 112|1 111,11 Kč je zaokrouhleno dolů na 1 111 Kč. Výsledná částka odpisu: CZK 1 111 × 1 = CZK 1 111|
|1 234,5 Kč|10|CZK 1 234.5 ÷ 10 = CZK 123,45|1 235 Kč|123,45 Kč je zaokrouhleno nahoru na 124 Kč. Výsledná částka odpisu: CZK 124 × 10 = CZK 1 240|123,45 Kč je zaokrouhleno dolů na 123 Kč. Výsledná částka odpisu: CZK 123 × 10 = CZK 1 230|



