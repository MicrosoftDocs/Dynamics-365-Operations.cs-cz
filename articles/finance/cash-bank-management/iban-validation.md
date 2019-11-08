---
title: Správa ověření mezinárodního čísla bankovního účtu (IBAN)
description: Toto téma vysvětluje správu ověření mezinárodního čísla bankovního účtu (IBAN).
author: mikefalkner
manager: aolson
ms.date: 08/24/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 2aaccd7c09d6daf8a237a433cc22ac1bfc3c1541
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/03/2019
ms.locfileid: "2551241"
---
# <a name="manage-international-bank-account-number-iban-account-validation"></a>Správa ověření mezinárodního čísla bankovního účtu (IBAN)

[!include [banner](../includes/banner.md)]

Ověření mezinárodního čísla bankovního účtu (IBAN) zvyšuje množství ověření, které se provádí při přidání čísla IBAN k bankovnímu účtu.

Informace o struktuře kódu IBAN jsou uloženy v aplikaci Microsoft Dynamics 365 Finance. Tyto informace se načtou automaticky, když použijete kód IBAN na bankovní účty poprvé. Obsahuje délku kódu IBAN počáteční pozice čísla bankovního účtu a směrového čísla, a délku čísla bankovního účtu a směrového čísla.

## <a name="set-up-iban-structures"></a>Nastavení struktur čísla IBAN

1. Přejděte do **Pokladna a banka \> Nastavení \> IBAN struktury**.
2. Všimněte si, že IBAN struktury pro každou zemi nebo oblast byly vytvořeny automaticky.
3. Pokud chcete přizpůsobit struktury pro konkrétní zemi nebo region, můžete je upravit.
4. Definice struktury budou částí každé nové verze. Lze použít nabídku **Resetovat struktury** pro načtení nejnovějších definic po každé aktualizaci.

## <a name="validate-the-iban-structure-in-a-bank-account"></a>Ověření IBAN struktury v bankovním účtu

1. Přejděte do části **Pokladna a banka \> Bankovní účty \> Bankovní účty**.
2. Vytvořte bankovní účet.
3. Na pevné kartě **Doplňkové informace** zadejte IBAN.

    Pokud délka kódu IBAN neodpovídá délce, která je definována pro každou zemi nebo oblast, dostanete zprávu s upozorněním. Nelze pokračovat, pokud délka čísla IBAN neodpovídá délce určené ve struktuře IBAN.

    Ověření také kontroluje, že číslo bankovního účtu odpovídá části IBAN, která představuje číslo bankovního účtu. Pokud číslo bankovního účtu neodpovídá, dostanete zprávu s upozorněním. Tato zpráva je pouze upozornění. Můžete pokračovat i v případě, že číslo bankovního účtu neodpovídá.

    Ověření také kontroluje, že číslo směrový kód banky odpovídá části IBAN, která představuje směrový kód banky. Směrový kód obsahuje číslo banky a často další pobočku banky. Pokud směrový kód neodpovídá, dostanete zprávu s upozorněním. Tato zpráva je pouze upozornění. Můžete pokračovat i v případě, že směrový kód neodpovídá.
