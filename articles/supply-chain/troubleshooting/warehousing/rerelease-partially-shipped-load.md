---
title: Částečně odeslaný náklad nelze uvolnit do skladu
description: V dřívějších verzích jste nemohli částečně uvolněný náklad znovu uvolnit při použití určitých funkcí s neúplnými rezervacemi. To bylo vyřešeno.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 0380e1963a38f2be55b31e06b3845f935661eed2
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475813"
---
# <a name="cant-re-release-a-partially-shipped-load-to-the-warehouse"></a>Částečně odeslaný náklad nelze uvolnit do skladu

## <a name="symptoms"></a>Příznaky

Částečně odeslaný náklad nemůžete uvolnit do skladu. Když provedete uvolnění do skladu, zobrazí se zpráva „Operace dokončena“, ale nic se nestane a pro zbývající množství se nevytvoří žádná práce. K tomuto problému dochází, když použijete funkci transportu nákladu a dojde k neúplné rezervaci.

## <a name="resolution"></a>Řešení

[Problém KB 470069](https://fix.lcs.dynamics.com/Issue/Details?kb=4574490&bugId=470069&dbType=3&qc=84ce1e09d7032d8b8ef86f5a0c68b86badf3dfaf29686c5ebbe97c53c0957b5f) („Částečně odeslané náklady lze znovu zařadit do vlny a zpracovat“) je opraven [vydaná verze 10.0.15](/dynamics365/supply-chain/get-started/whats-new-scm-10-0-15).
