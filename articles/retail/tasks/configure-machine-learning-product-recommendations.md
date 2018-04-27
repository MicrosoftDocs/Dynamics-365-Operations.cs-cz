--- 
title: " Konfigurace doporučení produktu využívajícího strojové učení"
description: "Tato procedura aktualizuje data v úložišti entit, které používá systém strojového učení využívající doporučení produktu, a pak aktivuje doporučení produktu v klientech POS."
author: ashishmsft
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 277ffb879b80fe57deeaa2b52c1543baaf820274
ms.contentlocale: cs-cz
ms.lasthandoff: 02/07/2018

---
# <a name="configure-machine-learning-powered-product-recommendations"></a> Konfigurace doporučení produktu využívajícího strojové učení

[!INCLUDE [task guide banner](../includes/task-guide-banner.md)]

Tato procedura aktualizuje data v úložišti entit, které používá systém strojového učení využívající doporučení produktu, a pak aktivuje doporučení produktu v klientech POS. Tato procedura používá v ukázkových datech společnost USRT.

1. Přejděte do nabídky Správa systému > Nastavení > Úložiště entit.
2. V seznamu vyhledejte a vyberte záznam 'RetailSales'.
3. Klikněte na možnost Aktualizovat.
4. Klikněte na tlačítko OK.
5. Zavřete stránku.
6. Přejděte do nabídky Maloobchodní a velkoobchodní prodej > Nastavení centrály > Parametry > Parametry maloobchodu.
7. Klepněte na kartu Strojové učení.
8. Vyberte možnost Ano v poli Povolit doporučení produktu.
    * Pokud se zobrazí zpráva "Nelze načíst modely doporučení", je to proto, že jste teprve nedávno aktualizovali úložiště entit a systém nemusel dokončit asimilaci nových dat. 2–3 hodiny počkejte a akci opakujte.  
9. Klikněte na položku Uložit.
10. Zavřete stránku.


