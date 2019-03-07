---
title: Nastavit kódy DPH
description: Kódy DPH se vytvoří pro každou nepřímou daň nebo clo, které je právnická osoba povinna vypočítávat, shromažďovat o nich informace a platit je finančním úřadům.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable, TaxData
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f29442c2ef2e3d0008a74298fda218e4cbd93f8e
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "349163"
---
# <a name="set-up-sales-tax-codes"></a>Nastavit kódy DPH

[!include [task guide banner](../../includes/task-guide-banner.md)]

Kódy DPH se vytvoří pro každou nepřímou daň nebo clo, které je právnická osoba povinna vypočítávat, shromažďovat o nich informace a platit je finančním úřadům.

Tento úkol používá ukázkovou společnost USMF.



1. Přejděte na Daň > Nepřímé daně > DPH > Kódy DPH.
2. Klikněte na položku Nová.
3. V poli Kód prodejní daně zadejte hodnotu.
4. Zadejte hodnotu do pole Název.
5. Vyberte Období vyrovnání a určete, pro které finanční úřady a v jakých intervalech je tato DPH vykazována a zaplacena.
6. Klikněte na odkaz na vybraném řádku v seznamu.
7. Vyberte možnost Skupina zaúčtování hl. knihy a určete hlavní účty pro zaúčtování DPH do hlavní knihy.
8. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
9. Klikněte na odkaz na vybraném řádku v seznamu.
10. Rozbalte pevnou záložku Výpočet.
    * Na pevné záložce Výpočet naleznete několik polí určujících způsob výpočtu částky DPH.  
11. V podokně akcí klikněte na možnost Kód prodejní daně.
12. Klepněte na položku Hodnoty.
13. Označte v seznamu vybraný řádek.
14. Zadejte hodnotu pro tento kód daně.
    * Pokud je vybrána možnost Částka za jednotku, hodnota na pevné záložce Výpočet v poli Zdroj se vynásobí množstvím v transakci a vypočítá se částka DPH.  Pokud kód daně není daní na základě jednotky, hodnota je procentuální a použije se pro Původ pro tento kód daně k výpočtu částky DPH.     
15. Klikněte na položku Uložit.
16. Zavřete stránku.
17. Klikněte na položku Uložit.

