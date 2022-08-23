---
title: Modul seznamu obrázků
description: Tento článek se zabývá moduly seznamu obrázků a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: e89624a98d3cbdd861391e994386ae57d2c38aa0
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269828"
---
# <a name="image-list-module"></a>Modul seznamu obrázků

[!include [banner](includes/banner.md)]

Tento článek se zabývá moduly seznamu obrázků a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.

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
1. V dialogovém okně **Výběr modulů** vyberte modul **Seznam obrázků** a poté klikněte na tlačítko **OK**.
1. Chcete-li vrátit šablonu se změnami, vyberte možnost **Uložit**, pak **Dokončit úpravy** a volbou **Publikovat** ji publikujte.
1. Přejděte na **Stránky** a otevřete domovskou stránku webu (nebo vytvořte novou domovskou stránku pomocí marketingové šablony).
1. V pozici **Hlavní** na výchozí stránce vyberte tlačítko se třemi tečkami (**...**) a vyberte možnost **Přidat modul**.
1. V dialogovém okně **Vybrat moduly** vyberte modul **Seznam obrázků** a poté klikněte na **OK**.
1. V podokně vlastností modulu seznamu obrázků přidejte záhlaví (například **Naše značky**).
1. Přidejte položku seznamu obrázků a zadejte obrázek, text odstavce a adresu URL přesměrování.
1. Podle potřeby přidejte a nakonfigurujte další moduly položky seznamu obrázků.
1. Vyberte možnost **Uložit** a poté vyberte možnost **Náhled**, chcete-li zobrazit náhled stránky.
1. Chcete-li vrátit šablonu se změnami, vyberte možnost **Dokončit úpravy** a volbou **Publikovat** ji publikujte.

## <a name="additional-resources"></a>Další prostředky

[Přehled knihovny modulů](starter-kit-overview.md)

[Motiv Adventure Works](adventure-works-theme.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
