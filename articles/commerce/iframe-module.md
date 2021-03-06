---
title: Modul iframe
description: Tohle téma se zabývá modulem iframe a popisuje, jak jej přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 09/15/2020
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
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 7b397b91d1b8a45347ef2d05f42fb7c610ab3912
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797063"
---
# <a name="iframe-module"></a>Modul iFrame

[!include [banner](includes/banner.md)]

Tohle téma se zabývá modulem iframe a popisuje, jak jej přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.

Modul iframe poskytuje prvek iframe (vložený rámec), který hostuje externí obsah na webu. Například může být použit k hostování videa YouTube nebo prohlížeče souborů PDF na jakékoli stránce webu. 

Modul iframe vyžaduje cílovou adresu URL. Poté je hostitelem obsahu cílové stránky uvnitř prvku HTML **iframe**. Externí adresy URL musí být na seznamu povolených podle směrnic o zásadách zabezpečení obsahu webu (CSP). U obsahu prvku iframe by měly být adresy URL povoleny pomocí směrnice **frame-ancestor**. Další informace viz [Správa zásad zabezpečení obsahu (CSP)](manage-csp.md).

> [!NOTE]
> Modul iframe je k dispozici v Dynamics 365 Commerce vydání 10.0.13.

Následující obrázek ukazuje příklady modulů iframe, které zobrazují externí videa na stránkách webu.

![Příklad modulů iframe zobrazujících externí videa](./media/ecommerce-iframe.PNG)

## <a name="iframe-module-properties"></a>Vlastnosti modulu iframe

| Název vlastnosti             | Hodnota                 | popis |
|---------------------------|-----------------------|-------------|
| Nadpis | Text | Nadpis modulu. |
| Cílová adresa URL | Adresa URL | Adresa URL, která je hostována v modulu. |
| Výška | Počet nebo procento | Výška modulu v pixelech nebo v procentech. Například hodnota **100** bude považována za počet pixelů a hodnota **100%** bude považována za procento. |
| Popisek aria | Text | Pro účely usnadnění přístupu lze definovat označení přístupných aplikací Rich Internet Applications (ARIA). |

## <a name="add-an-iframe-module-to-a-page"></a>Přidání modulu iframe na stránku

Chcete-li na stránku přidat modul iframe a zobrazit externí video, postupujte takto.

1. Přejděte na **Šablony** a poté volbou **Nová** vytvořte novou šablonu.
1. V dialogovém okně **Nová šablona** v části **Název šablony** zadejte **Šablona marketingu** a poté klikněte na tlačítko **OK**.
1. Chcete-li vrátit šablonu se změnami, vyberte možnost **Uložit**, pak **Dokončit úpravy** a volbou **Publikovat** ji publikujte.
1. Přejděte na **Stránky** a volbou **Nová** vytvořte novou stránku.
1. V dialogovém okně **Zvolte šablonu** vyberte šablonu **Šablona marketingu**. V části **Název stránky** zadejte **Stránka marketingu** a poté klikněte na tlačítko **OK**.
1. V pozici **Hlavní** na nové stránce vyberte tlačítko se třemi tečkami (**...**) a vyberte možnost **Přidat modul**.
1. V dialogovém okně **Přidat modul** vyberte modul **Kontejner** a poté klikněte na tlačítko **OK**.
1. V podokně vlastností modulu nastavte hodnotu **Šířka** na **Vyplnit kontejner**.
1. V pozici **Kontejner** vyberte tři tečky (**...**) a poté vyberte možnost **Přidat modul**.
1. V dialogovém okně **Přidat modul** vyberte modul **iframe** a poté klikněte na tlačítko **OK**.
1. V podokně vlastností modulu nastavte hodnotu **Cílová adresa URL** externí adresy URL videa.
1. Nastavte další vlastnosti, například **Nadpis** a **Výška**, dle potřeby.
1. Chcete-li vrátit stránku se změnami, vyberte možnost **Uložit**, pak **Dokončit úpravy** a volbou **Publikovat** ji publikujte.
1. Přejděte na marketingovou stránku svého webu. Měli byste vidět, že video je vykresleno v modulu iframe.
 
## <a name="additional-resources"></a>Další prostředky

[Přehled knihovny modulů](starter-kit-overview.md)

[Správa zásad zabezpečení obsahu (CSP)](manage-csp.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]