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
ms.openlocfilehash: 817802f1f2ad3ab07f35c28d3e833a14cd02cf8b9705c576325dc83933a0c6de
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6751762"
---
# <a name="the-indirect-costs-in-process-report-includes-deleted-production-orders"></a>Sestava Nepřímé náklady v procesu zahrnuje odstraněné výrobní zakázky

Číslo článku znalostní báze: 4612748

## <a name="symptoms"></a>Příznaky

Zpráva **Nepřímé náklady** v procesu obsahuje informace o výrobních zakázkách, které byly částečně zpracovány a později odstraněny.

## <a name="resolution"></a>Rozlišení

Když stornujete výrobní zakázku, stornujete také všechny transakce dané výrobní zakázky. Když odstraníte výrobní zakázku, tabulky vedlejší knihy a hlavní knihy přetrvají přes všechny transakce, které s ní souvisí. Sestavy budou zobrazovat transakce v tabulkách podřízené knihy. U konkrétní výrobní zakázky by čistá hodnota měla být 0,00.
