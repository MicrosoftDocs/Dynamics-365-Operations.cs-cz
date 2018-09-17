--- 
title: "Zpracování deníku přidělení hlavní knihy"
description: "Použijte stránku Požadavek na přidělení procesu k vytvoření deníku přidělování, který lze před zaúčtováním do hlavní knihy zkontrolovat a schválit nebo přímo zaúčtovat do hlavní knihy."
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerAllocationRequest, LedgerJournalTable, LedgerJournalTransAllocation
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 7d299657758b1e1322aef07bfe8c71f7bf00b0ca
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="process-ledger-allocation-journal"></a>Zpracování deníku přidělení hlavní knihy

[!include [task guide banner](../../includes/task-guide-banner.md)]

Použijte stránku Požadavek na přidělení procesu k vytvoření deníku přidělování, který lze před zaúčtováním do hlavní knihy zkontrolovat a schválit nebo přímo zaúčtovat do hlavní knihy. Předtím, než budete moci vytvořit deník přidělení, je nejprve nutné mít aktivní alespoň jedno pravidlo přidělení hlavní knihy. Tento úkol využívá ukázkovou společnost USMF.

1. Přejděte do hlavní knihy > Přidělení > Požadavek na přidělení procesu.
2. V poli Pravidlo klepnutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
3. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
4. Klikněte na odkaz na vybraném řádku v seznamu.
5. Do pole K datu zadejte datum.
    * Datum je velmi důležité, když je hlavní kniha zdrojem dat pro pravidlo. Toto datum určuje, jaké zůstatky hlavní knihy budou zahrnuty do přidělení.     V poli Nulový zdroj vyberte Zastavit. To zastaví proces přidělování a zobrazí zprávu informující o tom, že je vybrána nulová zdrojová částka.  
6. V poli Možnosti návrhu vyberte „Pouze návrh“.
    * Vyberte Návrh pouze zkontrolovat a před zaúčtováním přidělení do hlavní knihy volitelně schvalte výsledek v Denících přidělení.  
7. Zadejte datum do pole Datum zaúčtování do hlavní knihy.
8. Klepněte na tlačítko OK.
9. Přejděte do hlavní knihy > Přidělení > Deníky přidělení.
10. Klikněte na možnost Řádky.
11. Klikněte na možnost Zaúčtovat.
12. Klikněte na možnost Zaúčtovat.


