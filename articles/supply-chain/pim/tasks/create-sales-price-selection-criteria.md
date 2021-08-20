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
ms.openlocfilehash: 47ea7ea2093c540a88d9fd7249b470009c7595d40e2a727d8fcd3bb4b5d74bac
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6750069"
---
# <a name="create-sales-price-selection-criteria"></a>Vytvoření kritérií pro výběr prodejní ceny

[!include [banner](../../includes/banner.md)]

Tato procedura ukazuje, jak vytvořit kritérium výběru prodejní ceny pro modely prodejní ceny podle atributů. Spuštění této procedury vyžaduje, aby byl k dispozici nejméně jeden model prodejní ceny. Tento příklad používá cenový model pro model prodejních cen řešení Reproduktor ve společnosti ukázkových dat USMF. Manažer produktu obvykle používá tuto proceduru.

## <a name="add-a-new-criterion-for-an-existing-sales-price-model"></a>Přidání nového kritéria pro existující model prodejní ceny

1. Přejděte na **Řízení informací o produktech \> Produkty \> Modely konfigurace produktu**.
1. V seznamu vyberte řádek pro model výrobku řešení reproduktoru, ale neklikejte na odkaz pro název modelu.
1. V podokně akcí zvolte **Model**.
1. Vyberte **Kritéria cenového modelu**.
1. Zvolte **Nové**.
1. Do pole **Název** zadejte hodnotu „Skupina odběratelů 10“.
    * Název kritéria cenového modelu se používá na pomoc při identifikaci základních kritérií výběru.  
1. V poli **Cenový model** zadejte nebo vyberte hodnotu.
1. V poli **Typ objednávky** vyberte možnost *Prodejní objednávka*.
    * Typ objednávky určuje databázová pole, která budou k dispozici pro výběrový dotaz.  
1. Zadejte datum do pole **Platné od data**.
1. Do pole **Ukončit platnost k datu** zadejte datum.
1. Zvolte **Uložit**.

## <a name="create-the-query-for-the-selection-criteria"></a>Vytvoření dotazu pro kritérium výběru

1. Vyberte možnost **Upravit**.
2. V poli **Tabulka** vyberte *Odběratelé*.
3. V poli **Pole** vyberte *Skupina odběratelů*.
    * V tomto příkladu použijeme jako kritérium výběru konkrétní skupinu odběratelů.  
4. V poli **Kritéria** vyberte *Skupina odběratelů 10*.
5. Vyberte **OK**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]