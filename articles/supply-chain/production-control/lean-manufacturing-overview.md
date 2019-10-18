---
title: Lean manufacturing - přehled
description: Tento článek poskytuje přehled a popis funkcí lean manufacturing v aplikaci Dynamics 365 Supply Chain Management.
author: ChristianRytt
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardTransferJob, KanbanBoardWorkCell, KanbanJobSchedulingListPage, LeanProductionFlow
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19371
ms.assetid: 026c5605-6be7-4fdb-a6f2-8e37a806796c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d338318d3f7a1b56fe98e5c093ccbe795bd8de44
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250065"
---
# <a name="lean-manufacturing-overview"></a>Lean manufacturing – přehled

[!include [banner](../includes/banner.md)]

Tento článek poskytuje přehled a popis funkcí lean manufacturing v aplikaci Dynamics 365 Supply Chain Management.

Lean manufacturing nabízí nástroje, které lze použít k modelování štíhlých operací. Tyto nástroje podporují následující koncepce a podnikatelské činnosti:
-   Vytvoření základu pro lean manufacturing modelováním výroby a logistických procesů do podoby výrobních toků.
-   Implementace štíhlého poptávkového systému pomocí kanbanů pro signalizaci požadavků poptávky.
-   Sledování a správa kanbanovových úloh.

Architektura lean manufacturing obsahuje výrobní toky, aktivity a kanbanová pravidla. Tyto struktury jsou plně integrovány do procesů Supply Chain Management. Lean manufacturing můžete použít ve smíšeném výrobní prostředí, ve kterém se kombinují různé strategie dodávek, výroby a zdrojů. Tyto strategie zahrnují výrobní zakázky, dávkové objednávky pro zpracovatelské odvětví, nákupní objednávky a převodní příkazy.

| **Důležité**                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Aplikaci Supply Chain Management můžete použít k podpoře implementace lean manufacturingu s kanbany. Úspěšná implementace zásad štíhlé výroby však závisí na vnitřních obchodních procesech, které používáte, a skutečných výrobních podmínkách a prostředí. |

## <a name="modeling-manufacturing-and-logistics-processes-as-production-flows"></a> Modelování procesů výroby a logistiky do podoby výrobních toků
Základ pro lean manufacturing lze vytvořit modelováním výroby a logistických procesů do podoby výrobních toků. Tato aktivita se skládá z následujících úloh:
1.  Určete procesy, u kterých chcete implementovat strategii štíhlého doplnění, a poté tyto procesy namodelujte jako výrobní toky. Následně můžete procesy analyzovat a zefektivnit. Jedním z cílů štíhlé implementace je omezení plýtvání zdokonalením toku materiálů a informací.
2.  Výrobní tok definujte jako sekvenci aktivit, které popisují průběh materiálu. Aktivita převodu definuje pohyb jednoho nebo více produktů z jednoho místa na druhé. Aktivita procesu definuje operace s přidanou hodnotou, které jsou použity pro produkt.
3.  Vytvořte verzi výrobního toku, která definuje požadavky pro délku výrobního taktu. Tyto požadavky se používají k výpočtu časů cyklu každé aktivity ve výrobním toku. Můžete vytvořit několik verzí výrobních toků a poté zlepšovat procesy pomocí těchto verzí.

## <a name="using-kanbans-to-signal-demand-requirements"></a> Použití kanbanů k signalizaci požadavků poptávky
U poptávkového systému se zboží vyrobí jen tehdy, když je potřeba. Tento postup zkracuje dodací lhůtu a omezuje nadbytečné množství zásob. Kanbany můžete použít k plánování, sledování a zpracování požadavků, které jsou založeny na výrobních tocích. Kanbanové prostředí vytvoříte tak, že vytvoříte kanbanová pravidla, která definují, kdy se kanbany vytváří a jak jsou splněny požadavky. Můžete vytvářet dva typy kanbanových pravidel. Výrobní pravidla vytváří kanbanové úlohy procesu a odvolací kanbanová pravidla vytváří kanbanové úlohy převodu. Můžete nastavit následující strategie doplnění:
-   Kanbanová pravidla **Pevné množství** se vztahují k pevnému počtu manipulačních jednotek, což znamená, že počet aktivních kanbanů je konstantní. Vždy, když jsou spotřebovány všechny výrobky z Kanban a manipulační jednotky jsou ručně vyprázdněny, je vytvořen nový kanban stejného typu.Při vytváření pravidel pevného množství kanban můžete vypočítat optimální kanbanová množství a množství produktů, které jsou používány. Výpočet zohledňuje prognózy, skutečnou poptávku z otevřených objednávek, dobu realizace doplňování položek a historické požadavky.
-   Kanbanová pravidla **Plánováno** doplňují požadavky, které jsou vypočítány hlavním plánováním. Hlavní plánování generuje plánované kanbany, které mohou být potvrzeny na kanbany.
-   Kanbanová pravidla **Událost** doplňují požadavky, které pocházejí z řádků prodejní objednávky, řádků výrobního kusovníku, řádků kanbanu nebo nastaveného skladového minima. Při vygenerování se kanbany události propojí s požadavky na zdroj.

Po vytvoření kanbanů je na základě aktivit kanbanového toku, které jsou definovány v kanbanových pravidlech, vygenerována jedna nebo více kanbanových úloh.

## <a name="monitoring-and-maintaining-kanban-jobs"></a> Sledování a správa kanbanovových úloh
Lean manufacturing dává přehled o aktuálním stavu aktivit výroby a logistiky, které se řídí kanbanovými pravidly. V důsledku toho můžete plánovat a přiřazovat priority těmto úkolům:

-   Získání přehledu o aktuálním plánu kanbanové úlohy.
-   Plánování a přeplánování kanbanových úloh.
-   Sledování a registrace stavu kanbanových úloh.

V následujícím seznamu jsou popsány speciální kanbanové desky:
-   Plánování kanbanové úlohy – dává přehled o kanbanových úlohách. Deska zobrazuje kanbanové úlohy a jejich stav pro jednu nebo více pracovních buněk. Úlohy jsou uvedeny podle období plánování (dny nebo týdny), které jsou definovány v modelu výrobního toku. Na desce se zobrazuje také spotřeba kapacity pro každé období plánování, takže můžete sledovat naplánované vytížení. Můžete měnit stav kanbanových úloh, přeplánovat kanbanové úlohy na různá období plánování a provádět další úlohy.
-   Kanbanová deska pro úlohy převodu – dává přehled o aktuálních úlohách převodu. Můžete aktualizovat a registrovat výdejky, zahajovat a dokončovat úlohy převodu a provádět další úlohy.
-   Kanbanová deska pro úlohy procesu – tato deska slouží k podpoře normálního výrobního toku a dává přehled o aktuální situaci v jedné nebo více pracovních buňkách. Na této desce lze kanbanům určit prioritu, vyskladnit je nebo vyrobit. Správní slouží také k podpoře snímání čárových kódů pro potřeby vykazování kanbanů.

## <a name="kanban-jobs-and-integration-with-supply-chain-management-processes"></a>Kanbanové úlohy a integrace s procesy Supply Chain Management
Kanbanové úlohy jsou plně integrovány do aktuálních procesů pro skladové transakce v aplikaci Supply Chain Management.
-   Můžete provádět aktivity vyskladnění k doplnění materiálu, který se používá ke splnění požadavků kanbanových úloh.
-   Můžete vytisknout kanbanové karty, kolující kanbanové karty a výdejky, aby se kanbany lépe používaly. Tyto dokumenty představují sledování a registraci kanbanových úloh ve skladu a Dílenské výrobě.
-   Sejmutím čárového kódu můžete zaregistrovat aktivity výdeje a převodu ve skladu.

Lean manufacturing kromě toho podporuje procesy nákupů a fakturování služeb, na které odkazují subdodavatelské aktivity.
-   Řádky nákupní smlouvy a služby můžete přiřazovat subdodavatelským aktivitám.
-   Můžete vytvořit pravidelné nákupní objednávky a avíza příjmových dokladů a usnadnit tak nákup a fakturaci služeb.





