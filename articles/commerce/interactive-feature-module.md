---
title: Modul interaktivní funkce
description: Tohle téma se zabývá interaktivní moduly funkce a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: a01fb446a1b7dd07e0429b96ff949b88a591f800
ms.sourcegitcommit: 7e976059118938b0089e40bef948029a8c088b38
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/09/2021
ms.locfileid: "6479423"
---
# <a name="interactive-feature-module"></a>Modul interaktivní funkce

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Tohle téma se zabývá interaktivní moduly funkce a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.

Interaktivní moduly funkcí jsou mozaikové moduly, které lze použít k uvedení na trh více kategorií produktů nebo značek produktů pomocí kombinace obrázků a textu. Například prodejce může přidat modul interaktivní funkce na domovskou stránku webu elektronického obchodování, aby propagoval nejprodávanější kategorie. Modul interaktivních funkcí se podobá modulu seznamu dlaždic, ale má jiné rozložení a různé funkce interakce.

Každý modul interaktivních funkcí je sbírkou modulů položek interaktivních prvků. Každý modul položky funkce je řízen daty ze systému správy obsahu (CMS). Nezávisí na žádných dalších modulech nebo datech z centrály Commerce. Modul interaktivní funkce může být přidán na libovolnou stránku webu, kde chce maloprodejce něco nabízet nebo propagovat (například produkty, kategorie nebo značky).

> [!IMPORTANT]
> - Modul interaktivní funkce je k dispozici od verze Dynamics 365 Commerce verze 10.0.20.
> - Modul interaktivní funkce je uveden v motivu Adventure Works.

Následující obrázek ukazuje příklad modulu interaktivní funkce na domovské stránce Adventure Works.

![Příklad modulu interaktivní funkce na domovské stránce Adventure Works](./media/Feature.PNG)

## <a name="interactive-feature-module-and-themes"></a>Modul a motivy interaktivní funkce

Modul interaktivní funkce může podporovat různá rozložení a styly založené na motivu. Například v motivu Adventure Works má modul interaktivních funkcí rozložení ve dvou sloupcích, které zobrazuje efekty animace, když uživatel webu umístí kurzor nad každou položku. Modul interaktivních funkcí je optimalizován pro sudý počet obrázků, které jsou uspořádány ve dvousloupcovém rozvržení.

## <a name="interactive-feature-module-properties"></a>Vlastnosti modulu interaktivní funkce

| Název vlastnosti | Hodnoty | popis |
|---------------|--------|-------------|
| Záhlaví       | Text a značka nadpisu (**H1**, **H2**, **H3**, **H4**, **H5** nebo **H6**) | Textový nadpis pro modul interaktivní funkce. |

## <a name="interactive-feature-item-module-properties"></a>Vlastnosti modulu položky interaktivní funkce

| Název vlastnosti | Hodnoty | popis |
|---------------|--------|-------------|
| Obrázek         | Soubor obrázku | Obrázek, který představuje produkt nebo kategorii. Obrázek lze nahrát do knihovny médií v nástroji pro tvorbu webů Commerce nebo lze použít existující obrázek. |
| Záhlaví       | Text a značka nadpisu (**H1**, **H2**, **H3**, **H4**, **H5** nebo **H6**) | Standardně je použita značka nadpisu **H2** pro nadpis, ale značku lze změnit, aby odpovídala požadavkům na přístupnost. |
| Odstavec     | Text odstavce | Modul podporuje text odstavce ve formátu RTF. Jsou podporovány některé základní funkce pro formát RTF, například hypertextové odkazy, tučné a podtržené písmo, kurzíva. Některé z těchto funkcí mohou být přepsány motivem stránky, který je použit pro daný modul. |
| Připojení          | Text odkazu, adresa URL odkazu, popisek ARIA (Accessible Rich Internet Applications) a volič **Otevřít odkaz na nové kartě** | Modul podporuje jeden nebo více odkazů „výzvy k akci“. Je-li přidán odkaz, je nutné zadat text odkazu, adresu URL a popisek ARIA. Popisky ARIA by měly být názorné, aby splňovaly požadavky na usnadnění. Odkazy lze konfigurovat tak, aby byly otevřeny na nové kartě. |

## <a name="add-an-interactive-feature-module-to-a-new-page"></a>Přidání modulu interaktivní funkce na novou stránku

Chcete-li přidat modul interaktivní funkce na novou stránku a nastavit jeho požadované vlastnosti v tvůrci webů Commerce, postupujte následujícím způsobem.

1. Přejděte na **Šablony** a otevřete marketingovou šablonu pro domovskou stránku svého webu (nebo vytvořte novou marketingovou šablonu).
1. V pozici **Hlavní** na výchozí stránce vyberte tlačítko se třemi tečkami (**...**) a vyberte možnost **Přidat modul**.
1. V dialogovém okně **Přidat modul** vyberte modul **Interaktivní funkce** a poté klikněte na tlačítko **OK**.
1. Chcete-li vrátit šablonu se změnami, vyberte možnost **Uložit**, pak **Dokončit úpravy** a volbou **Publikovat** ji publikujte.
1. Přejděte na **Stránky** a otevřete domovskou stránku webu (nebo vytvořte novou domovskou stránku pomocí marketingové šablony).
1. V pozici **Hlavní** na výchozí stránce vyberte tlačítko se třemi tečkami (**...**) a vyberte možnost **Přidat modul**.
1. V dialogovém okně **Přidat modul** v části **Vyberte moduly** vyberte modul **Interaktivní funkce** a poté klikněte na tlačítko **OK**.
1. V podokně vlastností modulu interaktivní funkce přidejte nadpis.
1. V pozici **Interaktivní funkce** vyberte tlačítko se třemi tečkami (**...**) a poté vyberte možnost **Přidat modul**.
1. V dialogovém okně **Přidat modul** vyberte modul **Položka interaktivní funkce** a poté klikněte na tlačítko **OK**.
1. V podokně vlastností modulu položky interaktivní funkce přidejte obrázek, text nadpisu, text odstavce a adresu URL.
1. Podle potřeby přidejte a nakonfigurujte další moduly položky interaktivní funkce.
1. Vyberte možnost **Uložit** a poté vyberte možnost **Náhled**, chcete-li zobrazit náhled stránky.
1. Chcete-li vrátit šablonu se změnami, vyberte možnost **Dokončit úpravy** a volbou **Publikovat** ji publikujte.

## <a name="additional-resources"></a>Další prostředky

[Přehled knihovny modulů](starter-kit-overview.md)

[Motiv Adventure Works](adventure-works-theme.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
