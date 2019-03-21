---
title: Co je nového nebo změněného v aplikaci Dynamics 365 for Talent (31. ledna 2019)
description: Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 for Talent.
author: Darinkramer
manager: AnnBe
ms.date: 01/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-01-29
ms.dyn365.ops.version: Talent
ms.openlocfilehash: ab43bab53afd979d64099425f0582f6c1bb5a8b0
ms.sourcegitcommit: 383a344deb5abf48584ea2ee7774b8dbbbec49b3
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/08/2019
ms.locfileid: "377843"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-january-31-2019"></a>Co je nového nebo změněného v aplikaci Dynamics 365 for Talent (31. ledna 2019)

[!include [banner](includes/banner.md)]

Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Dynamics 365 for Talent.

**Sestavení 8.1.2128**

## <a name="core-hr-changes"></a>Změny Core HR

### <a name="time-off-taken-on-leave-people-card-doesnt-consider-leave-plan-dates"></a>Volno využité na kartě dovolené zaměstnanců nezohledňuje plánovaná data dovolené
Pro ty, kteří mají plány dovolené nepoužívané v kalendářním roce, karta **Vybráno** nyní zobrazuje dovolenou, která byla využita v roce dovolené definované pro plán. Pokud je například rok dovolené v organizaci od 1. června do 30. května a zaměstnanec si vyberte 3 dny v prosinci, budou se na kartě **Vybráno** k 15. lednu zobrazovat 3 dny. 

### <a name="accrual-amounts-not-matching-tier-date-basis"></a>Časové rozlišené částky neodpovídají základu data vrstvy
Byly přidány nové možnosti pro dovolenou a absenci (parametry **lidských zdrojů**) pro povolení zákazníkům určit, ke kterému datu jsou měsíce služby zaměstnance platné. V některých organizacích je tímto datem konec měsíce, jinde to ale může být začátek příštího měsíce. Jedna organizace může například udělovat čas volna k 31. prosinci, zatímco jiná k 1. lednu. Tato možnost vám umožní zvolit, kdy dojde k udělení. 

### <a name="worker-hire-actions-are-stuck-in-workflow-complete-state"></a>Akce náboru pracovníků jsou zastavené ve stavu Workflow dokončen
Byly provedeny změny k nápravě problémů, kdy malý počet workflow skončil se stavem Workflow dokončen Nové workflowy by se nyní měly přesunout do stavu Dokončeno, jakmile skončí workflow. Všechny workflowy ve stavu workflow byl dokončen budou přesunuty do chybového stavu umožňujícího aktualizaci nebo odebrání v případě potřeby. 
