---
title: Degresivní odpis 200 procent
description: Tento článek poskytuje přehled metody degresivního odpisu 200%.
author: moaamer
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: kfend
ms.custom: 13951
ms.assetid: 69b4e010-7683-4dc2-8a06-6d572f37e903
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7abcf26f3e658e8a6f451f26240890d183547982
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8870155"
---
# <a name="200-percent-reducing-balance-depreciation"></a>Degresivní odpis 200 procent

[!include [banner](../includes/banner.md)]

Tento článek poskytuje přehled metody degresivního odpisu 200%.

Pokud nastavujete odpisový profil dlouhodobého majetku a zaškrtnete volbu **Degresivní 200 %** v poli **Metoda** na stránce **Odpisové profily**, dlouhodobý majetek, který je přiřazen k tomuto odpisovému profilu, bude odpisován o stejný procentní podíl v každém období odpisu. Procentuální hodnota se vypočte na základě životnosti majetku. Když má například majetek životnost pět let, procentuální hodnota se vypočte jako 40 procent (200 % ÷ 5). 

Tato metoda je také známá jako klesající dvojitý zůstatek.

Pokud chcete nastavit 200% degresivní odpisování, je nutné také vybrat možnosti v polích **Odpisový rok** a **Frekvence období** na stránce **Odpisové profily**. Možnosti dostupné v poli **Frekvence období** se liší v závislosti na hodnotě vybrané v poli **Odpisový rok**.

## <a name="select-a-depreciation-year"></a>Výběr odpisového roku
V poli **Odpisový rok** na stránce **Odpisové plány** můžete vybrat buď **Kalendářní** nebo **Fiskální**. Výchozí hodnota je **Kalendářní**. 

Vaše volba určí, jaké možnosti budou dostupné v poli **Frekvence období**. Toto pole definuje časové rozdělení zaúčtování odpisů a částky v kalendářním roce.

### <a name="calendar"></a>Kalendář

V poli **Odpisový rok** můžete ponechat výchozí hodnotu **Kalendářní**. 

Možnost **Kalendářní** aktualizuje odpisovou základnu 1. ledna každého roku. Odpis obvykle zůstatková účetní hodnota mínus likvidační hodnota. V níže uvedených příkladech tohoto článku je odpisová základna čitatelem v prvním výrazu ve výpočtech ve sloupci Kalkulace. 

Vyberete-li jako odpisový rok možnost **Kalendář**, v poli **Frekvence období** jsou k dispozici následující možnosti:

-   Možnost **Ročně** provede zaúčtování 31. prosince.
-   **Měsíčně** provádí zaúčtování měsíčně na konci každého kalendářního měsíce.
-   **Čtvrtletně** provádí zaúčtování čtvrtletní částky na konci každého kalendářního čtvrtletí (31. března, 30. června, 30. září a 31. prosince).
-   **Pololetně** provádí zaúčtování pololetní částky na konci poloviny kalendářního roku (30. června a 31. prosince).
-   Položka **Denně** zaúčtuje částku odpisu pro metodu denních odpisů s použitím jedné transakce pro každý den.

### <a name="fiscal"></a>Fiskální

Vyberete-li možnost **Fiskální** v poli **Odpisový rok**, degresivní odpis 200 % je vypočten na základě fiskálního roku pro fiskální kalendář, který je určen pro knihu, nebo pro fiskální kalendář, který je vybrán na stránce **Hlavní kniha**. Fiskální kalendáře se nastavují na stránce **Fiskální kalendáře**. 

Například pro fiskální rok od 1. července do 30. června začíná výpočet odpisů datem 1. července. Fiskální rok může být delší nebo kratší než 12 měsíců. Odpisy se upravují pro jednotlivá období. Délka dalšího fiskálního roku záleží na nastavení období na stránce **Fiskální kalendáře**. 

Vyberete-li jako odpisový rok možnost **Fiskální**, v poli **Frekvence období** jsou k dispozici následující možnosti:

-   Možnost **Ročně** zaúčtuje celkovou částku odpisu vypočteného pro fiskální rok jako jednu částku poslední den fiskálního roku.
-   **Fiskální období** zaúčtuje celkovou částku odpisu vypočteného pro fiskální rok. Tato částka se rozloží do fiskálních období, která jsou definována na stránce **Fiskální kalendáře**.

## <a name="example-of-200-reducing-balance-depreciation"></a>Příklad 200% degresivního odpisování

| &nbsp;                         | &nbsp; |
|--------------------------------|--------|
| Pořizovací náklady               | 11 000 |
| Zůstatková hodnota                  | 1 000 |
| Odpisová základna              | 10 000 |
| Roky životnosti             | 5      |
| Roční procentuální hodnota odpisu | 40 %    |

Metoda degresivního odepisování 200 % vydělí 200 procent počtem roků životnosti. Procentuální hodnota se vynásobí čistou účetní hodnotou majetku, aby byla určena částka odpisu pro rok.

| Období | Výpočet částky ročního odpisu | Účetní hodnota             | Čistá účetní hodnota na konci roku |
|--------|-----------------------------------------------|------------------------|---------------------------------------|
| Rok 1 | (11 000 − 1000) × 40 % = 4000                | 11 000 − 4000 = 7000 | 11 000 – 1000 – 4000 = 6000        |
| Rok 2 | 6000 × 40 % = 2400                           | 7000 – 2400 = 4600  | 6000 – 2400 = 3600                 |
| Rok 3 | 3600 × 40 % = 1440                           | 4600 – 1440 = 3160  | 3600 – 1440 = 2160                 |

> [!NOTE] 
> Když částka vypočtená s použitím metody 200% degresivního odpisování klesne pod hodnotu menší než má částka, která by byla vypočtena s použitím lineární metody, obvykle dojde k převodu na lineární metodu pro zbytek životnosti.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
