---
title: Modul potvrzení objednávky
description: Toto téma popisuje moduly pro potvrzení objednávek a popisuje, jak je vytvořit v aplikaci Microsoft Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: e339ce02bb646d0d9a68c22b24fde9b72071de6f
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/01/2019
ms.locfileid: "2698319"
---
# <a name="order-confirmation-module"></a>Modul potvrzení objednávky

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Toto téma popisuje moduly pro potvrzení objednávek a popisuje, jak je vytvořit v aplikaci Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Přehled

Modul potvrzení objednávky slouží k zobrazení potvrzovací zprávy na stránce potvrzení objednávky poté, co byla objednávka vystavena. V modulu potvrzení objednávky je zobrazeno číslo potvrzení objednávky a e-mailová adresa odběratele, která byla poskytnuta během rezervace.

Při zadání objednávky v průběhu rezervace je číslo potvrzení objednávky a e-mailová adresa odběratele předána na stránku potvrzení objednávky jako řetězec dotazu v adrese URL stránky. Modul potvrzení objednávky tyto informace obdrží a uvede stav objednávky na stránce potvrzení objednávky. Modul potvrzení objednávky vyžaduje, aby tento kontext stránky poskytoval stav objednávky.

## <a name="order-confirmation-module-properties"></a>Vlastnosti modulu potvrzení objednávky

| Název vlastnosti | Hodnoty | Popis |
|---------------|--------|-------------|
| Záhlaví       | Text a značka nadpisu (**H1**, **H2**, **H3**, **H4**, **H5** nebo **H6**) | V modulu potvrzení objednávky může být k dispozici záhlaví. Standardně se pro značku nadpisu používá označení **H2**. Značku však lze změnit tak, aby vyhovovala požadavkům na usnadnění. |

## <a name="modules-that-can-be-used-in-an-order-confirmation-page-module"></a>Moduly, které lze použít v modulu stránky potvrzení objednávky 

- **Doporučení** – modul doporučení může být uveden na stránce potvrzení objednávky s cílem navrhovat ostatní produkty odběrateli.
- **Marketing** – modul marketingu může přidat marketingový obsah na stránku pro potvrzení objednávky.

## <a name="create-an-order-confirmation-page-module"></a>Přidání modulu stránky potvrzení objednávky

1. Vytvořte šablonu stránky s názvem **Šablona potvrzení objednávky**.
1. V úseku **Hlavní** výchozí stránky přidejte modul potvrzení objednávky.
1. V modulu potvrzení objednávky přidejte modul doporučení.
1. Uložení a náhled šablony. Modul potvrzení objednávky by neměl být zobrazen, protože vyžaduje kontext pro číslo potvrzení objednávky.
1. Vraťte šablonu se změnami a publikujte ji.
1. Šablonu potvrzení objednávky, kterou jste právě vytvořili, použijte pro vytvoření stránky s názvem **stránka potvrzení objednávky**.
1. Přidejte výchozí stránku do osnovy stránky.
1. V oblasti **Záhlaví** přidejte fragment záhlaví.
1. V oblasti **Zápatí** přidejte fragment zápatí.
1. V úseku **Hlavní** přidejte modul potvrzení objednávky.
1. V podokně vlastností modulu potvrzení objednávky přidejte **Potvrzení objednávky**pro záhlaví.
1. Pod modulem potvrzení objednávky přidejte modul doporučení a nakonfigurujte jej tak, aby používal nastavení **Nové** a **Nejlépe prodávané**.
1. Uložte a zobrazte náhled stránky, zarezervujte ji a publikujte ji.

## <a name="additional-resources"></a>Další zdroje

[Přehled startovací sady](starter-kit-overview.md)

[Modul kontejneru](add-container-module.md)

[Modul buy boxu](add-buy-box.md)

[Modul košíku](add-cart-module.md)

[Modul pokladny](add-checkout-module.md)

[Modul záhlaví](author-header-module.md)

[Modul zápatí](author-footer-module.md)
