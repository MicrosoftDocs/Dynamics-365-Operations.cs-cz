---
title: Sledování běhu hlavního plánování
description: Plánovač výroby chce vědět, zda probíhá hlavní plánování.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, InventItemIdLookupSimple, ReqLog, ReqProcessTaskTrace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b923b215528ecceaed9b5057ddb736ec959f1d65
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/01/2019
ms.locfileid: "1845106"
---
# <a name="monitor-a-master-planning-run"></a>Sledování běhu hlavního plánování

[!include [task guide banner](../../includes/task-guide-banner.md)]

Plánovač výroby chce vědět, zda probíhá hlavní plánování. K dokončení tohoto postupu jsou použita ukázková data společnosti USMF.


## <a name="run-master-planning"></a>Spuštění hlavního plánování
1. Klikněte na Hlavní plánování.
    * Tento údaj naleznete na výchozím řídicím panelu.  
2. V poli Plán zadejte nebo vyberte hodnotu.
    * Příklad: Statický plán  
3. Klikněte na položku Spustit.
4. V poli Sledovat čas zpracování vyberte hodnotu Ano.
    * Pokud již je políčko zaškrtnuto, tento krok vynechejte.  
5. Do pole Počet vláken zadejte číslo.
6. Rozbalte oddíl Záznamy k zahrnutí.
7. Klepněte na tlačítko Filtr.
8. Označte v seznamu vybraný řádek.
    * Označte řádek, kde Pole = Číslo položky.  
9. V poli Kritéria zadejte nebo vyberte hodnotu.
    * Příklad: T0001  
10. Klikněte na tlačítko OK.
11. Klikněte na tlačítko OK.

## <a name="monitor-the-master-planning-run"></a>Sledování běhu hlavního plánování
1. Klepněte na tlačítko Historie.
2. Klepněte na možnost Dotazy.
3. Klikněte na Doba trvání zpracování úkolu.
4. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
    * Pro každou položku můžete získat přehled o době potřebné k dokončení jednotlivých kroků plánování.  

