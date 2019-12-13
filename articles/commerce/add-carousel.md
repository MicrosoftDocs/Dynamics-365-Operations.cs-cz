---
title: Karuselový modul
description: Tohle téma se zabývá karuselovými moduly a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: c2c5adc8ab2e0330f7b07e5153fd8332ab0203e5
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785230"
---
# <a name="carousel-module"></a>Karuselový modul

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Tohle téma se zabývá karuselovými moduly a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Přehled

Karuselový modul slouží k umístění propagačních položek do karuselu, který mohou zákazníci procházet. Je to speciální modul kontejneru, který hostuje jiné moduly. Maloobchodní prodejce může například pomocí karuselového modulu na domovské stránce prezentovat nové produkty nebo propagační akce.

Do karuselového modulu můžete přidat modul hlavního banneru nebo propagační modul. Vlastnosti karuselového modulu pak definují způsob, jakým jsou tyto moduly vykreslovány.

## <a name="examples-of-carousel-modules-in-e-commerce"></a>Příklady karuselových modulů v elektronickém obchodu

- Na domovské stránce lze použít karusel s více propagačními moduly.
- Na stránce s podrobnostmi o produktu lze použít karusel s více propagačními moduly.
- Karusel lze použít na libovolné marketingové stránce k propagaci promoakcí a produktů.

## <a name="carousel-module-properties"></a>Vlastnosti karuselového modulu

| Název vlastnosti             | Hodnota                                | Popis |
|---------------------------|--------------------------------------|-------------|
| Přehrát automaticky                  | **Pravda** nebo **nepravda**                | Je- li nastavena hodnota **Pravda**, dojde k automatickému přechodu mezi položkami v karuselu. Pokud je hodnota nastavena na **Nepravda**, nedochází k žádnému přechodu, pokud zákazník nepoužije klávesnici nebo myš k přechodu z jedné položky na další položku. |
| Interval přechodu snímků | Hodnota v sekundách                   | Interval pro přechody mezi položkami. |
| Animace přechodu      | **Posunutí** nebo **Slábnutí**                | Efekt při přechodu. |
| Šířka                     | **Přizpůsobit kontejneru** nebo **Vyplnit obrazovku** | Je-li hodnota nastavena na **Přizpůsobit kontejneru**, budou položky uvnitř karuselu omezeny na šířku karuselu. Je-li hodnota nastavena na **Vyplnit obrazovku**, položky nejsou omezeny na šířku karuselu, ale mohou přejít do režimu celé obrazovky. Chcete-li dosáhnout požadovaného rozvržení, můžete změnit tuto hodnotu. |

## <a name="add-a-carousel-module-to-a-page"></a>Přidání karuselového modulu na stránku

Chcete-li přidat karuselový modul na novou stránku a nastavit požadované vlastnosti, postupujte následujícím způsobem.

1. Vytvořte šablonu stránky s názvem **Šablona karuselu**.
1. V pozici **Hlavní** na výchozí stránce přidejte karuselový modul.
1. Přidejte modul hlavního banneru do karuselového modulu.
1. Přidejte propagační modul do karuselového modulu.
1. Vraťte šablonu se změnami a publikujte ji. 
1. Šablonu karuselu, kterou jste právě vytvořili, použijte pro vytvoření stránky s názvem **Stránka karuselu**.
1. V úseku **Hlavní** nové stránky přidejte karuselový modul.
1. Nastavte vlastnost **Šířka** karuselového modulu na **Vyplnit obrazovku**. 
1. Nastavte vlastnost **Animace přechodu** na **Posunutí**.
1. Přidejte modul hlavního banneru do karuselového modulu.
1. V modulu hlavního banneru přidejte obrázek a nadpis a pak vyberte možnost **Uložit**.
1. Přidejte propagační modul do karuselového modulu.
1. V propagačním modulu přidejte obrázek, nadpis a odstavec textu.
1. Uložte stránku a zobrazte náhled. Stránka by měla zobrazit karusel, který má dva moduly uvnitř (modul hlavního banneru a propagační modul). Chcete-li dosáhnout požadovaného účinku, můžete změnit další vlastnosti pro karuselový a propagační modul nebo modul hlavního banneru.
1. Vraťte stránku se změnami a publikujte ji.

## <a name="additional-resources"></a>Další zdroje

[Přehled startovací sady](starter-kit-overview.md)

[Modul výstrahy](add-alert.md)

[Modul bloku s formátovaným obsahem](add-content-rich-block.md)

[Modul umístění obsahu](add-content-placement-modules.md)

[Propagační modul](add-feature-module.md)

[Modul hlavního banneru](add-hero-module.md)

[Modul přehrávače videa](add-video-player.md)
