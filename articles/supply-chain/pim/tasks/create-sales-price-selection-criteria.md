---
title: Vytvoření kritérií pro výběr prodejní ceny
description: Tato procedura ukazuje, jak vytvořit kritérium výběru prodejní ceny pro modely prodejní ceny podle atributů.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelSelectionCriteria, SysQueryForm, SysQueryTableLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5a616dcfdd755efc9bf0473e9239acb9127f11f8
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818150"
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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]