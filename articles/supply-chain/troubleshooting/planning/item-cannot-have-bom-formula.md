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
ms.openlocfilehash: 6739b8b1e4d080055a2a0501427eac1c2e8a96c5
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294029"
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
