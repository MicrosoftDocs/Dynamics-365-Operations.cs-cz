---
title: Položku nelze importovat pomocí entity Vydané produkty V2
description: Položku nelze importovat pomocí entity Vydané produkty V2.
author: t-benebo
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: EcoResProductDetailsExtended, DataManagementWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: myvakalo
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: bf6eb0eb755de3f2842c235946bfd7ccad04ccf7
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/07/2021
ms.locfileid: "7474717"
---
# <a name="you-cant-import-an-item-by-using-the-released-products-v2-entity"></a>Položku nelze importovat pomocí entity Vydané produkty V2

Číslo článku znalostní báze: 4611825

## <a name="symptoms"></a>Příznaky

Když se pokusíte importovat položku pomocí entity *Vydané produkty V2*, zobrazí se chybová zpráva podobná následujícímu příkladu:

> Nelze vytvořit záznam ve skupinách Položky - sledovací dimenze (EcoResTrackingDimensionGroupItem). Číslo položky: 2040663, dávka. Záznam již existuje.

## <a name="resolution"></a>Rozlišení

Chcete-li importovat nově vydané produkty, musíte použít entitu *Vydání produktu V2* místo entity *Vydané produkty V2*.
