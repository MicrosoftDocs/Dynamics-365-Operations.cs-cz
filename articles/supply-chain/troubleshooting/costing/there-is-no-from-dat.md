---
title: Na kartě Aktivní ceny na stránce Cena zboží není žádná hodnota od data
description: Na kartě Aktivní ceny na stránce Cena zboží není žádná hodnota od data.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventItemPrice
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: dc0071bc508fc1b2fcfa5071f0756434641b7e6f872308ed4febb0cb34d37840
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6730123"
---
# <a name="there-is-no-from-date-value-on-the-active-prices-tab-of-the-item-price-page"></a>Na kartě Aktivní ceny na stránce Cena zboží není žádná hodnota od data

Číslo článku znalostní báze: 4613548

## <a name="symptoms"></a>Příznaky

Na kartě **Aktivní ceny** na stránce **Cena zboží** není žádná hodnota **Od data**.

## <a name="resolution"></a>Rozlišení

Hodnota **Od data** (datum účinnosti), která je nastavena na nevyřízenou cenu, se nepřenáší na aktivní cenu.

Záznam o ceně položky má po vložení stav *Čeká na zpracování* a zamýšlené datum účinnosti. Když záznamu o ceně položky aktivujete, změní se jeho stav na *Aktivní* a datum účinnosti se změní na datum aktivace. Proto je datum aktivace aktivní ceny vždy skutečným datem aktivace.

Další informace naleznete v tématu [Přehled verzí výpočtu nákladů](../../cost-management/costing-versions.md).
