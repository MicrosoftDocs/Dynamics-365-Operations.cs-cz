---
title: Co je nového nebo změněného v aplikaci Dynamics 365 Talent (31. ledna 2019)
description: Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Talent.
author: andreabichsel
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
ms.author: anbichse
ms.search.validFrom: 2019-01-29
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 8e8c11e460a4678efea81f8d3d1eec96b673d329
ms.sourcegitcommit: 53174ed4e7cc4e1ba07cdfc39207e7296ef87c1f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/07/2020
ms.locfileid: "4690045"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-january-31-2019"></a>Co je nového nebo změněného v aplikaci Dynamics 365 Talent (31. ledna 2019)

Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Dynamics 365 Talent.

**Sestavení 8.1.2128**

## <a name="core-hr-changes"></a>Změny Core HR

### <a name="time-off-taken-on-leave-people-card-doesnt-consider-leave-plan-dates"></a>Volno využité na kartě dovolené zaměstnanců nezohledňuje plánovaná data dovolené
Pro plány pracovního volna nepoužívané v kalendářním roce, karta **Vybráno** nyní zobrazuje pracovní volno, které bylo využito v roce pracovního volna definovaného pro plán. Pokud je například rok pracovního volna v organizaci od 1. června do 30. května a zaměstnanec si vyberte 3 dny v prosinci, budou se na kartě **Vybráno** k 15. lednu zobrazovat 3 dny. 

### <a name="accrual-amounts-not-matching-tier-date-basis"></a>Časové rozlišené částky neodpovídají základu data vrstvy
Byly přidány nové možnosti pro dovolenou a absenci (parametry **lidských zdrojů**) pro povolení zákazníkům určit, ke kterému datu jsou měsíce služby zaměstnance platné. V některých organizacích je tímto datem konec měsíce, jinde to ale může být začátek příštího měsíce. Jedna organizace může například udělovat čas volna k 31. prosinci, zatímco jiná k 1. lednu. Tato možnost vám umožní zvolit, kdy dojde k udělení. 

### <a name="worker-hire-actions-are-stuck-in-workflow-complete-state"></a>Akce náboru pracovníků jsou zastavené ve stavu Workflow dokončen
Byly provedeny změny k nápravě problémů, kdy malý počet workflow skončil se stavem Workflow dokončen Nové workflowy by se nyní měly přesunout do stavu Dokončeno, jakmile skončí workflow. Všechny workflowy ve stavu workflow byl dokončen budou přesunuty do chybového stavu umožňujícího aktualizaci nebo odebrání v případě potřeby. 
