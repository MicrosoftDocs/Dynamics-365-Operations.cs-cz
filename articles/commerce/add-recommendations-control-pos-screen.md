---
title: Přidání doporučení na obrazovku transakce
description: Toto téma popisuje, jak přidat ovládací prvek doporučení na obrazovku transakcí na zařízení POS pomocí návrháře rozložení obrazovky v aplikaci Microsoft Dynamics 365 Commerce.
author: bebeale
manager: AnnBe
ms.date: 03/12/20
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailStoreTable, RetailTillLayout
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 9117f398ee1d9edbd3aee9bed366eea225964184
ms.sourcegitcommit: 1e7e7c4bc197b0a42e4d53d2a54600a2fb125b69
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/13/2020
ms.locfileid: "3127668"
---
# <a name="add-recommendations-to-the-transaction-screen"></a>Přidání doporučení na obrazovku transakce

[!include [banner](includes/banner.md)]


Toto téma popisuje, jak přidat ovládací prvek doporučení na obrazovku transakcí na zařízení POS pomocí návrháře rozložení obrazovky v aplikaci Microsoft Dynamics 365 Commerce. Další informace o doporučeních produktů naleznete v dokumentaci [doporučení produktu v dokumentaci POS](product.md).


Když používáte Commerce, můžete zobrazit na svém zařízení POS doporučení produktu. Abyste mohli zobrazit doporučení produktu, musíte přidat ovládací prvek na obrazovce transakce pomocí návrháře rozložení obrazovky. 

## <a name="open-layout-designer"></a>Otevřete návrháře rozložení

1. Přejděte do nabídky **Retail and Commerce** &gt; **Instalace kanálu** &gt; **Nastavení POS** &gt; **POS** &gt; **Rozložení obrazovky**.
2. Pomocí rychlého filtru vyhledejte obrazovku, ke které chcete přidat ovládací prvek. Například použijte filtr na pole **ID rozvržení obrazovky** pomocí hodnoty **F2CP16:9M**.
3. Vyhledejte na seznamu požadovaný záznam a vyberte ho. Vyberte například **Název: F2CP16:9M ID rozvržení obrazovky: F2CP16:9M**.
4. Klikněte na možnost **Návrhář rozložení**.
5. Podle pokynů spusťte návrháře rozložení. Po zobrazení výzvy k zadání přihlašovacích údajů zadejte stejné přihlašovací údaje, které jste použili při spuštění návrháře rozložení ze stránky **Rozložení obrazovky**.
6. Při přihlášení se zobrazí stránka podobná té na obrázku. Rozložení se bude lišit podle přizpůsobení, která jste pro svůj obchod provedli.


    [![Návrhář rozložení](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png)

## <a name="choose-a-display-option"></a>Zvolit zobrazenou možnost

K dispozici jsou dvě možnosti konfigurace. Vyberte možnost, která nejlépe vyhovuje vašemu obchodu, a postupujte podle dalších pokynů k dokončení nastavení ovládacího prvku. Tyto dvě možnosti jsou:

- Doporučení jsou vždy viditelná.
- Karta **Doporučení** se zobrazí v mřížce na pravé straně obrazovky.

### <a name="make-recommendations-always-visible"></a>Nastavení, aby byla doporučení vždy viditelná


1. Zmenšete výšku oblasti podrobností řádků transakce tak, aby byla stejná jako výška panelu odběratele po levé straně.


    [![Snížená výška oblasti podrobností řádků transakce](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)

2. Z nabídky vlevo přetáhněte ovládací prvek doporučení mezi oblast podrobností řádků transakce a mřížku tlačítek uprostřed dolní části obrazovky transakce. Změňte velikost ovládacího prvku tak, aby se vešel do prostoru.

    [![Ovládací prvek doporučení přidaný do rozvržení](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)


3. Návrháře rozložení uložíte a zavřete kliknutím na **X**.
4. V aplikaci Commerce přejděte na **Retail and Commerce** &gt; **IT pro Retail and Commerce** &gt; **Plány distribuce**.
5. V seznamu vyberte možnost **1090, Pokladny**.
6. Klikněte na možnost **Spustit**.


### <a name="add-a-recommendations-tab-to-the-button-grid-on-the-right-side-of-the-screen"></a>Jak přidat kartu Doporučení na mřížku tlačítek na pravé straně obrazovky

1. Klikněte pravým tlačítkem myši do prázdného místa pod poslední kartou na mřížce tlačítek umístěné na pravé straně stránky.

2. Klikněte na tlačítko**přizpůsobit**.

    [![Přizpůsobení – dialogové okno ovládacího prvku karty](./media/pic-5.png)](./media/pic-5.png)

3. Klikněte na možnost **Nová karta**.
4. Najděte novou kartu, kterou jste právě přidali. Možná se budete muset posunout dolů.
5. V rozevíracím seznamu **Obsah** zvolte **Doporučené produkty**.

    [![Zvolení doporučených produktů v poli obsahu](./media/pic-6.png)](./media/pic-6.png)

6. Do pole **Popisek** zadejte název pro kartu doporučení. Zadejte například "Doporučené produkty".
7. V poli **Obrázek** zvolte obrázek, který se zobrazí na kartě.
8. Klikněte na tlačítko **OK**. Nová karta se zobrazí v mřížce tlačítek.
9. Návrháře rozložení uložíte a zavřete kliknutím na **X**.
10. V aplikaci Commerce přejděte na **Retail and Commerce** &gt; **IT pro Retail and Commerce** &gt; **Plány distribuce**.
11. V seznamu vyberte možnost **1090, Pokladny**.
12. Klikněte na možnost **Spustit**.

## <a name="additional-resources"></a>Další prostředky

[Přehled doporučení produktu](product-recommendations.md)

[Povolení ADLS v prostředí Dynamics 365 Commerce](enable-adls-environment.md)

[Povolit doporučení produktu](enable-product-recommendations.md)

[Povolení přizpůsobených doporučení](personalized-recommendations.md)

[Odhlášení přizpůsobených doporučení](personalization-gdpr.md)

[Přidání seznamů doporučení na web e-Commerce](add-reco-list-to-page.md)

[Přidat doporučení produktu v POS](product.md)

[Úprava výsledků doporučení AI-ML](modify-product-recommendation-results.md)

[Ručně vytvořit uspořádaná doporučení](create-editorial-recommendation-lists.md)

[Vytvořit doporučení s ukázkovými daty](product-recommendations-demo-data.md)

[Často kladené dotazy k doporučení produktu](faq-recommendations.md)