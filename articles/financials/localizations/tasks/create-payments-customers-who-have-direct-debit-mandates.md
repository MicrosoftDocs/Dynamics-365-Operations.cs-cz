---
title: Vytváření plateb pro odběratele, který má zmocnění k přímému debetu
description: Tato procedura ukazuje, jak generovat soubor plateb přímého debetu ISO20022 pro odběratele, který má nakonfigurován přímý debet a fakturu k zaplacení.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustFreeInvoice, CustTableLookup, CustPostInvoiceJob, LedgerJournalTable, LedgerJournalTransCustPaym, SysQueryForm, CustPaymProposalEdit, BankAccountTableLookUp
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6781ac38fff6344bfc9546c3ffd2253fb3ef712c
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "342125"
---
# <a name="create-payments-for-a-customer-who-have-direct-debit-mandates"></a>Vytváření plateb pro odběratele, který má zmocnění k přímému debetu

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tato procedura ukazuje, jak generovat soubor plateb přímého debetu ISO20022 pro odběratele, který má nakonfigurován přímý debet a fakturu k zaplacení. Vytvoření a zaúčtování faktury je volitelné. Namísto faktury k zaplacení můžete vybrat zmocnění v deníku před generováním souboru plateb, na podporu scénáře zálohy odběratele.



K vytvoření tohoto postupu jsou použita ukázková data společnosti DEMF.



Toto je pátá z pěti procedur, které demonstrují proces plateb odběratele pomocí konfigurací elektronického výkaznictví. Před dokončením tohoto úkolu je třeba dokončit předchozí úkoly. Je nutné nejprve importovat konfigurace elektronického výkaznictví plateb odběratele, konfigurovat metodu plateb a nastavit informace o společnosti a odběrateli. 


## <a name="post-a-free-text-invoice-with-direct-debit-information"></a>Zaúčtování volné faktury s informacemi o přímém debetu
1. Přejděte na Pohledávky > Faktury > Všechny volné faktury.
2. Klikněte na položku Nová.
3. V poli Účet odběratele zadejte nebo vyberte hodnotu.
    * Vyberte například DE-010.  
4. V poli Metody platby zadejte nebo vyberte hodnotu.
    * Například Vyberte Elektronicky.  
5. V poli ID zmocnění k přímému debetu zadejte nebo vyberte hodnotu.
6. Klikněte na Přidat řádek.
7. Zadejte hodnotu do pole Popis.
8. Zadejte požadované hodnoty do pole Hlavní účet.
9. Zadejte číslo do pole Jednotková cena.
10. Klikněte na položku Zaúčtovat.
11. Klikněte na tlačítko OK.

## <a name="create-a-payment"></a>Vytvořte platby
1. Přejděte na Pohledávky > Platby > Deník plateb.
2. Klikněte na položku Nová.
3. V poli Název zadejte nebo vyberte hodnotu.
4. Klikněte na položku Řádky.
5. Klikněte na Návrh platby.
6. Klikněte na Vytvořit návrh plateb.
7. Rozbalte oddíl Záznamy k zahrnutí.
8. Klepněte na tlačítko Filtr.
9. V seznamu vyberte řádek v tabulce Transakce zákazníka a v poli Metoda platby.
    * Můžete použít libovolná kritéria pro výběr transakcí odběratele k zaplacení. V tomto příkladu jako metodu platby k filtrování transakcí použijte Elektronicky.  
10. V poli Kritéria zadejte nebo vyberte hodnotu.
11. Klikněte na tlačítko OK.
12. Klikněte na tlačítko OK.
13. Klikněte na Vytvořit platby.

## <a name="generate-a-payment-file"></a>Vygenerování souboru platby

