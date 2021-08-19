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
ms.openlocfilehash: 6b4361682246397732e8326b98b1b86ff878664e54c8c352296b0d7eaff6bbbd
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6719544"
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
