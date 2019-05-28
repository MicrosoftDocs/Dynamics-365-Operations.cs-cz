---
title: Co je nového nebo změněného v aplikaci Dynamics 365 for Talent (14. února 2019)
description: Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 for Talent.
author: Darinkramer
manager: AnnBe
ms.date: 02/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-02-14
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 1db7d032eade3f996e0554e64d6ea0704a347ed8
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517496"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-february-14-2019"></a>Co je nového nebo změněného v aplikaci Dynamics 365 for Talent (14. února 2019)

[!include [banner](includes/banner.md)]

Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Talent.

## <a name="changes-in-attract"></a>Změny v aplikaci Attract
V této verzi existuje několik menších oprav chyb.

## <a name="changes-in-onboarding"></a>Změny v aplikaci Onboarding
V této verzi existuje několik menších oprav chyb.
 
## <a name="changes-in-core-hr"></a>Změny v Core HR 
**Sestavení 8.1.2146**

### <a name="employee-fixed-compensation-entity-doesnt-export-all-records"></a>Entita fixní kompenzace zaměstnance neexportuje všechny záznamy
S touto změnou bude nyní entita **Fixní kompenzace zaměstnance** exportovat všechny záznamy. Entitu lze použít vytváření a aktualizaci stávajících záznamů fixní kompenzace pro zaměstnance. 

### <a name="employment-end-date-doesnt-honor-employee-preferred-time-zone-settings"></a>Koncové datum zaměstnání nedodržuje upřednostňované časové pásmo zaměstnance
Koncové datum zaměstnání nyní ctí uživatelem upřednostňované časové pásmo při vytváření nebo ukončení zaměstnání se společností.
 
### <a name="uk-addresses-display-in-analytics-as-eastern-switzerland-addresses"></a>Adresy Velké Británie se zobrazují v analytice jako adresy východního Švýcarska
V této verzi byla provedena změna za účelem opravy nesprávného uspořádání adres v sestavě **Správy zaměstnanců** „počet osob podle umístění“.
 
### <a name="termination-code-is-not-populated-on-the-worker-position-assignment-record-when-ending-the-position"></a>Kód ukončení není vyplněn na záznamu přiřazení pozice pracovníka při ukončení pozice
Při ukončování přiřazení pozice zaměstnanců byla provedena změna výchozího kódu důvodu ukončení.

### <a name="new-entity-created-for-job-compensation-levels"></a>Byla vytvořena nová entita pro úrovně pracovní kompenzace
Byla vytvořena nová entita platformy správy dat (DMF). Entita zajišťuje tvorbu a aktualizaci úrovní kompenzace, tržních hodnot a informací z průzkumů pro každou práci definovanou v systému.
