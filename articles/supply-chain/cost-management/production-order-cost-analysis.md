---
title: Analýza nákladů ve výrobní zakázce
description: Tento článek obsahuje informace o analýze nákladů, kterou lze provést pro dokončené a aktuální výrobní zakázky. Můžete analyzovat odhadované náklady a skutečné náklady na stránce Kalkulace ceny nebo pomocí sestavy Odhad a výpočet nákladů. Můžete sledovat informace o odhadovaných a skutečných nákladech (a množství) jsou zobrazeny pro každou položku komponenty, operaci postupu a nepřímé náklady.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventCostTrans, ProdCalcTrans, ProdTableJour, ProdTableListPage, ProdSetupHistoricalCost
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 79634
ms.assetid: ded5da04-f787-49f7-b5e5-75c2a2b92930
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dcc155a7fe5ca16e7543bf5917dbedadef987b62
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4423899"
---
# <a name="production-order-cost-analysis"></a>Analýza nákladů ve výrobní zakázce

[!include [banner](../includes/banner.md)]

Tento článek obsahuje informace o analýze nákladů, kterou lze provést pro dokončené a aktuální výrobní zakázky. Můžete analyzovat odhadované náklady a skutečné náklady na stránce Kalkulace ceny nebo pomocí sestavy Odhad a výpočet nákladů. Můžete sledovat informace o odhadovaných a skutečných nákladech (a množství) jsou zobrazeny pro každou položku komponenty, operaci postupu a nepřímé náklady.

Skutečné náklady pro výrobní zakázku závisejí na vykázané spotřebě materiálu a na provedených operacích postupu. K podrobným informacím transakcí o vykázané spotřebě materiálu, operacích postupu a nepřímých nákladech pro výrobní zakázku lze získat přístup na stránce **Zaúčtování výroby**.

## <a name="variance-analysis-for-a-completed-production-order"></a>Analýza odchylek u dokončených výrobních zakázek
Odchylky jsou výsledkem porovnání vykázaných výrobních činností s výpočtem standardních nákladů pro vyrobenou položku. Odchylky nenabízí porovnání s odhadovanými náklady na výrobní zakázku. Do vykázaných výrobních činností patří spotřeba materiálu, operace technologického postupu (společně se souvisejícími nepřímými náklady) a ohlášené dokončené množství. Jsou vypočteny následující čtyři verze hodnot nákladů:

-   Odchylka velikosti šarže
-   Výrobní odchylka množství
-   Odchylka výrobní ceny
-   Výrobní odchylka náhrady

V následujícím diagramu jsou uvedeny tyto čtyři odchylky, které způsobují rozdíl mezi skutečnými náklady na výrobní zakázku a náklady kalkulovanými v rámci záznamu o ceně položky v okamžiku ukončení výrobní zakázky. 

![Odchylky, které představují rozdíly v dokončené výrobní zakázce](./media/control.jpg) 

Výrobní odchylky lze analyzovat prostřednictvím stránky **Odchylka** nebo sestavy **Výrobní odchylka**. Uvedené možnosti umožňují prohlédnout si podrobné odchylky podle položek a provozních prostředků, nebo podle nákladové skupiny. Zásady pro rozúčtování nákladů v parametrech zásob určují, zda budou odchylky sledovány podle nákladových skupin. Můžete také použít možnost zobrazení **jediná**, **více** a **celkem** umožňující zobrazení souhrnných odchylek. Informace o podrobných odchylkách představují způsob, jak porozumět zdroji každé odchylky. Chcete-li předjímat odchylky před dokončením výrobní zakázky, analyzujte podrobné informace, které jsou k dispozici v sestavě **Odhad a výpočet nákladů**.

## <a name="cost-analysis-for-current-production-orders"></a>Analýza nákladů pro aktuální výrobní zakázky
Samostatné sestavy poskytují informace o jednotlivých typech transakcí. Pomocí těchto sestav můžete analyzovat náklady pro výrobní aktivity se sestavou. Informace jsou zobrazeny pouze pro aktuální výrobní zakázky se stavem **Spuštěno** nebo **Ohlášeno jako dokončené**.

-   **Materiály v procesu**− V této sestavě jsou uvedeny transakce výdejky, které jsou uvedeny v sestavě v porovnání s aktuálními výrobními zakázkami k aktuálnímu datu transakce. Sestava uvádí vydané množství komponenty a částku nákladů pro každou transakci. Použijte kritéria výběru pro jednu položku komponenty. Například chcete-li vytisknout údaje o vydaném množství komponenty v porovnání s odpovídajícími výrobními zakázkami. Vydané množství není aktualizováno podle množství, které je hlášeno jako dokončené pro nadřazenou položku. Z tohoto důvodu mohou být skutečná množství surovin v daném procesu nadhodnocena.
-   **Nedokončená práce**− V této sestavě jsou uvedeny transakce postupu (nebo transakce úloh), které jsou uvedeny v sestavě v porovnání s aktuálními výrobními zakázkami k aktuálnímu datu transakce. Sestava udává hodiny, částku a množství (množství bez závad i chybové množství), které je uvedeno pro jednotlivé transakce. Také obsahuje informace, jako je například číslo operace, ID operace nebo provozní prostředek. V sestavě je také uvedena celková doba a částka pro všechny transakce oproti výrobní zakázce a množství označené jako dokončené.
-   **Nepřímé náklady v procesu**− v této sestavě jsou uvedeny nepřímé náklady, které vznikly v porovnání s výrobními zakázkami. Tyto údaje vychází z hlášené spotřeby pro operace postupu a komponenty k zadanému datu transakce. V sestavě je uveden typ nepřímých nákladů (příplatek nebo sazba), kód listu nákladů pro nepřímé náklady a částka nákladů pro každou transakci. Tato sestava neobsahuje informace o kartě postupu nebo transakci výdejky, z níž byly nepřímé náklady vygenerovány.
-   **Náklady rozpracované výroby**− V této sestavě jsou uvedeny údaje o kombinované spotřebě materiálu, operacích postupu a nepřímých nákladech pro určené datum transakce.
-   **Dokončené položky v procesu**− V této sestavě jsou uvedeny aktuální výrobní zakázky a transakce označené jako dokončené k určenému datu transakce.


<a name="additional-resources"></a>Další zdroje
--------

[Běžné zdroje výrobních odchylek](common-sources-of-production-variances.md)



