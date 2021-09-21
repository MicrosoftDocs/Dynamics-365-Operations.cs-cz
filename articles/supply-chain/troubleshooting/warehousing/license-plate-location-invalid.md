---
title: Neplatná registrační značka nebo chyba umístění v mobilní aplikaci
description: Při skenování ID registrační značky nebo skladového místa se může zobrazit chyba, že nejsou platné. Ujistěte se, že ID registrační značky není rezervováno něčím jiným.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: f9f10dbade0d13b8fc4b0fc92981d84e6e28e83e
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475847"
---
# <a name="invalid-license-plate-or-location-error-when-scanning-in-the-mobile-app"></a>Při skenování v mobilní aplikaci došlo k chybě registrační značky nebo umístění

## <a name="symptoms"></a>Příznaky

Při skenování ID registrační značky nebo skladového místa se může zobrazit následující chybová zpráva:

> Registrační značka nebo skladové místo nejsou platné.

## <a name="resolution"></a>Řešení

Ujistěte se, že ID registrační značky není rezervováno něčím jiným. K tomuto problému docházelo, když hodnota, kterou uživatel naskenoval v mobilní aplikaci Řízení skladu, byla platným skladovým místem i platným ID registrační značky. Tento problém byl však vyřešen ve verzi 10.0.11.
