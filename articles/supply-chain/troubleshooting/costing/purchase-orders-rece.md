---
title: Fyzicky přijaté nákupní objednávky se v závěrečném přehledu zásob neobjeví
description: Fyzicky přijaté nákupní objednávky se neobjeví v závěrečném přehledu zásob Zkontrolovat otevřená množství.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventOpenQtyCritical
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 9508d6d75d8ebee7ca10140ed4c4215d7ad1dda7
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026337"
---
# <a name="physically-received-purchase-orders-dont-appear-on-the-inventory-closing-report"></a>Fyzicky přijaté nákupní objednávky se v závěrečném přehledu zásob neobjeví

Číslo článku znalostní báze: 4612595

## <a name="symptoms"></a>Příznaky

Fyzicky přijaté nákupní objednávky se neobjeví v závěrečném přehledu zásob **Zkontrolovat otevřená množství**.

## <a name="resolution"></a>Rozlišení

Zpráva **Zkontrolujte otevřené množství** zobrazuje transakce vystavení, které nelze k vybranému datu uzávěrky vypořádat proti finančně aktualizovaným příjmům ze skladu. Můžete se rozhodnout zahrnout do sestavy fyzické příjmy. V takovém případě se zobrazí fyzické příjmy, pokud mohou pokrýt emisní transakce, které nelze vypořádat. Další informace naleznete v tématu [Příprava na spuštění zásob](/dynamicsax-2012/appuser-itpro/preparing-to-run-inventory-close).
