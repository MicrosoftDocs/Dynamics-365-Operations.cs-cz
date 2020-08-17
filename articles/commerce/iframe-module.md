---
title: Modul iframe
description: Tohle téma se zabývá modulem iframe a popisuje, jak jej přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 07/31/2020
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
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 0616a772a416a7c9d9756a840c93b8601c08c3d0
ms.sourcegitcommit: 078befcd7f3531073ab2c08b365bcf132d6477b0
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/31/2020
ms.locfileid: "3646881"
---
# <a name="iframe-module"></a>Modul iframe

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Tohle téma se zabývá modulem iframe a popisuje, jak jej přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Přehled

Modul iframe poskytuje prvek iframe (vložený rámec), který hostuje externí obsah na webu. Například může být použit k hostování videa YouTube nebo prohlížeče souborů PDF na jakékoli stránce webu. 

Modul iframe vyžaduje cílovou adresu URL. Poté je hostitelem obsahu cílové stránky uvnitř prvku HTML **iframe**. Externí adresy URL musí být na seznamu povolených (také známý jako „whitelist“) podle směrnic o zásadách zabezpečení obsahu webu (CSP). U obsahu prvku iframe by měly být adresy URL povoleny pomocí směrnice **frame-ancestor**. Další informace viz [Správa zásad zabezpečení obsahu (CSP)](manage-csp.md).

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

[Přehled startovací sady](starter-kit-overview.md)

[Správa zásad zabezpečení obsahu (CSP)](manage-csp.md)
