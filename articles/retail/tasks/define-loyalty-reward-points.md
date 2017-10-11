--- 
title: " Definování bodů věrnostních odměn"
description: "Tato procedura vás provede definováním bodů věrnostních odměn."
author: scott-tucker
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: 56f11484d960ab22aefef359c18f71d54dc50071
ms.contentlocale: cs-cz
ms.lasthandoff: 07/28/2017

---
# <a name="define-loyalty-reward-points"></a> Definování bodů věrnostních odměn

[!include[task guide banner](../includes/task-guide-banner.md)]

Tato procedura vás provede definováním bodů věrnostních odměn. Body věrnostní odměny byste měli nastavit ještě před nastavením věrnostního programu. Tato procedura používá data ukázkové společnosti USRT.

1. Přejděte do nabídky Maloobchodní a velkoobchodní prodej > Odběratelé > Věrnost > Body věrnostní odměny.
2. Klikněte na položku Nová.
3. Zadejte hodnotu do pole ID bodu odměny.
4. Zadejte nějakou hodnotu do pole Popis.
5. Vyberte možnost v poli Typ bodu odměny.
    * Vyberte Množství, pokud chcete věrnostní body zaokrouhlit na nejbližší celé číslo. Pokud chcete, aby body odměny byly zaokrouhlování podle pravidel zaokrouhlení měny, vyberte Množství. Vyberete-li možnost Množství, přeskočte další krok této procedury.  
6. Zadejte hodnotu do pole Měna.
    * Pro typ částky bodů odměny budou mít všechny udělené body vybranou měnu. Pro body odměny pro typ množství toto pole nelze použít – vynechejte tento krok.  
7. Zaškrtněte nebo zrušte zaškrtnutí políčka Lze uplatnit.
8. Zadejte číslo do pole Uplatnit hodnocení.
    * Uplatnit hodnocení se používá, když dvě nebo více uplatnitelných bodových odměn je možné použít pro zaplacení produktů. Pokud dva body odměny mají stejné hodnocení pro uplatnění, pak se použije ten, který vyžaduje snížení počtu bodů.  
9. Zadejte číslo do pole Hodnota času konce platnosti.
    * Body odměny vyprší za zadaný počet dní, měsíců nebo roků po jejich vydání. Hodnota „0“ znamená, že body věrnostní odměny nikdy nevyprší.  
10. Vyberte možnost v poli Jednotka času konce platnosti.
11. Klikněte na položku Uložit.

