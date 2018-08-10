---
title: "Počáteční mimořádný odpis"
description: "Tento článek podává přehled o funkci počátečního mimořádného odpisu."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetBonus
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 3621
ms.assetid: 835ec594-744e-461c-a676-1b9abc094173
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 48d50cbba648beb9831e186cd160853abe79c4e4
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="bonus-depreciation"></a>Počáteční mimořádný odpis

[!include [banner](../includes/banner.md)]

Tento článek podává přehled o funkci počátečního mimořádného odpisu.

U mimořádných odpisů můžete odepsat vedlejší nebo mimořádné částky během prvního roku, ve kterém se majetek začal používat a odepisovat. Počáteční mimořádné odpisy musí být provedeny před veškerými jinými výpočty odpisů. Proto doporučujeme použít počáteční mimořádné odpisy s knihami, kde je zakázána funkce zaúčtování do hlavní knihy. Můžete použít možnost **Odstranit transakce nezaúčtované do hlavní knihy** k odstranění historických transakcí pro knihy, které nechcete zaúčtovat do hlavní knihy. Počáteční mimořádný odpis pak můžete uzpůsobit v cyklu majetku odstraněním transakcí odpisů, které byly dříve zaúčtovány. 

Počáteční mimořádný odpis lze vypočítat pomocí procesu navrhování nebo lze transakce počátečního mimořádného odpisu vytvořit ručně. Transakce počátečního mimořádného odpisu nelze vytvořit, pokud již odpisové transakce nebo transakce opravy odpisu pro danou knihu odpisů majetku existují.

Pokud pro výpočet počátečního mimořádného odpisu použijete proces navrhování, všechny existující transakce počátečního mimořádného budou zahrnuty do výpočtu základu. Výpočet zahrnuje také všechny předchozí počáteční mimořádné odpisy, které jste pro daný majetek zadali ručně. 

Pokud bude u majetku provedeno více počátečních mimořádných odpisů, zváží se jejich priorita. Každý bonus snižuje základ majetku pro další počáteční mimořádný odpis. Konečná zůstatková hodnota se v majetkovém základu pro výpočty počátečního mimořádného odpisu nebere v potaz a způsob odpisu se na počáteční mimořádný odpis nevztahuje. 

Ve Spojených státech amerických je v současné době některý majetek považován za majetek podle paragrafu 179. Pomocí odpočtu podle paragrafu 179 lze získat zpět část nebo celou hodnotu určitého majetku (až do určité výše). Náklady lze získat zpět jejich odečtením v roce, ve kterém začal být majetek používán.

## <a name="example"></a>Příklad
Předpokládejme, že následující počáteční mimořádné odpisy jsou přiřazeny ke knize odpisů majetku:

-   **Článek 179:** 1 000,00, priorita 1
-   **Volná zóna:** 30 procent, priorita 2

Předpokládejme, že pořizovací cena majetku je 5 000 USD. Při výpočtu počátečního mimořádného odpisu bude pro odpis Článku 179 částka počátečního mimořádného odpisu 1 000 USD. 

Další částka počátečního mimořádného odpisu - pro odpis ve volné zóně - se vypočítá pomocí následující kalkulace: 

Pořizovací cena - 1 000 USD (odpis podle článku 179) x 30 procent = 1 200 USD. 

Pokud je částka počátečního mimořádného odpisu větší než zbývající pořizovací cena, bude částka počátečního mimořádného odpisu výsledkem výpočtu pro počáteční mimořádný odpis nebo zbývající pořizovací cena podle toho, která je nižší. 

Pokud se zbývající pořizovací cena rovná 0 (nule) nebo je nižší, nebudou se transakce počátečního mimořádného odpisu generovat. 

Když se počáteční mimořádný odpis vypočítá pomocí procesu navrhování, vytvoří se transakce počátečního mimořádného odpisu pro všechny odpovídající záznamy počátečního mimořádného odpisu, které jsou přiřazeny ke knize odpisů majetku. 

Lze vytvořit neomezený počet záznamů počátečního mimořádného odpisu. Jakmile tyto záznamy přiřadíte ke knize odpisů skupiny majetku, použijí se i v knize odpisů majetku. 

Počáteční mimořádný odpis se zadává buď jako procento, nebo jako pevná částka. Při zaúčtování návrhů na odpisy budou transakce počátečního mimořádného odpisu zaúčtovány do knihy odpisů jako transakce, které jsou odděleny od odpisových transakcí.




