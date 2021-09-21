---
title: Nahlášení dokončené aktualizace selže s chybou chybějícího množství
description: Pokud se pokusíte ukončit výrobní zakázku, když hlásíte chybné množství, ale nikoliv množství materiálu, aktualizace sestavy jako dokončené selže.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 7785549c47063727f2749749940c1a96a351e70f
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475767"
---
# <a name="report-as-finished-update-fails-with-a-missing-quantity-error"></a>Nahlášení dokončené aktualizace selže s chybou chybějícího množství

## <a name="symptoms"></a>Příznaky

Pokoušíte se vykázat výrobní zakázku jako dokončenou, když hlásíte chybné množství, ale nikoliv, když hlásíte čas nebo množství materiálu. Aktualizace hlášení jako dokončeného selže při pokusu o ukončení výrobní zakázky a zobrazí se následující chybová zpráva:

> Chybí množství dokončené výroby.

## <a name="resolution"></a>Řešení

Pokud hlásíte chybné množství na výrobní zakázce, musíte nahlásit také správné množství.
