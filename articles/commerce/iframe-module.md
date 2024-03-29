---
title: Modul Iframe
description: Tento článek se zabývá modulem iframe a popisuje, jak jej přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: 248da5132d1a2c6dcf8f246628f969c8a200b26c
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269888"
---
# <a name="iframe-module"></a>Modul Iframe

[!include [banner](includes/banner.md)]

Tento článek se zabývá modulem iframe a popisuje, jak jej přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.

Modul iframe poskytuje prvek iframe (vložený rámec), který hostuje externí obsah na webu. Například může být použit k hostování videa YouTube nebo prohlížeče souborů PDF na jakékoli stránce webu. 

Modul iframe vyžaduje cílovou adresu URL. Poté je hostitelem obsahu cílové stránky uvnitř prvku HTML **iframe**. Externí adresy URL musí být na seznamu povolených podle směrnic o zásadách zabezpečení obsahu webu (CSP). U obsahu prvku iframe by měly být adresy URL povoleny pomocí směrnice **frame-ancestor**. Další informace viz [Správa zásad zabezpečení obsahu (CSP)](manage-csp.md).

> [!NOTE]
> Modul iframe je k dispozici v Dynamics 365 Commerce vydání 10.0.13.

Následující obrázek ukazuje příklady modulů iframe, které zobrazují externí videa na stránkách webu.

![Příklad modulů iframe zobrazujících externí videa.](./media/ecommerce-iframe.PNG)

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
1. V dialogovém okně **Vytvořit novou stránku** v části **Název stránky** zadejte **Stránka marketingu** a poté vyberte **Další**.
1. V části **Vyberte šablonu** vyberte vytvořenou položku **Marketingová šablona** a poté vyberte **Další**.
1. V části **Vyberte rozložení** vyberte rozložení stránky (např. **Flexibilní rozložení**) a poté vyberte **Další**.
1. V části **Zkontrolovat a dokončit** zkontrolujte konfiguraci stránky. Pokud potřebujete upravit informace o stránce, vyberte **Zpět**. Pokud jsou informace o stránce správné, vyberte **Vytvořit stránku**. 
1. V pozici **Hlavní** na nové stránce vyberte tlačítko se třemi tečkami (**...**) a vyberte možnost **Přidat modul**.
1. V dialogovém okně **Vybrat moduly** vyberte modul **Kontejner** a poté klikněte na **OK**.
1. V podokně vlastností modulu nastavte hodnotu **Šířka** na **Vyplnit kontejner**.
1. V pozici **Kontejner** vyberte tři tečky (**...**) a poté vyberte možnost **Přidat modul**.
1. V dialogovém okně **Vybrat moduly** vyberte modul **iframe** a poté klikněte na **OK**.
1. V podokně vlastností modulu nastavte hodnotu **Cílová adresa URL** externí adresy URL videa.
1. Nastavte další vlastnosti, například **Nadpis** a **Výška**, dle potřeby.
1. Chcete-li vrátit stránku se změnami, vyberte možnost **Uložit**, pak **Dokončit úpravy** a volbou **Publikovat** ji publikujte.
1. Přejděte na marketingovou stránku svého webu. Měli byste vidět, že video je vykresleno v modulu iframe.

> [!NOTE]
> Protože modul iframe hostí externí obsah, musí autoři stránek zajistit, aby obsah hostovaný v modulu iframe neporušoval zásady omezení obsahu na příslušném trhu. Pokud dojde k porušení obsahu na stránce, která používá modul iframe, může autor webu odebrat modul iframe tak, že stránku otevře v nástroji pro tvorbu webu a vybere **Odebrat modul** ve slotu modulu iframe a poté stránku uložit a znovu publikovat.

## <a name="additional-resources"></a>Další prostředky

[Přehled knihovny modulů](starter-kit-overview.md)

[Správa zásad zabezpečení obsahu (CSP)](manage-csp.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
