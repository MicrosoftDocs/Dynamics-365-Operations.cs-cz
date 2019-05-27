---
title: " Konfigurace doporučení produktu využívajícího strojové učení"
description: Tato procedura aktualizuje data v úložišti entit, které používá systém strojového učení využívající doporučení produktu, a pak aktivuje doporučení produktu v klientech POS.
author: ashishmsft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BIMeasurementDeployManagementEntityStore, RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 700af913f18e23c66db53a92033def06818af1ec
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1548432"
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

