---
title: Nastavení bankovních účtů společnosti pro převody kreditu ve formátu ISO20022
description: Tento postup popisuje způsob nastavení informací o konkrétním bankovním účtu společnosti, které jsou vyžadované pro generování souboru platby.
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
ms.openlocfilehash: a3ddcae4a53fffa07bd386174811c12150f2f162
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5819473"
---
# <a name="set-up-company-bank-accounts-for-iso20022-credit-transfers"></a>Nastavení bankovních účtů společnosti pro převody kreditu ve formátu ISO20022

[!include [banner](../../includes/banner.md)]

Tento postup popisuje způsob nastavení informací o konkrétním bankovním účtu společnosti, které jsou vyžadované pro generování souboru platby. Můžete nastavit informace požadované ke generování formátu pro převod kreditu ISO 20022, ale v závislosti na formátu mohou být požadovány další informace, jako je ID společnosti nebo kód třídění. 

K vytvoření tohoto postupu jsou použita ukázková data společnosti DEMF.

Toto je druhý z pěti úkolů, které společně popisují proces platby dodavatele pomocí konfigurací elektronického výkaznictví. Tento postup je určený pro funkci, která byla přidána do Dynamics 365 for Operations verze 1611.


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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]