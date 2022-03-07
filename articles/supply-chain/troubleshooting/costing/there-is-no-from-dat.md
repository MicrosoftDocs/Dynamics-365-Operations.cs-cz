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
ms.openlocfilehash: 3dd13f6a3e5ce3c894e96f420358d337f2e43dba
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026352"
---
# <a name="there-is-no-from-date-value-on-the-active-prices-tab-of-the-item-price-page"></a>Na kartě Aktivní ceny na stránce Cena zboží není žádná hodnota od data

Číslo článku znalostní báze: 4613548

## <a name="symptoms"></a>Příznaky

Na kartě **Aktivní ceny** na stránce **Cena zboží** není žádná hodnota **Od data**.

## <a name="resolution"></a>Rozlišení

Hodnota **Od data** (datum účinnosti), která je nastavena na nevyřízenou cenu, se nepřenáší na aktivní cenu.

Záznam o ceně položky má po vložení stav *Čeká na zpracování* a zamýšlené datum účinnosti. Když záznamu o ceně položky aktivujete, změní se jeho stav na *Aktivní* a datum účinnosti se změní na datum aktivace. Proto je datum aktivace aktivní ceny vždy skutečným datem aktivace.

Další informace naleznete v tématu [Přehled verzí výpočtu nákladů](../../cost-management/costing-versions.md).
