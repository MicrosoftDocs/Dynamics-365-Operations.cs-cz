--- 
title: "Nastavení bankovních účtů společnosti pro přímé debety ve formátu ISO20022"
description: "Tato úloha vás provede nastavením informací o bankovním účtu společnosti potřebném pro generování souborů platby dodavatele."
author: mrolecki
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 741d8ddca24e5fe083b4ddf775bb7f2d65a56fee
ms.contentlocale: cs-cz
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-company-bank-accounts-for-iso20022-direct-debits"></a>Nastavení bankovních účtů společnosti pro přímé debety ve formátu ISO20022

[!include[task guide banner](../../includes/task-guide-banner.md)]

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


