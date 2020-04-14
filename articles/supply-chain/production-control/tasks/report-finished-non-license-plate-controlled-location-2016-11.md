---
title: Ohlášení za dokončené pro umístění bez řízení na základě registračních značek (aplikace, květen 2016)
description: Tento průvodce úkolem obsahuje ukázku dokončeného hlášení do skladového místa, které není řízeno registrační značkou.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WrkCtrResourceGroup, ProdTableListPage, ProdTableCreate, InventItemIdLookupPurchase, ProdParmCostEstimation, ProdParmStartUp, ProdParmReportFinished, WHSWorkTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2e96267a80160a63258b97f2e6ac49fad753a93a
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148901"
---
# <a name="report-as-finished-to-a-non-license-plate-controlled-location--application-may-2016"></a>Ohlášení za dokončené pro umístění bez řízení na základě registračních značek (aplikace, květen 2016)

[!include [banner](../../includes/banner.md)]

Tento průvodce úkolem obsahuje ukázku dokončeného hlášení do skladového místa, které není řízeno registrační značkou. Předpokladem pro tento úkol je příslušné pracovní pravidlo. Předchozí průvodce úlohou popisoval nastavení pracovních zásad. Tento průvodce úkolem vyžaduje aplikaci Dynamics AX 7.0.1 nebo novější.




## <a name="set-up-an-output-location"></a>Nastavení výstupního umístění
1. Přejděte na nabídce Správa organizace > Zdroje > Skupiny prostředků.
2. V seznamu vyberte skupinu prostředků '5102'.
3. Klikněte na možnost Upravit.
4. V poli Výstupní sklad vyberte 51.
5. V poli Výstupní umístění vyberte 001.
    * Umístění 001 není umístění řízené registrační značkou. Umístění výstupu bez registrační značky můžete nastavit pouze v případě, že pro umístění existuje příslušné pracovní pravidlo.  

## <a name="create-a-production-order-and-report-it-as-finished"></a>Vytvoření výrobní zakázky a její ohlášení jako dokončené
1. Zavřete stránku.
2. Přejděte na Řízení výroby > Výrobní zakázky > Všechny výrobní zakázky.
3. Klikněte na možnost Nová výrobní zakázka.
4. V poli Číslo zboží zadejte 'L0101'.
5. Klepněte na volbu Nový.
6. V podokně akcí klikněte na možnost Výrobní zakázka.
7. Klepněte na Odhad.
8. Klepněte na tlačítko OK.
9. Klepněte na tlačítko Start.
10. Klepněte na kartuObecné.
11. V poli Automatická spotřeba kusovníku vyberte hodnotu „Nikdy“.
12. Klepněte na tlačítko OK.
13. Klepněte na možnost Vykázat jako dokončené.
14. Klepněte na kartuObecné.
15. Vyberte možnost Ano v poli Akceptovat chybu.
16. Klepněte na tlačítko OK.
17. V podokně akcí klikněte na možnost Sklad.
18. Klepněte na tlačítko Podrobnosti práce.
    * Pokud byla výrobní zakázka ohlášena jako dokončená, žádná práce nebyla pro vyskladnění vytvořena. K tomu dochází, protože jsou definovány zásady práce, které brání generování práce, když je produkt L0101 ohlášen za dokončený v umístění 001.  

