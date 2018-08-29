--- 
title: "Konfigurace nastavení metod platby, které ovlivňují výkazy maloobchodu"
description: "Tato procedura ukazuje konfigurace pro metody plateb maloobchodu, které ovlivní způsob pro vytváření a účtování výkazy maloobchodu."
author: jashanno
manager: AnnBe
ms.date: 11/14/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: ba21db9ee97dc4d851c77a906927ef513940b743
ms.contentlocale: cs-cz
ms.lasthandoff: 08/08/2018

---
# <a name="configure-payment-method-settings-that-affect-retail-statements"></a>Konfigurace nastavení metod platby, které ovlivňují výkazy maloobchodu

[!include [task guide banner](../includes/task-guide-banner.md)]

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


