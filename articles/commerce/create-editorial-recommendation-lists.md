---
title: Ručně vytvořit uspořádaná doporučení
description: V tomto tématu je vysvětleno, jak mohou manažeři prodeje ručně vytvářet a spravovat seznamy produktů pro zákazníky Microsoft Dynamics 365 Commerce.
author: bebeale
manager: AnnBe
ms.date: 03/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: b39ef61e7dabdd8a53d5666926a95cb7b9e6b9a5
ms.sourcegitcommit: 1e7e7c4bc197b0a42e4d53d2a54600a2fb125b69
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/13/2020
ms.locfileid: "3127714"
---
# <a name="manually-create-curated-recommendations"></a>Ručně vytvořit uspořádaná doporučení

[!include [banner](includes/banner.md)]

V tomto tématu je vysvětleno, jak mohou manažeři prodeje ručně vytvářet a spravovat seznamy doporučení produktů pro zákazníky Microsoft Dynamics 365 Commerce.

Seznamy vybraných produktů jsou kolekce jednotlivých položek obsahu vytvořených a doporučených lidmi.  

## <a name="create-a-new-list"></a>Vytvoření nového seznamu

Chcete-li vytvořit seznam doporučení vybraných produktů, postupujte takto.

1. Přejděte na **Retail and Commerce &gt; Doporučení produktů &gt; Seznamy doporučení**.
1. Zvolte **Nové**.
1. Zadejte hodnotu do pole **ID seznamu**.
1. Zadejte hodnotu do pole **Název seznamu**.
    - **Název seznamu** představuje nadpis seznamu, který se zobrazí v oddílu doporučených seznamů modulu **Kolekce produktů**.
1. Chcete-li přidat produkty do seznamu, vyberte možnost **Přidat produkty**.
1. Chcete-li změnit pořadí produktů v seznamu, zadejte hodnotu do sloupce **Pořadí zobrazení**.
    - Pokud mají dva produkty stejnou hodnotu pořadí zobrazení, pak se konečné pořadí těchto dvou výsledků může lišit od back office.
1. Kliknutím na tlačítko **Uložit** uložte seznam.

## <a name="example-list"></a>Ukázkový seznam

![Ukázkový doporučený seznam v administrativě](./media/examplecuratedrecolist.png)

## <a name="additional-resources"></a>Další prostředky

[Přehled doporučení produktu](product-recommendations.md)

[Povolení ADLS v prostředí Dynamics 365 Commerce](enable-adls-environment.md)

[Povolit doporučení produktu](enable-product-recommendations.md)

[Povolení přizpůsobených doporučení](personalized-recommendations.md)

[Odhlášení přizpůsobených doporučení](personalization-gdpr.md)

[Přidání seznamů doporučení na web e-Commerce](add-reco-list-to-page.md)

[Přidat doporučení produktu v POS](product.md)

[Přidání doporučení na obrazovku transakce](add-recommendations-control-pos-screen.md)

[Úprava výsledků doporučení AI-ML](modify-product-recommendation-results.md)

[Vytvořit doporučení s ukázkovými daty](product-recommendations-demo-data.md)

[Často kladené dotazy k doporučení produktu](faq-recommendations.md)
