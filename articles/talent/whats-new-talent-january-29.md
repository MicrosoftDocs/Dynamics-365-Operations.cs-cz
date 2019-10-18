---
title: Co je nového nebo změněného v aplikaci Dynamics 365 Talent (31. ledna 2019)
description: Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 01/31/2019
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
ms.search.validFrom: 2019-01-29
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 6dcdb37ba7a423e54a641c1d123f563a59648d46
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/23/2019
ms.locfileid: "2010307"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-january-31-2019"></a>Co je nového nebo změněného v aplikaci Dynamics 365 Talent (31. ledna 2019)

[!include [banner](includes/banner.md)]

Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Dynamics 365 Talent.

**Sestavení 8.1.2128**

## <a name="core-hr-changes"></a>Změny Core HR

### <a name="time-off-taken-on-leave-people-card-doesnt-consider-leave-plan-dates"></a>Volno využité na kartě dovolené zaměstnanců nezohledňuje plánovaná data dovolené
Pro ty, kteří mají plány dovolené nepoužívané v kalendářním roce, karta **Vybráno** nyní zobrazuje dovolenou, která byla využita v roce dovolené definované pro plán. Pokud je například rok dovolené v organizaci od 1. června do 30. května a zaměstnanec si vyberte 3 dny v prosinci, budou se na kartě **Vybráno** k 15. lednu zobrazovat 3 dny. 

### <a name="accrual-amounts-not-matching-tier-date-basis"></a>Časové rozlišené částky neodpovídají základu data vrstvy
Byly přidány nové možnosti pro dovolenou a absenci (parametry **lidských zdrojů**) pro povolení zákazníkům určit, ke kterému datu jsou měsíce služby zaměstnance platné. V některých organizacích je tímto datem konec měsíce, jinde to ale může být začátek příštího měsíce. Jedna organizace může například udělovat čas volna k 31. prosinci, zatímco jiná k 1. lednu. Tato možnost vám umožní zvolit, kdy dojde k udělení. 

### <a name="worker-hire-actions-are-stuck-in-workflow-complete-state"></a>Akce náboru pracovníků jsou zastavené ve stavu Workflow dokončen
Byly provedeny změny k nápravě problémů, kdy malý počet workflow skončil se stavem Workflow dokončen Nové workflowy by se nyní měly přesunout do stavu Dokončeno, jakmile skončí workflow. Všechny workflowy ve stavu workflow byl dokončen budou přesunuty do chybového stavu umožňujícího aktualizaci nebo odebrání v případě potřeby. 
