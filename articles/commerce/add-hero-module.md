---
title: Modul bloku obsahu
description: Tohle téma se zabývá moduly bloků s obsahem a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
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
ms.openlocfilehash: f91de93ce5ed4813f9f2adbe7678229189b5af2f
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025751"
---
# <a name="content-block-module"></a>Modul bloku obsahu


[!include [banner](includes/banner.md)]

Tohle téma se zabývá moduly bloků s obsahem a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Přehled

Modul bloku obsahu slouží k nabízení produktů a propagačních akcí prostřednictvím kombinace obrázků a textu. Maloobchodní prodejce může například přidat modul bloku obsahu na domovskou stránku webu elektronického obchodu a propagovat tak nový produkt a upoutat pozornost zákazníků.

Modul bloku obsahu je řízen daty ze systému správy obsahu (CMS). Jedná se o samostatný modul, který nezávisí na jiných modulech na stránce. Modul bloku obsahu může být umístěn na libovolné stránce webu, kde chce maloprodejce něco nabízet nebo propagovat (například produkty, prodeje nebo funkce).

## <a name="examples-of-content-block-module-in-e-commerce"></a>Příklady modulů bloků obsahu v elektronickém obchodování

- Modul bloku obsahu lze použít na domovské stránce webu elektronického obchodu a zvýraznit promoakce a nové produkty.
- Chcete-li prezentovat informace o produktu, můžete na stránce s podrobnostmi o produktu použít modul bloku obsahu.
- Do karuselového modulu lze vložit více modulů bloku obsahu pro zvýraznění více produktů nebo propagačních akcí.

## <a name="content-block-modules-and-themes"></a>Moduly bloku obsahu a motivy

Moduly bloku obsahu mohou podporovat různá rozložení a styly založené na motivu. Motiv Fabrikam například podporuje tři varianty rozvržení modulu bloku obsahu: hero, funkce a dlaždice. V rozvržení hero se zobrazuje obrázek na pozadí s překrytím textu. Rozvržení funkce zobrazuje obrázek a text vedle sebe. Rozložení dlaždic umožňuje více bloků obsahu ve formátu dlaždic.

Kromě toho může motiv vystavovat různé vlastnosti pro každé rozvržení. Vývojář motivů může vytvořit další rozložení s více styly pomocí modulu bloku obsahu.

Na následujícím obrázku je znázorněn příklad modulu blok obsahu s rozvržením Hero.

![Příklad hlavního modulu](./media/Hero.PNG)

Na následujícím obrázku je znázorněn příklad modulu blok obsahu s rozvržením funkce.

![Příklady propagačních modulů](./media/Feature.PNG)

## <a name="content-block-module-properties"></a>Vlastnosti modulu bloku obsahu

| Název vlastnosti  | Hodnoty | Popis |
|----------------|--------|-------------|
| Obrázek          | Soubor obrázku | Obrázek lze použít pro prezentaci produktu nebo promoakce. Obrázek lze odeslat do galerie obrázků nebo lze použít existující obrázek. |
| Záhlaví        | Text a značka nadpisu (**H1**, **H2**, **H3**, **H4**, **H5** nebo **H6**) | Každý modul hlavního banneru může mít nadpis. Standardně se pro značku nadpisu používá označení **H2**. Značku však lze změnit tak, aby vyhovovala požadavkům na usnadnění. |
| Odstavec      | Text odstavce | Moduly hlavního banneru podporují text odstavce ve formátu RTF. Jsou podporovány některé základní funkce pro formát RTF, například tučné a podtržené písmo, kurzíva a hypertextové odkazy. Některé z těchto funkcí mohou být přepsány motivem stránky, který je použit pro daný modul. |
| Připojení           | Text odkazu, adresa URL odkazu, popisek ARIA (Accessible Rich Internet Applications) a **Otevřít odkaz na nové kartě** | Moduly hlavního banneru podporují jeden nebo více odkazů pro volání akce. Je-li přidán odkaz, je nutné zadat text odkazu, adresu URL a popisek ARIA. Popisky ARIA by měly být názorné, aby splňovaly požadavky na usnadnění. Odkazy lze konfigurovat tak, aby byly otevřeny na nové kartě. |

## <a name="content-block-module-properties-exposed-by-the-fabrikam-theme"></a>Vlastnosti modulu bloku obsahu vystavené motivem Fabrikam 

| Název vlastnosti  | Hodnoty | Popis |
|----------------|--------|-------------|
| Umístění textu | **Vlevo**, **Vpravo**, **Střed** | Tato vlastnost definuje pozici textu na obrázku. Vztahuje se pouze na rozvržení Hero. |
| Motiv textu     | **Světlý** nebo **Tmavý** | Pro text lze definovat barevné schéma, které je založeno na obrázku pozadí. Má-li například obrázek tmavé pozadí, je možné použít světlý motiv, aby byl text lépe viditelný a odpovídal poměrům kontrastu barev pro účely usnadnění. Vztahuje se pouze na rozvržení Hero.|
| Umístění obrázku       | **Vlevo**, **vpravo** | Tato vlastnost určuje, zda má být obrázek vlevo nebo vpravo od textu. Vztahuje se pouze na rozvržení funkce.  |

## <a name="add-a-content-block-module-to-a-new-page"></a>Přidání modulu bloku obsahu na novou stránku

Chcete-li přidat modul hlavního banneru na novou stránku a nastavit požadované vlastnosti, postupujte následujícím způsobem.

1. Přejděte na **Šablony** a vytvořte šablonu stránky s názvem **šablona bloku obsahu**.
1. V pozici **Hlavní** na výchozí stránce přidejte modul hlavního banneru.
1. Vraťte šablonu se změnami a publikujte ji.
1. Šablonu hero, kterou jste právě vytvořili, použijte pro vytvoření stránky s názvem **Stránka bloku obsahu**.
1. V pozici **Hlavní** na výchozí stránce vyberte tlačítko se třemi tečkami (**...**) a vyberte možnost **Přidat modul**.
1. V dialogovém okně **Přidat modul** v části **Vyberte moduly** vyberte modul hlavního banneru a poté klikněte na tlačítko **OK**.
1. V levém stromu osnovy vyberte modul bloku obsahu.
1. V podokně vlastností vpravo vyberte možnost **Přidat obrázek**. Poté buď vyberte existující obrázek, nebo odešlete nový obrázek.
1. Vyberte **Nadpis**.
1. V dialogovém okně **Nadpis** přidejte text nadpisu, vyberte úroveň nadpisu a poté klikněte na tlačítko **OK**.
1. V části **Formátovanýtext** přidejte text podle potřeby.
1. Vyberte **Přidat odkaz**.
1. V dialogovém okně **Odkaz** přidejte text odkazu, adresu URL odkazu a popisek ARIA pro daný odkaz a poté klikněte na tlačítko **OK**.
1. Vyberte rozvržení **Hero**.
1. Uložte stránku a zobrazte náhled změn.
1. Vraťte stránku se změnami a publikujte ji.

## <a name="additional-resources"></a>Další zdroje

[Přehled startovací sady](starter-kit-overview.md)

[Modul propagačního banneru](add-alert.md)

[Karuselový modul](add-carousel.md)

[Modul textového bloku](add-content-rich-block.md)

[Modul videopřehrávače](add-video-player.md)
