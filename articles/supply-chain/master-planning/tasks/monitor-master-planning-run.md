---
title: Sledování běhu hlavního plánování
description: Toto téma vysvětluje, jak může plánovač provozu sledovat, zda probíhá hlavní spuštění plánování.
author: ChristianRytt
ms.date: 11/04/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, InventItemIdLookupSimple, ReqLog, ReqProcessTaskTrace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4db1173b35cd196ab39fae3cac3754439fab84d0
ms.sourcegitcommit: fcb8a3419e3597fe855cae9eb21333698518c2c7
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/09/2022
ms.locfileid: "8103156"
---
# <a name="monitor-a-master-planning-run"></a>Sledování běhu hlavního plánování

[!include [banner](../../includes/banner.md)]

## <a name="use-a-gantt-chart-to-visualize-master-planning-progress"></a>Použít Ganttův diagram ke znázornění průběhu hlavního plánování

Na stránce **Zobrazit průběh hlavního plánování** můžete zobrazit podrobné informace o historickém běhu hlavního plánování jako Ganttův diagram. Tato funkce vám může pomoci pochopit čas strávený v různých fázích hlavního plánování. Pro aktuální aktivní úlohu plánování lze pomocí stránky **Zobrazit průběh hlavního plánování** sledovat průběh a zobrazit odhadovanou zbývající dobu.

### <a name="turn-the-master-plan-progress-visualization-feature-on-or-off"></a>Zapnutí a vypnutí funkce vizualizace průběhu hlavního plánu

Od verze Supply Chain Management 10.0.21 je tato funkce ve výchozím nastavení zapnuta. Od verze Supply Chain Management 10.0.25 je tato funkce povinná a nelze ji vypnout. Pokud používáte verzi starší než 10.0.25, mohou správci tuto funkčnost zapnout nebo vypnout vyhledáním funkce *Znázornění průběhu hlavního plánování* v pracovním prostoru [Správa funkcí](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="use-the-master-plan-progress-visualization-feature"></a>Používání funkce vizualizace průběhu hlavního plánu

Na stránce **Zobrazit průběh hlavního plánování** lze zobrazit historické úlohy plánování i aktivní úlohy plánování. 

Chcete-li zobrazit historické úlohy plánování, existují dvě možnosti. 

1. Přejděte na **Hlavní plánování \> Nastavení \> Plány \> Hlavní plány** a v podokně úloh vyberte **Historie**. Při výběru požadované úlohy vyberte možnost **Dotazy** a poté vyberte možnost **Zobrazit průběh**
1. Přejděte na **Hlavní plánování \> Pracovní prostory \> Hlavní plánování** a na kartě Hlavní plánování klikněte na **Historie**. Při výběru požadované úlohy vyberte možnost **Dotazy** a poté vyberte možnost **Zobrazit průběh**

Chcete-li zobrazit aktivní úlohy plánování, existují dvě možnosti. 
1. Přejděte na **Hlavní plánování \> Pracovní prostory \> Hlavní plánování**, v podokně úloh vyberte **Nedokončený proces plánování**. Při výběru požadované úlohy vyberte možnost **Dotazy** a poté vyberte možnost **Zobrazit průběh**.
1. Přejděte na **Hlavní plánování \> Pracovní prostory \> Hlavní plánování** a na kartě Hlavní plánování klikněte na **Zobrazit průběh**. Při výběru požadované úlohy vyberte možnost **Dotazy** a poté vyberte možnost **Zobrazit průběh**

Všimněte si, že aktivní úlohy lze zobrazit pouze při zpracování úlohy plánování.

### <a name="analyze-a-master-planning-job"></a>Analýza úlohy hlavního plánování

V Ganttově diagramu můžete rozbalit všechny následující procesy plánování a zobrazit tak další podrobnosti o době strávené tímto způsobem:

- Inicializace
- Odstranění a vložení dat
- Plánování disponibility
- Zpoždění
- Zprávy akce
- Vyrovnání záloh
- Automatické potvrzování

Ganttův diagram je užitečný nástroj, pokud chcete zobrazit dopad zpráv s akcemi.

#### <a name="navigation-in-the-gantt-chart"></a>Navigace v Ganttově diagramu

- Chcete-li rozbalit vybranou skupinu a zobrazit podrobnosti, vyberte ve stromovém zobrazení znaménko plus (**+**).
- Chcete-li sbalit vybranou skupinu, vyberte ve stromovém zobrazení znaménko mínus (**-**).
- K navigaci můžete používat klávesnici. K pohybu mezi řádky používejte **šipku nahoru** a **šipku dolů**. K rozbalení a sbalení skupin použijte klávesy **šipka vpravo** a **šipka vlevo**.
- Chcete-li otevřít nebo zavřít všechny úrovně v Ganttově diagramu, vyberte možnost **rozbalit vše** nebo **Sbalit vše**.
- Chcete-li zobrazit související čas zpracování, podržte ukazatel myši nad úkolem. (Úkoly jsou na nejnižší úrovni v Ganttově diagramu.)

#### <a name="view-an-additional-master-planning-run-to-compare-jobs"></a>Zobrazení dalšího spuštění hlavního plánování pro porovnání úloh

Výběrem úlohy hlavního plánování v poli **Zobrazit další spuštění hlavního plánování** můžete zobrazit další spuštění hlavního plánování v Ganttově diagramu a porovnat tyto dvě úlohy.

#### <a name="bom-level-display"></a>Zobrazení na úrovni kusovníku

Úrovně kusovníku se zobrazují různě pro plánování disponibility, zpoždění, akce a potvrzování.

- **Plánování disponibility** – úrovně kusovníku se zobrazují očekávaným způsobem. Ty jsou vypočteny shora dolů.

    **Příklad:** úroveň kusovníku 0, 1, 2

- **Zpoždění** – úrovně kusovníku se zobrazují jako úrovně kusovníku plánování disponibility násobené hodnotou-1. (Jinými slovy, mají záporné znaménko.)

    **Příklad:** úroveň kusovníku –2, –1, 0

- **Zpráva akce** – úrovně kusovníku se zobrazují očekávaným způsobem. Ty jsou vypočteny shora dolů.

    **Příklad:** úroveň kusovníku 0, 1, 2

- **Automatické potvrzení** – úrovně kusovníku jsou zobrazeny jako 999 mínus úroveň kusovníku plánování disponibility.

    **Příklad:** úroveň kusovníku 999, 998, 997

Chování je shrnuto v následující tabulce.

| Zobrazená úroveň kusovníku | Koncové zboží | Dílčí komponenta | Surovina |
|---|---|---|---|
| Plánování disponibility | 0 | 1 | 2 |
| Zpoždění | 0 | –1 | –2 |
| Zpráva akce | 0 | 1 | 2 |
| Automatické potvrzování | 999 | 998 | 997 |

#### <a name="visualize-progress"></a>Průběh vizualizace

Pokud zobrazíte úlohu hlavního plánování, která je aktuálně spuštěna, zobrazí se průběh v Ganttově diagramu prostřednictvím barev. Pro modrý motiv se aplikují následující barvy: U jiných barevných motivů se barvy liší.

- **Tmavě modrá** – dokončené plánované úkoly.
- **Oranžová** – úkol, který právě probíhá.
- **Světle modrá** – odhad pro zbývající úkoly.

Barva se zobrazí pouze na nejnižší úrovni v Ganttově diagramu. Výběrem možnosti **Rozbalit vše** zobrazte všechny úkoly v rámci úlohy hlavního plánování. Odhad zbývajících úkolů je založen na historických úlohách hlavního plánování.

## <a name="run-master-planning-and-track-processing-time"></a>Spustit hlavní plánování a sledovat čas zpracování

1. Na výchozím řídicím panelu vyberte **Hlavní plánování**.
1. V poli **Plán** zadejte nebo vyberte hodnotu.
1. Vyberte **Spustit**.
1. Nastavte možnost **Sledovat čas zpracování** na **Ano**.
1. Do pole **Počet vláken** zadejte číslo.
1. Na pevné záložce **záznamy, které mají být zahrnuty** vyberte možnost **Filtr**.
1. V mřížce vyberte řádek, ve kterém je pole **Pole** nastaveno na **číslo položky**.
1. Zadejte hodnotu do pole **Kritéria**.
1. Vyberte **OK**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]