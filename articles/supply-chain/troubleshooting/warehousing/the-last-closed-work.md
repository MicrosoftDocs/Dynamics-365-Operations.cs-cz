---
title: Poslední uzavřený řádek práce musí mít hodnotu Vložit
description: Poslední uzavřený řádek práce musí mít hodnotu Vložit
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
ms.openlocfilehash: a5b78154b51252b3ac96ba28c254e823caf87019
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924368"
---
# <a name="the-last-closed-work-line-must-be-a-put"></a>Poslední uzavřený řádek práce musí mít hodnotu Vložit

Kód chyby: WAX1285

## <a name="symptoms"></a>Příznaky

Systém zobrazuje následující chybovou zprávu:

> Poslední uzavřený řádek práce musí mít hodnotu Vložit.

## <a name="cause"></a>Příčina

Práce nemůže být zrušena v aktuálním stavu.

Na posledním pracovním řádku je pole **Stav práce** nastaveno na hodnotu *Uzavřeno*, ale pole **Typ práce** není nastaveno na hodnotu *Vložit*.

## <a name="resolution"></a>Rozlišení

Chcete-li zrušit práci, postupujte takto.

1. Přejděte k nabídce **Řízení skladu \> Periodické úkoly \> Vyčistit \> Zrušit práci**.
1. Do pole **ID práce** zadejte ID práce, kterou chcete zrušit.
1. Vyberte **OK**.
1. Vyberte možnost **Ano** k potvrzení, že chcete práci zrušit.

Další informace viz [Zrušení práce skladu pro zpracování výjimek](../../warehousing/cancel-warehouse-work.md).
