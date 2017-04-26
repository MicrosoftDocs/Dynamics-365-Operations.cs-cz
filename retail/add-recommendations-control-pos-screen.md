---
title: "Přidání ovládacího prvku doporučení na stránku transakce na POS zařízení"
description: "Toto téma popisuje, jak přidat ovládací prvek doporučení na místa prodeje (POS) zařízení pomocí návrháře rozvržení obrazovky v Microsoft Dynamics 365 pro operace na obrazovce transakce."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 2377b1639a3c95fe6bba4754c4069cc12043e3d3
ms.lasthandoff: 03/31/2017


---

# <a name="add-a-recommendations-control-to-the-transaction-page-on-a-pos-device"></a>Přidání ovládacího prvku doporučení na stránku transakce na POS zařízení

[!include[banner](includes/banner.md)]


Toto téma popisuje, jak přidat ovládací prvek doporučení na místa prodeje (POS) zařízení pomocí návrháře rozvržení obrazovky v Microsoft Dynamics 365 pro operace na obrazovce transakce.

Doporučení produktu můžete zobrazit v zařízení POS při použití Microsoft Dynamics 365 pro operace. *Doporučení* jsou položky, které zákazník může zajímat na základě jejich historie nákupů, položek v seznamu jejich přání a položky, které ostatní zákazníci zakoupili online a v cihel a Malty obchody. Zobrazit doporučení produktu, musíte přidat ovládací prvek na obrazovce transakce pomocí návrháře rozvržení obrazovky.

## <a name="open-layout-designer"></a>Otevřete návrháře rozvržení
1.  Přejít na **maloobchodní a commerce**&gt;**nastavení kanálu**&gt;**instalace POS**&gt;**POS**&gt;**rozložení obrazovky**.
2.  Pomocí filtru rychlého hledání, kterou chcete přidat ovládací prvek na obrazovce. Například filtr na **ID rozvržení obrazovky** pole pomocí hodnoty "F2CP16:9M".
3.  Vyhledejte na seznamu požadovaný záznam a vyberte ho. Vyberte například "název: F2CP16:9M ID rozvržení obrazovky: F2CP16:9M".
4.  Klepněte na tlačítko **návrháře rozvržení**.
5.  Podle pokynů spusťte návrháře rozvržení. Po zobrazení výzvy k zadání pověření, zadejte stejná pověření, které se používaly při návrháře rozvržení byl spuštěn z **na obrazovce rozložení** stránky.
6.  Při přihlášení, zobrazí se stránka podobná té na obrázku. Rozložení se bude lišit podle vlastního nastavení, které byly provedeny pro svůj obchod.

[![screenlayout-pic-1](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png) zvolte volbu zobrazení
-----------------------

K dispozici jsou dvě možnosti konfigurace. Vyberte možnost, která nejlépe vyhovuje pro svůj obchod a postupujte podle pokynů a dokončete nastavení ovládacího prvku. Jsou dvě možnosti:
-   Doporučení jsou vždy viditelné.
-   A **doporučení** karta se zobrazí v mřížce na pravé straně obrazovky.

#### <a name="to-make-recommendations-always-visible"></a>Chcete-li vždy zobrazit doporučení

1.  Zmenšete výšku oblasti podrobností řádků transakce tak, aby stejné výšky jako zákazníka panel po levé straně. [](./media/pic-2.png)[![screenlayout-pic-2](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)
2.  Z nabídky vlevo přetáhněte a umístěte doporučení ovládací prvek mezi oblasti Podrobnosti řádku transakce a mřížky tlačítko uprostřed dolní části obrazovky transakce. Změnit velikost ovládacího prvku tak, aby se vešel do prostoru. [](./media/pic-3.png)[![screenlayout-pic-3](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)
3.  Klepněte **X** uložit a ukončit návrháře rozvržení.
4.  V 365 Dynamics pro operace, přejděte na **maloobchodní a commerce**&gt;**Retail IT**&gt;**plány distribuce**.
5.  V seznamu, vyberte **registruje 1090**.
6.  Klepněte na tlačítko **nyní spustit**.

#### <a name="to-add-a-recommendations-tab-to-the-button-grid-on-the-right-side-of-the-screen"></a>Chcete-li přidat kartu doporučení k mřížce tlačítka na pravé straně obrazovky

1.  Klepněte pravým tlačítkem myši prázdné místo pod poslední kartu na mřížce tlačítko umístěné na pravé straně stránky.
2.  Klepněte na **vlastní**. [![pic-5](./media/pic-5.png)](./media/pic-5.png)
3.  Klepněte na tlačítko **nová karta**.
4.  Najděte novou kartu, kterou jste právě přidali. Potřebujete Posun dolů.
5.  V **obsahu** rozevíracího seznamu, vyberte **doporučené produkty**. [![PIC-6](./media/pic-6.png)](./media/pic-6.png)
6.  V **popisek** pole, zadejte název pro kartu doporučení. Například zadejte "Doporučené produkty".
7.  V **obraz** vyberte obrázek, který se zobrazí na kartě.
8.  Click **OK**. Mřížky se zobrazí nová karta.
9.  Klepněte **X** uložit a ukončit návrháře rozvržení.
10. V 365 Dynamics pro operace, přejděte na **maloobchodní a commerce**&gt;**Retail IT**&gt;**plány distribuce**.
11. V seznamu, vyberte **registruje 1090**.
12. Klepněte na tlačítko **nyní spustit**.


<a name="see-also"></a>Viz také
--------

[Přehled produktu individuální doporučení](personalized-product-recommendations.md)




