---
title: Odpis koeficientem
description: Tento článek poskytuje přehled o metodě odpisu koeficientem.
author: moaamer
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: roschlom
ms.custom: 13831
ms.assetid: 2b6c4fe4-02ff-4191-bcad-32f1f34c15f2
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: aab5ab518f2806e1b27f352e354dc9280fd27def
ms.sourcegitcommit: 1707cf45217db6801df260ff60f4648bd9a4bb68
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/23/2021
ms.locfileid: "7674448"
---
# <a name="factor-depreciation"></a>Odpis koeficientem

[!include [banner](../includes/banner.md)]

Tento článek poskytuje přehled o metodě odpisu koeficientem.

Koeficienty jsou procenta, která se používají při odpisování majetku. Když nastavíte odpisový plán dlouhodobého majetku a v poli **Metoda** na stránce **Odpisové profily** vyberete hodnotu **Koeficient**, můžete nastavit progresivní, degresivní nebo lineární metodu odepisování:

-   Jestliže vyberete progresivní metodu odepisování, částka odpisu se v každém období odpisu zvýší.
-   Jestliže vyberete degresivní metodu odepisování, částka odpisu za dané období se bude v průběhu let snižovat.
-   Jestliže vyberete lineární metodu odepisování, odpis bude v každém období stejný.

Níže uvedená pravidla a příklady ukazují, jak lze nastavit koeficienty pro jednotlivé typy odpisů. 

> [!NOTE] 
> Když vyberete možnost **Faktor** v poli **Metoda**, zobrazí se pole **Faktor** a pole **Interval**.

## <a name="progressive-depreciation"></a>Progresivní metoda odepisování
Hodnota v poli **Koeficient** je větší než **50**.

### <a name="example"></a>Příklad

Pořizovací cena je 100 000, koeficient je 70, doba životnosti je 10 let a odepisování začíná 1. ledna. Částky odpisů a zůstatkové účetní hodnoty jsou zobrazeny pouze pro prvních šest let životnosti.

| Rok | Období      | Odpisovaná částka | Zůstatková účetní hodnota |
|------|-------------|---------------------|-----------------------|
| 1    | 31. prosince | 307,69              | 99 692,31             |
| 2    | 31. prosince | 1 447,21            | 98 245,10             |
| 3    | 31. prosince | 3 104,50            | 95 140,60             |
| 4    | 31. prosince | 5 150,21            | 89 990,39             |
| 5    | 31. prosince | 7 522,95            | 82 467,44             |
| 6    | 31. prosince | 10 184,06           | 72 283,38             |

## <a name="digressive-depreciation"></a>Degresivní metoda odepisování
Hodnota v poli **Koeficient** je menší než **50**.

### <a name="example"></a>Příklad

Pořizovací cena je 100 000, koeficient je 20, doba životnosti je 10 let a odepisování začíná 1. ledna. Částky odpisů a zůstatkové účetní hodnoty jsou zobrazeny pouze pro prvních šest let životnosti.

| Rok | Období      | Odpisovaná částka | Zůstatková účetní hodnota |
|------|-------------|---------------------|-----------------------|
| 1    | 31. prosince | 56 080,43           | 43 919,57             |
| 2    | 31. prosince | 10 665,70           | 33 253,87             |
| 3    | 31. prosince | 7 156,22            | 26 097,65             |
| 4    | 31. prosince | 5 538,06            | 20 559,59             |
| 5    | 31. prosince | 4 579,89            | 15 979,70             |
| 6    | 31. prosince | 3 937,36            | 12 042,34             |

## <a name="straight-line-depreciation"></a>Lineární metoda odepisování
Hodnota v poli **Koeficient** je rovna **50**. V tomto případě bude odpis stejný v každém období a je třeba zvážit vliv vámi vybraných hodnot na ostatní pole tak, jak je to popsáno v tématu [Lineární odpisování](straight-line-service-life-depreciation.md).





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
