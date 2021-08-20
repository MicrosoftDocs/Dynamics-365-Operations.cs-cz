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
ms.openlocfilehash: fc3381dab77cf80c0fd65f3bc27c11b814e72368631bd0e2145aac0be4f4fba4
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6760363"
---
# <a name="cumulation-of-customer-rebates-fails-when-item-rebate-groups-are-used"></a>Kumulace zákaznických slev selže při použití skupin slev na položky

Číslo článku znalostní báze: 4611372

## <a name="symptoms"></a>Příznaky

Když použijete dohody o slevách (typu *částka*) v kombinaci se skupinami slev na položky, vypočítají se slevy, ale kumulace selže.

## <a name="resolution"></a>Rozlišení

Systém se chová tak, jak byl navržen. Skupiny položek seskupují pouze položky, které mají stejnou podmínku prahové hodnoty. Podmínka slevy (prahová hodnota) je nastavena proti částce pro každou položku, nikoli proti kumulované částce pro jakoukoli položku ve skupině položek.
