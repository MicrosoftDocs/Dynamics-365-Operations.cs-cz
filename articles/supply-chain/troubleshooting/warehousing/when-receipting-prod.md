---
title: Na jednom dokladu je vytištěn pouze jeden štítek pro více pracovních hlaviček
description: Na jednom dokladu je vytištěn pouze jeden štítek pro více pracovních hlaviček.
author: perlynne
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WHSLicensePlateLabel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 8e11dc918eb3c9085018d15b43819522cc8bebe3
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026336"
---
# <a name="only-one-label-is-printed-for-multiple-work-headers-on-a-single-receipt"></a>Na jednom dokladu je vytištěn pouze jeden štítek pro více pracovních hlaviček

Číslo článku znalostní báze: 4614667

## <a name="symptoms"></a>Příznaky

Pro stejnou cílovou registrační značku je vytvořeno více pracovních hlaviček jako součást jedné události přijetí aplikace skladu. Po přijetí produktu je však vytištěn pouze jeden štítek s registrační značkou.

## <a name="resolution"></a>Rozlišení

Systém se chová tak, jak byl navržen.

V aktuálním designu je vždy vygenerován jeden štítek registračních značek vozidla, bez ohledu na počet existujících kombinací hlavičky a pracovní linky. Vygenerovaný štítek obsahuje informace pouze pro jednu kombinaci.

Chcete-li tento problém vyřešit, ujistěte se, že vytváření hlavičky práce je vždy mapováno pouze na jednu cílovou registrační značku.
