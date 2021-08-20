---
title: Práce nelze zrušit kvůli jejímu stavu
description: Práce nelze zrušit kvůli jejímu stavu
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTable_WHSWorkCancel, WHSWorkTableListPage_WHSWorkCancel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f983501b490c5516525b4d5904603ed62e8799f9e6124e5672b36a12804ecb0a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6755971"
---
# <a name="work-cant-be-canceled-because-of-its-status"></a>Práce nelze zrušit kvůli jejímu stavu

Kód chyby: WAX2190

## <a name="symptoms"></a>Příznaky

Systém zobrazuje následující chybovou zprávu:

> Nelze zrušit práci %1, protože má stav %2.

## <a name="cause"></a>Příčina

Práce nemůže být zrušena v aktuálním stavu.

Záhlaví práce nebo řádky práce nemají očekávanou hodnotu **Stav práce**. Pole **Stav práce** v záhlaví práce není nastaveno na hodnotu *Otevřeno* nebo *Probíhá*.

## <a name="resolution"></a>Rozlišení

Chcete-li zrušit práci, postupujte takto.

1. Přejděte k nabídce **Řízení skladu \> Periodické úkoly \> Vyčistit \> Zrušit práci**.
1. Do pole **ID práce** zadejte ID práce, kterou chcete zrušit.
1. Vyberte **OK**.
1. Vyberte možnost **Ano** k potvrzení, že chcete práci zrušit.

Další informace viz [Zrušení práce skladu pro zpracování výjimek](../../warehousing/cancel-warehouse-work.md).
