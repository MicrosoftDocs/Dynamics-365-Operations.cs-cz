---
title: Lineární odpis s vyrovnáním na konci životnosti
description: Tento článek poskytuje přehled o metodě odpisování Lineární s vyrovnáním na konci životnosti.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: roschlom
ms.custom: 13851
ms.assetid: 0fa2f71a-596c-414c-a6e6-8f7405a0bf81
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d2414ea97fefbec1e975498e171496e33057541c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4968997"
---
# <a name="straight-line-life-remaining-depreciation"></a>Lineární odpis s vyrovnáním na konci životnosti

[!include [banner](../includes/banner.md)]

Tento článek poskytuje přehled o metodě odpisování Lineární s vyrovnáním na konci životnosti.

Když nastavíte odpisový plán dlouhodobého majetku a zaškrtnete políčko **Lineární s vyrovnáním na konci životnosti** v poli **Metoda** na stránce **Profily odpisů**, budou odpisy dlouhodobého majetku přiřazeného k tomuto plánu založeny na zbývající době životnosti tohoto majetku. Obvykle bude tato částka ve všech obdobích odpisu stejná. Pokud chcete nastavit odpisování podle zbývající lineární životnosti, je nutné také vybrat možnosti v polích **Odpisový rok** a **Frekvence období** na stránce **Odpisové profily**. Možnosti dostupné v poli **Frekvence období** se liší v závislosti na hodnotě vybrané v poli **Odpisový rok**.

## <a name="select-a-depreciation-year"></a>Výběr odpisového roku
V poli **Odpisový rok** na stránce **Odpisové plány** můžete vybrat buď **Kalendářní** nebo **Fiskální**. Výchozí hodnota je **Kalendářní**. Vaše volba určí, jaké možnosti budou dostupné v poli **Frekvence období**. Toto pole definuje časové rozdělení zaúčtování odpisů a částky v kalendářním roce.

### <a name="calendar"></a>Kalendář

Pokud vyberete **Kalendář** v poli **_Odpisový rok_*_, předpokládá se rok od 1. ledna do 31. prosince, i když jste fiskální kalendář definovali odlišně. Možnost _* Kalendář** aktualizuje odpisovou základnu 1. ledna každého roku. Odpisová základna je obvykle zůstatková účetní hodnota mínus likvidační hodnota. V níže uvedených příkladech této kapitoly je odpisová základna čitatelem v prvním výrazu ve výpočtech ve sloupci Kalkulace. Vyberete-li jako odpisový rok možnost **Kalendář**, v poli **Frekvence období** jsou k dispozici následující možnosti:

-   Možnost **Ročně** provede zaúčtování 31. prosince.
-   **Měsíčně** provádí zaúčtování měsíčně na konci každého kalendářního měsíce.
-   **Čtvrtletně** provádí zaúčtování čtvrtletní částky na konci každého kalendářního čtvrtletí (31. března, 30. června, 30. září a 31. prosince).
-   **Pololetně** provádí zaúčtování pololetní částky na konci každého pololetí kalendářního roku (30. června a 31. prosince).
-   Položka **Denně** zaúčtuje částku odpisu pro metodu denních odpisů s použitím jedné transakce pro každý den.

Když například zvolíte **Ročně**, roční odpisy se zaúčtují pouze jednou – 31. prosince každého roku. Pokud vyberete **Měsíčně**, měsíční odpis se zaúčtuje každý měsíc jako 1/12 ročního odpisu.

### <a name="fiscal"></a>Fiskální

Pokud vyberete možnost **Fiskální** v poli **Odpisový rok**, bude použita metoda zbývajícího lineárního odpisu. Odpis je založen na zbývajících fiskální rocích. Například pro fiskální rok od 1. července 2015 do 30. června 2016 začíná výpočet odpisů datem 1. července. Fiskální rok může být delší nebo kratší než 12 měsíců. Odpisy se upravují pro jednotlivá fiskální období. Délka dalšího fiskálního roku záleží na nastavení fiskálního období na stránce **Fiskální kalendáře**. Vyberete-li jako odpisový rok možnost **Fiskální**, v poli **Frekvence období** jsou k dispozici následující možnosti:

-   Možnost **Ročně** zaúčtuje celkovou částku odpisu vypočteného pro fiskální rok jako jednu částku poslední den fiskálního roku.
-   **Fiskální období** vypočte celkovou částku odpisu pro fiskální rok. Tato částka se rozloží do fiskálních období, která jsou definována na stránce **Fiskální kalendáře** nebo pro fiskální kalendář uvedený pro knihu.

## <a name="example-of-straight-line-depreciation-of-an-unchanged-fixed-asset"></a>Příklady lineárního odpisu nezměněného dlouhodobého majetku
Dlouhodobý majetek má následující charakteristiky.

|                     |        |
|---------------------|--------|
| Pořizovací náklady    | 11 000 |
| Zůstatková hodnota       | 1 000  |
| Odpisová základna   | 10 000 |
| Roky životnosti  | 5      |
| Roční odpisy | 2 000  |

Částka odpisu je stejná pro každý rok: (pořizovací náklady - zůstatková hodnota) ÷ roky životnosti

| Období | Výpočet částky ročního odpisu | Čistá účetní hodnota na konci roku |
|--------|-----------------------------------------------|---------------------------------------|
| Rok 1 | (11 000 – 1 000) ÷ 5 = 2 000                  | 9 000                                 |
| Rok 2 | (9 000 – 1 000) ÷ 4 = 2 000                   | 7 000                                 |
| Rok 3 | (7 000 – 1 000) ÷ 3 = 2 000                   | 5 000                                 |
| Rok 4 | (5 000 – 1 000) ÷ 2 = 2 000                   | 3 000                                 |
| Rok 5 | (3 000 – 1 000) ÷ 1 = 2 000                   | 1 000                                 |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]