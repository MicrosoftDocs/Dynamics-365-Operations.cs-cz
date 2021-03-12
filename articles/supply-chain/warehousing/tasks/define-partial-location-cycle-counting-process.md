---
title: 'Definování procesu částečné cyklické inventury skladového místa '
description: Při použití plánů cyklických inventur pro vytvoření inventury můžete řídit vlastní inventurní operace vyžádáním pouze konkrétních produktů a variant produktů namísto všech zásob na skladě ve skladovém místě.
author: ShylaThompson
manager: tfehr
ms.date: 06/23/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItemCycleCount, WHSCycleCountPlan, WHSCycleCountPlanListPage, WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0778cc7c1703dcfd5ea77979aafc99f4f040830d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4977131"
---
# <a name="define-partial-location-cycle-counting-process"></a>Definování procesu částečné cyklické inventury skladového místa  

[!include [banner](../../includes/banner.md)]

Při použití plánů cyklických inventur pro vytvoření inventury můžete řídit vlastní inventurní operace vyžádáním pouze konkrétních produktů a variant produktů namísto všech zásob na skladě ve skladovém místě. Vyfiltrováním konkrétních produktů může vedoucí skladu snížit kontrolu režie, vyhnout se chybám konsolidace a ušetřit čas. Vedoucí skladu obvykle provádí nastavení. Tento proces můžete projít pomocí ukázkových dat společnosti USMF nebo pomocí vlastních dat.


## <a name="create-a-cycle-counting-work-template"></a>Vytvoření šablony práce cyklické inventury
1. Přejděte do nabídky Řízení skladu > Nastavení > Práce > Pracovní šablony.
2. V poli Typ pořadí pracovních činností vyberte možnost Cyklická inventura.
3. Klikněte na položku Nová.
4. V poli Pořadové číslo zadejte číslo.
    * Pořadí řazení je od nejnižšího čísla po nejvyšší číslo. Hodnota musí být větší než 0 (nula).  
5. Označte v seznamu vybraný řádek.
6. Zadejte hodnotu do pole Šablona práce.
7. Zadejte hodnotu do pole Popis pracovní šablony.
8. V poli ID fondu práce zadejte nebo vyberte hodnotu.
9. V poli Pracovní priorita zadejte číslo.
10. Klikněte na položku Uložit.
11. Klikněte na položku Nová.
12. Označte v seznamu vybraný řádek.
13. V poli Typ práce vyberte Inventura.
14. V poli ID pracovní třídy zadejte nebo vyberte hodnotu.
15. Klikněte na položku Uložit.
16. Klikněte na Zalomení řádků práce.
17. Klikněte na položku Nová.
18. V poli Pořadové číslo zadejte číslo.
    * Pořadí řazení je od nejnižšího čísla po nejvyšší číslo. Hodnota musí být větší než 0 (nula).  
19. Klikněte na položku Uložit.
20. Zavřete stránku.
21. Zavřete stránku.

## <a name="create-a-cycle-counting-plan"></a>Vytvoření plánu cyklické inventury
1. Přejděte do Správce skladu > Nastavení > Cyklická inventura > Plány cyklických inventur.
2. Klikněte na položku Nová.
3. Zadejte hodnotu do pole ID plánu cyklické inventury.
4. Zadejte hodnotu do pole Popis.
5. Do pole Maximální počet cyklických inventur zadejte číslo.
6. V poli Šablona práce zadejte nebo vyberte hodnotu.
7. Klikněte na položku Nová.
8. V poli Pořadové číslo zadejte číslo.
    * Pořadí řazení je od nejnižšího čísla po nejvyšší číslo. Hodnota musí být větší než 0 (nula).  
9. Zadejte nějakou hodnotu do pole Popis.
10. Klikněte na položku Uložit.
11. Klikněte na Definovat dotaz na produkt.
12. Označte v seznamu vybraný řádek.
13. V poli Kritéria zadejte nebo vyberte hodnotu.
14. Klikněte na tlačítko OK.
15. Zavřete stránku.

