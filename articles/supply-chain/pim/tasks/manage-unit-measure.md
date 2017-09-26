--- 
title: "Správa měrných jednotek"
description: "Tento postup popisuje definování měrné jednotky, poskytnutí překladů pro jednotky a jejich popisu a definování pravidel pro převod souvisejících jednotek."
author: sorenva
manager: AnnBe
ms.date: 02/12/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: de5baa1e5c30ee998d113f7366c445a65723dfdc
ms.contentlocale: cs-cz
ms.lasthandoff: 07/27/2017

---
# <a name="manage-unit-of-measure"></a>Správa měrných jednotek

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tento postup popisuje definování měrné jednotky, poskytnutí překladů pro jednotky a jejich popisu a definování pravidel pro převod souvisejících jednotek. Tento postup můžete projít pomocí ukázkových dat společnosti nebo pomocí vlastních dat.

1. Přejděte do části Údržba uvolněného produktu.
2. Klikněte na možnost Jednotky.

## <a name="create-a-unit-of-measure"></a>Vytvoření měrné jednotky
1. Klikněte na položku Nová.
2. Zadejte hodnotu do pole Jednotka.
    * Zadejte ID nebo symbol pro použití při odkazování na měrnou jednotku.  
3. Zadejte nějakou hodnotu do pole Popis.
    * Zadejte popisný název měrné jednotky v systémovém jazyce.  
4. V poli Třída jednotek vyberte možnost.
    * Třída jednotek určuje, do jakého logického seskupení, například do oblasti, hmotnosti nebo množství, měrná jednotka patří.  
5. V poli Desetinná přesnost zadejte číslo.
    * Určete počet desetinných míst, na který má být převedená měrná jednotka zaokrouhlena při dokončení výpočtu pro měrnou jednotku.  
6. Klikněte na položku Uložit.

## <a name="define-unit-translations"></a>Definování překladů jednotek
1. Klikněte na možnost Texty jednotek.
2. Klikněte na položku Nová.
    * Text jednotky použijte k vytvoření překladu ID nebo symbolu představujícího měrnou jednotku pro použití u externích dokumentů v jazycích odběratele nebo dodavatele.  
3. V poli Jazyk zadejte nebo vyberte hodnotu.
4. Zadejte hodnotu do pole Text.
5. Klikněte na položku Uložit.
6. Zavřete stránku.
7. Klikněte na možnost Popisy přeložené jednotky.
8. Klikněte na položku Nová.
    * Definujte popisy měrné jednotky pro daný jazyk.  
9. V poli Jazyk zadejte nebo vyberte hodnotu.
10. Zadejte nějakou hodnotu do pole Popis.
11. Klikněte na položku Uložit.
12. Zavřete stránku.

## <a name="define-unit-conversion-rules"></a>Definování pravidel pro převod jednotek
1. Klikněte na možnost Převody jednotek.
    * Definujte pravidla pro převod měrné jednotky do a z jiných měrných jednotek ve vybrané třídě jednotky.  
2. Kliknutím na možnost Nový otevřete dialogové okno.
3. Do pole Koeficient zadejte číslo.
    * Koeficient převodu mezi hodnotou Z jednotky a Do jednotky. Například koeficient převodu centimetrů na metry je 100, protože v jednom metru je 100 centimetrů.  
4. V poli Do jednotky zadejte nebo vyberte hodnotu.
5. Vyberte možnost v poli Zaokrouhlení.
    * Definujte, jak má být převedená hodnota zaokrouhlena.  
6. Klikněte na tlačítko OK.
7. Zavřete stránku.


