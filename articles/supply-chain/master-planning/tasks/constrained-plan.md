---
title: Vygenerování plánu s omezeními
description: Tento článek vysvětluje způsob vytvoření plánu, který bere v úvahu omezení materiálu a kapacity.
author: t-benebo
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqPlanSched
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 65884d556724cd6132fe328e95a5bec78885c174
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904007"
---
# <a name="generate-a-constrained-plan"></a>Vygenerování plánu s omezeními

[!include [banner](../../includes/banner.md)]

Tento článek vysvětluje způsob vytvoření plánu, který bere v úvahu omezení materiálu a kapacity. Plán zajišťuje, aby se výroba nespustila před zajištěním dostupnosti materiálu, a aby nedošlo k přeplnění prostředků. 

K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF. Tento postup je určen pro plánujícího produkce.


## <a name="set-up-a-constrained-plan"></a>Vytvoření plánu s omezeními
1. Na domovské stránce vyberte pracovní prostor **Hlavní plánování**.
2. Vyberte **Hlavní plány** v seznamu odkazů na úplně pravé straně pracovního prostoru.
3. Vyhledejte na seznamu požadovaný záznam a vyberte ho. Příklad: **Statický plán**  
4. Vyberte **Ano** v poli **Omezená kapacita**.
5. Do pole **Omezená kapacita – ochranná doba** zadejte `30`.
6. Rozbalte část **Ochranné doby ve dnech**.
7. Vyberte **Ano** v poli **Kapacita**.
8. V poli **Ochranná doba plánování kapacity (ve dnech)** zadejte číslo. Příklad: `60`  
9. Vyberte možnost **Ano** v poli **Vypočtená zpoždění**.
10. V poli **Vypočítat pevnou ochrannou dobu zpoždění (ve dnech)** zadejte číslo. Příklad: `60` 
11. Rozbalte část **Vypočtená zpoždění**.
12. Vyberte **Ano** v poli **Přidat vypočtené zpoždění k požadovanému datu**.
13. Zavřete stránku.

## <a name="create-a-constrained-plan"></a>Vytvoření plánu s omezením
1. Vyberte **Spustit**.
2. V poli **Hlavní plán** zadejte nebo vyberte plán, pro který jste nastavili omezení.  
3. Vyberte **OK**.
4. Vyberte **Plánované objednávky**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]