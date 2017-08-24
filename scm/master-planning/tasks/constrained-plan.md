--- 
title: "Vygenerování plánu s omezeními"
description: "Tento postup popisuje způsob vytvoření plánu, který bere v úvahu omezení materiálu a kapacity."
author: YuyuScheller
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 6735f0287e7a61ff494a48c97c44480c6038097c
ms.contentlocale: cs-cz
ms.lasthandoff: 07/27/2017

---
# <a name="generate-a-constrained-plan"></a>Vygenerování plánu s omezeními

[!include[task guide banner](../../includes/task-guide-banner.md)]

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


