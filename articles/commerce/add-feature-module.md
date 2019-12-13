---
title: Propagační modul
description: Tohle téma se zabývá propagačními moduly a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 76b59681d0bda11446f6db8b2685d1a0656f8f55
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785276"
---
# <a name="feature-module"></a>Propagační modul 

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Tohle téma se zabývá propagačními moduly a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Přehled

Propagační modul slouží k nabízení produktů a propagačních akcí prostřednictvím kombinace obrázků a textu. Maloobchodní prodejce může například přidat propagační modul na stránku podrobností o produktu, aby zdrůraznil charakteristiky produktu.

Propagační modul je řízen daty ze systému správy obsahu (CMS). Jedná se o samostatný modul, který nezávisí na jiných modulech na stránce. Propagační modul může být umístěn na libovolné stránce webu, kde chce maloprodejce něco nabízet nebo propagovat (například produkty, prodeje nebo funkce).

## <a name="examples-of-feature-modules-in-e-commerce"></a>Příklady propagačních modulů v elektronickém obchodování

Propagační modul se může používat na následujících stránkách:

- K prezentaci charakteristik produktu na stránce s podrobnostmi o produktu
- Domovská stránka k propagaci produktů
- Stránka kategorie, která umožňuje zvýraznit kategorii produktů

## <a name="feature-module-properties"></a>Vlastnosti propagačního modulu

| Název vlastnosti     | Hodnoty | Popis |
|-------------------|--------|-------------|
| Obrázek             | Soubor obrázku | Obrázek lze použít pro nabízení produktu nebo promoakce. Obrázek lze odeslat do galerie obrázků nebo lze použít existující obrázek. |
| Záhlaví           | Text a značka nadpisu (**H1**, **H2**, **H3**, **H4**, **H5** nebo **H6**) | Každý propagační modul může mít nadpis. Standardně se pro značku nadpisu používá označení **H2**. Značku však lze změnit tak, aby vyhovovala požadavkům na usnadnění. |
| Odstavec         | Text odstavce | Propagační moduly podporují text odstavce ve formátu RTF. Jsou podporovány některé základní funkce pro formát RTF, například tučné a podtržené písmo, kurzíva a hypertextové odkazy. Některé z těchto funkcí mohou být přepsány motivem stránky, který je použit pro daný modul. |
| Připojení              | Text odkazu, adresa URL odkazu, popisek ARIA (Accessible Rich Internet Applications) a **Otevřít odkaz na nové kartě** | Propagační moduly podporují jeden nebo více odkazů pro volání akce. Je-li přidán odkaz, je nutné zadat text odkazu, adresu URL a popisek ARIA. Popisky ARIA by měly být názorné, aby splňovaly požadavky na usnadnění. Odkazy lze konfigurovat tak, aby byly otevřeny na nové kartě. |
| Umístění obrázku   | **Vpravo**, **vlevo**, **nahoře** nebo **dole** | Tato vlastnost definuje pozici obrázku vzhledem k danému textu. Je-li například vybrána volba **Vpravo**, zobrazí se obrázek napravo od textu. |
| Velikost sloupce pro obrázek | Hodnota od **1** do **12** | Tato vlastnost definuje velikost obrázku vzhledem k danému textu. Velikost je vyjádřena jako počet sloupců na stránce. Na stránce je 12 sloupců. Ve výchozím nastavení má obrázek a text stejnou velikost (šest sloupců). Velikost však lze upravit podle potřeby. |

## <a name="add-a-feature-module-to-a-new-page"></a>Přidání propagačního modulu na novou stránku 

Chcete-li přidat propagační modul na novou stránku a nastavit požadované vlastnosti, postupujte následujícím způsobem.

1. Přejděte na **Šablony** a vytvořte šablonu stránky s názvem **Propagační šablona**.
1. V pozici **Hlavní** na výchozí stránce přidejte propagační modul.
1. Vraťte šablonu se změnami a publikujte ji.
1. Propagační šablonu, kterou jste právě vytvořili, použijte pro vytvoření stránky s názvem **Propagační stránka**.
1. V pozici **Hlavní** na výchozí stránce vyberte tlačítko se třemi tečkami (**...**) a vyberte možnost **Přidat modul**.
1. V dialogovém okně **Přidat modul** v části **Vyberte moduly** vyberte propagační modul a poté klikněte na tlačítko **OK**.
1. V levém stromu osnovy vyberte propagační modul.
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

[Modul hlavního banneru](add-hero-module.md)

[Modul přehrávače videa](add-video-player.md)
