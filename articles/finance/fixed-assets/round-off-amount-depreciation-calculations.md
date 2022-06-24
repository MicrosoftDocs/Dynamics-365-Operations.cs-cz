---
title: Částka pro zaokrouhlení výpočtů odpisů
description: Tento článek popisuje pole Zaokrouhlit odpis, které se nachází na stránce Nastavení knihy.
author: moaamer
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetBookTable, AssetDepBookTable
audience: Application User
ms.reviewer: kfend
ms.custom: 13931
ms.assetid: faf7db87-046f-41d1-9baf-0df66e373e97
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a93842f7cca483df89188695c945edf77e118cef
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8870097"
---
# <a name="round-off-amount-for-depreciation-calculations"></a>Částka pro zaokrouhlení výpočtů odpisů

[!include [banner](../includes/banner.md)]

Tento článek popisuje pole **Zaokrouhlit odpis**, které se nachází na stránce **Nastavení knihy**.

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







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
