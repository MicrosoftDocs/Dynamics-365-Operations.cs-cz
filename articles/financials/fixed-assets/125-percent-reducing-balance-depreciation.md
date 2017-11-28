---
title: "Degresivní odpis 125 procent"
description: "Tento článek poskytuje přehled o metodě odpisu „degresivní odpis 125 procent“."
author: saraschi2
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 13871
ms.assetid: 3abc263e-59d6-4f1a-986d-1be388948bd3
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 8ec88d799c44e035b6490861383557f8c3beda41
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="125-percent-reducing-balance-depreciation"></a>Degresivní odpis 125 procent

[!include[banner](../includes/banner.md)]


Tento článek poskytuje přehled o metodě odpisu „degresivní odpis 125 procent“.

Pokud nastavujete odpisový profil dlouhodobého majetku a zaškrtnete volbu **Degresivní 125 %** v poli **Metoda** na stránce **Odpisové profily**, dlouhodobý majetek, který je přiřazen k tomuto odpisovému profilu, bude odpisován o stejný procentní podíl v každém období odpisu. Tato procentuální hodnota se vypočte na základě životnosti majetku. Když má například majetek životnost pět let, procentuální hodnota se vypočte jako 25 procent (125 % ÷ 5).

Pokud chcete nastavit 125% degresivní odpisování, je nutné také vybrat možnosti v polích **Odpisový rok** a **Frekvence období** na stránce **Odpisové profily**. Možnosti dostupné v poli **Frekvence období** se liší v závislosti na hodnotě vybrané v poli **Odpisový rok**.

## <a name="select-a-depreciation-year"></a>Výběr odpisového roku
V poli **Odpisový rok** na stránce **Odpisové plány** můžete vybrat buď **Kalendářní** nebo **Fiskální**. Výchozí hodnota je **Kalendářní**. 

Vaše volba určí, jaké možnosti budou dostupné v poli **Frekvence období**. Toto pole definuje časové rozdělení zaúčtování odpisů a částky v kalendářním roce.

### <a name="calendar"></a>Kalendář

V poli **Odpisový rok** můžete ponechat výchozí hodnotu **Kalendářní**. 

Možnost **Kalendářní** aktualizuje odpisovou základnu 1. ledna každého roku. Odpisová základna je obvykle zůstatková účetní hodnota mínus likvidační hodnota. V níže uvedených příkladech této kapitoly je odpisová základna čitatelem v prvním výrazu ve výpočtech ve sloupci Kalkulace. 

Vyberete-li jako odpisový rok možnost **Kalendář**, v poli **Frekvence období** jsou k dispozici následující možnosti:

-   Možnost **Ročně** provede zaúčtování 31. prosince.
-   **Měsíčně** provádí zaúčtování měsíčně na konci každého kalendářního měsíce.
-   **Čtvrtletně** provádí zaúčtování čtvrtletní částky na konci každého kalendářního čtvrtletí (31. března, 30. června, 30. září a 31. prosince).
-   **Pololetně** provádí zaúčtování pololetní částky na konci poloviny kalendářního roku (30. června a 31. prosince).
-   Položka **Denně** zaúčtuje částku odpisu pro metodu denních odpisů s použitím jedné transakce pro každý den.

### <a name="fiscal"></a>Fiskální

Vyberete-li možnost **Fiskální** v poli **Odpisový rok**, degresivní odpis 125 % je vypočten na základě fiskálního roku pro fiskální kalendář, který je určen pro knihu, nebo pro fiskální kalendář, který je vybrán na stránce **Hlavní kniha**. Fiskální kalendáře se nastavují na stránce **Fiskální kalendáře**. 

Například pro fiskální rok od 1. července do 30. června začíná výpočet odpisů datem 1. července. Fiskální rok může být delší nebo kratší než 12 měsíců. Odpisování je automaticky upravováno pro jednotlivá období a délka dalšího fiskálního roku je určována dle nastavení období na stránce **Fiskální kalendáře**. 

Vyberete-li jako odpisový rok možnost **Fiskální**, v poli **Frekvence období** jsou k dispozici následující možnosti:

-   Možnost **Ročně** zaúčtuje celkovou částku odpisu vypočteného pro fiskální rok jako jednu částku poslední den fiskálního roku.
-   **Fiskální období** zaúčtuje celkovou částku odpisu vypočteného pro fiskální rok. Tato částka se rozloží do fiskálních období, která jsou definována na stránce **Fiskální kalendáře**.

## <a name="example-of-125-reducing-balance-depreciation"></a>Příklad 125% degresivního odpisování
|                                |        |
|--------------------------------|--------|
| Pořizovací náklady               | 11 000 |
| Zůstatková hodnota                  | 1 000  |
| Odpisová základna              | 10 000 |
| Roky životnosti             | 5      |
| Roční procentuální hodnota odpisu | 25 %    |

Metoda degresivního odepisování 125 % vydělí 125 procent počtem roků životnosti. Procentuální hodnota se vynásobí čistou účetní hodnotou majetku, aby byla určena částka odpisu pro rok.

| Období | Výpočet částky ročního odpisu | Účetní hodnota                    | Čistá účetní hodnota na konci roku |
|--------|-----------------------------------------------|-------------------------------|---------------------------------------|
| Rok 1 | (11 000 – 1 000) × 25 % = 2 500                | (11 000 – 2 500) = 8 500      | (11 000 – 1 000 – 2 500) = 7 500      |
| Rok 2 | 7 500 × 25 % = 1 875                           | (8 500 – 1 875) = 6 625       | (7 500 – 1 875) = 5 625               |
| Rok 3 | 5 625 × 25 % = 1 406,25                        | (6 625 – 1 406,25) = 5 218,75 | (5 625 – 1 406,25) = 4 218,75         |

> [!NOTE] 
> Když částka vypočtená s použitím metody 125% degresivního odpisování klesne pod hodnotu menší než má částka, která by byla vypočtena s použitím lineární metody, obvykle dojde k převodu na lineární metodu pro zbytek životnosti.




