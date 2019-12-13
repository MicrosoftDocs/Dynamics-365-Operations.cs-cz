---
title: Modul výstrahy
description: Tohle téma se zabývá moduly výstrahy a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
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
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 82138dd7f0934f732215f67a3726638eb87075d4
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785345"
---
# <a name="alert-module"></a>Modul výstrahy

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Tohle téma se zabývá moduly výstrahy a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Přehled

Modul výstrahy slouží k zobrazení vložených informačních zpráv na stránce. Moduly výstrah podporují textové zprávy a odkazy. Lze je použít k zobrazení promoakcí v rámci celého webu, které se zobrazí na všech stránkách webu elektronického obchodu. 

Moduly výstrah jsou řízeny daty ze systému správy obsahu (CMS) a lze je umístit na libovolnou stránku.

## <a name="examples-of-alert-modules-in-e-commerce"></a>Příklady modulů výstrah v elektronickém obchodu

Moduly výstrah lze použít v záhlaví webu, kde označují promoakce nebo zprávy na úrovni celého webu. Několik příkladů:

„Výroční výprodej končí za 10 dnů“

„Ušetřete v předškolním výprodeji. Pusťte se do nakupování.“

## <a name="alert-module-properties"></a>Vlastnosti modulu výstrahy

| Název vlastnosti  | Hodnota                              | Popis |
|----------------|------------------------------------|-------------|
| Text           | Text                               | Textová zpráva, která se zobrazí v modulu výstrahy. |
| Zarovnání textu | **Vpravo**, **vlevo** nebo **uprostřed** | Hodnota definující zarovnání textu v modulu výstrahy. |
| Zamítnout výstrahu  | **Pravda** nebo **nepravda**              | Je-li tato hodnota nastavena na hodnotu **pravda**, zákazník může výstrahu zavřít. |
| Připojení           | Adresa URL                                | Adresa URL pro volitelný odkaz. |

## <a name="add-an-alert-module-to-a-page"></a>Přidání modulu výstrahy na stránku 

Chcete-li přidat modul výstrahy na stránku a nastavit požadované vlastnosti, postupujte následujícím způsobem.

1. Vytvořte šablonu stránky s názvem **Šablona výstrahy**.
1. V pozici **Hlavní** na výchozí stránce přidejte modul výstrahy.
1. Vraťte šablonu se změnami a publikujte ji. 
1. Šablonu výstrahy, kterou jste právě vytvořili, použijte pro vytvoření stránky s názvem **Stránka výstrahy**. 
1. V pozici **Hlavní** nové stránky přidejte modul výstrahy.
1. V nastavení modulu výstrahy zadejte text výstrahy. Chcete-li dále upravit modul výstrahy, můžete upravit ostatní vlastnosti.
1. Uložte stránku a zobrazte náhled. V horní části stránky by se měla zobrazit výstraha obsahující text, který jste přidali.
1. Vraťte stránku se změnami a publikujte ji. 

## <a name="additional-resources"></a>Další zdroje

[Přehled startovací sady](starter-kit-overview.md)

[Karuselový modul](add-carousel.md)

[Modul bloku s formátovaným obsahem](add-content-rich-block.md)

[Modul umístění obsahu](add-content-placement-modules.md)

[Propagační modul](add-feature-module.md)

[Modul hlavního banneru ](add-hero-module.md)

[Modul přehrávače videa](add-video-player.md)
