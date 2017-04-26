---
title: "Půl roku odpisu při vyřazení dlouhodobého majetku pro Českou republiku"
description: "Toto téma vysvětluje, jak nastavit pololetní odpisy, tak, že použijete poloviční roční odpisy dlouhodobého majetku, které jsou prodávány nebo jinak."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 264554
ms.assetid: 7d9048c0-244a-4513-8f2d-05c63afdfce0
ms.search.region: Czech Republic
ms.author: epopov
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 6bb98cc72c2ec0c1551412dd39d5bea3ce10e2cd
ms.openlocfilehash: 40bd67a26f006b1e948cb1a82c9299d9a8fb9416
ms.lasthandoff: 03/31/2017


---

# <a name="half-yearly-depreciation-on-fixed-asset-disposal-for-the-czech-republic"></a>Pololetní odpisy vyřazení dlouhodobého majetku pro Českou republiku

[!include[banner](../includes/banner.md)]


Toto téma vysvětluje, jak nastavit pololetní odpisy, tak, že použijete poloviční roční odpisy dlouhodobého majetku, které jsou prodávány nebo jinak.

Při prodeji dlouhodobého majetku nebo převedl, můžete použít poloviční roční odpisy majetku pro daňové účely. Pololetní odpisy lze použít bez ohledu na datum vyřazení.

## <a name="set-up-depreciation-methods-for-the-depreciation-profile"></a>Nastavení metod odpisů pro odpisový profil
Použijte metody odpisů Rovnoměrné CZ a Zrychlené CZ pro uplatnění pololetních odpisů pro dlouhodobý majetek.

1.  Klepněte na tlačítko **dlouhodobého majetku**&gt;**nastavení**&gt;**odpisy**&gt;**Odpisové plány**.
2.  Klepněte na tlačítko **Nový** a vytvořte odpisový plán.
3.  V **metoda** pole: vyberte **Rovnoměrně CZ** nebo **Zrychleně CZ**.
4.  V **Odpisový rok** pole: vyberte **kalendář** jako základ pro výpočet odpisů.
5.  V **frekvence období** pole: vyberte **roční**.

## <a name="apply-the-halfyearly-depreciation-method"></a>Použití halfyearly metoda odpisu
Po nastavení metod odpisů lze použít pololetní odpisy majetku pro vyřazený majetek.

1.  Klepněte na tlačítko **dlouhodobého majetku**&gt;**deníky**&gt;**dlouhodobého majetku**.
2.  Na **přehled** karta, klepněte na tlačítko **nové** vytvořte deník a poté zadejte požadované podrobnosti.
3.  Klepněte na tlačítko **řádky** otevřete **doklad deníku** stránky.
4.  Vytvořte řádek deníku pro dlouhodobý majetek, který byl prodán nebo jinak vyřazen.
5.  Klepněte na tlačítko **návrhy**&gt;**návrh odpisu** otevřete **návrh odpisu** stránky.
6.  V **datum** zadejte datum deníku.
7.  Vyberte **vypočítat částku odpisu pololetní** políčko pololetní odpisy počítají. Je-li toto políčko zaškrtnuto, je roční částka odpisu vydělených dvěma a zaokrouhlena podle zaokrouhlení nastavení pro knihy odpisů.
8.  Volitelné: Vyberte **Shrnout odpisy** políčko, chcete-li shrnutí vypočteného odpisu pro každý dlouhodobý majetek nebo pro každý oceňovací model.
9.  Klepněte na tlačítko **OK** zavřete **návrh odpisu** stránky.
10. Zaúčtovat deník





