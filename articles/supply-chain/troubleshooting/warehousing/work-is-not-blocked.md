---
title: Práce není blokována
description: Práce není blokována
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTable_WHSWorkUnblocking
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: d64ab282972e46e8857581b59e5705dd15667328
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924197"
---
# <a name="work-isnt-blocked"></a>Práce není blokována

Kód chyby: WHSUnblockNotBlockedWorkErrorMessage

## <a name="symptoms"></a>Příznaky

Systém zobrazuje následující chybovou zprávu:

> Práce s ID %1 není blokována.

## <a name="cause"></a>Příčina

Možnost **Blokovaná vlna** na vlně je nastavena na hodnotu *Ne*. Práci nelze odblokovat, protože aktuálně není blokována.

## <a name="resolution"></a>Rozlišení

 Práci lze odblokovat pouze v případě, že je možnost **Blokovaná vlna** nastavena na hodnotu *Ano*.
