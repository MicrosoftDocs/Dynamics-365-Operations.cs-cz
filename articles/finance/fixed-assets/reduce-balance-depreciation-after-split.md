---
title: Snížení odpisu zůstatku po rozdělení
description: Tento článek popisuje metodu, která se používá v dlouhodobém majetku k výpočtu odpisů po rozdělení majetku pomocí metody snížení zůstatku.
author: moaamer
ms.date: 11/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-11-17
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 539967a9a73da91f6b49c1bb89f404267ae0a804
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8883293"
---
# <a name="reduce-balance-depreciation-after-a-split"></a>Snížení odpisu zůstatku po rozdělení

[!include [banner](../includes/banner.md)]

Tento článek popisuje metodu, která se používá v Dlouhodobém majetku k výpočtu odpisů po rozdělení majetku na jiný pomocí metody snížení zůstatku. Rok odpisování, který je nakonfigurován v knize majetku, je fiskální rok. Další informace viz [Snížení odpisu zůstatku](reduce-balance-depreciation.md) a [Rozdělení dlouhodobého majetku](tasks/split-fixed-asset.md).

Pokud rozdělíte dlouhodobý majetek během fiskálního období, které je pozdější než období, kdy byl majetek získán, odpisy sníženého zůstatku budou představovat čistou účetní hodnotu majetku (NBV) za předchozí rok. Bude také účtovat transakce úpravy akvizic a odpisů, které byly generovány z transakce, která rozděluje majetek. Toto chování předpokládá, že majetek byl získán v jednom fiskálním roce a rozdělen v pozdějším fiskálním roce. Částka, která musí být odepsána pro původní majetek po rozdělení, odráží NBV majetku před rozdělením majetku a transakci úpravy akvizice a odpisů, která byla zaúčtována pro rozdělení.

Platí například následující podmínky:

- Fiskální období je od 30. června do 1. července.
- Procento redukčního zůstatku je 18 procent a majetek je získán v červnu 2019 za pořizovací cenu 10 000 USD.
- Odpisy prvního fiskálního roku se rovnají 18 000 USD, měsíční odpisy se rovnají 150 USD a majetek se poté odepisuje do listopadu 2019, a to ve výši 738 75 USD.
- V listopadu 2019 je 80 procent majetku rozděleno na jiný dlouhodobý majetek.

[![Snížení odpisu zůstatku po rozdělení.](./media/reduce-balance-depreciation-after-split.png)](./media/reduce-balance-depreciation-after-split.png)

Částka k odpisu u původního majetku je 1 822,25 USD. Tato částka se rovná NBV před zaúčtováním rozdělené transakce (9 111,25 USD) plus úprava akvizice, která je generována během účtování rozdělené transakce (-8 000 USD), plus úprava odpisů, která je generována během rozdělené transakce (711 USD). Proto je odpis za druhý rok (1 822,25 × 18 procent) ÷ 12 = 27,33 USD.

Částka k odpisu nového dlouhodobého majetku v prvním roce je (8 000 × 18 procent) ÷ 12 = 120 USD.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
