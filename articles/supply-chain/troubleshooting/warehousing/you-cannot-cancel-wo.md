---
title: Nemůžete zrušit práci, která je na uživateli
description: Nemůžete zrušit práci, která je na uživateli
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
ms.openlocfilehash: e5f6912cfb1d5be8e46b7989856af99f8a611c11
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924394"
---
# <a name="you-cant-cancel-work-that-is-on-a-user"></a>Nemůžete zrušit práci, která je na uživateli

Kód chyby: WAX708

## <a name="symptoms"></a>Příznaky

Systém zobrazuje následující chybovou zprávu:

> Nelze stornovat práci, která je u daného uživatele.

## <a name="cause"></a>Příčina

Práce je uzamčena uživatelem a nelze ji zrušit. Chcete-li to potvrdit, otevřete ID práce a poté otevřete kartu **Obecné**. Pokud je práce uzamčena, pole **Stav práce** bude nastaveno na hodnotu *Probíhá* a pole **Zamknul** bude nastaveno na ID uživatele.

## <a name="resolution"></a>Rozlišení

Chcete-li zrušit práci, postupujte takto.

1. Přejděte k nabídce **Řízení skladu \> Periodické úkoly \> Vyčistit \> Zrušit práci**.
1. Do pole **ID práce** zadejte ID práce, kterou chcete zrušit.
1. Vyberte **OK**.
1. Vyberte možnost **Ano** k potvrzení, že chcete práci zrušit.

Další informace viz [Zrušení práce skladu pro zpracování výjimek](../../warehousing/cancel-warehouse-work.md).
