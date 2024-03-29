---
title: Možnost Celková částka a Interval výpočtu pro kódy DPH
description: Tento článek vysvětluje možnosti pro pole Metoda výpočtu pro kódy DPH, a postup výpočtu DPH v rámci intervalů a celých částek.
author: kailiang
ms.date: 10/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxData, TaxTable
audience: Application User
ms.reviewer: kfend
ms.custom: 5624
ms.assetid: 96166db4-b7ca-470b-aeb7-0a66fe0554c4
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0b81780e60825021ad7a700d85257ba0f5a2447a
ms.sourcegitcommit: 0d5c07ba91a9ceb2eeb11db032fd28037216789d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/25/2022
ms.locfileid: "9715234"
---
# <a name="whole-amount-and-interval-calculation-options-for-sales-tax-codes"></a>Možnost Celková částka a Interval výpočtu pro kódy DPH

[!include [banner](../includes/banner.md)]

Tento článek vysvětluje možnosti pro pole **Metoda výpočtu** pro kódy DPH, a postup výpočtu DPH v rámci intervalů a celých částek.

Můžete nastavit kód DPH, aby byl vypočten na základě celé částky nebo částky intervalu. Na stránce **Kódy DPH** pomocí pole **Metoda výpočtu** na pevné záložce **Výpočet** vyberte způsob výpočtu kódu DPH.
- Celá částka – Sazba daně se použije na celou zdanitelnou částku.
- Interval – základ daně je rozdělen do částí, kde každá část spadá do rozsahu, který má konkrétní kurz DPH. Část částky, která spadá do příslušného intervalu, je zdaněna podle sazby daně pro tento interval. Prodejní daň je součtem částek daně, které byly vypočteny pro každou částku intervalu.
  > [!NOTE]                                                                                                                              
  > Možnost Interval je k dispozici pouze při výběru řádku v poli Metoda výpočtu v oblasti DPH na stránce Parametry hlavní knihy. 

Intervaly jsou nastaveny na stránce Hodnoty kódu DPH zadáním minimálního a maximálního limitu částky pro jednotlivé daňové sazby. U daní, které se počítají z jakéhokoli základu, musejí být u intervalů dodržena následující pravidla (bez ohledu na vybranou metodu výpočtu):
-   První interval má dolní mez rovnou 0.
-   Poslední interval má maximální limit 0, což znamená nekonečno.
-   Maximální limit u intervalu musí být minimálním limitem následujícího intervalu.

Pokud částka odpovídá horní mezi předchozím intervalem a zároveň dolní mezi dalšího intervalu, použije se pro částku sazby DPH prvního intervalu. Jestliže částka nenáleží do žádného intervalu, které jsou definované dolní a horní mezí, použije se nulová sazba DPH.

## <a name="example-whole-amount-method-of-calculation"></a>Příklad: výpočet metodou celkové částky
Na stránce Hodnoty kódu DPH jsou sazby DPH nastaveny v následujících intervalech:

| Minimální limit     | Maximální limit     | Sazba daně     |
|-------------------|-------------------|--------------|
| 0,00              | 50,00             | 30 %          |
| 50,00             | 100,00            | 20 %          |
| 100,00            | 0,00              | 10 %          |

Prodejní daň bude vypočtena ve výši celé zdanitelné částky.

| Zdanitelná částka (cena) | Výpočet    | DPH |
|------------------------|----------------|-----------|
| 35,00                  | 35,00 \* 0,30  | 10,50 USD     |
| 50,00                  | 50,00 \* 0,30  | 15:00     |
| 85,00                  | 85,00 \* 0,20  | 17,00     |
| 305,00                 | 305,00 \* 0,10 | 30,50     |

## <a name="example-interval-method-of-calculation"></a> Příklad: výpočet metodou intervalu
Na stránce Hodnoty jsou sazby DPH nastaveny v následujících intervalech:

| Minimální limit     | Maximální limit     | Sazba daně     |
|-------------------|-------------------|--------------|
| 0,00              | 50,00             | 30 %          |
| 50,00             | 100,00            | 20 %          |
| 100,00            | 0,00              | 10 %          |

Prodejní daň je součtem částek daně, které byly vypočteny pro každou částku intervalu.

| Zdanitelná částka (cena) | Výpočet                                                               | DPH |
|------------------------|---------------------------------------------------------------------------|-----------|
| 35,00                  | 35,00 \* 0,30                                                             | 10,50 USD     |
| 50,00                  | 50,00 \* 0,30                                                             | 15:00     |
| 85,00                  | (50,00 \* 0,30 = 15,00) + (35,00 \* 0,20 = 7,00)                          | 22,00     |
| 305,00                 | (50,00 \* 0,30 = 15,00) + (50,00 \* 0,20 = 10,00) + (205 \* 0,10 = 20,50) | 45.50     |



Více informací najdete v části [Sazby DPH na základě polí Základ marže a Metody výpočtu](marginal-base-field.md).







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
