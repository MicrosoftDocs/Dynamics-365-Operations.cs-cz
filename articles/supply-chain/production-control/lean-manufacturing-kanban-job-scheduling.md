---
title: Plánování kanbanové úlohy pro lean manufacturing
description: V tomto článku jsou informace o vizuální kontrole plánování kanbanové úlohy a různých způsobech plánování kanbanových úloh.
author: johanhoffmann
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanBoardScheduleJobForward, KanbanBoardShowJobs, KanbanJobSchedulingListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 52961
ms.assetid: fe3b4822-6140-4b02-bebb-1fc17be2bce8
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f70c3cf44ce90b13250836013636920267d2016d
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/29/2021
ms.locfileid: "7570218"
---
# <a name="kanban-job-scheduling-for-lean-manufacturing"></a>Plánování kanbanové úlohy pro lean manufacturing

[!include [banner](../includes/banner.md)]

V tomto článku jsou informace o vizuální kontrole plánování kanbanové úlohy a různých způsobech plánování kanbanových úloh.  

Stránka **Plánování kanbanové úlohy** umožňuje vizuální kontrolu nad pracovními buňkami plánování lean manufacturingu. Nabízí přehled všech kanbanových úloh a nabízí několik možností filtrování. Na této stránce se lze přesunout na ostatní stránky, které souvisejí s konfigurací a spuštěním kanbanu.

## <a name="automatic-scheduling-of-kanban-jobs"></a>Automatické plánování kanbanové úlohy
Plánování může být spouštěno automaticky při nastavení parametru **Automaticky plánované množství** parametr v kanbanovém pravidle. Nastavíte-li **Automaticky plánované množství** na **1**, každá kanbanová úloha je naplánována bezprostředně po jeho vytvoření. Výsledek je tvořen řadou operací, co přijdou na řadu jako první. Pokud jste nastavili **automatické plánování množství** na hodnotu, která je větší než 1, jsou kanbanové úlohy seskupeny předtím, než budou plánovány. 

Tento pojem umožňuje velikost kanbanu snížit pod velikosti skutečné ekonomické dávky. Například velikost ekonomické dávky pro konkrétní zboží (nebo skupinu zboží) je 30. Místo vytvoření kanbanů, které používají množství produktu 30, můžete nakonfigurovat kanbanové pravidlo tak, aby měl množství produktu 10 a **Automaticky plánované množství** mělo hodnotu **3**. I když automatické plánování naplánuje kanbanové úlohy pro pracovní buňku pouze v případě, že existují tři neplánované úlohy, je plně průhledné k plánovači a jeho dílenskému nadřízenému, že dvě neplánované úlohy mohou čekat na spuštění. Plánovač nebo dílenský nadřízený poté můžete tyto dvě úlohy uvést do výroby ručním plánováním nebo vytvářením dalších kanbanů.

## <a name="manual-scheduling"></a>Ruční plánování
Pro ruční plánování aplikace Microsoft Dynamics AX 2012 zavedla desky kanbanového plánování. Ruční plánování lze kombinovat s automatickým plánováním. Deska kanbanového plánování vás nechá plánovat a rušit úlohy, přesouvat je v pořadí nebo je přesouvat z období do období. Úlohy, které jsou založeny na kanbanovém pravidle, kde hodnota **automatického plánování** je větší než **0**, mohou být ručně zrušeny. Tyto úlohy však lze přeplánovat, dojde-li k další události automatického plánování (když je vytvořen nový kanban). Pro ruční plánování jsou k dispozici následující možnosti:

-   **Plán** plánování vybrané úlohy podle data splatnosti. (Tato možnost, je podobná automatickému plánování.)
-   **Naplánovat po zadaném datu** zkouší plánovat vybrané úlohy podle data splatnosti, ale omezuje výsledek použitím zadaného nejbližšího data zahájení.
-   **Zpět** přesune vybrané plánované úlohy zpět v pořadí v rámci období.
-   **Vpřed** přesune vybrané plánované úlohy vpřed v pořadí v rámci období.
-   **Předchozí období** přesune vybrané úlohy naplánované na počátek nebo konec předchozího období.
-   **Další období** přesune vybrané úlohy naplánované na počátek nebo konec dalšího období.
-   **Plán** &gt; **Vrátit stav úlohy** umožňuje odebrat naplánovanou úlohu z plánu.

## <a name="lean-scheduling-groups"></a>Skupiny štíhlého plánování
Každý barva představuje skupiny štíhlého plánování. Skupiny štíhlého plánování mohou být volně určeny jako obecné skupiny nebo jako skupiny, které patří do jedné pracovní buňky. Položky a dimenze lze volně přiřadit do skupin plánování. Například v buňce Malování může skupinu plánování představovat barva produktu. Práce, která je řízena konkrétními požadavky na nástroje, mohou být položky seskupeny podle požadavku na nástroj a pracovní buňky balení mohou seskupovat položky podle šablony balení. Použití barev pro skupiny štíhlého plánování není povinné, ale doporučené. Zlepšuje přehled o stavu plánu. Například je velmi jednoduché zjistit, jaké barvy jsou vyrobeny v který den, a můžete tak na první pohled zjistit, jak optimalizovat tuto práci.

## <a name="work-cell-capacity-and-period-capacity"></a>Kapacita pracovní buňky a období kapacity
Kapacita štíhlé pracovní buňky je vždy souběžná kapacita. Jinak řečeno, v pracovní buňce může být aktivních více úloh současně. Kapacitu lze sledovat v těchto dvou režimech: propustnosti a hodinách.

### <a name="throughput"></a>Propustnost

Průměrné množství propustnosti referenčního období (standardní pracovní den, týden nebo měsíc) je určeno kapacitou pracovní buňky. Skutečná kapacita za den nebo týden je pak vypočítána na základě na pracovní doby kalendáře, který je k pracovní buňce přiřazen. Kapacita, která je zatížena úlohou, je množství úloh upravené poměrem propustnosti položky v pracovní buňce.

### <a name="hours"></a>Hodiny

Kalendář, který je přiřazen k pracovní buňce definuje podle dnů nebo týdnů dostupnou kapacitu. Kapacita, která je zatížena úlohou, je čas cyklu aktivity, upravené množstvím (výchozímu množství aktivity versus skutečnému množství úloh) a poměrem propustnosti položky v pracovní buňce.

#### <a name="period-capacity-factbox"></a>Okno s fakty kapacity období

Stránka se seznamy **Plánování kanbanové úlohy** obsahuje okna s fakty zobrazující dostupná a rezervovaná období kapacity pro vybranou pracovní buňku. V závislosti na vybraném plánu období v modelu výrobního toku období zobrazí dny nebo týdny.

## <a name="additional-resources"></a>Další zdroje





[!INCLUDE[footer-include](../../includes/footer-banner.md)]