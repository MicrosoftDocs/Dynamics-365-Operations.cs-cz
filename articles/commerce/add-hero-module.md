---
title: Modul hlavního banneru
description: Tohle téma se zabývá moduly hlavního banneru a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: c43704992e9759e7207f1b1c9bc958449daa6d1d
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785377"
---
# <a name="hero-module"></a>Modul hlavního banneru

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Tohle téma se zabývá moduly hlavního banneru a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Přehled

Modul hlavního banneru slouží k nabízení produktů a propagačních akcí prostřednictvím kombinace obrázků a textu. Maloobchodní prodejce může například přidat modul hlavního banneru na domovskou stránku webu elektronického obchodu a propagovat tak nový produkt a upoutat pozornost zákazníků.

Modul hlavního banneru je řízen daty ze systému správy obsahu (CMS). Jedná se o samostatný modul, který nezávisí na jiných modulech na stránce. Modul hlavního banneru může být umístěn na libovolné stránce webu, kde chce maloprodejce něco nabízet nebo propagovat (například produkty, prodeje nebo funkce).

## <a name="examples-of-hero-module-in-e-commerce"></a>Příklady modulů hlavního banneru v elektronickém obchodu

- Modul hlavního banneru lze použít na domovské stránce webu elektronického obchodu a zvýraznit promoakce a nové produkty.
- Chcete-li prezentovat informace o produktu, můžete na stránce s podrobnostmi o produktu použít modul hlavního banneru.
- Do karuselového modulu lze vložit více modulů hlavního banneru pro zvýraznění více produktů nebo propagačních akcí.

## <a name="hero-module-properties"></a>Vlastnosti modulu hlavního banneru

| Název vlastnosti  | Hodnoty | Popis |
|----------------|--------|-------------|
| Obrázek          | Soubor obrázku | Obrázek lze použít pro prezentaci produktu nebo promoakce. Obrázek lze odeslat do galerie obrázků nebo lze použít existující obrázek. |
| Záhlaví        | Text a značka nadpisu (**H1**, **H2**, **H3**, **H4**, **H5** nebo **H6**) | Každý modul hlavního banneru může mít nadpis. Standardně se pro značku nadpisu používá označení **H2**. Značku však lze změnit tak, aby vyhovovala požadavkům na usnadnění. |
| Odstavec      | Text odstavce | Moduly hlavního banneru podporují text odstavce ve formátu RTF. Jsou podporovány některé základní funkce pro formát RTF, například tučné a podtržené písmo, kurzíva a hypertextové odkazy. Některé z těchto funkcí mohou být přepsány motivem stránky, který je použit pro daný modul. |
| Připojení           | Text odkazu, adresa URL odkazu, popisek ARIA (Accessible Rich Internet Applications) a **Otevřít odkaz na nové kartě** | Moduly hlavního banneru podporují jeden nebo více odkazů pro volání akce. Je-li přidán odkaz, je nutné zadat text odkazu, adresu URL a popisek ARIA. Popisky ARIA by měly být názorné, aby splňovaly požadavky na usnadnění. Odkazy lze konfigurovat tak, aby byly otevřeny na nové kartě. |
| Umístění textu | **Vlevo nahoře**, **Vpravo nahoře**, **Uprostřed nahoře**, **Vlevo dole**, **Vpravo dole**, **Uprostřed dole**, **Uprostřed vlevo**, **Uprostřed vpravo** nebo **Uprostřed** | Tato vlastnost definuje pozici obrázku vzhledem k danému textu. Je-li například vybrána volba **Vpravo**, zobrazí se obrázek napravo od textu. |
| Motiv textu     | **Světlý** nebo **Tmavý** | Pro text lze definovat barevné schéma, které je založeno na obrázku pozadí. Má-li například obrázek tmavé pozadí, je možné použít světlý motiv, aby byl text lépe viditelný a odpovídal poměrům kontrastu barev pro účely usnadnění. |
| Přechod       | **Pravda** nebo **nepravda** | Přechod může být použit na obrázek, aby vyhověl poměrům kontrastu barev pro účely usnadnění. |

## <a name="add-a-hero-module-to-a-new-page"></a>Přidání modulu hlavního banneru na novou stránku

Chcete-li přidat modul hlavního banneru na novou stránku a nastavit požadované vlastnosti, postupujte následujícím způsobem.

1. Přejděte na **Šablony** a vytvořte šablonu stránky s názvem **Šablona hlavního banneru**.
1. V pozici **Hlavní** na výchozí stránce přidejte modul hlavního banneru.
1. Vraťte šablonu se změnami a publikujte ji.
1. Šablonu hlavního banneru, kterou jste právě vytvořili, použijte pro vytvoření stránky s názvem **Stránka hlavního banneru**.
1. V pozici **Hlavní** na výchozí stránce vyberte tlačítko se třemi tečkami (**...**) a vyberte možnost **Přidat modul**.
1. V dialogovém okně **Přidat modul** v části **Vyberte moduly** vyberte modul hlavního banneru a poté klikněte na tlačítko **OK**.
1. V levém stromu osnovy vyberte modul hlavního banneru.
1. V podokně vlastností vpravo vyberte možnost **Přidat obrázek**. Poté buď vyberte existující obrázek, nebo odešlete nový obrázek.
1. Vyberte **Nadpis**.
1. V dialogovém okně **Nadpis** přidejte text nadpisu, vyberte úroveň nadpisu a poté klikněte na tlačítko **OK**.
1. V části **Formátovanýtext** přidejte text podle potřeby.
1. Vyberte možnost **Přidat odkazakce**.
1. V dialogovém okně **Odkaz na akci** přidejte text odkazu, adresu URL odkazu a popisek ARIA pro daný odkaz a poté klikněte na tlačítko **OK**.
1. Uložte stránku a zobrazte náhled změn.
1. Vraťte stránku se změnami a publikujte ji.

## <a name="additional-resources"></a>Další zdroje

[Přehled startovací sady](starter-kit-overview.md)

[Modul výstrahy](add-alert.md)

[Karuselový modul](add-carousel.md)

[Modul bloku s formátovaným obsahem](add-content-rich-block.md)

[Modul umístění obsahu](add-content-placement-modules.md)

[Propagační modul](add-feature-module.md)

[Modul přehrávače videa](add-video-player.md)
