---
title: Při vytváření řádků prodejní objednávky je vybrána stejná obchodní dohoda
description: Pokud je pro dané datum definována více než jedna obchodní smlouva, je při vytváření řádků prodejní objednávky vždy vybrána taková obchodní smlouva, která má nejnižší cenu.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
ms.search.form: SalesTable, SalesTableListPage, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: a586a399fb349965b972191bec1271651bec5fcb
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475801"
---
# <a name="if-two-trade-agreements-exist-for-overlapping-dates-the-same-one-is-always-selected"></a>Pokud pro překrývající se data existují dvě obchodní smlouvy, je vždy vybrána stejná

## <a name="symptoms"></a>Příznaky

Pokud jsou definovány dvě obchodní smlouvy pro stejné období nebo překrývající se období, zdá se, že stejná obchodní smlouva je vybrána pokaždé, když vytvoříte řádky prodejní objednávky, které obsahují tyto položky.

## <a name="resolution"></a>Řešení

Pokud pro dané datum existuje více než jedna obchodní smlouva, je vždy vybrána obchodní smlouva, která má nejnižší cenu. Další informace získáte stažením následujícího dokumentu whitepaper: [Obchodní smlouvy v Microsoft Dynamics AX 2012](https://www.axug.com/HigherLogic/System/DownloadDocumentFile.ashx?DocumentFileKey=3396a3a8-1f48-4d85-8cd6-5fa982f62e90).
