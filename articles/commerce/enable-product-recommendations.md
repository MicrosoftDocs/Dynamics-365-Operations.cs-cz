---
title: Povolit doporučení produktu
description: V tomto tématu je vysvětleno, jak vytvořit doporučení produktu založená na strojovém učení na základě umělé inteligence (AI-ML) pro zákazníky Microsoft Dynamics 365 Commerce.
author: bebeale
manager: AnnBe
ms.date: 03/19/2020
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
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: d8a579be5df3c5e7718a6fb4720341f3bd01a64c
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/21/2020
ms.locfileid: "3154406"
---
# <a name="enable-product-recommendations"></a>Povolit doporučení produktu

[!include [banner](includes/banner.md)]

V tomto tématu je vysvětleno, jak vytvořit doporučení produktu založená na strojovém učení na základě umělé inteligence (AI-ML) pro zákazníky Microsoft Dynamics 365 Commerce. Další informace o seznamech doporučených produktů naleznete v tématu [Přehled doporučení produktu](product-recommendations.md).

## <a name="recommendations-pre-check"></a>Předběžná kontrola doporučení

Před povolením berte prosím na vědomí, že doporučení produktů jsou podporována pouze u zákazníků Commerce, kteří migrovali své úložiště pomocí Azure Data Lake Storage (ADLS). 

Postup při povolení ADLS naleznete v tématu [Jak povolit ADLS v prostředí Dynamics 365](enable-ADLS-environment.md).

Dále zkontrolujte, zda byly povoleny ukazatele RetailSale. Další informace o tomto procesu nastavení naleznete [zde.](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures)


## <a name="turn-on-recommendations"></a>Zapnutí doporučení

Chcete-li zapnout doporučení produktu, postupujte následujícím způsobem.

1. Přejděte na **Retail a Commerce &gt; Doporučení produktů &gt; Parametry doporučení**.
1. V seznamu sdílených parametrů maloobchodního prodeje vyberte **Seznamy doporučení**.
1. Nastavte možnost **Povolit doporučení** na **Ano**.

![Povolení doporučení produktu](./media/enableproductrecommendations.png)

> [!NOTE]
> Tento postup spustí proces generování seznamů doporučení produktů. Před tím, než jsou seznamy k dispozici, může uběhnou až několik hodin. Zobrazí se na pokladním místě (POS) nebo v řešení Dynamics 365 Commerce.

## <a name="configure-recommendation-list-parameters"></a>Konfigurace parametrů seznamu doporučení

Ve výchozím nastavení poskytují seznamy doporučení produktů na bázi AI-ML navrhované hodnoty. Výchozí navrhované hodnoty lze změnit tak, aby vyhovovaly toku vašeho podniku. Další informace o tom, jak změnit výchozí parametry, naleznete v části [Správa výsledků doporučení produktů na základě umělé inteligence a strojového učení](modify-product-recommendation-results.md).

## <a name="show-recommendations-on-pos-devices"></a>Zobrazení doporučení na zařízeních POS

Po povolení doporučení v administrativě Commerce je nutné přidat panel doporučení na řídicí obrazovku POS pomocí nástroje pro rozložení. Více o tomto procesu se dozvíte v části [Přidání ovládacího prvku doporučení na obrazovku transakce na zařízeních POS](add-recommendations-control-pos-screen.md). 

## <a name="enable-personalized-recommendations"></a>Povolení přizpůsobených doporučení

Další informace o získání přizpůsobených doporučení získáte v tématu [Povolení přizpůsobených doporučení produktů](personalized-recommendations.md).

## <a name="additional-resources"></a>Další prostředky

[Přehled doporučení produktu](product-recommendations.md)

[Povolení ADLS v prostředí Dynamics 365 Commerce](enable-adls-environment.md)

[Povolení přizpůsobených doporučení](personalized-recommendations.md)

[Odhlášení přizpůsobených doporučení](personalization-gdpr.md)

[Přidat doporučení produktu v POS](product.md)

[Přidání doporučení na obrazovku transakce](add-recommendations-control-pos-screen.md)

[Úprava výsledků doporučení AI-ML](modify-product-recommendation-results.md)

[Ručně vytvořit uspořádaná doporučení](create-editorial-recommendation-lists.md)

[Vytvořit doporučení s ukázkovými daty](product-recommendations-demo-data.md)

[Často kladené dotazy k doporučení produktu](faq-recommendations.md)

