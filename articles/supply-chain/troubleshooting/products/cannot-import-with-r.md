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
ms.openlocfilehash: efd773313f89784d8fca6b37d867e204cb2d06ab29694a19cbec7eed107a8019
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6764685"
---
# <a name="you-cant-import-an-item-by-using-the-released-products-v2-entity"></a>Položku nelze importovat pomocí entity Vydané produkty V2

Číslo článku znalostní báze: 4611825

## <a name="symptoms"></a>Příznaky

Když se pokusíte importovat položku pomocí entity *Vydané produkty V2*, zobrazí se chybová zpráva podobná následujícímu příkladu:

> Nelze vytvořit záznam ve skupinách Položky - sledovací dimenze (EcoResTrackingDimensionGroupItem). Číslo položky: 2040663, dávka. Záznam již existuje.

## <a name="resolution"></a>Rozlišení

Chcete-li importovat nově vydané produkty, musíte použít entitu *Vydání produktu V2* místo entity *Vydané produkty V2*.
