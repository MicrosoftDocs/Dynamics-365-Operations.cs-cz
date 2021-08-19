---
title: Práce nelze zrušit, protože je blokována
description: Práce nelze zrušit, protože je blokována
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTable_WHSWorkCancel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: a24f199484c7596189b19e4cddf344e9186c6044edd2906affca9b530de44168
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6722192"
---
# <a name="work-cant-be-canceled-because-its-blocked"></a>Práce nelze zrušit, protože je blokována

Kód chyby: WHSCancellationOfWorkBlockedByExecutingWave_ErrorMessage

## <a name="symptoms"></a>Příznaky

Systém zobrazuje následující chybovou zprávu:

> Práci %1 nelze zrušit, protože je blokována s typem důvodu %2. Než bude práci možné zrušit, musíte zrušit její blokování.

## <a name="cause"></a>Příčina

Práce je blokována a nelze ji zrušit.

Na stránce **Práce** na kartě **Obecné** je možnost **Blokováno** nastavena na hodnotu *Ano*. Toto nastavení označuje, že práce je blokována. Na kartě **Důvody blokování** je zobrazeno, proč byla práce zablokována.

## <a name="resolution"></a>Rozlišení

Chcete-li práci odblokovat, vyberte kartu **Důvody blokování** a potom proveďte jeden z těchto kroků:

- Pokud je pole **Důvod blokování práce** nastaveno na hodnotu *Nedefinovaný důvod*: V podokně akcí na kartě **Práce** ve skupině **Práce** vyberte možnost **Odblokovat práci**.
- Pokud je pole **Důvod blokování práce** nastaveno na hodnotu *Vlna zpracování*: V podokně akcí na kartě **Související informace** ve skupině **Související informace** vyberte možnost **Vlna**. V podokně akcí pak na stránce **Vlny** na kartě **Vlna** vyberte ve skupině **Vlna** možnost **Vyčistit data vlny**.

## <a name="workaround"></a>Alternativní řešení

Pokud předchozí kroky problém nevyřešily, můžete práci zrušit podle těchto kroků.

1. Přejděte k nabídce **Řízení skladu \> Periodické úkoly \> Vyčistit \> Zrušit práci**.
1. V poli **ID práce** zadejte ID práce, kterou chcete zrušit a které aktuálně obsahuje pro možnost **Stav práce** hodnotu *Otevřeno*, *Probíhá*, *Zrušeno*, *Kombinované* nebo *Uzavřené*.
1. Vyberte **OK**.
1. Vyberte možnost **Ano** k potvrzení, že chcete práci zrušit.

Další informace viz [Zrušení práce skladu pro zpracování výjimek](../../warehousing/cancel-warehouse-work.md).
