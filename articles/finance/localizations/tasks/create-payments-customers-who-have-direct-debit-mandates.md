---
title: Vytváření plateb pro odběratele, který má zmocnění k přímému debetu
description: Tato procedura ukazuje, jak generovat soubor plateb přímého debetu ISO20022 pro odběratele, který má nakonfigurován přímý debet a fakturu k zaplacení.
author: mrolecki
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustFreeInvoice, CustTableLookup, CustPostInvoiceJob, LedgerJournalTable, LedgerJournalTransCustPaym, SysQueryForm, CustPaymProposalEdit, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fa017b1d5cab377d1f36604cf54435beb6a4abb5
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5822670"
---
# <a name="create-payments-for-a-customer-who-have-direct-debit-mandates"></a>Vytváření plateb pro odběratele, který má zmocnění k přímému debetu

[!include [banner](../../includes/banner.md)]

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
11. Klepněte na tlačítko OK.
12. Klepněte na tlačítko OK.
13. Klikněte na Vytvořit platby.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]