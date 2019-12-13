---
title: Povolit doporučení produktu
description: V tomto tématu je vysvětleno, jak vytvořit doporučení produktu založená na strojovém učení na základě umělé inteligence (AI-ML) pro zákazníky Microsoft Dynamics 365 Commerce.
author: bebeale
manager: AnnBe
ms.date: 10/1/2019
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
ms.openlocfilehash: ecda571a356c6968196d09cc19923105cf4544ab
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770132"
---
# <a name="enable-product-recommendations"></a>Povolit doporučení produktu

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

V tomto tématu je vysvětleno, jak vytvořit doporučení produktu založená na strojovém učení na základě umělé inteligence (AI-ML) pro zákazníky Microsoft Dynamics 365 Commerce. Další informace o seznamech doporučených produktů naleznete v tématu [Přehled doporučení produktu](product-recommendations.md).

## <a name="recommendations-pre-check"></a>Předběžná kontrola doporučení
Před povolením berte prosím na vědomí, že doporučení produktů jsou podporována pouze u zákazníků F&O podporujících sestavení 10.0.6, kteří migrovali své úložiště pomocí BDL. 

Dále zkontrolujte, zda byly povoleny ukazatele RetailSale. Další informace o tomto procesu nastavení naleznete [zde.](https://docs.microsoft.com/en-us/dynamics365/ai/customer-insights/pm-measures)


## <a name="turn-on-recommendations"></a>Zapnutí doporučení

Chcete-li zapnout doporučení produktu, postupujte následujícím způsobem.

1. Přejděte na **Maloobchod** &gt; **Doporučení produktů** &gt; **Parametry doporučení**.
1. V seznamu sdílených parametrů maloobchodního prodeje vyberte **Seznamy doporučení**.
1. Nastavte možnost **Povolit doporučení** na **Ano**.

![Povolení doporučení produktu](./media/enableproductrecommendations.png)

> [!NOTE]
> Tento postup spustí proces generování seznamů doporučení produktů. Před tím, než jsou seznamy k dispozici, může uběhnou až několik hodin. Zobrazí se na pokladním místě (POS) nebo v řešení Dynamics 365 for Commerce.

## <a name="configure-recommendation-list-parameters"></a>Konfigurace parametrů seznamu doporučení
Ve výchozím nastavení poskytují seznamy doporučení produktů na bázi AI-ML navrhované hodnoty. Výchozí navrhované hodnoty lze změnit tak, aby vyhovovaly toku vašeho podniku. Další informace o tom, jak změnit výchozí parametry, naleznete v části [Správa výsledků doporučení produktů na základě umělé inteligence a strojového učení](modify-product-recommendation-results.md).

## <a name="show-recommendations-on-pos-devices"></a>Zobrazení doporučení na zařízeních POS
Po povolení doporučení v administrativě je nutné přidat panel doporučení na řídicí obrazovku POS pomocí nástroje pro rozložení. Informace o tomto procesu naleznete [zde.](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/add-recommendations-control-pos-screen)


## <a name="additional-resources"></a>Další zdroje

[Přehled doporučení produktu](product-recommendations.md)

[Přidání seznamů doporučení produktu na stránky](add-reco-list-to-page.md)

[Přidání panelu doporučení do zařízení POS](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/add-recommendations-control-pos-screen)


