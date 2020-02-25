---
title: Prohlídka stránek podrobností o produktu
description: Toto téma poskytuje přehled stránek podrobností o produktu (PDP) v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: dbf8f4c1ea479a508f4a0294020b7201b32fe228
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025918"
---
# <a name="overview-of-product-details-pages"></a>Prohlídka stránek podrobností o produktu


[!include [banner](includes/banner.md)]

Toto téma poskytuje přehled stránek podrobností o produktu (PDP) v řešení Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Přehled

Systém PDP poskytuje podrobné informace o produktu a umožňuje zákazníkům vybrat možnosti produktu, například velikost, styl a barvu. PDP by měl předprezentovat všechny informace o produktu, které odběratel potřebuje k provedení rozhodnutí o nákupu.

Následující obrázek znázorňuje příklad PDP

![Příklad stránky podrobností o produktu](./media/pdp.PNG)

## <a name="header-and-footer-modules"></a>Moduly záhlaví a zápatí

Horní okraj PDP obsahuje záhlaví, ve kterém jsou zobrazeny všechny kategorie produktů a další stránky, které chtějí odběratelé vyhledávat. Dolní okraj stránky má zápatí, které obsahuje rychlé odkazy na různá témata, která mohou být zajímavá.

## <a name="buy-box-module"></a>Modul buy boxu

Nejdůležitějším modulem systému PDP je modul buy boxu, který se zobrazí jako první položka v hlavní části stránky. Modul buy boxu zobrazuje důležité informace o produktu, jako je například název produktu, popis produktu, cena produktu, obrázky produktů a hodnocení produktu.

Modul buy boxu umožňuje odběrateli vybrat možnosti produktu (například velikost, styl a barvu) a přidat produkt do košíku. Rovněž umožňuje odběrateli nakoupit produkt online a vyzvednout jej v obchodě. Nákup online a výdej v modulu obchod používá integraci s rozhraními API služby Bing Maps k hledání blízkých obchodů nebo obchodů v jiném umístění, které určuje zákazník.

Modul buy boxu vyžaduje ID produktu. Toto ID je odvozeno od kontextu stránky. Je-li do stránky přidán modul buy boxu, na kterém kontext stránky neobsahuje ID produktu, nebudou informace správně vygenerovány.

## <a name="product-specifications-module"></a>Modul specifikací produktu

Modul specifikací produktu lze použít k předvedení dalších podrobností o produktu. Tyto podrobnosti jsou čerpány z atributů produktu v aplikaci Commerce. V modulu specifikace produktu jsou zobrazeny všechny atributy, pro které je vlastnost **viditelné** nastavena na hodnotu **true**. K načtení atributů produktu je vyžadováno ID produktu.

## <a name="recommendations-module"></a>Modul doporučení

Nejdůležitějším modulem systému PDP je modul doporučení. Zatímco odběratelé procházejí produkty, měly by jim být prezentovány další možnosti produktu, aby mohli najít správný produkt a nakupovat. Doporučení zákazníkům umožňují snadno objevit související obsah a pokračovat v nákupu.

K dispozici jsou různé typy seznamů doporučení:

- Seznam **Lidem se také líbí** je založen na strojovém učení. K poskytování doporučení používá historii transakcí ostatních zákazníků. Tento seznam je vygenerován službou doporučení a připomíná seznam "Zákazníci, kteří toto nakoupili, koupili také...". K vygenerování tohoto seznamu je nutné ID produktu.
- Seznam **Související** lze nakonfigurovat pro produkt v Commerce. U souvisejícího seznamu lze nakonfigurovat například pro hnědou koženou kabelku další kabelky, které jsou kožené nebo navržené pro cestování. Jiné typy souvisejících seznamů, například **Doplňky** a **Podobně**, lze také konfigurovat v Commerce. K vygenerování tohoto seznamu je nutné ID produktu. Proto, pokud je přidán na domovskou stránku, kde kontext stránky neobsahuje ID produktu, bude seznam prázdný.
- lgoritmem generované seznamy doporučení, jako je například **Trendující**, **Nejlepe prodávané** a **Nové**, lze použít na PDP. Ačkoli tyto seznamy nemusí přímo souviset s produktem v systémech PDP, jsou jiným způsobem, jak zákazníkům pomoci najít produkty, které je mohou zajímat. Tyto typy seznamů nevyžadují ID produktu. Jedná se o obecné seznamy, které jsou generovány na základě vzorků nákupu v celém webu.
- Redakční seznamy jsou ručně spravované seznamy. Maloobchodní prodejce se může například rozhodnout ručně spravovat seznamy výrobků, které chce prezentovat.

## <a name="ratings-and-reviews-modules"></a>Moduly hodnocení a recenzí

K zobrazení a přidání recenzí lze použít tři moduly:

- **Modul hodnocení a recenzí** - tento modul zobrazuje hodnocení a recenze poskytované jinými odběrateli. Zákazníci mohou tyto recenze třídit a filtrovat. Tento modul také zákazníkům umožňuje zákazníkům označovat recenze jako To se mi líbí nebo Už se mi to nelíbí a hlásit problémy.
- **Napsat recenzi** – tento modul umožní zákazníkům psát vlastní recenze produktu.
- **Histogram hodnocení** – Tento modul obsahuje histogram, který zobrazuje trend hodnocení produktu.

Další podrobnosti získáte v tématu [Přehled hodnocení a recenzí](ratings-reviews-overview.md).

## <a name="marketing-modules"></a>Moduly marketing

Pokud je marketingový obsah jedinečný pro určitý produkt, lze do PDP přidat libovolný marketingový modul. Marketingové moduly můžete přidat do PDP pomocí "obohacení" stránky. Další informace naleznete v tématu [Obohacení stránky produktu](enrich-product-page.md).

## <a name="additional-resources"></a>Další zdroje

[Přehled domovské stránky](quick-tour-home-page.md)

[Přehled výchozí cílové stránky kategorie a stránky výsledků hledání](category-search-page-overview.md)

[Přehled stránek košíku a pokladny](quick-tour-cart-checkout.md)

[Přehled stránek správy účtů](quick-tour-account-management.md)

[Obohacení stránky podrobností produktu](enrich-product-page.md)
