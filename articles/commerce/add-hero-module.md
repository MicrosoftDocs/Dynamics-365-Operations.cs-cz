---
title: Modul bloku obsahu
description: Tento článek se zabývá moduly bloků s obsahem a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: dc6d728f49befd0c156340379dba05f592ca7919
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9276993"
---
# <a name="content-block-module"></a>Modul bloku obsahu

[!include [banner](includes/banner.md)]

Tento článek se zabývá moduly bloků s obsahem a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.

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

![Příklad hlavního modulu.](./media/Hero.PNG)

Na následujícím obrázku je znázorněn příklad modulu blok obsahu s rozvržením funkce.

![Příklady propagačních modulů.](./media/Feature.PNG)

## <a name="content-block-module-properties"></a>Vlastnosti modulu bloku obsahu

| Název vlastnosti  | Hodnoty | popis |
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

1. Přejděte na **Šablony** a vytvořte šablonu stránky s názvem **Šablona bloku obsahu**.
1. V pozici **Hlavní** na výchozí stránce přidejte modul hlavního banneru.
1. Chcete-li vrátit šablonu se změnami, vyberte možnost **Uložit**, pak **Dokončit úpravy** a volbou **Publikovat** ji publikujte.
1. Šablonu hero, kterou jste právě vytvořili, použijte pro vytvoření stránky s názvem **Stránka bloku obsahu**.
1. V pozici **Hlavní** na výchozí stránce vyberte tlačítko se třemi tečkami (**...**) a vyberte možnost **Přidat modul**.
1. V dialogovém okně **Vybrat moduly** vyberte modul hlavního banneru a poté vyberte **OK**.
1. V levém stromu osnovy vyberte modul bloku obsahu.
1. V podokně vlastností vpravo vyberte možnost **Přidat obrázek**. Poté buď vyberte existující obrázek, nebo odešlete nový obrázek.
1. Vyberte **Nadpis**.
1. V dialogovém okně **Nadpis** přidejte text nadpisu, vyberte úroveň nadpisu a poté klikněte na tlačítko **OK**.
1. V části **Formátovanýtext** přidejte text podle potřeby.
1. Vyberte **Přidat odkaz**.
1. V dialogovém okně **Odkaz** přidejte text odkazu, adresu URL odkazu a popisek ARIA pro daný odkaz a poté klikněte na tlačítko **OK**.
1. Vyberte rozvržení **Hero**.
1. Vyberte možnost **Uložit** a poté vyberte možnost **Náhled**, chcete-li zobrazit náhled stránky.
1. Chcete-li vrátit šablonu se změnami, vyberte možnost **Dokončit úpravy** a volbou **Publikovat** ji publikujte. 

## <a name="additional-resources"></a>Další prostředky

[Přehled knihovny modulů](starter-kit-overview.md)

[Modul propagačního banneru](add-alert.md)

[Karuselový modul](add-carousel.md)

[Modul textového bloku](add-content-rich-block.md)

[Modul videopřehrávače](add-video-player.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
