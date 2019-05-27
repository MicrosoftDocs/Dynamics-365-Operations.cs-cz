---
title: Přidání ovládacího prvku doporučení na obrazovku transakce na zařízeních POS
description: Toto téma popisuje, jak přidat ovládací prvek doporučení na obrazovku transakcí na zařízení POS pomocí návrháře rozložení obrazovky v aplikaci Microsoft Dynamics 365 for Retail.
author: ashishmsft
manager: AnnBe
ms.date: 02/05/2018
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
ms.openlocfilehash: 213b47422a5e31c2cfc2d173b8c7d9efdecc7568
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1573365"
---
# <a name="add-a-recommendations-control-to-the-transaction-screen-on-pos-devices"></a>Přidání ovládacího prvku doporučení na obrazovku transakce na zařízeních POS

[!include [banner](includes/banner.md)]

> [!NOTE]
> Aktuální verzi služby doporučení produktu odstraňujeme, protože předěláváme tuto funkci s lepším algoritmem a novějšími funkčnostmi orientovanými na maloobchod. Další informace naleznete v části [Odstraněné nebo zastaralé funkce](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/migration-upgrade/deprecated-features).

Toto téma popisuje, jak přidat ovládací prvek doporučení na obrazovku transakcí na zařízení POS pomocí návrháře rozložení obrazovky v aplikaci Microsoft Dynamics 365 for Retail.

Když používáte Microsoft Dynamics 365 for Retail, můžete zobrazit na svém zařízení POS doporučení produktu. *Doporučení* jsou položky, které mohou vaše zákazníky zajímat na základě jejich historie nákupů, položky v jejich seznamu požadovaných položek a položky, které jiní zákazníci nakoupili online nebo v kamenných obchodech. Abyste mohli zobrazit doporučení produktu, musíte přidat ovládací prvek na obrazovce transakce pomocí návrháře rozložení obrazovky.

## <a name="open-layout-designer"></a>Otevřete návrháře rozložení

1. Přejděte do nabídky **Maloobchod** &gt; **Instalace kanálu** &gt; **Nastavení POS** &gt; **POS** &gt; **Rozložení obrazovky**.
2. Pomocí rychlého filtru vyhledejte obrazovku, ke které chcete přidat ovládací prvek. Například použijte filtr na pole **ID rozvržení obrazovky** pomocí hodnoty F2CP16:9M.
3. Vyhledejte na seznamu požadovaný záznam a vyberte ho. Vyberte například "Název: F2CP16:9M ID rozvržení obrazovky: F2CP16:9M".
4. Klikněte na možnost **Návrhář rozložení**.
5. Podle pokynů spusťte návrháře rozložení. Po zobrazení výzvy k zadání přihlašovacích údajů zadejte stejné přihlašovací údaje, které jste použili při spuštění návrháře rozložení ze stránky **Rozložení obrazovky**.
6. Při přihlášení se zobrazí stránka podobná té na obrázku. Rozložení se bude lišit podle přizpůsobení, která jste pro svůj obchod provedli.

    [![screenlayout-pic-1](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png)

## <a name="choose-a-display-option"></a>Zvolit zobrazenou možnost

K dispozici jsou dvě možnosti konfigurace. Vyberte možnost, která nejlépe vyhovuje vašemu obchodu, a postupujte podle dalších pokynů k dokončení nastavení ovládacího prvku. Tyto dvě možnosti jsou:

- Doporučení jsou vždy viditelná.
- Karta **Doporučení** se zobrazí v mřížce na pravé straně obrazovky.

### <a name="make-recommendations-always-visible"></a>Nastavení, aby byla doporučení vždy viditelná

1. Zmenšete výšku oblasti podrobností řádků transakce tak, aby byla stejná jako výška panelu odběratele po levé straně.

    [![screenlayout-pic-2](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)

2. Z nabídky vlevo přetáhněte ovládací prvek doporučení mezi oblast podrobností řádků transakce a mřížku tlačítek uprostřed dolní části obrazovky transakce. Změňte velikost ovládacího prvku tak, aby se vešel do prostoru.

    [![screenlayout-pic-3](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)

3. Návrháře rozložení uložíte a zavřete kliknutím na **X**.
4. V aplikaci Dynamics 365 for Retail přejděte do **Maloobchod** &gt; **IT pro maloobchod** &gt; **Plány distribuce**.
5. V seznamu vyberte možnost  **1090, Pokladny**.
6. Klikněte na možnost **Spustit**.

### <a name="add-a-recommendations-tab-to-the-button-grid-on-the-right-side-of-the-screen"></a>Jak přidat kartu Doporučení na mřížku tlačítek na pravé straně obrazovky

1. Klikněte pravým tlačítkem myši do prázdného místa pod poslední kartou na mřížce tlačítek umístěné na pravé straně stránky.
2. Klepněte na tlačítko **přizpůsobit**.

    [![pic-5](./media/pic-5.png)](./media/pic-5.png)

3. Klikněte na možnost **Nová karta**.
4. Najděte novou kartu, kterou jste právě přidali. Možná se budete muset posunout dolů.
5. V rozevíracím seznamu **Obsah** zvolte **Doporučené produkty**.

    [![pic-6](./media/pic-6.png)](./media/pic-6.png)

6. Do pole **Popisek** zadejte název pro kartu doporučení. Zadejte například "Doporučené produkty".
7. V poli **Obrázek** zvolte obrázek, který se zobrazí na kartě.
8. Klepněte na tlačítko **OK**. Nová karta se zobrazí v mřížce tlačítek.
9. Návrháře rozložení uložíte a zavřete kliknutím na **X**.
10. V aplikaci Dynamics 365 for Retail přejděte do **Maloobchod** &gt; **IT pro maloobchod** &gt; **Plány distribuce**.
11. V seznamu vyberte možnost  **1090, Pokladny**.
12. Klikněte na možnost **Spustit**.

## <a name="additional-resources"></a>Další zdroje

[Přehled doporučení přizpůsobeného produktu](personalized-product-recommendations.md)
