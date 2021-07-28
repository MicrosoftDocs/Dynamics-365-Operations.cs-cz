---
title: Modul seznamu obrázků
description: Tohle téma se zabývá moduly seznamu obrázků a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 07/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 485d0714927cef5a292fd1beee826a90e9233e35
ms.sourcegitcommit: 7e976059118938b0089e40bef948029a8c088b38
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/09/2021
ms.locfileid: "6479422"
---
# <a name="image-list-module"></a>Modul seznamu obrázků

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Tohle téma se zabývá moduly seznamu obrázků a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.

Modul seznamu obrázků lze použít ke snadnému přidání kolekce (pole) obrázků na stránky webu. Každý obrázek v poli lze konfigurovat pomocí odstavcového textu a adres URL odkazů. Modul seznamu obrázků je nejvhodnější pro zobrazení log značky nebo seznamu, který obsahuje loga.

> [!IMPORTANT]
> - Modul seznamu obrázků je k dispozici v knihovně modulu Commerce od verze Dynamics 365 Commerce 10.0.20.
> - Modul seznamu obrázků je uveden v motivu Adventure Works.

Následující obrázek ukazuje příklad, kde modul seznamu obrázků zobrazuje seznam textu, který obsahuje loga na stránce webu od firmy pro spotřebitele Adventure Works.

![Příklad modulu seznamu obrázků, který zobrazuje seznam textu obsahujícího loga](./media/Image_list.PNG)

Následující obrázek ukazuje příklad, kde modul seznamu obrázků zobrazuje loga značky na stránce webu od firmy pro firmy (B2B) Adventure Works.

![Příklad modulu seznamu obrázků, který zobrazuje loga značky](./media/Image_list_B2B.PNG)

## <a name="image-list-module-properties"></a>Vlastnosti modulu seznamu obrázků

| Název vlastnosti | Hodnoty | popis |
|---------------|--------|-------------|
| Záhlaví       | Text a značka nadpisu (**H1**, **H2**, **H3**, **H4**, **H5** nebo **H6**) | Textový nadpis pro modul seznamu obrázků. |
| Seznam obrázků    | Obrázky, text a adresy URL | Každá položka v poli je obrázek, který je doprovázen odstavcovým textem a adresou URL. |

## <a name="add-an-image-list-module-to-a-new-page"></a>Přidání modulu seznamu obrázků na novou stránku

Chcete-li přidat modul seznamu obrázků na novou stránku a nastavit jeho požadované vlastnosti v tvůrci webů Commerce, postupujte následujícím způsobem.

1. Přejděte na **Šablony** a otevřete marketingovou šablonu pro domovskou stránku svého webu (nebo vytvořte novou marketingovou šablonu).
1. V pozici **Hlavní** na výchozí stránce vyberte tlačítko se třemi tečkami (**...**) a vyberte možnost **Přidat modul**.
1. V dialogovém okně **Přidat modul** vyberte modul **Seznam obrázků** a poté klikněte na tlačítko **OK**.
1. Chcete-li vrátit šablonu se změnami, vyberte možnost **Uložit**, pak **Dokončit úpravy** a volbou **Publikovat** ji publikujte.
1. Přejděte na **Stránky** a otevřete domovskou stránku webu (nebo vytvořte novou domovskou stránku pomocí marketingové šablony).
1. V pozici **Hlavní** na výchozí stránce vyberte tlačítko se třemi tečkami (**...**) a vyberte možnost **Přidat modul**.
1. V dialogovém okně **Přidat modul** vyberte **Seznam obrázků** a poté klikněte na tlačítko **OK**.
1. V podokně vlastností modulu seznamu obrázků přidejte záhlaví (například **Naše značky**).
1. Přidejte položku seznamu obrázků a zadejte obrázek, text odstavce a adresu URL přesměrování.
1. Podle potřeby přidejte a nakonfigurujte další moduly položky seznamu obrázků.
1. Vyberte možnost **Uložit** a poté vyberte možnost **Náhled**, chcete-li zobrazit náhled stránky.
1. Chcete-li vrátit šablonu se změnami, vyberte možnost **Dokončit úpravy** a volbou **Publikovat** ji publikujte.

## <a name="additional-resources"></a>Další prostředky

[Přehled knihovny modulů](starter-kit-overview.md)

[Motiv Adventure Works](adventure-works-theme.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
