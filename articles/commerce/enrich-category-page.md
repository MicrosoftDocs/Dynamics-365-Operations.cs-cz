---
title: Obohacení cílové stránky kategorie
description: V tomto článku je popsáno obohacování stránek kategorií v řešení Dynamics 365 Commerce.
author: v-chgri
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: e3397ffee9b32f3d3efedea38255f88daee5233c
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282154"
---
# <a name="enrich-a-category-landing-page"></a>Obohacení cílové stránky kategorie

[!include [banner](includes/banner.md)]

V tomto článku je popsáno obohacování stránek kategorií v řešení Dynamics 365 Commerce.

Řešení Commerce poskytuje výchozí cílovou stránku kategorie, která se používá při zobrazení dat kategorie. Výchozí stránka kategorie obsahuje potřebné prvky, jako zpřesnění, umístění produktu zařazeného do kategorie, možnosti řazení, souhrn voleb a ovládací prvky stránkování. 

Namísto použití výchozí stránky kategorie však můžete použít „obohacenou“ cílovou stránku kategorie s dalším obsahem a specifickými prvky. Typické obohacení může zahrnovat přidání marketingového obchodního obsahu na stránku kategorie, které se týká. Tento obsah může zahrnovat umístění produktu, který je součástí více kategorií, pro účely křížového prodeje, redakční seznamy, obrázky, videa a další text. Výchozí stránku kategorie můžete buď upravit, nebo definovat jinou stránku kategorie pro určitou kategorii.

![Obohacená cílová stránka kategorie.](./media/CategoryLandingPages.png)

V tvůrci webů Commerce se na stránce **Produkt** nachází seznam kategorií z daného kanálu, které jsou přiřazeny k danému webu. Je- li pro stránku kategorie vybrán stav **Obohaceno**, tato stránka kategorie byla obohacena. V opačném případě se pro kategorii použije výchozí stránka a obsah kategorie. Chcete-li zobrazit náhled obohacených i neobohacených stránek kategorie, vyberte název kategorie.

Chcete-li obohatit stránku kategorie, postupujte podle následujících pokynů.

1. Na stránce **Produkty** vyberte název kategorie, jejíž stránku chcete obohatit. V editoru stránek se pro vybranou kategorii otevře výchozí stránka kategorie.
2. Vyberte **Obohatit stránku kategorie**.
3. Vyberte šablonu pro obohacenou stránku kategorie. Pokud provádíte pouze drobné změny, můžete vybrat výchozí stránku kategorie. Případně můžete vybrat některou ze šablon stránek kategorie. Když vyberete šablonu, otevře se editor stránek a vybraná šablona se použije k vytvoření nové stránky kategorie pro vybranou kategorii. Stránka je pro vás rezervována a nyní můžete provést změny.

> [!NOTE]
> Moduly, které používají data specifikace kategorie, používají data z vybrané kategorie. Nastavení šablony, kterou vyberete, určuje změny, které lze provést.

## <a name="additional-resources"></a>Další zdroje

[Úprava existující webové stránky](modify-existing-page.md)

[Přidání nové webové stránky](add-new-page.md)

[Výběr rozvržení stránky](select-page-layouts.md)

[Správa metadat SEO](manage-seo-metadata.md)

[Uložení, náhled a publikování stránky](save-preview-publish-page.md)

[Obohacení stránky produktu](enrich-product-page.md)

[Ověření přístupnosti obsahu stránky](verify-accessibility.md)

[Vytváření dynamických stránek elektronického obchodu na základě parametrů adresy URL](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
