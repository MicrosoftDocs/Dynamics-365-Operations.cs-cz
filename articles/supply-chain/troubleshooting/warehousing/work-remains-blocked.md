---
title: Práce zůstává blokována
description: Práce zůstává blokována
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTableListPage_WHSWorkUnblocking
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 898390c78bb26fb8a44f77a10ad27a00720f7d1a3396cec5fff10e9d6b93364d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6768563"
---
# <a name="work-remains-blocked"></a>Práce zůstává blokována

Kód chyby: WHSWorkBlockingExecutingWaveReason_ErrorMessage

## <a name="symptoms"></a>Příznaky

Systém zobrazuje následující chybovou zprávu:

> Práce %1 zůstává blokována, protože související vlna %2 má stav %3.

## <a name="cause"></a>Příčina

Práce se aktuálně zpracovává na vlně a nelze ji odblokovat, jak naznačuje jedna z následujících podmínek:

- Na kartě **Důvody blokování** je pole **Důvod blokování práce** pro jeden nebo více řádků nastaveno na hodnotu *Vlna zpracování*.
- Pokud vyberte možnost **Vlna** ve skupině **Související informace** na kartě **Související informace** podokna akcí, je pole **Stav vlny** nastaveno na hodnotu *Zpracování*.

## <a name="resolution"></a>Rozlišení

V podokně akcí na kartě **Související informace** ve skupině **Související informace** vyberte možnost **Vlna**. V podokně akcí pak na stránce **Vlny** na kartě **Vlna** vyberte ve skupině **Vlna** možnost **Vyčistit data vlny**.

## <a name="workaround"></a>Alternativní řešení

Pokud předchozí kroky problém nevyřešily, můžete práci zrušit podle těchto kroků.

1. Přejděte k nabídce **Řízení skladu \> Periodické úkoly \> Vyčistit \> Zrušit práci**.
1. V poli **ID práce** zadejte ID práce, kterou chcete zrušit a které aktuálně obsahuje pro možnost **Stav práce** hodnotu *Otevřeno*, *Probíhá*, *Zrušeno*, *Kombinované* nebo *Uzavřené*.
1. Vyberte **OK**.
1. Vyberte možnost **Ano** k potvrzení, že chcete práci zrušit.

Další informace viz [Zrušení práce skladu pro zpracování výjimek](../../warehousing/cancel-warehouse-work.md).
