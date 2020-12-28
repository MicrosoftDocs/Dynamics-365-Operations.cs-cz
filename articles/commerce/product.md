---
title: Přidání doporučení produktů v POS
description: Toto téma popisuje používání doporučení produktů na zařízení v místě prodeje (POS).
author: bebeale
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 259664
ms.assetid: 5dd8db08-cd96-4f7e-9e65-b05ca815d580
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 7afe9225b8fc966ca154a5eb7421e8d4cc7c3023
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4410893"
---
# <a name="add-product-recommendations-on-pos"></a>Přidání doporučení produktů v POS

[!include [banner](includes/banner.md)]

Doporučení produktu jsou ve své podstatě transformativní obchodní aplikace, která pokrývá všechny obchodní prostory a vytváří bohaté, poutavé a na míru šité zkušenosti objevování produktů. Chcete-li tuto funkci implementovat do programu POS, postupujte [podle pokynů, jak přidat doporučení na zařízení POS.](add-recommendations-control-pos-screen.md) 

Další informace o funkcích doporučeních produktů naleznete v [přehledu doporučení produktu.](../commerce/product-recommendations.md) 

## <a name="scenarios"></a>Scénáře

Doporučení produktu jsou povolena pro následující scénáře POS. Jsou k dispozici v Cloud POS nebo Modern POS (MPOS).

1. Na stránce **Podrobnosti o produktu**:

    - Pokud obchod asociuje návštěvy se stránkou **Podrobnosti o produktu** při vyhledávání předchozích transakcí napříč různými kanály, služba doporučení navrhuje další položky, které budou pravděpodobně nakoupeny společně.

    [![Doporučení na stránce Podrobnosti produktu](./media/proddetails.png)](./media/proddetails.png)

2. Na stránce **Transakce**:

    - Modul doporučení navrhuje položky založené na celém seznamu položek v nákupním košíku, které se často nakupují.

    > [!NOTE]
    > Pokud chce maloobchodník zobrazit doporučení na stránce **Transakce**, musí aktualizovat rozložení obrazovky v Dynamics 365 Commerce. Ovládací prvek **Doporučení** musí být na stránce **Transakce**.

    [![Doporučení na stránce Transakce](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)

## <a name="configure-commerce-to-enable-pos-recommendations"></a>Konfigurace aplikace Commerce pro povolení doporučení POS

Chcete-li nastavit doporučení produktu, postupujte následujícím způsobem:

1. Zkontrolujte, zda byla služba aktualizována v sestavení **10.0.6.**
2. Postupujte podle pokynů pro [povolení doporučení produktu](../commerce/enable-product-recommendations.md) pro váš podnik.
3. Volitelné: Chcete-li zobrazit doporučení na obrazovce transakce, přejděte na **Rozvržení obrazovky**, zvolte rozložení obrazovky, spusťte **Návrhář rozvržení obrazovky**, a potom umístěte ovládací prvek **doporučení**, kam je třeba.
4. Přejděte na **Parametry velkoobchodu**, vyberte **Strojové učení** a vyberte **Ano** v části **Povolit doporučení POS**.
5. Doporučení na POS zobrazíte spuštěním globální konfigurační úlohy **1110**. Aby se změny návrháře rozvržení obrazovky POS projevily, spusťte úlohu konfigurace kanálu **1070**.

## <a name="troubleshoot-issues-where-you-have-product-recommendations-already-enabled"></a>Řešení problémů, když máte doporučení produktu již povolena

- Přejděte na **Parametry velkoobchodu** \> **Seznam doporučení** \> **Zakázat doporučení produktu** a spusťte **globální konfigurační úlohu \[9999\]**. 
- Pokud jste přidali **Řízení doporučení** na svou obrazovku transakcí pomocí nástroje **Návrhář rozložení obrazovky**, odstraňte ho také.
- Máte-li další dotazy, vyhledejte další informace [v nejčastějších dotazech k doporučením produktu](../commerce/faq-recommendations.md).

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
