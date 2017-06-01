---
title: "Pololetní odpisy vyřazení dlouhodobého majetku pro Českou republiku"
description: "Toto téma vysvětluje, jak nastavit pololetní odpisy, tak abyste mohli použít pololetní odpisy dlouhodobého majetku, který je prodaný nebo jinak vyřazený."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 264554
ms.assetid: 7d9048c0-244a-4513-8f2d-05c63afdfce0
ms.search.region: Czech Republic
ms.author: epopov
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: bc4b55f1fe860dc4ac12743423aed985c245ee8f
ms.contentlocale: cs-cz
ms.lasthandoff: 05/25/2017


---

# <a name="half-yearly-depreciation-on-fixed-asset-disposal-for-the-czech-republic"></a>Pololetní odpisy vyřazení dlouhodobého majetku pro Českou republiku

[!include[banner](../includes/banner.md)]


Toto téma vysvětluje, jak nastavit pololetní odpisy, tak abyste mohli použít pololetní odpisy dlouhodobého majetku, který je prodaný nebo jinak vyřazený.

Při prodeji nebo jiném vyřazení dlouhodobého majetku můžete použít pololetní odpisy majetku pro daňové účely. Pololetní odpisy lze použít bez ohledu na datum vyřazení.

## <a name="set-up-depreciation-methods-for-the-depreciation-profile"></a>Nastavení metod odpisů pro odpisový profil
Použijte metody odpisů Rovnoměrné CZ a Zrychlené CZ pro uplatnění pololetních odpisů pro dlouhodobý majetek.

1.  Klikněte na **Dlouhodobý majetek** &gt; **Nastavení** &gt; **Odpisy** &gt; **Odpisové plány**.
2.  Klepněte na tlačítko **Nový** a vytvořte odpisový plán.
3.  V poli **Metoda** vyberte **Rovnoměrné CZ** nebo **Zrychlené CZ**.
4.  V poli **Odpisový rok** vyberte jako základ pro výpočet odpisů možnost **Kalendář**.
5.  V poli **Frekvence období** vyberte **Roční**.

## <a name="apply-the-halfyearly-depreciation-method"></a>Použití pololetní metody odpisů
Po nastavení metod odpisů lze použít pololetní odpisy majetku pro vyřazený majetek.

1.  Klikněte na **Dlouhodobý majetek** &gt; **Deníky** &gt; **Dlouhodobý majetek**.
2.  Na kartě **Přehled** kliknutím na možnost **Nový** vytvořte deník a zadejte požadované podrobnosti.
3.  Kliknutím na možnost **Řádky** otevřete stránku **Doklad deníku**.
4.  Vytvořte řádek deníku pro dlouhodobý majetek, který byl prodán nebo jinak vyřazen.
5.  Klepnutím na **Návrhy** &gt; **Návrh odpisu** otevřete stránku **Návrh odpisu**.
6.  Do pole **Do data** zadejte datum deníku.
7.  Zaškrtněte políčko **Vypočítat půlroční částku odpisu**, aby byla vypočítána pololetní částka odpisu. Pokud je toto políčko zaškrtnuto, je roční částka odpisu vydělena dvěma a zaokrouhlena podle nastavení zaokrouhlení knihy odpisů.
8.  Volitelné: Zaškrtněte políčko **Shrnout odpisy** pro shrnutí vypočteného odpisu pro každý dlouhodobý majetek nebo pro každý oceňovací model.
9.  Kliknutím na tlačítko **OK** zavřete stránku **Návrh odpisu**.
10. Zaúčtovat deník





