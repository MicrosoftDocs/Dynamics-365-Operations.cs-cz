--- 
title: " Konfigurace plateb pro maloobchodní výkazy"
description: "Tato procedura ukazuje konfigurace pro metody plateb maloobchodu, které ovlivní způsob pro vytváření a účtování výkazy maloobchodu."
author: jashanno
manager: AnnBe
ms.date: 11/14/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 8bbdbf882f6f73d03be0a036cb975109396e4a0d
ms.openlocfilehash: 19f9c0b1c3a93ed9c84d66041814fd64951744b0
ms.contentlocale: cs-cz
ms.lasthandoff: 11/14/2017

---
# <a name="payment-configurations-for-retail-statements"></a> Konfigurace plateb pro maloobchodní výkazy

[!include[task guide banner](../includes/task-guide-banner.md)]

Tato procedura ukazuje konfigurace pro metody plateb maloobchodu, které ovlivní způsob pro vytváření a účtování výkazy maloobchodu.

Tento záznam používá ukázkovou společnost USRT.

1. Přejděte do nabídky Maloobchodní a velkoobchodní prodej > Kanály > Maloobchody > Všechny maloobchody.
2. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
3. Klikněte na odkaz na vybraném řádku v seznamu.
4. V podokně akcí klikněte na možnost Nastavit.
5. Klikněte na Způsoby platby.
6. Rozbalte nebo sbalte oddíl zaúčtování.
7. Klikněte na položku Upravit.
    * Určete, zda mají být přijaté částky pro tento způsob zaúčtovány na účet hlavní knihy nebo bankovní účet.  
    * Vyberte účet, kam mají být zaúčtovány částky přijaté pro tento způsob platby.  
    * Vyberte účet pro zaúčtování možných rozdílů mezi celkovou přijatou částkou transakce a částkou, která byla započtena pro tento způsob platby.  
    * V tomto poli můžete zadat částku pro určení, kdy má být částka rozdílu zaúčtována na jiný účet rozdílů. To slouží ke sledování velkých rozdílů.  
    * Vyberte účet, který chcete zaúčtovat možné rozdíly mezi celkovou přijatou částkou transakce a vypočtenou částkou, když překročí hodnotu, která je definována v poli „Maximální částka rozdílu“.  
    * Vyberte možnost „Ano“ pro zaúčtování částek pro odvod do banky na samostatný účet.  
    * V tomto poli můžete vybrat, zda částky pro odvod do banky mají být zaúčtovány na účet hlavní knihy nebo bankovní účet.  
    * Vyberte účet, kam se mají zaúčtovat částky pro odvod do banky.  
    * Vyberte typ bankovní transakce, který se má použít při zaúčtování částek pro odvod do banky na bankovní účet.  
    * Vyberte možnost „Ano“ pro zaúčtování částek pro odvod do trezoru na samostatný účet.  
    * Vyberte, zda částky pro odvod do trezoru mají být zaúčtovány na účet hlavní knihy nebo bankovní účet.  
    * Vyberte účet, kam se mají zaúčtovat částky pro odvod do trezoru.  
8. Klikněte na položku Uložit.


