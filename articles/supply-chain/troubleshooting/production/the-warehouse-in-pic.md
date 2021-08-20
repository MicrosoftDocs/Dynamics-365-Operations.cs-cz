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
ms.openlocfilehash: 970930bbdd30b57a8374de7810bb3ece8cb19a7010b5ef19d90bfc39d09f172b
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6740544"
---
# <a name="the-warehouse-in-the-picking-list-journal-isnt-updated-on-a-bom-line"></a>Sklad v deníku výdejního seznamu není na řádku kusovníku aktualizován.

Číslo článku znalostní báze: 4614848

## <a name="symptoms"></a>Příznaky

Sklad v deníku výdejního seznamu není na řádku kusovníku aktualizován.

## <a name="resolution"></a>Rozlišení

Systém se chová tak, jak byl navržen. Pokud je vytvořen řádek deníku vychystávacího seznamu, který má odkaz (přes ID šarže) na produkční linku kusovníku, sklad na výrobní lince kusovníku nebude aktualizován, pokud se později změní dimenze skladu na řádku deníku výdejky produkce.
