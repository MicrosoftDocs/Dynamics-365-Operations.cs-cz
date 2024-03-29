---
title: Pololetní odpisy vyřazení dlouhodobého majetku pro Českou republiku
description: Tento článek vysvětluje, jak nastavit pololetní odpisy, tak abyste mohli použít pololetní odpisy dlouhodobého majetku, který je prodaný nebo jinak vyřazený.
author: EvgenyPopovMBS
ms.date: 10/31/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: kfend
ms.custom: 264554
ms.search.region: Czech Republic
ms.author: epopov
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: d1f5ddcccd5265cc4345b3ce4a8914f610d51144
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8872380"
---
# <a name="half-year-depreciation-on-fixed-asset-disposal-for-the-czech-republic"></a>Pololetní odpisy vyřazení dlouhodobého majetku pro Českou republiku

[!include [banner](../includes/banner.md)]

Tento článek vysvětluje, jak nastavit pololetní odpisy, tak abyste mohli použít pololetní odpisy dlouhodobého majetku, který je prodaný nebo jinak vyřazený.

Při prodeji nebo jiném vyřazení dlouhodobého majetku můžete použít pololetní odpisy majetku pro daňové účely. Pololetní odpisy lze použít bez ohledu na datum vyřazení.

## <a name="set-up-depreciation-methods-for-the-depreciation-profile"></a>Nastavení metod odpisů pro odpisový profil
Použijte metody odpisů Rovnoměrné CZ a Zrychlené CZ pro uplatnění pololetních odpisů pro dlouhodobý majetek.

1.  Klikněte na **Dlouhodobý majetek** &gt; **Nastavení** &gt; **Odpisy** &gt; **Odpisové plány**.
2.  Klepněte na tlačítko **Nový** a vytvořte odpisový plán.
3.  V poli **Metoda** vyberte **Rovnoměrné CZ** nebo **Zrychlené CZ**.
4.  V poli **Odpisový rok** vyberte jako základ pro výpočet odpisů možnost **Kalendář**.
5.  V poli **Frekvence období** vyberte **Roční**.

## <a name="apply-the-half-yearly-depreciation-method"></a>Použití pololetní metody odpisů
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






[!INCLUDE[footer-include](../../includes/footer-banner.md)]