---
title: Sestava Nepřímé náklady v procesu zahrnuje odstraněné výrobní zakázky
description: Zpráva Nepřímé náklady v procesu obsahuje informace o výrobních zakázkách, které byly částečně zpracovány a později odstraněny.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdIndirectCostInProgress
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 707fa9bb30129c3656e10c6756dee770a7712e65
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026338"
---
# <a name="the-indirect-costs-in-process-report-includes-deleted-production-orders"></a>Sestava Nepřímé náklady v procesu zahrnuje odstraněné výrobní zakázky

Číslo článku znalostní báze: 4612748

## <a name="symptoms"></a>Příznaky

Zpráva **Nepřímé náklady** v procesu obsahuje informace o výrobních zakázkách, které byly částečně zpracovány a později odstraněny.

## <a name="resolution"></a>Rozlišení

Když stornujete výrobní zakázku, stornujete také všechny transakce dané výrobní zakázky. Když odstraníte výrobní zakázku, tabulky vedlejší knihy a hlavní knihy přetrvají přes všechny transakce, které s ní souvisí. Sestavy budou zobrazovat transakce v tabulkách podřízené knihy. U konkrétní výrobní zakázky by čistá hodnota měla být 0,00.
