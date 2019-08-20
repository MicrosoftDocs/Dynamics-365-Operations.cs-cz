---
title: Přidání předchůdce k aktivitě výrobního toku
description: Ve verzi výrobního toku musí být všechny aktivity seřazeny.
author: cvocph
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityRelationNew, PlanActivityLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 346dca110fde9ff7600f3e4606529c27289dfc97
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/01/2019
ms.locfileid: "1838768"
---
# <a name="add-a-predecessor-to-a-production-flow-activity"></a>Přidání předchůdce k aktivitě výrobního toku

[!include [task guide banner](../../includes/task-guide-banner.md)]

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

