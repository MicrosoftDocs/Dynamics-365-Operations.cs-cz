---
title: Kumulace zákaznických slev selže při použití skupin slev na položky
description: Když použijete dohody o slevách na zákazníka v kombinaci se skupinami slev na položky, vypočítají se slevy, ale kumulace selže.
author: sherry-zheng
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: PdsRebateTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 5222d5a52a34ecfa4a1eac96a2cb561f257f17ea
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026327"
---
# <a name="cumulation-of-customer-rebates-fails-when-item-rebate-groups-are-used"></a>Kumulace zákaznických slev selže při použití skupin slev na položky

Číslo článku znalostní báze: 4611372

## <a name="symptoms"></a>Příznaky

Když použijete dohody o slevách (typu *částka*) v kombinaci se skupinami slev na položky, vypočítají se slevy, ale kumulace selže.

## <a name="resolution"></a>Rozlišení

Systém se chová tak, jak byl navržen. Skupiny položek seskupují pouze položky, které mají stejnou podmínku prahové hodnoty. Podmínka slevy (prahová hodnota) je nastavena proti částce pro každou položku, nikoli proti kumulované částce pro jakoukoli položku ve skupině položek.
