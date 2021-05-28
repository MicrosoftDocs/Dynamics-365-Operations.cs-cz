---
title: Prodejní objednávku zákazníka nelze fakturovat
description: Po povolení možnosti Automaticky zaúčtovat fakturu již nebudete moci fakturovat původní prodejní objednávku a původní nákupní objednávku přímé dodávky.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: SalesEditLines
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: ab18a2a1dec4b70c55a55637b087c6b11023aa40
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026333"
---
# <a name="you-cant-invoice-a-customer-facing-sales-order"></a>Prodejní objednávku zákazníka nelze fakturovat

Číslo článku znalostní báze: 4611793

## <a name="symptoms"></a>Příznaky

Po povolení možnosti **Automaticky zaúčtovat fakturu** na stránce **Mezipodnikové** dodavatele již nebudete moci fakturovat původní prodejní objednávku a původní nákupní objednávku přímé dodávky.

## <a name="resolution"></a>Rozlišení

Chování synchronizace pro faktury mezipodnikové a přímé dodávky je řízeno a vynuceno parametry, které jsou popsány v tématu [Nastavení parametrů pro zaúčtování mezipodnikové objednávky](/dynamicsax-2012/appuser-itpro/set-up-parameters-to-post-an-intercompany-order).

Po nastavení těchto parametrů musíte nejprve fakturovat mezipodnikovou prodejní objednávku. Původní prodejní objednávky a nákupní objednávky budou poté synchronizovány.
