---
title: Správci systému nemohou vymazat pozastavení objednávky, protože nejsou autorizovaní
description: Správci systému nemohou vymazat pozastavení objednávky, protože nejsou autorizovaní.
author: SmithaNataraj
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: acabd6409d9b2860535335bc648bcc34304e0cb0
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026354"
---
# <a name="system-administrators-cant-clear-order-holds-because-they-arent-authorized"></a>Správci systému nemohou vymazat pozastavení objednávky, protože nejsou autorizovaní

Číslo článku znalostní báze: 4614642

## <a name="symptoms"></a>Příznaky

Správci systému nemohou vymazat pozastavení prodejní objednávky, pokud nemají konkrétní roli, která je přiřazena v kódu blokování objednávky.

## <a name="resolution"></a>Rozlišení

Přístup k některým operacím, jako je zúčtování blokování prodejní objednávky, je řízen nastavením obchodních zásad. Správci systému obvykle nemají povoleno provádět operace tohoto typu. 

Častěji se přístup k provedení konkrétního úkolu řídí obchodními zásadami a k provádění tohoto úkolu jsou povoleny pouze konkrétní osoby v organizaci. Mezi příklady patří schválení, která jsou výsledkem schválení pracovního postupu, a konkrétní úkoly, které jsou výsledkem konfigurace pracovního postupu.

Ačkoli s přidržením objednávky není spojen žádný pracovní postup, princip je podobný. Relevantní role označuje konkrétní skupinu lidí v organizaci, kteří mají právo vymazat blokování objednávky. Toto právo by nemělo být nutně uděleno všem správcům, protože tento přístup porušuje definované obchodní zásady.
