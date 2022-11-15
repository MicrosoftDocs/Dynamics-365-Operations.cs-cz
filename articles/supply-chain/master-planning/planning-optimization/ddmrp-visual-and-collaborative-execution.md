---
title: Vizuální a společné provádění
description: Tento článek popisuje, jak monitorovat vaše oddělovací body, vyrovnávací zóny, plánované objednávky a historii plánování požadavků na materiál řízený poptávkou (DDMRP).
author: t-benebo
ms.date: 06/30/2022
ms.topic: article
ms.search.form: EcoResProductDetailsExtended, ReqDDMRPWorkspace, ReqDecouplingPointsStatusByNetFlow, ReqDecouplingPointStatusByOnHand, ReqPlannedOrderForm, ReqItemDecoupledLeadTime
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-06-30
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: ce32a4449da8e85f958f212f2c2dfd2841ca6887
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740816"
---
# <a name="visual-and-collaborative-execution"></a>Vizuální a společné provádění

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

Tento článek popisuje, jak monitorovat vaše oddělovací body, vyrovnávací zóny, plánované objednávky a historii plánování požadavků na materiál řízený poptávkou (DDMRP).

## <a name="visually-track-buffers-and-quantities-for-a-selected-item"></a>Vizuálně sledujte vyrovnávací zásoby a množství pro vybranou položku

V Microsoft Dynamics 365 Supply Chain Management můžete vizuálně sledovat, jak se v průběhu času mění vyrovnávací zásoby, množství na skladě a úrovně čistého toku pro jakýkoli vybraný produkt. Podle těchto kroků otevřete a zkontrolujte tabulky.

1. Přejděte na **Řízení informací o produktech \> Produkty \> Uvolněné produkty**.
1. Vyberte uvolněnou položku, která je nastavena jako bod oddělení. (Další informace naleznete v tématu [Umístění zásob](ddmrp-inventory-positioning.md).)
1. V podokně akcí na kartě **Plánování** vyberte **Disponibilita položky**.
1. Na stránce **Disponibilita položky** vyberte záznam disponibility položky, který vytvoří bod oddělení. (Tento záznam zobrazí název skupiny disponibility, která je nastavena tak, aby vytvořila body oddělení.)
1. Vyberte kartu **Na skladě**. Tato karta obsahuje graf, který ukazuje, jak se množství na skladě měnilo v průběhu času, spolu s hodnotou na skladě, která byla zaznamenána za určité období pokaždé, když je spuštěno hlavní plánování. Karta také obsahuje tabulku, která ukazuje, do které z následujících kategorií spadá každá zaznamenaná úroveň:

    - **Kriticky nízké** – Méně než polovina minima za dané období.
    - **Nízký** – Mezi polovinou minima a minimem.
    - **Průměr na skladě** – Mezi minimem a minimem plus zelená zóna.
    - **Nadprůměrný** – Vyšší než průměr.

    ![Historické úrovně na skladě na kartě Na skladě.](media/ddmrp-on-hand-graph.png "Historické úrovně na skladě na kartě Na skladě")

    > [!NOTE]
    > Barvy, které jsou použity na kartě **Na skladě**, představují jiné rozsahy než podobné barvy použité na kartě **Hodnoty vyrovnávacích zásob**.

1. Chcete-li zobrazit, jak se vaše hodnoty vyrovnávacích zásob měnily v průběhu času a jak se porovnávají s úrovněmi na skladě a čistého toku, vyberte kartu **Hodnoty vyrovnávacích zásob**.

    ![Historické úrovně na skladě a úrovně čistého toku na kartě Hodnoty vyrovnávacích zásob.](media/ddmrp-buffer-values-graph.png "Historické úrovně na skladě a úrovně čistého toku na kartě Hodnoty vyrovnávacích zásob")

## <a name="track-the-status-and-planned-orders-for-all-decoupling-points"></a>Sledování stavu a plánovaných objednávek pro všechny body oddělení

Pracovní prostor **MRP řízené poptávkou** poskytuje několik nástrojů spolu s klíčovými ukazateli výkonu (KPI) a přehledy stavu vašich položek bodu oddělení a souvisejících plánovaných zakázek. Chcete-li ho otevřít, přejděte na **Hlavní plánování \> Pracovní prostory \> MRP řízené poptávkou**.

![Pracovní prostor MRP řízená poptávkou.](media/ddmrp-workspace.png "Pracovní prostor MRP řízená poptávkou")

## <a name="get-overviews-of-decoupling-points-and-planned-orders"></a>Získání přehledu o bodech oddělení a plánovaných objednávkách

Vedle pracovního prostoru **MRP řízené poptávkou** Supply Chain Management poskytuje několik stránek, kde si můžete prohlédnout informace o vašem nastavení DDMRP, oddělovacích bodech a plánovaných objednávkách. Některé z těchto stránek také obsahují praktická tlačítka na podokně akcí, která umožňují spravovat vyrovnávací zásoby, spouštět hlavní plánování a otevírat další související zobrazení.

- Chcete-li zobrazit stav oddělovacího bodu podle úrovně čistého toku, přejděte na **Hlavní plánování \> Hlavní plánování \> DDMRP \> Stav oddělení bodů podle čistého toku**.
- Chcete-li zobrazit stav oddělovacího bodu podle úrovně zásob na skladě, přejděte na **Hlavní plánování \> Hlavní plánování \> DDMRP \> Stav oddělení bodů podle zásob na skladě**.
- Chcete-li zobrazit plánované objednávky pro body oddělení, přejděte na **Hlavní plánování \> Hlavní plánování \> DDMRP \> Plánované objednávky pro oddělovací body**.
- Chcete-li zobrazit oddělenou dobu realizace, přejděte na nabídku **Hlavní plánování \> Hlavní plánování \> DDMRP \> Oddělená doba realizace**.

## <a name="clean-up-decoupling-point-buffer-values"></a>Vyčištění hodnot vyrovnávacích zásob oddělovacího bodu

V průběhu času váš systém vytvoří velké množství historických dat, která souvisí s probíhajícími výpočty vyrovnávacích zásob. Tato historická data způsobí nárůst objemu vašich dat a mohou případně ovlivnit výkon vašeho systému. Proto doporučujeme občas vyčistit staré hodnoty vyrovnávacích zásob bodu oddělení.

> [!WARNING]
> Úloha čištění odstraní historická nastavení hodnot vyrovnávacích zásob a historické informace o stavu na skladě / čistém toku. Akci nelze vzít zpět.

Chcete-li vymazat hodnoty vyrovnávacích zásob pro bod oddělení, postupujte podle těchto kroků.

1. Přejděte na nabídku **Hlavní plánování \> Hlavní plánování \> DDMRP \> Vymazat hodnoty vyrovnávacích zásob bodu oddělení**.
1. V dialogovém okně **Vymazat hodnoty vyrovnávacích zásob bodu oddělení** nastavte následující pole:

    - **Odstranit záznamy starší než (dny)** – Určete věk nejmladších záznamů, které se mají uchovávat, ve dnech. Všechny záznamy hodnot vyrovnávacích zásob bodu oddělení, které jsou starší než tato hodnota, budou odstraněny.
    - **Hlavní plán** – Vyberte hlavní plán, který obsahuje položky, které toto mazání ovlivní. Mazání se bude vztahovat na všechny položky v plánu po použití nastavení **Filtr** zadaných v tomto dialogovém okně.

1. Chcete-li omezit sadu záznamů, na kterých má tato dávková úloha běžet, vyberte **Filtr** na záložce **Záznamy, které mají být zahrnuty**, aby se otevřelo dialogové okno **Dotaz**. Toto dialogové okno funguje stejně u jiných typů [prací na pozadí](../../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) v Supply Chain Management.
1. Na záložce s náhledem **Spustit na pozadí** určete, kdy a jak často se má mazání provádět. Pole fungují stejně jako u jiných typů [prací na pozadí](../../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) v Supply Chain Management.
1. Výběrem **OK** přidejte novou úlohu do fronty dávek k vykonání.
