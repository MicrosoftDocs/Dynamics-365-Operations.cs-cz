---
title: Modulu přihlášení k odběru
description: Tento článek se zabývá moduly přihlášení k odběru dlaždic a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/18/2022
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
ms.openlocfilehash: 23b74f5853ffb7f191ea7ee3da0d3238db339d34
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8852686"
---
# <a name="subscribe-module"></a>Modulu přihlášení k odběru

[!include [banner](includes/banner.md)]

Tento článek se zabývá moduly přihlášení k odběru dlaždic a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.

Moduly přihlášení k odběru lze na webových stránkách použít k získání informací o zákaznících pro zpravodaje nebo propagační akce.

Následující obrázek ukazuje příklad modulu přihlášení k odběru v zápatí stránky webu Adventure Works.

![Příklad modulu přihlášení k odběru v zápatí stránky webu Adventure Works](./media/Subscribe.PNG)

> [!IMPORTANT]
> - Modul přihlášení k odběru je k dispozici v knihovně modulu Commerce od verze Dynamics 365 Commerce 10.0.20.
> - Modul přihlášení k odběru je uveden v motivu Adventure Works.
> - Modul přihlášení k odběru vyžaduje rozšíření datové akce, aby fungovalo s některými poskytovateli marketingových e-mailů, aby po získání informací o zákazníkovi bylo možné zasílat informační bulletiny nebo propagační e-maily.

## <a name="subscribe-module-properties"></a>Vlastnosti modulu přihlášení k odběru

| Název vlastnosti | Hodnoty | popis |
|---------------|--------|-------------|
| Záhlaví       | Text a značka nadpisu (**H1**, **H2**, **H3**, **H4**, **H5** nebo **H6**) | Textový nadpis pro modul přihlášení k odběru, například **Přihlaste se k odběru zpravodaje** nebo **Zaregistrujte se s 10% slevou**. |
| Odstavec     | Text odstavce | Modul přihlášení k odběru podporuje text odstavce ve formátu RTF, aby v záhlaví poskytl další podrobnosti o výzvě k akci. |

## <a name="add-a-subscribe-module-to-a-new-page"></a>Přidání modulu přihlášení k odběru na novou stránku

Chcete-li přidat modul přihlášení k odběru na novou stránku a nastavit jeho požadované vlastnosti v tvůrci webů Commerce, postupujte následujícím způsobem.

1. Přejděte na **Šablony** a otevřete marketingovou šablonu pro domovskou stránku svého webu (nebo vytvořte novou marketingovou šablonu).
1. V pozici **Hlavní** na výchozí stránce vyberte tlačítko se třemi tečkami (**...**) a vyberte možnost **Přidat modul**.
1. V dialogovém okně **Vybrat moduly** vyberte modul **Odebírat** a poté klikněte na **OK**.
1. Chcete-li vrátit šablonu se změnami, vyberte možnost **Uložit**, pak **Dokončit úpravy** a volbou **Publikovat** ji publikujte.
1. Přejděte na **Stránky** a otevřete domovskou stránku webu (nebo vytvořte novou domovskou stránku pomocí marketingové šablony).
1. V pozici **Hlavní** na výchozí stránce vyberte tlačítko se třemi tečkami (**...**) a vyberte možnost **Přidat modul**.
1. V dialogovém okně **Vybrat moduly** vyberte modul **Odebírat** a poté klikněte na **OK**.
1. V podokně vlastností modulu přihlášení k odběru přidejte záhlaví, například **Přihlásit k odběru**.
1. Přidejte text odstavce, například **Nejnovější trendy, styly a propagační akce. Jste na seznamu? Přihlaste se k odběru a získejte nejnovější žhavé nabídky!**
1. Vyberte možnost **Uložit** a poté vyberte možnost **Náhled**, chcete-li zobrazit náhled stránky.
1. Chcete-li vrátit šablonu se změnami, vyberte možnost **Dokončit úpravy** a volbou **Publikovat** ji publikujte.

## <a name="additional-resources"></a>Další prostředky

[Přehled knihovny modulů](starter-kit-overview.md)

[Motiv Adventure Works](adventure-works-theme.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
