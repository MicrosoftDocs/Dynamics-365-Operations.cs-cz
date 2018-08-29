--- 
title: "Konfigurace parametrů Retail, které ovlivňují výkazy maloobchodu"
description: "Tato procedura ukazuje konfigurace pro Parametry maloobchodu, které ovlivní způsob, jakým se vytvářejí a účtují výkazy maloobchodu."
author: josaw1
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: ff12587d8332801131d5b0cac84e0db38f8f6142
ms.contentlocale: cs-cz
ms.lasthandoff: 08/08/2018

---
# <a name="configure-retail-parameters-that-affect-retail-statements"></a>Konfigurace parametrů Retail, které ovlivňují výkazy maloobchodu

[!include [task guide banner](../includes/task-guide-banner.md)]

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


