---
title: "Přidání ovládacího prvku doporučení na stránku transakce na zařízení POS"
description: "Toto téma popisuje, jak přidat ovládací prvek doporučení na obrazovku transakcí na zařízení POS pomocí návrháře rozložení obrazovky v aplikaci Microsoft Dynamics 365 for Retail."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Operations, Core, UnifiedOperations
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611, Retail Version
ms.translationtype: Human Translation
ms.sourcegitcommit: 52a16be4b07eafb493c7fd7ad52a6d9d1bb9ee89
ms.openlocfilehash: 1cb80decf8ef0f182feec5d4cbe76b37b106dcd2
ms.contentlocale: cs-cz
ms.lasthandoff: 06/20/2017


---

# <a name="add-a-recommendations-control-to-the-transaction-page-on-a-pos-device"></a>Přidání ovládacího prvku doporučení na stránku transakce na zařízení POS

[!include[banner](includes/banner.md)]


Toto téma popisuje, jak přidat ovládací prvek doporučení na obrazovku transakcí na zařízení POS pomocí návrháře rozložení obrazovky v aplikaci Microsoft Dynamics 365 for Retail.

Když používáte Microsoft Dynamics 365 for Retail, můžete zobrazit na svém zařízení POS doporučení produktu. *Doporučení* jsou položky, které mohou vaše zákazníky zajímat na základě jejich historie nákupů, položky v jejich seznamu požadovaných položek a položky, které jiní zákazníci nakoupili online nebo v kamenných obchodech. Abyste mohli zobrazit doporučení produktu, musíte přidat ovládací prvek na obrazovce transakce pomocí návrháře rozložení obrazovky.

## <a name="open-layout-designer"></a>Otevřete návrháře rozložení
1.  Přejděte do nabídky **Maloobchod** &gt; **Instalace kanálu** &gt; **Nastavení POS** &gt; **POS** &gt; **Rozložení obrazovky**.
2.  Pomocí rychlého filtru vyhledejte obrazovku, ke které chcete přidat ovládací prvek. Například použijte filtr na pole **ID rozvržení obrazovky** pomocí hodnoty F2CP16:9M.
3.  Vyhledejte na seznamu požadovaný záznam a vyberte ho. Vyberte například Název: F2CP16:9M ID rozvržení obrazovky: F2CP16:9M.
4.  Klikněte na možnost **Návrhář rozložení**.
5.  Podle pokynů spusťte návrháře rozložení. Po zobrazení výzvy k zadání přihlašovacích údajů zadejte stejné přihlašovací údaje, které jste použili při spuštění návrháře rozložení ze stránky **Rozložení obrazovky**.
6.  Při přihlášení se zobrazí stránka podobná té na obrázku. Rozložení se bude lišit podle přizpůsobení, která jste pro svůj obchod provedli.

[![screenlayout-pic-1](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png) Zvolte možnost zobrazení
-----------------------

K dispozici jsou dvě možnosti konfigurace. Vyberte možnost, která nejlépe vyhovuje vašemu obchodu, a postupujte podle dalších pokynů k dokončení nastavení ovládacího prvku. Tyto dvě možnosti jsou:
-   Doporučení jsou vždy viditelná.
-   Karta **Doporučení** se zobrazí v mřížce na pravé straně obrazovky.

#### <a name="to-make-recommendations-always-visible"></a>Jak udělat, aby byla doporučení vždy viditelná

1.  Zmenšete výšku oblasti podrobností řádků transakce tak, aby byla stejná jako výška panelu odběratele po levé straně.[](./media/pic-2.png)[![screenlayout-pic-2](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)
2.  Z nabídky vlevo přetáhněte ovládací prvek doporučení mezi oblast podrobností řádků transakce a mřížku tlačítek uprostřed dolní části obrazovky transakce. Změňte velikost ovládacího prvku tak, aby se vešel do prostoru.[](./media/pic-3.png)[![screenlayout-pic-3](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)
3.  Návrháře rozložení uložíte a zavřete kliknutím na **X**.
4.  V aplikaci Dynamics 365 for Retail přejděte na **Maloobchod** &gt; **IT pro maloobchod** &gt; **Plány distribuce**.
5.  V seznamu vyberte možnost **1090, Pokladny**.
6.  Klikněte na možnost **Spustit**.

#### <a name="to-add-a-recommendations-tab-to-the-button-grid-on-the-right-side-of-the-screen"></a>Jak přidat kartu Doporučení na mřížku tlačítek na pravé straně obrazovky

1.  Klikněte pravým tlačítkem myši do prázdného místa pod poslední kartou na mřížce tlačítek umístěné na pravé straně stránky.
2.  Klikněte na **Přizpůsobit**.[![pic-5](./media/pic-5.png)](./media/pic-5.png)
3.  Klikněte na možnost **Nová karta**.
4.  Najděte novou kartu, kterou jste právě přidali. Možná se budete muset posunout dolů.
5.  V rozevíracím seznamu **Obsah** zvolte **Doporučené produkty**. [![pic-6](./media/pic-6.png)](./media/pic-6.png)
6.  Do pole **Popisek** zadejte pro kartu doporučení. Například zadejte Doporučené produkty.
7.  V poli **Obrázek** zvolte obrázek, který se zobrazí na kartě.
8.  Klikněte na tlačítko **OK**. Nová karta se zobrazí v mřížce tlačítek.
9.  Návrháře rozložení uložíte a zavřete kliknutím na **X**.
10. V aplikaci Dynamics 365 for Retail přejděte na **Maloobchod** &gt; **IT pro maloobchod** &gt; **Plány distribuce**.
11. V seznamu vyberte možnost **1090, Pokladny**.
12. Klikněte na možnost **Spustit**.


<a name="see-also"></a>Viz také
--------

[Přehled přizpůsobených doporučení produktu](personalized-product-recommendations.md)




