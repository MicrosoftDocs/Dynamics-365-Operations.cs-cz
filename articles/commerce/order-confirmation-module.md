---
title: Modul potvrzení objednávky
description: Toto téma popisuje moduly pro potvrzení objednávek a popisuje, jak je použít v aplikaci Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e74ffbdfe57f9220cc9ed85edae4270409165b41
ms.sourcegitcommit: ccb39767bd3430c24f4653c26560bba2cd66553c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/19/2022
ms.locfileid: "8780377"
---
# <a name="order-confirmation-module"></a>Modul potvrzení objednávky

[!include [banner](includes/banner.md)]

Toto téma popisuje moduly pro potvrzení objednávek a popisuje, jak je použít v aplikaci Microsoft Dynamics 365 Commerce.

Po zadání objednávky lze pomocí modulu potvrzení objednávky zobrazit podrobnosti o potvrzení objednávky. Zobrazuje ID potvrzení objednávky, kontaktní informace z objednávky a další podrobnosti o objednávce, jako jsou například zakoupené položky, informace o platbách, možnosti vyzvednutí a způsob expedice.

## <a name="order-confirmation-module-properties"></a>Vlastnosti modulu potvrzení objednávky

| Název vlastnosti  | Hodnoty | Popis |
|----------------|--------|-------------|
| Záhlaví        | Text a značka nadpisu (**H1**, **H2**, **H3**, **H4**, **H5** nebo **H6**) | V modulu potvrzení objednávky může být k dispozici záhlaví. Standardně se pro značku nadpisu používá označení **H2**. Značku však lze změnit tak, aby vyhovovala požadavkům na usnadnění. |
| Kontaktní číslo | Text | Pro případ otázek souvisejících s objednávkami lze použít číslo kontaktní osoby. |
| Zobrazení informací o časovém úseku vyzvednutí | Pravda nebo nepravda | Tato vlastnost je k dispozici v aplikaci Dynamics 365 Commerce 10.0.15 a vyšší. Pokud má hodnotu pravda, zobrazí informace o časovém úseku vyzvednutí, pokud je k dispozici pro položku vyzvednutí|

## <a name="modules-that-can-be-used-on-an-order-confirmation-page"></a>Moduly, které lze použít na stránce potvrzení objednávky

Po vytvoření stránky potvrzení objednávky můžete kromě modulu potvrzení objednávky přidat další relevantní moduly. Několik příkladů:

- **Modul doporučení** – modul doporučení lze přidat na stránku potvrzení objednávky s cílem navrhovat ostatní produkty odběrateli.
- **Marketingové moduly** – kterýkoliv marketingový modul lze přidat na stránku potvrzení objednávky a zobrazit tak marketingový obsah.

## <a name="add-an-order-confirmation-module-to-a-page"></a>Přidání modulu potvrzení objednávky na stránku

Chcete-li přidat modul potvrzení objednávky na novou stránku a nastavit požadované vlastnosti, postupujte následujícím způsobem.

1. Přejděte na **Šablony** a poté volbou **Nová** vytvořte novou šablonu.
1. V dialogovém okně **Nová šablona** v části **Název šablony** zadejte název **šablony potvrzení objednávky** a vyberte **OK**.
1. V pozici **Tělo** vyberte tři tečky (**...**) a poté vyberte možnost **Přidat modul**.
1. V dialogovém okně **Vyberte moduly** vyberte modul **Výchozí stránka** a poté klikněte na tlačítko **OK**.
1. V pozici **Hlavní** modulu **Výchozí stránka** vyberte tlačítko se třemi tečkami (**...**) a vyberte možnost **Přidat modul**.
1. V dialogovém okně **Vyberte moduly** vyberte modul **Potvrzení objednávky** a poté klikněte na tlačítko **OK**.
1. Vyberte možnost **Uložit** a poté vyberte možnost **Náhled** k zobrazení náhledu šablony. Modul potvrzení objednávky nebude zobrazen, protože vyžaduje kontext pro číslo potvrzení objednávky.
1. Chcete-li vrátit šablonu se změnami, vyberte možnost **Dokončit úpravy** a volbou **Publikovat** ji publikujte.
1. Přejděte na **Stránky** a volbou **Nová** vytvořte novou stránku.
1. V dialogovém okně **Vytvořit novou stránku** v části **Název stránky** zadejte **Stránka potvrzení objednávky** a poté vyberte **Další**.
1. V části **Vyberte šablonu** vyberte vytvořenou položku **Šablona potvrzení objednávky** a poté vyberte **Další**.
1. V části **Vyberte rozložení** vyberte rozložení stránky (např. **Flexibilní rozložení**) a poté vyberte **Další**.
1. V části **Zkontrolovat a dokončit** zkontrolujte konfiguraci stránky. Pokud potřebujete upravit informace o stránce, vyberte **Zpět**. Pokud jsou informace o stránce správné, vyberte **Vytvořit stránku**. 
1. V pozici **Hlavní** modulu **Výchozí stránka** vyberte tlačítko se třemi tečkami (**...**) a vyberte možnost **Přidat modul**.
1. V dialogovém okně **Vyberte moduly** vyberte modul **Potvrzení objednávky** a poté klikněte na tlačítko **OK**.
1. V podokně podrobností modulu potvrzení objednávky vyberte **Nadpis** vedle symbolu tužky.
1. V poli **Text nadpisu** dialogového okna **Nadpis** zadejte text nadpisu **Potvrzení objednávky** a vyberte **OK**.
1. Vyberte možnost **Uložit** a poté vyberte možnost **Náhled**, chcete-li zobrazit náhled stránky.
1. Chcete-li vrátit stránku se změnami, vyberte možnost **Dokončit úpravy** a volbou **Publikovat** ji publikujte.

## <a name="additional-resources"></a>Další prostředky

[Modul košíku](add-cart-module.md)

[Modul ikony košíku](cart-icon-module.md)

[Modul pokladny](add-checkout-module.md)

[Platební modul](payment-module.md)

[Modul dodací adresy](ship-address-module.md)

[Modul možností doručení](delivery-options-module.md)

[Modul s informacemi o vyzvednutí](pickup-info-module.md)

[Modul dárkového poukazu](add-giftcard.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
