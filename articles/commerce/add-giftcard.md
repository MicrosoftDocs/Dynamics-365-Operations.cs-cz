---
title: Modul dárkového poukazu
description: Tohle téma se zabývá moduly dárkového poukazu a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 04/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 70047376cec44523cc9cfe4df792bde23c776d8c
ms.sourcegitcommit: ac966ea3a6c557fb5f9634b187b0e788d3e82d4d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/14/2020
ms.locfileid: "3261557"
---
# <a name="gift-card-module"></a>Modul dárkového poukazu

[!include [banner](includes/banner.md)]

Tohle téma se zabývá moduly dárkového poukazu a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Přehled

Dárkové poukazy jsou běžnou formou plateb a modul dárkových poukazů lze použít v modulu pokladny pro příjem dárkových poukazů. Modul dárkových poukazů podporuje dárkové poukazy pro Dynamics 365, SVS a Givex. SVS a Givex dárkové poukazy jsou uplatněny prostřednictvím poskytovatele plateb Adyen.

Další informace o podpoře externích dárkových poukazů, jako jsou například SVS a Givex, naleznete v tématu [Podpora externích dárkových poukazů](./dev-itpro/gift-card.md)

## <a name="module-properties"></a>Vlastnosti modulu

- **Zobrazit další pole** – Tato vlastnost určuje, která pole mají být zobrazena pro dárkové poukazy kromě čísla dárkového poukazu, který je ve výchozím nastavení vždy zobrazen. Některé dárkové poukazy například podporují zobrazení osobního identifikačního čísla (PIN) a další podporují zobrazování kódu PIN a data vypršení platnosti. Druhou možností může být nastavení této vlastnosti na "none", která by zobrazila pouze číslo dárkového poukazu a žádná další pole.

Podporované hodnoty:
-   PIN
-   Datum konce platnosti
-   PIN a datum konce platnosti 
-   Žádní

## <a name="site-settings-for-gift-card-modules"></a>Nastavení webu pro moduly dárkových poukazů

V konfigurátoru webů Commerce v **Nastavení webu \> Rozšíření** existuje nastavení modulu dárkového poukazu s názvem **Podporovaný typ dárkového poukazu**. Toto nastavení podporuje tři hodnoty:
- **Dárkový pouikaz Dynamics 365** - je-li použito toto nastavení, modul dárkového poukazu umožňuje pouze dárkové poukazy aplikace Dynamics 365. Toto nastavení je podporováno pouze pro přihlášené uživatele na webu e-Commerce.
- **Dárkové poukazy SVS a Givex** - je-li použito toto nastavení, modul dárkového poukazu umožňuje pouze dárkové poukazy SVS a Givex. Toto nastavení je podporováno pro přihlášené i anonymní uživatele na webu e-Commerce.
- **Dárkové poukazy Dynamics 365, SVS a Givex** - je-li použito toto nastavení, modul dárkového poukazu umožňuje dárkové poukazy Dynamics 365, SVS a Givex. Toto nastavení je podporováno pouze pro přihlášené uživatele na webu e-Commerce.

## <a name="add-a-gift-card-module-to-a-page"></a>Přidání modulu dárkového poukazu na stránku

Pokyny k přidání modulu dárkového poukazu na stránku pokladny a nastavení požadovaných vlastností naleznete v tématu [Modul pokladny](add-checkout-module.md).

## <a name="additional-resources"></a>Další prostředky

[Přehled startovací sady](starter-kit-overview.md)

[Modul pokladny](add-checkout-module.md)

[Podpora pro externí dárkové poukazy](./dev-itpro/gift-card.md)
