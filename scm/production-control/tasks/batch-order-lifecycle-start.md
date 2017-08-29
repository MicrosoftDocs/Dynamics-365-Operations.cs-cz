--- 
title: "Životní cyklus dávkové objednávky od vytvoření po spuštění"
description: "Tento proces vás provede první částí životního cyklu dávkové objednávky."
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
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: dcb0814ae51f5914654736a957638f7d8be81e3f
ms.contentlocale: cs-cz
ms.lasthandoff: 07/28/2017

---
# <a name="batch-order-lifecycle-from-create-to-start"></a>Životní cyklus dávkové objednávky od vytvoření po spuštění

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tento proces vás provede první částí životního cyklu dávkové objednávky.

Z vytvoření, odhadu ceny a ukončení plánování výrobní úlohy k vlastnímu spuštění dávkové objednávky.



K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF. 



Předpoklady pro spuštění procedury s jinou sadou dat je uvolněný produkt s aktivní verzí receptury a postupu.


## <a name="create-a-batch-order"></a>Vytvoření dávkové objednávky
1. Přejděte na možnost Všechny výrobní zakázky.
2. Klikněte na možnost Nová dávková objednávka.
3. V poli Číslo zboží zadejte nebo vyberte hodnotu.
4. Klepněte na volbu Nový.
5. Použijte rychlý filtr k filtrování v poli Výroba s hodnotou „b“.

## <a name="view-production-formula-and-expected-co-products"></a>Zobrazení výrobní receptury a očekávaných souběžných produktů
1. V podokně akcí klikněte na položku Výrobní zakázka.
2. Klepněte na možnost Receptura.
3. Zavřete stránku.
4. Klepněte na možnost Souběžné produkty.
5. Zavřete stránku.

## <a name="estimate-the-batch-order"></a>Odhad dávkové objednávky
1. Klepněte na Odhad.
2. Klikněte na tlačítko OK.
3. V podokně akcí klikněte na možnost Spravovat náklady.
4. Klepněte na Zobrazit podrobnosti výpočtu.
5. Zavřete stránku.

## <a name="release-the-batch-order"></a>Uvolnění dávkové objednávky
1. V podokně akcí klikněte na položku Výrobní zakázka.
2. Klikněte na položku Uvolnit.
3. Klikněte na tlačítko OK.

## <a name="schedule-production-jobs"></a>Úlohy plánu výroby
1. V podokně akcí klikněte na možnost Plán.
2. Klikněte na Plánovat úlohy.
3. Vyberte Ne v poli Omezená kapacita.
4. Vyberte Ne v poli Omezený materiál.
5. Klepněte na tlačítko OK.
6. V podokně akcí klikněte na položku Výrobní zakázka.
7. Klikněte na Všechny úlohy.
8. Zavřete stránku.

## <a name="start-the-batch-order"></a>Spuštění dávkové objednávky
1. Klikněte na položku Spustit.
2. Klikněte na záložku Obecné.
3. V poli Zaúčtovat výdejku vyberte možnost Ne.
4. Klikněte na tlačítko OK.
5. V podokně akcí klikněte na možnost Zobrazit.
6. Klepněte na Výdejka.
7. Klikněte na odkaz na vybraném řádku v seznamu.
8. Zavřete stránku.
9. Zavřete stránku.
10. Klepněte na Karta postupu.
11. Klikněte na odkaz na vybraném řádku v seznamu.
12. Zavřete stránku.
13. Zavřete stránku.


