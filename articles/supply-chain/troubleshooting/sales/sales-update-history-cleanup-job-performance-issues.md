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
ms.openlocfilehash: 4f04dc204c705b40ed25fadc75118feaef4d6b6e
ms.sourcegitcommit: 42bd701179e664947b6eafcd1804c83a5e64abcb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2021
ms.locfileid: "7641449"
---
# <a name="sales-update-history-cleanup-job-fails-or-has-performance-issues"></a>Úloha čištění historie prodejů selhává nebo má problémy s výkonem

## <a name="symptoms"></a>Příznaky

Dávková úloha **čištění historie prodejů** selhává nebo má problémy s výkonem.  

## <a name="cause"></a>Příčina

K tomu může dojít, pokud váš systém obsahuje velký počet aktualizací prodeje, což může mít za následek velké množství údajů o aktualizaci prodeje. Úloha čištění se pokusí vyčistit všechna tato data v jedné transakci. V důsledku toho může spuštění úlohy trvat velmi dlouho nebo dokonce selhat.

## <a name="resolution"></a>Řešení

Nová verze dávkové úlohy **Vyčištění historie aktualizace prodeje** je k dispozici pro Supply Chain Management verze 10.0.19 a novější. Tato funkce není ve výchozím nastavení zapnutá. Podrobnosti o tom, jak to funguje a jak to povolit ve správě funkcí, viz [Vylepšení výkonu vyčištění historie prodeje](../../sales-marketing/sales-update-history-cleanup-performance-improvements.md).

