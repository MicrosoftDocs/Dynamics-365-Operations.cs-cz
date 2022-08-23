---
title: Modul aktivního obrázku
description: Tento článek se zabývá moduly aktivního obrázku a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
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
ms.dyn365.ops.version: Release 10.0.8
ms.search.industry: ''
ms.search.form: ''
ms.openlocfilehash: fdcd54adc98c7bc52ab6ff1ef7d5d03616aadfc3
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9267610"
---
# <a name="active-image-module"></a>Modul aktivního obrázku

[!include [banner](includes/banner.md)]

Tento článek se zabývá moduly aktivního obrázku a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.

K vložení značek produktu do obrázku lze použít modul aktivního obrázku. Uživatelé webu elektronického obchodování pak mohou umístit kurzor nad značky a zobrazit náhled produktů zobrazených na obrázku. Náhledy se zobrazují ve vyskakovacích oknech. Výběrem vyskakovacího okna náhledu mohou uživatelé přejít přímo na stránku podrobností o produktu (PDP) pro příslušný produkt.

Značky jsou definovány pomocí souřadnic X a Y na obrázku. Každý označený bod by měl být nakonfigurován s ID produktu, který je zobrazen na obrázku.

Následující obrázek ukazuje příklad vyskakovacího okna náhledu na obrázku banneru na domovské stránce Adventure Works.

![Příklad vyskakovacího okna náhledu v modulu aktivního obrázku](./media/Active_image.PNG)

> [!IMPORTANT]
> - Modul aktivního obrázku je k dispozici od verze Dynamics 365 Commerce verze 10.0.20.
> - Modul aktivního obrázku je uveden v motivu Adventure Works.

## <a name="active-image-module-properties"></a>Vlastnosti modulu aktivního obrázku

| Název vlastnosti      | Hodnoty | popis |
|--------------------|--------|-------------|
| Obrázek              | Soubor obrázku | Obrázek lze použít pro prezentaci jednoho nebo více produktů. Obrázek lze nahrát do knihovny médií v nástroji pro tvorbu webů Commerce nebo lze použít existující obrázek. |
| Šířka              | Počet pixelů | Tato vlastnost definuje šířku obrázku. Aktivní souřadnice se počítají na základě šířky obrázku.|
| Aktivní souřadnice | Souřadnice X a Y a identifikační číslo produktu | Každé pole aktivního obrázku se skládá ze souřadnic X a Y a identifikačního čísla produktu.|
| Záhlaví            | Text a značka nadpisu (**H1**, **H2**, **H3**, **H4**, **H5** nebo **H6**) | Standardně je použita značka nadpisu **H2** pro nadpis, ale značku lze změnit, aby odpovídala požadavkům na přístupnost. |
| Odstavec          | Text odstavce | Modul podporuje text odstavce ve formátu RTF. Jsou podporovány některé základní funkce pro formát RTF, například hypertextové odkazy, tučné a podtržené písmo, kurzíva. Některé z těchto funkcí mohou být přepsány motivem stránky, který je použit pro daný modul. |
| Připojení               | Text odkazu, adresa URL odkazu, popisek ARIA (Accessible Rich Internet Applications) a volič **Otevřít odkaz na nové kartě** | Modul podporuje jeden nebo více odkazů „výzvy k akci“. Je-li přidán odkaz, je nutné zadat text odkazu, adresu URL a popisek ARIA. Popisky ARIA by měly být názorné, aby splňovaly požadavky na usnadnění. Odkazy lze konfigurovat tak, aby byly otevřeny na nové kartě. |
| Dílčí text           | Nadpis, text a odkazy | Lze přidat další kontext pro obrázek, například jméno autora nebo návrháře nebo odkazy na osobní blogy.|
| Motiv textu         | **Světlý** nebo **Tmavý** | Tato vlastnost umožňuje uživateli nastavit text na světlý nebo tmavý na základě obrázku pozadí. Je k dispozici jako rozšíření motivu v motivu Adventure Works. |

## <a name="add-an-active-image-module-to-a-new-page"></a>Přidání modulu aktivního obrázku na novou stránku

Chcete-li přidat modul aktivního obrázku na novou stránku a nastavit požadované vlastnosti, postupujte následujícím způsobem.

1. Přejděte na **Šablony** a otevřete marketingovou šablonu pro domovskou stránku svého webu (nebo vytvořte novou marketingovou šablonu).
1. V pozici **Hlavní** na výchozí stránce vyberte tlačítko se třemi tečkami (**...**) a vyberte možnost **Přidat modul**.
1. V dialogovém okně **Vybrat moduly** vyberte modul **Aktivní obrázek** a poté klikněte na tlačítko **OK**.
1. Chcete-li vrátit šablonu se změnami, vyberte možnost **Uložit**, pak **Dokončit úpravy** a volbou **Publikovat** ji publikujte.
1. Přejděte na **Stránky** a otevřete domovskou stránku webu (nebo vytvořte novou domovskou stránku pomocí marketingové šablony).
1. V pozici **Hlavní** na výchozí stránce vyberte tlačítko se třemi tečkami (**...**) a vyberte možnost **Přidat modul**.
1. V dialogovém okně **Vybrat moduly** vyberte modul **Aktivní obrázek** a poté klikněte na tlačítko **OK**.
1. V podokně vlastností modulu aktivního obrázku přidejte obrázek a nastavte šířku plátna na velikost obrázku.
1. Nastavte souřadnice X a Y a přidejte příslušné identifikační číslo produktu.
1. Podle potřeby přidejte a nakonfigurujte další moduly aktivního obrázku.
1. Vyberte možnost **Uložit** a poté vyberte možnost **Náhled**, chcete-li zobrazit náhled stránky.
1. Chcete-li vrátit šablonu se změnami, vyberte možnost **Dokončit úpravy** a volbou **Publikovat** ji publikujte.

## <a name="additional-resources"></a>Další prostředky

[Přehled knihovny modulů](starter-kit-overview.md)

[Motiv Adventure Works](adventure-works-theme.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
