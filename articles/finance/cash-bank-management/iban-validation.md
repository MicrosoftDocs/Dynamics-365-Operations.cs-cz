---
title: Správa ověření mezinárodního čísla bankovního účtu (IBAN)
description: Tento článek vysvětluje správu ověření mezinárodního čísla bankovního účtu (IBAN).
author: angelad116
ms.date: 08/24/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 0e64c763cb74362503a3d6dfa184b26df77f30b3
ms.sourcegitcommit: 0b7a034e644f4d93fe55c7baca5a3f89dbe56898
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/14/2022
ms.locfileid: "9151783"
---
# <a name="manage-international-bank-account-number-iban-account-validation"></a>Správa ověření mezinárodního čísla bankovního účtu (IBAN)

[!include [banner](../includes/banner.md)]

Ověření mezinárodního čísla bankovního účtu (IBAN) zvyšuje množství ověření, které se provádí při přidání čísla IBAN k bankovnímu účtu.

Informace o struktuře IBAN jsou uloženy v aplikaci Microsoft Dynamics 365 Finance a automaticky se načtou při prvním použití IBAN na bankovních účtech. Obsahuje délku kódu IBAN počáteční pozice čísla bankovního účtu a směrového čísla, a délku čísla bankovního účtu a směrového čísla.

## <a name="set-up-iban-structures"></a>Nastavení struktur čísla IBAN

1. Přejděte do **Pokladna a banka \> Nastavení \> IBAN struktury**.
2. Všimněte si, že IBAN struktury pro každou zemi nebo oblast byly vytvořeny automaticky.
3. Vyberte tlačítko **Upravit**, pokud je potřeba aktualizovat strukturu pro konkrétní zemi nebo region.
4. Definice struktury budou částí každé nové verze. Lze použít nabídku **Resetovat struktury** pro načtení nejnovějších definic po každé aktualizaci.

## <a name="validate-the-iban-structure-in-a-bank-account"></a>Ověření IBAN struktury v bankovním účtu

1. Přejděte do části **Pokladna a banka \> Bankovní účty \> Bankovní účty**.
2. Vytvořte bankovní účet.
3. Na pevné kartě **Doplňkové informace** zadejte IBAN.

    Pokud délka kódu IBAN neodpovídá délce, která je definována pro každou zemi nebo oblast, dostanete zprávu s upozorněním. Nelze pokračovat, pokud délka čísla IBAN neodpovídá délce určené ve struktuře IBAN.

    Ověření také kontroluje, že číslo bankovního účtu odpovídá části IBAN, která představuje číslo bankovního účtu. Pokud číslo bankovního účtu neodpovídá, dostanete zprávu s upozorněním. Tato zpráva je pouze upozornění. Můžete pokračovat i v případě, že číslo bankovního účtu neodpovídá.

    Ověření také kontroluje, že číslo směrový kód banky odpovídá části IBAN, která představuje směrový kód banky. Směrový kód obsahuje číslo banky a často další pobočku banky. Pokud směrový kód neodpovídá, dostanete zprávu s upozorněním. Tato zpráva je pouze upozornění. Můžete pokračovat i v případě, že směrový kód neodpovídá.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
