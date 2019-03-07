---
title: Vklad platby odběratele
description: Vložení platby odběratele.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransCustPaym, CustTableLookup
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f58cebce20e8516dc918e0bad1e020ffd7f791ee
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "313375"
---
# <a name="deposit-customer-payments"></a>Vklad platby odběratele

[!include [task guide banner](../../includes/task-guide-banner.md)]

Vložení platby odběratele. Tento úkol používá ukázkovou společnost USMF.

1. Přejděte na Pohledávky > Platby > Deník plateb.
2. Klikněte na položku Nová.
3. V poli Název kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
4. Vyberte deník platby. 
5. Klikněte na možnost Řádky.
6. V poli Účet vyberte odběratele, od kterého jste platbu zaznamenali.
7. V poli Dobropis zadejte částku platby.
    * Můžete určit, že chcete částku ponechat prázdnou a nechat systém vypočítat ji pomocí výběru faktur, které byly zaplaceny.  
8. Zadejte hodnotu do pole Odkaz na platbu.
    * Platební odkaz může být číslo šeku pro platbu, kterou zadáváte. Platební reference je vyžadována, pokud označíte zahrnutí platby na vkladové složence.  
9. Zaškrtněte pole Použít vklad. složenku.
    * Má-li být platba zahrnuta do zálohy, toto nastavení změňte na hodnotu Ano.  
10. Klikněte na položku Nová.
11. V poli Účet vyberte odběratele pro další platbu.
12. Do pole Dobropis zadejte výši úhrady.
13. Zadejte hodnotu do pole Odkaz na platbu.
14. Zaškrtněte pole Použít vklad. složenku.
15. Klikněte na položku Zaúčtovat.
    * Předtím, než lze generovat vkladové složenky, musí být zaúčtována platba. Tím je zajištěno, že platby se nezmění po vygenerování vkladové složenky.  
16. Klepněte na možnost Funkce.
17. Klikněte na Vkladová složenka.
18. Klikněte na tlačítko OK.
    * První stránka slouží k vytvoření vkladové složenky.  
19. Klikněte na tlačítko OK.
    * Druhý krok je tisk vkladové složenky, ale tento krok není nutný.  

