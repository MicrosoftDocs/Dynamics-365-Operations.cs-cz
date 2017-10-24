---
title: "Částka pro zaokrouhlení výpočtů odpisů"
description: "Tento článek popisuje pole Zaokrouhlit odpis, které se nachází na stránce Nastavení knihy."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetBookTable, AssetDepBookTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 13931
ms.assetid: faf7db87-046f-41d1-9baf-0df66e373e97
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: ae5c24633a9ce4ce43e213581eb64c8548eecf5d
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---

# <a name="round-off-amount-for-depreciation-calculations"></a>Částka pro zaokrouhlení výpočtů odpisů

[!include[banner](../includes/banner.md)]


Tento článek popisuje pole Zaokrouhlit odpis, které se nachází na stránce Nastavení knihy.

Celková částka odpisů je stanovena pro každou knihu. Současné odpisové částky se používají v profilu odpisování dlouhodobého majetku, který ukazuje budoucí odpisy a hodnotu dlouhodobého majetku, a také v návrzích na odpisy. Zadejte nejnižší částku odpisu povolenou pro tuto knihu. 

Bez ohledu na nastavené zaokrouhlování, není částka odpisu v posledním období odpisu zaokrouhlena. Na konci posledního období odpisu musí být hodnota dlouhodobého majetku 0 (nula) nebo hodnotu odpadu, pokud se používá konečná zůstatková hodnota.

### <a name="example"></a>Příklad

Odpis je bez zaokrouhlení vypočítán v částce 2 444,44. Stejně jako v následující tabulce se částky, které budou nabízeny, liší v závislosti na tom, jak je nastavené zaokrouhlování.

| Metoda zaokrouhlení | Odpisovaná částka |
|-----------------|---------------------|
| Zaokrouhlení 0,1    | 2 444,40            |
| Zaokrouhlení 1,00   | 2,444.00            |
| Zaokrouhlení 10,00  | 2,440.00            |
| Zaokrouhlení 100,00 | 2,400.00            |






