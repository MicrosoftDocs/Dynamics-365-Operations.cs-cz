---
title: Deaktivace verze výrobního toku
description: Když aktivní verze výrobního toku již není potřeba, je možné ji deaktivovat.
author: cvocph
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
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 091cafd02bd568323e586373fc8b0f983afee343
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "340745"
---
# <a name="deactivate-a-production-flow-version"></a>Deaktivace verze výrobního toku

[!include [task guide banner](../../includes/task-guide-banner.md)]

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

