---
title: Vyhledání akce
description: Tento článek popisuje funkci hledání akce. Hledání akce vám pomůže najít a spustit akce na stránce.
author: jasongre
ms.date: 03/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 62303
ms.assetid: 62c70de0-fdde-4417-8e08-0583fb095a40
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6277c37ac43b8cc05c8b53da5ca0a1909f58c4f9
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/31/2022
ms.locfileid: "8070027"
---
# <a name="action-search"></a>Vyhledání akce

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

Tento článek popisuje funkci hledání akce. Hledání akce vám pomůže najít a spustit akce na stránce.

## <a name="introduction"></a>Úvod

Stránky primárně vystavují příkazy v podoknech akcí, standardním podokně akcí, které se zobrazí v horní části stránky, a na panelech nástrojů, které se zobrazují v různých částech stránky. V předchozích verzích umožňovala funkce Klíčové tipy rychlý přístup k libovolnému tlačítku v podokně akcí stisknutím klávesy Alt a řady čísel.

[![keyTipsAX6.](./media/keytipsax6.png)](./media/keytipsax6.png)

Klíčové tipy již nejsou k dispozici, ale byly nahrazeny funkcí hledání akce. Nová funkce vám umožňuje rychle vyhledat a spustit tlačítko z jakéhokoli viditelného podokna akcí.

## <a name="using-action-search"></a>Použití hledání akcí

Chcete-li použít funkci hledání akce, postupujte takto.

1. V podokně akcí, klepněte na pole **vyhledávání akcí**. (Pole **vyhledávání akcí** obsahuje ikonu lupy.)
2. Zadejte část nebo celý název tlačítka, které chcete spustit. Můžete také hledat pomocí slov z „cesty“ k tlačítku. (Další informace o najdete v další části tohoto článku.) Obvykle se tlačítka se zobrazí v horní části seznamu výsledků poté, co zadáte dva až čtyři znaky.
3. Najděte a spusťte tlačítko v seznamu výsledků (pomocí myši nebo klávesnice).

Po spuštění tlačítka bude výběr vrácen do vaší poslední pozice na stránce tak, abyste mohli pokračovat v práci.

[![action-search-field.](./media/action-search-field.png)](./media/action-search-field.png)

Vyhledávání akcí také spustíte stisknutím kláves Ctrl +/ nebo Alt + Q. Stiskněte klávesovou zkratku ještě jednou, chcete-li se vrátit na výběr do vaší poslední pozice na stránce.

## <a name="understanding-the-results-list"></a>Vysvětlivky k seznamu výsledků

Často musíte znát umístění i kontext tlačítka, abyste plně porozuměli účelu daného tlačítka. Proto se v seznamu výsledků zobrazují další informace pro každou položku, které vám pomohou přesně pochopit, která tlačítka se zobrazí v seznamu. Zejména se zobrazí "cesta" tlačítka. Tato cesta může obsahovat popisky tyto prvky uživatelského rozhraní odpovídajícím způsobem:

- Karta podokno akcí
- Skupina tlačítek
- Tlačítko nabídky (pokud je tlačítko uvnitř tlačítka nabídky)
- Oddělovač nabídky (pokud tlačítko je v pojmenované skupině v rámci tlačítka nabídky)
- Skupina nebo karta na stránce (například název pevné záložky)

Předpokládejme například, že jste zadali výraz **cel** do pole **vyhledávání akcí** a nyní prověřujete seznam výsledků. První položka u tlačítek, která má název **Celkem**, je zvýrazněna. Rovněž je zobrazena cesta tlačítka **Prodejní objednávka** &gt; **Zobrazení**. Část **Prodejní objednávka** cesty odpovídá kartě **Prodejní objednávka** v podokně akcí a část **Zobrazení** cesty odpovídá skupině **Zobrazení** na této kartě. Podobně cesta tlačítka **Celková sleva** tlačítko (**Prodej** &gt; **Vypočítat**) informuje o tom, že toto tlačítko se nachází ve skupině **Vypočítat** na kartě podokna akcí **Prodej**. Z toho vyplývá, že tyto informace vám pomohou pochopit, které tlačítko bude přesně vyvoláno vyhledáním akce (pokud ho vyberete v podokně výsledků).

[![action-search-field-with-data.](./media/action-search-field-with-data.png)](./media/action-search-field-with-data.png)

V předchozím příkladu vyhledávání akce ukázalo výsledky ze standardního podokna akcí v horní části stránky. Vyhledávání akcí však zobrazuje také výsledky z viditelných panelů nástrojů, které jsou umístěny na jiných místech na stránce. Například vyhledáváte tlačítko **Zásoby na skladě**, které je na pevné záložce **Řádky prodejní objednávky**. V tomto případě vás cesta tlačítka v seznamu výsledků (**Řádky prodejní objednávky** &gt; **Zásoby** &gt; **Zobrazení**) informuje o tom, že toto tlačítko se nachází v nadpisu **Zobrazení** na tlačítku nabídky **Zásoby** na pevné záložce **Řádky prodejní objednávky**.

[![on-hand-inventory.](./media/on-hand-inventory.png)](./media/on-hand-inventory.png)

> [!NOTE]
> V hledání Akcí se nezobrazují některá tlačítka. Tyto zahrnují tlačítka ukončení dialogu a tlačítka z podformulářů. 

## <a name="action-search-vs-navigation-search"></a>Vyhledávání akcí versus hledání navigace

Akce hledání je určena k vyhledání a spuštění akcí na stránce. Existuje i samostatný mechanismus vyhledávání pro vyhledávání a navigaci na stránky. Další informace o této funkci naleznete v článku [Hledání navigace](navigation-search.md).


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]