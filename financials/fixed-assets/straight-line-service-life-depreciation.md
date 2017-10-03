---
title: "Lineární odpisování"
description: "Tento článek poskytuje přehled o metodě odpisování Lineární."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 3341
ms.assetid: ae5ceaeb-aeb7-45cd-b835-23cf9c5cf95a
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 5ff3d87f610489608f0bebadd9bb4c9c5c727992
ms.contentlocale: cs-cz
ms.lasthandoff: 05/25/2017

---

# <a name="straight-line-service-life-depreciation"></a>Lineární odpisování

[!include[banner](../includes/banner.md)]


Tento článek poskytuje přehled o metodě odpisování Lineární.

Když nastavíte profil odpisu dlouhodobého majetku a vyberete na stránce Odpisové profily možnost Lineární životnost v poli Metoda, majetek, který má přiřazený tento odpisový profil, bude odepsán na základě celkové době životnosti tohoto majetku. Obvykle bude tato částka ve všech obdobích odpisu stejná. 

Odpisovaná částka vypočtená lineárním odpisem s vyrovnáním na konci životnosti se bude od částky vypočtené lineárním odpisem lišit v případě, že bude pro majetek zaúčtována změna. 

Pokud chcete nastavit lineární odpisování, je nutné také vybrat možnosti v polích Odpisový rok a Frekvence období na stránce Odpisové profily.

## <a name="select-a-depreciation-year"></a>Výběr odpisového roku
V poli Odpisový rok na stránce Odpisové plány můžete vybrat buď Kalendářní, nebo Fiskální. Tato volba určí, jaké možnosti budou dostupné v poli Frekvence období. Výchozí volbou je Kalendářní.

### <a name="calendar"></a>Kalendář

Pokud vyberete Kalendář, bude použit rok od 1. ledna do 31. prosince, a to i v případě, že jste definovali fiskální kalendář odlišně. 

Možnost Kalendář aktualizuje odpisový základ (což je obvykle čistá účetní hodnota minus konečná zůstatková hodnota) 1. ledna každého roku. V níže uvedených příkladech této kapitoly je odpisová základna čitatelem v prvním výrazu ve výpočtech ve sloupci Kalkulace. 

Jestliže vyberete možnost Kalendářní, v poli Frekvence období jsou k dispozici následující možnosti, které definují časové rozdělení zaúčtování odpisů a částky během kalendářního roku:
-   Možnost Ročně provede zaúčtování 31 prosince.
-   Měsíčně provádí zaúčtování měsíčně na konci každého kalendářního měsíce.
-   Čtvrtletně provádí zaúčtování čtvrtletní částky na konci každého kalendářního čtvrtletí (31. března, 30. června, 30. září a 31. prosince).
-   Možnost Pololetně provádí zaúčtování pololetní částky na konci poloviny kalendářního roku (30. června a 31. prosince).
-   Denně zaúčtuje částku odpisu pro metodu denních odpisů s použitím jedné transakce pro každý den.

Když například zvolíte Ročně, roční odpisy se zaúčtují pouze jednou – 31. prosince každého roku. Pokud vyberete Měsíčně, měsíční odpis se zaúčtuje každý měsíc jako 1/12 ročního odpisu.

### <a name="fiscal"></a>Fiskální

Pokud vyberete možnost Fiskální v poli Odpisový rok, bude použita metoda lineárního odpisu. Výpočet se provede na základě fiskálního roku, který je definován fiskálním kalendářem zadaným pro knihu nebo fiskálním kalendář, který je vybraný na stránce Hlavní kniha. Fiskální kalendáře se nastavují na stránce Fiskální kalendáře.

Například pro fiskální rok od 1. července do 30. června začíná výpočet odpisů datem 1. července. Fiskální rok může být delší nebo kratší než 12 měsíců. Odpisy se automaticky upravují pro jednotlivá fiskální období. Délka dalšího fiskálního roku vychází z fiskálních období nastavených při vytváření nového fiskálního roku ve formuláři Fiskální kalendáře. 

Vyberete-li Fiskální, v poli Frekvence období jsou k dispozici následující možnosti:
-   Možnost Ročně zaúčtuje celkovou částku odpisu vypočteného pro fiskální rok jako jednu částku poslední den fiskálního roku.
-   Možnost Fiskální období vypočítá celkovou částku odpisu pro fiskální rok, který se rozloží do období definovaných na formuláři Fiskální kalendáře pro daný fiskální rok.

## <a name="example-straight-line-depreciation-of-an-unchanged-fixed-asset"></a>Příklad: Lineární odpis nezměněného dlouhodobého majetku
Předpokládejme, že má dlouhodobý majetek následující charakteristiky.

|                     |        |
|---------------------|--------|
| Pořizovací náklady    | 11 000 |
| Zůstatková hodnota       | 1 000  |
| Odpisová základna   | 10 000 |
| Roky životnosti  | 5      |
| Roční odpisy | 2 000  |

Odpisovaná částka bude každý rok stejná. (Pořizovací náklady - Zůstatková hodnota) / Počet roků provozní životnosti

| Období | Výpočet částky ročního odpisu | Čistá účetní hodnota na konci roku |
|--------|-------------------------------------------|---------------------------------------|
| Rok 1 | (11 000 - 1 000) / 5 = 2 000              | 9 000                                 |
| Rok 2 | (11 000 - 1 000) / 5 = 2 000              | 7 000                                 |
| Rok 3 | (11 000 - 1 000) / 5 = 2 000              | 5 000                                 |
| Rok 4 | (11 000 - 1 000) / 5 = 2 000              | 3 000                                 |
| Rok 5 | (11 000 - 1 000) / 5 = 2 000              | 1 000                                 |

## <a name="example-straight-line-depreciation-of-a-modified-fixed-asset"></a> Příklad: Lineární odpis upraveného dlouhodobého majetku

Předpokládejme, že v roce 2 přidáme ke stejnému dlouhodobému majetku opravu pořizovací ceny ve výši 4 000. 

Doba životnosti opravy pořizovací ceny je stejná jako u dlouhodobého majetku a začíná okamžikem jeho pořízení. Na konci roku 5 zůstává zůstatková účetní hodnota odpovídající zůstatkové účetní hodnotě opravy pořizovací ceny. Odpisy podle období se vypočtou způsobem znázorněným v následující tabulce.

| Období | Výpočet částky ročního odpisu | Čistá účetní hodnota na konci roku |
|--------|-------------------------------------------|---------------------------------------|
| Rok 1 | 10 000 / 5 = 2 000                        | 11 000 - 2 000 = 9 000                |
| Rok 2 | 4 000 (oprava pořizovací ceny)            | 9 000 + 4 000 =13 000                 |
| Rok 2 | 14 000 / 5 = 2 800                        | 13 000 - 2 800 = 10 200               |
| Rok 3 | 14 000 / 5 = 2 800                        | 10 200 - 2 800 = 7 400                |
| Rok 4 | 14 000 / 5 = 2 800                        | 7 400 - 2 800 = 4 600                 |
| Rok 5 | 14 000 / 5 = 2 800                        | 4 600 - 2 800 = 1 800                 |
| Rok 6 | Zbývajících 800\*                           | 1 800 - 800 = 1 000                   |

\**Protože zbývající částka je menší než odpisovaná částka, počítá se pouze zbývající částka mínus konečná zůstatková hodnota.






