---
title: Správa výsledků doporučení produktů na základě umělé inteligence a strojového učení
description: V tomto tématu je vysvětleno, jak přizpůsobovat výsledky doporučení produktu na základě umělé inteligence-strojového učení (AI-ML) pro váš podnik.
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
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 669b056c38614c8ac9be2d7b244a0ab0c73bc9f8
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770063"
---
# <a name="manage-ai-ml-based-product-recommendation-results"></a>Správa výsledků doporučení produktů na základě umělé inteligence a strojového učení

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

V tomto tématu je vysvětleno, jak přizpůsobovat výsledky doporučení produktu na základě umělé inteligence-strojového učení (AI-ML) pro váš podnik. 

Po povolení doporučení produktu budou výchozí nastavení účinná. Tyto parametry budou nebo mohou fungovat pro mnoho potřeb. Je nejvhodnější naplánovat strávený čas k vyhodnocení, zda výsledky odpovídají prodejnímu pohybu produktů. Před dalším provedením testování navrhujeme vyhodnocení výsledků za několik dní. 

## <a name="understanding-recommendation-list-parameters"></a>Principy parametrů seznamu doporučení

Před změnou parametrů se seznamte s tím, jak ovlivní výsledky níže.

### <a name="trending-product-list"></a>Seznam trendujících produktů

Seznam **Trendujících** produktů obsahuje dva parametry, které lze změnit: ![Příklad nastavení parametrů seznamu trendujíích produktů](./media/exampletrendingparameters.png)
1. **Zahrnout nové produkty z posledních X dnů** - produkty, které byly přidány do zadaného počtu dnů před aktuálním datem, lze použít k výběru kandidátů produktu. Výchozí hodnota v obrázku naznačuje, že v seznamu produktů pro trend je možné použít produkty v rozmezí 180 dnů.
1. **Zahrnout prodeje z posledních X dnů** - prodejní transakce, které se vyskytly během zadaného počtu dnů před aktuálním datem, lze použít k objednání produktů. Výchozí hodnota výše naznačuje, že k určení umístění produktu v seznamu trendujících produktů se použijí všechny nákupy produktu za posledních 30 dnů. 

### <a name="best-selling-product-list"></a>Seznam nejlépe se prodávajících produktů

V závislosti na vaší společnosti může nejlepší prodej vést k různým výsledkům, než je trend, přestože obě používají data transakcí k objednání produktů. Vzhledem k tomu, že nejlepší prodej nemá žádné přerušení na základě data sortimentu, je možné, že nejlepší prodeje budou stále obsahovat velmi populární starší produkty, které mohly být vyřazeny ze seznamu trendujících produktů. 

Seznam **Nejlépe se prodávajících** produktů má jeden parametr, který lze změnit:

![Příklad výchozího parametru seznamu nejlépe se prodávajících produktů](./media/examplebestsellingparameters.PNG)
1. **Zahrnout prodeje z posledních X dnů** - prodejní transakce, které se vyskytly během zadaného počtu dnů před aktuálním datem, lze použít k objednání produktů. Výchozí hodnota výše naznačuje, že k určení umístění produktu v seznamu nejlépe se prodávajících produktů se použijí všechny nákupy produktu za posledních 30 dnů. 

## <a name="manually-add-or-remove-products-from-recommendation-lists"></a>Ručně přidat nebo odebrat produkty ze seznamů doporučení

### <a name="for-new-trending-or-best-selling"></a>Pro nové, trendující nebo nejlépe se prodávající

1.  Přejděte na **Maloobchod** > **Doporučení prouktů** > **Parametry doporučení**.
1.  V seznamu sdílených parametrů maloobchodního prodeje vyberte **Seznamy doporučení**.
1.  Vyberte seznam, do kterého přidat či z kterého odebrat produkty.
1.  Chcete-li přidat produkty do tabulky, vyberte možnost **Přidat řádek.** 
1.  Ve sloupci produkt vyhledejte produkt podle **Názvu** nebo **Čísla produktu**.
![Příklad hledání produktu v seznamu nových produktů](./media/examplenewlistconfiguration1.png)
1.  Ve sloupci Typ řádku vyberte jednu z následujících možností:
    -   **Zahrnout** – vynutí umístění produkt v předu na seznamu
    -   **Vyloučit** – odebere produkt z tohoto seznamu ![Příklad zahrnutí nebo vyloučení produktu z nového seznamu produktů.](./media/examplenewlistconfiguration2.png)
1.  Při změně **Pořadí zobrazení** se změní pořadí, v jakém se produkty označené jako **zahrnout** objeví na seznamu.
    - Pokud mají dva produkty stejnou hodnotu **pořadí zobrazení**, pak se konečné pořadí těchto dvou výsledků může lišit od back office.
1.  Odebrání produktů z tabulky: vyberte řádek, který chcete odebrat, a vyberte možnost **Odstranit**.


### <a name="for-people-also-like-or-frequently-bought-together-lists"></a>Pro seznamy Lidem se také líbí a Často zakoupeno společně

V kontextu seznamů **Často zakoupeno společně** nebo **Lidem se také líbí** se strojní učení používá k analýze zákaznických vzorů nákupů, které doporučují související produkty často zakoupené společně pro jedinečný produkt typu seed. 
 
**Produkt typu seed** je produkt, pro který chcete generovat výsledky. V kontextu ruční úpravy seznamů doporučení přidáváte nebo odebíráte výsledky pro tento produkt. 

Chcete-li ručně přidat nebo odebrat výsledky pro produkt typu seed, postupujte takto:
1.  Vyberte **Produkt typu seed**. 
1.  Ve sloupci **Produkt** vyhledejte produkt podle **Názvu** nebo **Čísla produktu.**
![Příklad hledání produktu v seznamu Často zakoupeno společně](./media/exampleFBTlistconfiguration1.png)
1. Ve sloupci **Typ řádku** vyberte jednu z následujících možností:
    - **Zahrnout** – vynutí umístění produkt v předu na seznamu
    - **Vyloučit** – odebere produkt ze zobrazení v seznamu.     
![Příklad zahrnutí nebo vyloučení produktu v seznamu Často zakoupeno společně](./media/exampleFBTlistconfiguration2.png)
1.  Odebrání produktů z tabulky: vyberte řádek, který chcete odebrat, a vyberte možnost Odstranit.


## <a name="additional-resources"></a>Další zdroje

[Přehled doporučení produktu](product-recommendations.md)

[Povolit doporučení produktu](enable-product-recommendations.md)

[Přidání seznamů doporučení produktu na stránky](add-reco-list-to-page.md)
