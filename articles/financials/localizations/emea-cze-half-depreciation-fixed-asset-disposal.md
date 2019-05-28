---
title: Pololetní odpisy vyřazení dlouhodobého majetku pro Českou republiku
description: Toto téma vysvětluje, jak nastavit pololetní odpisy, tak abyste mohli použít pololetní odpisy dlouhodobého majetku, který je prodaný nebo jinak vyřazený.
author: EvgenyPopovMBS
manager: AnnBe
ms.date: 10/31/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 264554
ms.search.region: Czech Republic
ms.author: epopov
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 278020131f329990d0e18b3367acd7d39aa09912
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/07/2019
ms.locfileid: "1537654"
---
# <a name="half-yearly-depreciation-on-fixed-asset-disposal-for-the-czech-republic"></a>Pololetní odpisy vyřazení dlouhodobého majetku pro Českou republiku

[!include [banner](../includes/banner.md)]

Toto téma vysvětluje, jak nastavit pololetní odpisy, tak abyste mohli použít pololetní odpisy dlouhodobého majetku, který je prodaný nebo jinak vyřazený.

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




