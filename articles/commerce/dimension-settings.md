---
title: Použít nastavení zobrazení pro rozměry produktu
description: Toto téma popisuje nastavení zobrazení pro rozměry produktu a popisuje, jak je použít v Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: b901622bbfc8d6b3066879f6456a4ab618ca4076
ms.sourcegitcommit: 53b797ff1b524f581046b48cdde42f50b37495bc
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/28/2021
ms.locfileid: "6117213"
---
# <a name="apply-display-settings-for-product-dimensions"></a>Použít nastavení zobrazení pro rozměry produktu

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Toto téma popisuje nastavení zobrazení pro rozměry produktu a popisuje, jak je použít v Microsoft Dynamics 365 Commerce.

Dynamics 365 Commerce podporuje rozměry, styl a barevné rozměry k rozlišení variant produktu. Rozměry se obvykle zobrazují jako textové hodnoty, například „Malé“, „Střední“ a „Velké“ pro velikosti a „Černé“ a „Hnědé“ pro barvy. Pokud však produkt podporuje mnoho variant, může být obtížné procházet varianty produktu, protože k zobrazení obrázku pro každou variantu je zapotřebí více výběrů. Aby bylo snazší procházet varianty produktů, může verze Commerce verze 10.0.20 používat obrázky a hexadecimální (hex) kódy k zobrazení dimenzí jako políček.

V nástroji pro tvorbu webu Commerce je nastavení dimenzí definováno v **Nastavení webu \> Rozšíření \> Nastavení dimenzí**. Následující obrázek ukazuje příklad nastavení dimenze v nástroji pro tvorbu webů.

![Příklad nastavení webu v nástroji pro tvorbu webů Commerce](./dev-itpro/media/swatch_site_settings.PNG)

K dispozici jsou dvě nastavení dimenze:

- **Rozměry k zobrazení jako obrázek** - Určete, které dimenze by se měly objevit jako vzorník na stránkách webu elektronického obchodování, jako jsou stránky s podrobnostmi o produktu (PDP) a stránky se seznamem výsledků hledání. Jakoukoli kombinaci barev, velikostí a rozměrů stylu lze zobrazit jako vzorník. Pokud je vybrána dimenze pro zobrazení jako vzorník, vykreslení modulu Commerce bude hledat dostupnou konfiguraci vzorníku hexadecimálního kódu. Pokud není nakonfigurován žádný hexadecimální kód, systémová logika bude hledat konfiguraci vzorníku adresy URL obrázku. Pokud není nakonfigurován hexadecimální kód ani adresa URL obrázku, zobrazí se text.

    Následující ilustrace ukazuje příklad, kdy PDP na webu elektronického obchodování zahrnuje vzorníky barev a velikostí. V tomto příkladu je hexadecimální kód nakonfigurován pro barevnou dimenzi. Vzorník se proto zobrazuje jako barvy. Pro dimenzi velikosti však není nakonfigurován hexadecimální kód ani adresa URL obrázku. Proto se zobrazí text.

    ![Příklad barevné dimenze zobrazené jako vzorky na stránce s podrobnostmi o produktu elektronického obchodování](./dev-itpro/media/swatch_pdp.png)

- **Rozměry k zobrazení na kartě produktu** - Určete, jaké rozměry by se měly objevit na produktových kartách, které se zobrazují v seznamech a na stránkách seznamů. Než se dimenze může zobrazit na produktové kartě, musí být pro tuto dimenzi povoleno toto nastavení. Nastavení **Rozměry k zobrazení jako obrázek** by mělo být také povoleno. Chování výběru vzorků na produktových kartách je optimalizováno pro barevnou dimenzi. U jiných dimenzí může být vyžadováno rozšíření pohledu k přizpůsobení chování výběru vzorků.

    Následující obrázek ukazuje příklad, kdy stránka seznamu na webu elektronického obchodování obsahuje karty produktů, které obsahují vzorníky barev.

    ![Příklad barevné dimenze zobrazené jako vzorky na stránce se seznamem elektronického obchodování](./dev-itpro/media/swatch_searchresults.PNG)

Informace o tom, jak nakonfigurovat dimenze produktu tak, aby se na stránkách webu zobrazovaly jako vzorník, najdete v části [Nakonfigurujte hodnoty dimenze produktu tak, aby se zobrazovaly jako vzorky](./dev-itpro/dimensions-swatch.md).

## <a name="additional-resources"></a>Další prostředky

[Přehled knihovny modulů](starter-kit-overview.md)

[Modul výsledků hledání](search-result-module.md)

[Modul buy boxu](add-buy-box.md)

[Nakonfigurujte hodnoty dimenze produktu tak, aby se zobrazovaly jako vzorky](./dev-itpro/dimensions-swatch.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
