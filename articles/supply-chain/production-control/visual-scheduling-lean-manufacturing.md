---
title: "Vizuální plánování pro lean manufacturing"
description: "Toto téma obsahuje informace o desce plánování kanbanu, kterou Plánovač výroby může používat k řízení a optimalizaci výrobního plánu pro kanbanové úlohy."
author: johanhoffmann
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: KanbanBoard, KanbanJobSchedulingListPage, LeanProductionFlowVisualization
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 6218f54364e096bdd718ea35edb0b3666e65f2c1
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---

# <a name="visual-scheduling-for-lean-manufacturing"></a>Vizuální plánování pro lean manufacturing

[!include[banner](../includes/banner.md)]


Toto téma obsahuje informace o desce plánování kanbanu, kterou Plánovač výroby může používat k řízení a optimalizaci výrobního plánu pro kanbanové úlohy.

Toto téma obsahuje informace o desce plánování kanbanu, kterou Plánovač výroby může používat k řízení a optimalizaci výrobního plánu pro kanbanové úlohy.

Rozvrh plánování kanbanu umožňuje plánovači výroby řídit a optimalizovat plán výroby pro kanbanové úlohy. Zajišťuje transparentní tok kanbanových úloh a poskytuje plánovači výroby nástroj, který optimalizuje a upravuje výrobní plánu pro pracovní buňku lean manufacturing.

## <a name="visual-scheduling-of-kanban-jobs"></a>Vizuální plánování kanbanové úlohy
Kanbanová úloha se může skládat z jedné nebo mnoha kanbanových úloh. Existují dva typy kanbanových úloh:

-   Zpracovat
-   Převod

Je možné plánovat pouze úlohy typu **Proces**. Kanbanová úloha a její vlastnosti, jako je čas aktivity, jsou definovány ve výrobním toku kanbanu. V průběhu výrobního kanbanu je kanbanová úloha přiřazena také k pracovní buňce. Denní kapacity pracovní buňky je vypočtena na základě kapacity pracovní buňky nastavené ve skupině prostředků. Je upravena podle denní pracovní doby v souvisejícím kalendáři. Při plánování kanbanové úlohy úloha načte kapacitu pracovní buňky. Deska plánování kanbanu obsahuje následující hlavní funkce:

-   Grafické zobrazení plánu výroby v pracovní buňce lean. V tomto přehledu se zobrazují plánované kanbanové úlohy procesu v určitých obdobích.
-   Nástroj, který umožňuje naplánovat neplánované kanbanové úlohy a přeplánovat dříve naplánované úlohy.

## <a name="kanban-schedule-board"></a>Rozvrh plánování kanbanu
Stránka **Deska plánování kanbanu** stránka obsahuje sedm hlavních prvků, jak je uvedeno na následujícím obrázku. 

![Rozvrh plánování kanbanu](./media/kanban-schedule-board-1024x554.png)
1.  Podokno akcí
2.  Filtrovat pole
3.  Tlačítko pro neplánované úlohy
4.  Uzel období
5.  Kanbanová úloha
6.  Panel kapacity
7.  Časové měřítko

### <a name="view-the-time-scale"></a>Zobrazit časové měřítko

Deska je rozdělena do období, z nichž každé je vyjádřeno jako uzel (4). Uzly období, které jsou uvedeny na svislé ose, a vodorovných osách, představují časové měřítko (7) zobrazující délku období. Období má délku jeden den nebo jeden týden. Délka období je určena konfigurací pracovní buňky, která je vybrána pro desku plánu Kanbanu (2). Pro každý uzel období ukazuje deska plánu kanbanu, kolik plánovaných kanbanových úloh načítá období. Je zde také indikace maximální propustnosti období. Pokud plánovaná propustnost překračuje maximální propustnost, období se považuje za přetížené a zobrazí se červený výstražný symbol. Plánovaná kanbanová úlohy se zobrazí v období, které má plánovaný počáteční a koncový čas (5). Délka úlohy se rovná času aktivity. Kanbanové úlohy se zobrazují jako překrývající se za období, pokud jejich časy aktivit překročí délku výrobního taktu pracovní buňky.

### <a name="view-job-status"></a>Zobrazení stavu úlohy

Další informace o kanbanové úloze jsou k dispozici v popisu, který se zobrazí při umístění ukazatele myši na úlohu. Symbol obsahuje informace o stavu úlohy. Například symbol hodin znamená, že je kanbanová úloha po termínu plnění.

### <a name="use-colors-to-view-the-kanban-schedule-board"></a>Pomocí barev lze zobrazit, desku plánování kanbanu

K vylepšení přehledu, který deska plánování kanbanu poskytuje, můžete použít barvy k rozlišení kanbanových úloh. Barva kanbanové úlohy není konfigurována ve skupině štíhlého plánu, kde lze agregovat produkty, které se mají vyrobit ve stejném pořadí. Tlačítko **Použít barvy motivu** na kartě **Deska** podokna akcí umožňuje přepínat mezi barvami motivu aplikace a barvami, které jsou konfigurovány ve skupině štíhlého plánu. Pro každé období označuje panel kapacity (6) počet dostupných hodin pro období bylo načteno v rámci kanbanové úlohy. Pokud je období přetížené, panel kapacity vypadá silnější a zobrazuje se červeně. Všechny tyto funkce jsou k dispozici na kartě **deska** podokna akcí (1), v horní části stránky **Deska plánování kanbanu**.

## <a name="plan-unplanned-jobs"></a>Naplánovat neplánované úlohy
Můžete naplánovat neplánované kanbanové úlohy z dialogového okna **Naplánovat neplánované úlohy**. Toto dialogové okno otevřete kliknutím na tlačítko **Neplánované úlohy**, na kterém je zobrazeno číslo neplánovaných úloh. Případně klikněte na tlačítko **Naplánovat neplánované úlohy** na kartě **deska** podokna akcí. V dialogovém okně se zobrazuje seznam neplánovaných kanbanových úloh pro pracovní buňku. K filtrování všech polí v mřížce lze použít pole **Filtr**. Můžete například filtrovat kanbanové úlohy pro konkrétní produkt. Poté, co máte filtrovaný seznam úloh, které chcete naplánovat, vyberte je v seznamu a klepněte na tlačítko **OK**. Pokud chcete k plánování úloh použít automatické plánování, nastavte možnost **Automatické plánování** na **Ano**. V takovém případě jsou úlohy plánovány na období podle data splatnosti. Úlohy je možné plánovat také podle období. Stačí vybrat období v poli **Období**. Následující obrázek znázorňuje příklad dialogového okna **Naplánovat neplánované úlohy**. 

![Dialogové okno Naplánovat neplánované úlohy](./media/plan-unplanned-jobs-1024x564.png)

## <a name="sequence-kanban-jobs-within-the-same-period"></a>Pořadí kanbanových úloh ve stejném období
V rámci období můžete změnit pořadí jeden nebo více vybraných úloh. Tato možnost může být užitečná, pokud chcete určit prioritu některých úloh v rámci období. Případně můžete vytvořit sekvenci úloh, které mají stejné atributy produktu, k optimalizaci provádění úloh. Sekvenci můžete změnit přetažením nebo pomocí číselné řady **zpět** a **dopředu** a položek nabídky na kartě **Deska** podokna akcí.

## <a name="reassign-kanban-jobs-across-periods"></a>Opětné přiřazení kanbanových úloh napříč obdobími
Úlohy můžete znovu přiřadit z jednoho období do jiného. Tato možnost může být užitečná, pokud je období přetíženo a chcete vyrovnat vytížení s obdobími, která mají náhradní kapacitu. Úlohy můžete znovu přiřazovat přetažením nebo pomocí položek nabídky **Další období** a **Předchozí období** na kartě **Deska** podokna akcí.

## <a name="open-the-kanban-schedule-board"></a>Otevření desky plánu kanbanu
Desku plánování kanbanu můžete otevřít pomocí položky nabídky na následujících stránkách:

-   Stránka **Výrobní oblast**
-   Stránka **Plánování kanbanových úloh**
-   Stránka **Vizualizace výrobního toku**


<a name="see-also"></a>Viz také
--------

[Lean manufacturing – plánování kanbanové úlohy](lean-manufacturing-kanban-job-scheduling.md)


