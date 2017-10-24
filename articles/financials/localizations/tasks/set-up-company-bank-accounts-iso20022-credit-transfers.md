--- 
title: "Nastavení bankovních účtů společnosti pro převody kreditu ve formátu ISO20022"
description: "Tento postup popisuje způsob nastavení informací o konkrétním bankovním účtu společnosti, které jsou vyžadované pro generování souboru platby."
author: mrolecki
manager: AnnBe
ms.date: 10/24/2016
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
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 1d0eabdfdeb5ed7d0bdb6df87ebdfa0d41e87492
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-company-bank-accounts-for-iso20022-credit-transfers"></a>Nastavení bankovních účtů společnosti pro převody kreditu ve formátu ISO20022

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tento postup popisuje způsob nastavení informací o konkrétním bankovním účtu společnosti, které jsou vyžadované pro generování souboru platby. Můžete nastavit informace požadované ke generování formátu pro převod kreditu ISO 20022, ale v závislosti na formátu mohou být požadovány další informace, jako je ID společnosti nebo kód třídění. 

K vytvoření tohoto postupu jsou použita ukázková data společnosti DEMF.

Toto je druhý z pěti úkolů, které společně popisují proces platby dodavatele pomocí konfigurací elektronického výkaznictví. Tato procedura je určena pro funkci, která byla přidána do aplikace Dynamics 365 for Operations verze 1611.


## <a name="set-up-iban-and-swift-code"></a>Nastavení kódu IBAN a SWIFT
1. Přejděte do části Pokladna a banka > Bankovní účty.
2. Použijte rychlý filtr k filtrování v poli Bankovní účet s hodnotou 'DEMF OPER.
3. Kliknutím na tlačítko DEMF OPER otevřete podrobnosti o účtu.
4. Klikněte na položku Upravit.
5. Rozbalte oddíl Další identifikace.
6. Zadejte do pole IBAN hodnotu „DE89370400440532013000“.
7. V poli Kód SWIFT zadejte hodnotu DEUTDEFF.
    * Všimněte si, že pro spoustu formátů platby není požadován SWIFT\BIC, doporučujeme ho však pro bankovní účet zaregistrovat.  
8. Klikněte na položku Uložit.

## <a name="set-up-bank-account-for-the-legal-entity"></a>Nastavení bankovního účtu pro právnickou osobu
1. Přejděte do části na Správa organizace > Organizace > Právnické osoby.
2. Klikněte na položku Upravit.
3. Rozbalte část informací o bankovním účtu.
4. V poli Bankovní účet zadejte nebo vyberte hodnotu.
5. Klikněte na položku Uložit.


