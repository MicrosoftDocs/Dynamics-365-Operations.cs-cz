---
title: Vytvoření verze výrobního toku
description: Tento postup se zaměřuje na vytvoření nové verze výrobního toku.
author: cvocph
manager: tfehr
ms.date: 11/03/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b57dbd2516a25b414193ca76367bd8d5c4a1b298
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5255054"
---
# <a name="create-a-production-flow-version"></a>Vytvoření verze výrobního toku

[!include [banner](../../includes/banner.md)]

Tento postup se zaměřuje na vytvoření nové verze výrobního toku. Pro tuto proceduru musí být definovány výrobní parametry pro Lean manufacturing a jednotky měření pro čas třídy. Je třeba také definovat hodnotový proud a skupinu výroby. Další informace o výrobních tocích a aktivitách v lean manufacturingu naleznete v dokumentech white paper pro Lean manufacturing aplikace Microsoft Dynamics AX. K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.


## <a name="create-a-production-flow"></a>Vytvoření výrobního toku
1. Přejděte na Řízení výroby > Nastavení > Tok štíhlé výroby > Výrobního toky.
2. Klikněte na položku Nová.
3. Zadejte hodnotu do pole Název.
4. Zadejte nějakou hodnotu do pole Popis.
5. V poli Název kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
6. Klikněte na odkaz na vybraném řádku v seznamu.
    * Vyberte provozní jednotku typu hodnotového proudu. Hodnotový proud je provozní jednotka, která pokrývá všechny aktivity a toky hodnotového proudu. V této fázi provozní jednotky jsou omezeny právnickou osobou a nemají žádné další funkce.  
7. V poli Výrobní skupina klepnutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
8. Klikněte na odkaz na vybraném řádku v seznamu.
    * Vyberte skupinu výroby pro výrobní tok. Výrobní skupiny umožňují definici materiálu, práce, a účtů nedokončené výroby pro výrobní proces. Pro přidružení kontextu účetnictví k výrobnímu toku je nutné vybrat výrobní skupinu.  
9. Klikněte na položku Uložit.

## <a name="create-a-production-flow-version"></a>Vytvoření verze výrobního toku
1. Klepněte na možnost Přidat.
2. Do pole Datum vypršení platnosti zadejte datum a čas.
    * V případě potřeby definujte Datum vypršení platnosti pro verzi. Můžete ho kdykoli aktualizovat, a to dokonce i pro aktivní verze. Můžete ho využít pro plánování verze mimo fázi.  
3. Klikněte na tlačítko OK.
4. Označte v seznamu vybraný řádek.
5. Zadejte hodnotu do pole Jednotka.
6. Vyřešit změny jednotky taktu.
7. Do pole Průměrná doba výrobního taktu zadejte číslo.
    * Definujte Průměrnou délku výrobního taktu verze. Definujte cílovou průměrnou délku výrobního taktu pro ovládání taktu verze výrobního toku. Takt je definován jako množství za časové období. V tomto příkladu je délka výrobního taktu 0,2 hodin na 10 kusů. 8hodinová pracovní doba odpovídá denní kapacitě prostupnosti 400 kusů.  
8. V poli Množství na cyklus zadejte číslo.
    * Určete množství za cyklus ve vztahu k průměrné délce výrobního taktu.  
9. Přepněte rozšíření oddílu Podrobnosti verze.
10. Do pole Minimální doba výrobního taktu zadejte číslo.
    * Určete minimální délku výrobního taktu. Minimální délka výrobního taktu musí být menší nebo rovna průměrné délce výrobního taktu.  
11. Do pole Maximální doba výrobního taktu zadejte číslo.
    * Maximální délka výrobního taktu musí být vyšší nebo rovna průměrné délce výrobního taktu.  
12. Do pole Období skutečného času cyklu (dny) zadejte číslo.
    * Zadejte počet dní v období skutečného času cyklu. Období skutečného času cyklu je počet dnů, jejichž úlohy jsou zpětně seskupeny od aktuální minuty pro výpočet skutečného času cyklu. Hodnota může být změněna kdykoli a je použita pouze pro výpočet skutečného času cyklu.  
13. Klikněte na položku Uložit.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]