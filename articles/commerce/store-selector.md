---
title: Modul volby obchodu
description: Tohle téma se zabývá modulem výběru obchodu a popisuje, jak jej přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 03/19/2020
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
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: ''
ms.openlocfilehash: 460d05ca29d5b8da70a971a649d9edd786f7260d
ms.sourcegitcommit: 15c5ec742d648c5f3506d031a2ab6150dcbae348
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2020
ms.locfileid: "3378201"
---
# <a name="store-selector-module"></a>Modul volby obchodu

[!include [banner](includes/banner.md)]

Tohle téma se zabývá modulem výběru obchodu a popisuje, jak jej přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Přehled

Modul výběru obchodu je používán ve scénáři zákazníka „Nákup online, vyzvednutí v obchodě“ (BOPIS). Zobrazuje seznam obchodů, ve kterých je produkt k dispozici pro výdej, a také otevírací hodiny a zásoby produktů pro každý obchod.

Modul výběru obchodu vyžaduje pro vyhledání obchodů kontext produktu a umístění. V případě, že není k dispozici umístění, použije se umístění prohlížeče zákazníka za předpokladu, že zákazník udělí souhlas. Modul obsahuje vstupní pole, které umožňuje zákazníkovi zadat umístění (PSČ nebo město a stát) k vyhledání obchodů, které jsou v dosahu.

Modul volby obchodu je integrovaný s API geokódování služby Mapy Bing, které slouží k převodu umístění na zeměpisnou šířku a délku. Klíč rozhraní API mapy služby Bing je povinný a musí být přidán do stránky sdílené parametry pro Commerce v aplikaci Dynamics 365 Commerce.

Modul volby obchodu lze přidat do modulu buy boxu na stránce Podrobnosti o produktu a zobrazit obchody, ve kterých je produkt k dispozici pro výdej. Lze jej také přidat do modulu košíku. Při přidání do modulu košíku zobrazí modul volby obchodu možnosti vyzvednutí pro každou položku řádku nákupního košíku. Kromě toho s použitím vlastního kódu lze tento modul přidat na jiné stránky nebo do jiných modulů prostřednictvím rozšíření a přizpůsobení.

Aby scénář BOPIS fungoval, měly by být produkty konfigurovány se způsobem dodání „vyzvednutí zákazníkem“. V opačném případě se modul na příslušných stránkách nezobrazí. Podrobné informace o konfiguraci způsobu dodání naleznete v tématu [Nastavení způsobů dodání](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).

Následující obrázek znázorňuje příklad modulu volby obchodu použitého na stránce s podrobnostmi o produktu.

![Příklad modulu volby obchodu](./media/BOPIS.PNG)

## <a name="store-selector-module-usage-in-e-commerce"></a>Použití modulu volby obchodu v e-Commerce

- Modul volby obchodu lze použít na stránce Podrobnosti o produktu a vyhledat obchody v okolí, ve kterých je produkt k dispozici pro výdej.
- Modul volby obchodu lze použít na stránce košíku a vyhledat obchody v okolí, ve kterých je produkt v košíku k dispozici pro výdej.

## <a name="store-selector-module-properties"></a>Vlastnosti modulu volby obchodu

| Název vlastnosti             | Hodnota                 | popis |
|---------------------------|-----------------------|-------------|
| Poloměr pro hledání | Počet | Definuje poloměr při vyhledávání obchodů v mílích. Není-li zadána žádná hodnota, použije se výchozí poloměr 50 mil.|
|Podmínky služby | Adresa URL    |  Adresa URL podmínek služby, která je vyžadována službou Bing Maps. |

## <a name="add-a-store-selector-module-to-a-page"></a>Přidání modulu volby obchodu na stránku

Modul volby obchodu vyžaduje kontext produktu, a proto jej lze použít pouze v modulech buy boxu a košíku. Moduly volby obchodu nefungují mimo tyto moduly.

- Informace o přidání modulu volby obchodu do modulu buy boxu naleznete v tématu [Modul buy boxu](add-buy-box.md). 
- Informace o přidání modulu volby obchodu do modulu košíku naleznete v tématu [Modul košíku](add-cart-module.md).

## <a name="additional-resources"></a>Další prostředky

[Přehled startovací sady](starter-kit-overview.md)

[Modul buy boxu](add-buy-box.md)

[Modul košíku](add-cart-module.md)

[Rychlá prohlídka stránky podrobností o produktu](quick-tour-pdp.md)

[Rychlá prohlídka košíku a pokladny](quick-tour-cart-checkout.md)

[Nastavit způsoby dodání](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)

[Správa map Bing pro vaši organizaci](dev-itpro/manage-bing-maps.md)
