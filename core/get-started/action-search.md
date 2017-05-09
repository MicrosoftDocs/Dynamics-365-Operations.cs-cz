---
title: "Hledání akce"
description: "Tento článek popisuje funkci hledání akce v aplikaci Microsoft Dynamics 365 for Operations. Hledání akce vám pomůže najít a spustit akce na stránce."
author: jasongre
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 62303
ms.assetid: 62c70de0-fdde-4417-8e08-0583fb095a40
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 4bb647cfd3f012efbffa93a81462c538a24ac850
ms.openlocfilehash: 689d8f9fb0501c5007db21d41f126737af77b89e
ms.lasthandoff: 03/31/2017


---

# <a name="action-search"></a>Hledání akce

[!include[banner](../includes/banner.md)]


Tento článek popisuje funkci hledání akce v aplikaci Microsoft Dynamics 365 for Operations. Hledání akce vám pomůže najít a spustit akce na stránce.

<a name="introduction"></a>Úvod
------------

Stránky v aplikaci Microsoft Dynamics 365 for Operations vystavují příkazy v podoknech akcí, standardním podokně akcí, které se zobrazí v horní části stránky, a na panelech nástrojů, které se zobrazují v různých částech stránky. V předchozích verzích aplikace Dynamics AX umožňovala funkce Klíčové tipy rychlý přístup k libovolnému tlačítku v podokně akcí stisknutím klávesy Alt a řady čísel. 

[![keyTipsAX6](./media/keytipsax6.png)](./media/keytipsax6.png) V aktuální verzi aplikace Dynamics 365 for Operations nejsou tipy ke klávesám dále dostupné, ale byly nahrazeny funkcí vyhledávání akce. Nová funkce vám umožňuje rychle vyhledat a spustit tlačítko z jakéhokoli viditelného podokna akcí.

## <a name="using-action-search"></a>Použití hledání akcí
Chcete-li použít funkci hledání akce, postupujte takto.

1.  V podokně akcí, klepněte na pole **vyhledávání akcí**. (Pole **vyhledávání akcí** obsahuje ikonu lupy.)
2.  Zadejte část nebo celý název tlačítka, které chcete spustit. Můžete také hledat pomocí slov z „cesty“ k tlačítku. (Další informace o najdete v další části tohoto článku.) Obvykle se tlačítka se zobrazí v horní části seznamu výsledků poté, co zadáte dva až čtyři znaky.
3.  Najděte a spusťte tlačítko v seznamu výsledků (pomocí myši nebo klávesnice).

Po spuštění tlačítka bude výběr vrácen do vaší poslední pozice na stránce tak, abyste mohli pokračovat v práci. 

[![action-search-field](./media/action-search-field.png)](./media/action-search-field.png)

Vyhledávání akcí také spustíte stisknutím kláves Ctrl +/ nebo Alt + Q. Stiskněte klávesovou zkratku ještě jednou, chcete-li se vrátit na výběr do vaší poslední pozice na stránce.

## <a name="understanding-the-results-list"></a>Vysvětlivky k seznamu výsledků
Často v aplikaci 365 for Operations musíte znát umístění i kontext tlačítka, abyste plně porozuměli účelu daného tlačítka. Proto se zobrazují další informace pro každou položku v seznamu výsledků, které vám pomohou přesně pochopit, která tlačítka se zobrazí v seznamu. Zejména se zobrazí "cesta" tlačítka. Tato cesta může obsahovat popisky tyto prvky uživatelského rozhraní odpovídajícím způsobem:

-   Karta podokno akcí
-   Skupina tlačítek
-   Tlačítko nabídky (pokud je tlačítko uvnitř tlačítka nabídky)
-   Oddělovač nabídky (pokud tlačítko je v pojmenované skupině v rámci tlačítka nabídky)
-   Skupina nebo karta na stránce (například název pevné záložky)

Předpokládejme například, že jste zadali výraz **cel** do pole **vyhledávání akcí** a nyní prověřujete seznam výsledků. První položka u tlačítek, která má název **Celkem**, je zvýrazněna. Rovněž je zobrazena cesta tlačítka **Prodejní objednávka** &gt; **Zobrazení**. Část **Prodejní objednávka** odpovídá cestě na kartu **Prodejní objednávka** v podokně akcí a část **Zobrazení** odpovídá cestě do skupiny **Zobrazení** na této kartě. Podobně cesta k tlačítku **Celková sleva** (**Prodej**&gt;**Vypočítat**) informuje o tom, že toto tlačítko se nachází ve skupině **Vypočítat** na kartě **Prodej** v podokně akcí. Z toho vyplývá, že tyto informace vám pomohou pochopit, které tlačítko bude přesně vyvoláno vyhledáním akce (pokud ho vyberete v podokně výsledků). 

[![action-search-field-with-data](./media/action-search-field-with-data.png)](./media/action-search-field-with-data.png) 

V předchozím příkladu vyhledávání akce ukázalo výsledky ze standardního podokna akcí v horní části stránky. Vyhledávání akcí však zobrazuje také výsledky viditelných panelů nástrojů, které jsou umístěny na dalších místech na stránce. Například vyhledáváte tlačítko **Zásoby na skladě**, které se nachází na pevné záložce **Řádky prodejní objednávky**. V tomto případě cesta tlačítka v seznamu výsledků (**Řádky prodejní objednávky**&gt;**Zásoby**&gt;**Zobrazení**) vás informuje o tom, že toto tlačítko se nachází v nadpisu **Zobrazení** na tlačítku nabídky **Zásob** na pevné záložce **Řádky prodejní objednávky**. 

[![on-hand-inventory](./media/on-hand-inventory.png)](./media/on-hand-inventory.png)

## <a name="action-search-vs-navigation-search"></a>Vyhledávání akcí versus hledání navigace
Akce hledání je určena k vyhledání a spuštění akcí na stránce. Existuje i samostatný mechanismus vyhledávání pro vyhledávání a navigaci na stránky aplikace 365 for Operations. Další informace o této funkci naleznete v článku [Hledání navigace](navigation-search.md).




