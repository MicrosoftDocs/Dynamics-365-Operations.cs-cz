---
title: Karuselový modul
description: Tohle téma se zabývá karuselovými moduly a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 04/14/2020
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
ms.openlocfilehash: f399e4c5618b65b781fdd3ec835e841614579313
ms.sourcegitcommit: 7a1d01122790b904e2d96a7ea9f1d003392358a6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/17/2020
ms.locfileid: "3269721"
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

1. Zvolte **Nová** pro vytvoření šablony stránky.
1. V dialogovém okně **Nová šablona** v části **Název šablony** zadejte **Šablona karuselu** a poté klikněte na tlačítko **OK**.
1. Do úseku **Tělo** přidejte modul **Výchozí stránka**.
1. Chcete-li vrátit šablonu se změnami, vyberte možnost **Dokončit úpravy** a volbou **Publikovat** ji publikujte.  
1. Šablonu karuselu, kterou jste právě vytvořili, použijte pro vytvoření stránky s názvem **Stránka karuselu**.
1. V úseku **Hlavní** nové stránky přidejte modul kontejneru. 
1. V podokně napravo nastavte hodnotu **šířka** na **Vyplnit obrazovku**.
1. V části **Osnova stránky** stránky přidejte do modulu kontejneru modul karuselu.
1. Přidejte modul bloku obsahu do karuselového modulu. Vlastnosti modulu bloku obsahu lze nastavit v **Záhlaví**, **Odkaz**, **Rozložení** a dalších vlastností.
1. Přidání a konfigurace jiného modulu bloku obsahu.
1. Nastavte další vlastnosti modulu karuselu podle potřeby.
1. Vyberte možnost **Uložit** a poté vyberte možnost **Náhled**, chcete-li zobrazit náhled stránky. Stránka by měla zobrazit karusel, který má dva moduly uvnitř (modul hlavního banneru a propagační modul). Chcete-li dosáhnout požadovaného účinku, můžete změnit další vlastnosti pro karuselový a propagační modul nebo modul hlavního banneru.
1. Chcete-li vrátit stránku se změnami, vyberte možnost **Dokončit úpravy** a volbou **Publikovat** ji publikujte.

## <a name="additional-resources"></a>Další prostředky

[Přehled startovací sady](starter-kit-overview.md)

[Modul propagačního banneru](add-alert.md)

[Modul textového bloku](add-content-rich-block.md)

[Modul bloku obsahu](add-hero-module.md)

[Modul videopřehrávače](add-video-player.md)
