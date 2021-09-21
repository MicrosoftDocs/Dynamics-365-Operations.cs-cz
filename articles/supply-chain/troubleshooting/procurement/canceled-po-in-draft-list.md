---
title: Zrušené nákupní objednávky se zobrazí v seznamu konceptů v pracovním prostoru
description: Zrušené nákupní objednávky se zobrazí v seznamu konceptů v pracovním prostoru Příprava nákupní objednávky
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: f1dc23cd7e5b4b99cb7a9440d7d4666d8396511f
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475818"
---
# <a name="canceled-purchase-orders-appear-in-the-draft-list-in-the-workspace"></a>Zrušené nákupní objednávky se zobrazí v seznamu konceptů v pracovním prostoru

## <a name="symptoms"></a>Příznaky

Po zrušení nákupních objednávek, které byly ve stavu *Potvrzeno* se zrušené nákupní objednávky stále zobrazují v seznamu konceptů nákupních objednávek v pracovním prostoru **Příprava nákupní objednávky**.

## <a name="resolution"></a>Řešení

K tomuto problému dochází pouze u nákupních objednávek, které podléhají správě změn. Dochází k tomu, protože zrušení je považováno za změnu, kterou je nutné schválit. Schválení může být provedeno automaticky systémem. Proto je procesem odeslání zrušené nákupní objednávky do pracovního postupu schválení, aby mohla přejít do stavu *Schváleno*. V tomto okamžiku se nákupní objednávka již nebude zobrazovat v seznamu konceptů nákupních objednávek v pracovním prostoru **Příprava nákupní objednávky**.
