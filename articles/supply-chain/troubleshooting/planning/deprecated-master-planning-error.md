---
title: Při spuštění integrovaného hlavního plánovacího modulu se zobrazí chyba
description: Při spuštění zastaralého integrovaného hlavního plánovacího modulu se zobrazí chyba
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: Dialog_ReqCalcScheduleItemTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 7c0c674818a21d3ad422661fc427b0b9c4aad52b8d44d08791d2d703be528fe3
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6751714"
---
# <a name="you-receive-an-error-when-running-the-built-in-master-planning-engine"></a>Při spuštění integrovaného hlavního plánovacího modulu se zobrazí chyba

Kód chyby: ReqCalcScheduleItemTablePlanningOptimizationFitError

## <a name="symptoms"></a>Příznaky

Při spuštění hlavního plánování pomocí zastaralého integrovaného hlavního plánovacího modulu, zobrazí se následující chyba:

> Tato chybová zpráva se zobrazí, protože předdefinovaný hlavní plánovací modul byl použit pro scénáře podporované optimalizací plánování. Měli byste migrovat na optimalizaci plánování hned teď, protože aktuální vestavěné hlavní plánování bude zastaralé. Všimněte si, že toto spuštění hlavního plánování bylo úspěšně dokončeno. V případě, že vaše migrace má silné závislosti na čekajících funkcích, lze požádat o výjimku z dalšího používání integrovaného hlavního plánovacího modulu. Chcete-li začít, vyplňte prosím následující dotazník a případně požádejte o výjimku z migrace na optimalizaci plánování. [Dotazník pro optimalizaci plánování migrace a výjimky](https://go.microsoft.com/fwlink/?linkid=2144962)

## <a name="cause"></a>Příčina

Pokud spustíte plánování a nepoužíváte funkce řízení výroby, měli byste zvážit migraci na Optimalizaci plánování. Podpora integrovaného hlavního plánování je ukončena. Proto, pokud jej chcete i nadále používat bez přijetí chybové zprávy, musíte požádat o výjimku od společnosti Microsoft.

## <a name="resolution"></a>Řešení

Další informace o tom, jak migrovat na Optimalizaci plnánování, nebo jak požádat o výjimku, abyste místo toho mohli nadále používat zastaralý integrovaný plánovací modul, najdete v tématu [Migrace na optimalizaci plánování pro hlavní plánování](/dynamics365/supply-chain/master-planning/new-master-planning-engine).
