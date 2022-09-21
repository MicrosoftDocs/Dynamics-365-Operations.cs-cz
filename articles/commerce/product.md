---
title: Přidání doporučení produktů do POS
description: Tento článek popisuje používání doporučení produktů na zařízení v místě prodeje (POS).
author: bebeale
ms.date: 09/08/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.custom: 259664
ms.assetid: 5dd8db08-cd96-4f7e-9e65-b05ca815d580
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 170e2bf18aefc79a796620818c7100ff8e6e689a
ms.sourcegitcommit: f88273627ba105ede27f28fe67ccec2d7f78261c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/09/2022
ms.locfileid: "9460049"
---
# <a name="add-product-recommendations-on-pos"></a>Přidání doporučení produktů v POS

[!include [banner](includes/banner.md)]

Doporučení produktu jsou ve své podstatě transformativní obchodní aplikace, která pokrývá všechny obchodní prostory a vytváří bohaté, poutavé a na míru šité zkušenosti objevování produktů. Chcete-li tuto funkci implementovat do programu POS, postupujte [podle pokynů, jak přidat doporučení na zařízení POS.](add-recommendations-control-pos-screen.md) 

Další informace o funkcích doporučeních produktů naleznete v [přehledu doporučení produktu.](../commerce/product-recommendations.md) 

## <a name="scenarios"></a>Scénáře

Doporučení produktu jsou povolena pro následující scénáře POS. Jsou k dispozici v Cloud POS nebo Modern POS (MPOS).

1. Na stránce **Podrobnosti o produktu**:

    - Pokud obchod asociuje návštěvy se stránkou **Podrobnosti o produktu** při vyhledávání předchozích transakcí napříč různými kanály, služba doporučení navrhuje další položky, které budou pravděpodobně nakoupeny společně. V závislosti na doplňcích pro službu mohou prodejci zobrazit doporučení produktů **Nakupovat podobné produkty** a **Nakupovat podobný popis**, kromě personalizovaných doporučení pro uživatele, kteří mají předchozí historii nákupů.

    [![Doporučení na stránce Podrobnosti produktu.](./media/proddetails.png)](./media/proddetails.png)

2. Na stránce **Transakce**:

    - Modul doporučení navrhuje položky založené na celém seznamu položek v nákupním košíku, které se často nakupují.

    > [!NOTE]
    > Pokud chce maloobchodník zobrazit doporučení na stránce **Transakce**, musí aktualizovat rozložení obrazovky v Dynamics 365 Commerce. Ovládací prvek **Doporučení** musí být na stránce **Transakce**.

    [![Doporučení na stránce Transakce.](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)

## <a name="configure-commerce-to-enable-pos-recommendations"></a>Konfigurace aplikace Commerce pro povolení doporučení POS 

Chcete-li nastavit doporučení produktů, potvrďte, že jste provedli proces poskytování doporučení produktů Commerce podle kroků v části [Aktivace doporučení produktů](../commerce/enable-product-recommendations.md). Ve výchozím nastavení se doporučení zobrazují na stránce **Detaily produktu** i **Detaily zákazníka** poté, co provedete kroky zřizování a data budou úspěšně vytvořena. 

## <a name="add-recommendations-to-the-transaction-screen"></a>Přidání doporučení na obrazovku transakcí

1. Chcete-li přidat doporučení na obrazovku transakce, postupujte podle kroků v části [Přidání doporučení na obrazovku transakce](add-recommendations-control-pos-screen.md).
1. Chcete-li zohlednit změny provedené v návrháři rozvržení obrazovky POS, spusťte úlohu konfigurace kanálu **1070** v Commerce headquarters.

> [!NOTE] 
> Pokud chcete aktivovat doporučení POS pomocí souboru RecoMock s čárkami oddělenými hodnotami (CSV), musíte nasadit soubor CSV do knihovny prostředků Microsoft Dynamics Lifecycle Services (LCS), než nakonfigurujete správce rozložení. Pokud používáte soubor RecoMock CSV, nemusíte doporučení aktivovat. Soubor CSV je k dispozici pouze pro účely ukázky. Doporučuje se pro zákazníky nebo architekty řešení, kteří chtějí napodobit vzhled seznamů doporučení pro účely ukázky, aniž by museli kupovat přídavnou skladovou jednotku (SKU).

## <a name="additional-resources"></a>Další prostředky

[Přehled doporučení produktu](product-recommendations.md)

[Povolení Azure Data Lake Storage v prostředí Dynamics 365 Commerce](enable-adls-environment.md)

[Povolit doporučení produktu](enable-product-recommendations.md)

[Povolení přizpůsobených doporučení](personalized-recommendations.md)

[Odhlášení přizpůsobených doporučení](personalization-gdpr.md)

[Povolit doporučení typu „podobný vzhled“](shop-similar-looks.md)

[Přidání doporučení na obrazovku transakcí](add-recommendations-control-pos-screen.md)

[Úprava výsledků doporučení AI-ML](modify-product-recommendation-results.md)

[Ručně vytvořit uspořádaná doporučení](create-editorial-recommendation-lists.md)

[Vytvořit doporučení s ukázkovými daty](product-recommendations-demo-data.md)

[Často kladené dotazy k doporučení produktu](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
