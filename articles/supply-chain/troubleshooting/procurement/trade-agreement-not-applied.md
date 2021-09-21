---
title: Na importované řádky objednávky se nevztahují podmínky obchodní smlouvy
description: Ceny a slevy z obchodních smluv se neuplatňují na řádcích prodejních nebo nákupních objednávek, které se importují prostřednictvím správy dat
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart, PurchRFQTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: fef38819efaff2f2a927cf09fc7f469490149574
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475824"
---
# <a name="trade-agreement-conditions-arent-applied-to-imported-order-lines"></a>Na importované řádky objednávky se nevztahují podmínky obchodní smlouvy

## <a name="symptoms"></a>Příznaky

Obchodní smlouvy, které se vztahují na řádky prodejních nebo nákupních objednávek, se neuplatňují na řádky, které se importují prostřednictvím správy dat. Stejné obchodní smlouvy se však používají na řádcích prodejních nebo nákupních objednávek, které se vytvářejí ručně.

## <a name="cause"></a>Příčina

Pokud řádky nákupní objednávky, které jsou importovány prostřednictvím správy dat, již obsahují informace o ceně, obchodní smlouva nebude u těchto řádků přehodnocena. Například pokud **Procento slevy řádku** nebo některá z cenových a slevových hodnot je pro řádek nastaveno , pak nebudou obchodní smlouvy pro daný řádek vyhledávány.

## <a name="workaround"></a>Alternativní řešení

Toto chování se očekává a je podobné pro prodejní i nákupní objednávky.

Řešením je importovat řádky nákupní objednávky bez nastavení jakýchkoli informací o ceně. Poté budou použity obchodní smlouvy a řádky nákupní objednávky budou aktualizovány na základě definovaných obchodních smluv.
