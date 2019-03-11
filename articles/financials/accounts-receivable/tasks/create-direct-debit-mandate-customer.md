---
title: Vytvoření zmocnění k přímému debetu pro odběratele
description: Tento průvodce úkolem ukazuje, jak vytvořit zmocnění k přímému debetu a použít je ve faktuře.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, CustBankAccounts, BankAccountTable, CustPaymMode, CustDirectDebitMandate, BankAccountTableLookUp, SrsReportViewerForm,  LogisticsAddressCityLookup, CustFreeInvoice, CustTableLookup
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fc3052fdfc6e3dcf2826b3069f6d644201a70c3c
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "346886"
---
# <a name="create-a-direct-debit-mandate-for-a-customer"></a>Vytvoření zmocnění k přímému debetu pro odběratele

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tento průvodce úkolem ukazuje, jak vytvořit zmocnění k přímému debetu a použít je ve faktuře.


## <a name="create-a-bank-account"></a>Vytvoření bankovního účtu
1. Přejděte na Pohledávky > Zákazníci > Všichni odběratelé.
2. Vyberte například US-001.
3. V podokně akcí klikněte na možnost Odběratel.
4. Klikněte na možnost Bankovní účty.
5. Klikněte na položku Nová.
6. Zadejte hodnotu do pole Bankovní účet.
7. Zadejte hodnotu do pole Název.
8. Zadejte hodnotu do pole IBAN.
9. Zadejte hodnotu do pole Měna.
10. Klikněte na položku Uložit.
11. Zavřete stránku.
12. Přejděte do části Pokladna a banka > Bankovní účty > Bankovní účty.
13. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
14. Klikněte na odkaz na vybraném řádku v seznamu.
15. Klikněte na položku Upravit.
16. Rozbalte oddíl Další identifikace.
17. Zadejte hodnotu do pole ID přímého debetu.
18. Zadejte hodnotu do pole IBAN.
19. Zavřete stránku.
20. Zavřete stránku.

## <a name="define-the-electronic-payment-method"></a>Definování metody elektronické platby
1. Přejděte do nabídky Pohledávky > Nastavení platby > Metody platby.
2. Klikněte na položku Nová.
3. V poli Způsob platby zadejte hodnotu.
4. Zadejte nějakou hodnotu do pole Popis.
5. Typ platby pro metodu platby „zmocnění k přímému debetu“ musí být elektronická platba.
6. Vyberte možnost Ano v poli Požadovat zmocnění.
7. Zavřete stránku.

## <a name="add-a-direct-debit-mandate-to-a-customer"></a>Přidejte zmocnění k přímému debetu zákazníkovi.
1. Přejděte na Pohledávky > Zákazníci > Všichni odběratelé.
2. Vyberte například US-001.
3. Klikněte na položku Upravit.
4. Rozbalte položku Výchozí nastavení plateb.
5. V poli Metody platby zadejte nebo vyberte hodnotu.
6. Rozbalte položku Výchozí nastavení plateb.
7. Rozbalte část Zmocnění k přímému debetu.
8. Klepněte na možnost Přidat.
9. V poli Bankovní účet zadejte nebo vyberte hodnotu.
10. V poli Bankovní účet věřitele zadejte nebo vyberte hodnotu.
11. Zadejte počet plateb, u kterých očekáváte, že budou zpracovány pro zmocnění.
12. Klikněte na tlačítko OK.
13. Klepněte na položku Tisk.
14. Klikněte na Sestava zmocnění.
15. Zavřete stránku.
16. Klikněte na položku Upravit.
17. Do pole Datum podpisu zadejte datum.
18. Klepněte na tlačítko Ano.
19. Zadejte místo podpisu zmocnění.
20. Klikněte na tlačítko OK.
21. Zavřete stránku.

## <a name="create-a-free-text-invoice-with-mandate"></a>Vytvoření volné faktury se zmocněním
1. Přejděte na Pohledávky > Faktury > Všechny volné faktury.
2. Klikněte na položku Nová.
3. Vyberte odběratele, pro kterého jste vybrali zmocnění.
4. V poli ID zmocnění k přímému debetu zadejte nebo vyberte hodnotu.

