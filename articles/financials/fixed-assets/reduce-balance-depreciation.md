---
title: "Degresivní odpis"
description: "Tento článek poskytuje přehled o metodě degresivního odpisování."
author: twheeloc
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 3281
ms.assetid: 1b86763d-d47c-4a6a-a9a6-d97a736750da
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 9416af0efdf9b33b1de559d302a1ff4c5f530dce
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---

# <a name="reduce-balance-depreciation"></a>Degresivní odpis

[!include[banner](../includes/banner.md)]


Tento článek poskytuje přehled o metodě degresivního odpisování.

Pokud nastavujete odpisový plán dlouhodobého majetku a zaškrtnete volbu Zrychleně v poli Metoda na stránce Odpisové profily, odpisy dlouhodobého majetku, který je přiřazen k tomuto odpisovému plánu, prováděny o stejný procentní podíl v každém období odpisu.

Chcete-li nastavit degresivní odpisování, musíte také provést výběr v polích na pevné záložce Obecné na stránce Odpisové profily. Nejprve vyberte příslušný rok v poli Odpisový rok. V závislosti na vašem výběru se v poli Frekvence období zobrazí různé možnosti, jak je vysvětleno v následujících sekcích. 

Dále je pro odpisový plán nutné zadat hodnotu do pole Procento. Vyberte-li možnost Úplné odpisy, použije se zbývající základ odpisů v posledním odpisovém období a může jít o velkou částku. Některé země/oblasti nepoužívají přepínač na metodu lineárního odpisu. K přepínání dojde, pokud je částka alternativní metody odpisování vyšší než částka původního plánu odpisu anebo se s ní shoduje a odebraná částka odpisu je částkou alternativní metody. 

Vzhledem k tomu, že majetek nebude nikdy možné zcela odepsat na základě procentuálního výpočtu, pro úplný odpis majetku je třeba vybrat možnost Úplné odpisy.

## <a name="select-a-depreciation-year"></a>Výběr odpisového roku
V poli Odpisový rok na stránce Odpisové plány můžete vybrat buď Kalendářní, nebo Fiskální. Tato volba určí, jaké možnosti budou dostupné v poli Frekvence období. Výchozí volbou je Kalendářní.

### <a name="calendar"></a>Kalendář

Možnost Kalendářní aktualizuje odpisový základ (což je obvykle čistá účetní hodnota minus konečná zůstatková hodnota) 1. ledna každého roku. V příkladu degresivního odpisu později v tomto tématu je odpisová základna čitatelem v prvním výrazu ve výpočtech ve sloupci kalkulací. 

Jestliže vyberete možnost Kalendářní, v poli Frekvence období jsou k dispozici následující možnosti, které definují časové rozdělení zaúčtování odpisů a částky během kalendářního roku:

-   Ročně provádí zaúčtování 31. prosince.
-   Měsíčně provádí zaúčtování měsíčně na konci každého kalendářního měsíce.
-   Čtvrtletně provádí zaúčtování čtvrtletní částky na konci každého kalendářního čtvrtletí (31. března, 30. června, 30. září a 31. prosince).
-   Pololetně provádí zaúčtování pololetní částky na konci každého pololetí kalendářního roku (30. června a 31. prosince).
-   Denně zaúčtuje částku odpisu pro metodu denních odpisů s použitím jedné transakce pro každý den.

Když například zvolíte Ročně, roční odpisy se zaúčtují pouze jednou – 31. prosince každého roku. Pokud vyberete Měsíčně, měsíční odpis se zaúčtuje každý měsíc jako 1/12 ročního odpisu.

### <a name="fiscal"></a>Fiskální

Zaškrtnete-li v poli Odpisový rok volbu Fiskální, použije se metoda lineárního odpisu. Vypočítává se na základě fiskálního roku, který je nastaven na stránce Fiskální kalendáře, pro fiskální kalendář vybraný na stránce Hlavní kniha. Například pro fiskální rok od 1. července do 30. června začíná výpočet odpisů datem 1. července. Fiskální rok může být delší nebo kratší než 12 měsíců. Odpisy se upravují pro jednotlivá fiskální období. Délka dalšího fiskálního roku vychází z fiskálních období nastavených při vytváření nového fiskálního roku na stránce Fiskální kalendáře.


Vyberete-li Fiskální, v poli Frekvence období jsou k dispozici následující možnosti:

-   Ročně zaúčtuje celkovou částku odpisu vypočteného pro fiskální rok jako jednu částku poslední den fiskálního roku.
-   Fiskální období zaúčtuje celkovou částku odpisu vypočteného pro fiskální rok, která se rozloží do fiskálních období definovaných pro fiskální kalendář vybraný na stránce Hlavní kniha nebo pro fiskální kalendář vybraný pro knihu pro dlouhodobý majetek.

## <a name="example-of-reducing-balance-depreciation"></a>Příklad degresivního odpisování

Předpokládejme, že pořizovací cena dlouhodobého majetku činí 11 000, konečná zůstatková hodnota je 1000 a procentuální koeficient odpisu je 30. 

Pomocí metody Degresivní odpisování je 30 % odpisové základny (čistá účetní hodnota mínus konečná zůstatková hodnota) vypočítáno na konci předchozího odpisového období. Odpisy za první tři roky jsou uvedeny v následující tabulce.

| Období | Výpočet částky ročního odpisu | Čistá účetní hodnota na konci roku |
|--------|-------------------------------------------|---------------------------------------|
| Rok 1 | (11,000 - 1,000) \* 30% = 3,000           | (11 000 – 1 000) – 3 000 = 7 000      |
| Rok 2 | (7,000 - 1,000) \* 30% = 1,800            | (7 000 – 1 800) = 5 200                |
| Rok 3 | (5,200 - 1,000) \* 30% = 1,260            | (5 200 – 1 260) = 3 940               |

 
-






