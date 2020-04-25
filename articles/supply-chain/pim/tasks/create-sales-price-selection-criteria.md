---
title: Vytvoření kritérií pro výběr prodejní ceny
description: Tato procedura ukazuje, jak vytvořit kritérium výběru prodejní ceny pro modely prodejní ceny podle atributů.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelSelectionCriteria, SysQueryForm, SysQueryTableLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6d1385a83da5b6448a9c753d7469979796043b60
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/02/2020
ms.locfileid: "3203761"
---
# <a name="create-sales-price-selection-criteria"></a>Vytvoření kritérií pro výběr prodejní ceny

[!include [banner](../../includes/banner.md)]

Tato procedura ukazuje, jak vytvořit kritérium výběru prodejní ceny pro modely prodejní ceny podle atributů. Spuštění této procedury vyžaduje, aby byl k dispozici nejméně jeden model prodejní ceny. Tento příklad používá cenový model pro model prodejních cen řešení Reproduktor ve společnosti ukázkových dat USMF. Manažer produktu obvykle používá tuto proceduru.


## <a name="add-a-new-criterion-for-an-existing-sales-price-model"></a>Přidání nového kritéria pro existující model prodejní ceny
1. Klepněte na Definice modelu varianty produktu.
2. Klepněte na Modely konfigurace produktu.
3. V seznamu vyberte řádek pro model výrobku řešení reproduktoru, ale neklikejte na odkaz pro název modelu.
4. V podokně akcí klepněte na možnost Model.
5. Klikněte na Kritéria cenového modelu.
6. Klikněte na možnost Nový.
7. Do pole Název zadejte hodnotu Skupina odběratelů 10.
    * Název kritéria cenového modelu se používá na pomoc při identifikaci základních kritérií výběru.  
8. V poli Cenový model zadejte nebo vyberte hodnotu.
9. V poli Výchozí typ objednávky vyberte možnost Prodejní objednávka.
    * Typ objednávky určuje databázová pole, která budou k dispozici pro výběrový dotaz.  
10. Zadejte datum do pole Platné od data.
11. Do pole Ukončit platnost k datu zadejte datum.
12. Klikněte na položku Uložit.

## <a name="create-the-query-for-the-selection-criteria"></a>Vytvoření dotazu pro kritérium výběru
1. Klikněte na položku Upravit.
2. V poli Tabulka vyberte Odběratelé. 
3. V poli Pole vyberte Skupina odběratelů.
    * V tomto příkladu použijeme jako kritérium výběru konkrétní skupinu odběratelů.  
4. V poli Kritéria vyberte Skupina odběratelů 10. 
5. Klikněte na tlačítko OK.

