---
title: "Hledání akce"
description: "Tento článek popisuje funkce vyhledávání akcí v 365 Microsoft Dynamics pro operace. Akce hledání vám pomůže najít a spustit akce na stránce."
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


Tento článek popisuje funkce vyhledávání akcí v 365 Microsoft Dynamics pro operace. Akce hledání vám pomůže najít a spustit akce na stránce.

<a name="introduction"></a>Úvod
------------

Stránky v 365 Microsoft Dynamics pro operace především vystavovat příkazy na podokna akcí, standardní podokna akcí, které se zobrazí v horní části stránky a panely nástrojů, které se zobrazují v různých částech stránky. V předchozích verzích tipy klíč funkce umožňují rychlý přístup k libovolné tlačítko v podokně akcí stisknutím klávesy Alt a pak řadu písmen. 

[![keyTipsAX6](./media/keytipsax6.png)](./media/keytipsax6.png) však v aktuální verzi Dynamics 365 pro operace klíče tipy již nejsou k dispozici, ale byla nahrazena funkce Hledat akce. Nová funkce vám umožňuje rychle vyhledat a spustit tlačítko z jakéhokoli viditelného podokna akcí.

## <a name="using-action-search"></a>Použití hledání akcí
Chcete-li použít funkci hledání akce, postupujte takto.

1.  V podokně akcí, klepněte na pole **vyhledávání akcí**. (Pole **vyhledávání akcí** obsahuje ikonu lupy.)
2.  Zadejte část nebo celý název tlačítka, které chcete spustit. Můžete také hledat pomocí slov z tlačítka "cesta." (Další informace naleznete v další části tohoto článku.) Obvykle v horní části seznamu výsledků se zobrazí tlačítko po zadání dvou až čtyř znaků.
3.  Najděte a spusťte tlačítko v seznamu výsledků (pomocí myši nebo klávesnice).

Po spuštění tlačítka bude výběr vrácen do vaší poslední pozice na stránce tak, abyste mohli pokračovat v práci. 

[![pole hledání akcí](./media/action-search-field.png)](./media/action-search-field.png)

Vyhledávání akcí také spustíte stisknutím kláves Ctrl +/ nebo Alt + Q. Stiskněte klávesovou zkratku ještě jednou, chcete-li se vrátit na výběr do vaší poslední pozice na stránce.

## <a name="understanding-the-results-list"></a>Vysvětlivky k seznamu výsledků
Často v 365 Dynamics pro operace, musíte vědět, umístění a kontextu tlačítko tak, aby plně pochopit účel tohoto tlačítka. Proto další informace se zobrazí pro každou položku v seznamu výsledků k vám pomůže pochopit přesně která tlačítka se zobrazí v seznamu. Zejména se zobrazí "cesta" tlačítka. Tato cesta může obsahovat popisky tyto prvky uživatelského rozhraní odpovídajícím způsobem:

-   Karta podokno akcí
-   Skupina tlačítek
-   Tlačítko nabídky (pokud je tlačítko uvnitř tlačítka nabídky)
-   Oddělovač nabídky (pokud tlačítko je v pojmenované skupině v rámci tlačítka nabídky)
-   Skupina nebo karta na stránce (například název pevné záložky)

Předpokládejme například, že jste zadali výraz **cel** do pole **vyhledávání akcí** a nyní prověřujete seznam výsledků. První položka pro tlačítko s názvem **celkem**, je zvýrazněn. Tlačítko cestu **prodeje**&gt;**zobrazení** je rovněž uvedena. **Prodejní objednávka** odpovídá části cesty **prodeje** kartu v podokně akcí a **zobrazení** odpovídá části cesty **zobrazení** skupiny na dané kartě. Podobně cestu **celkové slevy** tlačítko (**prodat**&gt;**vypočítat**) informuje o tom, že toto tlačítko se nachází v **vypočítat** skupiny na **prodat** kartu v podokně akcí. Proto tyto informace vám pomohou porozumět přesně které tlačítko bude aktivován při vyhledávání akce (je-li v seznamu výsledků vyberte tlačítko). 

[![akce hledání pole s data](./media/action-search-field-with-data.png)](./media/action-search-field-with-data.png) 

V předchozím příkladu vyhledávání akce ukázalo výsledky ze standardního podokna akcí v horní části stránky. Vyhledávání akcí však zobrazuje také výsledky viditelných panelů nástrojů, které jsou umístěny na dalších místech na stránce. Například hledáte **na skladě** tlačítko, které se nachází na **řádky prodejní objednávky** s náhledem. V tomto případě cesta tlačítka v seznamu výsledků (**řádky prodejní objednávky**&gt;**zásob**&gt;**zobrazení**) informuje o tom, že toto tlačítko se nachází v **zobrazení** nadpis na **zásob** na tlačítko nabídky **řádky prodejní objednávky** s náhledem. 

[![zásoby na skladě](./media/on-hand-inventory.png)](./media/on-hand-inventory.png)

## <a name="action-search-vs-navigation-search"></a>Vyhledávání akcí versus hledání navigace
Hledat akce je určena k vyhledání a spuštění akce na stránce, je mechanismus samostatné vyhledávání pro vyhledávání a navigaci na stránky 365 Dynamics pro operace. Další informace o této funkci naleznete [navigace vyhledávání](navigation-search.md) článku.




