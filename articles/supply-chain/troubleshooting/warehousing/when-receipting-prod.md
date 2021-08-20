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
ms.openlocfilehash: cf307964a07c2b69eb5e4ef2cf9dc094482736d0970e333e84f674c9be6331c7
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6740520"
---
# <a name="only-one-label-is-printed-for-multiple-work-headers-on-a-single-receipt"></a>Na jednom dokladu je vytištěn pouze jeden štítek pro více pracovních hlaviček

Číslo článku znalostní báze: 4614667

## <a name="symptoms"></a>Příznaky

Pro stejnou cílovou registrační značku je vytvořeno více pracovních hlaviček jako součást jedné události přijetí aplikace skladu. Po přijetí produktu je však vytištěn pouze jeden štítek s registrační značkou.

## <a name="resolution"></a>Rozlišení

Systém se chová tak, jak byl navržen.

V aktuálním designu je vždy vygenerován jeden štítek registračních značek vozidla, bez ohledu na počet existujících kombinací hlavičky a pracovní linky. Vygenerovaný štítek obsahuje informace pouze pro jednu kombinaci.

Chcete-li tento problém vyřešit, ujistěte se, že vytváření hlavičky práce je vždy mapováno pouze na jednu cílovou registrační značku.
