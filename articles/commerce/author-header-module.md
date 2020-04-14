---
title: Modul záhlaví
description: Toto téma popisuje moduly záhlaví a popisuje, jak vytvořit moduly záhlaví v řešení Microsoft Dynamics 365 Commerce.
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
ms.dyn365.ops.version: ''
ms.openlocfilehash: efadd19681bbb21ea5b2b469e55bc6f4b0535046
ms.sourcegitcommit: 34e543e807ac8790597f522fe3b4f0266cf4ee56
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/24/2020
ms.locfileid: "3025645"
---
# <a name="header-module"></a>Modul záhlaví


[!include [banner](includes/banner.md)]

Toto téma popisuje moduly záhlaví a popisuje, jak vytvořit moduly záhlaví v řešení Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Přehled

V aplikaci Dynamics 365 Commerce se záhlaví stránky skládá z několika modulů, jako je například záhlaví, navigační nabídka, hledání, reklamní banner a moduly souhlasu se soubory cookie. 

Modul záhlaví obsahuje logo webu, odkazy na navigační hierarchii, odkazy na další stránky na webu, symbol košíku, symbol požadovaných položek, přihlašovací možnosti a vyhledávací panel. Modul záhlaví je automaticky optimalizován pro zařízení, na kterém je stránka prohlížena (jinými slovy desktopové nebo mobilní zařízení). Například v mobilním zařízení je navigační panel sbalen do tlačítka **Nabídka** (což je někdy nazýváno *hamburgerová nabídka*).

## <a name="properties-of-a-header-module"></a>Vlastnosti modulu záhlaví

Modul záhlaví podporuje vlastnosti **Obrázek loga**, **Odkaz na logo** a **Odkazy na můj účet**. 

Vlastnosti **Obrázek loga** a **Odkaz na logo** se používají k definování loga na stránce. Další informace naleznete v tématu [Přidat logo](add-logo.md). 

Vlastnost **Odkazy na můj účet** lze použít k definování stránek účtů, pro které chce vlastník webu zobrazit v záhlaví rychlé odkazy.

## <a name="modules-that-are-available-in-a-header-module"></a>Moduly, které jsou k dispozici v modulu záhlaví

Následující moduly lze použít v modulu záhlaví:

- **Navigační nabídka** – Navigační nabídka představuje hierarchii navigace kanálu a další statické navigační odkazy. Hierarchii navigace kanálu lze nakonfigurovat v aplikaci Dynamics 365 Commerce. Navigační nabídka obsahuje vlastnost **Zdroj navigace**, která se používá k určení položek navigační nabídky serveru Retail a statických položek nabídky jako zdroje. Jsou-li statické položky nabídky určeny jako zdroj, lze poskytnout relativní odkazy na jiné stránky na webu. Konfigurované položky jsou pak zobrazeny jako navigace v záhlaví. 
- **Vyhledávání** – Vyhledávací modul umožňuje uživatelům zadat hledané termíny, aby mohli vyhledávat produkty. Adresa URL výchozí stránky pro vyhledávání a parametry vyhledávacího dotazu musí být zadány v **Nastavení webu \> Rozšíření**. Modul vyhledávání obsahuje vlastnosti, které umožňují potlačit tlačítko hledání nebo popis podle potřeby. Modul vyhledávání také podporuje možnosti automatického navrhování, například výsledky hledání produktů, klíčových slov a kategorií.

## <a name="create-a-header-module-for-a-page"></a>Vytvoření modulu záhlaví stránky

Chcete-li vytvořit modul záhlaví, postupujte následujícím způsobem.

1. Vytvořte fragment s názvem **Fragment záhlaví** a do něj přidejte modul kontejneru.
1. V podokně vlastností modulu kontejner nastavte vlastnost **Šířka** na **Vyplnit kontejner**.
1. Přidejte moduly propagačních bannnerů a souhlas se soubory cookie do modulu kontejneru.
1. Do fragmentu přidejte další modul kontejneru a nastavte vlastnost **Šířka** na **Vyplnit kontejner**.
1. Přidejte modul záhlaví do druhého modulu kontejneru.
1. Do pozice **Navigační nabídky** modulu záhlaví přidejte modul navigační nabídka. 
1. V podokně vlastností modulu navigační nabídka konfigurujte vlastnosti modulu navigační nabídka.
1. Do pozice **Vyhledávání** modulu záhlaví přidejte modul vyhledávání. 
1. V podokně vlastností modulu vyhledávání konfigurujte vlastnosti modulu vyhledávání. 
1. Uložte fragment stránky, dokončete úpravy a publikujte ji. 

Chcete-li zajistit, aby se záhlaví zobrazilo na každé stránce, postupujte podle následujících kroků pro všechny šablony stránek, které jsou pro daný web vytvořeny.

1. Do pozice **Hlavní** na výchozí stránce přidejte do záhlaví fragment záhlaví stránky obsahující modul záhlaví.
1. Uložte šablonu, dokončete úpravy a publikujte ji.

## <a name="additional-resources"></a>Další zdroje

[Přehled startovací sady](starter-kit-overview.md)

[Modul kontejneru](add-container-module.md)

[Modul buy boxu](add-buy-box.md)

[Modul košíku](add-cart-module.md)

[Modul pokladny](add-checkout-module.md)

[Modul potvrzení objednávky](order-confirmation-module.md)

[Modul záhlaví](author-header-module.md)

[Modul zápatí](author-footer-module.md)
