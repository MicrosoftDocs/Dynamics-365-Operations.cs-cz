---
title: Sklad v deníku výdejního seznamu není na řádku kusovníku aktualizován.
description: Sklad v deníku výdejního seznamu není na řádku kusovníku aktualizován.
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdJournalTransBOM
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 5d24c0b8538f3894fd1d2a3edb3a6ed8633c9609
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026328"
---
# <a name="the-warehouse-in-the-picking-list-journal-isnt-updated-on-a-bom-line"></a>Sklad v deníku výdejního seznamu není na řádku kusovníku aktualizován.

Číslo článku znalostní báze: 4614848

## <a name="symptoms"></a>Příznaky

Sklad v deníku výdejního seznamu není na řádku kusovníku aktualizován.

## <a name="resolution"></a>Rozlišení

Systém se chová tak, jak byl navržen. Pokud je vytvořen řádek deníku vychystávacího seznamu, který má odkaz (přes ID šarže) na produkční linku kusovníku, sklad na výrobní lince kusovníku nebude aktualizován, pokud se později změní dimenze skladu na řádku deníku výdejky produkce.
