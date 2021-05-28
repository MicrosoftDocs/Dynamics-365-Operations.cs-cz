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
ms.openlocfilehash: 8182f2f83f6a3e4cf54fe6fa64b25a2f461ff541
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026329"
---
# <a name="you-cant-import-an-item-by-using-the-released-products-v2-entity"></a>Položku nelze importovat pomocí entity Vydané produkty V2

Číslo článku znalostní báze: 4611825

## <a name="symptoms"></a>Příznaky

Když se pokusíte importovat položku pomocí entity *Vydané produkty V2*, zobrazí se chybová zpráva podobná následujícímu příkladu:

> Nelze vytvořit záznam ve skupinách Položky - sledovací dimenze (EcoResTrackingDimensionGroupItem). Číslo položky: 2040663, dávka. Záznam již existuje.

## <a name="resolution"></a>Rozlišení

Chcete-li importovat nově vydané produkty, musíte použít entitu *Vydání produktu V2* místo entity *Vydané produkty V2*.
