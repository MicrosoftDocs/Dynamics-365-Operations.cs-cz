---
title: "Odhad nákladů výrobní zakázky"
description: "V tomto článku jsou informace o odhadu výrobních nákladů. Odhad výrobních nákladů poskytuje předpokládané náklady na spotřebu materiálu a kapacity při výrobě položky v plánovaném množství výrobní zakázky."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: BOMCalcTrans, InventCostTrans, ProdCalcTrans, ProdTableJour, ProdTableListPage
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 80633
ms.assetid: b4625d10-c852-4fda-b718-79df458de0d4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 3d43b186335b42fd5b7b6c84456d012f51b26799
ms.lasthandoff: 03/31/2017


---

# <a name="production-order-cost-estimation"></a>Odhad nákladů výrobní zakázky

[!include[banner](../includes/banner.md)]


V tomto článku jsou informace o odhadu výrobních nákladů. Odhad výrobních nákladů poskytuje předpokládané náklady na spotřebu materiálu a kapacity při výrobě položky v plánovaném množství výrobní zakázky. 

Po vytvoření výrobní zakázky je nutné odhadnout výrobní náklady. Účelem je odhad spotřeby položek a postupu pro výrobní proces, protože tyto odhady slouží jako základ následného plánování a výrobních procesů.

## <a name="production-cost-estimation"></a>Odhad výrobních nákladů
Odhady výrobních nákladů jsou založeny na následujících informacích:

-   množství ve výrobní zakázce,
-   součásti ve výrobních kusovnících (BOM),
-   operace postupu ve výrobním postupu,
-   nepřímé náklady, které se týkají součástí a operací,
-   údaje aktivních nákladů k datu výpočtu.

Pokud je položka fiktivního řádku ve výrobních kusovnících, budou výpočty odpovídat součástem a operacím postupu fiktivní položky. Pomocí úlohy odhadu lze přepočítat odhadované náklady, aby odrážely aktualizované údaje. Aktualizovanými údaji mohou být například změny v množství výrobní zakázky, komponenty ve výrobních kusovnících, operace ve výrobním postupu, nepřímé náklady, které lze platí pro tyto součásti a operace, nebo údaje aktivních nákladů k datu přepočítání. Při výpočtech odhadovaných nákladů je také navržena prodejní cena pro výrobní položku na základě přístupu náklady plus přirážka. Výpočty odhadovaných nákladů se mohou volitelně týkat referenčních objednávek, které odpovídají jiným výrobním zakázkám připojeným k dané výrobní zakázce.

## <a name="view-the-estimated-costs"></a>Zobrazení odhadovaných nákladů
Po spuštění odhadu lze výsledky zobrazit na stránce **Kalkulace ceny**. Odhad vypočte následující hodnoty:

-   **Výrobní náklady**: Výrobní náklady jsou na horním řádku odhadu. Zobrazuje celkové náklady na spuštění výrobní zakázky a celkovou prodejní cenu produkce. Jedná se o součet všech řádků nákladů v odhadu.
-   **Náklady na postup nebo prostředek**: Jsou to náklady pro výrobní operace. Patří mezi ně náklady prvků, jako je například přípravný čas, operační čas a režijní náklady.
-   **Náklady na materiál**: Jedná se o náklady a ceny součástí kusovníku vyžadovaných k výrobě položky. Tyto náklady byly zjištěny dříve a zadány do systému.

## <a name="other-uses-of-cost-estimation"></a>Další využití odhadu nákladů
Odhad nákladů také poskytuje následující informace:

-   smysluplné cenové nabídky,
-   odhady ziskovosti dané zakázky,
-   odhady použití surovin,
-   porovnání informací o nákladech z předchozí výroby,
-   informace o rozpočtu a prognóze,
-   odhady objemu výroby vyžadovaného k udržení konkrétních nákladů.




