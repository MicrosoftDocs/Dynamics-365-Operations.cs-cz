---
title: Degresivní odpis 175 %
description: Toto téma poskytuje přehled metody degresivního odpisu 175 %.
author: saraschi2
manager: AnnBe
ms.date: 10/30/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 13911
ms.assetid: cc5d001f-bcfe-4602-9ec1-9e265e9fd188
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3a21c315aa9a7193c20e4184da20d4d6d38386c4
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441194"
---
# <a name="175-percent-reducing-balance-depreciation"></a>Degresivní odpis 175 %

[!include [banner](../includes/banner.md)]

Toto téma poskytuje přehled metody degresivního odpisu 175 %.

Pokud nastavujete odpisový profil dlouhodobého majetku a zaškrtnete volbu **Degresivní 175 %** v poli **Metoda** na stránce **Odpisové profily**, dlouhodobý majetek, který je přiřazen k tomuto odpisovému profilu, bude odpisován o stejný procentní podíl v každém období odpisu. 

Pokud chcete nastavit 175% degresivní odpisování, je nutné také vybrat možnosti v polích **Odpisový rok** a **Frekvence období** na stránce **Odpisové profily**. Možnosti dostupné v poli **Frekvence období** se liší v závislosti na hodnotě vybrané v poli **Odpisový rok**.

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

Vyberete-li možnost **Fiskální** v poli **Odpisový rok**, degresivní odpis 175 % je vypočten na základě fiskálního roku pro fiskální kalendář, který je určen pro knihu, nebo pro fiskální kalendář, který je vybrán na stránce **Hlavní kniha**. Fiskální kalendáře se nastavují na stránce **Fiskální kalendáře**. Více informací získáte v tématu [Fiskální kalendáře, fiskální roky a období](../budgeting/fiscal-calendars-fiscal-years-periods.md).

Například pro fiskální rok od 1. července do 30. června začíná výpočet odpisů datem 1. července. Fiskální rok může být delší nebo kratší než 12 měsíců. Odpisování je automaticky upravováno pro jednotlivá období a délka dalšího fiskálního roku je určována dle nastavení období na stránce **Fiskální kalendáře**. 

Vyberete-li jako odpisový rok možnost **Fiskální**, v poli **Frekvence období** jsou k dispozici následující možnosti:

-   **Ročně** - Zaúčtuje celkovou částku odpisu vypočteného pro fiskální rok poslední den fiskálního roku.
-   **Fiskální období** vypočte celkovou částku odpisu pro fiskální rok. Tato částka se rozloží do fiskálních období, která jsou definována na stránce **Fiskální kalendáře**.

## <a name="example-of-175-reducing-balance-depreciation"></a>Příklad 175% degresivního odpisování

|                                |        |
|--------------------------------|--------|
| Pořizovací náklady               | 11 000 |
| Zůstatková hodnota                  | 1 000  |
| Odpisová základna              | 10 000 |
| Roky životnosti             | 5      |
| Roční procentuální hodnota odpisu | 35 %    |

Metoda degresivního odepisování 175 % vydělí 175 procent počtem roků životnosti. Procentuální hodnota se vynásobí čistou účetní hodnotou majetku, aby byla určena částka odpisu pro rok.

| Období | Výpočet částky ročního odpisu | Účetní hodnota                  | Čistá účetní hodnota na konci roku |
|--------|-----------------------------------------------|-----------------------------|---------------------------------------|
| Rok 1 | (11 000 – 1 000) × 35 % = 3 500                | 11 000 – 3 500 = 7 500      | 11 000 – 1 000 – 3 500 = 6 500        |
| Rok 2 | 6 500 × 35 % = 2 275                           | 7 500 – 2 275 = 5 225       | 6 500 – 2 275 = 4 225                 |
| Rok 3 | 4 225 × 35 % = 1 478,75                        | 5 225 – 1 478,75 = 3 746,25 | 4 225 – 1 478,75 = 2 746,25           |

> [!NOTE] 
> Když částka vypočtená s použitím metody 175% degresivního odpisování klesne pod hodnotu menší než má částka, která by byla vypočtena s použitím lineární metody, obvykle dojde k převodu na lineární metodu pro zbytek životnosti.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]