--- 
title: " Konfigurace doporučení produktu využívajícího strojové učení"
description: "Tato procedura aktualizuje data v úložišti entit, které používá systém strojového učení využívající doporučení produktu, a pak aktivuje doporučení produktu v klientech POS."
author: ashishmsft
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: c51c5f82efb50db1e238f4046506920975f33218
ms.contentlocale: cs-cz
ms.lasthandoff: 07/28/2017

---
# <a name="configure-machine-learning-powered-product-recommendations"></a> Konfigurace doporučení produktu využívajícího strojové učení

[!include[task guide banner](../includes/task-guide-banner.md)]

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


