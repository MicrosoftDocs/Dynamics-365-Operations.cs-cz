---
title: Modul galerie médií
description: Tohle téma se zabývá moduly galerie médií a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 0d05129145c5d6c3967b243cb0855a1c4fd3e84e
ms.sourcegitcommit: ccb39767bd3430c24f4653c26560bba2cd66553c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/19/2022
ms.locfileid: "8780861"
---
# <a name="media-gallery-module"></a>Modul galerie médií

[!include [banner](includes/banner.md)]

Tohle téma se zabývá moduly galerie médií a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.

Moduly galerie médií zobrazují jeden nebo více obrázků v zobrazení galerie. Moduly galerie médií podporují miniatury, které lze uspořádat vodorovně (jako řádek pod obrázkem) nebo svisle (jako sloupec vedle obrázku). Moduly galerie médií také poskytují funkce, které umožňují přiblížení (zvětšení) obrázků nebo zobrazení v režimu celé obrazovky. Aby bylo možné vykreslit obrázek v modulu galerie médií, musí být k dispozici v knihovně médií v knihovně médií v tvůrci webu Commerce. V současné době moduly galerie médií podporují pouze obrázky.

Ve výchozím režimu modul galerie médií používá ID produktu, které je dostupné z kontextu stránky na stránce s podrobnostmi o produktu (PDP), k vykreslení odpovídajících obrázků produktu. V centrále Commerce musí být pro všechny produkty definována cesta k souborům médií. Obrázky by pak měly být nahrány do knihovny médií Tvůrce stránek podle cesty k souboru, která byla definována pro produkty v centrále Commerce. Tyto obrázky zahrnují obrázky pro produkty a všechny varianty produktů. Další informace o tom, jak nahrávat obrázky do knihovny médií Tvůrce stránek, získáte v tématu [Nahrání obrázků](dam-upload-images.md).

Alternativně může modul galerie médií hostovat na stránce galerie obrázků plně uspořádanou sadu obrázků, kde neexistují žádné závislosti na ID produktu nebo kontextu stránky. V tomto případě musí být obrázky nahrány do knihovny médií Tvůrce stránek a určeny v Tvůrci stránek.

Zde je několik příkladů použití modulů galerie médií:

- Vykreslování obrázků produktu na PDP
- Vykreslování obrázků produktu na stránce marketingu produktů
- Představení kurátorské sady obrázků na marketingové stránce, například na stránce galerie

V příkladu na následujícím obrázku hostuje nákupní box na PDP obrázky produktů pomocí modulu galerie médií.

![Příklad nákupního boxu na stránce s podrobnostmi o produktu, který hostuje obrázky produktů pomocí modulu galerie médií.](./media/ecommerce-pdp-buybox.PNG)

## <a name="media-gallery-properties"></a>Vlastnosti galerie médií

| Název vlastnosti | Hodnoty | popis |
|---------------|--------|-------------|
| Zdroj obrázku | **Kontext stránky** nebo **ID produktu** | Výchozí hodnota je **Kontext stránky**. Pokud je vybrán **Kontext stránky**, modul očekává, že stránka poskytne informace o ID produktu. Je-li vybráno **ID produktu**, musí být jako hodnota názvu produktu uvedeno ID produktu vlastnosti **ID produktu**. Tato funkce je dostupná v Commerce verze 10.0.12. |
| ID produktu | ID produktu | Tato vlastnost je použitelná, pouze pokud je hodnota vlastnosti **Zdroj obrázku** **ID produktu**. |
| Zvětšení obrázku | **Vložený** nebo **Kontejner** | Tato vlastnost umožňuje uživateli přibližovat obrázky v modulu galerie médií. Obrázek lze přiblížit buď jako vložený, nebo v samostatném kontejneru vedle obrázku. Tato schopnost je dostupná ve verzi 10.0.12. |
| Faktor zvětšení | Desetinné číslo | Tato vlastnost určuje faktor měřítka pro zvětšení obrázků. Například pokud je hodnota nastavena na **2,5**, jsou obrázky 2,5krát zvětšeny. |
| Celá obrazovka | **Pravda** nebo **nepravda** | Tato vlastnost určuje, zda lze obrázky prohlížet v režimu celé obrazovky. V režimu celé obrazovky lze obrázky dále zvětšovat, pokud je zapnuta funkce zoomu. Tato schopnost je k dispozici v aplikaci Commerce verze 10.0.13. |
| Kvalita zvětšeného obrázku | Číslo od 1 do 100, které představuje procento a které je vybráno pomocí ovládacího prvku trackbar | Tato vlastnost definuje kvalitu obrazu pro zvětšené obrázky. Lze ji nastavit na 100 procent, aby bylo zajištěno, že zvětšený obrázek vždy používá nejvyšší možné rozlišení. Tato vlastnost není použitelná pro soubory PNG, protože používají bezztrátový formát. Tato schopnost je k dispozici v aplikaci Commerce verze 10.0.19. |
| Obrázky | Obrázky, které jsou vybrány z knihovny médií Tvůrce stránek | Kromě vykreslení z produktu lze obrázky upravovat také pro modul galerie médií. Tyto obrázky budou připojeny ke všem dostupným obrázkům produktu. Tato funkce je dostupná v Commerce verze 10.0.12. |
| Orientace miniatury | **Vertikální** nebo **Horizontální** | Tato vlastnost určuje, zda se mají miniatury zobrazovat ve svislém nebo vodorovném pruhu. |
| Skrýt obrázky hlavních produktů pro variantu | **Pravda** nebo **nepravda** | Pokud je tato vlastnost nastavena na **Pravda**, je-li vybrána varianta, jsou obrázky hlavního produktu skryty, pokud varianta neobsahuje žádné obrázky. Tato vlastnost nemá vliv na produkty, které nemají žádné varianty. |
| Aktualizace média při výběru dimenze | **Pravda** nebo **nepravda** | Pokud je tato vlastnost nastavena na **True**, obrázky v knihovně médií budou aktualizovány, když je vybrána jakákoli dimenze (například barva, styl nebo velikost) a pokud je k dispozici obrázek. Tato vlastnost pomáhá zjednodušit procházení, protože ne každá dimenze varianty produktu musí být vybrána, aby byl aktualizován odpovídající obrázek. Tato vlastnost je k dispozici na kartě **Rozšířené**. |

> [!IMPORTANT]
> Vlastnost **Aktualizace média při výběru dimenze** je k dispozici od verze Commerce verze 10.0.21. Vyžaduje instalaci balíčku knihovny modulů Commerce verze 9.31.

Následující obrázek ukazuje příklad modulu galerie médií, kde jsou k dispozici možnosti celé obrazovky a přiblížení.

![Příklad modulu galerie médií, kde jsou k dispozici možnosti celé obrazovky a přiblížení.](./media/ecommerce-media-zoom.png)

Následující obrázek ukazuje příklad modulu galerie médií, který obsahuje uspořádané obrázky (tj. učené obrázky nezávisí na ID produktu nebo kontextu stránky).

![Příklad modulu galerie médií, který má uspořádané obrázky.](./media/ecommerce-media-curated.PNG)

## <a name="commerce-scale-unit-interaction"></a>Interakce Commerce Scale Unit

Pokud je zdroj obrázku odvozen z kontextu stránky, k načtení obrázků se použije ID produktu z PDP. Modul galerie médií načítá cestu k souboru obrázku pro produkty pomocí rozhraní API Commerce Scale Unit. Obrázky jsou poté staženy z knihovny médií, aby mohly být vykresleny v modulu.

## <a name="add-a-media-gallery-module-to-a-page"></a>Přidání modulu galerie médií na stránku

Chcete-li přidat modul galerie médií na marketingovou stránku, postupujte podle následujících kroků.

1. Přejděte na **Šablony** a poté volbou **Nová** vytvořte novou šablonu.
1. V dialogovém okně **Nová šablona** v části **Název šablony** zadejte **Šablona marketingu** a poté klikněte na tlačítko **OK**.
1. V pozici **Tělo** vyberte tři tečky (**...**) a poté vyberte možnost **Přidat modul**.
1. V dialogovém okně **Vybrat moduly** vyberte modul **Výchozí stránka** a poté klikněte na tlačítko **OK**.
1. V pozici **Hlavní** na výchozí stránce vyberte tlačítko se třemi tečkami (**...**) a vyberte možnost **Přidat modul**.
1. V dialogovém okně **Vybrat moduly** vyberte modul **Kontejner** a poté klikněte na **OK**.
1. Chcete-li vrátit šablonu se změnami, vyberte možnost **Uložit**, pak **Dokončit úpravy** a volbou **Publikovat** ji publikujte.
1. Přejděte na **Stránky** a volbou **Nová** vytvořte novou stránku.
1. V dialogovém okně **Vytvořit novou stránku** v části **Název stránky** zadejte **Stránka galerie médií** a poté vyberte **Další**.
1. V části **Vyberte šablonu** vyberte vytvořenou položku **Marketingová šablona** a poté vyberte **Další**.
1. V části **Vyberte rozložení** vyberte rozložení stránky (např. **Flexibilní rozložení**) a poté vyberte **Další**.
1. V části **Zkontrolovat a dokončit** zkontrolujte konfiguraci stránky. Pokud potřebujete upravit informace o stránce, vyberte **Zpět**. Pokud jsou informace o stránce správné, vyberte **Vytvořit stránku**. 
1. V pozici **Hlavní** na nové stránce vyberte tlačítko se třemi tečkami (**...**) a vyberte možnost **Přidat modul**.
1. V dialogovém okně **Vybrat moduly** vyberte modul **Kontejner** a poté klikněte na **OK**.
1. V pozici **Kontejner** vyberte tři tečky (**...**) a poté vyberte možnost **Přidat modul**.
1. V dialogovém okně **Vyberte moduly** vyberte modul **Galerie médií** a poté klikněte na tlačítko **OK**.
1. V podokně vlastností modulu galerie médií pod **Zdroj obrázku** vyberte **Productid**. Pak do pole **ID produktu** zadejte ID produktu.
1. Vyberte možnost **Uložit** a poté vyberte možnost **Náhled**, chcete-li zobrazit náhled stránky. Obrázky produktu byste měli vidět v zobrazení galerie.
1. Chcete-li použít pouze uspořádané obrázky, v podokně vlastností pod **Zdroj obrázku** vyberte **Productid**. Pak v části **Obrázky** vyberte **Přidat obrázek** tolikrát, kolikrát je třeba k přidání obrázků z knihovny médií.
1. Nastavte všechny další vlastnosti, které chcete nastavit, například **Zvětšení obrázku**, **Faktor zvětšení** a **Orientace miniatur**.
1. Chcete-li po dokončení vrátit fragment stránky se změnami, vyberte možnost **Uložit**, pak **Dokončit úpravy** a volbou **Publikovat** jej publikujte.

## <a name="additional-resources"></a>Další prostředky

[Přehled knihovny modulů](starter-kit-overview.md)

[Modul buy boxu](add-buy-box.md)

[Modul kontejneru](add-container-module.md)

[Odeslání obrázků](dam-upload-images.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
