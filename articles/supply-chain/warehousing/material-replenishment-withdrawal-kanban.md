---
title: Doplnění s kanbany odběru
description: Toto téma popisuje, jak se kanban odběru používá pro doplnění materiálu pro výrobní aktivity.
author: johanhoffmann
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardTransferJob, KanbanFlow, KanbanRules
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7fe3ebe3c27c380d95cbc12b864264e9538d433f
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "320919"
---
# <a name="replenishment-with-withdrawal-kanbans"></a>Doplnění s kanbany odběru

[!include [banner](../includes/banner.md)]

Toto téma popisuje, jak se kanban odběru používá pro doplnění materiálu pro výrobní aktivity.

## <a name="workflow-for-material-replenishment-that-uses-the-withdrawal-kanban"></a>Workflow pro doplnění materiálu používající kanban odběru
-------------------------------------------------------------------

Kanban odběru lze použít k přesunutí kanbanu jedné položky mezi sklady a výrobními lokalitami, kde se spotřebovává materiál. Kanban odběru podporuje řešení založené na vyžádání doplnění materiálu, kdy je požadována signály vyžádání za účelem aktivace dodávky pro konkrétní poptávky. 

Následující scénář zobrazuje systém doplňování na vyžádání, kde signál vyžádání vyvolá vytvoření kanbanu k doplnění materiálu pro výrobní proces. 

[![Signál vyžádání vyvolá událost vytvoření kanbanu k doplnění materiálu pro výrobní proces](./media/material-replenishment-with-withdrawal-kanban.png)](./media/material-replenishment-with-withdrawal-kanban.png)

1.  Kanban odběru
2.  Kanban z místa a umístění pro příjem skladu práce
3.  Kanban do umístění a vstupní místo výroby
4.  Výrobní proces
5.  Skladová práce pro výdej ve skladu
6.  Skladová místa pro suroviny
7.  Sklad materiálu
8.  Výrobní sklad

V tomto scénáři výrobní proces (4) spotřebovává materiál ze vstupního místa výroby (3) ve výrobním skladu (8). Když se manipulační jednotka materiálu (kanban) spotřebovává, je registrována jako prázdná. Signál doplnění je vytvořen pro původní položku a je vytvořen nový kanban (1). V takovém případě původ položky sestává ze skladových míst ve skladu materiálu [7]. Materiál pro kanban je vydán a umístěn do skladovacího místa (2) ve stejném skladu. Při vyskladnění je materiál připraven pro převod z místa 2 do vstupního místa výroby (3) ve výrobním skladu (8).

## <a name="configure-warehouse-work-for-kanban-picking-for-the-withdrawal-kanban"></a>Konfigurace práce ve skladu pro vyzvednutí kanban u kanbanového odběru

Povolení vyzvednutí surovin pro kanban odběru, konfigurace šablon vlny, pracovních šablon a směrnic pro pracovní místo pro typ pracovního příkazu **Kanban – výdej**. Tento typ pořadí pracovních činností neslouží jenom na podporu procesu výdeje pro kanban odběru. Podporuje také proces vyskladnění pro výrobní kanban. Můžete však nakonfigurovat samostatný postup výdeje pro každý typ kanbanu oddělením šablony vlny, šablon práce a směrnic skladového místa. Když chcete oddělit šablony vlny, šablony práce a směrnice skladového místa, můžete nastavit kritéria pro daný typ aktivity (**proces** nebo **převod**) v dotazech pro tyto entity.

## <a name="configure-the-withdrawal-kanban"></a>Konfigurace kanbanu odběru

Aktivita převodu, která se používá pro kanban odběru, je nakonfigurována jako součást aktivované ho plánu aktivity do toku štíhlé výroby. V rámci konfigurace aktivity přenosu zadáte skladová místa "od" a "do" pro převod. Po konfiguraci aktivitu převodu ji můžete přiřadit kanbanovému pravidlu typu **výběr**. Kanbanové pravidlo stanoví zásady a konfigurace pro kanban odběru. Množství kanbanu definuje množství manipulačních jednotek kanbanu, které kanban při procesu převodu zvládá. Pevné množství kanban se použije, když je vybrána strategie pevného doplnění. Toto množství definuje počet kanbanů, které jsou zapotřebí k zabránění vyčerpání stavebního materiálu ve zdroji poptávky. Pevné množství lze vypočítat na základě skutečné poptávky, historické poptávky a úrovně služeb. Následující dva scénáře popisují, jak spravovat doplnění materiálu používající kanban odběru.

## <a name="scenario-1-replenish-a-production-input-location-by-using-a-fixed-withdrawal-kanban"></a>Scénář 1: Doplnění vstupního místa výroby pomocí pevného kanbanu odběru

Výrobní proces spotřebovává zakoupené suroviny ze vstupního místa výroby, které je ve výrobním skladu. Při přijetí suroviny od dodavatele se surovina uloží do skladu materiálu. Vzhledem k tomu, že poptávka po materiálu je považována za stabilní pro dané období, je nastavena na dodávky do výroby v kanbanovém toku v pevném množství. Když se kanban spotřebovává ve vstupním místě výroby, je registrován prázdný signál a do toku je přidán nový kanban stejného typu. 

Prázdný signál lze konfigurovat tak, aby proběhl automaticky při dokončení kanbanu. Případně lze nastavit prázdný signál jako ruční interakci, která je určena z převodní kanbanové desky nebo z nabídky handheldového zařízení. Převodní kanbanová deska je pracovní prostor, kde jsou spravovány všechny činnosti v cyklu životnosti kanbanu. 

Po vytvoření kanbanu je přidán řádek pro surovinu do kanbanové vlny skladu materiálu. V části výdeje seznam převodů kanbanu lze sledovat stav materiálu a související procesy skladu od vytvoření vlny do vytvoření práce, dokud nebude materiál na skladě v umístění "převod z" a připraven na převod do místa výrobního vstupu. Kanban lze dokončit z převodní kanbanové desky nebo nabídky handheldového zařízení. 

V tomto scénáře je práce výdeje ve skladu materiálu zpracována jako jedna aktivita. Aktivita převodu mezi skladem materiálu a skladem výroby je zpracována jako samostatná aktivita. Tento přístup může být užitečný například pokud se jedná o velkou fyzickou vzdálenost mezi dvěma sklady. Aktivita převodu kanbanu v tomto případě může představovat vytížení dodávky. 

Při malé vzdálenost mezi skladovými místy a vstupním místem výroby může být efektivnější zahrnout aktivitu převodu při vyskladnění. Po výdeji materiálu ho pak lze umístit přímo na vstupní místo výroby. Chcete-li podpořit tento proces, nakonfigurujte aktivitu převodu tak, aby se doplnila automaticky při zpracování práce výdeje kanbanu odběru.

## <a name="scenario-2-automatically-complete-the-transfer-activity-when-kanban-picking-work-is-processed"></a>Scénář 2: Automatické dokončení aktivity převodu při zpracování práce výdeje kanbanu

V následujícím scénáři je nakonfigurována aktivita kanbanu převodu na převod mezi dvěma místy ve stejném skladu. Aktivita převodu kanbanu odběru je nastavena tak, aby se doplnila automaticky. 

[![Automatické doplnění aktivity převodu při zpracování práce výdeje kanbanu](./media/transfer-activities-when-processing-kanban-picking.png)](./media/transfer-activities-when-processing-kanban-picking.png)

1.  Sdílený sklad pro suroviny a výrobu
2.  Skladová místa pro suroviny
3.  Kanban z místa a umístění pro příjem skladu práce
4.  Kanban odběru
5.  Vstupní místo výroby
6.  Výrobní proces

Když se kanban spotřebovává ve vstupním místě výroby, je vykazován jako prázdný signál a do toku je přidán nový kanban stejného typu. Po vytvoření kanbanu se do vlny kanbanu přidá řádek vlny. Při zpracování vlny kanbanu se vytvoří skladová práce vyskladnění kanbanu. Pracovník skladu zpracuje práci pro výdej kanbanu a je nasměrován na výdej materiálu pro kanban ve skladovém místě. Když tento pracovník skladu potvrdí vyskladnění, kanban bude automaticky doplněn a pracovník skladu dostane pokyn k vložení materiálu do vstupního skladového místa.

