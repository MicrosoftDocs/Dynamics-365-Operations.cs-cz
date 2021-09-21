---
title: Chyba výpočtu zpětného účtování nákladů při uzávěrce zásob
description: V dřívějších vydáních jste možná při uzavírání zásob obdrželi chybu výpočtu zpětného účtování nákladů. Tento problém byl vyřešen.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: ae92b7121998d6b1ba2f08ea5736c55637867fbf
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475781"
---
# <a name="backflush-costing-calculation-error-during-inventory-closing"></a>Chyba výpočtu zpětného účtování nákladů při uzávěrce zásob

## <a name="symptoms"></a>Příznaky

Ve verzích před vydáním 10.0.13, pokud nepoužíváte tok výpočtu nákladů štíhlé výroby, zobrazí se během uzávěrky skladu následující chybová varovná zpráva:

> Chystáte se provést uzávěrku skladu s datem %1. Žádné provedení výpočtu zpětného účtování nákladů s datem konce odpovídajícího období %1 nebylo zaregistrováno. Nezapomeňte spustit výpočet zpětného účtování nákladů s datem konce odpovídajícího období %1. Ocenění zásob, náklady prodaného zboží a odchylky nemusí být správné v dílčí knize nebo hlavní knize, dokud to nebude provedeno.

## <a name="resolution"></a>Řešení

Tento problém byl opraven ve verzi 10.0.13 a novější. Další informace naleznete v [KB 4582468](https://fix.lcs.dynamics.com/Issue/Details?kb=4582468&bugId=468844&dbType=3&qc=fcd64080446a27382cfde3e4c3bdcfb714279185932259cd11ceb0d500617296).
