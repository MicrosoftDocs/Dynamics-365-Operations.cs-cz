---
title: Použití nastavení měrné jednotky
description: Tento článek se týká nastavení měrných jednotek a popisuje, jak je použít v softwaru Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 04/23/2021
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
ms.openlocfilehash: 7a7be6395a8bfce38e84f850bd792f358941c18a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275534"
---
# <a name="apply-unit-of-measure-settings"></a>Použití nastavení měrné jednotky

[!include [banner](includes/banner.md)]

Tento článek se týká nastavení měrných jednotek a popisuje, jak je použít v softwaru Microsoft Dynamics 365 Commerce.

Produkt lze prodávat v různých jednotkách, například „jednotlivě“, „pár“ a „tucet“. V Commerce Headquarters lze pro produkt definovat měrnou jednotku prodeje a zobrazit ji na webu elektronického obchodu. Například pokud maloobchodník prodává produkt jednotlivě i v desítkách, lze zobrazit dostupné měrné jednotky společně s dalšími informacemi o produktu.

V příkladu na následujícím obrázku byla v Commerce Headquarters nakonfigurována měrná jednotka prodeje ve výši **ea** (jednotlivě).

![Příklad produktu, který je nakonfigurován s měrnou jednotkou v Commerce Headquarters.](./media/Productunit-headquarters.PNG)

> [!NOTE]
> Podpora pro použití a zobrazování měrných jednotek je k dispozici od verze Commerce 10.0.19.

## <a name="unit-of-measure-settings"></a>Nastavení měrných jednotek

Nastavení zobrazení měrné jednotky je definováno v konfigurátoru webů Commerce v nabídce **Nastavení webu \> Rozšíření \> Zobrazit měrnou jednotku pro produkty**. Existují tři podporovaná nastavení:

- **Nezobrazovat** – je-li toto nastavení vybráno, web elektronického obchodu nebude zobrazovat měrnou jednotku produktu. Toto chování je výchozím chováním.
- **Zobrazit při nákupu produktu** – když je toto nastavení vybráno, měrná jednotka se zobrazí na stránkách s podrobnostmi o produktu, košíku, pokladně, historii objednávek a stránkách podrobností objednávek.
- **Zobrazit v procházení a nakupování produktu** – pokud je toto nastavení vybráno, měrná jednotka se zobrazí na stránkách nákupu produktu a také během procházení produktu. V rámci tohoto chování se měrné jednotky zobrazují ve výsledcích vyhledávání a v modulech kolekce produktů.

> [!IMPORTANT]
> Nastavení zobrazení měrných jednotek je k dispozici od verze Commerce 10.0.19. Pokud provádíte aktualizaci ze starší verze Commerce, musíte ručně aktualizovat soubor appsettings.json. Další pokyny viz [SDK a aktualizace knihovny modulů](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).

## <a name="modules-that-use-unit-of-measure-settings"></a>Moduly, které používají nastavení měrné jednotky

Moduly, které používají nastavení měrné jednotky, zahrnují moduly buy boxu, seznamu přání, košíku, ikony košíku, kontejneru výsledků hledání, kolekce produktů, pokladny a podrobností objednávky.

Na příkladu na následujícím obrázku zobrazuje stránka s podrobnostmi o produktu (PDP) měrné jednotky (**ea**) pro produkt.

![Příklad PDP, která zobrazuje měrnou jednotku.](./media/Productunit-PDP.png)

Na příkladu na následujícím obrázku zobrazuje modul kolekce produktu měrné jednotky (**ea**) pro produkt.

![Příklad modulu kolekce produktu, který zobrazuje měrnou jednotku.](./media/Productunit-productcollection.png)

## <a name="additional-resources"></a>Další prostředky

[Přehled knihovny modulů](starter-kit-overview.md)

[Modul košíku](add-cart-module.md)

[Modul buy boxu](add-buy-box.md)

[Moduly a stránky správy obchodního vztahu](account-management.md)

[SDK a aktualizace knihovny modulů](e-commerce-extensibility/sdk-updates.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
