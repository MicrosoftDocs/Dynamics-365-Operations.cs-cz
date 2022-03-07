---
title: Přidání předchůdce k aktivitě výrobního toku
description: Ve verzi výrobního toku musí být všechny aktivity seřazeny.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityRelationNew, PlanActivityLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dc1aa742013faeeb545d746f9715c639a5b66b9b
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/29/2021
ms.locfileid: "7575068"
---
# <a name="add-a-predecessor-to-a-production-flow-activity"></a>Přidání předchůdce k aktivitě výrobního toku

[!include [banner](../../includes/banner.md)]

Ve verzi výrobního toku musí být všechny aktivity seřazeny. Aktivita může mít jednoho nebo více předchůdců nebo následníků. 

Tato procedura ukazuje, jak přidružit předchůdce k aktivitě. 

K provedení tohoto úkolu potřebujete výrobní tok, který má verzi konceptu s alespoň dvěma aktivitami, které mohou být propojeny. 

Další informace naleznete v dokumentu white paper "Production flows and activities in lean manufacturing." (Výrobní toky a aktivity v lean manufacturing.)


## <a name="find-the-production-flow-and-version"></a>Vyhledání výrobního toku a verze
1. Přejděte na Řízení výroby > Nastavení > Tok štíhlé výroby > Výrobního toky.
2. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
3. Klikněte na odkaz na vybraném řádku v seznamu.
4. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
5. Klepněte na aktivity.

## <a name="select-an-activity-and-add-a-predecessor"></a>Výběr aktivity a přidání předchůdce
1. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
2. Klikněte na Přidat předchůdce.
3. V poli Aktivita zadejte nebo vyberte hodnotu.
4. Do pole Poměr času cyklu zadejte číslo.
    * Výchozí poměr času cyklu relace aktivity je 1. Předpokladem je, aby obě aktivity byly spuštěna stejným tempem nebo ve stejné délce výrobního taktu. Pokud předchůdce běží vyšším tempem (nižší délka výrobního taktu), poměr by měl být nižší než 1, jestliže předchůdce pracuje pomalejším tempem (vyšším délka výrobního taktu), poměr času cyklu je vyšší než 1.  
5. Klikněte na tlačítko OK.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]