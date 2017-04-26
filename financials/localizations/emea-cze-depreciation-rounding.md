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

Částky jsou zaokrouhleny nahoru nebo dolů, na základě hodnoty zadané v **zaokrouhlením odpisy** pole a metodu zaokrouhlení, která je určena v **Metoda zaokrouhlení** v **knih odpisů** stránky. Částky odpisů (x), který má **zaokrouhlením odpisy** (y hodnoty), částka odpisu (z) se počítá jako x ÷ y. Částka odpisu zaokrouhlena nahoru nebo dolů zaokrouhlí se počítá jako z x y. Například částka odpisu CZK 1,111.11 a **zaokrouhlením odpisy** hodnoty **1**, částka odpisu se vypočte jako CZK 1,111.11 ÷ 1 nebo CZK 1,111.11. Odpisů zaokrouhlené částky se počítá jako CZK 1,112 × 1 nebo CZK 1,112. Částka odpisu zaokrouhleno dolů se počítá jako CZK 1,111 × 1 nebo CZK 1,111. Následující tabulce jsou uvedeny částky odpisů zaokrouhlené a zaokrouhleno dolů různých částek odpisů a **zaokrouhlením odpisy** hodnoty.

|Odpisovaná částka (x)|Zaokrouhlení odpisu (y)|Částka odpisu (z = x ÷ y)|Normální způsob zaokrouhlení| Metoda zaokrouhlení směrem dolů|Způsob zaokrouhlování zaokrouhlení|
|-----------------------|-----------------------|-----------------------|-----------------------|-----------------------|-----------------------|
|1,111.11 CZK|1|CZK 1,111.11 ÷ 1 = CZK 1,111.11|1,111.1 CZK|CZK 1,111.11 je zaokrouhleno k CZK 1,112. Částka odpisu konečný: 1,112 × 1 CZK = CZK 1,112|CZK 1,111.11 je zaokrouhleno dolů na CZK 1,111. Částka odpisu konečný: 1,111 × 1 CZK = CZK 1,111|
|1,234.5 CZK|10|CZK 1,234.5 ÷ 10 = CZK 123.45|1,235 CZK|123,45 Kč je zaokrouhleno nahoru na 124 Kč. Částka odpisu konečný: CZK 124 × 10 = 1 240 CZK|123,45 Kč je zaokrouhleno dolů na 123 Kč. Částka odpisu konečný: CZK 123 × 10 = 1 230 CZK|




