---
title: Obohacení stránky produktu
description: Toto téma popisuje, jak obohatit stránku produktu v řešení Microsoft Dynamics 365 Commerce.
author: psimolin
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: f6c1a9474ed514426386b1d7b4a72b62129cdb8a
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799030"
---
# <a name="enrich-a-product-page"></a>Obohacení stránky produktu

[!include [banner](includes/banner.md)]

Toto téma popisuje, jak obohatit stránku produktu v řešení Microsoft Dynamics 365 Commerce.

Ve výchozím nastavení používá web pro zobrazení dat produktu běžnou stránku. Tato stránka obsahuje základní informace o produktu a ovládací prvky, které jsou nutné k jeho prodeji. Můžete však doplnit informace, které pocházejí z Commerce Scale Unit, o další obrázky nebo text pro určitý produkt. Tento proces nazýváme obohacováním stránky produktu.

V mnoha případech budete chtít pro vaše produkty použít určitý dodatečný obsah. Když přejdete do části **Retail a Commerce** ve vývojovém nástroji, zobrazí se seznam produktů z kanálu, který je přiřazený k danému webu. V tomto seznamu určuje sloupec **Obohaceno**, zda byla stránka produktu pro produkt obohacena. Je-li ve sloupci zobrazeno zaškrtávací políčko, pro produkt existuje obohacená stránka produktu. Pokud se zaškrtávací políčko nezobrazuje, pro produkt je použita výchozí stránka a obsah produktu. Chcete-li zobrazit náhled obohacených i neobohacených stránek produktu, vyberte v seznamu název produktu.

## <a name="enrich-a-product-page"></a>Obohacení stránky produktu

Chcete-li obohatit stránku produktu, postupujte podle následujících kroků.

1. V části **Weby** vyberte **Fabrikam** (nebo název vašeho webu).
1. V navigačním podokně nalevo vyberte položku **Produkty**.
1. Vyberte libovolný produkt, který nemá obohacenou stránku.
1. V podokně akcí klikněte na možnost **Obohatit stránku produktu**.
1. Vyberte **Šablona stránky s podrobnostmi o produktu** a potom **OK**.
1. Ve stromu osnovy stránky nalevo rozbalte pozici **Hlavní**.
1. Vyberte tlačítko se třemi tečkami (**...**) vedle pozice **Hlavní** a poté vyberte možnost **Přidat modul**.
1. Vyberte **Kontejner 2** a potom **OK**.
1. Pro **Kontejner 2** vyberte tlačítko se třemi tečkami a poté vyberte možnost **Přidat modul**.
1. Vyberte možnost **Funkce** a potom **OK**.
1. V podokně vlastností vpravo v poli **Formátovaný text** zadejte aktualizovaný popis produktu.
1. Do pole **Nadpis** zadejte text nadpisu a pak vyberte **OK**.
1. Vyberte **Uložit** a potom vyberte **Dokončit úpravy**.
1. Do pole **Komentáře** zadejte **Obohacený produkt** a pak vyberte **OK**.
1. Volbou **Náhled** zobrazíte náhled obohacené stránky produktu. Až skončíte, zavřete kartu náhledu a vraťte se do nástroje pro vytváření obsahu.
1. Zvolte **Publikovat**.

## <a name="additional-resources"></a>Další zdroje

[Úprava existující webové stránky](modify-existing-page.md)

[Přidání nové webové stránky](add-new-page.md)

[Výběr rozvržení stránky](select-page-layouts.md)

[Správa metadat SEO](manage-seo-metadata.md)

[Uložení, náhled a publikování stránky](save-preview-publish-page.md)

[Obohacení cílové stránky kategorie](enrich-category-page.md)

[Ověření přístupnosti obsahu stránky](verify-accessibility.md)

[Vytváření dynamických stránek elektronického obchodu na základě parametrů adresy URL](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
