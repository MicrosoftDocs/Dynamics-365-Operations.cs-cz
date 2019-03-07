---
title: Ověření výrobního toku a verze
description: Tato procedura popisuje postup při vytvoření nového výrobního toku a první verze pro lean manufacturing.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4ae4c5f55d317a99e23ba6e76fc50ddece1e55a1
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "352843"
---
# <a name="validate-a-production-flow-and-version"></a>Ověření výrobního toku a verze

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tato procedura popisuje postup při vytvoření nového výrobního toku a první verze pro lean manufacturing. Předpoklady: Musí být definovány výrobní parametry pro Lean manufacturing a jednotky měření pro čas třídy. Je třeba definovat hodnotový proud a skupinu výroby. S koncepty výrobních toků a aktivitami se seznámíte v dokumentaci o Lean manufacturingu. Tato procedura se vztahuje k právnické osobě USMF v ukázkových datech. Avšak mohou být použity jiní právnické osoby za předpokladu, že právnická osoba je nakonfigurována pro Lean manufacturing.


## <a name="create-a-production-flow"></a>Vytvoření výrobního toku
1. Přejděte na Řízení výroby > Nastavení > Tok štíhlé výroby > Výrobního toky.
2. Klikněte na položku Nová.
3. Zadejte hodnotu do pole Název.
4. Zadejte nějakou hodnotu do pole Popis.
5. V poli Název kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
6. Klikněte na odkaz na vybraném řádku v seznamu.
    * Hodnotový proud je provozní jednotka, která pokrývá všechny aktivity a toky hodnotového proudu.   V této fázi provozní jednotky jsou omezeny právnickou osobou a nemají žádné další funkce.  
7. V poli Výrobní skupina klepnutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
8. Klikněte na odkaz na vybraném řádku v seznamu.
    * Výrobní skupiny umožňují definici materiálu, práce, a účtů nedokončené výroby pro výrobní proces. Pro přidružení kontextu účetnictví k výrobnímu toku je nutné vybrat výrobní skupinu.  
9. Klikněte na položku Uložit.

## <a name="create-a-production-flow-version"></a>Vytvoření verze výrobního toku
1. Klepněte na možnost Přidat.
2. Do pole Datum vypršení platnosti zadejte datum a čas.
    * Datum vypršení platnosti verze lze v každém okamžiku aktualizovat, a to dokonce i aktivní verze. Využijte vypršení platnosti verze k plánování fáze mimo verzi.  
3. Klikněte na tlačítko OK.
4. Označte v seznamu vybraný řádek.
5. Zadejte hodnotu do pole Jednotka.
6. Vyberte Jednotku taktu.
7. Do pole Průměrná doba výrobního taktu zadejte číslo.
    * Definujte cílovou průměrnou délku výrobního taktu pro ovládání taktu verze výrobního toku.   Takt je definován jako množství za časové období.  V tomto příkladu je délka výrobního taktu 0,2 hodin na 10 kusů. 8hodinová pracovní doba odpovídá denní kapacitě prostupnosti 400 kusů.  
8. V poli Množství na cyklus zadejte číslo.
9. Rozbalte nebo sbalte oddíl Podrobnosti verze.
10. Do pole Minimální doba výrobního taktu zadejte číslo.
    * Minimální délka výrobního taktu musí být menší nebo rovna průměrné délce výrobního taktu.  
11. Do pole Maximální doba výrobního taktu zadejte číslo.
    * Maximální délka výrobního taktu musí být vyšší nebo rovna průměrné délce výrobního taktu.  
12. Zadejte počet dní v období skutečného času cyklu
    * Období skutečného času cyklu je počet dnů, jejichž úlohy jsou zpětně seskupeny od aktuální minuty pro výpočet skutečného času cyklu. Hodnota může být změněna kdykoli a je použita pouze pro výpočet skutečného času cyklu.  
13. Klikněte na položku Uložit.

