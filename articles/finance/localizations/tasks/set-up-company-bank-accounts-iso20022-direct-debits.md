---
title: Nastavení bankovních účtů společnosti pro přímé debety ve formátu ISO20022
description: Tato úloha vás provede nastavením informací o bankovním účtu společnosti potřebném pro generování souborů platby dodavatele.
author: mrolecki
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BankAccountTable, OMLegalEntity, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 319bf71982987296a8270f596f8d2bb518dd1790
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5819449"
---
# <a name="set-up-company-bank-accounts-for-iso20022-direct-debits"></a>Nastavení bankovních účtů společnosti pro přímé debety ve formátu ISO20022

[!include [banner](../../includes/banner.md)]

Tato úloha vás provede nastavením informací o bankovním účtu společnosti potřebném pro generování souborů platby dodavatele. Tento postup používá jako příklad formát přímého debetu ISO 20022. Jiné formáty mohou vyžadovat další informace o nastavení jako ID společnosti nebo Třídicí kód.



Tento úkol byl vytvořen pomocí ukázkových dat společnosti DEMF.



Toto je druhý z pěti postupů, které společně popisují proces platby odběratele pomocí konfigurací elektronického výkaznictví.


## <a name="set-up-the-iban-and-swift-codes"></a>Nastavení kódů IBAN a SWIFT
1. Přejděte do části Pokladna a banka > Bankovní účty.
2. Použijte rychlý filtr k filtrování v poli Bankovní účet s hodnotou 'DEMF OPER.
3. Klikněte na odkaz na vybraném řádku v seznamu.
    * Příklad: kliknutím na DEMF OPER můžete otevřít podrobnosti o bankovním účtu.  
4. Klikněte na položku Upravit.
5. Rozbalte nebo sbalte oddíl Další identifikace.
6. Zadejte hodnotu do pole IBAN.
    * Zadejte například DE89370400440532013000.  
7. V poli Kód SWIFT zadejte hodnotu.
    * Zadejte například DEUTDEFF.    Všimněte si, že pro spoustu formátů platby není povinný SWIFT\BIC, doporučujeme ho však pro bankovní účet zaregistrovat.  
8. Klikněte na položku Uložit.

## <a name="set-up-a-bank-account-for-the-legal-entity"></a>Nastavení bankovního účtu pro právnickou osobu
1. Přejděte do části na Správa organizace > Organizace > Právnické osoby.
2. Klikněte na položku Upravit.
3. Rozbalte nebo sbalte oddíl Informace o bankovním účtu.
4. V poli Bankovní účet kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
5. Klikněte na odkaz na vybraném řádku v seznamu.
    * Příklad: vyberte bankovní účet DEMF OPER.  
6. Klikněte na položku Uložit.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]