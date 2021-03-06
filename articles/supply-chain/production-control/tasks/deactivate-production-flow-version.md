---
title: Deaktivace verze výrobního toku
description: Když aktivní verze výrobního toku již není potřeba, je možné ji deaktivovat.
author: cvocph
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LeanProductionFlow
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e47cb950ce488d8b6170f829e1fedc664b921a1a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5811551"
---
# <a name="deactivate-a-production-flow-version"></a>Deaktivace verze výrobního toku

[!include [banner](../../includes/banner.md)]

Když aktivní verze výrobního toku již není potřeba, je možné ji deaktivovat. Tuto možnost používejte pouze v případě, že všechna kanbanová pravidla a aktivity skončily a nebude znovu aktivovány. Všimněte si, že datum konce platnosti všechna kanbanových pravidel vztahující se k této verzi výrobního toku budou aktualizována na aktuální datum a čas. 

Chcete-li změnit aktivní verzi výrobního toku, zkuste nastavit datum vypršení platnosti aktivní verze a vytvořit novou verzi. To vám umožní pokračovat ve výrobních operacích při přípravě nové verze a souvisejících kanbanových pravidel. 

K vypršení platnosti aktivní verze výrobního toku je třeba nastavit datum vypršení platnosti. V tomto smyslu je deaktivace spíše výjimka než pravidlo. 

Pro tuto proceduru potřebujete výrobní tok ve verzi, kterou lze deaktivovat. Nepokoušejte se o to ve výrobním prostředí, pokud si nejste 100% jistí, že verze je zcela zastaralá.


## <a name="deactivate-a-production-flow-version"></a>Deaktivace verze výrobního toku
1. Přejděte na Řízení výroby > Nastavení > Tok štíhlé výroby > Výrobního toky.
2. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
3. Klikněte na odkaz na vybraném řádku v seznamu.
4. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
5. Klepněte na tlačítko Deaktivovat.
    * Pokud si nejste 100% jistí, že tato verze výrobního toku je zastaralá, nepokračujte. Klepnutí na tlačítko OK ukončí všechna aktivní kanbanová pravidla a okamžitě zastavení všechny výrobní a doplňovací aktivity této verze výrobního toku.  
6. Klikněte na tlačítko OK.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]