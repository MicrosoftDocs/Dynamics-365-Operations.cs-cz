---
title: Vygenerování plánu s omezeními
description: Tento postup popisuje způsob vytvoření plánu, který bere v úvahu omezení materiálu a kapacity.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqPlanSched
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 72cddd58b7068e08cddf24df83da8da2f7af7168
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/01/2019
ms.locfileid: "1845279"
---
# <a name="generate-a-constrained-plan"></a>Vygenerování plánu s omezeními

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tento postup popisuje způsob vytvoření plánu, který bere v úvahu omezení materiálu a kapacity. Plán zajišťuje, aby se výroba nespustila před zajištěním dostupnosti materiálu, a aby nedošlo k přeplnění prostředků. 

K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF. Tento postup je určen pro plánujícího produkce.


## <a name="set-up-a-constrained-plan"></a>Vytvoření plánu s omezeními
1. Klikněte na Hlavní plánování.
2. Klikněte na Hlavní plány.
3. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
    * Příklad: Statický plán  
4. Vyberte Ano v poli Omezená kapacita.
5. Do pole Omezená kapacita – ochranná doba zadejte 30.
6. Rozbalte část Ochranné doby ve dnech.
7. Vyberte Ano v poli Kapacita.
8. V poli Ochranná doba plánování kapacity (ve dnech) zadejte číslo.
    * Příklad: 60  
9. Vyberte možnost Ano v poli Vypočtená zpoždění.
10. V poli Vypočítat pevnou ochrannou dobu zpoždění (ve dnech) zadejte číslo.
    * Příklad: 60  
11. Rozbalte část Vypočtená zpoždění.
12. Vyberte Ano v poli Přidat vypočtené zpoždění k požadovanému datu.
13. Vyberte Ano v poli Přidat vypočtené zpoždění k požadovanému datu.
14. Vyberte Ano v poli Přidat vypočtené zpoždění k požadovanému datu.
15. Zavřete stránku.

## <a name="create-a-constrained-plan"></a>Vytvoření plánu s omezením
1. Klikněte na položku Spustit.
2. V poli Hlavní plán zadejte nebo vyberte hodnotu.
    * Vyberte plán, pro který jste nastavili omezení.  
3. Klikněte na tlačítko OK.
    * Tato operace může chvíli trvat.  
4. Klikněte na Plánované objednávky.

