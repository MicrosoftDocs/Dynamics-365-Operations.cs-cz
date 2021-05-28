---
title: Chyba, když je zaúčtován Deník dokončené výroby
description: Když zaúčtujete sestavu jako dokončený deník, zobrazí se chybová zpráva s oznámením, že objednané množství nelze snížit.
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdTableListPage, ProdParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 55db7d0033dd66c1b973abf96671a20ab05d61d8
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026326"
---
# <a name="error-when-the-report-as-finished-journal-is-posted"></a>Chyba, když je zaúčtován Deník dokončené výroby

Číslo článku znalostní báze: 4612891

## <a name="symptoms"></a>Příznaky

Když zaúčtujete deník **Nahlásit jako dokončené**, dojde k chybě a zobrazí se následující chybová zpráva:

> Objednané množství nemůže být sníženo, protože není dostatek otevřených skladových transakcí se stavem Objednáno. Položky jsou zakoupené, přijaté nebo registrované.

K této chybě dochází pouze v případě, že je pole **Chybné množství** nastaveno na prvním řádku deníku **Nahlásit jako dokončené** a pole **Dobré množství** je nastaveno na posledním řádku. Pokud je pole **Chybné množství** je nastaveno na posledním řádku, nedojde k žádné chybě.

## <a name="resolution"></a>Rozlišení

Chcete-li této chybě zabránit, otevřete stránku **Parametry řízení výroby** a poté na kartě **Obecné** nastavte možnost **Zvýšení zůstatku s chybovým množstvím** na *Ano*.
