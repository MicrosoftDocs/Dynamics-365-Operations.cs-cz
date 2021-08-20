---
title: Plánovaná nákupní objednávka se vytvoří, když nákup existuje do záporných dnů
description: Pokud je kód pokrytí min./max., Optimalizace plánování vytvoří plánovanou nákupní objednávku, pokud existuje nákup v záporných dnech.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo,MpsIntegrationParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ilebedev
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 94d569684a0bfa2398e98147b9b85531954f8d56748894034a048fa627230ef0
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6775500"
---
# <a name="planned-purchase-order-is-created-when-a-purchase-exists-within-negative-days"></a>Plánovaná nákupní objednávka se vytvoří, když nákup existuje do záporných dnů

Číslo článku znalostní báze: 4614298

## <a name="symptoms"></a>Příznaky

Pokud je kód pokrytí *min./max.*, Optimalizace plánování vytvoří plánovanou nákupní objednávku, pokud existuje nákup v záporných dnech.

## <a name="resolution"></a>Rozlišení

Optimalizace plánování nepodporuje negativní dny. Vždy však zajistí, že plánované objednávky nebudou naplánovány v době realizace vzhledem k aktuálnímu datu. Například dodací lhůta pro nákup je 10 dní a očekává se, že nákupní objednávka dorazí osm dní ode dneška. V takovém případě bude nákupní objednávka použita jako nabídka pro poptávku, což je pět dní ode dneška.

Proto doporučujeme upravit dobu realizace tak, aby pokryla všechny (nebo téměř všechny) vaše scénáře.
