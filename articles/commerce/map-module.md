---
title: Modul mapy
description: Tento článek popisuje moduly mapy a popisuje, jak je konfigurovat v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: d72091baf2f216bfbe33950950f8917c3ba1ba5c
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283339"
---
# <a name="map-module"></a>Modul mapy

[!include [banner](includes/banner.md)]


Tento článek popisuje moduly mapy a popisuje, jak je konfigurovat v řešení Microsoft Dynamics 365 Commerce.

Modul mapy zobrazuje umístění obchodů na interaktivní mapě, která je vykreslena pomocí [webového ovládacího prvku Bing Maps V8](/bingmaps/v8-web-control/). Klíč rozhraní API mapy služby Bing je povinný a musí být přidán do stránky se sdílenými parametry pro centrálu Commerce. Moduly mapy poskytují různá zobrazení, jako jsou silniční, anténní a pouliční, které si uživatelé mohou vybrat pro zobrazení polohy na mapě. Umožňují také interakce, jako je přibližování a používání polohy uživatele.

Modul mapy pracuje ve spojení s modulem pro výběr obchodů a určuje geografická umístění obchodů, které musí být vykresleny na mapě. Selektor úložiště a moduly mapy spolupracují, když uživatel vybere úložiště v jednom z těchto modulů na stránce webu. Moduly mapy lze rozšířit i na další scénáře, mimo interakci s moduly výběru obchodů. Vyžaduje se však přizpůsobení modulu.

> [!NOTE]
> Mapový modul je k dispozici v Dynamics 365 Commerce vydání 10.0.13.

Následující obrázek ukazuje příklad modulu mapy bloku použitého na stránce umístění obchodu.

![Příklad modulu volby obchodu.](./media/ecommerce-Storelocator.PNG)

## <a name="module-properties"></a>Vlastnosti modulu

| Název vlastnosti             | Hodnota                 | popis |
|---------------------------|-----------------------|-------------|
| Záhlaví | Text | Nadpis modulu. |
| Možnosti připínáčku: Výchozí ikona | Obrázek | Obrázek symbolu připínáčku, který se má použít pro obchody zobrazené na mapě. |
| Možnosti připínáčku: aktivní ikona | Obrázek | Obrázek symbolu připínáčku, který se má použít pro obchod vybraný na mapě. |
| Možnosti připínáčku: Barva výchozí ikony | Řetězec znaků | Text nebo hexadecimální hodnota barvy symbolů připínáčku na mapě. |
| Možnosti připínáčku: barva aktivní ikony | Řetězec znaků | Textová nebo hexadecimální hodnota barvy vybraných symbolů připínáčku na mapě. |
| Zobrazit index | **Pravda** nebo **nepravda** | Pokud je tato vlastnost nastavena na **pravda**, každý symbol připínáčku, který označuje obchod, zobrazí index. Tento index bude odpovídat indexu v zobrazení seznamu, které zobrazuje modul pro výběr úložiště. |

## <a name="add-allowed-mapping-urls-to-a-sites-content-security-policy-directives"></a>Přidejte povolené mapovací adresy URL do směrnic zásad zabezpečení obsahu webu

Aby modul map pracoval s mapami Bing, musíte zajistit, aby byly povoleny následující adresy URL maování podle zásad zabezpečení obsahu vašeho webu (CSP). Toto nastavení se provádí v nástroji Commerce site Builder přidáním povolených adres URL do různých směrnic CSP webu (například **img-src**). Další informace viz [Zásady zabezpečení obsahu](manage-csp.md). 

- Do směrnice **connect-src** přidejte **&#42;.bing.com**.
- Do směrnice **img-src** přidejte **&#42;.virtualearth.net**.
- Do směrnice **script-src** přidejte **&#42;.bing.com, &#42;.virtualearth.net**.
- Do směrnice **script-src** přidejte **&#42;.bing.com**.

## <a name="add-a-map-module-to-a-page"></a>Přidání modulu mapy na stránku

Podrobné informace o konfiguraci modulu mapy na stránce viz [Uložení modulu selektoru](store-selector.md). 
 
## <a name="additional-resources"></a>Další prostředky

[Přehled knihovny modulů](starter-kit-overview.md)

[Modul buy boxu](add-buy-box.md)

[Modul košíku](add-cart-module.md)

[Modul volby obchodu](store-selector.md)

[Správa map Bing pro vaši organizaci](./dev-itpro/manage-bing-maps.md)

[Webový ovládací prvek Bing Maps V8](/bingmaps/v8-web-control/)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
