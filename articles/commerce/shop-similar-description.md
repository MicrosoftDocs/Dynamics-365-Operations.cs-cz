---
title: Povolení doporučení „nákupu podobného vzhledu“
description: Tento článek popisuje, jak povolit v doporučení „nákupu zboží s podobným popisem“ v Microsoft Dynamics 365 Commerce.
author: bebeale
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: bebeale
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.16
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail, eCommerce
ms.search.form: ''
ms.openlocfilehash: c15122d15660144f46528bd8c575029bf9d966c6
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274971"
---
# <a name="enable-shop-similar-description-recommendations"></a>Povolení doporučení „nákupu podobného vzhledu“

[!include [banner](includes/banner.md)]

Tento článek popisuje, jak povolit v doporučení „nákupu zboží s podobným popisem“ v Microsoft Dynamics 365 Commerce.

Doporučení "nákupu zboží s podobným popisem" v Dynamics 365 Commerce využívá umělou inteligenci a strojové učení (AI-ML) k poskytování doporučení produkty, které mají podobný popis jako produkty, které zákazníci hledají. Poskytnutím doporučení typu „podobný popis“ pro všechny maloobchodní kanály v Commerce mohou maloobchodní prodejci pomoci zákazníkům snadno najít to, co hledají.

Funkce pro doporučení „nákupu zboží s podobným popisem“ používá název a popis produktů produktů typu seed k nalezení a doporučení podobných produktů v katalogu produktů maloobchodního prodejce.

Doporučení typu „podobný popis“ jsou k dispozici jak v místě prodeje (POS), tak v prostředí elektronického obchodování.

## <a name="example-scenarios"></a>Ukázkové scénáře

Následující ukázkové scénáře ukazují typy doporučení, které může funkce „nákupu zboží s podobným popisem“ poskytnout:

- Zákazník si prohlíží brýle v retro stylu s rohovou obroučkou a dostane několik doporučení na další brýle, které mají podobný design, v kontextu sortimentu maloobchodního prodejce.
- Zákazník používá doporučení k „nákupu zboží s podobným popisem“ k objevení dalších příchutí kávy, které jsou podobné příchuti, kterou již dříve od maloobchodního prodejce zakoupil.

## <a name="set-up-shop-similar-description-recommendations"></a>Nastavení doporučení „nákupu zboží s podobným popisem“

Doporučení produktů jsou podporována pouze u užovatelů Commerce, kteří migrovali své úložiště do služby Azure Data Lake Storage Gen2.

### <a name="prerequisites"></a>Předpoklady

Než se zákazníkům mohou zobrazit doporučení k „nákupu zboží s podobným popisem“, musíte splnit následující předpoklady:

- [Povolit doporučení produktů](enable-product-recommendations.md) v centrále Commerce.
- Ověřit, zda mediální server podporuje volání HTTPS.

### <a name="turn-on-the-shop-similar-description-recommendations-feature"></a>Zapnutí funkce „nákupu zboží s podobným popisem“

Chcete-li zapnout funkci doporučení typu „podobný popis“ v centrále Commerce, postupujte takto.

1. V pracovním prostoru **Správa funkcí**, v seznamu dostupných funkcí vyhledejte a vyberte **Nákup zboží s podobným popisem**.
1. V pravém podokně vyberte **Povolit**.

> [!NOTE]
> Když tuto funkci zapnete, systém začne generovat seznamy doporučení produktů. Může trvat až jeden den, než busou tyto seznamy k dispozici a viditelné online a v POS terminálech.
>
> Pokud tuto funkci vypnete, ostatních typů doporučení produktů se to nedotkne. Další informace o doporučeních produktů naleznete v tématu [Přehled doporučení produktu](product-recommendations.md).

## <a name="add-a-shop-similar-description-button-to-product-details-pages"></a>Přidejte tlačítko Nákup zboží s podobným popisem na stránky s podrobnostmi o produktu

Poté, co v centrále Commerce zapnete funkci doporučení typu „podobný popis“, můžete přidat tlačítko **Zboží s podobným popisem** do buy boxu na jakékoli stránce s podrobnostmi o produktu (PDP). Zákazník, který vybere toto tlačítko, se přesune na vyhrazenou stránku **Nákup zboží s podobným popisem**, která zobrazí vizuálně podobné produkty. Zákazník pak může pomocí selektorů dále filtrovat produkty.

K přidání tlačítka **Nákup zboží s podobným popisem** na PDP pomocí konfigurátoru webu Commerce, postupujte následujícím způsobem.

1. Otevře existující stránku konfigurátoru webu, která obsahuje modul buy boxu.
1. V levém navigačním podokně vyberte modul buy boxu.
1. V pravém navigačním podokně zaškrtněte políčko **Povolit odkaz na zboží s podobným popisem**.
1. Zvolte **Uložit**.
1. Chcete-li vrátit stránku se změnami, vyberte možnost **Dokončit úpravy** a volbou **Publikovat** ji publikujte. Po publikování stránky bude PDP obsahovat tlačítko **Nákup zboží s podobným popisem**.

Následující obrázek ukazuje zaškrtávací políčko **Povolit odkaz na na zboží s podobným popisem** a tlačítko **Podobný popis** na příkladu PDP v konfigurátoru webů.

![Zaškrtávací políčko Povolit odkaz na zboží s podobným popisem a tlačitko Podobný popis na PDP v konfigurátoru webů.](./media/ter_site_builder_buybox_button.png)

## <a name="additional-resources"></a>Další prostředky

[Přehled doporučení produktu](product-recommendations.md)

[Povolení Azure Data Lake Storage v prostředí Dynamics 365 Commerce](enable-adls-environment.md)

[Povolit doporučení produktu](enable-product-recommendations.md)

[Povolení doporučení „nákupu podobného vzhledu“](shop-similar-looks.md)

[Úprava výsledků doporučení AI-ML](modify-product-recommendation-results.md)

[Ručně vytvořit uspořádaná doporučení](create-editorial-recommendation-lists.md)

[Často kladené dotazy k doporučení produktu](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
