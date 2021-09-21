---
title: Maximální limit kupní smlouvy na nákupní žádanku není účinný
description: Maximální limit kupní smlouvy na nákupní žádanku není účinný
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart, PurchRFQTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: c19d40dce65acbe80d4572bfc4e925aa87ea4f02
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475774"
---
# <a name="the-purchase-agreement-maximum-limit-isnt-effective-on-a-purchase-requisition"></a>Maximální limit kupní smlouvy na nákupní žádanku není účinný

## <a name="symptoms"></a>Příznaky

Pokud je nákupní žádanka propojena s nákupní smlouvou, maximální limit z nákupní smlouvy neplatí na nákupní žádance. Informace o výchozí ceně jsou správně zadány, ale v nákupní žádance lze objednat více, než je maximální limit z kupní smlouvy.

## <a name="resolution"></a>Řešení

Toto chování se očekává. Protože žádanky nejsou vždy schváleny, nemělo by být v nákupní smlouvě vyhrazeno množství nebo částka. Proto nesplníte maximální limit z nákupní smlouvy.
