---
title: Nastavení bankovních účtů odběratelů a zákazníků pro přímé debety ve formátu ISO20022
description: Tato úloha vás provede nastavením bankovního účtu odběratele a zmocněním k přímému debetu odběratele, které jsou požadovány pro generování souboru plateb odběratele pro přímý debet ISO20022.
author: mrolecki
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustTable, CustBankAccounts, CustDirectDebitMandate, BankAccountTableLookUp,  LogisticsAddressCityLookup
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 595e89faa1e24ca937d399994e15ce53e3f5308b1c6fd7f43e4e831e70c15ad8
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6736860"
---
# <a name="set-up-customers-and-customer-bank-accounts-for-iso20022-direct-debits"></a>Nastavení bankovních účtů odběratelů a zákazníků pro přímé debety ve formátu ISO20022

[!include [banner](../../includes/banner.md)]

Tato úloha vás provede nastavením bankovního účtu odběratele a zmocněním k přímému debetu odběratele, které jsou požadovány pro generování souboru plateb odběratele pro přímý debet ISO20022. V závislosti na formátech platby odběratele, které jsou nastavené, mohou být pro odběratele nebo bankovní účet odběratele potřeba další informace, které nejsou zahrnuty v tomto postupu. 

Tento úkol byl vytvořen za použití ukázkových dat společnosti DEMF s primární adresou právnické osoby v Německu.



Toto je čtvrtý z pěti postupů, které společně popisují proces platby odběratele pomocí konfigurací elektronického výkaznictví.


## <a name="set-up-a-customer-bank-account"></a>Nastavení bankovního účtu odběratele
1. Přejděte na Pohledávky > Zákazníci > Všichni odběratelé.
2. Použijte rychlý filtr pro hledání záznamů. V poli Účet můžete například filtrovat pomocí hodnoty „DE-010“.
3. Klikněte na odkaz na vybraném řádku v seznamu.
4. V podokně akcí klikněte na možnost Odběratel.
5. Klikněte na možnost Bankovní účty.
6. Klikněte na položku Nová.
7. Zadejte hodnotu do pole Bankovní účet.
8. Zadejte hodnotu do pole Název.
    * Zadejte například banka EUR.  
9. V poli Bankovní skupiny zadejte nebo vyberte hodnotu.
10. Zadejte hodnotu do pole IBAN.
    * Zadejte například DE36200400000628808808.  
11. V poli Kód SWIFT zadejte hodnotu.
    * Například zadejte COBADEFFXXX.  Všimněte si, že pro spoustu formátů platby není povinný SWIFT\BIC, doporučujeme ho však pro bankovní účet zaregistrovat.  
12. Klikněte na položku Uložit.
13. Zavřete stránku.
14. Klikněte na položku Upravit.
15. Rozbalte položku Výchozí nastavení plateb.
16. V poli Bankovní účet zadejte nebo vyberte hodnotu.

## <a name="add-a-direct-debit-mandate"></a>Přidání zmocnění k přímému debetu
1. Rozbalte část Zmocnění k přímému debetu.
2. Klepněte na možnost Přidat.
3. V poli Bankovní účet věřitele zadejte nebo vyberte hodnotu.
    * Vyberte například DEMF OPER.  
4. Do pole Datum podpisu zadejte datum.
5. Klepnutím na tlačítko Ano dojde k potvrzení aktualizace data.
6. V poli Místo podpisu zadejte nebo vyberte hodnotu.
7. Do pole Očekávaný počet plateb zadejte číslo.
8. Klikněte na tlačítko OK.
9. Klikněte na položku Uložit.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]