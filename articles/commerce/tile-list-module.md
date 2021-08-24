---
title: Modul seznamu dlaždice
description: Tohle téma se zabývá moduly seznamu dlaždic a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 07/08/2021
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
ms.openlocfilehash: 513775afe325008ebd6cd18d2d9485a972984090da3803d255a1584b16b1e014
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6767844"
---
# <a name="tile-list-module"></a>Modul seznamu dlaždice

[!include [banner](includes/banner.md)]

Tohle téma se zabývá moduly seznamu dlaždic a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.

Modul seznamu dlaždic je kolekce dlaždic v karuselu. Používá se k marketingu kategorií produktů nebo značek produktů prostřednictvím obrázků a textu. Například prodejce může přidat modul seznamů dlaždic na domovskou stránku webu elektronického obchodování, aby propagoval všechny nejprodávanější kategorie.

Modul seznamu dlaždic je řízen daty ze systému správy obsahu (CMS). Nezávisí na žádných dalších modulech nebo datech z centrály Commerce. Modul seznamu dlaždic může být přidán na libovolnou stránku webu, kde chce maloprodejce něco nabízet nebo propagovat (například produkty, kategorie nebo značky).

Následující obrázek ukazuje příklad modulu seznamu dlaždic a modulů dlaždic na domovské stránce Adventure Works.

![Příklad modulu seznamu dlaždic a modulů dlaždic na domovské stránce Adventure Works](./media/Tile_list.PNG)

> [!IMPORTANT]
> Modul seznamu dlaždic je k dispozici od verze Dynamics 365 Commerce 10.0.20.
> Modul seznamu dlaždic je uveden v motivu Adventure Works.

## <a name="tile-list-modules-and-themes"></a>Moduly a motivy seznamu dlaždic

Modul seznamu dlaždic může podporovat různá rozložení a styly založené na motivu. Například v motivu Adventure Works dlaždice zobrazují efekt animace, když nad nimi uživatelé webu umístí kurzor. Každý motiv může obsahovat další vlastnosti pro seznam dlaždic a moduly dlaždic. Vývojáři motivů mohou také vytvářet další rozložení pro seznam dlaždic a moduly dlaždic.

## <a name="tile-list-module-properties"></a>Vlastnosti modulu seznamu dlaždic

| Název vlastnosti | Hodnoty | popis |
|---------------|--------|-------------|
| Záhlaví       | Text a značka nadpisu | Textový nadpis pro modul seznamu dlaždic. |

## <a name="tile-module-properties"></a>Vlastnosti modulu dlaždic

| Název vlastnosti | Hodnoty | popis |
|---------------|--------|-------------|
| Obrázek         | Soubor obrázku | Obrázek lze použít pro prezentaci produktu nebo kategorie. Obrázek lze nahrát do knihovny médií v nástroji pro tvorbu webů Commerce nebo lze použít existující obrázek. |
| Záhlaví       | Text a značka nadpisu (**H1**, **H2**, **H3**, **H4**, **H5** nebo **H6**) | Standardně je použita značka nadpisu **H2** pro nadpis, ale značku lze změnit, aby odpovídala požadavkům na přístupnost. |
| Odstavec     | Text odstavce | Modul podporuje text odstavce ve formátu RTF. Jsou podporovány některé základní funkce pro formát RTF, například hypertextové odkazy, tučné a podtržené písmo, kurzíva. Některé z těchto funkcí mohou být přepsány motivem stránky, který je použit pro daný modul. |
| Připojení          | Text odkazu, adresa URL odkazu, popisek ARIA (Accessible Rich Internet Applications) a **Otevřít odkaz na nové kartě** | Moduly podporují jeden nebo více odkazů „výzvy k akci“. Je-li přidán odkaz, je nutné zadat text odkazu, adresu URL a popisek ARIA. Popisky ARIA by měly být názorné, aby splňovaly požadavky na usnadnění. Odkazy lze konfigurovat tak, aby byly otevřeny na nové kartě. |
| Odkaz na dlaždici     | Text odkazu, adresa URL odkazu, popisek ARIA a volič **Otevřít odkaz na nové kartě** | Tato vlastnost se používá k definování odkazu „výzva k akci“. Je-li přidán odkaz, je nutné zadat text odkazu, adresu URL a popisek ARIA. Popisky ARIA by měly být názorné, aby splňovaly požadavky na usnadnění. Odkazy lze konfigurovat tak, aby byly otevřeny na nové kartě.|
| Ikona          | Obrázek | Kromě obrázku produktu nebo kategorie lze přidat symbol ikony. Obrázek symbolu ikony se objeví nad obrázkem produktu nebo kategorie. |

## <a name="add-a-tile-list-module-to-a-new-page"></a>Přidání modulu seznamu dlaždic na novou stránku

Chcete-li přidat modul seznamu dlaždic na novou stránku a nastavit požadované vlastnosti, postupujte následujícím způsobem.

1. Přejděte na **Šablony** a otevřete marketingovou šablonu pro domovskou stránku svého webu (nebo vytvořte novou marketingovou šablonu).
1. V pozici **Hlavní** na výchozí stránce vyberte tlačítko se třemi tečkami (**...**) a vyberte možnost **Přidat modul**.
1. V dialogovém okně **Přidat modul** vyberte modul **Seznam dlaždic** a poté klikněte na tlačítko **OK**.
1. Chcete-li vrátit šablonu se změnami, vyberte možnost **Uložit**, pak **Dokončit úpravy** a volbou **Publikovat** ji publikujte.
1. Přejděte na **Stránky** a otevřete domovskou stránku webu (nebo vytvořte novou domovskou stránku pomocí marketingové šablony).
1. V pozici **Hlavní** na výchozí stránce vyberte tlačítko se třemi tečkami (**...**) a vyberte možnost **Přidat modul**.
1. V dialogovém okně **Přidat modul** vyberte modul **Seznam dlaždic** a poté klikněte na tlačítko **OK**.
1. V podokně vlastností modulu seznamu dlaždic přidejte nadpis.
1. V pozici **Seznam dlaždic** vyberte tlačítko se třemi tečkami (**...**) a poté vyberte možnost **Přidat modul**.
1. V dialogovém okně **Přidat modul** vyberte modul **Modul dlaždic** a poté klikněte na tlačítko **OK**.
1. V podokně vlastností modulu dlaždic přidejte obrázek, záhlaví a obrázek symbolu ikony.
1. Podle potřeby přidejte a nakonfigurujte další moduly dlaždic.
1. Vyberte možnost **Uložit** a poté vyberte možnost **Náhled**, chcete-li zobrazit náhled stránky.
1. Chcete-li vrátit šablonu se změnami, vyberte možnost **Dokončit úpravy** a volbou **Publikovat** ji publikujte.

## <a name="additional-resources"></a>Další prostředky

[Přehled knihovny modulů](starter-kit-overview.md)

[Motiv Adventure Works](adventure-works-theme.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
