---
title: Úprava výsledků doporučení produktů na základě umělé inteligence a strojového učení
description: V tomto tématu je vysvětleno, jak přizpůsobovat výsledky doporučení produktu na základě umělé inteligence-strojového učení (AI-ML) pro váš podnik.
author: bebeale
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: dfe04881e71558ed326025d8f2545c3c611df3aa
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796963"
---
# <a name="adjust-ai-ml-based-product-recommendation-results"></a>Úprava výsledků doporučení produktů na základě umělé inteligence a strojového učení


[!include [banner](includes/banner.md)]

V tomto tématu je vysvětleno, jak upravit výsledky doporučení produktu na základě umělé inteligence-strojového učení (AI-ML) pro váš podnik. 

Po povolení doporučení produktu budou výchozí nastavení účinná. Tyto parametry budou nebo mohou fungovat pro mnoho potřeb. Je nejvhodnější naplánovat strávený čas k vyhodnocení, zda výsledky odpovídají prodejnímu pohybu produktů. Před dalším provedením testování navrhujeme vyhodnocení výsledků za několik dní. 

## <a name="understanding-recommendation-list-parameters"></a>Principy parametrů seznamu doporučení

Před změnou parametrů se seznamte s tím, jak ovlivní výsledky níže.

### <a name="trending-product-list"></a>Seznam "trendových" produktů

Seznam "trendových" produktů má dva parametry, které lze změnit:

![Příklad výchozích parametrů seznamu "trendů"](./media/exampletrendingparameters.png)

1. **Zahrnout nové produkty z posledních X dnů** - produkty, které byly přidány do zadaného počtu dnů před aktuálním datem, lze použít k výběru kandidátů produktu. Výchozí hodnota v obrázku naznačuje, že v seznamu produktů pro trend je možné použít produkty v rozmezí 180 dnů.
1. **Zahrnout prodeje z posledních X dnů** - prodejní transakce, které se vyskytly během zadaného počtu dnů před aktuálním datem, lze použít k objednání produktů. Výchozí hodnota výše naznačuje, že k určení umístění produktu v seznamu trendujících produktů se použijí všechny nákupy produktu za posledních 30 dnů. 

### <a name="best-selling-product-list"></a>Seznam "nejlépe prodávaných" produktů

V závislosti na vaší společnosti může seznam "nejlépe prodávaných produktů" vést k jiným výsledkům, než je trend, přestože oba používají data transakcí k objednání produktů. Vzhledem k tomu, že nejlepší prodej nemá žádné přerušení na základě data sortimentu, je možné, že nejlepší prodeje budou stále obsahovat velmi populární starší produkty, které mohly být vyřazeny ze seznamu trendujících produktů. 

Seznam "nejlépe prodávaných" produktů má jeden parametr, který lze změnit:

![Příklad výchozího parametru seznamu nejlépe se prodávajících produktů](./media/examplebestsellingparameters.PNG)

1. **Zahrnout prodeje z posledních X dnů** - prodejní transakce, které se vyskytly během zadaného počtu dnů před aktuálním datem, lze použít k objednání produktů. Výchozí hodnota výše naznačuje, že k určení umístění produktu v seznamu nejlépe se prodávajících produktů se použijí všechny nákupy produktu za posledních 30 dnů. 

## <a name="manually-add-or-remove-products-from-recommendation-lists"></a>Ručně přidat nebo odebrat produkty ze seznamů doporučení

### <a name="for-new-trending-or-best-selling-lists"></a>Pro nové, trendující nebo nejlépe prodávané

1.  Přejděte na **Maloobchod a velkoobchod** > **Doporučení produktů** > **Parametry doporučení**.
1.  V seznamu sdílených parametrů maloobchodního prodeje vyberte **Seznamy doporučení**.
1.  Vyberte seznam, do kterého přidat či z kterého odebrat produkty.
1.  Chcete-li přidat produkty do tabulky, vyberte možnost **Přidat řádek.** 
1.  Ve sloupci produkt vyhledejte produkt podle **názvu** nebo **čísla produktu**.

    ![Příklad hledání produktu v novém seznamu produktů](./media/examplenewlistconfiguration1.png)

1.  Ve sloupci Typ řádku vyberte jednu z následujících možností:
    -   **Zahrnout** – vynutí umístění produkt v předu na seznamu
    -   **Vyloučit** – odebere produkt ze zobrazení v seznamu.
    
    ![Příklad zahrnutí nebo vyloučení produktu z nového seznamu produktů](./media/examplenewlistconfiguration2.png)

1.  Při změně **Pořadí zobrazení** se změní pořadí, v jakém se produkty označené jako **zahrnout** objeví na seznamu.
    - Pokud mají dva produkty stejnou hodnotu **pořadí zobrazení**, pak se konečné pořadí těchto dvou výsledků může lišit od back office.
1.  Odebrání produktů z tabulky: vyberte řádek, který chcete odebrat, a vyberte možnost **Odstranit**.


### <a name="for-people-also-like-or-frequently-bought-together-lists"></a>Pro seznamy Lidem se také líbí a Často zakoupeno společně

V kontextu seznamů Často zakoupeno společně nebo Lidem se také líbí se strojní učení používá k analýze zákaznických vzorů nákupů, které doporučují související produkty často zakoupené společně pro jedinečný produkt typu seed. 
 
*Produkt typu seed* je produkt, pro který chcete generovat výsledky. V kontextu ruční úpravy seznamů doporučení přidáváte nebo odebíráte výsledky pro tento produkt. 

Chcete-li ručně přidat nebo odebrat výsledky pro produkt typu seed, postupujte takto:
1.  Vyberte **Produkt typu seed**. 
1.  Ve sloupci **Produkt** vyhledejte produkt podle **Názvu** nebo **Čísla produktu.**
![Příklad hledání produktu v seznamu Často zakoupeno společně](./media/exampleFBTlistconfiguration1.png)
1. Ve sloupci **Typ řádku** vyberte jednu z následujících možností:
    - **Zahrnout** – vynutí umístění produkt v předu na seznamu
    - **Vyloučit** – odebere produkt ze zobrazení v seznamu.     
![Příklad zahrnutí nebo vyloučení produktu v seznamu Často zakoupeno společně](./media/exampleFBTlistconfiguration2.png)
1.  Odebrání produktů z tabulky: vyberte řádek, který chcete odebrat, a vyberte možnost Odstranit.


## <a name="additional-resources"></a>Další prostředky

[Přehled doporučení produktu](product-recommendations.md)

[Povolení Azure Data Lake Storage v prostředí Dynamics 365 Commerce](enable-adls-environment.md)

[Povolit doporučení produktu](enable-product-recommendations.md)

[Povolení přizpůsobených doporučení](personalized-recommendations.md)

[Odhlášení přizpůsobených doporučení](personalization-gdpr.md)

[Povolit doporučení typu „podobný vzhled“](shop-similar-looks.md)

[Přidání doporučení produktu v POS](product.md)

[Přidání doporučení na obrazovku transakcí](add-recommendations-control-pos-screen.md)

[Ručně vytvořit uspořádaná doporučení](create-editorial-recommendation-lists.md)

[Vytvořit doporučení s ukázkovými daty](product-recommendations-demo-data.md)

[Často kladené dotazy k doporučení produktu](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]