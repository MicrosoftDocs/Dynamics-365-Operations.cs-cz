---
title: Modulu přihlášení k odběru
description: Tohle téma se zabývá moduly přihlášení k odběru dlaždic a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: c9c0ed18e3d5fd2521d63f8aa5b0ea668979c57d4de738b9d51a05a1cc0b6e72
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6730916"
---
# <a name="subscribe-module"></a>Modulu přihlášení k odběru

[!include [banner](includes/banner.md)]

Tohle téma se zabývá moduly přihlášení k odběru dlaždic a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.

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
1. V dialogovém okně **Přidat modul** vyberte modul **Přihlášení k odběru** a poté klikněte na tlačítko **OK**.
1. Chcete-li vrátit šablonu se změnami, vyberte možnost **Uložit**, pak **Dokončit úpravy** a volbou **Publikovat** ji publikujte.
1. Přejděte na **Stránky** a otevřete domovskou stránku webu (nebo vytvořte novou domovskou stránku pomocí marketingové šablony).
1. V pozici **Hlavní** na výchozí stránce vyberte tlačítko se třemi tečkami (**...**) a vyberte možnost **Přidat modul**.
1. V dialogovém okně **Přidat modul** vyberte modul **Přihlášení k odběru** a poté klikněte na tlačítko **OK**.
1. V podokně vlastností modulu přihlášení k odběru přidejte záhlaví, například **Přihlásit k odběru**.
1. Přidejte text odstavce, například **Nejnovější trendy, styly a propagační akce. Jste na seznamu? Přihlaste se k odběru a získejte nejnovější žhavé nabídky!**
1. Vyberte možnost **Uložit** a poté vyberte možnost **Náhled**, chcete-li zobrazit náhled stránky.
1. Chcete-li vrátit šablonu se změnami, vyberte možnost **Dokončit úpravy** a volbou **Publikovat** ji publikujte.

## <a name="additional-resources"></a>Další prostředky

[Přehled knihovny modulů](starter-kit-overview.md)

[Motiv Adventure Works](adventure-works-theme.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
