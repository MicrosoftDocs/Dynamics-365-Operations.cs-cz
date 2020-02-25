---
title: Karuselový modul
description: Tohle téma se zabývá karuselovými moduly a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
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
ms.openlocfilehash: f279d7db0a92df9e64b1d3f6ca01c65ca1478d79
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025774"
---
# <a name="carousel-module"></a>Karuselový modul


[!include [banner](includes/banner.md)]

Tohle téma se zabývá karuselovými moduly a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Přehled

Karuselový modul slouží k umístění propagačních položek do rotujícího banneru karuselu (včetně formátovaných obrázků), který mohou zákazníci procházet. Maloobchodní prodejce může například pomocí karuselového modulu na domovské stránce prezentovat nové produkty nebo propagační akce.

Do karuselového modulu můžete přidat modul bloku obsahu. Vlastnosti karuselového modulu pak definují způsob, jakým jsou tyto moduly vykreslovány.

## <a name="examples-of-carousel-modules-in-e-commerce"></a>Příklady karuselových modulů v elektronickém obchodu

- Na domovské stránce lze použít karusel s více propagačními moduly.
- Na stránce s podrobnostmi o produktu lze použít karusel s více propagačními moduly.
- Karusel lze použít na libovolné marketingové stránce k propagaci promoakcí a produktů.

## <a name="carousel-module-properties"></a>Vlastnosti karuselového modulu

| Název vlastnosti             | Hodnota                 | Popis |
|---------------------------|-----------------------|-------------|
| Přehrát automaticky                  | **Pravda** nebo **nepravda** | Je- li nastavena hodnota **Pravda**, dojde k automatickému přechodu mezi položkami v karuselu. Pokud je hodnota nastavena na **Nepravda**, nedochází k žádnému přechodu, pokud zákazník nepoužije klávesnici nebo myš k přechodu z jedné položky na další položku. |
| Interval přechodu snímků | Hodnota v sekundách    | Interval pro přechody mezi položkami. |
| Typ přechodu           | **Posunutí** nebo **Slábnutí** | Přechodový efekt mezi položkami. |
| Skrýt karuselové překlopení     | **Pravda** nebo **nepravda** | Je-li nastavena na **true**, bude páka karuselu a indikátor pořadí skrytý. |
| Povolit zrušení karuselu    | **Pravda** nebo **nepravda** | Je-li tato hodnota nastavena na hodnotu **pravda**, uživatelé mohou karusel zrušit. |

## <a name="add-a-carousel-module-to-a-page"></a>Přidání karuselového modulu na stránku

Chcete-li přidat karuselový modul na novou stránku a nastavit požadované vlastnosti, postupujte následujícím způsobem.

1. Vytvořte šablonu stránky s názvem **Šablona karuselu**.
1. Do úseku **Tělo** přidejte modul **Výchozí stránka**.
1. Vraťte šablonu se změnami a publikujte ji. 
1. Šablonu karuselu, kterou jste právě vytvořili, použijte pro vytvoření stránky s názvem **Stránka karuselu**.
1. V úseku **Hlavní** nové stránky přidejte modul kontejneru. 
1. V podokně napravo nastavte hodnotu **šířka** na **Vyplnit obrazovku**.
1. V části **Osnova stránky** stránky přidejte do modulu kontejneru modul karuselu.
1. Přidejte modul bloku obsahu do karuselového modulu. Vlastnosti modulu bloku obsahu lze nastavit v **Záhlaví**, **Odkaz**, **Rozložení** a dalších vlastností.
1. Přidání a konfigurace jiného modulu bloku obsahu.
1. Nastavte další vlastnosti modulu karuselu podle potřeby.
1. Uložte stránku a zobrazte náhled. Stránka by měla zobrazit karusel, který má dva moduly uvnitř (modul hlavního banneru a propagační modul). Chcete-li dosáhnout požadovaného účinku, můžete změnit další vlastnosti pro karuselový a propagační modul nebo modul hlavního banneru.
1. Dokončete úpravy stránky a publikujte ji.

## <a name="additional-resources"></a>Další zdroje

[Přehled startovací sady](starter-kit-overview.md)

[Modul propagačního banneru](add-alert.md)

[Modul textového bloku](add-content-rich-block.md)

[Modul bloku obsahu](add-hero-module.md)

[Modul videopřehrávače](add-video-player.md)
