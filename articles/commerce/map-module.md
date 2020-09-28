---
title: Modul mapy
description: Toto téma popisuje moduly mapy a popisuje, jak je konfigurovat v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 07/31/2020
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
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: ca531e6cbf0a1044b0a13e5cdf42c7b4f0498fe5
ms.sourcegitcommit: 629988f1a704d62648d98649056931b8c33b9e08
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/14/2020
ms.locfileid: "3811177"
---
# <a name="map-module"></a>Modul mapy

[!include [banner](includes/banner.md)]


Toto téma popisuje moduly mapy a popisuje, jak je konfigurovat v řešení Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Přehled

Modul mapy zobrazuje umístění obchodů na interaktivní mapě, která je vykreslena pomocí [webového ovládacího prvku Bing Maps V8](https://docs.microsoft.com/bingmaps/v8-web-control/). Klíč rozhraní API mapy služby Bing je povinný a musí být přidán do stránky se sdílenými parametry pro centrálu Commerce. Moduly mapy poskytují různá zobrazení, jako jsou silniční, anténní a pouliční, které si uživatelé mohou vybrat pro zobrazení polohy na mapě. Umožňují také interakce, jako je přibližování a používání polohy uživatele.

Modul mapy pracuje ve spojení s modulem pro výběr obchodů a určuje geografická umístění obchodů, které musí být vykresleny na mapě. Selektor úložiště a moduly mapy spolupracují, když uživatel vybere úložiště v jednom z těchto modulů na stránce webu. Moduly mapy lze rozšířit i na další scénáře, mimo interakci s moduly výběru obchodů. Vyžaduje se však přizpůsobení modulu.

Modul mapy byl představen ve verzi Commerce 10.0.13.

Následující obrázek ukazuje příklad modulu mapy bloku použitého na stránce umístění obchodu.

![Příklad modulu volby obchodu](./media/ecommerce-Storelocator.PNG)

## <a name="module-properties"></a>Vlastnosti modulu

| Název vlastnosti             | Hodnota                 | popis |
|---------------------------|-----------------------|-------------|
| Nadpis | Text | Nadpis modulu. |
| Možnosti připínáčku: Výchozí ikona | Obrázek | Obrázek symbolu připínáčku, který se má použít pro obchody zobrazené na mapě. |
| Možnosti připínáčku: aktivní ikona | Obrázek | Obrázek symbolu připínáčku, který se má použít pro obchod vybraný na mapě. |
| Možnosti připínáčku: Barva výchozí ikony | Řetězec znaků | Text nebo hexadecimální hodnota barvy symbolů připínáčku na mapě. |
| Možnosti připínáčku: barva aktivní ikony | Řetězec znaků | Textová nebo hexadecimální hodnota barvy vybraných symbolů připínáčku na mapě. |
| Zobrazit index | **Pravda** nebo **nepravda** | Pokud je tato vlastnost nastavena na **pravda**, každý symbol připínáčku, který označuje obchod, zobrazí index. Tento index bude odpovídat indexu v zobrazení seznamu, které zobrazuje modul pro výběr úložiště. |

## <a name="add-allowed-mapping-urls-to-a-sites-content-security-policy-directives"></a>Přidejte povolené mapovací adresy URL do směrnic zásad zabezpečení obsahu webu

Aby modul map pracoval s mapami Bing, musíte zajistit, aby byly povoleny následující adresy URL maování (známé také jako „whitelisted“) podle zásad zabezpečení obsahu vašeho webu (CSP). Toto nastavení se provádí v nástroji Commerce site Builder přidáním povolených adres URL do různých směrnic CSP webu (například **img-src**). Další informace viz [Zásady zabezpečení obsahu](manage-csp.md). 

- Do směrnice **connect-src** přidejte **&#42;.bing.com**.
- Do směrnice **img-src** přidejte **&#42;.virtualearth.net**.
- Do směrnice **script-src** přidejte **&#42;.bing.com, &#42;.virtualearth.net**.
- Do směrnice **script-src** přidejte **&#42;.bing.com**.

## <a name="add-a-map-module-to-a-page"></a>Přidání modulu mapy na stránku

Podrobné informace o konfiguraci modulu mapy na stránce viz [Uložení modulu selektoru](store-selector.md). 
 
## <a name="additional-resources"></a>Další prostředky

[Přehled startovací sady](starter-kit-overview.md)

[Modul buy boxu](add-buy-box.md)

[Modul košíku](add-cart-module.md)

[Modul volby obchodu](store-selector.md)

[Správa map Bing pro vaši organizaci](./dev-itpro/manage-bing-maps.md)

[Webový ovládací prvek Bing Maps V8](https://docs.microsoft.com/bingmaps/v8-web-control/)
