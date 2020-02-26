---
title: Modul Detaily objednávky
description: Toto téma popisuje moduly pro detaily objednávek a popisuje, jak je používat v aplikaci Microsoft Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 01/23/2020
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
ms.openlocfilehash: cb09a0b6ce1e48707f96021e9fad0006d9c1c55c
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/05/2020
ms.locfileid: "3026010"
---
# <a name="order-details-module"></a>Modul Detaily objednávky


[!include [banner](includes/banner.md)]

Toto téma popisuje moduly pro detaily objednávek a popisuje, jak je používat v aplikaci Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Přehled

Po zadání objednávky lze pomocí modulu detailů objednávky zobrazit podrobnosti o potvrzení objednávky. Zobrazuje ID potvrzení objednávky, kontaktní informace z objednávky a další podrobnosti o objednávce, jako jsou například zakoupené položky, informace o platbách a způsob expedice.

## <a name="order-confirmation-module-properties"></a>Vlastnosti modulu potvrzení objednávky

| Název vlastnosti  | Hodnoty | Popis |
|----------------|--------|-------------|
| Záhlaví        | Text a značka nadpisu (**H1**, **H2**, **H3**, **H4**, **H5** nebo **H6**) | V modulu potvrzení objednávky může být k dispozici záhlaví. Standardně se pro značku nadpisu používá označení **H2**. Značku však lze změnit tak, aby vyhovovala požadavkům na usnadnění. |
| Kontaktní číslo | Text | Pro případ otázek souvisejících s objednávkami lze použít číslo kontaktní osoby. |

## <a name="modules-that-can-be-used-on-an-order-details-page"></a>Moduly, které lze použít na stránce potvrzení objednávky

Po vytvoření stránky s podrobnostmi objednávky můžete kromě modulu podrobností objednávky přidat další relevantní moduly. Několik příkladů:

- **Modul doporučení** – modul doporučení lze přidat na stránku detailů objednávky s cílem navrhovat ostatní produkty odběrateli.
- **Marketingové moduly** – kterýkoliv marketingový modul lze přidat na stránku podrobnosti objednávky a zobrazit tak marketingový obsah.

## <a name="create-an-order-details-page-module"></a>Vytvoření modulu stránky detailů objednávky

1. Vytvořte šablonu stránky s názvem **Šablona Detaily objednávky**.
1. V úseku **Hlavní** výchozí stránky přidejte modul detailů objednávky.
1. V modulu detailů objednávky přidejte modul doporučení.
1. Uložení a náhled šablony. Modul detailů objednávky nebude zobrazen, protože vyžaduje kontext pro číslo potvrzení objednávky.
1. Dokončete úpravy šablony a publikujte ji.
1. Šablonu detailů objednávky, kterou jste právě vytvořili, použijte pro vytvoření stránky s názvem **stránka detailů objednávky**.
1. Přidejte výchozí stránku do osnovy stránky.
1. V oblasti **Záhlaví** přidejte fragment záhlaví.
1. V oblasti **Zápatí** přidejte fragment zápatí.
1. V úseku **Hlavní** přidejte modul detailů objednávky.
1. V podokně vlastností modulu detailů objednávky přidejte záhlaví **Detaily objednávky**.
1. Pod modulem detailů objednávky přidejte modul doporučení a nakonfigurujte jej tak, aby používal nastavení **Nové** a **Nejlépe prodávané**.
1. Uložte stránku a zobrazte náhled.
1. Dokončete úpravy stránky a publikujte ji.

## <a name="additional-resources"></a>Další zdroje

[Přehled startovací sady](starter-kit-overview.md)

[Modul kontejneru](add-container-module.md)

[Modul buy boxu](add-buy-box.md)

[Modul košíku](add-cart-module.md)

[Modul pokladny](add-checkout-module.md)

[Modul záhlaví](author-header-module.md)

[Modul zápatí](author-footer-module.md)
