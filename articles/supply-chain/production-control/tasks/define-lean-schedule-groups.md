---
title: Definování skupin štíhlého plánu
description: Skupiny štíhlého plánu jsou definovány pro rozdělení do skupin a rozlišení produkty v plánování kanbanu.
author: cvocph
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanScheduleGroup, GanttColorTableLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4e4ad3eb1f7c73d0b6671e2d1698d0647f6dbb93
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5257236"
---
# <a name="define-lean-schedule-groups"></a>Definování skupin štíhlého plánu

[!include [banner](../../includes/banner.md)]

Skupiny štíhlého plánu jsou definovány pro rozdělení do skupin a rozlišení produkty v plánování kanbanu. Seskupení lze provést jako obecné přidružení společností nebo jako specifické k pracovní buňce. Každá skupina má barevný kód přiřazeny pro vizuální označení na stránce se seznamem plánování kanbanu. K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.


## <a name="define-lean-scheduling-group"></a>Definování skupiny štíhlého plánování
1. Přejděte k Řízení informací o produktech > Lean manufacturing > Skupiny štíhlého plánu.
2. Klikněte na položku Nová.
3. Zadejte hodnotu do pole Skupina plánu.
    * Skupina plánu může být definována jako globální skupina nebo specifická pro pracovní buňku. V tomto jednoduchém příkladu budeme definovat globální skupinu a pracovní buňka zůstane prázdná. Nastavení této skupiny se vztahují na všechny pracovní buňky, které nemají konkrétní skupiny plánu.  
4. Z výběr barvy vyberte barvu.
    * Barvy jsou použity k označení úloh na stránce se seznamem kanbanového plánu nebo na kanbanové desce procesu.  
5. Označte v seznamu vybraný řádek.
6. Klikněte na odkaz na vybraném řádku v seznamu.

## <a name="associate-product"></a>Přidružení produktu
1. Přidružení specifického produktu
    * Existují dva způsoby přidružení produktů ke skupinám štíhlého plánu, buď jako specifického produktu (typ vztahu položky = zboží), nebo jako části alokačního klíče položky (typ vztahu položky = skupina).    
2. V poli Vztah položky vyberte Položka.
3. Zadejte hodnotu do pole Číslo zboží.
4. V poli Poměr propustnosti zadejte číslo.
    * Poměr výchozí propustnosti je 1, což znamená, že související produkty spotřebovávají přesně kapacitu stanovenou v aktivitách procesu výrobních toků. Poměr propustnosti > 1 definuje vyšší spotřebu prostředků, poměr propustnosti < 1 definuje nižší spotřebu prostředků. Poměr se používá při výpočtu nákladů a při výpočtu spotřeby kanbanové úlohy.  

## <a name="associate-item-allocation-key"></a>Přiřazení alokačního klíče položky
1. Přiřazení alokačního klíče položky
    * Přidejte přidružení k alokačnímu klíče položky použitím skupiny typ vztahu položky.   Všimněte si, že v tomto postupu je nutné mít ve svých datech definovanou prognózu alokačního klíče položky.  
2. V poli Vztah položky vyberte Skupina.
3. V poli Alokační klíč položky klepnutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
4. Klikněte na odkaz na vybraném řádku v seznamu.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]