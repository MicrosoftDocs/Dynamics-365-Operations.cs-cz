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
ms.openlocfilehash: 49faa2c68d496c5c0d8c7e4abfd93d9a917857220dd23c09a050fa3436e1d49a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6746860"
---
# <a name="physically-received-purchase-orders-dont-appear-on-the-inventory-closing-report"></a>Fyzicky přijaté nákupní objednávky se v závěrečném přehledu zásob neobjeví

Číslo článku znalostní báze: 4612595

## <a name="symptoms"></a>Příznaky

Fyzicky přijaté nákupní objednávky se neobjeví v závěrečném přehledu zásob **Zkontrolovat otevřená množství**.

## <a name="resolution"></a>Rozlišení

Zpráva **Zkontrolujte otevřené množství** zobrazuje transakce vystavení, které nelze k vybranému datu uzávěrky vypořádat proti finančně aktualizovaným příjmům ze skladu. Můžete se rozhodnout zahrnout do sestavy fyzické příjmy. V takovém případě se zobrazí fyzické příjmy, pokud mohou pokrýt emisní transakce, které nelze vypořádat. Další informace naleznete v tématu [Příprava na spuštění zásob](/dynamicsax-2012/appuser-itpro/preparing-to-run-inventory-close).
