---
title: "Přehled produktu individuální doporučení"
description: "Ve 365 Dynamics pro operace je možné zobrazit doporučení ohledně produktů v okamžiku prodeje (POS) zařízení. Doporučení jsou položky, které zákazník může zajímat na základě jejich historie nákupů, položek v seznamu jejich přání a položky, které ostatní zákazníci zakoupili online a v cihel a Malty obchody. Pro maloobchody s velkým katalogy doporučení zákazníkovi pomoci s zjišťování produktu. Předvádějící nejlepší produkty, které jsou zaměřeny na zájmy zákazníka a nákupních zvyklostech, doporučení produktu pomáhá maloobchodníkům se nahoru zákazník a zákazník více a mohou zlepšit uchovávání informací zákazníka. V 365 Dynamics pro operace jsou napájeny doporučení produktu kognitivních služeb a Microsoft Azure machine learning."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 259664
ms.assetid: 5dd8db08-cd96-4f7e-9e65-b05ca815d580
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: af1f4ba1ed5efe0e35d08d37d09e7ada4a4c1b7a
ms.lasthandoff: 03/31/2017


---

# <a name="personalized-product-recommendations-overview"></a>Přehled produktu individuální doporučení

[!include[banner](includes/banner.md)]


Ve 365 Dynamics pro operace je možné zobrazit doporučení ohledně produktů v okamžiku prodeje (POS) zařízení. Doporučení jsou položky, které zákazník může zajímat na základě jejich historie nákupů, položek v seznamu jejich přání a položky, které ostatní zákazníci zakoupili online a v cihel a Malty obchody. Pro maloobchody s velkým katalogy doporučení zákazníkovi pomoci s zjišťování produktu. Předvádějící nejlepší produkty, které jsou zaměřeny na zájmy zákazníka a nákupních zvyklostech, doporučení produktu pomáhá maloobchodníkům se nahoru zákazník a zákazník více a mohou zlepšit uchovávání informací zákazníka. V 365 Dynamics pro operace jsou napájeny doporučení produktu kognitivních služeb a Microsoft Azure machine learning.

<a name="scenarios"></a>Scénáře
---------

Doporučení produktu jsou povoleny pro následující scénáře POS. Jsou k dispozici v cloudu Retail POS nebo moderní POS (MPOS).

1.  V **podrobnosti o produktu** stránky:

-   Pokud úložiště spojení návštěvy **podrobnosti o produktu** jsou stránky, když se dívá na předchozí transakce napříč různými kanály motoru doporučení navrhuje další položky mohou být zakoupeny společně.
-   Pokud přidružení úložiště přidá zákazníka k transakci a poté navštíví **podrobnosti o produktu** stránce doporučení motoru poskytuje individuální doporučení prostřednictvím historie transakcí zákazníka.

[![proddetails](./media/proddetails.png)](./media/proddetails.png)

2.  V **transakce** stránky:

-   Motor doporučení navrhuje položky založené na celý seznam položek v košíku.
-   Pokud přidružení úložiště přidá k transakci zákazníka, doporučení motoru poskytuje osobní doporučení pomocí historie transakcí zákazníka a seznamu položek v nákupním košíku.

**Poznámka:** zobrazení doporučení na **transakce** stránky, prodejce potřebuje aktualizovat rozvržení obrazovky v 365 Dynamics pro operace. **Doporučení** ovládacího prvku musí zavěsit k **transakce** stránky. [![transactionscreenmultipleproductslargemessengersbag-5](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)

3.  Na **podrobnosti o odběrateli** stránky:
    -   Motor doporučení navrhuje položky založené na ID uživatele a položky v seznamu přání zákazníka.

[![customerdetailsrecommendations](./media/customerdetailsrecommendations.png)](./media/customerdetailsrecommendations.png)

## <a name="configure-dynamics-365-for-operations-to-enable-pos-recommendations"></a>Konfigurace Dynamics 365 pro operace povolit doporučení POS
Nastavit doporučení produktu, musíte proveďte následující kroky.

1.  Ujistěte se, zda jste vybrali správný **právnické osoby**.
2.  Přejděte do **Entity úložiště**, vyberte **maloobchodní prodej**a potom klepněte na tlačítko **aktualizace**. ** ** to použít ukázková data (nebo data) z provozní databáze a přesunout do úložiště entita.
3.  Volitelné: Chcete-li zobrazit doporučení na obrazovce transakce, přejděte na ** rozvržení obrazovky **zvolit rozložení obrazovky, snadné spuštění **návrháře rozvržení obrazovky**,** ** a potom umístěte ** doporučení kontroly ** v případě potřeby.
4.  Přejít na **parametry programu Retail**, vyberte **strojovém učení**, vyberte ** Ano ** v **POS povolit doporučení**.
5.  Doporučení na POS zobrazíte globální konfigurační úlohu spustit **1110**. Tak, aby odrážely provedené změny návrháře rozvržení obrazovky POS, spuštění úlohy konfigurace kanálu **1070**.

## <a name="how-does-it-work"></a>[]()Jak to funguje?
Pokud aktualizujete **Entity úložiště** entity následující akce konat.

-   Data ve formátu podle kognitivních služeb je extrahován z 365 Dynamics pro operace pracovní databáze a odeslána do obchodu Entity.
-   Data slouží k vyčištění dat pomocí skriptů podregistr jako součást činností ADF pomocí Azure Data Factory (ADF). Vyčištěny data jsou uložena do úložiště objektů blob.
-   Data z úložiště objektů blob slouží rozhraní API kognitivních služeb k doporučení model vlaku.

Při zapnutí **povolit doporučení** a spuštění úloh konfigurace, uplatněny následující akce.

-   Vzor pověření ID nastupují z rozhraní API a uloženy v 365 Dynamics pro operace pracovní databáze, v souboru web.config pro server AOS a také server maloobchodu.
-   Vzor pověření a ID jsou k dispozici na CRT tak, aby volání doporučení produktu z cloudu POS a MPOS v režimu online můžete dodržet.


<a name="see-also"></a>Viz také
--------

[Přidání ovládacího prvku doporučení na stránku transakce na POS zařízení](add-recommendations-control-pos-screen.md)




