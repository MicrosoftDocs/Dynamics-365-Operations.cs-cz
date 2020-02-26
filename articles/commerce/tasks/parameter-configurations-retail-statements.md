---
title: Konfigurace parametrů, které ovlivňují výkazy maloobchodu
description: Toto téma ukazuje konfigurace pro parametry velkoobchodu, které ovlivní způsob, jakým se vytvářejí a účtují výkazy maloobchodu.
author: josaw1
manager: AnnBe
ms.date: 08/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d8cae6d2fa7c469f50fa92141a6cb5a0af1df4b0
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/01/2020
ms.locfileid: "3021857"
---
# <a name="configure-parameters-that-affect-retail-statements"></a>Konfigurace parametrů, které ovlivňují výkazy maloobchodu

[!include[task guide banner](../includes/task-guide-banner.md)]

Toto téma ukazuje konfigurace pro parametry velkoobchodu, které ovlivní způsob, jakým se vytvářejí a účtují výkazy maloobchodu. Tato procedura používá ukázkovou společnost USRT.

1. V navigačním podokně přejděte na **Moduly > Maloobchodní a velkoobchodní prodej > Nastavení centrály > Parametry > Parametry velkoobchodu**.
2. Vyberte kartu **Účtování**.
    - Pokud chcete zaúčtovat konkrétně částky časové slevy, vyberte **Ano**.  
    - Pokud chcete použít výchozí účet, vyberte **Standardní** nebo vyberte **Periodický**, pokud chcete definovat účet, který má být použit pro jednotlivé časové slevy.  
      - Vyberte **Souhrn** v případě, že řádky zásob mají být agregovány vždy, když je to možné.  
      - Vyberte **Ano**, pokud faktury a platby mají být automaticky vyrovnány v rámci procesu zaúčtování výkazu.  
      - Vyberte **Ano**, pokud je nutné agregovat transakce odvodu do trezoru.  
      - Vyberte **Ano**, pokud je nutné agregovat transakce odvodu do banky.  
      - Výběrem možnosti **Ano** aktivujete agregace pro zaúčtování výkazu.  
      - Výběrem možnosti **Ano** můžete vytvořit a zpracovat objednávky současně při zaúčtování výkazů.  
      - Zadejte maximální počet objednávek, které mají být zpracovány v jednotlivých dávkových úlohách.  
3. Zvolte **Uložit**.

