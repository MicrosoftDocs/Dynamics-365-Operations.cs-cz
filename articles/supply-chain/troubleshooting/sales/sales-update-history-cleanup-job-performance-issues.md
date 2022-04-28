---
title: Úloha čištění historie prodejů selhává nebo má problémy s výkonem
description: Dávkové vyčištění historie prodeje může selhat nebo může trvat velmi dlouho, pokud existuje velké množství údajů o aktualizaci prodeje.
author: myvakalo
ms.date: 10/05/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: myvakalo
ms.search.validFrom: 2021-09-29
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 124fb90ecafd4f4cccbd8a8bb443694c95365732
ms.sourcegitcommit: 197e6ddee84522fd587c6e4ee4f9089101e301c2
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/13/2022
ms.locfileid: "8570303"
---
# <a name="sales-update-history-cleanup-job-fails-or-has-performance-issues"></a>Úloha čištění historie prodejů selhává nebo má problémy s výkonem

## <a name="symptoms"></a>Příznaky

Dávková úloha **čištění historie prodejů** selhává nebo má problémy s výkonem.  

## <a name="cause"></a>Příčina

K tomu může dojít, pokud váš systém obsahuje velký počet aktualizací prodeje, což může mít za následek velké množství údajů o aktualizaci prodeje. Úloha čištění se pokusí vyčistit všechna tato data v jedné transakci. V důsledku toho může spuštění úlohy trvat velmi dlouho nebo dokonce selhat.

## <a name="resolution"></a>Řešení

Nová verze dávkové úlohy **Vyčištění historie aktualizace prodeje** je k dispozici pro Supply Chain Management verze 10.0.19 a novější. Ve výchozím nastavení není tato funkce zapnutá. Podrobnosti o tom, jak to funguje a jak to povolit ve správě funkcí, viz [Naplánování vyčištění dat historie prodeje](../../sales-marketing/sales-update-history-cleanup-performance-improvements.md).

