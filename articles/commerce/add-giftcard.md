---
title: Modul dárkového poukazu
description: Tohle téma se zabývá moduly dárkového poukazu a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 09/15/2020
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
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: a4e4e06ab7032d68fcd36a8e80bc714ebaaac821
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797664"
---
# <a name="gift-card-module"></a>Modul dárkového poukazu

[!include [banner](includes/banner.md)]

Tohle téma se zabývá moduly dárkového poukazu a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.

Moduly dárkových poukazů lze použít v modulech pokladny pro příjem dárkových poukazů, což je běžná forma platby používaná při transakcích elektronického obchodování. Modul dárkových poukazů podporuje dárkové poukazy pro Dynamics 365, SVS a Givex. SVS a Givex dárkové poukazy jsou uplatněny prostřednictvím poskytovatele plateb Adyen. Další informace o podpoře externích dárkových poukazů, jako jsou například SVS a Givex, naleznete v tématu [Podpora externích dárkových poukazů](./dev-itpro/gift-card.md).

> [!NOTE]
> Podpora pro uplatnění dárkových karet SVS a Givex během procesu placení je k dispozici ve vydání Dynamics 365 Commerce 10.0.11. 

K dispozici jsou dva moduly dárkových poukazů:

- **Dárkový poukaz** – Tento modul lze použít na stránce pokladny k uplatnění dárkového poukazu jako úhrady. 
- **Kontrola zůstatku dárkového poukazu** – Tento modul lze použít na kterékoli stránce ke kontrole zůstatku dárkového poukazu. Tento modul je k dispozici v aplikaci Commerce verze 10.0.14 a novější.

> [!NOTE]
> Podpora modulu kontroly zůstatku dárkové karty je k dispozici ve vydání Dynamics 365 Commerce 10.0.14.

Následující obrázek znázorňuje příklad modulu dárkového poukazu na stránce pokladny.

![Příklad modulu dárkového poukazu](./media/ecommerce-giftcard.PNG)

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

> [!IMPORTANT]
> Tato nastavení jsou k dispozici ve vydání Dynamics 365 Commerce 10.0.11 a jsou vyžadována, pouze pokud potřebujete podporu pro dárkové karty SVS nebo Givex. Pokud provádíte aktualizaci ze starší verze Dynamics 365 Commerce, musíte ručně aktualizovat soubor appsettings.json. Pokyny k aktualizaci souboru appsettings.json najdete v části [Aktualizace SDK a knihoven modulů](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file). 

## <a name="add-a-gift-card-module-to-a-page"></a>Přidání modulu dárkového poukazu na stránku

Pokyny k přidání modulu dárkového poukazu na stránku pokladny a nastavení požadovaných vlastností naleznete v tématu [Modul pokladny](add-checkout-module.md).

## <a name="additional-resources"></a>Další prostředky

[Modul košíku](add-cart-module.md)

[Modul ikony košíku](cart-icon-module.md)

[Modul pokladny](add-checkout-module.md)

[Platební modul](payment-module.md)

[Modul dodací adresy](ship-address-module.md)

[Modul možností doručení](delivery-options-module.md)

[Modul s informacemi o vyzvednutí](pickup-info-module.md)

[Modul podrobností objednávky](order-confirmation-module.md)

[Podpora pro externí dárkové poukazy](./dev-itpro/gift-card.md)

[SDK a aktualizace knihovny modulů](e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]