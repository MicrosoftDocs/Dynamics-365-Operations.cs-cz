---
title: Výpočet návrhů kanbanového množství
description: Tento postup se zaměřuje na optimalizaci velikosti a množství kanbanu u konkrétních kanbanových pravidel pomocí výpočtu kanbanového množství.
author: ChristianRytt
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 96d68ca4440ac9eea4fa76a963adbe95bd69cf9e134daec64b39954837207eca
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6711800"
---
# <a name="calculate-kanban-quantity-suggestions"></a>Výpočet návrhů kanbanového množství

[!include [banner](../../includes/banner.md)]

Tento postup se zaměřuje na optimalizaci velikosti a množství kanbanu u konkrétních kanbanových pravidel pomocí výpočtu kanbanového množství. K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF. Tento postup je určen pro vedoucího hodnotového proudu. Je nutné, abyste dokončili postup Přidání zásad výpočtu kanbanového množství ke kanbanovému pravidlu.


## <a name="create-a-kanban-quantity-calculation"></a>Vytvoření výpočtu kanbanového množství
1. Přejít na Řízení výroby > Pravidelné úlohy > Výpočet kanbanového množství > Vypočítat kanbanové množství.
2. Klikněte na položku Nová.
3. Zadejte Speaker2016 do pole Název.
4. V poli Název kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
    * Vyberte pravidlo, které jste vytvořili v postupu Přidání zásad výpočtu kanbanového množství ke kanbanovému pravidlu. Například Speaker2016.  
5. Klikněte na odkaz na vybraném řádku v seznamu.
6. V poli Pravidlo aktivní ode dne nastavte datum a čas na 2012-12-17T08:00:00.
    * Toto datum slouží jako základ pro určení pevných kanbanových pravidel, která jsou zahrnuta do výpočtu kanbanového množství.  
7. Do pole Datum začátku období splněné poptávky nastavte datum a čas na 2012-11-17T09:00:00.
    * Počáteční datum zahrnutí dřívějších transakcí poptávky pro výpočet kanbanového množství.  
8. Do pole Datum konce období splněné poptávky nastavte datum a čas na 2012-12-17T07:59:59.
    * Koncové datum zahrnutí dřívějších transakcí poptávky pro výpočet kanbanového množství.  
9. Do pole Datum začátku období poptávky nastavte datum a čas na 2012-12-17T08:00:00.
    * Počáteční datum zahrnutí aktuálních transakcí poptávky pro výpočet kanbanového množství.  
10. Do pole Datum konce období poptávky nastavte datum a čas na 2013-01-16T07:59:59.
    * Koncové datum zahrnutí aktuálních transakcí poptávky pro výpočet kanbanového množství.  

## <a name="generate-kanban-quantity-proposal"></a>Generování návrhu kanbanového množství
1. Klikněte na položku Uložit.
2. Klepněte na tlačítko Generovat.
    * Tímto vytvoříte řádek návrhu kanbanového množství pro kanbanové pravidlo 000020.  

## <a name="run-kanban-quantity-calculation"></a>Spuštění výpočtu kanbanového množství
1. Klikněte na tlačítko Vypočítat.
    * Tímto vypočítáte návrh kanbanového množství.  
2. Klikněte na tlačítko OK.
3. Označte v seznamu vybraný řádek.
    * Všimněte si, že navrhované kanbanové množství je „2“.  

## <a name="change-product-quantity-and-calculate-again"></a>Změna množství produktu a opětovné provedení výpočtu
1. Nastavte Celkové množství produktu na 5.
2. Klikněte na tlačítko Vypočítat.
3. Klikněte na tlačítko OK.
    * Všimněte si, že s kanbanovým množstvím „5“ se návrh změní na kanbanové množství „4“.  
    * Důvodem je skutečnost, že se sníženým množstvím produktu je zapotřebí více kanbanu ke splnění požadavku.  

## <a name="update-kanban-rule"></a>Aktualizace kanbanového pravidla
1. Do pole Datum účinnosti pravidla zadejte datum a čas.
    * Nastavte Pravidlo aktivní ode dne na datum v budoucnosti. Například dnes + jeden rok.  
2. Klepněte na položku Aktualizovat.
3. Klikněte na tlačítko OK.
4. Zavřete stránku.

## <a name="validate-change-on-kanban-rule"></a>Ověření změny v kanbanovém pravidle
1. Přejděte k Řízení informací o produktech > Lean manufacturing > Kanbanová pravidla.
2. Klikněte na odkaz na vybraném řádku v seznamu.
    * Vyberte kanbanové pravidlo vytvořené v předchozím podúkolu. Toto by mělo být první kanbanové pravidlo v seznamu roztříděném podle čísla.  
3. Přepněte rozšíření oddílu Podrobnosti.
    * Všimněte si data platnosti, které znamená, že toto pravidlo není až do tohoto data aktivováno.  
4. Přepněte rozšíření oddílu Množství.
    * Všimněte si, že se jedná o výchozí množství, které jste zadali ve výpočtu kanbanového množství.  
    * Všimněte si, že se že jedná o pevné kanbanové množství „4“ z výpočtu kanbanového množství.  
5. Klikněte na kartu Panel seznamu.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]