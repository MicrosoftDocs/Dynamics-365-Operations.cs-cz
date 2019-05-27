---
title: " Konfigurace parametrů pro maloobchodní výkazy"
description: Tato procedura ukazuje konfigurace pro Parametry maloobchodu, které ovlivní způsob, jakým se vytvářejí a účtují výkazy maloobchodu.
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
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
ms.openlocfilehash: 6dacd2b80ca0d51d81d2bdf5bc2636b47da621ee
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1564286"
---
# <a name="parameter-configurations-for-retail-statements"></a> Konfigurace parametrů pro maloobchodní výkazy

[!include[task guide banner](../includes/task-guide-banner.md)]

Tato procedura ukazuje konfigurace pro Parametry maloobchodu, které ovlivní způsob, jakým se vytvářejí a účtují výkazy maloobchodu. Tato procedura používá ukázkovou společnost USRT.

1. Přejděte do nabídky Maloobchodní a velkoobchodní prodej > Nastavení centrály > Parametry > Parametry maloobchodu.
2. Klikněte na kartu Zaúčtování.
    * Pokud chcete zaúčtovat konkrétně částky časové slevy, vyberte "Ano".  
    * Pokud chcete použít výchozí účet, vyberte „Standardní“ nebo vyberte „Periodický“, pokud chcete definovat účet, který má být použit pro jednotlivé časové slevy.  
    * Vyberte „Souhrn“ v případě, že řádky zásob mají být agregovány vždy, když je to možné.  
    * Vyberte „Ano“, pokud faktury a platby mají být automaticky vyrovnány v rámci procesu zaúčtování výkazu.  
    * Vyberte „Ano“, pokud je nutné agregovat transakce odvodu do trezoru.  
    * Vyberte „Ano“, pokud je nutné agregovat transakce odvodu do banky.  
    * Výběrem možnosti „Ano“ aktivujete agregace pro zaúčtování výkazu.  
    * Výběrem možnosti „Ano“ můžete vytvořit a zpracovat objednávky současně při zaúčtování výkazů.  
    * Zadejte maximální počet objednávek, které mají být zpracovány v jednotlivých dávkových úlohách.  
3. Klikněte na položku Uložit.

