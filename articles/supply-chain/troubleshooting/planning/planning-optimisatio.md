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
ms.openlocfilehash: 826496c2de956ff949dd79ab8aa643053719bf75
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026343"
---
# <a name="planned-purchase-order-is-created-when-a-purchase-exists-within-negative-days"></a>Plánovaná nákupní objednávka se vytvoří, když nákup existuje do záporných dnů

Číslo článku znalostní báze: 4614298

## <a name="symptoms"></a>Příznaky

Pokud je kód pokrytí *min./max.*, Optimalizace plánování vytvoří plánovanou nákupní objednávku, pokud existuje nákup v záporných dnech.

## <a name="resolution"></a>Rozlišení

Optimalizace plánování nepodporuje negativní dny. Vždy však zajistí, že plánované objednávky nebudou naplánovány v době realizace vzhledem k aktuálnímu datu. Například dodací lhůta pro nákup je 10 dní a očekává se, že nákupní objednávka dorazí osm dní ode dneška. V takovém případě bude nákupní objednávka použita jako nabídka pro poptávku, což je pět dní ode dneška.

Proto doporučujeme upravit dobu realizace tak, aby pokryla všechny (nebo téměř všechny) vaše scénáře.
