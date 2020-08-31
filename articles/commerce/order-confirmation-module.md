---
title: Modul Detaily objednávky
description: Toto téma popisuje moduly pro detaily objednávek a popisuje, jak je používat v aplikaci Microsoft Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 06/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar-ms
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 5876b953a3b3d960c106acf37731fde13b93f8e7
ms.sourcegitcommit: ae0843763a8b6b232bb71db326fab28605ac6c53
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2020
ms.locfileid: "3661165"
---
# <a name="order-details-module"></a>Modul Detaily objednávky

[!include [banner](includes/banner.md)]

Toto téma popisuje moduly pro detaily objednávek a popisuje, jak je používat v aplikaci Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Přehled

Po zadání objednávky lze pomocí modulu detailů objednávky zobrazit podrobnosti o potvrzení objednávky. Zobrazuje ID potvrzení objednávky, kontaktní informace z objednávky a další podrobnosti o objednávce, jako jsou například zakoupené položky, informace o platbách a způsob expedice.

## <a name="order-details-module-properties"></a>Vlastnosti modulu podrobností objednávky

| Název vlastnosti  | Hodnoty | popis |
|----------------|--------|-------------|
| Nadpis        | Text a značka nadpisu (**H1**, **H2**, **H3**, **H4**, **H5** nebo **H6**) | V modulu podrobností objednávky může být k dispozici záhlaví. Standardně se pro značku nadpisu používá označení **H2**. Značku však lze změnit tak, aby vyhovovala požadavkům na usnadnění. |
| Kontaktní číslo | Text | Pro případ otázek souvisejících s objednávkami lze použít číslo kontaktní osoby. |

## <a name="modules-that-can-be-used-on-an-order-details-page"></a>Moduly, které lze použít na stránce potvrzení objednávky

Po vytvoření stránky s podrobnostmi objednávky můžete kromě modulu podrobností objednávky přidat další relevantní moduly. Několik příkladů:

- **Modul doporučení** – modul doporučení lze přidat na stránku detailů objednávky s cílem navrhovat ostatní produkty odběrateli.
- **Marketingové moduly** – kterýkoliv marketingový modul lze přidat na stránku podrobnosti objednávky a zobrazit tak marketingový obsah.

## <a name="add-an-order-details-module-to-a-page"></a>Přidání modulu podrobností objednávky na stránku

Chcete-li přidat modul podrobností objednávky na novou stránku a nastavit požadované vlastnosti, postupujte následujícím způsobem.

1. Přejděte na **Šablony** a poté volbou **Nová** vytvořte novou šablonu.
1. V dialogovém okně **Nová šablona** v části **Název šablony** zadejte název **šablony podrobností objednávky** a vyberte **OK**.
1. V pozici **Tělo** vyberte tři tečky (**...**) a poté vyberte možnost **Přidat modul**.
1. V dialogovém okně **Přidat modul** vyberte modul **Výchozí stránka** a poté klikněte na tlačítko **OK**.
1. V pozici **Hlavní** modulu **Výchozí stránka** vyberte tlačítko se třemi tečkami (**...**) a vyberte možnost **Přidat modul**.
1. V dialogovém okně **Přidat modul** vyberte modul **Podrobnosti objednávky** a poté klikněte na tlačítko **OK**.
1. Vyberte možnost **Uložit** a poté vyberte možnost **Náhled** k zobrazení náhledu šablony. Modul detailů objednávky nebude zobrazen, protože vyžaduje kontext pro číslo potvrzení objednávky.
1. Chcete-li vrátit šablonu se změnami, vyberte možnost **Dokončit úpravy** a volbou **Publikovat** ji publikujte.
1. Přejděte na **Stránky** a volbou **Nová** vytvořte novou stránku.
1. V dialogovém okně **Zvolte šablonu** vyberte šablonu **Šablona podrobností objednávky**. V části **Název stránky** zadejte **Stránka podrobností objednávky** a poté klikněte na tlačítko **OK**.
1. V pozici **Hlavní** modulu **Výchozí stránka** vyberte tlačítko se třemi tečkami (**...**) a vyberte možnost **Přidat modul**.
1. V dialogovém okně **Přidat modul** vyberte modul **Podrobnosti objednávky** a poté klikněte na tlačítko **OK**.
1. V podokně podrobností modulu podrobností objednávky vyberte **Nadpis** vedle symbolu tužky.
1. V poli **Text nadpisu** dialogového okna **Nadpis** zadejte text nadpisu **Podrobnosti o objednávce** a vyberte **OK**.
1. Vyberte možnost **Uložit** a poté vyberte možnost **Náhled**, chcete-li zobrazit náhled stránky.
1. Chcete-li vrátit stránku se změnami, vyberte možnost **Dokončit úpravy** a volbou **Publikovat** ji publikujte.

## <a name="additional-resources"></a>Další prostředky

[Modul košíku](add-cart-module.md)

[Modul ikony košíku](cart-icon-module.md)

[Modul pokladny](add-checkout-module.md)

[Modul platby](payment-module.md)

[Modul dodací adresy](ship-address-module.md)

[Modul možností doručení](delivery-options-module.md)

[Modul dárkového poukazu](add-giftcard.md)
