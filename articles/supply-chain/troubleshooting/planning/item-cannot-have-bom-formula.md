---
title: Položka nemůže mít kusovník ani recepturu
description: Když se pokusíte potvrdit objednávku, během ověřování položky se zobrazí chybová zpráva. Uvádí, že položka nemůže mít kusovník (BOM) ani recepturu.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPO
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 1e946adc3a04db60bf15ac7bb44163085e1c19802872964877d3929b1f79bf7d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6730099"
---
# <a name="item-cant-have-a-bom-or-formula"></a>Položka nemůže mít kusovník ani recepturu

Kód chyby: PRO2614

## <a name="symptoms"></a>Příznaky

Když se pokusíte vyřídit objednávku, během ověřování položky se zobrazí následující chybová zpráva:

> Položka nemůže mít kusovník ani recepturu

## <a name="resolution"></a>Řešení

Položky, které mají kusovník nebo recepturu, musí mít typ *Položka plánování*, *Kusovník* nebo *receptura*. Chcete-li změnit typ položky, postupujte následovně.

1. Přejděte na **Řízení informací o produktech \> Produkty \> Uvolněné produkty**.
1. Otevřete relevantní produkt.
1. Na pevné záložce **Technik** nastavte pole **Typ výroby** na *Položka plánování*, *Kusovník* nebo *receptura*.
