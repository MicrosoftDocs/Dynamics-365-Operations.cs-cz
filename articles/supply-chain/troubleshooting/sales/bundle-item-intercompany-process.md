---
title: V mezipodnikovém procesu není položka sady podporována
description: Položku sady nelze zakoupit. Prodejní objednávka nakupuje pouze součásti položky sady, nikoli samotnou položku sady.
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
ms.openlocfilehash: 21adc7d071837b762157364f6f8ed370c69c7fd3
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475798"
---
# <a name="a-bundle-item-isnt-supported-in-an-intercompany-process"></a>V mezipodnikovém procesu není položka sady podporována

## <a name="symptoms"></a>Příznaky

Položka sady není pro nákupní objednávku k dispozici, protože pokud prozkoumáte řádky prodejní objednávky pro položku sady, zjistíte, že množství je *0* (nula) a stav je *Zrušeno*.

## <a name="resolution"></a>Řešení

Toto chování je záměrné. Prodejní objednávka nakupuje pouze komponenty položky sady. Nezakupuje samotnou položku sady. Pokud si musíte koupit sadu, zvažte, zda ji musíte označit jako položku sady, protože tato funkce je navržena pro scénáře rozpoznávání výnosů. Další informace o položkách sady naleznete v tématu [Sady](/dynamics365/finance/accounts-receivable/revenue-recognition-setup).
