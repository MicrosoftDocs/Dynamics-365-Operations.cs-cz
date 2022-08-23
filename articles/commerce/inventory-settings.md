---
title: Použití nastavení zásob
description: Tento článek se týká nastavení zásob a popisuje, jak je použít v Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 10/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: bc55715b7c74f3b572459dd1aa7d409b7175535b
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9287585"
---
# <a name="apply-inventory-settings"></a>Použití nastavení zásob

[!include [banner](includes/banner.md)]

Tento článek se týká nastavení zásob a popisuje, jak je použít v Microsoft Dynamics 365 Commerce.

Nastavení zásob určuje, zda se mají zásoby zkontrolovat před přidáním produktů do košíku. Rovněž definují zprávy související se zásobami, například „Na skladě“ a „Zbývá jen několik“. Toto nastavení zajišťuje, že produkt nelze zakoupit, pokud není na skladě.

Dynamics 365 Commerce poskytuje odhady dostupnosti produktů na skladě. Informace o tom, jak se vypočítává odhadovaná dostupnost na skladě, viz [Vypočítat dostupnost zásob pro maloobchodní kanály](calculated-inventory-retail-channels.md).

V tvůrci webů Commerce lze definovat prahové hodnoty a rozsahy zásob pro produkt nebo kategorii. Určují, zda lze zásoby klasifikovat jako zásoby, nízké zásoby nebo vyprodané. Podrobnosti najdete v tématu [Konfigurace rezervních zásob a úrovní zásob](inventory-buffers-levels.md).

> [!NOTE]
> Podpora prahových hodnot a rozsahů inventáře je k dispozici v Dynamics 365 Commerce vydání 10.0.12.

## <a name="inventory-settings"></a>Nastavení zásob

V Commerce jsou nastavení zásob definována v **Nastavení webu \> Rozšíření \> Řízení zásob** ve tvůrci webu. Existuje šest nastavení zásob, z nichž jedno je zastaralé:

- **Povolit kontrolu skladu v aplikaci** – Toto nastavení zapne kontrolu zásob produktu. Buy box, nákupní košík a vyzvednutí v modulech obchod pak zkontrolují zásoby produktu a umožní přidání produktu do košíku, pouze pokud je k dispozici.
- **Úroveň zásob na základě** - Toto nastavení definuje způsob výpočtu úrovní zásob. Dostupné hodnoty jsou **Celkem k dispozici**, **Fyzicky k dispozici** a **Prahová hodnota pro vyprodáno**. V Commerce lze definovat prahové hodnoty a rozsahy zásob pro každý produkt a kategorii. Rozhraní API zásob vracejí informace o zásobách produktů pro majetek **Celkem k dispozici** a **Fyzicky k dispozici**. Prodejce rozhodne, zda hodnota **Celkem k dispozici** nebo **Fyzicky k dispozici** by měla být použita k určení počtu zásob a odpovídajících rozsahů pro stavy na skladě a vyprodáno.

    Hodnota **Prahová hodnota vyprodáno** nastavení **Úroveň zásob na základě** je zastaralá hodnota. Pokud je vybrána, počet zásob je určen z výsledků hodnoty **Celkem k dispozici**, ale prahová hodnota je definována pomocí numerického nastavení **Prahová hodnota pro vyprodáno**, které je popsáno dále. Toto nastavení prahové hodnoty se vztahuje na všechny produkty na webu elektronického obchodování. Pokud jsou zásoby pod prahovým číslem, produkt se považuje za vyprodaný. Jinak se to považuje za skladem. Možnosti hodnoty **Prahová hodnota pro vyprodáno** jsou omezené a nedoporučujeme je používat ve verzi 10.0.12 a novější.

- **Úroveň zásob pro více skladů** – Toto nastavení umožňuje výpočet úrovně zásob oproti výchozímu skladu nebo více skladům. Možnost **Na základě individuálního skladu** vypočítá úrovně zásob na základě výchozího skladu. Alternativně může web elektronického obchodu odkazovat na více skladů, aby se usnadnilo plnění. V takovém případě se možnost **Na základě agregátu pro sklady pro přepravu a vyzvednutí** používá k označení dostupnosti zboží. Když si například zákazník zakoupí položku a jako způsob dodání zvolí „dodání“, může být položka odeslána z jakéhokoli skladu ve skupině plnění, která má k dispozici zásoby. Na stránce s podrobnostmi o produktu (PDP) se zobrazí zpráva „Skladem“ pro odeslání, pokud má jakýkoli dostupný přepravní sklad ve skupině plnění zásoby. 

    > [!IMPORTANT] 
    > Nastavení **Úroveň zásob pro více skladů** je k dispozici od verze Commerce verze 10.0.19. Pokud provádíte aktualizaci ze starší verze Commerce, musíte ručně aktualizovat soubor appsettings.json. Další pokyny viz [SDK a aktualizace knihovny modulů](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).

- **Nastavení zásob pro stránky se seznamem produktů** – Toto nastavení definuje, jak se produkty, které nejsou skladem, zobrazí v seznamech produktů, které jsou vykreslovány pomocí modulů kolekce produktů a výsledků vyhledávání. Dostupné hodnoty jsou **Zobrazit v pořadí s ostatními produkty**, **Skrýt ze seznamu produkty, které nejsou na skladě** a **Zobrazit produkty, které nejsou skladem, na konci seznamu**. Chcete-li použít toto nastavení, musíte nejprve nakonfigurovat některá nezbytná nastavení v centrále Commerce. Více informací viz [Aktivace povědomí o zásobách pro modul výsledků vyhledávání](search-result-module.md#enable-inventory-awareness-for-the-search-results-module).

    > [!IMPORTANT] 
    > **Nastavení zásob pro stránky seznamu produktů** je k dispozici od verze Commerce verze 10.0.20. Pokud provádíte aktualizaci ze starší verze Commerce, musíte ručně aktualizovat soubor appsettings.json. Další pokyny viz [SDK a aktualizace knihovny modulů](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).

- **Rozsahy zásob** - Toto nastavení definuje rozsahy zásob, pro které se zpráva zobrazuje na modulech webu. Je to použitelné, pouze pokud je vybrána hodnota **Celkem k dispozici** nebo **Fyzicky k dispozici** pro nastavení **Úroveň zásob na základě**. Dostupné hodnoty jsou **Všechno**, **Nízké a vyprodané** a **Vyprodáno**.

    - Je-li vybráno **Všechno**, zobrazí se zprávy pro všechny rozsahy zásob, od skladem (zpráva „Dostupné“) po vyprodáno (zpráva „Není skladem“).
    - Je-li vybráno **Nízké a vyprodané**, zobrazí se zprávy pro všechny rozsahy zásob, kromě skladem (zpráva „Dostupné“).
    - Je-li vybráno **Vyprodáno**, zobrazí se pouze zpráva „Není na skladě“.

- **Prahová hodnota pro vyprodáno** - Toto staré číselné nastavení se projeví, pouze pokud je vybrána hodnota **Prahová hodnota pro vyprodáno** pro nastavení **Úroveň zásob na základě**.

> [!IMPORTANT] 
> Tato nastavení jsou k dispozici ve vydání Dynamics 365 Commerce 10.0.12. Pokud provádíte aktualizaci ze starší verze Dynamics 365 Commerce, musíte ručně aktualizovat soubor appsettings.json. Pokyny k aktualizaci souboru appsettings.json najdete v části [Aktualizace SDK a knihoven modulů](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).

## <a name="modules-that-use-inventory-settings"></a>Moduly, které používají nastavení zásob

Moduly Buy box, seznam přání, volby obchodu, košík a ikona košíku používají nastavení zásob k zobrazení rozsahů zásob a zpráv.

V příkladu na následujícím obrázku PDP zobrazuje zprávu na skladě („Dostupné“).

![Příklad modulu PDP, který obsahuje zprávu na skladě.](./media/pdp-InStock.png)

V příkladu na následujícím obrázku PDP zobrazuje zprávu „Není na skladě“.

![Příklad modulu PDP, který obsahuje zprávu vyprodáno.](./media/pdp-outofstock.png)

V příkladu na následujícím obrázku košík zobrazuje zprávu na skladě („Dostupné“).

![Příklad modulu košíku, který obsahuje zprávu na skladě.](./media/cart-instock.png)

## <a name="additional-resources"></a>Další prostředky

[Přehled knihovny modulů](starter-kit-overview.md)

[Konfigurace rezervních zásob a úrovní zásob](inventory-buffers-levels.md)

[Modul košíku](add-cart-module.md)

[Modul buy boxu](add-buy-box.md)

[Moduly a stránky správy obchodního vztahu](account-management.md)

[Modul volby obchodu](store-selector.md)

[SDK a aktualizace knihovny modulů](e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
