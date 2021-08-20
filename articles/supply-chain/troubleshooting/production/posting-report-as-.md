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
ms.openlocfilehash: 50a11aba46519a3a81c313aa1f685d45dcf35f64b50bc921d93968efab13b7b9
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6750923"
---
# <a name="error-when-the-report-as-finished-journal-is-posted"></a>Chyba, když je zaúčtován Deník dokončené výroby

Číslo článku znalostní báze: 4612891

## <a name="symptoms"></a>Příznaky

Když zaúčtujete deník **Nahlásit jako dokončené**, dojde k chybě a zobrazí se následující chybová zpráva:

> Objednané množství nemůže být sníženo, protože není dostatek otevřených skladových transakcí se stavem Objednáno. Položky jsou zakoupené, přijaté nebo registrované.

K této chybě dochází pouze v případě, že je pole **Chybné množství** nastaveno na prvním řádku deníku **Nahlásit jako dokončené** a pole **Dobré množství** je nastaveno na posledním řádku. Pokud je pole **Chybné množství** je nastaveno na posledním řádku, nedojde k žádné chybě.

## <a name="resolution"></a>Rozlišení

Chcete-li této chybě zabránit, otevřete stránku **Parametry řízení výroby** a poté na kartě **Obecné** nastavte možnost **Zvýšení zůstatku s chybovým množstvím** na *Ano*.
