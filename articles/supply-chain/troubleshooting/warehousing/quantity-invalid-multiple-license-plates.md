---
title: Množství není platné pro vychystávání prací s více LP
description: Když existuje vychystávací práce s více registračními značkami na jednom místě, množství není platné pro jednotku ks. Ověřte, zda jsou následující pole správná.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 5b245f71e80339fee3e42cfffa0396078a56926e
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475755"
---
# <a name="quantity-not-valid-when-theres-picking-work-with-multiple-lps-in-one-location"></a>Množství není platné, pokud probíhají práce vyzvedávání s více registračními značkami na jednom místě

## <a name="symptoms"></a>Příznaky

Když existuje vychystávací práce s více registračními značkami na jednom místě, množství není platné pro jednotku *ks* a zobrazí se následující chybová zpráva:

> Pro jednotku 1% není množství platné.

## <a name="resolution"></a>Řešení

Ověřte, že pole **ID skupiny pořadí jednotek** a **Převody jednotek** na uvolněném produktu nebo variantě produktu jsou nastavena správně.

Upozorňujeme, že ve verzi 10.0.15 byla vylepšena chybová zpráva, aby se zobrazilo očekávané množství (viz [KB 4581627](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486531)). Nová chybová zpráva je:

> Množství není platné. Očekáváno %1 %2.
