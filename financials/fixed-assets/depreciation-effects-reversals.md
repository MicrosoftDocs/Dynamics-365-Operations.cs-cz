---
title: "Efekty odpisů se storny"
description: "Tento článek popisuje potenciální důsledky stornování transakcí dlouhodobého majetku."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 2961
ms.assetid: 63a3ac92-c321-4379-a86a-b1b14915f340
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: d061ad8df477943259bff853d032c3df620e0b27
ms.contentlocale: cs-cz
ms.lasthandoff: 05/25/2017

---

# <a name="depreciation-effects-with-reversals"></a>Efekty odpisů se storny

[!include[banner](../includes/banner.md)]


Tento článek popisuje potenciální důsledky stornování transakcí dlouhodobého majetku. 

Transakce dlouhodobého majetku a transakce související s dlouhodobým majetkem můžete stornovat. Dále můžete stornovanou transakci odvolat. 

Můžete stornovat nebo odvolat transakci, která nebyla poslední transakcí zaúčtovanou do knihy pro majetek. Nejprve určete, zda byly po transakci, kterou stornujete, zaúčtovány nějaké transakce odpisů. Důvodem je skutečnost, že odpisy nejsou při stornování transakce přepočítány. Proto jsou odpisy často nadhodnoceny nebo podhodnoceny po stornování, jak je uvedeno v příkladech. 

Chcete-li zajistit správnost odpisů při stornování transakce, nepokračujte ve stornování v případě, že během stornování obdržíte zprávu s vysvětlením, že odpisy nebudou přepočítány. Namísto toho nejprve stornujte odpisovou transakci, která byla zaúčtována po transakci, kterou chcete stornovat, a poté pokračujte ve stornování. Nezobrazí se varování o přepočítání odpisů a můžete pokračovat ve stornování. 

Následující příklady zobrazují kalkulace, ke kterým dochází při pokračování i přes varovnou zprávu namísto prvního stornování odpisových transakcí.

## <a name="example-1-depreciation-is-overstated"></a> Příklad 1: Odpisy jsou nadhodnocené
Pro majetek je nastavena doba životnosti 5 let a lineární metoda odepisování (60 období odepisování). V tomto příkladu jsou odpisy nadhodnoceny.
#### <a name="asset-transaction-history"></a>Historie transakcí majetku

| Datum       | Typ transakce                                                          | Částka                                    |
|------------|---------------------------------------------------------------------------|-------------------------------------------|
| 1. leden  | Pořizovací cena                                                               | 59 000,00                                 |
| 1. leden  | Oprava pořizovací ceny                                                    | 1 000,00                                  |
| 31. leden | Odpisy (vytvořeno pomocí návrhu pro jedno odpisové období) | Kalkulace 1 000,00: Účetní hodnota (59 000 + 1 000) / Počet zbývajících odpisových období (60) |

#### <a name="reversal-action"></a>Akce Storno

| Datum      | Typ transakce                | Částka    |
|-----------|---------------------------------|-----------|
| 1. leden | Storno opravy pořizovací ceny | -1 000,00 |

#### <a name="depreciation-effect"></a>Efekt odpisů

| Datum        | Typ transakce        | Částka                                                                                |
|-------------|-------------------------|---------------------------------------------------------------------------------------|
| 28. únor | Odpis (návrh) | Kalkulace 983,05: Účetní hodnota (59 000 -1 000 odpisy) / Počet zbývajících odpisových období (59) |

Odpisy jsou nadhodnoceny o 16,95 (1 000 - 983,05).

## <a name="example-2-depreciation-is-understated"></a> Příklad 2: Odpisy jsou podhodnocené
Pro majetek je nastavena doba životnosti 5 let a lineární metoda odepisování (60 období odepisování). V tomto příkladu jsou odpisy podhodnoceny.
#### <a name="asset-transaction-history"></a>Historie transakcí majetku

| Datum       | Typ transakce                                                          | Částka                                      |
|------------|---------------------------------------------------------------------------|---------------------------------------------|
| 1. leden  | Pořizovací cena                                                               | 59 000,00                                   |
| 1. leden  | Snížení odpisu                                                     | 1 000,00                                    |
| 31. leden | Odpisy (vytvořeno pomocí návrhu pro jedno odpisové období) | Kalkulace 966,67: Účetní hodnota (59 000 - 1 000) / Počet zbývajících odpisových období (60) |

#### <a name="reversal-action"></a>Akce Storno

| Datum      | Typ transakce               | Částka    |
|-----------|--------------------------------|-----------|
| 1. leden | Storno snížení odpisu | -1 000,00 |

#### <a name="depreciation-effect"></a>Efekt odpisů

| Datum        | Typ transakce        | Částka                                                                                       |
|-------------|-------------------------|----------------------------------------------------------------------------------------------|
| 28. únor | Odpis (návrh) | Kalkulace 983,62: Účetní hodnota (59 000 - 966,67 odpisy) / Počet zbývajících odpisových období (59) |

Odpisy jsou podhodnoceny o 16,95 (983,62 - 966,67).



<a name="see-also"></a>Viz také
--------

[Odpisy dlouhodobého majetku](fixed-asset-depreciation.md)




